---
title: Sevkiyat konsolidasyonu çalışma ekranı kullanılarak sevkiyatları konsolide etme
description: Bu konu, çoklu siparişlerin aynı yükte yer alarak ambara serbest bırakıldığı ve ardından, sevkiyat konsolidasyon çalışma ekranı kullanılarak sevkiyatlar halinde konsolide edildiği bir senaryo sunar.
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-olbara
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: b1a2c9506b4444fc98a9e4f0389cbd69db4ce052
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383881"
---
# <a name="consolidate-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="7a2fb-103">Sevkiyat konsolidasyonu çalışma ekranı kullanılarak sevkiyatları konsolide etme</span><span class="sxs-lookup"><span data-stu-id="7a2fb-103">Consolidate shipments by using the shipment consolidation workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a2fb-104">Bu konu, çoklu siparişlerin aynı yükte yer alarak ambara serbest bırakıldığı ve ardından, sevkiyat konsolidasyon çalışma ekranı kullanılarak sevkiyatlar halinde konsolide edildiği bir senaryo sunar.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated into shipments later by using the shipment consolidation workbench.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="7a2fb-105">Tanıtım verilerini kullanılabilir hale getirme</span><span class="sxs-lookup"><span data-stu-id="7a2fb-105">Make demo data available</span></span>

<span data-ttu-id="7a2fb-106">Bu konudaki senaryo, Microsoft Dynamics 365 Supply Chain Management için sağlanan standart tanıtım verilerinde bulunan değerlere ve kayıtlara başvurur.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="7a2fb-107">Alıştırmaları yaparken burada sağlanan değerleri kullanmak isterseniz tanıtım verisinin yüklü olduğu bir ortamda çalıştığınızdan ve başlamadan önce tüzel kişiliği **USMF** olarak ayarladığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="7a2fb-108">Sevkiyat konsolidasyon ilkelerini ve ürün filtrelerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="7a2fb-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="7a2fb-109">Burada açıklanan senaryo, özelliği önceden açtığınız, [Sevkiyat konsolidasyonu ilkelerini yapılandırma](configure-shipment-consolidation-policies.md) alıştırmalarını yaptığınız ve burada açıklanan ilkeleri ve diğer kayıtları oluşturduğunuz varsayımına dayanır.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="7a2fb-110">Bu senaryoya devam etmeden önce söz konusu alıştırmaları yaptığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="turn-on-the-manual-shipment-consolidation-feature"></a><span data-ttu-id="7a2fb-111">Manuel sevkiyat konsolidasyon özelliğini açma</span><span class="sxs-lookup"><span data-stu-id="7a2fb-111">Turn on the manual shipment consolidation feature</span></span>

<span data-ttu-id="7a2fb-112">*Manuel sevkiyat konsolidasyon* özelliğini kullanabilmeniz için önce sisteminizde bu özelliği açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-112">Before you can use the *Manual shipment consolidation* feature, you must turn it on in your system.</span></span> <span data-ttu-id="7a2fb-113">Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="7a2fb-114">**Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:</span><span class="sxs-lookup"><span data-stu-id="7a2fb-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="7a2fb-115">**Modül:** *Ambar yönetimi*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="7a2fb-116">**Özellik adı:** *Manuel sevkiyat konsolidasyonu*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-116">**Feature name:** *Manual shipment consolidation*</span></span>

<span data-ttu-id="7a2fb-117">[Sevkiyat konsolidasyon ilkelerini yapılandırma](configure-shipment-consolidation-policies.md) konusunda bahsedildiği gibi ilkeleri oluşturabilmeniz için önce *Sevkiyatı konsolide et* özelliğini de etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-117">As was mentioned in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), you must also turn on the *Consolidate shipment* feature before you can create policies.</span></span> <span data-ttu-id="7a2fb-118">Ancak, o adımı zaten tamamlamış olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-118">However, you should already have completed that step.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="7a2fb-119">Bu senaryo için satış siparişleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="7a2fb-119">Create the sales orders for this scenario</span></span>

