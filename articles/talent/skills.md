---
title: "İşgücü yeteneklerini iş ihtiyaçlarıyla uyumlu hale getirme"
description: "Çalışanların, başvuranların veya ilgili kişilerin görevlerini etkili şekilde yerine getirmek için sahip olduğu veya sahip olması gereken yetenekleri izleyebilirsiniz. Ayrıca, belirli bir iş için gereken yetenekleri de belirtebilirsiniz."
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: edcb01c177a3e43cea7f0b7936a4129d27314016
ms.contentlocale: tr-tr
ms.lasthandoff: 01/19/2018

---

# <a name="align-workforce-skills-with-business-needs"></a><span data-ttu-id="a32f2-104">İşgücü yeteneklerini iş ihtiyaçlarıyla uyumlu hale getirme</span><span class="sxs-lookup"><span data-stu-id="a32f2-104">Align workforce skills with business needs</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="a32f2-105">Çalışanların, başvuranların veya ilgili kişilerin görevlerini etkili şekilde yerine getirmek için sahip olduğu veya sahip olması gereken yetenekleri izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a32f2-105">You can track the skills that workers, applicants, or contact persons have, or should have, to fulfill their roles effectively.</span></span> <span data-ttu-id="a32f2-106">Ayrıca, belirli bir iş için gereken yetenekleri de belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a32f2-106">You can also specify the skills that are required for a specific job.</span></span>

<span data-ttu-id="a32f2-107">İzleyebileceğiniz yetenek örnekleri aşağıda verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="a32f2-107">Examples of skills you can track include the following:</span></span>
-   <span data-ttu-id="a32f2-108">Gözetime yönelik – Diğerlerinin çalışmasını denetleme yeteneği.</span><span class="sxs-lookup"><span data-stu-id="a32f2-108">Supervisory – Ability to supervise the work of others.</span></span>
-   <span data-ttu-id="a32f2-109">Liderlik – Çalışanları ve iş alanlarını yönetme yeteneği.</span><span class="sxs-lookup"><span data-stu-id="a32f2-109">Leadership – Ability to lead employees and business domains.</span></span>
-   <span data-ttu-id="a32f2-110">Planlama - İleriyi görebilme, vizyonlar oluşturma ve bunları değerlendirme yeteneği.</span><span class="sxs-lookup"><span data-stu-id="a32f2-110">Planning – Ability to look ahead, to form visions, and to see them through.</span></span>
-   <span data-ttu-id="a32f2-111">HTML – HTML kodu yazabilme yeteneği.</span><span class="sxs-lookup"><span data-stu-id="a32f2-111">HTML – Ability to write HTML code.</span></span>

<span data-ttu-id="a32f2-112">Bir kişiye veya işe bir yetenek atayabilmek, bir yetenek eşleme araması ya da bir yetenek profili oluşturabilmek için, **Yetenekler** sayfasında yeteneklerle ilgili bilgileri girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="a32f2-112">Before you can assign a skill to a person or a job, create a skill-mapping search, or create a skill profile, you must enter information about the skills on the **Skills** page.</span></span> <span data-ttu-id="a32f2-113">Her bir yetenek için yetenek türünü ve değerlendirme modelini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a32f2-113">For each skill, you can select a skill type and a rating model.</span></span>

