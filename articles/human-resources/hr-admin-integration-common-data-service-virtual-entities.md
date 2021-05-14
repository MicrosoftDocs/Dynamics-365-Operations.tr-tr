---
title: Dataverse sanal tablolarını yapılandırma
description: Bu konu, Dynamics 365 Human Resources için sanal tabloların nasıl yapılandırılacağını göstermektedir. Mecvut sanal tabloları oluşturun ve güncelleştirin ve oluşturulan ve kullanılabilir tabloları inceleyin.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 04997aba427ae6013c8154593b09ae1a45a580c3
ms.sourcegitcommit: 9283caad2d0636f98579c995784abec19fda2e3f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935765"
---
# <a name="configure-dataverse-virtual-tables"></a>Dataverse sanal tablolarını yapılandırma

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Human Resources Microsoft Dataverse'taki sanal bir veri kaynağıdır. Dataverse ve Microsoft Power Platform'dan tam oluşturma, okuma, güncelleştirme ve silme (CRUD) işlemleri sağlar. Sanal tabloların verileri Dataverse'de depolanmaz ancak uygulama veritabanında depolanır.

Human Resources varlıklarındaki CRUD işlemlerini Dataverse'den etkinleştirmek için varlıkları Dataverse'de sanal tablolar olarak kullanılabilir yapmalısınız. Bu, Dataverse ve Microsoft Power Platform'dan Human Resources'daki veriler üzerinde CRUD işlemleri gerçekleştirmenizi sağlar. Operasyonlar, varlıklara veri yazarken veri bütünlüğünü sağlamak için Human Resources'ın tam iş mantığı doğrulamalarını da destekler.

> [!NOTE]
> Human Resources varlıkları Dataverse tablolarına karşılık gelir. Dataverse (önceden Common Data Service) ve terminoloji güncelleştirmeleri hakkında daha fazla bilgi için bkz. [Microsoft Dataverse nedir?](/powerapps/maker/data-platform/data-platform-intro)

## <a name="available-virtual-tables-for-human-resources"></a>Human Resources için kullanılabilir sanal tablolar

Human Resources'taki tüm Açık Veri Protokolü (OData) varlıkları Dataverse'de sanal tablolar olarak kullanılabilir. Bunlar Power Platform uygulamasında da kullanılabilir. Artık verileri Dataverse'a kopyalamadan veya eşitlemeden doğrudan Human Resources'dan tam CRUD özelliği ile verileri kullanarak uygulamalar ve deneyimler oluşturabilirsiniz. Human Resources'taki iş süreçleri için işbirliği senaryolarını etkinleştiren, harici tabanlı web siteleri oluşturmak için Power Apps portallarını kullanabilirsiniz.

