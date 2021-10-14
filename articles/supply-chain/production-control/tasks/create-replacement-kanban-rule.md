---
title: Değiştirme kanban kuralı oluşturma
description: Bu prosedürde mevcut bir kanban kuralının belirli bir tarihte yeni bir kanban kuralıyla nasıl değiştirileceği açıklanmıştır.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2db44c1b43a6dc5e0ab37a7756c4eecaab468e15
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570069"
---
# <a name="create-a-replacement-kanban-rule"></a>Değiştirme kanban kuralı oluşturma

[!include [banner](../../includes/banner.md)]

Bu prosedürde mevcut bir kanban kuralının belirli bir tarihte yeni bir kanban kuralıyla nasıl değiştirileceği açıklanmıştır. Bu, üretim akışındaki değişikliklerin veya stok yenileme kurallarının koordine edilmesi ve zamanlanması gerektiğinde kullanışlıdır. Prosedürün oluşturulması için kullanılan demo verisi şirketi USMF'dir. Bu yordam, değiştirilmiş bir üretim akışı ve yeni bir yenileme kuralı hazırlanırken kullanılması için işlem mühendisi veya değer akışı yöneticisi için hazırlanmıştır. Bu görev, 000022 kanban kuralını yeni bir kuralla değiştirir ve 48 olan maksimum miktarı yeni kural için 100'e yükseltir.


## <a name="select-a-kanban-rule-to-replace"></a>Değiştirilecek kanban kuralını seçme
1. Kanban kuralları'na gidin.
2. Listede, istenen kaydı bulun ve seçin.
    * 000022 kanban kuralını seçin.  

## <a name="create-a-replacement-kanban-rule"></a>Değiştirme kanban kuralı oluşturma
1. Kanban kuralını değiştir düğmesini tıklayın.
2. Yürürlük tarihi alanına bir tarih ve saat girin.
    * Örneğin bir hafta sonraki tarih gibi ileri bir tarih seçin. Bu, yeni kanban kuralının etkin olacağı ve eski kanban kuralının yerine geçeceği tarih ve saattir.  
    * Kanban kuralı, üretim akışındaki yolu değiştirirse, başka bir etkinlik seçilebilir.  Bu prosedürde etkinliği değiştirmeden bırakacağız.  
3. Tamam'a tıklayın.
    * Kanban kural 000022'nin değiştirilmesi için yeni bir kanban kuralının oluşturulacağına dikkat edin.  
    * Geçerlilik tarihi, kanban kuralı değiştirildiğinde seçilen tarihe göre ayarlanır.  
4. Listede, istenen kaydı bulun ve seçin.
    * 000022 değiştirilen kanban kuralını seçin.  
    * Değiştirilen kanban kuralının, geçerliliğin biteceği tarih olduğundan Bitiş tarihi ile aynı tarihe sahip olacağına dikkat edin.  
5. Listede satır 1'i seçin.
    * Listenin başından yeni kanban kuralını seçin. Bu, en büyük kanban kuralı numarasına sahip kanban kuralıdır.  
6. Listede, seçili satırdaki bağlantıya tıklayın.
    * Kanban kuralını açmak için kanban kuralı numarasını tıklatın.  

## <a name="modify-maximum-quantity-for-the-replacement-kanban-rule"></a>Kanban değiştirme kuralı için maksimum miktarı değiştirin
1. Maksimum miktarı '100' olarak ayarlayın.
    * Maksimum miktar alanını görüntülemek için Miktarlar Hızlı Sekmesini genişletin. Maksimum miktarın 100 olarak değiştirilmesi 100 kanban'a kadar işlenmesine izin verir.    Bu, bu görevdeki son adımdır.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]