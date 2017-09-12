---
title: "Konsolidasyon şirketinde para birimi yeniden değerleme"
description: 
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
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 643af8d771685fe8fd652b353d41f2679e0bef8b
ms.contentlocale: tr-tr
ms.lasthandoff: 07/18/2017

---

# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="5b598-102">Konsolidasyon şirketinde para birimi yeniden değerleme</span><span class="sxs-lookup"><span data-stu-id="5b598-102">Currency revaluation in a consolidation company</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="5b598-103">Verileri bir hesap para biriminden öbürüne birleştirdiğinizde, para biriminde değişiklik varsa para birimi yeniden değerlendirmesini hâlâ çalıştırmanız gerekir, böylece hesap bakileri doğru yeniden değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="5b598-103">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="5b598-104">Özgün verileri birleştirdiğinizde, **para birimi çeviri** sekmesini kullanarak ilk birleştirme işlemi sırasında döviz kurları çevirmek için seçin.</span><span class="sxs-lookup"><span data-stu-id="5b598-104">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="5b598-105">Yeni bir döviz kuru (örneğin, gelecek ay içinde) girildikten sonra hesap bakiyelerini yeniden değerlemek gerekir.</span><span class="sxs-lookup"><span data-stu-id="5b598-105">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="5b598-106">Gerçekleşmemiş Kazançlar veya zararlar sonra buna göre yeni döviz kuru ve tarihe göre güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="5b598-106">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="5b598-107">Aşağıdaki örnek işlem sırasında oluşturulan hesap girişlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="5b598-107">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="5b598-108">Şirket ayarı</span><span class="sxs-lookup"><span data-stu-id="5b598-108">Company setup</span></span>
-   <span data-ttu-id="5b598-109">**Kaynak ve işletim şirketi (USMF)** – ABD doları (USD), muhasebe ve raporlama para birimi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5b598-109">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="5b598-110">**Konsolide şirket (CON)** – muhasebe ve raporlama para birimi Euro (EUR) kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5b598-110">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="5b598-111">**Gerçekleşmiş kazanç**– Genel muhasebe hesabı 801500</span><span class="sxs-lookup"><span data-stu-id="5b598-111">**Realized gain **– Ledger account 801500</span></span>
    -   <span data-ttu-id="5b598-112">**Gerçekleşmiş kayıp**– genel muhasebe hesabı 801600</span><span class="sxs-lookup"><span data-stu-id="5b598-112">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="5b598-113">**Gerçekleşmemiş Kazanç**– genel muhasebe hesabı 801600</span><span class="sxs-lookup"><span data-stu-id="5b598-113">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="5b598-114">**Gerçekleşmemiş kayıp**– genel muhasebe hesabı 801400</span><span class="sxs-lookup"><span data-stu-id="5b598-114">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="5b598-115">Özgün hareketler</span><span class="sxs-lookup"><span data-stu-id="5b598-115">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="5b598-116">USMF'de Nakit Tahsilat hareketleri</span><span class="sxs-lookup"><span data-stu-id="5b598-116">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="5b598-117">Tarih</span><span class="sxs-lookup"><span data-stu-id="5b598-117">Date</span></span>       | <span data-ttu-id="5b598-118">Genel muhasebe hesabı</span><span class="sxs-lookup"><span data-stu-id="5b598-118">Ledger account</span></span>               | <span data-ttu-id="5b598-119">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="5b598-119">Currency</span></span> | <span data-ttu-id="5b598-120">Tutar</span><span class="sxs-lookup"><span data-stu-id="5b598-120">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="5b598-121">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="5b598-121">10/11/2015</span></span> | <span data-ttu-id="5b598-122">110110 – Nakit</span><span class="sxs-lookup"><span data-stu-id="5b598-122">110110 – Cash</span></span>                | <span data-ttu-id="5b598-123">ABD Doları</span><span class="sxs-lookup"><span data-stu-id="5b598-123">USD</span></span>      | <span data-ttu-id="5b598-124">500</span><span class="sxs-lookup"><span data-stu-id="5b598-124">500</span></span>    |
