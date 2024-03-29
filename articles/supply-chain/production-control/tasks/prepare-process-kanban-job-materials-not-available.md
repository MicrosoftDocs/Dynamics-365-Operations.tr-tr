---
title: Malzemeler iş hücresi için kullanılamadığında bir süreç kanban işi hazırlama
description: Bu yordam, bazı malzemeler için iş hücre kullanılamadığında bir süreç kanban işi hazırlanmasına odaklanır, bu nedenle ambardan malzeme çekme gerekli.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f75cdbc6ce6f7e427bf266c90428d73c065eac3
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576748"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a>Malzemeler iş hücresi için kullanılamadığında bir süreç kanban işi hazırlama

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]