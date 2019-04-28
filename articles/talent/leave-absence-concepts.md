---
title: İzin ve devamsızlık konseptleri
description: Bu konu, izin ve devamsızlık kavramlarını ve izin sürelerinin nasıl belirlediğini açıklar.
author: andreabichsel
manager: AnnBe
ms.date: 01/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application user
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: ''
ms.openlocfilehash: 96e3aa74e513a2421b04bac049400cf71042e2c8
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/19/2019
ms.locfileid: "857311"
---
# <a name="leave-and-absence-concepts"></a><span data-ttu-id="68657-103">İzin ve devamsızlık konseptleri</span><span class="sxs-lookup"><span data-stu-id="68657-103">Leave and absence concepts</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="68657-104">Bu konuda açıklanan kavramlar ve terimler, bir personele nasıl izin verileceğini ve personelin zaman bakiyelerinin nasıl hesapladığını belirlemenizde yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="68657-104">The concepts and terms that are described in this topic can help you determine how an employee is awarded time off, and how that employee's time balances are calculated.</span></span> <span data-ttu-id="68657-105">İzin ve devamsızlık yönetimi hakkında daha fazla bilgi için bkz. [İzin ve devamsızlık yönetimi](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).</span><span class="sxs-lookup"><span data-stu-id="68657-105">For more information about leave and absence management, see [Leave and absence management](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).</span></span>

## <a name="leave-plan-details"></a><span data-ttu-id="68657-106">İzin planı ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="68657-106">Leave plan details</span></span>

### <a name="start-date"></a><span data-ttu-id="68657-107">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-107">Start date</span></span>

<span data-ttu-id="68657-108">Başlangıç tarihi, tahakkuk işleme başladığındaki tarihtir.</span><span class="sxs-lookup"><span data-stu-id="68657-108">The start date is the date when accrual processing begins.</span></span> <span data-ttu-id="68657-109">Başlangıç tarihi ayrıca, ileriye taşıma tutarlarını hesaplamakta kullanılan yıl dönümü tarihidir.</span><span class="sxs-lookup"><span data-stu-id="68657-109">The start date also serves as the anniversary date that is used to calculate carry-forward amounts.</span></span>

## <a name="accruals"></a><span data-ttu-id="68657-110">Tahakkuklar</span><span class="sxs-lookup"><span data-stu-id="68657-110">Accruals</span></span>

<span data-ttu-id="68657-111">Tahakkuklar, bir personele ne zaman ve ne sıklıkta izin verileceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="68657-111">Accruals determine when and how often an employee is awarded time off.</span></span> <span data-ttu-id="68657-112">Tahakkukların ne zaman verileceğine dair ilkeler ve dağılım hakkındaki ilkeler **Tahakkuklar** bölümünde, izin ve devamsızlık planını ayarlarken tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="68657-112">Policies about when accruals should be awarded and policies about proration are defined in the **Accruals** section when setting up the leave and absence plan.</span></span>

### <a name="accrual-frequency"></a><span data-ttu-id="68657-113">Tahakkuk sıklığı</span><span class="sxs-lookup"><span data-stu-id="68657-113">Accrual frequency</span></span>

<span data-ttu-id="68657-114">Tahakkuk sıklığı, iznin ne sıklıkta tahakkuk edileceğini veya verileceğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="68657-114">The accrual frequency defines how often leave is accrued or awarded.</span></span> <span data-ttu-id="68657-115">Aşağıdaki seçenekler kullanılabilir durumdadır:</span><span class="sxs-lookup"><span data-stu-id="68657-115">The following options are available:</span></span>

- <span data-ttu-id="68657-116">Günlük</span><span class="sxs-lookup"><span data-stu-id="68657-116">Daily</span></span>
- <span data-ttu-id="68657-117">Haftalık</span><span class="sxs-lookup"><span data-stu-id="68657-117">Weekly</span></span>
- <span data-ttu-id="68657-118">İki haftalık</span><span class="sxs-lookup"><span data-stu-id="68657-118">Biweekly</span></span>
- <span data-ttu-id="68657-119">Yarım aylık</span><span class="sxs-lookup"><span data-stu-id="68657-119">Semimonthly</span></span>
- <span data-ttu-id="68657-120">Aylık</span><span class="sxs-lookup"><span data-stu-id="68657-120">Monthly</span></span>
- <span data-ttu-id="68657-121">Üç aylık</span><span class="sxs-lookup"><span data-stu-id="68657-121">Quarterly</span></span>
- <span data-ttu-id="68657-122">Yarı yıllık</span><span class="sxs-lookup"><span data-stu-id="68657-122">Semiannually</span></span>
- <span data-ttu-id="68657-123">Yıllık</span><span class="sxs-lookup"><span data-stu-id="68657-123">Annually</span></span>
- <span data-ttu-id="68657-124">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="68657-124">None</span></span>

### <a name="accrual-period-basis"></a><span data-ttu-id="68657-125">Tahakkuk dönemi esası</span><span class="sxs-lookup"><span data-stu-id="68657-125">Accrual period basis</span></span>

<span data-ttu-id="68657-126">Tahakkuk dönemi esası, tahakkuk dönemlerini hesaplamakta kullanılan tarihi belirler.</span><span class="sxs-lookup"><span data-stu-id="68657-126">The accrual period basis determines the date that is used to calculate accrual periods.</span></span> <span data-ttu-id="68657-127">Aşağıdaki seçenekler kullanılabilir durumdadır:</span><span class="sxs-lookup"><span data-stu-id="68657-127">The following options are available:</span></span>

- <span data-ttu-id="68657-128">**Plan başlangıç tarihi**</span><span class="sxs-lookup"><span data-stu-id="68657-128">**Plan start date**</span></span>
- <span data-ttu-id="68657-129">**Personel belirli tarihi** - Bu seçenek seçili olduğunda, değer, tahakkuk dönemlerini hesaplamakta kullanılan ilk tarih değerinin kaynağını belirler.</span><span class="sxs-lookup"><span data-stu-id="68657-129">**Employee specific date** – When this option is selected, the value determines the source of the initial date value that is used to calculate accrual periods.</span></span> <span data-ttu-id="68657-130">Aşağıdaki seçenekler kullanılabilir durumdadır:</span><span class="sxs-lookup"><span data-stu-id="68657-130">The following options are available:</span></span>

    - <span data-ttu-id="68657-131">Özel</span><span class="sxs-lookup"><span data-stu-id="68657-131">Custom</span></span>
    - <span data-ttu-id="68657-132">Yıldönümü tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-132">Anniversary date</span></span>
    - <span data-ttu-id="68657-133">Orijinal işe alma tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-133">Original hire date</span></span>
    - <span data-ttu-id="68657-134">Kıdem tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-134">Seniority date</span></span>
    - <span data-ttu-id="68657-135">Çalışanın ayarlanan başlama tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-135">Worker's adjusted start date</span></span>
    - <span data-ttu-id="68657-136">Çalışanın başlama tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-136">Worker's start date</span></span>

### <a name="accrual-award-date"></a><span data-ttu-id="68657-137">Fiili ikramiye tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-137">Accrual award date</span></span>

