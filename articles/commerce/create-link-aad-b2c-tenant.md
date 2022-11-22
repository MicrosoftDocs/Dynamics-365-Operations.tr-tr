---
title: Azure portalında mevcut bir Azure AD B2C kiracısı oluşturma veya bu kiracıya bağlantı sağlama
description: Bu makalede, Microsoft Azure portalda var olan bir Azure Active Directory (Azure AD) işletme-müşteri arası (B2C) kiracısının nasıl oluşturulacağı veya nasıl bağlantı kurulacağı açıklanmaktadır.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 0aa12387f00ffc3dd10688c6385c7952f089ab12
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785334"
---
# <a name="create-or-link-to-an-existing-azure-ad-b2c-tenant-in-the-azure-portal"></a>Azure portalında mevcut bir Azure AD B2C kiracısı oluşturma veya bu kiracıya bağlantı sağlama

[!include [banner](includes/banner.md)]

Bu makalede, Microsoft Azure portalda bir Azure Active Directory (Azure AD) işletme-müşteri arası (B2C) kiracısının nasıl oluşturulacağı veya nasıl bağlantı kurulacağı açıklanmaktadır. Daha fazla bilgi için bkz. [Öğretici: Azure Active Directory B2C kiracısı oluşturma](/azure/active-directory-b2c/tutorial-create-tenant).

Azure portalda Azure AD B2C kiracısı oluşturma veya mevcut bir kiracıya bağlantı kurma için bu adımları izleyin.

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

## <a name="next-steps"></a>Sonraki adımlar

Commerce'te bir B2C kiracısı ayarlama işlemine devam etmek için [B2C uygulama oluşturma](create-b2c-app.md) bölümüne devam edin.

## <a name="additional-resources"></a>Ek kaynaklar

[Commerce'ta B2C kiracısı ayarlama](set-up-b2c-tenant.md)

[B2C uygulaması oluşturma](create-b2c-app.md)

[Kullanıcı akış ilkeleri oluşturma](create-user-flow-policies.md)

[Sosyal kimlik sağlayıcıları ekleme (İsteğe bağlı)](add-social-identity-providers.md)

[Commerce Headquarters'ı yeni Azure AD B2C bilgileri ile güncelleştirme](update-hq-aad-b2c-info.md)

[Commerce site oluşturucuda B2C kiracınızı yapılandırma](config-b2c-tenant-site-builder.md)

[Ek B2C bilgileri](additional-b2c-info.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
