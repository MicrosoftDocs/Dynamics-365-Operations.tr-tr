---
title: "Attract'ta kariyer sitesi işlevi"
description: "Bu makale Microsoft Dynamics 365 for Talent - Attract içerisindeki adaya yönelik kariyer sitesi özelliği hakkında genel bakış sağlar. Bu makale bu işlevselliği ayarlamayı açıklar."
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 452e3e92ea32ab5f1e3720ab81ff2f7ea18b2a06
ms.contentlocale: tr-tr
ms.lasthandoff: 10/22/2018

---
# <a name="career-site-functionality-in-attract"></a><span data-ttu-id="7cdab-104">Attract'ta kariyer sitesi işlevi</span><span class="sxs-lookup"><span data-stu-id="7cdab-104">Career site functionality in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7cdab-105">Bu makale Microsoft Dynamics 365 for Talent: Attract içerisindeki adaya yönelik kariyer sitesi özelliği hakkında genel bakış sağlar.</span><span class="sxs-lookup"><span data-stu-id="7cdab-105">This article provides an overview of the candidate-facing career site functionality in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="7cdab-106">Bu makale bu işlevselliği ayarlamayı açıklar.</span><span class="sxs-lookup"><span data-stu-id="7cdab-106">It also explains how to set up this functionality.</span></span>

## <a name="overview"></a><span data-ttu-id="7cdab-107">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="7cdab-107">Overview</span></span>

<span data-ttu-id="7cdab-108">Attract, kariyer sitesini bir kiracıdaki her bir ortamda sağlar.</span><span class="sxs-lookup"><span data-stu-id="7cdab-108">Attract provides one career site for each environment in a tenant.</span></span> <span data-ttu-id="7cdab-109">Örneğin, bir kuruluşta bir geliştirme ortamı ve test ortamı varsa, geliştirme ortamı için bir mesleki site ve test ortamı için başka bir site sağlanır.</span><span class="sxs-lookup"><span data-stu-id="7cdab-109">For example, if an organization has a development environment and a test environment, one career site is provisioned for the development environment, and another career site is provisioned for the test environment.</span></span> <span data-ttu-id="7cdab-110">Mesleki her site **tamamen ayrılmış** ve kendi kimlik doğrulama mekanizması vardır.</span><span class="sxs-lookup"><span data-stu-id="7cdab-110">Each career site is **completely isolated** and has its own authentication mechanism.</span></span> <span data-ttu-id="7cdab-111">İşler ve aday profilleri mesleki siteler arasında paylaşılmaz.</span><span class="sxs-lookup"><span data-stu-id="7cdab-111">Jobs and candidate profiles aren't shared between career sites.</span></span>

<span data-ttu-id="7cdab-112">Varsayılan olarak, mesleki site herkese açıktır.</span><span class="sxs-lookup"><span data-stu-id="7cdab-112">By default, the career site is public.</span></span> <span data-ttu-id="7cdab-113">Bu nedenle, aday harici oturum açmadan işaretlenen tüm işleri görebilir.</span><span class="sxs-lookup"><span data-stu-id="7cdab-113">Therefore, candidates can view all jobs that are marked as external without having to sign in.</span></span> <span data-ttu-id="7cdab-114">Bununla birlikte, tüm eylemler adayların oturum açmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="7cdab-114">However, all other actions require that candidates sign in.</span></span>

## <a name="career-site-management"></a><span data-ttu-id="7cdab-115">Kariyer sitesi yönetimi</span><span class="sxs-lookup"><span data-stu-id="7cdab-115">Career site management</span></span>

<span data-ttu-id="7cdab-116">Aşağıdaki öğeler mesleki sitede ayarlarla denetlenir:</span><span class="sxs-lookup"><span data-stu-id="7cdab-116">The following items on the career site are controlled by settings:</span></span>

