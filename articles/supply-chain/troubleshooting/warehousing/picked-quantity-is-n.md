---
title: Sevk irsaliyesi oluşturma sırasında çekilen miktar yeterli değil
description: Sevk irsaliyesi oluşturduğunuzda giden yük, yük satırında oluşturulan iş miktarıyla eşleşmeyen bir çekilen miktar içerir.
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
ms.openlocfilehash: fa6054dc26e4306ec16e37b0e6c320342ed40fe0
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249186"
---
# <a name="picked-quantity-isnt-sufficient-during-packing-slip-generation"></a><span data-ttu-id="6dfed-103">Sevk irsaliyesi oluşturma sırasında çekilen miktar yeterli değil</span><span class="sxs-lookup"><span data-stu-id="6dfed-103">Picked quantity isn't sufficient during packing slip generation</span></span>

<span data-ttu-id="6dfed-104">Hata kodu: SYS54073</span><span class="sxs-lookup"><span data-stu-id="6dfed-104">Error code: SYS54073</span></span>

## <a name="symptoms"></a><span data-ttu-id="6dfed-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="6dfed-105">Symptoms</span></span>

<span data-ttu-id="6dfed-106">Sevk irsaliyesi oluşturduğunuzda giden yük, yük satırında oluşturulan iş miktarıyla eşleşmeyen bir çekilen miktar içerir.</span><span class="sxs-lookup"><span data-stu-id="6dfed-106">When you generate a packing slip, the outbound load contains a picked quantity that doesn't match the created work quantity on the load line.</span></span>

<span data-ttu-id="6dfed-107">Sevk irsaliyesi oluşturmaya çalıştığınızda, sistem aşağıdaki hata iletisini gösterir:</span><span class="sxs-lookup"><span data-stu-id="6dfed-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="6dfed-108">%1 çekilmiş olduğundan ve buna bağlı bakiyenin %3 olması gerektiğinden, %2 güncelleştirmesi için yeterli değil.</span><span class="sxs-lookup"><span data-stu-id="6dfed-108">As %1 have been picked, it is not sufficient to update %2, when, subsequently, the remainder must be %3.</span></span>

<span data-ttu-id="6dfed-109">Bu nedenle, yükleme için sevk irsaliyesi oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="6dfed-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="6dfed-110">Nedeni</span><span class="sxs-lookup"><span data-stu-id="6dfed-110">Cause</span></span>

<span data-ttu-id="6dfed-111">Aşağıdaki koşullardan biri mevcut olduğu için sevk irsaliyesi oluşturulamıyor:</span><span class="sxs-lookup"><span data-stu-id="6dfed-111">The packing slip can't be generated in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="6dfed-112">İlgili iş henüz teslim alınmadı ve son sevkiyat konumuna taşınmadı.</span><span class="sxs-lookup"><span data-stu-id="6dfed-112">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="6dfed-113">Teslim alınan iş miktarı, yükleme satırında oluşturulan iş miktarıyla eşleşmiyor.</span><span class="sxs-lookup"><span data-stu-id="6dfed-113">The picked work quantity doesn't match the created work quantity on the load line.</span></span>
- <span data-ttu-id="6dfed-114">Yük satırı miktarı, işin oluşturduğu miktar ve çekilen miktar eşleşmiyor.</span><span class="sxs-lookup"><span data-stu-id="6dfed-114">The load line quantity, work created quantity, and picked quantity don't match.</span></span>

## <a name="resolution"></a><span data-ttu-id="6dfed-115">Çözüm</span><span class="sxs-lookup"><span data-stu-id="6dfed-115">Resolution</span></span>

