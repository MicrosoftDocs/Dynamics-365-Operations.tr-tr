---
title: İş kartı cihazından plaka kontrollü bir yerleşime tamamlandı olarak bildirme
description: Bu konu, yerleşimi bir plaka kontrol ediyorsa bir üretim emrindeki bitmiş ürünleri bir stoka tamamlamaya ilişkin süreci açıklamaktadır.
author: johanhoffmann
manager: AnnBe
ms.date: 01/06/2020
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
ms.openlocfilehash: 63073035941cd2ef343c65364536fe76a9b71430
ms.sourcegitcommit: af36eb17b36092a3101bbfc96486b25036676558
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/06/2020
ms.locfileid: "2935134"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>İş kartı cihazından plaka kontrollü bir yerleşime tamamlandı olarak bildirme 

Tamamlandı bildirimi ile çağrılan süreç, bir üretim emrindeki bitmiş ürünleri stoka tamamlar. Bitmiş ürün gelişmiş ambar süreçleri için etkinleştirilmişse, o ürün, üretim çıkış yerleşimi adı verilen bir yerleşime tamamlandı olarak bildirilir. Üretim çıkış yerleşiminin ayarlanması hakkında bilgi için [Üretim çıkış yerleşimi](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location) konusuna bakın.

Üretim çıkış konumu lisans levhası denetimli ise, tamamlandı bildirimi yapılırken bir lisans kalıbının sağlanması gerekir. **Plaka** alanı, **İş kartı cihazı** sayfasındaki **İlerlemeyi bildir** komut isteminde görünür durumdadır. Alan yalnızca, üretim emrinin son operasyonunu raporlarken **rapor ilerleme durumu** satırında görünür ve üretim emri için madde ambar yönetim işlemleri için etkinleştirilir. 

Lisans levhası sağlamak için iki seçenek vardır
- Kullanıcı, lisans levhası alanında varolan bir lisans levhasını seçer.
- Lisans levhası otomatik olarak bir numara serisinden üretilir ve lisans levhası alanına varsayılan olarak kullanılır.

Lisans kalıbının otomatik olarak oluşturulmasına izin seçeneği, **Cihazlar için iş kartını konfigüre et** sayfasında **lisans levhası oluştur** seçeneği seçilerek konfigüre edilir.
