---
title: Derecelendirme ve incelemeleri yapılandırma
description: Bu konuda, e-ticaret sitenizi Microsoft Dynamics 365 Commerce'te müşteri derecelendirmelerini ve incelemelerini gösterecek şekilde konfigüre etme yöntemi açıklanmıştır.
author: gvrmohanreddy
manager: annbe
ms.date: 02/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3fcdf571378c25d71b3ef4f3baad062a25390417
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993562"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="3c2e3-103">Derecelendirme ve incelemeleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="3c2e3-103">Configure ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3c2e3-104">Bu konuda, e-ticaret sitenizi Microsoft Dynamics 365 Commerce'te müşteri derecelendirmelerini ve incelemelerini gösterecek şekilde konfigüre etme yöntemi açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="3c2e3-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3c2e3-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="3c2e3-105">Overview</span></span>

<span data-ttu-id="3c2e3-106">E-ticaret web sitelerindeki derecelendirmeler ve incelemeler, müşterilere bir satın alma kararı vermeden önce, bu ürünler hakkındaki diğer müşterilerin ne düşündüğünü göstererek, ürünler hakkında bilgi edinmesine yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="3c2e3-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision by showing them what other customers think about those products.</span></span> <span data-ttu-id="3c2e3-107">E-ticaret web sitelerinde, derecelendirmeler ve incelemeler, ürünler hakkında müşteri geribildirimi toplamaya yönelik bir mekanizmadır.</span><span class="sxs-lookup"><span data-stu-id="3c2e3-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="3c2e3-108">Derecelendirme ve incelemeleri gösterecek site yapılandırma</span><span class="sxs-lookup"><span data-stu-id="3c2e3-108">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="3c2e3-109">Kiracı kimliği, metin uzunluğunu gözden geçirme ve Başlık uzunluğunu gözden geçirme gibi derecelendirmeler ve incelemelerde ilgili konfigürasyon değerleri site düzeyinde yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="3c2e3-109">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="3c2e3-110">Derecelendirmeleri ve değerlendirmeleri göstermek üzere bir site yapılandırmak için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="3c2e3-110">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="3c2e3-111">**Ev \> Siteler** e gidin.</span><span class="sxs-lookup"><span data-stu-id="3c2e3-111">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="3c2e3-112">Sitenizin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="3c2e3-112">Select the name of your site.</span></span> 
1. <span data-ttu-id="3c2e3-113">**Site ayarları \> uzantılarına** gidin.</span><span class="sxs-lookup"><span data-stu-id="3c2e3-113">Go to **Site settings \> Extensions**.</span></span> 
1. <span data-ttu-id="3c2e3-114">**En fazla metni gözden geçir** alanına, metni İnceleme için gereken maksimum karakter sayısını (örneğin, **1000**) girin.</span><span class="sxs-lookup"><span data-stu-id="3c2e3-114">In the **Review text max length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="3c2e3-115">**En fazla başlık gözden geçir** alanına, başlık İnceleme için gereken maksimum karakter sayısını (örneğin, **55**) girin.</span><span class="sxs-lookup"><span data-stu-id="3c2e3-115">In the **Review title max length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="3c2e3-116">**kaydet ve yayınla** yı seçin.</span><span class="sxs-lookup"><span data-stu-id="3c2e3-116">Select **Save and Publish**.</span></span> 

