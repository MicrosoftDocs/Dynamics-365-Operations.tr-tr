---
title: iFrame modülü
description: Bu konu iFrame modülünü kapsamaktadır ve Microsoft Dynamics 365 Commerce'ün site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: 58446289c9a53af30d4d6d331a1a609ae0d2a0ad
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818210"
---
# <a name="iframe-module"></a><span data-ttu-id="2325e-103">iFrame modülü</span><span class="sxs-lookup"><span data-stu-id="2325e-103">Iframe module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2325e-104">Bu konu iFrame modülünü kapsamaktadır ve Microsoft Dynamics 365 Commerce'ün site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="2325e-104">This topic covers the iframe module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2325e-105">Özet</span><span class="sxs-lookup"><span data-stu-id="2325e-105">Overview</span></span>

<span data-ttu-id="2325e-106">iFrame modülü, bir sitedeki harici içeriği barındıran bir iFrame (satır içi çerçeve) sağlar.</span><span class="sxs-lookup"><span data-stu-id="2325e-106">An iframe module provides an iframe (inline frame) that hosts external content on a site.</span></span> <span data-ttu-id="2325e-107">Örneğin, herhangi bir site sayfasında bir YouTube videosu veya PDF dosyası görüntüleyiciyi barındırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2325e-107">For example, it can be used to host a YouTube video or a PDF file viewer on any site page.</span></span> 

<span data-ttu-id="2325e-108">iFrame modülü için hedef URL gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2325e-108">An iframe module requires a target URL.</span></span> <span data-ttu-id="2325e-109">Sonra, hedef sayfanın içeriğini bir HTML **iFrame** öğesinin içinde barındırır.</span><span class="sxs-lookup"><span data-stu-id="2325e-109">It then hosts the content of the target page inside an HTML **iframe** element.</span></span> <span data-ttu-id="2325e-110">Harici URL'lerin sitenin içerik güvenlik ilkesi (CSP) yönergeleri gereğince izin verilenler listesinde ("izinli liste" olarak da bilinir) olmaları gerekir.</span><span class="sxs-lookup"><span data-stu-id="2325e-110">External URLs must be on the allow list (also known as a "whitelist") per the site's content security policy (CSP) directives.</span></span> <span data-ttu-id="2325e-111">iFrame içeriği için URL'lere **frame-ancestor** yönergesi kullanılarak izin verilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="2325e-111">For iframe content, URLs should be allowed by using the **frame-ancestor** directive.</span></span> <span data-ttu-id="2325e-112">Daha fazla bilgi için bkz. [İçerik Güvenlik İlkesini (CSP) yönetme](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="2325e-112">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

> [!NOTE]
> <span data-ttu-id="2325e-113">iFrame modülü Dynamics 365 Commerce 10.0.13 sürümünde bulunur.</span><span class="sxs-lookup"><span data-stu-id="2325e-113">The iframe module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="2325e-114">Aşağıdaki resimde, site sayfalarındaki harici videoları gösteren iFrame modülleri örnekleri gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="2325e-114">The following image shows examples of iframe modules that showcase external videos on site pages.</span></span>

