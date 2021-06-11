---
title: Satış siparişlerinin otomatik serbest bırakılması kullanılarak ambara serbest bırakıldıklarında sevkiyatları konsolide etme
description: Bu konu, çoklu siparişlerin aynı otomatik ambara serbest bırakma periyodik yordamında yer alarak ambara serbest bırakıldığı bir senaryo sunar.
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: c02c8b4cd43e17d6dcf34e1912dbc68c19e60694
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116963"
---
# <a name="consolidate-shipments-released-to-the-warehouse-using-automatic-release-of-sales-orders"></a><span data-ttu-id="49a10-103">Satış siparişlerinin otomatik serbest bırakılması kullanılarak ambara serbest bırakıldıklarında sevkiyatları konsolide etme</span><span class="sxs-lookup"><span data-stu-id="49a10-103">Consolidate shipments released to the warehouse using automatic release of sales orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="49a10-104">Bu konu, çoklu siparişlerin aynı otomatik ambara serbest bırakma periyodik yordamında yer alarak ambara serbest bırakıldığı bir senaryo sunar.</span><span class="sxs-lookup"><span data-stu-id="49a10-104">This topic presents a scenario where multiple orders are released to the warehouse in the same automated release-to-warehouse periodic procedure.</span></span> <span data-ttu-id="49a10-105">Siparişler, sevkiyat konsolidasyon ilkeleri olarak tanımlanan kurallara göre otomatik olarak sevkiyatlar halinde konsolide edilecektir.</span><span class="sxs-lookup"><span data-stu-id="49a10-105">The orders will automatically be consolidated into shipments, based on rules that are defined as shipment consolidation policies.</span></span>

<span data-ttu-id="49a10-106">Senaryo sırasında, satış siparişi kümeleri oluşturacak ve her kümeyi ambara serbest bırakacaksınız.</span><span class="sxs-lookup"><span data-stu-id="49a10-106">During the scenario, you will create sets of sales orders and release each set to the warehouse.</span></span> <span data-ttu-id="49a10-107">Böylece, yapılandırılan ilkelere göre, sevkiyat konsolidasyonu sırasında oluşturulan veya güncelleştirilen sevkiyatları gözden geçireceksiniz.</span><span class="sxs-lookup"><span data-stu-id="49a10-107">You will then review the shipments that are created or updated during shipment consolidation, based on the configured policies.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="49a10-108">Tanıtım verilerini kullanılabilir hale getirme</span><span class="sxs-lookup"><span data-stu-id="49a10-108">Make demo data available</span></span>

<span data-ttu-id="49a10-109">Bu konudaki senaryo, Microsoft Dynamics 365 Supply Chain Management için sağlanan standart tanıtım verilerinde bulunan değerlere ve kayıtlara başvurur.</span><span class="sxs-lookup"><span data-stu-id="49a10-109">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="49a10-110">Alıştırmaları yaparken burada sağlanan değerleri kullanmak isterseniz tanıtım verisinin yüklü olduğu bir ortamda çalıştığınızdan ve başlamadan önce tüzel kişiliği **USMF** olarak ayarladığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="49a10-110">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="49a10-111">Sevkiyat konsolidasyon ilkelerini ve ürün filtrelerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="49a10-111">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="49a10-112">Burada açıklanan senaryo, özelliği önceden açtığınız, [Sevkiyat konsolidasyonu ilkelerini yapılandırma](configure-shipment-consolidation-policies.md) alıştırmalarını yaptığınız ve burada açıklanan ilkeleri ve diğer kayıtları oluşturduğunuz varsayımına dayanır.</span><span class="sxs-lookup"><span data-stu-id="49a10-112">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="49a10-113">Bu senaryoya devam etmeden önce söz konusu alıştırmaları yaptığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="49a10-113">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="49a10-114">Bu senaryo için satış siparişleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="49a10-114">Create the sales orders for this scenario</span></span>

