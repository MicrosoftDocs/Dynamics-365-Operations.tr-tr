---
title: Kanal gezinme hiyerarşisi oluşturma
description: Bu konuda, Microsoft Dynamics 365 Commerce'te bir kanal gezinme hiyerarşisinin nasıl oluşturulacağı açıklanmaktadır.
author: samjarawan
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 5df46de9dadfa0b7160a9b340ef36fdf963a0ad3
ms.sourcegitcommit: 6c2f5c3b038f696532c335e20b0fbafa155d6858
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951920"
---
# <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="90276-103">Kanal gezinme hiyerarşisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="90276-103">Create a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="90276-104">Bu konuda, Microsoft Dynamics 365 Commerce'te bir kanal gezinme hiyerarşisinin nasıl oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="90276-104">This topic describes how to create a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="90276-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="90276-105">Overview</span></span>

<span data-ttu-id="90276-106">Kanal gezinme hiyerarşisi, ürünleri gruplandırıp kategoriler halinde düzenleyerek ürünlere çevrimiçi veya satış noktasında (POS) göz atılabilmesi için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="90276-106">A channel navigation hierarchy is used to group and organize products into categories so that the products can be browsed online or in point of sale (POS).</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="90276-107">Kanal gezinme hiyerarşisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="90276-107">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="90276-108">Kanal gezinti hiyerarşisi oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="90276-108">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="90276-109">Gezinti bölmesinde, **Modüller \> Retail and commerce \> Ürünler ve kategoriler \> Kanal gezinme kategorileri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="90276-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Channel navigation categories**.</span></span>
1. <span data-ttu-id="90276-110">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="90276-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="90276-111">**Ad** kutusuna bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="90276-111">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="90276-112">**Açıklama** kutusuna bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="90276-112">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="90276-113">**Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="90276-113">Select **Create**.</span></span>
1. <span data-ttu-id="90276-114">Eylem bölmesinde, kök düğüm oluşturmak için **Yeni kategori düğümü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="90276-114">On the action pane, select **New category node** to create a root node.</span></span>
1. <span data-ttu-id="90276-115">**Ad** kutusuna bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="90276-115">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="90276-116">**Açıklama** kutusuna bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="90276-116">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="90276-117">**Kolay ad** kutusuna bir kolay ad girin.</span><span class="sxs-lookup"><span data-stu-id="90276-117">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="90276-118">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="90276-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="90276-119">Aşağıdaki resimde örnek bir kök düğüm gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="90276-119">The following image shows a example root node.</span></span>

