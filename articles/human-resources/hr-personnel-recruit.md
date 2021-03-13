---
title: İş adaylarını işe alma
description: Bu konu, Dynamics 365 Human Resources içinde adayların nasıl işe alınacağını gösterir .
author: andreabichsel
manager: tfehr
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f615584785ba48a140e4e97991a4594047fea8ee
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114517"
---
# <a name="recruit-job-candidates"></a><span data-ttu-id="d85ae-103">İş adaylarını işe alma</span><span class="sxs-lookup"><span data-stu-id="d85ae-103">Recruit job candidates</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="d85ae-104">Dynamics 365 Human Resources işe alma isteklerini yönetmenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="d85ae-104">Dynamics 365 Human Resources helps you to manage recruiting requests.</span></span> <span data-ttu-id="d85ae-105">Ayrıca, çalışanların iş adaylarına sorunsuz şekilde geçiş yapmanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="d85ae-105">It also helps you seamlessly transition job candidates to employees.</span></span> <span data-ttu-id="d85ae-106">Organizasyonunuzda ayrı bir işe alma uygulaması kullanılıyorsa, işe alma işleminiz aşağıdaki adımları içerebilir:</span><span class="sxs-lookup"><span data-stu-id="d85ae-106">If your organization uses a separate recruiting application, your recruiting process might include the following steps:</span></span>

- <span data-ttu-id="d85ae-107">İşe alma isteğinizi İnsan Kaynakları girin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-107">Enter your recruiting request in Human Resources.</span></span>
- <span data-ttu-id="d85ae-108">İşe alma uygulamasından İnsan Kaynakları aday başvurularını alın.</span><span class="sxs-lookup"><span data-stu-id="d85ae-108">Receive candidate referrals in Human Resources from the recruiting application.</span></span>
- <span data-ttu-id="d85ae-109">Aday onaylama işlemini İnsan Kaynakları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="d85ae-109">Complete the candidate approval process in Human Resources.</span></span>

<span data-ttu-id="d85ae-110">Ayrı bir işe alma uygulaması kullanmıyorsanız, İnsan Kaynakları adayların da el ile yönetilmesini sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d85ae-110">If you aren't using a separate recruiting application, you can also manually manage candidates in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="d85ae-111">Bir yönetici veya geliştiricisiyseniz İnsan Kaynakları üçüncü taraf işe alma uygulamasıyla bütünleştirmek istiyorsanız, bkz: [Dataverse tümleştirmeyi konfigüre et](hr-admin-integration-common-data-service.md) ve [Dataverse sanal tablolarını yapılandırma](hr-admin-integration-common-data-service-virtual-entities.md)</span><span class="sxs-lookup"><span data-stu-id="d85ae-111">If you're an admin or developer and want to integrate Human Resources with a third-party recruiting application, see [Configure Dataverse integration](hr-admin-integration-common-data-service.md) and [Configure Dataverse virtual tables](hr-admin-integration-common-data-service-virtual-entities.md)</span></span>
>
> <span data-ttu-id="d85ae-112">[AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics) işe alma tümleştirme uygulamalarını da bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d85ae-112">You can also find recruiting integration apps on [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span></span>
>
> <span data-ttu-id="d85ae-113">LinkedIn Talent Hub'ı ile tümleştirilmesine yönelik önizleme özelliğini denemek için, bkz. [LinkedIn Talent Hub ile entegre edin](hr-admin-integration-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="d85ae-113">To try out our preview feature for integrating with LinkedIn Talent Hub, see [Integrate with LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span></span>

## <a name="enable-recruiting-requests"></a><span data-ttu-id="d85ae-114">İşe alma isteklerini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="d85ae-114">Enable recruiting requests</span></span>

<span data-ttu-id="d85ae-115">İşe alma isteklerini İnsan Kaynakları göndermek istiyorsanız, önce **Human Resources paylaşılan parametrelerinde** işlevi etkinleştirmeniz gerekir .</span><span class="sxs-lookup"><span data-stu-id="d85ae-115">If you want to submit recruiting requests in Human Resources, you must first enable the functionality in **Human resources shared parameters**.</span></span>