<span data-ttu-id="68657-138">Tahakkuk verme tarihi, bir personele izin verileceği tarihi belirler.</span><span class="sxs-lookup"><span data-stu-id="68657-138">The accrual award date determines when an employee is awarded time off.</span></span> <span data-ttu-id="68657-139">Aşağıdaki seçenekler kullanılabilir durumdadır:</span><span class="sxs-lookup"><span data-stu-id="68657-139">The following options are available:</span></span>

- <span data-ttu-id="68657-140">**Tahakkuk dönemi bitiş tarihi** - Personele, verilme döneminin son gününde izin verilecektir.</span><span class="sxs-lookup"><span data-stu-id="68657-140">**Accrual period end date** – The employee will be awarded time off on the last day of the award period.</span></span>

    <span data-ttu-id="68657-141">Doğru değeri tahakkuk etmek için tahakkuk işleminin dönemin tamamını içermesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="68657-141">To accrue the correct amount, the accrual process must include the whole period.</span></span> <span data-ttu-id="68657-142">Örneğin, tahakkuk dönemi 1 Ocak 2018 ile 31 Ocak 2018 arasındadır.</span><span class="sxs-lookup"><span data-stu-id="68657-142">For example, the accrual period is January 1, 2018, through January 31, 2018.</span></span> <span data-ttu-id="68657-143">Bu durumda, Ocak'ın dahil edilmesi için tahakkukun 1 Şubat 2018 için yürütülmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="68657-143">In this case, for January to be included, the accrual must be run for February 1, 2018.</span></span>

- <span data-ttu-id="68657-144">**Tahakkuk dönemi başlangıç tarihi** - Personele, verilme döneminin ilk gününde izin verilecektir.</span><span class="sxs-lookup"><span data-stu-id="68657-144">**Accrual period start date** – The employee will be awarded time off on the first day of the award period.</span></span>

### <a name="accrual-policy-on-enrollment"></a><span data-ttu-id="68657-145">Tahakkuk ilkesi kaydı</span><span class="sxs-lookup"><span data-stu-id="68657-145">Accrual policy on enrollment</span></span>

<span data-ttu-id="68657-146">Kayıttaki tahakkuk ilkesi, tahakkukun bir personel, tahakkuk döneminin ortasında kayıt yaptığında nasıl hesaplanacağını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="68657-146">The accrual policy on enrollment defines how accrual is calculated when an employee is enrolled in the middle of an accrual period.</span></span> <span data-ttu-id="68657-147">Aşağıdaki seçenekler kullanılabilir durumdadır:</span><span class="sxs-lookup"><span data-stu-id="68657-147">The following options are available:</span></span>

- <span data-ttu-id="68657-148">**Dağıtılmış** - Kayıt tarihi ve başlangıç tarihi arasındaki tarih aralığı, farkı gün olarak belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="68657-148">**Prorated** – The date range between the enrollment date and the start date is used to determine the difference in days.</span></span> <span data-ttu-id="68657-149">Fark, tahakkuklar işlendiğine uygulanır.</span><span class="sxs-lookup"><span data-stu-id="68657-149">That difference is applied when accruals are processed.</span></span>
- <span data-ttu-id="68657-150">**Tam tahakkuk** - Tam tahakkuk tutarı, katmana dayalı olarak ilk tahakkuk işlemesi sırasında verilir.</span><span class="sxs-lookup"><span data-stu-id="68657-150">**Full accrual** – The full accrual amount, based on the tier, is awarded during the first accrual processing.</span></span>
- <span data-ttu-id="68657-151">**Tahakkuk yok** - Bir sonraki tahakkuk dönemine kadar hiç tahakkuk verilmez.</span><span class="sxs-lookup"><span data-stu-id="68657-151">**No accrual** – No accrual is awarded until the next accrual period.</span></span>

### <a name="accrual-policy-on-unenrollment"></a><span data-ttu-id="68657-152">Tahakkuk ilkesi kayıt sildirme</span><span class="sxs-lookup"><span data-stu-id="68657-152">Accrual policy on unenrollment</span></span>

<span data-ttu-id="68657-153">Kayıt sildirmedeki tahakkuk ilkesi, tahakkukun bir personel, tahakkuk döneminin ortasında kayıt sildirme yaptığında nasıl hesaplanacağını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="68657-153">The accrual policy on unenrollment defines how accrual is calculated when an employee is unenrolled in the middle of an accrual period.</span></span> <span data-ttu-id="68657-154">Aşağıdaki seçenekler kullanılabilir durumdadır:</span><span class="sxs-lookup"><span data-stu-id="68657-154">The following options are available:</span></span>

- <span data-ttu-id="68657-155">**Dağıtılmış** - Kayıt tarihi ve başlangıç tarihi arasındaki tarih aralığı, farkı gün olarak belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="68657-155">**Prorated** – The date range between the enrollment date and the start date is used to determine the difference in days.</span></span> <span data-ttu-id="68657-156">Fark, tahakkuklar işlendiğine uygulanır.</span><span class="sxs-lookup"><span data-stu-id="68657-156">That difference is applied when accruals are processed.</span></span>
- <span data-ttu-id="68657-157">**Tam tahakkuk** - Tam tahakkuk tutarı, katmana dayalı olarak ilk tahakkuk işlemesi sırasında verilir.</span><span class="sxs-lookup"><span data-stu-id="68657-157">**Full accrual** – The full accrual amount, based on the tier, is awarded during the first accrual processing.</span></span>
- <span data-ttu-id="68657-158">**Tahakkuk yok** - Bir sonraki tahakkuk dönemine kadar hiç tahakkuk verilmez.</span><span class="sxs-lookup"><span data-stu-id="68657-158">**No accrual** – No accrual is awarded until the next accrual period.</span></span>

## <a name="accrual-schedule"></a><span data-ttu-id="68657-159">Tahakkuk planı</span><span class="sxs-lookup"><span data-stu-id="68657-159">Accrual schedule</span></span>

<span data-ttu-id="68657-160">Tahakkuk planı, bir personelin izin nasıl tahakkuk ettiğini belirler ve hangi tutarın personel tarafından tahakkuk edeceğini ve ileri taşınacağını belirler.</span><span class="sxs-lookup"><span data-stu-id="68657-160">The accrual schedule determines how an employee will accrue time off, and what amounts that employee will accrue and carry forward.</span></span> <span data-ttu-id="68657-161">Katmanlar, iznin farklı düzeylere dayanarak verilmesi için oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="68657-161">Tiers can be created so that time off is awarded based on different levels.</span></span>

### <a name="months-of-service"></a><span data-ttu-id="68657-162">Hizmetteki ay sayısı</span><span class="sxs-lookup"><span data-stu-id="68657-162">Months of service</span></span>

<span data-ttu-id="68657-163">**Hizmet ayı** değeri, personelin tahakkuk hakkı kazanabilmesi için çalışması gereken minimum ay sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="68657-163">The **Months of service** value defines the minimum number of months that employees must work to be entitled to accruals.</span></span> <span data-ttu-id="68657-164">Personel için minimum gerekli değilse, değeri **0** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="68657-164">If no minimum is required for employees, set the value to **0**.</span></span>

