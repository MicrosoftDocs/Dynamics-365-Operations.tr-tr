---
title: Common Data Service sanal varlıklarını yapılandırma
description: Bu konu, Dynamics 365 Human Resources için sanal varlıkların nasıl yapılandırılacağını göstermektedir. Mecvut sanal varlıkları oluşturun ve güncelleştirin ve oluşturulan ve kullanılabilir varlıkları inceleyin.
author: andreabichsel
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0848b7556100fba38fcab0aa2a1a109e2e055fc9
ms.sourcegitcommit: b89baab13e530b5b1f079231619c628309a4742d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/05/2020
ms.locfileid: "3959587"
---
# <a name="configure-common-data-service-virtual-entities"></a><span data-ttu-id="19363-104">Common Data Service sanal varlıklarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="19363-104">Configure Common Data Service virtual entities</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="19363-105">Dynamics 365 Human Resources Common Data Service'taki sanal bir veri kaynağıdır.</span><span class="sxs-lookup"><span data-stu-id="19363-105">Dynamics 365 Human Resources is a virtual data source in Common Data Service.</span></span> <span data-ttu-id="19363-106">Common Data Service ve Microsoft Power Platform'dan tam oluşturma, okuma, güncelleştirme ve silme (CRUD) işlemleri sağlar.</span><span class="sxs-lookup"><span data-stu-id="19363-106">It provides full create, read, update, and delete (CRUD) operations from Common Data Service and Microsoft Power Platform.</span></span> <span data-ttu-id="19363-107">Sanal varlıkların verileri Common Data Service'de depolanmaz , ancak uygulama veritabanında depolanır.</span><span class="sxs-lookup"><span data-stu-id="19363-107">The data for virtual entities isn't stored in Common Data Service, but in the application database.</span></span> 

<span data-ttu-id="19363-108">Human Resources varlıklarındaki CRUD işlemlerini Common Data Service'den etkinleştirmek için, varlıkları Common Data Service'de sanal varlıklar olarak kullanılabilir yapmalısınız.</span><span class="sxs-lookup"><span data-stu-id="19363-108">To enable CRUD operations on Human Resources entities from Common Data Service, you must make the entities available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="19363-109">Bu, Common Data Service ve Microsoft Power Platform'dan Human Resources'daki veriler üzerinde CRUD işlemleri gerçekleştirmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="19363-109">This lets you perform CRUD operations from Common Data Service and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="19363-110">Operasyonlar, varlıklara veri yazarken veri bütünlüğünü sağlamak için Human Resources'ın tam iş mantığı doğrulamalarını da destekler.</span><span class="sxs-lookup"><span data-stu-id="19363-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

## <a name="available-virtual-entities-for-human-resources"></a><span data-ttu-id="19363-111">Human Resources için kullanılabilir sanal varlıklar</span><span class="sxs-lookup"><span data-stu-id="19363-111">Available virtual entities for Human Resources</span></span>

