---
title: "Bir üretim ortamındaki standart maliyetleri güncelleştirme"
description: "Bu makale, bir üretim ortamındaki standart maliyetleri güncelleştirme konusunda rehberlik sağlar."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79663
ms.assetid: 3a7c3d13-8dbc-442d-a281-ac0ebe99ec83
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b9ad13071c3e0c3a294e9d4413de160a58559640
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="update-standard-costs-in-a-manufacturing-environment"></a><span data-ttu-id="df14d-103">Bir üretim ortamındaki standart maliyetleri güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="df14d-103">Update standard costs in a manufacturing environment</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="df14d-104">Bu makale, bir üretim ortamındaki standart maliyetleri güncelleştirme konusunda rehberlik sağlar.</span><span class="sxs-lookup"><span data-stu-id="df14d-104">This article provides guidance about how to update standard costs in a manufacturing environment.</span></span> 

<span data-ttu-id="df14d-105">Güncelleştirmeler yeni maddeler, maliyet kategorileri veya dolaylı maliyet hesaplama formüllerini yansıtabilir.</span><span class="sxs-lookup"><span data-stu-id="df14d-105">Updates can reflect new items, cost categories, or indirect cost calculation formulas.</span></span> <span data-ttu-id="df14d-106">Ayrıca, düzeltmeleri ve maliyet değişikliklerini yansıtabilir.</span><span class="sxs-lookup"><span data-stu-id="df14d-106">They can also reflect corrections and cost changes.</span></span> <span data-ttu-id="df14d-107">Güncelleştirme tipi, aşağıdaki durumlarda gösterildiği gibi standart maliyetleri güncelleştirmek için yerine getirmeniz gereken adımları etkiler:</span><span class="sxs-lookup"><span data-stu-id="df14d-107">The type of update affects the steps that you must complete to update standard costs, as illustrated in the following cases:</span></span>

-   <span data-ttu-id="df14d-108">Satın alınan maddeler için beklenen standart maliyet değişikliklerini girin ve madde maliyeti kayıtlarının ilgili tarihteki durumunu **Etkin** olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="df14d-108">Enter expected standard cost changes for purchased items, and then change the status of the item cost records to **Active** on the appropriate date.</span></span> <span data-ttu-id="df14d-109">Ancak satın alınan maddeleri kullanan üretilmiş maddelerin maliyetlerini yeniden hesaplamayın.</span><span class="sxs-lookup"><span data-stu-id="df14d-109">However, don't recalculate the costs of manufactured items that use the purchased items.</span></span>
-   <span data-ttu-id="df14d-110">Yeni satın alınan bir madde için standart maliyetleri girin ancak üretilmiş maddelerin maliyetlerini, yeni satın alınan maddeyi bir bileşen olarak içeren bir ürün reçetesiyle (BOM) yeniden hesaplamayın.</span><span class="sxs-lookup"><span data-stu-id="df14d-110">Enter standard costs for a new purchased item, but don't recalculate the costs of manufactured items that have a bill of materials (BOM) version that contains the new purchased item as a component.</span></span>
-   <span data-ttu-id="df14d-111">Satın alınan bir maddenin maliyetini düzeltin veya değiştirin veya bir satınalma maddesine atanmış maliyet grubunu değiştirin ve tüm üretilmiş maddelerin maliyetini, satın alınan maddeyi bir bileşen olarak içeren bir ürün reçetesi ile hesaplayın.</span><span class="sxs-lookup"><span data-stu-id="df14d-111">Correct or change the cost of a purchased item, or change the cost group that is assigned to a purchased item, and calculate the cost for all manufactured items that have a BOM version that contains the purchased item as a component.</span></span>
-   <span data-ttu-id="df14d-112">Bir maliyet kategorisinin maliyetini değiştirin ve tüm üretilmiş maddelerin maliyetini, maliyet kategorisini kullanan rota faaliyetlerine sahip olan bir rota versiyonuyla hesaplayın.</span><span class="sxs-lookup"><span data-stu-id="df14d-112">Change the cost for a cost category, and calculate the cost for all manufactured items that have a route version that contains routing operations that use the cost category.</span></span>
-   <span data-ttu-id="df14d-113">Rota operasyonlarına atanmış olan maliyet kategorilerini veya maliyet kategorilerine atanmış olan maliyet grubunu değiştirin.</span><span class="sxs-lookup"><span data-stu-id="df14d-113">Change the cost categories that are assigned to routing operations or the cost group that is assigned to cost categories.</span></span> <span data-ttu-id="df14d-114">Daha sonra, maliyet kategorisi kullanan bir rota operasyonuna sahip bir rota versiyonuna sahip tüm üretilmiş maddeler için maliyeti hesaplayın.</span><span class="sxs-lookup"><span data-stu-id="df14d-114">Then calculate the cost for all manufactured items that have a route version that contains routing operations that use the cost category.</span></span>
-   <span data-ttu-id="df14d-115">Dolaylı maliyet hesaplama formülünü değiştirin ve değişiklikten etkilenen tüm üretilmiş maddelerin maliyetini hesaplayın.</span><span class="sxs-lookup"><span data-stu-id="df14d-115">Change an indirect cost calculation formula, and calculate the cost for all manufactured items that are affected by the change.</span></span>
-   <span data-ttu-id="df14d-116">Üretilmiş bir madde için üretim tesisini değiştirin veya ekleyin ve maddenin tesis için üretilmiş maliyetini hesaplayın.</span><span class="sxs-lookup"><span data-stu-id="df14d-116">Change or add a manufacturing site for a manufactured item, and calculate the item's manufactured cost for the site.</span></span>
-   <span data-ttu-id="df14d-117">Üretilmiş bir madde için maliyeti hesaplayın veya yeniden hesaplayın ve tüm üretilmiş maddelerin maliyetini, üretilmiş maddeyi bir bileşen olarak içeren bir ürün reçetesi versiyonuna sahip tüm maddeler için yeniden hesaplayın.</span><span class="sxs-lookup"><span data-stu-id="df14d-117">Calculate, or recalculate, the cost for a manufactured item, and recalculate the cost for all manufactured items that have a BOM version that contains the manufactured item as a component.</span></span>
-   <span data-ttu-id="df14d-118">Yeni üretilmiş maddenin maliyetlerini tanımlı, onaylı ve etkin ürün reçetesi ve rota bilgilerine dayanarak hesaplayın.</span><span class="sxs-lookup"><span data-stu-id="df14d-118">Calculate costs for a new manufactured item, based on its defined, approved, and active BOM and route information.</span></span>

<span data-ttu-id="df14d-119">Her durumda, standart maliyetlerin nasıl güncelleştirileceği dikkatle ele alınmalıdır.</span><span class="sxs-lookup"><span data-stu-id="df14d-119">Each case requires careful consideration about how to update standard costs.</span></span>




