---
title: Çift raporlama
description: Bu konu, hem Uluslararası Mali Raporlama Standardı (IFRS) hem de Varlık kiralamada yasal raporlama gereksinimlerini nasıl karşılayabileceğinizi gösteren bir örnekle size yol gösterir.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 96e1d4d460aef2f74422d5e4bd4fc68255466455
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4449000"
---
# <a name="dual-reporting"></a><span data-ttu-id="98442-103">Çift raporlama</span><span class="sxs-lookup"><span data-stu-id="98442-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98442-104">Bu konu, hem Uluslararası Mali Raporlama Standardı (IFRS) hem de Varlık kiralamada yasal raporlama gereksinimlerini nasıl karşılayabileceğinizi gösteren bir örnekle size yol gösterir.</span><span class="sxs-lookup"><span data-stu-id="98442-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="98442-105">Microsoft Dynamics 365 Finance'te deftere nakil katmanları hakında bilgi sahibi olmanız gereklidir ve örneği anlamanızı kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="98442-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="98442-106">Örnek</span><span class="sxs-lookup"><span data-stu-id="98442-106">Example</span></span>

<span data-ttu-id="98442-107">Aşağıdaki örnekte, hem nakit bazlı yöntem hem de IFRS raporlama yöntemleri kullanarak İtalya yasal raporlaması kapsamında bir kiralama ele alınır.</span><span class="sxs-lookup"><span data-stu-id="98442-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="98442-108">Şirketin hem İtalya yasal gereksinimlerini hem de IFRS 16 gereksinimlerini karşılamak için üç defter oluşturması gerekir.</span><span class="sxs-lookup"><span data-stu-id="98442-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="98442-109">Defterlerden biri IFRS 16, biri yasal gereksinimler ve biri de yasal deftere nakil işlemlerini otomatik olarak ters kaydetme için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="98442-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="98442-110">Defterler, aşağıdaki tablolarda gösterilen şekilde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="98442-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="98442-111">**IFRS 16 defteri**</span><span class="sxs-lookup"><span data-stu-id="98442-111">**IFRS 16 book**</span></span>

<span data-ttu-id="98442-112">IFRS 16 defteri, IFRS 16 muhasebe standardı ile uyumlu olacak şekilde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="98442-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="98442-113">Bu deftere nakledilecek tüm girişler, özel bir katmana nakledilir.</span><span class="sxs-lookup"><span data-stu-id="98442-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="98442-114">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="98442-114">Name</span></span>                                    | <span data-ttu-id="98442-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="98442-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="98442-116">Defter türü</span><span class="sxs-lookup"><span data-stu-id="98442-116">Book type</span></span>                               | <span data-ttu-id="98442-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="98442-117">IFRS 16</span></span>        |
| <span data-ttu-id="98442-118">Defter açıklaması</span><span class="sxs-lookup"><span data-stu-id="98442-118">Book description</span></span>                        | <span data-ttu-id="98442-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="98442-119">IFRS 16</span></span>        |
| <span data-ttu-id="98442-120">Deftere Nakletme Katmanı</span><span class="sxs-lookup"><span data-stu-id="98442-120">Posting Layer</span></span>                           | <span data-ttu-id="98442-121">Özel katman 1</span><span class="sxs-lookup"><span data-stu-id="98442-121">Custom layer 1</span></span> |
| <span data-ttu-id="98442-122">Kiralama Türü</span><span class="sxs-lookup"><span data-stu-id="98442-122">Lease Type</span></span>                              | <span data-ttu-id="98442-123">Finance</span><span class="sxs-lookup"><span data-stu-id="98442-123">Finance</span></span>        |
| <span data-ttu-id="98442-124">Muhasebe Altyapısı</span><span class="sxs-lookup"><span data-stu-id="98442-124">Accounting Framework</span></span>                    | <span data-ttu-id="98442-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="98442-125">IFRS 16</span></span>        |
| <span data-ttu-id="98442-126">Kiralama Süresi / Faydalı ömür Ayarı</span><span class="sxs-lookup"><span data-stu-id="98442-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="98442-127">0,00</span><span class="sxs-lookup"><span data-stu-id="98442-127">0.00</span></span>           |
| <span data-ttu-id="98442-128">Bugünkü Değer / Varlık Adil Değeri Ayarı</span><span class="sxs-lookup"><span data-stu-id="98442-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="98442-129">0,00</span><span class="sxs-lookup"><span data-stu-id="98442-129">0.00</span></span>           |
| <span data-ttu-id="98442-130">Kısa süre eşiği</span><span class="sxs-lookup"><span data-stu-id="98442-130">Short-term threshold</span></span>                    | <span data-ttu-id="98442-131">12</span><span class="sxs-lookup"><span data-stu-id="98442-131">12</span></span>             |
| <span data-ttu-id="98442-132">Düşük Değer Eşiği</span><span class="sxs-lookup"><span data-stu-id="98442-132">Low Value Threshold</span></span>                     | <span data-ttu-id="98442-133">5,000.00</span><span class="sxs-lookup"><span data-stu-id="98442-133">5,000.00</span></span>       |
| <span data-ttu-id="98442-134">Satıcıya Öde</span><span class="sxs-lookup"><span data-stu-id="98442-134">Pay to Vendor</span></span>                           | <span data-ttu-id="98442-135">No</span><span class="sxs-lookup"><span data-stu-id="98442-135">No</span></span>             |

<span data-ttu-id="98442-136">**Yasal defter**</span><span class="sxs-lookup"><span data-stu-id="98442-136">**Statutory book**</span></span>

<span data-ttu-id="98442-137">Yasal defter, şirketin kiralama giderini her ay kira için ödenen nakit tutarı olarak kaydedeceği nakit bazlı bir defterdir.</span><span class="sxs-lookup"><span data-stu-id="98442-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="98442-138">Bu kitap, kullanım hakkı (ROU) varlığı veya kiralama yükümlülüğü oluşturmaz.</span><span class="sxs-lookup"><span data-stu-id="98442-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="98442-139">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="98442-139">Name</span></span>                                    | <span data-ttu-id="98442-140">Tanım</span><span class="sxs-lookup"><span data-stu-id="98442-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="98442-141">Defter türü</span><span class="sxs-lookup"><span data-stu-id="98442-141">Book type</span></span>                               | <span data-ttu-id="98442-142">Yasal</span><span class="sxs-lookup"><span data-stu-id="98442-142">Statutory</span></span>   |
| <span data-ttu-id="98442-143">Defter açıklaması</span><span class="sxs-lookup"><span data-stu-id="98442-143">Book description</span></span>                        | <span data-ttu-id="98442-144">Yerel GAAP</span><span class="sxs-lookup"><span data-stu-id="98442-144">Local GAAP</span></span>  |
| <span data-ttu-id="98442-145">Deftere Nakletme Katmanı</span><span class="sxs-lookup"><span data-stu-id="98442-145">Posting Layer</span></span>                           | <span data-ttu-id="98442-146">Cari</span><span class="sxs-lookup"><span data-stu-id="98442-146">Current</span></span>     |
| <span data-ttu-id="98442-147">Kiralama Türü</span><span class="sxs-lookup"><span data-stu-id="98442-147">Lease Type</span></span>                              | <span data-ttu-id="98442-148">Otomatik</span><span class="sxs-lookup"><span data-stu-id="98442-148">Automatic</span></span>   |
| <span data-ttu-id="98442-149">Muhasebe Altyapısı</span><span class="sxs-lookup"><span data-stu-id="98442-149">Accounting Framework</span></span>                    | <span data-ttu-id="98442-150">Nakit esası</span><span class="sxs-lookup"><span data-stu-id="98442-150">Cash basis</span></span>  |
| <span data-ttu-id="98442-151">Kiralama Süresi / Faydalı ömür Ayarı</span><span class="sxs-lookup"><span data-stu-id="98442-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="98442-152">0,00</span><span class="sxs-lookup"><span data-stu-id="98442-152">0.00</span></span>        |
| <span data-ttu-id="98442-153">Bugünkü Değer / Varlık Adil Değeri Ayarı</span><span class="sxs-lookup"><span data-stu-id="98442-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="98442-154">0,00</span><span class="sxs-lookup"><span data-stu-id="98442-154">0.00</span></span>        |
| <span data-ttu-id="98442-155">Kısa süre eşiği</span><span class="sxs-lookup"><span data-stu-id="98442-155">Short-term threshold</span></span>                    | <span data-ttu-id="98442-156">0</span><span class="sxs-lookup"><span data-stu-id="98442-156">0</span></span>           |
| <span data-ttu-id="98442-157">Düşük Değer Eşiği</span><span class="sxs-lookup"><span data-stu-id="98442-157">Low Value Threshold</span></span>                     | <span data-ttu-id="98442-158">0</span><span class="sxs-lookup"><span data-stu-id="98442-158">0</span></span>           |
| <span data-ttu-id="98442-159">Satıcıya Öde</span><span class="sxs-lookup"><span data-stu-id="98442-159">Pay to Vendor</span></span>                           | <span data-ttu-id="98442-160">No</span><span class="sxs-lookup"><span data-stu-id="98442-160">No</span></span>          |

