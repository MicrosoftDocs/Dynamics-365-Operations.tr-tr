---
title: Ücret planları
description: Ücret ve Kazanç Yöneticileri, kuruluşun çalışanları için sabit veya değişken ücret planlarını korumak ve işlemek için Ücret yönetimi kullanabilirler.
author: andreabichsel
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmCompensationLevel, HRCCompGrid, HRMCompFixedAction, HRMCompFixedBudget, HRMCompFixedPlanTable, HcmCompensationWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: b773b12b7eb3a8a59627d011f2469a98c5dde58a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058932"
---
# <a name="compensation-plans"></a><span data-ttu-id="695c9-103">Ücret planları</span><span class="sxs-lookup"><span data-stu-id="695c9-103">Compensation plans</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="695c9-104">Ücret ve Kazanç Yöneticileri, kuruluşun çalışanları için sabit veya değişken ücret planlarını korumak ve işlemek için Ücret yönetimi kullanabilirler.</span><span class="sxs-lookup"><span data-stu-id="695c9-104">Compensation and Benefits Managers can use Compensation management to maintain and process fixed and variable compensation plans for the organization's employees.</span></span>

### <a name="introduction"></a><span data-ttu-id="695c9-105">Giriş</span><span class="sxs-lookup"><span data-stu-id="695c9-105">Introduction</span></span>

<span data-ttu-id="695c9-106">Ücret yönetimi, temel maaş ve ikramiyelerin teslimatının denetimi için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="695c9-106">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="695c9-107">Bir personelin sabit temel maaşı ve başarı artışı, sabit ücret planları aracılığıyla denetlenir.</span><span class="sxs-lookup"><span data-stu-id="695c9-107">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="695c9-108">İkramiyelerin ödemesi, örneğin prim ödemeleri, performans ödülleri, hisseler, hibeler ve ayrıca da tek seferlik ödüller, değişken ücret planları tarafından denetlenir.</span><span class="sxs-lookup"><span data-stu-id="695c9-108">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span> 

<span data-ttu-id="695c9-109">Çalışanlar her iki tipteki bir veya daha çok plana kayıtlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="695c9-109">Employees can be enrolled in one or more plans of both types.</span></span> <span data-ttu-id="695c9-110">Bir çalışanın ücret planındaki kayıt için uygun olması için aşağıdaki gereksinimleri karşılaması gerekir:</span><span class="sxs-lookup"><span data-stu-id="695c9-110">An employee must meet the following requirements in order to be eligible for enrollment in a compensation plan:</span></span>
-   <span data-ttu-id="695c9-111">Çalışanın aktif bir pozisyon atamasının olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="695c9-111">The employee must have an active position assignment.</span></span>
-   <span data-ttu-id="695c9-112">Çalışanın maaş planı uygunluk kuralları tarafından tanımlanan ölçütlere uyması gerekir.</span><span class="sxs-lookup"><span data-stu-id="695c9-112">The employee must meet the criteria that are defined by eligibility rules for a compensation plan.</span></span>

