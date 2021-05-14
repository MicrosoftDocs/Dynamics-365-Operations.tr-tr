---
title: Dataverse sanal tablolarını yapılandırma
description: Bu konu, Dynamics 365 Human Resources için sanal tabloların nasıl yapılandırılacağını göstermektedir. Mecvut sanal tabloları oluşturun ve güncelleştirin ve oluşturulan ve kullanılabilir tabloları inceleyin.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 04997aba427ae6013c8154593b09ae1a45a580c3
ms.sourcegitcommit: 9283caad2d0636f98579c995784abec19fda2e3f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935765"
---
# <a name="configure-dataverse-virtual-tables"></a><span data-ttu-id="547d3-104">Dataverse sanal tablolarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="547d3-104">Configure Dataverse virtual tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="547d3-105">Dynamics 365 Human Resources Microsoft Dataverse'taki sanal bir veri kaynağıdır.</span><span class="sxs-lookup"><span data-stu-id="547d3-105">Dynamics 365 Human Resources is a virtual data source in Microsoft Dataverse.</span></span> <span data-ttu-id="547d3-106">Dataverse ve Microsoft Power Platform'dan tam oluşturma, okuma, güncelleştirme ve silme (CRUD) işlemleri sağlar.</span><span class="sxs-lookup"><span data-stu-id="547d3-106">It provides full create, read, update, and delete (CRUD) operations from Dataverse and Microsoft Power Platform.</span></span> <span data-ttu-id="547d3-107">Sanal tabloların verileri Dataverse'de depolanmaz ancak uygulama veritabanında depolanır.</span><span class="sxs-lookup"><span data-stu-id="547d3-107">The data for virtual tables isn't stored in Dataverse, but in the application database.</span></span>

<span data-ttu-id="547d3-108">Human Resources varlıklarındaki CRUD işlemlerini Dataverse'den etkinleştirmek için varlıkları Dataverse'de sanal tablolar olarak kullanılabilir yapmalısınız.</span><span class="sxs-lookup"><span data-stu-id="547d3-108">To enable CRUD operations on Human Resources entities from Dataverse, you must make the entities available as virtual tables in Dataverse.</span></span> <span data-ttu-id="547d3-109">Bu, Dataverse ve Microsoft Power Platform'dan Human Resources'daki veriler üzerinde CRUD işlemleri gerçekleştirmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="547d3-109">This lets you perform CRUD operations from Dataverse and Microsoft Power Platform on data that's in Human Resources.</span></span> <span data-ttu-id="547d3-110">Operasyonlar, varlıklara veri yazarken veri bütünlüğünü sağlamak için Human Resources'ın tam iş mantığı doğrulamalarını da destekler.</span><span class="sxs-lookup"><span data-stu-id="547d3-110">The operations also support the full business logic validations of Human Resources to ensure data integrity when writing data to the entities.</span></span>

