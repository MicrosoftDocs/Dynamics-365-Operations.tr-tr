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
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: edd2082b5d2cafcb955f8e3c7762bcba523ac479
ms.sourcegitcommit: 0dace221e8874021dd212271567666f717d39793
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2020
ms.locfileid: "3071578"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="96cee-103">Derecelendirme ve incelemeleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="96cee-103">Configure ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="96cee-104">Bu konuda, e-ticaret sitenizi Microsoft Dynamics 365 Commerce'te müşteri derecelendirmelerini ve incelemelerini gösterecek şekilde konfigüre etme yöntemi açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="96cee-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="96cee-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="96cee-105">Overview</span></span>

<span data-ttu-id="96cee-106">E-ticaret web sitelerindeki derecelendirmeler ve incelemeler, müşterilere bir satın alma kararı vermeden önce, bu ürünler hakkındaki diğer müşterilerin ne düşündüğünü göstererek, ürünler hakkında bilgi edinmesine yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="96cee-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision by showing them what other customers think about those products.</span></span> <span data-ttu-id="96cee-107">E-ticaret web sitelerinde, derecelendirmeler ve incelemeler, ürünler hakkında müşteri geribildirimi toplamaya yönelik bir mekanizmadır.</span><span class="sxs-lookup"><span data-stu-id="96cee-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="96cee-108">Derecelendirme ve incelemeleri gösterecek site yapılandırma</span><span class="sxs-lookup"><span data-stu-id="96cee-108">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="96cee-109">Kiracı kimliği, metin uzunluğunu gözden geçirme ve Başlık uzunluğunu gözden geçirme gibi derecelendirmeler ve incelemelerde ilgili konfigürasyon değerleri site düzeyinde yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="96cee-109">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="96cee-110">Derecelendirmeleri ve değerlendirmeleri göstermek üzere bir site yapılandırmak için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="96cee-110">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="96cee-111">**Ev \> Siteler**e gidin.</span><span class="sxs-lookup"><span data-stu-id="96cee-111">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="96cee-112">Sitenizin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="96cee-112">Select the name of your site.</span></span> 
1. <span data-ttu-id="96cee-113">**Site ayarları \> uzantılarına** gidin.</span><span class="sxs-lookup"><span data-stu-id="96cee-113">Go to **Site settings \> Extensions**.</span></span> 
1. <span data-ttu-id="96cee-114">**En fazla metni gözden geçir** alanına, metni İnceleme için gereken maksimum karakter sayısını (örneğin, **1000**) girin.</span><span class="sxs-lookup"><span data-stu-id="96cee-114">In the **Review text max length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="96cee-115">**En fazla başlık gözden geçir** alanına, başlık İnceleme için gereken maksimum karakter sayısını (örneğin, **55**) girin.</span><span class="sxs-lookup"><span data-stu-id="96cee-115">In the **Review title max length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="96cee-116">**kaydet ve yayınla**yı seçin.</span><span class="sxs-lookup"><span data-stu-id="96cee-116">Select **Save and Publish**.</span></span> 

