---
title: Parçalarla çalışma
description: Bu konu, Microsoft Dynamics 365 Commerce'ta parçaları neden, ne zaman ve ne zaman kullanılacağını açıklamaktadır.
author: v-chgri
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 32482538b2913e6585257bcf7a1cbe780d3cdd30
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914712"
---
# <a name="work-with-fragments"></a><span data-ttu-id="908ce-103">Parçalarla çalışma</span><span class="sxs-lookup"><span data-stu-id="908ce-103">Work with fragments</span></span> 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="908ce-104">Bu konu, Microsoft Dynamics 365 Commerce'ta parçaları neden, ne zaman ve ne zaman kullanılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="908ce-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="908ce-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="908ce-105">Overview</span></span>

<span data-ttu-id="908ce-106">Parçalar, tüm sitenizde yeniden kullanılması gereken modül yapılandırmaları için merkezi bir yazma deneyimine olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="908ce-106">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="908ce-107">Örneğin, üstbilgiler, altbilgiler ve başlıklar birçok sayfada paylaşıldıklarından, genellikle parçalar halinde yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="908ce-107">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="908ce-108">Parçaları sitenizdeki diğer sayfalara eklenebilen minyatür Web sayfaları olarak düşünebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="908ce-108">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="908ce-109">Parçaların kendi yaşam döngüsü vardır.</span><span class="sxs-lookup"><span data-stu-id="908ce-109">Fragments have their own lifecycle.</span></span> <span data-ttu-id="908ce-110">Başka bir deyişle bunlar, yazma araçlarında bağımsız varlıklar olarak oluşturulur, başvurulur, güncellenir ve silinir.</span><span class="sxs-lookup"><span data-stu-id="908ce-110">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="908ce-111">Parçalar yapılandırıldıktan sonra, site yapınızda modüllerin kullanılabileceği her yerde kullanılabilirler.</span><span class="sxs-lookup"><span data-stu-id="908ce-111">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="908ce-112">Parçalar sayfalarda, mizanpajlarda, şablonlarda ve diğer parçalarda başvurulabilir.</span><span class="sxs-lookup"><span data-stu-id="908ce-112">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="908ce-113">Parçalar, diğer parçaların içinde en fazla yedi düzeye kadar iç içe geçmiş olabilir.</span><span class="sxs-lookup"><span data-stu-id="908ce-113">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="908ce-114">Örneğin, sitemizde birçok sayfada dönemsel olay yükseltmek istiyorsanız, bir parça kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="908ce-114">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="908ce-115">Yeni parça oluşturma işlemindeki ilk adım, başlatmak istediğiniz modül türünü seçmektir.</span><span class="sxs-lookup"><span data-stu-id="908ce-115">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="908ce-116">Bu örnekte, bir kahraman modülünden parça oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="908ce-116">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="908ce-117">Parçalar herhangi bir modül türünden oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="908ce-117">Fragments can be built from any module type.</span></span>

