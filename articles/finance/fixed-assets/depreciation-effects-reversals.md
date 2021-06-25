---
title: Ters işlemli amortismanın etkileri
description: Bu makalede, sabit kıymet hareketini ters kaydetmenin olası etkileri ele alınmaktadır.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0d47a25835eab16438ea47bf3960132debc8c975
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187904"
---
# <a name="depreciation-effects-with-reversals"></a><span data-ttu-id="bbefc-103">Ters işlemli amortismanın etkileri</span><span class="sxs-lookup"><span data-stu-id="bbefc-103">Depreciation effects with reversals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bbefc-104">Bu makalede, sabit kıymet hareketini ters kaydetmenin olası etkileri ele alınmaktadır.</span><span class="sxs-lookup"><span data-stu-id="bbefc-104">This article discusses potential implications of reversing a fixed asset transaction.</span></span> 

<span data-ttu-id="bbefc-105">Sabit kıymet hareketlerine ve sabit kıymetle ilişkili hareketlere ters işlem uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bbefc-105">You can reverse fixed asset transactions, and the transactions that are associated with a fixed asset.</span></span> <span data-ttu-id="bbefc-106">Ayrıca tersine çevrilmiş bir hareketi de iptal edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bbefc-106">You can also revoke a reversed transaction.</span></span> 

<span data-ttu-id="bbefc-107">Kıymet için deftere nakledilen en son hareket olmayan bir hareketi tersine çevirebilir veya iptal edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bbefc-107">You can reverse or revoke a transaction that was not the most recent transaction posted to the book for the asset.</span></span> <span data-ttu-id="bbefc-108">Öncelikle, tersine çevireceğiniz hareketten sonra herhangi bir amortisman hareketinin deftere nakledilip edilmediğini belirlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="bbefc-108">You should first determine whether any depreciation transactions were posted after the transaction that you are reversing.</span></span> <span data-ttu-id="bbefc-109">Bunun sebebi bir hareketi ters kaydettiğinizde amortismanın yeniden hesaplanmayacak olmasıdır.</span><span class="sxs-lookup"><span data-stu-id="bbefc-109">This is because depreciation is not recalculated when you reverse a transaction.</span></span> <span data-ttu-id="bbefc-110">Bu nedenle, amortisman ters işlem örneklerde gösterildiği gibi genellikle olduğundan daha fazla veya daha az belirtilir.</span><span class="sxs-lookup"><span data-stu-id="bbefc-110">Therefore, depreciation often is overstated or understated after the reversal, as shown in the examples.</span></span> 

<span data-ttu-id="bbefc-111">Bir hareketi tersine çevirdiğinizde amortismanın doğru olduğundan emin olmak için amortismanın yeniden hesaplanmayacağını belirten bir ileti alırsanız, iptal işlemiyle devam etmeyin.</span><span class="sxs-lookup"><span data-stu-id="bbefc-111">To make sure that depreciation is correct when you reverse a transaction, do not continue with the reversal if you receive a message that states that depreciation will not be recalculated.</span></span> <span data-ttu-id="bbefc-112">Bunun yerine, önce tersine çevirmeye çalıştığınız hareketten sonra nakledilen amortisman hareketini tersine çevirin ve sonra iptal işlemiyle devam edin.</span><span class="sxs-lookup"><span data-stu-id="bbefc-112">Instead, first reverse the depreciation transaction that was posted after the transaction you tried to reverse, and then continue with the reversal.</span></span> <span data-ttu-id="bbefc-113">Amortismanın yeniden hesaplanmasıyla ilgili uyarılmazsınız ve iptal işlemiyle devam edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bbefc-113">You will not be warned about depreciation recalculations, and you can continue with the reversal.</span></span> 

<span data-ttu-id="bbefc-114">Aşağıdaki örneklerde, uyarı iletisinden sonra, öncelikle amortisman hareketlerini tersine çevirmeden devam ederseniz oluşacak hesaplamalar gösterilir.</span><span class="sxs-lookup"><span data-stu-id="bbefc-114">The following examples show the calculations that occur if you continue beyond the message without first reversing the depreciation transactions.</span></span>

## <a name="example-1-depreciation-is-overstated"></a><span data-ttu-id="bbefc-115"> Örnek 1: Amortisman olduğundan daha fazla belirtilir</span><span class="sxs-lookup"><span data-stu-id="bbefc-115">Example 1: Depreciation is overstated</span></span>
<span data-ttu-id="bbefc-116">Bir kıymet 5 yıllık kullanım süresi ve sabit amortisman (60 amortisman dönemi) ile ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="bbefc-116">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="bbefc-117">Bu örnekte, amortisman olduğundan daha fazla belirtilmiştir.</span><span class="sxs-lookup"><span data-stu-id="bbefc-117">In this example, depreciation is overstated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="bbefc-118">Kıymet hareket geçmişi</span><span class="sxs-lookup"><span data-stu-id="bbefc-118">Asset transaction history</span></span>

