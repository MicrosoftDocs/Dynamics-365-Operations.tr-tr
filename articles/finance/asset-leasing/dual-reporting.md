---
title: Çift raporlama
description: Bu konu, hem Uluslararası Mali Raporlama Standardı (IFRS) hem de Varlık kiralamada yasal raporlama gereksinimlerini nasıl karşılayabileceğinizi gösteren bir örnekle size yol gösterir.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseBookMaster
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 86f42f8db707f3b8c62b9ec4c39ad6464f080748
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881168"
---
# <a name="dual-reporting"></a><span data-ttu-id="9cf23-103">Çift raporlama</span><span class="sxs-lookup"><span data-stu-id="9cf23-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9cf23-104">Bu konu, hem Uluslararası Mali Raporlama Standardı (IFRS) hem de Varlık kiralamada yasal raporlama gereksinimlerini nasıl karşılayabileceğinizi gösteren bir örnekle size yol gösterir.</span><span class="sxs-lookup"><span data-stu-id="9cf23-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="9cf23-105">Microsoft Dynamics 365 Finance'te deftere nakil katmanları hakında bilgi sahibi olmanız gereklidir ve örneği anlamanızı kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="9cf23-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="9cf23-106">Örnek</span><span class="sxs-lookup"><span data-stu-id="9cf23-106">Example</span></span>

<span data-ttu-id="9cf23-107">Aşağıdaki örnekte, hem nakit bazlı yöntem hem de IFRS raporlama yöntemleri kullanarak İtalya yasal raporlaması kapsamında bir kiralama ele alınır.</span><span class="sxs-lookup"><span data-stu-id="9cf23-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="9cf23-108">Şirketin hem İtalya yasal gereksinimlerini hem de IFRS 16 gereksinimlerini karşılamak için üç defter oluşturması gerekir.</span><span class="sxs-lookup"><span data-stu-id="9cf23-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="9cf23-109">Defterlerden biri IFRS 16, biri yasal gereksinimler ve biri de yasal deftere nakil işlemlerini otomatik olarak ters kaydetme için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="9cf23-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="9cf23-110">Defterler, aşağıdaki tablolarda gösterilen şekilde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="9cf23-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="9cf23-111">**IFRS 16 defteri**</span><span class="sxs-lookup"><span data-stu-id="9cf23-111">**IFRS 16 book**</span></span>

<span data-ttu-id="9cf23-112">IFRS 16 defteri, IFRS 16 muhasebe standardı ile uyumlu olacak şekilde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="9cf23-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="9cf23-113">Bu deftere nakledilecek tüm girişler, özel bir katmana nakledilir.</span><span class="sxs-lookup"><span data-stu-id="9cf23-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="9cf23-114">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="9cf23-114">Name</span></span>                                    | <span data-ttu-id="9cf23-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="9cf23-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="9cf23-116">Defter türü</span><span class="sxs-lookup"><span data-stu-id="9cf23-116">Book type</span></span>                               | <span data-ttu-id="9cf23-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="9cf23-117">IFRS 16</span></span>        |
| <span data-ttu-id="9cf23-118">Defter açıklaması</span><span class="sxs-lookup"><span data-stu-id="9cf23-118">Book description</span></span>                        | <span data-ttu-id="9cf23-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="9cf23-119">IFRS 16</span></span>        |
| <span data-ttu-id="9cf23-120">Deftere Nakletme Katmanı</span><span class="sxs-lookup"><span data-stu-id="9cf23-120">Posting Layer</span></span>                           | <span data-ttu-id="9cf23-121">Özel katman 1</span><span class="sxs-lookup"><span data-stu-id="9cf23-121">Custom layer 1</span></span> |
| <span data-ttu-id="9cf23-122">Kiralama Türü</span><span class="sxs-lookup"><span data-stu-id="9cf23-122">Lease Type</span></span>                              | <span data-ttu-id="9cf23-123">Finance</span><span class="sxs-lookup"><span data-stu-id="9cf23-123">Finance</span></span>        |
| <span data-ttu-id="9cf23-124">Muhasebe Altyapısı</span><span class="sxs-lookup"><span data-stu-id="9cf23-124">Accounting Framework</span></span>                    | <span data-ttu-id="9cf23-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="9cf23-125">IFRS 16</span></span>        |
| <span data-ttu-id="9cf23-126">Kiralama Süresi / Faydalı ömür Ayarı</span><span class="sxs-lookup"><span data-stu-id="9cf23-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="9cf23-127">0,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-127">0.00</span></span>           |
| <span data-ttu-id="9cf23-128">Bugünkü Değer / Varlık Adil Değeri Ayarı</span><span class="sxs-lookup"><span data-stu-id="9cf23-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="9cf23-129">0,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-129">0.00</span></span>           |
| <span data-ttu-id="9cf23-130">Kısa süre eşiği</span><span class="sxs-lookup"><span data-stu-id="9cf23-130">Short-term threshold</span></span>                    | <span data-ttu-id="9cf23-131">12</span><span class="sxs-lookup"><span data-stu-id="9cf23-131">12</span></span>             |
| <span data-ttu-id="9cf23-132">Düşük Değer Eşiği</span><span class="sxs-lookup"><span data-stu-id="9cf23-132">Low Value Threshold</span></span>                     | <span data-ttu-id="9cf23-133">5,000.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-133">5,000.00</span></span>       |
| <span data-ttu-id="9cf23-134">Satıcıya Öde</span><span class="sxs-lookup"><span data-stu-id="9cf23-134">Pay to Vendor</span></span>                           | <span data-ttu-id="9cf23-135">No</span><span class="sxs-lookup"><span data-stu-id="9cf23-135">No</span></span>             |

<span data-ttu-id="9cf23-136">**Yasal defter**</span><span class="sxs-lookup"><span data-stu-id="9cf23-136">**Statutory book**</span></span>

<span data-ttu-id="9cf23-137">Yasal defter, şirketin kiralama giderini her ay kira için ödenen nakit tutarı olarak kaydedeceği nakit bazlı bir defterdir.</span><span class="sxs-lookup"><span data-stu-id="9cf23-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="9cf23-138">Bu kitap, kullanım hakkı (ROU) varlığı veya kiralama yükümlülüğü oluşturmaz.</span><span class="sxs-lookup"><span data-stu-id="9cf23-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="9cf23-139">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="9cf23-139">Name</span></span>                                    | <span data-ttu-id="9cf23-140">Tanım</span><span class="sxs-lookup"><span data-stu-id="9cf23-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="9cf23-141">Defter türü</span><span class="sxs-lookup"><span data-stu-id="9cf23-141">Book type</span></span>                               | <span data-ttu-id="9cf23-142">Yasal</span><span class="sxs-lookup"><span data-stu-id="9cf23-142">Statutory</span></span>   |
| <span data-ttu-id="9cf23-143">Defter açıklaması</span><span class="sxs-lookup"><span data-stu-id="9cf23-143">Book description</span></span>                        | <span data-ttu-id="9cf23-144">Yerel GAAP</span><span class="sxs-lookup"><span data-stu-id="9cf23-144">Local GAAP</span></span>  |
| <span data-ttu-id="9cf23-145">Deftere Nakletme Katmanı</span><span class="sxs-lookup"><span data-stu-id="9cf23-145">Posting Layer</span></span>                           | <span data-ttu-id="9cf23-146">Cari</span><span class="sxs-lookup"><span data-stu-id="9cf23-146">Current</span></span>     |
| <span data-ttu-id="9cf23-147">Kiralama Türü</span><span class="sxs-lookup"><span data-stu-id="9cf23-147">Lease Type</span></span>                              | <span data-ttu-id="9cf23-148">Otomatik</span><span class="sxs-lookup"><span data-stu-id="9cf23-148">Automatic</span></span>   |
| <span data-ttu-id="9cf23-149">Muhasebe Altyapısı</span><span class="sxs-lookup"><span data-stu-id="9cf23-149">Accounting Framework</span></span>                    | <span data-ttu-id="9cf23-150">Nakit esası</span><span class="sxs-lookup"><span data-stu-id="9cf23-150">Cash basis</span></span>  |
| <span data-ttu-id="9cf23-151">Kiralama Süresi / Faydalı ömür Ayarı</span><span class="sxs-lookup"><span data-stu-id="9cf23-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="9cf23-152">0,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-152">0.00</span></span>        |
| <span data-ttu-id="9cf23-153">Bugünkü Değer / Varlık Adil Değeri Ayarı</span><span class="sxs-lookup"><span data-stu-id="9cf23-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="9cf23-154">0,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-154">0.00</span></span>        |
| <span data-ttu-id="9cf23-155">Kısa süre eşiği</span><span class="sxs-lookup"><span data-stu-id="9cf23-155">Short-term threshold</span></span>                    | <span data-ttu-id="9cf23-156">0</span><span class="sxs-lookup"><span data-stu-id="9cf23-156">0</span></span>           |
| <span data-ttu-id="9cf23-157">Düşük Değer Eşiği</span><span class="sxs-lookup"><span data-stu-id="9cf23-157">Low Value Threshold</span></span>                     | <span data-ttu-id="9cf23-158">0</span><span class="sxs-lookup"><span data-stu-id="9cf23-158">0</span></span>           |
| <span data-ttu-id="9cf23-159">Satıcıya Öde</span><span class="sxs-lookup"><span data-stu-id="9cf23-159">Pay to Vendor</span></span>                           | <span data-ttu-id="9cf23-160">No</span><span class="sxs-lookup"><span data-stu-id="9cf23-160">No</span></span>          |

