---
title: Kanban işlem işlerini yürütme
description: Bu prosedür, kanban proses işlerinin yürütülmesiyle ilgilidir.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0bccee458ee48c51bdeeb64cee1f62aac9bdf4f9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828550"
---
# <a name="execute-kanban-process-jobs"></a>Kanban işlem işlerini yürütme

[!include [banner](../../includes/banner.md)]

Bu prosedür, kanban proses işlerinin yürütülmesiyle ilgilidir. İlk iş, beklenen miktar ile tamamlanır ve hiçbir hata alınmaz. İkinci iş bir takım hatalarla tamamlanır. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu yordam makine operatörü için hazırlanmıştır.


## <a name="select-a-kanban-job"></a>Bir kanban işi seçin.
1. Üretim kontrolü > Kanban > İş işlemleri için kanban kartı'na gidin.
2. İş hücresi alanında, açılır menü düğmesine tıklayarak aramayı açın.
3. 1250 kaynak grubunun bulunduğu sırayı tıklayın. Böylece, İş listesi filtrelenerek sadece 1250 iş hücresi için olan işler görüntülenir.
    * Planlı iş durumuna sahip sırayı işaretleyin.  

## <a name="complete-a-job-with-expected-quantity"></a>Bir işi beklenen miktarla tamamlama
1. Ayrıntılar bölümünü genişletin veya daraltın.
    * Bu bölümde kart numarası, madde numarası, sipariş edilen miktar ve etkinlik adı hakkında önemli bilgiler verilmiştir.  
2. Üretim talimatları bölümünü genişletin veya daraltın.
    * Bu bölümde etkinlik için üretim talimatları verilmiştir. Talimatlar metin, resim, çizim ve diğer belge türlerinde olabilir.  
3. Başlat'a tıklayın.
    * Tamamlanmamış bir iş seçin. İş durumunu görüntülemek için İş durumu alanındaki durum simgelerini kullanın.      
4. Tamamla öğesine tıklayın.
    * İş, beklenen miktarla tamamlanır.  

## <a name="complete-a-job-with-errors"></a>Bir işi hatalarla tamamlama
1. Başlat'a tıklayın.
    * Bir iş tamamlandığında listedeki bir sonraki iş otomatik olarak seçilir. Bu nedenle, Başlat düğmesini tıklamadan önce bir iş seçmenize gerek yoktur.  
2. Eylem Bölmesinde, Üretim öğesine tıklayın.
3. Tamamla (ayrıntılar) düğmesini tıklayın.
4. Listede, seçili satırı işaretleyin.
5. Hata miktarı alanına bir sayı girin.
6. İyi miktar alanına bir sayı girin.
7. Tamam'a tıklayın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]