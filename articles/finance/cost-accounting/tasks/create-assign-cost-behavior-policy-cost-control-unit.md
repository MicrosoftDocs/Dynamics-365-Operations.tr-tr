---
title: Maliyet davranış ilkesi oluşturma ve bir maliyet kontrol birimine atama
description: Maliyet davranışı, maliyetlerin sabit veya değişken olarak sınıflandırılmasıdır.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e923bd4e8f89aa9398b6327fe28998f845218d4
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144416"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a>Maliyet davranış ilkesi oluşturma ve bir maliyet kontrol birimine atama

[!include [banner](../../includes/banner.md)]

Maliyet davranışı, maliyetlerin sabit veya değişken olarak sınıflandırılmasıdır. İlkenin etkin hale gelmesi için bir ilke ve karşılık gelen kurallarının bir maliyet kontrol birimine atanmış olması gerekir. Bu yordamı bir ilke oluşturmak ve sonra ilkeyi bir maliyet kontrol birimine atamak için kullanın.


## <a name="create-a-cost-behavior-hierarchy"></a>Bir maliyet davranış hiyerarşisi oluşturun
1. Maliyet muhasebesi > Boyutlar > Boyut hiyerarşileri'ne gidin.
2. Yeni'ye tıklayın.
3. Oluştur'a tıklayın.
4. Boyut hiyerarşisi adı alanında 'Maliyet davranış hiyerarşisi' yazın.
5. Boyut alanına bir değer girin veya buradan bir değer seçin.
    * Maliyet öğelerini seçin.  
6. Kaydet'e tıklayın.
7. Hiyerarşiyi görüntüle düğmesini tıklayın.
8. Yeni'ye tıklayın.
9. Düğüm adı alanına bir değer girin.
    * Sabit maliyet girin.  
10. Ağaçta 'Maliyet davranış hiyerarşisi' seçin.
11. Yeni'ye tıklayın.
12. Düğüm adı alanına bir değer girin.
    * Değişken maliyet girin.  
13. Kaydet'e tıklayın.
14. Ağaçta 'Maliyet davranış hiyerarşisi\Sabit maliyet' seçin.
15. Yeni'ye tıklayın.
16. Listede, seçili satırı işaretleyin.
17. Gelen boyutu üyesi alanına bir değer girin veya bir değer seçin.
    * Boyut üyelerinin aralığı boşluklar içerebilir ancak üyeler üst üste gelemez.  
18. Boyuta üyesi alanına bir değer girin veya bir değer seçin.
    * Boyut üyelerinin aralığı boşluklar içerebilir ancak üyeler üst üste gelemez.  
19. Ağaçta 'Maliyet davranış hiyerarşisi\Değişken maliyet' seçin.
20. Yeni'ye tıklayın.
21. Listede, seçili satırı işaretleyin.
22. Gelen boyutu üyesi alanına bir değer girin veya bir değer seçin.
    * Boyut üyelerinin aralığı boşluklar içerebilir ancak üyeler üst üste gelemez.  
23. Boyuta üyesi alanına bir değer girin veya bir değer seçin.
    * Boyut üyelerinin aralığı boşluklar içerebilir ancak üyeler üst üste gelemez.  
24. Kaydet'e tıklayın.

## <a name="create-the-policy-and-rules"></a>İlkeyi ve kuralları oluşturun
1. Maliyet muhasebesi > İlkeler > Maliyet davranış ilkeleri'ne gidin.
2. Yeni'ye tıklayın.
3. İlke adı alanına bir değer girin.
4. Maliyet öğesi boyut hiyerarşisi alanına bir değer girin veya bir değer seçin.
    * Yeni oluşturduğunuz ilke hiyerarşisini seçin.  
5. Maliyet nesnesi boyut hiyerarşisi alanına bir değer girin veya bir değer seçin.
    * Kuruluşu seçin.  
6. Kaydet'e tıklayın.
7. Yeni'ye tıklayın.
8. Listede, seçili satırı işaretleyin.
9. Maliyet öğesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.
    * Değişken maliyeti seçmek için hiyerarşiyi genişletin.  
10. Maliyet nesnesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.
    * Varsayılan olarak, değişken yüzdesi 100'dür.  
11. Maliyet kontrol birimi için ilke atamaları'na tıklayın.
12. Yeni'ye tıklayın.
13. Listede, seçili satırı işaretleyin.
14. Geçerlilik tarihi muhasebe veri alanına bir tarih girin.
    * Kurallar tarihe dayalıdır ve kullanıcı veya sistem kuralın süresini, daha yeni bir sürüm oluşturulursa doldurulabilir.  
15. Maliyet kontrol birimi alanına bir değer girin veya bir değer seçin.
16. Kaydet'e tıklayın.

