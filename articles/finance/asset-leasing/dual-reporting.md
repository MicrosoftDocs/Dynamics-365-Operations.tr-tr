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
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d6daa43178625316a40427728e7e4186691cc13c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5229562"
---
# <a name="dual-reporting"></a><span data-ttu-id="18924-103">Çift raporlama</span><span class="sxs-lookup"><span data-stu-id="18924-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="18924-104">Bu konu, hem Uluslararası Mali Raporlama Standardı (IFRS) hem de Varlık kiralamada yasal raporlama gereksinimlerini nasıl karşılayabileceğinizi gösteren bir örnekle size yol gösterir.</span><span class="sxs-lookup"><span data-stu-id="18924-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="18924-105">Microsoft Dynamics 365 Finance'te deftere nakil katmanları hakında bilgi sahibi olmanız gereklidir ve örneği anlamanızı kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="18924-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="18924-106">Örnek</span><span class="sxs-lookup"><span data-stu-id="18924-106">Example</span></span>

<span data-ttu-id="18924-107">Aşağıdaki örnekte, hem nakit bazlı yöntem hem de IFRS raporlama yöntemleri kullanarak İtalya yasal raporlaması kapsamında bir kiralama ele alınır.</span><span class="sxs-lookup"><span data-stu-id="18924-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="18924-108">Şirketin hem İtalya yasal gereksinimlerini hem de IFRS 16 gereksinimlerini karşılamak için üç defter oluşturması gerekir.</span><span class="sxs-lookup"><span data-stu-id="18924-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="18924-109">Defterlerden biri IFRS 16, biri yasal gereksinimler ve biri de yasal deftere nakil işlemlerini otomatik olarak ters kaydetme için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="18924-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="18924-110">Defterler, aşağıdaki tablolarda gösterilen şekilde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="18924-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="18924-111">**IFRS 16 defteri**</span><span class="sxs-lookup"><span data-stu-id="18924-111">**IFRS 16 book**</span></span>

<span data-ttu-id="18924-112">IFRS 16 defteri, IFRS 16 muhasebe standardı ile uyumlu olacak şekilde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="18924-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="18924-113">Bu deftere nakledilecek tüm girişler, özel bir katmana nakledilir.</span><span class="sxs-lookup"><span data-stu-id="18924-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="18924-114">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="18924-114">Name</span></span>                                    | <span data-ttu-id="18924-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="18924-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="18924-116">Defter türü</span><span class="sxs-lookup"><span data-stu-id="18924-116">Book type</span></span>                               | <span data-ttu-id="18924-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="18924-117">IFRS 16</span></span>        |
| <span data-ttu-id="18924-118">Defter açıklaması</span><span class="sxs-lookup"><span data-stu-id="18924-118">Book description</span></span>                        | <span data-ttu-id="18924-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="18924-119">IFRS 16</span></span>        |
| <span data-ttu-id="18924-120">Deftere Nakletme Katmanı</span><span class="sxs-lookup"><span data-stu-id="18924-120">Posting Layer</span></span>                           | <span data-ttu-id="18924-121">Özel katman 1</span><span class="sxs-lookup"><span data-stu-id="18924-121">Custom layer 1</span></span> |
| <span data-ttu-id="18924-122">Kiralama Türü</span><span class="sxs-lookup"><span data-stu-id="18924-122">Lease Type</span></span>                              | <span data-ttu-id="18924-123">Finance</span><span class="sxs-lookup"><span data-stu-id="18924-123">Finance</span></span>        |
| <span data-ttu-id="18924-124">Muhasebe Altyapısı</span><span class="sxs-lookup"><span data-stu-id="18924-124">Accounting Framework</span></span>                    | <span data-ttu-id="18924-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="18924-125">IFRS 16</span></span>        |
| <span data-ttu-id="18924-126">Kiralama Süresi / Faydalı ömür Ayarı</span><span class="sxs-lookup"><span data-stu-id="18924-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="18924-127">0,00</span><span class="sxs-lookup"><span data-stu-id="18924-127">0.00</span></span>           |
| <span data-ttu-id="18924-128">Bugünkü Değer / Varlık Adil Değeri Ayarı</span><span class="sxs-lookup"><span data-stu-id="18924-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="18924-129">0,00</span><span class="sxs-lookup"><span data-stu-id="18924-129">0.00</span></span>           |
| <span data-ttu-id="18924-130">Kısa süre eşiği</span><span class="sxs-lookup"><span data-stu-id="18924-130">Short-term threshold</span></span>                    | <span data-ttu-id="18924-131">12</span><span class="sxs-lookup"><span data-stu-id="18924-131">12</span></span>             |
| <span data-ttu-id="18924-132">Düşük Değer Eşiği</span><span class="sxs-lookup"><span data-stu-id="18924-132">Low Value Threshold</span></span>                     | <span data-ttu-id="18924-133">5,000.00</span><span class="sxs-lookup"><span data-stu-id="18924-133">5,000.00</span></span>       |
| <span data-ttu-id="18924-134">Satıcıya Öde</span><span class="sxs-lookup"><span data-stu-id="18924-134">Pay to Vendor</span></span>                           | <span data-ttu-id="18924-135">No</span><span class="sxs-lookup"><span data-stu-id="18924-135">No</span></span>             |

<span data-ttu-id="18924-136">**Yasal defter**</span><span class="sxs-lookup"><span data-stu-id="18924-136">**Statutory book**</span></span>

<span data-ttu-id="18924-137">Yasal defter, şirketin kiralama giderini her ay kira için ödenen nakit tutarı olarak kaydedeceği nakit bazlı bir defterdir.</span><span class="sxs-lookup"><span data-stu-id="18924-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="18924-138">Bu kitap, kullanım hakkı (ROU) varlığı veya kiralama yükümlülüğü oluşturmaz.</span><span class="sxs-lookup"><span data-stu-id="18924-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="18924-139">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="18924-139">Name</span></span>                                    | <span data-ttu-id="18924-140">Tanım</span><span class="sxs-lookup"><span data-stu-id="18924-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="18924-141">Defter türü</span><span class="sxs-lookup"><span data-stu-id="18924-141">Book type</span></span>                               | <span data-ttu-id="18924-142">Yasal</span><span class="sxs-lookup"><span data-stu-id="18924-142">Statutory</span></span>   |
| <span data-ttu-id="18924-143">Defter açıklaması</span><span class="sxs-lookup"><span data-stu-id="18924-143">Book description</span></span>                        | <span data-ttu-id="18924-144">Yerel GAAP</span><span class="sxs-lookup"><span data-stu-id="18924-144">Local GAAP</span></span>  |
| <span data-ttu-id="18924-145">Deftere Nakletme Katmanı</span><span class="sxs-lookup"><span data-stu-id="18924-145">Posting Layer</span></span>                           | <span data-ttu-id="18924-146">Cari</span><span class="sxs-lookup"><span data-stu-id="18924-146">Current</span></span>     |
| <span data-ttu-id="18924-147">Kiralama Türü</span><span class="sxs-lookup"><span data-stu-id="18924-147">Lease Type</span></span>                              | <span data-ttu-id="18924-148">Otomatik</span><span class="sxs-lookup"><span data-stu-id="18924-148">Automatic</span></span>   |
| <span data-ttu-id="18924-149">Muhasebe Altyapısı</span><span class="sxs-lookup"><span data-stu-id="18924-149">Accounting Framework</span></span>                    | <span data-ttu-id="18924-150">Nakit esası</span><span class="sxs-lookup"><span data-stu-id="18924-150">Cash basis</span></span>  |
| <span data-ttu-id="18924-151">Kiralama Süresi / Faydalı ömür Ayarı</span><span class="sxs-lookup"><span data-stu-id="18924-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="18924-152">0,00</span><span class="sxs-lookup"><span data-stu-id="18924-152">0.00</span></span>        |
| <span data-ttu-id="18924-153">Bugünkü Değer / Varlık Adil Değeri Ayarı</span><span class="sxs-lookup"><span data-stu-id="18924-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="18924-154">0,00</span><span class="sxs-lookup"><span data-stu-id="18924-154">0.00</span></span>        |
| <span data-ttu-id="18924-155">Kısa süre eşiği</span><span class="sxs-lookup"><span data-stu-id="18924-155">Short-term threshold</span></span>                    | <span data-ttu-id="18924-156">0</span><span class="sxs-lookup"><span data-stu-id="18924-156">0</span></span>           |
| <span data-ttu-id="18924-157">Düşük Değer Eşiği</span><span class="sxs-lookup"><span data-stu-id="18924-157">Low Value Threshold</span></span>                     | <span data-ttu-id="18924-158">0</span><span class="sxs-lookup"><span data-stu-id="18924-158">0</span></span>           |
| <span data-ttu-id="18924-159">Satıcıya Öde</span><span class="sxs-lookup"><span data-stu-id="18924-159">Pay to Vendor</span></span>                           | <span data-ttu-id="18924-160">No</span><span class="sxs-lookup"><span data-stu-id="18924-160">No</span></span>          |

