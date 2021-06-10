---
title: Departmanlar, işler ve pozisyonları kullanarak iş gücünüzü düzenleme
description: Departmanlar, işler ve pozisyonlar İnsan kaynakları içinde tutulan kuruluş öğeleridir. Bu konuda bu öğeler hakkında kavramsal bilgiler açıklanmıştır.
author: andreabichsel
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmJob, HcmPosition, OMOperatingUnit, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 87933
ms.assetid: eb5dcacb-a5fe-451d-b30a-7ef14da65d81
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 1279cd1eb0d495107515dd40f7d2e0f9dfd5e080
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058836"
---
# <a name="organize-your-workforce-by-using-departments-jobs-and-positions"></a><span data-ttu-id="02980-104">Departmanlar, işler ve pozisyonları kullanarak iş gücünüzü düzenleme</span><span class="sxs-lookup"><span data-stu-id="02980-104">Organize your workforce by using departments, jobs, and positions</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="02980-105">Departmanlar, işler ve pozisyonlar İnsan kaynakları içinde tutulan kuruluş öğeleridir.</span><span class="sxs-lookup"><span data-stu-id="02980-105">Departments, jobs, and positions are organizational elements that are maintained within Human resources.</span></span> <span data-ttu-id="02980-106">Bu konuda bu öğeler hakkında kavramsal bilgiler açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="02980-106">This article describes conceptual information about these elements.</span></span> 

<span data-ttu-id="02980-107">Aşağıdaki örnek, bu konuda açıklanan kavramları göstermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="02980-107">The following example is used to illustrate the concepts described in this article.</span></span>

|<span data-ttu-id="02980-108">**Departman**</span><span class="sxs-lookup"><span data-stu-id="02980-108">**Department**</span></span>|<span data-ttu-id="02980-109">**Bölme**</span><span class="sxs-lookup"><span data-stu-id="02980-109">**Position**</span></span>|<span data-ttu-id="02980-110">**İş**</span><span class="sxs-lookup"><span data-stu-id="02980-110">**Job**</span></span>|
|---|---|---|
|<span data-ttu-id="02980-111">**Satışlar**</span><span class="sxs-lookup"><span data-stu-id="02980-111">**Sales**</span></span>|<span data-ttu-id="02980-112">Satış yöneticisi (Doğu)</span><span class="sxs-lookup"><span data-stu-id="02980-112">Sales manager (East)</span></span>|<span data-ttu-id="02980-113">Satış yöneticisi</span><span class="sxs-lookup"><span data-stu-id="02980-113">Sales manager</span></span>|
|<span data-ttu-id="02980-114">**Satış**</span><span class="sxs-lookup"><span data-stu-id="02980-114">**Sales**</span></span>|<span data-ttu-id="02980-115">Satış yöneticisi (Batı)</span><span class="sxs-lookup"><span data-stu-id="02980-115">Sales manager (West)</span></span>|<span data-ttu-id="02980-116">Satış yöneticisi</span><span class="sxs-lookup"><span data-stu-id="02980-116">Sales manager</span></span>|
|<span data-ttu-id="02980-117">**Satış**</span><span class="sxs-lookup"><span data-stu-id="02980-117">**Sales**</span></span>|<span data-ttu-id="02980-118">Satış yöneticisi (Merkezi)</span><span class="sxs-lookup"><span data-stu-id="02980-118">Sales manager (Central)</span></span>|<span data-ttu-id="02980-119">Satış yöneticisi</span><span class="sxs-lookup"><span data-stu-id="02980-119">Sales manager</span></span>|
|<span data-ttu-id="02980-120">**Muhasebe**</span><span class="sxs-lookup"><span data-stu-id="02980-120">**Accounting**</span></span>|<span data-ttu-id="02980-121">Muhasebe gözetmeni</span><span class="sxs-lookup"><span data-stu-id="02980-121">Accounting supervisor</span></span>|<span data-ttu-id="02980-122">Muhasebe müdürü</span><span class="sxs-lookup"><span data-stu-id="02980-122">Accounting manager</span></span>|
|<span data-ttu-id="02980-123">**Muhasebe**</span><span class="sxs-lookup"><span data-stu-id="02980-123">**Accounting**</span></span>|<span data-ttu-id="02980-124">Muhasebe-A</span><span class="sxs-lookup"><span data-stu-id="02980-124">Accounting-A</span></span>|<span data-ttu-id="02980-125">Muhasebeci</span><span class="sxs-lookup"><span data-stu-id="02980-125">Accountant</span></span>|
|<span data-ttu-id="02980-126">**İnsan kaynakları**</span><span class="sxs-lookup"><span data-stu-id="02980-126">**Human resources**</span></span>|<span data-ttu-id="02980-127">İK yöneticisi (Doğu)</span><span class="sxs-lookup"><span data-stu-id="02980-127">HR manager (East)</span></span>|<span data-ttu-id="02980-128">İK yöneticisi</span><span class="sxs-lookup"><span data-stu-id="02980-128">HR manager</span></span>|
|<span data-ttu-id="02980-129">**İnsan kaynakları**</span><span class="sxs-lookup"><span data-stu-id="02980-129">**Human resources**</span></span>|<span data-ttu-id="02980-130">İK yöneticisi (Batı)</span><span class="sxs-lookup"><span data-stu-id="02980-130">HR manager (West)</span></span>|<span data-ttu-id="02980-131">İK yöneticisi</span><span class="sxs-lookup"><span data-stu-id="02980-131">HR manager</span></span>|
|<span data-ttu-id="02980-132">**İnsan kaynakları**</span><span class="sxs-lookup"><span data-stu-id="02980-132">**Human resources**</span></span>|<span data-ttu-id="02980-133">İK yöneticisi (Merkezi)</span><span class="sxs-lookup"><span data-stu-id="02980-133">HR manager (Central)</span></span>|<span data-ttu-id="02980-134">İK yöneticisi</span><span class="sxs-lookup"><span data-stu-id="02980-134">HR manager</span></span>|


 <a name="departments"></a><span data-ttu-id="02980-135">Departmanlar</span><span class="sxs-lookup"><span data-stu-id="02980-135">Departments</span></span>
