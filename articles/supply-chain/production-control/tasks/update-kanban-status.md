---
title: Kanban durumunu güncelleştirme
description: Yanlışlıkla bir kanban boşaltılırsa veya alınan bir kanbanın boşaltılması gerekiyorsa, kanban durumunu güncelleştirmeniz gerekir.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 97b6eea4e93967dbe1eea5eac9fe3fbf6b336a49
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838475"
---
# <a name="update-kanban-status"></a>Kanban durumunu güncelleştirme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Yanlışlıkla bir kanban boşaltılırsa veya alınan bir kanbanın boşaltılması gerekiyorsa, kanban durumunu güncelleştirmeniz gerekir. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu prosedür, mağaza denetleyicisi için hazırlanmıştır.


## <a name="find-the-kanban"></a>Kanbanı bulun.
1. Üretim denetimi > Kanban > Kanbanlar öğesine gidin.
2. İşleme ünitesi durumu sütun filtresini açın.
3. Temizle'ye tıklayın.
    * Bu, filtreleri sıfırlar.  
4. Kayıtları bulmak için Hızlı Filtre'yi kullanın. Örneğin, Kart numarası alanını bir '000149' değeriyle filtreleyin.

## <a name="change-emptied-status-to-received-status"></a>Boşaltıldı durumunu alındı olarak değiştirme
1. Boş işleme ünitesini ters çevir düğmesini tıklayın.
2. Tamam'a tıklayın.
    * İşlem ünitesi durumunun Alındı olduğuna dikkat edin.  

## <a name="change-received-status-to-emptied-status"></a>Alındı durumunu boşaltıldı olarak değiştirme
1. Kanbanı boşaltı düğmesini tıklayın.
2. Listede, seçili satırı işaretleyin.
    * İşlem ünitesi durumunun Boşaltıldı olduğuna dikkat edin.  

