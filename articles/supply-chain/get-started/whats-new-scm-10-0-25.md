---
title: Dynamics 365 Supply Chain Management 10.0.25'taki yenilikler veya değişiklikler (Nisan 2022)
description: Bu makalede, Microsoft Dynamics 365 Supply Chain Management 10.0.25'taki yeni veya değişen özellikler açıklanmaktadır.
author: kamaybac
ms.date: 03/14/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 89036920cc8738e2948ec1a78aafc4b35fff87fa
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219109"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10025-april-2022"></a>Dynamics 365 Supply Chain Management 10.0.25'taki yenilikler veya değişiklikler (Nisan 2022)

[!include [banner](../includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Supply Chain Management 10.0.25 sürümündeki yeni veya değişen özellikler listelenmektedir. Bu sürüm, 10.0.1149 derleme numarasına sahiptir ve aşağıdaki gibi kullanıma sunulmuştur:

- **Sürüm önizlemesi:** Şubat 2022
- **Sürüm genel kullanılabilirliği (kendi kendine güncelleştirme):** Mart 2022
- **Sürüm genel kullanılabilirliği (otomatik güncelleştirme):** Nisan 2022

## <a name="features-included-in-this-release"></a>Bu sürümdeki özellikler

Aşağıdaki tabloda, bu sürüme dahil edilen özellikler listelenmektedir. Bu makale ilk kez yayımlandıktan sonra derlemeye eklenen özellikleri dahil etmek için bu konuya güncelleştirmeler uygulayabiliriz.

| Özellik alanı | Özellik | Daha fazla bilgi | Etkinleştiren |
|---|---|---|---|
| Stok&nbsp;ve&nbsp;lojistik | [Tehlikeli maddeler geliştirmeleri](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/hazardous-materials-enhancements) | Çok yakında | Özellik yönetimi:<br>*Tehlikeli maddeler geliştirmeleri* |
| Stok&nbsp;ve&nbsp;lojistik | [Sevk istasyonları için sevk işi](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/packing-work-packing-stations) | [Giden konteynerleri paketlemeye ve sevkiyatları işlemeye yönelik paketleme işi](../warehousing/packing-work.md) | Özellik yönetimi:<br>*Sevk istasyonları için sevk işi* |
| Stok&nbsp;ve&nbsp;lojistik | [GS1 biçimi standartlarını kullanarak ambarda barkodları tarama](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) | [GS1 barkodları ve QR kodları](../warehousing/gs1-barcodes.md) | Özellik yönetimi:<br>*GS1 barkodlarını tara* |
| İmalat | [Üretim katı yürütme arabiriminde malzeme tüketimi ve ayırmalar](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/material-consumption-reservations-production-floor-execution-interface) | [Çalışanlar üretim katı yürütme arabirimini nasıl kullanır?](../production-control/production-floor-execution-use.md) | Özellik yönetimi:<br>*Üretim katı yürütme arabiriminde malzeme tüketimini kaydetme (WMS dışı)*<br><br>Ve/veya:<br><br>Özellik yönetimi:<br>*(Önizleme) Üretim katı yürütme arabiriminde (WMS özellikli) malzeme tüketimini kaydet* |
| Planlama | [Planlama Optimizasyonu Merkezi takvim Bakımı](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-centralized-calendar-maintenance) | [Takvimler ve master planlama](../master-planning/supply-chain-calendars-master-planning.md) | Varsayılan olarak etkin |
| Planlama | [Mevcut arzı iyileştirmek için Planlama İyileştirmesi önerileri](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-suggestions-optimize-existing-supply) | [Eylem iletileri](../master-planning/action-messages.md) | Varsayılan olarak etkin |
| Planlama | Basitleştirilmiş planlı siparişler | [Basitleştirilmiş planlı siparişler](../master-planning/planning-optimization/planned-orders-simplified.md ) | Özellik yönetimi:<br>*Basitleştirilmiş planlı siparişler* |

## <a name="feature-enhancements-included-in-this-release"></a>Bu sürümdeki özellik iyileştirmeleri

Aşağıdaki tabloda, bu sürümde dahil edilen özellik iyileştirmeleri listelenmektedir. Bu iyileştirmelerden her biri, mevcut bir özellik için artımlı bir geliştirme sağlar. Bunlar yalnızca iyileştirme olduğundan [sürüm planında](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features) listelenmez. Ancak, bu geliştirmelerin mevcut özelleştirmelerinizle veya tercihlerinizle çakışmayacağından emin olmak için, her biri varsayılan olarak kapatılmıştır (aksi belirtilmedikçe).

Bu özelliklerden herhangi birini açmak veya kapatmak istiyorsanız bunu [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) yapmalısınız.

| Modül | Özellik yönetiminde özellik adı | Daha fazla bilgi |
|---|---|---|
| Stok ve ambar yönetimi | (Polonya) Çeşitli SAD faturalarını bir SAD içinde bir Satınalma sipariş satırına bağlamaya izin ver | Bu özellik, birkaç farklı fatura için (farklı sevk irsaliyeleri gibi) satınalma siparişi satırları deftere nakledildiğinde satınalma siparişi satırlarını bölmenize ve bunları tek bir yönetim belgesine (SAD) bağlamanıza olanak tanır. |
| Tedarik ve kaynak atama | Muhasebe tarihine göre birden fazla satınalma taleplerini tek bir satınalma siparişi içinde konsolide et | Bu özellik, farklı satınalma taleplerinin farklı muhasebe tarihleri varsa birden çok satınalma siparişinin tek bir satınalma siparişinde birleştirilmesine olanak tanır. Satınalma siparişi oluşturma ve talep konsolidasyon satınalma ilkesi kuralları, talep satırlarının satınalma siparişi düzeyindeki muhasebe tarihine göre gruplandırılmasına ilişkin kararı otomatikleştirmek için ayarlanabilir. Hesap tarihi bütçe ayırmaları ve taahhütleri için kullanıldığından, bütçe denetimi etkinleştirildiğinde muhasebe tarihine göre satınalma siparişi konsolidasyonu desteklenmez. Bu nedenle, satınalma talebinden satınalma siparişime geçiş sırasında tutulmalıdır. |
| Tedarik ve kaynak atama | Eski varsayılan RFQ yanıt alanı ayarlarını görüntüle | Bu özellik, daha önce kullanıcı arabiriminden kaldırılan eski varsayılan teklif talebi (RFQ) yanıt alanı ayarlarını yeniden sunar. Bu ayarlar kullanıma hazır herhangi bir işlevsellik sağlamaz ancak gerektiği gibi sağlamak için özelleştirilebilir. Kuruluşunuz varsayılan RFQ yanıt alanı ayarları için işlevsellik eklediyse veya eklemeyi planlıyorsa bu özelliği etkinleştirin. Bu özellik etkinleştirildiğinde, **Tedarik ve kaynak parametreleri** sayfasına giderek, **Teklif talebi** sekmesini açarak ve **Teklif için varsayılan istek yanıt alanları** nı seçerek ayarlara erişebilirsiniz. |
| Tedarik ve kaynak atama | Satınalma siparişinde etkin boyut bağlantısı mali boyutuyla satıcıdan alınan mali boyutları birleştir | Bu özellik, bir mali boyut ile site stok boyutu arasında bir bağlantı ayarlarsanız, satınalma talep onayından sonra satıcılardan gelen mali boyutları etkin boyut bağlantısı mali boyutlarıyla birleştirmenizi sağlar. Satınalma siparişi oluşturma ve talep konsolidasyon satınalma ilkesi kuralları, satınalma siparişi başlığı düzeyinde etkin boyut bağlantısı mali boyutu olan satıcılardan mali boyutları birleştirme kararını yönlendirmek için ayarlanabilir. |
| Üretim denetimi | (Rusya) Üretim formülü/ürün reçetesi ve üretimde otomatik GTD rezervasyonu/tüketimi için varsayılan konum kurulumunu etkinleştirme | Bu özellik, ithal ham maddelerden üretim için ek seçenekler sağlar (yalnızca Rusça bölgesi):<ul><li>Hem kaynak gruplarında hem de ambarlarda üretim formülleri ve ürün reçeteleri için otomatik varsayılan konumu ayarlama seçeneği.</li><li>WMS dışı rezervasyon algoritmasına göre, WMS ile etkinleştirilen ambarlarda ham maddelerin *GTD numarası* boyutuna göre otomatik olarak ayrılması. Bu, *Ham madde çekme* için bir çalışma ilkesinin *Hiçbir Zaman* olarak ayarlanmış **İş oluşturma yöntemiyle** var olduğu ve ambar, konum ve madde numarası kurulumunun üretim (toplu iş) siparişinin stok hareketleriyle eşleştiği durumlarda geçerlidir.</li><li>Daha önce açıklandığı üzere, edinilen ayırmaya göre, malzeme çekme listesi deftere naklinde ham maddelerin *GTD numarası* boyutuna göre otomatik tüketimi.</li></ul> |
| Ambar yönetimi | (Önizleme) Gelen ve giden ambar emirleri için ölçek birimi desteği | Bu özellik, sistemin serbest bırakmadan ambara işleme sırasında giden ambar siparişleri oluşturmasına ve transfer emirleri sevk edildi olarak deftere nakledildiğinde gelen ambar siparişleri oluşturmasına neden olur. Sistem daha sonra her gelen veya giden ambar siparişini siparişi sevk etmekten veya teslim almaktan sorumlu ölçek birimiyle eşitler. Bu özelliği etkinleştirdikten sonra ambar yürütme iş yüklerinizin yükseltilmesi gerektiğini unutmayın. Daha fazla bilgi için bkz. [Bulut ve uç ölçek birimleri için ambar yönetimi iş yükleri](../cloud-edge/cloud-edge-workload-warehousing.md).<br><br>Bu özellik, *ASN'lerden yerine koyma çalışmasını ayırmayı* gerektirir ve Warehouse Management mobil uygulamasındaki plaka alma işlemini kullanarak transfer emirleri alma yeteneğini etkinleştirir. |

## <a name="feature-state-changes-in-this-release"></a>Bu sürümdeki özellik durumu değişiklikleri

Aşağıdaki tabloda, 10.0.25'ten itibaren zorunlu veya varsayılan olarak açık hale gelen özellikler listelenmektedir. 10.0.25'e güncelleştirme yaptığınızda, bu özelliklerin tümü sisteminiz için otomatik olarak açılır. Zorunlu özellikler kapatılamaz ancak varsayılan olarak açık olan özellikler [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)kullanılarak kapatılabilir.

Tablo ayrıca, daha önce genel önizlemede bulunan, ancak 10.0.25'te genel kullanıma sunulacak şekilde değiştirilen özellikleri de listeler, bu da özelliklerin artık üretim ortamlarında kullanım için önerildiği anlamına gelir. Aksi belirtilmedikçe bu özellikler varsayılan olarak kapalıdır, bu nedenle bunları kullanmak istiyorsanız etkinleştirmek için [Özellik yönetimini](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) kullanmanız gerekir.

| Modül | Özellik adı | Özellik durumu |
| --- | --- | --- |
| Kıymet yönetimi | [Bir bakım planı çalıştırırken iş emirlerini gruplama kuralları uygula](../asset-management/preventive-and-reactive-maintenance/creating-work-orders.md) | Genel kullanılabilir |
| Kıymet yönetimi | [Sayaç tabanlı bakım geliştirmeleri](../asset-management/preventive-and-reactive-maintenance/maintenance-plans.md) | Genel kullanılabilir |
| Maliyet yönetimi | [Maliyet hesaplama düzeyi](../cost-management/cost-calculation-level.md) | Genel kullanılabilir |
| Maliyet yönetimi | Stok kapanışını tersine çevirme işlemi için kullanıcı tanımlı toplu iş numarası kurulumunu etkinleştir | Genel kullanılabilir |
| Maliyet yönetimi | [Stok kapanışının ilerlemesiyle ilgili ayrıntılar](whats-new-scm-10-0-21.md) | Genel kullanılabilir |
| Maliyet yönetimi | [Stok standart maliyet yeniden değerlemesini varsayılan mali boyutlara ayarlama seçenekleri](../cost-management/manage-standard-cost-updates.md) | Genel kullanılabilir |
| Maliyet yönetimi | Stok değeri raporu verilerini temizleme | Varsayılan olarak açık |
| Maliyet yönetimi | [Stok değeri raporu depolama alanı](../cost-management/inventory-value-report-storage.md) | Varsayılan olarak açık |
| Maliyet yönetimi | Stok kapatma günlüğünü ızgarada göster | Varsayılan olarak açık |
| Mühendislik değişikliği yönetimi | [Mevcut ürünlerde değişiklik yönetimini etkinleştirme](../engineering-change-management/change-management-existing-products.md) | Varsayılan olarak açık |
| Mühendislik değişikliği yönetimi | [Mühendislik Değişikliği Yönetimi](../engineering-change-management/product-engineering-overview.md) | Varsayılan olarak açık |
| Mühendislik değişikliği yönetimi | [Üretim bölümü için mühendislik bildirimleri](../engineering-change-management/engineering-change-management.md) | Varsayılan olarak açık |
| Mühendislik değişikliği yönetimi | [Mühendislik Değişikliği Yönetimi'nde geliştirilmiş öznitelik devralma](../engineering-change-management/engineering-attributes-and-search.md) | Varsayılan olarak açık |
| Mühendislik değişikliği yönetimi | [Formüllerdeki ve formül içeriklerindeki değişiklikleri yönet](../engineering-change-management/manage-formula-changes.md) | Varsayılan olarak açık |
| Mühendislik değişikliği yönetimi | [Ürün hazır olma denetimleri](../engineering-change-management/product-readiness.md) | Varsayılan olarak açık |
| Mühendislik değişikliği yönetimi | [Mühendislik ürünleri için çeşit oluşturma](../engineering-change-management/engineering-variants.md) | Varsayılan olarak açık |
| Stok ve ambar yönetimi | Ürün reçetesi satırlarındaki ürün reçetesi sürümüne gezinti | Zorunlu |
| Master planlama | [Planlı toplu ve paketli siparişler için toplu iş olarak yürütülebilen kesinleştirme ve konsolidasyon](whats-new-scm-10-0-20.md) | Genel kullanılabilir |
| Master planlama | Bakım ile kaynak planlama | Genel kullanılabilir |
| Master planlama | Master plan kurulum sihirbazı özelliklerini etkinleştirme | Zorunlu |
| Master planlama | [Talep tahmini ayrıntılarıyla ilgili tahmin modeli seçimi](../master-planning/manual-adjustments-baseline-forecast.md) | Zorunlu |
| Master planlama | [Master planlama ilerlemesi görselleştirmesi](../master-planning/tasks/monitor-master-planning-run.md) | Zorunlu |
| Master planlama | [Planlı siparişleri paralel kesinleştirme](../master-planning/planning-optimization/planned-order-firming.md) | Zorunlu |
| Master planlama | [Filtreleme ile planlı sipariş kesinleştirici](../master-planning/planning-optimization/planned-order-firming.md) | Varsayılan olarak açık |
| Master planlama | [Planlı siparişler için kayıtlı görünümler](saved-views-scm.md) | Varsayılan olarak açık |
| Tedarik ve kaynak atama | Satınalma Talebi Dağıtımı Sıfırlama Düğmesini devre dışı bırak | Genel kullanılabilir |
| Tedarik ve kaynak atama | [Tedarikle ilgili iş akışlarını sıfırlamayı etkinleştir](whats-new-scm-10-0-20.md) | Genel kullanılabilir |
| Tedarik ve kaynak atama | Satıcı işbirliğinde kabul edilen satınalma siparişlerini toplu olarak onaylama özelliği | Zorunlu |
| Tedarik ve kaynak atama | Satınalma sözleşmesi Kapatıldı durumu | Zorunlu |
| Tedarik ve kaynak atama | Satınalma sözleşmesiyle ilişkili satınalma siparişi faturalarına satır ekle | Varsayılan olarak açık |
| Tedarik ve kaynak atama | Deftere nakil ürün girişi sayfasına Sipariş edilen miktar alanı ekle | Varsayılan olarak açık |
| Tedarik ve kaynak atama | [Satıcıların, satıcı işbirliği üzerinden tedarik kategorilerine başvurmasına izin ver](../procurement/category-requests-from-vendors.md) | Varsayılan olarak açık |
| Tedarik ve kaynak atama | Satınalma siparişlerindeki masraf başlangıç ve bitiş tutarları | Varsayılan olarak açık |
| Tedarik ve kaynak atama | Tesis ve ambarla masraf ayarı | Varsayılan olarak açık |
| Tedarik ve kaynak atama | Yıllık tarifeye göre satınalma harcı hesaplamasını etkinleştir | Varsayılan olarak açık |
| Tedarik ve kaynak atama | [Satınalma sözleşmesi sorumlu taraf](../procurement/purchase-agreements.md) | Varsayılan olarak açık |
| Tedarik ve kaynak atama | [Satın alma siparişleri için kayıtlı görünümler](saved-views-scm.md) | Varsayılan olarak açık |
| Ürün bilgileri yönetimi | [Varsayılan sipariş miktarlarında katı doğrulama](../production-control/default-order-settings.md) | Zorunlu |
| Ürün bilgileri yönetimi | Zaman aşımını önlemek için ürün reçetesi raporunu ön işleme | Varsayılan olarak açık |
| Ürün bilgileri yönetimi | Madde şablonları kullanılırken varsayılan mali boyutlar ayrı ayrı kullanılır | Varsayılan olarak açık |
| Ürün bilgileri yönetimi | Madde şablonları için ürün boyutu gruplarını etkinleştir | Varsayılan olarak açık |
| Ürün bilgileri yönetimi | Ürün çeşidi adlarını terminolojiye göre yeniden oluştur | Varsayılan olarak açık |
| Ürün bilgileri yönetimi | [Çeşit önerileri sayfa geliştirmeleri](../pim/tasks/create-predefined-product-variants.md) | Varsayılan olarak açık |
| Üretim denetimi | İyileştirilmiş üretim fiili ağırlık miktarı çekme | Genel kullanılabilir |
| Üretim denetimi | İş Kartı Terminali sayfasına yeni bir Molayı durdur düğmesi eklendi | Zorunlu |
| Üretim denetimi | [İş kartı cihazında tamamlandı olarak bildirme sırasında otomatik plaka numarası oluşturmayı etkinleştirin](../production-control/production-floor-execution-configure.md) | Zorunlu |
| Üretim denetimi | Alt sözleşmeli maddeler için kısmi girişe olanak tanıyın ve Satıcı türündeki ürün reçetesi satırları için hurda hesaplamasıyla ilgili sorunu düzeltin | Zorunlu |
| Üretim denetimi | [Temizlenebilmeleri için iş kartı cihazını ve iş kartı terminalini kilitleme özelliği](../production-control/production-floor-execution-configure.md) | Zorunlu |
| Üretim denetimi | İşleri Onayla ve Transfer et iletişim kutularındaki geliştirmeler | Zorunlu |
| Üretim denetimi | [İş Kartı Cihazına eklenen tamamlandı olarak işaretleme plakası](../production-control/production-floor-execution-configure.md) | Zorunlu |
| Üretim denetimi | [İş Kartı Cihazından etiket yazdır](../production-control/production-floor-execution-configure.md) | Zorunlu |
| Üretim denetimi | [Üretim katı yürütmesi](../production-control/production-floor-execution-configure.md) | Zorunlu |
| Üretim denetimi | [Üretim katı yürütme arabirimi için varlık yönetim işlevi](../production-control/production-floor-execution-configure.md) | Varsayılan olarak açık |
| Üretim denetimi | [Üretim katı yürütme arabiriminde iş arama](../production-control/production-floor-execution-configure.md) | Varsayılan olarak açık |
| Üretim denetimi | [Varsayılan üretim rezervasyonlarını geçersiz kıl](../production-control/override-default-reservation-principle.md) | Varsayılan olarak açık |
| Üretim denetimi | [Üretim katı yürütme arabiriminde seri, toplu iş ve plaka numaralarının tamamını göster](whats-new-scm-10-0-21.md) | Varsayılan olarak açık |
| Satış ve pazarlama | [Satış siparişi ayrıntıları performans iyileştirmesi](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-details-performance-enhancement) | Genel kullanılabilir |
| Satış ve pazarlama | Satış teklifi ayrıntıları performans iyileştirmesi | Genel kullanılabilir |
| Satış ve pazarlama | Satış siparişinin başvurulan veri dışarı aktarma ilkesi | Zorunlu |
| Satış ve pazarlama | [Satınalma siparişi satırını silme ilkesine yönelik satış siparişi](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-purchase-order-line-deletion-policy) | Zorunlu |
| Satış ve pazarlama | [Satış teklifinin başvurulan veri dışarı aktarma ilkesi](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/sales-quotation-referenced-data-export-policy)| Zorunlu |
| Satış ve pazarlama | [İlgili kişi veri varlığını dışa aktarma optimizasyonu](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization) | Varsayılan olarak açık |
| Satış ve pazarlama | Satış teklifi belgesi girişi ve belge sonuç alanlarında aramayı etkinleştir | Varsayılan olarak açık |
| Satış ve pazarlama | ["İlk 100" müşteri raporunun performansını iyileştir](whats-new-scm-10-0-23.md) | Varsayılan olarak açık |
| Satış ve pazarlama | Tahmini müşteri bakiyelerini yeniden hesapla | Varsayılan olarak açık |
| Satış ve pazarlama | [Fiili ağırlıklı ve fiili ağırlıksız ondalık hassasiyetli satış iade siparişi satırı kaydı](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-return-order-line-registration-decimal-precision-without-catch-weight) | Varsayılan olarak açık |
| Satış ve pazarlama | [Satış ve Pazarlama için Kayıtlı Görünümler](saved-views-scm.md) | Varsayılan olarak açık |
| Satış ve pazarlama | Tek tıklamayla satış siparişi onayı | Varsayılan olarak açık |
| Ambar yönetimi | [Yerleşim yönergeleri olan çapraz sevk şablonları](../warehousing/planned-cross-docking.md) | Genel kullanılabilir |
| Ambar yönetimi | [Durdurulan stoktan örnek alan kalite emirlerinden gelen beklenen girişleri devre dışı bırak](../inventory/inventory-blocking.md) | Genel kullanılabilir |
| Ambar yönetimi | Plaka alımı geçmişi | Genel kullanılabilir |
| Ambar yönetimi | [Malzeme işleme ekipmanı arabirimi](../warehousing/mhax.md) | Genel kullanılabilir |
| Ambar yönetimi | [Ambara serbest bırakırken miktarları en yakın satış birimine indirgenecek şekilde yuvarla](whats-new-scm-10-0-19.md) | Genel kullanılabilir |
| Ambar yönetimi | Ambar uygulaması işi listeleri için ölçek birimi desteği | Genel kullanılabilir |
| Ambar yönetimi | Sevkiyat dalgası etiket ayrıntıları | Genel kullanılabilir |
| Ambar yönetimi | [Sevk istasyonunda konteyner kapatma/yeniden açma için daha hızlı API kullanın](whats-new-scm-10-0-21.md) | Genel kullanılabilir |
| Ambar yönetimi | [Stok yenileme işleri için seçilen şablonları doğrula](whats-new-scm-10-0-20.md) | Genel kullanılabilir |
| Ambar yönetimi | Stok yenileme şablonunun mevcut anlık stok yenileme işini kullanmasına izin ver (birimler arasında) | Zorunlu |
| Ambar yönetimi | WHS kullanıcısı oluşturma işlemi sırasında GUID'leri otomatik olarak atama | Zorunlu |
| Ambar yönetimi | Yük maddesi teslim alma sırasında ambar uygulamasında ürün çeşitlerini ve izleme boyutlarını yakala | Zorunlu |
| Ambar yönetimi | [İzleme boyutları tarafından denetlenen maddelerin stok durumunu değiştir](../inventory/inventory-statuses.md) | Zorunlu |
| Ambar yönetimi | [İşteki iş havuzunu değiştirme](../warehousing/change-work-pool-on-work.md) | Zorunlu |
| Ambar yönetimi | [Küme konumu dolu](../warehousing/cluster-position-full.md) | Zorunlu |
| Ambar yönetimi | [Küme Yerine Koyma Özelliği](../warehousing/putaway-clusters.md) | Zorunlu |
| Ambar yönetimi | [Onayla ve aktar](../warehousing/confirm-and-transfer.md) | Zorunlu |
| Ambar yönetimi | [Toplu işlerden giden sevkiyatları onayla](../warehousing/confirm-outbound-shipments-from-batch-jobs.md) | Zorunlu |
| Ambar yönetimi | [Mobil cihazlarda bir alma özet sayfasının görüntülenip görüntülenmeyeceğini denetle](../warehousing/warehousing-mobile-device-app-license-plate-receiving.md) | Zorunlu |
| Ambar yönetimi | [El ile stok hareketi işlemini ertelenmiş olarak işleme](../warehousing/deferred-processing-manual-inventory-movement.md) | Zorunlu |
| Ambar yönetimi | Dalga yükü oluşturma şablonu gereksinimlerini karşılamayan yük oluşturmaya izin verme | Zorunlu |
| Ambar yönetimi | [Gelişmiş plaka etiketi düzenleri](../warehousing/document-routing-layout-for-license-plates.md) | Zorunlu |
| Ambar yönetimi | [Çoklu SKU konumu yönergeleri için tüm eylemleri değerlendir](/troubleshoot/dynamics-365/supply-chain/warehousing/evaluate-multiple-location-directive-actions) | Zorunlu |
| Ambar yönetimi | "Tüm Yükler" ve "Yük Ayrıntıları" sayfalarındaki Toplam Değer alanını gizle | Zorunlu |
| Ambar yönetimi | Plaka etiketi yapı yapılandırması | Zorunlu |
| Ambar yönetimi | Yönetici veya benzer güvenilen kullanıcılar için yük satırını el ile düzeltme | Zorunlu |
| Ambar yönetimi | [Yerleşim plakası konumlandırması](../warehousing/location-license-plate-positioning.md) | Zorunlu |
| Ambar yönetimi | [Yerleşim ürün boyutu karıştırması](../warehousing/location-product-dimension-mixing.md) | Zorunlu |
| Ambar yönetimi | Mobil cihaz stok hareketi stok durumu alanını düzenlenebilir yap | Zorunlu |
| Ambar yönetimi | Yönetici veya benzer güvenilen kullanıcılar için el ile satış satırı çekme hizmeti | Zorunlu |
| Ambar yönetimi | [Transfer emri sevk edilen plakalarının hedef ambarlardan farklı ambarlarda kullanılmasını engelle](../warehousing/warehousing-mobile-device-app-license-plate-receiving.md) | Zorunlu |
| Ambar yönetimi | Belirsiz "Konun / Plaka" adlarını çözmek için uyar | Zorunlu |
| Ambar yönetimi | [Kalite denetimi](../warehousing/quality-check.md) | Zorunlu |
| Ambar yönetimi | [Yeni ambar uygulaması için kullanıcı ayarları, simgeler ve adım başlıkları](../warehousing/install-configure-warehouse-management-app.md) | Zorunlu |
| Ambar yönetimi | [Ek yerleşim bölgesi](../warehousing/additional-location-zones.md) | Varsayılan olarak açık |
| Ambar yönetimi | [Transfer emirlerini ambar uygulamasından oluştur ve işle](../warehousing/create-transfer-order-from-warehouse-app.md) | Varsayılan olarak açık |
| Ambar yönetimi | Ambar mobil cihazları için hızlı doğrulamayı etkinleştir | Varsayılan olarak açık |
| Ambar yönetimi | [Ambar yönetimi eldeki girişlerini temizleme işi için maksimum yürütme süresi](../warehousing/onhand-cleanup.md) | Varsayılan olarak açık |
| Ambar yönetimi | [Giden iş yükü görselleştirmesi](../warehousing/outbound-workload-visualization.md) | Varsayılan olarak açık |
| Ambar yönetimi | [Ambar uygulaması olaylarını işle](../warehousing/warehouse-app-events.md) | Varsayılan olarak açık |
| Ambar yönetimi | [Yük planlama çalışma ekranı için kayıtlı görünüm](saved-views-scm.md) | Varsayılan olarak açık |
| Ambar yönetimi | [İş ayrıntıları sayfası için kayıtlı görünüm](saved-views-scm.md) | Varsayılan olarak açık |
| Ambar yönetimi | [Dalga işleme için kayıtlı görünüm](saved-views-scm.md) | Varsayılan olarak açık |
| Ambar yönetimi | [Yük işleme için kayıtlı görünümler](saved-views-scm.md) | Varsayılan olarak açık |
| Ambar yönetimi | [Sevkiyat işleme için kayıtlı görünümler](saved-views-scm.md) | Varsayılan olarak açık |
| Ambar yönetimi | [Dalga toplu iş ayrıntıları](../warehousing/wave-processing.md) | Varsayılan olarak açık |
| Ambar yönetimi | [Dalga yürütme bildirimleri](../warehousing/wave-execution-notifications.md) | Varsayılan olarak açık |

## <a name="additional-resources"></a>Ek kaynaklar

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finans ve operasyon uygulamaları için platform güncelleştirmeleri

Microsoft Dynamics 365 Supply Chain Management 10.0.25 platform güncelleştirmeleri içerir. Daha fazla bilgi için bkz. [Finans ve operasyon uygulamalarının 10.0.25 sürümü için platform güncelleştirmeleri (Nisan 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-25.md).

### <a name="bug-fixes"></a>Hata düzeltmeleri

10.0.25'nın parçası olan güncelleştirmelerin her birine dahil edilen hata düzeltmeleri hakkında bilgi için, Lifecycle Services'ta (LCS) oturum açın ve [BB makalesini](https://fix.lcs.dynamics.com/Issue/Details?bugId=654580&dbType=3&qc=3799fa965b008dd980d27cf740e4582e6384ec6601ae8a35b7eaec6f1287a868) görüntüleyin.

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 ve sektör bulutları: 2022 sürüm dalgası 1 planı

İş uygulamalarımız veya platformumuz için gelecek olan ve en son yayımlanan özellikleri merak ediyor musunuz?

[Dynamics 365 ve sektör bulutları: 2022 sürüm dalgası 1 planına](/dynamics365-release-plan/2022wave1/) göz atın. Baştan sona tüm ayrıntıları, planlama için kullanabileceğiniz tek bir belgede bir araya getirdik.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Kaldırılan ve kullanım dışı bırakılan Supply Chain Management özellikleri

[Dynamics 365 Supply Chain Management'taki kaldırılmış veya kullanım dışı bırakılmış özellikler](removed-deprecated-features-scm-updates.md) makalesi Supply Chain Management için kaldırılan veya kullanım dışı bırakılan veya kaldırılması ya da kullanım dışı bırakılması planlanan özellikleri açıklar.

- *Kaldırılan* özellik artık üründe bulunmaz.
- *Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Herhangi bir özellik üründen kaldırılmadan önce, kullanım dışı bırakma bildirimi kaldırma işleminden 12 ay önce [Dynamics 365 Supply Chain Management'taki kaldırılan veya kullanım dışı bırakılan özelliker](removed-deprecated-features-scm-updates.md) makalesinde duyurulacaktır.

Yalnızca derleme zamanını etkileyen ancak korumalı alan ve üretim ortamlarıyla ikili uyumlu olan son dakika değişiklikleri için kullanım dışı bırakma süresi 12 aydan kısa olacaktır. Genellikle, bunlar derleyiciye yapılması gereken işlevsel güncelleştirmelerdir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