| <span data-ttu-id="5b598-125">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="5b598-125">10/11/2015</span></span> | <span data-ttu-id="5b598-126">130100 – Alacak Hesapları</span><span class="sxs-lookup"><span data-stu-id="5b598-126">130100 – Accounts Receivable</span></span> | <span data-ttu-id="5b598-127">ABD Doları</span><span class="sxs-lookup"><span data-stu-id="5b598-127">USD</span></span>      | <span data-ttu-id="5b598-128">-500</span><span class="sxs-lookup"><span data-stu-id="5b598-128">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="5b598-129">Döviz kurları</span><span class="sxs-lookup"><span data-stu-id="5b598-129">Exchange rates</span></span>
| <span data-ttu-id="5b598-130">Kaynak para birimi</span><span class="sxs-lookup"><span data-stu-id="5b598-130">From currency</span></span> | <span data-ttu-id="5b598-131">Hedef para birimi</span><span class="sxs-lookup"><span data-stu-id="5b598-131">To currency</span></span> | <span data-ttu-id="5b598-132">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="5b598-132">Start date</span></span> | <span data-ttu-id="5b598-133">Döviz kuru</span><span class="sxs-lookup"><span data-stu-id="5b598-133">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="5b598-134">Euro</span><span class="sxs-lookup"><span data-stu-id="5b598-134">EUR</span></span>           | <span data-ttu-id="5b598-135">ABD Doları</span><span class="sxs-lookup"><span data-stu-id="5b598-135">USD</span></span>         | <span data-ttu-id="5b598-136">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="5b598-136">10/1/2015</span></span>  | <span data-ttu-id="5b598-137">200</span><span class="sxs-lookup"><span data-stu-id="5b598-137">200</span></span>           |
| <span data-ttu-id="5b598-138">Euro</span><span class="sxs-lookup"><span data-stu-id="5b598-138">EUR</span></span>           | <span data-ttu-id="5b598-139">ABD Doları</span><span class="sxs-lookup"><span data-stu-id="5b598-139">USD</span></span>         | <span data-ttu-id="5b598-140">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="5b598-140">11/1/2015</span></span>  | <span data-ttu-id="5b598-141">150</span><span class="sxs-lookup"><span data-stu-id="5b598-141">150</span></span>           |
| <span data-ttu-id="5b598-142">Euro</span><span class="sxs-lookup"><span data-stu-id="5b598-142">EUR</span></span>           | <span data-ttu-id="5b598-143">ABD Doları</span><span class="sxs-lookup"><span data-stu-id="5b598-143">USD</span></span>         | <span data-ttu-id="5b598-144">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="5b598-144">12/1/2012</span></span>  | <span data-ttu-id="5b598-145">100</span><span class="sxs-lookup"><span data-stu-id="5b598-145">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="5b598-146">Ekim 2015 için konsolidasyon gerçekleştirme</span><span class="sxs-lookup"><span data-stu-id="5b598-146">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="5b598-147">Konsolidasyon şirketinde bakiyeler</span><span class="sxs-lookup"><span data-stu-id="5b598-147">Balances in the consolidation company</span></span>

| <span data-ttu-id="5b598-148">Genel muhasebe hesabı</span><span class="sxs-lookup"><span data-stu-id="5b598-148">Ledger account</span></span> | <span data-ttu-id="5b598-149">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="5b598-149">Currency</span></span> | <span data-ttu-id="5b598-150">Tutar</span><span class="sxs-lookup"><span data-stu-id="5b598-150">Amount</span></span> | <span data-ttu-id="5b598-151">Hesaplama</span><span class="sxs-lookup"><span data-stu-id="5b598-151">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="5b598-152">110110</span><span class="sxs-lookup"><span data-stu-id="5b598-152">110110</span></span>         | <span data-ttu-id="5b598-153">Euro</span><span class="sxs-lookup"><span data-stu-id="5b598-153">EUR</span></span>      | <span data-ttu-id="5b598-154">250</span><span class="sxs-lookup"><span data-stu-id="5b598-154">250</span></span>    | <span data-ttu-id="5b598-155">500 USD × %50</span><span class="sxs-lookup"><span data-stu-id="5b598-155">500 USD × 50%</span></span>  |
| <span data-ttu-id="5b598-156">130100</span><span class="sxs-lookup"><span data-stu-id="5b598-156">130100</span></span>         | <span data-ttu-id="5b598-157">Euro</span><span class="sxs-lookup"><span data-stu-id="5b598-157">EUR</span></span>      | <span data-ttu-id="5b598-158">-250</span><span class="sxs-lookup"><span data-stu-id="5b598-158">-250</span></span>   | <span data-ttu-id="5b598-159">-500 USD × %50</span><span class="sxs-lookup"><span data-stu-id="5b598-159">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="5b598-160">1 Ekim 2015 ile 30 Kasım 2015 hesaplarından para birimi yeniden değerleme gerçekleştirme</span><span class="sxs-lookup"><span data-stu-id="5b598-160">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="5b598-161">Konsolidasyon şirketinde bakiyeler</span><span class="sxs-lookup"><span data-stu-id="5b598-161">Balances in the consolidation company</span></span>

