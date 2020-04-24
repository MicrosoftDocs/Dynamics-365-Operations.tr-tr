---
title: Tesis ve ambar kapsamı için master planlama, ambar zorunlu
description: Bu konu, site ve ambarın kapsam olduğu bir maddenin nasıl planlanacağını anlatır. Ambar boyutu zorunludur.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df35389176368c44c2ff4a3210fabc25bf24c807
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213688"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a><span data-ttu-id="0ce8c-104">Tesis ve ambar kapsamı için master planlama, ambar zorunlu</span><span class="sxs-lookup"><span data-stu-id="0ce8c-104">Master planning for site and warehouse coverage, warehouse mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ce8c-105">Bu konu, site ve ambarın kapsam olduğu bir maddenin nasıl planlanacağını anlatır.</span><span class="sxs-lookup"><span data-stu-id="0ce8c-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="0ce8c-106">Ambar boyutu zorunludur.</span><span class="sxs-lookup"><span data-stu-id="0ce8c-106">The warehouse dimension is mandatory.</span></span>

<span data-ttu-id="0ce8c-107">Bu master planlama senaryosu aşağıdaki koşulları kapsar:</span><span class="sxs-lookup"><span data-stu-id="0ce8c-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="0ce8c-108">Tesis boyutları zorunluya göre ayarlanmıştır ve talep hareketinde girilmesi gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="0ce8c-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="0ce8c-109">Ambar boyutları zorunluya göre ayarlanmıştır ve talep hareketinde girilmesi gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="0ce8c-109">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="0ce8c-110">Tesis ve ambar boyutları tedarik planlama için ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="0ce8c-110">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="0ce8c-111">Ayrıca, diğer boyutlar da tedarik planlama için ayarlanmış olabilir.</span><span class="sxs-lookup"><span data-stu-id="0ce8c-111">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="0ce8c-112">Ancak, bunlar birden çok tesis işlevselliğinden etkilenmemiştir.</span><span class="sxs-lookup"><span data-stu-id="0ce8c-112">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="0ce8c-113">Aşağıdaki grafikte, master plan planlamasının ne şekilde ilerlediği gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="0ce8c-113">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="0ce8c-114">Grafikte söz edilen parametreler ve bunların konumları aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="0ce8c-114">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="0ce8c-115">Ambar **El ile** olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="0ce8c-115">The warehouse is set to **Manual**.</span></span> <span data-ttu-id="0ce8c-116">Şu öğeleri tıklatın: **Stok yönetimi &gt; Kurulum &gt; Stok dökümü &gt; Ambarlar**.</span><span class="sxs-lookup"><span data-stu-id="0ce8c-116">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="0ce8c-117">**Master planlama** hızlı sekmesi üzerindeki **El ile** alanına bakınız.</span><span class="sxs-lookup"><span data-stu-id="0ce8c-117">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="0ce8c-118">Madde karşılama, madde için tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="0ce8c-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="0ce8c-119">**Ürün bilgileri yönetimi &gt; Ürünler&gt; Serbest bırakılan ürünler** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0ce8c-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="0ce8c-120">Maddeyi seçin ve sonra Eylem bölmesi üzerindeki **Plan** sekmesinde, **Madde kapsamı** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="0ce8c-120">Select the item, and then, on the Action pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="0ce8c-121">Stok yenileme ilişkileri ambar için tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="0ce8c-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="0ce8c-122">Şu öğeleri tıklatın: **Stok yönetimi &gt; Kurulum &gt; Stok dökümü &gt; Ambarlar**.</span><span class="sxs-lookup"><span data-stu-id="0ce8c-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="0ce8c-123">**Master planlama** hızlı sekmesi üzerindeki **Ana ambar** alan grubuna bakınız.</span><span class="sxs-lookup"><span data-stu-id="0ce8c-123">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="0ce8c-124">Varsayılan sipariş türü Ürün, Satınalma siparişi veya Kanban olarak ayarlıdır.</span><span class="sxs-lookup"><span data-stu-id="0ce8c-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="0ce8c-125">**Ürün bilgileri yönetimi &gt; Ürünler&gt; Serbest bırakılan ürünler** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0ce8c-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="0ce8c-126">Maddeyi seçin ve sonra Eylem bölmesi üzerindeki **Plan** sekmesinde, **Varsayılan sipariş ayarları** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="0ce8c-126">Select the item, and then, on the Action pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="0ce8c-127">**Varsayılan sipariş ayarları** formunda **Varsayılan sipariş türü**'ne bakınız.</span><span class="sxs-lookup"><span data-stu-id="0ce8c-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Tesis ve ambar kapsamı talep et, ambar zorunlu](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="0ce8c-129">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="0ce8c-129">Additional resources</span></span>
--------

[<span data-ttu-id="0ce8c-130">Master planlama ve birden çok tesis işlevine genel bakış</span><span class="sxs-lookup"><span data-stu-id="0ce8c-130">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="0ce8c-131">Tesis kapsamı için master planlama, ambar zorunlu</span><span class="sxs-lookup"><span data-stu-id="0ce8c-131">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="0ce8c-132">Tesis kapsamı için master planlama, ambar zorunlu değil</span><span class="sxs-lookup"><span data-stu-id="0ce8c-132">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="0ce8c-133">Tesis ve ambar kapsamı için master planlama, ambar zorunlu değil</span><span class="sxs-lookup"><span data-stu-id="0ce8c-133">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="0ce8c-134">Ürün reçetesi sürümünü belirleme</span><span class="sxs-lookup"><span data-stu-id="0ce8c-134">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



