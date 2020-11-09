---
title: Sipariş ayrıntıları modülü
description: Bu konu sipariş ayrıntıları modüllerini ve bunların nasıl Microsoft Dynamics 365 Commerce'te oluşturacağını açıklamaktadır ve kapsamaktadır.
author: anupamar
manager: annbe
ms.date: 06/18/2020
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
ms.openlocfilehash: 6610d2abe0a1b03ddd763f9a65fc1dab42f1da1b
ms.sourcegitcommit: 49f3011b8a6d8cdd038e153d8cb3cf773be25ae4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4015192"
---
# <a name="order-details-module"></a><span data-ttu-id="fb4e1-103">Sipariş ayrıntıları modülü</span><span class="sxs-lookup"><span data-stu-id="fb4e1-103">Order details module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fb4e1-104">Bu konu sipariş ayrıntıları modüllerini ve bunların nasıl Microsoft Dynamics 365 Commerce'te oluşturacağını açıklamaktadır ve kapsamaktadır.</span><span class="sxs-lookup"><span data-stu-id="fb4e1-104">This topic covers order details modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fb4e1-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="fb4e1-105">Overview</span></span>

<span data-ttu-id="fb4e1-106">Bir sipariş yerleştirildikten sonra, onay ayrıntılarını göstermek için sipariş ayrıntıları modülü kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="fb4e1-106">The order details module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="fb4e1-107">Sipariş onay kodunu, sipariş iletişim bilgilerini ve satın alınan maddeler, ödeme bilgileri ve sevkiyat yöntemi gibi diğer sipariş ayrıntılarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fb4e1-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, and the shipping method.</span></span>

## <a name="order-details-module-properties"></a><span data-ttu-id="fb4e1-108">Sipariş ayrıntıları modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="fb4e1-108">Order details module properties</span></span>

| <span data-ttu-id="fb4e1-109">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="fb4e1-109">Property name</span></span>  | <span data-ttu-id="fb4e1-110">Değerler</span><span class="sxs-lookup"><span data-stu-id="fb4e1-110">Values</span></span> | <span data-ttu-id="fb4e1-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="fb4e1-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="fb4e1-112">Başlık</span><span class="sxs-lookup"><span data-stu-id="fb4e1-112">Heading</span></span>        | <span data-ttu-id="fb4e1-113">Başlık metni ve başlık etiketi ( **H1** , **H2** , **H3** , **H4** , **H5** veya **H6** )</span><span class="sxs-lookup"><span data-stu-id="fb4e1-113">Heading text and heading tag ( **H1** , **H2** , **H3** , **H4** , **H5** , or **H6** )</span></span> | <span data-ttu-id="fb4e1-114">Sipariş ayrıntıları modülünün başlığı olabilir.</span><span class="sxs-lookup"><span data-stu-id="fb4e1-114">The order details module can have a heading.</span></span> <span data-ttu-id="fb4e1-115">Varsayılan olarak, başlık için **H2** başlık etiketi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fb4e1-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="fb4e1-116">Ancak, bu etiket erişilebilirlik gereksinimlerini karşılayacak şekilde değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="fb4e1-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="fb4e1-117">İlgili kişi numarası</span><span class="sxs-lookup"><span data-stu-id="fb4e1-117">Contact number</span></span> | <span data-ttu-id="fb4e1-118">Text</span><span class="sxs-lookup"><span data-stu-id="fb4e1-118">Text</span></span> | <span data-ttu-id="fb4e1-119">Siparişle ilgili sorular için bir ilgili kişi numarası sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="fb4e1-119">A contact number can be provided for order-related questions.</span></span> |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a><span data-ttu-id="fb4e1-120">Sipariş ayrıntıları sayfası modülünde kullanılabilen modüller</span><span class="sxs-lookup"><span data-stu-id="fb4e1-120">Modules that can be used on an order details page</span></span>

<span data-ttu-id="fb4e1-121">Sipariş Ayrıntıları sayfası oluşturduğunuzda, diğer ilgili modülleri de sipariş ayrıntıları modülünün yanı sıra ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fb4e1-121">When you create an order details page, you can add other relevant modules in addition to the order details module.</span></span> <span data-ttu-id="fb4e1-122">Burada bazı örnekler verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="fb4e1-122">Here are some examples:</span></span>

- <span data-ttu-id="fb4e1-123">**Öneriler modülü** – Müşteriye diğer ürünleri önermek için, sipariş onayı sayfasına öneri modülü koyulamıyor.</span><span class="sxs-lookup"><span data-stu-id="fb4e1-123">**Recommendations module** – The recommendations module can be added to the order details page to suggest other products to the customer.</span></span>
- <span data-ttu-id="fb4e1-124">**Pazarlama modülleri** – Pazarlama içeriğini göstermek için, sipariş ayrıntıları sayfasına herhangi bir pazarlama modülü eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="fb4e1-124">**Marketing modules** – Any marketing module can be added to the order details page to show marketing content.</span></span>