## <a name="compensation-setup"></a><span data-ttu-id="695c9-113"> Ücret ayarla</span><span class="sxs-lookup"><span data-stu-id="695c9-113">Compensation setup</span></span>
<span data-ttu-id="695c9-114">Aşağıdaki tablo, Şirketinizin ücretlendirme planını ayarlarken ücretlendirme işleminin bütünleyici olabilecek bileşenlerini listelemektedir.</span><span class="sxs-lookup"><span data-stu-id="695c9-114">The following table lists components of the compensation process that can be integral in setting up your company's compensation plans.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="695c9-115">Bileşen</span><span class="sxs-lookup"><span data-stu-id="695c9-115">Component</span></span></th>
<th><span data-ttu-id="695c9-116">Daha fazla bilgi...</span><span class="sxs-lookup"><span data-stu-id="695c9-116">More information…</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="695c9-117">Sabit maaş eylemleri</span><span class="sxs-lookup"><span data-stu-id="695c9-117">Fixed compensation actions</span></span></td>
<td><span data-ttu-id="695c9-118">Sabit ücret eylemleri iki amacı gerçekleştirir:</span><span class="sxs-lookup"><span data-stu-id="695c9-118">Fixed compensation actions accomplish two purposes:</span></span>
<ul>
<li><span data-ttu-id="695c9-119">Eylemler, bir çalışanın ücreti değiştiğinde kayıt edilmesi gereken bilgileri belirleyebilir.</span><span class="sxs-lookup"><span data-stu-id="695c9-119">Actions can specify the kind of information that must be recorded when an employee’s compensation changes.</span></span> <span data-ttu-id="695c9-120">Örneğin, promosyon veya indirme gibi bir değişim için bir sebebin kaydedilmesini gerektirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="695c9-120">For example, you can require that the reason a change, such as a promotion or a demotion be recorded.</span></span></li>
<li><span data-ttu-id="695c9-121">Eylemler, bir hesaplamanın bir sabit ücret planı işlendiğinde uygulandığından emin olunması sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="695c9-121">Actions can ensure that a calculation is applied when fixed compensation plans are processed.</span></span>  <span data-ttu-id="695c9-122">Örneğin, öz varlık türündeki eylemler, çalışanın ücretini, çalışanın seviyesinin en düşük referans noktasıyla kıyaslar ve çalışanın en az minimum miktar kadar ücret aldığından emin olunmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="695c9-122">For example, actions of type Equity will compare the employees pay to the minimum reference point for the level on the employee&#39;s and ensure the employee is getting paid at least the minimum.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="695c9-123">Düzeyler</span><span class="sxs-lookup"><span data-stu-id="695c9-123">Levels</span></span></td>
<td><span data-ttu-id="695c9-124">Düzeyler işlerle ve bir işle ilgili olan tüm pozisyonlarla ilişkilidir.</span><span class="sxs-lookup"><span data-stu-id="695c9-124">Levels are associated with jobs and any positions that are related to a job reference.</span></span> <span data-ttu-id="695c9-125">Üç ücret planı tipi için de farklı düzeyler oluşturabilirsiniz: Derece, Bant ve Adım.</span><span class="sxs-lookup"><span data-stu-id="695c9-125">You can create discrete levels for the three types of compensation plans: Grade, Band, and Step.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="695c9-126">Ücret kademesi kullanım oranı matrisi</span><span class="sxs-lookup"><span data-stu-id="695c9-126">Range utilization matrix</span></span></td>
<td><span data-ttu-id="695c9-127">Kademesi kullanım oranı matrisi, çalışanları işlerinin denetim noktalarına geçiş yaptırmanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="695c9-127">A range utilization matrix helps you transition employees to the control point for their jobs.</span></span> <span data-ttu-id="695c9-128">Ayrıca, bireysel bir çalışanın performansına veya şirketin genel performansına bakmaksızın, şirket içindeki ödeme oranı eşitliğini kontrol etmek için aralık kullanımını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="695c9-128">You can also use range utilization to control pay rate equity in the company without regard to an individual employee&#39;s performance or the overall performance of the company.</span></span> <span data-ttu-id="695c9-129">Örneğin, kendi aralıklarında daha düşük ödeme alan çalışanlar, aralıkta daha yüksek ücret alan çalışanlara göre daha yüksek oranlı artışlar alır.</span><span class="sxs-lookup"><span data-stu-id="695c9-129">For example, employees who are paid lower in their range get higher percentage increases than employees who are paid higher in the range.</span></span> <span data-ttu-id="695c9-130">Bu şekilde, öz varlıklar arasındaki farkları sistematik olarak mahsup edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="695c9-130">In this manner, you can systematically offset equity differences.</span></span> <span data-ttu-id="695c9-131">Kademesi kullanımı aşağıdaki gibi hesaplanır: (Sabit ödeme oranı - Aralik minimumu) ÷ (Aralık maksimumu - Aralık minimumu).</span><span class="sxs-lookup"><span data-stu-id="695c9-131">The range utilization is calculated as follows: (Fixed Pay Rate - Range Minimum) ÷ (Range Maximum - Range Minimum).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="695c9-132">Referans noktası ayarları</span><span class="sxs-lookup"><span data-stu-id="695c9-132">Reference point setups</span></span></td>
<td><span data-ttu-id="695c9-133">Bir referans noktası ayarlamasına, matris içindeki aralığı temsil eden bir dizi referans noktası dahildir.</span><span class="sxs-lookup"><span data-stu-id="695c9-133">A reference point setup includes a set of reference points that represent ranges in a matrix.</span></span> <span data-ttu-id="695c9-134">Her aralık bir ödeme oranı ile ilişkili olabilir.</span><span class="sxs-lookup"><span data-stu-id="695c9-134">Each range can be associated with a pay rate.</span></span> <span data-ttu-id="695c9-135">Örneğin, kademe planları genellikle; en az, orta nokta ve en sık referans noktalarına sahip olacaktır.</span><span class="sxs-lookup"><span data-stu-id="695c9-135">For example, grade plans will often have reference points of Minimum, Midpoint, and Maximum.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="695c9-136">Ücret matrisi</span><span class="sxs-lookup"><span data-stu-id="695c9-136">Compensation matrix</span></span></td>
<td><span data-ttu-id="695c9-137">Ücret matrisi, bir ücretlendirme yapısı oluşturmak için kullanabileceğiniz referans noktaları ve düzeyleri kümesidir.</span><span class="sxs-lookup"><span data-stu-id="695c9-137">A compensation matrix is the set of reference points and levels that you use to create a compensation structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="695c9-138">Maaş yapısı</span><span class="sxs-lookup"><span data-stu-id="695c9-138">Compensation structure</span></span></td>
<td><span data-ttu-id="695c9-139">Bir ücret yapısı, ödeme oranlarının her bir düzey için referans noktalarıyla ilişkilendirildiği bir ödeme matrisidir.</span><span class="sxs-lookup"><span data-stu-id="695c9-139">A compensation structure is a compensation matrix that has pay rates associated with the reference points for each level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="695c9-140">Uygunluk kuralları</span><span class="sxs-lookup"><span data-stu-id="695c9-140">Eligibility rules</span></span></td>
<td><span data-ttu-id="695c9-141">Uygunluk kuralları, çalışanların dahil olduğu belirli işler, iş işlevler, iş türler, departmanlar, işçi sendikaları veya belirli maaş planları tarafından kapsanan maaş bölgeleri tanımlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="695c9-141">Eligibility rules are used to identify employees in specific jobs, job functions, job types, departments, labor unions, or compensation regions that are covered by specific compensation plans.</span></span> <span data-ttu-id="695c9-142">Çalışanları plana kaydetmek için hem değişken hem de sabit maaş planları için uygunluk kuralları oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="695c9-142">You must create eligibility rules for both variable and fixed compensation plans in order to enroll employees in the plan.</span></span> <span data-ttu-id="695c9-143">Bir tazminat planına ilişkin uygunluk kurallarını belirttikten sonra, plandan, plan tarafından kapsanan işlere uygulanacak düzey kümelerini tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="695c9-143">After eligibility rules are specified for a compensation plan, you can define the levels that should apply to the jobs that are covered by the plan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="695c9-144">Ödeme sıklıkları</span><span class="sxs-lookup"><span data-stu-id="695c9-144">Pay frequencies</span></span></td>
<td><span data-ttu-id="695c9-145">Ödeme sıklıkları, ücretin belirtildiği zaman aralığını belirtmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="695c9-145">Pay frequencies are used to define the time period for which the compensation is specified.</span></span>  <span data-ttu-id="695c9-146">Örneğin, ödeme sıklığı, saatlik ödeme oranına karşılık, yıllık bir maaş olarak mı belirtilmiş olduğunu anlamanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="695c9-146">For example, the pay frequency helps you understand if the compensation amount is specified as an annual salary versus an hourly pay rate.</span></span> <span data-ttu-id="695c9-147">Ödeme sıklıkları ayrıca dönüşüm faktörlerini, aylık, haftalık, iki haftalık ve saatlik ödeme sıklıklarını, yıllık ödeme sıklığına dönüştürmek için dönüşüm faktörlerini ayarlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="695c9-147">Pay frequencies are also used to set up conversion factors to convert compensation amounts from monthly, weekly, biweekly and hourly pay frequencies to an annual pay frequency.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="695c9-148">Tazminat bölgeleri</span><span class="sxs-lookup"><span data-stu-id="695c9-148">Compensation regions</span></span></td>
<td><span data-ttu-id="695c9-149">Ücret bölgeleri, çalışma alanı konumu esas alınarak çalışanın maaşını belirtmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="695c9-149">Compensation regions are used to specify employee compensation based on the location of the workplace.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="695c9-150">Kontrol noktası</span><span class="sxs-lookup"><span data-stu-id="695c9-150">Control point</span></span></td>
<td><span data-ttu-id="695c9-151">Kontrol noktası tüm çalışanlar için tazminat düzeyinin ne olduğunu düşündüğünüzü belirleyen ödeme oranını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="695c9-151">The control point defines what you consider to be the ideal pay rate for all employees at a compensation level.</span></span> <span data-ttu-id="695c9-152">Kademeli plan yapılarında kontrol noktaları genellikle aralığın orta noktasıdır.</span><span class="sxs-lookup"><span data-stu-id="695c9-152">For grade plan structures, control points are typically the midpoint of the ranges.</span></span> <span data-ttu-id="695c9-153">Bant yapıları nadiren kontrol noktaları kullanır.</span><span class="sxs-lookup"><span data-stu-id="695c9-153">Band structures rarely use control points.</span></span> <span data-ttu-id="695c9-154">Sabit maaş planı için denetim noktasını, Sabit maaş planları formunda belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="695c9-154">You can specify the control point for a fixed compensation plan in the Fixed compensation plans form.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="695c9-155">İş işlevleri</span><span class="sxs-lookup"><span data-stu-id="695c9-155">Job functions</span></span></td>
<td><span data-ttu-id="695c9-156">İş işlevleri, belirli işler için maaş planlarını sınıflandırmada ve filtre uygulamada kullanılır.</span><span class="sxs-lookup"><span data-stu-id="695c9-156">Job functions are used to classify and filter compensation plans to specific jobs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="695c9-157">İş tipleri</span><span class="sxs-lookup"><span data-stu-id="695c9-157">Job types</span></span></td>
<td><span data-ttu-id="695c9-158">İş türleri, belirli işler için maaş planlarını sınıflandırmada ve filtre uygulamada kullanılır.</span><span class="sxs-lookup"><span data-stu-id="695c9-158">Job types are used to classify and filter compensation plans to specific jobs.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="695c9-159">Değişken maaş tipleri</span><span class="sxs-lookup"><span data-stu-id="695c9-159">Variable compensation types</span></span></td>
<td><span data-ttu-id="695c9-160">Stok ödülleri veya nakit ödül primleri gibi değişken tazminat tipleri değişken tazminat planlarında ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="695c9-160">Variable compensation types, such as stock awards or cash award bonuses, are set up in variable compensation plans.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="695c9-161">Maaş kılavuzları</span><span class="sxs-lookup"><span data-stu-id="695c9-161">Compensation grids</span></span></td>
<td><span data-ttu-id="695c9-162">Ücret yapısını içeren ücret kılavuzları.</span><span class="sxs-lookup"><span data-stu-id="695c9-162">Compensation grids contain the compensation structure.</span></span>  <span data-ttu-id="695c9-163">Ücret kılavuzları, bir veya birden fazla ücret planları tarafından kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="695c9-163">Compensation grids can be used by one or more compensation plans.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="695c9-164">Performans planları</span><span class="sxs-lookup"><span data-stu-id="695c9-164">Performance plans</span></span></td>
<td><span data-ttu-id="695c9-165">Performans planları bir performans için ödeme stratejisinde kullanmak için planı bir dağıtım matrisiyle ilişkilendirmede kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="695c9-165">Performance plans are used to associate performance with an allocation matrix, so that you can use the plan in a pay-for-performance strategy.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="695c9-166">Performans değerlendirmeleri</span><span class="sxs-lookup"><span data-stu-id="695c9-166">Performance ratings</span></span></td>
<td><span data-ttu-id="695c9-167">Performans notları, performans planlarında bir hak edilen ödül tutarını veya performans ödülünü belirlemek üzere kullanılır.</span><span class="sxs-lookup"><span data-stu-id="695c9-167">Performance ratings are used in performance plans to determine the amount of a merit award or performance award.</span></span></td>
</tr>
</tbody>
</table>