1. <span data-ttu-id="d85ae-116">**Personel yönetimi** çalışma alanında, **Bağlantılar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-116">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="d85ae-117">**Kurulum**'un altında, **İnsan kaynakları paylaşılan parametrelerini** seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-117">Under **Setup**, select **Human resources shared parameters**.</span></span>

3. <span data-ttu-id="d85ae-118">**İşe alma** sekmesinde, **İŞE ALMA** altında, **işe alma isteklerini** **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d85ae-118">On the **Recruitment** tab, under **RECRUITING**, set **Enable recruiting requests** to **Yes**.</span></span>

## <a name="add-a-recruiting-request-location"></a><span data-ttu-id="d85ae-119">İşe alma isteği Ekle konumu</span><span class="sxs-lookup"><span data-stu-id="d85ae-119">Add a recruiting request location</span></span>

<span data-ttu-id="d85ae-120">Kuruluşunuzun birden çok konumu varsa, bu dosyaları ekleyerek bunları ekleyebilirsiniz ve böylece istek, yeni işe çalıştığınız yerdeki bir yerleşim seçebilir.</span><span class="sxs-lookup"><span data-stu-id="d85ae-120">If your organization has multiple locations, you can add them so requestors can select a location where the new recruit will be working.</span></span> <span data-ttu-id="d85ae-121">Yerleşim, proje nakline dahil edilecek.</span><span class="sxs-lookup"><span data-stu-id="d85ae-121">The location will be included in the job posting.</span></span>

1. <span data-ttu-id="d85ae-122">Arama çubuğunda, **işe alma istek konumunu** girin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-122">In the search bar, enter **recruiting request location**.</span></span>

2. <span data-ttu-id="d85ae-123">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-123">Select **New**.</span></span>

3. <span data-ttu-id="d85ae-124">**İşe alma istek yerleşimi** alanına yerleşim adını girin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-124">In the **Recruiting request location** field, enter the location name.</span></span>

   ![İşe alma isteği Ekle konumu](./media/hr-recruit-0a-add-location.png)

4. <span data-ttu-id="d85ae-126">**Açıklama** alanında konumu için bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-126">In the **Description**, enter a description for the location.</span></span>

5. <span data-ttu-id="d85ae-127">**Konum** altında, **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-127">Under **Location**, select **Add**.</span></span> <span data-ttu-id="d85ae-128">**Yeni Adres** yerleşimi görünürse, konumun adresini girin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-128">If the **New address** popout appears, enter the address for the location.</span></span>

   ![Adresi gir](./media/hr-recruit-0b-address.png)

6. <span data-ttu-id="d85ae-130">**İlgili kişi bilgileri** altında yerleşimin ilgili kişisinin bilgilerini girin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-130">Under **Contact information**, enter the information for the location's contact.</span></span>

7. <span data-ttu-id="d85ae-131">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-131">Select **Save**.</span></span>

## <a name="add-a-recruiting-request"></a><span data-ttu-id="d85ae-132">İşe alma isteği Ekle</span><span class="sxs-lookup"><span data-stu-id="d85ae-132">Add a recruiting request</span></span>

<span data-ttu-id="d85ae-133">Yöneticiler İnsan Kaynakları işe alma istekleri gönderebilir.</span><span class="sxs-lookup"><span data-stu-id="d85ae-133">Managers can submit recruiting requests in Human Resources.</span></span> <span data-ttu-id="d85ae-134">Ayrı bir işe alma uygulaması kullanırsanız, bu adımlar tamamlandıktan sonra işe alma isteği gönderilir ve işe alma işlemini o uygulamada başlatır.</span><span class="sxs-lookup"><span data-stu-id="d85ae-134">If you use a separate recruiting application, completing these steps will send a recruiting request and start the recruiting process in that application.</span></span> <span data-ttu-id="d85ae-135">Aksi durumda, iş akışını kendi iç işe alma işleminiz için başlatmak üzere bu yordamı tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="d85ae-135">Otherwise, complete this procedure to begin the workflow for your own internal recruiting process.</span></span>

