---
title: Genel önizleme için Finance Insights (önizleme) sürüm 10.0.20 ve sonrası için yapılandırma
description: Bu konu, genel önizleme için Finance Insights sürüm 10.0.20 ve sonrasında bulunan özellikleri kullanmak üzere sisteminizi yapılandırma yöntemini açıklamaktadır.
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
ms.search.validFrom: 2021-06-03
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: eeb3061f215666d0aeb32094b5d04a9ae6e618f2
ms.sourcegitcommit: f6050b444e636ba662c00d0443c94a99f8ea0b0d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/28/2021
ms.locfileid: "6309677"
---
# <a name="configuration-for-finance-insights-for-public-preview-preview---version-10020-and-later"></a>Genel önizleme için Finance Insights (önizleme) sürüm 10.0.20 ve sonrası için yapılandırma

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Mali içgörüler, kuruluşunuza güçlü tahmin araçları sunmak için Microsoft Dynamics 365 Finance işlevlerini Dataverse, Azure ve AI Builder işlevleriyle bir araya getirir. Bu konu, genel önizleme için Finance Insights sürüm 10.0.20 ve sonrasında bulunan özellikleri sisteminizin kullanabilmesi için Dynamics 365 Finance sürüm 10.0.20'yi yapılandırma yöntemini açıklamaktadır.

> [!NOTE]
> Bu konuda açıklanan yapılandırma adımları yalnızca Finance sürüm 10.0.20 ve sonrası için geçerlidir. Finance Insights'ı sürüm 10.0.19 ve öncesinde ayarlamak için bkz. [Sürüm 10.0.19'e kadar Finance Insights yapılandırmaları](configure-for-fin-insites.md).

## <a name="deploy-finance"></a>Finance'i Dağıtma

Ortamları dağıtmak için aşağıdaki adımları uygulayın.

