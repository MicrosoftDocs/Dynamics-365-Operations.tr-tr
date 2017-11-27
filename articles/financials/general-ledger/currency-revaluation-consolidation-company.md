---
title: "Konsolidasyon şirketinde para birimi yeniden değerleme"
description: "Bu konu, para birimini bir konsolidasyon şirketinde yeniden değerlemeyi açıklar."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 27059b0d2a781453a7594bdc430005df6ea5c167
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="52340-103">Konsolidasyon şirketinde para birimi yeniden değerleme</span><span class="sxs-lookup"><span data-stu-id="52340-103">Currency revaluation in a consolidation company</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="52340-104">Verileri bir hesap para biriminden öbürüne birleştirdiğinizde, para biriminde değişiklik varsa para birimi yeniden değerlendirmesini hâlâ çalıştırmanız gerekir, böylece hesap bakileri doğru yeniden değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="52340-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="52340-105">Özgün verileri birleştirdiğinizde, **para birimi çeviri** sekmesini kullanarak ilk birleştirme işlemi sırasında döviz kurları çevirmek için seçin.</span><span class="sxs-lookup"><span data-stu-id="52340-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="52340-106">Yeni bir döviz kuru (örneğin, gelecek ay içinde) girildikten sonra hesap bakiyelerini yeniden değerlemek gerekir.</span><span class="sxs-lookup"><span data-stu-id="52340-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="52340-107">Gerçekleşmemiş Kazançlar veya zararlar sonra buna göre yeni döviz kuru ve tarihe göre güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="52340-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="52340-108">Aşağıdaki örnek işlem sırasında oluşturulan hesap girişlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="52340-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="52340-109">Şirket ayarı</span><span class="sxs-lookup"><span data-stu-id="52340-109">Company setup</span></span>
-   <span data-ttu-id="52340-110">**Kaynak ve işletim şirketi (USMF)** – ABD doları (USD), muhasebe ve raporlama para birimi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="52340-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="52340-111">**Konsolide şirket (CON)** – muhasebe ve raporlama para birimi Euro (EUR) kullanılır.</span><span class="sxs-lookup"><span data-stu-id="52340-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="52340-112">**Gerçekleşmiş kazanç**– Genel muhasebe hesabı 801500</span><span class="sxs-lookup"><span data-stu-id="52340-112">**Realized gain **– Ledger account 801500</span></span>
    -   <span data-ttu-id="52340-113">**Gerçekleşmiş kayıp**– genel muhasebe hesabı 801600</span><span class="sxs-lookup"><span data-stu-id="52340-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="52340-114">**Gerçekleşmemiş Kazanç**– genel muhasebe hesabı 801600</span><span class="sxs-lookup"><span data-stu-id="52340-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="52340-115">**Gerçekleşmemiş kayıp**– genel muhasebe hesabı 801400</span><span class="sxs-lookup"><span data-stu-id="52340-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="52340-116">Özgün hareketler</span><span class="sxs-lookup"><span data-stu-id="52340-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="52340-117">USMF'de Nakit Tahsilat hareketleri</span><span class="sxs-lookup"><span data-stu-id="52340-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="52340-118">Tarih</span><span class="sxs-lookup"><span data-stu-id="52340-118">Date</span></span>       | <span data-ttu-id="52340-119">Genel muhasebe hesabı</span><span class="sxs-lookup"><span data-stu-id="52340-119">Ledger account</span></span>               | <span data-ttu-id="52340-120">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="52340-120">Currency</span></span> | <span data-ttu-id="52340-121">Tutar</span><span class="sxs-lookup"><span data-stu-id="52340-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="52340-122">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="52340-122">10/11/2015</span></span> | <span data-ttu-id="52340-123">110110 – Nakit</span><span class="sxs-lookup"><span data-stu-id="52340-123">110110 – Cash</span></span>                | <span data-ttu-id="52340-124">ABD Doları</span><span class="sxs-lookup"><span data-stu-id="52340-124">USD</span></span>      | <span data-ttu-id="52340-125">500</span><span class="sxs-lookup"><span data-stu-id="52340-125">500</span></span>    |
