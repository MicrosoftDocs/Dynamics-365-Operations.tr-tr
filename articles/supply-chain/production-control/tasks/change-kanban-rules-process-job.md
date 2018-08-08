--- 
title: "Süreç işi için kanban kurallarını değiştirme"
description: "Bu yordam, belirli bir kanban için kullanılan kanban kuralını değiştirmeye odaklanır."
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7f8b2a67e03a64deae9d4bc9c7e3e714d134443c
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="change-kanban-rules-for-a-process-job"></a>Süreç işi için kanban kurallarını değiştirme

[!include [task guide banner](../../includes/task-guide-banner.md)]

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