| <span data-ttu-id="5b598-162">Genel muhasebe hesabı</span><span class="sxs-lookup"><span data-stu-id="5b598-162">Ledger account</span></span> | <span data-ttu-id="5b598-163">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="5b598-163">Currency</span></span> | <span data-ttu-id="5b598-164">Tutar</span><span class="sxs-lookup"><span data-stu-id="5b598-164">Amount</span></span>  | <span data-ttu-id="5b598-165">Hesaplama</span><span class="sxs-lookup"><span data-stu-id="5b598-165">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="5b598-166">110110</span><span class="sxs-lookup"><span data-stu-id="5b598-166">110110</span></span>         | <span data-ttu-id="5b598-167">Euro</span><span class="sxs-lookup"><span data-stu-id="5b598-167">EUR</span></span>      | <span data-ttu-id="5b598-168">333.33</span><span class="sxs-lookup"><span data-stu-id="5b598-168">333.33</span></span>  | <span data-ttu-id="5b598-169">Orijinal tutar 500 × %66.6667</span><span class="sxs-lookup"><span data-stu-id="5b598-169">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="5b598-170">130100</span><span class="sxs-lookup"><span data-stu-id="5b598-170">130100</span></span>         | <span data-ttu-id="5b598-171">Euro</span><span class="sxs-lookup"><span data-stu-id="5b598-171">EUR</span></span>      | <span data-ttu-id="5b598-172">-333.33</span><span class="sxs-lookup"><span data-stu-id="5b598-172">-333.33</span></span> | <span data-ttu-id="5b598-173">Orijinal tutar -500 × %66.6667</span><span class="sxs-lookup"><span data-stu-id="5b598-173">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="5b598-174">801400</span><span class="sxs-lookup"><span data-stu-id="5b598-174">801400</span></span>         | <span data-ttu-id="5b598-175">Euro</span><span class="sxs-lookup"><span data-stu-id="5b598-175">EUR</span></span>      | <span data-ttu-id="5b598-176">83.33</span><span class="sxs-lookup"><span data-stu-id="5b598-176">83.33</span></span>   | <span data-ttu-id="5b598-177">333.33 – 250</span><span class="sxs-lookup"><span data-stu-id="5b598-177">333.33 – 250</span></span>                       |
| <span data-ttu-id="5b598-178">801600</span><span class="sxs-lookup"><span data-stu-id="5b598-178">801600</span></span>         | <span data-ttu-id="5b598-179">Euro</span><span class="sxs-lookup"><span data-stu-id="5b598-179">EUR</span></span>      | <span data-ttu-id="5b598-180">-83.33</span><span class="sxs-lookup"><span data-stu-id="5b598-180">-83.33</span></span>  | <span data-ttu-id="5b598-181">-333.33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="5b598-181">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="5b598-182">Raporlama para birimi tutarları için Diğer hareketleri görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="5b598-182">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="5b598-183">1 Ekim 2015 ile 31 Aralık 2015 hesaplarından para birimi yeniden değerleme gerçekleştirme</span><span class="sxs-lookup"><span data-stu-id="5b598-183">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="5b598-184">Konsolidasyon şirketinde bakiyeler</span><span class="sxs-lookup"><span data-stu-id="5b598-184">Balances in the consolidation company</span></span>

| <span data-ttu-id="5b598-185">Genel muhasebe hesabı</span><span class="sxs-lookup"><span data-stu-id="5b598-185">Ledger account</span></span> | <span data-ttu-id="5b598-186">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="5b598-186">Currency</span></span> | <span data-ttu-id="5b598-187">Tutar</span><span class="sxs-lookup"><span data-stu-id="5b598-187">Amount</span></span>  | <span data-ttu-id="5b598-188">Hesaplama</span><span class="sxs-lookup"><span data-stu-id="5b598-188">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="5b598-189">110110</span><span class="sxs-lookup"><span data-stu-id="5b598-189">110110</span></span>         | <span data-ttu-id="5b598-190">Euro</span><span class="sxs-lookup"><span data-stu-id="5b598-190">EUR</span></span>      | <span data-ttu-id="5b598-191">500.00</span><span class="sxs-lookup"><span data-stu-id="5b598-191">500.00</span></span>  | <span data-ttu-id="5b598-192">Orijinal tutar of 500 × 1</span><span class="sxs-lookup"><span data-stu-id="5b598-192">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="5b598-193">130100</span><span class="sxs-lookup"><span data-stu-id="5b598-193">130100</span></span>         | <span data-ttu-id="5b598-194">Euro</span><span class="sxs-lookup"><span data-stu-id="5b598-194">EUR</span></span>      | <span data-ttu-id="5b598-195">-500.00</span><span class="sxs-lookup"><span data-stu-id="5b598-195">-500.00</span></span> | <span data-ttu-id="5b598-196">Orijinal tutar -500 × 1</span><span class="sxs-lookup"><span data-stu-id="5b598-196">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="5b598-197">801400</span><span class="sxs-lookup"><span data-stu-id="5b598-197">801400</span></span>         | <span data-ttu-id="5b598-198">Euro</span><span class="sxs-lookup"><span data-stu-id="5b598-198">EUR</span></span>      | <span data-ttu-id="5b598-199">250</span><span class="sxs-lookup"><span data-stu-id="5b598-199">250</span></span>     | <span data-ttu-id="5b598-200">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span><span class="sxs-lookup"><span data-stu-id="5b598-200">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="5b598-201">801600</span><span class="sxs-lookup"><span data-stu-id="5b598-201">801600</span></span>         | <span data-ttu-id="5b598-202">Euro</span><span class="sxs-lookup"><span data-stu-id="5b598-202">EUR</span></span>      | <span data-ttu-id="5b598-203">-250</span><span class="sxs-lookup"><span data-stu-id="5b598-203">-250</span></span>    | <span data-ttu-id="5b598-204">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span><span class="sxs-lookup"><span data-stu-id="5b598-204">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |






