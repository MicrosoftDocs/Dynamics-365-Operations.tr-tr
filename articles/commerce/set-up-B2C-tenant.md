---
title: Commerce'ta B2C kiracısı ayarlama
description: Bu konu, Dynamics 365 Commerce'ta kullanıcı sitesi kimlik doğrulaması için Azure Active Directory (Azure AD) işletme-müşteri arası (B2C) kiracılarınızın nasıl kurulacağını açıklamaktadır.
author: BrianShook
ms.date: 02/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.dyn365.ops.version: ''
ms.openlocfilehash: dcd5c022c00070922e287a6b8750810ff76bc26f
ms.sourcegitcommit: 39f1455215e0363cd1449bbc6bdff489097f9ded
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2022
ms.locfileid: "8092471"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a>Commerce'ta B2C kiracısı ayarlama

[!include [banner](includes/banner.md)]

Bu konu, Dynamics 365 Commerce'ta kullanıcı sitesi kimlik doğrulaması için Azure Active Directory (Azure AD) işletme-müşteri arası (B2C) kiracılarınızın nasıl kurulacağını açıklamaktadır.

Dynamics 365 Commerce, kullanıcı kimlik bilgileri ve kimlik doğrulama akışlarını desteklemek için Azure AD B2C kullanır. Kullanıcı, bu akışlar aracılığıyla kaydolabilir, oturum açabilir ve parolasını sıfırlayabilir. Azure AD B2C kullanıcının hassas kimlik doğrulama bilgilerini (örneğin, kullanıcı adı ve parolası) depolar. B2C kiracısındaki kullanıcı kaydı, bir B2C yerel hesap kaydını ya da B2C sosyal kimlik sağlayıcısı kaydını depolar. Bu B2C kayıtları Commerce ortamındaki müşteri kaydına geri bağlantı sağlar.

> [!WARNING] 
> Azure AD B2C, 1 Ağustos 2021'den itibaren eski Kullanıcı akışlarını devre dışı bırakıyor. Bu nedenle, Kullanıcı akışlarınızı önerilen yeni sürüme geçirmeyi planlamalısınız. Yeni sürüm, özellik eşliği ve yeni özellikler sağlar. Commerce sürüm 10.0.15 veya üzeri için modül kitaplığı önerilen B2C Kullanıcı akışlarıyla kullanılmalıdır. Daha fazla bilgi için, [Azure Active Directory B2C'deki Kullanıcı akışları](/azure/active-directory-b2c/user-flow-overview) konusuna bakın.
 
 > [!NOTE]
 > Commerce değerlendirme ortamları Gösterim amacıyla önceden yüklenmiş bir Azure AD B2C kiracısı ile gelir. Aşağıdaki adımları kullanarak kendi Azure AD B2C kiracınızı yüklemek, değerlendirme ortamları için gerekli değildir.

> [!TIP]
> Azure AD Kimlik Koruması ve Koşullu Erişim ile site kullanıcılarınızı daha fazla koruyabilir ve Azure AD B2C kiracılarınızın güvenliğini artırabilirsiniz. Azure AD B2C Premium P1 ve Premium P2 kiracılarına sunulan özellikleri incelemek için bkz. [Azure AD B2C için Kimlik Koruması ve Koşullu Erişim](/azure/active-directory-b2c/conditional-access-identity-protection-overview).

## <a name="dynamics-environment-prerequisites"></a>Dynamics ortam önkoşulları

Başlamadan önce, aşağıdaki önkoşulları yerine getirmesini sağlayarak Dynamics 365 Commerce ortamınızın ve e-ticaret kanalınızın uygun şekilde yapılandırıldığından emin olun.

- Commerce genel merkezindeki **AllowAnonymousAccess** POS işlemleri değerini "1" olarak ayarlayın:
    1. **POS İşlemleri**'ne gidin.
    1. İşlemler ızgarasında sağ tıklayın ve **Kişiselleştir**'i seçin.
    1. **Alan ekle**'yi seçin.
    1. Kullanılabilir sütunlar listesinde, **AllowAnonymousAccess** sütununu seçerek ekleyin.
    1. **Güncelleştir**'i seçin
    1. **612** "Müşteri ekleme" işlemi için **AllowAnonymousAccess**'i "1" olarak değiştirin.
    1. **1090 (Kayıtlar)** işini çalıştırın.