<span data-ttu-id="18924-161">**Yasal ters kayıt defteri**</span><span class="sxs-lookup"><span data-stu-id="18924-161">**Statutory reversal book**</span></span>

<span data-ttu-id="18924-162">Yasal ters kayıt defteri, yasal defterle aynı şekilde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="18924-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="18924-163">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="18924-163">Name</span></span>                                    | <span data-ttu-id="18924-164">Tanım</span><span class="sxs-lookup"><span data-stu-id="18924-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="18924-165">Defter türü</span><span class="sxs-lookup"><span data-stu-id="18924-165">Book type</span></span>                               | <span data-ttu-id="18924-166">Yasal - Ters Kayıt</span><span class="sxs-lookup"><span data-stu-id="18924-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="18924-167">Defter açıklaması</span><span class="sxs-lookup"><span data-stu-id="18924-167">Book description</span></span>                        | <span data-ttu-id="18924-168">Yasal defterin ters kaydedileceği defter</span><span class="sxs-lookup"><span data-stu-id="18924-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="18924-169">Deftere Nakletme Katmanı</span><span class="sxs-lookup"><span data-stu-id="18924-169">Posting Layer</span></span>                           | <span data-ttu-id="18924-170">Özel katman 1</span><span class="sxs-lookup"><span data-stu-id="18924-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="18924-171">Kiralama Türü</span><span class="sxs-lookup"><span data-stu-id="18924-171">Lease Type</span></span>                              | <span data-ttu-id="18924-172">Otomatik</span><span class="sxs-lookup"><span data-stu-id="18924-172">Automatic</span></span>                      |
| <span data-ttu-id="18924-173">Muhasebe Altyapısı</span><span class="sxs-lookup"><span data-stu-id="18924-173">Accounting Framework</span></span>                    | <span data-ttu-id="18924-174">Nakit esası</span><span class="sxs-lookup"><span data-stu-id="18924-174">Cash basis</span></span>                     |
| <span data-ttu-id="18924-175">Kiralama Süresi / Faydalı ömür Ayarı</span><span class="sxs-lookup"><span data-stu-id="18924-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="18924-176">0,00</span><span class="sxs-lookup"><span data-stu-id="18924-176">0.00</span></span>                           |
| <span data-ttu-id="18924-177">Bugünkü Değer / Varlık Adil Değeri Ayarı</span><span class="sxs-lookup"><span data-stu-id="18924-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="18924-178">0,00</span><span class="sxs-lookup"><span data-stu-id="18924-178">0.00</span></span>                           |
| <span data-ttu-id="18924-179">Kısa süre eşiği</span><span class="sxs-lookup"><span data-stu-id="18924-179">Short-term threshold</span></span>                    | <span data-ttu-id="18924-180">0</span><span class="sxs-lookup"><span data-stu-id="18924-180">0</span></span>                              |
| <span data-ttu-id="18924-181">Düşük Değer Eşiği</span><span class="sxs-lookup"><span data-stu-id="18924-181">Low Value Threshold</span></span>                     | <span data-ttu-id="18924-182">0</span><span class="sxs-lookup"><span data-stu-id="18924-182">0</span></span>                              |
| <span data-ttu-id="18924-183">Satıcıya Öde</span><span class="sxs-lookup"><span data-stu-id="18924-183">Pay to Vendor</span></span>                           | <span data-ttu-id="18924-184">No</span><span class="sxs-lookup"><span data-stu-id="18924-184">No</span></span>                             |

<span data-ttu-id="18924-185">Bu örnekte, **Genel** ve **Ödeme planı satırları** sekmelerinde aşağıdaki ayarlara sahip bir kiralama oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="18924-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="18924-186">**Genel sekmesi**</span><span class="sxs-lookup"><span data-stu-id="18924-186">**General tab**</span></span>

| <span data-ttu-id="18924-187">Alan</span><span class="sxs-lookup"><span data-stu-id="18924-187">Field</span></span>                      | <span data-ttu-id="18924-188">Değer</span><span class="sxs-lookup"><span data-stu-id="18924-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="18924-189">Alternatif borçlanma oranı</span><span class="sxs-lookup"><span data-stu-id="18924-189">Incremental borrowing rate</span></span> | <span data-ttu-id="18924-190">%5</span><span class="sxs-lookup"><span data-stu-id="18924-190">5%</span></span>               |
| <span data-ttu-id="18924-191">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="18924-191">Commencement date</span></span>          | <span data-ttu-id="18924-192">01.01.2020</span><span class="sxs-lookup"><span data-stu-id="18924-192">1/1/2020</span></span>         |
| <span data-ttu-id="18924-193">Kiralama grubu</span><span class="sxs-lookup"><span data-stu-id="18924-193">Lease group</span></span>                | <span data-ttu-id="18924-194">Binalar</span><span class="sxs-lookup"><span data-stu-id="18924-194">Buildings</span></span>        |
| <span data-ttu-id="18924-195">Satıcı</span><span class="sxs-lookup"><span data-stu-id="18924-195">Vendor</span></span>                     | <span data-ttu-id="18924-196">1001</span><span class="sxs-lookup"><span data-stu-id="18924-196">1001</span></span>             |
| <span data-ttu-id="18924-197">Kıymetin adil değeri</span><span class="sxs-lookup"><span data-stu-id="18924-197">Fair value of the asset</span></span>    | <span data-ttu-id="18924-198">245,000</span><span class="sxs-lookup"><span data-stu-id="18924-198">245,000</span></span>          |
| <span data-ttu-id="18924-199">Varlık faydalı ömrü</span><span class="sxs-lookup"><span data-stu-id="18924-199">Asset useful life</span></span>          | <span data-ttu-id="18924-200">120</span><span class="sxs-lookup"><span data-stu-id="18924-200">120</span></span>              |
| <span data-ttu-id="18924-201">Yıllık ödeme türü</span><span class="sxs-lookup"><span data-stu-id="18924-201">Annuity type</span></span>               | <span data-ttu-id="18924-202">Normal yıllık ödeme</span><span class="sxs-lookup"><span data-stu-id="18924-202">Ordinary annuity</span></span> |
| <span data-ttu-id="18924-203">Bileşim aralığı</span><span class="sxs-lookup"><span data-stu-id="18924-203">Compounding interval</span></span>       | <span data-ttu-id="18924-204">Monthly</span><span class="sxs-lookup"><span data-stu-id="18924-204">Monthly</span></span>          |