<span data-ttu-id="19363-112">Human Resources'taki tüm Açık Veri Protokolü (OData) varlıkları Common Data Service'de sanal varlıklar olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="19363-112">All Open Data Protocol (OData) entities in Human Resources are available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="19363-113">Bunlar Power Platform uygulamasında da kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="19363-113">They're also available in Power Platform.</span></span> <span data-ttu-id="19363-114">Artık verileri Common Data Service'a kopyalamadan veya eşitlemeden doğrudan Human Resources'dan tam CRUD özelliği ile verileri kullanarak uygulamalar ve deneyimler oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="19363-114">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Common Data Service.</span></span> <span data-ttu-id="19363-115">Human Resources'taki iş süreçleri için işbirliği senaryolarını etkinleştiren, harici tabanlı web siteleri oluşturmak için Power Apps portallarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="19363-115">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="19363-116">Ortamda etkinleştirilmiş sanal varlıkların listesini görüntüleyebilir ve [Power Apps](https://make.powerapps.com) içindeki varlıklarla **Dynamics 365 HR Sanal Varlıklar** çözümünde çalışmaya başlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="19363-116">You can view the list of virtual entities enabled in the environment, and begin working with the entities in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Entities** solution.</span></span>

![Power Apps'taki Dynamics 365 HR Sanal Varlıkları](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a><span data-ttu-id="19363-118">Sanal varlıklar ve doğal varlıklar</span><span class="sxs-lookup"><span data-stu-id="19363-118">Virtual entities versus natural entities</span></span>

<span data-ttu-id="19363-119">Human Resources için sanal varlıklar, Common Data Service'taki Human Resources için oluşturulan doğal varlıklarla aynı değildir.</span><span class="sxs-lookup"><span data-stu-id="19363-119">Virtual entities for Human Resources aren't the same as the natural Common Data Service entities created for Human Resources.</span></span> <span data-ttu-id="19363-120">Human Resources için doğal varlıklar ayrı olarak oluşturulur ve Common Data Service'deki HCM Ortak çözümünde tutulur.</span><span class="sxs-lookup"><span data-stu-id="19363-120">The natural entities for Human Resources are generated separately and maintained in the HCM Common solution in Common Data Service.</span></span> <span data-ttu-id="19363-121">Doğal varlıklarla, veriler Common Data Service'ta depolanır ve Human Resources uygulama veritabanıyla eşitleme gerektirir.</span><span class="sxs-lookup"><span data-stu-id="19363-121">With natural entities, the data is stored in Common Data Service and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="19363-122">Human Resources için Common Data Service doğal varlıkların listesi için bkz. [Common Data Service varlıkları](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span><span class="sxs-lookup"><span data-stu-id="19363-122">For a list of the natural Common Data Service entities for Human Resources, see [Common Data Service entities](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="19363-123">Ayar</span><span class="sxs-lookup"><span data-stu-id="19363-123">Setup</span></span>

<span data-ttu-id="19363-124">Ortamınızdaki sanal varlıkları etkinleştirmek için bu kurulum adımlarını izleyin.</span><span class="sxs-lookup"><span data-stu-id="19363-124">Follow these setup steps to enable virtual entities in your environment.</span></span> 

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="19363-125">Microsoft Azure'da uygulamayı kaydetme</span><span class="sxs-lookup"><span data-stu-id="19363-125">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="19363-126">İlk olarak, uygulamayı Azure portalında kaydetmeniz gerekir; böylece Microsoft kimlik platformu uygulama ve kullanıcılar için kimlik doğrulama ve yetkilendirme hizmetleri sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="19363-126">First, you need to register the app in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="19363-127">Azure'da uygulama kaydetme hakkında daha fazla bilgi için bkz. [Hızlı başlangıç: Microsoft kimlik platform ile uygulama kaydetme](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="19363-127">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="19363-128">[Microsoft Azure portalını](https://portal.azure.com) açın.</span><span class="sxs-lookup"><span data-stu-id="19363-128">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="19363-129">Azure hizmetleri listesinde **Uygulama kayıtları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="19363-129">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="19363-130">**Yeni kayıt** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="19363-130">Select **New registration**.</span></span>

4. <span data-ttu-id="19363-131">**Ad** alanına uygulama için açıklayıcı bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="19363-131">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="19363-132">Örneğin, **Dynamics 365 Human Resources Sanal Varlıkları**.</span><span class="sxs-lookup"><span data-stu-id="19363-132">For example, **Dynamics 365 Human Resources Virtual Entities**.</span></span>

5. <span data-ttu-id="19363-133">**Yeniden yönlendirme URI'si** alanında Human Resources kurulumunuzun ad alanı URL'sini girin.</span><span class="sxs-lookup"><span data-stu-id="19363-133">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="19363-134">**Kayıt**'ı seç.</span><span class="sxs-lookup"><span data-stu-id="19363-134">Select **Register**.</span></span>

7. <span data-ttu-id="19363-135">Kayıt tamamlandığında, Azure portalı uygulama kaydı **Uygulama (istemci) kimliğini** de içeren **Genel bakış** bölmesini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="19363-135">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="19363-136">Şu anda **Uygulama (istemci) kimliğini** not edin.</span><span class="sxs-lookup"><span data-stu-id="19363-136">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="19363-137">[Sanal varlık veri kaynağını yapılandırırken](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source) bu bilgileri gireceksiniz.</span><span class="sxs-lookup"><span data-stu-id="19363-137">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

8. <span data-ttu-id="19363-138">Sol gezinti bölmesinde, **Sertifikalar ve gizli anahtarlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="19363-138">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="19363-139">Sayfanın **İstemci gizli anahtarı** bölümünde **Yeni istemci gizli anahtarı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="19363-139">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="19363-140">Bir açıklama sağlayın, bir süre seçin ve **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="19363-140">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="19363-141">Gizli anahtar değerini kaydedin.</span><span class="sxs-lookup"><span data-stu-id="19363-141">Record the secret's value.</span></span> <span data-ttu-id="19363-142">[Sanal varlık veri kaynağını yapılandırırken](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source) bu bilgileri gireceksiniz.</span><span class="sxs-lookup"><span data-stu-id="19363-142">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="19363-143">Bu aşamada, gizli anahtarın değerini not aldığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="19363-143">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="19363-144">Bu sayfadan ayrıldıktan sonra gizli anahtar hiçbir zaman görüntülenmez.</span><span class="sxs-lookup"><span data-stu-id="19363-144">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a><span data-ttu-id="19363-145">Dynamics 365 HR Sanal Varlık uygulamasını yükleme</span><span class="sxs-lookup"><span data-stu-id="19363-145">Install the Dynamics 365 HR Virtual Entity app</span></span>

<span data-ttu-id="19363-146">Sanal varlık çözüm paketini Common Data Service'a dağıtmak için Dynamics 365 HR Sanal Varlık uygulamasını Power Apps ortamınıza yükleyin.</span><span class="sxs-lookup"><span data-stu-id="19363-146">Install the Dynamics 365 HR Virtual Entity app in your Power Apps environment to deploy the virtual entity solution package to Common Data Service.</span></span>

1. <span data-ttu-id="19363-147">[Power Platform Yönetim Merkezi](https://admin.powerplatform.microsoft.com)'ni açın.</span><span class="sxs-lookup"><span data-stu-id="19363-147">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="19363-148">**Ortamlar** listesinde, Human Resources kurulumunuzla ilişkilendirilen Power Apps ortamını seçin.</span><span class="sxs-lookup"><span data-stu-id="19363-148">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="19363-149">Sayfanın **Kaynaklar** bölümünde **Dynamics 365 uygulamaları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="19363-149">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="19363-150">**Uygulamayı yükle** eylemini seçin.</span><span class="sxs-lookup"><span data-stu-id="19363-150">Select the **Install app** action.</span></span>

5. <span data-ttu-id="19363-151">**Dynamics 365 HR Sanal Varlık** öğesini ve **İleri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="19363-151">Select **Dynamics 365 HR Virtual Entity**, and select **Next**.</span></span>

6. <span data-ttu-id="19363-152">Hizmet koşullarını gözden geçirin ve kabul etmek için işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="19363-152">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="19363-153">**Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="19363-153">Select **Install**.</span></span>

<span data-ttu-id="19363-154">Yükleme birkaç dakika sürer.</span><span class="sxs-lookup"><span data-stu-id="19363-154">The install takes a few minutes.</span></span> <span data-ttu-id="19363-155">Bu işlem tamamlandığında sonraki adımlara devam edin.</span><span class="sxs-lookup"><span data-stu-id="19363-155">When it completes, continue to the next steps.</span></span>

![Dynamics 365 HR Sanal Varlık uygulamasını Power Platform yönetim merkezinden yükleyin](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a><span data-ttu-id="19363-157">Sanal varlık veri kaynağını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="19363-157">Configure the virtual entity data source</span></span> 

<span data-ttu-id="19363-158">Sonraki adım, sanal varlık veri kaynağını Power Apps ortamında yapılandırmaktır.</span><span class="sxs-lookup"><span data-stu-id="19363-158">The next step is to configure the virtual entity data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="19363-159">[Power Platform Yönetim Merkezi](https://admin.powerplatform.microsoft.com)'ni açın.</span><span class="sxs-lookup"><span data-stu-id="19363-159">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="19363-160">**Ortamlar** listesinde, Human Resources kurulumunuzla ilişkilendirilen Power Apps ortamını seçin.</span><span class="sxs-lookup"><span data-stu-id="19363-160">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="19363-161">Sayfanın **Ayrıntılar** bölümünde **Ortam URL**'sini seçin.</span><span class="sxs-lookup"><span data-stu-id="19363-161">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="19363-162">**Çözüm Durumu Merkezi**'nde, uygulama sayfasının sağ üst kısmında **Gelişmiş Bul** simgesini seçin.</span><span class="sxs-lookup"><span data-stu-id="19363-162">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="19363-163">**Gelişmiş Bul** sayfasında, **Ara** açılan listesinde **Finance and Operations Sanal Veri Kaynağı Yapılandırmaları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="19363-163">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="19363-164">**Sonuçlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="19363-164">Select **Results**.</span></span>

7. <span data-ttu-id="19363-165">**Microsoft HR Veri Kaynağı** kaydını seçin.</span><span class="sxs-lookup"><span data-stu-id="19363-165">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="19363-166">Veri kaynağı yapılandırması için gerekli bilgileri girin.</span><span class="sxs-lookup"><span data-stu-id="19363-166">Enter the required information for the data source configuration.</span></span>

   - <span data-ttu-id="19363-167">**Hedef URL**: Human Resources ad alanınızın URL'si.</span><span class="sxs-lookup"><span data-stu-id="19363-167">**Target URL**: The URL of your Human Resources namespace.</span></span>
   - <span data-ttu-id="19363-168">**Kiracı Kimliği**: Azure Active Directory (Azure AD) kiracı kimliği.</span><span class="sxs-lookup"><span data-stu-id="19363-168">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>
   - <span data-ttu-id="19363-169">**AAD Uygulama Kodu**: Microsoft Azure portalında kayıtlı olan uygulama için oluşturulan uygulama (istemci) kimliği.</span><span class="sxs-lookup"><span data-stu-id="19363-169">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="19363-170">Bu bilgiyi daha önce [Uygulamayı Microsoft Azure'da kaydetme](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure) bölümünde almıştınız.</span><span class="sxs-lookup"><span data-stu-id="19363-170">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>
   - <span data-ttu-id="19363-171">**AAD Uygulama Gizli Anahtarı**: Microsoft Azure portalında kayıtlı olan uygulama için oluşturulan istemci gizli anahtarı.</span><span class="sxs-lookup"><span data-stu-id="19363-171">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="19363-172">Bu bilgiyi daha önce [Uygulamayı Microsoft Azure'da kaydetme](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure) bölümünde almıştınız.</span><span class="sxs-lookup"><span data-stu-id="19363-172">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

9. <span data-ttu-id="19363-173">**Kaydet ve Kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="19363-173">Select **Save & Close**.</span></span>

   ![Microsoft HR Veri Kaynağı](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="19363-175">Human Resources uygulamasında uygulama izinlerini verme</span><span class="sxs-lookup"><span data-stu-id="19363-175">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="19363-176">Human Resources'ta iki Azure AD uygulaması için izin verin:</span><span class="sxs-lookup"><span data-stu-id="19363-176">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="19363-177">Microsoft Azure portalında kiracınız için oluşturulan uygulama</span><span class="sxs-lookup"><span data-stu-id="19363-177">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="19363-178">Power Apps ortamında yüklü olan Dynamics 365 HR Sanal Varlık uygulaması</span><span class="sxs-lookup"><span data-stu-id="19363-178">The Dynamics 365 HR Virtual Entity app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="19363-179">Human Resources'ta **Azure Active Directory uygulamaları** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="19363-179">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="19363-180">Yeni uygulama kaydı oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="19363-180">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="19363-181">**İstemci kodu** alanına, Microsoft Azure portalına kaydettiğiniz uygulama istemci kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="19363-181">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="19363-182">**Ad** alanına, Microsoft Azure portalına kaydettiğiniz uygulama adını girin.</span><span class="sxs-lookup"><span data-stu-id="19363-182">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="19363-183">**Kullanıcı kimliği** alanında, Human Resources ve Power Apps ortamında yönetici izinlerine sahip olan kullanıcının kullanıcı kimliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="19363-183">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="19363-184">İkinci uygulama kaydını oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="19363-184">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="19363-185">**İstemci Kimliği**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="19363-185">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="19363-186">**Ad**: Dynamics 365 HR Sanal Varlığı</span><span class="sxs-lookup"><span data-stu-id="19363-186">**Name**: Dynamics 365 HR Virtual Entity</span></span>
    - <span data-ttu-id="19363-187">**Kullanıcı kimliği** alanında, Human Resources ve Power Apps ortamında yönetici izinlerine sahip olan kullanıcının kullanıcı kimliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="19363-187">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-entities"></a><span data-ttu-id="19363-188">Sanal varlıklar oluşturma</span><span class="sxs-lookup"><span data-stu-id="19363-188">Generate virtual entities</span></span>

<span data-ttu-id="19363-189">Kurulum tamamlandığında, Common Data Service örneğiniz içinde oluşturmak ve etkinleştirmek istediğiniz sanal varlıkları seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="19363-189">When setup completes, you can select the virtual entities you want to generate and enable in your Common Data Service instance.</span></span>

1. <span data-ttu-id="19363-190">[Power Platform Yönetim Merkezi](https://admin.powerplatform.microsoft.com)'ni açın.</span><span class="sxs-lookup"><span data-stu-id="19363-190">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="19363-191">**Ortamlar** listesinde, Human Resources kurulumunuzla ilişkilendirilen Power Apps ortamını seçin.</span><span class="sxs-lookup"><span data-stu-id="19363-191">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="19363-192">Sayfanın **Ayrıntılar** bölümünde **Ortam URL**'sini seçin.</span><span class="sxs-lookup"><span data-stu-id="19363-192">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="19363-193">**Çözüm Durumu Merkezi**'nde, uygulama sayfasının sağ üst kısmında **Gelişmiş Bul** simgesini seçin.</span><span class="sxs-lookup"><span data-stu-id="19363-193">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the page.</span></span>

5. <span data-ttu-id="19363-194">**Gelişmiş Bul** sayfasında, **Ara** açılan listesinde **Kullanılabilir HR Varlıkları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="19363-194">On the **Advanced Find** page, in the **Look for** dropdown list, select **Available HR Entities**.</span></span>

6. <span data-ttu-id="19363-195">Etkinleştirmek istediğiniz varlığı veya varlıkları bulmak için filtre seçeneklerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="19363-195">Use the filter options to find the entity or entities you want to enable.</span></span>

7. <span data-ttu-id="19363-196">Listeden bir varlık seçin.</span><span class="sxs-lookup"><span data-stu-id="19363-196">Select an entity from the list.</span></span>

8. <span data-ttu-id="19363-197">Varlık sayfasında, **Oluşturuldu** özelliğini varlık için **Evet** olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="19363-197">On the entity page, change the **Has Been Generated** property to **Yes** for the entity.</span></span>

9. <span data-ttu-id="19363-198">Varlık sayfasını kaydedin ve kapatın.</span><span class="sxs-lookup"><span data-stu-id="19363-198">Save and close the entity page.</span></span>

> [!NOTE]
> <span data-ttu-id="19363-199">**Birden Çok Kaydı Değiştir** sayfasını kullanarak, birden çok sanal varlık oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="19363-199">You can generate multiple virtual entities at once by using the **Change Multiple Records** page.</span></span> <span data-ttu-id="19363-200">Sayfada birden fazla kayıt seçin ve şeritte **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="19363-200">Select multiple records on the page, and select **Edit** on the ribbon.</span></span> <span data-ttu-id="19363-201">Daha sonra tüm kayıtlar için **Oluşturuldu** özelliğini değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="19363-201">You can then change the **Has Been Generated** property for all selected records.</span></span>

![Kullanılabilir HR Varlıkları](./media/hr-admin-integration-virtual-entities-available.jpg)

> [!NOTE]
> <span data-ttu-id="19363-203">Gelecekteki sürümlerde sanal varlıklar oluşturma sürecini kolaylaştırmak için, işlem Human Resources'taki bir sayfada gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="19363-203">To streamline the process of generating virtual entities in future releases, the process will occur in a page in Human Resources.</span></span>

## <a name="see-also"></a><span data-ttu-id="19363-204">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="19363-204">See also</span></span>

[<span data-ttu-id="19363-205">Common Data Service nedir?</span><span class="sxs-lookup"><span data-stu-id="19363-205">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="19363-206">Varlığa genel bakış</span><span class="sxs-lookup"><span data-stu-id="19363-206">Entity overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="19363-207">Varlık ilişkilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="19363-207">Entity relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="19363-208">Harici veri kaynağından veri içeren sanal varlıkları oluşturma ve düzenleme</span><span class="sxs-lookup"><span data-stu-id="19363-208">Create and edit virtual entities that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="19363-209">Power Apps portalları nedir?</span><span class="sxs-lookup"><span data-stu-id="19363-209">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="19363-210">Power Apps'ta uygulamalar oluşturmaya genel bakış</span><span class="sxs-lookup"><span data-stu-id="19363-210">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
