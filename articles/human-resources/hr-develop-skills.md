---
title: Yetenekleri konfigüre et
description: Çalışanlarınızın yeteneklerini Dynamics 365 Human Resources'ta izleyebilirsiniz. Ayrıca, belirli bir iş için gereken yetenekleri de belirtebilirsiniz.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 816822d1f3d365b4c5571c13e9f596e1c5d5e59c
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076571"
---
# <a name="configure-skills"></a><span data-ttu-id="609e9-104">Yetenekleri konfigüre et</span><span class="sxs-lookup"><span data-stu-id="609e9-104">Configure skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="609e9-105">Çalışanlarınızın yeteneklerini Dynamics 365 Human Resources'ta izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="609e9-105">You can track your worker's skills in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="609e9-106">Ayrıca, belirli bir iş için gereken yetenekleri de belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="609e9-106">You can also specify the skills that are required for a specific job.</span></span>

<span data-ttu-id="609e9-107">İzleyebileceğiniz yetenek örnekleri verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="609e9-107">Examples of skills you can track include:</span></span>

- <span data-ttu-id="609e9-108">Gözetime yönelik – Diğerlerinin çalışmasını denetleme yeteneği.</span><span class="sxs-lookup"><span data-stu-id="609e9-108">Supervisory – Ability to supervise the work of others.</span></span>
- <span data-ttu-id="609e9-109">Liderlik – Çalışanları ve iş alanlarını yönetme yeteneği.</span><span class="sxs-lookup"><span data-stu-id="609e9-109">Leadership – Ability to lead employees and business domains.</span></span>
- <span data-ttu-id="609e9-110">Planlama - İleriyi görebilme, vizyon deyimleri oluşturma ve bunları değerlendirme yeteneği.</span><span class="sxs-lookup"><span data-stu-id="609e9-110">Planning – Ability to look ahead, to form vision statements, and to see them through.</span></span>
- <span data-ttu-id="609e9-111">HTML – HTML kodu yazabilme yeteneği.</span><span class="sxs-lookup"><span data-stu-id="609e9-111">HTML – Ability to write HTML code.</span></span>

<span data-ttu-id="609e9-112">Yetenek tiplerini ve derecelendirme modellerini henüz ayarlamadıysanız, yetenek oluşturmadan önce bir miktar eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="609e9-112">If you haven't already set up skill types and rating models, you'll need to add some before creating skills.</span></span>

<span data-ttu-id="609e9-113">Aşağıdaki kişiler bir çalışan için yetenek girebilecek:</span><span class="sxs-lookup"><span data-stu-id="609e9-113">The following people can enter skills for a worker:</span></span>

- <span data-ttu-id="609e9-114">Çalışanlar self servise kendileri için yetenekler girebilecek.</span><span class="sxs-lookup"><span data-stu-id="609e9-114">Workers can enter skills for themselves in Employee self-service.</span></span> <span data-ttu-id="609e9-115">Bu yetenekler için yönetici onayı gereklidir.</span><span class="sxs-lookup"><span data-stu-id="609e9-115">These skills require manager approval.</span></span>
- <span data-ttu-id="609e9-116">Yöneticiler, çalışanları için yetenekler girebilirler.</span><span class="sxs-lookup"><span data-stu-id="609e9-116">Managers can enter skills for their workers.</span></span> <span data-ttu-id="609e9-117">Bu becerileri otomatik olarak onaylayan bir iş akışı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="609e9-117">You can create a workflow that auto-approves these skills.</span></span>

## <a name="create-a-skill-type"></a><span data-ttu-id="609e9-118">Beceri türü oluşturma</span><span class="sxs-lookup"><span data-stu-id="609e9-118">Create a skill type</span></span>

<span data-ttu-id="609e9-119">Yetenek tipleri yönetim veya satışlar gibi bireysel yeteneklerin altında kalan kategorilerlerdir.</span><span class="sxs-lookup"><span data-stu-id="609e9-119">Skill types are categories that individual skills fall under, such as Administration or Sales.</span></span>

1. <span data-ttu-id="609e9-120">**Çalışan geliştirme** çalışma alanında, **Bağlantılar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="609e9-120">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="609e9-121">**Yetki kurulumu** altında **Yetenek tipleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="609e9-121">Under **Competency setup**, select **Skill types**.</span></span>

3. <span data-ttu-id="609e9-122">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="609e9-122">Select **New**.</span></span>

4. <span data-ttu-id="609e9-123">Ardından aşağıdaki alanları tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="609e9-123">Complete the following fields:</span></span>

   - <span data-ttu-id="609e9-124">**Beceri türü**: Beceri türü için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="609e9-124">**Skill type**: Enter a name for the skill type.</span></span>
   - <span data-ttu-id="609e9-125">**Açıklama**: Beceri türü için bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="609e9-125">**Description**: Enter a description for the skill type.</span></span>

5. <span data-ttu-id="609e9-126">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="609e9-126">Select **Save**.</span></span>

## <a name="create-a-rating-model"></a><span data-ttu-id="609e9-127">Derecelendirme modeli oluşturma</span><span class="sxs-lookup"><span data-stu-id="609e9-127">Create a rating model</span></span>

<span data-ttu-id="609e9-128">Değerlendirme modelleri bir kişinin gerçek yetenek düzeyini, elde etmek için çalışmaları gereken düzeyi veya iş için gerekli olan yetenek düzeyini değerlendirmenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="609e9-128">Rating models help evaluate a person's actual level of skill, the level they should work to achieve, or the level of skill required for a job.</span></span> <span data-ttu-id="609e9-129">Derecelendirme modelindeki her düzeye bir faktör atanır.</span><span class="sxs-lookup"><span data-stu-id="609e9-129">Each level in a rating model is assigned a factor.</span></span>