<span data-ttu-id="9cf23-161">**Yasal ters kayıt defteri**</span><span class="sxs-lookup"><span data-stu-id="9cf23-161">**Statutory reversal book**</span></span>

<span data-ttu-id="9cf23-162">Yasal ters kayıt defteri, yasal defterle aynı şekilde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="9cf23-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="9cf23-163">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="9cf23-163">Name</span></span>                                    | <span data-ttu-id="9cf23-164">Tanım</span><span class="sxs-lookup"><span data-stu-id="9cf23-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="9cf23-165">Defter türü</span><span class="sxs-lookup"><span data-stu-id="9cf23-165">Book type</span></span>                               | <span data-ttu-id="9cf23-166">Yasal - Ters Kayıt</span><span class="sxs-lookup"><span data-stu-id="9cf23-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="9cf23-167">Defter açıklaması</span><span class="sxs-lookup"><span data-stu-id="9cf23-167">Book description</span></span>                        | <span data-ttu-id="9cf23-168">Yasal defterin ters kaydedileceği defter</span><span class="sxs-lookup"><span data-stu-id="9cf23-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="9cf23-169">Deftere Nakletme Katmanı</span><span class="sxs-lookup"><span data-stu-id="9cf23-169">Posting Layer</span></span>                           | <span data-ttu-id="9cf23-170">Özel katman 1</span><span class="sxs-lookup"><span data-stu-id="9cf23-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="9cf23-171">Kiralama Türü</span><span class="sxs-lookup"><span data-stu-id="9cf23-171">Lease Type</span></span>                              | <span data-ttu-id="9cf23-172">Otomatik</span><span class="sxs-lookup"><span data-stu-id="9cf23-172">Automatic</span></span>                      |
| <span data-ttu-id="9cf23-173">Muhasebe Altyapısı</span><span class="sxs-lookup"><span data-stu-id="9cf23-173">Accounting Framework</span></span>                    | <span data-ttu-id="9cf23-174">Nakit esası</span><span class="sxs-lookup"><span data-stu-id="9cf23-174">Cash basis</span></span>                     |
| <span data-ttu-id="9cf23-175">Kiralama Süresi / Faydalı ömür Ayarı</span><span class="sxs-lookup"><span data-stu-id="9cf23-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="9cf23-176">0,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-176">0.00</span></span>                           |
| <span data-ttu-id="9cf23-177">Bugünkü Değer / Varlık Adil Değeri Ayarı</span><span class="sxs-lookup"><span data-stu-id="9cf23-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="9cf23-178">0,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-178">0.00</span></span>                           |
| <span data-ttu-id="9cf23-179">Kısa süre eşiği</span><span class="sxs-lookup"><span data-stu-id="9cf23-179">Short-term threshold</span></span>                    | <span data-ttu-id="9cf23-180">0</span><span class="sxs-lookup"><span data-stu-id="9cf23-180">0</span></span>                              |
| <span data-ttu-id="9cf23-181">Düşük Değer Eşiği</span><span class="sxs-lookup"><span data-stu-id="9cf23-181">Low Value Threshold</span></span>                     | <span data-ttu-id="9cf23-182">0</span><span class="sxs-lookup"><span data-stu-id="9cf23-182">0</span></span>                              |
| <span data-ttu-id="9cf23-183">Satıcıya Öde</span><span class="sxs-lookup"><span data-stu-id="9cf23-183">Pay to Vendor</span></span>                           | <span data-ttu-id="9cf23-184">No</span><span class="sxs-lookup"><span data-stu-id="9cf23-184">No</span></span>                             |

<span data-ttu-id="9cf23-185">Bu örnekte, **Genel** ve **Ödeme planı satırları** sekmelerinde aşağıdaki ayarlara sahip bir kiralama oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="9cf23-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="9cf23-186">**Genel sekmesi**</span><span class="sxs-lookup"><span data-stu-id="9cf23-186">**General tab**</span></span>

| <span data-ttu-id="9cf23-187">Alan</span><span class="sxs-lookup"><span data-stu-id="9cf23-187">Field</span></span>                      | <span data-ttu-id="9cf23-188">Değer</span><span class="sxs-lookup"><span data-stu-id="9cf23-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="9cf23-189">Alternatif borçlanma oranı</span><span class="sxs-lookup"><span data-stu-id="9cf23-189">Incremental borrowing rate</span></span> | <span data-ttu-id="9cf23-190">%5</span><span class="sxs-lookup"><span data-stu-id="9cf23-190">5%</span></span>               |
| <span data-ttu-id="9cf23-191">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="9cf23-191">Commencement date</span></span>          | <span data-ttu-id="9cf23-192">01.01.2020</span><span class="sxs-lookup"><span data-stu-id="9cf23-192">1/1/2020</span></span>         |
| <span data-ttu-id="9cf23-193">Kiralama grubu</span><span class="sxs-lookup"><span data-stu-id="9cf23-193">Lease group</span></span>                | <span data-ttu-id="9cf23-194">Binalar</span><span class="sxs-lookup"><span data-stu-id="9cf23-194">Buildings</span></span>        |
| <span data-ttu-id="9cf23-195">Satıcı</span><span class="sxs-lookup"><span data-stu-id="9cf23-195">Vendor</span></span>                     | <span data-ttu-id="9cf23-196">1001</span><span class="sxs-lookup"><span data-stu-id="9cf23-196">1001</span></span>             |
| <span data-ttu-id="9cf23-197">Kıymetin adil değeri</span><span class="sxs-lookup"><span data-stu-id="9cf23-197">Fair value of the asset</span></span>    | <span data-ttu-id="9cf23-198">245,000</span><span class="sxs-lookup"><span data-stu-id="9cf23-198">245,000</span></span>          |
| <span data-ttu-id="9cf23-199">Varlık faydalı ömrü</span><span class="sxs-lookup"><span data-stu-id="9cf23-199">Asset useful life</span></span>          | <span data-ttu-id="9cf23-200">120</span><span class="sxs-lookup"><span data-stu-id="9cf23-200">120</span></span>              |
| <span data-ttu-id="9cf23-201">Yıllık ödeme türü</span><span class="sxs-lookup"><span data-stu-id="9cf23-201">Annuity type</span></span>               | <span data-ttu-id="9cf23-202">Normal yıllık ödeme</span><span class="sxs-lookup"><span data-stu-id="9cf23-202">Ordinary annuity</span></span> |
| <span data-ttu-id="9cf23-203">Bileşim aralığı</span><span class="sxs-lookup"><span data-stu-id="9cf23-203">Compounding interval</span></span>       | <span data-ttu-id="9cf23-204">Monthly</span><span class="sxs-lookup"><span data-stu-id="9cf23-204">Monthly</span></span>          |