<span data-ttu-id="7a2fb-120">Çalışabileceğiniz bir satış siparişleri koleksiyonu oluşturarak başlayın.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-120">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="7a2fb-121">Gelişmiş ambar (WMS) işlemleri için etkinleştirilen bir ambarla çalışmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-121">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="7a2fb-122">Başka bir ambar açıkça belirtilmedikçe, aşağıdaki sipariş kümelerinin her biri için aynı ambar kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-122">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="7a2fb-123">**Alacak hesapları \> Siparişler \> Tüm satış siparişleri** öğesine gidin ve aşağıdaki alt bölümlerde açıklanan ayarlara sahip bir satış siparişleri koleksiyonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-123">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="7a2fb-124">Sipariş kümesi 1'i oluşturma</span><span class="sxs-lookup"><span data-stu-id="7a2fb-124">Create order set 1</span></span>

#### <a name="sales-orders-1-1-and-1-2"></a><span data-ttu-id="7a2fb-125">Satış siparişleri 1-1 ve 1-2</span><span class="sxs-lookup"><span data-stu-id="7a2fb-125">Sales orders 1-1 and 1-2</span></span>

1. <span data-ttu-id="7a2fb-126">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="7a2fb-126">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="7a2fb-127">**Müşteri hesabı:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="7a2fb-128">**Teslimat şekli:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="7a2fb-129">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="7a2fb-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="7a2fb-130">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="7a2fb-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="7a2fb-131">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="7a2fb-132">**Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="7a2fb-133">Satış siparişi 1-3</span><span class="sxs-lookup"><span data-stu-id="7a2fb-133">Sales order 1-3</span></span>

