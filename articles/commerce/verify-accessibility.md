---
title: Sayfa içeriği erişilebilirliğini doğrulama
description: Bu konuda, Microsoft Dynamics 365 Commerce sayfa içeriğinin erişilebilirliğini nasıl doğrulanacaklarını açıklanmaktadır.
author: josaw1
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 186044fc7a360f227cecffb39bad0e225245dd4d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210983"
---
# <a name="verify-page-content-accessibility"></a><span data-ttu-id="b340b-103">Sayfa içeriği erişilebilirliğini doğrulama</span><span class="sxs-lookup"><span data-stu-id="b340b-103">Verify page content accessibility</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b340b-104">Bu konuda, Microsoft Dynamics 365 Commerce sayfa içeriğinin erişilebilirliğini nasıl doğrulanacaklarını açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="b340b-104">This topic describes how to verify the accessibility of page content in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b340b-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="b340b-105">Overview</span></span>

<span data-ttu-id="b340b-106">Bir sayfayı değiştirmeyi bitirdiğinizde, içeriğin Web'deki herkes tarafından erişilebilir olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="b340b-106">When you've finished changing a page, you should make sure that the content is accessible to everyone on the web.</span></span> <span data-ttu-id="b340b-107">Commerce geliştirme araçlarında, tümleşik [Microsoft Erişilebilirlik Öngörüler](https://accessibilityinsights.io/) hizmetini kullanarak sayfa içeriğinin erişilebilirliğini kolayca doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b340b-107">In the Commerce authoring tools, you can easily verify the accessibility of page content by using the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service.</span></span> <span data-ttu-id="b340b-108">Bu hizmet, sayfanızın içeriğini en son [World Wide Web Consortium (W3C) erişilebilirlik](https://www.w3.org/standards/webdesign/accessibility) yönergelerine göre doğrular.</span><span class="sxs-lookup"><span data-stu-id="b340b-108">This service verifies your page content against the latest [World Wide Web Consortium (W3C) accessibility](https://www.w3.org/standards/webdesign/accessibility) guidelines.</span></span>

<span data-ttu-id="b340b-109">[Microsoft Accessibility Insights](https://accessibilityinsights.io/) tümleştirmesini kullanabilmeniz için önce kiracı veya site düzeyinde açık olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b340b-109">The [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration must be turned on at the tenant or site level before you can use it.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a><span data-ttu-id="b340b-110">Kiracınızda bulunan tüm sitelerden Microsoft Erişilebilirlik Insights'ı açın</span><span class="sxs-lookup"><span data-stu-id="b340b-110">Turn on Microsoft Accessibility Insights for all the sites in your tenant</span></span>

<span data-ttu-id="b340b-111">Kiracınızda bulunan tüm Commerce siteleri için [Microsoft Accessibility Insights](https://accessibilityinsights.io/) tümleştirmesini açmak üzere aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b340b-111">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for all the Commerce sites in your tenant, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="b340b-112">Kiracı ayarlarına erişmek için, Commerce'te sistem yöneticisi olarak oturum açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b340b-112">To access tenant settings, you must be signed in to Commerce as a system admin.</span></span>

1. <span data-ttu-id="b340b-113">Commerce'te sistem yöneticisi olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="b340b-113">Sign in to Commerce as a system admin.</span></span>
1. <span data-ttu-id="b340b-114">Sol gezinti bölmesinde, genişletmek için **Kiracı Ayarlarını** seçin (dişli simgesinin yanında).</span><span class="sxs-lookup"><span data-stu-id="b340b-114">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
1. <span data-ttu-id="b340b-115">**Kiracı ayarları** altında **Özellikler** dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="b340b-115">Under **Tenant Settings**, select **Features**.</span></span>
1. <span data-ttu-id="b340b-116">**Erişilebilirlik denetimi** seçeneğini **açık** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b340b-116">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a><span data-ttu-id="b340b-117">Tek bir site için Microsoft Accessibility Insights'ı aç</span><span class="sxs-lookup"><span data-stu-id="b340b-117">Turn on Microsoft Accessibility Insights for a single site</span></span>

<span data-ttu-id="b340b-118">Kiracınızda bulunan tek bir Commerce sitesi için [Microsoft Accessibility Insights](https://accessibilityinsights.io/) tümleştirmesini açmak üzere aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b340b-118">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for a single Commerce site, follow these steps.</span></span>

1. <span data-ttu-id="b340b-119">**Siteler** altında, **Fabrikam**'ı seçin (veya sitenizin adını).</span><span class="sxs-lookup"><span data-stu-id="b340b-119">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="b340b-120">Sol gezinti bölmesinde, genişletmek için **Site Ayarları** seçin.</span><span class="sxs-lookup"><span data-stu-id="b340b-120">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="b340b-121">**Site ayarları** altında **Özellikler** dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="b340b-121">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="b340b-122">**Erişilebilirlik denetimi** seçeneğini **açık** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b340b-122">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a><span data-ttu-id="b340b-123">Giriş sayfasındaki içeriğin erişilebilirliğini doğrulayın</span><span class="sxs-lookup"><span data-stu-id="b340b-123">Verify the accessibility of the content on the home page</span></span>

<span data-ttu-id="b340b-124">Ticari olarak giriş sayfanızın içeriğini taramak ve doğrulamak amacıyla tümleşik [Microsoft Accessibility Insights](https://accessibilityinsights.io/) hizmetini kullanmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b340b-124">To use the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service to scan and verify the content of your home page in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="b340b-125">**Siteler** altında, **Fabrikam**'ı seçin (veya sitenizin adını).</span><span class="sxs-lookup"><span data-stu-id="b340b-125">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="b340b-126">Soldaki gezinti bölmesinde **Sayfalar** seçin.</span><span class="sxs-lookup"><span data-stu-id="b340b-126">In the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="b340b-127">Sayfa düzenleyicisinde açmak için giriş sayfasını bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="b340b-127">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="b340b-128">Komut çubuğunda, **Erişilebilirliği kontrol et** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="b340b-128">On the command bar, select **Check accessibility**.</span></span> <span data-ttu-id="b340b-129">**Erişilebilirlik denetle** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="b340b-129">The **Check Accessibility** page appears.</span></span>
1. <span data-ttu-id="b340b-130">Tarama tamamlandıktan sonra, raporun içeriğini gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="b340b-130">After the scan is completed, review the contents of the report.</span></span>
1. <span data-ttu-id="b340b-131">Herhangi bir kontrol başarısız olursa, daha fazla ayrıntı görüntüleyebilmek için, bunları genişletmek amacıyla her başarısız denetim öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="b340b-131">If any checks failed, select each failed check item to expand it so that you can view more details.</span></span>
1. <span data-ttu-id="b340b-132">İncelemeyi tamamladıktan sonra raporu kapatmak için **erişilebilirliği kontrol et** sayfasının en altına gidip **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b340b-132">To close the report after you've finished reviewing it, scroll to the bottom of the **Check Accessibility** page, and select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b340b-133">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b340b-133">Additional resources</span></span>

[<span data-ttu-id="b340b-134">Var olan site sayfasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="b340b-134">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="b340b-135">Yeni site sayfası ekleme</span><span class="sxs-lookup"><span data-stu-id="b340b-135">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="b340b-136">Sayfa düzeni seçme</span><span class="sxs-lookup"><span data-stu-id="b340b-136">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="b340b-137">SEO meta verilerini yönetme</span><span class="sxs-lookup"><span data-stu-id="b340b-137">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="b340b-138">Sayfa kaydetme, önizleme ve yayımlama</span><span class="sxs-lookup"><span data-stu-id="b340b-138">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="b340b-139">Ürün sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="b340b-139">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="b340b-140">Kategori açılış sayfasını zenginleştirme</span><span class="sxs-lookup"><span data-stu-id="b340b-140">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="b340b-141">URL parametrelerini temel alan dinamik e-ticaret sayfaları oluşturma</span><span class="sxs-lookup"><span data-stu-id="b340b-141">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]