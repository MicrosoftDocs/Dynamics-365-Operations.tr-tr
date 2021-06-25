---
title: Miktar, eksik teslimat yüzdesini aştığından sevkiyatı onaylayamazsınız
description: Miktar, eksik teslimat yüzdesini aştığından sevkiyatı onaylayamazsınız
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm,WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 625003731485329b93f5f9454ccece580c889613
ms.sourcegitcommit: c2c6d687a89bc1534c029109315c23e92865b63b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/31/2021
ms.locfileid: "6123831"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-underdelivery-percentage"></a><span data-ttu-id="890c8-103">Miktar, eksik teslimat yüzdesini aştığından sevkiyatı onaylayamazsınız</span><span class="sxs-lookup"><span data-stu-id="890c8-103">You can't confirm a shipment because the quantity exceeds the underdelivery percentage</span></span>

<span data-ttu-id="890c8-104">Hata kodu: WAX1686</span><span class="sxs-lookup"><span data-stu-id="890c8-104">Error code: WAX1686</span></span>

## <a name="symptoms"></a><span data-ttu-id="890c8-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="890c8-105">Symptoms</span></span>

<span data-ttu-id="890c8-106">Bir sevkiyatı onaylamaya çalıştığınızda, sistem aşağıdaki hata iletisini gösterir:</span><span class="sxs-lookup"><span data-stu-id="890c8-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="890c8-107">%2 maddesinin miktarı eksik teslimat için tanımlanan yüzdeyi aştığından %1 yükü için sevkiyat onaylanamadı.</span><span class="sxs-lookup"><span data-stu-id="890c8-107">The shipment for load %1 could not be confirmed because the quantity for item %2 exceeds the percentage that is defined for underdelivery.</span></span>

<span data-ttu-id="890c8-108">Bu nedenle, yükleme için sevkiyat işlemini onaylayamazsınız.</span><span class="sxs-lookup"><span data-stu-id="890c8-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="890c8-109">Nedeni</span><span class="sxs-lookup"><span data-stu-id="890c8-109">Cause</span></span>

<span data-ttu-id="890c8-110">Yük veya sevkiyat miktarı yalnızca kısmen çekildi.</span><span class="sxs-lookup"><span data-stu-id="890c8-110">The quantity of the load or shipment has been only partially picked.</span></span> <span data-ttu-id="890c8-111">Mevcut miktar, izin verilen eksik teslimat yüzdesi dışında kalan bir yüzdeyle çekilen miktarın altında.</span><span class="sxs-lookup"><span data-stu-id="890c8-111">The quantity is currently less than the picked quantity by a percentage that is outside the allowed underdelivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="890c8-112">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="890c8-112">Resolution</span></span>

<span data-ttu-id="890c8-113">Bu sorunu gidermek için aşağıdaki görevlerden birini tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="890c8-113">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="890c8-114">Yük satırı miktarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="890c8-114">Set the load line quantity.</span></span>
- <span data-ttu-id="890c8-115">Eksik teslimat yüzdesini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="890c8-115">Set the underdelivery percentage.</span></span>

### <a name="set-the-load-line-quantity"></a><span data-ttu-id="890c8-116">Yük satırı miktarını ayarlayın</span><span class="sxs-lookup"><span data-stu-id="890c8-116">Set the load line quantity</span></span>

<span data-ttu-id="890c8-117">Yük satırı miktarını ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="890c8-117">To set the load line quantity, follow these steps.</span></span>

1. <span data-ttu-id="890c8-118">**Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="890c8-118">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="890c8-119">Sevkiyatın onaylanamadığı ilgili yükü seçin.</span><span class="sxs-lookup"><span data-stu-id="890c8-119">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="890c8-120">**Yük satırları** hızlı sekmesinde, eksik teslimat yüzdesini aşan maddenin yük satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="890c8-120">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="890c8-121">**Satır ayrıntıları** hızlı sekmesinde, **Sipariş**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="890c8-121">On the **Line details** FastTab, select **Order**.</span></span>
1. <span data-ttu-id="890c8-122">**Miktar** alanında, sevkiyat onayının gerçekleşmesi için değeri çekilen miktara (yani **Oluşturulan çalışma miktarı** değerine) ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="890c8-122">In the **Quantity** field, set the value to the picked quantity (that is, to the **Work created quantity** value), so that shipment confirmation can occur.</span></span>

### <a name="set-the-underdelivery-percentage"></a><span data-ttu-id="890c8-123">Eksik teslimat yüzdesini ayarlayın</span><span class="sxs-lookup"><span data-stu-id="890c8-123">Set the underdelivery percentage</span></span>

<span data-ttu-id="890c8-124">eksik teslimat yüzdesini ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="890c8-124">To set the underdelivery percentage, follow these steps.</span></span>

1. <span data-ttu-id="890c8-125">**Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="890c8-125">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="890c8-126">Sevkiyatın onaylanamadığı ilgili yükü seçin.</span><span class="sxs-lookup"><span data-stu-id="890c8-126">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="890c8-127">**Yük satırları** hızlı sekmesinde, eksik teslimat yüzdesini aşan maddenin yük satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="890c8-127">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="890c8-128">**Satır ayrıntıları** hızlı sekmesinde, **Genel**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="890c8-128">On the **Line details** FastTab, select **General**.</span></span>
1. <span data-ttu-id="890c8-129">**eksik teslimat** alanında, sevkiyat onayının gerçekleşmesi için, değeri yük miktarına göre çekilen miktardan daha büyük bir yüzdeye ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="890c8-129">In the **Underdelivery** field, set the value to a larger percentage that accommodates the quantity that has been picked against the load quantity, so that shipment confirmation can occur.</span></span>