1. <span data-ttu-id="7a2fb-134">Aşağıdaki ayarlara sahip bir satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="7a2fb-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="7a2fb-135">**Müşteri hesabı:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="7a2fb-136">**Teslimat şekli:** *10*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="7a2fb-137">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="7a2fb-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="7a2fb-138">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="7a2fb-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="7a2fb-139">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="7a2fb-140">**Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="7a2fb-141">Aşağıdaki ayarlara sahip ikinci bir satış siparişi satırı oluşturun:</span><span class="sxs-lookup"><span data-stu-id="7a2fb-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="7a2fb-142">**Madde numarası:** *A0002* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="7a2fb-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="7a2fb-143">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="7a2fb-144">**Teslimat şekli:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="7a2fb-145">**Stok \> Rezervasyon**'u ve sonra Eylem Bölmesi'nde, ikinci sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="7a2fb-146">Sipariş kümesi 2'yi oluşturma</span><span class="sxs-lookup"><span data-stu-id="7a2fb-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="7a2fb-147">Satış siparişleri 2-1 ve 2-2</span><span class="sxs-lookup"><span data-stu-id="7a2fb-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="7a2fb-148">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="7a2fb-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="7a2fb-149">**Müşteri hesabı:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-149">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="7a2fb-150">**Teslimat şekli:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-150">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="7a2fb-151">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="7a2fb-151">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="7a2fb-152">**Madde numarası:** *M9200* (**Kod 4** filtresinin *Yanıcı* değerine ayarlandığı bir madde)</span><span class="sxs-lookup"><span data-stu-id="7a2fb-152">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="7a2fb-153">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-153">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="7a2fb-154">**Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-154">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="7a2fb-155">Aşağıdaki ayarlara sahip ikinci bir satış siparişi satırı oluşturun:</span><span class="sxs-lookup"><span data-stu-id="7a2fb-155">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="7a2fb-156">**Madde numarası:** *M9201* (**Kod 4** filtresinin *Patlayıcı* değerine ayarlandığı bir madde)</span><span class="sxs-lookup"><span data-stu-id="7a2fb-156">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="7a2fb-157">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-157">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="7a2fb-158">**Teslimat şekli:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-158">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="7a2fb-159">**Stok \> Rezervasyon**'u ve sonra Eylem Bölmesi'nde, ikinci sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-159">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="7a2fb-160">Sipariş kümesi 3'ü oluşturma</span><span class="sxs-lookup"><span data-stu-id="7a2fb-160">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="7a2fb-161">Satış siparişleri 3-1 ve 3-2</span><span class="sxs-lookup"><span data-stu-id="7a2fb-161">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="7a2fb-162">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="7a2fb-162">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="7a2fb-163">**Müşteri hesabı:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-163">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="7a2fb-164">**Müşteri talebi:** *1*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-164">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="7a2fb-165">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="7a2fb-165">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="7a2fb-166">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="7a2fb-166">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="7a2fb-167">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-167">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="7a2fb-168">**Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-168">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="7a2fb-169">Satış siparişleri 3-3 ve 3-4</span><span class="sxs-lookup"><span data-stu-id="7a2fb-169">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="7a2fb-170">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="7a2fb-170">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="7a2fb-171">**Müşteri hesabı:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-171">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="7a2fb-172">**Müşteri talebi:** *2*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-172">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="7a2fb-173">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="7a2fb-173">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="7a2fb-174">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="7a2fb-174">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="7a2fb-175">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-175">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="7a2fb-176">**Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-176">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="7a2fb-177">Sipariş kümesi 4'ü oluşturma</span><span class="sxs-lookup"><span data-stu-id="7a2fb-177">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="7a2fb-178">Satış siparişleri 4-1 ve 4-2</span><span class="sxs-lookup"><span data-stu-id="7a2fb-178">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="7a2fb-179">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="7a2fb-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="7a2fb-180">**Müşteri hesabı:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-180">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="7a2fb-181">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="7a2fb-181">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="7a2fb-182">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="7a2fb-182">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="7a2fb-183">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-183">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="7a2fb-184">**Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-184">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="7a2fb-185">Satış siparişleri 4-3 ve 4-4</span><span class="sxs-lookup"><span data-stu-id="7a2fb-185">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="7a2fb-186">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="7a2fb-186">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="7a2fb-187">**Müşteri hesabı:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-187">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="7a2fb-188">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="7a2fb-188">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="7a2fb-189">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="7a2fb-189">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="7a2fb-190">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-190">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="7a2fb-191">**Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-191">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="7a2fb-192">Satış siparişleri 4-5 ve 4-6</span><span class="sxs-lookup"><span data-stu-id="7a2fb-192">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="7a2fb-193">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="7a2fb-193">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="7a2fb-194">**Müşteri hesabı:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="7a2fb-195">**Tesis:** *6*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-195">**Site:** *6*</span></span>
    - <span data-ttu-id="7a2fb-196">**Ambar:** *61*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-196">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="7a2fb-197">**Havuz:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-197">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="7a2fb-198">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="7a2fb-198">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="7a2fb-199">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="7a2fb-199">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="7a2fb-200">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-200">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="7a2fb-201">**Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-201">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="7a2fb-202">Satış siparişleri 4-7 ve 4-8</span><span class="sxs-lookup"><span data-stu-id="7a2fb-202">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="7a2fb-203">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="7a2fb-203">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="7a2fb-204">**Müşteri hesabı:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-204">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="7a2fb-205">**Tesis:** *6*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-205">**Site:** *6*</span></span>
    - <span data-ttu-id="7a2fb-206">**Ambar:** *61*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-206">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="7a2fb-207">**Havuz:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-207">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="7a2fb-208">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="7a2fb-208">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="7a2fb-209">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="7a2fb-209">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="7a2fb-210">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-210">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="7a2fb-211">**Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-211">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="7a2fb-212">Siparişleri ambara serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="7a2fb-212">Release the orders to the warehouse</span></span>

