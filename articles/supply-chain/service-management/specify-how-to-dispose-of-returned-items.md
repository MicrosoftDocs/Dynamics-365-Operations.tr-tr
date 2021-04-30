---
title: İade edilen maddelerin nasıl elden çıkarılacağını belirtme
description: İade edilen maddelerin nasıl elden çıkarılacağını belirtin.
author: ShylaThompson
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c827df81621346733953dc77e16e269f8c3767a8
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910125"
---
# <a name="specify-how-to-dispose-of-returned-items"></a><span data-ttu-id="b0b06-103">İade edilen maddelerin nasıl elden çıkarılacağını belirtme</span><span class="sxs-lookup"><span data-stu-id="b0b06-103">Specify how to dispose of returned items</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b0b06-104">Bir iade siparişini işlerken, ürünün neden iade edildiğini tanımlamak için bir iade neden kodu belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b0b06-104">When you handle a return order, you must specify a reason return code to identify why the product is being returned.</span></span> <span data-ttu-id="b0b06-105">Bir elden çıkarma kodu ve iade edilen ürün ile birlikte ne yapılması gerektiğini belirlemek için bir elden çıkarma eylemi de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b0b06-105">You must also specify a disposition code and a disposition action to determine what should be done with the returned product itself.</span></span>

<span data-ttu-id="b0b06-106">Elden çıkarma kodu, iade siparişini oluşturduğunuzda, madde varışını kaydettiğinizde veya madde varışında sevk irsaliyesi güncelleştirmesi yaptığınızda ve bir karantina emrini bitirdiğinizde geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="b0b06-106">A disposition code can be applied when you create the return order, register item arrival or packing-slip update an item arrival, and end a quarantine order.</span></span>

