---
title: Planlamayı kullanarak soru formlarını dağıtma
description: Soru formu planlama, soru formlarınızı planlamanıza ve birden fazla alıcıya dağıtmanıza izin verir.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMKnowledgeCollectorPlanningTable, KMKnowledgeCollectorPlanningMulti, SysQueryForm, HcmPersonLookup, KMKnowledgeCollectorPlanning, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 952048ce0a2ac94be70d7bde0dc52610f19151ed
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056312"
---
# <a name="distribute-questionnaires-using-scheduling"></a><span data-ttu-id="fe7c5-103">Planlamayı kullanarak soru formlarını dağıtma</span><span class="sxs-lookup"><span data-stu-id="fe7c5-103">Distribute questionnaires using scheduling</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="fe7c5-104">Soru formu planlama, soru formlarınızı planlamanıza ve birden fazla alıcıya dağıtmanıza izin verir.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-104">Questionnaire scheduling allows you to plan and distribute questionnaires to multiple respondents.</span></span> <span data-ttu-id="fe7c5-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-105">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-questionnaire-schedule"></a><span data-ttu-id="fe7c5-106">Soru formu planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="fe7c5-106">Create a questionnaire schedule</span></span>

1. <span data-ttu-id="fe7c5-107">Soru formu > Dağıt > Soru formu planları'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-107">Go to Questionnaire > Distribute > Questionnaire schedules.</span></span>

2. <span data-ttu-id="fe7c5-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-108">Click New.</span></span>

3. <span data-ttu-id="fe7c5-109">Planlama alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-109">In the Scheduling field, type a value.</span></span>

4. <span data-ttu-id="fe7c5-110">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="fe7c5-111">İsimlerin yanıtlarla ilişkilendirilmeden kaydedilmesi gerekiyorsa planı İsimsiz konumuna ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-111">Set the schedule to Anonymous if the responses should be recorded without names associated to the response.</span></span>  
    * <span data-ttu-id="fe7c5-112">İK parametrelerinde ilk olarak anonim sonuçlara izin verme ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-112">Allowing anonymous results must be set up in the HR parameters first.</span></span>  

5. <span data-ttu-id="fe7c5-113">Tür alanında planlama türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-113">In the Type field, select the planning type.</span></span>  <span data-ttu-id="fe7c5-114">Bu örnekte Memnuniyet Türü'nü kullanacağız.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-114">In this example we will use the Satisfaction type.</span></span>

6. <span data-ttu-id="fe7c5-115">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-115">In the list, find and select the desired record.</span></span>

7. <span data-ttu-id="fe7c5-116">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-116">In the list, click the link in the selected row.</span></span>

8. <span data-ttu-id="fe7c5-117">Tarih alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-117">In the Date field, enter a date.</span></span>

9. <span data-ttu-id="fe7c5-118">Çalışan self servis bölümü için E-posta'yı genişletin.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-118">Expand the Email for employee self service section.</span></span>

10. <span data-ttu-id="fe7c5-119">Konu alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-119">In the Subject field, type a value.</span></span>

    * <span data-ttu-id="fe7c5-120">Örnek: Soru formu mevcut</span><span class="sxs-lookup"><span data-stu-id="fe7c5-120">Example: Questionnaire available</span></span>  

11. <span data-ttu-id="fe7c5-121">Metin alanına e-posta iletinizin gövdesini yazın.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-121">In the Text field, type the body of your email message.</span></span> <span data-ttu-id="fe7c5-122">Sistemdeki değerleri değiştirmek için değişken kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-122">Note, the variable can be used to substitue values in the system.</span></span>

    * <span data-ttu-id="fe7c5-123">Örnek: Sayın %P%,  İşçi Sağlığı soru formunu tamamlamak için lütfen Personel Self Servisinde oturum açın.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-123">Example: Dear %P%, Please log in to Employee Self Service to complete the Workforce Health questionnaire.</span></span>  <span data-ttu-id="fe7c5-124">Contoso</span><span class="sxs-lookup"><span data-stu-id="fe7c5-124">Contoso</span></span>  

12. <span data-ttu-id="fe7c5-125">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-125">Click Save.</span></span>

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a><span data-ttu-id="fe7c5-126">Yanıtlanması gereken soru formlarını ve yanıtlayanların seçilmesinde kullanılacak sorguları seçmek için Kurulum ayrıntılarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-126">Use the Setup details to select the questionnaire(s) to be answered as well as any queries to use to select respondents.</span></span>

1. <span data-ttu-id="fe7c5-127">Kurulum ayrıntıları'nı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-127">Click Setup details.</span></span>

2. <span data-ttu-id="fe7c5-128">Listede, soru formu için yanıtlayanları sistemde aramak üzere kullanmak için bir soru seçin.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-128">In the list, select a query to use to search the system for respondents for the questionnaire.</span></span>

    * <span data-ttu-id="fe7c5-129">Örnek: Çalışanlar</span><span class="sxs-lookup"><span data-stu-id="fe7c5-129">Example: Workers</span></span>  

