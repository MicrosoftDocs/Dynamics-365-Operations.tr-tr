---
title: Bir proje için satın alma emirleri
description: Bu makalede bir proje için satın alma emirlerinin oluşturulmasında kullanılabilecek çeşitli yöntemler açıklanmıştır. Kullandığınız yöntem, satın alma emrinin amacına, satın alınan maddelerin ne zaman tüketildiğine ve satın alınan maddelerin bir projeye ne zaman şarj edileceğine göre değişir.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4975b9f9e20906fb1259e36a07d8ef3db4f4fee
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174570"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="c1096-104">Bir proje için satın alma emirleri</span><span class="sxs-lookup"><span data-stu-id="c1096-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1096-105">Bu makalede bir proje için satın alma emirlerinin oluşturulmasında kullanılabilecek çeşitli yöntemler açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="c1096-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="c1096-106">Kullandığınız yöntem, satın alma emrinin amacına, satın alınan maddelerin ne zaman tüketildiğine ve satın alınan maddelerin bir projeye ne zaman şarj edileceğine göre değişir.</span><span class="sxs-lookup"><span data-stu-id="c1096-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="c1096-107">Bir satın alma emri oluşturmak için yöntemler</span><span class="sxs-lookup"><span data-stu-id="c1096-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="c1096-108">Proje yönetimi ve hesap işlemlerinde bir satın alma emri oluşturmak için aşağıdaki yöntemlerden birini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c1096-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="c1096-109">Satın alma emrinin amacı, satın alma emrinin ne zaman tamamlanacağını ve buna bağlı olarak maddelerin ne zaman bir projeye gider yazılacağını belirlemektir.</span><span class="sxs-lookup"><span data-stu-id="c1096-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c1096-110">Yöntem</span><span class="sxs-lookup"><span data-stu-id="c1096-110">Method</span></span></th>
<th><span data-ttu-id="c1096-111">Amaç</span><span class="sxs-lookup"><span data-stu-id="c1096-111">Purpose</span></span></th>
<th><span data-ttu-id="c1096-112">Maddelerin tüketimi</span><span class="sxs-lookup"><span data-stu-id="c1096-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c1096-113">Doğrudan bir projeden bir satın alma emri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c1096-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="c1096-114">Bir projede tüketilmek üzere bir harici satıcıdan maddeler satın almak için bu yöntemi kullanın.</span><span class="sxs-lookup"><span data-stu-id="c1096-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="c1096-115">Satın alma emrini iki şekilde oluşturabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="c1096-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="c1096-116">Projenin içinden.</span><span class="sxs-lookup"><span data-stu-id="c1096-116">From the project itself.</span></span> <span data-ttu-id="c1096-117">Bu durumda proje halihazırda satın alma emri için tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="c1096-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="c1096-118">Proje satın alma emrine gelerek.</span><span class="sxs-lookup"><span data-stu-id="c1096-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="c1096-119">Hem satıcıyı hem de satın alma emrinin oluşturulacağı projeyi seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="c1096-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="c1096-120">Maddeler satıcı faturası güncelleştirildiğinde tüketilir.</span><span class="sxs-lookup"><span data-stu-id="c1096-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1096-121">Bir satış siparişinden satınalma siparişi oluşturma.</span><span class="sxs-lookup"><span data-stu-id="c1096-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="c1096-122">Bu yöntemi, maddeleri bir projeden satış siparişi oluşturduğunuzda satın almak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="c1096-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="c1096-123">Maddeler, satış siparişinin faturası müşteriye kesildiğinde tüketilir.</span><span class="sxs-lookup"><span data-stu-id="c1096-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1096-124">Bir madde gereksiniminden satınalma siparişi oluşturma.</span><span class="sxs-lookup"><span data-stu-id="c1096-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="c1096-125">Bu yöntemi, maddeleri bir projeden bir madde gereksinimi oluşturduğunuzda satın almak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="c1096-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="c1096-126">Maddeler, madde gereksinimi sevk irsaliyesi güncelleştirildiğinde tüketilir.</span><span class="sxs-lookup"><span data-stu-id="c1096-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="c1096-127">Satıcı faturasını veya sevk irsaliyesini güncelleştirdiğinizde, sizden madde gereksinimindeki sevk irsaliyesini güncelleştirmeniz istenir.</span><span class="sxs-lookup"><span data-stu-id="c1096-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="c1096-128">Daha fazla bilgi için bkz. [Bir madde talebinden maddeleri bir satınama siparişinden teslim alma](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="c1096-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>

