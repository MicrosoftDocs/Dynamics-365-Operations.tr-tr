---
title: Tahmin doğruluğunu izleme
description: Bu konuda Dynamics 365 Supply Chain Management'ın hesapladığı tahmin doğruluğu türleri anlatılmakta ve doğruluk değerlerini nasıl görüntüleyebileceğiniz açıklanmaktadır.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4cf65826279f0741ce5abc89d8f15bfec98c83ef
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813696"
---
# <a name="monitor-forecast-accuracy"></a>Tahmin doğruluğunu izleme

[!include [banner](../includes/banner.md)]

Bu konuda Microsoft Dynamics 365 Supply Chain Management'ın hesapladığı tahmin doğruluğu türleri anlatılmakta ve doğruluk değerlerini nasıl görüntüleyebileceğiniz açıklanmaktadır.

Supply Chain Management, aşağıdaki tahmin doğruluğu türlerini hesaplar:

-   Ana Planlamanın kullandığı geçmiş tahmini geçmiş taleple karşılaştırmak suretiyle, geçmiş tahmin doğruluğu. Geçmiş tahmin doğruluğuna ait değerleri (hem mutlak değerler hem de yüzde değerleri) görüntülemek için, **Talep tahmini ayrıntıları** sayfasındaki **Doğruluğu göster** öğesine tıklayın.
-   Öngörüler oluşturmak için kullanılan tahmin modelinin tahmini doğruluğu. Doğruluk yüzdesini **Talep tahmini ayrıntıları** sayfasındaki **Model ayrıntıları - MAPE** öğesi altında görüntüleyebilirsiniz. 

> [!NOTE]
> Talep tahmini Microsoft Azure Machine Learning hizmetini kullanıyorsanız dahili model doğruluğu hesaplaması, test verileri kümesine dayanır. Test verileri kümesinin boyutunu belirtmek için, **Talep tahmini parametreleri** sayfasında **TEST\_SET\_SIZE\_PERCENT** parametresini ayarlayın. Örneğin, değeri **20** olarak ayarlamak için, iç model doğruluğunu hesaplamada geçmiş verilerin son yüzde 20'si kullanılacaktır.


<a name="additional-resources"></a>Ek kaynaklar
--------

[Düzeltilen tahmini yetkilendirme](authorize-adjusted-forecast.md)

[Bir talep tahmini hesaplarken aykırı değerleri geçmiş hareket verilerinden kaldırma](remove-historical-outliers-calculating-demand-forecast.md)