<span data-ttu-id="98442-161">**Yasal ters kayıt defteri**</span><span class="sxs-lookup"><span data-stu-id="98442-161">**Statutory reversal book**</span></span>

<span data-ttu-id="98442-162">Yasal ters kayıt defteri, yasal defterle aynı şekilde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="98442-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="98442-163">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="98442-163">Name</span></span>                                    | <span data-ttu-id="98442-164">Tanım</span><span class="sxs-lookup"><span data-stu-id="98442-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="98442-165">Defter türü</span><span class="sxs-lookup"><span data-stu-id="98442-165">Book type</span></span>                               | <span data-ttu-id="98442-166">Yasal - Ters Kayıt</span><span class="sxs-lookup"><span data-stu-id="98442-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="98442-167">Defter açıklaması</span><span class="sxs-lookup"><span data-stu-id="98442-167">Book description</span></span>                        | <span data-ttu-id="98442-168">Yasal defterin ters kaydedileceği defter</span><span class="sxs-lookup"><span data-stu-id="98442-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="98442-169">Deftere Nakletme Katmanı</span><span class="sxs-lookup"><span data-stu-id="98442-169">Posting Layer</span></span>                           | <span data-ttu-id="98442-170">Özel katman 1</span><span class="sxs-lookup"><span data-stu-id="98442-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="98442-171">Kiralama Türü</span><span class="sxs-lookup"><span data-stu-id="98442-171">Lease Type</span></span>                              | <span data-ttu-id="98442-172">Otomatik</span><span class="sxs-lookup"><span data-stu-id="98442-172">Automatic</span></span>                      |
| <span data-ttu-id="98442-173">Muhasebe Altyapısı</span><span class="sxs-lookup"><span data-stu-id="98442-173">Accounting Framework</span></span>                    | <span data-ttu-id="98442-174">Nakit esası</span><span class="sxs-lookup"><span data-stu-id="98442-174">Cash basis</span></span>                     |
| <span data-ttu-id="98442-175">Kiralama Süresi / Faydalı ömür Ayarı</span><span class="sxs-lookup"><span data-stu-id="98442-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="98442-176">0,00</span><span class="sxs-lookup"><span data-stu-id="98442-176">0.00</span></span>                           |
| <span data-ttu-id="98442-177">Bugünkü Değer / Varlık Adil Değeri Ayarı</span><span class="sxs-lookup"><span data-stu-id="98442-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="98442-178">0,00</span><span class="sxs-lookup"><span data-stu-id="98442-178">0.00</span></span>                           |
| <span data-ttu-id="98442-179">Kısa süre eşiği</span><span class="sxs-lookup"><span data-stu-id="98442-179">Short-term threshold</span></span>                    | <span data-ttu-id="98442-180">0</span><span class="sxs-lookup"><span data-stu-id="98442-180">0</span></span>                              |
| <span data-ttu-id="98442-181">Düşük Değer Eşiği</span><span class="sxs-lookup"><span data-stu-id="98442-181">Low Value Threshold</span></span>                     | <span data-ttu-id="98442-182">0</span><span class="sxs-lookup"><span data-stu-id="98442-182">0</span></span>                              |
| <span data-ttu-id="98442-183">Satıcıya Öde</span><span class="sxs-lookup"><span data-stu-id="98442-183">Pay to Vendor</span></span>                           | <span data-ttu-id="98442-184">No</span><span class="sxs-lookup"><span data-stu-id="98442-184">No</span></span>                             |

<span data-ttu-id="98442-185">Bu örnekte, **Genel** ve **Ödeme planı satırları** sekmelerinde aşağıdaki ayarlara sahip bir kiralama oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="98442-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="98442-186">**Genel sekmesi**</span><span class="sxs-lookup"><span data-stu-id="98442-186">**General tab**</span></span>

| <span data-ttu-id="98442-187">Alan</span><span class="sxs-lookup"><span data-stu-id="98442-187">Field</span></span>                      | <span data-ttu-id="98442-188">Değer</span><span class="sxs-lookup"><span data-stu-id="98442-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="98442-189">Alternatif borçlanma oranı</span><span class="sxs-lookup"><span data-stu-id="98442-189">Incremental borrowing rate</span></span> | <span data-ttu-id="98442-190">%5</span><span class="sxs-lookup"><span data-stu-id="98442-190">5%</span></span>               |
| <span data-ttu-id="98442-191">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="98442-191">Commencement date</span></span>          | <span data-ttu-id="98442-192">01.01.2020</span><span class="sxs-lookup"><span data-stu-id="98442-192">1/1/2020</span></span>         |
| <span data-ttu-id="98442-193">Kiralama grubu</span><span class="sxs-lookup"><span data-stu-id="98442-193">Lease group</span></span>                | <span data-ttu-id="98442-194">Binalar</span><span class="sxs-lookup"><span data-stu-id="98442-194">Buildings</span></span>        |
| <span data-ttu-id="98442-195">Satıcı</span><span class="sxs-lookup"><span data-stu-id="98442-195">Vendor</span></span>                     | <span data-ttu-id="98442-196">1001</span><span class="sxs-lookup"><span data-stu-id="98442-196">1001</span></span>             |
| <span data-ttu-id="98442-197">Kıymetin adil değeri</span><span class="sxs-lookup"><span data-stu-id="98442-197">Fair value of the asset</span></span>    | <span data-ttu-id="98442-198">245,000</span><span class="sxs-lookup"><span data-stu-id="98442-198">245,000</span></span>          |
| <span data-ttu-id="98442-199">Varlık faydalı ömrü</span><span class="sxs-lookup"><span data-stu-id="98442-199">Asset useful life</span></span>          | <span data-ttu-id="98442-200">120</span><span class="sxs-lookup"><span data-stu-id="98442-200">120</span></span>              |
| <span data-ttu-id="98442-201">Yıllık ödeme türü</span><span class="sxs-lookup"><span data-stu-id="98442-201">Annuity type</span></span>               | <span data-ttu-id="98442-202">Normal yıllık ödeme</span><span class="sxs-lookup"><span data-stu-id="98442-202">Ordinary annuity</span></span> |
| <span data-ttu-id="98442-203">Bileşim aralığı</span><span class="sxs-lookup"><span data-stu-id="98442-203">Compounding interval</span></span>       | <span data-ttu-id="98442-204">Monthly</span><span class="sxs-lookup"><span data-stu-id="98442-204">Monthly</span></span>          |