<span data-ttu-id="18924-205">**Ödeme planı satırları sekmesi**</span><span class="sxs-lookup"><span data-stu-id="18924-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="18924-206">Alan</span><span class="sxs-lookup"><span data-stu-id="18924-206">Field</span></span>             | <span data-ttu-id="18924-207">Değer</span><span class="sxs-lookup"><span data-stu-id="18924-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="18924-208">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="18924-208">Start date</span></span>        | <span data-ttu-id="18924-209">01.01.2020</span><span class="sxs-lookup"><span data-stu-id="18924-209">1/1/2020</span></span>   |
| <span data-ttu-id="18924-210">Dönem aralığı</span><span class="sxs-lookup"><span data-stu-id="18924-210">Period interval</span></span>   | <span data-ttu-id="18924-211">Aylar</span><span class="sxs-lookup"><span data-stu-id="18924-211">Months</span></span>     |
| <span data-ttu-id="18924-212">Dönemler</span><span class="sxs-lookup"><span data-stu-id="18924-212">Periods</span></span>           | <span data-ttu-id="18924-213">24</span><span class="sxs-lookup"><span data-stu-id="18924-213">24</span></span>         |
| <span data-ttu-id="18924-214">Bitiş tarihi</span><span class="sxs-lookup"><span data-stu-id="18924-214">End date</span></span>          | <span data-ttu-id="18924-215">31.12.2020</span><span class="sxs-lookup"><span data-stu-id="18924-215">12/31/2020</span></span> |
| <span data-ttu-id="18924-216">Ödeme sıklığı</span><span class="sxs-lookup"><span data-stu-id="18924-216">Payment frequency</span></span> | <span data-ttu-id="18924-217">Monthly</span><span class="sxs-lookup"><span data-stu-id="18924-217">Monthly</span></span>    |
| <span data-ttu-id="18924-218">Ödeme tutarı</span><span class="sxs-lookup"><span data-stu-id="18924-218">Payment amount</span></span>    | <span data-ttu-id="18924-219">1,000</span><span class="sxs-lookup"><span data-stu-id="18924-219">1,000</span></span>      |

