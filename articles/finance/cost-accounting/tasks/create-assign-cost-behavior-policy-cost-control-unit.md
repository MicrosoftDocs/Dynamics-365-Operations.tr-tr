---
title: Maliyet davranış ilkesi oluşturma ve bir maliyet kontrol birimine atama
description: Maliyet davranışı, maliyetlerin sabit veya değişken olarak sınıflandırılmasıdır.
author: twheeloc
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostBehaviorRule
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 653bfb69c4ca118c700755cb95a6b349d2c6bbad
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735156"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a>Maliyet davranış ilkesi oluşturma ve bir maliyet kontrol birimine atama

[!include [banner](../../includes/banner.md)]

Maliyet davranışı, maliyetlerin sabit veya değişken olarak sınıflandırılmasıdır. İlkenin etkin hale gelmesi için bir ilke ve karşılık gelen kurallarının bir maliyet kontrol birimine atanmış olması gerekir. Bu yordamı bir ilke oluşturmak ve sonra ilkeyi bir maliyet kontrol birimine atamak için kullanın.


## <a name="create-a-cost-behavior-hierarchy"></a>Bir maliyet davranış hiyerarşisi oluşturun
1. **Maliyet muhasebesi > Boyutlar > Boyut hiyerarşileri**'ne gidin.
2. **Yeni**'yi tıklatın.
3. **Oluştur**'a tıklayın.
4. **Boyut hiyerarşisi adı** alanında 'Maliyet davranış hiyerarşisi' yazın.
5. **Boyut** alanına bir değer girin veya buradan bir değer seçin.
    * Maliyet öğelerini seçin.  
6. **Kaydet**'e tıklayın.
7. **Hiyerarşiyi görüntüle** düğmesini tıklayın.
8. **Yeni**'yi tıklatın.
9. **Düğüm adı** alanına bir değer girin.
    * Sabit maliyet girin.  
10. Ağaçta 'Maliyet davranış hiyerarşisi' seçin.
11. **Yeni**'yi tıklatın.
12. **Düğüm adı** alanına bir değer girin.
    * Değişken maliyet girin.  
13. **Kaydet**'e tıklayın.
14. Ağaçta 'Maliyet davranış hiyerarşisi\Sabit maliyet' seçin.
15. **Yeni**'yi tıklatın.
16. Listede, seçili satırı işaretleyin.
17. **Kaynak boyut üyesi** alanında bir değer girin veya bir değer seçin.
    * Boyut üyelerinin aralığı boşluklar içerebilir ancak üyeler üst üste gelemez.  
18. **Hedef boyut üyesi** alanında bir değer girin veya bir değer seçin.
    * Boyut üyelerinin aralığı boşluklar içerebilir ancak üyeler üst üste gelemez.  
19. Ağaçta 'Maliyet davranış hiyerarşisi\Değişken maliyet' seçin.
20. **Yeni**'yi tıklatın.
21. Listede, seçili satırı işaretleyin.
22. **Kaynak boyut üyesi** alanında bir değer girin veya bir değer seçin.
    * Boyut üyelerinin aralığı boşluklar içerebilir ancak üyeler üst üste gelemez.  
23. **Hedef boyut üyesi** alanında bir değer girin veya bir değer seçin.
    * Boyut üyelerinin aralığı boşluklar içerebilir ancak üyeler üst üste gelemez.  
24. **Kaydet**'e tıklayın.

## <a name="create-the-policy-and-rules"></a>İlkeyi ve kuralları oluşturun
1. **Maliyet muhasebesi > İlkeler > Maliyet davranış ilkeleri**'ne gidin.
2. **Yeni**'yi tıklatın.
3. **İlke adı** alanına bir değer girin.
4. **Maliyet öğesi boyut hiyerarşisi** alanına bir değer girin veya bir değer seçin.
    * Yeni oluşturduğunuz ilke hiyerarşisini seçin.  
5. **Maliyet nesnesi boyut hiyerarşisi** alanına bir değer girin veya bir değer seçin.
    * Kuruluşu seçin.  
6. **Kaydet**'e tıklayın.
7. **Yeni**'yi tıklatın.
8. Listede, seçili satırı işaretleyin.
9. **Maliyet öğesi boyut hiyerarşi düğümü** alanına bir değer girin veya bir değer seçin.
    * Değişken maliyeti seçmek için hiyerarşiyi genişletin.  
10. **Maliyet nesnesi boyut hiyerarşi düğümü** alanına bir değer girin veya bir değer seçin.
    * Varsayılan olarak, değişken yüzdesi 100'dür.  
11. **Maliyet kontrol birimi için ilke atamaları**'na tıklayın.
12. **Yeni**'yi tıklatın.
13. Listede, seçili satırı işaretleyin.
14. **Muhasebe tarihinden itibaren geçerli** alanına bir tarih girin.
    * Kurallar tarihe dayalıdır ve kullanıcı veya sistem kuralın süresini, daha yeni bir sürüm oluşturulursa doldurulabilir.  
15. **Maliyet kontrol birimi** alanına bir değer girin veya bir değer seçin.
16. **Kaydet**'e tıklayın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
