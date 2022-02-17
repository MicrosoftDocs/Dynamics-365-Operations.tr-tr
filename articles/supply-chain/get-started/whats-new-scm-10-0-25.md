---
title: Dynamics 365 Supply Chain Management 10.0.25 (Nisan 2022) Önizlemesi
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management 10.0.25'daki yeni veya değişen özellikler açıklanmaktadır.
author: kamaybac
ms.date: 02/01/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 0ce9bc4685542cf691d862c0fec76f3f7b40c6b6
ms.sourcegitcommit: 7893ffb081c36838f110fadf29a183f9bdb72dd3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/02/2022
ms.locfileid: "8087332"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10025-april-2022"></a>Dynamics 365 Supply Chain Management 10.0.25 (Nisan 2022) Önizlemesi

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bu konuda, Microsoft Dynamics 365 Supply Chain Management önizleme sürümü 10.0.25'deki yeni veya değişen özellikler listelenmektedir. Bu sürüm, 10.0.1149 derleme numarasına sahiptir ve aşağıdaki gibi kullanıma sunulmuştur:

- **Sürüm önizlemesi:** Şubat 2022
- **Sürüm genel kullanılabilirliği (kendi kendine güncelleştirme):** Mart 2022
- **Sürüm genel kullanılabilirliği (otomatik güncelleştirme):** Nisan 2022

## <a name="features-included-in-this-release"></a>Bu sürümdeki özellikler

Aşağıdaki tabloda, bu sürüme dahil edilen özellikler listelenmektedir. Bu konu ilk kez yayımlandıktan sonra derlemeye eklenen özellikleri dahil etmek için bu konuya güncelleştirmeler uygulayabiliriz.

| Özellik alanı | Özellik | Daha fazla bilgi | Etkinleştiren |
|---|---|---|---|
| Stok&nbsp;ve&nbsp;lojistik | Tehlikeli maddeler geliştirmeleri | Bu geliştirmeler, şirketlerin farklı coğrafyalarda tehlikeli maddeler taşırken yerel düzenlemelere daha iyi uyum sağlamalarına yardımcı olmak için mevcut tehlikeli madde işlevselliğini oluşturur. <!-- KFM: Update to 2022w1 link when published -->| Özellik yönetimi:<br>*Tehlikeli maddeler geliştirmeleri* |
| Stok&nbsp;ve&nbsp;lojistik | Sevk istasyonları için sevk işi | Bu özellik, paketleme ve nakliye operasyonlarınızın esnekliğini ve çevikliğini büyük ölçüde artırır. Paketleme işlemi sırasında, ambar çalışanları artık aynı sevkiyat ve yük ile ilgili tek tek parselleri paketleyebilir ve gönderebilir. Bazı maddeler hemen sevkiyata hazırsa, aynı sevk irsaliyesinin parçası olan sipariş satırlarının birlikte sevk edilmesi gerekmez. Tek bir sipariş, farklı nakliye zamanlarında birden fazla parselde paketlenebilir ve gönderilebilir, böylece bekleme süreleri azaltılabilir ve çeviklik artırılabilir.<!-- KFM: Update to 2022w1 link when published --> | Özellik yönetimi:<br>*Sevk istasyonları için sevk işi* |
| Stok&nbsp;ve&nbsp;lojistik | [GS1 biçimi standartlarını kullanarak ambarda barkodları tarama](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) <!-- KFM: Update to 2022w1 link when published --> | [GS1 barkodları ve QR kodları](../warehousing/gs1-barcodes.md) | Özellik yönetimi:<br>*GS1 barkodlarını tara* |
| İmalat | [Üretim katı yürütme arabiriminde malzeme tüketimi ve ayırmalar](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/material-consumption-reservations-production-floor-execution-interface) | [Çalışanlar üretim katı yürütme arabirimini nasıl kullanır?](../production-control/production-floor-execution-use.md) | Özellik yönetimi:<br>*(Önizleme) Üretim katı yürütme arabiriminde (WMS özellikli) malzeme tüketimini kaydet* |
| İmalat | [Malzeme tüketimini ölçek birimlerinde kaydetme](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/register-material-consumption-scale-units) | [Bulut ve uç ölçek birimleri için üretim yürütme iş yükleri](../cloud-edge/cloud-edge-workload-manufacturing.md) | Özellik yönetimi:<br>*Mobil uygulamadaki malzeme tüketimini bir ölçek birimine kaydet* |
| Planlama | [Mevcut arzı iyileştirmek için Planlama İyileştirmesi önerileri](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-suggestions-optimize-existing-supply) | [Eylem iletileri](../master-planning/action-messages.md) | Varsayılan olarak etkin |
| Planlama | Basitleştirilmiş planlı siparişler | [Basitleştirilmiş planlı siparişler](../master-planning/planning-optimization/planned-orders-simplified.md ) | Özellik yönetimi:<br>*Basitleştirilmiş planlı siparişler* |

