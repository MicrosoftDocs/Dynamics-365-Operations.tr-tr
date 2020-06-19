---
title: Akordiyon modülü
description: Bu konu akordiyon modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
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
ms.openlocfilehash: e06a0e0289e8c0c718aff4beab2c7a6ceb0a8cb1
ms.sourcegitcommit: 2683aacb426bfb3b541637edf1f8ec2d6cb5a745
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/01/2020
ms.locfileid: "3417266"
---
# <a name="accordion-module"></a><span data-ttu-id="bcf0a-103">Akordiyon modülü</span><span class="sxs-lookup"><span data-stu-id="bcf0a-103">Accordion module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="bcf0a-104">Bu konu akordiyon modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-104">This topic covers accordion modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="bcf0a-105">Özet</span><span class="sxs-lookup"><span data-stu-id="bcf0a-105">Overview</span></span>

<span data-ttu-id="bcf0a-106">Akordiyon modülleri, bir sayfadaki bilgileri veya modülleri daraltılabilir bir çekmece benzeri yetenek sağlayarak düzenlemek için kullanılan kapsayıcı benzeri modüllerdir.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-106">Accordion modules are container-like modules that are used to organize the information or modules on a page by providing a collapsible drawer-like capability.</span></span> <span data-ttu-id="bcf0a-107">Bir akordiyon modülü herhangi bir sayfada kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-107">An accordion module can be used on any page.</span></span>

<span data-ttu-id="bcf0a-108">Her akordiyon modülü içinde bir veya daha fazla akordiyon madde modülü eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-108">Inside every accordion module, one or more accordion item modules can be added.</span></span> <span data-ttu-id="bcf0a-109">Her bir akordiyon öğesi modülü daraltılabilir bir çekmeceyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-109">Each accordion item module represents a collapsible drawer.</span></span> <span data-ttu-id="bcf0a-110">Her akordiyon madde modülü içinde bir veya daha fazla modülü eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-110">Inside every accordion item module, one or more modules can be added.</span></span> <span data-ttu-id="bcf0a-111">Bir akordiyon madde modülüne eklenebilecek modül türlerinde bir sınırlama yoktur.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-111">There are no restrictions on the types of modules that can be added to an accordion item module.</span></span>

<span data-ttu-id="bcf0a-112">Aşağıdaki resimde, bir mağazanın sık sorulan sorular (SSS) sayfasındaki bilgileri düzenlemek için kullanılan bir akordiyon modülü örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-112">The following image shows an example of an accordion module that is used to organize information on a store's frequently asked questions (FAQ) page.</span></span>

![Akordiyon modülü örneği](./media/ecommerce-accordion.PNG)

## <a name="accordion-module-properties"></a><span data-ttu-id="bcf0a-114">Akordiyon modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="bcf0a-114">Accordion module properties</span></span>

