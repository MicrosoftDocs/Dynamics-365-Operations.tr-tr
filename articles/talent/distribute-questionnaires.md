---
title: "Bir anketi dağıtın ve tamamlayın."
description: "Bu konu, tasarladığınız anketlerin onları tamamlayacak kişi veya kişi grubu için kullanılabilir olması için onları nasıl dağıtacağınızı açıklar."
author: kherr75
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 3954ec2a06c7a2ec964b656e088f8c677094c963
ms.contentlocale: tr-tr
ms.lasthandoff: 02/07/2018

---

# <a name="distribute-and-complete-a-questionnaire"></a><span data-ttu-id="a4833-103">Bir anketi dağıtın ve tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="a4833-103">Distribute and complete a questionnaire</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="a4833-104">Bu konu, tasarladığınız anketlerin onları tamamlayacak kişi veya kişi grubu için kullanılabilir olması için onları nasıl dağıtacağınızı açıklar.</span><span class="sxs-lookup"><span data-stu-id="a4833-104">This topic explains how distribute the questionnaires that you design, so that they are available to the person or group of people who will complete them.</span></span> 

<span data-ttu-id="a4833-105">Bir anketi dağıtmanın birden çok yolu vardır:</span><span class="sxs-lookup"><span data-stu-id="a4833-105">There are multiple ways to distribute a questionnaire:</span></span>

-   <span data-ttu-id="a4833-106">Anketi aktif olarak işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="a4833-106">Mark the questionnaire as active.</span></span> <span data-ttu-id="a4833-107">Ardından anket, erişimi kısıtlamak için bir anket grubu ayarlanmadığı sürece tüm çalışanlar tarafından kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a4833-107">The questionnaire is then available to all employees, unless a questionnaire group is set up to restrict access to it.</span></span>
-   <span data-ttu-id="a4833-108">Bir anket grubuna haklar atayın.</span><span class="sxs-lookup"><span data-stu-id="a4833-108">Assign rights to a questionnaire group.</span></span> <span data-ttu-id="a4833-109">Anket daha sonra seçili grubun tüm üyeleri tarafından kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a4833-109">The questionnaire is then available to all members of the selected group.</span></span>
-   <span data-ttu-id="a4833-110">Planlı yanıt oturumları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a4833-110">Create planned answer sessions.</span></span> <span data-ttu-id="a4833-111">Anket daha sonra yalnızca belirli bir kişi tarafından kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a4833-111">The questionnaire is then available only to a particular person.</span></span>
-   <span data-ttu-id="a4833-112">Bir planlama oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a4833-112">Create a schedule.</span></span> <span data-ttu-id="a4833-113">Anket daha sonra birden çok kişi tarafından kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a4833-113">The questionnaire can then be available to multiple people.</span></span>

## <a name="marking-a-questionnaire-as-active"></a><span data-ttu-id="a4833-114">Anketi aktif olarak işaretlemek.</span><span class="sxs-lookup"><span data-stu-id="a4833-114">Marking a questionnaire as active</span></span>
<span data-ttu-id="a4833-115">**Soru formları** sayfasındaki **Etkin** alanı **Evet** olarak ayarlayarak, soru formlarını tüm personelin tamamlamaları üzere kullanılabilir hale getirirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4833-115">By setting the **Active** field to **Yes** on the **Questionnaires** page, you make the questionnaire available for all employees to complete.</span></span> <span data-ttu-id="a4833-116">Yanıtlayanlar, soru formunu birden çok kez tamamlayabilirler.</span><span class="sxs-lookup"><span data-stu-id="a4833-116">Respondents can complete the questionnaire multiple times.</span></span> <span data-ttu-id="a4833-117">Bu işlev, yıl boyunca sürekli geribildirim toplamak istiyorsanız yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="a4833-117">This functionality is useful if you want to gather continual feedback throughout the year.</span></span> <span data-ttu-id="a4833-118">Örneğin, çalışanların kafeteryadaki öğle yemeği hizmeti hakkında geribildirim vermek için kullanacağı bir anket yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4833-118">For example, you can make a questionnaire that employees use to give feedback about the lunch service in the cafeteria.</span></span>

## <a name="questionnaire-groups"></a><span data-ttu-id="a4833-119">Soru formu grupları</span><span class="sxs-lookup"><span data-stu-id="a4833-119">Questionnaire groups</span></span>
<span data-ttu-id="a4833-120">Anket grupları ayarlayabilir ve ardından anketin dağıtılması gereken yanıtlayanları ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4833-120">You can set up questionnaire groups and then include the respondents that a questionnaire should be distributed to.</span></span> 

