---
title: Madde modeli grupları başka bir tüzel kişiliğe kopyalandıklarında alan ayarları eksik
description: Madde modeli grupları başka bir tüzel kişiliğe kopyalandıklarında alan ayarları eksik kalıyor.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f6fdfef0bc377418ed8a9c8830e74526a0b95eb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026978"
---
# <a name="missing-field-settings-when-item-model-groups-are-copied-to-another-legal-entity"></a><span data-ttu-id="a1e78-103">Madde modeli grupları başka bir tüzel kişiliğe kopyalandıklarında alan ayarları eksik</span><span class="sxs-lookup"><span data-stu-id="a1e78-103">Missing field settings when item model groups are copied to another legal entity</span></span>

<span data-ttu-id="a1e78-104">KB numarası: 4612800</span><span class="sxs-lookup"><span data-stu-id="a1e78-104">KB number: 4612800</span></span>

## <a name="symptoms"></a><span data-ttu-id="a1e78-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="a1e78-105">Symptoms</span></span>

<span data-ttu-id="a1e78-106">*Madde modeli grubu stok ilkeleri* varlığını kullanarak madde modeli gruplarını başka bir tüzel kişiliğe (şirket) kopyaladığınızda, hedef tüzel kişilikteki yeni model grubunda bazı alan ayarları (örneğin, stok modeli ve açıklama) eksik.</span><span class="sxs-lookup"><span data-stu-id="a1e78-106">When you copy item model groups to another legal entity (company) by using the *Item model group inventory policies* entity, some field settings (for example, the inventory model and description) are missing in the new model group in the destination legal entity.</span></span>

## <a name="resolution"></a><span data-ttu-id="a1e78-107">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="a1e78-107">Resolution</span></span>

<span data-ttu-id="a1e78-108">Bir madde modeli grubunun başka bir tüzel kişilikte tam bir kopyasını oluşturmak için, madde modeli grubuyla ilişkilendirilmiş hem madde modeli grubu stok ilkelerini (`InventInventoryPolicyEntity`) hem de maliyet akışı varsayım ilkelerini (`InventCostFlowAssumptionPolicyEntity`) seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="a1e78-108">To create a complete copy of an item model group to another legal entity, you must also select both the item model group inventory policies (`InventInventoryPolicyEntity`) and the cost flow assumption policies (`InventCostFlowAssumptionPolicyEntity`) that are associated with the item model group.</span></span>
