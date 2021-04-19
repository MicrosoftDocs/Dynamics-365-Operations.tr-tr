---
title: Önceden ayarlanmış düzenlerle çalışma
description: Bu konuda, Microsoft Dynamics 365 Commerce'ta önceden belirlenmiş düzenlerle nasıl çalışılacağı açıklanmaktadır.
author: phinneyridge
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ce54be1032777ffcaac474773cdeeef3b9028110
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793933"
---
# <a name="work-with-preset-layouts"></a><span data-ttu-id="95610-103">Önceden ayarlanmış düzenlerle çalışma</span><span class="sxs-lookup"><span data-stu-id="95610-103">Work with preset layouts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="95610-104">Bu konuda, Microsoft Dynamics 365 Commerce'ta önceden belirlenmiş düzenlerle nasıl çalışılacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="95610-104">This topic describes how to work with preset layouts in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="95610-105">Bu konudaki yordamları gerçekleştirmeden önce, [hazır ayar ve özel düzenleri](templates-layouts-overview.md#preset-and-custom-layouts) okuduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="95610-105">Before you complete the procedures in this topic, be sure to read [Preset and custom layouts](templates-layouts-overview.md#preset-and-custom-layouts).</span></span> <span data-ttu-id="95610-106">Genel genel bakış için, bkz. [Şablonlar ve düzenler genel bakış](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="95610-106">For a general overview, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="create-a-new-preset-layout"></a><span data-ttu-id="95610-107">Yeni önceden ayarlanmış düzeni oluşturma</span><span class="sxs-lookup"><span data-stu-id="95610-107">Create a new preset layout</span></span>

<span data-ttu-id="95610-108">Önceden ayarlı düzen oluşturmak için iki yöntem vardır.</span><span class="sxs-lookup"><span data-stu-id="95610-108">There are two methods for creating a preset layout.</span></span> <span data-ttu-id="95610-109">Varolan bir özel düzeni yeni bir hazır ayar düzeni olarak kaydedebilir veya sıfırdan bir hazır ayar düzeni oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="95610-109">You can save an existing custom layout as a new preset layout, or you can create a preset layout from scratch.</span></span>

### <a name="create-a-preset-layout-from-an-existing-custom-layout"></a><span data-ttu-id="95610-110">Varolan özel düzenden önceden belirlenmiş düzen oluşturma</span><span class="sxs-lookup"><span data-stu-id="95610-110">Create a preset layout from an existing custom layout</span></span>

<span data-ttu-id="95610-111">Varolan özel düzenden önceden belirlenmiş düzen oluşturmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="95610-111">To create a preset layout from an existing custom layout, follow these steps.</span></span>

1. <span data-ttu-id="95610-112">Şu anda hazır ayar düzeni kullanmayan ve sitenizdeki diğer sayfalar için yeniden kullanmak istediğiniz bir modül yapısına sahip olan varolan sayfayı açın.</span><span class="sxs-lookup"><span data-stu-id="95610-112">Open an existing page that doesn't currently use a preset layout, and that has a module structure that you want to reuse for other pages on your site.</span></span>
1. <span data-ttu-id="95610-113">Sayfayı kullanıma almak için **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="95610-113">Select **Edit** to check out the page.</span></span>
1. <span data-ttu-id="95610-114">**Yeni Düzen olarak kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="95610-114">Select **Save as new layout**.</span></span> <span data-ttu-id="95610-115">**Yeni düzen olarak Kaydet** iletişim kutusu görünür.</span><span class="sxs-lookup"><span data-stu-id="95610-115">The **Save as new layout** dialog box appears.</span></span>
1. <span data-ttu-id="95610-116">Önceden ayarlı düzen için bir ad ve açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="95610-116">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="95610-117">Girdiğiniz değerler, yerleşiminizde yeni sayfalar oluştururken veya bu yazarlardan diğerine geçiş yaparken diğer yazarlar tarafından gösterilir.</span><span class="sxs-lookup"><span data-stu-id="95610-117">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="95610-118">Bu nedenle, sayfa yazarları için yararlı olacak değerleri girin.</span><span class="sxs-lookup"><span data-stu-id="95610-118">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="95610-119">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="95610-119">Select **OK**.</span></span>

