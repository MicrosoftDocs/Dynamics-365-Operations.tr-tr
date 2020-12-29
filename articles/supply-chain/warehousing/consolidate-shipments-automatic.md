---
title: Satış siparişlerinin otomatik serbest bırakılması kullanılarak ambara serbest bırakıldıklarında sevkiyatları konsolide etme
description: Bu konu, çoklu siparişlerin aynı otomatik ambara serbest bırakma periyodik yordamında yer alarak ambara serbest bırakıldığı bir senaryo sunar.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: ac3ab25dc1355ee15e1209950ff0f3b3933b7095
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4439641"
---
# <a name="consolidate-shipments-when-they-are-released-to-the-warehouse-by-using-automatic-release-of-sales-orders"></a><span data-ttu-id="c6d43-103">Satış siparişlerinin otomatik serbest bırakılması kullanılarak ambara serbest bırakıldıklarında sevkiyatları konsolide etme</span><span class="sxs-lookup"><span data-stu-id="c6d43-103">Consolidate shipments when they are released to the warehouse by using Automatic release of sales orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6d43-104">Bu konu, çoklu siparişlerin aynı otomatik ambara serbest bırakma periyodik yordamında yer alarak ambara serbest bırakıldığı bir senaryo sunar.</span><span class="sxs-lookup"><span data-stu-id="c6d43-104">This topic presents a scenario where multiple orders are released to the warehouse in the same automated release-to-warehouse periodic procedure.</span></span> <span data-ttu-id="c6d43-105">Siparişler, sevkiyat konsolidasyon ilkeleri olarak tanımlanan kurallara göre otomatik olarak sevkiyatlar halinde konsolide edilecektir.</span><span class="sxs-lookup"><span data-stu-id="c6d43-105">The orders will automatically be consolidated into shipments, based on rules that are defined as shipment consolidation policies.</span></span>

<span data-ttu-id="c6d43-106">Senaryo sırasında, satış siparişi kümeleri oluşturacak ve her kümeyi ambara serbest bırakacaksınız.</span><span class="sxs-lookup"><span data-stu-id="c6d43-106">During the scenario, you will create sets of sales orders and release each set to the warehouse.</span></span> <span data-ttu-id="c6d43-107">Böylece, yapılandırılan ilkelere göre, sevkiyat konsolidasyonu sırasında oluşturulan veya güncelleştirilen sevkiyatları gözden geçireceksiniz.</span><span class="sxs-lookup"><span data-stu-id="c6d43-107">You will then review the shipments that are created or updated during shipment consolidation, based on the configured policies.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="c6d43-108">Tanıtım verilerini kullanılabilir hale getirme</span><span class="sxs-lookup"><span data-stu-id="c6d43-108">Make demo data available</span></span>

<span data-ttu-id="c6d43-109">Bu konudaki senaryo, Microsoft Dynamics 365 Supply Chain Management için sağlanan standart tanıtım verilerinde bulunan değerlere ve kayıtlara başvurur.</span><span class="sxs-lookup"><span data-stu-id="c6d43-109">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="c6d43-110">Alıştırmaları yaparken burada sağlanan değerleri kullanmak isterseniz tanıtım verisinin yüklü olduğu bir ortamda çalıştığınızdan ve başlamadan önce tüzel kişiliği **USMF** olarak ayarladığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="c6d43-110">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="c6d43-111">Sevkiyat konsolidasyon ilkelerini ve ürün filtrelerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="c6d43-111">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="c6d43-112">Burada açıklanan senaryo, özelliği önceden açtığınız, [Sevkiyat konsolidasyonu ilkelerini yapılandırma](configure-shipment-consolidation-policies.md) alıştırmalarını yaptığınız ve burada açıklanan ilkeleri ve diğer kayıtları oluşturduğunuz varsayımına dayanır.</span><span class="sxs-lookup"><span data-stu-id="c6d43-112">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="c6d43-113">Bu senaryoya devam etmeden önce söz konusu alıştırmaları yaptığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="c6d43-113">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="c6d43-114">Bu senaryo için satış siparişleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="c6d43-114">Create the sales orders for this scenario</span></span>

