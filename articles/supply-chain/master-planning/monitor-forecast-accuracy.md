---
title: Tahmin doğruluğunu izleme
description: Bu konuda Dynamics 365 Supply Chain Management'ın hesapladığı tahmin doğruluğu türleri anlatılmakta ve doğruluk değerlerini nasıl görüntüleyebileceğiniz açıklanmaktadır.
author: roxanadiaconu
manager: tfehr
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8548fa9f64a579816e51bbd7ad9f63db290eaa38
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244219"
---
# <a name="monitor-forecast-accuracy"></a><span data-ttu-id="ff327-103">Tahmin doğruluğunu izleme</span><span class="sxs-lookup"><span data-stu-id="ff327-103">Monitor forecast accuracy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ff327-104">Bu konuda Microsoft Dynamics 365 Supply Chain Management'ın hesapladığı tahmin doğruluğu türleri anlatılmakta ve doğruluk değerlerini nasıl görüntüleyebileceğiniz açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ff327-104">This topic describes the types of forecast accuracy that Microsoft Dynamics 365 Supply Chain Management calculates, and explains how you can view the accuracy values.</span></span>

<span data-ttu-id="ff327-105">Supply Chain Management, aşağıdaki tahmin doğruluğu türlerini hesaplar:</span><span class="sxs-lookup"><span data-stu-id="ff327-105">Supply Chain Management calculates the following types of forecast accuracy:</span></span>

-   <span data-ttu-id="ff327-106">Ana Planlamanın kullandığı geçmiş tahmini geçmiş taleple karşılaştırmak suretiyle, geçmiş tahmin doğruluğu.</span><span class="sxs-lookup"><span data-stu-id="ff327-106">Historical forecast accuracy, by comparing the historical forecast that Master Planning uses with the historical demand.</span></span> <span data-ttu-id="ff327-107">Geçmiş tahmin doğruluğuna ait değerleri (hem mutlak değerler hem de yüzde değerleri) görüntülemek için, **Talep tahmini ayrıntıları** sayfasındaki **Doğruluğu göster** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ff327-107">To view the values (both absolute values and percentage values) for historical forecast accuracy, click **Show accuracy** on the **Demand forecast details** page.</span></span>
-   <span data-ttu-id="ff327-108">Öngörüler oluşturmak için kullanılan tahmin modelinin tahmini doğruluğu.</span><span class="sxs-lookup"><span data-stu-id="ff327-108">The estimated accuracy of the forecasting model that is used to generate the predictions.</span></span> <span data-ttu-id="ff327-109">Doğruluk yüzdesini **Talep tahmini ayrıntıları** sayfasındaki **Model ayrıntıları - MAPE** öğesi altında görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ff327-109">You can view the accuracy percentage under **Model details - MAPE** on the **Demand forecast details** page.</span></span> 

> [!NOTE]
> <span data-ttu-id="ff327-110">Talep tahmini Microsoft Azure Machine Learning kullanıyorsanız dahili model doğruluğu hesaplaması, test verileri kümesine dayanır.</span><span class="sxs-lookup"><span data-stu-id="ff327-110">If you use the Demand forecasting Microsoft Azure Machine Learning, the calculation of internal model accuracy is based on the test data set.</span></span> <span data-ttu-id="ff327-111">Test verileri kümesinin boyutunu belirtmek için, **Talep tahmini parametreleri** sayfasında **TEST\_SET\_SIZE\_PERCENT** parametresini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ff327-111">To specify the size of the test data set, set the **TEST\_SET\_SIZE\_PERCENT** parameter on the **Demand forecasting parameters** page.</span></span> <span data-ttu-id="ff327-112">Örneğin, değeri **20** olarak ayarlamak için, iç model doğruluğunu hesaplamada geçmiş verilerin son yüzde 20'si kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="ff327-112">For example, if you set the value to **20**, the last 20 percent of the historical data will be used to calculate the internal model accuracy.</span></span>


<a name="additional-resources"></a><span data-ttu-id="ff327-113">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="ff327-113">Additional resources</span></span>
--------

[<span data-ttu-id="ff327-114">Düzeltilen tahmini yetkilendirme</span><span class="sxs-lookup"><span data-stu-id="ff327-114">Authorize an adjusted forecast</span></span>](authorize-adjusted-forecast.md)

[<span data-ttu-id="ff327-115">Bir talep tahmini hesaplarken aykırı değerleri geçmiş hareket verilerinden kaldırma</span><span class="sxs-lookup"><span data-stu-id="ff327-115">Remove outliers from historical transaction data when calculating a demand forecast</span></span>](remove-historical-outliers-calculating-demand-forecast.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]