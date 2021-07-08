---
title: Birimde kalan fiziksel miktar sıfır olmamalıdır
description: Bir sevk irsaliyesi oluşturduğunuzda, buna sağlanan verilerde sıfır olmayan stok miktarı ancak sıfır satış miktarı vardır.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: bfd381160bcfd1e6e5489e16cc22178b8a5142ee
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248808"
---
# <a name="physical-remaining-quantity-in-the-unit-must-not-be-zero"></a><span data-ttu-id="1faa9-103">Birimde kalan fiziksel miktar sıfır olmamalıdır</span><span class="sxs-lookup"><span data-stu-id="1faa9-103">Physical remaining quantity in the unit must not be zero</span></span>

<span data-ttu-id="1faa9-104">Hata kodu: SYS19591</span><span class="sxs-lookup"><span data-stu-id="1faa9-104">Error code: SYS19591</span></span>

## <a name="symptoms"></a><span data-ttu-id="1faa9-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="1faa9-105">Symptoms</span></span>

<span data-ttu-id="1faa9-106">Bir sevk irsaliyesi oluşturduğunuzda, buna sağlanan verilerde sıfır olmayan stok miktarı ancak sıfır satış miktarı vardır.</span><span class="sxs-lookup"><span data-stu-id="1faa9-106">When you generate a packing slip, the data that is supplied to it has a non-zero inventory quantity but a zero sales quantity.</span></span>

<span data-ttu-id="1faa9-107">Sevk irasliyesi oluşturmaya çalıştığınızda, sistem aşağıdaki hata iletisini gösterir:</span><span class="sxs-lookup"><span data-stu-id="1faa9-107">When you try to generate the packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="1faa9-108">%1 birimi cinsinden kalan fiziksel miktar sıfırdan farklı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1faa9-108">Physical remaining quantity in the unit %1 must be other than zero.</span></span>

<span data-ttu-id="1faa9-109">Bu nedenle, yükleme için sevk irsaliyesi oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="1faa9-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="1faa9-110">Nedeni</span><span class="sxs-lookup"><span data-stu-id="1faa9-110">Cause</span></span>

<span data-ttu-id="1faa9-111">Sistem, stok birimindeki fiziksel kalan miktarı ve sevkiyat birimindeki fiziksel kalan miktarı değerlendirir.</span><span class="sxs-lookup"><span data-stu-id="1faa9-111">The system evaluates the physical remaining quantity in the inventory unit and the physical remaining quantity in the shipping unit.</span></span> <span data-ttu-id="1faa9-112">Sistem sevkiyat biriminde kalan fiziksel miktarın 0 (sıfır) olduğunu, ancak stok birimindeki fiziksel kalan miktarın 0 olmadığını tespit ederse, sevk irsaliyesini oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="1faa9-112">If the system finds that the physical remaining quantity in the shipping unit is 0 (zero), but the physical remaining quantity in the inventory unit isn't 0, you can't generate the packing slip.</span></span> <span data-ttu-id="1faa9-113">Örneğin, maddenin satış birimi ve stok birimi farklıysa ve birimler arasındaki dönüştürme doğru değilse bu sorun oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="1faa9-113">For example, this issue might occur if the sales unit and inventory unit for the item differ, and the conversion between units isn't accurate.</span></span>

## <a name="resolution"></a><span data-ttu-id="1faa9-114">Çözüm</span><span class="sxs-lookup"><span data-stu-id="1faa9-114">Resolution</span></span>

<span data-ttu-id="1faa9-115">Yükleme veya sevkiyat işlemi şu anda sevk irsaliyesi oluşturmanın başarısız olduğu bir durumdadır.</span><span class="sxs-lookup"><span data-stu-id="1faa9-115">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="1faa9-116">Bu sorunu gidermek için aşağıdaki görevlerden birini tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="1faa9-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="1faa9-117">Yük satırlarınızı gözden geçirin ve tüm ilgili işlerin son sevkiyat konumunda tamamlandığından ve miktarların aynı olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="1faa9-117">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="1faa9-118">Yük satırlarını gözden geçirin ve miktarın yuvarlama sorunları olmadan net bir şekilde dönüştürülebilmesini sağlamak için ayarlamalar yapın.</span><span class="sxs-lookup"><span data-stu-id="1faa9-118">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without rounding issues.</span></span>
- <span data-ttu-id="1faa9-119">Yük satırlarınızı gözden geçirin ve birim ve miktarın birimin ondalık duyarlığıyla uyumlu hale getirilmesini sağlamak için ayarlamalar yapın.</span><span class="sxs-lookup"><span data-stu-id="1faa9-119">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>
- <span data-ttu-id="1faa9-120">Stok ölçü biriminin satış ölçü biriminden küçük olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="1faa9-120">Make sure that the inventory unit of measure is smaller than the sales unit of measure.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="1faa9-121">Yük satırlarınızı gözden geçirin ve tüm ilgili işlerin son sevkiyat konumunda tamamlandığından ve miktarların aynı olduğundan emin olun</span><span class="sxs-lookup"><span data-stu-id="1faa9-121">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="1faa9-122">Yük satırlarınızı gözden geçirmek için aşağıdaki yordamı kullanın ve tüm ilgili işlerin son sevkiyat konumunda tamamlandığından ve miktarların aynı olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="1faa9-122">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="1faa9-123">**Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="1faa9-123">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="1faa9-124">Sevkiyatın onaylanamadığı ilgili yükü seçin.</span><span class="sxs-lookup"><span data-stu-id="1faa9-124">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="1faa9-125">**Yük satırları** hızlı sekmesinde, yük satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="1faa9-125">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="1faa9-126">**Oluşturulan iş miktarı** alanının değerini not alın.</span><span class="sxs-lookup"><span data-stu-id="1faa9-126">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="1faa9-127">Eylem Bölmesinde **Yüklemeler** sekmesindeki **İlgili bilgiler** grubunda **Çalışma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="1faa9-127">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="1faa9-128">İşin son sevkiyat konumunda tamamlandığını ve teslim alınan iş miktarının yükleme satırındaki oluşturulan iş miktarıyla eşleştiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="1faa9-128">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="1faa9-129">Tüm ölçütlerin karşılandığından emin olmak için bu prosedürü tüm yükleme satırları için yineleyin.</span><span class="sxs-lookup"><span data-stu-id="1faa9-129">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-rounding-issues"></a><span data-ttu-id="1faa9-130">Yük satırlarını gözden geçirin ve miktarın yuvarlama sorunları olmadan net bir şekilde dönüştürülebilmesini sağlamak için ayarlamalar yapın</span><span class="sxs-lookup"><span data-stu-id="1faa9-130">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without rounding issues</span></span>