| <span data-ttu-id="bbefc-119">Tarih</span><span class="sxs-lookup"><span data-stu-id="bbefc-119">Date</span></span>       | <span data-ttu-id="bbefc-120">Hareket tipi</span><span class="sxs-lookup"><span data-stu-id="bbefc-120">Transaction type</span></span>                                                          | <span data-ttu-id="bbefc-121">Tutar</span><span class="sxs-lookup"><span data-stu-id="bbefc-121">Amount</span></span>                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="bbefc-122">1 Ocak</span><span class="sxs-lookup"><span data-stu-id="bbefc-122">January 1</span></span>  | <span data-ttu-id="bbefc-123">Alım</span><span class="sxs-lookup"><span data-stu-id="bbefc-123">Acquisition</span></span>                                                               | <span data-ttu-id="bbefc-124">59.000,00</span><span class="sxs-lookup"><span data-stu-id="bbefc-124">59,000.00</span></span>                                 |
| <span data-ttu-id="bbefc-125">1 Ocak</span><span class="sxs-lookup"><span data-stu-id="bbefc-125">January 1</span></span>  | <span data-ttu-id="bbefc-126">Alım düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="bbefc-126">Acquisition adjustment</span></span>                                                    | <span data-ttu-id="bbefc-127">1.000,00</span><span class="sxs-lookup"><span data-stu-id="bbefc-127">1,000.00</span></span>                                  |
| <span data-ttu-id="bbefc-128">31 Ocak</span><span class="sxs-lookup"><span data-stu-id="bbefc-128">January 31</span></span> | <span data-ttu-id="bbefc-129">Amortisman (bir amortisman dönemine yönelik teklifin kullanılmasıyla oluşturulan)</span><span class="sxs-lookup"><span data-stu-id="bbefc-129">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="bbefc-130">1.000,00Hesaplaması: Defter değeri (59.000 + 1.000 amortisman) / kalan amortisman dönemi sayısı (60)</span><span class="sxs-lookup"><span data-stu-id="bbefc-130">1,000.00Calculation: Book value (59,000 + 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="bbefc-131">Tersine çevirme eylemi</span><span class="sxs-lookup"><span data-stu-id="bbefc-131">Reversal action</span></span>

| <span data-ttu-id="bbefc-132">Tarih</span><span class="sxs-lookup"><span data-stu-id="bbefc-132">Date</span></span>      | <span data-ttu-id="bbefc-133">Hareket türü</span><span class="sxs-lookup"><span data-stu-id="bbefc-133">Transaction type</span></span>                | <span data-ttu-id="bbefc-134">Tutar</span><span class="sxs-lookup"><span data-stu-id="bbefc-134">Amount</span></span>    |
|-----------|---------------------------------|-----------|
| <span data-ttu-id="bbefc-135">1 Ocak</span><span class="sxs-lookup"><span data-stu-id="bbefc-135">January 1</span></span> | <span data-ttu-id="bbefc-136">Alım ayarlaması iptali</span><span class="sxs-lookup"><span data-stu-id="bbefc-136">Acquisition adjustment reversal</span></span> | <span data-ttu-id="bbefc-137">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="bbefc-137">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="bbefc-138">Amortisman etkisi</span><span class="sxs-lookup"><span data-stu-id="bbefc-138">Depreciation effect</span></span>

| <span data-ttu-id="bbefc-139">Tarih</span><span class="sxs-lookup"><span data-stu-id="bbefc-139">Date</span></span>        | <span data-ttu-id="bbefc-140">Hareket türü</span><span class="sxs-lookup"><span data-stu-id="bbefc-140">Transaction type</span></span>        | <span data-ttu-id="bbefc-141">Tutar</span><span class="sxs-lookup"><span data-stu-id="bbefc-141">Amount</span></span>                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bbefc-142">28 Şubat</span><span class="sxs-lookup"><span data-stu-id="bbefc-142">February 28</span></span> | <span data-ttu-id="bbefc-143">Amortisman (teklif)</span><span class="sxs-lookup"><span data-stu-id="bbefc-143">Depreciation (proposal)</span></span> | <span data-ttu-id="bbefc-144">983,05Hesaplaması: Defter değeri (59.000 - 1.000 amortisman) / kalan amortisman dönemi sayısı (59)</span><span class="sxs-lookup"><span data-stu-id="bbefc-144">983.05Calculation: Book value (59,000 - 1,000 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="bbefc-145">Amortisman 16,95 değeri kadar daha fazla belirtilir (1000 - 983,05).</span><span class="sxs-lookup"><span data-stu-id="bbefc-145">Depreciation is overstated by 16.95 (1,000 - 983.05).</span></span>

## <a name="example-2-depreciation-is-understated"></a><span data-ttu-id="bbefc-146"> Örnek 2: Amortisman olduğundan daha az belirtilir</span><span class="sxs-lookup"><span data-stu-id="bbefc-146">Example 2: Depreciation is understated</span></span>
<span data-ttu-id="bbefc-147">Bir kıymet 5 yıllık kullanım süresi ve sabit amortisman (60 amortisman dönemi) ile ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="bbefc-147">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="bbefc-148">Bu örnekte, amortisman olduğundan daha az belirtilmiştir.</span><span class="sxs-lookup"><span data-stu-id="bbefc-148">In this example, depreciation is understated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="bbefc-149">Kıymet hareket geçmişi</span><span class="sxs-lookup"><span data-stu-id="bbefc-149">Asset transaction history</span></span>

| <span data-ttu-id="bbefc-150">Tarih</span><span class="sxs-lookup"><span data-stu-id="bbefc-150">Date</span></span>       | <span data-ttu-id="bbefc-151">Hareket türü</span><span class="sxs-lookup"><span data-stu-id="bbefc-151">Transaction type</span></span>                                                          | <span data-ttu-id="bbefc-152">Tutar</span><span class="sxs-lookup"><span data-stu-id="bbefc-152">Amount</span></span>                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="bbefc-153">1 Ocak</span><span class="sxs-lookup"><span data-stu-id="bbefc-153">January 1</span></span>  | <span data-ttu-id="bbefc-154">Alım</span><span class="sxs-lookup"><span data-stu-id="bbefc-154">Acquisition</span></span>                                                               | <span data-ttu-id="bbefc-155">59.000,00</span><span class="sxs-lookup"><span data-stu-id="bbefc-155">59,000.00</span></span>                                   |
| <span data-ttu-id="bbefc-156">1 Ocak</span><span class="sxs-lookup"><span data-stu-id="bbefc-156">January 1</span></span>  | <span data-ttu-id="bbefc-157">Değer azaltma düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="bbefc-157">Write-down adjustment</span></span>                                                     | <span data-ttu-id="bbefc-158">1.000,00</span><span class="sxs-lookup"><span data-stu-id="bbefc-158">1,000.00</span></span>                                    |
| <span data-ttu-id="bbefc-159">31 Ocak</span><span class="sxs-lookup"><span data-stu-id="bbefc-159">January 31</span></span> | <span data-ttu-id="bbefc-160">Amortisman (bir amortisman dönemine yönelik teklifin kullanılmasıyla oluşturulan)</span><span class="sxs-lookup"><span data-stu-id="bbefc-160">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="bbefc-161">966,67Hesaplaması: Defter değeri (59.000 - 1.000 amortisman) / kalan amortisman dönemi sayısı (60)</span><span class="sxs-lookup"><span data-stu-id="bbefc-161">966.67Calculation: Book value (59,000 - 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="bbefc-162">Tersine çevirme eylemi</span><span class="sxs-lookup"><span data-stu-id="bbefc-162">Reversal action</span></span>

| <span data-ttu-id="bbefc-163">Tarih</span><span class="sxs-lookup"><span data-stu-id="bbefc-163">Date</span></span>      | <span data-ttu-id="bbefc-164">Hareket türü</span><span class="sxs-lookup"><span data-stu-id="bbefc-164">Transaction type</span></span>               | <span data-ttu-id="bbefc-165">Tutar</span><span class="sxs-lookup"><span data-stu-id="bbefc-165">Amount</span></span>    |
|-----------|--------------------------------|-----------|
| <span data-ttu-id="bbefc-166">1 Ocak</span><span class="sxs-lookup"><span data-stu-id="bbefc-166">January 1</span></span> | <span data-ttu-id="bbefc-167">Değer azaltma düzeltmesi iptali</span><span class="sxs-lookup"><span data-stu-id="bbefc-167">Write-down adjustment reversal</span></span> | <span data-ttu-id="bbefc-168">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="bbefc-168">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="bbefc-169">Amortisman etkisi</span><span class="sxs-lookup"><span data-stu-id="bbefc-169">Depreciation effect</span></span>

| <span data-ttu-id="bbefc-170">Tarih</span><span class="sxs-lookup"><span data-stu-id="bbefc-170">Date</span></span>        | <span data-ttu-id="bbefc-171">Hareket türü</span><span class="sxs-lookup"><span data-stu-id="bbefc-171">Transaction type</span></span>        | <span data-ttu-id="bbefc-172">Tutar</span><span class="sxs-lookup"><span data-stu-id="bbefc-172">Amount</span></span>                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbefc-173">28 Şubat</span><span class="sxs-lookup"><span data-stu-id="bbefc-173">February 28</span></span> | <span data-ttu-id="bbefc-174">Amortisman (teklif)</span><span class="sxs-lookup"><span data-stu-id="bbefc-174">Depreciation (proposal)</span></span> | <span data-ttu-id="bbefc-175">983,62Hesaplaması: Defter değeri (59.000 - 966,67 amortisman) / kalan amortisman dönemi sayısı (59)</span><span class="sxs-lookup"><span data-stu-id="bbefc-175">983.62Calculation: Book value (59,000 - 966.67 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="bbefc-176">Amortisman 16,95 değeri kadar daha az belirtilir (983,62 - 966,67).</span><span class="sxs-lookup"><span data-stu-id="bbefc-176">Depreciation is understated by 16.95 (983.62 - 966.67).</span></span>



## <a name="additional-resources"></a><span data-ttu-id="bbefc-177">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="bbefc-177">Additional resources</span></span>

[<span data-ttu-id="bbefc-178">Sabit kıymet amortismanı</span><span class="sxs-lookup"><span data-stu-id="bbefc-178">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]