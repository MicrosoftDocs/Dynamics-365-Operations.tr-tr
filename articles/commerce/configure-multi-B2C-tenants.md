---
title: Commerce ortamında birden fazla B2C kiracısı yapılandırma
description: Bu makale, özel bir Dynamics 365 Commerce ortamında kullanıcı kimlik doğrulaması için kanal başına birden çok Microsoft Azure Active Directory (Azure AD) İşletme-Müşteri Arası (B2C) kiracısının ne zaman ve nasıl ayarlanacağını açıklamaktadır.
author: BrianShook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-12
ms.dyn365.ops.version: ''
ms.search.industry: retail
ms.search.form: ''
ms.openlocfilehash: 4966a3df20544fd6cdff493b8bd1aa566aecdfe9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276905"
---
# <a name="configure-multiple-b2c-tenants-in-a-commerce-environment"></a>Commerce ortamında birden fazla B2C kiracısı yapılandırma

[!include [banner](includes/banner.md)]

Bu makale, özel bir Dynamics 365 Commerce ortamında kullanıcı kimlik doğrulaması için kanal başına birden çok Microsoft Azure Active Directory (Azure AD) işletme-müşteri arası (B2C) kiracısının ne zaman ve nasıl ayarlanacağını açıklamaktadır.

Dynamics 365 Commerce, kullanıcı kimlik bilgileri ve kimlik doğrulama akışlarını desteklemek için Azure AD B2C bulut kimliği hizmetini kullanır. Kullanıcılar parolalarını kaydetmek, oturum açmak ve sıfırlamak için kimlik doğrulama akışlarını kullanabilirler. Azure AD B2C kullanıcının hassas kimlik doğrulama bilgilerini (örneğin, kullanıcı adı ve parola) depolar. Kullanıcı kaydı her B2C kiracısı için benzersizdir ve kullanıcı adı (e-posta adresi) kimlik bilgileri ya da sosyal kimlik sağlayıcısı kimlik bilgilerini kullanır.

Çoğu durumda, bir Commerce ortamında tek bir Azure AD B2C kiracısı kullanılır. Böylece Commerce müşterileri aynı Commerce ortamında birden çok site oluşturabilir ve yayımlayabilir ve aynı müşteri kimlik bilgileri bu sitelerde kullanılabilir. Ancak, ortamdaki sitelerin farklı markalar olarak değerlendirilmesi ve kullanıcılara ayrı işletmeler halinde görünmesi gerekiyorsa, site/marka ayrımı için kullanılan kanal için bir B2C kiracısı yapılandırılabilir.

## <a name="considerations-when-multiple-b2c-tenants-are-set-up-per-channel"></a>Kanal başına birden çok B2C kiracısı ayarlarken dikkate alınması gereken noktalar

Genellikle, her bir kanal veya site ayrı bir işletme ele alındığında, Commerce'taki Kullanıcı kimlik doğrulaması akışlarına göre en iyi seçenek, ayrı tüzel kişilikler kullanmaktır. Ancak, her bir kanalı/siteyi aynı ortam ve tüzel kişilik içinde tutmak ama her bir site için ayrı kullanıcı kimlik doğrulaması olmasını istiyorsanız, devam etmeden önce aşağıdaki noktaları göz önünde bulundurmanız önemlidir:

- Kullanıcıların her bir kanal/site için kendi farklı kimlik bilgileri olacaktır.

    Her hesap ayrı bir B2C kiracısında benzersiz bir giriş olacağından, aynı kişinin kanal/site başına iki ayrı hesabı olabilir.

- Microsoft Dynamics ortamında, genel kayıt aramaları için ayrı müşteri kayıtları döndürülür.

    Bir kullanıcı kanallar/siteler arasında aynı e-posta adresini kullanırsa, genel müşteri aramaları her bir kanal/site için sonuçları döndürür. (Bir kanal göstergesi gösterilecektir.)

