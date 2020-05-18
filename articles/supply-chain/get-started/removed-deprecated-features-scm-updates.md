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
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a><span data-ttu-id="4d18d-103">Dynamics 365 Supply Chain Management'ta kaldırılan veya artık kullanılmayan özellikler</span><span class="sxs-lookup"><span data-stu-id="4d18d-103">Removed or deprecated features in Dynamics 365 Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d18d-104">Dynamics 365 Supply Chain Management için kaldırılan veya kullanımı sonlandırılan yeni özellikler belgelendiğinde bu konu güncelleştirilecektir.</span><span class="sxs-lookup"><span data-stu-id="4d18d-104">This topic will be updated as new removed or deprecated features are documented for Dynamics 365 Supply Chain Management.</span></span>

- <span data-ttu-id="4d18d-105">*Kaldırılan* özellik artık üründe bulunmaz.</span><span class="sxs-lookup"><span data-stu-id="4d18d-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="4d18d-106">*Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.</span><span class="sxs-lookup"><span data-stu-id="4d18d-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="4d18d-107">Bu liste, kaldırılan veya kullanımına son verilen özellikleri kendi planlamanız için göz önünde bulundurmanız amacıyla hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="4d18d-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span>

> [!NOTE]
> <span data-ttu-id="4d18d-108">Finance and Operations uygulamlarındai nesneler hakkında ayrıntılı bilgiye [Teknik referans](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep) raporları altından ulaşabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d18d-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="4d18d-109">Finance and Operations uygulamalarının her sürümünde değiştirilen veya kaldırılan nesneler hakkında bilgi edinmek için bu raporların farklı sürümlerini karşılaştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d18d-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a><span data-ttu-id="4d18d-110">Supply Chain Management 10.0.11 sürümünden kaldırılan veya kullanım dışı bırakılan özellikler</span><span class="sxs-lookup"><span data-stu-id="4d18d-110">Features removed or deprecated in the Supply Chain Management 10.0.11 release</span></span>

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a><span data-ttu-id="4d18d-111">Sağıtım senaryoları için yerleşik Supply Chain Management master planlama altyapısı kullanımı</span><span class="sxs-lookup"><span data-stu-id="4d18d-111">Use of built-in Supply Chain Management master planning engine for distribution scenarios</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="4d18d-112">**Kullanımı sonlandırma/kaldırma nedeni**</span><span class="sxs-lookup"><span data-stu-id="4d18d-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="4d18d-113">Master planlama çalışması sırasında performansı artırmak ve SQL veritabanı yükünü en aza indirmek için, yerleşik Supply Chain Management master planlama altyapısı Planlamayı En İyi Duruma Getirme ile değiştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="4d18d-113">To enhance performance and minimize the SQL database load during master planning runs, the built-in Supply Chain Management master planning engine is being replaced by Planning Optimization.</span></span> <span data-ttu-id="4d18d-114">Planlamayı En İyi Duruma Getirme, çalışma saatleri sırasında bile gerçekleştirilebilecek hızlı planlama çalıştırma olanağı sağlar.</span><span class="sxs-lookup"><span data-stu-id="4d18d-114">Planning Optimization allows for fast planning runs that can be performed even during office hours.</span></span> <span data-ttu-id="4d18d-115">Bu, planlayıcıların talep veya planlama parametrelerinde yapılan değişikliklere hemen tepki vermesine olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="4d18d-115">This enables planners to react immediately to changes in demand or planning parameters.</span></span> |
| <span data-ttu-id="4d18d-116">**Başka bir özellikle mi değiştirildi?**</span><span class="sxs-lookup"><span data-stu-id="4d18d-116">**Replaced by another feature?**</span></span>   | <span data-ttu-id="4d18d-117">Evet, Planlamayı En İyi Duruma Getirme hizmeti mevcut yerleşik Supply Chain Management master planlama altyapısının yerini alacaktır.</span><span class="sxs-lookup"><span data-stu-id="4d18d-117">Yes, Planning Optimization will replace the existing built-in Supply Chain Management master planning engine.</span></span> |
| <span data-ttu-id="4d18d-118">**Etkilenen ürün alanları**</span><span class="sxs-lookup"><span data-stu-id="4d18d-118">**Product areas affected**</span></span>         | <span data-ttu-id="4d18d-119">Supply Chain Management - Master planlama</span><span class="sxs-lookup"><span data-stu-id="4d18d-119">Supply Chain Management - Master planning</span></span> |
| <span data-ttu-id="4d18d-120">**Dağıtım seçeneği**</span><span class="sxs-lookup"><span data-stu-id="4d18d-120">**Deployment option**</span></span>              | <span data-ttu-id="4d18d-121">Yalnızca bulut.</span><span class="sxs-lookup"><span data-stu-id="4d18d-121">Cloud only.</span></span> <span data-ttu-id="4d18d-122">Planlamayı En İyi Duruma Getirme şirket içi dağıtımlarda desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="4d18d-122">Planning Optimization is not supported with on-premises deployments.</span></span> |
| <span data-ttu-id="4d18d-123">**Durum**</span><span class="sxs-lookup"><span data-stu-id="4d18d-123">**Status**</span></span>                         | <span data-ttu-id="4d18d-124">Kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="4d18d-124">Deprecated.</span></span> <span data-ttu-id="4d18d-125">Nisan 2021'de dağıtım senaryoları artık yerleşik Dynamics 365 Supply Chain Management master planlama altyapısıyla desteklenmeyecektir.</span><span class="sxs-lookup"><span data-stu-id="4d18d-125">On April 2021, distribution scenarios will no longer be supported with the built-in Dynamics 365 Supply Chain Management master planning engine.</span></span> <span data-ttu-id="4d18d-126">Dağıtım senaryoları için, müşterilerin master planlama hesaplamaları için Planlamayı En İyi Duruma Getirme kullanmaları gerekir.</span><span class="sxs-lookup"><span data-stu-id="4d18d-126">For distribution scenarios, customers must use Planning Optimization for master planning calculations.</span></span> <span data-ttu-id="4d18d-127">Daha fazla bilgi için bkz. [Planlamayı En İyi Duruma Getirme belgeleri](https://go.microsoft.com/fwlink/?linkid=2105830).</span><span class="sxs-lookup"><span data-stu-id="4d18d-127">For more information, see [Planning Optimization documentation](https://go.microsoft.com/fwlink/?linkid=2105830).</span></span> <span data-ttu-id="4d18d-128">Dynamics 365 Supply Chain Management'ın şirket içi dağıtımlarına sahip olan müşteriler, 2021 Nisan sonrasında dağıtım senaryoları için Supply Chain Management master planlama altyapısını kullanmaya devam edebilir.</span><span class="sxs-lookup"><span data-stu-id="4d18d-128">Customers with on-premises deployments of Dynamics 365 Supply Chain Management may continue to use the Supply Chain Management master planning engine for distribution scenarios after April 2021.</span></span> <span data-ttu-id="4d18d-129">Ancak, daha fazla özellik geliştirmesi sağlanmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="4d18d-129">However, no more feature enhancements will be provided.</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="4d18d-130">Kaldırılmış veya kullanım dışı bırakılmış özellikler hakkındaki önceki duyurular</span><span class="sxs-lookup"><span data-stu-id="4d18d-130">Previous announcements about removed or deprecated features</span></span>

<span data-ttu-id="4d18d-131">Önceki sürümlerde kaldırılmış veya kaldırılmış özellikler hakkında daha fazla bilgi edinmek için, [önceki sürümlerdeki kaldırılmış veya kaldırılmış özelliklere](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md) bakın.</span><span class="sxs-lookup"><span data-stu-id="4d18d-131">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>