<span data-ttu-id="95610-120">Yeni sayfalar oluşturduğunuzda veya aynı şablon hiyerarşisindeki bir sayfa için farklı bir düzen seçtiğinizde, önceden ayarlanmış düzen artık kullanılabilir olacaktır.</span><span class="sxs-lookup"><span data-stu-id="95610-120">The preset layout will now be available when you create new pages or select a different layout for a page in the same template hierarchy.</span></span>

> [!TIP]
> <span data-ttu-id="95610-121">Belirli bir sayfanın önceden belirlenmiş bir yerleşime bağlı olup olmadığını hızlı şekilde görmek için, sayfalar liste görünümünde sayfayı seçin ve sağdaki Özellik bölmesinde Düzen meta verilerini inceleyin.</span><span class="sxs-lookup"><span data-stu-id="95610-121">To quickly see whether a specific page is currently bound to a preset layout, select the page in the pages list view, and inspect the layout metadata in the property pane on the right.</span></span>

### <a name="create-a-new-preset-layout"></a><span data-ttu-id="95610-122">Yeni önceden ayarlanmış düzeni oluşturma</span><span class="sxs-lookup"><span data-stu-id="95610-122">Create a new preset layout</span></span>

<span data-ttu-id="95610-123">Sıfırdan önceden belirlenmiş düzen oluşturmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="95610-123">To create a preset layout from scratch, follow these steps.</span></span>

1. <span data-ttu-id="95610-124">Soldaki gezinti bölmesinde **Düzenler** seçin.</span><span class="sxs-lookup"><span data-stu-id="95610-124">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="95610-125">**Yeni Düzen** seçin.</span><span class="sxs-lookup"><span data-stu-id="95610-125">Select **New Layout**.</span></span> <span data-ttu-id="95610-126">**Yeni düzen** iletişim kutusu görünür.</span><span class="sxs-lookup"><span data-stu-id="95610-126">The **New layout** dialog box appears.</span></span>
1. <span data-ttu-id="95610-127">Hazır ayar düzeniniz için kullanılacak şablonu seçin.</span><span class="sxs-lookup"><span data-stu-id="95610-127">Select the template to use for your preset layout.</span></span>
1. <span data-ttu-id="95610-128">Önceden ayarlı düzen için bir ad ve açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="95610-128">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="95610-129">Girdiğiniz değerler, yerleşiminizde yeni sayfalar oluştururken veya bu yazarlardan diğerine geçiş yaparken diğer yazarlar tarafından gösterilir.</span><span class="sxs-lookup"><span data-stu-id="95610-129">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="95610-130">Bu nedenle, sayfa yazarları için yararlı olacak değerleri girin.</span><span class="sxs-lookup"><span data-stu-id="95610-130">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="95610-131">Yeni hazır ayar düzenini oluşturmak ve düzen düzenleyicisini açmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="95610-131">Select **OK** to create the new preset layout and open the layout editor.</span></span>
1. <span data-ttu-id="95610-132">Düzen Düzenleyicisinde, sol taraftaki anahat ağacını ve sağdaki Özellik bölmesini kullanarak modülleri ekleyin ve konfigüre edin.</span><span class="sxs-lookup"><span data-stu-id="95610-132">In the layout editor, add and configure modules by using the outline tree on the left and the property pane on the right.</span></span> <span data-ttu-id="95610-133">(Bu işlem, şablon düzenleyicisinde bir şablon için modül ekleme ve konfigüre etme işlemine benzer.) Modüllerin yerleşimi ve tüm kilitli varsayılan ayarlar, bu önceden ayarlanmış düzeni kullanan tüm sayfalar için merkezi modül yapılandırmasına dönüşür.</span><span class="sxs-lookup"><span data-stu-id="95610-133">(The process resembles the process for adding and configuring modules for a template in the template editor.) The arrangement of modules and any locked default settings become the centralized module configuration for any pages that use this preset layout.</span></span>

