---
title: Dynamics 365 Supply Chain Management'ta kaldırılan veya artık kullanılmayan özellikler
description: Bu konu Dynamics 365 Supply Chain Management'taki kaldırılmış veya kaldırılması planlanan özellikleri açıklar.
author: kamaybac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 43e57b75933a67c1ee3fb0a59400b0d1bdab931cec5826346247cc361a0206df
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720432"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Dynamics 365 Supply Chain Management'ta kaldırılan veya artık kullanılmayan özellikler

[!include [banner](../includes/banner.md)]

Dynamics 365 Supply Chain Management için kaldırılan veya kullanımı sonlandırılan yeni özellikler belgelendiğinde bu konu güncelleştirilecektir.

- *Kaldırılan* özellik artık üründe bulunmaz.
- *Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Bu liste, kaldırılan veya kullanımına son verilen özellikleri kendi planlamanız için göz önünde bulundurmanız amacıyla hazırlanmıştır.

> [!NOTE]
> Finance and Operations uygulamlarındai nesneler hakkında ayrıntılı bilgiye [Teknik referans](/dynamics/s-e/) raporları altından ulaşabilirsiniz. Finance and Operations uygulamalarının her sürümünde değiştirilen veya kaldırılan nesneler hakkında bilgi edinmek için bu raporların farklı sürümlerini karşılaştırabilirsiniz.


## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10019-release"></a>Supply Chain Management 10.0.19 sürümünden kaldırılan veya kullanım dışı bırakılan özellikler

### <a name="job-card-device"></a>İş kartı cihazı

| &nbsp;  | &nbsp;  |
|---|---|
| **Kullanımı sonlandırma/kaldırma nedeni** | [İş kartı cihazı,](../production-control/config-job-card-device.md) yeni [üretim katı yürütme arabirimiyle](../production-control/production-floor-execution-configure.md) değiştiriliyor. |
| **Başka bir özellikle mi değiştirildi?**   | Evet, [iş kartı cihazı,](../production-control/config-job-card-device.md) yeni [üretim katı yürütme arabirimiyle](../production-control/production-floor-execution-configure.md) değiştirilecek. |
| **Etkilenen ürün alanları** | Supply Chain Management - üretim denetimi |
| **Dağıtım seçeneği** | Bulut ve Şirket içi |
| **Durum** | Kaldırıldı. İş kartı cihazı hata ve güvenlik düzeltmesi desteği alacaktır, ancak özellik geliştirmeleri artık sağlanmayacaktır. Nisan 2022 tarihinden sonra, iş kartı cihazı artık desteklenmeyecek ve müşterilerin yeni üretim katı yürütme arabirimine taşınması istenecektir. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10018-release"></a>Supply Chain Management 10.0.18 sürümünden kaldırılan veya kullanım dışı bırakılan özellikler