- <span data-ttu-id="7cdab-117">**Kuruluş adı:** Kuruluş adı, kariyer sitesinin üstündeki gezinti çubuğunda görünür.</span><span class="sxs-lookup"><span data-stu-id="7cdab-117">**Organization name:** The organization name appears on the navigation bar at the top of the career site.</span></span> <span data-ttu-id="7cdab-118">Aday kuruluş adını seçerek tüm açık iş listeleyen bir sayfaya gider.</span><span class="sxs-lookup"><span data-stu-id="7cdab-118">By selecting the organization name, candidates go to a page that lists all open jobs.</span></span>
- <span data-ttu-id="7cdab-119">**Kuruluş logosu:** Kuruluşun logo görüntüsü kariyer sitesinin sol üst köşesinde görünür.</span><span class="sxs-lookup"><span data-stu-id="7cdab-119">**Organization logo:** An image of the organization's logo appears in the upper left of the career site.</span></span> <span data-ttu-id="7cdab-120">Aday logo görüntüsünü seçerek tüm açık iş listeleyen bir sayfaya gider.</span><span class="sxs-lookup"><span data-stu-id="7cdab-120">By selecting the logo image, candidates go to a page that lists all open jobs.</span></span>

<span data-ttu-id="7cdab-121">Kuruluş adı ve logosu için değerleri ayarlamak üzere, Attract'ta yönetici olarak oturum açın; **Ayarlar** menüsündeki (çark simgesi) **Yönetim Merkezi**'ni seçin ve **şirket bilgileri** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7cdab-121">To set the values for the organization name and logo, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu (the gear symbol), and then select the **Company information** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="7cdab-122">Kariyer sitesinde görüntülenen logo görüntüsünün, sabit 20 piksel (px) yüksekliği vardır.</span><span class="sxs-lookup"><span data-stu-id="7cdab-122">The logo image that appears on the career site has a fixed height of 20 pixels (px).</span></span> <span data-ttu-id="7cdab-123">Yönetim merkezine eklediğiniz görüntü uyacak şekilde ölçeklendirilir.</span><span class="sxs-lookup"><span data-stu-id="7cdab-123">The image that you add in the Admin center is scaled to fit.</span></span> <span data-ttu-id="7cdab-124">Bu nedenle, genişliği resme bağlı olarak değişebilir.</span><span class="sxs-lookup"><span data-stu-id="7cdab-124">Therefore, depending on the image, the width might change.</span></span>

## <a name="career-site-url"></a><span data-ttu-id="7cdab-125">Kariyer sitesi URL'si</span><span class="sxs-lookup"><span data-stu-id="7cdab-125">Career site URL</span></span>

