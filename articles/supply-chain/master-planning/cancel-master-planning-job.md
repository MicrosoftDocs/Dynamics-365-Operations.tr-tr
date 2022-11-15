---
title: Kullanımdan kaldırılan master planlama altyapısı kullanılarak oluşturulan bir işi iptal etme
description: Bu makalede, kullanımdan kaldırılan master planlama altyapısı kullanan etkin bir planlama işinin nasıl iptal edileceği açıklanmaktadır.
author: t-benebo
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace, ReqProcessList
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7b71a43f407050dccb7550db7c4b6a98a596d589
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740890"
---
# <a name="cancel-a-job-that-was-created-using-the-deprecated-master-planning-engine"></a>Kullanımdan kaldırılan master planlama altyapısı kullanılarak oluşturulan bir işi iptal etme

[!include [banner](../includes/banner.md)]

Kullanımdan kaldırılan master planlama altyapısı kullanılarak oluşturulan bir işi iptal etmenin birkaç yolu vardır. Örneğin, bir ana planlama işini yanlışlıkla başlatılmış veya beklenenden uzun süre çalıştırılarak iptal etmek isteyebilirsiniz ve sonlandırmak isteyebilirsiniz.

Bir planlama işini iptal etmenin en iyi yolu, **tamamlanmamış planlama işlemleri** sayfasından alınır. **Toplu iş** ve **toplu iş gelişmiş** sayfalarından alternatif seçenekler yalnızca, **bitmemiş planlama işlemleri** sayfasından bir kaç dakika içinde ana planlama işi iptal edilirken kullanılmalıdır.

## <a name="preferred-cancel-option"></a>Tercih edilen iptal seçeneği

### <a name="cancel-master-planning-job-from-the-unfinished-planning-processes-page"></a>Bitmemiş planlama işlemleri sayfasından Master planlama işini iptal etme

1. **Master planlama > Sorgular ve raporlar > Master planlama > Bitmemiş planlama süreçleri**'ne gidin.
2. İptal etmek istediğiniz planlama sürecini içeren satırını seçin.
3. **İptal**'i seçin.

## <a name="additional-cancel-options"></a>Ek iptal seçenekleri

Bunlar yalnızca, master planlama işi **Tamamlanmamış planlama işlemleri** sayfasından, birkaç dakika içinde tamamlanmamışsa kullanılmalıdır.

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a>Master planlama işini **toplu işler** sayfasından Sil

1. **Sistem yönetimi > Sorgular > Toplu işler**'e gidin.
2. Silmek istediğiniz planlama işini içeren satırını seçin.
3. **Sil**'i seçin.

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a>Master planlama işi görevini **toplu işler gelişmiş** sayfasından iptal et

1. **Sistem yönetimi > Sorgular > Toplu işler**'e gidin.
2. İş kodu listede gösterilmezse, **Gelişmiş forma geç**'i tıklatın, aksi durumda bir sonraki adımla devam edin.
3. Toplu işi açın. Sonlandırmak istediğiniz görevlerle ilgili toplu işe ait **İş kodu**'nu seçin.
4. **Toplu iş görevlerinde** sona erdirmek istediğiniz görevleri seçin.
5. **Durumu değiştir**'i, **İptal ediliyor**'u seçip **Tamam**'a tıklayın.
6. **Toplu işlem görevleri** hızlı sekmesinde, **Durdur**'u tıklatın.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]