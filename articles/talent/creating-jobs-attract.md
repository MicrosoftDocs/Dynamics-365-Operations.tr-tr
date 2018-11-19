---
title: "Attract'ta iş oluşturun, onaylayın ve yayınlayın"
description: "Bu konu, Attract'taki bir işin öğelerini açıklar. Bu aynı zamanda bir iş oluşturmayı açıklar."
author: josaw
manager: AnnBe
ms.date: 10/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: 
ms.author: josaw
ms.search.validFrom: 2018-10-24
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: 2fc6bf25d303d7d8de8002a923a080b90dcfbeab
ms.openlocfilehash: af945042c150fff1a95cdb046f2a712cb2c2c061
ms.contentlocale: tr-tr
ms.lasthandoff: 10/24/2018

---

# <a name="create-approve-and-post-jobs-in-attract"></a><span data-ttu-id="4ee07-104">Attract'ta iş oluşturun, onaylayın ve yayınlayın</span><span class="sxs-lookup"><span data-stu-id="4ee07-104">Create, approve, and post jobs in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4ee07-105">Bu konu, Microsoft Dynamics 365 for Talent: Attract'taki bir işin öğelerini açıklar.</span><span class="sxs-lookup"><span data-stu-id="4ee07-105">This topic describes the elements of a job in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="4ee07-106">Bu aynı zamanda bir iş oluşturmayı açıklar.</span><span class="sxs-lookup"><span data-stu-id="4ee07-106">It also explains how to create a job.</span></span>

## <a name="job-creation"></a><span data-ttu-id="4ee07-107">İş oluşturma</span><span class="sxs-lookup"><span data-stu-id="4ee07-107">Job creation</span></span>

<span data-ttu-id="4ee07-108">Yöneticiler, işe alanlar ve işe alma müdürleri işler oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="4ee07-108">Admins, recruiters, and hiring managers can create jobs.</span></span> <span data-ttu-id="4ee07-109">Bir iş oluşturduğunuzda, işlem sırasında rolünüzü seçmeniz istenir: işe alma yöneticisi veya işveren.</span><span class="sxs-lookup"><span data-stu-id="4ee07-109">When you create a job, you're prompted to select your role in the process: hiring manager or recruiter.</span></span> <span data-ttu-id="4ee07-110">Bir rol seçtikten sonra işlem şablonu seçmeniz istenir.</span><span class="sxs-lookup"><span data-stu-id="4ee07-110">After you select a role, you're prompted to select a process template.</span></span> <span data-ttu-id="4ee07-111">**Atla**'yı seçerseniz varsayılan şablon kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4ee07-111">If you select **Skip**, the default template is used.</span></span> <span data-ttu-id="4ee07-112">İşlem şablonları hakkında daha fazla bilgi için bkz. [Attract'ta işlem şablonu oluştur](./process-templates-attract.md).</span><span class="sxs-lookup"><span data-stu-id="4ee07-112">For more information about process templates, see [Create a process template in Attract](./process-templates-attract.md).</span></span>

<span data-ttu-id="4ee07-113">Attract'taki bir işin iş ayrıntıları, işe alma ekibi, bir işe alma işlemi, iş yayınlama ve analitiği vardır.</span><span class="sxs-lookup"><span data-stu-id="4ee07-113">A job in Attract has job details, a hiring team, a hiring process, job postings, and analytics.</span></span>

## <a name="job-details"></a><span data-ttu-id="4ee07-114">İş ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="4ee07-114">Job details</span></span>

<span data-ttu-id="4ee07-115">**İş ayrıntıları** sekmesi, iş sorumlulukları ve öznitelikleri hakkında ayrıntılı bilgi içerir.</span><span class="sxs-lookup"><span data-stu-id="4ee07-115">The **Job details** tab contains details about the job's responsibilities and attributes.</span></span> <span data-ttu-id="4ee07-116">İş unvanı, iş açıklaması ve iş yeri alanları gerekli alanlardır.</span><span class="sxs-lookup"><span data-stu-id="4ee07-116">The fields for the job title, job description, and job location are required.</span></span> <span data-ttu-id="4ee07-117">Diğer alanlar, isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="4ee07-117">The other fields are optional.</span></span>

