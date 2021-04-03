---
title: Fiziksel ve mali güncellemeler
description: Bu konu hangi türdeki hareketlerin miktarları arttırdığı veya azalttığına ilişkin genel bir bakış sağlar.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee65fa43b43bc8b6cbf9763ac4fa8774f30afb98
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263578"
---
# <a name="physical-and-financial-updates"></a><span data-ttu-id="0dae5-103">Fiziksel ve mali güncellemeler</span><span class="sxs-lookup"><span data-stu-id="0dae5-103">Physical and financial updates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0dae5-104">Bu konu hangi türdeki hareketlerin miktarları arttırdığı veya azalttığına ilişkin genel bir bakış sağlar.</span><span class="sxs-lookup"><span data-stu-id="0dae5-104">This topic provides an overview of which types of transactions increase or decrease inventory quantities.</span></span> 

<span data-ttu-id="0dae5-105">Stok hareketleri, Dynamics 365 Supply Chain Management uygulamasında fiziksel olarak ve mali olarak güncellenebilir.</span><span class="sxs-lookup"><span data-stu-id="0dae5-105">Inventory transactions can be physically updated and financially updated in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="0dae5-106">Bazı fiziksel ve mali hareket türleri stok miktarlarını artırırken, bazıları bu miktarlar azaltır.</span><span class="sxs-lookup"><span data-stu-id="0dae5-106">Some types of physical and financial transactions increase inventory quantities, whereas others decrease the quantity.</span></span>

## <a name="physical-increases"></a><span data-ttu-id="0dae5-107">Fiziksel artışlar</span><span class="sxs-lookup"><span data-stu-id="0dae5-107">Physical increases</span></span>
<span data-ttu-id="0dae5-108">Bir fiziksel hareket nakledildiğinde, hareket kaydının durumu **Alındı** olur.</span><span class="sxs-lookup"><span data-stu-id="0dae5-108">When a physical transaction is posted, the status of the transaction record is **Received**.</span></span> <span data-ttu-id="0dae5-109">Aşağıdaki hareketler fiziksel artış olarak kabul edilir:</span><span class="sxs-lookup"><span data-stu-id="0dae5-109">The following transactions are considered physical increases:</span></span>

-   <span data-ttu-id="0dae5-110">Satınalma siparişi girişi</span><span class="sxs-lookup"><span data-stu-id="0dae5-110">Purchase order receipt</span></span>
-   <span data-ttu-id="0dae5-111">Satış siparişinin sevk irsaliyesi iadesi</span><span class="sxs-lookup"><span data-stu-id="0dae5-111">Sales order packing slip return</span></span>
-   <span data-ttu-id="0dae5-112">Bir üretim emrinin tamamlandı olarak rapor edilmesi</span><span class="sxs-lookup"><span data-stu-id="0dae5-112">Reporting a production order as finished</span></span>
-   <span data-ttu-id="0dae5-113">Üretim emri malzeme çekme listesinde ürüne göre</span><span class="sxs-lookup"><span data-stu-id="0dae5-113">By-product on a production order picking list</span></span>

## <a name="financial-increases"></a><span data-ttu-id="0dae5-114">Mali artışlar</span><span class="sxs-lookup"><span data-stu-id="0dae5-114">Financial increases</span></span>
<span data-ttu-id="0dae5-115">Bir mali giriş hareketi nakledildiğinde, miktarı artıran hareket kaydının durumu **Satın alındı** olur.</span><span class="sxs-lookup"><span data-stu-id="0dae5-115">When a financial receipt transaction is posted, the status of the transaction record that increases the quantity is **Purchased**.</span></span> <span data-ttu-id="0dae5-116">Aşağıdaki hareketler mali artış olarak kabul edilir:</span><span class="sxs-lookup"><span data-stu-id="0dae5-116">The following transactions are considered financial increases:</span></span>

-   <span data-ttu-id="0dae5-117">Satıcı faturası</span><span class="sxs-lookup"><span data-stu-id="0dae5-117">Vendor invoice</span></span>
-   <span data-ttu-id="0dae5-118">İade için satınalma siparişi faturası</span><span class="sxs-lookup"><span data-stu-id="0dae5-118">Sales order invoice for a return</span></span>
-   <span data-ttu-id="0dae5-119">Üretim emri maliyeti</span><span class="sxs-lookup"><span data-stu-id="0dae5-119">Production order costing</span></span>
-   <span data-ttu-id="0dae5-120">Hareket, kar ve zarar, sayım, malzeme listesi ve transfer vb. gibi pozitif miktar stok günlükleri</span><span class="sxs-lookup"><span data-stu-id="0dae5-120">Positive quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

## <a name="transactions-that-increase-quantity"></a><span data-ttu-id="0dae5-121">Miktarı artıran hareketler</span><span class="sxs-lookup"><span data-stu-id="0dae5-121">Transactions that increase quantity</span></span>
<span data-ttu-id="0dae5-122">Miktarı artıran hareketler çalışan ortalama maliyet fiyatı üzerinden nakledilir.</span><span class="sxs-lookup"><span data-stu-id="0dae5-122">Transactions that increase quantity are posted at the running average cost price.</span></span> <span data-ttu-id="0dae5-123">Hesaplanan cari ortalama maliyet fiyat, finansal olarak takip edilen her bir stok boyutu için bu hareketlerin her birinin maliyetine dayanır.</span><span class="sxs-lookup"><span data-stu-id="0dae5-123">The calculated running average cost price is based on the cost of each of these transactions for each inventory dimension that is being tracked financially.</span></span> <span data-ttu-id="0dae5-124">Çalışan ortalama maliyet fiyatları hakkında daha fazla bilgi için [Çalışan ortalama maliyet fiyatı](running-average-cost-price.md) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="0dae5-124">For information about running average cost prices, see [Running average cost price](running-average-cost-price.md).</span></span>