1. <span data-ttu-id="d85ae-136">**Çalışan self servisini** seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-136">Select **Employee self service**.</span></span>

2. <span data-ttu-id="d85ae-137">**Ekibim** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-137">Select the **My team** tab.</span></span>

3. <span data-ttu-id="d85ae-138">**İşe almak için talep** seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-138">Select  **Request to recruit**.</span></span>

   ![İşe alma isteği başlat](./media/hr-recruit-1-request-to-recruit.png)

4. <span data-ttu-id="d85ae-140">**Açıklama**, **iş** ve **Tahmini Başlangıç tarihi** alanlarını tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="d85ae-140">Complete the **Description**, **Job**, and **Estimated start date** fields.</span></span>

   ![İşe alma isteğini tamamlayın](./media/hr-recruit-2-request-to-recruit.png)

5. <span data-ttu-id="d85ae-142">**Devam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-142">Select **Continue**.</span></span> <span data-ttu-id="d85ae-143">Konumlarınıza ilişkin işe alma isteği görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="d85ae-143">The recruiting request for your position appears.</span></span>

6. <span data-ttu-id="d85ae-144">**Genel** altında, **Recruiter** açılan menüsünden bir işe alan seçin ve **işe alma isteği yerleşimi** açılan menüsünden bir yerleşim seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-144">Under **General**, select a recruiter from the **Recruiter** dropdown, and then select a location from the **Recruiting request location** dropdown.</span></span>

7. <span data-ttu-id="d85ae-145">**İş** altında, gerekli tüm bilgileri değiştirin ve sonra **işten ayrıntıları oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-145">Under **Job**, change any information as needed, and then select **Create details from job**.</span></span>

   ![İşten ayrıntı oluştur](./media/hr-recruit-3-create-details-from-job.png)

   <span data-ttu-id="d85ae-147">İşe alma isteğinin geri kalanı girdiğiniz işle ilgili varsayılan bilgilerle doldurulur.</span><span class="sxs-lookup"><span data-stu-id="d85ae-147">The rest of the recruiting request will populate with the default information for the job you entered.</span></span>

8. <span data-ttu-id="d85ae-148">**Harici açıklama** altında harici olarak açık bir iş açıklaması girin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-148">Under **External description**, enter an external-facing job description.</span></span>

9. <span data-ttu-id="d85ae-149">**Pozisyonlar** altında, **Ekle** 'yi seçin ve sonra bu işe alma isteği için bir pozisyon seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-149">Under **Positions**, select **Add**, and then select a position for this recruiting request.</span></span>

   ![Pozisyon Ekle](./media/hr-recruit-4-select-position.png)

10. <span data-ttu-id="d85ae-151">**Yetenekler**'in altında , **Ekle**'yi seçin ve sonra da bir yetenek seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-151">Under **Skills**, select **Add**, and then select a skill.</span></span>

11. <span data-ttu-id="d85ae-152">**Eğitim gereksinimleri** altında , **Ekle**'yi seçin ve sonra **eğitim** ve **eğitim düzeyi** açılan listelerinden değerleri seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-152">Under **Educational requirements**, select **Add**, and then select values from the **Education** and **Level of education** dropdowns.</span></span>

   ![Eğitim gereksinimleri Ekle](./media/hr-recruit-5-select-educational-requirements.png)

12. <span data-ttu-id="d85ae-154">**Yorum** altında gerektiği şekilde yorumlar ekleyin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-154">Under **Comment**, add comments as necessary.</span></span>

13. <span data-ttu-id="d85ae-155">**Dengeleme** altında, **düzey** açılan menüsünden bir düzey seçin ve sonra **düşük eşik**, **kontrol noktası** ve **yüksek eşik ayarlarını** gerektiği gibi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d85ae-155">Under **Compensation**, select a level from the **Level** dropdown, and then adjust **Low threshold**, **Control point**, and **High threshold** as necessary.</span></span>