<span data-ttu-id="4ee07-118">Varsayılan olarak **Boş pozisyon sayısı** **1** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="4ee07-118">By default, the **Number of openings** field is set to **1**.</span></span> <span data-ttu-id="4ee07-119">Ancak, değerde değişiklik yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4ee07-119">However, you can change the value.</span></span> <span data-ttu-id="4ee07-120">Ne zaman iş için bir teklif hazırlanırsa **Mevcut boş pozisyon sayısı** alanının değeri azaltılır.</span><span class="sxs-lookup"><span data-stu-id="4ee07-120">When an offer has been prepared for a job, the value of the **Number of openings available** field is decremented.</span></span>

<span data-ttu-id="4ee07-121">Konum yönetimi Yönetim Merkezinde etkinleştirilirse **Pozisyonları güncelleştir** araması kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4ee07-121">If position management has been turned on in the Admin Center, the **Update positions** lookup is available.</span></span> <span data-ttu-id="4ee07-122">Bu arama Uygulamalar için Common Data Service'teki JobPosition varlığını okur ve iş için seçilebilecek pozisyonların bir listesini verir.</span><span class="sxs-lookup"><span data-stu-id="4ee07-122">This lookup reads the JobPosition entity in Common Data Service for Apps and returns a list of positions that can be selected for the job.</span></span> <span data-ttu-id="4ee07-123">Seçtiğiniz pozisyon sayısı açık pozisyon sayısını aşarsa, bir uyarı alırsınız.</span><span class="sxs-lookup"><span data-stu-id="4ee07-123">If the number of positions that you select exceeds the number of open positions, you receive a warning.</span></span> <span data-ttu-id="4ee07-124">Pozisyon birden çok iş üzerinde kullanılırsa da uyarı alırsınız.</span><span class="sxs-lookup"><span data-stu-id="4ee07-124">You also receive a warning if a position is used on multiple jobs.</span></span>

> [!NOTE]
> <span data-ttu-id="4ee07-125">Pozisyon yönetimi, Kapsamlı işe alma eklentisinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4ee07-125">Position management is available with the Comprehensive Hiring Add-on.</span></span>

<span data-ttu-id="4ee07-126">İşe alma sürecinin Teklif eylemindeki ayarlara bağlı olarak pozisyon sayısı, bir teklifte iki kez kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4ee07-126">Depending on the settings in the Offer activity of the hiring process, a position number can be used twice in an offer.</span></span> <span data-ttu-id="4ee07-127">Daha fazla bilgi için bkz. [İşe alma süreci](./activities-attract.md).</span><span class="sxs-lookup"><span data-stu-id="4ee07-127">For more information, see [Hiring process](./activities-attract.md).</span></span>

<span data-ttu-id="4ee07-128">Attract'ta varsayılan **Beceriler** kümesi bulunur.</span><span class="sxs-lookup"><span data-stu-id="4ee07-128">Attract includes a default set of **Skills**.</span></span> <span data-ttu-id="4ee07-129">Bu beceriler yazarken öneri olarak görünür.</span><span class="sxs-lookup"><span data-stu-id="4ee07-129">These skills appear as suggestions as you type.</span></span> <span data-ttu-id="4ee07-130">Yeni yetenek metin alanına girip Enter' basarak daha fazla yetenek ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4ee07-130">You can add more skills by entering the new skill text in the field and then pressing Enter.</span></span>

<span data-ttu-id="4ee07-131">Attract'ta varsayılan **İş fonksiyonları** kümesi bulunur.</span><span class="sxs-lookup"><span data-stu-id="4ee07-131">Attract includes a default set of **Job functions**.</span></span> <span data-ttu-id="4ee07-132">Yeni iş fonksiyonu alanına girip Enter tuşuna basın, en çok üç iş fonksiyonu ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4ee07-132">You can add up to three more job functions by entering the new job function in the field and then pressing Enter.</span></span>

<span data-ttu-id="4ee07-133">Attract'ta varsayılan **Şirket sektörü** kümesi bulunur.</span><span class="sxs-lookup"><span data-stu-id="4ee07-133">Attract includes a default set of **Company industry**.</span></span> <span data-ttu-id="4ee07-134">Yeni şirket sektörü alanına girip Enter tuşuna basın, en çok üç şirket sektörü ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4ee07-134">You can add up to three more company industries by entering the new company industry in the field and then pressing Enter.</span></span>

## <a name="hiring-team"></a><span data-ttu-id="4ee07-135">İşe alım takımı</span><span class="sxs-lookup"><span data-stu-id="4ee07-135">Hiring team</span></span>

