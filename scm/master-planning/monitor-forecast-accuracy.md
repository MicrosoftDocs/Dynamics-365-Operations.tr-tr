---
title: "Tahmin doğruluğunu izleme"
description: "Bu makalede, Microsoft Dynamics 365 for Operations&quot;ın hesapladığı tahmin doğruluğu türleri anlatılmakta ve doğruluk değerlerini nasıl görüntüleyebileceğiniz açıklanmaktadır."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 7e470e05d9acb1e7417d0d77655be99e94d15e1d
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="monitor-forecast-accuracy"></a>Tahmin doğruluğunu izleme

[!include[banner](../includes/banner.md)]


Bu makalede, Microsoft Dynamics 365 for Operations'ın hesapladığı tahmin doğruluğu türleri anlatılmakta ve doğruluk değerlerini nasıl görüntüleyebileceğiniz açıklanmaktadır.

Dynamics 365 for Operations, aşağıdaki tahmin doğruluğu türlerini hesaplar:

-   Ana Planlamanın kullandığı geçmiş tahmini geçmiş taleple karşılaştırmak suretiyle, geçmiş tahmin doğruluğu. Geçmiş tahmin doğruluğuna ait değerleri (hem mutlak değerler hem de yüzde değerleri) görüntülemek için, **Talep tahmini ayrıntıları** sayfasındaki **Doğruluğu göster** öğesine tıklayın.
-   Öngörüler oluşturmak için kullanılan tahmin modelinin tahmini doğruluğu. Doğruluk yüzdesini **Talep tahmini ayrıntıları** sayfasındaki **Model ayrıntıları - MAPE** öğesi altında görüntüleyebilirsiniz. 

**Not:** Dynamics 365 for Operations Talep tahmini Microsoft Azure Machine Learning hizmeti kullanıyorsanız, iç model doğruluğu hesaplaması test verileri kümesine dayanır. Test verileri kümesinin boyutunu belirtmek için, **Talep tahmini parametreleri** sayfasında **TEST\_SET\_SIZE\_PERCENT** parametresini ayarlayın. Örneğin, değeri **20** olarak ayarlamak için, iç model doğruluğunu hesaplamada geçmiş verilerin son yüzde 20'si kullanılacaktır.


<a name="see-also"></a>Ayrıca bkz.
--------

[Ayarlanmış tahmini yetkilendirme](authorize-adjusted-forecast.md)

[Bir talep tahmin hesaplarken, geçmiş işlem verilerinden aykırı değerleri kaldırın.](remove-historical-outliers-calculating-demand-forecast.md)



