---
title: Alım satım varlıkların sıralama düzenini değiştirme
description: Bu konu, alım satım ilgili çeşitli kuruluşlar için Dynamics 365 Commerce'deki görüntüleme sırasını denetlemeyle ilgili kavramları açıklamaktadır.
author: josaw1
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 54929f924bd9c2b59dec453cf580e0b2bc149d38
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799481"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a><span data-ttu-id="0f14f-103">Alım satım varlıkların sıralama düzenini değiştirme</span><span class="sxs-lookup"><span data-stu-id="0f14f-103">Change the sort order for merchandising entities</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="0f14f-104">Perakendeciler, tüm kanallarda müşteri etkileşimi için ürün keşfini bir ana araç olarak kabul edin.</span><span class="sxs-lookup"><span data-stu-id="0f14f-104">Retailers consider product discovery a primary tool for customer interaction across all channels.</span></span> <span data-ttu-id="0f14f-105">Çeşitli işlevler müşterilerin ürünleri kolayca bulmasına yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="0f14f-105">Various functionality can help customers easily discover products.</span></span> <span data-ttu-id="0f14f-106">Örneğin kategorilerine, aramaya ve filtreye göz atabilirler.</span><span class="sxs-lookup"><span data-stu-id="0f14f-106">For example, they can browse categories, search, and filter.</span></span>

<span data-ttu-id="0f14f-107">Bu konu, alım satım ilgili çeşitli kuruluşlar için görüntüleme sırasını denetlemeyle ilgili kavramları açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="0f14f-107">This topic explains the concepts that are related to controlling the display order for various merchandising-related entities.</span></span> <span data-ttu-id="0f14f-108">Sıralama düzenini nasıl değiştireceğinizi de açıklar.</span><span class="sxs-lookup"><span data-stu-id="0f14f-108">It also explains how to change the sort order.</span></span>

## <a name="overview"></a><span data-ttu-id="0f14f-109">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="0f14f-109">Overview</span></span>

<span data-ttu-id="0f14f-110">Çeşitli alım satım ilişkili varlıkları sıralama desteği geliştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="0f14f-110">The support for sorting various merchandising-related entities has been enhanced.</span></span> <span data-ttu-id="0f14f-111">Bu destek şimdi, daha önce uygulama ortaklarından eklenti gerektiren mevcut müşteri senaryoları ile daha uyumludur.</span><span class="sxs-lookup"><span data-stu-id="0f14f-111">This support is now better aligned with existing customer scenarios that previously required extensions from implementation partners.</span></span>

<span data-ttu-id="0f14f-112">Sürüm 10.0.5'ten önceki Retail sürümlerinde, gezinti hiyerarşisindeki kategorilerin sıralama düzeni alfabetik idi.</span><span class="sxs-lookup"><span data-stu-id="0f14f-112">In versions of Retail that are earlier than version 10.0.5, the sort order for categories in the navigation hierarchy was alphabetical.</span></span> <span data-ttu-id="0f14f-113">Yeni özel sıralama düzeni işlevi alım ve satım yöneticilerinin tüm Son Kullanıcı istemcileri üzerinde Merchandising ile ilgili çeşitli varlıklar için sıralama düzenini konfigüre etmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="0f14f-113">The new custom sort order functionality lets merchandising managers configure the sort order for various merchandising-related entities across all end-user clients.</span></span> <span data-ttu-id="0f14f-114">Bu istemciler Yönetim Merkezleri (HQ) ve çağrı merkezleri içerirler.</span><span class="sxs-lookup"><span data-stu-id="0f14f-114">These clients include headquarters (HQ) and call centers.</span></span>

## <a name="configure-the-display-order-for-categories-in-the-product-hierarchy"></a><span data-ttu-id="0f14f-115">Ürün hiyerarşisindeki kategorilerin görüntülenme sırasını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="0f14f-115">Configure the display order for categories in the product hierarchy</span></span>

<span data-ttu-id="0f14f-116">Bu yordamı tamamlayabilmek için, demo verilerinin çalışma ortamınıza yüklenmiş olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="0f14f-116">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="0f14f-117">**Retail ve Commerce \> Ürünler ve kategoriler \> Commerce ürün hiyerarşisi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="0f14f-117">Go to **Retail and Commerce \> Products and categories \> Commerce product hierarchy**.</span></span>
2. <span data-ttu-id="0f14f-118">**Kategori hiyerarşisi düzenle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0f14f-118">Click **Edit category hierarchy**.</span></span>
3. <span data-ttu-id="0f14f-119">**Düzenle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="0f14f-119">Click **Edit**.</span></span>
4. <span data-ttu-id="0f14f-120">Ağaçta **TÜMÜ \> Eylem Sporları**'nı genişletin.</span><span class="sxs-lookup"><span data-stu-id="0f14f-120">In the tree, expand **ALL \> Action Sports**.</span></span>
5. <span data-ttu-id="0f14f-121">Ağaçta **TÜMÜ \> Takım Sporları**'nı genişletin.</span><span class="sxs-lookup"><span data-stu-id="0f14f-121">In the tree, expand **ALL \> Team Sports**.</span></span>
6. <span data-ttu-id="0f14f-122">**Görüntüleme sırası** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="0f14f-122">In the **Display order** field, enter a number.</span></span> <span data-ttu-id="0f14f-123">(Bu sayı eksi olabilir.)</span><span class="sxs-lookup"><span data-stu-id="0f14f-123">(The number can be negative.)</span></span>
7. <span data-ttu-id="0f14f-124">Sırasını değiştirmek istediğiniz ek kategoriler için 4 ile 6 arasındaki adımları yineleyin.</span><span class="sxs-lookup"><span data-stu-id="0f14f-124">Repeat steps 4 through 6 for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="0f14f-125">Kanal gezinti hiyerarşisinin görüntüleme sırası, Commerce ürün hiyerarşisi için HQ ve kategoriye göre serbest bırakılan Ürünler için yansıtılır.</span><span class="sxs-lookup"><span data-stu-id="0f14f-125">The display order for the channel navigation hierarchy will be reflected in HQ for the commerce product hierarchy and released products by category.</span></span>

