---
title: Stok konumları
description: Stok konumları ile temel depolama (WSM I) birlikte kullanılarak maddelerin nerede depolandıkları ve maddelerin bir WMS I ambarında nereden çekildikleri belirlenir.
author: perlynne
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSLocation, WMSBlockingCause, WHSLocation
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2134
ms.assetid: 69bf6922-4151-447f-b678-4ba95637f54c
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c8d5459e37b5827b6a2ff07c892c2ff25b76ecd6
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187494"
---
# <a name="inventory-locations"></a><span data-ttu-id="c9b3f-103">Stok konumları</span><span class="sxs-lookup"><span data-stu-id="c9b3f-103">Inventory locations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9b3f-104">Stok konumları ile temel depolama (WSM I) birlikte kullanılarak maddelerin nerede depolandıkları ve maddelerin bir WMS I ambarında nereden çekildikleri belirlenir.</span><span class="sxs-lookup"><span data-stu-id="c9b3f-104">Inventory locations are used with basic warehousing (WMS I) to determine where items are stored and where items are picked from in a WMS I warehouse.</span></span>

<span data-ttu-id="c9b3f-105">Bu konu, Stok yönetimi modülündeki özellikler için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="c9b3f-105">This topic applies to features in the Inventory management module.</span></span> <span data-ttu-id="c9b3f-106">Ambar yönetimi modülündeki özellikler için geçerli değildir.</span><span class="sxs-lookup"><span data-stu-id="c9b3f-106">It does not apply to features in the Warehouse management module.</span></span>

<span data-ttu-id="c9b3f-107">Konum terimi, maddelerin depolandığı ve çekildiği yeri ifade eder.</span><span class="sxs-lookup"><span data-stu-id="c9b3f-107">The term location refers to the place that items are stored and drawn from.</span></span>

<span data-ttu-id="c9b3f-108">Her yerleşim için, maddenin yerleştirildiği yer de belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="c9b3f-108">For each location, the place where the item is inserted can also be specified.</span></span> <span data-ttu-id="c9b3f-109">Varsayılan olarak bunlar aynıdır.</span><span class="sxs-lookup"><span data-stu-id="c9b3f-109">By default, they are the same.</span></span> <span data-ttu-id="c9b3f-110">Maddeler genellikle bir yerleşimin aynı yönünden çekilir veya yerleştirilirler ancak her zaman durum böyle olmaz.</span><span class="sxs-lookup"><span data-stu-id="c9b3f-110">Items are usually inserted and drawn from the same side of a location, but not always.</span></span> <span data-ttu-id="c9b3f-111">Örneğin aktif depoların raflarında saklanan maddeler bir koridordan yerleştirilir ve diğer koridordan çekilir.</span><span class="sxs-lookup"><span data-stu-id="c9b3f-111">For example, items that are stored in live storage racks are inserted from one aisle and drawn from another.</span></span> <span data-ttu-id="c9b3f-112">Ana giriş genellikle koordinatları ile belirlenen bir konum adı tarafından verilir: ambar, koridor, dolap, raf ve depo gözü.</span><span class="sxs-lookup"><span data-stu-id="c9b3f-112">The main input is given by a location name, which is usually determined by its coordinates: warehouse, aisle, rack, shelf, and bin.</span></span> <span data-ttu-id="c9b3f-113">Bu isim veya kimlik el ile girilebilir veya konum koordinatlarından üretilebilir—örneğin, Stok konumları sayfasındaki koridor 1, dolap 2, raf 3, bölme 4 için 01-02-03-4.</span><span class="sxs-lookup"><span data-stu-id="c9b3f-113">This name or ID can be entered manually or generated from the location coordinates—for example, 01-02-03-4 for aisle 1, rack 2, shelf 3, bin 4 in the Inventory locations page.</span></span>
<span data-ttu-id="c9b3f-114">Yerleşim özellikleri</span><span class="sxs-lookup"><span data-stu-id="c9b3f-114">Location properties</span></span>

<span data-ttu-id="c9b3f-115">Bir yerleşim aşağıdaki özelliklere sahiptir:</span><span class="sxs-lookup"><span data-stu-id="c9b3f-115">A location has the following characteristics:</span></span>
-   <span data-ttu-id="c9b3f-116">Boyut (yükseklik, genişlik, derinlik ve dolayısıyla hacim)</span><span class="sxs-lookup"><span data-stu-id="c9b3f-116">Size (height, width, depth, and thereby volume)</span></span>
-   <span data-ttu-id="c9b3f-117">Ambar, koridor, dolap, raf ve bölme pozisyonu</span><span class="sxs-lookup"><span data-stu-id="c9b3f-117">Warehouse, aisle, rack, shelf, and bin position</span></span>
-   <span data-ttu-id="c9b3f-118">Konum türü (toplu yerleşim, malzeme çekme konumu, giriş noktası, çıkış noktası, üretim giriş konumu, inceleme konumu veya kanban süpermarketi)</span><span class="sxs-lookup"><span data-stu-id="c9b3f-118">Location type (bulk location, picking location, inbound dock, outbound dock, production input location, inspection location, or kanban supermarket)</span></span>