<span data-ttu-id="c6d43-115">Çalışabileceğiniz bir satış siparişleri koleksiyonu oluşturarak başlayın.</span><span class="sxs-lookup"><span data-stu-id="c6d43-115">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="c6d43-116">Gelişmiş ambar (WMS) işlemleri için etkinleştirilen bir ambarla çalışmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="c6d43-116">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="c6d43-117">Başka bir ambar açıkça belirtilmedikçe, aşağıdaki sipariş kümelerinin her biri için aynı ambar kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c6d43-117">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="c6d43-118">**Alacak hesapları \> Siparişler \> Tüm satış siparişleri** öğesine gidin ve aşağıdaki alt bölümlerde açıklanan ayarlara sahip bir satış siparişleri koleksiyonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c6d43-118">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="c6d43-119">Sipariş kümesi 1'i oluşturma</span><span class="sxs-lookup"><span data-stu-id="c6d43-119">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="c6d43-120">Satış siparişi 1-1</span><span class="sxs-lookup"><span data-stu-id="c6d43-120">Sales order 1-1</span></span>

1. <span data-ttu-id="c6d43-121">Aşağıdaki ayarlara sahip bir satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="c6d43-121">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="c6d43-122">**Müşteri hesabı:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="c6d43-122">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="c6d43-123">**Teslimat şekli:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="c6d43-123">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="c6d43-124">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="c6d43-124">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c6d43-125">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="c6d43-125">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c6d43-126">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c6d43-126">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="c6d43-127">Satış siparişi 1-2</span><span class="sxs-lookup"><span data-stu-id="c6d43-127">Sales order 1-2</span></span>

1. <span data-ttu-id="c6d43-128">Aşağıdaki ayarlara sahip bir satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="c6d43-128">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="c6d43-129">**Müşteri hesabı:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="c6d43-129">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="c6d43-130">**Teslimat şekli:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="c6d43-130">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="c6d43-131">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="c6d43-131">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c6d43-132">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="c6d43-132">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c6d43-133">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c6d43-133">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="c6d43-134">Satış siparişi 1-3</span><span class="sxs-lookup"><span data-stu-id="c6d43-134">Sales order 1-3</span></span>

1. <span data-ttu-id="c6d43-135">Aşağıdaki ayarlara sahip bir satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="c6d43-135">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="c6d43-136">**Müşteri hesabı:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="c6d43-136">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="c6d43-137">**Teslimat şekli:** *10*</span><span class="sxs-lookup"><span data-stu-id="c6d43-137">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="c6d43-138">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="c6d43-138">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c6d43-139">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="c6d43-139">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c6d43-140">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c6d43-140">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="c6d43-141">Aşağıdaki ayarlara sahip ikinci bir satış siparişi satırı oluşturun:</span><span class="sxs-lookup"><span data-stu-id="c6d43-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="c6d43-142">**Madde numarası:** *A0002* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="c6d43-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c6d43-143">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c6d43-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="c6d43-144">**Teslimat şekli:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="c6d43-144">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="c6d43-145">Sipariş kümesi 2'yi oluşturma</span><span class="sxs-lookup"><span data-stu-id="c6d43-145">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="c6d43-146">Satış siparişleri 2-1 ve 2-2</span><span class="sxs-lookup"><span data-stu-id="c6d43-146">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="c6d43-147">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="c6d43-147">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="c6d43-148">**Müşteri hesabı:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="c6d43-148">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="c6d43-149">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="c6d43-149">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c6d43-150">**Madde numarası:** *M9200* (**Kod 4** filtresinin *Yanıcı* değerine ayarlandığı bir madde)</span><span class="sxs-lookup"><span data-stu-id="c6d43-150">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="c6d43-151">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c6d43-151">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="c6d43-152">Aşağıdaki ayarlara sahip ikinci bir satış siparişi satırı oluşturun:</span><span class="sxs-lookup"><span data-stu-id="c6d43-152">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="c6d43-153">**Madde numarası:** *M9201* (**Kod 4** filtresinin *Patlayıcı* değerine ayarlandığı bir madde)</span><span class="sxs-lookup"><span data-stu-id="c6d43-153">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="c6d43-154">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c6d43-154">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="c6d43-155">**Teslimat şekli:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="c6d43-155">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="c6d43-156">Sipariş kümesi 3'ü oluşturma</span><span class="sxs-lookup"><span data-stu-id="c6d43-156">Create order set 3</span></span>

