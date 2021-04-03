---
title: LinkedIn Talent Hub ile tümleştirme
description: Bu konu Microsoft Dynamics 365 Human Resources ile LinkedIn Talent Hub arasında tümleştirmeyi ayarlamayı açıklar.
author: jaredha
manager: tfehr
ms.date: 10/20/2020
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
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2a017d67177bcbee86abf920cf8d83f37312c5eb
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465210"
---
# <a name="integrate-with-linkedin-talent-hub"></a><span data-ttu-id="8c762-103">LinkedIn Talent Hub ile tümleştirme</span><span class="sxs-lookup"><span data-stu-id="8c762-103">Integrate with LinkedIn Talent Hub</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [banner](includes/preview-feature.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="8c762-104">[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) bir başvuran izleme sistemi (ATS) platformudur.</span><span class="sxs-lookup"><span data-stu-id="8c762-104">[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) is an applicant tracking system (ATS) platform.</span></span> <span data-ttu-id="8c762-105">Tek bir yerden çalışanları bulmanıza, yönetmenize ve işe almanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="8c762-105">It lets you source, manage, and hire employees all in one place.</span></span> <span data-ttu-id="8c762-106">Microsoft Dynamics 365 Human Resources ile LinkedIn Talent Hub'ı tümleştirerek bir pozisyon için işe alınan kişiler için Human Resources'da kolayca çalışan kayıtları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8c762-106">By integrating Microsoft Dynamics 365 Human Resources with LinkedIn Talent Hub, you can easily create employee records in Human Resources for applicants who have been hired for a position.</span></span>

## <a name="setup"></a><span data-ttu-id="8c762-107">Ayar</span><span class="sxs-lookup"><span data-stu-id="8c762-107">Setup</span></span>

<span data-ttu-id="8c762-108">Bir sistem yöneticisinin LinkedIn Talent Hub ile tümleştirmeyi etkinleştirmek için kurulum görevlerini tamamlaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="8c762-108">A system administrator must complete setup tasks to enable integration with LinkedIn Talent Hub.</span></span> <span data-ttu-id="8c762-109">Öncelikle, LinkedIn Talent Hub'a Human Resources'a veri yazmak için uygun izinleri vermek üzere Power Apps ortamında bir kullanıcı ve güvenlik rolü ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="8c762-109">First, in the Power Apps environment, you must set up a user and security role to grant LinkedIn Talent Hub the appropriate permissions to write data into Human Resources.</span></span>

### <a name="link-your-environment-to-linkedin-talent-hub"></a><span data-ttu-id="8c762-110">Ortamınızı LinkedIn Talent Hub'a bağlayın</span><span class="sxs-lookup"><span data-stu-id="8c762-110">Link your environment to LinkedIn Talent Hub</span></span>

1. <span data-ttu-id="8c762-111">[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub)'ı açın.</span><span class="sxs-lookup"><span data-stu-id="8c762-111">Open [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).</span></span>

2. <span data-ttu-id="8c762-112">Kullanıcı açılan menüsünde **Ürün Ayarları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="8c762-112">On the user drop-down menu, select **Product Settings**.</span></span>

3. <span data-ttu-id="8c762-113">Sol gezinti bölmesinde, **Gelişmiş** bölümünde, **Tümleştirmeler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8c762-113">In the left navigation pane, in the **Advanced** section, select **Integrations**.</span></span>

4. <span data-ttu-id="8c762-114">Microsoft Dynamics 365 Human Resources tümleştirmesi için **Yetkilendir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8c762-114">Select **Authorize** for the Microsoft Dynamics 365 Human Resources integration.</span></span>

