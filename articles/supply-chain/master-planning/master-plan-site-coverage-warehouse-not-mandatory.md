---
title: Tesis kapsamı için master planlama, ambar zorunlu değil
description: Bu konu, site boyutunun kapsam olduğu bir maddenin nasıl planlanacağını anlatır.
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
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f4cde5c570148ca58c4ea583a8f538a72d4957d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439532"
---
# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a><span data-ttu-id="bb1a8-103">Tesis kapsamı için master planlama, ambar zorunlu değil</span><span class="sxs-lookup"><span data-stu-id="bb1a8-103">Master planning for site coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bb1a8-104">Bu konu, site boyutunun kapsam olduğu bir maddenin nasıl planlanacağını anlatır.</span><span class="sxs-lookup"><span data-stu-id="bb1a8-104">This topic describes how an item that has the site dimension set for coverage is planned.</span></span>

<span data-ttu-id="bb1a8-105">Bu master planlama senaryosu aşağıdaki koşulları kapsar:</span><span class="sxs-lookup"><span data-stu-id="bb1a8-105">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="bb1a8-106">Tesis boyutları zorunluya göre ayarlanmıştır ve talep hareketinde girilmesi gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="bb1a8-106">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="bb1a8-107">Ambar boyutu zorunluya göre ayarlanmamıştır.</span><span class="sxs-lookup"><span data-stu-id="bb1a8-107">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="bb1a8-108">Ambar biliniyor olabilir, ancak master plan planlama hesaplamasında kullanılmamıştır.</span><span class="sxs-lookup"><span data-stu-id="bb1a8-108">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="bb1a8-109">Tesis boyutu tedarik planlama için ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="bb1a8-109">The site dimension is set for coverage planning.</span></span>
-   <span data-ttu-id="bb1a8-110">Ambar boyutu tedarik planlama için ayarlanmamıştır.</span><span class="sxs-lookup"><span data-stu-id="bb1a8-110">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="bb1a8-111">Bu nedenle, arz ve talep tesise (ve belki de, diğer tedarik planlaması yapılmış boyutlara) göre toplanır.</span><span class="sxs-lookup"><span data-stu-id="bb1a8-111">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="bb1a8-112">Aşağıdaki grafikte, master plan planlamasının ne şekilde ilerlediği gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="bb1a8-112">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="bb1a8-113">Grafikte söz edilen parametreler ve bunların konumları aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="bb1a8-113">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="bb1a8-114">Madde karşılama, madde için tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="bb1a8-114">Item coverage is defined for the item.</span></span> <span data-ttu-id="bb1a8-115">**Ürün bilgileri yönetimi &gt; Ürünler&gt; Serbest bırakılan ürünler** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bb1a8-115">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="bb1a8-116">Maddeyi seçin ve rdından **Planla &gt; Madde kapsamı** düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bb1a8-116">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="bb1a8-117">Stok yenileme ilişkileri ambar için tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="bb1a8-117">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="bb1a8-118">Şu öğeleri tıklatın: **Stok yönetimi &gt; Kurulum &gt; Stok dökümü &gt; Ambarlar**.</span><span class="sxs-lookup"><span data-stu-id="bb1a8-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="bb1a8-119">**Master planlama** sekmesi üzerindeki **Ana ambar** alan grubuna bakın.</span><span class="sxs-lookup"><span data-stu-id="bb1a8-119">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="bb1a8-120">Varsayılan sipariş türü Ürün, Satın alma siparişi veya Kanban olarak ayarlıdır.</span><span class="sxs-lookup"><span data-stu-id="bb1a8-120">The default order type is set to Production, Purchase order or Kanban.</span></span> <span data-ttu-id="bb1a8-121">**Ürün bilgileri yönetimi &gt; Ürünler&gt; Serbest bırakılan ürünler** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bb1a8-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="bb1a8-122">Maddeyi seçin ve ardından **Plan &gt; Varsayılan sipariş ayarları** düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bb1a8-122">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="bb1a8-123">**Varsayılan sipariş ayarları** formunda **Varsayılan sipariş türü** alanına bakınız.</span><span class="sxs-lookup"><span data-stu-id="bb1a8-123">In the **Default order settings** form, see the **Default order type** field.</span></span>

![Tesis kapsamı talebi ambar zorunlu değil    ](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="bb1a8-125">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="bb1a8-125">Additional resources</span></span>
--------

[<span data-ttu-id="bb1a8-126">Master planlama ve birden çok tesis işlevine genel bakış</span><span class="sxs-lookup"><span data-stu-id="bb1a8-126">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="bb1a8-127">Tesis ve ambar kapsamı için master planlama, ambar zorunlu</span><span class="sxs-lookup"><span data-stu-id="bb1a8-127">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="bb1a8-128">Tesis kapsamı için master planlama, ambar zorunlu</span><span class="sxs-lookup"><span data-stu-id="bb1a8-128">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="bb1a8-129">Tesis kapsamı için master planlama, ambar zorunlu değil</span><span class="sxs-lookup"><span data-stu-id="bb1a8-129">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="bb1a8-130">Ürün reçetesi sürümünü belirleme</span><span class="sxs-lookup"><span data-stu-id="bb1a8-130">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



