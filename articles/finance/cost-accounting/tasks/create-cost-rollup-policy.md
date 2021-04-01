---
title: Maliyet yuvarlaması ilkesi oluşturma
description: Bu yordam, bir maliyet yuvarlama ilkesini oluşturmayı ve ilke için kurallar oluşturmayı gösterir.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6505d658103a4c34dfe7c7eb86ad4ea41515ccfb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5261296"
---
# <a name="create-a-cost-rollup-policy"></a>Maliyet yuvarlaması ilkesi oluşturma

[!include [banner](../../includes/banner.md)]

Bu yordam, bir maliyet yuvarlama ilkesini oluşturmayı ve ilke için kurallar oluşturmayı gösterir. Bu yöntemi oluşturmak için kullanılan demo verisi USP2'dir.


## <a name="create-a-policy"></a>Bir ilke oluşturun
1. Maliyet muhasebesi > İlkeler > Maliyet yuvarlama ilkeleri'ne gidin.
2. Yeni'ye tıklayın.
3. İlke adı alanına bir değer girin.
4. Açıklama alanına bir değer girin.
5. Maliyet nesnesi boyut hiyerarşisi alanına bir değer girin veya bir değer seçin.
    * Maliyet yuvarlama CC'yi seçin.  
6. Maliyet öğesi boyut hiyerarşisi alanına bir değer girin veya bir değer seçin.
    * Maliyet yuvarlama CC'yi seçin.  
7. Kaydet'e tıklayın.

## <a name="create-rules-for-the-cost-rollup-policy"></a>Maliyet yuvarlama ilkesi için kurallar oluşturun
1. Yeni'ye tıklayın.
2. Listede, seçili satırı işaretleyin.
3. Maliyet nesnesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.
    * 007'yi seçin.  
4. Maliyet öğesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.
    * Maliyet yuvarlama CE'yi seçin.  
5. İkincil maliyet öğesi alanına bir değer girin veya bir değer seçin.
    * Bu örnek için, ikincil maliyet öğesi CC-007'yi maliyet merkezine eşleyin.  
6. Yeni'ye tıklayın.
7. Listede, seçili satırı işaretleyin.
8. Maliyet nesnesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.
    * 008'yi seçin.  
9. Maliyet öğesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.
    * Maliyet yuvarlama CE'yi seçin.  
10. İkincil maliyet öğesi alanına bir değer girin veya bir değer seçin.
    * Bu örnek için, ikincil maliyet öğesi CC-008'yi maliyet merkezine eşleyin.  
11. Yeni'ye tıklayın.
12. Listede, seçili satırı işaretleyin.
13. Maliyet nesnesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.
    * 009'yi seçin.  
14. Maliyet öğesi boyut hiyerarşi düğümü alanına bir değer girin veya bir değer seçin.
    * Maliyet yuvarlama CE'yi seçin.  
15. İkincil maliyet öğesi alanına bir değer girin veya bir değer seçin.
    * Bu örnek için, ikincil maliyet öğesi CC-009'yi maliyet merkezine eşleyin.  
    * Tüm maliyet merkezleri karşılık gelen ikincil maliyet öğelerine eşlenene kadar devam edin.  
16. Kaydet'e tıklayın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]