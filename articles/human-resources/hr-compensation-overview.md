---
title: Ücret planları
description: Ücret ve Kazanç Yöneticileri, kuruluşun çalışanları için sabit veya değişken ücret planlarını korumak ve işlemek için Ücret yönetimi kullanabilirler.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmCompensationLevel, HRCCompGrid, HRMCompFixedAction, HRMCompFixedBudget, HRMCompFixedPlanTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 1b2494ac717bc8c0171be49cc39e6aefff4425ab
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010915"
---
# <a name="compensation-plans"></a><span data-ttu-id="994d8-103">Ücret planları</span><span class="sxs-lookup"><span data-stu-id="994d8-103">Compensation plans</span></span>

<span data-ttu-id="994d8-104">Ücret ve Kazanç Yöneticileri, kuruluşun çalışanları için sabit veya değişken ücret planlarını korumak ve işlemek için Ücret yönetimi kullanabilirler.</span><span class="sxs-lookup"><span data-stu-id="994d8-104">Compensation and Benefits Managers can use Compensation management to maintain and process fixed and variable compensation plans for the organization's employees.</span></span>

### <a name="introduction"></a><span data-ttu-id="994d8-105">Giriş</span><span class="sxs-lookup"><span data-stu-id="994d8-105">Introduction</span></span>

<span data-ttu-id="994d8-106">Ücret yönetimi, temel maaş ve ikramiyelerin teslimatının denetimi için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="994d8-106">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="994d8-107">Bir personelin sabit temel maaşı ve başarı artışı, sabit ücret planları aracılığıyla denetlenir.</span><span class="sxs-lookup"><span data-stu-id="994d8-107">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="994d8-108">İkramiyelerin ödemesi, örneğin prim ödemeleri, performans ödülleri, hisseler, hibeler ve ayrıca da tek seferlik ödüller, değişken ücret planları tarafından denetlenir.</span><span class="sxs-lookup"><span data-stu-id="994d8-108">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span> 

<span data-ttu-id="994d8-109">Çalışanlar her iki tipteki bir veya daha çok plana kayıtlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="994d8-109">Employees can be enrolled in one or more plans of both types.</span></span> <span data-ttu-id="994d8-110">Bir çalışanın ücret planındaki kayıt için uygun olması için aşağıdaki gereksinimleri karşılaması gerekir:</span><span class="sxs-lookup"><span data-stu-id="994d8-110">An employee must meet the following requirements in order to be eligible for enrollment in a compensation plan:</span></span>
-   <span data-ttu-id="994d8-111">Çalışanın aktif bir pozisyon atamasının olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="994d8-111">The employee must have an active position assignment.</span></span>
-   <span data-ttu-id="994d8-112">Çalışanın maaş planı uygunluk kuralları tarafından tanımlanan ölçütlere uyması gerekir.</span><span class="sxs-lookup"><span data-stu-id="994d8-112">The employee must meet the criteria that are defined by eligibility rules for a compensation plan.</span></span>

