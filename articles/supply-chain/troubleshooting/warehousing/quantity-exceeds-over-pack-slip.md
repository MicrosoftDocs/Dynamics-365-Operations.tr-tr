---
title: Sevk irsaliyesi oluşturma sırasında miktar fazla teslimat yüzdesini aşıyor
description: Sevk irsaliyesi oluşturduğunuzda, giden yük fazla teslimat yüzdesini aşan bir miktar içerir.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSSalesPackingSlipPost,WHSLoadPlanningListPage_WHSSalesPackingSlipPost,WHSLoadPlanningWorkbench_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1106322cc3772c1b671b7fa82fb74039c028ba35
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249184"
---
# <a name="quantity-exceeds-over-delivery-percentage-during-packing-slip-generation"></a><span data-ttu-id="f58f8-103">Sevk irsaliyesi oluşturma sırasında miktar fazla teslimat yüzdesini aşıyor</span><span class="sxs-lookup"><span data-stu-id="f58f8-103">Quantity exceeds over-delivery percentage during packing slip generation</span></span>

<span data-ttu-id="f58f8-104">Hata kodu: SYS24920</span><span class="sxs-lookup"><span data-stu-id="f58f8-104">Error code: SYS24920</span></span>

## <a name="symptoms"></a><span data-ttu-id="f58f8-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="f58f8-105">Symptoms</span></span>

<span data-ttu-id="f58f8-106">Sevk irsaliyesi oluşturduğunuzda, giden yük fazla teslimat yüzdesini aşan bir miktar içerir.</span><span class="sxs-lookup"><span data-stu-id="f58f8-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the over-delivery percentage.</span></span>

<span data-ttu-id="f58f8-107">Sevk irsaliyesi oluşturmaya çalıştığınızda, sistem aşağıdaki hata iletisini gösterir:</span><span class="sxs-lookup"><span data-stu-id="f58f8-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="f58f8-108">Satırın fazla teslimat yüzdesi %1, ancak izin verilen fazla teslimat yüzdesi %2.</span><span class="sxs-lookup"><span data-stu-id="f58f8-108">Overdelivery of line is %1 percent, but the allowed overdelivery is only %2 percent.</span></span>

<span data-ttu-id="f58f8-109">Bu nedenle, yükleme için sevk irsaliyesi oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="f58f8-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="f58f8-110">Nedeni</span><span class="sxs-lookup"><span data-stu-id="f58f8-110">Cause</span></span>

<span data-ttu-id="f58f8-111">Yük veya sevkiyart için çekilen miktar sipariş edilen miktardan çoktur ve fazla teslimat yüzdesi aralığında değildir.</span><span class="sxs-lookup"><span data-stu-id="f58f8-111">The picked quantity for the load or shipment is more than the ordered quantity and isn't within the range of the over-delivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="f58f8-112">Çözüm</span><span class="sxs-lookup"><span data-stu-id="f58f8-112">Resolution</span></span>

<span data-ttu-id="f58f8-113">Yükleme veya sevkiyat işlemi şu anda sevk irsaliyesi oluşturmanın başarısız olduğu bir durumdadır.</span><span class="sxs-lookup"><span data-stu-id="f58f8-113">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="f58f8-114">Bu sorunu gidermek için aşağıdaki görevlerden birini tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="f58f8-114">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="f58f8-115">Yük satırı miktarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="f58f8-115">Adjust the load line quantity.</span></span>
- <span data-ttu-id="f58f8-116">Fazla teslimat yüzdesini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f58f8-116">Adjust the over-delivery percentage.</span></span>
- <span data-ttu-id="f58f8-117">Tersine çevirin ve ayarlamalar yapın.</span><span class="sxs-lookup"><span data-stu-id="f58f8-117">Reverse and make adjustments.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="f58f8-118">Yük satırı miktarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="f58f8-118">Adjust the load line quantity</span></span>

