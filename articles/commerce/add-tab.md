---
title: Sekme modülü
description: Bu konu sekme modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8375c33bd6ffd3004cfc9d7b686d9a0edc77cdef
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209239"
---
# <a name="tab-module"></a><span data-ttu-id="2b4c3-103">Sekme modülü</span><span class="sxs-lookup"><span data-stu-id="2b4c3-103">Tab module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2b4c3-104">Bu konu sekme modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-104">This topic covers tab modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="2b4c3-105">Sekme modülleri, sekmelerdeki bir site sayfasındaki bilgileri düzenlemek için kullanılan kapsayıcı benzeri modüllerdir.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-105">Tab modules are container-like modules that are used to organize the information on a site page on tabs.</span></span> <span data-ttu-id="2b4c3-106">Bunlar, bilgilerin sekmelerde sunulması gereken her sayfada kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-106">They can be used on any page where information must be presented on tabs.</span></span>

<span data-ttu-id="2b4c3-107">Her sekme modülü içinde bir veya daha fazla sekme madde modülü eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-107">In every tab module, one or more tab item modules can be added.</span></span> <span data-ttu-id="2b4c3-108">Her sekme öğesi modülü tek bir sekmeyi temsil eder. Her sekme madde modülünde, bir veya daha fazla modül eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-108">Each tab item module represents a single tab. In each tab item module, one or more modules can be added.</span></span> <span data-ttu-id="2b4c3-109">Bir sekme madde modülüne eklenebilecek modül türlerinde bir sınırlama yoktur.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-109">There are no restrictions on the types of modules that can be added to a tab item module.</span></span>

<span data-ttu-id="2b4c3-110">Aşağıdaki resimde site sayfasında kullanılan bir sekme modülü örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-110">The following image shows an example of a tab module on a site page.</span></span> <span data-ttu-id="2b4c3-111">Bu örnekte, **Sevkiyat** sekmesi seçili.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-111">In this example, the **Shipping** tab selected.</span></span>

