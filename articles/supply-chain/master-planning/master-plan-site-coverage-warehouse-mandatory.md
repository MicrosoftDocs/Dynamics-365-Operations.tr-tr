---
title: "Tesis kapsamı için master planlama, ambar zorunlu"
description: "Bu konuda, kapsam boyutu olarak tesisi olan bir maddenin nasıl planlanacağını açıklanmaktadır. Ambar zorunlu bir boyuttur."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 14df626025a22237afe30cc5b08d42b475fc3a4f
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a><span data-ttu-id="24e7c-104">Tesis kapsamı için master planlama, ambar zorunlu</span><span class="sxs-lookup"><span data-stu-id="24e7c-104">Master planning for site coverage, mandatory warehouse</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="24e7c-105">Bu konuda, kapsam boyutu olarak tesisi olan bir maddenin nasıl planlanacağını açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="24e7c-105">This topic describes how an item that has the site as coverage dimension is planned.</span></span> <span data-ttu-id="24e7c-106">Ambar zorunlu bir boyuttur.</span><span class="sxs-lookup"><span data-stu-id="24e7c-106">Warehouse is a mandatory dimension.</span></span>

<span data-ttu-id="24e7c-107">Bu master planlama senaryosu aşağıdaki koşulları kapsar:</span><span class="sxs-lookup"><span data-stu-id="24e7c-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="24e7c-108">Tesis boyutları zorunluya göre ayarlanmıştır ve talep hareketinde girilmesi gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="24e7c-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="24e7c-109">Bu ayar değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="24e7c-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="24e7c-110">Ambar boyutları zorunluya göre ayarlanmıştır ve talep hareketinde girilmesi gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="24e7c-110">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="24e7c-111">Tesis boyutu tedarik planlama için ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="24e7c-111">The site dimension is set for coverage planning.</span></span> <span data-ttu-id="24e7c-112">Ayrıca, diğer boyutlar da tedarik planlama için ayarlanmış olabilir.</span><span class="sxs-lookup"><span data-stu-id="24e7c-112">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="24e7c-113">Ancak, bunlar birden çok tesis işlevselliğinden etkilenmemiştir.</span><span class="sxs-lookup"><span data-stu-id="24e7c-113">However, they are not affected by the multisite functionality.</span></span>
-   <span data-ttu-id="24e7c-114">Ambar boyutu tedarik planlama için ayarlanmamıştır.</span><span class="sxs-lookup"><span data-stu-id="24e7c-114">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="24e7c-115">Bu nedenle, arz ve talep tesise (ve belki de, diğer tedarik planlaması yapılmış boyutlara) göre toplanır.</span><span class="sxs-lookup"><span data-stu-id="24e7c-115">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="24e7c-116">Aşağıdaki grafikte, master plan planlamasının ne şekilde ilerlediği gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="24e7c-116">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="24e7c-117">Grafikte söz edilen parametreler ve bunların konumları aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="24e7c-117">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="24e7c-118">Madde karşılama, madde için tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="24e7c-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="24e7c-119">**Ürün bilgileri yönetimi &gt; Ürünler&gt; Serbest bırakılan ürünler** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="24e7c-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="24e7c-120">Maddeyi seçin ve rdından **Planla &gt; Madde kapsamı** düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="24e7c-120">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="24e7c-121">Stok yenileme ilişkileri ambar için tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="24e7c-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="24e7c-122">Şu öğeleri tıklatın: **Stok yönetimi &gt; Kurulum &gt; Stok dökümü &gt; Ambarlar**.</span><span class="sxs-lookup"><span data-stu-id="24e7c-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="24e7c-123">**Master planlama** sekmesi üzerindeki **Ana ambar** alan grubuna bakın.</span><span class="sxs-lookup"><span data-stu-id="24e7c-123">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="24e7c-124">Varsayılan sipariş türü Ürün, Satınalma siparişi veya Kanban olarak ayarlıdır.</span><span class="sxs-lookup"><span data-stu-id="24e7c-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="24e7c-125">**Ürün bilgileri yönetimi &gt; Ürünler&gt; Serbest bırakılan ürünler** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="24e7c-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="24e7c-126">Maddeyi seçin ve ardından **Plan &gt; Varsayılan sipariş ayarları** düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="24e7c-126">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="24e7c-127">**Varsayılan sipariş ayarları** formunda **Varsayılan sipariş türü**'ne bakınız.</span><span class="sxs-lookup"><span data-stu-id="24e7c-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Tesis kapsamı talebi ambar zorunlu](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="see-also"></a><span data-ttu-id="24e7c-129">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="24e7c-129">See also</span></span>
--------

[<span data-ttu-id="24e7c-130">Master planlama ve birden çok tesis işlevi</span><span class="sxs-lookup"><span data-stu-id="24e7c-130">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="24e7c-131">Master planlama - tesis ve ambar kapsamı, ambar zorunlu</span><span class="sxs-lookup"><span data-stu-id="24e7c-131">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="24e7c-132">Master planlama - tesis kapsamı. ambar zorunlu</span><span class="sxs-lookup"><span data-stu-id="24e7c-132">Master planning - site coverage. warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="24e7c-133">Master planlama - tesis ve ambar kapsamı, ambar zorunlu değil</span><span class="sxs-lookup"><span data-stu-id="24e7c-133">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="24e7c-134">Master planlama - Ürün reçetesi sürümünün nasıl belirlendiği</span><span class="sxs-lookup"><span data-stu-id="24e7c-134">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)




