---
title: Attract'ta kariyer sitesi işlevi
description: Bu konu, Attract içinde adaya yönelik site işlevi hakkında genel bakış sağlar.
author: josaw1
manager: AnnBe
ms.date: 02/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-02-12
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: 087ab4034a1e601e7f3514c77d56ef54b0c5c52d
ms.sourcegitcommit: 1ee613a88edddab036d145f27f19d071a4b8ad24
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/13/2019
ms.locfileid: "389990"
---
# <a name="career-site-functionality-in-attract"></a><span data-ttu-id="c7506-103">Attract'ta kariyer sitesi işlevi</span><span class="sxs-lookup"><span data-stu-id="c7506-103">Career site functionality in Attract</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c7506-104">Bu konu, Microsoft Dynamics 365 for Talent: Attract içinde adaya yönelik site işlevi hakkında genel bakış sağlar.</span><span class="sxs-lookup"><span data-stu-id="c7506-104">This topic provides an overview of the candidate-facing career site functionality in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="c7506-105">Bu makale bu işlevselliği ayarlamayı açıklar.</span><span class="sxs-lookup"><span data-stu-id="c7506-105">It also explains how to set up this functionality.</span></span>

<span data-ttu-id="c7506-106">Attract, kariyer sitesini bir kiracıdaki her bir ortamda sağlar.</span><span class="sxs-lookup"><span data-stu-id="c7506-106">Attract provides one career site for each environment in a tenant.</span></span> <span data-ttu-id="c7506-107">Örneğin, bir kuruluşta bir geliştirme ortamı ve test ortamı varsa, geliştirme ortamı için bir mesleki site ve test ortamı için başka bir site sağlanır.</span><span class="sxs-lookup"><span data-stu-id="c7506-107">For example, if an organization has a development environment and a test environment, one career site is provisioned for the development environment, and another career site is provisioned for the test environment.</span></span> <span data-ttu-id="c7506-108">Mesleki her site tamamen ayrılmış ve kendi kimlik doğrulama mekanizması vardır.</span><span class="sxs-lookup"><span data-stu-id="c7506-108">Each career site is completely isolated and has its own authentication mechanism.</span></span> <span data-ttu-id="c7506-109">İşler ve aday profilleri mesleki siteler arasında paylaşılmaz.</span><span class="sxs-lookup"><span data-stu-id="c7506-109">Jobs and candidate profiles aren't shared between career sites.</span></span>

<span data-ttu-id="c7506-110">Varsayılan olarak, mesleki site herkese açıktır.</span><span class="sxs-lookup"><span data-stu-id="c7506-110">By default, the career site is public.</span></span> <span data-ttu-id="c7506-111">Bu nedenle, aday harici oturum açmadan işaretlenen tüm işleri görebilir.</span><span class="sxs-lookup"><span data-stu-id="c7506-111">Therefore, candidates can view all jobs that are marked as external without having to sign in.</span></span> <span data-ttu-id="c7506-112">Bununla birlikte, tüm eylemler adayların oturum açmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="c7506-112">However, all other actions require that candidates sign in.</span></span>

## <a name="career-site-management"></a><span data-ttu-id="c7506-113">Kariyer sitesi yönetimi</span><span class="sxs-lookup"><span data-stu-id="c7506-113">Career site management</span></span>

<span data-ttu-id="c7506-114">Aşağıdaki öğeler için değerleri ayarlamak üzere, Attract'ta yönetici olarak oturum açın; **Ayarlar** menüsündeki (çark simgesi) **Yönetim Merkezi**'ni seçin ve **Şirket bilgileri** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c7506-114">To set the values for the following items, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu (the gear symbol), and then select the **Company information** tab.</span></span>

-   <span data-ttu-id="c7506-115">**Kuruluş adı** - Kuruluş adı, kariyer sitesinin üstündeki gezinti çubuğunda görünür.</span><span class="sxs-lookup"><span data-stu-id="c7506-115">**Organization name** - The organization name appears on the navigation bar at the top of the career site.</span></span> <span data-ttu-id="c7506-116">Aday kuruluş adını seçerek tüm açık iş listeleyen bir sayfaya gider.</span><span class="sxs-lookup"><span data-stu-id="c7506-116">By selecting the organization name, candidates go to a page that lists all open jobs.</span></span>