![Özel negatif değerlerle sıralanan ürün hiyerarşisi](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Ürün hiyerarşisine göre özel sıralanmış, kategoriye göre yayınlanan ürünler](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a><span data-ttu-id="0f14f-128">Kanal gezinme hiyerarşisindeki kategorilerin görüntülenme sırasını konfigüre etme</span><span class="sxs-lookup"><span data-stu-id="0f14f-128">Configure the display order for categories in the channel navigation hierarchy</span></span>

<span data-ttu-id="0f14f-129">Bu yordamı tamamlayabilmek için, demo verilerinin çalışma ortamınıza yüklenmiş olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="0f14f-129">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="0f14f-130">**Retail and Commerce \> Ürünler ve kategoriler \> Kanal gezinme kategorileri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="0f14f-130">Go to **Retail and Commerce \> Products and categories \> Channel navigation categories**.</span></span>
2. <span data-ttu-id="0f14f-131">Listesinde, **Moda göre gezinti** hiyerarşisini seçin.</span><span class="sxs-lookup"><span data-stu-id="0f14f-131">In the list, select the **Fashion navigation** hierarchy.</span></span>
3. <span data-ttu-id="0f14f-132">**Kategori hiyerarşisi düzenle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0f14f-132">Click **Edit category hierarchy**.</span></span>
4. <span data-ttu-id="0f14f-133">**Düzenle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="0f14f-133">Click **Edit**.</span></span>
5. <span data-ttu-id="0f14f-134">Ağaçta **Moda \> Womenswear \> Kadın Ayakkabısı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="0f14f-134">In the tree, select **Fashion \> Womenswear \> Womens Shoes**.</span></span>
6. <span data-ttu-id="0f14f-135">**Görüntüleme sırası** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="0f14f-135">In the **Display order** field, enter a number.</span></span>
7. <span data-ttu-id="0f14f-136">Ağaçta **Moda \> Womenswear \> Üstler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0f14f-136">In the tree, select **Fashion \> Womenswear \> Tops**.</span></span>

    <span data-ttu-id="0f14f-137">Benzer şekilde, alt kategorilerin sıralama düzenini de tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0f14f-137">Likewise, you can define the sort order for the sub-categories.</span></span>

8. <span data-ttu-id="0f14f-138">Ağaçta **Moda \> Menswear \> Günlük Gömlekler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0f14f-138">In the tree, select **Fashion \> Menswear \> Casual Shirts**.</span></span>
9. <span data-ttu-id="0f14f-139">**Görüntüleme sırası** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="0f14f-139">In the **Display order** field, enter a number.</span></span>
10. <span data-ttu-id="0f14f-140">Ağaçta **Moda \> Menswear \> Montlar ve Ceketler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0f14f-140">In the tree, select **Fashion \> Menswear \> Coats & Jackets**.</span></span>
11. <span data-ttu-id="0f14f-141">**Görüntüleme sırası** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="0f14f-141">In the **Display order** field, enter a number.</span></span>
12. <span data-ttu-id="0f14f-142">Sırasını değiştirmek istediğiniz ek kategoriler için adımları yineleyin.</span><span class="sxs-lookup"><span data-stu-id="0f14f-142">Repeat for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="0f14f-143">Kanal gezinme hiyerarşisinin görüntüleme sırası HQ, Katalog ve kanallarda yansıtılır.</span><span class="sxs-lookup"><span data-stu-id="0f14f-143">The display order for the channel navigation hierarchy is reflected in HQ, catalog, and channels.</span></span>

![Kanal gezinme hiyerarşisi özel sıralandı](./media/ChannelNavCustomSorted.png)

![Katalog Gezinti hiyerarşisi kanal gezinti hiyerarşisine göre özel sıralandı](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![Özel sıralı kategorileri olan POS](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> <span data-ttu-id="0f14f-147">Varsayılan olarak, özel sıralama düzeni özelliği kapalıdır.</span><span class="sxs-lookup"><span data-stu-id="0f14f-147">By default the custom sort order feature is turned off.</span></span> <span data-ttu-id="0f14f-148">Bu özelliği ve diğer özellikleri nasıl açacağınızı öğrenmek için [Özellik Yönetimi](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview)'ne bakın.</span><span class="sxs-lookup"><span data-stu-id="0f14f-148">To learn how to turn on this feature and other features, see [Feature management](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]