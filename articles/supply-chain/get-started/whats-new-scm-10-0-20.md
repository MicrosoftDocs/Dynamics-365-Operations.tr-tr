---
title: Dynamics 365 Supply Chain Management 10.0.20 önizlemesi (2021 Ağustos)
description: Bu konuda, Dynamics 365 Supply Chain Management 10.0.20'daki yeni veya değişen özellikler açıklanmaktadır.
author: kamaybac
ms.date: 05/28/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 3a35d3becbf81c51d29ef2e0f4cbf6a12cd196b8
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187638"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10020-august-2021"></a>Dynamics 365 Supply Chain Management 10.0.20 önizlemesi (2021 Ağustos)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bu konuda, Microsoft Dynamics 365 Supply Chain Management önizleme sürümü 10.0.20'deki yeni veya değişen özellikler listelenmektedir. Bu sürüm, 10.0.886 derleme numarasına sahiptir ve aşağıdaki gibi kullanıma sunulmuştur:

- **Sürümün önizlemesi:** Mayıs 2021
- **Sürüm genel kullanılabilirliği (kendi kendine güncelleştirme):** Temmuz 2021
- **Sürüm genel kullanılabilirliği (otomatik güncelleştirme):** Temmuz 2021


## <a name="features-included-in-this-release"></a>Bu sürümdeki özellikler

Aşağıdaki tabloda, bu sürümde yer alan özellikler yer almaktadır. *Özellik* sütunu, her bir özellik için resmi kullanıma sunma tarihlerini görebileceğiniz [kullanıma sunma planına](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) bağlantılar sağlar. *Ek bilgi* sütunu, ilgili belgelerin diğer ayrıntılrını ve/veya bağlantılarını sağlar.

Bu özelliklerin çoğunun kullanılabilmesi için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) kullanılarak etkinleştirilmesi gerekir. Listelenen özelliklerden bazıları hala önizleme görünümünde, bazılaru genel olarak kullanılabilir durumda olabilir.