-   <span data-ttu-id="c7506-117">**Kuruluş logosu** - Kuruluşun logo görüntüsü kariyer sitesinin sol üst köşesinde görünür.</span><span class="sxs-lookup"><span data-stu-id="c7506-117">**Organization logo** - An image of the organization's logo appears in the upper left of the career site.</span></span> <span data-ttu-id="c7506-118">Aday logo görüntüsünü seçerek tüm açık iş listeleyen bir sayfaya gider.</span><span class="sxs-lookup"><span data-stu-id="c7506-118">By selecting the logo image, candidates go to a page that lists all open jobs.</span></span>

    >   [!NOTE] 
    >   <span data-ttu-id="c7506-119">Kariyer sitesinde görüntülenen logo görüntüsünün, sabit 20 piksel (px) yüksekliği vardır.</span><span class="sxs-lookup"><span data-stu-id="c7506-119">The logo image that appears on the career site has a fixed height of 20 pixels (px).</span></span> <span data-ttu-id="c7506-120">Yönetim merkezine eklediğiniz görüntü uyacak şekilde ölçeklendirilir.</span><span class="sxs-lookup"><span data-stu-id="c7506-120">The image that you add in the Admin center is scaled to fit.</span></span> <span data-ttu-id="c7506-121">Bu nedenle, genişliği resme bağlı olarak değişebilir.</span><span class="sxs-lookup"><span data-stu-id="c7506-121">Therefore, depending on the image, the width might change.</span></span>
 
<span data-ttu-id="c7506-122">Aşağıdaki öğeler için değerleri ayarlamak üzere, Attract'ta yönetici olarak oturum açın; **Ayarlar** menüsündeki **Yönetim Merkezi**'ni seçin ve **Kariyer sitesi yönetimi** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c7506-122">To set the values for the following items, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu, and then select the **Career site management** tab.</span></span>

-   <span data-ttu-id="c7506-123">**Arama Motoru Optimizasyonu** - Etkinleştirildiğinde, Attract kariyer sitesine gönderilen tüm ortak iş ilanları, Bing ve Google gibi arama motorları kullanılarak aranabilir olacaktır.</span><span class="sxs-lookup"><span data-stu-id="c7506-123">**Search Engine Optimization** - When enabled, all public jobs posted to Attract career site will be searchable using search engines like Bing and Google.</span></span>

    >   [!NOTE] 
    >   <span data-ttu-id="c7506-124">Bu ayarın etkinleştirilmesiyle, arama sonuçlarının görüntülenmesi arasında bir gecikme olabilir, kullandığınız arama motoruna bağlı olarak.</span><span class="sxs-lookup"><span data-stu-id="c7506-124">There might be a delay between turning this setting on and search results appearing, depending on the search engine that you are using.</span></span>
         
## <a name="career-site-urls"></a><span data-ttu-id="c7506-125">Kariyer sitesi URL'leri</span><span class="sxs-lookup"><span data-stu-id="c7506-125">Career site URLs</span></span>

<span data-ttu-id="c7506-126">Aşağıdaki liste, sık kullanılan kariyer sitesi URL'leri ve bunlara nasıl erişileceğini içerir.</span><span class="sxs-lookup"><span data-stu-id="c7506-126">The following list contains the commonly used career site URLs and how to access them.</span></span>

-   <span data-ttu-id="c7506-127">**Kariyer sitesi giriş sayfası URL'si** - Kariyeri sitesi giriş sayfası URL'sini görüntülemek için, Attract'e bir yönetici olarak oturum açın, **Ayarlar** menüsünde **Yönetici merkezi**'ni seçin ve sonra **Kariyer sitesi yönetimi** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c7506-127">**Career site home page URL** - To view the career site home page URL, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu, and then select the **Career site management** tab.</span></span>

