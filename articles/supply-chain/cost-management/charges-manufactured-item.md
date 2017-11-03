---
title: "Üretilen bir madde için giderleri görüntüleme"
description: "Üretilen bir ürünün sabit maliyetleri, operasyon hazırlık sürelerini ve sabit miktara veya sabit hurda tutarına sahip bileşeni yansıtır."
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 274483
ms.assetid: 6f5b851b-c5a7-43ef-b380-0d316667c1ef
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: fe766a2969e647500452ecb64040d2157a155416
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="display-charges-for-a-manufactured-item"></a><span data-ttu-id="a8f4a-103">Üretilen bir madde için giderleri görüntüleme</span><span class="sxs-lookup"><span data-stu-id="a8f4a-103">Display charges for a manufactured item</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a8f4a-104">Üretilen bir ürünün sabit maliyetleri, operasyon hazırlık sürelerini ve sabit miktara veya sabit hurda tutarına sahip bileşeni yansıtır.</span><span class="sxs-lookup"><span data-stu-id="a8f4a-104">The constant costs of a manufactured item reflect the operation setup times and the components that have a constant quantity or a constant scrap amount.</span></span>

<span data-ttu-id="a8f4a-105">Maddenin giderlerinin hesaplanan tutarı, maddenin birim maliyeti ile görüntülenebilir.</span><span class="sxs-lookup"><span data-stu-id="a8f4a-105">The calculated amount of an item's charges can be displayed with the item's unit costs.</span></span> <span data-ttu-id="a8f4a-106">Ancak, masraflar bazen ayrı alanlar olarak görüntülenir ve maddenin birim maliyetlerine eklenmemiştir.</span><span class="sxs-lookup"><span data-stu-id="a8f4a-106">However, the charges are sometimes displayed as separate fields, and they are not included in the item's unit costs.</span></span> <span data-ttu-id="a8f4a-107">Değişiklikler ayrı alanlar olarak görüntülendiğinde, bir alan toplam giderleri gösterir, diğer alan tutarı amorti etmekte kullanılan maliyetli lot miktarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a8f4a-107">When the charges appear as separate fields, one field displays the total amount of charges, and another field displays the costing lot size that is used to amortize the amount.</span></span> <span data-ttu-id="a8f4a-108">Örneğin, madde fiyat sayfası, giderleri iki farklı alan olarak gösterir.</span><span class="sxs-lookup"><span data-stu-id="a8f4a-108">The Item price page, for example, displays the charges as two separate fields.</span></span> <span data-ttu-id="a8f4a-109">Ancak, Tüm sayfa, maddenin birim başına maliyetini ve birim maliyetlerine dahil edilen amorti edilmiş maliyetleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="a8f4a-109">However, the Complete page displays the item's total cost per unit, and the amortized costs are included in the unit costs.</span></span>

<span data-ttu-id="a8f4a-110">Üretilen bir maddeye ilişkin giderler standart maliyetler için maddenin birim maliyetine her zaman dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="a8f4a-110">The charges for a manufactured item are always included in the item's unit cost for standard cost purposes.</span></span> <span data-ttu-id="a8f4a-111">Planlanan maliyetler için bu giderler isteğe bağlı olarak dahil edilebilir.</span><span class="sxs-lookup"><span data-stu-id="a8f4a-111">They can optionally be included for planned cost purposes.</span></span> <span data-ttu-id="a8f4a-112">Maliyet versiyonundaki bir ilke, üretilen bir maddenin maliyetine giderlerin dahil edilmesini zorunlu kılar.</span><span class="sxs-lookup"><span data-stu-id="a8f4a-112">A policy in the costing version enforces the inclusion of charges in the cost of a manufactured item.</span></span> <span data-ttu-id="a8f4a-113">Bir maddenin maliyet kaydını etkinleştirdiğinizde, Madde fiyatı sayfasında görüntülenen, maddenin taban maliyet bilgileri için giderleri güncelleştirirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a8f4a-113">When you activate an item's cost record, you update the charges for the item's base cost information, which is displayed in the Item price page.</span></span> <span data-ttu-id="a8f4a-114">Giderler iki ayrı alanda gösterilir ve maddenin birim fiyatına dahil değildirler.</span><span class="sxs-lookup"><span data-stu-id="a8f4a-114">The charges are displayed as two separate fields, and they are not included in the item's unit cost.</span></span> <span data-ttu-id="a8f4a-115">Etkinleştirme farklı tesisleri yansıtsa da her etkinleştirme maddenin taban maliyet bilgilerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a8f4a-115">Each activation updates the item's base cost information, even if the activation reflects different sites.</span></span> <span data-ttu-id="a8f4a-116">Bu nedenle, taban maliyet bilgisini bir referans bilgisi olarak görüntülemelisiniz.</span><span class="sxs-lookup"><span data-stu-id="a8f4a-116">Therefore, you should view the base cost information as reference information.</span></span>






