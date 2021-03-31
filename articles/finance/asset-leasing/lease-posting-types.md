---
title: Kira deftere nakil türleri
description: Bu konuda, varlık kiralama hareketleri için kullanılan deftere nakil türleri açıklanmıştır.
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
ms.openlocfilehash: 9b7d8c545c1addaa570d54855bbad6c576783007
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5229514"
---
# <a name="lease-posting-types"></a><span data-ttu-id="6ea9e-103">Kira deftere nakil türleri</span><span class="sxs-lookup"><span data-stu-id="6ea9e-103">Lease posting types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ea9e-104">Bu konuda, varlık kiralama hareketleri için kullanılan deftere nakil türleri açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-104">This topic describes the posting types that are used for asset leasing transactions.</span></span>

## <a name="lease-asset"></a><span data-ttu-id="6ea9e-105">Kiralama kıymeti</span><span class="sxs-lookup"><span data-stu-id="6ea9e-105">Lease asset</span></span>

<span data-ttu-id="6ea9e-106">Hesap, kullanım hakkı (ROU) varlığıyla ilişkilidir.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-106">The account is associated with the right-of-use (ROU) asset.</span></span> <span data-ttu-id="6ea9e-107">Kiralama; yeni kiralama muhasebe standartları, Muhasabe Standartları Kodlaması Konu 842 (ASC 842) ve Uluslararası Mali Raporlama Standardı 16 (IFRS 16) kapsamında ilk kez kabul edildiğinde hesap borçlandırılır.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-107">This account is debited when a lease is initially recognized under the new lease accounting standards, Accounting Standards Codification Topic 842 (ASC 842) and International Financial Reporting Standard 16 (IFRS 16).</span></span> <span data-ttu-id="6ea9e-108">Değiştirilmiş bir kiralama için, bu hesap, değişikliğin kira yükümlülüğünü artırmasına veya azaltmasına bağlı olarak borçlandırılabilir veya alacaklandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-108">For a modified lease, this account might be either debited or credited, depending on whether the modification increases or decreases the lease liability.</span></span>

<span data-ttu-id="6ea9e-109">**Örnek günlük girişleri**: İlk kabul</span><span class="sxs-lookup"><span data-stu-id="6ea9e-109">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="6ea9e-110">**Borç**: Kiralama varlığı XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-110">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="6ea9e-111">**Alacak**: Kiralama yükümlülüğü XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-111">**Credit:** Lease liability XXX</span></span>

## <a name="lease-liability"></a><span data-ttu-id="6ea9e-112">Kiralama yükümlülüğü</span><span class="sxs-lookup"><span data-stu-id="6ea9e-112">Lease liability</span></span>

<span data-ttu-id="6ea9e-113">Hesap, yeni IFRS 16 ve ASC 842 standartları kapsamında ödemelere iskonto uygulandığında oluşan kira yükümlülüğüyle ilişkilidir.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-113">The account is associated with the lease liability that occurs when payments are discounted under the new IFRS 16 and ASC 842 standards.</span></span> <span data-ttu-id="6ea9e-114">Bu hesap, bir kiralama yeni standartlar kapsamında ilk kez kabul edildiğinde alacaklandırılır.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-114">This account is credited when a lease is initially recognized under the new standards.</span></span> <span data-ttu-id="6ea9e-115">Kira ödemeleri için borçlandırılır ve faiz tahakkukları için alacaklandırılır.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-115">It's debited for lease payments and credited for interest accruals.</span></span>

<span data-ttu-id="6ea9e-116">**Örnek günlük girişleri**: İlk kabul</span><span class="sxs-lookup"><span data-stu-id="6ea9e-116">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="6ea9e-117">**Borç**: Kiralama varlığı XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-117">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="6ea9e-118">**Alacak**: Kiralama yükümlülüğü XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-118">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="6ea9e-119">**Örnek günlük girişleri**: Faiz tahakkuku</span><span class="sxs-lookup"><span data-stu-id="6ea9e-119">**Example journal entries:** Interest accrual</span></span><br>
<span data-ttu-id="6ea9e-120">**Borç**: Faiz gideri XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-120">**Debit:** Interest expense XXX</span></span><br>
<span data-ttu-id="6ea9e-121">**Alacak**: Kiralama yükümlülüğü XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-121">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="6ea9e-122">**Örnek günlük girişleri**: Kira ödemesi</span><span class="sxs-lookup"><span data-stu-id="6ea9e-122">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="6ea9e-123">**Borç**: Kiralama yükümlülüğü XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-123">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="6ea9e-124">**Alacak**: Satıcı borç/kira ödemesi XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-124">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="short-term-lease-liability"></a><span data-ttu-id="6ea9e-125">Kısa süreli kiralama yükümlülüğü</span><span class="sxs-lookup"><span data-stu-id="6ea9e-125">Short-term lease liability</span></span>

