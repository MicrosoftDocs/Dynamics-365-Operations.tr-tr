---
title: Finance Insights için Yapılandırma (10.0.19 sürümüne kadar)
description: Bu konuda, sisteminizin Finance Insights'da (10.0.19 sürümüne kadar) sunulan özellikleri kullanabilmesini sağlayacak yapılandırma adımları açıklanmaktadır.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 6ad06bb6d041fc060b3a99538f6d4d0af333180f
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186432"
---
# <a name="configuration-for-finance-insights-preview"></a><span data-ttu-id="2f6c3-103">Mali içgörüler için yapılandırma (önizleme)</span><span class="sxs-lookup"><span data-stu-id="2f6c3-103">Configuration for Finance insights (preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="2f6c3-104">Finance Insights'ı ayarlamak için aşağıdaki yordamlar, 10.0.19'a kadar Microsoft Dynamics 365 Finance sürümleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-104">The following procedures for setting up Finance insights are valid for Microsoft Dynamics 365 Finance versions up to 10.0.19.</span></span> <span data-ttu-id="2f6c3-105">Finance Insights'ı sürüm 10.0.20 ve sonrasında ayarlamak için bkz. [Sürüm 10.0.20 ve sonrasında Finance Insights yapılandırmaları](configure-for-fin-insites-PubPrvw.md).</span><span class="sxs-lookup"><span data-stu-id="2f6c3-105">To set up Finance insights on version 10.0.20 and later, see [Configuration for Finance Insights (preview) - versions 10.0.20 and beyond](configure-for-fin-insites-PubPrvw.md).</span></span>

<span data-ttu-id="2f6c3-106">Mali içgörüler, kuruluşunuza güçlü tahmin araçları sunmak için Microsoft Dynamics 365 Finance işlevlerini Microsoft Dataverse, Azure ve AI Builder işlevleriyle bir araya getirir.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-106">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Microsoft Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="2f6c3-107">Bu konuda, sisteminizin Mali içgörülerde sunulan özellikleri kullanabilmesini sağlayacak yapılandırma adımları açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-107">This topic explains the configuration steps that will enable your system to use the capabilities that are available in Finance insights.</span></span>

## <a name="deploy-dynamics-365-finance"></a><span data-ttu-id="2f6c3-108">Dynamics 365 Finance dağıtımı</span><span class="sxs-lookup"><span data-stu-id="2f6c3-108">Deploy Dynamics 365 Finance</span></span>

<span data-ttu-id="2f6c3-109">Şu adımları izleyerek ortamları dağıtın.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-109">Deploy the environments by following these steps.</span></span>

1. <span data-ttu-id="2f6c3-110">Microsoft Dynamics Lifecycle Services (LCS) portalında, bir Dynamics 365 Finance ortamı oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-110">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Dynamics 365 Finance environment.</span></span> <span data-ttu-id="2f6c3-111">Ortam, sürüm 10.0.11/Platform update 35 veya daha sonraki bir uygulama sürümü gerektirir.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-111">The environment requires app version 10.0.11/Platform update 35 or later.</span></span>
2. <span data-ttu-id="2f6c3-112">Ortam, Korumalı Alan içinde yüksek kullanılabilirlik (HA) ortamı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-112">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="2f6c3-113">(Bu ortam türü aynı zamanda Katman 2 ortamı olarak da bilinir.) Daha fazla bilgi için bkz. [Ortam planlama](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="2f6c3-113">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="2f6c3-114">Finance Insights'ı bir korumalı alanda yapılandırıyorsanız tahminlerin çalışması için üretim verilerini ilgili ortama kopyalamanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-114">If you are configuring Finance insights in a Sandbox environment, you might need to copy production data to that environment for predictions to work.</span></span> <span data-ttu-id="2f6c3-115">Tahmin modeli, tahminleri oluşturmak için birkaç senelik verileri kullanır.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-115">The prediction model uses multiple years of data to build predictions.</span></span> <span data-ttu-id="2f6c3-116">Contoso demo verileri, tahmin modelini yeterince geliştirmek için yeterli tarihsel veri içermez.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-116">The Contoso demo data doesn’t contain enough historical data to train the prediction model adequately.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="2f6c3-117">Dataverse'ı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="2f6c3-117">Configure Dataverse</span></span>

<span data-ttu-id="2f6c3-118">Finance Insights için Dataverse'ü yapılandırmak için aşağıdaki adımları kullanın.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-118">Use the following steps to configure Dataverse for Finance insights.</span></span>

1. <span data-ttu-id="2f6c3-119">LCS'deki ortam sayfasını açın ve **Power Platform Tümleştirme** bölümünün ayarlı olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-119">Open the environment page in LCS and verify that the **Power Platform Integration** section is already setup.</span></span>
    1. <span data-ttu-id="2f6c3-120">Ayarlıysa Dynamics 365 Finance Ortamına bağlı Dataverse ortam adının listelenmiş olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-120">If it is already set up, the Dataverse environment name linked to the Dynamics 365 Finance Environment should be listed.</span></span> <span data-ttu-id="2f6c3-121">Dataverse ortam adını kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-121">Copy the Dataverse environment name.</span></span>
    2. <span data-ttu-id="2f6c3-122">Ayarlı değilse aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2f6c3-122">If it is not set up, follow these steps:</span></span>
        1. <span data-ttu-id="2f6c3-123">Power Platform Tümleştirme bölümünde **Kurulum** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-123">Select the **Setup** button in the Power Platform Integration section.</span></span> <span data-ttu-id="2f6c3-124">Ortamın kurulumu bir saat kadar sürebilir.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-124">It may take up to an hour for the environment to be set up.</span></span>
        2. <span data-ttu-id="2f6c3-125">Dataverse ortamı başarıyla ayarlandığında Dynamics 365 Finance Ortamına bağlı Dataverse ortam adının listelenmiş olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-125">If the Dataverse environment is successfully set up, the Dataverse environment name linked to the Dynamics 365 Finance Environment should be listed.</span></span> <span data-ttu-id="2f6c3-126">Dataverse ortam adını kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-126">Copy the Dataverse environment name.</span></span>
> [!NOTE]
> <span data-ttu-id="2f6c3-127">Ortam kurulumu tamamladıktan sonra, **Uygulamalar için CDS bağlantısı** düğmesini **SEÇMEYİN**.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-127">After completing the environment set up, **DO NOT** select the **Link to CDS for Apps** button.</span></span> <span data-ttu-id="2f6c3-128">Bu, Finance Insights için gerekli değildir ve LCS'de gerekli Ortam Eklentilerini tamamlama özelliğini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-128">This is not needed for Finance Insights and will disable the ability to complete the required Environment Add-ins in LCS.</span></span>

