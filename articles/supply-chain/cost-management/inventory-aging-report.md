---
title: Stok yaşlandırma raporu örnekleri ve mantığı
description: Bu konu, Stok yaşlandırma raporunun sonuçlarının nasıl yorumlanacağını gösteren bazı örnekler sunar.
author: AndersGirke
ms.date: 5/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: edc974bcbd72ef62438fd6271a6fd0e56143f976
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821597"
---
# <a name="inventory-aging-report-examples-and-logic"></a><span data-ttu-id="3d365-103">Stok yaşlandırma raporu örnekleri ve mantığı</span><span class="sxs-lookup"><span data-stu-id="3d365-103">Inventory aging report examples and logic</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d365-104">Bu konu, **Stok yaşlandırma** raporunun sonuçlarının nasıl yorumlanacağını gösteren bazı örnekler sunar.</span><span class="sxs-lookup"><span data-stu-id="3d365-104">This topic presents some examples that show how to interpret the results of an **Inventory aging** report.</span></span> <span data-ttu-id="3d365-105">Bu rapor, seçili bir madde veya madde grubu için eldeki miktar ve stok değerlerini çeşitli dönem demetlerinde kategorileştirir.</span><span class="sxs-lookup"><span data-stu-id="3d365-105">This report categorizes on-hand quantity and inventory values for a selected item or item group into several period buckets.</span></span> <span data-ttu-id="3d365-106">Bu konu ayrıca raporun iç mantığını da gösterir.</span><span class="sxs-lookup"><span data-stu-id="3d365-106">This topic also shows the internal logic of the report.</span></span>

<span data-ttu-id="3d365-107">Bu konudaki örneklerde, standart **Stok yaşlandırma** raporunda sunulan sonuçlar gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="3d365-107">The examples in this topic show results that are presented on a standard **Inventory aging** report.</span></span> <span data-ttu-id="3d365-108">Ancak genel olarak, özellikle de işlenmesi gereken çok sayıda madde ve ambara sahipseniz bu raporun [Stok yaşlandırma raporu depolama](inventory-aging-report-storage.md) sürümünü kullanmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="3d365-108">However, in general, we recommend that you use the [Inventory aging report storage](inventory-aging-report-storage.md) version of this report, especially when you have many items and warehouses that must be processed.</span></span> <span data-ttu-id="3d365-109">Stok yaşlandırma raporu depolaması, oluşturduğunuz her raporu kaydeder, sonuçları etkileşimli bir sayfa ve bir grafik olarak gösterir ve kaydedilmiş herhangi bir raporu dışa aktarmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="3d365-109">Inventory aging report storage saves each report that you generate, shows the results as an interactive page and a chart, and lets you export any saved report.</span></span>

## <a name="sample-data-that-is-used-in-these-examples"></a><span data-ttu-id="3d365-110">Bu örneklerde kullanılan örnek veriler</span><span class="sxs-lookup"><span data-stu-id="3d365-110">Sample data that is used in these examples</span></span>

<span data-ttu-id="3d365-111">Bu konudaki örnekler, bu bölümde açıklanan örnek stok hareketi verilerini temel almaktadır.</span><span class="sxs-lookup"><span data-stu-id="3d365-111">The examples in this topic are based on the sample inventory transaction data that is described in this section.</span></span>

### <a name="storage-dimension-setup"></a><span data-ttu-id="3d365-112">Depolama boyutu kurulumu</span><span class="sxs-lookup"><span data-stu-id="3d365-112">Storage dimension setup</span></span>

<span data-ttu-id="3d365-113">Örnek sistem, aşağıdaki depolama boyutları kurulumunu içerir.</span><span class="sxs-lookup"><span data-stu-id="3d365-113">The example system contains the following setup of storage dimensions.</span></span>

| <span data-ttu-id="3d365-114">Dosya Adı</span><span class="sxs-lookup"><span data-stu-id="3d365-114">Name</span></span>      | <span data-ttu-id="3d365-115">Active</span><span class="sxs-lookup"><span data-stu-id="3d365-115">Active</span></span> | <span data-ttu-id="3d365-116">Fiziksel stok</span><span class="sxs-lookup"><span data-stu-id="3d365-116">Physical inventory</span></span> | <span data-ttu-id="3d365-117">Mali stok</span><span class="sxs-lookup"><span data-stu-id="3d365-117">Financial inventory</span></span> |
|-----------|--------|--------------------|---------------------|
| <span data-ttu-id="3d365-118">Tesis</span><span class="sxs-lookup"><span data-stu-id="3d365-118">Site</span></span>      | <span data-ttu-id="3d365-119">Evet</span><span class="sxs-lookup"><span data-stu-id="3d365-119">Yes</span></span>    | <span data-ttu-id="3d365-120">Evet</span><span class="sxs-lookup"><span data-stu-id="3d365-120">Yes</span></span>                | <span data-ttu-id="3d365-121">Evet</span><span class="sxs-lookup"><span data-stu-id="3d365-121">Yes</span></span>                 |
| <span data-ttu-id="3d365-122">Ambar</span><span class="sxs-lookup"><span data-stu-id="3d365-122">Warehouse</span></span> | <span data-ttu-id="3d365-123">Evet</span><span class="sxs-lookup"><span data-stu-id="3d365-123">Yes</span></span>    | <span data-ttu-id="3d365-124">Evet</span><span class="sxs-lookup"><span data-stu-id="3d365-124">Yes</span></span>                | <span data-ttu-id="3d365-125">No</span><span class="sxs-lookup"><span data-stu-id="3d365-125">No</span></span>                  |

### <a name="inventory-model"></a><span data-ttu-id="3d365-126">Stok modeli</span><span class="sxs-lookup"><span data-stu-id="3d365-126">Inventory model</span></span>