------------

<span data-ttu-id="02980-136">Bir departman, organizasyonun satış veya muhasebe gibi belirli organizasyon alanından sorumlu bir kategorisini veya işlevsel alanını temsil eden bir işletme birimidir.</span><span class="sxs-lookup"><span data-stu-id="02980-136">A department is an operating unit that represents a category or functional area of an organization that is responsible for a specific area of the organization, such as sales or accounting.</span></span> <span data-ttu-id="02980-137">Bir departman, işlevsel alanlar konusunda raporlama yapmak için kullanılır ve kar ve zarar sorumluluğu olabilir.</span><span class="sxs-lookup"><span data-stu-id="02980-137">A department is used to report on functional areas and may have profit and loss responsibility.</span></span> <span data-ttu-id="02980-138">Ayrıca, bir departman maliyet merkezleri grubu da içerebilir.</span><span class="sxs-lookup"><span data-stu-id="02980-138">Also, a department might include a group of cost centers.</span></span> <span data-ttu-id="02980-139">Satış, muhasebe ve insan kaynakları organizasyondaki departmanlara bazı örneklerdir.</span><span class="sxs-lookup"><span data-stu-id="02980-139">Sales, accounting, and human resources are some examples of departments in an organization.</span></span>

## <a name="jobs-and-positions"></a><span data-ttu-id="02980-140">İşler ve pozisyonlar</span><span class="sxs-lookup"><span data-stu-id="02980-140">Jobs and positions</span></span>
<span data-ttu-id="02980-141">Bir iş, işi gerçekleştiren birinden beklenen görev ve sorumluluklar toplamıdır.</span><span class="sxs-lookup"><span data-stu-id="02980-141">A job is a collection of tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="02980-142">Bir pozisyon, bir işin bireysel eşdüşümüdür.</span><span class="sxs-lookup"><span data-stu-id="02980-142">A position is an individual instance of a job.</span></span> <span data-ttu-id="02980-143">İşle ilgili pozisyonlar için sorumluluk alanları, iş görevleri, iş işlevleri, beceriler, eğitim bilgileri ve bir iş için gereken sertifikalar da gereklidir.</span><span class="sxs-lookup"><span data-stu-id="02980-143">Areas of responsibility, job tasks, job functions, skills, education information, and certificates that are required for a job are also required for positions that are associated with a job.</span></span>
### <a name="job-tasks"></a><span data-ttu-id="02980-144">İş görevleri</span><span class="sxs-lookup"><span data-stu-id="02980-144">Job tasks</span></span>