#### <a name="sales-order-3-1"></a><span data-ttu-id="c6d43-157">Satış siparişi 3-1</span><span class="sxs-lookup"><span data-stu-id="c6d43-157">Sales order 3-1</span></span>

1. <span data-ttu-id="c6d43-158">Aşağıdaki ayarlara sahip bir satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="c6d43-158">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="c6d43-159">**Müşteri hesabı:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="c6d43-159">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="c6d43-160">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="c6d43-160">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c6d43-161">**Madde numarası:** *M9200* (**Kod 4** filtresinin *Yanıcı* değerine ayarlandığı bir madde)</span><span class="sxs-lookup"><span data-stu-id="c6d43-161">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="c6d43-162">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c6d43-162">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="c6d43-163">Aşağıdaki ayarlara sahip ikinci bir satış siparişi satırı oluşturun:</span><span class="sxs-lookup"><span data-stu-id="c6d43-163">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="c6d43-164">**Madde numarası:** *M9201* (**Kod 4** filtresinin *Patlayıcı* değerine ayarlandığı bir madde)</span><span class="sxs-lookup"><span data-stu-id="c6d43-164">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="c6d43-165">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c6d43-165">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="c6d43-166">**Teslimat şekli:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="c6d43-166">**Mode of delivery:** *Airwa-Air*</span></span>

> [!NOTE]
> <span data-ttu-id="c6d43-167">Bu sipariş, sipariş kümesi 2 için oluşturduğunuz iki siparişle aynıdır.</span><span class="sxs-lookup"><span data-stu-id="c6d43-167">This order is identical to the two orders that you created for order set 2.</span></span> <span data-ttu-id="c6d43-168">Ancak, bu senaryoda daha sonra ayrı olarak serbest bırakacağınız için kendi sipariş kümesi olarak listelenir.</span><span class="sxs-lookup"><span data-stu-id="c6d43-168">However, it's listed as its own order set because you will release it separately later in this scenario.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="c6d43-169">Sipariş kümesi 4'ü oluşturma</span><span class="sxs-lookup"><span data-stu-id="c6d43-169">Create order set 4</span></span>

#### <a name="sales-order-4-1"></a><span data-ttu-id="c6d43-170">Satış siparişi 4-1</span><span class="sxs-lookup"><span data-stu-id="c6d43-170">Sales order 4-1</span></span>

1. <span data-ttu-id="c6d43-171">Aşağıdaki ayarlara sahip bir satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="c6d43-171">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="c6d43-172">**Müşteri hesabı:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="c6d43-172">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="c6d43-173">**Müşteri talebi:** *1*</span><span class="sxs-lookup"><span data-stu-id="c6d43-173">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="c6d43-174">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="c6d43-174">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c6d43-175">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="c6d43-175">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c6d43-176">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c6d43-176">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-5"></a><span data-ttu-id="c6d43-177">Sipariş kümesi 5'yi oluşturma</span><span class="sxs-lookup"><span data-stu-id="c6d43-177">Create order set 5</span></span>