<span data-ttu-id="3d365-127">Örnek sistem için, serbest bırakılan ürünlerin stok modeli *FIFO* ve stok modeli için **Maliyet fiyatı** ayarı *Fiziksel değeri dahil et*'tir.</span><span class="sxs-lookup"><span data-stu-id="3d365-127">For the example system, the inventory model for the released products is *FIFO*, and the **Cost price** setting for the inventory model is *Include physical value*.</span></span>

### <a name="inventory-transactions"></a><span data-ttu-id="3d365-128">Stok hareketleri</span><span class="sxs-lookup"><span data-stu-id="3d365-128">Inventory transactions</span></span>

<span data-ttu-id="3d365-129">Örnek sistem, *1000* madde numarasına sahip olan serbest bırakılan ürün için aşağıdaki stok hareketlerini içerir.</span><span class="sxs-lookup"><span data-stu-id="3d365-129">The example system contains the following inventory transactions for a released product that has the item number *1000*.</span></span>

| <span data-ttu-id="3d365-130">Referans</span><span class="sxs-lookup"><span data-stu-id="3d365-130">Reference</span></span>      | <span data-ttu-id="3d365-131">Tesis</span><span class="sxs-lookup"><span data-stu-id="3d365-131">Site</span></span> | <span data-ttu-id="3d365-132">Ambar</span><span class="sxs-lookup"><span data-stu-id="3d365-132">Warehouse</span></span> | <span data-ttu-id="3d365-133">Giriş</span><span class="sxs-lookup"><span data-stu-id="3d365-133">Receipt</span></span>   | <span data-ttu-id="3d365-134">Çıkış</span><span class="sxs-lookup"><span data-stu-id="3d365-134">Issue</span></span> | <span data-ttu-id="3d365-135">Fiili tarih</span><span class="sxs-lookup"><span data-stu-id="3d365-135">Physical date</span></span> | <span data-ttu-id="3d365-136">Mali tarih</span><span class="sxs-lookup"><span data-stu-id="3d365-136">Financial date</span></span> | <span data-ttu-id="3d365-137">Miktar</span><span class="sxs-lookup"><span data-stu-id="3d365-137">Quantity</span></span> | <span data-ttu-id="3d365-138">Maliyet tutarı</span><span class="sxs-lookup"><span data-stu-id="3d365-138">Cost amount</span></span> | <span data-ttu-id="3d365-139">Fiziksel maliyet tutarı</span><span class="sxs-lookup"><span data-stu-id="3d365-139">Physical cost amount</span></span> |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| <span data-ttu-id="3d365-140">Satın alma siparişi</span><span class="sxs-lookup"><span data-stu-id="3d365-140">Purchase order</span></span> | <span data-ttu-id="3d365-141">1</span><span class="sxs-lookup"><span data-stu-id="3d365-141">1</span></span>    | <span data-ttu-id="3d365-142">11</span><span class="sxs-lookup"><span data-stu-id="3d365-142">11</span></span>        | <span data-ttu-id="3d365-143">Satın alınan</span><span class="sxs-lookup"><span data-stu-id="3d365-143">Purchased</span></span> |       | <span data-ttu-id="3d365-144">Mart 15</span><span class="sxs-lookup"><span data-stu-id="3d365-144">March 15</span></span>      | <span data-ttu-id="3d365-145">Mart 15</span><span class="sxs-lookup"><span data-stu-id="3d365-145">March 15</span></span>       | <span data-ttu-id="3d365-146">10</span><span class="sxs-lookup"><span data-stu-id="3d365-146">10</span></span>       | <span data-ttu-id="3d365-147">1,000</span><span class="sxs-lookup"><span data-stu-id="3d365-147">1,000</span></span>       | <span data-ttu-id="3d365-148">1,000</span><span class="sxs-lookup"><span data-stu-id="3d365-148">1,000</span></span>                |
| <span data-ttu-id="3d365-149">Satın alma siparişi</span><span class="sxs-lookup"><span data-stu-id="3d365-149">Purchase order</span></span> | <span data-ttu-id="3d365-150">2</span><span class="sxs-lookup"><span data-stu-id="3d365-150">2</span></span>    | <span data-ttu-id="3d365-151">21</span><span class="sxs-lookup"><span data-stu-id="3d365-151">21</span></span>        | <span data-ttu-id="3d365-152">Satın alınan</span><span class="sxs-lookup"><span data-stu-id="3d365-152">Purchased</span></span> |       | <span data-ttu-id="3d365-153">Mart 15</span><span class="sxs-lookup"><span data-stu-id="3d365-153">March 15</span></span>      | <span data-ttu-id="3d365-154">Mart 15</span><span class="sxs-lookup"><span data-stu-id="3d365-154">March 15</span></span>       | <span data-ttu-id="3d365-155">10</span><span class="sxs-lookup"><span data-stu-id="3d365-155">10</span></span>       | <span data-ttu-id="3d365-156">2,000</span><span class="sxs-lookup"><span data-stu-id="3d365-156">2,000</span></span>       | <span data-ttu-id="3d365-157">2,000</span><span class="sxs-lookup"><span data-stu-id="3d365-157">2,000</span></span>                |
| <span data-ttu-id="3d365-158">Satın alma siparişi</span><span class="sxs-lookup"><span data-stu-id="3d365-158">Purchase order</span></span> | <span data-ttu-id="3d365-159">1</span><span class="sxs-lookup"><span data-stu-id="3d365-159">1</span></span>    | <span data-ttu-id="3d365-160">11</span><span class="sxs-lookup"><span data-stu-id="3d365-160">11</span></span>        | <span data-ttu-id="3d365-161">Alınan</span><span class="sxs-lookup"><span data-stu-id="3d365-161">Received</span></span>  |       | <span data-ttu-id="3d365-162">Nisan 15</span><span class="sxs-lookup"><span data-stu-id="3d365-162">April 15</span></span>      |                | <span data-ttu-id="3d365-163">5</span><span class="sxs-lookup"><span data-stu-id="3d365-163">5</span></span>        |             | <span data-ttu-id="3d365-164">375</span><span class="sxs-lookup"><span data-stu-id="3d365-164">375</span></span>                  |
| <span data-ttu-id="3d365-165">Transfer emri</span><span class="sxs-lookup"><span data-stu-id="3d365-165">Transfer order</span></span> | <span data-ttu-id="3d365-166">1</span><span class="sxs-lookup"><span data-stu-id="3d365-166">1</span></span>    | <span data-ttu-id="3d365-167">11</span><span class="sxs-lookup"><span data-stu-id="3d365-167">11</span></span>        |           | <span data-ttu-id="3d365-168">Satılan</span><span class="sxs-lookup"><span data-stu-id="3d365-168">Sold</span></span>  | <span data-ttu-id="3d365-169">Mayıs 2</span><span class="sxs-lookup"><span data-stu-id="3d365-169">May 2</span></span>         | <span data-ttu-id="3d365-170">Mayıs 2</span><span class="sxs-lookup"><span data-stu-id="3d365-170">May 2</span></span>          | <span data-ttu-id="3d365-171">-5</span><span class="sxs-lookup"><span data-stu-id="3d365-171">-5</span></span>       | <span data-ttu-id="3d365-172">-458,33</span><span class="sxs-lookup"><span data-stu-id="3d365-172">-458.33</span></span>     | <span data-ttu-id="3d365-173">-458,33</span><span class="sxs-lookup"><span data-stu-id="3d365-173">-458.33</span></span>              |
| <span data-ttu-id="3d365-174">Transfer emri</span><span class="sxs-lookup"><span data-stu-id="3d365-174">Transfer order</span></span> | <span data-ttu-id="3d365-175">1</span><span class="sxs-lookup"><span data-stu-id="3d365-175">1</span></span>    | <span data-ttu-id="3d365-176">12</span><span class="sxs-lookup"><span data-stu-id="3d365-176">12</span></span>        | <span data-ttu-id="3d365-177">Satın alınan</span><span class="sxs-lookup"><span data-stu-id="3d365-177">Purchased</span></span> |       | <span data-ttu-id="3d365-178">Mayıs 2</span><span class="sxs-lookup"><span data-stu-id="3d365-178">May 2</span></span>         | <span data-ttu-id="3d365-179">Mayıs 2</span><span class="sxs-lookup"><span data-stu-id="3d365-179">May 2</span></span>          | <span data-ttu-id="3d365-180">5</span><span class="sxs-lookup"><span data-stu-id="3d365-180">5</span></span>        | <span data-ttu-id="3d365-181">458.33</span><span class="sxs-lookup"><span data-stu-id="3d365-181">458.33</span></span>      | <span data-ttu-id="3d365-182">458.33</span><span class="sxs-lookup"><span data-stu-id="3d365-182">458.33</span></span>               |
| <span data-ttu-id="3d365-183">Satış siparişi</span><span class="sxs-lookup"><span data-stu-id="3d365-183">Sales order</span></span>    | <span data-ttu-id="3d365-184">1</span><span class="sxs-lookup"><span data-stu-id="3d365-184">1</span></span>    | <span data-ttu-id="3d365-185">12</span><span class="sxs-lookup"><span data-stu-id="3d365-185">12</span></span>        |           | <span data-ttu-id="3d365-186">Satılan</span><span class="sxs-lookup"><span data-stu-id="3d365-186">Sold</span></span>  | <span data-ttu-id="3d365-187">Mayıs 3</span><span class="sxs-lookup"><span data-stu-id="3d365-187">May 3</span></span>         | <span data-ttu-id="3d365-188">Mayıs 3</span><span class="sxs-lookup"><span data-stu-id="3d365-188">May 3</span></span>          | <span data-ttu-id="3d365-189">-1</span><span class="sxs-lookup"><span data-stu-id="3d365-189">-1</span></span>       | <span data-ttu-id="3d365-190">-91,67</span><span class="sxs-lookup"><span data-stu-id="3d365-190">-91.67</span></span>      | <span data-ttu-id="3d365-191">-91,67</span><span class="sxs-lookup"><span data-stu-id="3d365-191">-91.67</span></span>               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a><span data-ttu-id="3d365-192">Her dönem demetindeki miktarların ve tutarların hesaplanması</span><span class="sxs-lookup"><span data-stu-id="3d365-192">How quantities and amounts in each period bucket are calculated</span></span>

