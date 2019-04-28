---
title: LinkedIn Recruiter ile kaynak bulma
description: Bu konu, iş ve iş adayı önerileri almak için makine öğrenimini kullanma hakkında bilgi sağlar.
author: andreabichsel
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 4ac7a302e5bf589beb2b560b0ff5818e90c67139
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/19/2019
ms.locfileid: "859586"
---
# <a name="sourcing-with-linkedin-recruiter"></a><span data-ttu-id="6298b-103">LinkedIn Recruiter ile kaynak bulma</span><span class="sxs-lookup"><span data-stu-id="6298b-103">Sourcing with LinkedIn Recruiter</span></span>
[!include[banner](../includes/banner.md)]

<span data-ttu-id="6298b-104">LinkedIn, dünyanın en büyük beceri veritabanı ve çoğu zaman işe alanların doldurmak istediği işler için kaynak adaylar bulmak, adaylarla iletişim kurmak için kullandığı birincil sistemdir.</span><span class="sxs-lookup"><span data-stu-id="6298b-104">LinkedIn is the world’s largest talent database and often the primary system that recruiters use to find, communicate with, and source candidates for the jobs that recruiters are looking to fill.</span></span> <span data-ttu-id="6298b-105">LinkedIn Recruiter'in Dynamics 365 for Talent: Attract ile entegrasyonu, kullanıcıların işe alımını ve verileri iki sistem arasında eşit tutmayı kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="6298b-105">LinkedIn Recruiter integration with Dynamics 365 for Talent: Attract makes it easier for users to hire, and to keep the data in sync between the two systems.</span></span>

> [!NOTE]
> <span data-ttu-id="6298b-106">Kapsamlı işe alma eklentisi ve LinkedIn Recruiter lisans sayısı, Attract ile LinkedIn Recruiter kullanabilmek için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="6298b-106">You need the Comprehensive hiring add-on and LinkedIn Recruiter seats to be able to use LinkedIn Recruiter integration with Attract.</span></span>

## <a name="set-up-linkedin-recruiter-with-attract"></a><span data-ttu-id="6298b-107">Attract ile LinkedIn Recruiter ayarlamak</span><span class="sxs-lookup"><span data-stu-id="6298b-107">Set up LinkedIn Recruiter with Attract</span></span> 

<span data-ttu-id="6298b-108">LinkedIn Recruiter özellikleri kullanabilmek için önce Attract örneğinizle sözleşme düzeyi veya şirket düzeyinde erişim yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="6298b-108">Before you can use the LinkedIn Recruiter capabilities, you must configure contract-level or company-level access with your Attract instance.</span></span> <span data-ttu-id="6298b-109">Yapılandırma işlemini tamamlamak için LinkedIn Recruiter sözleşmenizden yönetici olan kullanıcıyla çalışmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="6298b-109">To complete the configuration process, you must work with the user who is an Admin on your LinkedIn Recruiter contract.</span></span> <span data-ttu-id="6298b-110">Attract ile LinkedIn Recruiter konfigüre etmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="6298b-110">Complete the following steps to configure LinkedIn Recruiter with Attract.</span></span>

1.  <span data-ttu-id="6298b-111">Bir yönetici olarak Attract oturumu açın ve  **Yönetici Ayarları**na gidin.</span><span class="sxs-lookup"><span data-stu-id="6298b-111">Sign in to Attract as an Admin and go to **Admin Settings**.</span></span>

2.  <span data-ttu-id="6298b-112">Sol bölmedeki **LinkedIn Entegrasyonu** sekmesine tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6298b-112">On the left pane, click the **LinkedIn Integration** tab.</span></span>