<span data-ttu-id="02980-145">O işe yönelik pozisyondaki bir işçinin tamamlaması gereken temel görevleri açıklayan iş görevleri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="02980-145">You can create job tasks that describe the basic tasks that a worker in a position for that job must complete.</span></span> <span data-ttu-id="02980-146">Birden fazla işe aynı iş görevi eklenebilir ve bu işlere yönelik pozisyonlar bu iş görevlerini alacaktır.</span><span class="sxs-lookup"><span data-stu-id="02980-146">The same job task can be added to multiple jobs, and positions for those jobs will inherit those job tasks.</span></span> <span data-ttu-id="02980-147">İş görevlerine örnekler aşağıdaki tabloda listelenmiştir.</span><span class="sxs-lookup"><span data-stu-id="02980-147">Examples of job tasks are listed in the following table.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="02980-148">İş</span><span class="sxs-lookup"><span data-stu-id="02980-148">Job</span></span></th>
<th><span data-ttu-id="02980-149">İş görevi</span><span class="sxs-lookup"><span data-stu-id="02980-149">Job task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="02980-150">Satış yöneticisi</span><span class="sxs-lookup"><span data-stu-id="02980-150">Sales manager</span></span></td>
<td><ul>
<li><span data-ttu-id="02980-151"><span class="input">Perf-review</span> – Her bir satış personelinin performansını gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="02980-151"><span class="input">Perf-review</span> – Review each salesperson’s job performance.</span></span></li>
<li><span data-ttu-id="02980-152"><span class="input">Abs-review</span> – Her bir satış personelinin devamsızlık taleplerini veya kayıtlarını onaylayın veya reddedin.</span><span class="sxs-lookup"><span data-stu-id="02980-152"><span class="input">Abs-review</span> – Approve or reject each salesperson’s absence requests or registrations.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02980-153">Muhasebeci</span><span class="sxs-lookup"><span data-stu-id="02980-153">Accountant</span></span></td>
<td><span data-ttu-id="02980-154"><span class="input">FIN-Report</span> – Finans müdürüne haftalık mali raporlar sunun.</span><span class="sxs-lookup"><span data-stu-id="02980-154"><span class="input">FIN-Report</span> – Present weekly financial reports to chief financial officer.</span></span></td>
</tr>
</tbody>
</table>

### <a name="job-functions"></a><span data-ttu-id="02980-155">İş işlevleri</span><span class="sxs-lookup"><span data-stu-id="02980-155">Job functions</span></span>

<span data-ttu-id="02980-156">İş işlevleri iş görevleri gibidir.</span><span class="sxs-lookup"><span data-stu-id="02980-156">Job functions are like job tasks.</span></span> <span data-ttu-id="02980-157">Bir iş işlevi, projeye atanan bir veya daha fazla görevi veya sorumluluğu açıklar.</span><span class="sxs-lookup"><span data-stu-id="02980-157">A job function describes one or more tasks, duties or responsibilities that are assigned to a job.</span></span> <span data-ttu-id="02980-158">İş türleri, işlere atanabilir ve maaş planları için uygunluk kuralları oluşturmak ve uygulamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="02980-158">Job functions can be assigned to jobs and used to set up and implement eligibility rules for compensation plans.</span></span> <span data-ttu-id="02980-159">İş işlevlerine ilişkin örnekler aşağıdaki tabloda listelenmiştir.</span><span class="sxs-lookup"><span data-stu-id="02980-159">Examples of job functions are listed in the following table.</span></span>

| <span data-ttu-id="02980-160">İş</span><span class="sxs-lookup"><span data-stu-id="02980-160">Job</span></span>           | <span data-ttu-id="02980-161">İş işlevi</span><span class="sxs-lookup"><span data-stu-id="02980-161">Job function</span></span>                                                |
|---------------|-------------------------------------------------------------|
| <span data-ttu-id="02980-162">Satış yöneticisi</span><span class="sxs-lookup"><span data-stu-id="02980-162">Sales manager</span></span> | <span data-ttu-id="02980-163">Mng-people – Size rapor veren insanları yönetin.</span><span class="sxs-lookup"><span data-stu-id="02980-163">Mng-people – Manage people who report to you.</span></span>               |
| <span data-ttu-id="02980-164">Muhasebeci</span><span class="sxs-lookup"><span data-stu-id="02980-164">Accountant</span></span>    | <span data-ttu-id="02980-165">FIN-Review – Hesap kümeleri için mali verileri tutun.</span><span class="sxs-lookup"><span data-stu-id="02980-165">FIN-Review – Maintain financial data for a set of accounts.</span></span> |

