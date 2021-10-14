---
title: Kanban durumunu güncelleştirme
description: Yanlışlıkla bir kanban boşaltılırsa veya alınan bir kanbanın boşaltılması gerekiyorsa, kanban durumunu güncelleştirmeniz gerekir.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3fd19febe38d5d0a201d5a50bc57ddb541e12051
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574365"
---
# <a name="update-kanban-status"></a>Kanban durumunu güncelleştirme

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]