> [!NOTE]
> <span data-ttu-id="547d3-111">Human Resources varlıkları Dataverse tablolarına karşılık gelir.</span><span class="sxs-lookup"><span data-stu-id="547d3-111">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="547d3-112">Dataverse (önceden Common Data Service) ve terminoloji güncelleştirmeleri hakkında daha fazla bilgi için bkz. [Microsoft Dataverse nedir?](/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="547d3-112">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span></span>

## <a name="available-virtual-tables-for-human-resources"></a><span data-ttu-id="547d3-113">Human Resources için kullanılabilir sanal tablolar</span><span class="sxs-lookup"><span data-stu-id="547d3-113">Available virtual tables for Human Resources</span></span>

<span data-ttu-id="547d3-114">Human Resources'taki tüm Açık Veri Protokolü (OData) varlıkları Dataverse'de sanal tablolar olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="547d3-114">All Open Data Protocol (OData) entities in Human Resources are available as virtual tables in Dataverse.</span></span> <span data-ttu-id="547d3-115">Bunlar Power Platform uygulamasında da kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="547d3-115">They're also available in Power Platform.</span></span> <span data-ttu-id="547d3-116">Artık verileri Dataverse'a kopyalamadan veya eşitlemeden doğrudan Human Resources'dan tam CRUD özelliği ile verileri kullanarak uygulamalar ve deneyimler oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="547d3-116">You can now build apps and experiences with data directly from Human Resources with full CRUD capability, without copying or synchronizing data to Dataverse.</span></span> <span data-ttu-id="547d3-117">Human Resources'taki iş süreçleri için işbirliği senaryolarını etkinleştiren, harici tabanlı web siteleri oluşturmak için Power Apps portallarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="547d3-117">You can use Power Apps portals to build external-facing websites that enable collaboration scenarios for business processes in Human Resources.</span></span>

<span data-ttu-id="547d3-118">Ortamda etkinleştirilmiş sanal tabloların listesini görüntüleyebilir ve [Power Apps](https://make.powerapps.com) içindeki tablolarla **Dynamics 365 HR Sanal Tablolar** çözümünde çalışmaya başlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="547d3-118">You can view the list of virtual tables enabled in the environment, and begin working with the tables in [Power Apps](https://make.powerapps.com), in the **Dynamics 365 HR Virtual Tables** solution.</span></span>

![Power Apps'teki Dynamics 365 HR Sanal Tabloları](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-tables-versus-native-tables"></a><span data-ttu-id="547d3-120">Sanal tablolar ve yerel tablolar karşılaştırması</span><span class="sxs-lookup"><span data-stu-id="547d3-120">Virtual tables versus native tables</span></span>

<span data-ttu-id="547d3-121">Human Resources için sanal tablolar, Dataverse'teki Human Resources için oluşturulan yerel tablolarla aynı değildir.</span><span class="sxs-lookup"><span data-stu-id="547d3-121">Virtual tables for Human Resources aren't the same as the native Dataverse tables created for Human Resources.</span></span> 

<span data-ttu-id="547d3-122">Human Resources için yerel tablolar ayrı olarak oluşturulur ve Dataverse'deki HCM Ortak çözümünde tutulur.</span><span class="sxs-lookup"><span data-stu-id="547d3-122">The native tables for Human Resources are generated separately and maintained in the HCM Common solution in Dataverse.</span></span> <span data-ttu-id="547d3-123">Yerel tablolarla, veriler Dataverse'ta depolanır ve Human Resources uygulama veritabanıyla eşitleme gerektirir.</span><span class="sxs-lookup"><span data-stu-id="547d3-123">With native tables, the data is stored in Dataverse and requires synchronization with the Human Resources application database.</span></span>

> [!NOTE]
> <span data-ttu-id="547d3-124">Human Resources için Dataverse yerel tablolarının listesi için bkz. [Dataverse tabloları](./hr-developer-entities.md).</span><span class="sxs-lookup"><span data-stu-id="547d3-124">For a list of the native Dataverse tables for Human Resources, see [Dataverse tables](./hr-developer-entities.md).</span></span>

## <a name="setup"></a><span data-ttu-id="547d3-125">Ayar</span><span class="sxs-lookup"><span data-stu-id="547d3-125">Setup</span></span>

<span data-ttu-id="547d3-126">Ortamınızdaki sanal tabloları etkinleştirmek için bu kurulum adımlarını izleyin.</span><span class="sxs-lookup"><span data-stu-id="547d3-126">Follow these setup steps to enable virtual tables in your environment.</span></span>

### <a name="enable-virtual-tables-in-human-resources"></a><span data-ttu-id="547d3-127">Human Resources'ta sanal tabloları etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="547d3-127">Enable virtual tables in Human Resources</span></span>

<span data-ttu-id="547d3-128">Önce, **özellik yönetimi** çalışma alanında sanal tabloları etkinleştirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="547d3-128">First, you must enable virtual tables in the **Feature management** workspace.</span></span>

1. <span data-ttu-id="547d3-129">İnsan Kaynakları, **sistem yönetimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="547d3-129">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="547d3-130">**Özellik yönetimi** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="547d3-130">Select the **Feature management** tile.</span></span>

3. <span data-ttu-id="547d3-131">**Dataverse'te HR için sanal tablo desteği**'ni seçin ve **Etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="547d3-131">Select **Virtual table support for HR in Dataverse**, and then select **Enable**.</span></span>

<span data-ttu-id="547d3-132">Özellikleri devre dışı bırakma ve etkinleştirmeyle ilgili daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="547d3-132">For more information about enabling and disabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

### <a name="register-the-app-in-microsoft-azure"></a><span data-ttu-id="547d3-133">Microsoft Azure'da uygulamayı kaydetme</span><span class="sxs-lookup"><span data-stu-id="547d3-133">Register the app in Microsoft Azure</span></span>

<span data-ttu-id="547d3-134">Human Resource örneğinizi Azure portalında kaydetmeniz gerekir; böylece Microsoft kimlik platformu uygulama ve kullanıcılar için kimlik doğrulama ve yetkilendirme hizmetleri sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="547d3-134">You must register your Human Resources instance in the Azure portal so the Microsoft identity platform can provide authentication and authorization services for the app and users.</span></span> <span data-ttu-id="547d3-135">Azure'da uygulama kaydetme hakkında daha fazla bilgi için bkz. [Hızlı başlangıç: Microsoft kimlik platform ile uygulama kaydetme](/azure/active-directory/develop/quickstart-register-app).</span><span class="sxs-lookup"><span data-stu-id="547d3-135">For more information about registering apps in Azure, see [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app).</span></span>

1. <span data-ttu-id="547d3-136">[Microsoft Azure portalını](https://portal.azure.com) açın.</span><span class="sxs-lookup"><span data-stu-id="547d3-136">Open the [Microsoft Azure portal](https://portal.azure.com).</span></span>

2. <span data-ttu-id="547d3-137">Azure hizmetleri listesinde **Uygulama kayıtları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="547d3-137">In the Azure services list, select **App registrations**.</span></span>

3. <span data-ttu-id="547d3-138">**Yeni kayıt** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="547d3-138">Select **New registration**.</span></span>

4. <span data-ttu-id="547d3-139">**Ad** alanına uygulama için açıklayıcı bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="547d3-139">In the **Name** field, enter a descriptive name for the app.</span></span> <span data-ttu-id="547d3-140">Örneğin, **Dynamics 365 Human Resources Sanal Tabloları**.</span><span class="sxs-lookup"><span data-stu-id="547d3-140">For example, **Dynamics 365 Human Resources Virtual Tables**.</span></span>

5. <span data-ttu-id="547d3-141">**Yeniden yönlendirme URI'si** alanında Human Resources kurulumunuzun ad alanı URL'sini girin.</span><span class="sxs-lookup"><span data-stu-id="547d3-141">In the **Redirect URI** field, enter the namespace URL of your instance of Human Resources.</span></span>

6. <span data-ttu-id="547d3-142">**Kayıt**'ı seç.</span><span class="sxs-lookup"><span data-stu-id="547d3-142">Select **Register**.</span></span>

7. <span data-ttu-id="547d3-143">Kayıt tamamlandığında, Azure portalı uygulama kaydı **Uygulama (istemci) kimliğini** de içeren **Genel bakış** bölmesini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="547d3-143">When registration completes, the Azure portal displays the app registration's **Overview** pane, which includes its **Application (client) ID**.</span></span> <span data-ttu-id="547d3-144">Şu anda **Uygulama (istemci) kimliğini** not edin.</span><span class="sxs-lookup"><span data-stu-id="547d3-144">Take note of the **Application (client) ID** at this time.</span></span> <span data-ttu-id="547d3-145">[Sanal tablo veri kaynağını yapılandırırken](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source) bu bilgileri gireceksiniz.</span><span class="sxs-lookup"><span data-stu-id="547d3-145">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

8. <span data-ttu-id="547d3-146">Sol gezinti bölmesinde, **Sertifikalar ve gizli anahtarlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="547d3-146">In the left navigation pane, select **Certificates and secrets**.</span></span>

9. <span data-ttu-id="547d3-147">Sayfanın **İstemci gizli anahtarı** bölümünde **Yeni istemci gizli anahtarı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="547d3-147">In the **Client secrets** section of the page, select **New client secret**.</span></span>

10. <span data-ttu-id="547d3-148">Bir açıklama sağlayın, bir süre seçin ve **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="547d3-148">Provide a description, select a duration, and select **Add**.</span></span>

11. <span data-ttu-id="547d3-149">Gizli öğenin değerini tablonun **Değer** özelliği bölümünden kaydedin.</span><span class="sxs-lookup"><span data-stu-id="547d3-149">Record the secret's value from the **Value** property of the table.</span></span> <span data-ttu-id="547d3-150">[Sanal tablo veri kaynağını yapılandırırken](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source) bu bilgileri gireceksiniz.</span><span class="sxs-lookup"><span data-stu-id="547d3-150">You'll enter this information when you [Configure the virtual table data source](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="547d3-151">Bu aşamada, gizli anahtarın değerini not aldığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="547d3-151">Be sure to take note of the secret's value at this time.</span></span> <span data-ttu-id="547d3-152">Bu sayfadan ayrıldıktan sonra gizli anahtar hiçbir zaman görüntülenmez.</span><span class="sxs-lookup"><span data-stu-id="547d3-152">The secret is never displayed again after you leave this page.</span></span>

### <a name="install-the-dynamics-365-hr-virtual-table-app"></a><span data-ttu-id="547d3-153">Dynamics 365 HR Sanal Tablo uygulamasını yükleme</span><span class="sxs-lookup"><span data-stu-id="547d3-153">Install the Dynamics 365 HR Virtual Table app</span></span>

<span data-ttu-id="547d3-154">Sanal tablo çözüm paketini Dataverse'a dağıtmak için Dynamics 365 HR Sanal Tablo uygulamasını Power Apps ortamınıza yükleyin.</span><span class="sxs-lookup"><span data-stu-id="547d3-154">Install the Dynamics 365 HR Virtual Table app in your Power Apps environment to deploy the virtual table solution package to Dataverse.</span></span>

1. <span data-ttu-id="547d3-155">Human Resources'ta **Microsoft Dataverse tümleştirmesi** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="547d3-155">In Human Resources, open the **Microsoft Dataverse integration** page.</span></span>

2. <span data-ttu-id="547d3-156">**Sanal tablolar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="547d3-156">Select the **Virtual tables** tab.</span></span>

3. <span data-ttu-id="547d3-157">**Sanal tablo uygulamasını yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="547d3-157">Select **Install virtual table app**.</span></span>

### <a name="configure-the-virtual-table-data-source"></a><span data-ttu-id="547d3-158">Sanal tablo veri kaynağını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="547d3-158">Configure the virtual table data source</span></span>

<span data-ttu-id="547d3-159">Sonraki adım, sanal tablo veri kaynağını Power Apps ortamında yapılandırmaktır.</span><span class="sxs-lookup"><span data-stu-id="547d3-159">The next step is to configure the virtual table data source in the Power Apps environment.</span></span>

1. <span data-ttu-id="547d3-160">[Power Platform Yönetim Merkezi](https://admin.powerplatform.microsoft.com)'ni açın.</span><span class="sxs-lookup"><span data-stu-id="547d3-160">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="547d3-161">**Ortamlar** listesinde, Human Resources kurulumunuzla ilişkilendirilen Power Apps ortamını seçin.</span><span class="sxs-lookup"><span data-stu-id="547d3-161">In the **Environments** list, select the Power Apps environment associated with your Human Resources instance.</span></span>

3. <span data-ttu-id="547d3-162">Sayfanın **Ayrıntılar** bölümünde **Ortam URL**'sini seçin.</span><span class="sxs-lookup"><span data-stu-id="547d3-162">Select the **Environment URL** in the **Details** section of the page.</span></span>

4. <span data-ttu-id="547d3-163">**Çözüm Durumu Merkezi**'nde, uygulama sayfasının sağ üst kısmında **Gelişmiş Bul** simgesini seçin.</span><span class="sxs-lookup"><span data-stu-id="547d3-163">In the **Solution Health Hub**, select the **Advanced Find** icon in the top right of the application page.</span></span>

5. <span data-ttu-id="547d3-164">**Gelişmiş Bul** sayfasında, **Ara** açılan listesinde **Finance and Operations Sanal Veri Kaynağı Yapılandırmaları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="547d3-164">On the **Advanced Find** page, in the **Look for** dropdown list, select **Finance and Operations Virtual Data Source Configurations**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="547d3-165">Sanal tablo uygulamasının önceki kurulum adımından yüklenmesi birkaç dakika sürebilir.</span><span class="sxs-lookup"><span data-stu-id="547d3-165">The installation of the virtual table app from the previous setup step can take a few minutes.</span></span> <span data-ttu-id="547d3-166">**Finance and Operations Sanal Veri Kaynağı Yapılandırmaları** listede yoksa, bir dakika bekleyip listeyi yenileyin.</span><span class="sxs-lookup"><span data-stu-id="547d3-166">If **Finance and Operations Virtual Data Source Configurations** isn't available in the list, wait for a minute and refresh the list.</span></span>

6. <span data-ttu-id="547d3-167">**Sonuçlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="547d3-167">Select **Results**.</span></span>

7. <span data-ttu-id="547d3-168">**Microsoft HR Veri Kaynağı** kaydını seçin.</span><span class="sxs-lookup"><span data-stu-id="547d3-168">Select the **Microsoft HR Data Source** record.</span></span>

8. <span data-ttu-id="547d3-169">Veri kaynağı yapılandırması için gerekli bilgileri girin:</span><span class="sxs-lookup"><span data-stu-id="547d3-169">Enter the required information for the data source configuration:</span></span>

   - <span data-ttu-id="547d3-170">**Hedef URL**: Human Resources ad alanınızın URL'si.</span><span class="sxs-lookup"><span data-stu-id="547d3-170">**Target URL**: The URL of your Human Resources namespace.</span></span> <span data-ttu-id="547d3-171">Hedef URL 'nin biçimi:</span><span class="sxs-lookup"><span data-stu-id="547d3-171">The format of the target URL is:</span></span>
     
     <span data-ttu-id="547d3-172">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span><span class="sxs-lookup"><span data-stu-id="547d3-172">https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/</span></span>

     <span data-ttu-id="547d3-173">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="547d3-173">For example:</span></span>
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     ><span data-ttu-id="547d3-174">Hata almamak için URL'nin sonuna "**/**" karakteri eklediğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="547d3-174">Be sure to include the "**/**" character at the end of the URL to avoid receiving an error.</span></span>

   - <span data-ttu-id="547d3-175">**Kiracı Kimliği**: Azure Active Directory (Azure AD) kiracı kimliği.</span><span class="sxs-lookup"><span data-stu-id="547d3-175">**Tenant ID**: The Azure Active Directory (Azure AD) tenant ID.</span></span>

   - <span data-ttu-id="547d3-176">**AAD Uygulama Kodu**: Microsoft Azure portalında kayıtlı olan uygulama için oluşturulan uygulama (istemci) kimliği.</span><span class="sxs-lookup"><span data-stu-id="547d3-176">**AAD Application ID**: The application (client) ID created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="547d3-177">Bu bilgiyi daha önce [Uygulamayı Microsoft Azure'da kaydetme](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure) bölümünde almıştınız.</span><span class="sxs-lookup"><span data-stu-id="547d3-177">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   - <span data-ttu-id="547d3-178">**AAD Uygulama Gizli Anahtarı**: Microsoft Azure portalında kayıtlı olan uygulama için oluşturulan istemci gizli anahtarı.</span><span class="sxs-lookup"><span data-stu-id="547d3-178">**AAD Application Secret**: The client secret created for the application registered in the Microsoft Azure portal.</span></span> <span data-ttu-id="547d3-179">Bu bilgiyi daha önce [Uygulamayı Microsoft Azure'da kaydetme](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure) bölümünde almıştınız.</span><span class="sxs-lookup"><span data-stu-id="547d3-179">You received this information earlier during the step [Register the app in Microsoft Azure](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure).</span></span>

   ![Microsoft HR Veri Kaynağı](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. <span data-ttu-id="547d3-181">**Kaydet ve Kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="547d3-181">Select **Save & Close**.</span></span>

### <a name="grant-app-permissions-in-human-resources"></a><span data-ttu-id="547d3-182">Human Resources uygulamasında uygulama izinlerini verme</span><span class="sxs-lookup"><span data-stu-id="547d3-182">Grant app permissions in Human Resources</span></span>

<span data-ttu-id="547d3-183">Human Resources'ta iki Azure AD uygulaması için izin verin:</span><span class="sxs-lookup"><span data-stu-id="547d3-183">Grant permissions for the two Azure AD applications in Human Resources:</span></span>

- <span data-ttu-id="547d3-184">Microsoft Azure portalında kiracınız için oluşturulan uygulama</span><span class="sxs-lookup"><span data-stu-id="547d3-184">The app created for your tenant in the Microsoft Azure portal</span></span>
- <span data-ttu-id="547d3-185">Power Apps ortamında yüklü olan Dynamics 365 HR Sanal Tablo uygulaması</span><span class="sxs-lookup"><span data-stu-id="547d3-185">The Dynamics 365 HR Virtual Table app installed in the Power Apps environment</span></span> 

1. <span data-ttu-id="547d3-186">Human Resources'ta **Azure Active Directory uygulamaları** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="547d3-186">In Human Resources, open the **Azure Active Directory applications** page.</span></span>

2. <span data-ttu-id="547d3-187">Yeni uygulama kaydı oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="547d3-187">Select **New** to create a new application record:</span></span>

    - <span data-ttu-id="547d3-188">**İstemci kodu** alanına, Microsoft Azure portalına kaydettiğiniz uygulama istemci kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="547d3-188">In the **Client ID** field, enter the client ID of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="547d3-189">**Ad** alanına, Microsoft Azure portalına kaydettiğiniz uygulama adını girin.</span><span class="sxs-lookup"><span data-stu-id="547d3-189">In the **Name** field, enter the name of the app you registered in the Microsoft Azure portal.</span></span>
    - <span data-ttu-id="547d3-190">**Kullanıcı kimliği** alanında, Human Resources ve Power Apps ortamında yönetici izinlerine sahip olan kullanıcının kullanıcı kimliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="547d3-190">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

3. <span data-ttu-id="547d3-191">İkinci uygulama kaydını oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="547d3-191">Select **New** to create a second application record:</span></span>

    - <span data-ttu-id="547d3-192">**İstemci Kimliği**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="547d3-192">**Client Id**: f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span>
    - <span data-ttu-id="547d3-193">**Ad**: Dynamics 365 HR Sanal Tablosu</span><span class="sxs-lookup"><span data-stu-id="547d3-193">**Name**: Dynamics 365 HR Virtual Table</span></span>
    - <span data-ttu-id="547d3-194">**Kullanıcı kimliği** alanında, Human Resources ve Power Apps ortamında yönetici izinlerine sahip olan kullanıcının kullanıcı kimliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="547d3-194">In the **User ID** field, select the user ID of a user with admin permissions in Human Resources and the Power Apps environment.</span></span>

## <a name="generate-virtual-tables"></a><span data-ttu-id="547d3-195">Sanal tablolar oluşturma</span><span class="sxs-lookup"><span data-stu-id="547d3-195">Generate virtual tables</span></span>

<span data-ttu-id="547d3-196">Kurulum tamamlandığında, Dataverse örneğiniz içinde oluşturmak ve etkinleştirmek istediğiniz sanal tabloları seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="547d3-196">When setup completes, you can select the virtual tables you want to generate and enable in your Dataverse instance.</span></span>

1. <span data-ttu-id="547d3-197">Human Resources'ta **Microsoft Dataverse tümleştirmesi** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="547d3-197">In Human Resources, open the **Microsoft Dataverse integration** page.</span></span>

2. <span data-ttu-id="547d3-198">**Sanal tablolar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="547d3-198">Select the **Virtual tables** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="547d3-199">**Sanal tabloları etkinleştir** geçiş düğmesi, gerekli tüm kurulum tamamlandığında otomatik olarak **Evet** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="547d3-199">The **Enable virtual tables** toggle will be set to **Yes** automatically when all required setup has been completed.</span></span> <span data-ttu-id="547d3-200">Geçiş düğmesi **Hayır** olarak ayarlanmışsa, tüm önkoşul kurulumun tamamlandığından emin olmak için bu belgenin önceki bölümlerindeki adımları gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="547d3-200">If the toggle is set to **No**, review the steps in previous sections of this document to ensure all prerequisite setup is completed.</span></span>

3. <span data-ttu-id="547d3-201">Dataverse'te oluşturmak istediğiniz tabloyu veya tabloları seçin.</span><span class="sxs-lookup"><span data-stu-id="547d3-201">Select the table or tables you want to generate in Dataverse.</span></span>

4. <span data-ttu-id="547d3-202">**Oluştur/Yenile**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="547d3-202">Select **Generate/refresh**.</span></span>

![Dataverse Tümleştirmesi](./media/hr-admin-integration-dataverse-integration.png)

## <a name="check-table-generation-status"></a><span data-ttu-id="547d3-204">Tablo oluşturma durumunu denetleme</span><span class="sxs-lookup"><span data-stu-id="547d3-204">Check table generation status</span></span>

<span data-ttu-id="547d3-205">Sanal tablolar Dataverse içinde zaman uyumsuz bir arka plan işleminde oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="547d3-205">Virtual tables are generated in Dataverse through an asynchronous background process.</span></span> <span data-ttu-id="547d3-206">İşlemin üzerindeki güncelleştirmeler işlem merkezinde görüntülenebilir.</span><span class="sxs-lookup"><span data-stu-id="547d3-206">Updates on the process display in the action center.</span></span> <span data-ttu-id="547d3-207">Hata günlükleri de dahil olmak üzere işlemle ilgili ayrıntılar, **işlem otomasyonları** sayfasında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="547d3-207">Details on the process, including error logs, appear in the **Process automations** page.</span></span>

1. <span data-ttu-id="547d3-208">Human Resources'da, **İşlem otomasyonları** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="547d3-208">In Human Resources, open the **Process automations** page.</span></span>

2. <span data-ttu-id="547d3-209">**Arka plan işlemleri** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="547d3-209">Select the **Background processes** tab.</span></span>

3. <span data-ttu-id="547d3-210">**Sanal tablo yoklama asenkron operasyonu arka plan işlemi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="547d3-210">Select **Virtual table poll async operation background process**.</span></span>

4. <span data-ttu-id="547d3-211">**En son sonuçları görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="547d3-211">Select **View most recent results**.</span></span>

<span data-ttu-id="547d3-212">Yan taraftaki bölme işlemle ilgili en son yürütme sonuçlarını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="547d3-212">The slideout pane displays the most recent execution results for the process.</span></span> <span data-ttu-id="547d3-213">Dataverse'ten gelen tüm hatalar da dahil olmak üzere, işlem günlüğünü görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="547d3-213">You can view the log for the process, including any errors returned from Dataverse.</span></span>

## <a name="see-also"></a><span data-ttu-id="547d3-214">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="547d3-214">See also</span></span>

[<span data-ttu-id="547d3-215">Dataverse nedir?</span><span class="sxs-lookup"><span data-stu-id="547d3-215">What is Dataverse?</span></span>](/powerapps/maker/common-data-service/data-platform-intro)<br>
[<span data-ttu-id="547d3-216">Dataverse'teki tablolar</span><span class="sxs-lookup"><span data-stu-id="547d3-216">Tables in Dataverse</span></span>](/powerapps/maker/common-data-service/entity-overview)<br>
[<span data-ttu-id="547d3-217">Tablo ilişkilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="547d3-217">Table relationships overview</span></span>](/powerapps/maker/common-data-service/relationships-overview)<br>
[<span data-ttu-id="547d3-218">Harici veri kaynağından veri içeren sanal tablolar oluşturma ve düzenleme</span><span class="sxs-lookup"><span data-stu-id="547d3-218">Create and edit virtual tables that contain data from an external data source</span></span>](/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[<span data-ttu-id="547d3-219">Power Apps portalları nedir?</span><span class="sxs-lookup"><span data-stu-id="547d3-219">What is Power Apps portals?</span></span>](/powerapps/maker/portals/overview)<br>
[<span data-ttu-id="547d3-220">Power Apps'ta uygulamalar oluşturmaya genel bakış</span><span class="sxs-lookup"><span data-stu-id="547d3-220">Overview of creating apps in Power Apps</span></span>](/powerapps/maker/)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
