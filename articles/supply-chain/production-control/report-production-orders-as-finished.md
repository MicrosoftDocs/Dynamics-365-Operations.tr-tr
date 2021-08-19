---
title: Üretim emirlerini tamamlandı olarak raporlama
description: Tamamlamdı olarak raporlama bir üretim aşamasıdır. Bu aşamada, bitmiş ürünün rapor edilir ve üretim emrinden stoğa taşınır.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: kamaybac
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d509f0f732c1255a87bf810ab9a3bba3f61e2061f9a761ee0797b3fec45e45a3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6717088"
---
# <a name="report-production-orders-as-finished"></a>Üretim emirlerini tamamlandı olarak raporlama

[!include [banner](../includes/banner.md)]

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





[!INCLUDE[footer-include](../../includes/footer-banner.md)]