## <a name="feature-enhancements-included-in-this-release"></a>Bu sürümdeki özellik iyileştirmeleri

Aşağıdaki tabloda, bu sürümde dahil edilen özellik iyileştirmeleri listelenmektedir. Bu iyileştirmelerden her biri, mevcut bir özellik için artımlı bir geliştirme sağlar. Bunlar yalnızca iyileştirme olduğundan [sürüm planında](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features) listelenmez. Ancak, bu geliştirmelerin mevcut özelleştirmelerinizle veya tercihlerinizle çakışmayacağından emin olmak için, her biri varsayılan olarak kapatılmıştır (aksi belirtilmedikçe).

Bu özelliklerden herhangi birini açmak veya kapatmak istiyorsanız bunu [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) yapmalısınız.

| Modül | Özellik yönetiminde özellik adı | Daha fazla bilgi |
|---|---|---|
| Stok ve ambar yönetimi | (Polonya) Çeşitli SAD faturalarını bir SAD içinde bir Satınalma sipariş satırına bağlamaya izin ver | Bu özellik, birkaç farklı fatura için (farklı sevk irsaliyeleri gibi) satınalma siparişi satırları deftere nakledildiğinde satınalma siparişi satırlarını bölmenize ve bunları tek bir yönetim belgesine (SAD) bağlamanıza olanak tanır. |
| Tedarik ve kaynak atama | Muhasebe tarihine göre birden fazla satınalma taleplerini tek bir satınalma siparişi içinde konsolide et | Bu özellik, farklı satınalma taleplerinin farklı muhasebe tarihleri varsa birden çok satınalma siparişinin tek bir satınalma siparişinde birleştirilmesine olanak tanır. Satınalma siparişi oluşturma ve talep konsolidasyon satınalma ilkesi kuralları, talep satırlarının satınalma siparişi düzeyindeki muhasebe tarihine göre gruplandırılmasına ilişkin kararı otomatikleştirmek için ayarlanabilir. Hesap tarihi bütçe ayırmaları ve taahhütleri için kullanıldığından, bütçe denetimi etkinleştirildiğinde muhasebe tarihine göre satınalma siparişi konsolidasyonu desteklenmez. Bu nedenle, satınalma talebinden satınalma siparişime geçiş sırasında tutulmalıdır. |
| Tedarik ve kaynak atama | Satınalma Talebi Dağıtımı Sıfırlama Düğmesini devre dışı bırak | Bu özellik, gözden geçirilmiş satınalma taleplerinde **Muhasebe dağıtımı** sayfasındaki **Sıfırla** düğmesini devre dışı bırakır. |
| Tedarik ve kaynak atama | Eski varsayılan RFQ yanıt alanı ayarlarını görüntüle | Bu özellik, daha önce kullanıcı arabiriminden kaldırılan eski varsayılan teklif talebi (RFQ) yanıt alanı ayarlarını yeniden sunar. Bu ayarlar kullanıma hazır herhangi bir işlevsellik sağlamaz ancak gerektiği gibi sağlamak için özelleştirilebilir. Kuruluşunuz varsayılan RFQ yanıt alanı ayarları için işlevsellik eklediyse veya eklemeyi planlıyorsa bu özelliği etkinleştirin. Bu özellik etkinleştirildiğinde, **Tedarik ve kaynak parametreleri** sayfasına giderek, **Teklif talebi** sekmesini açarak ve **Teklif için varsayılan istek yanıt alanları** nı seçerek ayarlara erişebilirsiniz. |
| Tedarik ve kaynak atama | Satınalma siparişinde etkin boyut bağlantısı mali boyutuyla satıcıdan alınan mali boyutları birleştir | Bu özellik, bir mali boyut ile site stok boyutu arasında bir bağlantı ayarlarsanız, satınalma talep onayından sonra satıcılardan gelen mali boyutları etkin boyut bağlantısı mali boyutlarıyla birleştirmenizi sağlar. Satınalma siparişi oluşturma ve talep konsolidasyon satınalma ilkesi kuralları, satınalma siparişi başlığı düzeyinde etkin boyut bağlantısı mali boyutu olan satıcılardan mali boyutları birleştirme kararını yönlendirmek için ayarlanabilir. |
| Üretim denetimi | (Rusya) Üretim formülü/ürün reçetesi ve üretimde otomatik GTD rezervasyonu/tüketimi için varsayılan konum kurulumunu etkinleştirme | Bu özellik, ithal ham maddelerden üretim için ek seçenekler sağlar (yalnızca Rusça bölgesi):<ul><li>Hem kaynak gruplarında hem de ambarlarda üretim formülleri ve ürün reçeteleri için otomatik varsayılan konumu ayarlama seçeneği.</li><li>WMS dışı rezervasyon algoritmasına göre, WMS ile etkinleştirilen ambarlarda ham maddelerin *GTD numarası* boyutuna göre otomatik olarak ayrılması. Bu, *Ham madde çekme* için bir çalışma ilkesinin *Hiçbir Zaman* olarak ayarlanmış **İş oluşturma yöntemiyle** var olduğu ve ambar, konum ve madde numarası kurulumunun üretim (toplu iş) siparişinin stok hareketleriyle eşleştiği durumlarda geçerlidir.</li><li>Daha önce açıklandığı üzere, edinilen ayırmaya göre, malzeme çekme listesi deftere naklinde ham maddelerin *GTD numarası* boyutuna göre otomatik tüketimi.</li></ul> |
| Ambar yönetimi | Durdurulan stoktan örnek alan kalite emirlerinden gelen beklenen girişleri devre dışı bırak | Bu özellik, sistemin stoku engelleme durumuyla örnekleyen kalite siparişleri için beklenen giriş hareketlerini oluşturmasını engeller. Engellenen stok kullanılamadığından, bu özellik beklenen girişleri kaldırır. Bu, stokun, veri bütünlüğü sorunlarına neden olabilen birden çok engelleme durumuyla bitmediğinden emin olmanıza yardımcı olur. |
| Ambar yönetimi | (Önizleme) Gelen ve giden ambar emirleri için ölçek birimi desteği | Bu özellik, sistemin serbest bırakmadan ambara işleme sırasında giden ambar siparişleri oluşturmasına ve transfer emirleri sevk edildi olarak deftere nakledildiğinde gelen ambar siparişleri oluşturmasına neden olur. Sistem daha sonra her gelen veya giden ambar siparişini siparişi sevk etmekten veya teslim almaktan sorumlu ölçek birimiyle eşitler. Bu özelliği etkinleştirdikten sonra ambar yürütme iş yüklerinizin yükseltilmesi gerektiğini unutmayın. Daha fazla bilgi için bkz. [Bulut ve uç ölçek birimleri için ambar yönetimi iş yükleri](../cloud-edge/cloud-edge-workload-warehousing.md).<br><br>Bu özellik, *ASN'lerden yerine koyma çalışmasını ayırmayı* gerektirir ve Warehouse Management mobil uygulamasındaki plaka alma işlemini kullanarak transfer emirleri alma yeteneğini etkinleştirir. |