<span data-ttu-id="98442-205">**Ödeme planı satırları sekmesi**</span><span class="sxs-lookup"><span data-stu-id="98442-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="98442-206">Alan</span><span class="sxs-lookup"><span data-stu-id="98442-206">Field</span></span>             | <span data-ttu-id="98442-207">Değer</span><span class="sxs-lookup"><span data-stu-id="98442-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="98442-208">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="98442-208">Start date</span></span>        | <span data-ttu-id="98442-209">01.01.2020</span><span class="sxs-lookup"><span data-stu-id="98442-209">1/1/2020</span></span>   |
| <span data-ttu-id="98442-210">Dönem aralığı</span><span class="sxs-lookup"><span data-stu-id="98442-210">Period interval</span></span>   | <span data-ttu-id="98442-211">Aylar</span><span class="sxs-lookup"><span data-stu-id="98442-211">Months</span></span>     |
| <span data-ttu-id="98442-212">Dönemler</span><span class="sxs-lookup"><span data-stu-id="98442-212">Periods</span></span>           | <span data-ttu-id="98442-213">24</span><span class="sxs-lookup"><span data-stu-id="98442-213">24</span></span>         |
| <span data-ttu-id="98442-214">Bitiş tarihi</span><span class="sxs-lookup"><span data-stu-id="98442-214">End date</span></span>          | <span data-ttu-id="98442-215">31.12.2020</span><span class="sxs-lookup"><span data-stu-id="98442-215">12/31/2020</span></span> |
| <span data-ttu-id="98442-216">Ödeme sıklığı</span><span class="sxs-lookup"><span data-stu-id="98442-216">Payment frequency</span></span> | <span data-ttu-id="98442-217">Monthly</span><span class="sxs-lookup"><span data-stu-id="98442-217">Monthly</span></span>    |
| <span data-ttu-id="98442-218">Ödeme tutarı</span><span class="sxs-lookup"><span data-stu-id="98442-218">Payment amount</span></span>    | <span data-ttu-id="98442-219">1,000</span><span class="sxs-lookup"><span data-stu-id="98442-219">1,000</span></span>      |

