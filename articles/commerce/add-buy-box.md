---
title: Satın alma kutusu modülü
description: Bu konu satın alma kutusu modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 07/31/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3fe5c1eb5808ef778aeda29442fa884556671296
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686682"
---
# <a name="buy-box-module"></a><span data-ttu-id="88da1-103">Satın alma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="88da1-103">Buy box module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="88da1-104">Bu konu satın alma kutusu modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="88da1-104">This topic covers buy box modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="88da1-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="88da1-105">Overview</span></span>

<span data-ttu-id="88da1-106">Terim *satın alma kutusu* genellikle, ürün satın alma işlemi yapmak için gereken en önemli bilgileri barındıran, ürün Ayrıntıları sayfasının "manşet" alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="88da1-106">The term *buy box* typically refers to the area of a product details page that is "above the fold," and that hosts all the most important information that is required to make a product purchase.</span></span> <span data-ttu-id="88da1-107">(Sayfanın ilk yüklendiği sırada "manşet" olan alan görünür, böylece görmek için kullanıcıların aşağı kaydırılması gerekmez.)</span><span class="sxs-lookup"><span data-stu-id="88da1-107">(An area that is "above the fold" is visible when the page is first loaded, so that users don't have to scroll down to see it.)</span></span>

<span data-ttu-id="88da1-108">Satın alma kutusu modülü, Ürün Ayrıntıları sayfasının satın alma kutusu alanında gösterilen tüm modülleri barındırmak için kullanılan özel bir konteynerdir.</span><span class="sxs-lookup"><span data-stu-id="88da1-108">A buy box module is special container that is used to host all the modules that are shown in the buy box area of a product details page.</span></span>

<span data-ttu-id="88da1-109">Ürün Ayrıntıları sayfasının URL'SI ürün kodunu içerir.</span><span class="sxs-lookup"><span data-stu-id="88da1-109">The URL of a product details page includes the product ID.</span></span> <span data-ttu-id="88da1-110">Bir satınalma kutusu modülünü işlemek için gereken tüm bilgiler bu ürün kimliğinden türetilir.</span><span class="sxs-lookup"><span data-stu-id="88da1-110">All the information that is required to render a buy box module is derived from this product ID.</span></span> <span data-ttu-id="88da1-111">Bir ürün kodu sağlanmazsa, satın alma kutusu modülü sayfada doğru olarak işlenmez.</span><span class="sxs-lookup"><span data-stu-id="88da1-111">If a product ID isn't provided, the buy box module won't be rendered correctly on a page.</span></span> <span data-ttu-id="88da1-112">Bu nedenle, satın alma kutusu modülü yalnızca ürün içeriği olan sayfalarda kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="88da1-112">Therefore, a buy box module can be used only on pages that have product context.</span></span> <span data-ttu-id="88da1-113">Ürün bağlamı bulunmayan bir sayfada (örneğin, giriş sayfası veya pazarlama sayfası) kullanmak için, ek özelleştirmeler yapmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="88da1-113">To use it on a page that doesn't have product context (for example, a home page or a marketing page), you must do additional customizations.</span></span>

<span data-ttu-id="88da1-114">Aşağıdaki resimde ürün ayrıntıları sayfasında kullanılan bir satın alma kutusu modülü örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="88da1-114">The following image shows an example of a buy box module on a product details page.</span></span>

![Satın alma kutusu modülü örneği](./media/ecommerce-pdp-buybox.PNG)

## <a name="buy-box-module-properties-and-slots"></a><span data-ttu-id="88da1-116">Satın alma kutusu modülü özelliklerini ve yuvaları</span><span class="sxs-lookup"><span data-stu-id="88da1-116">Buy box module properties and slots</span></span> 

<span data-ttu-id="88da1-117">Ürün Ayrıntıları sayfasında, satınalma kutusu iki bölgeye ayrılmıştır: soldaki ortam bölgesi ve sağda bulunan bir içerik bölgesi.</span><span class="sxs-lookup"><span data-stu-id="88da1-117">On a product details page, a buy box is divided into two regions: a media region on the left and a content region on the right.</span></span> <span data-ttu-id="88da1-118">Varsayılan olarak, ortam bölgesi sütunu genişliğinin içerik bölgesi sütunu genişliğine oranı 2:1'dir.</span><span class="sxs-lookup"><span data-stu-id="88da1-118">By default, the ratio of the width of the media region column to the width of the content region column is 2:1.</span></span> <span data-ttu-id="88da1-119">Mobil cihazlarda iki bölge yığılır, böylece diğer bölgenin altında bir alan görünür.</span><span class="sxs-lookup"><span data-stu-id="88da1-119">On mobile devices, the two regions are stacked so that one region appears below the other region.</span></span> <span data-ttu-id="88da1-120">Temalar, sütun genişlikleri ve yığınlama derecesini özelleştirmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="88da1-120">Themes can be used to customize the column widths and stacking rank.</span></span>

<span data-ttu-id="88da1-121">Satınalma kutusu modülü bir ürünün başlığını, açıklamasını, fiyatını ve derecelendirmelerini işler.</span><span class="sxs-lookup"><span data-stu-id="88da1-121">A buy box module renders the title, description, price, and ratings of a product.</span></span> <span data-ttu-id="88da1-122">Ayrıca müşteriler boyut, stil ve renk gibi farklı ürün özniteliklerine sahip ürün çeşitlerini da seçmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="88da1-122">It also lets customers select product variants that have different product attributes, such as size, style, and color.</span></span> <span data-ttu-id="88da1-123">Bir ürün çeşidi seçildiğinde, satınalma kutusundaki diğer Özellikler (örneğin, ürün açıklaması ve görüntüler) değişken bilgilerini yansıtacak şekilde güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="88da1-123">When a product variant is selected, other properties in the buy box (for example, the product description and images) are updated to reflect the variant information.</span></span> 

<span data-ttu-id="88da1-124">Müşterilerin satın alınacak maddelerin miktarını belirtebilmesi için bir miktar seçici sağlanır.</span><span class="sxs-lookup"><span data-stu-id="88da1-124">A quantity selector is provided, so that customers can specify the quantity of items to purchase.</span></span> <span data-ttu-id="88da1-125">Satın alınabilecek maksimum miktar, Tesis ayarlarında tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="88da1-125">The maximum quantity that can be purchased can be defined in the site settings.</span></span>

<span data-ttu-id="88da1-126">Müşteriler, satınalma kutusunda, alışveriş sepetine ürün ekleme, istek listesine ürün ekleme ve malzeme çekme yerleşimi seçme gibi eylemleri gerçekleştirebilirler.</span><span class="sxs-lookup"><span data-stu-id="88da1-126">From the buy box, customers can also perform actions such as adding a product to the cart, adding a product to their wishlist, and selecting a pickup location.</span></span> <span data-ttu-id="88da1-127">Bu eylemler bir ürün veya ürün çeşidi için gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="88da1-127">These actions can be performed on a product or a product variant.</span></span> <span data-ttu-id="88da1-128">Bir ürünü bir istek listesine listesine eklemek için müşterinin oturum açmış olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="88da1-128">To add a product to a wishlist, the customer must be signed in.</span></span>

<span data-ttu-id="88da1-129">Temalar, satın alma kutusu ürün özelliklerini ve eylem denetimlerini kaldırmak veya değiştirmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="88da1-129">Themes can be used to remove or change the order of buy box product properties and action controls.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="88da1-130">Modül özellikleri</span><span class="sxs-lookup"><span data-stu-id="88da1-130">Module properties</span></span>

- <span data-ttu-id="88da1-131">**Başlık etiketi** – bu özellik, ürün başlığının başlık etiketini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="88da1-131">**Heading tag** – This property defines the heading tag for the product title.</span></span> <span data-ttu-id="88da1-132">Satın al kutusu sayfanın en üstünde ise, erişilebilirlik standartlarını karşılamak için bu özelliğin **H1** olarak ayarlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="88da1-132">If the buy box is at the top of the page, this property should be set to **h1** to meet accessibility standards.</span></span> 

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a><span data-ttu-id="88da1-133">Satınalma kutusu modülünde kullanılabilen modüller</span><span class="sxs-lookup"><span data-stu-id="88da1-133">Modules that can be used in a buy box module</span></span>

- <span data-ttu-id="88da1-134">**Ortam Galerisi** – bu modül, ürün ayrıntıları sayfasındaki bir ürünün görüntülerini sergilemesinde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="88da1-134">**Media gallery** – This module is used to showcase images of a product on a product details page.</span></span> <span data-ttu-id="88da1-135">Bu modülle ilgili daha fazla bilgi için bkz. [Ortam galerisi modülü](media-gallery-module.md).</span><span class="sxs-lookup"><span data-stu-id="88da1-135">For more information about this module, see [Media gallery module](media-gallery-module.md).</span></span>
- <span data-ttu-id="88da1-136">**Mağaza seçici** - Bu modül bir maddenin almak için kullanılabilir olduğu yakındaki mağazaların listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="88da1-136">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="88da1-137">Kullanıcıların yakındaki mağazaları bulabilmesi için bir konum girmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="88da1-137">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="88da1-138">Bu modülle ilgili daha fazla bilgi için bkz. [Mağaza seçici modülü](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="88da1-138">For more information about this module, see [Store selector module](store-selector.md).</span></span>

## <a name="buy-box-module-settings"></a><span data-ttu-id="88da1-139">Satın alma kutusu modülü ayarları</span><span class="sxs-lookup"><span data-stu-id="88da1-139">Buy box module settings</span></span>

<span data-ttu-id="88da1-140">Aşağıdaki satın alma kutusu modülü ayarları **Site Ayarları \> Uzantılar** üzerinden yapılandırılabilecek ayarlara sahiptir:</span><span class="sxs-lookup"><span data-stu-id="88da1-140">The following buy box module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="88da1-141">**Sepet miktar sınırı** - Bu özellik, alışveriş sepetine eklenebilecek maksimum madde sayısını belirtmekte kullanılır.</span><span class="sxs-lookup"><span data-stu-id="88da1-141">**Cart line quantity limit** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="88da1-142">Örneğin, bir perakende satılan her ürünün yalnızca 10 tanesi tek bir harekette satılabilir olduğuna karar verebilir.</span><span class="sxs-lookup"><span data-stu-id="88da1-142">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="88da1-143">**Stok** - Stok ayarlarının nasıl uygulanacağı hakkında bilgi için bkz. [Envanter ayarları uygula](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="88da1-143">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="88da1-144">**Sepete Ekle** - Bu özellik, bir öğe alışveriş sepetine eklendikten sonra davranışı belirtmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="88da1-144">**Add to cart** - This property is used to specify the behavior after an item is added to the cart.</span></span> <span data-ttu-id="88da1-145">Olası değerler **alışveriş sepetine gidin**, **sepete gitmeyin** ve **bildirimleri göster**.</span><span class="sxs-lookup"><span data-stu-id="88da1-145">The possible values are **Navigate to cart**, **Do not navigate to cart**, and **Show notifications**.</span></span> <span data-ttu-id="88da1-146">Değer **sepete gitmek** üzere ayarlandığında , kullanıcılar bir öğe ekledikten sonra sepet sayfasına gönderilir.</span><span class="sxs-lookup"><span data-stu-id="88da1-146">When the value is set to **Navigate to cart**, users are sent to the cart page after they add an item.</span></span> <span data-ttu-id="88da1-147">Değer **sepete gitme** olarak ayarlandığında , kullanıcılar bir öğe ekledikten sonra sepet sayfasına gönderilmez.</span><span class="sxs-lookup"><span data-stu-id="88da1-147">When the value is set to **Do not navigate to cart**, users aren't sent to the cart page after they add an item.</span></span> <span data-ttu-id="88da1-148">Değer **bildirimleri gösterecek** şekilde ayarlandığında kullanıcılara bir onay bildirimi gösterilir ve ürün ayrıntıları sayfasına gözatmaya devam edebilir.</span><span class="sxs-lookup"><span data-stu-id="88da1-148">When the value is set to **Show notifications**, users are shown a confirmation notification and can continue to browse on the product details page.</span></span> 

    <span data-ttu-id="88da1-149">Aşağıdaki resimde fabrikam sitesindeki "Sepete eklenen" onay bildirimine bir örnek gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="88da1-149">The following image shows an example of an "added to cart" confirmation notification on the Fabrikam site.</span></span>

    ![Bildirim modülü örneği](./media/ecommerce-addtocart-notifications.PNG)

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="88da1-151">Ticari ölçek birim etkileşimi</span><span class="sxs-lookup"><span data-stu-id="88da1-151">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="88da1-152">Satın alma kutusu modülü, ürün bilgilerini Commerce Scale Unit uygulama programlama arayüzleri (API'ler) kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="88da1-152">The buy box module retrieves product information by using Commerce Scale Unit application programming interfaces (APIs).</span></span> <span data-ttu-id="88da1-153">Ürün Ayrıntıları sayfasındaki ürün kimliği tüm bilgileri almak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="88da1-153">The product ID from the product details page is used to retrieve all information.</span></span>

## <a name="add-a-buy-box-module-to-a-page"></a><span data-ttu-id="88da1-154">Sayfaya satınalma kutusu modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="88da1-154">Add a buy box module to a page</span></span>

<span data-ttu-id="88da1-155">Bir yeni sayfaya satın alma kutusu modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="88da1-155">To add a buy box module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="88da1-156">**Parçalar**'a gidin ve yeni parça oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="88da1-156">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="88da1-157">**Yeni sayfa parçası** iletişim kutusunda, **Satın alma kutusu** modülünü seçin.</span><span class="sxs-lookup"><span data-stu-id="88da1-157">In the **New page fragment** dialog box, select the **Buybox** module.</span></span>
1. <span data-ttu-id="88da1-158">**Sayfa parçası adı** altında, **Satın alma kutusu** için bir ad girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="88da1-158">Under **Page fragment name**, enter the name **Buy box fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="88da1-159">**Ortam Galerisi** modülünü içeren kapsayıcı yuvasında üç noktayı (**...**) seçin ve sonra **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="88da1-159">In the **Media Gallery** slot of the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="88da1-160">**Modül Ekle** iletişim kutusunda **Ortam galerisi** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="88da1-160">In the **Add Module** dialog box, select the **Media gallery** module, and then select **OK**.</span></span>
1. <span data-ttu-id="88da1-161">**Mağaza seçici** modülünü içeren kapsayıcı yuvasında üç noktayı (**...**) seçin ve sonra **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="88da1-161">In the **Store selector** slot of the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="88da1-162">**Modül Ekle** iletişim kutusunda **Mağaza seçici** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="88da1-162">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="88da1-163">**Kaydet**'i seçin, parçayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="88da1-163">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="88da1-164">Bir yeni şablonu oluşturmak için **Şablonlar**'a gidin ve **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="88da1-164">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="88da1-165">**Yeni Şablon** iletişim kutusunda **Şablon adı** altında, **PDP şablonu**'nu girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="88da1-165">In the **New Template** dialog box, under **Template name**, enter **PDP template**, and then select **OK**.</span></span>
1. <span data-ttu-id="88da1-166">**Gövde** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="88da1-166">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="88da1-167">**Modül Ekle** iletişim kutusunda **Varsayılan sayfa** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="88da1-167">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="88da1-168">Varsayılan sayfada **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Sayfa parçası ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="88da1-168">In the **Main** slot of the default page, select the ellipsis (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="88da1-169">**Sayfa parçası seç** iletişim kutusunda daha önce oluşturduğunuz **Satın alma kutusu parçası** parçasını ve sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="88da1-169">In the **Select page fragment** dialog box, select the **Buy box fragment** fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="88da1-170">**Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="88da1-170">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="88da1-171">**Sayfalar**'a gidin ve yeni sayfa oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="88da1-171">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="88da1-172">**Şablon seç** iletişim kutusunda **PDP şablon** şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="88da1-172">In the **Choose a template** dialog box, select the **PDP template** template.</span></span> <span data-ttu-id="88da1-173">Bir **sayfa adı** ve sayfa **PDP sayfası** girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="88da1-173">Under **Page name**, enter **PDP page**, and then select **OK**.</span></span>
1. <span data-ttu-id="88da1-174">Yeni sayfada **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Sayfa parçası ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="88da1-174">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="88da1-175">**Sayfa parçası seç** iletişim kutusunda daha önce oluşturduğunuz **Satın alma kutusu parçası** parçasını ve sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="88da1-175">In the **Select page fragment** dialog box, select the **Buy box fragment** fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="88da1-176">Sayfayı kaydet ve önizleyin.</span><span class="sxs-lookup"><span data-stu-id="88da1-176">Save and preview the page.</span></span> <span data-ttu-id="88da1-177">**?productid=&lt;Product ID&gt;** sorgu dizesi parametresini önizleme sayfasının URL 'sine ekleyin.</span><span class="sxs-lookup"><span data-stu-id="88da1-177">Add the **?productid=&lt;product id&gt;** query string parameter to the URL of the preview page.</span></span> <span data-ttu-id="88da1-178">Bu şekilde, ürün bağlamı Önizleme sayfasını yüklemek ve oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="88da1-178">In that way, the product context is used to load and render the preview page.</span></span>
1. <span data-ttu-id="88da1-179">**Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="88da1-179">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="88da1-180">Ürün Ayrıntıları sayfasında bir satınalma kutusu görünmelidir.</span><span class="sxs-lookup"><span data-stu-id="88da1-180">A buy box should appear on the product details page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="88da1-181">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="88da1-181">Additional resources</span></span>

[<span data-ttu-id="88da1-182">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="88da1-182">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="88da1-183">Mağaza seçicisi modülü</span><span class="sxs-lookup"><span data-stu-id="88da1-183">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="88da1-184">Ortam galerisi modülü</span><span class="sxs-lookup"><span data-stu-id="88da1-184">Media gallery module</span></span>](media-gallery-module.md)

[<span data-ttu-id="88da1-185">Kapsayıcı modülü</span><span class="sxs-lookup"><span data-stu-id="88da1-185">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="88da1-186">Sepet modülü</span><span class="sxs-lookup"><span data-stu-id="88da1-186">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="88da1-187">Sepet simgesi modülü</span><span class="sxs-lookup"><span data-stu-id="88da1-187">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="88da1-188">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="88da1-188">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="88da1-189">Sipariş onayı modülü</span><span class="sxs-lookup"><span data-stu-id="88da1-189">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="88da1-190">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="88da1-190">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="88da1-191">Alt bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="88da1-191">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="88da1-192">Perakende kanalları için stok kullanılabilirliğini hesaplama</span><span class="sxs-lookup"><span data-stu-id="88da1-192">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
