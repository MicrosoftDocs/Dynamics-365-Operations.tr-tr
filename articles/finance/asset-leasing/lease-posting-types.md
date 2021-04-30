---
title: Kira deftere nakil türleri
description: Bu konuda, varlık kiralama hareketleri için kullanılan deftere nakil türleri açıklanmıştır.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1d76c7ea72346c432db04bbe7947dea0c2911ea8
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881144"
---
# <a name="lease-posting-types"></a><span data-ttu-id="6bb25-103">Kira deftere nakil türleri</span><span class="sxs-lookup"><span data-stu-id="6bb25-103">Lease posting types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6bb25-104">Bu konuda, varlık kiralama hareketleri için kullanılan deftere nakil türleri açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="6bb25-104">This topic describes the posting types that are used for asset leasing transactions.</span></span>

## <a name="lease-asset"></a><span data-ttu-id="6bb25-105">Kiralama kıymeti</span><span class="sxs-lookup"><span data-stu-id="6bb25-105">Lease asset</span></span>

<span data-ttu-id="6bb25-106">Hesap, kullanım hakkı (ROU) varlığıyla ilişkilidir.</span><span class="sxs-lookup"><span data-stu-id="6bb25-106">The account is associated with the right-of-use (ROU) asset.</span></span> <span data-ttu-id="6bb25-107">Kiralama; yeni kiralama muhasebe standartları, Muhasabe Standartları Kodlaması Konu 842 (ASC 842) ve Uluslararası Mali Raporlama Standardı 16 (IFRS 16) kapsamında ilk kez kabul edildiğinde hesap borçlandırılır.</span><span class="sxs-lookup"><span data-stu-id="6bb25-107">This account is debited when a lease is initially recognized under the new lease accounting standards, Accounting Standards Codification Topic 842 (ASC 842) and International Financial Reporting Standard 16 (IFRS 16).</span></span> <span data-ttu-id="6bb25-108">Değiştirilmiş bir kiralama için, bu hesap, değişikliğin kira yükümlülüğünü artırmasına veya azaltmasına bağlı olarak borçlandırılabilir veya alacaklandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="6bb25-108">For a modified lease, this account might be either debited or credited, depending on whether the modification increases or decreases the lease liability.</span></span>

<span data-ttu-id="6bb25-109">**Örnek günlük girişleri**: İlk kabul</span><span class="sxs-lookup"><span data-stu-id="6bb25-109">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="6bb25-110">**Borç**: Kiralama varlığı XXX</span><span class="sxs-lookup"><span data-stu-id="6bb25-110">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="6bb25-111">**Alacak**: Kiralama yükümlülüğü XXX</span><span class="sxs-lookup"><span data-stu-id="6bb25-111">**Credit:** Lease liability XXX</span></span>

## <a name="lease-liability"></a><span data-ttu-id="6bb25-112">Kiralama yükümlülüğü</span><span class="sxs-lookup"><span data-stu-id="6bb25-112">Lease liability</span></span>

<span data-ttu-id="6bb25-113">Hesap, yeni IFRS 16 ve ASC 842 standartları kapsamında ödemelere iskonto uygulandığında oluşan kira yükümlülüğüyle ilişkilidir.</span><span class="sxs-lookup"><span data-stu-id="6bb25-113">The account is associated with the lease liability that occurs when payments are discounted under the new IFRS 16 and ASC 842 standards.</span></span> <span data-ttu-id="6bb25-114">Bu hesap, bir kiralama yeni standartlar kapsamında ilk kez kabul edildiğinde alacaklandırılır.</span><span class="sxs-lookup"><span data-stu-id="6bb25-114">This account is credited when a lease is initially recognized under the new standards.</span></span> <span data-ttu-id="6bb25-115">Kira ödemeleri için borçlandırılır ve faiz tahakkukları için alacaklandırılır.</span><span class="sxs-lookup"><span data-stu-id="6bb25-115">It's debited for lease payments and credited for interest accruals.</span></span>

