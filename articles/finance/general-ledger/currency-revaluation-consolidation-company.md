---
title: Konsolidasyon şirketinde para birimi yeniden değerleme
description: Bu konu, para birimini bir konsolidasyon şirketinde yeniden değerlemeyi açıklar.
author: roschlom
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: roschlom
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 81de31ee75b4be38256505bc7b875dc15473c75a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212241"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="be429-103">Konsolidasyon şirketinde para birimi yeniden değerleme</span><span class="sxs-lookup"><span data-stu-id="be429-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be429-104">Verileri bir hesap para biriminden öbürüne birleştirdiğinizde, para biriminde değişiklik varsa para birimi yeniden değerlendirmesini hâlâ çalıştırmanız gerekir, böylece hesap bakileri doğru yeniden değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="be429-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="be429-105">Özgün verileri birleştirdiğinizde, **para birimi çeviri** sekmesini kullanarak ilk birleştirme işlemi sırasında döviz kurları çevirmek için seçin.</span><span class="sxs-lookup"><span data-stu-id="be429-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="be429-106">Yeni bir döviz kuru (örneğin, gelecek ay içinde) girildikten sonra hesap bakiyelerini yeniden değerlemek gerekir.</span><span class="sxs-lookup"><span data-stu-id="be429-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="be429-107">Gerçekleşmemiş Kazançlar veya zararlar sonra buna göre yeni döviz kuru ve tarihe göre güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="be429-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="be429-108">Aşağıdaki örnek işlem sırasında oluşturulan hesap girişlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="be429-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="be429-109">Şirket ayarı</span><span class="sxs-lookup"><span data-stu-id="be429-109">Company setup</span></span>
-   <span data-ttu-id="be429-110">**Kaynak ve işletim şirketi (USMF)** – ABD doları (USD), muhasebe ve raporlama para birimi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="be429-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="be429-111">**Konsolide şirket (CON)** – muhasebe ve raporlama para birimi Euro (EUR) kullanılır.</span><span class="sxs-lookup"><span data-stu-id="be429-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="be429-112">**Gerçekleşmiş Kazanç** – genel muhasebe hesabı 801500</span><span class="sxs-lookup"><span data-stu-id="be429-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="be429-113">**Gerçekleşmiş kayıp** – genel muhasebe hesabı 801600</span><span class="sxs-lookup"><span data-stu-id="be429-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="be429-114">**Gerçekleşmemiş Kazanç**– genel muhasebe hesabı 801600</span><span class="sxs-lookup"><span data-stu-id="be429-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="be429-115">**Gerçekleşmemiş kayıp**– genel muhasebe hesabı 801400</span><span class="sxs-lookup"><span data-stu-id="be429-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="be429-116">Özgün hareketler</span><span class="sxs-lookup"><span data-stu-id="be429-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="be429-117">USMF'de Nakit Tahsilat hareketleri</span><span class="sxs-lookup"><span data-stu-id="be429-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="be429-118">Tarih</span><span class="sxs-lookup"><span data-stu-id="be429-118">Date</span></span>       | <span data-ttu-id="be429-119">Genel muhasebe hesabı</span><span class="sxs-lookup"><span data-stu-id="be429-119">Ledger account</span></span>               | <span data-ttu-id="be429-120">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="be429-120">Currency</span></span> | <span data-ttu-id="be429-121">Tutar</span><span class="sxs-lookup"><span data-stu-id="be429-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="be429-122">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="be429-122">10/11/2015</span></span> | <span data-ttu-id="be429-123">110110 – Nakit</span><span class="sxs-lookup"><span data-stu-id="be429-123">110110 – Cash</span></span>                | <span data-ttu-id="be429-124">ABD Doları</span><span class="sxs-lookup"><span data-stu-id="be429-124">USD</span></span>      | <span data-ttu-id="be429-125">500</span><span class="sxs-lookup"><span data-stu-id="be429-125">500</span></span>    |
| <span data-ttu-id="be429-126">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="be429-126">10/11/2015</span></span> | <span data-ttu-id="be429-127">130100 – Alacak Hesapları</span><span class="sxs-lookup"><span data-stu-id="be429-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="be429-128">ABD Doları</span><span class="sxs-lookup"><span data-stu-id="be429-128">USD</span></span>      | <span data-ttu-id="be429-129">-500</span><span class="sxs-lookup"><span data-stu-id="be429-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="be429-130">Döviz kurları</span><span class="sxs-lookup"><span data-stu-id="be429-130">Exchange rates</span></span>

