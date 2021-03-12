---
title: Sipariş onayı modülü
description: Bu konu sipariş onaylama modüllerini ve bunların nasıl Microsoft Dynamics 365 Commerce'te kullanılacağını açıklamaktadır ve kapsamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 9d916d2687777403f2b0df7c35171948ad2fb7db
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972767"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="fcc08-103">Sipariş onayı modülü</span><span class="sxs-lookup"><span data-stu-id="fcc08-103">Order confirmation module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fcc08-104">Bu konu sipariş onaylama modüllerini ve bunların nasıl Microsoft Dynamics 365 Commerce'te kullanılacağını açıklamaktadır ve kapsamaktadır.</span><span class="sxs-lookup"><span data-stu-id="fcc08-104">This topic covers order confirmation modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fcc08-105">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="fcc08-105">Overview</span></span>

<span data-ttu-id="fcc08-106">Bir sipariş yerleştirildikten sonra, onay ayrıntılarını göstermek için sipariş onayı modülü kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="fcc08-106">The order confirmation module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="fcc08-107">Sipariş onay kodunu, sipariş iletişim bilgilerini ve satın alınan maddeler, ödeme bilgileri, teslim alma seçenekleri ve sevkiyat yöntemi gibi diğer sipariş ayrıntılarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fcc08-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, pickup options, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="fcc08-108">Sipariş onayı modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="fcc08-108">Order confirmation module properties</span></span>

| <span data-ttu-id="fcc08-109">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="fcc08-109">Property name</span></span>  | <span data-ttu-id="fcc08-110">Değerler</span><span class="sxs-lookup"><span data-stu-id="fcc08-110">Values</span></span> | <span data-ttu-id="fcc08-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="fcc08-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="fcc08-112">Başlık</span><span class="sxs-lookup"><span data-stu-id="fcc08-112">Heading</span></span>        | <span data-ttu-id="fcc08-113">Başlık metni ve başlık etiketi (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**)</span><span class="sxs-lookup"><span data-stu-id="fcc08-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="fcc08-114">Sipariş teyidi modülünün başlığı olabilir.</span><span class="sxs-lookup"><span data-stu-id="fcc08-114">The order confirmation module can have a heading.</span></span> <span data-ttu-id="fcc08-115">Varsayılan olarak, başlık için **H2** başlık etiketi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fcc08-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="fcc08-116">Ancak, bu etiket erişilebilirlik gereksinimlerini karşılayacak şekilde değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="fcc08-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="fcc08-117">İlgili kişi numarası</span><span class="sxs-lookup"><span data-stu-id="fcc08-117">Contact number</span></span> | <span data-ttu-id="fcc08-118">Text</span><span class="sxs-lookup"><span data-stu-id="fcc08-118">Text</span></span> | <span data-ttu-id="fcc08-119">Siparişle ilgili sorular için bir ilgili kişi numarası sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="fcc08-119">A contact number can be provided for order-related questions.</span></span> |
| <span data-ttu-id="fcc08-120">Malzeme çekme zaman lotu bilgilerini göster</span><span class="sxs-lookup"><span data-stu-id="fcc08-120">Show pickup timeslot information</span></span> | <span data-ttu-id="fcc08-121">Doğru veya Yanlış</span><span class="sxs-lookup"><span data-stu-id="fcc08-121">True or False</span></span> | <span data-ttu-id="fcc08-122">Bu özellik Dynamics 365 Commerce 10.0.15 ve daha yüksek sürümlerde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="fcc08-122">This property is available in Dynamics 365 Commerce 10.0.15 and higher.</span></span> <span data-ttu-id="fcc08-123">Doğru olduğunda, malzeme çekme maddesi için sağlanmışsa malzeme çekme zaman Lot bilgilerini görüntüler</span><span class="sxs-lookup"><span data-stu-id="fcc08-123">When true, it displays the pickup timeslot information if provided for a pickup item</span></span>|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a><span data-ttu-id="fcc08-124">Sipariş onayı sayfası modülünde kullanılabilen modüller</span><span class="sxs-lookup"><span data-stu-id="fcc08-124">Modules that can be used on an order confirmation page</span></span>

<span data-ttu-id="fcc08-125">Sipariş onayı sayfası oluşturduğunuzda, diğer ilgili modülleri de sipariş onayı modülünün yanı sıra ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fcc08-125">When you create an order confirmation page, you can add other relevant modules in addition to the order confirmation module.</span></span> <span data-ttu-id="fcc08-126">Burada bazı örnekler verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="fcc08-126">Here are some examples:</span></span>

