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
ms.openlocfilehash: 9a35abcb8a2f6aa8031c8d84a44c2a8ad93883ac
ms.sourcegitcommit: 0354ca7e566fbd2eb0aabdd40000d4ac5c44ea78
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/04/2020
ms.locfileid: "4669195"
---
# <a name="recruit-job-candidates"></a><span data-ttu-id="58a73-103">İş adaylarını işe alma</span><span class="sxs-lookup"><span data-stu-id="58a73-103">Recruit job candidates</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="58a73-104">Dynamics 365 Human Resources işe alma isteklerini yönetmenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="58a73-104">Dynamics 365 Human Resources helps you to manage recruiting requests.</span></span> <span data-ttu-id="58a73-105">Ayrıca, çalışanların iş adaylarına sorunsuz şekilde geçiş yapmanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="58a73-105">It also helps you seamlessly transition job candidates to employees.</span></span> <span data-ttu-id="58a73-106">Organizasyonunuzda ayrı bir işe alma uygulaması kullanılıyorsa, işe alma işleminiz aşağıdaki adımları içerebilir:</span><span class="sxs-lookup"><span data-stu-id="58a73-106">If your organization uses a separate recruiting application, your recruiting process might include the following steps:</span></span>

- <span data-ttu-id="58a73-107">İşe alma isteğinizi İnsan Kaynakları girin.</span><span class="sxs-lookup"><span data-stu-id="58a73-107">Enter your recruiting request in Human Resources.</span></span>
- <span data-ttu-id="58a73-108">İşe alma uygulamasından İnsan Kaynakları aday başvurularını alın.</span><span class="sxs-lookup"><span data-stu-id="58a73-108">Receive candidate referrals in Human Resources from the recruiting application.</span></span>
- <span data-ttu-id="58a73-109">Aday onaylama işlemini İnsan Kaynakları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="58a73-109">Complete the candidate approval process in Human Resources.</span></span>

