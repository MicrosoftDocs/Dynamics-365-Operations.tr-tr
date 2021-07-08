---
title: Güncelleştirmeye çalıştığınız miktar alınan/teslim edilen miktarı aşıyor.
description: Sevk irsaliyesi oluşturduğunuzda giden yük, satış siparişi için çekilen ve rezerve edilen iş miktarını aşan bir miktar içeriyor.
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
ms.openlocfilehash: 66d9cd80cc61e00d1d88ab4f59d03054d746cdd9
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249187"
---
# <a name="quantity-that-youre-trying-to-update-exceeds-the-receiveddelivered-quantity"></a><span data-ttu-id="83d83-103">Güncelleştirmeye çalıştığınız miktar alınan/teslim edilen miktarı aşıyor</span><span class="sxs-lookup"><span data-stu-id="83d83-103">Quantity that you're trying to update exceeds the received/delivered quantity</span></span>

<span data-ttu-id="83d83-104">Hata kodu: SYS7676</span><span class="sxs-lookup"><span data-stu-id="83d83-104">Error code: SYS7676</span></span>

## <a name="symptoms"></a><span data-ttu-id="83d83-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="83d83-105">Symptoms</span></span>

<span data-ttu-id="83d83-106">Sevk irsaliyesi oluşturduğunuzda giden yük, satış siparişi için çekilen ve rezerve edilen iş miktarını aşan bir miktar içeriyor.</span><span class="sxs-lookup"><span data-stu-id="83d83-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the work quantity that was picked and reserved for the sales order.</span></span>

<span data-ttu-id="83d83-107">Sevk irsaliyesi oluşturmaya çalıştığınızda, sistem aşağıdaki hata iletisini gösterir:</span><span class="sxs-lookup"><span data-stu-id="83d83-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="83d83-108">Güncelleştirmeye çalıştığınız miktar, alınan/teslim edilen miktarı aşıyor.</span><span class="sxs-lookup"><span data-stu-id="83d83-108">The quantity that you are trying to update exceeds the quantity received/delivered.</span></span>

<span data-ttu-id="83d83-109">Bu nedenle, yükleme için sevk irsaliyesi oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="83d83-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="83d83-110">Nedeni</span><span class="sxs-lookup"><span data-stu-id="83d83-110">Cause</span></span>

<span data-ttu-id="83d83-111">Teslim alınan iş miktarı, yükleme satırında oluşturulan iş miktarıyla eşleşmiyor.</span><span class="sxs-lookup"><span data-stu-id="83d83-111">The picked work quantity doesn't match the created work quantity on the load line.</span></span> <span data-ttu-id="83d83-112">Örneğin, yükleme satırı miktarı, oluşturulan iş miktarı veya çekilen miktar doğru değilse bu sorun oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="83d83-112">For example, this issue might occur if the load line quantity, work created quantity, or picked quantity isn't accurate.</span></span>

## <a name="resolution"></a><span data-ttu-id="83d83-113">Çözüm</span><span class="sxs-lookup"><span data-stu-id="83d83-113">Resolution</span></span>

