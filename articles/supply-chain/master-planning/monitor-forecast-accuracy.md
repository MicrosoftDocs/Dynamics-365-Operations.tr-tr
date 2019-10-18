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
ms.openlocfilehash: 6f238afadfa064e972ef11a95fdad073f63ff20c
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250680"
---
# <a name="monitor-forecast-accuracy"></a><span data-ttu-id="249d3-103">Tahmin doğruluğunu izleme</span><span class="sxs-lookup"><span data-stu-id="249d3-103">Monitor forecast accuracy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="249d3-104">Bu konuda Microsoft Dynamics 365 Supply Chain Management'ın hesapladığı tahmin doğruluğu türleri anlatılmakta ve doğruluk değerlerini nasıl görüntüleyebileceğiniz açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="249d3-104">This topic describes the types of forecast accuracy that Microsoft Dynamics 365 Supply Chain Management calculates, and explains how you can view the accuracy values.</span></span>

<span data-ttu-id="249d3-105">Supply Chain Management, aşağıdaki tahmin doğruluğu türlerini hesaplar:</span><span class="sxs-lookup"><span data-stu-id="249d3-105">Supply Chain Management calculates the following types of forecast accuracy:</span></span>

-   <span data-ttu-id="249d3-106">Ana Planlamanın kullandığı geçmiş tahmini geçmiş taleple karşılaştırmak suretiyle, geçmiş tahmin doğruluğu.</span><span class="sxs-lookup"><span data-stu-id="249d3-106">Historical forecast accuracy, by comparing the historical forecast that Master Planning uses with the historical demand.</span></span> <span data-ttu-id="249d3-107">Geçmiş tahmin doğruluğuna ait değerleri (hem mutlak değerler hem de yüzde değerleri) görüntülemek için, **Talep tahmini ayrıntıları** sayfasındaki **Doğruluğu göster** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="249d3-107">To view the values (both absolute values and percentage values) for historical forecast accuracy, click **Show accuracy** on the **Demand forecast details** page.</span></span>
-   <span data-ttu-id="249d3-108">Öngörüler oluşturmak için kullanılan tahmin modelinin tahmini doğruluğu.</span><span class="sxs-lookup"><span data-stu-id="249d3-108">The estimated accuracy of the forecasting model that is used to generate the predictions.</span></span> <span data-ttu-id="249d3-109">Doğruluk yüzdesini **Talep tahmini ayrıntıları** sayfasındaki **Model ayrıntıları - MAPE** öğesi altında görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="249d3-109">You can view the accuracy percentage under **Model details - MAPE** on the **Demand forecast details** page.</span></span> 

> [!NOTE]
> <span data-ttu-id="249d3-110">Talep tahmini Microsoft Azure Machine Learning hizmetini kullanıyorsanız dahili model doğruluğu hesaplaması, test verileri kümesine dayanır.</span><span class="sxs-lookup"><span data-stu-id="249d3-110">If you use the Demand forecasting Microsoft Azure Machine Learning service, the calculation of internal model accuracy is based on the test data set.</span></span> <span data-ttu-id="249d3-111">Test verileri kümesinin boyutunu belirtmek için, **Talep tahmini parametreleri** sayfasında **TEST\_SET\_SIZE\_PERCENT** parametresini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="249d3-111">To specify the size of the test data set, set the **TEST\_SET\_SIZE\_PERCENT** parameter on the **Demand forecasting parameters** page.</span></span> <span data-ttu-id="249d3-112">Örneğin, değeri **20** olarak ayarlamak için, iç model doğruluğunu hesaplamada geçmiş verilerin son yüzde 20'si kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="249d3-112">For example, if you set the value to **20**, the last 20 percent of the historical data will be used to calculate the internal model accuracy.</span></span>


<a name="additional-resources"></a><span data-ttu-id="249d3-113">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="249d3-113">Additional resources</span></span>
--------

[<span data-ttu-id="249d3-114">Ayarlanmış tahmini yetkilendirme</span><span class="sxs-lookup"><span data-stu-id="249d3-114">Authorizing the adjusted forecast</span></span>](authorize-adjusted-forecast.md)

[<span data-ttu-id="249d3-115">Bir talep tahmini hesaplarken aykırı değerleri geçmiş hareket verilerinden kaldırma</span><span class="sxs-lookup"><span data-stu-id="249d3-115">Remove outliers from historical transaction data when calculating a demand forecast</span></span>](remove-historical-outliers-calculating-demand-forecast.md)



