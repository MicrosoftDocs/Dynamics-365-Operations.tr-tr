---
title: Kanban iş durumu geri al
description: Bu yordam, yanlış bir kanban iş durumunun geri alınması üzerinde odaklanır.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9bc147ec517b8141b4764f67d21b4c4a2e4d6e6e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981168"
---
# <a name="revert-kanban-job-status"></a>Kanban iş durumu geri al

[!include [banner](../../includes/banner.md)]

Bu yordam, yanlış bir kanban iş durumunun geri alınması üzerinde odaklanır. Bu, makine operatörünün yanlış işi güncelleştirmesi veya yanlışlıkla hatalı bir durum ayarı girmesi durumunda yararlıdır. Bu yordamda, bir kanban işi yanlışlıkla hazırlandı olarak kaydedilmiştir ve durumu daha sonra döndürülmüştür. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu yordam mağaza idarecisine veya yalın üretim şirketinde çalışan makine operatörüne yöneliktir.


## <a name="open-process-board-for-the-work-cell"></a>İş hücresi için işleme panosunu açın
1. İşleme işleri için kanban panosuna gidin.
2. İş hücresi alanına bir değer girin veya buradan bir değer seçin.
    * İş hücresi 1260'yi seç  

## <a name="prepare-kanban-job"></a>Kanban işini hazırla
1. Hazırla'ya tıklayın.
    * Hazırla'yı üzeri gir olduğu için tıklatamıyorsanız, kanban simgesinin boş olmasıyla anlaşılabilecek şekilde, seçili kanban'ın iş durumunun Planlı olduğundan emin olun. Hazırla başarısız olursa, tüm malzemelerin, malzeme çekme listesinde mevcut olduğundan emin olun.  
2. Listeden hazırlanmış işi seç.
    * Şu an hazırlamış olduğunuz ilk projeyi seçin.  
    * İş durumunun hazırlanmış olduğuna, kanban simgesi içindeki üçgen ile gösterildiği şekilde, dikkat edin.  

## <a name="revert-the-status-of-the-prepared-kanban-job"></a>Hazırlanan kanban işinin durumunu geri döndür
1. Listede, seçili satırı işaretleyin.
    * Önceden hazırlanmış ilk projeyi seçin.  
2. Eylem Bölmesinde, Üretim öğesine tıklayın.
3. Durumu geri al'a tıklayın.
    * Aşağıdaki koşullar doğru olduğunda bir alternatif kanban kuralı kullanabilirsiniz:  - Stok yenileme stratejisi her iki kural için de aynıdır.  - Her iki kural için de üretim akışı sürümü aynıdır.  - Sağlanan ürün her iki kural için de aynıdır.  - Kanban kurallarının son aktivitesi için yapılandırılmış olan tüm akış faaliyetlerinin her iki kural için de aynı olması gerekir.  - Sağlanan stok boyutları her iki kural için de yapılandırılmış olmalıdır.  - İşleme birimi durumunun Atanmamış olması gerekir.  - Olay kanbanları yapılandırmaları da aynı olmalıdır.  
    * Yeni durumun Planlı olduğundan emin olun.  
4. Tamam'a tıklayın.
5. Listede, seçili satırın işaretini kaldırın.
    * Aynı işi seçin.  
    * Kanban işi için iş durumunun bir boş kanban simgesiyle gösterildiği üzere, Planlı'ya dönüştürüldüğüne dikkat edin.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]