<span data-ttu-id="83d83-114">Yükleme veya sevkiyat işlemi şu anda sevk irsaliyesi oluşturmanın başarısız olduğu bir durumdadır.</span><span class="sxs-lookup"><span data-stu-id="83d83-114">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="83d83-115">Bu sorunu gidermek için aşağıdaki görevlerden birini tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="83d83-115">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="83d83-116">Yük satırlarınızı gözden geçirin ve tüm ilgili işlerin son sevkiyat konumunda tamamlandığından ve miktarların aynı olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="83d83-116">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="83d83-117">Yük satırı miktarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="83d83-117">Adjust the load line quantity.</span></span>
- <span data-ttu-id="83d83-118">Tüm çekme kayıtlarını tersine çevirin ve çekme işlemini yineleyin.</span><span class="sxs-lookup"><span data-stu-id="83d83-118">Reverse all pick registrations, and redo picking.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="83d83-119">Yük satırlarınızı gözden geçirin ve tüm ilgili işlerin son sevkiyat konumunda tamamlandığından ve miktarların aynı olduğundan emin olun</span><span class="sxs-lookup"><span data-stu-id="83d83-119">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="83d83-120">Yük satırlarınızı gözden geçirmek için aşağıdaki yordamı kullanın ve tüm ilgili işlerin son sevkiyat konumunda tamamlandığından ve miktarların aynı olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="83d83-120">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="83d83-121">**Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="83d83-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="83d83-122">Sevkiyatın oluşturulamadığı ilgili yükü seçin.</span><span class="sxs-lookup"><span data-stu-id="83d83-122">Select the load that the shipment can't be generated for.</span></span>
1. <span data-ttu-id="83d83-123">**Yük satırları** hızlı sekmesinde, yük satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="83d83-123">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="83d83-124">**Oluşturulan iş miktarı** alanının değerini not alın.</span><span class="sxs-lookup"><span data-stu-id="83d83-124">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="83d83-125">Eylem Bölmesinde **Yüklemeler** sekmesindeki **İlgili bilgiler** grubunda **Çalışma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="83d83-125">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="83d83-126">İşin son sevkiyat konumunda tamamlandığını ve teslim alınan iş miktarının yükleme satırındaki oluşturulan iş miktarıyla eşleştiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="83d83-126">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="83d83-127">Tüm ölçütlerin karşılandığından emin olmak için bu prosedürü tüm yükleme satırları için yineleyin.</span><span class="sxs-lookup"><span data-stu-id="83d83-127">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="83d83-128">Yük satırı miktarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="83d83-128">Adjust the load line quantity</span></span>

<span data-ttu-id="83d83-129">Yük satırı miktarını ayarlamak için aşağıdaki yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="83d83-129">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="83d83-130">**Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="83d83-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="83d83-131">Sevk irsaliyesinin oluşturulamadığı yükü seçin.</span><span class="sxs-lookup"><span data-stu-id="83d83-131">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="83d83-132">Eylem Bölmesi'nde,  **Sevk ve teslim alma** sekmesinin  **Tersine çevir** grubunda  **Sevkiyat onayını tersine çevir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="83d83-132">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="83d83-133"> *\*Yük satırları** sekmesinde, soruna neden olan maddenin yük satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="83d83-133">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="83d83-134">Çekilen miktarı ayarlamak için **Çekilen miktarı düş**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="83d83-134">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="83d83-135">Yük satırındaki ayarlamaları yansıtacak şekilde **Yük satırını azalt** alanını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="83d83-135">Set the **Reduce load line** field to reflect adjustments on the load line.</span></span>

### <a name="reverse-all-pick-registrations-and-redo-picking"></a><span data-ttu-id="83d83-136">Tüm çekme kayıtlarını tersine çevirme ve çekme işlemini yineleme</span><span class="sxs-lookup"><span data-stu-id="83d83-136">Reverse all pick registrations, and redo picking</span></span>

<span data-ttu-id="83d83-137">Birisi bir yük satırını iş olmadan kapatmak için çekme kaydını kullandıysa, yük satırı miktarı ile çekilen miktar arasında bir tutarsızlık oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="83d83-137">If someone used pick registration to close a load line without work, a discrepancy can occur between the load line quantity and the picked quantity.</span></span> <span data-ttu-id="83d83-138">Bu durumda, el ile çekme kaydı tersine çevrilmeli ve çekme işlemi Warehouse Management mobil uygulaması kullanılarak tamamlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="83d83-138">In this case, manual pick registration must be reversed, and picking must then be completed by using the Warehouse Management mobile app.</span></span>

<span data-ttu-id="83d83-139">Çekme kaydını tersine çevirmek için aşağıdaki yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="83d83-139">Use the following procedure to reverse the pick registration.</span></span>

1. <span data-ttu-id="83d83-140">**Alacak hesapları \> Siparişler \> Tüm siparişler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="83d83-140">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="83d83-141">Yük için sevk irsaliyesini deftere nakledemeyeceğiniz satış siparişini seçin.</span><span class="sxs-lookup"><span data-stu-id="83d83-141">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="83d83-142"> *\*Satış siparişi satırları** sekmesinde, çekme kaydının yapıldığı satış siparişi satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="83d83-142">On the **Sales order lines** tab, select the sales order line that pick registration was done for.</span></span>
1. <span data-ttu-id="83d83-143">Madde çekmeyi iptal etmek için **Satırı güncelleştir \> Çek**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="83d83-143">Select **Update line \> Pick** to unpick the items.</span></span>