- Adres defteri, kullanıcıları her kanal için izlemek amacıyla kullanıcıları gruplamaya yardımcı olmak üzere kullanılabilir.
- Kanal başına müşteri kaydı sayısı artabilir ve bu artış genel müşteri aramalarının performansını etkileyebilir.
- B2C kiracıları, müşterilerin yanlış bir kiracıya kaydolması durumunu engellenmeye yardımcı olmak amacıyla bir kanalla dikkatli şekilde eşlenmelidir. Aksi durumda, karışıklık veya izleme sorunları oluşabilir.

Aşağıdaki örnekte bir Commerce ortamındaki birden fazla B2C kiracısı gösterilmektedir.

![Commerce ortamındaki birden fazla B2C kiracısı.](media/MultiB2C_In_Environment.png)

İşletmeniz için aynı Commerce ortamında kanal başına farklı B2C kiracıları gerektiğine karar verirseniz, bu özelliği istemek için aşağıdaki bölümlerdeki yordamları tamamlayın.

## <a name="configure-b2c-tenants-in-your-environment"></a>Ortamınızdaki B2C kiracıları yapılandırma

Ortamınızda B2C kiracıları yapılandırmak için, bu bölümdeki ilgili yordamları tamamlayın.

### <a name="add-an-azure-ad-b2c-tenant"></a>Azure AD B2C kiracısı ekleme

Ortamınıza bir Azure AD B2C kiracısı eklemek için aşağıdaki adımları izleyin.

1. Bir sistem yöneticisi olarak ortamınız için Commerce site oluşturucuda oturum açın. Azure AD B2C kiracıları yapılandırmak için Commerce ortamınızda sistem yöneticisi olmanız gerekir.
1. Sol gezinti bölmesinde, genişletmek için **Kiracı Ayarları**'nı seçin.
1. **B2C Ayarları**'nı ve daha sonra **Yönet**'i seçin.
1. **B2C Uygulaması Ekle**'yi seçin ve aşağıdaki bilgileri girin:

    - **Uygulama Adı**: Commerce'ta yönetme bağlamında uygulama için kullanılacak adı girin. Azure portalında Azure AD B2C uygulamasını kurarken seçtiğiniz uygulama adını kullanmanızı öneririz. Böylece, Commerce'ta B2C kiracıları yönetirken karışıklığı azaltabilirsiniz.
    - **Kiracı Adı**: B2C kiracısı adını Azure portalında göründüğü şekliyle girin.
    - **Parolayı Unut İlke Kimliği**: İlke kimliğini (Azure portalındaki ilkenin adı) girin.
    - **Kaydol Oturum Aç İlke Kimliği**: İlke kimliğini (Azure portalındaki ilkenin adı) girin.
    - **İstemci GUID'i**: Azure AD B2C kiracısı kimliğini Azure portalında göründüğü şekliyle girin (B2C kiracısı için uygulama kimliği değil).
    - **Profili Düzenle İlke Kimliği**: İlke kimliğini (Azure portalındaki ilkenin adı) girin.

1. Bu bilgileri girmeyi bitirdiğinizde, değişikliklerinizi kaydetmek için **Tamam**'ı seçin. Yeni Azure AD B2C kiracınız şimdi **B2C uygulamalarını yönet** altındaki listede görünmelidir.

> [!NOTE]
> Dynamics 365 Commerce takım bunları ayarlamanızı istemedikçe **Kapsam**, **Etkileşimli olmayan ilke kodu**, **Etkileşimli olmayan istemci kodu**, **Oturum açma özel etki alanı** ve **Kayıt ilkesi Kodu** alanlarını boş bırakmanız gerekir.


### <a name="manage-or-delete-an-azure-ad-b2c-tenant"></a>Azure AD B2C kiracısını yönetme veya silme

1. Bir sistem yöneticisi olarak ortamınız için Commerce site oluşturucuda oturum açın. Azure AD B2C kiracıları yapılandırmak için Commerce ortamınızda sistem yöneticisi olmanız gerekir.
1. Sol gezinti bölmesinde, genişletmek için **Kiracı Ayarları**'nı seçin.
1. **B2C Ayarları**'nı ve daha sonra **Yönet**'i seçin.
1. B2C kiracısını düzenlemek için yanındaki kalem simgesini seçin. B2C kiracısını silmek için, yanındaki çöp tenekesi simgesini seçin.
1. **Kaydet**'i ve sonra değişikliklerinizi etkinleştirmek için **Yayımla**'yı seçin.

