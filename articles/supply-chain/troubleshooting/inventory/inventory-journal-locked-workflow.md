---
title: Stok günlüğünüz kilitli ve iş akışı toplu işi çalışmıyor
description: Stok günlükleriniz bazı işlemler tarafından kilitlenmiş ve yayınlanmıyor
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8b21ec2e2b3b8546dcb138422c5540053392c179
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477821"
---
# <a name="your-inventory-journal-is-locked-and-the-workflow-batch-job-doesnt-work"></a>Stok günlüğünüz kilitli ve iş akışı toplu işi çalışmıyor

## <a name="symptoms"></a>Belirtiler

Stok günlükleriniz bir işlem tarafından kilitlenmiş ve yayınlanmıyor. Örneğin, deftere nakil sırasında (bir sistem kilitleme işlemidir) bilinmeyen bir hata oluşursa günlük, sistem kilitli durumunda kalabilir. Bu durumda, iş akışı iş öğesi işleyicisi, kilit doğrulama işlemini gerçekleştirirken bir hata oluşturur.

## <a name="resolution"></a>Çözüm

Supply Chain Management için SQL Server kurulumunda oturum açın ve **InventJournalTable.SystemBlocked** seçeneğinin *1* olarak ayarlanıp ayarlanmadığını kontrol edin. Bu şekilde ayarlanmışsa günlüğün kilitli durumda olmaması gerektiğinden emin olun ve ardından **InventJournalTable.SystemBlocked** seçeneğini *0* olarak ayarlayın.