![Sekme modülü örneği](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a><span data-ttu-id="2b4c3-113">Sekme modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="2b4c3-113">Tab module properties</span></span>

| <span data-ttu-id="2b4c3-114">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="2b4c3-114">Property name</span></span> | <span data-ttu-id="2b4c3-115">Değerler</span><span class="sxs-lookup"><span data-stu-id="2b4c3-115">Values</span></span> | <span data-ttu-id="2b4c3-116">Tanım</span><span class="sxs-lookup"><span data-stu-id="2b4c3-116">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="2b4c3-117">Başlık</span><span class="sxs-lookup"><span data-stu-id="2b4c3-117">Heading</span></span> | <span data-ttu-id="2b4c3-118">Metin</span><span class="sxs-lookup"><span data-stu-id="2b4c3-118">Text</span></span> | <span data-ttu-id="2b4c3-119">Bu özellik sekme modülü için isteğe bağlı bir metin başlığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-119">This property specifies an optional text heading for the tab module.</span></span> |
| <span data-ttu-id="2b4c3-120">Etkin sekme dizini</span><span class="sxs-lookup"><span data-stu-id="2b4c3-120">Active Tab Index</span></span> | <span data-ttu-id="2b4c3-121">Sayı</span><span class="sxs-lookup"><span data-stu-id="2b4c3-121">Number</span></span> | <span data-ttu-id="2b4c3-122">Bu özellik, sayfa yüklendiğinde varsayılan olarak etkin olması gereken sekmeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-122">This property specifies the tab that should be active by default when a page is loaded.</span></span> <span data-ttu-id="2b4c3-123">Herhangi bir değer sağlanmazsa, ilk sekme öğesi varsayılan olarak etkindir.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-123">If no value is provided, the first tab item is active by default.</span></span> |

## <a name="tab-item-module-properties"></a><span data-ttu-id="2b4c3-124">Sekme madde modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="2b4c3-124">Tab item module properties</span></span>

| <span data-ttu-id="2b4c3-125">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="2b4c3-125">Property name</span></span> | <span data-ttu-id="2b4c3-126">Değerler</span><span class="sxs-lookup"><span data-stu-id="2b4c3-126">Values</span></span> | <span data-ttu-id="2b4c3-127">Tanım</span><span class="sxs-lookup"><span data-stu-id="2b4c3-127">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="2b4c3-128">Ünvan</span><span class="sxs-lookup"><span data-stu-id="2b4c3-128">Title</span></span> | <span data-ttu-id="2b4c3-129">Metin</span><span class="sxs-lookup"><span data-stu-id="2b4c3-129">Text</span></span> | <span data-ttu-id="2b4c3-130">Bu özellik sekme madde modülü için bir başlık metini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-130">This property specifies the title text for the tab item module.</span></span> |

## <a name="add-a-tab-module-to-a-page"></a><span data-ttu-id="2b4c3-131">Sayfaya sekme modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="2b4c3-131">Add a tab module to a page</span></span>

<span data-ttu-id="2b4c3-132">Bir sayfaya sekme modülü eklemek ve özellikleri ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-132">To add a tab module to a page and set the properties, follow these steps.</span></span>

1. <span data-ttu-id="2b4c3-133">**Mağaza politikaları sayfası** adlı yeni bir sayfa oluşturmak için sayfalara gidin ve Fabrikam pazarlama şablonunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-133">Use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store policies page**.</span></span>
1. <span data-ttu-id="2b4c3-134">**Varsayılan sayfada** **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-134">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2b4c3-135">**Modül Ekle** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-135">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2b4c3-136">**Konteyner** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-136">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2b4c3-137">**Modül Ekle** iletişim kutusunda **sekme** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-137">In the **Add Module** dialog box, select the **Tab** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2b4c3-138">Sekme modülünün Özellik bölmesinde, kurşun kalem simgesinin yanındaki **Başlık**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-138">In the property pane of the tab module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="2b4c3-139">**Başlık** iletişim kutusunda, **başlık metni** altında başlık metni girin (örneğin, **ilkeler**).</span><span class="sxs-lookup"><span data-stu-id="2b4c3-139">In the **Heading** dialog box, under **Heading Text**, enter heading text (for example, **Policies**).</span></span> <span data-ttu-id="2b4c3-140">Daha sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-140">Then select **OK**.</span></span>
1. <span data-ttu-id="2b4c3-141">**Sekme** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-141">In the **Tab** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2b4c3-142">**Modül Ekle** iletişim kutusunda **sekme madde** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-142">In the **Add Module** dialog box, select the **Tab item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2b4c3-143">Sekme madde modülünün Özellik bölmesinde, **başlık** altında başlık metnini girin (örneğin, **Teslimat**).</span><span class="sxs-lookup"><span data-stu-id="2b4c3-143">In the property pane of the tab item module, under **Title**, enter title text (for example, **Delivery**).</span></span>
1. <span data-ttu-id="2b4c3-144">**Sekme madde** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-144">In the **Tab item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2b4c3-145">**Modül Ekle** iletişim kutusunda **Metin bloku** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-145">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2b4c3-146">Metin bloku modülünün özellik panosunda, **Zengin metin** altına mtein paragrafı girin.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-146">In the property pane of the text block module, under **Rich text**, enter a paragraph of text.</span></span>
1. <span data-ttu-id="2b4c3-147">**Sekme** yuvasında, başlıkları olan birkaç sekme öğesi modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-147">In the **Tab** slot, add a few more tab item modules that have titles.</span></span> <span data-ttu-id="2b4c3-148">Her bir sekme madde modülünde içeriği olan bir metin bloğu modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-148">In each tab item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="2b4c3-149">**Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-149">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="2b4c3-150">Sayfa, sekme öğesi modülleri içeren bir sekme modülünü gösterir eklediğiniz içeriğe sahip.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-150">The page will show a tab module that contains tab item modules have the content that you added.</span></span>
1. <span data-ttu-id="2b4c3-151">Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b4c3-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2b4c3-152">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="2b4c3-152">Additional resources</span></span>

[<span data-ttu-id="2b4c3-153">Modül kitaplığına genel bakış</span><span class="sxs-lookup"><span data-stu-id="2b4c3-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2b4c3-154">Kapsayıcı modülü</span><span class="sxs-lookup"><span data-stu-id="2b4c3-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="2b4c3-155">Akordeon modülü</span><span class="sxs-lookup"><span data-stu-id="2b4c3-155">Accordion module</span></span>](add-accordion.md)

[<span data-ttu-id="2b4c3-156">Metin bloğu modülü</span><span class="sxs-lookup"><span data-stu-id="2b4c3-156">Text block module</span></span>](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]