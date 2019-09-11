---
title: Alım satım varlıkların sıralama düzenini değiştirme
description: Bu konu, alım satım ilgili çeşitli kuruluşlar için Microsoft Dynamics 365 for Retail'deki görüntüleme sırasını denetlemeyle ilgili kavramları açıklamaktadır.
author: ashishharchwani
manager: AnnBe
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 2be3c1198ac6fff851be1bead2f0995202f1f0e7
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2019
ms.locfileid: "1866173"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a><span data-ttu-id="9e605-103">Alım satım varlıkların sıralama düzenini değiştirme</span><span class="sxs-lookup"><span data-stu-id="9e605-103">Change the sort order for merchandising entities</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="9e605-104">Perakendeciler, tüm perakende kanallarında müşteri etkileşimi için ürün keşfini bir ana araç olarak kabul edin.</span><span class="sxs-lookup"><span data-stu-id="9e605-104">Retailers consider product discovery a primary tool for customer interaction across all retail channels.</span></span> <span data-ttu-id="9e605-105">Çeşitli işlevler müşterilerin ürünleri kolayca bulmasına yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="9e605-105">Various functionality can help customers easily discover products.</span></span> <span data-ttu-id="9e605-106">Örneğin kategorilerine, aramaya ve filtreye göz atabilirler.</span><span class="sxs-lookup"><span data-stu-id="9e605-106">For example, they can browse categories, search, and filter.</span></span>

<span data-ttu-id="9e605-107">Bu konu, alım satım ilgili çeşitli kuruluşlar için görüntüleme sırasını denetlemeyle ilgili kavramları açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="9e605-107">This topic explains the concepts that are related to controlling the display order for various merchandising-related entities.</span></span> <span data-ttu-id="9e605-108">Sıralama düzenini nasıl değiştireceğinizi de açıklar.</span><span class="sxs-lookup"><span data-stu-id="9e605-108">It also explains how to change the sort order.</span></span>

## <a name="overview"></a><span data-ttu-id="9e605-109">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="9e605-109">Overview</span></span>

<span data-ttu-id="9e605-110">Çeşitli alım satım ilişkili varlıkları sıralama desteği geliştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="9e605-110">The support for sorting various merchandising-related entities has been enhanced.</span></span> <span data-ttu-id="9e605-111">Bu destek şimdi, daha önce uygulama ortaklarından eklenti gerektiren mevcut müşteri senaryoları ile daha uyumludur.</span><span class="sxs-lookup"><span data-stu-id="9e605-111">This support is now better aligned with existing customer scenarios that previously required extensions from implementation partners.</span></span>

<span data-ttu-id="9e605-112">Sürüm 10.0.5'ten önceki Microsoft Dynamics 365 for Retail sürümlerinde, gezinti hiyerarşisindeki kategorilerin sıralama düzeni alfabetik idi.</span><span class="sxs-lookup"><span data-stu-id="9e605-112">In versions of Microsoft Dynamics 365 for Retail that are earlier than version 10.0.5, the sort order for categories in the navigation hierarchy was alphabetical.</span></span> <span data-ttu-id="9e605-113">Yeni özel sıralama düzeni işlevi alım ve satım yöneticilerinin tüm Son Kullanıcı istemcileri üzerinde Merchandising ile ilgili çeşitli varlıklar için sıralama düzenini konfigüre etmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="9e605-113">The new custom sort order functionality lets merchandising managers configure the sort order for various merchandising-related entities across all end-user clients.</span></span> <span data-ttu-id="9e605-114">Bu istemciler Yönetim Merkezleri (HQ) ve çağrı merkezleri içerirler.</span><span class="sxs-lookup"><span data-stu-id="9e605-114">These clients include headquarters (HQ) and call centers.</span></span>

## <a name="configure-the-display-order-for-categories-in-the-retail-product-hierarchy"></a><span data-ttu-id="9e605-115">Perakende ürün hiyerarşisindeki kategorilerin görüntülenme sırasını konfigüre etme</span><span class="sxs-lookup"><span data-stu-id="9e605-115">Configure the display order for categories in the retail product hierarchy</span></span>

<span data-ttu-id="9e605-116">Bu yordamı tamamlayabilmek için, demo verilerinin çalışma ortamınıza yüklenmiş olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="9e605-116">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="9e605-117">**Perakende \> Ürünler ve kategoriler \> Perakende ürün hiyerarşisi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="9e605-117">Go to **Retail \> Products and categories \> Retail product hierarchy**.</span></span>
2. <span data-ttu-id="9e605-118">**Kategori hiyerarşisi düzenle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9e605-118">Click **Edit category hierarchy**.</span></span>
3. <span data-ttu-id="9e605-119">**Düzenle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9e605-119">Click **Edit**.</span></span>
4. <span data-ttu-id="9e605-120">Ağaçta **TÜMÜ \> Eylem Sporları**'nı genişletin.</span><span class="sxs-lookup"><span data-stu-id="9e605-120">In the tree, expand **ALL \> Action Sports**.</span></span>
5. <span data-ttu-id="9e605-121">Ağaçta **TÜMÜ \> Takım Sporları**'nı genişletin.</span><span class="sxs-lookup"><span data-stu-id="9e605-121">In the tree, expand **ALL \> Team Sports**.</span></span>
6. <span data-ttu-id="9e605-122">**Görüntüleme sırası** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="9e605-122">In the **Display order** field, enter a number.</span></span> <span data-ttu-id="9e605-123">(Bu sayı eksi olabilir.)</span><span class="sxs-lookup"><span data-stu-id="9e605-123">(The number can be negative.)</span></span>
7. <span data-ttu-id="9e605-124">Sırasını değiştirmek istediğiniz ek kategoriler için 4 ile 6 arasındaki adımları yineleyin.</span><span class="sxs-lookup"><span data-stu-id="9e605-124">Repeat steps 4 through 6 for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="9e605-125">Kanal gezinti hiyerarşisinin görüntüleme sırası, perakende ürün hiyerarşisi için HQ ve kategoriye göre serbest bırakılan Ürünler için yansıtılır.</span><span class="sxs-lookup"><span data-stu-id="9e605-125">The display order for the channel navigation hierarchy will be reflected in HQ for the retail product hierarchy and released products by category.</span></span>

