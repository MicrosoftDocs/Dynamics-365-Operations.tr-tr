---
title: Planlamayı En İyi Duruma Getirme uygunluk analizi
description: Bu konuda, geçerli ayar ve verilerinizi Planlamayı En İyi Duruma Getirme işlevinin özelliklerine göre nasıl doğrulayacağınız açıklanmaktadır.
author: ChristianRytt
ms.date: 07/07/2021
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
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 308b5132056be5bc8591fdd91f6495d1811e5cd0
ms.sourcegitcommit: 73d320d2103f2b0c6ecbb2b9df746469bc544ea2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6433706"
---
# <a name="planning-optimization-fit-analysis"></a>Planlamayı En İyi Duruma Getirme uygunluk analizi

[!include [banner](../../includes/banner.md)]

Geçiş sürecinin bir parçası olarak Planlamayı En İyi Duruma Getirme için uygunluk analizinin sonucunu incelemeniz gerekir. Planlamayı En İyi Duruma Getirme kapsamının geçerli yerleşik master planlama işlevine eşit olmadığını unutmayın. İş ortağınızla birlikte çalışmanızı ve geçişe hazırlanmak için belgeleri okumanızı öneririz. 

Planlamayı EN İyi Duruma Getirme uygunluk analizi, yerleşik master planlama altyapısı ve Planlamayı En İyi Duruma Getirme arasındaki sonuç farklılıklarını belirlemenize yardımcı olur. Bu analiz, geçerli kurulumunuza ve verilerinize göre yapılır. 

Planlamayı En İyi Duruma Getirme uygunluk analizi sonucu görmek için **Master planlama** \> **Kurulum** \> **Planlamayı En İyi Duruma Getirme uygunluk analizi**'ne gidin ve **Analiz çalıştır**'ı seçin. Analizde tutarsızlıklar bulunursa bunlar aynı sayfada listelenir. (Analizin çalıştırılması birkaç dakika sürebilir.)

> [!NOTE]
> Tutarsızlıklar varsa yine de Planlamayı En İyi Duruma Getirmeye özelliğini kullanabilirsiniz. Uygunluk analizinin sonuçları yalnızca planlama servisinin geçerli ayarınızı dikkate almadığı yerleri gösterir. Başka bir deyişle, bazı işlemlerin yok sayılabileceği veya desteklenmeyebileceği yerleri gösterir.

## <a name="analysis-results-example-1"></a>Analiz sonuçları: Örnek 1

- **Özellik:** Üretim
- **Sorun:** Ürün reçetesi (BOM) düzeyi sıfırdan büyük olan maddeler: 56
- **Açıklama:** Uygunluk analizi, üretim için BOM ayarı olan 56 madde buldu. Planlamayı En İyi Duruma Getirme özelliğinin geçerli sürümü üretimi desteklemediğinden Planlamayı En İyi Duruma Getirme, planlı üretim emirleri yerine planlı satın alma emirleri oluşturur. Ayrıca etkilenen maddelerin listelendiği bir uyarı da gösterir.

## <a name="analysis-results-example-2"></a>Analiz sonuçları: Örnek 2

- **Özellik:** Eylemler
- **Sorun:** Eylem hesaplaması etkinleştirilen karşılama grupları: 6
- **Açıklama:** Uygunluk analizi, eylem hesaplamasının açık olduğu altı karşılama grubu buldu. Planlamayı En İyi Duruma Getirme özelliğinin geçerli sürümü eylemleri desteklemediğinden eylemler master planlama sırasında oluşturulur.

## <a name="overview-of-possible-results-from-the-fit-analysis"></a>Uygunluk analizinden elde edilecek olası sonuçlara genel bakış