<span data-ttu-id="6ea9e-126">Kısa süreli kiralama yükümlülüğü yeniden sınıflandırma günlük girişi deftere nakledildiğinde, hesap kısa süreli kira yükümlülüğüyle ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-126">The account is associated with the short-term lease liability when the short-term lease liability reclass journal entry is posted.</span></span> <span data-ttu-id="6ea9e-127">Bu hesap, ayın son günündeki amortisman planında kısa süreli yükümlülük için alacaklandırılır.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-127">This account is credited for the short-term liability from the amortization schedule on the last day of the month.</span></span> <span data-ttu-id="6ea9e-128">Ancak, aynı tutar sonraki ayın ilk gününe borç olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-128">However, the same amount is debited on the first day of the next month.</span></span>

<span data-ttu-id="6ea9e-129">**Örnek günlük girişleri**: Kısa süreli kira yükümlülüğü yeniden sınıflandırma</span><span class="sxs-lookup"><span data-stu-id="6ea9e-129">**Example journal entries:** Short-term lease liability reclass</span></span><br>
<span data-ttu-id="6ea9e-130">**Borç**: Kiralama yükümlülüğü XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-130">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="6ea9e-131">**Alacak**: Kısa süreli kiralama yükümlülüğü XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-131">**Credit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="6ea9e-132">**Borç**: Kısa süreli kiralama yükümlülüğü XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-132">**Debit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="6ea9e-133">**Alacak**: Kiralama yükümlülüğü XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-133">**Credit:** Lease liability XXX</span></span>

## <a name="depreciation-expense"></a><span data-ttu-id="6ea9e-134">Amortisman gideri</span><span class="sxs-lookup"><span data-stu-id="6ea9e-134">Depreciation expense</span></span>

<span data-ttu-id="6ea9e-135">Hesap, IFRS 16, ASC 842 ve IAS 17 ile ASC 840 kapsamındaki finansal kiralamalar kapsamındaki ROU valrığının amortismanıyla ilgili giderle ilişkilidir.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-135">The account is associated with the expense that is related to the depreciation of the ROU asset under IFRS 16, ASC 842, and finance leases under IAS 17 and ASC 840.</span></span> <span data-ttu-id="6ea9e-136">Her ay ROU varlığına amortisman uygulandığında bu hesaba borç kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-136">This account is debited when an ROU asset is depreciated each month.</span></span>

<span data-ttu-id="6ea9e-137">**Örnek günlük girişleri**: Amortisman tahakkuku</span><span class="sxs-lookup"><span data-stu-id="6ea9e-137">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="6ea9e-138">**Borç**: Amortisman gideri XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-138">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="6ea9e-139">**Alacak:** Birikmiş Amortisman XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-139">**Credit:** Accumulated Depreciation XXX</span></span>

## <a name="gainloss-on-lease-modification"></a><span data-ttu-id="6ea9e-140">Kiralama değişikliğinde kazanç/kayıp</span><span class="sxs-lookup"><span data-stu-id="6ea9e-140">Gain/loss on lease modification</span></span>

<span data-ttu-id="6ea9e-141">Hesap, kiralama değişikliklerinden doğan tüm kazanç veya kayıplarla ilişkilidir.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-141">The account is associated with any gains or losses that arise from lease modifications.</span></span> <span data-ttu-id="6ea9e-142">Değişiklik, kiralama yükümlülüğünü ROU varlığının defter değerini aşacak bir tutarda azaltırsa kiralama değişikliği sırasında bir kazanç oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-142">A gain might arise during a lease modification if the modification decreases the lease liability by an amount that exceeds the carrying value of the ROU asset.</span></span>

