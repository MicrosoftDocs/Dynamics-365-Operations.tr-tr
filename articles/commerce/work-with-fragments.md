---
title: Parçalarla çalışma
description: Bu konu, Microsoft Dynamics 365 Commerce'ta parçaları neden, ne zaman ve ne zaman kullanılacağını açıklamaktadır.
author: v-chgri
manager: annbe
ms.date: 07/31/2020
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
ms.openlocfilehash: 7ae834f38fe380ce0a66f5b1968f1261af670979
ms.sourcegitcommit: 078befcd7f3531073ab2c08b365bcf132d6477b0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/31/2020
ms.locfileid: "3646003"
---
# <a name="work-with-fragments"></a><span data-ttu-id="4d5cf-103">Parçalarla çalışma</span><span class="sxs-lookup"><span data-stu-id="4d5cf-103">Work with fragments</span></span> 

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="4d5cf-104">Bu konu, Microsoft Dynamics 365 Commerce'ta parçaları neden, ne zaman ve ne zaman kullanılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4d5cf-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="4d5cf-105">Overview</span></span>

<span data-ttu-id="4d5cf-106">Parçalar, tüm sitenizde yeniden kullanılması gereken modül yapılandırmaları için merkezi bir yazma deneyimine olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-106">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="4d5cf-107">Örneğin, üstbilgiler, altbilgiler ve başlıklar birçok sayfada paylaşıldıklarından, genellikle parçalar halinde yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-107">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="4d5cf-108">Parçaları sitenizdeki diğer sayfalara eklenebilen minyatür Web sayfaları olarak düşünebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-108">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="4d5cf-109">Parçaların kendi yaşam döngüsü vardır.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-109">Fragments have their own lifecycle.</span></span> <span data-ttu-id="4d5cf-110">Başka bir deyişle bunlar, yazma araçlarında bağımsız varlıklar olarak oluşturulur, başvurulur, güncellenir ve silinir.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-110">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="4d5cf-111">Parçalar yapılandırıldıktan sonra, site yapınızda modüllerin kullanılabileceği her yerde kullanılabilirler.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-111">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="4d5cf-112">Parçalar sayfalarda, mizanpajlarda, şablonlarda ve diğer parçalarda başvurulabilir.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-112">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="4d5cf-113">Parçalar, diğer parçaların içinde en fazla yedi düzeye kadar iç içe geçmiş olabilir.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-113">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="4d5cf-114">Örneğin, sitemizde birçok sayfada dönemsel olay yükseltmek istiyorsanız, bir parça kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-114">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="4d5cf-115">Yeni parça oluşturma işlemindeki ilk adım, başlatmak istediğiniz modül türünü seçmektir.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-115">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="4d5cf-116">Bu örnekte, bir kahraman modülünden parça oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-116">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="4d5cf-117">Parçalar herhangi bir modül türünden oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-117">Fragments can be built from any module type.</span></span>

<span data-ttu-id="4d5cf-118">Bundan sonra, hero parçacığını özel tanıtım içerikleriniz ile konfigüre edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-118">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="4d5cf-119">Ayrıca, bunu gereksinim duyduğunuz şekilde yerelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-119">You can also localize it as you require.</span></span> <span data-ttu-id="4d5cf-120">Yeni tek başına kahraman parçası daha sonra, siteniz genelinde önceden yapılandırılmış bir modül olarak tüketilebilir.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-120">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="4d5cf-121">Bunu şablonlara, belirli sayfalara veya kahramanı modüllerini içerebilecek diğer parçalara kolayca ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-121">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="4d5cf-122">Parçanın eklendiği tüm yerler, oluşturduğunuz Merkez kahraman parçasına yapılan referanslardır.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-122">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="4d5cf-123">Değişiklikleri parçalara yayımlarsanız, bu değişiklikler derhal site genelinde referans alınan tüm yerlere yansıtılır.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-123">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="4d5cf-124">Bu nedenle, parçalar bir sitede modül konfigürasyonlarını tekrar kullanmak ve merkezi olarak yönetmek için güçlü ve etkili bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-124">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="4d5cf-125">Bunları etkili şekilde kullanarak, size önemli ölçüde yükseltebilir ve Site içeriğiyle ilgili maliyeti azaltmaya yardımcı olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-125">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="4d5cf-126">Aşağıdaki şekil, bir e-ticaret sitesinde paylaşılan modül konfigürasyonlarını merkezileştirmek için parçaların nasıl kullanılabileceğini göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-126">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![Aşağıdaki şekil, bir e-ticaret sitesinde paylaşılan modül konfigürasyonlarını merkezileştirmek için parçaların nasıl kullanılabileceğini göstermektedir.](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="4d5cf-128">Parça oluştur</span><span class="sxs-lookup"><span data-stu-id="4d5cf-128">Create a fragment</span></span>

<span data-ttu-id="4d5cf-129">Yeni bir parça oluşturabilir veya varolan bir modül konfigürasyonunu parça olarak kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-129">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="4d5cf-130">Varolan bir modül konfigürasyonunu parça olarak kaydet</span><span class="sxs-lookup"><span data-stu-id="4d5cf-130">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="4d5cf-131">Önceden yapılandırılmış bir modülü yeniden kullanılabilir parçaya dönüştürmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-131">To convert a previously configured module to a reusable fragment, follow these steps.</span></span>