### <a name="hours-worked"></a><span data-ttu-id="68657-165">Çalışılan saatler</span><span class="sxs-lookup"><span data-stu-id="68657-165">Hours worked</span></span>

<span data-ttu-id="68657-166">**Çalışılan saatler** değeri, personelin tahakkuk hakkı kazanabilmesi için tahakkuk başına çalışması gereken minimum saat sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="68657-166">The **Hours worked** value defines the minimum number of hours that employees must work per accrual period to be entitled to accruals.</span></span> <span data-ttu-id="68657-167">Personel için minimum gerekli değilse, değeri **0** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="68657-167">If no minimum is required for employees, set the value to **0**.</span></span>

### <a name="accrual-amount"></a><span data-ttu-id="68657-168">Tahakkuk tutarı</span><span class="sxs-lookup"><span data-stu-id="68657-168">Accrual amount</span></span>

<span data-ttu-id="68657-169">Tahakkuk tutarı saat veya gün cinsinden çalışanların tahakkuk numarasıdır dönem başına düşen.</span><span class="sxs-lookup"><span data-stu-id="68657-169">The accrual amount is the number of hours or days that employees will accrue per period.</span></span> <span data-ttu-id="68657-170">Dönem, tahakkuk sıklığını temel alır.</span><span class="sxs-lookup"><span data-stu-id="68657-170">The period is based on the accrual frequency.</span></span>

### <a name="minimum-balance"></a><span data-ttu-id="68657-171">Minimum bakiye</span><span class="sxs-lookup"><span data-stu-id="68657-171">Minimum balance</span></span>

<span data-ttu-id="68657-172">Bir negatif değer, minimum bakiye için kullanılabilir, eğer personel kullanılabilir sahip olduğundan daha fazla izin talep ederse.</span><span class="sxs-lookup"><span data-stu-id="68657-172">A negative value can be used for the minimum balance if employees can request more leave than they have available.</span></span>

### <a name="maximum-carry-forward"></a><span data-ttu-id="68657-173">Maksimum ileriye taşıma</span><span class="sxs-lookup"><span data-stu-id="68657-173">Maximum carry-forward</span></span>

<span data-ttu-id="68657-174">Tahakkuk işlemi, başlangıç tarihinin yıl dönümündeki maksimum ileri taşıma bakiyesini aşan izin bakiyelerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="68657-174">The accrual process will adjust leave balances that exceed the maximum carry-forward balance on the anniversary of the start date.</span></span>

### <a name="grant-amount"></a><span data-ttu-id="68657-175">Tutar ver</span><span class="sxs-lookup"><span data-stu-id="68657-175">Grant amount</span></span>

<span data-ttu-id="68657-176">Tutar ver, izin planına ilk kaydolduklarında personele verilen saat veya günün ilk sayısıdır.</span><span class="sxs-lookup"><span data-stu-id="68657-176">The grant amount is the initial number of hours or days that employees are granted when they first enroll in the leave plan.</span></span> <span data-ttu-id="68657-177">Tutar, her bir tahakkuk dönemi için tahakkuk edilmez.</span><span class="sxs-lookup"><span data-stu-id="68657-177">The amount doesn't accrue for each accrual period.</span></span>

## <a name="enrollments-and-balances"></a><span data-ttu-id="68657-178">Kayıtlar ve bakiyeler</span><span class="sxs-lookup"><span data-stu-id="68657-178">Enrollments and balances</span></span>

### <a name="enrollment-date"></a><span data-ttu-id="68657-179">Kayıt tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-179">Enrollment date</span></span>

<span data-ttu-id="68657-180">Kayıt tarihi, bir personelin izin tahakkuk etmeye başlayabileceği tarihi belirtir.</span><span class="sxs-lookup"><span data-stu-id="68657-180">The enrollment date determines when an employee can start to accrue time off.</span></span> <span data-ttu-id="68657-181">Örneğin, bir personel bir tatil planına 15 Haziran 2018 tarihinde kaydolduysa, 15 Haziran 2018 tarhinden önce herhangi bir süre tahakkuk edemez.</span><span class="sxs-lookup"><span data-stu-id="68657-181">For example, if an employee is enrolled in a vacation plan on June 15, 2018, she can't accrue any time off before June 15, 2018.</span></span>

### <a name="current-balance"></a><span data-ttu-id="68657-182">Mevcut bakiye</span><span class="sxs-lookup"><span data-stu-id="68657-182">Current balance</span></span>

<span data-ttu-id="68657-183">Tahakkuk bakiyesi, izin talepleri için kullanılabilir izin tutarıdır.</span><span class="sxs-lookup"><span data-stu-id="68657-183">The current balance is the amount of leave that is available for time off requests.</span></span> <span data-ttu-id="68657-184">Bu tutar tahakkukları, onaylanmış talepleri ve geçerli tarih üzerinden ayarlamaları içerir.</span><span class="sxs-lookup"><span data-stu-id="68657-184">This amount includes accruals, approved requests, and adjustments through the current date.</span></span>

### <a name="current-balance-examples"></a><span data-ttu-id="68657-185">Geçerli bakiye örnekleri</span><span class="sxs-lookup"><span data-stu-id="68657-185">Current balance examples</span></span>

#### <a name="annual-plan"></a><span data-ttu-id="68657-186">Yıllık plan</span><span class="sxs-lookup"><span data-stu-id="68657-186">Annual plan</span></span>

<span data-ttu-id="68657-187">**Plan kurulumu**</span><span class="sxs-lookup"><span data-stu-id="68657-187">**Plan setup**</span></span>

| <span data-ttu-id="68657-188">Plan başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-188">Plan start date</span></span> | <span data-ttu-id="68657-189">Kayıt tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-189">Enrollment date</span></span> | <span data-ttu-id="68657-190">Tahakkuk sıklığı</span><span class="sxs-lookup"><span data-stu-id="68657-190">Accrual frequency</span></span> | <span data-ttu-id="68657-191">Tahakkuk dönemi esası</span><span class="sxs-lookup"><span data-stu-id="68657-191">Accrual period basis</span></span> | <span data-ttu-id="68657-192">Fiili ikramiye tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-192">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="68657-193">01/01/2018</span><span class="sxs-lookup"><span data-stu-id="68657-193">1/1/2018</span></span>        | <span data-ttu-id="68657-194">01/01/2018</span><span class="sxs-lookup"><span data-stu-id="68657-194">1/1/2018</span></span>        | <span data-ttu-id="68657-195">Yıllık</span><span class="sxs-lookup"><span data-stu-id="68657-195">Annual</span></span>            | <span data-ttu-id="68657-196">Plan başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-196">Plan start date</span></span>      | <span data-ttu-id="68657-197">Tahakkuk döneminin sonu</span><span class="sxs-lookup"><span data-stu-id="68657-197">End of accrual period</span></span> |

<span data-ttu-id="68657-198">Tahakkuklar 1 Ocak 2019 (01/01/2019) tarihinde işlenir, böylece dönemin tamamı dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="68657-198">Accruals are processed on January 1, 2019 (1/1/2019), so that that whole period is included.</span></span>