## <a name="modify-a-preset-layout"></a><span data-ttu-id="95610-134">Önceden belirlenmiş yerleşimi değiştirme</span><span class="sxs-lookup"><span data-stu-id="95610-134">Modify a preset layout</span></span>

<span data-ttu-id="95610-135">Önceden belirlenmiş düzen değiştirmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="95610-135">To modify a preset layout, follow these steps.</span></span>

1. <span data-ttu-id="95610-136">Soldaki gezinti bölmesinde **Düzenler** seçin.</span><span class="sxs-lookup"><span data-stu-id="95610-136">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="95610-137">Düzen düzenleyicisinde, soldaki anahat ağacında, değiştirilecek modülü seçin.</span><span class="sxs-lookup"><span data-stu-id="95610-137">In the layout editor, in the outline tree on the left, select the module to modify.</span></span> <span data-ttu-id="95610-138">Ardından şu adımlardan birini izleyin:</span><span class="sxs-lookup"><span data-stu-id="95610-138">Then follow any of these steps:</span></span>

    - <span data-ttu-id="95610-139">Bir modülü üst öğenin içinde yukarı veya aşağı taşımak için üç nokta düğmesini (**...**) oluşturun ve **yukarı taşı** veya **aşağı taşı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="95610-139">To move a module up or down inside its parent, select the ellipsis button (**...**) for the module, and then select **Move up** or **Move down**.</span></span>
    - <span data-ttu-id="95610-140">Bir modülün varsayılan ayarlarını değiştirmek için, varsayılan değerleri girmek ve isteğe bağlı olarak bunları tüm aşağı akış sayfalarında kilitlemek için özellik bölmesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="95610-140">To change a module's default settings, use the property pane to enter default values and optionally lock them for all downstream pages.</span></span>
    - <span data-ttu-id="95610-141">Konteyner modüllerine yeni modüller veya parçalar eklemek için üç nokta düğmesini seçin ve sonra **Modül ekle**'yi veya **Parça ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="95610-141">To add new modules or fragments to container modules, select the ellipsis button, and then select **Add module** or **Add fragment**.</span></span>
    - <span data-ttu-id="95610-142">Bir modülü düzenden kaldırmak için, üç nokta düğmesini de seçin ve sonra **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="95610-142">To remove a module from the layout, select the ellipsis button, and then select **Delete**.</span></span>

## <a name="change-a-preset-layout-theme"></a><span data-ttu-id="95610-143">Hazır ayar düzen temasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="95610-143">Change a preset layout theme</span></span>

<span data-ttu-id="95610-144">Tipik bir uygulama, varsayılan temayı önceden belirlenmiş bir düzen kullanan tüm sayfalar için ayarlayacaktır.</span><span class="sxs-lookup"><span data-stu-id="95610-144">A typical practice is to set a default theme for all pages that use a preset layout.</span></span>

<span data-ttu-id="95610-145">Hazır ayar düzeninizi kullanan tüm alt sayfaların temasını ayarlamak veya değiştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="95610-145">To set or change the theme for all child pages that use your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="95610-146">Düzen düzenleyicisinde, soldaki anahat ağacında, sayfa konteyner modülü seçin.</span><span class="sxs-lookup"><span data-stu-id="95610-146">In the layout editor, in the outline tree on the left, select the page container module.</span></span> <span data-ttu-id="95610-147">(Bu modül genellikle ikinci düğümdür ve **varsayılan sayfa** olarak adlandırılır.)</span><span class="sxs-lookup"><span data-stu-id="95610-147">(Typically, this module is the second node and is named **Default page**.)</span></span>
1. <span data-ttu-id="95610-148">Sağdaki özellik bölmesinde, **Tema** alanında bir tema seçin.</span><span class="sxs-lookup"><span data-stu-id="95610-148">In the property pane on the right, in the **Theme** field, select a theme.</span></span>

