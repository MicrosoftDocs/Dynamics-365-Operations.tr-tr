---
title: İmalat için sabit miktarlı kanban kuralı oluşturma
description: Bu yordam, bir iş hücresinde, yalın bir imalat ortamında dönüşen etkinlikleri tetiklemek üzere sabit üretim oluşturmak için gereken ayarlara odaklanır.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 540df772f132f60c9d8e7e937e72d3f51f6759ab
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255265"
---
# <a name="create-a-fixed-quantity-kanban-rule-for-manufacturing"></a>İmalat için sabit miktarlı kanban kuralı oluşturma

[!include [banner](../../includes/banner.md)]

Bu yordam, bir iş hücresinde, yalın bir imalat ortamında dönüşen etkinlikleri tetiklemek üzere sabit üretim oluşturmak için gereken ayarlara odaklanır. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu yordam, yeni veya değiştirilmiş bir ürünün üretimine hazırlanırken kullanılması için İşlem Mühendisi veya Değer Akışı Yöneticisi için hazırlanmıştır.


## <a name="create-new-kanban-rule"></a>Yeni kanban kuralı oluştur
1. Kanban kuralları'na gidin.
2. Yeni'ye tıklayın.
    * Varsayılan Tür olarak Üretim'in ve Stok yenileme stratejisi olarak Sabit ayarlandığını göz ardı etmeyin. Bu parametreleri değiştirmek zorunda değilsiniz.  
3. İlk plan alanında bir değer girin veya bir değer seçin.
    * Bu eylem, kanban kuralına dayalı olarak oluşturulan kanbanlar için gerçekleştirilir.  'SpeakerTestAndPackaging' öğesini seçin.  
4. Ayrıntılar bölümünü genişletin.
5. Ürün alanında bir değer girin veya bir değer seçin.
    * L0050 öğesini seçin.  
6. Ölçü birimi alanında bir değer girin veya bir değer seçin.
    * Dakika'yı seçin.  
7. Sağlama süresi alanında bir sayı girin.
    * 5 girin.  

## <a name="set-quantities"></a>Miktarları ayarla
1. Miktarlar bölümünü genişletin.
2. Varsayılan mktarı '10' olacak şekilde ayarlayın.
    * Bu, her kanban için transfer edilecek miktardır.  
3. Ürün miktar farkı onay kutusunu işaretleyin.
    * Bununla, seçili kanbanlar varsayılan miktardan bir sapmayla tamamlanabilir.  Kanbanların 8-12 miktarıyla tamamlanmasını sağlamak için her iki sapmayı da 2 olarak ayarlayın.  
4. Aşağıdaki Fark değerini '2' olarak ayarlayın.
    * Bu, daha düşük şekilde 10 - 2 = 8 olarak tamamlanmasını sağlar.  
5. Yukarıdaki Fark değerini'2' olarak ayarlayın.
    * Bu, daha yüksek şekilde 10 + 2 = 12 olarak tamamlanmasını sağlar.  
6. Sabit kanban miktarı alanında bir sayı girin.
    * Bu, kanbanların etkin olması gereken tutardır. Bu durumda, her 10 tane için 5 kanban işlenir.  
7. Uyarı sınırı minimumı alanında '2' girin.
    * Hedefte olması gereken tam kanbanların minimum tutarını izlemek için kullanılır. Örneğin, bu kanban tutarının genel görünümüne ilişkin kullanılır.  
8. Uyarı sınırı maksimumu alanında '4' girin.
    * Hedefte olması gereken tam kanbanların maksimum tutarını izlemek için kullanılır. Örneğin, bu kanban tutarının genel görünümüne ilişkin kullanılır.  
9. Otomatik planlama miktarı alanında '1' girin.
    * Bunun 1 olarak ayarlanması her bir kanbanın otomatik olarak planlanacağını gösterir.   3 girildiyse, 3 boş kanban planlama için hazır olana kadar kanbanlar planlanmaz. Bu, işleri gruplamak ve çok fazla ayar yapmanın önüne geçmek için yararlıdır.  

## <a name="create-kanbans"></a>Kanban Oluştur
1. Kanbanlar bölümünü genişletin.
2. Kaydet'e tıklayın.
    * Kanbanlar oluşturulmadan önce kanban kuralının kaydedilmesi gerekir.  
3. Ekle öğesini tıklatın.
    * Etkin kanban olmadığını, bu nedenle de 'Önerilen yeni kanban sayısı'nın 5 olduğuna dikkat edin. Bu, 'Sabit kanban miktarı'na eşittir.  
4. Oluştur'a tıklayın.
    * Bu, 5 kanban oluşturur.  
    * Bu üretim kanbanı kuralı için her 10 başına 5 kanban oluşturulduğunu unutmayın. Bu yordamın son aşamasıdır.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]