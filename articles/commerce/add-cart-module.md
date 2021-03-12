---
title: Sepet modülü
description: Bu konu sepet modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: abb9909c03577763ff7e6242c9395a58159df6ca
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985991"
---
# <a name="cart-module"></a><span data-ttu-id="6b0a7-103">Sepet modülü</span><span class="sxs-lookup"><span data-stu-id="6b0a7-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6b0a7-104">Bu konu sepet modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6b0a7-105">Özet</span><span class="sxs-lookup"><span data-stu-id="6b0a7-105">Overview</span></span>

<span data-ttu-id="6b0a7-106">Bir sepet modülü, müşteri kullanıma devam etmeden önce alışveriş sepetine eklenen maddeleri göstermek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="6b0a7-107">Ayrıca, modül sipariş özeti gösterir ve müşterinin promosyon kodları uygulamasını veya kaldırmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="6b0a7-108">Sepet modülü, oturum açan kullanıma alma ve konuk kullanıma almayı destekler.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="6b0a7-109">Ayrıca bir **Alışverişe geri git** bağlantısı da destekler.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="6b0a7-110">Bu bağlantı için yolu **Site Ayarları \> Uzantılar \> Rotalar** adresinden yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="6b0a7-111">Sepet modülü, tüm sitede kullanılabilen bir tarayıcı tanımlama bilgisi olan sepet kimliğine göre verileri işler.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="6b0a7-112">Aşağıdaki resimde fabrikam sitesindeki bir sepet sayfası örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Fabrikam sitesindeki bir sepet modülü örneği](./media/cart2.PNG)

<span data-ttu-id="6b0a7-114">Aşağıdaki resimde fabrikam sitesindeki bir sepet sayfası örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-114">The following image shows an example of a cart page on the Fabrikam site.</span></span> <span data-ttu-id="6b0a7-115">Bu örnekte, bir satır maddesi için işleme masrafı vardır.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-115">In this example, there is a handling fee for a line item.</span></span>