<span data-ttu-id="49a10-115">Çalışabileceğiniz bir satış siparişleri koleksiyonu oluşturarak başlayın.</span><span class="sxs-lookup"><span data-stu-id="49a10-115">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="49a10-116">Gelişmiş ambar (WMS) işlemleri için etkinleştirilen bir ambarla çalışmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="49a10-116">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="49a10-117">Başka bir ambar açıkça belirtilmedikçe, aşağıdaki sipariş kümelerinin her biri için aynı ambar kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="49a10-117">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="49a10-118">**Alacak hesapları \> Siparişler \> Tüm satış siparişleri** öğesine gidin ve aşağıdaki alt bölümlerde açıklanan ayarlara sahip bir satış siparişleri koleksiyonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="49a10-118">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="49a10-119">Sipariş kümesi 1'i oluşturma</span><span class="sxs-lookup"><span data-stu-id="49a10-119">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="49a10-120">Satış siparişi 1-1</span><span class="sxs-lookup"><span data-stu-id="49a10-120">Sales order 1-1</span></span>

1. <span data-ttu-id="49a10-121">Aşağıdaki ayarlara sahip bir satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="49a10-121">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="49a10-122">**Müşteri hesabı:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="49a10-122">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="49a10-123">**Teslimat şekli:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="49a10-123">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="49a10-124">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="49a10-124">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="49a10-125">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="49a10-125">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="49a10-126">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="49a10-126">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="49a10-127">Satış siparişi 1-2</span><span class="sxs-lookup"><span data-stu-id="49a10-127">Sales order 1-2</span></span>

1. <span data-ttu-id="49a10-128">Aşağıdaki ayarlara sahip bir satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="49a10-128">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="49a10-129">**Müşteri hesabı:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="49a10-129">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="49a10-130">**Teslimat şekli:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="49a10-130">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="49a10-131">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="49a10-131">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="49a10-132">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="49a10-132">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="49a10-133">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="49a10-133">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="49a10-134">Satış siparişi 1-3</span><span class="sxs-lookup"><span data-stu-id="49a10-134">Sales order 1-3</span></span>

1. <span data-ttu-id="49a10-135">Aşağıdaki ayarlara sahip bir satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="49a10-135">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="49a10-136">**Müşteri hesabı:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="49a10-136">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="49a10-137">**Teslimat şekli:** *10*</span><span class="sxs-lookup"><span data-stu-id="49a10-137">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="49a10-138">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="49a10-138">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="49a10-139">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="49a10-139">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="49a10-140">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="49a10-140">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="49a10-141">Aşağıdaki ayarlara sahip ikinci bir satış siparişi satırı oluşturun:</span><span class="sxs-lookup"><span data-stu-id="49a10-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="49a10-142">**Madde numarası:** *A0002* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="49a10-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="49a10-143">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="49a10-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="49a10-144">**Teslimat şekli:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="49a10-144">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="49a10-145">Sipariş kümesi 2'yi oluşturma</span><span class="sxs-lookup"><span data-stu-id="49a10-145">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="49a10-146">Satış siparişleri 2-1 ve 2-2</span><span class="sxs-lookup"><span data-stu-id="49a10-146">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="49a10-147">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="49a10-147">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="49a10-148">**Müşteri hesabı:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="49a10-148">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="49a10-149">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="49a10-149">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="49a10-150">**Madde numarası:** *M9200* (**Kod 4** filtresinin *Yanıcı* değerine ayarlandığı bir madde)</span><span class="sxs-lookup"><span data-stu-id="49a10-150">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="49a10-151">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="49a10-151">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="49a10-152">Aşağıdaki ayarlara sahip ikinci bir satış siparişi satırı oluşturun:</span><span class="sxs-lookup"><span data-stu-id="49a10-152">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="49a10-153">**Madde numarası:** *M9201* (**Kod 4** filtresinin *Patlayıcı* değerine ayarlandığı bir madde)</span><span class="sxs-lookup"><span data-stu-id="49a10-153">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="49a10-154">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="49a10-154">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="49a10-155">**Teslimat şekli:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="49a10-155">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="49a10-156">Sipariş kümesi 3'ü oluşturma</span><span class="sxs-lookup"><span data-stu-id="49a10-156">Create order set 3</span></span>

#### <a name="sales-order-3-1"></a><span data-ttu-id="49a10-157">Satış siparişi 3-1</span><span class="sxs-lookup"><span data-stu-id="49a10-157">Sales order 3-1</span></span>

