---
title: Kanal gezinme hiyerarşisi oluşturma
description: Bu konuda, Microsoft Dynamics 365 Commerce'te bir kanal gezinme hiyerarşisinin nasıl oluşturulacağı açıklanmaktadır.
author: samjarawan
ms.date: 01/27/2020
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
ms.openlocfilehash: 358f3d40c7a21184c20da342d6b2bf72dd4e7bbd
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795847"
---
# <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="4c941-103">Kanal gezinme hiyerarşisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="4c941-103">Create a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="4c941-104">Bu konuda, Microsoft Dynamics 365 Commerce'te bir kanal gezinme hiyerarşisinin nasıl oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="4c941-104">This topic describes how to create a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4c941-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="4c941-105">Overview</span></span>

<span data-ttu-id="4c941-106">Kanal gezinme hiyerarşisi, ürünleri gruplandırıp kategoriler halinde düzenleyerek ürünlere çevrimiçi veya satış noktasında (POS) göz atılabilmesi için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4c941-106">A channel navigation hierarchy is used to group and organize products into categories so that the products can be browsed online or in point of sale (POS).</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="4c941-107">Kanal gezinme hiyerarşisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="4c941-107">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="4c941-108">Kanal gezinti hiyerarşisi oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4c941-108">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="4c941-109">Gezinti bölmesinde, **Modüller \> Retail and commerce \> Ürünler ve kategoriler \> Kanal gezinme kategorileri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="4c941-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Channel navigation categories**.</span></span>
1. <span data-ttu-id="4c941-110">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4c941-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="4c941-111">**Ad** kutusuna bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="4c941-111">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="4c941-112">**Açıklama** kutusuna bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="4c941-112">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="4c941-113">**Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="4c941-113">Select **Create**.</span></span>
1. <span data-ttu-id="4c941-114">Eylem bölmesinde, kök düğüm oluşturmak için **Yeni kategori düğümü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="4c941-114">On the action pane, select **New category node** to create a root node.</span></span>
1. <span data-ttu-id="4c941-115">**Ad** kutusuna bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="4c941-115">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="4c941-116">**Açıklama** kutusuna bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="4c941-116">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="4c941-117">**Kolay ad** kutusuna bir kolay ad girin.</span><span class="sxs-lookup"><span data-stu-id="4c941-117">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="4c941-118">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4c941-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="4c941-119">Aşağıdaki resimde örnek bir kök düğüm gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="4c941-119">The following image shows a example root node.</span></span>

