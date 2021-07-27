---
title: Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama
description: Bu konuda, Microsoft Dynamics 365 Commerce'ta Azure Active Directory (Azure AD) işletme-müşteri (B2C) kiracılar kullanıcıları için özelleştirilmiş kaydolmayı işleyen özel sayfaların nasıl oluşturulacağı açıklanmaktadır.
author: brianshook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 214f99563f8bb08d8c051f904d0ca0a88267aa6b
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349662"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a>Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama

[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce'ta Azure Active Directory (Azure AD) işletme-müşteri (B2C) kiracılar kullanıcıları için özelleştirilmiş kaydolmayı işleyen özel sayfaların nasıl oluşturulacağı açıklanmaktadır.

Dynamics 365 Commerce'te kullanıcı oturum açma akışlarını işlemek amacıyla yazılan özel sayfaları kullanmak için, Commerce ortamında başvurulacak Azure AD ilkeleri ayarlamanız gerekir. Azure AD B2C uygulamasını kullanarak "Kaydet ve oturum aç," "profil düzenlemesi" ve "parola sıfırlama" Azure AD B2C ilkelerini yapılandırabilirsiniz. Daha sonra, Azure AD B2C kiracısı ve ilke adlarına, Microsoft Dynamics Lifecycle Services (LCS) kullanılarak Commerce ortamı için yapılan sağlama işlemi sırasında başvurulabilir.

Özel Commerce sayfaları oturum açma, kayıt, hesap profili düzenleme, parola sıfırlama veya genel AAD modülü kullanılarak oluşturulabilir. Bu özel sayfalar için yayınlanan sayfa URL'lerine, Azure portalında Azure AD B2C ilkesi yapılandırmalarında başvurulmalıdır.

> [!WARNING] 
> Azure AD B2C, 1 Ağustos 2021'den itibaren eski Kullanıcı akışlarını devre dışı bırakıyor. Bu nedenle, Kullanıcı akışlarınızı önerilen yeni sürüme geçirmeyi planlamalısınız. Yeni sürüm, özellik eşliği ve yeni özellikler sağlar. Daha fazla bilgi için, [Azure Active Directory B2C'deki Kullanıcı akışları](/azure/active-directory-b2c/user-flow-overview) konusuna bakın.

>Commerce sürüm 10.0.15 veya üzeri için modül kitaplığı önerilen B2C Kullanıcı akışlarıyla kullanılmalıdır. Azure AD B2C'de sunulan varsayılan kullanıcı ilkesi sayfaları da kullanılabilir ve Şirket markalaması ile ilgili ek arka plan görüntüsü, amblem ve arka plan renk değişikliklerine izin verir. Tasarım yetenekleri daha kısıtlı olsa da varsayılan kullanıcı ilkesi sayfaları, adanmış özel sayfalar oluşturup yapılandırmadan, Azure AD B2C ilkesi işlevselliği sağlar. 

## <a name="set-up-b2c-policies"></a>B2C ilkelerini ayarla

Azure AD B2C kiracınızı ayarladıktan ve Commerce ortamınızla ilişkilendirdikten sonra, Azure portalında **Azure AD B2C** sayfasına gidin ve menüsünde, **İlkeler** altında, **Kullanıcı akışlarını (ilkeler)** seçin.

![Kullanıcı akışları (ilkeler) komutu menüde.](./media/B2C_CustomPage_PoliciesMenu.png)

"Kaydet ve oturum aç", "Profil düzenlemesi" ve "parola sıfırlama" kullanıcı oturum açma akışlarını yapılandırabilirsiniz.

### <a name="configure-the-sign-up-and-sign-in-policy"></a>"Oturum aç ve oturum aç" ilkesini yapılandırın

"Oturum aç ve oturum aç" ilkesini yapılandırmak için aşağıdaki adımları izleyin.

1. **Yeni Kullanıcı akışı**'nı seçin, **Kaydol ve oturum aç**'ı seçin ve **önerilen** sekmesinde **Oluştur**'u seçin.
1. İlke için bir ad girin (örneğin **B2C\_1\_KaydolOturumAç**).
1. **Kimlik sağlayıcıları** bölümünde, ilke için kullanılacak kimlik sağlayıcılarını seçin. En azından, **e-posta kaydı** seçilmelidir.
1. **Öznitelik topla** sütununda, **E-posta Adresi**, **Verilen ad** ve **Soyadı** onay kutularını seçin.
1. **İade talebi** sütununda , **e-posta adreslerinin**, **verilen ad**, **kimlik sağlayıcı**, **soyadı** ve **kullanıcının nesne kodu** onay kutularını seçin.

    ![Seçilen öznitelikler ve talepler.](./media/B2C_SignInSignUp_Attributes.png)

