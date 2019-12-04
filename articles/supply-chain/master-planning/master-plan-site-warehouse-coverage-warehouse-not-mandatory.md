---
title: Tesis ve ambar kapsamı için master planlama, ambar zorunlu değil
description: Bu konu, site ve ambarın kapsam olduğu bir maddenin nasıl planlanacağını anlatır. Ambar boyutu zorunlu değildir.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cea228e04632bd61f60771b09481241df5d16bd3
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813719"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a><span data-ttu-id="c1e1f-104">Tesis ve ambar kapsamı için master planlama, ambar zorunlu değil</span><span class="sxs-lookup"><span data-stu-id="c1e1f-104">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1e1f-105">Bu konu, site ve ambarın kapsam olduğu bir maddenin nasıl planlanacağını anlatır.</span><span class="sxs-lookup"><span data-stu-id="c1e1f-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="c1e1f-106">Ambar boyutu zorunlu değildir.</span><span class="sxs-lookup"><span data-stu-id="c1e1f-106">The warehouse dimension is not mandatory.</span></span>

<span data-ttu-id="c1e1f-107">Bu master planlama senaryosu aşağıdaki koşulları kapsar:</span><span class="sxs-lookup"><span data-stu-id="c1e1f-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="c1e1f-108">Tesis boyutları zorunluya göre ayarlanmıştır ve talep hareketinde girilmesi gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="c1e1f-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="c1e1f-109">Bu ayar değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="c1e1f-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="c1e1f-110">Ambar boyutu zorunluya göre ayarlanmamıştır.</span><span class="sxs-lookup"><span data-stu-id="c1e1f-110">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="c1e1f-111">Ambar biliniyor olabilir, ancak master plan planlama hesaplamasında kullanılmamıştır.</span><span class="sxs-lookup"><span data-stu-id="c1e1f-111">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="c1e1f-112">Tesis ve ambar boyutları tedarik planlama için ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="c1e1f-112">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="c1e1f-113">Ayrıca, diğer boyutlar da tedarik planlama için ayarlanmış olabilir.</span><span class="sxs-lookup"><span data-stu-id="c1e1f-113">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="c1e1f-114">Ancak, bunlar birden çok tesis işlevselliğinden etkilenmemiştir.</span><span class="sxs-lookup"><span data-stu-id="c1e1f-114">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="c1e1f-115">Aşağıdaki grafikte, master plan planlamasının ne şekilde ilerlediği gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="c1e1f-115">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="c1e1f-116">Grafikte söz edilen parametreler ve bunların konumları aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="c1e1f-116">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="c1e1f-117">Ambar El ile olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="c1e1f-117">The warehouse is set to Manual.</span></span> <span data-ttu-id="c1e1f-118">Şu öğeleri tıklatın: **Stok yönetimi &gt; Kurulum &gt; Stok dökümü &gt; Ambarlar**.</span><span class="sxs-lookup"><span data-stu-id="c1e1f-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="c1e1f-119">**Master planlama** hızlı sekmesi üzerindeki **El ile** alanına bakınız.</span><span class="sxs-lookup"><span data-stu-id="c1e1f-119">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="c1e1f-120">Madde karşılama, madde için tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="c1e1f-120">Item coverage is defined for the item.</span></span> <span data-ttu-id="c1e1f-121">**Ürün bilgileri yönetimi &gt; Ürünler&gt; Serbest bırakılan ürünler** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c1e1f-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="c1e1f-122">Maddeyi seçin ve sonra Eylem bölmesi üzerindeki **Plan** sekmesinde, **Madde kapsamı** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c1e1f-122">Select the item, and then, on the Action pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="c1e1f-123">Stok yenileme ilişkileri ambar için tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="c1e1f-123">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="c1e1f-124">Şu öğeleri tıklatın: **Stok yönetimi &gt; Kurulum &gt; Stok dökümü &gt; Ambarlar**.</span><span class="sxs-lookup"><span data-stu-id="c1e1f-124">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="c1e1f-125">**Master planlama** hızlı sekmesi üzerindeki **Ana ambar** alan grubuna bakınız.</span><span class="sxs-lookup"><span data-stu-id="c1e1f-125">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="c1e1f-126">Varsayılan sipariş türü Ürün, Satınalma siparişi veya Kanban olarak ayarlıdır.</span><span class="sxs-lookup"><span data-stu-id="c1e1f-126">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="c1e1f-127">**Ürün bilgileri yönetimi &gt; Ürünler&gt; Serbest bırakılan ürünler** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c1e1f-127">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="c1e1f-128">Maddeyi seçin ve sonra Eylem bölmesi üzerindeki **Plan** sekmesinde, **Varsayılan sipariş ayarları** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c1e1f-128">Select the item, and then, on the Action pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="c1e1f-129">**Varsayılan sipariş ayarları** formunda **Varsayılan sipariş türü**'ne bakınız.</span><span class="sxs-lookup"><span data-stu-id="c1e1f-129">In the **Default order settings** form, see the **Default order type**.</span></span>

![Tesis ve ambar talebi, ambar zorunlu değil](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="c1e1f-131">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="c1e1f-131">Additional resources</span></span>
--------

[<span data-ttu-id="c1e1f-132">Master planlama ve birden çok tesis işlevine genel bakış</span><span class="sxs-lookup"><span data-stu-id="c1e1f-132">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="c1e1f-133">Tesis kapsamı için master planlama, ambar zorunlu</span><span class="sxs-lookup"><span data-stu-id="c1e1f-133">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="c1e1f-134">Tesis ve ambar kapsamı için master planlama, ambar zorunlu</span><span class="sxs-lookup"><span data-stu-id="c1e1f-134">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="c1e1f-135">Tesis ve ambar kapsamı için master planlama, ambar zorunlu değil</span><span class="sxs-lookup"><span data-stu-id="c1e1f-135">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="c1e1f-136">Ürün reçetesi sürümünü belirleme</span><span class="sxs-lookup"><span data-stu-id="c1e1f-136">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



