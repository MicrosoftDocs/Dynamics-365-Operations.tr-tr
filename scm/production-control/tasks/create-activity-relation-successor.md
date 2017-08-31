--- 
title: "Faaliyet ilişkisi oluşturma: - Ardıl"
description: "Bir yalın imalat akışındaki faaliyetlerin akışı etkinlik ilişkileri üzerinden belgelenir."
author: cvocph
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
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 5ac47a00a8eb40658af54274ce1d80349ec23d1e
ms.contentlocale: tr-tr
ms.lasthandoff: 07/28/2017

---
# <a name="create-activity-relation-successor"></a>Faaliyet ilişkisi oluşturma: Ardıl

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bir yalın imalat akışındaki faaliyetlerin akışı etkinlik ilişkileri üzerinden belgelenir. Bu kayıt, bir etkinlik ilişkisinin nasıl oluşturulacağını gösterir.

Ön koşullar:

- Taslak modunda bir üretim akışı ve sürüm. 

- Üretim akışında birbirini izleyen iki faaliyet oluşturulur ancak ilişkilendirilmez.


## <a name="find-the-production-flow-version"></a>Üretim akışı sürümünü bul 
1. Üretim kontrolü > Kurulum > Yalın üretim akışı > Üretim akışları seçeneğine gidin.
2. Listede, istenen kaydı bulun ve seçin.
3. Listede, seçili satırdaki bağlantıya tıklayın.
4. Listede, seçili satırı işaretleyin.
5. Listede bir taslak sürüm seçin.
    * Faaliyet ilişkileri, üretim akışının hem taslak hem de etkin sürümlerine eklenebilir.  

## <a name="open-the-activity-overview"></a>Faaliyet genel bakışını aç
1. Faaliyetler'i tıklatın.
    * Formun, çalışmakta olduğunuz üretim akışı Sürümü için ayrılan tüm üretim akışı faaliyetlerini gösterdiğini unutmayın.  

## <a name="add-a-successor"></a>Bir Ardıl ekle
1. Ardıl ekle öğesini tıklatın.
2. Faaliyet alanında, aramayı açmak için açılır menü düğmesine tıklayın.
3. Listede, istenen kaydı bulun ve seçin.
4. Listede, seçili satırdaki bağlantıya tıklayın.
5. Sınırlama onay kutusunu işaretleyin.
6. Sınırlama değeri alanında bir numara girin.
    * Sınırlama süresi, öncelin zamanlanmış bitiş (vade tarihi ve saati) ve ardılın zamanlanmış başlangıç süresi arasında zamanlanacak süredir.  
7. Birimler alanında bir değer girin.
8. Döngü süresi oranı alanında bir sayı girin.
    * Her iki etkinlik de aynı takt'ta çalışırsa, döngü zamanı oranı 1 olmalıdır. Öncül, ardılın iki katı hızda çalışıyorsa, oran 2 olmalıdır.   Döngü zamanı oranları, üretim akışı etkinliklerinin ayrı ayrı döngü zamanlarını hesaplamakta kullanılır.  
9. Tamam'a tıklayın.
10. Sayfayı kapatın.
11. GridPanel sekmesini tıklatın.
12. Sayfayı kapatın.
13. Sayfayı yenileyin.


