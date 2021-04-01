---
title: Yük planlama çalışma ekranından Ambara serbest bırakma kullanılarak sevkiyatları konsolide etme
description: Bu konu, çoklu siparişlerin aynı yükte yer alarak ambara serbest bırakıldığı ve ardından, otomatik olarak sevkiyatlar halinde birleştirildiği bir senaryo sunar.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 2fd13c2ceb8843b79b9dbc87acf77f219f0244f5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242265"
---
# <a name="consolidate-shipments-by-using-release-to-warehouse-from-the-load-planning-workbench"></a><span data-ttu-id="f9bf1-103">Yük planlama çalışma ekranından Ambara serbest bırakma kullanılarak sevkiyatları konsolide etme</span><span class="sxs-lookup"><span data-stu-id="f9bf1-103">Consolidate shipments by using Release to warehouse from the load planning workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9bf1-104">Bu konu, çoklu siparişlerin aynı yükte yer alarak ambara serbest bırakıldığı ve ardından, otomatik olarak sevkiyatlar halinde birleştirildiği bir senaryo sunar.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-104">This topic presents a scenario where multiple orders are released to the warehouse in the same load and are then automatically consolidated into shipments.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="f9bf1-105">Tanıtım verilerini kullanılabilir hale getirme</span><span class="sxs-lookup"><span data-stu-id="f9bf1-105">Make demo data available</span></span>

<span data-ttu-id="f9bf1-106">Bu konudaki senaryo, Microsoft Dynamics 365 Supply Chain Management için sağlanan standart tanıtım verilerinde bulunan değerlere ve kayıtlara başvurur.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="f9bf1-107">Alıştırmaları yaparken burada sağlanan değerleri kullanmak isterseniz tanıtım verisinin yüklü olduğu bir ortamda çalıştığınızdan ve başlamadan önce tüzel kişiliği **USMF** olarak ayarladığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="f9bf1-108">Sevkiyat konsolidasyon ilkelerini ve ürün filtrelerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="f9bf1-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="f9bf1-109">Burada açıklanan senaryo, özelliği önceden açtığınız, [Sevkiyat konsolidasyonu ilkelerini yapılandırma](configure-shipment-consolidation-policies.md) alıştırmalarını yaptığınız ve burada açıklanan ilkeleri ve diğer kayıtları oluşturduğunuz varsayımına dayanır.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="f9bf1-110">Bu senaryoya devam etmeden önce söz konusu alıştırmaları yaptığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="f9bf1-111">Bu senaryo için satış siparişleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="f9bf1-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="f9bf1-112">Çalışabileceğiniz bir satış siparişleri koleksiyonu oluşturarak başlayın.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="f9bf1-113">Gelişmiş ambar (WMS) işlemleri için etkinleştirilen bir ambarla çalışmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="f9bf1-114">Başka bir ambar açıkça belirtilmedikçe, aşağıdaki sipariş kümelerinin her biri için aynı ambar kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="f9bf1-115">**Alacak hesapları \> Siparişler \> Tüm satış siparişleri** öğesine gidin ve aşağıdaki alt bölümlerde açıklanan ayarlara sahip bir satış siparişleri koleksiyonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="f9bf1-116">Sipariş kümesi 1'i oluşturma</span><span class="sxs-lookup"><span data-stu-id="f9bf1-116">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="f9bf1-117">Satış siparişi 1-1</span><span class="sxs-lookup"><span data-stu-id="f9bf1-117">Sales order 1-1</span></span>

1. <span data-ttu-id="f9bf1-118">Aşağıdaki ayarlara sahip bir satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="f9bf1-118">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="f9bf1-119">**Müşteri hesabı:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="f9bf1-119">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="f9bf1-120">**Teslimat şekli:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="f9bf1-120">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="f9bf1-121">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="f9bf1-121">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="f9bf1-122">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="f9bf1-122">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="f9bf1-123">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f9bf1-123">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="f9bf1-124">**Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-124">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="f9bf1-125">Satış siparişi 1-2</span><span class="sxs-lookup"><span data-stu-id="f9bf1-125">Sales order 1-2</span></span>

1. <span data-ttu-id="f9bf1-126">Aşağıdaki ayarlara sahip bir satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="f9bf1-126">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="f9bf1-127">**Müşteri hesabı:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="f9bf1-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="f9bf1-128">**Teslimat şekli:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="f9bf1-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="f9bf1-129">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="f9bf1-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="f9bf1-130">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="f9bf1-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="f9bf1-131">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f9bf1-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="f9bf1-132">**Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="f9bf1-133">Satış siparişi 1-3</span><span class="sxs-lookup"><span data-stu-id="f9bf1-133">Sales order 1-3</span></span>

