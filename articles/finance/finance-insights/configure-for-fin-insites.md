---
title: Mali İçgörüler için Yapılandırma (önizleme)
description: Bu konuda, sisteminizin Mali içgörülerde sunulan özellikleri kullanabilmesini sağlayacak yapılandırma adımları açıklanmaktadır.
author: ShivamPandey-msft
ms.date: 11/25/2020
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
ms.openlocfilehash: 2443bb057a8b7fe280ed26ecae4e50f671b5e082
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818812"
---
# <a name="configuration-for-finance-insights-preview"></a>Mali içgörüler için yapılandırma (önizleme)

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Mali içgörüler, kuruluşunuza güçlü tahmin araçları sunmak için Microsoft Dynamics 365 Finance işlevlerini Microsoft Dataverse, Azure ve AI Builder işlevleriyle bir araya getirir. Bu konuda, sisteminizin Mali içgörülerde sunulan özellikleri kullanabilmesini sağlayacak yapılandırma adımları açıklanmaktadır.

## <a name="deploy-dynamics-365-finance"></a>Dynamics 365 Finance dağıtımı

Şu adımları izleyerek ortamları dağıtın.

1. Microsoft Dynamics Lifecycle Services (LCS) portalında, bir Dynamics 365 Finance ortamı oluşturun veya güncelleştirin. Ortam, sürüm 10.0.11/Platform update 35 veya daha sonraki bir uygulama sürümü gerektirir.
2. Ortam, Korumalı Alan içinde yüksek kullanılabilirlik (HA) ortamı olmalıdır. (Bu ortam türü aynı zamanda Katman 2 ortamı olarak da bilinir.) Daha fazla bilgi için bkz. [Ortam planlama](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
3. Contoso tanıtım verilerini kullanıyorsanız Müşteri ödeme tahminleri, Nakit akışı tahminleri ve Bütçe tahminleri özelliklerini kullanmak için ek örnek verilere ihtiyaç duyarsınız. 

## <a name="configure-dataverse"></a>Dataverse'ı yapılandırma

Sonraki manuel yapılandırma adımlarını tamamlayabilir veya sağlanan Windows PowerShell betiğini kullanarak yapılandırma işlemini hızlandırabilirsiniz. PowerShell betik dosyasının çalışması bittiğinde size Mali içgörüleri yapılandırmak için kullanabileceğiniz değerler sunar. 

> [!NOTE]
> Betik dosyasını çalıştırmak için bilgisayarınızda PowerShell'i açın. PowerShell sürüm 5 gerekebilir. Microsoft Azure CLI "Try it" seçeneği çalışmayabilir.

# <a name="manual-configuration-steps"></a>[El ile yapılandırma adımları](#tab/configuration-steps)

1. [Power Platform yönetim merkezini](https://admin.powerplatform.microsoft.com/)açın ve aynı Active Directory kiracısında yeni bir Dataverse ortamı oluşturmak için aşağıdaki adımları izleyin:

    1. **Ortamlar** sayfasını açın.

        [![Ortamlar sayfası](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)

    2. **Yeni ortam**'ı seçin.
    3. **Tür** alanında **Korumalı alan**'ı seçin.
    4. **Veritabanı Oluştur** seçeneğini **Evet** olarak ayarlayın.
    5. **Sonraki**'yi seçin.
    6. Kuruluşunuz için dili ve para birimini seçin.
    7. Diğer alanlar için varsayılan değerleri kabul edin.
    8. **Kaydet**'i seçin.
    9. **Ortamlar** sayfasını yenileyin.
    10. **Durum** alanının değeri **Hazır** olarak güncelleştirilene kadar bekleyin.
    11. Dataverse kuruluş kodunu not edin.
    12. Ortamı seçin ve sonra **Ayarlar**'ı seçin.
    13. **Kaynaklar \> Tüm Eski Ayarlar**'ı seçin.
    14. Üst gezinti çubuğunda, **Ayarlar**'ı seçin ve ardından **Özelleştirmeler**'i seçin.
    15. **Geliştirici Kaynakları**'nı seçin.
    16. **Kurulum Referansı Bilgi Kodu** alanını, daha önce not ettiğiniz Dataverse kuruluş kodu değeri olarak ayarlayın.
    17. Tarayıcının adres çubuğunda Dataverse kuruluşunun URL'sini not edin. Örneğin, URL şu şekilde olabilir: `https://org42b2b3d3.crm.dynamics.com`.

2. Nakit akışı tahminleri veya bütçe tahminleri özelliğini kullanmayı planlıyorsanız kuruluşunuzun ek açıklama sınırını en az 50 megabayt (MB) olarak güncelleştirmek için aşağıdaki adımları izleyin:

    1. [Power Apps portalını](https://make.powerapps.com) açın.
    2. Yeni oluşturduğunuz ortamı seçin ve sonra **Gelişmiş ayarlar**'ı seçin .
    3. **Ayarlar \> E-posta Yapılandırması**'nı seçin.
    4. **Maksimum dosya boyutu** alanının değerini **51.200** olarak değiştirin. (Değer, kilobayt \[KB\] cinsinden ifade edilir.)
    5. Yaptığınız değişiklikleri kaydetmek için **Tamam**'ı seçin.

# <a name="windows-powershell-configuration-script"></a>[Windows PowerShell yapılandırma betik dosyası](#tab/powershell-configuration-script)

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

## <a name="configure-the-azure-setup"></a>Azure kurulumunu yapılandırma

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a>Dataverse dizin kodunu ve kullanıcının Azure AD nesne kodunu girin

1. Dataverse dizin kodunu girin:

    1. [Azure portalını](https://portal.azure.com) açın.
    2. Dataverse ortamı oluşturmak için kullanılan kullanıcı kimliğini kullanarak oturum açın.
    3. **Azure Active Directory** gidin.
    4. **Kiracı Kimliği** değerini kopyalayın.

2. Kullanıcının Azure Active Directory (Azure AD) nesne kimliğini girin:

    1. [Azure portalı](https://portal.azure.com) içinde **Kullanıcılar**'a gidin ve e-posta adresine göre kullanıcıyı arayın.
    2. Kullanıcının adını seçin.
    3. **Nesne Kimliği** değerini kopyalayın.

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a>Mali içgörüler Data Lake kaynaklarını ayarlamak için Azure Cloud Shell kullanma

# <a name="use-a-windows-powershell-script"></a>[Windows PowerShell betik dosyası kullanma](#tab/use-a-powershell-script)

[Azure Data Lake'e aktarmayı yapılandırma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/configure-export-data-lake) konusunda açıklandığı gibi Azure kaynaklarını kolayca ayarlayabilmeniz için Windows PowerShell betik dosyası sağlanmıştır. El ile kurulum yapmayı tercih ediyorsanız bu yordamı atlayın ve [El ile kurulum](#manual-setup) bölümündeki yordama devam edin.

> [!NOTE]
> PowerShell betiğini çalıştırmak için aşağıdaki adımları izleyin. Azure CLI "Try it" seçeneği veya betiği bilgisayarınızda çalıştırmak işe yaramayabilir.

Windows PowerShell betik dosyasını kullanarak Azure yapılandırmayla ilgili bu adımları izleyin. Azure kaynak grubu, Azure kaynakları ve bir Azure AD uygulaması oluşturma haklarınız olmalıdır. Gerekli izinler hakkında daha fazla bilgi için bkz. [Azure AD izinlerini denetleme](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).

1. [Azure portalda](https://portal.azure.com) hedef Azure aboneliğinize gidin. **Arama** alanının sağında bulunan **Cloud Shell** düğmesini seçin.
2. **PowerShell**'i seçin.
3. İstenirse, depolama alanı oluşturun. Ardından, Windows PowerShell betiğini oturuma yükleyin.
4. Betik dosyasını çalıştırın.
5. Betik dosyasını çalıştırmak için istemleri izleyin.
6. LCS'ye **Data Lake'e dışarı aktar** eklentisini yüklemek için betik dosyası çıktısındaki bilgileri kullanın.
7. Finance'teki **Veri bağlantıları** sayfasında varlık deposunu etkinleştirmek için betik dosyası çıktısındaki bilgileri kullanın (**Sistem yönetimi \> Sistem parametreleri \> Veri bağlantıları**).

### <a name="manual-setup"></a>El ile kurulum

#### <a name="add-applications-to-the-azure-ad-tenant"></a>Azure AD kiracısına uygulama ekleme

1. [Azure portalda](https://portal.azure.com) **Azure Active Directory**'ye gidin.
2. **Yönet \> Kurumsal uygulamalar** öğesini seçin.
3. Uygulama kimliğine göre aşağıdaki uygulamaları arayın.

    | Uygulama                              | Uygulama kodu                               |
    |------------------------------------------|--------------------------------------|
    | Microsoft Dynamics ERP Mikro Hizmetleri     | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |
    | Microsoft Dynamics ERP Mikro Hizmetleri CDS | 703e2651-d3fc-48f5-942c-74274233dba8 |
    | AI Builder Yetkilendirme Hizmeti         | ad40333e-9910-4b61-b281-e3aeeb8c3ef3 |

Önceki uygulamalardan hiçbirini bulamazsanız aşağıdaki adımları deneyin.

1. Yerel makinenizde, **Başlat** menüsünü seçin ve **powershell**'i arayın.
2. **Windows PowerShell**'i seçin ve basılı tutun (veya sağ tıklayın) ve sonra **Yönetici olarak çalıştır**'ı seçin.
3. **AzureAD** modülünü yüklemek için aşağıdaki komutu çalıştırın.

    `Install-Module -Name AzureAD`

4. Devam etmek için NuGet sağlayıcısı gerekiyorsa yüklemek için **Y**'yi seçin.
5. "Güvenilmeyen depo" iletisi görüntülenirse devam etmek için **Y**'yi seçin.
6. Eklenmesi gereken her uygulama için uygulamayı Azure AD'ye eklemek üzere aşağıdaki komutları çalıştırın. İstendiğinde, Azure AD yöneticisi olarak oturum açın.

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a>Azure kaynakları oluşturma

> [!NOTE]
> Dataverse ortamıyla aynı Azure AD kurulumunda aşağıdaki kaynakları oluşturduğunuzdan emin olun. Farklı bir Azure AD kurulumundan kaynak kullanamazsınız.

1. Yeni depolama hesabı oluşturma:

    1. [Azure portalında](https://portal.azure.com) bir depolama hesabı oluşturun.
    2. **Depolama hesabı oluştur** iletişim kutusunda, aşağıdaki alanları ayarlayın:

        - **Konum**: Ortamınızın bulunduğu veri merkezini seçin.
        - **Performans**: **Standart** seçeneğini belirlemenizi öneririz.
        - **Hesap türü**: **StorageV2**'yi seçmelisiniz.

    3. **Gelişmiş seçenekler** iletişim kutusunda **Data Lake Storage 2. Nesil** seçeneği için **Hiyerarşik ad alanları** bölümünde **Etkinleştir**'i seçin. Bu özelliği devre dışı bırakırsanız Power BI veri akışları gibi hizmetleri kullanarak, Finance and Operations uygulamalarının yazdığı verileri kullanamazsınız.
    4. **İncele ve oluştur**'u seçin. Dağıtım tamamlandığında, yeni kaynak Azure portalında gösterilir.
    5. Oluşturduğunuz depolama hesabına gidin.
    6. Sol menüde **Erişim anahtarları**'nı seçin.
    7. **Key1** veya **Key2** için bağlantı dizesini kopyalayıp kaydedin.
    8. Depolama hesabı adını kopyalayın ve kaydedin.

2. Yeni bir anahtar kasası oluşturma:

    1. [Azure portalında](https://portal.azure.com) bir anahtar kasası oluşturun.
    2. **Anahtar kasası oluştur** iletişim kutusundaki **Konum** alanında ortamınızın bulunduğu veri merkezini seçin.
    3. Anahtar kasası oluşturulduktan sonra, kasayı listeden seçin ve ardından **Gizli anahtarlar**'ı seçin.
    4. **Oluştur/İçe aktar** seçeneğini belirleyin.
    5. **Gizli anahtar oluştur** iletişim kutusunda **Karşıya yükleme seçenekleri** alanında, **El ile** seçeneğini belirleyin.
    6. Gizli anahtar için bir ad girin. Daha sonra sağlamanız gerekeceği için bu adı not edin.
    7. **Değer** alanında, önceki yordamda depolama hesabından elde ettiğiniz bağlantı dizesini girin.
    8. **Etkin**'i ve ardından **Oluştur**'u seçin. Gizli anahtar oluşturulur ve Key Vault'a eklenir.
    9. **Key Vault'a Genel Bakış**'a gidin ve DNS adını not edin.

3. Bir Azure AD uygulaması oluşturma ve kaydetme:

    1. [Azure portalında](https://portal.azure.com) **Azure Active Directory**'ye gidin ve ardından **Uygulama kayıtları**'nı seçin.
    2. **Yeni uygulama kaydı**'nı seçin ve aşağıdaki alanları ayarlayın:

        - **Ad**: Uygulamanın adını girin.
        - **Uygulama türü**: **Web API'si** seçeneğini belirleyin.
        - **Yeniden yönlendirme URI'si kurulumu**: Dynamics 365 kurulumunuzun URL'sini girin (ör. `https://yourdynamicsinstance.dynamics.com/auth`).

    3. Yeni oluşturduğunuz uygulamaya gidin ve **Uygulama (istemci) kimliği** değerini kopyalayın ve kaydedin. Anahtar kasasını ayarlarken bu değeri sağlamanız gerekir.
    4. **API izinleri**'ne gidin ve şu adımları izleyin:

        1. **İzin ekle**'yi seçin.
        2. **Azure Key Vault**'u seçin.
        3. Temsilci izinleri seçtikten sonra **kullanıcı\_kimliğe bürünmey**'yi seçin.
        4. **İzin ekle**'yi seçin.

    5. Uygulama menüsünde, **Sertifikalar \& gizli anahtarlar**'ı seçin ve ardından Key Vault gizli anahtarlarını oluşturmak için bu adımları izleyin:

        1. **Yeni gizli anahtar**'ı seçin.
        2. **Anahtar Açıklaması** alanına bir ad girin.
        3. Bir süre seçin ve ardından **Ekle**'yi seçin. **Değer** alanında gizli anahtar oluşturulur.
        4. Gizli anahtar değerini kopyalayın ve kaydedin.

4. Key Vault gizli anahtarları oluşturma:

    1. Daha önce oluşturduğunuz anahtar kasasına gidin ve **Gizli Anahtarlar**'ı seçin.
    2. Aşağıdaki tabloda bulunan her gizli anahtar adı için şu adımları izleyin:

        1. **Oluştur/İçe aktar** seçeneğini belirleyin.
        2. **Gizli anahtar oluştur** iletişim kutusunda **Karşıya yükleme seçenekleri** alanında, **El ile** seçeneğini belirleyin.
        3. Aşağıdaki tablodan gizli anahtar adını ve değerini oluşturun.
        4. **Etkin**'i ve ardından **Oluştur**'u seçin. Gizli anahtar oluşturulur ve Key Vault'a eklenir.

        | Parola adı                       | Gizli anahtar değeri                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | app-id                            | Daha önce oluşturduğunuz uygulamanın uygulama kimliği                                      |
        | app-secret                        | Daha önce kaydettiğiniz gizli anahtar                                                    |
        | storage-account-name              | Daha önce oluşturduğunuz depolama hesabının adı (ör. **storageaccount1**)       |
        | storage-account-connection-string | Depolama hesabı için **Erişim anahtarları** sayfasından kopyaladığınız bağlantı dizesi |

5. Anahtar kasasına erişmek için uygulamayı yetkilendirme:

    1. [Azure portalında](https://portal.azure.com), daha önce oluşturduğunuz anahtar kasasını açın.
    2. Erişim ilkelerini seçin.
    3. Aşağıdaki tabloda bulunan her uygulama için şu adımları izleyin:

        1. Erişim ilkesi oluşturmak için **Erişim İlkesi Ekle**'yi seçin.
        2. **Gizli anahtar izinleri** alanında, aşağıdaki tabloda yer alan izinleri seçin.
        3. **Sorumlu seç** alanında aşağıdaki tablodan uygulama görünen adını arayın.
        4. **Seç** öğesini seçin.
        5. **Ekle**'yi seçin.
        6. **Kaydet**'i seçin.

        | Uygulama                                              | İzinler |
        |----------------------------------------------------------|-------------|
        | Oluşturduğunuz yeni uygulamanın görünen adı | Al, Listele   |
        | **Microsoft Dynamics ERP Mikro Hizmetleri**                 | Al, Listele   |

6. Depolama hesabına erişmek için rolleri atama:

    1. [Azure portalında](https://portal.azure.com), daha önce oluşturduğunuz depolama hesabını açın.
    2. **Access Control (IAM)** seçeneğini belirleyin ve ardından **Rol Atamaları**'nı seçin.
    3. **Ekle, Rol Ataması Ekle** seçeneğini belirleyin.
    4. Aşağıdaki tabloda bulunan her uygulama için şu adımları izleyin:

        1. Aşağıdaki tablodan rolü seçin.
        2. **Erişim ata** alanını **Azure AD kullanıcısı, grubu veya hizmet sorumlusu** olarak bırakın.
        3. **Seç** alanında aşağıdaki tablodan uygulamayı girin.
        4. **Kaydet**'i seçin.

        | Uygulama                                              | Rol                        |
        |----------------------------------------------------------|-----------------------------|
        | Oluşturduğunuz yeni uygulamanın görünen adı | Sahip                       |
        | Oluşturduğunuz yeni uygulamanın görünen adı | Katılımcı                 |
        | Oluşturduğunuz yeni uygulamanın görünen adı | Depolama Hesabı Katılımcısı |
        | Oluşturduğunuz yeni uygulamanın görünen adı | Depolama Blobu Veri Sahibi     |
        | **AI Builder Yetkilendirme Hizmeti**                     | Depolama Blobu Veri Okuyucusu    |

# <a name="azure-cli"></a>[Azure CLI](#tab/azure-azure-cli)

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

## <a name="configure-the-entity-store"></a>Varlık deposunu yapılandırma

Finance ortamınızda varlık deposunu ayarlamak için bu adımları izleyin.

1. **Sistem Yönetimi \> Kurulum \> Sistem parametreleri \> Veri bağlantıları** bölümüne gidin.
2. **Data Lake tümleştirmesini etkinleştir** seçeneğini **Evet** olarak ayarlayın.
3. Aşağıdaki Key Vault alanlarını ayarlayın:

    - **Uygulama (istemci) kimliği**: Daha önce oluşturduğunuz uygulama istemcisi kimliğini girin.
    - **Uygulama Gizli Anahtarı**: Daha önce oluşturduğunuz uygulama için kaydettiğiniz gizli anahtarı girin.
    - **DNS adı**: Daha önce oluşturduğunuz uygulamanın uygulama ayrıntıları sayfasında Etki Alanı Adı Sistemi (DNS) adını bulabilirsiniz.
    - **Gizli anahtar adı**: **storage-account-connection-string** dizesini girin.

## <a name="configure-the-data-lake"></a>Veri gölünü yapılandırma

LCS'yi kullanarak Azure Data Lake eklentisini ortama eklemek için bu adımları izleyin.

1. LCS'de oturum açın ve sonra sayfanın sağ tarafındaki ortam adının altında **Tüm Ayrıntılar**'ı seçin.
2. **Ortam eklentileri** bölümünde, **Yeni bir eklenti yükleyin**'i seçin.
3. **Data Lake'e dışarı aktar** eklentisini seçin.
4. Aşağıdaki değerleri girin.

    | Değer                                                              | Tanım |
    |--------------------------------------------------------------------|-------------|
    | Key Vault'un bulunduğu Azure Aboneliğinin Kiracı Kimliği | Depolama hesabı, uygulamalar ve anahtar kasalarının bulunduğu kiracının kimliğidir. Bu değeri bulmak için [Azure portalı](https://portal.azure.com) açın , **Azure Active Directory** öğesine gidin ve **Kiracı Kimliği** değerini kopyalayın. |
    | Key Vault'unuz için DNS adı belirtin                             | Anahtar kasasının DNS adı (ör. `https://customkeyvault.vault.azure.net/`). (Bu değer, varlık deposunda kullanılan DNS adıyla eşleşir.) |
    | Depolama hesabının adını içeren gizli anahtarı girin   | **storage-account-name** |
    | Data Lake'e erişmek için kullanılacak Uygulama Kimliği için Gizli Anahtar Adı          | **app-id** |
    | Uygulama Kimliği ile kullanılacak gizli anahtar adı                                 | **app-secret** |

5. Koşulları kabul edin ve **Yükle**'yi seçin.

Eklenti birkaç dakika içinde yüklenir.

## <a name="configure-ai-builder"></a>AI Builder'ı yapılandırma

1. LCS'de oturum açın ve **Ortam ayrıntıları** sayfasını açın.
2. **Ortam eklentileri** bölümüne kaydırın. Bu ortamda zaten yüklü olan eklentileri görmelisiniz. Bunların arasında **Data Lake'e dışarı aktar** eklentisi bulunmuyorsa bu eklentiyi yapılandırın.
3. **İçgörü edinme** eklentisini seçin.
4. **İçgörü edinme** eklenti ayrıntıları sayfasında aşağıdaki değerleri girin.

    | Değer                                                    | Tanım |
    |----------------------------------------------------------|-------------|
    | CDS Kuruluş URL'si                                     | Dataverse kurulumunun Dataverse kuruluşu URL'si. Bu değeri bulmak için [Power Apps portalını](https://make.powerapps.com) açın, sağ üst köşede **Ayarlar** düğmesini (dişli simgesi) seçin, **Gelişmiş ayarlar**'ı seçin ve URL'yi kopyalayın. (URL "dynamics.com" ile biter) |
    | CDS Kuruluş Kimliği                                               | Dataverse kurulumunun ortam kimliği. Bu değeri bulmak için [Power Apps portalını](https://make.powerapps.com) açın, sağ üst köşede **Ayarlar** düğmesini (dişli simgesi) seçin, **Özelleştirmeler \> Geliştirici Kaynakları \> Kurulum Referansı Bilgileri** öğesini seçin ve **Kimlik** değerini kopyalayın. |
    | CDS Kiracı Kimliği (AAD'den Dizin Kimliği)               | Dataverse kurulumunun kiracı kimliği. Bu değeri bulmak için [Azure portalı](https://portal.azure.com) açın , **Azure Active Directory** öğesine gidin ve **Kiracı Kimliği** değerini kopyalayın. |
    | Sistem yöneticisi rolüne sahip kullanıcı nesnesi kimliğini belirtin | Dataverse'te kullanıcının Azure AD kullanıcı nesnesi kimliği. Bu kullanıcı, Dataverse kurulumunun sistem yöneticisi olmalıdır. Bu değeri bulmak için, [Azure portalı](https://portal.azure.com) açın, **Azure Active Directory \> Kullanıcılar** bölümüne gidin, kullanıcıyı seçin ve **Kimlik** bölümünde **Nesne Kimliği** değerini kopyalayın. |
    | Bu kiracı için varsayılan CDS ortamı mı?      | Dataverse kurulumu, oluşturulan ilk üretim kurulumu ise bu onay kutusunu seçin. Dataverse kurulumu el ile oluşturulmuşsa bu onay kutusunun işaretini kaldırın. |

## <a name="feedback-and-support"></a>Geri bildirim ve destek

Geri bildirim sağlamak veya destek almak istiyorsanız lütfen [Müşteri ödeme içgörüleri (Önizleme)](mailto:fiap@microsoft.com) ekibine e-posta gönderin.

## <a name="privacy-notice"></a>Gizlilik bildirimi

Önizlemeler (1), Dynamics 365 Finance and Operations hizmetinden daha az gizlilik ve güvenlik önlemleri kullanabilir, (2) bu hizmet için hizmet düzeyi sözleşmesine (SLA) dahil edilmez, (3) kişisel verileri veya yasal ya da mevzuat uyumluluğu gereksinimlerine tabi olan diğer verileri işlemek için kullanılmamalıdır ve (4) sınırlı desteğe sahiptir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]