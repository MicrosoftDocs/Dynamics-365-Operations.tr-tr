---
title: Kanban satır olayı kullanarak kanban kuralı oluşturma
description: Bu yordam, bir işlem etkinliğinden çekmeyi tetiklemek için kanban satır olayı ayarını kullanarak bir kanban kuralı oluşturur.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3b6a589d95fde61cbd6743f9e3e3170a1b8d6f91613cde0df94037872b491018
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746903"
---
# <a name="create-a-kanban-rule-using-a-kanban-line-event"></a>Kanban satır olayı kullanarak kanban kuralı oluşturma

[!include [banner](../../includes/banner.md)]

Bu yordam, bir işlem etkinliğinden çekmeyi tetiklemek için kanban satır olayı ayarını kullanarak bir kanban kuralı oluşturur. Miktarın 25'e eşit veya 25'ten daha büyük olduğu her durumda kanban kuralı, bir kanban işlem etkinliği tarafından tetiklenir. Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu görev, yalın bir ortamda yeni veya değiştirilmiş bir ürünün üretimine hazırlanırken kullanılması için işlem mühendisi veya değer akışı yöneticisi için hazırlanmıştır.


## <a name="create-a-kanban-rule"></a>Kanban kuralı oluşturun
1. Ürün bilgi yönetimi > Yalın imalat > Kanban kuralları'na gidin.
2. Yeni'ye tıklayın.
3. Yenileme stratejisi alanında 'Olay' öğesini seçin.
    * Bu işlem talepten doğrudan kanbanlar oluşturur. Siparişe göre üretim senaryosunu tanımlayan kuralları ayarlamak için kullanılır.  
4. İlk plan alanında bir değer girin veya bir değer seçin.
    * SpeakerAssemblyAndPolish öğesini girin veya seçin. Üretim kanban kuralının ilk etkinliği üretim akışında bir işleme etkinliğidir. Bir etkinlik seçtiğinizde, etkinliğin geçerlilik tarihleri kanban kuralının geçerlilik tarihlerine kopyalanır.  
5. Ayrıntılar bölümünü genişletin.
6. Ürün alanına "L0001" yazın.
7. Olaylat bölümünü genişletin.
8. Kanban satır olayı alanında "Otomatik" öğesini seçin.
    * Bu işlem istek üzerinde olay kanbanları oluşturur.  Aşağı doğru işleme etkinliği için gerekli olan malzemeyi yenileyen kanban kurallarını yapılandırmak için bu alan kullanılır. Otomatik'i seçtiğinizde taleple birlikte olay kanbanları oluşturulur. Üretimi aynı gün gerçekleştirmeyi bekliyorsanız bu ayar önerilir.  
9. Minimum olay miktarını '25' olarak ayarlayın.
    * Olay kanbanları, talep miktarı bu alana eşit veya bu alandan fazla olduğunda oluşturulur. Bu özellik, bir makinede bu alandan daha az sipariş miktarı ve başka bir makinede bu alandan daha fazla sipariş miktarı üretmek istediğinizde kullanışlıdır.  
10. Kaydet'e tıklayın.

## <a name="create-sales-order-and-trigger-kanban-chain"></a>Satış siparişi oluşturun ve kanban zincirini tetikleyin
1. Sales and marketing > Sales orders > All sales orders (Satış ve pazarlama > Satış siparişleri > Tüm satış siparişleri) menüsüne gidin.
2. Yeni'ye tıklayın.
3. Müşteri hesabı alanında bir değer girin veya seçin.
    * US-003, Forest Wholesales Müşteri hesabını seçin.  
4. Tamam'a tıklayın.
5. Madde numarası alanına 'L0001' girin.
    * L0001, kanban kuralını oluşturduğunuz maddedir.  
6. Miktarı '27' olarak ayarlayın.
    * Kanban kuralında 27, minimum miktar olan 25'ten daha büyük olduğundan bu bir olay kanbanını tetikler.  
7. Tesis alanında '1' girin.
8. Ambar alanında bir değer girin veya bir değer seçin.
    * Ambar 13'ü seçin.  
9. Kaydet'e tıklayın.

## <a name="view-the-kanban-generated-by-the-kanban-rule"></a>Kanban kuralı tarafından oluşturulan kanbanı görüntüleyin
1. Ürün bilgi yönetimi > Yalın imalat > Kanban kuralları'na gidin.
2. Listede, istenen kaydı bulun ve seçin.
3. Kanbanlar bölümünü genişletin.
    * Oluşturulan kanban kuralına bağlı olarak etkinliği işlemek amacıyla 27 için bir kanban oluşturulduğuna dikkat edin.  
    * Bu son adımdır.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]