- Commerce genel merkezindeki numara sırası müşteri hesabı **El İle** özniteliğini **Hayır** olarak ayarlayın:
    1. **Retail ve Commerce \> Genel merkez ayarı \> Parametreler \> Alacak hesapları parametreleri**'ne gidin.
    1. **Numara serileri**'ni seçin.
    1. **Müşteri hesabı** satırında, **Numara Sıra Kodu** değerini çift tıklayın.
    1. Numara serisinin **Genel** hızlı sekmesinde, **El İle** seçeneğini **Hayır** olarak ayarlayın.

Dynamics 365 Commerce ortamınızın dağıtımından sonra, ortamda [Çekirdek verileri başlatma](enable-configure-retail-functionality.md) da önerilir.

## <a name="create-or-link-to-an-existing-azure-ad-b2c-tenant-in-the-azure-portal"></a>Azure portalında mevcut bir Azure AD B2C kiracısı oluşturma veya bu kiracıya bağlantı sağlama

Bu bölüm, Commerce sitenizde kullanılmak üzere bir Azure AD B2C kiracısı oluşturmayı veya bağlamayı kapsamaktadır. Daha fazla bilgi için bkz. [Öğretici: Azure Active Directory B2C kiracısı oluşturma](/azure/active-directory-b2c/tutorial-create-tenant).

