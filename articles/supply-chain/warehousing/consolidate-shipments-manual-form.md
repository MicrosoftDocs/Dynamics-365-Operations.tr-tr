---
title: Sevkiyatları konsolide etme sayfası kullanılarak sevkiyatları manuel olarak konsolide etme
description: Bu konu, çoklu siparişlerin aynı yükte yer alarak ambara serbest bırakıldığı ve ardından, Sevkiyatları konsolide etme sayfası kullanılarak konsolide edildiği bir senaryo sunar.
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
ms.openlocfilehash: 6d9186fe242fa56b6a360d6a4e4284c0c3eac141
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242217"
---
# <a name="consolidate-shipments-manually-by-using-the-consolidate-shipments-page"></a><span data-ttu-id="13527-103">Sevkiyatları konsolide etme sayfası kullanılarak sevkiyatları manuel olarak konsolide etme</span><span class="sxs-lookup"><span data-stu-id="13527-103">Consolidate shipments manually by using the Consolidate shipments page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="13527-104">Bu konu, çoklu siparişlerin aynı yükte yer alarak ambara serbest bırakıldığı ve ardından, **Sevkiyatları konsolide etme** sayfası kullanılarak konsolide edildiği bir senaryo sunar.</span><span class="sxs-lookup"><span data-stu-id="13527-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated later by using the **Consolidate shipments** page.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="13527-105">Tanıtım verilerini kullanılabilir hale getirme</span><span class="sxs-lookup"><span data-stu-id="13527-105">Make demo data available</span></span>

<span data-ttu-id="13527-106">Bu konudaki senaryo, Microsoft Dynamics 365 Supply Chain Management için sağlanan standart tanıtım verilerinde bulunan değerlere ve kayıtlara başvurur.</span><span class="sxs-lookup"><span data-stu-id="13527-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="13527-107">Alıştırmaları yaparken burada sağlanan değerleri kullanmak isterseniz tanıtım verisinin yüklü olduğu bir ortamda çalıştığınızdan ve başlamadan önce tüzel kişiliği **USMF** olarak ayarladığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="13527-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="13527-108">Sevkiyat konsolidasyon ilkelerini ve ürün filtrelerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="13527-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="13527-109">Burada açıklanan senaryo, özelliği önceden açtığınız, [Sevkiyat konsolidasyonu ilkelerini yapılandırma](configure-shipment-consolidation-policies.md) alıştırmalarını yaptığınız ve burada açıklanan ilkeleri ve diğer kayıtları oluşturduğunuz varsayımına dayanır.</span><span class="sxs-lookup"><span data-stu-id="13527-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="13527-110">Bu senaryoya devam etmeden önce söz konusu alıştırmaları yaptığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="13527-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="13527-111">Bu senaryo için satış siparişleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="13527-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="13527-112">Çalışabileceğiniz bir satış siparişleri koleksiyonu oluşturarak başlayın.</span><span class="sxs-lookup"><span data-stu-id="13527-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="13527-113">Gelişmiş ambar (WMS) işlemleri için etkinleştirilen bir ambarla çalışmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="13527-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="13527-114">Başka bir ambar açıkça belirtilmedikçe, aşağıdaki sipariş kümelerinin her biri için aynı ambar kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="13527-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="13527-115">**Alacak hesapları \> Siparişler \> Tüm satış siparişleri** öğesine gidin ve aşağıdaki alt bölümlerde açıklanan ayarlara sahip bir satış siparişleri koleksiyonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="13527-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-sales-orders-1-and-2"></a><span data-ttu-id="13527-116">Satış siparişi 1 ve 2'yi oluşturma</span><span class="sxs-lookup"><span data-stu-id="13527-116">Create sales orders 1 and 2</span></span>

1. <span data-ttu-id="13527-117">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="13527-117">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="13527-118">**Müşteri hesabı:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="13527-118">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="13527-119">**Havuz:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="13527-119">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="13527-120">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="13527-120">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="13527-121">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="13527-121">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="13527-122">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="13527-122">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="13527-123">**Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="13527-123">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-sales-orders-3-and-4"></a><span data-ttu-id="13527-124">Satış siparişi 3 ve 4'ü oluşturma</span><span class="sxs-lookup"><span data-stu-id="13527-124">Create sales orders 3 and 4</span></span>

