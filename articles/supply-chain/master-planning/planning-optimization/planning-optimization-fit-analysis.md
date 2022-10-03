---
title: Planlama Optimizasyonu uygunluk analizi
description: Bu makalede, geçerli ayar ve verilerinizi Planlamayı En İyi Duruma Getirme işlevinin özelliklerine göre nasıl doğrulayacağınız açıklanmaktadır.
author: t-benebo
ms.date: 08/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsFitAnalysis, MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 7e32b3ed6ed96de7193cc496e0630969137cd0c1
ms.sourcegitcommit: 15b331f39d6e3ef811b9c2bf055a4f5b4572bae2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/26/2022
ms.locfileid: "9591863"
---
# <a name="planning-optimization-fit-analysis"></a>Planlamayı En İyi Duruma Getirme uygunluk analizi

[!include [banner](../../includes/banner.md)]

Geçiş sürecinin bir parçası olarak Planlamayı En İyi Duruma Getirme için uygunluk analizinin sonucunu incelemeniz gerekir. Planlamayı En İyi Duruma Getirme kapsamının geçerli yerleşik master planlama işlevine eşit olmadığını unutmayın. İş ortağınızla birlikte çalışmanızı ve geçişe hazırlanmak için belgeleri okumanızı öneririz. 

Planlamayı EN İyi Duruma Getirme uygunluk analizi, yerleşik master planlama altyapısı ve Planlamayı En İyi Duruma Getirme arasındaki sonuç farklılıklarını belirlemenize yardımcı olur. Bu analiz, geçerli kurulumunuza ve verilerinize göre yapılır. 

Planlamayı En İyi Duruma Getirme uygunluk analizi sonucu görmek için **Master planlama** \> **Kurulum** \> **Planlamayı En İyi Duruma Getirme uygunluk analizi**'ne gidin ve **Analiz çalıştır**'ı seçin. Analizde tutarsızlıklar bulunursa bunlar aynı sayfada listelenir. (Analizin çalıştırılması birkaç dakika sürebilir.)

> [!NOTE]
>
> - Bazı tutarsızlıklar, Planlama Optimizasyonu uygunluk analizi tarafından belirlenemez. Daha fazla bilgi için bkz. [Klasik master planlama ile Planlama Optimizasyonu arasındaki farklar](planning-optimization-differences-with-built-in.md).
>
> - Tutarsızlıklar varsa yine de Planlamayı En İyi Duruma Getirmeye özelliğini kullanabilirsiniz. Uygunluk analizinin sonuçları yalnızca planlama servisinin geçerli ayarınızı dikkate almadığı yerleri gösterir. Başka bir deyişle, bazı işlemlerin yok sayılabileceği veya desteklenmeyebileceği yerleri gösterir.

## <a name="analysis-results-example-1"></a>Analiz sonuçları: Örnek 1

- **Özellik:** Üretim
- **Sorun:** Ürün reçetesi (BOM) düzeyi sıfırdan büyük olan maddeler: 56
- **Açıklama:** Uygunluk analizi, üretim için BOM ayarı olan 56 madde buldu. Planlamayı En İyi Duruma Getirme özelliğinin geçerli sürümü üretimi desteklemediğinden Planlamayı En İyi Duruma Getirme, planlı üretim emirleri yerine planlı satın alma emirleri oluşturur. Ayrıca etkilenen maddelerin listelendiği bir uyarı da gösterir.

## <a name="analysis-results-example-2"></a>Analiz sonuçları: Örnek 2

- **Özellik:** Eylemler
- **Sorun:** Eylem hesaplaması etkinleştirilen karşılama grupları: 6
- **Açıklama:** Uygunluk analizi, eylem hesaplamasının açık olduğu altı karşılama grubu buldu. Planlamayı En İyi Duruma Getirme özelliğinin geçerli sürümü eylemleri desteklemediğinden eylemler master planlama sırasında oluşturulur.

## <a name="overview-of-possible-results-from-the-fit-analysis"></a>Uygunluk analizinden elde edilecek olası sonuçlara genel bakış

