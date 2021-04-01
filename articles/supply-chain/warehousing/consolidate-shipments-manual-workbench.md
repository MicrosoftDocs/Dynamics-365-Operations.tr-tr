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
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSShipConsolidationSetShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 9b7dc72d789fd331c3636c406ac6a45566ba81ca
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242193"
---
# <a name="consolidate-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="550e9-103">Sevkiyat konsolidasyonu çalışma ekranı kullanılarak sevkiyatları konsolide etme</span><span class="sxs-lookup"><span data-stu-id="550e9-103">Consolidate shipments by using the shipment consolidation workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="550e9-104">Bu konu, çoklu siparişlerin aynı yükte yer alarak ambara serbest bırakıldığı ve ardından, sevkiyat konsolidasyon çalışma ekranı kullanılarak sevkiyatlar halinde konsolide edildiği bir senaryo sunar.</span><span class="sxs-lookup"><span data-stu-id="550e9-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated into shipments later by using the shipment consolidation workbench.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="550e9-105">Tanıtım verilerini kullanılabilir hale getirme</span><span class="sxs-lookup"><span data-stu-id="550e9-105">Make demo data available</span></span>

<span data-ttu-id="550e9-106">Bu konudaki senaryo, Microsoft Dynamics 365 Supply Chain Management için sağlanan standart tanıtım verilerinde bulunan değerlere ve kayıtlara başvurur.</span><span class="sxs-lookup"><span data-stu-id="550e9-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="550e9-107">Alıştırmaları yaparken burada sağlanan değerleri kullanmak isterseniz tanıtım verisinin yüklü olduğu bir ortamda çalıştığınızdan ve başlamadan önce tüzel kişiliği **USMF** olarak ayarladığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="550e9-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="550e9-108">Sevkiyat konsolidasyon ilkelerini ve ürün filtrelerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="550e9-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="550e9-109">Burada açıklanan senaryo, özelliği önceden açtığınız, [Sevkiyat konsolidasyonu ilkelerini yapılandırma](configure-shipment-consolidation-policies.md) alıştırmalarını yaptığınız ve burada açıklanan ilkeleri ve diğer kayıtları oluşturduğunuz varsayımına dayanır.</span><span class="sxs-lookup"><span data-stu-id="550e9-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="550e9-110">Bu senaryoya devam etmeden önce söz konusu alıştırmaları yaptığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="550e9-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="turn-on-the-manual-shipment-consolidation-feature"></a><span data-ttu-id="550e9-111">Manuel sevkiyat konsolidasyon özelliğini açma</span><span class="sxs-lookup"><span data-stu-id="550e9-111">Turn on the manual shipment consolidation feature</span></span>

<span data-ttu-id="550e9-112">*Manuel sevkiyat konsolidasyon* özelliğini kullanabilmeniz için önce sisteminizde bu özelliği açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="550e9-112">Before you can use the *Manual shipment consolidation* feature, you must turn it on in your system.</span></span> <span data-ttu-id="550e9-113">Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="550e9-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="550e9-114">**Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:</span><span class="sxs-lookup"><span data-stu-id="550e9-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="550e9-115">**Modül:** *Ambar yönetimi*</span><span class="sxs-lookup"><span data-stu-id="550e9-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="550e9-116">**Özellik adı:** *Manuel sevkiyat konsolidasyonu*</span><span class="sxs-lookup"><span data-stu-id="550e9-116">**Feature name:** *Manual shipment consolidation*</span></span>

<span data-ttu-id="550e9-117">[Sevkiyat konsolidasyon ilkelerini yapılandırma](configure-shipment-consolidation-policies.md) konusunda bahsedildiği gibi ilkeleri oluşturabilmeniz için önce *Sevkiyatı konsolide et* özelliğini de etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="550e9-117">As was mentioned in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), you must also turn on the *Consolidate shipment* feature before you can create policies.</span></span> <span data-ttu-id="550e9-118">Ancak, o adımı zaten tamamlamış olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="550e9-118">However, you should already have completed that step.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="550e9-119">Bu senaryo için satış siparişleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="550e9-119">Create the sales orders for this scenario</span></span>

