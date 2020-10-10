---
title: Ana planlama işini iptal etme
description: Bu konuda, yerleşik planlama işlevini kullanan etkin bir planlama işinin nasıl iptal edileceği açıklanmaktadır.
author: ChristianRytt
manager: tfehr
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace, ReqProcessList
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6f5ce460cc2915d1d4d9b5699723a62ed7f94599
ms.sourcegitcommit: cde71bc7d14ea6cdff2c4e991057d39a6a0473d9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2020
ms.locfileid: "3886883"
---
# <a name="cancel-a-master-planning-job"></a>Ana planlama işini iptal etme

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management'ta, Master planlama işini iptal etmek için çoklu seçenekler vardır. Örneğin, bir ana planlama işini yanlışlıkla başlatılmış veya beklenenden uzun süre çalıştırılarak iptal etmek isteyebilirsiniz ve sonlandırmak isteyebilirsiniz. Bir planlama işini iptal etmenin en iyi yolu, **tamamlanmamış planlama işlemleri** sayfasından alınır. **Toplu iş** ve **toplu iş gelişmiş** sayfalarından alternatif seçenekler yalnızca, **bitmemiş planlama işlemleri** sayfasından bir kaç dakika içinde ana planlama işi iptal edilirken kullanılmalıdır.

## <a name="preferred-cancel-option"></a>Tercih edilen iptal seçeneği
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a>**Bitmemiş planlama işlemleri** sayfasından Master planlama işini iptal et
1. **Master planlama > Sorgular ve raporlar > Master planlama > Bitmemiş planlama süreçleri**'ne gidin.
2. İptal etmek istediğiniz planlama sürecini içeren satırını seçin.
3. **İptal**'e tıklayın

## <a name="additional-cancel-options"></a>Ek iptal seçenekleri
Bunlar yalnızca, master planlama işi **Tamamlanmamış planlama işlemleri** sayfasından, birkaç dakika içinde tamamlanmamışsa kullanılmalıdır.

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a>Master planlama işini **toplu işler** sayfasından Sil
1. **Sistem yönetimi > Sorgular > Toplu işler**'e gidin.
2. Silmek istediğiniz planlama işini içeren satırını seçin.
3. **Sil** öğesini tıklayın.

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a>Master planlama işi görevini **toplu işler gelişmiş** sayfasından iptal et
1. **Sistem yönetimi > Sorgular > Toplu işler**'e gidin.
2. İş kodu listede gösterilmezse, **Gelişmiş forma geç**'i tıklatın, aksi durumda bir sonraki adımla devam edin.
3. Toplu işi açın. Sonlandırmak istediğiniz görevlerle ilgili toplu iş için **iş kodu** tıklatın.
4. **Toplu iş görevlerinde** sona erdirmek istediğiniz görevleri seçin.
5. **Durumu değiştir**'e tıklayın, **İptal etme**'yi seçip **Tamam**'a tıklayın.
6. **Toplu işlem görevleri** hızlı sekmesinde, **Durdur**'u tıklatın.
