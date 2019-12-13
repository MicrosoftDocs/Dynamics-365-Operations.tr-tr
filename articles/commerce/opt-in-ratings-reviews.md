---
title: Derecelendirme ve incelemeleri kullanmayı kabul etme
description: Bu konu, Microsoft Dynamics 365 Commerce sitenizde derecelendirmelerin ve incelemelerinizin nasıl kullanılacağını açıklamaktadır.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 10e3c33af232fa46df09a103b2e73eae09a909eb
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697992"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>Derecelendirme ve incelemeleri kullanmayı kabul etme

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce sitenizde derecelendirmelerin ve incelemelerinizin nasıl kullanılacağını açıklamaktadır.

## <a name="overview"></a>Genel Bakış

Derecelendirmeler ve İncelemeler çözümü, Microsoft Dynamics Lifecycle Services (LCS) kullanarak Dynamics 365 Commerce kullanabileceğiniz bir çok yönlü kanal çözümüdür. LCS, perakendeciler tarafından yetki alma için sağlama kaynağı yönetiminde kullanılan bir yönetim portaldır.

Commerce Web sitenizde derecelendirmeler ve İncelemeler çözümünü kullanmak istiyorsanız, önce bunu kabul etmelisiniz.

## <a name="opt-in-to-use-ratings-and-reviews"></a>Derecelendirme ve incelemeleri kullanmayı kabul etme

Sitenizde derecelendirme ve İncelemeler kullanmayı kabul etmek için aşağıdaki adımları izleyin.

1. [Yeni e-ticaret sitesi dağıtma](deploy-ecommerce-site.md) adımlarını izleyin.
1. Yine LCS içinde olduğunuzda, **Retail Deployment kurulumuna \> diğer ayarlar**'a gidin.
1. **Derecelendirmeleri etkinleştir ve gözden geçirme hizmeti** seçeneğini **Evet** olarak ayarlayın.
1. Derecelendirmeler için **AAD güvenlik grubunda ve aracı incelendirmesine (güvenlik grubu nesne kodu)** alanına, derecelendirme ve moderatlamaları içeren Microsoft Azure Active Directory (Azure AD) güvenlik grubunun kimliğini girin.

    ![Derecelendirme ve incelemeleri kullanmayı kabul etme](media/LCS_RnR_Preference.png)

1. E-ticaret başlatma sürecini tamamlayın.

## <a name="additional-resources"></a>Ek kaynaklar

[Derecelendirme ve incelemelere genel bakış](ratings-reviews-overview.md)

[Derecelendirme ve incelemeleri yönetme](manage-reviews.md)

[Derecelendirme ve incelemeleri yapılandırma](configure-ratings-reviews.md)

[Dynamics 365 Retail'de ürün derecelendirmelerini eşitleme](sync-product-ratings.md)