14. <span data-ttu-id="d85ae-156">İşe alma isteğiniz tamamlandığında ve işe alma işlemini başlatmaya hazır olduğunuzda, menü çubuğunda **Etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-156">When your recruiting request is complete and you're ready to start the recruiting process, select **Activate** in the menu bar.</span></span>

   ![İşe alma isteğini etkinleştir](./media/hr-recruit-6-activate-recruit-request.png)

15. <span data-ttu-id="d85ae-158">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-158">Select **Save**.</span></span>

## <a name="view-and-edit-your-recruiting-requests"></a><span data-ttu-id="d85ae-159">İşe alma isteklerinizi görüntüleyin ve düzenleyin</span><span class="sxs-lookup"><span data-stu-id="d85ae-159">View and edit your recruiting requests</span></span>

<span data-ttu-id="d85ae-160">Bir yönetici iseniz ve kendi isteklerinizi görüntülemek istiyorsanız:</span><span class="sxs-lookup"><span data-stu-id="d85ae-160">If you're a manager and want to view your own requests:</span></span>

1. <span data-ttu-id="d85ae-161">**Çalışan self servisini** seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-161">Select **Employee self service**.</span></span>

2. <span data-ttu-id="d85ae-162">**Ekibim** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-162">Select the **My team** tab.</span></span>

3. <span data-ttu-id="d85ae-163">**Ekip bilgilerim** altında, **İşe alma istekleri** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-163">Under **My team information**, select the **Recruiting requests** tab.</span></span>

   ![Işe alma istekleri sekmesini seçin](./media/hr-recruit-7-recruiting-requests.png)

4. <span data-ttu-id="d85ae-165">İşe alma isteğini görüntülemek veya düzenlemek için bunu kılavuzda seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-165">To view or edit a recruiting request, select it in the grid.</span></span>

<span data-ttu-id="d85ae-166">Bir İK Pro iseniz ve tüm işe alma isteklerini görüntülemek istiyorsanız:</span><span class="sxs-lookup"><span data-stu-id="d85ae-166">If you're an HR pro and want to view all recruiting requests:</span></span>

1. <span data-ttu-id="d85ae-167">**Personel yönetimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-167">Select **Personnel management**.</span></span>

