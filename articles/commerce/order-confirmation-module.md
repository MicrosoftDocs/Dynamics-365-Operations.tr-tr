---
title: Sipariş ayrıntıları modülü
description: Bu konu sipariş ayrıntıları modüllerini ve bunların nasıl Microsoft Dynamics 365 Commerce'te oluşturacağını açıklamaktadır ve kapsamaktadır.
author: anupamar
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: cb09a0b6ce1e48707f96021e9fad0006d9c1c55c
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026029"
---
# <a name="order-details-module"></a><span data-ttu-id="fcbea-103">Sipariş ayrıntıları modülü</span><span class="sxs-lookup"><span data-stu-id="fcbea-103">Order details module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="fcbea-104">Bu konu sipariş ayrıntıları modüllerini ve bunların nasıl Microsoft Dynamics 365 Commerce'te oluşturacağını açıklamaktadır ve kapsamaktadır.</span><span class="sxs-lookup"><span data-stu-id="fcbea-104">This topic covers order details modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fcbea-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="fcbea-105">Overview</span></span>

<span data-ttu-id="fcbea-106">Bir sipariş yerleştirildikten sonra, onay ayrıntılarını göstermek için sipariş ayrıntıları modülü kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="fcbea-106">The order details module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="fcbea-107">Sipariş onay kodunu, sipariş iletişim bilgilerini ve satın alınan maddeler, ödeme bilgileri ve sevkiyat yöntemi gibi diğer sipariş ayrıntılarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fcbea-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="fcbea-108">Sipariş onayı modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="fcbea-108">Order confirmation module properties</span></span>

| <span data-ttu-id="fcbea-109">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="fcbea-109">Property name</span></span>  | <span data-ttu-id="fcbea-110">Değerler</span><span class="sxs-lookup"><span data-stu-id="fcbea-110">Values</span></span> | <span data-ttu-id="fcbea-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="fcbea-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="fcbea-112">Başlık</span><span class="sxs-lookup"><span data-stu-id="fcbea-112">Heading</span></span>        | <span data-ttu-id="fcbea-113">Başlık metni ve başlık etiketi (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**)</span><span class="sxs-lookup"><span data-stu-id="fcbea-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="fcbea-114">Sipariş teyidi modülünün başlığı olabilir.</span><span class="sxs-lookup"><span data-stu-id="fcbea-114">The order confirmation module can have a heading.</span></span> <span data-ttu-id="fcbea-115">Varsayılan olarak, başlık için **H2** başlık etiketi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fcbea-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="fcbea-116">Ancak, bu etiket erişilebilirlik gereksinimlerini karşılayacak şekilde değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="fcbea-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="fcbea-117">İlgili kişi numarası</span><span class="sxs-lookup"><span data-stu-id="fcbea-117">Contact number</span></span> | <span data-ttu-id="fcbea-118">Text</span><span class="sxs-lookup"><span data-stu-id="fcbea-118">Text</span></span> | <span data-ttu-id="fcbea-119">Siparişle ilgili sorular için bir ilgili kişi numarası sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="fcbea-119">A contact number can be provided for order-related questions.</span></span> |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a><span data-ttu-id="fcbea-120">Sipariş ayrıntıları sayfası modülünde kullanılabilen modüller</span><span class="sxs-lookup"><span data-stu-id="fcbea-120">Modules that can be used on an order details page</span></span>

<span data-ttu-id="fcbea-121">Sipariş Ayrıntıları sayfası oluşturduğunuzda, diğer ilgili modülleri de sipariş ayrıntıları modülünün yanı sıra ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fcbea-121">When you create an order details page, you can add other relevant modules in addition to the order details module.</span></span> <span data-ttu-id="fcbea-122">Burada bazı örnekler verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="fcbea-122">Here are some examples:</span></span>

- <span data-ttu-id="fcbea-123">**Öneriler modülü** – Müşteriye diğer ürünleri önermek için, sipariş onayı sayfasına öneri modülü koyulamıyor.</span><span class="sxs-lookup"><span data-stu-id="fcbea-123">**Recommendations module** – The recommendations module can be added to the order details page to suggest other products to the customer.</span></span>
- <span data-ttu-id="fcbea-124">**Pazarlama modülleri** – Pazarlama içeriğini göstermek için, sipariş ayrıntıları sayfasına herhangi bir pazarlama modülü eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="fcbea-124">**Marketing modules** – Any marketing module can be added to the order details page to show marketing content.</span></span>

