---
title: Süreç işi için kanban kurallarını değiştirme
description: Bu yordam, belirli bir kanban için kullanılan kanban kuralını değiştirmeye odaklanır.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2bdbbbf8a8b3d1596c251224cba996c0631050c4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829318"
---
# <a name="change-kanban-rules-for-a-process-job"></a>Süreç işi için kanban kurallarını değiştirme

[!include [banner](../../includes/banner.md)]

Bu yordam, belirli bir kanban için kullanılan kanban kuralını değiştirmeye odaklanır. Bu, yük kaynaklarını eşitlemek için veya döküm sırasında yararlıdır. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu yordam, bir yalın üretim şirketinde çalışan ve değer akışından sorumlu planlayıcı için tasarlanmıştır.


## <a name="copy-kanban-rule"></a>Kanban kuralını kopyalama
1. Kanban kuralları'na gidin.
2. Listede, istenen kaydı bulun ve seçin.
    * L0001 için 000022 Kanban olayı kuralını seçin.  
3. Kanban kuralını çoğalt'ı tıklatın.
4. Tamam'a tıklayın.

## <a name="change-kanban-rule"></a>Kanban kuralını değiştirme
1. Sayfayı kapatın.
2. Kanban işi planlaması'na gidin.
3. Listede, seçili satırı işaretleyin.
    * Kanban 000177 içeren satırı seçin.  
4. Alternatif kanban kuralı kullan'ı tıklatın.
5. İleri düğmesini tıklatın.
6. Kanban kuralı alanında bir değer girin veya bir değer seçin.
    * Daha önce oluşturulan kanban kuralını seçin. Bu, en büyük sayıya sahip kanban kuralıdır.  
7. Son düğmesini tıklatın.
    * Kanban işi şimdi artık başka bir kanban kuralını kullanmaktadır. Bu, yük iş hücrelerini eşitlemek için yararlı olabilir.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]