1. <span data-ttu-id="4d5cf-132">Bir parçaya dönüştürmek istediğiniz modülü içeren sayfayı veya şablonu açın.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-132">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="4d5cf-133">Sol taraftaki ana hat bölmesinde veya doğrudan ana tuvalden, önceden yapılandırılmış modülü seçin.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-133">In the outline pane on the left or directly in the main canvas, select the previously configured module.</span></span>
1. <span data-ttu-id="4d5cf-134">Ana hat bölmesinde veya tuval içinde seçili modülün araç çubuğunda modül adının yanındaki üç noktayı (**...**) seçin.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-134">Select the ellipsis (**...**) next to the name of the module in either the outline pane or the selected module's toolbar in the canvas.</span></span> 
1. <span data-ttu-id="4d5cf-135">**Sayfa Parçası Olarak Paylaş**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-135">Select **Share as Page Fragment**.</span></span> 
1. <span data-ttu-id="4d5cf-136">**Sayfa Parçası Olarak Kaydet** iletişim kutusunda, parça için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-136">In the **Save as Page Fragment** dialog box, enter a name for the fragment.</span></span>
1. <span data-ttu-id="4d5cf-137">Modül konfigürasyonunu diğer sayfalara eklenebilecek bir parça olarak kaydetmek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-137">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>

<span data-ttu-id="4d5cf-138">Aşağıdaki resimde bir modül yapılandırmasının bir parça olarak nasıl kaydedileceği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-138">The following image shows how to save a module configuration as a fragment.</span></span>

![Bir modül yapılandırmasının parça olarak nasıl kaydedileceği ile ilgili bir ekran yakalama](./media/save-as-fragment.png)

### <a name="create-a-new-fragment"></a><span data-ttu-id="4d5cf-140">Yeni bir parça oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-140">Create a new fragment</span></span>

<span data-ttu-id="4d5cf-141">Bir yeni parça oluşturmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-141">To create a new fragment, follow these steps.</span></span>

1. <span data-ttu-id="4d5cf-142">Soldaki gezinti bölmesinde **Parçalar** seçin.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-142">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="4d5cf-143">**Yeni Sayfa Parçası**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-143">Select **New Page Fragment**.</span></span> <span data-ttu-id="4d5cf-144">Kullanılabilen tüm modül türlerini gösteren bir iletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-144">A dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="4d5cf-145">Daha önce belirtildiği gibi, parçalar herhangi bir modül türünden oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-145">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="4d5cf-146">Parçanız için bir modül türü seçin.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-146">Select a module type for your fragment.</span></span>

<span data-ttu-id="4d5cf-147">Aşağıdaki resimde, yeni bir parçanın oluşturulacağı yer gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-147">The following image shows where to create a new fragment.</span></span>

![Yeni parçanın oluşturulacağı yerin Ekran yakalaması](./media/fragment-nav-menu.png)

> [!TIP]
> <span data-ttu-id="4d5cf-149">Genel bir konteyner modülü türü seçerek parçanız daha sonra güncelleştirmeniz ve yapılandırmanız gerektiğinde en iyi esnekliği elde edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-149">By selecting a generic container module type, you get the most flexibility when you need to update and configure your fragment later.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="4d5cf-150">Sayfaya parça ekleme, kaldırma veya düzenleme</span><span class="sxs-lookup"><span data-stu-id="4d5cf-150">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="4d5cf-151">Aşağıdaki yordamlarda parçaların nasıl ekleneceği, kaldırılacağı ve düzenleneceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-151">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="4d5cf-152">Parça ekle</span><span class="sxs-lookup"><span data-stu-id="4d5cf-152">Add a fragment</span></span>

<span data-ttu-id="4d5cf-153">Bir sayfaya parça eklemek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-153">To add a fragment to a page, follow these steps.</span></span>

1. <span data-ttu-id="4d5cf-154">Soldaki ana hat bölmesinde veya doğrudan ana tuvalde, alt modüllerin eklenebileceği bir kapsayıcı veya yuva seçin.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-154">In the outline pane on the left or directly in the main canvas, select a container or slot to which child modules can be added.</span></span>
1. <span data-ttu-id="4d5cf-155">Çevrimiçi bölmesinde kapsayıcının veya yuvanın adının yanındaki üç noktayı (**...**) seçin.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-155">In the online pane, select the ellipsis (**...**) next to the name of the container or slot.</span></span>  <span data-ttu-id="4d5cf-156">Alternatif olarak, ana tuvali kullanıyorsanız artı simgesini (**+**) seçin.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-156">Alternately, if using the main canvas, select the plus symbol (**+**).</span></span>  
1. <span data-ttu-id="4d5cf-157">**Parça Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-157">Select **Add Fragment**.</span></span>

    ![Bir yuvaya veya kapsayıcıya varolan bir parçanın nasıl ekleneceği ile ilgili bir ekran yakalama](./media/add-fragment.png)
 
    > [!NOTE]
    > <span data-ttu-id="4d5cf-159">Bir konteyner veya yuva yeni alt modülleri desteklemiyorsa, **Parça Ekle** seçeneği kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-159">If the container or slot doesn't support new child modules, the **Add Fragment** option is unavailable.</span></span>
    