![Satır ögesi için işleme ücreti bulunan bir sepet modülü örneği](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="6b0a7-117">Sepet modülü özelliklerini ve yuvaları</span><span class="sxs-lookup"><span data-stu-id="6b0a7-117">Cart module properties and slots</span></span>

| <span data-ttu-id="6b0a7-118">Özellik</span><span class="sxs-lookup"><span data-stu-id="6b0a7-118">Property</span></span> | <span data-ttu-id="6b0a7-119">Değerler</span><span class="sxs-lookup"><span data-stu-id="6b0a7-119">Values</span></span> | <span data-ttu-id="6b0a7-120">Tanım</span><span class="sxs-lookup"><span data-stu-id="6b0a7-120">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="6b0a7-121">Başlık</span><span class="sxs-lookup"><span data-stu-id="6b0a7-121">Heading</span></span> | <span data-ttu-id="6b0a7-122">Başlık metmi ve başlık etiketi (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**)</span><span class="sxs-lookup"><span data-stu-id="6b0a7-122">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="6b0a7-123">"Alışveriş çantası" veya "Sepetinizdeki maddeler" gibi bir sepet başlığı.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-123">A heading for the cart, such as "Shopping bag" or "Items in your cart."</span></span> |
| <span data-ttu-id="6b0a7-124">Stokta yok hatalarını göster</span><span class="sxs-lookup"><span data-stu-id="6b0a7-124">Show out of stock errors</span></span> | <span data-ttu-id="6b0a7-125">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="6b0a7-125">**True** or **False**</span></span> | <span data-ttu-id="6b0a7-126">Bu özellik **Doğru** olarak ayarlanırsa, alışveriş sepeti sayfası stokla ilgili hataları gösterir.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-126">If this property is set to **True**, the cart page will show stock-related errors.</span></span> <span data-ttu-id="6b0a7-127">Sitede stok denetimleri uygulanıyorsa bu özelliği **Doğru** olarak ayarlamanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-127">We recommend that you set this property to **True** if inventory checks are applied on the site.</span></span> |
| <span data-ttu-id="6b0a7-128">Kalemler için sevkiyat masraflarını göster</span><span class="sxs-lookup"><span data-stu-id="6b0a7-128">Show shipping charges for line items</span></span> | <span data-ttu-id="6b0a7-129">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="6b0a7-129">**True** or **False**</span></span> | <span data-ttu-id="6b0a7-130">Bu özellik **Doğru** olarak ayarlanırsa, bu bilginin var olması durumunda sepet satırı maddeleri sevkiyat giderlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-130">If this property is set to **True**, cart line items will show the shipping charges, if this information is available.</span></span> <span data-ttu-id="6b0a7-131">Kullanıcılar ödeme akışında yalnızca sevkiyatı seçtiğindan bu özellik Fabrikam temasında desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-131">This feature isn't supported in the Fabrikam theme, because users select shipping only in the checkout flow.</span></span> <span data-ttu-id="6b0a7-132">Ancak, varsa bu özellik diğer iş akışlarında etkinleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-132">However, this feature can be turned on in other workflows if it's applicable.</span></span> |
| <span data-ttu-id="6b0a7-133">Mevcut promosyonları göster</span><span class="sxs-lookup"><span data-stu-id="6b0a7-133">Show available promotions</span></span>| <span data-ttu-id="6b0a7-134">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="6b0a7-134">**True** or **False**</span></span> | <span data-ttu-id="6b0a7-135">Bu özellik **Doğru** olarak ayarlanırsa alışveriş sepeti, içindeki ürünlere göre mevcut promosyonları gösterir.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-135">If this property is set to **True**, the cart shows available promotions, based on items in the cart.</span></span> <span data-ttu-id="6b0a7-136">Bu özellik Dynamics 365 Commerce sürüm 10.0.16'da kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-136">This capability is available in the Dynamics 365 Commerce 10.0.16 release.</span></span> |

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="6b0a7-137">Sepet modülünde kullanılabilen modüller</span><span class="sxs-lookup"><span data-stu-id="6b0a7-137">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="6b0a7-138">**Metin bloğu** – bu modül sepet modülündeki özel iletileri destekler.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-138">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="6b0a7-139">İletiler, içerik yönetim sistemi (CMS) tarafından çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-139">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="6b0a7-140">"Siparişinizdeki sorunları için 1-800-Fabrikam ile iletişim" gibi herhangi bir ileti eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-140">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="6b0a7-141">**Mağaza seçici** - Bu modül bir maddenin almak için kullanılabilir olduğu yakındaki mağazaların listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-141">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="6b0a7-142">Kullanıcıların yakındaki mağazaları bulabilmesi için bir konum girmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-142">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="6b0a7-143">Bu modülle ilgili daha fazla bilgi için bkz. [Mağaza seçme modülü](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="6b0a7-143">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="6b0a7-144">Modül özellikleri</span><span class="sxs-lookup"><span data-stu-id="6b0a7-144">Module properties</span></span>

<span data-ttu-id="6b0a7-145">Aşağıdaki sepet modülü ayarları **Site Ayarları \> Uzantılar** üzerinden yapılandırılabilecek ayarlara sahiptir:</span><span class="sxs-lookup"><span data-stu-id="6b0a7-145">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="6b0a7-146">**Maksimum miktar** - Bu özellik, alışveriş sepetine eklenebilecek maksimum madde sayısını belirtmekte kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-146">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="6b0a7-147">Örneğin, bir perakende satılan her ürünün yalnızca 10 tanesi tek bir harekette satılabilir olduğuna karar verebilir.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-147">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="6b0a7-148">**Stok** - Stok ayarlarının nasıl uygulanacağı hakkında bilgi için bkz. [Envanter ayarları uygula](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="6b0a7-148">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="6b0a7-149">**Alışverişe dön** – Bu özellik, **alışverişe geri dön** bağlantısına ait rotayı belirtmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-149">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="6b0a7-150">Rota, Tesis düzeyinde konfigüre edilebilir ve perakendeciler müşteriyi giriş sayfasına veya sitedeki herhangi bir sayfaya geri geçirmesine olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-150">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6b0a7-151">Dynamics 365 Commerce 10.0.14 sürümü ve sonrasında, sepetteki maddeler, Commerce Headquarters'daki çevrimiçi mağazanın çevrimiçi işlevsellik profilinde tanımlanan ayarlara göre toplanır.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-151">In the Dynamics 365 Commerce 10.0.14 release and later, items in the cart are aggregated based on the settings that are defined in the online functionality profile for the online store in Commerce headquarters.</span></span> <span data-ttu-id="6b0a7-152">Bir çevrimiçi işlevsellik profili oluşturma ve toplama için gerekli özellikleri ayarlama hakkında daha fazla bilgi için, bkz. [Çevrimiçi işlevsellik profili oluşturma](online-functionality-profile.md).</span><span class="sxs-lookup"><span data-stu-id="6b0a7-152">For more information about how to create an online functionality profile and set the properties that are required for aggregation, see [Create an online functionality profile](online-functionality-profile.md).</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="6b0a7-153">Ticari ölçek birim etkileşimi</span><span class="sxs-lookup"><span data-stu-id="6b0a7-153">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="6b0a7-154">Sepet modülü, ürün bilgilerini Commerce Scale Unit API'leri kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-154">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="6b0a7-155">Commerce Scale Unit'deki tüm ürün bilgilerini almak için, tarayıcı tanımlama bilgisinden alışveriş sepetinin kodu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-155">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="6b0a7-156">Sayfaya sepet modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="6b0a7-156">Add a cart module to a page</span></span>

<span data-ttu-id="6b0a7-157">Bir yeni sayfaya sepet modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-157">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="6b0a7-158">**Parçalar**'a gidin ve yeni parça oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-158">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="6b0a7-159">**Yeni parça** iletişim kutusunda, **Sepet** modülünü seçin.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-159">In the **New fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="6b0a7-160">**Parça adı** altında, **Sepet parçası** için bir ad girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-160">Under **Fragment name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="6b0a7-161">**Sepet** yuvasını seçin.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-161">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="6b0a7-162">Sağdaki Özellikler bölmesinde, Kurşun Kalem sembolünü seçin, alana başlık metnini girin ve onay işareti simgesini seçin.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-162">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="6b0a7-163">**Sepet** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-163">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="6b0a7-164">**Modül Ekle** iletişim kutusunda **Mağaza seçici** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-164">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="6b0a7-165">**Kaydet**'i seçin, parçayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-165">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="6b0a7-166">Bir yeni şablonu oluşturmak için **Şablonlar**'a gidin ve **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-166">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="6b0a7-167">**Yeni Şablon** iletişim kutusunda **Şablon adı** altında, şablon için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-167">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="6b0a7-168">Anahat ağacında **Gövde** yuvasını seçin, üç nokta (**...**) ve sonra **Parça ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-168">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="6b0a7-169">**Parça seç** iletişim kutusunda **Sepet parçası** öğesini ve sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-169">In the **Select fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="6b0a7-170">**Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-170">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="6b0a7-171">**Sayfalar**'a gidin ve yeni sayfa oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-171">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="6b0a7-172">**Şablon Seç** iletişim kutusunda oluşturduğunuz şablonu seçin, sayfa adı girin ve sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-172">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="6b0a7-173">**Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-173">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="6b0a7-174">Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="6b0a7-174">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6b0a7-175">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="6b0a7-175">Additional resources</span></span>

[<span data-ttu-id="6b0a7-176">Sepet simgesi modülü</span><span class="sxs-lookup"><span data-stu-id="6b0a7-176">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="6b0a7-177">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="6b0a7-177">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="6b0a7-178">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="6b0a7-178">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="6b0a7-179">Sevkiyat adresi modülü</span><span class="sxs-lookup"><span data-stu-id="6b0a7-179">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="6b0a7-180">Teslimat seçenekleri modülü</span><span class="sxs-lookup"><span data-stu-id="6b0a7-180">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="6b0a7-181">Malzeme çekme bilgileri modülü</span><span class="sxs-lookup"><span data-stu-id="6b0a7-181">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="6b0a7-182">Sipariş ayrıntıları modülü</span><span class="sxs-lookup"><span data-stu-id="6b0a7-182">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="6b0a7-183">Hediye kartı modülü</span><span class="sxs-lookup"><span data-stu-id="6b0a7-183">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="6b0a7-184">Perakende kanalları için stok kullanılabilirliğini hesaplama</span><span class="sxs-lookup"><span data-stu-id="6b0a7-184">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)

[<span data-ttu-id="6b0a7-185">Çevrimiçi işlevsellik profili oluşturma</span><span class="sxs-lookup"><span data-stu-id="6b0a7-185">Create an online functionality profile</span></span>](online-functionality-profile.md)
