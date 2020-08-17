---
title: iFrame modülü
description: Bu konu iFrame modülünü kapsamaktadır ve Microsoft Dynamics 365 Commerce'ün site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 07/31/2020
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
ms.openlocfilehash: 0616a772a416a7c9d9756a840c93b8601c08c3d0
ms.sourcegitcommit: 078befcd7f3531073ab2c08b365bcf132d6477b0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/31/2020
ms.locfileid: "3647071"
---
# <a name="iframe-module"></a><span data-ttu-id="c2966-103">iFrame modülü</span><span class="sxs-lookup"><span data-stu-id="c2966-103">Iframe module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="c2966-104">Bu konu iFrame modülünü kapsamaktadır ve Microsoft Dynamics 365 Commerce'ün site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="c2966-104">This topic covers the iframe module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c2966-105">Özet</span><span class="sxs-lookup"><span data-stu-id="c2966-105">Overview</span></span>

<span data-ttu-id="c2966-106">iFrame modülü, bir sitedeki harici içeriği barındıran bir iFrame (satır içi çerçeve) sağlar.</span><span class="sxs-lookup"><span data-stu-id="c2966-106">An iframe module provides an iframe (inline frame) that hosts external content on a site.</span></span> <span data-ttu-id="c2966-107">Örneğin, herhangi bir site sayfasında bir YouTube videosu veya PDF dosyası görüntüleyiciyi barındırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c2966-107">For example, it can be used to host a YouTube video or a PDF file viewer on any site page.</span></span> 

<span data-ttu-id="c2966-108">iFrame modülü için hedef URL gereklidir.</span><span class="sxs-lookup"><span data-stu-id="c2966-108">An iframe module requires a target URL.</span></span> <span data-ttu-id="c2966-109">Sonra, hedef sayfanın içeriğini bir HTML **iFrame** öğesinin içinde barındırır.</span><span class="sxs-lookup"><span data-stu-id="c2966-109">It then hosts the content of the target page inside an HTML **iframe** element.</span></span> <span data-ttu-id="c2966-110">Harici URL'lerin sitenin içerik güvenlik ilkesi (CSP) yönergeleri gereğince izin verilenler listesinde ("izinli liste" olarak da bilinir) olmaları gerekir.</span><span class="sxs-lookup"><span data-stu-id="c2966-110">External URLs must be on the allow list (also known as a "whitelist") per the site's content security policy (CSP) directives.</span></span> <span data-ttu-id="c2966-111">iFrame içeriği için URL'lere **frame-ancestor** yönergesi kullanılarak izin verilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="c2966-111">For iframe content, URLs should be allowed by using the **frame-ancestor** directive.</span></span> <span data-ttu-id="c2966-112">Daha fazla bilgi için bkz. [İçerik Güvenlik İlkesini (CSP) yönetme](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="c2966-112">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

<span data-ttu-id="c2966-113">Aşağıdaki resimde, site sayfalarındaki harici videoları gösteren iFrame modülleri örnekleri gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="c2966-113">The following image shows examples of iframe modules that showcase external videos on site pages.</span></span>

