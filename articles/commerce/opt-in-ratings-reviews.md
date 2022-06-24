---
title: Derecelendirme ve incelemeleri kullanmayı kabul etme
description: Bu makale, Microsoft Dynamics 365 Commerce sitenizde derecelendirmelerin ve incelemelerinizin nasıl kullanılacağını açıklamaktadır.
author: gvrmohanreddy
ms.date: 02/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b591799bd5bf00e74e782040bfdc1b678c4c87d0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906924"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>Derecelendirme ve incelemeleri kullanmayı kabul etme

[!include [banner](includes/banner.md)]

Bu makale, Microsoft Dynamics 365 Commerce sitenizde derecelendirmelerin ve incelemelerinizin nasıl kullanılacağını açıklamaktadır.

Derecelendirmeler ve İncelemeler çözümü, Microsoft Dynamics Lifecycle Services (LCS) kullanarak Dynamics 365 Commerce kullanabileceğiniz bir çok yönlü kanal çözümüdür. LCS, perakendeciler tarafından yetki alma için sağlama kaynağı yönetiminde kullanılan bir yönetim portaldır.

Commerce web sitenizde derecelendirmeler ve incelemeler çözümünü kullanmak istiyorsanız, Dynamics 365 Commerce'te e-ticaret sitenizin dağıtım sırasında derecelendirmelere ve incelemelere karşı kabul etmelisiniz.

## <a name="opt-in-to-use-ratings-and-reviews"></a>Derecelendirme ve incelemeleri kullanmayı kabul etme

Sitenizde derecelendirme ve İncelemeler kullanmayı kabul etmek için aşağıdaki adımları izleyin.

1. [Yeni e-ticaret sitesi dağıtma](deploy-ecommerce-site.md) adımlarını izleyin.
1. Yine LCS içinde olduğunuzda, **Retail Deployment kurulumuna \> diğer ayarlar**'a gidin.
1. **Derecelendirmeleri etkinleştir ve gözden geçirme hizmeti** seçeneğini **Evet** olarak ayarlayın.
1. Derecelendirmeler için **AAD güvenlik grubunda ve aracı incelendirmesine** alanına, derecelendirme ve moderatlamaları içeren Microsoft Azure Active Directory (Azure AD) güvenlik grubunun kimliğini girin.

    ![Derecelendirme ve incelemeleri kullanmayı kabul etme.](media/LCS_RnR_Preference_2.png)

1. E-ticaret başlatma sürecini tamamlayın.

> [!NOTE] 
> Derecelendirme ve İncelemeler gerekmeden henüz bir e-ticaret sitesi dağıtmış olan ve şimdi Dynamics 365 Commerce paketten alınan derecelendirme ve değerlendirmeleri kullanan bir Dynamics 365 Commerce müşteriniz varsa, lütfen bir servis isteği gönderin. Servis isteği gönderme hakkında bilgi için bkz. [Hizmet istekleri sürecini gönder](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json). 

## <a name="additional-resources"></a>Ek kaynaklar

[Derecelendirmelere ve incelemelere genel bakış](ratings-reviews-overview.md)

[Derecelendirme ve incelemeleri yönetme](manage-reviews.md)

[Derecelendirme ve incelemeleri yapılandırma](configure-ratings-reviews.md)

[Dynamics 365 Commerce'de ürün derecelendirmelerini eşitleme](sync-product-ratings.md)

[Derecelendirmelerin ve incelemelerin moderatör tarafından el ile yayımlanmasını etkinleştirme](manual-publish-rating-reviews.md)

[Derecelendirmeleri ve değerlendirmeleri içe ve dışa aktarma](import-export-reviews.md)

[Hizmetten hizmete kimlik doğrulamasını yapılandırma](service-to-service-auth.md)

[Derecelendirmeler ve incelemelerle ilgili SSS](ratings-reviews-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
