---
title: Kanban işlerini planlama
description: Bu prosedür, belirli bir iş hücresi için kanban işlerini zamanlama işlemine odaklanmaktadır.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, KanbanPeriodCapacityPart, SysLookupMultiSelectGrid, KanbanBoardScheduleJobForward
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3a56bca460af229b53d41959d48562ef425c0bf7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843493"
---
# <a name="schedule-kanban-jobs"></a>Kanban işlerini planlama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu prosedür, belirli bir iş hücresi için kanban işlerini zamanlama işlemine odaklanmaktadır. "Malzemeler kullanılabilir olmadığında bir kanban işi hazırla" prosedürü, bu prosedürü oluşturmanın bir önkoşuldur. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu görev, kanbanlarla çalışan atölye gözetmenlerine ve üretim planlayıcılarına yöneliktir.


## <a name="select-kanban-jobs-for-a-work-cell"></a>Bir iş hücresi için kanban işlerini seçin
1. Üretim denetimi > Kanban > Kanban işi planlaması'na gidin.
2. Dönem kapasitesi olgu kutusunu genişletin
    * Kanban bilgi kutusunu genişletin.  
3. İş hücresi alanında, açılır menü düğmesine tıklayarak aramayı açın.
4. Listede, seçili satırı işaretleyin.
    * İş hücresi 1250'yi seç Bu, görünümü filtreleyerek sadece 1250 iş hücresi için olan işler görüntülenir.  
5. Listede, seçili satırdaki bağlantıya tıklayın.
6. Seç'e tıklayın.

## <a name="schedule-a-kanban-job-in-the-first-available-period"></a>Kanban işini ilk kullanılabilir dönemde zamanlayın.
1. Listede, seçili satırı işaretleyin.
    * Listede "Planlanmadı" durumunda olan ilk satırı seçin. İş durumu alanındaki noktalı simge Planlanmadı durumunu gösterir.  
2. Planla'ya tıklayın.
    * Bu, kanban işini ilk kullanılabilir dönemde zamanlar.  
    * Kanban işinin listede son sıraya taşındığına dikkat edin çünkü bugünden başlayan döneme eklenmiştir.  
    * Dönem bugünden başlayarak tamamen doluysa, iş ilk kullanılabilir döneme taşınır.  

## <a name="schedule-two-kanban-jobs-for-a-specific-day"></a>Belirli bir gün için iki kanban işini zamanlayın
1. Listede satır 1'i seçin.
    * İlk satırın İş durumu alanındaki değerinin Planlanmadı olduğunu göreceksiniz.  
2. Listede satır 2'yi seçin.
    * İkinci satırın İş durumu alanındaki değerinin Planlanmadı olduğunu göreceksiniz. Şimdi ilk iki işi seçmiş durumdasınız.  
3. Zaman çizelgesi başlangıç tarihi'ne tıklayarak, açılır iletişim kutusunu açın.
4. Kapasite eksikliği tepkisini geçersiz kıl kutusunu işaretleyin veya kutunun işaretini kaldırın.
    * Bu seçenek, varsayılan kapasite eksikliğine tepkiyi geçersiz kılmanıza olanak sağlar.  
5. Kapasite eksikliğine tepki alanında, "Talep edilen döneme ekle"yi seçin.
    * Bu seçenek, iş hücresinin aşırı yüklü olup olmamasına bakılmaksızın, işin istenen döneme eklenmesini sağlar.  
6. Planla'ya tıklayın.
    * Her iki işin istenen öneme eklendiğine dikkat edin.  
    * Dönem kapasitesi bölümünde, her bir dönemin yükünü görebilirsiniz. Tüketim alanı bu dönemde zamanlanan tüketimi gösterir. Zamanlanmış tüketim bu dönemdeki kullanılabilir kapasiteden daha yüksekse, aşırı yüklenmiş tüketim seçilecektir.  