<span data-ttu-id="98442-220">Bu kiralamayı iki altyapıda kaydetmek için geçerli deftere nakil katmanını ve özel deftere nakil katmanını kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="98442-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="98442-221">Aşağıdaki tabloda, her bir raporlama standardı kapsamında mali bilgilerin adil bir şekilde temsil edilmesini gerektiren her bir günlük girişi örneği gösterilir.</span><span class="sxs-lookup"><span data-stu-id="98442-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="98442-222">Kiralamanın ilk ayı için her bir günlük girişinin ayrıntılı açıklaması daha sonra sağlanır.</span><span class="sxs-lookup"><span data-stu-id="98442-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="98442-223">Hesap numarası</span><span class="sxs-lookup"><span data-stu-id="98442-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="98442-224">Tanım</span><span class="sxs-lookup"><span data-stu-id="98442-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="98442-225">Yasal defter (geçerli katman)</span><span class="sxs-lookup"><span data-stu-id="98442-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="98442-226">Geçerli katman toplamı</span><span class="sxs-lookup"><span data-stu-id="98442-226">Current layer total</span></span></th>
<th><span data-ttu-id="98442-227">Ters kayıt defteri (özel katman)</span><span class="sxs-lookup"><span data-stu-id="98442-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="98442-228">IFRS 16 defteri (özel katman)</span><span class="sxs-lookup"><span data-stu-id="98442-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="98442-229">Geçerli katman + özel katman toplamı</span><span class="sxs-lookup"><span data-stu-id="98442-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="98442-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="98442-230">JE-100</span></span></th>
<th><span data-ttu-id="98442-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="98442-231">JE-110</span></span></th>
<th><span data-ttu-id="98442-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="98442-232">JE-120</span></span></th>
<th><span data-ttu-id="98442-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="98442-233">JE-130</span></span></th>
<th><span data-ttu-id="98442-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="98442-234">JE-140</span></span></th>
<th><span data-ttu-id="98442-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="98442-235">JE-150</span></span></th>
<th><span data-ttu-id="98442-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="98442-236">JE-160</span></span></th>
<th><span data-ttu-id="98442-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="98442-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="98442-238">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="98442-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="98442-239">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="98442-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="98442-240">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="98442-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="98442-241">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="98442-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="98442-242">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="98442-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="98442-243">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="98442-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="98442-244">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="98442-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="98442-245">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="98442-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="98442-246">1</span><span class="sxs-lookup"><span data-stu-id="98442-246">1</span></span></td>
<td><span data-ttu-id="98442-247">Kiralama gideri</span><span class="sxs-lookup"><span data-stu-id="98442-247">Lease expense</span></span></td>
<td><span data-ttu-id="98442-248">1,000.00</span><span class="sxs-lookup"><span data-stu-id="98442-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="98442-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="98442-249">1,000.00</span></span></td>
<td><span data-ttu-id="98442-250">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="98442-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="98442-251">0,00</span><span class="sxs-lookup"><span data-stu-id="98442-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98442-252">2</span><span class="sxs-lookup"><span data-stu-id="98442-252">2</span></span></td>
<td><span data-ttu-id="98442-253">Banka masrafı</span><span class="sxs-lookup"><span data-stu-id="98442-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="98442-254">3.00</span><span class="sxs-lookup"><span data-stu-id="98442-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="98442-255">3.00</span><span class="sxs-lookup"><span data-stu-id="98442-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="98442-256">3.00</span><span class="sxs-lookup"><span data-stu-id="98442-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98442-257">3</span><span class="sxs-lookup"><span data-stu-id="98442-257">3</span></span></td>
<td><span data-ttu-id="98442-258">KDV gideri</span><span class="sxs-lookup"><span data-stu-id="98442-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="98442-259">5.00</span><span class="sxs-lookup"><span data-stu-id="98442-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="98442-260">5.00</span><span class="sxs-lookup"><span data-stu-id="98442-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="98442-261">5.00</span><span class="sxs-lookup"><span data-stu-id="98442-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98442-262">4</span><span class="sxs-lookup"><span data-stu-id="98442-262">4</span></span></td>
<td><span data-ttu-id="98442-263">Kliring hesabı</span><span class="sxs-lookup"><span data-stu-id="98442-263">Clearing account</span></span></td>
<td><span data-ttu-id="98442-264">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="98442-264">-1,000.00</span></span></td>
<td><span data-ttu-id="98442-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="98442-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="98442-266">0,00</span><span class="sxs-lookup"><span data-stu-id="98442-266">0.00</span></span></td>
<td><span data-ttu-id="98442-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="98442-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="98442-268">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="98442-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="98442-269">0,00</span><span class="sxs-lookup"><span data-stu-id="98442-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98442-270">5</span><span class="sxs-lookup"><span data-stu-id="98442-270">5</span></span></td>
<td><span data-ttu-id="98442-271">Borç hesapları</span><span class="sxs-lookup"><span data-stu-id="98442-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="98442-272">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="98442-272">-1,008.00</span></span></td>
<td><span data-ttu-id="98442-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="98442-273">1,008.00</span></span></td>
<td><span data-ttu-id="98442-274">0,00</span><span class="sxs-lookup"><span data-stu-id="98442-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="98442-275">0,00</span><span class="sxs-lookup"><span data-stu-id="98442-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98442-276">6</span><span class="sxs-lookup"><span data-stu-id="98442-276">6</span></span></td>
<td><span data-ttu-id="98442-277">ROU varlığı</span><span class="sxs-lookup"><span data-stu-id="98442-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="98442-278">0,00</span><span class="sxs-lookup"><span data-stu-id="98442-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="98442-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="98442-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="98442-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="98442-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98442-281">7</span><span class="sxs-lookup"><span data-stu-id="98442-281">7</span></span></td>
<td><span data-ttu-id="98442-282">Finansal kiralama yükümlülüğü</span><span class="sxs-lookup"><span data-stu-id="98442-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="98442-283">0,00</span><span class="sxs-lookup"><span data-stu-id="98442-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="98442-284">-22.794,00</span><span class="sxs-lookup"><span data-stu-id="98442-284">-22,794.00</span></span></td>
<td><span data-ttu-id="98442-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="98442-285">1,000.00</span></span></td>
<td><span data-ttu-id="98442-286">-94,97</span><span class="sxs-lookup"><span data-stu-id="98442-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="98442-287">-21.888,87</span><span class="sxs-lookup"><span data-stu-id="98442-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98442-288">8</span><span class="sxs-lookup"><span data-stu-id="98442-288">8</span></span></td>
<td><span data-ttu-id="98442-289">Vade farkı gideri</span><span class="sxs-lookup"><span data-stu-id="98442-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="98442-290">0,00</span><span class="sxs-lookup"><span data-stu-id="98442-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="98442-291">94.97</span><span class="sxs-lookup"><span data-stu-id="98442-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="98442-292">94.97</span><span class="sxs-lookup"><span data-stu-id="98442-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98442-293">9</span><span class="sxs-lookup"><span data-stu-id="98442-293">9</span></span></td>
<td><span data-ttu-id="98442-294">Nakit</span><span class="sxs-lookup"><span data-stu-id="98442-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="98442-295">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="98442-295">-1,008.00</span></span></td>
<td><span data-ttu-id="98442-296">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="98442-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="98442-297">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="98442-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98442-298">10</span><span class="sxs-lookup"><span data-stu-id="98442-298">10</span></span></td>
<td><span data-ttu-id="98442-299">Amortisman gideri</span><span class="sxs-lookup"><span data-stu-id="98442-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="98442-300">0,00</span><span class="sxs-lookup"><span data-stu-id="98442-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="98442-301">949.75</span><span class="sxs-lookup"><span data-stu-id="98442-301">949.75</span></span></td>
<td><span data-ttu-id="98442-302">949.75</span><span class="sxs-lookup"><span data-stu-id="98442-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98442-303">11</span><span class="sxs-lookup"><span data-stu-id="98442-303">11</span></span></td>
<td><span data-ttu-id="98442-304">Birikmiş amortisman</span><span class="sxs-lookup"><span data-stu-id="98442-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="98442-305">0,00</span><span class="sxs-lookup"><span data-stu-id="98442-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="98442-306">-949,75</span><span class="sxs-lookup"><span data-stu-id="98442-306">-949.75</span></span></td>
<td><span data-ttu-id="98442-307">-949,75</span><span class="sxs-lookup"><span data-stu-id="98442-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="98442-308">Önceki tabloda gösterildiği gibi, hem yasal raporlama hem de IFRS raporlaması kapsamında raporlamak için üç defter gereklidir.</span><span class="sxs-lookup"><span data-stu-id="98442-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="98442-309">Yasal defter, kira ödemesini, geçerli katmanda nakit bazlı muhasebe kurallarına göre kaydeder.</span><span class="sxs-lookup"><span data-stu-id="98442-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="98442-310">Yasal ters kayıt defteri, yasal günlük girişlerini ters kaydeder.</span><span class="sxs-lookup"><span data-stu-id="98442-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="98442-311">IFRS 16 defteri, IFRS 16 kapsamında gerekli olan günlük girişlerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="98442-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="98442-312">Kiralamayı yalnızca bir kez girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="98442-312">You must enter a lease only one time.</span></span> <span data-ttu-id="98442-313">Ardından, kiralamayla ilişkili tüm defterleri görmek için **Defterler** sayfasını açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="98442-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="98442-314">Defterleri oluşturduğunuzda, bunların üçü aynı kiralama kaydıyla ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="98442-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="98442-315">İlk günlük girişi, kiralama giderini yasal deftere kaydeder.</span><span class="sxs-lookup"><span data-stu-id="98442-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="98442-316">Ödemeleri toplu işte veya yasal defterdeki ödeme planını seçerek oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="98442-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="98442-317">Bu örnekte, aşağıdaki günlük girişi yasal defter için ödeme planından oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="98442-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="98442-318">Kira ödemesi – 31.01.2020 – JE 100</span><span class="sxs-lookup"><span data-stu-id="98442-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="98442-319">Hesap türü</span><span class="sxs-lookup"><span data-stu-id="98442-319">Account type</span></span> | <span data-ttu-id="98442-320">Hesap numarası</span><span class="sxs-lookup"><span data-stu-id="98442-320">Account number</span></span> | <span data-ttu-id="98442-321">Katman</span><span class="sxs-lookup"><span data-stu-id="98442-321">Layer</span></span>   | <span data-ttu-id="98442-322">Hesap açıklaması</span><span class="sxs-lookup"><span data-stu-id="98442-322">Account description</span></span> | <span data-ttu-id="98442-323">Borç</span><span class="sxs-lookup"><span data-stu-id="98442-323">Debit</span></span>    | <span data-ttu-id="98442-324">Kredi</span><span class="sxs-lookup"><span data-stu-id="98442-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="98442-325">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="98442-325">Ledger</span></span>       | <span data-ttu-id="98442-326">1</span><span class="sxs-lookup"><span data-stu-id="98442-326">1</span></span>              | <span data-ttu-id="98442-327">Cari</span><span class="sxs-lookup"><span data-stu-id="98442-327">Current</span></span> | <span data-ttu-id="98442-328">Kiralama gideri</span><span class="sxs-lookup"><span data-stu-id="98442-328">Lease expense</span></span>       | <span data-ttu-id="98442-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="98442-329">1,000.00</span></span> |          |
| <span data-ttu-id="98442-330">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="98442-330">Ledger</span></span>       | <span data-ttu-id="98442-331">4</span><span class="sxs-lookup"><span data-stu-id="98442-331">4</span></span>              | <span data-ttu-id="98442-332">Cari</span><span class="sxs-lookup"><span data-stu-id="98442-332">Current</span></span> | <span data-ttu-id="98442-333">Kliring hesabı</span><span class="sxs-lookup"><span data-stu-id="98442-333">Clearing account</span></span>    |          | <span data-ttu-id="98442-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="98442-334">1,000.00</span></span> |

