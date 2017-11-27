---
title: "Bir işin bileşenlerini ayarlamak"
description: "Bu konu, bir işin içerebileceği konsept öğelerini açıklar ve bu öğeleri kuruluşunuzda nasıl kullanabileceğiniz hakkında örnekler sağlar."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle
audience: Application User
ms.author: rschloma
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Retail
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 962b3084c5340813d1697cab680621350510d4b9
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="setting-up-the-components-of-a-job"></a><span data-ttu-id="e7fd4-103">Bir işin bileşenlerini ayarlamak</span><span class="sxs-lookup"><span data-stu-id="e7fd4-103">Setting up the components of a job</span></span>

[!include[banner](includes/banner.md)]

[!include[retail name](includes/retail-name.md)]


<span data-ttu-id="e7fd4-104">Bu konu, bir işin içerebileceği konsept öğelerini açıklar ve bu öğeleri kuruluşunuzda nasıl kullanabileceğiniz hakkında örnekler sağlar.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-104">This topic describes the conceptual elements that a job can include and provides examples of how you can use those elements in your organization.</span></span> 

<span data-ttu-id="e7fd4-105">Yeni işler oluşturabilmeden önce, bazı referans bilgileri ayarlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-105">Before you can create jobs, you must set up some reference information.</span></span> <span data-ttu-id="e7fd4-106">Sadece bir isme sahip bir iş oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-106">You can create a job that has only a name.</span></span> <span data-ttu-id="e7fd4-107">Ancak, örneğin bir iş unvanı gibi ek bilgiler ekleyerek, işe atanmış olan konumlara varsayılan değerler sağlarsınız.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-107">However, by including additional information, such as a job title, you provide default values for the positions that are assigned to the job.</span></span> <span data-ttu-id="e7fd4-108">Ek olarak, girdiğiniz bazı bilgiler maaş planlarını belirli işlere filtrelemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-108">Additionally, some of the information that you enter can be used to filter compensation plans to specific jobs.</span></span> <span data-ttu-id="e7fd4-109">Maaş planlarını belirli bir işe filtrelemek için uygunluk ayarlamak istiyorsanız, iş işlevleri ve iş görevlerini, işleri ayarlamadan önce ayarlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-109">If you want to set up eligibility that you can use to filter compensation plans to a specific job, you should set up job functions and job types before you set up jobs.</span></span> <span data-ttu-id="e7fd4-110">Bu varsayılan değerleri mevcut bulundurarak, işe konumlar eklerken zaman kazanırsınız.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-110">By having these default values available, you will save time when you add positions to the job.</span></span> 

<span data-ttu-id="e7fd4-111">Bazı iş ayrıntıları, örneğin iş unvanı, türü ve işlevi, yürürlük tarihine sahiptir.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-111">Some job details, such as the job title, type, and function, are date-effective.</span></span> <span data-ttu-id="e7fd4-112">Bugün bir iş oluşturursanız ancak bunları daha sonra bu ayrıntıları eklemezseniz ve daha sonra işe oluşturulma tarihinde bakarsanız, bu ayrıntılar görüntülenmez.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-112">If you create a job today but don't add these details until later, and you then look at the job as of the creation date, these details won't appear.</span></span> <span data-ttu-id="e7fd4-113">Bu nedenle, bu başvuru bilgilerinin bazılarını, ihtiyaç duymadan oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-113">Therefore, you should create some of this reference information before you require it.</span></span> <span data-ttu-id="e7fd4-114">Bu sayede, yeni işlere bilgileri, onları oluştururken ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-114">That way, you can add the information to new jobs when you create them.</span></span>

## <a name="job-titles"></a><span data-ttu-id="e7fd4-115">İş başlıkları</span><span class="sxs-lookup"><span data-stu-id="e7fd4-115">Job titles</span></span>
<span data-ttu-id="e7fd4-116">İşler oluşturmadan önce, bu işler için unvanlar ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-116">Before you create jobs, you must set up titles for those jobs.</span></span> <span data-ttu-id="e7fd4-117">Pozisyonlar, iş unvanlarını, pozisyonların ilişkili olduğu işlerden devralır.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-117">Positions inherit job titles from the jobs that the positions are associated with.</span></span> 