![Perakende ürün hiyerarşisi özel negatif değerlerle sıralandı](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Kategoriye göre Yayınlanan Ürünler perakende ürün hiyerarşisine göre özel sıralanmış](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a><span data-ttu-id="9e605-128">Kanal gezinme hiyerarşisindeki kategorilerin görüntülenme sırasını konfigüre etme</span><span class="sxs-lookup"><span data-stu-id="9e605-128">Configure the display order for categories in the channel navigation hierarchy</span></span>

<span data-ttu-id="9e605-129">Bu yordamı tamamlayabilmek için, demo verilerinin çalışma ortamınıza yüklenmiş olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="9e605-129">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="9e605-130">**Perakende \> Ürünler ve kategoriler \> Kanal gezinti kategorileri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="9e605-130">Go to **Retail \> Products and categories \> Channel navigation categories**.</span></span>
2. <span data-ttu-id="9e605-131">Listesinde, **Moda göre gezinti** hiyerarşisini seçin.</span><span class="sxs-lookup"><span data-stu-id="9e605-131">In the list, select the **Fashion navigation** hierarchy.</span></span>
3. <span data-ttu-id="9e605-132">**Kategori hiyerarşisi düzenle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9e605-132">Click **Edit category hierarchy**.</span></span>
4. <span data-ttu-id="9e605-133">**Düzenle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9e605-133">Click **Edit**.</span></span>
5. <span data-ttu-id="9e605-134">Ağaçta **Moda \> Womenswear \> Kadın Ayakkabısı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="9e605-134">In the tree, select **Fashion \> Womenswear \> Womens Shoes**.</span></span>
6. <span data-ttu-id="9e605-135">**Görüntüleme sırası** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="9e605-135">In the **Display order** field, enter a number.</span></span>
7. <span data-ttu-id="9e605-136">Ağaçta **Moda \> Womenswear \> Üstler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9e605-136">In the tree, select **Fashion \> Womenswear \> Tops**.</span></span>

    <span data-ttu-id="9e605-137">Benzer şekilde, alt kategorilerin sıralama düzenini de tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9e605-137">Likewise, you can define the sort order for the sub-categories.</span></span>

8. <span data-ttu-id="9e605-138">Ağaçta **Moda \> Menswear \> Günlük Gömlekler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9e605-138">In the tree, select **Fashion \> Menswear \> Casual Shirts**.</span></span>
9. <span data-ttu-id="9e605-139">**Görüntüleme sırası** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="9e605-139">In the **Display order** field, enter a number.</span></span>
10. <span data-ttu-id="9e605-140">Ağaçta **Moda \> Menswear \> Montlar ve Ceketler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9e605-140">In the tree, select **Fashion \> Menswear \> Coats & Jackets**.</span></span>
11. <span data-ttu-id="9e605-141">**Görüntüleme sırası** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="9e605-141">In the **Display order** field, enter a number.</span></span>
12. <span data-ttu-id="9e605-142">Sırasını değiştirmek istediğiniz ek kategoriler için adımları yineleyin.</span><span class="sxs-lookup"><span data-stu-id="9e605-142">Repeat for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="9e605-143">Kanal gezinme hiyerarşisinin görüntüleme sırası HQ, Katalog ve perakende kanallarında yansıtılır.</span><span class="sxs-lookup"><span data-stu-id="9e605-143">The display order for the channel navigation hierarchy is reflected in HQ, catalog, and retail channels.</span></span>

![Kanal gezinme hiyerarşisi özel sıralandı](./media/ChannelNavCustomSorted.png)

![Katalog Gezinti hiyerarşisi kanal gezinti hiyerarşisine göre özel sıralandı](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![Özel sıralı kategorileri olan POS](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> <span data-ttu-id="9e605-147">Varsayılan olarak, özel sıralama düzeni özelliği kapalıdır.</span><span class="sxs-lookup"><span data-stu-id="9e605-147">By default the custom sort order feature is turned off.</span></span> <span data-ttu-id="9e605-148">Bu özelliği ve diğer özellikleri nasıl açacağınızı öğrenmek için [Özellik Yönetimi](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview)'ne bakın.</span><span class="sxs-lookup"><span data-stu-id="9e605-148">To learn how to turn on this feature and other features, see [Feature management](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span></span>
