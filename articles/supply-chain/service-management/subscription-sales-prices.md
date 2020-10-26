---
title: Abonelik satış fiyatı
description: Abonelik oluşturduğunuzda, satış fiyatı Satış fiyatı (abonelik) formunda oluşturulmuş olan satış fiyatı ayarından türetilir.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f03efbbca4fc9da76c6ead7566457beb79c8c249
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985877"
---
# <a name="subscription-sales-prices"></a><span data-ttu-id="166db-103">Abonelik satış fiyatı</span><span class="sxs-lookup"><span data-stu-id="166db-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="166db-104">Abonelik oluşturduğunuzda, satış fiyatı **Satış fiyatı (abonelik)** formunda oluşturulmuş olan satış fiyatı ayarından türetilir.</span><span class="sxs-lookup"><span data-stu-id="166db-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="166db-105">**Satış fiyatı (abonelik)** formunda belirli bir abonelik için satış fiyatları oluşturabileceğiniz gibi, daha geniş bir uygulama alanı olan satış fiyatları da oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="166db-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="166db-106">Satış fiyatının aboneliğe uygulanması için, abonelikle satış fiyatının dönem kodu dönem koduyla ve para birimi satış fiyatı para birimiyle aynı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="166db-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="166db-107">Aboneliğin ve satış fiyatının dönem kodu ve para birimi aynıysa, abonelik satış fiyatları aşağıdaki tabloda listelenen öncelikler temel alınarak seçilir.</span><span class="sxs-lookup"><span data-stu-id="166db-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="166db-108">Tablodaki boş hücre alanın boş olduğunu ve X işareti de değerin hareketin oluşturulduğu abonelikteki değerle aynı olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="166db-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

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
<th><p><span data-ttu-id="166db-109">Öncelik </span><span class="sxs-lookup"><span data-stu-id="166db-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="166db-110"><strong>Kategori</strong></span><span class="sxs-lookup"><span data-stu-id="166db-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="166db-111"><strong>Proje kodu</strong></span><span class="sxs-lookup"><span data-stu-id="166db-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="166db-112"><strong>Abonelik</strong></span><span class="sxs-lookup"><span data-stu-id="166db-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="166db-113"><strong>Satış para birimi</strong></span><span class="sxs-lookup"><span data-stu-id="166db-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="166db-114"><strong>Dönem kodu</strong></span><span class="sxs-lookup"><span data-stu-id="166db-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="166db-115">1</span><span class="sxs-lookup"><span data-stu-id="166db-115">1</span></span></p></td>
<td><p><span data-ttu-id="166db-116">X</span><span class="sxs-lookup"><span data-stu-id="166db-116">X</span></span></p></td>
<td><p><span data-ttu-id="166db-117">X</span><span class="sxs-lookup"><span data-stu-id="166db-117">X</span></span></p></td>
<td><p><span data-ttu-id="166db-118">X</span><span class="sxs-lookup"><span data-stu-id="166db-118">X</span></span></p></td>
<td><p><span data-ttu-id="166db-119">X</span><span class="sxs-lookup"><span data-stu-id="166db-119">X</span></span></p></td>
<td><p><span data-ttu-id="166db-120">X</span><span class="sxs-lookup"><span data-stu-id="166db-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="166db-121">2</span><span class="sxs-lookup"><span data-stu-id="166db-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="166db-122">X</span><span class="sxs-lookup"><span data-stu-id="166db-122">X</span></span></p></td>
<td><p><span data-ttu-id="166db-123">X</span><span class="sxs-lookup"><span data-stu-id="166db-123">X</span></span></p></td>
<td><p><span data-ttu-id="166db-124">X</span><span class="sxs-lookup"><span data-stu-id="166db-124">X</span></span></p></td>
<td><p><span data-ttu-id="166db-125">X</span><span class="sxs-lookup"><span data-stu-id="166db-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="166db-126">3</span><span class="sxs-lookup"><span data-stu-id="166db-126">3</span></span></p></td>
<td><p><span data-ttu-id="166db-127">X</span><span class="sxs-lookup"><span data-stu-id="166db-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="166db-128">X</span><span class="sxs-lookup"><span data-stu-id="166db-128">X</span></span></p></td>
<td><p><span data-ttu-id="166db-129">X</span><span class="sxs-lookup"><span data-stu-id="166db-129">X</span></span></p></td>
<td><p><span data-ttu-id="166db-130">X</span><span class="sxs-lookup"><span data-stu-id="166db-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="166db-131">4</span><span class="sxs-lookup"><span data-stu-id="166db-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="166db-132">X</span><span class="sxs-lookup"><span data-stu-id="166db-132">X</span></span></p></td>
<td><p><span data-ttu-id="166db-133">X</span><span class="sxs-lookup"><span data-stu-id="166db-133">X</span></span></p></td>
<td><p><span data-ttu-id="166db-134">X</span><span class="sxs-lookup"><span data-stu-id="166db-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="166db-135">5</span><span class="sxs-lookup"><span data-stu-id="166db-135">5</span></span></p></td>
<td><p><span data-ttu-id="166db-136">X</span><span class="sxs-lookup"><span data-stu-id="166db-136">X</span></span></p></td>
<td><p><span data-ttu-id="166db-137">X</span><span class="sxs-lookup"><span data-stu-id="166db-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="166db-138">X</span><span class="sxs-lookup"><span data-stu-id="166db-138">X</span></span></p></td>
<td><p><span data-ttu-id="166db-139">X</span><span class="sxs-lookup"><span data-stu-id="166db-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="166db-140">6</span><span class="sxs-lookup"><span data-stu-id="166db-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="166db-141">X</span><span class="sxs-lookup"><span data-stu-id="166db-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="166db-142">X</span><span class="sxs-lookup"><span data-stu-id="166db-142">X</span></span></p></td>
<td><p><span data-ttu-id="166db-143">X</span><span class="sxs-lookup"><span data-stu-id="166db-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="166db-144">7</span><span class="sxs-lookup"><span data-stu-id="166db-144">7</span></span></p></td>
<td><p><span data-ttu-id="166db-145">X</span><span class="sxs-lookup"><span data-stu-id="166db-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="166db-146">X</span><span class="sxs-lookup"><span data-stu-id="166db-146">X</span></span></p></td>
<td><p><span data-ttu-id="166db-147">X</span><span class="sxs-lookup"><span data-stu-id="166db-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="166db-148">8</span><span class="sxs-lookup"><span data-stu-id="166db-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="166db-149">X</span><span class="sxs-lookup"><span data-stu-id="166db-149">X</span></span></p></td>
<td><p><span data-ttu-id="166db-150">X</span><span class="sxs-lookup"><span data-stu-id="166db-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="166db-151">Abonelik ücreti oluşturulduğunda, abonelik satış fiyatı olarak en yüksek ayrıntı düzeyine sahip satış fiyatı (yukarıdaki tabloda belirtildiği gibi) seçilir.</span><span class="sxs-lookup"><span data-stu-id="166db-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="166db-152">Abonelik satış fiyatlarını güncelleştirme ve dizine alma</span><span class="sxs-lookup"><span data-stu-id="166db-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="166db-153">Taban fiyatı veya dizini güncelleştirerek abonelik satış fiyatını güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="166db-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="166db-154">Güncelleştirme işlemini belirli bir yüzdeyle veya yeni bir değerle gerçekleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="166db-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="166db-155">Abonelik ücreti satış fiyatları</span><span class="sxs-lookup"><span data-stu-id="166db-155">Subscription fee sales prices</span></span>