<span data-ttu-id="6bb25-116">**Örnek günlük girişleri**: İlk kabul</span><span class="sxs-lookup"><span data-stu-id="6bb25-116">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="6bb25-117">**Borç**: Kiralama varlığı XXX</span><span class="sxs-lookup"><span data-stu-id="6bb25-117">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="6bb25-118">**Alacak**: Kiralama yükümlülüğü XXX</span><span class="sxs-lookup"><span data-stu-id="6bb25-118">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="6bb25-119">**Örnek günlük girişleri**: Faiz tahakkuku</span><span class="sxs-lookup"><span data-stu-id="6bb25-119">**Example journal entries:** Interest accrual</span></span><br>
<span data-ttu-id="6bb25-120">**Borç**: Faiz gideri XXX</span><span class="sxs-lookup"><span data-stu-id="6bb25-120">**Debit:** Interest expense XXX</span></span><br>
<span data-ttu-id="6bb25-121">**Alacak**: Kiralama yükümlülüğü XXX</span><span class="sxs-lookup"><span data-stu-id="6bb25-121">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="6bb25-122">**Örnek günlük girişleri**: Kira ödemesi</span><span class="sxs-lookup"><span data-stu-id="6bb25-122">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="6bb25-123">**Borç**: Kiralama yükümlülüğü XXX</span><span class="sxs-lookup"><span data-stu-id="6bb25-123">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="6bb25-124">**Alacak**: Satıcı borç/kira ödemesi XXX</span><span class="sxs-lookup"><span data-stu-id="6bb25-124">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="short-term-lease-liability"></a><span data-ttu-id="6bb25-125">Kısa süreli kiralama yükümlülüğü</span><span class="sxs-lookup"><span data-stu-id="6bb25-125">Short-term lease liability</span></span>

<span data-ttu-id="6bb25-126">Kısa süreli kiralama yükümlülüğü yeniden sınıflandırma günlük girişi deftere nakledildiğinde, hesap kısa süreli kira yükümlülüğüyle ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="6bb25-126">The account is associated with the short-term lease liability when the short-term lease liability reclass journal entry is posted.</span></span> <span data-ttu-id="6bb25-127">Bu hesap, ayın son günündeki amortisman planında kısa süreli yükümlülük için alacaklandırılır.</span><span class="sxs-lookup"><span data-stu-id="6bb25-127">This account is credited for the short-term liability from the amortization schedule on the last day of the month.</span></span> <span data-ttu-id="6bb25-128">Ancak, aynı tutar sonraki ayın ilk gününe borç olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="6bb25-128">However, the same amount is debited on the first day of the next month.</span></span>

<span data-ttu-id="6bb25-129">**Örnek günlük girişleri**: Kısa süreli kira yükümlülüğü yeniden sınıflandırma</span><span class="sxs-lookup"><span data-stu-id="6bb25-129">**Example journal entries:** Short-term lease liability reclass</span></span><br>
<span data-ttu-id="6bb25-130">**Borç**: Kiralama yükümlülüğü XXX</span><span class="sxs-lookup"><span data-stu-id="6bb25-130">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="6bb25-131">**Alacak**: Kısa süreli kiralama yükümlülüğü XXX</span><span class="sxs-lookup"><span data-stu-id="6bb25-131">**Credit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="6bb25-132">**Borç**: Kısa süreli kiralama yükümlülüğü XXX</span><span class="sxs-lookup"><span data-stu-id="6bb25-132">**Debit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="6bb25-133">**Alacak**: Kiralama yükümlülüğü XXX</span><span class="sxs-lookup"><span data-stu-id="6bb25-133">**Credit:** Lease liability XXX</span></span>

## <a name="depreciation-expense"></a><span data-ttu-id="6bb25-134">Amortisman gideri</span><span class="sxs-lookup"><span data-stu-id="6bb25-134">Depreciation expense</span></span>