1. [Azure portalında](https://portal.azure.com/) adresinden oturum açın.
1. Azure portalı menüsünden, **Kaynak oluştur**'u seçin. Commerce ortamınızla bağlanacak aboneliği ve dizini kullandığınızdan emin olun.

    ![Azure Portalında Kaynak Oluşturma.](./media/B2CImage_1.png)

1. **Kimlik \> Azure Active Directory B2C**'ye gidin.
1. **Yeni B2C Kiracısı Oluştur veya mevcut bir Kiracıya bağla** sayfasında, şirketinizin gereksinimlerine en uygun olan aşağıdaki seçeneklerden birini kullanın:

    - **Yeni Azure AD B2C kiracısı oluştur**: Yeni bir Azure AD B2C kiracısı oluşturmak için bu seçeneği kullanın.
        1. **Yeni bir Azure AD B2C Kiracısı oluştur**'u seçin.
        1. **Kuruluş adı** altında, kuruluş adını girin.
        1. **İlk etki alanı adı** altında, ilk etki alanı adını girin.
        1. **Ülke veya bölge** için ülkeyi veya bölgeyi seçin.
        1. Kiracı oluşturmak için **Oluştur**'u seçin.

     ![Yeni bir Azure AD Kiracısı Oluşturma.](./media/B2CImage_2.png)

     - **Mevcut Azure AD B2C kiracısını Azure aboneliğime bağla**: Bu seçeneği, zaten bağlanmak istediğiniz bir Azure AD B2C kiracınız varsa kullanın.
        1. **Mevcut Azure AD B2C Kiracısını Azure aboneliğime bağla**'yı seçin.
        1. **Azure AD B2C Kiracısı** için uygun B2C kiracısını seçin. Seçim kutusunda "Uygun B2C Kiracısı bulunamadı" iletisi görünürse, mevcut bir uygun B2C kiracınız yoktur ve yenisini oluşturmanız gerekir.
        1. **Kaynak grubu** için **Yeni oluştur**'u seçin. Kiracıyı içerecek kaynak grubu için bir **Ad** girin, **Kaynak grubu konumu**'nu ve ardından **Oluştur**'u seçin.

    ![Mevcut Azure AD B2C Kiracısını Azure Aboneliğine Bağlama.](./media/B2CImage_3.png)

1. Yeni Azure AD B2C dizini oluşturulduktan sonra (bu birkaç dakika sürebilir), panoda yeni dizine bir bağlantı görüntülenir. Bu bağlantı sizi "Azure Active Directory B2C'ye hoş geldiniz" sayfasına yönlendirir.

    ![Yeni Azure AD Dizinine bağlama](./media/B2CImage_4.png)

> [!NOTE]
> Azure hesabınızda birden fazla aboneliğiniz varsa veya etkin bir aboneliğe bağlamadan B2C kiracısı ayarladıysanız, **Sorun giderme** başlığı sizi kiracıyı aboneliğe bağlamaya yönlendirecektir. Sorun giderme iletisini seçin ve abonelik sorununu gidermek için yönergeleri izleyin.

Aşağıdaki resimde, bir Azure AD B2C **Sorun giderme** başlığı örneği gösterilmektedir.

![Dizinde Etkin Abonelik olmadığını gösteren uyarı.](./media/B2CImage_5.png)

## <a name="create-the-b2c-application"></a>B2C uygulaması oluşturma

B2C kiracısı oluşturulduktan sonra, Commerce ile etkileşimde bulunmak için yeni Azure AD B2C kiracınız içinde bir B2C uygulaması oluşturacaksınız.

B2C uygulaması oluşturmak için şu adımları izleyin.

1. Azure portalında **Uygulama kayıtları**'na gidin ve ardından **Yeni kayıt**'ı seçin.
1. **Ad** altında, bu Azure AD B2C uygulamasına verilecek adı girin.
1. **Desteklenen hesap türleri altında**, **herhangi bir kimlik sağlayıcısı veya kuruluş dizinindeki hesaplar (Kullanıcı akışı olan kullanıcıların kimliklerini doğrulamak için)** seçeneğini belirleyin.
1. **Yeniden yönlendirme URI'ı** için, **Web** yazarak adanmış yanıt URL'nizi girin. Yanıt URL'leri ve nasıl biçimlendirilecekleri hakkında bilgi almak için [Yanıt URL'leri](#reply-urls) konusuna bakın. Bir kullanıcının kimliği doğrulandığında, Azure AD B2C'den sitenize yeniden yönlendirmeler sağlamak için yeniden yönlendirme URI/yanıt URL'si girilmelidir. Yanıt URL'si kayıt işlemi sırasında eklenebilir veya daha sonra, B2C uygulamasının **Genel Bakış** bölümündeki **Özet** menüsünden **Yeniden yönlendirme URI'si ekle** bağlantısı seçilerek eklenebilir.
1. **İzinler** için **openid ve offline_access izinleri için yönetici izni ver**'i seçin.
1. **Kayıt**'ı seç.
1. Yeni oluşturulan uygulamayı seçin ve **Kimlik doğrulama** menüsüne gidin. 
1. Yanıt URL'si girilirse, **Örtük onay ve karma akışlar** altında, uygulama için bunları etkinleştirmek üzere her iki **Erişim belirteci** ve **Kimlik belirteci** seçeneğini belirleyin ve sonra **Kaydet**'i seçin. Kayıt sırasında yanıt URL'si girilmediyse, **Platform ekle**, **Web**'i seçerek ve uygulamanın yeniden yönlendirme URI'sini seçerek de bu sayfaya eklenebilirler. **Örtük onay ve karma akışlar** bölümü daha sonra hem **Erişim belirteçleri** hem de **Kimlik belirteci** seçeneklerini belirlemek için kullanılabilir olacaktır.
1. Azure Portal'ın **Genel bakış** menüsüne gidin ve **uygulama (istemci) kimliğini** kopyalayın. Sonraki kurulum adımları için bu ID'yi not edin (ileride **istemci GUID** olarak başvurulur).

Azure AD B2C'deki uygulama kayıtları hakkında ek bilgi için, lütfen [Azure Active Directory B2C için yeni uygulama kayıtları deneyimine bakın](/azure/active-directory-b2c/app-registrations-training-guide)

### <a name="reply-urls"></a>Yanıt URL'leri

Yanıt URL'leri, siteniz bir kullanıcı kimliğini doğrulamak için Azure AD B2C çağırdığında dönüş etki alanlarını için izin listesi sağladığından önemlidir. Bu, kimliği doğrulanmış kullanıcının oturum açtığı etki alanına (site etki alanı) geri döndürülmesini sağlar. 

**Azure AD B2c - Uygulamalar \> Yeni uygulama** ekranındaki **Yanıt URL'si** kutusunda, hem sitenizin etki alanı hem de (ortamınız sağlandıktan sonra) Commece tarafından oluşturulan URL için ayrı satırlar eklemeniz gerekir. Bu URL'lerin her zaman geçerli bir URL biçimi kullanması ve yalnızca temel URL'ler olması gerekir (sonunda eğik çizgi veya yollar olmamalıdır). Ardından ``/_msdyn365/authresp`` dizesinin temel URL'lere aşağıdaki örneklerde gösterildiği şekilde eklenmesi gerekir.

- ``https://www.fabrikam.com/_msdyn365/authresp``(Etki alanı e-ticaret etki alanıyla tamamen eşleşmelidir. Birden çok etki alanınız varsa, her etki alanı için bu URL'yi eklemeniz gerekir.)
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="create-user-flow-policies"></a>Kullanıcı akış ilkeleri oluşturma

Kullanıcı akışları, Azure AD B2C'nin güvenli oturum açma, kaydolma, profil düzenleme ve parola kullanıcı deneyimlerini unutmak için kullandığı ilkelerdir. Dynamics 365 Commerce, Azure AD B2C kiracısı ile etkileşimde bulunmak üzere ilke eylemlerini gerçekleştirmek için bu akışları kullanır. Bir kullanıcı bu ilkelerle etkileşim kurduğunda, eylemleri gerçekleştirmek üzere Azure AD B2C kiracısına yeniden yönlendirilir.

Azure AD B2C üç temel kullanıcı akışı türü sağlar:
- Kaydolma ve oturum açma
- Profil düzenleme
- Parola sıfırlandı

Azure AD tarafından sağlanan varsayılan kullanıcı akışlarını kullanmayı seçebilirsiniz; bu durumda Azure AD B2C tarafından barındırılan sayfa görüntülenir. Alternatif olarak, bu kullanıcı akış deneyimlerinin görünümünü ve hissini denetlemek için bir HTML sayfası oluşturabilirsiniz. 

Kullanıcı ilkesi sayfalarını Dynamics 365 Commerce'te oluşturulan sayfalarla özelleştirmek için bkz. [Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama](custom-pages-user-logins.md). Ek bilgi için bkz. [Azure Active Directory B2C'de kullanıcı arabirimi deneyimlerini özelleştirme](/azure/active-directory-b2c/tutorial-customize-ui).

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a>Kullanıcı akış ilkesinde kaydolma ve oturum açma oluşturma

