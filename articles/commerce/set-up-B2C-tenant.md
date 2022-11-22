---
title: Commerce'te B2C kiracısı ayarlama
description: Bu makale, Microsoft Dynamics 365 Commerce'ta kullanıcı sitesi kimlik doğrulaması için Azure Active Directory (Azure AD) işletme-müşteri arası (B2C) kiracılarınızın nasıl kurulacağını açıklamaktadır.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 3421dd3d67198a99ac236a56cbb4f300cb591a03
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785166"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a>Commerce'te B2C kiracısı ayarlama

[!include [banner](includes/banner.md)]

Bu makale, Dynamics 365 Commerce'ta kullanıcı sitesi kimlik doğrulaması için Azure Active Directory (Azure AD) işletme-müşteri arası (B2C) kiracılarınızın nasıl kurulacağını açıklamaktadır.

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

## <a name="next-steps"></a>Sonraki adımlar

Commerce'te bir B2C kiracısı ayarlama işlemine devam etmek için [Azure portalında mevcut Azure AD B2C kiracısı oluşturma veya bağlantı kurma](create-link-aad-b2c-tenant.md) bölümüne geçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Azure portalında mevcut bir Azure AD B2C kiracısı oluşturma veya bu kiracıya bağlantı sağlama](create-link-aad-b2c-tenant.md)

[B2C uygulaması oluşturma](create-b2c-app.md)

[Kullanıcı akış ilkeleri oluşturma](create-user-flow-policies.md)

[Sosyal kimlik sağlayıcıları ekleme (İsteğe bağlı)](add-social-identity-providers.md)

[Commerce Headquarters'ı yeni Azure AD B2C bilgileri ile güncelleştirme](update-hq-aad-b2c-info.md)

[Commerce site oluşturucuda B2C kiracınızı yapılandırma](config-b2c-tenant-site-builder.md)

[Ek B2C bilgileri](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