2. <span data-ttu-id="d85ae-168">**Işe alma istekleri** seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-168">Select **Recruiting requests**.</span></span>

   ![Personel yönetiminde işe alma isteklerini görüntüle](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. <span data-ttu-id="d85ae-170">İşe alma isteğini görüntülemek veya düzenlemek için bunu kılavuzda seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-170">To view or edit a recruiting request, select it in the grid.</span></span>

## <a name="add-or-edit-a-candidate-profile"></a><span data-ttu-id="d85ae-171">Aday profili ekleme veya düzenleme</span><span class="sxs-lookup"><span data-stu-id="d85ae-171">Add or edit a candidate profile</span></span>

<span data-ttu-id="d85ae-172">Kuruluşunuz işe alma isteklerini yönetmek için başka bir uygulamayla tümleşikse, işe alma istekleri o uygulamaya iletilir.</span><span class="sxs-lookup"><span data-stu-id="d85ae-172">If your organization has integrated with another application to manage recruiting requests, recruiting requests are forwarded to that application.</span></span> <span data-ttu-id="d85ae-173">İşe alma uygulaması daha sonra aday bilgilerini İnsan Kaynakları geri gönderir.</span><span class="sxs-lookup"><span data-stu-id="d85ae-173">The recruiting application then sends candidate information back to Human Resources.</span></span> <span data-ttu-id="d85ae-174">Aksi durumda, kendi iç işe alma işlemlerinizi takip edebilir ve aday bilgilerini el ile girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d85ae-174">Otherwise, you can follow your own internal recruiting processes and enter candidate information manually.</span></span>

1. <span data-ttu-id="d85ae-175">**Personel yönetimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-175">Select **Personnel management**.</span></span>

2. <span data-ttu-id="d85ae-176">**Bağlantılar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-176">Select **Links**.</span></span>

3. <span data-ttu-id="d85ae-177">**İşe alma** altında **Adaylar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-177">Under **Recruiting**, select **Candidates**.</span></span>

   ![Adayları görüntüle](./media/hr-recruit-9-candidates.png)

4. <span data-ttu-id="d85ae-179">Aday eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-179">To add a candidate, select **New**.</span></span> <span data-ttu-id="d85ae-180">Varolan bir adayı düzenlemek için, listeden aday seçin ve **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-180">To edit an existing candidate, select the candidate from the list and then select **Edit**.</span></span> <span data-ttu-id="d85ae-181">Aday profili görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="d85ae-181">The candidate profile appears.</span></span>

5. <span data-ttu-id="d85ae-182">**Aday Özeti** altında aday bilgilerini gerektiği gibi girin veya düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-182">Under **Candidate summary**, enter or edit the candidate information as necessary.</span></span>

6. <span data-ttu-id="d85ae-183">**İşe alma isteği** altında adayı bağlamak için bir işe alma isteği seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-183">Under **Recruiting request**, select a recruiting request to link the candidate to.</span></span> <span data-ttu-id="d85ae-184">**Tahmini Başlangıç tarihi**, **işe alma Yöneticisi**, **Konum** ve **Açıklama alanlarını** gerektiği gibi tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="d85ae-184">Then complete the **Estimated start date**, **Hiring manager**, **Position**, and **Description fields** as appropriate.</span></span>

   ![İşe alma isteğine bağla](./media/hr-recruit-10-link-to-recruiting-request.png)

7. <span data-ttu-id="d85ae-186">Aday kaydına dahil etmek istediğiniz aşağıdaki alanlardaki tüm bilgileri tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="d85ae-186">Complete all the information in the following areas that you want to include in the candidate's record:</span></span>
   - <span data-ttu-id="d85ae-187">**Yorumlar**</span><span class="sxs-lookup"><span data-stu-id="d85ae-187">**Comments**</span></span>
   - <span data-ttu-id="d85ae-188">**Mesleki deneyim**</span><span class="sxs-lookup"><span data-stu-id="d85ae-188">**Professional experience**</span></span>
   - <span data-ttu-id="d85ae-189">**İletişim bilgileri**</span><span class="sxs-lookup"><span data-stu-id="d85ae-189">**Contact information**</span></span>
   - <span data-ttu-id="d85ae-190">**Eğitim**</span><span class="sxs-lookup"><span data-stu-id="d85ae-190">**Education**</span></span>
   - <span data-ttu-id="d85ae-191">**Yetenekler**</span><span class="sxs-lookup"><span data-stu-id="d85ae-191">**Skills**</span></span>
   - <span data-ttu-id="d85ae-192">**Sertifikalar**</span><span class="sxs-lookup"><span data-stu-id="d85ae-192">**Certificates**</span></span>
   - <span data-ttu-id="d85ae-193">**Filtrelemeler**</span><span class="sxs-lookup"><span data-stu-id="d85ae-193">**Screenings**</span></span>

8. <span data-ttu-id="d85ae-194">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-194">Select **Save**.</span></span>

## <a name="hire-a-candidate"></a><span data-ttu-id="d85ae-195">Adayı işe al</span><span class="sxs-lookup"><span data-stu-id="d85ae-195">Hire a candidate</span></span>

<span data-ttu-id="d85ae-196">Bir adayı işe almak için hazır olduğunuzda, adayı bir çalışana aktarmak için aşağıdaki yordamı izleyin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-196">When you're ready to hire a candidate, follow this procedure to transition the candidate to an employee.</span></span>

1. <span data-ttu-id="d85ae-197">Aday formunda **işe al**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-197">On the candidate form, select **Hire**.</span></span>

   ![Adayı işe al](./media/hr-recruit-11-hire.png)

2. <span data-ttu-id="d85ae-199">**İşe yeni çalışan** formunda, **Ayrıntılar** altında tüm alanları doldurun.</span><span class="sxs-lookup"><span data-stu-id="d85ae-199">On the **Hire new worker** form, under **Details**, complete all the fields.</span></span>

   ![Yeni işe alma ayrıntılarını girin](./media/hr-recruit-12-hire-new-worker.png)

3. <span data-ttu-id="d85ae-201">**Pozisyon ayrıntıları** altında , bilgileri gerektiği gibi doğrulayın ve değiştirin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-201">Under **Position details**, verify and change information as necessary.</span></span>

4. <span data-ttu-id="d85ae-202">**Ekleme listeleri listesi** altında , bu çalışana ait ilgili ekleme denetim listelerini seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-202">Under **Onboarding checklists**, select the relevant onboarding checklists for this employee.</span></span>

5. <span data-ttu-id="d85ae-203">Çalışan kaydını oluşturmak için **devam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-203">Select **Continue** to create the employee record.</span></span>

   >[!NOTE]
   ><span data-ttu-id="d85ae-204">Kuruluşunuzun iş akışlarına bağlı olarak, aday kaydı, bir çalışan kaydı yapılmadan önce ek onay adımlarıyla geçebilir.</span><span class="sxs-lookup"><span data-stu-id="d85ae-204">Depending on your organization's workflows, the candidate record may go through additional approval steps before becoming an employee record.</span></span>

## <a name="decide-not-to-hire-a-candidate"></a><span data-ttu-id="d85ae-205">Aday işe gerekmediğine karar verme</span><span class="sxs-lookup"><span data-stu-id="d85ae-205">Decide not to hire a candidate</span></span>

<span data-ttu-id="d85ae-206">Bir adayı işe gerekmediğine karar verirseniz, aşağıdaki yordamı izleyerek onları vetele alma işleminden çıkarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d85ae-206">If you decide not to hire a candidate, follow this procedure to remove them from the vetting process.</span></span> 

1. <span data-ttu-id="d85ae-207">Aday formunda **işe alma**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-207">On the candidate form, select **Do not hire**.</span></span>

   ![Adayı işe alma](./media/hr-recruit-13-do-not-hire.png)

2. <span data-ttu-id="d85ae-209">Bir **neden kodu** seçin ve açıklama ekleyin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-209">Select a **Reason code** and include any comments.</span></span>

3. <span data-ttu-id="d85ae-210">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-210">Select **OK**.</span></span>

## <a name="dismiss-a-candidate"></a><span data-ttu-id="d85ae-211">Adayı kapat</span><span class="sxs-lookup"><span data-stu-id="d85ae-211">Dismiss a candidate</span></span>

<span data-ttu-id="d85ae-212">Gerekirse, bir adayı işe aldıktan sonra kapatabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d85ae-212">If needed, you can dismiss a candidate after hiring them.</span></span> <span data-ttu-id="d85ae-213">Örneğin, bir aday teklifinizi reddedebilir veya ilk gününde göstermeyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d85ae-213">For example, a candidate might reject your offer or not show up on their first day.</span></span>

- <span data-ttu-id="d85ae-214">Aday formunda **Adayı kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d85ae-214">On the candidate form, select **Dismiss candidate**.</span></span>

  ![Adayı bırakın.](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a><span data-ttu-id="d85ae-216">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="d85ae-216">See also</span></span>

[<span data-ttu-id="d85ae-217">Dataverse sanal tablolarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="d85ae-217">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="d85ae-218">İş gücünüzü düzenleme</span><span class="sxs-lookup"><span data-stu-id="d85ae-218">Organize your workforce</span></span>](hr-personnel-departments-jobs-positions.md)<br>
[<span data-ttu-id="d85ae-219">İşin bileşenlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="d85ae-219">Set up the components of a job</span></span>](hr-personnel-jobs.md)
