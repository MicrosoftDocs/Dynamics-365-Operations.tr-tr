---
title: ER veri modellerinin parametreli çağrılarını destekleme
description: Bu makalede, elektronik raporlama (ER) veri modelleri için parametre haline getirilmiş çağrıların nasıl uygulanacağını açıklanmaktadır.
author: kfend
ms.date: 03/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-10-01
ms.dyn365.ops.version: 10.0.15
ms.custom: ''
ms.assetid: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula, ERDataModelDesigner
ms.openlocfilehash: 5be189c19d963991ec012de189bbf7b721b88fef
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276003"
---
# <a name="support-parameterized-calls-of-er-data-models"></a>ER veri modellerinin parametreli çağrılarını destekleme

[!include [banner](../includes/banner.md)]

İş belgeleri oluşturmak için, aşağıdaki ER bileşenlerini içeren bir [Elektronik raporlama (ER)](general-electronic-reporting.md) çözümü konfigüre edin:

- **[Biçim](er-overview-components.md#format-component)** – Bu bileşen, bir iş belgesinin yapısını belirtir.
- **Biçim eşlemesi** – Bu bileşen, çalışma zamanında bir iş belgesinin nasıl doldurulacağını denetler.
- **[Model eşleme](er-overview-components.md#model-mapping-component)** – Bu bileşen, verilerin uygulamadan neleri biçim eşlemesine çekeceğini belirler.
- **[Veri modeli](er-overview-components.md#data-model-component)** – Bu bileşen, bağımsız bileşenler arasında bilgi geçirir.

Bir ER biçimi çalıştırdığınızda, her biçim öğesi kök biçim öğesinden başlayarak çalıştırılır. Çalıştırılan bir biçim öğesinde [veri kaynağı](general-electronic-reporting.md#configuring-data-model-mappings-for-outgoing-documents) bağlantısı bulunduğunda veri kaynağı, beklenilen verileri teslim edecek şekilde çalıştırılır ve biçim öğesini doldurmak için kullanır. *Model* türünün bir veri kaynağı çağrıldığında, model eşleme ayarları temel alınarak verileri uygulamadan dışarı çekmek için uygun model eşleme çağrılır.

Daha önce, bu model eşleme çağrıları, çalıştırılan biçimin mantığına bağlı hale getirmek için parametreleştirilemezdi. Yalnızca aşağıdaki veri akışı desteklenirdi.

<table>
<tbody>
<tr align="center">
<td>
<b>Biçim</b><br>
Biçim&nbsp;öğesi<br>
&nbsp;
</td>
<td>
<i>Bağlama</i><br>
&gt;&nbsp;istek&nbsp;&gt;<br>
&lt;&nbsp;değer&nbsp;&lt;
</td>
<td><b>Biçim&nbsp;eşleme</b><br>
Veri kaynağı<br>
&nbsp;
</td>
<td>
<i>Veri&nbsp;modeli</i><br>
&gt;&nbsp;istek&nbsp;&gt;<br>
&lt;&nbsp;değer&nbsp;&lt;
</td>
<td>
<b>Model&nbsp;eşleme</b><br>
Veri&nbsp;kaynağı<br>
&nbsp;
</td>
<td>
<i>Bağlama</i><br>
&gt;&nbsp;istek&nbsp;&gt;<br>
&lt;&nbsp;değer&nbsp;&lt;
</td>
<td>
<b>Tablo</b><br>
Kaydet<br>
Alan
</td>
</tr>
</tbody>
</table>

Ancak, sürüm 10.0.15 ve sonrasında çağrılabilecek olan veri modeli alanlarını yalnızca yapılandırılan parametrelerin değerleri sağlandığında konfigüre edebilirsiniz. Böyle bir alan bir biçim bileşeninden konfigüre edildiğinde ve çağrıldığında, çağrının bağımsız değişkenleri olarak, gerekli parametrelerin bir biçim bağlamasında sağlanması gerekir. Bu durumlarda bağımsız değişkenlerin değerleri formata özgü değerlere göre belirtilebilir. Bu nedenle, aşağıdaki veri akışını desteklemek üzere veri modeli çağrıları için **dinamik çalışma zamanı parametreleştirmesini** kullanabilirsiniz.

<table>
<tbody>
<tr align="center">
<td>
<b>Biçim</b><br>
Biçim&nbsp;öğesi&nbsp;1<br>
<br>
Biçim&nbsp;öğesi&nbsp;2<br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>Bağlama</i><br>
&gt;&nbsp;istek&nbsp;1&nbsp;&gt;<br>
&lt;&nbsp;değer&nbsp;1&nbsp;&lt;<br>
&gt;&nbsp;istek&nbsp;2&nbsp;&gt;<br>
&lt;&nbsp;değer&nbsp;3&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>Biçim&nbsp;eşleme</b><br>
Veri&nbsp;kaynağı&nbsp;1<br>
&nbsp;<br>
<b>value2=Func(value1)</b><br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>Veri&nbsp;modeli</i><br>
&gt;&nbsp;field1&nbsp;&gt;<br>
&lt;&nbsp;değer&nbsp;1&nbsp;&lt;<br>
<b>&gt;&nbsp;field2(value2)&nbsp;&gt;</b><br>
&lt;&nbsp;değer&nbsp;3&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>Model&nbsp;eşleme</b><br>
Veri&nbsp;kaynağı&nbsp;1<br>
<br>
Veri&nbsp;kaynağı&nbsp;2<br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>Bağlama</i><br>
&gt;&nbsp;istek&nbsp;1&nbsp;&gt;<br>
&lt;&nbsp;değer&nbsp;1&nbsp;&lt;<br>
&gt;&nbsp;istek&nbsp;2&nbsp;&gt;<br>
&lt;&nbsp;değer&nbsp;3&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>Tablo&nbsp;1</b><br>
Kayıt&nbsp;1<br>
Alan&nbsp;1<br>
<b>Tablo&nbsp;2</b><br>
Kayıt&nbsp;2<br>
Alan&nbsp;2
</td>
</tr>
</tbody>
</table>

Yeni işlevsellik, [*Kayıt*](er-formula-supported-data-types-composite.md#record) veya [*Kayıt listesi*](er-formula-supported-data-types-composite.md#record-list) türünün herhangi bir veri modeli alanına çağrı parametreleştirmenizi sağlar. Veri modeli alanının parametreleri için aşağıdaki veri türleri desteklenir:

- [Boole](er-formula-supported-data-types-primitive.md#boolean)
- [Konteyner](er-formula-supported-data-types-composite.md#container)
- [Date](er-formula-supported-data-types-primitive.md#date)
- [Tarih/Saat](er-formula-supported-data-types-primitive.md#datetime)
- [GUID](er-formula-supported-data-types-primitive.md#guid)
- [Int64](er-formula-supported-data-types-primitive.md#int64)
- [Tamsayı](er-formula-supported-data-types-primitive.md#integer)
- [Gerçek](er-formula-supported-data-types-primitive.md#real)
- [Dize](er-formula-supported-data-types-primitive.md#string)

Bir veri modeli alanının her parametresini, tanımlı veri türünün tek değeri ve bu tür değerlerin [*listesi*](er-formula-supported-data-types-composite.md#record-list) olarak sağlanabileceği şekilde belirtebilirsiniz.

> [!NOTE]
> Veri modeli alanının parametresi için varsayılan değer desteklenmez. Veri modelindeki bir alana parametre eklerseniz ve bu veri modelinin sürümü zaten serbest bırakılmış ve yayımlanmışsa, bu veri modeli değişikliği geriye dönük olarak uyumlu olmadığından, ilgili tüm model eşlemelerini ve biçimlerini bu modelin yeni sürümüne yeniden [temellendirmelisiniz](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase).

Model eşleme çağrılarını formata özgü olarak yapmak için parametreleştirilmiş veri modeli alanları konfigüre edebilirsiniz. Bu yaklaşım, tek bir veri modelinin birçok biçimi için yapılandırılması gereken model eşleme sayısını azaltmada size yardımcı olabilir. Bu yaklaşımı, biçimlendirlerinizin yürütme performansını artırmak ve iş belgelerini oluşturmak için gereken zamanı azaltmak için de kullanabilirsiniz. Bu özellik hakkında daha fazla bilgi edinmek için bu makaledeki örneği tamamlayın.

## <a name="example-use-parameterized-calls-of-er-data-models"></a>Örnek: ER veri modellerinin parametreli çağrılarını kullanma

Aşağıdaki adımlarda, Sistem Yöneticisi veya Elektronik Raporlama Geliştirici rolündeki bir kullanıcının, çağrı için bağımsız değişken sağlayarak çalışma zamanında hesaplanan bir değer olan bir veri modelini, model eşlemeyi ve bir biçim ER bileşenini içeren bir ER çözümünü çalışan biçimin formülü kullanılarak nasıl tasarlayabileceği açıklanır. 

Bu adımlar **DEMF** şirketinde gerçekleştirilebilir. Kod değişikliği yapılması gerekmez. 

Bu örnekte, **Litware, Inc.** örnek şirketi için gerekli ER [yapılandırmalarını](general-electronic-reporting.md#Configuration) oluşturacaksınız. **Litware, Inc.** (`http://www.litware.com`) örnek şirketinin yapılandırma sağlayıcısının ER çerçevesinde listelendiğinden ve **Etkin** olarak işaretlendiğinden emin olun. Bu yapılandırma sağlayıcısı listede yoksa veya **Etkin** olarak işaretli değilse [Bir yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md) konusundaki adımları izleyin.

### <a name="business-scenario"></a>İş senaryosu

Denetim amacıyla elektronik bir belge oluşturmak için çalıştırabileceğiniz bir biçim içeren bir ER çözümünüz var. Bu biçim, satış siparişleri ve satınalma siparişleriyle ilgili vergi hareketlerini ve hareket tarihi ve vergi değeri gibi gerekli ayrıntıları içerir. Yeni mali yıl itibariyle bu belgenin yapısı değişti. Artık oluşturulan raporlarda hareketleri sunulan tüm tarafların (müşteriler ve satıcılar) ek ayrıntılarını içeren genişletilmiş bir belge göndermeniz gerekir. Bu nedenle, ER çözümünüzü bu yeni gereksinimle uyumlu belgeler oluşturacak şekilde değiştirmelisiniz.

### <a name="configure-the-er-framework"></a>ER altyapısını yapılandırma

En az ER parametre kümesini ayarlamak için [ER altyapısını yapılandırma](er-quick-start2-customize-report.md#ConfigureFramework) bölümündeki adımları izleyin. Yeni bir ER çözümü tasarlamak için ER çerçevesini kullanmaya başlamadan önce bu kurulumu tamamlamanız gerekir.

### <a name="design-a-domain-specific-data-model"></a>Etki alanına özel veri modeli tasarlama

Gerekli veri modeli bileşeni içeren yeni bir ER yapılandırması oluşturmanız gerekir. Bu veri modeli daha sonra bir denetim raporu oluşturmak üzere bir ER biçimi tasarlarken veri kaynağı olarak kullanılacaktır.

Gerekli veri modelini Microsoft tarafından sağlanan bir XML dosyasından almak için bu adımları izleyin.

1. [Sample audit model.version.1.xml](https://download.microsoft.com/download/7/1/9/719b0132-fed7-4c73-8afa-90cac29c2fee/Sample-audit-model.version.1.xml) dosyasını indirin ve yerel bilgisayarınıza kaydedin.
2. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
3. **Elektronik raporlama** çalışma alanında **Raporlama yapılandırmaları**'nı seçin.
4. **Yapılandırmalar** sayfasında Eylem Bölmesindeki **Değiştir** \> **XML dosyasından yükle**'yi seçin.
5. **Gözat**'ı seçin ve **Sample audit model.version.1.xml** dosyasını bulup seçin.
6. Yapılandırmayı içe aktarmak için **Tamam**'ı seçin.

    ![Yapılandırmalar sayfasındaki fatura modeli içe aktarılan ER veri modeli yapılandırması.](./media/er-data-model-parameterized-calls-imported-model.png)

Aşağıdaki şekil, **Veri modeli tasarımcısı** sayfasındaki yapılandırılan veri modelinin düzenlenebilir sürümünü gösterir.

![Veri modeli tasarımcısı sayfasındaki ER veri modelinin yapısı.](./media/er-data-model-parameterized-calls-model1.png)

Şu anda, model yalnızca gerekli ayrıntılara sahip vergi hareketlerini açığa çıkarmak için tasarlanmıştır.

### <a name="design-a-model-mapping-for-the-configured-data-model"></a>Yapılandırılan veri modeli için bir model eşlemesi tasarlama

Elektronik Raporlama Geliştirici rolünde bir kullanıcı olarak, Örnek denetim veri modeli için bir model eşleme bileşeni içeren yeni bir ER yapılandırması oluşturmanız gerekir. Bu bileşen Microsoft Dynamics 365 Finance için yapılandırılmış veri modelini uygular ve bu uygulamaya özgüdür. Model eşleme bileşenini, yapılandırılan veri modelini çalışma zamanında uygulama verileriyle doldurmak için kullanılması gereken uygulama nesnelerini belirtecek şekilde yapılandırmanız gerekir. Bu görevi tamamlamak için, Finance'te vergi iş etki alanının veri yapısı uygulama ayrıntılarını bilmeniz gerekir.

Gerekli model eşlemeyi Microsoft tarafından sağlanan bir XML dosyasından almak için bu adımları izleyin.

1. [Sample audit model mapping.version.1.1xml](https://download.microsoft.com/download/c/0/3/c03a4673-b1b1-4ef8-96d0-bf96518be6e0/Sample-audit-model-mapping.version.1.1.xml) dosyasını indirin ve yerel bilgisayarınıza kaydedin.
2. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
3. **Elektronik raporlama** çalışma alanında **Raporlama yapılandırmaları**'nı seçin.
4. **Yapılandırmalar** sayfasında Eylem Bölmesindeki **Değiştir** \> **XML dosyasından yükle**'yi seçin.
5. **Gözat**'ı seçin ve **Sample audit mapping.version.1.1.xml** dosyasını bulup seçin.
6. Yapılandırmayı içe aktarmak için **Tamam**'ı seçin.

    ![Yapılandırmalar sayfasındaki fatura modeli içe aktarılan ER model eşleme yapılandırması.](./media/er-data-model-parameterized-calls-imported-mapping.png)

Aşağıdaki şekil, **Model eşleme tasarımcısı** sayfasındaki yapılandırılmış model eşlemesinin düzenlenebilir sürümünü gösterir.

![Model eşlemesi tasarımcısı sayfasındaki ER model eşlemesi yapısı.](./media/er-data-model-parameterized-calls-mapping1.png)

Şu anda, model eşleme gerekli ayrıntılara sahip vergi hareketlerini açığa çıkarmak için tasarlanmıştır. Bu bilgileri `TaxTrans` uygulama tablosundan, yapılandırılmış `TaxTrans` ve `TaxTransFiltered` ER veri kaynaklarını kullanarak getirir.

### <a name="design-a-new-format"></a>Yeni biçim tasarlama

Elektronik Raporlama İşlev Danışmanı rolündeki bir kullanıcı olarak, bir biçim bileşeni içeren yeni bir ER yapılandırması oluşturmanız gerekir. Format bileşenini, gereken tüm ayrıntılara sahip olan vergi hareketleriyle doldurmak üzere konfigüre etmelisiniz.

Gerekli biçimi Microsoft tarafından sağlanan bir XML dosyasından almak için bu adımları izleyin.

1. [Sample audit format.version.1.1.xml](https://download.microsoft.com/download/e/b/7/eb7e126e-2bb3-4bbb-a735-ffd4c48920b1/Sample-audit-format.version.1.1.xml) dosyasını indirin ve yerel bilgisayarınıza kaydedin.
2. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
3. **Elektronik raporlama** çalışma alanında **Raporlama yapılandırmaları**'nı seçin.
4. **Yapılandırmalar** sayfasında Eylem Bölmesindeki **Değiştir** \> **XML dosyasından yükle**'yi seçin.
5. **Gözat**'ı seçin ve **Sample audit format.version.1.1.xml** dosyasını bulup seçin.
6. Yapılandırmayı içe aktarmak için **Tamam**'ı seçin.

    ![Yapılandırmalar sayfasındaki fatura modeli içe aktarılan ER biçim yapılandırması.](./media/er-data-model-parameterized-calls-imported-format.png)

Aşağıdaki şekil, **Biçim tasarımcısı** sayfasındaki yapılandırılmış biçimin düzenlenebilir sürümünü gösterir.

![Biçim tasarımcısı sayfasındaki ER biçiminin yapısı.](./media/er-data-model-parameterized-calls-format1.png)

ER biçimi, bir raporu virgülle ayrılmış değerler (CSV) biçiminde bir metin dosyası olarak oluşturmak üzere yapılandırılmıştır.

### <a name="run-the-imported-format"></a>İçe aktarılan biçimi çalıştırma

1. **Konfigürasyonlar** sayfasında **Örnek denetleme biçimi** yapılandırmasını seçin ve eylem bölmesinde, **Çalıştır**'ı seçin.
2. **Elektronik rapor parametreleri** iletişim kutusunda, **Dahil edilecek kayıtlar** sekmesinde **Filtre**'yi seçin.
3. **PIV-110000004** ve **INV-10000001** fişlerinin vergi hareketlerini seçmek üzere koşulları belirleyin.
4. **Tamam**'ı seçin.
5. **Tamam**'ı seçin.
6. Seçili fişlerle ilgili vergi hareketlerini içeren oluşturulan belgeyi gözden geçirin.

    ![Oluşturulan belgenin vergi hareketleriyle önizlemesi.](./media/er-data-model-parameterized-calls-output1.png)

### <a name="adjust-the-imported-er-solution"></a>İçe aktarılan ER çözümünü ayarlama

Yeni gereksinime göre, göndermeniz gereken belge, hareketleri dahil edilen müşteri ve satıcı adlarını içermelidir. Bu nedenle, içe aktardığınız ER çözümünü bu yeni gereksinimle uyumlu bir belge oluşturacak şekilde değiştirmelisiniz.

İçe aktarılan ER bileşenlerinde gerekli değişiklikleri nasıl uygulamak istediğinize karar verin.

Bariz yaklaşım aşağıdaki değişiklikleri uygulamaktır:

- Veri modelinizde, yeni `Transaction.Party.Name` veri modeli alanını *Dize* türünde ekleyin.
- Model eşleştirmesinde, `DirPartyTable` uygulama tablosunun ilgili kaydına erişmek ve bundan `Name` alanının değerini getirmek için, kullanılabilir tablo ilişkilerini kullanarak yeni veri modeli alanı bağlamasını konfigüre edin.

Bu yaklaşım işe yarayacaktır ancak hareket tablosu `TaxTrans` olduğundan ve büyük miktarda kayıt içerebileceğinden SQL veritabanında performans sorunlarına neden olabilir. Bu durumda, bir `TaxTrans` tablosunda performans sorunlarına neden olabilecek kayıt sayısına eşit olması gereken `DirPartyTable` çağrı sayısı.

Alternatif olarak, aşağıdaki değişiklikleri uygulayabilirsiniz:

- Veri modelinizde yeni `Party` kökü ve yeni `Party.Name` alanı ekleyin.
- Model eşlemenizde, `TaxTrans` tablosundan başlayarak, `DirPartyTable` uygulama tablosunun ilgili kaydına erişmek için tablo ilişkilerinde kullanılan tüm tablo kayıtlarına katılacak yeni bir veri kaynağı ekleyin.

Bu yaklaşım işe yarar ancak bazı bellek tüketimi sorunlarına neden olabilir. Veritabanı performans sorunlarını önlemek amacıyla, yeni bir [JOIN](er-join-data-sources.md) veri kaynağı uygulama veritabanına tek bir SQL isteği olarak çalıştırılsa bile, sonuç, uygulama sunucusunun belleğine getirilmelidir. Kayıtların sayısı ve bu kayıtlardaki alan sayısı çok büyük olacağından, bu yaklaşım çok ağır bellek tüketimine neden olabilir. Belleğin yetersiz olduğu çalışma zamanı özel durumu bile oluşturulabilir.

Çalışan bir biçim bellekte, oluşturulan bir raporda sunulacak tüm vergi hareketleri için benzersiz tanımlama kodları olduğunda, bu değişiklikleri uygulayabilirsiniz. Yalnızca benzersiz kodların korunması gerektiğinden, son kod kümesi bellek tüketimini etkileyecek kadar büyük olmayacaktır. Kod kümesi daha sonra *Model* türüne ait bir veri kaynağı çağrısının bağımsız değişkeni olarak model eşlemeye geçirilir. Bu çağrıya bağlı olarak, model eşlemesi, `DirPartyTable` tablosundan uygulama veritabanına yalnızca kodları sağlanan kod kümesinde bulunan tarafların kayıtlarını getirmek üzere tek bir SQL talebinde bulunacak yeni bir ER veri kaynağı çalıştırır.

### <a name="adjust-the-imported-data-model"></a>İçe aktarılan veri modelini ayarlama

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında soldaki yapılandırma ağacında, **Örnek denetim modeli**'ni seçin.
3. **Sürümler** hızlı sekmesinde durumu **Taslak** olan **2** sürümünü seçin.
4. **Yapılandırma bileşenleri** hızlı sekmesini seçin.
5. Düzenlenecek veri modelini açmak için **Tasarımcı**'yı seçin.
6. **Veri modeli** sayfasında, `Root` alanının seçili olduğundan emin olun ve sonra **Yeni**'yi seçin.
7. Açılan iletişim kutusunda şu adımları izleyin:

    1. **Yeni düğüm olarak** alan grubunda, **Etkin düğüm seçeneğinin alt öğesini** seçin.
    2. **Ad** alanına, **Taraf** yazın.
    3. **Madde türü** alanında **Kayıt listesi**'ni seçin.
    4. Yeni alan eklemeyi bitirmek için **Ekle**'yi seçin.

8. `Root.Party` alanının seçili olduğundan emin olun ve sonra **Düğüm** sekmesinde **Parametreler**'i seçin.
9. **Parametreler** iletişim kutusunda şu adımları izleyin:

    1. **Parametreler** sekmesinde **Yeni**'yi seçin.
    2. **Ad** alanına, **PartyRefRecId** girin.
    3. **Tür** alanında **Int64**'ü seçin.
    4. **Liste** onay kutusunu seçin.
    5. Parametreleri girmeyi tamamlamak için **Tamam**'ı seçin.

    > [!NOTE]
    > `Root.Party` veri modeli alanını, **PartyRefRecId** parametresinde bir değer sağlandığında çağrılan bir alan olarak yapılandırdınız. Bu değer, *Int64* veri türünde bir `Value` alanı içeren kayıtlar listesinde bulunmalıdır.

    ![Parametreler iletişim kutusu.](./media/er-data-model-parameterized-calls-model2a.png)

10. `Root.Party` alanının hala seçili olduğundan emin olun ve sonra **Yeni**'yi seçin.
11. Açılan iletişim kutusunda şu adımları izleyin:

    1. **Yeni düğüm olarak** alan grubunda, **Etkin düğüm seçeneğinin alt öğesini** seçin.
    2. **Ad** alanına, **Ad** yazın.
    3. **Madde türü** alanında **Dize**'yi seçin.
    4. Yeni alan eklemeyi bitirmek için **Ekle**'yi seçin.

12. **Kaydet**'i seçin ve ardından **Veri modeli** sayfasını kapatın.

    ![Veri modeli tasarımcısı sayfasındaki ayarlanan ER veri modelinin yapısı.](./media/er-data-model-parameterized-calls-model2b.png)

13. **Sürümler** hızlı sekmesinde,sürüm **2** için **Durumu değiştir** \> **Tamamlandı**'yı seçin. Daha sonra **Tamam**'ı seçin.

    > [!NOTE]
    > Veri modeli değişiklikleriniz, **Örnek denetim modeli** ER yapılandırmasının ikinci sürümünde bulunan **Örnek denetim modeli** veri modeli bileşeninin ikinci düzeltmesinde depolanır.

![Yapılandırmalar sayfasındaki fatura modeli güncelleştirilen ER veri modeli yapılandırması.](./media/er-data-model-parameterized-calls-updated-model.png)

### <a name="adjust-the-imported-model-mapping"></a>İçe aktarılan model eşleşmesini ayarlama

1. **Yapılandırmalar** sayfasında soldaki yapılandırma ağacında, **Örnek denetim modeli**'ni genişletin.
2. **Örnek denetleme modeli eşlemesi** seçin ve sonra **Sürümler** hızlı sekmesinde, ilk veri modeli sürümüne (sürüm **1.2**) dayalı olan ve **Taslak** durumunda olan ikinci eşleme sürümünü seçin.
3. **Yeniden temellendirme** seçin.
4. **Hedef sürüm** alanında, **Örnek denetim modeli** temel modelinin **2** sürümünü bırakın.
5. Yeniden temellendirdiğiniz ve model eşlemenizi en son veri modeli değişiklikleriyle hizalamak için **Tamam**'ı seçin.

    İkinci model sürümünün şu anda temel olarak kullanıldığını belirtmek için, düzenlenebilir model eşlerinizin sürüm numarasının **1.2**'den **2.2**'ye değiştirildiğine dikkat edin.

6. **Tasarımcı**’yı seçin.
7. **Veri kaynağı eşleme modeli** sayfasında geçerli model eşlemesi için **Tasarımcı**'yı seçin.
8. `DirPartyTable` uygulama tablosuna erişmek üzere yeni bir veri kaynağı eklemek için aşağıdaki adımları izleyin:

    1. **Veri kaynağı türü** bölmesinde, **Dynamics 365 for Operations \> Tablo kayıtlarını** seçin.
    2. **Veri kaynakları** bölmesinde **Kök ekle**'yi seçin.
    3. **Ad** alanına, **PartyTable** girin.
    4. **Tablo** alanına, **DirPartyTable** girin.
    5. Yeni veri kaynağını eklemeyi bitirmek için **Tamam**'ı seçin.

9. Sağlanan kayıt tanımlama kodları listesine göre, `DirPartyTable` kayıtları istemek üzere yeni bir veri kaynağı eklemek için aşağıdaki adımları izleyin:

    1. **Veri kaynağı türü** bölmesinde, **Genel \> Boş kapsayıcı**'yı seçin.
    2. **Veri kaynakları** bölmesinde **Kök ekle**'yi seçin.
    3. **Ad** alanına, **Veri** yazın.
    4. Yeni veri kaynağını eklemeyi bitirmek için **Tamam**'ı seçin.
    5. **Veri kaynakları** bölmesinde, **Veri** veri kaynağını seçin.
    6. **Veri kaynağı türü** bölmesinde, **İşlevler \> Hesaplanan alan**'ı seçin.
    7. **Veri kaynakları** bölmesinde **Ekle**'yi seçin.
    8. **Ad** alanına, **DirParty** girin.
    9. **Formül düzenle**’yi seçin.
    10. **Formül tasarımcısı** sayfasında, **Parametreler**'i seçin.
    11. **Parametreler** iletişim kutusunda şu adımları izleyin:

        1. **Parametreler** sekmesinde **Yeni**'yi seçin.
        2. **Ad** alanına, **DirPartyId** girin.
        3. **Tür** alanında **Int64**'ü seçin.
        4. **Liste** onay kutusunu seçin.
        5. **Tamam**'ı seçin.

        > [!NOTE]
        > Bu hesaplanan alanı, çalışma zamanında *Int64* türünde tek bir `Value` alanı olan bir kayıt listesi olarak konfigüre edilen tek bir parametrenin bağımsız değişkenini kabul edecek şekilde yapılandırdınız.

    12. **Formül** alanında, aşağıdaki ifadeyi girin:

        `FILTER(PartyTable, VALUEINLARGE(PartyTable.RecId, DirPartyId, DirPartyId.Value))`

        > [!NOTE]
        > `DirParty` alanı çağrıldığında bir bağımsız değişken olarak sağlanan `DirPartyId` listesine kayıt tanımlama kodlarının dahil edildiği `DirPartyTable` kayıtları getirmek için `DirParty` hesaplanan alanını konfigüre ettiniz.

        ![Formül tasarımcısı sayfasındaki uygulama tablosundan taraf adlarını getirmek için formül.](./media/er-data-model-parameterized-calls-formula1.png)

    13. **Kaydet**'i seçin ve sonra **Formül tasarımcısı** sayfasını kapatın.
    14. **Kaydet**'i seçin ve sonra yeni veri kaynağını eklemeyi bitirmek için **Tamam**'ı seçin.

10. Yeni veri kaynağını yeni veri modeli alanına bağlamak için aşağıdaki adımları izleyin, böylece taraf adlarını göstermek için veri modeli kullanılır:

    1. **Veri modeli** bölmesinde, `Root.Party` veri modeli alanını seçin.
    2. **Veri modeli** bölmesinde **Düzenle**'yi seçin.
    3. **Formül tasarımcısı** sayfasında, **Formül** alanına `Data.DirParty(PartyRefRecId)` ifadesini girin.
    4. **Kaydet**'i seçin ve sonra **Formül tasarımcısı** sayfasını kapatın.

        > [!NOTE]
        > Yapılandırılan `Data.DirParty` veri kaynağını çağırma ve `Root.Party` veri modeli alanı çağrıldığında belirtilen biçimde olacak olan kayıt tanımlama kodlarının kayıt listesini sağlayacak olan bağlamayı yapılandırdınız.

    5. **Veri modeli** bölmesinde, `Root.Party.Name` veri modeli alanını seçin.
    6. **Veri modeli** bölmesinde **Düzenle**'yi seçin.
    7. **Formül tasarımcısı** sayfasında, **Veri kaynağı** bölmesinde, **Veri \> DirParty**'yi genişletin ve **Ad**'ı seçin.
    8. **Veri kaynağını ekle**'yi seçin.
    9. **Kaydet**'i seçin ve sonra **Formül tasarımcısı** sayfasını kapatın.

    ![Model eşlemesi tasarımcısı sayfasındaki ayarlanan ER model eşlemesi yapısı.](./media/er-data-model-parameterized-calls-mapping2.png)

11. **Kaydet**'i seçin ve **Model eşleme tasarımcısı** sayfasını kapatın.
12. **Veri kaynağı modeli eşleme** sayfasını kapatın.
13. **Sürümler** hızlı sekmesinde, sürüm **2.2** için **Durumu değiştir \> Tamamlandı**'yı seçin. Daha sonra **Tamam**'ı seçin.

### <a name="adjust-the-imported-format"></a>İçe aktarılan biçimi ayarlama

1. **Yapılandırmalar** sayfasında, **Örnek denetim biçimi**'ni seçin.
2. **Sürümler** hızlı sekmesinde durumu **Taslak** olan **1.2** sürümünü seçin.
3. **Yeniden temellendirme** seçin.
4. **Hedef sürüm** alanında, **Örnek denetim modeli** temel modelinin **2** sürümünü bırakın.
5. Biçiminizi, en yeni veri modeli değişiklikleriyle yeniden temellendirmek ve hizalamak için **Tamam**'ı seçin.
6. **Tasarımcı**’yı seçin.
7. **Biçim tasarımcısı** sayfasında, biçim yapısı ağacında **Genişlet/Daralt**'ı seçin.
8. Hareketleri oluşturulan raporlarda sunulan tarafların kayıt tanımlama kodlarını toplamak için yeni bir biçim öğesi eklemek üzere bu adımları izleyin.

    1. Biçim yapısı ağacında, **Report.Row.Trans** sıralama öğesini seçin.
    2. **Ekle**'yi seçin.
    3. **Ekle** iletişim kutusunda, **Veri kaynağı \> Öğe**'yi seçin.
    4. **Bileşen özellikleri** iletişim kutusunda, **Ad** alanına **Kimlik** girin.
    5. **Veri türü** alanında **Int64** seçin.
    6. **Tamam**'ı seçin.

    > [!NOTE]
    > Bir **Veri kaynağı \>Madde** öğesi iç hesaplamaları ve veri dönüşümünü yalnızca çalışan biçim kapsamında gerçekleştirmek için kullanılabilir. Bu nedenle, bu biçim öğesini ekleyerek oluşturulan bir belgenin içeriğini değiştirmeyin.

9. Oluşturulan raporlarda taraf adlarını girmek üzere yeni biçim öğeleri eklemek için aşağıdaki adımları izleyin:

    1. **Report.Row** sıra öğesini seçin.
    2. **Ekle**'yi seçin.
    3. **Ekle** iletişim kutusunda **Metin\>Sıra**'yı seçin.
    4. **Bileşen özellikleri** iletişim kutusunda, **Ad** alanına **Taraf** girin.
    5. **Tamam**'ı seçin.
    6. **Report.Row.Party** sıra öğesini seçin.
    7. **Ekle**'yi seçin.
    8. **Ekle** iletişim kutusunda **Metin \> Dize**'yi seçin.
    9. **Bileşen özellikleri** iletişim kutusunda, **Ad** alanına **Ad** girin.
    10. **Tamam**'ı seçin.

10. Hareketleri oluşturulan raporlarda sunulan tarafların kayıt tanımlama kodlarını toplamak için yeni bir veri kaynağı eklemek üzere bu adımları izleyin:

    1. **Eşleme** sekmesinde **Kök ekle**'yi seçin.
    2. **Veri kaynağı ekle** iletişim kutusunda, **İşlevler \> Veri toplama**'yı seçin.
    3. **"Veri toplama" veri kaynağı özellikleri** iletişim kutusunda, **Ad** alanına **PartyIds** girin.
    4. **Madde türü** alanında **Int64** seçin.
    5. **Tamam**'ı seçin.

11. Hareketleri oluşturulan raporlarda sunulan tarafların kayıt tanımlama kodlarını toplamak için yeni bir bağlama eklemek üzere bu adımları izleyin:

    1. Biçim yapısı ağacında, **Report.Row.Trans.Id** veri maddesi öğesini seçin.
    2. **Formül düzenle**’yi seçin.
    3. **Formül tasarımcısı** sayfasında, `PartyIds.Collect(model.Transaction.Party.RecId)` ifadesini girin.
    4. **Kaydet**'i seçin ve sonra **Formül tasarımcısı** sayfasını kapatın.

12. Oluşturulan raporlarda taraf adlarını girmek üzere yeni bağlamalar eklemek için aşağıdaki adımları izleyin:

    1. Biçim yapısı ağacında, **Report.Party** sıralama öğesini seçin.
    2. **Formül düzenle**’yi seçin.
    3. **Formül tasarımcısı** sayfasında, `model.Party(PartyIds.Result)` ifadesini girin.
    4. **Kaydet**'i seçin ve sonra **Formül tasarımcısı** sayfasını kapatın.
    5. Biçim yapısı ağacında, **Report.Party.Name** sıralama öğesini seçin.
    6. **Eşleme** sekmesinde `model.Party.Name` veri modeli alanını seçin.
    7. **Bağla**'yı seçin.

    ![Biçim tasarımcısı sayfasındaki ayarlanan ER biçiminin yapısı.](./media/er-data-model-parameterized-calls-format2.png)

13. **Kaydet**'i seçin ve sonra **Biçim tasarımcısı** sayfasını kapatın.
14. **Veri kaynağı modeli eşleme** sayfasını kapatın.
15. **Sürümler** hızlı sekmesinde,sürüm **2.2** için **Durumu değiştir** \> **Tamamlandı**'yı seçin. Daha sonra **Tamam**'ı seçin.

### <a name="run-the-adjusted-format"></a>Ayarlanan biçimi çalıştırma

1. **Konfigürasyonlar** sayfasında **Örnek denetleme biçimi**'ni seçin ve eylem bölmesinde, **Çalıştır**'ı seçin.
2. **Elektronik rapor parametreleri** iletişim kutusunda, **Dahil edilecek kayıtlar** sekmesinde **Filtre**'yi seçin.
3. **PIV-110000004** ve **INV-10000001** fişlerinin vergi hareketlerini seçmek üzere koşulları belirleyin.
4. **Tamam**'ı seçin.
5. **Tamam**'ı seçin.
6. Seçili fişlerle ilgili vergi hareketlerini ve karşılık gelen müşteri ve satıcının adını içeren oluşturulmuş belgeyi gözden geçirin.

    ![Oluşturulan belgenin vergi hareketleriyle ve taraf adlarıyla önizlemesi.](./media/er-data-model-parameterized-calls-output2.png)

7. **Borç hesapları** \> **Satıcılar** \> **Tüm satıcılar**'a gidin ve seçili **PIV-110000004** fişinin ayrıntılarını inceleyin, satıcı adı da dahil.

    ![Tüm satıcılar ve fatura günlüğü sayfalarındaki satınalma fişi ayrıntılarını gözden geçirme.](./media/er-data-model-parameterized-calls-review1.gif)

8. **Alacak hesapları** \> **Müşteriler** \> **Tüm müşteriler**'e gidin ve seçili **INV-10000001** fişinin ayrıntılarını inceleyin, müşteri adı da dahil.

    ![Tüm müşteriler ve Deftere nakledilen satış vergisi sayfalarının satış fiş ayrıntılarını gözden geçirme.](./media/er-data-model-parameterized-calls-review2.gif)

ER çözümünün bu yürütmesi hakkında daha fazla bilgi için, yerleşik [performans izleme ](trace-execution-er-troubleshoot-perf.md) ayrıştırıcısını kullanın.

## <a name="additional-resources"></a>Ek kaynaklar

- [Hesaplanan alan türünün ER veri kaynaklarının parametreleştirilmiş çağrılarını destekleme](er-calculated-field-type.md)
- [Performans sorunlarını gidermek için ER biçimlerinin yürütülmesini izleme](trace-execution-er-troubleshoot-perf.md)
- [VERİ TOPLAMA veri kaynaklarını Elektronik raporlama biçimlerinde kullanma](er-data-collection-data-sources.md)
- [ValueInLarge ER işlevi](er-functions-logical-valueinlarge.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
