---
title: CPOS'u özel Azure AD uygulaması kullanacak şekilde yapılandırma
description: Bu makalede, Cloud POS'un (CPOS) özel bir Azure Active Directory (Azure AD) uygulaması kullanacak şekilde nasıl yapılandırılacağı açıklanmaktadır.
author: boycez
ms.date: 11/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 5e4ff797410e1e94869cc37684e7622ec0d97842
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746273"
---
# <a name="configure-cpos-to-use-a-custom-azure-ad-app"></a>CPOS'u özel Azure AD uygulaması kullanacak şekilde yapılandırma

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Commerce'teki Cloud POS (CPOS) varsayılan olarak, Azure Active Directory (Azure AD) içindeki kayıtlı birinci taraf Microsoft uygulamasına işaret eder. Bu nedenle CPOS'u, Azure AD'de herhangi bir değişiklik yapmak zorunda kalmadan kullanabilirsiniz. Ancak, CPOS örneğinizi kontrol ettiğiniz özel bir Azure AD uygulamasına işaret edecek şekilde ayarlamanız iyi olacaktır. Bu makalede, CPOS'un özel bir Azure AD uygulaması kullanacak şekilde nasıl yapılandırılacağı açıklanmaktadır.

## <a name="set-up-a-custom-retail-server-app-in-azure-ad"></a>Azure AD'de özel bir Retail Server uygulaması ayarlama

Azure AD'de özel bir Retail Server uygulaması oluşturmak ve yapılandırmak için aşağıdaki adımları izleyin.