## <a name="rating-models"></a><span data-ttu-id="a32f2-114">Değerlendirme modelleri</span><span class="sxs-lookup"><span data-stu-id="a32f2-114">Rating models</span></span>
<span data-ttu-id="a32f2-115">Değerlendirme modelleri bir kişinin gerçek yetenek düzeyini, elde etmek için çalışmaları gereken düzeyi veya iş için gerekli olan yetenek düzeyini değerlendirmenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="a32f2-115">Rating models help evaluate a person's actual level of skill, the level they should work to achieve, or the level of skill that is required for a job.</span></span> <span data-ttu-id="a32f2-116">Bir derecelendirme modeli için en fazla 10 düzey girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a32f2-116">You can enter up to 10 levels for a rating model.</span></span>  <span data-ttu-id="a32f2-117">Derecelendirme modelindeki her düzeye bir faktör atanır.</span><span class="sxs-lookup"><span data-stu-id="a32f2-117">Each level in a rating model is assigned a factor.</span></span>  <span data-ttu-id="a32f2-118">Faktör değeri, farklı değerlendirme modelleri kullanılan yetenek skorlarını normalleştirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a32f2-118">The factor value will be used to normalize the scores of skills that use different rating models.</span></span>  <span data-ttu-id="a32f2-119">Faktörün 0-9 arasında bir numarası ve her düzeyin benzersiz bir faktörü olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a32f2-119">The factor must be a number between 0-9 and each level must have a unique factor.</span></span>  <span data-ttu-id="a32f2-120">Faktör değerleri yüksek düzeyler bir derecelendirme modelinde daha fazla ağırlık taşır.</span><span class="sxs-lookup"><span data-stu-id="a32f2-120">Levels with higher factor values carry more weight in a rating model.</span></span>

## <a name="specify-job-skills"></a><span data-ttu-id="a32f2-121"> İş yeteneklerini belirtme</span><span class="sxs-lookup"><span data-stu-id="a32f2-121">Specify job skills</span></span>
<span data-ttu-id="a32f2-122">Bir iş hakkındaki bilgileri girerken, bir kişinin o işte gereken çalışmayı yapması için sahip olması gereken yetenekleri belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a32f2-122">When you enter information about a job, you can specify the skills that a person should have to perform the work required for the job.</span></span>  <span data-ttu-id="a32f2-123">Ayrıca, istenen her yetenek için istenen düzeyi ve o yeteneğin önem düzeyini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a32f2-123">In addition you can specify the desired level for each skill as well the level of importance of the skill.</span></span> <span data-ttu-id="a32f2-124">Farklı işler, aynı yeteneğin farklı düzeylerini gerektirebilir.</span><span class="sxs-lookup"><span data-stu-id="a32f2-124">Different jobs can require different levels of importance for the same skill.</span></span>

## <a name="enter-skills-for-workers-applicants-or-contacts"></a><span data-ttu-id="a32f2-125"> Çalışanlar, başvuranlar veya ilgili kişiler için yetenekleri girme</span><span class="sxs-lookup"><span data-stu-id="a32f2-125">Enter skills for workers, applicants, or contacts</span></span>
<span data-ttu-id="a32f2-126">Çalışanlar, başvuranlar veya ilgili kişiler için hedef yetenekler veya gerçek yetenekler girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a32f2-126">You can enter target skills or actual skills for workers, applicants, or contacts.</span></span> <span data-ttu-id="a32f2-127">Hedef yetenek, bir kişinin elde etmeyi planladığı yetenektir.</span><span class="sxs-lookup"><span data-stu-id="a32f2-127">A target skill is a skill that a person plans to achieve.</span></span> <span data-ttu-id="a32f2-128">Gerçek yetenek, bir kişinin sahip olduğu yetenektir.</span><span class="sxs-lookup"><span data-stu-id="a32f2-128">An actual skill is a skill that a person currently has.</span></span>

## <a name="skill-mapping-and-skill-mapping-profiles"></a><span data-ttu-id="a32f2-129"> Yetenek eşleme ve Yetenek eşleme profilleri</span><span class="sxs-lookup"><span data-stu-id="a32f2-129">Skill mapping and Skill mapping profiles</span></span>
<span data-ttu-id="a32f2-130">Belirli türde bir görevi yerine getirmeye uygun nitelikte bir işçi, başvuru sahibi veya ilgili kişi bulmak için bir yetenek eşleştirme araması oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a32f2-130">You can create a skill-mapping search to find a worker, applicant, or contact person who is qualified to perform a specific type of task.</span></span> <span data-ttu-id="a32f2-131">Yetenek eşleştirme aramaları yetenekleri, eğitimi, sertifikaları, güven gerektiren pozisyonları ve proje deneyimini arayıp, girilen ölçütlere uyan sonuçları döndürür.</span><span class="sxs-lookup"><span data-stu-id="a32f2-131">Skill-mapping searches look across skills, education, certificates, positions of trust and project experience and return results that match the criteria entered.</span></span>  <span data-ttu-id="a32f2-132">Örneğin, kuruluşunuzda hangi çalışanların CPA kazandığını bilmek yararlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="a32f2-132">For example, it might be useful to know which workers in your organization earned their CPA.</span></span>

