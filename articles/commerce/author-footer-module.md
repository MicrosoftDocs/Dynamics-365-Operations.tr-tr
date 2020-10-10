---
title: Alt bilgi modülü
description: Bu konu altbilgi modüllerini ve bunların nasıl Dynamics 365 Commerce içine yazılacağını kapsamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 42a71ea9498461febca80952acc3158517918332
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/16/2020
ms.locfileid: "3816973"
---
# <a name="footer-module"></a><span data-ttu-id="b363f-103">Alt bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="b363f-103">Footer module</span></span>  

[!include [banner](includes/banner.md)]

<span data-ttu-id="b363f-104">Bu konu altbilgi modüllerini ve bunların nasıl Microsoft Dynamics 365 Commerce'te oluşturacağını açıklamaktadır ve kapsamaktadır.</span><span class="sxs-lookup"><span data-stu-id="b363f-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b363f-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="b363f-105">Overview</span></span>

<span data-ttu-id="b363f-106">Altbilgi modülü, sayfa altbilgisinde gösterilen modülleri barındırmak için kullanılan özel bir kapsayıcıdır.</span><span class="sxs-lookup"><span data-stu-id="b363f-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="b363f-107">Örneğin, **Bize başvurun** ve **Mağaza ilkeleri** sayfaları gibi çeşitli sayfaların bağlantılarını içerebilir.</span><span class="sxs-lookup"><span data-stu-id="b363f-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

<span data-ttu-id="b363f-108">Aşağıdaki resimde site sayfasında kullanılan bir altbilgi modülü örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="b363f-108">The following image shows an example of a footer module on a site page.</span></span>