<span data-ttu-id="1faa9-131">Yük satırlarını gözden geçirmek için aşağıdaki yordamı kullanın ve miktarın yuvarlama sorunları olmadan net bir şekilde dönüştürülebilmesini sağlamak için ayarlamalar yapın</span><span class="sxs-lookup"><span data-stu-id="1faa9-131">Use the following procedure to review your load lines and make adjustments to ensure that the quantity can be cleanly converted without rounding issues.</span></span>

1. <span data-ttu-id="1faa9-132">**Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="1faa9-132">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="1faa9-133">Sevk irsaliyesinin oluşturulamadığı yükü seçin.</span><span class="sxs-lookup"><span data-stu-id="1faa9-133">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="1faa9-134">Eylem Bölmesi'nde,  **Sevk ve teslim alma** sekmesinin  **Tersine çevir** grubunda  **Sevkiyat onayını tersine çevir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1faa9-134">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="1faa9-135"> *\*Yük satırları** sekmesinde, fazla teslimatı aşan maddenin yük satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="1faa9-135">On the **Load lines** tab, select the load line for the item that exceeds the over-delivery.</span></span>
1. <span data-ttu-id="1faa9-136">Çekilen miktarı ayarlamak için **Çekilen miktarı düş**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="1faa9-136">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="1faa9-137"> *\*Satır ayrıntıları** sekmesinde, *\*Sipariş*\*'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1faa9-137">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="1faa9-138">Sevk irsaliyesi oluşturma işleminin devam edebilmesi için **Miktar** alanını çekilen miktara (yani **İşle oluşturulan miktar** alanının değerine) ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1faa9-138">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a><span data-ttu-id="1faa9-139">Yük satırlarınızı gözden geçirin ve birim ve miktarın birimin ondalık duyarlığıyla uyumlu hale getirilmesini sağlamak için ayarlamalar yapın</span><span class="sxs-lookup"><span data-stu-id="1faa9-139">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit</span></span>

<span data-ttu-id="1faa9-140">Yük satırlarınızı gözden geçirmek için aşağıdaki yordamı kullanın ve birim ve miktarın birimin ondalık duyarlığıyla uyumlu hale getirilmesini sağlamak için ayarlamalar yapın.</span><span class="sxs-lookup"><span data-stu-id="1faa9-140">Use the following procedure to review your load lines and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

1. <span data-ttu-id="1faa9-141">**Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="1faa9-141">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="1faa9-142">Sevk irsaliyesinin oluşturulamadığı yükü seçin.</span><span class="sxs-lookup"><span data-stu-id="1faa9-142">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="1faa9-143">**Yük satırları** hızlı sekmesinde, soruna neden olan maddenin yük satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="1faa9-143">On the **Load lines** FastTab, select the load line for the item that causes an issue.</span></span> <span data-ttu-id="1faa9-144">**Miktar** ve **Birim** alanlarının değerini not alın.</span><span class="sxs-lookup"><span data-stu-id="1faa9-144">Make a note of the value of the **Quantity** and **Unit** fields.</span></span>
1. <span data-ttu-id="1faa9-145">**Kuruluş yönetimi \> Birimler \> Birimler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="1faa9-145">Go to **Organization administration \> Units \> Units**.</span></span>
1. <span data-ttu-id="1faa9-146">Sevk irsaliyesinin oluşturulamadığı birimi seçin.</span><span class="sxs-lookup"><span data-stu-id="1faa9-146">Select the unit that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="1faa9-147">**Ondalık duyarlık** alanının değerini gerektiği gibi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1faa9-147">Adjust the value of the **Decimal precision** field as required.</span></span>

### <a name="make-sure-that-the-inventory-unit-of-measure-is-smaller-than-the-sales-unit-of-measure"></a><span data-ttu-id="1faa9-148">Stok ölçüm biriminin satış ölçüm biriminden küçük olduğundan emin olun</span><span class="sxs-lookup"><span data-stu-id="1faa9-148">Make sure that the inventory unit of measure is smaller than the sales unit of measure</span></span>

<span data-ttu-id="1faa9-149">Stok ölçü biriminin satış ölçü biriminden küçük olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="1faa9-149">Make sure that the inventory unit of measure is smaller than the sales unit of measure.</span></span> <span data-ttu-id="1faa9-150">Madde için ölçü birimini gerektiği gibi yeniden yapılandırmayı düşünün.</span><span class="sxs-lookup"><span data-stu-id="1faa9-150">Consider reconfiguring the unit of measure for the item as required.</span></span>
