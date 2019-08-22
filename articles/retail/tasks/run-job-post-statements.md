---
title: Deyimleri nakletmek için işi yapılandır ve çalıştır
description: Bu yordam, seçili bir mağaza veya mağaza grubuna ilişkin ekstreleri deftere nakletmek için yinelenen toplu işi çalıştırma ve yapılandırmayla ilgili açıklamalar sağlar.
author: josaw1
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a24014f7e1b925e0fdb20b91bcc9594feb8f4c5c
ms.sourcegitcommit: fc40279d0e56f8a43c601bca6265fdde4c8c4c7e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/29/2019
ms.locfileid: "1792260"
---
# <a name="configure-and-run-job-to-post-statements"></a>Deyimleri nakletmek için işi yapılandır ve çalıştır

[!include[task guide banner](../includes/task-guide-banner.md)]

Bu yordam, seçili bir mağaza veya mağaza grubuna ilişkin ekstreleri deftere nakletmek için yinelenen toplu işi çalıştırma ve yapılandırmayla ilgili açıklamalar sağlar. Bu yordam USRT demo veri şirketini kullanır.

1. Tüm çalışma alanları > .. > Perakende mağazası mali öğeleri'ne gidin.
2. Ekstreleri toplu işle deftere naklet'e tıklayın.
    * Bir kuruluş hiyerarşisi seçin ve kuruluş düğümleri ağacından tek bir mağaza veya bir düğüm seçin. Bir mağaza grubu için toplu iş oluşturmak istiyorsanız bir düğüm belirtin.  
    * Seçiminizi eklemek için oka tıklayın.  
3. Arka plan sekmesinde Çalıştır'a tıklayın. ![Arka planda çalıştır](../dev-itpro/media/runbackground.png "Arka planda çalıştır") 
4. Toplu işlem onay kutusunu işaretleyin veya işaretini kaldırın.
![Toplu İş İşleme](../dev-itpro/media/batchprocessing.png "Toplu İş İşleme ve Tekrar Etme") 
5. Yineleme'ye tıklayın.
6. Başlangıç tarihi alanına bir tarih girin.
7. Başlangıç saati alanına saati girin.
    * Yinelemenin belirli bir çalıştırma sayısı sonunda mı, belirli bir tarihte mi sonlandırılacağını yoksa hiçbir zaman sonlandırılmayacağını mı belirtin. Ardından işin ne sıklıkta çalıştırılacağını belirtmek için çeşitli seçenekleri belirtin.  
8. Tamam'a tıklayın.
9. Tamam'a tıklayın.