<span data-ttu-id="68657-199">**Sonuçlar**</span><span class="sxs-lookup"><span data-stu-id="68657-199">**Results**</span></span>

| <span data-ttu-id="68657-200">Tahakkuk tutarı</span><span class="sxs-lookup"><span data-stu-id="68657-200">Accrual amount</span></span> | <span data-ttu-id="68657-201">Minimum bakiye</span><span class="sxs-lookup"><span data-stu-id="68657-201">Minimum balance</span></span> | <span data-ttu-id="68657-202">Maksimum ileriye taşıma</span><span class="sxs-lookup"><span data-stu-id="68657-202">Maximum carry-forward</span></span> | <span data-ttu-id="68657-203">Talep tutarı</span><span class="sxs-lookup"><span data-stu-id="68657-203">Request amount</span></span> | <span data-ttu-id="68657-204">Geçerli bakiye (01/01/2019 itibariyle)</span><span class="sxs-lookup"><span data-stu-id="68657-204">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="68657-205">200</span><span class="sxs-lookup"><span data-stu-id="68657-205">200</span></span>            | <span data-ttu-id="68657-206">0</span><span class="sxs-lookup"><span data-stu-id="68657-206">0</span></span>               | <span data-ttu-id="68657-207">120</span><span class="sxs-lookup"><span data-stu-id="68657-207">120</span></span>                   | <span data-ttu-id="68657-208">40</span><span class="sxs-lookup"><span data-stu-id="68657-208">40</span></span>             | <span data-ttu-id="68657-209">160</span><span class="sxs-lookup"><span data-stu-id="68657-209">160</span></span>                              |

<span data-ttu-id="68657-210">Geçerli bakiye (160) = Tahakkuk tutarı (200) - Talep tutarı (40)</span><span class="sxs-lookup"><span data-stu-id="68657-210">Current balance (160) = Accrual amount (200) – Request amount (40)</span></span>

#### <a name="semimonthly-plan"></a><span data-ttu-id="68657-211">Yarım aylık plan</span><span class="sxs-lookup"><span data-stu-id="68657-211">Semimonthly plan</span></span>

<span data-ttu-id="68657-212">**Plan kurulumu**</span><span class="sxs-lookup"><span data-stu-id="68657-212">**Plan setup**</span></span>

| <span data-ttu-id="68657-213">Plan başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-213">Plan start date</span></span> | <span data-ttu-id="68657-214">Kayıt tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-214">Enrollment date</span></span> | <span data-ttu-id="68657-215">Tahakkuk sıklığı</span><span class="sxs-lookup"><span data-stu-id="68657-215">Accrual frequency</span></span> | <span data-ttu-id="68657-216">Tahakkuk dönemi esası</span><span class="sxs-lookup"><span data-stu-id="68657-216">Accrual period basis</span></span> | <span data-ttu-id="68657-217">Fiili ikramiye tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-217">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="68657-218">01/01/2018</span><span class="sxs-lookup"><span data-stu-id="68657-218">1/1/2018</span></span>        | <span data-ttu-id="68657-219">01/02/2018</span><span class="sxs-lookup"><span data-stu-id="68657-219">2/1/2018</span></span>        | <span data-ttu-id="68657-220">Yarım aylık</span><span class="sxs-lookup"><span data-stu-id="68657-220">Semimonthly</span></span>       | <span data-ttu-id="68657-221">Plan başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-221">Plan start date</span></span>      | <span data-ttu-id="68657-222">Tahakkuk döneminin sonu</span><span class="sxs-lookup"><span data-stu-id="68657-222">End of accrual period</span></span> |

<span data-ttu-id="68657-223">Tahakkuklar 1 Mayıs 2018 (01/05/2018) tarihinde işlenir, böylece dönemin tamamı dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="68657-223">Accruals are processed on May 1, 2018 (5/1/2018), so that that whole period is included.</span></span>

<span data-ttu-id="68657-224">**Sonuçlar**</span><span class="sxs-lookup"><span data-stu-id="68657-224">**Results**</span></span>

| <span data-ttu-id="68657-225">Tahakkuk tutarı</span><span class="sxs-lookup"><span data-stu-id="68657-225">Accrual amount</span></span> | <span data-ttu-id="68657-226">Minimum bakiye</span><span class="sxs-lookup"><span data-stu-id="68657-226">Minimum balance</span></span> | <span data-ttu-id="68657-227">Maksimum ileriye taşıma</span><span class="sxs-lookup"><span data-stu-id="68657-227">Maximum carry-forward</span></span> | <span data-ttu-id="68657-228">Talep tutarı</span><span class="sxs-lookup"><span data-stu-id="68657-228">Request amount</span></span> | <span data-ttu-id="68657-229">Geçerli bakiye (01/01/2019 itibariyle)</span><span class="sxs-lookup"><span data-stu-id="68657-229">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="68657-230">5</span><span class="sxs-lookup"><span data-stu-id="68657-230">5</span></span>              | <span data-ttu-id="68657-231">0</span><span class="sxs-lookup"><span data-stu-id="68657-231">0</span></span>               | <span data-ttu-id="68657-232">120</span><span class="sxs-lookup"><span data-stu-id="68657-232">120</span></span>                   | <span data-ttu-id="68657-233">8</span><span class="sxs-lookup"><span data-stu-id="68657-233">8</span></span>              | <span data-ttu-id="68657-234">22</span><span class="sxs-lookup"><span data-stu-id="68657-234">22</span></span>                               |

<span data-ttu-id="68657-235">Geçerli bakiye (22) = Tahakkuk tutarı (5 × 6) - Talep tutarı (8)</span><span class="sxs-lookup"><span data-stu-id="68657-235">Current balance (22) = Accrual amount (5 × 6) – Request amount (8)</span></span>

#### <a name="monthly-plan"></a><span data-ttu-id="68657-236">Aylık plan</span><span class="sxs-lookup"><span data-stu-id="68657-236">Monthly plan</span></span>

<span data-ttu-id="68657-237">**Plan kurulumu**</span><span class="sxs-lookup"><span data-stu-id="68657-237">**Plan setup**</span></span>

| <span data-ttu-id="68657-238">Plan başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-238">Plan start date</span></span> | <span data-ttu-id="68657-239">Kayıt tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-239">Enrollment date</span></span> | <span data-ttu-id="68657-240">Tahakkuk sıklığı</span><span class="sxs-lookup"><span data-stu-id="68657-240">Accrual frequency</span></span> | <span data-ttu-id="68657-241">Tahakkuk dönemi esası</span><span class="sxs-lookup"><span data-stu-id="68657-241">Accrual period basis</span></span> | <span data-ttu-id="68657-242">Fiili ikramiye tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-242">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="68657-243">01/01/2018</span><span class="sxs-lookup"><span data-stu-id="68657-243">1/1/2018</span></span>        | <span data-ttu-id="68657-244">01/02/2018</span><span class="sxs-lookup"><span data-stu-id="68657-244">2/1/2018</span></span>        | <span data-ttu-id="68657-245">Yarım aylık</span><span class="sxs-lookup"><span data-stu-id="68657-245">Semimonthly</span></span>       | <span data-ttu-id="68657-246">Plan başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-246">Plan start date</span></span>      | <span data-ttu-id="68657-247">Tahakkuk döneminin sonu</span><span class="sxs-lookup"><span data-stu-id="68657-247">End of accrual period</span></span> |

