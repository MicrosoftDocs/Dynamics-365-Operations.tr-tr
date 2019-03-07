---
title: İade edilen maddelerin kısmi teslimatlarını alma
description: Kısmi teslimatlar sipariş iadesi sevkiyatlarına göre değil, sipariş iadesi satırlarına göre tanımlanır.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2b7bfad1e0d80675848353d4118960d44f2dc01
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "363925"
---
# <a name="receive-partial-deliveries-of-returned-items"></a><span data-ttu-id="f1d18-103">İade edilen maddelerin kısmi teslimatlarını alma</span><span class="sxs-lookup"><span data-stu-id="f1d18-103">Receive partial deliveries of returned items</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="f1d18-104">Kısmi teslimatlar sipariş iadesi sevkiyatlarına göre değil, sipariş iadesi satırlarına göre tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="f1d18-104">Partial deliveries are defined in terms of return order lines, not return order shipments.</span></span>

<span data-ttu-id="f1d18-105">Diğer bir deyişle, bir sipariş iadesi satırındaki tam miktarı alır ancak sipariş iadesindeki diğer satırlardan hiçbir şey almazsanız, teslimat kısmi bir teslimat olmaz.</span><span class="sxs-lookup"><span data-stu-id="f1d18-105">This means that if you receive the full quantity that is indicated on one return order line, but you receive nothing from the other lines in the return order, the delivery is not a partial delivery.</span></span> <span data-ttu-id="f1d18-106">Ancak, bir sipariş iadesi satırında belirli bir maddenin 10 biriminin iade edilmesi isteniyorsa, ancak siz yalnızca dördünü alırsanız, bu kısmi bir teslimattır.</span><span class="sxs-lookup"><span data-stu-id="f1d18-106">However, if a return order line requires 10 units of a particular item to be returned, but you receive only four, it is a partial delivery.</span></span>

<span data-ttu-id="f1d18-107">Bir iade sevkiyatı bir sipariş iadesi satırının tam miktarından daha azını içeriyorsa, sevkiyatı bir kenara bırakıp iade edilen miktarın geri kalanının gelmesini bekleyebilirsiniz veya kısmi miktarı kaydedip deftere nakledebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f1d18-107">If a return shipment contains less than the full quantity of a return order line, you can set the shipment aside and wait for the rest of the returned quantity to arrive, or you can register and post the partial quantity.</span></span>

## <a name="register-and-post-a-partial-quantity"></a><span data-ttu-id="f1d18-108">Kısmi miktarı kaydetme ve deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="f1d18-108">Register and post a partial quantity</span></span>

1.  <span data-ttu-id="f1d18-109">**Varışa genel bakış - Ambar: %1, Nokta: %2, Günlük adı: %3** formunda varış için bir iade siparişi seçtikten sonra, varış günlüğünü oluşturmak için **Varışı başlat**'a tıklayın ve ardından **Günlükler** \> **Girişlerden varışları göster**'e tıklayarak **Yerleşim günlüğü** formunu açın.</span><span class="sxs-lookup"><span data-stu-id="f1d18-109">After you select a return order for arrival on the **Arrival overview - Warehouse: %1, Dock: %2, Journal name: %3** form, click **Start arrival** to create the arrival journal, and then click **Journals** \> **Show arrivals from receipts** to open the **Location journal** form.</span></span>

2.  <span data-ttu-id="f1d18-110">Çalışmak istediğiniz günlük satırını seçin ve **Satırlar**'ı tıklayarak **Günlük satırları, yerleşimler** formunu açın.</span><span class="sxs-lookup"><span data-stu-id="f1d18-110">Select the line of the journal that you want to work with, and then click **Lines** to open the **Journal lines, locations** form.</span></span>

3.  <span data-ttu-id="f1d18-111">Yalnızca kısmi miktarın geldiği madde numarasının satırını seçin ve **Böl** formunu açmak için sırasıyla **İşlevler** \> **Böl**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f1d18-111">Select the line of the item number for which only a partial quantity has arrived, and then click **Functions** \> **Split** to open the **Split** form.</span></span>

4.  <span data-ttu-id="f1d18-112">**Miktarı böl** alanında alınan toplam madde sayısı için miktarı girin ve **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f1d18-112">In the **Split quantity** field, enter the quantity for the total number of items that have been received, and then click **OK**.</span></span>

5.  <span data-ttu-id="f1d18-113">**Günlük satırları, yerleşimler** formunda gelen madde miktarı için satırı seçin ve **Deftere naklet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f1d18-113">On the **Journal lines, locations** form, select the line for the quantity of items that has arrived, and then click **Post**.</span></span> <span data-ttu-id="f1d18-114">Maddeler geldikten sonra ek miktar için satırı deftere nakledebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f1d18-114">You can post the line for the additional quantity after the items have arrived.</span></span>




