---
title: Servis siparişlerini birleştir
description: Servis siparişlerini birleştirebilirsiniz.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f2a27e0476ba0b4868d713d87248941dfc3579ff
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202917"
---
# <a name="combine-service-orders"></a><span data-ttu-id="fd8a8-103">Servis siparişlerini birleştir</span><span class="sxs-lookup"><span data-stu-id="fd8a8-103">Combine service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="fd8a8-104">Servis siparişi satırlarını **Servis sözleşmeleri** formunda otomatik olarak oluşturduğunuzda, bunları nasıl gruplandırmak istediğinizi belirtmek için aşağıdaki seçeneklerden birini seçebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="fd8a8-104">When you create service order lines automatically in the **Service agreements** form, you can choose one of the following options to specify how you want to group them:</span></span>

  - <span data-ttu-id="fd8a8-105">**Servis sözleşmesine göre**</span><span class="sxs-lookup"><span data-stu-id="fd8a8-105">**By service agreement**</span></span>

  - <span data-ttu-id="fd8a8-106">**Servis görevine göre**</span><span class="sxs-lookup"><span data-stu-id="fd8a8-106">**By service task**</span></span>

  - <span data-ttu-id="fd8a8-107">**Personele göre**</span><span class="sxs-lookup"><span data-stu-id="fd8a8-107">**By employee**</span></span>

  - <span data-ttu-id="fd8a8-108">**Servis nesnesine göre**</span><span class="sxs-lookup"><span data-stu-id="fd8a8-108">**By service object**</span></span>

## <a name="example"></a><span data-ttu-id="fd8a8-109">Örnek</span><span class="sxs-lookup"><span data-stu-id="fd8a8-109">Example</span></span>

<span data-ttu-id="fd8a8-110">Başlangıç tarihi 31-03-2007 olan bir servis anlaşması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="fd8a8-110">You create a service agreement that has a start date on 03-31-2007.</span></span> <span data-ttu-id="fd8a8-111">**Servis siparişlerini birleştir** alanında, **Servis nesnesine göre**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fd8a8-111">In the **Combine service orders** field, you specify **By service object**.</span></span> <span data-ttu-id="fd8a8-112">Ardından, aşağıdaki servis anlaşması satırlarını oluşturabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="fd8a8-112">You then create the following service agreement lines:</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fd8a8-113">Sözleşme satır numarası</span><span class="sxs-lookup"><span data-stu-id="fd8a8-113">Agreement line number</span></span></p></th>
<th><p><span data-ttu-id="fd8a8-114">Hareket türü</span><span class="sxs-lookup"><span data-stu-id="fd8a8-114">Transaction type</span></span></p></th>
<th><p><span data-ttu-id="fd8a8-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="fd8a8-115">Description</span></span></p></th>
<th><p><span data-ttu-id="fd8a8-116">Aralık</span><span class="sxs-lookup"><span data-stu-id="fd8a8-116">Interval</span></span></p></th>
<th><p><span data-ttu-id="fd8a8-117">Servis nesnesi</span><span class="sxs-lookup"><span data-stu-id="fd8a8-117">Service object</span></span></p></th>
<th><p><span data-ttu-id="fd8a8-118">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="fd8a8-118">Start date</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fd8a8-119">1</span><span class="sxs-lookup"><span data-stu-id="fd8a8-119">1</span></span></p></td>
<td><p><span data-ttu-id="fd8a8-120"><strong>Saat</strong></span><span class="sxs-lookup"><span data-stu-id="fd8a8-120"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="fd8a8-121">SAL1</span><span class="sxs-lookup"><span data-stu-id="fd8a8-121">SAL1</span></span></p></td>
<td><p><span data-ttu-id="fd8a8-122">Haftalık</span><span class="sxs-lookup"><span data-stu-id="fd8a8-122">Weekly</span></span></p></td>
<td><p><span data-ttu-id="fd8a8-123">X-1</span><span class="sxs-lookup"><span data-stu-id="fd8a8-123">X-1</span></span></p></td>
<td><p><span data-ttu-id="fd8a8-124">01-04-2007</span><span class="sxs-lookup"><span data-stu-id="fd8a8-124">04-01-2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd8a8-125">2</span><span class="sxs-lookup"><span data-stu-id="fd8a8-125">2</span></span></p></td>
<td><p><span data-ttu-id="fd8a8-126"><strong>Saat</strong></span><span class="sxs-lookup"><span data-stu-id="fd8a8-126"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="fd8a8-127">SAL2</span><span class="sxs-lookup"><span data-stu-id="fd8a8-127">SAL2</span></span></p></td>
<td><p><span data-ttu-id="fd8a8-128">İki haftalık</span><span class="sxs-lookup"><span data-stu-id="fd8a8-128">Biweekly</span></span></p></td>
<td><p><span data-ttu-id="fd8a8-129">X-2</span><span class="sxs-lookup"><span data-stu-id="fd8a8-129">X-2</span></span></p></td>
<td><p><span data-ttu-id="fd8a8-130">01-04-2007</span><span class="sxs-lookup"><span data-stu-id="fd8a8-130">04-01-2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd8a8-131">3</span><span class="sxs-lookup"><span data-stu-id="fd8a8-131">3</span></span></p></td>
<td><p><span data-ttu-id="fd8a8-132"><strong>Saat</strong></span><span class="sxs-lookup"><span data-stu-id="fd8a8-132"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="fd8a8-133">SAL3</span><span class="sxs-lookup"><span data-stu-id="fd8a8-133">SAL3</span></span></p></td>
<td><p><span data-ttu-id="fd8a8-134">Haftalık</span><span class="sxs-lookup"><span data-stu-id="fd8a8-134">Weekly</span></span></p></td>
<td><p><span data-ttu-id="fd8a8-135">X-2</span><span class="sxs-lookup"><span data-stu-id="fd8a8-135">X-2</span></span></p></td>
<td><p><span data-ttu-id="fd8a8-136">01-04-2007</span><span class="sxs-lookup"><span data-stu-id="fd8a8-136">04-01-2007</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fd8a8-137">Servis anlaşması satırlarından herhangi biri için zaman pencereleri belirtmezsiniz.</span><span class="sxs-lookup"><span data-stu-id="fd8a8-137">You do not specify time windows for any of the service agreement lines.</span></span> <span data-ttu-id="fd8a8-138">Bu nedenle, servis siparişi satırları karşılık geldikleri hesaplanmış günden başka bir güne taşınmaz.</span><span class="sxs-lookup"><span data-stu-id="fd8a8-138">Therefore, the service order lines will not move from the calculated day on which they fall.</span></span>

