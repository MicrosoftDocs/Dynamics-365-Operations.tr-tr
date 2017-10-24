--- 
title: "Maliyet yuvarlaması ilkesi oluşturma"
description: "Bu yordam, bir maliyet yuvarlama ilkesini oluşturmayı ve ilke için kurallar oluşturmayı gösterir."
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 42656cbf445fd3f79844884d7d35243c5b051a4a
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-cost-rollup-policy"></a>Maliyet yuvarlaması ilkesi oluşturma

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