5. <span data-ttu-id="8c762-115">**Dynamics 365 Human Resources** sayfasında LinkedIn Talent Hub'ı bağlayacağınız ortamı seçin ve sonra **Bağla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="8c762-115">On the **Dynamics 365 Human Resources** page, select the environment to link LinkedIn Talent Hub to, and then select **Link**.</span></span>

    ![LinkedIn Talent Hub işe alma](./media/hr-admin-integration-talent-hub-onboarding.jpg)

    > [!NOTE]
    > <span data-ttu-id="8c762-117">Yalnızca Kullanıcı hesabınızın, hem Human Resources ortamında hem de ilişkili Power Apps ortamında yönetici erişimi olan ortamlara bağlanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8c762-117">You can link only to environments where your user account has administrator access to both the Human Resources environment and the associated Power Apps environment.</span></span> <span data-ttu-id="8c762-118">Human Resources bağlantı sayfasında herhangi bir ortam listelenmiyorsa, Human Resources ortamlarını kiracıda lisansladığınızdan ve bağlantı sayfasında oturum açmış olan kullanıcının hem Human Resources ortamı hem de Power Apps ortamı için yönetici izinlerine sahip olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="8c762-118">If no environments are listed on the Human Resources link page, make sure that you have licensed Human Resources environments on the tenant, and that the user that you signed in to the link page as has administrator permissions to both the Human Resources environment and the Power Apps environment.</span></span>

### <a name="create-a-power-apps-security-role"></a><span data-ttu-id="8c762-119">Power Apps Güvenlik rolü oluşturma</span><span class="sxs-lookup"><span data-stu-id="8c762-119">Create a Power Apps security role</span></span>