<span data-ttu-id="4ee07-136">**İşe alım ekibi** sekmesi, işe dahil edilecek kişilerin listesini içerir.</span><span class="sxs-lookup"><span data-stu-id="4ee07-136">The **Hiring team** tab contains the list of individuals who will be involved in the job.</span></span> <span data-ttu-id="4ee07-137">Kullanıcılar işe alma ekibine eklendiğinde, işe alma ekibinde role atanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4ee07-137">When users are added to a hiring team, they must be assigned a role on the hiring team.</span></span> <span data-ttu-id="4ee07-138">Rol, kullanıcıların aldıkları bildirimleri ve erişimi olduğu verileri belirler.</span><span class="sxs-lookup"><span data-stu-id="4ee07-138">The role determines the data that the users have access to and the notifications that they receive.</span></span> <span data-ttu-id="4ee07-139">Seçilebilecek roller **İş veren**, **İşe Alma Yöneticisi**, **Temsilci**, ve **Görüşmeyi Yapan**dır.</span><span class="sxs-lookup"><span data-stu-id="4ee07-139">The roles that can be selected are **Recruiter**, **Hiring manager**, **Delegate**, and **Interviewer**.</span></span> <span data-ttu-id="4ee07-140">Rol izinleri hakkında daha fazla bilgi için "Rol yönetimi" belgesine bakın.</span><span class="sxs-lookup"><span data-stu-id="4ee07-140">For more information about role privileges, see the "Role management" document.</span></span> <span data-ttu-id="4ee07-141">İşe alanlar ve işe alma müdürleri kendi adlarına çalışması için bir veya birden çok temsilci atayabilir.</span><span class="sxs-lookup"><span data-stu-id="4ee07-141">Recruiters and hiring managers can appoint one or more delegates to work on their behalf.</span></span> <span data-ttu-id="4ee07-142">Temsilciler hakkında daha fazla bilgi için bkz: [Attract'te güvenlik ve rol yönetimi](./security-attract.md).</span><span class="sxs-lookup"><span data-stu-id="4ee07-142">For more information about delegates, see [Security and role management in Attract](./security-attract.md).</span></span>

<span data-ttu-id="4ee07-143">İşe alma ekibi, iş etkinleştirildikten sonra güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="4ee07-143">The hiring team can be updated after the job is activated.</span></span>

## <a name="process"></a><span data-ttu-id="4ee07-144">İşlem</span><span class="sxs-lookup"><span data-stu-id="4ee07-144">Process</span></span>

<span data-ttu-id="4ee07-145">İşe alma süreci hakkında varsayılan bilgiler, iş oluştururken seçtiğiniz işlem şablonunu temel alır.</span><span class="sxs-lookup"><span data-stu-id="4ee07-145">Default information about the hiring process is based on the process template that was selected when the job was created.</span></span> <span data-ttu-id="4ee07-146">O anda belirli bir şablon seçilmezse, varsayılan şablon kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4ee07-146">If a specific template wasn't selected at that time, the default template is used.</span></span> <span data-ttu-id="4ee07-147">İşe alma işlemi tanımladığınızda Aday müşteri, Başvuru ve Teklif aşamaları dışında çeşitli aşamalar ekleyebilir veya kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4ee07-147">When you define the hiring process, you can add or remove various stages, except the Prospect, Application, and Offer stages.</span></span> <span data-ttu-id="4ee07-148">Ancak aday müşteri aşaması kaldırılamaz, devre dışı bırakılabilir.</span><span class="sxs-lookup"><span data-stu-id="4ee07-148">Although the Prospect stage can't be removed, it can be turned off.</span></span> <span data-ttu-id="4ee07-149">Her aşamada, bir veya birkaç faaliyet ekleyebilir veya kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4ee07-149">Within each stage, you can add or remove one or more predefined activities.</span></span>

<span data-ttu-id="4ee07-150">İşe alma işlemine eklenebilen faaliyetler hakkında daha fazla bilgi için bkz. [Attract işe alma süreci faaliyetleri ](./activities-attract.md).</span><span class="sxs-lookup"><span data-stu-id="4ee07-150">For more information about activities that can be added to the hiring process, see [Hiring process activities in Attract](./activities-attract.md).</span></span>

> [!NOTE]
> <span data-ttu-id="4ee07-151">İşe alma süreci, iş etkinleştirildikten sonra güncelleştirilemez.</span><span class="sxs-lookup"><span data-stu-id="4ee07-151">The process hiring can't be updated after a job is activated.</span></span>

