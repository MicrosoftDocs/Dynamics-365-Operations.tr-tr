---
title: Hizmetten hizmete kimlik doğrulamasını yapılandırma
description: Bu makalede, derecelendirmelere ve incelemelere ilişkin hizmet API'lerini güvenli şekilde çağırmak amacıyla Microsoft Dynamics 365 Commerce'te Hizmetten Hizmete kimlik doğrulamasının nasıl yapılandırılacağı açıklanmaktadır.
author: gvrmohanreddy
ms.date: 01/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: acb3a6220d146d32bbeb5bd8169033bc897ec3fe
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871619"
---
# <a name="configure-service-to-service-authentication"></a>Hizmetten hizmete kimlik doğrulamasını yapılandırma

[!include [banner](includes/banner.md)]

Bu makalede, derecelendirmelere ve incelemelere ilişkin hizmet uygulama programlama arabirimlerini (API'ler) güvenli şekilde çağırmak amacıyla Microsoft Dynamics 365 Commerce'te Hizmetten Hizmete (S2S) kimlik doğrulamasının nasıl yapılandırılacağı açıklanmaktadır.

Dynamics 365 Commerce, çok kanallı çözüm olarak [derecelendirmeler ve incelemeler](ratings-reviews-overview.md) sunar. Bu çözüm, çeşitli görevlerin gerçekleştirilebileceği şekilde, Commerce dışından gelen hizmet API'lerine erişim sağlar. Bu görevler harici sisteminizden gelen derecelendirmeleri ve değerlendirmeleri Commerce'e aktarmayı ve derecelendirmeler ve incelemeleri Commerce'den dışa aktarmayı içerir. Commerce'in derecelendirmeleri ve incelemeleri güvenli bir şekilde çağırmasını etkinleştirmek için öncelikle bu makaledeki prosedürleri tamamlayarak S2S kimlik doğrulamasını yapılandırmanız gerekir.

## <a name="add-a-new-app-registration"></a>Yeni uygulama kaydı ekle

Yeni bir uygulama kaydı ekleyebilmek için, [Azure portalını](https://portal.azure.com) kullanarak bir uygulama oluşturmanız gerekir. Azure Active Directory'de (Azure AD) bir uygulama kaydetmek ve kimlik doğrulamayı etkinleştirmek için [Power Automate'te özel bağlayıcıyla Azure Active Directory kullanma](/connectors/custom-connectors/azure-active-directory-authentication) konusundaki adımları izleyin.

Azure portalından aşağıdaki kimlikleri toplayın. Aşağıdaki adımlarda bu kimliklere gereksinim duyarsınız.

- İstemci uygulaması kodu
- İstemci dizini (kiracı) kimliği

Commerce site oluşturucuda yeni bir uygulama kaydı oluşturmak için aşağıdaki adımları izleyin.

1. **Giriş \> İncelemeler \> Ayarlar**'a gidin.
1. **Hizmetten Hizmete (S2S) Kimlik Doğrulaması** altında **Yönet**'i seçin.

    ![Commerce site oluşturucudaki Hizmetten Hizmete (S2S) Kimlik Doğrulaması bölümündeki yönet düğmesi.](media/Ratings-reviews-settings-service-to-service-authentication.png)

1. Sağda görüntülenen **S2S Uygulama Girişleri** bölmesinde, **Yeni S2S Uygulama Kaydı ekle**'yi seçin.
1. **S2S Uygulama Girişi Ekle** iletişim kutusuna, aşağıdaki gerekli bilgileri girin. Azure uygulama kaydı içindeki değerleri kullanın.

    - **Ad** - Uygulamanızın adını girin (ör. **Fabrikam Uygulaması**).
    - **İstemci Uygulama Kimliği** - Uygulama kimliğini girin (ör. **00000000-0000-0000-0000-000000000000**).
    - **Dizin (Kiracı) Kimliği** - Dizin kimliğini girin (ör. **00000000-0000-0000-0000-000000000000**).

    ![Commerce site oluşturucusunda S2S Uygulama Girişi Ekle iletişim kutusu.](media/Ratings-reviews-settings-S2S-APP-entry.png)

1. **Gönder**'i seçin. Uygulamanızın adı, **S2S Uygulama Girişleri** bölmesinde görüntülenmelidir.
1. **S2S Uygulama Girişleri** bölmesini kapatın.
1. **Kaydet**'i seçin.

## <a name="edit-an-existing-app-registration"></a>Varolan bir uygulama kaydını düzenle

Commerce site oluşturucuda varolan bir uygulama kaydını düzenlemek için aşağıdaki adımları izleyin.

1. **Giriş \> İncelemeler \> Ayarlar**'a gidin.
1. **Hizmetten Hizmete (S2S) Kimlik Doğrulaması** altında **Yönet**'i seçin.
1. **S2S Uygulama Girişleri** bölmesinde, düzenlemek istediğiniz girdinin yanındaki kalem simgesini seçin.
1. **Ad**, **İstemci Uygulama Kimliği** ve **Dizin (kiracı) kimlik** alanlarındaki değerleri gerektiği gibi güncelleştirin.
1. **Gönder**'i seçin.
1. **S2S Uygulama Girişleri** bölmesini kapatın.
1. **Kaydet**'i seçin.

## <a name="remove-an-existing-app-registration"></a>Varolan bir uygulama kaydını kaldırma

Commerce site oluşturucuda varolan bir uygulama kaydını kaldırmak için aşağıdaki adımları izleyin.

1. **Giriş \> İncelemeler \> Ayarlar**'a gidin.
1. **Hizmetten Hizmete (S2S) Kimlik Doğrulaması** altında **Yönet**'i seçin.
1. **S2S Uygulama Girişleri** bölmesinde, kaldırmak istediğiniz girdinin yanındaki çöp kutusu simgesini seçin. Giriş listeden kaldırılır.
1. **S2S Uygulama Girişleri** bölmesini kapatın.
1. **Kaydet**'i seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Derecelendirmelere ve incelemelere genel bakış](ratings-reviews-overview.md)

[Derecelendirme ve incelemeleri kullanmayı kabul etme](opt-in-ratings-reviews.md)

[Derecelendirme ve incelemeleri yönetme](manage-reviews.md)

[Derecelendirme ve incelemeleri yapılandırma](configure-ratings-reviews.md)

[Ürün derecelendirmelerini eşitleme](sync-product-ratings.md)

[Derecelendirmelerin ve incelemelerin moderatör tarafından el ile yayımlanmasını etkinleştirme](manual-publish-rating-reviews.md)

[Derecelendirmeleri ve değerlendirmeleri içe ve dışa aktarma](import-export-reviews.md)

[Derecelendirmeler ve incelemelerle ilgili SSS](ratings-reviews-faq.md) 