1. <span data-ttu-id="4d5cf-160">**Parça Ekle** iletişim kutusunda, eklenecek bir parça arayıp seçin.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-160">In the **Add Fragment** dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="4d5cf-161">Listelenmiş parça listelenmezse, önce seçilen konteyner veya yuvanın desteklediği bir modül türünden bir parça oluşturmanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-161">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="4d5cf-162">Seçili parça sayfanızdaki seçili konteynere veya yuvaya eklemek için istediğiniz parçayı seçin.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-162">Select your desired fragment to add it to the container or slot on your page.</span></span>

    ![Parça seçicinin kalıcı penceresindeki Ekran yakalaması](./media/fragment-picker.png)

> [!NOTE]
> <span data-ttu-id="4d5cf-164">Bir konteynerde veya bir yuvada izin verilen modüller, sayfa şablonu veya modüllerin kendi tanımları tarafından tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-164">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="4d5cf-165">Parça kaldırma</span><span class="sxs-lookup"><span data-stu-id="4d5cf-165">Remove a fragment</span></span>

<span data-ttu-id="4d5cf-166">Sayfada yuva veya konteynerden parça kaldırmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-166">To remove a fragment from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="4d5cf-167">Soldaki ana hat bölmesinde, kaldırılacak parçanın adının yanında üç nokta (**...**) düğmesini seçin ve çöp kutusu sembolünü seçin.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-167">In the outline pane on the left, select the ellipsis (**...**) next to the name of the fragment to be removed, and then select the trash can symbol.</span></span>  <span data-ttu-id="4d5cf-168">Alternatif olarak, parçayı tuval içinde seçebilir ve parçanın araç çubuğunda çöp kutusu sembolünü seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-168">Alternately, you can select the fragment in the canvas and select the trash can symbol in the fragment's toolbar.</span></span>
1. <span data-ttu-id="4d5cf-169">Parçayı kaldırma isteğinizi onaylamanız istendiğinde, **tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-169">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="4d5cf-170">Sayfadan bir parçayı kaldırdığınızda, yalnızca bu sayfadan gelen başvuruyu kaldırırsınız.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-170">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="4d5cf-171">Sitenizden parçayı **silmeyin**.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-171">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="4d5cf-172">Sitenizdeki parçaları silmek için, parça denetçisi Kullanıcı arabirimini (UI) kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-172">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="4d5cf-173">Bir sitedeki parçaları yalnızca herhangi bir sayfa, şablon veya başka parçalar tarafından başvurulmuyorsa silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-173">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="4d5cf-174">Parça Düzenle</span><span class="sxs-lookup"><span data-stu-id="4d5cf-174">Edit a fragment</span></span>

<span data-ttu-id="4d5cf-175">Parçaları düzenlemek için, parça düzenleyici kullanıcı arabimirni kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-175">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="4d5cf-176">Bu kısıtlama tasarımdan kaynaklanır.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-176">This restriction is by design.</span></span> <span data-ttu-id="4d5cf-177">Yazarların belirli bir sayfa için modülleri düzenleme işlemini, birçok sayfada paylaşılabilecek parça düzenleme işlemi ile karıştıradığından emin olmanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-177">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="4d5cf-178">Bir parça düzenlemek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-178">To edit a fragment, follow these steps.</span></span>

1. <span data-ttu-id="4d5cf-179">Soldaki gezinti bölmesinde **Parçalar** seçin.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-179">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="4d5cf-180">**Parçalar** altında düzenlenecek parçayı seçin.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-180">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="4d5cf-181">Parçanın modül özelliklerini ve yapısını gereksinim duyduğunuz şekilde Düzenle.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-181">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="4d5cf-182">İşlem, düzenleme modüllerinin sayfa düzenleyici görünümde düzenlenmesi işlemine benzer.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-182">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="4d5cf-183">Bir parçayı sayfada, şablonda veya üst parçada seçerek ve sağdaki Özellikler bölmesinde **parça Düzenle** 'yi seçerek düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d5cf-183">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4d5cf-184">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="4d5cf-184">Additional resources</span></span>

[<span data-ttu-id="4d5cf-185">Şablonlar ve düzenlere genel bakış</span><span class="sxs-lookup"><span data-stu-id="4d5cf-185">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="4d5cf-186">Şablonlarla çalışma</span><span class="sxs-lookup"><span data-stu-id="4d5cf-186">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="4d5cf-187">Önceden ayarlanmış düzenlerle çalışma</span><span class="sxs-lookup"><span data-stu-id="4d5cf-187">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="4d5cf-188">Yayınlama gruplarıyla çalışma</span><span class="sxs-lookup"><span data-stu-id="4d5cf-188">Work with publish groups</span></span>](publish-groups.md)