![Harici videoları gösteren iFrame modülleri örneği](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a><span data-ttu-id="2325e-116">iFrame modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="2325e-116">Iframe module properties</span></span>

| <span data-ttu-id="2325e-117">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="2325e-117">Property name</span></span>             | <span data-ttu-id="2325e-118">Değer</span><span class="sxs-lookup"><span data-stu-id="2325e-118">Value</span></span>                 | <span data-ttu-id="2325e-119">Tanım</span><span class="sxs-lookup"><span data-stu-id="2325e-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="2325e-120">Başlık</span><span class="sxs-lookup"><span data-stu-id="2325e-120">Heading</span></span> | <span data-ttu-id="2325e-121">Metin</span><span class="sxs-lookup"><span data-stu-id="2325e-121">Text</span></span> | <span data-ttu-id="2325e-122">Modülün başlığı.</span><span class="sxs-lookup"><span data-stu-id="2325e-122">The heading for the module.</span></span> |
| <span data-ttu-id="2325e-123">Hedef URL</span><span class="sxs-lookup"><span data-stu-id="2325e-123">Target URL</span></span> | <span data-ttu-id="2325e-124">URL</span><span class="sxs-lookup"><span data-stu-id="2325e-124">URL</span></span> | <span data-ttu-id="2325e-125">Modülde barındırılan URL.</span><span class="sxs-lookup"><span data-stu-id="2325e-125">The URL that is hosted in the module.</span></span> |
| <span data-ttu-id="2325e-126">Yükseklik</span><span class="sxs-lookup"><span data-stu-id="2325e-126">Height</span></span> | <span data-ttu-id="2325e-127">Sayı veya yüzde</span><span class="sxs-lookup"><span data-stu-id="2325e-127">Number or percentage</span></span> | <span data-ttu-id="2325e-128">Modülün piksel cinsinden veya yüzde olarak yüksekliği.</span><span class="sxs-lookup"><span data-stu-id="2325e-128">The height of the module, in pixels or as a percentage.</span></span> <span data-ttu-id="2325e-129">Örneğin, **100** değeri piksel sayısı olarak değerlendirilir ve **%100** değeri yüzde olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="2325e-129">For example, the value **100** will be treated as a number of pixels, and the value **100%** will be treated as a percentage.</span></span> |
| <span data-ttu-id="2325e-130">Aria etiketi</span><span class="sxs-lookup"><span data-stu-id="2325e-130">Aria label</span></span> | <span data-ttu-id="2325e-131">Metin</span><span class="sxs-lookup"><span data-stu-id="2325e-131">Text</span></span> | <span data-ttu-id="2325e-132">Erişilebilirlik amacıyla, bir Erişilebilir Zengin İnternet Uygulamaları (ARIA) etiketi tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="2325e-132">An Accessible Rich Internet Applications (ARIA) label can be defined for accessibility purposes.</span></span> |

## <a name="add-an-iframe-module-to-a-page"></a><span data-ttu-id="2325e-133">Sayfaya iFrame modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="2325e-133">Add an iframe module to a page</span></span>

<span data-ttu-id="2325e-134">Bir sayfaya harici bir video göstermek üzere bir iFrame modülü eklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="2325e-134">To add an iframe module to a page to show an external video, follow these steps.</span></span>

1. <span data-ttu-id="2325e-135">Bir yeni şablonu oluşturmak için **Şablonlar**'a gidin ve **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2325e-135">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="2325e-136">**Yeni Şablon** iletişim kutusunda **Şablon adı** altında, **Pazarlama şablonu**'nu girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2325e-136">In the **New Template** dialog box, under **Template name**, enter **Marketing template**, and then select **OK**.</span></span>
1. <span data-ttu-id="2325e-137">**Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2325e-137">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="2325e-138">**Sayfalar**'a gidin ve yeni sayfa oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2325e-138">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="2325e-139">**Şablon seçin** iletişim kutusunda **Pazarlama şablonu** şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="2325e-139">In the **Choose a template** dialog box, select the **Marketing template** template.</span></span> <span data-ttu-id="2325e-140">**Sayfa adı** altında **Pazarlama sayfası** girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2325e-140">Under **Page name**, enter **Marketing page**, and then select **OK**.</span></span>
1. <span data-ttu-id="2325e-141">Yeni sayfada **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2325e-141">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2325e-142">**Modül Ekle** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2325e-142">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2325e-143">Modülün özellikler bölmesinde, **Genişlik** değerini **Dolgu Kapsayıcısı** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2325e-143">In the module's properties pane, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="2325e-144">**Konteyner** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2325e-144">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2325e-145">**Modül Ekle** iletişim kutusunda **iFrame** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2325e-145">In the **Add Module** dialog box, select the **iframe** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2325e-146">Modülün özellikler bölmesinde, **Hedef URL** değerini bir videonun harici URL'si olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2325e-146">In the module's properties pane, set the **Target URL** value to an external URL for a video.</span></span>
1. <span data-ttu-id="2325e-147">İhtiyacınıza göre, **Başlık** ve **Yükseklik** gibi diğer özellikleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2325e-147">Set other properties, such as **Heading** and **Height**, as you require.</span></span>
1. <span data-ttu-id="2325e-148">**Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2325e-148">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="2325e-149">Sitenizdeki pazarlama sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="2325e-149">Go to the marketing page on your site.</span></span> <span data-ttu-id="2325e-150">Videonun iFrame modülünde işlendiğini görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="2325e-150">You should see that the video is rendered in the iframe module.</span></span>
 
## <a name="additional-resources"></a><span data-ttu-id="2325e-151">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="2325e-151">Additional resources</span></span>

[<span data-ttu-id="2325e-152">Modül kitaplığına genel bakış</span><span class="sxs-lookup"><span data-stu-id="2325e-152">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2325e-153">İçerik Güvenliği İlkesini (CSP) yönetme</span><span class="sxs-lookup"><span data-stu-id="2325e-153">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