## <a name="transactions-that-decrease-quantity"></a><span data-ttu-id="0dae5-125">Miktarı azaltan hareketler</span><span class="sxs-lookup"><span data-stu-id="0dae5-125">Transactions that decrease quantity</span></span>
<span data-ttu-id="0dae5-126">Miktarı azaltan bir hareket nakledildiğinde bu stokla ilişkili olan stok modeline bakılmaksızın, hesaplanan cari ortalama maliyet fiyatı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0dae5-126">The calculated running average cost price is used  when a transaction that decreases quantity is posted, regardless of the inventory model that is associated with that inventory.</span></span> <span data-ttu-id="0dae5-127">Miktarı azaltan hareket kesinlikle nakledilmeden önce başka bir harekete işaretlenmemiş olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0dae5-127">The transaction that decreases quantity must not have been marked to another transaction before it was posted.</span></span> <span data-ttu-id="0dae5-128">Eldeki fiziksel stokun negatif hale gelmesi durumunda **Madde** sayfasında tanımlanan stok maliyeti kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0dae5-128">If the physical on-hand inventory becomes negative, the inventory cost that is defined for the item on the **Item** page is used.</span></span> 

> [!NOTE]
> <span data-ttu-id="0dae5-129">Birden fazla saha içeren bir işlev etkinleştirilirse bunun yerine bu maliyet, bir saha için **Varsayılan sipariş ayarları** sayfasında tanımlanan stok maliyeti olur.</span><span class="sxs-lookup"><span data-stu-id="0dae5-129">If multisite functionality is enabled, this cost will instead be the inventory cost that is defined for a site on the **Default order settings** page.</span></span>

## <a name="physical-issues-vs-financial-issues"></a><span data-ttu-id="0dae5-130">Fiziksel çıkışlar ile mali çıkışlar karşılaştırması</span><span class="sxs-lookup"><span data-stu-id="0dae5-130">Physical issues vs. financial issues</span></span>
<span data-ttu-id="0dae5-131">Bir fiziksel çıkış hareketi nakledildiğinde, hareket kaydının durumu **Kesinti yapıldı** olur.</span><span class="sxs-lookup"><span data-stu-id="0dae5-131">When a physical issue transaction is posted, the status of the transaction record is **Deducted**.</span></span> <span data-ttu-id="0dae5-132">Aşağıdaki hareketler fiziksel çıkışlar olarak kabul edilir:</span><span class="sxs-lookup"><span data-stu-id="0dae5-132">The following transactions are considered physical issues:</span></span>

-   <span data-ttu-id="0dae5-133">Üretim emri malzeme çekme listesi günlüğü</span><span class="sxs-lookup"><span data-stu-id="0dae5-133">Production order picking list journal</span></span>
-   <span data-ttu-id="0dae5-134">Satış siparişinin sevk irsaliyesi</span><span class="sxs-lookup"><span data-stu-id="0dae5-134">Sales order packing slip</span></span>
-   <span data-ttu-id="0dae5-135">Satınalma siparişinin sevk irsaliyesi iadesi</span><span class="sxs-lookup"><span data-stu-id="0dae5-135">Purchase order packing slip return</span></span>

<span data-ttu-id="0dae5-136">Bir finansal hareket nakledildiğinde, hareket kaydının durumu **Satılan** olur.</span><span class="sxs-lookup"><span data-stu-id="0dae5-136">When a financial transaction is posted, the status of the transaction record is **Sold**.</span></span> <span data-ttu-id="0dae5-137">Aşağıdaki hareketler mali çıkışlar olarak kabul edilir:</span><span class="sxs-lookup"><span data-stu-id="0dae5-137">The following transactions are considered financial issues:</span></span>

-   <span data-ttu-id="0dae5-138">Bir üretim emrinin sonlandırılması</span><span class="sxs-lookup"><span data-stu-id="0dae5-138">Ending a production order</span></span>
-   <span data-ttu-id="0dae5-139">Satış siparişi faturası</span><span class="sxs-lookup"><span data-stu-id="0dae5-139">Sales order invoice</span></span>
-   <span data-ttu-id="0dae5-140">Satıcı fatura iadesi</span><span class="sxs-lookup"><span data-stu-id="0dae5-140">Vendor invoice return</span></span>
-   <span data-ttu-id="0dae5-141">Hareket, kar ve zarar, sayım, malzeme listesi ve transfer vb. gibi negatif miktar stok günlükleri</span><span class="sxs-lookup"><span data-stu-id="0dae5-141">Negative quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

<span data-ttu-id="0dae5-142">Miktarı azaltan hareketler çalışan ortalama maliyet fiyatı üzerinden nakledilir.</span><span class="sxs-lookup"><span data-stu-id="0dae5-142">Transactions that decrease quantity are posted at the running average cost price.</span></span> <span data-ttu-id="0dae5-143">Bu nedenle, her bir maddeye atanan stok modeline dayalı olarak, çıkış hareketlerinin giriş hareketlerine kapatılması için stok kapanışı prosedürü uygulanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0dae5-143">Therefore, the inventory close procedure is required in order to settle issue transactions to receipt transactions, based on the inventory model that is assigned to each item.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]