Aşağıdaki tabloda, bir uygunluk analizinin ardından gösterilebilecek çeşitli sonuçlar gösterilmektedir. Sayı işaretleri (*\#*) listelenen soruna sahip kayıt sayısını gösteren bir sayıyla değiştirilecektir.

> [!IMPORTANT]
> Henüz desteklenmeyen özellikler için aşağıdaki tablo, geçerli yol haritasını temel alarak tahmini olan beklenen kullanılabilirlik bilgilerini sağlar. Bu tahminler, herhangi bir bildirimde bulunmadan değiştirilebilir.

| Özellik | Listelenen sorun | Açıklama | Beklenen kullanılabilirlik |
| --- | --- | --- | --- |
| Eylemler | Eylemler hesaplaması etkin olan karşılama grupları: *\#* | Bu özellik şimdi desteklenmektedir. | Destekleniyor |
| Temel takvimler | Temel takvimi kullanan takvimler: *\#* | Bu özellik şimdi desteklenmektedir. | Destekleniyor | 
| Toplu iş değerlendirme kodları | Netleştirilemeyen toplu iş değerlendirme ana verileri: *\#* | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, toplu iş değerlendirme kodları yok sayılır. | 2022 sürüm 2 <!-- KFM: Now available? [Use batch disposition codes to mark batches as available or unavailable](../../inventory/batch-disposition-codes.md) --> |
| Teslim edilebilir miktar (CTP) | Teslimat tarihi denetimi teslim edilebilir miktar olarak ayarlanmış varsayılan sipariş ayarları: *\#* | Supply Chain Management 10.0.28 ve daha yeni sürümlerde, *Planlama İyileştirmesi için CTP* olarak adlandırılan bir işlemle dinamik plan çalıştırıldıktan sonra onaylanmış sevkiyat ve giriş tarihleri kullanılabilir hale gelir. Supply Chain Management'ın eski sürümleri için, Planlama İyileştirmesi etkinleştirildiğinde eski CTP ayarı yok sayılır. | Destekleniyor |
| Dinamik plana statik kopyalama | Dinamik plana statik kopyalama master planlama parametrelerinde etkinleştirildi. | Planlamayı En İyi Duruma Getirme statik planı bu ayardan bağımsız olarak dinamik plana kopyalamaz. Genel olarak, bu kavram, Planlamayı En İyi Duruma Getirme sağlayan hız ve tamamlama nedeniyle daha az ilgilidir. İki veya daha fazla plan kullanılıyorsa, master planlama her plan için tetiklenmelidir. | Yok |
| Kesinleştirme | Otomatik kesinleştirme zaman dilimi ayarlanmış karşılama grupları: *\#* | Sürüm 10.0.7 ve sonrasında, kesinleştirme ( *Planlamayı En İyi Duruma Getirme için Otomatik kesinleştirme* özelliğinin [Özellik yönetiminde](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) etkinleştirilmiş olması koşuluyla) ayrı bir kesinleştirme toplu işi olarak desteklenir. Planlamayı En İyi Duruma Getirme için otomatik kesinleştirmenin gereksinim tarihini (bitiş tarihi) değil, sipariş tarihini temel aldığını unutmayın. Bu davranış, planlanan siparişlerin, sağlama süresini kesinleştirme zaman dilimine dahil etmek zorunda kalmadan, vade tarihinde kesinleştirilmesini sağlar. | Destekleniyor |
| Kesinleştirme | Otomatik kesinleştirme ayarlanmış madde karşılama kayıtları: *\#* | Sürüm 10.0.7 ve sonrasında, otomatik kesinleştirme ( *Planlamayı En İyi Duruma Getirme için Otomatik kesinleştirme* özelliğinin [Özellik yönetiminde](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) etkinleştirilmiş olması koşuluyla) ayrı bir kesinleştirme toplu işi olarak desteklenir. Planlamayı En İyi Duruma Getirme için otomatik kesinleştirmenin gereksinim tarihini (bitiş tarihi) değil, sipariş tarihini temel aldığını unutmayın. Bu davranış, planlanan siparişlerin, sağlama süresini kesinleştirme zaman dilimine dahil etmek zorunda kalmadan, vade tarihinde kesinleştirilmesini sağlar. | Destekleniyor |
| Kesinleştirme | Otomatik kesinleştirme ayarlanmış master planlar: *\#* | Sürüm 10.0.7 ve sonrasında, otomatik kesinleştirme ( *Planlamayı En İyi Duruma Getirme için Otomatik kesinleştirme* özelliğinin [Özellik yönetiminde](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) etkinleştirilmiş olması koşuluyla) ayrı bir kesinleştirme toplu işi olarak desteklenir. Planlamayı En İyi Duruma Getirme için otomatik kesinleştirmenin gereksinim tarihini (bitiş tarihi) değil, sipariş tarihini temel aldığını unutmayın. Bu davranış, planlanan siparişlerin, sağlama süresini kesinleştirme zaman dilimine dahil etmek zorunda kalmadan, vade tarihinde kesinleştirilmesini sağlar. | Destekleniyor |
| FitAnalysisPlanningItems | Planlama Maddeleri: *\#* | Bu özellik beklemededir. Şu anda, planlama maddeleri Planlamayı En İyi Duruma Getirme özelliği etkinleştirildiğinde, normal maddeler gibi işlenmektedir. | 2022 sürüm 2 veya sonrası |
| Tahmin | "Şirketlerarası siparişleri dahil et" etkin karşılama grupları: *\#* | Bu özellik şimdi desteklenmektedir. Ek bilgi için bkz. [Şirketlerarası planlama](Intercompany-planning.md) | Destekleniyor |
| Tahmin | "Tahmin azaltma ölçütü" ayarına sahip karşılama grupları, "Siparişler" ayarından farklı bir değere ayarlanır: *\#* | Bu özellik şimdi desteklenmektedir. - Ek bilgi için bkz. [Talep tahmini ile master planlama](demand-forecast.md). | Destekleniyor |
| Tahmin | Alt modellere sahip tahmin modelleri: *\#* |  Bu özellik şimdi desteklenmektedir. - Ek bilgi için bkz. [Talep tahmini ile master planlama](demand-forecast.md). | Destekleniyor |
| Tahmin | "Tedarik tahminini dahil et" seçeneğinin etkin olduğu Master planlar: *\#* | Bu özellik beklemededir. Şu anda tedarik tahminleri, Planlamayı En İyi Duruma Getirme etkin olduğunda desteklenmez. Bu ayar ne olursa olsun yok sayılır. | 2022 sürüm 2 veya sonrası |
| Dondurma zaman dilimi | Dondurma zaman dilimi ayarlanmış karşılama grupları: *\#* | Bu özellik beklemededir. Şu anda, bu ayara bakılmaksızın, Planlamayı En İyi Duruma Getirme özelliği etkinleştirildiğinde, dondurma zaman dilimi ayarı yok sayılır. | 2022 sürüm 2 |
| Dondurma zaman dilimi | Dondurma zaman dilimi ayarlanmış madde karşılama kayıtları: *\#* | Bu özellik beklemededir. Şu anda, bu ayara bakılmaksızın, Planlamayı En İyi Duruma Getirme özelliği etkinleştirildiğinde, dondurma zaman dilimi ayarı yok sayılır. | 2022 sürüm 2 |
| Dondurma zaman dilimi | Dondurma zaman dilimi ayarlanmış master planlar: *\#* | Bu özellik beklemededir. Şu anda, bu ayara bakılmaksızın, Planlamayı En İyi Duruma Getirme özelliği etkinleştirildiğinde, dondurma zaman dilimi ayarı yok sayılır. | 2022 sürüm 2 |
| Şirketlerarası | Planlanmış aşağı akış talebi dahil master planlar: *\#* | Bu özellik şimdi desteklenmektedir. Ek bilgi için bkz. [Şirketlerarası planlama](Intercompany-planning.md) | Destekleniyor |
| Kanban | Planlanan sipariş türü kanban olan madde karşılama kayıtları: *\#* | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, Kanban olarak ayarlanmış madde karşılama yok sayılır. Kanban planlı sipariş türü Master planlama sırasında bir uyarı oluşturacak ve planlanan satınalma siparişleri ilgili talebi kapsayacak şekilde oluşturulacaktır. | Gelecekteki dalga |
| Kanban | Varsayılan sipariş türü kanban olan maddeler: *\#* | Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, Kanban olarak ayarlanmış varsayılan sipariş türü yok sayılır. Kanban varsayılan sipariş türü Master planlama sırasında bir uyarı oluşturacak ve planlanan satınalma siparişleri ilgili talebi kapsayacak şekilde oluşturulacaktır. | Gelecekteki dalga |
| Ürün yaşam döngüsü durumu | Ürün yaşam döngüsü durumları planlama için etkin değil: *\#* | Bu özellik şimdi desteklenmektedir. Ek bilgi için bkz. [Belirli ürün yaşam döngüsü durumlarına sahip ürünleri hariç tutma](product-lifecycle-state.md) | Destekleniyor |
| Üretim | Yuvarlama veya birden fazla kurulum içeren ürün reçetesi satırları: *\#* | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, ürün reçetesi satırlarında yuvarlama ve birden çok kurulum bu ayara bakılmaksızın yok sayılır. | Gelecekteki dalga|
| Üretim | Formül ölçümü içeren ürün reçetesi/formül satırları: *\#* | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, ürün reçetesi ve formül satırlarında formül ölçümü bu ayara bakılmaksızın yok sayılır. | 2022 sürüm 2 |
| Üretim | Madde alternatifi olan ürün reçetesi/formül satırları (plan grupları): *\#* | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, ürün reçetesi ve formül satırlarında madde alternatifi (plan grupları) bu ayara bakılmaksızın yok sayılır. | 2022 sürüm 2 |
| Üretim | Negatif miktara sahip ürün reçetesi/formül satırları: *\#* | Bu özellik beklemededir. Negatif miktarı olan ürün reçetesi ve formül satırları 0 (sıfır) miktarıyla dahil edilir ve Planlamayı En İyi Duruma Getirme etkinleştirildiğinde bir uyarı verilir. Uyarılardan kaçınmak için ana verileri güncelleştirin. | 2022 sürüm 2 |
| Üretim | Kaynak tüketimi içeren ürün reçetesi/formül satırları: *\#* | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, kaynak tüketimi olan ürün reçetesi ve formül satırları yok sayılır. Bu özellik desteklenmeye başladığında, malzeme gereksinimi üretim başlangıç tarihi olarak ayarlanır. Bu özellik desteklenene kadar, kaynak tüketim bayrağıyla işaretlenen malzemeler için gereksinimler oluşturulmaz. | 2022 sürüm 2 |
| Üretim | Adım tüketimi içeren ürün reçetesi/formül satırları: *\#* | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, adım tüketimi ürün reçetesi ve formül satırında yok sayılır. | 2022 sürüm 2 |
| Üretim | Sabit ıskarta veya değişken ıskartanın tanımlandığı ürün reçeteleri: *\#* | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, ürün reçetelerinde tanımlanan sabit ıskarta ve değişken ıskarta yok sayılır. | 2022 sürüm 2 |
| Üretim | Alt sözleşme içeren ürün reçeteleri: *\#* | Bu özellik şimdi desteklenmektedir. | Destekleniyor |
| Üretim | Tesis içermeyen ürün reçeteleri: *\#* | Bu özellik şimdi desteklenmektedir. Ek bilgi için bkz. [Üretim planlama](production-planning.md) | Destekleniyor |
| Üretim | Belirli ürün reçetesi veya rota gereksinimleri tanımlanmış talep: *\#* | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde belirli ürün reçetesi veya talepte tanımlanan rota gereksinimleri (satış siparişindeki alt ürün reçetesi veya alt rota gibi) yok sayılır. Standart ürün reçetesi veya rota, bu ayardan bağımsız olarak kullanılır. | 2022 sürüm 2 |
| Üretim | Ortak/Yan ürünlere içeren formül sürümleri: *\#* | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, formül sürümüyle ilişkilendirilmiş ortak ürünler ve yan ürünler yok sayılır. | 2022 sürüm 2 |
| Üretim | Verim içeren Formül sürümleri: *\#* | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, formül sürümüyle ilişkilendirilmiş verim yok sayılır. | 2022 sürüm 2 |
| Üretim | Sıralama içeren planlar: *\#* | Bu özellik beklemededir. Şu anda, bu ayara bakılmaksızın, Planlamayı En İyi Duruma Getirme özelliği etkinleştirildiğinde, sıralama yok sayılır. | 2022 sürüm 2 |
| Üretim | Planlanan başlangıcı bugünden önce olan başlatılmamış serbest bırakılan üretim emirleri: *\#* | Bu özellik beklemededir. Şu anda, bir üretim emri gecikirse, master planlama bunun bugün tamamlanacağını varsayar. Bu, teslimat tarihi geçmişte olan, ancak henüz tamamlanmamış olan yayımlanmış üretim emirleriyle ilgilidir. | Gelecekteki dalga |
| Üretim | Sınırlı kapasiteyle planlanan kaynaklar: *\#* | Bu özellik şimdi desteklenmektedir.| Destekleniyor |
| Üretim | Planlamada kullanılan rotalar: *\#* | Bu özellik desteklenmektedir. | Destekleniyor |
| Üretim | Açılım kullanılarak satış satırı rezervasyonu: *\#* | Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, açılım kullanan satış satırı rezervasyonu desteklenmez. | Gelecekteki dalga |
| Üretim | Üretim emirlerinin açılımı ile planlama: *\#* | Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, üretim emirlerinin açılımını kullanan planlama desteklenmez. Üretim emirleri ayrı olarak zamanlanabilir. | Gelecekteki dalga |
| Teklif talepleri | Teklif talepleri etkin olan master planlar: *\#* | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde teklif talepleri (RFQs) talep olarak değerlendirilmez. Bu ayar ne olursa olsun yok sayılır. | 2022 sürüm 2 |
| Talepler | Taleplerin etkin olduğu master planlar: *\#* | Bu özellik şimdi desteklenmektedir. Ek bilgi için bkz. [Satın alma talepleri](purchase-requisitions.md) | Destekleniyor |
| Emniyet marjları | Güvenlik marjına sahip karşılama grupları: *\#* | Bu özellik şimdi desteklenmektedir. Ek bilgi için bkz. [Güvenlik marjları](safety-margins.md) | Destekleniyor |
| Emniyet marjları | Güvenlik marjına sahip master planlar: *\#* | Bu özellik şimdi desteklenmektedir. Ek bilgi için bkz. [Güvenlik marjları](safety-margins.md) |  Destekleniyor |
| Emniyet stoğu karşılama | "Minimum karşılama" değeri "Bugünün tarihi + tedarik süresi"den farklı olan madde karşılama kayıtları: *\#* | Planlamayı En İyi Duruma Getirme daima *Bugünün tarihi + tedarik süresi*'ni kullanır. Bu değişiklik, ileride basitleştirilmiş bir planlama kurulumuna hazırlanmak ve eyleme geçirilebilir bir sonuç sağlamak için yapılmıştır. Emniyet stoğu için tedarik zamanı dahil edilmezse, geçerli düşük eldeki stok için oluşturulan planlı siparişler, sağlama süresi nedeniyle her zaman gecikecektir. Bu davranış belirgin gürültüye ve istenmeyen planlı siparişlere neden olabilir. En iyi yöntem, *Bugünün tarihi + tedarik süresi* kullanılacak şekilde ayarı değiştirmektir. Uyarılardan kaçınmak için ana verileri güncelleştirin. | - |
| Satış teklifleri | Satış teklifleri etkin olan master planlar: *\#* | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, teklifler dikkate alınmaz. Bu ayar ne olursa olsun yok sayılır. | 2022 sürüm 2 veya sonrası |
| Raf ömrü | Raf ömrünün etkin olduğu master planlar: *\#* | Bu özellik beklemededir. Şu anda, bu ayara bakılmaksızın, Planlamayı En İyi Duruma Getirme özelliği etkinleştirildiğinde, raf ömrü dikkate alınmaz. | Destekleniyor |

## <a name="additional-resources"></a>Ek kaynaklar

[Planlama Optimizasyonuna genel bakış](planning-optimization-overview.md)

[Planlama Optimizasyonunu kullanmaya başlama](get-started.md)

[Klasik master planlama ile Planlama Optimizasyonu arasındaki farklar](planning-optimization-differences-with-built-in.md)

[Planlama Optimizasyonu tarafından kullanılmayan parametreler](not-used-parameters.md)

[Plan geçmişini ve planlama günlüklerini görüntüleme](plan-history-logs.md)

[Plana filtre uygulama](plan-filters.md)

[Planlama işini iptal etme](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