<span data-ttu-id="7a2fb-213">Bu senaryo için oluşturduğunuz her satış siparişini ambara serbest bırakmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-213">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="7a2fb-214">**Alacak hesapları \> Siparişler \> Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-214">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="7a2fb-215">Serbest bırakılacak satış siparişini bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-215">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="7a2fb-216">Eylem Bölmesi'ndeki **Ambar** sekmesinde, seçili satış siparişini serbest bırakmak için **Eylemler \> Ambara serbest bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-216">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="7a2fb-217">Bu yordamı, bu senaryo için oluşturduğunuz diğer satış siparişlerinin her biri için yineleyin.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-217">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-the-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="7a2fb-218">Sevkiyat konsolidasyonu çalışma ekranı kullanılarak sevkiyatları konsolide etme</span><span class="sxs-lookup"><span data-stu-id="7a2fb-218">Consolidate the shipments by using the shipment consolidation workbench</span></span>

1. <span data-ttu-id="7a2fb-219">**Ambar yönetimi \> Ambara serbest bırakma \> Sevkiyat konsolidasyonu çalışma ekranı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-219">Go to **Warehouse management \> Release to warehouse \> Shipment consolidation workbench**.</span></span>
1. <span data-ttu-id="7a2fb-220">Eylem Bölmesi'nde, **Sorgu düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-220">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="7a2fb-221">Sorgu düzenleyici iletişim kutusunda, kılavuza aşağıdaki ayarlara sahip bir satır eklemek için **Aralık** sekmesinde **Ekle**'yi seçin:</span><span class="sxs-lookup"><span data-stu-id="7a2fb-221">In the query editor dialog box, on the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="7a2fb-222">**Tablo:** *Satış siparişleri*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-222">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="7a2fb-223">**Alan:** *Satış siparişi*</span><span class="sxs-lookup"><span data-stu-id="7a2fb-223">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="7a2fb-224">**Ölçütler:** Bu senaryo için oluşturduğunuz her sipariş kümesi için virgülle ayrılmış satış siparişi numaralarının listesini girin.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-224">**Criteria:** Enter a comma-separated list of the sales order numbers for each order set that you created for this scenario.</span></span>

1. <span data-ttu-id="7a2fb-225">Sorgunuzu kaydetmek için **Tamam**'ı seçin ve iletişim kutusunu kapatın.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-225">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="7a2fb-226">Eylem Bölmesi'nde, **Sevkiyatları konsolide et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-226">On the Action Pane, select **Consolidate shipments**.</span></span>
1. <span data-ttu-id="7a2fb-227">Tüm sevkiyatları seçin ve ardından Eylem Bölmesi'nde, **Konsolide et**'i belirleyin.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-227">Select all the shipments, and then, on the Action Pane, select **Consolidate**.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="7a2fb-228">Sevkiyatları doğrulama</span><span class="sxs-lookup"><span data-stu-id="7a2fb-228">Verify the shipments</span></span>

<span data-ttu-id="7a2fb-229">Aşağıdaki yordam, sevkiyat konsolidasyonu nedeniyle oluşturulan veya güncelleştirilen sevkiyatları doğrulamanıza olanak verir.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-229">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="7a2fb-230">Bu senaryo için oluşturduğunuz her bir sipariş kümesini gözden geçirmek için bunu kullanın ve sonra, beklenen sonuçları elde ettiğinize emin olmak için izleyen alt bölümleri gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-230">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="7a2fb-231">**Ambar yönetimi \> Sevkiyatlar \> Tüm sevkiyatlar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-231">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="7a2fb-232">Gerekli sevkiyatı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-232">Find and select the required shipment.</span></span>
1. <span data-ttu-id="7a2fb-233">Sevkiyat oluşturulduğunda veya güncelleştirildiğinde bir konsolidasyon ilkesi kullanılmışsa bunu **Sevkiyat konsolidasyon ilkesi** alanında görmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-233">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="related-shipments-for-order-set-1"></a><span data-ttu-id="7a2fb-234">Sipariş kümesi 1 için ilgili sevkiyatlar</span><span class="sxs-lookup"><span data-stu-id="7a2fb-234">Related shipments for order set 1</span></span>

