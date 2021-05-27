---
title: Test veya geliştirme sırasında mağazaya erişimi sınırlama
description: Bu konu mağaza içi test veya geliştirme gerçekleştirilirken Microsoft Dynamics 365 Commerce mağazasına erişimin nasıl kısıtlanacağını açıklamaktadır.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: cdc9b6af55bcba98f5ea7607bb1847f61a707778
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018350"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a>Test veya geliştirme sırasında mağazaya erişimi sınırlama

[!include [banner](../../includes/banner.md)]

Bu konu mağaza içi test veya geliştirme gerçekleştirilirken Microsoft Dynamics 365 Commerce mağazasına erişimin nasıl kısıtlanacağını açıklamaktadır.

## <a name="description"></a>Tanım

Mağaza içi test veya etkin geliştirme sırasında, harici kullanıcıların yayınlanan mağaza sayfalarına erişmesini engellemek için sitenize erişimi kısıtlamak isteyebilirsiniz.

## <a name="resolution"></a>Çözünürlük

### <a name="set-up-azure-ad-b2c-by-using-standard-user-flows"></a>Standart Kullanıcı akışlarını kullanarak Azure AD B2C'yi ayarlama

E-Ticaret siteniz için Azure Active Directory B2C'yi (Azure AD B2C) yapılandırma hakkında bilgi için, bkz. [Commerce'te B2C kiracısı ayarlama](../set-up-b2c-tenant.md).

### <a name="restrict-user-access-to-storefront-pages-and-block-the-creation-of-new-users"></a>Mağaza sayfalara Kullanıcı erişimini kısıtlama ve yeni kullanıcıların oluşturulmasını engelleme

Commerce Site Builder'da mağaza sayfalarına Kullanıcı erişimini kısıtlamak için aşağıdaki adımları izleyin.

1. Sitenize gidin.
1. **Sayfaları** seçin ve sonra da kullanıcı erişimini kısıtlayacağınız sayfayı seçin.
1. Modül veya parça yuvasını seçin ve ardından **Düzenle**'yi seçin.
1. Özellikler bölmesinde, **Oturum açılması gerekiyor mu?** seçeneğini belirleyin ve sonra **düzenlemeyi bitir**'i seçin.
1. **Yayımla**'yı seçin.

Azure AD'de yeni kullanıcıların oluşturulmasını engellemek için aşağıdaki adımları izleyin.

1. [Azure portal](https://portal.azure.com/)'a gidin.
1. Sitenizin erişimi için oluşturduğunuz Azure AD B2C uygulamasını seçin.
1. Soldaki gezinti bölmesinde **Kullanıcı akışlarını** seçin.
1. **Kullanıcı akışları** sayfasında, **Yeni Kullanıcı Akışı**'nı seçin.
1. **Bir Kullanıcı akış türü seçin** sayfasında, **önizleme**'yi seçin.
1. Sayfanın ortasında, **oturum aç: v2** seçeneğini belirleyin. Daha sonra, test veya geliştirme sırasında akışı Azure AD B2C için sitenizin standart Kullanıcı akışı olarak yapılandırmak için, [Commerce'te bir B2C kiracısı ayarlama](../set-up-b2c-tenant.md) adımlarını izleyin.

## <a name="additional-resources"></a>Ek kaynaklar

[Commerce'ta B2C kiracısı ayarlama](../set-up-b2c-tenant.md)

[Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama](../custom-pages-user-logins.md)
