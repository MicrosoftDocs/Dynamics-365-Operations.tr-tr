---
title: POS oturum açma için Azure Active Directory kimlik doğrulamasını yapılandırma
description: Bu konu, Microsoft Dynamics 365 Commerce satış noktasında kimlik doğrulama yöntemi olarak Azure Active Directory'yi yapılandırma yöntemini açıklamaktadır.
author: boycezhu
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 63121a9b5f1b062b7ca927f6b9eb1689ce8aa698
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270695"
---
# <a name="configure-azure-active-directory-authentication-for-pos-sign-in"></a>POS oturum açma için Azure Active Directory kimlik doğrulamasını yapılandırma

[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce (POS) satış noktasında kimlik doğrulama yöntemi olarak Azure Active Directory'yi (Azure AD) yapılandırma yöntemini açıklamaktadır.

Microsoft Azure, Microsoft 365, ve Microsoft Teams gibi diğer Microsoft bulut hizmetleriyle birlikte Dynamics 365 Commerce kullanan perakendeciler genellikle uygulamalar arasında güvenli ve sorunsuz oturum açma deneyimi sağlamak amacıyla kullanıcı kimlik bilgilerinin merkezi yönetimi için Azure AD kullanmak ister. Commerce POS için Azure AD kimlik doğrulamasını kullanmak için önce Commerce genel merkezinde kimlik doğrulama yöntemi olarak Azure AD'yi yapılandırmalısınız.

## <a name="configure-pos-authentication-method"></a>POS kimlik doğrulama yöntemini yapılandırma

Commerce genel merkezinde POS kimlik doğrulama yöntemini yapılandırmak için aşağıdaki adımları izleyin.
    
1. **Retail ve Commerce \> Kanal kurulumu \> POS ayarı \> POS profilleri \> İşlevsellik profilleri**'ne gidin ve değişiklikleri yapmak üzere bir işlev profili seçin.
1. **İşlevler** hızlı sekmesinin **POS personeli oturum açma** bölümündeki **Oturum Açma Kimlik Doğrulama Yöntemi** açılır listesinden dilediğiniz kimlik doğrulama yöntemini seçin.

    **Oturum açma kimlik doğrulama yöntemi**'nde üç seçenek bulunur:
    
    - **Personel Kimliği ve Parola** - Bu varsayılan seçenek POS kullanıcılarının, POS'ta oturum açmak ve erişim yöneticisini geçersiz kılma işlevlerine erişmek için bir personel kodu ve parola girmesini gerektirir.
    - **Çoklu oturum açmasız Azure AD** - Bu seçenek POS kullanıcılarının, POS'ta oturum açmak ve erişim yöneticisini geçersiz kılma işlevlerine erişmek için Azure AD kimlik bilgilerini kullanarak oturum açmasını gerektirir. POS istemcisi yenilendiğinde veya yeniden açıldığında, POS kullanıcısının tekrar oturum açmak için Azure AD kimlik bilgilerini sağlaması gerekir.
    - **Çoklu oturum açmalı Azure AD** - Bu seçenek işaretlendiğinde, POS kullanıcıları aynı web tarayıcısındaki diğer web uygulamaları tarafından kullanılan etkin Azure AD kimlik bilgilerini kullanarak Bulut POS'ta (CPOS) oturum açabilir veya Windows'ta açılı olan Azure AD kimlik bilgilerini kullanarak Modern POS'ta (MPOS) oturum açabilir. Her iki yöntem de POS oturum açma ekranında Azure AD kimlik bilgilerini girmeye gerek kalmadan oturum açmaya izin verir. Ancak, POS yöneticisi geçersiz kılma işlevine erişmek için yine de Azure AD kimlik bilgilerinin kullanılarak oturum açılması gerekir.

1. **Retail ve Commerce > Retail ve Commerce IT > Dağıtım planı**'na gidin ve en son işlevsellik profili ayarlarını POS istemcileriyle eşitlemek için **1070 (Kanal yapılandırması)** işini çalıştırın.

> [!NOTE]
> - **Çoklu oturum açmasız Azure AD** kimlik doğrulama yöntemi seçeneği, Commerce 10.0.18 ve önceki sürümlerde **Azure Active Directory** seçeneğinin yerini alır.
> - Azure AD kimlik doğrulaması, etkin bir internet bağlantısı gerektirir ve POS çevrimdışıyken çalışmaz.

## <a name="associate-azure-ad-accounts-with-pos-users"></a>Azure AD hesaplarını POS kullanıcıları ile ilişkilendirme

Azure AD'yi POS kimlik doğrulama yöntemi olarak kullanmak için Azure AD hesaplarını Commerce genel merkezindeki POS kullanıcılarıyla ilişkilendirmeniz gerekir. 

Azure AD hesaplarını Commerce genel merkezindeki POS kullanıcılarıyla ilişkilendirmek için aşağıdaki adımları izleyin.
    
1. **Retail ve Commerce > Personel > Çalışanlar**'a gidin ve bir çalışan kaydı açın.
1. Eylem Bölmesinde, **Commerce** sekmesini seçin ve ardından **Harici kimlik** altında **Mevcut kimliği ilişkilendir**'i seçin. 
1. **Mevcut harici kimliği kullan** iletişim kutusunda, **E-posta kullanarak ara**'yı seçin, bir Azure AD e-posta adresi girin ve sonra **Ara**'yı seçin.
1. Döndürülen Azure AD hesabını seçin, ardından **Tamam**'ı seçin.

Yukarıdaki yapılandırma ayarlarından sonra çalışanın ayrıntılar sayfasındaki **Commerce** sekmesinde bulunan **Diğer ad**, **UPN** ve **Harici alt kimlik tanımlayıcı** alanları doldurulacaktır.

En güncel POS kullanıcısını ve  Azure AD hesap verilerini kanala eşitlemek için **Retail ve Commerce > Retail ve Commerce IT > Dağıtım planı**'ndaki **1060 (Personel)** işini yürütmeniz gerekir.

> [!NOTE]
> Bir en iyi uygulama olarak, parola, POS izni, ilişkili Azure AD hesabı veya çalışan adres defteri gibi çalışan bilgileri Commerce genel merkezinde güncelleştirildikten sonra, en güncel çalışan bilgilerini kanalla eşitlemek için **1060 (Personel)** işini yürütmenizi öneririz. Ardından POS istemcisi kullanıcı kimlik doğrulaması ve yetkilendirme denetimleri için doğru verileri alabilir.

## <a name="pos-lock-register-and-sign-out-with-azure-ad-authentication"></a>Azure AD kimlik doğrulamasıyla POS kayıt kilitleme ve oturum kapatma

POS, Azure AD kimlik doğrulama yöntemini kullanacak şekilde yapılandırıldığında şu gerçekleşir:

- **Kayıt kilitle** işlevi, POS uygulamasında kullanılamaz. 
- **Otomatik olarak kilitle** işlevi, **Otomatik olarak oturum kapat** işleviyle aynı şekilde davranır.
- POS kullanıcısı, **Oturumu kapat**'ı seçerse çoklu oturum açma etkin olsun veya olmasın, kullanıcıdan POS bir daha başlatıldığında Azure AD kimlik bilgileriyle oturum açması istenir.

## <a name="manager-override-functionality-with-azure-ad-authentication"></a>Azure AD kimlik doğrulamasıyla yönetici geçersiz kılma işlevi

POS, Azure AD kimlik doğrulaması kullanacak şekilde yapılandırıldığına, yönetici geçersiz kılma işlevi yönetici kullanıcının Azure AD kimlik bilgilerini soran bir iletişim kutusu açar. Yönetici oturum açma onaylandıktan sonra, yöneticinin Azure AD kimlik bilgileri bırakılır ve sonraki POS işlemleri için önceki kullanıcının Azure AD kimlik bilgileri kullanılır.

> [!NOTE]
> - Commerce 10.0.18 ve önceki sürümlerde, yöneticiyi geçersiz kılma işlevi Azure AD'yi desteklemez. POS, Azure AD kimlik doğrulama yöntemini kullanacak şekilde yapılandırılmış olsa bile, bir personel kodu ve parola gereklidir.
> - CPOS'u Safari web tarayıcısı üzerinde veya bir Apple iOS cihazı üzerinde kullanırken, yönetici geçersiz kılma işlevinin Azure AD kimlik doğrulamasıyla çalışması için, öncelikle Safari ayarlarındaki **Açılır pencereleri engelle** seçeneğini kapatmanız gerekir. 

## <a name="security-best-practices-for-azure-ad-based-pos-authentication-on-shared-devices"></a>Paylaşılan cihazlarda Azure AD tabanlı POS kimlik doğrulamasıyla ilgili en iyi güvenlik uygulamaları

Birçok perakendeci, perakende mağaza ortamlarını paylaşılan fiziksel bir aygıttan POS uygulamasına erişmesi gerekecek şekilde kurar. Bu bağlamda çoklu oturum açma, rahat ve sorunsuz bir kimlik doğrulama deneyimi sağlıyor olsa da aynı zamanda geçerli POS kullanıcısının, POS'ta hareketleri veya operasyonları gerçekleştirmek için başka bir kullanıcının kimlik bilgilerinin kullanıldığını fark etmediği bir güvenlik boşluğu oluşturabilir. POS'u Azure AD kimlik doğrulama yöntemini kullanacak şekilde yapılandırmadan önce, hangi seçeneğin uygun olduğuna karar vermek üzere güvenlik ilkenizi ve paylaşılan aygıtın oturum açma ayarlarını gözden geçirmeniz önemle önerilir.

- Perakende ortamınız fiziksel aygıt ile oturum açma için paylaşılan bir hesap (örneğin bir yerel hesap) kullanıyorsa **Çoklu oturum açmasız Azure AD** seçeneğini kullanmanız önerilir. Bu, her bir POS kullanıcısının POS'ta oturum açmak için açıkça Azure AD kimlik bilgileri kullanmasını gerektirir.
- Perakende ortamınız POS'ta ve POS'un barındırıldığı fiziksel cihazda oturum açmak için çalışanların kendi Azure AD hesaplarını kullanmasını gerektiriyorsa **Çoklu oturum açmalı Azure AD** seçeneğini kullanmanız önerilir.

## <a name="additional-resources"></a>Ek kaynaklar

[ Çalışanı yapılandırma](tasks/worker.md)

[Perakende işlevselliği profili oluşturma](retail-functionality-profile.md)


[MPOS ve Bulut POS için genişletilmiş oturum açma işlevini ayarlama](extended-logon.md)

[Paylaşılan ortamlarda Cloud POS için en iyi güvenlik uygulamaları](dev-itpro/secure-retail-cloud-pos.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
