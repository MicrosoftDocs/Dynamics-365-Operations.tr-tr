---
title: LBD kullanarak özel donanımda uç ölçek birimlerini dağıtma
description: Bu makale, yerel iş verilerini (LBD) temel alan özel donanım ve dağıtım kullanarak şirket içi kenar ölçek birimlerinin nasıl sağlanması gerektiğini açıklamaktadır.
author: Mirzaab
ms.date: 01/24/2022
ms.topic: article
ms.prod: dynamics-365
ms.service: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 794de8c0d77949789e4046418ac2b55dba1bee02
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882764"
---
# <a name="deploy-edge-scale-units-on-custom-hardware-using-lbd"></a>LBD kullanarak özel donanımda uç ölçek birimleri dağıtma

[!include [banner](../includes/banner.md)]

Kenar ölçek birimleri, tedarik zinciri yönetimi için dağıtılmış karma topolojide önemli bir rol oynar. Karma topolojide, iş yüklerini Supply Chain Management bulut merkezi ile bulutta veya kenardaki ek ölçek birimleri arasında dağıtabilirsiniz.

Kenar ölçek birimleri yerel iş verileri (LBD) [yerinde ortam](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md) oluşturularak dağıtılabilir ve sonra Supply Chain Management için dağıtılmış karma topolojiniz içinde bir ölçek birimi olarak çalışacak şekilde konfigüre edilebilir. Bu, şirket içi LBD ortamını bulutta bir merkez olarak çalışacak şekilde yapılandırılmış olan bir Supply Chain Management ortamı ile ilişkilendirerek elde edilir.  

Bu makale, şirket içi bir LBD ortamının kenar ölçek birimi olarak nasıl ayarlanacağını ve sonra da bir merkez ile nasıl ilişkilendirileceğini açıklar.

## <a name="infrastructure-considerations"></a>Altyapı ile ilgili hususlar

Uç ölçek birimleri, şirket içi ortamlarda çalışır, böylece altyapı gereksinimleri oldukça benzerdir. Ancak, dikkat edilmesi gereken belirli farklılıklar vardır:

- Uç ölçek birimleri Financial Reporting'i kullanmaz, bu nedenle Financial Reporting düğümleri gerekmez.
- Üretim ve depolama iş yükleri işlem açısından yoğun değildir, bu nedenle işlem gücünü AOS düğümlerine uygun şekilde boyutlandırmayı düşünün.

## <a name="deployment-overview"></a>Dağıtıma genel bakış

Dağıtım adımlarına genel bakış.

1. **LBD projenizde, Microsoft Dynamics Lifecycle Services (LCS) içinde LBD yuvasını etkinleştirin.**

