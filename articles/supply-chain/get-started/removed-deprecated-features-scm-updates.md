---
title: Dynamics 365 Supply Chain Management'ta kaldırılan veya artık kullanılmayan özellikler
description: Bu konu Dynamics 365 Supply Chain Management'taki kaldırılmış veya kaldırılması planlanan özellikleri açıklar.
author: kamaybac
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: d4d2805e36f132660152370cbeee856862ad6faa
ms.sourcegitcommit: 069ed5789517b550065e5e2317658fec4027359e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/07/2020
ms.locfileid: "4689550"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Dynamics 365 Supply Chain Management'ta kaldırılan veya artık kullanılmayan özellikler

[!include [banner](../includes/banner.md)]

Dynamics 365 Supply Chain Management için kaldırılan veya kullanımı sonlandırılan yeni özellikler belgelendiğinde bu konu güncelleştirilecektir.

- *Kaldırılan* özellik artık üründe bulunmaz.
- *Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Bu liste, kaldırılan veya kullanımına son verilen özellikleri kendi planlamanız için göz önünde bulundurmanız amacıyla hazırlanmıştır.

> [!NOTE]
> Finance and Operations uygulamlarındai nesneler hakkında ayrıntılı bilgiye [Teknik referans](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep) raporları altından ulaşabilirsiniz. Finance and Operations uygulamalarının her sürümünde değiştirilen veya kaldırılan nesneler hakkında bilgi edinmek için bu raporların farklı sürümlerini karşılaştırabilirsiniz.

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10015-release"></a>Supply Chain Management 10.0.15 sürümünden kaldırılan veya kullanım dışı bırakılan özellikler

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Dynamics 365 için Internet Explorer 11 desteği kullanım dışı bırakılmıştır

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Aralık 2020 itibarıyla geçerli olmak üzere, tüm Dynamics 365 ürünleri için Microsoft Internet Explorer 11 desteği kullanım dışı, bırakılacaktır ve Internet Explorer 11, Ağustos 2021'den sonra desteklenmeyecektir.<br><br>Bu, Internet Explorer 11 arabirimi aracılığıyla kullanılmak üzere tasarlanmış olan Dynamics 365 ürünlerini kullanan müşterileri etkileyecektir. Ağustos 2021'den sonra, Internet Explorer 11, bu tür Dynamics 365 ürünleri için desteklenmeyecektir. |
| **Başka bir özellikle mi değiştirildi?**   | Müşterilerin Microsoft Edge'e geçiş yapması önerilir.|
| **Etkilenen ürün alanları**         | Tüm Dynamics 365 ürünleri |
| **Dağıtım seçeneği**              | Tümü|
| **Durum**                         | Kaldırıldı. Internet Explorer 11 Ağustos 2021'den sonra desteklenmeyecektir.|

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-manufacturing-scenarios"></a>Üretim senaryoları için yerleşik Supply Chain Management master planlama altyapısı kullanımı

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Master planlama çalışması sırasında performansı artırmak ve SQL veritabanı yükünü en aza indirmek için, yerleşik Supply Chain Management master planlama altyapısı Planlamayı En İyi Duruma Getirme ile değiştiriliyor. Planlamayı En İyi Duruma Getirme, çalışma saatleri sırasında bile gerçekleştirilebilecek hızlı planlama çalıştırma olanağı sağlar. Bu, planlayıcıların talep veya planlama parametrelerinde yapılan değişikliklere hemen tepki vermesine olanak sağlar. |
| **Başka bir özellikle mi değiştirildi?**   | Evet, Planlamayı En İyi Duruma Getirme hizmeti mevcut yerleşik Supply Chain Management master planlama altyapısının yerini alacaktır. |
| **Etkilenen ürün alanları**         | Supply Chain Management - Master planlama |
| **Dağıtım seçeneği**              | Yalnızca bulut. Planlamayı En İyi Duruma Getirme şirket içi dağıtımlarda desteklenmez. |
| **Durum**                         | Kaldırıldı. 1 Ekim 2021 itibarıyla, üretim senaryoları artık yerleşik Dynamics 365 Supply Chain Management master planlama altyapısıyla desteklenmeyecektir. Üretim senaryoları için müşterilerin master planlama hesaplamaları için Planlama İyileştirmesi'ni kullanmaları gerekir. Daha fazla bilgi için bkz. [Planlamayı En İyi Duruma Getirme belgeleri](https://go.microsoft.com/fwlink/?linkid=2105830). Dynamics 365 Supply Chain Management'ın şirket içi dağıtımlarına sahip olan müşteriler, Ekim 2021 sonrasında üretim senaryoları için Supply Chain Management master planlama altyapısını kullanmaya devam edebilir. Ancak, daha fazla özellik geliştirmesi sağlanmayacaktır. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Supply Chain Management 10.0.11 sürümünden kaldırılan veya kullanım dışı bırakılan özellikler

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>Sağıtım senaryoları için yerleşik Supply Chain Management master planlama altyapısı kullanımı

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Master planlama çalışması sırasında performansı artırmak ve SQL veritabanı yükünü en aza indirmek için, yerleşik Supply Chain Management master planlama altyapısı Planlamayı En İyi Duruma Getirme ile değiştiriliyor. Planlamayı En İyi Duruma Getirme, çalışma saatleri sırasında bile gerçekleştirilebilecek hızlı planlama çalıştırma olanağı sağlar. Bu, planlayıcıların talep veya planlama parametrelerinde yapılan değişikliklere hemen tepki vermesine olanak sağlar. |
| **Başka bir özellikle mi değiştirildi?**   | Evet, Planlamayı En İyi Duruma Getirme hizmeti mevcut yerleşik Supply Chain Management master planlama altyapısının yerini alacaktır. |
| **Etkilenen ürün alanları**         | Supply Chain Management - Master planlama |
| **Dağıtım seçeneği**              | Yalnızca bulut. Planlamayı En İyi Duruma Getirme şirket içi dağıtımlarda desteklenmez. |
| **Durum**                         | Kaldırıldı. 1 Nisan 2021 itibarıyla, dağıtım senaryoları artık yerleşik Dynamics 365 Supply Chain Management master planlama altyapısıyla desteklenmeyecektir. Dağıtım senaryoları için, müşterilerin master planlama hesaplamaları için Planlamayı En İyi Duruma Getirme kullanmaları gerekir. Daha fazla bilgi için bkz. [Planlamayı En İyi Duruma Getirme belgeleri](https://go.microsoft.com/fwlink/?linkid=2105830). Dynamics 365 Supply Chain Management'ın şirket içi dağıtımlarına sahip olan müşteriler, 2021 Nisan sonrasında dağıtım senaryoları için Supply Chain Management master planlama altyapısını kullanmaya devam edebilir. Ancak, daha fazla özellik geliştirmesi sağlanmayacaktır. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Kaldırılmış veya kullanım dışı bırakılmış özellikler hakkındaki önceki duyurular

Önceki sürümlerde kaldırılmış veya kaldırılmış özellikler hakkında daha fazla bilgi edinmek için, [önceki sürümlerdeki kaldırılmış veya kaldırılmış özelliklere](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md) bakın.