Aşağıdaki tabloda, bir uygunluk analizinin ardından gösterilebilecek çeşitli sonuçlar gösterilmektedir. Sayı işaretleri (_\#_) listelenen soruna sahip kayıt sayısını gösteren bir sayıyla değiştirilecektir. Desteklenen veya önizlemedeki özellikler, 10.0.9 sürümünde veya sonraki sürümlerde kullanılabilir ("Beklenen kullanılabilirlik" sütununda daha üst bir sürüm numarası listelenmediği sürece).

| Özellik | Listelenen sorun | Açıklama | Beklenen kullanılabilirlik |
| --- | --- | --- | --- |
| Eylemler | Eylemler hesaplaması etkin olan karşılama grupları: _\#_ | Bu özellik beklemededir. Şu anda, bu ayara bakılmaksızın eylemler Planlamayı En İyi Duruma Getirme etkinleştirildiğinde master planlama sırasında oluşturulmaz. Eylemlerin başlıca amacı, varolan siparişlerde değişiklik önermektir. Eylemlerin iş süreçlerinizin bir parçası olarak etkin şekilde uygulanıp uygulanmadığını veya siparişlerle ilgili gecikme bilgilerinin yeterli olup olmadığı değerlendirin. | Nisan 2022 |
| Temel takvimler | Temel takvimi kullanan takvimler: _\#_ | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde temel takvim yok sayılır. İş süreçleriniz için temel takvimin gerekip gerekmediğini veya takvimlerdeki doğrudan kurulumun yeterli olup olmadığını değerlendirin. | Nisan 2022 | 
| Toplu iş değerlendirme kodları | Netleştirilemeyen toplu iş değerlendirme ana verileri: _\#_ | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, toplu iş değerlendirme kodları yok sayılır. | Ekim 2022 veya sonrası |
| Teslim edilebilir miktar (CTP) | Teslimat tarihi denetimi teslim edilebilir miktar olarak ayarlanmış varsayılan sipariş ayarları: _\#_ | Bu özellik beklemededir. Şu anda, bu ayara bakılmaksızın, Planlamayı En İyi Duruma Getirme özelliği etkinleştirildiğinde, CTP yok sayılır. | 2022 Ekim |
| Dinamik plana statik kopyalama | Dinamik plana statik kopyalama master planlama parametrelerinde etkinleştirildi. | Planlamayı En İyi Duruma Getirme statik planı bu ayardan bağımsız olarak dinamik plana kopyalamaz. Genel olarak, bu kavram, Planlamayı En İyi Duruma Getirme sağlayan hız ve tamamlama nedeniyle daha az ilgilidir. İki veya daha fazla plan kullanılıyorsa, master planlama her plan için tetiklenmelidir. | 2022 Ekim |
| Kesinleştirme | Otomatik kesinleştirme zaman dilimi ayarlanmış karşılama grupları: _\#_ | Sürüm 10.0.7 ve sonrasında, kesinleştirme ( _Planlamayı En İyi Duruma Getirme için Otomatik kesinleştirme_ özelliğinin [Özellik yönetiminde](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) etkinleştirilmiş olması koşuluyla) ayrı bir kesinleştirme toplu işi olarak desteklenir. Planlamayı En İyi Duruma Getirme için otomatik kesinleştirmenin gereksinim tarihini (bitiş tarihi) değil, sipariş tarihini temel aldığını unutmayın. Bu davranış, planlanan siparişlerin, sağlama süresini kesinleştirme zaman dilimine dahil etmek zorunda kalmadan, vade tarihinde kesinleştirilmesini sağlar. | Destekleniyor |
| Kesinleştirme | Otomatik kesinleştirme ayarlanmış madde karşılama kayıtları: _\#_ | Sürüm 10.0.7 ve sonrasında, otomatik kesinleştirme ( _Planlamayı En İyi Duruma Getirme için Otomatik kesinleştirme_ özelliğinin [Özellik yönetiminde](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) etkinleştirilmiş olması koşuluyla) ayrı bir kesinleştirme toplu işi olarak desteklenir. Planlamayı En İyi Duruma Getirme için otomatik kesinleştirmenin gereksinim tarihini (bitiş tarihi) değil, sipariş tarihini temel aldığını unutmayın. Bu davranış, planlanan siparişlerin, sağlama süresini kesinleştirme zaman dilimine dahil etmek zorunda kalmadan, vade tarihinde kesinleştirilmesini sağlar. | Destekleniyor |
| Kesinleştirme | Otomatik kesinleştirme ayarlanmış master planlar: _\#_ | Sürüm 10.0.7 ve sonrasında, otomatik kesinleştirme ( _Planlamayı En İyi Duruma Getirme için Otomatik kesinleştirme_ özelliğinin [Özellik yönetiminde](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) etkinleştirilmiş olması koşuluyla) ayrı bir kesinleştirme toplu işi olarak desteklenir. Planlamayı En İyi Duruma Getirme için otomatik kesinleştirmenin gereksinim tarihini (bitiş tarihi) değil, sipariş tarihini temel aldığını unutmayın. Bu davranış, planlanan siparişlerin, sağlama süresini kesinleştirme zaman dilimine dahil etmek zorunda kalmadan, vade tarihinde kesinleştirilmesini sağlar. | Destekleniyor |
| FitAnalysisPlanningItems | Planlama Maddeleri: _\#_ | Bu özellik beklemededir. Şu anda, planlama maddeleri Planlamayı En İyi Duruma Getirme özelliği etkinleştirildiğinde, normal maddeler gibi işlenmektedir. | Ekim 2022 veya sonrası |
| Tahmin | "Şirketlerarası siparişleri dahil et" etkin karşılama grupları: _\#_ | Bu özellik şimdi desteklenmektedir. Ek bilgi için bkz. [Şirketlerarası planlama](Intercompany-planning.md) | Destekleniyor |
| Tahmin | "Tahmin azaltma ölçütü" ayarına sahip karşılama grupları, "Siparişler" ayarından farklı bir değere ayarlanır: _\#_ | Bu özellik şimdi desteklenmektedir. - Ek bilgi için bkz. [Talep tahmini ile master planlama](demand-forecast.md). | Destekleniyor |
| Tahmin | Alt modellere sahip tahmin modelleri: _\#_ |  Bu özellik şimdi desteklenmektedir. - Ek bilgi için bkz. [Talep tahmini ile master planlama](demand-forecast.md). | Destekleniyor |
| Tahmin | "Tedarik tahminini dahil et" seçeneğinin etkin olduğu Master planlar: _\#_ | Bu özellik beklemededir. Şu anda tedarik tahminleri, Planlamayı En İyi Duruma Getirme etkin olduğunda desteklenmez. Bu ayar ne olursa olsun yok sayılır. | Ekim 2022 veya sonrası |
| Dondurma zaman dilimi | Dondurma zaman dilimi ayarlanmış karşılama grupları: _\#_ | Dondurma zaman dilimi genellikle kullanılmaz ve şu anda Planlamayı En İyi Duruma Getirme için bunun dahil edileceği plan yoktur. Şu anda, bu ayara bakılmaksızın, Planlamayı En İyi Duruma Getirme özelliği etkinleştirildiğinde, dondurma zaman dilimi ayarı yok sayılır. | - |
| Dondurma zaman dilimi | Dondurma zaman dilimi ayarlanmış madde karşılama kayıtları: _\#_ | Dondurma zaman dilimi genellikle kullanılmaz ve şu anda Planlamayı En İyi Duruma Getirme için bunun dahil edileceği plan yoktur. Şu anda, bu ayara bakılmaksızın, Planlamayı En İyi Duruma Getirme özelliği etkinleştirildiğinde, dondurma zaman dilimi ayarı yok sayılır. | - |
| Dondurma zaman dilimi | Dondurma zaman dilimi ayarlanmış master planlar: _\#_ | Dondurma zaman dilimi genellikle kullanılmaz ve şu anda Planlamayı En İyi Duruma Getirme için bunun dahil edileceği plan yoktur. Şu anda, bu ayara bakılmaksızın, Planlamayı En İyi Duruma Getirme özelliği etkinleştirildiğinde, dondurma zaman dilimi ayarı yok sayılır. | - |
| Şirketlerarası | Planlanmış aşağı akış talebi dahil master planlar: _\#_ | Bu özellik şimdi desteklenmektedir. Ek bilgi için bkz. [Şirketlerarası planlama](Intercompany-planning.md) | Destekleniyor |
| Kanban | Planlanan sipariş türü kanban olan madde karşılama kayıtları: _\#_ | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, Kanban olarak ayarlanmış madde karşılama yok sayılır. Kanban planlı sipariş türü Master planlama sırasında bir uyarı oluşturacak ve planlanan satınalma siparişleri ilgili talebi kapsayacak şekilde oluşturulacaktır. | Ekim 2022 veya sonrası |
| Kanban | Varsayılan sipariş türü kanban olan maddeler: _\#_ | Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, Kanban olarak ayarlanmış varsayılan sipariş türü yok sayılır. Kanban varsayılan sipariş türü Master planlama sırasında bir uyarı oluşturacak ve planlanan satınalma siparişleri ilgili talebi kapsayacak şekilde oluşturulacaktır. | Ekim 2022 veya sonrası |
| Ürün yaşam döngüsü durumu | Ürün yaşam döngüsü durumları planlama için etkin değil: _\#_ | Bu özellik şimdi desteklenmektedir. Ek bilgi için bkz. [Belirli ürün yaşam döngüsü olan ürünleri hariç tutma](product-lifecycle-state.md) | Destekleniyor |
| Üretim | Yuvarlama veya birden fazla kurulum içeren ürün reçetesi satırları: _\#_ | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, ürün reçetesi satırlarında yuvarlama ve birden çok kurulum bu ayara bakılmaksızın yok sayılır. | 2021 Ekim |
| Üretim | Formül ölçümü içeren ürün reçetesi/formül satırları: _\#_ | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, ürün reçetesi ve formül satırlarında formül ölçümü bu ayara bakılmaksızın yok sayılır. | 2022 Ekim |
| Üretim | Madde alternatifi olan ürün reçetesi/formül satırları (plan grupları): _\#_ | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, ürün reçetesi ve formül satırlarında madde alternatifi (plan grupları) bu ayara bakılmaksızın yok sayılır. | 2022 Ekim |
| Üretim | Negatif miktara sahip ürün reçetesi/formül satırları: _\#_ | Bu özellik beklemededir. Negatif miktarı olan ürün reçetesi ve formül satırları 0 (sıfır) miktarıyla dahil edilir ve Planlamayı En İyi Duruma Getirme etkinleştirildiğinde bir uyarı verilir. Uyarılardan kaçınmak için ana verileri güncelleştirin. | 2022 Ekim |
| Üretim | Kaynak tüketimi içeren ürün reçetesi/formül satırları: _\#_ | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, kaynak tüketimi olan ürün reçetesi ve formül satırları yok sayılır. Bu özellik desteklenmeye başladığında, malzeme gereksinimi üretim başlangıç tarihi olarak ayarlanır. Bu özellik desteklenene kadar, kaynak tüketim bayrağıyla işaretlenen malzemeler için gereksinimler oluşturulmaz. | 2022 Ekim |
| Üretim | Adım tüketimi içeren ürün reçetesi/formül satırları: _\#_ | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, adım tüketimi ürün reçetesi ve formül satırında yok sayılır. | 2022 Ekim |
| Üretim | Sabit ıskarta veya değişken ıskartanın tanımlandığı ürün reçeteleri: _\#_ | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, ürün reçetelerinde tanımlanan sabit ıskarta ve değişken ıskarta yok sayılır. | 2022 Ekim |
| Üretim | Alt sözleşme içeren ürün reçeteleri: _\#_ | Bu özellik beklemededir. Şu anda, bu ayara bakılmaksızın, Planlamayı En İyi Duruma Getirme özelliği etkinleştirildiğinde, ürün reçetelerindeki alr sözleşme ayarı yok sayılır. | Nisan 2022 |
| Üretim | Tesis içermeyen ürün reçeteleri: _\#_ | Bu özellik şimdi desteklenmektedir. Ek bilgi için bkz. [Ürün planlama](production-planning.md) | Destekleniyor |
| Üretim | Belirli ürün reçetesi veya rota gereksinimleri tanımlanmış talep: _\#_ | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde belirli ürün reçetesi veya talepte tanımlanan rota gereksinimleri (satış siparişindeki alt ürün reçetesi veya alt rota gibi) yok sayılır. Standart ürün reçetesi veya rota, bu ayardan bağımsız olarak kullanılır. | 2022 Ekim |
| Üretim | Ortak/Yan ürünlere içeren formül sürümleri: _\#_ | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, formül sürümüyle ilişkilendirilmiş ortak ürünler ve yan ürünler yok sayılır. | 2022 Ekim |
| Üretim | Verim içeren Formül sürümleri: _\#_ | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, formül sürümüyle ilişkilendirilmiş verim yok sayılır. | 2022 Ekim |
| Üretim | Sıralama içeren planlar: _\#_ | Bu özellik beklemededir. Şu anda, bu ayara bakılmaksızın, Planlamayı En İyi Duruma Getirme özelliği etkinleştirildiğinde, sıralama yok sayılır. | 2022 Ekim |
| Üretim | Planlanan başlangıcı bugünden önce olan başlatılmamış serbest bırakılan üretim emirleri: _\#_ | Bu özellik beklemededir. Şu anda, bir üretim emri gecikirse, master planlama bunun bugün tamamlanacağını varsayar. Bu, teslimat tarihi geçmişte olan, ancak henüz tamamlanmamış olan yayımlanmış üretim emirleriyle ilgilidir. | 2022 Ekim |
| Üretim | Sınırlı kapasiteyle planlanan kaynaklar: _\#_ | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde sınırlı kapasiteyle zamanlanan kaynaklar yok sayılır. Planlama, üründen alınan varsayılan sağlama süresine göre yapılır. | 2022 Ekim |
| Üretim | Planlamada kullanılan rotalar: _\#_ | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, rotalar yok sayılır. Ürünün varsayılan sağlama süresi kullanılır. | Önizleme: Sesteklenen (10.0.20), Genel kullanıma sunma: 2021 Ekim |
| Üretim | Açılım kullanılarak satış satırı rezervasyonu: _\#_ | Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, açılım kullanan satış satırı rezervasyonu desteklenmez. | 2022 Ekim |
| Üretim | Üretim emirlerinin açılımı ile planlama: _\#_ | Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, üretim emirlerinin açılımını kullanan planlama desteklenmez. Üretim emirleri ayrı olarak zamanlanabilir. | 2022 Ekim |
| Teklif talepleri | Teklif talepleri etkin olan master planlar: _\#_ | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde teklif talepleri (RFQs) talep olarak değerlendirilmez. Bu ayar ne olursa olsun yok sayılır. | 2022 Ekim |
| Talepler | Taleplerin etkin olduğu master planlar: _\#_ | Bu özellik şimdi desteklenmektedir. Ek bilgi için bkz. [Satın alma talepleri](purchase-requisitions.md) | Destekleniyor |
| Güvenlik marjları | Emniyet marjına sahip karşılama grupları: _\#_ | Bu özellik şimdi kısmen desteklenmektedir. Ek bilgi için bkz. [Güvenlik marjları](safety-margins.md) | Giriş marjı: Desteklenir. Sipariş yenileme sınırı ve çıkış marjı: Ocak 2022 |
| Güvenlik marjları | Emniyet marjına sahip master planlar: _\#_ | Bu özellik şimdi kısmen desteklenmektedir. Ek bilgi için bkz. [Güvenlik marjları](safety-margins.md) | Giriş marjı: Desteklenir. Sipariş yenileme sınırı ve çıkış marjı: Ocak 2022 |
| Emniyet stoğu karşılama | "Minimum karşılama" değeri "Bugünün tarihi + tedarik süresi"den farklı olan madde karşılama kayıtları: _\#_ | Planlamayı En İyi Duruma Getirme daima *Bugünün tarihi + tedarik süresi*'ni kullanır. Bu değişiklik, ileride basitleştirilmiş bir planlama kurulumuna hazırlanmak ve eyleme geçirilebilir bir sonuç sağlamak için yapılmıştır. Emniyet stoğu için tedarik zamanı dahil edilmezse, geçerli düşük eldeki stok için oluşturulan planlı siparişler, sağlama süresi nedeniyle her zaman gecikecektir. Bu davranış belirgin gürültüye ve istenmeyen planlı siparişlere neden olabilir. En iyi yöntem, *Bugünün tarihi + tedarik süresi* kullanılacak şekilde ayarı değiştirmektir. Uyarılardan kaçınmak için ana verileri güncelleştirin. | - |
| Satış teklifleri | Satış teklifleri etkin olan master planlar: _\#_ | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, teklifler dikkate alınmaz. Bu ayar ne olursa olsun yok sayılır. | Ekim 2022 veya sonrası |
| Raf ömrü | Raf ömrünün etkin olduğu master planlar: _\#_ | Bu özellik beklemededir. Şu anda, bu ayara bakılmaksızın, Planlamayı En İyi Duruma Getirme özelliği etkinleştirildiğinde, raf ömrü dikkate alınmaz. | Nisan 2022 |

## <a name="additional-resources"></a>Ek kaynaklar

[Planlama Optimizasyonuna genel bakış](planning-optimization-overview.md)

[Planlama Optimizasyonunu kullanmaya başlama](get-started.md)

[Plan geçmişini ve planlama günlüklerini görüntüleme](plan-history-logs.md)

[Plana filtre uygulama](plan-filters.md)

[Planlama işini iptal etme](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
