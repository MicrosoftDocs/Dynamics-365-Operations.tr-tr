---
title: Birden fazla faaliyet için kanban kuralı oluşturma
description: Bu yordam, bir üretim akışından birden fazla faaliyeti içeren bir kanban kuralının nasıl oluşturulacağını gösterir.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, KanbanFlowSelection, InventItemIdLookupSimple, KanbanCreateScheduled, Kanban
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f55034f4f0557023ce0c659c1e8258214cf8bfa3
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569275"
---
# <a name="create-a-kanban-rule-for-multiple-activities"></a>Birden fazla faaliyet için kanban kuralı oluşturma

[!include [banner](../../includes/banner.md)]

Bu yordam, bir üretim akışından birden fazla faaliyeti içeren bir kanban kuralının nasıl oluşturulacağını gösterir. Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu görev, yalın bir ortamda yeni veya değiştirilmiş bir ürünün üretimine hazırlanırken kullanılması için işlem mühendisi veya değer akışı yöneticisi için hazırlanmıştır.


## <a name="create-a-new-kanban-rule"></a>Yeni bir kanban kuralı oluştur
1. Ürün bilgi yönetimi > Yalın imalat > Kanban kuralları'na gidin.
2. Yeni'ye tıklayın.
3. Stok yenileme stratejisi alanında "Planlandı"yı seçin.
4. İlk plan alanında bir değer girin veya bir değer seçin.
    * SpeakerAssemblyAndPolish öğesini seçin.  
5. Birden çok faaliyet onay kutusunu seçin.
    * Amaç kanban kuralında birden fazla faaliyet içermektir. En son planlı faaliyeti seçtiğinizde üretim akışında bir yol seçersiniz.  
6. Son plan faaliyeti alanına bir değer girin veya bir değer seçin.
    * SpeakerTestAndPackaging öğesini seçin. Değeri seçtikten sonra otomatik olarak bir sayfa açılır. Kanban akışı SpeakerAssemblyAndPolish > SpeakerTestAndPackaging öğesini seçin. Tamam'a tıklayın.  
7. Ayrıntılar bölümünü genişletin.
8. Ürün alanında bir değer girin veya bir değer seçin.
    * Madde L0006'yı seçin.  

## <a name="create-kanban-and-view-jobs"></a>Kanban oluşturun ve işleri görüntüleyin
1. Kanbanlar bölümünü genişletin.
2. Ekle öğesini tıklatın.
3. Yeni kanbanların sayısı alanına "1" girin.
    * Bu, bir kanban oluşturur.  
4. Toplam ürün miktarını '3'e ayarlayın.
    * Kanban, 3 ürünü işler.  
5. Vade tarihi/saati alanına bir tarih ve saat girin.
    * Bugün girebilirsiniz.  
6. Oluştur'a tıklayın.
7. Ayrıntılar seçeneğini tıklatın.
    * Kanbanın, üretim akışından iki işlem işi olduğuna dikkat edin. Birincisi SpeakerAssemblyAndPolish ve ikincisi de SpeakerTestAndPackaging öğeleridir.  
    * Bu son adımdır!  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]