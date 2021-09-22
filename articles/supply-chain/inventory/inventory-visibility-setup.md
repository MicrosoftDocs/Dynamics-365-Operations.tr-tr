---
title: Stok Görünürlüğü Eklentisini Yükleme
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management için Stok Görünürlüğü Eklentisi'nin nasıl yüklendiği açıklanmaktadır.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: b2b85f533a3318701ed08857b899cf9bdd103863
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474832"
---
# <a name="install-and-set-up-inventory-visibility"></a>Stok Görünürlüğü'nü yükleme ve ayarlama

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Bu konuda, Microsoft Dynamics 365 Supply Chain Management için Stok Görünürlüğü Eklentisi'nin nasıl yüklendiği açıklanmaktadır.

Stok Görünürlüğü Eklentisi'ni yüklemek için Microsoft Dynamics Lifecycle Services (LCS) kullanmanız gerekir. LCS, Finance and Operations uygulamalarınızın uygulama yaşam döngüsünü yönetmenize yardımcı olan bir ortam ve düzenli olarak güncelleştirilen bir dizi hizmet sağlayan bir işbirliği portalıdır.

Daha fazla bilgi için bkz. [Lifecycle Services kaynakları](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

## <a name="inventory-visibility-prerequisites"></a>Stok Görünürlüğü önkoşulları

Stok Görünürlüğü Eklentisi'ni yüklemeden önce aşağıdaki görevleri tamamlamanız gerekir:

- En az bir ortamın dağıtıldığı bir LCS uygulama projesi edinin.
- Eklentilerin ayarlanması için önkoşulların tamamlandığından emin olun. Bu önkoşullar hakkında bilgi için bkz. [Eklentilere genel bakış](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Stok Görünürlüğü, çift yazma bağlantısı gerektirmez.
- Aşağıdaki gerekli dosyaları almak için [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) adresinden Stok Görünürlüğü ürün takımına başvurun:

    - `InventoryServiceApplication.PackageDeployer.zip`
    - `Inventory Visibility Integration.zip` (Supply Chain Management'ın çalıştırdığınız bu sürümü 10.0.18 sürümünden daha eskiyse)

> [!NOTE]
> Şu anda desteklenen ülkeler ve bölgeler arasında Kanada (CCA, ECA), Amerika Birleşik Devletleri (WUS, EUS), Avrupa Birliği (NEU, WEU), Birleşik Krallık (SUK, WUK), Avustralya (EAU, SEAU), Japonya (EJP, WJP) ve Brezilya (SBR, SCUS) bulunmaktadır.

Bu önkoşullarla ilgili herhangi bir sorunuz varsa Stok Görünürlüğü ürün takımına başvurun.

## <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a>Ayarlama Dataverse

Dataverse'i Stok Görünürlüğü ile kullanılabilecek şekilde ayarlamak için Stok Görünürlüğü paketini dağıtmak üzere Package Deployer aracını kullanın. Aşağıdaki alt bölümlerde, her bir görevin nasıl tamamlanacağı açıklanmaktadır.

> [!NOTE]
> Şu anda yalnızca LCS'yi kullanarak oluşturulan Dataverse ortamları desteklenmektedir. Dataverse ortamınız başka bir yolla (örneğin, Power Apps yönetim merkezini kullanarak) oluşturulduysa ve Supply Chain Management ortamınıza bağlıysa eşleşme sorununu çözmek için ilk olarak Stok Görünürlüğü ürün takımına başvurmanız gerekir. Ardından Stok Görünürlüğü'nü yükleyebilirsiniz.

### <a name="migrate-from-an-old-version-of-the-dataverse-solution"></a>Dataverse çözümünün eski bir sürümünden geçiş yapma

Stok Görünürlüğü Dataverse çözümünün eski bir sürümünü yüklediyseniz bu yönergeleri kullanarak sürümünüzü güncelleştirin. İki durum vardır:

- **Durum 1:** Dataverse'i `Inventory Visibility Dataverse Solution_1_0_0_2_managed.zip` çözümünü içeri aktararak el ile ayarladıysanız şu adımları izleyin:

    1. Aşağıdaki üç dosyayı indirin:

        - `Inventory Visibility Dataverse Solution_1_0_0_3_managed.zip`
        - `InventoryServiceBase_managed.cab`
        - `InventoryServiceApplication.PackageDeployer.zip`

    1. Şu adımları izleyerek `Inventory Visibility Dataverse Solution_1_0_0_3_managed.zip` ve `InventoryServiceBase_managed.cab` dosyalarını el ile Dataverse'e içeri aktarın:

        1. Dataverse ortamınızın URL'sini açın.
        1. **Çözümler** sayfasını açın.
        1. **İçe aktar**'ı seçin.

    1. `InventoryServiceApplication.PackageDeployer.zip` paketini dağıtmak için Package Deployer aracını kullanın. Yönergeler için daha sonra bu konudaki [Paketi dağıtmak için Package Deployer aracını kullanma](#deploy-package) bölümüne bakın.

- **Durum 2:** Dataverse'i eski `.*PackageDeployer.zip` paketini yüklemeden önce Package Deployer aracını kullanarak ayarladıysanız `InventoryServiceApplication.PackageDeployer.zip` dosyasını indirin ve güncelleştirme işlemi yapın. Yönergeler için [Paketi dağıtmak için Package Deployer aracını kullanma](#deploy-package) bölümüne bakın.

### <a name="use-the-package-deployer-tool-to-deploy-the-package"></a><a name="deploy-package"></a>Paketi dağıtmak için Package Deployer aracını kullanma

1. Geliştirici araçlarını, [NuGet'ten araçları indirme](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget) bölümünde açıklandığı şekilde yükleyin.
1. Aşağıdaki adımları izleyerek Teams grubundan indirdiğiniz `InventoryServiceApplication.PackageDeployer.zip` dosyasının engelini kaldırın:

    1. Dosyayı seçin ve basılı tutun (veya sağ tıklayın) ve ardından **Özellikler**'i seçin.
    1. **Özellikler** iletişim kutusunda, **Genel** sekmesinde, **Güvenlik** bölümünü bulun, **Engellemeyi Kaldır**'ı seçin ve değişikliği uygulayın. **Genel** sekmesinde **Güvenlik** bölümü yoksa dosya engelli değildir. Bu durumda, sonraki adıma geçin.

    ![İndirilen dosyanın engellemesini kaldırma](media/unblock-file.png "İndirilen dosyanın engellemesini kaldırma")

1. Aşağıdaki öğeleri bulmak için `InventoryServiceApplication.PackageDeployer.zip` dosyasının sıkıştırmasını açın:

    - `InventoryServiceApplication` klasörü
    - `[Content_Types].xml` dosyası
    - `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll` dosyası

1. Bu öğelerin her birini `.\Tools\PackageDeployment` dizinine kopyalayın. (Bu dizin, geliştirici araçlarını yüklediğinizde oluşturulmuştur.)
1. `.\Tools\PackageDeployment\PackageDeployer.exe` dosyasını çalıştırın ve çözümleri içeri aktarmak için ekrandaki yönergeleri izleyin.

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>Stok Görünürlüğü Eklentisini Yükleme

Eklentiyi yüklemeden önce Azure aboneliğiniz altında bir uygulama kaydedin ve Azure Active Directory (Azure AD) bölümüne bir istemci gizli anahtarı ekleyin. Yönergeler için bkz. [Uygulama kaydetme](/azure/active-directory/develop/quickstart-register-app) ve [İstemci gizli anahtarı ekleme](/azure/active-directory/develop/quickstart-register-app#add-a-certificate). Daha sonra ihtiyacınız olacağından **Uygulama (istemci) kimliği**, **İstemci gizli anahtarı** ve **Kiracı Kimliği** değerlerini not ettiğinizden emin olun.

Azure AD'ye uygulama kaydedip istemci gizli anahtarı ekledikten sonra şu adımları izleyerek Stok Görünürlüğü Eklentisi'ni yükleyin.

1. [LCS](https://lcs.dynamics.com/Logon/Index)'de oturum açın
1. Ana sayfada, ortamınızın dağıtıldığı projeyi seçin.
1. Proje sayfasında, eklentiyi yüklemek istediğiniz ortamı seçin.
1. Ortam sayfasında, **Power Platform tümleştirmesi** bölümünde aşağı kaydırarak **Ortam eklentileri** bölümünü bulun. Burada, Dataverse ortam adını bulabilirsiniz.
1. **Ortam eklentileri** bölümünde, **Yeni bir eklenti yükleyin**'i seçin.

    ![LCS'deki ortam sayfası](media/inventory-visibility-environment.png "LCS'deki ortam sayfası")

1. **Yeni eklenti yükleyin** bağlantısını seçin. Kullanılabilir eklentilerin bir listesi görüntülenir.
1. Listede, **Stok Görünürlüğü**'nü seçin.
1. Ortamınız için aşağıdaki alanları ayarlayın:

    - **AAD uygulama (istemci) kimliği**: Daha önce oluşturup not ettiğiniz Azure AD uygulama kimliğini girin.
    - **AAD kiracı kimliği**: Daha önce not ettiğiniz kiracı kimliğini girin.

    ![Eklenti sayfasını ayarlama](media/inventory-visibility-setup.png "Eklenti sayfasını ayarlama")

1. **Hüküm ve koşullar** onay kutusunu seçerek hüküm ve koşulları kabul edin.
1. **Yükle**'yi seçin. Eklentinin durumu **Yükleniyor** olarak gösterilir. Yükleme tamamlandığında sayfayı yenileyin. Durum **Yüklendi** olarak değişecektir.

> [!IMPORTANT]
> Birden fazla LCS ortamınız varsa her ortam için farklı bir Azure AD uygulaması oluşturun. Farklı ortamlar için Stok Görünürlüğü Eklentisini yüklemek üzere aynı uygulama kimliğini ve kiracı kimliğini kullanırsanız daha eski ortamlar için bir belirteç sorunu oluşur. Yalnızca en son yüklenen geçerlidir.

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>Stok Görünürlüğü Eklentisi'ni kaldırma

Stok Görünürlüğü Eklentisi'ni kaldırmak için LCS sayfasında **Kaldır**'ı seçin. Kaldırma işlemi, Stok Görünürlüğü Eklentisi'ni sonlandırır, LCS'den eklentinin kaydını iptal eder ve Stok Görünürlüğü Eklentisi veri önbelleğinde depolanan geçici verileri siler. Ancak Dataverse aboneliğinizde depolanan birincil stok verileri silinmez.

Dataverse aboneliğinizde depolanan stok verilerini kaldırmak için [Power Apps](https://make.powerapps.com) uygulamasını açın, gezinti çubuğunda **Ortam** seçeneğini belirleyin ve LCS ortamınızla bağlantılı Dataverse ortamını seçin. Ardından **Çözümler**'e gidin ve aşağıdaki beş çözümü silin:

- Dynamics 365 çözümlerinde Stok Görünürlüğü uygulaması için bağlayıcı çözümü
- Dynamics 365 FNO SCM Stok Görünürlüğü Uygulamalar Çözümü
- Stok Hizmeti Yapılandırması
- Tek Başına Stok Görünürlüğü
- Dynamics 365 FNO SCM Stok Görünürlüğü Temel Çözümü

Bu çözümler silindikten sonra tablolarda depolanan veriler de silinir.

## <a name="set-up-inventory-visibility-in-supply-chain-management"></a><a name="setup-dynamics-scm"></a>Supply Chain Management uygulamasında Stok Görünürlüğü'nü ayarlama

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>Stok Görünürlüğü tümleştirme paketini dağıtma

Supply Chain Management sürüm 10.0.17 veya önceki bir sürümünü çalıştırıyorsanız paket dosyasını almak için [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) adresinden Stok Görünürlüğü yerleşik destek ekibine başvurun. Ardından LCS'de paketi dağıtın.

> [!NOTE]
> Dağıtım sırasında bir sürüm uyuşmazlığı hatası oluşursa X++ projesini geliştirme ortamınıza el ile içeri aktarmanız gerekir. Daha sonra, dağıtılabilir paketi geliştirme ortamınızda oluşturun ve üretim ortamınızda dağıtın.
>
> Kod, Supply Chain Management sürüm 10.0.18'e dahildir. Bu sürümü veya sonraki bir sürümünü çalıştırıyorsanız dağıtım gerekli değildir.

Supply Chain Management ortamınızda aşağıdaki özelliklerin açık olduğundan emin olun. (Varsayılan olarak bunlar açıktır.)

| Özellik açıklaması | Kod sürümü | Sınıfı değiştirme |
|---|---|---|
| InventSum tablosunda stok boyutlarını kullanmayı etkinleştirme veya devre dışı bırakma      | 10.0.11 | InventUseDimOfInventSumToggle      |
| InventSumDelta tablosunda stok boyutlarını kullanmayı etkinleştirme veya devre dışı bırakma | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>Stok Görünürlüğü tümleştirmesini kurma

Eklentiyi yükledikten sonra aşağıdaki adımları uygulayarak Supply Chain Management sisteminizi eklentiyle çalışmaya hazırlayın.

1. Supply Chain Management'ta **[Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** çalışma alanını açın ve aşağıdaki özellikleri açın:
    - *Stok Görünürlüğü Tümleştirmesi*: Gereklidir.
    - *Rezervasyon denkleştirme ile Stok Görünürlüğü tümleştirmesi*: Önerilir ancak isteğe bağlıdır. Sürüm 10.0.22 veya sonraki bir sürüm gereklidir. Daha fazla bilgi için bkz. [Stok Görünürlüğü rezervasyonları](inventory-visibility-reservations.md).

1. **Stok Yönetimi \> Ayar \> Stok Görünürlüğü Tümleştirme parametreleri**'ne gidin.
1. **Genel** sekmesini açın ve aşağıdaki ayarları yapın:
    - **Stok Görünürlüğü uç noktası**: Stok Görünürlüğü'nü çalıştırdığınız ortamın URL'sini girin. Daha fazla bilgi için bkz. [Hizmet uç noktasını bulma](inventory-visibility-configuration.md#get-service-endpoint).
    - **Tek bir istekteki maksimum kayıt sayısı**: Tek bir isteğe dahil edilecek maksimum kayıt sayısı olarak ayarlayın. 1000'den küçük veya 1000'e eşit bir pozitif tamsayı girmeniz gerekir. Varsayılan değer 512'dır. Microsoft Desteği'nden önerilmediği veya değiştirmeniz gerektiğinden emin olmadığınız sürece varsayılan değeri korumanızı kesinlikle öneririz.

1. İsteğe bağlı *Rezervasyon denkleştirme ile Stok Görünürlüğü tümleştirmesi* özelliğini etkinleştirdiyseniz **Reservasyon denkleştirme** sekmesini açın ve aşağıdaki ayarları yapın:
    - **Rezervasyon denkleştirmeyi etkinleştir**: Bu işlevi etkinleştirmek için *Evet* olarak ayarlayın.
    - **Rezervasyon denkleştirme değiştirici**: Stok Görünürlüğü'nde yapılan rezervasyonları denkleştirecek stok hareketi durumunu seçin. Bu ayar, denkleştirme işlemlerini tetikleyen sipariş işleme aşamasını belirler. Aşama, siparişin stok hareketi durumuna göre izlenir. Aşağıdakilerden birini seçin:
        - *Siparişte*: *Harekette* durumu için sipariş oluşturulduğunda bir denkleştirme isteği gönderir. Denkleştirme miktarı, oluşturulan siparişin miktarıdır.
        - *Rezerve edilmiş*: *Rezerve edilmiş siparişli hareket* durumu için sipariş, rezerve edildiğinde, alındığında, sevk irsaliyesi deftere nakledildiğinde veya faturalandığında bir denkleştirme isteği gönderir. İstek, belirtilen işlem gerçekleştiğinde ilk adım için yalnızca bir kez tetiklenir. Denkleştirme miktarı, ilgili sipariş satırında stok hareketi durumunun *Siparişte* yerine *Siparişli rezerve miktar* (veya sonraki durum) olarak değiştirildiği miktardır.

1. **Stok Yönetimi \> Periyodik \> Stok Görünürlüğü Tümleştirmesi**'ne gidin ve işi etkinleştirin. Supply Chain Management'taki tüm stok değişikliği olayları artık Stok Görünürlüğü'ne nakledilecektir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
