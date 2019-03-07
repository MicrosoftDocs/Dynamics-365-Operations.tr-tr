---
title: Tesis ve ambar kapsamı için master planlama, ambar zorunlu
description: Bu konu, site ve ambarın kapsam olduğu bir maddenin nasıl planlanacağını anlatır. Ambar boyutu zorunludur.
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
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c52fc9955afe2a7502d0e1f9e7cdfc5b89bbb31d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "365351"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a><span data-ttu-id="03565-104">Tesis ve ambar kapsamı için master planlama, ambar zorunlu</span><span class="sxs-lookup"><span data-stu-id="03565-104">Master planning for site and warehouse coverage, warehouse mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03565-105">Bu konu, site ve ambarın kapsam olduğu bir maddenin nasıl planlanacağını anlatır.</span><span class="sxs-lookup"><span data-stu-id="03565-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="03565-106">Ambar boyutu zorunludur.</span><span class="sxs-lookup"><span data-stu-id="03565-106">The warehouse dimension is mandatory.</span></span>

<span data-ttu-id="03565-107">Bu master planlama senaryosu aşağıdaki koşulları kapsar:</span><span class="sxs-lookup"><span data-stu-id="03565-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="03565-108">Tesis boyutları zorunluya göre ayarlanmıştır ve talep hareketinde girilmesi gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="03565-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="03565-109">Ambar boyutları zorunluya göre ayarlanmıştır ve talep hareketinde girilmesi gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="03565-109">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="03565-110">Tesis ve ambar boyutları tedarik planlama için ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="03565-110">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="03565-111">Ayrıca, diğer boyutlar da tedarik planlama için ayarlanmış olabilir.</span><span class="sxs-lookup"><span data-stu-id="03565-111">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="03565-112">Ancak, bunlar birden çok tesis işlevselliğinden etkilenmemiştir.</span><span class="sxs-lookup"><span data-stu-id="03565-112">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="03565-113">Aşağıdaki grafikte, master plan planlamasının ne şekilde ilerlediği gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="03565-113">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="03565-114">Grafikte söz edilen parametreler ve bunların konumları aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="03565-114">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="03565-115">Ambar **El ile** olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="03565-115">The warehouse is set to **Manual**.</span></span> <span data-ttu-id="03565-116">Şu öğeleri tıklatın: **Stok yönetimi &gt; Kurulum &gt; Stok dökümü &gt; Ambarlar**.</span><span class="sxs-lookup"><span data-stu-id="03565-116">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="03565-117">**Master planlama** hızlı sekmesi üzerindeki **El ile** alanına bakınız.</span><span class="sxs-lookup"><span data-stu-id="03565-117">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="03565-118">Madde karşılama, madde için tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="03565-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="03565-119">**Ürün bilgileri yönetimi &gt; Ürünler&gt; Serbest bırakılan ürünler** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03565-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="03565-120">Maddeyi seçin ve sonra Eylem bölmesi üzerindeki **Plan** sekmesinde, **Madde kapsamı** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="03565-120">Select the item, and then, on the Action pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="03565-121">Stok yenileme ilişkileri ambar için tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="03565-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="03565-122">Şu öğeleri tıklatın: **Stok yönetimi &gt; Kurulum &gt; Stok dökümü &gt; Ambarlar**.</span><span class="sxs-lookup"><span data-stu-id="03565-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="03565-123">**Master planlama** hızlı sekmesi üzerindeki **Ana ambar** alan grubuna bakınız.</span><span class="sxs-lookup"><span data-stu-id="03565-123">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="03565-124">Varsayılan sipariş türü Ürün, Satınalma siparişi veya Kanban olarak ayarlıdır.</span><span class="sxs-lookup"><span data-stu-id="03565-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="03565-125">**Ürün bilgileri yönetimi &gt; Ürünler&gt; Serbest bırakılan ürünler** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03565-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="03565-126">Maddeyi seçin ve sonra Eylem bölmesi üzerindeki **Plan** sekmesinde, **Varsayılan sipariş ayarları** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="03565-126">Select the item, and then, on the Action pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="03565-127">**Varsayılan sipariş ayarları** formunda **Varsayılan sipariş türü**'ne bakınız.</span><span class="sxs-lookup"><span data-stu-id="03565-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Tesis ve ambar kapsamı talep et, ambar zorunlu](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="03565-129">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="03565-129">Additional resources</span></span>
--------

[<span data-ttu-id="03565-130">Master planlama ve birden çok tesis işlevi</span><span class="sxs-lookup"><span data-stu-id="03565-130">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="03565-131">Master planlama - tesis kapsamı, ambar zorunlu</span><span class="sxs-lookup"><span data-stu-id="03565-131">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="03565-132">Master planlama - tesis kapsamı, ambar zorunlu değil</span><span class="sxs-lookup"><span data-stu-id="03565-132">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="03565-133">Master planlama - tesis ve ambar kapsamı, ambar zorunlu değil</span><span class="sxs-lookup"><span data-stu-id="03565-133">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="03565-134">Master planlama - Ürün reçetesi sürümünün nasıl belirlendiği</span><span class="sxs-lookup"><span data-stu-id="03565-134">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)