<span data-ttu-id="550e9-120">Çalışabileceğiniz bir satış siparişleri koleksiyonu oluşturarak başlayın.</span><span class="sxs-lookup"><span data-stu-id="550e9-120">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="550e9-121">Gelişmiş ambar (WMS) işlemleri için etkinleştirilen bir ambarla çalışmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="550e9-121">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="550e9-122">Başka bir ambar açıkça belirtilmedikçe, aşağıdaki sipariş kümelerinin her biri için aynı ambar kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="550e9-122">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="550e9-123">**Alacak hesapları \> Siparişler \> Tüm satış siparişleri** öğesine gidin ve aşağıdaki alt bölümlerde açıklanan ayarlara sahip bir satış siparişleri koleksiyonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="550e9-123">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="550e9-124">Sipariş kümesi 1'i oluşturma</span><span class="sxs-lookup"><span data-stu-id="550e9-124">Create order set 1</span></span>

#### <a name="sales-orders-1-1-and-1-2"></a><span data-ttu-id="550e9-125">Satış siparişleri 1-1 ve 1-2</span><span class="sxs-lookup"><span data-stu-id="550e9-125">Sales orders 1-1 and 1-2</span></span>

1. <span data-ttu-id="550e9-126">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="550e9-126">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="550e9-127">**Müşteri hesabı:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="550e9-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="550e9-128">**Teslimat şekli:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="550e9-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="550e9-129">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="550e9-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="550e9-130">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="550e9-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="550e9-131">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="550e9-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="550e9-132">**Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="550e9-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="550e9-133">Satış siparişi 1-3</span><span class="sxs-lookup"><span data-stu-id="550e9-133">Sales order 1-3</span></span>