<span data-ttu-id="a32f2-133">Yetenek eşleştirme profilleri, iş gereksinimlerine doğrudan karşılık gelen nitelikleri taşıyan mevcut çalışanları veya adayları bulmanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="a32f2-133">Skill-mapping profiles allow you to find current employees or candidates with qualifications that directly correspond to business needs.</span></span>  <span data-ttu-id="a32f2-134">Örneğin, kuruluşunuzdaki bir açık pozisyon için yetenek eşleştirme profili oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a32f2-134">For example, you could create a skill-mapping profile for an open position in your organization.</span></span> <span data-ttu-id="a32f2-135">Belirli bir iş için bir profil oluşturarak ve o işteki yetenekleri, eğitimi ve sertifikaları profile kopyalayarak profilde girilen bir veya daha fazla ölçüte uyan çalışanları, başvuranları ve ilgili kişileri hızlıca arayabilir ve bir iş için gereken yeteneklere en uygun adayların listesini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a32f2-135">By creating a profile for a particular job and copying the skills, education and certificates from that job to the profile, you can quickly search workers, applicants and contact persons who match one or more of the criteria entered on the profile and view a list of the candidates whose skills most closely match the skills required for the job.</span></span>

><span data-ttu-id="a32f2-136">**Not** Yalnızca yetenek eşleme aramalarına eklenmek üzere seçilen çalışanlar, başvuranlar ve ilgili kişiler bir yetenek eşleme sonuçları listesinde görüntülenebilir ya da yetenek profiline eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="a32f2-136">**Note** Only workers, applicants, and contact persons who are selected to be included in skill mapping searches can be displayed in a skill-mapping results list, or included in a skill profile.</span></span> <span data-ttu-id="a32f2-137">Yetenek eşleme aramalarına bir çalışan, başvuran veya ilgili kişi eklemek için **Yetenek eşlemeye dahil et** seçimini aşağıdaki sayfalarda Evet olarak ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="a32f2-137">To include a worker, applicant, or contact person in skill mapping searches, set the **Include in skill mapping** selection to Yes in the following pages:</span></span>

> + <span data-ttu-id="a32f2-138">Çalışan</span><span class="sxs-lookup"><span data-stu-id="a32f2-138">Worker</span></span>
> + <span data-ttu-id="a32f2-139">Çalışan</span><span class="sxs-lookup"><span data-stu-id="a32f2-139">Employee</span></span>
> + <span data-ttu-id="a32f2-140">Başvuran</span><span class="sxs-lookup"><span data-stu-id="a32f2-140">Applicant</span></span>
> + <span data-ttu-id="a32f2-141">İlgili kişiler</span><span class="sxs-lookup"><span data-stu-id="a32f2-141">Contacts</span></span>

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a><span data-ttu-id="a32f2-142"> Yetenek eksikliği analizi ve yetenek profili analizi</span><span class="sxs-lookup"><span data-stu-id="a32f2-142">Skill gap analysis and skill profile analysis</span></span>
<span data-ttu-id="a32f2-143">Bir çalışan, başvuran veya ilgili kişinin belirli bir tarih itibariyle sahip olduğu yetkinliklerin listesini görmek için bir yetenek profili analizi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a32f2-143">You can create a skill profile analysis to view a list of the competencies of a worker, applicant, or contact person as of a specific date.</span></span> <span data-ttu-id="a32f2-144">Bir kişinin yeteneklerini ve belirli bir iş için gereken yetenekleri karşılaştırmak için bir yetenek eksikliği analizi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a32f2-144">You can create a skill gap analysis to compare a person’s skills and the skills that are required for a specific job.</span></span>  



<a name="see-also"></a><span data-ttu-id="a32f2-145">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="a32f2-145">See also</span></span>
--------

[<span data-ttu-id="a32f2-146">İnsan kaynakları</span><span class="sxs-lookup"><span data-stu-id="a32f2-146">Human resources</span></span>](index.md)




