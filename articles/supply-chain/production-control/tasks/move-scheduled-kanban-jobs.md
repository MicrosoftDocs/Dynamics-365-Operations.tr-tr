---
title: Planlanmış kanban işlerini taşıma
description: Bu prosedür, planlanan işlem kanban işlerini farklı bir döneme taşımaya odaklanmaktadır.
author: ChristianRytt
ms.date: 11/07/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d58ee740824809f15da68db66616bb01d5dbfab
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825026"
---
# <a name="move-scheduled-kanban-jobs"></a>Planlanmış kanban işlerini taşıma

[!include [banner](../../includes/banner.md)]

Bu prosedür, planlanan işlem kanban işlerini farklı bir döneme taşımaya odaklanmaktadır. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu prosedür, kanbanlarla çalışan atölye gözetmenlerine veya üretim planlayıcılarına yöneliktir.

## <a name="select-scheduled-kanban-jobs"></a>Planlanmış kanban işlerini seçin. 

1. **Üretim denetimi > Kanban > Kanban işi planlaması**'na gidin. 

2. **İş hücresi** alanında, açılır menü düğmesine tıklayarak aramayı açın. 

3. Listede, seçili satırı işaretleyin. 
   - İş hücresi 1250'yi seç 
4. **Seç**'e tıklayın. 

5. **İş durumunu görüntüle** alanında **Planlandı**'yı seçin. Bu, yalnızca zamanlanmış kanban işlerini görüntülemek üzere iş listesine filtre uygular. 

## <a name="move-kanban-jobs-to-a-different-period"></a>Kanban işlerini başka bir döneme taşıyın. 

1. Listede, istenen kaydı bulun ve seçin. İş durumu **Planlanan iş** olan bir iş seçin. Örneğin **Planlanan dönem** alanında bir iş 20 Aralık 2012 tarihine zamanlanmıştır. Bu durumda işi önceki döneme taşıyın. 

2. **Önceki dönem**'i tıklayın. 

3. İşi önceki dönemin son işi olarak iş listesinin sonuna taşımak için **Sonlandır** üzerine tıklayın. 

4. Listede, istenen kaydı bulun ve seçin. İş durumu **Planlanan iş** olan bir iş seçin. Örneğin **Planlanan dönem** alanında bir iş 18 Aralık 2012 tarihine zamanlanmıştır. Bu durumda işi sonraki döneme taşıyın. 

5. **Sonraki dönem**'i tıklayın. 

6. İşi önceki dönemin işi olarak iş listesinin başına taşımak için **Başlat** üzerine tıklayın. 

## <a name="move-a-job-within-a-period"></a>Bir işi dönem içinde taşıyın. 

1. Listede, istenen kaydı bulun ve seçin. İş durumu Planlandı olan bir iş seçin. Örneğin **Planlanan dönem** alanında ikinci iş 19 Aralık 2012 tarihine zamanlanmıştır. Bu durumda işi planlanan dönem içinde taşıyın. 

2. **İleri**'ye tıklayın. İşin listede bir satır aşağıya taşındığına dikkat edin. 

3. **Geri**'yi tıklatın. İşin listede bir satır yukarıya taşındığına dikkat edin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]