<span data-ttu-id="98442-335">Borç hesapları uzmanı, Varlık kiralama dışındaki kirayı ödemek için fatura oluştururken standart Dynamics 365 işlevini kullanır.</span><span class="sxs-lookup"><span data-stu-id="98442-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="98442-336">Ancak, Borç hesapları uzmanı aşağıdaki girişi oluşturmak için borç hesabı olarak **Kiralama gideri**'ni seçmek yerine kliring hesabı seçer.</span><span class="sxs-lookup"><span data-stu-id="98442-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="98442-337">AP işlemi – 31.01.2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="98442-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="98442-338">Hesap türü</span><span class="sxs-lookup"><span data-stu-id="98442-338">Account type</span></span> | <span data-ttu-id="98442-339">Hesap numarası</span><span class="sxs-lookup"><span data-stu-id="98442-339">Account number</span></span> | <span data-ttu-id="98442-340">Katman</span><span class="sxs-lookup"><span data-stu-id="98442-340">Layer</span></span>   | <span data-ttu-id="98442-341">Hesap açıklaması</span><span class="sxs-lookup"><span data-stu-id="98442-341">Account description</span></span> | <span data-ttu-id="98442-342">Borç</span><span class="sxs-lookup"><span data-stu-id="98442-342">Debit</span></span>    | <span data-ttu-id="98442-343">Kredi</span><span class="sxs-lookup"><span data-stu-id="98442-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="98442-344">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="98442-344">Ledger</span></span>       | <span data-ttu-id="98442-345">4</span><span class="sxs-lookup"><span data-stu-id="98442-345">4</span></span>              | <span data-ttu-id="98442-346">Cari</span><span class="sxs-lookup"><span data-stu-id="98442-346">Current</span></span> | <span data-ttu-id="98442-347">Kliring hesabı</span><span class="sxs-lookup"><span data-stu-id="98442-347">Clearing account</span></span>    | <span data-ttu-id="98442-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="98442-348">1,000.00</span></span> |          |
| <span data-ttu-id="98442-349">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="98442-349">Ledger</span></span>       | <span data-ttu-id="98442-350">2</span><span class="sxs-lookup"><span data-stu-id="98442-350">2</span></span>              | <span data-ttu-id="98442-351">Cari</span><span class="sxs-lookup"><span data-stu-id="98442-351">Current</span></span> | <span data-ttu-id="98442-352">Banka masrafı</span><span class="sxs-lookup"><span data-stu-id="98442-352">Bank fee</span></span>            | <span data-ttu-id="98442-353">3.00</span><span class="sxs-lookup"><span data-stu-id="98442-353">3.00</span></span>     |          |
| <span data-ttu-id="98442-354">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="98442-354">Ledger</span></span>       | <span data-ttu-id="98442-355">3</span><span class="sxs-lookup"><span data-stu-id="98442-355">3</span></span>              | <span data-ttu-id="98442-356">Cari</span><span class="sxs-lookup"><span data-stu-id="98442-356">Current</span></span> | <span data-ttu-id="98442-357">KDV gideri</span><span class="sxs-lookup"><span data-stu-id="98442-357">VAT expense</span></span>         | <span data-ttu-id="98442-358">5.00</span><span class="sxs-lookup"><span data-stu-id="98442-358">5.00</span></span>     |          |
| <span data-ttu-id="98442-359">Satıcı</span><span class="sxs-lookup"><span data-stu-id="98442-359">Vendor</span></span>       | <span data-ttu-id="98442-360">5</span><span class="sxs-lookup"><span data-stu-id="98442-360">5</span></span>              | <span data-ttu-id="98442-361">Cari</span><span class="sxs-lookup"><span data-stu-id="98442-361">Current</span></span> | <span data-ttu-id="98442-362">Borç hesapları</span><span class="sxs-lookup"><span data-stu-id="98442-362">Accounts payable</span></span>    |          | <span data-ttu-id="98442-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="98442-363">1,008.00</span></span> |

<span data-ttu-id="98442-364">Ekstre satıcıya verildiğinde, normal ödeme sürecini takip edersiniz.</span><span class="sxs-lookup"><span data-stu-id="98442-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="98442-365">Bu işlem sırasında aşağıdaki günlük girişi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="98442-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="98442-366">Nakit ödemesi – 31.01.2020 – JE 120</span><span class="sxs-lookup"><span data-stu-id="98442-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="98442-367">Hesap türü</span><span class="sxs-lookup"><span data-stu-id="98442-367">Account type</span></span> | <span data-ttu-id="98442-368">Hesap numarası</span><span class="sxs-lookup"><span data-stu-id="98442-368">Account number</span></span> | <span data-ttu-id="98442-369">Katman</span><span class="sxs-lookup"><span data-stu-id="98442-369">Layer</span></span>   | <span data-ttu-id="98442-370">Hesap açıklaması</span><span class="sxs-lookup"><span data-stu-id="98442-370">Account description</span></span> | <span data-ttu-id="98442-371">Borç</span><span class="sxs-lookup"><span data-stu-id="98442-371">Debit</span></span>    | <span data-ttu-id="98442-372">Kredi</span><span class="sxs-lookup"><span data-stu-id="98442-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="98442-373">Satıcı</span><span class="sxs-lookup"><span data-stu-id="98442-373">Vendor</span></span>       | <span data-ttu-id="98442-374">5</span><span class="sxs-lookup"><span data-stu-id="98442-374">5</span></span>              | <span data-ttu-id="98442-375">Cari</span><span class="sxs-lookup"><span data-stu-id="98442-375">Current</span></span> | <span data-ttu-id="98442-376">Borç Hesapları</span><span class="sxs-lookup"><span data-stu-id="98442-376">Accounts Payable</span></span>    | <span data-ttu-id="98442-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="98442-377">1,008.00</span></span> |          |
| <span data-ttu-id="98442-378">Banka</span><span class="sxs-lookup"><span data-stu-id="98442-378">Bank</span></span>         | <span data-ttu-id="98442-379">9</span><span class="sxs-lookup"><span data-stu-id="98442-379">9</span></span>              | <span data-ttu-id="98442-380">Cari</span><span class="sxs-lookup"><span data-stu-id="98442-380">Current</span></span> | <span data-ttu-id="98442-381">Nakit</span><span class="sxs-lookup"><span data-stu-id="98442-381">Cash</span></span>                |          | <span data-ttu-id="98442-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="98442-382">1,008.00</span></span> |

