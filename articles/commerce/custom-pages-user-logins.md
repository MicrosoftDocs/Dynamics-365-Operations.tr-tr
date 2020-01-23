---
title: Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama
description: Bu konuda, Microsoft Dynamics 365 Commerce'ta Azure Active Directory (Azure AD) işletme-müşteri (B2C) kiracılar kullanıcıları için özelleştirilmiş kaydolmayı işleyen özel sayfaların nasıl oluşturulacağı açıklanmaktadır.
author: brianshook
manager: annbe
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 20bfacbc2374003814e12e7737644d118d404cc0
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945571"
---
# <a name="set-up-custom-pages-for-user-logins"></a>Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce'ta Azure Active Directory (Azure AD) işletme-müşteri (B2C) kiracılar kullanıcıları için özelleştirilmiş kaydolmayı işleyen özel sayfaların nasıl oluşturulacağı açıklanmaktadır.

## <a name="overview"></a>Genel Bakış

Dynamics 365 Commerce'te kullanıcı oturum açma akışlarını işlemek amacıyla yazılan özel sayfaları kullanmak için, Commerce ortamında başvurulacak Azure AD ilkeleri ayarlamanız gerekir. Azure AD B2C uygulamasını kullanarak "Kaydet ve oturum aç," "profil düzenlemesi" ve "parola sıfırlama" Azure AD B2C ilkelerini yapılandırabilirsiniz. Daha sonra, Azure AD B2C kiracısı ve ilke adlarına, Microsoft Dynamics Lifecycle Services (LCS) kullanılarak Commerce ortamı için yapılan sağlama işlemi sırasında başvurulabilir.

Özel ticaret sayfaları oturum açma, kayıt, hesap profili düzenleme veya parola sıfırlama modülü kullanılarak oluşturulabilir. Bu özel sayfalar için yayınlanan sayfa URL'lerine, Azure portalında Azure AD B2C ilkesi yapılandırmalarında başvurulmalıdır.

## <a name="set-up-b2c-policies"></a>B2C ilkelerini ayarla

Azure AD B2C kiracınızı ayarladıktan ve Commerce ortamınızla ilişkilendirdikten sonra, Azure portalında **Azure AD B2C** sayfasına gidin ve menüsünde, **İlkeler** altında, **Kullanıcı akışlarını (ilkeler)** seçin.

![Kullanıcı akışları (ilkeler) komutu menüde](./media/B2C_CustomPage_PoliciesMenu.png)

"Kaydet ve oturum aç", "Profil düzenlemesi" ve "parola sıfırlama" kullanıcı oturum açma akışlarını yapılandırabilirsiniz.

### <a name="configure-the-sign-up-and-sign-in-policy"></a>"Oturum aç ve oturum aç" ilkesini yapılandırın

"Oturum aç ve oturum aç" ilkesini yapılandırmak için aşağıdaki adımları izleyin.

1. **Yeni Kullanıcı akışı**'nı seçin ve **önerilen** sekmede **Kaydol ve oturum aç** ilkesini seçin.
1. İlke için bir ad girin (örneğin **B2C\_1\_KaydolOturumAç**).
1. **Kimlik sağlayıcıları** bölümünde, ilke için kullanılacak kimlik sağlayıcılarını seçin. En azından, **e-posta kaydı** seçilmelidir.
1. **Öznitelik topla** sütununda, **E-posta Adresi**, **Verilen ad** ve **Soyadı** onay kutularını seçin.
1. **İade talebi** sütununda , **e-posta adreslerinin**, **verilen ad**, **kimlik sağlayıcı**, **soyadı** ve **kullanıcının nesne kodu** onay kutularını seçin.

    ![Seçilen öznitelikler ve talepler](./media/B2C_SignInSignUp_Attributes.png)