## <a name="postings"></a><span data-ttu-id="4ee07-152">Deftere nakil işlemleri</span><span class="sxs-lookup"><span data-stu-id="4ee07-152">Postings</span></span>

<span data-ttu-id="4ee07-153">Bir iş etkinleştirildikten sonra yayınlanabilir.</span><span class="sxs-lookup"><span data-stu-id="4ee07-153">After a job is activated, it can be posted.</span></span> <span data-ttu-id="4ee07-154">Yalnızca iş verenler ve yöneticiler, işleri yayınlayabilir.</span><span class="sxs-lookup"><span data-stu-id="4ee07-154">Only recruiters and admins can post jobs.</span></span> <span data-ttu-id="4ee07-155">İş, Talent Careers (bir Microsoft Dynamics 365 for Talent kariyer sitesi) veya LinkedIn'de yayınlanabilir.</span><span class="sxs-lookup"><span data-stu-id="4ee07-155">The job can be posted to either Talent Careers (a Microsoft Dynamics 365 for Talent career site) or LinkedIn.</span></span> <span data-ttu-id="4ee07-156">Attract ekibi, iş kurulu toplayıcılarıyla ortaklık için devamlı çalışır.</span><span class="sxs-lookup"><span data-stu-id="4ee07-156">The Attract team continually works to partner with job board aggregators.</span></span> <span data-ttu-id="4ee07-157">Bu nedenle, zaman içinde bu listeyi genişler.</span><span class="sxs-lookup"><span data-stu-id="4ee07-157">Therefore, this list will expand over time.</span></span>

