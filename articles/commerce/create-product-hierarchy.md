---
title: Yeni bir ürün hiyerarşisi oluşturma
description: Bu konuda, Microsoft Dynamics 365 Commerce'te yeni ürün hiyerarşisinin nasıl oluşturulacağı açıklanmaktadır.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: c7d0c792a8590be474b05dea262ae11d15e0ada3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965235"
---
# <a name="create-a-new-product-hierarchy"></a><span data-ttu-id="10435-103">Yeni bir ürün hiyerarşisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="10435-103">Create a new product hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="10435-104">Bu konuda, Microsoft Dynamics 365 Commerce'te yeni ürün hiyerarşisinin nasıl oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="10435-104">This topic describes how to create a new product hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="10435-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="10435-105">Overview</span></span>

<span data-ttu-id="10435-106">Dynamics 365 Commerce birden fazla perakende kanalı destekler.</span><span class="sxs-lookup"><span data-stu-id="10435-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="10435-107">Bu perakende kanalları çevrimiçi mağazaları, çağrı merkezlerini ve perakende mağazalarını (tuğla dibek mağazalar olarak da bilinir) içerir.</span><span class="sxs-lookup"><span data-stu-id="10435-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="10435-108">Her perakende mağaza kanalının kendi ödeme türleri, fiyat grupları, satış noktası (POS) kasaları, gelir hesapları ve gider hesapları ve personeli olabilir.</span><span class="sxs-lookup"><span data-stu-id="10435-108">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="10435-109">Bir perakende mağaza kanalı oluşturabilmeniz için tüm bu öğeleri ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="10435-109">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="10435-110">Kuruluşunuzun genel ürün hiyerarşisini tanımlamak için bir Commerce ürün hiyerarşisi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="10435-110">A Commerce product hierarchy is used to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="10435-111">Alım satım, fiyatlandırma ve promosyonlar, raporlama ve ürün çeşidi planlaması için bir Commerce ürün hiyerarşisi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="10435-111">You can use a Commerce product hierarchy for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="10435-112">Kuruluş başına yalnızca bir Commerce ürün hiyerarşisi atanabilir.</span><span class="sxs-lookup"><span data-stu-id="10435-112">Only one Commerce product hierarchy can be assigned per organization.</span></span>

## <a name="create-and-configure-a-product-hierarchy"></a><span data-ttu-id="10435-113">Ürün hiyerarşisini oluşturma ve yapılandırma</span><span class="sxs-lookup"><span data-stu-id="10435-113">Create and configure a product hierarchy</span></span>

<span data-ttu-id="10435-114">Bir Commerce ürün hiyerarşisi oluşturmak ve yapılandırmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="10435-114">To create and configure a Commerce product hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="10435-115">Gezinti bölmesinde, **Modüller \> Retail and commerce \> Ürünler ve kategoriler \> Commerce ürün hiyerarşisi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="10435-115">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Commerce product hierarchy**.</span></span>
1. <span data-ttu-id="10435-116">Henüz bir hiyerarşi yoksa, hiyerarşinin kökünü oluşturmak için **Eylem bölmesinde** **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="10435-116">If no hierachy exists yet, on the **Action pane**, select **New** to create the root of the hierarchy.</span></span>
1. <span data-ttu-id="10435-117">**Genel** altında:</span><span class="sxs-lookup"><span data-stu-id="10435-117">Under **General**:</span></span>
    1. <span data-ttu-id="10435-118">**Ad** kutusuna bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="10435-118">In the **Name** box, enter a name.</span></span>
    1. <span data-ttu-id="10435-119">**Açıklama** kutusuna bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="10435-119">In the **Description** box, enter a description.</span></span>
    1. <span data-ttu-id="10435-120">**Kolay ad** kutusuna bir kolay ad girin.</span><span class="sxs-lookup"><span data-stu-id="10435-120">In the **Friendly name** box, enter a friendly name.</span></span>
    1. <span data-ttu-id="10435-121">**Etkin** ayarını **Evet** yapın.</span><span class="sxs-lookup"><span data-stu-id="10435-121">Set **Active** to **Yes**.</span></span>