<span data-ttu-id="a4833-121">Aşağıdaki sayfalardan anket grupları oluşturabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="a4833-121">You can create questionnaire groups from the following pages:</span></span>

-   <span data-ttu-id="a4833-122">**Anket grupları**– Yalnızca bir anket grubundaki bireyler seçili anketi tamamlayabilir.</span><span class="sxs-lookup"><span data-stu-id="a4833-122">**Questionnaire groups** – Only individuals in a questionnaire group can complete a selected questionnaire.</span></span> <span data-ttu-id="a4833-123">Örneğin, hedef kitleniz yüklenicilerse, bu yanıtlayanlara özel bir anket grubu oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="a4833-123">For example, your intended audience is contractors, so you create a questionnaire group that is specific to those respondents.</span></span>
-   <span data-ttu-id="a4833-124">**Anket grubu üyeleri** – Anket gruplarına kişiler ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4833-124">**Questionnaire group members** – You can add people to the questionnaire groups.</span></span>

<span data-ttu-id="a4833-125">Bir soru formu grubunu bir soru formuna eklemek için **Soru formları** sayfasında, **Kullanıcı hakları** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4833-125">To assign a questionnaire group to a questionnaire, on the **Questionnaires** page, click **User rights**.</span></span> <span data-ttu-id="a4833-126">Soru formu etkin olarak kaydedildikten sonra, soru formu grubunun üyeleri, soru formunu tamamlayabilirler.</span><span class="sxs-lookup"><span data-stu-id="a4833-126">After the questionnaire is saved as active, the members of the questionnaire group can complete the questionnaire.</span></span> <span data-ttu-id="a4833-127">Bu işlev, bir soru formunu daha büyük bir gruba açmadan önce seçili kişiler grubunda denemek istiyorsanız veya bir soru formunu çok özel bir hedef kitleye hedeflemek istiyorsanız yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="a4833-127">This functionality is helpful if you want to test a questionnaire on a select group of people before you roll it out to a larger group, or if you want to target a questionnaire to a very specific audience.</span></span>

## <a name="planned-answer-sessions-in-a-questionnaire"></a><span data-ttu-id="a4833-128">Soru formu başına planlanan yanıt oturumu</span><span class="sxs-lookup"><span data-stu-id="a4833-128">Planned answer sessions in a questionnaire</span></span>
<span data-ttu-id="a4833-129">Planlı yanıt oturumları tasarladığınız ve yanıtlayanlarını seçtiğiniz anketlerdir.</span><span class="sxs-lookup"><span data-stu-id="a4833-129">Planned answer sessions are questionnaires that you've designed and selected the respondents for.</span></span> 

> <span data-ttu-id="a4833-130">**Not** Planlı yanıt oturumları ayarlamadan önce bir anket tasarlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="a4833-130">**Note** Before you can set up planned answer sessions, you must design a questionnaire.</span></span> 

<span data-ttu-id="a4833-131">**Planlı yanıt oturumu** sayfasında, tek bir çalışan için planlı bir yanıt oturumu oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4833-131">On the **Planned answer session** page, you can create a planned answer session for an individual employee.</span></span> <span data-ttu-id="a4833-132">Sayfadaki liste tüm planlı anketleri görüntüler.</span><span class="sxs-lookup"><span data-stu-id="a4833-132">The list on the page displays all planned questionnaires.</span></span> 

<span data-ttu-id="a4833-133">Planlı yanıt oturumları aynı zamanda **Anket planlamaları** sayfasında kullanılır, burada birden çok kişi için anketler planlayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="a4833-133">Planned answer sessions are also used on the **Questionnaire schedules** page, where you can plan questionnaires for multiple people:</span></span>

-   <span data-ttu-id="a4833-134">Çalışanlar</span><span class="sxs-lookup"><span data-stu-id="a4833-134">Employees</span></span>
-   <span data-ttu-id="a4833-135">Kurs katılımcıları</span><span class="sxs-lookup"><span data-stu-id="a4833-135">Course participants</span></span>
-   <span data-ttu-id="a4833-136">Organizasyon birimleri</span><span class="sxs-lookup"><span data-stu-id="a4833-136">Organizational units</span></span>

<span data-ttu-id="a4833-137">Herkes anketi yalnızca bir kez yanıtlayabilir.</span><span class="sxs-lookup"><span data-stu-id="a4833-137">Each person can answer the questionnaire only one time.</span></span>

## <a name="scheduling-a-questionnaire"></a><span data-ttu-id="a4833-138">Bir anket planlama</span><span class="sxs-lookup"><span data-stu-id="a4833-138">Scheduling a questionnaire</span></span>
<span data-ttu-id="a4833-139">Birden fazla yanıtlayan için isteğe bağlı olarak bir anket planlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4833-139">You can optionally schedule a questionnaire for multiple respondents.</span></span>

