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
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b4c91399e96c54f7cf9968a15e3fff90c3a71ca6
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="093ac-103">Konsolidasyon şirketinde para birimi yeniden değerleme</span><span class="sxs-lookup"><span data-stu-id="093ac-103">Currency revaluation in a consolidation company</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="093ac-104">Verileri bir hesap para biriminden öbürüne birleştirdiğinizde, para biriminde değişiklik varsa para birimi yeniden değerlendirmesini hâlâ çalıştırmanız gerekir, böylece hesap bakileri doğru yeniden değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="093ac-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="093ac-105">Özgün verileri birleştirdiğinizde, **para birimi çeviri** sekmesini kullanarak ilk birleştirme işlemi sırasında döviz kurları çevirmek için seçin.</span><span class="sxs-lookup"><span data-stu-id="093ac-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="093ac-106">Yeni bir döviz kuru (örneğin, gelecek ay içinde) girildikten sonra hesap bakiyelerini yeniden değerlemek gerekir.</span><span class="sxs-lookup"><span data-stu-id="093ac-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="093ac-107">Gerçekleşmemiş Kazançlar veya zararlar sonra buna göre yeni döviz kuru ve tarihe göre güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="093ac-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="093ac-108">Aşağıdaki örnek işlem sırasında oluşturulan hesap girişlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="093ac-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="093ac-109">Şirket ayarı</span><span class="sxs-lookup"><span data-stu-id="093ac-109">Company setup</span></span>
-   <span data-ttu-id="093ac-110">**Kaynak ve işletim şirketi (USMF)** – ABD doları (USD), muhasebe ve raporlama para birimi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="093ac-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="093ac-111">**Konsolide şirket (CON)** – muhasebe ve raporlama para birimi Euro (EUR) kullanılır.</span><span class="sxs-lookup"><span data-stu-id="093ac-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="093ac-112">**Gerçekleşmiş kazanç**– Genel muhasebe hesabı 801500</span><span class="sxs-lookup"><span data-stu-id="093ac-112">**Realized gain **– Ledger account 801500</span></span>
    -   <span data-ttu-id="093ac-113">**Gerçekleşmiş kayıp**– genel muhasebe hesabı 801600</span><span class="sxs-lookup"><span data-stu-id="093ac-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="093ac-114">**Gerçekleşmemiş Kazanç**– genel muhasebe hesabı 801600</span><span class="sxs-lookup"><span data-stu-id="093ac-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="093ac-115">**Gerçekleşmemiş kayıp**– genel muhasebe hesabı 801400</span><span class="sxs-lookup"><span data-stu-id="093ac-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="093ac-116">Özgün hareketler</span><span class="sxs-lookup"><span data-stu-id="093ac-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="093ac-117">USMF'de Nakit Tahsilat hareketleri</span><span class="sxs-lookup"><span data-stu-id="093ac-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="093ac-118">Tarih</span><span class="sxs-lookup"><span data-stu-id="093ac-118">Date</span></span>       | <span data-ttu-id="093ac-119">Genel muhasebe hesabı</span><span class="sxs-lookup"><span data-stu-id="093ac-119">Ledger account</span></span>               | <span data-ttu-id="093ac-120">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="093ac-120">Currency</span></span> | <span data-ttu-id="093ac-121">Tutar</span><span class="sxs-lookup"><span data-stu-id="093ac-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="093ac-122">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="093ac-122">10/11/2015</span></span> | <span data-ttu-id="093ac-123">110110 – Nakit</span><span class="sxs-lookup"><span data-stu-id="093ac-123">110110 – Cash</span></span>                | <span data-ttu-id="093ac-124">ABD Doları</span><span class="sxs-lookup"><span data-stu-id="093ac-124">USD</span></span>      | <span data-ttu-id="093ac-125">500</span><span class="sxs-lookup"><span data-stu-id="093ac-125">500</span></span>    |
