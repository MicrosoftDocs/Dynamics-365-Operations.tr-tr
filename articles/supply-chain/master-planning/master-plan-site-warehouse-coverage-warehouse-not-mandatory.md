---
title: "Tesis ve ambar kapsamı için master planlama, ambar zorunlu değil"
description: "Bu konu, site ve ambarın kapsam olduğu bir maddenin nasıl planlanacağını anlatır. Ambar boyutu zorunlu değildir."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 45796049cddef137eb2ca1e4331197e4b4a65071
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---

# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a><span data-ttu-id="01b61-104">Tesis ve ambar kapsamı için master planlama, ambar zorunlu değil</span><span class="sxs-lookup"><span data-stu-id="01b61-104">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="01b61-105">Bu konu, site ve ambarın kapsam olduğu bir maddenin nasıl planlanacağını anlatır.</span><span class="sxs-lookup"><span data-stu-id="01b61-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="01b61-106">Ambar boyutu zorunlu değildir.</span><span class="sxs-lookup"><span data-stu-id="01b61-106">The warehouse dimension is not mandatory.</span></span>

<span data-ttu-id="01b61-107">Bu master planlama senaryosu aşağıdaki koşulları kapsar:</span><span class="sxs-lookup"><span data-stu-id="01b61-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="01b61-108">Tesis boyutları zorunluya göre ayarlanmıştır ve talep hareketinde girilmesi gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="01b61-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="01b61-109">Bu ayar değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="01b61-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="01b61-110">Ambar boyutu zorunluya göre ayarlanmamıştır.</span><span class="sxs-lookup"><span data-stu-id="01b61-110">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="01b61-111">Ambar biliniyor olabilir, ancak master plan planlama hesaplamasında kullanılmamıştır.</span><span class="sxs-lookup"><span data-stu-id="01b61-111">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="01b61-112">Tesis ve ambar boyutları tedarik planlama için ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="01b61-112">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="01b61-113">Ayrıca, diğer boyutlar da tedarik planlama için ayarlanmış olabilir.</span><span class="sxs-lookup"><span data-stu-id="01b61-113">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="01b61-114">Ancak, bunlar birden çok tesis işlevselliğinden etkilenmemiştir.</span><span class="sxs-lookup"><span data-stu-id="01b61-114">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="01b61-115">Aşağıdaki grafikte, master plan planlamasının ne şekilde ilerlediği gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="01b61-115">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="01b61-116">Grafikte söz edilen parametreler ve bunların konumları aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="01b61-116">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="01b61-117">Ambar El ile olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="01b61-117">The warehouse is set to Manual.</span></span> <span data-ttu-id="01b61-118">Şu öğeleri tıklatın: **Stok yönetimi &gt; Kurulum &gt; Stok dökümü &gt; Ambarlar**.</span><span class="sxs-lookup"><span data-stu-id="01b61-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="01b61-119">**Master planlama** hızlı sekmesi üzerindeki **El ile** alanına bakınız.</span><span class="sxs-lookup"><span data-stu-id="01b61-119">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="01b61-120">Madde karşılama, madde için tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="01b61-120">Item coverage is defined for the item.</span></span> <span data-ttu-id="01b61-121">**Ürün bilgileri yönetimi &gt; Ürünler&gt; Serbest bırakılan ürünler** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="01b61-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="01b61-122">Maddeyi seçin ve sonra Eylem bölmesi üzerindeki **Plan** sekmesinde, **Madde kapsamı** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="01b61-122">Select the item, and then, on the Action pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="01b61-123">Stok yenileme ilişkileri ambar için tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="01b61-123">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="01b61-124">Şu öğeleri tıklatın: **Stok yönetimi &gt; Kurulum &gt; Stok dökümü &gt; Ambarlar**.</span><span class="sxs-lookup"><span data-stu-id="01b61-124">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="01b61-125">**Master planlama** hızlı sekmesi üzerindeki **Ana ambar** alan grubuna bakınız.</span><span class="sxs-lookup"><span data-stu-id="01b61-125">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="01b61-126">Varsayılan sipariş türü Ürün, Satınalma siparişi veya Kanban olarak ayarlıdır.</span><span class="sxs-lookup"><span data-stu-id="01b61-126">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="01b61-127">**Ürün bilgileri yönetimi &gt; Ürünler&gt; Serbest bırakılan ürünler** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="01b61-127">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="01b61-128">Maddeyi seçin ve sonra Eylem bölmesi üzerindeki **Plan** sekmesinde, **Varsayılan sipariş ayarları** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="01b61-128">Select the item, and then, on the Action pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="01b61-129">**Varsayılan sipariş ayarları** formunda **Varsayılan sipariş türü**'ne bakınız.</span><span class="sxs-lookup"><span data-stu-id="01b61-129">In the **Default order settings** form, see the **Default order type**.</span></span>

![Tesis ve ambar talebi, ambar zorunlu değil](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)


-



<a name="additional-resources"></a><span data-ttu-id="01b61-131">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="01b61-131">Additional resources</span></span>
--------

[<span data-ttu-id="01b61-132">Master planlama ve birden çok tesis işlevi</span><span class="sxs-lookup"><span data-stu-id="01b61-132">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="01b61-133">Master planlama - tesis ve ambar kapsamı, ambar zorunlu</span><span class="sxs-lookup"><span data-stu-id="01b61-133">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="01b61-134">Master planlama - tesis kapsamı, ambar zorunlu</span><span class="sxs-lookup"><span data-stu-id="01b61-134">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="01b61-135">Master planlama - tesis kapsamı, ambar zorunlu değil</span><span class="sxs-lookup"><span data-stu-id="01b61-135">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="01b61-136">Master planlama - Ürün reçetesi sürümünün nasıl belirlendiği</span><span class="sxs-lookup"><span data-stu-id="01b61-136">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)