<span data-ttu-id="4ee07-158">İş yayınları hakkında daha fazla bilgi için [Attract'taki kariyer sitesi işlevi](./career-site.md).</span><span class="sxs-lookup"><span data-stu-id="4ee07-158">For more information about job postings, see [Career site functionality in Attract](./career-site.md).</span></span>

> [!NOTE]
> <span data-ttu-id="4ee07-159">İş yayınlama işlevi yalnızca işe Attract için Kapsamlı İşe Alım Eklentisiyle kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4ee07-159">The job posting functionality is available only with the Comprehensive Hiring Add-on for Attract.</span></span>

## <a name="activate"></a><span data-ttu-id="4ee07-160">Etkinleştir</span><span class="sxs-lookup"><span data-stu-id="4ee07-160">Activate</span></span>

<span data-ttu-id="4ee07-161">Bir iş etkinleştirildikten sonra yayınlanabilir, adaylar ve başvuranlar eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="4ee07-161">After a job is activated, it can be posted, and prospects and applicants can be added to it.</span></span> <span data-ttu-id="4ee07-162">Bir işe aday ekleme seçeneği, işe alma sürecindeki Aday eyleminde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="4ee07-162">The option to add prospects to a job is set in the Prospect activity in the hiring process.</span></span>

> [!NOTE]
> <span data-ttu-id="4ee07-163">İşe alma süreci, iş etkinleştirildikten sonra güncelleştirilemez.</span><span class="sxs-lookup"><span data-stu-id="4ee07-163">The process hiring can't be updated after a job is activated.</span></span>

## <a name="prospects-and-applicants"></a><span data-ttu-id="4ee07-164">Adaylar ve başvuranlar</span><span class="sxs-lookup"><span data-stu-id="4ee07-164">Prospects and applicants</span></span>

<span data-ttu-id="4ee07-165">Bir işe aday ekleme seçeneği, işe alma sürecindeki [Aday eyleminde](./activities-attract.md#prospect-activity) ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="4ee07-165">The option to add prospects to a job is set in the [Prospect activity](./activities-attract.md#prospect-activity) in the hiring process.</span></span> <span data-ttu-id="4ee07-166">Bu seçenek, iş etkinleştirmeden önce ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4ee07-166">This option should be set before you activate the job.</span></span> <span data-ttu-id="4ee07-167">Bir iş etkinleştirildikten sonra, adaylar ve başvuranlar eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="4ee07-167">After a job is activated, prospects and applicants can be added to it.</span></span>

## <a name="approvals"></a><span data-ttu-id="4ee07-168">Onaylar</span><span class="sxs-lookup"><span data-stu-id="4ee07-168">Approvals</span></span>

<span data-ttu-id="4ee07-169">Attract işleri, onay için gönderilebilir.</span><span class="sxs-lookup"><span data-stu-id="4ee07-169">Attract jobs can be submitted for approval.</span></span> <span data-ttu-id="4ee07-170">Tüm işler onay gerektirmez.</span><span class="sxs-lookup"><span data-stu-id="4ee07-170">Not all jobs require approval.</span></span> <span data-ttu-id="4ee07-171">Gereksinim şablon düzeyinde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="4ee07-171">The requirement is set at the template level.</span></span> <span data-ttu-id="4ee07-172">Varsayılan olarak, onaylar şablonda kapatılır.</span><span class="sxs-lookup"><span data-stu-id="4ee07-172">By default, approvals are turned off on the template.</span></span> <span data-ttu-id="4ee07-173">Onayları belirlemek için, bir işlem şablonuna gidin ve **Onay** alanını Varsayılan olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4ee07-173">To set up approvals, go to a process template, and set the **Approval** field to Default.</span></span> <span data-ttu-id="4ee07-174">Daha sonra iş oluştururken bu şablonu seçin.</span><span class="sxs-lookup"><span data-stu-id="4ee07-174">Then select that template when you create the job.</span></span>

<span data-ttu-id="4ee07-175">Bir iş kaydedildikten sonra onay için gönderilebilir.</span><span class="sxs-lookup"><span data-stu-id="4ee07-175">After a job is saved, it can be submitted for approval.</span></span> <span data-ttu-id="4ee07-176">Onayları kullanan belge durumları aşağıdaki tabloda listelenmiştir.</span><span class="sxs-lookup"><span data-stu-id="4ee07-176">The following table lists the statuses of a document that uses approvals.</span></span>

| <span data-ttu-id="4ee07-177">Durum</span><span class="sxs-lookup"><span data-stu-id="4ee07-177">Status</span></span>   | <span data-ttu-id="4ee07-178">İl</span><span class="sxs-lookup"><span data-stu-id="4ee07-178">State</span></span>                                                               |
|----------|---------------------------------------------------------------------|
| <span data-ttu-id="4ee07-179">Taslak</span><span class="sxs-lookup"><span data-stu-id="4ee07-179">Draft</span></span>    | <span data-ttu-id="4ee07-180">İş kaydedildi, ancak bir iş akışına gönderilmedi.</span><span class="sxs-lookup"><span data-stu-id="4ee07-180">The job has been saved, but it hasn't been submitted to a workflow.</span></span> |
| <span data-ttu-id="4ee07-181">Bekleyen</span><span class="sxs-lookup"><span data-stu-id="4ee07-181">Pending</span></span>  | <span data-ttu-id="4ee07-182">İş, onaylayıcılara gönderildi.</span><span class="sxs-lookup"><span data-stu-id="4ee07-182">The job has been submitted to approvers.</span></span>                            |
| <span data-ttu-id="4ee07-183">Onaylandı</span><span class="sxs-lookup"><span data-stu-id="4ee07-183">Approved</span></span> | <span data-ttu-id="4ee07-184">İş onaylandı, ancak etkinleştirilmedi.</span><span class="sxs-lookup"><span data-stu-id="4ee07-184">The job has been approved, but it hasn't been activated.</span></span>            |
| <span data-ttu-id="4ee07-185">Reddedildi</span><span class="sxs-lookup"><span data-stu-id="4ee07-185">Rejected</span></span> | <span data-ttu-id="4ee07-186">İş reddedildi ve etkinleştirilemez.</span><span class="sxs-lookup"><span data-stu-id="4ee07-186">The job has been rejected, and it can't be activated.</span></span>               |
| <span data-ttu-id="4ee07-187">Etkin</span><span class="sxs-lookup"><span data-stu-id="4ee07-187">Active</span></span>   | <span data-ttu-id="4ee07-188">İş onaylanmış ve etkinleştirilmiş.</span><span class="sxs-lookup"><span data-stu-id="4ee07-188">The job has been approved and activated.</span></span>                            |

<span data-ttu-id="4ee07-189">İş listesinde iş durumları üzerinde filtre uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4ee07-189">In the job list, you can filter on the job statuses.</span></span>

<span data-ttu-id="4ee07-190">Şirket içindeki herhangi bir Microsoft Azure Active Directory (Azure AD) kullanıcısına onaylar gönderilebilir.</span><span class="sxs-lookup"><span data-stu-id="4ee07-190">Approvals can be sent to any Microsoft Azure Active Directory (Azure AD) user in the company.</span></span> <span data-ttu-id="4ee07-191">Onaylar, paralel şekilde onaylayanlar olarak listelenen tüm kişilere gönderilir.</span><span class="sxs-lookup"><span data-stu-id="4ee07-191">The approvals are sent in parallel to all the people who are listed as approvers.</span></span> <span data-ttu-id="4ee07-192">Bir iş onaylandıktan sonra etkinleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="4ee07-192">After a job is approved, it can be activated.</span></span>

<span data-ttu-id="4ee07-193">Onaylayanlar olarak listelenen kişiler, Attract'ta onaylamak için bir öğe olduğunu bildiren bir bildirim alır.</span><span class="sxs-lookup"><span data-stu-id="4ee07-193">The people who are listed as approvers will receive a notification in Attract to inform them that they have an item to approve.</span></span> <span data-ttu-id="4ee07-194">Onay öğesi panodaki **Size atanan** bölümünde de görünür.</span><span class="sxs-lookup"><span data-stu-id="4ee07-194">An approval item will also appear in the **Assigned to you** section on the dashboard.</span></span> <span data-ttu-id="4ee07-195">Biri işi kabul edince veya onaylayınca işe alım ekibi bir bildirim alır.</span><span class="sxs-lookup"><span data-stu-id="4ee07-195">After someone accepts or approves a job, the hiring team will receive a notification.</span></span> <span data-ttu-id="4ee07-196">Son olarak, işe alım ekibi iş onaylandığında bildirim alır.</span><span class="sxs-lookup"><span data-stu-id="4ee07-196">Finally, the hiring team will receive a notification when the job is approved.</span></span>

## <a name="create-a-job"></a><span data-ttu-id="4ee07-197">İş oluşturma</span><span class="sxs-lookup"><span data-stu-id="4ee07-197">Create a job</span></span>

<span data-ttu-id="4ee07-198">Bir iş oluşturmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4ee07-198">Follow these steps to create a job.</span></span>

1. <span data-ttu-id="4ee07-199">**İşler**e gidin.</span><span class="sxs-lookup"><span data-stu-id="4ee07-199">Go to **Jobs**.</span></span>
2. <span data-ttu-id="4ee07-200">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4ee07-200">Select **New**.</span></span>
3. <span data-ttu-id="4ee07-201">**İş unvanı** alanına iş unvanı girin.</span><span class="sxs-lookup"><span data-stu-id="4ee07-201">In the **Job title** field, enter the job title.</span></span> <span data-ttu-id="4ee07-202">**Rol** alanına rolünüzü girin.</span><span class="sxs-lookup"><span data-stu-id="4ee07-202">In the **Role** field, enter your role.</span></span>
4. <span data-ttu-id="4ee07-203">**Şablon** alanında bir şablon seçin.</span><span class="sxs-lookup"><span data-stu-id="4ee07-203">In the **Template** field, select a template.</span></span> <span data-ttu-id="4ee07-204">Alternatif olarak **Atla**yı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4ee07-204">Alternatively, select **Skip**.</span></span> <span data-ttu-id="4ee07-205">**Atla** öğesini seçerseniz varsayılan şablon olarak işaretlenen şablon kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4ee07-205">If you select **Skip**, the template that is marked as the default template is used.</span></span>

    <span data-ttu-id="4ee07-206">Belge onay işlemine gitmesi gerekiyorsa **Onay işlemi** alanının **Varsayılan** olarak ayarlandığı bir şablon seçin.</span><span class="sxs-lookup"><span data-stu-id="4ee07-206">If the document should go through an approval process, select a template where the **Approval process** field is set to **Default**.</span></span>

5. <span data-ttu-id="4ee07-207">**Ayrıntılar** sekmesinde işin ayrıntılarını girin.</span><span class="sxs-lookup"><span data-stu-id="4ee07-207">On the **Details** tab, enter the details of the job.</span></span> <span data-ttu-id="4ee07-208">**Unvan**, **İş açıklaması** ve **Konum** alanları gerekli alanlardır.</span><span class="sxs-lookup"><span data-stu-id="4ee07-208">The **Title**, **Job description**, and **Location** fields are required.</span></span>
6. <span data-ttu-id="4ee07-209">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4ee07-209">Select **Save**.</span></span>
7. <span data-ttu-id="4ee07-210">**İşe alım ekibi** sekmesinde, bir işe alma yöneticisi, işe alan veya görüşmeyi yapan ekleyin.</span><span class="sxs-lookup"><span data-stu-id="4ee07-210">On the **Hiring team** tab, add a hiring manager, recruiter, or interviewer.</span></span>
8. <span data-ttu-id="4ee07-211">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4ee07-211">Select **Save**.</span></span>
9. <span data-ttu-id="4ee07-212">**Süreç** sekmesinde, gereken aşamaları ekleyin veya kaldırın:</span><span class="sxs-lookup"><span data-stu-id="4ee07-212">On the **Process** tab, add or remove stages as you require:</span></span>

    - <span data-ttu-id="4ee07-213">Aşama eklemek için **+ Yeni aşama**yı seçin.</span><span class="sxs-lookup"><span data-stu-id="4ee07-213">To add a stage, select **+ New Stage**.</span></span>
    - <span data-ttu-id="4ee07-214">Aşama kaldırmak için kaldırılacak aşama üzerine imleci getirin ve görünen çöp kutusu düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4ee07-214">To remove a stage, hover the pointer over the stage to remove, and then select the trash can button that appears.</span></span>

        > [!NOTE]
        > <span data-ttu-id="4ee07-215">Aday, Başvuru ve Teklif aşamaları kaldırılamaz.</span><span class="sxs-lookup"><span data-stu-id="4ee07-215">The Prospect, Application, and Offer stages can't be removed.</span></span>

10. <span data-ttu-id="4ee07-216">Gereken eylemleri ekleyip kaldırın:</span><span class="sxs-lookup"><span data-stu-id="4ee07-216">Add or remove activities as you require:</span></span>

    - <span data-ttu-id="4ee07-217">Aktivite eklemek için sağdaki listeden uygun aşamaya sürükleyin.</span><span class="sxs-lookup"><span data-stu-id="4ee07-217">To add an activity, drag it from the list on the right to the appropriate stage.</span></span> <span data-ttu-id="4ee07-218">Alternatif olarak, faaliyete çift tıklatın ve eklemek için aşamayı seçin.</span><span class="sxs-lookup"><span data-stu-id="4ee07-218">Alternatively, double-click the activity, and then select the stage to add it to.</span></span>
    - <span data-ttu-id="4ee07-219">Faaliyeti kaldırmak için, aktiviteyi genişletin ve faaliyet üst bilgisindeki çöp kutusu düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4ee07-219">To remove an activity, expand the activity, and then select the trash can button on the activity header.</span></span>

11. <span data-ttu-id="4ee07-220">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4ee07-220">Select **Save**.</span></span>
12. <span data-ttu-id="4ee07-221">Onay işlemi kullanmayı seçtiyseniz, aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="4ee07-221">If you selected to use an approval process, follow these steps:</span></span>

    1. <span data-ttu-id="4ee07-222">**+ Onaylayan ekle**'yi seçin ve Azure AD hesabı olan bir kullanıcı girin.</span><span class="sxs-lookup"><span data-stu-id="4ee07-222">Select **+ Add approver**, and then enter a user who has an Azure AD account.</span></span> <span data-ttu-id="4ee07-223">Birden çok onaylayan ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4ee07-223">You can add multiple approvers.</span></span>
    2. <span data-ttu-id="4ee07-224">**Onaylayanlara gönder**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4ee07-224">Select **Send to approvers**.</span></span>

    <span data-ttu-id="4ee07-225">İşin **İş durumu** alanı **Bekleyen** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="4ee07-225">The **Job status** field of the job is set to **Pending**.</span></span> <span data-ttu-id="4ee07-226">**İş durumu** alanı değeri **Onaylandı** olarak değiştiğinde, iş etkin hale getirilebilir.</span><span class="sxs-lookup"><span data-stu-id="4ee07-226">After the value of the **Job status** field changes to **Approved**, the job can be activated.</span></span>

13. <span data-ttu-id="4ee07-227">İşi etkinleştirmek için **Etkinleştir** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4ee07-227">To activate the job, select **Activate**.</span></span>
14. <span data-ttu-id="4ee07-228">İşi yayınlamak için **Gönderiler**'e gidin, Talen Careers sitesi veya LinkedIn'in altındaki **Hemen Yayınla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="4ee07-228">To post the job, go to **Postings**, and then select **Post Now** under the Talent Careers site or LinkedIn.</span></span>