<span data-ttu-id="6bb25-135">Hesap, IFRS 16, ASC 842 ve IAS 17 ile ASC 840 kapsamındaki finansal kiralamalar kapsamındaki ROU valrığının amortismanıyla ilgili giderle ilişkilidir.</span><span class="sxs-lookup"><span data-stu-id="6bb25-135">The account is associated with the expense that is related to the depreciation of the ROU asset under IFRS 16, ASC 842, and finance leases under IAS 17 and ASC 840.</span></span> <span data-ttu-id="6bb25-136">Her ay ROU varlığına amortisman uygulandığında bu hesaba borç kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="6bb25-136">This account is debited when an ROU asset is depreciated each month.</span></span>

<span data-ttu-id="6bb25-137">**Örnek günlük girişleri**: Amortisman tahakkuku</span><span class="sxs-lookup"><span data-stu-id="6bb25-137">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="6bb25-138">**Borç**: Amortisman gideri XXX</span><span class="sxs-lookup"><span data-stu-id="6bb25-138">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="6bb25-139">**Alacak:** Birikmiş Amortisman XXX</span><span class="sxs-lookup"><span data-stu-id="6bb25-139">**Credit:** Accumulated Depreciation XXX</span></span>

## <a name="gainloss-on-lease-modification"></a><span data-ttu-id="6bb25-140">Kiralama değişikliğinde kazanç/kayıp</span><span class="sxs-lookup"><span data-stu-id="6bb25-140">Gain/loss on lease modification</span></span>

<span data-ttu-id="6bb25-141">Hesap, kiralama değişikliklerinden doğan tüm kazanç veya kayıplarla ilişkilidir.</span><span class="sxs-lookup"><span data-stu-id="6bb25-141">The account is associated with any gains or losses that arise from lease modifications.</span></span> <span data-ttu-id="6bb25-142">Değişiklik, kiralama yükümlülüğünü ROU varlığının defter değerini aşacak bir tutarda azaltırsa kiralama değişikliği sırasında bir kazanç oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="6bb25-142">A gain might arise during a lease modification if the modification decreases the lease liability by an amount that exceeds the carrying value of the ROU asset.</span></span>

<span data-ttu-id="6bb25-143">Örneğin, bir kiralamanın kiralama yükümlülüğü geçerli defter değerinin 150.000 ABD doları ve ROU varlığının defter değerinin 100.000 ABD doları olduğunu düşünelim.</span><span class="sxs-lookup"><span data-stu-id="6bb25-143">For example, a lease has a current carrying value of the lease liability of $150,000 and a carrying value of the ROU asset of $100,000.</span></span> <span data-ttu-id="6bb25-144">Kira değiştirilir ve bu değişiklik gelecekteki en düşük kira ödemelerinin (PVFMLP) yeni bir şimdiki değerini oluşturur (40.000 ABD doları).</span><span class="sxs-lookup"><span data-stu-id="6bb25-144">The lease is modified, and this modification produces a new present value of the future minimum lease payments (PVFMLP) of $40,000.</span></span> <span data-ttu-id="6bb25-145">Bu nedenle, kiralama yükümlülüğü 110.000 (150.000 – 40.000) (ABD doları) ile borç kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="6bb25-145">Therefore, the lease liability will be debited by $110,000 ($150,000 – $40,000).</span></span> <span data-ttu-id="6bb25-146">ROU varlığı yalnızca 100.000 ABD doları olduğundan, 110.000 ABD doları tutarındaki azalma varlığı 0 (sıfır) değerinin altına düşürür.</span><span class="sxs-lookup"><span data-stu-id="6bb25-146">Because the ROU asset is only $100,000, the decrease of $110,000 will decrease the asset past 0 (zero).</span></span> <span data-ttu-id="6bb25-147">Bu nedenle, muhasebe kılavuzu kalan kısmın bir kazanç hesabına kaydedilmesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6bb25-147">Therefore, the accounting guidance states that the remainder should be booked to a gain account.</span></span> <span data-ttu-id="6bb25-148">Bu durumda, son günlük girişi kiralama yükümlülüğüne 110.000 ABD doları borç, kiralama varlığına 100.000 ABD doları alacak ve kazanç hesabına 10.000 ABD doları alacak olacaktır.</span><span class="sxs-lookup"><span data-stu-id="6bb25-148">In this case, the final journal entry will be a debit to the lease liability for $110,000, a credit to the lease asset for $100,000, and a credit to the gain account for $10,000.</span></span>

