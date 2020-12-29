---
title: Mali İçgörüler için Yapılandırma (önizleme)
description: Bu konuda, sisteminizin Mali içgörülerde sunulan özellikleri kullanabilmesini sağlayacak yapılandırma adımları açıklanmaktadır.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 38cdeb9110691e594b4b90fc5bc79e369c9f4707
ms.sourcegitcommit: 1cfd6e0c808341b0f5bafbde7d04b0255b27352f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/02/2020
ms.locfileid: "4664102"
---
# <a name="configuration-for-finance-insights-preview"></a><span data-ttu-id="49899-103">Mali içgörüler için yapılandırma (önizleme)</span><span class="sxs-lookup"><span data-stu-id="49899-103">Configuration for Finance insights (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="49899-104">Mali içgörüler, kuruluşunuza güçlü tahmin araçları sunmak için Microsoft Dynamics 365 Finance işlevlerini Common Data Service, Azure ve AI Builder işlevleriyle bir araya getirir.</span><span class="sxs-lookup"><span data-stu-id="49899-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Common Data Service, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="49899-105">Bu konuda, sisteminizin Mali içgörülerde sunulan özellikleri kullanabilmesini sağlayacak yapılandırma adımları açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="49899-105">This topic explains the configuration steps that will enable your system to use the capabilities that are available in Finance insights.</span></span>

## <a name="deploy-dynamics-365-finance"></a><span data-ttu-id="49899-106">Dynamics 365 Finance dağıtımı</span><span class="sxs-lookup"><span data-stu-id="49899-106">Deploy Dynamics 365 Finance</span></span>

<span data-ttu-id="49899-107">Şu adımları izleyerek ortamları dağıtın.</span><span class="sxs-lookup"><span data-stu-id="49899-107">Deploy the environments by following these steps.</span></span>

