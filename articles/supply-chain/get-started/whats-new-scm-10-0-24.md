---
title: Dynamics 365 Supply Chain Management 10.0.24 önizlemesi (Şubat 2022)
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management 10.0.24'daki yeni veya değişen özellikler açıklanmaktadır.
author: kamaybac
ms.date: 12/03/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 1b5742ddf7e5e2c5c32c446a0bde08f4964d6b95
ms.sourcegitcommit: 96515ddbe2f65905140b16088ba62e9b258863fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/04/2021
ms.locfileid: "7891886"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10024-february-2022"></a>Dynamics 365 Supply Chain Management 10.0.24 önizlemesi (Şubat 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bu konuda, Microsoft Dynamics 365 Supply Chain Management önizleme sürümü 10.0.24'deki yeni veya değişen özellikler listelenmektedir. Bu sürüm, 10.0.1084 derleme numarasına sahiptir ve aşağıdaki gibi kullanıma sunulmuştur:

- **Önizleme sürümü:** Aralık 2021
- **Sürüm genel kullanılabilirliği (otomatik güncelleştirme):** Ocak 2022
- **Sürüm genel kullanılabilirliği (otomatik güncelleştirme):** Şubat 2022

## <a name="features-included-in-this-release"></a>Bu sürümdeki özellikler

Aşağıdaki tabloda, bu sürüme dahil edilen özellikler listelenmektedir. Bu konu ilk kez yayımlandıktan sonra derlemeye eklenen özellikleri dahil etmek için bu konuya güncelleştirmeler uygulayabiliriz.

| Özellik alanı | Özellik | Daha fazla bilgi | Etkinleştiren |
|---|---|---|---|
| Dağıtılmış karma topoloji | [Ölçek birimlerinde gelişmiş ambar yürütme iş yükleri](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-warehouse-execution-workloads-scale-units) | [Bulut ve uç ölçek birimleri için ambar yönetimi iş yükleri](../cloud-edge/cloud-edge-workload-warehousing.md) | Varsayılan olarak etkinleştirilir. |
| Planlama | [Sipariş yenileme sınırı ve çıkış marjı için Planlamayı En İyi Duruma Getirme desteği](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planning-optimization-support-reorder-margin-issue-margin) | [Emniyet marjları](../master-planning/planning-optimization/safety-margins.md) | Varsayılan olarak etkinleştirilir. |

## <a name="feature-enhancements-included-in-this-release"></a>Bu sürümdeki özellik iyileştirmeleri

Aşağıdaki tabloda, bu sürümde dahil edilen özellik iyileştirmeleri listelenmektedir. Bu iyileştirmelerden her biri, mevcut bir özellik için artımlı bir geliştirme sağlar. Bunlar yalnızca iyileştirme olduğundan [sürüm planında](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/planned-features) listelenmez. Ancak, bu geliştirmelerin mevcut özelleştirmelerinizle veya tercihlerinizle çakışmayacağından emin olmak için, her biri varsayılan olarak kapatılmıştır (aksi belirtilmedikçe).

Bu özelliklerden herhangi birini açmak veya kapatmak istiyorsanız bunu [özellik yönetiminde](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) yapmalısınız.

