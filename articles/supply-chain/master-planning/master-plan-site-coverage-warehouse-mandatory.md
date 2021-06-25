---
title: Tesis kapsamı için master planlama, ambar zorunlu
description: Bu konuda, kapsam boyutu olarak tesisi olan bir maddenin nasıl planlanacağını açıklanmaktadır. Ambar zorunlu bir boyuttur.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 008061d286505a2e678e15fbff7706da9c410dfe
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187566"
---
# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a><span data-ttu-id="80dae-104">Tesis kapsamı için master planlama, ambar zorunlu</span><span class="sxs-lookup"><span data-stu-id="80dae-104">Master planning for site coverage, mandatory warehouse</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="80dae-105">Bu konuda, kapsam boyutu olarak tesisi olan bir maddenin nasıl planlanacağını açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="80dae-105">This topic describes how an item that has the site as coverage dimension is planned.</span></span> <span data-ttu-id="80dae-106">Ambar zorunlu bir boyuttur.</span><span class="sxs-lookup"><span data-stu-id="80dae-106">Warehouse is a mandatory dimension.</span></span>

<span data-ttu-id="80dae-107">Bu master planlama senaryosu aşağıdaki koşulları kapsar:</span><span class="sxs-lookup"><span data-stu-id="80dae-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="80dae-108">Tesis boyutları zorunluya göre ayarlanmıştır ve talep hareketinde girilmesi gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="80dae-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="80dae-109">Bu ayar değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="80dae-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="80dae-110">Ambar boyutları zorunluya göre ayarlanmıştır ve talep hareketinde girilmesi gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="80dae-110">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="80dae-111">Tesis boyutu tedarik planlama için ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="80dae-111">The site dimension is set for coverage planning.</span></span> <span data-ttu-id="80dae-112">Ayrıca, diğer boyutlar da tedarik planlama için ayarlanmış olabilir.</span><span class="sxs-lookup"><span data-stu-id="80dae-112">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="80dae-113">Ancak, bunlar birden çok tesis işlevselliğinden etkilenmemiştir.</span><span class="sxs-lookup"><span data-stu-id="80dae-113">However, they are not affected by the multisite functionality.</span></span>
-   <span data-ttu-id="80dae-114">Ambar boyutu tedarik planlama için ayarlanmamıştır.</span><span class="sxs-lookup"><span data-stu-id="80dae-114">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="80dae-115">Bu nedenle, arz ve talep tesise (ve belki de, diğer tedarik planlaması yapılmış boyutlara) göre toplanır.</span><span class="sxs-lookup"><span data-stu-id="80dae-115">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="80dae-116">Aşağıdaki grafikte, master plan planlamasının ne şekilde ilerlediği gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="80dae-116">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="80dae-117">Grafikte söz edilen parametreler ve bunların konumları aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="80dae-117">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="80dae-118">Madde karşılama, madde için tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="80dae-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="80dae-119">**Ürün bilgileri yönetimi &gt; Ürünler&gt; Serbest bırakılan ürünler** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="80dae-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="80dae-120">Maddeyi seçin ve rdından **Planla &gt; Madde kapsamı** düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="80dae-120">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="80dae-121">Stok yenileme ilişkileri ambar için tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="80dae-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="80dae-122">Şu öğeleri tıklatın: **Stok yönetimi &gt; Kurulum &gt; Stok dökümü &gt; Ambarlar**.</span><span class="sxs-lookup"><span data-stu-id="80dae-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="80dae-123">**Master planlama** sekmesi üzerindeki **Ana ambar** alan grubuna bakın.</span><span class="sxs-lookup"><span data-stu-id="80dae-123">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="80dae-124">Varsayılan sipariş türü Ürün, Satınalma siparişi veya Kanban olarak ayarlıdır.</span><span class="sxs-lookup"><span data-stu-id="80dae-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="80dae-125">**Ürün bilgileri yönetimi &gt; Ürünler&gt; Serbest bırakılan ürünler** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="80dae-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="80dae-126">Maddeyi seçin ve ardından **Plan &gt; Varsayılan sipariş ayarları** düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="80dae-126">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="80dae-127">**Varsayılan sipariş ayarları** formunda **Varsayılan sipariş türü**'ne bakınız.</span><span class="sxs-lookup"><span data-stu-id="80dae-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Tesis kapsamı talebi ambar zorunlu](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



## <a name="additional-resources"></a><span data-ttu-id="80dae-129">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="80dae-129">Additional resources</span></span>

[<span data-ttu-id="80dae-130">Master planlama ve birden çok tesis işlevine genel bakış</span><span class="sxs-lookup"><span data-stu-id="80dae-130">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="80dae-131">Tesis ve ambar kapsamı için master planlama, ambar zorunlu</span><span class="sxs-lookup"><span data-stu-id="80dae-131">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="80dae-132">Tesis kapsamı için master planlama, ambar zorunlu</span><span class="sxs-lookup"><span data-stu-id="80dae-132">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="80dae-133">Tesis ve ambar kapsamı için master planlama, ambar zorunlu değil</span><span class="sxs-lookup"><span data-stu-id="80dae-133">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="80dae-134">Ürün reçetesi sürümünü belirleme</span><span class="sxs-lookup"><span data-stu-id="80dae-134">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]