Kullanıcı akışı ilkesinde kaydolma ve oturum açma oluşturmak için aşağıdaki adımları izleyin.

1. Azure portalında, sol gezinti bölmesinde **Kullanıcı akışları (ilkeler)** öğesini seçin.
1. **Azure AD B2C - Kullanıcı akışları (ilkeler)** sayfasında, **Yeni Kullanıcı Akışı**'nı seçin.
1. **Kaydolma ve oturum açma** ilkesini seçin ve ardından **önerilen** sürümünü seçin.
1. **Ad** altında bir ilke adı girin. Bu ad, daha sonra portalın atadığı bir önekle (örneğin, "B2C_1_") birlikte görüntülenecektir.
1. **Kimlik sağlayıcıları** altında , **Yerel hesaplar** bölümünde, **E-posta kaydı** seçeneğini belirleyin. Commerce için birçok genel senaryoda e-posta kimlik doğrulaması kullanılır. Sosyal içerik kimlik sağlayıcısı kimlik doğrulaması da kullanıyorsanız, bunlar şu anda seçilebilir.
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

Aşağıdaki resim, kullanıcı akışında Azure AD B2C kayıt olma ve oturum açmayla ilgili bir örnektir.

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

## <a name="add-social-identity-providers-optional"></a>Sosyal kimlik sağlayıcıları ekleme (İsteğe bağlı)

Sosyal kimlik sağlayıcıları kullanıcıların kimlik doğrulama için sosyal hesaplarını kullanmalarına olanak tanır. Sosyal kimlik sağlayıcı kimlik doğrulaması ekleme Dynamics 365 Commerce'ta isteğe bağlıdır. 

Sosyal kimlik sağlayıcı kimlik doğrulaması eklenmezse, varsayılan Azure AD B2C profilleri kullanıcı tabanınızın ana profilleri olacaktır. Kullanıcılar kendi kullanıcı adını (tercih ettikleri e-posta adresi) seçer ve bir parola ayarlar. Azure AD B2C, kullanıcıların kimliklerini doğrudan doğrular. 

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

Bir sosyal kimlik sağlayıcısı eklemek ve ayarlamak için aşağıdaki adımları izleyin.  