## <a name="create-an-order-details-page-module"></a><span data-ttu-id="fcbea-125">Sipariş ayrıntıları sayfa modülü oluşturma</span><span class="sxs-lookup"><span data-stu-id="fcbea-125">Create an order details page module</span></span>

1. <span data-ttu-id="fcbea-126">**Sipariş ayrıntıları şablonu** adlı bir sayfa şablonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="fcbea-126">Create a page template that is named **Order details template**.</span></span>
1. <span data-ttu-id="fcbea-127">Varsayılan sayfanın **ana** yuvasına bir sipariş ayrıntıları modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="fcbea-127">In the **Main** slot of the default page, add an order details module.</span></span>
1. <span data-ttu-id="fcbea-128">Sipariş ayrıntıları modülünde bir öneri modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="fcbea-128">In the order details module, add a recommendations module.</span></span>
1. <span data-ttu-id="fcbea-129">Şablonu kaydet ve önizleyin.</span><span class="sxs-lookup"><span data-stu-id="fcbea-129">Save and preview the template.</span></span> <span data-ttu-id="fcbea-130">Sipariş ayrıntıları numarasının bağlamını gerektirdiğinden, sipariş teyidi modülü işlenmemelidir.</span><span class="sxs-lookup"><span data-stu-id="fcbea-130">The order details module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="fcbea-131">Şablon düzenlemeyi tamamlayın ve sonra yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="fcbea-131">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="fcbea-132">**Sipariş ayrıntıları sayfası** adlı bir sayfa oluşturmak için yeni oluşturduğunuz sipariş ayrıntıları şablonunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="fcbea-132">Use the order details template that you just created to create a page that is named **order details page**.</span></span>
1. <span data-ttu-id="fcbea-133">Sayfa anahattına varsayılan sayfayı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="fcbea-133">Add the default page to the page outline.</span></span>
1. <span data-ttu-id="fcbea-134">**Üstbilgi** yuvasında bir üstbilgi parçası ekleyin.</span><span class="sxs-lookup"><span data-stu-id="fcbea-134">In the **Header** slot, add a header fragment.</span></span>
1. <span data-ttu-id="fcbea-135">**Altbilgi** yuvasında bir altbilgi parçası ekleyin.</span><span class="sxs-lookup"><span data-stu-id="fcbea-135">In the **Footer** slot, add a footer fragment.</span></span>
1. <span data-ttu-id="fcbea-136">**Ana** yuvasına bir sipariş ayrıntıları modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="fcbea-136">In the **Main** slot, add an order details module.</span></span>
1. <span data-ttu-id="fcbea-137">Sipariş ayrıntıları modülünün Özellik bölmesinde Başlık **Sipariş ayrıntıları** ekleyin.</span><span class="sxs-lookup"><span data-stu-id="fcbea-137">In the property pane for the order details module, add the heading **Order details**.</span></span>
1. <span data-ttu-id="fcbea-138">Sipariş ayrıntıları modülünün altında, bir öneri modülü ekleyin ve bunu **yeni** ve **en iyi satış** ayarlarını kullanacak şekilde konfigüre edin.</span><span class="sxs-lookup"><span data-stu-id="fcbea-138">Below the order details module, add a recommendations module, and configure it so that it uses the **New** and **Best Selling** settings.</span></span>
1. <span data-ttu-id="fcbea-139">Sayfayı kaydet ve önizleyin.</span><span class="sxs-lookup"><span data-stu-id="fcbea-139">Save and preview the page.</span></span>
1. <span data-ttu-id="fcbea-140">Sayfayı düzenlemeyi tamamlayın ve sonra yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="fcbea-140">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fcbea-141">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="fcbea-141">Additional resources</span></span>

[<span data-ttu-id="fcbea-142">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="fcbea-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="fcbea-143">Konteyner modülü</span><span class="sxs-lookup"><span data-stu-id="fcbea-143">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="fcbea-144">Satınalma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="fcbea-144">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="fcbea-145">Sepet modülü</span><span class="sxs-lookup"><span data-stu-id="fcbea-145">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="fcbea-146">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="fcbea-146">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="fcbea-147">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="fcbea-147">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="fcbea-148">Alt bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="fcbea-148">Footer module</span></span>](author-footer-module.md)