## <a name="compensation-setup"></a><span data-ttu-id="994d8-113"> Ücret ayarla</span><span class="sxs-lookup"><span data-stu-id="994d8-113">Compensation setup</span></span>
<span data-ttu-id="994d8-114">Aşağıdaki tablo, Şirketinizin ücretlendirme planını ayarlarken ücretlendirme işleminin bütünleyici olabilecek bileşenlerini listelemektedir.</span><span class="sxs-lookup"><span data-stu-id="994d8-114">The following table lists components of the compensation process that can be integral in setting up your company's compensation plans.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="994d8-115">Bileşen</span><span class="sxs-lookup"><span data-stu-id="994d8-115">Component</span></span></th>
<th><span data-ttu-id="994d8-116">Daha fazla bilgi...</span><span class="sxs-lookup"><span data-stu-id="994d8-116">More information…</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="994d8-117">Sabit maaş eylemleri</span><span class="sxs-lookup"><span data-stu-id="994d8-117">Fixed compensation actions</span></span></td>
<td><span data-ttu-id="994d8-118">Sabit ücret eylemleri iki amacı gerçekleştirir:</span><span class="sxs-lookup"><span data-stu-id="994d8-118">Fixed compensation actions accomplish two purposes:</span></span>
<ul>
<li><span data-ttu-id="994d8-119">Eylemler, bir çalışanın ücreti değiştiğinde kayıt edilmesi gereken bilgileri belirleyebilir.</span><span class="sxs-lookup"><span data-stu-id="994d8-119">Actions can specify the kind of information that must be recorded when an employee’s compensation changes.</span></span> <span data-ttu-id="994d8-120">Örneğin, promosyon veya indirme gibi bir değişim için bir sebebin kaydedilmesini gerektirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="994d8-120">For example, you can require that the reason a change, such as a promotion or a demotion be recorded.</span></span></li>
<li><span data-ttu-id="994d8-121">Eylemler, bir hesaplamanın bir sabit ücret planı işlendiğinde uygulandığından emin olunması sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="994d8-121">Actions can ensure that a calculation is applied when fixed compensation plans are processed.</span></span>  <span data-ttu-id="994d8-122">Örneğin, öz varlık türündeki eylemler, çalışanın ücretini, çalışanın seviyesinin en düşük referans noktasıyla kıyaslar ve çalışanın en az minimum miktar kadar ücret aldığından emin olunmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="994d8-122">For example, actions of type Equity will compare the employees pay to the minimum reference point for the level on the employee&#39;s and ensure the employee is getting paid at least the minimum.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="994d8-123">Düzeyler</span><span class="sxs-lookup"><span data-stu-id="994d8-123">Levels</span></span></td>
<td><span data-ttu-id="994d8-124">Düzeyler işlerle ve bir işle ilgili olan tüm pozisyonlarla ilişkilidir.</span><span class="sxs-lookup"><span data-stu-id="994d8-124">Levels are associated with jobs and any positions that are related to a job reference.</span></span> <span data-ttu-id="994d8-125">Üç ücret planı tipi için de farklı düzeyler oluşturabilirsiniz: Derece, Bant ve Adım.</span><span class="sxs-lookup"><span data-stu-id="994d8-125">You can create discrete levels for the three types of compensation plans: Grade, Band, and Step.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="994d8-126">Ücret kademesi kullanım oranı matrisi</span><span class="sxs-lookup"><span data-stu-id="994d8-126">Range utilization matrix</span></span></td>
<td><span data-ttu-id="994d8-127">Kademesi kullanım oranı matrisi, çalışanları işlerinin denetim noktalarına geçiş yaptırmanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="994d8-127">A range utilization matrix helps you transition employees to the control point for their jobs.</span></span> <span data-ttu-id="994d8-128">Ayrıca, bireysel bir çalışanın performansına veya şirketin genel performansına bakmaksızın, şirket içindeki ödeme oranı eşitliğini kontrol etmek için aralık kullanımını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="994d8-128">You can also use range utilization to control pay rate equity in the company without regard to an individual employee&#39;s performance or the overall performance of the company.</span></span> <span data-ttu-id="994d8-129">Örneğin, kendi aralıklarında daha düşük ödeme alan çalışanlar, aralıkta daha yüksek ücret alan çalışanlara göre daha yüksek oranlı artışlar alır.</span><span class="sxs-lookup"><span data-stu-id="994d8-129">For example, employees who are paid lower in their range get higher percentage increases than employees who are paid higher in the range.</span></span> <span data-ttu-id="994d8-130">Bu şekilde, öz varlıklar arasındaki farkları sistematik olarak mahsup edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="994d8-130">In this manner, you can systematically offset equity differences.</span></span> <span data-ttu-id="994d8-131">Kademesi kullanımı aşağıdaki gibi hesaplanır: (Sabit ödeme oranı - Aralik minimumu) ÷ (Aralık maksimumu - Aralık minimumu).</span><span class="sxs-lookup"><span data-stu-id="994d8-131">The range utilization is calculated as follows: (Fixed Pay Rate - Range Minimum) ÷ (Range Maximum - Range Minimum).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="994d8-132">Referans noktası ayarları</span><span class="sxs-lookup"><span data-stu-id="994d8-132">Reference point setups</span></span></td>
<td><span data-ttu-id="994d8-133">Bir referans noktası ayarlamasına, matris içindeki aralığı temsil eden bir dizi referans noktası dahildir.</span><span class="sxs-lookup"><span data-stu-id="994d8-133">A reference point setup includes a set of reference points that represent ranges in a matrix.</span></span> <span data-ttu-id="994d8-134">Her aralık bir ödeme oranı ile ilişkili olabilir.</span><span class="sxs-lookup"><span data-stu-id="994d8-134">Each range can be associated with a pay rate.</span></span> <span data-ttu-id="994d8-135">Örneğin, kademe planları genellikle; en az, orta nokta ve en sık referans noktalarına sahip olacaktır.</span><span class="sxs-lookup"><span data-stu-id="994d8-135">For example, grade plans will often have reference points of Minimum, Midpoint, and Maximum.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="994d8-136">Ücret matrisi</span><span class="sxs-lookup"><span data-stu-id="994d8-136">Compensation matrix</span></span></td>
<td><span data-ttu-id="994d8-137">Ücret matrisi, bir ücretlendirme yapısı oluşturmak için kullanabileceğiniz referans noktaları ve düzeyleri kümesidir.</span><span class="sxs-lookup"><span data-stu-id="994d8-137">A compensation matrix is the set of reference points and levels that you use to create a compensation structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="994d8-138">Maaş yapısı</span><span class="sxs-lookup"><span data-stu-id="994d8-138">Compensation structure</span></span></td>
<td><span data-ttu-id="994d8-139">Bir ücret yapısı, ödeme oranlarının her bir düzey için referans noktalarıyla ilişkilendirildiği bir ödeme matrisidir.</span><span class="sxs-lookup"><span data-stu-id="994d8-139">A compensation structure is a compensation matrix that has pay rates associated with the reference points for each level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="994d8-140">Uygunluk kuralları</span><span class="sxs-lookup"><span data-stu-id="994d8-140">Eligibility rules</span></span></td>
<td><span data-ttu-id="994d8-141">Uygunluk kuralları, çalışanların dahil olduğu belirli işler, iş işlevler, iş türler, departmanlar, işçi sendikaları veya belirli maaş planları tarafından kapsanan maaş bölgeleri tanımlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="994d8-141">Eligibility rules are used to identify employees in specific jobs, job functions, job types, departments, labor unions, or compensation regions that are covered by specific compensation plans.</span></span> <span data-ttu-id="994d8-142">Çalışanları plana kaydetmek için hem değişken hem de sabit maaş planları için uygunluk kuralları oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="994d8-142">You must create eligibility rules for both variable and fixed compensation plans in order to enroll employees in the plan.</span></span> <span data-ttu-id="994d8-143">Bir tazminat planına ilişkin uygunluk kurallarını belirttikten sonra, plandan, plan tarafından kapsanan işlere uygulanacak düzey kümelerini tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="994d8-143">After eligibility rules are specified for a compensation plan, you can define the levels that should apply to the jobs that are covered by the plan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="994d8-144">Ödeme sıklıkları</span><span class="sxs-lookup"><span data-stu-id="994d8-144">Pay frequencies</span></span></td>
<td><span data-ttu-id="994d8-145">Ödeme sıklıkları, ücretin belirtildiği zaman aralığını belirtmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="994d8-145">Pay frequencies are used to define the time period for which the compensation is specified.</span></span>  <span data-ttu-id="994d8-146">Örneğin, ödeme sıklığı, saatlik ödeme oranına karşılık, yıllık bir maaş olarak mı belirtilmiş olduğunu anlamanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="994d8-146">For example, the pay frequency helps you understand if the compensation amount is specified as an annual salary versus an hourly pay rate.</span></span> <span data-ttu-id="994d8-147">Ödeme sıklıkları ayrıca dönüşüm faktörlerini, aylık, haftalık, iki haftalık ve saatlik ödeme sıklıklarını, yıllık ödeme sıklığına dönüştürmek için dönüşüm faktörlerini ayarlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="994d8-147">Pay frequencies are also used to set up conversion factors to convert compensation amounts from monthly, weekly, biweekly and hourly pay frequencies to an annual pay frequency.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="994d8-148">Tazminat bölgeleri</span><span class="sxs-lookup"><span data-stu-id="994d8-148">Compensation regions</span></span></td>
<td><span data-ttu-id="994d8-149">Ücret bölgeleri, çalışma alanı konumu esas alınarak çalışanın maaşını belirtmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="994d8-149">Compensation regions are used to specify employee compensation based on the location of the workplace.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="994d8-150">Kontrol noktası</span><span class="sxs-lookup"><span data-stu-id="994d8-150">Control point</span></span></td>
<td><span data-ttu-id="994d8-151">Kontrol noktası tüm çalışanlar için tazminat düzeyinin ne olduğunu düşündüğünüzü belirleyen ödeme oranını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="994d8-151">The control point defines what you consider to be the ideal pay rate for all employees at a compensation level.</span></span> <span data-ttu-id="994d8-152">Kademeli plan yapılarında kontrol noktaları genellikle aralığın orta noktasıdır.</span><span class="sxs-lookup"><span data-stu-id="994d8-152">For grade plan structures, control points are typically the midpoint of the ranges.</span></span> <span data-ttu-id="994d8-153">Bant yapıları nadiren kontrol noktaları kullanır.</span><span class="sxs-lookup"><span data-stu-id="994d8-153">Band structures rarely use control points.</span></span> <span data-ttu-id="994d8-154">Sabit maaş planı için denetim noktasını, Sabit maaş planları formunda belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="994d8-154">You can specify the control point for a fixed compensation plan in the Fixed compensation plans form.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="994d8-155">İş işlevleri</span><span class="sxs-lookup"><span data-stu-id="994d8-155">Job functions</span></span></td>
<td><span data-ttu-id="994d8-156">İş işlevleri, belirli işler için maaş planlarını sınıflandırmada ve filtre uygulamada kullanılır.</span><span class="sxs-lookup"><span data-stu-id="994d8-156">Job functions are used to classify and filter compensation plans to specific jobs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="994d8-157">İş tipleri</span><span class="sxs-lookup"><span data-stu-id="994d8-157">Job types</span></span></td>
<td><span data-ttu-id="994d8-158">İş türleri, belirli işler için maaş planlarını sınıflandırmada ve filtre uygulamada kullanılır.</span><span class="sxs-lookup"><span data-stu-id="994d8-158">Job types are used to classify and filter compensation plans to specific jobs.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="994d8-159">Değişken maaş tipleri</span><span class="sxs-lookup"><span data-stu-id="994d8-159">Variable compensation types</span></span></td>
<td><span data-ttu-id="994d8-160">Stok ödülleri veya nakit ödül primleri gibi değişken tazminat tipleri değişken tazminat planlarında ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="994d8-160">Variable compensation types, such as stock awards or cash award bonuses, are set up in variable compensation plans.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="994d8-161">Maaş kılavuzları</span><span class="sxs-lookup"><span data-stu-id="994d8-161">Compensation grids</span></span></td>
<td><span data-ttu-id="994d8-162">Ücret yapısını içeren ücret kılavuzları.</span><span class="sxs-lookup"><span data-stu-id="994d8-162">Compensation grids contain the compensation structure.</span></span>  <span data-ttu-id="994d8-163">Ücret kılavuzları, bir veya birden fazla ücret planları tarafından kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="994d8-163">Compensation grids can be used by one or more compensation plans.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="994d8-164">Performans planları</span><span class="sxs-lookup"><span data-stu-id="994d8-164">Performance plans</span></span></td>
<td><span data-ttu-id="994d8-165">Performans planları bir performans için ödeme stratejisinde kullanmak için planı bir dağıtım matrisiyle ilişkilendirmede kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="994d8-165">Performance plans are used to associate performance with an allocation matrix, so that you can use the plan in a pay-for-performance strategy.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="994d8-166">Performans değerlendirmeleri</span><span class="sxs-lookup"><span data-stu-id="994d8-166">Performance ratings</span></span></td>
<td><span data-ttu-id="994d8-167">Performans notları, performans planlarında bir hak edilen ödül tutarını veya performans ödülünü belirlemek üzere kullanılır.</span><span class="sxs-lookup"><span data-stu-id="994d8-167">Performance ratings are used in performance plans to determine the amount of a merit award or performance award.</span></span></td>
</tr>
</tbody>
</table>

