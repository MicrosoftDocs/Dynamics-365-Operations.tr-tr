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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cbdb69202ebec19f4442041cfb1f99857da36d2e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416434"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="4cfd0-103">Derecelendirme ve incelemeleri kullanmayı kabul etme</span><span class="sxs-lookup"><span data-stu-id="4cfd0-103">Opt in to use ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4cfd0-104">Bu konu, Microsoft Dynamics 365 Commerce sitenizde derecelendirmelerin ve incelemelerinizin nasıl kullanılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="4cfd0-104">This topic explains how to opt in to use ratings and reviews on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="4cfd0-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="4cfd0-105">Overview</span></span>

<span data-ttu-id="4cfd0-106">Derecelendirmeler ve İncelemeler çözümü, Microsoft Dynamics Lifecycle Services (LCS) kullanarak Dynamics 365 Commerce kullanabileceğiniz bir çok yönlü kanal çözümüdür.</span><span class="sxs-lookup"><span data-stu-id="4cfd0-106">The ratings and reviews solution is an omni-channel solution that you can make available in Dynamics 365 Commerce by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="4cfd0-107">LCS, perakendeciler tarafından yetki alma için sağlama kaynağı yönetiminde kullanılan bir yönetim portaldır.</span><span class="sxs-lookup"><span data-stu-id="4cfd0-107">LCS is an administration portal that retailers use to manage their environments from provisioning to decommissioning.</span></span>

<span data-ttu-id="4cfd0-108">Commerce web sitenizde derecelendirmeler ve incelemeler çözümünü kullanmak istiyorsanız, Dynamics 365 Commerce'te e-ticaret sitenizin dağıtım sırasında derecelendirmelere ve incelemelere karşı kabul etmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="4cfd0-108">If you want to use the ratings and reviews solution on your Commerce website, you must opt in for ratings and reviews during deployment of your e-Commerce site on Dynamics 365 Commerce.</span></span>

## <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="4cfd0-109">Derecelendirme ve incelemeleri kullanmayı kabul etme</span><span class="sxs-lookup"><span data-stu-id="4cfd0-109">Opt in to use ratings and reviews</span></span>

<span data-ttu-id="4cfd0-110">Sitenizde derecelendirme ve İncelemeler kullanmayı kabul etmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4cfd0-110">To opt in to use ratings and reviews on your site, follow these steps.</span></span>

1. <span data-ttu-id="4cfd0-111">[Yeni e-ticaret sitesi dağıtma](deploy-ecommerce-site.md) adımlarını izleyin.</span><span class="sxs-lookup"><span data-stu-id="4cfd0-111">Follow the steps in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span>
1. <span data-ttu-id="4cfd0-112">Yine LCS içinde olduğunuzda, **Retail Deployment kurulumuna \> diğer ayarlar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="4cfd0-112">While you're still in LCS, go to **Retail deployment setup \> Other settings**.</span></span>
1. <span data-ttu-id="4cfd0-113">**Derecelendirmeleri etkinleştir ve gözden geçirme hizmeti** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4cfd0-113">Set the **Enable ratings and reviews service** option to **Yes**.</span></span>
1. <span data-ttu-id="4cfd0-114">Derecelendirmeler için **AAD güvenlik grubunda ve aracı incelendirmesine (güvenlik grubu nesne kodu)** alanına, derecelendirme ve moderatlamaları içeren Microsoft Azure Active Directory (Azure AD) güvenlik grubunun kimliğini girin.</span><span class="sxs-lookup"><span data-stu-id="4cfd0-114">In the **AAD security group for ratings and review moderator (security group object id)** field, enter the ID of the Microsoft Azure Active Directory (Azure AD) security group that includes the ratings and reviews moderators.</span></span>

    ![Derecelendirme ve incelemeleri kullanmayı kabul etme](media/LCS_RnR_Preference.png)

1. <span data-ttu-id="4cfd0-116">E-ticaret başlatma sürecini tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="4cfd0-116">Complete the e-Commerce initialization process.</span></span>

> [!NOTE] 
> <span data-ttu-id="4cfd0-117">Derecelendirme ve İncelemeler gerekmeden henüz bir e-ticaret sitesi dağıtmış olan ve şimdi Dynamics 365 Commerce paketten alınan derecelendirme ve değerlendirmeleri kullanan bir Dynamics 365 Commerce müşteriniz varsa, lütfen bir servis isteği gönderin.</span><span class="sxs-lookup"><span data-stu-id="4cfd0-117">If you are an existing Dynamics 365 Commerce customer who has already deployed an e-Commerce site without having opted in for ratings and reviews and now want to use ratings and reviews from the Dynamics 365 Commerce package, please submit a service request.</span></span> <span data-ttu-id="4cfd0-118">Servis isteği gönderme hakkında bilgi için bkz. [Hizmet istekleri sürecini gönder](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="4cfd0-118">For information about how to submit a service request, see [Submit service requests process](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json).</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="4cfd0-119">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="4cfd0-119">Additional resources</span></span>

[<span data-ttu-id="4cfd0-120">Derecelendirmelere ve incelemelere genel bakış</span><span class="sxs-lookup"><span data-stu-id="4cfd0-120">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="4cfd0-121">Derecelendirme ve incelemeleri yönetme</span><span class="sxs-lookup"><span data-stu-id="4cfd0-121">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="4cfd0-122">Derecelendirme ve incelemeleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="4cfd0-122">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="4cfd0-123">Dynamics 365 Commerce'de ürün derecelendirmelerini eşitleme</span><span class="sxs-lookup"><span data-stu-id="4cfd0-123">Sync product ratings in Dynamics 365 Commerce</span></span>](sync-product-ratings.md)