<span data-ttu-id="68657-248">Tahakkuklar 1 Mayıs 2018 (01/05/2018) tarihinde işlenir, böylece dönemin tamamı dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="68657-248">Accruals are processed on May 1, 2018 (5/1/2018), so that that whole period is included.</span></span>

<span data-ttu-id="68657-249">**Sonuçlar**</span><span class="sxs-lookup"><span data-stu-id="68657-249">**Results**</span></span>

| <span data-ttu-id="68657-250">Tahakkuk tutarı</span><span class="sxs-lookup"><span data-stu-id="68657-250">Accrual amount</span></span> | <span data-ttu-id="68657-251">Minimum bakiye</span><span class="sxs-lookup"><span data-stu-id="68657-251">Minimum balance</span></span> | <span data-ttu-id="68657-252">Maksimum ileriye taşıma</span><span class="sxs-lookup"><span data-stu-id="68657-252">Maximum carry-forward</span></span> | <span data-ttu-id="68657-253">Talep tutarı</span><span class="sxs-lookup"><span data-stu-id="68657-253">Request amount</span></span> | <span data-ttu-id="68657-254">Geçerli bakiye (01/01/2019 itibariyle)</span><span class="sxs-lookup"><span data-stu-id="68657-254">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="68657-255">5</span><span class="sxs-lookup"><span data-stu-id="68657-255">5</span></span>              | <span data-ttu-id="68657-256">0</span><span class="sxs-lookup"><span data-stu-id="68657-256">0</span></span>               | <span data-ttu-id="68657-257">120</span><span class="sxs-lookup"><span data-stu-id="68657-257">120</span></span>                   | <span data-ttu-id="68657-258">8</span><span class="sxs-lookup"><span data-stu-id="68657-258">8</span></span>              | <span data-ttu-id="68657-259">7</span><span class="sxs-lookup"><span data-stu-id="68657-259">7</span></span>                                |

<span data-ttu-id="68657-260">Geçerli bakiye (7) = Tahakkuk tutarı (5 × 3) - Talep tutarı (8)</span><span class="sxs-lookup"><span data-stu-id="68657-260">Current balance (7) = Accrual amount (5 × 3) – Request amount (8)</span></span>

### <a name="forecasted-balance"></a><span data-ttu-id="68657-261">Tahmin edilen bakiye</span><span class="sxs-lookup"><span data-stu-id="68657-261">Forecasted balance</span></span>

<span data-ttu-id="68657-262">*Tahmin edilen bakiye*, gelecekteki bir tarihte kullanılabilir olan iznin tutarıdır.</span><span class="sxs-lookup"><span data-stu-id="68657-262">The *forecasted balance* is the amount of leave that is available on a future date.</span></span> <span data-ttu-id="68657-263">Tahakkuk ve ileriye taşıma ayarlamaları, bu tarihe kadar tahmin edilir.</span><span class="sxs-lookup"><span data-stu-id="68657-263">Accruals and carry-forward adjustments are forecasted up to that date.</span></span>

<span data-ttu-id="68657-264">Aşağıdaki formül kullanılır:</span><span class="sxs-lookup"><span data-stu-id="68657-264">The following formula is used:</span></span>

<span data-ttu-id="68657-265">Pazartesi tahmin edilen bakiye = Geçerli bakiye – Talepler + Tahakkuklar – İleriye taşıma ayarlaması</span><span class="sxs-lookup"><span data-stu-id="68657-265">Monday forecasted balance = Current balance – Requests + Accruals – Carry-forward adjustment</span></span>

### <a name="forecasted-balance-examples"></a><span data-ttu-id="68657-266">Tahmin edilen bakiye örnekleri</span><span class="sxs-lookup"><span data-stu-id="68657-266">Forecasted balance examples</span></span>

#### <a name="annual-plan"></a><span data-ttu-id="68657-267">Yıllık plan</span><span class="sxs-lookup"><span data-stu-id="68657-267">Annual plan</span></span>

<span data-ttu-id="68657-268">**Plan kurulumu**</span><span class="sxs-lookup"><span data-stu-id="68657-268">**Plan setup**</span></span>

| <span data-ttu-id="68657-269">Plan başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-269">Plan start date</span></span> | <span data-ttu-id="68657-270">Kayıt tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-270">Enrollment date</span></span> | <span data-ttu-id="68657-271">Tahakkuk sıklığı</span><span class="sxs-lookup"><span data-stu-id="68657-271">Accrual frequency</span></span> | <span data-ttu-id="68657-272">Tahakkuk dönemi esası</span><span class="sxs-lookup"><span data-stu-id="68657-272">Accrual period basis</span></span> | <span data-ttu-id="68657-273">Fiili ikramiye tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-273">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="68657-274">01/01/2018</span><span class="sxs-lookup"><span data-stu-id="68657-274">1/1/2018</span></span>        | <span data-ttu-id="68657-275">01/01/2018</span><span class="sxs-lookup"><span data-stu-id="68657-275">1/1/2018</span></span>        | <span data-ttu-id="68657-276">Yıllık</span><span class="sxs-lookup"><span data-stu-id="68657-276">Annual</span></span>            | <span data-ttu-id="68657-277">Plan başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-277">Plan start date</span></span>      | <span data-ttu-id="68657-278">Tahakkuk döneminin sonu</span><span class="sxs-lookup"><span data-stu-id="68657-278">End of accrual period</span></span> |

<span data-ttu-id="68657-279">Tahakkuklar 15 Şubat 2019 (15/02/2019) tarihinde işlenir, böylece dönemin tamamı dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="68657-279">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="68657-280">**Sonuçlar**</span><span class="sxs-lookup"><span data-stu-id="68657-280">**Results**</span></span>

| <span data-ttu-id="68657-281">Tahakkuk tutarı</span><span class="sxs-lookup"><span data-stu-id="68657-281">Accrual amount</span></span> | <span data-ttu-id="68657-282">Minimum bakiye</span><span class="sxs-lookup"><span data-stu-id="68657-282">Minimum balance</span></span> | <span data-ttu-id="68657-283">Maksimum ileriye taşıma</span><span class="sxs-lookup"><span data-stu-id="68657-283">Maximum carry-forward</span></span> | <span data-ttu-id="68657-284">Mevcut bakiye</span><span class="sxs-lookup"><span data-stu-id="68657-284">Current balance</span></span> | <span data-ttu-id="68657-285">Tahmin edilen bakiye (15/02/2019 itibariyle)</span><span class="sxs-lookup"><span data-stu-id="68657-285">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="68657-286">20</span><span class="sxs-lookup"><span data-stu-id="68657-286">20</span></span>             | <span data-ttu-id="68657-287">0</span><span class="sxs-lookup"><span data-stu-id="68657-287">0</span></span>               | <span data-ttu-id="68657-288">20</span><span class="sxs-lookup"><span data-stu-id="68657-288">20</span></span>                    | <span data-ttu-id="68657-289">40</span><span class="sxs-lookup"><span data-stu-id="68657-289">40</span></span>              | <span data-ttu-id="68657-290">40</span><span class="sxs-lookup"><span data-stu-id="68657-290">40</span></span>                                   |