<span data-ttu-id="fd8a8-139">Daha sonra, servis siparişi satırlarını **Servis siparişleri oluştur** formunda 01-04-2007'den 30-04-2007'ye kadar oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fd8a8-139">Next, you generate service order lines from the **Create service orders** form from 04-01-2007 until 04-30-2007.</span></span>

<span data-ttu-id="fd8a8-140">Toplam olarak 10 servis siparişi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="fd8a8-140">In total, 10 service orders are created.</span></span> <span data-ttu-id="fd8a8-141">Seçtiğiniz birleştirilmiş ayar **Servis nesnesine göre** olduğundan, oluşturulan tüm servis siparişlerinde yalnızca bir özel servis nesnesine sahip servis sipariş satırları bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="fd8a8-141">Because the combined setting that you selected was **By service object**, all service orders that are created have only service order lines with one specific service object.</span></span> <span data-ttu-id="fd8a8-142">Servis anlaşmasından oluşturulan ve aynı servis tarihi ile servis nesnesine sahip olan servis siparişi satırları aynı servis siparişinde birleştirilir.</span><span class="sxs-lookup"><span data-stu-id="fd8a8-142">Service order lines that are generated from the service agreement and have the same service date and object are combined on the same service order.</span></span>


> [!NOTE]
> <P><span data-ttu-id="fd8a8-143">Bu örnekte, <STRONG>Servis yönetimi parametreleri</STRONG> formunda belirtilen takvimde kapalı gün bulunmamaktadır.</span><span class="sxs-lookup"><span data-stu-id="fd8a8-143">In this example, the calendar that is specified in the <STRONG>Service management parameters</STRONG> form has no closed days.</span></span></P>



<span data-ttu-id="fd8a8-144">Servis siparişi satırlarının servis siparişlerine ayrıntılı şekilde gruplandırılması, servis sözleşmesi satırlarında belirttiğiniz zaman aralığına göre gerçekleşmektedir.</span><span class="sxs-lookup"><span data-stu-id="fd8a8-144">Additional grouping of service order lines into service orders occurs according to any time window that you specify on the service agreement lines.</span></span>

## <a name="see-also"></a><span data-ttu-id="fd8a8-145">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="fd8a8-145">See also</span></span>

[<span data-ttu-id="fd8a8-146">Servis siparişlerini otomatik olarak oluşturma</span><span class="sxs-lookup"><span data-stu-id="fd8a8-146">Create service orders automatically</span></span>](create-service-orders-automatically.md)

  


