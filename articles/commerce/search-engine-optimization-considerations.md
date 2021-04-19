---
title: Siteniz için arama motoru optimizasyonu (SEO) konuları
description: Bu konu, gelişmede sizin sitenizin üretime yönelik arama motoru iyileştirme (SEO) konularını kapsamaktadır.
author: psimolin
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 52a10c754315bfef2a01c593f5fa5366e9054982
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791811"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a><span data-ttu-id="5772f-103">Siteniz için arama motoru optimizasyonu (SEO) konuları</span><span class="sxs-lookup"><span data-stu-id="5772f-103">Search engine optimization (SEO) considerations for your site</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5772f-104">Bu konu, gelişmede sizin sitenizin üretime yönelik arama motoru iyileştirme (SEO) konularını kapsamaktadır.</span><span class="sxs-lookup"><span data-stu-id="5772f-104">This topic covers earch engine optimization (SEO) considerations for your site from development to production.</span></span>

## <a name="a-site-that-is-under-development"></a><span data-ttu-id="5772f-105">Geliştirilme aşamasında olan bir site</span><span class="sxs-lookup"><span data-stu-id="5772f-105">A site that is under development</span></span>

<span data-ttu-id="5772f-106">Bir site gelitirme altýnda, tüm site sayfaları **NOINDEX** ve **NOFOLLOW** meta etiketlerine sahip olmalıdır, böylece arama motorları, sitenizin sayfalarını ve mağaza geliştirme sürümlerini kendi önbelleğinde dizinlerler.</span><span class="sxs-lookup"><span data-stu-id="5772f-106">While a site is under development, all site pages should have the **NOINDEX** and **NOFOLLOW** meta tags, so that search engines don't index the pages and store development versions of your site in their cache.</span></span> <span data-ttu-id="5772f-107">Bu konfigürasyonu yapmak için, site sayfası şablonuna varsayılan meta etiketler modülünü eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="5772f-107">To do this configuration, you must add the default meta tags module to the site page template.</span></span> <span data-ttu-id="5772f-108">Daha sonra, varsayılan meta etiketler özellikleri sayfa düzenleyicisinin SEO Özellikler bölümünde kullanılabilir olacak.</span><span class="sxs-lookup"><span data-stu-id="5772f-108">The default meta tags properties will then be available in the SEO properties section in the page editor.</span></span> <span data-ttu-id="5772f-109">Meta etiketleri yönetmek için bu özellikleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5772f-109">You can use these properties to manage the meta tags.</span></span>

## <a name="soft-launch-of-a-site"></a><span data-ttu-id="5772f-110">Siteyi yazılımla başlatma</span><span class="sxs-lookup"><span data-stu-id="5772f-110">Soft launch of a site</span></span>

<span data-ttu-id="5772f-111">"Yazılımla başlatma" sırasında, tam başlatma gerçekleşmeden önce sınırlı bir izleyici veya Pazar için bir Web sitesi kullanılabilir hale getirilir.</span><span class="sxs-lookup"><span data-stu-id="5772f-111">During a "soft launch," a website is made available to a limited audience or market before the full launch occurs.</span></span> <span data-ttu-id="5772f-112">Web sitenizin yazılımla başlatılması durumunda, **NOINDEX** meta etiketlerinin yerinde kalmasını düşünmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="5772f-112">If you do a soft launch of your website, you should consider leaving the **NOINDEX** meta tags in place.</span></span> <span data-ttu-id="5772f-113">Bu şekilde, yazılım başlatmanın erişmek istediğiniz sınırlı hedef kitle ile sınırlı kalmasını sağlamaya yardımcı olursunuz.</span><span class="sxs-lookup"><span data-stu-id="5772f-113">In this way, you help guarantee that the soft launch remains restricted to the limited audience that you want to reach.</span></span>

## <a name="a-site-that-is-in-production"></a><span data-ttu-id="5772f-114">Üretimdeki bir site</span><span class="sxs-lookup"><span data-stu-id="5772f-114">A site that is in production</span></span>