1. Azure portalında **Kimlik Sağlayıcılar**'a gidin.
1. **Ekle**'yi seçin. **Kimlik sağlayıcı ekle** ekranı görünür.
1. **Ad** altında, kullanıcılara oturum açma ekranında gösterilecek adı girin.
1. **Kimlik sağlayıcı türü** altında, listeden bir kimlik sağlayıcı seçin.
1. **Tamam**'ı seçin.
1. **Sosyal kimlik sağlayıcı ayarla** ekranına erişmek için **Bu kimlik sağlayıcıyı ayarla**'yı seçin.
1. **İstemci Kimliği** altında, kimlik sağlayıcı uygulaması kurulumundan elde edilen istemci kimliğini girin.
1. **İstemci gizli anahtarı** altında, kimlik sağlayıcı uygulaması kurulumundan elde edilen istemci gizli anahtarını girin.
1. Kaydolma oturum açma ilkeleri için kullanıcı akışı ekleme:
1. **Azure AD B2C – Kullanıcı akışları (ilkeler) \> {oturum açma kayıt olma ilkeniz} \> Kimlik sağlayıcılar**'a gidin.
1. Oturum aç/kaydol kullanıcı akışı ilkesini eklemek için, hesabınız için ayarladığınız her bir kimlik sağlayıcısını seçin. Bunları test etmek amacıyla her bir kimlik sağlayıcısı için **Kullanıcı akışını çalıştır**'ı seçin. Yeni bir sekme, yeni kimlik sağlayıcı seçim kutusunu görüntüleyen oturum açma sayfasını görüntüleyecektir.

Aşağıdaki resim, Azure AD B2C'deki **Kimlik sağlayıcı ekle** ve **Sosyal kimlik sağlayıcı ayarla** ekranlarının örneğini gösterir.

![Uygulamanıza bir Sosyal Kimlik Sağlayıcı ekleme.](./media/B2CImage_14.png)

Aşağıdaki resimde, Azure AD B2C **Kimlik Sağlayıcıları** sayfasında kimlik sağlayıcılarının nasıl seçileceği gösterilmektedir.

![İlkeniz için etkinleştirilecek her Sosyal Kimlik Sağlayıcıyı seçme.](./media/B2CImage_16.png)

Aşağıdaki resimde, sosyal kimlik sağlayıcı oturum açma düğmesinin görüntülendiği varsayılan oturum açma ekranı örneği gösterilmektedir.

> [!NOTE]
> Kullanıcı akışlarınız için Commerce'te oluşturulmuş özel sayfaları kullanıyorsanız, sosyal kimlik sağlayıcıları düğmelerinin, Commerce modül kütüphanesinin genişletilebilirlik özellikleri kullanılarak eklenmesi gerekecektir. Ek olarak, uygulamalarınızı belirli bir sosyal içerik kimliği sağlayıcısıyla ayarlarken, bazı durumlarda URL veya yapılandırma dizeleri büyük/küçük harf duyarlı olabilir. Daha fazla bilgi için sosyal içerik kimliği sağlayıcınızın bağlantı yönergelerine bakın.
 
![Sosyal Kimlik Sağlayıcı oturum açma düğmesinin görüntülendiği varsayılan oturum açma ekranı örneği.](./media/B2CImage_17.png)

## <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a>Commerce Headquarters'ı yeni Azure AD B2C bilgileri ile güncelleştirme

Yukarıdaki Azure AD B2C sağlama adımları tamamlandıktan sonra, Azure AD B2C uygulamasının Dynamics 365 Commerce ortamınıza kaydedilmesi gerekir.

Genel merkezi Azure AD B2C bilgileriyle güncelleştirmek için aşağıdaki adımları izleyin.

