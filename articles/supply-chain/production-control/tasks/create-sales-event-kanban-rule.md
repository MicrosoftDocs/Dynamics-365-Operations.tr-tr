---
title: Satış olayı kanban kuralı oluşturma
description: Bu yordam, satış siparişi oluşturma sırasında tetiklenecek bir kanban kuralı oluşturmak için gereken ayarlara odaklanır.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d2bee6e81acd029406c95237f0b4ba4ab2565ea1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1573079"
---
# <a name="create-a-sales-event-kanban-rule"></a>Satış olayı kanban kuralı oluşturma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, satış siparişi oluşturma sırasında tetiklenecek bir kanban kuralı oluşturmak için gereken ayarlara odaklanır. Olay kanbanı kuralı, satış siparişi satırlarından kaynaklanan gereksinimleri yeniler. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Yeni veya değiştirilmiş bir ürünün üretimine hazırlanırken kullanılması için işlem mühendisi veya değer akışı yöneticisi için hazırlanmıştır.




## <a name="create-a-new-kanban-rule"></a>Yeni bir kanban kuralı oluştur
1. Kanban kuralları'na gidin.
2. Yeni'ye tıklayın.
3. Yenileme stratejisi alanında 'Olay' öğesini seçin.
    * Olay seçilmesi, kanban kuralının bir olay tarafından (örneğin, bir satış siparişi satırı oluşturulması) tetikleneceği anlamına gelir.   Bu, her bir kanbanın belirli bir isteği kapsaması gereken alanlara uygulanır.  
4. İlk plan alanında bir değer girin veya bir değer seçin.
    * Son Derleme öğesini seçin.  
5. Ayrıntılar bölümünü genişletin.
6. Ürün alanında bir değer girin veya bir değer seçin.
    * L0050 öğesini seçin.  

## <a name="define-an-event"></a>Bir olay tanımla
1. Olaylat bölümünü genişletin.
2. Satış olayı alanında 'Otomatik' öğesini seçin.
    * Satış olayı Otomatik olarak seçilerek, bir satış satırı ürün ve giriş konumuyla eşleştiğinde bu kanban kuralı otomatik olarak tetiklenir. Bu yordamda, ambar 13'te ürün L0050'dir.  
3. Minimum olay miktarını '50' olarak ayarlayın.
    * 50 minimum olay miktarı ile, kanban kuralı yalnızca 50 veya daha fazla bir miktarda olay olduğunda tetiklenir.  
4. Üretim akışı bölümünü genişletin.
    * Giriş konumunun ambar 13 olduğuna dikkat edin. Bunun anlamı kanban kuralın bu konum için tetikleneceğidir.  
    * Bu örnekte, ambar 13'te bulunan 50 veya daha fazla miktardaki L0050 ürünü bu kanban kuralını tetikler.  

## <a name="create-sales-line-to-trigger-event-kanban-rule"></a>Olay kanbanı kuralı tetiklemek için satış satırı oluştur
1. Tüm satış siparişleri'ne gidin.
    * Kanban kuralı kaydedildiğinde bir uyarı gösterilir, bunun anlamı kanbanların satış siparişi oluşturma sırasında gerçek zamanlı oluşturulacağıdır.  
2. Yeni'ye tıklayın.
3. Müşteri hesabı alanında bir değer girin veya seçin.
    * Örneğin, ABD-003 öğesini seçin.  
4. Tamam'a tıklayın.
5. Madde numarası alanına 'L0050' girin.
6. Tesis alanında '1' girin.
    * Ambar 13 Site 1'de olduğundan Site 1'i seçin.  
7. Ambar alanında bir değer girin veya bir değer seçin.
    * Ambar'ı 13 olarak ayarlayın.  
8. Miktarı '75' olarak ayarlayın.
    * Oluşturulan kanban kuralını tetiklemek için 50 veya daha yüksek değerde miktar girin.  

## <a name="verify-that-kanban-is-created"></a>Kanbanın oluşturulduğunu doğrula
1. Ürün ve tedarik seçeneğine tıklayın.
2. İlişkilendirme ağacını görüntüle'yi tıklatın.
    * Satış satırıyla aynı miktara sahip bir kanban oluşturulduğuna dikkat edin. L0050 üretmek için gereken malzeme sorunlarını da görebilirsiniz. Bu yordamın son aşamasıdır.  

