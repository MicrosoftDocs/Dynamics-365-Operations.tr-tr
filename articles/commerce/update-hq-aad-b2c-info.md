---
title: Commerce Headquarters'ı yeni Azure AD B2C bilgileri ile güncelleştirme
description: Bu makalede, Microsoft Dynamics 365 Commerce headquarters'ın yeni Azure Active Directory (Azure AD) işletme-müşteri arası (B2C) bilgileriyle nasıl güncelleştirileceği açıklanır.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: c65949ff97182d2692319ac2af00e3ef35a79580
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785337"
---
# <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a>Commerce Headquarters'ı yeni Azure AD B2C bilgileri ile güncelleştirme

[!include [banner](includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce headquarters'ın yeni Azure Active Directory (Azure AD) işletme-müşteri arası (B2C) bilgileriyle nasıl güncelleştirileceği açıklanır.

Yukarıdaki Azure AD B2C sağlama adımları tamamlandıktan sonra, Azure AD B2C uygulamasının Dynamics 365 Commerce ortamınıza kaydedilmesi gerekir.

Genel merkezi Azure AD B2C bilgileriyle güncelleştirmek için aşağıdaki adımları izleyin.

1. Commerce'ta **Commerce Paylaşılan Parametreleri**'ne gidin ve sol menüde **Kimlik Sağlayıcılar**'ı seçin.
1. **Kimlik Sağlayıcılar** altında aşağıdakileri yapın:
    1. **Veren** kutusuna, kimlik sağlayıcı verenin dizesini girin. Verenin dizesini bulmak için aşağıdaki [Headquarters kurulumu için veren dizesini al](#obtain-issuer-string-for-headquarters-setup) bölümüne bakın.
    1. **Ad** kutusuna, veren kaydınız için bir ad girin.
    1. **Tür** kutusuna, **Azure AD B2C (id_token)** girin.
1. **Bağlı Olan Taraflar** altında, yukarıdaki B2C kimlik sağlayıcı öğesi seçiliyken aşağıdakileri yapın:
    1. **ClientID** kutusuna, B2C uygulamanızın kimliğini girin; kimliği B2C uygulamanızın özellikler sayfasındaki **Uygulama Kimliği** kutucuğunda bulabilirsiniz.
    1. **Tür** kutusuna **Genel** girin.
    1. **Kullanıcı Türü** kutusuna **Müşteri** girin.
1. Eylem bölmesinde, **Kaydet**'i seçin.
1. Commerce arama kutusunda, **Dağıtım planı**'nı arayın
1. **Dağıtım planları** sayfasının sol gezinti menüsünde, **1110 Global yapılandırma** işini seçin.
1. Eylem bölmesinde **Şimdi Çalıştır**'ı seçin.

### <a name="obtain-issuer-string-for-headquarters-setup"></a>Yönetim merkezi kurulumu için verenin dizesini al

Kimlik sağlayıcı veren dizenizi almak için aşağıdaki adımları izleyin.

1. Azure Portal'ın Azure AD B2C sayfasında, **Kaydolma ve oturum açma** kullanıcı akışınıza gidin.
1. Sol gezinti menüsünde **sayfa düzenlerini** seçin, **Düzen adı** altında **Birleşik kaydolma veya oturum açma sayfası**'nı seçin ve **Kullanıcı akışını Çalıştır**'ı seçin.
1. Uygulamanızın , yukarıda oluşturulmuş olan Azure AD B2C uygulamanıza ayarlandığından emin olun ve sonra ``.../.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>`` değerini içeren **Kullanıcı akışını çalıştır** altında görüntülenen kullanıcı akışı bağlantısını seçin. (**Kullanıcı akışını çalşıtır**'ı seçmeyin.) Veren dizesini  toplamak üzere ilkenin meta verilerini görüntüleyen yeni bir sekme açılacaktır.
1. Tarayıcı sekmesinde görüntülenen meta veri sayfasında, aşağıdaki örneğe benzer görünen kimlik sağlayıcısı vereni dizesini kopyalayın (**veren** değeri "https://" ile başlayıp ""/v2.0/" ile biter).
   - ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.
 
**VEYA**: Aynı meta veri URL'sini el ile oluşturmak için aşağıdaki adımları uygulayın.

1. B2C kiracınızı ve ilkenizi kullanarak aşağıdaki gibi bir meta veri adres URL'si oluşturun: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``
    - Örnek: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.
1. Meta veri adresi URL'sini tarayıcının adres çubuğuna girin.
1. Meta verilerde, kimlik sağlayıcı veren URL'sini (**"veren"** değeri) kopyalayın.
    - Örnek: ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.

## <a name="next-steps"></a>Sonraki adımlar

Commerce'te bir B2C kiracısı ayarlama işlemine devam etmek için [Commerce site oluşturucuda B2C kiracınızı yapılandırma](config-b2c-tenant-site-builder.md) bölümüne gidin.

## <a name="additional-resources"></a>Ek kaynaklar

[Commerce'ta B2C kiracısı ayarlama](set-up-b2c-tenant.md)

[Azure portalında mevcut bir Azure AD B2C kiracısı oluşturma veya bu kiracıya bağlantı sağlama](create-link-aad-b2c-tenant.md)

[B2C uygulaması oluşturma](create-b2c-app.md)

[Kullanıcı akış ilkeleri oluşturma](create-user-flow-policies.md)

[Sosyal kimlik sağlayıcıları ekleme (İsteğe bağlı)](add-social-identity-providers.md)

[Commerce site oluşturucuda B2C kiracınızı yapılandırma](config-b2c-tenant-site-builder.md)

[Ek B2C bilgileri](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
