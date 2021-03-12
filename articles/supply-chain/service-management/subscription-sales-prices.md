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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 35f4e3f3bdbdad7a48b89bad7da96d221f09bdb4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974241"
---
# <a name="subscription-sales-prices"></a><span data-ttu-id="0d526-103">Abonelik satış fiyatı</span><span class="sxs-lookup"><span data-stu-id="0d526-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="0d526-104">Abonelik oluşturduğunuzda, satış fiyatı **Satış fiyatı (abonelik)** formunda oluşturulmuş olan satış fiyatı ayarından türetilir.</span><span class="sxs-lookup"><span data-stu-id="0d526-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="0d526-105">**Satış fiyatı (abonelik)** formunda belirli bir abonelik için satış fiyatları oluşturabileceğiniz gibi, daha geniş bir uygulama alanı olan satış fiyatları da oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0d526-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="0d526-106">Satış fiyatının aboneliğe uygulanması için, abonelikle satış fiyatının dönem kodu dönem koduyla ve para birimi satış fiyatı para birimiyle aynı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0d526-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="0d526-107">Aboneliğin ve satış fiyatının dönem kodu ve para birimi aynıysa, abonelik satış fiyatları aşağıdaki tabloda listelenen öncelikler temel alınarak seçilir.</span><span class="sxs-lookup"><span data-stu-id="0d526-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="0d526-108">Tablodaki boş hücre alanın boş olduğunu ve X işareti de değerin hareketin oluşturulduğu abonelikteki değerle aynı olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="0d526-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

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
<th><p><span data-ttu-id="0d526-109">Öncelik </span><span class="sxs-lookup"><span data-stu-id="0d526-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="0d526-110"><strong>Kategori</strong></span><span class="sxs-lookup"><span data-stu-id="0d526-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="0d526-111"><strong>Proje kodu</strong></span><span class="sxs-lookup"><span data-stu-id="0d526-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="0d526-112"><strong>Abonelik</strong></span><span class="sxs-lookup"><span data-stu-id="0d526-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="0d526-113"><strong>Satış para birimi</strong></span><span class="sxs-lookup"><span data-stu-id="0d526-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="0d526-114"><strong>Dönem kodu</strong></span><span class="sxs-lookup"><span data-stu-id="0d526-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0d526-115">1</span><span class="sxs-lookup"><span data-stu-id="0d526-115">1</span></span></p></td>
<td><p><span data-ttu-id="0d526-116">X</span><span class="sxs-lookup"><span data-stu-id="0d526-116">X</span></span></p></td>
<td><p><span data-ttu-id="0d526-117">X</span><span class="sxs-lookup"><span data-stu-id="0d526-117">X</span></span></p></td>
<td><p><span data-ttu-id="0d526-118">X</span><span class="sxs-lookup"><span data-stu-id="0d526-118">X</span></span></p></td>
<td><p><span data-ttu-id="0d526-119">X</span><span class="sxs-lookup"><span data-stu-id="0d526-119">X</span></span></p></td>
<td><p><span data-ttu-id="0d526-120">X</span><span class="sxs-lookup"><span data-stu-id="0d526-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d526-121">2</span><span class="sxs-lookup"><span data-stu-id="0d526-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0d526-122">X</span><span class="sxs-lookup"><span data-stu-id="0d526-122">X</span></span></p></td>
<td><p><span data-ttu-id="0d526-123">X</span><span class="sxs-lookup"><span data-stu-id="0d526-123">X</span></span></p></td>
<td><p><span data-ttu-id="0d526-124">X</span><span class="sxs-lookup"><span data-stu-id="0d526-124">X</span></span></p></td>
<td><p><span data-ttu-id="0d526-125">X</span><span class="sxs-lookup"><span data-stu-id="0d526-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d526-126">3</span><span class="sxs-lookup"><span data-stu-id="0d526-126">3</span></span></p></td>
<td><p><span data-ttu-id="0d526-127">X</span><span class="sxs-lookup"><span data-stu-id="0d526-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0d526-128">X</span><span class="sxs-lookup"><span data-stu-id="0d526-128">X</span></span></p></td>
<td><p><span data-ttu-id="0d526-129">X</span><span class="sxs-lookup"><span data-stu-id="0d526-129">X</span></span></p></td>
<td><p><span data-ttu-id="0d526-130">X</span><span class="sxs-lookup"><span data-stu-id="0d526-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d526-131">4</span><span class="sxs-lookup"><span data-stu-id="0d526-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0d526-132">X</span><span class="sxs-lookup"><span data-stu-id="0d526-132">X</span></span></p></td>
<td><p><span data-ttu-id="0d526-133">X</span><span class="sxs-lookup"><span data-stu-id="0d526-133">X</span></span></p></td>
<td><p><span data-ttu-id="0d526-134">X</span><span class="sxs-lookup"><span data-stu-id="0d526-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d526-135">5</span><span class="sxs-lookup"><span data-stu-id="0d526-135">5</span></span></p></td>
<td><p><span data-ttu-id="0d526-136">X</span><span class="sxs-lookup"><span data-stu-id="0d526-136">X</span></span></p></td>
<td><p><span data-ttu-id="0d526-137">X</span><span class="sxs-lookup"><span data-stu-id="0d526-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0d526-138">X</span><span class="sxs-lookup"><span data-stu-id="0d526-138">X</span></span></p></td>
<td><p><span data-ttu-id="0d526-139">X</span><span class="sxs-lookup"><span data-stu-id="0d526-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d526-140">6</span><span class="sxs-lookup"><span data-stu-id="0d526-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0d526-141">X</span><span class="sxs-lookup"><span data-stu-id="0d526-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0d526-142">X</span><span class="sxs-lookup"><span data-stu-id="0d526-142">X</span></span></p></td>
<td><p><span data-ttu-id="0d526-143">X</span><span class="sxs-lookup"><span data-stu-id="0d526-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d526-144">7</span><span class="sxs-lookup"><span data-stu-id="0d526-144">7</span></span></p></td>
<td><p><span data-ttu-id="0d526-145">X</span><span class="sxs-lookup"><span data-stu-id="0d526-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0d526-146">X</span><span class="sxs-lookup"><span data-stu-id="0d526-146">X</span></span></p></td>
<td><p><span data-ttu-id="0d526-147">X</span><span class="sxs-lookup"><span data-stu-id="0d526-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d526-148">8</span><span class="sxs-lookup"><span data-stu-id="0d526-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="0d526-149">X</span><span class="sxs-lookup"><span data-stu-id="0d526-149">X</span></span></p></td>
<td><p><span data-ttu-id="0d526-150">X</span><span class="sxs-lookup"><span data-stu-id="0d526-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0d526-151">Abonelik ücreti oluşturulduğunda, abonelik satış fiyatı olarak en yüksek ayrıntı düzeyine sahip satış fiyatı (yukarıdaki tabloda belirtildiği gibi) seçilir.</span><span class="sxs-lookup"><span data-stu-id="0d526-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="0d526-152">Abonelik satış fiyatlarını güncelleştirme ve dizine alma</span><span class="sxs-lookup"><span data-stu-id="0d526-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="0d526-153">Taban fiyatı veya dizini güncelleştirerek abonelik satış fiyatını güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0d526-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="0d526-154">Güncelleştirme işlemini belirli bir yüzdeyle veya yeni bir değerle gerçekleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0d526-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="0d526-155">Abonelik ücreti satış fiyatları</span><span class="sxs-lookup"><span data-stu-id="0d526-155">Subscription fee sales prices</span></span>

