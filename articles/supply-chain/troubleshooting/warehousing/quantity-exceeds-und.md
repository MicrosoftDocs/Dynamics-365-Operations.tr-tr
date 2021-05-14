---
title: Miktar, eksik teslimat yüzdesini aştığından sevkiyatı onaylayamazsınız
description: Miktar, eksik teslimat yüzdesini aştığından sevkiyatı onaylayamazsınız
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5339b9d800f7454e2a00c230a8d5deca3979c074
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938565"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-underdelivery-percentage"></a><span data-ttu-id="208a9-103">Miktar, eksik teslimat yüzdesini aştığından sevkiyatı onaylayamazsınız</span><span class="sxs-lookup"><span data-stu-id="208a9-103">You can't confirm a shipment because the quantity exceeds the underdelivery percentage</span></span>

<span data-ttu-id="208a9-104">Hata kodu: WAX1687</span><span class="sxs-lookup"><span data-stu-id="208a9-104">Error code: WAX1687</span></span>

## <a name="symptoms"></a><span data-ttu-id="208a9-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="208a9-105">Symptoms</span></span>

<span data-ttu-id="208a9-106">Bir sevkiyatı onaylamaya çalıştığınızda, sistem aşağıdaki hata iletisini gösterir:</span><span class="sxs-lookup"><span data-stu-id="208a9-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="208a9-107">%2 maddesinin miktarı eksik teslimat için tanımlanan yüzdeyi aştığından %1 yükü için sevkiyat onaylanamadı.</span><span class="sxs-lookup"><span data-stu-id="208a9-107">The shipment for load %1 could not be confirmed because the quantity for item %2 exceeds the percentage that is defined for underdelivery.</span></span>

<span data-ttu-id="208a9-108">Bu nedenle, yükleme için sevkiyat işlemini onaylayamazsınız.</span><span class="sxs-lookup"><span data-stu-id="208a9-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="208a9-109">Nedeni</span><span class="sxs-lookup"><span data-stu-id="208a9-109">Cause</span></span>

<span data-ttu-id="208a9-110">Yük veya sevkiyat miktarı yalnızca kısmen çekildi.</span><span class="sxs-lookup"><span data-stu-id="208a9-110">The quantity of the load or shipment has been only partially picked.</span></span> <span data-ttu-id="208a9-111">Mevcut miktar, izin verilen eksik teslimat yüzdesi dışında kalan bir yüzdeyle çekilen miktarın altında.</span><span class="sxs-lookup"><span data-stu-id="208a9-111">The quantity is currently less than the picked quantity by a percentage that is outside the allowed underdelivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="208a9-112">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="208a9-112">Resolution</span></span>

<span data-ttu-id="208a9-113">Bu sorunu gidermek için aşağıdaki görevlerden birini tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="208a9-113">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="208a9-114">Yük satırı miktarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="208a9-114">Set the load line quantity.</span></span>
- <span data-ttu-id="208a9-115">Eksik teslimat yüzdesini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="208a9-115">Set the underdelivery percentage.</span></span>

### <a name="set-the-load-line-quantity"></a><span data-ttu-id="208a9-116">Yük satırı miktarını ayarlayın</span><span class="sxs-lookup"><span data-stu-id="208a9-116">Set the load line quantity</span></span>

<span data-ttu-id="208a9-117">Yük satırı miktarını ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="208a9-117">To set the load line quantity, follow these steps.</span></span>

1. <span data-ttu-id="208a9-118">**Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="208a9-118">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="208a9-119">Sevkiyatın onaylanamadığı ilgili yükü seçin.</span><span class="sxs-lookup"><span data-stu-id="208a9-119">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="208a9-120">**Yük satırları** hızlı sekmesinde, eksik teslimat yüzdesini aşan maddenin yük satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="208a9-120">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="208a9-121">**Satır ayrıntıları** hızlı sekmesinde, **Sipariş**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="208a9-121">On the **Line details** FastTab, select **Order**.</span></span>
1. <span data-ttu-id="208a9-122">**Miktar** alanında, sevkiyat onayının gerçekleşmesi için değeri çekilen miktara (yani **Oluşturulan çalışma miktarı** değerine) ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="208a9-122">In the **Quantity** field, set the value to the picked quantity (that is, to the **Work created quantity** value), so that shipment confirmation can occur.</span></span>

### <a name="set-the-underdelivery-percentage"></a><span data-ttu-id="208a9-123">Eksik teslimat yüzdesini ayarlayın</span><span class="sxs-lookup"><span data-stu-id="208a9-123">Set the underdelivery percentage</span></span>

<span data-ttu-id="208a9-124">eksik teslimat yüzdesini ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="208a9-124">To set the underdelivery percentage, follow these steps.</span></span>

1. <span data-ttu-id="208a9-125">**Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="208a9-125">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="208a9-126">Sevkiyatın onaylanamadığı ilgili yükü seçin.</span><span class="sxs-lookup"><span data-stu-id="208a9-126">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="208a9-127">**Yük satırları** hızlı sekmesinde, eksik teslimat yüzdesini aşan maddenin yük satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="208a9-127">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="208a9-128">**Satır ayrıntıları** hızlı sekmesinde, **Genel**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="208a9-128">On the **Line details** FastTab, select **General**.</span></span>
1. <span data-ttu-id="208a9-129">**eksik teslimat** alanında, sevkiyat onayının gerçekleşmesi için, değeri yük miktarına göre çekilen miktardan daha büyük bir yüzdeye ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="208a9-129">In the **Underdelivery** field, set the value to a larger percentage that accommodates the quantity that has been picked against the load quantity, so that shipment confirmation can occur.</span></span>