## <a name="add-an-order-details-module-to-a-page"></a><span data-ttu-id="fb4e1-125">Sayfaya sipariş ayrıntıları modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="fb4e1-125">Add an order details module to a page</span></span>

<span data-ttu-id="fb4e1-126">Bir yeni sayfaya sipariş ayrıntıları modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="fb4e1-126">To add an order details module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="fb4e1-127">Bir yeni şablonu oluşturmak için **Şablonlar** 'a gidin ve **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fb4e1-127">Go to **Templates** , and select **New** to create a new template.</span></span>
1. <span data-ttu-id="fb4e1-128">**Yeni Şablon** iletişim kutusunda **Şablon adı** altında, **Sipariş ayrıntıları şablonu** adını girin ve ve **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="fb4e1-128">In the **New Template** dialog box, under **Template name** , enter the name **Order details template** , and then select **OK**.</span></span>
1. <span data-ttu-id="fb4e1-129">**Gövde** yuvası için üç nokta ( **...** ) düğmesini seçin ve **Modül Ekle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fb4e1-129">In the **Body** slot, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="fb4e1-130">**Modül Ekle** iletişim kutusunda **Varsayılan sayfa** modülünü seçin ve **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="fb4e1-130">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="fb4e1-131">**Varsayılan sayfa** modülünde **ana** yuvayı seçin, üç nokta düğmesini ( **...** ) ve sonra **Modül ekle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fb4e1-131">In the **Main** slot of the **Default Page** module, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="fb4e1-132">**Modül Ekle** iletişim kutusunda **Sipariş ayrıntıları** modülünü seçin ve **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="fb4e1-132">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="fb4e1-133">**Kaydet** 'i seçin ve ardından şablonu önizlemek için **Önizleme** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fb4e1-133">Select **Save** , and then select **Preview** to preview the template.</span></span> <span data-ttu-id="fb4e1-134">Sipariş ayrıntıları numarasının bağlamını gerektirdiğinden, sipariş teyidi modülü işlenmemelidir.</span><span class="sxs-lookup"><span data-stu-id="fb4e1-134">The order details module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="fb4e1-135">Şablonu iade etmek için **Düzenlemeyi bitir** 'i seçin, ardından yayımlamak için **Yayımla** 'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="fb4e1-135">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="fb4e1-136">**Sayfalar** 'a gidin ve yeni sayfa oluşturmak için **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fb4e1-136">Go to **Pages** , and select **New** to create a new page.</span></span>
1. <span data-ttu-id="fb4e1-137">**Şablon seç** iletişim kutusunda **Sipariş ayrıntıları şablonu** 'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="fb4e1-137">In the **Choose a template** dialog box, select **Order details template**.</span></span> <span data-ttu-id="fb4e1-138">**Sayfa adı** altından **Sipariş ayrıntıları sayfası** girin ve **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="fb4e1-138">Under **Page name** , enter **Order details page** , and then select **OK**.</span></span>
1. <span data-ttu-id="fb4e1-139">**Varsayılan sayfa** modülünde **ana** yuvayı seçin, üç nokta düğmesini ( **...** ) ve sonra **Modül ekle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fb4e1-139">In the **Main** slot of the **Default Page** module, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="fb4e1-140">**Modül Ekle** iletişim kutusunda **Sipariş ayrıntıları** modülünü seçin ve **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="fb4e1-140">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="fb4e1-141">Sipariş ayrıntılatı modülünün özellikler bölmesinde, kurşun kalem simgesinin yanındaki **Başlık** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="fb4e1-141">In the properties pane for the order details module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="fb4e1-142">**Başlık** iletişim kutusunun **Başlık Metni** alanında, **Sipairş ayrıntıları** başlık metnini girin ve ardından **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="fb4e1-142">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order details** , and then select **OK**.</span></span>
1. <span data-ttu-id="fb4e1-143">**Kaydet** 'i seçin ve ardından sayfayı önizlemek için **Önizleme** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fb4e1-143">Select **Save** , and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="fb4e1-144">Sayfayı iade etmek için **Düzenlemeyi bitir** 'i seçin, ardından yayımlamak için **Yayımla** 'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="fb4e1-144">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fb4e1-145">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="fb4e1-145">Additional resources</span></span>

[<span data-ttu-id="fb4e1-146">Sepet modülü</span><span class="sxs-lookup"><span data-stu-id="fb4e1-146">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="fb4e1-147">Sepet simgesi modülü</span><span class="sxs-lookup"><span data-stu-id="fb4e1-147">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="fb4e1-148">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="fb4e1-148">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="fb4e1-149">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="fb4e1-149">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="fb4e1-150">Sevkiyat adresi modülü</span><span class="sxs-lookup"><span data-stu-id="fb4e1-150">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="fb4e1-151">Teslimat seçenekleri modülü</span><span class="sxs-lookup"><span data-stu-id="fb4e1-151">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="fb4e1-152">Hediye kartı modülü</span><span class="sxs-lookup"><span data-stu-id="fb4e1-152">Gift card module</span></span>](add-giftcard.md)