1. <span data-ttu-id="13527-125">Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="13527-125">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="13527-126">**Müşteri hesabı:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="13527-126">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="13527-127">**Havuz:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="13527-127">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="13527-128">Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="13527-128">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="13527-129">**Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)</span><span class="sxs-lookup"><span data-stu-id="13527-129">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="13527-130">**Miktar:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="13527-130">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="13527-131">**Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="13527-131">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="13527-132">Siparişleri ambara serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="13527-132">Release the orders to the warehouse</span></span>

<span data-ttu-id="13527-133">Bu senaryo için oluşturduğunuz her satış siparişini ambara serbest bırakmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="13527-133">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="13527-134">**Alacak hesapları \> Siparişler \> Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="13527-134">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="13527-135">Serbest bırakılacak satış siparişini bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="13527-135">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="13527-136">Eylem Bölmesi'ndeki **Ambar** sekmesinde, seçili satış siparişini serbest bırakmak için **Eylemler \> Ambara serbest bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="13527-136">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="13527-137">Bu yordamı, bu senaryo için oluşturduğunuz diğer satış siparişlerinin her biri için yineleyin.</span><span class="sxs-lookup"><span data-stu-id="13527-137">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-shipments"></a><span data-ttu-id="13527-138">Sevkiyatları konsolide et</span><span class="sxs-lookup"><span data-stu-id="13527-138">Consolidate shipments</span></span>

1. <span data-ttu-id="13527-139">**Ambar yönetimi \> Sevkiyatlar \> Tüm sevkiyatlar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="13527-139">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="13527-140">Satış siparişi 1 ambara serbest bırakıldığında oluşturulan bir sevkiyatı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="13527-140">Find and select a shipment that was created when sales order 1 was released to the warehouse.</span></span> <span data-ttu-id="13527-141">(**Sevkiyat konsolidasyon ilkesi** alanı *Sipariş havuzu* olarak ayarlanmalıdır.)</span><span class="sxs-lookup"><span data-stu-id="13527-141">(Its **Shipment consolidation policy** field should be set to *Order pool*.)</span></span>
1. <span data-ttu-id="13527-142">Eylem Bölmesi'ndeki **Sevkiyatlar** sekmesinde, **Sevkiyatlar \> Sevkiyatları konsolide et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="13527-142">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="13527-143">Konsolidasyon için önerilen sevkiyatları doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="13527-143">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="13527-144">Konsolidasyon için yalnızca aynı ilkeye sahip bir sevkiyat önerilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="13527-144">Only one shipment that has the same policy should be suggested for consolidation.</span></span>
1. <span data-ttu-id="13527-145">**Sevkiyat konsolidasyonu** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="13527-145">Close the **Shipment consolidation** page.</span></span>
1. <span data-ttu-id="13527-146">Satış siparişi 3 ambara serbest bırakıldığında oluşturulan bir sevkiyatı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="13527-146">Find and select a shipment that was created when sales order 3 was released to the warehouse.</span></span> <span data-ttu-id="13527-147">(**Sevkiyat konsolidasyon ilkesi** alanı *Varsayılan* olarak ayarlanmalıdır.)</span><span class="sxs-lookup"><span data-stu-id="13527-147">(Its **Shipment consolidation policy** field should be set to *Default*.)</span></span>
1. <span data-ttu-id="13527-148">Eylem Bölmesi'ndeki **Sevkiyatlar** sekmesinde, **Sevkiyatlar \> Sevkiyatları konsolide et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="13527-148">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="13527-149">Konsolidasyon için herhangi bir sevkiyatın önerilmediğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="13527-149">Verify that no shipments are suggested for consolidation.</span></span>
1. <span data-ttu-id="13527-150">**Filtreleri göster**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="13527-150">Select **Show filters**.</span></span>
1. <span data-ttu-id="13527-151">**Filtreler** bölmesinde, **Sipariş numarası** filtresini kaldırın ve sonra **Uygula**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="13527-151">In the **Filters** pane, remove the **Order number** filter, and then select **Apply**.</span></span>
1. <span data-ttu-id="13527-152">Konsolidasyon için önerilen sevkiyatları doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="13527-152">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="13527-153">Konsolidasyon için yalnızca aynı ilkeye sahip bir sevkiyat önerilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="13527-153">Only one shipment that has the same policy should be suggested for consolidation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="13527-154">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="13527-154">Additional resources</span></span>

- [<span data-ttu-id="13527-155">Sevkiyat konsolidasyonu ilkeleri</span><span class="sxs-lookup"><span data-stu-id="13527-155">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="13527-156">Sevkiyat konsolidasyon ilkelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="13527-156">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]