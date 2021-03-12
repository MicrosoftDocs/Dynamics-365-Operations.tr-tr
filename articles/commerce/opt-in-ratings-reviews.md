---
title: Derecelendirme ve incelemeleri kullanmayı kabul etme
description: Bu konu, Microsoft Dynamics 365 Commerce sitenizde derecelendirmelerin ve incelemelerinizin nasıl kullanılacağını açıklamaktadır.
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: 481a8750b2333d5dd5de2c05e175569804a6046f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985848"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>Derecelendirme ve incelemeleri kullanmayı kabul etme

[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce sitenizde derecelendirmelerin ve incelemelerinizin nasıl kullanılacağını açıklamaktadır.

## <a name="overview"></a>Genel Bakış

Derecelendirmeler ve İncelemeler çözümü, Microsoft Dynamics Lifecycle Services (LCS) kullanarak Dynamics 365 Commerce kullanabileceğiniz bir çok yönlü kanal çözümüdür. LCS, perakendeciler tarafından yetki alma için sağlama kaynağı yönetiminde kullanılan bir yönetim portaldır.

Commerce web sitenizde derecelendirmeler ve incelemeler çözümünü kullanmak istiyorsanız, Dynamics 365 Commerce'te e-ticaret sitenizin dağıtım sırasında derecelendirmelere ve incelemelere karşı kabul etmelisiniz.

## <a name="opt-in-to-use-ratings-and-reviews"></a>Derecelendirme ve incelemeleri kullanmayı kabul etme

Sitenizde derecelendirme ve İncelemeler kullanmayı kabul etmek için aşağıdaki adımları izleyin.

1. [Yeni e-ticaret sitesi dağıtma](deploy-ecommerce-site.md) adımlarını izleyin.
1. Yine LCS içinde olduğunuzda, **Retail Deployment kurulumuna \> diğer ayarlar**'a gidin.
1. **Derecelendirmeleri etkinleştir ve gözden geçirme hizmeti** seçeneğini **Evet** olarak ayarlayın.
1. Derecelendirmeler için **AAD güvenlik grubunda ve aracı incelendirmesine (güvenlik grubu nesne kodu)** alanına, derecelendirme ve moderatlamaları içeren Microsoft Azure Active Directory (Azure AD) güvenlik grubunun kimliğini girin.

    ![Derecelendirme ve incelemeleri kullanmayı kabul etme](media/LCS_RnR_Preference.png)

1. E-ticaret başlatma sürecini tamamlayın.

> [!NOTE] 
> Derecelendirme ve İncelemeler gerekmeden henüz bir e-ticaret sitesi dağıtmış olan ve şimdi Dynamics 365 Commerce paketten alınan derecelendirme ve değerlendirmeleri kullanan bir Dynamics 365 Commerce müşteriniz varsa, lütfen bir servis isteği gönderin. Servis isteği gönderme hakkında bilgi için bkz. [Hizmet istekleri sürecini gönder](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json). 

## <a name="additional-resources"></a>Ek kaynaklar

[Derecelendirmelere ve incelemelere genel bakış](ratings-reviews-overview.md)

[Derecelendirme ve incelemeleri yönetme](manage-reviews.md)

[Derecelendirme ve incelemeleri yapılandırma](configure-ratings-reviews.md)

[Dynamics 365 Commerce'de ürün derecelendirmelerini eşitleme](sync-product-ratings.md)