1. <span data-ttu-id="f9bf1-134">Aşağıdaki ayarlara sahip bir satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="f9bf1-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="f9bf1-135">**Müşteri hesabı:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="f9bf1-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="f9bf1-136">**Teslimat şekli:** *10*</span><span class="sxs-lookup"><span data-stu-id="f9bf1-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="f9bf1-137">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="f9bf1-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="f9bf1-138">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="f9bf1-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="f9bf1-139">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f9bf1-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="f9bf1-140">**Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="f9bf1-141">Aşağıdaki ayarlara sahip ikinci bir satış siparişi satırı oluşturun:</span><span class="sxs-lookup"><span data-stu-id="f9bf1-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="f9bf1-142">**Madde numarası:** *A0002* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="f9bf1-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="f9bf1-143">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f9bf1-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="f9bf1-144">**Teslimat şekli:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="f9bf1-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="f9bf1-145">**Stok \> Rezervasyon**'u ve sonra Eylem Bölmesi'nde, ikinci sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="f9bf1-146">Sipariş kümesi 2'yi oluşturma</span><span class="sxs-lookup"><span data-stu-id="f9bf1-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="f9bf1-147">Satış siparişleri 2-1 ve 2-2</span><span class="sxs-lookup"><span data-stu-id="f9bf1-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="f9bf1-148">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="f9bf1-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="f9bf1-149">**Müşteri hesabı:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="f9bf1-149">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="f9bf1-150">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="f9bf1-150">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="f9bf1-151">**Madde numarası:** *M9200* (**Kod 4** filtresinin *Yanıcı* değerine ayarlandığı bir madde)</span><span class="sxs-lookup"><span data-stu-id="f9bf1-151">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="f9bf1-152">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f9bf1-152">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="f9bf1-153">**Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-153">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="f9bf1-154">Aşağıdaki ayarlara sahip ikinci bir satış siparişi satırı oluşturun:</span><span class="sxs-lookup"><span data-stu-id="f9bf1-154">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="f9bf1-155">**Madde numarası:** *M9201* (**Kod 4** filtresinin *Patlayıcı* değerine ayarlandığı bir madde)</span><span class="sxs-lookup"><span data-stu-id="f9bf1-155">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="f9bf1-156">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f9bf1-156">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="f9bf1-157">**Teslimat şekli:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="f9bf1-157">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="f9bf1-158">**Stok \> Rezervasyon**'u ve sonra Eylem Bölmesi'nde, ikinci sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-158">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="f9bf1-159">Sipariş kümesi 3'ü oluşturma</span><span class="sxs-lookup"><span data-stu-id="f9bf1-159">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="f9bf1-160">Satış siparişleri 3-1 ve 3-2</span><span class="sxs-lookup"><span data-stu-id="f9bf1-160">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="f9bf1-161">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="f9bf1-161">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="f9bf1-162">**Müşteri hesabı:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="f9bf1-162">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="f9bf1-163">**Müşteri talebi:** *1*</span><span class="sxs-lookup"><span data-stu-id="f9bf1-163">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="f9bf1-164">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="f9bf1-164">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="f9bf1-165">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="f9bf1-165">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="f9bf1-166">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f9bf1-166">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="f9bf1-167">**Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-167">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="f9bf1-168">Satış siparişleri 3-3 ve 3-4</span><span class="sxs-lookup"><span data-stu-id="f9bf1-168">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="f9bf1-169">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="f9bf1-169">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="f9bf1-170">**Müşteri hesabı:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="f9bf1-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="f9bf1-171">**Müşteri talebi:** *2*</span><span class="sxs-lookup"><span data-stu-id="f9bf1-171">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="f9bf1-172">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="f9bf1-172">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="f9bf1-173">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="f9bf1-173">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="f9bf1-174">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f9bf1-174">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="f9bf1-175">**Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-175">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="f9bf1-176">Sipariş kümesi 4'ü oluşturma</span><span class="sxs-lookup"><span data-stu-id="f9bf1-176">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="f9bf1-177">Satış siparişleri 4-1 ve 4-2</span><span class="sxs-lookup"><span data-stu-id="f9bf1-177">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="f9bf1-178">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="f9bf1-178">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="f9bf1-179">**Müşteri hesabı:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="f9bf1-179">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="f9bf1-180">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="f9bf1-180">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="f9bf1-181">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="f9bf1-181">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="f9bf1-182">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f9bf1-182">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="f9bf1-183">**Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-183">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="f9bf1-184">Satış siparişleri 4-3 ve 4-4</span><span class="sxs-lookup"><span data-stu-id="f9bf1-184">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="f9bf1-185">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="f9bf1-185">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="f9bf1-186">**Müşteri hesabı:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="f9bf1-186">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="f9bf1-187">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="f9bf1-187">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="f9bf1-188">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="f9bf1-188">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="f9bf1-189">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f9bf1-189">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="f9bf1-190">**Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-190">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="f9bf1-191">Satış siparişleri 4-5 ve 4-6</span><span class="sxs-lookup"><span data-stu-id="f9bf1-191">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="f9bf1-192">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="f9bf1-192">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="f9bf1-193">**Müşteri hesabı:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="f9bf1-193">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="f9bf1-194">**Tesis:** *6*</span><span class="sxs-lookup"><span data-stu-id="f9bf1-194">**Site:** *6*</span></span>
    - <span data-ttu-id="f9bf1-195">**Ambar:** *61*</span><span class="sxs-lookup"><span data-stu-id="f9bf1-195">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="f9bf1-196">**Havuz:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="f9bf1-196">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="f9bf1-197">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="f9bf1-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="f9bf1-198">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="f9bf1-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="f9bf1-199">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f9bf1-199">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="f9bf1-200">**Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-200">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="f9bf1-201">Satış siparişleri 4-7 ve 4-8</span><span class="sxs-lookup"><span data-stu-id="f9bf1-201">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="f9bf1-202">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="f9bf1-202">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="f9bf1-203">**Müşteri hesabı:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="f9bf1-203">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="f9bf1-204">**Tesis:** *6*</span><span class="sxs-lookup"><span data-stu-id="f9bf1-204">**Site:** *6*</span></span>
    - <span data-ttu-id="f9bf1-205">**Ambar:** *61*</span><span class="sxs-lookup"><span data-stu-id="f9bf1-205">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="f9bf1-206">**Havuz:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-206">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="f9bf1-207">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="f9bf1-207">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="f9bf1-208">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="f9bf1-208">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="f9bf1-209">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="f9bf1-209">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="f9bf1-210">**Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-210">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="use-the-load-planning-workbench-to-create-loads-and-release-them-to-the-warehouse"></a><span data-ttu-id="f9bf1-211">Yükler oluşturmak ve bunları ambara serbest bırakmak için yük planlama çalışma ekranını kullanma</span><span class="sxs-lookup"><span data-stu-id="f9bf1-211">Use the load planning workbench to create loads and release them to the warehouse</span></span>

