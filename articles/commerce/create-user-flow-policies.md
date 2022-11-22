---
title: Kullanıcı akış ilkeleri oluşturma
description: Bu makalede, Microsoft Azure portalda kullanıcı akış ilkelerinin nasıl oluşturulacağı açıklanır.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 91b9d99dfd8c3d100ca197aa499ca86799bbffc8
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785335"
---
# <a name="create-user-flow-policies"></a>Kullanıcı akış ilkeleri oluşturma

[!include [banner](includes/banner.md)]

Bu makalede, Microsoft Azure portalda kullanıcı akış ilkelerinin nasıl oluşturulacağı açıklanır.

Kullanıcı akışları, Azure Active Directory (Azure AD) işletmeden müşteriye (B2C)'nin güvenli oturum açma, kaydolma, profil düzenleme ve parola kullanıcı deneyimlerini unutmak için kullandığı ilkelerdir. Dynamics 365 Commerce, Azure AD B2C kiracısı ile etkileşimde bulunmak üzere ilke eylemlerini gerçekleştirmek için bu akışları kullanır. Bir kullanıcı bu ilkelerle etkileşim kurduğunda, eylemleri gerçekleştirmek üzere Azure AD B2C kiracısına yeniden yönlendirilir.

Azure AD B2C üç temel kullanıcı akışı türü sağlar:
- Kaydolma ve oturum açma
- Profil düzenleme
- Parola sıfırlandı

Azure AD tarafından sağlanan varsayılan kullanıcı akışlarını kullanmayı seçebilirsiniz; bu durumda Azure AD B2C tarafından barındırılan sayfa görüntülenir. Alternatif olarak, bu kullanıcı akış deneyimlerinin görünümünü ve hissini denetlemek için bir HTML sayfası oluşturabilirsiniz. 

Kullanıcı ilkesi sayfalarını Dynamics 365 Commerce'te oluşturulan sayfalarla özelleştirmek için bkz. [Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama](custom-pages-user-logins.md). Ek bilgi için bkz. [Azure Active Directory B2C'de kullanıcı arabirimi deneyimlerini özelleştirme](/azure/active-directory-b2c/tutorial-customize-ui).

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a>Kaydolma ve oturum açma kullanıcı akış ilkesi oluşturma

Kaydolma ve oturum açma kullanıcı akış ilkesi oluşturmak için aşağıdaki adımları izleyin.

1. Azure portalında, sol gezinti bölmesinde **Kullanıcı akışları (ilkeler)** öğesini seçin.
1. **Azure AD B2C - Kullanıcı akışları (ilkeler)** sayfasında, **Yeni Kullanıcı Akışı**'nı seçin.
1. **Kaydolma ve oturum açma** ilkesini seçin ve ardından **önerilen** sürümünü seçin.
1. **Ad** altında bir ilke adı girin. Bu ad, daha sonra portalın atadığı bir önekle (örneğin, "B2C_1_") birlikte görüntülenecektir.
1. **Kimlik sağlayıcıları** altında , **Yerel hesaplar** bölümünde, **E-posta kaydı** seçeneğini belirleyin. Commerce için birçok genel senaryoda e-posta kimlik doğrulaması kullanılır. Sosyal içerik kimlik sağlayıcısı kimlik doğrulaması da kullanıyorsanız şu anda bunları da seçebilirsiniz.
1. **Çok faktörlü Kimlik Doğrulaması** altında şirketiniz için uygun seçeneği belirleyin. 
1. **Kullanıcı öznitelikleri ve talepler** altında, öznitelikleri veya iade taleplerini toplamak için ilgili seçenekleri seçin. Özniteliklerin ve talep seçeneklerinin tam listesini almak için **Daha fazla göster...** seçeneğini belirleyin. Commerce aşağıdaki varsayılan seçenekleri gerekli kılar:

    | **Öznitelik topla** | **İade talebi** |
    | ---------------------- | ----------------- |
    | E-posta Adresi          | E-posta Adresleri   |
    | Verilen Ad             | Verilen Ad        |
    |                        | Kimlik Sağlayıcı |
    | Soyadı                | Soyadı           |
    |                        | Kullanıcının Nesne kodu  |

1. **Oluştur**'u seçin.

Aşağıdaki resim, Azure AD B2C kaydolma ve oturum açma kullanıcı akışıyla ilgili bir örnektir.