<span data-ttu-id="9cf23-205">**Ödeme planı satırları sekmesi**</span><span class="sxs-lookup"><span data-stu-id="9cf23-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="9cf23-206">Alan</span><span class="sxs-lookup"><span data-stu-id="9cf23-206">Field</span></span>             | <span data-ttu-id="9cf23-207">Değer</span><span class="sxs-lookup"><span data-stu-id="9cf23-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="9cf23-208">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="9cf23-208">Start date</span></span>        | <span data-ttu-id="9cf23-209">01.01.2020</span><span class="sxs-lookup"><span data-stu-id="9cf23-209">1/1/2020</span></span>   |
| <span data-ttu-id="9cf23-210">Dönem aralığı</span><span class="sxs-lookup"><span data-stu-id="9cf23-210">Period interval</span></span>   | <span data-ttu-id="9cf23-211">Aylar</span><span class="sxs-lookup"><span data-stu-id="9cf23-211">Months</span></span>     |
| <span data-ttu-id="9cf23-212">Dönemler</span><span class="sxs-lookup"><span data-stu-id="9cf23-212">Periods</span></span>           | <span data-ttu-id="9cf23-213">24</span><span class="sxs-lookup"><span data-stu-id="9cf23-213">24</span></span>         |
| <span data-ttu-id="9cf23-214">Bitiş tarihi</span><span class="sxs-lookup"><span data-stu-id="9cf23-214">End date</span></span>          | <span data-ttu-id="9cf23-215">31.12.2020</span><span class="sxs-lookup"><span data-stu-id="9cf23-215">12/31/2020</span></span> |
| <span data-ttu-id="9cf23-216">Ödeme sıklığı</span><span class="sxs-lookup"><span data-stu-id="9cf23-216">Payment frequency</span></span> | <span data-ttu-id="9cf23-217">Monthly</span><span class="sxs-lookup"><span data-stu-id="9cf23-217">Monthly</span></span>    |
| <span data-ttu-id="9cf23-218">Ödeme tutarı</span><span class="sxs-lookup"><span data-stu-id="9cf23-218">Payment amount</span></span>    | <span data-ttu-id="9cf23-219">1,000</span><span class="sxs-lookup"><span data-stu-id="9cf23-219">1,000</span></span>      |

