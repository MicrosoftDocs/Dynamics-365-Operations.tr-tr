---
title: Minimum stok olayı kullanarak kanban kuralı oluşturma
description: Bu yordam, belirli bir ürünün her zaman belirli bir konumda bulunabilir olmasını sağlamak için bir minimum stok olayı kullanan bir kanban kuralı oluşturmak için gereken kuruluma odaklanır.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a9ba8ec2abb26e3b9ee7e14bdf882c1ffcb205b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558538"
---
# <a name="create-a-kanban-rule-using-a-minimum-stock-event"></a>Minimum stok olayı kullanarak kanban kuralı oluşturma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, belirli bir ürünün her zaman belirli bir konumda bulunabilir olmasını sağlamak için bir minimum stok olayı kullanan bir kanban kuralı oluşturmak için gereken kuruluma odaklanır. Stok seviyesi 200 adedin altına düştüğünde konuma malzeme transfer etmek için bir kanban kuralı oluşturulur. İlişkilendirme olayının işlenmesini çalıştırarak gerekli kanbanlar oluşturulur. Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu görev, yalın bir ortamda yeni veya değiştirilmiş bir ürünün üretimine hazırlanırken kullanılması için işlem mühendisi veya değer akışı yöneticisi için hazırlanmıştır.


## <a name="create-a-new-kanban-rule"></a>Yeni bir kanban kuralı oluştur
1. Ürün bilgi yönetimi > Yalın imalat > Kanban kuralları'na gidin.
2. Yeni'ye tıklayın.
3. Tür alanından 'Çek' seçimini yapın.
    * Transfer kanbanlarının oluşturulması için bu tür kullanılır.  
4. Yenileme stratejisi alanında 'Olay' öğesini seçin.
    * Olay stratejisi, bir olaya göre kanbanların transferini oluşturmak için kullanılır. Bu yordamın sonraki bölümünde stok yenilemeyi kullanarak transfer kanbanları tetiklersiniz.  
5. İlk plan alanında bir değer girin veya bir değer seçin.
    * ReplenishSpeakerComponents öğesini girin veya seçin. Bu transfer faaliyeti, alıcı (çıkış) ambarına ve konum 12'ye sahiptir, bu da malzemelerin ambar 12'deki konum 12'ye taşınacağı anlamına gelir.  
6. Ayrıntılar bölümünü genişletin.
7. Ürün alanında bir değer girin veya bir değer seçin.
    * M0007 öğesini seçin.  
8. Olaylat bölümünü genişletin.
9. Stok yenileme olayı alanında "Toplu İş" öğesini seçin.
    * Bu, İlişkilendirme olayının işlenmesi sırasında ilgili konumda gereken malzemenin karşılanması için kanbanlar oluşturur.  

## <a name="set-the-minimum-quantity-for-the-item"></a>Madde için minimum miktarı ayarlayın
1. Ürün alanındaki bağlantıyı izlemek için tıklayın.
2. Madde numarası alanındaki bağlantıyı izlemek için tıklayın.
3. Ürün resmi bilgi kutusunu genişletin.
4. Eylem Bölmesinde, Planla öğesine tıklayın.
5. Madde kapsamı'na tıklayın.
6. Yeni'ye tıklayın.
7. Listede, seçili satırı işaretleyin.
8. Ambar alanında bir değer girin veya bir değer seçin.
    * Ambar'ı 12 olarak ayarlayın.  
9. Minimumu "200" olarak ayarlayın.

## <a name="run-the-batch-event-creation-job"></a>Toplu olay oluşturma işini çalıştırın
1. Üretim kontrolü > Dönemsel görevler > Kanban işi toplu işlemi > İlişkilendirme olayının işlenmesi'ne gidin.
2. Tamam'a tıklayın.
3. Ürün bilgi yönetimi > Yalın imalat > Kanban kuralları'na gidin.
4. Listede, seçili satırdaki bağlantıya tıklayın.
    * Daha önce oluşturduğunuz kanban kuralını seçin.  
5. Kanbanlar bölümünü genişletin.
    * Gerekli malzemeyi ambar 12'ye transfer etmek için bir kanban oluşturulduğuna dikkat edin.  

