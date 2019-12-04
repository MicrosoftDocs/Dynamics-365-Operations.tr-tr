---
title: Her tüzel kişilik için belirtilen parametreleri kullanmak için ER biçimlerini yapılandırma
description: Bu konu, Elektronik raporlama (ER) biçimlerini her tüzel kişilik için belirtilen parametreleri kullanacak şekilde nasıl yapılandıracağınızı açıklar.
author: NickSelin
manager: AnnBe
ms.date: 10/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: d32da76ee46ff5293ae8fefb16d251564b6be21a
ms.sourcegitcommit: d6196d83c7b9166ddb4fe43a91e6bd0ad9da2099
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/31/2019
ms.locfileid: "2694258"
---
# <a name="configure-er-formats-to-use-parameters-that-are-specified-per-legal-entity"></a>Her tüzel kişilik için belirtilen parametreleri kullanmak için ER biçimlerini yapılandırma

[!include[banner](../includes/banner.md)]

## <a name="overview"></a>Genel Bakış

Tasarlayacağınız Elektronik raporlama (ER) biçimlerinin çoğunda, kurulumunuzun her bir tüzel kişiliğine özgü bir değer kümesi kullanarak verileri filtrelemelisiniz (örneğin, vergi hareketlerini filtrelemek için bir vergi kodu kümesi). Şu anda, bu tür filtreleme bir ER biçiminde yapılandırıldığında tüzel kişiliğe bağlı değerler (örneğin vergi kodları) ER biçiminin ifadelerinde veri filtreleme kurallarını belirtmek için kullanılır. Bu nedenle, ER biçimi tüzel kişiliğe özgü yapılır ve gerekli raporları oluşturmak için ER biçimini çalıştırmanız gereken her tüzel kişilik için orijinal ER biçiminin türetilmiş kopyalarını oluşturmalısınız. Her türetilmiş ER biçimi; tüzel kişiliğe özgü değerleri içine alacak şekilde düzenlenmeli, orijinal (temel) sürüm güncellendiğinde yeniden yayınlanmalı, bir test ortamından dışa aktarılmalı ve üretim kullanımı için dağıtılması gerektiğinde bir üretim ortamına içe aktarılmalıdır. Bu nedenle, bu tür yapılandırılmış ER çözümünün bakımı çeşitli nedenlerden dolayı oldukça karmaşık ve zaman alıcıdır:

-   Ne kadar çok tüzel kişilik varsa o kadar çok ER biçim yapılandırması korunmalıdır.
-   ER yapılandırmalarının bakımı, iş kullanıcılarının ER bilgisine sahip olmasını gerektirir.

ER uygulamasına özgü parametreler özelliği, yetkili kullanıcıların veri filtrelemelerini bir dizi soyut kurala göre ER biçiminde yapılandırmasına olanak tanır. Bu kurallar kümesi, bir ER biçiminde mevcut olan veri kaynaklarını kullanmak için yapılandırılabilir. İş kullanıcıları daha sonra, karşılık gelen ER biçimi ayarlarına ve ER biçiminin veri kaynakları tarafından erişilecek olan mevcut tüzel kişilik verilerine dayanarak otomatik olarak oluşturulan kullanıcı arabirimini (UI) kullanarak ER çerçevesinin ötesinde gerçek kurallar belirleyebilirler. ER biçimi için belirtilen kurallar kümesi Dynamics 365 Finance (Finance) kurulumunun geçerli tüzel kişiliğinden dışa aktarılabilir. Bu daha sonra, aynı Finance kurulumunun ya da aynı ER biçiminin bir kurallar kümesi olarak farklı bir kurulumun başka bir tüzel kişiliğine içe aktarılabilir.

## <a name="prerequisites"></a>Önkoşullar

Bu konudaki örnekleri tamamlamak üzere aşağıdaki rollerden biri için Finance ile aynı kiracıya sağlanan Regulatory Configuration Services (RCS) kurulumuna erişiminiz olmalıdır:

- Elektronik raporlama geliştirici
- Elektronik raporlama işlev danışmanı
- Sistem yöneticisi

[HESAPLANAN ALAN türüne göre ER veri kaynaklarının parametreli çağrılarını destekleme](er-calculated-field-type.md) konusundaki adımları tamamlamanızı öneririz. Bu adımları zaten tamamladıysanız takip eden **ER yapılandırmalarını RCS'ye içe aktarma** bölümündeki adımları atlayabilirsiniz.

## <a name="import-er-configurations-into-rcs"></a>ER yapılandırmalarını RCS'ye içe aktarma