<span data-ttu-id="3d365-193">Önceki bölümlerde açıklanan örnek verileri kullanarak, aşağıdaki ayarlara sahip bir **Stok yaşlandırma** raporu çalıştırabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="3d365-193">By using the sample data that is described in the previous sections, you can run an **Inventory aging** report that has the following settings:</span></span>

- <span data-ttu-id="3d365-194">**Başlangıç tarihi:** *9 Mayıs 2020*</span><span class="sxs-lookup"><span data-stu-id="3d365-194">**As of date:** *May 9, 2020*</span></span>
- <span data-ttu-id="3d365-195">**Tesis:** *Görüntüle*</span><span class="sxs-lookup"><span data-stu-id="3d365-195">**Site:** *View*</span></span>
- <span data-ttu-id="3d365-196">**Ambar:** *Hayır*</span><span class="sxs-lookup"><span data-stu-id="3d365-196">**Warehouse:** *No*</span></span>
- <span data-ttu-id="3d365-197">**Madde numarası:** *Toplam*</span><span class="sxs-lookup"><span data-stu-id="3d365-197">**Item number:** *Total*</span></span>
- <span data-ttu-id="3d365-198">**Yaşlandırma dönemi:** Bu alanı aylık demetler oluşturmak üzere ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="3d365-198">**Aging period:** Set this field to generate monthly buckets.</span></span>