- <span data-ttu-id="fcc08-127">**Öneriler modülü** – Müşteriye diğer ürünleri önermek için, sipariş onayı sayfasına öneri modülü koyulamıyor.</span><span class="sxs-lookup"><span data-stu-id="fcc08-127">**Recommendations module** – The recommendations module can be added to the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="fcc08-128">**Pazarlama modülleri** – Pazarlama içeriğini göstermek için, sipariş onayı sayfasına herhangi bir pazarlama modülü eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="fcc08-128">**Marketing modules** – Any marketing module can be added to the order confirmation page to show marketing content.</span></span>

## <a name="add-an-order-confirmation-module-to-a-page"></a><span data-ttu-id="fcc08-129">Sayfaya sipariş onayı modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="fcc08-129">Add an order confirmation module to a page</span></span>

<span data-ttu-id="fcc08-130">Bir yeni sayfaya sipariş onayı modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="fcc08-130">To add an order confirmation module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="fcc08-131">Bir yeni şablonu oluşturmak için **Şablonlar**'a gidin ve **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fcc08-131">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="fcc08-132">**Yeni Şablon** iletişim kutusunda **Şablon adı** altında, **Sipariş onayı şablonu** adını girin ve ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="fcc08-132">In the **New Template** dialog box, under **Template name**, enter the name **Order confirmation template**, and then select **OK**.</span></span>
1. <span data-ttu-id="fcc08-133">**Gövde** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fcc08-133">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="fcc08-134">**Modül Ekle** iletişim kutusunda **Varsayılan sayfa** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="fcc08-134">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="fcc08-135">**Varsayılan sayfa** modülünde **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fcc08-135">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="fcc08-136">**Modül Ekle** iletişim kutusunda **Sipariş onayı** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="fcc08-136">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="fcc08-137">**Kaydet**'i seçin ve ardından şablonu önizlemek için **Önizleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fcc08-137">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="fcc08-138">Sipariş onay numarasının bağlamını gerektirdiğinden, sipariş teyidi modülü işlenmemelidir.</span><span class="sxs-lookup"><span data-stu-id="fcc08-138">The order confirmation module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="fcc08-139">Şablonu iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="fcc08-139">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="fcc08-140">**Sayfalar**'a gidin ve yeni sayfa oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fcc08-140">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="fcc08-141">**Şablon seç** iletişim kutusunda **Sipariş onayı şablonu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="fcc08-141">In the **Choose a template** dialog box, select **Order confirmation template**.</span></span> <span data-ttu-id="fcc08-142">**Sayfa adı** altından **Sipariş onayı sayfası** girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="fcc08-142">Under **Page name**, enter **Order confirmation page**, and then select **OK**.</span></span>
1. <span data-ttu-id="fcc08-143">**Varsayılan sayfa** modülünde **ana** yuvayı seçin, üç nokta düğmesini (**...**) ve sonra **Modül ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fcc08-143">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="fcc08-144">**Modül Ekle** iletişim kutusunda **Sipariş onayı** modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="fcc08-144">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="fcc08-145">Sipariş onayı modülünün özellikler bölmesinde, kurşun kalem simgesinin yanındaki **Başlık**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="fcc08-145">In the properties pane for the order confirmation module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="fcc08-146">**Başlık** iletişim kutusunun **Başlık Metni** alanında, **Sipairş onayı** başlık metnini girin ve ardından **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="fcc08-146">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order confirmation**, and then select **OK**.</span></span>
1. <span data-ttu-id="fcc08-147">**Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fcc08-147">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="fcc08-148">Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="fcc08-148">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fcc08-149">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="fcc08-149">Additional resources</span></span>

[<span data-ttu-id="fcc08-150">Sepet modülü</span><span class="sxs-lookup"><span data-stu-id="fcc08-150">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="fcc08-151">Sepet simgesi modülü</span><span class="sxs-lookup"><span data-stu-id="fcc08-151">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="fcc08-152">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="fcc08-152">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="fcc08-153">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="fcc08-153">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="fcc08-154">Sevkiyat adresi modülü</span><span class="sxs-lookup"><span data-stu-id="fcc08-154">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="fcc08-155">Teslimat seçenekleri modülü</span><span class="sxs-lookup"><span data-stu-id="fcc08-155">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="fcc08-156">Malzeme çekme bilgileri modülü</span><span class="sxs-lookup"><span data-stu-id="fcc08-156">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="fcc08-157">Hediye kartı modülü</span><span class="sxs-lookup"><span data-stu-id="fcc08-157">Gift card module</span></span>](add-giftcard.md)
