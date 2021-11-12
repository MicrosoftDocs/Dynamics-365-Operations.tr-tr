---
title: LBD kullanarak özel donanımda uç ölçek birimleri dağıtma (Önizleme)
description: Bu konu, yerel iş verilerini (LBD) temel alan özel donanım ve dağıtım kullanarak şirket içi kenar ölçek birimlerinin nasıl sağlanması gerektiğini açıklamaktadır.
author: cabeln
ms.date: 04/22/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 0ebbdaab9d6f040497d3158db2712e102b6e9aa8
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678993"
---
# <a name="deploy-edge-scale-units-on-custom-hardware-using-lbd-preview"></a>LBD kullanarak özel donanımda uç ölçek birimleri dağıtma (Önizleme)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)] <!--KFM: Until 11/1/2021 -->

Kenar ölçek birimleri, tedarik zinciri yönetimi için dağıtılmış karma topolojide önemli bir rol oynar. Karma topolojide, iş yüklerini Supply Chain Management bulut merkezi ile bulutta veya kenardaki ek ölçek birimleri arasında dağıtabilirsiniz.

Kenar ölçek birimleri yerel iş verileri (LBD) [yerinde ortam](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md) oluşturularak dağıtılabilir ve sonra Supply Chain Management için dağıtılmış karma topolojiniz içinde bir ölçek birimi olarak çalışacak şekilde konfigüre edilebilir. Bu, şirket içi LBD ortamını bulutta bir merkez olarak çalışacak şekilde yapılandırılmış olan bir Supply Chain Management ortamı ile ilişkilendirerek elde edilir.  