<span data-ttu-id="68657-291">Tahmin edilen bakiye (40) = Tahakkuk tutarı (20) + Geçerli bakiye (40) – İleriye taşıma ayarlaması (20)</span><span class="sxs-lookup"><span data-stu-id="68657-291">Forecasted balance (40) = Accrual amount (20) + Current balance (40) – Carry-forward adjustment (20)</span></span>

#### <a name="semimonthly-plan"></a><span data-ttu-id="68657-292">Yarım aylık plan</span><span class="sxs-lookup"><span data-stu-id="68657-292">Semimonthly plan</span></span>

<span data-ttu-id="68657-293">**Plan kurulumu**</span><span class="sxs-lookup"><span data-stu-id="68657-293">**Plan setup**</span></span>

| <span data-ttu-id="68657-294">Plan başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-294">Plan start date</span></span> | <span data-ttu-id="68657-295">Kayıt tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-295">Enrollment date</span></span> | <span data-ttu-id="68657-296">Tahakkuk sıklığı</span><span class="sxs-lookup"><span data-stu-id="68657-296">Accrual frequency</span></span> | <span data-ttu-id="68657-297">Tahakkuk dönemi esası</span><span class="sxs-lookup"><span data-stu-id="68657-297">Accrual period basis</span></span> | <span data-ttu-id="68657-298">Fiili ikramiye tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-298">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="68657-299">01/01/2018</span><span class="sxs-lookup"><span data-stu-id="68657-299">1/1/2018</span></span>        | <span data-ttu-id="68657-300">01/02/2018</span><span class="sxs-lookup"><span data-stu-id="68657-300">2/1/2018</span></span>        | <span data-ttu-id="68657-301">Yarım aylık</span><span class="sxs-lookup"><span data-stu-id="68657-301">Semimonthly</span></span>       | <span data-ttu-id="68657-302">Plan başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-302">Plan start date</span></span>      | <span data-ttu-id="68657-303">Tahakkuk döneminin sonu</span><span class="sxs-lookup"><span data-stu-id="68657-303">End of accrual period</span></span> |

<span data-ttu-id="68657-304">Tahakkuklar 15 Şubat 2019 (15/02/2019) tarihinde işlenir, böylece dönemin tamamı dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="68657-304">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="68657-305">**Sonuçlar**</span><span class="sxs-lookup"><span data-stu-id="68657-305">**Results**</span></span>

| <span data-ttu-id="68657-306">Tahakkuk tutarı</span><span class="sxs-lookup"><span data-stu-id="68657-306">Accrual amount</span></span> | <span data-ttu-id="68657-307">Minimum bakiye</span><span class="sxs-lookup"><span data-stu-id="68657-307">Minimum balance</span></span> | <span data-ttu-id="68657-308">Maksimum ileriye taşıma</span><span class="sxs-lookup"><span data-stu-id="68657-308">Maximum carry-forward</span></span> | <span data-ttu-id="68657-309">Mevcut bakiye</span><span class="sxs-lookup"><span data-stu-id="68657-309">Current balance</span></span> | <span data-ttu-id="68657-310">Tahmin edilen bakiye (15/02/2019 itibariyle)</span><span class="sxs-lookup"><span data-stu-id="68657-310">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="68657-311">5</span><span class="sxs-lookup"><span data-stu-id="68657-311">5</span></span>              | <span data-ttu-id="68657-312">0</span><span class="sxs-lookup"><span data-stu-id="68657-312">0</span></span>               | <span data-ttu-id="68657-313">20</span><span class="sxs-lookup"><span data-stu-id="68657-313">20</span></span>                    | <span data-ttu-id="68657-314">40</span><span class="sxs-lookup"><span data-stu-id="68657-314">40</span></span>              | <span data-ttu-id="68657-315">35</span><span class="sxs-lookup"><span data-stu-id="68657-315">35</span></span>                                   |

<span data-ttu-id="68657-316">Tahmin edilen bakiye (35) = Tahakkuk tutarı (5 × 3) + Geçerli bakiye (40) – İleriye taşıma ayarlaması (20)</span><span class="sxs-lookup"><span data-stu-id="68657-316">Forecasted balance (35) = Accrual amount (5 × 3) + Current balance (40) – Carry-forward adjustment (20)</span></span>

#### <a name="monthly-plan"></a><span data-ttu-id="68657-317">Aylık plan</span><span class="sxs-lookup"><span data-stu-id="68657-317">Monthly plan</span></span>

<span data-ttu-id="68657-318">**Plan kurulumu**</span><span class="sxs-lookup"><span data-stu-id="68657-318">**Plan setup**</span></span>

| <span data-ttu-id="68657-319">Plan başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-319">Plan start date</span></span> | <span data-ttu-id="68657-320">Kayıt tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-320">Enrollment date</span></span> | <span data-ttu-id="68657-321">Tahakkuk sıklığı</span><span class="sxs-lookup"><span data-stu-id="68657-321">Accrual frequency</span></span> | <span data-ttu-id="68657-322">Tahakkuk dönemi esası</span><span class="sxs-lookup"><span data-stu-id="68657-322">Accrual period basis</span></span> | <span data-ttu-id="68657-323">Fiili ikramiye tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-323">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="68657-324">01/01/2018</span><span class="sxs-lookup"><span data-stu-id="68657-324">1/1/2018</span></span>        | <span data-ttu-id="68657-325">01/02/2018</span><span class="sxs-lookup"><span data-stu-id="68657-325">2/1/2018</span></span>        | <span data-ttu-id="68657-326">Yarım aylık</span><span class="sxs-lookup"><span data-stu-id="68657-326">Semimonthly</span></span>       | <span data-ttu-id="68657-327">Plan başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-327">Plan start date</span></span>      | <span data-ttu-id="68657-328">Tahakkuk döneminin sonu</span><span class="sxs-lookup"><span data-stu-id="68657-328">End of accrual period</span></span> |

<span data-ttu-id="68657-329">Tahakkuklar 15 Şubat 2019 (15/02/2019) tarihinde işlenir, böylece dönemin tamamı dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="68657-329">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="68657-330">**Sonuçlar**</span><span class="sxs-lookup"><span data-stu-id="68657-330">**Results**</span></span>

