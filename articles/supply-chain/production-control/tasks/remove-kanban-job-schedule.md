---
title: Kanban işini planlamadan kaldırma
description: Bu prosedür, bir planlanan işlem kanban işini, durumu Planlanmadı'ya döndürerek planlamadan kaldırmaya odaklanmaktadır.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3e9a512e7f391e08a35fd0eea449af12d81e644
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828598"
---
# <a name="remove-a-kanban-job-from-the-schedule"></a>Kanban işini planlamadan kaldırma

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]