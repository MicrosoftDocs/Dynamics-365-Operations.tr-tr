---
title: Sosyal kimlik sağlayıcıları ekleme
description: Bu makalede, Microsoft Azure portala sosyal içerik kimlik sağlayıcılarının nasıl ekleneceği açıklanır.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 5596097a5484acafda54adcfffa68fb59c8fbc65
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785332"
---
# <a name="add-social-identity-providers"></a>Sosyal kimlik sağlayıcıları ekleme

[!include [banner](includes/banner.md)]

Bu makalede, Microsoft Azure portala sosyal içerik kimlik sağlayıcılarının nasıl ekleneceği açıklanır.

Sosyal kimlik sağlayıcıları kullanıcıların kimlik doğrulama için sosyal hesaplarını kullanmalarına olanak tanır. Sosyal kimlik sağlayıcı kimlik doğrulaması ekleme Dynamics 365 Commerce'ta isteğe bağlıdır. 

Sosyal kimlik sağlayıcı kimlik doğrulaması eklenmezse, varsayılan Azure Active Directory (Azure AD) B2C profilleri kullanıcı tabanınızın ana profilleri olacaktır. Kullanıcılar kendi kullanıcı adını (tercih ettikleri e-posta adresi) seçer ve bir parola ayarlar. Azure AD B2C, kullanıcıların kimliklerini doğrudan doğrular. 

Sosyal kimlik sağlayıcı kimlik doğrulaması eklenir ve kullanıcı sunulan sosyal kimlik sağlayıcılardan birini seçerse, Azure AD B2C kiracısında yine de bir varlık oluşturulur. Azure AD B2C, kullanıcının kimlik bilgilerini sosyal kimlik sağlayıcıyla doğrulayacaktır.

> [!NOTE]
> Kimlik sağlayıcı oturum açma işlemi B2C kiracısı içinde bir kayıt oluşturur ancak bu kayıt, kimlik doğrulama için harici sosyal kimlik sağlayıcı referansı çağıracağından yerel hesaplardan farklı bir biçimdedir. Kullanıcı, sosyal kimlik sağlayıcılarında aynı e-posta adresini kullanabilir; bu, kimlik doğrulama için kullanılan e-posta kullanıcı adının kiracı için benzersiz olmayabileceği anlamına gelir. Azure AD B2C, yalnızca kullanıcıların yerel B2C hesaplarında benzersiz bir e-posta adresine sahip olmasını zorunlu kılar.

Kimlik doğrulama için bir sosyal kimlik sağlayıcısı eklemeden önce, kimlik sağlayıcının portalına gitmeniz ve Azure AD B2C belgelerinde belirtildiği gibi bir kimlik sağlayıcı uygulaması ayarlamanız gerekir. Belge bağlantılarının listesi aşağıda verilmiştir.

