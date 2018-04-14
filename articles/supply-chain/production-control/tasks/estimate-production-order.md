---
title: "Üretim emrini tahmin etme"
description: "USMF demo veri şirketi veya kendi veri kümenizi kullanarak, bu yordamı çalıştırabilirsiniz."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 454ecd9bfa19a2486610d9a412057f42ae2d68a2
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---
# <a name="estimate-a-production-order"></a><span data-ttu-id="e5417-103">Üretim emrini tahmin etme</span><span class="sxs-lookup"><span data-stu-id="e5417-103">Estimate a production order</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e5417-104">USMF demo veri şirketi veya kendi veri kümenizi kullanarak, bu yordamı çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e5417-104">You can run this procedure by using the USMF demo data company or your own data set.</span></span> <span data-ttu-id="e5417-105">Her iki durumda da, Oluşturulmuş statüsünde olan açık bir üretim emrine sahip olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e5417-105">In both cases, you need to have an open production order that has the Created status.</span></span> <span data-ttu-id="e5417-106">Bu, üretim emri ömrünü açıklayan yedi yordamdan ikincisidir.</span><span class="sxs-lookup"><span data-stu-id="e5417-106">This is the second procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="estimate-a-production-order"></a><span data-ttu-id="e5417-107">Üretim emrini tahmin etme</span><span class="sxs-lookup"><span data-stu-id="e5417-107">Estimate a production order</span></span>
1. <span data-ttu-id="e5417-108">Üretim denetimi > Üretim emirleri > Tüm üretim emirleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e5417-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="e5417-109">Kılavuzda Oluşturulmuş durumunda olan bir siparişi seçin.</span><span class="sxs-lookup"><span data-stu-id="e5417-109">Select an order that has the Created status in the grid.</span></span>
3. <span data-ttu-id="e5417-110">Eylem Bölmesinde, Üretim emri öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e5417-110">On the Action Pane, click Production order.</span></span>
4. <span data-ttu-id="e5417-111">Tahmin seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e5417-111">Click Estimate.</span></span>
    * <span data-ttu-id="e5417-112">Bu adımda, tek bir üretim emrinin tahmini maliyetleri hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="e5417-112">In this step, the estimated costs of a single production order is calculated.</span></span>   
5. <span data-ttu-id="e5417-113">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e5417-113">Click OK.</span></span>

## <a name="view-the-calculation-details"></a><span data-ttu-id="e5417-114">Hesaplama ayrıntılarını görüntüleyin</span><span class="sxs-lookup"><span data-stu-id="e5417-114">View the calculation details</span></span>
1. <span data-ttu-id="e5417-115">Eylem Bölmesi'nde, Maliyetleri yönet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e5417-115">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="e5417-116">Hesaplama ayrıntılarını görüntüle seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e5417-116">Click View calculation details.</span></span>
    * <span data-ttu-id="e5417-117">Bu sayfayı maliyet dökümünü görüntüler.</span><span class="sxs-lookup"><span data-stu-id="e5417-117">This page displays the cost breakdown.</span></span> <span data-ttu-id="e5417-118">Örneğin, ilk satırın bitmiş ürünü için birim başına toplam maliyet fiyatı görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e5417-118">For example, you can view the total cost price per unit for the finished product in the first row.</span></span> <span data-ttu-id="e5417-119">Sonraki satırlar, ürün reçetesi, üretim rotası ve dolaylı maliyetlere göre olan maliyetleri içerir.</span><span class="sxs-lookup"><span data-stu-id="e5417-119">The subsequent rows contain costs according to the bill of materials, production route, and indirect costs.</span></span>  