<span data-ttu-id="96cee-117">Aşağıdaki çizim, bu yapılandırmasının Dynamics 365 Commerce'te nasıl gözükeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="96cee-117">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Derecelendirme ve incelemeleri gösterecek site yapılandırma](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="96cee-119">Bir ürün derecelendirmesini PDP'nin incelemeler bölümüne bağlama</span><span class="sxs-lookup"><span data-stu-id="96cee-119">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="96cee-120">Ürün derecelendirmesi, PDP'nin en üstünde ürün başlığının altında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="96cee-120">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="96cee-121">Ürün derecelendirmesi, aynı PDP'nin **incelemeler** bölümüyle bağlantılı olacak şekilde konfigüre edilebilir.</span><span class="sxs-lookup"><span data-stu-id="96cee-121">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="96cee-122">Bir ürün derecelendirmesini PDP 'nin **incelemeler** bölümüne bağlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="96cee-122">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="96cee-123">PDP şablonu açın.</span><span class="sxs-lookup"><span data-stu-id="96cee-123">Open the PDP template.</span></span> 
1. <span data-ttu-id="96cee-124">**Satın alma kutusu konteyner modülü ayarlarına** git.</span><span class="sxs-lookup"><span data-stu-id="96cee-124">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="96cee-125">**Satınalma kutusu** altında, **ürün derecelendirmeleri**'ni seçin ve sonra **bağlantıyı tam gözden geçirme modülü için tıklatın** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="96cee-125">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="96cee-126">Aşağıdaki çizim, bu yapılandırmasının Dynamics 365 Commerce'te nasıl gözükeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="96cee-126">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Bir ürün derecelendirmesini PDP'nin incelemeler bölümüne bağlama](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="96cee-128">Gizlilik ve ilke sayfası için bağlantıyı yapılandırın</span><span class="sxs-lookup"><span data-stu-id="96cee-128">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="96cee-129">Gizlilik ve ilke sayfası için bağlantıyı yapılandırmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="96cee-129">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="96cee-130">**Ev \> Siteler**e gidin.</span><span class="sxs-lookup"><span data-stu-id="96cee-130">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="96cee-131">Sitenizin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="96cee-131">Select the name of your site.</span></span> 
1. <span data-ttu-id="96cee-132">**Site ayarları \> uzantılarına** gidin.</span><span class="sxs-lookup"><span data-stu-id="96cee-132">Go to **Site settings \> Extensions**.</span></span>
1. <span data-ttu-id="96cee-133">**Rotalar** sekmesinde, **RNR Gizlilik ve ilke** altında **bağlantı ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="96cee-133">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="96cee-134">Zaten bir bağlantı girilmiş ve bunu değiştirmek istiyorsanız, bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="96cee-134">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="96cee-135">**Bağlantı ekle** iletişim kutusunda gizlilik ve ilke sayfası bağlantısını seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="96cee-135">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="96cee-136">**kaydet ve yayınla**yı seçin.</span><span class="sxs-lookup"><span data-stu-id="96cee-136">Select **Save and Publish**.</span></span> 

<span data-ttu-id="96cee-137">Aşağıdaki çizim, bu yapılandırmasının Dynamics 365 Commerce'te nasıl gözükeceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="96cee-137">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Gizlilik ve ilke sayfası için bağlantıyı yapılandırın](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="configure-ratings-and-reviews-modules-on-product-details-pages"></a><span data-ttu-id="96cee-139">Ürün ayrıntıları sayfalarındaki derecelendirme ve İnceleme modüllerini konfigüre edin</span><span class="sxs-lookup"><span data-stu-id="96cee-139">Configure ratings and reviews modules on product details pages</span></span>

<span data-ttu-id="96cee-140">Ürün Ayrıntıları sayfalarındaki derecelendirmeleri konfigüre etme ve modüllerin modüllerini İnceleme hakkında bilgi için bkz [Derecelendirme ve incelemeler](ratings-reviews-modules.md).</span><span class="sxs-lookup"><span data-stu-id="96cee-140">For information on configuring ratings and reviews modules on product details pages, see [Ratings and reviews modules](ratings-reviews-modules.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="96cee-141">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="96cee-141">Additional resources</span></span>

[<span data-ttu-id="96cee-142">Derecelendirmelere ve incelemelere genel bakış</span><span class="sxs-lookup"><span data-stu-id="96cee-142">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="96cee-143">Derecelendirme ve incelemeleri kullanmayı kabul etme</span><span class="sxs-lookup"><span data-stu-id="96cee-143">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="96cee-144">Derecelendirme ve incelemeleri yönetme</span><span class="sxs-lookup"><span data-stu-id="96cee-144">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="96cee-145">Ürün ayrıntıları sayfalarındaki derecelendirme ve İnceleme modüllerini konfigüre edin</span><span class="sxs-lookup"><span data-stu-id="96cee-145">Configure ratings and reviews modules on product details pages</span></span>](ratings-reviews-modules.md)

[<span data-ttu-id="96cee-146">Dynamics 365 Retail'de ürün derecelendirmelerini eşitleme</span><span class="sxs-lookup"><span data-stu-id="96cee-146">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