<span data-ttu-id="18924-220">Bu kiralamayı iki altyapıda kaydetmek için geçerli deftere nakil katmanını ve özel deftere nakil katmanını kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="18924-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="18924-221">Aşağıdaki tabloda, her bir raporlama standardı kapsamında mali bilgilerin adil bir şekilde temsil edilmesini gerektiren her bir günlük girişi örneği gösterilir.</span><span class="sxs-lookup"><span data-stu-id="18924-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="18924-222">Kiralamanın ilk ayı için her bir günlük girişinin ayrıntılı açıklaması daha sonra sağlanır.</span><span class="sxs-lookup"><span data-stu-id="18924-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="18924-223">Hesap numarası</span><span class="sxs-lookup"><span data-stu-id="18924-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="18924-224">Tanım</span><span class="sxs-lookup"><span data-stu-id="18924-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="18924-225">Yasal defter (geçerli katman)</span><span class="sxs-lookup"><span data-stu-id="18924-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="18924-226">Geçerli katman toplamı</span><span class="sxs-lookup"><span data-stu-id="18924-226">Current layer total</span></span></th>
<th><span data-ttu-id="18924-227">Ters kayıt defteri (özel katman)</span><span class="sxs-lookup"><span data-stu-id="18924-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="18924-228">IFRS 16 defteri (özel katman)</span><span class="sxs-lookup"><span data-stu-id="18924-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="18924-229">Geçerli katman + özel katman toplamı</span><span class="sxs-lookup"><span data-stu-id="18924-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="18924-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="18924-230">JE-100</span></span></th>
<th><span data-ttu-id="18924-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="18924-231">JE-110</span></span></th>
<th><span data-ttu-id="18924-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="18924-232">JE-120</span></span></th>
<th><span data-ttu-id="18924-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="18924-233">JE-130</span></span></th>
<th><span data-ttu-id="18924-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="18924-234">JE-140</span></span></th>
<th><span data-ttu-id="18924-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="18924-235">JE-150</span></span></th>
<th><span data-ttu-id="18924-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="18924-236">JE-160</span></span></th>
<th><span data-ttu-id="18924-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="18924-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="18924-238">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="18924-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="18924-239">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="18924-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="18924-240">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="18924-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="18924-241">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="18924-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="18924-242">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="18924-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="18924-243">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="18924-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="18924-244">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="18924-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="18924-245">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="18924-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="18924-246">1</span><span class="sxs-lookup"><span data-stu-id="18924-246">1</span></span></td>
<td><span data-ttu-id="18924-247">Kiralama gideri</span><span class="sxs-lookup"><span data-stu-id="18924-247">Lease expense</span></span></td>
<td><span data-ttu-id="18924-248">1,000.00</span><span class="sxs-lookup"><span data-stu-id="18924-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="18924-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="18924-249">1,000.00</span></span></td>
<td><span data-ttu-id="18924-250">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="18924-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="18924-251">0,00</span><span class="sxs-lookup"><span data-stu-id="18924-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="18924-252">2</span><span class="sxs-lookup"><span data-stu-id="18924-252">2</span></span></td>
<td><span data-ttu-id="18924-253">Banka masrafı</span><span class="sxs-lookup"><span data-stu-id="18924-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="18924-254">3.00</span><span class="sxs-lookup"><span data-stu-id="18924-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="18924-255">3.00</span><span class="sxs-lookup"><span data-stu-id="18924-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="18924-256">3.00</span><span class="sxs-lookup"><span data-stu-id="18924-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="18924-257">3</span><span class="sxs-lookup"><span data-stu-id="18924-257">3</span></span></td>
<td><span data-ttu-id="18924-258">KDV gideri</span><span class="sxs-lookup"><span data-stu-id="18924-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="18924-259">5.00</span><span class="sxs-lookup"><span data-stu-id="18924-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="18924-260">5.00</span><span class="sxs-lookup"><span data-stu-id="18924-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="18924-261">5.00</span><span class="sxs-lookup"><span data-stu-id="18924-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="18924-262">4</span><span class="sxs-lookup"><span data-stu-id="18924-262">4</span></span></td>
<td><span data-ttu-id="18924-263">Kliring hesabı</span><span class="sxs-lookup"><span data-stu-id="18924-263">Clearing account</span></span></td>
<td><span data-ttu-id="18924-264">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="18924-264">-1,000.00</span></span></td>
<td><span data-ttu-id="18924-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="18924-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="18924-266">0,00</span><span class="sxs-lookup"><span data-stu-id="18924-266">0.00</span></span></td>
<td><span data-ttu-id="18924-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="18924-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="18924-268">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="18924-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="18924-269">0,00</span><span class="sxs-lookup"><span data-stu-id="18924-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="18924-270">5</span><span class="sxs-lookup"><span data-stu-id="18924-270">5</span></span></td>
<td><span data-ttu-id="18924-271">Borç hesapları</span><span class="sxs-lookup"><span data-stu-id="18924-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="18924-272">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="18924-272">-1,008.00</span></span></td>
<td><span data-ttu-id="18924-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="18924-273">1,008.00</span></span></td>
<td><span data-ttu-id="18924-274">0,00</span><span class="sxs-lookup"><span data-stu-id="18924-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="18924-275">0,00</span><span class="sxs-lookup"><span data-stu-id="18924-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="18924-276">6</span><span class="sxs-lookup"><span data-stu-id="18924-276">6</span></span></td>
<td><span data-ttu-id="18924-277">ROU varlığı</span><span class="sxs-lookup"><span data-stu-id="18924-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="18924-278">0,00</span><span class="sxs-lookup"><span data-stu-id="18924-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="18924-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="18924-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="18924-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="18924-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="18924-281">7</span><span class="sxs-lookup"><span data-stu-id="18924-281">7</span></span></td>
<td><span data-ttu-id="18924-282">Finansal kiralama yükümlülüğü</span><span class="sxs-lookup"><span data-stu-id="18924-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="18924-283">0,00</span><span class="sxs-lookup"><span data-stu-id="18924-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="18924-284">-22.794,00</span><span class="sxs-lookup"><span data-stu-id="18924-284">-22,794.00</span></span></td>
<td><span data-ttu-id="18924-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="18924-285">1,000.00</span></span></td>
<td><span data-ttu-id="18924-286">-94,97</span><span class="sxs-lookup"><span data-stu-id="18924-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="18924-287">-21.888,87</span><span class="sxs-lookup"><span data-stu-id="18924-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="18924-288">8</span><span class="sxs-lookup"><span data-stu-id="18924-288">8</span></span></td>
<td><span data-ttu-id="18924-289">Vade farkı gideri</span><span class="sxs-lookup"><span data-stu-id="18924-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="18924-290">0,00</span><span class="sxs-lookup"><span data-stu-id="18924-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="18924-291">94.97</span><span class="sxs-lookup"><span data-stu-id="18924-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="18924-292">94.97</span><span class="sxs-lookup"><span data-stu-id="18924-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="18924-293">9</span><span class="sxs-lookup"><span data-stu-id="18924-293">9</span></span></td>
<td><span data-ttu-id="18924-294">Nakit</span><span class="sxs-lookup"><span data-stu-id="18924-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="18924-295">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="18924-295">-1,008.00</span></span></td>
<td><span data-ttu-id="18924-296">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="18924-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="18924-297">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="18924-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="18924-298">10</span><span class="sxs-lookup"><span data-stu-id="18924-298">10</span></span></td>
<td><span data-ttu-id="18924-299">Amortisman gideri</span><span class="sxs-lookup"><span data-stu-id="18924-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="18924-300">0,00</span><span class="sxs-lookup"><span data-stu-id="18924-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="18924-301">949.75</span><span class="sxs-lookup"><span data-stu-id="18924-301">949.75</span></span></td>
<td><span data-ttu-id="18924-302">949.75</span><span class="sxs-lookup"><span data-stu-id="18924-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="18924-303">11</span><span class="sxs-lookup"><span data-stu-id="18924-303">11</span></span></td>
<td><span data-ttu-id="18924-304">Birikmiş amortisman</span><span class="sxs-lookup"><span data-stu-id="18924-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="18924-305">0,00</span><span class="sxs-lookup"><span data-stu-id="18924-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="18924-306">-949,75</span><span class="sxs-lookup"><span data-stu-id="18924-306">-949.75</span></span></td>
<td><span data-ttu-id="18924-307">-949,75</span><span class="sxs-lookup"><span data-stu-id="18924-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="18924-308">Önceki tabloda gösterildiği gibi, hem yasal raporlama hem de IFRS raporlaması kapsamında raporlamak için üç defter gereklidir.</span><span class="sxs-lookup"><span data-stu-id="18924-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="18924-309">Yasal defter, kira ödemesini, geçerli katmanda nakit bazlı muhasebe kurallarına göre kaydeder.</span><span class="sxs-lookup"><span data-stu-id="18924-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="18924-310">Yasal ters kayıt defteri, yasal günlük girişlerini ters kaydeder.</span><span class="sxs-lookup"><span data-stu-id="18924-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="18924-311">IFRS 16 defteri, IFRS 16 kapsamında gerekli olan günlük girişlerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="18924-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="18924-312">Kiralamayı yalnızca bir kez girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="18924-312">You must enter a lease only one time.</span></span> <span data-ttu-id="18924-313">Ardından, kiralamayla ilişkili tüm defterleri görmek için **Defterler** sayfasını açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="18924-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="18924-314">Defterleri oluşturduğunuzda, bunların üçü aynı kiralama kaydıyla ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="18924-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="18924-315">İlk günlük girişi, kiralama giderini yasal deftere kaydeder.</span><span class="sxs-lookup"><span data-stu-id="18924-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="18924-316">Ödemeleri toplu işte veya yasal defterdeki ödeme planını seçerek oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="18924-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="18924-317">Bu örnekte, aşağıdaki günlük girişi yasal defter için ödeme planından oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="18924-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="18924-318">Kira ödemesi – 31.01.2020 – JE 100</span><span class="sxs-lookup"><span data-stu-id="18924-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="18924-319">Hesap türü</span><span class="sxs-lookup"><span data-stu-id="18924-319">Account type</span></span> | <span data-ttu-id="18924-320">Hesap numarası</span><span class="sxs-lookup"><span data-stu-id="18924-320">Account number</span></span> | <span data-ttu-id="18924-321">Katman</span><span class="sxs-lookup"><span data-stu-id="18924-321">Layer</span></span>   | <span data-ttu-id="18924-322">Hesap açıklaması</span><span class="sxs-lookup"><span data-stu-id="18924-322">Account description</span></span> | <span data-ttu-id="18924-323">Borç</span><span class="sxs-lookup"><span data-stu-id="18924-323">Debit</span></span>    | <span data-ttu-id="18924-324">Kredi</span><span class="sxs-lookup"><span data-stu-id="18924-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="18924-325">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="18924-325">Ledger</span></span>       | <span data-ttu-id="18924-326">1</span><span class="sxs-lookup"><span data-stu-id="18924-326">1</span></span>              | <span data-ttu-id="18924-327">Cari</span><span class="sxs-lookup"><span data-stu-id="18924-327">Current</span></span> | <span data-ttu-id="18924-328">Kiralama gideri</span><span class="sxs-lookup"><span data-stu-id="18924-328">Lease expense</span></span>       | <span data-ttu-id="18924-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="18924-329">1,000.00</span></span> |          |
| <span data-ttu-id="18924-330">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="18924-330">Ledger</span></span>       | <span data-ttu-id="18924-331">4</span><span class="sxs-lookup"><span data-stu-id="18924-331">4</span></span>              | <span data-ttu-id="18924-332">Cari</span><span class="sxs-lookup"><span data-stu-id="18924-332">Current</span></span> | <span data-ttu-id="18924-333">Kliring hesabı</span><span class="sxs-lookup"><span data-stu-id="18924-333">Clearing account</span></span>    |          | <span data-ttu-id="18924-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="18924-334">1,000.00</span></span> |