1. <span data-ttu-id="49899-108">Microsoft Dynamics Lifecycle Services (LCS) portalında, bir Dynamics 365 Finance ortamı oluşturun veya güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="49899-108">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Dynamics 365 Finance environment.</span></span> <span data-ttu-id="49899-109">Ortam, sürüm 10.0.11/Platform update 35 veya daha sonraki bir uygulama sürümü gerektirir.</span><span class="sxs-lookup"><span data-stu-id="49899-109">The environment requires app version 10.0.11/Platform update 35 or later.</span></span>
2. <span data-ttu-id="49899-110">Ortam, Korumalı Alan içinde yüksek kullanılabilirlik (HA) ortamı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="49899-110">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="49899-111">(Bu ortam türü aynı zamanda Katman 2 ortamı olarak da bilinir.) Daha fazla bilgi için bkz. [Ortam planlama](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="49899-111">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="49899-112">Contoso tanıtım verilerini kullanıyorsanız Müşteri ödeme tahminleri, Nakit akışı tahminleri ve Bütçe tahminleri özelliklerini kullanmak için ek örnek verilere ihtiyaç duyarsınız.</span><span class="sxs-lookup"><span data-stu-id="49899-112">If you're using Contoso demo data, you will require additional sample data to use the Customer payment predictions, Cash flow forecasts, and Budget forecasts features.</span></span> 

## <a name="configure-common-data-service"></a><span data-ttu-id="49899-113">Common Data Service'ı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="49899-113">Configure Common Data Service</span></span>

<span data-ttu-id="49899-114">Sonraki manuel yapılandırma adımlarını tamamlayabilir veya sağlanan Windows PowerShell betiğini kullanarak yapılandırma işlemini hızlandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="49899-114">You can complete the manual configuration steps that follow, or you can speed up the configuration process by using the Windows PowerShell script that is provided.</span></span> <span data-ttu-id="49899-115">PowerShell betik dosyasının çalışması bittiğinde size Mali içgörüleri yapılandırmak için kullanabileceğiniz değerler sunar.</span><span class="sxs-lookup"><span data-stu-id="49899-115">When the PowerShell script has finished running, it will give you values to use to configure Finance insights.</span></span> 

> [!NOTE]
> <span data-ttu-id="49899-116">Betik dosyasını çalıştırmak için bilgisayarınızda PowerShell'i açın.</span><span class="sxs-lookup"><span data-stu-id="49899-116">Open PowerShell on your PC to run the script.</span></span> <span data-ttu-id="49899-117">PowerShell sürüm 5 gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="49899-117">You may need PowerShell version 5.</span></span> <span data-ttu-id="49899-118">Microsoft Azure CLI "Try it" seçeneği çalışmayabilir.</span><span class="sxs-lookup"><span data-stu-id="49899-118">The Microsoft Azure CLI "Try it" option may not work.</span></span>

# <a name="manual-configuration-steps"></a>[<span data-ttu-id="49899-119">El ile yapılandırma adımları</span><span class="sxs-lookup"><span data-stu-id="49899-119">Manual configuration steps</span></span>](#tab/configuration-steps)

1. <span data-ttu-id="49899-120">[Power Platform yönetim merkezini](https://admin.powerplatform.microsoft.com/)açın ve aynı Active Directory kiracısında yeni bir Common Data Service ortamı oluşturmak için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="49899-120">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), and follow these steps to create a new Common Data Service environment in the same Active Directory tenant:</span></span>

    1. <span data-ttu-id="49899-121">**Ortamlar** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="49899-121">Open the **Environments** page.</span></span>

        <span data-ttu-id="49899-122">[![Ortamlar sayfası](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span><span class="sxs-lookup"><span data-stu-id="49899-122">[![Environments page](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span></span>

    2. <span data-ttu-id="49899-123">**Yeni ortam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-123">Select **New environment**.</span></span>
    3. <span data-ttu-id="49899-124">**Tür** alanında **Korumalı alan**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-124">In the **Type** field, select **Sandbox**.</span></span>
    4. <span data-ttu-id="49899-125">**Veritabanı Oluştur** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="49899-125">Set the **Create Database** option to **Yes**.</span></span>
    5. <span data-ttu-id="49899-126">**Sonraki**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-126">Select **Next**.</span></span>
    6. <span data-ttu-id="49899-127">Kuruluşunuz için dili ve para birimini seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-127">Select the language and currency for your organization.</span></span>
    7. <span data-ttu-id="49899-128">Diğer alanlar için varsayılan değerleri kabul edin.</span><span class="sxs-lookup"><span data-stu-id="49899-128">Accept the default values for the other fields.</span></span>
    8. <span data-ttu-id="49899-129">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-129">Select **Save**.</span></span>
    9. <span data-ttu-id="49899-130">**Ortamlar** sayfasını yenileyin.</span><span class="sxs-lookup"><span data-stu-id="49899-130">Refresh the **Environments** page.</span></span>
    10. <span data-ttu-id="49899-131">**Durum** alanının değeri **Hazır** olarak güncelleştirilene kadar bekleyin.</span><span class="sxs-lookup"><span data-stu-id="49899-131">Wait until the value of the **State** field is updated to **Ready**.</span></span>
    11. <span data-ttu-id="49899-132">Common Data Service kuruluş kodunu not edin.</span><span class="sxs-lookup"><span data-stu-id="49899-132">Make a note of the Common Data Service organization ID.</span></span>
    12. <span data-ttu-id="49899-133">Ortamı seçin ve sonra **Ayarlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-133">Select the environment, and then select **Settings**.</span></span>
    13. <span data-ttu-id="49899-134">**Kaynaklar \> Tüm Eski Ayarlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-134">Select **Resources \> All Legacy Settings**.</span></span>
    14. <span data-ttu-id="49899-135">Üst gezinti çubuğunda, **Ayarlar**'ı seçin ve ardından **Özelleştirmeler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-135">On the top navigation bar, select **Settings**, and then select **Customizations**.</span></span>
    15. <span data-ttu-id="49899-136">**Geliştirici Kaynakları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-136">Select **Developer Resources**.</span></span>
    16. <span data-ttu-id="49899-137">**Kurulum Referansı Bilgi Kodu** alanını, daha önce not ettiğiniz Common Data Service kuruluş kodu değeri olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="49899-137">Set the **Instance Reference Information ID** field to the Common Data Service organization ID value that you made a note of earlier.</span></span>
    17. <span data-ttu-id="49899-138">Tarayıcının adres çubuğunda Common Data Service kuruluşunun URL'sini not edin.</span><span class="sxs-lookup"><span data-stu-id="49899-138">In the browser's address bar, make a note of the URL for the Common Data Service organization.</span></span> <span data-ttu-id="49899-139">Örneğin, URL şu şekilde olabilir: `https://org42b2b3d3.crm.dynamics.com`.</span><span class="sxs-lookup"><span data-stu-id="49899-139">For example, the URL might be `https://org42b2b3d3.crm.dynamics.com`.</span></span>

2. <span data-ttu-id="49899-140">Nakit akışı tahminleri veya bütçe tahminleri özelliğini kullanmayı planlıyorsanız kuruluşunuzun ek açıklama sınırını en az 50 megabayt (MB) olarak güncelleştirmek için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="49899-140">If you plan to use the Cash flow forecasts or Budget forecasts feature, follow these steps to update the annotation limit for your organization to at least 50 megabytes (MB):</span></span>

    1. <span data-ttu-id="49899-141">[Power Apps portalını](https://make.powerapps.com) açın.</span><span class="sxs-lookup"><span data-stu-id="49899-141">Open the [Power Apps portal](https://make.powerapps.com).</span></span>
    2. <span data-ttu-id="49899-142">Yeni oluşturduğunuz ortamı seçin ve sonra **Gelişmiş ayarlar**'ı seçin .</span><span class="sxs-lookup"><span data-stu-id="49899-142">Select the environment that you just created, and then select **Advanced settings**.</span></span>
    3. <span data-ttu-id="49899-143">**Ayarlar \> E-posta Yapılandırması**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-143">Select **Settings \> Email Configuration**.</span></span>
    4. <span data-ttu-id="49899-144">**Maksimum dosya boyutu** alanının değerini **51.200** olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="49899-144">Change the value of the **Maximum file size** field to **51,200**.</span></span> <span data-ttu-id="49899-145">(Değer, kilobayt \[KB\] cinsinden ifade edilir.)</span><span class="sxs-lookup"><span data-stu-id="49899-145">(The value is expressed in kilobytes \[KB\].)</span></span>
    5. <span data-ttu-id="49899-146">Yaptığınız değişiklikleri kaydetmek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-146">Select **OK** to save your changes.</span></span>

# <a name="windows-powershell-configuration-script"></a>[<span data-ttu-id="49899-147">Windows PowerShell yapılandırma betik dosyası</span><span class="sxs-lookup"><span data-stu-id="49899-147">Windows PowerShell configuration script</span></span>](#tab/powershell-configuration-script)

```azurecli-interactive
Write-Output 'The following modules need to be present for execution of this script:'
Write-Output '  Microsoft.PowerApps.Administration.PowerShell'
Write-Output '  Microsoft.PowerApps.PowerShell'
Write-Output '  Microsoft.Xrm.Tooling.CrmConnector.PowerShell'

try {
    $moduleConsent = Read-Host 'Is it ok to install or update these modules as needed? (yes/no)'
    if ($moduleConsent -ne 'yes' -and $moduleConsent -ne 'y') {
        Write-Warning 'User declined to install required modules.'
        return
    }

    $module = 'Microsoft.PowerApps.Administration.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '2.0.61' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '2.0.61' -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    $module = 'Microsoft.PowerApps.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '1.0.9' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '1.0.9' -AllowClobber -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    $module = 'Microsoft.Xrm.Tooling.CrmConnector.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '3.3.0.892' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '3.3.0.892' -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    Write-Output '================================================================================='

    $useMfa = $false
    $useMfaPrompt = Read-Host "Does your organization require the use of multi-factor authentication? (yes/no)"
    if ($useMfaPrompt -eq 'yes' -or $useMfaPrompt -eq 'y') {
        $useMfa = $true
    }
    if(-not $useMfa) {
        $credential = Get-Credential -Message 'Power Apps Credential'
    }

    $orgFriendlyName = Read-Host "Enter the name of the CDS Organization to use or create: (blank for 'FinanceInsightsOrg')"
    if ($orgFriendlyName.Trim() -eq '') {
        $orgFriendlyName = 'FinanceInsightsOrg'
    }

    $isDefaultOrgPrompt = Read-Host ("Is '" + $orgFriendlyName + "' the default organization for your tenant? (yes/no)")
    if ($isDefaultOrgPrompt -eq 'yes' -or $isDefaultOrgPrompt -eq 'y') {
        $isDefaultOrg = $true
    }

    if ($credential) {
        Add-PowerAppsAccount -Username $credential.UserName -Password $credential.Password
    }
    else {
        Add-PowerAppsAccount
    }

    if ($isDefaultOrg) {
        $orgMatch = ('(default)')
        $environment = (Get-AdminPowerAppEnvironment | Where-Object { $_.IsDefault -eq $true })
    }
    else {
        $orgMatch = ('{0} (*)' -f $orgFriendlyName)
        $environment = (Get-AdminPowerAppEnvironment | Where-Object { ($_.IsDefault -eq $false -and ($_.DisplayName -eq $orgFriendlyName -or $_.DisplayName -like $orgMatch)) })
    }

    $getCrmOrgParams = @{ 'OnlineType' = 'Office365' }
    if ($credential) {
        $getCrmOrgParams.Credential = $credential
    }

    if ($null -eq $environment) {
        Write-Output '================================================================================='
        Write-Output 'PowerApps environment not found. A new one will be provisioned.'

        $invalid = 'invalid'

        $location = $invalid
        $cdsLocations = (Get-AdminPowerAppEnvironmentLocations | Select-Object LocationName).LocationName
        while (-not ($location -in $cdsLocations)) {
            $location = (Read-Host -Prompt "Enter the location in which to create the new PowerApps environment: ('help' to see values)")
            if ($location -eq 'help') {
                $cdsLocations
            }
        }

        $currency = $invalid
        $cdsCurrencies = (Get-AdminPowerAppCdsDatabaseCurrencies -Location $location | Select-Object CurrencyName).CurrencyName
        while ($currency -ne '' -and -not ($currency -in $cdsCurrencies)) {
            $currency = (Read-Host -Prompt "Enter the currency to use for the new PowerApps environment: ('help' to see values, blank for default)")
            if ($currency -eq 'help') {
                $cdsCurrencies
            }
        }

        $language = $invalid
        $cdsLanguages = (Get-AdminPowerAppCdsDatabaseLanguages -Location $location | Select-Object LanguageName, LanguageDisplayName)
        while ($language -ne '' -and -not ($language -in $cdsLanguages.LanguageName)) {
            $language = (Read-Host -Prompt "Enter the language name to use for the new PowerApps environment: ('help' to see values, blank for default)")
            if ($language -eq 'help') {
                $cdsLanguages | Format-Table -Property LanguageName, LanguageDisplayName
            }
        }

        Write-Output 'Provisioning PowerApps environment. This may take several minutes.'

        $sleep = 15

        $envParams = @{ 'DisplayName' = $orgFriendlyName; 'EnvironmentSku' = 'Sandbox'; 'ProvisionDatabase' = $true; 'Location' = $location; 'WaitUntilFinished' = $true }
        if ($language.Trim() -ne '') {
            $envParams.LanguageName = $language
        }
        if ($currency.Trim() -ne '') {
            $envParams.CurrencyName = $currency
        }
        $newEnvResult = New-AdminPowerAppEnvironment @envParams
        if (($null -eq $newEnvResult) -or ($newEnvResult.CommonDataServiceDatabaseProvisioningState -ne 'Succeeded')) {
            Write-Warning 'Failed to create to PowerApps environment'
            if ($null -ne $newEnvResult) {
                $newEnvResult
            }
        }
        else {
            $environment = $null
            $retryCount = 0
            while (($null -eq $environment) -and ($retryCount -lt 5)) {
                Start-Sleep -Seconds $sleep
                $environment = (Get-AdminPowerAppEnvironment | Where-Object { ($_.DisplayName -like $orgMatch) })
            }
            Write-Output ("Provisioned PowerApps environment with name: '" + $environment.DisplayName + "'")
        }

        Write-Output 'Waiting for CDS organization provisioning. This may take several minutes.'
        if (-not $credential) {
            $sleep = 120
            Write-Output 'You may be prompted for credentials multiple times while checking the status of the provisioning.'
        }

        while ($null -eq $crmOrg) {
            Start-Sleep -Seconds $sleep
            $crmOrg = (Get-CrmOrganizations @getCrmOrgParams) | Where-Object { $_.FriendlyName -eq $orgFriendlyName }
        }
    }
    else {
        $crmOrgs = Get-CrmOrganizations @getCrmOrgParams
        if ($UseDefaultOrganization -eq $true) {
            $crmOrg = $crmOrgs | Where-Object { $_.FriendlyName -match $orgMatch }
        }
        else {
            $crmOrg = $crmOrgs | Where-Object { $_.FriendlyName -eq $orgFriendlyName }
        }
    }

    Write-Output '================================================================================='
    Write-Output 'Values for PowerAI LCS Add-In:'
    Write-Output ("  CDS organization url:             " + $crmOrg.WebApplicationUrl)
    Write-Output ("  CDS organization ID:              " + $crmOrg.OrganizationId)
}
catch {
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $_.Exception.InnerException
    while ($null -ne $inner) {
        Write-Output 'Inner Exception:'
        Write-Error $_.Exception.Message
        Write-Warning $_.Exception.StackTrace
        $inner = $inner.InnerException
    }
}
```
---

## <a name="configure-the-azure-setup"></a><span data-ttu-id="49899-148">Azure kurulumunu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="49899-148">Configure the Azure setup</span></span>

### <a name="enter-the-common-data-service-directory-id-and-the-users-azure-ad-object-id"></a><span data-ttu-id="49899-149">Common Data Service dizin kodunu ve kullanıcının Azure AD nesne kodunu girin</span><span class="sxs-lookup"><span data-stu-id="49899-149">Enter the Common Data Service directory ID and the user's Azure AD object ID</span></span>

1. <span data-ttu-id="49899-150">Common Data Service dizin kodunu girin:</span><span class="sxs-lookup"><span data-stu-id="49899-150">Enter the Common Data Service directory ID:</span></span>

    1. <span data-ttu-id="49899-151">[Azure portalını](https://portal.azure.com) açın.</span><span class="sxs-lookup"><span data-stu-id="49899-151">Open the [Azure portal](https://portal.azure.com).</span></span>
    2. <span data-ttu-id="49899-152">Common Data Service ortamı oluşturmak için kullanılan kullanıcı kimliğini kullanarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="49899-152">Sign in by using the user ID that was used to create the Common Data Service environment.</span></span>
    3. <span data-ttu-id="49899-153">**Azure Active Directory** gidin.</span><span class="sxs-lookup"><span data-stu-id="49899-153">Go to **Azure Active Directory**.</span></span>
    4. <span data-ttu-id="49899-154">**Kiracı Kimliği** değerini kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="49899-154">Copy the **Tenant ID** value.</span></span>

2. <span data-ttu-id="49899-155">Kullanıcının Azure Active Directory (Azure AD) nesne kimliğini girin:</span><span class="sxs-lookup"><span data-stu-id="49899-155">Enter the user's Azure Active Directory (Azure AD) object ID:</span></span>

    1. <span data-ttu-id="49899-156">[Azure portalı](https://portal.azure.com) içinde **Kullanıcılar**'a gidin ve e-posta adresine göre kullanıcıyı arayın.</span><span class="sxs-lookup"><span data-stu-id="49899-156">In the [Azure portal](https://portal.azure.com), go to **Users**, and search for the user by email address.</span></span>
    2. <span data-ttu-id="49899-157">Kullanıcının adını seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-157">Select the user's name.</span></span>
    3. <span data-ttu-id="49899-158">**Nesne Kimliği** değerini kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="49899-158">Copy the **Object ID** value.</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="49899-159">Mali içgörüler Data Lake kaynaklarını ayarlamak için Azure Cloud Shell kullanma</span><span class="sxs-lookup"><span data-stu-id="49899-159">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="49899-160">Windows PowerShell betik dosyası kullanma</span><span class="sxs-lookup"><span data-stu-id="49899-160">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="49899-161">[Azure Data Lake'e aktarmayı yapılandırma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/configure-export-data-lake) konusunda açıklandığı gibi Azure kaynaklarını kolayca ayarlayabilmeniz için Windows PowerShell betik dosyası sağlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="49899-161">A Windows PowerShell script has been provided, so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/configure-export-data-lake).</span></span> <span data-ttu-id="49899-162">El ile kurulum yapmayı tercih ediyorsanız bu yordamı atlayın ve [El ile kurulum](#manual-setup) bölümündeki yordama devam edin.</span><span class="sxs-lookup"><span data-stu-id="49899-162">If you prefer to do manual setup, skip this procedure, and continue with the procedure in the [Manual setup](#manual-setup) section.</span></span>

> [!NOTE]
> <span data-ttu-id="49899-163">PowerShell betiğini çalıştırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="49899-163">Follow the steps below to run the PowerShell script.</span></span> <span data-ttu-id="49899-164">Azure CLI "Try it" seçeneği veya betiği bilgisayarınızda çalıştırmak işe yaramayabilir.</span><span class="sxs-lookup"><span data-stu-id="49899-164">The Azure CLI "Try it" option, or running the script on your PC may not work.</span></span>

<span data-ttu-id="49899-165">Windows PowerShell betik dosyasını kullanarak Azure yapılandırmayla ilgili bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="49899-165">Follow these steps to configure Azure by using the Windows PowerShell script.</span></span> <span data-ttu-id="49899-166">Azure kaynak grubu, Azure kaynakları ve bir Azure AD uygulaması oluşturma haklarınız olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="49899-166">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="49899-167">Gerekli izinler hakkında daha fazla bilgi için bkz. [Azure AD izinlerini denetleme](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="49899-167">For information about the required permissions, see [Check Azure AD permissions](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="49899-168">[Azure portalda](https://portal.azure.com) hedef Azure aboneliğinize gidin.</span><span class="sxs-lookup"><span data-stu-id="49899-168">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span> <span data-ttu-id="49899-169">**Arama** alanının sağında bulunan **Cloud Shell** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-169">Select the **Cloud Shell** button to the right of the **Search** field.</span></span>
2. <span data-ttu-id="49899-170">**PowerShell**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-170">Select **PowerShell**.</span></span>
3. <span data-ttu-id="49899-171">İstenirse, depolama alanı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="49899-171">Create storage, if you're prompted to do so.</span></span> <span data-ttu-id="49899-172">Ardından, Windows PowerShell betiğini oturuma yükleyin.</span><span class="sxs-lookup"><span data-stu-id="49899-172">Then upload the Windows PowerShell script to the session.</span></span>
4. <span data-ttu-id="49899-173">Betik dosyasını çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="49899-173">Run the script.</span></span>
5. <span data-ttu-id="49899-174">Betik dosyasını çalıştırmak için istemleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="49899-174">Follow the prompts to run the script.</span></span>
6. <span data-ttu-id="49899-175">LCS'ye **Data Lake'e dışarı aktar** eklentisini yüklemek için betik dosyası çıktısındaki bilgileri kullanın.</span><span class="sxs-lookup"><span data-stu-id="49899-175">Use the information from the script output to install the **Export to Data Lake** add-in in LCS.</span></span>
7. <span data-ttu-id="49899-176">Finance'teki **Veri bağlantıları** sayfasında varlık deposunu etkinleştirmek için betik dosyası çıktısındaki bilgileri kullanın (**Sistem yönetimi \> Sistem parametreleri \> Veri bağlantıları**).</span><span class="sxs-lookup"><span data-stu-id="49899-176">Use the information from the script output to enable the entity store on the **Data connections** page in Finance (**System administration \> System parameters \> Data connections**).</span></span>

### <a name="manual-setup"></a><span data-ttu-id="49899-177">El ile kurulum</span><span class="sxs-lookup"><span data-stu-id="49899-177">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="49899-178">Azure AD kiracısına uygulama ekleme</span><span class="sxs-lookup"><span data-stu-id="49899-178">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="49899-179">[Azure portalda](https://portal.azure.com) **Azure Active Directory**'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="49899-179">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="49899-180">**Yönet \> Kurumsal uygulamalar** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-180">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="49899-181">Uygulama kimliğine göre aşağıdaki uygulamaları arayın.</span><span class="sxs-lookup"><span data-stu-id="49899-181">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="49899-182">Uygulama</span><span class="sxs-lookup"><span data-stu-id="49899-182">Application</span></span>                              | <span data-ttu-id="49899-183">Uygulama kodu</span><span class="sxs-lookup"><span data-stu-id="49899-183">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="49899-184">Microsoft Dynamics ERP Mikro Hizmetleri</span><span class="sxs-lookup"><span data-stu-id="49899-184">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="49899-185">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="49899-185">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="49899-186">Microsoft Dynamics ERP Mikro Hizmetleri CDS</span><span class="sxs-lookup"><span data-stu-id="49899-186">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="49899-187">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="49899-187">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="49899-188">AI Builder Yetkilendirme Hizmeti</span><span class="sxs-lookup"><span data-stu-id="49899-188">AI Builder Authorization Service</span></span>         | <span data-ttu-id="49899-189">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="49899-189">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="49899-190">Önceki uygulamalardan hiçbirini bulamazsanız aşağıdaki adımları deneyin.</span><span class="sxs-lookup"><span data-stu-id="49899-190">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="49899-191">Yerel makinenizde, **Başlat** menüsünü seçin ve **powershell**'i arayın.</span><span class="sxs-lookup"><span data-stu-id="49899-191">On your local machine, select the **Start** menu, and search for **powershell**.</span></span>
2. <span data-ttu-id="49899-192">**Windows PowerShell**'i seçin ve basılı tutun (veya sağ tıklayın) ve sonra **Yönetici olarak çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-192">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="49899-193">**AzureAD** modülünü yüklemek için aşağıdaki komutu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="49899-193">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="49899-194">Devam etmek için NuGet sağlayıcısı gerekiyorsa yüklemek için **Y**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-194">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="49899-195">"Güvenilmeyen depo" iletisi görüntülenirse devam etmek için **Y**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-195">If an "Untrusted repository" message appears, select **Y** to continue.</span></span>
6. <span data-ttu-id="49899-196">Eklenmesi gereken her uygulama için uygulamayı Azure AD'ye eklemek üzere aşağıdaki komutları çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="49899-196">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="49899-197">İstendiğinde, Azure AD yöneticisi olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="49899-197">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="49899-198">Azure kaynakları oluşturma</span><span class="sxs-lookup"><span data-stu-id="49899-198">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="49899-199">Common Data Service ortamıyla aynı Azure AD kurulumunda aşağıdaki kaynakları oluşturduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="49899-199">Make sure that you create the following resources in the same Azure AD instance as the Common Data Service environment.</span></span> <span data-ttu-id="49899-200">Farklı bir Azure AD kurulumundan kaynak kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="49899-200">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="49899-201">Yeni depolama hesabı oluşturma:</span><span class="sxs-lookup"><span data-stu-id="49899-201">Create a new storage account:</span></span>

    1. <span data-ttu-id="49899-202">[Azure portalında](https://portal.azure.com) bir depolama hesabı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="49899-202">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="49899-203">**Depolama hesabı oluştur** iletişim kutusunda, aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="49899-203">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="49899-204">**Konum**: Ortamınızın bulunduğu veri merkezini seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-204">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="49899-205">**Performans**: **Standart** seçeneğini belirlemenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="49899-205">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="49899-206">**Hesap türü**: **StorageV2**'yi seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="49899-206">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="49899-207">**Gelişmiş seçenekler** iletişim kutusunda **Data Lake Storage 2. Nesil** seçeneği için **Hiyerarşik ad alanları** bölümünde **Etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-207">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="49899-208">Bu özelliği devre dışı bırakırsanız Power BI veri akışları gibi hizmetleri kullanarak, Finance and Operations uygulamalarının yazdığı verileri kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="49899-208">If you disable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="49899-209">**İncele ve oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-209">Select **Review and create**.</span></span> <span data-ttu-id="49899-210">Dağıtım tamamlandığında, yeni kaynak Azure portalında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="49899-210">When the deployment is completed, the new resource will be shown in the Azure portal.</span></span>
    5. <span data-ttu-id="49899-211">Oluşturduğunuz depolama hesabına gidin.</span><span class="sxs-lookup"><span data-stu-id="49899-211">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="49899-212">Sol menüde **Erişim anahtarları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-212">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="49899-213">**Key1** veya **Key2** için bağlantı dizesini kopyalayıp kaydedin.</span><span class="sxs-lookup"><span data-stu-id="49899-213">Copy and save the connection string for either **Key1** or **Key2**.</span></span>
    8. <span data-ttu-id="49899-214">Depolama hesabı adını kopyalayın ve kaydedin.</span><span class="sxs-lookup"><span data-stu-id="49899-214">Copy and save the storage account name.</span></span>

2. <span data-ttu-id="49899-215">Yeni bir anahtar kasası oluşturma:</span><span class="sxs-lookup"><span data-stu-id="49899-215">Create a new key vault:</span></span>

    1. <span data-ttu-id="49899-216">[Azure portalında](https://portal.azure.com) bir anahtar kasası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="49899-216">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="49899-217">**Anahtar kasası oluştur** iletişim kutusundaki **Konum** alanında ortamınızın bulunduğu veri merkezini seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-217">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="49899-218">Anahtar kasası oluşturulduktan sonra, kasayı listeden seçin ve ardından **Gizli anahtarlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-218">After key vault is created, select it in the list, and then select **Secrets**.</span></span>
    4. <span data-ttu-id="49899-219">**Oluştur/İçe aktar** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="49899-219">Select **Generate/Import**.</span></span>
    5. <span data-ttu-id="49899-220">**Gizli anahtar oluştur** iletişim kutusunda **Karşıya yükleme seçenekleri** alanında, **El ile** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="49899-220">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
    6. <span data-ttu-id="49899-221">Gizli anahtar için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="49899-221">Enter a name for the secret.</span></span> <span data-ttu-id="49899-222">Daha sonra sağlamanız gerekeceği için bu adı not edin.</span><span class="sxs-lookup"><span data-stu-id="49899-222">Make a note of the name, because you will have to provide it later.</span></span>
    7. <span data-ttu-id="49899-223">**Değer** alanında, önceki yordamda depolama hesabından elde ettiğiniz bağlantı dizesini girin.</span><span class="sxs-lookup"><span data-stu-id="49899-223">In the **Value** field, enter the connection string that you obtained from the storage account in the previous procedure.</span></span>
    8. <span data-ttu-id="49899-224">**Etkin**'i ve ardından **Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-224">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="49899-225">Gizli anahtar oluşturulur ve Key Vault'a eklenir.</span><span class="sxs-lookup"><span data-stu-id="49899-225">The secret is created and added to Key Vault.</span></span>
    9. <span data-ttu-id="49899-226">**Key Vault'a Genel Bakış**'a gidin ve DNS adını not edin.</span><span class="sxs-lookup"><span data-stu-id="49899-226">Go to the **Key Vault Overview**, and make a note of the DNS name.</span></span>

3. <span data-ttu-id="49899-227">Bir Azure AD uygulaması oluşturma ve kaydetme:</span><span class="sxs-lookup"><span data-stu-id="49899-227">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="49899-228">[Azure portalında](https://portal.azure.com) **Azure Active Directory**'ye gidin ve ardından **Uygulama kayıtları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-228">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="49899-229">**Yeni uygulama kaydı**'nı seçin ve aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="49899-229">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="49899-230">**Ad**: Uygulamanın adını girin.</span><span class="sxs-lookup"><span data-stu-id="49899-230">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="49899-231">**Uygulama türü**: **Web API'si** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="49899-231">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="49899-232">**Yeniden yönlendirme URI'si kurulumu**: Dynamics 365 kurulumunuzun URL'sini girin (ör. `https://yourdynamicsinstance.dynamics.com/auth`).</span><span class="sxs-lookup"><span data-stu-id="49899-232">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as, `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="49899-233">Yeni oluşturduğunuz uygulamaya gidin ve **Uygulama (istemci) kimliği** değerini kopyalayın ve kaydedin.</span><span class="sxs-lookup"><span data-stu-id="49899-233">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="49899-234">Anahtar kasasını ayarlarken bu değeri sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="49899-234">You will have to provide this value later, when you set up the key vault.</span></span>
    4. <span data-ttu-id="49899-235">**API izinleri**'ne gidin ve şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="49899-235">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="49899-236">**İzin ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-236">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="49899-237">**Azure Key Vault**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-237">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="49899-238">Temsilci izinleri seçtikten sonra **kullanıcı\_kimliğe bürünmey**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-238">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="49899-239">**İzin ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-239">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="49899-240">Uygulama menüsünde, **Sertifikalar ve gizli anahtarlar**'ı seçin ve ardından Key Vault gizli anahtarlarını oluşturmak için bu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="49899-240">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="49899-241">**Yeni gizli anahtar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-241">Select **New client secret**.</span></span>
        2. <span data-ttu-id="49899-242">**Anahtar Açıklaması** alanına bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="49899-242">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="49899-243">Bir süre seçin ve ardından **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-243">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="49899-244">**Değer** alanında gizli anahtar oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="49899-244">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="49899-245">Gizli anahtar değerini kopyalayın ve kaydedin.</span><span class="sxs-lookup"><span data-stu-id="49899-245">Copy and save the secret value.</span></span>

4. <span data-ttu-id="49899-246">Key Vault gizli anahtarları oluşturma:</span><span class="sxs-lookup"><span data-stu-id="49899-246">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="49899-247">Daha önce oluşturduğunuz anahtar kasasına gidin ve **Gizli Anahtarlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-247">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="49899-248">Aşağıdaki tabloda bulunan her gizli anahtar adı için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="49899-248">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="49899-249">**Oluştur/İçe aktar** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="49899-249">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="49899-250">**Gizli anahtar oluştur** iletişim kutusunda **Karşıya yükleme seçenekleri** alanında, **El ile** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="49899-250">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="49899-251">Aşağıdaki tablodan gizli anahtar adını ve değerini oluşturun.</span><span class="sxs-lookup"><span data-stu-id="49899-251">Create the secret name and value from the following table.</span></span>
        4. <span data-ttu-id="49899-252">**Etkin**'i ve ardından **Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-252">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="49899-253">Gizli anahtar oluşturulur ve Key Vault'a eklenir.</span><span class="sxs-lookup"><span data-stu-id="49899-253">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="49899-254">Parola adı</span><span class="sxs-lookup"><span data-stu-id="49899-254">Secret name</span></span>                       | <span data-ttu-id="49899-255">Gizli anahtar değeri</span><span class="sxs-lookup"><span data-stu-id="49899-255">Secret value</span></span>                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | <span data-ttu-id="49899-256">app-id</span><span class="sxs-lookup"><span data-stu-id="49899-256">app-id</span></span>                            | <span data-ttu-id="49899-257">Daha önce oluşturduğunuz uygulamanın uygulama kimliği</span><span class="sxs-lookup"><span data-stu-id="49899-257">The app ID of the application that you created earlier</span></span>                                      |
        | <span data-ttu-id="49899-258">app-secret</span><span class="sxs-lookup"><span data-stu-id="49899-258">app-secret</span></span>                        | <span data-ttu-id="49899-259">Daha önce kaydettiğiniz gizli anahtar</span><span class="sxs-lookup"><span data-stu-id="49899-259">The client secret that you saved earlier</span></span>                                                    |
        | <span data-ttu-id="49899-260">storage-account-name</span><span class="sxs-lookup"><span data-stu-id="49899-260">storage-account-name</span></span>              | <span data-ttu-id="49899-261">Daha önce oluşturduğunuz depolama hesabının adı (ör. **storageaccount1**)</span><span class="sxs-lookup"><span data-stu-id="49899-261">The name of the storage account that you created earlier, such as **storageaccount1**</span></span>       |
        | <span data-ttu-id="49899-262">storage-account-connection-string</span><span class="sxs-lookup"><span data-stu-id="49899-262">storage-account-connection-string</span></span> | <span data-ttu-id="49899-263">Depolama hesabı için **Erişim anahtarları** sayfasından kopyaladığınız bağlantı dizesi</span><span class="sxs-lookup"><span data-stu-id="49899-263">The connection string that you copied from the **Access keys** page for the storage account</span></span> |

5. <span data-ttu-id="49899-264">Anahtar kasasına erişmek için uygulamayı yetkilendirme:</span><span class="sxs-lookup"><span data-stu-id="49899-264">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="49899-265">[Azure portalında](https://portal.azure.com), daha önce oluşturduğunuz anahtar kasasını açın.</span><span class="sxs-lookup"><span data-stu-id="49899-265">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="49899-266">Erişim ilkelerini seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-266">Select the access policies.</span></span>
    3. <span data-ttu-id="49899-267">Aşağıdaki tabloda bulunan her uygulama için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="49899-267">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="49899-268">Erişim ilkesi oluşturmak için **Erişim İlkesi Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-268">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="49899-269">**Gizli anahtar izinleri** alanında, aşağıdaki tabloda yer alan izinleri seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-269">In the **Secret permissions** field, select the permissions from the following table.</span></span>
        3. <span data-ttu-id="49899-270">**Sorumlu seç** alanında aşağıdaki tablodan uygulama görünen adını arayın.</span><span class="sxs-lookup"><span data-stu-id="49899-270">In the **Select principal** field, search for the application display name from the following table.</span></span>
        4. <span data-ttu-id="49899-271">**Seç** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-271">Select **Select**.</span></span>
        5. <span data-ttu-id="49899-272">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-272">Select **Add**.</span></span>
        6. <span data-ttu-id="49899-273">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-273">Select **Save**.</span></span>

        | <span data-ttu-id="49899-274">Uygulama</span><span class="sxs-lookup"><span data-stu-id="49899-274">Application</span></span>                                              | <span data-ttu-id="49899-275">İzinler</span><span class="sxs-lookup"><span data-stu-id="49899-275">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="49899-276">Oluşturduğunuz yeni uygulamanın görünen adı</span><span class="sxs-lookup"><span data-stu-id="49899-276">The display name of the new application that you created</span></span> | <span data-ttu-id="49899-277">Al, Listele</span><span class="sxs-lookup"><span data-stu-id="49899-277">Get, List</span></span>   |
        | <span data-ttu-id="49899-278">**Microsoft Dynamics ERP Mikro Hizmetleri**</span><span class="sxs-lookup"><span data-stu-id="49899-278">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="49899-279">Al, Listele</span><span class="sxs-lookup"><span data-stu-id="49899-279">Get, List</span></span>   |

6. <span data-ttu-id="49899-280">Depolama hesabına erişmek için rolleri atama:</span><span class="sxs-lookup"><span data-stu-id="49899-280">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="49899-281">[Azure portalında](https://portal.azure.com), daha önce oluşturduğunuz depolama hesabını açın.</span><span class="sxs-lookup"><span data-stu-id="49899-281">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="49899-282">**Access Control (IAM)** seçeneğini belirleyin ve ardından **Rol Atamaları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-282">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="49899-283">**Ekle, Rol Ataması Ekle** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="49899-283">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="49899-284">Aşağıdaki tabloda bulunan her uygulama için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="49899-284">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="49899-285">Aşağıdaki tablodan rolü seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-285">Select the role from the following table.</span></span>
        2. <span data-ttu-id="49899-286">**Erişim ata** alanını **Azure AD kullanıcısı, grubu veya hizmet sorumlusu** olarak bırakın.</span><span class="sxs-lookup"><span data-stu-id="49899-286">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="49899-287">**Seç** alanında aşağıdaki tablodan uygulamayı girin.</span><span class="sxs-lookup"><span data-stu-id="49899-287">In the **Select** field, enter the application from the following table.</span></span>
        4. <span data-ttu-id="49899-288">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-288">Select **Save**.</span></span>

        | <span data-ttu-id="49899-289">Uygulama</span><span class="sxs-lookup"><span data-stu-id="49899-289">Application</span></span>                                              | <span data-ttu-id="49899-290">Rol</span><span class="sxs-lookup"><span data-stu-id="49899-290">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="49899-291">Oluşturduğunuz yeni uygulamanın görünen adı</span><span class="sxs-lookup"><span data-stu-id="49899-291">The display name of the new application that you created</span></span> | <span data-ttu-id="49899-292">Sahip</span><span class="sxs-lookup"><span data-stu-id="49899-292">Owner</span></span>                       |
        | <span data-ttu-id="49899-293">Oluşturduğunuz yeni uygulamanın görünen adı</span><span class="sxs-lookup"><span data-stu-id="49899-293">The display name of the new application that you created</span></span> | <span data-ttu-id="49899-294">Katılımcı</span><span class="sxs-lookup"><span data-stu-id="49899-294">Contributor</span></span>                 |
        | <span data-ttu-id="49899-295">Oluşturduğunuz yeni uygulamanın görünen adı</span><span class="sxs-lookup"><span data-stu-id="49899-295">The display name of the new application that you created</span></span> | <span data-ttu-id="49899-296">Depolama Hesabı Katılımcısı</span><span class="sxs-lookup"><span data-stu-id="49899-296">Storage Account Contributor</span></span> |
        | <span data-ttu-id="49899-297">Oluşturduğunuz yeni uygulamanın görünen adı</span><span class="sxs-lookup"><span data-stu-id="49899-297">The display name of the new application that you created</span></span> | <span data-ttu-id="49899-298">Depolama Blobu Veri Sahibi</span><span class="sxs-lookup"><span data-stu-id="49899-298">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="49899-299">**AI Builder Yetkilendirme Hizmeti**</span><span class="sxs-lookup"><span data-stu-id="49899-299">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="49899-300">Depolama Blobu Veri Okuyucusu</span><span class="sxs-lookup"><span data-stu-id="49899-300">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="49899-301">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="49899-301">Azure CLI</span></span>](#tab/azure-azure-cli)

```
function New-FinanceDataLakeAzureResources {
    $defaultSecretExpiryInYear = 1

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

    $subscriptionId = (Read-Host -Prompt "Enter the Azure Subscription ID: (blank for default)")
    if ($subscriptionId.Trim() -ne '') {
        $azSubscription = Select-AzSubscription -SubscriptionId $subscriptionId
    }

    $resourceGroupName = (Read-Host -Prompt "Enter the Azure Resource Group name: (blank for 'FinanceDataLake')")
    if ($null -eq $resourceGroupName -or $resourceGroupName.Trim() -eq '') {
        $resourceGroupName = 'FinanceDataLake'
    }
    $resourceGroup = Get-AzResourceGroup -Name $resourceGroupName -ErrorAction SilentlyContinue

    if (-not ($resourceGroup)) {
        $resourceLocation = ''
        $azResourceLocations = (Get-AzLocation | Select-Object Location).Location
        while ($resourceLocation.Trim() -eq '' -or (-not ($resourceLocation -in $azResourceLocations))) {
            $resourceLocation = (Read-Host -Prompt "Enter the location in which to create the Azure Resource Group: ('help' to see values)")
            if ($resourceLocation -eq 'help') {
                $azResourceLocations
                $resourceLocation = ''
            }
        }
        $resourceGroup = New-AzResourceGroup -Name $resourceGroupName -Location $resourceLocation
    }
    else {
        $resourceLocation = $resourceGroup.Location
    }

    $clientAppName = (Read-Host -Prompt "Enter the name of the application registration: (blank for 'Finance Data Lake Application')")
    if ($clientAppName.Trim() -eq '') {
        $clientAppName = 'Finance Data Lake Application'
    }

    Write-Output '================================================================================='

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $MicrosoftDynamicsERPMicroservicesAppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesAppId | Format-Table -AutoSize
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $MicrosoftDynamicsERPMicroservicesAppId + "'")
        Write-Output ("Added AAD Enterprise Application 'Microsoft Dynamics ERP Microservices' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesAppId)
    }
    else {
        Write-Output ("Found AAD Enterprise Application 'Microsoft Dynamics ERP Microservices' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesAppId)
    }
    $MicrosoftDynamicsERPMicroservicesAppObjectId = $service.ObjectId

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $MicrosoftDynamicsERPMicroservicesCDSAppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesCDSAppId | Format-Table -AutoSize
        Write-Output ("Added AAD Enterprise Application 'Microsoft Dynamics ERP Microservices CDS' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesCDSAppId)
    }
    else {
        Write-Output ("Found AAD Enterprise Application 'Microsoft Dynamics ERP Microservices CDS' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesCDSAppId)
    }

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AIBuilderAuthorizationServiceAppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $AIBuilderAuthorizationServiceAppId | Format-Table -AutoSize
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AIBuilderAuthorizationServiceAppId + "'")
        Write-Output ("Added AAD Enterprise Application 'AI Builder Authorization Service' with Application ID {0}" -f $AIBuilderAuthorizationServiceAppId)
    }
    else {
        Write-Output ("Found AAD Enterprise Application 'AI Builder Authorization Service' with Application ID {0}" -f $AIBuilderAuthorizationServiceAppId)
    }
    $aibuilderAuthorizationServiceObjectId = $service.ObjectId

    Write-Output '================================================================================='

    $clientAppSPN = Get-AzureADServicePrincipal -Filter ("DisplayName eq '" + $clientAppName + "'")
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

        $clientApp = New-AzureADApplication -DisplayName $clientAppName -RequiredResourceAccess @($keyVaultAccess, $graphAccess)
        $clientAppSPN = New-AzureADServicePrincipal -AppId $clientApp.AppId -Tags @($clientAppName)
        $clientAppId = $clientApp.AppId
        Write-Output ('Created App Registration "' + $clientAppName + '" with Application Id: ' + $clientAppId)
    }
    else {
        $clientApp = Get-AzureADApplication -Filter ("DisplayName eq '" + $clientAppName + "'")
        $clientAppId = $clientApp.AppId
        Write-Output ('Found App Registration "' + $clientAppName + '" with Application Id: ' + $clientAppId)
    }
            
    $clientAppSecretCredential = New-AzureADApplicationPasswordCredential -ObjectId $clientApp.ObjectId -CustomKeyIdentifier "ClientAppAccessKey" -EndDate (get-date).AddYears($defaultSecretExpiryInYear)
    $ClientAppSecret = $clientAppSecretCredential.Value
    $clientAppSpId = $clientAppSPN.ObjectId

    Write-Output ('Generated application secret: ' + $ClientAppSecret)
    Write-Output '================================================================================='

    $templateObject = ConvertFrom-Json $azureTemplate -AsHashtable
    $templateObject.{$schema} = "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#"
    Write-Output 'Provisioning Azure resources. This may take a few minutes.'
    $deployment = New-AzResourceGroupDeployment -ResourceGroupName $resourceGroupName -TemplateObject $templateObject -aibuilderAppObjectId $aibuilderAuthorizationServiceObjectId -clientAppId $clientAppId -clientAppSecret $ClientAppSecret -clientAppSpObjectId  $clientAppSpId -microserviceSpObjectId $MicrosoftDynamicsERPMicroservicesAppObjectId -userSpObjectId $user.ObjectId

    if ($deployment.ProvisioningState -eq 'Succeeded') {
        Write-Output "Successfully deployed the following resources to Azure:"
        Write-Output ("  Key Vault:                         " + $deployment.Outputs.keyVaultName.Value)
        Write-Output ("  Storage Account:                   " + $deployment.Outputs.storageAccountName.Value)
    }
    else {
        Write-Output ("Provisioning Azure resources failed with the following state: " + $deployment.ProvisioningState)
        Write-Output ("Some of the resources may have been created in resource group: " + $resourceGroupName)
    }

    Write-Output '================================================================================='

    $keyVault = Get-AzKeyVault -VaultName $deployment.Outputs.keyVaultName.Value
    Write-Output "Values for LCS Data Lake Add-In:"
    Write-Output ("  Tenant ID:                         " + $subscriptionContext.Context.Subscription.TenantId)
    Write-Output ("  DNS Name:                          " + $keyVault.VaultUri)
    Write-Output "  Storage account secret name:       storage-account-name"
    Write-Output "  Application ID secret name:        app-id"
    Write-Output "  Application Secret secret name:    app-secret"
    Write-Warning "Copy this information for the LCS Add-in as it is not saved. Azure Cloud Shell will eventually time out and close."

    Write-Output '================================================================================='
    Write-Output "Values for System parameters > Data connections:"
    Write-Output ("  Application ID:                    " + $clientAppId)
    Write-Output ("  Application Secret:                " + $ClientAppSecret)
    Write-Output ("  DNS name:                          " + $keyVault.VaultUri)
    Write-Output "  Secret name:                       storage-account-connection-string"
    Write-Warning "Copy this information for the System parameters as it is not saved. Azure Cloud Shell will eventually time out and close."
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
  New-FinanceDataLakeAzureResources
}
catch {
  Write-Error $_.Exception.Message
  Write-Warning $_.Exception.StackTrace
  $inner = $_.Exception.InnerException
  while ($null -ne $inner) {
    Write-Output 'Inner Exception:'
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $inner.InnerException
  }
}

```
---

## <a name="configure-the-entity-store"></a><span data-ttu-id="49899-302">Varlık deposunu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="49899-302">Configure the entity store</span></span>

<span data-ttu-id="49899-303">Finance ortamınızda varlık deposunu ayarlamak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="49899-303">Follow these steps to set up the entity store in your Finance environment.</span></span>

1. <span data-ttu-id="49899-304">**Sistem Yönetimi \> Kurulum \> Sistem parametreleri \> Veri bağlantıları** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="49899-304">Go to **System administration \> Setup \> System parameters \> Data connections**.</span></span>
2. <span data-ttu-id="49899-305">**Data Lake tümleştirmesini etkinleştir** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="49899-305">Set the **Enable Data Lake integration** option to **Yes**.</span></span>
3. <span data-ttu-id="49899-306">Aşağıdaki Key Vault alanlarını ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="49899-306">Set the following Key Vault fields:</span></span>

    - <span data-ttu-id="49899-307">**Uygulama (istemci) kimliği**: Daha önce oluşturduğunuz uygulama istemcisi kimliğini girin.</span><span class="sxs-lookup"><span data-stu-id="49899-307">**Application (client) ID** – Enter the application client ID that you created earlier.</span></span>
    - <span data-ttu-id="49899-308">**Uygulama Gizli Anahtarı**: Daha önce oluşturduğunuz uygulama için kaydettiğiniz gizli anahtarı girin.</span><span class="sxs-lookup"><span data-stu-id="49899-308">**Application Secret** – Enter the secret that you saved for the application that you created earlier.</span></span>
    - <span data-ttu-id="49899-309">**DNS adı**: Daha önce oluşturduğunuz uygulamanın uygulama ayrıntıları sayfasında Etki Alanı Adı Sistemi (DNS) adını bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="49899-309">**DNS name** – You can find the Domain Name System (DNS) name on the application details page for the application that you created earlier.</span></span>
    - <span data-ttu-id="49899-310">**Gizli anahtar adı**: **storage-account-connection-string** dizesini girin.</span><span class="sxs-lookup"><span data-stu-id="49899-310">**Secret name** – Enter **storage-account-connection-string**.</span></span>

## <a name="configure-the-data-lake"></a><span data-ttu-id="49899-311">Veri gölünü yapılandırma</span><span class="sxs-lookup"><span data-stu-id="49899-311">Configure the data lake</span></span>

<span data-ttu-id="49899-312">LCS'yi kullanarak Azure Data Lake eklentisini ortama eklemek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="49899-312">Follow these steps to use LCS to add the Azure Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="49899-313">LCS'de oturum açın ve sonra sayfanın sağ tarafındaki ortam adının altında **Tüm Ayrıntılar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-313">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="49899-314">**Ortam eklentileri** bölümünde, **Yeni bir eklenti yükleyin**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-314">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="49899-315">**Data Lake'e dışarı aktar** eklentisini seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-315">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="49899-316">Aşağıdaki değerleri girin.</span><span class="sxs-lookup"><span data-stu-id="49899-316">Enter the following values.</span></span>

    | <span data-ttu-id="49899-317">Değer</span><span class="sxs-lookup"><span data-stu-id="49899-317">Value</span></span>                                                              | <span data-ttu-id="49899-318">Tanım</span><span class="sxs-lookup"><span data-stu-id="49899-318">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="49899-319">Key Vault'un bulunduğu Azure Aboneliğinin Kiracı Kimliği</span><span class="sxs-lookup"><span data-stu-id="49899-319">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="49899-320">Depolama hesabı, uygulamalar ve anahtar kasalarının bulunduğu kiracının kimliğidir.</span><span class="sxs-lookup"><span data-stu-id="49899-320">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="49899-321">Bu değeri bulmak için [Azure portalı](https://portal.azure.com) açın , **Azure Active Directory** öğesine gidin ve **Kiracı Kimliği** değerini kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="49899-321">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="49899-322">Key Vault'unuz için DNS adı belirtin</span><span class="sxs-lookup"><span data-stu-id="49899-322">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="49899-323">Anahtar kasasının DNS adı (ör. `https://customkeyvault.vault.azure.net/`).</span><span class="sxs-lookup"><span data-stu-id="49899-323">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> <span data-ttu-id="49899-324">(Bu değer, varlık deposunda kullanılan DNS adıyla eşleşir.)</span><span class="sxs-lookup"><span data-stu-id="49899-324">(This value matches the DNS name that is used in the entity store.)</span></span> |
    | <span data-ttu-id="49899-325">Depolama hesabının adını içeren gizli anahtarı girin</span><span class="sxs-lookup"><span data-stu-id="49899-325">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="49899-326">**storage-account-name**</span><span class="sxs-lookup"><span data-stu-id="49899-326">**storage-account-name**</span></span> |
    | <span data-ttu-id="49899-327">Data Lake'e erişmek için kullanılacak Uygulama Kimliği için Gizli Anahtar Adı</span><span class="sxs-lookup"><span data-stu-id="49899-327">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="49899-328">**app-id**</span><span class="sxs-lookup"><span data-stu-id="49899-328">**app-id**</span></span> |
    | <span data-ttu-id="49899-329">Uygulama Kimliği ile kullanılacak gizli anahtar adı</span><span class="sxs-lookup"><span data-stu-id="49899-329">Secret name to be used with App ID</span></span>                                 | <span data-ttu-id="49899-330">**app-secret**</span><span class="sxs-lookup"><span data-stu-id="49899-330">**app-secret**</span></span> |

5. <span data-ttu-id="49899-331">Koşulları kabul edin ve **Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-331">Agree to the terms, and select **Install**.</span></span>

<span data-ttu-id="49899-332">Eklenti birkaç dakika içinde yüklenir.</span><span class="sxs-lookup"><span data-stu-id="49899-332">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-ai-builder"></a><span data-ttu-id="49899-333">AI Builder'ı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="49899-333">Configure AI Builder</span></span>

1. <span data-ttu-id="49899-334">LCS'de oturum açın ve **Ortam ayrıntıları** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="49899-334">Sign in to LCS, and open the **Environment details** page.</span></span>
2. <span data-ttu-id="49899-335">**Ortam eklentileri** bölümüne kaydırın.</span><span class="sxs-lookup"><span data-stu-id="49899-335">Scroll to the **Environment add-ins** section.</span></span> <span data-ttu-id="49899-336">Bu ortamda zaten yüklü olan eklentileri görmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="49899-336">You should see the add-ins that are already installed in this environment.</span></span> <span data-ttu-id="49899-337">Bunların arasında **Data Lake'e dışarı aktar** eklentisi bulunmuyorsa bu eklentiyi yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="49899-337">If the **Export to Data Lake** add-in isn't among them, configure this add-in.</span></span>
3. <span data-ttu-id="49899-338">**İçgörü edinme** eklentisini seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-338">Select the **Get insights** add-in.</span></span>
4. <span data-ttu-id="49899-339">**İçgörü edinme** eklenti ayrıntıları sayfasında aşağıdaki değerleri girin.</span><span class="sxs-lookup"><span data-stu-id="49899-339">On the **Get insights** add-in details page, enter the following values.</span></span>

    | <span data-ttu-id="49899-340">Değer</span><span class="sxs-lookup"><span data-stu-id="49899-340">Value</span></span>                                                    | <span data-ttu-id="49899-341">Tanım</span><span class="sxs-lookup"><span data-stu-id="49899-341">Description</span></span> |
    |----------------------------------------------------------|-------------|
    | <span data-ttu-id="49899-342">CDS Kuruluş URL'si</span><span class="sxs-lookup"><span data-stu-id="49899-342">CDS Organization URL</span></span>                                     | <span data-ttu-id="49899-343">Common Data Service kurulumunun Common Data Service kuruluşu URL'si.</span><span class="sxs-lookup"><span data-stu-id="49899-343">The Common Data Service organization URL of the Common Data Service instance.</span></span> <span data-ttu-id="49899-344">Bu değeri bulmak için [Power Apps portalını](https://make.powerapps.com) açın, sağ üst köşede **Ayarlar** düğmesini (dişli simgesi) seçin, **Gelişmiş ayarlar**'ı seçin ve URL'yi kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="49899-344">To find this value, open the [Power Apps portal](https://make.powerapps.com), select the **Settings** button (gear symbol) in the upper-right upper corner, select **Advanced settings**, and copy the URL.</span></span> <span data-ttu-id="49899-345">(URL "dynamics.com" ile biter)</span><span class="sxs-lookup"><span data-stu-id="49899-345">(The URL ends with "dynamics.com.")</span></span> |
    | <span data-ttu-id="49899-346">CDS Kuruluş Kimliği</span><span class="sxs-lookup"><span data-stu-id="49899-346">CDS Org ID</span></span>                                               | <span data-ttu-id="49899-347">Common Data Service kurulumunun ortam kimliği.</span><span class="sxs-lookup"><span data-stu-id="49899-347">The environment ID of the Common Data Service instance.</span></span> <span data-ttu-id="49899-348">Bu değeri bulmak için [Power Apps portalını](https://make.powerapps.com) açın, sağ üst köşede **Ayarlar** düğmesini (dişli simgesi) seçin, **Özelleştirmeler \> Geliştirici Kaynakları \> Kurulum Referansı Bilgileri** öğesini seçin ve **Kimlik** değerini kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="49899-348">To find this value, open the [Power Apps portal](https://make.powerapps.com), select the **Settings** button (gear symbol) in the upper-right upper corner, select **Customizations \> Developer resources \> Instance Reference Information**, and copy the **ID** value.</span></span> |
    | <span data-ttu-id="49899-349">CDS Kiracı Kimliği (AAD'den Dizin Kimliği)</span><span class="sxs-lookup"><span data-stu-id="49899-349">CDS Tenant ID (Directory ID from AAD)</span></span>               | <span data-ttu-id="49899-350">Common Data Service kurulumunun kiracı kimliği.</span><span class="sxs-lookup"><span data-stu-id="49899-350">The tenant ID of the Common Data Service instance.</span></span> <span data-ttu-id="49899-351">Bu değeri bulmak için [Azure portalı](https://portal.azure.com) açın , **Azure Active Directory** öğesine gidin ve **Kiracı Kimliği** değerini kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="49899-351">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="49899-352">Sistem yöneticisi rolüne sahip kullanıcı nesnesi kimliğini belirtin</span><span class="sxs-lookup"><span data-stu-id="49899-352">Provide user object ID who has system administrator role</span></span> | <span data-ttu-id="49899-353">Common Data Service'te kullanıcının Azure AD kullanıcı nesnesi kimliği.</span><span class="sxs-lookup"><span data-stu-id="49899-353">The Azure AD user object ID of the user in Common Data Service.</span></span> <span data-ttu-id="49899-354">Bu kullanıcı, Common Data Service kurulumunun sistem yöneticisi olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="49899-354">This user must be a system administrator of the Common Data Service instance.</span></span> <span data-ttu-id="49899-355">Bu değeri bulmak için, [Azure portalı](https://portal.azure.com) açın, **Azure Active Directory \> Kullanıcılar** bölümüne gidin, kullanıcıyı seçin ve **Kimlik** bölümünde **Nesne Kimliği** değerini kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="49899-355">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory \> Users**, select the user, and then, in the **Identity** section, copy the **Object ID** value.</span></span> |
    | <span data-ttu-id="49899-356">Bu kiracı için varsayılan CDS ortamı mı?</span><span class="sxs-lookup"><span data-stu-id="49899-356">Is this the default CDS environment for the tenant?</span></span>      | <span data-ttu-id="49899-357">Common Data Service kurulumu, oluşturulan ilk üretim kurulumu ise bu onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="49899-357">If the Common Data Service instance was the first production instance that was created, select this check box.</span></span> <span data-ttu-id="49899-358">Common Data Service kurulumu el ile oluşturulmuşsa bu onay kutusunun işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="49899-358">If the Common Data Service instance was manually created, clear this check box.</span></span> |

## <a name="feedback-and-support"></a><span data-ttu-id="49899-359">Geri bildirim ve destek</span><span class="sxs-lookup"><span data-stu-id="49899-359">Feedback and support</span></span>

<span data-ttu-id="49899-360">Geri bildirim sağlamak veya destek almak istiyorsanız lütfen [Müşteri ödeme içgörüleri (Önizleme)](mailto:fiap@microsoft.com) ekibine e-posta gönderin.</span><span class="sxs-lookup"><span data-stu-id="49899-360">Please send an email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in providing feedback or need support.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="49899-361">Gizlilik bildirimi</span><span class="sxs-lookup"><span data-stu-id="49899-361">Privacy notice</span></span>

<span data-ttu-id="49899-362">Önizlemeler (1), Dynamics 365 Finance and Operations hizmetinden daha az gizlilik ve güvenlik önlemleri kullanabilir, (2) bu hizmet için hizmet düzeyi sözleşmesine (SLA) dahil edilmez, (3) kişisel verileri veya yasal ya da mevzuat uyumluluğu gereksinimlerine tabi olan diğer verileri işlemek için kullanılmamalıdır ve (4) sınırlı desteğe sahiptir.</span><span class="sxs-lookup"><span data-stu-id="49899-362">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