<span data-ttu-id="0d526-156">Abonelik ücreti oluşturulurken, satış fiyatında aboneliğin satış fiyatı ayarı temel alınır.</span><span class="sxs-lookup"><span data-stu-id="0d526-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="0d526-157">Abonelik fiyatı ayarındaki taban fiyatını kullanabileceğiniz gibi, endekslenen satış fiyatları da oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0d526-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="0d526-158">Örnek</span><span class="sxs-lookup"><span data-stu-id="0d526-158">Example</span></span>

<span data-ttu-id="0d526-159">Yeni 9030 projesi için 500 Euro abonelik satış fiyatları ayarlamak istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="0d526-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="0d526-160">**Satış fiyatı (abonelik)** formunda, aşağıdaki tabloda gösterildiği şekilde bir abonelik satış fiyatı satırı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0d526-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

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
<th><p><span data-ttu-id="0d526-161">Geçerlilik başlangıcı</span><span class="sxs-lookup"><span data-stu-id="0d526-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="0d526-162">Kategori</span><span class="sxs-lookup"><span data-stu-id="0d526-162">Category</span></span></p></th>
<th><p><span data-ttu-id="0d526-163">Proje</span><span class="sxs-lookup"><span data-stu-id="0d526-163">Project</span></span></p></th>
<th><p><span data-ttu-id="0d526-164">Abonelik</span><span class="sxs-lookup"><span data-stu-id="0d526-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="0d526-165">Dönem kodu</span><span class="sxs-lookup"><span data-stu-id="0d526-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="0d526-166">Satış para birimi</span><span class="sxs-lookup"><span data-stu-id="0d526-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="0d526-167">Satış fiyatı</span><span class="sxs-lookup"><span data-stu-id="0d526-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0d526-168">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="0d526-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0d526-169">9030</span><span class="sxs-lookup"><span data-stu-id="0d526-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0d526-170">Ay</span><span class="sxs-lookup"><span data-stu-id="0d526-170">Month</span></span></p></td>
<td><p><span data-ttu-id="0d526-171">Euro</span><span class="sxs-lookup"><span data-stu-id="0d526-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="0d526-172">500</span><span class="sxs-lookup"><span data-stu-id="0d526-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0d526-173">**Kategori** ve **Abonelik** alanlarının boş bırakıldığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="0d526-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="0d526-174">Şimdi aşağıdaki abonelikleri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0d526-174">You then create the following subscriptions.</span></span>

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
<th><p><span data-ttu-id="0d526-175">Servis aboneliği</span><span class="sxs-lookup"><span data-stu-id="0d526-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="0d526-176">Proje</span><span class="sxs-lookup"><span data-stu-id="0d526-176">Project</span></span></p></th>
<th><p><span data-ttu-id="0d526-177">Abonelik grubu</span><span class="sxs-lookup"><span data-stu-id="0d526-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="0d526-178">Kategori</span><span class="sxs-lookup"><span data-stu-id="0d526-178">Category</span></span></p></th>
<th><p><span data-ttu-id="0d526-179">Para birimi</span><span class="sxs-lookup"><span data-stu-id="0d526-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="0d526-180">Dönem kodu</span><span class="sxs-lookup"><span data-stu-id="0d526-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0d526-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="0d526-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="0d526-182">9030</span><span class="sxs-lookup"><span data-stu-id="0d526-182">9030</span></span></p></td>
<td><p><span data-ttu-id="0d526-183">Abo1</span><span class="sxs-lookup"><span data-stu-id="0d526-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="0d526-184">AboKat1</span><span class="sxs-lookup"><span data-stu-id="0d526-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="0d526-185">Euro</span><span class="sxs-lookup"><span data-stu-id="0d526-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="0d526-186">Aylık</span><span class="sxs-lookup"><span data-stu-id="0d526-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d526-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="0d526-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="0d526-188">9030</span><span class="sxs-lookup"><span data-stu-id="0d526-188">9030</span></span></p></td>
<td><p><span data-ttu-id="0d526-189">Abo1</span><span class="sxs-lookup"><span data-stu-id="0d526-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="0d526-190">AboKat2</span><span class="sxs-lookup"><span data-stu-id="0d526-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="0d526-191">Euro</span><span class="sxs-lookup"><span data-stu-id="0d526-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="0d526-192">Aylık</span><span class="sxs-lookup"><span data-stu-id="0d526-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0d526-193">Şimdi Abo1 abonelik grubundaki her iki abonelik için de abonelik ücretlerini oluşturursunuz:</span><span class="sxs-lookup"><span data-stu-id="0d526-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="0d526-194">**Hizmet yönetimi** \> **Kurulum** \> **Servis abonelikleri** \> **Abonelik grupları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0d526-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="0d526-195">**Abonelik grupları** formunda **İşlev** \> **Abonelik ücreti oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0d526-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="0d526-196">**Abonelik ücreti oluştur** formuna, uygun bilgileri girin.</span><span class="sxs-lookup"><span data-stu-id="0d526-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="0d526-197">Daha fazla bilgi için bkz. [Abonelik ücreti hareketleri oluşturma](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="0d526-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="0d526-198">500 EUR değerindeki satış fiyatına sahip bir abonelik ücreti her iki abonelik için aşağıdaki tabloda gösterildiği şekilde oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="0d526-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="0d526-199">Proje tarihi</span><span class="sxs-lookup"><span data-stu-id="0d526-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="0d526-200">Servis aboneliği</span><span class="sxs-lookup"><span data-stu-id="0d526-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="0d526-201">Proje</span><span class="sxs-lookup"><span data-stu-id="0d526-201">Project</span></span></p></th>
<th><p><span data-ttu-id="0d526-202">Kategori</span><span class="sxs-lookup"><span data-stu-id="0d526-202">Category</span></span></p></th>
<th><p><span data-ttu-id="0d526-203">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="0d526-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="0d526-204">Bitiş tarihi</span><span class="sxs-lookup"><span data-stu-id="0d526-204">End date</span></span></p></th>
<th><p><span data-ttu-id="0d526-205">Satış para birimi</span><span class="sxs-lookup"><span data-stu-id="0d526-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="0d526-206">Satış fiyatı</span><span class="sxs-lookup"><span data-stu-id="0d526-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0d526-207">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="0d526-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="0d526-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="0d526-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="0d526-209">9030</span><span class="sxs-lookup"><span data-stu-id="0d526-209">9030</span></span></p></td>
<td><p><span data-ttu-id="0d526-210">AboKat1</span><span class="sxs-lookup"><span data-stu-id="0d526-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="0d526-211">01-01-2007</span><span class="sxs-lookup"><span data-stu-id="0d526-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="0d526-212">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="0d526-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="0d526-213">Euro</span><span class="sxs-lookup"><span data-stu-id="0d526-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="0d526-214">500</span><span class="sxs-lookup"><span data-stu-id="0d526-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d526-215">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="0d526-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="0d526-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="0d526-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="0d526-217">9030</span><span class="sxs-lookup"><span data-stu-id="0d526-217">9030</span></span></p></td>
<td><p><span data-ttu-id="0d526-218">AboKat2</span><span class="sxs-lookup"><span data-stu-id="0d526-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="0d526-219">01-01-2007</span><span class="sxs-lookup"><span data-stu-id="0d526-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="0d526-220">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="0d526-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="0d526-221">Euro</span><span class="sxs-lookup"><span data-stu-id="0d526-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="0d526-222">500</span><span class="sxs-lookup"><span data-stu-id="0d526-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0d526-223">Daha sonra, 9030 projesinin AboKat1 kategorisi için satış fiyatları belirlemek istediğinize karar verdiniz diyelim.</span><span class="sxs-lookup"><span data-stu-id="0d526-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="0d526-224">Bu nedenle, 9030 projesi ve SubCat1 ücret kategorisi birleşimi için satış fiyatı 550 Euro olan yeni bir satış fiyatı satırı oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="0d526-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="0d526-225">Artık 9030 projesinin aşağıdaki tabloda gösterildiği şekilde iki abonelik satış fiyatı satırı vardır:</span><span class="sxs-lookup"><span data-stu-id="0d526-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="0d526-226">Geçerlilik başlangıcı</span><span class="sxs-lookup"><span data-stu-id="0d526-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="0d526-227">Kategori</span><span class="sxs-lookup"><span data-stu-id="0d526-227">Category</span></span></p></th>
<th><p><span data-ttu-id="0d526-228">Proje</span><span class="sxs-lookup"><span data-stu-id="0d526-228">Project</span></span></p></th>
<th><p><span data-ttu-id="0d526-229">Abonelik</span><span class="sxs-lookup"><span data-stu-id="0d526-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="0d526-230">Dönem kodu</span><span class="sxs-lookup"><span data-stu-id="0d526-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="0d526-231">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="0d526-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="0d526-232">Satış fiyatı</span><span class="sxs-lookup"><span data-stu-id="0d526-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0d526-233">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="0d526-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0d526-234">9030</span><span class="sxs-lookup"><span data-stu-id="0d526-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0d526-235">Ay</span><span class="sxs-lookup"><span data-stu-id="0d526-235">Month</span></span></p></td>
<td><p><span data-ttu-id="0d526-236">Euro</span><span class="sxs-lookup"><span data-stu-id="0d526-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="0d526-237">500</span><span class="sxs-lookup"><span data-stu-id="0d526-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d526-238">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="0d526-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="0d526-239">AboKat1</span><span class="sxs-lookup"><span data-stu-id="0d526-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="0d526-240">9030</span><span class="sxs-lookup"><span data-stu-id="0d526-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0d526-241">Ay</span><span class="sxs-lookup"><span data-stu-id="0d526-241">Month</span></span></p></td>
<td><p><span data-ttu-id="0d526-242">Euro</span><span class="sxs-lookup"><span data-stu-id="0d526-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="0d526-243">550</span><span class="sxs-lookup"><span data-stu-id="0d526-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0d526-244">Abo1 abonelik grubundaki her iki aboneliğin abonelik ücretlerini oluşturmak için yukarıda açıklanan prosedürü tekrarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="0d526-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="0d526-245">Aşağıdaki tabloda abonelik grubuna eklenmiş her abonelik her abonelik için oluşturulan hareketler gösterilir.</span><span class="sxs-lookup"><span data-stu-id="0d526-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

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
<th><p><span data-ttu-id="0d526-246">Proje tarihi</span><span class="sxs-lookup"><span data-stu-id="0d526-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="0d526-247">Abonelik</span><span class="sxs-lookup"><span data-stu-id="0d526-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="0d526-248">Proje</span><span class="sxs-lookup"><span data-stu-id="0d526-248">Project</span></span></p></th>
<th><p><span data-ttu-id="0d526-249">Kategori</span><span class="sxs-lookup"><span data-stu-id="0d526-249">Category</span></span></p></th>
<th><p><span data-ttu-id="0d526-250">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="0d526-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="0d526-251">Bitiş tarihi</span><span class="sxs-lookup"><span data-stu-id="0d526-251">End date</span></span></p></th>
<th><p><span data-ttu-id="0d526-252">Satış para birimi</span><span class="sxs-lookup"><span data-stu-id="0d526-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="0d526-253">Satış fiyatı</span><span class="sxs-lookup"><span data-stu-id="0d526-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0d526-254">28-07-2007</span><span class="sxs-lookup"><span data-stu-id="0d526-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="0d526-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="0d526-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="0d526-256">9030</span><span class="sxs-lookup"><span data-stu-id="0d526-256">9030</span></span></p></td>
<td><p><span data-ttu-id="0d526-257">AboKat1</span><span class="sxs-lookup"><span data-stu-id="0d526-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="0d526-258">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="0d526-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="0d526-259">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="0d526-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="0d526-260">Euro</span><span class="sxs-lookup"><span data-stu-id="0d526-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="0d526-261">550</span><span class="sxs-lookup"><span data-stu-id="0d526-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d526-262">28-07-2008</span><span class="sxs-lookup"><span data-stu-id="0d526-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="0d526-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="0d526-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="0d526-264">9030</span><span class="sxs-lookup"><span data-stu-id="0d526-264">9030</span></span></p></td>
<td><p><span data-ttu-id="0d526-265">AboKat2</span><span class="sxs-lookup"><span data-stu-id="0d526-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="0d526-266">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="0d526-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="0d526-267">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="0d526-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="0d526-268">Euro</span><span class="sxs-lookup"><span data-stu-id="0d526-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="0d526-269">500</span><span class="sxs-lookup"><span data-stu-id="0d526-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0d526-270">00020\_135 aboneliği için olan ilk harekette, belirtilen proje ve kategori birleşimine ayarlanan abonelik satış fiyatından 550 Euro satış fiyatı türetilir.</span><span class="sxs-lookup"><span data-stu-id="0d526-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="0d526-271">00021\_135 aboneliği için olan ikinci harekette, 9030 projesi ve SubCat2 kategorisi birleşimi için fiyat ayarı bulunmadığından, projenin abonelik satış fiyatı olarak 500 Euro satış fiyatı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0d526-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="0d526-272">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="0d526-272">See also</span></span>

[<span data-ttu-id="0d526-273">Abonelik satış fiyatlarını güncelleştirme ve dizine alma</span><span class="sxs-lookup"><span data-stu-id="0d526-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  