<span data-ttu-id="3d365-199">Bu durumda, oluşturulan raporun içeriği aşağıdaki örneğe benzeyecektir.</span><span class="sxs-lookup"><span data-stu-id="3d365-199">In this case, the content of the report that is generated will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="3d365-200">Madde kodu</span><span class="sxs-lookup"><span data-stu-id="3d365-200">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="3d365-201">Tesis</span><span class="sxs-lookup"><span data-stu-id="3d365-201">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="3d365-202">Eldeki miktar</span><span class="sxs-lookup"><span data-stu-id="3d365-202">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="3d365-203">Eldeki değer</span><span class="sxs-lookup"><span data-stu-id="3d365-203">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="3d365-204">Stok değeri miktarı</span><span class="sxs-lookup"><span data-stu-id="3d365-204">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="3d365-205">Stok değeri</span><span class="sxs-lookup"><span data-stu-id="3d365-205">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="3d365-206">Ortalama birim maliyeti</span><span class="sxs-lookup"><span data-stu-id="3d365-206">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="3d365-207">8/5/2020 - 1/5/2020</span><span class="sxs-lookup"><span data-stu-id="3d365-207">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="3d365-208">30/4/2020 - 1/4/2020</span><span class="sxs-lookup"><span data-stu-id="3d365-208">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="3d365-209">31/3/2020 - 1/3/2020</span><span class="sxs-lookup"><span data-stu-id="3d365-209">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="3d365-210">P1:Miktar</span><span class="sxs-lookup"><span data-stu-id="3d365-210">P1:Quantity</span></span></th>
    <th><span data-ttu-id="3d365-211">P1:Tutar</span><span class="sxs-lookup"><span data-stu-id="3d365-211">P1:Amount</span></span></th>
    <th><span data-ttu-id="3d365-212">P2:Miktar</span><span class="sxs-lookup"><span data-stu-id="3d365-212">P2:Quantity</span></span></th>
    <th><span data-ttu-id="3d365-213">P2:Tutar</span><span class="sxs-lookup"><span data-stu-id="3d365-213">P2:Amount</span></span></th>
    <th><span data-ttu-id="3d365-214">P3:Miktar</span><span class="sxs-lookup"><span data-stu-id="3d365-214">P3:Quantity</span></span></th>
    <th><span data-ttu-id="3d365-215">P3:Tutar</span><span class="sxs-lookup"><span data-stu-id="3d365-215">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="3d365-216">1000</span><span class="sxs-lookup"><span data-stu-id="3d365-216">1000</span></span></td>
    <td><span data-ttu-id="3d365-217">1</span><span class="sxs-lookup"><span data-stu-id="3d365-217">1</span></span></td>
    <td><span data-ttu-id="3d365-218">14</span><span class="sxs-lookup"><span data-stu-id="3d365-218">14</span></span></td>
    <td><span data-ttu-id="3d365-219">1,283.33</span><span class="sxs-lookup"><span data-stu-id="3d365-219">1,283.33</span></span></td>
    <td><span data-ttu-id="3d365-220">14</span><span class="sxs-lookup"><span data-stu-id="3d365-220">14</span></span></td>
    <td><span data-ttu-id="3d365-221">1,283.33</span><span class="sxs-lookup"><span data-stu-id="3d365-221">1,283.33</span></span></td>
    <td><span data-ttu-id="3d365-222">91.67</span><span class="sxs-lookup"><span data-stu-id="3d365-222">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="3d365-223">5.00</span><span class="sxs-lookup"><span data-stu-id="3d365-223">5.00</span></span></td>
    <td><span data-ttu-id="3d365-224">458.33</span><span class="sxs-lookup"><span data-stu-id="3d365-224">458.33</span></span></td>
    <td><span data-ttu-id="3d365-225">9.00</span><span class="sxs-lookup"><span data-stu-id="3d365-225">9.00</span></span></td>
    <td><span data-ttu-id="3d365-226">825.00</span><span class="sxs-lookup"><span data-stu-id="3d365-226">825.00</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="3d365-227">1000</span><span class="sxs-lookup"><span data-stu-id="3d365-227">1000</span></span></td>
    <td><span data-ttu-id="3d365-228">2</span><span class="sxs-lookup"><span data-stu-id="3d365-228">2</span></span></td>
    <td><span data-ttu-id="3d365-229">10</span><span class="sxs-lookup"><span data-stu-id="3d365-229">10</span></span></td>
    <td><span data-ttu-id="3d365-230">2,000.00</span><span class="sxs-lookup"><span data-stu-id="3d365-230">2,000.00</span></span></td>
    <td><span data-ttu-id="3d365-231">10</span><span class="sxs-lookup"><span data-stu-id="3d365-231">10</span></span></td>
    <td><span data-ttu-id="3d365-232">2,000.00</span><span class="sxs-lookup"><span data-stu-id="3d365-232">2,000.00</span></span></td>
    <td><span data-ttu-id="3d365-233">200.00</span><span class="sxs-lookup"><span data-stu-id="3d365-233">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="3d365-234">10,00</span><span class="sxs-lookup"><span data-stu-id="3d365-234">10.00</span></span></td>
    <td><span data-ttu-id="3d365-235">2,000.00</span><span class="sxs-lookup"><span data-stu-id="3d365-235">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="3d365-236"><strong>1000 Toplam</strong></span><span class="sxs-lookup"><span data-stu-id="3d365-236"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td><span data-ttu-id="3d365-237"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="3d365-237"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="3d365-238"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="3d365-238"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="3d365-239"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="3d365-239"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="3d365-240"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="3d365-240"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="3d365-241"><strong>19</strong></span><span class="sxs-lookup"><span data-stu-id="3d365-241"><strong>19</strong></span></span></td>
    <td><span data-ttu-id="3d365-242"><strong>2,825.00</strong></span><span class="sxs-lookup"><span data-stu-id="3d365-242"><strong>2,825.00</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="3d365-243">Bu örnek raporda aşağıdaki ayrıntılara dikkat edin:</span><span class="sxs-lookup"><span data-stu-id="3d365-243">Note the following details in this example report:</span></span>

