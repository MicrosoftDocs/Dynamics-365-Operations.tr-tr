---
title: Common Data Service sanal varlıklarını yapılandırma
description: Bu konu, Dynamics 365 Human Resources için sanal varlıkların nasıl yapılandırılacağını göstermektedir. Mecvut sanal varlıkları oluşturun ve güncelleştirin ve oluşturulan ve kullanılabilir varlıkları inceleyin.
author: andreabichsel
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0848b7556100fba38fcab0aa2a1a109e2e055fc9
ms.sourcegitcommit: b89baab13e530b5b1f079231619c628309a4742d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/05/2020
ms.locfileid: "3959587"
---
# <a name="configure-common-data-service-virtual-entities"></a>Common Data Service sanal varlıklarını yapılandırma

[!include [banner](includes/preview-feature.md)]

Dynamics 365 Human Resources Common Data Service'taki sanal bir veri kaynağıdır. Common Data Service ve Microsoft Power Platform'dan tam oluşturma, okuma, güncelleştirme ve silme (CRUD) işlemleri sağlar. Sanal varlıkların verileri Common Data Service'de depolanmaz , ancak uygulama veritabanında depolanır. 

Human Resources varlıklarındaki CRUD işlemlerini Common Data Service'den etkinleştirmek için, varlıkları Common Data Service'de sanal varlıklar olarak kullanılabilir yapmalısınız. Bu, Common Data Service ve Microsoft Power Platform'dan Human Resources'daki veriler üzerinde CRUD işlemleri gerçekleştirmenizi sağlar. Operasyonlar, varlıklara veri yazarken veri bütünlüğünü sağlamak için Human Resources'ın tam iş mantığı doğrulamalarını da destekler.

## <a name="available-virtual-entities-for-human-resources"></a>Human Resources için kullanılabilir sanal varlıklar

Human Resources'taki tüm Açık Veri Protokolü (OData) varlıkları Common Data Service'de sanal varlıklar olarak kullanılabilir. Bunlar Power Platform uygulamasında da kullanılabilir. Artık verileri Common Data Service'a kopyalamadan veya eşitlemeden doğrudan Human Resources'dan tam CRUD özelliği ile verileri kullanarak uygulamalar ve deneyimler oluşturabilirsiniz. Human Resources'taki iş süreçleri için işbirliği senaryolarını etkinleştiren, harici tabanlı web siteleri oluşturmak için Power Apps portallarını kullanabilirsiniz.