<span data-ttu-id="98442-383">Bu aşamada, yasal raporlama gereksinimleri kaypsamında bu kiralamayı tam olarak kaydetmiş olursunuz ve geçerli katmanı kullanarak bir mizan oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="98442-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="98442-384">Sistem, aşağıdaki rakamları içeren bir mizan döndürür.</span><span class="sxs-lookup"><span data-stu-id="98442-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="98442-385">Hesap numarası</span><span class="sxs-lookup"><span data-stu-id="98442-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="98442-386">Tanım</span><span class="sxs-lookup"><span data-stu-id="98442-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="98442-387">Yasal defter (geçerli katman)</span><span class="sxs-lookup"><span data-stu-id="98442-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="98442-388">Geçerli katman toplamı</span><span class="sxs-lookup"><span data-stu-id="98442-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="98442-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="98442-389">JE-100</span></span></th>
<th><span data-ttu-id="98442-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="98442-390">JE-110</span></span></th>
<th><span data-ttu-id="98442-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="98442-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="98442-392">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="98442-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="98442-393">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="98442-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="98442-394">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="98442-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="98442-395">1</span><span class="sxs-lookup"><span data-stu-id="98442-395">1</span></span></td>
<td><span data-ttu-id="98442-396">Kiralama gideri</span><span class="sxs-lookup"><span data-stu-id="98442-396">Lease expense</span></span></td>
<td><span data-ttu-id="98442-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="98442-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="98442-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="98442-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98442-399">2</span><span class="sxs-lookup"><span data-stu-id="98442-399">2</span></span></td>
<td><span data-ttu-id="98442-400">Banka masrafı</span><span class="sxs-lookup"><span data-stu-id="98442-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="98442-401">3.00</span><span class="sxs-lookup"><span data-stu-id="98442-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="98442-402">3.00</span><span class="sxs-lookup"><span data-stu-id="98442-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98442-403">3</span><span class="sxs-lookup"><span data-stu-id="98442-403">3</span></span></td>
<td><span data-ttu-id="98442-404">KDV gideri</span><span class="sxs-lookup"><span data-stu-id="98442-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="98442-405">5.00</span><span class="sxs-lookup"><span data-stu-id="98442-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="98442-406">5.00</span><span class="sxs-lookup"><span data-stu-id="98442-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98442-407">4</span><span class="sxs-lookup"><span data-stu-id="98442-407">4</span></span></td>
<td><span data-ttu-id="98442-408">Kliring hesabı</span><span class="sxs-lookup"><span data-stu-id="98442-408">Clearing account</span></span></td>
<td><span data-ttu-id="98442-409">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="98442-409">-1,000.00</span></span></td>
<td><span data-ttu-id="98442-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="98442-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="98442-411">0,00</span><span class="sxs-lookup"><span data-stu-id="98442-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98442-412">5</span><span class="sxs-lookup"><span data-stu-id="98442-412">5</span></span></td>
<td><span data-ttu-id="98442-413">Borç hesapları</span><span class="sxs-lookup"><span data-stu-id="98442-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="98442-414">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="98442-414">-1,008.00</span></span></td>
<td><span data-ttu-id="98442-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="98442-415">1,008.00</span></span></td>
<td><span data-ttu-id="98442-416">0,00</span><span class="sxs-lookup"><span data-stu-id="98442-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98442-417">6</span><span class="sxs-lookup"><span data-stu-id="98442-417">6</span></span></td>
<td><span data-ttu-id="98442-418">ROU varlığı</span><span class="sxs-lookup"><span data-stu-id="98442-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="98442-419">0,00</span><span class="sxs-lookup"><span data-stu-id="98442-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98442-420">7</span><span class="sxs-lookup"><span data-stu-id="98442-420">7</span></span></td>
<td><span data-ttu-id="98442-421">Finansal kiralama yükümlülüğü</span><span class="sxs-lookup"><span data-stu-id="98442-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="98442-422">0,00</span><span class="sxs-lookup"><span data-stu-id="98442-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98442-423">8</span><span class="sxs-lookup"><span data-stu-id="98442-423">8</span></span></td>
<td><span data-ttu-id="98442-424">Vade farkı gideri</span><span class="sxs-lookup"><span data-stu-id="98442-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="98442-425">0,00</span><span class="sxs-lookup"><span data-stu-id="98442-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98442-426">9</span><span class="sxs-lookup"><span data-stu-id="98442-426">9</span></span></td>
<td><span data-ttu-id="98442-427">Nakit</span><span class="sxs-lookup"><span data-stu-id="98442-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="98442-428">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="98442-428">-1,008.00</span></span></td>
<td><span data-ttu-id="98442-429">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="98442-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98442-430">10</span><span class="sxs-lookup"><span data-stu-id="98442-430">10</span></span></td>
<td><span data-ttu-id="98442-431">Amortisman gideri</span><span class="sxs-lookup"><span data-stu-id="98442-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="98442-432">0,00</span><span class="sxs-lookup"><span data-stu-id="98442-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="98442-433">11</span><span class="sxs-lookup"><span data-stu-id="98442-433">11</span></span></td>
<td><span data-ttu-id="98442-434">Birikmiş amortisman</span><span class="sxs-lookup"><span data-stu-id="98442-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="98442-435">0,00</span><span class="sxs-lookup"><span data-stu-id="98442-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="98442-436">Aynı mizanı çalıştırmak için IFRS 16 rakamlarını kullanmak istiyorsanız yasal muhasebe günlük girişlerine ters kayıt işlemi uygulanmalıdır ve IFRS 16 günlük girişleri deftere nakledilmelidir.</span><span class="sxs-lookup"><span data-stu-id="98442-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="98442-437">Yasal günlük girişlerini ters kaydetmek için bu örnek, yasal defterle aynı kuruluma sahip, ancak ters bir deftere nakil profili bulunan bir yasal ters kayıt defteri içerir.</span><span class="sxs-lookup"><span data-stu-id="98442-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="98442-438">Örneğin, yasal defter bir kiralama gideri hesabını *borçlandırır* ancak ters kayıt defteri bu hesabı *alacaklandırır*.</span><span class="sxs-lookup"><span data-stu-id="98442-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="98442-439">Bu ilişkiler, **Varlık kiralama parametreleri** sayfasındaki Varlık kiralama deftere nakil hesaplarında kolayca tanımlanır (**Varlık kiralama \> Kurulum \> Varlık kiralama parametreleri**).</span><span class="sxs-lookup"><span data-stu-id="98442-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="98442-440">Yasal defter için kullanılan işlemin aynısı ters kayıt defteri için kullanılırsa aşağıdaki günlük girişi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="98442-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="98442-441">Aradaki fark, ters kayıt defterinin ters kayıt girişlerini yasal defterden kaydetmesidir.</span><span class="sxs-lookup"><span data-stu-id="98442-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="98442-442">Ters kayıt girişleri de özel katmanda yapılır.</span><span class="sxs-lookup"><span data-stu-id="98442-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="98442-443">Geçerli katmanda bir mizan çalıştırıldığında, ters kayıt günlük girişleri dahil edilmez.</span><span class="sxs-lookup"><span data-stu-id="98442-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="98442-444">Kira ödemesi – 31.01.2020 – JE 130</span><span class="sxs-lookup"><span data-stu-id="98442-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="98442-445">Hesap türü</span><span class="sxs-lookup"><span data-stu-id="98442-445">Account type</span></span> | <span data-ttu-id="98442-446">Hesap numarası</span><span class="sxs-lookup"><span data-stu-id="98442-446">Account number</span></span> | <span data-ttu-id="98442-447">Katman</span><span class="sxs-lookup"><span data-stu-id="98442-447">Layer</span></span>  | <span data-ttu-id="98442-448">Hesap açıklaması</span><span class="sxs-lookup"><span data-stu-id="98442-448">Account description</span></span> | <span data-ttu-id="98442-449">Borç</span><span class="sxs-lookup"><span data-stu-id="98442-449">Debit</span></span>    | <span data-ttu-id="98442-450">Kredi</span><span class="sxs-lookup"><span data-stu-id="98442-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="98442-451">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="98442-451">Ledger</span></span>       | <span data-ttu-id="98442-452">4</span><span class="sxs-lookup"><span data-stu-id="98442-452">4</span></span>              | <span data-ttu-id="98442-453">Özel</span><span class="sxs-lookup"><span data-stu-id="98442-453">Custom</span></span> | <span data-ttu-id="98442-454">Kliring hesabı</span><span class="sxs-lookup"><span data-stu-id="98442-454">Clearing account</span></span>    | <span data-ttu-id="98442-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="98442-455">1,000.00</span></span> |          |
| <span data-ttu-id="98442-456">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="98442-456">Ledger</span></span>       | <span data-ttu-id="98442-457">1</span><span class="sxs-lookup"><span data-stu-id="98442-457">1</span></span>              | <span data-ttu-id="98442-458">Özel</span><span class="sxs-lookup"><span data-stu-id="98442-458">Custom</span></span> | <span data-ttu-id="98442-459">Kiralama gideri</span><span class="sxs-lookup"><span data-stu-id="98442-459">Lease expense</span></span>       |          | <span data-ttu-id="98442-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="98442-460">1,000.00</span></span> |

<span data-ttu-id="98442-461">Yasal günlük girişlerini kaldırdığınıza göre IFRS 16'nın gerektirdiği tüm günlük girişlerini IFRS 16 defterine kaydedersiniz.</span><span class="sxs-lookup"><span data-stu-id="98442-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="98442-462">Bu girişler arasında ROU varlığının ve yükümlülüğün ilk kabulü ile faiz ve amortisman kaydı yer alır.</span><span class="sxs-lookup"><span data-stu-id="98442-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="98442-463">İlk kabul – 01.01.2020 – JE 140</span><span class="sxs-lookup"><span data-stu-id="98442-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="98442-464">Hesap türü</span><span class="sxs-lookup"><span data-stu-id="98442-464">Account type</span></span> | <span data-ttu-id="98442-465">Hesap numarası</span><span class="sxs-lookup"><span data-stu-id="98442-465">Account number</span></span> | <span data-ttu-id="98442-466">Katman</span><span class="sxs-lookup"><span data-stu-id="98442-466">Layer</span></span>  | <span data-ttu-id="98442-467">Hesap açıklaması</span><span class="sxs-lookup"><span data-stu-id="98442-467">Account description</span></span>      | <span data-ttu-id="98442-468">Borç</span><span class="sxs-lookup"><span data-stu-id="98442-468">Debit</span></span>     | <span data-ttu-id="98442-469">Kredi</span><span class="sxs-lookup"><span data-stu-id="98442-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="98442-470">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="98442-470">Ledger</span></span>       | <span data-ttu-id="98442-471">6</span><span class="sxs-lookup"><span data-stu-id="98442-471">6</span></span>              | <span data-ttu-id="98442-472">Özel</span><span class="sxs-lookup"><span data-stu-id="98442-472">Custom</span></span> | <span data-ttu-id="98442-473">ROU Varlığı</span><span class="sxs-lookup"><span data-stu-id="98442-473">ROU Asset</span></span>                | <span data-ttu-id="98442-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="98442-474">22,793.90</span></span> |           |
| <span data-ttu-id="98442-475">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="98442-475">Ledger</span></span>       | <span data-ttu-id="98442-476">7</span><span class="sxs-lookup"><span data-stu-id="98442-476">7</span></span>              | <span data-ttu-id="98442-477">Özel</span><span class="sxs-lookup"><span data-stu-id="98442-477">Custom</span></span> | <span data-ttu-id="98442-478">Finansal kiralama yükümlülüğü</span><span class="sxs-lookup"><span data-stu-id="98442-478">Finance lease obligation</span></span> |           | <span data-ttu-id="98442-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="98442-479">22,793.90</span></span> |