![Harici videoları gösteren iFrame modülleri örneği](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a><span data-ttu-id="c2966-115">iFrame modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="c2966-115">Iframe module properties</span></span>

| <span data-ttu-id="c2966-116">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="c2966-116">Property name</span></span>             | <span data-ttu-id="c2966-117">Değer</span><span class="sxs-lookup"><span data-stu-id="c2966-117">Value</span></span>                 | <span data-ttu-id="c2966-118">Tanım</span><span class="sxs-lookup"><span data-stu-id="c2966-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="c2966-119">Başlık</span><span class="sxs-lookup"><span data-stu-id="c2966-119">Heading</span></span> | <span data-ttu-id="c2966-120">Metin</span><span class="sxs-lookup"><span data-stu-id="c2966-120">Text</span></span> | <span data-ttu-id="c2966-121">Modülün başlığı.</span><span class="sxs-lookup"><span data-stu-id="c2966-121">The heading for the module.</span></span> |
| <span data-ttu-id="c2966-122">Hedef URL</span><span class="sxs-lookup"><span data-stu-id="c2966-122">Target URL</span></span> | <span data-ttu-id="c2966-123">URL</span><span class="sxs-lookup"><span data-stu-id="c2966-123">URL</span></span> | <span data-ttu-id="c2966-124">Modülde barındırılan URL.</span><span class="sxs-lookup"><span data-stu-id="c2966-124">The URL that is hosted in the module.</span></span> |
| <span data-ttu-id="c2966-125">Yükseklik</span><span class="sxs-lookup"><span data-stu-id="c2966-125">Height</span></span> | <span data-ttu-id="c2966-126">Sayı veya yüzde</span><span class="sxs-lookup"><span data-stu-id="c2966-126">Number or percentage</span></span> | <span data-ttu-id="c2966-127">Modülün piksel cinsinden veya yüzde olarak yüksekliği.</span><span class="sxs-lookup"><span data-stu-id="c2966-127">The height of the module, in pixels or as a percentage.</span></span> <span data-ttu-id="c2966-128">Örneğin, **100** değeri piksel sayısı olarak değerlendirilir ve **%100** değeri yüzde olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="c2966-128">For example, the value **100** will be treated as a number of pixels, and the value **100%** will be treated as a percentage.</span></span> |
| <span data-ttu-id="c2966-129">Aria etiketi</span><span class="sxs-lookup"><span data-stu-id="c2966-129">Aria label</span></span> | <span data-ttu-id="c2966-130">Metin</span><span class="sxs-lookup"><span data-stu-id="c2966-130">Text</span></span> | <span data-ttu-id="c2966-131">Erişilebilirlik amacıyla, bir Erişilebilir Zengin İnternet Uygulamaları (ARIA) etiketi tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="c2966-131">An Accessible Rich Internet Applications (ARIA) label can be defined for accessibility purposes.</span></span> |

## <a name="add-an-iframe-module-to-a-page"></a><span data-ttu-id="c2966-132">Sayfaya iFrame modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="c2966-132">Add an iframe module to a page</span></span>

<span data-ttu-id="c2966-133">Bir sayfaya harici bir video göstermek üzere bir iFrame modülü eklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c2966-133">To add an iframe module to a page to show an external video, follow these steps.</span></span>

1. <span data-ttu-id="c2966-134">Bir yeni şablonu oluşturmak için **Şablonlar**'a gidin ve **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c2966-134">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="c2966-135">**Yeni Şablon** iletişim kutusunda **Şablon adı** altında, **Pazarlama şablonu**'nu girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c2966-135">In the **New Template** dialog box, under **Template name**, enter **Marketing template**, and then select **OK**.</span></span>
1. <span data-ttu-id="c2966-136">**Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="c2966-136">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="c2966-137">**Sayfalar**'a gidin ve yeni sayfa oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c2966-137">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="c2966-138">**Şablon seçin** iletişim kutusunda **Pazarlama şablonu** şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="c2966-138">In the **Choose a template** dialog box, select the **Marketing template** template.</span></span> <span data-ttu-id="c2966-139">**Sayfa adı** altında **Pazarlama sayfası** girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c2966-139">Under **Page name**, enter **Marketing page**, and then select **OK**.</span></span>
1. <span data-ttu-id="c2966-140">Yeni sayfada **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c2966-140">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c2966-141">**Modül Ekle** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c2966-141">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c2966-142">Modülün özellikler bölmesinde, **Genişlik** değerini **Dolgu Kapsayıcısı** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c2966-142">In the module's properties pane, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="c2966-143">**Konteyner** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c2966-143">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c2966-144">**Modül Ekle** iletişim kutusunda **iFrame** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c2966-144">In the **Add Module** dialog box, select the **iframe** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c2966-145">Modülün özellikler bölmesinde, **Hedef URL** değerini bir videonun harici URL'si olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c2966-145">In the module's properties pane, set the **Target URL** value to an external URL for a video.</span></span>
1. <span data-ttu-id="c2966-146">İhtiyacınıza göre, **Başlık** ve **Yükseklik** gibi diğer özellikleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c2966-146">Set other properties, such as **Heading** and **Height**, as you require.</span></span>
1. <span data-ttu-id="c2966-147">**Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="c2966-147">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="c2966-148">Sitenizdeki pazarlama sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="c2966-148">Go to the marketing page on your site.</span></span> <span data-ttu-id="c2966-149">Videonun iFrame modülünde işlendiğini görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="c2966-149">You should see that the video is rendered in the iframe module.</span></span>
 
## <a name="additional-resources"></a><span data-ttu-id="c2966-150">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="c2966-150">Additional resources</span></span>

[<span data-ttu-id="c2966-151">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="c2966-151">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c2966-152">İçerik Güvenliği İlkesini (CSP) yönetme</span><span class="sxs-lookup"><span data-stu-id="c2966-152">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