<span data-ttu-id="9cf23-220">Bu kiralamayı iki altyapıda kaydetmek için geçerli deftere nakil katmanını ve özel deftere nakil katmanını kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="9cf23-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="9cf23-221">Aşağıdaki tabloda, her bir raporlama standardı kapsamında mali bilgilerin adil bir şekilde temsil edilmesini gerektiren her bir günlük girişi örneği gösterilir.</span><span class="sxs-lookup"><span data-stu-id="9cf23-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="9cf23-222">Kiralamanın ilk ayı için her bir günlük girişinin ayrıntılı açıklaması daha sonra sağlanır.</span><span class="sxs-lookup"><span data-stu-id="9cf23-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="9cf23-223">Hesap numarası</span><span class="sxs-lookup"><span data-stu-id="9cf23-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="9cf23-224">Tanım</span><span class="sxs-lookup"><span data-stu-id="9cf23-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="9cf23-225">Yasal defter (geçerli katman)</span><span class="sxs-lookup"><span data-stu-id="9cf23-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="9cf23-226">Geçerli katman toplamı</span><span class="sxs-lookup"><span data-stu-id="9cf23-226">Current layer total</span></span></th>
<th><span data-ttu-id="9cf23-227">Ters kayıt defteri (özel katman)</span><span class="sxs-lookup"><span data-stu-id="9cf23-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="9cf23-228">IFRS 16 defteri (özel katman)</span><span class="sxs-lookup"><span data-stu-id="9cf23-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="9cf23-229">Geçerli katman + özel katman toplamı</span><span class="sxs-lookup"><span data-stu-id="9cf23-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="9cf23-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="9cf23-230">JE-100</span></span></th>
<th><span data-ttu-id="9cf23-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="9cf23-231">JE-110</span></span></th>
<th><span data-ttu-id="9cf23-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="9cf23-232">JE-120</span></span></th>
<th><span data-ttu-id="9cf23-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="9cf23-233">JE-130</span></span></th>
<th><span data-ttu-id="9cf23-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="9cf23-234">JE-140</span></span></th>
<th><span data-ttu-id="9cf23-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="9cf23-235">JE-150</span></span></th>
<th><span data-ttu-id="9cf23-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="9cf23-236">JE-160</span></span></th>
<th><span data-ttu-id="9cf23-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="9cf23-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="9cf23-238">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="9cf23-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="9cf23-239">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="9cf23-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="9cf23-240">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="9cf23-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="9cf23-241">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="9cf23-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="9cf23-242">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="9cf23-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="9cf23-243">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="9cf23-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="9cf23-244">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="9cf23-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="9cf23-245">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="9cf23-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9cf23-246">1</span><span class="sxs-lookup"><span data-stu-id="9cf23-246">1</span></span></td>
<td><span data-ttu-id="9cf23-247">Kiralama gideri</span><span class="sxs-lookup"><span data-stu-id="9cf23-247">Lease expense</span></span></td>
<td><span data-ttu-id="9cf23-248">1,000.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="9cf23-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-249">1,000.00</span></span></td>
<td><span data-ttu-id="9cf23-250">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="9cf23-251">0,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cf23-252">2</span><span class="sxs-lookup"><span data-stu-id="9cf23-252">2</span></span></td>
<td><span data-ttu-id="9cf23-253">Banka masrafı</span><span class="sxs-lookup"><span data-stu-id="9cf23-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="9cf23-254">3.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="9cf23-255">3.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="9cf23-256">3.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cf23-257">3</span><span class="sxs-lookup"><span data-stu-id="9cf23-257">3</span></span></td>
<td><span data-ttu-id="9cf23-258">KDV gideri</span><span class="sxs-lookup"><span data-stu-id="9cf23-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="9cf23-259">5.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="9cf23-260">5.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="9cf23-261">5.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cf23-262">4</span><span class="sxs-lookup"><span data-stu-id="9cf23-262">4</span></span></td>
<td><span data-ttu-id="9cf23-263">Kliring hesabı</span><span class="sxs-lookup"><span data-stu-id="9cf23-263">Clearing account</span></span></td>
<td><span data-ttu-id="9cf23-264">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-264">-1,000.00</span></span></td>
<td><span data-ttu-id="9cf23-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="9cf23-266">0,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-266">0.00</span></span></td>
<td><span data-ttu-id="9cf23-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="9cf23-268">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="9cf23-269">0,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cf23-270">5</span><span class="sxs-lookup"><span data-stu-id="9cf23-270">5</span></span></td>
<td><span data-ttu-id="9cf23-271">Borç hesapları</span><span class="sxs-lookup"><span data-stu-id="9cf23-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="9cf23-272">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-272">-1,008.00</span></span></td>
<td><span data-ttu-id="9cf23-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-273">1,008.00</span></span></td>
<td><span data-ttu-id="9cf23-274">0,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="9cf23-275">0,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cf23-276">6</span><span class="sxs-lookup"><span data-stu-id="9cf23-276">6</span></span></td>
<td><span data-ttu-id="9cf23-277">ROU varlığı</span><span class="sxs-lookup"><span data-stu-id="9cf23-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="9cf23-278">0,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="9cf23-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="9cf23-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="9cf23-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cf23-281">7</span><span class="sxs-lookup"><span data-stu-id="9cf23-281">7</span></span></td>
<td><span data-ttu-id="9cf23-282">Finansal kiralama yükümlülüğü</span><span class="sxs-lookup"><span data-stu-id="9cf23-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="9cf23-283">0,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="9cf23-284">-22.794,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-284">-22,794.00</span></span></td>
<td><span data-ttu-id="9cf23-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-285">1,000.00</span></span></td>
<td><span data-ttu-id="9cf23-286">-94,97</span><span class="sxs-lookup"><span data-stu-id="9cf23-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="9cf23-287">-21.888,87</span><span class="sxs-lookup"><span data-stu-id="9cf23-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cf23-288">8</span><span class="sxs-lookup"><span data-stu-id="9cf23-288">8</span></span></td>
<td><span data-ttu-id="9cf23-289">Vade farkı gideri</span><span class="sxs-lookup"><span data-stu-id="9cf23-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="9cf23-290">0,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="9cf23-291">94.97</span><span class="sxs-lookup"><span data-stu-id="9cf23-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="9cf23-292">94.97</span><span class="sxs-lookup"><span data-stu-id="9cf23-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cf23-293">9</span><span class="sxs-lookup"><span data-stu-id="9cf23-293">9</span></span></td>
<td><span data-ttu-id="9cf23-294">Nakit</span><span class="sxs-lookup"><span data-stu-id="9cf23-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="9cf23-295">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-295">-1,008.00</span></span></td>
<td><span data-ttu-id="9cf23-296">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="9cf23-297">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cf23-298">10</span><span class="sxs-lookup"><span data-stu-id="9cf23-298">10</span></span></td>
<td><span data-ttu-id="9cf23-299">Amortisman gideri</span><span class="sxs-lookup"><span data-stu-id="9cf23-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="9cf23-300">0,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="9cf23-301">949.75</span><span class="sxs-lookup"><span data-stu-id="9cf23-301">949.75</span></span></td>
<td><span data-ttu-id="9cf23-302">949.75</span><span class="sxs-lookup"><span data-stu-id="9cf23-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cf23-303">11</span><span class="sxs-lookup"><span data-stu-id="9cf23-303">11</span></span></td>
<td><span data-ttu-id="9cf23-304">Birikmiş amortisman</span><span class="sxs-lookup"><span data-stu-id="9cf23-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="9cf23-305">0,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="9cf23-306">-949,75</span><span class="sxs-lookup"><span data-stu-id="9cf23-306">-949.75</span></span></td>
<td><span data-ttu-id="9cf23-307">-949,75</span><span class="sxs-lookup"><span data-stu-id="9cf23-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9cf23-308">Önceki tabloda gösterildiği gibi, hem yasal raporlama hem de IFRS raporlaması kapsamında raporlamak için üç defter gereklidir.</span><span class="sxs-lookup"><span data-stu-id="9cf23-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="9cf23-309">Yasal defter, kira ödemesini, geçerli katmanda nakit bazlı muhasebe kurallarına göre kaydeder.</span><span class="sxs-lookup"><span data-stu-id="9cf23-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="9cf23-310">Yasal ters kayıt defteri, yasal günlük girişlerini ters kaydeder.</span><span class="sxs-lookup"><span data-stu-id="9cf23-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="9cf23-311">IFRS 16 defteri, IFRS 16 kapsamında gerekli olan günlük girişlerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9cf23-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="9cf23-312">Kiralamayı yalnızca bir kez girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="9cf23-312">You must enter a lease only one time.</span></span> <span data-ttu-id="9cf23-313">Ardından, kiralamayla ilişkili tüm defterleri görmek için **Defterler** sayfasını açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9cf23-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="9cf23-314">Defterleri oluşturduğunuzda, bunların üçü aynı kiralama kaydıyla ilişkilendirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="9cf23-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="9cf23-315">İlk günlük girişi, kiralama giderini yasal deftere kaydeder.</span><span class="sxs-lookup"><span data-stu-id="9cf23-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="9cf23-316">Ödemeleri toplu işte veya yasal defterdeki ödeme planını seçerek oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9cf23-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="9cf23-317">Bu örnekte, aşağıdaki günlük girişi yasal defter için ödeme planından oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="9cf23-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="9cf23-318">Kira ödemesi – 31.01.2020 – JE 100</span><span class="sxs-lookup"><span data-stu-id="9cf23-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="9cf23-319">Hesap türü</span><span class="sxs-lookup"><span data-stu-id="9cf23-319">Account type</span></span> | <span data-ttu-id="9cf23-320">Hesap numarası</span><span class="sxs-lookup"><span data-stu-id="9cf23-320">Account number</span></span> | <span data-ttu-id="9cf23-321">Katman</span><span class="sxs-lookup"><span data-stu-id="9cf23-321">Layer</span></span>   | <span data-ttu-id="9cf23-322">Hesap açıklaması</span><span class="sxs-lookup"><span data-stu-id="9cf23-322">Account description</span></span> | <span data-ttu-id="9cf23-323">Borç</span><span class="sxs-lookup"><span data-stu-id="9cf23-323">Debit</span></span>    | <span data-ttu-id="9cf23-324">Kredi</span><span class="sxs-lookup"><span data-stu-id="9cf23-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="9cf23-325">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="9cf23-325">Ledger</span></span>       | <span data-ttu-id="9cf23-326">1</span><span class="sxs-lookup"><span data-stu-id="9cf23-326">1</span></span>              | <span data-ttu-id="9cf23-327">Cari</span><span class="sxs-lookup"><span data-stu-id="9cf23-327">Current</span></span> | <span data-ttu-id="9cf23-328">Kiralama gideri</span><span class="sxs-lookup"><span data-stu-id="9cf23-328">Lease expense</span></span>       | <span data-ttu-id="9cf23-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-329">1,000.00</span></span> |          |
| <span data-ttu-id="9cf23-330">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="9cf23-330">Ledger</span></span>       | <span data-ttu-id="9cf23-331">4</span><span class="sxs-lookup"><span data-stu-id="9cf23-331">4</span></span>              | <span data-ttu-id="9cf23-332">Cari</span><span class="sxs-lookup"><span data-stu-id="9cf23-332">Current</span></span> | <span data-ttu-id="9cf23-333">Kliring hesabı</span><span class="sxs-lookup"><span data-stu-id="9cf23-333">Clearing account</span></span>    |          | <span data-ttu-id="9cf23-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-334">1,000.00</span></span> |