1. <span data-ttu-id="49a10-158">Aşağıdaki ayarlara sahip bir satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="49a10-158">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="49a10-159">**Müşteri hesabı:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="49a10-159">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="49a10-160">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="49a10-160">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="49a10-161">**Madde numarası:** *M9200* (**Kod 4** filtresinin *Yanıcı* değerine ayarlandığı bir madde)</span><span class="sxs-lookup"><span data-stu-id="49a10-161">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="49a10-162">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="49a10-162">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="49a10-163">Aşağıdaki ayarlara sahip ikinci bir satış siparişi satırı oluşturun:</span><span class="sxs-lookup"><span data-stu-id="49a10-163">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="49a10-164">**Madde numarası:** *M9201* (**Kod 4** filtresinin *Patlayıcı* değerine ayarlandığı bir madde)</span><span class="sxs-lookup"><span data-stu-id="49a10-164">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="49a10-165">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="49a10-165">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="49a10-166">**Teslimat şekli:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="49a10-166">**Mode of delivery:** *Airwa-Air*</span></span>

> [!NOTE]
> <span data-ttu-id="49a10-167">Bu sipariş, sipariş kümesi 2 için oluşturduğunuz iki siparişle aynıdır.</span><span class="sxs-lookup"><span data-stu-id="49a10-167">This order is identical to the two orders that you created for order set 2.</span></span> <span data-ttu-id="49a10-168">Ancak, bu senaryoda daha sonra ayrı olarak serbest bırakacağınız için kendi sipariş kümesi olarak listelenir.</span><span class="sxs-lookup"><span data-stu-id="49a10-168">However, it's listed as its own order set because you will release it separately later in this scenario.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="49a10-169">Sipariş kümesi 4'ü oluşturma</span><span class="sxs-lookup"><span data-stu-id="49a10-169">Create order set 4</span></span>

#### <a name="sales-order-4-1"></a><span data-ttu-id="49a10-170">Satış siparişi 4-1</span><span class="sxs-lookup"><span data-stu-id="49a10-170">Sales order 4-1</span></span>

1. <span data-ttu-id="49a10-171">Aşağıdaki ayarlara sahip bir satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="49a10-171">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="49a10-172">**Müşteri hesabı:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="49a10-172">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="49a10-173">**Müşteri talebi:** *1*</span><span class="sxs-lookup"><span data-stu-id="49a10-173">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="49a10-174">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="49a10-174">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="49a10-175">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="49a10-175">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="49a10-176">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="49a10-176">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-5"></a><span data-ttu-id="49a10-177">Sipariş kümesi 5'yi oluşturma</span><span class="sxs-lookup"><span data-stu-id="49a10-177">Create order set 5</span></span>

#### <a name="sales-orders-5-1-and-5-2"></a><span data-ttu-id="49a10-178">Satış siparişleri 5-1 ve 5-2</span><span class="sxs-lookup"><span data-stu-id="49a10-178">Sales orders 5-1 and 5-2</span></span>

1. <span data-ttu-id="49a10-179">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="49a10-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="49a10-180">**Müşteri hesabı:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="49a10-180">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="49a10-181">**Müşteri talebi:** *2*</span><span class="sxs-lookup"><span data-stu-id="49a10-181">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="49a10-182">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="49a10-182">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="49a10-183">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="49a10-183">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="49a10-184">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="49a10-184">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-5-3"></a><span data-ttu-id="49a10-185">Satış siparişi 5-3</span><span class="sxs-lookup"><span data-stu-id="49a10-185">Sales order 5-3</span></span>

1. <span data-ttu-id="49a10-186">Aşağıdaki ayarlara sahip bir satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="49a10-186">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="49a10-187">**Müşteri hesabı:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="49a10-187">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="49a10-188">**Müşteri talebi:** *1*</span><span class="sxs-lookup"><span data-stu-id="49a10-188">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="49a10-189">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="49a10-189">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="49a10-190">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="49a10-190">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="49a10-191">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="49a10-191">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-6"></a><span data-ttu-id="49a10-192">Sipariş kümesi 6'yi oluşturma</span><span class="sxs-lookup"><span data-stu-id="49a10-192">Create order set 6</span></span>

#### <a name="sales-orders-6-1-and-6-2"></a><span data-ttu-id="49a10-193">Satış siparişleri 6-1 ve 6-2</span><span class="sxs-lookup"><span data-stu-id="49a10-193">Sales orders 6-1 and 6-2</span></span>