<span data-ttu-id="e7fd4-118">Arama özelliğini kullanarak açabileceğiniz **Unvanlar** sayfasını kullanarak iş unvanlarını korumak.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-118">Maintain job titles using the **Titles** page, which you can open by using the Search function.</span></span> <span data-ttu-id="e7fd4-119">**Unvanlar **sayfasında, işlerinizde kullanmayı planladığınız unvanları girin.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-119">On the **Titles **page, enter the titles that you plan to use for your jobs.</span></span>

## <a name="job-types"></a><span data-ttu-id="e7fd4-120">İş tipleri</span><span class="sxs-lookup"><span data-stu-id="e7fd4-120">Job types</span></span>
<span data-ttu-id="e7fd4-121">Benzer işleri kategorilere gruplamak için iş türlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-121">You use job types to group similar jobs into categories.</span></span> <span data-ttu-id="e7fd4-122">İş türleri, zorunlu değildir.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-122">Job types aren't required.</span></span> <span data-ttu-id="e7fd4-123">Ancak, maaş yönetimi için uygunluk kuralları oluşturduğunuzda iş türlerini kullanmayı planlıyorsanız, işleri ayarlamadan önce iş tiplerini ayarlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-123">However, if you plan to use job types when you set up eligibility rules for compensation management, you should set up job types before you set up jobs.</span></span> <span data-ttu-id="e7fd4-124">İş türlerine bazı örnekler tam zamanlı ve yarı zamanlı veya maaşlı ve saatlik ödemelidir.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-124">Some examples of job types are full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="e7fd4-125">**İş türleri** sayfasını kullanarak iş türlerini yönetirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-125">You maintain job types by using the **Job types** page.</span></span> <span data-ttu-id="e7fd4-126">**İş türleri** sayfası üzerinde, iş türü için kısa bir açıklama ve ad girin.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-126">On the **Job types** page, enter a name and a brief description for the job type.</span></span> <span data-ttu-id="e7fd4-127">**Muaf durumu** alanında, Adil İş Standartları Yasası (FLSA) muafiyet durumunu, şu iş durumuna sahip işler için belirtmek üzere aşağıdaki seçeneklerden birini işaretleyin:</span><span class="sxs-lookup"><span data-stu-id="e7fd4-127">In the **Exempt status** field, select one of the following options to indicate the Fair Labor Standards Act (FLSA) exempt status of jobs that have this job type:</span></span>

-   <span data-ttu-id="e7fd4-128">**Muafiyet** – İşler, FLSA kapsamı altında fazla mesai dışında tutulurlar.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-128">**Exempt** – Jobs are exempt from overtime under the FLSA.</span></span>
-   <span data-ttu-id="e7fd4-129">**Muaf olmayan** – İşler, FLSA kapsamı altında fazla mesai dışında tutulmaz.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-129">**Non-exempt** – Jobs aren't exempt from overtime under the FLSA.</span></span>
-   <span data-ttu-id="e7fd4-130">**Geçerli değildir** – FLSA kapsamı için geçerli değildir.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-130">**Does not apply** – FLSA coverage isn't applicable.</span></span>