2. <span data-ttu-id="2f6c3-129">[Power Platform yönetim merkezini](https://admin.powerplatform.microsoft.com/)açın ve aynı Active Directory kiracısında yeni bir Dataverse ortamı oluşturmak için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2f6c3-129">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), and follow these steps to create a new Dataverse environment in the same Active Directory tenant:</span></span>

    1. <span data-ttu-id="2f6c3-130">**Ortamlar** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-130">Open the **Environments** page.</span></span>

        <span data-ttu-id="2f6c3-131">[![Ortamlar sayfası](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span><span class="sxs-lookup"><span data-stu-id="2f6c3-131">[![Environments page](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span></span>

    2. <span data-ttu-id="2f6c3-132">Yukarıda oluşturulan Dataverse ortamını seçin ve ardından **Ayarlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-132">Select the Dataverse environment created above and then select **Settings**.</span></span>
    3. <span data-ttu-id="2f6c3-133">**Kaynaklar \> Tüm Eski Ayarlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-133">Select **Resources \> All Legacy Settings**.</span></span>
    4. <span data-ttu-id="2f6c3-134">Üst gezinti çubuğunda, **Ayarlar**'ı seçin ve ardından **Özelleştirmeler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-134">On the top navigation bar, select **Settings**, and then select **Customizations**.</span></span>
    5. <span data-ttu-id="2f6c3-135">**Geliştirici Kaynakları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-135">Select **Developer Resources**.</span></span>
    6. <span data-ttu-id="2f6c3-136">**Dataverse kuruluş kimliği** değerini kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-136">Copy the **Dataverse organization ID** value.</span></span>
    7. <span data-ttu-id="2f6c3-137">Tarayıcının adres çubuğunda Dataverse kuruluşunun URL'sini not edin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-137">In the browser's address bar, make a note of the URL for the Dataverse organization.</span></span> <span data-ttu-id="2f6c3-138">Örneğin, URL şu şekilde olabilir: `https://org42b2b3d3.crm.dynamics.com`.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-138">For example, the URL might be `https://org42b2b3d3.crm.dynamics.com`.</span></span>

3. <span data-ttu-id="2f6c3-139">Nakit akışı tahminleri veya bütçe tahminleri özelliğini kullanmayı planlıyorsanız kuruluşunuzun ek açıklama sınırını en az 50 megabayt (MB) olarak güncelleştirmek için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2f6c3-139">If you plan to use the Cash flow forecasts or Budget forecasts feature, follow these steps to update the annotation limit for your organization to at least 50 megabytes (MB):</span></span>

    1. <span data-ttu-id="2f6c3-140">[Power Apps portalını](https://make.powerapps.com) açın.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-140">Open the [Power Apps portal](https://make.powerapps.com).</span></span>
    2. <span data-ttu-id="2f6c3-141">Yeni oluşturduğunuz ortamı seçin ve sonra **Gelişmiş ayarlar**'ı seçin .</span><span class="sxs-lookup"><span data-stu-id="2f6c3-141">Select the environment that you just created, and then select **Advanced settings**.</span></span>
    3. <span data-ttu-id="2f6c3-142">**Ayarlar \> E-posta Yapılandırması**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-142">Select **Settings \> Email Configuration**.</span></span>
    4. <span data-ttu-id="2f6c3-143">**Maksimum dosya boyutu** alanının değerini **51.200** olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-143">Change the value of the **Maximum file size** field to **51,200**.</span></span> <span data-ttu-id="2f6c3-144">(Değer, kilobayt \[KB\] cinsinden ifade edilir.)</span><span class="sxs-lookup"><span data-stu-id="2f6c3-144">(The value is expressed in kilobytes \[KB\].)</span></span>
    5. <span data-ttu-id="2f6c3-145">Yaptığınız değişiklikleri kaydetmek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-145">Select **OK** to save your changes.</span></span>

## <a name="configure-the-azure-setup"></a><span data-ttu-id="2f6c3-146">Azure kurulumunu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="2f6c3-146">Configure the Azure setup</span></span>

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a><span data-ttu-id="2f6c3-147">Dataverse dizin kodunu ve kullanıcının Azure AD nesne kodunu girin</span><span class="sxs-lookup"><span data-stu-id="2f6c3-147">Enter the Dataverse directory ID and the user's Azure AD object ID</span></span>

1. <span data-ttu-id="2f6c3-148">Dataverse dizin kodunu girin:</span><span class="sxs-lookup"><span data-stu-id="2f6c3-148">Enter the Dataverse directory ID:</span></span>

    1. <span data-ttu-id="2f6c3-149">[Azure portalını](https://portal.azure.com) açın.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-149">Open the [Azure portal](https://portal.azure.com).</span></span>
    2. <span data-ttu-id="2f6c3-150">Dataverse ortamı oluşturmak için kullanılan kullanıcı kimliğini kullanarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-150">Sign in by using the user ID that was used to create the Dataverse environment.</span></span>
    3. <span data-ttu-id="2f6c3-151">**Azure Active Directory** gidin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-151">Go to **Azure Active Directory**.</span></span>
    4. <span data-ttu-id="2f6c3-152">**Kiracı Kimliği** değerini kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-152">Copy the **Tenant ID** value.</span></span>

2. <span data-ttu-id="2f6c3-153">Kullanıcının Azure Active Directory (Azure AD) nesne kimliğini girin:</span><span class="sxs-lookup"><span data-stu-id="2f6c3-153">Enter the user's Azure Active Directory (Azure AD) object ID:</span></span>

    1. <span data-ttu-id="2f6c3-154">[Azure portalı](https://portal.azure.com) içinde **Kullanıcılar**'a gidin ve e-posta adresine göre kullanıcıyı arayın.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-154">In the [Azure portal](https://portal.azure.com), go to **Users**, and search for the user by email address.</span></span>
    2. <span data-ttu-id="2f6c3-155">Kullanıcının adını seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-155">Select the user's name.</span></span>
    3. <span data-ttu-id="2f6c3-156">**Nesne Kimliği** değerini kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-156">Copy the **Object ID** value.</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="2f6c3-157">Mali içgörüler Data Lake kaynaklarını ayarlamak için Azure Cloud Shell kullanma</span><span class="sxs-lookup"><span data-stu-id="2f6c3-157">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="2f6c3-158">Windows PowerShell betik dosyası kullanma</span><span class="sxs-lookup"><span data-stu-id="2f6c3-158">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="2f6c3-159">[Azure Data Lake'e aktarmayı yapılandırma](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) konusunda açıklandığı gibi Azure kaynaklarını kolayca ayarlayabilmeniz için Windows PowerShell betik dosyası sağlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-159">A Windows PowerShell script has been provided, so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="2f6c3-160">El ile kurulum yapmayı tercih ediyorsanız bu yordamı atlayın ve [El ile kurulum](#manual-setup) bölümündeki yordama devam edin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-160">If you prefer to do manual setup, skip this procedure, and continue with the procedure in the [Manual setup](#manual-setup) section.</span></span>

> [!NOTE]
> <span data-ttu-id="2f6c3-161">PowerShell betiğini çalıştırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-161">Follow the steps below to run the PowerShell script.</span></span> <span data-ttu-id="2f6c3-162">Azure CLI "Try it" seçeneği veya betiği bilgisayarınızda çalıştırmak işe yaramayabilir.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-162">The Azure CLI "Try it" option, or running the script on your PC may not work.</span></span>

<span data-ttu-id="2f6c3-163">Windows PowerShell betik dosyasını kullanarak Azure yapılandırmayla ilgili bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-163">Follow these steps to configure Azure by using the Windows PowerShell script.</span></span> <span data-ttu-id="2f6c3-164">Azure kaynak grubu, Azure kaynakları ve bir Azure AD uygulaması oluşturma haklarınız olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-164">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="2f6c3-165">Gerekli izinler hakkında daha fazla bilgi için bkz. [Azure AD izinlerini denetleme](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="2f6c3-165">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="2f6c3-166">[Azure portalda](https://portal.azure.com) hedef Azure aboneliğinize gidin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-166">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span> <span data-ttu-id="2f6c3-167">**Arama** alanının sağında bulunan **Cloud Shell** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-167">Select the **Cloud Shell** button to the right of the **Search** field.</span></span>
2. <span data-ttu-id="2f6c3-168">**PowerShell**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-168">Select **PowerShell**.</span></span>
3. <span data-ttu-id="2f6c3-169">İstenirse depolama alanı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-169">Create storage if you're prompted to do so.</span></span>
4. <span data-ttu-id="2f6c3-170">**Azure CLI** sekmesine gidin ve **Kopyala**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-170">Go to the **Azure CLI** tab and select **Copy**.</span></span>  
5. <span data-ttu-id="2f6c3-171">Not defterini açın ve PowerShell betiğini yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-171">Open Notepad and paste the PowerShell script.</span></span> <span data-ttu-id="2f6c3-172">Dosyayı, ConfigureDataLake.ps1 olarak kaydedin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-172">Save the file as ConfigureDataLake.ps1.</span></span>
6. <span data-ttu-id="2f6c3-173">Cloud Shell'de yükleme için menü seçeneğini kullanarak Windows PowerShell betiğini oturuma yükleyin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-173">Upload the Windows PowerShell script to the session using the menu option for upload in Cloud Shell.</span></span>
7. <span data-ttu-id="2f6c3-174">.\ConfigureDataLake.ps1 betiğini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-174">Run the script .\ConfigureDataLake.ps1.</span></span>
8. <span data-ttu-id="2f6c3-175">Betik dosyasını çalıştırmak için istemleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-175">Follow the prompts to run the script.</span></span>
9. <span data-ttu-id="2f6c3-176">LCS'ye **Data Lake'e dışarı aktar** eklentisini yüklemek için betik dosyası çıktısındaki bilgileri kullanın.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-176">Use the information from the script output to install the **Export to Data Lake** add-in in LCS.</span></span>
10. <span data-ttu-id="2f6c3-177">Finance'teki **Veri bağlantıları** sayfasında varlık deposunu etkinleştirmek için betik dosyası çıktısındaki bilgileri kullanın (**Sistem yönetimi \> Sistem parametreleri \> Veri bağlantıları**).</span><span class="sxs-lookup"><span data-stu-id="2f6c3-177">Use the information from the script output to enable the entity store on the **Data connections** page in Finance (**System administration \> System parameters \> Data connections**).</span></span>

### <a name="manual-setup"></a><span data-ttu-id="2f6c3-178">El ile kurulum</span><span class="sxs-lookup"><span data-stu-id="2f6c3-178">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="2f6c3-179">Azure AD kiracısına uygulama ekleme</span><span class="sxs-lookup"><span data-stu-id="2f6c3-179">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="2f6c3-180">[Azure portalda](https://portal.azure.com) **Azure Active Directory**'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-180">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="2f6c3-181">**Yönet \> Kurumsal uygulamalar** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-181">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="2f6c3-182">Uygulama kimliğine göre aşağıdaki uygulamaları arayın.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-182">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="2f6c3-183">Uygulama</span><span class="sxs-lookup"><span data-stu-id="2f6c3-183">Application</span></span>                              | <span data-ttu-id="2f6c3-184">Uygulama kodu</span><span class="sxs-lookup"><span data-stu-id="2f6c3-184">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="2f6c3-185">Microsoft Dynamics ERP Mikro Hizmetleri</span><span class="sxs-lookup"><span data-stu-id="2f6c3-185">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="2f6c3-186">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="2f6c3-186">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="2f6c3-187">Microsoft Dynamics ERP Mikro Hizmetleri CDS</span><span class="sxs-lookup"><span data-stu-id="2f6c3-187">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="2f6c3-188">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="2f6c3-188">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="2f6c3-189">AI Builder Yetkilendirme Hizmeti</span><span class="sxs-lookup"><span data-stu-id="2f6c3-189">AI Builder Authorization Service</span></span>         | <span data-ttu-id="2f6c3-190">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="2f6c3-190">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="2f6c3-191">Önceki uygulamalardan hiçbirini bulamazsanız aşağıdaki adımları deneyin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-191">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="2f6c3-192">Yerel makinenizde, **Başlat** menüsünü seçin ve **powershell**'i arayın.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-192">On your local machine, select the **Start** menu, and search for **powershell**.</span></span>
2. <span data-ttu-id="2f6c3-193">**Windows PowerShell**'i seçin ve basılı tutun (veya sağ tıklayın) ve sonra **Yönetici olarak çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-193">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="2f6c3-194">**AzureAD** modülünü yüklemek için aşağıdaki komutu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-194">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="2f6c3-195">Devam etmek için NuGet sağlayıcısı gerekiyorsa yüklemek için **Y**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-195">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="2f6c3-196">"Güvenilmeyen depo" iletisi görüntülenirse devam etmek için **Y**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-196">If an "Untrusted repository" message appears, select **Y** to continue.</span></span>
6. <span data-ttu-id="2f6c3-197">Eklenmesi gereken her uygulama için uygulamayı Azure AD'ye eklemek üzere aşağıdaki komutları çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-197">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="2f6c3-198">İstendiğinde, Azure AD yöneticisi olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-198">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="2f6c3-199">Azure kaynakları oluşturma</span><span class="sxs-lookup"><span data-stu-id="2f6c3-199">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="2f6c3-200">Dataverse ortamıyla aynı Azure AD kurulumunda aşağıdaki kaynakları oluşturduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-200">Make sure that you create the following resources in the same Azure AD instance as the Dataverse environment.</span></span> <span data-ttu-id="2f6c3-201">Farklı bir Azure AD kurulumundan kaynak kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-201">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="2f6c3-202">Yeni depolama hesabı oluşturma:</span><span class="sxs-lookup"><span data-stu-id="2f6c3-202">Create a new storage account:</span></span>

    1. <span data-ttu-id="2f6c3-203">[Azure portalında](https://portal.azure.com) bir depolama hesabı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-203">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="2f6c3-204">**Depolama hesabı oluştur** iletişim kutusunda, aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2f6c3-204">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="2f6c3-205">**Konum**: Ortamınızın bulunduğu veri merkezini seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-205">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="2f6c3-206">**Performans**: **Standart** seçeneğini belirlemenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-206">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="2f6c3-207">**Hesap türü**: **StorageV2**'yi seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-207">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="2f6c3-208">**Gelişmiş seçenekler** iletişim kutusunda **Data Lake Storage 2. Nesil** seçeneği için **Hiyerarşik ad alanları** bölümünde **Etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-208">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="2f6c3-209">Bu özelliği devre dışı bırakırsanız Power BI veri akışları gibi hizmetleri kullanarak, Finance and Operations uygulamalarının yazdığı verileri kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-209">If you disable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="2f6c3-210">**İncele ve oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-210">Select **Review and create**.</span></span> <span data-ttu-id="2f6c3-211">Dağıtım tamamlandığında, yeni kaynak Azure portalında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-211">When the deployment is completed, the new resource will be shown in the Azure portal.</span></span>
    5. <span data-ttu-id="2f6c3-212">Oluşturduğunuz depolama hesabına gidin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-212">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="2f6c3-213">Sol menüde **Erişim anahtarları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-213">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="2f6c3-214">**Key1** veya **Key2** için bağlantı dizesini kopyalayıp kaydedin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-214">Copy and save the connection string for either **Key1** or **Key2**.</span></span>
    8. <span data-ttu-id="2f6c3-215">Depolama hesabı adını kopyalayın ve kaydedin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-215">Copy and save the storage account name.</span></span>

2. <span data-ttu-id="2f6c3-216">Yeni bir anahtar kasası oluşturma:</span><span class="sxs-lookup"><span data-stu-id="2f6c3-216">Create a new key vault:</span></span>

    1. <span data-ttu-id="2f6c3-217">[Azure portalında](https://portal.azure.com) bir anahtar kasası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-217">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="2f6c3-218">**Anahtar kasası oluştur** iletişim kutusundaki **Konum** alanında ortamınızın bulunduğu veri merkezini seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-218">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="2f6c3-219">Anahtar kasası oluşturulduktan sonra, kasayı listeden seçin ve ardından **Gizli anahtarlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-219">After key vault is created, select it in the list, and then select **Secrets**.</span></span>
    4. <span data-ttu-id="2f6c3-220">**Oluştur/İçe aktar** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-220">Select **Generate/Import**.</span></span>
    5. <span data-ttu-id="2f6c3-221">**Gizli anahtar oluştur** iletişim kutusunda **Karşıya yükleme seçenekleri** alanında, **El ile** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-221">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
    6. <span data-ttu-id="2f6c3-222">Gizli anahtar için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-222">Enter a name for the secret.</span></span> <span data-ttu-id="2f6c3-223">Daha sonra sağlamanız gerekeceği için bu adı not edin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-223">Make a note of the name, because you will have to provide it later.</span></span>
    7. <span data-ttu-id="2f6c3-224">**Değer** alanında, önceki yordamda depolama hesabından elde ettiğiniz bağlantı dizesini girin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-224">In the **Value** field, enter the connection string that you obtained from the storage account in the previous procedure.</span></span>
    8. <span data-ttu-id="2f6c3-225">**Etkin**'i ve ardından **Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-225">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="2f6c3-226">Gizli anahtar oluşturulur ve Key Vault'a eklenir.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-226">The secret is created and added to Key Vault.</span></span>
    9. <span data-ttu-id="2f6c3-227">**Key Vault'a Genel Bakış**'a gidin ve DNS adını not edin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-227">Go to the **Key Vault Overview**, and make a note of the DNS name.</span></span>

3. <span data-ttu-id="2f6c3-228">Bir Azure AD uygulaması oluşturma ve kaydetme:</span><span class="sxs-lookup"><span data-stu-id="2f6c3-228">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="2f6c3-229">[Azure portalında](https://portal.azure.com) **Azure Active Directory**'ye gidin ve ardından **Uygulama kayıtları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-229">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="2f6c3-230">**Yeni uygulama kaydı**'nı seçin ve aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2f6c3-230">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="2f6c3-231">**Ad**: Uygulamanın adını girin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-231">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="2f6c3-232">**Uygulama türü**: **Web API'si** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-232">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="2f6c3-233">**Yeniden yönlendirme URI'si kurulumu**: Dynamics 365 kurulumunuzun URL'sini girin (ör. `https://yourdynamicsinstance.dynamics.com/auth`).</span><span class="sxs-lookup"><span data-stu-id="2f6c3-233">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as, `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="2f6c3-234">Yeni oluşturduğunuz uygulamaya gidin ve **Uygulama (istemci) kimliği** değerini kopyalayın ve kaydedin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-234">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="2f6c3-235">Anahtar kasasını ayarlarken bu değeri sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-235">You will have to provide this value later, when you set up the key vault.</span></span>
    4. <span data-ttu-id="2f6c3-236">**API izinleri**'ne gidin ve şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2f6c3-236">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="2f6c3-237">**İzin ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-237">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="2f6c3-238">**Azure Key Vault**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-238">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="2f6c3-239">Temsilci izinleri seçtikten sonra **kullanıcı\_kimliğe bürünmey**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-239">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="2f6c3-240">**İzin ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-240">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="2f6c3-241">Uygulama menüsünde, **Sertifikalar \& gizli anahtarlar**'ı seçin ve ardından Key Vault gizli anahtarlarını oluşturmak için bu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2f6c3-241">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="2f6c3-242">**Yeni gizli anahtar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-242">Select **New client secret**.</span></span>
        2. <span data-ttu-id="2f6c3-243">**Anahtar Açıklaması** alanına bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-243">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="2f6c3-244">Bir süre seçin ve ardından **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-244">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="2f6c3-245">**Değer** alanında gizli anahtar oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-245">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="2f6c3-246">Gizli anahtar değerini kopyalayın ve kaydedin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-246">Copy and save the secret value.</span></span>

4. <span data-ttu-id="2f6c3-247">Key Vault gizli anahtarları oluşturma:</span><span class="sxs-lookup"><span data-stu-id="2f6c3-247">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="2f6c3-248">Daha önce oluşturduğunuz anahtar kasasına gidin ve **Gizli Anahtarlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-248">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="2f6c3-249">Aşağıdaki tabloda bulunan her gizli anahtar adı için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2f6c3-249">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="2f6c3-250">**Oluştur/İçe aktar** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-250">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="2f6c3-251">**Gizli anahtar oluştur** iletişim kutusunda **Karşıya yükleme seçenekleri** alanında, **El ile** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-251">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="2f6c3-252">Aşağıdaki tablodan gizli anahtar adını ve değerini oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-252">Create the secret name and value from the following table.</span></span>
        4. <span data-ttu-id="2f6c3-253">**Etkin**'i ve ardından **Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-253">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="2f6c3-254">Gizli anahtar oluşturulur ve Key Vault'a eklenir.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-254">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="2f6c3-255">Parola adı</span><span class="sxs-lookup"><span data-stu-id="2f6c3-255">Secret name</span></span>                       | <span data-ttu-id="2f6c3-256">Gizli anahtar değeri</span><span class="sxs-lookup"><span data-stu-id="2f6c3-256">Secret value</span></span>                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | <span data-ttu-id="2f6c3-257">app-id</span><span class="sxs-lookup"><span data-stu-id="2f6c3-257">app-id</span></span>                            | <span data-ttu-id="2f6c3-258">Daha önce oluşturduğunuz uygulamanın uygulama kimliği</span><span class="sxs-lookup"><span data-stu-id="2f6c3-258">The app ID of the application that you created earlier</span></span>                                      |
        | <span data-ttu-id="2f6c3-259">app-secret</span><span class="sxs-lookup"><span data-stu-id="2f6c3-259">app-secret</span></span>                        | <span data-ttu-id="2f6c3-260">Daha önce kaydettiğiniz gizli anahtar</span><span class="sxs-lookup"><span data-stu-id="2f6c3-260">The client secret that you saved earlier</span></span>                                                    |
        | <span data-ttu-id="2f6c3-261">storage-account-name</span><span class="sxs-lookup"><span data-stu-id="2f6c3-261">storage-account-name</span></span>              | <span data-ttu-id="2f6c3-262">Daha önce oluşturduğunuz depolama hesabının adı (ör. **storageaccount1**)</span><span class="sxs-lookup"><span data-stu-id="2f6c3-262">The name of the storage account that you created earlier, such as **storageaccount1**</span></span>       |
        | <span data-ttu-id="2f6c3-263">storage-account-connection-string</span><span class="sxs-lookup"><span data-stu-id="2f6c3-263">storage-account-connection-string</span></span> | <span data-ttu-id="2f6c3-264">Depolama hesabı için **Erişim anahtarları** sayfasından kopyaladığınız bağlantı dizesi</span><span class="sxs-lookup"><span data-stu-id="2f6c3-264">The connection string that you copied from the **Access keys** page for the storage account</span></span> |

5. <span data-ttu-id="2f6c3-265">Anahtar kasasına erişmek için uygulamayı yetkilendirme:</span><span class="sxs-lookup"><span data-stu-id="2f6c3-265">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="2f6c3-266">[Azure portalında](https://portal.azure.com), daha önce oluşturduğunuz anahtar kasasını açın.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-266">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="2f6c3-267">Erişim ilkelerini seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-267">Select the access policies.</span></span>
    3. <span data-ttu-id="2f6c3-268">Aşağıdaki tabloda bulunan her uygulama için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2f6c3-268">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="2f6c3-269">Erişim ilkesi oluşturmak için **Erişim İlkesi Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-269">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="2f6c3-270">**Gizli anahtar izinleri** alanında, aşağıdaki tabloda yer alan izinleri seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-270">In the **Secret permissions** field, select the permissions from the following table.</span></span>
        3. <span data-ttu-id="2f6c3-271">**Sorumlu seç** alanında aşağıdaki tablodan uygulama görünen adını arayın.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-271">In the **Select principal** field, search for the application display name from the following table.</span></span>
        4. <span data-ttu-id="2f6c3-272">**Seç** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-272">Select **Select**.</span></span>
        5. <span data-ttu-id="2f6c3-273">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-273">Select **Add**.</span></span>
        6. <span data-ttu-id="2f6c3-274">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-274">Select **Save**.</span></span>

        | <span data-ttu-id="2f6c3-275">Uygulama</span><span class="sxs-lookup"><span data-stu-id="2f6c3-275">Application</span></span>                                              | <span data-ttu-id="2f6c3-276">İzinler</span><span class="sxs-lookup"><span data-stu-id="2f6c3-276">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="2f6c3-277">Oluşturduğunuz yeni uygulamanın görünen adı</span><span class="sxs-lookup"><span data-stu-id="2f6c3-277">The display name of the new application that you created</span></span> | <span data-ttu-id="2f6c3-278">Al, Listele</span><span class="sxs-lookup"><span data-stu-id="2f6c3-278">Get, List</span></span>   |
        | <span data-ttu-id="2f6c3-279">**Microsoft Dynamics ERP Mikro Hizmetleri**</span><span class="sxs-lookup"><span data-stu-id="2f6c3-279">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="2f6c3-280">Al, Listele</span><span class="sxs-lookup"><span data-stu-id="2f6c3-280">Get, List</span></span>   |

6. <span data-ttu-id="2f6c3-281">Depolama hesabına erişmek için rolleri atama:</span><span class="sxs-lookup"><span data-stu-id="2f6c3-281">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="2f6c3-282">[Azure portalında](https://portal.azure.com), daha önce oluşturduğunuz depolama hesabını açın.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-282">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="2f6c3-283">**Access Control (IAM)** seçeneğini belirleyin ve ardından **Rol Atamaları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-283">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="2f6c3-284">**Ekle, Rol Ataması Ekle** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-284">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="2f6c3-285">Aşağıdaki tabloda bulunan her uygulama için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2f6c3-285">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="2f6c3-286">Aşağıdaki tablodan rolü seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-286">Select the role from the following table.</span></span>
        2. <span data-ttu-id="2f6c3-287">**Erişim ata** alanını **Azure AD kullanıcısı, grubu veya hizmet sorumlusu** olarak bırakın.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-287">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="2f6c3-288">**Seç** alanında aşağıdaki tablodan uygulamayı girin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-288">In the **Select** field, enter the application from the following table.</span></span>
        4. <span data-ttu-id="2f6c3-289">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-289">Select **Save**.</span></span>

        | <span data-ttu-id="2f6c3-290">Uygulama</span><span class="sxs-lookup"><span data-stu-id="2f6c3-290">Application</span></span>                                              | <span data-ttu-id="2f6c3-291">Rol</span><span class="sxs-lookup"><span data-stu-id="2f6c3-291">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="2f6c3-292">Oluşturduğunuz yeni uygulamanın görünen adı</span><span class="sxs-lookup"><span data-stu-id="2f6c3-292">The display name of the new application that you created</span></span> | <span data-ttu-id="2f6c3-293">Sahip</span><span class="sxs-lookup"><span data-stu-id="2f6c3-293">Owner</span></span>                       |
        | <span data-ttu-id="2f6c3-294">Oluşturduğunuz yeni uygulamanın görünen adı</span><span class="sxs-lookup"><span data-stu-id="2f6c3-294">The display name of the new application that you created</span></span> | <span data-ttu-id="2f6c3-295">Katılımcı</span><span class="sxs-lookup"><span data-stu-id="2f6c3-295">Contributor</span></span>                 |
        | <span data-ttu-id="2f6c3-296">Oluşturduğunuz yeni uygulamanın görünen adı</span><span class="sxs-lookup"><span data-stu-id="2f6c3-296">The display name of the new application that you created</span></span> | <span data-ttu-id="2f6c3-297">Depolama Hesabı Katılımcısı</span><span class="sxs-lookup"><span data-stu-id="2f6c3-297">Storage Account Contributor</span></span> |
        | <span data-ttu-id="2f6c3-298">Oluşturduğunuz yeni uygulamanın görünen adı</span><span class="sxs-lookup"><span data-stu-id="2f6c3-298">The display name of the new application that you created</span></span> | <span data-ttu-id="2f6c3-299">Depolama Blobu Veri Sahibi</span><span class="sxs-lookup"><span data-stu-id="2f6c3-299">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="2f6c3-300">**AI Builder Yetkilendirme Hizmeti**</span><span class="sxs-lookup"><span data-stu-id="2f6c3-300">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="2f6c3-301">Depolama Blobu Veri Okuyucusu</span><span class="sxs-lookup"><span data-stu-id="2f6c3-301">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="2f6c3-302">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="2f6c3-302">Azure CLI</span></span>](#tab/azure-azure-cli)

```
function New-FinanceDataLakeAzureResources {
    Assert-ScriptSetup

    $ClientAppName = 'Finance Data Lake Application'
    $DefaultSecretExpiryInYear = 1
    $MicrosoftDynamicsERPMicroservicesAppId = '0cdb527f-a8d1-4bf8-9436-b352c68682b2'
    $MicrosoftDynamicsERPMicroservicesCDSAppId = '703e2651-d3fc-48f5-942c-74274233dba8'
    $AIBuilderAuthorizationServiceAppId = 'ad40333e-9910-4b61-b281-e3aeeb8c3ef3'
    $KeyVaultServicePrincipalAppId = 'cfa8b339-82a2-471a-a3c9-0fc0be7a4093'
    $GraphServicePrincipalAppId = '00000003-0000-0000-c000-000000000000'

    Import-Module AzureAD.Standard.Preview
    $connectAzureADParameters = @{ 'Identity' = $true; 'TenantId' = $env:ACC_TID }
    $azContext = AzureAD.Standard.Preview\Connect-AzureAD @connectAzureADParameters
    $userContext = ConvertFrom-Json ((az ad signed-in-user show) -join '')
    $user = Get-AzureADUser -Filter ("UserPrincipalName eq '" + $userContext.UserPrincipalName + "'")

    Set-AzureSubscription
    
    $resourceGroup = $null
    $ResourceGroupName = 'D365FinanceInsightsDataLake'
    $ResourceGroupNameSuffix = ''
    $FullResourceGroupName = ''
    Write-Output ("The default Azure Resource Group name is '{0}'" -f $ResourceGroupName)
    while (-not ($resourceGroup)) {
        $ResourceGroupNameSuffix = (Read-Host -Prompt "Enter optional Azure Resource Group name suffix: (leave blank for no suffix)")
        if ([string]::IsNullOrWhitespace($ResourceGroupNameSuffix))
        {
            $FullResourceGroupName = $ResourceGroupName
        }
        else
        {
            if ($ResourceGroupNameSuffix -notmatch "^[A-Za-z0-9]+$") {
                Write-Warning "The Azure Resource Group name suffix can only include alphanumeric characters."
                continue
            }

            if ($ResourceGroupNameSuffix.Length -gt 60) {
                Write-Warning "The Azure Resource Group name suffix cannot be longer than 60 characters."
                continue
            }

            $FullResourceGroupName = $ResourceGroupName + $ResourceGroupNameSuffix
        }
        
        $resourceGroup = Get-AzResourceGroup -Name $FullResourceGroupName -ErrorAction SilentlyContinue

        if (-not ($resourceGroup)) {
            Write-Output ("Your new Azure Resource Group name is '{0}'" -f $FullResourceGroupName)
            $resourceLocation = ''
            $azResourceLocations = (Get-AzLocation | Select-Object Location).Location
            while ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations))) {
                $resourceLocation = (Read-Host -Prompt "Enter the location in which to create the Azure Resource Group: ('help' to see values)")
                if ($resourceLocation -eq 'help') {
                    Write-Output ("List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
                elseif ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations)))
                {
                    Write-Warning ("The provided location is not available for resource group. List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
            }
            $resourceGroup = New-AzResourceGroup -Name $FullResourceGroupName -Location $resourceLocation
            Write-Output ("Created Azure Resource Group '{0}'" -f $resourceGroup.ResourceGroupName)
        }
        else {
            Write-Output ("Found Azure Resource Group '{0}'" -f ($resourceGroup.ResourceGroupName))
        }
    }

    Write-Output '================================================================================='
    $MicrosoftDynamicsERPMicroservicesAppObjectId = Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesAppId
    Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesCDSAppId | Out-Null
    $aibuilderAuthorizationServiceObjectId = Create-ADServicePrincipal -AppId $AIBuilderAuthorizationServiceAppId
    Write-Output ('=================================================================================')

    $clientAppSPN = Get-AzureADServicePrincipal -Filter ("DisplayName eq '" + $ClientAppName + "'")
    if (-not ($clientAppSPN)) {
        $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        if (-not $keyVaultPrincipal)
        {
            New-AzureADServicePrincipal -AppId $KeyVaultServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Key Vault principal to AAD"
            $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        }
        $keyVaultAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $keyVaultAccess.ResourceAppId = $keyVaultPrincipal.AppId
        $keyVaultAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $keyVaultPrincipal.Oauth2Permissions.Id, "Scope")

        $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        if (-not $graphPrincipal)
        {
            New-AzureADServicePrincipal -AppId $GraphServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Graph principal to AAD"
            $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        }
        $userRead = $graphPrincipal.Oauth2Permissions | Where-Object { $_.Type -eq "User" -and $_.Value -eq "User.Read" }
        $graphAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $graphAccess.ResourceAppId = $graphPrincipal.AppId
        $graphAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $userRead.Id, "Scope")

        $clientApp = New-AzureADApplication -DisplayName $ClientAppName -RequiredResourceAccess @($keyVaultAccess, $graphAccess)
        $clientAppSPN = New-AzureADServicePrincipal -AppId $clientApp.AppId -Tags @($ClientAppName)
        $clientAppId = $clientApp.AppId
        Write-Output ('Created App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
    else {
        $clientApp = Get-AzureADApplication -Filter ("DisplayName eq '" + $ClientAppName + "'")
        $clientAppId = $clientApp.AppId
        Write-Output ('Found App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
            
    $clientAppSecretCredential = New-AzureADApplicationPasswordCredential -ObjectId $clientApp.ObjectId -CustomKeyIdentifier "ClientAppAccessKey" -EndDate (get-date).AddYears($DefaultSecretExpiryInYear)
    $ClientAppSecret = $clientAppSecretCredential.Value
    $clientAppSpId = $clientAppSPN.ObjectId

    Write-Output ('Generated application secret: ' + $ClientAppSecret)
    Write-Output '================================================================================='

    $templateObject = ConvertFrom-Json $azureTemplate -AsHashtable
    $templateObject.{$schema} = "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#"
    Write-Output 'Provisioning Azure resources. This may take a few minutes.'
    try {
        $deployment = New-AzResourceGroupDeployment -ResourceGroupName $FullResourceGroupName -TemplateObject $templateObject -aibuilderAppObjectId $aibuilderAuthorizationServiceObjectId -clientAppId $clientAppId -clientAppSecret $ClientAppSecret -clientAppSpObjectId  $clientAppSpId -microserviceSpObjectId $MicrosoftDynamicsERPMicroservicesAppObjectId -userSpObjectId $user.ObjectId -Force -ErrorAction Stop
    }
    catch {
        $ErrorMessage = $_.Exception.Message
        if ($ErrorMessage.Contains("not allowed to be updated"))
        {
            Write-Error ($ErrorMessage)
            Write-Warning "Some items in the existing resource group $FullResourceGroupName could not be updated. To resolve the issue, remove the existing resource group $FullResourceGroupName and run the script again."
        }
        else {
            throw
        }

    }
    if ($deployment.ProvisioningState -eq 'Succeeded') {
        Write-Output "Successfully deployed the following resources to Azure:"
        Write-Output ("  Key Vault:                         " + $deployment.Outputs.keyVaultName.Value)
        Write-Output ("  Storage Account:                   " + $deployment.Outputs.storageAccountName.Value)
        
        $keyVault = Get-AzKeyVault -VaultName $deployment.Outputs.keyVaultName.Value
        $tenantId = (Get-AzContext).Tenant.Id

        Write-Output "Values for LCS Data Lake Add-In:"
        Write-Output ("  Tenant ID:                         " + $tenantId)
        Write-Output ("  DNS Name:                          " + $keyVault.VaultUri)
        Write-Output "  Storage account secret name:       storage-account-name"
        Write-Output "  Application ID secret name:        app-id"
        Write-Output "  Application Secret secret name:    app-secret"
        Write-Warning "Copy this information for the LCS Add-in for easy access. Azure Cloud Shell will eventually time out and close."

        Write-Output '================================================================================='
        Write-Output "Values for System parameters > Data connections:"
        Write-Output ("  Application ID:                    " + $clientAppId)
        Write-Output ("  Application Secret:                " + $ClientAppSecret)
        Write-Output ("  DNS name:                          " + $keyVault.VaultUri)
        Write-Output "  Secret name:                       storage-account-connection-string"
        Write-Warning "Copy this information for the System parameters for easy access. Azure Cloud Shell will eventually time out and close."
    }
    else {
        Write-Output ("Provisioning Azure resources failed with the following state: " + $deployment.ProvisioningState)
        Write-Output ("Some of the resources may have been created in resource group: " + $FullResourceGroupName)
    }
}

function Assert-ScriptSetup {
    if ($PSVersionTable.PSEdition -ne 'Core' -or -not $env:ACC_TID) { 
        throw "This script needs to be uploaded and run from Azure Cloud Shell (PowerShell)." 
    }
    
    if ((Get-AzContext) -eq $null -and (Connect-AzAccount) -eq $null) {
        throw 'Unable to connect to Azure account.'
    }
}

function Set-AzureSubscription {
    $azSubscription = $null
    while (-not ($azSubscription)) {
        $subscriptionId = (Read-Host -Prompt "Enter the Azure Subscription ID: (leave blank for default)")
        if ([string]::IsNullOrWhitespace($subscriptionId)){
            break
        }
        elseif (-not [guid]::TryParse($subscriptionId, $([ref][guid]::Empty))) {
                Write-Warning "Azure Subscription ID must be a valid GUID."
                continue
        }

        $azSubscription = Select-AzSubscription -SubscriptionId $subscriptionId
    }
}

function Create-ADServicePrincipal {
    param (
        [string] $AppId
    )

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $AppId | Out-Null
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
        Write-Host ("Added AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }
    else {
        Write-Host ("Found AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }

    return $service.ObjectId
}

$azureTemplate = @"
{
    "contentVersion": "1.0.0.0",
    "parameters": {
      "aibuilderAppObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of the AI Builder application."
        }
      },
      "clientAppId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the application ID of client application."
        }
      },
      "clientAppSecret": {
        "type": "String",
        "metadata": {
          "description": "Specifies the Azure App ID client secret to in azure key vault."
        }
      },
      "clientAppSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of a client application service principal."
        }
      },
      "userSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of tenant admin service principal."
        }
      },
      "microserviceSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of Microsoft Dynamics ERP Microservices service principal."
        }
      },
      "storageAccountType": {
        "type": "string",
        "defaultValue": "Standard_LRS",
        "allowedValues": [
          "Standard_LRS",
          "Standard_GRS",
          "Standard_ZRS",
          "Premium_LRS"
        ],
        "metadata": {
          "description": "Storage Account type"
        }
      }
    },
    "variables": {
      "storageAccountApiVersion": "2019-06-01",
      "keyVaultApiVersion": "2018-02-14",
      "secretsPermissions": [
        "list",
        "get"
      ],
      "location": "[resourceGroup().location]",
      "storageAccountName": "[concat('store', uniquestring(resourceGroup().id))]",
      "keyVaultName": "[concat('keyvault', uniquestring(resourceGroup().id))]",
      "owner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '8e3af657-a8ff-443c-a75c-2fe8c4bcb635')]",
      "contributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b24988ac-6180-42a0-ab88-20f7382dd24c')]",
      "storageAccountContributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '17d1049b-9a84-46fb-8f53-869881c3d3ab')]",
      "storageBlobDataOwner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b7e6dc6d-f1e8-4753-8033-0f276bb0955b')]",
      "storageBlobDataReader": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '2a2b9908-6ea1-4ae2-8e65-a410df84e7d1')]"
    },
    "resources": [
      {
        "type": "Microsoft.Storage/storageAccounts",
        "apiVersion": "[variables('storageAccountApiVersion')]",
        "name": "[variables('storageAccountName')]",
        "location": "[variables('location')]",
        "sku": {
          "name": "[parameters('storageAccountType')]"
        },
        "kind": "StorageV2",
        "properties": {
          "accessTier": "Hot",
          "supportsHttpsTrafficOnly": true,
          "isHnsEnabled": true
        },
        "resources": [
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'1')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('owner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'2')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('contributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'3')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageAccountContributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'4')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataOwner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'5')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataReader')]",
              "principalId": "[parameters('aibuilderAppObjectId')]"
            }
          }
        ]
      },
      {
        "type": "Microsoft.KeyVault/vaults",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "name": "[variables('keyVaultName')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName'))]"
        ],
        "tags": {
        },
        "properties": {
          "enabledForDeployment": false,
          "enabledForTemplateDeployment": false,
          "enabledForDiskEncryption": false,
          "enableRbacAuthorization": false,
          "accessPolicies": [
            {
              "objectId": "[parameters('clientAppSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('microserviceSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('userSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            }
          ],
          "tenantId": "[subscription().tenantId]",
          "sku": {
            "name": "Standard",
            "family": "A"
          },
          "enableSoftDelete": false,
          "networkAcls": {
            "defaultAction": "Allow",
            "bypass": "AzureServices"
          }
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-id')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppId')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-secret')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppSecret')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-name')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[variables('storageAccountName')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-connection-string')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[concat('DefaultEndpointsProtocol=https;AccountName=', variables('storageAccountName'), ';AccountKey=', listKeys(resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName')), variables('storageAccountApiVersion')).keys[0].value, ';EndpointSuffix=core.windows.net')]"
        }
      }
    ],
    "outputs": {
      "storageAccountName": {
        "type": "string",
        "value": "[variables('storageAccountName')]"
      },
      "keyVaultName": {
        "type": "string",
        "value": "[variables('keyVaultName')]"
      }
    }
  }
"@

try {
  Start-Transcript -path (Join-Path $HOME Provision-FinInsights-Azure.log)
  New-FinanceDataLakeAzureResources
}
catch {
  Write-Error $_.Exception.Message

  if ($PSItem.Exception.StackTrace -ne $null)
  {
      Write-Warning $_.Exception.StackTrace
  }

  $inner = $_.Exception.InnerException
  while ($null -ne $inner) {
    Write-Output 'Inner Exception:'
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $inner.InnerException
  }
}
finally {
  Stop-Transcript
}

```
---



## <a name="configure-the-data-lake"></a><span data-ttu-id="2f6c3-303">Veri gölünü yapılandırma</span><span class="sxs-lookup"><span data-stu-id="2f6c3-303">Configure the data lake</span></span>

<span data-ttu-id="2f6c3-304">LCS'yi kullanarak Azure Data Lake eklentisini ortama eklemek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-304">Follow these steps to use LCS to add the Azure Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="2f6c3-305">LCS'de oturum açın ve sonra sayfanın sağ tarafındaki ortam adının altında **Tüm Ayrıntılar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-305">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="2f6c3-306">**Ortam eklentileri** bölümünde, **Yeni bir eklenti yükleyin**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-306">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="2f6c3-307">**Data Lake'e dışarı aktar** eklentisini seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-307">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="2f6c3-308">Aşağıdaki değerleri girin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-308">Enter the following values.</span></span>

    | <span data-ttu-id="2f6c3-309">Değer</span><span class="sxs-lookup"><span data-stu-id="2f6c3-309">Value</span></span>                                                              | <span data-ttu-id="2f6c3-310">Tanım</span><span class="sxs-lookup"><span data-stu-id="2f6c3-310">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="2f6c3-311">Key Vault'un bulunduğu Azure Aboneliğinin Kiracı Kimliği</span><span class="sxs-lookup"><span data-stu-id="2f6c3-311">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="2f6c3-312">Depolama hesabı, uygulamalar ve anahtar kasalarının bulunduğu kiracının kimliğidir.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-312">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="2f6c3-313">Bu değeri bulmak için [Azure portalı](https://portal.azure.com) açın , **Azure Active Directory** öğesine gidin ve **Kiracı Kimliği** değerini kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-313">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="2f6c3-314">Key Vault'unuz için DNS adı belirtin</span><span class="sxs-lookup"><span data-stu-id="2f6c3-314">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="2f6c3-315">Anahtar kasasının DNS adı (ör. `https://customkeyvault.vault.azure.net/`).</span><span class="sxs-lookup"><span data-stu-id="2f6c3-315">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> <span data-ttu-id="2f6c3-316">(Bu değer, varlık deposunda kullanılan DNS adıyla eşleşir.)</span><span class="sxs-lookup"><span data-stu-id="2f6c3-316">(This value matches the DNS name that is used in the entity store.)</span></span> |
    | <span data-ttu-id="2f6c3-317">Depolama hesabının adını içeren gizli anahtarı girin</span><span class="sxs-lookup"><span data-stu-id="2f6c3-317">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="2f6c3-318">**storage-account-name**</span><span class="sxs-lookup"><span data-stu-id="2f6c3-318">**storage-account-name**</span></span> |
    | <span data-ttu-id="2f6c3-319">Data Lake'e erişmek için kullanılacak Uygulama Kimliği için Gizli Anahtar Adı</span><span class="sxs-lookup"><span data-stu-id="2f6c3-319">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="2f6c3-320">**app-id**</span><span class="sxs-lookup"><span data-stu-id="2f6c3-320">**app-id**</span></span> |
    | <span data-ttu-id="2f6c3-321">Uygulama Kimliği ile kullanılacak gizli anahtar adı</span><span class="sxs-lookup"><span data-stu-id="2f6c3-321">Secret name to be used with App ID</span></span>                                 | <span data-ttu-id="2f6c3-322">**app-secret**</span><span class="sxs-lookup"><span data-stu-id="2f6c3-322">**app-secret**</span></span> |

5. <span data-ttu-id="2f6c3-323">Koşulları kabul edin ve **Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-323">Agree to the terms, and select **Install**.</span></span>

<span data-ttu-id="2f6c3-324">Eklenti birkaç dakika içinde yüklenir.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-324">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-ai-builder"></a><span data-ttu-id="2f6c3-325">AI Builder'ı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="2f6c3-325">Configure AI Builder</span></span>

1. <span data-ttu-id="2f6c3-326">LCS'de oturum açın ve **Ortam ayrıntıları** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-326">Sign in to LCS, and open the **Environment details** page.</span></span>
2. <span data-ttu-id="2f6c3-327">**Ortam eklentileri** bölümüne kaydırın.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-327">Scroll to the **Environment add-ins** section.</span></span> <span data-ttu-id="2f6c3-328">Bu ortamda zaten yüklü olan eklentileri görmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-328">You should see the add-ins that are already installed in this environment.</span></span> <span data-ttu-id="2f6c3-329">Bunların arasında **Data Lake'e dışarı aktar** eklentisi bulunmuyorsa bu eklentiyi yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-329">If the **Export to Data Lake** add-in isn't among them, configure this add-in.</span></span>
3. <span data-ttu-id="2f6c3-330">**İçgörü edinme** eklentisini seçin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-330">Select the **Get insights** add-in.</span></span>
4. <span data-ttu-id="2f6c3-331">**İçgörü edinme** eklenti ayrıntıları sayfasında aşağıdaki değerleri girin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-331">On the **Get insights** add-in details page, enter the following values.</span></span>

    | <span data-ttu-id="2f6c3-332">Değer</span><span class="sxs-lookup"><span data-stu-id="2f6c3-332">Value</span></span>                                                    | <span data-ttu-id="2f6c3-333">Tanım</span><span class="sxs-lookup"><span data-stu-id="2f6c3-333">Description</span></span> |
    |----------------------------------------------------------|-------------|
    | <span data-ttu-id="2f6c3-334">CDS Kuruluş URL'si</span><span class="sxs-lookup"><span data-stu-id="2f6c3-334">CDS Organization URL</span></span>                                     | <span data-ttu-id="2f6c3-335">Yukarıdan kopyalanan Dataverse kuruluş URL'si.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-335">The Dataverse organization URL copied from above.</span></span> |
    | <span data-ttu-id="2f6c3-336">CDS Kuruluş Kimliği</span><span class="sxs-lookup"><span data-stu-id="2f6c3-336">CDS Org ID</span></span>                                               | <span data-ttu-id="2f6c3-337">Yukarıdan kopyalanan Dataverse kuruluş kimliği.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-337">The Dataverse organization ID copied from above.</span></span> |
5. <span data-ttu-id="2f6c3-338">**Bu, Kiracı için varsayılan CDS ortamı mı**'nı etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-338">Enable **Is this the default environment for you Tenant**.</span></span>
    
## <a name="configure-the-entity-store"></a><span data-ttu-id="2f6c3-339">Varlık deposunu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="2f6c3-339">Configure the entity store</span></span>

<span data-ttu-id="2f6c3-340">Finance ortamınızda varlık deposunu ayarlamak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-340">Follow these steps to set up the entity store in your Finance environment.</span></span>

1. <span data-ttu-id="2f6c3-341">**Sistem Yönetimi \> Kurulum \> Sistem parametreleri \> Veri bağlantıları** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-341">Go to **System administration \> Setup \> System parameters \> Data connections**.</span></span>
2. <span data-ttu-id="2f6c3-342">Aşağıdaki anahtar kasası alanlarını ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="2f6c3-342">Set the following key vault fields:</span></span>

    - <span data-ttu-id="2f6c3-343">**Uygulama (istemci) kimliği**: Daha önce oluşturduğunuz uygulama istemcisi kimliğini girin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-343">**Application (client) ID** – Enter the application client ID that you created earlier.</span></span>
    - <span data-ttu-id="2f6c3-344">**Uygulama Gizli Anahtarı**: Daha önce oluşturduğunuz uygulama için kaydettiğiniz gizli anahtarı girin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-344">**Application Secret** – Enter the secret that you saved for the application that you created earlier.</span></span>
    - <span data-ttu-id="2f6c3-345">**DNS adı**: Daha önce oluşturduğunuz uygulamanın uygulama ayrıntıları sayfasında Etki Alanı Adı Sistemi (DNS) adını bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-345">**DNS name** – You can find the Domain Name System (DNS) name on the application details page for the application that you created earlier.</span></span>
    - <span data-ttu-id="2f6c3-346">**Gizli anahtar adı**: **storage-account-connection-string** dizesini girin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-346">**Secret name** – Enter **storage-account-connection-string**.</span></span>
3. <span data-ttu-id="2f6c3-347">**Data Lake tümleştirmesi**'ni etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-347">Enable **Enable Data Lake integration**.</span></span>
4. <span data-ttu-id="2f6c3-348">**Azure Key Vault'u test et**'i seçin ve hata olmadığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-348">Select **Test Azure Key Vault** and verify there are no errors.</span></span>
5. <span data-ttu-id="2f6c3-349">**Azure depolamayı test et**'i seçin ve hata olmadığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-349">Select **Test Azure storage** and verify there are no errors.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="2f6c3-350">Geri bildirim ve destek</span><span class="sxs-lookup"><span data-stu-id="2f6c3-350">Feedback and support</span></span>

<span data-ttu-id="2f6c3-351">Geri bildirim sağlamak veya destek almak istiyorsanız lütfen [Müşteri ödeme içgörüleri (Önizleme)](mailto:fiap@microsoft.com) ekibine e-posta gönderin.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-351">Please send an email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in providing feedback or need support.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="2f6c3-352">Gizlilik bildirimi</span><span class="sxs-lookup"><span data-stu-id="2f6c3-352">Privacy notice</span></span>

<span data-ttu-id="2f6c3-353">Önizlemeler (1), Dynamics 365 Finance and Operations hizmetinden daha az gizlilik ve güvenlik önlemleri kullanabilir, (2) bu hizmet için hizmet düzeyi sözleşmesine (SLA) dahil edilmez, (3) kişisel verileri veya yasal ya da mevzuat uyumluluğu gereksinimlerine tabi olan diğer verileri işlemek için kullanılmamalıdır ve (4) sınırlı desteğe sahiptir.</span><span class="sxs-lookup"><span data-stu-id="2f6c3-353">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