<span data-ttu-id="5772f-115">Bir site üretimde olduğunda, tüm site sayfalarının doğru etiketlendiğinden emin olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="5772f-115">When a site is in production, you should make sure that all site pages are correctly tagged.</span></span> <span data-ttu-id="5772f-116">Microsoft Dynamics 365 Commerce, sayfa için girilen bilgileri bu sayfadaki tüm SEO bilgilerini işlemek için kullanır.</span><span class="sxs-lookup"><span data-stu-id="5772f-116">Microsoft Dynamics 365 Commerce uses the information that is entered for a page to render all the SEO information on that page.</span></span> <span data-ttu-id="5772f-117">Aşağıdaki modüller bu işlevi sağlar: kategori sayfası Özeti, liste sayfası Özeti ve ürün sayfası Özeti.</span><span class="sxs-lookup"><span data-stu-id="5772f-117">The following modules provide this functionality: category page summary, list page summary, and product page summary.</span></span>

<span data-ttu-id="5772f-118">Arama motoru dizinini oluşturma işlemini en iyi duruma getirmek için, işleme çerçevesi hem Dynamics 365 Commerce'de hem de modüle özel bilgiler için yapılandırılan SEO özelliklerinden bilgileri kullanır.</span><span class="sxs-lookup"><span data-stu-id="5772f-118">To optimize search engine indexing, the rendering framework uses both information from the SEO properties that are configured in Dynamics 365 Commerce and module-specific information.</span></span> <span data-ttu-id="5772f-119">Üretimdeki bir site için robots.txt dosyasının tüm sitenizde dizin oluşturmaya olanak verdiğinden ve yayımlanmış site haritası belgenize bağlantılar içerdiğinden emin olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="5772f-119">For a site that is in production, you should make sure that the robots.txt file allows for indexing of your whole site, and that it contains links to your published site map document.</span></span> <span data-ttu-id="5772f-120">**Site ayarları \> Site eşlemelerinin etkin** olduğu site haritası oluşturma işlevini etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="5772f-120">You should turn on the site map generation functionality at **Site Settings \> Site maps enabled**.</span></span>

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a><span data-ttu-id="5772f-121">Dahili önizleme, sınırlı hedef kitleler ve tüm izleyiciler için sayfa SEO ayarları</span><span class="sxs-lookup"><span data-stu-id="5772f-121">Page SEO settings for internal preview, limited audiences, and all audiences</span></span>

<span data-ttu-id="5772f-122">Dynamics 365 Commerce, görsel sayfa oluşturucuda "gördüğünüz şey aldığınız şeydir" (WYSIWYG) kimlik doğrulamalı önizleme desteği sağladığından, yazarlar bilgilerin site ziyaretçileri tarafından görülebileceğini düşünmenize gerek kalmadan sayfa içeriğini hazırlayabilir.</span><span class="sxs-lookup"><span data-stu-id="5772f-122">Because Dynamics 365 Commerce supports "what you see is what you get" (WYSIWYG) authenticated previews in visual page builder, authors can prepare their page content without having to worry that the information will become visible to site visitors.</span></span> <span data-ttu-id="5772f-123">Bir sayfanın yayımlanması gerekiyorsa, ancak etkilenme sayısının sınırlı olması gerekiyorsa, bu bir **NOINDEX** meta etiketine sahip olmalıdır ve bu nedenle arama motorları tarafından dizin oluşturulmayacak.</span><span class="sxs-lookup"><span data-stu-id="5772f-123">If a page must be published, but its exposure must be limited, it should have the **NOINDEX** meta tag, so that it won't be indexed by search engines.</span></span> <span data-ttu-id="5772f-124">Daha sonra, sayfa tüm izleyiciler için hazır olduğunda, arama motoru dizininin verimliliğini en üst düzeye çıkarmak için tüm temel SEO meta verileri bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5772f-124">Then, when the page is ready for all audiences, all the basic SEO metadata should be present, to maximize the efficiency of search engine indexing.</span></span> <span data-ttu-id="5772f-125">Ek olarak, **NOLIMIT** meta etiketi kaldırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5772f-125">Additionally, the **NOLIMIT** meta tag should be removed.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5772f-126">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="5772f-126">Additional resources</span></span>

[<span data-ttu-id="5772f-127">e-Ticaret kullanıcıları ve rolleri yönetme</span><span class="sxs-lookup"><span data-stu-id="5772f-127">Manage e-Commerce users and roles</span></span>](manage-ecommerce-users-roles.md)

[<span data-ttu-id="5772f-128">Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme</span><span class="sxs-lookup"><span data-stu-id="5772f-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="5772f-129">İçerik Güvenliği İlkesini (CSP) yönetme</span><span class="sxs-lookup"><span data-stu-id="5772f-129">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]