1. <span data-ttu-id="609e9-130">**Çalışan geliştirme** çalışma alanında, **Bağlantılar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="609e9-130">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="609e9-131">**Yetki kurulumu** altında, **değerlendirme modelleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="609e9-131">Under **Competency setup**, select **Rating models**.</span></span>

3. <span data-ttu-id="609e9-132">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="609e9-132">Select **New**.</span></span>

4. <span data-ttu-id="609e9-133">Ardından aşağıdaki alanları tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="609e9-133">Complete the following fields:</span></span>

   - <span data-ttu-id="609e9-134">**Derecelendirme**: değerlendirme modeli için **yetenekler** gibi bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="609e9-134">**Rating**: Enter a name for the rating model, such as **Skills**.</span></span>
   - <span data-ttu-id="609e9-135">**Açıklama**: **Yetenek derecelendirmeleri** gibi bir değerlendirme modeli açıklaması girin.</span><span class="sxs-lookup"><span data-stu-id="609e9-135">**Description**: Enter a description for the rating model, such as **Skill ratings**.</span></span>

5. <span data-ttu-id="609e9-136">**Düzeyler** bölümünde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="609e9-136">In the **Levels** section, select **New**.</span></span> <span data-ttu-id="609e9-137">Eklemek istediğiniz her düzey için, aşağıdaki alanları tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="609e9-137">For each level you want to add, complete the following fields:</span></span>

   - <span data-ttu-id="609e9-138">**Düzey**: Düzey için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="609e9-138">**Level**: Enter a name for the level.</span></span>
   - <span data-ttu-id="609e9-139">**Açıklama**: Düzey için bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="609e9-139">**Description**: Enter a description for the level.</span></span>
   - <span data-ttu-id="609e9-140">**Faktör**: 0-9 bir faktör değeri girin.</span><span class="sxs-lookup"><span data-stu-id="609e9-140">**Factor**: Enter a factor value from 0-9.</span></span> <span data-ttu-id="609e9-141">Faktörlr, farklı değerlendirme modelleri kullanılan yetenek skorlarını normalleştirmeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="609e9-141">Factors help normalize the scores of skills that use different rating models.</span></span> <span data-ttu-id="609e9-142">Her düzey benzersiz bir etmenle sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="609e9-142">Each level must have a unique factor.</span></span> <span data-ttu-id="609e9-143">Faktör değerleri yüksek düzeyler bir derecelendirme modelinde daha fazla ağırlık taşır.</span><span class="sxs-lookup"><span data-stu-id="609e9-143">Levels with higher factor values carry more weight in a rating model.</span></span>

   <span data-ttu-id="609e9-144">Gerektiğinde düzeyler eklemeye devam edin.</span><span class="sxs-lookup"><span data-stu-id="609e9-144">Continue adding levels as necessary.</span></span> <span data-ttu-id="609e9-145">Bir derecelendirme modeli için en fazla 10 düzey girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="609e9-145">You can enter up to 10 levels for each rating model.</span></span>

6. <span data-ttu-id="609e9-146">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="609e9-146">Select **Save**.</span></span>

## <a name="create-a-skill"></a><span data-ttu-id="609e9-147">Beceri oluşturma</span><span class="sxs-lookup"><span data-stu-id="609e9-147">Create a skill</span></span>

<span data-ttu-id="609e9-148">Bir kişiye veya işe bir yetenek atayabilmek, bir yetenek eşleme araması ya da bir yetenek profili oluşturabilmek için, **Yetenekler** sayfasında yeteneklerle ilgili bilgileri girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="609e9-148">Before you can assign a skill, or create a skill-mapping search or skill profile, you must enter information about the skills on the **Skills** page.</span></span> <span data-ttu-id="609e9-149">Her bir yetenek için yetenek türünü ve değerlendirme modelini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="609e9-149">For each skill, you can select a skill type and a rating model.</span></span>

1. <span data-ttu-id="609e9-150">**Çalışan geliştirme** çalışma alanında, **Bağlantılar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="609e9-150">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="609e9-151">**Yetki kurulumu** altında **Yetenekler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="609e9-151">Under **Competency setup**, select **Skills**.</span></span>

3. <span data-ttu-id="609e9-152">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="609e9-152">Select **New**.</span></span>

4. <span data-ttu-id="609e9-153">Ardından aşağıdaki alanları tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="609e9-153">Complete the following fields:</span></span>

   - <span data-ttu-id="609e9-154">**Beceri**: Beceri için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="609e9-154">**Skill**: Enter a name for the skill.</span></span>
   - <span data-ttu-id="609e9-155">**Açıklama**: Beceri için bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="609e9-155">**Description**: Enter a description for the skill.</span></span>
   - <span data-ttu-id="609e9-156">**Derecelendirme**: Bu beceri için kullanmak istediğiniz derecelendirme modelini seçin.</span><span class="sxs-lookup"><span data-stu-id="609e9-156">**Rating**: Select the rating model you want to use for this skill.</span></span>
   - <span data-ttu-id="609e9-157">**Yetenek türü**: Yetenek tipleri listesinden seçim yapın.</span><span class="sxs-lookup"><span data-stu-id="609e9-157">**Skill type**: Select from the list of skill types.</span></span>

5. <span data-ttu-id="609e9-158">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="609e9-158">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="609e9-159">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="609e9-159">See also</span></span>

[<span data-ttu-id="609e9-160">Yetenekleri girin</span><span class="sxs-lookup"><span data-stu-id="609e9-160">Enter skills</span></span>](hr-develop-enter-skills.md)<br>
[<span data-ttu-id="609e9-161">Becerileri eşleştirme</span><span class="sxs-lookup"><span data-stu-id="609e9-161">Map skills</span></span>](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]