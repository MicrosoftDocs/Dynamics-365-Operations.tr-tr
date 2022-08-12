---
title: Planlama Optimizasyonu uygunluk analizi
description: Bu makalede, geçerli ayar ve verilerinizi Planlamayı En İyi Duruma Getirme işlevinin özelliklerine göre nasıl doğrulayacağınız açıklanmaktadır.
author: t-benebo
ms.date: 06/29/2022
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
ms.openlocfilehash: e3e20b0dc782ed56e256f8fa9540f4a7a3f32ef0
ms.sourcegitcommit: 84e9946509c34a67d88c9dd9cc934d7d245ddb27
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/30/2022
ms.locfileid: "9093848"
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

> [!NOTE]
> Bazı tutarsızlıklar, Planlama Optimizasyonu uygunluk analizi tarafından belirlenemez. Daha fazla bilgi için bkz. [Klasik master planlama ile Planlama Optimizasyonu arasındaki farklar](planning-optimization-differences-with-built-in.md).

| Özellik | Listelenen sorun | Açıklama | Beklenen kullanılabilirlik |
| --- | --- | --- | --- |
| Eylemler | Eylemler hesaplaması etkin olan karşılama grupları: _\#_ | Bu özellik şimdi desteklenmektedir. | Destekleniyor |
| Temel takvimler | Temel takvimi kullanan takvimler: _\#_ | Bu özellik şimdi desteklenmektedir. | Destekleniyor | 
| Toplu iş değerlendirme kodları | Netleştirilemeyen toplu iş değerlendirme ana verileri: _\#_ | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, toplu iş değerlendirme kodları yok sayılır. | 2022 Ekim |
| Teslim edilebilir miktar (CTP) | Teslimat tarihi denetimi teslim edilebilir miktar olarak ayarlanmış varsayılan sipariş ayarları: _\#_ | Supply Chain Management 10.0.28 ve daha yeni sürümlerde, *Planlama İyileştirmesi için CTP* olarak adlandırılan bir işlemle dinamik plan çalıştırıldıktan sonra onaylanmış sevkiyat ve giriş tarihleri kullanılabilir hale gelir. Supply Chain Management'ın eski sürümleri için, Planlama İyileştirmesi etkinleştirildiğinde eski CTP ayarı yok sayılır. | Destekleniyor |
| Dinamik plana statik kopyalama | Dinamik plana statik kopyalama master planlama parametrelerinde etkinleştirildi. | Planlamayı En İyi Duruma Getirme statik planı bu ayardan bağımsız olarak dinamik plana kopyalamaz. Genel olarak, bu kavram, Planlamayı En İyi Duruma Getirme sağlayan hız ve tamamlama nedeniyle daha az ilgilidir. İki veya daha fazla plan kullanılıyorsa, master planlama her plan için tetiklenmelidir. | Yok |
| Kesinleştirme | Otomatik kesinleştirme zaman dilimi ayarlanmış karşılama grupları: _\#_ | Sürüm 10.0.7 ve sonrasında, kesinleştirme ( _Planlamayı En İyi Duruma Getirme için Otomatik kesinleştirme_ özelliğinin [Özellik yönetiminde](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) etkinleştirilmiş olması koşuluyla) ayrı bir kesinleştirme toplu işi olarak desteklenir. Planlamayı En İyi Duruma Getirme için otomatik kesinleştirmenin gereksinim tarihini (bitiş tarihi) değil, sipariş tarihini temel aldığını unutmayın. Bu davranış, planlanan siparişlerin, sağlama süresini kesinleştirme zaman dilimine dahil etmek zorunda kalmadan, vade tarihinde kesinleştirilmesini sağlar. | Destekleniyor |
| Kesinleştirme | Otomatik kesinleştirme ayarlanmış madde karşılama kayıtları: _\#_ | Sürüm 10.0.7 ve sonrasında, otomatik kesinleştirme ( _Planlamayı En İyi Duruma Getirme için Otomatik kesinleştirme_ özelliğinin [Özellik yönetiminde](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) etkinleştirilmiş olması koşuluyla) ayrı bir kesinleştirme toplu işi olarak desteklenir. Planlamayı En İyi Duruma Getirme için otomatik kesinleştirmenin gereksinim tarihini (bitiş tarihi) değil, sipariş tarihini temel aldığını unutmayın. Bu davranış, planlanan siparişlerin, sağlama süresini kesinleştirme zaman dilimine dahil etmek zorunda kalmadan, vade tarihinde kesinleştirilmesini sağlar. | Destekleniyor |
| Kesinleştirme | Otomatik kesinleştirme ayarlanmış master planlar: _\#_ | Sürüm 10.0.7 ve sonrasında, otomatik kesinleştirme ( _Planlamayı En İyi Duruma Getirme için Otomatik kesinleştirme_ özelliğinin [Özellik yönetiminde](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) etkinleştirilmiş olması koşuluyla) ayrı bir kesinleştirme toplu işi olarak desteklenir. Planlamayı En İyi Duruma Getirme için otomatik kesinleştirmenin gereksinim tarihini (bitiş tarihi) değil, sipariş tarihini temel aldığını unutmayın. Bu davranış, planlanan siparişlerin, sağlama süresini kesinleştirme zaman dilimine dahil etmek zorunda kalmadan, vade tarihinde kesinleştirilmesini sağlar. | Destekleniyor |
| FitAnalysisPlanningItems | Planlama Maddeleri: _\#_ | Bu özellik beklemededir. Şu anda, planlama maddeleri Planlamayı En İyi Duruma Getirme özelliği etkinleştirildiğinde, normal maddeler gibi işlenmektedir. | Ekim 2022 veya sonrası |
| Tahmin | "Şirketlerarası siparişleri dahil et" etkin karşılama grupları: _\#_ | Bu özellik şimdi desteklenmektedir. Ek bilgi için bkz. [Şirketlerarası planlama](Intercompany-planning.md) | Destekleniyor |
| Tahmin | "Tahmin azaltma ölçütü" ayarına sahip karşılama grupları, "Siparişler" ayarından farklı bir değere ayarlanır: _\#_ | Bu özellik şimdi desteklenmektedir. - Ek bilgi için bkz. [Talep tahmini ile master planlama](demand-forecast.md). | Destekleniyor |
| Tahmin | Alt modellere sahip tahmin modelleri: _\#_ |  Bu özellik şimdi desteklenmektedir. - Ek bilgi için bkz. [Talep tahmini ile master planlama](demand-forecast.md). | Destekleniyor |
| Tahmin | "Tedarik tahminini dahil et" seçeneğinin etkin olduğu Master planlar: _\#_ | Bu özellik beklemededir. Şu anda tedarik tahminleri, Planlamayı En İyi Duruma Getirme etkin olduğunda desteklenmez. Bu ayar ne olursa olsun yok sayılır. | Ekim 2022 veya sonrası |
| Dondurma zaman dilimi | Dondurma zaman dilimi ayarlanmış karşılama grupları: _\#_ | Bu özellik beklemededir. Şu anda, bu ayara bakılmaksızın, Planlamayı En İyi Duruma Getirme özelliği etkinleştirildiğinde, dondurma zaman dilimi ayarı yok sayılır. | 2022 Ekim |
| Dondurma zaman dilimi | Dondurma zaman dilimi ayarlanmış madde karşılama kayıtları: _\#_ | Bu özellik beklemededir. Şu anda, bu ayara bakılmaksızın, Planlamayı En İyi Duruma Getirme özelliği etkinleştirildiğinde, dondurma zaman dilimi ayarı yok sayılır. | 2022 Ekim |
| Dondurma zaman dilimi | Dondurma zaman dilimi ayarlanmış master planlar: _\#_ | Bu özellik beklemededir. Şu anda, bu ayara bakılmaksızın, Planlamayı En İyi Duruma Getirme özelliği etkinleştirildiğinde, dondurma zaman dilimi ayarı yok sayılır. | 2022 Ekim |
| Şirketlerarası | Planlanmış aşağı akış talebi dahil master planlar: _\#_ | Bu özellik şimdi desteklenmektedir. Ek bilgi için bkz. [Şirketlerarası planlama](Intercompany-planning.md) | Destekleniyor |
| Kanban | Planlanan sipariş türü kanban olan madde karşılama kayıtları: _\#_ | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, Kanban olarak ayarlanmış madde karşılama yok sayılır. Kanban planlı sipariş türü Master planlama sırasında bir uyarı oluşturacak ve planlanan satınalma siparişleri ilgili talebi kapsayacak şekilde oluşturulacaktır. | 2023 veya üstü |
| Kanban | Varsayılan sipariş türü kanban olan maddeler: _\#_ | Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, Kanban olarak ayarlanmış varsayılan sipariş türü yok sayılır. Kanban varsayılan sipariş türü Master planlama sırasında bir uyarı oluşturacak ve planlanan satınalma siparişleri ilgili talebi kapsayacak şekilde oluşturulacaktır. | 2023 veya üstü |
| Ürün yaşam döngüsü durumu | Ürün yaşam döngüsü durumları planlama için etkin değil: _\#_ | Bu özellik şimdi desteklenmektedir. Ek bilgi için bkz. [Belirli ürün yaşam döngüsü durumlarına sahip ürünleri hariç tutma](product-lifecycle-state.md) | Destekleniyor |
| Üretim | Yuvarlama veya birden fazla kurulum içeren ürün reçetesi satırları: _\#_ | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, ürün reçetesi satırlarında yuvarlama ve birden çok kurulum bu ayara bakılmaksızın yok sayılır. | 2021 Ekim |
| Üretim | Formül ölçümü içeren ürün reçetesi/formül satırları: _\#_ | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, ürün reçetesi ve formül satırlarında formül ölçümü bu ayara bakılmaksızın yok sayılır. | 2022 Ekim |
| Üretim | Madde alternatifi olan ürün reçetesi/formül satırları (plan grupları): _\#_ | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, ürün reçetesi ve formül satırlarında madde alternatifi (plan grupları) bu ayara bakılmaksızın yok sayılır. | 2022 Aralık |
| Üretim | Negatif miktara sahip ürün reçetesi/formül satırları: _\#_ | Bu özellik beklemededir. Negatif miktarı olan ürün reçetesi ve formül satırları 0 (sıfır) miktarıyla dahil edilir ve Planlamayı En İyi Duruma Getirme etkinleştirildiğinde bir uyarı verilir. Uyarılardan kaçınmak için ana verileri güncelleştirin. | 2022 Aralık |
| Üretim | Kaynak tüketimi içeren ürün reçetesi/formül satırları: _\#_ | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, kaynak tüketimi olan ürün reçetesi ve formül satırları yok sayılır. Bu özellik desteklenmeye başladığında, malzeme gereksinimi üretim başlangıç tarihi olarak ayarlanır. Bu özellik desteklenene kadar, kaynak tüketim bayrağıyla işaretlenen malzemeler için gereksinimler oluşturulmaz. | 2022 Aralık |
| Üretim | Adım tüketimi içeren ürün reçetesi/formül satırları: _\#_ | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, adım tüketimi ürün reçetesi ve formül satırında yok sayılır. | 2022 Aralık |
| Üretim | Sabit ıskarta veya değişken ıskartanın tanımlandığı ürün reçeteleri: _\#_ | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, ürün reçetelerinde tanımlanan sabit ıskarta ve değişken ıskarta yok sayılır. | 2022 Ekim |
| Üretim | Alt sözleşme içeren ürün reçeteleri: _\#_ | Bu özellik şimdi desteklenmektedir. | Destekleniyor |
| Üretim | Tesis içermeyen ürün reçeteleri: _\#_ | Bu özellik şimdi desteklenmektedir. Ek bilgi için bkz. [Üretim planlama](production-planning.md) | Destekleniyor |
| Üretim | Belirli ürün reçetesi veya rota gereksinimleri tanımlanmış talep: _\#_ | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde belirli ürün reçetesi veya talepte tanımlanan rota gereksinimleri (satış siparişindeki alt ürün reçetesi veya alt rota gibi) yok sayılır. Standart ürün reçetesi veya rota, bu ayardan bağımsız olarak kullanılır. | 2022 Aralık |
| Üretim | Ortak/Yan ürünlere içeren formül sürümleri: _\#_ | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, formül sürümüyle ilişkilendirilmiş ortak ürünler ve yan ürünler yok sayılır. | 2022 Aralık |
| Üretim | Verim içeren Formül sürümleri: _\#_ | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, formül sürümüyle ilişkilendirilmiş verim yok sayılır. | 2022 Aralık |
| Üretim | Sıralama içeren planlar: _\#_ | Bu özellik beklemededir. Şu anda, bu ayara bakılmaksızın, Planlamayı En İyi Duruma Getirme özelliği etkinleştirildiğinde, sıralama yok sayılır. | 2022 Aralık |
| Üretim | Planlanan başlangıcı bugünden önce olan başlatılmamış serbest bırakılan üretim emirleri: _\#_ | Bu özellik beklemededir. Şu anda, bir üretim emri gecikirse, master planlama bunun bugün tamamlanacağını varsayar. Bu, teslimat tarihi geçmişte olan, ancak henüz tamamlanmamış olan yayımlanmış üretim emirleriyle ilgilidir. | 2023 veya üstü |
| Üretim | Sınırlı kapasiteyle planlanan kaynaklar: _\#_ | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde sınırlı kapasiteyle zamanlanan kaynaklar yok sayılır. Planlama, üründen alınan varsayılan sağlama süresine göre yapılır. | 2022 Ekim |
| Üretim | Planlamada kullanılan rotalar: _\#_ | Bu özellik desteklenmektedir. | Destekleniyor |
| Üretim | Açılım kullanılarak satış satırı rezervasyonu: _\#_ | Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, açılım kullanan satış satırı rezervasyonu desteklenmez. | 2023 veya üstü |
| Üretim | Üretim emirlerinin açılımı ile planlama: _\#_ | Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, üretim emirlerinin açılımını kullanan planlama desteklenmez. Üretim emirleri ayrı olarak zamanlanabilir. | 2023 veya üstü |
| Teklif talepleri | Teklif talepleri etkin olan master planlar: _\#_ | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde teklif talepleri (RFQs) talep olarak değerlendirilmez. Bu ayar ne olursa olsun yok sayılır. | 2022 Aralık |
| Talepler | Taleplerin etkin olduğu master planlar: _\#_ | Bu özellik şimdi desteklenmektedir. Ek bilgi için bkz. [Satın alma talepleri](purchase-requisitions.md) | Destekleniyor |
| Emniyet marjları | Güvenlik marjına sahip karşılama grupları: _\#_ | Bu özellik şimdi desteklenmektedir. Ek bilgi için bkz. [Güvenlik marjları](safety-margins.md) | Destekleniyor |
| Emniyet marjları | Güvenlik marjına sahip master planlar: _\#_ | Bu özellik şimdi desteklenmektedir. Ek bilgi için bkz. [Güvenlik marjları](safety-margins.md) |  Destekleniyor |
| Emniyet stoğu karşılama | "Minimum karşılama" değeri "Bugünün tarihi + tedarik süresi"den farklı olan madde karşılama kayıtları: _\#_ | Planlamayı En İyi Duruma Getirme daima *Bugünün tarihi + tedarik süresi*'ni kullanır. Bu değişiklik, ileride basitleştirilmiş bir planlama kurulumuna hazırlanmak ve eyleme geçirilebilir bir sonuç sağlamak için yapılmıştır. Emniyet stoğu için tedarik zamanı dahil edilmezse, geçerli düşük eldeki stok için oluşturulan planlı siparişler, sağlama süresi nedeniyle her zaman gecikecektir. Bu davranış belirgin gürültüye ve istenmeyen planlı siparişlere neden olabilir. En iyi yöntem, *Bugünün tarihi + tedarik süresi* kullanılacak şekilde ayarı değiştirmektir. Uyarılardan kaçınmak için ana verileri güncelleştirin. | - |
| Satış teklifleri | Satış teklifleri etkin olan master planlar: _\#_ | Bu özellik beklemededir. Şu anda, Planlamayı En İyi Duruma Getirme etkinleştirildiğinde, teklifler dikkate alınmaz. Bu ayar ne olursa olsun yok sayılır. | Ekim 2022 veya sonrası |
| Raf ömrü | Raf ömrünün etkin olduğu master planlar: _\#_ | Bu özellik beklemededir. Şu anda, bu ayara bakılmaksızın, Planlamayı En İyi Duruma Getirme özelliği etkinleştirildiğinde, raf ömrü dikkate alınmaz. | 2022 Haziran |

## <a name="additional-resources"></a>Ek kaynaklar

[Planlama Optimizasyonuna genel bakış](planning-optimization-overview.md)

[Planlama Optimizasyonunu kullanmaya başlama](get-started.md)

[Klasik master planlama ile Planlama Optimizasyonu arasındaki farklar](planning-optimization-differences-with-built-in.md)

[Planlama Optimizasyonu tarafından kullanılmayan parametreler](not-used-parameters.md)

[Plan geçmişini ve planlama günlüklerini görüntüleme](plan-history-logs.md)

[Plana filtre uygulama](plan-filters.md)

[Planlama işini iptal etme](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