3. <span data-ttu-id="fe7c5-130">Göster düğmesini tıklayın veya belirli kişileri seçmek için sorguyu değiştirin veya belirli ölçütlerle eşleşen kişileri bulmak üzere sorguyu ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-130">Click View or modify query to select specific people or adjust the query to find people who match specific criteria.</span></span>

    * <span data-ttu-id="fe7c5-131">Tüm yanıtlayanların sistemde ayrıca kullanıcı olmaları gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-131">Note that all respondents must also be users in the system.</span></span>  

4. <span data-ttu-id="fe7c5-132">Listede, Kişi için satırı işaretleyin</span><span class="sxs-lookup"><span data-stu-id="fe7c5-132">In the list, mark the row for Person</span></span>

5. <span data-ttu-id="fe7c5-133">Ölçütler alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-133">In the Criteria field, enter or select a value.</span></span>

    * <span data-ttu-id="fe7c5-134">Julia Funderburk'ı seçin</span><span class="sxs-lookup"><span data-stu-id="fe7c5-134">Select Julia Funderburk</span></span>  

6. <span data-ttu-id="fe7c5-135">Listede, Julia Funderburk'u seçin</span><span class="sxs-lookup"><span data-stu-id="fe7c5-135">In the list, select Julia Funderburk</span></span>

7. <span data-ttu-id="fe7c5-136">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-136">Click OK.</span></span>

8. <span data-ttu-id="fe7c5-137">Soru formları sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-137">Click the Questionnaires tab.</span></span>

9. <span data-ttu-id="fe7c5-138">Ağaçta, "Memnuniyet Anketi soru formu türü düğümü"nü genişletin.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-138">In the tree, expand 'the node for the questionnaire type Satisfaction Survey'.</span></span>

10. <span data-ttu-id="fe7c5-139">Ağaçta, "İşçi Sağlığı Değerlendirmesi" kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-139">In the tree, check 'Workforce Health Assessment'.</span></span>

11. <span data-ttu-id="fe7c5-140">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-140">Click OK.</span></span>

12. <span data-ttu-id="fe7c5-141">Planlı yanıt oturumu oluşturma</span><span class="sxs-lookup"><span data-stu-id="fe7c5-141">Click Planned answer session.</span></span>

    * <span data-ttu-id="fe7c5-142">Planlı yanıt oturumlarının her bir seçilen/sorgulanan kullanıcı için oluşturulduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-142">Note that Planned answer sessions have been created for each selected/queried user.</span></span>  

13. <span data-ttu-id="fe7c5-143">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-143">Close the page.</span></span>

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a><span data-ttu-id="fe7c5-144">Soru formunu yanıtlayanlar tarafından tamamlanması için kullanılabilir hale getirmek üzere soru formu planını başlatın.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-144">Start the questionnaire schedule in order to make the questionnaire available for respondents to complete.</span></span>

1. <span data-ttu-id="fe7c5-145">İşlevler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-145">Click Functions.</span></span>

2. <span data-ttu-id="fe7c5-146">Başlat'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-146">Click Start.</span></span>

3. <span data-ttu-id="fe7c5-147">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-147">Click OK.</span></span>

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a><span data-ttu-id="fe7c5-148">Mevcut soru formunu yanıtlayanları bilgilendirmek üzere e-posta gönderin.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-148">Send the email to inform respondents of the available questionnaire.</span></span>

1. <span data-ttu-id="fe7c5-149">İşlevler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-149">Click Functions.</span></span>

2. <span data-ttu-id="fe7c5-150">E-posta gönder'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-150">Click Send email.</span></span>

3. <span data-ttu-id="fe7c5-151">İptal'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-151">Click Cancel.</span></span>

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a><span data-ttu-id="fe7c5-152">Soru formunu tamamlaması gerekenleri izlemek için Planlı yanıt oturumları'nı kullanın.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-152">Use Planned answer sessions to monitor who needs to complete the questionnaire.</span></span>

1. <span data-ttu-id="fe7c5-153">Planlı yanıt oturumu oluşturma</span><span class="sxs-lookup"><span data-stu-id="fe7c5-153">Click Planned answer session.</span></span>

    * <span data-ttu-id="fe7c5-154">Planlı oturumu sonlandırmaya hazır duruma geldiğinizde varsa, kalan planlı yanıt oturumunu silin.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-154">Delete any remaining planned answer session when you're ready to end the scheduled session.</span></span>  

2. <span data-ttu-id="fe7c5-155">Sil'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-155">Click Delete.</span></span>

3. <span data-ttu-id="fe7c5-156">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-156">Click Yes.</span></span>

4. <span data-ttu-id="fe7c5-157">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-157">Close the page.</span></span>

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a><span data-ttu-id="fe7c5-158">Tüm yanıtlayanlar soru formunu tamamladığında ve/veya kalan tüm Planlı yanıt oturumları silindiğinde planı sonlandırın.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-158">End the schedule when all respondents have completed the questionnaire and/or all remaining Planned answer sessions have been deleted.</span></span>

1. <span data-ttu-id="fe7c5-159">İşlevler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-159">Click Functions.</span></span>
2. <span data-ttu-id="fe7c5-160">Sonlandır'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-160">Click End.</span></span>
3. <span data-ttu-id="fe7c5-161">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe7c5-161">Click OK.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]