![Altbilgi modülü örneği](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a><span data-ttu-id="b363f-110">Alt bilgi modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="b363f-110">Footer module properties</span></span> 

<span data-ttu-id="b363f-111">Çoğu kapsayıcı gibi bir altbilgi modülü de başlık ve genişlik için özellikleri destekler.</span><span class="sxs-lookup"><span data-stu-id="b363f-111">Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id="b363f-112">Çoklu alt bilgi kategorisi modüllerinin eklenmesini de destekler.</span><span class="sxs-lookup"><span data-stu-id="b363f-112">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="b363f-113">Eklenen her altbilgi kategorisi modülü altbilgi modülünde bir sütun olarak işlenir.</span><span class="sxs-lookup"><span data-stu-id="b363f-113">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="b363f-114">Altbilgi modülünde bulunan modüller</span><span class="sxs-lookup"><span data-stu-id="b363f-114">Modules available in a footer module</span></span>

<span data-ttu-id="b363f-115">**Alt bilgi maddeleri** – bir altbilgi öğeleri modülü bir başlık, bir resim ve bir bağlantı içerebilir.</span><span class="sxs-lookup"><span data-stu-id="b363f-115">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="b363f-116">Başlık tek başına veya bir görüntü ve bir bağlantıyla birlikte kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b363f-116">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="b363f-117">Alt bilgideki her bağlantı yalnızca metin içerecek şekilde yapılandırılabilir (örneğin, "bize başvurun" ve "Gizlilik" bağlantıları) veya hem metin, hem de resim (örneğin, sosyal medya bağlantıları) vardır.</span><span class="sxs-lookup"><span data-stu-id="b363f-117">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="b363f-118">**Başa dön** – en başa dön modülü sayfanın başına hızlı gezinti için bir bağlantı sağlar.</span><span class="sxs-lookup"><span data-stu-id="b363f-118">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="b363f-119">Bir hedef gerekli.</span><span class="sxs-lookup"><span data-stu-id="b363f-119">A destination is required.</span></span> <span data-ttu-id="b363f-120">Varsayılan hedef değeri, kullanıcıyı sayfanın en üstüne götüren \# değeridir.</span><span class="sxs-lookup"><span data-stu-id="b363f-120">The default destination value is \#, which takes the user to the top of the page.</span></span>

## <a name="create-a-footer-module"></a><span data-ttu-id="b363f-121">Alt bilgi modülü oluşturma</span><span class="sxs-lookup"><span data-stu-id="b363f-121">Create a footer module</span></span>

1. <span data-ttu-id="b363f-122">**Parçalar**'a gidin ve yeni parça oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b363f-122">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="b363f-123">**Yeni parça** iletişim kutusunda **Kapsayıcı** modülünü seçin, parça için bir ad girin ve sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b363f-123">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="b363f-124">**Varsayılan Konteyner** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b363f-124">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b363f-125">**Modül Ekle** iletişim kutusunda **alt bilgi kategorisi** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b363f-125">In the **Add Module** dialog box, select the **Footer category** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b363f-126">**Altbilgi kategorisi** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b363f-126">In the **Footer category** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b363f-127">**Modül Ekle** iletişim kutusunda **alt bilgi öğesi** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b363f-127">In the **Add Module** dialog box, select the **Footer item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b363f-128">**Altbilgi madde** yuvasını seçin, daha sonra sağdaki özellikler bölmesinde, başlığı, bağlantı ve metin bağlantısını ve resmi gerektiği gibi yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="b363f-128">Select the **Footer item** slot, and then, in the properties pane on the right, configure the heading, link and link text, and image as needed.</span></span>
1. <span data-ttu-id="b363f-129">Daha fazla alt bilgi öğesi eklemek için 5 ile 7. adımları tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="b363f-129">To add more footer items, repeat steps 5 through 7 for each.</span></span>
1. <span data-ttu-id="b363f-130">Alt bilginize "başa dön" bağlantısı eklemek için **Altbilgi kategorisi** yuvasında üç nokta (**...**) düğmesini ve sonra da **Modül Ekle** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="b363f-130">To add a "back to top" link to your footer, select the ellipsis (**...**) in the **Footer category** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="b363f-131">**Modül Ekle** iletişim kutusunda **başa dön** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b363f-131">In the **Add Module** dialog box, select the **Back to top** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b363f-132">**Başa dön** yuvasını seçin, daha sonra sağdaki özellikler bölmesinde, metni ve diğer modül özelliklerini gerektiği gibi yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="b363f-132">Select the **Back to top** slot, and then, in the properties pane on the right, configure the text and other module properties as needed.</span></span>
1. <span data-ttu-id="b363f-133">Parçayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b363f-133">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="b363f-134">Üstbilginin her sayfada göründüğünü garantilemek için, site için oluşturulan her sayfa şablonunda aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b363f-134">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="b363f-135">**Varsayılan sayfanın** **Altbilgi** yuvasında, altbilgi modülünde, oluşturduğunuz altbilgi parçasını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="b363f-135">In the **Footer** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="b363f-136">Şablonu iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b363f-136">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="b363f-137">Parçayı sayfa şablonlarına ekleyerek, altbilginin her sayfada oluşturulmasını sağlamaya yardımcı olursunuz.</span><span class="sxs-lookup"><span data-stu-id="b363f-137">By adding the fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b363f-138">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b363f-138">Additional resources</span></span>

[<span data-ttu-id="b363f-139">Modül kitaplığına genel bakış</span><span class="sxs-lookup"><span data-stu-id="b363f-139">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b363f-140">Kapsayıcı modülü</span><span class="sxs-lookup"><span data-stu-id="b363f-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="b363f-141">Satın alma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="b363f-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="b363f-142">Alışveriş sepeti modülü</span><span class="sxs-lookup"><span data-stu-id="b363f-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b363f-143">Ödeme yapma modülü</span><span class="sxs-lookup"><span data-stu-id="b363f-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b363f-144">Sipariş onayı modülü</span><span class="sxs-lookup"><span data-stu-id="b363f-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b363f-145">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="b363f-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="b363f-146">Alt bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="b363f-146">Footer module</span></span>](author-footer-module.md)