1. <span data-ttu-id="550e9-134">Aşağıdaki ayarlara sahip bir satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="550e9-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="550e9-135">**Müşteri hesabı:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="550e9-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="550e9-136">**Teslimat şekli:** *10*</span><span class="sxs-lookup"><span data-stu-id="550e9-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="550e9-137">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="550e9-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="550e9-138">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="550e9-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="550e9-139">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="550e9-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="550e9-140">**Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="550e9-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="550e9-141">Aşağıdaki ayarlara sahip ikinci bir satış siparişi satırı oluşturun:</span><span class="sxs-lookup"><span data-stu-id="550e9-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="550e9-142">**Madde numarası:** *A0002* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="550e9-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="550e9-143">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="550e9-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="550e9-144">**Teslimat şekli:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="550e9-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="550e9-145">**Stok \> Rezervasyon**'u ve sonra Eylem Bölmesi'nde, ikinci sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="550e9-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="550e9-146">Sipariş kümesi 2'yi oluşturma</span><span class="sxs-lookup"><span data-stu-id="550e9-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="550e9-147">Satış siparişleri 2-1 ve 2-2</span><span class="sxs-lookup"><span data-stu-id="550e9-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="550e9-148">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="550e9-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="550e9-149">**Müşteri hesabı:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="550e9-149">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="550e9-150">**Teslimat şekli:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="550e9-150">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="550e9-151">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="550e9-151">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="550e9-152">**Madde numarası:** *M9200* (**Kod 4** filtresinin *Yanıcı* değerine ayarlandığı bir madde)</span><span class="sxs-lookup"><span data-stu-id="550e9-152">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="550e9-153">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="550e9-153">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="550e9-154">**Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="550e9-154">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="550e9-155">Aşağıdaki ayarlara sahip ikinci bir satış siparişi satırı oluşturun:</span><span class="sxs-lookup"><span data-stu-id="550e9-155">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="550e9-156">**Madde numarası:** *M9201* (**Kod 4** filtresinin *Patlayıcı* değerine ayarlandığı bir madde)</span><span class="sxs-lookup"><span data-stu-id="550e9-156">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="550e9-157">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="550e9-157">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="550e9-158">**Teslimat şekli:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="550e9-158">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="550e9-159">**Stok \> Rezervasyon**'u ve sonra Eylem Bölmesi'nde, ikinci sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="550e9-159">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="550e9-160">Sipariş kümesi 3'ü oluşturma</span><span class="sxs-lookup"><span data-stu-id="550e9-160">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="550e9-161">Satış siparişleri 3-1 ve 3-2</span><span class="sxs-lookup"><span data-stu-id="550e9-161">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="550e9-162">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="550e9-162">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="550e9-163">**Müşteri hesabı:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="550e9-163">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="550e9-164">**Müşteri talebi:** *1*</span><span class="sxs-lookup"><span data-stu-id="550e9-164">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="550e9-165">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="550e9-165">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="550e9-166">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="550e9-166">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="550e9-167">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="550e9-167">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="550e9-168">**Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="550e9-168">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="550e9-169">Satış siparişleri 3-3 ve 3-4</span><span class="sxs-lookup"><span data-stu-id="550e9-169">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="550e9-170">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="550e9-170">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="550e9-171">**Müşteri hesabı:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="550e9-171">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="550e9-172">**Müşteri talebi:** *2*</span><span class="sxs-lookup"><span data-stu-id="550e9-172">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="550e9-173">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="550e9-173">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="550e9-174">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="550e9-174">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="550e9-175">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="550e9-175">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="550e9-176">**Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="550e9-176">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="550e9-177">Sipariş kümesi 4'ü oluşturma</span><span class="sxs-lookup"><span data-stu-id="550e9-177">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="550e9-178">Satış siparişleri 4-1 ve 4-2</span><span class="sxs-lookup"><span data-stu-id="550e9-178">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="550e9-179">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="550e9-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="550e9-180">**Müşteri hesabı:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="550e9-180">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="550e9-181">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="550e9-181">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="550e9-182">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="550e9-182">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="550e9-183">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="550e9-183">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="550e9-184">**Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="550e9-184">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="550e9-185">Satış siparişleri 4-3 ve 4-4</span><span class="sxs-lookup"><span data-stu-id="550e9-185">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="550e9-186">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="550e9-186">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="550e9-187">**Müşteri hesabı:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="550e9-187">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="550e9-188">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="550e9-188">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="550e9-189">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="550e9-189">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="550e9-190">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="550e9-190">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="550e9-191">**Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="550e9-191">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="550e9-192">Satış siparişleri 4-5 ve 4-6</span><span class="sxs-lookup"><span data-stu-id="550e9-192">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="550e9-193">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="550e9-193">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="550e9-194">**Müşteri hesabı:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="550e9-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="550e9-195">**Tesis:** *6*</span><span class="sxs-lookup"><span data-stu-id="550e9-195">**Site:** *6*</span></span>
    - <span data-ttu-id="550e9-196">**Ambar:** *61*</span><span class="sxs-lookup"><span data-stu-id="550e9-196">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="550e9-197">**Havuz:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="550e9-197">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="550e9-198">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="550e9-198">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="550e9-199">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="550e9-199">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="550e9-200">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="550e9-200">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="550e9-201">**Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="550e9-201">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="550e9-202">Satış siparişleri 4-7 ve 4-8</span><span class="sxs-lookup"><span data-stu-id="550e9-202">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="550e9-203">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="550e9-203">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="550e9-204">**Müşteri hesabı:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="550e9-204">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="550e9-205">**Tesis:** *6*</span><span class="sxs-lookup"><span data-stu-id="550e9-205">**Site:** *6*</span></span>
    - <span data-ttu-id="550e9-206">**Ambar:** *61*</span><span class="sxs-lookup"><span data-stu-id="550e9-206">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="550e9-207">**Havuz:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="550e9-207">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="550e9-208">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="550e9-208">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="550e9-209">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="550e9-209">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="550e9-210">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="550e9-210">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="550e9-211">**Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="550e9-211">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="550e9-212">Siparişleri ambara serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="550e9-212">Release the orders to the warehouse</span></span>