### <a name="dynamics-365-for-finance-and-operations---warehousing-the-warehouse-app"></a>Dynamics 365 for Finance and Operations: Depolama (ambar uygulaması)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Nisan 2021'den itibaren, *Dynamics 365 for Finance and Operations -Ambar* (ambar uygulaması) kullanım dışıdır ve Nisan 2022'den sonra desteklenmeyecektir. Şimdi Supply Chain Management 10.0.17 sürümüyle yayınlanan *ambar yönetimi mobil uygulaması* yerini almıştır. Yeni uygulama tam bir değişiklik yapar ama geçişi kolaylaştıran aynı temel çerçeveyi kullanır. Gerekirse, kullanıcılar, yeni uygulamayı kullanmaya alışana kadar iki uygulama yan yana kullanılabilir.<br><br>Yeni Ambar Yönetimi mobil uygulaması hakkında daha fazla bilgi için bkz. [Ambar Yönetimi mobil uygulamasını](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-application) ve [Ambar Yönetimi mobil uygulamasını yükleme ve bağlama](../warehousing/install-configure-warehouse-management-app.md). |
| **Başka bir özellikle mi değiştirildi?**   | Evet, yeni ambar yönetimi mobil uygulaması ile değiştirildi. |
| **Etkilenen ürün alanları**         | Supply Chain Management - ambar uygulaması |
| **Dağıtım seçeneği**              | Bulut ve Şirket içi |
| **Durum**                         | Kaldırıldı. Ambar uygulaması hata ve güvenlik düzeltmesi desteği alacaktır, ancak özellik geliştirmeleri artık sağlanmayacaktır. Nisan 2022 tarihinden sonra, eski ambar uygulaması artık desteklenmeyecek ve müşterilerin yeni ambar yönetimi mobil uygulamasına taşınması istenecektir. Eski ambar uygulaması daha sonra Microsoft Store ve Google Play Store'dan kaldırılacaktır.  |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10015-release"></a>Supply Chain Management 10.0.15 sürümünden kaldırılan veya kullanım dışı bırakılan özellikler

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Dynamics 365 için Internet Explorer 11 desteği kullanım dışı bırakılmıştır

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Aralık 2020 itibarıyla geçerli olmak üzere, tüm Dynamics 365 ürünleri için Microsoft Internet Explorer 11 desteği kullanım dışı, bırakılacaktır ve Internet Explorer 11, Ağustos 2021'den sonra desteklenmeyecektir.<br><br>Bu, Internet Explorer 11 arabirimi aracılığıyla kullanılmak üzere tasarlanmış olan Dynamics 365 ürünlerini kullanan müşterileri etkileyecektir. Ağustos 2021'den sonra, Internet Explorer 11, bu tür Dynamics 365 ürünleri için desteklenmeyecektir. |
| **Başka bir özellikle mi değiştirildi?**   | Müşterilerin Microsoft Edge'e geçiş yapması önerilir.|
| **Etkilenen ürün alanları**         | Tüm Dynamics 365 ürünleri |
| **Dağıtım seçeneği**              | Tümü|
| **Durum**                         | Kaldırıldı. Internet Explorer 11 Ağustos 2021'den sonra desteklenmeyecektir.|

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-manufacturing-scenarios"></a>Üretim senaryoları için yerleşik Supply Chain Management master planlama altyapısı kullanımı

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Master planlama çalışması sırasında performansı artırmak ve SQL veritabanı yükünü en aza indirmek için, yerleşik Supply Chain Management master planlama altyapısı Planlamayı En İyi Duruma Getirme ile değiştiriliyor. Planlamayı En İyi Duruma Getirme, çalışma saatleri sırasında bile gerçekleştirilebilecek hızlı planlama çalıştırma olanağı sağlar. Bu, planlayıcıların talep veya planlama parametrelerinde yapılan değişikliklere hemen tepki vermesine olanak sağlar. |
| **Başka bir özellikle mi değiştirildi?**   | Evet, Planlamayı En İyi Duruma Getirme hizmeti mevcut yerleşik Supply Chain Management master planlama altyapısının yerini alacaktır. |
| **Etkilenen ürün alanları**         | Supply Chain Management - Master planlama |
| **Dağıtım seçeneği**              | Yalnızca bulut. Planlamayı En İyi Duruma Getirme şirket içi dağıtımlarda desteklenmez. |
| **Durum**                         | Kaldırıldı. 1 Nisan 2022 itibarıyla, üretim senaryoları artık yerleşik Dynamics 365 Supply Chain Management master planlama altyapısıyla desteklenmeyecektir. Üretim senaryoları için müşterilerin master planlama hesaplamaları için Planlama İyileştirmesi'ni kullanmaları gerekir. Daha fazla bilgi için bkz. [Planlamayı En İyi Duruma Getirme belgeleri](../master-planning/planning-optimization/planning-optimization-overview.md). Dynamics 365 Supply Chain Management'ın şirket içi dağıtımlarına sahip olan müşteriler, Nisan 2022 sonrasında üretim senaryoları için Supply Chain Management master planlama altyapısını kullanmaya devam edebilir. Ancak, daha fazla özellik geliştirmesi sağlanmayacaktır. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Supply Chain Management 10.0.11 sürümünden kaldırılan veya kullanım dışı bırakılan özellikler

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>Sağıtım senaryoları için yerleşik Supply Chain Management master planlama altyapısı kullanımı

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Master planlama çalışması sırasında performansı artırmak ve SQL veritabanı yükünü en aza indirmek için, yerleşik Supply Chain Management master planlama altyapısı Planlamayı En İyi Duruma Getirme ile değiştiriliyor. Planlamayı En İyi Duruma Getirme, çalışma saatleri sırasında bile gerçekleştirilebilecek hızlı planlama çalıştırma olanağı sağlar. Bu, planlayıcıların talep veya planlama parametrelerinde yapılan değişikliklere hemen tepki vermesine olanak sağlar. |
| **Başka bir özellikle mi değiştirildi?**   | Evet, Planlamayı En İyi Duruma Getirme hizmeti mevcut yerleşik Supply Chain Management master planlama altyapısının yerini alacaktır. |
| **Etkilenen ürün alanları**         | Supply Chain Management - Master planlama |
| **Dağıtım seçeneği**              | Yalnızca bulut. Planlamayı En İyi Duruma Getirme şirket içi dağıtımlarda desteklenmez. |
| **Durum**                         | Kaldırıldı. 1 Nisan 2021 itibarıyla, dağıtım senaryoları artık yerleşik Dynamics 365 Supply Chain Management master planlama altyapısıyla desteklenmeyecektir. Dağıtım senaryoları için, müşterilerin master planlama hesaplamaları için Planlamayı En İyi Duruma Getirme kullanmaları gerekir. Daha fazla bilgi için bkz. [Planlamayı En İyi Duruma Getirme belgeleri](../master-planning/planning-optimization/planning-optimization-overview.md). Dynamics 365 Supply Chain Management'ın şirket içi dağıtımlarına sahip olan müşteriler, 2021 Nisan sonrasında dağıtım senaryoları için Supply Chain Management master planlama altyapısını kullanmaya devam edebilir. Ancak, daha fazla özellik geliştirmesi sağlanmayacaktır. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Kaldırılmış veya kullanım dışı bırakılmış özellikler hakkındaki önceki duyurular

Önceki sürümlerde kaldırılmış veya kaldırılmış özellikler hakkında daha fazla bilgi edinmek için, [önceki sürümlerdeki kaldırılmış veya kaldırılmış özelliklere](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md) bakın.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