![Kayıt Olma ve Oturum Açma ilke ayarları.](./media/B2CImage_11.png)

   
### <a name="create-a-profile-editing-user-flow-policy"></a>Profil düzenleme kullanıcı akışı ilkesi oluşturma

Profil düzenleme kullanıcı akışı ilkesi oluşturmak için aşağıdaki adımları izleyin.

1. Azure portalında, sol gezinti bölmesinde **Kullanıcı akışları (ilkeler)** öğesini seçin.
1. **Azure AD B2C - Kullanıcı akışları (ilkeler)** sayfasında, **Yeni Kullanıcı Akışı**'nı seçin.
1. **Profil düzenleme**'yi seçin ve sonra **önerilen** sürümü seçin.
1. **Ad** altında, profil düzenleme kullanıcı akışını girin. Bu ad, daha sonra portalın atadığı bir önekle (örneğin, "B2C_1_") birlikte görüntülenecektir.
1. **Kimlik sağlayıcıları** altında , **Yerel hesaplar** bölümünde, **E-posta Oturum Açma** seçeneğini belirleyin.
1. **Kullanıcı öznitelikleri** altında, aşağıdaki onay kutularını seçin:
    
    | **Öznitelik topla** | **İade talebi** |
    | ---------------------- | ----------------- |
    |                        | E-posta Adresleri   |
    | Verilen Ad             | Verilen Ad        |
    |                        | Kimlik Sağlayıcı |
    | Soyadı                | Soyadı           |
    |                        | Kullanıcı Nesne kodu  |
    
1. **Oluştur**'u seçin.

Aşağıdaki resimde, Azure AD B2C profili düzenleme kullanıcı akışı örneği gösterilmektedir.

![Azure AD B2C profil düzenleme kullanıcı akışı örneği](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a>Parola sıfırlama kullanıcı akışı ilkesi oluşturma

Parola sıfırlama kullanıcı akışı ilkesi oluşturmak için aşağıdaki adımları izleyin.

1. Azure portalında, sol gezinti bölmesinde **Kullanıcı akışları (ilkeler)** öğesini seçin.
1. **Azure AD B2C - Kullanıcı akışları (ilkeler)** sayfasında, **Yeni Kullanıcı Akışı**'nı seçin.
1. **Parolayı sıfırla**'yı seçin ve sonra **önerilen** sürümü seçin.
1. **Ad** altında, parola sıfırlama kullanıcı akışı için bir ad girin.
1. **Kimlik sağlayıcılar** atında **E-posta adresini kullanarak parolayı sıfırla**'yı seçin.
1. **Oluştur**'u seçin.
1. **Uygulama talepleri** altında, aşağıdaki onay kutularını seçin:
    - **E-posta adresleri**
    - **Verilen Ad**
    - **Soyadı**
    - **Kullanıcı Nesne kodu**
1. **Oluştur**'u seçin.

Aşağıdaki resimde, Azure AD B2C parola sıfırlama kullanıcı akışında **Posta adresi kullanılarak parolayı sıfırla** ayarının nerede yapıldığı gösterilmektedir.

![Parola Sıfırlama ilkesinde "Posta adresini kullanarak Parolayı Sıfırla" ayarı](./media/B2CImage_13.png)

## <a name="next-steps"></a>Sonraki adımlar

Commerce'te bir B2C kiracısı ayarlama işlemine devam etmek için [Sosyal kimlik sağlayıcıları ekleme](add-social-identity-providers.md) bölümüne gidin.

## <a name="additional-resources"></a>Ek kaynaklar

[Commerce'ta B2C kiracısı ayarlama](set-up-b2c-tenant.md)

[Azure portalında mevcut bir Azure AD B2C kiracısı oluşturma veya bu kiracıya bağlantı sağlama](create-link-aad-b2c-tenant.md)

[B2C uygulaması oluşturma](create-b2c-app.md)

[Sosyal kimlik sağlayıcıları ekleme (İsteğe bağlı)](add-social-identity-providers.md)

[Commerce Headquarters'ı yeni Azure AD B2C bilgileri ile güncelleştirme](update-hq-aad-b2c-info.md)

[Commerce site oluşturucuda B2C kiracınızı yapılandırma](config-b2c-tenant-site-builder.md)

[Ek B2C bilgileri](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