<span data-ttu-id="550e9-213">Bu senaryo için oluşturduğunuz her satış siparişini ambara serbest bırakmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="550e9-213">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="550e9-214">**Alacak hesapları \> Siparişler \> Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="550e9-214">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="550e9-215">Serbest bırakılacak satış siparişini bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="550e9-215">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="550e9-216">Eylem Bölmesi'ndeki **Ambar** sekmesinde, seçili satış siparişini serbest bırakmak için **Eylemler \> Ambara serbest bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="550e9-216">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="550e9-217">Bu yordamı, bu senaryo için oluşturduğunuz diğer satış siparişlerinin her biri için yineleyin.</span><span class="sxs-lookup"><span data-stu-id="550e9-217">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-the-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="550e9-218">Sevkiyat konsolidasyonu çalışma ekranı kullanılarak sevkiyatları konsolide etme</span><span class="sxs-lookup"><span data-stu-id="550e9-218">Consolidate the shipments by using the shipment consolidation workbench</span></span>

1. <span data-ttu-id="550e9-219">**Ambar yönetimi \> Ambara serbest bırakma \> Sevkiyat konsolidasyonu çalışma ekranı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="550e9-219">Go to **Warehouse management \> Release to warehouse \> Shipment consolidation workbench**.</span></span>
1. <span data-ttu-id="550e9-220">Eylem Bölmesi'nde, **Sorgu düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="550e9-220">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="550e9-221">Sorgu düzenleyici iletişim kutusunda, kılavuza aşağıdaki ayarlara sahip bir satır eklemek için **Aralık** sekmesinde **Ekle**'yi seçin:</span><span class="sxs-lookup"><span data-stu-id="550e9-221">In the query editor dialog box, on the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="550e9-222">**Tablo:** *Satış siparişleri*</span><span class="sxs-lookup"><span data-stu-id="550e9-222">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="550e9-223">**Alan:** *Satış siparişi*</span><span class="sxs-lookup"><span data-stu-id="550e9-223">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="550e9-224">**Ölçütler:** Bu senaryo için oluşturduğunuz her sipariş kümesi için virgülle ayrılmış satış siparişi numaralarının listesini girin.</span><span class="sxs-lookup"><span data-stu-id="550e9-224">**Criteria:** Enter a comma-separated list of the sales order numbers for each order set that you created for this scenario.</span></span>

1. <span data-ttu-id="550e9-225">Sorgunuzu kaydetmek için **Tamam**'ı seçin ve iletişim kutusunu kapatın.</span><span class="sxs-lookup"><span data-stu-id="550e9-225">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="550e9-226">Eylem Bölmesi'nde, **Sevkiyatları konsolide et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="550e9-226">On the Action Pane, select **Consolidate shipments**.</span></span>
1. <span data-ttu-id="550e9-227">Tüm sevkiyatları seçin ve ardından Eylem Bölmesi'nde, **Konsolide et**'i belirleyin.</span><span class="sxs-lookup"><span data-stu-id="550e9-227">Select all the shipments, and then, on the Action Pane, select **Consolidate**.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="550e9-228">Sevkiyatları doğrulama</span><span class="sxs-lookup"><span data-stu-id="550e9-228">Verify the shipments</span></span>

<span data-ttu-id="550e9-229">Aşağıdaki yordam, sevkiyat konsolidasyonu nedeniyle oluşturulan veya güncelleştirilen sevkiyatları doğrulamanıza olanak verir.</span><span class="sxs-lookup"><span data-stu-id="550e9-229">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="550e9-230">Bu senaryo için oluşturduğunuz her bir sipariş kümesini gözden geçirmek için bunu kullanın ve sonra, beklenen sonuçları elde ettiğinize emin olmak için izleyen alt bölümleri gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="550e9-230">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="550e9-231">**Ambar yönetimi \> Sevkiyatlar \> Tüm sevkiyatlar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="550e9-231">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="550e9-232">Gerekli sevkiyatı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="550e9-232">Find and select the required shipment.</span></span>
1. <span data-ttu-id="550e9-233">Sevkiyat oluşturulduğunda veya güncelleştirildiğinde bir konsolidasyon ilkesi kullanılmışsa bunu **Sevkiyat konsolidasyon ilkesi** alanında görmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="550e9-233">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="related-shipments-for-order-set-1"></a><span data-ttu-id="550e9-234">Sipariş kümesi 1 için ilgili sevkiyatlar</span><span class="sxs-lookup"><span data-stu-id="550e9-234">Related shipments for order set 1</span></span>