[Microsoft İndirme Merkezi](https://go.microsoft.com/fwlink/?linkid=851448)'nden **HESAPLANAN ALAN türüne göre ER veri kaynaklarının parametreli çağrılarını destekleme** zip dosyasını indirin. Bu zip dosyası, ayıklanması ve yerel olarak depolanması gereken aşağıdaki ER yapılandırmalarını içerir.

| **İçerik açıklaması**                        | **Dosya adı**                                        |
|------------------------------------------------|------------------------------------------------------|
| Örnek **ER veri modeli** yapılandırma dosyası    | Parametreleştirilmiş calls.version.1.xml öğrenme modeli     |
| Örnek **ER meta verisi** yapılandırma dosyası      | Parametreleştirilmiş calls.version.1.xml öğrenmek için meta veri  |
| Örnek **ER model eşlemesi** yapılandırma dosyası | Parametreleştirilmiş calls.version.1.xml öğrenmek için eşleme |
| Örnek **ER biçimi** yapılandırması             | Parametreleştirilmiş calls.version.1.xml öğrenmek için biçimlendirme  |

Ardından, RCS kurulumunuzda oturum açın.

Bu örnekte, Litware, Inc. örnek şirketi için bir yapılandırma oluşturacaksınız. Bu prosedürü tamamlamadan önce RCS'deki [Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md) konusundaki adımları tamamlamanız gerekir.

1.  Varsayılan panoda **Elektronik raporlama**'yı seçin.
2.  **Raporlama yapılandırmaları**'nı seçin.
3.  Daha önce indirdiğiniz ER yapılandırmalarını aşağıdaki sırayla RCS'ye içe aktarın: veri modeli, meta veriler, model eşleme ve biçim. Her bir ER yapılandırması için aşağıdaki adımları izleyin:

    1.  **Döviz**'i seçin.
    2.  **XML dosyasından yükle**'yi seçin.
    3.  Gerekli ER yapılandırması için XML biçimindeki dosyayı seçmek üzere **Gözat**'ı seçin.
    4.  **Tamam**'ı seçin.

## <a name="review-the-er-solution-that-is-provided"></a>Sağlanan ER çözümünü gözden geçirme

1.  Yapılandırma ağacında, **Parametreli çağrıları öğrenme modeli** öğesinin içeriğini genişletin.
2.  **Parametreli çağrıları öğrenmek için biçimlendirme** öğesini seçin.
3.  **Tasarımcı**’yı seçin.
4.  **Genişlet/Daralt**'ı seçin.

    **Parametreli çağrıları öğrenmek için biçimlendirme** ER biçimi, çeşitli vergilendirme düzeylerini (normal, azaltılmış ve yok) sunan XML biçiminde bir vergi beyannamesi oluşturmak için tasarlanmıştır. Her düzey farklı ayrıntılara sahiptir.

    ![ER İşlem tasarımcısı sayfası](./media/RCS-AppSpecParms-ReviewFormat.PNG)

5.  **Eşleme** sekmesinde **Model**, **Veri** ve **Özet** öğelerini genişletin.

    **Model. Data. Summary** veri kaynağı, vergi hareketleri listesini döndürür. Bu hareketler vergi koduna göre özetlenir. Bu veri kaynağı için **Model.Data.Summary.Level** hesaplanan alanı, her özetlenen kaydın vergilendirme düzeyine ilişkin kodu döndürecek şekilde yapılandırılmıştır. Çalışma zamanında **Model.Data.Summary** veri kaynağından alınabilecek herhangi bir vergi kodu için hesaplanan alan vergilendirme düzeyi kodunu (**Normal**, **Azaltılmış**, **Yok** veya **Diğer**) metin değeri olarak döndürür. **Model.Data.Summary.Level** hesaplanan alanı, **Model.Data.Summary** veri kaynağının kayıtlarını filtrelemek ve **Model.Data2.Level1**, **Model.Data2.Level2** ve **Model.Data2.Level3** alanlarını kullanarak vergilendirme düzeyini temsil eden her XML öğesinde filtrelenmiş verileri girmek için kullanılır.

    ![ER İşlem tasarımcısı sayfası](./media/RCS-AppSpecParms-ReviewFormat-Data2Fld.PNG)

    **Model.Data.Summary.Level** hesaplanan alanı bir ER ifadesi içerecek şekilde yapılandırılmıştır. Vergi kodlarının (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD** ve **InVAT0**) bu yapılandırmaya sabit kodlandığını unutmayın. Bu nedenle, bu ER biçimi belirtilen vergi kodlarının yapılandırıldığı tüzel kişiliğe bağlıdır.

    ![ER İşlem tasarımcısı sayfası](./media/RCS-AppSpecParms-ReviewFormat-LevelFld.PNG)

    Her tüzel kişiliğe ait farklı vergi kodları kümesini desteklemek için aşağıdaki adımları izlemelisiniz:

    - Her tüzel kişilik için ER biçiminin türetilmiş bir sürümünü oluşturun.
    - Tüzel kişilik ayarını temel alarak **Model.Data.Summary.Level** hesaplanan alanındaki vergi kodlarını güncelleştirin.

6.  **Biçim tasarımcısı** sayfasını kapatın.

## <a name="create-a-derived-format"></a>Türetilmiş biçim oluşturma

Ardından, her tüzel kişilik için farklı bir vergi kodu setini tek bir ER biçiminde desteklemek için ER uygulamasına özgü parametreler özelliğini kullanacaksınız.

1.  Yapılandırma ağacında, **Parametreli çağrıları öğrenme modeli** öğesinin içeriğini genişletin.
2.  **Parametreli çağrıları öğrenmek için biçimlendirme** öğesini seçin.
3.  **Yapılandırma oluştur**'u seçin.
4.  **Ad'dan Türet: Parametreli çağrıları öğrenme biçimi, Microsoft** seçeneğini belirleyin.
5.  **Ad** alanına **LE verilerinin nasıl aranacağını öğrenmek için biçimlendirme** yazın.
6.  **Yapılandırma oluştur**'u seçin.

## <a name="configure-a-derived-format"></a>Türetilmiş biçim yapılandırma

### <a name="add-a-format-enumeration"></a>Biçim numaralandırması ekleme

Ardından, yeni bir ER biçim numaralandırması ekleyeceksiniz. Bu biçim numaralandırma değerleri, ER biçiminde kullanılan çeşitli vergilendirme düzeyleri için tüzel kişiliğe bağlı vergi kodu setlerini belirten iş kullanıcılarına sunulur.

1.  **Tasarımcı**’yı seçin.
2.  **Biçim numaralandırmaları**'nı seçin.
3.  **Ekle**'yi seçin.
4.  **Ad** alanına **Vergilendirme düzeyleri listesi** yazın.
5.  **Kaydet**'i seçin.
6.  **Biçim numaralandırması değerleri** sekmesinde **Ekle**'yi seçin.
7.  **Ad** alanına **Normal vergilendirme** yazın.
8.  Yeniden **Ekle**'yi seçin.
9.  **Ad** alanına **Azaltılmış vergilendirme** yazın.
10. Yeniden **Ekle**'yi seçin.
11. **Ad** alanına **Vergilendirme yok** yazın.
12. Yeniden **Ekle**'yi seçin.
13. **Ad** alanına, **Diğer** yazın.

    ![ER İşlem tasarımcısı sayfası](./media/RCS-AppSpecParms-ConfigureFormat-Enum.PNG)

    İş kullanıcıları, tüzel kişiliğe bağlı vergi kodu kümelerini belirlemek için farklı dilleri kullanabileceğinden, bu numaralandırma değerlerini Finance'taki kullanıcılar için tercih edilen dil olarak yapılandırılmış dillere çevirmenizi öneririz.

14. **Vergilendirme yok** kaydını seçin.
15. **Etiket** alanına tıklayın.
16. **Çevir**'i seçin.
17. **Metin çevirisi** bölmesinde, **Etiket Kodu** alanına **LBL_LEVELENUM_NO** yazın.
18. **Varsayılan dilde metin** alanına **Vergilendirme yok** yazın.
19. **Dil** alanında, **DE**'yi seçin.
20. **Çevrilen metin** alanına, **keine Besteuerung** yazın.
21. **Çevir**'i seçin.

    ![ER İşlem tasarımcısı sayfası](./media/RCS-AppSpecParms-ConfigureFormat-EnumTranslate.PNG)

22. **Kaydet**'i seçin.
23. **Biçim numaralandırmaları** sayfasını kapatın.

### <a name="add-a-new-lookup-data-source"></a>Yeni bir veri kaynağı araması ekleme

Ardından, iş kullanıcılarının özetlenen her hareket kaydı için doğru vergilendirme düzeyini tanıyacak şekilde tüzel kişiliğe bağlı kuralları nasıl belirteceğini belirlemek için yeni bir veri kaynağı ekleyeceksiniz.

1.  **Eşleme** sekmesinde **Ekle**'yi seçin.
2.  **Biçim numaralandırması\Arama**'yı seçin.

    Az önce, iş kullanıcılarının vergilendirme düzeyi kabulü için belirlediği her kuralın bir ER biçim numaralandırması değeri döndüreceğini tanımladınız. **Biçim numaralandırma** bloğuna ek olarak, **Arama** veri kaynağı türüne **Veri modeli** ve **Dynamics 365 for Operations** blokları altından erişilebildiğine dikkat edin. Bu nedenle, ER veri modeli numaralandırmaları ve uygulama numaralandırmaları, bu tür veri kaynakları için döndürülen değer türlerini belirtmek için kullanılabilir.
    
3.  **Ad** alanına, **Seçici** yazın.
4.  **Biçim numaralandırma** alanında, **Vergilendirme düzeyleri listesi**'ni seçin.

    Az önce, bu veri kaynağında belirtilen her kural için bir iş kullanıcısının, **Vergilendirme düzeyleri listesi** biçim numaralandırma değerlerinden birini, döndürülen değer olarak seçmesi gerektiğini belirlediniz.
    
5.  **Aramayı düzenle**'yi seçin.
6.  **Sütunlar**'ı seçin.
7.  **Model** öğesini genişletin.
8.  **Veri** öğesini genişletin.
9.  **Vergi** öğesini genişletin.
10. **Model.Data.Tax.Code** öğesini seçin.
11. **Ekle** düğmesini (sağ ok) seçin.

    ![ER İşlem tasarımcısı sayfası](./media/RCS-AppSpecParms-ConfigureFormat-Lookup1.PNG)

    Az önce, vergilendirme düzeyinin kabulünde bu veri kaynağında belirtilen her kural için iş kullanıcısının bir koşul olarak vergi kodlarından birini seçmesi gerektiğini belirttiniz. İş kullanıcısının seçebileceği vergi kodlarının listesi **Model.Data.Tax** veri kaynağı tarafından döndürülür. Bu veri kaynağı **Ad** alanını içerdiğinden iş kullanıcılarına sunulan aramadaki her vergi kodu değeri için vergi kodunun adı gösterilir.
    
12. **Tamam**'ı seçin.

    ![ER İşlem tasarımcısı sayfası](./media/RCS-AppSpecParms-ConfigureFormat-Lookup2.PNG)

    İş kullanıcıları, bu veri kaynağının kayıtları olarak birden fazla kural ekleyebilir. Her kayıt bir satır koduyla numaralandırılır. Kurallar artan satır numarasına göre değerlendirilir.

    **Vergi kodu** alanını bu arama veri kaynağındaki kurallar için bir koşul olarak seçtiğiniz ve **Vergi kodu**, **Dize** veri türünün bir alanı olarak ayarlandığı için her kural, veri kaynağına iletilen vergi kodu ile veri kaynağının bu kaydında tanımlanan vergi kodu karşılaştırılarak çalışma zamanında değerlendirilir.

    Yapılandırılmış koşulu sağlayan bir kural bulunduğunda bu veri kaynağı **Arama sonucu** alanında tanımlanan kuralın arama değerini döndürür. Herhangi bir kural bulunmazsa kullanıcıya mevcut veri kaynağının doğru bir değer veremediğini bildirmek için bir özel durum oluşturulur.

13. **Kaydet**'i seçin.
14. **Arama tasarımcısı** sayfasını kapatın.
15. **Tamam**'ı seçin.

    Veri kaynağına **Dize** veri türünün **Kod** parametresinin bağımsız değişkeni olarak iletilen herhangi bir vergi kodu için vergilendirme düzeyini **Vergilendirme düzeyleri listesi** biçimindeki numaralandırma değeri olarak döndürecek yeni bir veri kaynağı eklediğinizi unutmayın.
    
    ![ER İşlem tasarımcısı sayfası](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld.PNG)

    Yapılandırılmış kuralların değerlendirilmesinin, bu kuralların koşullarını tanımlamak için seçilen alanların veri türüne bağlı olduğunu unutmayın. **Sayısal** veya **Tarih** veri türünün bir alanı olarak yapılandırılmış bir alan seçtiğinizde ölçütler daha önce **Dize** veri türü için açıklanan ölçütlerden farklı olur. **Sayısal** ve **Tarih** alanları için kuralın bir değer aralığı olarak belirtilmesi gerekir. Veri kaynağına iletilen bir değer yapılandırılmış aralıkta olduğunda kuralın koşulu yerine getirilmiş sayılır.
    
    Aşağıdaki çizim, bu tür bir ayarın örneğini gösterir. **String** veri türünün **Model.Data.Tax.Code** alanına ek olarak **Gerçek** veri türünün **Model.Tax.Summary.Base** alanı, bir arama veri kaynağının koşullarını belirtmek için kullanılır.
    
    ![ER İşlem tasarımcısı sayfası](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld2.PNG)

    Bu arama veri kaynağı için **Model.Data.Tax.Code** ve **Model.Tax.Summary.Base** alanları seçildiğinden, bu veri kaynağının her kuralı aşağıdaki şekilde yapılandırılır:
    
    -   Sunulan listede **Vergilendirme düzeyleri listesi** biçim numaralandırma değeri, döndürülen bir değer olarak seçilmelidir.
    -   Vergi kodu, bu kuralın bir koşulu olarak girilmelidir. Yalnızca **Model.Data.Tax** veri kaynağı tarafından sağlanan vergi kodları geçerlidir.
    -   Vergi matrahının minimum ve maksimum değerleri bu kuralın şartları olarak girilmelidir.

    Aşağıda bu veri kaynağının her kuralının çalışma zamanında nasıl değerlendirileceği verilmiştir:
    -   Bu veri kaynağına iletilen **Dize** veri türünün kodu, bir kuralın vergi koduna eşit mi?
    -   Bu veri kaynağına iletilen **Gerçek** veri türünün değeri, belirli minimum ve maksimum değerler arasında mı?

    Bir kural, her iki koşul da sağlandığında geçerli sayılır.

### <a name="translate-the-label-of-the-lookup-data-source-that-was-added"></a>Eklenen arama veri kaynağının etiketini çevirme

İş kullanıcıları, tüzel kişiliğe bağlı vergi kodu kümelerini belirlemek için farklı diller kullanabileceğinden eklediğiniz arama veri kaynağının etiketini çevirmenizi öneririz; böylece etiket, ilgili sayfada her kullanıcının tercih ettiği dilde gösterilir.

1.  **Model.Data.Selector** veri kaynağını seçin.
2.  **Düzenle** öğesini seçin.
3.  **Etiket** alanına tıklayın.
4.  **Çevir**'i seçin.
5.  **Metin çevirisi** bölmesinde, **Etiket Kodu** alanına **LBL_SELECTOR_DS** yazın.
6.  **Varsayılan dilde metin** alanına **Vergi koduyla vergi düzeyini seçme** yazın.
7.  **Dil** alanında, **DE**'yi seçin.
8.  **Çevrilmiş metin** alanına **Steuerebene für Steuerkennzeichen auswählen** yazın.
9.  **Çevir**'i seçin.
10. **Tamam**'ı seçin.

    ![ER İşlem tasarımcısı sayfası](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFldTranslate.PNG)

### <a name="add-a-new-field-to-consume-the-configured-lookup"></a>Yapılandırılmış aramayı kullanmak için yeni bir alan ekleme

1.  **Model.Data** öğesini genişletin.
2.  **Model.Data.Summary** öğesini seçin.
3.  **Ekle**'yi seçin.
4.  **İşlevler/Hesaplanan alan** öğesini seçin.
5.  **Ad** alanına **LevelByLookup** yazın.
6.  **Formül düzenle**’yi seçin.
7.  **Formül alanı**'na **Model.Selector(Model.Data.Summary.Code)** yazın.
8.  **Kaydet**'i seçin.

    ![ER İşlem tasarımcısı sayfası](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld.PNG)

9.  **Formül düzenleyici** sayfasını kapatın.
10. **Tamam**'ı seçin.

    ![ER İşlem tasarımcısı sayfası](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld2.PNG)

    Eklediğiniz **LevelByLookup** hesaplanan alanın vergilendirme düzeyini, özetlenen her vergi hareketi kaydı için **Vergilendirme düzeyleri listesi** biçimi numaralandırmasının değeri olarak döndüreceğini unutmayın. Kaydın vergi kodu **Model.Selector** arama veri kaynağına geçirilir ve bu veri kaynağı için kurallar, doğru vergilendirme düzeyini seçmek için kullanılır.

### <a name="add-a-new-format-enumeration-based-data-source"></a>Yeni bir biçim numaralandırması tabanlı veri kaynağı ekleme

Ardından, daha önce eklediğiniz biçim numaralandırmasını ifade eden yeni bir veri kaynağı ekleyeceksiniz. Bu veri kaynağının değerleri daha sonra bir ER biçimi ifadesinde kullanılır.

1.  **Kök ekle**'yi seçin.
2.  **Biçim numaralandırması\Numaralandırma**'yı seçin.
3.  **Ad** alanına **TaxationLevel** yazın.
4.  **Biçim numaralandırma** alanında, **Vergilendirme düzeyleri listesi**'ni seçin.
5.  **Kaydet**'i seçin.

### <a name="modify-an-existing-field-to-start-to-use-the-lookup"></a>Aramayı kullanmaya başlamak için var olan bir alanı değiştirme

Ardından var olan hesaplanan alanı, vergi koduna bağlı olarak doğru vergilendirme düzeyi değerini döndürmek için yapılandırılmış arama veri kaynağını kullanacak şekilde değiştireceksiniz.

1.  **Model.Data.Summary.Level** öğesini seçin.
2.  **Düzenle** öğesini seçin.
3.  **Formül düzenle**’yi seçin.

    **Model.Data.Summary.Level** alanının geçerli ifadesinin aşağıdaki sabit kodlanmış vergi kodlarını içerdiğini unutmayın:
    
    CASE (@.Code, "VAT19", "Regular", "InVAT19", "Regular", "VAT7", "Reduced", "InVAT7", "Reduced", "THIRD", "None", "InVAT0", "None", "Other")

4.  **Formül** alanına **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Regular", TaxationLevel.'Reduced taxation', "Reduced", TaxationLevel.'No taxation', "None", "Other")** yazın.

    ![ER İşlem tasarımcısı sayfası](./media/RCS-AppSpecParms-ConfigureFormat-ChangeLookupFld.PNG)
    
    **Model.Data.Summary.Level** alanına ait ifadenin artık geçerli kaydın vergi koduna göre vergilendirme düzeyini ve bir iş kullanıcısının **Model.Data.Selector** arama veri kaynağında yapılandırdığı kurallar kümesini döndüreceğini unutmayın.
    
5.  **Kaydet**'i seçin.
6.  **Formül tasarımcısı** sayfasını kapatın.
7.  **Tamam**'ı seçin.
8.  **Kaydet**'i seçin.
9.  **Biçim tasarımcısı** sayfasını kapatın.

## <a name="complete-the-draft-version-of-a-derived-format"></a>Türetilmiş biçimin taslak sürümünü tamamlama

1.  **Sürümler** hızlı sekmesinde **Durumu değiştir**'i seçin.
2.  **Tamamlandı**'yı seçin.
3.  **Tamam**'ı seçin.

## <a name="export-completed-version-of-modified-format"></a>Değiştirilmiş biçimin tamamlanmış sürümünü dışa aktarma

1.  Yapılandırma ağacında **LE verilerinin nasıl aranacağını öğrenmek için biçimlendirme** öğesini seçin.
2.  **Sürümler** hızlı sekmesinde durumu **Tamamlandı** olan kaydı seçin.
3.  **Döviz**'i seçin.
4.  **XML dosyası olarak dışa aktar**'ı seçin.
5.  **Tamam**'ı seçin.
6.  Web tarayıcısı bir **LE verilerinin nasıl aranacağını öğrenmek için biçimlendirme.xml** dosyası indirir. Bu dosyayı yerel olarak depolayın.

**LE verilerinin nasıl aranacağını öğrenmek için biçimlendirme** öğesinin üst öğeleri için bu bölümdeki adımları tekrarlayın ve aşağıdaki dosyaları yerel olarak depolayın:

-   Parametreli çağrıları öğrenmek için biçimlendirme.xml
-   Parametreli çağrıları öğrenmek için eşleme.xml
-   Parametreli çağrıları öğrenme modeli.xml

Vergi hareketlerini farklı vergilendirme düzeylerine göre filtrelemek üzere tüzel kişiliğe bağlı vergi kodları kümeleri oluşturmak üzere yapılandırılmış **LE verilerinin nasıl aranacağını öğrenmek için biçimlendirme** ER biçimini nasıl kullanacağınızı öğrenmek için [Her tüzel kişilik için ER biçiminin parametrelerini ayarlama](er-app-specific-parameters-set-up.md) konusundaki adımları tamamlayın.

## <a name="additional-resources"></a>Ek kaynaklar

[Elektronik raporlamada formül tasarımcısı](general-electronic-reporting-formula-designer.md)

[Her tüzel kişilik için ER biçiminin parametrelerini ayarlama](er-app-specific-parameters-set-up.md)