> [!WARNING]
> Bir B2C kiracısı canlı/yayımlanmış bir site için yapılandırıldığında, kullanıcılar kiracıda bulunan hesapları kullanarak oturum açabilirler. **Kiracı Ayarları \> B2C Kiracısı** menüsünde yapılandırılmış bir kiracıyı silerseniz, bu B2C kiracısının ilişkisini, kiracının kanallarıyla ilişkilendirilmiş olan sitelerden kaldırırsınız. Bu durumda, kullanıcılarınız hesaplarında artık oturum açamayabilirler. Bu nedenle, yapılandırılmış bir kiracıyı silerken çok dikkatli olun.
>
> Yapılandırılmış bir kiracı silindiğinde, B2C kiracısı ve kayıtları korunmaya devam eder, ancak bu kiracının Commerce sistem yapılandırması değiştirilir veya kaldırılır. Siteye kaydolmaya veya sitede oturum açmaya çalışan kullanıcılar, varsayılan veya sitenin kanalı için yapılandırılan yeni ilişkili B2C kiracısında yeni bir firma kaydı oluşturacaktır.

## <a name="configure-your-channel-with-a-b2c-tenant"></a>Kanalınızı bir B2C kiracısı ile yapılandırma

1. Bir sistem yöneticisi olarak ortamınız için Commerce site oluşturucuda oturum açın. Azure AD B2C kiracıları yapılandırmak için Commerce ortamınızda sistem yöneticisi olmanız gerekir.
1. Sol gezinti bölmesinde, genişletmek için **Site Ayarları** seçin.
1. **Kanallar**'ı seçin ve sonra yapılandırılacak kanalı seçin.
1. Sağdaki özellikler bölmesinde, **B2C Uygulaması Seç** alanında, bu kanal için kullanılacak yapılandırılmış Azure AD B2C kiracısını seçin.
1. Yeni veya güncelleştirilmiş yapılandırmayı uygulamak için komut çubuğunda **Kaydet ve Yayımla**'yı seçin.

> [!WARNING]
> Kanala atanmış B2C uygulamasını değiştirirseniz, ortamda zaten kaydolmuş olan tüm kullanıcılar için kurulmuş olan geçerli başvuruları kaldırırsınız. Bu durumda, geçerli olarak atanmış olan B2C uygulamasıyla ilişkilendirilmiş kimlik bilgileri kullanıcılar tarafından kullanılamaz. Bu nedenle, yalnızca kanalı ilk kez ayarlıyorsanız kanal Azure AD B2C yapılandırmasını değiştirin; hiçbir kullanıcı oturum açamayacaktır. Aksi durumda, kullanıcıların yeni Azure AD B2C kiracısında bir kayıt oluşturmak için yeniden kaydolması gerekebilir.
## <a name="additional-resources"></a>Ek kaynaklar

[Etki alanı adınızı yapılandırma](configure-your-domain-name.md)

[Yeni bir e-ticaret kiracısını dağıtma](deploy-ecommerce-site.md)

[E-ticaret sitesi oluşturma](create-ecommerce-site.md)

[Dynamics 365 Commerce sitesini çevrimiçi bir kanalla ilişkilendirme](associate-site-online-store.md)

[robots.txt dosyalarını yönetme](manage-robots-txt-files.md)

[URL yeniden yönlendirmelerini toplu olarak yükleme](upload-bulk-redirects.md)

[Commerce'ta B2C kiracısı ayarlama](set-up-B2C-tenant.md)

[Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama](custom-pages-user-logins.md)

[İçerik teslim ağı (CDN) için destek ekleme](add-cdn-support.md)

[Konum tabanlı mağaza algılamayı etkinleştirme](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