1. İlkeyi oluşturmak için **Tamam**'ı seçin.
1. Yeni ilke adını çift tıklatın ve sonra gezinme bölmesinde **Özellikler**'i seçin.
1. **JavaScript'i zorlamayı etkinleştir sayfa düzeni (Önizleme)** seçeneğini **açık** olarak ayarlayın.

    ![Yeni ilke için Özellikler sayfası.](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> İlke adı, Commerce ortamında tam olarak referans edilir. (**B2C\_1\_** öneki başvuruya dahil edilecek.) İlkeler, oluşturulduktan sonra yeniden adlandırılamaz. Commerce ortamınız için varolan bir ilkeyi değiştiriyorsanız, özgün ilkeyi silebilir ve aynı ada sahip yeni bir ilke oluşturabilirsiniz. Alternatif olarak, ortam önceden sağlanmış ise, yeni ilke adını bir servis isteği aracılığıyla gönderebilirsiniz.

Özel sayfaları oluşturduktan sonra kurulum işlemini bitirmek için bu ilkeye geri dönersiniz. Şimdilik, Azure portalında **Kullanıcı akışları (ilkeler)** sayfasına dönmek için ilkeyi kapatın.

### <a name="configure-the-profile-editing-policy"></a>"Profil düzenleme" ilkesini yapılandırın

"Profil düzenleme" ilkesini yapılandırmak üzere bu adımları izleyin.

1. **Yeni Kullanıcı akışı**'nı seçin, **Profil düzenleme**'yi seçin ve **önerilen** sekmesinde **Oluştur**'u seçin.
1. İlke için bir ad girin (örneğin **B2C\_1\_ProfilDüzenleme**).
1. **Kimlik sağlayıcıları** bölümünde, ilke için kullanılacak kimlik sağlayıcılarını seçin. En azından **yerel hesap girişi** seçilmiş olmalıdır.
1. **Öznitelik topla** sütununda, **Ad** ve **Soyadı** onay kutularını seçin.
1. **İade talebi** sütununda , **e-posta adreslerinin**, **verilen ad**, **kimlik sağlayıcı**, **soyadı** ve **kullanıcının nesne kodu** onay kutularını seçin.
1. İlkeyi oluşturmak için **Tamam**'ı seçin.
1. Yeni ilke adını çift tıklatın ve sonra gezinme bölmesinde **Özellikler**'i seçin.
1. **JavaScript'i zorlamayı etkinleştir sayfa düzeni (Önizleme)** seçeneğini **açık** olarak ayarlayın.

Özel sayfaları oluşturduktan sonra kurulum işlemini bitirmek için bu ilkeye geri dönersiniz. Şimdilik, Azure portalında **Kullanıcı akışları (ilkeler)** sayfasına dönmek için ilkeyi kapatın.

### <a name="configure-the-password-reset-policy"></a>"Parola sıfırlama" ilkesini yapılandırın

"Parola sıfırlama" ilkesini yapılandırmak üzere bu adımları izleyin.

1. **Yeni Kullanıcı akışı**'nı seçin ve sonra da **parola sıfırla** seçeneğini belirleyip **Önerilen** sekmesini seçin ve **oluştur**'a tıklayın.
1. İlke için bir ad girin (örneğin **B2C\_1\_ParolayıUnut**).
1. **Kimlik sağlayıcılar** bölümünde, **e-posta adresini kullanarak Parolayı Sıfırla** 'yı seçin.
1. **İade talebi** sütununda , **e-posta adreslerinin**, **verilen ad**, **soyadı** ve **kullanıcının nesne kodu** onay kutularını seçin.
1. İlkeyi oluşturmak için **Tamam**'ı seçin.
1. Yeni ilke adını çift tıklatın ve sonra gezinme bölmesinde **Özellikler**'i seçin.
1. **JavaScript'i zorlamayı etkinleştir sayfa düzeni (Önizleme)** seçeneğini **açık** olarak ayarlayın.

Özel sayfaları oluşturduktan sonra kurulum işlemini bitirmek için bu ilkeye geri dönersiniz. Şimdilik, Azure portalında **Kullanıcı akışları (ilkeler)** sayfasına dönmek için ilkeyi kapatın.

## <a name="build-the-custom-pages"></a>Özel sayfalar oluşturma

Ayrılmış Azure AD modülleri, Azure AD B2C Kullanıcı ilkeleri için özel sayfalar oluşturmak amacıyla, Commerce'e dahil edilmiştir. Sayfalar, aşağıda ayrıntılı olarak oluşturulan ana Azure AD B2C modüllerini kullanan her Kullanıcı ilkesi sayfası düzeni için özel olarak oluşturulabilir. Alternatif olarak, **AAD genel** modülü, Azure AD B2C'deki tüm sayfa düzenleri ve ilkeleri için kullanılabilir (Aşağıda listelenmeyen ilkelerde sayfa mizanpajı seçenekleri için de). 

- Sayfaya özel Azure AD modülleri, Azure AD B2C tarafından işlenmiş olan veri giriş öğelerine bağlıdır. Bu modüller, sayfalarınızdaki öğelerin konumlandırılmasını daha fazla kontrol etmek için size daha fazla denetim sağlar. Ancak, aşağıda açıklanan varsayılan ayarların dışında kalan sapmaları dikkate almak için daha fazla sayfa ve modül uzantısı oluşturulması gerekebilir.
- **AAD genel** modülü, Kullanıcı ilkesi sayfa düzenindeki tüm öğeleri işlemesi için Azure AD B2C için "div" öğesini oluşturur; bu sayfanın B2C işlevlerine daha fazla esneklik sağlar, ancak konumlandırma ve stil ile ilgili daha az denetim sağlar (ancak CSS sitenizin görünümünü ve hissini eşleştirmek için kullanılabilir).

**AAD Genel** modülü ile tek bir sayfa oluşturabilir ve bunu tüm Kullanıcı ilkesi sayfalarınız için kullanabilir veya oturum açma, kaydolma, profil düzenleme, parola sıfırlama ve parola sıfırlama doğrulaması için bağımsız Azure AD modülleri kullanarak belirli sayfaları oluşturabilirsiniz. Ayrıca, aşağıda not edilen sayfa düzenleri için özel Azure AD sayfalarını ve bu veya diğer kullanıcı ilkeleri sayfalarındaki diğer sayfa düzenleri için genel AAD modülü sayfasını kullanarak her ikisinin karışımını kullanabilirsiniz.

Modül kitaplığıyla birlikte gelen Azure AD modülleri hakkında daha fazla bilgi edinmek için [Kimlik Yönetimi sayfalarını ve modüllerini](identity-mgmt-modules.md) okuyun.

Kullanıcı oturum açma işlerini ele almak üzere belirli kimlik modüllerine sahip özel sayfalar oluşturmak için aşağıdaki adımları izleyin.

1. Commerce site oluşturucuda sitenize gidin.
1. Aşağıdaki beş şablonu ve sayfayı oluşturun (henüz sitenizde yoksa):
    - **Oturum açma** şablonu ve oturum açma modülünü kullanan sayfa.
    - **Kaydolma** şablonu ve kaydolma modülünü kullanan sayfa.
    - **Parola sıfırlama** şablonu ve parola sıfırlama modülünü kullanan sayfa.
    - **Parola sıfırlama doğrulaması** şablonu ve parola sıfırlama doğrulama modülünü kullanan sayfa.
    - Hesap profili düzenleme modülünü kullanan bir **profil Düzenle** şablonu ve sayfa.

Sayfaları derlediğinizde aşağıdaki yönergeleri izleyin:

- Her sayfa veya modülle ilgili iş gereksinimlerinize en uygun düzeni ve stili kullanın.
- Azure AD B2C kurulumunda kullanılması gereken tüm sayfaları ve URL 'leri yayımlayın.
- Sayfalar ve URL'ler yayımlandıktan sonra, Azure AD B2C ilkesi yapılandırmaları için kullanılması gereken URL'leri toplayın. A **?preloadscripts = true** soneki kullanıldığında, her URL 'ye eklenir.

> [!IMPORTANT]
> Azure AD B2C'de başvurulmak üzere oluşturulan sayfalar doğrudan Azure AD B2C kiracısı etki alanından sunulur. Göreli bağlantıları olan evrensel üstbilgileri ve altbilgileri yeniden kullanmayın. Kullanıldıkları sırada bu sayfalar Azure AD B2C etki alanında barındırılacak çünkü tüm bağlantılar için yalnızca mutlak URL'ler kullanılmalıdır. Azure AD İlişkili özel sayfalar için mutlak URL'lerle belirli üst bilgi ve alt bilgilerle birlikte Retail Server'a bağlantının kaldırılmasını gerektiren herhangi bir Commerce'e özel modül oluşturmanız önerilir. Örneğin, sık kullanılanlar, arama çubuğu, oturum açma bağlantısı ve sepet modülleri, Azure AD B2C Kullanıcı akışlarında kullanılacak sayfalara eklenmemelidir.

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a>Azure AD B2C ilkelerini özel sayfa bilgileriyle konfigüre edin 

Azure portalında **Azure AD B2C** sayfasına dönün ve sonra menüde **ilkeler** altında **Kullanıcı akışları'nı (ilkeler)** seçin.

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a>"Kaydol ve oturum aç" ilkesini özel sayfa bilgileriyle güncelleştirme

"Kaydol ve oturum aç" ilkesini özel sayfa bilgileriyle güncelleştirmek için şu adımları izleyin.

1. Daha önce konfigüre ettiğiniz **oturum açma ve kaydolma** ilkesinde, gezinti bölmesinde **sayfa düzenleri**'ni seçin.
1. **Birleşik kayıt veya oturum açma sayfa** düzenini seçin.
1. **Özel sayfa içeriğini kullan** seçeneğini **Evet** olarak ayarlayın.
1. **Özel sayfa URI** alanına tam oturum açma URL 'si girin. **?preloadscripts=true** sonekini ekleyin. Örneğin ``www.<my domain>.com/sign-in?preloadscripts=true`` yazın.
1. **Sayfa düzeni sürümü** alanında, sürüm **2.1.0** veya sonrasını seçin (Commerce sürüm 10.0.15 veya üstü için modül kitaplığı gerektirir).
1. **Kaydet**'i seçin.
1. **Yerel hesap kayıt sayfası** düzenini seçin.
1. **Özel sayfa içeriğini kullan** seçeneğini **Evet** olarak ayarlayın.
1. **Özel sayfa URI** alanına tam oturum açma URL 'si girin. **?preloadscripts=true** sonekini ekleyin. Örneğin ``www.<my domain>.com/sign-up?preloadscripts=true`` yazın.
1. **Sayfa düzeni sürümü** alanında, sürüm **2.1.0** veya sonrasını seçin (Commerce sürüm 10.0.15 veya üstü için modül kitaplığı gerektirir).
1. **Kullanıcı öznitelikleri** bölümünde, şu adımları izleyin:
    1. **Ad** ve **Soyadı** öznitelikleri için **doğrulama gerekli** alanında **Hayır**'ı seçin.
    1. **E-posta adresi** özniteliği için **Doğrulama gerekli** sütununda varsayılan değer olan **Evet**'i seçili olarak bırakmanız önerilir. Bu seçenek, belirli bir e-posta adresiyle kaydolan kullanıcıların e-posta adresine sahip olduklarını doğrular.
    1. **E-posta adresi**, **ad** ve **Soyadı** öznitelikleri için **İsteğe bağlı** sütununda **Hayır**'ı seçin.
1. **Kaydet**'i seçin.

    ![Yerel hesap kayıt sayfası ilkesi yapılandırması.](./media/B2C_SignInSignUp_Recommended_PageLayoutExample.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a>"Profil düzenleme" ilkesini özel sayfa bilgileriyle güncelleştirme

"Profil düzenleme" ilkesini özel sayfa bilgileriyle güncelleştirmek için şu adımları izleyin.

1. Daha önce konfigüre ettiğiniz **Profil düzenleme** ilkesinde, gezinti bölmesinde **sayfa düzenleri**'ni seçin.
1. **Profil Düzenle sayfası** düzenini seçin (ekranınıza bağlı olarak, diğer düzen seçeneklerini geçmek için aşağı kaydırmak gerekebilir).
1. **Özel sayfa içeriğini kullan** seçeneğini **Evet** olarak ayarlayın.
1. **Özel sayfa URI** alanına tam profil düzenleme URL'si girin. **?preloadscripts=true** sonekini ekleyin. Örneğin ``www.<my domain>.com/profile-edit?preloadscripts=true`` yazın.
1. **Sayfa düzeni sürümü** için sürüm **2.1.0** veya sonrasını seçin (Commerce sürüm 10.0.15 veya üstü için modül kitaplığı gerektirir).
1. **Kullanıcı öznitelikleri** bölümünde, şu adımları izleyin:
    1. **Ad** ve **Soyadı** öznitelikleri için **İsteğe bağlı** sütununda **Hayır**'ı seçin.
    1. **Ad** ve **Soyadı** öznitelikleri için **doğrulama gerekli** alanında **Hayır**'ı seçin.
1. **Kaydet**'i seçin.

### <a name="update-the-password-reset-policy-with-custom-page-information"></a>"Parola sıfırlama" ilkesini özel sayfa bilgileriyle güncelleştirme

"Parola sıfırlama" ilkesini özel sayfa bilgileriyle güncelleştirmek için şu adımları izleyin.

1. Daha önce konfigüre ettiğiniz **Parola sıfırlama** ilkesinde, gezinti bölmesinde **sayfa düzenleri**'ni seçin.
1. **Parolayı unuttum sayfası** düzenini seçin.
1. **Özel sayfa içeriğini kullan** seçeneğini **Evet** olarak ayarlayın.
1. **Özel sayfa URI** alanına tam parola sıfırlama doğrulama URL'si girin. **?preloadscripts=true** sonekini ekleyin. Örneğin ``www.<my domain>.com/password-reset-verification?preloadscripts=true`` yazın.
1. **Sayfa düzeni sürümü** alanında, sürüm **2.1.0** veya sonrasını seçin (Commerce sürüm 10.0.15 veya üstü için modül kitaplığı gerektirir).
2. **Kaydet**'i seçin.
3. **Parolayı değiştir sayfası** düzenini seçin.
4. **Özel sayfa içeriğini kullan** seçeneğini **Evet** olarak ayarlayın.
5. **Özel sayfa URI** alanına tam parola sıfırlama URL'si girin. **?preloadscripts=true** sonekini ekleyin. Örneğin ``www.<my domain>.com/password-reset?preloadscripts=true`` yazın.
6. **Sayfa düzeni sürümü** alanında, sürüm **2.1.0** veya sonrasını seçin (Commerce sürüm 10.0.15 veya üstü için modül kitaplığı gerektirir).
7. **Kaydet**'i seçin.

## <a name="customize-default-text-strings-for-labels-and-descriptions"></a>Etiketler ve açıklamalar için varsayılan metin dizelerini Özelleştir

Modül kitaplığında, oturum açma modülleri, Etiketler ve açıklamalar için varsayılan metin dizeleriyle önceden doldurulur. Üzerinde çalıştığınız modülün Özellikler bölmesindeki dizeleri özelleştirebilirsiniz. Sayfada ek dizeler (**Parolanızı mı unuttunuz?** bağlantı metni veya **Hesap oluştur** eylem çağrısı metni gibi), Commerce yazılım geliştirme setini (SDK) kullanarak ve oturum açma modülü için global.json dosyasındaki değerleri güncelleştirmeyi gerektirir.

Örneğin, Unutulan parola bağlantısı için varsayılan metin **parola unutuldu mu?**'dur. Aşağıda bu varsayılan metin oturum açma sayfasında gösterilir.

![Oturum açma sayfasında Unutulan parola bağlantısı için varsayılan metin.](./media/B2C_SignUp_ModuleFace.png)

Ancak, modül kitaplığı oturum açma modülü için Global.json dosyasında **Parolayı unuttunuz mu?** metnini düzenleyebilirsiniz, aşağıdaki şekilde gösterildiği gibi.

![Oturum açma modülünün Global.json dosyasında bağlantı metni güncelleştirildi.](./media/B2C_CustomizingStringsForModule.png)

Global.json dosyasını güncelleştirip değişikliklerinizi yayımladıktan sonra, yeni bağlantı metni hem ticaret hem de canlı oturum açma sayfasında bulunan modülde günlükte görüntülenir.

## <a name="additional-resources"></a>Ek kaynaklar

[Etki alanı adınızı yapılandırma](configure-your-domain-name.md)

[Yeni bir e-ticaret kiracısını dağıtma](deploy-ecommerce-site.md)

[E-ticaret sitesi oluşturma](create-ecommerce-site.md)

[Dynamics 365 Commerce sitesini çevrimiçi bir kanalla ilişkilendirme](associate-site-online-store.md)

[robots.txt dosyalarını yönetme](manage-robots-txt-files.md)

[URL yeniden yönlendirmelerini toplu olarak yükleme](upload-bulk-redirects.md)

[Commerce'ta B2C kiracısı ayarlama](set-up-B2C-tenant.md)

[Commerce ortamında birden fazla B2C kiracısı yapılandırma](configure-multi-B2C-tenants.md)

[İçerik teslim ağı (CDN) için destek ekleme](add-cdn-support.md)

[Konum tabanlı mağaza algılamayı etkinleştirme](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]