![Örnek kök düğüm](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a><span data-ttu-id="90276-121">Gezinme kategorisi düğümleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="90276-121">Create navigation category nodes</span></span>

<span data-ttu-id="90276-122">Kanaldaki ürün kategorilerini temsil edecek ek gezinme kategorisi düğümleri oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="90276-122">To create any additional navigation category nodes to represent the product categories on the channel, follow these steps.</span></span>

1. <span data-ttu-id="90276-123">Gezinti bölmesinde, kategori eklenecek ana düğümü seçin.</span><span class="sxs-lookup"><span data-stu-id="90276-123">In the navigation pane, select the parent node to add a category to.</span></span>
1. <span data-ttu-id="90276-124">Eylem bölmesinde **Yeni kategori düğümü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="90276-124">On the action pane, select **New category node**.</span></span>
1. <span data-ttu-id="90276-125">**Ad** kutusuna bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="90276-125">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="90276-126">**Açıklama** kutusuna bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="90276-126">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="90276-127">**Kolay ad** kutusuna bir kolay ad girin.</span><span class="sxs-lookup"><span data-stu-id="90276-127">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="90276-128">**Görüntüleme sırası** kutusuna bir görüntüleme sırası girin (isteğe bağlı).</span><span class="sxs-lookup"><span data-stu-id="90276-128">In the **Display order** box, enter a display order (optional).</span></span>
1. <span data-ttu-id="90276-129">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="90276-129">On the action pane, select **Save**.</span></span>

<span data-ttu-id="90276-130">Aşağıdaki resimde, tamamlanmış kanal gezinme hiyerarşisinin bir örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="90276-130">The following image shows an example of a completed channel navigation hierarchy.</span></span>

![Örnek kanal hiyerarşisi](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a><span data-ttu-id="90276-132">Kategori düğümlerine ürünler ekleme</span><span class="sxs-lookup"><span data-stu-id="90276-132">Add products to category nodes</span></span>

<span data-ttu-id="90276-133">Kategori düğümlerine ürünler eklemek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="90276-133">To add products to category nodes, follow these steps.</span></span>

1. <span data-ttu-id="90276-134">Bir kategori düğümü seçin.</span><span class="sxs-lookup"><span data-stu-id="90276-134">Select a category node.</span></span>
1. <span data-ttu-id="90276-135">**Ürünler** altında, **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="90276-135">Under **Products**, select **Add**.</span></span>
1. <span data-ttu-id="90276-136">Ürün numarası veya ürün adı kullanarak eklemek istediğiniz yeni ürünü veya ürünleri bulun ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="90276-136">Find the new product(s) you want to add using product number or product name, and then select **OK**.</span></span>
1. <span data-ttu-id="90276-137">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="90276-137">On the action pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="90276-138">Kanal gezinme hiyerarşisi içinde bir düğüme ürünlerin eklenmesi, ürünlerin seçili bir kanalda görünmesi için yeterli değildir; ürünlerin bir kanalla ilişkili olması da gereklidir.</span><span class="sxs-lookup"><span data-stu-id="90276-138">Adding products to a node inside the channel navigation hierarchy is not sufficient for the products to show up on a selected channel, the products must also be assorted to a channel.</span></span> <span data-ttu-id="90276-139">Ürün çeşitleri hakkında daha fazla bilgi için bkz. [Ürün çeşitleri yönetimi](assortments.md).</span><span class="sxs-lookup"><span data-stu-id="90276-139">For more information on assortments, see [Assortment management](assortments.md).</span></span>

<span data-ttu-id="90276-140">Aşağıdaki resimde, ürünler eklenmiş bir düğüm örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="90276-140">The following image shows an example node with products added.</span></span>

![Kategori düğümüne ürünler ekleme](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a><span data-ttu-id="90276-142">Kategori düğümlerine ürün öznitelik grupları ekleme</span><span class="sxs-lookup"><span data-stu-id="90276-142">Add product attribute groups to category nodes</span></span>

> [!NOTE]
> <span data-ttu-id="90276-143">Öznitelik gruplarını kanal gezinme hiyerarşisinin içindeki bir düğüme ekleyebilmeniz için önce bu grupların oluşturulması gerekir.</span><span class="sxs-lookup"><span data-stu-id="90276-143">Attribute groups must be created before you can add them to a node inside the channel navigation hierarchy.</span></span>

<span data-ttu-id="90276-144">Kategori düğümüne ürün öznitelik grubu eklemek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="90276-144">To add product an attribute group to a category node, follow these steps.</span></span>

1. <span data-ttu-id="90276-145">Bir kategori düğümü seçin.</span><span class="sxs-lookup"><span data-stu-id="90276-145">Select a category node.</span></span>
1. <span data-ttu-id="90276-146">**Ürün öznitelik grubu** altında, **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="90276-146">Under **Product attribute group**, select **Add**.</span></span>
1. <span data-ttu-id="90276-147">Eklemek istediğiniz öznitelik grubunu veya gruplarını bulun ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="90276-147">Find the attribute group(s) you would like to add, and then select **OK**.</span></span>
1. <span data-ttu-id="90276-148">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="90276-148">On the action pane, select **Save**.</span></span>

<span data-ttu-id="90276-149">Aşağıdaki resimde, ürün öznitelik grupları eklenmiş bir düğüm örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="90276-149">The following image shows a sample node with product attribute groups added.</span></span>

![Düğümdeki ürün öznitelik grupları](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a><span data-ttu-id="90276-151">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="90276-151">Additional resources</span></span>

[<span data-ttu-id="90276-152">Ürün çeşitlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="90276-152">Set up assortments</span></span>](set-up-assortments.md)

[<span data-ttu-id="90276-153">Öznitelikleri ve öznitelik gruplarını yönetme</span><span class="sxs-lookup"><span data-stu-id="90276-153">Manage attributes and attribute groups</span></span>](attribute-attributegroups-lifecycle.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
