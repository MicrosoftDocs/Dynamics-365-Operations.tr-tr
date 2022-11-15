---
title: Dynamics 365 Supply Chain Management'tan kaldırılan veya kullanım dışı bırakılan özellikler
description: Bu makale Dynamics 365 Supply Chain Management'taki kaldırılmış veya kaldırılması planlanan özellikleri açıklar.
author: kamaybac
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 722b34e89a54715db39259549c11a78d69d2b4d3
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739883"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Dynamics 365 Supply Chain Management'tan kaldırılan veya kullanım dışı bırakılan özellikler

[!include [banner](../includes/banner.md)]

Dynamics 365 Supply Chain Management için kaldırılan veya kullanımı sonlandırılan yeni özellikler belgelendiğinde bu makale güncelleştirilecektir.

- *Kaldırılan* özellik artık üründe bulunmaz.
- *Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Bu liste, kaldırılan veya kullanımına son verilen özellikleri kendi planlamanız için göz önünde bulundurmanız amacıyla hazırlanmıştır.

> [!NOTE]
> Finans ve operasyon uygulamalarındaki nesneler hakkında ayrıntılı bilgiye [Teknik referans raporları](/dynamics/s-e/) altından ulaşabilirsiniz. Finans ve operasyon uygulamalarının her sürümünde değiştirilen veya kaldırılan nesneler hakkında bilgi edinmek için bu raporların farklı sürümlerini karşılaştırabilirsiniz.

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10029-release"></a>Supply Chain Management 10.0.29 sürümünden kaldırılan veya kullanım dışı bırakılan özellikler

### <a name="stock-transfer-orders-that-have-tax-on-the-transfer-price"></a>Transfer fiyatı vergi içeren stok transfer emirleri

| &nbsp;  | &nbsp;  |
|---|---|
| **Kullanımı sonlandırma/kaldırma nedeni** | [Transfer fiyatı vergi içeren stok transfer emirleri](../../finance/localizations/apac-ind-gst-stock-transfer-transactions.md) işlevi [Hindistan için stok transfer emirleri](../../finance/localizations/apac-ind-stock-transfer.md) işleviyle değiştiriliyor. |
| **Başka bir özellikle mi değiştirildi?**   | Evet, [Transfer fiyatı vergi içeren stok transfer emirleri](../../finance/localizations/apac-ind-gst-stock-transfer-transactions.md) işlevi [Hindistan için stok transfer emirleri](../../finance/localizations/apac-ind-stock-transfer.md) işleviyle değiştiriliyor. |
| **Etkilenen ürün alanları** | Supply Chain Management - stok |
| **Dağıtım seçeneği** | Bulut ve Şirket içi |
| **Çalıştırma Durumu** | <p>Kullanım dışı bırakılıyor. *Transfer fiyatı vergi içeren stok transfer emirleri* işlevi artık hata düzeltmeleri ve güvenlik düzeltmeleriyle ilgili destek almayacaktır.</p><p>Nisan 2023 tarihinden sonra müşterilerin varsayılan olarak *Hindistan için stok transfer emirleri* iyileştirilmiş işlevini kullanmaları istenecektir. 2023 Ekim tarihinden sonra, *Transfer fiyatı vergi içeren stok transfer emirleri* işlevi artık kullanılamayacak ve müşterilerin *Hindistan için stok transfer emirleri* geliştirilmiş işlevine geçiş yapması istenecektir.</p><p>Daha fazla bilgi için bkz. [Hindistan için stok transfer emirleri](../../finance/localizations/apac-ind-stock-transfer.md).</p> |

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