<span data-ttu-id="18924-335">Borç hesapları uzmanı, Varlık kiralama dışındaki kirayı ödemek için fatura oluştururken standart Dynamics 365 işlevini kullanır.</span><span class="sxs-lookup"><span data-stu-id="18924-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="18924-336">Ancak, Borç hesapları uzmanı aşağıdaki girişi oluşturmak için borç hesabı olarak **Kiralama gideri**'ni seçmek yerine kliring hesabı seçer.</span><span class="sxs-lookup"><span data-stu-id="18924-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="18924-337">AP işlemi – 31.01.2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="18924-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="18924-338">Hesap türü</span><span class="sxs-lookup"><span data-stu-id="18924-338">Account type</span></span> | <span data-ttu-id="18924-339">Hesap numarası</span><span class="sxs-lookup"><span data-stu-id="18924-339">Account number</span></span> | <span data-ttu-id="18924-340">Katman</span><span class="sxs-lookup"><span data-stu-id="18924-340">Layer</span></span>   | <span data-ttu-id="18924-341">Hesap açıklaması</span><span class="sxs-lookup"><span data-stu-id="18924-341">Account description</span></span> | <span data-ttu-id="18924-342">Borç</span><span class="sxs-lookup"><span data-stu-id="18924-342">Debit</span></span>    | <span data-ttu-id="18924-343">Kredi</span><span class="sxs-lookup"><span data-stu-id="18924-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="18924-344">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="18924-344">Ledger</span></span>       | <span data-ttu-id="18924-345">4</span><span class="sxs-lookup"><span data-stu-id="18924-345">4</span></span>              | <span data-ttu-id="18924-346">Cari</span><span class="sxs-lookup"><span data-stu-id="18924-346">Current</span></span> | <span data-ttu-id="18924-347">Kliring hesabı</span><span class="sxs-lookup"><span data-stu-id="18924-347">Clearing account</span></span>    | <span data-ttu-id="18924-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="18924-348">1,000.00</span></span> |          |
| <span data-ttu-id="18924-349">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="18924-349">Ledger</span></span>       | <span data-ttu-id="18924-350">2</span><span class="sxs-lookup"><span data-stu-id="18924-350">2</span></span>              | <span data-ttu-id="18924-351">Cari</span><span class="sxs-lookup"><span data-stu-id="18924-351">Current</span></span> | <span data-ttu-id="18924-352">Banka masrafı</span><span class="sxs-lookup"><span data-stu-id="18924-352">Bank fee</span></span>            | <span data-ttu-id="18924-353">3.00</span><span class="sxs-lookup"><span data-stu-id="18924-353">3.00</span></span>     |          |
| <span data-ttu-id="18924-354">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="18924-354">Ledger</span></span>       | <span data-ttu-id="18924-355">3</span><span class="sxs-lookup"><span data-stu-id="18924-355">3</span></span>              | <span data-ttu-id="18924-356">Cari</span><span class="sxs-lookup"><span data-stu-id="18924-356">Current</span></span> | <span data-ttu-id="18924-357">KDV gideri</span><span class="sxs-lookup"><span data-stu-id="18924-357">VAT expense</span></span>         | <span data-ttu-id="18924-358">5.00</span><span class="sxs-lookup"><span data-stu-id="18924-358">5.00</span></span>     |          |
| <span data-ttu-id="18924-359">Satıcı</span><span class="sxs-lookup"><span data-stu-id="18924-359">Vendor</span></span>       | <span data-ttu-id="18924-360">5</span><span class="sxs-lookup"><span data-stu-id="18924-360">5</span></span>              | <span data-ttu-id="18924-361">Cari</span><span class="sxs-lookup"><span data-stu-id="18924-361">Current</span></span> | <span data-ttu-id="18924-362">Borç hesapları</span><span class="sxs-lookup"><span data-stu-id="18924-362">Accounts payable</span></span>    |          | <span data-ttu-id="18924-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="18924-363">1,008.00</span></span> |

<span data-ttu-id="18924-364">Ekstre satıcıya verildiğinde, normal ödeme sürecini takip edersiniz.</span><span class="sxs-lookup"><span data-stu-id="18924-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="18924-365">Bu işlem sırasında aşağıdaki günlük girişi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="18924-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="18924-366">Nakit ödemesi – 31.01.2020 – JE 120</span><span class="sxs-lookup"><span data-stu-id="18924-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="18924-367">Hesap türü</span><span class="sxs-lookup"><span data-stu-id="18924-367">Account type</span></span> | <span data-ttu-id="18924-368">Hesap numarası</span><span class="sxs-lookup"><span data-stu-id="18924-368">Account number</span></span> | <span data-ttu-id="18924-369">Katman</span><span class="sxs-lookup"><span data-stu-id="18924-369">Layer</span></span>   | <span data-ttu-id="18924-370">Hesap açıklaması</span><span class="sxs-lookup"><span data-stu-id="18924-370">Account description</span></span> | <span data-ttu-id="18924-371">Borç</span><span class="sxs-lookup"><span data-stu-id="18924-371">Debit</span></span>    | <span data-ttu-id="18924-372">Kredi</span><span class="sxs-lookup"><span data-stu-id="18924-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="18924-373">Satıcı</span><span class="sxs-lookup"><span data-stu-id="18924-373">Vendor</span></span>       | <span data-ttu-id="18924-374">5</span><span class="sxs-lookup"><span data-stu-id="18924-374">5</span></span>              | <span data-ttu-id="18924-375">Cari</span><span class="sxs-lookup"><span data-stu-id="18924-375">Current</span></span> | <span data-ttu-id="18924-376">Borç Hesapları</span><span class="sxs-lookup"><span data-stu-id="18924-376">Accounts Payable</span></span>    | <span data-ttu-id="18924-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="18924-377">1,008.00</span></span> |          |
| <span data-ttu-id="18924-378">Banka</span><span class="sxs-lookup"><span data-stu-id="18924-378">Bank</span></span>         | <span data-ttu-id="18924-379">9</span><span class="sxs-lookup"><span data-stu-id="18924-379">9</span></span>              | <span data-ttu-id="18924-380">Cari</span><span class="sxs-lookup"><span data-stu-id="18924-380">Current</span></span> | <span data-ttu-id="18924-381">Nakit</span><span class="sxs-lookup"><span data-stu-id="18924-381">Cash</span></span>                |          | <span data-ttu-id="18924-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="18924-382">1,008.00</span></span> |

