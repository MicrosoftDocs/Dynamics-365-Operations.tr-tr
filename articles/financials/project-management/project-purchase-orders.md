---
title: "Bir proje için satın alma emirleri"
description: "Bu makalede bir proje için satın alma emirlerinin oluşturulmasında kullanılabilecek çeşitli yöntemler açıklanmıştır. Kullandığınız yöntem, satın alma emrinin amacına, satın alınan maddelerin ne zaman tüketildiğine ve satın alınan maddelerin bir projeye ne zaman şarj edileceğine göre değişir."
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: dae65394a2180ccbf3317a41b635ba97034e541b
ms.contentlocale: tr-tr
ms.lasthandoff: 03/26/2018

---

# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="95af3-104">Bir proje için satın alma emirleri</span><span class="sxs-lookup"><span data-stu-id="95af3-104">Purchase orders for a project</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="95af3-105">Bu makalede bir proje için satın alma emirlerinin oluşturulmasında kullanılabilecek çeşitli yöntemler açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="95af3-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="95af3-106">Kullandığınız yöntem, satın alma emrinin amacına, satın alınan maddelerin ne zaman tüketildiğine ve satın alınan maddelerin bir projeye ne zaman şarj edileceğine göre değişir.</span><span class="sxs-lookup"><span data-stu-id="95af3-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

<span data-ttu-id="95af3-107">Microsoft Dynamics 365 for Finance and Operations'ta bir proje için satınalma siparişleri oluşturmak amacıyla birden fazla yöntem kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="95af3-107">In Microsoft Dynamics 365 for Finance and Operations, you can use multiple methods to create purchase orders for a project.</span></span> <span data-ttu-id="95af3-108">Kullandığınız yöntem, satın alma emrinin amacına, satın alınan maddelerin ne zaman tüketildiğine ve satın alınan maddelerin bir projeye ne zaman şarj edileceğine göre değişir.</span><span class="sxs-lookup"><span data-stu-id="95af3-108">The method that you use depends on the purpose of the purchase order, when the purchased items are consumed, and when the purchased items are charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="95af3-109">Bir satın alma emri oluşturmak için yöntemler</span><span class="sxs-lookup"><span data-stu-id="95af3-109">Methods for creating a purchase order</span></span>

<span data-ttu-id="95af3-110">Proje yönetimi ve hesap işlemlerinde bir satın alma emri oluşturmak için aşağıdaki yöntemlerden birini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="95af3-110">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="95af3-111">Satın alma emrinin amacı, satın alma emrinin ne zaman tamamlanacağını ve buna bağlı olarak maddelerin ne zaman bir projeye gider yazılacağını belirlemektir.</span><span class="sxs-lookup"><span data-stu-id="95af3-111">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="95af3-112">Yöntem</span><span class="sxs-lookup"><span data-stu-id="95af3-112">Method</span></span></th>
<th><span data-ttu-id="95af3-113">Amaç</span><span class="sxs-lookup"><span data-stu-id="95af3-113">Purpose</span></span></th>
<th><span data-ttu-id="95af3-114">Maddelerin tüketimi</span><span class="sxs-lookup"><span data-stu-id="95af3-114">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="95af3-115">Doğrudan bir projeden bir satın alma emri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="95af3-115">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="95af3-116">Bir projede tüketilmek üzere bir harici satıcıdan maddeler satın almak için bu yöntemi kullanın.</span><span class="sxs-lookup"><span data-stu-id="95af3-116">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="95af3-117">Satın alma emrini iki şekilde oluşturabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="95af3-117">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="95af3-118">Projenin içinden.</span><span class="sxs-lookup"><span data-stu-id="95af3-118">From the project itself.</span></span> <span data-ttu-id="95af3-119">Bu durumda proje halihazırda satın alma emri için tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="95af3-119">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="95af3-120">Proje satın alma emrine gelerek.</span><span class="sxs-lookup"><span data-stu-id="95af3-120">By navigating to the project purchase order.</span></span> <span data-ttu-id="95af3-121">Hem satıcıyı hem de satın alma emrinin oluşturulacağı projeyi seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="95af3-121">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="95af3-122">Maddeler satıcı faturası güncelleştirildiğinde tüketilir.</span><span class="sxs-lookup"><span data-stu-id="95af3-122">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="95af3-123">Bir satış siparişinden satınalma siparişi oluşturma.</span><span class="sxs-lookup"><span data-stu-id="95af3-123">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="95af3-124">Bu yöntemi, maddeleri bir projeden satış siparişi oluşturduğunuzda satın almak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="95af3-124">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="95af3-125">Maddeler, satış siparişinin faturası müşteriye kesildiğinde tüketilir.</span><span class="sxs-lookup"><span data-stu-id="95af3-125">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="95af3-126">Bir madde gereksiniminden satınalma siparişi oluşturma.</span><span class="sxs-lookup"><span data-stu-id="95af3-126">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="95af3-127">Bu yöntemi, maddeleri bir projeden bir madde gereksinimi oluşturduğunuzda satın almak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="95af3-127">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="95af3-128">Maddeler, madde gereksinimi sevk irsaliyesi güncelleştirildiğinde tüketilir.</span><span class="sxs-lookup"><span data-stu-id="95af3-128">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="95af3-129">Satıcı faturasını veya sevk irsaliyesini güncelleştirdiğinizde, sizden madde gereksinimindeki sevk irsaliyesini güncelleştirmeniz istenir.</span><span class="sxs-lookup"><span data-stu-id="95af3-129">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="95af3-130">Daha fazla bilgi için bkz. [Bir madde talebinden maddeleri bir satınama siparişinden teslim alma](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="95af3-130">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>