## <a name="process-events"></a><span data-ttu-id="695c9-168"> İşleme olayları</span><span class="sxs-lookup"><span data-stu-id="695c9-168">Process events</span></span>
<span data-ttu-id="695c9-169">Bir işleme olayı, bir veya daha fazla sabit ya da değişken tazminat planına kayıtlı tüm çalışanlar için belirli bir döneme ait tazminat bilgilerini hesaplayan ücret iş akışlarıdır.</span><span class="sxs-lookup"><span data-stu-id="695c9-169">A process event calculates compensation information for a specific period for all employees who are enrolled in one or more fixed or variable compensation plans.</span></span> <span data-ttu-id="695c9-170">Bir işleme olayını, ücretlendirme sonuçlarını test etmek veya güncelleştirmek için tekrar tekrar çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="695c9-170">You can run a process event repeatedly to test or update calculated compensation results.</span></span>

<a name="compensation-events"></a><span data-ttu-id="695c9-171">Maaş olayları</span><span class="sxs-lookup"><span data-stu-id="695c9-171">Compensation events</span></span>
-------------------

<span data-ttu-id="695c9-172">İşlem etkinliği her çalıştırıldığında bir ücret etkinliği oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="695c9-172">Each time a process event is run, a compensation event is created.</span></span>  <span data-ttu-id="695c9-173">Ücret etkinlikleri, bu işlem etkinliğine dahil edilmiş her personel ücret işleminin sonucunu içerirler.</span><span class="sxs-lookup"><span data-stu-id="695c9-173">Compensation events contain the results of the compensation process for each employee included in that process event.</span></span>  <span data-ttu-id="695c9-174">Hesaplamalar doğru olduğunda, işlem etkinliklerinden etkilenen personellerin ücret kayıtlarını güncelleştirmek için ücret etkinliğini yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="695c9-174">When the calculations are correct, you can load the compensation event to update the compensation records for the employees who are affected by the process event.</span></span>

## <a name="recommendations"></a><span data-ttu-id="695c9-175"> Öneriler</span><span class="sxs-lookup"><span data-stu-id="695c9-175">Recommendations</span></span>
<span data-ttu-id="695c9-176">İşlem olayını çalıştırdıktan sonra, bir çalışanın başarı artış veya ikramiye tutarına, işleme olayında hesaplanan yönergelere göre ayarlamalar yapılması önerilir.</span><span class="sxs-lookup"><span data-stu-id="695c9-176">After you run a process event, you can recommend adjustments to an employee’s merit increase or award amount, based on the calculated guidelines of the process event.</span></span> <span data-ttu-id="695c9-177">Çalışanlar için öneriler yapmak için ücret planlarını veya işlem olayını ayarladığınızda, önerileri etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="695c9-177">To make recommendations for employees, you must enable recommendations when you set up compensation plans or when you set up the process event.</span></span>





[!INCLUDE[footer-include](../includes/footer-banner.md)]