## <a name="process-events"></a><span data-ttu-id="994d8-168"> İşleme olayları</span><span class="sxs-lookup"><span data-stu-id="994d8-168">Process events</span></span>
<span data-ttu-id="994d8-169">Bir işleme olayı, bir veya daha fazla sabit ya da değişken tazminat planına kayıtlı tüm çalışanlar için belirli bir döneme ait tazminat bilgilerini hesaplayan ücret iş akışlarıdır.</span><span class="sxs-lookup"><span data-stu-id="994d8-169">A process event calculates compensation information for a specific period for all employees who are enrolled in one or more fixed or variable compensation plans.</span></span> <span data-ttu-id="994d8-170">Bir işleme olayını, ücretlendirme sonuçlarını test etmek veya güncelleştirmek için tekrar tekrar çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="994d8-170">You can run a process event repeatedly to test or update calculated compensation results.</span></span>

<a name="compensation-events"></a><span data-ttu-id="994d8-171">Maaş olayları</span><span class="sxs-lookup"><span data-stu-id="994d8-171">Compensation events</span></span>
-------------------

<span data-ttu-id="994d8-172">İşlem etkinliği her çalıştırıldığında bir ücret etkinliği oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="994d8-172">Each time a process event is run, a compensation event is created.</span></span>  <span data-ttu-id="994d8-173">Ücret etkinlikleri, bu işlem etkinliğine dahil edilmiş her personel ücret işleminin sonucunu içerirler.</span><span class="sxs-lookup"><span data-stu-id="994d8-173">Compensation events contain the results of the compensation process for each employee included in that process event.</span></span>  <span data-ttu-id="994d8-174">Hesaplamalar doğru olduğunda, işlem etkinliklerinden etkilenen personellerin ücret kayıtlarını güncelleştirmek için ücret etkinliğini yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="994d8-174">When the calculations are correct, you can load the compensation event to update the compensation records for the employees who are affected by the process event.</span></span>

## <a name="recommendations"></a><span data-ttu-id="994d8-175"> Öneriler</span><span class="sxs-lookup"><span data-stu-id="994d8-175">Recommendations</span></span>
<span data-ttu-id="994d8-176">İşlem olayını çalıştırdıktan sonra, bir çalışanın başarı artış veya ikramiye tutarına, işleme olayında hesaplanan yönergelere göre ayarlamalar yapılması önerilir.</span><span class="sxs-lookup"><span data-stu-id="994d8-176">After you run a process event, you can recommend adjustments to an employee’s merit increase or award amount, based on the calculated guidelines of the process event.</span></span> <span data-ttu-id="994d8-177">Çalışanlar için öneriler yapmak için ücret planlarını veya işlem olayını ayarladığınızda, önerileri etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="994d8-177">To make recommendations for employees, you must enable recommendations when you set up compensation plans or when you set up the process event.</span></span>



