--- 
title: "Planlanmış kanban işlerini taşıma"
description: "Bu prosedür, planlanan işlem kanban işlerini farklı bir döneme taşımaya odaklanmaktadır."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
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
ms.openlocfilehash: 2a12a6859a3a436706822873bc6fdd781e0ef032
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="move-scheduled-kanban-jobs"></a>Planlanmış kanban işlerini taşıma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu prosedür, planlanan işlem kanban işlerini farklı bir döneme taşımaya odaklanmaktadır. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu prosedür, kanbanlarla çalışan atölye gözetmenlerine veya üretim planlayıcılarına yöneliktir.


## <a name="select-scheduled-kanban-jobs"></a>Planlanmış kanban işlerini seçin
1. Üretim denetimi > Kanban > Kanban işi zamanlaması'nı gidin.
2. !MtCMR!İş hücresi alanında, açılır menü düğmesine tıklayarak aramayı açın. áçêìõý !
3. Listede, seçili satırı işaretleyin.
    * İş hücresi 1250'yi seç  
4. Seç'e tıklayın.
5. İş durumunu görüntüle alanında "Planlandı"yı seçin.
    * Bu, yalnızca zamanlanmış kanban işlerini görüntülemek üzere iş listesine filtre uygular.  

## <a name="move-kanban-jobs-to-a-different-period"></a>Kanban işlerini başka bir döneme taşıyın
1. İstediğiniz girişi bulup seçin.
    * İş durumu Planlandı olan bir iş seçin. Örneğin Planlanan dönem alanında bir iş 20 Aralık 2012  tarihine zamanlanmıştır. Bu durumda işi önceki döneme taşıyın.  
2. Önceki dönem'e tıklayın.
3. Bitiş'e tıklayın.
    * Bu, işi önceki dönemin son işi olarak iş listesinin sonuna taşır.  
4. İstediğiniz girişi bulup seçin.
    * İş durumu Planlandı olan bir iş seçin. Örneğin Planlanan dönem alanında bir iş 18 Aralık 2012 tarihine zamanlanmıştır. Bu durumda işi sonraki döneme taşıyın.  
5. Sonraki dönem'e tıklayın.
6. Başlat'a tıklayın.
    * Bu, işi önceki dönemin ilk işi olarak iş listesinin başına taşır.  

## <a name="task-move-a-job-within-a-period"></a>Görev: Bir işi dönem içinde taşıyın
1. İstediğiniz girişi bulup seçin.
    * İş durumu Planlandı olan bir iş seçin. Örneğin Planlanan dönem alanında ikinci iş 19 Aralık 2012 tarihine zamanlanmıştır. Bu durumda işi planlanan dönem içinde taşıyın.  
2. İleri'ye tıklayın.
    * İşin listede bir satır aşağıya taşındığına dikkat edin.  
3. Geri'ye tıklayın.
    * İşin listede bir satır yukarıya taşındığına dikkat edin.  