<span data-ttu-id="f9bf1-212">Bu senaryo için oluşturduğunuz her sipariş kümesi için bir yük oluşturmak ve sonra bunu ambara serbest bırakmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-212">Follow these steps to create a load for each order set that you created for this scenario and then release it to the warehouse.</span></span>

1. <span data-ttu-id="f9bf1-213">**Ambar yönetimi \> Yükler \> Yük planlama çalışma ekranı** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-213">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="f9bf1-214">**Satış satırları** sekmesinde, bu senaryo için oluşturduğunuz sipariş kümelerinden birindeki tüm satış siparişi satırlarını bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-214">On the **Sales lines** tab, find and select all the sales order lines from one of the order sets that you created for this scenario.</span></span>
1. <span data-ttu-id="f9bf1-215">Eylem Bölmesi'ndeki **Arz ve talep** sekmesinde, seçili sipariş satırlarını yeni bir Yüke eklemek için **Ekle \> Yeni yüke** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-215">On the Action Pane, on the **Supply and demand** tab, select **Add \> To new load** to add the selected order lines to a new Load.</span></span>
1. <span data-ttu-id="f9bf1-216">**Yük şablonu ataması** iletişim kutusundaki **Yük şablonu kimliği** alanında, *Stnd Yük Şablonu* gibi bir yük şablonu seçin.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-216">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *Stnd Load Template*.</span></span>
1. <span data-ttu-id="f9bf1-217">İletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-217">Select **OK** to close the dialog box.</span></span> 
1. <span data-ttu-id="f9bf1-218">**Yükler** bölümünde, az önce oluşturduğunuz yükü bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-218">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="f9bf1-219">Seçili yükü ambara serbest bırakmak için **Serbest bırak \> Ambara serbest bırak** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-219">Select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="f9bf1-220">Bu yordamı, bu senaryo için oluşturduğunuz diğer üç sipariş kümesi için yineleyin.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-220">Repeat this procedure for the other three order sets that you created for this scenario.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="f9bf1-221">Sevkiyatları doğrulama</span><span class="sxs-lookup"><span data-stu-id="f9bf1-221">Verify the shipments</span></span>

