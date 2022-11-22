---
title: B2C uygulaması oluşturma
description: Bu makalede, Microsoft Azure portalda işletme-müşteri arası (B2C) uygulamasının nasıl oluşturulacağı açıklanır.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: d8956d51bac7bf2a162a370ae5ef1c7e7cdc1e2f
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785333"
---
# <a name="create-a-b2c-application"></a>B2C uygulaması oluşturma

[!include [banner](includes/banner.md)]

Bu makalede, Microsoft Azure portalda işletme-müşteri arası (B2C) uygulamasının nasıl oluşturulacağı açıklanır.

B2C kiracınızı oluşturulduktan sonra, Commerce ile etkileşimde bulunmak için yeni Azure Active Directory (Azure AD) B2C kiracınız içinde bir B2C uygulaması oluşturacaksınız.

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

## <a name="next-steps"></a>Sonraki adımlar

Commerce'te bir B2C kiracısı ayarlama işlemine devam etmek için [Kullanıcı akışı ilkeleri oluşturma](create-user-flow-policies.md) bölümüne gidin.

## <a name="additional-resources"></a>Ek kaynaklar

[Commerce'ta B2C kiracısı ayarlama](set-up-b2c-tenant.md)

[Azure portalında mevcut bir Azure AD B2C kiracısı oluşturma veya bu kiracıya bağlantı sağlama](create-link-aad-b2c-tenant.md)

[Kullanıcı akış ilkeleri oluşturma](create-user-flow-policies.md)

[Sosyal kimlik sağlayıcıları ekleme (İsteğe bağlı)](add-social-identity-providers.md)

[Commerce Headquarters'ı yeni Azure AD B2C bilgileri ile güncelleştirme](update-hq-aad-b2c-info.md)

[Commerce site oluşturucuda B2C kiracınızı yapılandırma](config-b2c-tenant-site-builder.md)

[Ek B2C bilgileri](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