1. <span data-ttu-id="8c762-120">[Power Platform Yönetim Merkezi](https://admin.powerplatform.microsoft.com)'ni açın.</span><span class="sxs-lookup"><span data-stu-id="8c762-120">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="8c762-121">**Ortamlar** listesinde, LinkedIn Talent Hub örneğinizi bağlamak istediğiniz Human Resources ortamıyla ilişkilendirilmiş ortamı seçin.</span><span class="sxs-lookup"><span data-stu-id="8c762-121">In the **Environments** list, select the environment that is associated with the Human Resources environment that you want to link your instance of LinkedIn Talent Hub to.</span></span>

3. <span data-ttu-id="8c762-122">**Ayarlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8c762-122">Select **Settings**.</span></span>

4. <span data-ttu-id="8c762-123">**Kullanıcılar + izinler** düğümünü genişletin ve **Güvenlik rolleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="8c762-123">Expand the **Users + Permissions** node, and select **Security Roles**.</span></span>

5. <span data-ttu-id="8c762-124">**Güvenlik rolleri** sayfasında, araç çubuğunda **Yeni rol**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="8c762-124">On the **Security Roles** page, on the toolbar, select **New role**.</span></span>

6. <span data-ttu-id="8c762-125">**Ayrıntılar** sekmesinde, **LinkedIn Talent Hub HRIS tümleştirmesi** gibi rol için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="8c762-125">On the **Details** tab, enter a name for the role, such as **LinkedIn Talent Hub HRIS Integration**.</span></span>

7. <span data-ttu-id="8c762-126">**Özelleştirme** sekmesinde, aşağıdaki varlıklar için kuruluş düzeyinde **okuma** izni seçin:</span><span class="sxs-lookup"><span data-stu-id="8c762-126">On the **Customization** tab, select organization-level **Read** permission for the following entities:</span></span>

    - <span data-ttu-id="8c762-127">Varlık</span><span class="sxs-lookup"><span data-stu-id="8c762-127">Entity</span></span>
    - <span data-ttu-id="8c762-128">Alan</span><span class="sxs-lookup"><span data-stu-id="8c762-128">Field</span></span>
    - <span data-ttu-id="8c762-129">Yakınlık derecesi</span><span class="sxs-lookup"><span data-stu-id="8c762-129">Relationship</span></span>

8. <span data-ttu-id="8c762-130">Güvenlik rolünü kaydedin ve kapatın.</span><span class="sxs-lookup"><span data-stu-id="8c762-130">Save and close the security role.</span></span>

### <a name="create-a-power-apps-application-user"></a><span data-ttu-id="8c762-131">Power Apps uygulaması kullanıcısı oluşturun</span><span class="sxs-lookup"><span data-stu-id="8c762-131">Create a Power Apps application user</span></span>

<span data-ttu-id="8c762-132">Aday kayıtlarını Power Apps ortamına yazmak için bağdaştırıcıya gereken izinleri vermek amacıyla LinkedIn Talent Hub bağdaştırıcısı için bir uygulama kullanıcısı oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8c762-132">An application user must be created for the LinkedIn Talent Hub adapter to grant permissions to the adapter to write candidate records into the Power Apps environment.</span></span>

1. <span data-ttu-id="8c762-133">[Power Platform Yönetim Merkezi](https://admin.powerplatform.microsoft.com)'ni açın.</span><span class="sxs-lookup"><span data-stu-id="8c762-133">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="8c762-134">**Ortamlar** listesinde, LinkedIn Talent Hub örneğinizi bağlamak istediğiniz Human Resources ortamıyla ilişkilendirilmiş ortamı seçin.</span><span class="sxs-lookup"><span data-stu-id="8c762-134">In the **Environments** list, select the environment that is associated with the Human Resources environment that you want to link your instance of LinkedIn Talent Hub to.</span></span>

3. <span data-ttu-id="8c762-135">**Ayarlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8c762-135">Select **Settings**.</span></span>

4. <span data-ttu-id="8c762-136">**Kullanıcılar + izinler** düğümünü genişletin ve **Kullanıcılar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8c762-136">Expand the **Users + Permissions** node, and select **Users**.</span></span>

5. <span data-ttu-id="8c762-137">**Dynamics 365'te kullanıcıları Yönet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8c762-137">Select **Manage users in Dynamics 365**.</span></span>

6. <span data-ttu-id="8c762-138">Görünümü varsayılan **etkin kullanıcılar** görünümünden **uygulama kullanıcıları** görünümüne değiştirmek için listenin üzerindeki açılan menüyü kullanın.</span><span class="sxs-lookup"><span data-stu-id="8c762-138">Use the drop-down menu above the list to change the view from the default **Enabled Users** view to **Application Users**.</span></span>

    ![Uygulama Kullanıcıları görünümü](./media/hr-admin-integration-power-apps-application-users.jpg)

7. <span data-ttu-id="8c762-140">Araç çubuğunda **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8c762-140">On the toolbar, select **New**.</span></span>

8. <span data-ttu-id="8c762-141">**Yeni kullanıcı** sayfası üzerinde, aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="8c762-141">On the **New user** page, follow these steps:</span></span>

    1. <span data-ttu-id="8c762-142">**Kullanıcı türü** alanının değerini **Uygulama Kullanıcısı** olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="8c762-142">Change the value of the **User type** field to **Application User**.</span></span>
    2. <span data-ttu-id="8c762-143">**Kullanıcı adı** alanını **Dynamics365 HR LinkedIn HRIS tümleştirmesine** ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="8c762-143">Set the **User Name** field to **Dynamics365 HR LinkedIn HRIS Integration**.</span></span>
    3. <span data-ttu-id="8c762-144">**Uygulama Kimliği** alanını **3a225c96-d62a-44ce-b3ec-bd4e8e9befef** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="8c762-144">Set the **Application ID** field to **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span></span>
    4. <span data-ttu-id="8c762-145">**Adı**, **Soyadı** ve **birincil e-posta** alanlarına herhangi bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="8c762-145">Enter any value in the **First Name**, **Last Name**, and **Primary Email** fields.</span></span>
    5. <span data-ttu-id="8c762-146">Araç çubuğunda **Kaydet\& Kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8c762-146">On the toolbar, select **Save \& Close**.</span></span>

### <a name="assign-a-security-role-to-the-new-user"></a><span data-ttu-id="8c762-147">Yeni kullanıcıya güvenlik rolü atama</span><span class="sxs-lookup"><span data-stu-id="8c762-147">Assign a security role to the new user</span></span>

<span data-ttu-id="8c762-148">Önceki bölümde yeni uygulama kullanıcısını kaydettikten ve kapattıktan sonra, **kullanıcılar listesi** sayfasına geri dönülür.</span><span class="sxs-lookup"><span data-stu-id="8c762-148">After you save and close the new application user in the previous section, you're returned to the **Users list** page.</span></span>

1. <span data-ttu-id="8c762-149">**Kullanıcılar listesi** sayfasında, görünümü **uygulama kullanıcıları** olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="8c762-149">On the **Users list** page, change the view to **Application Users**.</span></span>

2. <span data-ttu-id="8c762-150">Önceki bölümde oluşturduğunuz uygulama kullanıcısını seçin.</span><span class="sxs-lookup"><span data-stu-id="8c762-150">Select the application user that you created in the previous section.</span></span>

3. <span data-ttu-id="8c762-151">Araç çubuğunda **Rolleri Yönet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8c762-151">On the toolbar, select **Manage Roles**.</span></span>

4. <span data-ttu-id="8c762-152">Tümleştirme için daha önce oluşturduğunuz güvenlik rolünü seçin.</span><span class="sxs-lookup"><span data-stu-id="8c762-152">Select the security role that you created earlier for the integration.</span></span>

5. <span data-ttu-id="8c762-153">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8c762-153">Select **OK**.</span></span>

### <a name="add-an-azure-active-directory-app-in-human-resources"></a><span data-ttu-id="8c762-154">Human Resources'ta bir Azure Active Directory uygulaması ekleme</span><span class="sxs-lookup"><span data-stu-id="8c762-154">Add an Azure Active Directory app in Human Resources</span></span>

1. <span data-ttu-id="8c762-155">Dynamics 365 Human Resources'ta **Azure Active Directory uygulamaları** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="8c762-155">In Dynamics 365 Human Resources, open the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="8c762-156">Listeye yeni bir kayıt ekleyin ve aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="8c762-156">Add a new record to the list, and set the following fields:</span></span>

    - <span data-ttu-id="8c762-157">**İstemci kimliği**: **3a225c96-d62a-44ce-b3ec-bd4e8e9befef** değerini girin.</span><span class="sxs-lookup"><span data-stu-id="8c762-157">**Client ID**: Enter **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span></span>
    - <span data-ttu-id="8c762-158">**Ad**: **LinkedIn Talent Hub HRIS tümleştirmesi** gibi daha önce oluşturduğunuz Power Apps güvenlik rolünün adını girin.</span><span class="sxs-lookup"><span data-stu-id="8c762-158">**Name**: Enter the name of the Power Apps security role that you created earlier, such as **LinkedIn Talent Hub HRIS Integration**.</span></span>
    - <span data-ttu-id="8c762-159">**Kullanıcı kimliği**: Personel yönetiminde veri yazma izni olan bir kullanıcı seçin.</span><span class="sxs-lookup"><span data-stu-id="8c762-159">**User ID**: Select a user who has permissions to write data in Personnel Management.</span></span>

### <a name="create-the-table-in-dataverse"></a><span data-ttu-id="8c762-160">Tabloyu Dataverse'te oluşturma</span><span class="sxs-lookup"><span data-stu-id="8c762-160">Create the table in Dataverse</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8c762-161">LinkedIn Talent Hub ile tümleştirme, Human Resources için Dataverse'te sanal tablolara bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="8c762-161">The integration with LinkedIn Talent Hub depends on virtual tables in Dataverse for Human Resources.</span></span> <span data-ttu-id="8c762-162">Kurulumda bu adım için bir önkoşul olarak, sanal tablolar yapılandırmalısınız.</span><span class="sxs-lookup"><span data-stu-id="8c762-162">As a prerequisite for this step in the setup, you must configure virtual tables.</span></span> <span data-ttu-id="8c762-163">Sanal tabloların nasıl yapılandırılacağı hakkında bilgi için bkz. [Dataverse sanal tablolarını yapılandırma](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span><span class="sxs-lookup"><span data-stu-id="8c762-163">For information about how to configure virtual tables, see [Configure Dataverse virtual tables](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span></span>

1. <span data-ttu-id="8c762-164">Human Resources'ta **Dataverse tümleştirmesi** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="8c762-164">In Human Resources, open the **Dataverse integration** page.</span></span>

2. <span data-ttu-id="8c762-165">**Sanal tablolar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8c762-165">Select the **Virtual tables** tab.</span></span>

3. <span data-ttu-id="8c762-166">**LinkedIn dışa aktarılan aday**'ı bulmak için varlık listesini varlık etiketine göre filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="8c762-166">Filter the entity list by entity label to find **LinkedIn exported candidate**.</span></span>

4. <span data-ttu-id="8c762-167">Varlığı ve ardından **Oluştur/Yenile**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8c762-167">Select the entity, and then select **Generate/refresh**.</span></span>

## <a name="exporting-candidate-records"></a><span data-ttu-id="8c762-168">Aday kayıtlarını dışa aktarma</span><span class="sxs-lookup"><span data-stu-id="8c762-168">Exporting candidate records</span></span>

<span data-ttu-id="8c762-169">Kurulum tamamlandıktan sonra, işe alma ve İnsan kaynakları (HR) uzmanları, işe alınan aday kayıtlarını LinkedIn Talent Hub'dan Human Resources'a dışa aktarmak için LinkedIn Talent Hub'daki **HRIS'e Dışarı Aktar** işlevini kullanabilirler.</span><span class="sxs-lookup"><span data-stu-id="8c762-169">After the setup is completed, recruiters and human resources (HR) professionals can use the **Export to HRIS** function in LinkedIn Talent Hub to export hired candidate records from LinkedIn Talent Hub to Human Resources.</span></span>

### <a name="export-records-from-linkedin-talent-hub"></a><span data-ttu-id="8c762-170">LinkedIn Talent Hub'dan kayıtları dışa aktar</span><span class="sxs-lookup"><span data-stu-id="8c762-170">Export records from LinkedIn Talent Hub</span></span>

<span data-ttu-id="8c762-171">Bir aday işe alma sürecinden geçip işe alındığında, aday kaydını LinkedIn Talent Hub'dan Human Resources'a dışa aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8c762-171">After a candidate has moved through the recruiting process and has been hired, you can export the candidate record from LinkedIn Talent Hub to Human Resources.</span></span>

1. <span data-ttu-id="8c762-172">LinkedIn Talent Hub'da yeni çalışanın çalışacağı projeyi açın.</span><span class="sxs-lookup"><span data-stu-id="8c762-172">In LinkedIn Talent Hub, open the project that you hired the new employee for.</span></span>

2. <span data-ttu-id="8c762-173">Bir aday kaydı seçin.</span><span class="sxs-lookup"><span data-stu-id="8c762-173">Select a candidate record.</span></span>

3. <span data-ttu-id="8c762-174">**Aşamayı değiştir**'i ve ardından **İşe alındı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="8c762-174">Select **Change stage**, and then select **Hired**.</span></span>

4. <span data-ttu-id="8c762-175">Aday için üç nokta menüsünde (**...**) **HRIS'e Dışa Aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8c762-175">On the ellipsis menu (**...**) for the candidate, select **Export to HRIS**.</span></span>

5. <span data-ttu-id="8c762-176">**HRIS'e Dışa aktar** bölmesinde, dışa aktarılması gereken bilgileri girin:</span><span class="sxs-lookup"><span data-stu-id="8c762-176">In the **Export to HRIS** pane, enter the information that must be exported:</span></span>

    - <span data-ttu-id="8c762-177">**HRIS sağlayıcısı** alanında **Microsoft Dynamics 365 Human Resources**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8c762-177">In the **HRIS provider** field, select **Microsoft Dynamics 365 Human Resources**.</span></span>
    - <span data-ttu-id="8c762-178">**Başlangıç tarihi** alanında yeni çalışan için bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="8c762-178">In the **Start date** field, select a value for the new employee.</span></span>
    - <span data-ttu-id="8c762-179">**İş unvanı** alanına, yeni çalışanın işi için bir iş unvanı girin.</span><span class="sxs-lookup"><span data-stu-id="8c762-179">In the **Job title** field, enter a job title for the new employee's job.</span></span>
    - <span data-ttu-id="8c762-180">**Konum** alanına, çalışanın çalışacağı konumu girin.</span><span class="sxs-lookup"><span data-stu-id="8c762-180">In the **Location** field, enter the location where the employee will be based.</span></span>
    - <span data-ttu-id="8c762-181">Çalışanın e-posta adresini girin veya doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="8c762-181">Enter or verify the employee's email address.</span></span>

![LinkedIn Talent Hub'da HRIS'e Dışa Aktar bölmesi](./media/hr-admin-integration-linkedin-talent-hub-export.jpg)

## <a name="complete-onboarding-in-human-resources"></a><span data-ttu-id="8c762-183">Human Resources'ta işe almayı tamamlama</span><span class="sxs-lookup"><span data-stu-id="8c762-183">Complete onboarding in Human Resources</span></span>

<span data-ttu-id="8c762-184">LinkedIn Talent Hub'dan Human Resources'a dışa aktarılan aday kayıtları **personel yönetimi** sayfasının **işe alınacak adaylar** bölümünde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="8c762-184">Candidate records that are exported from LinkedIn Talent Hub to Human Resources appear in the **Candidates to hire** section of the **Personnel management** page.</span></span>

1. <span data-ttu-id="8c762-185">Human Resources'da, **Personel yönetimi** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="8c762-185">In Human Resources, open the **Personnel management** page.</span></span>

2. <span data-ttu-id="8c762-186">**İşe alınacak adaylar** bölümünde, Seçilen aday için **İşe al**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8c762-186">In the **Candidates to hire** section, select **Hire** for the selected candidate.</span></span>

3. <span data-ttu-id="8c762-187">**Yeni çalışanı işe al** iletişim kutusunda, kaydı inceleyin ve gerekli bilgileri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="8c762-187">In the **Hire new worker** dialog box, review the record, and add any required information.</span></span> <span data-ttu-id="8c762-188">Ayrıca, adayın işe alındığı pozisyon numarasını da seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8c762-188">You can also select the position number that the candidate has been hired for.</span></span>

<span data-ttu-id="8c762-189">Gerekli bilgiler girildikten sonra, çalışan kayıtlarını oluşturmak ve çalışanların işe başlamasını sağlamak için standart işlemlerinize devam edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8c762-189">After the required information has been entered, you can continue with your standard processes for creating employee records and onboarding employees.</span></span>

<span data-ttu-id="8c762-190">Aşağıdaki ayrıntılar içe aktarılır ve yeni çalışan kaydına dahil edilir:</span><span class="sxs-lookup"><span data-stu-id="8c762-190">The following details are imported and included on the new employee record:</span></span>

- <span data-ttu-id="8c762-191">Adı</span><span class="sxs-lookup"><span data-stu-id="8c762-191">First name</span></span>
- <span data-ttu-id="8c762-192">Soyadı</span><span class="sxs-lookup"><span data-stu-id="8c762-192">Last name</span></span>
- <span data-ttu-id="8c762-193">İstihdam başlama tarihi</span><span class="sxs-lookup"><span data-stu-id="8c762-193">Employment start date</span></span>
- <span data-ttu-id="8c762-194">E-posta adresi</span><span class="sxs-lookup"><span data-stu-id="8c762-194">Email address</span></span>
- <span data-ttu-id="8c762-195">Telefon numarası</span><span class="sxs-lookup"><span data-stu-id="8c762-195">Phone number</span></span>

## <a name="see-also"></a><span data-ttu-id="8c762-196">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="8c762-196">See also</span></span>

[<span data-ttu-id="8c762-197">Dataverse sanal tablolarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="8c762-197">Configure Dataverse virtual tables</span></span>](./hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="8c762-198">Microsoft Dataverse nedir?</span><span class="sxs-lookup"><span data-stu-id="8c762-198">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)


[!INCLUDE[footer-include](../includes/footer-banner.md)]