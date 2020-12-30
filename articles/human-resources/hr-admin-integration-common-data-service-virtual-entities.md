---
title: Common Data Service sanal varlıklarını yapılandırma
description: Bu konu, Dynamics 365 Human Resources için sanal varlıkların nasıl yapılandırılacağını göstermektedir. Mecvut sanal varlıkları oluşturun ve güncelleştirin ve oluşturulan ve kullanılabilir varlıkları inceleyin.
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
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
ms.openlocfilehash: 2b590faeab600d04c9d5303693ec1e9ac682250d
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645613"
---
# <a name="configure-common-data-service-virtual-entities"></a><span data-ttu-id="4cf1d-104">Common Data Service sanal varlıklarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="4cf1d-104">Configure Common Data Service virtual entities</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="4cf1d-105">Dynamics 365 Human Resources Common Data Service'taki sanal bir veri kaynağıdır.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-105">Dynamics 365 Human Resources is a virtual data source in Common Data Service.</span></span> <span data-ttu-id="4cf1d-106">Common Data Service ve Microsoft Power Platform'dan tam oluşturma, okuma, güncelleştirme ve silme (CRUD) işlemleri sağlar.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-106">It provides full create, read, update, and delete (CRUD) operations from Common Data Service and Microsoft Power Platform.</span></span> <span data-ttu-id="4cf1d-107">Sanal varlıkların verileri Common Data Service'de depolanmaz , ancak uygulama veritabanında depolanır.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-107">The data for virtual entities isn't stored in Common Data Service, but in the application database.</span></span> 

<span data-ttu-id="4cf1d-108">Human Resources varlıklarındaki CRUD işlemlerini Common Data Service'den etkinleştirmek için, varlıkları Common Data Service'de sanal varlıklar olarak kullanılabilir yapmalısınız.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-108">To enable CRUD operations on Human Resources entities from Common Data Service, you must make the entities available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="4cf1d-109">Bu, Common Data Service ve Microsoft Power Platform'dan Human Resources'daki veriler üzerinde CRUD işlemleri gerçekleştirmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-109">This lets you perform CRUD operations from Common Data Service and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="4cf1d-110">Operasyonlar, varlıklara veri yazarken veri bütünlüğünü sağlamak için Human Resources'ın tam iş mantığı doğrulamalarını da destekler.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

## <a name="available-virtual-entities-for-human-resources"></a><span data-ttu-id="4cf1d-111">Human Resources için kullanılabilir sanal varlıklar</span><span class="sxs-lookup"><span data-stu-id="4cf1d-111">Available virtual entities for Human Resources</span></span>

<span data-ttu-id="4cf1d-112">Human Resources'taki tüm Açık Veri Protokolü (OData) varlıkları Common Data Service'de sanal varlıklar olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-112">All Open Data Protocol (OData) entities in Human Resources are available as virtual entities in Common Data Service.</span></span> <span data-ttu-id="4cf1d-113">Bunlar Power Platform uygulamasında da kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-113">They're also available in Power Platform.</span></span> <span data-ttu-id="4cf1d-114">Artık verileri Common Data Service'a kopyalamadan veya eşitlemeden doğrudan Human Resources'dan tam CRUD özelliği ile verileri kullanarak uygulamalar ve deneyimler oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-114">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Common Data Service.</span></span> <span data-ttu-id="4cf1d-115">Human Resources'taki iş süreçleri için işbirliği senaryolarını etkinleştiren, harici tabanlı web siteleri oluşturmak için Power Apps portallarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-115">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="4cf1d-116">Ortamda etkinleştirilmiş sanal varlıkların listesini görüntüleyebilir ve [Power Apps](https://make.powerapps.com) içindeki varlıklarla **Dynamics 365 HR Sanal Varlıklar** çözümünde çalışmaya başlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-116">You can view the list of virtual entities enabled in the environment, and begin working with the entities in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Entities** solution.</span></span>