<span data-ttu-id="9cf23-335">Borç hesapları uzmanı, Varlık kiralama dışındaki kirayı ödemek için fatura oluştururken standart Dynamics 365 işlevini kullanır.</span><span class="sxs-lookup"><span data-stu-id="9cf23-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="9cf23-336">Ancak, Borç hesapları uzmanı aşağıdaki girişi oluşturmak için borç hesabı olarak **Kiralama gideri**'ni seçmek yerine kliring hesabı seçer.</span><span class="sxs-lookup"><span data-stu-id="9cf23-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="9cf23-337">AP işlemi – 31.01.2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="9cf23-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="9cf23-338">Hesap türü</span><span class="sxs-lookup"><span data-stu-id="9cf23-338">Account type</span></span> | <span data-ttu-id="9cf23-339">Hesap numarası</span><span class="sxs-lookup"><span data-stu-id="9cf23-339">Account number</span></span> | <span data-ttu-id="9cf23-340">Katman</span><span class="sxs-lookup"><span data-stu-id="9cf23-340">Layer</span></span>   | <span data-ttu-id="9cf23-341">Hesap açıklaması</span><span class="sxs-lookup"><span data-stu-id="9cf23-341">Account description</span></span> | <span data-ttu-id="9cf23-342">Borç</span><span class="sxs-lookup"><span data-stu-id="9cf23-342">Debit</span></span>    | <span data-ttu-id="9cf23-343">Kredi</span><span class="sxs-lookup"><span data-stu-id="9cf23-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="9cf23-344">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="9cf23-344">Ledger</span></span>       | <span data-ttu-id="9cf23-345">4</span><span class="sxs-lookup"><span data-stu-id="9cf23-345">4</span></span>              | <span data-ttu-id="9cf23-346">Cari</span><span class="sxs-lookup"><span data-stu-id="9cf23-346">Current</span></span> | <span data-ttu-id="9cf23-347">Kliring hesabı</span><span class="sxs-lookup"><span data-stu-id="9cf23-347">Clearing account</span></span>    | <span data-ttu-id="9cf23-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-348">1,000.00</span></span> |          |
| <span data-ttu-id="9cf23-349">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="9cf23-349">Ledger</span></span>       | <span data-ttu-id="9cf23-350">2</span><span class="sxs-lookup"><span data-stu-id="9cf23-350">2</span></span>              | <span data-ttu-id="9cf23-351">Cari</span><span class="sxs-lookup"><span data-stu-id="9cf23-351">Current</span></span> | <span data-ttu-id="9cf23-352">Banka masrafı</span><span class="sxs-lookup"><span data-stu-id="9cf23-352">Bank fee</span></span>            | <span data-ttu-id="9cf23-353">3.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-353">3.00</span></span>     |          |
| <span data-ttu-id="9cf23-354">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="9cf23-354">Ledger</span></span>       | <span data-ttu-id="9cf23-355">3</span><span class="sxs-lookup"><span data-stu-id="9cf23-355">3</span></span>              | <span data-ttu-id="9cf23-356">Cari</span><span class="sxs-lookup"><span data-stu-id="9cf23-356">Current</span></span> | <span data-ttu-id="9cf23-357">KDV gideri</span><span class="sxs-lookup"><span data-stu-id="9cf23-357">VAT expense</span></span>         | <span data-ttu-id="9cf23-358">5.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-358">5.00</span></span>     |          |
| <span data-ttu-id="9cf23-359">Satıcı</span><span class="sxs-lookup"><span data-stu-id="9cf23-359">Vendor</span></span>       | <span data-ttu-id="9cf23-360">5</span><span class="sxs-lookup"><span data-stu-id="9cf23-360">5</span></span>              | <span data-ttu-id="9cf23-361">Cari</span><span class="sxs-lookup"><span data-stu-id="9cf23-361">Current</span></span> | <span data-ttu-id="9cf23-362">Borç hesapları</span><span class="sxs-lookup"><span data-stu-id="9cf23-362">Accounts payable</span></span>    |          | <span data-ttu-id="9cf23-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-363">1,008.00</span></span> |

<span data-ttu-id="9cf23-364">Ekstre satıcıya verildiğinde, normal ödeme sürecini takip edersiniz.</span><span class="sxs-lookup"><span data-stu-id="9cf23-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="9cf23-365">Bu işlem sırasında aşağıdaki günlük girişi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="9cf23-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="9cf23-366">Nakit ödemesi – 31.01.2020 – JE 120</span><span class="sxs-lookup"><span data-stu-id="9cf23-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="9cf23-367">Hesap türü</span><span class="sxs-lookup"><span data-stu-id="9cf23-367">Account type</span></span> | <span data-ttu-id="9cf23-368">Hesap numarası</span><span class="sxs-lookup"><span data-stu-id="9cf23-368">Account number</span></span> | <span data-ttu-id="9cf23-369">Katman</span><span class="sxs-lookup"><span data-stu-id="9cf23-369">Layer</span></span>   | <span data-ttu-id="9cf23-370">Hesap açıklaması</span><span class="sxs-lookup"><span data-stu-id="9cf23-370">Account description</span></span> | <span data-ttu-id="9cf23-371">Borç</span><span class="sxs-lookup"><span data-stu-id="9cf23-371">Debit</span></span>    | <span data-ttu-id="9cf23-372">Kredi</span><span class="sxs-lookup"><span data-stu-id="9cf23-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="9cf23-373">Satıcı</span><span class="sxs-lookup"><span data-stu-id="9cf23-373">Vendor</span></span>       | <span data-ttu-id="9cf23-374">5</span><span class="sxs-lookup"><span data-stu-id="9cf23-374">5</span></span>              | <span data-ttu-id="9cf23-375">Cari</span><span class="sxs-lookup"><span data-stu-id="9cf23-375">Current</span></span> | <span data-ttu-id="9cf23-376">Borç Hesapları</span><span class="sxs-lookup"><span data-stu-id="9cf23-376">Accounts Payable</span></span>    | <span data-ttu-id="9cf23-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-377">1,008.00</span></span> |          |
| <span data-ttu-id="9cf23-378">Banka</span><span class="sxs-lookup"><span data-stu-id="9cf23-378">Bank</span></span>         | <span data-ttu-id="9cf23-379">9</span><span class="sxs-lookup"><span data-stu-id="9cf23-379">9</span></span>              | <span data-ttu-id="9cf23-380">Cari</span><span class="sxs-lookup"><span data-stu-id="9cf23-380">Current</span></span> | <span data-ttu-id="9cf23-381">Nakit</span><span class="sxs-lookup"><span data-stu-id="9cf23-381">Cash</span></span>                |          | <span data-ttu-id="9cf23-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-382">1,008.00</span></span> |

