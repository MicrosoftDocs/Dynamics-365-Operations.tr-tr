--- 
title: "Kanban işini planlamadan kaldırma"
description: "Bu prosedür, bir planlanan işlem kanban işini, durumu Planlanmadı'ya döndürerek planlamadan kaldırmaya odaklanmaktadır."
author: ChristianRytt
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
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9a0f246bfe42dde0befdf5c4f01d2ad1e1200b12
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="remove-a-kanban-job-from-the-schedule"></a>Kanban işini planlamadan kaldırma

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Bu prosedür, bir planlanan işlem kanban işini, durumu Planlanmadı'ya döndürerek planlamadan kaldırmaya odaklanmaktadır. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu prosedür atölye gözetmenlerine veya üretim planlayıcılarına yöneliktir.


## <a name="find-a-planned-kanban-job"></a>Planlanmış bir kanban işi bulun
1. Üretim denetimi > Kanban > Kanban işi planlaması'na gidin.
2. İş hücresi alanında, açılır menü düğmesine tıklayarak aramayı açın.
3. Listede, seçili satırdaki bağlantıya tıklayın.
    * İş hücresi 1250'yi seç  
4. Seç'e tıklayın.
5. İş durumunu görüntüle alanında "Planlandı"yı seçin.

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a>Planlanmış kanban işini planlamadan kaldırın
1. Listede, istenen kaydı bulun ve seçin.
    * Örneğin, 19 Aralık 2012'den, Planlandı durumunda olan bir işi seçin.  
2. Eylem Bölmesinde, Planla öğesine tıklayın.
3. İş durumunu geri al'a tıklayın.
4. Tamam'a tıklayın.
    * Bu, geçerli işin "Planlandı" olan durumunu "Planlanmadı"ya döndürür ve işlem panosundan kaldırır.   


