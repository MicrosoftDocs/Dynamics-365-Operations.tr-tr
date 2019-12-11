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
# <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="58a7d-103">Derecelendirme ve incelemeleri kullanmayı kabul etme</span><span class="sxs-lookup"><span data-stu-id="58a7d-103">Opt in to use ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="58a7d-104">Bu konu, Microsoft Dynamics 365 Commerce sitenizde derecelendirmelerin ve incelemelerinizin nasıl kullanılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="58a7d-104">This topic explains how to opt in to use ratings and reviews on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="58a7d-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="58a7d-105">Overview</span></span>

<span data-ttu-id="58a7d-106">Derecelendirmeler ve İncelemeler çözümü, Microsoft Dynamics Lifecycle Services (LCS) kullanarak Dynamics 365 Commerce kullanabileceğiniz bir çok yönlü kanal çözümüdür.</span><span class="sxs-lookup"><span data-stu-id="58a7d-106">The ratings and reviews solution is an omnichannel solution that you can make available in Dynamics 365 Commerce by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="58a7d-107">LCS, perakendeciler tarafından yetki alma için sağlama kaynağı yönetiminde kullanılan bir yönetim portaldır.</span><span class="sxs-lookup"><span data-stu-id="58a7d-107">LCS is an administration portal that retailers use to manage their environments from provisioning to decommissioning.</span></span>

<span data-ttu-id="58a7d-108">Commerce Web sitenizde derecelendirmeler ve İncelemeler çözümünü kullanmak istiyorsanız, önce bunu kabul etmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="58a7d-108">If you want to use the ratings and reviews solution on your Commerce website, you must first opt in.</span></span>

## <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="58a7d-109">Derecelendirme ve incelemeleri kullanmayı kabul etme</span><span class="sxs-lookup"><span data-stu-id="58a7d-109">Opt in to use ratings and reviews</span></span>

<span data-ttu-id="58a7d-110">Sitenizde derecelendirme ve İncelemeler kullanmayı kabul etmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="58a7d-110">To opt in to use ratings and reviews on your site, follow these steps.</span></span>

1. <span data-ttu-id="58a7d-111">[Yeni e-ticaret sitesi dağıtma](deploy-ecommerce-site.md) adımlarını izleyin.</span><span class="sxs-lookup"><span data-stu-id="58a7d-111">Follow the steps in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span>
1. <span data-ttu-id="58a7d-112">Yine LCS içinde olduğunuzda, **Retail Deployment kurulumuna \> diğer ayarlar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="58a7d-112">While you're still in LCS, go to **Retail deployment setup \> Other settings**.</span></span>
1. <span data-ttu-id="58a7d-113">**Derecelendirmeleri etkinleştir ve gözden geçirme hizmeti** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="58a7d-113">Set the **Enable ratings and reviews service** option to **Yes**.</span></span>
1. <span data-ttu-id="58a7d-114">Derecelendirmeler için **AAD güvenlik grubunda ve aracı incelendirmesine (güvenlik grubu nesne kodu)** alanına, derecelendirme ve moderatlamaları içeren Microsoft Azure Active Directory (Azure AD) güvenlik grubunun kimliğini girin.</span><span class="sxs-lookup"><span data-stu-id="58a7d-114">In the **AAD security group for ratings and review moderator (security group object id)** field, enter the ID of the Microsoft Azure Active Directory (Azure AD) security group that includes the ratings and reviews moderators.</span></span>

    ![Derecelendirme ve incelemeleri kullanmayı kabul etme](media/LCS_RnR_Preference.png)

1. <span data-ttu-id="58a7d-116">E-ticaret başlatma sürecini tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="58a7d-116">Complete the e-Commerce initialization process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="58a7d-117">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="58a7d-117">Additional resources</span></span>

[<span data-ttu-id="58a7d-118">Derecelendirme ve incelemelere genel bakış</span><span class="sxs-lookup"><span data-stu-id="58a7d-118">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="58a7d-119">Derecelendirme ve incelemeleri yönetme</span><span class="sxs-lookup"><span data-stu-id="58a7d-119">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="58a7d-120">Derecelendirme ve incelemeleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="58a7d-120">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="58a7d-121">Dynamics 365 Retail'de ürün derecelendirmelerini eşitleme</span><span class="sxs-lookup"><span data-stu-id="58a7d-121">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