1. **Bir LBD ortamını *boş* bir veritabanı ile ayarlayın ve dağıtın.**

    En son topolojiyle LBD ortamını ve boş bir veritabanını dağıtmak için LCS kullanın. Daha fazla bilgi için bu makalenin ilerisinde yer alan [Boş veritabanıyla LBD ortamı ayarlama ve dağıtma](#set-up-deploy) başlığına bakın. Merkez ve ölçek birimi ortamlarında, Supply Chain Management sürüm 10.0.21 veya üstü ile kullanmalısınız.

1. **Hedef paketleri LCS içindeki LBD projesi varlıklarına yükleyin.**

    Merkez ve kenar ölçek birimi boyunca kullandığınız uygulama, platform ve özelleştirme paketlerini hazırlayın. Daha fazla bilgi için, bu makalenin ilerleyen bölümlerindeki [LCS'de LBD proje varlıklarına hedef paketlerini yükleme](#upload-packages) başlığına bakın.

1. **LBD ortamına hedef paketleri ile hizmet verme.**

    Bu adım, aynı yapı ve özelleştirmelerin merkeze ve bağlı bileşene dağıtılmasını sağlar. Daha fazla bilgi için bu makalenin ilerleyen bölümlerindeki [Hedef paketlerle LBD ortamında hizmet verme](#service-target-packages) başlığına bakın.

1. **Ölçek birimi konfigürasyonunu ve iş yükü atamasını tamamlayın.**

    Daha fazla bilgi için bu makalenin ilerleyen bölümlerindeki [LBD kenar ölçek birimini bir merkez bölümüne atama](#assign-edge-to-hub) konusuna bakın.

Bu makalenin kalan bölümleri, bu adımları tamamlama hakkında ayrıntı verir.

## <a name="set-up-and-deploy-an-lbd-environment-with-an-empty-database"></a><a name="set-up-deploy"></a>Bir LBD ortamını boş bir veritabanı ile ayarlayın ve dağıtın

Bu adım, işlevsel LBD ortamı oluşturur. Ancak, ortamın merkez ortamıyla aynı uygulama ve platform sürümlerine sahip olması gerekmez. Ek olarak, özelleştirmeler eksik ve henüz bir ölçek birimi olarak çalışacak şekilde etkinleştirilmemiş.

1. [Şirket içi ortamları ayarlama ve dağıtma (Platform güncelleştirmesi 41 ve sonrası)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md) bölümündeki talimatları izleyin. Merkez ve ölçek birimi ortamlarında, Supply Chain Management sürüm 10.0.21 veya üstü ile kullanmalısınız. Ek olarak, altyapı kodlarının sürüm 2.12.0 veya üstünü kullanmalısınız. 

    > [!IMPORTANT]
    > Bu makaledeki adımları uygulamadan **önce** bu bölümün geri kalanını okuyun.

1. Konfigürasyonunuzu \\ConfigTemplate.xml dosyasında açıklamadan önce, aşağıdaki kodu çalıştırın:

    ```powershell
    .\Configure-ScriptsForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > Bu komut dosyası, kenar ölçek birimleri dağıtımı için gerekli olmayan tüm yapılandırmaları kaldıracaktır.

1. [Veritabanlarını yapılandırma](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) bölümünde açıklandığı gibi boş veri içeren bir veritabanı kurun. Bu adım için boş data.bak dosyasını kullanın.
1. [Veritabanı yapılandırma](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) adımını tamamladıktan sonra, Ölçek Birimi ALM Düzenleyici veritabanını konfigüre etmek için aşağıdaki kodu çalıştırın.

    > [!NOTE]
    > [Veritabanı yapılandırma](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) adımı sırasında Financial Reporting veritabanını konfigüre etmeyin.

    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName EdgeScaleUnit
    ```

    Initialize-Database.ps1 kodu, aşağıdaki eylemleri gerçekleştirir:

    1. **ScaleUnitAlmDb** adlı boş bir veritabanı oluşturun.
    2. Kullanıcıları, aşağıdaki tabloyu temel alan veritabanı rolleriyle eşleyin.

        | Kullanıcı            | Tür | Veritabanı rolü |
        |-----------------|------|---------------|
        | svc-LocalAgent$ | gMSA | db\_owner     |

1. [Şirket içi ortamları ayarlama ve dağıtma (Platform güncelleştirmesi 41 ve sonrası)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md) bölümündeki talimatları izlemeye devam edin.
1. [AD FS yapılandırması](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) adımını tamamlandıktan sonra şu adımları izleyin:

    1. ALM Düzenleme hizmetinin Uygulama Nesne Sunucunuzla (AOS) iletişim kurmasını sağlayacak yeni bir Active Directory Federasyon Hizmetleri (AD FS) uygulaması oluşturun.

        ```powershell
        # Host URL is your DNS record\host name for accessing the AOS
        .\Create-ADFSServerApplicationForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -HostUrl 'https://ax.d365ffo.onprem.contoso.com'
        ```

    1. ALM Düzenleme Servisinin Ölçek Birim Yönetimi hizmeti ile iletişim kurmasını sağlayacak yeni bir Azure Active Directory (Azure AD) uygulaması oluşturun.

        ```powershell
        # Example .\Create-SumAADApplication.ps1 -ConfigurationFilePath ..\ConfigTemplate.xml -TenantId '6240a19e-86f1-41af-91ab-dbe29dbcfb95' -ApplicationDisplayName 'EdgeAgent-SUMCommunication-EN01'
        .\Create-SumAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                       -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                       -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
        ```

1. [Şirket içi ortamları ayarlama ve dağıtma (Platform güncelleştirmesi 41 ve sonrası)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md) bölümündeki talimatları izlemeye devam edin. Yerel aracının yapılandırmasını girmeniz gerektiğinde, Sınır Ölçek Birimi özelliklerinin etkin olmasını sağladığınızdan ve gerekli tüm parametreleri sağladığınızdan emin olun.

    ![Uç Ölçek Birimi özelliklerini etkinleştirme.](media/EnableEdgeScaleUnitFeatures.png "Uç Ölçek Birimi özelliklerini etkinleştirme.")

1. Ortamınızı LCS'den dağıtmadan önce dağıtım öncesi betik ayarlayın. Daha fazla bilgi için bkz. [Yerel aracı dağıtım öncesi ve dağıtım sonrası kodları](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md).

    1. **Altyapı Komut Dosyalarındaki** **ScaleUnit** klasörünün Configure-CloudAndEdge.ps1 betiğini, ortamda kurulmuş olan aracı dosyası depolama paylaşımında bulunan **Komut dosyaları** klasörüne kopyalayın. Tipik bir yol şöyledir: \\\\lbdiscsi01\\agent\\Scripts.
    2. Gerekli parametreleri kullanarak kodları çağırabilecek **PreDeployment.ps1** kodunu oluşturun. Dağıtım öncesi betiği, aracı dosya depolama paylaşımında **Komut dosyaları** klasörüne konulmalıdır. Aksi durumda çalıştırılamaz. Tipik bir yol şöyledir: \\\\lbdiscsi01\\agent\\Scripts\\PreDeployment.ps1.

        PreDeployment.ps1 komut dosyasının içeriği aşağıdaki örneğe benzeyecektir.

        ```powershell
        $agentShare = '\\lbdiscsi01\agent'
        
        Write-Output "AgentShare is set to $agentShare" 
        . $PSScriptRoot\Configure-CloudAndEdge.ps1 -AgentShare $agentShare -InstanceId '@A'
        ```

        > [!NOTE]
        > InstanceId parametresi yalnızca iki karakter olmalıdır. İlk karakter @, ikincisi ise İngiliz alfabesinde yer alan herhangi bir büyük harf olabilir.
        >
        > - Geçerli değerler:
        >   - @D
        >   - @X
        > - Geçerli olmayan değerler:
        >   - @a
        >   - @4
        >   - @#

1. Ortamı, kullanılabilen en son taban topolojisini kullanarak dağıtın.
1. Ortamı dağıttıktan sonra şu adımları izleyin:

    1. İş veritabanınızda aşağıdaki SQL komutlarını çalıştırın (AXDB).

        ```sql
        ALTER TABLE dbo.NUMBERSEQUENCETABLE ENABLE CHANGE_TRACKING WITH (TRACK_COLUMNS_UPDATED = ON)
        delete from NumberSequenceTable
        delete from NumberSequenceReference
        delete from NumberSequenceScope
        delete from FeatureManagementMetadata
        delete from FeatureManagementState
        delete from SysFeatureStateV0
        ```

    1. Eşzamanlı maksimum toplu iş oturumunu 4'ten fazla olan bir değerle artırın.

        ```sql
        Update batchserverconfig set maxbatchsessions = '<Replace with number of concurrent batch tasks you want>'
        ```

    1. Değişiklik izlemenin iş veritabanınızda (AXDB) etkinleştirildiğini doğrulayın.

        1. SQL Server Management Studio'yu (SSMS) açın.
        1. İş veritabanınızı (AXDB) seçin ve basılı tutun (veya sağ tıklayın) ve ardından **Özellikler**'i seçin.
        1. Görünen pencerede, **Değişiklik İzleme**'yi seçin ve aşağıdaki değerleri ayarların:

            - **Değişiklik İzleme:** *Doğru*
            - **Saklama Süresi:** *7*
            - **Saklama Birimi:** *Gün*
            - **Otomatik Temizleme:** *Doğru*

    1. Daha önce oluşturduğunuz AD FS uygulama kimliğini (Create-ADFSServerApplicationForEdgeScaleUnits.ps1 betiğini kullanarak), ölçek birimindeki Azure AD uygulamaları tablosuna ekleyin. Bu adımı kullanıcı arabirimi (UI) aracılığıyla el ile tamamlayabilirsiniz. Alternatif olarak, aşağıdaki kodu kullanarak veritabanı aracılığıyla tamamlayabilirsiniz.

        ```sql
        DECLARE @ALMOrchestratorId NVARCHAR(76) = '<Replace with the ADFS Application ID created in a previous step>';

        IF NOT EXISTS (SELECT TOP 1 1 FROM SysAADClientTable WHERE AADClientId = @ALMOrchestratorId)
        BEGIN
            INSERT INTO SysAADClientTable (AADClientId, UserId, Name, ModifiedBy, CreatedBy)
            VALUES (@ALMOrchestratorId, 'ScaleUnitManagement', 'Scale Unit Management', 'Admin', 'Admin');
        END
        ```

## <a name="set-up-an-azure-key-vault-and-an-azure-ad-application-to-enable-communication-between-scale-units"></a><a name="set-up-keyvault"></a>Ölçek birimleri arasındaki iletişimi etkinleştirmek için bir Azure Key Vault ve bir Azure AD uygulaması ayarlayın

1. Ortamınız dağıtıldıktan sonra, merkez ve ölçek birimi arasında güvenilir iletişimi sağlamak için ek bir Azure AD uygulaması oluşturun.

    ```powershell
    .\Create-SpokeToHubAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                          -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                          -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
    ```

1. Uygulamayı oluşturduktan sonra, bir gizli anahtar oluşturmanız ve bilgileri bir Azure Key Vault'a kaydetmeniz gerekir. Ek olarak, oluşturulan Azure AD uygulamasına erişim izni vermelisiniz, böylece anahtar kasasında depolanan gizli anahtarı alabilirler. Kolaylık olması için, aşağıdaki komut dosyası gereken tüm eylemleri otomatik olarak gerçekleştirecek.

    ```powershell
    .\Create-SpokeToHubAADAppSecrets.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                         -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                         -SubscriptionName '<Any subscription within your tenant>' `
                                         -ResourceGroupName '<Any resource group within your subscription>' `
                                         -KeyVaultName '<Any key vault within your resource group>' `
                                         -Location '<Any Azure location where Azure Key Vault is available>' `
                                         -LCSEnvironmentId '<The LCS environment ID of your deployed scale unit>' `
    ```

    > [!NOTE]
    > Belirtilen **KeyVaultName** değerine sahip hiçbir anahtar kasası yoksa, komut dosyası otomatik olarak bir tane oluşturur.

1. Oluşturduğunuz Azure AD uygulama kimliğini (Create-SpokeToHubAADApplication.ps1 komut dosyasını kullanırken) merkeziniz içindeki Azure AD uygulamaları tablosuna ekleyin. Bu adımı UI aracılığıyla el ile tamamlayabilirsiniz.

## <a name="upload-target-packages-into-lbd-project-assets-in-lcs"></a><a name="upload-packages"></a>Hedef paketleri LCS içindeki LBD projesi varlıklarına yükleyin

Bu adım, uygulama sürümü, platform sürümü ve LBD ölçeği birim ortamınıza geçiş yapılacak özelleştirmeleri hazırlar.

1. Aynı birleşik uygulama/platform paketini merkez ortamına uygulanmış LCS şirket içi projenin varlık kitaplığına yükleyin.
1. Merkez ortamına uygulanmış özel dağıtılabilir paketin bir kopyasını alın ve bunu LCS şirket içi projenin varlık kitaplığına yükleyin.

## <a name="service-the-lbd-environment-with-target-packages"></a><a name="service-target-packages"></a>LBD ortamına hedef paketleri ile hizmet verme

Bu adım, LBD ölçeği birim ortamınızdaki uygulama sürümü, platform sürümü ve özelleştirmeleri merkez ile hizalar.

1. Önceki adımda karşıya yüklediğiniz birleşik uygulama/platform paketine sahip LBD ortamına hizmet verme.
1. Önceki adımda karşıya yüklediğiniz özel dağıtılabilir pakete sahip LBD ortamına hizmet verme.

    ![Güncelleştirmeleri LCS'de uygulama.](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "Güncelleştirmeleri LCS'de uygulama")

    ![Özelleştirme paketinizi seçme.](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "Özelleştirme paketinizi seçme")

## <a name="assign-your-lbd-edge-scale-unit-to-a-hub"></a><a name="assign-edge-to-hub"></a>LBD kenar ölçek birimini merkeze atayın

Sınır Ölçek Birimi Yönetim Portalı aracılığıyla uç ölçek biriminizi konfigüre eder ve yönetirsiniz. Daha fazla bilgi için bkz. [Ölçek Birim Yöneticisi portalını kullanarak bulut ölçek birimlerini ve iş yüklerini yönetme](./cloud-edge-landing-page.md#scale-unit-manager-portal).

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