| <span data-ttu-id="68657-331">Tahakkuk tutarı</span><span class="sxs-lookup"><span data-stu-id="68657-331">Accrual amount</span></span> | <span data-ttu-id="68657-332">Minimum bakiye</span><span class="sxs-lookup"><span data-stu-id="68657-332">Minimum balance</span></span> | <span data-ttu-id="68657-333">Maksimum ileriye taşıma</span><span class="sxs-lookup"><span data-stu-id="68657-333">Maximum carry-forward</span></span> | <span data-ttu-id="68657-334">Mevcut bakiye</span><span class="sxs-lookup"><span data-stu-id="68657-334">Current balance</span></span> | <span data-ttu-id="68657-335">Tahmin edilen bakiye (15/02/2019 itibariyle)</span><span class="sxs-lookup"><span data-stu-id="68657-335">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="68657-336">10</span><span class="sxs-lookup"><span data-stu-id="68657-336">10</span></span>             | <span data-ttu-id="68657-337">0</span><span class="sxs-lookup"><span data-stu-id="68657-337">0</span></span>               | <span data-ttu-id="68657-338">20</span><span class="sxs-lookup"><span data-stu-id="68657-338">20</span></span>                    | <span data-ttu-id="68657-339">40</span><span class="sxs-lookup"><span data-stu-id="68657-339">40</span></span>              | <span data-ttu-id="68657-340">30</span><span class="sxs-lookup"><span data-stu-id="68657-340">30</span></span>                                   |

<span data-ttu-id="68657-341">Tahmin edilen bakiye (30) = Tahakkuk tutarı (10 × 1) + Geçerli bakiye (40) – İleriye taşıma ayarlaması (20)</span><span class="sxs-lookup"><span data-stu-id="68657-341">Forecasted balance (30) = Accrual amount (10 × 1) + Current balance (40) – Carry-forward adjustment (20)</span></span>

### <a name="proration-balance-examples"></a><span data-ttu-id="68657-342">Dağılım bakiye örnekleri</span><span class="sxs-lookup"><span data-stu-id="68657-342">Proration balance examples</span></span>

#### <a name="prorated-monthly-plan"></a><span data-ttu-id="68657-343">Dağıtılan aylık plan</span><span class="sxs-lookup"><span data-stu-id="68657-343">Prorated monthly plan</span></span>

<span data-ttu-id="68657-344">**Plan kurulumu**</span><span class="sxs-lookup"><span data-stu-id="68657-344">**Plan setup**</span></span>

| <span data-ttu-id="68657-345">Plan başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-345">Plan start date</span></span> | <span data-ttu-id="68657-346">Tahakkuk sıklığı</span><span class="sxs-lookup"><span data-stu-id="68657-346">Accrual frequency</span></span> | <span data-ttu-id="68657-347">Tahakkuk dönemi esası</span><span class="sxs-lookup"><span data-stu-id="68657-347">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="68657-348">01/01/2018</span><span class="sxs-lookup"><span data-stu-id="68657-348">1/1/2018</span></span>        | <span data-ttu-id="68657-349">Aylık</span><span class="sxs-lookup"><span data-stu-id="68657-349">Monthly</span></span>           | <span data-ttu-id="68657-350">Plan başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-350">Plan start date</span></span>      |

<span data-ttu-id="68657-351">**Sonuçlar**</span><span class="sxs-lookup"><span data-stu-id="68657-351">**Results**</span></span>

| <span data-ttu-id="68657-352">Personel</span><span class="sxs-lookup"><span data-stu-id="68657-352">Employee</span></span>            | <span data-ttu-id="68657-353">Hizmetteki ay sayısı</span><span class="sxs-lookup"><span data-stu-id="68657-353">Months of service</span></span> | <span data-ttu-id="68657-354">Kayıt tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-354">Enrollment date</span></span> | <span data-ttu-id="68657-355">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-355">Start date</span></span> | <span data-ttu-id="68657-356">Tahakkuk tutarı</span><span class="sxs-lookup"><span data-stu-id="68657-356">Accrual amount</span></span> | <span data-ttu-id="68657-357">İşlem tahakkuku</span><span class="sxs-lookup"><span data-stu-id="68657-357">Process accrual</span></span> | <span data-ttu-id="68657-358">Bilanço</span><span class="sxs-lookup"><span data-stu-id="68657-358">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="68657-359">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="68657-359">Jeannette Nicholson</span></span> | <span data-ttu-id="68657-360">0,00</span><span class="sxs-lookup"><span data-stu-id="68657-360">0.00</span></span>              | <span data-ttu-id="68657-361">01/06/2018</span><span class="sxs-lookup"><span data-stu-id="68657-361">6/1/2018</span></span>        | <span data-ttu-id="68657-362">01/06/2018</span><span class="sxs-lookup"><span data-stu-id="68657-362">6/1/2018</span></span>   | <span data-ttu-id="68657-363">1.00</span><span class="sxs-lookup"><span data-stu-id="68657-363">1.00</span></span>           | <span data-ttu-id="68657-364">01/09/2018</span><span class="sxs-lookup"><span data-stu-id="68657-364">9/1/2018</span></span>        | <span data-ttu-id="68657-365">3,00</span><span class="sxs-lookup"><span data-stu-id="68657-365">3.00</span></span>    |
| <span data-ttu-id="68657-366">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="68657-366">Jay Norman</span></span>          | <span data-ttu-id="68657-367">0,00</span><span class="sxs-lookup"><span data-stu-id="68657-367">0.00</span></span>              | <span data-ttu-id="68657-368">15/06/2018</span><span class="sxs-lookup"><span data-stu-id="68657-368">6/15/2018</span></span>       | <span data-ttu-id="68657-369">15/06/2018</span><span class="sxs-lookup"><span data-stu-id="68657-369">6/15/2018</span></span>  | <span data-ttu-id="68657-370">1.00</span><span class="sxs-lookup"><span data-stu-id="68657-370">1.00</span></span>           | <span data-ttu-id="68657-371">01/09/2018</span><span class="sxs-lookup"><span data-stu-id="68657-371">9/1/2018</span></span>        | <span data-ttu-id="68657-372">2,53</span><span class="sxs-lookup"><span data-stu-id="68657-372">2.53</span></span>    |

#### <a name="full-accrual-monthly-plan"></a><span data-ttu-id="68657-373">Aylık tam tahakkuk planı</span><span class="sxs-lookup"><span data-stu-id="68657-373">Full accrual monthly plan</span></span>

<span data-ttu-id="68657-374">**Plan kurulumu**</span><span class="sxs-lookup"><span data-stu-id="68657-374">**Plan setup**</span></span>

| <span data-ttu-id="68657-375">Plan başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-375">Plan start date</span></span> | <span data-ttu-id="68657-376">Tahakkuk sıklığı</span><span class="sxs-lookup"><span data-stu-id="68657-376">Accrual frequency</span></span> | <span data-ttu-id="68657-377">Tahakkuk dönemi esası</span><span class="sxs-lookup"><span data-stu-id="68657-377">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="68657-378">01/01/2018</span><span class="sxs-lookup"><span data-stu-id="68657-378">1/1/2018</span></span>        | <span data-ttu-id="68657-379">Aylık</span><span class="sxs-lookup"><span data-stu-id="68657-379">Monthly</span></span>           | <span data-ttu-id="68657-380">Plan başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-380">Plan start date</span></span>      |

<span data-ttu-id="68657-381">**Sonuçlar**</span><span class="sxs-lookup"><span data-stu-id="68657-381">**Results**</span></span>

