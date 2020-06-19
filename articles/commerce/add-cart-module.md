---
title: Sepet modülü
description: Bu konu sepet modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3ba46fd90507a9cf8da92598c8449a2e553da352
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411285"
---
# <a name="cart-module"></a><span data-ttu-id="2b022-103">Sepet modülü</span><span class="sxs-lookup"><span data-stu-id="2b022-103">Cart module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="2b022-104">Bu konu sepet modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="2b022-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2b022-105">Özet</span><span class="sxs-lookup"><span data-stu-id="2b022-105">Overview</span></span>

<span data-ttu-id="2b022-106">Bir sepet modülü, müşteri kullanıma devam etmeden önce alışveriş sepetine eklenen maddeleri göstermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2b022-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="2b022-107">Ayrıca, modül sipariş özeti gösterir ve müşterinin promosyon kodları uygulamasını veya kaldırmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="2b022-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="2b022-108">Sepet modülü, oturum açan kullanıma alma ve konuk kullanıma almayı destekler.</span><span class="sxs-lookup"><span data-stu-id="2b022-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="2b022-109">Ayrıca bir **Alışverişe geri git** bağlantısı da destekler.</span><span class="sxs-lookup"><span data-stu-id="2b022-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="2b022-110">Bu bağlantı için yolu **Site Ayarları \> Uzantılar \> Rotalar** adresinden yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b022-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="2b022-111">Sepet modülü, tüm sitede kullanılabilen bir tarayıcı tanımlama bilgisi olan sepet kimliğine göre verileri işler.</span><span class="sxs-lookup"><span data-stu-id="2b022-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="2b022-112">Aşağıdaki resimde fabrikam sitesindeki bir sepet sayfası örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="2b022-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Sepet modülü örneği](./media/cart2.PNG)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="2b022-114">Sepet modülü özelliklerini ve yuvaları</span><span class="sxs-lookup"><span data-stu-id="2b022-114">Cart module properties and slots</span></span>

<span data-ttu-id="2b022-115">Sepet modülü bir **Başlık** özelliğine sahiptir ve bu **Alışveriş sepeti** ve **Sepetinizdeki öğeler** gibi değerlere ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="2b022-115">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="2b022-116">Sepet modülünde kullanılabilen modüller</span><span class="sxs-lookup"><span data-stu-id="2b022-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="2b022-117">**Metin bloğu** – bu modül sepet modülündeki özel iletileri destekler.</span><span class="sxs-lookup"><span data-stu-id="2b022-117">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="2b022-118">İletiler, içerik yönetim sistemi (CMS) tarafından çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="2b022-118">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="2b022-119">"Siparişinizdeki sorunları için 1-800-Fabrikam ile iletişim" gibi herhangi bir ileti eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="2b022-119">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="2b022-120">**Mağaza seçici** - Bu modül bir maddenin almak için kullanılabilir olduğu yakındaki mağazaların listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="2b022-120">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="2b022-121">Kullanıcıların yakındaki mağazaları bulabilmesi için bir konum girmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="2b022-121">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="2b022-122">Bu modülle ilgili daha fazla bilgi için bkz. [Mağaza seçme modülü](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="2b022-122">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="2b022-123">Modül özellikleri</span><span class="sxs-lookup"><span data-stu-id="2b022-123">Module properties</span></span>

