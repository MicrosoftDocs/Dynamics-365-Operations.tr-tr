---
title: Master planlama çalışmasını izleme
description: Üretim planlayıcısı, bir master planlama çalışmasının devam edip etmediğini görmek istiyor.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c2e158d8cbad1f5d4f377f6a8eb43487b34ffdc
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565633"
---
# <a name="monitor-a-master-planning-run"></a>Master planlama çalışmasını izleme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Üretim planlayıcısı, bir master planlama çalışmasının devam edip etmediğini görmek istiyor. Bu prosedürü tamamlamak için USMF demo veri şirketini kullanın.


## <a name="run-master-planning"></a>Master planlamayı çalıştırma
1. Master planlama'ya tıklayın.
    * Bunu varsayılan panosunda bulabilirsiniz.  
2. Plan alanında bir değer girin veya bir değer seçin.
    * Örnek: StaticPlan  
3. Çalıştır öğesine tıklayın.
4. Takip işleme süresi alanından Evet'i seçin.
    * Alan zaten seçilmişse bu adımı atlayın.  
5. İş parçacığı sayısı alanına bir rakam girin.
6. Eklenecek kayıtlar bölümünü genişletin.
7. Filtre'ye tıklayın.
8. Listede, seçili satırı işaretleyin.
    * Alan = Madde numarası olan sırayı işaretleyin.  
9. Ölçütler alanında bir değer girin veya seçin.
    * Örnek: T0001  
10. Tamam'a tıklayın.
11. Tamam'a tıklayın.

## <a name="monitor-the-master-planning-run"></a>Master planlama yürütmeyi izleme
1. Geçmiş öğesini tıklayın.
2. Sorgulamalar’ı tıklatın.
3. İşlem görevi süresi öğesini tıklayın.
4. Listede, istenen kaydı bulun ve seçin.
    * Her madde için, planlama adımlarının her birinin ne kadar sürede tamamlandığını görebilirsiniz.  