<span data-ttu-id="6bb25-149">**Örnek günlük girişleri**: Kiralama değişikliği</span><span class="sxs-lookup"><span data-stu-id="6bb25-149">**Example journal entries:** Lease modification</span></span><br>
<span data-ttu-id="6bb25-150">**Borç**: Kiralama yükümlülüğü XXX</span><span class="sxs-lookup"><span data-stu-id="6bb25-150">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="6bb25-151">**Alacak**: Kiralama Varlığı XXX</span><span class="sxs-lookup"><span data-stu-id="6bb25-151">**Credit:** Lease Asset XXX</span></span><br>
<span data-ttu-id="6bb25-152">**Alacak**: Kazanç XXX</span><span class="sxs-lookup"><span data-stu-id="6bb25-152">**Credit:** Gain XXX</span></span>

## <a name="accumulated-depreciation"></a><span data-ttu-id="6bb25-153">Birikmiş amortisman</span><span class="sxs-lookup"><span data-stu-id="6bb25-153">Accumulated depreciation</span></span>

<span data-ttu-id="6bb25-154">Hesap, ROU varlığının karşı varlık hesabıyla ilişkilidir.</span><span class="sxs-lookup"><span data-stu-id="6bb25-154">The account is associated with the contra-asset account of the ROU asset.</span></span> <span data-ttu-id="6bb25-155">Bu hesap, bir amortisman gideri deftere nakledildiğinde alacaklandırılır.</span><span class="sxs-lookup"><span data-stu-id="6bb25-155">This account is credited when a depreciation expense is posted.</span></span>

<span data-ttu-id="6bb25-156">**Örnek günlük girişleri**: Amortisman tahakkuku</span><span class="sxs-lookup"><span data-stu-id="6bb25-156">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="6bb25-157">**Borç**: Amortisman gideri XXX</span><span class="sxs-lookup"><span data-stu-id="6bb25-157">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="6bb25-158">**Alacak:** Birikmiş amortisman XXX</span><span class="sxs-lookup"><span data-stu-id="6bb25-158">**Credit:** Accumulated depreciation XXX</span></span>

## <a name="variable-payment"></a><span data-ttu-id="6bb25-159">Değişken ödeme</span><span class="sxs-lookup"><span data-stu-id="6bb25-159">Variable payment</span></span>

<span data-ttu-id="6bb25-160">Hesap, ASC 842, ASC 840 ve IAS 17 kiralamaları kapsamında endeks yeniden değerleme tarafından oluşturulan değişken kira ödemeleriyle ilişkilidir.</span><span class="sxs-lookup"><span data-stu-id="6bb25-160">The account is associated with variable lease payments that are produced by an index revaluation under ASC 842, ASC 840, and IAS 17 leases.</span></span> <span data-ttu-id="6bb25-161">Kira ödemesi planında değişken ödemeler **Değişken ödeme** sütununa dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="6bb25-161">In the lease payment schedule, variable payments are included in the **Variable payment** column.</span></span> <span data-ttu-id="6bb25-162">Değişken ödeme içeren bir ödeme planı satırı için fatura oluşturulduğunda, bu hesaba borç kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="6bb25-162">This account is debited when an invoice is created against a payment schedule line that contains a variable payment.</span></span>

<span data-ttu-id="6bb25-163">**Örnek günlük girişleri**: Kira ödemesi</span><span class="sxs-lookup"><span data-stu-id="6bb25-163">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="6bb25-164">**Borç**: Kiralama yükümlülüğü XXX</span><span class="sxs-lookup"><span data-stu-id="6bb25-164">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="6bb25-165">**Borç**: Değişken ödeme XXX</span><span class="sxs-lookup"><span data-stu-id="6bb25-165">**Debit:** Variable payment XXX</span></span><br>
<span data-ttu-id="6bb25-166">**Alacak**: Satıcı borç/kira ödemesi XXX</span><span class="sxs-lookup"><span data-stu-id="6bb25-166">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="deferred-rent-asset-liability"></a><span data-ttu-id="6bb25-167">Ertelenmiş kira varlığı (yükümlülüğü)</span><span class="sxs-lookup"><span data-stu-id="6bb25-167">Deferred rent asset (liability)</span></span>