### <a name="job-types"></a><span data-ttu-id="02980-166">İş tipleri</span><span class="sxs-lookup"><span data-stu-id="02980-166">Job types</span></span>

<span data-ttu-id="02980-167">Benzer işleri kategorilere ayırmak için iş türlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="02980-167">Use job types to classify similar jobs into categories.</span></span> <span data-ttu-id="02980-168">İş türleri de iş işlevleri gibi işlere atanabilir ve maaş planları için uygunluk kuralları oluşturmak ve uygulamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="02980-168">Job types, just like job functions, can be assigned to jobs and used to set up and implement eligibility rules for compensation plans.</span></span> <span data-ttu-id="02980-169">Aşağıdaki listede iş türlerine bazı örnekler verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="02980-169">Some examples of job types are included in the following list:</span></span>
-   <span data-ttu-id="02980-170">Tam zamanlı</span><span class="sxs-lookup"><span data-stu-id="02980-170">Full-time</span></span>
-   <span data-ttu-id="02980-171">Yarı zamanlı</span><span class="sxs-lookup"><span data-stu-id="02980-171">Part-time</span></span>
-   <span data-ttu-id="02980-172">Maaş</span><span class="sxs-lookup"><span data-stu-id="02980-172">Salary</span></span>
-   <span data-ttu-id="02980-173">Saatlik ödeme</span><span class="sxs-lookup"><span data-stu-id="02980-173">Hourly pay</span></span>

### <a name="areas-of-responsibility"></a><span data-ttu-id="02980-174">Sorumluluk alanları</span><span class="sxs-lookup"><span data-stu-id="02980-174">Areas of responsibility</span></span>

<span data-ttu-id="02980-175">Bir pozisyondaki işçinin o iş için sorumlu olacağı iş rollerini, süreçleri ve ürünleri belirtmek üzere sorumluluk alanlarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="02980-175">Use areas of responsibility to indicate the work roles, processes, and products that a worker in a position for that job would be responsible for.</span></span> <span data-ttu-id="02980-176">"Muhasebeci" başlıklı bir iş için sorumluluk alanına örnek "A Ürünü için finansal raporlama" olabilir.</span><span class="sxs-lookup"><span data-stu-id="02980-176">An example of an area of responsibility for a job titled “Accountant” might be “Financial reporting for Product A”.</span></span>

<a name="positions"></a><span data-ttu-id="02980-177">Pozisyonlar</span><span class="sxs-lookup"><span data-stu-id="02980-177">Positions</span></span>
----------

<span data-ttu-id="02980-178">Pozisyonlar, organizasyon hiyerarşisinin alt düzeylerinin önemli bir öğesidir.</span><span class="sxs-lookup"><span data-stu-id="02980-178">Positions are an important element of the lower level of an organization hierarchy.</span></span> <span data-ttu-id="02980-179">Bir pozisyon, bir işin bireysel eşdüşümüdür.</span><span class="sxs-lookup"><span data-stu-id="02980-179">A position is an individual instance of a job.</span></span> <span data-ttu-id="02980-180">Örneğin "Satış yöneticisi (Doğu)" pozisyonu, "Satış yöneticisi" işiyle ilişkilendirilmiş işlerden sadece biridir.</span><span class="sxs-lookup"><span data-stu-id="02980-180">For example, the position, “Sales manager (East),” is just one of the positions that is associated with the job, “Sales manager.”</span></span> <span data-ttu-id="02980-181">Bir departmanda ve çalışanlara tanmış olarak pozisyonlar vardır.</span><span class="sxs-lookup"><span data-stu-id="02980-181">Positions exist in a department and are assigned to workers.</span></span>
### <a name="position-creation-and-maintenance"></a><span data-ttu-id="02980-182">Pozisyon oluşturma ve muhafaza etme</span><span class="sxs-lookup"><span data-stu-id="02980-182">Position creation and maintenance</span></span>