### <a name="planning-types"></a><span data-ttu-id="a4833-140">Planlama tipleri</span><span class="sxs-lookup"><span data-stu-id="a4833-140">Planning types</span></span>

<span data-ttu-id="a4833-141">Birden fazla yanıtlayan için planlı yanıt oturumları planlamak istiyorsanız planlama türleri gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a4833-141">Planning types are required if you want to schedule planned answer sessions for multiple respondents.</span></span> <span data-ttu-id="a4833-142">Planlama tipleri, anket planlamalarını sınıflandırmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a4833-142">Planning types are used to classify questionnaire schedules.</span></span> <span data-ttu-id="a4833-143">Örneğin, aşağıdaki amaçlarla anketler planlayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="a4833-143">For example, you can schedule questionnaires for the following purposes:</span></span>

-   <span data-ttu-id="a4833-144">Değerlendirme</span><span class="sxs-lookup"><span data-stu-id="a4833-144">Evaluation</span></span>
-   <span data-ttu-id="a4833-145">Anket</span><span class="sxs-lookup"><span data-stu-id="a4833-145">Survey</span></span>
-   <span data-ttu-id="a4833-146">Test etme</span><span class="sxs-lookup"><span data-stu-id="a4833-146">Testing</span></span>

<span data-ttu-id="a4833-147">Bir naket planlaması için planlama türlerini **Anket planlamaları** sayfasında belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4833-147">You can specify planning types for a questionnaire schedule on the **Questionnaire schedules** page.</span></span>

### <a name="reference-types-for-questionnaire"></a><span data-ttu-id="a4833-148">Anket için referans türleri</span><span class="sxs-lookup"><span data-stu-id="a4833-148">Reference types for questionnaire</span></span>

<span data-ttu-id="a4833-149">Bir anket planlarken seçebileceğiniz yanıtlayanlar için ölçütleri girmek için referans türlerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4833-149">You can use reference types to enter criteria for the respondents that you might select when you schedule a questionnaire.</span></span> 

<span data-ttu-id="a4833-150">**Referans türleri** sayfasını kullanarak bir anket için referans türleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a4833-150">Use the **Reference types** page to set up reference types for a questionnaire.</span></span> <span data-ttu-id="a4833-151">Her referans türü Microsoft Dynamics 365 for Finance and Operations'ta bir tabloya karşılık gelir.</span><span class="sxs-lookup"><span data-stu-id="a4833-151">Each reference type corresponds to a table in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="a4833-152">Anket planlamaları oluşturduğunuzda, anketin ilişkilendirileceği bir dizi kayıt veya tek tek kayıtları belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4833-152">When you create questionnaire schedules, you can specify individual records in the table or a range of records that the questionnaire will be associated with.</span></span> 

<span data-ttu-id="a4833-153">Örneğin, kurslar tablo seçerseniz, anketin hangi özel kurs için olacağına karar verebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4833-153">For example, if you select the Courses table, you can decide which specific course the questionnaire will be for.</span></span> <span data-ttu-id="a4833-154">Kurslar tablosu için bir referans belirlerken, **Kurslar** sayfasındaki bazı alanlar ve düğmeler kullanılabilir hale gelir.</span><span class="sxs-lookup"><span data-stu-id="a4833-154">When you set up a reference for the Courses table, some fields and buttons on the **Courses** page become available.</span></span>

### <a name="questionnaire-schedules"></a><span data-ttu-id="a4833-155">Soru formu planlamaları</span><span class="sxs-lookup"><span data-stu-id="a4833-155">Questionnaire schedules</span></span>

<span data-ttu-id="a4833-156">Soru formu tablolarını, bir kullanıcı grubu için bir referans türüne dayalı olarak çoklu planlı yanıt oturumları oluşturmak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4833-156">You can use questionnaire schedules to generate multiple planned answer sessions for a group of users, based on a reference type.</span></span> <span data-ttu-id="a4833-157">**Soru formu tabloları** sayfasında zamanlamayı oluşturmak.</span><span class="sxs-lookup"><span data-stu-id="a4833-157">Create a schedule on the **Questionnaire schedules** page.</span></span> <span data-ttu-id="a4833-158">Zamanlamayı kategorize etmek için planlama türünü ve sistemi, belirli kullanıcılar için sorgulamak üzere referans türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="a4833-158">Select the planning type to categorize the schedule, and also select the reference type that should be used to query the system for specific users.</span></span> <span data-ttu-id="a4833-159">Örneğin, referans türünü Kurslar tablosu olarak ayarlarsanız, **Referans** alanında belirli bir kursu seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4833-159">For example, if you set the reference type to the Courses table, you can select a specific course in the **Reference** field.</span></span> 