Kenar ölçek birimleri şu anda önizlemededir. Bu nedenle, yalnızca [önizleme koşullarına](https://aka.ms/scmcnepreviewterms) göre bu tür bir ortamı kullanabilirsiniz.

Bu konu, şirket içi bir LBD ortamının kenar ölçek birimi olarak nasıl ayarlanacağını ve sonra da bir merkez ile nasıl ilişkilendirileceğini açıklar.

## <a name="deployment-overview"></a>Dağıtıma genel bakış

Dağıtım adımlarına genel bakış.

1. **LBD projenizde, Microsoft Dynamics Lifecycle Services (LCS) içinde LBD yuvasını etkinleştirin.**

    Önizleme sırasında, LBD uç ölçek birimleri varolan LBD müşterilerini hedefleyin. Yalnızca belirli müşteri durumlarında ek 60 günlük sınırlı LBD korumalı alan yuvası sağlanacaktır.

1. **Bir LBD ortamını *boş* bir veritabanı ile ayarlayın ve dağıtın.**

    En son topolojiyle LBD ortamını ve boş bir veritabanını dağıtmak için LCS kullanın. Daha fazla bilgi için, bu konunun ilerisinde yer alan [Boş veritabanıyla LBD ortamı ayarlama ve dağıtma](#set-up-deploy) başlığına bakın. Merkez ve ölçek birimi ortamlarında, Supply Chain Management sürüm 10.0.19 platform güncelleştirmesi 43 veya üstünü ile kullanmalısınız.

1. **Hedef paketleri LCS içindeki LBD projesi varlıklarına yükleyin.**

    Merkez ve kenar ölçek birimi boyunca kullandığınız uygulama, platform ve özelleştirme paketlerini hazırlayın. Daha fazla bilgi için, bu konunun ilerleyen bölümlerindeki [LCS'de LBD proje varlıklarına hedef paketlerini yükleme](#upload-packages) başlığına bakın.

1. **LBD ortamına hedef paketleri ile hizmet verme.**

    Bu adım, aynı yapı ve özelleştirmelerin merkeze ve bağlı bileşene dağıtılmasını sağlar. Daha fazla bilgi için bu konunun ilerleyen bölümlerindeki [Hedef paketlerle LBD ortamında hizmet verme](#service-target-packages) başlığına bakın.

1. **Ölçek birimi konfigürasyonunu ve iş yükü atamasını tamamlayın.**

    Daha fazla bilgi için, bu konunun ilerleyen bölümlerindeki [LBD kenar ölçek birimini bir merkez bölümüne atama](#assign-edge-to-hub) konusuna bakın.

Bu konunun kalan bölümleri, bu adımları tamamlama hakkında ayrıntı verir.

## <a name="set-up-and-deploy-an-lbd-environment-with-an-empty-database"></a><a name="set-up-deploy"></a>Bir LBD ortamını boş bir veritabanı ile ayarlayın ve dağıtın

Bu adım, işlevsel LBD ortamı oluşturur. Ancak, ortamın merkez ortamıyla aynı uygulama ve platform sürümlerine sahip olması gerekmez. Ek olarak, özelleştirmeler eksik ve henüz bir ölçek birimi olarak çalışacak şekilde etkinleştirilmemiş.

1. [Şirket içi ortamları ayarlama ve dağıtma (Platform güncelleştirmesi 41 ve sonrası)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md) bölümündeki talimatları izleyin. Merkez ve ölçek birimi ortamlarında, Supply Chain Management sürüm 10.0.19 platform güncelleştirmesi 43 veya üstünü ile kullanmalısınız

    > [!IMPORTANT]
    > Bu konudaki adımları uygulamadan **önce** bu bölümün geri kalanını okuyun.

1. Konfigürasyonunuzu \\ConfigTemplate.xml dosyasında açıklamadan önce, aşağıdaki kodu çalıştırın:

    ```powershell
    .\Configure-ScriptsForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > Bu komut dosyası, kenar ölçek birimleri dağıtımı için gerekli olmayan tüm yapılandırmaları kaldıracaktır.

1. [Veritabanlarını yapılandırma](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) bölümünde açıklandığı gibi boş veri içeren bir veritabanı kurun. Bu adım için boş data.bak dosyasını kullanın.
1. Dağıtım öncesi betik kurulumu. Daha fazla bilgi için bkz. [Yerel aracı dağıtım öncesi ve dağıtım sonrası kodları](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md).

    1. **Altyapı Komut Dosyalarındaki** **ScaleUnit** klasörünün içeriğini, ortamda kurulmuş olan aracı dosyası depolama paylaşımında bulunan **Komut dosyaları** klasörüne kopyalayın. Tipik bir yol şöyledir: \\\\lbdiscsi01\\agent\\Scripts.
    2. Gerekli parametreleri kullanarak kodları çağırabilecek **PreDeployment.ps1** kodunu oluşturun. Dağıtım öncesi betiği, aracı dosya depolama paylaşımında **Komut dosyaları** klasörüne konulmalıdır. Aksi durumda çalıştırılamaz. Tipik bir yol şöyledir: \\\\lbdiscsi01\\agent\\Scripts\\PreDeployment.ps1.

        PreDeployment.ps1 komut dosyasının içeriği aşağıdaki örneğe benzeyecektir.

        ```powershell
        $agentShare = '\\lbdiscsi01\agent'
        
        Write-Output "AgentShare is set to $agentShare" 
        & $agentShare\Scripts\Configure-CloudandEdge.ps1 -AgentShare $agentShare -InstanceId '@A' -DatabaseServer 'lbdsqla01.contoso.com' -DatabaseName 'AXDB'
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

## <a name="upload-target-packages-into-lbd-project-assets-in-lcs"></a><a name="upload-packages"></a>Hedef paketleri LCS içindeki LBD projesi varlıklarına yükleyin

Bu adım, uygulama sürümü, platform sürümü ve LBD ölçeği birim ortamınıza geçiş yapılacak özelleştirmeleri hazırlar.

1. Aynı birleşik uygulama/platform paketini merkez ortamına uygulanmış LCS şirket içi projenin varlık kitaplığına yükleyin.
1. Merkez ortamına uygulanmış özel dağıtılabilir paketin bir kopyasını alın ve bunu LCS şirket içi projenin varlık kitaplığına yükleyin.

## <a name="service-the-lbd-environment-with-target-packages"></a><a name="service-target-packages"></a>LBD ortamına hedef paketleri ile hizmet verme

Bu adım, LBD ölçeği birim ortamınızdaki uygulama sürümü, platform sürümü ve özelleştirmeleri merkez ile hizalar.

1. Önceki adımda karşıya yüklediğiniz birleşik uygulama/platform paketine sahip LBD ortamına hizmet verme.
1. Önceki adımda karşıya yüklediğiniz özel dağıtılabilir pakete sahip LBD ortamına hizmet verme.

    ![Koru > LCS'de güncelleştirmeleri uygulayı seçme.](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "Koru > LCS'de güncelleştirmeleri uygulayı seçme")

    ![Özelleştirme paketinizi seçme.](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "Özelleştirme paketinizi seçme")

## <a name="assign-your-lbd-edge-scale-unit-to-a-hub"></a><a name="assign-edge-to-hub"></a>LBD kenar ölçek birimini merkeze atayın

Kenar ölçek birimleri hala önizlemede olduğundan, LBD kenar ölçek birimini bir merkeze atamak için, GitHub'da bulunan [ölçek birim dağıtımı ve konfigürasyon araçlarını](https://github.com/microsoft/SCMScaleUnitDevTools) kullanmanız gerekir. İşlem, LBD yapılandırmasının kenar ölçek birimi olarak işlev görmesine ve merkez ile ilişkilenmesine olanak tanır. İşlem, tek bir kutu geliştirme ortamını yapılandırmaya benzer.

1. [SCMScaleUnitDevTools](https://github.com/microsoft/SCMScaleUnitDevTools/releases) en son sürümünü karşıdan yükleyin ve dosyanın içeriğini açın.
1. `UserConfig.sample.xml` dosyasının bir kopyasını oluşturun ve adını `UserConfig.xml` koyun.
1. Azure AD kiracınızda, [Ölçek birimi ve iş yükleri için dağıtım kılavuzu](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide#aad-application-registrations) bölümünde açıklandığı şekilde bir Microsoft Azure Active Directory (Azure AD) uygulaması oluşturun.
    1. Oluşturduktan sonra, merkeziniz üzerindeki Azure AD uygulamaları formuna (SysAADClientTable) gidin.
    1. Yeni bir giriş oluşturun ve **İstemci Kimliği**'ni oluşturduğunuz uygulamanın kimliğine ayarlayın. **Ad**'ı *ScaleUnits* olarak ve **Kullanıcı Kimliğini** *Yönetici* olarak ayarlayın.

1. [Ölçek birimi ve iş yükleri için dağıtım kılavuzu](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide#adfs-application-registrations) bölümünde açıklandığı üzere Active Directory Federasyon Hizmeti (AD FS) uygulaması oluşturun.
    1. Oluşturduktan sonra, kenar ölçek biriminiz üzerindeki Azure AD uygulamaları formuna (SysAADClientTable) gidin.
    1. Yeni bir giriş oluşturun ve **İstemci Kimliği**'ni oluşturduğunuz uygulamanın kimliğine ayarlayın. **Kullanıcı Kimliğini** *Yönetici* olarak ayarlayın.

1. `UserConfig.xml` dosyasını değiştirin.
    1. `InterAOSAADConfiguration` bölümünde, daha önce oluşturduğunuz Azure AD uygulamasındaki bilgileri girin.
        - `AppId` öğesinde, Azure uygulamasının uygulama kodunu girin.
        - `AppSecret` öğesinde, Azure uygulamasının uygulama gizli dizisini girin.
        - `Authority` öğesi, kiracınıza ait güvenlik yetkilisini belirten URL'yi içermelidir.

        ```xml
        <InterAOSAADConfiguration>
            <AppId>8dab14f6-97b1-48e3-b51b-350b45f6ede5</AppId>
            <AppSecret>k6em-_7.lopty56TGUedDTVhtER-j_6anY1</AppSecret>
            <Authority>https://login.windows.net/contoso.onmicrosoft.com</Authority>
        </InterAOSAADConfiguration>
        ```

    1. `ScaleUnitConfiguration` bölümünün altında, birinci `ScaleUnitInstance` için `AuthConfiguration` bölümünü değiştirin.
        - `AppId` öğesinde, Azure uygulamasının uygulama kodunu girin.
        - `AppSecret` öğesinde, Azure uygulamasının uygulama gizli dizisini girin.
        - `Authority` öğesi, kiracınıza ait güvenlik yetkilisini belirten URL'yi içermelidir.

        ```xml
        <AuthConfiguration>
            <AppId>8dab14f6-97b1-48e3-b51b-350b45f6ede5</AppId>
            <AppSecret>k6em-_7.lopdz.6d3DTVOtf9Lo-j_6anY1</AppSecret>
            <Authority>https://login.windows.net/contoso.onmicrosoft.com</Authority>
        </AuthConfiguration>
        ```

    1. Ek olarak, aynı bu `ScaleUnitInstance` için şu değerleri ayarlayın:
        - `Domain` öğesinde merkezinizin URL'sini belirtin. Örneğin: `https://cloudhub.sandbox.operations.dynamics.com/`
        - `EnvironmentType` öğesinde, `LCSHosted` değerinin ayarlandığından emin olun.

    1. `ScaleUnitConfiguration` bölümünün altında, ikinci `ScaleUnitInstance` için `AuthConfiguration` bölümünü değiştirin.
        - `AppId` öğesinde, AD FS uygulamasının uygulama kodunu girin.
        - `AppSecret` öğesinde, ADFS uygulamasının uygulama gizli dizisini girin.
        - `Authority` öğesi, AD FS örneğinizin URL'sini içermelidir.

        ```xml
        <AuthConfiguration>
            <AppId>26b16f25-21d8-4d36-987b-62df292895aa</AppId>
            <AppSecret>iZFfObgI6lLtY9kEbBjEFV98NqI5_YZ0e5SBcWER</AppSecret>
            <Authority>https://adfs.contoso.com/adfs</Authority>
        </AuthConfiguration>
        ```

    1. Ek olarak, aynı bu `ScaleUnitInstance` için şu değerleri ayarlayın:
        - `Domain` öğesinde, kenar ölçek biriminizin URL'sini belirtin. Örneğin: https://ax.contoso.com/
        - `EnvironmentType` öğesinde, LBD değerinin ayarlandığından emin olun.
        - `ScaleUnitId` öğesinde, `Configure-CloudandEdge.ps1` dağıtım öncesi betiğini yapılandırılırken `InstanceId`'de belirttiğiniz aynı değeri girin.

        > [!NOTE]
        > Varsayılan kimliği (@A) kullanmazsanız, İş yükleri bölümü altındaki tüm ConfiguredWorkload için ScaleUnitId'yi güncelleştirin.

1. PowerShell'i açın ve `UserConfig.xml` dosyasını içeren klasöre gidin.

1. Aracı bu komutla çalıştırın.

    ```powershell
    .\CLI.exe
    ```

    > [!NOTE]
    > Her eylemden sonra aracı yeniden başlatmak zorunda kalırsınız.

1. Araçta, **2. İş yükü kurulumu için ortamları hazırla** seçeneğini belirleyin. Sonra aşağıdaki adımları çalıştırın:
    1. **1. Merkezi hazırlayın** seçeneğini belirleyin.
    1. **2. Ölçek Birimini hazırlayın** seçeneğini belirleyin.

    > [!NOTE]
    > Bu komutu temiz bir yüklemeden çalıştırmıyorsanız ve başarısız olduysa, aşağıdaki eylemleri gerçekleştirin:
    >
    > - `aos-storage` klasöründeki tüm klasörleri kaldırın (`GACAssemblies` hariç).
    > - İş veritabanınızda aşağıdaki SQL komutunu çalıştırın (AXDB):
    >
    > ```sql 
    > delete from storagefoler
    > ```

1. İş veritabanınızda aşağıdaki SQL komutlarını çalıştırın (AXDB):

    ```sql
    delete from FEATUREMANAGEMENTMETADATA
    delete from FEATUREMANAGEMENTSTATE
    delete from NUMBERSEQUENCESCOPE
    ```

1. Değişiklik izlemenin iş veritabanınızda (AXDB) etkinleştirildiğini doğrulayın
    1. SQL Server Management Studio'yu (SSMS) başlatın.
    1. İş veritabanına (AXDB) sağ tıklatın ve özellikleri seçin.
    1. Açılan pencerede, **Değişiklik İzleme**'yi seçin ve aşağıdaki ayarları yapın:

        - **Değişiklik İzleme:** *Doğru*
        - **Saklama Süresi:** *7*
        - **Saklama Birimi:** *Gün*
        - **Otomatik Temizleme:** *Doğru*

1. Araçta **3. İş yüklerini yükleyin** seçeneğini belirleyin. Sonra aşağıdaki adımları çalıştırın:
    1. **1. Merkeze kur** seçeneğini belirleyin.
    1. **2. Ölçek Birimine yükleyin** seçeneğini belirleyin.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