1. Commerce'ta **Commerce Paylaşılan Parametreleri**'ne gidin ve sol menüde **Kimlik Sağlayıcılar**'ı seçin.
1. **Kimlik Sağlayıcılar** altında aşağıdakileri yapın:
    1. **Veren** kutusuna, kimlik sağlayıcı verenin URL'sini girin. Veren URL'nizi bulmak için, aşağıdaki [Verenin URL'sini al](#obtain-issuer-url) bölümüne bakın.
    1. **Ad** kutusuna, veren kaydınız için bir ad girin.
    1. **Tür** kutusuna, **Azure AD B2C (id_token)** girin.
1. **Bağlı Olan Taraflar** altında, yukarıdaki B2C kimlik sağlayıcı öğesi seçiliyken aşağıdakileri yapın:
    1. **İstemci Kimliği** kutusuna, B2C uygulama kimliğinizi girin. Bunu, B2C uygulamanızın özellikler sayfasındaki **Uygulama Kimliği** kutusunda bulabilirsiniz.
    1. **Tür** kutusuna **Genel** girin.
    1. **Kullanıcı Türü** kutusuna **Müşteri** girin.
1. Eylem bölmesinde, **Kaydet**'i seçin.
1. Commerce arama kutusunda, **Dağıtım planı**'nı arayın
1. **Dağıtım planları** sayfasının sol gezinti menüsünde, **1110 Global yapılandırma** işini seçin.
1. Eylem bölmesinde **Şimdi Çalıştır**'ı seçin.

### <a name="obtain-issuer-url"></a>Verenin URL'sini alma

Kimlik sağlayıcı veren URL'nizi almak için aşağıdaki adımları izleyin.
1. Azure Portal'ın Azure AD B2C sayfasında, **Kaydolma ve oturum açma** kullanıcı akışınıza gidin.
1. Sol gezinti menüsünde **sayfa düzenlerini** seçin, **Düzen adı** altında **Birleşik kaydolma veya oturum açma sayfası**'nı seçin ve **Kullanıcı akışını Çalıştır**'ı seçin.
1. Uygulamanızın , yukarıda oluşturulmuş olan Azure AD B2C uygulamanıza ayarlandığından emin olun ve sonra ``.../.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>`` değerini içeren **Kullanıcı akışını çalıştır** başlığı altındaki bağlantıyı seçin.
1. Tarayıcı sekmesinde bir meta veri sayfası görüntülenir. Kimlik sağlayıcısı verenin URL'sini (**"veren"** değeri) kopyalayın.
   - Örnek: ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.
 
**VEYA**: Aynı meta veri URL'sini el ile oluşturmak için aşağıdaki adımları uygulayın.

1. B2C kiracınızı ve ilkenizi kullanarak aşağıdaki gibi bir meta veri adres URL'si oluşturun: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``
    - Örnek: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.
1. Meta veri adresi URL'sini tarayıcının adres çubuğuna girin.
1. Meta verilerde, kimlik sağlayıcı veren URL'sini (**"veren"** değeri) kopyalayın.
    - Örnek: ``https://login.fabrikam.com/011115c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.

## <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a>Commerce site oluşturucuda B2C kiracınızı yapılandırma

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
1. **Kiracı Ayarları** altında **B2C Ayarları**'nı seçin. 
1. Ana pencerede **B2C Uygulamaları**'nın yanındaki **Yönet** öğesini seçin. (Kiracınız B2C Uygulamaları listesinde görüntüleniyorsa, daha önce bir yönetici tarafından eklenmiş demektir. Aşağıdaki adım 6'da belirtilen öğelerin B2C Uygulamanız ile eşleştiğini doğrulayın.)
1. **B2C Uygulaması Ekle**'yi seçin.
1. B2C kiracısı ve uygulamanızın değerlerini kullanarak, aşağıdaki gerekli maddeleri görüntülenen forma girin. Gerekli olmayan alanlar (yıldız işareti olmayan alanlar) boş bırakılabilir.

    - **Uygulama Adı**: B2C Uygulamanızın adı, örneğin "Fabrikam B2C".
    - **Kiracı Adı**: B2C kiracısı adı (örneğin, etki alanı B2C kiracısı için "fabrikam.onmicrosoft.com" olarak görünüyorsa "Fabrikam" kullanın). 
    - **Parola Unutma İlkesi Kimliği**: Parolayı unutma kullanıcı akışı ilke kimliği, örneğin "B2C_1_PasswordReset".
    - **Kaydolma Oturum Açma İlkesi Kimliği**: Kullanıcı akış ilkesi kayıt olma ve oturum açma kimliği, örneğin "B2C_1_signup_signin".
    - **İstemci GUID'i**: B2C uygulama kimliği, örneğin "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".
    - **Profil Düzenle İlkesi Kimliği**: Profil düzenleme kullanıcı akışı ilkesi kimliği, örneğin "B2C_1A_ProfileEdit".

1. **Tamam**'ı seçin. Şimdi, B2C uygulamanızın adının listede yer aldığını görmeniz gerekir.
1. Değişikliklerinizi kaydetmek için **Kaydet**'i seçin.

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a>B2C uygulamasını sitenizle ve kanalınızla ilişkilendirme