<span data-ttu-id="6bb25-168">Bu hesap, ertelenmiş kira işlemi kiralaması tarafından oluşturulan ertelenmiş kira varlığı veya yükümlülüğü ile ilişkilidir.</span><span class="sxs-lookup"><span data-stu-id="6bb25-168">The account is associated with the deferred rent asset or liability that is produced by a deferred rent treatment lease.</span></span> <span data-ttu-id="6bb25-169">Kira ödemesi tutarı dönemin sabit esaslı kira giderinden fazlaysa ertelenmiş kira işlem kiralaması için fatura oluşturulduğunda bu hesaba borç kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="6bb25-169">This account is debited when an invoice is posted against a deferred rent treatment lease, if the lease payment amount is more than the period's straight-line rent expense.</span></span> <span data-ttu-id="6bb25-170">Kira ödemesi dönemin sabit esaslı kira giderinden azsa alacak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="6bb25-170">It's credited if the lease payment is less than the period's straight-line rent expense.</span></span>

<span data-ttu-id="6bb25-171">**Örnek günlük girişleri**: Kira ödemesi (ertelenmiş kira işlem kiralama)</span><span class="sxs-lookup"><span data-stu-id="6bb25-171">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="6bb25-172">**Borç**: Kiralama gideri XXX</span><span class="sxs-lookup"><span data-stu-id="6bb25-172">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="6bb25-173">**Alacak**: Ertelenmiş kira yükümlülüğü XXX</span><span class="sxs-lookup"><span data-stu-id="6bb25-173">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="6bb25-174">**Alacak**: Satıcı borç/kira ödemesi XXX</span><span class="sxs-lookup"><span data-stu-id="6bb25-174">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="lease-expense"></a><span data-ttu-id="6bb25-175">Kiralama gideri</span><span class="sxs-lookup"><span data-stu-id="6bb25-175">Lease expense</span></span>

<span data-ttu-id="6bb25-176">Kiralama ertelenmiş kira işlem kiralaması olarak sınıflandırılırsa hesap kiralama gideriyle ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="6bb25-176">The account is associated with the lease expense if the lease is classified as a deferred rent treatment lease.</span></span> <span data-ttu-id="6bb25-177">Ertelenmiş kira işlem kiralaması için bir fatura oluşturulduğunda bu hesaba borç kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="6bb25-177">This account is debited when an invoice is posted against a deferred rent treatment lease.</span></span>

<span data-ttu-id="6bb25-178">**Örnek günlük girişleri**: Kira ödemesi (ertelenmiş kira işlem kiralama)</span><span class="sxs-lookup"><span data-stu-id="6bb25-178">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="6bb25-179">**Borç**: Kiralama gideri XXX</span><span class="sxs-lookup"><span data-stu-id="6bb25-179">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="6bb25-180">**Alacak**: Ertelenmiş kira yükümlülüğü XXX</span><span class="sxs-lookup"><span data-stu-id="6bb25-180">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="6bb25-181">**Alacak**: Satıcı borç/kira ödemesi XXX</span><span class="sxs-lookup"><span data-stu-id="6bb25-181">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="impairment-expense"></a><span data-ttu-id="6bb25-182">Değer düşüşü gideri</span><span class="sxs-lookup"><span data-stu-id="6bb25-182">Impairment expense</span></span>

<span data-ttu-id="6bb25-183">Bir kiralamanın değeri düşürüldüğünde hesap deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="6bb25-183">The account is posted against when a lease is impaired.</span></span> <span data-ttu-id="6bb25-184">Bu hesap borçlandırılır ancak ROU varlığı hesabı doğrudan alacaklandırılır.</span><span class="sxs-lookup"><span data-stu-id="6bb25-184">This account is debited, whereas the ROU asset account is directly credited.</span></span>

