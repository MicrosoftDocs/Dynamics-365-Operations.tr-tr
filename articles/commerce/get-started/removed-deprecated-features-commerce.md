---
title: Dynamics 365 Commerce'ta kaldırılan veya artık kullanılmayan özellikler
description: Bu konu Dynamics 365 Commerce'dan kaldırılmış veya kaldırılması planlanan özellikleri açıklar.
author: josaw
manager: AnnBe
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: c47c5430a8f5d67e13c95db609a95d5ad66933ae
ms.sourcegitcommit: a8b6cd799eddaf5be9aec9ea3c2b55e2c3231652
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2020
ms.locfileid: "3335288"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a><span data-ttu-id="17ea7-103">Dynamics 365 Commerce'ta kaldırılan veya artık kullanılmayan özellikler</span><span class="sxs-lookup"><span data-stu-id="17ea7-103">Removed or deprecated features in Dynamics 365 Commerce</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17ea7-104">Bu konu Dynamics 365 Commerce'dan kaldırılmış veya kaldırılması planlanan özellikleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="17ea7-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Commerce.</span></span>

- <span data-ttu-id="17ea7-105">*Kaldırılan* özellik artık üründe bulunmaz.</span><span class="sxs-lookup"><span data-stu-id="17ea7-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="17ea7-106">*Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.</span><span class="sxs-lookup"><span data-stu-id="17ea7-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="17ea7-107">Bu liste, kaldırılan veya kullanımına son verilen özellikleri kendi planlamanız için göz önünde bulundurmanız amacıyla hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="17ea7-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="17ea7-108">Finance and Operations uygulamlarındai nesneler hakkında ayrıntılı bilgiye [Teknik referans](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep) raporları altından ulaşabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="17ea7-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="17ea7-109">Finance and Operations uygulamalarının her sürümünde değiştirilen veya kaldırılan nesneler hakkında bilgi edinmek için bu raporların farklı sürümlerini karşılaştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="17ea7-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a><span data-ttu-id="17ea7-110">Commerce 10.0.10 sürümünden kaldırılan veya kullanımı sonlandırılan özellikler</span><span class="sxs-lookup"><span data-stu-id="17ea7-110">Features removed or deprecated in the Commerce 10.0.10 release</span></span>
### <a name="pos-operation-803---picking-and-receiving"></a><span data-ttu-id="17ea7-111">POS işlemi 803 - Malzeme çekme ve teslim alma</span><span class="sxs-lookup"><span data-stu-id="17ea7-111">POS operation 803 - Picking and receiving</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="17ea7-112">**Kullanımı sonlandırma/kaldırma nedeni**</span><span class="sxs-lookup"><span data-stu-id="17ea7-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="17ea7-113">Yeni işlem tasarımı nedeniyle, malzeme çekme ve teslim alma işlemleri kullanımdan kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="17ea7-113">Picking and receiving operations is being deprecated due to new operation redesign.</span></span> |
| <span data-ttu-id="17ea7-114">**Başka bir özellikle mi değiştirildi?**</span><span class="sxs-lookup"><span data-stu-id="17ea7-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="17ea7-115">Evet.</span><span class="sxs-lookup"><span data-stu-id="17ea7-115">Yes.</span></span> <span data-ttu-id="17ea7-116">Bunun yerine iki yeni POS işlemi sunuldu: gelen işlem (804) ve giden işlem (805).</span><span class="sxs-lookup"><span data-stu-id="17ea7-116">It is replaced by two new POS operations: inbound operation (804) and outbound operation (805).</span></span>|
| <span data-ttu-id="17ea7-117">**Etkilenen ürün alanları**</span><span class="sxs-lookup"><span data-stu-id="17ea7-117">**Product areas affected**</span></span>         | <span data-ttu-id="17ea7-118">Satış noktası (POS) uygulaması</span><span class="sxs-lookup"><span data-stu-id="17ea7-118">Point of sale (POS) application</span></span> |
| <span data-ttu-id="17ea7-119">**Dağıtım seçeneği**</span><span class="sxs-lookup"><span data-stu-id="17ea7-119">**Deployment option**</span></span>              | <span data-ttu-id="17ea7-120">Tümü</span><span class="sxs-lookup"><span data-stu-id="17ea7-120">All</span></span> |
| <span data-ttu-id="17ea7-121">**Durum**</span><span class="sxs-lookup"><span data-stu-id="17ea7-121">**Status**</span></span>                         | <span data-ttu-id="17ea7-122">Kullanım dışı: 10.0.10 sürümü itibarıyla, malzeme çekme ve teslim alma işlemi artık yeni özellik güncelleştirmesi almayacak.</span><span class="sxs-lookup"><span data-stu-id="17ea7-122">Deprecated: As of release 10.0.10, the picking and receiving operation will no longer receive any new feature updates.</span></span> <span data-ttu-id="17ea7-123">Gelecekteki sürümlerde bu işlem için yalnızca kritik hata düzeltmeleri yapılacak.</span><span class="sxs-lookup"><span data-stu-id="17ea7-123">Only critical bug fixes will be done for this operation in future releases.</span></span> <span data-ttu-id="17ea7-124">Tüm kullanıcıların, uzun dönemli ürün oyl haritasının bir parçası olmaya devam edecek yeni [Gelen işlemler](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) ve [Giden işlemler](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation) özelliğine geçiş yapması önerilir.</span><span class="sxs-lookup"><span data-stu-id="17ea7-124">All customers are encouraged to move to the new [Inbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) and [Outbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), which will continue to be part of our long-term product roadmap.</span></span> |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a><span data-ttu-id="17ea7-125">Commerce 10.0.7 sürümünden kaldırılan veya kullanım dışı bırakılan özellikler</span><span class="sxs-lookup"><span data-stu-id="17ea7-125">Features removed or deprecated in the Commerce 10.0.7 release</span></span>
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a><span data-ttu-id="17ea7-126">Commerce GetProductAvailabilities ve GetAvailableInventoryNearby API'ları</span><span class="sxs-lookup"><span data-stu-id="17ea7-126">Commerce GetProductAvailabilities and GetAvailableInventoryNearby API's</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="17ea7-127">**Kullanımı sonlandırma/kaldırma nedeni**</span><span class="sxs-lookup"><span data-stu-id="17ea7-127">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="17ea7-128">GetProductAvailabilities ve GetAvailableInventoryNearby API'larının yerini almak üzere yeni optimize edilmiş API'lar oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="17ea7-128">New optimized APIs have been created to replace the GetProductAvailabilities and GetAvailableInventoryNearby APIs.</span></span> |
| <span data-ttu-id="17ea7-129">**Başka bir özellikle mi değiştirildi?**</span><span class="sxs-lookup"><span data-stu-id="17ea7-129">**Replaced by another feature?**</span></span>   | <span data-ttu-id="17ea7-130">Evet: GetEstimatedAvailabilty ve GetEstimatedProductWarehouseAvailability API'ları ile değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="17ea7-130">Yes: It is replaced by GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs.</span></span> |
| <span data-ttu-id="17ea7-131">**Etkilenen ürün alanları**</span><span class="sxs-lookup"><span data-stu-id="17ea7-131">**Product areas affected**</span></span>         | <span data-ttu-id="17ea7-132">e-Ticaret uygulaması SDK</span><span class="sxs-lookup"><span data-stu-id="17ea7-132">e-Commerce application SDK</span></span> |
| <span data-ttu-id="17ea7-133">**Dağıtım seçeneği**</span><span class="sxs-lookup"><span data-stu-id="17ea7-133">**Deployment option**</span></span>              | <span data-ttu-id="17ea7-134">Tümü</span><span class="sxs-lookup"><span data-stu-id="17ea7-134">All</span></span> |
| <span data-ttu-id="17ea7-135">**Durum**</span><span class="sxs-lookup"><span data-stu-id="17ea7-135">**Status**</span></span>                         | <span data-ttu-id="17ea7-136">Kullanım dışı: 10.0.7 sürümü itibarıyla, GetProductAvailabilities ve GetAvailableInventoryNearby için mühendislik yatırımlar yapılmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="17ea7-136">Deprecated: As of release 10.0.7, there will no longer be engineering investments made for GetProductAvailabilities and GetAvailableInventoryNearby.</span></span> <span data-ttu-id="17ea7-137">E-ticaret dağıtımlarında bu API'ları kullanan kuruluşların yeni GetProductAvailabilities ve GetAvailableInventoryNearby API'larına geçiş yapması ve [En iyi duruma getirilmiş ürün kullanılabilirliği hesaplama özelliğini](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels) etkinleştirmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="17ea7-137">Organizations that use these APIs in their e-Commerce deployments should convert to the new GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs and enable the [Optimized product availability calculation feature](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).</span></span>  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="17ea7-138">Kaldırılmış veya kullanım dışı bırakılmış özellikler hakkındaki önceki duyurular</span><span class="sxs-lookup"><span data-stu-id="17ea7-138">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="17ea7-139">Önceki sürümlerde kaldırılmış veya kaldırılmış özellikler hakkında daha fazla bilgi edinmek için, [önceki sürümlerdeki kaldırılmış veya kaldırılmış özelliklere](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json) bakın.</span><span class="sxs-lookup"><span data-stu-id="17ea7-139">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span></span>
