---
title: Fiziksel güncelleştirme miktarının ondalık yuvarlaması hatalı
description: Sevk irsaliyesi oluşturduğunuzda giden yük, birimde tanımlanan ondalık hassasiyetle eşleşmeyen bir miktar içeriyor.
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
ms.openlocfilehash: 1e63440834f516879aa8ad711bd789e62b0ee993
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248809"
---
# <a name="decimal-rounding-of-the-physical-updating-quantity-is-incorrect"></a><span data-ttu-id="cd264-103">Fiziksel güncelleştirme miktarının ondalık yuvarlaması hatalı</span><span class="sxs-lookup"><span data-stu-id="cd264-103">Decimal rounding of the physical updating quantity is incorrect</span></span>

<span data-ttu-id="cd264-104">Hata kodu: SYS19589</span><span class="sxs-lookup"><span data-stu-id="cd264-104">Error code: SYS19589</span></span>

## <a name="symptoms"></a><span data-ttu-id="cd264-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="cd264-105">Symptoms</span></span>

<span data-ttu-id="cd264-106">Sevk irsaliyesi oluşturduğunuzda giden yük, birimde tanımlanan ondalık hassasiyetle eşleşmeyen bir miktar içeriyor.</span><span class="sxs-lookup"><span data-stu-id="cd264-106">When you generate a packing slip, the outbound load contains a quantity that doesn't match the decimal precision that is defined in the unit.</span></span>

<span data-ttu-id="cd264-107">Sevk irsaliyesi oluşturmaya çalıştığınızda, sistem aşağıdaki hata iletisini gösterir:</span><span class="sxs-lookup"><span data-stu-id="cd264-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="cd264-108">%1 birimi cinsinden fiziksel güncelleştirme miktarıyla ilgili ondalık yuvarlama işlemi yanlış.</span><span class="sxs-lookup"><span data-stu-id="cd264-108">Decimal rounding of the physical updating quantity in the unit %1 is incorrect.</span></span>

<span data-ttu-id="cd264-109">Bu nedenle, yükleme için sevk irsaliyesi oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="cd264-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="cd264-110">Nedeni</span><span class="sxs-lookup"><span data-stu-id="cd264-110">Cause</span></span>

<span data-ttu-id="cd264-111">Sistem, sevkiyat miktarını ondalık yuvarlamasının sevkiyat birimi için tanımlanan ondalık hassasiyetle uygun olup olmadığını değerlendirir.</span><span class="sxs-lookup"><span data-stu-id="cd264-111">The system evaluates whether the decimal rounding of the shipping quantity corresponds to the decimal precision that is defined for the shipping unit.</span></span> <span data-ttu-id="cd264-112">Sistem sevkiyat miktarını belirtilen ondalık basamak sayısına yuvarladığında, yuvarlanan sevkiyat miktarının gerçek sevkiyat miktarıyla eşleşmediğini tespit ederse, sevk irsaliyesini oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="cd264-112">When the system rounds the shipping quantity to the specified number of decimal places, if it finds that the rounded shipping quantity doesn't match the actual shipping quantity, you can't generate the packing slip.</span></span> <span data-ttu-id="cd264-113">Örneğin, satış miktarı 1,75 kilogram (kg) ise, ancak ondalık duyarlık *1* olarak ayarlanmışsa, bu sorun oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="cd264-113">For example, this issue might occur if the sales quantity is 1.75 kilograms (kg), but the decimal precision is set to *1*.</span></span>

## <a name="resolution"></a><span data-ttu-id="cd264-114">Çözüm</span><span class="sxs-lookup"><span data-stu-id="cd264-114">Resolution</span></span>