<span data-ttu-id="c9b3f-119">Çevrimiçi sistemlerde operatörün belirli bir madde için doğru yerleşimi seçtiğini doğrulamak için bir denetim metni kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c9b3f-119">Check text can be used in online systems to verify that the operator has selected the correct location for a specific item.</span></span> <span data-ttu-id="c9b3f-120">Bu denetim metni el ile veya varsayılan olarak oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="c9b3f-120">This check text can be created manually or by default.</span></span>

## <a name="sort-codes"></a><span data-ttu-id="c9b3f-121">Sıralama kodları</span><span class="sxs-lookup"><span data-stu-id="c9b3f-121">Sort codes</span></span>
<span data-ttu-id="c9b3f-122">Malzeme çekme hatlarını en iyi şekilde idare edebilmek için, malzeme çekme sırası da dahil olmak üzere maddelerin stoktan çekilmesi için gerekli bilgilerin detaylarını içeren sıralama kodlarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="c9b3f-122">Use sort codes to optimize the handling of picking lines, which describe the information that is required for picking items from inventory, including the picking order.</span></span> <span data-ttu-id="c9b3f-123">Sıralama kodları koridor veya diğer koordinatlara göre tanımlanabilir veya yerleşim noktasına el ile atanabilir.</span><span class="sxs-lookup"><span data-stu-id="c9b3f-123">Sort codes can be specified by the aisle and other coordinates, or assigned manually for the location.</span></span>

## <a name="blocked-locations"></a><span data-ttu-id="c9b3f-124">Kullanım dışı bırakılan yerleşimler</span><span class="sxs-lookup"><span data-stu-id="c9b3f-124">Blocked locations</span></span>
<span data-ttu-id="c9b3f-125">Bazen bir yerleşimi, örneğin onarımlar için bir süre için kullanım dışı bırakmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="c9b3f-125">Occasionally, you might want to indicate that a location is blocked for a period of time, for example, to allow for repairs.</span></span> <span data-ttu-id="c9b3f-126">Bazen de, yalnızca giriş veya çıkışı engellemek isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c9b3f-126">At other times, you may want to indicate blocking of only the input or only output.</span></span>

## <a name="tree-structure"></a><span data-ttu-id="c9b3f-127">Ağaç yapısı</span><span class="sxs-lookup"><span data-stu-id="c9b3f-127">Tree structure</span></span>

<span data-ttu-id="c9b3f-128">Stok konumları sayfasında, ambar düzenini ağaç yapısında stok konumlarının yapısına göre tanımlı bir görüntüleme formatında görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c9b3f-128">In the Inventory locations page, you can view the warehouse layout in a tree structure based on the coordinates of inventory locations, in a defined display format.</span></span>

## <a name="maintain-inventory-locations-via-the-warehouse-form"></a><span data-ttu-id="c9b3f-129">Ambar formu üzerinden stok konumlarını muhafaza etme</span><span class="sxs-lookup"><span data-stu-id="c9b3f-129">Maintain inventory locations via the warehouse form</span></span>

<span data-ttu-id="c9b3f-130">Konumları bir ambardan diğerine kopyalamak ve sihirbaz üzerinden konum oluşturmak mümkündür.</span><span class="sxs-lookup"><span data-stu-id="c9b3f-130">It is possible to copy locations from one warehouse to another and to create locations via a wizard.</span></span> <span data-ttu-id="c9b3f-131">Sihirbazı çalıştırmadan önce, Ambar sayfasında varsayılan konum adlarını tanımladığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="c9b3f-131">Before you run the wizard you should make sure that you have defined the default location names on the Warehouse page.</span></span>



## <a name="additional-resources"></a><span data-ttu-id="c9b3f-132">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="c9b3f-132">Additional resources</span></span>

[<span data-ttu-id="c9b3f-133">Yeni ambar düzeni oluşturma</span><span class="sxs-lookup"><span data-stu-id="c9b3f-133">Create a new warehouse layout</span></span>](tasks/create-new-warehouse-layout.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]