-   <span data-ttu-id="c7506-128">**Bireysel iş ilanı başvuru URL'si** - Siz ilk defa [bir harici iş ilanı verdiğinizde](Creating-jobs-Attract.md#postings), Attract uygulamasından **Uygula** bağlantısını kopyalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7506-128">**Individual job post apply URL** - When you [post an external job](Creating-jobs-Attract.md#postings) for the first time, you can copy the **Apply** link from the Attract application.</span></span> <span data-ttu-id="c7506-129">Bu bağlantı için URL aşağıdaki biçimde olacaktır: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)</span><span class="sxs-lookup"><span data-stu-id="c7506-129">The URL for this link will be in the following format: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)</span></span>

-   <span data-ttu-id="c7506-130">**Bireysel iş ilanı URL'si** - İş ilanının URL'si, Başvur URL'sinin bir alt dizesidir.</span><span class="sxs-lookup"><span data-stu-id="c7506-130">**Individual job post URL** - The URL of the job post is a substring of the Apply URL.</span></span> <span data-ttu-id="c7506-131">İş numarasına kadar her şeyden oluşur.</span><span class="sxs-lookup"><span data-stu-id="c7506-131">It consists of everything up through the job number.</span></span> <span data-ttu-id="c7506-132">Bu nedenle, öncedeki Başvur URL'si için iş ilanı URL'si [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e) olur</span><span class="sxs-lookup"><span data-stu-id="c7506-132">Therefore, for the preceding Apply URL, the job post URL is [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e)</span></span>

## <a name="authentication-options"></a><span data-ttu-id="c7506-133">Kimlik doğrulama seçenekleri</span><span class="sxs-lookup"><span data-stu-id="c7506-133">Authentication options</span></span>

<span data-ttu-id="c7506-134">Adayların Attract mesleki sitesi için seçenekleri şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c7506-134">Candidates have the following sign-in options for an Attract career site:</span></span>

-   <span data-ttu-id="c7506-135">Kişisel hesap:</span><span class="sxs-lookup"><span data-stu-id="c7506-135">Personal account:</span></span>

    -   <span data-ttu-id="c7506-136">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="c7506-136">LinkedIn</span></span>

    -   <span data-ttu-id="c7506-137">Microsoft</span><span class="sxs-lookup"><span data-stu-id="c7506-137">Microsoft</span></span>

    -   <span data-ttu-id="c7506-138">Google</span><span class="sxs-lookup"><span data-stu-id="c7506-138">Google</span></span>

    -   <span data-ttu-id="c7506-139">Facebook</span><span class="sxs-lookup"><span data-stu-id="c7506-139">Facebook</span></span>

-   <span data-ttu-id="c7506-140">İş veya okul hesabı:</span><span class="sxs-lookup"><span data-stu-id="c7506-140">Work or school account:</span></span>

    -   <span data-ttu-id="c7506-141">Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="c7506-141">Microsoft Azure Active Directory (Azure AD)</span></span>

<span data-ttu-id="c7506-142">Azure AD oturum açma, yalnızca dahili aday içindir.</span><span class="sxs-lookup"><span data-stu-id="c7506-142">Azure AD sign-in is intended only for internal candidates.</span></span> <span data-ttu-id="c7506-143">Bu nedenle, yalnızca Azure AD kimlik bilgilerini kullanan iç adaylar için çalışır.</span><span class="sxs-lookup"><span data-stu-id="c7506-143">Therefore, it works only for internal candidates who use their company Azure AD credentials.</span></span> <span data-ttu-id="c7506-144">Örneğin, Contoso Ltd bir çalışanı olan bir aday, alakalı olmayan bir şirket olan Alpine Ski House'da bir işe başvurmak istiyor.</span><span class="sxs-lookup"><span data-stu-id="c7506-144">For example, a candidate who is currently an employee of Contoso Ltd wants to apply for a job in an unrelated company, Alpine Ski House.</span></span> <span data-ttu-id="c7506-145">Bu durumda, çalışan Contoso Ltd.'den kendi şirket Azure AD kimlik bilgilerini kullanmaya çalışırsa, başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="c7506-145">In this case, the sign-in will be unsuccessful if the employee tries to use Azure AD credentials from Contoso Ltd.</span></span>