<span data-ttu-id="f9bf1-222">Aşağıdaki yordam, sevkiyat konsolidasyonu nedeniyle oluşturulan veya güncelleştirilen sevkiyatları doğrulamanıza olanak verir.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-222">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="f9bf1-223">Bu senaryo için oluşturduğunuz her bir sipariş kümesini gözden geçirmek için bunu kullanın ve sonra, beklenen sonuçları elde ettiğinize emin olmak için izleyen alt bölümleri gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-223">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="f9bf1-224">**Ambar yönetimi \> Sevkiyatlar \> Tüm sevkiyatlar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-224">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="f9bf1-225">Gerekli sevkiyatı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-225">Find and select the required shipment.</span></span>
1. <span data-ttu-id="f9bf1-226">Sevkiyat oluşturulduğunda veya güncelleştirildiğinde bir konsolidasyon ilkesi kullanılmışsa bunu **Sevkiyat konsolidasyon ilkesi** alanında görmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-226">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-order-set-1-in-one-load"></a><span data-ttu-id="f9bf1-227">Bir yükte sipariş kümesi 1'i serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="f9bf1-227">Release order set 1 in one load</span></span>

<span data-ttu-id="f9bf1-228">İki sevkiyat oluşturulmuş olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="f9bf1-228">Two shipments should have been created:</span></span>

- <span data-ttu-id="f9bf1-229">İlk sevkiyat üç satır içerir ve *CustomerMode* sevkiyat konsolidasyon ilkesi kullanılarak oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-229">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="f9bf1-230">Taşıma teslimat şekli için *Hava yolu* kullanmayan ikinci sevkiyat, *CustomerOrderNo* sevkiyat konsolidasyon ilkesi kullanılarak oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-230">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-order-set-2-in-one-load"></a><span data-ttu-id="f9bf1-231">Bir yükte sipariş kümesi 2'yi serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="f9bf1-231">Release order set 2 in one load</span></span>

<span data-ttu-id="f9bf1-232">Üç sevkiyat oluşturulmuş olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="f9bf1-232">Three shipments should have been created:</span></span>

- <span data-ttu-id="f9bf1-233">İlk sevkiyat *Yanıcı* maddeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-233">The first shipment contains the *Flammable* items.</span></span>
- <span data-ttu-id="f9bf1-234">Diğer iki sevkiyatın her biri, *Patlayıcı* madde içeren bir satır içerir.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-234">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-order-set-3-in-one-load"></a><span data-ttu-id="f9bf1-235">Bir yükte sipariş kümesi 3'ü serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="f9bf1-235">Release order set 3 in one load</span></span>

<span data-ttu-id="f9bf1-236">İki sevkiyat oluşturulmuş olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="f9bf1-236">Two shipments should have been created:</span></span>

- <span data-ttu-id="f9bf1-237">İlk sevkiyat, **Müşteri talebi** alanının *1* olarak ayarlandığı satış siparişinden sipariş satırları içerir.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-237">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="f9bf1-238">İkinci sevkiyat, **Müşteri talebi** alanının *2* olarak ayarlandığı satış siparişinden sipariş satırları içerir.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-238">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="release-order-set-4-in-one-load"></a><span data-ttu-id="f9bf1-239">Bir yükte sipariş kümesi 4'ü serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="f9bf1-239">Release order set 4 in one load</span></span>

<span data-ttu-id="f9bf1-240">Dört sevkiyat oluşturulmuş olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="f9bf1-240">Four shipments should have been created:</span></span>

- <span data-ttu-id="f9bf1-241">Müşteri hesabı *US-003* ile ilgili iki siparişin satırları, *Sipariş havuzu* sevkiyat konsolidasyon ilkesi kullanılarak tek bir sevkiyatta gruplandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-241">Lines from two orders for customer account *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="f9bf1-242">Müşteri hesabı *US-004* ile ilgili iki siparişin satırları, *Sipariş havuzu* sevkiyat konsolidasyon ilkesi kullanılarak tek bir sevkiyatta gruplandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-242">Lines from two orders for customer account *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="f9bf1-243">Müşteri hesabı *US-007* ile ilgili satış siparişi 4-5 ve 4-6'daki satırlar, *Sipariş havuzu* sevkiyat konsolidasyon ilkesi kullanılarak tek bir sevkiyatta gruplandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-243">Lines from sales orders 4-5 and 4-6 for customer account *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="f9bf1-244">Müşteri hesabı *US-007* ile ilgili satış siparişi 4-7 ve 4-8'daki satırlar, *CrossOrder* sevkiyat konsolidasyon ilkesi kullanılarak tek bir sevkiyatta gruplandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="f9bf1-244">Lines from sales orders 4-7 and 4-8 for customer account *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f9bf1-245">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="f9bf1-245">Additional resources</span></span>

- [<span data-ttu-id="f9bf1-246">Sevkiyat konsolidasyonu ilkeleri</span><span class="sxs-lookup"><span data-stu-id="f9bf1-246">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="f9bf1-247">Sevkiyat konsolidasyon ilkelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="f9bf1-247">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]