- <span data-ttu-id="3d365-244">Raporda gösterilen **Stok değeri miktarı**, **Stok değeri** ve **Ortalama birim maliyet** değerleri, mali stok boyutu (bu durumda **Tesis**) için olan değerlerdir.</span><span class="sxs-lookup"><span data-stu-id="3d365-244">The **Inventory value quantity**, **Inventory value**, and **Average unit cost** values that are shown on the report are values for the financial inventory dimension (**Site**, in this case).</span></span>

    <span data-ttu-id="3d365-245">Örneğin, 1 numaralı tesiste, rapor aşağıdaki bilgileri gösterir:</span><span class="sxs-lookup"><span data-stu-id="3d365-245">For example, for site 1, the report shows the following information:</span></span>

    - <span data-ttu-id="3d365-246">**Stok değeri miktarı** değeri *14*'tür (= 10 + 5 – 5 + 5 – 1).</span><span class="sxs-lookup"><span data-stu-id="3d365-246">The **Inventory value quantity** value is *14* (= 10 + 5 – 5 + 5 – 1).</span></span>
    - <span data-ttu-id="3d365-247">**Stok değeri** değeri *1.283,33*'tür (= 1.000 + 375 – 458,33 + 458,33 – 91,67).</span><span class="sxs-lookup"><span data-stu-id="3d365-247">The **Inventory value** value is *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67).</span></span>
    - <span data-ttu-id="3d365-248">**Ortalama birim maliyet** değeri *91,67*'dir.</span><span class="sxs-lookup"><span data-stu-id="3d365-248">The **Average unit cost** value is *91.67*.</span></span>
    - <span data-ttu-id="3d365-249">Her bir dönem demetindeki **Eldeki stok değeri** değeri ve **Tutar** değeri **Ortalama birim maliyet** değeri kullanılarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="3d365-249">The **On-hand value** value and the **Amount** value in each period bucket are calculated by using the **Average unit cost** value.</span></span>

- <span data-ttu-id="3d365-250">Rapor, her dönem demeti için alınan toplam stok miktarını özetleyerek her bir dönem demeti için eldeki miktarı belirler.</span><span class="sxs-lookup"><span data-stu-id="3d365-250">The report determines the on-hand quantity for each period bucket by summarizing the total received inventory quantity for each period bucket.</span></span> <span data-ttu-id="3d365-251">Daha sonra, maddelerin kullandığı stok modelini dikkate almaksızın, verilen toplam miktarı düşmek için ilk giren, ilk çıkan (FIFO) ilkesini uygular.</span><span class="sxs-lookup"><span data-stu-id="3d365-251">It then applies the first in, first out (FIFO) principle to deduct the total issued quantity, regardless of the inventory model that the items use.</span></span>

