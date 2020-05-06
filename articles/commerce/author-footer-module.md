---
title: Alt bilgi modülü
description: Bu konu altbilgi modüllerini ve bunların nasıl Dynamics 365 Commerce içine yazılacağını kapsamaktadır.
author: anupamar
manager: annbe
ms.date: 04/14/2020
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
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 51f8d26d6223dcd1f6961058cd9d772a67c69670
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269648"
---
# <a name="footer-module"></a><span data-ttu-id="55901-103">Alt bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="55901-103">Footer module</span></span>  


[!include [banner](includes/banner.md)]

<span data-ttu-id="55901-104">Bu konu altbilgi modüllerini ve bunların nasıl Microsoft Dynamics 365 Commerce'te oluşturacağını açıklamaktadır ve kapsamaktadır.</span><span class="sxs-lookup"><span data-stu-id="55901-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="55901-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="55901-105">Overview</span></span>

<span data-ttu-id="55901-106">Altbilgi modülü, sayfa altbilgisinde gösterilen modülleri barındırmak için kullanılan özel bir kapsayıcıdır.</span><span class="sxs-lookup"><span data-stu-id="55901-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="55901-107">Örneğin, **Bize başvurun** ve **Mağaza ilkeleri** sayfaları gibi çeşitli sayfaların bağlantılarını içerebilir.</span><span class="sxs-lookup"><span data-stu-id="55901-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

## <a name="footer-module-properties"></a><span data-ttu-id="55901-108">Alt bilgi modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="55901-108">Footer module properties</span></span> 

<span data-ttu-id="55901-109">Çoğu kapsayıcı gibi bir altbilgi modülü de başlık ve genişlik için özellikleri destekler.</span><span class="sxs-lookup"><span data-stu-id="55901-109">Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id="55901-110">Çoklu alt bilgi kategorisi modüllerinin eklenmesini de destekler.</span><span class="sxs-lookup"><span data-stu-id="55901-110">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="55901-111">Eklenen her altbilgi kategorisi modülü altbilgi modülünde bir sütun olarak işlenir.</span><span class="sxs-lookup"><span data-stu-id="55901-111">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="55901-112">Altbilgi modülünde bulunan modüller</span><span class="sxs-lookup"><span data-stu-id="55901-112">Modules available in a footer module</span></span>

<span data-ttu-id="55901-113">**Alt bilgi maddeleri** – bir altbilgi öğeleri modülü bir başlık, bir resim ve bir bağlantı içerebilir.</span><span class="sxs-lookup"><span data-stu-id="55901-113">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="55901-114">Başlık tek başına veya bir görüntü ve bir bağlantıyla birlikte kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="55901-114">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="55901-115">Alt bilgideki her bağlantı yalnızca metin içerecek şekilde yapılandırılabilir (örneğin, "bize başvurun" ve "Gizlilik" bağlantıları) veya hem metin, hem de resim (örneğin, sosyal medya bağlantıları) vardır.</span><span class="sxs-lookup"><span data-stu-id="55901-115">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="55901-116">**Başa dön** – en başa dön modülü sayfanın başına hızlı gezinti için bir bağlantı sağlar.</span><span class="sxs-lookup"><span data-stu-id="55901-116">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="55901-117">Bir hedef gerekli.</span><span class="sxs-lookup"><span data-stu-id="55901-117">A destination is required.</span></span> <span data-ttu-id="55901-118">Varsayılan hedef değeri, kullanıcıyı sayfanın en üstüne götüren # değeridir.</span><span class="sxs-lookup"><span data-stu-id="55901-118">The default destination value is #, which takes the user to the top of the page.</span></span>

## <a name="author-a-footer-module"></a><span data-ttu-id="55901-119">Alt bilgi modülü düzenleme</span><span class="sxs-lookup"><span data-stu-id="55901-119">Author a footer module</span></span>