| Modül | Özellik yönetiminde özellik adı | Daha fazla bilgi |
|---|---|---|
| Üretim denetimi | Üretim emirleri için isteğe bağlı malzeme kullanılabilirliği kontrolü | Bu özellik, **Üretim katı yönetimi** çalışma alanından kullanılabilen **Üretim emirlerini serbest bırak** sayfasını açmayı hızlandırır. Bu özellik olmadan, sistem, sayfayı açar açmaz listelenen tüm üretim emirleri için malzemelerin kullanılabilir olup olmadığını otomatik olarak kontrol eder ve bu da çok sayıda siparişiniz varsa önemli zaman alabilir. Bu özellik etkinleştirildiğinde, sistem bunun yerine, malzemeleri yalnızca seçili siparişler için ve gerektiğinde denetlemeyi başlatmak için kullanabileceğiniz bir araç çubuğu düğmesi sağlar. |
| Üretim denetimi | (Önizleme) Üretim katı yürütme arabiriminde malzeme tüketimini kaydetme (WMS dışı) | Bu özellik, çalışanların malzeme tüketimini, toplu iş numaralarını ve seri numaralarını kaydetmek için üretim katı yürütme arabirimini kullanmalarını sağlar. Bu özellik yalnızca gelişmiş ambar işlemlerini (WMS) kullanmak üzere etkinleştirilmemiş maddeleri destekler. WMS etkin maddeler için destek gelecekteki bir sürüm için planlanmıştır.<p>Özellikle proses endüstrilerindekiler olmak üzere bazı üreticilerin, her bir toplu iş veya üretim emri için tüketilen malzeme miktarını açıkça kaydetmesi gerekir. Örneğin, çalışanlar çalışırken tüketilen malzeme miktarını tartmak için bir ölçek kullanabilir. Tam malzeme izlenebilirliğini sağlamak için bu kuruluşların her ürünü üretirken hangi parti numaralarının tüketildiğini de kaydetmeleri gerekir. |
| Üretim denetimi | Bulut ve uç ölçek birimleri için ambar yönetimi iş yükünde tamamlandı olarak bildirme | Bu özellik, uygulama bir bulut veya kenar ölçeği birimindeki ambar yönetimi iş yüküne karşı çalışırken bir üretim veya toplu iş siparişini tamamlandı olarak bildirmek için çalışanların Warehouse Management mobil uygulamasını kullanmasına olanak tanır. Daha fazla bilgi için bkz. [Ölçek biriminde tamamlandı ve yerine kondu olarak bildirme](../cloud-edge/cloud-edge-workload-manufacturing.md#RAF). |
| Üretim denetimi | Bulut ve uç ölçek birimi için ambar yönetimi iş yükünde üretim emrini başlatma | Bu özellik, uygulama bir bulut veya kenar ölçeği birimindeki ambar yönetimi iş yüküne karşı çalışırken bir üretim veya toplu iş siparişini başlatmak için çalışanların Warehouse Management mobil uygulamasını kullanmasına olanak tanır. |
| Ambar yönetimi | Yeni yük planlama workbench'i sayfaları | İki yeni yük planlama workbench'i sayfasını etkinleştirir: **Gelen yük planlama workbench'i** ve **Giden yük planlama workbench'i**. |

## <a name="new-and-updated-documentation-resources"></a>Yeni ve güncelleştirilmiş belge kaynakları

Aşağıdaki yardım konularını yakın bir zamanda ekledik veya önemli ölçüde güncelleştirdik. Bu konuların, önceki bölümde listelendiği üzere bu sürüm için eklenen yeni özelliklerle ilgili olması gerekmez. Ancak mevcut özelliklerden daha fazla yararlanmanıza yardımcı olabilirler.

| Özellik alanı | Yeni veya güncelleştirilmiş konular |
|---|---|
| Maliyet yönetimi | [Stok değeri raporları](../cost-management/inventory-value-report-storage.md) |
| Maliyet yönetimi | [Stok değer raporu örnekleri ve mantığı](../cost-management/inventory-value-report-examples.md) |
| Master planlama | [Planlama Optimizasyonu tarafından kullanılan tarih ve saat parametreleri](../master-planning/planning-optimization/date-time-used.md) |
| Master planlama | [Talep tahmini kurulumu](../master-planning/demand-forecasting-setup.md) |
| Master planlama | [Maddeler için minimum kapsamı güncelleştirmek için emniyet stoku günlüğünü kullanma](../master-planning/safety-stock-journal.md) |
| Üretim denetimi | [Üretim katı yürütme arabirimini özelleştirme](../production-control/production-floor-execution-customize.md) |
| Üretim denetimi | [Üretim katı yürütme arabirimini düzenleme](../production-control/production-floor-execution-styles.md) |
| Satış ve pazarlama | [Satış geçmişi temizleme işlemi performans iyileştirmeleri](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) |
| Ambar yönetimi | [Mobil cihaz kullanıcı hesapları](../warehousing/mobile-device-work-users.md) |

## <a name="additional-resources"></a>Ek kaynaklar

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finance and Operations uygulamaları için platform güncelleştirmeleri

Microsoft Dynamics 365 Supply Chain Management 10.0.24 platform güncelleştirmeleri içerir. Daha fazla bilgi için bkz. [Finance and Operations uygulamalarının 10.0.24 sürümü için platform güncelleştirmeleri (Kasım 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-24.md).

### <a name="bug-fixes"></a>Hata düzeltmeleri

10.0.24'nın parçası olan güncelleştirmelerin her birine dahil edilen hata düzeltmeleri hakkında bilgi için, Lifecycle Services'ta (LCS) oturum açın ve [BB makalesini](https://fix.lcs.dynamics.com/Issue/Details?bugId=641306&dbType=3&qc=5b1d5e49c96b8a5cfb5601889a413e6f3773ba6500f9bc47310dcc5c54fff42f) görüntüleyin.

### <a name="dynamics-365-and-industry-clouds-2021-release-wave-2-plan"></a>Dynamics 365 ve sektör bulutları: 2021 sürüm dalgası 2 planı

İş uygulamalarımız veya platformumuz için gelecek olan ve en son yayımlanan özellikleri merak ediyor musunuz?

[Dynamics 365 ve sektör bulutları: 2021 sürüm dalgası 2 planına](/dynamics365-release-plan/2021wave2/) göz atın. Baştan sona tüm ayrıntıları, planlama için kullanabileceğiniz tek bir belgede bir araya getirdik.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Kaldırılan ve kullanım dışı bırakılan Supply Chain Management özellikleri

[Dynamics 365 Supply Chain Management'taki kaldırılmış veya kullanım dışı bırakılmış özellikler](removed-deprecated-features-scm-updates.md) konusu Supply Chain Management için kaldırılan veya kullanım dışı bırakılan veya kaldırılması ya da kullanım dışı bırakılması planlanan özellikleri açıklar.

- *Kaldırılan* özellik artık üründe bulunmaz.
- *Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Herhangi bir özellik üründen kaldırılmadan önce, kullanım dışı bırakma bildirimi kaldırma işleminden 12 ay önce [Dynamics 365 Supply Chain Management'taki kaldırılan veya kullanım dışı bırakılan özelliker](removed-deprecated-features-scm-updates.md) konusunda duyurulacaktır.

Yalnızca derleme zamanını etkileyen ancak korumalı alan ve üretim ortamlarıyla ikili uyumlu olan son dakika değişiklikleri için kullanım dışı bırakma süresi 12 aydan kısa olacaktır. Genellikle, bunlar derleyiciye yapılması gereken işlevsel güncelleştirmelerdir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