| <span data-ttu-id="093ac-126">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="093ac-126">10/11/2015</span></span> | <span data-ttu-id="093ac-127">130100 – Alacak Hesapları</span><span class="sxs-lookup"><span data-stu-id="093ac-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="093ac-128">ABD Doları</span><span class="sxs-lookup"><span data-stu-id="093ac-128">USD</span></span>      | <span data-ttu-id="093ac-129">-500</span><span class="sxs-lookup"><span data-stu-id="093ac-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="093ac-130">Döviz kurları</span><span class="sxs-lookup"><span data-stu-id="093ac-130">Exchange rates</span></span>
| <span data-ttu-id="093ac-131">Kaynak para birimi</span><span class="sxs-lookup"><span data-stu-id="093ac-131">From currency</span></span> | <span data-ttu-id="093ac-132">Hedef para birimi</span><span class="sxs-lookup"><span data-stu-id="093ac-132">To currency</span></span> | <span data-ttu-id="093ac-133">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="093ac-133">Start date</span></span> | <span data-ttu-id="093ac-134">Döviz kuru</span><span class="sxs-lookup"><span data-stu-id="093ac-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="093ac-135">Euro</span><span class="sxs-lookup"><span data-stu-id="093ac-135">EUR</span></span>           | <span data-ttu-id="093ac-136">ABD Doları</span><span class="sxs-lookup"><span data-stu-id="093ac-136">USD</span></span>         | <span data-ttu-id="093ac-137">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="093ac-137">10/1/2015</span></span>  | <span data-ttu-id="093ac-138">200</span><span class="sxs-lookup"><span data-stu-id="093ac-138">200</span></span>           |
| <span data-ttu-id="093ac-139">Euro</span><span class="sxs-lookup"><span data-stu-id="093ac-139">EUR</span></span>           | <span data-ttu-id="093ac-140">ABD Doları</span><span class="sxs-lookup"><span data-stu-id="093ac-140">USD</span></span>         | <span data-ttu-id="093ac-141">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="093ac-141">11/1/2015</span></span>  | <span data-ttu-id="093ac-142">150</span><span class="sxs-lookup"><span data-stu-id="093ac-142">150</span></span>           |
| <span data-ttu-id="093ac-143">Euro</span><span class="sxs-lookup"><span data-stu-id="093ac-143">EUR</span></span>           | <span data-ttu-id="093ac-144">ABD Doları</span><span class="sxs-lookup"><span data-stu-id="093ac-144">USD</span></span>         | <span data-ttu-id="093ac-145">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="093ac-145">12/1/2012</span></span>  | <span data-ttu-id="093ac-146">100</span><span class="sxs-lookup"><span data-stu-id="093ac-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="093ac-147">Ekim 2015 için konsolidasyon gerçekleştirme</span><span class="sxs-lookup"><span data-stu-id="093ac-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="093ac-148">Konsolidasyon şirketinde bakiyeler</span><span class="sxs-lookup"><span data-stu-id="093ac-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="093ac-149">Genel muhasebe hesabı</span><span class="sxs-lookup"><span data-stu-id="093ac-149">Ledger account</span></span> | <span data-ttu-id="093ac-150">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="093ac-150">Currency</span></span> | <span data-ttu-id="093ac-151">Tutar</span><span class="sxs-lookup"><span data-stu-id="093ac-151">Amount</span></span> | <span data-ttu-id="093ac-152">Hesaplama</span><span class="sxs-lookup"><span data-stu-id="093ac-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="093ac-153">110110</span><span class="sxs-lookup"><span data-stu-id="093ac-153">110110</span></span>         | <span data-ttu-id="093ac-154">Euro</span><span class="sxs-lookup"><span data-stu-id="093ac-154">EUR</span></span>      | <span data-ttu-id="093ac-155">250</span><span class="sxs-lookup"><span data-stu-id="093ac-155">250</span></span>    | <span data-ttu-id="093ac-156">500 USD × %50</span><span class="sxs-lookup"><span data-stu-id="093ac-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="093ac-157">130100</span><span class="sxs-lookup"><span data-stu-id="093ac-157">130100</span></span>         | <span data-ttu-id="093ac-158">Euro</span><span class="sxs-lookup"><span data-stu-id="093ac-158">EUR</span></span>      | <span data-ttu-id="093ac-159">-250</span><span class="sxs-lookup"><span data-stu-id="093ac-159">-250</span></span>   | <span data-ttu-id="093ac-160">-500 USD × %50</span><span class="sxs-lookup"><span data-stu-id="093ac-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="093ac-161">1 Ekim 2015 ile 30 Kasım 2015 hesaplarından para birimi yeniden değerleme gerçekleştirme</span><span class="sxs-lookup"><span data-stu-id="093ac-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="093ac-162">Konsolidasyon şirketinde bakiyeler</span><span class="sxs-lookup"><span data-stu-id="093ac-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="093ac-163">Genel muhasebe hesabı</span><span class="sxs-lookup"><span data-stu-id="093ac-163">Ledger account</span></span> | <span data-ttu-id="093ac-164">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="093ac-164">Currency</span></span> | <span data-ttu-id="093ac-165">Tutar</span><span class="sxs-lookup"><span data-stu-id="093ac-165">Amount</span></span>  | <span data-ttu-id="093ac-166">Hesaplama</span><span class="sxs-lookup"><span data-stu-id="093ac-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="093ac-167">110110</span><span class="sxs-lookup"><span data-stu-id="093ac-167">110110</span></span>         | <span data-ttu-id="093ac-168">Euro</span><span class="sxs-lookup"><span data-stu-id="093ac-168">EUR</span></span>      | <span data-ttu-id="093ac-169">333.33</span><span class="sxs-lookup"><span data-stu-id="093ac-169">333.33</span></span>  | <span data-ttu-id="093ac-170">Orijinal tutar 500 × %66.6667</span><span class="sxs-lookup"><span data-stu-id="093ac-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="093ac-171">130100</span><span class="sxs-lookup"><span data-stu-id="093ac-171">130100</span></span>         | <span data-ttu-id="093ac-172">Euro</span><span class="sxs-lookup"><span data-stu-id="093ac-172">EUR</span></span>      | <span data-ttu-id="093ac-173">-333.33</span><span class="sxs-lookup"><span data-stu-id="093ac-173">-333.33</span></span> | <span data-ttu-id="093ac-174">Orijinal tutar -500 × %66.6667</span><span class="sxs-lookup"><span data-stu-id="093ac-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="093ac-175">801400</span><span class="sxs-lookup"><span data-stu-id="093ac-175">801400</span></span>         | <span data-ttu-id="093ac-176">Euro</span><span class="sxs-lookup"><span data-stu-id="093ac-176">EUR</span></span>      | <span data-ttu-id="093ac-177">83.33</span><span class="sxs-lookup"><span data-stu-id="093ac-177">83.33</span></span>   | <span data-ttu-id="093ac-178">333.33 – 250</span><span class="sxs-lookup"><span data-stu-id="093ac-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="093ac-179">801600</span><span class="sxs-lookup"><span data-stu-id="093ac-179">801600</span></span>         | <span data-ttu-id="093ac-180">Euro</span><span class="sxs-lookup"><span data-stu-id="093ac-180">EUR</span></span>      | <span data-ttu-id="093ac-181">-83.33</span><span class="sxs-lookup"><span data-stu-id="093ac-181">-83.33</span></span>  | <span data-ttu-id="093ac-182">-333.33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="093ac-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="093ac-183">Raporlama para birimi tutarları için Diğer hareketleri görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="093ac-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="093ac-184">1 Ekim 2015 ile 31 Aralık 2015 hesaplarından para birimi yeniden değerleme gerçekleştirme</span><span class="sxs-lookup"><span data-stu-id="093ac-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="093ac-185">Konsolidasyon şirketinde bakiyeler</span><span class="sxs-lookup"><span data-stu-id="093ac-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="093ac-186">Genel muhasebe hesabı</span><span class="sxs-lookup"><span data-stu-id="093ac-186">Ledger account</span></span> | <span data-ttu-id="093ac-187">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="093ac-187">Currency</span></span> | <span data-ttu-id="093ac-188">Tutar</span><span class="sxs-lookup"><span data-stu-id="093ac-188">Amount</span></span>  | <span data-ttu-id="093ac-189">Hesaplama</span><span class="sxs-lookup"><span data-stu-id="093ac-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="093ac-190">110110</span><span class="sxs-lookup"><span data-stu-id="093ac-190">110110</span></span>         | <span data-ttu-id="093ac-191">Euro</span><span class="sxs-lookup"><span data-stu-id="093ac-191">EUR</span></span>      | <span data-ttu-id="093ac-192">500.00</span><span class="sxs-lookup"><span data-stu-id="093ac-192">500.00</span></span>  | <span data-ttu-id="093ac-193">Orijinal tutar of 500 × 1</span><span class="sxs-lookup"><span data-stu-id="093ac-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="093ac-194">130100</span><span class="sxs-lookup"><span data-stu-id="093ac-194">130100</span></span>         | <span data-ttu-id="093ac-195">Euro</span><span class="sxs-lookup"><span data-stu-id="093ac-195">EUR</span></span>      | <span data-ttu-id="093ac-196">-500.00</span><span class="sxs-lookup"><span data-stu-id="093ac-196">-500.00</span></span> | <span data-ttu-id="093ac-197">Orijinal tutar -500 × 1</span><span class="sxs-lookup"><span data-stu-id="093ac-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="093ac-198">801400</span><span class="sxs-lookup"><span data-stu-id="093ac-198">801400</span></span>         | <span data-ttu-id="093ac-199">Euro</span><span class="sxs-lookup"><span data-stu-id="093ac-199">EUR</span></span>      | <span data-ttu-id="093ac-200">250</span><span class="sxs-lookup"><span data-stu-id="093ac-200">250</span></span>     | <span data-ttu-id="093ac-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span><span class="sxs-lookup"><span data-stu-id="093ac-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="093ac-202">801600</span><span class="sxs-lookup"><span data-stu-id="093ac-202">801600</span></span>         | <span data-ttu-id="093ac-203">Euro</span><span class="sxs-lookup"><span data-stu-id="093ac-203">EUR</span></span>      | <span data-ttu-id="093ac-204">-250</span><span class="sxs-lookup"><span data-stu-id="093ac-204">-250</span></span>    | <span data-ttu-id="093ac-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span><span class="sxs-lookup"><span data-stu-id="093ac-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |






