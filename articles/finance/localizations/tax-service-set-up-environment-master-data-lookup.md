---
title: Vergi hesaplama konfigürasyonu için master veri aramasını etkinleştir
description: Bu makale, vergi hesaplama ana veri arama işlevini nasıl etkinleştirebileceğinizi ve ayarlayabileceğinizi açıklamaktadır.
author: kai-cloud
ms.date: 07/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2f9d882340171173e5e503f8b5e3aa856e8544b0
ms.sourcegitcommit: f2175fe5e900d39f34167d671aab5074b09cc1b8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/17/2022
ms.locfileid: "9306218"
---
# <a name="enable-master-data-lookup-for-tax-calculation-configuration"></a>Vergi hesaplama konfigürasyonu için master veri aramasını etkinleştir 

[!include [banner](../includes/banner.md)]

Bu makale, vergi hesaplama ana veri arama işlevini nasıl etkinleştirebileceğinizi ve ayarlayabileceğinizi açıklamaktadır. **Tüzel kişilik**, **Satıcı hesabı**, **Madde kodu** ve **Teslim koşulu** gibi alanlar için vergi hesaplama yapılandırmasındaki değerleri seçmek üzere bir açılan liste kullanılabilir. Bu değerler, bağlı Microsoft Dynamics 365 Finance ortamından Microsoft Dataverse veri kaynağı kullanılarak alınır.

> [!NOTE] 
> Vergi hesaplama yöneticisi veri arama işlevi isteğe bağlı işlevselliktir. Regulatory Configuration Service'teki (RCS) **Vergi Hizmeti Dataverse veri kaynağı desteği** özelliğini devre dışı bırakırsanız aşağıdaki adımları atlayabilirsiniz. Ancak, bu durumda, açılan liste vergi hesaplama yapılandırmasında kullanılamaz.

Vergi Hesaplama özellik sürümü yapılandırmasında açılır listeyi etkinleştirmek için aşağıdaki adımları tamamlayın.

1. [Microsoft Power Platform tümleştirmesini etkinleştirin ve Dataverse ortamını açın.](#enable)
2. [Finans ve operasyon sanal varlıklarını yükleyin.](#install)
3. [Azure Active Directory (Azure AD) uygulaması kaydedin.](#register)
4. [Finans ve operasyon uygulamalarında uygulama izinleri verin.](#grant)
5. [Sanal varlık veri kaynağını yapılandırın.](#configure)
6. [Dataverse sanal varlıklarını etkinleştirin.](#virtual)
7. [Vergi Hesaplama için bağlı uygulamayı ayarlayın.](#set-up)
8. [Dataverse Model Eşleme yapılandırmasını içeri aktarın ve ayarlayın.](#import)

## <a name="enable-microsoft-power-platform-integration-and-open-the-dataverse-environment"></a><a name='enable'></a>Microsoft Power Platform tümleştirmesini etkinleştirme ve Dataverse ortamını açma

Finans ve operasyon uygulamaları ve Microsoft Power Platform tümleştirmesi Microsoft Dynamics Lifecycle Services (LCS) içinde yeni bir finans ve operasyon uygulamaları ortamı oluşturduğunuzda etkinleştirilebilir. Daha fazla bilgi için bkz. [Microsoft Power Platform tümleştirmesi - Eklentilere genel bakış](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Bu işlemi tamamladıktan sonra, bir Microsoft Power Platform ortamının adı, **Power Platform tümleştirmesi** bölümünde görünür.

1. LCS'de, finans ve operasyon ortamınızda **Power Platform Tümleştirmesi** bölümünde, bağlı ortam için **Ortam adı** değerini bulup not edin.

    [![Ortam adı değeri.](./media/tcs-dataverse-master-data-lookup-1.png)](./media/tcs-dataverse-master-data-lookup-1.png)

2. [Power Platform yönetim merkezinde](https://admin.powerplatform.microsoft.com/environments), **Ortamlar** sekmesinde, not ettiğiniz **Ortam adı** değeriyle eşleşen ortamı seçin.
3. **Ayrıntılar** sayfasında, Dataverse ortamının **Ortam URL'si** değerini bulun. Bu değeri, [Adım 7. Vergi Hesaplama için bağlı uygulamayı ayarlama](#set-up) aşamasında kullanmak üzere not edin.
4. **Ortam URL'si** değerini seçtiğinizde tarayıcınızda Dataverse ortamını açabildiğinizden emin olun.

    [![Dataverse ortamı sayfası.](./media/tcs-dataverse-master-data-lookup-2.png)](./media/tcs-dataverse-master-data-lookup-2.png)

    > [!NOTE]
    > Dataverse ortamını tarayıcınızda açık tutun. Bu ortamı [Adım 5. Sanal varlık veri kaynağını yapılandırma](#configure) aşamasında kullanacaksınız.

Daha fazla bilgi için bkz. [Microsoft Power Platform tümleştirmesini etkinleştirme](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md).

## <a name="install-finance-and-operations-virtual-entities"></a><a name='install'></a>Finans ve operasyon sanal varlıklarını yükleme

Finans ve operasyon sanal varlıkları için Dataverse çözümünün Microsoft AppSource sanal varlık çözümünden yüklenmesi gerekir.

1. AppSource'ta, [Finans ve operasyon sanal varlığı](https://appsource.microsoft.com/product/dynamics-365/mscrm.finance_and_operations_virtual_entity) öğesini bulun.
2. **Şimdi al**'ı seçin.
3. **Ortam seç** alanında, daha önce not ettiğiniz **Ortam adı** değerini girin.
4. Onay kutularını seçin ve ardından **Yükle**'yi seçin.

Yükleme işlemi tamamlandığında, **Finans ve operasyon sanal varlığı** uygulamasını [Power Platform yönetim merkezi](https://admin.powerplatform.microsoft.com/) içinde, **Kaynaklar**\>**Dynamics 365 uygulamaları** altında bulabilirsiniz.

Daha fazla bilgi için bkz. [Sanal varlık çözümünü alma](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#get-virtual-entity-solution).

## <a name="register-an-azure-ad-application"></a><a name='register'></a>Azure AD uygulaması kaydetme

Dataverse tarafından çağrılabilmeleri için Azure AD uygulamasını finans ve operasyon uygulamalarıyla aynı kiracı üzerinde kaydetmeniz gerekir.

1. [Azure portalında](https://portal.azure.com), **Azure Active Directory \> Uygulama kayıtları**'na gidin.
2. **Yeni kayıt**'ı seçin ve aşağıdaki bilgileri girin:

    - **Ad** – Benzersiz bir ad girin.
    - **Hesap türü** – **Herhangi bir Azure AD dizini** (tek kiracılı veya çok kiracılı) girin.
    - **Yeniden Yönlendirme URI'si** – Bu alanı boş bırakın.

3. **Kayıt**'ı seç.
4. Daha sonra gereksinim duyacağınız **Uygulama (istemci) Kodu** değerini not edin.

    [![Azure AD Uygulaması (istemci) Kimliği değeri.](./media/tcs-dataverse-master-data-lookup-3.png)](./media/tcs-dataverse-master-data-lookup-3.png)

5. Uygulama için bir simetrik anahtar oluşturun.
6. Yeni uygulamada, **Sertifikalar ve parolalar**'ı seçin.
7. **Yeni gizli anahtar**'ı seçin.
8. Bir açıklama girin, bitiş tarihi seçin ve ardından **Kaydet** seçeneğini belirleyin. Anahtar oluşturulur ve gösterilir. Daha sonra kullanmak üzere değeri kopyalayın.

Daha fazla bilgi için bkz. [Azure AD uygulaması kaydetme](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#register-the-app-in-the-azure-portal).

## <a name="grant-app-permissions-in-finance-and-operations-apps"></a><a name='grant'></a>Finans ve operasyon uygulamalarında uygulama izinleri verme

Dataverse, finans ve operasyon uygulamalarını çağırmak için oluşturduğunuz Azure AD uygulamasını kullanır. Bu nedenle, uygulamanın finans ve uygulamaları tarafından güvenilir olması ve uygun haklara sahip bir kullanıcı hesabıyla ilişkilendirilmiş olması gerekir. Finans ve operasyon uygulamalarında, **yalnızca** sanal varlık işlevselliği haklarına sahip olan özel bir hizmet kullanıcısı oluşturmanız gerekir. Bu hizmet kullanıcısının başka hakları olmamalıdır. Bu adımı tamamladıktan sonra, oluşturduğunuz Azure AD uygulamasının parolasını içeren tüm uygulamalar finans ve operasyon uygulamaları ortamını çağırıp sanal varlık işlevselliğine erişebilir.

1. Ortamınızda, **Sistem Yönetimi**\>**Kullanıcılar**\>**Kullanıcılar**'a gidin.
2. Yeni bir kullanıcı eklemek için **Yeni**'yi seçin ve aşağıdaki bilgileri girin:

    - **Kullanıcı Kimliği** – **dataverseintegration** veya başka bir değer girin.
    - **Kullanıcı adı** – **dataverse tümleştirmesi** veya başka bir değer girin.
    - **Sağlayıcı** – Bu alanı **NonAAD** olarak ayarlayın.
    - **E-posta** – **dataverseintegration** veya başka bir değer girin. (Değerin geçerli bir e-posta hesabı olması gerekmez.)

3. Kullanıcıya **Dataverse sanal varlık tümleştirme uygulaması** güvenlik rolünü atayın.
4. **Sistem kullanıcısı** dahil diğer tüm rolleri kaldırın.
5. **Sistem Yönetimi** \> **Kurulum** \> **Azure Active Directory uygulamaları**'na giderek Dataverse'i kaydedin. 
6. Satır ekleyin ve **İstemci Kimliği** alanında, daha önce not ettiğiniz **Uygulama (istemci) kimliği** değerini girin.
7. **Ad** alanına, bir ad girin. Örneğin, **Dataverse Tümleştirmesi** yazın.
8. **Kullanıcı kimliği** alanında, daha önce oluşturduğunuz kullanıcı kimliğini girin.

Daha fazla bilgi için bkz. [Finans ve Operasyon uygulamalarında uygulama izinleri verme](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#grant-app-permissions-in-finance-and-operations-apps).

## <a name="configure-the-virtual-entity-data-source"></a><a name='configure'></a>Sanal varlık veri kaynağını yapılandırma

Dataverse'e bağlanacağı Finans ve operasyon uygulaması örneğini girmeniz gerekir.

1. Dataverse ortamınız [Adım 1. Microsoft Power Platform tümleştirmesini etkinleştirme ve Dataverse ortamını açma](#enable) aşamasından itibaren tarayıcınızda açık olmalıdır. Sağ üst köşedeki ayarlar düğmesini (çark simgesi) ve ardından **Gelişmiş Ayarlar**'ı seçin.

    [![Dataverse ortamında Gelişmiş ayarları açma.](./media/tcs-dataverse-master-data-lookup-4.png)](./media/tcs-dataverse-master-data-lookup-4.png)

2. **Ayarlar** açılır menüsünde, **Yönetim**'i seçin.

    [![Yönetim.](./media/tcs-dataverse-master-data-lookup-5.png)](./media/tcs-dataverse-master-data-lookup-5.png)

3. **Sanal Varlık Veri Kaynakları**'nı seçin.

    [![Sanal Varlık Veri Kaynakları.](./media/tcs-dataverse-master-data-lookup-6.png)](./media/tcs-dataverse-master-data-lookup-6.png)

4. **Finans ve Operasyon** adlı veri kaynağını seçin.

    [![Finans ve Operasyon veri kaynağı.](./media/tcs-dataverse-master-data-lookup-7.png)](./media/tcs-dataverse-master-data-lookup-7.png)

5. Önceki adımlardan aşağıdaki bilgileri girin:

    - **Hedef URL** – Finans ve operasyon uygulamalarına erişebileceğiniz URL'yi girin.
    - **OAuth URL'si** – `https://login.windows.net/` yazın.
    - **Kiracı kimliği** – Kiracınızı belirtin. Bu değer şirketinizin e-posta adresinin etki alanı adı olabilir (örneğin contoso.com).
    - **AAD Uygulama Kimliği** – Daha önce oluşturduğunuz **Uygulama (istemci) kimliği** değerini girin.
    - **AAD Uygulama parolası** – Daha önce oluşturulan parolayı girin.
    - **AAD Kaynağı** – **00000015-0000-0000-c000-000000000000** yazın. Bu değer, finans ve operasyon uygulamalarını temsil eden Azure AD uygulamasıdır. Bu her zaman aynı değer olmalıdır.

6. Değişikliklerinizi kaydedin.
7. Sayfayı kapatıp **Yönetim** sayfasına dönün ve [Adım 6. Dataverse sanal varlıklarını etkinleştirme](#virtual) aşamasına geçin.

    [![Varlığı düzenlemeye kapatma.](./media/tcs-dataverse-master-data-lookup-8.png)](./media/tcs-dataverse-master-data-lookup-8.png)

Daha fazla bilgi için bkz. [Sanal varlık veri kaynağını yapılandırma](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#configure-the-virtual-entity-data-source).

## <a name="enable-dataverse-virtual-entities"></a><a name='virtual'></a>Dataverse sanal varlıklarını etkinleştirme

Vergi Hesaplama yapılandırması tarafından kullanılabilmeleri için finans ve operasyon uygulamalarındaki sanal varlıkların görünürlüğü **Evet** olarak ayarlanmalıdır.

> [!NOTE]
> [Adım 8. Vergi Hesaplama için bağlı uygulamayı ayarlama](#import) aşamasında tek bir tıklamayla Vergi Hesaplama ile ilgili sanal varlıkları etkinleştirerek bu adımı atlayabilirsiniz. Ancak finans ve operasyon uygulamaları ile Dataverse arasındaki bağlantının iyi kurulduğunu göstermek için en az bir sanal varlığı el ile etkinleştirmenizi öneririz.

1. Dataverse ortamınızda, **Yönetim** sayfasında, sağ üst köşedeki filtre düğmesini (huni simgesi) seçin.

    [![Filtre düğmesi.](./media/tcs-dataverse-master-data-lookup-9.png)](./media/tcs-dataverse-master-data-lookup-9.png)

2. **Gelişmiş bul** penceresinde, **Ara** alanında, **Kullanılabilir Finans ve Operasyon Varlıkları**'nı seçin.
3. Şu kuralı ekletin: **Ad** – **İçerir** – **CompanyInfoEntity**. Ardından **Sonuçlar**'ı seçin.

    [![Gelişmiş bul penceresi.](./media/tcs-dataverse-master-data-lookup-10.png)](./media/tcs-dataverse-master-data-lookup-10.png)

4. Arama sonuçlarında **CompanyInfoEntity** öğesini seçin, **Görünür** onay kutusunu işaretleyin ve **Kaydet** seçeneğini belirleyin.

    [![Varlık görünürlüğünü ayarlama.](./media/tcs-dataverse-master-data-lookup-11.png)](./media/tcs-dataverse-master-data-lookup-11.png)

5. Vergi Hesaplama yapılandırmasında başvurulan aşağıdaki varlıklar için önceki adımları tekrarlayın:

    - CompanyInfoEntity
    - CurrencyEntity
    - CustCustomerV3Entity
    - DeliveryTermsEntity
    - EcoResProductCategoryEntity
    - EcoResReleasedProductV2Entity
    - LogisticsAddressCountryRegionTranslationEntity
    - LogisticsAddressStateEntity
    - PurchProcurementChargeCDSEntity
    - SalesChargeCDSEntity
    - TaxGroupEntity
    - TaxItemGroupHeadingEntity
    - VendVendorV2Entity
    - InventOperationalSiteV2Entity
    - TaxExemptCodeEntity
    - InventWarehouseEntity

    > [!NOTE]
    > Bir varlığın yalnızca ilk 5000 kaydı Dataverse tarafından alınabilir ve Vergi Hesaplama yapılandırmasının açılır menüsünde kullanılabilir hale getirilebilir.

Daha fazla bilgi için bkz. [Microsoft Dataverse sanal varlıklarını etkinleştirme](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).

## <a name="set-up-the-connected-application-for-tax-calculation"></a><a name='set-up'></a>Vergi Hesaplama için bağlı uygulamayı ayarlama

1. **Elektronik raporlama**'ya gidin, ardından **İlgili bağlantılar** bölümünde, **Bağlı uygulamalar**'ı seçin.

    [![Bağlı uygulamalar.](./media/tcs-dataverse-master-data-lookup-12.png)](./media/tcs-dataverse-master-data-lookup-12.png)

2. Kayıt eklemek için **Yeni**'yi seçin ve aşağıdaki bilgileri girin.

    - **Ad**: Ad girin.
    - **Tür** – **Dataverse**'ü seçin.
    - **Uygulama** – Dataverse ortamınızın [Adım 1. Microsoft Power Platform tümleştirmesini etkinleştirme ve Dataverse ortamını açma](#enable) aşamasında not ettiğiniz **Ortam URL'si** değerini girin.
    - **Kiracı** – Kiracınızı girin.
    - **Özel URL** – Dataverse URL'nizi girin ve bu URL'ye **/api/data/v9.1** ekleyin.

3. **Bağlantıyı denetle**'yi seçin ve ardından iletişim kutusunda **Seçili uzak uygulamaya bağlanmak için buraya tıklayın**'ı seçin.

    [![Bağlantıyı denetleme.](./media/tcs-dataverse-master-data-lookup-13.png)](./media/tcs-dataverse-master-data-lookup-13.png)
4. Bağlantının başarıyla kurulduğunu gösteren "Başarılı!" iletisi aldığınızdan emin olun.

    [![Başarılı iletisi.](./media/tcs-dataverse-master-data-lookup-14.png)](./media/tcs-dataverse-master-data-lookup-14.png)
    
5. RCS'de, **Özellik yönetimi** çalışma alanını açın ve aşağıdaki özellikleri etkinleştirin:

    - Globalleştirme özellikleri
    - Elektronik raporlama Dataverse veri kaynakları desteği
    - Vergi Hizmeti Dataverse veri kaynakları desteği

## <a name="import-and-set-up-the-dataverse-model-mapping-configuration"></a><a name='import'></a>Dataverse Model Eşleme yapılandırmasını içeri aktarma ve ayarlama

Microsoft, finans ve operasyonlar uygulamalarından Vergi Hesaplama işlevine aktarılan varlıklar için varsayılan model eşleme yapılandırmaları sağlar.

1. RCS'de, **Elektronik raporlama**'ya gidin.
2. **Yapılandırma sağlayıcıları** bölümünde, **Microsoft** sağlayıcısı kutucuğunda **Depolar**'ı seçin.

    [![Depolar.](./media/tcs-dataverse-master-data-lookup-15.png)](./media/tcs-dataverse-master-data-lookup-15.png)

3. **Genel yapılandırma deposu** kaydını, ardından **Aç**'ı seçin.
4. **Vergi Veri Modeli**\>**Vergi Hesaplama Veri Modeli** altından, **Dataverse Model Eşleme** yapılandırmasını seçin.
5. **Sürümler** hızlı sekmesinde, finans ve operasyon uygulamaları sürümünüzle eşleşen bir sürüm seçin ve **İçeri aktar** seçeneğini belirleyin.

    [![Dataverse Model Eşleme yapılandırmasını içeri aktarma.](./media/tcs-dataverse-master-data-lookup-16.png)](./media/tcs-dataverse-master-data-lookup-16.png)

    > [!IMPORTANT]
    > **Dataverse Model Eşleme** yapılandırması yalnızca içeri aktarılan en yüksek sürümde geçerlidir. Bu nedenle, uygulamayı planladığınız Vergi Hesaplama yapılandırması sürümünden daha yüksek bir **Dataverse Model Eşleme** yapılandırması sürümünü içeri aktarmamalısınız. Örneğin, Vergi Hesaplama yapılandırmasının 40.50.225 sürümünü uygulamayı planlıyorsanız, yalnızca **Dataverse Model Eşleme** yapılandırmasının 40.50.13 sürümünü içeri aktarmalısınız. Sürüm 40.54.14'ü içeri aktarmamalısınız. Aksi halde, yapılandırmada bir veri modeli uyuşmazlığı oluşur.

6. **Elektronik raporlama**'ya dönün ve **Vergi yapılandırmaları** kutucuğunu seçin.
7. İçeri aktarılan **Dataverse Model Eşleme** yapılandırmasını seçin ve **Düzenle** seçeneğini belirleyin.
8. **Model eşleme için varsayılan** seçeneğini **Evet** olarak ayarlayın.
9. **Bağlı uygulama** alanında, [Adım 7. Vergi Hesaplama için bağlı uygulama ayarlama](#set-up) aşamasında ayarladığınız bağlı uygulamayı seçin.
10. Vergi Hesaplama ile ilgili tüm sanal varlıkları görünür hale getirmek için **Sanal tablo görünürlüğünü ayarla** seçeneğini **Evet** olarak ayarlayın.

Ana veri arama işlevselliğini ayarlama işlemini tamamladınız. Dynamics 365 Finance'teki **Tüzel kişilik**, **Satıcı hesabı**, **Madde kodu** ve **Teslimat koşulu** gibi alanlar için bir açılır liste **Vergi Hesaplama özellik sürümü** kurulumunda etkinleştirilir.

[![Tüzel varlık açılır listesi.](./media/tcs-dataverse-master-data-lookup-17.png)](./media/tcs-dataverse-master-data-lookup-17.png)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