Ortamda etkinleştirilmiş sanal tabloların listesini görüntüleyebilir ve [Power Apps](https://make.powerapps.com) içindeki tablolarla **Dynamics 365 HR Sanal Tablolar** çözümünde çalışmaya başlayabilirsiniz.

![Power Apps'teki Dynamics 365 HR Sanal Tabloları](./media/hr-admin-integration-virtual-entities-power-apps.jpg)

## <a name="virtual-tables-versus-native-tables"></a>Sanal tablolar ve yerel tablolar karşılaştırması

Human Resources için sanal tablolar, Dataverse'teki Human Resources için oluşturulan yerel tablolarla aynı değildir. 

Human Resources için yerel tablolar ayrı olarak oluşturulur ve Dataverse'deki HCM Ortak çözümünde tutulur. Yerel tablolarla, veriler Dataverse'ta depolanır ve Human Resources uygulama veritabanıyla eşitleme gerektirir.

> [!NOTE]
> Human Resources için Dataverse yerel tablolarının listesi için bkz. [Dataverse tabloları](./hr-developer-entities.md).

## <a name="setup"></a>Ayar

Ortamınızdaki sanal tabloları etkinleştirmek için bu kurulum adımlarını izleyin.

### <a name="enable-virtual-tables-in-human-resources"></a>Human Resources'ta sanal tabloları etkinleştirme

Önce, **özellik yönetimi** çalışma alanında sanal tabloları etkinleştirmelisiniz.

1. İnsan Kaynakları, **sistem yönetimi**'ni seçin.

2. **Özellik yönetimi** kutucuğunu seçin.

3. **Dataverse'te HR için sanal tablo desteği**'ni seçin ve **Etkinleştir**'i seçin.

Özellikleri devre dışı bırakma ve etkinleştirmeyle ilgili daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).

### <a name="register-the-app-in-microsoft-azure"></a>Microsoft Azure'da uygulamayı kaydetme

Human Resource örneğinizi Azure portalında kaydetmeniz gerekir; böylece Microsoft kimlik platformu uygulama ve kullanıcılar için kimlik doğrulama ve yetkilendirme hizmetleri sağlayabilir. Azure'da uygulama kaydetme hakkında daha fazla bilgi için bkz. [Hızlı başlangıç: Microsoft kimlik platform ile uygulama kaydetme](/azure/active-directory/develop/quickstart-register-app).

1. [Microsoft Azure portalını](https://portal.azure.com) açın.

2. Azure hizmetleri listesinde **Uygulama kayıtları**'nı seçin.

3. **Yeni kayıt** öğesini seçin.

4. **Ad** alanına uygulama için açıklayıcı bir ad girin. Örneğin, **Dynamics 365 Human Resources Sanal Tabloları**.

5. **Yeniden yönlendirme URI'si** alanında Human Resources kurulumunuzun ad alanı URL'sini girin.

6. **Kayıt**'ı seç.

7. Kayıt tamamlandığında, Azure portalı uygulama kaydı **Uygulama (istemci) kimliğini** de içeren **Genel bakış** bölmesini görüntüler. Şu anda **Uygulama (istemci) kimliğini** not edin. [Sanal tablo veri kaynağını yapılandırırken](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source) bu bilgileri gireceksiniz.

8. Sol gezinti bölmesinde, **Sertifikalar ve gizli anahtarlar**'ı seçin.

9. Sayfanın **İstemci gizli anahtarı** bölümünde **Yeni istemci gizli anahtarı**'nı seçin.

10. Bir açıklama sağlayın, bir süre seçin ve **Ekle**'yi seçin.

11. Gizli öğenin değerini tablonun **Değer** özelliği bölümünden kaydedin. [Sanal tablo veri kaynağını yapılandırırken](hr-admin-integration-common-data-service-virtual-entities.md#configure-the-virtual-table-data-source) bu bilgileri gireceksiniz.

    > [!IMPORTANT]
    > Bu aşamada, gizli anahtarın değerini not aldığınızdan emin olun. Bu sayfadan ayrıldıktan sonra gizli anahtar hiçbir zaman görüntülenmez.

### <a name="install-the-dynamics-365-hr-virtual-table-app"></a>Dynamics 365 HR Sanal Tablo uygulamasını yükleme

Sanal tablo çözüm paketini Dataverse'a dağıtmak için Dynamics 365 HR Sanal Tablo uygulamasını Power Apps ortamınıza yükleyin.

1. Human Resources'ta **Microsoft Dataverse tümleştirmesi** sayfasını açın.

2. **Sanal tablolar** sekmesini seçin.

3. **Sanal tablo uygulamasını yükle**'yi seçin.

### <a name="configure-the-virtual-table-data-source"></a>Sanal tablo veri kaynağını yapılandırma

Sonraki adım, sanal tablo veri kaynağını Power Apps ortamında yapılandırmaktır.

1. [Power Platform Yönetim Merkezi](https://admin.powerplatform.microsoft.com)'ni açın.

2. **Ortamlar** listesinde, Human Resources kurulumunuzla ilişkilendirilen Power Apps ortamını seçin.

3. Sayfanın **Ayrıntılar** bölümünde **Ortam URL**'sini seçin.

4. **Çözüm Durumu Merkezi**'nde, uygulama sayfasının sağ üst kısmında **Gelişmiş Bul** simgesini seçin.

5. **Gelişmiş Bul** sayfasında, **Ara** açılan listesinde **Finance and Operations Sanal Veri Kaynağı Yapılandırmaları**'nı seçin.

   > [!NOTE]
   > Sanal tablo uygulamasının önceki kurulum adımından yüklenmesi birkaç dakika sürebilir. **Finance and Operations Sanal Veri Kaynağı Yapılandırmaları** listede yoksa, bir dakika bekleyip listeyi yenileyin.

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
- Power Apps ortamında yüklü olan Dynamics 365 HR Sanal Tablo uygulaması 

1. Human Resources'ta **Azure Active Directory uygulamaları** sayfasını açın.

2. Yeni uygulama kaydı oluşturmak için **Yeni**'yi seçin.

    - **İstemci kodu** alanına, Microsoft Azure portalına kaydettiğiniz uygulama istemci kodunu girin.
    - **Ad** alanına, Microsoft Azure portalına kaydettiğiniz uygulama adını girin.
    - **Kullanıcı kimliği** alanında, Human Resources ve Power Apps ortamında yönetici izinlerine sahip olan kullanıcının kullanıcı kimliğini seçin.

3. İkinci uygulama kaydını oluşturmak için **Yeni**'yi seçin.

    - **İstemci Kimliği**: f9be0c49-aa22-4ec6-911a-c5da515226ff
    - **Ad**: Dynamics 365 HR Sanal Tablosu
    - **Kullanıcı kimliği** alanında, Human Resources ve Power Apps ortamında yönetici izinlerine sahip olan kullanıcının kullanıcı kimliğini seçin.

## <a name="generate-virtual-tables"></a>Sanal tablolar oluşturma

Kurulum tamamlandığında, Dataverse örneğiniz içinde oluşturmak ve etkinleştirmek istediğiniz sanal tabloları seçebilirsiniz.

1. Human Resources'ta **Microsoft Dataverse tümleştirmesi** sayfasını açın.

2. **Sanal tablolar** sekmesini seçin.

> [!NOTE]
> **Sanal tabloları etkinleştir** geçiş düğmesi, gerekli tüm kurulum tamamlandığında otomatik olarak **Evet** olarak ayarlanır. Geçiş düğmesi **Hayır** olarak ayarlanmışsa, tüm önkoşul kurulumun tamamlandığından emin olmak için bu belgenin önceki bölümlerindeki adımları gözden geçirin.

3. Dataverse'te oluşturmak istediğiniz tabloyu veya tabloları seçin.

4. **Oluştur/Yenile**'yi seçin.

![Dataverse Tümleştirmesi](./media/hr-admin-integration-dataverse-integration.png)

## <a name="check-table-generation-status"></a>Tablo oluşturma durumunu denetleme

Sanal tablolar Dataverse içinde zaman uyumsuz bir arka plan işleminde oluşturulur. İşlemin üzerindeki güncelleştirmeler işlem merkezinde görüntülenebilir. Hata günlükleri de dahil olmak üzere işlemle ilgili ayrıntılar, **işlem otomasyonları** sayfasında görüntülenir.

1. Human Resources'da, **İşlem otomasyonları** sayfasını açın.

2. **Arka plan işlemleri** sekmesini seçin.

3. **Sanal tablo yoklama asenkron operasyonu arka plan işlemi**'ni seçin.

4. **En son sonuçları görüntüle**'yi seçin.

Yan taraftaki bölme işlemle ilgili en son yürütme sonuçlarını görüntüler. Dataverse'ten gelen tüm hatalar da dahil olmak üzere, işlem günlüğünü görüntüleyebilirsiniz.

## <a name="see-also"></a>Ayrıca bkz.

[Dataverse nedir?](/powerapps/maker/common-data-service/data-platform-intro)<br>
[Dataverse'teki tablolar](/powerapps/maker/common-data-service/entity-overview)<br>
[Tablo ilişkilerine genel bakış](/powerapps/maker/common-data-service/relationships-overview)<br>
[Harici veri kaynağından veri içeren sanal tablolar oluşturma ve düzenleme](/powerapps/maker/common-data-service/create-edit-virtual-entities)<br>
[Power Apps portalları nedir?](/powerapps/maker/portals/overview)<br>
[Power Apps'ta uygulamalar oluşturmaya genel bakış](/powerapps/maker/)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
