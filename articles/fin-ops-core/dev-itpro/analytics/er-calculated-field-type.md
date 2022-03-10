---
title: Hesaplanan alan türünün ER veri kaynaklarının parametreleştirilmiş çağrılarını destekleme
description: Bu konu, ER veri kaynakları için Hesaplanan alan türünün nasıl kullanılacağı hakkında bilgi sağlar.
author: NickSelin
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fb09e1ccd4b2be08e43784330adf4092ca25f5a6
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349172"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a>Hesaplanan alan türünün ER veri kaynaklarının parametreleştirilmiş çağrılarını destekleme

[!include [banner](../includes/banner.md)]

Bu konu **Hesaplanan alan** türünü kullanarak Elektronik raporlama (ER) veri kaynağını nasıl tasarlayabileceğinizi açıklamaktadır. Bu veri kaynağı, yürütüldüğünde bu veri kaynağını çağıran bir bağlamada yapılandırılmış olan parametre bağımsız değişkenlerinin değerleriyle denetlenebilecek bir ER ifadesi içerebilir. Bu tür bir veri kaynağının parametreleştirilmiş çağrılarını yapılandırarak, birçok bağlamada tek bir veri kaynağını yeniden kullanabilirsiniz ve böylece, ER model eşlemeleri veya ER biçimlerinde yapılandırılması gereken veri kaynaklarının toplam sayısı azalır. Ayrıca, bakım maliyetlerini ve diğer tüketicilerin kullanım maliyetini azaltan yapılandırılmış ER bileşenini de basitleştirir.

## <a name="prerequisites"></a>Önkoşullar
Bu konudaki örnekleri tamamlamak için şu erişimlere sahip olmanız gerekir:

- Aşağıdaki rollerden birine erişim:

    - Elektronik raporlama geliştirici
    - Elektronik raporlama işlev danışmanı
    - Sistem yöneticisi

- Aşağıdaki rollerden biri için, Finance and Operations ile aynı kiracı için sağlanan Regulatory Configuration Services'a (RCS) erişim:

    - Elektronik raporlama geliştirici
    - Elektronik raporlama işlev danışmanı
    - Sistem yöneticisi

Ayrıca, aşağıdaki dosyaları da indirip yerel olarak depolamalısınız.

