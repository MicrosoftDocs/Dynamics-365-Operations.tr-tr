---
title: "Konsolidasyon şirketinde para birimi yeniden değerleme"
description: "Bu konu, para birimini bir konsolidasyon şirketinde yeniden değerlemeyi açıklar."
author: ShylaThompson
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ad0083018d2734cb1e36cbf5f94105376c57cdf9
ms.openlocfilehash: 76290564037ab6f5c7a1cd4508a819bd603e8148
ms.contentlocale: tr-tr
ms.lasthandoff: 10/02/2018

---

# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="ebb28-103">Konsolidasyon şirketinde para birimi yeniden değerleme</span><span class="sxs-lookup"><span data-stu-id="ebb28-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ebb28-104">Verileri bir hesap para biriminden öbürüne birleştirdiğinizde, para biriminde değişiklik varsa para birimi yeniden değerlendirmesini hâlâ çalıştırmanız gerekir, böylece hesap bakileri doğru yeniden değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="ebb28-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="ebb28-105">Özgün verileri birleştirdiğinizde, **para birimi çeviri** sekmesini kullanarak ilk birleştirme işlemi sırasında döviz kurları çevirmek için seçin.</span><span class="sxs-lookup"><span data-stu-id="ebb28-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="ebb28-106">Yeni bir döviz kuru (örneğin, gelecek ay içinde) girildikten sonra hesap bakiyelerini yeniden değerlemek gerekir.</span><span class="sxs-lookup"><span data-stu-id="ebb28-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="ebb28-107">Gerçekleşmemiş Kazançlar veya zararlar sonra buna göre yeni döviz kuru ve tarihe göre güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="ebb28-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="ebb28-108">Aşağıdaki örnek işlem sırasında oluşturulan hesap girişlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ebb28-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="ebb28-109">Şirket ayarı</span><span class="sxs-lookup"><span data-stu-id="ebb28-109">Company setup</span></span>
-   <span data-ttu-id="ebb28-110">**Kaynak ve işletim şirketi (USMF)** – ABD doları (USD), muhasebe ve raporlama para birimi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ebb28-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="ebb28-111">**Konsolide şirket (CON)** – muhasebe ve raporlama para birimi Euro (EUR) kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ebb28-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="ebb28-112">**Gerçekleşmiş Kazanç** – genel muhasebe hesabı 801500</span><span class="sxs-lookup"><span data-stu-id="ebb28-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="ebb28-113">**Gerçekleşmiş kayıp** – genel muhasebe hesabı 801600</span><span class="sxs-lookup"><span data-stu-id="ebb28-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="ebb28-114">**Gerçekleşmemiş Kazanç**– genel muhasebe hesabı 801600</span><span class="sxs-lookup"><span data-stu-id="ebb28-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="ebb28-115">**Gerçekleşmemiş kayıp**– genel muhasebe hesabı 801400</span><span class="sxs-lookup"><span data-stu-id="ebb28-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="ebb28-116">Özgün hareketler</span><span class="sxs-lookup"><span data-stu-id="ebb28-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="ebb28-117">USMF'de Nakit Tahsilat hareketleri</span><span class="sxs-lookup"><span data-stu-id="ebb28-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="ebb28-118">Tarih</span><span class="sxs-lookup"><span data-stu-id="ebb28-118">Date</span></span>       | <span data-ttu-id="ebb28-119">Genel muhasebe hesabı</span><span class="sxs-lookup"><span data-stu-id="ebb28-119">Ledger account</span></span>               | <span data-ttu-id="ebb28-120">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="ebb28-120">Currency</span></span> | <span data-ttu-id="ebb28-121">Tutar</span><span class="sxs-lookup"><span data-stu-id="ebb28-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="ebb28-122">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="ebb28-122">10/11/2015</span></span> | <span data-ttu-id="ebb28-123">110110 – Nakit</span><span class="sxs-lookup"><span data-stu-id="ebb28-123">110110 – Cash</span></span>                | <span data-ttu-id="ebb28-124">ABD Doları</span><span class="sxs-lookup"><span data-stu-id="ebb28-124">USD</span></span>      | <span data-ttu-id="ebb28-125">500</span><span class="sxs-lookup"><span data-stu-id="ebb28-125">500</span></span>    |
| <span data-ttu-id="ebb28-126">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="ebb28-126">10/11/2015</span></span> | <span data-ttu-id="ebb28-127">130100 – Alacak Hesapları</span><span class="sxs-lookup"><span data-stu-id="ebb28-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="ebb28-128">ABD Doları</span><span class="sxs-lookup"><span data-stu-id="ebb28-128">USD</span></span>      | <span data-ttu-id="ebb28-129">-500</span><span class="sxs-lookup"><span data-stu-id="ebb28-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="ebb28-130">Döviz kurları</span><span class="sxs-lookup"><span data-stu-id="ebb28-130">Exchange rates</span></span>

