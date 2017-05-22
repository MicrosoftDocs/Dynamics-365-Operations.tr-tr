---
title: "Üretim emirlerini tamamlandı olarak raporlama"
description: "Tamamlamdı olarak raporlama bir üretim aşamasıdır. Bu aşamada, bitmiş ürünün rapor edilir ve üretim emrinden stoğa taşınır."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: f6369a424d384a93d1497825b6877b929e76f8b9
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="report-production-orders-as-finished"></a>Üretim emirlerini tamamlandı olarak raporlama

[!include[banner](../includes/banner.md)]


Tamamlamdı olarak raporlama bir üretim aşamasıdır. Bu aşamada, bitmiş ürünün rapor edilir ve üretim emrinden stoğa taşınır.

Bir üretim siparişindeki bir miktar nihai ürün, tamamlandı olarak raporlandığında, stokta eldeki miktar olarak güncelleştirilir. Başlangıçta planlanan sipariş miktarının kısmi miktarları tamamlandı olarak rapor edilebilir. Miktarlar tamamlandı olarak rapor edilirken hatalı miktarların ilgili bir hata nedeniyle birlikte rapor edilmesi de mümkündür. Üretim siparişi, tamamlandı olarak Rapor edildi aşamasına ulaştığında üretim siparişinde rapor edilecek daha fazla miktar kalmamıştır.
Aşağıdaki özellikler aynı zamanda **Tamamlandı olarak rapor et** süreciyle de ilgilidir:
-   Raporlanan miktara paralel olarak (geri yıkama) ham madde tüketiminin ve harcanan sürenin ayarlanması mümkündür.
-   Depo süreçleri için etkinleştirilen maddeler için yerine koyma çalışması oluşturulabilir.
-   Nihai malların planlanan veya standart maliyet değeri, defter hesaplarına rapor edilecek şekilde ayarlanabilir.
-   Bir kalite ilişkisinin kurulumuna dayalı olarak, raporlanan miktar için bir miktar emri oluşturulabilir.

Miktar, çıkış konumuna rapor edilir. Depo çalışması daha sonra miktarın çıkış konumundan, yerine çalışmasına yönelik konum direktifi tarafından tanımlanan nihai konumuna taşınmak üzere oluşturulur.

-   Bir miktar ilişkisi kurulmuşsa, bir üretim siparişi, tamamlandı olarak rapor edildiğinde bir kalite emri oluşturulabilir.

## <a name="set-a-production-order-to-reporting-as-finished"></a>Bir üretim emrini tamamlandı olarak Rapor ediliyor konumuna ayarlayın.
Bir üretim emrini **Tamamlandı olarak rapor et** konumuna ayarlamak için standart üretim emri güncelleme işlevini veya rota ve iş kartı günlüklerini veya **Tamamlandı olarak rapor et** günlüğünü kullanabilirsiniz. Üretim emrinin son işiyle ilgili rapor verdiğinizde **Tamamlandı olarak rapor et** aşamasını ayrıca iş kartı terminaliyle ve iş kartı cihaz sayfalarıyla güncelleyebilirsiniz. Son olarak, eldeki depo cihazı çözümü için bir süreç olarak **Tamamlandı olarak rapor et** seçeneğini etkinleştirebilirsiniz.  