<span data-ttu-id="58a73-110">Ayrı bir işe alma uygulaması kullanmıyorsanız, İnsan Kaynakları adayların da el ile yönetilmesini sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="58a73-110">If you aren't using a separate recruiting application, you can also manually manage candidates in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="58a73-111">Bir yönetici veya geliştiricisiyseniz İnsan Kaynakları üçüncü taraf işe alma uygulamasıyla bütünleştirmek istiyorsanız, bkz: [Common Data Service tümleştirmeyi konfigüre et](hr-admin-integration-common-data-service.md) ve [Common Data Service sanal varlıkları konfigüre et](hr-admin-integration-common-data-service-virtual-entities.md)</span><span class="sxs-lookup"><span data-stu-id="58a73-111">If you're an admin or developer and want to integrate Human Resources with a third-party recruiting application, see [Configure Common Data Service integration](hr-admin-integration-common-data-service.md) and [Configure Common Data Service virtual entities](hr-admin-integration-common-data-service-virtual-entities.md)</span></span>
>
> <span data-ttu-id="58a73-112">[AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics) işe alma tümleştirme uygulamalarını da bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="58a73-112">You can also find recruiting integration apps on [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span></span>
>
> <span data-ttu-id="58a73-113">LinkedIn Talent Hub'ı ile tümleştirilmesine yönelik önizleme özelliğini denemek için, bkz. [LinkedIn Talent Hub ile entegre edin](hr-admin-integration-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="58a73-113">To try out our preview feature for integrating with LinkedIn Talent Hub, see [Integrate with LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span></span>

## <a name="enable-recruiting-requests"></a><span data-ttu-id="58a73-114">İşe alma isteklerini etkinleştir</span><span class="sxs-lookup"><span data-stu-id="58a73-114">Enable recruiting requests</span></span>

<span data-ttu-id="58a73-115">İşe alma isteklerini İnsan Kaynakları göndermek istiyorsanız, önce **insan kaynakları parametrelerinde** işlevi etkinleştirmeniz gerekir .</span><span class="sxs-lookup"><span data-stu-id="58a73-115">If you want to submit recruiting requests in Human Resources, you must first enable the functionality in **Human resources parameters**.</span></span>

1. <span data-ttu-id="58a73-116">**Personel yönetimi** çalışma alanında, **Bağlantılar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-116">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="58a73-117">**Kurulum**'un altında, **İnsan kaynakları parametrelerini** seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-117">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="58a73-118">**Genel** sekmesinde, **işe alma** altında, **işe alma isteklerini** **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="58a73-118">On the **General** tab, under **RECRUITING**, set **Enable recruiting requests** to **Yes**.</span></span>

   ![İşe alma isteklerini etkinleştir](./media/hr-recruit-0-enable-requests.png)

## <a name="add-a-recruiting-request-location"></a><span data-ttu-id="58a73-120">İşe alma isteği Ekle konumu</span><span class="sxs-lookup"><span data-stu-id="58a73-120">Add a recruiting request location</span></span>

<span data-ttu-id="58a73-121">Kuruluşunuzun birden çok konumu varsa, bu dosyaları ekleyerek bunları ekleyebilirsiniz ve böylece istek, yeni işe çalıştığınız yerdeki bir yerleşim seçebilir.</span><span class="sxs-lookup"><span data-stu-id="58a73-121">If your organization has multiple locations, you can add them so requestors can select a location where the new recruit will be working.</span></span> <span data-ttu-id="58a73-122">Yerleşim, proje nakline dahil edilecek.</span><span class="sxs-lookup"><span data-stu-id="58a73-122">The location will be included in the job posting.</span></span>

1. <span data-ttu-id="58a73-123">Arama çubuğunda, **işe alma istek konumunu** girin.</span><span class="sxs-lookup"><span data-stu-id="58a73-123">In the search bar, enter **recruiting request location**.</span></span>

2. <span data-ttu-id="58a73-124">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-124">Select **New**.</span></span>

3. <span data-ttu-id="58a73-125">**İşe alma istek yerleşimi** alanına yerleşim adını girin.</span><span class="sxs-lookup"><span data-stu-id="58a73-125">In the **Recruiting request location** field, enter the location name.</span></span>

   ![İşe alma isteği Ekle konumu](./media/hr-recruit-0a-add-location.png)

4. <span data-ttu-id="58a73-127">**Açıklama** alanında konumu için bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="58a73-127">In the **Description**, enter a description for the location.</span></span>

5. <span data-ttu-id="58a73-128">**Konum** altında, **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-128">Under **Location**, select **Add**.</span></span> <span data-ttu-id="58a73-129">**Yeni Adres** yerleşimi görünürse, konumun adresini girin.</span><span class="sxs-lookup"><span data-stu-id="58a73-129">If the **New address** popout appears, enter the address for the location.</span></span>

   ![Adresi gir](./media/hr-recruit-0b-address.png)

6. <span data-ttu-id="58a73-131">**İlgili kişi bilgileri** altında yerleşimin ilgili kişisinin bilgilerini girin.</span><span class="sxs-lookup"><span data-stu-id="58a73-131">Under **Contact information**, enter the information for the location's contact.</span></span>

7. <span data-ttu-id="58a73-132">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-132">Select **Save**.</span></span>

## <a name="add-a-recruiting-request"></a><span data-ttu-id="58a73-133">İşe alma isteği Ekle</span><span class="sxs-lookup"><span data-stu-id="58a73-133">Add a recruiting request</span></span>

<span data-ttu-id="58a73-134">Yöneticiler İnsan Kaynakları işe alma istekleri gönderebilir.</span><span class="sxs-lookup"><span data-stu-id="58a73-134">Managers can submit recruiting requests in Human Resources.</span></span> <span data-ttu-id="58a73-135">Ayrı bir işe alma uygulaması kullanırsanız, bu adımlar tamamlandıktan sonra işe alma isteği gönderilir ve işe alma işlemini o uygulamada başlatır.</span><span class="sxs-lookup"><span data-stu-id="58a73-135">If you use a separate recruiting application, completing these steps will send a recruiting request and start the recruiting process in that application.</span></span> <span data-ttu-id="58a73-136">Aksi durumda, iş akışını kendi iç işe alma işleminiz için başlatmak üzere bu yordamı tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="58a73-136">Otherwise, complete this procedure to begin the workflow for your own internal recruiting process.</span></span>

1. <span data-ttu-id="58a73-137">**Çalışan self servisini** seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-137">Select **Employee self service**.</span></span>

2. <span data-ttu-id="58a73-138">**Ekibim** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-138">Select the **My team** tab.</span></span>

3. <span data-ttu-id="58a73-139">**İşe almak için talep** seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-139">Select  **Request to recruit**.</span></span>

   ![İşe alma isteği başlat](./media/hr-recruit-1-request-to-recruit.png)

4. <span data-ttu-id="58a73-141">**Açıklama**, **iş** ve **Tahmini Başlangıç tarihi** alanlarını tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="58a73-141">Complete the **Description**, **Job**, and **Estimated start date** fields.</span></span>

   ![İşe alma isteğini tamamlayın](./media/hr-recruit-2-request-to-recruit.png)

5. <span data-ttu-id="58a73-143">**Devam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-143">Select **Continue**.</span></span> <span data-ttu-id="58a73-144">Konumlarınıza ilişkin işe alma isteği görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="58a73-144">The recruiting request for your position appears.</span></span>

6. <span data-ttu-id="58a73-145">**Genel** altında, **Recruiter** açılan menüsünden bir işe alan seçin ve **işe alma isteği yerleşimi** açılan menüsünden bir yerleşim seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-145">Under **General**, select a recruiter from the **Recruiter** dropdown, and then select a location from the **Recruiting request location** dropdown.</span></span>

7. <span data-ttu-id="58a73-146">**İş** altında, gerekli tüm bilgileri değiştirin ve sonra **işten ayrıntıları oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-146">Under **Job**, change any information as needed, and then select **Create details from job**.</span></span>

   ![İşten ayrıntı oluştur](./media/hr-recruit-3-create-details-from-job.png)

   <span data-ttu-id="58a73-148">İşe alma isteğinin geri kalanı girdiğiniz işle ilgili varsayılan bilgilerle doldurulur.</span><span class="sxs-lookup"><span data-stu-id="58a73-148">The rest of the recruiting request will populate with the default information for the job you entered.</span></span>

8. <span data-ttu-id="58a73-149">**Harici açıklama** altında harici olarak açık bir iş açıklaması girin.</span><span class="sxs-lookup"><span data-stu-id="58a73-149">Under **External description**, enter an external-facing job description.</span></span>

9. <span data-ttu-id="58a73-150">**Pozisyonlar** altında, **Ekle** 'yi seçin ve sonra bu işe alma isteği için bir pozisyon seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-150">Under **Positions**, select **Add**, and then select a position for this recruiting request.</span></span>

   ![Pozisyon Ekle](./media/hr-recruit-4-select-position.png)

10. <span data-ttu-id="58a73-152">**Yetenekler**'in altında , **Ekle**'yi seçin ve sonra da bir yetenek seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-152">Under **Skills**, select **Add**, and then select a skill.</span></span>

11. <span data-ttu-id="58a73-153">**Eğitim gereksinimleri** altında , **Ekle**'yi seçin ve sonra **eğitim** ve **eğitim düzeyi** açılan listelerinden değerleri seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-153">Under **Educational requirements**, select **Add**, and then select values from the **Education** and **Level of education** dropdowns.</span></span>

   ![Eğitim gereksinimleri Ekle](./media/hr-recruit-5-select-educational-requirements.png)

12. <span data-ttu-id="58a73-155">**Yorum** altında gerektiği şekilde yorumlar ekleyin.</span><span class="sxs-lookup"><span data-stu-id="58a73-155">Under **Comment**, add comments as necessary.</span></span>

13. <span data-ttu-id="58a73-156">**Dengeleme** altında, **düzey** açılan menüsünden bir düzey seçin ve sonra **düşük eşik**, **kontrol noktası** ve **yüksek eşik ayarlarını** gerektiği gibi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="58a73-156">Under **Compensation**, select a level from the **Level** dropdown, and then adjust **Low threshold**, **Control point**, and **High threshold** as necessary.</span></span>

14. <span data-ttu-id="58a73-157">İşe alma isteğiniz tamamlandığında ve işe alma işlemini başlatmaya hazır olduğunuzda, menü çubuğunda **Etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-157">When your recruiting request is complete and you're ready to start the recruiting process, select **Activate** in the menu bar.</span></span>

   ![İşe alma isteğini etkinleştir](./media/hr-recruit-6-activate-recruit-request.png)

15. <span data-ttu-id="58a73-159">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-159">Select **Save**.</span></span>

## <a name="view-and-edit-your-recruiting-requests"></a><span data-ttu-id="58a73-160">İşe alma isteklerinizi görüntüleyin ve düzenleyin</span><span class="sxs-lookup"><span data-stu-id="58a73-160">View and edit your recruiting requests</span></span>

<span data-ttu-id="58a73-161">Bir yönetici iseniz ve kendi isteklerinizi görüntülemek istiyorsanız:</span><span class="sxs-lookup"><span data-stu-id="58a73-161">If you're a manager and want to view your own requests:</span></span>

1. <span data-ttu-id="58a73-162">**Çalışan self servisini** seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-162">Select **Employee self service**.</span></span>

2. <span data-ttu-id="58a73-163">**Ekibim** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-163">Select the **My team** tab.</span></span>

3. <span data-ttu-id="58a73-164">**Ekip bilgilerim** altında, **İşe alma istekleri** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-164">Under **My team information**, select the **Recruiting requests** tab.</span></span>

   ![Işe alma istekleri sekmesini seçin](./media/hr-recruit-7-recruiting-requests.png)

4. <span data-ttu-id="58a73-166">İşe alma isteğini görüntülemek veya düzenlemek için bunu kılavuzda seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-166">To view or edit a recruiting request, select it in the grid.</span></span>

<span data-ttu-id="58a73-167">Bir İK Pro iseniz ve tüm işe alma isteklerini görüntülemek istiyorsanız:</span><span class="sxs-lookup"><span data-stu-id="58a73-167">If you're an HR pro and want to view all recruiting requests:</span></span>

1. <span data-ttu-id="58a73-168">**Personel yönetimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-168">Select **Personnel management**.</span></span>

2. <span data-ttu-id="58a73-169">**Işe alma istekleri** seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-169">Select **Recruiting requests**.</span></span>

   ![Personel yönetiminde işe alma isteklerini görüntüle](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. <span data-ttu-id="58a73-171">İşe alma isteğini görüntülemek veya düzenlemek için bunu kılavuzda seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-171">To view or edit a recruiting request, select it in the grid.</span></span>

## <a name="add-or-edit-a-candidate-profile"></a><span data-ttu-id="58a73-172">Aday profili ekleme veya düzenleme</span><span class="sxs-lookup"><span data-stu-id="58a73-172">Add or edit a candidate profile</span></span>

<span data-ttu-id="58a73-173">Kuruluşunuz işe alma isteklerini yönetmek için başka bir uygulamayla tümleşikse, işe alma istekleri o uygulamaya iletilir.</span><span class="sxs-lookup"><span data-stu-id="58a73-173">If your organization has integrated with another application to manage recruiting requests, recruiting requests are forwarded to that application.</span></span> <span data-ttu-id="58a73-174">İşe alma uygulaması daha sonra aday bilgilerini İnsan Kaynakları geri gönderir.</span><span class="sxs-lookup"><span data-stu-id="58a73-174">The recruiting application then sends candidate information back to Human Resources.</span></span> <span data-ttu-id="58a73-175">Aksi durumda, kendi iç işe alma işlemlerinizi takip edebilir ve aday bilgilerini el ile girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="58a73-175">Otherwise, you can follow your own internal recruiting processes and enter candidate information manually.</span></span>

1. <span data-ttu-id="58a73-176">**Personel yönetimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-176">Select **Personnel management**.</span></span>

2. <span data-ttu-id="58a73-177">**Bağlantılar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-177">Select **Links**.</span></span>

3. <span data-ttu-id="58a73-178">**İşe alma** altında **Adaylar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-178">Under **Recruiting**, select **Candidates**.</span></span>

   ![Adayları görüntüle](./media/hr-recruit-9-candidates.png)

4. <span data-ttu-id="58a73-180">Aday eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-180">To add a candidate, select **New**.</span></span> <span data-ttu-id="58a73-181">Varolan bir adayı düzenlemek için, listeden aday seçin ve **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-181">To edit an existing candidate, select the candidate from the list and then select **Edit**.</span></span> <span data-ttu-id="58a73-182">Aday profili görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="58a73-182">The candidate profile appears.</span></span>

5. <span data-ttu-id="58a73-183">**Aday Özeti** altında aday bilgilerini gerektiği gibi girin veya düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="58a73-183">Under **Candidate summary**, enter or edit the candidate information as necessary.</span></span>

6. <span data-ttu-id="58a73-184">**İşe alma isteği** altında adayı bağlamak için bir işe alma isteği seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-184">Under **Recruiting request**, select a recruiting request to link the candidate to.</span></span> <span data-ttu-id="58a73-185">**Tahmini Başlangıç tarihi**, **işe alma Yöneticisi**, **Konum** ve **Açıklama alanlarını** gerektiği gibi tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="58a73-185">Then complete the **Estimated start date**, **Hiring manager**, **Position**, and **Description fields** as appropriate.</span></span>

   ![İşe alma isteğine bağla](./media/hr-recruit-10-link-to-recruiting-request.png)

7. <span data-ttu-id="58a73-187">Aday kaydına dahil etmek istediğiniz aşağıdaki alanlardaki tüm bilgileri tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="58a73-187">Complete all the information in the following areas that you want to include in the candidate's record:</span></span>
   - <span data-ttu-id="58a73-188">**Yorumlar**</span><span class="sxs-lookup"><span data-stu-id="58a73-188">**Comments**</span></span>
   - <span data-ttu-id="58a73-189">**Mesleki deneyim**</span><span class="sxs-lookup"><span data-stu-id="58a73-189">**Professional experience**</span></span>
   - <span data-ttu-id="58a73-190">**İletişim bilgileri**</span><span class="sxs-lookup"><span data-stu-id="58a73-190">**Contact information**</span></span>
   - <span data-ttu-id="58a73-191">**Eğitim**</span><span class="sxs-lookup"><span data-stu-id="58a73-191">**Education**</span></span>
   - <span data-ttu-id="58a73-192">**Yetenekler**</span><span class="sxs-lookup"><span data-stu-id="58a73-192">**Skills**</span></span>
   - <span data-ttu-id="58a73-193">**Sertifikalar**</span><span class="sxs-lookup"><span data-stu-id="58a73-193">**Certificates**</span></span>
   - <span data-ttu-id="58a73-194">**Filtrelemeler**</span><span class="sxs-lookup"><span data-stu-id="58a73-194">**Screenings**</span></span>

8. <span data-ttu-id="58a73-195">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-195">Select **Save**.</span></span>

## <a name="hire-a-candidate"></a><span data-ttu-id="58a73-196">Adayı işe al</span><span class="sxs-lookup"><span data-stu-id="58a73-196">Hire a candidate</span></span>

<span data-ttu-id="58a73-197">Bir adayı işe almak için hazır olduğunuzda, adayı bir çalışana aktarmak için aşağıdaki yordamı izleyin.</span><span class="sxs-lookup"><span data-stu-id="58a73-197">When you're ready to hire a candidate, follow this procedure to transition the candidate to an employee.</span></span>

1. <span data-ttu-id="58a73-198">Aday formunda **işe al**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-198">On the candidate form, select **Hire**.</span></span>

   ![Adayı işe al](./media/hr-recruit-11-hire.png)

2. <span data-ttu-id="58a73-200">**İşe yeni çalışan** formunda, **Ayrıntılar** altında tüm alanları doldurun.</span><span class="sxs-lookup"><span data-stu-id="58a73-200">On the **Hire new worker** form, under **Details**, complete all the fields.</span></span>

   ![Yeni işe alma ayrıntılarını girin](./media/hr-recruit-12-hire-new-worker.png)

3. <span data-ttu-id="58a73-202">**Pozisyon ayrıntıları** altında , bilgileri gerektiği gibi doğrulayın ve değiştirin.</span><span class="sxs-lookup"><span data-stu-id="58a73-202">Under **Position details**, verify and change information as necessary.</span></span>

4. <span data-ttu-id="58a73-203">**Ekleme listeleri listesi** altında , bu çalışana ait ilgili ekleme denetim listelerini seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-203">Under **Onboarding checklists**, select the relevant onboarding checklists for this employee.</span></span>

5. <span data-ttu-id="58a73-204">Çalışan kaydını oluşturmak için **devam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-204">Select **Continue** to create the employee record.</span></span>

   >[!NOTE]
   ><span data-ttu-id="58a73-205">Kuruluşunuzun iş akışlarına bağlı olarak, aday kaydı, bir çalışan kaydı yapılmadan önce ek onay adımlarıyla geçebilir.</span><span class="sxs-lookup"><span data-stu-id="58a73-205">Depending on your organization's workflows, the candidate record may go through additional approval steps before becoming an employee record.</span></span>

## <a name="decide-not-to-hire-a-candidate"></a><span data-ttu-id="58a73-206">Aday işe gerekmediğine karar verme</span><span class="sxs-lookup"><span data-stu-id="58a73-206">Decide not to hire a candidate</span></span>

<span data-ttu-id="58a73-207">Bir adayı işe gerekmediğine karar verirseniz, aşağıdaki yordamı izleyerek onları vetele alma işleminden çıkarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="58a73-207">If you decide not to hire a candidate, follow this procedure to remove them from the vetting process.</span></span> 

1. <span data-ttu-id="58a73-208">Aday formunda **işe alma**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-208">On the candidate form, select **Do not hire**.</span></span>

   ![Adayı işe alma](./media/hr-recruit-13-do-not-hire.png)

2. <span data-ttu-id="58a73-210">Bir **neden kodu** seçin ve açıklama ekleyin.</span><span class="sxs-lookup"><span data-stu-id="58a73-210">Select a **Reason code** and include any comments.</span></span>

3. <span data-ttu-id="58a73-211">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-211">Select **OK**.</span></span>

## <a name="dismiss-a-candidate"></a><span data-ttu-id="58a73-212">Adayı kapat</span><span class="sxs-lookup"><span data-stu-id="58a73-212">Dismiss a candidate</span></span>

<span data-ttu-id="58a73-213">Gerekirse, bir adayı işe aldıktan sonra kapatabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="58a73-213">If needed, you can dismiss a candidate after hiring them.</span></span> <span data-ttu-id="58a73-214">Örneğin, bir aday teklifinizi reddedebilir veya ilk gününde göstermeyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="58a73-214">For example, a candidate might reject your offer or not show up on their first day.</span></span>

- <span data-ttu-id="58a73-215">Aday formunda **Adayı kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="58a73-215">On the candidate form, select **Dismiss candidate**.</span></span>

  ![Adayı bırakın.](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a><span data-ttu-id="58a73-217">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="58a73-217">See also</span></span>

[<span data-ttu-id="58a73-218">Common Data Service sanal varlıklarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="58a73-218">Configure Common Data Service virtual entities</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="58a73-219">İş gücünüzü düzenleme</span><span class="sxs-lookup"><span data-stu-id="58a73-219">Organize your workforce</span></span>](hr-personnel-departments-jobs-positions.md)<br>
[<span data-ttu-id="58a73-220">İşin bileşenlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="58a73-220">Set up the components of a job</span></span>](hr-personnel-jobs.md)