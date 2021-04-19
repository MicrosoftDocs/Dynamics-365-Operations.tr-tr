---
title: Sipariş onayı modülü
description: Bu konu sipariş onaylama modüllerini ve bunların nasıl Microsoft Dynamics 365 Commerce'te kullanılacağını açıklamaktadır ve kapsamaktadır.
author: anupamar-ms
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1f8742637cc8ed29abcfb9a8061a8d2602762d4f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804589"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="e2a88-103">Sipariş onayı modülü</span><span class="sxs-lookup"><span data-stu-id="e2a88-103">Order confirmation module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e2a88-104">Bu konu sipariş onaylama modüllerini ve bunların nasıl Microsoft Dynamics 365 Commerce'te kullanılacağını açıklamaktadır ve kapsamaktadır.</span><span class="sxs-lookup"><span data-stu-id="e2a88-104">This topic covers order confirmation modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e2a88-105">Bir sipariş yerleştirildikten sonra, onay ayrıntılarını göstermek için sipariş onayı modülü kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e2a88-105">The order confirmation module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="e2a88-106">Sipariş onay kodunu, sipariş iletişim bilgilerini ve satın alınan maddeler, ödeme bilgileri, teslim alma seçenekleri ve sevkiyat yöntemi gibi diğer sipariş ayrıntılarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e2a88-106">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, pickup options, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="e2a88-107">Sipariş onayı modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="e2a88-107">Order confirmation module properties</span></span>

| <span data-ttu-id="e2a88-108">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="e2a88-108">Property name</span></span>  | <span data-ttu-id="e2a88-109">Değerler</span><span class="sxs-lookup"><span data-stu-id="e2a88-109">Values</span></span> | <span data-ttu-id="e2a88-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="e2a88-110">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="e2a88-111">Başlık</span><span class="sxs-lookup"><span data-stu-id="e2a88-111">Heading</span></span>        | <span data-ttu-id="e2a88-112">Başlık metni ve başlık etiketi (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**)</span><span class="sxs-lookup"><span data-stu-id="e2a88-112">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="e2a88-113">Sipariş teyidi modülünün başlığı olabilir.</span><span class="sxs-lookup"><span data-stu-id="e2a88-113">The order confirmation module can have a heading.</span></span> <span data-ttu-id="e2a88-114">Varsayılan olarak, başlık için **H2** başlık etiketi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e2a88-114">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="e2a88-115">Ancak, bu etiket erişilebilirlik gereksinimlerini karşılayacak şekilde değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="e2a88-115">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="e2a88-116">İlgili kişi numarası</span><span class="sxs-lookup"><span data-stu-id="e2a88-116">Contact number</span></span> | <span data-ttu-id="e2a88-117">Text</span><span class="sxs-lookup"><span data-stu-id="e2a88-117">Text</span></span> | <span data-ttu-id="e2a88-118">Siparişle ilgili sorular için bir ilgili kişi numarası sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="e2a88-118">A contact number can be provided for order-related questions.</span></span> |
| <span data-ttu-id="e2a88-119">Malzeme çekme zaman lotu bilgilerini göster</span><span class="sxs-lookup"><span data-stu-id="e2a88-119">Show pickup timeslot information</span></span> | <span data-ttu-id="e2a88-120">Doğru veya Yanlış</span><span class="sxs-lookup"><span data-stu-id="e2a88-120">True or False</span></span> | <span data-ttu-id="e2a88-121">Bu özellik Dynamics 365 Commerce 10.0.15 ve daha yüksek sürümlerde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e2a88-121">This property is available in Dynamics 365 Commerce 10.0.15 and higher.</span></span> <span data-ttu-id="e2a88-122">Doğru olduğunda, malzeme çekme maddesi için sağlanmışsa malzeme çekme zaman Lot bilgilerini görüntüler</span><span class="sxs-lookup"><span data-stu-id="e2a88-122">When true, it displays the pickup timeslot information if provided for a pickup item</span></span>|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a><span data-ttu-id="e2a88-123">Sipariş onayı sayfası modülünde kullanılabilen modüller</span><span class="sxs-lookup"><span data-stu-id="e2a88-123">Modules that can be used on an order confirmation page</span></span>

<span data-ttu-id="e2a88-124">Sipariş onayı sayfası oluşturduğunuzda, diğer ilgili modülleri de sipariş onayı modülünün yanı sıra ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e2a88-124">When you create an order confirmation page, you can add other relevant modules in addition to the order confirmation module.</span></span> <span data-ttu-id="e2a88-125">Burada bazı örnekler verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="e2a88-125">Here are some examples:</span></span>

