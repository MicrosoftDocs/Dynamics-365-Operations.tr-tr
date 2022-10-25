---
title: Dynamics 365 Supply Chain Management 10.0.29 önizlemesi (Ekim 2022)
description: Bu makalede, Microsoft Dynamics 365 Supply Chain Management 10.0.29'taki yeni veya değişen özellikler açıklanmaktadır.
author: kamaybac
ms.date: 08/12/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 62e06f2348ca3524beaaef5d8879c199db56696f
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689296"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10029-october-2022"></a>Dynamics 365 Supply Chain Management 10.0.29 sürümündeki yenilikler veya değişiklikler (Ekim 2022)

[!include [banner](../includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Supply Chain Management sürümü 10.0.29'teki yeni veya değişen özellikler listelenmektedir. Bu sürüm, 10.0.1326 derleme numarasına sahiptir ve aşağıdaki planlamaya göre kullanıma sunulmuştur:

- **Sürümün önizlemesi:** Ağustos 2022
- **Sürüm genel kullanılabilirliği (kendi kendini güncelleştirme):** Eylül 2022
- **Sürüm genel kullanılabilirliği (otomatik güncelleştirme):** Ekim 2022

## <a name="features-included-in-this-release"></a>Bu sürümdeki özellikler

Aşağıdaki tabloda, bu sürüme dahil edilen özellikler listelenmektedir. Bu makale ilk kez yayımlandıktan sonra derlemeye eklenen özellikleri dahil etmek için bu konuya güncelleştirmeler uygulayabiliriz.

| Özellik alanı | Özellik | Daha fazla bilgi | Etkinleştiren |
|---|---|---|---|
| Stok ve lojistik | [Stok Görünürlüğünde WMS maddelerini tahsis etme ve ayırma](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/allocate-reserve-whs-items-inventory-visibility) | Çok yakında | Varsayılan olarak etkin |
| Stok ve lojistik | [Kolaylaştırılmış eldeki stok listelerini önceden yükleme](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/query-inventory-visibility-summary-entity) | [Inventory Visibility uygulamasını kullanma](../inventory/inventory-visibility-power-platform.md) | Hizmet yapılandırması tarafından etkinleştirilir |
| Siparişe göre tedarik otomasyonu | [Özel sipariş tedarik otomasyonu](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/make-to-order-supply-automation) | [Özel sipariş tedarik otomasyonu](../master-planning/make-to-order-supply-automation.md) | Özellik yönetimi:<br>*Özel sipariş tedarik otomasyonu* |
| Planlama | [DDMRP için ayrıntılı öngörüleri görüntüle ve uygulama](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/view-apply-detailed-insights-ddmrp) | [Talep Temelli Malzeme Gereksinimleri Planlamasına genel bakış](../master-planning/planning-optimization/ddmrp-overview.md) | Özellik yönetimi:<br>*(Önizleme) Planlama Optimizasyonu için DDMRP* |
| Üretim denetimi | [Günlüklere nakletmeden önce tamamlanan malları fiziksel olarak kullanılabilir şeklinde işaretleme](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/make-finished-goods-physically-before-posting) | [Günlüklere nakletmeden önce tamamlanan malları fiziksel olarak kullanılabilir şeklinde işaretleme](../production-control/deferred-posting.md) | Özellik yönetimi:<br>*(Önizleme) Günlüklere nakletmeden önce tamamlanan malları fiziksel olarak kullanılabilir şeklinde işaretle* |
| Ambar yönetimi | [Warehouse mobile app'te ilgili verileri arama](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/look-up-relevant-data-within-warehouse-mobile-app) | [Warehouse Management mobil uygulaması sapmalarını kullanarak verileri sorgulama](../warehousing/warehouse-app-data-inquiry.md) | Özellik yönetimi:<br>*Warehouse Management uygulaması veri sorgusu akışı* |

## <a name="feature-enhancements-included-in-this-release"></a>Bu sürümdeki özellik iyileştirmeleri

Aşağıdaki tabloda, bu sürümde dahil edilen özellik iyileştirmeleri listelenmektedir. Bu iyileştirmelerden her biri, mevcut bir özellik için artımlı bir geliştirme sağlar. Bunlar yalnızca iyileştirme olduğundan [sürüm planında](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features) listelenmez. Ancak, bu geliştirmelerin mevcut özelleştirmelerinizle veya tercihlerinizle çakışmayacağından emin olmak için, her biri varsayılan olarak kapatılmıştır (aksi belirtilmedikçe).

Bu özelliklerden herhangi birini açmak veya kapatmak istiyorsanız bunu [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) yapmalısınız.

| Modül | Özellik yönetiminde özellik adı | Daha fazla bilgi |
|---|---|---|
| Maliyet yönetimi | Ortak ürünün beklemedeki fiyatının hesaplanması için iyileştirme | Bu özellik, ortak ürün fiyatlarının çoklu iş parçacıkları kullanılarak hesaplandığı durumlarda oluşabilecek bir çakışmayı giderir. Sistemin her ortak ürün fiyatının yalnızca bir kez hesaplandığından emin olmasını sağlar. Bu hesaplamanın sonucu daha sonra diğer tüm hesaplamalar için giriş olarak kullanılır. Bekleyen bir fiyat zaten varsa, bu fiyat kullanılır. |
| Master planlama | Hareketleri Planlama İyileştirmesi'nde grupla | Bu özellik, Planlama Optimizasyonu kullanılırken tek bir satış siparişi satırı sağlamak için oluşturulan planlı sipariş sayısının azaltılmasına yardımcı olur. Bu özellik etkinleştirildiğinde Planlama Optimizasyonu, bir sipariş satırına ait tüm stok hareketlerini tam miktar için tek bir gereksinim olarak gruplayacaktır. (Bu davranış, yerleşik planlama altyapısı davranışıyla eşleşir.) Tedarik ve talep ayrı olarak gruplandırılır. Bu nedenle özellik, hareketleri böldüğünüzde ve kapsam boyutları olmayan boyutları (toplu iş numaraları veya seri numaraları gibi) kullandığınızda, hareket hacmini azaltmaya yardımcı olur. |
| Tedarik ve kaynak atama | Satıcıyı satın alma siparişleri için beklemeye al | Bu özellik, satınalma siparişleri için satıcıyı beklemeye almanıza olanak tanır. Bir satıcıyı satınalma siparişleri için beklemede olarak işaretleyen yeni bir *Satınalma siparişi* bekleme türü ekler. Satınalma siparişleri için beklemede olan satıcılar için yeni satınalma siparişleri oluşturamazsınız, ancak yine de o satıcılarla ilgili açık fatura veya ödeme işlemlerine devam edebilirsiniz. |
| Satış ve pazarlama | İçeri aktarma sırasında satır net tutarını hesapla | Bu özellik, OData veya çift yazma kullanılarak *Satış siparişi satırları*, *Satış teklifi satırları* veya *İade siparişi satırları* varlığı aracılığıyla verileri içe aktardığınızda, sistemin satır toplamlarını yeniden hesaplaması gerekip gerekmeyeceğini denetlemenize olanak tanır. Sadece satış siparişi satırları, satış teklifi satırları ve/veya iade siparişi satırlarındaki **Net tutar** alanında yapılan değişiklikleri kısıtlayan yürürlükteki ticari sözleşme değerlendirme ilkeleriniz de bulunduğunda geçerlidir. **Satır net tutarını hesapla** adlı bir ayarı, **Alacak hesapları > Kurulum > Alacak hesapları parametreleri** sayfasına ekler. Bu ayar *Evet* olarak ayarlandığında sistem, gerektiğinde satır tutarlarını yeniden hesaplar (dolayısıyla, satır net tutarı için tüm ticari sözleşme değerlendirme ilkeleri göz ardı edilir). Ayar *Hayır* olarak ayarlandığında, satır fiyatı, miktarı ve/veya iskontosundaki gelen değişiklikler satır net tutarının yeniden hesaplanması gerektiğini belirtmiş olsa bile sistem, satır net tutarını hiçbir zaman otomatik olarak hesaplamayacaktır. Bu özellik varsayılan olarak etkinleştirilir ve başlangıçta **Satır net tutarını hesapla**'yı *Evet* olarak ayarlar. *Hayır* ayarı, 10.0.23 öncesi sürümlerde sistem davranışıyla eşleşir ve esas olarak eski tümleştirme senaryolarını desteklemek için sağlanmıştır.<br><br>Daha fazla bilgi için bkz. [Satış siparişlerini, teklifleri ve iadeleri içe aktarırken satır net tutarlarını yeniden hesaplama](../sales-marketing/calc-line-net-amounts-import.md). |
| Satış ve pazarlama | Çoklu iş parçacığı kullanarak satış toplamlarını hesapla | Bu özellik, bir toplu işteki satış toplamlarını hesaplarken sistemin paralel işlemeyi kullanmasını sağlayarak performansı iyileştirmenize yardımcı olur. Özellik, **Satış toplamlarını hesapla** iletişim kutusuna yeni bir **İş parçacığı sayısı** alanı ekler. Hesaplamayı bir toplu işte çalıştırmayı seçerseniz, iş parçacığı sayısı üst sınırını ayarlamak için bu alanı kullanabilirsiniz. Değeri *0* (sıfır) veya *1* olarak ayarlarsanız, tek bir iş parçacığı kullanılır. 1'den büyük olan değerler çoklu iş parçacığını etkinleştirir. |
| Satış ve pazarlama | Şirketlerarası için el ile girilen fiyatları ve iskontoları güncelleştir | Bu özellik, şirketlerarası siparişler için el ile değişiklik ilkeleri desteği ekler. Şirketlerarası satış ve satınalma siparişleri arasında el ile değişiklik ilkelerinin aktarılması için destek içerir. Daha önce, yalnızca şirketlerarası olmayan siparişler için el ile değişiklik ilkeleri desteklenir. Bu özellik etkinleştirildiğinde, bir şirketlerarası siparişte yaptığınız değişiklikleri kaydettikten sonra sistem size fiyatları ve iskontoları güncelleştirme seçeneğini sunar. Bu seçenek, yeni fiyat ve iskonto ayrıntılarını şirketlerarası siparişe uygulamak veya siparişi değiştirilmemiş şekilde bırakmak isteyip istemediğinizi seçmenizi sağlar. |

## <a name="new-and-updated-documentation-resources"></a>Yeni ve güncelleştirilmiş belge kaynakları

Aşağıdaki Yardım makalelerini yakın bir zamanda ekledik veya önemli ölçüde güncelleştirdik. Bu makalelerin, önceki bölümlerde listelendiği üzere bu sürüm için eklenen yeni özelliklerle ilgili olması gerekmez. Ancak mevcut özelliklerden daha fazla yararlanmanıza yardımcı olabilirler.

| Özellik alanı | Yeni veya güncelleştirilmiş makaleler |
|---|---|
| Master planlama, CTP | [CTP kullanarak satış siparişi teslimat tarihlerini hesaplama](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md) |
| Master planlama, DDMRP | [Talep Temelli Malzeme Gereksinimleri Planlamasına genel bakış](../master-planning/planning-optimization/ddmrp-overview.md)<br>[Sisteminiz için DDMRP özelliğini etkinleştirme](../master-planning/planning-optimization/ddmrp-enable.md)<br>[Stok konumlandırma](../master-planning/planning-optimization/ddmrp-inventory-positioning.md)<br>[Tampon profili ve düzeyleri](../master-planning/planning-optimization/ddmrp-buffer-profile-and-levels.md)<br>[Talep-temelli planlama](../master-planning/planning-optimization/ddmrp-planning.md)<br>[Görsel ve işbirliğine dayalı yürütme](../master-planning/planning-optimization/ddmrp-visual-and-collaborative-execution.md) |
| Ambar yönetimi | [Konteynerleri sevkiyat için paketleme](../warehousing/packing-containers.md)<br>[Giden konteynerleri paketlemeye ve sevkiyatları işlemeye yönelik paketleme işi](../warehousing/packing-work.md) |

## <a name="feature-state-changes-in-this-release"></a>Bu sürümdeki özellik durumu değişiklikleri

Aşağıdaki tabloda, 10.0.29 sürümünde zorunlu veya varsayılan olarak açık hale gelen özellikler listelenmektedir. 10.0.29 sürümüne güncelleştirme yaptığınızda, bu özelliklerin tümü sisteminiz için otomatik olarak açılır. Zorunlu özellikler kapatılamaz ancak varsayılan olarak açık olan özellikler [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) kullanılarak kapatılabilir.

Tablo ayrıca, daha önce genel önizlemede bulunan, ancak 10.0.29 sürümünde genel kullanıma sunulacak şekilde değiştirilen özellikleri de listeler, bu da özelliklerin artık üretim ortamlarında kullanım için önerildiği anlamına gelir. Bu değişiklik, özelliklerin artık üretim ortamlarında kullanılması için önerildiğini belirtir. Aksi belirtilmedikçe varsayılan olarak, bu özellikler kapalıdır. Dolayısıyla, bu özellikleri kullanmak istiyorsanız etkinleştirmek için [Özellik yönetimini](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) kullanmanız gerekir.

| Modül | Özellik adı | Yeni özellik durumu |
| --- | --- | --- |
| Kıymet yönetimi | [Üretim katı yürütme arabirimi için varlık yönetim işlevi](../production-control/production-floor-execution-configure.md) | Zorunlu |
| Maliyet yönetimi | [Kapatmada İptal ve ayarlama etiketini Tersine çevir olarak değiştir](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/change-terminology-inventory-closing-cancellation-inventory-closing-reverse) | Zorunlu |
| Maliyet yönetimi | Ürün reçetesi hesaplama ayrıntıları çapraz maliyetlendirme sürümlerini temizleme | Zorunlu |
| Maliyet yönetimi | [Madde fiyatları depolamasını karşılaştır](../cost-management/compare-item-price.md) | Zorunlu |
| Maliyet yönetimi | [Maliyet hesaplama düzeyi](../cost-management/cost-calculation-level.md) | Varsayılan olarak açık |
| Maliyet yönetimi | Stok kapanışını tersine çevirme işlemi için kullanıcı tanımlı toplu iş numarası kurulumunu etkinleştir | Varsayılan olarak açık |
| Maliyet yönetimi | [Stok kapanışının ilerlemesiyle ilgili ayrıntılar](whats-new-scm-10-0-21.md) | Varsayılan olarak açık |
| Maliyet yönetimi | [Stok değeri raporu depolama alanı](../cost-management/inventory-value-report-storage.md) | Zorunlu |
| Maliyet yönetimi | Stok değeri raporu verilerini temizleme | Zorunlu |
| Maliyet yönetimi | Hareketli ortalama, geri dönüş maliyeti sırası | Zorunlu |
| Maliyet yönetimi | Stok kapatma günlüğünü ızgarada göster | Zorunlu |
| Maliyet yönetimi | Tamamen kapatılmamış hareketleri bulunan maddeleri özet biçiminde göster | Zorunlu |
| Stok ve ambar yönetimi | Boş toplu iş öznitelik değerlerine izin ver | Zorunlu |
| Stok ve ambar yönetimi | Stok transfer emri satırlarının satır numaralarını otomatik artırın | Zorunlu |
| Stok ve ambar yönetimi | Satış satırından transfer siparişi oluştur | Zorunlu |
| Stok ve ambar yönetimi | İş akışındaki stok günlüğü satırı alanını devre dışı bırakma | Zorunlu |
| Stok ve ambar yönetimi | Stok kalite yönetimi parametreleri uyarısı özelliğini etkinleştir | Zorunlu |
| Stok ve ambar yönetimi | (Çin) Fiziksel giriş ve çıkış maliyetlerini aylık ortalama maliyetten hariç tut | Varsayılan olarak açık |
| Stok ve ambar yönetimi | [Stok günlüğü onaylama iş akışı](../inventory/inventory-journal-workflow.md) | Zorunlu |
| Stok ve ambar yönetimi | [Eldeki stok rapor depolama alanı](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/inventory-on-hand-report-storage) | Zorunlu |
| Stok ve ambar yönetimi | [Stok yönetimi için kayıtlı görünümler](saved-views-scm.md) | Zorunlu |
| Stok ve ambar yönetimi | Transfer emri iptali | Zorunlu |
| Stok ve ambar yönetimi | Stok günlüklerinde ölçü birimi ve birim miktarı kullanılıyor | Zorunlu |
| Stok ve ambar yönetimi | Stok günlüğünün kilidini açma | Zorunlu |
| İmalat | [Otomatik olarak deftere nakledilen malzeme çekme listeleri için ambarın etkinleştirildiği malzemeleri otomatik çekme](whats-new-scm-10-0-23.md) | Genel kullanılabilir |
| İmalat | Üretim rotası işlemleri için malzeme listesinde stok boyutlarının görüntülenmesini etkinleştir | Zorunlu |
| İmalat | [İş Kartı Cihazında iş sona erdi bildirimi yaparken toplu iş ve seri numaralarını girmek için etkinleştirin](../production-control/report-finished-job-device.md) | Varsayılan olarak açık |
| İmalat | İyileştirilmiş üretim fiili ağırlık miktarı çekme | Varsayılan olarak açık |
| İmalat | [Üretim katı yürütme arabiriminde iş arama](../production-control/production-floor-execution-configure.md) | Zorunlu |
| İmalat | [Üretim yürütme sistemi tümleştirmesi](../production-control/mes-integration.md) | Varsayılan olarak açık |
| İmalat | [Üretim katı yürütme arabirimi için "Günüm" görünümü](../production-control/production-floor-execution-configure.md) | Varsayılan olarak açık |
| İmalat | [Üretim emirleri için isteğe bağlı malzeme kullanılabilirliği kontrolü](whats-new-scm-10-0-24.md) | Varsayılan olarak açık |
| İmalat | [Varsayılan üretim rezervasyonlarını geçersiz kıl](../production-control/override-default-reservation-principle.md) | Zorunlu |
| İmalat | [Üretim katı yürütme arabiriminde malzeme tüketimini kaydetme (WMS dışı)](../production-control/production-floor-execution-configure.md) | Genel kullanılabilir |
| İmalat | [Üretim katı yürütme arabiriminden elde edilen fiili ağırlık öğeleriyle ilgili rapor](../production-control/production-floor-execution-configure.md) | Genel kullanılabilir |
| İmalat | [Üretim katı yürütme arabiriminden ortak ve yan ürünler raporu](../production-control/production-floor-execution-configure.md) | Varsayılan olarak açık |
| İmalat | [Üretim katı yürütme arabiriminde planlama maddelerini raporla](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-process-manufacturing) | Varsayılan olarak açık |
| İmalat | [Üretim denetimi için kayıtlı görünümler](saved-views-scm.md) | Zorunlu |
| İmalat | [Üretim katı yürütme arabiriminde seri, toplu iş ve plaka numaralarının tamamını göster](../production-control/production-floor-execution-configure.md) | Zorunlu |
| İmalat | [Planlanan tüketim tarihine göre hammadde son tarihlerini doğrula](whats-new-scm-10-0-23.md) | Varsayılan olarak açık |
| Master planlama | [Planlama En İyi Duruma Getirme için otomatik kesinleştirme](../master-planning/planning-optimization/planned-order-firming.md) | Zorunlu |
| Master planlama | [Planlı toplu ve paketli siparişler için toplu iş olarak yürütülebilen kesinleştirme ve konsolidasyon](whats-new-scm-10-0-20.md) | Varsayılan olarak açık |
| Master planlama | [Ön işleme filtreleri etkin olduğunda eldeki stoka sahip maddeleri dahil et](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/master-planning-include-items-on-hand-when-pre-processing-filters-are-enabled) | Varsayılan olarak açık |
| Master planlama | [Planlama Optimizasyonu için sonsuz kapasite planlaması](../master-planning/planning-optimization/infinite-capacity-planning.md) | Varsayılan olarak açık |
| Master planlama | [Planlamayı En İyi Duruma Getirme Marjları](../master-planning/planning-optimization/safety-margins.md) | Zorunlu |
| Master planlama | [Planlama Optimizasyonu için Negatif günler](../master-planning/planning-optimization/delay-tolerance.md) | Zorunlu |
| Master planlama | [Ayarlanan talep tahmininin paralel yetkilendirmesi](whats-new-scm-10-0-20.md) | Zorunlu |
| Master planlama | [Filtreleme ile planlı sipariş kesinleştirici](../master-planning/planning-optimization/planned-order-firming.md) | Zorunlu |
| Master planlama | [Planlama Optimizasyonu için planlı üretim emirleri](../master-planning/planning-optimization/production-planning.md) | Zorunlu |
| Master planlama | [Planlamayı En İyi Duruma Getirme için satınalma ticari sözleşmeleri](../master-planning/planning-optimization/purchase-trade-agreement.md) | Zorunlu |
| Master planlama | [Planlı siparişler için kayıtlı görünümler](saved-views-scm.md) | Zorunlu |
| Tedarik ve kaynak atama | Satınalma siparişlerindeki masraf başlangıç ve bitiş tutarları | Zorunlu |
| Tedarik ve kaynak atama | Satınalma talebi dağıtımı sıfırlama düğmesini devre dışı bırakma | Varsayılan olarak açık |
| Tedarik ve kaynak atama | [Tedarikle ilgili iş akışlarını sıfırlamayı etkinleştir](whats-new-scm-10-0-20.md) | Varsayılan olarak açık |
| Tedarik ve kaynak atama | [Toplu iş görevi başına satınalma siparişi satırlarının sayısını sınırla](whats-new-scm-10-0-27.md) | Varsayılan olarak açık |
| Tedarik ve kaynak atama | [Satınalma siparişinde etkin boyut bağlantısı mali boyutuyla satıcıdan alınan mali boyutları birleştir](whats-new-scm-10-0-25.md) | Zorunlu |
| Tedarik ve kaynak atama | [Stoğu tutulan ürünlerin miktarları ve stoğu tutulmayan ürünlerin kalanlarını, girişler ve satıcı faturaları için deftere naklet](whats-new-scm-10-0-26.md) | Genel kullanılabilir |
| Tedarik ve kaynak atama | [İş akışında birden fazla satın alma talebi olduğunda genel bütçe ayırmalarının aşırı kullanımını engelle](whats-new-scm-10-0-21.md) | Varsayılan olarak açık |
| Tedarik ve kaynak atama | [Satınalma sözleşmesi sorumlu taraf](../procurement/purchase-agreements.md) | Zorunlu |
| Tedarik ve kaynak atama | [Satın alma siparişleri için kayıtlı görünümler](saved-views-scm.md) | Zorunlu |
| Ürün bilgileri yönetimi | Zaman aşımını önlemek için ürün reçetesi raporunu ön işleme | Zorunlu |
| Ürün bilgileri yönetimi | Madde şablonları kullanılırken varsayılan mali boyutlar ayrı ayrı kullanılır | Zorunlu |
| Ürün bilgileri yönetimi | Madde şablonları için ürün boyutu gruplarını etkinleştir | Zorunlu |
| Ürün bilgileri yönetimi | Madde - barkod varlığı geliştirmeleri | Zorunlu |
| Ürün bilgileri yönetimi | Ürün çeşidi adlarını terminolojiye göre yeniden oluştur | Zorunlu |
| Ürün bilgileri yönetimi | [Serbest bırakılan ürünler için kayıtlı görünümler](saved-views-scm.md) | Zorunlu |
| Ürün bilgileri yönetimi | [Çeşit önerileri sayfa geliştirmeleri](../pim/tasks/create-predefined-product-variants.md) | Zorunlu |
| Satış ve pazarlama | [Satış siparişinde masraf tahsisatı](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/miscellaneous-charges-enhancements) | Zorunlu |
| Satış ve pazarlama | Satış siparişi güncelleştirme geçmişini temizle | Zorunlu |
| Satış ve pazarlama | [Yaşına göre satış güncelleştirme geçmişini temizle](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) | Zorunlu |
| Satış ve pazarlama | [İlgili kişi veri varlığını dışa aktarma optimizasyonu](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization) | Zorunlu |
| Satış ve pazarlama | Satış alacak dekontu için toplam iskonto grubunu kopyala | Zorunlu |
| Satış ve pazarlama | [Satış teklifi belgesi girişi ve belge sonuç alanlarında aramayı etkinleştir](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | Zorunlu |
| Satış ve pazarlama | ["İlk 100" müşteri raporunun performansını iyileştir](whats-new-scm-10-0-23.md) | Zorunlu |
| Satış ve pazarlama | Geçmiş temizleme görevlerine bekleyen kayıtları dahil et | Zorunlu |
| Satış ve pazarlama | Toplu iş görevi başına satış siparişi satırlarının sayısını sınırla | Varsayılan olarak açık |
| Satış ve pazarlama | [Deftere nakledilmek için seçilebilecek satış siparişi sayısını kısıtlayın](whats-new-scm-10-0-21.md) | Zorunlu |
| Satış ve pazarlama | Tahmini müşteri bakiyelerini yeniden hesapla | Zorunlu |
| Satış ve pazarlama | [Fiili ağırlıklı ve fiili ağırlıksız ondalık hassasiyetli satış iade siparişi satırı kaydı](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-return-order-line-registration-decimal-precision-without-catch-weight) | Zorunlu |
| Satış ve pazarlama | [Satış ve pazarlama için kayıtlı görünümler](saved-views-scm.md) | Zorunlu |
| Satış ve pazarlama | [Tek tıklamayla satış siparişi onayı](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/single-click-sales-order-confirmation) | Zorunlu |
| Taşıma yönetimi | Deftere nakledilen satıcı faturası günlüğü olmayan navlun faturası satırları ile navlun faturalarının farklı olmasına izin ver | Varsayılan olarak açık |
| Taşıma yönetimi | [Navlun faturası atarken satıcı fatura günlüğü oluşturmayı etkinleştir](whats-new-scm-10-0-20.md) | Varsayılan olarak açık |
| Taşıma yönetimi | [Küçük Paket Sevkiyatı](../warehousing/small-parcel-shipping.md) | Zorunlu |
| Taşıma yönetimi | [USMCA kaynak sertifikasyonu belgesi](../transportation/usmca-certification-of-origin.md) | Varsayılan olarak açık |
| Ambar yönetimi | [Ek yerleşim bölgesi](../warehousing/additional-location-zones.md) | Zorunlu |
| Ambar yönetimi | [İşi iptal et](../warehousing/cancel-warehouse-work.md) | Zorunlu |
| Ambar yönetimi | [Sevkiyatı konsolide et](../warehousing/configure-shipment-consolidation-policies.md) | Zorunlu |
| Ambar yönetimi | [Transfer emirlerini ambar uygulamasından oluştur ve işle](../warehousing/create-transfer-order-from-warehouse-app.md) | Zorunlu |
| Ambar yönetimi | Yerleşim yönergeleri olan çapraz sevk şablonları | Varsayılan olarak açık |
| Ambar yönetimi | [Yerine koyma işini ÖSB'lerden ayır](whats-new-scm-10-0-21.md) | Zorunlu |
| Ambar yönetimi | [Ertelenen yerine koyma işlemleri](../warehousing/deferred-processing-manual-inventory-movement.md) | Zorunlu |
| Ambar yönetimi | Ertelenen yerine koyma - konteyner | Varsayılan olarak açık |
| Ambar yönetimi | Ertelenmiş yerine koyma: Tetikleyici olayı Önceki olarak ayarlanan denetim şablonu özelliği için etkinleştirin | Zorunlu |
| Ambar yönetimi | [Durdurulan stoktan örnek alan kalite emirlerinden gelen beklenen girişleri devre dışı bırak](../inventory/inventory-blocking.md) | Varsayılan olarak açık |
| Ambar yönetimi | Ambar mobil cihazları için hızlı doğrulamayı etkinleştir | Zorunlu |
| Ambar yönetimi | [GS1 barkodları için geliştirilmiş ayrıştırıcı](../warehousing/gs1-barcodes.md) | Genel kullanılabilir |
| Ambar yönetimi | [Esnek siparişle taahhüt edilen plaka rezervasyonu](../warehousing/flexible-warehouse-level-dimension-reservation.md) | Zorunlu |
| Ambar yönetimi | [Esnek ambar düzeyinde boyut rezervasyonu](../warehousing/flexible-warehouse-level-dimension-reservation.md) | Zorunlu |
| Ambar yönetimi | [Madde konsolidasyon yerleşimi kullanımı](../warehousing/item-consolidation-location-utilization.md) | Varsayılan olarak açık |
| Ambar yönetimi | Plaka alımı geçmişi | Varsayılan olarak açık |
| Ambar yönetimi | [El ile sevkiyat konsolidasyonu](../warehousing/consolidate-shipments-manual-workbench.md) | Varsayılan olarak açık |
| Ambar yönetimi | [Yönetici veya benzer güvenilen kullanıcılar için el ile transfer satırı çekme hizmeti](whats-new-scm-10-0-28.md) | Genel kullanılabilir |
| Ambar yönetimi | [Malzeme işleme ekipmanı arabirimi](../warehousing/mhax.md) | Zorunlu |
| Ambar yönetimi | [Yeni yük planlama workbench'i sayfaları](whats-new-scm-10-0-24.md) | Genel kullanılabilir |
| Ambar yönetimi | [Giden iş yükü görselleştirmesi](../warehousing/outbound-workload-visualization.md) | Zorunlu |
| Ambar yönetimi | [Planlanmış çapraz sevk](../warehousing/planned-cross-docking.md) | Zorunlu |
| Ambar yönetimi | [Ambar uygulaması olaylarını işle](../warehousing/warehouse-app-events.md) | Zorunlu |
| Ambar yönetimi | Ortak ürün ve yan ürün yerine koyma işi şablonu için sorgu iyileştirmesi | Zorunlu |
| Ambar yönetimi | [Ambara serbest bırakırken miktarları en yakın satış birimine indirgenecek şekilde yuvarla](whats-new-scm-10-0-19.md) | Zorunlu |
| Ambar yönetimi | [Yük planlama çalışma ekranı için kayıtlı görünüm](saved-views-scm.md) | Zorunlu |
| Ambar yönetimi | [İş ayrıntıları sayfası için kayıtlı görünüm](saved-views-scm.md) | Zorunlu |
| Ambar yönetimi | [Dalga işleme için kayıtlı görünüm](saved-views-scm.md) | Zorunlu |
| Ambar yönetimi | [Yük işleme için kayıtlı görünümler](saved-views-scm.md) | Zorunlu |
| Ambar yönetimi | [Sevkiyat işleme için kayıtlı görünümler](saved-views-scm.md) | Zorunlu |
| Ambar yönetimi | [GS1 barkodlarını tara](../warehousing/gs1-barcodes.md) | Genel kullanılabilir |
| Ambar yönetimi | Sevkiyat dalgası etiket ayrıntıları | Zorunlu |
| Ambar yönetimi | [Karışık birimleri yerleştir](whats-new-scm-10-0-21.md) | Zorunlu |
| Ambar yönetimi | [Sevk istasyonunda konteyner kapatma/yeniden açma için daha hızlı API kullanın](whats-new-scm-10-0-21.md) | Varsayılan olarak açık |
| Ambar yönetimi | [Stok yenileme işleri için seçilen şablonları doğrula](whats-new-scm-10-0-20.md) | Varsayılan olarak açık |
| Ambar yönetimi | [Ambar uygulaması yükseltilen alanları](../warehousing/warehouse-app-promoted-fields.md) | Zorunlu |
| Ambar yönetimi | [Ambar uygulaması adım yönergeleri](../warehousing/mobile-app-titles-instructions.md) | Zorunlu |
| Ambar yönetimi | [Ambar yerleşimi durumu](../warehousing/warehouse-location-status.md) | Zorunlu |
| Ambar yönetimi | [Warehouse Management uygulaması sapmaları](../warehousing/warehouse-app-detours.md) | Varsayılan olarak açık |
| Ambar yönetimi | [Dalga toplu iş ayrıntıları](../warehousing/wave-processing.md) | Zorunlu |
| Ambar yönetimi | [Dalga yürütme bildirimleri](../warehousing/wave-execution-notifications.md) | Zorunlu |

## <a name="additional-resources"></a>Ek kaynaklar

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finans ve Operasyon uygulamaları için Platform güncelleştirmeleri

Microsoft Dynamics 365 Supply Chain Management 10.0.29 platform güncelleştirmeleri içerir. Daha fazla bilgi için bkz. [Finans ve Operasyon uygulamalarının 10.0.29 sürümü için platform güncelleştirmeleri (Ekim 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-29.md).

### <a name="bug-fixes"></a>Hata düzeltmeleri

10.0.29 sürümünün parçası olan güncelleştirmelerin her birine dahil edilen hata düzeltmeleri hakkında bilgi için, Lifecycle Services'ta (LCS) oturum açın ve [KB makalesini](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559) görüntüleyin.

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 ve sektör bulutları: 2022 sürüm dalgası 1 planı

İş uygulamalarımız veya platformumuz için gelecek olan ve en son yayımlanan özellikleri merak ediyor musunuz?

[Dynamics 365 ve sektör bulutları: 2022 sürüm dalgası 2 planına](/dynamics365-release-plan/2022wave2/) göz atın. Baştan sona tüm ayrıntıları, planlama için kullanabileceğiniz tek bir belgede bir araya getirdik.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Kaldırılan ve kullanım dışı bırakılan Supply Chain Management özellikleri

[Dynamics 365 Supply Chain Management'taki kaldırılmış veya kullanım dışı bırakılmış özellikler](removed-deprecated-features-scm-updates.md) makalesi Supply Chain Management için kaldırılan veya kullanım dışı bırakılan veya kaldırılması ya da kullanım dışı bırakılması planlanan özellikleri açıklar.

- *Kaldırılan* özellik artık üründe bulunmaz.
- *Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Herhangi bir özellik üründen kaldırılmadan önce, kullanım dışı bırakma bildirimi kaldırma işleminden 12 ay önce [Dynamics 365 Supply Chain Management'taki kaldırılan veya kullanım dışı bırakılan özelliker](removed-deprecated-features-scm-updates.md) makalesinde duyurulacaktır.

Yalnızca derleme zamanını etkileyen ancak korumalı alan ve üretim ortamlarıyla ikili uyumlu olan son dakika değişiklikleri için kullanım dışı bırakma süresi 12 aydan kısa olacaktır. Genellikle, bunlar derleyiciye yapılması gereken işlevsel güncelleştirmelerdir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