1. <span data-ttu-id="55901-120">Gezinti bölmesinde, **parçalar**'ı seçin ve sonra **yeni sayfa parçası**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="55901-120">In the navigation pane, select **Fragments**, and then select **New Page Fragment**.</span></span>
1. <span data-ttu-id="55901-121">**Yeni sayfa parçası** iletişim kutusunda altbilgi modülünü seçin, sayfa parçası için bir ad girin ve sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="55901-121">In the **New Page Fragment** dialog box, select the footer module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="55901-122">Soldaki anahat ağacı 'nda üç nokta düğmesini (**...**) ekleyin ve sonra da **Modül Ekle** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="55901-122">In the outline tree on the left, select the ellipsis button (**...**) for the footer module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="55901-123">**Modül Ekle** iletişim kutusunda alt bilgi kategorisi modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="55901-123">In the **Add Module** dialog box, select the footer category module, and then select **OK**.</span></span>
1. <span data-ttu-id="55901-124">Soldaki anahat ağacı alt bilgi kategori modülü için üç nokta düğmesini ve sonra da **Modül Ekle** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="55901-124">In the outline tree, select the ellipsis button for the footer category module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="55901-125">**Modül Ekle** iletişim kutusunda alt bilgi öğesi modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="55901-125">In the **Add Module** dialog box, select the footer item module, and then select **OK**.</span></span>
1. <span data-ttu-id="55901-126">Anahat ağacında altbilgi madde modülünü seçin.</span><span class="sxs-lookup"><span data-stu-id="55901-126">In the outline tree, select the footer item module.</span></span> <span data-ttu-id="55901-127">Daha sonra sağdaki özellikler bölmesinde, başlığı, bağlantı ve metin bağlantısını ve resmi gerektiği gibi yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="55901-127">Then, in the properties pane on the right, configure the heading, link and link text, and image as you require.</span></span>
1. <span data-ttu-id="55901-128">Daha fazla alt bilgi öğesi eklemek için 5 ile 7. adımları tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="55901-128">To add more footer items, repeat steps 5 through 7.</span></span>
1. <span data-ttu-id="55901-129">Alt bilginize "başa dön" bağlantısı eklemek için üç nokta düğmesini ve sonra da **Modül Ekle** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="55901-129">To add a "back to top" link to your footer, select the ellipsis button for the footer category module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="55901-130">**Modül Ekle** iletişim kutusunda başa dön modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="55901-130">In the **Add Module** dialog box, select the back to top module, and then select **OK**.</span></span>
1. <span data-ttu-id="55901-131">Anahat ağacında başa dön modülünü seçin.</span><span class="sxs-lookup"><span data-stu-id="55901-131">In the outline tree, select the back to top module.</span></span> <span data-ttu-id="55901-132">Daha sonra sağdaki Özellikler bölmesinde, en başa dön modülünü gerektiği gibi yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="55901-132">Then, in the properties pane on the right, configure the back to top module as you require.</span></span>
1. <span data-ttu-id="55901-133">**Kaydet**'i seçin, sayfa parçasını iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="55901-133">Select **Save**, select **Finish editing** to check in the page fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="55901-134">Site için oluşturulan her sayfa şablonunda, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="55901-134">On every page template that has been created for the site, follow these steps.</span></span>

1. <span data-ttu-id="55901-135">Varsayılan sayfanın **ana** yuvasında, altbilgi modülünde, oluşturduğunuz altbilgi parçasını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="55901-135">In the **Main** slot of the default page, in the footer module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="55901-136">**Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="55901-136">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="55901-137">Sayfa parçasını sayfa şablonlarına ekleyerek, altbilginin her sayfada oluşturulmasını sağlamaya yardımcı olursunuz.</span><span class="sxs-lookup"><span data-stu-id="55901-137">By adding the page fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="55901-138">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="55901-138">Additional resources</span></span>

[<span data-ttu-id="55901-139">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="55901-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="55901-140">Konteyner modülü</span><span class="sxs-lookup"><span data-stu-id="55901-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="55901-141">Satın alma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="55901-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="55901-142">Sepet modülü</span><span class="sxs-lookup"><span data-stu-id="55901-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="55901-143">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="55901-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="55901-144">Sipariş onayı modülü</span><span class="sxs-lookup"><span data-stu-id="55901-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="55901-145">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="55901-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="55901-146">Alt bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="55901-146">Footer module</span></span>](author-footer-module.md)
