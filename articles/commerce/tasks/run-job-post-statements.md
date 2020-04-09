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
ms.openlocfilehash: f89203850b302b769b22920fa5c42d2b0b877684
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141189"
---
# <a name="configure-and-run-job-to-post-statements"></a>Deyimleri nakletmek için işi yapılandır ve çalıştır

[!include [banner](../includes/banner.md)]

Bu yordam, seçili bir mağaza veya mağaza grubuna ilişkin ekstreleri deftere nakletmek için yinelenen toplu işi çalıştırma ve yapılandırmayla ilgili açıklamalar sağlar. Bu yordam USRT demo veri şirketini kullanır.

1. Tüm çalışma alanları > .. > Mağaza mali öğeleri.
2. Ekstreleri toplu işle deftere naklet'e tıklayın.
    * Bir kuruluş hiyerarşisi seçin ve kuruluş düğümleri ağacından tek bir mağaza veya bir düğüm seçin. Bir mağaza grubu için toplu iş oluşturmak istiyorsanız bir düğüm belirtin.  
    * Seçiminizi eklemek için oka tıklayın.  
3. Arka plan sekmesinde Çalıştır'a tıklayın. ![Arka planda çalıştır](../dev-itpro/media/runbackground.png "Arka planda çalıştır") 
4. Toplu işlem onay kutusunu işaretleyin veya işaretini kaldırın.
![Toplu İşlem](../dev-itpro/media/batchprocessing.png "Toplu İşlem ve yineleme") 
5. Yineleme'ye tıklayın.
6. Başlangıç tarihi alanına bir tarih girin.
7. Başlangıç saati alanına saati girin.
    * Yinelemenin belirli bir çalıştırma sayısı sonunda mı, belirli bir tarihte mi sonlandırılacağını yoksa hiçbir zaman sonlandırılmayacağını mı belirtin. Ardından işin ne sıklıkta çalıştırılacağını belirtmek için çeşitli seçenekleri belirtin.  
8. Tamam'a tıklayın.
9. Tamam'a tıklayın.

