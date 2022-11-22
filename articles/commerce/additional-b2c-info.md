---
title: Ek B2C bilgileri
description: Bu makalede, Microsoft Dynamics 365 Commerce'te işletmeden müşteriye (B2C) kiracınızı nasıl ayarlayacağınıza ilişkin ek bilgiler sağlanmaktadır.
author: BrianShook
ms.date: 11/14/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: b60ef15544cd30c44968ee7a588a8a9fb08e8223
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785331"
---
# <a name="additional-b2c-information"></a>Ek B2C bilgileri

[!include [banner](includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce'te işletmeden müşteriye (B2C) kiracınızı nasıl ayarlayacağınıza ilişkin ek bilgiler sağlanmaktadır.

### <a name="customer-migration"></a>Müşteri geçişi

Müşteri kayıtlarını önceki bir kimlik sağlayıcı platformundan geçirmeyi düşünüyorsanız, lütfen müşteri geçiş gereksinimlerinizi gözden geçirmek için Dynamics 365 Commerce ekibiyle birlikte çalışın.

Müşteri geçisindeki ek Azure AD B2C belgeleri için bkz. [Kullanıcıları Azure Active Directory B2C'ye geçirme](/azure/active-directory-b2c/active-directory-b2c-user-migration).

### <a name="custom-policies"></a>Özel ilkeler

Azure AD B2C etkileşimlerini ve ilke akışlarını standart B2C ilkeleriyle sunulandan daha fazla özelleştirme hakkında ek bilgi için bkz. [Azure Active Directory'deki özel ilkeler](/azure/active-directory-b2c/active-directory-b2c-overview-custom). 

### <a name="secondary-admin"></a>İkincil yönetici

B2C kiracınızın **Kullanıcılar** bölümünde isteğe bağlı, ikincil bir yönetici hesabı eklenebilir. Bu doğrudan bir hesap veya genel bir hesap olabilir. Bir hesabı ekip kaynakları arasında paylaşmanız gerekirse, ortak hesap da oluşturulabilir. Azure AD B2C'de depolanan verilerin hassasiyeti nedeniyle, ortak hesabın şirketinizin güvenlik uygulamalarıyla yakından izlenmesi gerekir.

### <a name="set-up-a-custom-sign-in-domain"></a>Özel oturum açma etki alanı ayarlama

Azure AD B2C, Azure AD B2C kiracısı için özel oturum açma etki alanı kurmanıza olanak sağlar. Yönergeler için bkz. [Azure Active Directory B2C için özel etki alanlarını etkinleştirme](/azure/active-directory-b2c/custom-domain). 

Özel oturum açma etki alanı kullanırsanız, etki alanının Commerce site oluşturucuda girilmesi gerekir.

Site oluşturucuda özel bir oturum açma etki alanı girmek için, aşağıdaki adımları izleyin.

1. Site oluşturucunun sağ üst köşesinde site değiştiriciyi seçin ve sonra **Siteleri yönet**'i seçin.
1. Sol gezinti bölmesinde, **Kiracı ayarları \> Site kimlik doğrulama kurulumu**'nu seçin.
1. **Site kimlik doğrulama profilleri** bölümünde **Yönet**'i seçin.
1. Sağdaki açılır menüde, özel etki alanı girmek istediğiniz site kimlik doğrulama profilinin yanındaki **Düzenle** düğmesini (kurşun kalem simgesi) seçin.
1. **Site kimlik doğrulama profilini düzenle** iletişim kutusunda, **Oturum açma özel etki alanı** altında, özel oturum açma etki alanınızı (örneğin, 'login.fabrikam.com') girin.

> [!WARNING]
> Azure AD B2C kiracısı için özel bir etki alanına güncelleştirdiğinizde, bu değişiklik kiracının ürettiği belirtecin veren ayrıntılarını etkiler. Böylece, veren ayrıntıları, Azure AD B2C tarafından sağlanan varsayılan etki alanı yerine özel etki alanını içerecektir. Commerce Headquarters'daki farklı bir **Veren** yapılandırması (**Retail ve Commerce \> Headquarters kurulumu \> Parametreler \> Commerce paylaşılan parametreleri \> Kimlik Sağlayıcıları**), sistemin site kullanıcılarıyla etkileşimini değiştirir ve bir kullanıcı yeni verenle kimlik doğrulaması yapıyorsa yeni bir müşteri kaydı oluşturulmasına neden olabilir. Tüm özel etki alanı değişiklikleri, canlı bir Azure AD B2C ortamında özel etki alanına geçmeden önce kapsamlı olarak test edilmelidir.

## <a name="additional-resources"></a>Ek kaynaklar

[Commerce'ta B2C kiracısı ayarlama](set-up-b2c-tenant.md)

[Azure portalında mevcut bir Azure AD B2C kiracısı oluşturma veya bu kiracıya bağlantı sağlama](create-link-aad-b2c-tenant.md)

[B2C uygulaması oluşturma](create-b2c-app.md)

[Kullanıcı akış ilkeleri oluşturma](create-user-flow-policies.md)

[Sosyal kimlik sağlayıcıları ekleme (İsteğe bağlı)](add-social-identity-providers.md)

[Commerce Headquarters'ı yeni Azure AD B2C bilgileri ile güncelleştirme](update-hq-aad-b2c-info.md)

[Commerce site oluşturucuda B2C kiracınızı yapılandırma](config-b2c-tenant-site-builder.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
