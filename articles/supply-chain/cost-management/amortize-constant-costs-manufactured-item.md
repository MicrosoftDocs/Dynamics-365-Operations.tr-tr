---
title: "Üretilen maddeler için sabit maliyetlerin itfası"
description: "Üretilen bir ürünün sabit maliyetleri, operasyon hazırlık sürelerini ve sabit miktara veya sabit hurda tutarına sahip bileşeni yansıtır."
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcDialog, BOMCalcTable, BOMCalcTrans
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 274503
ms.assetid: 535ab25d-a031-4e8c-84ec-478f2987a1ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2e9d15e35661d37036af48d4d1183e4f25012e57
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---

# <a name="amortize-constant-costs-for-a-manufactured-item"></a><span data-ttu-id="782e7-103">Üretilen maddeler için sabit maliyetlerin itfası</span><span class="sxs-lookup"><span data-stu-id="782e7-103">Amortize constant costs for a manufactured item</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="782e7-104">Üretilen bir ürünün sabit maliyetleri, operasyon hazırlık sürelerini ve sabit miktara veya sabit hurda tutarına sahip bileşeni yansıtır.</span><span class="sxs-lookup"><span data-stu-id="782e7-104">A manufactured item’s constant costs reflect the operation setup times and the components that have a constant quantity or a constant scrap amount.</span></span> 

<span data-ttu-id="782e7-105">Lot büyüklüğünü maliyetlendirme kavramı, bu sabit maliyetleri üretilen maddenin hesaplanan maliyetinde itfa etmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="782e7-105">The concept of a costing lot size is used to amortize these constant costs in the calculated cost of a manufactured item.</span></span> <span data-ttu-id="782e7-106">Bu kavram muhasebe lot boyutunun da aralarında bulunduğu birkaç eş anlamlı sözcüğe sahiptir.</span><span class="sxs-lookup"><span data-stu-id="782e7-106">This concept has several synonyms, one of which is accounting lot size.</span></span> <span data-ttu-id="782e7-107">Benzer şekilde, sabit maliyetlerin itfası kavramının da, orantılı sabit maliyetlerin de aralarında bulunduğu çeşitli eş anlamlı sözcükleri vardır.</span><span class="sxs-lookup"><span data-stu-id="782e7-107">The concept of amortizing constant costs also has several synonyms, one of which is proportional constant costs.</span></span>

<span data-ttu-id="782e7-108">Üretin bir madde için bir maliyetlendirme lotunun miktarı, bir ürün reçetesi (BOM) hesaplamasında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="782e7-108">The quantity of a costing lot size for a manufactured item is used in a bill of material (BOM) calculation.</span></span> <span data-ttu-id="782e7-109">Miktar, aşağıdaki şekilde gösterildiği gibi, ürün reçetesini nasıl başlattığınıza ve gerçekleştirdiğinize bağlıdır:</span><span class="sxs-lookup"><span data-stu-id="782e7-109">The quantity depends on how you initiate and perform the BOM calculation, as illustrated by the following:</span></span>