-   <span data-ttu-id="02980-183">Pozisyonla ilişkili sistem değişikliklerinin geçmişini erişimi kolay bir liste sayfasında görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="02980-183">You can view a history of position-related system changes in an easy-to-access list page.</span></span>
-   <span data-ttu-id="02980-184">Kullanıcılarınızın pozisyonda oluşturup değiştirirken seçebileceği sebep kodları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="02980-184">You can create reason codes that your users can select when they create or modify positions.</span></span>
-   <span data-ttu-id="02980-185">Personel eylem türleri oluşturup personel eylemlerine bir numara sırası atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="02980-185">You can create personnel action types and assign a number sequence to personnel actions.</span></span>
-   <span data-ttu-id="02980-186">Pozisyon ekleme ve değişikliklerinin onay gerektirmesini sağlayacak iş akışları ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="02980-186">You can set up workflow so that position additions and changes can require approval.</span></span>

### <a name="position-duration"></a><span data-ttu-id="02980-187">Pozisyon süresi</span><span class="sxs-lookup"><span data-stu-id="02980-187">Position duration</span></span>

<span data-ttu-id="02980-188">Her pozisyon, geçerli olacağı bir zaman zarfına sahiptir.</span><span class="sxs-lookup"><span data-stu-id="02980-188">Every position has a length of time that the position is effective.</span></span> <span data-ttu-id="02980-189">Bu zaman zarfına süre denilir.</span><span class="sxs-lookup"><span data-stu-id="02980-189">This length of time is referred to as duration.</span></span> <span data-ttu-id="02980-190">Örneğin, yaz pozisyonları 1 Mayıs 2015'ten 31 Ağustos 2015'e kadar bir süreye sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="02980-190">For example, summer positions might have duration of May 1, 2015 until August 31, 2015.</span></span>

### <a name="worker-assignments"></a><span data-ttu-id="02980-191">Çalışan atamaları</span><span class="sxs-lookup"><span data-stu-id="02980-191">Worker assignments</span></span>

<span data-ttu-id="02980-192">Bir pozisyona işçi atadığınızda, o pozisyonu doldurmuş olursunuz.</span><span class="sxs-lookup"><span data-stu-id="02980-192">When you assign a worker to a position, you fill that position.</span></span> <span data-ttu-id="02980-193">İşçileri birden fazla pozisyona atayabilirsiniz ancak bir pozisyona aynı anda yalnızca bir işçi atanabilir.</span><span class="sxs-lookup"><span data-stu-id="02980-193">You can assign workers to multiple positions, but only one worker can be assigned to a position at the same time.</span></span>

### <a name="reporting-relationships"></a><span data-ttu-id="02980-194">Raporlama ilişkileri</span><span class="sxs-lookup"><span data-stu-id="02980-194">Reporting relationships</span></span>

<span data-ttu-id="02980-195">Pozisyonlar, bir organizasyon hiyerarşisinin alt düzeyi için önemli öğelerdir.</span><span class="sxs-lookup"><span data-stu-id="02980-195">Positions are important elements of the lower level of an organization hierarchy.</span></span> <span data-ttu-id="02980-196">Pozisyon formunda, bir pozisyonun rapor vereceği pozisyonu belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="02980-196">In the Position form, you can specify the position that a position reports to.</span></span> <span data-ttu-id="02980-197">Bir pozisyona başka bir pozisyona rapor veren bir işçi atadığınızda, iki pozisyona atanan işçiler arasında bir raporlama ilişkisi oluşturmuş olursunuz.</span><span class="sxs-lookup"><span data-stu-id="02980-197">When you assign a worker to a position that reports to another position, you create a reporting relationship between the workers who are assigned to the two positions.</span></span> <span data-ttu-id="02980-198">Örneğin, "Muhasebeci A" pozisyonu "Muhasebe Gözetmeni" pozisyonuna rapor verir.</span><span class="sxs-lookup"><span data-stu-id="02980-198">For example, position “Accountant-A” reports to position “Accounting Supervisor”.</span></span> <span data-ttu-id="02980-199">Kim Akers "Muhasebe Gözetmeni" pozisyonuna atanmıştır ve Sanjay Patel "Muhasebeci A" pozisyonuna atanmıştır.</span><span class="sxs-lookup"><span data-stu-id="02980-199">Kim Akers is assigned to position “Accounting Supervisor” and Sanjay Patel is assigned to position “Accountant-A”.</span></span> <span data-ttu-id="02980-200">Bu, Sanjay Patel'in Kim Akers'a rapor vereceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="02980-200">This means that Sanjay Patel reports to Kim Akers.</span></span> 