<span data-ttu-id="98442-480">Kira ödemesi diğer kira ödemeleriyle aynı şekilde deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="98442-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="98442-481">Kliring hesabının kullanılma nedeni, nakitin yalnızca bir kez alacak olarak kaydedilmesini sağlamaktır.</span><span class="sxs-lookup"><span data-stu-id="98442-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="98442-482">Kira ödemesi – 31.01.2020 – JE 150</span><span class="sxs-lookup"><span data-stu-id="98442-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="98442-483">Hesap türü</span><span class="sxs-lookup"><span data-stu-id="98442-483">Account type</span></span> | <span data-ttu-id="98442-484">Hesap numarası</span><span class="sxs-lookup"><span data-stu-id="98442-484">Account number</span></span> | <span data-ttu-id="98442-485">Katman</span><span class="sxs-lookup"><span data-stu-id="98442-485">Layer</span></span>  | <span data-ttu-id="98442-486">Hesap açıklaması</span><span class="sxs-lookup"><span data-stu-id="98442-486">Account description</span></span>      | <span data-ttu-id="98442-487">Borç</span><span class="sxs-lookup"><span data-stu-id="98442-487">Debit</span></span>    | <span data-ttu-id="98442-488">Kredi</span><span class="sxs-lookup"><span data-stu-id="98442-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="98442-489">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="98442-489">Ledger</span></span>       | <span data-ttu-id="98442-490">7</span><span class="sxs-lookup"><span data-stu-id="98442-490">7</span></span>              | <span data-ttu-id="98442-491">Özel</span><span class="sxs-lookup"><span data-stu-id="98442-491">Custom</span></span> | <span data-ttu-id="98442-492">Finansal kiralama yükümlülüğü</span><span class="sxs-lookup"><span data-stu-id="98442-492">Finance lease obligation</span></span> | <span data-ttu-id="98442-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="98442-493">1,000.00</span></span> |          |
| <span data-ttu-id="98442-494">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="98442-494">Ledger</span></span>       | <span data-ttu-id="98442-495">4</span><span class="sxs-lookup"><span data-stu-id="98442-495">4</span></span>              | <span data-ttu-id="98442-496">Özel</span><span class="sxs-lookup"><span data-stu-id="98442-496">Custom</span></span> | <span data-ttu-id="98442-497">Kliring hesabı</span><span class="sxs-lookup"><span data-stu-id="98442-497">Clearing account</span></span>         |          | <span data-ttu-id="98442-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="98442-498">1,000.00</span></span> |

<span data-ttu-id="98442-499">Faiz gideri günlüğü girişi, yükümlülük amortisman planlamasından oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="98442-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="98442-500">Faiz gideri – 31.01.2020 – JE 160</span><span class="sxs-lookup"><span data-stu-id="98442-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="98442-501">Hesap türü</span><span class="sxs-lookup"><span data-stu-id="98442-501">Account type</span></span> | <span data-ttu-id="98442-502">Hesap numarası</span><span class="sxs-lookup"><span data-stu-id="98442-502">Account number</span></span> | <span data-ttu-id="98442-503">Katman</span><span class="sxs-lookup"><span data-stu-id="98442-503">Layer</span></span>  | <span data-ttu-id="98442-504">Hesap açıklaması</span><span class="sxs-lookup"><span data-stu-id="98442-504">Account description</span></span>      | <span data-ttu-id="98442-505">Borç</span><span class="sxs-lookup"><span data-stu-id="98442-505">Debit</span></span> | <span data-ttu-id="98442-506">Kredi</span><span class="sxs-lookup"><span data-stu-id="98442-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="98442-507">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="98442-507">Ledger</span></span>       | <span data-ttu-id="98442-508">8</span><span class="sxs-lookup"><span data-stu-id="98442-508">8</span></span>              | <span data-ttu-id="98442-509">Özel</span><span class="sxs-lookup"><span data-stu-id="98442-509">Custom</span></span> | <span data-ttu-id="98442-510">Vade farkı gideri</span><span class="sxs-lookup"><span data-stu-id="98442-510">Interest expense</span></span>         | <span data-ttu-id="98442-511">94.97</span><span class="sxs-lookup"><span data-stu-id="98442-511">94.97</span></span> |        |
| <span data-ttu-id="98442-512">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="98442-512">Ledger</span></span>       | <span data-ttu-id="98442-513">7</span><span class="sxs-lookup"><span data-stu-id="98442-513">7</span></span>              | <span data-ttu-id="98442-514">Özel</span><span class="sxs-lookup"><span data-stu-id="98442-514">Custom</span></span> | <span data-ttu-id="98442-515">Finansal kiralama yükümlülüğü</span><span class="sxs-lookup"><span data-stu-id="98442-515">Finance lease obligation</span></span> |       | <span data-ttu-id="98442-516">94.97</span><span class="sxs-lookup"><span data-stu-id="98442-516">94.97</span></span>  |

<span data-ttu-id="98442-517">Amortisman gideri günlük girişi, varlık amortisman planlamasından oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="98442-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="98442-518">Amortisman gideri – 31.01.2020 – JE 170</span><span class="sxs-lookup"><span data-stu-id="98442-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="98442-519">Hesap türü</span><span class="sxs-lookup"><span data-stu-id="98442-519">Account type</span></span> | <span data-ttu-id="98442-520">Hesap numarası</span><span class="sxs-lookup"><span data-stu-id="98442-520">Account number</span></span> | <span data-ttu-id="98442-521">Katman</span><span class="sxs-lookup"><span data-stu-id="98442-521">Layer</span></span>  | <span data-ttu-id="98442-522">Hesap açıklaması</span><span class="sxs-lookup"><span data-stu-id="98442-522">Account description</span></span>      | <span data-ttu-id="98442-523">Borç</span><span class="sxs-lookup"><span data-stu-id="98442-523">Debit</span></span>  | <span data-ttu-id="98442-524">Kredi</span><span class="sxs-lookup"><span data-stu-id="98442-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="98442-525">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="98442-525">Ledger</span></span>       | <span data-ttu-id="98442-526">10</span><span class="sxs-lookup"><span data-stu-id="98442-526">10</span></span>             | <span data-ttu-id="98442-527">Özel</span><span class="sxs-lookup"><span data-stu-id="98442-527">Custom</span></span> | <span data-ttu-id="98442-528">Amortisman gideri</span><span class="sxs-lookup"><span data-stu-id="98442-528">Depreciation expense</span></span>     | <span data-ttu-id="98442-529">949.75</span><span class="sxs-lookup"><span data-stu-id="98442-529">949.75</span></span> |        |
| <span data-ttu-id="98442-530">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="98442-530">Ledger</span></span>       | <span data-ttu-id="98442-531">11</span><span class="sxs-lookup"><span data-stu-id="98442-531">11</span></span>             | <span data-ttu-id="98442-532">Özel</span><span class="sxs-lookup"><span data-stu-id="98442-532">Custom</span></span> | <span data-ttu-id="98442-533">Birikmiş amortisman</span><span class="sxs-lookup"><span data-stu-id="98442-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="98442-534">949.75</span><span class="sxs-lookup"><span data-stu-id="98442-534">949.75</span></span> |