![Power Apps'taki Dynamics 365 HR Sanal Varlıkları](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a><span data-ttu-id="4cf1d-118">Sanal varlıklar ve doğal varlıklar</span><span class="sxs-lookup"><span data-stu-id="4cf1d-118">Virtual entities versus natural entities</span></span>

<span data-ttu-id="4cf1d-119">Human Resources için sanal varlıklar, Common Data Service'taki Human Resources için oluşturulan doğal varlıklarla aynı değildir.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-119">Virtual entities for Human Resources aren't the same as the natural Common Data Service entities created for Human Resources.</span></span> <span data-ttu-id="4cf1d-120">Human Resources için doğal varlıklar ayrı olarak oluşturulur ve Common Data Service'deki HCM Ortak çözümünde tutulur.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-120">The natural entities for Human Resources are generated separately and maintained in the HCM Common solution in Common Data Service.</span></span> <span data-ttu-id="4cf1d-121">Doğal varlıklarla, veriler Common Data Service'ta depolanır ve Human Resources uygulama veritabanıyla eşitleme gerektirir.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-121">With natural entities, the data is stored in Common Data Service and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="4cf1d-122">Human Resources için Common Data Service doğal varlıkların listesi için bkz. [Common Data Service varlıkları](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span><span class="sxs-lookup"><span data-stu-id="4cf1d-122">For a list of the natural Common Data Service entities for Human Resources, see [Common Data Service entities](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).</span></span>

## <a name="setup"></a><span data-ttu-id="4cf1d-123">Ayar</span><span class="sxs-lookup"><span data-stu-id="4cf1d-123">Setup</span></span>

<span data-ttu-id="4cf1d-124">Ortamınızdaki sanal varlıkları etkinleştirmek için bu kurulum adımlarını izleyin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-124">Follow these setup steps to enable virtual entities in your environment.</span></span>

### <a name="enable-virtual-entities-in-human-resources"></a><span data-ttu-id="4cf1d-125">Human Resources'ta sanal varlıkları etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="4cf1d-125">Enable virtual entities in Human Resources</span></span>

<span data-ttu-id="4cf1d-126">Önce, **özellik yönetimi** çalışma alanında sanal varlıkları etkinleştirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-126">First, you must enable virtual entities in the **Feature management** workspace.</span></span>

1. <span data-ttu-id="4cf1d-127">İnsan Kaynakları, **sistem yönetimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-127">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="4cf1d-128">**Özellik yönetimi** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-128">Select the **Feature management** tile.</span></span>

3. <span data-ttu-id="4cf1d-129">**HR/CD 'de sanal varlık desteğini** seçin ve **Etkinleştir** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-129">Select **Virtual Entity support in HR/CDS**, and then select **Enable**.</span></span>

<span data-ttu-id="4cf1d-130">Özellikleri devre dışı bırakma ve etkinleştirmeyle ilgili daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="4cf1d-130">For more information about enabling and disabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="4cf1d-131">Microsoft Azure'da uygulamayı kaydetme</span><span class="sxs-lookup"><span data-stu-id="4cf1d-131">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="4cf1d-132">Human Resource örneğinizi Azure portalında kaydetmeniz gerekir; böylece Microsoft kimlik platformu uygulama ve kullanıcılar için kimlik doğrulama ve yetkilendirme hizmetleri sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-132">You must register your Human Resources instance in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="4cf1d-133">Azure'da uygulama kaydetme hakkında daha fazla bilgi için bkz. [Hızlı başlangıç: Microsoft kimlik platform ile uygulama kaydetme](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="4cf1d-133">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="4cf1d-134">[Microsoft Azure portalını](https://portal.azure.com) açın.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-134">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="4cf1d-135">Azure hizmetleri listesinde **Uygulama kayıtları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-135">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="4cf1d-136">**Yeni kayıt** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-136">Select **New registration**.</span></span>

4. <span data-ttu-id="4cf1d-137">**Ad** alanına uygulama için açıklayıcı bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-137">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="4cf1d-138">Örneğin, **Dynamics 365 Human Resources Sanal Varlıkları**.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-138">For example, **Dynamics 365 Human Resources Virtual Entities**.</span></span>

5. <span data-ttu-id="4cf1d-139">**Yeniden yönlendirme URI'si** alanında Human Resources kurulumunuzun ad alanı URL'sini girin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-139">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="4cf1d-140">**Kayıt**'ı seç.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-140">Select **Register**.</span></span>

7. <span data-ttu-id="4cf1d-141">Kayıt tamamlandığında, Azure portalı uygulama kaydı **Uygulama (istemci) kimliğini** de içeren **Genel bakış** bölmesini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-141">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="4cf1d-142">Şu anda **Uygulama (istemci) kimliğini** not edin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-142">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="4cf1d-143">[Sanal varlık veri kaynağını yapılandırırken](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source) bu bilgileri gireceksiniz.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-143">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

8. <span data-ttu-id="4cf1d-144">Sol gezinti bölmesinde, **Sertifikalar ve gizli anahtarlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-144">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="4cf1d-145">Sayfanın **İstemci gizli anahtarı** bölümünde **Yeni istemci gizli anahtarı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-145">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="4cf1d-146">Bir açıklama sağlayın, bir süre seçin ve **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-146">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="4cf1d-147">Gizli anahtar değerini kaydedin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-147">Record the secret's value.</span></span> <span data-ttu-id="4cf1d-148">[Sanal varlık veri kaynağını yapılandırırken](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source) bu bilgileri gireceksiniz.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-148">You'll enter this information when you [Configure the virtual entity data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="4cf1d-149">Bu aşamada, gizli anahtarın değerini not aldığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-149">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="4cf1d-150">Bu sayfadan ayrıldıktan sonra gizli anahtar hiçbir zaman görüntülenmez.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-150">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a><span data-ttu-id="4cf1d-151">Dynamics 365 HR Sanal Varlık uygulamasını yükleme</span><span class="sxs-lookup"><span data-stu-id="4cf1d-151">Install the Dynamics 365 HR Virtual Entity app</span></span>

<span data-ttu-id="4cf1d-152">Sanal varlık çözüm paketini Common Data Service'a dağıtmak için Dynamics 365 HR Sanal Varlık uygulamasını Power Apps ortamınıza yükleyin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-152">Install the Dynamics 365 HR Virtual Entity app in your Power Apps environment to deploy the virtual entity solution package to Common Data Service.</span></span>

1. <span data-ttu-id="4cf1d-153">[Power Platform Yönetim Merkezi](https://admin.powerplatform.microsoft.com)'ni açın.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-153">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="4cf1d-154">**Ortamlar** listesinde, Human Resources kurulumunuzla ilişkilendirilen Power Apps ortamını seçin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-154">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="4cf1d-155">Sayfanın **Kaynaklar** bölümünde **Dynamics 365 uygulamaları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-155">In the **Resources** section of the page, select **Dynamics 365 apps**.</span></span>

4. <span data-ttu-id="4cf1d-156">**Uygulamayı yükle** eylemini seçin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-156">Select the **Install app** action.</span></span>

5. <span data-ttu-id="4cf1d-157">**Dynamics 365 HR Sanal Varlık** öğesini ve **İleri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-157">Select **Dynamics 365 HR Virtual Entity**, and select **Next**.</span></span>

6. <span data-ttu-id="4cf1d-158">Hizmet koşullarını gözden geçirin ve kabul etmek için işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-158">Review and mark to agree to the terms of service.</span></span>

7. <span data-ttu-id="4cf1d-159">**Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-159">Select **Install**.</span></span>

<span data-ttu-id="4cf1d-160">Yükleme birkaç dakika sürer.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-160">The install takes a few minutes.</span></span> <span data-ttu-id="4cf1d-161">Bu işlem tamamlandığında sonraki adımlara devam edin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-161">When it completes, continue to the next steps.</span></span>

![Dynamics 365 HR Sanal Varlık uygulamasını Power Platform yönetim merkezinden yükleyin](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a><span data-ttu-id="4cf1d-163">Sanal varlık veri kaynağını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="4cf1d-163">Configure the virtual entity data source</span></span> 

<span data-ttu-id="4cf1d-164">Sonraki adım, sanal varlık veri kaynağını Power Apps ortamında yapılandırmaktır.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-164">The next step is to configure the virtual entity data source in the Power Apps environment.</span></span> 

1. <span data-ttu-id="4cf1d-165">[Power Platform Yönetim Merkezi](https://admin.powerplatform.microsoft.com)'ni açın.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-165">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="4cf1d-166">**Ortamlar** listesinde, Human Resources kurulumunuzla ilişkilendirilen Power Apps ortamını seçin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-166">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="4cf1d-167">Sayfanın **Ayrıntılar** bölümünde **Ortam URL**'sini seçin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-167">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="4cf1d-168">**Çözüm Durumu Merkezi**'nde, uygulama sayfasının sağ üst kısmında **Gelişmiş Bul** simgesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-168">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="4cf1d-169">**Gelişmiş Bul** sayfasında, **Ara** açılan listesinde **Finance and Operations Sanal Veri Kaynağı Yapılandırmaları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-169">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

6. <span data-ttu-id="4cf1d-170">**Sonuçlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-170">Select **Results**.</span></span>

7. <span data-ttu-id="4cf1d-171">**Microsoft HR Veri Kaynağı** kaydını seçin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-171">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="4cf1d-172">Veri kaynağı yapılandırması için gerekli bilgileri girin:</span><span class="sxs-lookup"><span data-stu-id="4cf1d-172">Enter the required information for the data source configuration:</span></span>

   - <span data-ttu-id="4cf1d-173">**Hedef URL**: Human Resources ad alanınızın URL'si.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-173">**Target URL**: The URL of your Human Resources namespace.</span></span> <span data-ttu-id="4cf1d-174">Hedef URL 'nin biçimi:</span><span class="sxs-lookup"><span data-stu-id="4cf1d-174">The format of the target URL is:</span></span>
     
     <span data-ttu-id="4cf1d-175">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span><span class="sxs-lookup"><span data-stu-id="4cf1d-175">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span></span>

     <span data-ttu-id="4cf1d-176">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="4cf1d-176">For example:</span></span>
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     ><span data-ttu-id="4cf1d-177">Hata almamak için URL'nin sonuna "**/**" karakteri eklediğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-177">Be sure to include the "**/**" character at the end of the URL to avoid receiving an error.</span></span>

   - <span data-ttu-id="4cf1d-178">**Kiracı Kimliği**: Azure Active Directory (Azure AD) kiracı kimliği.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-178">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>

   - <span data-ttu-id="4cf1d-179">**AAD Uygulama Kodu**: Microsoft Azure portalında kayıtlı olan uygulama için oluşturulan uygulama (istemci) kimliği.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-179">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="4cf1d-180">Bu bilgiyi daha önce [Uygulamayı Microsoft Azure'da kaydetme](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure) bölümünde almıştınız.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-180">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   - <span data-ttu-id="4cf1d-181">**AAD Uygulama Gizli Anahtarı**: Microsoft Azure portalında kayıtlı olan uygulama için oluşturulan istemci gizli anahtarı.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-181">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="4cf1d-182">Bu bilgiyi daha önce [Uygulamayı Microsoft Azure'da kaydetme](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure) bölümünde almıştınız.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-182">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   ![Microsoft HR Veri Kaynağı](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. <span data-ttu-id="4cf1d-184">**Kaydet ve Kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-184">Select **Save & Close**.</span></span>

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="4cf1d-185">Human Resources uygulamasında uygulama izinlerini verme</span><span class="sxs-lookup"><span data-stu-id="4cf1d-185">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="4cf1d-186">Human Resources'ta iki Azure AD uygulaması için izin verin:</span><span class="sxs-lookup"><span data-stu-id="4cf1d-186">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="4cf1d-187">Microsoft Azure portalında kiracınız için oluşturulan uygulama</span><span class="sxs-lookup"><span data-stu-id="4cf1d-187">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="4cf1d-188">Power Apps ortamında yüklü olan Dynamics 365 HR Sanal Varlık uygulaması</span><span class="sxs-lookup"><span data-stu-id="4cf1d-188">The Dynamics 365 HR Virtual Entity app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="4cf1d-189">Human Resources'ta **Azure Active Directory uygulamaları** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-189">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="4cf1d-190">Yeni uygulama kaydı oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-190">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="4cf1d-191">**İstemci kodu** alanına, Microsoft Azure portalına kaydettiğiniz uygulama istemci kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-191">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="4cf1d-192">**Ad** alanına, Microsoft Azure portalına kaydettiğiniz uygulama adını girin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-192">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="4cf1d-193">**Kullanıcı kimliği** alanında, Human Resources ve Power Apps ortamında yönetici izinlerine sahip olan kullanıcının kullanıcı kimliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-193">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="4cf1d-194">İkinci uygulama kaydını oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-194">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="4cf1d-195">**İstemci Kimliği**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="4cf1d-195">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="4cf1d-196">**Ad**: Dynamics 365 HR Sanal Varlığı</span><span class="sxs-lookup"><span data-stu-id="4cf1d-196">**Name**: Dynamics 365 HR Virtual Entity</span></span>
    - <span data-ttu-id="4cf1d-197">**Kullanıcı kimliği** alanında, Human Resources ve Power Apps ortamında yönetici izinlerine sahip olan kullanıcının kullanıcı kimliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-197">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-entities"></a><span data-ttu-id="4cf1d-198">Sanal varlıklar oluşturma</span><span class="sxs-lookup"><span data-stu-id="4cf1d-198">Generate virtual entities</span></span>

<span data-ttu-id="4cf1d-199">Kurulum tamamlandığında, Common Data Service örneğiniz içinde oluşturmak ve etkinleştirmek istediğiniz sanal varlıkları seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-199">When setup completes, you can select the virtual entities you want to generate and enable in your Common Data Service instance.</span></span>

1. <span data-ttu-id="4cf1d-200">Human Resources'ta **Common Data Service (CDS) tümleştirmesi** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-200">In Human Resources, open the **Common Data Service (CDS) integration** page.</span></span>

2. <span data-ttu-id="4cf1d-201">**Sanal varlıklar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-201">Select the **Virtual entities** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="4cf1d-202">**Sanal varlığı etkinleştir** geçiş düğmesi, gerekli tüm kurulum tamamlandığında otomatik olarak **Evet** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-202">The **Enable the virtual entity** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="4cf1d-203">Geçiş düğmesi **Hayır** olarak ayarlanmışsa, tüm önkoşul kurulumun tamamlandığından emin olmak için bu belgenin önceki bölümlerindeki adımları gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-203">If the toggle is set to **No**, review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="4cf1d-204">Common Data Service'te oluşturmak istediğiniz varlığı veya varlıkları seçin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-204">Select the entity or entities you want to generate in Common Data Service.</span></span>

4. <span data-ttu-id="4cf1d-205">**Oluştur/Yenile**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-205">Select **Generate/refresh**.</span></span>

![Common Data Service Tümleştirmesi](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-entity-generation-status"></a><span data-ttu-id="4cf1d-207">Varlık oluşturma durumunu denetle</span><span class="sxs-lookup"><span data-stu-id="4cf1d-207">Check entity generation status</span></span>

<span data-ttu-id="4cf1d-208">Sanal varlıklar Common Data Service içinde zaman uyumsuz bir arka plan işleminde oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-208">Virtual entities are generated in Common Data Service through an asynchronous background process.</span></span> <span data-ttu-id="4cf1d-209">İşlemin üzerindeki güncelleştirmeler işlem merkezinde görüntülenebilir.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-209">Updates on the process display in the action center.</span></span> <span data-ttu-id="4cf1d-210">Hata günlükleri de dahil olmak üzere işlemle ilgili ayrıntılar, **işlem otomasyonları** sayfasında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-210">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="4cf1d-211">Human Resources'da, **İşlem otomasyonları** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-211">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="4cf1d-212">**Arka plan işlemleri** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-212">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="4cf1d-213">**Sanal varlık yoklama asenkron operasyonu arka plan işlemi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-213">Select **Virtual entity poll async operation background process**.</span></span>

4. <span data-ttu-id="4cf1d-214">**En son sonuçları görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-214">Select **View most recent results**.</span></span>

<span data-ttu-id="4cf1d-215">Yan taraftaki bölme işlemle ilgili en son yürütme sonuçlarını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-215">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="4cf1d-216">Common Data Service'ten gelen tüm hatalar da dahil olmak üzere, işlem günlüğünü görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-216">You can view the log for the process, including any errors returned from Common Data Service.</span></span>

## <a name="see-also"></a><span data-ttu-id="4cf1d-217">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="4cf1d-217">See also</span></span>

[<span data-ttu-id="4cf1d-218">Common Data Service nedir?</span><span class="sxs-lookup"><span data-stu-id="4cf1d-218">What is Common Data Service?</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="4cf1d-219">Varlığa genel bakış</span><span class="sxs-lookup"><span data-stu-id="4cf1d-219">Entity overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="4cf1d-220">Varlık ilişkilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="4cf1d-220">Entity relationships overview</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="4cf1d-221">Harici veri kaynağından veri içeren sanal varlıkları oluşturma ve düzenleme</span><span class="sxs-lookup"><span data-stu-id="4cf1d-221">Create and edit virtual entities that contain data from an external data source</span></span>](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="4cf1d-222">Power Apps portalları nedir?</span><span class="sxs-lookup"><span data-stu-id="4cf1d-222">What is Power Apps portals?</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="4cf1d-223">Power Apps'ta uygulamalar oluşturmaya genel bakış</span><span class="sxs-lookup"><span data-stu-id="4cf1d-223">Overview of creating apps in Power Apps</span></span>](https://docs.microsoft.com/powerapps/maker/)
