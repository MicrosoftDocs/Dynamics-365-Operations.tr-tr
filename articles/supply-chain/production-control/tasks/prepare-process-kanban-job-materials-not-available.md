--- 
title: "Malzemeler iş hücresi için kullanılamadığında bir süreç kanban işi hazırlama"
description: "Bu yordam, bazı malzemeler için iş hücre kullanılamadığında bir süreç kanban işi hazırlanmasına odaklanır, bu nedenle ambardan malzeme çekme gerekli."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5a47af6910a9686e74ab6d1069dd02079e60cb8a
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a>Malzemeler iş hücresi için kullanılamadığında bir süreç kanban işi hazırlama

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, bazı malzemeler için iş hücre kullanılamadığında bir süreç kanban işi hazırlanmasına odaklanır, bu nedenle ambardan malzeme çekme gerekli. "Malzeme hazır olduğunda bir süreç kanban işi hazırla" yordamı, bu yordamı oluşturmak için bir önkoşuldur. Bu yordam makine operatörü için hazırlanmıştır. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.

1. Üretim kontrolü > Kanban > İş işlemleri için kanban kartı'na gidin.
2. İş hücresi alanında, açılır menü düğmesine tıklayarak aramayı açın.
3. Listede, seçili satırdaki bağlantıya tıklayın.
    * İş hücresi 1250'yi seç  
4. Listede, istenen kaydı bulun ve seçin.
    * Kanban 000356'yı seçin.  
5. Listede, istenen kaydı bulun ve seçin.
    * Listede satır 4'ün seçimini kaldırın. ya da "Malzeme hazır olduğunda bir süreç kanban işi hazırlayın" görevini tamamlamadıysanız satır 4'ü seçin.  
6. Malzeme çekme listesi bölümünün genişletilmiş görünümüne geçin.
    * Tedarik durumundaki Giriş yok simgesi, madde P0002'nin 48 ea iş hücresinden eksik olduğunu gösterir.  

## <a name="transfer-materials-to-work-cell"></a>Malzemeleri iş hücresine nakledin
1. Transfer işleri bölümünün genişletilmiş görünümüne geçin.
2. Madde numarası alanında 'P0002' değeriyle filtreleme yapmak için Hızlı Filtre'yi kullanın.
3. Listede, istenen kaydı bulun ve seçin.
4. Başlat'a tıklayın.
    * Transfer devam ediyor.  
5. Tamamla öğesine tıklayın.
    * Madde P0002 kanban işi için malzeme çekme listesinde kullanılabilir. Başka bir deyişle, gerekli tüm malzemelerle kanban hazırlayabilirsiniz.  
6. Hazırla'ya tıklayın.
    * İş durumu'ndaki bir simgenin işin şimdi hazır olduğunu belirttiğini unutmayın.  