## <a name="add-hierarchy-nodes"></a><span data-ttu-id="10435-122">Hiyerarşi düğümleri ekleme</span><span class="sxs-lookup"><span data-stu-id="10435-122">Add hierarchy nodes</span></span>

<span data-ttu-id="10435-123">Hiyerarşi düğümleri eklemek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="10435-123">To add hierarchy nodes, follow these steps.</span></span>

1. <span data-ttu-id="10435-124">Eylem bölmesinde **Kategori hiyerarşisini düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="10435-124">On the action pane, select **Edit category hierarchy**.</span></span>
1. <span data-ttu-id="10435-125">Yeni düğüm eklemek istediğiniz üst düğümü ve ardından **Yeni kategori düğümü**' nü seçin.</span><span class="sxs-lookup"><span data-stu-id="10435-125">Select the parent node you want to add a new node to, and then select **New category node**.</span></span>
1. <span data-ttu-id="10435-126">**Genel** bölümünde bir **Ad**, **Açıklama**, **Kolay ad** ve **Anahtar sözcükler** girin.</span><span class="sxs-lookup"><span data-stu-id="10435-126">In the **General** section provide a **Name**, **Description**, **Friendly name** and **Keywords**.</span></span>
1. <span data-ttu-id="10435-127">**Genel** altında:</span><span class="sxs-lookup"><span data-stu-id="10435-127">Under **General**:</span></span>
    1. <span data-ttu-id="10435-128">**Ad** kutusuna bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="10435-128">In the **Name** box, enter a name.</span></span>
    1. <span data-ttu-id="10435-129">**Açıklama** kutusuna bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="10435-129">In the **Description** box, enter a description.</span></span>
    1. <span data-ttu-id="10435-130">**Kolay ad** kutusuna bir kolay ad girin.</span><span class="sxs-lookup"><span data-stu-id="10435-130">In the **Friendly name** box, enter a friendly name.</span></span>
    1. <span data-ttu-id="10435-131">**Anahtar sözcükler** kutusuna ilgili anahtar sözcükleri girin.</span><span class="sxs-lookup"><span data-stu-id="10435-131">In the **Keywords** box, enter relevant keywords.</span></span>
    1. <span data-ttu-id="10435-132">**Görüntüleme sırası** kutusuna, görüntüleme sırası için bir numara girin (isteğe bağlı).</span><span class="sxs-lookup"><span data-stu-id="10435-132">In the **Display order** box, enter a number for the display order (optional).</span></span>
1. <span data-ttu-id="10435-133">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="10435-133">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="10435-134">Başka düğümler eklemek için yukarıdaki adımları yineleyin.</span><span class="sxs-lookup"><span data-stu-id="10435-134">Repeat the steps above to add additional nodes.</span></span>

<span data-ttu-id="10435-135">Aşağıdaki resimde yeni bir ürün hiyerarşisi düğümünün oluşturulması gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="10435-135">The following image shows the creation of a new product hierarchy node.</span></span>

![Ürün hiyerarşisi oluşturma](media/create-product-hierarchy.png)

## <a name="other-settings"></a><span data-ttu-id="10435-137">Diğer ayarlar</span><span class="sxs-lookup"><span data-stu-id="10435-137">Other settings</span></span>

<span data-ttu-id="10435-138">Gerektiğinde her bir kategori grubuna kategori öznitelik grupları da atanabilir.</span><span class="sxs-lookup"><span data-stu-id="10435-138">Category attribute groups can also be assigned to each group as required.</span></span>  

## <a name="additional-resources"></a><span data-ttu-id="10435-139">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="10435-139">Additional resources</span></span>

[<span data-ttu-id="10435-140">Commerce hiyerarşileri</span><span class="sxs-lookup"><span data-stu-id="10435-140">commerce hierarchies</span></span>](retail-hierarchies.md)

[<span data-ttu-id="10435-141">Ürün kategorilerini ve ürünleri yönetme </span><span class="sxs-lookup"><span data-stu-id="10435-141">Manage product categories and products </span></span>](category-management-product-creation.md)

[<span data-ttu-id="10435-142">Ticari varlıkların sıralama düzenini değiştirme</span><span class="sxs-lookup"><span data-stu-id="10435-142">Change the sort order for merchandizing entities</span></span>](custom-order-categories-nav-retail-prod-hierarchy.md)
