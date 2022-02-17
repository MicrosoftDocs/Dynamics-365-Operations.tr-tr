---
title: GROUPBY veri kaynaklarını kullanarak kayıtları ve toplam hesaplamaları gruplama
description: Bu konuda, Elektronik raporlama'da (ER) GROUPBY türü veri kaynaklarını nasıl kullanabileceğiniz açıklanmaktadır.
author: NickSelin
ms.date: 01/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a6cdc486c5f799bdedafa38e90be989fd328c96
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075647"
---
# <a name="group-records-and-aggregate-calculations-by-using-groupby-data-sources"></a>GROUPBY veri kaynaklarını kullanarak kayıtları ve toplam hesaplamaları gruplama

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

[Elektronik raporlama (ER)](general-electronic-reporting.md) modeli eşlemelerini veya biçimlerini yapılandırırken, **GroupBy** türünde gerekli veri kaynakları [ekleyebilirsiniz](#AddMmDataSource2).

Tasarım zamanında, **GroupBy** veri kaynağı aşağıdaki öğeleri tanımlayacak şekilde yapılandırılır:

- Çalışma zamanında gruplandırılacak kayıtları içeren [temel veri kaynağı](#BaseDataSource) 
- Çalışma zamanında kayıt gruplandırması için kullanılacak temel veri kaynağının [gruplandırma alanları](#GroupingFields)
- Çalışma zamanında keşfedilen her grup için yapılacak toplam hesaplamaları belirten [toplama işlevleri](#AggregateFunctions)

Çalışma zamanında, yapılandırılmış bir **GroupBy** veri kaynağı, gruplandırma alanlarında aynı değerlere sahip kayıtları gruplandırır ve sonra bir kayıt listesi döndürür. Her kayıt tek bir grubu temsil eder. Her grup için veri kaynağı, ilk kayıtların gruplandırıldığı alan değerlerini, hesaplanan toplama işlevlerinin değerlerini ve gruba ait temel veri kaynağının kayıtlarının listesini gösterir.

## <a name="aggregate-functions"></a><a name="AggregateFunctions"></a>Toplama işlevleri

Çalışma zamanında, her kayıt grubu için her toplama hesaplaması yapılır. Bu hesaplama, **GroupBy** türünün düzenlenebilir veri kaynağında gruplandırma için seçilen bir veri kaynağının kayıtlarındaki tek bir alanın veya ifadenin değeri kullanılarak yapılır. Şu anda aşağıdaki toplama işlevleri desteklenmektedir:

- **AVG** – Bu işlev bir gruptaki değerlerin ortalamasını verir. Yalnızca sayısal alanlarla kullanılabilir.
- **COUNT** – Bu işlev, bir grupta bulunan öğe sayısını döndürür.
- **Min** – Bu işlev, gruptaki değerler arasında en düşük değeri döndürür.
- **Max** – Bu işlev, gruptaki değerler arasında en büyük değeri döndürür.
- **SUM** – Bu işlev, bir gruptaki tüm değerlerin toplamını döndürür. Yalnızca sayısal alanlarla kullanılabilir.

## <a name="execution-location"></a><a name="ExecutionLocation"></a>Yürütme konumu

Bir **GroupBy** veri kaynağını düzenlediğinizde ve gruplandırılması gereken kayıtları içeren temel veri kaynağını belirttiğinizde, sistem bu **GroupBy** veri kaynağının yürütülmesi için en verimli [konumu](#ExecutionLocation) otomatik olarak algılar. Temel veri kaynağı [sorgulanabilirse](er-functions-list-filter.md#usage-notes) (diğer bir deyişle veritabanı düzeyinde çalıştırılabilirse) uygulama veritabanı düzenlenebilir **GroupBy** veri kaynağının yürütme konumu olarak da belirtilir. Aksi takdirde, uygulama sunucusu belleği, yürütme konumu olarak belirtilir.

Yapılandırılan veri kaynağına uygulanabilecek konumu seçerek otomatik olarak algılanan yürütme konumunu el ile değiştirebilirsiniz. Seçilen yürütme konumu geçerli değilse, tasarım zamanında bir [doğrulama hatası](er-components-inspections.md#i5) oluşur.

> [!TIP]
> Çok sayıda kaydı açığa çıkaran veri kaynaklarını gruplandırmak için veritabanı konumunu kullanmanızı öneririz.

## <a name="memory-consumption"></a><a name="MemoryConsumption"></a>Bellek tüketimi

Varsayılan olarak, bir **GroupBy** veri kaynağı bellekte çalıştırılırsa, uygulama sunucusu belleği, bulunan her gruba ait temel veri kaynağının kayıtlarını tek bir grubun kayıtları olarak depolamak için kullanılır. Bellek tüketimini azaltmaya yardımcı olmak için, yalnızca toplanan işlevleri hesaplamak üzere yapılandırılmışlarsa ve gruplarının kayıtları çalışma zamanında kullanılmazsa **GroupBy** veri kaynakları için kayıt depolamayı bastırabilirsiniz. Bellek tüketimini bu şekilde azaltmak için **Özellik yönetimi** çalışma alanında **Kayıt gruplandırması yalnızca toplamaları hesaplamak için kullanıldığında ER'de bellek kullanımını azalt**'ı etkinleştirin.

## <a name="alternatives"></a><a name="Alternatives"></a>Alternatifler

Benzer toplamalar, [farklı](er-data-collection-data-sources.md#if-i-have-to-calculate-running-totals-and-collect-data-what-is-the-difference-between-using-a-data-collection-data-source-and-using-the-built-in-data-collection-functions) veri kaynakları veya ER yerleşik işlevleri kullanılarak hesaplanabilir.

Bu özellik hakkında daha fazla bilgi edinmek için aşağıdaki örneği tamamlayın.

## <a name="example-use-a-groupby-data-source-for-aggregate-calculations-and-record-grouping"></a><a name="Example"></a>Örnek: Toplama hesaplamaları ve kayıt gruplandırması için GROUPBY veri kaynağını kullanma

Bu örnek, Sistem yöneticisi veya Elektronik raporlama işlev danışmanı rolündeki bir kullanıcının, toplama işlevlerini ve grup kayıtlarını hesaplamak için kullanılan bir **GROUPBY** veri kaynağına sahip bir ER modeli eşlemesini nasıl yapılandırabileceğini gösterir. Bu model eşlemesi, İntrastat bildirimi oluşturulduğunda denetim raporunu yazdırmak için kullanılır. Bu rapor, bildirilen İntrastat hareketlerini gözden geçirmenizi sağlar.

Bu örnekteki yordamlar Microsoft Dynamics 365 Finance'teki **DEMF** şirketinde tamamlanabilir. 

### <a name="prepare-sample-data"></a>Örnek verileri hazırlama

**İntrastat** sayfasında raporlama için İntrastat hareketleriniz olduğundan emin olun. Bu örnekte hareketleri **Taşıma** alanına göre gruplayacağınız için farklı taşıma kodları için hareketleriniz olmalıdır.

![İntrastat sayfasında İntrastat hareketlerini hazırlama.](./media/er-groupby-data-sources-prepare-transactions.png)

### <a name="configure-the-er-framework"></a>ER altyapısını yapılandırma

En az ER parametre kümesini ayarlamak için [ER altyapısını yapılandırma](er-quick-start2-customize-report.md#ConfigureFramework) bölümündeki adımları izleyin. ER model eşlemesi tasarlamak için ER çerçevesini kullanmaya başlamadan önce bu kurulumu tamamlamanız gerekir.

### <a name="import-the-standard-er-format-configuration"></a>Standart ER biçimi yapılandırmasını içeri aktarma

Standart ER yapılandırmalarını Dynamics 365 Finance kurulumunuza eklemek için [Standart ER biçimi yapılandırmasını içeri aktarma](er-quick-start2-customize-report.md#ImportERSolution1) bölümündeki adımları izleyin. **İntrastat modeli** yapılandırmasının sürüm 1'ini depodan içeri aktarın.

### <a name="create-a-custom-data-model-configuration"></a>Özel veri modeli yapılandırması oluşturma

İçeri aktarılan [İntrastat modeli](er-quick-start3-customize-report.md#add-a-custom-data-model-configuration) yapılandırmasından türetilen yeni bir **İntrastat modeli (Litware)** ER veri modeli yapılandırmasını el ile eklemek için **Özel veri modeli yapılandırması ekleme** bölümündeki adımları izleyin.

### <a name="configure-a-custom-data-model-component"></a>Özel veri modeli bileşeni yapılandırma

Türetilen **İntrastat modeli (Litware)** veri modelinde gerekli değişiklikleri yapmak için bu adımları izleyin, böylece gerekli ayrıntılara sahip aktarım kodlarını göstermek için kullanılabilir.

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında, yapılandırma ağacında **İntrastat modeli (Litware)** öğesini seçin.
3. **Tasarımcı**’yı seçin.
4. **Veri modeli tasarımcısı** sayfasında, model ağacında **İntrastat**'ı seçin.
5. Seçili **İntrastat** düğümü için yeni bir iç içe düğüm eklemek üzere **Yeni**'yi seçin. Veri modeli düğümü eklemek için açılan iletişim kutusunda şu adımları izleyin:

    1. **Ad** alanında, **Taşıma** girin.
    2. **Madde türü** alanında **Kayıt listesi**'ni seçin.
    3. Yeni düğüm eklemek için **Ekle**'ye tıklayın.

6. Yeni eklediğiniz **Taşıma** düğümü için yeni bir iç içe düğüm eklemek üzere **Yeni**'yi seçin. Veri modeli düğümü eklemek için açılan iletişim kutusunda şu adımları izleyin:

    1. **Ad** alanında, **Kod** girin.
    2. **Madde türü** alanında **Dize**'yi seçin.
    3. Yeni düğüm eklemek için **Ekle**'ye tıklayın.

7. **Taşıma** düğümü için başka bir iç içe düğüm eklemek için **Yeni**'yi seçin. Veri modeli düğümü eklemek için açılan iletişim kutusunda şu adımları izleyin:

    1. **Ad** alanında, **TotalInvoicedAmount** girin.
    2. **Madde türü** alanında **Gerçek**'i seçin.
    3. Yeni düğüm eklemek için **Ekle**'ye tıklayın.

8. **Taşıma** düğümü için başka bir iç içe düğüm eklemek için **Yeni**'yi seçin. Veri modeli düğümü eklemek için açılan iletişim kutusunda şu adımları izleyin:

    1. **Ad** alanında, **NumberOfTransactions** girin.
    2. **Madde türü** alanında **Tamsayı**'yı seçin.
    3. Yeni düğüm eklemek için **Ekle**'ye tıklayın.

9. **Taşıma** düğümü için başka bir iç içe düğüm eklemek için **Yeni**'yi seçin. Veri modeli düğümü eklemek için açılan iletişim kutusunda şu adımları izleyin:

    1. **Ad** alanında, **Hareket** girin.
    2. **Madde türü** alanında **Kayıt listesi**'ni seçin.
    3. Yeni düğüm eklemek için **Ekle**'ye tıklayın.

10. Yeni eklediğiniz **Hareket** düğümü için **Düğüm** Hızlı Sekmesinde **Öğe başvurusunu değiştir**'i seçin.
11. **Öğe başvurusunu değiştir** iletişim kutusunda, veri modeli ağacında **CommodityRecord**'u seçin. Daha sonra **Tamam**'ı seçin.

![ER veri modeli tasarımcısında yapılandırılmış veri modeli.](./media/er-groupby-data-sources-configure-data-model.png)

### <a name="complete-the-design-of-a-custom-data-model"></a>Özel veri modelinin tasarımını tamamlama

Türetilmiş **İntrastat modeli (Litware)** [veri modelinin tasarımını tamamlamak](er-quick-start3-customize-report.md#add-a-custom-data-model-configuration) için veri modelinin tasarımını tamamlama adımlarını izleyin.

### <a name="create-a-new-model-mapping-configuration"></a>Yeni model eşleme yapılandırması oluşturma

Türetilmiş **İntrastat modeli (Litware)** yapılandırması için el ile yeni bir **İntrastat örnek eşlemesi** ER modeli eşleme yapılandırması eklemek üzere [Yeni model eşleme yapılandırması oluşturma](er-quick-start1-new-solution.md#CreateModelMapping) bölümündeki adımları izleyin.

### <a name="add-a-new-model-mapping-component"></a>Yeni model eşleme bileşeni ekleme

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında, yapılandırma ağacında **İntrastat modeli** yapılandırmasını genişletin.
3. **İntrastat örnek eşleme** yapılandırmasını seçin.
4. Eşleme listesini açmak için **Tasarımcı**'yı seçin.
5. Varolan eşleme bileşenini kaldırmak için **Sil**'i seçin.
6. Yeni bir eşleme bileşeni eklemek için **Yeni**'yi seçin.
7. **Tanım** alanında **İntrastat**'ı seçin
8. **Ad** alanına **İntrastat eşlemesi** girin.
9. Yeni eşlemeyi yapılandırmak için **Tasarımcı**'yı seçin.

### <a name="design-the-added-model-mapping-component"></a>Eklenen model eşleme bileşenini tasarlama

#### <a name="add-a-data-source-to-access-an-application-table"></a><a name="AddMmDataSource1"></a>Bir uygulama tablosuna erişmek için veri kaynağı ekleme

İntrastat hareketlerinin ayrıntılarını içeren uygulama tablolarına erişmek için bir veri kaynağı yapılandırın.

1. **Model eşleme tasarımcısı** sayfasında, **Veri kaynağı türleri** bölmesinde, **Dynamics 365 for Operations\\Tablo kayıtları**'nı seçin.
2. **Veri kaynakları** bölmesinde, **İntrastat** tablosuna erişmek için kullanılacak yeni bir veri kaynağı eklemek üzere **Kök ekle**'yi seçin. **İntrastat** tablosundaki her kayıt tek bir İntrastat hareketini temsil eder.
3. **Veri kaynağı özellikleri** iletişim kutusunda, **Ad** alanına **Hareket** girin.
4. **Tablo** alanına **İntrastat eşlemesi** girin.
5. Yeni veri kaynağını eklemek için **Tamam**'ı seçin.

#### <a name="add-a-data-source-to-group-intrastat-transactions"></a><a name="AddMmDataSource2"></a>İntrastat hareketlerini gruplamak için veri kaynağı ekleme

İntrastat hareketlerini gruplamak ve toplama işlevlerini hesaplamak için bir **GroupBy** veri kaynağı yapılandırın.

1. **Model eşleme tasarımcısı** sayfasında, **Veri kaynağı türleri** bölmesinde **İşlevler\\Gruplama ölçütü**'nü seçin.
2. **Veri kaynakları** bölmesinde, İntrastat hareketlerini gruplamak ve toplama işlevlerini hesaplamak için kullanılacak yeni bir veri kaynağı eklemek üzere **Kök ekle**'yi seçin.
3. **Veri kaynağı özellikleri** iletişim kutusunda, **Ad** alanına **TransportRecord** girin.
4. Gruplandırma koşullarını yapılandırmak için **Grubu düzenle**'yi seçin.
5. **"Gruplandırma ölçütü" parametrelerini düzenle** sayfasında, sağ bölmedeki veri kaynakları listesinde **Hareket** veri kaynağını seçin ve genişletin.
6. Yapılandırılan **GroupBy** veri kaynağı için <a name="BaseDataSource">temel veri kaynağı</a> olarak **Hareket** veri kaynağının seçildiğini belirtmek üzere **Alanı ekle \> Hangi gruba**'yı seçin. **Hareket** veri kaynağının kayıtları gruplandırılacak ve bu veri kaynağının alan değerleri toplama işlevlerindeki hesaplamalar için kullanılacaktır.
7. Yapılandırılan **GroupBy** veri kaynağının <a name="GroupingFields">gruplandırma ölçütü</a> olarak temel veri kaynağının **Taşıma** alanının seçildiğini belirtmek için **Hareket\Taşıma** alanını seçin ve sonra **Alanı ekle \> Gruplandırılan alan**'ı seçin. Başka bir deyişle, **Hareket** veri kaynağının kayıtları **Taşıma** alanının değerine göre gruplandırılacaktır. Yapılandırılan **GroupBy** veri kaynağının her kaydı, temel veri kaynağının kayıtlarında bulunan tek bir aktarım kodunu temsil eder.
8. **Transaction\AmountMST** alanını seçin ve şu adımları izleyin:

    1. Bu alan için bir <a name="AggregateFunctions">toplam değerin</a> hesaplanacağını belirtmek üzere, **Alanı ekle \> Toplam değer alanları**'nı seçin.
    2. **Toplamalar** bölmesinde, seçili **Transaction\AmountMST** alanı için eklenen kayıtta, **Yöntem** alanında **Sum** işlevini seçin.
    3. İsteğe bağlı **Ad** alanında, **TotalInvoicedAmount** girin.

    Bu ayarlar, her taşıma grubu için **Transaction\AmountMST** alanının toplam tutarının hesaplanacağını belirtir.

9. **Transaction\RecId** alanını seçin ve şu adımları izleyin:

    1. Bu alan için bir toplam değerin hesaplanacağını belirtmek üzere, **Alanı ekle \> Toplam değer alanları**'nı seçin.
    2. **Toplamalar** bölmesinde, seçili **Transaction\RecId** alanı için eklenen kayıtta, **Yöntem** alanında **Count** işlevini seçin.
    3. İsteğe bağlı **Ad** alanında, **NumberOfTransactions** girin.

    Bu ayarlar, her taşıma grubu için gruptaki işlem sayısının hesaplanacağını belirtir.

10. **Kaydet**'i seçin.
11. Düzenlenebilir veri kaynağının <a name="ExecutionLocation">yürütme</a> parametrelerini gözden geçirin. **Yürütme konumu** alanında **Otomatik Algıla**'nın otomatik olarak seçildiğine ve **Yürütme** alanında **SQL** değerinin bulunduğuna dikkat edin. Bu ayarlar seçili **Hareket** temel veri kaynağının şu anda sorgulanabilir olduğunu belirtir ve düzenlenebilir **GroupBy** veri kaynağını veritabanı düzeyinde çalıştırabilirsiniz.
12. Kullanılabilir değerlerin listesini gözden geçirmek için **Yürütme konumu** alanı aramasını açın. Bu **GroupBy** veri kaynağını veritabanı düzeyinde veya uygulama sunucusu belleğinde çalıştırılacak şekilde zorlamak için **Sorgu** veya **Bellekte**'yi seçebileceğinize dikkat edin.
13. **Kaydet**'i seçin ve **"Gruplama Ölçütü" parametrelerini düzenle** sayfasını kapatın.
14. **GroupBy** veri kaynağının ayarlarını tamamlamak için **Tamam**'ı seçin.

#### <a name="bind-the-groupby-data-source-to-data-model-fields"></a><a name="AddMmBindings"></a>GroupBy veri kaynağını veri modeli alanlarına bağlama

Veri modelinin çalışma zamanında uygulama verileriyle nasıl doldurulacağını belirtmek için yapılandırılmış veri kaynağını veri modelinin alanlarına bağlayın.

1. **Model eşleme tasarımcısı** sayfasında, **Veri modeli** bölmesinde **Taşıma** düğümünü genişletin.
2. **Veri kaynakları** bölmesinde, **TransportRecord** veri kaynağını genişletin.
3. Keşfedilen taşıma gruplarının listesini göstermek için bir bağlama ekleyin:

    1. **Veri modeli** bölmesinde **Taşıma** öğesini seçin.
    2. **Veri kaynakları** bölmesinde, **TransportRecord** veri kaynağını seçin.
    3. **Bağla**'yı seçin.

4. Keşfedilen her aktarım grubunun aktarım kodunu göstermek için bir bağlama ekleyin:

    1. **Transport.Code** veri modeli öğesini seçin.
    2. **TransportRecord.grouped.TransportMode** gruplanan alanını seçin.
    3. **Bağla**'yı seçin.

5. Keşfedilen her taşıma grubu için hesaplanan toplama işlevlerinin değerlerini göstermek için bir bağlama ekleyin:

    1. **Transport.NumberOfTransactions** veri modeli öğesini seçin.
    2. **TransportRecord.aggregated.NumberOfTransactions** toplu alanını seçin.
    3. **Bağla**'yı seçin.
    4. **Transport.TotalInvoicedAmount** veri modeli öğesini seçin.
    5. **TransportRecord.aggregated.TotalInvoicedAmount** toplam değer alanını seçin.
    6. **Bağla**'yı seçin.

6. Bulunan her taşıma grubuna ait hareket kayıtlarını göstermek için bir bağlama ekleyin:

    1. **Transport.Transaction** veri modeli öğesini seçin.
    2. **TransportRecord.lines** alanını seçin.
    3. **Bağla**'yı seçin.

    Her bulunan taşıma grubuna ait İntrastat hareketlerinin ayrıntılarını çalışma zamanında ortaya çıkarmak için **Transport.Transaction** veri modeli öğesinin ve **TransportRecord.lines** veri kaynağı alanının iç içe geçmiş öğeleri için bağlamaları yapılandırmaya devam edebilirsiniz.

![ER model eşleme tasarımcısında yapılandırılmış model eşlemesi.](./media/er-groupby-data-sources-configure-model-mapping.png)

### <a name="debug-the-added-model-mapping-component"></a>Eklenen model eşleme bileşeninde hata ayıklama

Yapılandırılmış model eşlemesini test etmek için [ER veri kaynağı hata ayıklayıcısını](er-debug-data-sources.md) kullanın.

1. **Model eşleme tasarımcısı** sayfasında **Hata ayıklamayı başlat**'ı seçin.
2. **Veri kaynaklarında hata ayıkla** sayfasında, sol bölmede **TransportRecord** veri kaynağını seçin ve sonra **Tüm kayıtları oku**'yu seçin.
3. **TransportRecord** veri kaynağını genişletin ve aşağıdaki adımları izleyin:

    1. **TransportRecord.grouped.TransportMode** veri kaynağını seçin.
    2. **Değeri al**'ı seçin.
    3. **TransportRecord.grouped.NumberOfTransactions** veri kaynağını seçin.
    4. **Değeri al**'ı seçin.
    5. **TransportRecord.grouped.TotalInvoicedAmount** veri kaynağını seçin.
    6. **Değeri al**'ı seçin.

4. Sağ bölmede **Tümünü genişlet**'i seçin.

**TransportRecord** veri kaynağı iki kayıt sunar ve iki aktarım kodu sunar. Her taşıma kodu için hareket sayısı ve toplam faturalanan tutar hesaplanır.

> [!NOTE]
> "Yavaş okuma" yaklaşımı, veritabanı çağrılarını en iyi duruma getirmek için bir **GroupBy** veri kaynağı çağrıldığında kullanılır. Bu nedenle, **GroupBy** veri kaynağındaki bazı alan değerleri, yalnızca veri modeli alanlarına bağlı olduğunda ER veri kaynağı hata ayıklayıcısında hesaplanır.

![Veri kaynaklarında hata ayıklama sayfasında hata ayıklamanın sonuçları.](./media/er-groupby-data-sources-debug-datasource.png)

## <a name="frequently-asked-questions"></a>Sık sorulan sorular

### <a name="is-there-any-way-to-calculate-grand-totals-when-the-group-totals-are-calculated"></a>Grup toplamları hesaplandığında genel toplamları hesaplamanın bir yolu var mı?

Evet. Genel toplamları hesaplamak için daha önce yapılandırdığınız **GroupBy** veri kaynağının temel veri kaynağı olarak kullanıldığı başka bir **GroupBy** veri kaynağı yapılandırın. Aşağıdaki çizimde, **GroupBy** türünün **TransportRecord** veri kaynağının **SUM** toplama işlevini temel alarak toplama **SUM** işlevini hesaplamak için kullanılan **GroupBy** türünün **Toplamlar** veri kaynağı gösterilmektedir.

![ER modeli eşleme tasarımcısındaki veri kaynağını toplar.](./media/er-groupby-data-sources-configure-model-mapping2.png)

Aşağıdaki şekilde, **Toplamlar** veri kaynağı hata ayıklamasının sonuçları gösterilmektedir.

![Hata ayıklama sayfasında, Toplamlar veri kaynağı hata ayıklamasının sonuçları.](./media/er-groupby-data-sources-debug-datasource2.png)

## <a name="additional-resources"></a>Ek kaynaklar

- [Elektronik Raporlamaya genel bakış](general-electronic-reporting.md)
- [Veri akışı ve dönüşümünü analiz etmek için yürütülen bir ER biçiminin veri kaynaklarında hata ayıklama](er-debug-data-sources.md)
- [VERİ TOPLAMA veri kaynaklarını Elektronik raporlama biçimlerinde kullanma](er-data-collection-data-sources.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