<span data-ttu-id="3d365-252">Aynı raporu tekrar çalıştırırsanız, ancak bu kez hem **Tesis** hem de **Ambar** alanlarını *Görüntüle* olarak ayarlarsanız, yeni rapor aşağıdaki örneğe benzer.</span><span class="sxs-lookup"><span data-stu-id="3d365-252">If you run the same report again, but this time you set both the **Site** and **Warehouse** fields to *View*, the new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="3d365-253">Madde kodu</span><span class="sxs-lookup"><span data-stu-id="3d365-253">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="3d365-254">Tesis</span><span class="sxs-lookup"><span data-stu-id="3d365-254">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="3d365-255">Ambar</span><span class="sxs-lookup"><span data-stu-id="3d365-255">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="3d365-256">Eldeki miktar</span><span class="sxs-lookup"><span data-stu-id="3d365-256">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="3d365-257">Eldeki değer</span><span class="sxs-lookup"><span data-stu-id="3d365-257">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="3d365-258">Stok değeri miktarı</span><span class="sxs-lookup"><span data-stu-id="3d365-258">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="3d365-259">Stok değeri</span><span class="sxs-lookup"><span data-stu-id="3d365-259">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="3d365-260">Ortalama birim maliyeti</span><span class="sxs-lookup"><span data-stu-id="3d365-260">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="3d365-261">8/5/2020 - 1/5/2020</span><span class="sxs-lookup"><span data-stu-id="3d365-261">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="3d365-262">30/4/2020 - 1/4/2020</span><span class="sxs-lookup"><span data-stu-id="3d365-262">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="3d365-263">31/3/2020 - 1/3/2020</span><span class="sxs-lookup"><span data-stu-id="3d365-263">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="3d365-264">P1:Miktar</span><span class="sxs-lookup"><span data-stu-id="3d365-264">P1:Quantity</span></span></th>
    <th><span data-ttu-id="3d365-265">P1:Tutar</span><span class="sxs-lookup"><span data-stu-id="3d365-265">P1:Amount</span></span></th>
    <th><span data-ttu-id="3d365-266">P2:Miktar</span><span class="sxs-lookup"><span data-stu-id="3d365-266">P2:Quantity</span></span></th>
    <th><span data-ttu-id="3d365-267">P2:Tutar</span><span class="sxs-lookup"><span data-stu-id="3d365-267">P2:Amount</span></span></th>
    <th><span data-ttu-id="3d365-268">P3:Miktar</span><span class="sxs-lookup"><span data-stu-id="3d365-268">P3:Quantity</span></span></th>
    <th><span data-ttu-id="3d365-269">P3:Tutar</span><span class="sxs-lookup"><span data-stu-id="3d365-269">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="3d365-270">1000</span><span class="sxs-lookup"><span data-stu-id="3d365-270">1000</span></span></td>
    <td><span data-ttu-id="3d365-271">1</span><span class="sxs-lookup"><span data-stu-id="3d365-271">1</span></span></td>
    <td><span data-ttu-id="3d365-272">11</span><span class="sxs-lookup"><span data-stu-id="3d365-272">11</span></span></td>
    <td><span data-ttu-id="3d365-273">10</span><span class="sxs-lookup"><span data-stu-id="3d365-273">10</span></span></td>
    <td><span data-ttu-id="3d365-274">916.67</span><span class="sxs-lookup"><span data-stu-id="3d365-274">916.67</span></span></td>
    <td><span data-ttu-id="3d365-275">14</span><span class="sxs-lookup"><span data-stu-id="3d365-275">14</span></span></td>
    <td><span data-ttu-id="3d365-276">1,283.33</span><span class="sxs-lookup"><span data-stu-id="3d365-276">1,283.33</span></span></td>
    <td><span data-ttu-id="3d365-277">91.67</span><span class="sxs-lookup"><span data-stu-id="3d365-277">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="3d365-278">5.00</span><span class="sxs-lookup"><span data-stu-id="3d365-278">5.00</span></span></td>
    <td><span data-ttu-id="3d365-279">458.33</span><span class="sxs-lookup"><span data-stu-id="3d365-279">458.33</span></span></td>
    <td><span data-ttu-id="3d365-280">5.00</span><span class="sxs-lookup"><span data-stu-id="3d365-280">5.00</span></span></td>
    <td><span data-ttu-id="3d365-281">458.33</span><span class="sxs-lookup"><span data-stu-id="3d365-281">458.33</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="3d365-282">1000</span><span class="sxs-lookup"><span data-stu-id="3d365-282">1000</span></span></td>
    <td><span data-ttu-id="3d365-283">1</span><span class="sxs-lookup"><span data-stu-id="3d365-283">1</span></span></td>
    <td><span data-ttu-id="3d365-284">12</span><span class="sxs-lookup"><span data-stu-id="3d365-284">12</span></span></td>
    <td><span data-ttu-id="3d365-285">4</span><span class="sxs-lookup"><span data-stu-id="3d365-285">4</span></span></td>
    <td><span data-ttu-id="3d365-286">366.67</span><span class="sxs-lookup"><span data-stu-id="3d365-286">366.67</span></span></td>
    <td><span data-ttu-id="3d365-287">14</span><span class="sxs-lookup"><span data-stu-id="3d365-287">14</span></span></td>
    <td><span data-ttu-id="3d365-288">1,283.33</span><span class="sxs-lookup"><span data-stu-id="3d365-288">1,283.33</span></span></td>
    <td><span data-ttu-id="3d365-289">91.67</span><span class="sxs-lookup"><span data-stu-id="3d365-289">91.67</span></span></td>
    <td><span data-ttu-id="3d365-290">4.00</span><span class="sxs-lookup"><span data-stu-id="3d365-290">4.00</span></span></td>
    <td><span data-ttu-id="3d365-291">366.67</span><span class="sxs-lookup"><span data-stu-id="3d365-291">366.67</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="3d365-292">1000</span><span class="sxs-lookup"><span data-stu-id="3d365-292">1000</span></span></td>
    <td><span data-ttu-id="3d365-293">2</span><span class="sxs-lookup"><span data-stu-id="3d365-293">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="3d365-294">10</span><span class="sxs-lookup"><span data-stu-id="3d365-294">10</span></span></td>
    <td><span data-ttu-id="3d365-295">2,000.00</span><span class="sxs-lookup"><span data-stu-id="3d365-295">2,000.00</span></span></td>
    <td><span data-ttu-id="3d365-296">10</span><span class="sxs-lookup"><span data-stu-id="3d365-296">10</span></span></td>
    <td><span data-ttu-id="3d365-297">2,000.00</span><span class="sxs-lookup"><span data-stu-id="3d365-297">2,000.00</span></span></td>
    <td><span data-ttu-id="3d365-298">200.00</span><span class="sxs-lookup"><span data-stu-id="3d365-298">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="3d365-299">10,00</span><span class="sxs-lookup"><span data-stu-id="3d365-299">10.00</span></span></td>
    <td><span data-ttu-id="3d365-300">2,000.00</span><span class="sxs-lookup"><span data-stu-id="3d365-300">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="3d365-301"><strong>1000 Toplam</strong></span><span class="sxs-lookup"><span data-stu-id="3d365-301"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="3d365-302"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="3d365-302"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="3d365-303"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="3d365-303"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="3d365-304"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="3d365-304"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="3d365-305"><strong>366.67</strong></span><span class="sxs-lookup"><span data-stu-id="3d365-305"><strong>366.67</strong></span></span></td>
    <td><span data-ttu-id="3d365-306"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="3d365-306"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="3d365-307"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="3d365-307"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="3d365-308"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="3d365-308"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="3d365-309"><strong>2,458.33</strong></span><span class="sxs-lookup"><span data-stu-id="3d365-309"><strong>2,458.33</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="3d365-310">Bu kez, tesis 1, biri ambar 11 diğeri ise 12 için olmak üzere iki satıra ayrılır.</span><span class="sxs-lookup"><span data-stu-id="3d365-310">This time, site 1 is split into two rows, one for warehouse 11 and one for warehouse 12.</span></span> <span data-ttu-id="3d365-311">Ancak, **Stok değeri miktarı**, **Stok değeri** ve **Ortalama birim maliyet** değerleri aynıdır çünkü **Ambar** mali bir stok boyutu değildir.</span><span class="sxs-lookup"><span data-stu-id="3d365-311">However, the **Inventory value quantity**, **Inventory value**, and **Average unit cost** values are the same, because **Warehouse** isn't a financial inventory dimension.</span></span>