<span data-ttu-id="9cf23-383">Bu aşamada, yasal raporlama gereksinimleri kaypsamında bu kiralamayı tam olarak kaydetmiş olursunuz ve geçerli katmanı kullanarak bir mizan oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9cf23-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="9cf23-384">Sistem, aşağıdaki rakamları içeren bir mizan döndürür.</span><span class="sxs-lookup"><span data-stu-id="9cf23-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="9cf23-385">Hesap numarası</span><span class="sxs-lookup"><span data-stu-id="9cf23-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="9cf23-386">Tanım</span><span class="sxs-lookup"><span data-stu-id="9cf23-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="9cf23-387">Yasal defter (geçerli katman)</span><span class="sxs-lookup"><span data-stu-id="9cf23-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="9cf23-388">Geçerli katman toplamı</span><span class="sxs-lookup"><span data-stu-id="9cf23-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="9cf23-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="9cf23-389">JE-100</span></span></th>
<th><span data-ttu-id="9cf23-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="9cf23-390">JE-110</span></span></th>
<th><span data-ttu-id="9cf23-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="9cf23-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="9cf23-392">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="9cf23-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="9cf23-393">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="9cf23-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="9cf23-394">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="9cf23-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9cf23-395">1</span><span class="sxs-lookup"><span data-stu-id="9cf23-395">1</span></span></td>
<td><span data-ttu-id="9cf23-396">Kiralama gideri</span><span class="sxs-lookup"><span data-stu-id="9cf23-396">Lease expense</span></span></td>
<td><span data-ttu-id="9cf23-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="9cf23-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cf23-399">2</span><span class="sxs-lookup"><span data-stu-id="9cf23-399">2</span></span></td>
<td><span data-ttu-id="9cf23-400">Banka masrafı</span><span class="sxs-lookup"><span data-stu-id="9cf23-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="9cf23-401">3.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="9cf23-402">3.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cf23-403">3</span><span class="sxs-lookup"><span data-stu-id="9cf23-403">3</span></span></td>
<td><span data-ttu-id="9cf23-404">KDV gideri</span><span class="sxs-lookup"><span data-stu-id="9cf23-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="9cf23-405">5.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="9cf23-406">5.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cf23-407">4</span><span class="sxs-lookup"><span data-stu-id="9cf23-407">4</span></span></td>
<td><span data-ttu-id="9cf23-408">Kliring hesabı</span><span class="sxs-lookup"><span data-stu-id="9cf23-408">Clearing account</span></span></td>
<td><span data-ttu-id="9cf23-409">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-409">-1,000.00</span></span></td>
<td><span data-ttu-id="9cf23-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="9cf23-411">0,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cf23-412">5</span><span class="sxs-lookup"><span data-stu-id="9cf23-412">5</span></span></td>
<td><span data-ttu-id="9cf23-413">Borç hesapları</span><span class="sxs-lookup"><span data-stu-id="9cf23-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="9cf23-414">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-414">-1,008.00</span></span></td>
<td><span data-ttu-id="9cf23-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-415">1,008.00</span></span></td>
<td><span data-ttu-id="9cf23-416">0,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cf23-417">6</span><span class="sxs-lookup"><span data-stu-id="9cf23-417">6</span></span></td>
<td><span data-ttu-id="9cf23-418">ROU varlığı</span><span class="sxs-lookup"><span data-stu-id="9cf23-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="9cf23-419">0,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cf23-420">7</span><span class="sxs-lookup"><span data-stu-id="9cf23-420">7</span></span></td>
<td><span data-ttu-id="9cf23-421">Finansal kiralama yükümlülüğü</span><span class="sxs-lookup"><span data-stu-id="9cf23-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="9cf23-422">0,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cf23-423">8</span><span class="sxs-lookup"><span data-stu-id="9cf23-423">8</span></span></td>
<td><span data-ttu-id="9cf23-424">Vade farkı gideri</span><span class="sxs-lookup"><span data-stu-id="9cf23-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="9cf23-425">0,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cf23-426">9</span><span class="sxs-lookup"><span data-stu-id="9cf23-426">9</span></span></td>
<td><span data-ttu-id="9cf23-427">Nakit</span><span class="sxs-lookup"><span data-stu-id="9cf23-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="9cf23-428">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-428">-1,008.00</span></span></td>
<td><span data-ttu-id="9cf23-429">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cf23-430">10</span><span class="sxs-lookup"><span data-stu-id="9cf23-430">10</span></span></td>
<td><span data-ttu-id="9cf23-431">Amortisman gideri</span><span class="sxs-lookup"><span data-stu-id="9cf23-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="9cf23-432">0,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cf23-433">11</span><span class="sxs-lookup"><span data-stu-id="9cf23-433">11</span></span></td>
<td><span data-ttu-id="9cf23-434">Birikmiş amortisman</span><span class="sxs-lookup"><span data-stu-id="9cf23-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="9cf23-435">0,00</span><span class="sxs-lookup"><span data-stu-id="9cf23-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9cf23-436">Aynı mizanı çalıştırmak için IFRS 16 rakamlarını kullanmak istiyorsanız yasal muhasebe günlük girişlerine ters kayıt işlemi uygulanmalıdır ve IFRS 16 günlük girişleri deftere nakledilmelidir.</span><span class="sxs-lookup"><span data-stu-id="9cf23-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="9cf23-437">Yasal günlük girişlerini ters kaydetmek için bu örnek, yasal defterle aynı kuruluma sahip, ancak ters bir deftere nakil profili bulunan bir yasal ters kayıt defteri içerir.</span><span class="sxs-lookup"><span data-stu-id="9cf23-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="9cf23-438">Örneğin, yasal defter bir kiralama gideri hesabını *borçlandırır* ancak ters kayıt defteri bu hesabı *alacaklandırır*.</span><span class="sxs-lookup"><span data-stu-id="9cf23-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="9cf23-439">Bu ilişkiler, **Varlık kiralama parametreleri** sayfasındaki Varlık kiralama deftere nakil hesaplarında kolayca tanımlanır (**Varlık kiralama \> Kurulum \> Varlık kiralama parametreleri**).</span><span class="sxs-lookup"><span data-stu-id="9cf23-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="9cf23-440">Yasal defter için kullanılan işlemin aynısı ters kayıt defteri için kullanılırsa aşağıdaki günlük girişi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="9cf23-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="9cf23-441">Aradaki fark, ters kayıt defterinin ters kayıt girişlerini yasal defterden kaydetmesidir.</span><span class="sxs-lookup"><span data-stu-id="9cf23-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="9cf23-442">Ters kayıt girişleri de özel katmanda yapılır.</span><span class="sxs-lookup"><span data-stu-id="9cf23-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="9cf23-443">Geçerli katmanda bir mizan çalıştırıldığında, ters kayıt günlük girişleri dahil edilmez.</span><span class="sxs-lookup"><span data-stu-id="9cf23-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="9cf23-444">Kira ödemesi – 31.01.2020 – JE 130</span><span class="sxs-lookup"><span data-stu-id="9cf23-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="9cf23-445">Hesap türü</span><span class="sxs-lookup"><span data-stu-id="9cf23-445">Account type</span></span> | <span data-ttu-id="9cf23-446">Hesap numarası</span><span class="sxs-lookup"><span data-stu-id="9cf23-446">Account number</span></span> | <span data-ttu-id="9cf23-447">Katman</span><span class="sxs-lookup"><span data-stu-id="9cf23-447">Layer</span></span>  | <span data-ttu-id="9cf23-448">Hesap açıklaması</span><span class="sxs-lookup"><span data-stu-id="9cf23-448">Account description</span></span> | <span data-ttu-id="9cf23-449">Borç</span><span class="sxs-lookup"><span data-stu-id="9cf23-449">Debit</span></span>    | <span data-ttu-id="9cf23-450">Kredi</span><span class="sxs-lookup"><span data-stu-id="9cf23-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="9cf23-451">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="9cf23-451">Ledger</span></span>       | <span data-ttu-id="9cf23-452">4</span><span class="sxs-lookup"><span data-stu-id="9cf23-452">4</span></span>              | <span data-ttu-id="9cf23-453">Özel</span><span class="sxs-lookup"><span data-stu-id="9cf23-453">Custom</span></span> | <span data-ttu-id="9cf23-454">Kliring hesabı</span><span class="sxs-lookup"><span data-stu-id="9cf23-454">Clearing account</span></span>    | <span data-ttu-id="9cf23-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-455">1,000.00</span></span> |          |
| <span data-ttu-id="9cf23-456">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="9cf23-456">Ledger</span></span>       | <span data-ttu-id="9cf23-457">1</span><span class="sxs-lookup"><span data-stu-id="9cf23-457">1</span></span>              | <span data-ttu-id="9cf23-458">Özel</span><span class="sxs-lookup"><span data-stu-id="9cf23-458">Custom</span></span> | <span data-ttu-id="9cf23-459">Kiralama gideri</span><span class="sxs-lookup"><span data-stu-id="9cf23-459">Lease expense</span></span>       |          | <span data-ttu-id="9cf23-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-460">1,000.00</span></span> |

<span data-ttu-id="9cf23-461">Yasal günlük girişlerini kaldırdığınıza göre IFRS 16'nın gerektirdiği tüm günlük girişlerini IFRS 16 defterine kaydedersiniz.</span><span class="sxs-lookup"><span data-stu-id="9cf23-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="9cf23-462">Bu girişler arasında ROU varlığının ve yükümlülüğün ilk kabulü ile faiz ve amortisman kaydı yer alır.</span><span class="sxs-lookup"><span data-stu-id="9cf23-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="9cf23-463">İlk kabul – 01.01.2020 – JE 140</span><span class="sxs-lookup"><span data-stu-id="9cf23-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="9cf23-464">Hesap türü</span><span class="sxs-lookup"><span data-stu-id="9cf23-464">Account type</span></span> | <span data-ttu-id="9cf23-465">Hesap numarası</span><span class="sxs-lookup"><span data-stu-id="9cf23-465">Account number</span></span> | <span data-ttu-id="9cf23-466">Katman</span><span class="sxs-lookup"><span data-stu-id="9cf23-466">Layer</span></span>  | <span data-ttu-id="9cf23-467">Hesap açıklaması</span><span class="sxs-lookup"><span data-stu-id="9cf23-467">Account description</span></span>      | <span data-ttu-id="9cf23-468">Borç</span><span class="sxs-lookup"><span data-stu-id="9cf23-468">Debit</span></span>     | <span data-ttu-id="9cf23-469">Kredi</span><span class="sxs-lookup"><span data-stu-id="9cf23-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="9cf23-470">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="9cf23-470">Ledger</span></span>       | <span data-ttu-id="9cf23-471">6</span><span class="sxs-lookup"><span data-stu-id="9cf23-471">6</span></span>              | <span data-ttu-id="9cf23-472">Özel</span><span class="sxs-lookup"><span data-stu-id="9cf23-472">Custom</span></span> | <span data-ttu-id="9cf23-473">ROU Varlığı</span><span class="sxs-lookup"><span data-stu-id="9cf23-473">ROU Asset</span></span>                | <span data-ttu-id="9cf23-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="9cf23-474">22,793.90</span></span> |           |
| <span data-ttu-id="9cf23-475">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="9cf23-475">Ledger</span></span>       | <span data-ttu-id="9cf23-476">7</span><span class="sxs-lookup"><span data-stu-id="9cf23-476">7</span></span>              | <span data-ttu-id="9cf23-477">Özel</span><span class="sxs-lookup"><span data-stu-id="9cf23-477">Custom</span></span> | <span data-ttu-id="9cf23-478">Finansal kiralama yükümlülüğü</span><span class="sxs-lookup"><span data-stu-id="9cf23-478">Finance lease obligation</span></span> |           | <span data-ttu-id="9cf23-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="9cf23-479">22,793.90</span></span> |