<span data-ttu-id="7cdab-126">İlk defa [harici bir iş paylaştığınızda](./Creating-jobs-Attract.md#postings), Attract uygulamasından **Uygula** bağlantısını kopyalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7cdab-126">When you [post an external job](./Creating-jobs-Attract.md#postings) for the first time, you can copy the **Apply** link from the Attract application.</span></span> <span data-ttu-id="7cdab-127">Bu bağlantı URL'si şu biçimde olur:`https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`</span><span class="sxs-lookup"><span data-stu-id="7cdab-127">The URL for this link will be in the following format: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`</span></span>

<span data-ttu-id="7cdab-128">Kariyer sitesinin URL'si bir **Uygula** URL'sinin alt dizesidir.</span><span class="sxs-lookup"><span data-stu-id="7cdab-128">The URL of the career site is a substring of the **Apply** URL.</span></span> <span data-ttu-id="7cdab-129">Şirket adına kadar her şeyen oluşur.</span><span class="sxs-lookup"><span data-stu-id="7cdab-129">It consists of everything up through the company name.</span></span> <span data-ttu-id="7cdab-130">Bu nedenle, önceki **Uygula** URL'si için, kariyer site URL'si: `https://jobs.talent.dynamics.com/jobs/<company_name>/`.</span><span class="sxs-lookup"><span data-stu-id="7cdab-130">Therefore, for the preceding **Apply** URL, the career site URL is `https://jobs.talent.dynamics.com/jobs/<company_name>/`.</span></span>

## <a name="authentication-options"></a><span data-ttu-id="7cdab-131">Kimlik doğrulama seçenekleri</span><span class="sxs-lookup"><span data-stu-id="7cdab-131">Authentication options</span></span>

<span data-ttu-id="7cdab-132">Adayların Attract mesleki sitesi için seçenekleri şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7cdab-132">Candidates have the following sign-in options for an Attract career site:</span></span>

- <span data-ttu-id="7cdab-133">Kişisel hesap:</span><span class="sxs-lookup"><span data-stu-id="7cdab-133">Personal account:</span></span>

    - <span data-ttu-id="7cdab-134">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="7cdab-134">LinkedIn</span></span>
    - <span data-ttu-id="7cdab-135">Microsoft</span><span class="sxs-lookup"><span data-stu-id="7cdab-135">Microsoft</span></span>
    - <span data-ttu-id="7cdab-136">Google</span><span class="sxs-lookup"><span data-stu-id="7cdab-136">Google</span></span>
    - <span data-ttu-id="7cdab-137">Facebook</span><span class="sxs-lookup"><span data-stu-id="7cdab-137">Facebook</span></span>

- <span data-ttu-id="7cdab-138">İş veya okul hesabı:</span><span class="sxs-lookup"><span data-stu-id="7cdab-138">Work or school account:</span></span>

    - <span data-ttu-id="7cdab-139">Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="7cdab-139">Microsoft Azure Active Directory (Azure AD)</span></span>

<span data-ttu-id="7cdab-140">Azure AD oturum açma, yalnızca dahili aday içindir.</span><span class="sxs-lookup"><span data-stu-id="7cdab-140">Azure AD sign-in is intended only for internal candidates.</span></span> <span data-ttu-id="7cdab-141">Bu nedenle, yalnızca Azure AD kimlik bilgilerini kullanan iç adaylar için çalışır.</span><span class="sxs-lookup"><span data-stu-id="7cdab-141">Therefore, it works only for internal candidates who use their company Azure AD credentials.</span></span> <span data-ttu-id="7cdab-142">Örneğin, Contoso Ltd bir çalışanı olan bir aday, alakalı olmayan bir şirket olan Alpine Ski House'da bir işe başvurmak istiyor.</span><span class="sxs-lookup"><span data-stu-id="7cdab-142">For example, a candidate who is currently an employee of Contoso Ltd wants to apply for a job in an unrelated company, Alpine Ski House.</span></span> <span data-ttu-id="7cdab-143">Bu durumda, çalışan Contoso Ltd.'den kendi şirket Azure AD kimlik bilgilerini kullanmaya çalışırsa, başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="7cdab-143">In this case, the sign-in will be unsuccessful if the employee tries to use his or her Azure AD credentials from Contoso Ltd.</span></span>

## <a name="create-and-maintain-a-profile"></a><span data-ttu-id="7cdab-144">Profil oluştur ve sürdür</span><span class="sxs-lookup"><span data-stu-id="7cdab-144">Create and maintain a profile</span></span>

<span data-ttu-id="7cdab-145">Mesleki siteye adaylar oturum açtıktan sonra profil oluşturmak ve kendi profilini güncelleştirmek için sayfanın üstündeki gezinme çubuğunda **Profilim**'i seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7cdab-145">After candidates sign in to the career site, they can select **My profile** on the navigation bar at the top of the page to create and maintain their profile.</span></span> <span data-ttu-id="7cdab-146">Profil kişisel bilgileri, iş deneyimiyle ilgili bilgiler, eğitim ayrıntıları, belgeleri, bağlantıları ve beceri kümeleri hakkında bilgi içerir.</span><span class="sxs-lookup"><span data-stu-id="7cdab-146">The profile includes personal information, information about work experience, education details, documents, links, and information about skill sets.</span></span> <span data-ttu-id="7cdab-147">Profil oluşturulduktan sonra adayın ilgilendiği işlere başvurmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="7cdab-147">After a profile is created, it can be used to apply for jobs that the candidate is interested in.</span></span> <span data-ttu-id="7cdab-148">Profiller, Attract'a adaylar için doğru işlere önermesine yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="7cdab-148">Profiles also help Attract recommend the right jobs to candidates.</span></span>

## <a name="find-the-right-job"></a><span data-ttu-id="7cdab-149">Uygun işi bulun</span><span class="sxs-lookup"><span data-stu-id="7cdab-149">Find the right job</span></span>

<span data-ttu-id="7cdab-150">İş listesi sayfasında, aday arama koşulları girerek belirli bir iş için arama yapabilir.</span><span class="sxs-lookup"><span data-stu-id="7cdab-150">On the job list page, candidates can search for a specific job by entering search terms.</span></span> <span data-ttu-id="7cdab-151">Arama işlevselliği, iş başlığı ve açıklamada iş arama terimlerine bakar arar ve sonuçları ilgili işleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="7cdab-151">The search functionality looks for the search terms in job titles and job descriptions, and shows relevant jobs as results.</span></span> <span data-ttu-id="7cdab-152">Adaylar iş yeri veya işlevleri temel alarak herhangi bir anda sonuçları filtreleyebilir.</span><span class="sxs-lookup"><span data-stu-id="7cdab-152">Candidates can filter the results at any time, based on the job location or job function.</span></span>

<span data-ttu-id="7cdab-153">Adaylar kariyer sitesinde önerilen iş kümesini de görebilir.</span><span class="sxs-lookup"><span data-stu-id="7cdab-153">Candidates can also view a set of recommended jobs on the career site.</span></span> <span data-ttu-id="7cdab-154">Aday için önerilen güncelleştirmelerin işleri adayın eski başvuruları, profili ve özgeçmiş üzerinde temel alır.</span><span class="sxs-lookup"><span data-stu-id="7cdab-154">The jobs that are recommended to a candidate are based on the candidate's past applications, profile, and resumes.</span></span>

> [!NOTE]
> <span data-ttu-id="7cdab-155">İş önerileri mesleki sitede en az 10 iş varsa ve aday profilini tamamlarsa gösterilir.</span><span class="sxs-lookup"><span data-stu-id="7cdab-155">Job recommendations are shown only if at least 10 jobs are posted on the career site, and if the candidate has completed his or her profile.</span></span>

## <a name="apply-for-jobs"></a><span data-ttu-id="7cdab-156">İşlere başvur</span><span class="sxs-lookup"><span data-stu-id="7cdab-156">Apply for jobs</span></span>

<span data-ttu-id="7cdab-157">Adaylar doğru işi bulduktan sonra, iş ayrıntıları sayfasında **Uygula** düğmesini kullanarak başvurabilirler.</span><span class="sxs-lookup"><span data-stu-id="7cdab-157">After candidates find the right job, they can apply by using the **Apply** button on the job details page.</span></span> <span data-ttu-id="7cdab-158">Bu aşamada adaylar yeni bir profil oluşturabilir veya varolan profillerindeki ilgili bilgileri gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="7cdab-158">At this point, candidates can either create a brand-new profile or review the information in their existing profile.</span></span> <span data-ttu-id="7cdab-159">Adaylar gerekirse bir özgeçmiş ve sonra iş başvurusu gönderebilir.</span><span class="sxs-lookup"><span data-stu-id="7cdab-159">Candidates can also upload a resume, as required, and then submit the job application.</span></span>

## <a name="check-application-status"></a><span data-ttu-id="7cdab-160">Başvuru durumunu kontrol edin</span><span class="sxs-lookup"><span data-stu-id="7cdab-160">Check application status</span></span>

<span data-ttu-id="7cdab-161">Adaylar bir veya daha fazla işe başvurduğunda, açık ve kapalı uygulamalarını görüntülemek için sayfanın üstündeki gezinme çubuğundaki **Başvurular**'ı seçebilir.</span><span class="sxs-lookup"><span data-stu-id="7cdab-161">After candidates apply for one or more jobs, they can select **Applications** on the navigation bar at the top of the page to view their open and closed applications.</span></span> <span data-ttu-id="7cdab-162">Aday başvurularından birini açarken geçerli aşamayı ve tamamlaması gereken eylem öğelerini görür.</span><span class="sxs-lookup"><span data-stu-id="7cdab-162">When candidates open one of their applications, they see the current stage and any pending action items that they must complete.</span></span> <span data-ttu-id="7cdab-163">Örneğin, bir adayın yüz yüze görüşme tarihlerini belirtmesi gerekiyorsa sayfada seçenekleri gösterilir.</span><span class="sxs-lookup"><span data-stu-id="7cdab-163">For example, if a candidate must provide potential dates for an in-person interview, the page shows his or her options.</span></span>

## <a name="internal-jobs"></a><span data-ttu-id="7cdab-164">Dahili işler</span><span class="sxs-lookup"><span data-stu-id="7cdab-164">Internal jobs</span></span>

<span data-ttu-id="7cdab-165">Şu anda, dahili olarak işaretlenen ve Attract kariyer sitesine gönderilmeyen işler kariyer sitesinde görünmez.</span><span class="sxs-lookup"><span data-stu-id="7cdab-165">Currently, jobs that are marked as internal and posted to the Attract career site don't appear on the career site.</span></span> <span data-ttu-id="7cdab-166">Yalnızca Attract başvurusundan koplayanabilen **Başvur** URL'siyle erişilebilir.</span><span class="sxs-lookup"><span data-stu-id="7cdab-166">They are accessible only via the direct **Apply** URL that can be copied from the Attract application.</span></span>