1. <span data-ttu-id="49a10-194">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="49a10-194">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="49a10-195">**Müşteri hesabı:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="49a10-195">**Customer account:** *US-003*</span></span>
    - <span data-ttu-id="49a10-196">**Müşteri talebi:** *2*</span><span class="sxs-lookup"><span data-stu-id="49a10-196">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="49a10-197">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="49a10-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="49a10-198">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="49a10-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="49a10-199">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="49a10-199">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-3-and-6-4"></a><span data-ttu-id="49a10-200">Satış siparişleri 6-3 ve 6-4</span><span class="sxs-lookup"><span data-stu-id="49a10-200">Sales orders 6-3 and 6-4</span></span>

1. <span data-ttu-id="49a10-201">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="49a10-201">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="49a10-202">**Müşteri hesabı:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="49a10-202">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="49a10-203">**Müşteri talebi:** *1*</span><span class="sxs-lookup"><span data-stu-id="49a10-203">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="49a10-204">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="49a10-204">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="49a10-205">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="49a10-205">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="49a10-206">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="49a10-206">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-5-and-6-6"></a><span data-ttu-id="49a10-207">Satış siparişleri 6-5 ve 6-6</span><span class="sxs-lookup"><span data-stu-id="49a10-207">Sales orders 6-5 and 6-6</span></span>

1. <span data-ttu-id="49a10-208">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="49a10-208">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="49a10-209">**Müşteri hesabı:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="49a10-209">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="49a10-210">**Tesis:** *6*</span><span class="sxs-lookup"><span data-stu-id="49a10-210">**Site:** *6*</span></span>
    - <span data-ttu-id="49a10-211">**Ambar:** *61*</span><span class="sxs-lookup"><span data-stu-id="49a10-211">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="49a10-212">**Havuz:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="49a10-212">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="49a10-213">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="49a10-213">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="49a10-214">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="49a10-214">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="49a10-215">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="49a10-215">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-7-and-6-8"></a><span data-ttu-id="49a10-216">Satış siparişleri 6-7 ve 6-8</span><span class="sxs-lookup"><span data-stu-id="49a10-216">Sales orders 6-7 and 6-8</span></span>

1. <span data-ttu-id="49a10-217">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="49a10-217">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="49a10-218">**Müşteri hesabı:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="49a10-218">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="49a10-219">**Tesis:** *6*</span><span class="sxs-lookup"><span data-stu-id="49a10-219">**Site:** *6*</span></span>
    - <span data-ttu-id="49a10-220">**Ambar:** *61*</span><span class="sxs-lookup"><span data-stu-id="49a10-220">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="49a10-221">**Havuz:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="49a10-221">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="49a10-222">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="49a10-222">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="49a10-223">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="49a10-223">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="49a10-224">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="49a10-224">**Quantity:** *1.00*</span></span>

## <a name="automatic-release-of-sales-orders-to-the-warehouse"></a><span data-ttu-id="49a10-225">Satış siparişlerini ambara otomatik olarak serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="49a10-225">Automatic release of sales orders to the warehouse</span></span>