![Örnek kök düğüm](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a><span data-ttu-id="4c941-121">Gezinme kategorisi düğümleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="4c941-121">Create navigation category nodes</span></span>

<span data-ttu-id="4c941-122">Kanaldaki ürün kategorilerini temsil edecek ek gezinme kategorisi düğümleri oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4c941-122">To create any additional navigation category nodes to represent the product categories on the channel, follow these steps.</span></span>

1. <span data-ttu-id="4c941-123">Gezinti bölmesinde, kategori eklenecek ana düğümü seçin.</span><span class="sxs-lookup"><span data-stu-id="4c941-123">In the navigation pane, select the parent node to add a category to.</span></span>
1. <span data-ttu-id="4c941-124">Eylem bölmesinde **Yeni kategori düğümü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="4c941-124">On the action pane, select **New category node**.</span></span>
1. <span data-ttu-id="4c941-125">**Ad** kutusuna bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="4c941-125">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="4c941-126">**Açıklama** kutusuna bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="4c941-126">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="4c941-127">**Kolay ad** kutusuna bir kolay ad girin.</span><span class="sxs-lookup"><span data-stu-id="4c941-127">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="4c941-128">**Görüntüleme sırası** kutusuna bir görüntüleme sırası girin (isteğe bağlı).</span><span class="sxs-lookup"><span data-stu-id="4c941-128">In the **Display order** box, enter a display order (optional).</span></span>
1. <span data-ttu-id="4c941-129">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4c941-129">On the action pane, select **Save**.</span></span>

<span data-ttu-id="4c941-130">Aşağıdaki resimde, tamamlanmış kanal gezinme hiyerarşisinin bir örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="4c941-130">The following image shows an example of a completed channel navigation hierarchy.</span></span>

![Örnek kanal hiyerarşisi](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a><span data-ttu-id="4c941-132">Kategori düğümlerine ürünler ekleme</span><span class="sxs-lookup"><span data-stu-id="4c941-132">Add products to category nodes</span></span>

<span data-ttu-id="4c941-133">Kategori düğümlerine ürünler eklemek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4c941-133">To add products to category nodes, follow these steps.</span></span>

1. <span data-ttu-id="4c941-134">Bir kategori düğümü seçin.</span><span class="sxs-lookup"><span data-stu-id="4c941-134">Select a category node.</span></span>
1. <span data-ttu-id="4c941-135">**Ürünler** altında, **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4c941-135">Under **Products**, select **Add**.</span></span>
1. <span data-ttu-id="4c941-136">Ürün numarası veya ürün adı kullanarak eklemek istediğiniz yeni ürünü veya ürünleri bulun ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4c941-136">Find the new product(s) you want to add using product number or product name, and then select **OK**.</span></span>
1. <span data-ttu-id="4c941-137">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4c941-137">On the action pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="4c941-138">Kanal gezinme hiyerarşisi içinde bir düğüme ürünlerin eklenmesi, ürünlerin seçili bir kanalda görünmesi için yeterli değildir; ürünlerin bir ürünle ilişkili olması da gereklidir.</span><span class="sxs-lookup"><span data-stu-id="4c941-138">Adding products to a node inside the channel navigation hierarchy is not sufficient for the products to show up on a selected channel, the products must also be assorted to a product.</span></span>

<span data-ttu-id="4c941-139">Aşağıdaki resimde, ürünler eklenmiş bir düğüm örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="4c941-139">The following image shows an example node with products added.</span></span>

![Kategori düğümüne ürünler ekleme](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a><span data-ttu-id="4c941-141">Kategori düğümlerine ürün öznitelik grupları ekleme</span><span class="sxs-lookup"><span data-stu-id="4c941-141">Add product attribute groups to category nodes</span></span>

> [!NOTE]
> <span data-ttu-id="4c941-142">Öznitelik gruplarını kanal gezinme hiyerarşisinin içindeki bir düğüme ekleyebilmeniz için önce bu grupların oluşturulması gerekir.</span><span class="sxs-lookup"><span data-stu-id="4c941-142">Attribute groups must be created before you can add them to a node inside the channel navigation hierarchy.</span></span>

<span data-ttu-id="4c941-143">Kategori düğümüne ürün öznitelik grubu eklemek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4c941-143">To add product an attribute group to a category node, follow these steps.</span></span>

1. <span data-ttu-id="4c941-144">Bir kategori düğümü seçin.</span><span class="sxs-lookup"><span data-stu-id="4c941-144">Select a category node.</span></span>
1. <span data-ttu-id="4c941-145">**Ürün öznitelik grubu** altında, **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4c941-145">Under **Product attribute group**, select **Add**.</span></span>
1. <span data-ttu-id="4c941-146">Eklemek istediğiniz öznitelik grubunu veya gruplarını bulun ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4c941-146">Find the attribute group(s) you would like to add, and then select **OK**.</span></span>
1. <span data-ttu-id="4c941-147">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4c941-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="4c941-148">Aşağıdaki resimde, ürün öznitelik grupları eklenmiş bir düğüm örneği gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="4c941-148">The following image shows a sample node with product attribute groups added.</span></span>

![Düğümdeki ürün öznitelik grupları](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a><span data-ttu-id="4c941-150">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="4c941-150">Additional resources</span></span>

[<span data-ttu-id="4c941-151">Ürün çeşitlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="4c941-151">Set up assortments</span></span>](set-up-assortments.md)

[<span data-ttu-id="4c941-152">Öznitelikleri ve öznitelik gruplarını yönetme</span><span class="sxs-lookup"><span data-stu-id="4c941-152">Manage attributes and attribute groups</span></span>](attribute-attributegroups-lifecycle.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]