#### <a name="sales-orders-5-1-and-5-2"></a><span data-ttu-id="c6d43-178">Satış siparişleri 5-1 ve 5-2</span><span class="sxs-lookup"><span data-stu-id="c6d43-178">Sales orders 5-1 and 5-2</span></span>

1. <span data-ttu-id="c6d43-179">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="c6d43-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="c6d43-180">**Müşteri hesabı:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="c6d43-180">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="c6d43-181">**Müşteri talebi:** *2*</span><span class="sxs-lookup"><span data-stu-id="c6d43-181">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="c6d43-182">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="c6d43-182">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c6d43-183">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="c6d43-183">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c6d43-184">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c6d43-184">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-5-3"></a><span data-ttu-id="c6d43-185">Satış siparişi 5-3</span><span class="sxs-lookup"><span data-stu-id="c6d43-185">Sales order 5-3</span></span>

1. <span data-ttu-id="c6d43-186">Aşağıdaki ayarlara sahip bir satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="c6d43-186">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="c6d43-187">**Müşteri hesabı:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="c6d43-187">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="c6d43-188">**Müşteri talebi:** *1*</span><span class="sxs-lookup"><span data-stu-id="c6d43-188">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="c6d43-189">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="c6d43-189">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c6d43-190">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="c6d43-190">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c6d43-191">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c6d43-191">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-6"></a><span data-ttu-id="c6d43-192">Sipariş kümesi 6'yi oluşturma</span><span class="sxs-lookup"><span data-stu-id="c6d43-192">Create order set 6</span></span>

#### <a name="sales-orders-6-1-and-6-2"></a><span data-ttu-id="c6d43-193">Satış siparişleri 6-1 ve 6-2</span><span class="sxs-lookup"><span data-stu-id="c6d43-193">Sales orders 6-1 and 6-2</span></span>

1. <span data-ttu-id="c6d43-194">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="c6d43-194">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="c6d43-195">**Müşteri hesabı:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="c6d43-195">**Customer account:** *US-003*</span></span>
    - <span data-ttu-id="c6d43-196">**Müşteri talebi:** *2*</span><span class="sxs-lookup"><span data-stu-id="c6d43-196">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="c6d43-197">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="c6d43-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c6d43-198">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="c6d43-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c6d43-199">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c6d43-199">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-3-and-6-4"></a><span data-ttu-id="c6d43-200">Satış siparişleri 6-3 ve 6-4</span><span class="sxs-lookup"><span data-stu-id="c6d43-200">Sales orders 6-3 and 6-4</span></span>

1. <span data-ttu-id="c6d43-201">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="c6d43-201">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="c6d43-202">**Müşteri hesabı:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="c6d43-202">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="c6d43-203">**Müşteri talebi:** *1*</span><span class="sxs-lookup"><span data-stu-id="c6d43-203">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="c6d43-204">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="c6d43-204">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c6d43-205">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="c6d43-205">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c6d43-206">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c6d43-206">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-5-and-6-6"></a><span data-ttu-id="c6d43-207">Satış siparişleri 6-5 ve 6-6</span><span class="sxs-lookup"><span data-stu-id="c6d43-207">Sales orders 6-5 and 6-6</span></span>

1. <span data-ttu-id="c6d43-208">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="c6d43-208">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="c6d43-209">**Müşteri hesabı:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="c6d43-209">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="c6d43-210">**Tesis:** *6*</span><span class="sxs-lookup"><span data-stu-id="c6d43-210">**Site:** *6*</span></span>
    - <span data-ttu-id="c6d43-211">**Ambar:** *61*</span><span class="sxs-lookup"><span data-stu-id="c6d43-211">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="c6d43-212">**Havuz:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="c6d43-212">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="c6d43-213">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="c6d43-213">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c6d43-214">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="c6d43-214">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c6d43-215">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c6d43-215">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-7-and-6-8"></a><span data-ttu-id="c6d43-216">Satış siparişleri 6-7 ve 6-8</span><span class="sxs-lookup"><span data-stu-id="c6d43-216">Sales orders 6-7 and 6-8</span></span>

