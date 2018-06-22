---
title: "Azaltma günleri örneği"
description: "Azaltma günleri örneği."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 69e4b1b0fe100b17e5b2c59be81604019347956f
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---


# <a name="reduction-days-example"></a><span data-ttu-id="10249-103">Azaltma günleri örneği</span><span class="sxs-lookup"><span data-stu-id="10249-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="10249-104">Bir müşterinin bakım aboneliği için aşağıda açıklandığı şekilde bir abonelik hareketi oluşturdunuz.</span><span class="sxs-lookup"><span data-stu-id="10249-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="10249-105">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="10249-105">From date</span></span></p></th>
<th><p><span data-ttu-id="10249-106">Bitiş tarihi</span><span class="sxs-lookup"><span data-stu-id="10249-106">To date</span></span></p></th>
<th><p><span data-ttu-id="10249-107">Abonelik</span><span class="sxs-lookup"><span data-stu-id="10249-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="10249-108">Abonelik türü</span><span class="sxs-lookup"><span data-stu-id="10249-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="10249-109">Proje</span><span class="sxs-lookup"><span data-stu-id="10249-109">Project</span></span></p></th>
<th><p><span data-ttu-id="10249-110">Kategori</span><span class="sxs-lookup"><span data-stu-id="10249-110">Category</span></span></p></th>
<th><p><span data-ttu-id="10249-111">Satış para birimi</span><span class="sxs-lookup"><span data-stu-id="10249-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="10249-112">Satış fiyatı</span><span class="sxs-lookup"><span data-stu-id="10249-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10249-113">01 Mart 2011</span><span class="sxs-lookup"><span data-stu-id="10249-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="10249-114">31 Mart 2011</span><span class="sxs-lookup"><span data-stu-id="10249-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="10249-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="10249-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="10249-116"><strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="10249-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="10249-117">9013</span><span class="sxs-lookup"><span data-stu-id="10249-117">9013</span></span></p></td>
<td><p><span data-ttu-id="10249-118">AboKat2</span><span class="sxs-lookup"><span data-stu-id="10249-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="10249-119">Euro</span><span class="sxs-lookup"><span data-stu-id="10249-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="10249-120">200,00</span><span class="sxs-lookup"><span data-stu-id="10249-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="10249-121">Müşteri, iki gün için (19 ve 11 Mart) servis karşılama ihtiyacı olmadığını bildiriyor.</span><span class="sxs-lookup"><span data-stu-id="10249-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="10249-122">Abonelikten bu iki günü düşmeyi kabul ediyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="10249-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="10249-123">Aşağıdaki tabloda açıklandığı gibi **Azaltma günleri** türünde yeni bir işlem oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="10249-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="10249-124">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="10249-124">From date</span></span></p></th>
<th><p><span data-ttu-id="10249-125">Bitiş tarihi</span><span class="sxs-lookup"><span data-stu-id="10249-125">To date</span></span></p></th>
<th><p><span data-ttu-id="10249-126">Abonelik</span><span class="sxs-lookup"><span data-stu-id="10249-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="10249-127">Abonelik türü</span><span class="sxs-lookup"><span data-stu-id="10249-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="10249-128">Proje</span><span class="sxs-lookup"><span data-stu-id="10249-128">Project</span></span></p></th>
<th><p><span data-ttu-id="10249-129">Kategori</span><span class="sxs-lookup"><span data-stu-id="10249-129">Category</span></span></p></th>
<th><p><span data-ttu-id="10249-130">Satış para birimi</span><span class="sxs-lookup"><span data-stu-id="10249-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="10249-131">Satış fiyatı</span><span class="sxs-lookup"><span data-stu-id="10249-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10249-132">10 Mart 2011</span><span class="sxs-lookup"><span data-stu-id="10249-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="10249-133">11 Mart 2011</span><span class="sxs-lookup"><span data-stu-id="10249-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="10249-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="10249-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="10249-135"><strong>İndirim günleri</strong></span><span class="sxs-lookup"><span data-stu-id="10249-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="10249-136">9013</span><span class="sxs-lookup"><span data-stu-id="10249-136">9013</span></span></p></td>
<td><p><span data-ttu-id="10249-137">AboKat2</span><span class="sxs-lookup"><span data-stu-id="10249-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="10249-138">Euro</span><span class="sxs-lookup"><span data-stu-id="10249-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="10249-139">-12,90</span><span class="sxs-lookup"><span data-stu-id="10249-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="10249-140">Mart 2011'e ait işlemler faturalandırıldığında, 200 EUR değerindeki satış fiyatından 12,90 EUR düşülür.</span><span class="sxs-lookup"><span data-stu-id="10249-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="10249-141">Abonelik işlemi için borçlandırılabilir tutar bu durumda 187,10 EUR olur ve iki işlem toplam 187,10 EUR olarak faturalandırılır.</span><span class="sxs-lookup"><span data-stu-id="10249-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="10249-142">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="10249-142">See also</span></span>

[<span data-ttu-id="10249-143">Abonelik ücretlerindeki günleri azaltma</span><span class="sxs-lookup"><span data-stu-id="10249-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  


