---
title: Sayfa içeriği erişilebilirliğini doğrulama
description: Bu konuda, Microsoft Dynamics 365 Commerce sayfa içeriğinin erişilebilirliğini nasıl doğrulanacaklarını açıklanmaktadır.
author: josaw1
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 885696c13b0e5353e6dbd9dc21cf075d5e301786
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791643"
---
# <a name="verify-page-content-accessibility"></a><span data-ttu-id="02597-103">Sayfa içeriği erişilebilirliğini doğrulama</span><span class="sxs-lookup"><span data-stu-id="02597-103">Verify page content accessibility</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="02597-104">Bu konuda, Microsoft Dynamics 365 Commerce sayfa içeriğinin erişilebilirliğini nasıl doğrulanacaklarını açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="02597-104">This topic describes how to verify the accessibility of page content in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="02597-105">Bir sayfayı değiştirmeyi bitirdiğinizde, içeriğin Web'deki herkes tarafından erişilebilir olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="02597-105">When you've finished changing a page, you should make sure that the content is accessible to everyone on the web.</span></span> <span data-ttu-id="02597-106">Commerce geliştirme araçlarında, tümleşik [Microsoft Erişilebilirlik Öngörüler](https://accessibilityinsights.io/) hizmetini kullanarak sayfa içeriğinin erişilebilirliğini kolayca doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="02597-106">In the Commerce authoring tools, you can easily verify the accessibility of page content by using the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service.</span></span> <span data-ttu-id="02597-107">Bu hizmet, sayfanızın içeriğini en son [World Wide Web Consortium (W3C) erişilebilirlik](https://www.w3.org/standards/webdesign/accessibility) yönergelerine göre doğrular.</span><span class="sxs-lookup"><span data-stu-id="02597-107">This service verifies your page content against the latest [World Wide Web Consortium (W3C) accessibility](https://www.w3.org/standards/webdesign/accessibility) guidelines.</span></span>

<span data-ttu-id="02597-108">[Microsoft Accessibility Insights](https://accessibilityinsights.io/) tümleştirmesini kullanabilmeniz için önce kiracı veya site düzeyinde açık olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="02597-108">The [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration must be turned on at the tenant or site level before you can use it.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a><span data-ttu-id="02597-109">Kiracınızda bulunan tüm sitelerden Microsoft Erişilebilirlik Insights'ı açın</span><span class="sxs-lookup"><span data-stu-id="02597-109">Turn on Microsoft Accessibility Insights for all the sites in your tenant</span></span>

<span data-ttu-id="02597-110">Kiracınızda bulunan tüm Commerce siteleri için [Microsoft Accessibility Insights](https://accessibilityinsights.io/) tümleştirmesini açmak üzere aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="02597-110">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for all the Commerce sites in your tenant, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="02597-111">Kiracı ayarlarına erişmek için, Commerce'te sistem yöneticisi olarak oturum açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="02597-111">To access tenant settings, you must be signed in to Commerce as a system admin.</span></span>

1. <span data-ttu-id="02597-112">Commerce'te sistem yöneticisi olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="02597-112">Sign in to Commerce as a system admin.</span></span>
1. <span data-ttu-id="02597-113">Sol gezinti bölmesinde, genişletmek için **Kiracı Ayarlarını** seçin (dişli simgesinin yanında).</span><span class="sxs-lookup"><span data-stu-id="02597-113">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
1. <span data-ttu-id="02597-114">**Kiracı ayarları** altında **Özellikler** dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="02597-114">Under **Tenant Settings**, select **Features**.</span></span>
1. <span data-ttu-id="02597-115">**Erişilebilirlik denetimi** seçeneğini **açık** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="02597-115">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a><span data-ttu-id="02597-116">Tek bir site için Microsoft Accessibility Insights'ı aç</span><span class="sxs-lookup"><span data-stu-id="02597-116">Turn on Microsoft Accessibility Insights for a single site</span></span>

<span data-ttu-id="02597-117">Kiracınızda bulunan tek bir Commerce sitesi için [Microsoft Accessibility Insights](https://accessibilityinsights.io/) tümleştirmesini açmak üzere aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="02597-117">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for a single Commerce site, follow these steps.</span></span>

1. <span data-ttu-id="02597-118">**Siteler** altında, **Fabrikam**'ı seçin (veya sitenizin adını).</span><span class="sxs-lookup"><span data-stu-id="02597-118">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="02597-119">Sol gezinti bölmesinde, genişletmek için **Site Ayarları** seçin.</span><span class="sxs-lookup"><span data-stu-id="02597-119">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="02597-120">**Site ayarları** altında **Özellikler** dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="02597-120">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="02597-121">**Erişilebilirlik denetimi** seçeneğini **açık** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="02597-121">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a><span data-ttu-id="02597-122">Giriş sayfasındaki içeriğin erişilebilirliğini doğrulayın</span><span class="sxs-lookup"><span data-stu-id="02597-122">Verify the accessibility of the content on the home page</span></span>

<span data-ttu-id="02597-123">Ticari olarak giriş sayfanızın içeriğini taramak ve doğrulamak amacıyla tümleşik [Microsoft Accessibility Insights](https://accessibilityinsights.io/) hizmetini kullanmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="02597-123">To use the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service to scan and verify the content of your home page in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="02597-124">**Siteler** altında, **Fabrikam**'ı seçin (veya sitenizin adını).</span><span class="sxs-lookup"><span data-stu-id="02597-124">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="02597-125">Soldaki gezinti bölmesinde **Sayfalar** seçin.</span><span class="sxs-lookup"><span data-stu-id="02597-125">In the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="02597-126">Sayfa düzenleyicisinde açmak için giriş sayfasını bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="02597-126">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="02597-127">Komut çubuğunda, **Erişilebilirliği kontrol et** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="02597-127">On the command bar, select **Check accessibility**.</span></span> <span data-ttu-id="02597-128">**Erişilebilirlik denetle** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="02597-128">The **Check Accessibility** page appears.</span></span>
1. <span data-ttu-id="02597-129">Tarama tamamlandıktan sonra, raporun içeriğini gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="02597-129">After the scan is completed, review the contents of the report.</span></span>
1. <span data-ttu-id="02597-130">Herhangi bir kontrol başarısız olursa, daha fazla ayrıntı görüntüleyebilmek için, bunları genişletmek amacıyla her başarısız denetim öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="02597-130">If any checks failed, select each failed check item to expand it so that you can view more details.</span></span>
1. <span data-ttu-id="02597-131">İncelemeyi tamamladıktan sonra raporu kapatmak için **erişilebilirliği kontrol et** sayfasının en altına gidip **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="02597-131">To close the report after you've finished reviewing it, scroll to the bottom of the **Check Accessibility** page, and select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="02597-132">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="02597-132">Additional resources</span></span>

[<span data-ttu-id="02597-133">Var olan site sayfasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="02597-133">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="02597-134">Yeni site sayfası ekleme</span><span class="sxs-lookup"><span data-stu-id="02597-134">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="02597-135">Sayfa düzeni seçme</span><span class="sxs-lookup"><span data-stu-id="02597-135">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="02597-136">SEO meta verilerini yönetme</span><span class="sxs-lookup"><span data-stu-id="02597-136">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="02597-137">Sayfa kaydetme, önizleme ve yayımlama</span><span class="sxs-lookup"><span data-stu-id="02597-137">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="02597-138">Ürün sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="02597-138">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="02597-139">Kategori açılış sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="02597-139">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="02597-140">URL parametrelerini temel alan dinamik e-ticaret sayfaları oluşturma</span><span class="sxs-lookup"><span data-stu-id="02597-140">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
