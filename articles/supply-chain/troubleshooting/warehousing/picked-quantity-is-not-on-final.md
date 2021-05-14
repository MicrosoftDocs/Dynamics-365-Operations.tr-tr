---
title: Teslim alınmadığı için sevkiyatı onaylayamazsınız
description: Teslim alınmadığı için sevkiyatı onaylayamazsınız
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
ms.openlocfilehash: 23a517e7769dc86ebec30e4f17c62172a6ad8801
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938567"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a><span data-ttu-id="7f826-103">Teslim alınmadığı için sevkiyatı onaylayamazsınız</span><span class="sxs-lookup"><span data-stu-id="7f826-103">You can't confirm a shipment because items haven't been picked</span></span>

<span data-ttu-id="7f826-104">Hata kodu: LoadNotPickedAndMovedToFinalShippingLocation</span><span class="sxs-lookup"><span data-stu-id="7f826-104">Error code: LoadNotPickedAndMovedToFinalShippingLocation</span></span>

## <a name="symptoms"></a><span data-ttu-id="7f826-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="7f826-105">Symptoms</span></span>

<span data-ttu-id="7f826-106">Bir sevkiyatı onaylamaya çalıştığınızda, sistem aşağıdaki hata iletisini gösterir:</span><span class="sxs-lookup"><span data-stu-id="7f826-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="7f826-107">%1 yükü için ihtiyaç duyulan maddelerin bazıları henüz çekilmedi ve son sevkiyat konumuna taşındı.</span><span class="sxs-lookup"><span data-stu-id="7f826-107">Some of the items that are needed for load %1 have not yet been picked and moved to the final shipping location.</span></span>

<span data-ttu-id="7f826-108">Bu nedenle, yükleme için sevkiyat işlemini onaylayamazsınız.</span><span class="sxs-lookup"><span data-stu-id="7f826-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="7f826-109">Nedeni</span><span class="sxs-lookup"><span data-stu-id="7f826-109">Cause</span></span>

<span data-ttu-id="7f826-110">Aşağıdaki koşullardan biri mevcut olduğu için yük veya sevkiyat mevcut durumunda onaylanamıyor:</span><span class="sxs-lookup"><span data-stu-id="7f826-110">The load or shipment can't be confirmed in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="7f826-111">İlgili iş henüz teslim alınmadı ve son sevkiyat konumuna taşınmadı.</span><span class="sxs-lookup"><span data-stu-id="7f826-111">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="7f826-112">Teslim alınan iş miktarı, yükleme satırında oluşturulan iş miktarıyla eşleşmiyor.</span><span class="sxs-lookup"><span data-stu-id="7f826-112">The picked work quantity doesn't match the created work quantity on the load line.</span></span>

## <a name="resolution"></a><span data-ttu-id="7f826-113">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="7f826-113">Resolution</span></span>

<span data-ttu-id="7f826-114">İlgili satış siparişlerini veya yükleme ya da sevkiyat için transfer emirlerini denetleyin.</span><span class="sxs-lookup"><span data-stu-id="7f826-114">Check the related sales orders or transfer orders for the load or shipment.</span></span> <span data-ttu-id="7f826-115">Tüm ilgili işlerin son sevkiyat konumunda tamamlandığından ve miktarların aynı olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="7f826-115">Make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="7f826-116">**Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="7f826-116">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="7f826-117">Sevkiyatın onaylanamadığı ilgili yükü seçin.</span><span class="sxs-lookup"><span data-stu-id="7f826-117">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="7f826-118">**Yük satırları** hızlı sekmesinde, yük satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="7f826-118">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="7f826-119">**Oluşturulan iş miktarı** alanının değerini not alın.</span><span class="sxs-lookup"><span data-stu-id="7f826-119">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="7f826-120">Eylem Bölmesinde **Yüklemeler** sekmesindeki **İlgili bilgiler** grubunda **Çalışma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="7f826-120">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="7f826-121">İşin son sevkiyat konumunda tamamlandığını ve teslim alınan iş miktarının yükleme satırındaki oluşturulan iş miktarıyla eşleştiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="7f826-121">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="7f826-122">Tüm ölçütlerin karşılandığından emin olmak için bu prosedürü tüm yükleme satırları için yineleyin.</span><span class="sxs-lookup"><span data-stu-id="7f826-122">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>