### <a name="supply-chain-management--warehousing-the-warehouse-app"></a><a name="wma"></a>Supply Chain Management - Ambarlama (ambar uygulaması)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Nisan 2021'den itibaren, *Supply Chain Management - Ambarlama* (ambar uygulaması) kullanım dışıdır ve Nisan 2022'den sonra desteklenmeyecektir. Şimdi Supply Chain Management 10.0.17 sürümüyle yayınlanan *ambar yönetimi mobil uygulaması* yerini almıştır. Yeni uygulama tam bir değişiklik yapar ama geçişi kolaylaştıran aynı temel çerçeveyi kullanır. Gerekirse, kullanıcılar, yeni uygulamayı kullanmaya alışana kadar iki uygulama yan yana kullanılabilir.<br><br>Yeni Ambar Yönetimi mobil uygulaması hakkında daha fazla bilgi için bkz. [Ambar Yönetimi mobil uygulamasını](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-application) ve [Ambar Yönetimi mobil uygulamasını yükleme ve bağlama](../warehousing/install-configure-warehouse-management-app.md). |
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
| **Durum**                         | Kaldırıldı. 1 Nisan 2022 itibarıyla, üretim senaryoları artık yerleşik Supply Chain Management master planlama altyapısıyla desteklenmeyecektir. Bu tarihten itibaren, Microsoft yerleşik planlama altyapısı için tüm üretim geliştirme senaryolarını durdurur, yeni özellikleri serbest bırakmayacak ve yalnızca kritik hata düzeltmelerini yayımlayacaktır. Bu tarihten sonra, üretim senaryoları için destek gerektiren tüm şirketler master planlama hesaplamalarında Planlama Optimizasyonu kullanmalıdır. Planlama Optimizasyonu, 2022 Ekim tarihinde üretim senaryolarını tam olarak destekleyecek şekilde beklenmektedir. Daha fazla bilgi için [Kullanımdan kaldırılan master planlamaya genel bakış](../master-planning/deprecated-master-planning-overview.md) bölümüne bakın.<br><br>Supply Chain Management'ın şirket içi dağıtımlarına sahip olan şirketler, Nisan 2022 sonrasında üretim senaryoları için yerleşik master planlama altyapısını kullanmaya devam edebilir. Ancak, daha fazla özellik geliştirmesi sağlanmayacaktır. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Supply Chain Management 10.0.11 sürümünden kaldırılan veya kullanım dışı bırakılan özellikler

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>Sağıtım senaryoları için yerleşik Supply Chain Management master planlama altyapısı kullanımı

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Master planlama çalışması sırasında performansı artırmak ve SQL veritabanı yükünü en aza indirmek için, yerleşik Supply Chain Management master planlama altyapısı Planlamayı En İyi Duruma Getirme ile değiştiriliyor. Planlamayı En İyi Duruma Getirme, çalışma saatleri sırasında bile gerçekleştirilebilecek hızlı planlama çalıştırma olanağı sağlar. Bu, planlayıcıların talep veya planlama parametrelerinde yapılan değişikliklere hemen tepki vermesine olanak sağlar. |
| **Başka bir özellikle mi değiştirildi?**   | Evet, Planlamayı En İyi Duruma Getirme hizmeti mevcut yerleşik Supply Chain Management master planlama altyapısının yerini alacaktır. |
| **Etkilenen ürün alanları**         | Supply Chain Management - Master planlama |
| **Dağıtım seçeneği**              | Yalnızca bulut. Planlamayı En İyi Duruma Getirme şirket içi dağıtımlarda desteklenmez. |
| **Durum**                         | Kaldırıldı. 1 Nisan 2021 itibarıyla, dağıtım senaryoları artık yerleşik Dynamics 365 Supply Chain Management master planlama altyapısıyla desteklenmeyecektir. Dağıtım senaryoları için, müşterilerin master planlama hesaplamaları için Planlamayı En İyi Duruma Getirme kullanmaları gerekir. Daha fazla bilgi için [Kullanımdan kaldırılan master planlamaya genel bakış](../master-planning/deprecated-master-planning-overview.md) bölümüne bakın. Dynamics 365 Supply Chain Management'ın şirket içi dağıtımlarına sahip olan müşteriler, 2021 Nisan sonrasında dağıtım senaryoları için Supply Chain Management master planlama altyapısını kullanmaya devam edebilir. Ancak, daha fazla özellik geliştirmesi sağlanmayacaktır. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Kaldırılmış veya kullanım dışı bırakılmış özellikler hakkındaki önceki duyurular

Önceki sürümlerde kaldırılmış veya kaldırılmış özellikler hakkında daha fazla bilgi edinmek için, [önceki sürümlerdeki kaldırılmış veya kaldırılmış özelliklere](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md) bakın.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

