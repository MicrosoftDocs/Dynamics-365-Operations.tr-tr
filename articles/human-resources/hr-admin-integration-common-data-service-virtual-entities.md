---
title: Common Data Service sanal varlıklarını yapılandırma
description: Bu konu, Dynamics 365 Human Resources için sanal varlıkların nasıl yapılandırılacağını göstermektedir. Mecvut sanal varlıkları oluşturun ve güncelleştirin ve oluşturulan ve kullanılabilir varlıkları inceleyin.
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
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
ms.openlocfilehash: 2b590faeab600d04c9d5303693ec1e9ac682250d
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645613"
---
# <a name="configure-common-data-service-virtual-entities"></a>Common Data Service sanal varlıklarını yapılandırma

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

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

### <a name="enable-virtual-entities-in-human-resources"></a>Human Resources'ta sanal varlıkları etkinleştirme

Önce, **özellik yönetimi** çalışma alanında sanal varlıkları etkinleştirmelisiniz.

1. İnsan Kaynakları, **sistem yönetimi**'ni seçin.

2. **Özellik yönetimi** kutucuğunu seçin.

3. **HR/CD 'de sanal varlık desteğini** seçin ve **Etkinleştir** 'i seçin.

Özellikleri devre dışı bırakma ve etkinleştirmeyle ilgili daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).

### <a name="register-the-app-in-microsoft-azure"></a>Microsoft Azure'da uygulamayı kaydetme

Human Resource örneğinizi Azure portalında kaydetmeniz gerekir; böylece Microsoft kimlik platformu uygulama ve kullanıcılar için kimlik doğrulama ve yetkilendirme hizmetleri sağlayabilir. Azure'da uygulama kaydetme hakkında daha fazla bilgi için bkz. [Hızlı başlangıç: Microsoft kimlik platform ile uygulama kaydetme](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app).

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

8. Veri kaynağı yapılandırması için gerekli bilgileri girin:

   - **Hedef URL**: Human Resources ad alanınızın URL'si. Hedef URL 'nin biçimi:
     
     https://\<hostname\>.hr.talent.dynamics.com/namespaces/\<namespaceID\>/

     Örneğin:
     
     `https://aos.rts-sf-5ea54e35c68-westus2.hr.talent.dynamics.com/namespaces/49d24c565-8f4d-4891-b174-bf83d948ed0c/`

     >[!NOTE]
     >Hata almamak için URL'nin sonuna "**/**" karakteri eklediğinizden emin olun.

   - **Kiracı Kimliği**: Azure Active Directory (Azure AD) kiracı kimliği.

   - **AAD Uygulama Kodu**: Microsoft Azure portalında kayıtlı olan uygulama için oluşturulan uygulama (istemci) kimliği. Bu bilgiyi daha önce [Uygulamayı Microsoft Azure'da kaydetme](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure) bölümünde almıştınız.

   - **AAD Uygulama Gizli Anahtarı**: Microsoft Azure portalında kayıtlı olan uygulama için oluşturulan istemci gizli anahtarı. Bu bilgiyi daha önce [Uygulamayı Microsoft Azure'da kaydetme](hr-admin-integration-common-data-service-virtual-entities.md#register-the-app-in-microsoft-azure) bölümünde almıştınız.

   ![Microsoft HR Veri Kaynağı](./media/hr-admin-integration-virtual-entities-hr-data-source.jpg)

9. **Kaydet ve Kapat**'ı seçin.

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

1. Human Resources'ta **Common Data Service (CDS) tümleştirmesi** sayfasını açın.

2. **Sanal varlıklar** sekmesini seçin.

> [!NOTE]
> **Sanal varlığı etkinleştir** geçiş düğmesi, gerekli tüm kurulum tamamlandığında otomatik olarak **Evet** olarak ayarlanır. Geçiş düğmesi **Hayır** olarak ayarlanmışsa, tüm önkoşul kurulumun tamamlandığından emin olmak için bu belgenin önceki bölümlerindeki adımları gözden geçirin.

3. Common Data Service'te oluşturmak istediğiniz varlığı veya varlıkları seçin.

4. **Oluştur/Yenile**'yi seçin.

![Common Data Service Tümleştirmesi](./media/hr-admin-integration-common-data-service-integration.jpg)

## <a name="check-entity-generation-status"></a>Varlık oluşturma durumunu denetle

Sanal varlıklar Common Data Service içinde zaman uyumsuz bir arka plan işleminde oluşturulur. İşlemin üzerindeki güncelleştirmeler işlem merkezinde görüntülenebilir. Hata günlükleri de dahil olmak üzere işlemle ilgili ayrıntılar, **işlem otomasyonları** sayfasında görüntülenir.

1. Human Resources'da, **İşlem otomasyonları** sayfasını açın.

2. **Arka plan işlemleri** sekmesini seçin.

3. **Sanal varlık yoklama asenkron operasyonu arka plan işlemi**'ni seçin.

4. **En son sonuçları görüntüle**'yi seçin.

Yan taraftaki bölme işlemle ilgili en son yürütme sonuçlarını görüntüler. Common Data Service'ten gelen tüm hatalar da dahil olmak üzere, işlem günlüğünü görüntüleyebilirsiniz.

## <a name="see-also"></a>Ayrıca bkz.

[Common Data Service nedir?](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)<br>
[Varlığa genel bakış](https://docs.microsoft.com/powerapps/maker/common-data-service/entity-overview)<br>
[Varlık ilişkilerine genel bakış](https://docs.microsoft.com/powerapps/maker/common-data-service/relationships-overview)<br>
[Harici veri kaynağından veri içeren sanal varlıkları oluşturma ve düzenleme](https://docs.microsoft.com/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[Power Apps portalları nedir?](https://docs.microsoft.com/powerapps/maker/portals/overview)<br>
[Power Apps'ta uygulamalar oluşturmaya genel bakış](https://docs.microsoft.com/powerapps/maker/)
