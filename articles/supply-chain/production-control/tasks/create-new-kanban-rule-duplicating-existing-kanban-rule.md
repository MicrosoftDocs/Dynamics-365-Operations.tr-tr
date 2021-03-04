---
title: Mevcut bir kuralı çoğaltarak yeni bir kanban kuralı oluşturma
description: Bu yordam, varolan bir kanban kuralının kopyasını oluşturmaya odaklanır.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 84a0093d95c2f7084c7a0ed17f8b2f86d654b5d7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439018"
---
# <a name="create-a-new-kanban-rule-by-duplicating-an-existing-kanban-rule"></a>Mevcut bir kuralı çoğaltarak yeni bir kanban kuralı oluşturma

[!include [banner](../../includes/banner.md)]

Bu yordam, varolan bir kanban kuralının kopyasını oluşturmaya odaklanır. Varolan kanban kurallara dayalı yeni kanban kurallar oluşturmak istiyorsanız yararlıdır. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu yordam, değiştirilmiş bir üretim akışı ve yeni bir yenileme kuralı hazırlanırken kullanılması için işlem mühendisi veya değer akışı yöneticisi için hazırlanmıştır.


## <a name="select-a-kanban-rule"></a>Bir kanban kuralı seç
1. Kanban kuralları'na gidin.
2. Listede, istenen kaydı bulun ve seçin.
    * M0006 ürünü için 000017 kanban kuralını seçin.  

## <a name="duplicate-a-kanban-rule"></a>Bir kanban kuralını çoğalt
1. Kanban kuralını çoğalt'ı tıklatın.
    * Bir kanban kuralı çoğaltılırken türü, tarihleri, faaliyetleri ve ürün seçimini değiştirmek mümkündür. Sonraki adımda bu yordam için ürünü değiştirin.  
2. Ürün alanında bir değer girin veya bir değer seçin.
    * M0007 öğesini seçin.  
3. Tamam'a tıklayın.
    * 000017 kanban kuralının bir kopyasının oluşturulduğunu unutmayın.    



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]