<span data-ttu-id="b0b06-107">İş süreçlerini desteklemek için gereken herhangi bir elden çıkarma kodunu tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b0b06-107">You can define any disposition codes that you need in order to support the business processes.</span></span> <span data-ttu-id="b0b06-108">Aşağıdaki tabloda iade edilen maddeyi elden çıkarma atamak için genellikle kullanılan kodlar sağlanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="b0b06-108">The following table provides a set of typically used codes to assign return-item disposition.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b0b06-109">Elden Çıkarma türü</span><span class="sxs-lookup"><span data-stu-id="b0b06-109">Disposition type</span></span></p></th>
<th><p><span data-ttu-id="b0b06-110">Genel kod</span><span class="sxs-lookup"><span data-stu-id="b0b06-110">Common code</span></span></p></th>
<th><p><span data-ttu-id="b0b06-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="b0b06-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b0b06-112">Elden çıkarma</span><span class="sxs-lookup"><span data-stu-id="b0b06-112">Disposal</span></span></p></td>
<td><p><span data-ttu-id="b0b06-113">SC</span><span class="sxs-lookup"><span data-stu-id="b0b06-113">SC</span></span></p></td>
<td><p><span data-ttu-id="b0b06-114">Hurdaya Ayır/İmha Et</span><span class="sxs-lookup"><span data-stu-id="b0b06-114">Scrap/Destroy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0b06-115">Elden çıkarma</span><span class="sxs-lookup"><span data-stu-id="b0b06-115">Disposal</span></span></p></td>
<td><p><span data-ttu-id="b0b06-116">DC</span><span class="sxs-lookup"><span data-stu-id="b0b06-116">DC</span></span></p></td>
<td><p><span data-ttu-id="b0b06-117">Hayır Kurumuna Bağışla</span><span class="sxs-lookup"><span data-stu-id="b0b06-117">Donate to Charity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0b06-118">Elden çıkarma</span><span class="sxs-lookup"><span data-stu-id="b0b06-118">Disposal</span></span></p></td>
<td><p><span data-ttu-id="b0b06-119">TD</span><span class="sxs-lookup"><span data-stu-id="b0b06-119">TD</span></span></p></td>
<td><p><span data-ttu-id="b0b06-120">Üçüncü Taraf Elden Çıkarma</span><span class="sxs-lookup"><span data-stu-id="b0b06-120">Third-Party Disposal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0b06-121">Elden çıkarma</span><span class="sxs-lookup"><span data-stu-id="b0b06-121">Disposal</span></span></p></td>
<td><p><span data-ttu-id="b0b06-122">SL</span><span class="sxs-lookup"><span data-stu-id="b0b06-122">SL</span></span></p></td>
<td><p><span data-ttu-id="b0b06-123">Kurtar</span><span class="sxs-lookup"><span data-stu-id="b0b06-123">Salvage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0b06-124">Elden çıkarma</span><span class="sxs-lookup"><span data-stu-id="b0b06-124">Disposal</span></span></p></td>
<td><p><span data-ttu-id="b0b06-125">TS</span><span class="sxs-lookup"><span data-stu-id="b0b06-125">TS</span></span></p></td>
<td><p><span data-ttu-id="b0b06-126">Üçüncü Taraf Satışı (İkincil Piyasalar)</span><span class="sxs-lookup"><span data-stu-id="b0b06-126">Third-Party Sale (Secondary Markets)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0b06-127">Onarım/Değiştirme</span><span class="sxs-lookup"><span data-stu-id="b0b06-127">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="b0b06-128">RW</span><span class="sxs-lookup"><span data-stu-id="b0b06-128">RW</span></span></p></td>
<td><p><span data-ttu-id="b0b06-129">Yeniden İşle</span><span class="sxs-lookup"><span data-stu-id="b0b06-129">Rework</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0b06-130">Onarım/Değiştirme</span><span class="sxs-lookup"><span data-stu-id="b0b06-130">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="b0b06-131">RF</span><span class="sxs-lookup"><span data-stu-id="b0b06-131">RF</span></span></p></td>
<td><p><span data-ttu-id="b0b06-132">Yeniden Üret/Yeniden Sağla</span><span class="sxs-lookup"><span data-stu-id="b0b06-132">Remanufacture/Refurbish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0b06-133">Onarım/Değiştirme</span><span class="sxs-lookup"><span data-stu-id="b0b06-133">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="b0b06-134">MD</span><span class="sxs-lookup"><span data-stu-id="b0b06-134">MD</span></span></p></td>
<td><p><span data-ttu-id="b0b06-135">Değişiklik Yap</span><span class="sxs-lookup"><span data-stu-id="b0b06-135">Modify</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0b06-136">Onarım/Değiştirme</span><span class="sxs-lookup"><span data-stu-id="b0b06-136">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="b0b06-137">RP</span><span class="sxs-lookup"><span data-stu-id="b0b06-137">RP</span></span></p></td>
<td><p><span data-ttu-id="b0b06-138">Onar</span><span class="sxs-lookup"><span data-stu-id="b0b06-138">Repair</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0b06-139">Onarım/Değiştirme</span><span class="sxs-lookup"><span data-stu-id="b0b06-139">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="b0b06-140">RV</span><span class="sxs-lookup"><span data-stu-id="b0b06-140">RV</span></span></p></td>
<td><p><span data-ttu-id="b0b06-141">Satıcıya İade Et</span><span class="sxs-lookup"><span data-stu-id="b0b06-141">Return to Vendor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0b06-142">Diğer</span><span class="sxs-lookup"><span data-stu-id="b0b06-142">Other</span></span></p></td>
<td><p><span data-ttu-id="b0b06-143">AI</span><span class="sxs-lookup"><span data-stu-id="b0b06-143">AI</span></span></p></td>
<td><p><span data-ttu-id="b0b06-144">Olduğu gibi kullan</span><span class="sxs-lookup"><span data-stu-id="b0b06-144">Use as is</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0b06-145">Diğer</span><span class="sxs-lookup"><span data-stu-id="b0b06-145">Other</span></span></p></td>
<td><p><span data-ttu-id="b0b06-146">RS</span><span class="sxs-lookup"><span data-stu-id="b0b06-146">RS</span></span></p></td>
<td><p><span data-ttu-id="b0b06-147">Yeniden sat</span><span class="sxs-lookup"><span data-stu-id="b0b06-147">Resale</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0b06-148">Diğer</span><span class="sxs-lookup"><span data-stu-id="b0b06-148">Other</span></span></p></td>
<td><p><span data-ttu-id="b0b06-149">EX</span><span class="sxs-lookup"><span data-stu-id="b0b06-149">EX</span></span></p></td>
<td><p><span data-ttu-id="b0b06-150">Döviz</span><span class="sxs-lookup"><span data-stu-id="b0b06-150">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0b06-151">Diğer</span><span class="sxs-lookup"><span data-stu-id="b0b06-151">Other</span></span></p></td>
<td><p><span data-ttu-id="b0b06-152">MS</span><span class="sxs-lookup"><span data-stu-id="b0b06-152">MS</span></span></p></td>
<td><p><span data-ttu-id="b0b06-153">Çeşitli</span><span class="sxs-lookup"><span data-stu-id="b0b06-153">Miscellaneous</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b0b06-154">Tanımladığınız her elden çıkarma kodu için bir elden çıkarma eylemi seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b0b06-154">For each disposition code that you define, you must select a disposition action.</span></span> <span data-ttu-id="b0b06-155">Elden çıkarma eylemi elden çıkarma kodlarının fiziksel ve mali etkilerini belirler.</span><span class="sxs-lookup"><span data-stu-id="b0b06-155">The disposition action determines the physical and financial implications of the disposition codes.</span></span> <span data-ttu-id="b0b06-156">Örneğin, elden çıkarma eylemi iade edilen maddenin fiziksel olarak işlenme şeklini, iade edilen ürünün mali etkisini ve müşteriye bir değiştirme maddesi gönderilip gönderilmeyeceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="b0b06-156">For example, the disposition action determines the physical handling of the returned item, the financial effect of the returned item, and if a replacement item must be sent to the customer.</span></span> <span data-ttu-id="b0b06-157">İş gereksinimlerinize göre sınırsız sayıda elden çıkarma kodu tanımlayabilirsiniz, ancak arasından seçim yapabileceğiniz yalnızca altı önceden tanımlanmış değerlendirme eylemi bulunur.</span><span class="sxs-lookup"><span data-stu-id="b0b06-157">You can define an unlimited number of disposition codes according to your business needs, but there are only six predefined disposition actions that you can select from.</span></span> <span data-ttu-id="b0b06-158">Aşağıdaki tabloda değerlendirme eylemleri ve tanımlamaları verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="b0b06-158">The following table provides the disposition actions and their definitions.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b0b06-159">Elden çıkarma eylemi</span><span class="sxs-lookup"><span data-stu-id="b0b06-159">Disposition action</span></span></p></th>
<th><p><span data-ttu-id="b0b06-160">Tanım</span><span class="sxs-lookup"><span data-stu-id="b0b06-160">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b0b06-161"><strong>Alacak</strong></span><span class="sxs-lookup"><span data-stu-id="b0b06-161"><strong>Credit</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b06-162">Maddeyi stoğa iade edin ve müşteriyi alacaklandırın.</span><span class="sxs-lookup"><span data-stu-id="b0b06-162">Return the item to inventory and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0b06-163"><strong>Yalnızca alacaklandır</strong></span><span class="sxs-lookup"><span data-stu-id="b0b06-163"><strong>Credit only</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b06-164">Maddenin iade edilmesini talep etmeden veya beklemeden müşteriyi alacaklandırın.</span><span class="sxs-lookup"><span data-stu-id="b0b06-164">Credit the customer without requiring or expecting the item to be returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0b06-165"><strong>Hurda</strong></span><span class="sxs-lookup"><span data-stu-id="b0b06-165"><strong>Scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b06-166">Maddeyi hurdaya çıkarın ve müşteriyi alacaklandırın.</span><span class="sxs-lookup"><span data-stu-id="b0b06-166">Scrap the item and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0b06-167"><strong>Değiştir ve alacaklandır</strong></span><span class="sxs-lookup"><span data-stu-id="b0b06-167"><strong>Replace and credit</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b06-168">Maddeyi stoğa iade edin, değişiklik siparişi oluşturun ve müşteriyi alacaklandırın.</span><span class="sxs-lookup"><span data-stu-id="b0b06-168">Return the item to inventory, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0b06-169"><strong>Değiştir ve ıskartaya ayır</strong></span><span class="sxs-lookup"><span data-stu-id="b0b06-169"><strong>Replace and scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b06-170">Maddeyi hurdaya çıkarın, değişiklik siparişi oluşturun ve müşteriyi alacaklandırın.</span><span class="sxs-lookup"><span data-stu-id="b0b06-170">Scrap the item, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0b06-171"><strong>Müşteriye iade et</strong></span><span class="sxs-lookup"><span data-stu-id="b0b06-171"><strong>Return to customer</strong></span></span></p></td>
<td><p><span data-ttu-id="b0b06-172">İade edilen ürünü reddedin ve müşteriye iade edin.</span><span class="sxs-lookup"><span data-stu-id="b0b06-172">Reject the returned item and return it to the customer.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="select-a-disposition-code-for-a-quarantine-order"></a><span data-ttu-id="b0b06-173">Bir karantina emri için elden çıkarma kodu seçme</span><span class="sxs-lookup"><span data-stu-id="b0b06-173">Select a disposition code for a quarantine order</span></span>

1.  <span data-ttu-id="b0b06-174">**Stok yönetimi** \> **Periyodik** \> **Kalite yönetimi** \> **Karantina emirleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b0b06-174">Click **Inventory management** \> **Periodic** \> **Quality management** \> **Quarantine orders**.</span></span>

2.  <span data-ttu-id="b0b06-175">Mevcut bir karantina emri için **Genel bakış** sekmesindeki **Elden çıkarma kodu** alanından bir eylem seçin.</span><span class="sxs-lookup"><span data-stu-id="b0b06-175">For an existing quarantine order, select an action from the **Disposition code** field on the **Overview** tab.</span></span>



## <a name="see-also"></a><span data-ttu-id="b0b06-176">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="b0b06-176">See also</span></span>

[<span data-ttu-id="b0b06-177">Karantina siparişi (form)</span><span class="sxs-lookup"><span data-stu-id="b0b06-177">Quarantine order (form)</span></span>](/dynamicsax-2012//quarantine-order-form)

<span data-ttu-id="b0b06-178">[Elden çıkarma kodları (form)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="b0b06-178">[Disposition codes (form)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]