---
title: Miktar sıfır olduğundan sevkiyatı onaylayamazsınız
description: Miktar sıfır olduğundan sevkiyatı onaylayamazsınız
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
ms.openlocfilehash: 7a06f0651db741a867e1e9fe7dbab841a928c22b
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938566"
---
# <a name="you-cant-confirm-a-shipment-because-there-is-zero-quantity"></a><span data-ttu-id="2cd57-103">Miktar sıfır olduğundan sevkiyatı onaylayamazsınız</span><span class="sxs-lookup"><span data-stu-id="2cd57-103">You can't confirm a shipment because there is zero quantity</span></span>

<span data-ttu-id="2cd57-104">Hata kodu: LoadLineWarningUpdatedToZero</span><span class="sxs-lookup"><span data-stu-id="2cd57-104">Error code: LoadLineWarningUpdatedToZero</span></span>

## <a name="symptoms"></a><span data-ttu-id="2cd57-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="2cd57-105">Symptoms</span></span>

<span data-ttu-id="2cd57-106">Bir sevkiyatı onaylamaya çalıştığınızda, sistem aşağıdaki hata iletisini gösterir:</span><span class="sxs-lookup"><span data-stu-id="2cd57-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="2cd57-107">Bu madde için hiçbir miktarın sevk edilmesine izin vermeyen eksik teslimat ayarlarından dolayı, %1 maddesi ve %2 sevkiyatı için yük satırı sıfır miktara sahip olacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="2cd57-107">Load line for item %1 and shipment %2 has been updated to have zero quantity due to underdelivery setup allowing not to ship any quantities for this item.</span></span>

<span data-ttu-id="2cd57-108">Bu nedenle, yükleme için sevkiyat işlemini onaylayamazsınız.</span><span class="sxs-lookup"><span data-stu-id="2cd57-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="2cd57-109">Nedeni</span><span class="sxs-lookup"><span data-stu-id="2cd57-109">Cause</span></span>

<span data-ttu-id="2cd57-110">Sistem, teslim alınan miktarın; teslim alınan miktar, yükleme satırı miktarı ve eksik teslimat yüzdesine göre beklenen sınırlar içinde olup olmadığını değerlendirir.</span><span class="sxs-lookup"><span data-stu-id="2cd57-110">The system evaluates whether the picked quantity is within the expected limits, based on the picked quantity, load line quantity, and underdelivery percentage.</span></span> <span data-ttu-id="2cd57-111">Sistem, yükleme satırındaki teslim alınan miktarın 0 (sıfır) olduğunu belirlerse, sevkiyatı onaylayamazsınız.</span><span class="sxs-lookup"><span data-stu-id="2cd57-111">If the system finds that the picked quantity on the load line is 0 (zero), you can't confirm the shipment.</span></span> <span data-ttu-id="2cd57-112">Örneğin, iş iptal edilirse ve yükleme satırındaki eksik teslimat yüzdesi yüzde 100 ise bu sorun oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="2cd57-112">For example, this issue might occur if work has been canceled, and the underdelivery percentage on the load line is 100 percent.</span></span>

## <a name="resolution"></a><span data-ttu-id="2cd57-113">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="2cd57-113">Resolution</span></span>

<span data-ttu-id="2cd57-114">Eksik teslimat yüzdesinin ve miktarların, teslim alınan işle uyumlu olduğundan emin olmak için yükleme satırlarını denetleyin.</span><span class="sxs-lookup"><span data-stu-id="2cd57-114">Check your load lines to make sure that the underdelivery percentage and quantities are aligned with the picked work.</span></span>

1. <span data-ttu-id="2cd57-115">**Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="2cd57-115">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="2cd57-116">Sevkiyatın onaylanamadığı ilgili yükü seçin.</span><span class="sxs-lookup"><span data-stu-id="2cd57-116">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="2cd57-117">**Yük satırları** hızlı sekmesinde, eksik teslimat yüzdesini aşan maddenin yük satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="2cd57-117">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="2cd57-118">**Eksik teslimat** alanının veya **Miktar** alanının değerini gerektiği gibi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2cd57-118">Adjust the value of the **Underdelivery** field or the **Quantity** field as required.</span></span>

> [!TIP]
> <span data-ttu-id="2cd57-119">Sorun hala düzelmezse mevcut miktar, yükleme veya sevkiyat ile uyumlu hale gelene kadar ilgili satış siparişleri veya transfer emirleri için daha fazla teslim alma işi tamamlamanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="2cd57-119">If the issue still isn't fixed, you might have to complete more picking work for the related sales orders or transfer orders until the available quantity is aligned with the load or shipment.</span></span>
