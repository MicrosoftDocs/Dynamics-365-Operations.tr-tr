---
title: Modüllerle çalışma
description: Bu konu, Microsoft Dynamics 365 Commerce'ta modüllerin nasıl ve ne zaman kullanılacağını açıklamaktadır.
author: v-chgri
manager: annbe
ms.date: 01/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 769d6754fa944830b989d657e0dad9cc42212932
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025891"
---
# <a name="work-with-modules"></a><span data-ttu-id="646c7-103">Modüllerle çalışma</span><span class="sxs-lookup"><span data-stu-id="646c7-103">Work with modules</span></span>

<span data-ttu-id="646c7-104">Bu konu, Microsoft Dynamics 365 Commerce'ta modüllerin nasıl ve ne zaman kullanılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="646c7-104">This topic describes how and when to use modules in Microsoft Dynamics 365 Commerce.</span></span>


[!include [banner](includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="646c7-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="646c7-105">Overview</span></span>

<span data-ttu-id="646c7-106">Modüller, sayfa yapınızı oluşturan mantıksal yapı taşlarıdır ve çeşitli amaçlara ve kapsamlarına sahiptirler.</span><span class="sxs-lookup"><span data-stu-id="646c7-106">Modules are logical building blocks that make up your page structure, and they have various purposes and scopes.</span></span> <span data-ttu-id="646c7-107">Bazı modüller yüksek düzey konteynerlerdir ve bunların tek amacı diğer modülleri (alt modüller) tutmak ve düzenlemek içindir.</span><span class="sxs-lookup"><span data-stu-id="646c7-107">Some modules are high-level containers, and their only purpose is to hold and organize other modules (child modules).</span></span> <span data-ttu-id="646c7-108">Basit bir resim yerleşimi modülü gibi diğer modüller ise çok özel bir amaca sahiptir.</span><span class="sxs-lookup"><span data-stu-id="646c7-108">Other modules, such as a simple image placement module, have a very specific purpose.</span></span> <span data-ttu-id="646c7-109">Döngü modülü gibi diğer modüller ise bu iki kategori arasında bir yere denk düşen bir yer.</span><span class="sxs-lookup"><span data-stu-id="646c7-109">Other modules, such as a carousel module, fall somewhere between those two categories.</span></span>

<span data-ttu-id="646c7-110">Varsayılan olarak Dynamics 365 Commerce siteniz, temel e-ticaret senaryolarını elde etmenizi sağlayan bir başlangıç kiti modül kitaplığı içerir.</span><span class="sxs-lookup"><span data-stu-id="646c7-110">By default, your Dynamics 365 Commerce site includes a starter kit module library that lets you achieve most basic e-Commerce scenarios.</span></span> <span data-ttu-id="646c7-111">Bu modülleri kullanarak bir uçtan uca e-ticaret sitesi oluşturmak zorunda olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="646c7-111">You should be able to construct an end-to-end e-Commerce site just by using these modules.</span></span> <span data-ttu-id="646c7-112">Ancak, bu modülleri özelleştirmek veya belirli gereksinimler için yeni, özel modüller oluşturmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="646c7-112">However, you might also want to customize these modules or build new, custom modules for specific needs.</span></span> <span data-ttu-id="646c7-113">Özel modüller oluşturmak istiyorsanız özel bir modül kitaplığı oluşturmanıza yardımcı olacak bir modül tasarımı yazılım geliştirme seti (SDK) vardır.</span><span class="sxs-lookup"><span data-stu-id="646c7-113">If you want to build custom modules, a module design software development kit (SDK) is available to help you create a custom module library.</span></span>

## <a name="container-modules-and-slots"></a><span data-ttu-id="646c7-114">Konteyner modüller ve yuvalar</span><span class="sxs-lookup"><span data-stu-id="646c7-114">Container modules and slots</span></span>

<span data-ttu-id="646c7-115">Daha önce belirtildiği gibi bazı modüller alt modülleri tutacak şekilde tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="646c7-115">As was mentioned earlier, some modules are designed to hold child modules.</span></span> <span data-ttu-id="646c7-116">Bu modüller *konteyner* olarak bilinir ve iç içe geçmiş modül hiyerarşilerine izin verir.</span><span class="sxs-lookup"><span data-stu-id="646c7-116">These modules are known as *containers*, and they allow for hierarchies of nested modules.</span></span> <span data-ttu-id="646c7-117">Konteyner modüller *yuvalar* içerir.</span><span class="sxs-lookup"><span data-stu-id="646c7-117">Container modules include *slots*.</span></span> <span data-ttu-id="646c7-118">Yuvalar, konteynerdeki alt modüllerin düzenini ve amacını işlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="646c7-118">Slots are used to handle the layout and purpose of child modules in the container.</span></span> <span data-ttu-id="646c7-119">Aşağıda, çeşitli önemli yuvaların tanımlandığı, temel sayfa kapsayıcı modülü (herhangi bir sayfa için üst düzey modülüdür) yer alan bir örnek verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="646c7-119">An example is a basic page container module (a top-level module for any page) that defines several important slots:</span></span>

- <span data-ttu-id="646c7-120">Bir üstbilgi yuvası</span><span class="sxs-lookup"><span data-stu-id="646c7-120">A header slot</span></span>
- <span data-ttu-id="646c7-121">Bir gövde yuvası</span><span class="sxs-lookup"><span data-stu-id="646c7-121">A body slot</span></span>
- <span data-ttu-id="646c7-122">Bir altbilgi yuvası</span><span class="sxs-lookup"><span data-stu-id="646c7-122">A footer slot</span></span>

<span data-ttu-id="646c7-123">Modülün geliştiricisi bu yuvaları tanımlar ve hangi alt modüllerin ve kaç alt modülün doğrudan bunun içine koyulacağını belirler.</span><span class="sxs-lookup"><span data-stu-id="646c7-123">The module's developer defines these slots, and determines which child modules and how many child modules can be put directly inside it.</span></span> <span data-ttu-id="646c7-124">Örneğin, üstbilgi yuvası **üstbilgi modülü** türünün yalnızca bir modülünü destekleyebilir, oysa gövde yuvası herhangi bir türdeki (diğer sayfa kapsayıcı modüller dışında) sınırsız sayıda modülü destekleyebilir.</span><span class="sxs-lookup"><span data-stu-id="646c7-124">For example, the header slot might support only one module of the **Header Module** type, whereas the body slot might support an unlimited number of modules of any type (except other page container modules).</span></span>

<span data-ttu-id="646c7-125">Yazma araçlarında, sayfa yazarlarının her yuvaya hangi modüllerin konulacağını ve bunların ne koyabileceği konusunda bilinmesi gerekmez.</span><span class="sxs-lookup"><span data-stu-id="646c7-125">In the authoring tools, page authors don't have to know in advance which modules can and can't be put in each slot.</span></span> <span data-ttu-id="646c7-126">Sayfa yazarları bir yuva seçtikten sonra bu sayfaya eklenecek bir modül seçmeyi denediğinizde, bu yuva için desteklenen modül türlerinin filtrelenmiş bir görünümünü görürler.</span><span class="sxs-lookup"><span data-stu-id="646c7-126">When page authors select a slot and then try to select a module to add to it, they see a filtered view of module types that are supported for that slot.</span></span>

## <a name="content-modules"></a><span data-ttu-id="646c7-127">İçerik modülleri</span><span class="sxs-lookup"><span data-stu-id="646c7-127">Content modules</span></span>

<span data-ttu-id="646c7-128">İçerik modülleri, metin (ör., başlıklar, paragraflar ve bağlantılar) veya varlık başvuruları (ör., görüntüler, video ve PDF'ler) gibi içerik ve ortam öğeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="646c7-128">Content modules contain content and media elements, such as text (for example, headlines, paragraphs, and links) or asset references (for example, images, video, and PDFs).</span></span> <span data-ttu-id="646c7-129">Tipik içerik modülü türlerine örnek olarak **Her**, **Özellik** ve **Ana başlık** verilebilir.</span><span class="sxs-lookup"><span data-stu-id="646c7-129">Examples of typical content module types are **Hero**, **Feature**, and **Banner**.</span></span> <span data-ttu-id="646c7-130">Bu üç tür modüller metin veya ortam içerebilir ve sayfada herhangi bir şeyin görünmesini sağlamak için alt modüller gerekmez.</span><span class="sxs-lookup"><span data-stu-id="646c7-130">Modules of these three types can contain text or media, and they don't require any child modules to make something visible on a page.</span></span>

<span data-ttu-id="646c7-131">Normal, günlük sayfa ve içerik yazma faaliyetlerinin büyük çoğunluğu içerik modüllerini içerir çünkü bu modüller, üst kapsayıcı modüllerinde işlenen gerçek içeriği tanımlar.</span><span class="sxs-lookup"><span data-stu-id="646c7-131">The majority of typical, day-to-day page and content authoring activities involve content modules, primarily because these modules define the actual content that is rendered in their parent container modules.</span></span> <span data-ttu-id="646c7-132">Birçok içerik modülü vardır ve bu modüller genellikle bir sayfanın iç içe modül hiyerarşisine ekleyebileceğiniz son taşlardır.</span><span class="sxs-lookup"><span data-stu-id="646c7-132">Many content modules are available, and these modules are typically the last pieces that you will add to a page's hierarchy of nested modules.</span></span>

<span data-ttu-id="646c7-133">Aşağıdaki şekil, modüllerin üst kapsayıcı modül yuvalarında nasıl iç içe geçmiş olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="646c7-133">The following illustration shows how modules are nested inside parent container module slots.</span></span>

![İçe içe geçme modülleri](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a><span data-ttu-id="646c7-135">Modül ekle veya kaldır</span><span class="sxs-lookup"><span data-stu-id="646c7-135">Add or remove modules</span></span>

<span data-ttu-id="646c7-136">Aşağıdaki yordamlarda modüllerin nasıl ekleneceği ve kaldırılacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="646c7-136">The following procedures describe how to add and remove modules.</span></span>

### <a name="add-a-module"></a><span data-ttu-id="646c7-137">Modül ekle</span><span class="sxs-lookup"><span data-stu-id="646c7-137">Add a module</span></span>

<span data-ttu-id="646c7-138">Sayfada yuv aveya konteynere modül eklemek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="646c7-138">To add a module to a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="646c7-139">Soldaki anahat bölmesinde, alt modülün eklenebileceği bir konteyner veya yuva seçin.</span><span class="sxs-lookup"><span data-stu-id="646c7-139">In the outline pane on the left, select a container or slot that a child module can be added to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="646c7-140">Modül tasarımcısı, belirli bir modül yuvasına eklenebilecek modül türlerinin listesini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="646c7-140">The module designer defines the list of modules types that can be added to a specific module slot.</span></span> <span data-ttu-id="646c7-141">Böylece, şablon yazarları, belirli bir şablondan oluşturulan tüm sayfalar için tutarlı arama motoru iyileştirmesi (SEO) ve geliştirme verimliliğini sağlamaya yardımcı olmak için izin verilen modül seçeneklerini geliştirebilirler.</span><span class="sxs-lookup"><span data-stu-id="646c7-141">Template authors can then refine the allowed module options to help guarantee consistent search engine optimization (SEO) and authoring efficiency for all the pages pages that are built from a specific template.</span></span>

1. <span data-ttu-id="646c7-142">Modül için üç nokta düğmesini (**...**) seçin ve sonra **Modül ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="646c7-142">Select the ellipsis button (**...**) for the module, and then select **Add Module**.</span></span> <span data-ttu-id="646c7-143">**Modül Ekle** iletişim kutusu görünür.</span><span class="sxs-lookup"><span data-stu-id="646c7-143">The **Add Module** dialog box appears.</span></span> <span data-ttu-id="646c7-144">Yalnızca seçili konteynerde veya yuvada desteklenen modüller görünür şekilde bu iletişim kutusuna otomatik olarak filtre uygulanır.</span><span class="sxs-lookup"><span data-stu-id="646c7-144">This dialog box is automatically filtered so that it shows only modules that are supported in the selected container or slot.</span></span> <span data-ttu-id="646c7-145">Modül listesi sayfa şablonu veya konteyner modülü tanımı tarafından belirlenir.</span><span class="sxs-lookup"><span data-stu-id="646c7-145">The list of modules is determined by the page's template or the container module definition.</span></span>

    > [!NOTE]
    > <span data-ttu-id="646c7-146">Bir konteyner veya yuva yeni alt modülleri desteklemiyorsa, **Modül Ekle** seçeneği kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="646c7-146">If a container or slot doesn't support new child modules, the **Add Module** option is unavailable.</span></span>

1. <span data-ttu-id="646c7-147">İletişim kutusunda, sayfanıza eklenecek bir modül arayıp seçin.</span><span class="sxs-lookup"><span data-stu-id="646c7-147">In the dialog box, search for and select a module to add to your page.</span></span>

    > [!TIP]
    > <span data-ttu-id="646c7-148">**Özellik** ve **Hero** yeni başlayanlar için daha iyi modül türleridir.</span><span class="sxs-lookup"><span data-stu-id="646c7-148">**Feature** and **Hero** are good module types for beginners to work with.</span></span>

1. <span data-ttu-id="646c7-149">Seçili modülü sayfanızdaki seçili konteynere veya yuvaya eklemek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="646c7-149">Select **OK** to add the selected module to the selected container or slot on your page.</span></span>

### <a name="remove-a-module"></a><span data-ttu-id="646c7-150">Modül kaldırma</span><span class="sxs-lookup"><span data-stu-id="646c7-150">Remove a module</span></span>

<span data-ttu-id="646c7-151">Sayfada yuva veya konteynerden modül kaldırmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="646c7-151">To remove a module from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="646c7-152">Soldaki anahat bölmesinde, kaldırılacak modülün adının yanında üç nokta düğmesini seçin ve çöp tenekesi düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="646c7-152">In the outline pane on the left, select the ellipsis button next to the name of the module to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="646c7-153">Modülü kaldırma isteğinizi onaylamanız istendiğinde, **tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="646c7-153">When you're prompted to confirm that you want to remove the module, select **OK**.</span></span>

## <a name="configure-modules"></a><span data-ttu-id="646c7-154">Modülleri konfigüre et</span><span class="sxs-lookup"><span data-stu-id="646c7-154">Configure modules</span></span>

<span data-ttu-id="646c7-155">Aşağıdaki yordamlarda içerik ve konteyner modüllerin nasıl yapılandırılacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="646c7-155">The following procedures describe how to configure content and container modules.</span></span>

### <a name="configure-a-content-module"></a><span data-ttu-id="646c7-156">Bir içerik modülü konfigüre edin</span><span class="sxs-lookup"><span data-stu-id="646c7-156">Configure a content module</span></span>

<span data-ttu-id="646c7-157">Sayfada bir içerik modülünü konfigüre etmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="646c7-157">To configure a content module on a page, follow these steps.</span></span>

1. <span data-ttu-id="646c7-158">Soldaki anahat bölmesinde ağacı genişletin ve bir içerik modülü türü seçin ( Örneğin, **özellik**, **hero** veya **başlık**).</span><span class="sxs-lookup"><span data-stu-id="646c7-158">In the outline pane on the left, expand the tree and select any content module (for example, **Feature**, **Hero**, or **Banner**).</span></span>
1. <span data-ttu-id="646c7-159">Sağdaki özellikler bölmesinde, modülün içerik ve ayarlar denetimlerini bulun.</span><span class="sxs-lookup"><span data-stu-id="646c7-159">In the properties pane on the right, find the module's content and settings controls.</span></span>
1. <span data-ttu-id="646c7-160">İstenen modül denetimlerinin özelliklerini girin.</span><span class="sxs-lookup"><span data-stu-id="646c7-160">Enter properties for any desired module controls.</span></span>
1. <span data-ttu-id="646c7-161">Komut çubuğunda **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="646c7-161">Select **Save** in the command bar.</span></span> <span data-ttu-id="646c7-162">Bu, önizleme tuvalini de yenilenecek.</span><span class="sxs-lookup"><span data-stu-id="646c7-162">This will also refresh the preview canvas.</span></span>

### <a name="configure-a-container-module"></a><span data-ttu-id="646c7-163">Konteyner modülü yapılandırma</span><span class="sxs-lookup"><span data-stu-id="646c7-163">Configure a container module</span></span>

<span data-ttu-id="646c7-164">Sayfada bir konteyner modülünü konfigüre etmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="646c7-164">To configure a container module on a page, follow these steps.</span></span>

1. <span data-ttu-id="646c7-165">Sayfanızda bir konteyner modülü seçin (örneğin, bir döngü veya sıvı konteyner modülü).</span><span class="sxs-lookup"><span data-stu-id="646c7-165">Select a container module on your page (for example, a carousel or fluid container module).</span></span>
1. <span data-ttu-id="646c7-166">Sağdaki Özellikler bölmesinde, üst bilgileri seçerek iç içe geçmiş denetimleri genişletin ve gerekli tüm denetim değerlerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="646c7-166">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="646c7-167">Soldaki anahat bölmesinde, konteyner veya konteyner içindeki yuvalardan birinin adının yanında üç nokta düğmesini seçin ve **Modül ekle**yi seçin.</span><span class="sxs-lookup"><span data-stu-id="646c7-167">In the outline pane on the left, select the ellipsis button next to the name of either the container or any slots inside the container, and then select **Add Module**.</span></span> <span data-ttu-id="646c7-168">Daha sonra seçili konteynere alt modüller ekleyin.</span><span class="sxs-lookup"><span data-stu-id="646c7-168">Then, add child modules to the selected container.</span></span> <span data-ttu-id="646c7-169">Daha fazla bilgi için bu konunun önceki [Modüllerle çalış](#add-a-module) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="646c7-169">For more information, see the [Work with modules](#add-a-module) section earlier in this topic.</span></span>
1. <span data-ttu-id="646c7-170">Bir üst kapsayıcıda eş öğe olarak birden fazla alt modül varsa, bunların görüntüleme sıralarını üst konteynerde değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="646c7-170">If multiple child modules exist as siblings in a parent container, you can change their display order in the parent container.</span></span> <span data-ttu-id="646c7-171">Modül için üç nokta düğmesini seçin ve sonra yukarı ok ve aşağı ok düğmelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="646c7-171">Select the ellipsis button for a module, and then use the up arrow and down arrow buttons.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="646c7-172">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="646c7-172">Additional resources</span></span>

[<span data-ttu-id="646c7-173">Şablonlar ve düzenlere genel bakış</span><span class="sxs-lookup"><span data-stu-id="646c7-173">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="646c7-174">Şablonlarla çalışma</span><span class="sxs-lookup"><span data-stu-id="646c7-174">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="646c7-175">Önceden ayarlanmış düzenlerle çalışma</span><span class="sxs-lookup"><span data-stu-id="646c7-175">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="646c7-176">Parçalarla çalışma</span><span class="sxs-lookup"><span data-stu-id="646c7-176">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="646c7-177">Sayfaya konteyner modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="646c7-177">Add a container module to a page</span></span>](add-container-module.md)

[<span data-ttu-id="646c7-178">Yayımlama gruplarıyla çalışma</span><span class="sxs-lookup"><span data-stu-id="646c7-178">Work with publish groups</span></span>](publish-groups.md)