<span data-ttu-id="3d365-312">Ek olarak, tesis 1'in miktar dağılımının farklı olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="3d365-312">Additionally, notice that the quantity distribution of site 1 is different.</span></span> <span data-ttu-id="3d365-313">Çalıştırdığınız ilk raporda, sistem aynı tesiste oluşan transfer emrini yok saymış ve satış faturası tutarını tesis 1'de **31/3/2020-1/3/2020** dönem aralığından düşürmüştü.</span><span class="sxs-lookup"><span data-stu-id="3d365-313">In the first report that you ran, the system ignored the transfer order that occurred in the same site and deducted the quantity of the sales invoice from the **3/31/2020 - 3/1/2020** period bucket in site 1.</span></span> <span data-ttu-id="3d365-314">Ancak, yeni raporda, sistem satış faturasının miktarını, Ambar 12'deki **8/5/2020-1/5/2020** dönem aralığından düşürdü.</span><span class="sxs-lookup"><span data-stu-id="3d365-314">However, in the new report, the system deducts the quantity of the sales invoice from the **5/8/2020 - 5/1/2020** period bucket in warehouse 12.</span></span>

## <a name="effects-of-inventory-closing"></a><span data-ttu-id="3d365-315">Stok kapanışının etkileri</span><span class="sxs-lookup"><span data-stu-id="3d365-315">Effects of inventory closing</span></span>

<span data-ttu-id="3d365-316">Mayıs için stok kapanışı çalıştırır ve ardından önceki raporu yeniden çalıştırırsanız ancak **Başlangıç tarihi** alanını *31 Mayıs 2020* olarak ayarlarsanız, aşağıdaki sonuçları görürsünüz:</span><span class="sxs-lookup"><span data-stu-id="3d365-316">If you run the inventory closing for May and then run the previous report again, but you set the **As of date** field to *May 31, 2020*, you will notice the following results:</span></span>

- <span data-ttu-id="3d365-317">**Stok değeri** ve **Ortalama birim maliyet** değerleri güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="3d365-317">The **Inventory value** and **Average unit cost** values are updated.</span></span>
- <span data-ttu-id="3d365-318">Her dönem demetindeki **Eldeki stok değeri** değeri ve **Tutar** değerleri buna göre güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="3d365-318">The **On-hand value** value and all the **Amount** values in every period bucket are updated accordingly.</span></span>