## <a name="feature-state-changes-in-this-release"></a>Bu sürümdeki özellik durumu değişiklikleri

Aşağıdaki tabloda, 10.0.25'ten itibaren zorunlu veya varsayılan olarak açık hale gelen özellikler listelenmektedir. 10.0.25'e güncelleştirme yaptığınızda, bu özelliklerin tümü sisteminiz için otomatik olarak açılır. Zorunlu özellikler kapatılamaz ancak varsayılan olarak açık olan özellikler [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)kullanılarak kapatılabilir.

Tablo ayrıca, daha önce genel önizlemede bulunan, ancak 10.0.25'te genel kullanıma sunulacak şekilde değiştirilen özellikleri de listeler, bu da özelliklerin artık üretim ortamlarında kullanım için önerildiği anlamına gelir. Aksi belirtilmedikçe bu özellikler varsayılan olarak kapalıdır, bu nedenle bunları kullanmak istiyorsanız etkinleştirmek için [Özellik yönetimini](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) kullanmanız gerekir.

| Modül | Özellik adı | Özellik durumu |
| --- | --- | --- |
| Kıymet yönetimi | Bir bakım planı çalıştırırken iş emirlerini gruplama kuralları uygula | Genel kullanılabilir |
| Kıymet yönetimi | Sayaç tabanlı bakım geliştirmeleri | Genel kullanılabilir |
| Maliyet yönetimi | Maliyet hesaplama düzeyi | Genel kullanılabilir |
| Maliyet yönetimi | Stok kapanışını tersine çevirme işlemi için kullanıcı tanımlı toplu iş numarası kurulumunu etkinleştir | Genel kullanılabilir |
| Maliyet yönetimi | Stok kapanışının ilerlemesiyle ilgili ayrıntılar | Genel kullanılabilir |
| Maliyet yönetimi | Stok standart maliyet yeniden değerlemesini varsayılan mali boyutlara ayarlama seçenekleri | Genel kullanılabilir |
| Maliyet yönetimi | Stok değeri raporu verilerini temizleme | Varsayılan olarak açık |
| Maliyet yönetimi | Stok değeri raporu depolama alanı | Varsayılan olarak açık |
| Maliyet yönetimi | Stok kapatma günlüğünü ızgarada göster | Varsayılan olarak açık |
| Mühendislik değişikliği yönetimi | Mevcut ürünlerde değişiklik yönetimini etkinleştirme | Varsayılan olarak açık |
| Mühendislik değişikliği yönetimi | Mühendislik Değişikliği Yönetimi | Varsayılan olarak açık |
| Mühendislik değişikliği yönetimi | Üretim bölümü için mühendislik bildirimleri | Varsayılan olarak açık |
| Mühendislik değişikliği yönetimi | Mühendislik Değişikliği Yönetimi'nde geliştirilmiş öznitelik devralma | Varsayılan olarak açık |
| Mühendislik değişikliği yönetimi | Formüllerdeki ve formül içeriklerindeki değişiklikleri yönet | Varsayılan olarak açık |
| Mühendislik değişikliği yönetimi | Ürün hazır olma denetimleri | Varsayılan olarak açık |
| Mühendislik değişikliği yönetimi | Mühendislik ürünleri için çeşit oluşturma | Varsayılan olarak açık |
| Stok ve ambar yönetimi | Ürün reçetesi satırlarındaki ürün reçetesi sürümüne gezinti | Zorunlu |
| Master planlama | Planlı toplu ve paketli siparişler için toplu iş olarak yürütülebilen kesinleştirme ve konsolidasyon | Genel kullanılabilir |
| Master planlama | Bakım ile kaynak planlama | Genel kullanılabilir |
| Master planlama | Master plan kurulum sihirbazı özelliklerini etkinleştirme | Zorunlu |
| Master planlama | Talep tahmini ayrıntılarıyla ilgili tahmin modeli seçimi | Zorunlu |
| Master planlama | Master planlama ilerlemesi görselleştirmesi | Zorunlu |
| Master planlama | Planlı siparişleri paralel kesinleştirme | Zorunlu |
| Master planlama | Filtreleme ile planlı sipariş kesinleştirici | Varsayılan olarak açık |
| Master planlama | Planlı siparişler için kayıtlı görünümler | Varsayılan olarak açık |
| Tedarik ve kaynak atama | Satınalma Talebi Dağıtımı Sıfırlama Düğmesini devre dışı bırak | Genel kullanılabilir |
| Tedarik ve kaynak atama | Tedarikle ilgili iş akışlarını sıfırlamayı etkinleştir | Genel kullanılabilir |
| Tedarik ve kaynak atama | Satıcı işbirliğinde kabul edilen satınalma siparişlerini toplu olarak onaylama özelliği | Zorunlu |
| Tedarik ve kaynak atama | Satınalma sözleşmesi Kapatıldı durumu | Zorunlu |
| Tedarik ve kaynak atama | Satınalma sözleşmesiyle ilişkili satınalma siparişi faturalarına satır ekle | Varsayılan olarak açık |
| Tedarik ve kaynak atama | Deftere nakil ürün girişi sayfasına Sipariş edilen miktar alanı ekle | Varsayılan olarak açık |
| Tedarik ve kaynak atama | Satıcıların, satıcı işbirliği üzerinden tedarik kategorilerine başvurmasına izin ver | Varsayılan olarak açık |
| Tedarik ve kaynak atama | Satınalma siparişlerindeki masraf başlangıç ve bitiş tutarları | Varsayılan olarak açık |
| Tedarik ve kaynak atama | Tesis ve ambarla masraf ayarı | Varsayılan olarak açık |
| Tedarik ve kaynak atama | Yıllık tarifeye göre satınalma harcı hesaplamasını etkinleştir | Varsayılan olarak açık |
| Tedarik ve kaynak atama | Satınalma sözleşmesi sorumlu taraf | Varsayılan olarak açık |
| Tedarik ve kaynak atama | Satın alma siparişleri için kayıtlı görünümler | Varsayılan olarak açık |
| Ürün bilgileri yönetimi | Varsayılan sipariş miktarlarında katı doğrulama | Zorunlu |
| Ürün bilgileri yönetimi | Zaman aşımını önlemek için ürün reçetesi raporunu ön işleme | Varsayılan olarak açık |
| Ürün bilgileri yönetimi | Madde şablonları kullanılırken varsayılan mali boyutlar ayrı ayrı kullanılır | Varsayılan olarak açık |
| Ürün bilgileri yönetimi | Madde şablonları için ürün boyutu gruplarını etkinleştir | Varsayılan olarak açık |
| Ürün bilgileri yönetimi | Ürün çeşidi adlarını terminolojiye göre yeniden oluştur | Varsayılan olarak açık |
| Ürün bilgileri yönetimi | Çeşit önerileri sayfa geliştirmeleri | Varsayılan olarak açık |
| Üretim denetimi | İyileştirilmiş üretim fiili ağırlık miktarı çekme | Genel kullanılabilir |
| Üretim denetimi | İş Kartı Terminali sayfasına yeni bir Molayı durdur düğmesi eklendi | Zorunlu |
| Üretim denetimi | İş kartı cihazında tamamlandı olarak bildirme sırasında otomatik plaka numarası oluşturmayı etkinleştirin | Zorunlu |
| Üretim denetimi | Alt sözleşmeli maddeler için kısmi girişe olanak tanıyın ve Satıcı türündeki ürün reçetesi satırları için hurda hesaplamasıyla ilgili sorunu düzeltin | Zorunlu |
| Üretim denetimi | Temizlenebilmeleri için iş kartı cihazını ve iş kartı terminalini kilitleme özelliği | Zorunlu |
| Üretim denetimi | İşleri Onayla ve Transfer et iletişim kutularındaki geliştirmeler | Zorunlu |
| Üretim denetimi | İş Kartı Cihazına eklenen tamamlandı olarak işaretleme plakası | Zorunlu |
| Üretim denetimi | İş Kartı Cihazından etiket yazdır | Zorunlu |
| Üretim denetimi | Üretim katı yürütmesi | Zorunlu |
| Üretim denetimi | Üretim katı yürütme arabirimi için varlık yönetim işlevi | Varsayılan olarak açık |
| Üretim denetimi | Üretim katı yürütme arabiriminde iş arama | Varsayılan olarak açık |
| Üretim denetimi | Varsayılan üretim rezervasyonlarını geçersiz kıl | Varsayılan olarak açık |
| Üretim denetimi | Üretim katı yürütme arabiriminde seri, toplu iş ve plaka numaralarının tamamını göster | Varsayılan olarak açık |
| Satış ve pazarlama | Satış siparişi ayrıntıları performans iyileştirmesi | Genel kullanılabilir |
| Satış ve pazarlama | Satış teklifi ayrıntıları performans iyileştirmesi | Genel kullanılabilir |
| Satış ve pazarlama | Satış siparişinin başvurulan veri dışarı aktarma ilkesi | Zorunlu |
| Satış ve pazarlama | Satınalma siparişi satırını silme ilkesine yönelik satış siparişi | Zorunlu |
| Satış ve pazarlama | Satış teklifinin başvurulan veri dışarı aktarma ilkesi | Zorunlu |
| Satış ve pazarlama | İlgili kişi veri varlığını dışa aktarma optimizasyonu | Varsayılan olarak açık |
| Satış ve pazarlama | Satış teklifi belgesi girişi ve belge sonuç alanlarında aramayı etkinleştir | Varsayılan olarak açık |
| Satış ve pazarlama | "İlk 100" müşteri raporunun performansını iyileştir | Varsayılan olarak açık |
| Satış ve pazarlama | Tahmini müşteri bakiyelerini yeniden hesapla | Varsayılan olarak açık |
| Satış ve pazarlama | Fiili ağırlıklı ve fiili ağırlıksız ondalık hassasiyetli satış iade siparişi satırı kaydı | Varsayılan olarak açık |
| Satış ve pazarlama | Satış ve Pazarlama için Kayıtlı Görünümler | Varsayılan olarak açık |
| Satış ve pazarlama | Tek tıklamayla satış siparişi onayı | Varsayılan olarak açık |
| Ambar yönetimi | Yerleşim yönergeleri olan çapraz sevk şablonları | Genel kullanılabilir |
| Ambar yönetimi | Durdurulan stoktan örnek alan kalite emirlerinden gelen beklenen girişleri devre dışı bırak | Genel kullanılabilir |
| Ambar yönetimi | Plaka alımı geçmişi | Genel kullanılabilir |
| Ambar yönetimi | Ambara serbest bırakırken miktarları en yakın satış birimine indirgenecek şekilde yuvarla | Genel kullanılabilir |
| Ambar yönetimi | Ambar uygulaması işi listeleri için ölçek birimi desteği | Genel kullanılabilir |
| Ambar yönetimi | Sevkiyat dalgası etiket ayrıntıları | Genel kullanılabilir |
| Ambar yönetimi | Sevk istasyonunda konteyner kapatma/yeniden açma için daha hızlı API kullanın | Genel kullanılabilir |
| Ambar yönetimi | Stok yenileme işleri için seçilen şablonları doğrula | Genel kullanılabilir |
| Ambar yönetimi | Stok yenileme şablonunun mevcut anlık stok yenileme işini kullanmasına izin ver (birimler arasında) | Zorunlu |
| Ambar yönetimi | WHS kullanıcısı oluşturma işlemi sırasında GUID'leri otomatik olarak atama | Zorunlu |
| Ambar yönetimi | Yük maddesi teslim alma sırasında ambar uygulamasında ürün çeşitlerini ve izleme boyutlarını yakala | Zorunlu |
| Ambar yönetimi | İzleme boyutları tarafından denetlenen maddelerin stok durumunu değiştir | Zorunlu |
| Ambar yönetimi | İşteki iş havuzunu değiştirme | Zorunlu |
| Ambar yönetimi | Küme konumu dolu | Zorunlu |
| Ambar yönetimi | Küme Yerine Koyma Özelliği | Zorunlu |
| Ambar yönetimi | Onayla ve aktar | Zorunlu |
| Ambar yönetimi | Toplu işlerden giden sevkiyatları onayla | Zorunlu |
| Ambar yönetimi | Mobil cihazlarda bir alma özet sayfasının görüntülenip görüntülenmeyeceğini denetle | Zorunlu |
| Ambar yönetimi | El ile stok hareketi işlemini ertelenmiş olarak işleme | Zorunlu |
| Ambar yönetimi | Dalga yükü oluşturma şablonu gereksinimlerini karşılamayan yük oluşturmaya izin verme | Zorunlu |
| Ambar yönetimi | Gelişmiş plaka etiketi düzenleri | Zorunlu |
| Ambar yönetimi | Çoklu SKU konumu yönergeleri için tüm eylemleri değerlendir | Zorunlu |
| Ambar yönetimi | "Tüm Yükler" ve "Yük Ayrıntıları" sayfalarındaki Toplam Değer alanını gizle | Zorunlu |
| Ambar yönetimi | Plaka etiketi yapı yapılandırması | Zorunlu |
| Ambar yönetimi | Yönetici veya benzer güvenilen kullanıcılar için yük satırını el ile düzeltme | Zorunlu |
| Ambar yönetimi | Yerleşim plakası konumlandırması | Zorunlu |
| Ambar yönetimi | Yerleşim ürün boyutu karıştırması | Zorunlu |
| Ambar yönetimi | Mobil cihaz stok hareketi stok durumu alanını düzenlenebilir yap | Zorunlu |
| Ambar yönetimi | Yönetici veya benzer güvenilen kullanıcılar için el ile satış satırı çekme hizmeti | Zorunlu |
| Ambar yönetimi | Transfer emri sevk edilen plakalarının hedef ambarlardan farklı ambarlarda kullanılmasını engelle | Zorunlu |
| Ambar yönetimi | Belirsiz "Konun / Plaka" adlarını çözmek için uyar | Zorunlu |
| Ambar yönetimi | Kalite denetimi | Zorunlu |
| Ambar yönetimi | Yeni ambar uygulaması için kullanıcı ayarları, simgeler ve adım başlıkları | Zorunlu |
| Ambar yönetimi | Ek yerleşim bölgesi | Varsayılan olarak açık |
| Ambar yönetimi | Transfer emirlerini ambar uygulamasından oluştur ve işle | Varsayılan olarak açık |
| Ambar yönetimi | Ambar mobil cihazları için hızlı doğrulamayı etkinleştir | Varsayılan olarak açık |
| Ambar yönetimi | Madde konsolidasyon yerleşimi kullanımı | Varsayılan olarak açık |
| Ambar yönetimi | Ambar yönetimi eldeki girişlerini temizleme işi için maksimum yürütme süresi | Varsayılan olarak açık |
| Ambar yönetimi | Giden iş yükü görselleştirmesi | Varsayılan olarak açık |
| Ambar yönetimi | Ambar uygulaması olaylarını işle | Varsayılan olarak açık |
| Ambar yönetimi | Yük planlama çalışma ekranı için kayıtlı görünüm | Varsayılan olarak açık |
| Ambar yönetimi | İş ayrıntıları sayfası için kayıtlı görünüm | Varsayılan olarak açık |
| Ambar yönetimi | Dalga işleme için kayıtlı görünüm | Varsayılan olarak açık |
| Ambar yönetimi | Yük işleme için kayıtlı görünümler | Varsayılan olarak açık |
| Ambar yönetimi | Sevkiyat işleme için kayıtlı görünümler | Varsayılan olarak açık |
| Ambar yönetimi | Dalga toplu iş ayrıntıları | Varsayılan olarak açık |
| Ambar yönetimi | Dalga yürütme bildirimleri | Varsayılan olarak açık |