<span data-ttu-id="550e9-235">İki sevkiyat oluşturulmuş olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="550e9-235">Two shipments should have been created:</span></span>

- <span data-ttu-id="550e9-236">İlk sevkiyat üç satır içerir ve *CustomerMode* sevkiyat konsolidasyon ilkesi kullanılarak oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="550e9-236">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="550e9-237">Taşıma teslimat şekli için *Hava yolu* kullanmayan ikinci sevkiyat, *CustomerOrderNo* sevkiyat konsolidasyon ilkesi kullanılarak oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="550e9-237">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="related-shipments-for-order-set-2"></a><span data-ttu-id="550e9-238">Sipariş kümesi 2 için ilgili sevkiyatlar</span><span class="sxs-lookup"><span data-stu-id="550e9-238">Related shipments for order set 2</span></span>

<span data-ttu-id="550e9-239">Üç sevkiyat oluşturulmuş olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="550e9-239">Three shipments should have been created:</span></span>

- <span data-ttu-id="550e9-240">İlk sevkiyat *Yanıcı* maddeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="550e9-240">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="550e9-241">Diğer iki sevkiyatın her biri, *Patlayıcı* madde içeren bir satır içerir.</span><span class="sxs-lookup"><span data-stu-id="550e9-241">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="related-shipments-for-order-set-3"></a><span data-ttu-id="550e9-242">Sipariş kümesi 3 için ilgili sevkiyatlar</span><span class="sxs-lookup"><span data-stu-id="550e9-242">Related shipments for order set 3</span></span>

<span data-ttu-id="550e9-243">İki sevkiyat oluşturulmuş olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="550e9-243">Two shipments should have been created:</span></span>

- <span data-ttu-id="550e9-244">İlk sevkiyat, **Müşteri talebi** alanının *1* olarak ayarlandığı satış siparişinden sipariş satırları içerir.</span><span class="sxs-lookup"><span data-stu-id="550e9-244">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="550e9-245">İkinci sevkiyat, **Müşteri talebi** alanının *2* olarak ayarlandığı satış siparişinden sipariş satırları içerir.</span><span class="sxs-lookup"><span data-stu-id="550e9-245">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="related-shipments-for-order-set-4"></a><span data-ttu-id="550e9-246">Sipariş kümesi 4 için ilgili sevkiyatlar</span><span class="sxs-lookup"><span data-stu-id="550e9-246">Related shipments for order set 4</span></span>

<span data-ttu-id="550e9-247">Dört sevkiyat oluşturulmuş olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="550e9-247">Four shipments should have been created:</span></span>

- <span data-ttu-id="550e9-248">Müşteri *US-003* ile ilgili iki siparişin satırları, *Sipariş havuzu* sevkiyat konsolidasyon ilkesi kullanılarak tek bir sevkiyatta gruplandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="550e9-248">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="550e9-249">Müşteri *US-004* ile ilgili iki siparişin satırları, *Sipariş havuzu* sevkiyat konsolidasyon ilkesi kullanılarak tek bir sevkiyatta gruplandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="550e9-249">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="550e9-250">Müşteri *US-007* ile ilgili satış siparişi 4-5 ve 4-6'daki satırlar, *Sipariş havuzu* sevkiyat konsolidasyon ilkesi kullanılarak tek bir sevkiyatta gruplandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="550e9-250">Lines from sales orders 4-5 and 4-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="550e9-251">Müşteri *US-007* ile ilgili satış siparişi 4-7 ve 4-8'daki satırlar, *CrossOrder* sevkiyat konsolidasyon ilkesi kullanılarak tek bir sevkiyatta gruplandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="550e9-251">Lines from sales orders 4-7 and 4-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="550e9-252">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="550e9-252">Additional resources</span></span>

- [<span data-ttu-id="550e9-253">Sevkiyat konsolidasyonu ilkeleri</span><span class="sxs-lookup"><span data-stu-id="550e9-253">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="550e9-254">Sevkiyat konsolidasyon ilkelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="550e9-254">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]