## <a name="job-functions"></a><span data-ttu-id="e7fd4-131">İş işlevleri</span><span class="sxs-lookup"><span data-stu-id="e7fd4-131">Job functions</span></span>
<span data-ttu-id="e7fd4-132">İş işlevleri, yüksek seviye işlevsellik kategorileri açıklar ve yüksek düzey görevleri ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-132">Job junctions describe high-level functional categories and relate high-level duties.</span></span> <span data-ttu-id="e7fd4-133">İş işlevleri, zorunlu değildir.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-133">Job functions aren't required.</span></span> <span data-ttu-id="e7fd4-134">Tazminat planlarını belirli işlere göre filtrelemek için iş işlevlerini iş tipleriyle birlikte kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-134">You can use job functions, together with job types, to filter compensation plans to specific jobs.</span></span> <span data-ttu-id="e7fd4-135">**Uygunluk kuralları** sayfasında uygunluk kuralları oluşturarak iş işlevlerini ve iş türlerini, maaş planları ile ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-135">You associate job functions and job types with compensation plans by setting up eligibility rules on the **Eligibility rules** page.</span></span> <span data-ttu-id="e7fd4-136">Bir uygunluk kuralı aracılığıyla tanımlamış olduğunuz belirli bir iş türü ve iş işlevine uygulanacak bir diz seviyeyi bir ücret planına iliştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-136">You can then attach a set of levels to a compensation plan that apply to the specific combination of a job type and job function that you've defined through an eligibility rule.</span></span> <span data-ttu-id="e7fd4-137">(Bu özellikler hem sabit maaş planları hem de değişken maaş planları için geçerlidir.) Ancak, maaş yönetimi için uygunluk kuralları oluşturduğunuzda iş işlevlerini kullanmayı planlıyorsanız, işleri ayarlamadan önce iş işlevlerini ayarlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-137">(These features apply to both fixed compensation plans and variable compensation plans.) However, if you plan to use job functions when you set up eligibility rules for compensation management, you should set up job functions before you set up jobs.</span></span> <span data-ttu-id="e7fd4-138">Aşağıdaki tablo iş işlevlerine bazı örnekleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-138">The following table shows some examples of job functions.</span></span>

| <span data-ttu-id="e7fd4-139">İş</span><span class="sxs-lookup"><span data-stu-id="e7fd4-139">Job</span></span>           | <span data-ttu-id="e7fd4-140">İş işlevi</span><span class="sxs-lookup"><span data-stu-id="e7fd4-140">Job function</span></span>         |
|---------------|----------------------|
| <span data-ttu-id="e7fd4-141">Satış yöneticisi</span><span class="sxs-lookup"><span data-stu-id="e7fd4-141">Sales manager</span></span> | <span data-ttu-id="e7fd4-142">Orta düzey Yönetici</span><span class="sxs-lookup"><span data-stu-id="e7fd4-142">Mid-level Manager</span></span>    |
| <span data-ttu-id="e7fd4-143">Muhasebeci</span><span class="sxs-lookup"><span data-stu-id="e7fd4-143">Accountant</span></span>    | <span data-ttu-id="e7fd4-144">Profesyoneller</span><span class="sxs-lookup"><span data-stu-id="e7fd4-144">Professionals</span></span>        |

<span data-ttu-id="e7fd4-145">İş işlevlerini, **İş işlevleri** sayfasını kullanarak yönetirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-145">You maintain job functions by using the **Job functions** page.</span></span> <span data-ttu-id="e7fd4-146">**İş işlevleri** sayfası üzerinde, bir kimlik saptama kodu ve iş işlevi için kısa bir açıklama girersiniz.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-146">On the **Job functions** page, enter an identification code and a brief description for the job function.</span></span>

