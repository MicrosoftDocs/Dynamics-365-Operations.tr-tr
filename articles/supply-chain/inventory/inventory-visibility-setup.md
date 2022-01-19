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
ms.openlocfilehash: 26f8820fe707b8a2dff0dcc1a24884ef02e5616f
ms.sourcegitcommit: f5fd2122a889b04e14f18184aabd37f4bfb42974
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/10/2022
ms.locfileid: "7952508"
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

> [!NOTE]
> Şu anda desteklenen ülkeler ve bölgeler arasında Kanada (CCA, ECA), Amerika Birleşik Devletleri (WUS, EUS), Avrupa Birliği (NEU, WEU), Birleşik Krallık (SUK, WUK), Avustralya (EAU, SEAU), Japonya (EJP, WJP) ve Brezilya (SBR, SCUS) bulunmaktadır.

Bu ön koşullarla ilgili herhangi bir sorunuz varsa [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) adresinden Stok Görünürlüğü ürün takımıyla iletişime geçin.

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>Stok Görünürlüğü Eklentisini Yükleme

Eklentiyi yüklemeden önce Azure aboneliğiniz altında bir uygulama kaydedin ve Azure Active Directory (Azure AD) bölümüne bir istemci gizli anahtarı ekleyin. Yönergeler için bkz. [Uygulama kaydetme](/azure/active-directory/develop/quickstart-register-app) ve [İstemci gizli anahtarı ekleme](/azure/active-directory/develop/quickstart-register-app#add-a-certificate). Daha sonra ihtiyacınız olacağından **Uygulama (istemci) kimliği**, **İstemci gizli anahtarı** ve **Kiracı Kimliği** değerlerini not ettiğinizden emin olun.

Azure AD'ye uygulama kaydedip istemci gizli anahtarı ekledikten sonra şu adımları izleyerek Stok Görünürlüğü Eklentisi'ni yükleyin.

1. [LCS](https://lcs.dynamics.com/Logon/Index)'de oturum açın
1. Ana sayfada, ortamınızın dağıtıldığı projeyi seçin.
1. Proje sayfasında, eklentiyi yüklemek istediğiniz ortamı seçin.
1. Ortam sayfasında, **Power Platform tümleştirmesi** bölümünde aşağı kaydırarak **Ortam eklentileri** bölümünü bulun. Burada, Dataverse ortam adını bulabilirsiniz. Dataverse ortam adının Stok Görünürlüğü için kullanmak istediğiniz ad olduğunu onaylayın.

    > [!NOTE]
    > Şu anda yalnızca LCS'yi kullanarak oluşturulan Dataverse ortamları desteklenmektedir. Dataverse ortamınız başka bir yolla (örneğin, Power Apps yönetim merkezini kullanarak) oluşturulduysa ve Supply Chain Management ortamınıza bağlıysa eşleşme sorununu çözmek için ilk olarak [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) adresinden Stok Görünürlüğü ürün takımına başvurmanız gerekir. Ardından Stok Görünürlüğü'nü yükleyebilirsiniz.

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
1. Dataverse uygulamasında, sol gezinme bölmesinde **Uygulamalar** bölümünü seçin ve **Stok Görünürlüğü** Power Apps uygulamasının başarıyla yüklendiğini doğrulayın. **Uygulamalar** bölümü yoksa [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) adresinden Stok Görünürlüğü ürün takımıyla iletişime geçin.

> [!TIP]
> Kullanışlı kılavuzlar bulabileceğiniz, en son güncelleştirmelerinizi alabileceğiniz ve envanter görünürlüğünün kullanımıyla ilgili soruları alabileceğiniz, Stok Görünürlüğü Eklentisi kullanıcı grubuna katılmanızı öneririz. Katılmak için lütfen [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com)'da Stok Görünürlüğü ürün ekibine e-posta gönderin ve Supply Chain Management ortam kimliğinizi ekleyin.

> [!IMPORTANT]
> Birden fazla LCS ortamınız varsa her ortam için farklı bir Azure AD uygulaması oluşturun. Farklı ortamlar için Stok Görünürlüğü Eklentisini yüklemek üzere aynı uygulama kimliğini ve kiracı kimliğini kullanırsanız daha eski ortamlar için bir belirteç sorunu oluşur. Yalnızca en son yüklenen geçerlidir.

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>Stok Görünürlüğü Eklentisi'ni kaldırma

Stok Görünürlüğü Eklentisi'ni kaldırmak için LCS sayfasında **Kaldır**'ı seçin. Kaldırma işlemi, Stok Görünürlüğü Eklentisi'ni sonlandırır, LCS'den eklentinin kaydını iptal eder ve Stok Görünürlüğü Eklentisi veri önbelleğinde depolanan geçici verileri siler. Ancak Dataverse aboneliğinizde depolanan birincil stok verileri silinmez.

Dataverse aboneliğinizde depolanan stok verilerini kaldırmak için [Power Apps](https://make.powerapps.com) uygulamasını açın, gezinti çubuğunda **Ortam** seçeneğini belirleyin ve LCS ortamınızla bağlantılı Dataverse ortamını seçin. Ardından **Çözümler**'e gidin ve aşağıdaki beş çözümü şu sırayla silin:

1. Dynamics 365 çözümlerinde Stok Görünürlüğü uygulaması için bağlayıcı çözümü
1. Dynamics 365 FNO SCM Stok Görünürlüğü Uygulamalar Çözümü
1. Stok Hizmeti Yapılandırması
1. Tek Başına Stok Görünürlüğü
1. Dynamics 365 FNO SCM Stok Görünürlüğü Temel Çözümü

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