| <span data-ttu-id="bcf0a-115">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="bcf0a-115">Property name</span></span> | <span data-ttu-id="bcf0a-116">Değerler</span><span class="sxs-lookup"><span data-stu-id="bcf0a-116">Values</span></span> | <span data-ttu-id="bcf0a-117">Tanım</span><span class="sxs-lookup"><span data-stu-id="bcf0a-117">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="bcf0a-118">Başlık</span><span class="sxs-lookup"><span data-stu-id="bcf0a-118">Heading</span></span> | <span data-ttu-id="bcf0a-119">Metin</span><span class="sxs-lookup"><span data-stu-id="bcf0a-119">Text</span></span> | <span data-ttu-id="bcf0a-120">Bu özellik akordiyon modülü için isteğe bağlı bir metin başlığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-120">This property specifies an optional text heading for the accordion module.</span></span> |
| <span data-ttu-id="bcf0a-121">Tümünü Genişlet</span><span class="sxs-lookup"><span data-stu-id="bcf0a-121">Expand All</span></span> | <span data-ttu-id="bcf0a-122">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="bcf0a-122">**True** or **False**</span></span> | <span data-ttu-id="bcf0a-123">Değer **doğru** olarak ayarlanırsa akordiyon modülündeki tüm öğelerin genişletilebileceği ve daraltılabilmesi için genişletme/daraltma işlevi açılır.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-123">If the value is set to **True**, expand/collapse functionality is turned on, so that all items in the accordion module can be expanded and collapsed.</span></span> |
| <span data-ttu-id="bcf0a-124">Etkileşim stili</span><span class="sxs-lookup"><span data-stu-id="bcf0a-124">Interaction Style</span></span> | <span data-ttu-id="bcf0a-125">**Bağımsız** veya **yalnızca bir öğeyi genişlet**</span><span class="sxs-lookup"><span data-stu-id="bcf0a-125">**Independent** or **Expand one item only**</span></span> | <span data-ttu-id="bcf0a-126">Bu özellik, akordiyon öğeler için etkileşimin stilini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-126">This property defines the style of interaction for accordion items.</span></span> <span data-ttu-id="bcf0a-127">Değer **bağımsız** olarak ayarlandığında her bir akordiyon öğesi bağımsız olarak genişletilebilir veya daraltılabilir.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-127">If the value is set to **Independent**, each accordion item can be expanded or collapsed independently.</span></span> <span data-ttu-id="bcf0a-128">Değer **yalnızca bir öğeyi genişletmek** üzere ayarlandıysa bir seferde yalnızca bir madde genişletilebilir.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-128">If the value is set to **Expand one item only**, only one item can be expanded at a time.</span></span> <span data-ttu-id="bcf0a-129">Öğeler genişletildiği gibi, önceden genişletilmiş öğeler daraltılmıştır.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-129">As items are expanded, previously expanded items are collapsed.</span></span> |

## <a name="accordion-item-module-properties"></a><span data-ttu-id="bcf0a-130">Akordiyon madde modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="bcf0a-130">Accordion item module properties</span></span>

| <span data-ttu-id="bcf0a-131">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="bcf0a-131">Property name</span></span> | <span data-ttu-id="bcf0a-132">Değerler</span><span class="sxs-lookup"><span data-stu-id="bcf0a-132">Values</span></span> | <span data-ttu-id="bcf0a-133">Tanım</span><span class="sxs-lookup"><span data-stu-id="bcf0a-133">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="bcf0a-134">Ünvan</span><span class="sxs-lookup"><span data-stu-id="bcf0a-134">Title</span></span> | <span data-ttu-id="bcf0a-135">Metin</span><span class="sxs-lookup"><span data-stu-id="bcf0a-135">Text</span></span> | <span data-ttu-id="bcf0a-136">Bu özellik akordiyon madde modülü için bir başlık metini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-136">This property specifies the title text for the accordion item module.</span></span> <span data-ttu-id="bcf0a-137">Başlık bölgesini seçerek, kullanıcılar bölümü genişletebilir veya daraltabilir.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-137">By selecting the title region, users can expand or collapse the section.</span></span> |
| <span data-ttu-id="bcf0a-138">Varsayılan olarak genişlet</span><span class="sxs-lookup"><span data-stu-id="bcf0a-138">Expand by default</span></span> | <span data-ttu-id="bcf0a-139">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="bcf0a-139">**True** or **False**</span></span> | <span data-ttu-id="bcf0a-140">Değer **doğru** olarak ayarlanırsa sayfa yüklendiğinde akordiyon madde varsayılan olarak genişletilir.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-140">If the value is set to **True**, the accordion item is expanded by default when the page is loaded.</span></span> |

## <a name="add-an-accordion-module-to-a-faq-page"></a><span data-ttu-id="bcf0a-141">SSS sayfasına akordiyon modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="bcf0a-141">Add an accordion module to a FAQ page</span></span>

<span data-ttu-id="bcf0a-142">SSS sayfaya akordiyon modülü eklemek ve özelliklerini site oluşturucuda ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-142">To add an accordion module to a FAQ page and set its properties in site builder, follow these steps.</span></span>

