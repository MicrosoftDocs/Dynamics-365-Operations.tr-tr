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
# <a name="missing-field-settings-when-item-model-groups-are-copied-to-another-legal-entity"></a>Madde modeli grupları başka bir tüzel kişiliğe kopyalandıklarında alan ayarları eksik

KB numarası: 4612800

## <a name="symptoms"></a>Belirtiler

*Madde modeli grubu stok ilkeleri* varlığını kullanarak madde modeli gruplarını başka bir tüzel kişiliğe (şirket) kopyaladığınızda, hedef tüzel kişilikteki yeni model grubunda bazı alan ayarları (örneğin, stok modeli ve açıklama) eksik.

## <a name="resolution"></a>Çözünürlük

Bir madde modeli grubunun başka bir tüzel kişilikte tam bir kopyasını oluşturmak için, madde modeli grubuyla ilişkilendirilmiş hem madde modeli grubu stok ilkelerini (`InventInventoryPolicyEntity`) hem de maliyet akışı varsayım ilkelerini (`InventCostFlowAssumptionPolicyEntity`) seçmeniz gerekir.
