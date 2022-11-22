---
title: Commerce site oluşturucuda B2C kiracınızı yapılandırma
description: Bu makale, Microsoft Dynamics 365 Commerce site oluşturucuda işletme-müşteri arası (B2C) kiracınızın nasıl yapılandırılacağını açıklamaktadır.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 181edf1570f1a9d071a7fae38ff9d73ff3c068fa
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785336"
---
# <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a>Commerce site oluşturucuda B2C kiracınızı yapılandırma

[!include [banner](includes/banner.md)]

Bu makale, Microsoft Dynamics 365 Commerce site oluşturucuda işletme-müşteri arası (B2C) kiracınızın nasıl yapılandırılacağını açıklamaktadır.

Azure AD B2C kiracısı kurulumu tamamlandıktan sonra, B2C kiracısını Commerce site oluşturucuda yapılandırmanız gerekir. Yapılandırma adımları Azure portalından B2C uygulama bilgilerinin toplanmasını, bu B2C uygulama bilgilerinin site oluşturucuya girilmesini ve daha sonra B2C uygulamasının sitenizle ve kanalınızla ilişkilendirilmesini içerir.

### <a name="collect-the-required-application-information"></a>Gerekli uygulama bilgilerini toplama

Gerekli uygulama bilgilerini toplamak için aşağıdaki adımları izleyin.