<span data-ttu-id="6ea9e-143">Örneğin, bir kiralamanın kiralama yükümlülüğü geçerli defter değerinin 150.000 ABD doları ve ROU varlığının defter değerinin 100.000 ABD doları olduğunu düşünelim.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-143">For example, a lease has a current carrying value of the lease liability of $150,000 and a carrying value of the ROU asset of $100,000.</span></span> <span data-ttu-id="6ea9e-144">Kira değiştirilir ve bu değişiklik gelecekteki en düşük kira ödemelerinin (PVFMLP) yeni bir şimdiki değerini oluşturur (40.000 ABD doları).</span><span class="sxs-lookup"><span data-stu-id="6ea9e-144">The lease is modified, and this modification produces a new present value of the future minimum lease payments (PVFMLP) of $40,000.</span></span> <span data-ttu-id="6ea9e-145">Bu nedenle, kiralama yükümlülüğü 110.000 (150.000 – 40.000) (ABD doları) ile borç kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-145">Therefore, the lease liability will be debited by $110,000 ($150,000 – $40,000).</span></span> <span data-ttu-id="6ea9e-146">ROU varlığı yalnızca 100.000 ABD doları olduğundan, 110.000 ABD doları tutarındaki azalma varlığı 0 (sıfır) değerinin altına düşürür.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-146">Because the ROU asset is only $100,000, the decrease of $110,000 will decrease the asset past 0 (zero).</span></span> <span data-ttu-id="6ea9e-147">Bu nedenle, muhasebe kılavuzu kalan kısmın bir kazanç hesabına kaydedilmesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-147">Therefore, the accounting guidance states that the remainder should be booked to a gain account.</span></span> <span data-ttu-id="6ea9e-148">Bu durumda, son günlük girişi kiralama yükümlülüğüne 110.000 ABD doları borç, kiralama varlığına 100.000 ABD doları alacak ve kazanç hesabına 10.000 ABD doları alacak olacaktır.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-148">In this case, the final journal entry will be a debit to the lease liability for $110,000, a credit to the lease asset for $100,000, and a credit to the gain account for $10,000.</span></span>

<span data-ttu-id="6ea9e-149">**Örnek günlük girişleri**: Kiralama değişikliği</span><span class="sxs-lookup"><span data-stu-id="6ea9e-149">**Example journal entries:** Lease modification</span></span><br>
<span data-ttu-id="6ea9e-150">**Borç**: Kiralama yükümlülüğü XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-150">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="6ea9e-151">**Alacak**: Kiralama Varlığı XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-151">**Credit:** Lease Asset XXX</span></span><br>
<span data-ttu-id="6ea9e-152">**Alacak**: Kazanç XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-152">**Credit:** Gain XXX</span></span>

## <a name="accumulated-depreciation"></a><span data-ttu-id="6ea9e-153">Birikmiş amortisman</span><span class="sxs-lookup"><span data-stu-id="6ea9e-153">Accumulated depreciation</span></span>

<span data-ttu-id="6ea9e-154">Hesap, ROU varlığının karşı varlık hesabıyla ilişkilidir.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-154">The account is associated with the contra-asset account of the ROU asset.</span></span> <span data-ttu-id="6ea9e-155">Bu hesap, bir amortisman gideri deftere nakledildiğinde alacaklandırılır.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-155">This account is credited when a depreciation expense is posted.</span></span>

<span data-ttu-id="6ea9e-156">**Örnek günlük girişleri**: Amortisman tahakkuku</span><span class="sxs-lookup"><span data-stu-id="6ea9e-156">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="6ea9e-157">**Borç**: Amortisman gideri XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-157">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="6ea9e-158">**Alacak:** Birikmiş amortisman XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-158">**Credit:** Accumulated depreciation XXX</span></span>

## <a name="retained-earnings"></a><span data-ttu-id="6ea9e-159">Yedek akçe</span><span class="sxs-lookup"><span data-stu-id="6ea9e-159">Retained earnings</span></span>

<span data-ttu-id="6ea9e-160">Bu hesap, dağıtılmamış kazançlarla ilişkilidir.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-160">The account is associated with retained earnings.</span></span> <span data-ttu-id="6ea9e-161">Bu hesap, tam geriye dönük yöntem veya kümülatif yakalama seçeneği A yöntemi kullanılarak bir geçiş düzeltme günlüğü girişinde borçlandırılabilir veya alacaklandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-161">This account might be either debited or credited in a transition adjustment journal entry by using the full retrospective method or the cumulative catch-up option A method.</span></span> <span data-ttu-id="6ea9e-162">İlk ROU varlığı ile kiralama yükümlülüğü arasındaki fark, dağıtılmamış kazançlara kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-162">The difference between the initial ROU asset and lease liability is booked to retained earnings.</span></span> <span data-ttu-id="6ea9e-163">Nadiren de olsa, ROU varlığının kiralama yükümlülüğüne eşit olması için değerinin artırılması veya azaltılması amacıyla kiralama sınıflandırmasının finansaldan işletmeye geçmesi durumunda kalan kazançlar da kiralama değişikliğinden etkilenebilir.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-163">In rare cases, the retained earnings might also be affected during lease modification, if the classification of a lease is changed from finance to operating to write the ROU asset up or down so that it equals the lease liability.</span></span>

