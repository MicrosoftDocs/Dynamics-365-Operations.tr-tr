---
title: Modüllerle çalışma
description: Bu konu, Microsoft Dynamics 365 Commerce'ta modüllerin nasıl ve ne zaman kullanılacağını açıklamaktadır.
author: phinneyridge
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6d872719d3b1aa27ccfdcf36d7739c883e7b4996
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801373"
---
# <a name="work-with-modules"></a><span data-ttu-id="30fe1-103">Modüllerle çalışma</span><span class="sxs-lookup"><span data-stu-id="30fe1-103">Work with modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="30fe1-104">Bu konu, Microsoft Dynamics 365 Commerce'ta modüllerin nasıl ve ne zaman kullanılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="30fe1-104">This topic describes how and when to use modules in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="30fe1-105">Modüller, sayfa yapınızı oluşturan mantıksal yapı taşlarıdır ve çeşitli amaçlara ve kapsamlarına sahiptirler.</span><span class="sxs-lookup"><span data-stu-id="30fe1-105">Modules are logical building blocks that make up your page structure, and they have various purposes and scopes.</span></span> <span data-ttu-id="30fe1-106">Bazı modüller yüksek düzey konteynerlerdir ve bunların tek amacı diğer modülleri (alt modüller) tutmak ve düzenlemek içindir.</span><span class="sxs-lookup"><span data-stu-id="30fe1-106">Some modules are high-level containers, and their only purpose is to hold and organize other modules (child modules).</span></span> <span data-ttu-id="30fe1-107">Basit bir resim yerleşimi modülü gibi diğer modüller ise çok özel bir amaca sahiptir.</span><span class="sxs-lookup"><span data-stu-id="30fe1-107">Other modules, such as a simple image placement module, have a very specific purpose.</span></span> <span data-ttu-id="30fe1-108">Döngü modülü gibi diğer modüller ise bu iki kategori arasında bir yere denk düşen bir yer.</span><span class="sxs-lookup"><span data-stu-id="30fe1-108">Other modules, such as a carousel module, fall somewhere between those two categories.</span></span>

<span data-ttu-id="30fe1-109">Varsayılan olarak Dynamics 365 Commerce siteniz, temel e-ticaret senaryolarını elde etmenizi sağlayan bir modül kitaplığı içerir.</span><span class="sxs-lookup"><span data-stu-id="30fe1-109">By default, your Dynamics 365 Commerce site includes a module library that lets you achieve most basic e-Commerce scenarios.</span></span> <span data-ttu-id="30fe1-110">Bu modülleri kullanarak bir uçtan uca e-ticaret sitesi oluşturmak zorunda olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="30fe1-110">You should be able to construct an end-to-end e-Commerce site just by using these modules.</span></span> <span data-ttu-id="30fe1-111">Ancak, bu modülleri özelleştirmek veya belirli gereksinimler için yeni, özel modüller oluşturmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="30fe1-111">However, you might also want to customize these modules or build new, custom modules for specific needs.</span></span> <span data-ttu-id="30fe1-112">Özel modüller oluşturmak istiyorsanız özel bir modül kitaplığı oluşturmanıza yardımcı olacak bir modül tasarımı yazılım geliştirme seti (SDK) vardır.</span><span class="sxs-lookup"><span data-stu-id="30fe1-112">If you want to build custom modules, a module design software development kit (SDK) is available to help you create a custom module library.</span></span>

## <a name="container-modules-and-slots"></a><span data-ttu-id="30fe1-113">Konteyner modüller ve yuvalar</span><span class="sxs-lookup"><span data-stu-id="30fe1-113">Container modules and slots</span></span>