<span data-ttu-id="49a10-226">Daha önce oluşturduğunuz her satış siparişi kümesi için ambara otomatik olarak serbest bırakma yordamını tamamlayacaksınız.</span><span class="sxs-lookup"><span data-stu-id="49a10-226">For each set of sales orders that you created earlier, you will complete a procedure for automatic release to the warehouse.</span></span> <span data-ttu-id="49a10-227">Her örnekte, burada sağlanan [temel ambara serbest bırakma yordamı](#release-procedure) üzerinden çalışacaksınız.</span><span class="sxs-lookup"><span data-stu-id="49a10-227">In each case, you will work through the [basic release-to-warehouse procedure](#release-procedure) that is provided here.</span></span>

### <a name="basic-release-to-warehouse-procedure"></a><a name="release-procedure"></a><span data-ttu-id="49a10-228">Temel ambara serbest bırakma yordamı</span><span class="sxs-lookup"><span data-stu-id="49a10-228">Basic release-to-warehouse procedure</span></span>

<span data-ttu-id="49a10-229">Daha önce oluşturduğunuz her satış siparişi kümesi için aşağıdaki alt bölümlerde özetlenen üç yordamı tamamlayacaksınız.</span><span class="sxs-lookup"><span data-stu-id="49a10-229">For each set of sales orders that you created earlier, you will complete the three procedures that are outlined in the following subsections.</span></span>

#### <a name="update-the-wave-template-that-will-be-used-during-release"></a><span data-ttu-id="49a10-230">Serbest bırakma sırasında kullanılacak dalga şablonunu güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="49a10-230">Update the wave template that will be used during release</span></span>

1. <span data-ttu-id="49a10-231">**Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga şablonları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="49a10-231">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="49a10-232">**Dalga şablonu türü** alanını *Sevkiyat* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="49a10-232">Set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="49a10-233">Bu senaryo için oluşturduğunuz sipariş kümelerinde kullandığınız ambarla ilişkilendirilmiş dalga şablonunu bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="49a10-233">Find and select the wave template that is associated with the warehouse that you used in the order sets that you created for this scenario.</span></span> <span data-ttu-id="49a10-234">Örneğin, ambar *24*'ü kullandıysanız **24 Sevkiyat Varsayılan** dalga şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="49a10-234">For example, if you used warehouse *24*, select the **24 Shipping Default** wave template.</span></span> <span data-ttu-id="49a10-235">Ambar *61*'i kullandıysanız **61 Sevkiyat** dalga şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="49a10-235">If you used warehouse *61*, select the **61 Shipping** wave template.</span></span>
1. <span data-ttu-id="49a10-236">Eylem Bölmesi'nde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="49a10-236">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="49a10-237">**Dalgayı ambara serbest bırakma sırasında işle** seçeneğini *Hayır* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="49a10-237">Set the **Process wave at release to warehouse** option to *No*.</span></span>

#### <a name="release-to-the-warehouse"></a><span data-ttu-id="49a10-238">Ambara serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="49a10-238">Release to the warehouse</span></span>

1. <span data-ttu-id="49a10-239">**Ambar yönetimi \> Ambara serbest bırakma \> Satış siparişlerini otomatik serbest bırakma** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="49a10-239">Go to **Warehouse management \> Release to warehouse \> Automatic release of sales orders**.</span></span>
1. <span data-ttu-id="49a10-240">**Serbest bırakılacak miktar** alanını *Tümü* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="49a10-240">Set the **Quantity to release** field to *All*.</span></span>
1. <span data-ttu-id="49a10-241">**Eklenecek kayıtlar** hızlı sekmesinde, sorgu iletişim kutusunu açmak için **Filtre**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="49a10-241">On the **Records to include** FastTab, select **Filter** to open the query dialog box.</span></span>
1. <span data-ttu-id="49a10-242">Kılavuza aşağıdaki ayarlara sahip bir satır eklemek için **Aralık** sekmesinde **Ekle**'yi seçin:</span><span class="sxs-lookup"><span data-stu-id="49a10-242">On the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="49a10-243">**Tablo:** *Satış siparişi*</span><span class="sxs-lookup"><span data-stu-id="49a10-243">**Table:** *Sales order*</span></span>
    - <span data-ttu-id="49a10-244">**Türetilmiş tablo:** *Satış siparişi*</span><span class="sxs-lookup"><span data-stu-id="49a10-244">**Derived table:** *Sales order*</span></span>
    - <span data-ttu-id="49a10-245">**Alan:** *Satış siparişi*</span><span class="sxs-lookup"><span data-stu-id="49a10-245">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="49a10-246">**Ölçütler:** İstenen sipariş kümesinden satış siparişi numaralarının virgülle ayrılmış listesini girin.</span><span class="sxs-lookup"><span data-stu-id="49a10-246">**Criteria:** Enter a comma-separated list of the sales order numbers from the desired order set.</span></span>

1. <span data-ttu-id="49a10-247">Sorgunuzu kaydetmek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="49a10-247">Select **OK** to save your query.</span></span>
1. <span data-ttu-id="49a10-248">*Otomatik ambara serbest bırakma* yordamını başlatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="49a10-248">Select **OK** to start the *Automatic release to warehouse* procedure.</span></span>

#### <a name="review-the-shipment-that-is-created-or-updated"></a><span data-ttu-id="49a10-249">Oluşturulan veya güncelleştirilen sevkiyatı gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="49a10-249">Review the shipment that is created or updated</span></span>

1. <span data-ttu-id="49a10-250">**Ambar yönetimi \> Sevkiyatlar \> Tüm sevkiyatlar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="49a10-250">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="49a10-251">Gerekli sevkiyatı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="49a10-251">Find and select the required shipment.</span></span>
1. <span data-ttu-id="49a10-252">Sevkiyat oluşturulduğunda veya güncelleştirildiğinde bir konsolidasyon ilkesi kullanılmışsa bunu **Sevkiyat konsolidasyon ilkesi** alanında görmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="49a10-252">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-sales-orders-from-order-set-1"></a><span data-ttu-id="49a10-253">Sipariş kümesi 1'deki satış siparişlerini serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="49a10-253">Release sales orders from order set 1</span></span>

<span data-ttu-id="49a10-254">Sipariş kümesi 1'deki satış siparişlerini serbest bırakmak için [temel ambara serbest bırakma yordamını](#release-procedure) izleyin.</span><span class="sxs-lookup"><span data-stu-id="49a10-254">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 1.</span></span>

<span data-ttu-id="49a10-255">Bitirdiğinizde, iki sevkiyatın oluşturulduğunu görmelisiniz:</span><span class="sxs-lookup"><span data-stu-id="49a10-255">When you've finished, you should see that two shipments were created:</span></span>

- <span data-ttu-id="49a10-256">İlk sevkiyat üç satır içerir ve *CustomerMode* sevkiyat konsolidasyon ilkesi kullanılarak oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="49a10-256">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="49a10-257">Taşıma teslimat şekli için *Hava yolu* kullanmayan ikinci sevkiyat, *CustomerOrderNo* sevkiyat konsolidasyon ilkesi kullanılarak oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="49a10-257">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-sales-orders-from-order-set-2"></a><span data-ttu-id="49a10-258">Sipariş kümesi 2'deki satış siparişlerini serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="49a10-258">Release sales orders from order set 2</span></span>

<span data-ttu-id="49a10-259">Sipariş kümesi 2'deki satış siparişlerini serbest bırakmak için [temel ambara serbest bırakma yordamını](#release-procedure) izleyin.</span><span class="sxs-lookup"><span data-stu-id="49a10-259">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 2.</span></span>

<span data-ttu-id="49a10-260">Bitirdiğinizde, üç sevkiyatın oluşturulduğunu görmelisiniz:</span><span class="sxs-lookup"><span data-stu-id="49a10-260">When you've finished, you should see that three shipments were created:</span></span>

- <span data-ttu-id="49a10-261">İlk sevkiyat *Yanıcı* maddeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="49a10-261">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="49a10-262">Diğer iki sevkiyatın her biri, *Patlayıcı* madde içeren bir satır içerir.</span><span class="sxs-lookup"><span data-stu-id="49a10-262">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-3"></a><span data-ttu-id="49a10-263">Sipariş kümesi 3'teki satış siparişlerini serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="49a10-263">Release sales orders from order set 3</span></span>

<span data-ttu-id="49a10-264">Sipariş kümesi 3'teki satış siparişlerini serbest bırakmak için [temel ambara serbest bırakma yordamını](#release-procedure) izleyin.</span><span class="sxs-lookup"><span data-stu-id="49a10-264">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 3.</span></span>

<span data-ttu-id="49a10-265">Bitirdiğinizde, aşağıdaki eylemlerin gerçekleştiğini görmelisiniz:</span><span class="sxs-lookup"><span data-stu-id="49a10-265">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="49a10-266">Var olan bir sevkiyat (sipariş kümesi 2 ambara serbest bırakıldığında oluşturulan sevkiyat) güncelleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="49a10-266">One existing shipment (the shipment that was created when order set 2 was released to the warehouse) was updated.</span></span> <span data-ttu-id="49a10-267">*Yanıcı* maddeyi içeren bir satır eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="49a10-267">A line that has the *Flammable* item was added.</span></span>
- <span data-ttu-id="49a10-268">*Patlayıcı* maddeyi içeren yeni bir sevkiyat oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="49a10-268">One new shipment was created that contains the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-4"></a><span data-ttu-id="49a10-269">Sipariş kümesi 4'teki satış siparişlerini serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="49a10-269">Release sales orders from order set 4</span></span>

<span data-ttu-id="49a10-270">Sipariş kümesi 4'teki satış siparişlerini serbest bırakmak için [temel ambara serbest bırakma yordamını](#release-procedure) izleyin.</span><span class="sxs-lookup"><span data-stu-id="49a10-270">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 4.</span></span>

<span data-ttu-id="49a10-271">Bitirdiğinizde, var olan bir sevkiyatın (**Müşteri talebi** alanının *1* olarak ayarlandığı) güncelleştirilmiş olduğunu görmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="49a10-271">When you've finished, you should see that one existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="49a10-272">Buna yeni bir satır eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="49a10-272">One new line was added to it.</span></span>

### <a name="release-sales-orders-from-order-set-5"></a><span data-ttu-id="49a10-273">Sipariş kümesi 5'teki satış siparişlerini serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="49a10-273">Release sales orders from order set 5</span></span>

<span data-ttu-id="49a10-274">Sipariş kümesi 5'teki satış siparişlerini serbest bırakmak için [temel ambara serbest bırakma yordamını](#release-procedure) izleyin.</span><span class="sxs-lookup"><span data-stu-id="49a10-274">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 5.</span></span>

<span data-ttu-id="49a10-275">Bitirdiğinizde, aşağıdaki eylemlerin gerçekleştiğini görmelisiniz:</span><span class="sxs-lookup"><span data-stu-id="49a10-275">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="49a10-276">Var olan bir sevkiyat (**Müşteri talebi** alanı *1* olarak ayarlandığı) güncelleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="49a10-276">One existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="49a10-277">Satış siparişi 5-3'ten bir satır (**Müşteri talebi** alanının *1* olarak ayarlandığı) buna eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="49a10-277">A line from sales order 5-3 (where the **Customer requisition** field is set to *1*) was added to it.</span></span>
- <span data-ttu-id="49a10-278">Satış siparişi 5-1 ve 5-2'den satırların tek bir sevkiyat olarak gruplandırıldığı, yeni bir sevkiyat oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="49a10-278">One new shipment was created, where lines from sales orders 5-1 and 5-2 are grouped into one shipment.</span></span>

### <a name="release-sales-orders-from-order-set-6"></a><span data-ttu-id="49a10-279">Sipariş kümesi 6'daki satış siparişlerini serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="49a10-279">Release sales orders from order set 6</span></span>

<span data-ttu-id="49a10-280">Sipariş kümesi 6'daki satış siparişlerini serbest bırakmak için [temel ambara serbest bırakma yordamını](#release-procedure) izleyin.</span><span class="sxs-lookup"><span data-stu-id="49a10-280">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 6.</span></span>

<span data-ttu-id="49a10-281">Bitirdiğinizde, dört sevkiyatın oluşturulduğunu görmelisiniz:</span><span class="sxs-lookup"><span data-stu-id="49a10-281">When you've finished, you should see that four shipments were created:</span></span>

- <span data-ttu-id="49a10-282">Müşteri *US-003* ile ilgili iki siparişin satırları, *Sipariş havuzu* sevkiyat konsolidasyon ilkesi kullanılarak tek bir sevkiyatta gruplandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="49a10-282">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="49a10-283">Müşteri *US-004* ile ilgili iki siparişin satırları, *Sipariş havuzu* sevkiyat konsolidasyon ilkesi kullanılarak tek bir sevkiyatta gruplandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="49a10-283">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="49a10-284">Müşteri *US-007* ile ilgili satış siparişi 6-5 ve 6-6'daki satırlar, *Sipariş havuzu* sevkiyat konsolidasyon ilkesi kullanılarak tek bir sevkiyatta gruplandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="49a10-284">Lines from sales orders 6-5 and 6-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="49a10-285">Müşteri *US-007* ile ilgili satış siparişi 6-7 ve 6-8'deki satırlar, *CrossOrder* sevkiyat konsolidasyon ilkesi kullanılarak tek bir sevkiyatta gruplandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="49a10-285">Lines from sales orders 6-7 and 6-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="49a10-286">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="49a10-286">Additional resources</span></span>

- [<span data-ttu-id="49a10-287">Sevkiyat konsolidasyonu ilkeleri</span><span class="sxs-lookup"><span data-stu-id="49a10-287">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="49a10-288">Sevkiyat konsolidasyon ilkelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="49a10-288">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]