<span data-ttu-id="18924-383">Bu aşamada, yasal raporlama gereksinimleri kaypsamında bu kiralamayı tam olarak kaydetmiş olursunuz ve geçerli katmanı kullanarak bir mizan oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="18924-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="18924-384">Sistem, aşağıdaki rakamları içeren bir mizan döndürür.</span><span class="sxs-lookup"><span data-stu-id="18924-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="18924-385">Hesap numarası</span><span class="sxs-lookup"><span data-stu-id="18924-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="18924-386">Tanım</span><span class="sxs-lookup"><span data-stu-id="18924-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="18924-387">Yasal defter (geçerli katman)</span><span class="sxs-lookup"><span data-stu-id="18924-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="18924-388">Geçerli katman toplamı</span><span class="sxs-lookup"><span data-stu-id="18924-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="18924-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="18924-389">JE-100</span></span></th>
<th><span data-ttu-id="18924-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="18924-390">JE-110</span></span></th>
<th><span data-ttu-id="18924-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="18924-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="18924-392">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="18924-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="18924-393">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="18924-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="18924-394">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="18924-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="18924-395">1</span><span class="sxs-lookup"><span data-stu-id="18924-395">1</span></span></td>
<td><span data-ttu-id="18924-396">Kiralama gideri</span><span class="sxs-lookup"><span data-stu-id="18924-396">Lease expense</span></span></td>
<td><span data-ttu-id="18924-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="18924-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="18924-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="18924-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="18924-399">2</span><span class="sxs-lookup"><span data-stu-id="18924-399">2</span></span></td>
<td><span data-ttu-id="18924-400">Banka masrafı</span><span class="sxs-lookup"><span data-stu-id="18924-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="18924-401">3.00</span><span class="sxs-lookup"><span data-stu-id="18924-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="18924-402">3.00</span><span class="sxs-lookup"><span data-stu-id="18924-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="18924-403">3</span><span class="sxs-lookup"><span data-stu-id="18924-403">3</span></span></td>
<td><span data-ttu-id="18924-404">KDV gideri</span><span class="sxs-lookup"><span data-stu-id="18924-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="18924-405">5.00</span><span class="sxs-lookup"><span data-stu-id="18924-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="18924-406">5.00</span><span class="sxs-lookup"><span data-stu-id="18924-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="18924-407">4</span><span class="sxs-lookup"><span data-stu-id="18924-407">4</span></span></td>
<td><span data-ttu-id="18924-408">Kliring hesabı</span><span class="sxs-lookup"><span data-stu-id="18924-408">Clearing account</span></span></td>
<td><span data-ttu-id="18924-409">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="18924-409">-1,000.00</span></span></td>
<td><span data-ttu-id="18924-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="18924-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="18924-411">0,00</span><span class="sxs-lookup"><span data-stu-id="18924-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="18924-412">5</span><span class="sxs-lookup"><span data-stu-id="18924-412">5</span></span></td>
<td><span data-ttu-id="18924-413">Borç hesapları</span><span class="sxs-lookup"><span data-stu-id="18924-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="18924-414">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="18924-414">-1,008.00</span></span></td>
<td><span data-ttu-id="18924-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="18924-415">1,008.00</span></span></td>
<td><span data-ttu-id="18924-416">0,00</span><span class="sxs-lookup"><span data-stu-id="18924-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="18924-417">6</span><span class="sxs-lookup"><span data-stu-id="18924-417">6</span></span></td>
<td><span data-ttu-id="18924-418">ROU varlığı</span><span class="sxs-lookup"><span data-stu-id="18924-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="18924-419">0,00</span><span class="sxs-lookup"><span data-stu-id="18924-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="18924-420">7</span><span class="sxs-lookup"><span data-stu-id="18924-420">7</span></span></td>
<td><span data-ttu-id="18924-421">Finansal kiralama yükümlülüğü</span><span class="sxs-lookup"><span data-stu-id="18924-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="18924-422">0,00</span><span class="sxs-lookup"><span data-stu-id="18924-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="18924-423">8</span><span class="sxs-lookup"><span data-stu-id="18924-423">8</span></span></td>
<td><span data-ttu-id="18924-424">Vade farkı gideri</span><span class="sxs-lookup"><span data-stu-id="18924-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="18924-425">0,00</span><span class="sxs-lookup"><span data-stu-id="18924-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="18924-426">9</span><span class="sxs-lookup"><span data-stu-id="18924-426">9</span></span></td>
<td><span data-ttu-id="18924-427">Nakit</span><span class="sxs-lookup"><span data-stu-id="18924-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="18924-428">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="18924-428">-1,008.00</span></span></td>
<td><span data-ttu-id="18924-429">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="18924-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="18924-430">10</span><span class="sxs-lookup"><span data-stu-id="18924-430">10</span></span></td>
<td><span data-ttu-id="18924-431">Amortisman gideri</span><span class="sxs-lookup"><span data-stu-id="18924-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="18924-432">0,00</span><span class="sxs-lookup"><span data-stu-id="18924-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="18924-433">11</span><span class="sxs-lookup"><span data-stu-id="18924-433">11</span></span></td>
<td><span data-ttu-id="18924-434">Birikmiş amortisman</span><span class="sxs-lookup"><span data-stu-id="18924-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="18924-435">0,00</span><span class="sxs-lookup"><span data-stu-id="18924-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="18924-436">Aynı mizanı çalıştırmak için IFRS 16 rakamlarını kullanmak istiyorsanız yasal muhasebe günlük girişlerine ters kayıt işlemi uygulanmalıdır ve IFRS 16 günlük girişleri deftere nakledilmelidir.</span><span class="sxs-lookup"><span data-stu-id="18924-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="18924-437">Yasal günlük girişlerini ters kaydetmek için bu örnek, yasal defterle aynı kuruluma sahip, ancak ters bir deftere nakil profili bulunan bir yasal ters kayıt defteri içerir.</span><span class="sxs-lookup"><span data-stu-id="18924-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="18924-438">Örneğin, yasal defter bir kiralama gideri hesabını *borçlandırır* ancak ters kayıt defteri bu hesabı *alacaklandırır*.</span><span class="sxs-lookup"><span data-stu-id="18924-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="18924-439">Bu ilişkiler, **Varlık kiralama parametreleri** sayfasındaki Varlık kiralama deftere nakil hesaplarında kolayca tanımlanır (**Varlık kiralama \> Kurulum \> Varlık kiralama parametreleri**).</span><span class="sxs-lookup"><span data-stu-id="18924-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="18924-440">Yasal defter için kullanılan işlemin aynısı ters kayıt defteri için kullanılırsa aşağıdaki günlük girişi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="18924-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="18924-441">Aradaki fark, ters kayıt defterinin ters kayıt girişlerini yasal defterden kaydetmesidir.</span><span class="sxs-lookup"><span data-stu-id="18924-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="18924-442">Ters kayıt girişleri de özel katmanda yapılır.</span><span class="sxs-lookup"><span data-stu-id="18924-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="18924-443">Geçerli katmanda bir mizan çalıştırıldığında, ters kayıt günlük girişleri dahil edilmez.</span><span class="sxs-lookup"><span data-stu-id="18924-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="18924-444">Kira ödemesi – 31.01.2020 – JE 130</span><span class="sxs-lookup"><span data-stu-id="18924-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="18924-445">Hesap türü</span><span class="sxs-lookup"><span data-stu-id="18924-445">Account type</span></span> | <span data-ttu-id="18924-446">Hesap numarası</span><span class="sxs-lookup"><span data-stu-id="18924-446">Account number</span></span> | <span data-ttu-id="18924-447">Katman</span><span class="sxs-lookup"><span data-stu-id="18924-447">Layer</span></span>  | <span data-ttu-id="18924-448">Hesap açıklaması</span><span class="sxs-lookup"><span data-stu-id="18924-448">Account description</span></span> | <span data-ttu-id="18924-449">Borç</span><span class="sxs-lookup"><span data-stu-id="18924-449">Debit</span></span>    | <span data-ttu-id="18924-450">Kredi</span><span class="sxs-lookup"><span data-stu-id="18924-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="18924-451">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="18924-451">Ledger</span></span>       | <span data-ttu-id="18924-452">4</span><span class="sxs-lookup"><span data-stu-id="18924-452">4</span></span>              | <span data-ttu-id="18924-453">Özel</span><span class="sxs-lookup"><span data-stu-id="18924-453">Custom</span></span> | <span data-ttu-id="18924-454">Kliring hesabı</span><span class="sxs-lookup"><span data-stu-id="18924-454">Clearing account</span></span>    | <span data-ttu-id="18924-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="18924-455">1,000.00</span></span> |          |
| <span data-ttu-id="18924-456">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="18924-456">Ledger</span></span>       | <span data-ttu-id="18924-457">1</span><span class="sxs-lookup"><span data-stu-id="18924-457">1</span></span>              | <span data-ttu-id="18924-458">Özel</span><span class="sxs-lookup"><span data-stu-id="18924-458">Custom</span></span> | <span data-ttu-id="18924-459">Kiralama gideri</span><span class="sxs-lookup"><span data-stu-id="18924-459">Lease expense</span></span>       |          | <span data-ttu-id="18924-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="18924-460">1,000.00</span></span> |

<span data-ttu-id="18924-461">Yasal günlük girişlerini kaldırdığınıza göre IFRS 16'nın gerektirdiği tüm günlük girişlerini IFRS 16 defterine kaydedersiniz.</span><span class="sxs-lookup"><span data-stu-id="18924-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="18924-462">Bu girişler arasında ROU varlığının ve yükümlülüğün ilk kabulü ile faiz ve amortisman kaydı yer alır.</span><span class="sxs-lookup"><span data-stu-id="18924-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="18924-463">İlk kabul – 01.01.2020 – JE 140</span><span class="sxs-lookup"><span data-stu-id="18924-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="18924-464">Hesap türü</span><span class="sxs-lookup"><span data-stu-id="18924-464">Account type</span></span> | <span data-ttu-id="18924-465">Hesap numarası</span><span class="sxs-lookup"><span data-stu-id="18924-465">Account number</span></span> | <span data-ttu-id="18924-466">Katman</span><span class="sxs-lookup"><span data-stu-id="18924-466">Layer</span></span>  | <span data-ttu-id="18924-467">Hesap açıklaması</span><span class="sxs-lookup"><span data-stu-id="18924-467">Account description</span></span>      | <span data-ttu-id="18924-468">Borç</span><span class="sxs-lookup"><span data-stu-id="18924-468">Debit</span></span>     | <span data-ttu-id="18924-469">Kredi</span><span class="sxs-lookup"><span data-stu-id="18924-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="18924-470">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="18924-470">Ledger</span></span>       | <span data-ttu-id="18924-471">6</span><span class="sxs-lookup"><span data-stu-id="18924-471">6</span></span>              | <span data-ttu-id="18924-472">Özel</span><span class="sxs-lookup"><span data-stu-id="18924-472">Custom</span></span> | <span data-ttu-id="18924-473">ROU Varlığı</span><span class="sxs-lookup"><span data-stu-id="18924-473">ROU Asset</span></span>                | <span data-ttu-id="18924-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="18924-474">22,793.90</span></span> |           |
| <span data-ttu-id="18924-475">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="18924-475">Ledger</span></span>       | <span data-ttu-id="18924-476">7</span><span class="sxs-lookup"><span data-stu-id="18924-476">7</span></span>              | <span data-ttu-id="18924-477">Özel</span><span class="sxs-lookup"><span data-stu-id="18924-477">Custom</span></span> | <span data-ttu-id="18924-478">Finansal kiralama yükümlülüğü</span><span class="sxs-lookup"><span data-stu-id="18924-478">Finance lease obligation</span></span> |           | <span data-ttu-id="18924-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="18924-479">22,793.90</span></span> |