<span data-ttu-id="166db-156">Abonelik ücreti oluşturulurken, satış fiyatında aboneliğin satış fiyatı ayarı temel alınır.</span><span class="sxs-lookup"><span data-stu-id="166db-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="166db-157">Abonelik fiyatı ayarındaki taban fiyatını kullanabileceğiniz gibi, endekslenen satış fiyatları da oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="166db-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="166db-158">Örnek</span><span class="sxs-lookup"><span data-stu-id="166db-158">Example</span></span>

<span data-ttu-id="166db-159">Yeni 9030 projesi için 500 Euro abonelik satış fiyatları ayarlamak istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="166db-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="166db-160">**Satış fiyatı (abonelik)** formunda, aşağıdaki tabloda gösterildiği şekilde bir abonelik satış fiyatı satırı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="166db-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="166db-161">Geçerlilik başlangıcı</span><span class="sxs-lookup"><span data-stu-id="166db-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="166db-162">Kategori</span><span class="sxs-lookup"><span data-stu-id="166db-162">Category</span></span></p></th>
<th><p><span data-ttu-id="166db-163">Proje</span><span class="sxs-lookup"><span data-stu-id="166db-163">Project</span></span></p></th>
<th><p><span data-ttu-id="166db-164">Abonelik</span><span class="sxs-lookup"><span data-stu-id="166db-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="166db-165">Dönem kodu</span><span class="sxs-lookup"><span data-stu-id="166db-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="166db-166">Satış para birimi</span><span class="sxs-lookup"><span data-stu-id="166db-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="166db-167">Satış fiyatı</span><span class="sxs-lookup"><span data-stu-id="166db-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="166db-168">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="166db-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="166db-169">9030</span><span class="sxs-lookup"><span data-stu-id="166db-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="166db-170">Ay</span><span class="sxs-lookup"><span data-stu-id="166db-170">Month</span></span></p></td>
<td><p><span data-ttu-id="166db-171">Euro</span><span class="sxs-lookup"><span data-stu-id="166db-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="166db-172">500</span><span class="sxs-lookup"><span data-stu-id="166db-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="166db-173">**Kategori** ve **Abonelik** alanlarının boş bırakıldığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="166db-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="166db-174">Şimdi aşağıdaki abonelikleri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="166db-174">You then create the following subscriptions.</span></span>

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
<th><p><span data-ttu-id="166db-175">Servis aboneliği</span><span class="sxs-lookup"><span data-stu-id="166db-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="166db-176">Proje</span><span class="sxs-lookup"><span data-stu-id="166db-176">Project</span></span></p></th>
<th><p><span data-ttu-id="166db-177">Abonelik grubu</span><span class="sxs-lookup"><span data-stu-id="166db-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="166db-178">Kategori</span><span class="sxs-lookup"><span data-stu-id="166db-178">Category</span></span></p></th>
<th><p><span data-ttu-id="166db-179">Para birimi</span><span class="sxs-lookup"><span data-stu-id="166db-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="166db-180">Dönem kodu</span><span class="sxs-lookup"><span data-stu-id="166db-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="166db-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="166db-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="166db-182">9030</span><span class="sxs-lookup"><span data-stu-id="166db-182">9030</span></span></p></td>
<td><p><span data-ttu-id="166db-183">Abo1</span><span class="sxs-lookup"><span data-stu-id="166db-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="166db-184">AboKat1</span><span class="sxs-lookup"><span data-stu-id="166db-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="166db-185">Euro</span><span class="sxs-lookup"><span data-stu-id="166db-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="166db-186">Aylık</span><span class="sxs-lookup"><span data-stu-id="166db-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="166db-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="166db-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="166db-188">9030</span><span class="sxs-lookup"><span data-stu-id="166db-188">9030</span></span></p></td>
<td><p><span data-ttu-id="166db-189">Abo1</span><span class="sxs-lookup"><span data-stu-id="166db-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="166db-190">AboKat2</span><span class="sxs-lookup"><span data-stu-id="166db-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="166db-191">Euro</span><span class="sxs-lookup"><span data-stu-id="166db-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="166db-192">Aylık</span><span class="sxs-lookup"><span data-stu-id="166db-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="166db-193">Şimdi Abo1 abonelik grubundaki her iki abonelik için de abonelik ücretlerini oluşturursunuz:</span><span class="sxs-lookup"><span data-stu-id="166db-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="166db-194">**Hizmet yönetimi** \> **Kurulum** \> **Servis abonelikleri** \> **Abonelik grupları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="166db-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="166db-195">**Abonelik grupları** formunda **İşlev** \> **Abonelik ücreti oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="166db-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="166db-196">**Abonelik ücreti oluştur** formuna, uygun bilgileri girin.</span><span class="sxs-lookup"><span data-stu-id="166db-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="166db-197">Daha fazla bilgi için bkz. [Abonelik ücreti hareketleri oluşturma](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="166db-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="166db-198">500 EUR değerindeki satış fiyatına sahip bir abonelik ücreti her iki abonelik için aşağıdaki tabloda gösterildiği şekilde oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="166db-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="166db-199">Proje tarihi</span><span class="sxs-lookup"><span data-stu-id="166db-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="166db-200">Servis aboneliği</span><span class="sxs-lookup"><span data-stu-id="166db-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="166db-201">Proje</span><span class="sxs-lookup"><span data-stu-id="166db-201">Project</span></span></p></th>
<th><p><span data-ttu-id="166db-202">Kategori</span><span class="sxs-lookup"><span data-stu-id="166db-202">Category</span></span></p></th>
<th><p><span data-ttu-id="166db-203">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="166db-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="166db-204">Bitiş tarihi</span><span class="sxs-lookup"><span data-stu-id="166db-204">End date</span></span></p></th>
<th><p><span data-ttu-id="166db-205">Satış para birimi</span><span class="sxs-lookup"><span data-stu-id="166db-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="166db-206">Satış fiyatı</span><span class="sxs-lookup"><span data-stu-id="166db-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="166db-207">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="166db-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="166db-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="166db-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="166db-209">9030</span><span class="sxs-lookup"><span data-stu-id="166db-209">9030</span></span></p></td>
<td><p><span data-ttu-id="166db-210">AboKat1</span><span class="sxs-lookup"><span data-stu-id="166db-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="166db-211">01-01-2007</span><span class="sxs-lookup"><span data-stu-id="166db-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="166db-212">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="166db-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="166db-213">Euro</span><span class="sxs-lookup"><span data-stu-id="166db-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="166db-214">500</span><span class="sxs-lookup"><span data-stu-id="166db-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="166db-215">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="166db-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="166db-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="166db-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="166db-217">9030</span><span class="sxs-lookup"><span data-stu-id="166db-217">9030</span></span></p></td>
<td><p><span data-ttu-id="166db-218">AboKat2</span><span class="sxs-lookup"><span data-stu-id="166db-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="166db-219">01-01-2007</span><span class="sxs-lookup"><span data-stu-id="166db-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="166db-220">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="166db-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="166db-221">Euro</span><span class="sxs-lookup"><span data-stu-id="166db-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="166db-222">500</span><span class="sxs-lookup"><span data-stu-id="166db-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="166db-223">Daha sonra, 9030 projesinin AboKat1 kategorisi için satış fiyatları belirlemek istediğinize karar verdiniz diyelim.</span><span class="sxs-lookup"><span data-stu-id="166db-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="166db-224">Bu nedenle, 9030 projesi ve SubCat1 ücret kategorisi birleşimi için satış fiyatı 550 Euro olan yeni bir satış fiyatı satırı oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="166db-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="166db-225">Artık 9030 projesinin aşağıdaki tabloda gösterildiği şekilde iki abonelik satış fiyatı satırı vardır:</span><span class="sxs-lookup"><span data-stu-id="166db-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="166db-226">Geçerlilik başlangıcı</span><span class="sxs-lookup"><span data-stu-id="166db-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="166db-227">Kategori</span><span class="sxs-lookup"><span data-stu-id="166db-227">Category</span></span></p></th>
<th><p><span data-ttu-id="166db-228">Proje</span><span class="sxs-lookup"><span data-stu-id="166db-228">Project</span></span></p></th>
<th><p><span data-ttu-id="166db-229">Abonelik</span><span class="sxs-lookup"><span data-stu-id="166db-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="166db-230">Dönem kodu</span><span class="sxs-lookup"><span data-stu-id="166db-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="166db-231">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="166db-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="166db-232">Satış fiyatı</span><span class="sxs-lookup"><span data-stu-id="166db-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="166db-233">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="166db-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="166db-234">9030</span><span class="sxs-lookup"><span data-stu-id="166db-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="166db-235">Ay</span><span class="sxs-lookup"><span data-stu-id="166db-235">Month</span></span></p></td>
<td><p><span data-ttu-id="166db-236">Euro</span><span class="sxs-lookup"><span data-stu-id="166db-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="166db-237">500</span><span class="sxs-lookup"><span data-stu-id="166db-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="166db-238">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="166db-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="166db-239">AboKat1</span><span class="sxs-lookup"><span data-stu-id="166db-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="166db-240">9030</span><span class="sxs-lookup"><span data-stu-id="166db-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="166db-241">Ay</span><span class="sxs-lookup"><span data-stu-id="166db-241">Month</span></span></p></td>
<td><p><span data-ttu-id="166db-242">Euro</span><span class="sxs-lookup"><span data-stu-id="166db-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="166db-243">550</span><span class="sxs-lookup"><span data-stu-id="166db-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="166db-244">Abo1 abonelik grubundaki her iki aboneliğin abonelik ücretlerini oluşturmak için yukarıda açıklanan prosedürü tekrarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="166db-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="166db-245">Aşağıdaki tabloda abonelik grubuna eklenmiş her abonelik her abonelik için oluşturulan hareketler gösterilir.</span><span class="sxs-lookup"><span data-stu-id="166db-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

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
<th><p><span data-ttu-id="166db-246">Proje tarihi</span><span class="sxs-lookup"><span data-stu-id="166db-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="166db-247">Abonelik</span><span class="sxs-lookup"><span data-stu-id="166db-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="166db-248">Proje</span><span class="sxs-lookup"><span data-stu-id="166db-248">Project</span></span></p></th>
<th><p><span data-ttu-id="166db-249">Kategori</span><span class="sxs-lookup"><span data-stu-id="166db-249">Category</span></span></p></th>
<th><p><span data-ttu-id="166db-250">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="166db-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="166db-251">Bitiş tarihi</span><span class="sxs-lookup"><span data-stu-id="166db-251">End date</span></span></p></th>
<th><p><span data-ttu-id="166db-252">Satış para birimi</span><span class="sxs-lookup"><span data-stu-id="166db-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="166db-253">Satış fiyatı</span><span class="sxs-lookup"><span data-stu-id="166db-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="166db-254">28-07-2007</span><span class="sxs-lookup"><span data-stu-id="166db-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="166db-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="166db-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="166db-256">9030</span><span class="sxs-lookup"><span data-stu-id="166db-256">9030</span></span></p></td>
<td><p><span data-ttu-id="166db-257">AboKat1</span><span class="sxs-lookup"><span data-stu-id="166db-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="166db-258">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="166db-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="166db-259">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="166db-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="166db-260">Euro</span><span class="sxs-lookup"><span data-stu-id="166db-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="166db-261">550</span><span class="sxs-lookup"><span data-stu-id="166db-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="166db-262">28-07-2008</span><span class="sxs-lookup"><span data-stu-id="166db-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="166db-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="166db-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="166db-264">9030</span><span class="sxs-lookup"><span data-stu-id="166db-264">9030</span></span></p></td>
<td><p><span data-ttu-id="166db-265">AboKat2</span><span class="sxs-lookup"><span data-stu-id="166db-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="166db-266">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="166db-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="166db-267">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="166db-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="166db-268">Euro</span><span class="sxs-lookup"><span data-stu-id="166db-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="166db-269">500</span><span class="sxs-lookup"><span data-stu-id="166db-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="166db-270">00020\_135 aboneliği için olan ilk harekette, belirtilen proje ve kategori birleşimine ayarlanan abonelik satış fiyatından 550 Euro satış fiyatı türetilir.</span><span class="sxs-lookup"><span data-stu-id="166db-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="166db-271">00021\_135 aboneliği için olan ikinci harekette, 9030 projesi ve SubCat2 kategorisi birleşimi için fiyat ayarı bulunmadığından, projenin abonelik satış fiyatı olarak 500 Euro satış fiyatı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="166db-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="166db-272">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="166db-272">See also</span></span>

[<span data-ttu-id="166db-273">Abonelik satış fiyatlarını güncelleştirme ve dizine alma</span><span class="sxs-lookup"><span data-stu-id="166db-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  