1. <span data-ttu-id="bcf0a-143">**Mağaza SSS** adlı yeni bir sayfa oluşturmak için **sayfalara** gidin ve Fabrikam pazarlama şablonunu (veya sınırlamaları olmayan tüm şablonları) kullanın.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-143">Go to **Pages**, and use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store FAQ**.</span></span>
1. <span data-ttu-id="bcf0a-144">**Varsayılan sayfada** **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-144">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="bcf0a-145">**Modül Ekle** iletişim kutusunda **Konteyner** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-145">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="bcf0a-146">**Konteyner** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-146">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="bcf0a-147">**Modül Ekle** iletişim kutusunda **akordiyon** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-147">In the **Add Module** dialog box, select the **Accordion** module, and then select **OK**.</span></span>
1. <span data-ttu-id="bcf0a-148">Akordiyon modülünün Özellik bölmesinde, kurşun kalem simgesinin yanındaki **Başlık**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-148">In the property pane of the accordion module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="bcf0a-149">**Başlık** iletişim kutusunda, **başlık metni** altında **sık sorulan soruları** girin.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-149">In the **Heading** dialog box, under **Heading Text**, enter **Frequently asked questions**.</span></span> <span data-ttu-id="bcf0a-150">Daha sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-150">Then select **OK**.</span></span>
1. <span data-ttu-id="bcf0a-151">Akordiyon modülünün Özellik bölmesinde, **Tümünü Genişlet** onay kutusunu seçin ve sonra **etkileşim stili** alanında **bağımsız**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-151">In the property pane of the accordion module, select the **Show expand all** check box, and then, in the **Interaction style** field, select **Independent**.</span></span>
1. <span data-ttu-id="bcf0a-152">**Akordiyon** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-152">In the **Accordion** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="bcf0a-153">**Modül Ekle** iletişim kutusunda **akordiyon madde** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-153">In the **Add Module** dialog box, select the **Accordion item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="bcf0a-154">Accordion madde modülünün Özellik bölmesinde, **başlık** altında başlık metnini girin (örneğin, **çalışma nasıl döner?**).</span><span class="sxs-lookup"><span data-stu-id="bcf0a-154">In the property pane of the accordion item module, under **Title**, enter title text (for example, **How do returns work?**).</span></span>
1. <span data-ttu-id="bcf0a-155">**Akordiyon madde** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-155">In the **Accordion item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="bcf0a-156">**Modül Ekle** iletişim kutusunda **Metin bloku** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-156">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="bcf0a-157">Metin bloğu modülünün Özellik bölmesinde bir paragraf metni girin (örneğin, **İadeler çağrı merkezi aracılığıyla işlenmelidir. İadeler için 1-800-FABRIKAM arayın. Ürünlerin 30 günlük bir iade ilkesi vardır. İadeler bu zaman çerçevesinde başlatılmalıdır.**).</span><span class="sxs-lookup"><span data-stu-id="bcf0a-157">In the property pane of the text block module, enter a paragraph of text (for example, **Returns must be processed via the call center. Contact 1-800-FABRIKAM for returns. Products have a 30-day return policy. Returns must be initiated within this time frame.**).</span></span>
1. <span data-ttu-id="bcf0a-158">**Akordiyon** yuvasında birkaç tane daha akordiyon madde modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-158">In the **Accordion** slot, add a few more accordion item modules.</span></span> <span data-ttu-id="bcf0a-159">Her bir akordiyon madde modülünde içeriği olan bir metin bloğu modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-159">In each accordion item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="bcf0a-160">**Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-160">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="bcf0a-161">Sayfa, eklediğiniz içeriğe sahip bir akordiyon modülü gösterir.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-161">The page will show an accordion module that has the content that you added.</span></span>
1. <span data-ttu-id="bcf0a-162">Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="bcf0a-162">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bcf0a-163">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="bcf0a-163">Additional resources</span></span>

[<span data-ttu-id="bcf0a-164">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="bcf0a-164">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="bcf0a-165">Konteyner modülü</span><span class="sxs-lookup"><span data-stu-id="bcf0a-165">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="bcf0a-166">Sekme modülü</span><span class="sxs-lookup"><span data-stu-id="bcf0a-166">Tab module</span></span>](add-tab.md)

[<span data-ttu-id="bcf0a-167">Metin bloğu modülü</span><span class="sxs-lookup"><span data-stu-id="bcf0a-167">Text block module</span></span>](add-content-rich-block.md)