1. İlkeyi oluşturmak için **Tamam**'ı seçin.
1. Yeni ilke adını çift tıklatın ve sonra gezinme bölmesinde **Özellikler**'i seçin.
1. **JavaScript'i zorlamayı etkinleştir sayfa düzeni (Önizleme)** seçeneğini **açık** olarak ayarlayın.

    ![Yeni ilke için Özellikler sayfası](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> İlke adı, Commerce ortamında tam olarak referans edilir. (**B2C\_1\_** öneki başvuruya dahil edilecek.) İlkeler, oluşturulduktan sonra yeniden adlandırılamaz. Commerce ortamınız için varolan bir ilkeyi değiştiriyorsanız, özgün ilkeyi silebilir ve aynı ada sahip yeni bir ilke oluşturabilirsiniz. Alternatif olarak, ortam önceden sağlanmış ise, yeni ilke adını bir servis isteği aracılığıyla gönderebilirsiniz.

Özel sayfaları oluşturduktan sonra kurulum işlemini bitirmek için bu ilkeye geri dönersiniz. Şimdilik, Azure portalında **Kullanıcı akışları (ilkeler)** sayfasına dönmek için ilkeyi kapatın.

### <a name="configure-the-profile-editing-policy"></a>"Profil düzenleme" ilkesini yapılandırın

"Profil düzenleme" ilkesini yapılandırmak üzere bu adımları izleyin.

1. **Yeni Kullanıcı akışı**'nı seçin ve **önerilen** sekmede **Profil düzenleme** ilkesini seçin.
1. İlke için bir ad girin (örneğin **B2C\_1\_ProfilDüzenleme**).
1. **Kimlik sağlayıcıları** bölümünde, ilke için kullanılacak kimlik sağlayıcılarını seçin. En azından **yerel hesap girişi** seçilmiş olmalıdır.
1. **Öznitelik topla** sütununda, **E-posta Adresleri** ve **Soyadı** onay kutularını seçin.
1. **İade talebi** sütununda , **e-posta adreslerinin**, **verilen ad**, **kimlik sağlayıcı**, **soyadı** ve **kullanıcının nesne kodu** onay kutularını seçin.
1. İlkeyi oluşturmak için **Tamam**'ı seçin.
1. Yeni ilke adını çift tıklatın ve sonra gezinme bölmesinde **Özellikler**'i seçin.
1. **JavaScript'i zorlamayı etkinleştir sayfa düzeni (Önizleme)** seçeneğini **açık** olarak ayarlayın.

Özel sayfaları oluşturduktan sonra kurulum işlemini bitirmek için bu ilkeye geri dönersiniz. Şimdilik, Azure portalında **Kullanıcı akışları (ilkeler)** sayfasına dönmek için ilkeyi kapatın.

### <a name="configure-the-password-reset-policy"></a>"Parola sıfırlama" ilkesini yapılandırın

"Parola sıfırlama" ilkesini yapılandırmak üzere bu adımları izleyin.

1. **Yeni Kullanıcı akışı**'nı seçin ve **Önizleme** sekmede **Parola sıfırlama v1.1** ilkesini seçin.

    ![Önizleme sekmesinde parola sıfırlama v 1.1 ilkesi seçildi](./media/B2C_ForgetPassword_Menu.png)

1. İlke için bir ad girin (örneğin **B2C\_1\_ParolayıUnut**).
1. **Kimlik sağlayıcılar** bölümünde, **e-posta adresini kullanarak Parolayı Sıfırla** 'yı seçin.
1. **İade talebi** sütununda , **e-posta adreslerinin**, **verilen ad**, **soyadı** ve **kullanıcının nesne kodu** onay kutularını seçin.

    ![Talepler seçildi](./media/B2C_ForgetPassword_Attributes.png)

1. İlkeyi oluşturmak için **Tamam**'ı seçin.
1. Yeni ilke adını çift tıklatın ve sonra gezinme bölmesinde **Özellikler**'i seçin.
1. **JavaScript'i zorlamayı etkinleştir sayfa düzeni (Önizleme)** seçeneğini **açık** olarak ayarlayın.

Özel sayfaları oluşturduktan sonra kurulum işlemini bitirmek için bu ilkeye geri dönersiniz. Şimdilik, Azure portalında **Kullanıcı akışları (ilkeler)** sayfasına dönmek için ilkeyi kapatın.

## <a name="build-the-custom-pages"></a>Özel sayfalar oluşturma

Kullanıcı oturum açma işlerine özel sayfalar oluşturmak için aşağıdaki adımları izleyin.

1. Commerce geliştirme araçlarında sitenize gidin.
1. Aşağıdaki beş şablonu ve beş sayfayı oluşturun:

    - **Oturum açma** şablonu ve oturum açma modülünü kullanan sayfa.
    - **Kaydolma** şablonu ve kaydolma modülünü kullanan sayfa.
    - **Parola sıfırlama** şablonu ve parola sıfırlama modülünü kullanan sayfa.
    - **Parola sıfırlama doğrulaması** şablonu ve parola sıfırlama doğrulama modülünü kullanan sayfa.
    - Hesap profili düzenleme modülünü kullanan bir **profil Düzenle** şablonu ve sayfa

Sayfaları derlediğinizde aşağıdaki yönergeleri izleyin:

- Her sayfa veya modülle ilgili iş gereksinimlerinize en uygun düzeni ve stili kullanın.
- Azure AD B2C kurulumunda kullanılması gereken tüm sayfaları ve URL 'leri yayımlayın.
- Sayfalar ve URL'ler yayımlandıktan sonra, Azure AD B2C ilkesi yapılandırmaları için kullanılması gereken URL'leri toplayın. A **?preloadscripts = true** soneki kullanıldığında, her URL 'ye eklenir.

> [!IMPORTANT]
> Göreli bağlantıları olan evrensel üstbilgileri ve altbilgileri yeniden kullanmayın. Kullanıldıkları sırada bu sayfalar Azure AD B2C etki alanında barındırılacak çünkü tüm bağlantılar için yalnızca mutlak URL'ler kullanılmalıdır.

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a>Azure AD B2C ilkelerini özel sayfa bilgileriyle konfigüre edin 

Azure portalında **Azure AD B2C** sayfasına dönün ve sonra menüde **ilkeler** altında **Kullanıcı akışları'nı (ilkeler)** seçin.

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a>"Kaydol ve oturum aç" ilkesini özel sayfa bilgileriyle güncelleştirme

"Kaydol ve oturum aç" ilkesini özel sayfa bilgileriyle güncelleştirmek için şu adımları izleyin.

1. Daha önce konfigüre ettiğiniz **oturum açma ve kaydolma** ilkesinde, gezinti bölmesinde **sayfa düzenleri**'ni seçin.
1. **Birleşik kayıt veya oturum açma sayfa** düzenini seçin.
1. **Özel sayfa içeriğini kullan** seçeneğini **Evet** olarak ayarlayın.
1. **Özel sayfa URI** alanına tam oturum açma URL 'si girin. **?preloadscripts=true** sonekini ekleyin. Örneğin ``www.<my domain>.com/sign-in?preloadscripts=true`` yazın.
1. **Sayfa düzeni sürümü (Önizleme)** alanında, **1.2.0** seçin.
1. **Yerel hesap kayıt sayfası** düzenini seçin.
1. **Özel sayfa içeriğini kullan** seçeneğini **Evet** olarak ayarlayın.
1. **Özel sayfa URI** alanına tam oturum açma URL 'si girin. **?preloadscripts=true** sonekini ekleyin. Örneğin ``www.<my domain>.com/sign-up?preloadscripts=true`` yazın.
1. **Sayfa düzeni sürümü (Önizleme)** alanında, **1.2.0** seçin.
1. **Kullanıcı öznitelikleri** bölümünde, şu adımları izleyin:

    1. **E-posta adresi**, **verilen ad** ve **Soyadı** öznitelikleri için **doğrulama gerekli** alanında **Hayır**'ı seçin.
    1. **Verilen ad** ve **Soyadı** öznitelikleri için **İsteğe bağlı** alanında **Hayır**'ı seçin.

    ![Yerel hesap kayıt sayfası ilkesi yapılandırması](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a>"Profil düzenleme" ilkesini özel sayfa bilgileriyle güncelleştirme

"Profil düzenleme" ilkesini özel sayfa bilgileriyle güncelleştirmek için şu adımları izleyin.

1. Daha önce konfigüre ettiğiniz **Profil düzenleme** ilkesinde, gezinti bölmesinde **sayfa düzenleri**'ni seçin.
1. **Profil düzenleme sayfa** düzenini seçin.
1. **Özel sayfa içeriğini kullan** seçeneğini **Evet** olarak ayarlayın.
1. **Özel sayfa URI** alanına tam profil düzenleme URL'si girin. **?preloadscripts=true** sonekini ekleyin. Örneğin ``www.<my domain>.com/profile-edit?preloadscripts=true`` yazın.
1. **Sayfa düzeni sürümü (Önizleme)** alanında, **1.2.0** seçin.
1. **Kullanıcı öznitelikleri** bölümünde, şu adımları izleyin:

    1. **E-posta adresi**, **verilen ad** öznitelikleri için **doğrulama gerekli** alanında **Hayır**'ı seçin.
    1. **Verilen ad** ve **Soyadı** öznitelikleri için **İsteğe bağlı** alanında **Hayır**'ı seçin.

### <a name="update-the-password-reset-policy-with-custom-page-information"></a>"Parola sıfırlama" ilkesini özel sayfa bilgileriyle güncelleştirme

"Parola sıfırlama" ilkesini özel sayfa bilgileriyle güncelleştirmek için şu adımları izleyin.

1. Daha önce konfigüre ettiğiniz **Parola sıfırlama** ilkesinde, gezinti bölmesinde **sayfa düzenleri**'ni seçin.
1. **Yeni parola sayfası** düzenini seçin.
1. **Özel sayfa içeriğini kullan** seçeneğini **Evet** olarak ayarlayın.
1. **Özel sayfa URI** alanına tam parola sıfırlama URL'si girin. **?preloadscripts=true** sonekini ekleyin. Örneğin ``www.<my domain>.com/passwordreset?preloadscripts=true`` yazın.
1. **Sayfa düzeni sürümü (Önizleme)** alanında, **1.2.0** seçin.
1. **Hesap doğrulama sayfası** düzenini seçin.
1. **Özel sayfa içeriğini kullan** seçeneğini **Evet** olarak ayarlayın.
1. **Özel sayfa URI** alanına tam parola sıfırlama doğrulama URL'si girin. **?preloadscripts=true** sonekini ekleyin. Örneğin ``www.<my domain>.com/passwordreset-verification?preloadscripts=true`` yazın.
1. **Sayfa düzeni sürümü (Önizleme)** alanında, **1.2.0** seçin.



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a>Etiketler ve açıklamalar için varsayılan metin dizelerini Özelleştir

Başlangıç kitinde, oturum açma modülleri, Etiketler ve açıklamalar için varsayılan metin dizeleriyle önceden doldurulur. Yazılım geliştirme setinde (SDK) Bu dizeleri, günlük modülünde bulunan Global.JSON dosyasındaki değerleri güncelleştirerek özelleştirebilirsiniz.

Örneğin, Unutulan parola bağlantısı için varsayılan metin **parola unutuldu mu?**'dur. Aşağıda bu varsayılan metin oturum açma sayfasında gösterilir.

![Oturum açma sayfasında Unutulan parola bağlantısı için varsayılan metin](./media/B2C_SignUp_ModuleFace.png)

Ancak, başlangıç seti oturum açma modülü için Global.json dosyasında **Parolayı unuttunuz mu?** metnini düzenleyebilirsiniz, aşağıdaki şekilde gösterildiği gibi.

![Oturum açma modülünün Global.json dosyasında bağlantı metni güncelleştirildi](./media/B2C_CustomizingStringsForModule.png)

Global.json dosyasını güncelleştirip değişikliklerinizi yayımladıktan sonra, yeni bağlantı metni hem ticaret hem de canlı oturum açma sayfasında bulunan modülde günlükte görüntülenir.

## <a name="additional-resources"></a>Ek kaynaklar

[Etki alanı adınızı yapılandırma](configure-your-domain-name.md)

[Yeni e-Ticaret sitesini dağıtma](deploy-ecommerce-site.md)

[e-Ticaret sitesi oluşturma](create-ecommerce-site.md)

[Çevrimiçi siteyi bir kanalla ilişkilendirme](associate-site-online-store.md)

[Robots.txt dosyalarını yönetme](manage-robots-txt-files.md)

[İçerik teslim ağı (CDN) için destek ekleme](add-cdn-support.md)

[Konum tabanlı mağaza algılamayı etkinleştirme](enable-store-detection.md)