<span data-ttu-id="2b022-124">Aşağıdaki sepet modülü ayarları **Site Ayarları \> Uzantılar** üzerinden yapılandırılabilecek ayarlara sahiptir:</span><span class="sxs-lookup"><span data-stu-id="2b022-124">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="2b022-125">**Maksimum miktar** - Bu özellik, alışveriş sepetine eklenebilecek maksimum madde sayısını belirtmekte kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2b022-125">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="2b022-126">Örneğin, bir perakende satılan her ürünün yalnızca 10 tanesi tek bir harekette satılabilir olduğuna karar verebilir.</span><span class="sxs-lookup"><span data-stu-id="2b022-126">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="2b022-127">**Stok** - Stok ayarlarının nasıl uygulanacağı hakkında bilgi için bkz. [Envanter ayarları uygula](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="2b022-127">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="2b022-128">**Alışverişe dön** – Bu özellik, **alışverişe geri dön** bağlantısına ait rotayı belirtmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2b022-128">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="2b022-129">Rota, Tesis düzeyinde konfigüre edilebilir ve perakendeciler müşteriyi giriş sayfasına veya sitedeki herhangi bir sayfaya geri geçirmesine olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="2b022-129">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="2b022-130">Ticari ölçek birim etkileşimi</span><span class="sxs-lookup"><span data-stu-id="2b022-130">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="2b022-131">Sepet modülü, ürün bilgilerini Commerce Scale Unit API'leri kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="2b022-131">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="2b022-132">Commerce Scale Unit'deki tüm ürün bilgilerini almak için, tarayıcı tanımlama bilgisinden alışveriş sepetinin kodu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2b022-132">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="2b022-133">Sayfaya sepet modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="2b022-133">Add a cart module to a page</span></span>

<span data-ttu-id="2b022-134">Bir yeni sayfaya sepet modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="2b022-134">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="2b022-135">**Sayfa Parçaları**'na gidin ve yeni parçası oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b022-135">Go to **Page Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="2b022-136">**Yeni Sayfa Parçası** iletişim kutusunda, **Sepet kutusu** modülünü seçin.</span><span class="sxs-lookup"><span data-stu-id="2b022-136">In the **New Page Fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="2b022-137">**Sayfa parçası adı** altında, **Sepet parça** için bir ad girin ve **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b022-137">Under **Page Fragment Name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="2b022-138">**Sepet** yuvasını seçin.</span><span class="sxs-lookup"><span data-stu-id="2b022-138">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="2b022-139">Sağdaki Özellikler bölmesinde, Kurşun Kalem sembolünü seçin, alana başlık metnini girin ve onay işareti simgesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2b022-139">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="2b022-140">**Sepet** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b022-140">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2b022-141">**Modül Ekle** iletişim kutusunda **Mağaza seçici** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b022-141">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2b022-142">**Kaydet**'i seçin, parçayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b022-142">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="2b022-143">Bir yeni şablonu oluşturmak için **Şablonlar**'a gidin ve **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b022-143">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="2b022-144">**Yeni Şablon** iletişim kutusunda **Şablon adı** altında, şablon için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="2b022-144">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="2b022-145">Anahat ağacında **Gövde** yuvasını seçin, üç nokta (**...**) ve sonra **Parça ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b022-145">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="2b022-146">**Sayfa Parçası Seç** iletişim kutusunda **Sepet parçası** parçasını ve sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b022-146">In the **Select Page Fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="2b022-147">**Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b022-147">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="2b022-148">**Sayfalar**'a gidin ve yeni sayfa oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b022-148">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="2b022-149">**Şablon Seç** iletişim kutusunda oluşturduğunuz şablonu seçin, sayfa adı girin ve sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b022-149">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="2b022-150">**Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2b022-150">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="2b022-151">Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b022-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2b022-152">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="2b022-152">Additional resources</span></span>

[<span data-ttu-id="2b022-153">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="2b022-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2b022-154">Konteyner modülü</span><span class="sxs-lookup"><span data-stu-id="2b022-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="2b022-155">Mağaza seçicisi modülü</span><span class="sxs-lookup"><span data-stu-id="2b022-155">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="2b022-156">Satınalma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="2b022-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="2b022-157">Sepet simgesi modülü</span><span class="sxs-lookup"><span data-stu-id="2b022-157">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="2b022-158">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="2b022-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="2b022-159">Sipariş onayı modülü</span><span class="sxs-lookup"><span data-stu-id="2b022-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="2b022-160">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="2b022-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="2b022-161">Alt bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="2b022-161">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="2b022-162">Perakende kanalları için stok kullanılabilirliğini hesaplama</span><span class="sxs-lookup"><span data-stu-id="2b022-162">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