<span data-ttu-id="a4833-160">Anketi ve diğer ölçütleri seçmek için **Kurulum ayrıntıları** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a4833-160">Click **Setup details** to select the questionnaire and other criteria.</span></span> <span data-ttu-id="a4833-161">Örneğin, soru formu bir eğitmenin değerlendirmesiyse, eğitmenin adını bir kriter olarak belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a4833-161">For example, specify the instructor's name as a criterion if the questionnaire is an evaluation of the instructor.</span></span> <span data-ttu-id="a4833-162">Kurulum ayarlarını girmeyi bitirdikten sonra, sistem planlanmış yanıtlama oturumlarını, bu sorguya dahil edilmiş kullanıcılar için oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a4833-162">After you've finished entering the setup details, the system generates planned answer sessions for the users that are included in the query.</span></span> 

<span data-ttu-id="a4833-163">Bir zamanlama için yanıt oturumlarını görüntülemek için **Planlı yanıt oturumları** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a4833-163">Click **Planned answer sessions** to view the answer sessions for the schedule.</span></span> <span data-ttu-id="a4833-164">Ardından ek planlı yanıt oturumlarını el ile oluşturabilir veya yanıtlanmamış olan planlı yanıt oturumlarını silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4833-164">You can then manually create additional planned answer sessions or delete planned answer sessions that haven't been answered.</span></span> 

<span data-ttu-id="a4833-165">Anketi ilgili planlı yanıt oturumlarındaki kullanıcılar için kullanılabilir hale getirmek için **İşlevler** &gt; **Başlat** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a4833-165">Click **Functions** &gt; **Start** to make the questionnaire available to the users in related planned answer sessions.</span></span> <span data-ttu-id="a4833-166">Anketin tamamlanmış yanıtlarını görüntülemek için **Yanıtlar** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a4833-166">Click **Answers** to view the completed responses to the questionnaire.</span></span> <span data-ttu-id="a4833-167">İsteğe bağlı olarak, anket zamanlama ayarlarını, Planlı yanıt oturumlarını ve yeni bir anket zamanlama yanıtlarını kopyalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4833-167">You can optionally copy the questionnaire schedule settings, planned answer sessions, and answers to a new questionnaire schedule.</span></span>

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a><span data-ttu-id="a4833-168">Yanıtlayanları onlar için kullanılabilir olan anketler hakkında bilgilendirin</span><span class="sxs-lookup"><span data-stu-id="a4833-168">Notifying respondents about questionnaires that are available to them</span></span>
<span data-ttu-id="a4833-169">Bir anketi dağıttığınızda, yanıtlayanları anketlerin onlar için kullanılabilir olduğu hakkında bilgilendirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="a4833-169">When you distribute a questionnaire, you must notify respondents that questionnaires are available to them.</span></span> 

### <a name="notifying-respondents-about-a-planned-answer-session"></a><span data-ttu-id="a4833-170">Yanıtlayanları planlı bir yanıt oturumu hakkında bilgilendirin</span><span class="sxs-lookup"><span data-stu-id="a4833-170">Notifying respondents about a planned answer session</span></span>

<span data-ttu-id="a4833-171">Planlı bir yanıt oturumu kullanıyorsanız, kişiyi telefon ya da e-postayla doğrudan bilgilendirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="a4833-171">If you use a planned answer session, you must notify the person directly, such as by telephone or email.</span></span>

### <a name="notifying-respondents-about-a-scheduling"></a><span data-ttu-id="a4833-172">Yanıtlayanları bir planlama hakkında bilgilendirin</span><span class="sxs-lookup"><span data-stu-id="a4833-172">Notifying respondents about a scheduling</span></span>

<span data-ttu-id="a4833-173">Bir ankete atanmış olan tüm yanıtlayanlara bir e-posta hazırlamak ve göndermek için **Anket planlamaları** sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="a4833-173">Use the **Questionnaire schedules** page to prepare and send email to all respondents who are assigned to the questionnaire.</span></span> <span data-ttu-id="a4833-174">**Personel self servisi için e-posta** sekmesinde e-posta metnini girin. Zamanlama başladıktan sonra, e-postayı oluşturmak ve alıcılara göndermek için **İşlevler** &gt; **E-posta gönder** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4833-174">Enter the email text on the **E-mail for employee self service** tab. After the schedule has been started, click **Functions** &gt; **Send e-mail** to generate and send the email to the respondents.</span></span> <span data-ttu-id="a4833-175">Yanıtlayanlar web sitesinde oturum açarak soru formunu doldurabilirler.</span><span class="sxs-lookup"><span data-stu-id="a4833-175">Respondents can then sign in to the website and complete the questionnaire.</span></span> 