<span data-ttu-id="7a2fb-235">İki sevkiyat oluşturulmuş olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="7a2fb-235">Two shipments should have been created:</span></span>

- <span data-ttu-id="7a2fb-236">İlk sevkiyat üç satır içerir ve *CustomerMode* sevkiyat konsolidasyon ilkesi kullanılarak oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-236">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="7a2fb-237">Taşıma teslimat şekli için *Hava yolu* kullanmayan ikinci sevkiyat, *CustomerOrderNo* sevkiyat konsolidasyon ilkesi kullanılarak oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-237">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="related-shipments-for-order-set-2"></a><span data-ttu-id="7a2fb-238">Sipariş kümesi 2 için ilgili sevkiyatlar</span><span class="sxs-lookup"><span data-stu-id="7a2fb-238">Related shipments for order set 2</span></span>

<span data-ttu-id="7a2fb-239">Üç sevkiyat oluşturulmuş olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="7a2fb-239">Three shipments should have been created:</span></span>

- <span data-ttu-id="7a2fb-240">İlk sevkiyat *Yanıcı* maddeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-240">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="7a2fb-241">Diğer iki sevkiyatın her biri, *Patlayıcı* madde içeren bir satır içerir.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-241">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="related-shipments-for-order-set-3"></a><span data-ttu-id="7a2fb-242">Sipariş kümesi 3 için ilgili sevkiyatlar</span><span class="sxs-lookup"><span data-stu-id="7a2fb-242">Related shipments for order set 3</span></span>

<span data-ttu-id="7a2fb-243">İki sevkiyat oluşturulmuş olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="7a2fb-243">Two shipments should have been created:</span></span>

- <span data-ttu-id="7a2fb-244">İlk sevkiyat, **Müşteri talebi** alanının *1* olarak ayarlandığı satış siparişinden sipariş satırları içerir.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-244">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="7a2fb-245">İkinci sevkiyat, **Müşteri talebi** alanının *2* olarak ayarlandığı satış siparişinden sipariş satırları içerir.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-245">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="related-shipments-for-order-set-4"></a><span data-ttu-id="7a2fb-246">Sipariş kümesi 4 için ilgili sevkiyatlar</span><span class="sxs-lookup"><span data-stu-id="7a2fb-246">Related shipments for order set 4</span></span>

<span data-ttu-id="7a2fb-247">Dört sevkiyat oluşturulmuş olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="7a2fb-247">Four shipments should have been created:</span></span>

- <span data-ttu-id="7a2fb-248">Müşteri *US-003* ile ilgili iki siparişin satırları, *Sipariş havuzu* sevkiyat konsolidasyon ilkesi kullanılarak tek bir sevkiyatta gruplandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-248">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="7a2fb-249">Müşteri *US-004* ile ilgili iki siparişin satırları, *Sipariş havuzu* sevkiyat konsolidasyon ilkesi kullanılarak tek bir sevkiyatta gruplandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-249">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="7a2fb-250">Müşteri *US-007* ile ilgili satış siparişi 4-5 ve 4-6'daki satırlar, *Sipariş havuzu* sevkiyat konsolidasyon ilkesi kullanılarak tek bir sevkiyatta gruplandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-250">Lines from sales orders 4-5 and 4-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="7a2fb-251">Müşteri *US-007* ile ilgili satış siparişi 4-7 ve 4-8'daki satırlar, *CrossOrder* sevkiyat konsolidasyon ilkesi kullanılarak tek bir sevkiyatta gruplandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="7a2fb-251">Lines from sales orders 4-7 and 4-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7a2fb-252">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="7a2fb-252">Additional resources</span></span>

- [<span data-ttu-id="7a2fb-253">Sevkiyat konsolidasyonu ilkeleri</span><span class="sxs-lookup"><span data-stu-id="7a2fb-253">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="7a2fb-254">Sevkiyat konsolidasyon ilkelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="7a2fb-254">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)