<span data-ttu-id="cd264-115">Yükleme veya sevkiyat işlemi şu anda sevk irsaliyesi oluşturmanın başarısız olduğu bir durumdadır.</span><span class="sxs-lookup"><span data-stu-id="cd264-115">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="cd264-116">Bu sorunu gidermek için aşağıdaki görevlerden birini tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="cd264-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="cd264-117">Yük satırlarını gözden geçirin ve miktarın ondalık sayılar veya yuvarlama sorunları olmadan net bir şekilde dönüştürülebilmesini sağlamak için ayarlamalar yapın.</span><span class="sxs-lookup"><span data-stu-id="cd264-117">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues.</span></span>
- <span data-ttu-id="cd264-118">Yük satırlarınızı gözden geçirin ve birim ve miktarın birimin ondalık duyarlığıyla uyumlu hale getirilmesini sağlamak için ayarlamalar yapın.</span><span class="sxs-lookup"><span data-stu-id="cd264-118">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-decimal-numbers-and-any-other-rounding-issues"></a><span data-ttu-id="cd264-119">Yük satırlarını gözden geçirin ve miktarın ondalık sayılar veya yuvarlama sorunları olmadan net bir şekilde dönüştürülebilmesini sağlamak için ayarlamalar yapın</span><span class="sxs-lookup"><span data-stu-id="cd264-119">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues</span></span>

<span data-ttu-id="cd264-120">Yük satırlarını gözden geçirmek için aşağıdaki yordamı kullanın ve miktarın ondalık sayılar veya yuvarlama sorunları olmadan net bir şekilde dönüştürülebilmesini sağlamak için ayarlamalar yapın.</span><span class="sxs-lookup"><span data-stu-id="cd264-120">Use the following procedure to review your load lines and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues.</span></span>

1. <span data-ttu-id="cd264-121">**Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="cd264-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="cd264-122">Sevk irsaliyesinin oluşturulamadığı yükü seçin.</span><span class="sxs-lookup"><span data-stu-id="cd264-122">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="cd264-123">Eylem Bölmesi'nde,  **Sevk ve teslim alma** sekmesinin  **Tersine çevir** grubunda  **Sevkiyat onayını tersine çevir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="cd264-123">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="cd264-124"> *\*Yük satırları** sekmesinde, soruna neden olan maddenin yük satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="cd264-124">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="cd264-125">Çekilen miktarı ayarlamak için **Çekilen miktarı düş**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="cd264-125">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="cd264-126"> *\*Satır ayrıntıları** sekmesinde, *\*Sipariş*\*'i seçin.</span><span class="sxs-lookup"><span data-stu-id="cd264-126">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="cd264-127">Sevk irsaliyesi oluşturma işleminin devam edebilmesi için **Miktar** alanını çekilen miktara (yani **İşle oluşturulan miktar** alanının değerine) ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="cd264-127">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a><span data-ttu-id="cd264-128">Yük satırlarınızı gözden geçirin ve birim ve miktarın birimin ondalık duyarlığıyla uyumlu hale getirilmesini sağlamak için ayarlamalar yapın</span><span class="sxs-lookup"><span data-stu-id="cd264-128">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit</span></span>

<span data-ttu-id="cd264-129">Yük satırlarınızı gözden geçirmek için aşağıdaki yordamı kullanın ve birim ve miktarın birimin ondalık duyarlığıyla uyumlu hale getirilmesini sağlamak için ayarlamalar yapın.</span><span class="sxs-lookup"><span data-stu-id="cd264-129">Use the following procedure to review your load lines and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

1. <span data-ttu-id="cd264-130">**Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="cd264-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="cd264-131">Sevk irsaliyesinin oluşturulamadığı yükü seçin.</span><span class="sxs-lookup"><span data-stu-id="cd264-131">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="cd264-132">**Yük satırları** hızlı sekmesinde, soruna neden olan maddenin yük satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="cd264-132">On the **Load lines** FastTab, select the load line for the item that causes an issue.</span></span> <span data-ttu-id="cd264-133">**Miktar** ve **Birim** alanlarının değerini not alın.</span><span class="sxs-lookup"><span data-stu-id="cd264-133">Make a note of the value of the **Quantity** and **Unit** fields.</span></span>
1. <span data-ttu-id="cd264-134">**Kuruluş yönetimi \> Birimler \> Birimler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="cd264-134">Go to **Organization administration \> Units \> Units**.</span></span>
1. <span data-ttu-id="cd264-135">Sevk irsaliyesinin oluşturulamadığı birimi seçin.</span><span class="sxs-lookup"><span data-stu-id="cd264-135">Select the unit that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="cd264-136">**Ondalık duyarlık** alanının değerini gerektiği gibi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="cd264-136">Adjust the value of the **Decimal precision** field as required.</span></span>