<span data-ttu-id="6bb25-185">**Örnek günlük girişleri**: Kira ödemesi</span><span class="sxs-lookup"><span data-stu-id="6bb25-185">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="6bb25-186">**Borç:** Değer düşüşü gideri XXX</span><span class="sxs-lookup"><span data-stu-id="6bb25-186">**Debit:** Impairment expense XXX</span></span><br>
<span data-ttu-id="6bb25-187">**Alacak**: ROU varlığı XXX</span><span class="sxs-lookup"><span data-stu-id="6bb25-187">**Credit:** ROU asset XXX</span></span>

## <a name="lease-payment"></a><span data-ttu-id="6bb25-188">Kira ödemesi</span><span class="sxs-lookup"><span data-stu-id="6bb25-188">Lease payment</span></span>

<span data-ttu-id="6bb25-189">**Satıcıya Öde** parametresi kapalıysa hesap deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="6bb25-189">The account is posted against if the **Pay to Vendor** parameter is turned off.</span></span> <span data-ttu-id="6bb25-190">Parametre kapatılmışsa satıcı borcu yerine bu hesap alacaklandırılır.</span><span class="sxs-lookup"><span data-stu-id="6bb25-190">This account is credited instead of the vendor payable if the parameter is turned off.</span></span>

<span data-ttu-id="6bb25-191">**Örnek günlük girişleri**: Kira ödemesi</span><span class="sxs-lookup"><span data-stu-id="6bb25-191">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="6bb25-192">**Borç**: Kiralama yükümlülüğü XXX</span><span class="sxs-lookup"><span data-stu-id="6bb25-192">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="6bb25-193">**Alacak**: Kira ödemesi XXX</span><span class="sxs-lookup"><span data-stu-id="6bb25-193">**Credit:** Lease payment XXX</span></span>

## <a name="expense-type-postings"></a><span data-ttu-id="6bb25-194">Gider türü deftere nakiller</span><span class="sxs-lookup"><span data-stu-id="6bb25-194">Expense type postings</span></span>

<span data-ttu-id="6bb25-195">Her gider türü için seçilen hesap, ilgili gider türü için bir ödeme oluşturulduğunda borçlandırılır.</span><span class="sxs-lookup"><span data-stu-id="6bb25-195">The account that is selected for each expense type is debited when a payment for that expense type is generated.</span></span> <span data-ttu-id="6bb25-196">Örneğin, **Sigorta** gider türü için belirtilen bir hesap, sigorta gideri için icra maliyeti planından bir fatura veya ödeme günlük giriş oluşturulduğunda borçlandırılır.</span><span class="sxs-lookup"><span data-stu-id="6bb25-196">For example, the account that is specified for the **Insurance** expense type is debited whenever an invoice or payment journal entry is created from the executory cost schedule for insurance expense.</span></span>

<span data-ttu-id="6bb25-197">**Örnek günlük girişleri**: Sigorta ödemesi</span><span class="sxs-lookup"><span data-stu-id="6bb25-197">**Example journal entries:** Insurance payment</span></span><br>
<span data-ttu-id="6bb25-198">**Borç**: Sigorta gideri türü hesabı XXX</span><span class="sxs-lookup"><span data-stu-id="6bb25-198">**Debit:** Insurance expense type account XXX</span></span><br>
<span data-ttu-id="6bb25-199">**Alacak**: Mahsup hesap XXX</span><span class="sxs-lookup"><span data-stu-id="6bb25-199">**Credit:** Offset account XXX</span></span>

> [!NOTE]
> <span data-ttu-id="6bb25-200">Mahsup hesap, icra maliyeti ödeme planı için satırlardaki kiralama düzeyinde seçilir.</span><span class="sxs-lookup"><span data-stu-id="6bb25-200">The offset account is selected at the lease level on the lines for the executory cost payment schedule.</span></span> <span data-ttu-id="6bb25-201">Bu mahsup hesap, satıcıyla veya bir genel muhasebe hesabıyla ilişkilendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="6bb25-201">This offset account can associated with the vendor, or with a ledger account.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