> <span data-ttu-id="a4833-176">**Not** E-posta işlevlerini kullanmadan önce BT yöneticiniz e-posta ayarlarını **E-posta parametreleri** sayfasında girmelidir.</span><span class="sxs-lookup"><span data-stu-id="a4833-176">**Note** Before you can use the email functionality, your IT administrator must enter the email settings on the **E-mail parameters** page.</span></span>

## <a name="ending-a-scheduled-questionnaire"></a><span data-ttu-id="a4833-177">Planlanmış bir anketi sonlandırma</span><span class="sxs-lookup"><span data-stu-id="a4833-177">Ending a scheduled questionnaire</span></span>
<span data-ttu-id="a4833-178">Tüm yanıtlayan kişiler kendilerine atanmış soru oturumlarını tamamladıktan sonra çizelgelenmiş bir soru formunu sonlandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4833-178">You can end a scheduled questionnaire after all respondents have completed their assigned answer sessions.</span></span> <span data-ttu-id="a4833-179">Planlamış bir anket sonlandırıldıktan sonra, ayarlarını yeni bir planlamaya kopyalayamazsınız.</span><span class="sxs-lookup"><span data-stu-id="a4833-179">After a scheduled questionnaire is ended, you can't copy its settings to a new schedule.</span></span> 

> <span data-ttu-id="a4833-180">**Not** Bir veya daha fazla yanıtlayan anketi tamamlamadıysa, buna rağmen planlamayı sonlandırmak istiyorsanız, öncelikle bu yanıtlayanları  **Planlı yanıt oturumu** sayfasından silmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="a4833-180">**Note** If one or more respondents haven't completed the questionnaire, but you still want to end the scheduling, you must first delete those respondents from the list on the **Planned answer session** page.</span></span> <span data-ttu-id="a4833-181">Ardından planlamayı sonlandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4833-181">You can then end the schedule.</span></span>

## <a name="completing-questionnaires"></a><span data-ttu-id="a4833-182">Soru formlarını tamamlama</span><span class="sxs-lookup"><span data-stu-id="a4833-182">Completing questionnaires</span></span>
<span data-ttu-id="a4833-183">Bir anketi tasarladıktan ve dağıttıktan sonra, anket seçili yanıtlayanlar tarafından tamamlanabilir.</span><span class="sxs-lookup"><span data-stu-id="a4833-183">After you've designed and distributed a questionnaire, the questionnaire can be completed by selected respondents.</span></span> <span data-ttu-id="a4833-184">İki yerleşimden kullanabileceğiniz soru formlarını tamamlayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="a4833-184">You can complete the questionnaires that are available to you from two locations:</span></span>

-   <span data-ttu-id="a4833-185">Gezinti bölmesinde **Anketler** &gt; **Dağıt** &gt; **Bir anketi tamamlamak** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a4833-185">In the navigation pane, click **Questionnaires** &gt; **Distribute** &gt; **Complete a questionnaire**.</span></span>
-   <span data-ttu-id="a4833-186">Çalışan Self-Servisinde **Tamamlanacak anketler** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a4833-186">In Employee self-service, click **Questionnaires to complete**.</span></span>

<span data-ttu-id="a4833-187">Anketler belirli kullanıcılar veya kullanıcı grupları ya da bir ağdaki tüm kullanıcılar için kullanıma sunulabilir.</span><span class="sxs-lookup"><span data-stu-id="a4833-187">Questionnaires can made be available to specific users or groups of users, or to all users in a network.</span></span>

<a name="see-also"></a><span data-ttu-id="a4833-188">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="a4833-188">See also</span></span>
--------

[<span data-ttu-id="a4833-189">Soru formları tasarlama</span><span class="sxs-lookup"><span data-stu-id="a4833-189">Designing questionnaires</span></span>](design-questionnaires.md)

[<span data-ttu-id="a4833-190">Soru formlarını kullanma</span><span class="sxs-lookup"><span data-stu-id="a4833-190">Using questionnaires</span></span>](questionnaires.md)

[<span data-ttu-id="a4833-191">Soru formlarının sonuçlarını görüntüleyin ve değerlendirin</span><span class="sxs-lookup"><span data-stu-id="a4833-191">Viewing and evaluating the results of questionnaires</span></span>](evaluate-questionnaire-results.md)