<span data-ttu-id="18924-480">Kira ödemesi diğer kira ödemeleriyle aynı şekilde deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="18924-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="18924-481">Kliring hesabının kullanılma nedeni, nakitin yalnızca bir kez alacak olarak kaydedilmesini sağlamaktır.</span><span class="sxs-lookup"><span data-stu-id="18924-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="18924-482">Kira ödemesi – 31.01.2020 – JE 150</span><span class="sxs-lookup"><span data-stu-id="18924-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="18924-483">Hesap türü</span><span class="sxs-lookup"><span data-stu-id="18924-483">Account type</span></span> | <span data-ttu-id="18924-484">Hesap numarası</span><span class="sxs-lookup"><span data-stu-id="18924-484">Account number</span></span> | <span data-ttu-id="18924-485">Katman</span><span class="sxs-lookup"><span data-stu-id="18924-485">Layer</span></span>  | <span data-ttu-id="18924-486">Hesap açıklaması</span><span class="sxs-lookup"><span data-stu-id="18924-486">Account description</span></span>      | <span data-ttu-id="18924-487">Borç</span><span class="sxs-lookup"><span data-stu-id="18924-487">Debit</span></span>    | <span data-ttu-id="18924-488">Kredi</span><span class="sxs-lookup"><span data-stu-id="18924-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="18924-489">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="18924-489">Ledger</span></span>       | <span data-ttu-id="18924-490">7</span><span class="sxs-lookup"><span data-stu-id="18924-490">7</span></span>              | <span data-ttu-id="18924-491">Özel</span><span class="sxs-lookup"><span data-stu-id="18924-491">Custom</span></span> | <span data-ttu-id="18924-492">Finansal kiralama yükümlülüğü</span><span class="sxs-lookup"><span data-stu-id="18924-492">Finance lease obligation</span></span> | <span data-ttu-id="18924-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="18924-493">1,000.00</span></span> |          |
| <span data-ttu-id="18924-494">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="18924-494">Ledger</span></span>       | <span data-ttu-id="18924-495">4</span><span class="sxs-lookup"><span data-stu-id="18924-495">4</span></span>              | <span data-ttu-id="18924-496">Özel</span><span class="sxs-lookup"><span data-stu-id="18924-496">Custom</span></span> | <span data-ttu-id="18924-497">Kliring hesabı</span><span class="sxs-lookup"><span data-stu-id="18924-497">Clearing account</span></span>         |          | <span data-ttu-id="18924-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="18924-498">1,000.00</span></span> |

<span data-ttu-id="18924-499">Faiz gideri günlüğü girişi, yükümlülük amortisman planlamasından oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="18924-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="18924-500">Faiz gideri – 31.01.2020 – JE 160</span><span class="sxs-lookup"><span data-stu-id="18924-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="18924-501">Hesap türü</span><span class="sxs-lookup"><span data-stu-id="18924-501">Account type</span></span> | <span data-ttu-id="18924-502">Hesap numarası</span><span class="sxs-lookup"><span data-stu-id="18924-502">Account number</span></span> | <span data-ttu-id="18924-503">Katman</span><span class="sxs-lookup"><span data-stu-id="18924-503">Layer</span></span>  | <span data-ttu-id="18924-504">Hesap açıklaması</span><span class="sxs-lookup"><span data-stu-id="18924-504">Account description</span></span>      | <span data-ttu-id="18924-505">Borç</span><span class="sxs-lookup"><span data-stu-id="18924-505">Debit</span></span> | <span data-ttu-id="18924-506">Kredi</span><span class="sxs-lookup"><span data-stu-id="18924-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="18924-507">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="18924-507">Ledger</span></span>       | <span data-ttu-id="18924-508">8</span><span class="sxs-lookup"><span data-stu-id="18924-508">8</span></span>              | <span data-ttu-id="18924-509">Özel</span><span class="sxs-lookup"><span data-stu-id="18924-509">Custom</span></span> | <span data-ttu-id="18924-510">Vade farkı gideri</span><span class="sxs-lookup"><span data-stu-id="18924-510">Interest expense</span></span>         | <span data-ttu-id="18924-511">94.97</span><span class="sxs-lookup"><span data-stu-id="18924-511">94.97</span></span> |        |
| <span data-ttu-id="18924-512">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="18924-512">Ledger</span></span>       | <span data-ttu-id="18924-513">7</span><span class="sxs-lookup"><span data-stu-id="18924-513">7</span></span>              | <span data-ttu-id="18924-514">Özel</span><span class="sxs-lookup"><span data-stu-id="18924-514">Custom</span></span> | <span data-ttu-id="18924-515">Finansal kiralama yükümlülüğü</span><span class="sxs-lookup"><span data-stu-id="18924-515">Finance lease obligation</span></span> |       | <span data-ttu-id="18924-516">94.97</span><span class="sxs-lookup"><span data-stu-id="18924-516">94.97</span></span>  |

<span data-ttu-id="18924-517">Amortisman gideri günlük girişi, varlık amortisman planlamasından oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="18924-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="18924-518">Amortisman gideri – 31.01.2020 – JE 170</span><span class="sxs-lookup"><span data-stu-id="18924-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="18924-519">Hesap türü</span><span class="sxs-lookup"><span data-stu-id="18924-519">Account type</span></span> | <span data-ttu-id="18924-520">Hesap numarası</span><span class="sxs-lookup"><span data-stu-id="18924-520">Account number</span></span> | <span data-ttu-id="18924-521">Katman</span><span class="sxs-lookup"><span data-stu-id="18924-521">Layer</span></span>  | <span data-ttu-id="18924-522">Hesap açıklaması</span><span class="sxs-lookup"><span data-stu-id="18924-522">Account description</span></span>      | <span data-ttu-id="18924-523">Borç</span><span class="sxs-lookup"><span data-stu-id="18924-523">Debit</span></span>  | <span data-ttu-id="18924-524">Kredi</span><span class="sxs-lookup"><span data-stu-id="18924-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="18924-525">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="18924-525">Ledger</span></span>       | <span data-ttu-id="18924-526">10</span><span class="sxs-lookup"><span data-stu-id="18924-526">10</span></span>             | <span data-ttu-id="18924-527">Özel</span><span class="sxs-lookup"><span data-stu-id="18924-527">Custom</span></span> | <span data-ttu-id="18924-528">Amortisman gideri</span><span class="sxs-lookup"><span data-stu-id="18924-528">Depreciation expense</span></span>     | <span data-ttu-id="18924-529">949.75</span><span class="sxs-lookup"><span data-stu-id="18924-529">949.75</span></span> |        |
| <span data-ttu-id="18924-530">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="18924-530">Ledger</span></span>       | <span data-ttu-id="18924-531">11</span><span class="sxs-lookup"><span data-stu-id="18924-531">11</span></span>             | <span data-ttu-id="18924-532">Özel</span><span class="sxs-lookup"><span data-stu-id="18924-532">Custom</span></span> | <span data-ttu-id="18924-533">Birikmiş amortisman</span><span class="sxs-lookup"><span data-stu-id="18924-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="18924-534">949.75</span><span class="sxs-lookup"><span data-stu-id="18924-534">949.75</span></span> |