| **İçerik**                           | **Dosya adı**                                        |
|---------------------------------------|------------------------------------------------------|
| Örnek ER verisi modeli yapılandırması    | [Parametreleştirilmiş calls.version.1.xml öğrenme modeli](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)     |
| Örnek ER meta verisi yapılandırması      | [Parametreleştirilmiş calls.version.1.xml öğrenmek için meta veri](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |
| Örnek ER model eşleme yapılandırması | [Parametreleştirilmiş calls.version.1.xml öğrenmek için eşleme](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg) |
| Örnek ER biçimi yapılandırması        | [Parametreleştirilmiş calls.version.1.xml öğrenmek için biçimlendirme](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |

## <a name="sign-in-to-your-rcs-instance"></a>RCS kurulumunuzda oturum açın
Bu örnekte, Litware, Inc. adlı örnek şirket için bir yapılandırma oluşturacaksınız. Öncelikle, RCS'de [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md) prosedüründeki adımları tamamlamanız gerekir:

1. Varsayılan panoda **Elektronik raporlama**'yı seçin.
2. **Raporlama yapılandırmaları**'nı seçin.
3. İndirilen yapılandırmaları RCS'de şu sırada içe aktarın: veri modeli, meta veriler, model eşleme, biçim. Her bir ER yapılandırması için aşağıdaki adımları tamamlayın:

    1. **Exchange**'i seçin.
    2. **XML dosyasından yükle**'yi seçin.
    3. Gerekli ER yapılandırması için XML biçimini seçmek için **Gözat**'ı seçin.
    4. **Tamam**'ı seçin.

## <a name="review-the-provided-er-solution"></a>Sağlanan ER çözümünü gözden geçirme

### <a name="review-model-mapping"></a>Model eşlemeyi gözden geçirme

1. Yapıalndırma ağacında, **Parametreli çağrıları öğrenme modeli** öğesini genişletin.
2. **Parametreli çağrıları öğrenmek için eşleme**'yi seçin.
3. **Tasarımcı**’yı seçin.
4. **Tasarımcı**’yı seçin.  
   
    Bu ER model eşlemesi aşağıdakileri yapacak şekilde tasarlanmıştır:

    - **TaxTable** tablosunda bulunan vergi kodlarının lisesini (**Vergi** veri kaynağı) getirmek.
    - **TaxTrans** tablosunda bulunan vergi hareketlerinin listesini (**Hareket** veri kaynağı) getirmek:
    
        - Getirilen hareketlerin (**GR** veri kaynağı) listesini vergi koduna göre gruplandırmak.
        - Her vergi kodu için toplu değerleri izleyen gruplanan hareketler için hesaplama yapmak:

            - Vergi matrahı değerlerinin toplamı.
            - Vergi değerlerinin toplamı.
            - Uygulanan vergi oranının minimum değeri.

    Bu yapılandırmadaki model eşlemesi, bu model için oluşturulan ve Finance and Operations'da yürütülen ER biçimleri için temel veri modelini uygular. Sonuç olarak **Vergi** ve **Gr** veri kaynaklarının içeriği soyut veri kaynakları gibi ER biçimleri için sunulur.

    ![Vergi ve Gr veri kaynaklarını gösteren model eşleme tasarımcısı sayfası.](media/er-calculated-field-type-01.png)

5.  **Model eşleme tasarımcısı** sayfasını kapatın
6.  **Model eşleme** sayfasını kapatın.

### <a name="review-format"></a>Biçimi gözden geçirme

1. Yapıalndırma ağacında, **Parametreli çağrıları öğrenme modeli** öğesini genişletin.
2. **Parametreli çağrıları öğrenmek için biçimlendirme**'yi seçin.
3. **Tasarımcı**’yı seçin. Bu ER biçimi aşağıdakileri yapacak şekilde tasarlanmıştır:

    - XML biçiminde bir vergi beyanı oluşturmak.
    - Vergi beyanında aşağıdaki vergilendirme düzeylerini sunmak: normal, azaltılmış ve yok.
    - Her bir vergilendirme düzeyinde birden çok ayrıntı sunmak ve her düzeyde farklı ayrıntılara sahip olmak.

    ![Biçim tasarımcısı sayfası.](media/er-calculated-field-type-02.png)

4. **Eşleme**'yi seçin.
5. **Model**, **Veri** ve **Özet** öğelerini genişletin. 

    Hesaplanan **Model.Data.Summary.Level** alanı, vergilendirme düzeyi kodunu döndüren ifadeyi içerir (**Normal**, **Azaltılmış**, **Yok** veya **Diğer)**; bu ifade çalışma zamanında **Model.Data.Summary** veri kaynağından elde edilebilecek vergi kodu için metin değeridir.

    ![Parametreli çağrıları öğrenmek için veri modeli modelinin ayrıntılarını gösteren biçim tasarımcısı sayfası.](media/er-calculated-field-type-03.png)

6. **Model**.**Data2** öğesini genişletin.
7. **Model**.**Data2.Summary2** öğesini genişletin.
   
    **Model**.**Data2.Summary2**, **Model.Data.Summary** veri kaynağı hareketi ayrıntılarını vergilendirme düzeyine göre (**Model.Data.Summary.Level** hesaplanan alanı tarafından döndürülen) gruplandırmak ve toplamları hesaplamak üzere yapılandıırlır.

    ![Model.Data2.Summary2 veri kaynağının ayrıntılarını gösteren biçim tasarımcısı sayfası.](media/er-calculated-field-type-04.png)

8. **Model**.**Data2.Level1**, **Model**.**Data2.Level2** ve **Model**.**Data2.Level3.** hesaplanan alanlarını gözden geçirin. Bu hesaplanan alanlar **Model**.**Data2.Summary2** kayıtları listesini filtremek için kullanılır ve yalnızca belirli bir vergilendirme düzeyini temsil eden kayıtları döndürür.
9. **Biçim tasarımcısı** sayfasını kapatın.

## <a name="create-a-derived-format"></a>Türetilmiş biçim oluşturma
Var olan üç alanı kullanmak yerine, gerekli vergilendirme düzeyini filtrelemek için bir hesaplanmış alan ekleyerek sağlanan biçimi geliştirebilirsiniz: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** ve **Model**.**Data2.Level3**. Gerekli vergilendirme düzeyi, bu yeni hesaplanan alanın çağrıldığı yerde belirtilebilir.

1. Yapıalndırma ağacında, **Parametreli çağrıları öğrenme modeli** öğesini genişletin.
2. **Parametreli çağrıları öğrenmek için biçimlendirme**'yi seçin.
3. **Yapılandırma oluştur**'u seçin.
4. **Ad'dan Türet: Parametreli çağrıları öğrenme biçimi, Microsoft** öğesini seçin.
5. **Ad** alanına **Parametreleri çağrıları öğrenme biçimi (özel)** girin.
6. **Yapılandırma oluştur**'u seçin.

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a>Kayıt listesi döndüren parametreli bir hesaplanan alan yapılandırma

### <a name="start-adding-a-new-calculated-field"></a>Yeni hesaplanan alan eklemeye başlama

1. **Tasarımcı**’yı seçin.
2. Tüm biçim öğelerini genişletmek için **Genişlet/Daralt**'ı seçin.
3. **Eşleme**'yi seçin.
4. **Model** öğesini genişletin.
5. **Model.Data2** öğesini seçin.
6. **Ekle**'yi seçin.
7. **İşlevler\\Hesaplanan alan** öğesini seçin.
8. **Ad** alanına, **Düzeyler** yazın.
9. **Formül düzenle**’yi seçin.

### <a name="define-a-parameter-for-adding-a-calculated-field"></a>Hesaplanan alan eklemek için parametre tanımlama

1. **Parametreler**'i seçin.
2. **Yeni**'yi seçin.
3. **Ad** alanına **Vergilendirme Düzeyi** girin.
4. **Tür** alanında **Dize**'yi seçin.

    Parametrenin bağımsız değişkeninin türünü belirtmek için yalnızca temel veri türleri kullanılabilir. Bu nedenle **Kayıt listesi**, **Kayıt** ve **Numaralandırma** türleri bu amaçla kullanılamaz.

    Tek bir hesaplanan alan için belirtilebilecek maksimum parametre sayısı 8'dir.

    ![Parametre veri kaynağı listesi.](media/er-calculated-field-type-05.png)

5. **Tamam**'ı seçin.

Bu parametreyi ekleyerek, bu hesaplanan alanı çağırmak için yerinde olması gereken koşulu belirtirsiniz. Bu hesaplanan alanı çağırdığınızda, **Vergilendirme Düzeyi** parametresinin bağımsız değişkenini **Dize** biçimiyle bir değer olarak belirtmeniz gerekir.

   Yalnızca bir kapsayıcıda bulunan hesaplanan alanlar için parametreler (**Kayıt listesi**, **Kayıt** veya **Kapsayıcı**) tanımladığından emin olun.

   Yapılandırılan parametre, bu hesaplanan alan için veri kaynakları listesinde bulunur. **Veri kaynağı ekle**'yi seçerek parametreyi yapılandırılan ifadeye ekleyebilirsiniz.

   ![Veri kaynağı alanları.](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a>Hesaplanan alan eklemek için ifade tanımlama

1. **Formül** alanına şunu girin: 

    **WHERE(\@.Summary2, \@.Summary2.grouped.Level =**
    
2. Veri kaynakları listesinde **Vergilendirme Düzeyi** parametresini seçin.
3. **Veri kaynağını ekle**'yi seçin.
4. **Formül** alanında, ifadeyi şu şekilde tamamlayın:  

    **WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**

5. **Kaydet**'i seçin.

    ![Veri kaynağı alanı bilgileri.](media/er-calculated-field-type-07.png)

6. **Formül tasarımcısı** sayfasını kapatın.

### <a name="finish-adding-a-new-calculated-field"></a>Yeni hesaplanan alan eklemeyi bitirme

- **Tamam**'ı seçin.

**Biçim Tasarımcısı** sayfasında, yapılandırılmış **Düzeyler** parametreli hesaplanan alanı bir **Dize** bağımsız değişkeni gerektirir.

![Hesaplanan alan düzeylerinin genişletilmiş listesi.](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a>Biçim öğelerini bağlamak için yapılandırılmış hesaplanan alanı kullanma

1. Yapılandırılmış hesaplanan alanı seçmek için **Model.Data2.Levels** öğesini seçin.
2. **Statement.Taxation.Regular** biçim öğesini seçin.
3. **Bağla**'yı seçin.
4. Seçili biçim öğesinin tüm iç içe geçmiş biçim öğelerinde kullanılmakta olan **Level1** veri kaynağının yeni **Levels** veri kaynağıyla değiştirilmesini onaylamak için **Evet**'i seçin.

    Uygulanan bağlama parametreli hesaplanan alan çağrısı olarak oluşturuldu. Varsayılan olarak, bağlı biçim öğesinin adı aşağıdaki koşullarda parametreli hesaplanan alan için bağımsız değişken olarak kullanılır:

      - Hesaplanan alan tek bir parametre kullanacak şekilde yapılandırılır.
      - Bu parametrenin veri türü **Dize** olarak tanımlanır.

    Bağlı biçim öğesinin adı boş olduğunda, bu öğenin veri kaynağı adı uygulanan bağlamada kullanılır.

5. **Statement.Taxation.Reduced** biçim öğesini seçin.
6. **Bağla**'yı seçin.
7. Seçili biçim öğesinin altında tüm iç içe geçmiş biçim öğelerinde kullanılmakta olan **Level2** veri kaynağının yeni **Levels** veri kaynağıyla değiştirilmesini onaylamak için **Evet**'i seçin.
8. **Statement.Taxation.None** biçim öğesini seçin.
9. **Bağla**'yı seçin.
10. Seçili biçim öğesinin altında tüm iç içe geçmiş biçim öğelerinde kullanılmakta olan **Level3** veri kaynağının yeni **Levels** veri kaynağıyla değiştirilmesini onaylamak için **Evet**'i seçin.

   Vergilendirme düzeyini temsil eden XML öğesi için parametreli hesaplanan alanın bağımsız değişkenini belirttiğinizde (örneğin, metin değeri olarak **Model.Data2.Levels("Reduced")**), iç içe geçmiş XML öznitelikleri için aynı işlemi yapmanız gerekmez — bunların bağlamaları, üst düzeyde tanımlanan bağımsız değişken değerini devralır(**Model.Data2.Levels("Reduced").aggregated.Base** değil **Model.Data2.Levels.aggregated.Base**).

Parametreli hesaplanan alanın yinelenen çağrıları desteklenmez.

**Formülü düzenle**'yi seçebilir ve seçili bağlamada parametreli hesaplanan alanın varsayılan olarak uygulanan bağımsız değişkenini değiştirebilirsiniz. Bu bağımsız değişken eksikse, çalışma zamanında hatalara neden olabilir — kullanıcılara, geçerli biçim doğrulandığında böyle bir durumla ilgili bilgi verilir.

![Doğrulama uyarı bildirimi.](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a>Bir kayıt döndüren parametreli bir hesaplanan alan yapılandırma
Parametreli hesaplanan alan bir kayıt döndürdüğünde, öğeleri biçimlendirmek için bu kaydın ayrı alanların bağlamasını desteklemesi gerekir. Bu gibi durumlarda parametreli hesaplanan alanı çağırmak için bir bağımsız değişkenin değerini içeren üst bir bağlama olmaz — bu değerin tek bir kayıt alanı bağlamasında tanımlanması gerekir.

### <a name="start-adding-a-new-calculated-field"></a>Yeni hesaplanan alan eklemeye başlama

1. **Model.Data2** öğesini seçin.
2. **Ekle**'yi seçin.
3. **İşlevler\\Hesaplanan alan** öğesini seçin.
4. **Ad** alanına, **LevelRecord** girin.
5. **Formül düzenle**’yi seçin.

### <a name="define-a-parameter-for-adding-a-calculated-field"></a>Hesaplanan alan eklemek için parametre tanımlama

1. **Parametreler**'i seçin.
2. **Yeni**'yi seçin.
3. **Ad** alanına **Vergilendirme Düzeyi** girin.
4. **Tür** alanında **Dize**'yi seçin.
5. **Tamam**'ı seçin.

### <a name="define-an-expression-for-adding-a-calculated-field"></a>Hesaplanan alan eklemek için ifade tanımlama

1. **Formül** alanına, aşağıdaki ifadeyi girin:  
    
    **FIRSTORNULL(\@.Levels(**

2. **Vergilendirme düzeyi** parametresini seçin.
3. **Veri kaynağını ekle**'yi seçin.
4. **Formül** alanında, ifadenin son şeklini vermek için Adım 1'de girdiğiniz ifadeye **'Taxation Level'))** ekleyin:  
    
    **FIRSTORNULL(\@.Levels('Taxation Level'))**

5. **Kaydet**'i seçin.
6. **Formül tasarımcısı** sayfasını kapatın.

### <a name="finish-adding-a-new-calculated-field"></a>Yeni hesaplanan alan eklemeyi bitirme

-   **Tamam**'ı seçin.

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a>Biçim öğelerini bağlamak için yapılandırılmış hesaplanan alanı kullanma

1. Yapılandırılmış hesaplanan alanı seçmek için **Model.Data2.LevelRecord** öğesini genişletin.
2. Yapılandırılmış hesaplanan alanının **Model.Data2.LevelRecord.aggregated** kapsayıcısını genişletin.
3. **Model.Data2.LevelRecord.aggregated.Base** alanını seçin.
4. **Statement.Taxation.None** biçim öğesini seçin.
5. **Bağlamayı kaldır**'ı seçin.
6. **Statement.Taxation.None.Base** biçim öğesini seçin.
7. **Bağla**'yı seçin.
8. **Formül düzenle**’yi seçin.
9. İfadeyi **Model.Data2.LevelRecord("None").aggregated.Base** olarak değiştirin.

![Güncelleştirilmiş ifade.](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a>Kullanılmayan hesaplanan alanları kaldırma

1. **Model.Data2.Level1** öğesini seçin.
2. **Sil**'i seçin.
3. **Model.Data2.Level2** öğesini seçin.
4. **Sil**'i seçin.
5. **Model.Data2.Level3** öğesini seçin.
6. **Sil**'i seçin.
7. **Kaydet**'i seçin.

  > [!NOTE]
  > Aynı hesaplanan alanını **Model.Data2.Levels** biçim bağlamalarında birkaç kez yeniden kullandınız. Tek bir hesaplanmış alanı kullanmak ve sürdürmek bunu birden çok benzer alan için yapmatan çok daha kolaydır.

8. **Biçim tasarımcısı** sayfasını kapatın.

## <a name="complete-adjusted-version-of-a-derived-format"></a>Türetilmiş biçimin düzenlenmiş sürümünü tamamlama

1. **Sürümler** hızlı sekmesinde, **Durumu değiştir**'i seçin.
2. **Tamamlandı**'yı seçin.

## <a name="export-completed-version-of-a-derived-format"></a>Türetilmiş biçimin tamamlanmış sürümünü dışa aktarma

1. Yapılandırma ağacında **Parametreli çağrıları öğrenmek için biçimlendirme (özel)** öğesini seçin.
2. **Sürümler** hızlı sekmesinde tamamlanan 1.1.1. sürümünü seçin
3. **Döviz**'i seçin.
4. **XML dosyası olarak dışa aktar**'ı seçin.
5. İndirilen yapılandırmayı yerel olarak XML biçiminde depolayın.

## <a name="test-er-formats"></a>ER biçimlerini test etme 
Yapılandırılmış parametreli hesaplanan alanların doğru çalıştığından emin olmak için başlangıç ve geliştirilmiş ER biçimlerini çalıştırabilirsiniz.

### <a name="import-er-configurations"></a>ER yapılandırmaları içe aktarın
**RCS** türünün ER deposunu kullanarak RCS'den gözden geçirilmiş yapılandırmaları içe aktarabilirsiniz. [Düzenleyici Yapılandırma Hizmetleri'nden (RCS) Elektronik raporlama (ER) yapılandırmalarını içe aktarma](rcs-download-configurations.md) konusundaki adımları zaten biliyorsanız yapılandırmaları ortamınıza aktarmak için bu konuda daha önce açıklanan yapılandırılmış ER deposunu kullanın. Aksi halde, şu adımları izleyin:

1. **DEMF** şirketini seçin ve varsayılan panoda **Elektronik raporlama**'yı seçin.
2. **Raporlama yapılandırmaları**'nı seçin.
3. Microsoft Download Center'dan indirilen yapılandırmaları şu sırada içe aktarın: veri modeli, model eşleme, biçim. Her bir ER yapılandırması için aşağıdaki adımları tamamlayın:

    1. **Exchange**'i seçin.
    2. **XML dosyasından yükle**'yi seçin.
    3. XML biçimindeki gerekli ER yapılandırmasını seçmek için **Gözat**'ı seçin.
    4. **Tamam**'ı seçin.

4. **Parametreli çağrıları öğrenmek için biçimlendirme (özel)** biçiminin RCS'den dışa aktarılan tamamlanmış 1.1.1 sürümünü içe aktarın:

    1. **Exchange**'i seçin.
    2. **XML dosyasından yükle**'yi seçin.
    3. Yerel olarak depolanan XML biçimindeki **Parametreli çağrıları öğrenmek için biçimlendime (özel)** dosyasını seçmek için **Gözat**'ı seçin.
    4. **Tamam**'ı seçin.

### <a name="run-er-formats"></a>ER biçimlerini çalıştırma

1. Yapıalndırma ağacında, **Parametreli çağrıları öğrenme modeli** öğesini genişletin.
2. **Parametreli çağrıları öğrenmek için biçimlendirme**'yi seçin.
3. En üst şerittteki **Çalıştır** öğesini seçin.
4. Yerel olarak oluşturulan çıktıyı kaydedin.
5. **Parametreli çağrıları öğrenmek için biçimlendirme (özel)** öğesini seçin.
6. En üst şerittteki **Çalıştır** öğesini seçin.
7. Oluşturulan çıktıyı yerel olarak kaydedin. 
8. Oluşturulan çıktıların içeriğini karşılaştırın.

## <a name="additional-resources"></a>Ek kaynaklar

- [Elektronik raporlamada (ER) formül tasarımcısı](general-electronic-reporting-formula-designer.md)
- [Parametreli HESAPLANAN ALAN veri kaynakları ekleyerek ER çözümleri performansını iyileştirme](er-calculated-field-ds-performance.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]