<span data-ttu-id="3c2e3-117">Aşağıdaki çizim, bu yapılandırmasının Dynamics 365 Commerce'te nasıl gözükeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="3c2e3-117">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Derecelendirme ve incelemeleri gösterecek site yapılandırma](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="3c2e3-119">Bir ürün derecelendirmesini PDP'nin incelemeler bölümüne bağlama</span><span class="sxs-lookup"><span data-stu-id="3c2e3-119">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="3c2e3-120">Ürün derecelendirmesi, PDP'nin en üstünde ürün başlığının altında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="3c2e3-120">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="3c2e3-121">Ürün derecelendirmesi, aynı PDP'nin **incelemeler** bölümüyle bağlantılı olacak şekilde konfigüre edilebilir.</span><span class="sxs-lookup"><span data-stu-id="3c2e3-121">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="3c2e3-122">Bir ürün derecelendirmesini PDP 'nin **incelemeler** bölümüne bağlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="3c2e3-122">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="3c2e3-123">PDP şablonu açın.</span><span class="sxs-lookup"><span data-stu-id="3c2e3-123">Open the PDP template.</span></span> 
1. <span data-ttu-id="3c2e3-124">**Satın alma kutusu konteyner modülü ayarlarına** git.</span><span class="sxs-lookup"><span data-stu-id="3c2e3-124">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="3c2e3-125">**Satınalma kutusu** altında, **ürün derecelendirmeleri**'ni seçin ve sonra **bağlantıyı tam gözden geçirme modülü için tıklatın** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="3c2e3-125">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="3c2e3-126">Aşağıdaki çizim, bu yapılandırmasının Dynamics 365 Commerce'te nasıl gözükeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="3c2e3-126">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Bir ürün derecelendirmesini PDP'nin incelemeler bölümüne bağlama](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="3c2e3-128">Gizlilik ve ilke sayfası için bağlantıyı yapılandırın</span><span class="sxs-lookup"><span data-stu-id="3c2e3-128">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="3c2e3-129">Gizlilik ve ilke sayfası için bağlantıyı yapılandırmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="3c2e3-129">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="3c2e3-130">**Ev \> Siteler** e gidin.</span><span class="sxs-lookup"><span data-stu-id="3c2e3-130">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="3c2e3-131">Sitenizin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="3c2e3-131">Select the name of your site.</span></span> 
1. <span data-ttu-id="3c2e3-132">**Site ayarları \> uzantılarına** gidin.</span><span class="sxs-lookup"><span data-stu-id="3c2e3-132">Go to **Site settings \> Extensions**.</span></span>
1. <span data-ttu-id="3c2e3-133">**Rotalar** sekmesinde, **RNR Gizlilik ve ilke** altında **bağlantı ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3c2e3-133">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="3c2e3-134">Zaten bir bağlantı girilmiş ve bunu değiştirmek istiyorsanız, bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="3c2e3-134">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="3c2e3-135">**Bağlantı ekle** iletişim kutusunda gizlilik ve ilke sayfası bağlantısını seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="3c2e3-135">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="3c2e3-136">**kaydet ve yayınla** yı seçin.</span><span class="sxs-lookup"><span data-stu-id="3c2e3-136">Select **Save and Publish**.</span></span> 

<span data-ttu-id="3c2e3-137">Aşağıdaki çizim, bu yapılandırmasının Dynamics 365 Commerce'te nasıl gözükeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="3c2e3-137">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Gizlilik ve ilke sayfası için bağlantıyı yapılandırın](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="configure-ratings-and-reviews-modules-on-product-details-pages"></a><span data-ttu-id="3c2e3-139">Ürün ayrıntıları sayfalarındaki derecelendirme ve İnceleme modüllerini konfigüre edin</span><span class="sxs-lookup"><span data-stu-id="3c2e3-139">Configure ratings and reviews modules on product details pages</span></span>

<span data-ttu-id="3c2e3-140">Ürün Ayrıntıları sayfalarındaki derecelendirmeleri konfigüre etme ve modüllerin modüllerini İnceleme hakkında bilgi için bkz [Derecelendirme ve incelemeler](ratings-reviews-modules.md).</span><span class="sxs-lookup"><span data-stu-id="3c2e3-140">For information on configuring ratings and reviews modules on product details pages, see [Ratings and reviews modules](ratings-reviews-modules.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3c2e3-141">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="3c2e3-141">Additional resources</span></span>

[<span data-ttu-id="3c2e3-142">Derecelendirmelere ve incelemelere genel bakış</span><span class="sxs-lookup"><span data-stu-id="3c2e3-142">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="3c2e3-143">Derecelendirme ve incelemeleri kullanmayı kabul etme</span><span class="sxs-lookup"><span data-stu-id="3c2e3-143">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="3c2e3-144">Derecelendirme ve incelemeleri yönetme</span><span class="sxs-lookup"><span data-stu-id="3c2e3-144">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="3c2e3-145">Ürün ayrıntıları sayfalarındaki derecelendirme ve İnceleme modüllerini konfigüre edin</span><span class="sxs-lookup"><span data-stu-id="3c2e3-145">Configure ratings and reviews modules on product details pages</span></span>](ratings-reviews-modules.md)

[<span data-ttu-id="3c2e3-146">Dynamics 365 Retail'de ürün derecelendirmelerini eşitleme</span><span class="sxs-lookup"><span data-stu-id="3c2e3-146">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