<span data-ttu-id="9cf23-480">Kira ödemesi diğer kira ödemeleriyle aynı şekilde deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="9cf23-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="9cf23-481">Kliring hesabının kullanılma nedeni, nakitin yalnızca bir kez alacak olarak kaydedilmesini sağlamaktır.</span><span class="sxs-lookup"><span data-stu-id="9cf23-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="9cf23-482">Kira ödemesi – 31.01.2020 – JE 150</span><span class="sxs-lookup"><span data-stu-id="9cf23-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="9cf23-483">Hesap türü</span><span class="sxs-lookup"><span data-stu-id="9cf23-483">Account type</span></span> | <span data-ttu-id="9cf23-484">Hesap numarası</span><span class="sxs-lookup"><span data-stu-id="9cf23-484">Account number</span></span> | <span data-ttu-id="9cf23-485">Katman</span><span class="sxs-lookup"><span data-stu-id="9cf23-485">Layer</span></span>  | <span data-ttu-id="9cf23-486">Hesap açıklaması</span><span class="sxs-lookup"><span data-stu-id="9cf23-486">Account description</span></span>      | <span data-ttu-id="9cf23-487">Borç</span><span class="sxs-lookup"><span data-stu-id="9cf23-487">Debit</span></span>    | <span data-ttu-id="9cf23-488">Kredi</span><span class="sxs-lookup"><span data-stu-id="9cf23-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="9cf23-489">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="9cf23-489">Ledger</span></span>       | <span data-ttu-id="9cf23-490">7</span><span class="sxs-lookup"><span data-stu-id="9cf23-490">7</span></span>              | <span data-ttu-id="9cf23-491">Özel</span><span class="sxs-lookup"><span data-stu-id="9cf23-491">Custom</span></span> | <span data-ttu-id="9cf23-492">Finansal kiralama yükümlülüğü</span><span class="sxs-lookup"><span data-stu-id="9cf23-492">Finance lease obligation</span></span> | <span data-ttu-id="9cf23-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-493">1,000.00</span></span> |          |
| <span data-ttu-id="9cf23-494">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="9cf23-494">Ledger</span></span>       | <span data-ttu-id="9cf23-495">4</span><span class="sxs-lookup"><span data-stu-id="9cf23-495">4</span></span>              | <span data-ttu-id="9cf23-496">Özel</span><span class="sxs-lookup"><span data-stu-id="9cf23-496">Custom</span></span> | <span data-ttu-id="9cf23-497">Kliring hesabı</span><span class="sxs-lookup"><span data-stu-id="9cf23-497">Clearing account</span></span>         |          | <span data-ttu-id="9cf23-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-498">1,000.00</span></span> |

<span data-ttu-id="9cf23-499">Faiz gideri günlüğü girişi, yükümlülük amortisman planlamasından oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="9cf23-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="9cf23-500">Faiz gideri – 31.01.2020 – JE 160</span><span class="sxs-lookup"><span data-stu-id="9cf23-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="9cf23-501">Hesap türü</span><span class="sxs-lookup"><span data-stu-id="9cf23-501">Account type</span></span> | <span data-ttu-id="9cf23-502">Hesap numarası</span><span class="sxs-lookup"><span data-stu-id="9cf23-502">Account number</span></span> | <span data-ttu-id="9cf23-503">Katman</span><span class="sxs-lookup"><span data-stu-id="9cf23-503">Layer</span></span>  | <span data-ttu-id="9cf23-504">Hesap açıklaması</span><span class="sxs-lookup"><span data-stu-id="9cf23-504">Account description</span></span>      | <span data-ttu-id="9cf23-505">Borç</span><span class="sxs-lookup"><span data-stu-id="9cf23-505">Debit</span></span> | <span data-ttu-id="9cf23-506">Kredi</span><span class="sxs-lookup"><span data-stu-id="9cf23-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="9cf23-507">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="9cf23-507">Ledger</span></span>       | <span data-ttu-id="9cf23-508">8</span><span class="sxs-lookup"><span data-stu-id="9cf23-508">8</span></span>              | <span data-ttu-id="9cf23-509">Özel</span><span class="sxs-lookup"><span data-stu-id="9cf23-509">Custom</span></span> | <span data-ttu-id="9cf23-510">Vade farkı gideri</span><span class="sxs-lookup"><span data-stu-id="9cf23-510">Interest expense</span></span>         | <span data-ttu-id="9cf23-511">94.97</span><span class="sxs-lookup"><span data-stu-id="9cf23-511">94.97</span></span> |        |
| <span data-ttu-id="9cf23-512">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="9cf23-512">Ledger</span></span>       | <span data-ttu-id="9cf23-513">7</span><span class="sxs-lookup"><span data-stu-id="9cf23-513">7</span></span>              | <span data-ttu-id="9cf23-514">Özel</span><span class="sxs-lookup"><span data-stu-id="9cf23-514">Custom</span></span> | <span data-ttu-id="9cf23-515">Finansal kiralama yükümlülüğü</span><span class="sxs-lookup"><span data-stu-id="9cf23-515">Finance lease obligation</span></span> |       | <span data-ttu-id="9cf23-516">94.97</span><span class="sxs-lookup"><span data-stu-id="9cf23-516">94.97</span></span>  |

<span data-ttu-id="9cf23-517">Amortisman gideri günlük girişi, varlık amortisman planlamasından oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="9cf23-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="9cf23-518">Amortisman gideri – 31.01.2020 – JE 170</span><span class="sxs-lookup"><span data-stu-id="9cf23-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="9cf23-519">Hesap türü</span><span class="sxs-lookup"><span data-stu-id="9cf23-519">Account type</span></span> | <span data-ttu-id="9cf23-520">Hesap numarası</span><span class="sxs-lookup"><span data-stu-id="9cf23-520">Account number</span></span> | <span data-ttu-id="9cf23-521">Katman</span><span class="sxs-lookup"><span data-stu-id="9cf23-521">Layer</span></span>  | <span data-ttu-id="9cf23-522">Hesap açıklaması</span><span class="sxs-lookup"><span data-stu-id="9cf23-522">Account description</span></span>      | <span data-ttu-id="9cf23-523">Borç</span><span class="sxs-lookup"><span data-stu-id="9cf23-523">Debit</span></span>  | <span data-ttu-id="9cf23-524">Kredi</span><span class="sxs-lookup"><span data-stu-id="9cf23-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="9cf23-525">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="9cf23-525">Ledger</span></span>       | <span data-ttu-id="9cf23-526">10</span><span class="sxs-lookup"><span data-stu-id="9cf23-526">10</span></span>             | <span data-ttu-id="9cf23-527">Özel</span><span class="sxs-lookup"><span data-stu-id="9cf23-527">Custom</span></span> | <span data-ttu-id="9cf23-528">Amortisman gideri</span><span class="sxs-lookup"><span data-stu-id="9cf23-528">Depreciation expense</span></span>     | <span data-ttu-id="9cf23-529">949.75</span><span class="sxs-lookup"><span data-stu-id="9cf23-529">949.75</span></span> |        |
| <span data-ttu-id="9cf23-530">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="9cf23-530">Ledger</span></span>       | <span data-ttu-id="9cf23-531">11</span><span class="sxs-lookup"><span data-stu-id="9cf23-531">11</span></span>             | <span data-ttu-id="9cf23-532">Özel</span><span class="sxs-lookup"><span data-stu-id="9cf23-532">Custom</span></span> | <span data-ttu-id="9cf23-533">Birikmiş amortisman</span><span class="sxs-lookup"><span data-stu-id="9cf23-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="9cf23-534">949.75</span><span class="sxs-lookup"><span data-stu-id="9cf23-534">949.75</span></span> |

