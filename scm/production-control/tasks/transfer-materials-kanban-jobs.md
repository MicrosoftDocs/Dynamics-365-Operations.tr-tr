--- 
title: "Malzemeleri kanban işleriyle transfer etme (yalnızca Şubat 2016)"
description: "Bu yordam, malzemelerin aktarmak için bir çekme kanban işini yürütmek üzerinde odaklanır."
author: ChristianRytt
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 72403aa502cadf2a727bdd67ad8cd612dafd502b
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="transfer-materials-with-kanban-jobs-february-2016-only"></a>Malzemeleri kanban işleriyle transfer etme (yalnızca Şubat 2016)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, malzemelerin aktarmak için bir çekme kanban işini yürütmek üzerinde odaklanır. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu yordam ambar çalışanı için hazırlanmıştır.


## <a name="display-transfer-jobs"></a>Transfer işlerini görüntüler
1. Production control > Kanban > Kanban board for transfer jobs (Üretim kontrolü > Kanban > Transfer işleri için kanban panosu) menüsüne gidin.
2. Filtreler bölümünü genişletin veya daraltın.
    * Filtreler bölümünde üretim akışı, eylem adı, kaynak ambar ve konumu, hedef ambar ve konumu ile filtreleyerek hangi işleri görmek istediğinizi seçebilirsiniz.  
3. Kaynak ambar alanına '11' yazın.
4. Hedef konum alanına '12' yazın.

## <a name="start-a-transfer-job"></a>Bir transfer işi başlat
1. Listede, eğer varsa, seçili satırın işaretini kaldırın.
2. Listede satır 4'ü seçin.
    * Durumu Planlanmami; olan ilk işi seçin. Yalnız bu işin seçildiğinden emin olun.  
3. Başlat'a tıklayın.
    * Bir simgenin işin başladığı belirttiğine dikkat edin.  

## <a name="select-a-second-transfer-job-and-change-quantity"></a>İkinci bir transfer işi seçin ve miktarı değiştirin
1. Listede, istenen kaydı bulun ve seçin.
    * Birden fazla iş seçebilirsiniz fakat şimdilik sadece satır 5'i seçin.  
2. Listede, istenen kaydı bulun ve seçin.
    * Önceki adımdaki işin seçilen tek iş olduğundan emin olun. Diğer tüm işlerin seçimlerini kaldırın.  
3. İş miktarı alanındaki değeri, daha sonra başvurmak üzere not edin
4. İş miktarını '30' olacak şekilde ayarlayın.
    * Uyarıya dikkat edin! 30 transfer etmenize izin verilmez. Kanban kural ayarına göre sadece başlangıçtaki miktarı aktarabilirsiniz.  
5. Daha önce not edilen değeri İş miktarı alanında kullanın
    * İş miktarını önceki değere ayarlayın.  

## <a name="start-the-second-transfer-job"></a>İkinci transfer işlemini başlatın
1. Başlat'a tıklayın.
    * Bu, satır 5'deki işin transferini başlatacaktır.  

## <a name="complete-both-transfer-jobs"></a>Her iki transfer işini tamamlayın
1. Listede satır 4'ü seçin.
    * Şimdi satır 4 ve 5'te iki transfer işi seçilmiştir.  
2. Tamamla öğesine tıklayın.
    * Bu her iki işin transferini tamamlayacaktır.  