<span data-ttu-id="6ea9e-164">**Örnek günlük girişleri**: Geçiş düzeltmesi (tam geriye dönük veya kümülatif yakalama seçeneği A yöntemi)</span><span class="sxs-lookup"><span data-stu-id="6ea9e-164">**Example journal entries:** Transition adjustment (full retrospective or cumulative catch-up option A method)</span></span><br>
<span data-ttu-id="6ea9e-165">**Borç**: Kiralama yükümlülüğü XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-165">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="6ea9e-166">**Alacak**: Kiralama varlığı XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-166">**Credit:** Lease asset XXX</span></span><br>
<span data-ttu-id="6ea9e-167">**Alacak**: Dağıtılmamış kazançlar xxx</span><span class="sxs-lookup"><span data-stu-id="6ea9e-167">**Credit:** Retained earnings XXX</span></span>

## <a name="variable-payment"></a><span data-ttu-id="6ea9e-168">Değişken ödeme</span><span class="sxs-lookup"><span data-stu-id="6ea9e-168">Variable payment</span></span>

<span data-ttu-id="6ea9e-169">Hesap, ASC 842, ASC 840 ve IAS 17 kiralamaları kapsamında endeks yeniden değerleme tarafından oluşturulan değişken kira ödemeleriyle ilişkilidir.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-169">The account is associated with variable lease payments that are produced by an index revaluation under ASC 842, ASC 840, and IAS 17 leases.</span></span> <span data-ttu-id="6ea9e-170">Kira ödemesi planında değişken ödemeler **Değişken ödeme** sütununa dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-170">In the lease payment schedule, variable payments are included in the **Variable payment** column.</span></span> <span data-ttu-id="6ea9e-171">Değişken ödeme içeren bir ödeme planı satırı için fatura oluşturulduğunda, bu hesaba borç kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-171">This account is debited when an invoice is created against a payment schedule line that contains a variable payment.</span></span>

<span data-ttu-id="6ea9e-172">**Örnek günlük girişleri**: Kira ödemesi</span><span class="sxs-lookup"><span data-stu-id="6ea9e-172">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="6ea9e-173">**Borç**: Kiralama yükümlülüğü XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-173">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="6ea9e-174">**Borç**: Değişken ödeme XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-174">**Debit:** Variable payment XXX</span></span><br>
<span data-ttu-id="6ea9e-175">**Alacak**: Satıcı borç/kira ödemesi XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-175">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="deferred-rent-asset-liability"></a><span data-ttu-id="6ea9e-176">Ertelenmiş kira varlığı (yükümlülüğü)</span><span class="sxs-lookup"><span data-stu-id="6ea9e-176">Deferred rent asset (liability)</span></span>

<span data-ttu-id="6ea9e-177">Bu hesap, ertelenmiş kira işlemi kiralaması tarafından oluşturulan ertelenmiş kira varlığı veya yükümlülüğü ile ilişkilidir.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-177">The account is associated with the deferred rent asset or liability that is produced by a deferred rent treatment lease.</span></span> <span data-ttu-id="6ea9e-178">Kira ödemesi tutarı dönemin sabit esaslı kira giderinden fazlaysa ertelenmiş kira işlem kiralaması için fatura oluşturulduğunda bu hesaba borç kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-178">This account is debited when an invoice is posted against a deferred rent treatment lease, if the lease payment amount is more than the period's straight-line rent expense.</span></span> <span data-ttu-id="6ea9e-179">Kira ödemesi dönemin sabit esaslı kira giderinden azsa alacak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-179">It's credited if the lease payment is less than the period's straight-line rent expense.</span></span>

<span data-ttu-id="6ea9e-180">**Örnek günlük girişleri**: Kira ödemesi (ertelenmiş kira işlem kiralama)</span><span class="sxs-lookup"><span data-stu-id="6ea9e-180">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="6ea9e-181">**Borç**: Kiralama gideri XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-181">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="6ea9e-182">**Alacak**: Ertelenmiş kira yükümlülüğü XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-182">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="6ea9e-183">**Alacak**: Satıcı borç/kira ödemesi XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-183">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="lease-expense"></a><span data-ttu-id="6ea9e-184">Kiralama gideri</span><span class="sxs-lookup"><span data-stu-id="6ea9e-184">Lease expense</span></span>

<span data-ttu-id="6ea9e-185">Kiralama ertelenmiş kira işlem kiralaması olarak sınıflandırılırsa hesap kiralama gideriyle ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-185">The account is associated with the lease expense if the lease is classified as a deferred rent treatment lease.</span></span> <span data-ttu-id="6ea9e-186">Ertelenmiş kira işlem kiralaması için bir fatura oluşturulduğunda bu hesaba borç kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-186">This account is debited when an invoice is posted against a deferred rent treatment lease.</span></span>