<span data-ttu-id="18924-535">Tüm bu günlük girişleri oluşturulup deftere nakledildikten sonra, aşağıdaki "özel katman 1" değerlerini görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="18924-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="18924-536">Son sütuna banka ücreti, katma değer vergisi (KDV) gideri ve önceki katmandan nakit azaltmanın dahil olduğunu görürsünüz ancak yasal raporlama günlük girişleri dahil değildir.</span><span class="sxs-lookup"><span data-stu-id="18924-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="18924-537">Bu sayede, doğru çift raporlama özelliklerini kullanmış olursunuz.</span><span class="sxs-lookup"><span data-stu-id="18924-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="18924-538">Bu aşamada, şirketin yalnızca mizanı çalıştırması ve IFRS mizanı oluşturmak için geçerli katman ile özel katmanı birleştirmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="18924-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="18924-539">Hesap No.</span><span class="sxs-lookup"><span data-stu-id="18924-539">Account No</span></span> | <span data-ttu-id="18924-540">Tanım</span><span class="sxs-lookup"><span data-stu-id="18924-540">Description</span></span>              | <span data-ttu-id="18924-541">Yasal Defter\-Geçerli Katman\-JE\-100\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="18924-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="18924-542">Yasal Defter\-Geçerli Katman\-JE\-110\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="18924-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="18924-543">Yasal Defter\-Geçerli Katman\-JE\-120\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="18924-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="18924-544">Geçerli Katman \- Toplamlar</span><span class="sxs-lookup"><span data-stu-id="18924-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="18924-545">Ters Kayıt Defteri\-Özel katman\-JE\-130\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="18924-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="18924-546">IFRS 16 Defteri\-Özel katman\-JE\-140\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="18924-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="18924-547">IFRS 16 Defteri\-Özel katman\-JE\-150\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="18924-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="18924-548">IFRS 16 Defteri\-Özel katman\-JE\-160\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="18924-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="18924-549">IFRS 16 Defteri\-Özel katman\-JE\-170\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="18924-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="18924-550">Geçerli Katman \+ Geçerli Katman \- Toplamlar</span><span class="sxs-lookup"><span data-stu-id="18924-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="18924-551">1</span><span class="sxs-lookup"><span data-stu-id="18924-551">1</span></span>          | <span data-ttu-id="18924-552">Kiralama gideri</span><span class="sxs-lookup"><span data-stu-id="18924-552">Lease expense</span></span>            | <span data-ttu-id="18924-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="18924-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="18924-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="18924-554">1,000\.00</span></span>               |   | <span data-ttu-id="18924-555">\-1.000</span><span class="sxs-lookup"><span data-stu-id="18924-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="18924-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="18924-556">0\.00</span></span>                                   |
| <span data-ttu-id="18924-557">2</span><span class="sxs-lookup"><span data-stu-id="18924-557">2</span></span>          | <span data-ttu-id="18924-558">Banka masrafı</span><span class="sxs-lookup"><span data-stu-id="18924-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="18924-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="18924-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="18924-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="18924-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="18924-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="18924-561">3\.00</span></span>                                   |
| <span data-ttu-id="18924-562">3</span><span class="sxs-lookup"><span data-stu-id="18924-562">3</span></span>          | <span data-ttu-id="18924-563">KDV gideri</span><span class="sxs-lookup"><span data-stu-id="18924-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="18924-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="18924-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="18924-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="18924-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="18924-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="18924-566">5\.00</span></span>                                   |
| <span data-ttu-id="18924-567">4</span><span class="sxs-lookup"><span data-stu-id="18924-567">4</span></span>          | <span data-ttu-id="18924-568">Kliring hesabı</span><span class="sxs-lookup"><span data-stu-id="18924-568">Clearing account</span></span>         | <span data-ttu-id="18924-569">\-1.000\.00</span><span class="sxs-lookup"><span data-stu-id="18924-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="18924-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="18924-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="18924-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="18924-571">0\.00</span></span>                   |   | <span data-ttu-id="18924-572">1,000</span><span class="sxs-lookup"><span data-stu-id="18924-572">1,000</span></span>                                           |                                                | <span data-ttu-id="18924-573">\-1.000</span><span class="sxs-lookup"><span data-stu-id="18924-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="18924-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="18924-574">0\.00</span></span>                                   |
| <span data-ttu-id="18924-575">5</span><span class="sxs-lookup"><span data-stu-id="18924-575">5</span></span>          | <span data-ttu-id="18924-576">Borç hesapları</span><span class="sxs-lookup"><span data-stu-id="18924-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="18924-577">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="18924-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="18924-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="18924-578">1,008\.00</span></span>                                         | <span data-ttu-id="18924-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="18924-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="18924-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="18924-580">0\.00</span></span>                                   |
| <span data-ttu-id="18924-581">6</span><span class="sxs-lookup"><span data-stu-id="18924-581">6</span></span>          | <span data-ttu-id="18924-582">ROU varlığı</span><span class="sxs-lookup"><span data-stu-id="18924-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="18924-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="18924-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="18924-584">22,794</span><span class="sxs-lookup"><span data-stu-id="18924-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="18924-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="18924-585">22,793\.90</span></span>                              |
| <span data-ttu-id="18924-586">7</span><span class="sxs-lookup"><span data-stu-id="18924-586">7</span></span>          | <span data-ttu-id="18924-587">Finansal kiralama yükümlülüğü</span><span class="sxs-lookup"><span data-stu-id="18924-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="18924-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="18924-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="18924-589">\-22.794</span><span class="sxs-lookup"><span data-stu-id="18924-589">\-22,794</span></span>                                       | <span data-ttu-id="18924-590">1,000</span><span class="sxs-lookup"><span data-stu-id="18924-590">1,000</span></span>                                          | <span data-ttu-id="18924-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="18924-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="18924-592">\-21,888\.87</span><span class="sxs-lookup"><span data-stu-id="18924-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="18924-593">8</span><span class="sxs-lookup"><span data-stu-id="18924-593">8</span></span>          | <span data-ttu-id="18924-594">Vade farkı gideri</span><span class="sxs-lookup"><span data-stu-id="18924-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="18924-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="18924-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="18924-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="18924-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="18924-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="18924-597">94\.97</span></span>                                  |
| <span data-ttu-id="18924-598">9</span><span class="sxs-lookup"><span data-stu-id="18924-598">9</span></span>          | <span data-ttu-id="18924-599">Nakit</span><span class="sxs-lookup"><span data-stu-id="18924-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="18924-600">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="18924-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="18924-601">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="18924-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="18924-602">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="18924-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="18924-603">10</span><span class="sxs-lookup"><span data-stu-id="18924-603">10</span></span>         | <span data-ttu-id="18924-604">Amortisman gideri</span><span class="sxs-lookup"><span data-stu-id="18924-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="18924-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="18924-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="18924-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="18924-606">949\.75</span></span>                                        | <span data-ttu-id="18924-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="18924-607">949\.75</span></span>                                 |
| <span data-ttu-id="18924-608">11</span><span class="sxs-lookup"><span data-stu-id="18924-608">11</span></span>         | <span data-ttu-id="18924-609">Birikmiş amortisman</span><span class="sxs-lookup"><span data-stu-id="18924-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="18924-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="18924-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="18924-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="18924-611">\-949\.75</span></span>                                      | <span data-ttu-id="18924-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="18924-612">\-949\.75</span></span>                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]