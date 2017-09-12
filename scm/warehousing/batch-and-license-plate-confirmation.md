---
title: "Toplu iş ve lisans plaka onayı"
description: "Bu konu bir mobil cihazdan toplu iş ve plaka onayının nasıl ayarlanacağını ve uygulanacağını açıklamaktadır."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: bf9447f81d6c1ff543ceb5a058428ed1c0090da0
ms.contentlocale: tr-tr
ms.lasthandoff: 07/18/2017

---

# <a name="batch-and-license-plate-confirmation"></a><span data-ttu-id="e4cc9-103">Toplu iş ve lisans plaka onayı</span><span class="sxs-lookup"><span data-stu-id="e4cc9-103">Batch and license plate confirmation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e4cc9-104">Toplu iş onayı, doğru toplu işin mobil cihazdan alındığını onaylamanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-104">Batch confirmation allows you to confirm that the correct batch is being picked from the mobile device.</span></span> <span data-ttu-id="e4cc9-105">*Toplu iş üstü*'nün arama hiyerarşisindeki toplu iş aralıklarının daha yüksek olduğunu belirttiği yalnızca toplu iş üstü maddelerin ilk çekilmesinde, çekilen toplu işin, iş satırındaki toplu iş olduğunu doğrulamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-105">On the initial pick of work for batch above-items only, where *batch above* indicates that batch ranges higher than location in the search hierarchy, you must verify that the batch that is picked matches the batch on the work line.</span></span> 

<span data-ttu-id="e4cc9-106">Plaka onayı, doğru plakanın mobil cihazdan alındığını onaylamanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-106">License plate confirmation allows you to confirm that the correct license plate is being picked from the mobile device.</span></span> <span data-ttu-id="e4cc9-107">Bir aşama konumundan iş çekerken, çekilen plakanın, iş ile ilişkilendirilmiş plaka ile eşleştiğini doğrulamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-107">When picking work from a stage location, you must verify that the license plate that is picked matches the license plate that is associated with the work.</span></span> <span data-ttu-id="e4cc9-108">İş, bir plakanın taratılması ile başlatıldıysa, onay adımı atlanacaktır.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-108">If the work is started by scanning a license plate, this confirmation step will be skipped.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="e4cc9-109">Uygulandığı yerler</span><span class="sxs-lookup"><span data-stu-id="e4cc9-109">Where it applies</span></span>
<span data-ttu-id="e4cc9-110">Onay yalnızca aşağıdaki senaryolarda geçerlidir:</span><span class="sxs-lookup"><span data-stu-id="e4cc9-110">Confirmation applies in the following scenarios:</span></span>

- <span data-ttu-id="e4cc9-111">Toplu onay, yalnızca toplu iş üst maddeleri için işin ilk çekmelerine uygulanır.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-111">Batch confirmation applies to the initial picks of work for batch above-items.</span></span>
- <span data-ttu-id="e4cc9-112">Plaka onayı, aşama konumlarından çekmelere uygulanır.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-112">License plate confirmation applies to picks from stage locations.</span></span>

## <a name="set-up-batch-and-license-plate-confirmation"></a><span data-ttu-id="e4cc9-113">Toplu iş ve plaka onayını ayarlama</span><span class="sxs-lookup"><span data-stu-id="e4cc9-113">Set up batch and license plate confirmation</span></span>
<span data-ttu-id="e4cc9-114">Toplu iş ve plaka onayı yapılandırmasını mobil cihaz menü öğelerinden yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-114">You can configure batch and license plate confirmation from the mobile device menu items.</span></span>  
1.  <span data-ttu-id="e4cc9-115">İşler mobil cihaz menü öğesinden, iş onay kurulumunu açın.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-115">From the mobile device menu items, enter the work confirmation setup.</span></span>  
2.  <span data-ttu-id="e4cc9-116">Toplu iş veya plaka onayı için seçeneği işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-116">Select the option for either batch or license plate confirmation.</span></span> <span data-ttu-id="e4cc9-117">Her iki seçenek de otomatik onayın etkinleştirilmiş olmadığı iş türü çekmeleri için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-117">Both options are available for work type picks that do not have automatic confirmation enabled.</span></span>  