| <span data-ttu-id="be429-131">Kaynak para birimi</span><span class="sxs-lookup"><span data-stu-id="be429-131">From currency</span></span> | <span data-ttu-id="be429-132">Hedef para birimi</span><span class="sxs-lookup"><span data-stu-id="be429-132">To currency</span></span> | <span data-ttu-id="be429-133">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="be429-133">Start date</span></span> | <span data-ttu-id="be429-134">Döviz kuru</span><span class="sxs-lookup"><span data-stu-id="be429-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="be429-135">Euro</span><span class="sxs-lookup"><span data-stu-id="be429-135">EUR</span></span>           | <span data-ttu-id="be429-136">ABD Doları</span><span class="sxs-lookup"><span data-stu-id="be429-136">USD</span></span>         | <span data-ttu-id="be429-137">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="be429-137">10/1/2015</span></span>  | <span data-ttu-id="be429-138">200</span><span class="sxs-lookup"><span data-stu-id="be429-138">200</span></span>           |
| <span data-ttu-id="be429-139">Euro</span><span class="sxs-lookup"><span data-stu-id="be429-139">EUR</span></span>           | <span data-ttu-id="be429-140">ABD Doları</span><span class="sxs-lookup"><span data-stu-id="be429-140">USD</span></span>         | <span data-ttu-id="be429-141">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="be429-141">11/1/2015</span></span>  | <span data-ttu-id="be429-142">150</span><span class="sxs-lookup"><span data-stu-id="be429-142">150</span></span>           |
| <span data-ttu-id="be429-143">Euro</span><span class="sxs-lookup"><span data-stu-id="be429-143">EUR</span></span>           | <span data-ttu-id="be429-144">ABD Doları</span><span class="sxs-lookup"><span data-stu-id="be429-144">USD</span></span>         | <span data-ttu-id="be429-145">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="be429-145">12/1/2012</span></span>  | <span data-ttu-id="be429-146">100</span><span class="sxs-lookup"><span data-stu-id="be429-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="be429-147">Ekim 2015 için konsolidasyon gerçekleştirme</span><span class="sxs-lookup"><span data-stu-id="be429-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="be429-148">Konsolidasyon şirketinde bakiyeler</span><span class="sxs-lookup"><span data-stu-id="be429-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="be429-149">Genel muhasebe hesabı</span><span class="sxs-lookup"><span data-stu-id="be429-149">Ledger account</span></span> | <span data-ttu-id="be429-150">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="be429-150">Currency</span></span> | <span data-ttu-id="be429-151">Tutar</span><span class="sxs-lookup"><span data-stu-id="be429-151">Amount</span></span> | <span data-ttu-id="be429-152">Hesaplama</span><span class="sxs-lookup"><span data-stu-id="be429-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="be429-153">110110</span><span class="sxs-lookup"><span data-stu-id="be429-153">110110</span></span>         | <span data-ttu-id="be429-154">Euro</span><span class="sxs-lookup"><span data-stu-id="be429-154">EUR</span></span>      | <span data-ttu-id="be429-155">250</span><span class="sxs-lookup"><span data-stu-id="be429-155">250</span></span>    | <span data-ttu-id="be429-156">500 USD × %50</span><span class="sxs-lookup"><span data-stu-id="be429-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="be429-157">130100</span><span class="sxs-lookup"><span data-stu-id="be429-157">130100</span></span>         | <span data-ttu-id="be429-158">Euro</span><span class="sxs-lookup"><span data-stu-id="be429-158">EUR</span></span>      | <span data-ttu-id="be429-159">-250</span><span class="sxs-lookup"><span data-stu-id="be429-159">-250</span></span>   | <span data-ttu-id="be429-160">-500 USD × %50</span><span class="sxs-lookup"><span data-stu-id="be429-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="be429-161">1 Ekim 2015 ile 30 Kasım 2015 hesaplarından para birimi yeniden değerleme gerçekleştirme</span><span class="sxs-lookup"><span data-stu-id="be429-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="be429-162">Konsolidasyon şirketinde bakiyeler</span><span class="sxs-lookup"><span data-stu-id="be429-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="be429-163">Genel muhasebe hesabı</span><span class="sxs-lookup"><span data-stu-id="be429-163">Ledger account</span></span> | <span data-ttu-id="be429-164">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="be429-164">Currency</span></span> | <span data-ttu-id="be429-165">Tutar</span><span class="sxs-lookup"><span data-stu-id="be429-165">Amount</span></span>  | <span data-ttu-id="be429-166">Hesaplama</span><span class="sxs-lookup"><span data-stu-id="be429-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="be429-167">110110</span><span class="sxs-lookup"><span data-stu-id="be429-167">110110</span></span>         | <span data-ttu-id="be429-168">Euro</span><span class="sxs-lookup"><span data-stu-id="be429-168">EUR</span></span>      | <span data-ttu-id="be429-169">333.33</span><span class="sxs-lookup"><span data-stu-id="be429-169">333.33</span></span>  | <span data-ttu-id="be429-170">Orijinal tutar 500 × %66,6667</span><span class="sxs-lookup"><span data-stu-id="be429-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="be429-171">130100</span><span class="sxs-lookup"><span data-stu-id="be429-171">130100</span></span>         | <span data-ttu-id="be429-172">Euro</span><span class="sxs-lookup"><span data-stu-id="be429-172">EUR</span></span>      | <span data-ttu-id="be429-173">-333.33</span><span class="sxs-lookup"><span data-stu-id="be429-173">-333.33</span></span> | <span data-ttu-id="be429-174">Orijinal tutar -500 × %66,6667</span><span class="sxs-lookup"><span data-stu-id="be429-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="be429-175">801400</span><span class="sxs-lookup"><span data-stu-id="be429-175">801400</span></span>         | <span data-ttu-id="be429-176">Euro</span><span class="sxs-lookup"><span data-stu-id="be429-176">EUR</span></span>      | <span data-ttu-id="be429-177">83.33</span><span class="sxs-lookup"><span data-stu-id="be429-177">83.33</span></span>   | <span data-ttu-id="be429-178">333.33 – 250</span><span class="sxs-lookup"><span data-stu-id="be429-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="be429-179">801600</span><span class="sxs-lookup"><span data-stu-id="be429-179">801600</span></span>         | <span data-ttu-id="be429-180">Euro</span><span class="sxs-lookup"><span data-stu-id="be429-180">EUR</span></span>      | <span data-ttu-id="be429-181">-83.33</span><span class="sxs-lookup"><span data-stu-id="be429-181">-83.33</span></span>  | <span data-ttu-id="be429-182">-333.33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="be429-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="be429-183">Raporlama para birimi tutarları için Diğer hareketleri görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="be429-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="be429-184">1 Ekim 2015 ile 31 Aralık 2015 hesaplarından para birimi yeniden değerleme gerçekleştirme</span><span class="sxs-lookup"><span data-stu-id="be429-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="be429-185">Konsolidasyon şirketinde bakiyeler</span><span class="sxs-lookup"><span data-stu-id="be429-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="be429-186">Genel muhasebe hesabı</span><span class="sxs-lookup"><span data-stu-id="be429-186">Ledger account</span></span> | <span data-ttu-id="be429-187">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="be429-187">Currency</span></span> | <span data-ttu-id="be429-188">Tutar</span><span class="sxs-lookup"><span data-stu-id="be429-188">Amount</span></span>  | <span data-ttu-id="be429-189">Hesaplama</span><span class="sxs-lookup"><span data-stu-id="be429-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="be429-190">110110</span><span class="sxs-lookup"><span data-stu-id="be429-190">110110</span></span>         | <span data-ttu-id="be429-191">Euro</span><span class="sxs-lookup"><span data-stu-id="be429-191">EUR</span></span>      | <span data-ttu-id="be429-192">500.00</span><span class="sxs-lookup"><span data-stu-id="be429-192">500.00</span></span>  | <span data-ttu-id="be429-193">Orijinal tutar of 500 × 1</span><span class="sxs-lookup"><span data-stu-id="be429-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="be429-194">130100</span><span class="sxs-lookup"><span data-stu-id="be429-194">130100</span></span>         | <span data-ttu-id="be429-195">Euro</span><span class="sxs-lookup"><span data-stu-id="be429-195">EUR</span></span>      | <span data-ttu-id="be429-196">-500.00</span><span class="sxs-lookup"><span data-stu-id="be429-196">-500.00</span></span> | <span data-ttu-id="be429-197">Orijinal tutar -500 × 1</span><span class="sxs-lookup"><span data-stu-id="be429-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="be429-198">801400</span><span class="sxs-lookup"><span data-stu-id="be429-198">801400</span></span>         | <span data-ttu-id="be429-199">Euro</span><span class="sxs-lookup"><span data-stu-id="be429-199">EUR</span></span>      | <span data-ttu-id="be429-200">250</span><span class="sxs-lookup"><span data-stu-id="be429-200">250</span></span>     | <span data-ttu-id="be429-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span><span class="sxs-lookup"><span data-stu-id="be429-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="be429-202">801600</span><span class="sxs-lookup"><span data-stu-id="be429-202">801600</span></span>         | <span data-ttu-id="be429-203">Euro</span><span class="sxs-lookup"><span data-stu-id="be429-203">EUR</span></span>      | <span data-ttu-id="be429-204">-250</span><span class="sxs-lookup"><span data-stu-id="be429-204">-250</span></span>    | <span data-ttu-id="be429-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span><span class="sxs-lookup"><span data-stu-id="be429-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]