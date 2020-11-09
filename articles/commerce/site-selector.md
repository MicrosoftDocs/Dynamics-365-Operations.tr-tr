---
title: Site seçicisi modülü
description: Bu konu site seçici modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'in site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
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
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: bd54695f54b501631f916328c05bfd47e538d50d
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055842"
---
# <a name="site-selector-module"></a><span data-ttu-id="036b5-103">Site seçicisi modülü</span><span class="sxs-lookup"><span data-stu-id="036b5-103">Site selector module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="036b5-104">Bu konu site seçici modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'in site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="036b5-104">This topic covers the site selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="036b5-105">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="036b5-105">Overview</span></span>

<span data-ttu-id="036b5-106">Bir işletme, pazarlar, bölgeler ve konumlarda farklı sitelere sahip olduğunda, site kullanıcıları siteler arasında geçiş yapmak ve tercih edilen alışveriş sitesini seçmek için kolay bir yola gereksinim duyar.</span><span class="sxs-lookup"><span data-stu-id="036b5-106">When a business has different sites across markets, regions, and locales, site users need an easy way to switch between sites and select their preferred shopping site.</span></span> <span data-ttu-id="036b5-107">Bu senaryoya uyum sağlamak için, site seçici modülü kullanıcıların birden çok siteye göz atmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="036b5-107">To accommodate this scenario, the site selector module lets users browse across multiple sites.</span></span>

<span data-ttu-id="036b5-108">Site seçici modülü site kullanıcılarının göz atabileceği siteler listesi (pazarlar, bölgeler veya konumlar) ile konfigüre edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="036b5-108">The site selector module must be configured with the list of sites (markets, regions, or locales) that site users can browse.</span></span>

> [!NOTE]
> <span data-ttu-id="036b5-109">Site seçici modülü Dynamics 365 Commerce 10.0.14 sürümünde bulunur.</span><span class="sxs-lookup"><span data-stu-id="036b5-109">The site selector module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="036b5-110">Aşağıdaki çizimde site sayfası üstbilgisinde tanıtılan bir site seçici modülü örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="036b5-110">The following illustration shows an example of a site selector module that is featured in the header of a site page.</span></span>

![Site sayfası üst bilgisindeki bir site seçici modülü örneği](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a><span data-ttu-id="036b5-112">Site seçicisi modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="036b5-112">Site selector module properties</span></span>

| <span data-ttu-id="036b5-113">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="036b5-113">Property name</span></span> | <span data-ttu-id="036b5-114">Değer</span><span class="sxs-lookup"><span data-stu-id="036b5-114">Value</span></span>                 | <span data-ttu-id="036b5-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="036b5-115">Description</span></span> |
|---------------|-----------------------|-------------|
| <span data-ttu-id="036b5-116">Başlık</span><span class="sxs-lookup"><span data-stu-id="036b5-116">Heading</span></span>       | <span data-ttu-id="036b5-117">Metin</span><span class="sxs-lookup"><span data-stu-id="036b5-117">Text</span></span>                  | <span data-ttu-id="036b5-118">Modülün başlığı.</span><span class="sxs-lookup"><span data-stu-id="036b5-118">The heading for the module.</span></span> |
| <span data-ttu-id="036b5-119">Site seçenekleri</span><span class="sxs-lookup"><span data-stu-id="036b5-119">Site options</span></span>  | <span data-ttu-id="036b5-120">Ad, resim, URL</span><span class="sxs-lookup"><span data-stu-id="036b5-120">Name, Image, URL</span></span>      | <span data-ttu-id="036b5-121">Bu özellik, bir ad, sitenin giriş sayfası bağlantısı ve modüldeki her site için gösterilecek isteğe bağlı bir resim belirtir.</span><span class="sxs-lookup"><span data-stu-id="036b5-121">This property specifies a name, a link to the site's home page, and an optional image to show for each site that is included in the module.</span></span> <span data-ttu-id="036b5-122">Resim bir bayrak veya bir pazar, bölge veya konumun herhangi bir temsili olabilir.</span><span class="sxs-lookup"><span data-stu-id="036b5-122">The image can be a flag, or some representation of a market, region, or locale.</span></span> |

## <a name="add-a-site-selector-module-to-a-page"></a><span data-ttu-id="036b5-123">Bir sayfaya site seçici modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="036b5-123">Add a site selector module to a page</span></span>

<span data-ttu-id="036b5-124">Site seçici modülü, site seçici yuvasının altındaki [üst bilgi modülüne](author-header-module.md) eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="036b5-124">The site selector module can be added to the [Header module](author-header-module.md) under the site selector slot.</span></span> <span data-ttu-id="036b5-125">Eklendikten sonra, modül üst bilgisini ve site seçeneklerini tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="036b5-125">After it's added, you can define the module heading and site options.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="036b5-126">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="036b5-126">Additional resources</span></span>

[<span data-ttu-id="036b5-127">Modül kitaplığına genel bakış</span><span class="sxs-lookup"><span data-stu-id="036b5-127">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="036b5-128">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="036b5-128">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="036b5-129">İçerik haritası modülü</span><span class="sxs-lookup"><span data-stu-id="036b5-129">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="036b5-130">Gezinti menüsü modülü</span><span class="sxs-lookup"><span data-stu-id="036b5-130">Navigation menu module</span></span>](nav-menu-module.md)
