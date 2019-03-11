---
title: Planlanmış kanban işlerini taşıma
description: Bu prosedür, planlanan işlem kanban işlerini farklı bir döneme taşımaya odaklanmaktadır.
author: ChristianRytt
manager: AnnBe
ms.date: 11/07/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f791c9048ef6efe1585c991f998099cd1fc12df7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "310864"
---
# <a name="move-scheduled-kanban-jobs"></a>Planlanmış kanban işlerini taşıma

[!include [task guide banner](../../includes/task-guide-banner.md)]

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
