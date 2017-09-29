--- 
title: "Kısmi konum döngü sayımı işlemini tanımlama "
description: "Sayım işi oluştururken döngü sayımı planları kullanırsanız, gerçek sayma operasyonunu, konumda bulunan eldeki stokların yerine yalnızca çeşitli ürünler ve ürün çeşitlerinin sayılmasına yönlendirebilirsiniz."
author: YuyuScheller
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 507a1147fea62c12490291362d365224efeda97e
ms.contentlocale: tr-tr
ms.lasthandoff: 07/28/2017

---
# <a name="define-partial-location-cycle-counting-process"></a>Kısmi konum döngü sayımı işlemini tanımlama  

[!include[task guide banner](../../includes/task-guide-banner.md)]

Sayım işi oluştururken döngü sayımı planları kullanırsanız, gerçek sayma operasyonunu, konumda bulunan eldeki stokların yerine yalnızca çeşitli ürünler ve ürün çeşitlerinin sayılmasına yönlendirebilirsiniz. Belirli ürünleri filtreleyerek, ambar yöneticisi inceleme yükünü azaltabilir, konsolidasyon hatalarının önlemeye yardımcı olabilir ve zaman tasarruf edebilir. Bir ambar yöneticisi tipik olarak kurulum görevlerini gerçekleştirir. Bu yordamı demo verileri şirketi USMF veya kendi verilerinizi kullanarak yerine getirebilirsiniz.


## <a name="create-a-cycle-counting-work-template"></a>Bir döngü sayımı iş şablonu oluşturun
1. Ambar yönetimi > Kurulum > İş > İş şablonları öğesine gidin.
2. İş siparişi türü alanında 'Döngü sayımı' seçin.
3. Yeni'ye tıklayın.
4. Sıra numarası alanına bir numara girin.
    * Sıralama düzeni en küçük sayıdan en büyük sayıyadır. Değer 0'dan (sıfır) fazla olmalıdır.  
5. Listede, seçili satırı işaretleyin.
6. İş şablonu alanında bir değer girin.
7. İş şablonu açıklaması alanında bir değer girin.
8. İş havuz kodu alanında bir değer girin veya bir değer seçin.
9. İş önceliği alanına bir sayı girin.
10. Kaydet'e tıklayın.
11. Yeni'ye tıklayın.
12. Listede, seçili satırı işaretleyin.
13. İş türü alanında 'Sayım'ı seçin.
14. İş sınıfı kodu alanına bir değer girin veya buradan bir değer seçin.
15. Kaydet'e tıklayın.
16. İş satırı molaları'na tıklayın.
17. Yeni'ye tıklayın.
18. Sıra numarası alanına bir numara girin.
    * Sıralama düzeni en küçük sayıdan en büyük sayıyadır. Değer 0'dan (sıfır) fazla olmalıdır.  
19. Kaydet'e tıklayın.
20. Sayfayı kapatın.
21. Sayfayı kapatın.

## <a name="create-a-cycle-counting-plan"></a>Bir döngü sayımı planı oluşturun
1. Ambar yönetimi > Kurulum > Döngü sayımı > Döngü sayımı planları öğesine gidin.
2. Yeni'ye tıklayın.
3. Döngü sayımı planı numarası alanına bir değer yazın.
4. Tanım alanına bir değer girin.
5. Maksimum döngü sayımı miktarı alanına bir sayı girin.
6. İş şablonu alanında bir değer girin veya bir değer seçin.
7. Yeni'ye tıklayın.
8. Sıra numarası alanına bir numara girin.
    * Sıralama düzeni en küçük sayıdan en büyük sayıyadır. Değer 0'dan (sıfır) fazla olmalıdır.  
9. Açıklama alanına bir değer girin.
10. Kaydet'e tıklayın.
11. Ürün sorgusu tanımla'ya tıklayın.
12. Listede, seçili satırı işaretleyin.
13. Ölçütler alanında bir değer girin veya seçin.
14. Tamam'a tıklayın.
15. Sayfayı kapatın.