| <span data-ttu-id="52340-126">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="52340-126">10/11/2015</span></span> | <span data-ttu-id="52340-127">130100 – Alacak Hesapları</span><span class="sxs-lookup"><span data-stu-id="52340-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="52340-128">ABD Doları</span><span class="sxs-lookup"><span data-stu-id="52340-128">USD</span></span>      | <span data-ttu-id="52340-129">-500</span><span class="sxs-lookup"><span data-stu-id="52340-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="52340-130">Döviz kurları</span><span class="sxs-lookup"><span data-stu-id="52340-130">Exchange rates</span></span>
| <span data-ttu-id="52340-131">Kaynak para birimi</span><span class="sxs-lookup"><span data-stu-id="52340-131">From currency</span></span> | <span data-ttu-id="52340-132">Hedef para birimi</span><span class="sxs-lookup"><span data-stu-id="52340-132">To currency</span></span> | <span data-ttu-id="52340-133">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="52340-133">Start date</span></span> | <span data-ttu-id="52340-134">Döviz kuru</span><span class="sxs-lookup"><span data-stu-id="52340-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="52340-135">Euro</span><span class="sxs-lookup"><span data-stu-id="52340-135">EUR</span></span>           | <span data-ttu-id="52340-136">ABD Doları</span><span class="sxs-lookup"><span data-stu-id="52340-136">USD</span></span>         | <span data-ttu-id="52340-137">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="52340-137">10/1/2015</span></span>  | <span data-ttu-id="52340-138">200</span><span class="sxs-lookup"><span data-stu-id="52340-138">200</span></span>           |
| <span data-ttu-id="52340-139">Euro</span><span class="sxs-lookup"><span data-stu-id="52340-139">EUR</span></span>           | <span data-ttu-id="52340-140">ABD Doları</span><span class="sxs-lookup"><span data-stu-id="52340-140">USD</span></span>         | <span data-ttu-id="52340-141">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="52340-141">11/1/2015</span></span>  | <span data-ttu-id="52340-142">150</span><span class="sxs-lookup"><span data-stu-id="52340-142">150</span></span>           |
| <span data-ttu-id="52340-143">Euro</span><span class="sxs-lookup"><span data-stu-id="52340-143">EUR</span></span>           | <span data-ttu-id="52340-144">ABD Doları</span><span class="sxs-lookup"><span data-stu-id="52340-144">USD</span></span>         | <span data-ttu-id="52340-145">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="52340-145">12/1/2012</span></span>  | <span data-ttu-id="52340-146">100</span><span class="sxs-lookup"><span data-stu-id="52340-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="52340-147">Ekim 2015 için konsolidasyon gerçekleştirme</span><span class="sxs-lookup"><span data-stu-id="52340-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="52340-148">Konsolidasyon şirketinde bakiyeler</span><span class="sxs-lookup"><span data-stu-id="52340-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="52340-149">Genel muhasebe hesabı</span><span class="sxs-lookup"><span data-stu-id="52340-149">Ledger account</span></span> | <span data-ttu-id="52340-150">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="52340-150">Currency</span></span> | <span data-ttu-id="52340-151">Tutar</span><span class="sxs-lookup"><span data-stu-id="52340-151">Amount</span></span> | <span data-ttu-id="52340-152">Hesaplama</span><span class="sxs-lookup"><span data-stu-id="52340-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="52340-153">110110</span><span class="sxs-lookup"><span data-stu-id="52340-153">110110</span></span>         | <span data-ttu-id="52340-154">Euro</span><span class="sxs-lookup"><span data-stu-id="52340-154">EUR</span></span>      | <span data-ttu-id="52340-155">250</span><span class="sxs-lookup"><span data-stu-id="52340-155">250</span></span>    | <span data-ttu-id="52340-156">500 USD × %50</span><span class="sxs-lookup"><span data-stu-id="52340-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="52340-157">130100</span><span class="sxs-lookup"><span data-stu-id="52340-157">130100</span></span>         | <span data-ttu-id="52340-158">Euro</span><span class="sxs-lookup"><span data-stu-id="52340-158">EUR</span></span>      | <span data-ttu-id="52340-159">-250</span><span class="sxs-lookup"><span data-stu-id="52340-159">-250</span></span>   | <span data-ttu-id="52340-160">-500 USD × %50</span><span class="sxs-lookup"><span data-stu-id="52340-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="52340-161">1 Ekim 2015 ile 30 Kasım 2015 hesaplarından para birimi yeniden değerleme gerçekleştirme</span><span class="sxs-lookup"><span data-stu-id="52340-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="52340-162">Konsolidasyon şirketinde bakiyeler</span><span class="sxs-lookup"><span data-stu-id="52340-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="52340-163">Genel muhasebe hesabı</span><span class="sxs-lookup"><span data-stu-id="52340-163">Ledger account</span></span> | <span data-ttu-id="52340-164">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="52340-164">Currency</span></span> | <span data-ttu-id="52340-165">Tutar</span><span class="sxs-lookup"><span data-stu-id="52340-165">Amount</span></span>  | <span data-ttu-id="52340-166">Hesaplama</span><span class="sxs-lookup"><span data-stu-id="52340-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="52340-167">110110</span><span class="sxs-lookup"><span data-stu-id="52340-167">110110</span></span>         | <span data-ttu-id="52340-168">Euro</span><span class="sxs-lookup"><span data-stu-id="52340-168">EUR</span></span>      | <span data-ttu-id="52340-169">333.33</span><span class="sxs-lookup"><span data-stu-id="52340-169">333.33</span></span>  | <span data-ttu-id="52340-170">Orijinal tutar 500 × %66.6667</span><span class="sxs-lookup"><span data-stu-id="52340-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="52340-171">130100</span><span class="sxs-lookup"><span data-stu-id="52340-171">130100</span></span>         | <span data-ttu-id="52340-172">Euro</span><span class="sxs-lookup"><span data-stu-id="52340-172">EUR</span></span>      | <span data-ttu-id="52340-173">-333.33</span><span class="sxs-lookup"><span data-stu-id="52340-173">-333.33</span></span> | <span data-ttu-id="52340-174">Orijinal tutar -500 × %66.6667</span><span class="sxs-lookup"><span data-stu-id="52340-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="52340-175">801400</span><span class="sxs-lookup"><span data-stu-id="52340-175">801400</span></span>         | <span data-ttu-id="52340-176">Euro</span><span class="sxs-lookup"><span data-stu-id="52340-176">EUR</span></span>      | <span data-ttu-id="52340-177">83.33</span><span class="sxs-lookup"><span data-stu-id="52340-177">83.33</span></span>   | <span data-ttu-id="52340-178">333.33 – 250</span><span class="sxs-lookup"><span data-stu-id="52340-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="52340-179">801600</span><span class="sxs-lookup"><span data-stu-id="52340-179">801600</span></span>         | <span data-ttu-id="52340-180">Euro</span><span class="sxs-lookup"><span data-stu-id="52340-180">EUR</span></span>      | <span data-ttu-id="52340-181">-83.33</span><span class="sxs-lookup"><span data-stu-id="52340-181">-83.33</span></span>  | <span data-ttu-id="52340-182">-333.33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="52340-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="52340-183">Raporlama para birimi tutarları için Diğer hareketleri görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="52340-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="52340-184">1 Ekim 2015 ile 31 Aralık 2015 hesaplarından para birimi yeniden değerleme gerçekleştirme</span><span class="sxs-lookup"><span data-stu-id="52340-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="52340-185">Konsolidasyon şirketinde bakiyeler</span><span class="sxs-lookup"><span data-stu-id="52340-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="52340-186">Genel muhasebe hesabı</span><span class="sxs-lookup"><span data-stu-id="52340-186">Ledger account</span></span> | <span data-ttu-id="52340-187">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="52340-187">Currency</span></span> | <span data-ttu-id="52340-188">Tutar</span><span class="sxs-lookup"><span data-stu-id="52340-188">Amount</span></span>  | <span data-ttu-id="52340-189">Hesaplama</span><span class="sxs-lookup"><span data-stu-id="52340-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="52340-190">110110</span><span class="sxs-lookup"><span data-stu-id="52340-190">110110</span></span>         | <span data-ttu-id="52340-191">Euro</span><span class="sxs-lookup"><span data-stu-id="52340-191">EUR</span></span>      | <span data-ttu-id="52340-192">500.00</span><span class="sxs-lookup"><span data-stu-id="52340-192">500.00</span></span>  | <span data-ttu-id="52340-193">Orijinal tutar of 500 × 1</span><span class="sxs-lookup"><span data-stu-id="52340-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="52340-194">130100</span><span class="sxs-lookup"><span data-stu-id="52340-194">130100</span></span>         | <span data-ttu-id="52340-195">Euro</span><span class="sxs-lookup"><span data-stu-id="52340-195">EUR</span></span>      | <span data-ttu-id="52340-196">-500.00</span><span class="sxs-lookup"><span data-stu-id="52340-196">-500.00</span></span> | <span data-ttu-id="52340-197">Orijinal tutar -500 × 1</span><span class="sxs-lookup"><span data-stu-id="52340-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="52340-198">801400</span><span class="sxs-lookup"><span data-stu-id="52340-198">801400</span></span>         | <span data-ttu-id="52340-199">Euro</span><span class="sxs-lookup"><span data-stu-id="52340-199">EUR</span></span>      | <span data-ttu-id="52340-200">250</span><span class="sxs-lookup"><span data-stu-id="52340-200">250</span></span>     | <span data-ttu-id="52340-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span><span class="sxs-lookup"><span data-stu-id="52340-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="52340-202">801600</span><span class="sxs-lookup"><span data-stu-id="52340-202">801600</span></span>         | <span data-ttu-id="52340-203">Euro</span><span class="sxs-lookup"><span data-stu-id="52340-203">EUR</span></span>      | <span data-ttu-id="52340-204">-250</span><span class="sxs-lookup"><span data-stu-id="52340-204">-250</span></span>    | <span data-ttu-id="52340-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span><span class="sxs-lookup"><span data-stu-id="52340-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |






