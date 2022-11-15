---
title: Tahmin doğruluğunu izleme
description: Bu makalede, Dynamics 365 Supply Chain Management'in hesapladığı tahmin doğruluğu türleri anlatılmakta ve doğruluk değerlerini nasıl görüntüleyebileceğiniz açıklanmaktadır.
author: t-benebo
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76248d87533fd233b255060aa278c76e13719700
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740752"
---
# <a name="monitor-forecast-accuracy"></a>Tahmin doğruluğunu izleme

[!include [banner](../includes/banner.md)]

Bu makalede Microsoft Dynamics 365 Supply Chain Management'ın hesapladığı tahmin doğruluğu türleri anlatılmakta ve doğruluk değerlerini nasıl görüntüleyebileceğiniz açıklanmaktadır.

Supply Chain Management, aşağıdaki tahmin doğruluğu türlerini hesaplar:

-   Ana Planlamanın kullandığı geçmiş tahmini geçmiş taleple karşılaştırmak suretiyle, geçmiş tahmin doğruluğu. Geçmiş tahmin doğruluğuna ait değerleri (hem mutlak değerler hem de yüzde değerleri) görüntülemek için, **Talep tahmini ayrıntıları** sayfasındaki **Doğruluğu göster** öğesine tıklayın.
-   Öngörüler oluşturmak için kullanılan tahmin modelinin tahmini doğruluğu. Doğruluk yüzdesini **Talep tahmini ayrıntıları** sayfasındaki **Model ayrıntıları - MAPE** öğesi altında görüntüleyebilirsiniz. 

> [!NOTE]
> Talep tahmini Microsoft Azure Machine Learning kullanıyorsanız dahili model doğruluğu hesaplaması, test verileri kümesine dayanır. Test verileri kümesinin boyutunu belirtmek için, **Talep tahmini parametreleri** sayfasında **TEST\_SET\_SIZE\_PERCENT** parametresini ayarlayın. Örneğin, değeri **20** olarak ayarlamak için, iç model doğruluğunu hesaplamada geçmiş verilerin son yüzde 20'si kullanılacaktır.


## <a name="additional-resources"></a>Ek kaynaklar

- [Düzeltilen tahmini yetkilendirme](authorize-adjusted-forecast.md)
- [Bir talep tahmini hesaplarken aykırı değerleri geçmiş hareket verilerinden kaldırma](remove-historical-outliers-calculating-demand-forecast.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]