## <a name="additional-resources"></a>Ek kaynaklar

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finance ve Operations uygulamaları için Platform güncelleştirmeleri

Microsoft Dynamics 365 Supply Chain Management 10.0.25 platform güncelleştirmeleri içerir. Daha fazla bilgi için bkz. [Finance ve Operations uygulamalarının 10.0.25 sürümü için platform güncelleştirmeleri (Nisan 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-25.md).

### <a name="bug-fixes"></a>Hata düzeltmeleri

10.0.25'nın parçası olan güncelleştirmelerin her birine dahil edilen hata düzeltmeleri hakkında bilgi için, Lifecycle Services'ta (LCS) oturum açın ve [BB makalesini](https://fix.lcs.dynamics.com/Issue/Details?bugId=654580&dbType=3&qc=3799fa965b008dd980d27cf740e4582e6384ec6601ae8a35b7eaec6f1287a868) görüntüleyin.

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 ve sektör bulutları: 2022 sürüm dalgası 1 planı

İş uygulamalarımız veya platformumuz için gelecek olan ve en son yayımlanan özellikleri merak ediyor musunuz?

[Dynamics 365 ve sektör bulutları: 2022 sürüm dalgası 1 planına](/dynamics365-release-plan/2022wave1/) göz atın. Baştan sona tüm ayrıntıları, planlama için kullanabileceğiniz tek bir belgede bir araya getirdik.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Kaldırılan ve kullanım dışı bırakılan Supply Chain Management özellikleri

[Dynamics 365 Supply Chain Management'taki kaldırılmış veya kullanım dışı bırakılmış özellikler](removed-deprecated-features-scm-updates.md) konusu Supply Chain Management için kaldırılan veya kullanım dışı bırakılan veya kaldırılması ya da kullanım dışı bırakılması planlanan özellikleri açıklar.

- *Kaldırılan* özellik artık üründe bulunmaz.
- *Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Herhangi bir özellik üründen kaldırılmadan önce, kullanım dışı bırakma bildirimi kaldırma işleminden 12 ay önce [Dynamics 365 Supply Chain Management'taki kaldırılan veya kullanım dışı bırakılan özelliker](removed-deprecated-features-scm-updates.md) konusunda duyurulacaktır.

Yalnızca derleme zamanını etkileyen ancak korumalı alan ve üretim ortamlarıyla ikili uyumlu olan son dakika değişiklikleri için kullanım dışı bırakma süresi 12 aydan kısa olacaktır. Genellikle, bunlar derleyiciye yapılması gereken işlevsel güncelleştirmelerdir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
