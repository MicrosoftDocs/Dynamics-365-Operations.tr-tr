---
title: Sekme modülü
description: Bu konu sekme modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 06/01/2020
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 60af9b74f7e647e83229e352a03c09d63d0c7902
ms.sourcegitcommit: 2683aacb426bfb3b541637edf1f8ec2d6cb5a745
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/01/2020
ms.locfileid: "3417381"
---
# <a name="tab-module"></a><span data-ttu-id="0c1d0-103">Sekme modülü</span><span class="sxs-lookup"><span data-stu-id="0c1d0-103">Tab module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="0c1d0-104">Bu konu sekme modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="0c1d0-104">This topic covers tab modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0c1d0-105">Özet</span><span class="sxs-lookup"><span data-stu-id="0c1d0-105">Overview</span></span>

<span data-ttu-id="0c1d0-106">Sekme modülleri, sekmelerdeki bir site sayfasındaki bilgileri düzenlemek için kullanılan kapsayıcı benzeri modüllerdir.</span><span class="sxs-lookup"><span data-stu-id="0c1d0-106">Tab modules are container-like modules that are used to organize the information on a site page on tabs.</span></span> <span data-ttu-id="0c1d0-107">Bunlar, bilgilerin sekmelerde sunulması gereken her sayfada kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0c1d0-107">They can be used on any page where information must be presented on tabs.</span></span>

<span data-ttu-id="0c1d0-108">Her sekme modülü içinde bir veya daha fazla sekme madde modülü eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="0c1d0-108">In every tab module, one or more tab item modules can be added.</span></span> <span data-ttu-id="0c1d0-109">Her sekme öğesi modülü tek bir sekmeyi temsil eder. Her sekme madde modülünde, bir veya daha fazla modül eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="0c1d0-109">Each tab item module represents a single tab. In each tab item module, one or more modules can be added.</span></span> <span data-ttu-id="0c1d0-110">Bir sekme madde modülüne eklenebilecek modül türlerinde bir sınırlama yoktur.</span><span class="sxs-lookup"><span data-stu-id="0c1d0-110">There are no restrictions on the types of modules that can be added to a tab item module.</span></span>

<span data-ttu-id="0c1d0-111">Aşağıdaki resimde site sayfasında kullanılan bir sekme modülü örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="0c1d0-111">The following image shows an example of a tab module on a site page.</span></span> <span data-ttu-id="0c1d0-112">Bu örnekte, **Sevkiyat** sekmesi seçili.</span><span class="sxs-lookup"><span data-stu-id="0c1d0-112">In this example, the **Shipping** tab selected.</span></span>