<span data-ttu-id="6dfed-116">Yükleme veya sevkiyat işlemi şu anda sevk irsaliyesi oluşturmanın başarısız olduğu bir durumdadır.</span><span class="sxs-lookup"><span data-stu-id="6dfed-116">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="6dfed-117">Bu sorunu gidermek için aşağıdaki görevlerden birini tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="6dfed-117">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="6dfed-118">Yük satırlarınızı gözden geçirin ve tüm ilgili işlerin son sevkiyat konumunda tamamlandığından ve miktarların aynı olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="6dfed-118">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="6dfed-119">Yük satırı miktarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="6dfed-119">Adjust the load line quantity.</span></span>
- <span data-ttu-id="6dfed-120">Tüm çekme kayıtlarını tersine çevirin ve çekme işlemini yineleyin.</span><span class="sxs-lookup"><span data-stu-id="6dfed-120">Reverse all pick registrations, and redo picking.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="6dfed-121">Yük satırlarınızı gözden geçirin ve tüm ilgili işlerin son sevkiyat konumunda tamamlandığından ve miktarların aynı olduğundan emin olun</span><span class="sxs-lookup"><span data-stu-id="6dfed-121">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="6dfed-122">Yük satırlarınızı gözden geçirmek için aşağıdaki yordamı kullanın ve tüm ilgili işlerin son sevkiyat konumunda tamamlandığından ve miktarların aynı olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="6dfed-122">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="6dfed-123">**Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="6dfed-123">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="6dfed-124">Sevk irsaliyesinin oluşturulamadığı yükü seçin.</span><span class="sxs-lookup"><span data-stu-id="6dfed-124">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="6dfed-125">**Yük satırları** hızlı sekmesinde, yük satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="6dfed-125">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="6dfed-126">**Oluşturulan iş miktarı** alanının değerini not alın.</span><span class="sxs-lookup"><span data-stu-id="6dfed-126">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="6dfed-127">Eylem Bölmesinde **Yüklemeler** sekmesindeki **İlgili bilgiler** grubunda **Çalışma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="6dfed-127">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="6dfed-128">İşin son sevkiyat konumunda tamamlandığını ve teslim alınan iş miktarının yükleme satırındaki oluşturulan iş miktarıyla eşleştiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="6dfed-128">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="6dfed-129">Tüm ölçütlerin karşılandığından emin olmak için bu prosedürü tüm yükleme satırları için yineleyin.</span><span class="sxs-lookup"><span data-stu-id="6dfed-129">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="6dfed-130">Yük satırı miktarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="6dfed-130">Adjust the load line quantity</span></span>

<span data-ttu-id="6dfed-131">Yük satırı miktarını ayarlamak için aşağıdaki yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="6dfed-131">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="6dfed-132">**Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="6dfed-132">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="6dfed-133">Sevk irsaliyesinin oluşturulamadığı yükü seçin.</span><span class="sxs-lookup"><span data-stu-id="6dfed-133">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="6dfed-134">Eylem Bölmesi'nde,  **Sevk ve teslim alma** sekmesinin  **Tersine çevir** grubunda  **Sevkiyat onayını tersine çevir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6dfed-134">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="6dfed-135"> *\*Yük satırları** sekmesinde, soruna neden olan maddenin yük satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="6dfed-135">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="6dfed-136">Çekilen miktarı ayarlamak için **Çekilen miktarı düş**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="6dfed-136">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="6dfed-137">Yük satırındaki ayarlamaları yansıtacak şekilde **Yük satırını azalt** alanını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6dfed-137">Set the **Reduce load line** field to reflect adjustments on the load line.</span></span>

### <a name="reverse-all-pick-registrations-and-redo-picking"></a><span data-ttu-id="6dfed-138">Tüm çekme kayıtlarını tersine çevirme ve çekme işlemini yineleme</span><span class="sxs-lookup"><span data-stu-id="6dfed-138">Reverse all pick registrations, and redo picking</span></span>

<span data-ttu-id="6dfed-139">Sorun, birisi iş olmayan yük satırını kapatmak için çekme kaydı kullandığını için oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="6dfed-139">The issue might occur because someone used pick registration to close a load line without work.</span></span> <span data-ttu-id="6dfed-140">Bu durumda, el ile çekme kaydı tersine çevrilmeli ve çekme işlemi Warehouse Management mobil uygulaması kullanılarak tamamlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6dfed-140">In this case, manual pick registration must be reversed, and picking must then be completed by using the Warehouse Management mobile app.</span></span>

<span data-ttu-id="6dfed-141">Çekme kaydını tersine çevirmek için aşağıdaki yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="6dfed-141">Use the following procedure to reverse the pick registration.</span></span>

1. <span data-ttu-id="6dfed-142">**Alacak hesapları \> Siparişler \> Tüm siparişler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="6dfed-142">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="6dfed-143">Yük için sevk irsaliyesini deftere nakledemeyeceğiniz satış siparişini seçin.</span><span class="sxs-lookup"><span data-stu-id="6dfed-143">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="6dfed-144"> *\*Satış siparişi satırları** sekmesinde, çekme kaydının yapıldığı satış siparişi satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="6dfed-144">On the **Sales order lines** tab, select the sales order line that pick registration was done for.</span></span>
1. <span data-ttu-id="6dfed-145">Madde çekmeyi iptal etmek için **Satırı güncelleştir \> Çek**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6dfed-145">Select **Update line \> Pick** to unpick the items.</span></span>
