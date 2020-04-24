---
title: Kanban kuralına kanban miktarı hesaplama ilkesi ekleme
description: Bu yordam, kanban miktarı hesaplama ilkesi oluşturma ve miktarları ve kanban boyutunu en iyi duruma getirmek için kanban kuralına eklemeye odaklanır.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanQuantityPolicy, KanbanRules
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 19f563379a10bbe42681a5f61779fb9e72d1f60c
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211020"
---
# <a name="add-a-kanban-quantity-calculation-policy-to-a-kanban-rule"></a>Kanban kuralına kanban miktarı hesaplama ilkesi ekleme

[!include [banner](../../includes/banner.md)]

Bu yordam, kanban miktarı hesaplama ilkesi oluşturma ve miktarları ve kanban boyutunu en iyi duruma getirmek için kanban kuralına eklemeye odaklanır. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu yordam değer akışı yöneticisi için hazırlanmıştır. Bu yordam kanban miktarı önerilerini hesapla yordamını oluşturmak için bir önkoşuldur. 


## <a name="create-a-kanban-quantity-calculation-policy"></a>Bir kanban miktar hesaplama ilkesi oluştur
1. Üretim kontrol > Periyodik görevler > Kanban miktarı hesaplama > Kanban miktarı hesaplama ilkeleri'ne gidin.
2. Yeni'ye tıklayın.
3. İsim alanına bir değer yazın.
    * Örneğin, Speaker2016 yazın.  
4. Master plan alanında, aramayı açmak için açılır menü düğmesine tıklayın.
5. Listede, istenen kaydı bulun ve seçin.
    * Talep hesaplamak için StaticPlan seçin.  
6. Listede, seçili satırdaki bağlantıya tıklayın.
7. Kaydet'e tıklayın.
8. Minimum kanban miktarı alanında '1' girin.
    * Bu, Kanban miktarı hesaplamasına dahil edilen ek kanban sayısıdır.  
9. Güvenlik faktörü'nü '1'e ayarlayın.
    * Bu, ek emniyet stoğu miktarını hesaplamak için kullanılan faktördür.  
10. Gün sonra alanına, '30' girin.
    * Bu, talebin hesaplamaya dahil edildiği kanban miktarı hesaplama tarihinden geriye doğru gün sayısıdır.  
11. Geride kalan gün alanına '30' girin.
    * Bu, talebin hesaplamaya dahil edildiği kanban miktarı hesaplama tarihinden ileriye doğru gün sayısıdır.  Hesaplanmada kullanılan formül gerçek değerlerle gösterilir. Örneğin, Kanban miktarı = ((Ortalama günlük talep x bekleme süresi x 2,00) / Malzeme işleme birimi başına ürün miktarı) + 1  
12. Sayfayı kapatın.

## <a name="add-the-kanban-quantity-calculation-policy-to-a-kanban-rule"></a>Kanban miktar hesaplama ilkesini bir kanban kuralına ekleyin.
1. Ürün bilgi yönetimi > Yalın imalat > Kanban kuralları'na gidin.
2. Listede, istenen kaydı bulun ve seçin.
    * Bu yordam için kanban kuralı 000020'yi seçin.  
3. Listede, seçili satırdaki bağlantıya tıklayın.
4. Kanban miktarı hesaplama ilkeleri bölümün genişlemesini değiştirin.
5. Ekle öğesini tıklatın.
    * Önceki alt görevde oluşturduğunuz kanban miktarı hesaplama ilkesini ekleyin.  
6. Listede, seçili satırı işaretleyin.
7. Ad alanında, açılır menü düğmesine tıklayarak aramayı açın.
8. Listede, seçili satırdaki bağlantıya tıklayın.
    * Önceki alt görev oluşturduğunuz Speaker2016 ilkesini seçin.  