-   <span data-ttu-id="782e7-110">Maddenin ürün reçetesi hesaplamasındaki varsayılan hesaplama miktarı − Maddenin standart stok için sipariş miktarı, lot büyüklüğü maliyetlendirmesi için varsayılan olarak davranır, ancak varsayılan değer maddenin çoklu sipariş miktarını yansıtan miktardan büyük olabilir.</span><span class="sxs-lookup"><span data-stu-id="782e7-110">Default calculation quantity in an item’s BOM calculation − The item’s standard order quantity for inventory acts as the costing lot size, but the default value might be a greater quantity to reflect the item’s order quantity multiple.</span></span> <span data-ttu-id="782e7-111">Maddenin standart ve çoklu sipariş miktarı varsayılan sipariş ayarlarında veya tesise özgü sipariş ayarlarında tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="782e7-111">The item’s standard order quantity and multiple can be defined within its default order settings or site-specific order settings.</span></span>
-   <span data-ttu-id="782e7-112">Maddenin ürün reçetesi hesaplamasında belirtilen hesaplama miktarı − Belirtilen hesaplama miktarı maddenin lot büyüklüğü maliyetlendirmesi gibi davranır.</span><span class="sxs-lookup"><span data-stu-id="782e7-112">Specified calculation quantity in an item’s BOM calculation − The specified calculation quantity acts as the costing lot size for the item.</span></span> <span data-ttu-id="782e7-113">Hesaplama miktarı başlangıçta maddenin standart sipariş miktarını kullanır, ancak varsayılan değer istenildiğinde el ile değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="782e7-113">The calculation quantity initially uses the item’s standard order quantity, but the default value can be manually overridden.</span></span> <span data-ttu-id="782e7-114">Belirtilen hesaplama miktarı, belirli bir madde için maliyetlendirme lot boyutunu temsil eder ve ürün reçetesi hattı üretim türüne sahip üretilen bileşenler için.</span><span class="sxs-lookup"><span data-stu-id="782e7-114">The specified calculation quantity represents the costing lot size for the specified item, and for manufactured components that have a BOM line type of production.</span></span> <span data-ttu-id="782e7-115">Bunun sebebi, bileşenin tam miktarda üretilecek olduğunun varsayılmasıdır.</span><span class="sxs-lookup"><span data-stu-id="782e7-115">This is because it is assumed that the component will be produced to the exact quantity.</span></span> <span data-ttu-id="782e7-116">Üretilen diğer bileşenlere yönelik lot büyüklüğü maliyetlendirmesi maddenin BOM satır tipine sahip, her birinin standart sipariş miktarını yansıtır.</span><span class="sxs-lookup"><span data-stu-id="782e7-116">The costing lot size for other manufactured components that have a BOM line type of item will reflect their standard order quantity.</span></span>
-   <span data-ttu-id="782e7-117">Maddenin ürün reçetesi hesaplamasında belirtilen siparişe göre üretim hesaplaması miktarı − Belirtilen hesaplama miktarı, ürün reçetesi hesaplamalarında siparişe göre üretim açılımı modu kullanıldığında madde ve maddenin üretilen bileşenleri için lot büyüklüğü hesaplaması gibi davranır.</span><span class="sxs-lookup"><span data-stu-id="782e7-117">Specified make-to-order calculation quantity in an item’s BOM calculation − The specified calculation quantity acts as the costing lot size for the item and its manufactured components when BOM calculations use a make-to-order explosion mode.</span></span> <span data-ttu-id="782e7-118">Üretilen bileşenlerin, üretime yönelik ürün reçetesi satır tipiyle üretilen bileşende olduğu gibi, tam miktarda üretileceği varsayılır.</span><span class="sxs-lookup"><span data-stu-id="782e7-118">It is assumed that the manufactured components will be produced to the exact quantity, just like a manufactured component that has a BOM line type of production.</span></span>
-   <span data-ttu-id="782e7-119">Siparişe özel ürün reçetesi hesaplamasında belirtilen hesaplama miktarı − Siparişe özel ürün reçetesi hesaplaması, satış siparişi, satış teklifi veya servis siparişindeki bir satır maddesi için gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="782e7-119">Specified calculation quantity in an order-specific BOM calculation − An order-specific BOM calculation can be performed for a line item on a sales order, sales quotation, or service order.</span></span> <span data-ttu-id="782e7-120">Belirtilen hesaplama miktarı, kaynak satır maddesindeki miktarı kullanır, ancak varsayılan miktar geçersiz kılınabilir.</span><span class="sxs-lookup"><span data-stu-id="782e7-120">The specified calculation quantity uses the quantity on the originating line item, but the default quantity can be overridden.</span></span> <span data-ttu-id="782e7-121">Siparişe özel ürün reçetesi hesaplamasının siparişe göre üretim mi, yoksa çok düzeyli açılım modu mu kullanacağı seçilebilir.</span><span class="sxs-lookup"><span data-stu-id="782e7-121">You can select whether the order-specific BOM calculation uses a make-to-order or multilevel explosion mode.</span></span>

<span data-ttu-id="782e7-122">Üretilen maddenin hesaplanan miktarının itfa edilen sabit maliyetleri, belirlenmiş giderlere tabidir.</span><span class="sxs-lookup"><span data-stu-id="782e7-122">The calculated amount of a manufactured item’s amortized constant costs is termed charges.</span></span>






