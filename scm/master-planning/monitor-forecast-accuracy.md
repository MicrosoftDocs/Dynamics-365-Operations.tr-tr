---
title: "Monitör tahmin doğruluk"
description: "Bu makale Microsoft Dynamics 365 işlemleri için hesaplar ve doğruluk değerleri görüntüleme biçimini açıklar tahmin doğruluk türlerini açıklar."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d3f88a4fa54217cea909c54955de05e2175db0cd
ms.lasthandoff: 03/29/2017


---

# <a name="monitor-forecast-accuracy"></a>Monitör tahmin doğruluk

Bu makale Microsoft Dynamics 365 işlemleri için hesaplar ve doğruluk değerleri görüntüleme biçimini açıklar tahmin doğruluk türlerini açıklar.

Dynamics 365 işlemleri için tahmin doğruluğunu aşağıdaki türde hesaplar:

-   Ana Planlamanın kullandığı geçmiş tahmini geçmiş taleple karşılaştırmak suretiyle, geçmiş tahmin doğruluğu. Geçmiş tahmin doğruluğuna ait değerleri (hem mutlak değerler hem de yüzde değerleri) görüntülemek için, **Talep tahmini ayrıntıları** sayfasındaki **Doğruluğu göster** öğesine tıklayın.
-   Öngörüler oluşturmak için kullanılan tahmin modelinin tahmini doğruluğu. Doğruluk yüzdesini **Talep tahmini ayrıntıları** sayfasındaki **Model ayrıntıları - MAPE** öğesi altında görüntüleyebilirsiniz. 

**Not:** Dynamics 365 işlemleri isteğe bağlı Microsoft Azure makine öğrenme hizmeti tahmini için kullanırsanız, iç modeli doğruluğunu sınama veri kümesi üzerinde dayanır. Test veri kümesi boyutunu belirtmek için set **TEST\_AYARLAMAK\_BOYUTU\_yüzde** parametresi **isteğe bağlı parametreleri tahmin** sayfa. Örneğin, değeri **20** olarak ayarlamak için, iç model doğruluğunu hesaplamada geçmiş verilerin son yüzde 20'si kullanılacaktır.


<a name="see-also"></a>Ayrıca bkz.
--------

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)

[Remove outliers from historical transaction data when calculating a demand forecast](remove-historical-outliers-calculating-demand-forecast.md)