1. Microsoft Dynamics Lifecycle Services'da (LCS), bir Finance ortamı oluşturun veya güncelleştirin. Ortam, sürüm 10.0.20 veya daha sonraki bir Finance and Operations uygulamaları sürümü gerektirir.
2. Ortam, Korumalı Alan içinde yüksek kullanılabilirlik (HA) ortamı olmalıdır. (Bu ortam türü aynı zamanda Katman 2 ortamı olarak da bilinir.) Daha fazla bilgi için bkz. [Ortam planlama](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
3. Finance Insights'ı bir korumalı alanda yapılandırıyorsanız tahminlerin çalışması için üretim verilerini ilgili ortama kopyalamanız gerekebilir. Tahmin modeli, tahminleri oluşturmak için birkaç senelik verileri kullanır. Contoso demo verileri, tahmin modelini yeterince geliştirmek için yeterli tarihsel veri içermez. 

## <a name="configure-dataverse"></a>Dataverse'ı yapılandırma

Finance Insights için Dataverse'ü yapılandırmak için aşağıdaki adımları uygulayın.

1. LCS'de, ortam sayfasını açın ve **Power Platform Tümleştirme** bölümünün zaten ayarlı olduğunu doğrulayın.

    - Zaten ayarlıysa Finance ortamına bağlı Dataverse ortam adının listelenmiş olması gerekir.
    - Henüz ayarlı değilse aşağıdaki adımları izleyin:

        1. **Power Platform Tümleştirme** bölümünde **Kurulum** öğesini seçin. Ortamın kurulumu bir saate kadar sürebilir.
        2. Dataverse ortamı başarıyla ayarlanmışsa, Finance ortamına bağlı Dataverse ortam adının listelenmiş olması gerekir.

        > [!NOTE]
        > Ortam kurulumunu tamamladıktan sonra, **Uygulamalar için CDS'e bağla** öğesini **seçmeyin**. Bu düğme, Finance Insights için gerekli değildir. Bu düğmeyi seçerseniz, LCS'de gerekli ortam eklentilerini yapılandıramazsınız.

## <a name="configure-azure"></a>Azure'yi Yapılandırma

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a>Mali içgörüler Data Lake kaynaklarını ayarlamak için Azure Cloud Shell kullanma

# <a name="use-a-windows-powershell-script"></a>[Windows PowerShell betik dosyası kullanma](#tab/use-a-powershell-script)

[Azure Data Lake'e aktarmayı yapılandırma](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) konusunda açıklandığı gibi Azure kaynaklarını kolayca ayarlayabilmeniz için Windows PowerShell betik dosyası sağlanmıştır. Kurulumu el ile yapmayı tercih ediyorsanız bu yordamı atlayın ve [El ile kurulum](#manual-setup) bölümündeki yordamı tamamlayın.

> [!NOTE]
> Windows PowerShell betiğini çalıştırmak için aşağıdaki yordamı kullanın. Azure CLI'da **Dene** seçeneğini kullanırsanız veya betiği bilgisayarınızda çalıştırırsanız kurulum çalışmayabilir.

Azure'yi yapılandırmak için Windows PowerShell betik dosyasını kullanmayla ilgili bu adımları izleyin. Azure kaynak grubu, Azure kaynakları ve bir Azure AD uygulaması oluşturma haklarınız olmalıdır. Gerekli izinler hakkında daha fazla bilgi için bkz. [Azure AD izinlerini denetleme](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).

1. [Azure portalda](https://portal.azure.com) hedef Azure aboneliğinize gidin.
2. **Arama** alanının sağında bulunan **Cloud Shell** öğesini seçin.
3. **PowerShell**'i seçin.
4. Oluşturmanız istenirse depolama alanı oluşturun.
5. **Azure CLI** sekmesinde, **Kopyala**'yı seçin.
6. Not defterinde yeni bir dosya açın ve Windows PowerShell betiğini yapıştırın.
7. Dosyayı, **ConfigureDataLake.ps1** olarak kaydedin.
8. Cloud Shell'de yükleme için menü seçeneğini kullanarak Windows PowerShell betiğini oturuma yükleyin.
9. **.\ConfigureDataLake.ps1** betiğini çalıştırın.
10. Betik dosyasını çalıştırmak için istemleri izleyin.
11. LCS'ye Data Lake'e dışarı aktar eklentisini yüklemek için betik dosyası çıktısındaki bilgileri kullanın.

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

1. Yerel bilgisayarınızda, **Başlat** menüsünde ve **powershell**'i arayın.
2. **Windows PowerShell**'i seçin ve basılı tutun (veya sağ tıklayın) ve sonra **Yönetici olarak çalıştır**'ı seçin.
3. **AzureAD** modülünü yüklemek için aşağıdaki komutu çalıştırın.

    `Install-Module -Name AzureAD`

4. Devam etmek için NuGet sağlayıcısı gerekiyorsa yüklemek için **Y**'yi seçin.
5. "Güvenilmeyen depo" iletisi alırsanız devam etmek için **Y**'yi seçin.
6. Eklenmesi gereken her uygulama için uygulamayı Azure AD'ye eklemek üzere aşağıdaki komutları çalıştırın. İstendiğinde, Azure AD yöneticisi olarak oturum açın.

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a>Azure kaynakları oluşturma

> [!NOTE]
> Dataverse ortamıyla aynı Azure AD kurulumunda aşağıdaki kaynakları oluşturduğunuzdan emin olun. Farklı bir Azure AD kurulumundan kaynak kullanamazsınız.

1. Depolama hesabı oluşturma:

    1. [Azure portalında](https://portal.azure.com) bir depolama hesabı oluşturun.
    2. **Depolama hesabı oluştur** iletişim kutusunda, aşağıdaki alanları ayarlayın:

        - **Konum**: Ortamınızın bulunduğu veri merkezini seçin.
        - **Performans**: **Standart** seçeneğini belirlemenizi öneririz.
        - **Hesap türü**: **StorageV2**'yi seçmelisiniz.

    3. **Gelişmiş seçenekler** iletişim kutusunda **Data Lake Storage 2. Nesil** seçeneği için **Hiyerarşik ad alanları** bölümünde **Etkinleştir**'i seçin. Bu özelliği etkinleştirmezseniz Power BI veri akışları gibi hizmetleri kullanarak, Finance and Operations uygulamalarının yazdığı verileri kullanamazsınız.
    4. **İncele ve oluştur**'u seçin. Dağıtım tamamlandığında, yeni kaynak Azure portalında gösterilir.
    5. Oluşturduğunuz depolama hesabına gidin.
    6. Sol menüde **Erişim anahtarları**'nı seçin.
    7. Depolama hesabının adını kopyalayın ve kaydedin. Anahtar kasası gizli dizilerini ayarlarken bu değeri sağlamanız gerekir.

2. Anahtar kasası oluşturma:

    1. [Azure portalında](https://portal.azure.com) bir anahtar kasası oluşturun.
    2. **Anahtar kasası oluştur** iletişim kutusundaki **Konum** alanında ortamınızın bulunduğu veri merkezini seçin.
    3. Anahtar kasası oluşturulduktan sonra, **Anahtar Kasasına Genel Bakış** bölümüne gidin ve DNS adını kopyalayıp kaydedin. Data Lake eklentisini ayarlarken bu değeri sağlamanız gerekir.

3. Bir Azure AD uygulaması oluşturma ve kaydetme:

    1. [Azure portalında](https://portal.azure.com) **Azure Active Directory**'ye gidin ve ardından **Uygulama kayıtları**'nı seçin.
    2. **Yeni uygulama kaydı**'nı seçin ve aşağıdaki alanları ayarlayın:

        - **Ad**: Uygulamanın adını girin.
        - **Uygulama türü**: **Web API'si** seçeneğini belirleyin.
        - **Yeniden yönlendirme URI'si kurulumu**: Dynamics 365 kurulumunuzun URL'sini girin (ör. `https://yourdynamicsinstance.dynamics.com/auth`).

    3. Yeni oluşturduğunuz uygulamaya gidin ve **Uygulama (istemci) kimliği** değerini kopyalayın ve kaydedin. Anahtar kasası gizli dizilerini ayarlarken bu değeri sağlamanız gerekir.
    4. **API izinleri**'ne gidin ve şu adımları izleyin:

        1. **İzin ekle**'yi seçin.
        2. **Azure Key Vault**'u seçin.
        3. Temsilci izinleri seçtikten sonra **kullanıcı\_kimliğe bürünmey**'yi seçin.
        4. **İzin ekle**'yi seçin.

    5. Uygulama menüsünde, **Sertifikalar \& gizli anahtarlar**'ı seçin ve ardından Key Vault gizli anahtarlarını oluşturmak için bu adımları izleyin:

        1. **Yeni gizli anahtar**'ı seçin.
        2. **Anahtar Açıklaması** alanına bir ad girin.
        3. Bir süre seçin ve ardından **Ekle**'yi seçin. **Değer** alanında gizli anahtar oluşturulur.
        4. Gizli anahtar değerini kopyalayın ve kaydedin. Anahtar kasası gizli dizilerini ayarlarken bu değeri sağlamanız gerekir.

4. Key Vault gizli anahtarları oluşturma:

    1. Daha önce oluşturduğunuz anahtar kasasına gidin ve **Gizli Anahtarlar**'ı seçin.
    2. Aşağıdaki tabloda bulunan her gizli anahtar adı için şu adımları izleyin:

        1. **Oluştur/İçe aktar** seçeneğini belirleyin.
        2. **Gizli anahtar oluştur** iletişim kutusunda **Karşıya yükleme seçenekleri** alanında, **El ile** seçeneğini belirleyin.
        3. Tablodan gizli anahtar adını ve değerini oluşturun.
        4. **Etkin**'i ve ardından **Oluştur**'u seçin. Gizli anahtar oluşturulur ve Key Vault'a eklenir.

        | Parola adı                       | Gizli anahtar değeri                                                                                 |
        |-----------------------------------|----------------------------------------------------------------------------------------------|
        | app-id                            | Daha önce oluşturduğunuz uygulamanın uygulama kimliği.                                      |
        | app-secret                        | Daha önce kaydettiğiniz gizli anahtar.                                                    |
        | storage-account-name              | Daha önce oluşturduğunuz depolama hesabının adı (ör. **storageaccount1**).       |

5. Anahtar kasasına erişmek için uygulamayı yetkilendirme:

    1. [Azure portalında](https://portal.azure.com), daha önce oluşturduğunuz anahtar kasasını açın.
    2. Erişim ilkelerini seçin.
    3. Aşağıdaki tabloda bulunan her uygulama için şu adımları izleyin:

        1. Erişim ilkesi oluşturmak için **Erişim İlkesi Ekle**'yi seçin.
        2. **Gizli anahtar izinleri** alanında, tabloda yer alan izinleri seçin.
        3. **Sorumlu seç** alanında tablodan uygulama görünen adını arayın.
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

        1. Tablodan rolü seçin.
        2. **Erişim ata** alanını **Azure AD kullanıcısı, grubu veya hizmet sorumlusu** olarak bırakın.
        3. **Seç** alanında tablodan uygulamayı girin.
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

## <a name="configure-the-export-to-data-lake-add-in"></a>Data Lake eklentisine Aktarmayı yapılandırma

LCS'yi kullanarak Data Lake eklentisini ortama aktarmak için bu adımları izleyin.

1. LCS'de oturum açın ve sonra sayfanın sağ tarafındaki ortam adının altında **Tüm Ayrıntılar**'ı seçin.
2. **Ortam eklentileri** bölümünde, **Yeni bir eklenti yükleyin**'i seçin.
3. **Data Lake'e dışarı aktar** eklentisini seçin.
4. Aşağıdaki değerleri girin.

    | Değer                                                              | Tanım |
    |--------------------------------------------------------------------|-------------|
    | Key Vault'un bulunduğu Azure Aboneliğinin Kiracı Kimliği | Depolama hesabı, uygulamalar ve anahtar kasalarının bulunduğu kiracının kimliğidir. Bu değeri edinmek için [Azure portalı](https://portal.azure.com) açın , **Azure Active Directory** öğesine gidin ve **Kiracı Kimliği** değerini kopyalayın. |
    | Key Vault'unuz için DNS adı belirtin                             | Anahtar kasasının DNS adı (ör. `https://customkeyvault.vault.azure.net/`). |
    | Depolama hesabının adını içeren gizli anahtarı girin   | **storage-account-name** |
    | Data Lake'e erişmek için kullanılacak Uygulama Kimliği için Gizli Anahtar Adı          | **app-id** |
    | Uygulama gizli anahtarı için gizli dizi adı                                  | **app-secret** |

5. Koşulları kabul edin ve ardından **Yükle**'yi seçin.

Eklenti birkaç dakika içinde yüklenir.

## <a name="configure-the-finance-insights-add-in"></a>Finance Insights eklentisini yapılandırma

> [!NOTE]
> Daha önce İçgörü edinme eklentisini yüklediyseniz, aşağıdaki yordamı gerçekleştirmeden önce bu eklentiyi kaldırın.

Bu adımları izleyip, Finance Insights eklentisini yükleyin.

1. LCS'de oturum açın ve sonra sayfanın sağ tarafındaki ortam adının altında **Tüm Ayrıntılar**'ı seçin.
2. **Ortam eklentileri** bölümünde, **Yeni bir eklenti yükleyin**'i seçin.
3. **Finance Insights** eklentisini seçin.
4. Koşulları kabul edin ve ardından **Yükle**'yi seçin.

Eklentinin yüklenmesi birkaç dakika sürebilir.

## <a name="feedback-and-support"></a>Geri bildirim ve destek

Geri bildirim sağlamak veya destek almak istiyorsanız lütfen [Finance Insights (Önizleme)](mailto:fiap@microsoft.com) ekibine e-posta gönderin.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