## <a name="save-check-in-preview-and-publish-a-preset-layout"></a><span data-ttu-id="95610-149">Hazır ayar düzenine kaydetme, iade etme, önizleme ve yayımlama</span><span class="sxs-lookup"><span data-stu-id="95610-149">Save, check in, preview, and publish a preset layout</span></span>

<span data-ttu-id="95610-150">Hazır ayar düzeninizi kaydetmek ve iade etmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="95610-150">To save and check in your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="95610-151">Mizanpaj Düzenleyicisinin üst kısmında **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="95610-151">Select **Save** at the top of the layout editor.</span></span> <span data-ttu-id="95610-152">Kaydedilen değişiklikler, bu akış yönündeki sayfaları iade edilene kadar etkilemez.</span><span class="sxs-lookup"><span data-stu-id="95610-152">Saved changes don't affect downstream pages until they are checked in.</span></span>
1. <span data-ttu-id="95610-153">**Düzenlemeyi bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="95610-153">Select **Finish editing**.</span></span> <span data-ttu-id="95610-154">Değişiklikleriniz, aşağı akışlar için artık bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="95610-154">Your changes are now discoverable for downstream workflows.</span></span>

<span data-ttu-id="95610-155">Değişikliklerinizin önizlemesine bakmak için, önceden ayarlanmış düzenini kullanan varolan bir sayfayı açın veya düzenden yeni bir sayfa oluşturun.</span><span class="sxs-lookup"><span data-stu-id="95610-155">To preview your changes, either open an existing page that uses the preset layout or create a new page from the layout.</span></span>

<span data-ttu-id="95610-156">Değişiklik önceden belirlenmiş yerleşiminizde yapılan değişiklikleri önizledikten sonra, görünümü canlı sitenizde yayımlamak için aşağıdaki adımlardan birini izleyin:</span><span class="sxs-lookup"><span data-stu-id="95610-156">After you've previewed the changes to your preset layout, follow one of these steps to publish the layout to your live site:</span></span>

* <span data-ttu-id="95610-157">**Düzenlere** gidin, düzeni seçin ve sonra **Yayınla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="95610-157">Go to **Layouts**, select the layout, and then select **Publish**.</span></span>
* <span data-ttu-id="95610-158">Düzen düzenleyicisini açmak için düzen açını ve ardından **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="95610-158">Select the layout name to open the layout editor, and then select **Publish**.</span></span>
* <span data-ttu-id="95610-159">Yayımlanmamış yerleşime başvuran bir sayfa yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="95610-159">Publish a page that references the unpublished layout.</span></span> <span data-ttu-id="95610-160">Düzen otomatik olarak yayımlanacak.</span><span class="sxs-lookup"><span data-stu-id="95610-160">The layout will automatically be published.</span></span>

> [!WARNING]
> <span data-ttu-id="95610-161">Önceden belirlenmiş mizanpajlara birden çok sayfa başvuruyor.</span><span class="sxs-lookup"><span data-stu-id="95610-161">Preset layouts can be referenced by multiple pages.</span></span> <span data-ttu-id="95610-162">Önceden belirlenmiş bir düzeni yayımladığınızda, birden çok sayfanın düzenini etkileyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="95610-162">When you publish a preset layout, be aware that you might affect the layout of multiple pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="95610-163">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="95610-163">Additional resources</span></span>

[<span data-ttu-id="95610-164">Şablonlar ve düzenlere genel bakış</span><span class="sxs-lookup"><span data-stu-id="95610-164">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="95610-165">Şablonlarla çalışma</span><span class="sxs-lookup"><span data-stu-id="95610-165">Work with templates</span></span>](work-with-templates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