- <span data-ttu-id="e2a88-126">**Öneriler modülü** – Müşteriye diğer ürünleri önermek için, sipariş onayı sayfasına öneri modülü koyulamıyor.</span><span class="sxs-lookup"><span data-stu-id="e2a88-126">**Recommendations module** – The recommendations module can be added to the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="e2a88-127">**Pazarlama modülleri** – Pazarlama içeriğini göstermek için, sipariş onayı sayfasına herhangi bir pazarlama modülü eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="e2a88-127">**Marketing modules** – Any marketing module can be added to the order confirmation page to show marketing content.</span></span>

## <a name="add-an-order-confirmation-module-to-a-page"></a><span data-ttu-id="e2a88-128">Sayfaya sipariş onayı modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="e2a88-128">Add an order confirmation module to a page</span></span>

<span data-ttu-id="e2a88-129">Bir yeni sayfaya sipariş onayı modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e2a88-129">To add an order confirmation module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="e2a88-130">Bir yeni şablonu oluşturmak için **Şablonlar**'a gidin ve **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e2a88-130">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="e2a88-131">**Yeni Şablon** iletişim kutusunda **Şablon adı** altında, **Sipariş onayı şablonu** adını girin ve ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e2a88-131">In the **New Template** dialog box, under **Template name**, enter the name **Order confirmation template**, and then select **OK**.</span></span>
1. <span data-ttu-id="e2a88-132">**Gövde** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e2a88-132">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e2a88-133">**Modül Ekle** iletişim kutusunda **Varsayılan sayfa** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e2a88-133">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e2a88-134">**Varsayılan sayfa** modülünde **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e2a88-134">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e2a88-135">**Modül Ekle** iletişim kutusunda **Sipariş onayı** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e2a88-135">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e2a88-136">**Kaydet**'i seçin ve ardından şablonu önizlemek için **Önizleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e2a88-136">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="e2a88-137">Sipariş onay numarasının bağlamını gerektirdiğinden, sipariş teyidi modülü işlenmemelidir.</span><span class="sxs-lookup"><span data-stu-id="e2a88-137">The order confirmation module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="e2a88-138">Şablonu iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="e2a88-138">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="e2a88-139">**Sayfalar**'a gidin ve yeni sayfa oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e2a88-139">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="e2a88-140">**Şablon seç** iletişim kutusunda **Sipariş onayı şablonu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="e2a88-140">In the **Choose a template** dialog box, select **Order confirmation template**.</span></span> <span data-ttu-id="e2a88-141">**Sayfa adı** altından **Sipariş onayı sayfası** girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e2a88-141">Under **Page name**, enter **Order confirmation page**, and then select **OK**.</span></span>
1. <span data-ttu-id="e2a88-142">**Varsayılan sayfa** modülünde **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e2a88-142">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e2a88-143">**Modül Ekle** iletişim kutusunda **Sipariş onayı** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e2a88-143">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e2a88-144">Sipariş onayı modülünün özellikler bölmesinde, kurşun kalem simgesinin yanındaki **Başlık**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e2a88-144">In the properties pane for the order confirmation module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="e2a88-145">**Başlık** iletişim kutusunun **Başlık Metni** alanında, **Sipairş onayı** başlık metnini girin ve ardından **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e2a88-145">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order confirmation**, and then select **OK**.</span></span>
1. <span data-ttu-id="e2a88-146">**Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e2a88-146">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="e2a88-147">Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="e2a88-147">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e2a88-148">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="e2a88-148">Additional resources</span></span>

[<span data-ttu-id="e2a88-149">Sepet modülü</span><span class="sxs-lookup"><span data-stu-id="e2a88-149">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="e2a88-150">Sepet simgesi modülü</span><span class="sxs-lookup"><span data-stu-id="e2a88-150">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="e2a88-151">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="e2a88-151">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="e2a88-152">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="e2a88-152">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="e2a88-153">Sevkiyat adresi modülü</span><span class="sxs-lookup"><span data-stu-id="e2a88-153">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="e2a88-154">Teslimat seçenekleri modülü</span><span class="sxs-lookup"><span data-stu-id="e2a88-154">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="e2a88-155">Malzeme çekme bilgileri modülü</span><span class="sxs-lookup"><span data-stu-id="e2a88-155">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="e2a88-156">Hediye kartı modülü</span><span class="sxs-lookup"><span data-stu-id="e2a88-156">Gift card module</span></span>](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]