<span data-ttu-id="02980-201">Organizasyonunuz bir matris hiyerarşisi veya başka bir özel hiyerarşi kullanıyorsa, pozisyon hiyerarşisi türleri ayarlayabilir ve ayarladığınız her bir hiyerarşi türü için pozisyonlara rapor ilişkileri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="02980-201">If your organization uses a matrix hierarchy or another custom hierarchy, you can set up position hierarchy types and then add reporting relationships to positions for each hierarchy type that you set up.</span></span> <span data-ttu-id="02980-202">Örneğin, Lori Penor Adventure Works'te genel müdürdür ve “Genel Müdür” pozisyonuna atanmıştır.</span><span class="sxs-lookup"><span data-stu-id="02980-202">For example, Lori Penor is a general manager at Adventure Works and is assigned to the “General Manager” position.</span></span> <span data-ttu-id="02980-203">Lori ıvır zıvır temizliğinde kullanılan bir ürünün geliştirilmesini yönetmektedir.</span><span class="sxs-lookup"><span data-stu-id="02980-203">Lori manages the development of a product that is used to clean widgets.</span></span> <span data-ttu-id="02980-204">Lori'nin ürünü geliştirmek için finans konusunda muhasebecinin yardımına ihtiyacı vardır.</span><span class="sxs-lookup"><span data-stu-id="02980-204">Lori requires an accountant to help with the finances for developing the product.</span></span> <span data-ttu-id="02980-205">Bu nedenle, Sanjay Patel'i muhasebeci olarak işe almıştır.</span><span class="sxs-lookup"><span data-stu-id="02980-205">Therefore, she has recruited Sanjay Patel to be the accountant.</span></span> <span data-ttu-id="02980-206">Sanjay, doğrudan Kim Akers'a rapor vermektedir, ancak ıvır zıvır temizleyicisi geliştirme çalışmasının finansmanı konusunda Lori Penor ile birlikte de çalışır.</span><span class="sxs-lookup"><span data-stu-id="02980-206">Sanjay reports directly to Kim Akers, but also works with Lori Penor on his work related to the finances for developing the widget cleaner.</span></span> 

<span data-ttu-id="02980-207">Önceki örnek için, Sanjay Patel ve Lori Penor arasında iş ilişkisi oluşturacak aşağıdaki görevleri tamamlarsınız:</span><span class="sxs-lookup"><span data-stu-id="02980-207">For the previous example, you would complete the following tasks to set up the working relationship between Sanjay Patel and Lori Penor:</span></span>
1.  <span data-ttu-id="02980-208">Ivır zıvır temizleme ürünü üzerinde çalışmaktan sorumlu olan pozisyonları içeren bir hiyerarşi yaratmak için "Ivır zıvır" adlı özel bir pozisyon hiyerarşisi türü oluşturun.</span><span class="sxs-lookup"><span data-stu-id="02980-208">Create a custom position hierarchy type called “Widget” to create a hierarchy that includes positions responsible for working on the widget cleaner product.</span></span>
2.  <span data-ttu-id="02980-209">Genel Müdür pozisyonunu Muhasebeci A pozisyonunun Ivır zıvır hiyerarşisinde rapor vereceği pozisyon olacak şekilde atayın.</span><span class="sxs-lookup"><span data-stu-id="02980-209">Assign the General Manager position to be the position that the Accountant-A position reports to in the Widget hierarchy.</span></span>

<span data-ttu-id="02980-210">Pozisyon hiyerarşisini kullanarak pozisyonların raporlama yapısını görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="02980-210">Use the position hierarchy to view the reporting structure of positions.</span></span> <span data-ttu-id="02980-211">Birden fazla pozisyon hiyerarşiniz varsa, pozisyon hiyerarşisindeki her bir hiyerarşi türü için hiyerarşileri görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="02980-211">If you have multiple position hierarchies, you can view the hierarchy for each hierarchy type in the position hierarchy.</span></span> <span data-ttu-id="02980-212">Ayrıca, bir pozisyonu pozisyon koduna veya o pozisyona atanan işçinin adına göre aratabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="02980-212">Also, you can search for a position by position ID or by the name of the worker who is assigned to the position.</span></span> <span data-ttu-id="02980-213">Pozisyon hiyerarşisi bir organizasyon hiyerarşisidir.</span><span class="sxs-lookup"><span data-stu-id="02980-213">The position hierarchy is an organizational hierarchy.</span></span>