<span data-ttu-id="30fe1-114">Daha önce belirtildiği gibi bazı modüller alt modülleri tutacak şekilde tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="30fe1-114">As was mentioned earlier, some modules are designed to hold child modules.</span></span> <span data-ttu-id="30fe1-115">Bu modüller *konteyner* olarak bilinir ve iç içe geçmiş modül hiyerarşilerine izin verir.</span><span class="sxs-lookup"><span data-stu-id="30fe1-115">These modules are known as *containers*, and they allow for hierarchies of nested modules.</span></span> <span data-ttu-id="30fe1-116">Konteyner modüller *yuvalar* içerir.</span><span class="sxs-lookup"><span data-stu-id="30fe1-116">Container modules include *slots*.</span></span> <span data-ttu-id="30fe1-117">Yuvalar, konteynerdeki alt modüllerin düzenini ve amacını işlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="30fe1-117">Slots are used to handle the layout and purpose of child modules in the container.</span></span> <span data-ttu-id="30fe1-118">Aşağıda, çeşitli önemli yuvaların tanımlandığı, temel sayfa kapsayıcı modülü (herhangi bir sayfa için üst düzey modülüdür) yer alan bir örnek verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="30fe1-118">An example is a basic page container module (a top-level module for any page) that defines several important slots:</span></span>

- <span data-ttu-id="30fe1-119">Bir üstbilgi yuvası</span><span class="sxs-lookup"><span data-stu-id="30fe1-119">A header slot</span></span>
- <span data-ttu-id="30fe1-120">Bir alt başlık yuvası</span><span class="sxs-lookup"><span data-stu-id="30fe1-120">A sub-header slot</span></span>
- <span data-ttu-id="30fe1-121">Bir ana yuva</span><span class="sxs-lookup"><span data-stu-id="30fe1-121">A main slot</span></span>
- <span data-ttu-id="30fe1-122">Bir altbilgi yuvası</span><span class="sxs-lookup"><span data-stu-id="30fe1-122">A footer slot</span></span>
- <span data-ttu-id="30fe1-123">Bir alt bilgi yuvası</span><span class="sxs-lookup"><span data-stu-id="30fe1-123">A sub-footer slot</span></span>

<span data-ttu-id="30fe1-124">Modülün geliştiricisi bu yuvaları tanımlar ve hangi alt modüllerin ve kaç alt modülün doğrudan bunun içine koyulacağını belirler.</span><span class="sxs-lookup"><span data-stu-id="30fe1-124">The module's developer defines these slots, and determines which child modules and how many child modules can be put directly inside it.</span></span> <span data-ttu-id="30fe1-125">Örneğin, üstbilgi yuvası **üstbilgi modülü** türünün yalnızca bir modülünü destekleyebilir, oysa gövde yuvası herhangi bir türdeki (diğer sayfa kapsayıcı modüller dışında) sınırsız sayıda modülü destekleyebilir.</span><span class="sxs-lookup"><span data-stu-id="30fe1-125">For example, the header slot might support only one module of the **Header Module** type, whereas the body slot might support an unlimited number of modules of any type (except other page container modules).</span></span>

<span data-ttu-id="30fe1-126">Yazma araçlarında, sayfa yazarlarının her yuvaya hangi modüllerin konulacağını ve bunların ne koyabileceği konusunda bilinmesi gerekmez.</span><span class="sxs-lookup"><span data-stu-id="30fe1-126">In the authoring tools, page authors don't have to know in advance which modules can and can't be put in each slot.</span></span> <span data-ttu-id="30fe1-127">Sayfa yazarları bir yuva seçtikten sonra bu sayfaya eklenecek bir modül seçmeyi denediğinizde, bu yuva için desteklenen modül türlerinin filtrelenmiş bir görünümünü görürler.</span><span class="sxs-lookup"><span data-stu-id="30fe1-127">When page authors select a slot and then try to select a module to add to it, they see a filtered view of module types that are supported for that slot.</span></span>

## <a name="content-modules"></a><span data-ttu-id="30fe1-128">İçerik modülleri</span><span class="sxs-lookup"><span data-stu-id="30fe1-128">Content modules</span></span>