| <span data-ttu-id="ebb28-131">Kaynak para birimi</span><span class="sxs-lookup"><span data-stu-id="ebb28-131">From currency</span></span> | <span data-ttu-id="ebb28-132">Hedef para birimi</span><span class="sxs-lookup"><span data-stu-id="ebb28-132">To currency</span></span> | <span data-ttu-id="ebb28-133">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="ebb28-133">Start date</span></span> | <span data-ttu-id="ebb28-134">Döviz kuru</span><span class="sxs-lookup"><span data-stu-id="ebb28-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="ebb28-135">Euro</span><span class="sxs-lookup"><span data-stu-id="ebb28-135">EUR</span></span>           | <span data-ttu-id="ebb28-136">ABD Doları</span><span class="sxs-lookup"><span data-stu-id="ebb28-136">USD</span></span>         | <span data-ttu-id="ebb28-137">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="ebb28-137">10/1/2015</span></span>  | <span data-ttu-id="ebb28-138">200</span><span class="sxs-lookup"><span data-stu-id="ebb28-138">200</span></span>           |
| <span data-ttu-id="ebb28-139">Euro</span><span class="sxs-lookup"><span data-stu-id="ebb28-139">EUR</span></span>           | <span data-ttu-id="ebb28-140">ABD Doları</span><span class="sxs-lookup"><span data-stu-id="ebb28-140">USD</span></span>         | <span data-ttu-id="ebb28-141">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="ebb28-141">11/1/2015</span></span>  | <span data-ttu-id="ebb28-142">150</span><span class="sxs-lookup"><span data-stu-id="ebb28-142">150</span></span>           |
| <span data-ttu-id="ebb28-143">Euro</span><span class="sxs-lookup"><span data-stu-id="ebb28-143">EUR</span></span>           | <span data-ttu-id="ebb28-144">ABD Doları</span><span class="sxs-lookup"><span data-stu-id="ebb28-144">USD</span></span>         | <span data-ttu-id="ebb28-145">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="ebb28-145">12/1/2012</span></span>  | <span data-ttu-id="ebb28-146">100</span><span class="sxs-lookup"><span data-stu-id="ebb28-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="ebb28-147">Ekim 2015 için konsolidasyon gerçekleştirme</span><span class="sxs-lookup"><span data-stu-id="ebb28-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="ebb28-148">Konsolidasyon şirketinde bakiyeler</span><span class="sxs-lookup"><span data-stu-id="ebb28-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="ebb28-149">Genel muhasebe hesabı</span><span class="sxs-lookup"><span data-stu-id="ebb28-149">Ledger account</span></span> | <span data-ttu-id="ebb28-150">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="ebb28-150">Currency</span></span> | <span data-ttu-id="ebb28-151">Tutar</span><span class="sxs-lookup"><span data-stu-id="ebb28-151">Amount</span></span> | <span data-ttu-id="ebb28-152">Hesaplama</span><span class="sxs-lookup"><span data-stu-id="ebb28-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="ebb28-153">110110</span><span class="sxs-lookup"><span data-stu-id="ebb28-153">110110</span></span>         | <span data-ttu-id="ebb28-154">Euro</span><span class="sxs-lookup"><span data-stu-id="ebb28-154">EUR</span></span>      | <span data-ttu-id="ebb28-155">250</span><span class="sxs-lookup"><span data-stu-id="ebb28-155">250</span></span>    | <span data-ttu-id="ebb28-156">500 USD × %50</span><span class="sxs-lookup"><span data-stu-id="ebb28-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="ebb28-157">130100</span><span class="sxs-lookup"><span data-stu-id="ebb28-157">130100</span></span>         | <span data-ttu-id="ebb28-158">Euro</span><span class="sxs-lookup"><span data-stu-id="ebb28-158">EUR</span></span>      | <span data-ttu-id="ebb28-159">-250</span><span class="sxs-lookup"><span data-stu-id="ebb28-159">-250</span></span>   | <span data-ttu-id="ebb28-160">-500 USD × %50</span><span class="sxs-lookup"><span data-stu-id="ebb28-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="ebb28-161">1 Ekim 2015 ile 30 Kasım 2015 hesaplarından para birimi yeniden değerleme gerçekleştirme</span><span class="sxs-lookup"><span data-stu-id="ebb28-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="ebb28-162">Konsolidasyon şirketinde bakiyeler</span><span class="sxs-lookup"><span data-stu-id="ebb28-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="ebb28-163">Genel muhasebe hesabı</span><span class="sxs-lookup"><span data-stu-id="ebb28-163">Ledger account</span></span> | <span data-ttu-id="ebb28-164">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="ebb28-164">Currency</span></span> | <span data-ttu-id="ebb28-165">Tutar</span><span class="sxs-lookup"><span data-stu-id="ebb28-165">Amount</span></span>  | <span data-ttu-id="ebb28-166">Hesaplama</span><span class="sxs-lookup"><span data-stu-id="ebb28-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="ebb28-167">110110</span><span class="sxs-lookup"><span data-stu-id="ebb28-167">110110</span></span>         | <span data-ttu-id="ebb28-168">Euro</span><span class="sxs-lookup"><span data-stu-id="ebb28-168">EUR</span></span>      | <span data-ttu-id="ebb28-169">333.33</span><span class="sxs-lookup"><span data-stu-id="ebb28-169">333.33</span></span>  | <span data-ttu-id="ebb28-170">Orijinal tutar 500 × %66.6667</span><span class="sxs-lookup"><span data-stu-id="ebb28-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="ebb28-171">130100</span><span class="sxs-lookup"><span data-stu-id="ebb28-171">130100</span></span>         | <span data-ttu-id="ebb28-172">Euro</span><span class="sxs-lookup"><span data-stu-id="ebb28-172">EUR</span></span>      | <span data-ttu-id="ebb28-173">-333.33</span><span class="sxs-lookup"><span data-stu-id="ebb28-173">-333.33</span></span> | <span data-ttu-id="ebb28-174">Orijinal tutar -500 × %66.6667</span><span class="sxs-lookup"><span data-stu-id="ebb28-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="ebb28-175">801400</span><span class="sxs-lookup"><span data-stu-id="ebb28-175">801400</span></span>         | <span data-ttu-id="ebb28-176">Euro</span><span class="sxs-lookup"><span data-stu-id="ebb28-176">EUR</span></span>      | <span data-ttu-id="ebb28-177">83.33</span><span class="sxs-lookup"><span data-stu-id="ebb28-177">83.33</span></span>   | <span data-ttu-id="ebb28-178">333.33 – 250</span><span class="sxs-lookup"><span data-stu-id="ebb28-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="ebb28-179">801600</span><span class="sxs-lookup"><span data-stu-id="ebb28-179">801600</span></span>         | <span data-ttu-id="ebb28-180">Euro</span><span class="sxs-lookup"><span data-stu-id="ebb28-180">EUR</span></span>      | <span data-ttu-id="ebb28-181">-83.33</span><span class="sxs-lookup"><span data-stu-id="ebb28-181">-83.33</span></span>  | <span data-ttu-id="ebb28-182">-333.33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="ebb28-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="ebb28-183">Raporlama para birimi tutarları için Diğer hareketleri görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="ebb28-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="ebb28-184">1 Ekim 2015 ile 31 Aralık 2015 hesaplarından para birimi yeniden değerleme gerçekleştirme</span><span class="sxs-lookup"><span data-stu-id="ebb28-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="ebb28-185">Konsolidasyon şirketinde bakiyeler</span><span class="sxs-lookup"><span data-stu-id="ebb28-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="ebb28-186">Genel muhasebe hesabı</span><span class="sxs-lookup"><span data-stu-id="ebb28-186">Ledger account</span></span> | <span data-ttu-id="ebb28-187">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="ebb28-187">Currency</span></span> | <span data-ttu-id="ebb28-188">Tutar</span><span class="sxs-lookup"><span data-stu-id="ebb28-188">Amount</span></span>  | <span data-ttu-id="ebb28-189">Hesaplama</span><span class="sxs-lookup"><span data-stu-id="ebb28-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="ebb28-190">110110</span><span class="sxs-lookup"><span data-stu-id="ebb28-190">110110</span></span>         | <span data-ttu-id="ebb28-191">Euro</span><span class="sxs-lookup"><span data-stu-id="ebb28-191">EUR</span></span>      | <span data-ttu-id="ebb28-192">500.00</span><span class="sxs-lookup"><span data-stu-id="ebb28-192">500.00</span></span>  | <span data-ttu-id="ebb28-193">Orijinal tutar of 500 × 1</span><span class="sxs-lookup"><span data-stu-id="ebb28-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="ebb28-194">130100</span><span class="sxs-lookup"><span data-stu-id="ebb28-194">130100</span></span>         | <span data-ttu-id="ebb28-195">Euro</span><span class="sxs-lookup"><span data-stu-id="ebb28-195">EUR</span></span>      | <span data-ttu-id="ebb28-196">-500.00</span><span class="sxs-lookup"><span data-stu-id="ebb28-196">-500.00</span></span> | <span data-ttu-id="ebb28-197">Orijinal tutar -500 × 1</span><span class="sxs-lookup"><span data-stu-id="ebb28-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="ebb28-198">801400</span><span class="sxs-lookup"><span data-stu-id="ebb28-198">801400</span></span>         | <span data-ttu-id="ebb28-199">Euro</span><span class="sxs-lookup"><span data-stu-id="ebb28-199">EUR</span></span>      | <span data-ttu-id="ebb28-200">250</span><span class="sxs-lookup"><span data-stu-id="ebb28-200">250</span></span>     | <span data-ttu-id="ebb28-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span><span class="sxs-lookup"><span data-stu-id="ebb28-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="ebb28-202">801600</span><span class="sxs-lookup"><span data-stu-id="ebb28-202">801600</span></span>         | <span data-ttu-id="ebb28-203">Euro</span><span class="sxs-lookup"><span data-stu-id="ebb28-203">EUR</span></span>      | <span data-ttu-id="ebb28-204">-250</span><span class="sxs-lookup"><span data-stu-id="ebb28-204">-250</span></span>    | <span data-ttu-id="ebb28-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span><span class="sxs-lookup"><span data-stu-id="ebb28-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |






