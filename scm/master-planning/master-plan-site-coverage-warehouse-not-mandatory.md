---
title: "Tesis kapsamı için master planlama, ambar zorunlu değil"
description: "Bu konu, site boyutunun kapsam olduğu bir maddenin nasıl planlanacağını anlatır."
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
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 79582e92daeaf0afb032448d36be12edd0926089
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---

# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a><span data-ttu-id="ea567-103">Tesis kapsamı için master planlama, ambar zorunlu değil</span><span class="sxs-lookup"><span data-stu-id="ea567-103">Master planning for site coverage, warehouse not mandatory</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ea567-104">Bu konu, site boyutunun kapsam olduğu bir maddenin nasıl planlanacağını anlatır.</span><span class="sxs-lookup"><span data-stu-id="ea567-104">This topic describes how an item that has the site dimension set for coverage is planned.</span></span>

<span data-ttu-id="ea567-105">Bu master planlama senaryosu aşağıdaki koşulları kapsar:</span><span class="sxs-lookup"><span data-stu-id="ea567-105">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="ea567-106">Tesis boyutları zorunluya göre ayarlanmıştır ve talep hareketinde girilmesi gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="ea567-106">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="ea567-107">Ambar boyutu zorunluya göre ayarlanmamıştır.</span><span class="sxs-lookup"><span data-stu-id="ea567-107">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="ea567-108">Ambar biliniyor olabilir, ancak master plan planlama hesaplamasında kullanılmamıştır.</span><span class="sxs-lookup"><span data-stu-id="ea567-108">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="ea567-109">Tesis boyutu tedarik planlama için ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="ea567-109">The site dimension is set for coverage planning.</span></span>
-   <span data-ttu-id="ea567-110">Ambar boyutu tedarik planlama için ayarlanmamıştır.</span><span class="sxs-lookup"><span data-stu-id="ea567-110">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="ea567-111">Bu nedenle, arz ve talep tesise (ve belki de, diğer tedarik planlaması yapılmış boyutlara) göre toplanır.</span><span class="sxs-lookup"><span data-stu-id="ea567-111">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="ea567-112">Aşağıdaki grafikte, master plan planlamasının ne şekilde ilerlediği gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="ea567-112">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="ea567-113">Grafikte söz edilen parametreler ve bunların konumları aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="ea567-113">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="ea567-114">Madde karşılama, madde için tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="ea567-114">Item coverage is defined for the item.</span></span> <span data-ttu-id="ea567-115">**Ürün bilgileri yönetimi &gt; Ürünler&gt; Serbest bırakılan ürünler** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ea567-115">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="ea567-116">Maddeyi seçin ve rdından **Planla &gt; Madde kapsamı** düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ea567-116">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="ea567-117">Stok yenileme ilişkileri ambar için tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="ea567-117">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="ea567-118">Şu öğeleri tıklatın: **Stok yönetimi &gt; Kurulum &gt; Stok dökümü &gt; Ambarlar**.</span><span class="sxs-lookup"><span data-stu-id="ea567-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="ea567-119">**Master planlama** sekmesi üzerindeki **Ana ambar** alan grubuna bakın.</span><span class="sxs-lookup"><span data-stu-id="ea567-119">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="ea567-120">Varsayılan sipariş türü Ürün, Satın alma siparişi veya Kanban olarak ayarlıdır.</span><span class="sxs-lookup"><span data-stu-id="ea567-120">The default order type is set to Production, Purchase order or Kanban.</span></span> <span data-ttu-id="ea567-121">**Ürün bilgileri yönetimi &gt; Ürünler&gt; Serbest bırakılan ürünler** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ea567-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="ea567-122">Maddeyi seçin ve ardından **Plan &gt; Varsayılan sipariş ayarları** düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ea567-122">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="ea567-123">**Varsayılan sipariş ayarları** formunda **Varsayılan sipariş türü** alanına bakınız.</span><span class="sxs-lookup"><span data-stu-id="ea567-123">In the **Default order settings** form, see the **Default order type** field.</span></span>

![Tesis kapsamı talebi ambar zorunlu değil    ](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="see-also"></a><span data-ttu-id="ea567-125">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="ea567-125">See also</span></span>
--------

[<span data-ttu-id="ea567-126">Master planlama ve birden çok tesis işlevi</span><span class="sxs-lookup"><span data-stu-id="ea567-126">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="ea567-127">Master planlama - tesis kapsamı, ambar zorunlu</span><span class="sxs-lookup"><span data-stu-id="ea567-127">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="ea567-128">Master planlama - tesis ve ambar kapsamı, ambar zorunlu değil</span><span class="sxs-lookup"><span data-stu-id="ea567-128">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="ea567-129">Master planlama - tesis ve ambar kapsamı, ambar zorunlu</span><span class="sxs-lookup"><span data-stu-id="ea567-129">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="ea567-130">Master planlama - ürün reçetesi sürümünün nasıl belirlendiği</span><span class="sxs-lookup"><span data-stu-id="ea567-130">Master planning - how the BOM version is determined</span></span>](master-plan-bom-version-determined.md)




