---
title: Stok Görünürlüğü Eklentisini Yükleme
description: Bu makalede, Microsoft Dynamics 365 Supply Chain Management için Stok Görünürlüğü Eklentisi'nin nasıl yüklendiği açıklanmaktadır.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: c08568b14d7f5c79a1d3609107a88f905498ce2b
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762794"
---
# <a name="install-and-set-up-inventory-visibility"></a>Inventory Visibility'yi yükleme ve ayarlama

[!include [banner](../includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Supply Chain Management için Stok Görünürlüğü Eklentisi'nin nasıl yüklendiği açıklanmaktadır.

Stok Görünürlüğü Eklentisi'ni yüklemek için [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/v2) kullanmanız gerekir. Lifecycle Services, Finans ve Operasyon uygulamalarınızın uygulama yaşam döngüsünü yönetmenize yardımcı olan bir ortam ve düzenli olarak güncelleştirilen bir dizi hizmet sağlayan bir işbirliği portalıdır. Daha fazla bilgi için bkz. [Lifecycle Services kaynakları](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

> [!TIP]
> Kullanışlı kılavuzlar bulabileceğiniz, en son güncelleştirmelerinizi alabileceğiniz ve envanter görünürlüğünün kullanımıyla ilgili soruları alabileceğiniz, Stok Görünürlüğü Eklentisi kullanıcı grubuna katılmanızı öneririz. Katılmak için lütfen [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com)'da Stok Görünürlüğü ürün ekibine e-posta gönderin ve Supply Chain Management ortam kimliğinizi ekleyin.

## <a name="inventory-visibility-prerequisites"></a>Stok Görünürlüğü önkoşulları

Stok Görünürlüğü Eklentisi'ni yüklemeden önce aşağıdaki görevleri tamamlamanız gerekir:

- En az bir ortamın dağıtıldığı bir Lifecycle Services uygulama projesi edinin.
- Eklentilerin ayarlanması için önkoşulların tamamlandığından emin olun. Bu önkoşullar hakkında bilgi için bkz. [Eklentilere genel bakış](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Stok Görünürlüğü, çift yazma bağlantısı gerektirmez.

> [!NOTE]
> Şu anda desteklenen ülkeler ve bölgeler arasında Kanada (CCA, ECA), Amerika Birleşik Devletleri (WUS, EUS), Avrupa Birliği (NEU, WEU), Birleşik Krallık (SUK, WUK), Avustralya (EAU, SEAU), Japonya (EJP, WJP) ve Brezilya (SBR, SCUS) bulunmaktadır.

Bu ön koşullarla ilgili herhangi bir sorunuz varsa [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) adresinden Stok Görünürlüğü ürün takımıyla iletişime geçin.

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>Stok Görünürlüğü Eklentisini Yükleme

Eklentiyi yüklemeden önce Azure aboneliğiniz altında bir uygulama kaydedin ve Azure Active Directory (Azure AD) bölümüne bir istemci gizli anahtarı ekleyin. Yönergeler için bkz. [Uygulama kaydetme](/azure/active-directory/develop/quickstart-register-app) ve [İstemci gizli anahtarı ekleme](/azure/active-directory/develop/quickstart-register-app#add-a-certificate). Daha sonra ihtiyacınız olacağından **Uygulama (istemci) kimliği**, **İstemci gizli anahtarı** ve **Kiracı Kimliği** değerlerini not ettiğinizden emin olun.

> [!IMPORTANT]
> Birden fazla Lifecycle Services ortamınız varsa her biri için farklı bir Azure AD uygulaması oluşturun. Farklı ortamlar için Stok Görünürlüğü Eklentisini yüklemek üzere aynı uygulama kimliğini ve kiracı kimliğini kullanırsanız daha eski ortamlar için bir belirteç sorunu oluşur. Sonuç olarak, yalnızca son yükleme geçerli olacak.

Azure AD'ye uygulama kaydedip istemci gizli anahtarı ekledikten sonra şu adımları izleyerek Stok Görünürlüğü Eklentisi'ni yükleyin.

1. [Lifecycle Services](https://lcs.dynamics.com/Logon/Index)'ta oturum açın.
1. Ana sayfada, ortamınızın dağıtıldığı projeyi seçin.
1. Proje sayfasında, eklentiyi yüklemek istediğiniz ortamı seçin.
1. Ortam sayfasında, **Power Platform tümleştirmesi** bölümünde aşağı kaydırarak **Ortam eklentileri** bölümünü bulun. Burada, Dataverse ortam adını bulabilirsiniz. Dataverse ortam adının Stok Görünürlüğü için kullanmak istediğiniz ad olduğunu onaylayın.

    > [!NOTE]
    > Şu anda yalnızca Lifecycle Services kullanılarak oluşturulan Dataverse ortamları desteklenmektedir. Dataverse ortamınız başka bir yolla (örneğin, PowerApps Yönetim Merkezini kullanarak) oluşturulduysa ve Supply Chain Management ortamınıza bağlıysa Stok Görünürlüğü eklentisini yüklemeden önce ilk olarak eşleşme sorununu çözmeniz gerekir.
    >
    > Çift yazma ortamınız Dataverse örneğine bağlıyken Lifecycle Services, Power Platform tümleştirmesi için ayarlanmamış olabilir. Bu bağlama uyuşmazlığı, beklenmeyen davranışlara neden olabilir. Aynı bağlantının iş olayları, sanal tablolar ve eklentiler tarafından kullanılabilmesi için Lifecycle Services ortam ayrıntılarının bağlı olduğunuz çift yazma ortamının ayrıntılarıyla eşleşmesi önerilir. Eşleme sorununun nasıl düzeltileceği hakkında bilgi için bkz. [Bağlama uyumsuzluğu](../../fin-ops-core/dev-itpro/data-entities/dual-write/lcs-setup.md#linking-mismatch). Eşleme sorunu çözümlendikten sonra, Stok Görünürlüğü'nü yüklemeye devam edebilirsiniz.

1. **Ortam eklentileri** bölümünde **Yeni bir eklenti yükleyin**'i seçin.

    ![Lifecycle Services'ta ortam sayfası](media/inventory-visibility-environment.png "Lifecycle Services'ta ortam sayfası")

1. **Yeni eklenti yükleyin** bağlantısını seçin. Kullanılabilir eklentilerin bir listesi görüntülenir.
1. Listede, **Stok Görünürlüğü**'nü seçin.
1. Ortamınız için aşağıdaki alanları ayarlayın:

    - **AAD uygulama (istemci) kimliği**: Daha önce oluşturup not ettiğiniz Azure AD uygulama kimliğini girin.
    - **AAD kiracı kimliği**: Daha önce not ettiğiniz kiracı kimliğini girin.

    ![Eklenti sayfasını ayarlama](media/inventory-visibility-setup.png "Eklenti sayfasını ayarlama")

1. **Hüküm ve koşullar** onay kutusunu seçerek hüküm ve koşulları kabul edin.
1. **Yükle**'yi seçin. Eklentinin durumu **Yükleniyor** olarak gösterilir. Yükleme tamamlandığında sayfayı yenileyin. Durum **Yüklendi** olarak değişecektir.
1. Dataverse uygulamasında, sol gezinme bölmesinde **Uygulamalar** bölümünü seçin ve **Stok Görünürlüğü** Power Apps uygulamasının başarıyla yüklendiğini doğrulayın. **Uygulamalar** bölümü yoksa [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) adresinden Stok Görünürlüğü ürün takımıyla iletişime geçin.

> [!NOTE]
> Sistem Lifecycle Services'da Stok Görünürlüğünü yükleme izniniz olmadığı konusunda sizi uyarırsa, izninizi değiştirmek için yöneticiye başvurmanız gerekir.
>
> Lifecycle Services sayfasından yüklenmesi bir saatten fazla sürerse kullanıcı hesabınız büyük olasılıkla Dataverse ortamundaki çözümleri yükleme iznine sahip olmayabilir. Sorunu gidermek için şu adımları izleyin:
>
> 1. Lifecycle Services sayfasından Stok Görünürlüğü eklentisini yükleme işlemini iptal edin.
> 1. [Microsoft 365 yönetim merkezinde](https://admin.microsoft.com) oturum açın ve eklentiyi yüklemek için kullanmak istediğiniz kullanıcı hesabında kendisine atanmış bir "Dynamics 365 Unified Operations Planı" lisansı olduğundan emin olun. Gerekirse lisansı atayın.
> 1. İlgili kullanıcı hesabını kullanarak [Power Platform yönetim merkezinde](https://admin.powerplatform.microsoft.com) oturum açın. Daha sonra, aşağıdaki adımları izleyerek stok görünülürlüğü eklentisini yükleyin:
>     1. Eklentiyi yüklemek istediğiniz ortamı seçin.
>     1. **Dynamics 365 Uygulamaları**'nı seçin.
>     1. **Uygulamayı Yükle**'yi seçin.
>     1. **Stok Görünürlüğü**'nü seçin
>
> 1. Yükleme tamamlandıktan sonra, Lifecycle Services sayfasına geri dönün ve **Stok Görünürlüğü** eklentisini yeniden yüklemeyi deneyin.

## <a name="set-up-inventory-visibility-in-supply-chain-management"></a><a name="setup-dynamics-scm"></a>Supply Chain Management uygulamasında Stok Görünürlüğü'nü ayarlama

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>Stok Görünürlüğü tümleştirme paketini dağıtma

Supply Chain Management sürüm 10.0.17 veya önceki bir sürümünü çalıştırıyorsanız paket dosyasını almak için [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) adresinden Stok Görünürlüğü yerleşik destek ekibine başvurun. Sonra paketi LifeCycle Services'da dağıtın.

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
    - **Rezervasyon denkleştirme değiştirici**: Stok Görünürlüğü'nde yapılan rezervasyonları denkleştirecek stok hareketi durumunu seçin. Bu ayar, denkleştirme işlemlerini tetikleyen sipariş işleme aşamasını belirler. Aşama, siparişin stok hareketi durumuna göre izlenir. Aşağıdaki seçeneklerden birini belirleyin:
        - *Siparişte*: *Harekette* durumu için sipariş oluşturulduğunda bir denkleştirme isteği gönderir. Denkleştirme miktarı, oluşturulan siparişin miktarıdır.
        - *Rezerve edilmiş*: *Rezerve edilmiş siparişli hareket* durumu için sipariş, rezerve edildiğinde, alındığında, sevk irsaliyesi deftere nakledildiğinde veya faturalandığında bir denkleştirme isteği gönderir. İstek, belirtilen işlem gerçekleştiğinde ilk adım için yalnızca bir kez tetiklenir. Denkleştirme miktarı, ilgili sipariş satırında stok hareketi durumunun *Siparişte* yerine *Siparişli rezerve miktar* (veya sonraki durum) olarak değiştirildiği miktardır.

1. **Stok Yönetimi \> Periyodik \> Stok Görünürlüğü Tümleştirmesi**'ne gidin ve işi etkinleştirin. Supply Chain Management'taki tüm stok değişikliği olayları artık Stok Görünürlüğü'ne nakledilecektir.

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>Stok Görünürlüğü Eklentisi'ni kaldırma

Stok Görünürlüğü Eklentisi'ni kaldırmak için aşağıdaki adımları izleyin:

1. Supply Chain Management'ta oturun açın.
1. **Stok Yönetimi \> Periyodik \> Stok Görünürlüğü Tümleştirmesi**'ne gidin ve işi devre dışı bırakın.
1. Lifecycle Services'a gidin ve eklentiyi kaldırmak istediğiniz ortam sayfasını açın (ayrıca bkz. [Stok Görünürlüğü Eklentisini yükleme](#install-add-in)).
1. **Kaldır**'ı seçin.
1. Kaldırma işlemi, Stok Görünürlüğü Eklentisi'ni sonlandırır, Lifecycle Services'tan eklentinin kaydını iptal eder ve Stok Görünürlüğü Eklentisi veri önbelleğinde depolanan geçici verileri siler. Ancak, Dataverse aboneliğinize eşitlenmiş olan birincil stok verileri burada depolanmaya devam eder. Bu verileri silmek için bu yordamın geri kalan bölümünü tamamlayın.
1. [Power Apps](https://make.powerapps.com)'i açın.
1. Gezinti çubuğunda **Ortam**'ı seçin.
1. Lifecycle Services ortamınız ile ilgili olan Dataverse ortamını seçin.
1. **Çözümler**'e gidin ve aşağıdaki çözümleri şu sırayla silin:
    1. Dynamics 365 Inventory Visibility – Bağlayıcı
    1. Dynamics 365 Inventory Visibility – Eklentiler
    1. Dynamics 365 Inventory Visibility – Uygulama
    1. Dynamics 365 Inventory Visibility – Denetimler
    1. Dynamics 365 Inventory Visibility – Temel 

    Bu çözümler silindikten sonra tablolarda depolanan veriler de silinir.

> [!NOTE]
> Stok Görünürlüğü Eklentisini kaldırdıktan sonra bir Supply Chain Management veritabanını geri yüklerseniz ve sonra eklentiyi yeniden yüklemek isterseniz, eklentiyi yeniden yüklemeden önce Dataverse aboneliğinizde depolanan eski Stok Görünürlük verilerini (önceki yordamda açıklandığı gibi) sildiğinizden emin olun. Bu durum, aksi takdirde ortaya çıkabilecek veri tutarsızlığı sorunlarını engeller.

## <a name="clean-inventory-visibility-data-from-dataverse-before-restoring-the-supply-chain-management-database"></a><a name="restore-environment-database"></a>Supply Chain Management veritabanını geri yüklemeden önce Dataverse'den Stok Görünürlük verilerini temizleme

Stok Görünürlüğünü kullanıyor olmanız ve sonra Supply Chain Management veritabanınızı geri yüklemeniz durumunda geri yüklenen veritabanınız daha önce Stok Görünürlüğü ile Dataverse'e eşitlenen veriler ile artık tutarlı olmayan veriler içerebilir. Bu veri tutarsızlığı sistem hatalarına ve diğer sorunlara neden olabilir. Bu nedenle, bir Supply Chain Management veritabanını geri yüklemeden önce daima tüm Stok Görünürlük verilerini Dataverse'den temizlemeniz önemlidir.

Bir Supply Chain Management veritabanını geri yüklemeniz gerekiyorsa, aşağıdaki yordamı kullanın:

1. Stok Görünürlüğü Eklentisini kaldırın ve [Stok Görünürlüğü Eklentisi](#uninstall-add-in) bölümünde açıklandığı şekilde Dataverse'deki tüm ilgili verileri kaldırın
1. Supply Chain Management veritabanınızı [Veritabanını belirli noktaya geri yükleme (PITR)](../../fin-ops-core/dev-itpro/database/database-point-in-time-restore.md) veya [Üretim veritabanını korumalı alan ortamında belirli bir noktaya geri yükleme](../../fin-ops-core/dev-itpro/database/database-pitr-prod-sandbox.md) bölümünde açıklandığı şekilde geri yükleyin.
1. Yine de kullanmak istiyorsanız yeniden yükleyin ve Stok Görünürlüğü Eklentisini [Stok Görünürlüğü Eklentisini Yükleme](#install-add-in) ve [Stok Görünürlüğü tümleştirmesini ayarlama](#setup-inventory-visibility-integration) bölümünde açıklandığı şekilde ayarlayın


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