## <a name="job-tasks"></a><span data-ttu-id="e7fd4-147">İş görevleri</span><span class="sxs-lookup"><span data-stu-id="e7fd4-147">Job tasks</span></span>
<span data-ttu-id="e7fd4-148">İş görevleri, bir iş için bir konumda olan bir çalışanın tamamlaması gereken temel görevleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-148">Job tasks describe the basic tasks that a worker who is in a position for a job must complete.</span></span> <span data-ttu-id="e7fd4-149">Aynı iş görevi, birden fazla işe ve bu iş görevlerini kullanan iş pozisyonlarına eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-149">The same job task can be added to multiple jobs, and to positions for the jobs that use those job tasks.</span></span> <span data-ttu-id="e7fd4-150">Aşağıdaki tablo iş görevlerinin bazı örneklerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-150">The following table shows some examples of job tasks.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e7fd4-151">İş</span><span class="sxs-lookup"><span data-stu-id="e7fd4-151">Job</span></span></th>
<th><span data-ttu-id="e7fd4-152">İş görevi</span><span class="sxs-lookup"><span data-stu-id="e7fd4-152">Job task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e7fd4-153">Satış yöneticisi</span><span class="sxs-lookup"><span data-stu-id="e7fd4-153">Sales manager</span></span></td>
<td><ul>
<li><span data-ttu-id="e7fd4-154"><strong>Perf-review</strong> – Her bir satış personelinin performansını gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-154"><strong>Perf-review</strong> – Review each salesperson's job performance.</span></span></li>
<li><span data-ttu-id="e7fd4-155"><strong>Abs-review</strong> – Her bir satış personelinin devamsızlık taleplerini veya kayıtlarını onaylayın veya reddedin.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-155"><strong>Abs-review</strong> – Approve or reject each salesperson's absence requests or registrations.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e7fd4-156">Muhasebeci</span><span class="sxs-lookup"><span data-stu-id="e7fd4-156">Accountant</span></span></td>
<td><span data-ttu-id="e7fd4-157"><strong>FIN-Report</strong> – Finans müdürüne haftalık mali raporlar sunun.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-157"><strong>FIN-Report</strong> – Present weekly financial reports to the chief financial officer.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e7fd4-158">**İş görevleri** sayfasını kullanarak iş görevlerini yönetirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-158">You maintain job tasks by using the **Job tasks** page.</span></span> <span data-ttu-id="e7fd4-159">**İş görevleri** sayfası üzerinde, iş görevi için kısa bir açıklama ve ad girin.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-159">On the **Job tasks** page, enter a name and description for the job task.</span></span> <span data-ttu-id="e7fd4-160">İsteğe bağlı olarak **Not** alanında ek bilgiler girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-160">In the **Note** field, you can optionally enter additional information.</span></span> <span data-ttu-id="e7fd4-161">Belirli bir iş için notlar, burada girmiş olduğunuz notları değiştirmeden güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-161">The notes can be updated for a specific job without changing the notes that you entered here.</span></span>

## <a name="areas-of-responsibility"></a><span data-ttu-id="e7fd4-162">Sorumluluk alanları</span><span class="sxs-lookup"><span data-stu-id="e7fd4-162">Areas of responsibility</span></span>
<span data-ttu-id="e7fd4-163">Bir pozisyondaki çalışanın o iş için sorumlu olacağı iş rollerini, süreçleri ve ürünleri belirtmek üzere sorumluluk alanlarını kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-163">You use areas of responsibility to indicate the work roles, processes, and products that a worker who is in a position for a job is responsible for.</span></span> <span data-ttu-id="e7fd4-164">Örneğin, "Muhasebeci" olarak adlandırılan bir iş için, sorumluluk alanlarından biri "Ürün A için mali raporlama" olabilir.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-164">For example, for a job that is named "Accountant," one area of responsibility might be "Financial reporting for product A."</span></span> <span data-ttu-id="e7fd4-165">Arama işlevi ile bulabileceğiniz **Sorumluluk alanları** sayfasını kullanarak sorumluluk alanlarını yönetirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-165">You maintain areas of responsibility by using the **Areas of responsibility** page, which you can find by using the Search function.</span></span> <span data-ttu-id="e7fd4-166">**Sorumluluk alanları** sayfasında, sorumluluk için bir isim ve açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-166">On the **Areas of responsibility** page, enter a name and description for the responsibility.</span></span> <span data-ttu-id="e7fd4-167">İsteğe bağlı olarak **Not** alanında ek bilgiler girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-167">In the **Note** field, you can optionally enter additional information.</span></span> <span data-ttu-id="e7fd4-168">Belirli bir iş için notlar, burada girmiş olduğunuz notları değiştirmeden güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="e7fd4-168">The notes can be updated for a specific job without changing the notes that you entered here.</span></span>




