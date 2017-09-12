---
title: "Stok boyutu başına cari ortalama maliyeti izleme"
description: "Her stok maddesine bir stok boyutu grubu eklenir. Dolayısıyla, cari ortalama maliyet fiyatı, mali olarak izlenmekte olan stok boyutlarından seçilenlere dayanarak hesaplanır."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: a88ec380810a9a2d7048d5a8773ebb5960e4cf86
ms.contentlocale: tr-tr
ms.lasthandoff: 07/18/2017

---

# <a name="tracking-running-average-cost-per-inventory-dimension"></a><span data-ttu-id="48cbe-104">Stok boyutu başına cari ortalama maliyeti izleme</span><span class="sxs-lookup"><span data-stu-id="48cbe-104">Tracking running average cost per inventory dimension</span></span>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


<span data-ttu-id="48cbe-105">Her stok maddesine bir stok boyutu grubu eklenir.</span><span class="sxs-lookup"><span data-stu-id="48cbe-105">An inventory dimension group is attached to every inventory item.</span></span> <span data-ttu-id="48cbe-106">Dolayısıyla, cari ortalama maliyet fiyatı, mali olarak izlenmekte olan stok boyutlarından seçilenlere dayanarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="48cbe-106">Therefore, the running average cost price of an item is calculated based on the selected inventory dimensions that are being tracked financially.</span></span>

<span data-ttu-id="48cbe-107">Stok boyutları üç türlüdür: ürün, depolama ve izleme.</span><span class="sxs-lookup"><span data-stu-id="48cbe-107">There are three types of inventory dimensions: product, storage, and tracking.</span></span> <span data-ttu-id="48cbe-108">Ürün boyutları; yapılandırma, ebat ve rengi içerir.</span><span class="sxs-lookup"><span data-stu-id="48cbe-108">Product dimensions include configuration, size, and color.</span></span> <span data-ttu-id="48cbe-109">Ürün boyutları her zaman mali olarak izlenir.</span><span class="sxs-lookup"><span data-stu-id="48cbe-109">Product dimensions are always tracked financially.</span></span> <span data-ttu-id="48cbe-110">Depolama ve izleme boyutları tesis, ambar, konum, stok durumu, plaka, toplu iş numarası ve seri numarasını içerir.</span><span class="sxs-lookup"><span data-stu-id="48cbe-110">Storage and tracking dimensions include site, warehouse, location, inventory status, license plate, batch number, and serial number.</span></span> <span data-ttu-id="48cbe-111">Hangi depolama ve izleme boyutlarının mali olarak izleneceğine karar verebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="48cbe-111">You can decide which storage and tracking dimensions are tracked financially.</span></span> 

<span data-ttu-id="48cbe-112">**Örnek 1**</span><span class="sxs-lookup"><span data-stu-id="48cbe-112">**Example 1**</span></span> 

<span data-ttu-id="48cbe-113">Maddeye iliştirilen depolama boyutu grubu ambar tarafından mali olarak izleniyorsa, cari ortalama maliyet fiyatı her ambar için hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="48cbe-113">If the storage dimension group that is attached to the item is financially tracked by warehouse, the running average cost price is calculated per warehouse.</span></span> <span data-ttu-id="48cbe-114">Aşağıdaki satınalma siparişleri faturalandırılmıştır:</span><span class="sxs-lookup"><span data-stu-id="48cbe-114">The following purchase orders have been invoiced:</span></span>

-   <span data-ttu-id="48cbe-115">GW ambarı için 10,00 ABD Doları maliyet fiyatında 2 miktarı için bir satınalma siparişi faturalandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="48cbe-115">A purchase order for a quantity of 2 at a cost price of USD 10.00 has been invoiced for warehouse GW.</span></span>
-   <span data-ttu-id="48cbe-116">GW ambarı için 12,00 ABD Doları maliyet fiyatında 3 miktarı için bir satınalma siparişi faturalandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="48cbe-116">A purchase order for a quantity of 3 at a cost price of USD 12.00 has been invoiced for warehouse GW.</span></span>
-   <span data-ttu-id="48cbe-117">MW ambarı için 15,00 ABD Doları maliyet fiyatında 5 miktarı için bir satınalma siparişi faturalandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="48cbe-117">A purchase order for a quantity of 5 at a cost price of USD 15.00 has been invoiced for warehouse MW.</span></span>