## <a name="create-and-maintain-a-profile"></a><span data-ttu-id="c7506-146">Profil oluştur ve sürdür</span><span class="sxs-lookup"><span data-stu-id="c7506-146">Create and maintain a profile</span></span>

<span data-ttu-id="c7506-147">Mesleki siteye adaylar oturum açtıktan sonra profil oluşturmak ve kendi profilini güncelleştirmek için sayfanın üstündeki gezinme çubuğunda **Profilim**'i seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7506-147">After candidates sign in to the career site, they can select **My profile** on the navigation bar at the top of the page to create and maintain their profile.</span></span>
<span data-ttu-id="c7506-148">Profil kişisel bilgileri, iş deneyimiyle ilgili bilgiler, eğitim ayrıntıları, belgeleri, bağlantıları ve beceri kümeleri hakkında bilgi içerir.</span><span class="sxs-lookup"><span data-stu-id="c7506-148">The profile includes personal information, information about work experience, education details, documents, links, and information about skill sets.</span></span> <span data-ttu-id="c7506-149">Profil oluşturulduktan sonra adayın ilgilendiği işlere başvurmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c7506-149">After a profile is created, it can be used to apply for jobs that the candidate is interested in.</span></span> <span data-ttu-id="c7506-150">Profiller, Attract'a adaylar için doğru işlere önermesine yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="c7506-150">Profiles also help Attract recommend the right jobs to candidates.</span></span>

>   [!NOTE]
>   <span data-ttu-id="c7506-151">Aday kullanıyorsa, yukarıda listelenen e-posta kimliği için yetkilendirme sağlayıcılarını birini kullanarak oturum açın, profiliyle ilişkili ilgili kişi e-posta kodu, e-posta kodu varsayılan olur.</span><span class="sxs-lookup"><span data-stu-id="c7506-151">If a candidate uses an email ID to sign in using one of the authentication providers listed above, that email ID will default to the contact email ID associated with the profile.</span></span> <span data-ttu-id="c7506-152">Ancak, sonraki istenilen zaman değiştirilebilir ve ilkinden tümüyle bağımsızdır.</span><span class="sxs-lookup"><span data-stu-id="c7506-152">However, the latter can be changed at any time and is completely independent of the former.</span></span> <span data-ttu-id="c7506-153">Attract her zaman iletişim e-posta kimliğini, tüm e-posta iletişimleri için profilinizle ilişkilendirecektir.</span><span class="sxs-lookup"><span data-stu-id="c7506-153">Attract will always use the contact email ID to associate with your profile for all email communications.</span></span>

## <a name="find-the-right-job"></a><span data-ttu-id="c7506-154">Uygun işi bulun</span><span class="sxs-lookup"><span data-stu-id="c7506-154">Find the right job</span></span>

<span data-ttu-id="c7506-155">İş listesi sayfasında, aday arama koşulları girerek belirli bir iş için arama yapabilir.</span><span class="sxs-lookup"><span data-stu-id="c7506-155">On the job list page, candidates can search for a specific job by entering search terms.</span></span> <span data-ttu-id="c7506-156">Arama işlevselliği, iş başlığı ve açıklamada iş arama terimlerine bakar arar ve sonuçları ilgili işleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="c7506-156">The search functionality looks for the search terms in job titles and job descriptions, and shows relevant jobs as results.</span></span> <span data-ttu-id="c7506-157">Adaylar iş yeri veya işlevleri temel alarak herhangi bir anda sonuçları filtreleyebilir.</span><span class="sxs-lookup"><span data-stu-id="c7506-157">Candidates can filter the results at any time, based on the job location or job function.</span></span>