1. Azure portalında **Giriş \> Azure AD B2C - Uygulama kayıtları**'na gidin.
1. Uygulamanızı seçin ve sonra sol gezinti bölmesinde uygulama ayrıntılarını elde etmek için **Genel bakış**'ı seçin.
1. **Uygulama (istemci) kimliği** başvurusunda, B2C kiracınızda oluşturulan B2C uygulamasının uygulama kodunu toplayın. Bu, daha sonra site oluşturucuda **İstemci GUID**'i olarak girilir.
1. **Yeniden yönlendirme URI**'lerini seçin ve siteniz için gösterilen yanıt URL'sini (kurulumda girilen yanıt URL'si) toplayın.
1. **Giriş \> Azure AD B2C – Kullanıcı akışları** öğesine gidin ve her kullanıcı akışı ilkesinin tam adını toplayın.

Aşağıdaki resim **Azure AD B2C - Uygulama akışları** genel bakış sayfasının bir örneğini gösterir.

![Azure AD B2C - Uygulama (istemci) kimliği vurgulanmış olarak Uygulama kayıtları genel bakış sayfası](./media/ClientGUID_Application_AzurePortal.png)

Aşağıdaki resimde, **Azure AD B2C - Kullanıcı akışları (ilkeler)** sayfasındaki kullanıcı akış ilkelerinin bir örneği gösterilmektedir.

![Her B2C ilke akışının adını toplama.](./media/B2CImage_22.png)

### <a name="enter-your-azure-ad-b2c-tenant-application-information-into-commerce"></a>Azure AD B2C kiracısı uygulama bilgilerinizi Commerce'a girme

B2C kiracısını sitelerinizle ilişkilendirmeden önce, Azure AD B2C kiracısı ayrıntılarını Commerce site oluşturucusuna girmeniz gerekir.

Azure AD B2C kiracısı uygulama bilgilerinizi Commerce'a eklemek için aşağıdaki adımları izleyin.

1. Ortamınız için Commerce site oluşturucuda yönetici olarak oturum açın.
1. Sol gezinti bölmesinde, genişletmek için **Kiracı Ayarları**'nı seçin.
1. **Kiracı Ayarları** altında, **Site kimlik doğrulama kurulumu**'nu seçin. 
1. **Site kimlik doğrulama profilleri**'nin yanındaki ana pencerede **Yönet**'i seçin. (Kiracınız site kimlik doğrulama profilleri listesinde görüntüleniyorsa, daha önce bir yönetici tarafından eklenmiş demektir. Aşağıdaki adım 6'da belirtilen öğelerin hedef B2C kurulumunuzun öğeleriyle eşleştiğini doğrulayın. Farklı kullanıcı ilke kimlikleri gibi küçük farklılıkları dikkate almak için benzer Azure AD B2C kiracıları veya uygulamaları kullanılarak da yeni bir profil oluşturulabilir.)
1. **Site kimlik doğrulama profili ekle**'yi seçin.
1. B2C kiracısı ve uygulamanızın değerlerini kullanarak, aşağıdaki gerekli maddeleri görüntülenen forma girin. Gerekli olmayan alanlar (yıldız işareti olmayan alanlar) boş bırakılabilir.

    - **Uygulama Adı**: B2C Uygulamanızın adı, örneğin "Fabrikam B2C".
    - **Kiracı Adı**: B2C kiracısı adı (örneğin, etki alanı B2C kiracısı için "fabrikam.onmicrosoft.com" olarak görünüyorsa "Fabrikam" kullanın). 
    - **Parola Unutma İlkesi Kimliği**: Parolayı unutma kullanıcı akışı ilke kimliği, örneğin "B2C_1_PasswordReset".
    - **Kaydolma Oturum Açma İlkesi Kimliği**: Kaydolma ve oturum açma kullanıcı akış ilkesi kimliği, örneğin "B2C_1_signup_signin".
    - **İstemci GUID'i**: B2C uygulama kimliği, örneğin "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".
    - **Profil Düzenle İlkesi Kimliği**: Profil düzenleme kullanıcı akışı ilkesi kimliği, örneğin "B2C_1A_ProfileEdit".

1. **Tamam**'ı seçin. Şimdi, B2C uygulamanızın adının listede yer aldığını görmeniz gerekir.
1. Değişikliklerinizi kaydetmek için **Kaydet**'i seçin.

İsteğe bağlı **Oturum açma özel etki alanı** alanı yalnızca, Azure AD B2C kiracısı için özel bir etki alanı ayarlıyorsanız kullanılmalıdır. **Oturum açma özel etki alanı** alanının kullanımıyla ilgili ek bilgiler ve değerlendirmeler için [Ek B2C bilgilerine](additional-b2c-info.md) bakın.

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a>B2C uygulamasını sitenizle ve kanalınızla ilişkilendirme

> [!WARNING]
> - Siteniz zaten bir B2C uygulamasıyla ilişkilendirilmişse, farklı bir B2C uygulamasına geçmek, bu ortamda zaten kaydolan kullanıcılar için kurulmuş olan geçerli referansları kaldırır. Değiştirilmesi durumunda, geçerli olarak atanmış olan B2C uygulamasıyla ilişkilendirilmiş kimlik bilgileri kullanıcılar tarafından kullanılamaz. 
> - Yalnızca kanalın B2C uygulamasını ilk kez ayarlıyorsanız veya kullanıcıların yeni B2C uygulamasıyla bu kanala yönelik yeni kimlik bilgileriyle yeniden kaydolmasını istiyorsanız, B2C uygulamasını güncelleştirin. Kanalları B2C uygulamalarıyla ilişkilendirilirken dikkatli olun ve uygulamaları açık şekilde adlandırın. Bir kanal aşağıdaki adımlarda bir B2C uygulamasıyla ilişkilendirilmezse, siteniz için o kanalda oturum açan kullanıcılar, B2C uygulamalarının **Kiracı \> B2C Ayarları** listesinde **varsayılan** olarak gösterilen B2C uygulamasına girecektir.

B2C uygulamasını sitenizle ve kanalınızla ilişkilendirmek için şu adımları izleyin.

1. Commerce site oluşturucuda sitenize gidin.
1. Sol gezinti bölmesinde, genişletmek için **Site Ayarları** seçin.
1. **Site Ayarları** altında, **Kanallar**'ı seçin.
1. **Kanallar** altındaki ana pencerede kanalı seçin.
1. Sağdaki kanal özellikleri bölmesinde, **B2C Uygulaması Seç** açılır menüsünden B2C uygulamanızın adını seçin.
1. **Kapat**'ı ve ardından **Kaydet ve Yayımla**'yı seçin.

## <a name="next-steps"></a>Sonraki adımlar

Commerce'te bir B2C kiracısı ayarlama işlemine devam etmek için [Ek B2C bilgilerine](additional-b2c-info.md) devam edin.

## <a name="additional-resources"></a>Ek kaynaklar

[Commerce'ta B2C kiracısı ayarlama](set-up-b2c-tenant.md)

[Azure portalında mevcut bir Azure AD B2C kiracısı oluşturma veya bu kiracıya bağlantı sağlama](create-link-aad-b2c-tenant.md)

[B2C uygulaması oluşturma](create-b2c-app.md)

[Kullanıcı akış ilkeleri oluşturma](create-user-flow-policies.md)

[Sosyal kimlik sağlayıcıları ekleme (İsteğe bağlı)](add-social-identity-providers.md)

[Commerce Headquarters'ı yeni Azure AD B2C bilgileri ile güncelleştirme](update-hq-aad-b2c-info.md)

[Ek B2C bilgileri](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
