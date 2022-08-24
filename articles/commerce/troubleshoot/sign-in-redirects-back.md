---
title: Oturum açma bağlantısı yeniden e-ticaret sitesine yönlendiriyor
description: Bu makale, oturum açma bağlantısının oturum açma sayfasına gitmek yerine e-ticaret sitesine geri yönlendirmesine yardımcı olabilecek sorun giderme kılavuzu sağlar.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 0bc9c0afbd6b349d8565f9eea56e207eae179f65
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291468"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a>Oturum açma bağlantısı yeniden e-ticaret sitesine yönlendiriyor

[!include [banner](../../includes/banner.md)]

Bu makale, oturum açma bağlantısının oturum açma sayfasına gitmek yerine e-ticaret sitesine geri yönlendirmesine yardımcı olabilecek sorun giderme kılavuzu sağlar.

## <a name="description"></a>Tanım

Commerce Site Builder'da yeni bir Microsoft Azure Active Directory B2C (Azure AD B2C) kiracısı yapılandırdıktan sonra, **Oturum aç** bağlantısını seçen kullanıcılar oturum açma sayfasına gitmeden ana e-ticaret açılış sayfasına geri yönlendiriliyor.

## <a name="resolution"></a>Çözünürlük

### <a name="confirm-that-the-reply-url-is-correctly-configured-in-the-azure-ad-b2c-application"></a>Azure AD B2C uygulamasında yanıt URL'sinin doğru yapılandırıldığını onaylayın

Azure AD B2C uygulamasında yanıt URL'sinin doğru yapılandırıldığını onaylamak için aşağıdaki adımları izleyin.

1. [Azure portal](https://portal.azure.com/)'a gidin.
1. Sitenizin erişimi için oluşturduğunuz Azure AD B2C uygulamasını seçin.
1. Azure AD B2C kurulumu sırasında oluşturduğunuz uygulamayı seçin.
1. **Yanıt URL'si** altında, aşağıdaki resimdeki örnekte gösterildiği gibi, listenin hem site etki alanı URL'si hem de e-ticaret tarafından oluşturulan URL girdilerini içerdiğinden emin olun.

    ![Azure AD B2C yanıt URL'si girişleri.](media/aad-b2c-reply-url.jpg)

> [!NOTE]
> Hem site etki alanı URL'si hem de e-ticaret tarafından oluşturulan URL, başta veya sonda eğik çizgiler içermeyen geçerli bir URL biçiminde olmalıdır.

## <a name="additional-resources"></a>Ek kaynaklar

[Azure Active Directory B2C'de web uygulamasını kaydetme](/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[Commerce'ta B2C kiracısı ayarlama](../set-up-b2c-tenant.md)