<span data-ttu-id="c7506-158">Adaylar kariyer sitesinde önerilen iş kümesini de görebilir.</span><span class="sxs-lookup"><span data-stu-id="c7506-158">Candidates can also view a set of recommended jobs on the career site.</span></span> <span data-ttu-id="c7506-159">Aday için önerilen güncelleştirmelerin işleri adayın eski başvuruları, profili ve özgeçmiş üzerinde temel alır.</span><span class="sxs-lookup"><span data-stu-id="c7506-159">The jobs that are recommended to a candidate are based on the candidate's past applications, profile, and resumes.</span></span>

>   [!NOTE] 
>   <span data-ttu-id="c7506-160">İş önerileri mesleki sitede en az 10 iş varsa ve aday profilini tamamlarsa gösterilir.</span><span class="sxs-lookup"><span data-stu-id="c7506-160">Job recommendations are shown only if at least 10 jobs are posted on the career site, and if the candidate has completed a profile.</span></span>

## <a name="apply-for-jobs"></a><span data-ttu-id="c7506-161">İşlere başvur</span><span class="sxs-lookup"><span data-stu-id="c7506-161">Apply for jobs</span></span>

<span data-ttu-id="c7506-162">Adaylar doğru işi bulduktan sonra, **İş ayrıntıları** sayfasında **Uygula** düğmesini kullanarak başvurabilirler.</span><span class="sxs-lookup"><span data-stu-id="c7506-162">After candidates find the right job, they can apply by using the **Apply** button on the **Job details** page.</span></span> <span data-ttu-id="c7506-163">Bu aşamada adaylar yeni bir profil oluşturabilir veya varolan profillerindeki ilgili bilgileri gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="c7506-163">At this point, candidates can either create a new profile or review the information in their existing profile.</span></span>
<span data-ttu-id="c7506-164">Adaylar gerekirse bir özgeçmiş ve sonra iş başvurusu gönderebilir.</span><span class="sxs-lookup"><span data-stu-id="c7506-164">Candidates can also upload a resume, as required, and then submit the job application.</span></span>

## <a name="check-application-status"></a><span data-ttu-id="c7506-165">Başvuru durumunu kontrol edin</span><span class="sxs-lookup"><span data-stu-id="c7506-165">Check application status</span></span>

<span data-ttu-id="c7506-166">Adaylar bir veya daha fazla işe başvurduğunda, açık ve kapalı uygulamalarını görüntülemek için sayfanın üstündeki gezinme çubuğundaki **Başvurular**'ı seçebilir.</span><span class="sxs-lookup"><span data-stu-id="c7506-166">After candidates apply for one or more jobs, they can select **Applications** on the navigation bar at the top of the page to view their open and closed applications.</span></span> <span data-ttu-id="c7506-167">Aday başvurularından birini açarken geçerli aşamayı ve tamamlaması gereken eylem öğelerini görür.</span><span class="sxs-lookup"><span data-stu-id="c7506-167">When candidates open one of their applications, they see the current stage and any pending action items that they must complete.</span></span> <span data-ttu-id="c7506-168">Örneğin, bir adayın yüz yüze görüşme tarihlerini belirtmesi gerekiyorsa sayfada kullanılabilir seçenekleri gösterilir.</span><span class="sxs-lookup"><span data-stu-id="c7506-168">For example, if a candidate must provide potential dates for an in-person interview, the page shows the available options.</span></span>

## <a name="internal-jobs"></a><span data-ttu-id="c7506-169">Dahili işler</span><span class="sxs-lookup"><span data-stu-id="c7506-169">Internal jobs</span></span>

<span data-ttu-id="c7506-170">Şu anda, dahili olarak işaretlenen ve Attract kariyer sitesine gönderilmeyen işler kariyer sitesinde görünmez.</span><span class="sxs-lookup"><span data-stu-id="c7506-170">Currently, jobs that are marked as internal and posted to the Attract career site don't appear on the career site.</span></span> <span data-ttu-id="c7506-171">Yalnızca Attract uygulamasından kopyalanabilecek doğrudan **Başvur** URL'sini kullanarak erişilebilirler.</span><span class="sxs-lookup"><span data-stu-id="c7506-171">They are only accessible using the direct **Apply** URL that can be copied from the Attract application.</span></span>