> [!WARNING]
> Siteniz zaten bir B2C uygulamasıyla ilişkilendirilmişse, farklı bir B2C uygulamasına geçmek, bu ortamda zaten kaydolan kullanıcılar için kurulmuş olan geçerli referansları kaldırır. Değiştirilmesi durumunda, geçerli olarak atanmış olan B2C uygulamasıyla ilişkilendirilmiş kimlik bilgileri kullanıcılar tarafından kullanılamaz. 
> 
> Yalnızca kanalın B2C uygulamasını ilk kez ayarlıyorsanız veya kullanıcıların yeni B2C uygulamasıyla bu kanala yönelik yeni kimlik bilgileriyle yeniden kaydolmasını istiyorsanız, B2C uygulamasını güncelleştirin. Kanalları B2C uygulamalarıyla ilişkilendirilirken dikkatli olun ve uygulamaları açık şekilde adlandırın. Bir kanal aşağıdaki adımlarda bir B2C uygulamasıyla ilişkilendirilmezse, siteniz için o kanalda oturum açan kullanıcılar, B2C uygulamalarının **Kiracı \> B2C Ayarları** listesinde **varsayılan** olarak gösterilen B2C uygulamasına girecektir.

B2C uygulamasını sitenizle ve kanalınızla ilişkilendirmek için şu adımları izleyin.

1. Commerce site oluşturucuda sitenize gidin.
1. Sol gezinti bölmesinde, genişletmek için **Site Ayarları** seçin.
1. **Site Ayarları** altında, **Kanallar**'ı seçin.
1. **Kanallar** altındaki ana pencerede kanalı seçin.
1. Sağdaki kanal özellikleri bölmesinde, **B2C Uygulaması Seç** açılır menüsünden B2C uygulamanızın adını seçin.
1. **Kapat**'ı ve ardından **Kaydet ve Yayımla**'yı seçin.

## <a name="additional-b2c-information"></a>Ek B2C bilgileri

### <a name="customer-migration"></a>Müşteri geçişi

Müşteri kayıtlarını önceki bir kimlik sağlayıcı platformundan geçirmeyi düşünüyorsanız, lütfen müşteri geçiş gereksinimlerinizi gözden geçirmek için Dynamics 365 Commerce ekibiyle birlikte çalışın.

Müşteri geçisindeki ek Azure AD B2C belgeleri için bkz. [Kullanıcıları Azure Active Directory B2C'ye geçirme](/azure/active-directory-b2c/active-directory-b2c-user-migration).

### <a name="custom-policies"></a>Özel ilkeler

Azure AD B2C etkileşimlerini ve ilke akışlarını standart B2C ilkeleriyle sunulandan daha fazla özelleştirme hakkında ek bilgi için bkz. [Azure Active Directory'deki özel ilkeler](/azure/active-directory-b2c/active-directory-b2c-overview-custom). 

### <a name="secondary-admin"></a>İkincil yönetici

B2C kiracınızın **Kullanıcılar** bölümünde isteğe bağlı, ikincil bir yönetici hesabı eklenebilir. Bu doğrudan bir hesap veya genel bir hesap olabilir. Bir hesabı ekip kaynakları arasında paylaşmanız gerekirse, ortak hesap da oluşturulabilir. Azure AD B2C'de depolanan verilerin hassasiyeti nedeniyle, ortak hesabın şirketinizin güvenlik uygulamalarıyla yakından izlenmesi gerekir.

## <a name="additional-resources"></a>Ek kaynaklar

[Etki alanı adınızı yapılandırma](configure-your-domain-name.md)

[Yeni bir e-ticaret kiracısını dağıtma](deploy-ecommerce-site.md)

[E-ticaret sitesi oluşturma](create-ecommerce-site.md)

[Dynamics 365 Commerce sitesini çevrimiçi bir kanalla ilişkilendirme](associate-site-online-store.md)

[robots.txt dosyalarını yönetme](manage-robots-txt-files.md)

[URL yeniden yönlendirmelerini toplu olarak yükleme](upload-bulk-redirects.md)

[Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama](custom-pages-user-logins.md)

[Commerce ortamında birden fazla B2C kiracısı yapılandırma](configure-multi-B2C-tenants.md)

[İçerik teslim ağı (CDN) için destek ekleme](add-cdn-support.md)

[Konum tabanlı mağaza algılamayı etkinleştirme](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