<span data-ttu-id="6ea9e-187">**Örnek günlük girişleri**: Kira ödemesi (ertelenmiş kira işlem kiralama)</span><span class="sxs-lookup"><span data-stu-id="6ea9e-187">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="6ea9e-188">**Borç**: Kiralama gideri XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-188">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="6ea9e-189">**Alacak**: Ertelenmiş kira yükümlülüğü XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-189">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="6ea9e-190">**Alacak**: Satıcı borç/kira ödemesi XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-190">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="impairment-expense"></a><span data-ttu-id="6ea9e-191">Değer düşüşü gideri</span><span class="sxs-lookup"><span data-stu-id="6ea9e-191">Impairment expense</span></span>

<span data-ttu-id="6ea9e-192">Bir kiralamanın değeri düşürüldüğünde hesap deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-192">The account is posted against when a lease is impaired.</span></span> <span data-ttu-id="6ea9e-193">Bu hesap borçlandırılır ancak ROU varlığı hesabı doğrudan alacaklandırılır.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-193">This account is debited, whereas the ROU asset account is directly credited.</span></span>

<span data-ttu-id="6ea9e-194">**Örnek günlük girişleri**: Kira ödemesi</span><span class="sxs-lookup"><span data-stu-id="6ea9e-194">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="6ea9e-195">**Borç:** Değer düşüşü gideri XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-195">**Debit:** Impairment expense XXX</span></span><br>
<span data-ttu-id="6ea9e-196">**Alacak**: ROU varlığı XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-196">**Credit:** ROU asset XXX</span></span>

## <a name="lease-payment"></a><span data-ttu-id="6ea9e-197">Kira ödemesi</span><span class="sxs-lookup"><span data-stu-id="6ea9e-197">Lease payment</span></span>

<span data-ttu-id="6ea9e-198">**Satıcıya Öde** parametresi kapalıysa hesap deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-198">The account is posted against if the **Pay to Vendor** parameter is turned off.</span></span> <span data-ttu-id="6ea9e-199">Parametre kapatılmışsa satıcı borcu yerine bu hesap alacaklandırılır.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-199">This account is credited instead of the vendor payable if the parameter is turned off.</span></span>

<span data-ttu-id="6ea9e-200">**Örnek günlük girişleri**: Kira ödemesi</span><span class="sxs-lookup"><span data-stu-id="6ea9e-200">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="6ea9e-201">**Borç**: Kiralama yükümlülüğü XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-201">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="6ea9e-202">**Alacak**: Kira ödemesi XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-202">**Credit:** Lease payment XXX</span></span>

## <a name="expense-type-postings"></a><span data-ttu-id="6ea9e-203">Gider türü deftere nakiller</span><span class="sxs-lookup"><span data-stu-id="6ea9e-203">Expense type postings</span></span>

<span data-ttu-id="6ea9e-204">Her gider türü için seçilen hesap, ilgili gider türü için bir ödeme oluşturulduğunda borçlandırılır.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-204">The account that is selected for each expense type is debited when a payment for that expense type is generated.</span></span> <span data-ttu-id="6ea9e-205">Örneğin, **Sigorta** gider türü için belirtilen bir hesap, sigorta gideri için icra maliyeti planından bir fatura veya ödeme günlük giriş oluşturulduğunda borçlandırılır.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-205">For example, the account that is specified for the **Insurance** expense type is debited whenever an invoice or payment journal entry is created from the executory cost schedule for insurance expense.</span></span>

<span data-ttu-id="6ea9e-206">**Örnek günlük girişleri**: Sigorta ödemesi</span><span class="sxs-lookup"><span data-stu-id="6ea9e-206">**Example journal entries:** Insurance payment</span></span><br>
<span data-ttu-id="6ea9e-207">**Borç**: Sigorta gideri türü hesabı XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-207">**Debit:** Insurance expense type account XXX</span></span><br>
<span data-ttu-id="6ea9e-208">**Alacak**: Mahsup hesap XXX</span><span class="sxs-lookup"><span data-stu-id="6ea9e-208">**Credit:** Offset account XXX</span></span>

> [!NOTE]
> <span data-ttu-id="6ea9e-209">Mahsup hesap, icra maliyeti ödeme planı için satırlardaki kiralama düzeyinde seçilir.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-209">The offset account is selected at the lease level on the lines for the executory cost payment schedule.</span></span> <span data-ttu-id="6ea9e-210">Bu mahsup hesap, satıcıyla veya bir genel muhasebe hesabıyla ilişkilendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="6ea9e-210">This offset account can associated with the vendor, or with a ledger account.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]