---
title: Sevk irsaliyesi oluşturma sırasında miktar eksik teslimat yüzdesini aşıyor
description: Sevk irsaliyesi oluşturduğunuzda, giden yük eksik teslimat yüzdesini aşan bir miktar içerir.
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
ms.openlocfilehash: ecdd377d12faf40f64736e93671dcf42ff132403
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249182"
---
# <a name="quantity-exceeds-under-delivery-percentage-during-packing-slip-generation"></a><span data-ttu-id="b382d-103">Sevk irsaliyesi oluşturma sırasında miktar eksik teslimat yüzdesini aşıyor</span><span class="sxs-lookup"><span data-stu-id="b382d-103">Quantity exceeds under-delivery percentage during packing slip generation</span></span>

<span data-ttu-id="b382d-104">Hata kodu: SYS24921</span><span class="sxs-lookup"><span data-stu-id="b382d-104">Error code: SYS24921</span></span>

## <a name="symptoms"></a><span data-ttu-id="b382d-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="b382d-105">Symptoms</span></span>

<span data-ttu-id="b382d-106">Sevk irsaliyesi oluşturduğunuzda, giden yük eksik teslimat yüzdesini aşan bir miktar içerir.</span><span class="sxs-lookup"><span data-stu-id="b382d-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the under-delivery percentage.</span></span>

<span data-ttu-id="b382d-107">Sevk irsaliyesi oluşturmaya çalıştığınızda, sistem aşağıdaki hata iletisini gösterir:</span><span class="sxs-lookup"><span data-stu-id="b382d-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="b382d-108">Satırın eksik teslimat yüzdesi %1, ancak izin verilen eksik teslimat yüzdesi %2.</span><span class="sxs-lookup"><span data-stu-id="b382d-108">Underdelivery of line is %1 percent, but the allowed underdelivery is only %2 percent.</span></span>

<span data-ttu-id="b382d-109">Bu nedenle, yükleme için sevk irsaliyesi oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="b382d-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="b382d-110">Nedeni</span><span class="sxs-lookup"><span data-stu-id="b382d-110">Cause</span></span>

<span data-ttu-id="b382d-111">Yük veya sevkiyart için çekilen miktar sipariş edilen miktardan azdır ve eksik teslimat yüzdesi aralığında değildir.</span><span class="sxs-lookup"><span data-stu-id="b382d-111">The picked quantity for the load or shipment is less than the ordered quantity and isn't within the range of the under-delivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="b382d-112">Çözüm</span><span class="sxs-lookup"><span data-stu-id="b382d-112">Resolution</span></span>

<span data-ttu-id="b382d-113">Yükleme veya sevkiyat işlemi şu anda sevk irsaliyesi oluşturmanın başarısız olduğu bir durumdadır.</span><span class="sxs-lookup"><span data-stu-id="b382d-113">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="b382d-114">Bu sorunu gidermek için aşağıdaki görevlerden birini tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="b382d-114">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="b382d-115">Eksik teslimat yüzdesini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b382d-115">Adjust the under-delivery percentage.</span></span>
- <span data-ttu-id="b382d-116">Tersine çevirin ve ayarlamalar yapın.</span><span class="sxs-lookup"><span data-stu-id="b382d-116">Reverse and make adjustments.</span></span>

### <a name="adjust-the-under-delivery-percentage"></a><span data-ttu-id="b382d-117">Eksik teslimat yüzdesini ayarlama</span><span class="sxs-lookup"><span data-stu-id="b382d-117">Adjust the under-delivery percentage</span></span>

<span data-ttu-id="b382d-118">Eksik teslimat yüzdesini ayarlamak için aşağıdaki yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="b382d-118">Use the following procedure to adjust the under-delivery percentage.</span></span>

1. <span data-ttu-id="b382d-119">**Alacak hesapları \> Siparişler \> Tüm siparişler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="b382d-119">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="b382d-120">Yük için sevk irsaliyesini deftere nakledemeyeceğiniz satış siparişini seçin.</span><span class="sxs-lookup"><span data-stu-id="b382d-120">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="b382d-121"> *\*Satış siparişi satırları** sekmesinde, eksik teslimat yüzdesini aşan satış siparişi satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="b382d-121">On the **Sales order lines** tab, select the sales order line for the item that exceeds the under-delivery percentage.</span></span>
1. <span data-ttu-id="b382d-122"> *\*Satır ayrıntıları** sekmesinde, *\*Teslimatı*\*'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b382d-122">On the  **Line details** tab, select **Delivery**.</span></span>
1. <span data-ttu-id="b382d-123">**Eksik teslimat** alanını, sevk irsaliyesi oluşturma işleminin devam edebilmesi için, yük miktarına karşı çekilen miktara uygun olması için daha yüksek bir yüzdeye ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b382d-123">Set the **Underdelivery** field to a larger percentage that accommodates the quantity that was picked against the load quantity, so that packing slip generation can proceed.</span></span>

### <a name="reverse-and-make-adjustments"></a><span data-ttu-id="b382d-124">Tersine çevirme ve ayarlamalar yapma</span><span class="sxs-lookup"><span data-stu-id="b382d-124">Reverse and make adjustments</span></span>

<span data-ttu-id="b382d-125">Yük için deftere nakledilen her şeyi tersine çevirin (örneğin, sevk irsaliyesi, sevk irsaliyesi onayı ve iş), satış siparişi ayarlamaları yapın, siparişi ambara yeniden serbest bırakın ve sevkiyat yordamını tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="b382d-125">Reverse everything that has been posted for the load (for example, the packing slip, shipment confirmation, and work), make sales order adjustments, re-release the order to the warehouse, and complete the shipment procedure.</span></span>

<span data-ttu-id="b382d-126">Sevk irsaliyesini iptal etmek için aşağıdaki yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="b382d-126">Use the following procedure to cancel a packing slip.</span></span>

1. <span data-ttu-id="b382d-127">**Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="b382d-127">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="b382d-128">Eylem Bölmesi'nde,  **Sevk ve teslim alma** sekmesinin  **Tersine çevir** grubunda  **Sevk irsaliyelerini iptal et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b382d-128">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Cancel packing slips**.</span></span>

<span data-ttu-id="b382d-129">Sevkiyat onayını tersine çevirmek için aşağıdaki yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="b382d-129">Use the following procedure to reverse a shipment confirmation.</span></span>

1. <span data-ttu-id="b382d-130">**Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="b382d-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="b382d-131">Eylem Bölmesi'nde,  **Sevk ve teslim alma** sekmesinin  **Tersine çevir** grubunda  **Sevkiyat onayını tersine çevir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b382d-131">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>

<span data-ttu-id="b382d-132">İşi tersine çevirmek için aşağıdaki yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="b382d-132">Use the following procedure to reverse work.</span></span>

1. <span data-ttu-id="b382d-133">**Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="b382d-133">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="b382d-134">Eylem Bölmesinde  **Yükler** sekmesindeki  **İş** grubunda  **İşi tersine çevir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b382d-134">On the Action Pane, on the **Loads** tab, in the **Work** group, select **Reverse work**.</span></span>