1. Herhangi bir Azure AD kullanıcı hesabını kullanarak [Azure Active Directory yönetim merkezinde](https://aad.portal.azure.com) oturum açın. Kullanıcı hesabının yönetici izinleri olması gerekmez.
1. **Azure Active Directory** öğesini seçin.
1. **Uygulama kayıtları**'nı seçin ve sonra **Uygulama kaydet** iletişim kutusunu açmak için **Yeni kayıt**'ı seçin.
1. Aşağıdaki alanları ayarlayın:

    - **Ad**: Uygulama için özel bir ad girin. Örneğin, **Özel Retail Server** girin.
    - **Desteklenen hesap türleri** – Varsayılan seçenek olan **Yalnızca bu kuruluş dizinindeki hesaplar (Yalnızca Microsoft - Tek kiracılı)** seçeneğini seçin.
    - **Yeniden yönlendirme URI'si** – Bu alan isteğe bağlıdır. Boş bırakın.
    - **Servis Ağacı Kimliği** – Bu alan isteğe bağlıdır. Boş bırakın.
    
1. **Kayıt**'ı seç. Yeni kaydedilen uygulama için yapılandırma sayfası görüntülenir.
1. **Genel Bakış \> Temel Bilgiler** bölümünde, **Uygulama Kimliği URI'si ekle**'yi seçin ve ardından **Uygulama Kimliği URI'sinin** yanındaki **Ayarla**'yı seçin. Önerilen değeri not edin ve sonra bu değeri kabul etmek için **Kaydet**'i seçin. 
1. **Kapsam ekle**'yi seçin ve ardından aşağıdaki alanları ayarlayın:

    - **Kapsam adı**: Kapsam için özel bir ad girin. Örneğin, **Legacy.Access.Full** girin.
    - **Kim izin verebilir** – Kuruluşunuzun güvenlik ilkelerine göre, yöneticilerin ve kullanıcıların mı yoksa yalnızca yöneticilerin mi izin verebileceğini belirtin.
    - **Yönetici onayı görünen adı** – Bir görünen ad girin. Örneğin, **Retail Server'a Erişim** girin.
    - **Yönetici onayı açıklaması** – Bir açıklama girin. Örneğin, **Retail Server API'lerine erişim verir** girin.

1. Kapsam oluşturma işlemini tamamlamak için **Kapsam ekle**'yi seçin.

## <a name="set-up-a-custom-cpos-app-in-azure-ad"></a>Azure AD'de özel bir CPOS uygulaması ayarlama

> [!IMPORTANT]
> Commerce sürüm 10.0.21 öncesinde oluşturulmuş, varolan bir özel CPOS Azure AD uygulamasını yükseltiyorsanız, [Commerce sürüm 10.0.21 öncesinde oluşturulmuş varolan bir özel CPOS Azure AD uygulamasını yükseltme](#upgrade-an-existing-custom-cpos-azure-ad-app-created-before-commerce-version-10021) bölümünde verilen adımları izleyin.

Azure AD'de özel bir CPOS uygulaması oluşturmak ve yapılandırmak için aşağıdaki adımları izleyin.

1. Herhangi bir Azure AD kullanıcı hesabını kullanarak [Azure Active Directory yönetim merkezinde](https://aad.portal.azure.com) oturum açın. Kullanıcı hesabının yönetici izinleri olması gerekmez.
1. **Azure Active Directory** öğesini seçin.
1. **Uygulama kayıtları**'nı seçin ve sonra **Uygulama kaydet** iletişim kutusunu açmak için **Yeni kayıt**'ı seçin.
1. Aşağıdaki alanları ayarlayın:

    - **Ad**: Uygulama için bir ad girin. Örneğin, **Özel Cloud POS** girin.
    - **Desteklenen hesap türleri** – Varsayılan seçenek olan **Yalnızca bu kuruluş dizinindeki hesaplar (Yalnızca Microsoft - Tek kiracılı)** seçeneğini seçin.
    - **Yeniden yönlendirme URI'si** – Açılan listede **Tek sayfalı uygulama (SPA)**'yı seçin ve sonra CPOS URI'nizi girin.
    - **Servis Ağacı Kimliği** – Bu alan isteğe bağlıdır. Boş bırakın.

1. **Kayıt**'ı seç. Yeni kaydedilen uygulama için yapılandırma sayfası görüntülenir.
1. **Bildirim** bölümünde, **oauth2AllowIdTokenImplicitFlow** ve **oauth2AllowImplicitFlow** parametrelerini **true** olarak ayarlayıp **Kaydet**'i seçin.
1. **Belirteç yapılandırması** bölümünde, iki talep eklemek için aşağıdaki adımları izleyin:

    1. **İsteğe bağlı talep ekle** öğesini seçin. **Belirteç türü** alanını **Kimlik** olarak ayarlayın ve sonra da **sid** talebini seçin. **Ekle**'yi seçin.
    1. **İsteğe bağlı talep ekle** öğesini seçin. **Belirteç türü** alanını **Erişim** olarak ayarlayın ve sonra da **sid** talebini seçin. **Ekle**'yi seçin.

1. **API izinleri** bölümünde **İzin ekle**'yi seçin.
1. **Kuruluşumun kullandığı API'ler** sekmesinde, [Azure AD'de özel bir Retail Server uygulaması oluşturma](#set-up-a-custom-retail-server-app-in-azure-ad) bölümünde oluşturduğunuz Retail Server uygulamasını arayın. Ardından **İzin ekle**'yi seçin.
1. **Genel Bakış** bölümünde, **Uygulama (istemci) kimliği** alanındaki değeri not edin.

### <a name="upgrade-an-existing-custom-cpos-azure-ad-app-created-before-commerce-version-10021"></a>Commerce sürüm 10.0.21 öncesinde oluşturulmuş, varolan bir özel CPOS Azure AD uygulamasını yükseltme

Commerce sürüm 10.0.21 öncesinde oluşturulmuş, varolan bir özel CPOS Azure AD uygulamasını yükseltmek için aşağıdaki adımları izleyin. 

1. Özel CPOS Azure AD uygulamanızı Azure portalda açın.
1. **Kimlik Doğrulaması** sekmesini seçin.
1. Daha sonra kullanmak üzere, **Web** türündeki özgün yeniden yönlendirme URl'sini kopyalayıp kaydedin ve ardından silin.
1. **Platform ekle**, ardından **Tek sayfalı uygulama (SPA)** seçeneklerini belirleyin.
1. Yukarıda kopyaladığınız özgün web yeniden yönlendirme URl'sini SPA platformuna ekleyin.
1. **Belirteç yapılandırması** bölümünde, iki talep eklemek için aşağıdaki adımları izleyin:
    1. **İsteğe bağlı talep ekle** öğesini seçin. **Belirteç türü** alanını **Kimlik** olarak ayarlayın ve sonra da **sid** talebini seçin. **Ekle**'yi seçin.
    1. **İsteğe bağlı talep ekle** öğesini seçin. **Belirteç türü** alanını **Erişim** olarak ayarlayın ve sonra da **sid** talebini seçin. **Ekle**'yi seçin.

## <a name="update-the-cpos-configuration-file"></a>CPOS yapılandırma dosyasını güncelleştirme

CPOS config.json dosyasını açın ve içinde aşağıdaki güncelleştirmeleri yapın.

1. **AADClientId** anahtar değerini, [Azure AD'de özel bir CPOS uygulaması ayarlama](#set-up-a-custom-cpos-app-in-azure-ad) bölümünde oluşturduğunuz özel CPOS uygulamasının **Uygulama (istemci) kimliği** değeriyle değiştirin.
1. **AADRetailServerResourceId** anahtar değerini, [Azure AD'de özel bir Retail Server uygulaması ayarlama](#set-up-a-custom-retail-server-app-in-azure-ad) bölümünde oluşturduğunuz özel Retail Server uygulamasının **Uygulama kimliği URI'si** değeriyle değiştirin.

CPOS, güvenlik belirteci elde etmek için Azure AD'ye istek gönderdiğinde her iki parametreyi de kullanır.

## <a name="update-identity-providers-settings-in-commerce-headquarters"></a>Commerce Headquarters'da kimlik sağlayıcıları ayarlarını güncelleştirme

Ardından Commerce Headquarters'da kimlik sağlayıcıları ayarlarını güncelleştirmeniz gerekir.

1. Commerce headquarters'da, **Paylaşılan Commerce parametreleri** sayfasını açın.
1. **Kimlik sağlayıcıları** sekmesindeki **Kimlik sağlayıcıları** bölümünde, **Tür** **Azure Active Directory** olarak ayarlandığı ve **Veren** alanının Azure AD kiracınıza işaret ettiği satırı seçin. Bu ayar, Azure AD kiracınıza karşılık gelen kimlik sağlayıcısıyla ilgili verileri içeren alt kılavuzlar ile çalışacağınızı bildirir.
1. **Bağlı olan taraflar** bölümünde, satır eklemek için **Ekle**'yi seçin.
1. Aşağıdaki alanları ayarlayın:

    - **ClientId** – [Azure AD'de özel bir CPOS uygulaması ayarlama](#set-up-a-custom-cpos-app-in-azure-ad) bölümünde oluşturduğunuz özel CPOS uygulamasının **Uygulama (istemci) kimliği** değerini girin.
    - **Tür** – **Genel**'i seçin.
    - **UserType** – **Çalışan**'ı seçin.

1. Eklediğiniz satırı seçin. **Bağlı Olan Taraflar** bölümünün altındaki **Sunucu Kaynak Kimlikleri** bölümü, **Bağlı Olan Taraflar** kılavuzunda seçtiğiniz uygulama tarafından erişilebilen Retail Server uygulama kimliklerini gösterir.
1. **Sunucu Kaynak Kimlikleri** bölümünde satır eklemek için **Ekle**'yi seçin.
1. **Server Resource Id** alanında [Azure AD'de özel bir Retail Server uygulaması ayarlama](#set-up-a-custom-retail-server-app-in-azure-ad) bölümünde oluşturduğunuz özel Retail Server uygulamasının **Uygulama kimliği URI'si** değerini girin.

    > [!IMPORTANT]
    > Önceki adımlarda sözü edilen tüm alanlar büyük/küçük harfe duyarlıdır. Girdiğiniz değerlerin Azure AD yönetim merkezinde yapılandırılan değerlerle tam olarak eşleşmesi gerekir.

1. **Retail ve Commerce BT \> Dağıtım planı**'na gidin ve **1110** (**Genel yapılandırma**) işini yürütün.

Şimdi kendi Azure AD uygulamanızı kullanarak CPOS cihazlarını etkinleştirebilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar

[Satış noktası (POS) cihazını etkinleştirme](dev-itpro/retail-device-activation.md)

[Etkinleştirme hesaplarını yönetme ve cihazları doğrulama](set-up-activation-accounts-validate-devices-hq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