## <a name="date-effective-records"></a><span data-ttu-id="02980-214">Yürürlüğe girme tarihi kayıtları</span><span class="sxs-lookup"><span data-stu-id="02980-214">Date effective records</span></span>
<span data-ttu-id="02980-215">Bazı kayıtlar için, kayda ileride yapılacak değişiklikleri belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="02980-215">For some records, you can specify future changes to the record.</span></span> <span data-ttu-id="02980-216">Aşağıdaki bilgilerin geçerliliği tarihe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="02980-216">The following information is date effective.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="02980-217">Kayıtlar</span><span class="sxs-lookup"><span data-stu-id="02980-217">Records</span></span></th>
<th><span data-ttu-id="02980-218">Geçerlilik tarihine sahip bilgiler</span><span class="sxs-lookup"><span data-stu-id="02980-218">Date effective information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="02980-219">İşler</span><span class="sxs-lookup"><span data-stu-id="02980-219">Jobs</span></span></td>
<td><ul>
<li><span data-ttu-id="02980-220">Bazı ayrıntılı iş bilgileri</span><span class="sxs-lookup"><span data-stu-id="02980-220">Some detailed job information</span></span></li>
<li><span data-ttu-id="02980-221">İş sınıflandırma bilgileri</span><span class="sxs-lookup"><span data-stu-id="02980-221">Job classification information</span></span></li>
<li><span data-ttu-id="02980-222">Maaş bilgileri</span><span class="sxs-lookup"><span data-stu-id="02980-222">Compensation information</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02980-223">Pozisyonlar</span><span class="sxs-lookup"><span data-stu-id="02980-223">Positions</span></span></td>
<td><ul>
<li><span data-ttu-id="02980-224">Bazı ayrıntılı pozisyon bilgileri</span><span class="sxs-lookup"><span data-stu-id="02980-224">Some detailed position information</span></span></li>
<li><span data-ttu-id="02980-225">Çalışan atamaları</span><span class="sxs-lookup"><span data-stu-id="02980-225">Worker assignments</span></span></li>
<li><span data-ttu-id="02980-226">Pozisyon süreleri</span><span class="sxs-lookup"><span data-stu-id="02980-226">Position durations</span></span></li>
<li><span data-ttu-id="02980-227">Pozisyon hiyerarşileri</span><span class="sxs-lookup"><span data-stu-id="02980-227">Position hierarchies</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="02980-228">Önceki tabloda sözü edilen bilgileri bir pozisyona veya işe yönelik olarak değiştirebilir ve pozisyon veya işe yapılan değişikliklerin ne zaman geçerlilik kazanacağını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="02980-228">You can modify the information mentioned in the previous table for a position or a job and specify a date when the modifications to the position or job should take effect.</span></span> <span data-ttu-id="02980-229">Örneğin, bir pozisyon yalnızca bir işçiye atanabilir ancak Muhasebe A pozisyonuna atanan Sanjay Patel iki hafta boyunca işte olmayacak.</span><span class="sxs-lookup"><span data-stu-id="02980-229">For example, a position can only be assigned to one worker, but Sanjay Patel, who is assigned to the position Accountant-A, will be leaving in two weeks.</span></span> <span data-ttu-id="02980-230">Sanjay Patel ayrıldığında, Sanjay'ın yerini Joe Healy alır.</span><span class="sxs-lookup"><span data-stu-id="02980-230">Joe Healy will replace Sanjay Patel when Sanjay leaves.</span></span> <span data-ttu-id="02980-231">Sanjay hala kendi pozisyona atanmış olsa da, Joe Healy'i atamanın ancak Sanjay'ın son gününden sonra geçerli olacağı şekilde aynı pozisyona atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="02980-231">Even though Sanjay is still assigned to his position, you can assign Joe Healy to the same position so that the assignment is effective only after Sanjay’s last day.</span></span>







[!INCLUDE[footer-include](../includes/footer-banner.md)]