<span data-ttu-id="6298b-113">[![LinkedIn Recruiter tümleştirme başlatmak için Attract yönetici görünümü](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span><span class="sxs-lookup"><span data-stu-id="6298b-113">[![Attract Admin view to start LinkedIn Recruiter integration](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span></span>

3.  <span data-ttu-id="6298b-114">**Bağlan**a tıklayın, kurulumu başlatın, LinkedIn oturum açma işleminde kılavuzluk alın.</span><span class="sxs-lookup"><span data-stu-id="6298b-114">Click **Connect** to start the setup and be guided through the LinkedIn sign-in process.</span></span>

4.  <span data-ttu-id="6298b-115">Birde çok LinkedIn sözleşmelerinde lisansınız varsa, Attract sistemine bağlanmak istediğiniz sözleşmeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="6298b-115">If you have seats on multiple LinkedIn contracts, select the contract that you would like to connect to the Attract system.</span></span> <span data-ttu-id="6298b-116">LinkedIn sözleşmesinde tek bir lisans varsa, bu adım gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="6298b-116">If you have a seat on only one LinkedIn contract, this step will not be needed.</span></span>

5.  <span data-ttu-id="6298b-117">LinkedIn pencere öğesi gösterilen tümleştirmelerin listesiyle, Yönetici ayarlarını şimdi yükler.</span><span class="sxs-lookup"><span data-stu-id="6298b-117">The LinkedIn widget will now load in your Admin settings with the list of integrations shown.</span></span> <span data-ttu-id="6298b-118">**Recruiter System connect** altında **Talep**e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6298b-118">Under **Recruiter System connect**, click **Request**.</span></span>

<span data-ttu-id="6298b-119">[![LinkedIn Recruiter tümleştirme talebi başlatmak için Attract yönetici görünümü](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span><span class="sxs-lookup"><span data-stu-id="6298b-119">[![Attract Admin view to Request LinkedIn Recruiter integration](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span></span>

6.  <span data-ttu-id="6298b-120">Attract'tan tümleştirme istedikten sonra **Ortak hazır** olarak gösterilir ve **İşveren Yönetici ayarları**ndan açmaya hazır olur.</span><span class="sxs-lookup"><span data-stu-id="6298b-120">After the integration is requested from Attract, it will show as **Partner ready** and is ready to be turned on from **Recruiter Admin settings**.</span></span> <span data-ttu-id="6298b-121">Bu sayfada **Ortağa bildir** görürseniz birkaç saniye bekleyin, **Ortağa bildir**e tıklayın ve sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="6298b-121">If you see **Notify partner** on this page, wait a few seconds, click **Notify partner**, and then refresh the page.</span></span> <span data-ttu-id="6298b-122">Şimdi **Ortak hazır** olarak görünür.</span><span class="sxs-lookup"><span data-stu-id="6298b-122">It should now show as **Partner ready**.</span></span>

<span data-ttu-id="6298b-123">[![İsteklerin Attract tarafının tamamlandığını belirten Attract Yönetici görünümü](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span><span class="sxs-lookup"><span data-stu-id="6298b-123">[![Attract Admin view to indicate Attract side of requests have been completed](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span></span>

<span data-ttu-id="6298b-124">Sonraki adımı tamamlamak için LinkedIn Recruiter Sözleşmenizde bir Yönetici ayrıcalığı olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="6298b-124">To complete the next step, you need to have an Admin privilege on your LinkedIn Recruiter Contract.</span></span>

7.  <span data-ttu-id="6298b-125">LinkedIn için yönetici hesabı kullanarak oturum açın ve sağ üstteki LinkedIn Recruiter gidin.</span><span class="sxs-lookup"><span data-stu-id="6298b-125">Sign in to LinkedIn using the Admin account and go to LinkedIn Recruiter on the top right.</span></span> 

8. <span data-ttu-id="6298b-126">Ekranın üstündeki **Daha fazla** menüsünde **Yönetici ayarları**ve ardından **ATS** sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6298b-126">On the **More** menu at the top of the screen, click **Admin Settings**, and then click the **ATS** Tab.</span></span>

<span data-ttu-id="6298b-127">Attract sistem açılabilir birkaç seçenekle listede görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="6298b-127">The Attract system will be listed with a couple of options that can be turned on.</span></span>

9. <span data-ttu-id="6298b-128">Dışa aktarmak için yalnızca 1 tıklamayı etkinleştirmek isterseniz, **ATS göstergesinde** ve **ATS profil pencere öğesi**nde, **Şirket düzeyinde erişim**i seçin.</span><span class="sxs-lookup"><span data-stu-id="6298b-128">If you want to enable only 1-Click export for the **In-ATS indicator** and the **In-ATS Profile Widget**, select **Company-level access**.</span></span> <span data-ttu-id="6298b-129">Tüm şirket düzeyinde erişim özelliklerini artı InMail geçmişi, Not geçmişi ve InMail saplama profil erişimi etkinleştirmek isterseniz, **Sözleşme düzeyi erişimi** seçin.</span><span class="sxs-lookup"><span data-stu-id="6298b-129">If you want to enable all of Company-level access features plus InMail history, Notes history, and the InMail stub profile access, select **Contract-level access**.</span></span>

10. <span data-ttu-id="6298b-130">LinkedIn Recruiter **Yönetici-ATS** ayarlarından istediğiniz erişim düzeyini açın.</span><span class="sxs-lookup"><span data-stu-id="6298b-130">Turn on the desired access level from your LinkedIn Recruiter **Admin-ATS** settings.</span></span>

<span data-ttu-id="6298b-131">[![LinkedIn Recruiter Yönetici görünümünden Attract tümleştirmeyi aç](./media/EnableRSC.png)](./media/EnableRSC.png)</span><span class="sxs-lookup"><span data-stu-id="6298b-131">[![Turn on Attract integration from LinkedIn Recruiter Admin view](./media/EnableRSC.png)](./media/EnableRSC.png)</span></span>

12. <span data-ttu-id="6298b-132">AttractAdmin olarak Attract Yönetici ayarlarına dönün ve**LinkedIn tümleştirme** sekmesini seçin. LinkedIn pencere öğesi yüklemesini, seçilen erişim düzeyi açık olarak **Etkin** şeklinde görmeniz gerkeir.</span><span class="sxs-lookup"><span data-stu-id="6298b-132">Go back to Attract Admin Settings as an AttractAdmin and select the **LinkedIn integration** tab. You should now see the LinkedIn widget load showing **Enabled** with the selected access level turned on.</span></span>

<span data-ttu-id="6298b-133">[![LinkedIn Recruiter tümleştirme tamamlandı](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span><span class="sxs-lookup"><span data-stu-id="6298b-133">[![LinkedIn Recruiter integration complete](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span></span>

## <a name="using-linkedin-recruiter-capabilities"></a><span data-ttu-id="6298b-134">LinkedIn Recruiter yeterliliklerini kullanmak</span><span class="sxs-lookup"><span data-stu-id="6298b-134">Using LinkedIn Recruiter capabilities</span></span>

<span data-ttu-id="6298b-135">LinkedIn Recruiter özellikleri Attract Yönetici tarafından etkinleştirildiğinde iş alın yöneticileri ve işverenlerin erişimine açık olur.</span><span class="sxs-lookup"><span data-stu-id="6298b-135">After LinkedIn Recruiter capabilities has been enabled by the Attract Admin it is available for hiring managers and recruiters to access.</span></span> <span data-ttu-id="6298b-136">LinkedIn hesabınızı bu özellikleri kullanmak için **kullanıcı ayarları** altından bağlayın.</span><span class="sxs-lookup"><span data-stu-id="6298b-136">To use these capabilities, connect your LinkedIn account under **User Settings**.</span></span> <span data-ttu-id="6298b-137">Hem yönetici hem de kullanıcı ayarları bağlandıktan sonra birkaç özellik kullanılabilir olacaktır.</span><span class="sxs-lookup"><span data-stu-id="6298b-137">Several capabilities will be available after both the Admin and User settings have been connected.</span></span>

### <a name="in-ats-profile-widget"></a><span data-ttu-id="6298b-138">ATS profil pencere öğesi</span><span class="sxs-lookup"><span data-stu-id="6298b-138">In-ATS profile widget</span></span>

<span data-ttu-id="6298b-139">Adayın LinkedIn profilini Attract içinde görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6298b-139">You can view the candidate’s LinkedIn profile in Attract.</span></span> <span data-ttu-id="6298b-140">LinkedIn pencere öğesi, LinkedIn kullanıcı bilgileri ATS bilgileriyle eşleştiğinde aday profili görüntüler.</span><span class="sxs-lookup"><span data-stu-id="6298b-140">The LinkedIn widget will display the candidate profile when the ATS information matches the LinkedIn information of its users.</span></span>

<span data-ttu-id="6298b-141">Profil görüntülemek için aday profiline işten veya beceri havuzundan gidin.</span><span class="sxs-lookup"><span data-stu-id="6298b-141">To view a profile, go the candidate profile either from a job or talent pool.</span></span> <span data-ttu-id="6298b-142">Aday profilinde **LinkedIn** sekmesini seçin ve profil pencere öğesi yüklenir.</span><span class="sxs-lookup"><span data-stu-id="6298b-142">In the candidate profile, select the **LinkedIn** tab and the profile widget will load.</span></span> <span data-ttu-id="6298b-143">Bu sayfadan LinkedIn Recruiter projelerinize aday da kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6298b-143">You can also save the candidate to your LinkedIn Recruiter projects from this page.</span></span>
1. <span data-ttu-id="6298b-144">LinkedIn, eşleşmeyi e-posta ve LinkedIn üye kimliğ (tam eşleşme) arasında bulduysa, adayın profili gösterilecektir.</span><span class="sxs-lookup"><span data-stu-id="6298b-144">If LinkedIn found the match based on email and LinkedIn member ID (exact match), the candidate's profile will be shown.</span></span> <span data-ttu-id="6298b-145">Kullanıcının bağlantı Kes/profile seçeneği hala vardır.</span><span class="sxs-lookup"><span data-stu-id="6298b-145">The user still has an option to link/unlink the profile.</span></span>

2. <span data-ttu-id="6298b-146">LinkedIn, adayı e-posta veya üye kimliğine dayanarak bulamadıysa, aday adına dayanarak olası aday eşleşmelerinin bir listesini gösterir ve kullanıcı bunlar arasından birini seçip profili bağlantılayabilir.</span><span class="sxs-lookup"><span data-stu-id="6298b-146">If LinkedIn cannot find the candidate based on their email or member ID, it will show a list of possible candidate matches based on candidate name and the user can choose one of them and link the profile.</span></span>  

3. <span data-ttu-id="6298b-147">LinkedIn, adına dayanarak herhangi bir aday bulamazsa, eşleşme bulunamadı döndürür.</span><span class="sxs-lookup"><span data-stu-id="6298b-147">If LinkedIn cannot find any candidate based on the name, it will return that no match was found.</span></span>

### <a name="1-click-export"></a><span data-ttu-id="6298b-148">1 tıkla dışa aktarma</span><span class="sxs-lookup"><span data-stu-id="6298b-148">1-click export</span></span> 

<span data-ttu-id="6298b-149">LinkedIn'de aday kaynağı bulurken a.ık olan işlere 1 tıklamayla aday dışa aktarımı yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6298b-149">While sourcing candidates in LinkedIn, you can 1-click export the candidate to the jobs that you currently have open.</span></span> <span data-ttu-id="6298b-150">1 tıkla dışa aktarma için aşağıdaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="6298b-150">Complete the following steps for a 1-click export.</span></span> <span data-ttu-id="6298b-151">Aşağıdaki adımları tamamlamadan önce iş için işe alma yöneticisi veya İşveren atanmış ve işin **Aday müşteri** aşaması olduğundan emin olun</span><span class="sxs-lookup"><span data-stu-id="6298b-151">Before you complete these steps, verify that you are a assigned the role of Hiring manager or Recruiter for the job and that the job has a **Prospect** stage.</span></span>

1.  <span data-ttu-id="6298b-152">İş oluşturun, uygun roller atayın ve işi etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="6298b-152">Create the job, assign the appropriate roles, and activate the job.</span></span>

2.  <span data-ttu-id="6298b-153">İş etkinleştirildiğinde LinkedIn Recruiter'e ilerleyin.</span><span class="sxs-lookup"><span data-stu-id="6298b-153">When the job is activated, navigate to LinkedIn Recruiter.</span></span>

3.  <span data-ttu-id="6298b-154">Aradığınız adayı bulun ve profiline gidin.</span><span class="sxs-lookup"><span data-stu-id="6298b-154">Find the candidate that you are looking for and go to their profile.</span></span>

4.  <span data-ttu-id="6298b-155">Kişi kartında iş arama kutusunu kullanıp iş başlığı veya Attract'ta etkinleştirilmiş İş Kodu kullanarak işi bulun.</span><span class="sxs-lookup"><span data-stu-id="6298b-155">Using the job search box in the contact card, find the job using the title or the Job ID that was activated in Attract.</span></span> <span data-ttu-id="6298b-156">İş bulamazsanız, **ATS değişikliği**ne tıklayarak doğru Attract örneği bulun.</span><span class="sxs-lookup"><span data-stu-id="6298b-156">If you don’t find the job, click **Change ATS** to find the correct Attract instance.</span></span>

5. <span data-ttu-id="6298b-157">İş seçtikten sonra **dışa aktar**a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6298b-157">After the job is selected, click **Export**.</span></span> <span data-ttu-id="6298b-158">Aday Attract tarafından getirilir.</span><span class="sxs-lookup"><span data-stu-id="6298b-158">The candidate is now fetched by Attract.</span></span>

6.  <span data-ttu-id="6298b-159">Attract'a gidin ve ilgili işi açın.</span><span class="sxs-lookup"><span data-stu-id="6298b-159">Go to Attract and open the respective job.</span></span> <span data-ttu-id="6298b-160">İşin **Aday müşteri** aşamasında dışa aktardığınız adayı bulursunuz.</span><span class="sxs-lookup"><span data-stu-id="6298b-160">You will find the candidate that you just exported in the **Prospect** stage of the job.</span></span>

### <a name="in-ats-indicator"></a><span data-ttu-id="6298b-161">ATS göstergesinde</span><span class="sxs-lookup"><span data-stu-id="6298b-161">In-ATS indicator</span></span> 

<span data-ttu-id="6298b-162">LinkedIn Recruiter kullanarak, adayın kuruluşunuzdaki diğer işlere başvurup başvurmadığını izler, iş başvurularının hangi aşamalarında olduklarına bakabilir ve LinkedIn Recruiter'de Attract'tan gelen geri bildirimlerle yorumları görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6298b-162">Using LinkedIn recruiter, you can track whether a candidate has applied to other jobs in your organization, look at where they are in different stages of job applications, and view the feedback and comments from Attract in LinkedIn Recruiter.</span></span>

1.  <span data-ttu-id="6298b-163">LinkedIn Recruiter'i açın ve aradığınız aday profilini bulun.</span><span class="sxs-lookup"><span data-stu-id="6298b-163">Open LinkedIn Recruiter and locate the candidate profile that you are looking for.</span></span>

2.  <span data-ttu-id="6298b-164">Adayın profilinde **ATS'de** bölümünü açmak için aşağı kaydırın.</span><span class="sxs-lookup"><span data-stu-id="6298b-164">Scroll down to view the **In-ATS** section on the candidate’s profile.</span></span>

3.  <span data-ttu-id="6298b-165">Bu pencere öğesini, LinkedIn Recruiter görünümündeki Attract'ta mevcut olan aday hakkındaki bilgileri görüntülemek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6298b-165">You can use this widget to view all of the information about the candidate that’s present in Attract from within the LinkedIn Recruiter view.</span></span>

4.  <span data-ttu-id="6298b-166">**İşler ve durumlarını** seçerek parçası oldukları işleri, son durumu ve her işte nasıl ilerlediklerini görün.</span><span class="sxs-lookup"><span data-stu-id="6298b-166">Select the **Jobs & Statuses** tab to see jobs they are part of, the latest status, and how they have been moving against each job.</span></span>

5.  <span data-ttu-id="6298b-167">**görüşme geribildirimi** sekmesini seçerek görüşmecilerin Attract'a gönderdiği geri bildirimleri görün.</span><span class="sxs-lookup"><span data-stu-id="6298b-167">Select the **Interview Feedback** tab to see feedback that the interviewers have submitted in Attract.</span></span>

6.  <span data-ttu-id="6298b-168">**Notlar** sekmesini seçerek Attract'ta bu başvuran için yakalanan notları görün.</span><span class="sxs-lookup"><span data-stu-id="6298b-168">Select the **Notes** tab to see notes that have been captured for this applicant in Attract.</span></span>

> [!NOTE]
> <span data-ttu-id="6298b-169">Aday, ön aday aşamasını geçemediyse aday ve başvuru verisi, LinkedIn Recruiter eşitlenmez.</span><span class="sxs-lookup"><span data-stu-id="6298b-169">Candidate and application data will not be synced to LinkedIn Recruiter if the candidate hasn't moved past the prospect stage.</span></span>

### <a name="inmail-history"></a><span data-ttu-id="6298b-170">InMail geçmişi</span><span class="sxs-lookup"><span data-stu-id="6298b-170">InMail history</span></span>

<span data-ttu-id="6298b-171">LinkedIn InMail geçmişi, LinkedIn Recruiter ile sözleşme düzeyinde erişimle kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6298b-171">The LinkedIn InMail history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="6298b-172">Etkin olduğunda, adayla olan tüm InMail geçmişi görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6298b-172">When it is enabled, you can view your entire InMail history with the candidate.</span></span> <span data-ttu-id="6298b-173">Adayla InMail değişimi yapan kuruluşunuzdan diğer kullanıcıları görebilir ancak aralarındaki mesajları göremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="6298b-173">You can also see who else from your organization has exchanged InMail with the candidate, however you can't view the messages between them.</span></span>

<span data-ttu-id="6298b-174">InMail geçmişini görüntülemek için adayın profiline gidin. **LinkedIn** sekmesine gidin ve geçmişini görüntülemek için aşağı aydırma yapın.</span><span class="sxs-lookup"><span data-stu-id="6298b-174">To view InMail history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="6298b-175">Aday ile bir sohbet gerçekleştirdiyseniz, InMail geçmişini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6298b-175">You can view InMail history if you have had a discussion with the candidate.</span></span> <span data-ttu-id="6298b-176">Her birkaç saatte bir InMail gelen iletileri Attract ile eşitlenecektir.</span><span class="sxs-lookup"><span data-stu-id="6298b-176">The messages from InMail will sync with Attract every couple of hours.</span></span>

### <a name="notes-history"></a><span data-ttu-id="6298b-177">Notlar geçmişi</span><span class="sxs-lookup"><span data-stu-id="6298b-177">Notes history</span></span> 

<span data-ttu-id="6298b-178">LinkedIn notlar geçmişi, LinkedIn Recruiter ile sözleşme düzeyinde erişimle kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6298b-178">The LinkedIn notes history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="6298b-179">Etkinleştirildiğinde, aday hakkında kurumunuzda farklı işverenler tarafından yakalanan notları görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6298b-179">When it is enabled, you can view the notes that have been captured about the candidate by different recruiters from your organization.</span></span>

<span data-ttu-id="6298b-180">Notlar geçmişini görüntülemek için adayın profiline gidin. **LinkedIn** sekmesine gidin ve geçmişini görüntülemek için aşağı aydırma yapın.</span><span class="sxs-lookup"><span data-stu-id="6298b-180">To view Notes history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="6298b-181">LinkedIn Recruiter'dan aday hakkındaki tüm notları görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6298b-181">You can view all the notes about the candidate from LinkedIn Recruiter.</span></span>

### <a name="inmail-stub-profile"></a><span data-ttu-id="6298b-182">InMail saplama profili</span><span class="sxs-lookup"><span data-stu-id="6298b-182">InMail stub profile</span></span>

<span data-ttu-id="6298b-183">InMail saplama profili, LinkedIn Recruiter ile sözleşme düzeyinde erişimle kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6298b-183">The InMail stub profile is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="6298b-184">Adaylar kuruluşunuzdaki herhangi bir kullanıcıyla LinkedIn profillerini paylaşmayı kabul ederse, adayları Attract'ta takip edebilir ve her aday için yeni bir aday kaydı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6298b-184">If candidates agree to share their LinkedIn profiles with any user in your organization, you can track the candidates in Attract and a new candidate record will be created for each candidate.</span></span> <span data-ttu-id="6298b-185">Aday, sistemde bir e-posta adresi ile zaten mevcutsa veya adresini işe alımcı ile paylaşmayı seçmişse, adayın e-posta adresini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6298b-185">You can view candidate's email address if the candidate already exists in the system with an email address or has chosen to share their address with the recruiter.</span></span>

<span data-ttu-id="6298b-186">Aday listesini görüntülemek için **Beceri havuzları**na gidin, sistem tarafından oluşturulan LinkedIn beceri havuzunu görün.</span><span class="sxs-lookup"><span data-stu-id="6298b-186">To view the list of candidates, go to **Talent pools** to see a system-created LinkedIn talent pool.</span></span> <span data-ttu-id="6298b-187">Bu beceri havuzu, LinkedIn'den alınan aday ve alt profilleri listesini içerir. Adayın adını ve soyadını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6298b-187">This talent pool contains the list candidates and their stub profiles as received from LinkedIn, showing the candidate's first name and last name.</span></span> <span data-ttu-id="6298b-188">Adayın e-posta kodu, aday e-posta adresini paylaşmayı seçtiyse görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="6298b-188">The candidate’s email ID will be displayed if the candidate had chosen to share their email address.</span></span>