<span data-ttu-id="908ce-118">Bundan sonra, hero parçacığını özel tanıtım içerikleriniz ile konfigüre edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="908ce-118">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="908ce-119">Ayrıca, bunu gereksinim duyduğunuz şekilde yerelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="908ce-119">You can also localize it as you require.</span></span> <span data-ttu-id="908ce-120">Yeni tek başına kahraman parçası daha sonra, siteniz genelinde önceden yapılandırılmış bir modül olarak tüketilebilir.</span><span class="sxs-lookup"><span data-stu-id="908ce-120">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="908ce-121">Bunu şablonlara, belirli sayfalara veya kahramanı modüllerini içerebilecek diğer parçalara kolayca ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="908ce-121">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="908ce-122">Parçanın eklendiği tüm yerler, oluşturduğunuz Merkez kahraman parçasına yapılan referanslardır.</span><span class="sxs-lookup"><span data-stu-id="908ce-122">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="908ce-123">Değişiklikleri parçalara yayımlarsanız, bu değişiklikler derhal site genelinde referans alınan tüm yerlere yansıtılır.</span><span class="sxs-lookup"><span data-stu-id="908ce-123">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="908ce-124">Bu nedenle, parçalar bir sitede modül konfigürasyonlarını tekrar kullanmak ve merkezi olarak yönetmek için güçlü ve etkili bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="908ce-124">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="908ce-125">Bunları etkili şekilde kullanarak, size önemli ölçüde yükseltebilir ve Site içeriğiyle ilgili maliyeti azaltmaya yardımcı olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="908ce-125">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="908ce-126">Aşağıdaki şekil, bir e-ticaret sitesinde paylaşılan modül konfigürasyonlarını merkezileştirmek için parçaların nasıl kullanılabileceğini göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="908ce-126">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![Aşağıdaki şekil, bir e-ticaret sitesinde paylaşılan modül konfigürasyonlarını merkezileştirmek için parçaların nasıl kullanılabileceğini göstermektedir.](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="908ce-128">Parça oluştur</span><span class="sxs-lookup"><span data-stu-id="908ce-128">Create a fragment</span></span>

<span data-ttu-id="908ce-129">Yeni bir parça oluşturabilir veya varolan bir modül konfigürasyonunu parça olarak kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="908ce-129">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="create-a-new-fragment"></a><span data-ttu-id="908ce-130">Yeni bir parça oluşturun.</span><span class="sxs-lookup"><span data-stu-id="908ce-130">Create a new fragment</span></span>

<span data-ttu-id="908ce-131">Bir yeni parça oluşturmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="908ce-131">To create a new fragment, follow these steps.</span></span>

1. <span data-ttu-id="908ce-132">Soldaki gezinti bölmesinde **Parçalar** seçin.</span><span class="sxs-lookup"><span data-stu-id="908ce-132">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="908ce-133">**Yeni Sayfa Parçası**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="908ce-133">Select **New Page Fragment**.</span></span> <span data-ttu-id="908ce-134">Kullanılabilen tüm modül türlerini gösteren bir iletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="908ce-134">A dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="908ce-135">Daha önce belirtildiği gibi, parçalar herhangi bir modül türünden oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="908ce-135">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="908ce-136">Parçanız için bir modül türü seçin ve sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="908ce-136">Select a module type for your fragment, and then select **OK**.</span></span>

    > [!TIP]
    > <span data-ttu-id="908ce-137">Genel bir konteyner modülü türü seçerek parçanız daha sonra güncelleştirmeniz ve yapılandırmanız gerektiğinde en iyi esnekliği elde edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="908ce-137">By selecting a generic container module type, you get the most flexibility when you must update and configure your fragment later.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="908ce-138">Varolan bir modül konfigürasyonunu parça olarak kaydet</span><span class="sxs-lookup"><span data-stu-id="908ce-138">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="908ce-139">Önceden yapılandırılmış bir modülü yeniden kullanılabilir parçaya dönüştürmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="908ce-139">To convert a previously configured module to a reusable fragment, follow these steps.</span></span>

1. <span data-ttu-id="908ce-140">Bir parçaya dönüştürmek istediğiniz modülü içeren sayfayı veya şablonu açın.</span><span class="sxs-lookup"><span data-stu-id="908ce-140">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="908ce-141">Soldaki anahat bölmesinde, modülün adının yanında üç nokta düğmesini (**...**) seçin ve **Parça olarak kaydet** seçin.</span><span class="sxs-lookup"><span data-stu-id="908ce-141">In the outline pane on the left, select the ellipsis button (**...**) next to the name of the module, and then select **Save as Fragment**.</span></span> <span data-ttu-id="908ce-142">İletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="908ce-142">A dialog box appears.</span></span>
1. <span data-ttu-id="908ce-143">Parça için bir ad ve meta veri girin.</span><span class="sxs-lookup"><span data-stu-id="908ce-143">Enter a name and metadata for the fragment.</span></span>
1. <span data-ttu-id="908ce-144">Modül konfigürasyonunu diğer sayfalara eklenebilecek bir parça olarak kaydetmek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="908ce-144">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="908ce-145">Sayfaya parça ekleme, kaldırma veya düzenleme</span><span class="sxs-lookup"><span data-stu-id="908ce-145">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="908ce-146">Aşağıdaki yordamlarda parçaların nasıl ekleneceği, kaldırılacağı ve düzenleneceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="908ce-146">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="908ce-147">Parça ekle</span><span class="sxs-lookup"><span data-stu-id="908ce-147">Add a fragment</span></span>

<span data-ttu-id="908ce-148">Bir sayfaya parça eklemek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="908ce-148">To add a fragment to a page, follow these steps.</span></span>

1. <span data-ttu-id="908ce-149">Soldaki anahat bölmesinde, alt modüllerin eklenebileceği bir konteyner veya yuva seçin.</span><span class="sxs-lookup"><span data-stu-id="908ce-149">In the outline pane on the left, select a container or slot that child modules can be added to.</span></span>
1. <span data-ttu-id="908ce-150">Konteyner veya yuvanın adının yanındaki üç nokta düğmesini seçin ve **parça Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="908ce-150">Select the ellipsis button next to the name of the container or slot, and then select **Add Fragment**.</span></span> <span data-ttu-id="908ce-151">İletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="908ce-151">A dialog box appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="908ce-152">Bir konteyner veya yuva yeni alt modülleri desteklemiyorsa, **Parça Ekle** seçeneği kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="908ce-152">If the container or slot doesn't support new child modules, the **Add Fragment** option is unavailable.</span></span>

1. <span data-ttu-id="908ce-153">İletişim kutusunda, eklenecek bir parça arayıp seçin.</span><span class="sxs-lookup"><span data-stu-id="908ce-153">In the dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="908ce-154">Listelenmiş parça listelenmezse, önce seçilen konteyner veya yuvanın desteklediği bir modül türünden bir parça oluşturmanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="908ce-154">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="908ce-155">Seçili parça sayfanızdaki seçili konteynere veya yuvaya eklemek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="908ce-155">Select **OK** to add the selected fragment to the selected container or slot on your page.</span></span>

> [!NOTE]
> <span data-ttu-id="908ce-156">Bir konteynerde veya bir yuvada izin verilen modüller, sayfa şablonu veya modüllerin kendi tanımları tarafından tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="908ce-156">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="908ce-157">Parça kaldırma</span><span class="sxs-lookup"><span data-stu-id="908ce-157">Remove a fragment</span></span>

<span data-ttu-id="908ce-158">Sayfada yuva veya konteynerden parça kaldırmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="908ce-158">To remove a fragment from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="908ce-159">Soldaki anahat bölmesinde, kaldırılacak parçanın adının yanında üç nokta düğmesini seçin ve çöp tenekesi düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="908ce-159">In the outline pane on the left, select the ellipsis button next to the name of the fragment to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="908ce-160">Parçayı kaldırma isteğinizi onaylamanız istendiğinde, **tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="908ce-160">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="908ce-161">Sayfadan bir parçayı kaldırdığınızda, yalnızca bu sayfadan gelen başvuruyu kaldırırsınız.</span><span class="sxs-lookup"><span data-stu-id="908ce-161">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="908ce-162">Sitenizden parçayı **silmeyin**.</span><span class="sxs-lookup"><span data-stu-id="908ce-162">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="908ce-163">Sitenizdeki parçaları silmek için, parça denetçisi Kullanıcı arabirimini (UI) kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="908ce-163">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="908ce-164">Bir sitedeki parçaları yalnızca herhangi bir sayfa, şablon veya başka parçalar tarafından başvurulmuyorsa silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="908ce-164">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="908ce-165">Parça Düzenle</span><span class="sxs-lookup"><span data-stu-id="908ce-165">Edit a fragment</span></span>

<span data-ttu-id="908ce-166">Parçaları düzenlemek için, parça düzenleyici kullanıcı arabimirni kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="908ce-166">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="908ce-167">Bu kısıtlama tasarımdan kaynaklanır.</span><span class="sxs-lookup"><span data-stu-id="908ce-167">This restriction is by design.</span></span> <span data-ttu-id="908ce-168">Yazarların belirli bir sayfa için modülleri düzenleme işlemini, birçok sayfada paylaşılabilecek parça düzenleme işlemi ile karıştıradığından emin olmanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="908ce-168">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="908ce-169">Bir parça düzenlemek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="908ce-169">To edit a fragment, follow these steps.</span></span>

1. <span data-ttu-id="908ce-170">Soldaki gezinti bölmesinde **Parçalar** seçin.</span><span class="sxs-lookup"><span data-stu-id="908ce-170">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="908ce-171">**Parçalar** altında düzenlenecek parçayı seçin.</span><span class="sxs-lookup"><span data-stu-id="908ce-171">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="908ce-172">Parçanın modül özelliklerini ve yapısını gereksinim duyduğunuz şekilde Düzenle.</span><span class="sxs-lookup"><span data-stu-id="908ce-172">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="908ce-173">İşlem, düzenleme modüllerinin sayfa düzenleyici görünümde düzenlenmesi işlemine benzer.</span><span class="sxs-lookup"><span data-stu-id="908ce-173">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="908ce-174">Bir parçayı sayfada, şablonda veya üst parçada seçerek ve sağdaki Özellikler bölmesinde **parça Düzenle** 'yi seçerek düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="908ce-174">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="908ce-175">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="908ce-175">Additional resources</span></span>

[<span data-ttu-id="908ce-176">Şablonlar ve düzenlere genel bakış</span><span class="sxs-lookup"><span data-stu-id="908ce-176">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="908ce-177">Şablonlarla çalışma</span><span class="sxs-lookup"><span data-stu-id="908ce-177">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="908ce-178">Önceden ayarlanmış düzenlerle çalışma</span><span class="sxs-lookup"><span data-stu-id="908ce-178">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="908ce-179">Yayınlama gruplarıyla çalışma</span><span class="sxs-lookup"><span data-stu-id="908ce-179">Work with publish groups</span></span>](publish-groups.md)
