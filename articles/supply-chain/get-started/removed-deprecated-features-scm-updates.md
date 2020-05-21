---
title: Dynamics 365 Supply Chain Management'ta kaldırılan veya artık kullanılmayan özellikler
description: Bu konu Dynamics 365 Supply Chain Management'taki kaldırılmış veya kaldırılması planlanan özellikleri açıklar.
author: kamaybac
manager: AnnBe
ms.date: 04/30/2020
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
ms.openlocfilehash: 7502cd16129431d41d152508fb3b49ff85a5a9f8
ms.sourcegitcommit: f1db998ecfccca660eb15cc2739b12c8463fa54d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2020
ms.locfileid: "3331260"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Dynamics 365 Supply Chain Management'ta kaldırılan veya artık kullanılmayan özellikler

[!include [banner](../includes/banner.md)]

Dynamics 365 Supply Chain Management için kaldırılan veya kullanımı sonlandırılan yeni özellikler belgelendiğinde bu konu güncelleştirilecektir.

- *Kaldırılan* özellik artık üründe bulunmaz.
- *Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Bu liste, kaldırılan veya kullanımına son verilen özellikleri kendi planlamanız için göz önünde bulundurmanız amacıyla hazırlanmıştır.

> [!NOTE]
> Finance and Operations uygulamlarındai nesneler hakkında ayrıntılı bilgiye [Teknik referans](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep) raporları altından ulaşabilirsiniz. Finance and Operations uygulamalarının her sürümünde değiştirilen veya kaldırılan nesneler hakkında bilgi edinmek için bu raporların farklı sürümlerini karşılaştırabilirsiniz.

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Supply Chain Management 10.0.11 sürümünden kaldırılan veya kullanım dışı bırakılan özellikler

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>Sağıtım senaryoları için yerleşik Supply Chain Management master planlama altyapısı kullanımı

|   |  |
|------------|--------------------|
| **Kullanımı sonlandırma/kaldırma nedeni** | Master planlama çalışması sırasında performansı artırmak ve SQL veritabanı yükünü en aza indirmek için, yerleşik Supply Chain Management master planlama altyapısı Planlamayı En İyi Duruma Getirme ile değiştiriliyor. Planlamayı En İyi Duruma Getirme, çalışma saatleri sırasında bile gerçekleştirilebilecek hızlı planlama çalıştırma olanağı sağlar. Bu, planlayıcıların talep veya planlama parametrelerinde yapılan değişikliklere hemen tepki vermesine olanak sağlar. |
| **Başka bir özellikle mi değiştirildi?**   | Evet, Planlamayı En İyi Duruma Getirme hizmeti mevcut yerleşik Supply Chain Management master planlama altyapısının yerini alacaktır. |
| **Etkilenen ürün alanları**         | Supply Chain Management - Master planlama |
| **Dağıtım seçeneği**              | Yalnızca bulut. Planlamayı En İyi Duruma Getirme şirket içi dağıtımlarda desteklenmez. |
| **Durum**                         | Kaldırıldı. Nisan 2021'de dağıtım senaryoları artık yerleşik Dynamics 365 Supply Chain Management master planlama altyapısıyla desteklenmeyecektir. Dağıtım senaryoları için, müşterilerin master planlama hesaplamaları için Planlamayı En İyi Duruma Getirme kullanmaları gerekir. Daha fazla bilgi için bkz. [Planlamayı En İyi Duruma Getirme belgeleri](https://go.microsoft.com/fwlink/?linkid=2105830). Dynamics 365 Supply Chain Management'ın şirket içi dağıtımlarına sahip olan müşteriler, 2021 Nisan sonrasında dağıtım senaryoları için Supply Chain Management master planlama altyapısını kullanmaya devam edebilir. Ancak, daha fazla özellik geliştirmesi sağlanmayacaktır. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Kaldırılmış veya kullanım dışı bırakılmış özellikler hakkındaki önceki duyurular

Önceki sürümlerde kaldırılmış veya kaldırılmış özellikler hakkında daha fazla bilgi edinmek için, [önceki sürümlerdeki kaldırılmış veya kaldırılmış özelliklere](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md) bakın.