1. <span data-ttu-id="c6d43-217">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="c6d43-217">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="c6d43-218">**Müşteri hesabı:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="c6d43-218">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="c6d43-219">**Tesis:** *6*</span><span class="sxs-lookup"><span data-stu-id="c6d43-219">**Site:** *6*</span></span>
    - <span data-ttu-id="c6d43-220">**Ambar:** *61*</span><span class="sxs-lookup"><span data-stu-id="c6d43-220">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="c6d43-221">**Havuz:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="c6d43-221">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="c6d43-222">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="c6d43-222">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="c6d43-223">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="c6d43-223">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="c6d43-224">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="c6d43-224">**Quantity:** *1.00*</span></span>

## <a name="automatic-release-of-sales-orders-to-the-warehouse"></a><span data-ttu-id="c6d43-225">Satış siparişlerini ambara otomatik olarak serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="c6d43-225">Automatic release of sales orders to the warehouse</span></span>

<span data-ttu-id="c6d43-226">Daha önce oluşturduğunuz her satış siparişi kümesi için ambara otomatik olarak serbest bırakma yordamını tamamlayacaksınız.</span><span class="sxs-lookup"><span data-stu-id="c6d43-226">For each set of sales orders that you created earlier, you will complete a procedure for automatic release to the warehouse.</span></span> <span data-ttu-id="c6d43-227">Her örnekte, burada sağlanan [temel ambara serbest bırakma yordamı](#release-procedure) üzerinden çalışacaksınız.</span><span class="sxs-lookup"><span data-stu-id="c6d43-227">In each case, you will work through the [basic release-to-warehouse procedure](#release-procedure) that is provided here.</span></span>

### <a name="basic-release-to-warehouse-procedure"></a><a name="release-procedure"></a><span data-ttu-id="c6d43-228">Temel ambara serbest bırakma yordamı</span><span class="sxs-lookup"><span data-stu-id="c6d43-228">Basic release-to-warehouse procedure</span></span>

<span data-ttu-id="c6d43-229">Daha önce oluşturduğunuz her satış siparişi kümesi için aşağıdaki alt bölümlerde özetlenen üç yordamı tamamlayacaksınız.</span><span class="sxs-lookup"><span data-stu-id="c6d43-229">For each set of sales orders that you created earlier, you will complete the three procedures that are outlined in the following subsections.</span></span>

#### <a name="update-the-wave-template-that-will-be-used-during-release"></a><span data-ttu-id="c6d43-230">Serbest bırakma sırasında kullanılacak dalga şablonunu güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c6d43-230">Update the wave template that will be used during release</span></span>

1. <span data-ttu-id="c6d43-231">**Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga şablonları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="c6d43-231">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="c6d43-232">**Dalga şablonu türü** alanını *Sevkiyat* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c6d43-232">Set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="c6d43-233">Bu senaryo için oluşturduğunuz sipariş kümelerinde kullandığınız ambarla ilişkilendirilmiş dalga şablonunu bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="c6d43-233">Find and select the wave template that is associated with the warehouse that you used in the order sets that you created for this scenario.</span></span> <span data-ttu-id="c6d43-234">Örneğin, ambar *24*'ü kullandıysanız **24 Sevkiyat Varsayılan** dalga şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="c6d43-234">For example, if you used warehouse *24*, select the **24 Shipping Default** wave template.</span></span> <span data-ttu-id="c6d43-235">Ambar *61*'i kullandıysanız **61 Sevkiyat** dalga şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="c6d43-235">If you used warehouse *61*, select the **61 Shipping** wave template.</span></span>
1. <span data-ttu-id="c6d43-236">Eylem Bölmesi'nde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c6d43-236">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="c6d43-237">**Dalgayı ambara serbest bırakma sırasında işle** seçeneğini *Hayır* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c6d43-237">Set the **Process wave at release to warehouse** option to *No*.</span></span>

#### <a name="release-to-the-warehouse"></a><span data-ttu-id="c6d43-238">Ambara serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="c6d43-238">Release to the warehouse</span></span>

1. <span data-ttu-id="c6d43-239">**Ambar yönetimi \> Ambara serbest bırakma \> Satış siparişlerini otomatik serbest bırakma** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="c6d43-239">Go to **Warehouse management \> Release to warehouse \> Automatic release of sales orders**.</span></span>
1. <span data-ttu-id="c6d43-240">**Serbest bırakılacak miktar** alanını *Tümü* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c6d43-240">Set the **Quantity to release** field to *All*.</span></span>
1. <span data-ttu-id="c6d43-241">**Eklenecek kayıtlar** hızlı sekmesinde, sorgu iletişim kutusunu açmak için **Filtre**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c6d43-241">On the **Records to include** FastTab, select **Filter** to open the query dialog box.</span></span>
1. <span data-ttu-id="c6d43-242">Kılavuza aşağıdaki ayarlara sahip bir satır eklemek için **Aralık** sekmesinde **Ekle**'yi seçin:</span><span class="sxs-lookup"><span data-stu-id="c6d43-242">On the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="c6d43-243">**Tablo:** *Satış siparişi*</span><span class="sxs-lookup"><span data-stu-id="c6d43-243">**Table:** *Sales order*</span></span>
    - <span data-ttu-id="c6d43-244">**Türetilmiş tablo:** *Satış siparişi*</span><span class="sxs-lookup"><span data-stu-id="c6d43-244">**Derived table:** *Sales order*</span></span>
    - <span data-ttu-id="c6d43-245">**Alan:** *Satış siparişi*</span><span class="sxs-lookup"><span data-stu-id="c6d43-245">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="c6d43-246">**Ölçütler:** İstenen sipariş kümesinden satış siparişi numaralarının virgülle ayrılmış listesini girin.</span><span class="sxs-lookup"><span data-stu-id="c6d43-246">**Criteria:** Enter a comma-separated list of the sales order numbers from the desired order set.</span></span>

1. <span data-ttu-id="c6d43-247">Sorgunuzu kaydetmek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c6d43-247">Select **OK** to save your query.</span></span>
1. <span data-ttu-id="c6d43-248">*Otomatik ambara serbest bırakma* yordamını başlatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c6d43-248">Select **OK** to start the *Automatic release to warehouse* procedure.</span></span>

#### <a name="review-the-shipment-that-is-created-or-updated"></a><span data-ttu-id="c6d43-249">Oluşturulan veya güncelleştirilen sevkiyatı gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="c6d43-249">Review the shipment that is created or updated</span></span>

1. <span data-ttu-id="c6d43-250">**Ambar yönetimi \> Sevkiyatlar \> Tüm sevkiyatlar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="c6d43-250">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="c6d43-251">Gerekli sevkiyatı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="c6d43-251">Find and select the required shipment.</span></span>
1. <span data-ttu-id="c6d43-252">Sevkiyat oluşturulduğunda veya güncelleştirildiğinde bir konsolidasyon ilkesi kullanılmışsa bunu **Sevkiyat konsolidasyon ilkesi** alanında görmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="c6d43-252">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-sales-orders-from-order-set-1"></a><span data-ttu-id="c6d43-253">Sipariş kümesi 1'deki satış siparişlerini serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="c6d43-253">Release sales orders from order set 1</span></span>

<span data-ttu-id="c6d43-254">Sipariş kümesi 1'deki satış siparişlerini serbest bırakmak için [temel ambara serbest bırakma yordamını](#release-procedure) izleyin.</span><span class="sxs-lookup"><span data-stu-id="c6d43-254">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 1.</span></span>

<span data-ttu-id="c6d43-255">Bitirdiğinizde, iki sevkiyatın oluşturulduğunu görmelisiniz:</span><span class="sxs-lookup"><span data-stu-id="c6d43-255">When you've finished, you should see that two shipments were created:</span></span>

- <span data-ttu-id="c6d43-256">İlk sevkiyat üç satır içerir ve *CustomerMode* sevkiyat konsolidasyon ilkesi kullanılarak oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="c6d43-256">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="c6d43-257">Taşıma teslimat şekli için *Hava yolu* kullanmayan ikinci sevkiyat, *CustomerOrderNo* sevkiyat konsolidasyon ilkesi kullanılarak oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="c6d43-257">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-sales-orders-from-order-set-2"></a><span data-ttu-id="c6d43-258">Sipariş kümesi 2'deki satış siparişlerini serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="c6d43-258">Release sales orders from order set 2</span></span>

<span data-ttu-id="c6d43-259">Sipariş kümesi 2'deki satış siparişlerini serbest bırakmak için [temel ambara serbest bırakma yordamını](#release-procedure) izleyin.</span><span class="sxs-lookup"><span data-stu-id="c6d43-259">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 2.</span></span>

<span data-ttu-id="c6d43-260">Bitirdiğinizde, üç sevkiyatın oluşturulduğunu görmelisiniz:</span><span class="sxs-lookup"><span data-stu-id="c6d43-260">When you've finished, you should see that three shipments were created:</span></span>

- <span data-ttu-id="c6d43-261">İlk sevkiyat *Yanıcı* maddeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="c6d43-261">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="c6d43-262">Diğer iki sevkiyatın her biri, *Patlayıcı* madde içeren bir satır içerir.</span><span class="sxs-lookup"><span data-stu-id="c6d43-262">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-3"></a><span data-ttu-id="c6d43-263">Sipariş kümesi 3'teki satış siparişlerini serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="c6d43-263">Release sales orders from order set 3</span></span>

<span data-ttu-id="c6d43-264">Sipariş kümesi 3'teki satış siparişlerini serbest bırakmak için [temel ambara serbest bırakma yordamını](#release-procedure) izleyin.</span><span class="sxs-lookup"><span data-stu-id="c6d43-264">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 3.</span></span>

<span data-ttu-id="c6d43-265">Bitirdiğinizde, aşağıdaki eylemlerin gerçekleştiğini görmelisiniz:</span><span class="sxs-lookup"><span data-stu-id="c6d43-265">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="c6d43-266">Var olan bir sevkiyat (sipariş kümesi 2 ambara serbest bırakıldığında oluşturulan sevkiyat) güncelleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="c6d43-266">One existing shipment (the shipment that was created when order set 2 was released to the warehouse) was updated.</span></span> <span data-ttu-id="c6d43-267">*Yanıcı* maddeyi içeren bir satır eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="c6d43-267">A line that has the *Flammable* item was added.</span></span>
- <span data-ttu-id="c6d43-268">*Patlayıcı* maddeyi içeren yeni bir sevkiyat oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="c6d43-268">One new shipment was created that contains the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-4"></a><span data-ttu-id="c6d43-269">Sipariş kümesi 4'teki satış siparişlerini serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="c6d43-269">Release sales orders from order set 4</span></span>

<span data-ttu-id="c6d43-270">Sipariş kümesi 4'teki satış siparişlerini serbest bırakmak için [temel ambara serbest bırakma yordamını](#release-procedure) izleyin.</span><span class="sxs-lookup"><span data-stu-id="c6d43-270">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 4.</span></span>

<span data-ttu-id="c6d43-271">Bitirdiğinizde, var olan bir sevkiyatın (**Müşteri talebi** alanının *1* olarak ayarlandığı) güncelleştirilmiş olduğunu görmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="c6d43-271">When you've finished, you should see that one existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="c6d43-272">Buna yeni bir satır eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="c6d43-272">One new line was added to it.</span></span>

### <a name="release-sales-orders-from-order-set-5"></a><span data-ttu-id="c6d43-273">Sipariş kümesi 5'teki satış siparişlerini serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="c6d43-273">Release sales orders from order set 5</span></span>

<span data-ttu-id="c6d43-274">Sipariş kümesi 5'teki satış siparişlerini serbest bırakmak için [temel ambara serbest bırakma yordamını](#release-procedure) izleyin.</span><span class="sxs-lookup"><span data-stu-id="c6d43-274">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 5.</span></span>

<span data-ttu-id="c6d43-275">Bitirdiğinizde, aşağıdaki eylemlerin gerçekleştiğini görmelisiniz:</span><span class="sxs-lookup"><span data-stu-id="c6d43-275">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="c6d43-276">Var olan bir sevkiyat (**Müşteri talebi** alanı *1* olarak ayarlandığı) güncelleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="c6d43-276">One existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="c6d43-277">Satış siparişi 5-3'ten bir satır (**Müşteri talebi** alanının *1* olarak ayarlandığı) buna eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="c6d43-277">A line from sales order 5-3 (where the **Customer requisition** field is set to *1*) was added to it.</span></span>
- <span data-ttu-id="c6d43-278">Satış siparişi 5-1 ve 5-2'den satırların tek bir sevkiyat olarak gruplandırıldığı, yeni bir sevkiyat oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="c6d43-278">One new shipment was created, where lines from sales orders 5-1 and 5-2 are grouped into one shipment.</span></span>

### <a name="release-sales-orders-from-order-set-6"></a><span data-ttu-id="c6d43-279">Sipariş kümesi 6'daki satış siparişlerini serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="c6d43-279">Release sales orders from order set 6</span></span>

<span data-ttu-id="c6d43-280">Sipariş kümesi 6'daki satış siparişlerini serbest bırakmak için [temel ambara serbest bırakma yordamını](#release-procedure) izleyin.</span><span class="sxs-lookup"><span data-stu-id="c6d43-280">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 6.</span></span>

<span data-ttu-id="c6d43-281">Bitirdiğinizde, dört sevkiyatın oluşturulduğunu görmelisiniz:</span><span class="sxs-lookup"><span data-stu-id="c6d43-281">When you've finished, you should see that four shipments were created:</span></span>

- <span data-ttu-id="c6d43-282">Müşteri *US-003* ile ilgili iki siparişin satırları, *Sipariş havuzu* sevkiyat konsolidasyon ilkesi kullanılarak tek bir sevkiyatta gruplandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="c6d43-282">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="c6d43-283">Müşteri *US-004* ile ilgili iki siparişin satırları, *Sipariş havuzu* sevkiyat konsolidasyon ilkesi kullanılarak tek bir sevkiyatta gruplandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="c6d43-283">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="c6d43-284">Müşteri *US-007* ile ilgili satış siparişi 6-5 ve 6-6'daki satırlar, *Sipariş havuzu* sevkiyat konsolidasyon ilkesi kullanılarak tek bir sevkiyatta gruplandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="c6d43-284">Lines from sales orders 6-5 and 6-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="c6d43-285">Müşteri *US-007* ile ilgili satış siparişi 6-7 ve 6-8'deki satırlar, *CrossOrder* sevkiyat konsolidasyon ilkesi kullanılarak tek bir sevkiyatta gruplandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="c6d43-285">Lines from sales orders 6-7 and 6-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c6d43-286">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="c6d43-286">Additional resources</span></span>

- [<span data-ttu-id="c6d43-287">Sevkiyat konsolidasyonu ilkeleri</span><span class="sxs-lookup"><span data-stu-id="c6d43-287">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="c6d43-288">Sevkiyat konsolidasyon ilkelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="c6d43-288">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