Ortamda etkinleştirilmiş sanal varlıkların listesini görüntüleyebilir ve [Power Apps](https://make.powerapps.com) içindeki varlıklarla **Dynamics 365 HR Sanal Varlıklar** çözümünde çalışmaya başlayabilirsiniz.

![Power Apps'taki Dynamics 365 HR Sanal Varlıkları](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-entities-versus-natural-entities"></a>Sanal varlıklar ve doğal varlıklar

Human Resources için sanal varlıklar, Common Data Service'taki Human Resources için oluşturulan doğal varlıklarla aynı değildir. Human Resources için doğal varlıklar ayrı olarak oluşturulur ve Common Data Service'deki HCM Ortak çözümünde tutulur. Doğal varlıklarla, veriler Common Data Service'ta depolanır ve Human Resources uygulama veritabanıyla eşitleme gerektirir.

> [!NOTE]
> Human Resources için Common Data Service doğal varlıkların listesi için bkz. [Common Data Service varlıkları](https://docs.microsoft.com/dynamics365/human-resources/hr-developer-entities).

## <a name="setup"></a>Ayar

Ortamınızdaki sanal varlıkları etkinleştirmek için bu kurulum adımlarını izleyin. 

### <a name="register-the-app-in-microsoft-azure"></a>Microsoft Azure'da uygulamayı kaydetme

İlk olarak, uygulamayı Azure portalında kaydetmeniz gerekir; böylece Microsoft kimlik platformu uygulama ve kullanıcılar için kimlik doğrulama ve yetkilendirme hizmetleri sağlayabilir. Azure'da uygulama kaydetme hakkında daha fazla bilgi için bkz. [Hızlı başlangıç: Microsoft kimlik platform ile uygulama kaydetme](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).

1. [Microsoft Azure portalını](https://portal.azure.com) açın.

2. Azure hizmetleri listesinde **Uygulama kayıtları**'nı seçin.

3. **Yeni kayıt** öğesini seçin.

4. **Ad** alanına uygulama için açıklayıcı bir ad girin. Örneğin, **Dynamics 365 Human Resources Sanal Varlıkları**.

5. **Yeniden yönlendirme URI'si** alanında Human Resources kurulumunuzun ad alanı URL'sini girin.

6. **Kayıt**'ı seç.

7. Kayıt tamamlandığında, Azure portalı uygulama kaydı **Uygulama (istemci) kimliğini** de içeren **Genel bakış** bölmesini görüntüler. Şu anda **Uygulama (istemci) kimliğini** not edin. [Sanal varlık veri kaynağını yapılandırırken](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source) bu bilgileri gireceksiniz.

8. Sol gezinti bölmesinde, **Sertifikalar ve gizli anahtarlar**'ı seçin.

9. Sayfanın **İstemci gizli anahtarı** bölümünde **Yeni istemci gizli anahtarı**'nı seçin.

10. Bir açıklama sağlayın, bir süre seçin ve **Ekle**'yi seçin.

11. Gizli anahtar değerini kaydedin. [Sanal varlık veri kaynağını yapılandırırken](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-entity-data-source) bu bilgileri gireceksiniz.

    > [!IMPORTANT]
    > Bu aşamada, gizli anahtarın değerini not aldığınızdan emin olun. Bu sayfadan ayrıldıktan sonra gizli anahtar hiçbir zaman görüntülenmez.

### <a name="install-the-dynamics-365-hr-virtual-entity-app"></a>Dynamics 365 HR Sanal Varlık uygulamasını yükleme

Sanal varlık çözüm paketini Common Data Service'a dağıtmak için Dynamics 365 HR Sanal Varlık uygulamasını Power Apps ortamınıza yükleyin.

1. [Power Platform Yönetim Merkezi](https://admin.powerplatform.microsoft.com)'ni açın.

2. **Ortamlar** listesinde, Human Resources kurulumunuzla ilişkilendirilen Power Apps ortamını seçin.

3. Sayfanın **Kaynaklar** bölümünde **Dynamics 365 uygulamaları**'nı seçin.

4. **Uygulamayı yükle** eylemini seçin.

5. **Dynamics 365 HR Sanal Varlık** öğesini ve **İleri**'yi seçin.

6. Hizmet koşullarını gözden geçirin ve kabul etmek için işaretleyin.

7. **Yükle**'yi seçin.

Yükleme birkaç dakika sürer. Bu işlem tamamlandığında sonraki adımlara devam edin.

![Dynamics 365 HR Sanal Varlık uygulamasını Power Platform yönetim merkezinden yükleyin](./media/hr-admin-integration-virtual-entities-power-platform-install.jpg)

### <a name="configure-the-virtual-entity-data-source"></a>Sanal varlık veri kaynağını yapılandırma 

Sonraki adım, sanal varlık veri kaynağını Power Apps ortamında yapılandırmaktır. 

1. [Power Platform Yönetim Merkezi](https://admin.powerplatform.microsoft.com)'ni açın.

2. **Ortamlar** listesinde, Human Resources kurulumunuzla ilişkilendirilen Power Apps ortamını seçin.

3. Sayfanın **Ayrıntılar** bölümünde **Ortam URL**'sini seçin.

4. **Çözüm Durumu Merkezi**'nde, uygulama sayfasının sağ üst kısmında **Gelişmiş Bul** simgesini seçin.

5. **Gelişmiş Bul** sayfasında, **Ara** açılan listesinde **Finance and Operations Sanal Veri Kaynağı Yapılandırmaları**'nı seçin.

6. **Sonuçlar**'ı seçin.

7. **Microsoft HR Veri Kaynağı** kaydını seçin.

8. Veri kaynağı yapılandırması için gerekli bilgileri girin.

   - **Hedef URL**: Human Resources ad alanınızın URL'si.
   - **Kiracı Kimliği**: Azure Active Directory (Azure AD) kiracı kimliği.
   - **AAD Uygulama Kodu**: Microsoft Azure portalında kayıtlı olan uygulama için oluşturulan uygulama (istemci) kimliği. Bu bilgiyi daha önce [Uygulamayı Microsoft Azure'da kaydetme](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure) bölümünde almıştınız.
   - **AAD Uygulama Gizli Anahtarı**: Microsoft Azure portalında kayıtlı olan uygulama için oluşturulan istemci gizli anahtarı. Bu bilgiyi daha önce [Uygulamayı Microsoft Azure'da kaydetme](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure) bölümünde almıştınız.

9. **Kaydet ve Kapat**'ı seçin.

   ![Microsoft HR Veri Kaynağı](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

### <a name="grant-app-permissions-in-human-resources"></a>Human Resources uygulamasında uygulama izinlerini verme

Human Resources'ta iki Azure AD uygulaması için izin verin:

- Microsoft Azure portalında kiracınız için oluşturulan uygulama
- Power Apps ortamında yüklü olan Dynamics 365 HR Sanal Varlık uygulaması 

1. Human Resources'ta **Azure Active Directory uygulamaları** sayfasını açın.

2. Yeni uygulama kaydı oluşturmak için **Yeni**'yi seçin.

    - **İstemci kodu** alanına, Microsoft Azure portalına kaydettiğiniz uygulama istemci kodunu girin.
    - **Ad** alanına, Microsoft Azure portalına kaydettiğiniz uygulama adını girin.
    - **Kullanıcı kimliği** alanında, Human Resources ve Power Apps ortamında yönetici izinlerine sahip olan kullanıcının kullanıcı kimliğini seçin.

3. İkinci uygulama kaydını oluşturmak için **Yeni**'yi seçin.

    - **İstemci Kimliği**: f9be0c49-aa22-4ec6-911a-c5da515226ff
    - **Ad**: Dynamics 365 HR Sanal Varlığı
    - **Kullanıcı kimliği** alanında, Human Resources ve Power Apps ortamında yönetici izinlerine sahip olan kullanıcının kullanıcı kimliğini seçin.

## <a name="generate-virtual-entities"></a>Sanal varlıklar oluşturma

Kurulum tamamlandığında, Common Data Service örneğiniz içinde oluşturmak ve etkinleştirmek istediğiniz sanal varlıkları seçebilirsiniz.

1. [Power Platform Yönetim Merkezi](https://admin.powerplatform.microsoft.com)'ni açın.

2. **Ortamlar** listesinde, Human Resources kurulumunuzla ilişkilendirilen Power Apps ortamını seçin.

3. Sayfanın **Ayrıntılar** bölümünde **Ortam URL**'sini seçin.

4. **Çözüm Durumu Merkezi**'nde, uygulama sayfasının sağ üst kısmında **Gelişmiş Bul** simgesini seçin.

5. **Gelişmiş Bul** sayfasında, **Ara** açılan listesinde **Kullanılabilir HR Varlıkları**'nı seçin.

6. Etkinleştirmek istediğiniz varlığı veya varlıkları bulmak için filtre seçeneklerini kullanın.

7. Listeden bir varlık seçin.

8. Varlık sayfasında, **Oluşturuldu** özelliğini varlık için **Evet** olarak değiştirin.

9. Varlık sayfasını kaydedin ve kapatın.

> [!NOTE]
> **Birden Çok Kaydı Değiştir** sayfasını kullanarak, birden çok sanal varlık oluşturabilirsiniz. Sayfada birden fazla kayıt seçin ve şeritte **Düzenle**'yi seçin. Daha sonra tüm kayıtlar için **Oluşturuldu** özelliğini değiştirebilirsiniz.

![Kullanılabilir HR Varlıkları](./media/hr-admin-integration-virtual-entities-available.jpg)

> [!NOTE]
> Gelecekteki sürümlerde sanal varlıklar oluşturma sürecini kolaylaştırmak için, işlem Human Resources'taki bir sayfada gerçekleşir.

## <a name="see-also"></a>Ayrıca bkz.

[Common Data Service nedir?](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[Varlığa genel bakış](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[Varlık ilişkilerine genel bakış](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[Harici veri kaynağından veri içeren sanal varlıkları oluşturma ve düzenleme](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[Power Apps portalları nedir?](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[Power Apps'ta uygulamalar oluşturmaya genel bakış](https://docs.microsoft.com/powerapps/maker/)