| Özellik alanı | Özellik | Daha fazla bilgi |
|---|---|---|
| Stok&nbsp;ve&nbsp;lojistik | [Satış siparişi ayrıntıları performans iyileştirmesi](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-order-details-performance-enhancement) | Bu özellik satış siparişlerini açarken özellikle birçok satır içeren siparişler için Kullanıcı arabirimini daha fazla tepki verir. |
| İmalat | [Kalite emirleri oluşturmak için proses otomasyon akışlarını çağırın](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/invoke-process-automation-flows-create-quality-orders) | [Kalite emirleri oluşturmak için proses otomasyon akışlarını çağırın](../production-control/process-automation-quality-orders.md ) |
| İmalat | [Üretim için geliştirilmiş üretim katı yürütme arabirimi](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-manufacturing) | [Üretim katı yürütme arabirimini yapılandırma](../production-control/production-floor-execution-configure.md) |
| Ürün bilgileri yönetimi | [Formüllerdeki ve içeriklerindeki değişiklikleri yönetme](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/engineering-change-management-support-process-manufacturing) | [Formüllerdeki ve içeriklerindeki değişiklikleri yönetme](../engineering-change-management/manage-formula-changes.md) |
| Ürün bilgileri yönetimi | [Ürün hazır olma denetimleri](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/product-readiness-checks) | [Ürün hazırlığı](../engineering-change-management/product-readiness.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Bu sürümdeki özellik iyileştirmeleri

Aşağıdaki tabloda, bu sürümde yer alan özellik iyileştirmeleri yer almaktadır. Bunların her biri varolan bir özellik için artımlı bir geliştirme sağlar. Bunlar yalnızca geliştirmeler olduğundan, [sürüm planında](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) listelenmezler. Ancak, bu geliştirmelerin mevcut özelleştirmelerinizle veya tercihlerinizle çakışmayacağından emin olmak için, her biri varsayılan olarak kapatılmıştır (aksi belirtilmedikçe). Bu özelliklerden herhangi birini kullanmak istiyorsanız, bunları [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'nde açıkça etkinleştirmeniz gerekir.

| Özellik alanı | Özellik&nbsp;yönetiminde&nbsp;özellik&nbsp;adı | Daha fazla bilgi |
|---|---|---|
| Master planlama | Planlama Optimizasyonu için Negatif günler | Bu önizleme özelliği , tedarik gruplarında tanımlanan **negatif günle** r parametresine dayalı olarak gecikme toleransını dikkate almak Için planlama en iyileştirmesi sağlar. |
| Master planlama | Ayarlanan talep tahmininin paralel yetkilendirmesi | Bu özellik, ayarlanmış talep tahmin sayfasından **ayarlanmış talep tahmininin** paralel olarak yetkilendirilmeye olanak tanır. Yüksek sayıda tahminlerde yetki bulunduğunda, bu özelliğin amacı performansı artırmakla aynıdır. Yetkilendirilme sırasında, Kullanıcı, Yetkilendirme iletişim kutusundaki **iş parçacığı sayısını** belirtebilir. |
| Master planlama | (Önizleme) Planlı toplu ve paketli siparişler için toplu iş olarak yürütülebilen kesinleştirme ve konsolidasyon | Bu özellik sayesinde planlı toplu paketli siparişleri kesinleştirmek ve konsolide etmek için toplu işleri kullanabilirsiniz. |
| Üretim denetimi | Genel rotaları kopyala | Bu özellik, madde özel olmayan rotaları kullanıcıların kopyalamasına olanak tanımak için rotayı Kopyala işlevini geliştirir. Bir maddeye henüz atanmamış bir rotanın üzerine yazmak için rota işlevini Kopyala işlevi kullanıldıktan sonra, sistemin tüm ilgili bilgileri (tesis, rota grubu, kaynak gereksinimleri ve çeşitli saatler gibi) güncelleştirmesi için olanak tanır. |
| Üretim denetimi | Bir rota işlemi değiştirildiğinde ilgili kaynak gereksinimlerini güncelleştir | Bu özellik, bir kullanıcı mevcut bir rota adımının işlemini değiştirdikten sonra sistemin ilgili kaynak gereksinimlerini güncelleştirmesini sağlar. |
| Ürün bilgileri yönetimi | Ürün reçetesi raporu zaman aşımını önleme için ön işlem | Bu özellik, ürün reçetesi raporunun önceden işlenmesine neden olur. Bu, rapor için büyük bir veri yükü olduğunda zaman aşımı sorunlarını ortadan kaldıracak. |
| Tedarik ve kaynak atama | Tedarikle ilgili iş akışlarını sıfırlamayı etkinleştir | Bu önizleme özelliği, aşağıdaki iş akışlarını taslak durumuna sıfırlamanıza olanak sağlar: Satınalma Siparişi, satıcı değişikliği ve Satınalma Talepleri. |
| Taşıma yönetimi | Navlun faturası atarken satıcı fatura günlüğü oluşturmayı etkinleştir | Bu özellik etkinleştirildiğinde, yalnızca ödeme-satıcı seçeneğini kullanırken mutabakat nedenleriyle ilgili bir satıcı faturası günlüğü oluşturulur. Aksi takdirde, her zaman fatura günlüğü oluşturulur. |
| Ambar yönetimi | Stok yenileme işleri için seçilen şablonları doğrula | Bu özellik, kullanıcıların bir stok yenileme işi ayarlarken geçerli stok yenileme şablonları seçmesini sağlar. Kullanıcıların bir şablon olmadan bir stok yenileme işi oluşturmasını ve *dalga talep* türünde şablon seçmesini engeller. Bu işlem, stok yenileme çalışması oluşturmayacak ve işlenmesi uzun sürebilir. |

## <a name="new-and-updated-documentation-resources"></a>Yeni ve güncelleştirilmiş belge kaynakları

Aşağıdaki yardım konularını yakın bir zamanda ekledik veya önemli ölçüde güncelleştirdik. Önceki bölümde listelendiği gibi, bunların bu sürüm için eklenen yeni özelliklerle ilgili olması gerekmez ancak var olan özelliklerden daha fazla bilgi almanıza yardımcı olabilirler.

| Özellik alanı | Yeni veya güncelleştirilmiş konular |
|---|---|
| Mühendislik değişim yönetimi | [Ürün yaşam döngüsü durumu ve hareketler](../engineering-change-management/product-lifecycle-state-transactions.md) |
| Stok Yönetimi | [Stok Görünürlüğü Eklentisi](../inventory/inventory-visibility.md)<br><br>[Kalite ve uyumsuzluk yönetimine genel bakış](../inventory/quality-management-processes.md) (artı tüm ilgili kalite-yönetim konuları) |
| Tedarik ve kaynak atama | [Satıcı sertifikasyonunu koruma](../../finance/public-sector/manage-vendor-certification.md) |
| Üretim denetimi | [Üretim katı yürütme arabirimini düzenleme](../production-control/production-floor-execution-styles.md) |
| Ambar yönetimi | [Warehouse Management mobil uygulaması için adım simgeleri ve başlıklar atama](../warehousing/step-icons-titles.md)<br><br>[Manuel stok hareketinin ertelenmiş işlemesi](../warehousing/deferred-processing-manual-inventory-movement.md) |

## <a name="additional-resources"></a>Ek kaynaklar

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finance and Operations uygulamaları için platform güncelleştirmeleri

Microsoft Dynamics 365 Supply Chain Management 10.0.20 platform güncelleştirmeleri içerir. Daha fazla bilgi için bkz. [Finance and Operations uygulamalarının 10.0.20 sürümü için platform güncelleştirmeleri (Temmuz 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20.md). <!-- KFM: Confirm link -->

### <a name="bug-fixes"></a>Hata düzeltmeleri

10.0.20'nın parçası olan güncelleştirmelerin her birine dahil edilen hata düzeltmeleri hakkında bilgi için, Lifecycle Services'ta (LCS) oturum açın ve [BB makalesini](https://fix.lcs.dynamics.com/Issue/Details?bugId=586707&dbType=3&qc=d0dad8eee2af234e8c288e2a7df14c579004518673d014be511f900cfed008f8) görüntüleyin. 

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365: 2021 sürüm dalgası 1 planı

İş uygulamalarımız veya platformumuz için gelecek olan ve en son yayımlanan özellikleri merak ediyor musunuz?

[Dynamics 365: 2021 sürüm dalgası 1 planını](/dynamics365-release-plan/2021wave1/) inceleyin. Baştan sona tüm ayrıntıları, planlama için kullanabileceğiniz tek bir belgede bir araya getirdik.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Kaldırılan ve kullanım dışı bırakılan Supply Chain Management özellikleri

[Dynamics 365 Supply Chain Management'taki kaldırılmış veya kullanım dışı bırakılmış özellikler](removed-deprecated-features-scm-updates.md) konusu Supply Chain Management için kaldırılan veya kullanım dışı bırakılan veya kaldırılması ya da kullanım dışı bırakılması planlanan özellikleri açıklar.

- *Kaldırılan* özellik artık üründe bulunmaz.
- *Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Herhangi bir özellik üründen kaldırılmadan önce, kullanım dışı bırakma bildirimi kaldırma işleminden 12 ay önce [Dynamics 365 Supply Chain Management'taki kaldırılan veya kullanım dışı bırakılan özelliker](removed-deprecated-features-scm-updates.md) konusunda duyurulacaktır.

Yalnızca derleme zamanını etkileyen ancak korumalı alan ve üretim ortamlarıyla ikili uyumlu olan son dakika değişiklikleri için kullanım dışı bırakma süresi 12 aydan kısa olacaktır. Genellikle, bunlar derleyiciye yapılması gereken işlevsel güncelleştirmelerdir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