| <span data-ttu-id="68657-382">Personel</span><span class="sxs-lookup"><span data-stu-id="68657-382">Employee</span></span>            | <span data-ttu-id="68657-383">Hizmetteki ay sayısı</span><span class="sxs-lookup"><span data-stu-id="68657-383">Months of service</span></span> | <span data-ttu-id="68657-384">Kayıt tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-384">Enrollment date</span></span> | <span data-ttu-id="68657-385">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-385">Start date</span></span> | <span data-ttu-id="68657-386">Tahakkuk tutarı</span><span class="sxs-lookup"><span data-stu-id="68657-386">Accrual amount</span></span> | <span data-ttu-id="68657-387">İşlem tahakkuku</span><span class="sxs-lookup"><span data-stu-id="68657-387">Process accrual</span></span> | <span data-ttu-id="68657-388">Bilanço</span><span class="sxs-lookup"><span data-stu-id="68657-388">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="68657-389">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="68657-389">Jeannette Nicholson</span></span> | <span data-ttu-id="68657-390">0,00</span><span class="sxs-lookup"><span data-stu-id="68657-390">0.00</span></span>              | <span data-ttu-id="68657-391">01/06/2018</span><span class="sxs-lookup"><span data-stu-id="68657-391">6/1/2018</span></span>        | <span data-ttu-id="68657-392">01/06/2018</span><span class="sxs-lookup"><span data-stu-id="68657-392">6/1/2018</span></span>   | <span data-ttu-id="68657-393">1.00</span><span class="sxs-lookup"><span data-stu-id="68657-393">1.00</span></span>           | <span data-ttu-id="68657-394">01/09/2018</span><span class="sxs-lookup"><span data-stu-id="68657-394">9/1/2018</span></span>        | <span data-ttu-id="68657-395">3,00</span><span class="sxs-lookup"><span data-stu-id="68657-395">3.00</span></span>    |
| <span data-ttu-id="68657-396">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="68657-396">Jay Norman</span></span>          | <span data-ttu-id="68657-397">0,00</span><span class="sxs-lookup"><span data-stu-id="68657-397">0.00</span></span>              | <span data-ttu-id="68657-398">15/06/2018</span><span class="sxs-lookup"><span data-stu-id="68657-398">6/15/2018</span></span>       | <span data-ttu-id="68657-399">15/06/2018</span><span class="sxs-lookup"><span data-stu-id="68657-399">6/15/2018</span></span>  | <span data-ttu-id="68657-400">1.00</span><span class="sxs-lookup"><span data-stu-id="68657-400">1.00</span></span>           | <span data-ttu-id="68657-401">01/09/2018</span><span class="sxs-lookup"><span data-stu-id="68657-401">9/1/2018</span></span>        | <span data-ttu-id="68657-402">3,00</span><span class="sxs-lookup"><span data-stu-id="68657-402">3.00</span></span>    |

#### <a name="no-accrual-monthly-plan"></a><span data-ttu-id="68657-403">Aylık tahakkuk planı yok</span><span class="sxs-lookup"><span data-stu-id="68657-403">No accrual monthly plan</span></span>

<span data-ttu-id="68657-404">**Plan kurulumu**</span><span class="sxs-lookup"><span data-stu-id="68657-404">**Plan setup**</span></span>

| <span data-ttu-id="68657-405">Plan başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-405">Plan start date</span></span> | <span data-ttu-id="68657-406">Tahakkuk sıklığı</span><span class="sxs-lookup"><span data-stu-id="68657-406">Accrual frequency</span></span> | <span data-ttu-id="68657-407">Tahakkuk dönemi esası</span><span class="sxs-lookup"><span data-stu-id="68657-407">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="68657-408">01/01/2018</span><span class="sxs-lookup"><span data-stu-id="68657-408">1/1/2018</span></span>        | <span data-ttu-id="68657-409">Aylık</span><span class="sxs-lookup"><span data-stu-id="68657-409">Monthly</span></span>           | <span data-ttu-id="68657-410">Plan başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-410">Plan start date</span></span>      |

<span data-ttu-id="68657-411">**Sonuçlar**</span><span class="sxs-lookup"><span data-stu-id="68657-411">**Results**</span></span>

| <span data-ttu-id="68657-412">Personel</span><span class="sxs-lookup"><span data-stu-id="68657-412">Employee</span></span>            | <span data-ttu-id="68657-413">Hizmetteki ay sayısı</span><span class="sxs-lookup"><span data-stu-id="68657-413">Months of service</span></span> | <span data-ttu-id="68657-414">Kayıt tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-414">Enrollment date</span></span> | <span data-ttu-id="68657-415">Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="68657-415">Start date</span></span> | <span data-ttu-id="68657-416">Tahakkuk tutarı</span><span class="sxs-lookup"><span data-stu-id="68657-416">Accrual amount</span></span> | <span data-ttu-id="68657-417">İşlem tahakkuku</span><span class="sxs-lookup"><span data-stu-id="68657-417">Process accrual</span></span> | <span data-ttu-id="68657-418">Bilanço</span><span class="sxs-lookup"><span data-stu-id="68657-418">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="68657-419">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="68657-419">Jeannette Nicholson</span></span> | <span data-ttu-id="68657-420">0,00</span><span class="sxs-lookup"><span data-stu-id="68657-420">0.00</span></span>              | <span data-ttu-id="68657-421">01/06/2018</span><span class="sxs-lookup"><span data-stu-id="68657-421">6/1/2018</span></span>        | <span data-ttu-id="68657-422">01/06/2018</span><span class="sxs-lookup"><span data-stu-id="68657-422">6/1/2018</span></span>   | <span data-ttu-id="68657-423">1.00</span><span class="sxs-lookup"><span data-stu-id="68657-423">1.00</span></span>           | <span data-ttu-id="68657-424">01/09/2018</span><span class="sxs-lookup"><span data-stu-id="68657-424">9/1/2018</span></span>        | <span data-ttu-id="68657-425">3,00</span><span class="sxs-lookup"><span data-stu-id="68657-425">3.00</span></span>    |
| <span data-ttu-id="68657-426">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="68657-426">Jay Norman</span></span>          | <span data-ttu-id="68657-427">0,00</span><span class="sxs-lookup"><span data-stu-id="68657-427">0.00</span></span>              | <span data-ttu-id="68657-428">15/06/2018</span><span class="sxs-lookup"><span data-stu-id="68657-428">6/15/2018</span></span>       | <span data-ttu-id="68657-429">15/06/2018</span><span class="sxs-lookup"><span data-stu-id="68657-429">6/15/2018</span></span>  | <span data-ttu-id="68657-430">1.00</span><span class="sxs-lookup"><span data-stu-id="68657-430">1.00</span></span>           | <span data-ttu-id="68657-431">01/09/2018</span><span class="sxs-lookup"><span data-stu-id="68657-431">9/1/2018</span></span>        | <span data-ttu-id="68657-432">2.00</span><span class="sxs-lookup"><span data-stu-id="68657-432">2.00</span></span>    |