![Sekme modülü örneği](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a><span data-ttu-id="0c1d0-114">Sekme modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="0c1d0-114">Tab module properties</span></span>

| <span data-ttu-id="0c1d0-115">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="0c1d0-115">Property name</span></span> | <span data-ttu-id="0c1d0-116">Değerler</span><span class="sxs-lookup"><span data-stu-id="0c1d0-116">Values</span></span> | <span data-ttu-id="0c1d0-117">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c1d0-117">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="0c1d0-118">Başlık</span><span class="sxs-lookup"><span data-stu-id="0c1d0-118">Heading</span></span> | <span data-ttu-id="0c1d0-119">Metin</span><span class="sxs-lookup"><span data-stu-id="0c1d0-119">Text</span></span> | <span data-ttu-id="0c1d0-120">Bu özellik sekme modülü için isteğe bağlı bir metin başlığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c1d0-120">This property specifies an optional text heading for the tab module.</span></span> |
| <span data-ttu-id="0c1d0-121">Etkin sekme dizini</span><span class="sxs-lookup"><span data-stu-id="0c1d0-121">Active Tab Index</span></span> | <span data-ttu-id="0c1d0-122">Sayı</span><span class="sxs-lookup"><span data-stu-id="0c1d0-122">Number</span></span> | <span data-ttu-id="0c1d0-123">Bu özellik, sayfa yüklendiğinde varsayılan olarak etkin olması gereken sekmeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c1d0-123">This property specifies the tab that should be active by default when a page is loaded.</span></span> <span data-ttu-id="0c1d0-124">Herhangi bir değer sağlanmazsa, ilk sekme öğesi varsayılan olarak etkindir.</span><span class="sxs-lookup"><span data-stu-id="0c1d0-124">If no value is provided, the first tab item is active by default.</span></span> |

## <a name="tab-item-module-properties"></a><span data-ttu-id="0c1d0-125">Sekme madde modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="0c1d0-125">Tab item module properties</span></span>

| <span data-ttu-id="0c1d0-126">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="0c1d0-126">Property name</span></span> | <span data-ttu-id="0c1d0-127">Değerler</span><span class="sxs-lookup"><span data-stu-id="0c1d0-127">Values</span></span> | <span data-ttu-id="0c1d0-128">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c1d0-128">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="0c1d0-129">Ünvan</span><span class="sxs-lookup"><span data-stu-id="0c1d0-129">Title</span></span> | <span data-ttu-id="0c1d0-130">Metin</span><span class="sxs-lookup"><span data-stu-id="0c1d0-130">Text</span></span> | <span data-ttu-id="0c1d0-131">Bu özellik sekme madde modülü için bir başlık metini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c1d0-131">This property specifies the title text for the tab item module.</span></span> |

## <a name="add-a-tab-module-to-a-page"></a><span data-ttu-id="0c1d0-132">Sayfaya sekme modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="0c1d0-132">Add a tab module to a page</span></span>

<span data-ttu-id="0c1d0-133">Bir sayfaya sekme modülü eklemek ve özellikleri ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="0c1d0-133">To add a tab module to a page and set the properties, follow these steps.</span></span>

1. <span data-ttu-id="0c1d0-134">**Mağaza politikaları sayfası** adlı yeni bir sayfa oluşturmak için sayfalara gidin ve Fabrikam pazarlama şablonunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="0c1d0-134">Use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store policies page**.</span></span>
1. <span data-ttu-id="0c1d0-135">**Varsayılan sayfada** **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0c1d0-135">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0c1d0-136">**Modül Ekle** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0c1d0-136">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0c1d0-137">**Konteyner** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0c1d0-137">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0c1d0-138">**Modül Ekle** iletişim kutusunda **sekme** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0c1d0-138">In the **Add Module** dialog box, select the **Tab** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0c1d0-139">Sekme modülünün Özellik bölmesinde, kurşun kalem simgesinin yanındaki **Başlık**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0c1d0-139">In the property pane of the tab module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="0c1d0-140">**Başlık** iletişim kutusunda, **başlık metni** altında başlık metni girin (örneğin, **ilkeler**).</span><span class="sxs-lookup"><span data-stu-id="0c1d0-140">In the **Heading** dialog box, under **Heading Text**, enter heading text (for example, **Policies**).</span></span> <span data-ttu-id="0c1d0-141">Daha sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0c1d0-141">Then select **OK**.</span></span>
1. <span data-ttu-id="0c1d0-142">**Sekme** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0c1d0-142">In the **Tab** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0c1d0-143">**Modül Ekle** iletişim kutusunda **sekme madde** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0c1d0-143">In the **Add Module** dialog box, select the **Tab item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0c1d0-144">Sekme madde modülünün Özellik bölmesinde, **başlık** altında başlık metnini girin (örneğin, **Teslimat**).</span><span class="sxs-lookup"><span data-stu-id="0c1d0-144">In the property pane of the tab item module, under **Title**, enter title text (for example, **Delivery**).</span></span>
1. <span data-ttu-id="0c1d0-145">**Sekme madde** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0c1d0-145">In the **Tab item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0c1d0-146">**Modül Ekle** iletişim kutusunda **Metin bloku** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0c1d0-146">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0c1d0-147">Metin bloku modülünün özellik panosunda, **Zengin metin** altına mtein paragrafı girin.</span><span class="sxs-lookup"><span data-stu-id="0c1d0-147">In the property pane of the text block module, under **Rich text**, enter a paragraph of text.</span></span>
1. <span data-ttu-id="0c1d0-148">**Sekme** yuvasında, başlıkları olan birkaç sekme öğesi modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="0c1d0-148">In the **Tab** slot, add a few more tab item modules that have titles.</span></span> <span data-ttu-id="0c1d0-149">Her bir sekme madde modülünde içeriği olan bir metin bloğu modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="0c1d0-149">In each tab item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="0c1d0-150">**Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0c1d0-150">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="0c1d0-151">Sayfa, sekme öğesi modülleri içeren bir sekme modülünü gösterir eklediğiniz içeriğe sahip.</span><span class="sxs-lookup"><span data-stu-id="0c1d0-151">The page will show a tab module that contains tab item modules have the content that you added.</span></span>
1. <span data-ttu-id="0c1d0-152">Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="0c1d0-152">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0c1d0-153">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="0c1d0-153">Additional resources</span></span>

[<span data-ttu-id="0c1d0-154">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="0c1d0-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="0c1d0-155">Konteyner modülü</span><span class="sxs-lookup"><span data-stu-id="0c1d0-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="0c1d0-156">Akordiyon modülü</span><span class="sxs-lookup"><span data-stu-id="0c1d0-156">Accordion module</span></span>](add-accordion.md)

[<span data-ttu-id="0c1d0-157">Metin bloğu modülü</span><span class="sxs-lookup"><span data-stu-id="0c1d0-157">Text block module</span></span>](add-content-rich-block.md)
