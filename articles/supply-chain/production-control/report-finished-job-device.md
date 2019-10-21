---
title: İş kartı cihazından plaka kontrollü bir yerleşime tamamlandı olarak bildirme
description: Bu konu, yerleşimi bir plaka kontrol ediyorsa bir üretim emrindeki bitmiş ürünleri bir stoka tamamlamaya ilişkin süreci açıklamaktadır.
author: johanhoffmann
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: 35ad27a6b8a52bfd086fbe4fc57b1681ff88fd5b
ms.sourcegitcommit: 58db26b7edf02e7c33aaaf1c934e3263aa74b01f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/11/2019
ms.locfileid: "1995154"
---
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>İş kartı cihazından plaka kontrollü bir yerleşime tamamlandı olarak bildirme 

Tamamlandı bildirimi ile çağrılan süreç, bir üretim emrindeki bitmiş ürünleri stoka tamamlar. Bitmiş ürün gelişmiş ambar süreçleri için etkinleştirilmişse, o ürün, üretim çıkış yerleşimi adı verilen bir yerleşime tamamlandı olarak bildirilir. Üretim çıkış yerleşiminin ayarlanması hakkında bilgi için [Üretim çıkış yerleşimi](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location) konusuna bakın.

Bu görevi tamamlamak için, varolan bir plaka numarasını seçmelisiniz. Üretim çıkış yerleşimi, plaka tarafından izlenmeye ayarlanmışsa, üretim çıkış yerleşimine tamamlandı olarak bildirilirken bir plaka numarası eklenmelidir. **Plaka** alanı, **İş kartı cihazı** sayfasındaki **İlerlemeyi bildir** komut isteminde görünür durumdadır. Alan **İlerlemeyi bildir** komut isteminde yalnızca üretim emrinin son işlemi bildirilirken görünür. Alan yalnızca üretim emrine ait madde ambar yönetim süreçleri için etkinleştirildiğinde gösterilir. 