<span data-ttu-id="3d365-319">Yeni rapor aşağıdaki örneğe benzeyecektir.</span><span class="sxs-lookup"><span data-stu-id="3d365-319">The new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="3d365-320">Madde kodu</span><span class="sxs-lookup"><span data-stu-id="3d365-320">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="3d365-321">Tesis</span><span class="sxs-lookup"><span data-stu-id="3d365-321">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="3d365-322">Ambar</span><span class="sxs-lookup"><span data-stu-id="3d365-322">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="3d365-323">Eldeki miktar</span><span class="sxs-lookup"><span data-stu-id="3d365-323">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="3d365-324">Eldeki değer</span><span class="sxs-lookup"><span data-stu-id="3d365-324">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="3d365-325">Stok değeri miktarı</span><span class="sxs-lookup"><span data-stu-id="3d365-325">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="3d365-326">Stok değeri</span><span class="sxs-lookup"><span data-stu-id="3d365-326">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="3d365-327">Ortalama birim maliyeti</span><span class="sxs-lookup"><span data-stu-id="3d365-327">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="3d365-328">31/5/2020 - 1/5/2020</span><span class="sxs-lookup"><span data-stu-id="3d365-328">5/31/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="3d365-329">30/4/2020 - 1/4/2020</span><span class="sxs-lookup"><span data-stu-id="3d365-329">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="3d365-330">31/3/2020 - 1/3/2020</span><span class="sxs-lookup"><span data-stu-id="3d365-330">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="3d365-331">P1:Miktar</span><span class="sxs-lookup"><span data-stu-id="3d365-331">P1:Quantity</span></span></th>
    <th><span data-ttu-id="3d365-332">P1:Tutar</span><span class="sxs-lookup"><span data-stu-id="3d365-332">P1:Amount</span></span></th>
    <th><span data-ttu-id="3d365-333">P2:Miktar</span><span class="sxs-lookup"><span data-stu-id="3d365-333">P2:Quantity</span></span></th>
    <th><span data-ttu-id="3d365-334">P2:Tutar</span><span class="sxs-lookup"><span data-stu-id="3d365-334">P2:Amount</span></span></th>
    <th><span data-ttu-id="3d365-335">P3:Miktar</span><span class="sxs-lookup"><span data-stu-id="3d365-335">P3:Quantity</span></span></th>
    <th><span data-ttu-id="3d365-336">P3:Tutar</span><span class="sxs-lookup"><span data-stu-id="3d365-336">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="3d365-337">1000</span><span class="sxs-lookup"><span data-stu-id="3d365-337">1000</span></span></td>
    <td><span data-ttu-id="3d365-338">1</span><span class="sxs-lookup"><span data-stu-id="3d365-338">1</span></span></td>
    <td><span data-ttu-id="3d365-339">11</span><span class="sxs-lookup"><span data-stu-id="3d365-339">11</span></span></td>
    <td><span data-ttu-id="3d365-340">10</span><span class="sxs-lookup"><span data-stu-id="3d365-340">10</span></span></td>
    <td><span data-ttu-id="3d365-341">910.70</span><span class="sxs-lookup"><span data-stu-id="3d365-341">910.70</span></span></td>
    <td><span data-ttu-id="3d365-342">14</span><span class="sxs-lookup"><span data-stu-id="3d365-342">14</span></span></td>
    <td><span data-ttu-id="3d365-343">1,275.00</span><span class="sxs-lookup"><span data-stu-id="3d365-343">1,275.00</span></span></td>
    <td><span data-ttu-id="3d365-344">91.07</span><span class="sxs-lookup"><span data-stu-id="3d365-344">91.07</span></span></td>
    <td><span data-ttu-id="3d365-345">0,00</span><span class="sxs-lookup"><span data-stu-id="3d365-345">0.00</span></span></td>
    <td></td>
    <td><span data-ttu-id="3d365-346">5.00</span><span class="sxs-lookup"><span data-stu-id="3d365-346">5.00</span></span></td>
    <td><span data-ttu-id="3d365-347">455.36</span><span class="sxs-lookup"><span data-stu-id="3d365-347">455.36</span></span></td>
    <td><span data-ttu-id="3d365-348">5.00</span><span class="sxs-lookup"><span data-stu-id="3d365-348">5.00</span></span></td>
    <td><span data-ttu-id="3d365-349">455.36</span><span class="sxs-lookup"><span data-stu-id="3d365-349">455.36</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="3d365-350">1000</span><span class="sxs-lookup"><span data-stu-id="3d365-350">1000</span></span></td>
    <td><span data-ttu-id="3d365-351">1</span><span class="sxs-lookup"><span data-stu-id="3d365-351">1</span></span></td>
    <td><span data-ttu-id="3d365-352">12</span><span class="sxs-lookup"><span data-stu-id="3d365-352">12</span></span></td>
    <td><span data-ttu-id="3d365-353">4</span><span class="sxs-lookup"><span data-stu-id="3d365-353">4</span></span></td>
    <td><span data-ttu-id="3d365-354">364.29</span><span class="sxs-lookup"><span data-stu-id="3d365-354">364.29</span></span></td>
    <td><span data-ttu-id="3d365-355">14</span><span class="sxs-lookup"><span data-stu-id="3d365-355">14</span></span></td>
    <td><span data-ttu-id="3d365-356">1,275.00</span><span class="sxs-lookup"><span data-stu-id="3d365-356">1,275.00</span></span></td>
    <td><span data-ttu-id="3d365-357">91.07</span><span class="sxs-lookup"><span data-stu-id="3d365-357">91.07</span></span></td>
    <td><span data-ttu-id="3d365-358">4.00</span><span class="sxs-lookup"><span data-stu-id="3d365-358">4.00</span></span></td>
    <td><span data-ttu-id="3d365-359">364.29</span><span class="sxs-lookup"><span data-stu-id="3d365-359">364.29</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="3d365-360">1000</span><span class="sxs-lookup"><span data-stu-id="3d365-360">1000</span></span></td>
    <td><span data-ttu-id="3d365-361">2</span><span class="sxs-lookup"><span data-stu-id="3d365-361">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="3d365-362">10</span><span class="sxs-lookup"><span data-stu-id="3d365-362">10</span></span></td>
    <td><span data-ttu-id="3d365-363">2,000.00</span><span class="sxs-lookup"><span data-stu-id="3d365-363">2,000.00</span></span></td>
    <td><span data-ttu-id="3d365-364">10</span><span class="sxs-lookup"><span data-stu-id="3d365-364">10</span></span></td>
    <td><span data-ttu-id="3d365-365">2,000.00</span><span class="sxs-lookup"><span data-stu-id="3d365-365">2,000.00</span></span></td>
    <td><span data-ttu-id="3d365-366">200.00</span><span class="sxs-lookup"><span data-stu-id="3d365-366">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="3d365-367">10,00</span><span class="sxs-lookup"><span data-stu-id="3d365-367">10.00</span></span></td>
    <td><span data-ttu-id="3d365-368">2,000.00</span><span class="sxs-lookup"><span data-stu-id="3d365-368">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="3d365-369"><strong>1000 Toplam</strong></span><span class="sxs-lookup"><span data-stu-id="3d365-369"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="3d365-370"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="3d365-370"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="3d365-371"><strong>3,275.00</strong></span><span class="sxs-lookup"><span data-stu-id="3d365-371"><strong>3,275.00</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="3d365-372"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="3d365-372"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="3d365-373"><strong>364.29</strong></span><span class="sxs-lookup"><span data-stu-id="3d365-373"><strong>364.29</strong></span></span></td>
    <td><span data-ttu-id="3d365-374"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="3d365-374"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="3d365-375"><strong>455.36</strong></span><span class="sxs-lookup"><span data-stu-id="3d365-375"><strong>455.36</strong></span></span></td>
    <td><span data-ttu-id="3d365-376"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="3d365-376"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="3d365-377"><strong>2,455.36</strong></span><span class="sxs-lookup"><span data-stu-id="3d365-377"><strong>2,455.36</strong></span></span></td>
</tr>
</tfoot>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]