<span data-ttu-id="30fe1-129">İçerik modülleri, metin (ör., başlıklar, paragraflar ve bağlantılar) veya varlık başvuruları (ör., görüntüler, video ve PDF'ler) gibi içerik ve ortam öğeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="30fe1-129">Content modules contain content and media elements, such as text (for example, headlines, paragraphs, and links) or asset references (for example, images, video, and PDFs).</span></span> <span data-ttu-id="30fe1-130">Tipik içerik modülü türleri arasında içerik bloku, metin bloku ve promosyon başlık modülleri bulunur.</span><span class="sxs-lookup"><span data-stu-id="30fe1-130">Typical content module types include content block, text block, and promo banner modules.</span></span> <span data-ttu-id="30fe1-131">Bu üç tür modüller metin veya ortam içerebilir ve sayfada herhangi bir şeyin görünmesini sağlamak için alt modüller gerekmez.</span><span class="sxs-lookup"><span data-stu-id="30fe1-131">Modules of these three types can contain text or media, and they don't require any child modules to make something visible on a page.</span></span>

<span data-ttu-id="30fe1-132">Normal, günlük sayfa ve içerik yazma faaliyetlerinin büyük çoğunluğu içerik modüllerini içerir çünkü bu modüller, üst kapsayıcı modüllerinde işlenen gerçek içeriği tanımlar.</span><span class="sxs-lookup"><span data-stu-id="30fe1-132">The majority of typical, day-to-day page and content authoring activities involve content modules, primarily because these modules define the actual content that is rendered in their parent container modules.</span></span> <span data-ttu-id="30fe1-133">Birçok içerik modülü vardır ve bu modüller genellikle bir sayfanın iç içe modül hiyerarşisine ekleyebileceğiniz son taşlardır.</span><span class="sxs-lookup"><span data-stu-id="30fe1-133">Many content modules are available, and these modules are typically the last pieces that you will add to a page's hierarchy of nested modules.</span></span>

<span data-ttu-id="30fe1-134">Aşağıdaki şekil, modüllerin üst kapsayıcı modül yuvalarında nasıl iç içe geçmiş olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="30fe1-134">The following illustration shows how modules are nested inside parent container module slots.</span></span>

![İçe içe geçme modülleri](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a><span data-ttu-id="30fe1-136">Modül ekle veya kaldır</span><span class="sxs-lookup"><span data-stu-id="30fe1-136">Add or remove modules</span></span>

<span data-ttu-id="30fe1-137">Aşağıdaki yordamlarda modüllerin nasıl ekleneceği ve kaldırılacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="30fe1-137">The following procedures describe how to add and remove modules.</span></span>

### <a name="add-a-module"></a><span data-ttu-id="30fe1-138">Modül ekle</span><span class="sxs-lookup"><span data-stu-id="30fe1-138">Add a module</span></span>

<span data-ttu-id="30fe1-139">Sayfada yuv aveya konteynere modül eklemek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="30fe1-139">To add a module to a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="30fe1-140">Soldaki ana hat bölmesinde veya doğrudan ana tuvalde, alt modülün eklenebileceği bir kapsayıcı veya yuva seçin.</span><span class="sxs-lookup"><span data-stu-id="30fe1-140">In the outline pane on the left or directly in the main canvas, select a container or slot to which a child module can be added.</span></span>

    > [!NOTE]
    > <span data-ttu-id="30fe1-141">Modül tasarımcısı, belirli bir modül yuvasına eklenebilecek modül türlerinin listesini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="30fe1-141">The module designer defines the list of modules types that can be added to a specific module slot.</span></span> <span data-ttu-id="30fe1-142">Böylece, şablon yazarları, belirli bir şablondan oluşturulan tüm sayfalar için tutarlı arama motoru iyileştirmesi (SEO) ve geliştirme verimliliğini sağlamaya yardımcı olmak için izin verilen modül seçeneklerini geliştirebilirler.</span><span class="sxs-lookup"><span data-stu-id="30fe1-142">Template authors can then refine the allowed module options to help guarantee consistent search engine optimization (SEO) and authoring efficiency for all the pages that are built from a specific template.</span></span> <span data-ttu-id="30fe1-143">Bir yuvaya modül eklerken **Modül Ekle** iletişim kutusu, yalnızca seçili kapsayıcı veya yuvada desteklenen modülleri gösterecek şekilde otomatik olarak filtrelenir.</span><span class="sxs-lookup"><span data-stu-id="30fe1-143">When adding a module to a slot, the **Add Module** dialog box is automatically filtered so that it shows only modules that are supported in the selected container or slot.</span></span> <span data-ttu-id="30fe1-144">Bu izin verilen modüüller liste sisayfa şablonu veya kapsayıcı modülü tanımı tarafından belirlenir.</span><span class="sxs-lookup"><span data-stu-id="30fe1-144">This list of allowed modules is determined by the page's template or the container's module definition.</span></span>

1. <span data-ttu-id="30fe1-145">Ana hat bölmesini kullanıyorsanız, modül adının yanındaki üç noktayı (**...**) seçin ve sonra **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="30fe1-145">If using the outline pane, select the ellipsis (**...**) next to the module name, and then select **Add Module**.</span></span> <span data-ttu-id="30fe1-146">Denetimleri doğrudan tuval içinde kullanıyorsanız, boş bir yuvada veya seçili olan modüle bitişik olan artı sembolünü (**++**) seçin ve sonra **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="30fe1-146">If using the controls directly within the canvas, select the plus symbol (**+**) in an empty slot or adjacent to the currently selected module, and then select **Add Module**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="30fe1-147">Bir konteyner veya yuva yeni alt modülleri desteklemiyorsa, **Modül Ekle** seçeneği kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="30fe1-147">If a container or slot doesn't support new child modules, the **Add Module** option is unavailable.</span></span>

1. <span data-ttu-id="30fe1-148">**Modül Ekle** iletişim kutusunda, sayfanıza eklenecek bir modül arayıp seçin.</span><span class="sxs-lookup"><span data-stu-id="30fe1-148">In the **Add Module** dialog box, select a module to add to your page.</span></span>

    > [!TIP]
    > <span data-ttu-id="30fe1-149">**İçerik bloku**, yeni başlayanların çalışması için iyi bir modüldür.</span><span class="sxs-lookup"><span data-stu-id="30fe1-149">**Content block** is a good module type for beginners to work with.</span></span>

1. <span data-ttu-id="30fe1-150">Seçili modülü sayfanızdaki seçili konteynere veya yuvaya eklemek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="30fe1-150">Select **OK** to add the selected module to the selected container or slot on your page.</span></span>

### <a name="remove-a-module"></a><span data-ttu-id="30fe1-151">Modül kaldırma</span><span class="sxs-lookup"><span data-stu-id="30fe1-151">Remove a module</span></span>

<span data-ttu-id="30fe1-152">Sayfada yuva veya konteynerden modül kaldırmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="30fe1-152">To remove a module from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="30fe1-153">Soldaki ana hat bölmesinde, kaldırılacak modülün adının yanında üç nokta (**...**) düğmesini seçin ve çöp kutusu sembolünü seçin.</span><span class="sxs-lookup"><span data-stu-id="30fe1-153">In the outline pane on the left, select the ellipsis (**...**) next to the name of the module to be removed, and then select the trash can symbol.</span></span> <span data-ttu-id="30fe1-154">Alternatif olarak, ana tuval içinde, seçili bir modülün araç çubuğunda çöp kutusu sembolünü seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="30fe1-154">Alternately, in the main canvas you can select the trash can symbol on a selected module's toolbar.</span></span>
1. <span data-ttu-id="30fe1-155">Modülü kaldırma isteğinizi onaylamanız istendiğinde, **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="30fe1-155">When prompted to confirm that you want to remove the module, select **OK**.</span></span>

## <a name="move-a-module-to-a-new-position"></a><span data-ttu-id="30fe1-156">Mobülü yeni bir konuma taşıma</span><span class="sxs-lookup"><span data-stu-id="30fe1-156">Move a module to a new position</span></span>

<span data-ttu-id="30fe1-157">Bir modülü sayfanızda yeni bir konuma taşımak için aşağıdaki yöntemlerden birini kullanın.</span><span class="sxs-lookup"><span data-stu-id="30fe1-157">To move a module to a new position within your page, use any of the following methods.</span></span>

### <a name="move-a-module-using-the-outline-pane"></a><span data-ttu-id="30fe1-158">Bir modülü ana hat bölmesini kullanarak taşıma</span><span class="sxs-lookup"><span data-stu-id="30fe1-158">Move a module using the outline pane</span></span>

<span data-ttu-id="30fe1-159">Bir modülü ana hat bölmesini kullanarak taşımak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="30fe1-159">To move a module using the outline pane, follow these steps.</span></span>

1. <span data-ttu-id="30fe1-160">Ana hat bölmesinde taşımak istediğiniz modülü seçin ve tutun, sonra modülü ana hatta yeni bir konuma sürükleyin.</span><span class="sxs-lookup"><span data-stu-id="30fe1-160">Select and hold the module you want to move in the outline pane, then drag the module to a new position in the outline.</span></span> <span data-ttu-id="30fe1-161">Ana hattaki ve tuvaldeki mavi çizgi modülün nereye yerleştirilebileceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="30fe1-161">The blue line in the outline and on the canvas indicates where the module can be placed.</span></span>
1. <span data-ttu-id="30fe1-162">Yeni pozisyona bırakmak için modülü serbest bırakın.</span><span class="sxs-lookup"><span data-stu-id="30fe1-162">Release the module to drop it into the new position.</span></span>

### <a name="move-a-module-directly-within-the-canvas"></a><span data-ttu-id="30fe1-163">Modülü doğrudan tuval içinde taşıma</span><span class="sxs-lookup"><span data-stu-id="30fe1-163">Move a module directly within the canvas</span></span>

<span data-ttu-id="30fe1-164">Bir modülü doğrudan tuval içinde taşımak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="30fe1-164">To move a module directly within the canvas, follow these steps.</span></span>

1. <span data-ttu-id="30fe1-165">Tuvalde taşımak istediğiniz modülü seçin.</span><span class="sxs-lookup"><span data-stu-id="30fe1-165">Select the module you want to move in the canvas.</span></span> 
1. <span data-ttu-id="30fe1-166">Modülün araç çubuğunda yukarı veya aşağı doğru bir ok sembolü seçin ve sonra oku sayfada yeni bir konuma sürükleyin.</span><span class="sxs-lookup"><span data-stu-id="30fe1-166">Select either an upward or downward pointing arrow symbol in the module's toolbar, and then drag the arrow to a new position on the page.</span></span> <span data-ttu-id="30fe1-167">Tuval ve ana hattaki mavi çizgi modülün nereye yerleştirilebileceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="30fe1-167">The blue line in the canvas and outline indicates where the module can be placed.</span></span> <span data-ttu-id="30fe1-168">Bir modül yukarı veya aşağı taşınamayacağı takdirde o ok sembolü gri kalır.</span><span class="sxs-lookup"><span data-stu-id="30fe1-168">If a module cannot be moved up or down, that arrow symbol will be grayed out.</span></span> 
1. <span data-ttu-id="30fe1-169">Yeni pozisyona bırakmak için modülü serbest bırakın.</span><span class="sxs-lookup"><span data-stu-id="30fe1-169">Release the module to drop it into the new position.</span></span>

### <a name="move-a-module-using-the-ellipsis-menu"></a><span data-ttu-id="30fe1-170">Bir modülü üç nokta menüsünü kullanarak taşıma</span><span class="sxs-lookup"><span data-stu-id="30fe1-170">Move a module using the ellipsis menu</span></span>

<span data-ttu-id="30fe1-171">Bir modülü üç nokta menüsünü kullanarak taşımak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="30fe1-171">To move a module using the ellipsis menu, follow these steps.</span></span>

1. <span data-ttu-id="30fe1-172">Ana hattan veya tuval içinden bir modül seçin.</span><span class="sxs-lookup"><span data-stu-id="30fe1-172">Select a module in either the outline or the canvas.</span></span>
1. <span data-ttu-id="30fe1-173">Ana hat bölmesinde modül adının yanındaki veya tuval içinde modülün araç çubuğundaki üç noktayı (**...**) seçin.</span><span class="sxs-lookup"><span data-stu-id="30fe1-173">Select the ellipsis (**...**) next to the module's name in the outline pane, or in the module's toolbar in the canvas.</span></span>
1. <span data-ttu-id="30fe1-174">Modül, kapsayıcı veya yuva içinde yukarı veya aşağı taşınacaksa, **Yukarı** veya **Aşağı** seçeneklerini görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="30fe1-174">If the module can be moved up or down within the container or slot, you will see options for **Move up** or **Move down**.</span></span> <span data-ttu-id="30fe1-175">Modülü, alt öğelerine göre yukarı veya aşağı taşımak için istenen taşıma seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="30fe1-175">Select the desired move option to move the module up or down relative to its siblings.</span></span>

## <a name="configure-modules"></a><span data-ttu-id="30fe1-176">Modülleri konfigüre et</span><span class="sxs-lookup"><span data-stu-id="30fe1-176">Configure modules</span></span>

<span data-ttu-id="30fe1-177">Aşağıdaki yordamlarda içerik ve konteyner modüllerin nasıl yapılandırılacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="30fe1-177">The following procedures describe how to configure content and container modules.</span></span>

### <a name="configure-a-content-module"></a><span data-ttu-id="30fe1-178">Bir içerik modülü konfigüre edin</span><span class="sxs-lookup"><span data-stu-id="30fe1-178">Configure a content module</span></span>

<span data-ttu-id="30fe1-179">Sayfada bir içerik modülünü konfigüre etmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="30fe1-179">To configure a content module on a page, follow these steps.</span></span>

1. <span data-ttu-id="30fe1-180">Soldaki ana hat bölmesinde ağacı genişletin ve herhangi bir içerik modülünü seçin (örneğin, **İçerik bloku**).</span><span class="sxs-lookup"><span data-stu-id="30fe1-180">In the outline pane on the left, expand the tree and select any content module (for example, **Content block**).</span></span> <span data-ttu-id="30fe1-181">Alternatif olarak modülü ana tuvalde de seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="30fe1-181">Alternately, you can select the module in the main canvas.</span></span>
1. <span data-ttu-id="30fe1-182">Sağdaki modül özellikleri bölmesinde istenen modül denetimlerinin özelliklerini girin.</span><span class="sxs-lookup"><span data-stu-id="30fe1-182">In the module properties pane on the right, enter properties for any desired module controls.</span></span>
1. <span data-ttu-id="30fe1-183">Komut satırında **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="30fe1-183">On the command bar, select **Save**.</span></span> <span data-ttu-id="30fe1-184">Bu, önizleme tuvalini de yenilenecek.</span><span class="sxs-lookup"><span data-stu-id="30fe1-184">This will also refresh the preview canvas.</span></span>

### <a name="edit-module-text-properties"></a><span data-ttu-id="30fe1-185">Modül metni özelliklerini düzenleme</span><span class="sxs-lookup"><span data-stu-id="30fe1-185">Edit module text properties</span></span>

<span data-ttu-id="30fe1-186">Salt okunur olmayan modül metni özellikleri doğrudan tuval içinde düzenlenebilir.</span><span class="sxs-lookup"><span data-stu-id="30fe1-186">Module text properties that are not read-only can be edited directly in the canvas.</span></span>

<span data-ttu-id="30fe1-187">Modül metni özelliklerini düzenlemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="30fe1-187">To edit module text properties, follow these steps.</span></span>

1. <span data-ttu-id="30fe1-188">Tuvaldeki metin denetimini seçin ve sonra imlecinizi metni düzenlemek istediğiniz yere getirin.</span><span class="sxs-lookup"><span data-stu-id="30fe1-188">Select the text control in the canvas, then place your cursor where you wish to edit text.</span></span>
1. <span data-ttu-id="30fe1-189">Metin içeriğinizi girin.</span><span class="sxs-lookup"><span data-stu-id="30fe1-189">Enter your text content.</span></span>
1. <span data-ttu-id="30fe1-190">Diğer içeriği düzenlemeye devam etmek için metin içeriğinin dışında bir yeri seçin.</span><span class="sxs-lookup"><span data-stu-id="30fe1-190">Select anywhere outside the text content to continue editing other content.</span></span>

### <a name="inline-image-selection"></a><span data-ttu-id="30fe1-191">Satır içi resim seçimi</span><span class="sxs-lookup"><span data-stu-id="30fe1-191">Inline image selection</span></span>

<span data-ttu-id="30fe1-192">Salt okunur olmayan modül resimleri doğrudan tuvalden değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="30fe1-192">Module images that are not read-only can be changed directly from the canvas.</span></span>

<span data-ttu-id="30fe1-193">Bir içerik modülüne yönelik yeni bir resim seçmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="30fe1-193">To choose a new image for a content module, follow these steps.</span></span>

1. <span data-ttu-id="30fe1-194">Tuval içinde, resme çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="30fe1-194">In the canvas, double-click the image.</span></span> <span data-ttu-id="30fe1-195">Bu, ortam seçici penceresini açar.</span><span class="sxs-lookup"><span data-stu-id="30fe1-195">This will bring up the media picker window.</span></span>
1. <span data-ttu-id="30fe1-196">Kullanmak istediğiniz yeni bir resmi bulup seçin ve **Tamam'ı** seçin.</span><span class="sxs-lookup"><span data-stu-id="30fe1-196">Find and select a new image you want to use, and then select **OK**.</span></span> <span data-ttu-id="30fe1-197">Yeni resim tuval içinde işlenir.</span><span class="sxs-lookup"><span data-stu-id="30fe1-197">The new image is now rendered in the canvas.</span></span>

### <a name="configure-a-container-module"></a><span data-ttu-id="30fe1-198">Konteyner modülü yapılandırma</span><span class="sxs-lookup"><span data-stu-id="30fe1-198">Configure a container module</span></span>

<span data-ttu-id="30fe1-199">Sayfada bir konteyner modülünü konfigüre etmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="30fe1-199">To configure a container module on a page, follow these steps.</span></span>

1. <span data-ttu-id="30fe1-200">Sayfanızda bir konteyner modülü seçin (örneğin, bir döngü veya sıvı konteyner modülü).</span><span class="sxs-lookup"><span data-stu-id="30fe1-200">Select a container module on your page (for example, a carousel or fluid container module).</span></span>
1. <span data-ttu-id="30fe1-201">Sağdaki Özellikler bölmesinde, üst bilgileri seçerek iç içe geçmiş denetimleri genişletin ve gerekli tüm denetim değerlerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="30fe1-201">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="30fe1-202">Soldaki anahat bölmesinde, konteyner veya konteyner içindeki yuvalardan birinin adının yanında üç nokta düğmesini seçin ve **Modül ekle** yi seçin.</span><span class="sxs-lookup"><span data-stu-id="30fe1-202">In the outline pane on the left, select the ellipsis button next to the name of either the container or any slots inside the container, and then select **Add Module**.</span></span> <span data-ttu-id="30fe1-203">Daha sonra seçili konteynere alt modüller ekleyin.</span><span class="sxs-lookup"><span data-stu-id="30fe1-203">Then, add child modules to the selected container.</span></span> <span data-ttu-id="30fe1-204">Daha fazla bilgi için bu konunun önceki [Modüllerle çalış](#add-a-module) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="30fe1-204">For more information, see the [Work with modules](#add-a-module) section earlier in this topic.</span></span>
1. <span data-ttu-id="30fe1-205">Bir üst kapsayıcıda eş öğe olarak birden fazla alt modül varsa, bunların görüntüleme sıralarını üst konteynerde değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="30fe1-205">If multiple child modules exist as siblings in a parent container, you can change their display order in the parent container.</span></span> <span data-ttu-id="30fe1-206">Modül için üç nokta düğmesini seçin ve sonra yukarı ok ve aşağı ok düğmelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="30fe1-206">Select the ellipsis button for a module, and then use the up arrow and down arrow buttons.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="30fe1-207">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="30fe1-207">Additional resources</span></span>

[<span data-ttu-id="30fe1-208">Şablonlar ve düzenlere genel bakış</span><span class="sxs-lookup"><span data-stu-id="30fe1-208">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="30fe1-209">Şablonlarla çalışma</span><span class="sxs-lookup"><span data-stu-id="30fe1-209">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="30fe1-210">Önceden ayarlanmış düzenlerle çalışma</span><span class="sxs-lookup"><span data-stu-id="30fe1-210">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="30fe1-211">Parçalarla çalışma</span><span class="sxs-lookup"><span data-stu-id="30fe1-211">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="30fe1-212">Sayfaya konteyner modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="30fe1-212">Add a container module to a page</span></span>](add-container-module.md)

[<span data-ttu-id="30fe1-213">Yayımlama gruplarıyla çalışma</span><span class="sxs-lookup"><span data-stu-id="30fe1-213">Work with publish groups</span></span>](publish-groups.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