- [Amazon](/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [Azure AD (Tek Kiracı)](/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [Microsoft Hesabı](/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [Facebook](/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [GitHub](/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [Google](/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [LinkedIn](/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [OpenID Connect](/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [Twitter](/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a>Sosyal kimlik sağlayıcı ekleme ve ayarlama

> [!NOTE]
> Sosyal içerik kimlik sağlayıcıları eklemek, Microsoft Dynamics 365 Commerce'da işletme- müşteri arası (B2C) kiracı ayarlarken isteğe bağlı bir adımdır.

Bir sosyal kimlik sağlayıcısı eklemek ve ayarlamak için aşağıdaki adımları izleyin.  

1. Azure portalında **Kimlik Sağlayıcılar**'a gidin.
1. **Ekle**'yi seçin. **Kimlik sağlayıcı ekle** ekranı görünür.
1. **Ad** altında, kullanıcılara oturum açma ekranında gösterilecek adı girin.
1. **Kimlik sağlayıcı türü** altında, listeden bir kimlik sağlayıcı seçin.
1. **Tamam**'ı seçin.
1. **Sosyal kimlik sağlayıcı ayarla** ekranına erişmek için **Bu kimlik sağlayıcıyı ayarla**'yı seçin.
1. **İstemci Kimliği** altında, kimlik sağlayıcı uygulaması kurulumundan elde edilen istemci kimliğini girin.
1. **İstemci gizli anahtarı** altında, kimlik sağlayıcı uygulaması kurulumundan elde edilen istemci gizli anahtarını girin.
1. Oturum açma/kaydolma ilkeleri için kullanıcı akışı ekleme:
1. **Azure AD B2C – Kullanıcı akışları (ilkeler) \> {oturum açma kayıt olma ilkeniz} \> Kimlik sağlayıcılar**'a gidin.
1. Oturum aç/kaydol kullanıcı akışı ilkesini eklemek için, hesabınız için ayarladığınız her bir kimlik sağlayıcısını seçin. Akışları  test etmek amacıyla her bir kimlik sağlayıcısı için **Kullanıcı akışını çalıştır**'ı seçin. Yeni bir sekme, yeni kimlik sağlayıcı seçim kutusunu görüntüleyen oturum açma sayfasını görüntüleyecektir.

Aşağıdaki resim, Azure AD B2C'deki **Kimlik sağlayıcı ekle** ve **Sosyal kimlik sağlayıcı ayarla** ekranlarının örneğini gösterir.

![Uygulamanıza bir Sosyal Kimlik Sağlayıcı ekleme.](./media/B2CImage_14.png)

Aşağıdaki resimde, Azure AD B2C **Kimlik Sağlayıcıları** sayfasında kimlik sağlayıcılarının nasıl seçileceği gösterilmektedir.

![İlkeniz için etkinleştirilecek her Sosyal Kimlik Sağlayıcıyı seçme.](./media/B2CImage_16.png)

Aşağıdaki resimde, sosyal kimlik sağlayıcı oturum açma düğmesinin görüntülendiği varsayılan oturum açma ekranı örneği gösterilmektedir.

> [!NOTE]
> Kullanıcı akışlarınız için Commerce'te oluşturulmuş özel sayfaları kullanıyorsanız, sosyal kimlik sağlayıcıları düğmelerinin, Commerce modül kütüphanesinin genişletilebilirlik özellikleri kullanılarak eklenmesi gerekecektir. Ek olarak, uygulamalarınızı belirli bir sosyal içerik kimliği sağlayıcısıyla ayarlarken, bazı durumlarda URL veya yapılandırma dizeleri büyük/küçük harf duyarlı olabilir. Daha fazla bilgi için sosyal içerik kimliği sağlayıcınızın bağlantı yönergelerine bakın.
 
![Sosyal Kimlik Sağlayıcı oturum açma düğmesinin görüntülendiği varsayılan oturum açma ekranı örneği.](./media/B2CImage_17.png)

## <a name="next-steps"></a>Sonraki adımlar

Commerce'ta bir B2C kiracısı ayarlama işlemine devam etmek için [Commerce Headquarters'ı yeni Azure AD B2C bilgileriyle güncelleştirme](update-hq-aad-b2c-info.md) bölümüne ilerleyin.

## <a name="additional-resources"></a>Ek kaynaklar

[Commerce'ta B2C kiracısı ayarlama](set-up-b2c-tenant.md)

[Azure portalında mevcut bir Azure AD B2C kiracısı oluşturma veya bu kiracıya bağlantı sağlama](create-link-aad-b2c-tenant.md)

[B2C uygulaması oluşturma](create-b2c-app.md)

[Kullanıcı akış ilkeleri oluşturma](create-user-flow-policies.md)

[Commerce Headquarters'ı yeni Azure AD B2C bilgileri ile güncelleştirme](update-hq-aad-b2c-info.md)

[Commerce site oluşturucuda B2C kiracınızı yapılandırma](config-b2c-tenant-site-builder.md)

[Ek B2C bilgileri](additional-b2c-info.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