<span data-ttu-id="98442-535">Tüm bu günlük girişleri oluşturulup deftere nakledildikten sonra, aşağıdaki "özel katman 1" değerlerini görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="98442-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="98442-536">Son sütuna banka ücreti, katma değer vergisi (KDV) gideri ve önceki katmandan nakit azaltmanın dahil olduğunu görürsünüz ancak yasal raporlama günlük girişleri dahil değildir.</span><span class="sxs-lookup"><span data-stu-id="98442-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="98442-537">Bu sayede, doğru çift raporlama özelliklerini kullanmış olursunuz.</span><span class="sxs-lookup"><span data-stu-id="98442-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="98442-538">Bu aşamada, şirketin yalnızca mizanı çalıştırması ve IFRS mizanı oluşturmak için geçerli katman ile özel katmanı birleştirmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="98442-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="98442-539">Hesap No.</span><span class="sxs-lookup"><span data-stu-id="98442-539">Account No</span></span> | <span data-ttu-id="98442-540">Tanım</span><span class="sxs-lookup"><span data-stu-id="98442-540">Description</span></span>              | <span data-ttu-id="98442-541">Yasal Defter\-Geçerli Katman\-JE\-100\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="98442-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="98442-542">Yasal Defter\-Geçerli Katman\-JE\-110\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="98442-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="98442-543">Yasal Defter\-Geçerli Katman\-JE\-120\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="98442-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="98442-544">Geçerli Katman \- Toplamlar</span><span class="sxs-lookup"><span data-stu-id="98442-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="98442-545">Ters Kayıt Defteri\-Özel katman\-JE\-130\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="98442-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="98442-546">IFRS 16 Defteri\-Özel katman\-JE\-140\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="98442-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="98442-547">IFRS 16 Defteri\-Özel katman\-JE\-150\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="98442-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="98442-548">IFRS 16 Defteri\-Özel katman\-JE\-160\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="98442-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="98442-549">IFRS 16 Defteri\-Özel katman\-JE\-170\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="98442-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="98442-550">Geçerli Katman \+ Geçerli Katman \- Toplamlar</span><span class="sxs-lookup"><span data-stu-id="98442-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="98442-551">1</span><span class="sxs-lookup"><span data-stu-id="98442-551">1</span></span>          | <span data-ttu-id="98442-552">Kiralama gideri</span><span class="sxs-lookup"><span data-stu-id="98442-552">Lease expense</span></span>            | <span data-ttu-id="98442-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="98442-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="98442-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="98442-554">1,000\.00</span></span>               |   | <span data-ttu-id="98442-555">\-1.000</span><span class="sxs-lookup"><span data-stu-id="98442-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="98442-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="98442-556">0\.00</span></span>                                   |
| <span data-ttu-id="98442-557">2</span><span class="sxs-lookup"><span data-stu-id="98442-557">2</span></span>          | <span data-ttu-id="98442-558">Banka masrafı</span><span class="sxs-lookup"><span data-stu-id="98442-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="98442-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="98442-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="98442-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="98442-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="98442-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="98442-561">3\.00</span></span>                                   |
| <span data-ttu-id="98442-562">3</span><span class="sxs-lookup"><span data-stu-id="98442-562">3</span></span>          | <span data-ttu-id="98442-563">KDV gideri</span><span class="sxs-lookup"><span data-stu-id="98442-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="98442-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="98442-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="98442-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="98442-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="98442-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="98442-566">5\.00</span></span>                                   |
| <span data-ttu-id="98442-567">4</span><span class="sxs-lookup"><span data-stu-id="98442-567">4</span></span>          | <span data-ttu-id="98442-568">Kliring hesabı</span><span class="sxs-lookup"><span data-stu-id="98442-568">Clearing account</span></span>         | <span data-ttu-id="98442-569">\-1.000\.00</span><span class="sxs-lookup"><span data-stu-id="98442-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="98442-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="98442-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="98442-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="98442-571">0\.00</span></span>                   |   | <span data-ttu-id="98442-572">1,000</span><span class="sxs-lookup"><span data-stu-id="98442-572">1,000</span></span>                                           |                                                | <span data-ttu-id="98442-573">\-1.000</span><span class="sxs-lookup"><span data-stu-id="98442-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="98442-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="98442-574">0\.00</span></span>                                   |
| <span data-ttu-id="98442-575">5</span><span class="sxs-lookup"><span data-stu-id="98442-575">5</span></span>          | <span data-ttu-id="98442-576">Borç hesapları</span><span class="sxs-lookup"><span data-stu-id="98442-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="98442-577">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="98442-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="98442-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="98442-578">1,008\.00</span></span>                                         | <span data-ttu-id="98442-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="98442-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="98442-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="98442-580">0\.00</span></span>                                   |
| <span data-ttu-id="98442-581">6</span><span class="sxs-lookup"><span data-stu-id="98442-581">6</span></span>          | <span data-ttu-id="98442-582">ROU varlığı</span><span class="sxs-lookup"><span data-stu-id="98442-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="98442-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="98442-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="98442-584">22,794</span><span class="sxs-lookup"><span data-stu-id="98442-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="98442-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="98442-585">22,793\.90</span></span>                              |
| <span data-ttu-id="98442-586">7</span><span class="sxs-lookup"><span data-stu-id="98442-586">7</span></span>          | <span data-ttu-id="98442-587">Finansal kiralama yükümlülüğü</span><span class="sxs-lookup"><span data-stu-id="98442-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="98442-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="98442-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="98442-589">\-22.794</span><span class="sxs-lookup"><span data-stu-id="98442-589">\-22,794</span></span>                                       | <span data-ttu-id="98442-590">1,000</span><span class="sxs-lookup"><span data-stu-id="98442-590">1,000</span></span>                                          | <span data-ttu-id="98442-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="98442-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="98442-592">\-21,888\.87</span><span class="sxs-lookup"><span data-stu-id="98442-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="98442-593">8</span><span class="sxs-lookup"><span data-stu-id="98442-593">8</span></span>          | <span data-ttu-id="98442-594">Vade farkı gideri</span><span class="sxs-lookup"><span data-stu-id="98442-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="98442-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="98442-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="98442-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="98442-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="98442-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="98442-597">94\.97</span></span>                                  |
| <span data-ttu-id="98442-598">9</span><span class="sxs-lookup"><span data-stu-id="98442-598">9</span></span>          | <span data-ttu-id="98442-599">Nakit</span><span class="sxs-lookup"><span data-stu-id="98442-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="98442-600">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="98442-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="98442-601">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="98442-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="98442-602">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="98442-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="98442-603">10</span><span class="sxs-lookup"><span data-stu-id="98442-603">10</span></span>         | <span data-ttu-id="98442-604">Amortisman gideri</span><span class="sxs-lookup"><span data-stu-id="98442-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="98442-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="98442-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="98442-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="98442-606">949\.75</span></span>                                        | <span data-ttu-id="98442-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="98442-607">949\.75</span></span>                                 |
| <span data-ttu-id="98442-608">11</span><span class="sxs-lookup"><span data-stu-id="98442-608">11</span></span>         | <span data-ttu-id="98442-609">Birikmiş amortisman</span><span class="sxs-lookup"><span data-stu-id="98442-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="98442-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="98442-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="98442-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="98442-611">\-949\.75</span></span>                                      | <span data-ttu-id="98442-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="98442-612">\-949\.75</span></span>                               |