<span data-ttu-id="9cf23-535">Tüm bu günlük girişleri oluşturulup deftere nakledildikten sonra, aşağıdaki "özel katman 1" değerlerini görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="9cf23-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="9cf23-536">Son sütuna banka ücreti, katma değer vergisi (KDV) gideri ve önceki katmandan nakit azaltmanın dahil olduğunu görürsünüz ancak yasal raporlama günlük girişleri dahil değildir.</span><span class="sxs-lookup"><span data-stu-id="9cf23-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="9cf23-537">Bu sayede, doğru çift raporlama özelliklerini kullanmış olursunuz.</span><span class="sxs-lookup"><span data-stu-id="9cf23-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="9cf23-538">Bu aşamada, şirketin yalnızca mizanı çalıştırması ve IFRS mizanı oluşturmak için geçerli katman ile özel katmanı birleştirmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="9cf23-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="9cf23-539">Hesap No.</span><span class="sxs-lookup"><span data-stu-id="9cf23-539">Account No</span></span> | <span data-ttu-id="9cf23-540">Tanım</span><span class="sxs-lookup"><span data-stu-id="9cf23-540">Description</span></span>              | <span data-ttu-id="9cf23-541">Yasal Defter\-Geçerli Katman\-JE\-100\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="9cf23-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="9cf23-542">Yasal Defter\-Geçerli Katman\-JE\-110\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="9cf23-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="9cf23-543">Yasal Defter\-Geçerli Katman\-JE\-120\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="9cf23-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="9cf23-544">Geçerli Katman \- Toplamlar</span><span class="sxs-lookup"><span data-stu-id="9cf23-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="9cf23-545">Ters Kayıt Defteri\-Özel katman\-JE\-130\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="9cf23-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="9cf23-546">IFRS 16 Defteri\-Özel katman\-JE\-140\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="9cf23-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="9cf23-547">IFRS 16 Defteri\-Özel katman\-JE\-150\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="9cf23-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="9cf23-548">IFRS 16 Defteri\-Özel katman\-JE\-160\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="9cf23-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="9cf23-549">IFRS 16 Defteri\-Özel katman\-JE\-170\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="9cf23-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="9cf23-550">Geçerli Katman \+ Geçerli Katman \- Toplamlar</span><span class="sxs-lookup"><span data-stu-id="9cf23-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="9cf23-551">1</span><span class="sxs-lookup"><span data-stu-id="9cf23-551">1</span></span>          | <span data-ttu-id="9cf23-552">Kiralama gideri</span><span class="sxs-lookup"><span data-stu-id="9cf23-552">Lease expense</span></span>            | <span data-ttu-id="9cf23-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="9cf23-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-554">1,000\.00</span></span>               |   | <span data-ttu-id="9cf23-555">\-1.000</span><span class="sxs-lookup"><span data-stu-id="9cf23-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="9cf23-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-556">0\.00</span></span>                                   |
| <span data-ttu-id="9cf23-557">2</span><span class="sxs-lookup"><span data-stu-id="9cf23-557">2</span></span>          | <span data-ttu-id="9cf23-558">Banka masrafı</span><span class="sxs-lookup"><span data-stu-id="9cf23-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="9cf23-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="9cf23-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="9cf23-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-561">3\.00</span></span>                                   |
| <span data-ttu-id="9cf23-562">3</span><span class="sxs-lookup"><span data-stu-id="9cf23-562">3</span></span>          | <span data-ttu-id="9cf23-563">KDV gideri</span><span class="sxs-lookup"><span data-stu-id="9cf23-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="9cf23-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="9cf23-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="9cf23-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-566">5\.00</span></span>                                   |
| <span data-ttu-id="9cf23-567">4</span><span class="sxs-lookup"><span data-stu-id="9cf23-567">4</span></span>          | <span data-ttu-id="9cf23-568">Kliring hesabı</span><span class="sxs-lookup"><span data-stu-id="9cf23-568">Clearing account</span></span>         | <span data-ttu-id="9cf23-569">\-1.000\.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="9cf23-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="9cf23-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-571">0\.00</span></span>                   |   | <span data-ttu-id="9cf23-572">1,000</span><span class="sxs-lookup"><span data-stu-id="9cf23-572">1,000</span></span>                                           |                                                | <span data-ttu-id="9cf23-573">\-1.000</span><span class="sxs-lookup"><span data-stu-id="9cf23-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="9cf23-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-574">0\.00</span></span>                                   |
| <span data-ttu-id="9cf23-575">5</span><span class="sxs-lookup"><span data-stu-id="9cf23-575">5</span></span>          | <span data-ttu-id="9cf23-576">Borç hesapları</span><span class="sxs-lookup"><span data-stu-id="9cf23-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="9cf23-577">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="9cf23-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-578">1,008\.00</span></span>                                         | <span data-ttu-id="9cf23-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="9cf23-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-580">0\.00</span></span>                                   |
| <span data-ttu-id="9cf23-581">6</span><span class="sxs-lookup"><span data-stu-id="9cf23-581">6</span></span>          | <span data-ttu-id="9cf23-582">ROU varlığı</span><span class="sxs-lookup"><span data-stu-id="9cf23-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="9cf23-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="9cf23-584">22,794</span><span class="sxs-lookup"><span data-stu-id="9cf23-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="9cf23-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="9cf23-585">22,793\.90</span></span>                              |
| <span data-ttu-id="9cf23-586">7</span><span class="sxs-lookup"><span data-stu-id="9cf23-586">7</span></span>          | <span data-ttu-id="9cf23-587">Finansal kiralama yükümlülüğü</span><span class="sxs-lookup"><span data-stu-id="9cf23-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="9cf23-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="9cf23-589">\-22.794</span><span class="sxs-lookup"><span data-stu-id="9cf23-589">\-22,794</span></span>                                       | <span data-ttu-id="9cf23-590">1,000</span><span class="sxs-lookup"><span data-stu-id="9cf23-590">1,000</span></span>                                          | <span data-ttu-id="9cf23-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="9cf23-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="9cf23-592">\-21,888\.87</span><span class="sxs-lookup"><span data-stu-id="9cf23-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="9cf23-593">8</span><span class="sxs-lookup"><span data-stu-id="9cf23-593">8</span></span>          | <span data-ttu-id="9cf23-594">Vade farkı gideri</span><span class="sxs-lookup"><span data-stu-id="9cf23-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="9cf23-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="9cf23-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="9cf23-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="9cf23-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="9cf23-597">94\.97</span></span>                                  |
| <span data-ttu-id="9cf23-598">9</span><span class="sxs-lookup"><span data-stu-id="9cf23-598">9</span></span>          | <span data-ttu-id="9cf23-599">Nakit</span><span class="sxs-lookup"><span data-stu-id="9cf23-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="9cf23-600">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="9cf23-601">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="9cf23-602">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="9cf23-603">10</span><span class="sxs-lookup"><span data-stu-id="9cf23-603">10</span></span>         | <span data-ttu-id="9cf23-604">Amortisman gideri</span><span class="sxs-lookup"><span data-stu-id="9cf23-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="9cf23-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="9cf23-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="9cf23-606">949\.75</span></span>                                        | <span data-ttu-id="9cf23-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="9cf23-607">949\.75</span></span>                                 |
| <span data-ttu-id="9cf23-608">11</span><span class="sxs-lookup"><span data-stu-id="9cf23-608">11</span></span>         | <span data-ttu-id="9cf23-609">Birikmiş amortisman</span><span class="sxs-lookup"><span data-stu-id="9cf23-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="9cf23-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="9cf23-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="9cf23-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="9cf23-611">\-949\.75</span></span>                                      | <span data-ttu-id="9cf23-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="9cf23-612">\-949\.75</span></span>                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