<span data-ttu-id="48cbe-118">Ambar GW için yürütülen ortalama maliyet fiyatı 11,20 ABD dolarıdır ve ambar MW için yürütülen ortalama maliyet fiyatı 15,00 ABD dolarıdır.</span><span class="sxs-lookup"><span data-stu-id="48cbe-118">The running average cost price for warehouse GW is USD 11.20, and the running average cost price for warehouse MW is USD 15.00.</span></span> <span data-ttu-id="48cbe-119">Ambar GW için bir satış emri faturası deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="48cbe-119">A sales order invoice is posted for warehouse GW.</span></span> <span data-ttu-id="48cbe-120">Stokun değeri ve satılan malların maliyeti (stok kapanışı çalıştırılmadan önce ve işaretlenmemiş olarak) 11,20 ABD dolarıdır.</span><span class="sxs-lookup"><span data-stu-id="48cbe-120">The value of the inventory and the cost of goods sold (before inventory close is run and without marking) is USD 11.20.</span></span> <span data-ttu-id="48cbe-121">Ambar MW için başka bir satış emri deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="48cbe-121">Another sales order is posted for warehouse MW.</span></span> <span data-ttu-id="48cbe-122">Stokun değeri ve satılan malların maliyeti (stok kapanışı çalıştırılmadan önce ve işaretlenmemiş olarak) 15,00 ABD dolarıdır.</span><span class="sxs-lookup"><span data-stu-id="48cbe-122">The value of the inventory and the cost of goods sold (before inventory close is run and without marking) is USD 15.00.</span></span> 

<span data-ttu-id="48cbe-123">**Örnek 2** Maddeye iliştirilmiş depolama boyut grubu mali olarak ambar tarafından izleniyorsa ve izleme boyutu grubu toplu iş numarası tarafından mali olarak izleniyorsa, her toplu iş için yürütülen ortalama maliyet fiyatı hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="48cbe-123">**Example 2** If the storage dimension group that is attached to the item is financially tracked by warehouse, and the tracking dimension group is financially tracked by batch number, the running average cost price is calculated for each batch.</span></span> 

<span data-ttu-id="48cbe-124">**Not:** Maliyet fiyatını her zaman izlenen tüm mali boyutlarla görüntülemenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="48cbe-124">**Note:** We recommend that you always view the cost price for all financial dimensions that are being tracked.</span></span> <span data-ttu-id="48cbe-125">Aşağıdaki satınalma siparişleri faturalandırılmıştır:</span><span class="sxs-lookup"><span data-stu-id="48cbe-125">The following purchase orders have been invoiced:</span></span>

-   <span data-ttu-id="48cbe-126">10,00 ABD Doları maliyet fiyatında 2 miktarı için bir satınalma siparişi; GW ambarı ve AAA toplu işi için faturalandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="48cbe-126">A purchase order for a quantity of 2 at a cost price of USD 10.00 has been invoiced for warehouse GW and batch AAA.</span></span>
-   <span data-ttu-id="48cbe-127">12,00 ABD Doları maliyet fiyatında 3 miktarı için bir satınalma siparişi; GW ambarı ve AAA toplu işi için faturalandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="48cbe-127">A purchase order for a quantity of 3 at a cost price of USD 12.00 has been invoiced for warehouse GW and batch AAA.</span></span>
-   <span data-ttu-id="48cbe-128">15,00 ABD Doları maliyet fiyatında 2 miktarı için bir satınalma siparişi; GW ambarı ve BBB toplu işi için faturalandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="48cbe-128">A purchase order for a quantity of 2 at a cost price of USD 15.00 has been invoiced for warehouse GW and batch BBB.</span></span>

<span data-ttu-id="48cbe-129">Ambar GW ve toplu iş AAA için yürütülen ortalama maliyet fiyatı 11,20 ABD dolarıdır ve ambar MW ve toplu iş BBB için yürütülen ortalama maliyet fiyatı 15,00 ABD dolarıdır.</span><span class="sxs-lookup"><span data-stu-id="48cbe-129">The running average cost price for warehouse GW and batch AAA is USD 11.20, and the running average cost price for warehouse GW and batch BBB is USD 15.00.</span></span>