<span data-ttu-id="f58f8-119">Yük satırı miktarını ayarlamak için aşağıdaki yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="f58f8-119">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="f58f8-120">**Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="f58f8-120">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="f58f8-121">Sevk irsaliyesinin oluşturulamadığı yükü seçin.</span><span class="sxs-lookup"><span data-stu-id="f58f8-121">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="f58f8-122">Eylem Bölmesi'nde,  **Sevk ve teslim alma** sekmesinin  **Tersine çevir** grubunda  **Sevkiyat onayını tersine çevir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f58f8-122">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="f58f8-123"> *\*Yük satırları** sekmesinde, fazla teslimat yüzdesini aşan maddenin yük satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="f58f8-123">On the **Load lines** tab, select the load line for the item that exceeds the over-delivery percentage.</span></span>
1. <span data-ttu-id="f58f8-124">Çekilen miktarı ayarlamak için **Çekilen miktarı düş**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="f58f8-124">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="f58f8-125"> *\*Satır ayrıntıları** sekmesinde, *\*Sipariş*\*'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f58f8-125">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="f58f8-126">Sevk irsaliyesi oluşturma işleminin devam edebilmesi için **Miktar** alanını çekilen miktara (yani **İşle oluşturulan miktar** alanının değerine) ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f58f8-126">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="adjust-the-over-delivery-percentage"></a><span data-ttu-id="f58f8-127">Fazla teslimat yüzdesini ayarlama</span><span class="sxs-lookup"><span data-stu-id="f58f8-127">Adjust the over-delivery percentage</span></span>

<span data-ttu-id="f58f8-128">Fazla teslimat yüzdesini ayarlamak için aşağıdaki yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="f58f8-128">Use the following procedure to adjust the over-delivery percentage.</span></span>

1. <span data-ttu-id="f58f8-129">**Alacak hesapları \> Siparişler \> Tüm siparişler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="f58f8-129">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="f58f8-130">Yük için sevk irsaliyesini deftere nakledemeyeceğiniz satış siparişini seçin.</span><span class="sxs-lookup"><span data-stu-id="f58f8-130">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="f58f8-131"> *\*Satış siparişi satırları** sekmesinde, fazla teslimat yüzdesini aşan satış siparişi satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="f58f8-131">On the **Sales order lines** tab, select the sales order line for the item that exceeds the over-delivery percentage.</span></span>
1. <span data-ttu-id="f58f8-132"> *\*Satır ayrıntıları** sekmesinde, *\*Teslimatı*\*'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f58f8-132">On the  **Line details** tab, select **Delivery**.</span></span>
1. <span data-ttu-id="f58f8-133">**Fazla teslimat** alanını, sevk irsaliyesi oluşturma işleminin devam edebilmesi için, yük miktarına karşı çekilen miktara uygun olması için daha yüksek bir yüzdeye ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f58f8-133">Set the **Overdelivery** field to a larger percentage that accommodates the quantity that was picked against the load quantity, so that packing slip generation can proceed.</span></span>

### <a name="reverse-and-make-adjustments"></a><span data-ttu-id="f58f8-134">Tersine çevirme ve ayarlamalar yapma</span><span class="sxs-lookup"><span data-stu-id="f58f8-134">Reverse and make adjustments</span></span>

<span data-ttu-id="f58f8-135">Yük için deftere nakledilen her şeyi tersine çevirin (örneğin, sevk irsaliyesi, sevk irsaliyesi onayı ve iş), satış siparişi ayarlamaları yapın, siparişi ambara yeniden serbest bırakın ve sevkiyat yordamını tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="f58f8-135">Reverse everything that has been posted for the load (for example, the packing slip, shipment confirmation, and work), make sales order adjustments, re-release the order to the warehouse, and complete the shipment procedure.</span></span>

<span data-ttu-id="f58f8-136">Sevk irsaliyesini iptal etmek için aşağıdaki yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="f58f8-136">Use the following procedure to cancel a packing slip.</span></span>

1. <span data-ttu-id="f58f8-137">**Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="f58f8-137">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="f58f8-138">Eylem Bölmesi'nde,  **Sevk ve teslim alma** sekmesinin  **Tersine çevir** grubunda  **Sevk irsaliyelerini iptal et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f58f8-138">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Cancel packing slips**.</span></span>

<span data-ttu-id="f58f8-139">Sevkiyat onayını tersine çevirmek için aşağıdaki yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="f58f8-139">Use the following procedure to reverse a shipment confirmation.</span></span>

1. <span data-ttu-id="f58f8-140">**Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="f58f8-140">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="f58f8-141">Eylem Bölmesi'nde,  **Sevk ve teslim alma** sekmesinin  **Tersine çevir** grubunda  **Sevkiyat onayını tersine çevir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f58f8-141">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>

<span data-ttu-id="f58f8-142">İşi tersine çevirmek için aşağıdaki yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="f58f8-142">Use the following procedure to reverse work.</span></span>

1. <span data-ttu-id="f58f8-143">**Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="f58f8-143">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="f58f8-144">Eylem Bölmesinde  **Yükler** sekmesindeki  **İş** grubunda  **İşi tersine çevir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f58f8-144">On the Action Pane, on the **Loads** tab, in the **Work** group, select **Reverse work**.</span></span>
