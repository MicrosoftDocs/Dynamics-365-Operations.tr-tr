---
title: Çeşit grubu oluşturma
description: Bu konuda, Microsoft Dynamics 365 Commerce'te bir ürün için boyut, stil veya renk çeşidi grubunun nasıl oluşturulacağı açıklanmaktadır.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
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
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b9acd41c000b22e6c74b0d636a7f58917e4b5ac5
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001887"
---
# <a name="create-a-variant-group"></a><span data-ttu-id="febb6-103">Çeşit grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="febb6-103">Create a variant group</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="febb6-104">Bu konuda, Microsoft Dynamics 365 Commerce'te bir ürün için boyut, stil veya renk çeşidi grubunun nasıl oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="febb6-104">This topic describes how to create a size, style, or color variant group for a product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="febb6-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="febb6-105">Overview</span></span>

<span data-ttu-id="febb6-106">Dynamics 365 Commerce, ürünler için birden çok çeşidi destekliyor.</span><span class="sxs-lookup"><span data-stu-id="febb6-106">Dynamics 365 Commerce supports multiple variants for products.</span></span> <span data-ttu-id="febb6-107">Farklı ürün kategorileri için çeşit grupları ayarlamak idealdir.</span><span class="sxs-lookup"><span data-stu-id="febb6-107">It is ideal to set up variant groups for different product categories.</span></span> <span data-ttu-id="febb6-108">Örneğin, çok küçük, küçük, orta, büyük ve ekstra büyük boyutlarda tişörtler için bir boyut grubu oluşturulabilir veya bir ürünün mevcut tüm renklerini eklemek için bir renk grubu oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="febb6-108">For example, a size group can be created for t-shirts with sizes extra small, small, medium, large, and extra large, or a color group could be created to include all available colors of a product.</span></span> <span data-ttu-id="febb6-109">Ürünler eklenmeden önce çeşit grupları eklenmelidir.</span><span class="sxs-lookup"><span data-stu-id="febb6-109">Variant groups should be added before products are added.</span></span>

<span data-ttu-id="febb6-110">Bu konuda, bir boyut grubu oluşturulacak ve yapılandırılacak.</span><span class="sxs-lookup"><span data-stu-id="febb6-110">In this topic, a size group will be created and configured.</span></span> <span data-ttu-id="febb6-111">Stil gruplarını ve renk gruplarını ekleyip yapılandırmak için benzer yordamlar kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="febb6-111">Similar procedures can be used for adding and configuring style groups and color groups.</span></span>

## <a name="create-a-size-group"></a><span data-ttu-id="febb6-112">Boyut grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="febb6-112">Create a size group</span></span>

<span data-ttu-id="febb6-113">Boyut grubu oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="febb6-113">To create a size group, follow these steps.</span></span>
 
1. <span data-ttu-id="febb6-114">Gezinti bölmesinde, **Modüller \> Retail and commerce \> Ürünler ve kategoriler \> Çeşit grupları \> Boyut grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="febb6-114">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**.</span></span>
1. <span data-ttu-id="febb6-115">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="febb6-115">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="febb6-116">**Boyut grubu** kutusuna, boyut grubu için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="febb6-116">In the **Size group** box, enter a name for the size group.</span></span>
1. <span data-ttu-id="febb6-117">**Açıklama** kutusuna, uygun bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="febb6-117">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="febb6-118">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="febb6-118">On the action pane, select **Save**.</span></span>

## <a name="add-attributes-to-the-size-group"></a><span data-ttu-id="febb6-119">Boyut grubuna öznitelikler ekleme</span><span class="sxs-lookup"><span data-stu-id="febb6-119">Add attributes to the size group</span></span>

<span data-ttu-id="febb6-120">Bir boyut grubuna öznitelikler eklemek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="febb6-120">To add attributes to a size group, follow these steps.</span></span>

1. <span data-ttu-id="febb6-121">Gezinti bölmesinde, **Modüller \> Retail and commerce \> Ürünler ve kategoriler \> Çeşit grupları \> Boyut grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="febb6-121">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**</span></span>
1. <span data-ttu-id="febb6-122">Gezinti bölmesinde bir boyut grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="febb6-122">In the navigation pane, select a size group.</span></span>
1. <span data-ttu-id="febb6-123">**Boyut grubu satırları** altında, **Ekle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="febb6-123">Under **Size group lines**, select **Add**.</span></span>
1. <span data-ttu-id="febb6-124">**Boyut** kutusuna, boyutu temsil eden bir dize girin (örneğin "XL").</span><span class="sxs-lookup"><span data-stu-id="febb6-124">In the **Size** box, enter a string representing the size (for example, "XL").</span></span>
1. <span data-ttu-id="febb6-125">**Boyut adı** kutusuna boyut için bir ad girin (örneğin, "Çok Büyük").</span><span class="sxs-lookup"><span data-stu-id="febb6-125">In the **Size name** box, enter a name for the size (for example, "Extra Large").</span></span>
1. <span data-ttu-id="febb6-126">**Stok yenileme ağırlığı** kutusuna, stok yenileme ağırlığını temsil eden bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="febb6-126">In the **Replenishment weight** box, enter a number representing the replenishment weight.</span></span>
1. <span data-ttu-id="febb6-127">**Barkoddaki sayı** kutusunda, barkodu temsil eden bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="febb6-127">In the **Number in bar code** box, enter a number representing the bar code.</span></span>
1. <span data-ttu-id="febb6-128">**Görüntüleme sırası** kutusuna, görüntüleme sırasını temsil eden bir numara girin.</span><span class="sxs-lookup"><span data-stu-id="febb6-128">In the **Display order** box, enter a number representing the display order.</span></span>
1. <span data-ttu-id="febb6-129">Boyutları eklemeyi bitirince, eylem bölmesinde **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="febb6-129">When finished adding sizes, select **Save** on the action pane.</span></span>

<span data-ttu-id="febb6-130">Aşağıdaki resimde, "tişört boyutları" için bir boyut grubu örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="febb6-130">The following image shows an example of a size group for "casual shirt sizes".</span></span>

![Boyut grubu oluşturma](media/create-variant-group.png)

## <a name="additional-resources"></a><span data-ttu-id="febb6-132">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="febb6-132">Additional resources</span></span>

[<span data-ttu-id="febb6-133">Ürün bilgilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="febb6-133">Product information overview</span></span>](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="febb6-134">Perakende ürünlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="febb6-134">Set up retail products</span></span>](set-up-retail-products.md)

[<span data-ttu-id="febb6-135">Ürün boyutları</span><span class="sxs-lookup"><span data-stu-id="febb6-135">Product dimensions</span></span>](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)
