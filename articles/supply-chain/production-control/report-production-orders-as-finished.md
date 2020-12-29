---
title: Üretim emirlerini tamamlandı olarak raporlama
description: Tamamlamdı olarak raporlama bir üretim aşamasıdır. Bu aşamada, bitmiş ürünün rapor edilir ve üretim emrinden stoğa taşınır.
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdJournalTransJob, ProdJournalTransProd, ProdJournalTransRoute, ProdParmReportFinished, ProdRouteOprOverview
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 27061
ms.assetid: 1c2dfc54-a293-49f2-9b96-5a912ac5762c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87e5d4f46a2ae34a2bc114a92ed4e037875dde43
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439231"
---
# <a name="report-production-orders-as-finished"></a><span data-ttu-id="1748d-104">Üretim emirlerini tamamlandı olarak raporlama</span><span class="sxs-lookup"><span data-stu-id="1748d-104">Report production orders as finished</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1748d-105">Tamamlamdı olarak raporlama bir üretim aşamasıdır.</span><span class="sxs-lookup"><span data-stu-id="1748d-105">Report as finished is a production stage.</span></span> <span data-ttu-id="1748d-106">Bu aşamada, bitmiş ürünün rapor edilir ve üretim emrinden stoğa taşınır.</span><span class="sxs-lookup"><span data-stu-id="1748d-106">At this stage, a finished product is reported and moved from the production order to the inventory.</span></span>

<span data-ttu-id="1748d-107">Bir üretim siparişindeki bir miktar nihai ürün, tamamlandı olarak raporlandığında, stokta eldeki miktar olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="1748d-107">When a quantity of the finished goods is reported as finished on a production order it is updated as on-hand in the inventory.</span></span> <span data-ttu-id="1748d-108">Başlangıçta planlanan sipariş miktarının kısmi miktarları tamamlandı olarak rapor edilebilir.</span><span class="sxs-lookup"><span data-stu-id="1748d-108">Partial quantities of the originally planned order quantity can be reported as finished.</span></span> <span data-ttu-id="1748d-109">Miktarlar tamamlandı olarak rapor edilirken hatalı miktarların ilgili bir hata nedeniyle birlikte rapor edilmesi de mümkündür.</span><span class="sxs-lookup"><span data-stu-id="1748d-109">It is also possible to report error quantities with an associated error reason when reporting quantities as finished.</span></span> <span data-ttu-id="1748d-110">Üretim siparişi, tamamlandı olarak Rapor edildi aşamasına ulaştığında üretim siparişinde rapor edilecek daha fazla miktar kalmamıştır.</span><span class="sxs-lookup"><span data-stu-id="1748d-110">When the production order reach the stage Reported as finished it indicates that no more quantity is going to be reported at the production  order.</span></span>
<span data-ttu-id="1748d-111">Aşağıdaki özellikler aynı zamanda **Tamamlandı olarak rapor et** süreciyle de ilgilidir:</span><span class="sxs-lookup"><span data-stu-id="1748d-111">The following characteristics are also associated with the **Report as finished** process:</span></span>
-   <span data-ttu-id="1748d-112">Raporlanan miktara paralel olarak (geri yıkama) ham madde tüketiminin ve harcanan sürenin ayarlanması mümkündür.</span><span class="sxs-lookup"><span data-stu-id="1748d-112">It is possible to set up consumption of raw material and time that are proportional to the reported quantity (back-flushing)</span></span>
-   <span data-ttu-id="1748d-113">Depo süreçleri için etkinleştirilen maddeler için yerine koyma çalışması oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="1748d-113">Put-away work can be generated for items that are enabled for warehouse processes.</span></span>
-   <span data-ttu-id="1748d-114">Nihai malların planlanan veya standart maliyet değeri, defter hesaplarına rapor edilecek şekilde ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="1748d-114">The planned or standard cost value of the finished goods can be set up to be reported to ledger accounts.</span></span>
-   <span data-ttu-id="1748d-115">Bir kalite ilişkisinin kurulumuna dayalı olarak, raporlanan miktar için bir miktar emri oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="1748d-115">A quality order can be created for the reported quantity based on the setup of a quality association.</span></span>

<span data-ttu-id="1748d-116">Miktar, çıkış konumuna rapor edilir.</span><span class="sxs-lookup"><span data-stu-id="1748d-116">The quantity is reported to the output location.</span></span> <span data-ttu-id="1748d-117">Depo çalışması daha sonra miktarın çıkış konumundan, yerine çalışmasına yönelik konum direktifi tarafından tanımlanan nihai konumuna taşınmak üzere oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1748d-117">Warehouse work is then generated to move the quantity from the output location to its final destination defined by the location directive for the put-away work.</span></span>

-   <span data-ttu-id="1748d-118">Bir miktar ilişkisi kurulmuşsa, bir üretim siparişi, tamamlandı olarak rapor edildiğinde bir kalite emri oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="1748d-118">A quality order can be created when a production order is reported as finished if a quality association has been set up.</span></span>

## <a name="set-a-production-order-to-reporting-as-finished"></a><span data-ttu-id="1748d-119">Bir üretim emrini tamamlandı olarak Rapor ediliyor konumuna ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1748d-119">Set a production order to Reporting as finished</span></span>
<span data-ttu-id="1748d-120">Bir üretim emrini **Tamamlandı olarak rapor et** konumuna ayarlamak için standart üretim emri güncelleme işlevini veya rota ve iş kartı günlüklerini veya **Tamamlandı olarak rapor et** günlüğünü kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1748d-120">You can set a production order to **Report as finished** through the standard production order update function, or through the route and job card journals, or through the journal **Report as finished**.</span></span> <span data-ttu-id="1748d-121">Üretim emrinin son işiyle ilgili rapor verdiğinizde **Tamamlandı olarak rapor et** aşamasını ayrıca iş kartı terminaliyle ve iş kartı cihaz sayfalarıyla güncelleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1748d-121">You can also update the stage to **Report as finished** through the job card terminal and job card device pages, when you report on the last job of the production order.</span></span> <span data-ttu-id="1748d-122">Son olarak, eldeki depo cihazı çözümü için bir süreç olarak **Tamamlandı olarak rapor et** seçeneğini etkinleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1748d-122">Finally, you can enable the **Report as finished** option as a process for the handheld warehouse device solution.</span></span>  



