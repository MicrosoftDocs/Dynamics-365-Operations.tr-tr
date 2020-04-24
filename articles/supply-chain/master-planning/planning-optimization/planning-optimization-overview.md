---
title: Planlamayı En İyi Duruma Getirmeye genel bakış
description: Bu konu, Planlamayı En İyi Duruma Getirme işlevine genel bir bakış sağlar.
author: ChristianRytt
manager: tfehr
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: f88ee8067fdd816ba6890ee28bafe8fa4d3b3ac5
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208743"
---
# <a name="planning-optimization-overview"></a><span data-ttu-id="b00d4-103">Planlamayı En İyi Duruma Getirmeye genel bakış</span><span class="sxs-lookup"><span data-stu-id="b00d4-103">Planning Optimization overview</span></span>

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="b00d4-104">Microsoft Dynamics 365 Supply Chain Management için Planlamayı En İyi Duruma Getirme Eklentisi, Dynamics 365 Supply Chain Management dışında gerçekleşecek master planlama hesaplamasını ve ilgili SQL veritabanını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="b00d4-104">The Planning Optimization Add-in for Microsoft Dynamics 365 Supply Chain Management enables master planning calculation to occur outside Dynamics 365 Supply Chain Management and the related SQL database.</span></span> <span data-ttu-id="b00d4-105">Planlamayı En İyi Duruma Getirme işleviyle ilişkili kazançlar arasında master planlama çalışmaları sırasında artan performans ve SQL veritabanı üzerinde en az etki vardır.</span><span class="sxs-lookup"><span data-stu-id="b00d4-105">The benefits that are associated with the Planning Optimization functionality include improved performance and minimal impact on SQL database during master planning runs.</span></span> <span data-ttu-id="b00d4-106">Hızlı planlama çalışmaları, planlayıcıların talep ve parametre değişikliklerine hemen tepki verebileceği şekilde ofis saatlerinde de yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="b00d4-106">Quick planning runs can be done even during office hours, so that planners can immediately react to demand or parameter changes.</span></span>

<span data-ttu-id="b00d4-107">Planlamayı En İyi Duruma Getirmeyi kullanmak için Microsoft Dynamics Lifecycle Services'taki (LCS) projenizden Planlamayı En İyi Duruma Getirme Eklentisi'ni yüklemeniz ve Supply Chain Management'ta Planlamayı En İyi Duruma Getirme işlevini açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b00d4-107">To use Planning Optimization, you must install the Planning Optimization Add-in from your project in Microsoft Dynamics Lifecycle Services (LCS) and turn on the Planning Optimization functionality in Supply Chain Management.</span></span> <span data-ttu-id="b00d4-108">Daha fazla bilgi için bkz. [Planlamayı En İyi Duruma Getirmeye başlayın](get-started.md).</span><span class="sxs-lookup"><span data-stu-id="b00d4-108">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="b00d4-109">Aşağıdaki resimde, Planlamayı En İyi Duruma Getirmeyi ofis saatlerinde çalıştırmanın avantajı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="b00d4-109">The following illustration shows the advantage of running Planning Optimization during office hours.</span></span>

![Planlamayı En İyi Duruma Getirmeyi ofis saatlerinde çalıştırmanın avantajı](media/PlanningOptimization1.png)

## <a name="improved-performance"></a><span data-ttu-id="b00d4-111">Artan performans</span><span class="sxs-lookup"><span data-stu-id="b00d4-111">Improved performance</span></span>

<span data-ttu-id="b00d4-112">Planlamayı En İyi Duruma Getirme, uzun süreli master planları içeren senaryolarda kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b00d4-112">Planning Optimization can be used in scenarios that involve long-running master plans.</span></span> <span data-ttu-id="b00d4-113">Özellikle çok büyük miktarlarda veri içeren çok hızlı hesaplamalar için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="b00d4-113">It's specifically designed for very fast calculations that involve very large volumes of data.</span></span> <span data-ttu-id="b00d4-114">Aşırı ölçeklenebilir çok kiracılı bir hizmet olarak oluşturulduğundan birden fazla kurulum, planı hesaplamak için aynı anda birlikte çalışabilir.</span><span class="sxs-lookup"><span data-stu-id="b00d4-114">Because it's built as a hyper-scalable multitenant service, multiple instances can work together simultaneously to calculate the plan.</span></span> <span data-ttu-id="b00d4-115">Ayrıca, planlama hizmeti sisteminizden master planlama yükünü kaldırır ve sunucu yükünü en aza indiren veri akışı ile çalışır.</span><span class="sxs-lookup"><span data-stu-id="b00d4-115">Additionally, the planning service removes the load of master planning from your system and works with a data stream that minimizes the server load.</span></span>

<span data-ttu-id="b00d4-116">Planlamayı En İyi Duruma Getirme aşağıdaki hedeflere ulaşmanıza yardımcı olabilir:</span><span class="sxs-lookup"><span data-stu-id="b00d4-116">Planning Optimization can help you achieve the following goals:</span></span>

- <span data-ttu-id="b00d4-117">Daha kısa çalışma zamanı üzerinden planlama performansını artırın.</span><span class="sxs-lookup"><span data-stu-id="b00d4-117">Improve planning performance through a shorter runtime.</span></span>
- <span data-ttu-id="b00d4-118">Master planlama çalışması sırasında diğer süreçler üzerindeki etkiyi azaltın.</span><span class="sxs-lookup"><span data-stu-id="b00d4-118">Reduce the impact on other processes during the master planning run.</span></span>
- <span data-ttu-id="b00d4-119">Daha sık planlama çalışmaları yapın.</span><span class="sxs-lookup"><span data-stu-id="b00d4-119">Do more frequent planning runs.</span></span> <span data-ttu-id="b00d4-120">(Günlük çalışmalarla sınırlı değilsiniz.)</span><span class="sxs-lookup"><span data-stu-id="b00d4-120">(You aren't limited to daily runs.)</span></span>
- <span data-ttu-id="b00d4-121">Gelecekteki işletme büyümesinin planlama sistemine aşırı yükleme yapmayacağından emin olun.</span><span class="sxs-lookup"><span data-stu-id="b00d4-121">Be confident that future business growth won't overload the planning system.</span></span>

## <a name="architecture-and-data-flow"></a><span data-ttu-id="b00d4-122">Mimari ve veri akışı</span><span class="sxs-lookup"><span data-stu-id="b00d4-122">Architecture and data flow</span></span>

<span data-ttu-id="b00d4-123">LCS'den Planlamayı En İyi Duruma Getirme Eklentisi yüklendiğinde Planlamayı En İyi Duruma Getirme hizmeti için güvenli bir bağlantı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b00d4-123">When the Planning Optimization Add-in is installed from LCS, a secure connection to the Planning Optimization service is established.</span></span> <span data-ttu-id="b00d4-124">Hizmet, ilgili Supply Chain Management kurulumu olarak aynı veri merkezi ülkesi veya bölgesinde bulunur.</span><span class="sxs-lookup"><span data-stu-id="b00d4-124">The service is located in the same data center country or region as the related Supply Chain Management instance.</span></span> <span data-ttu-id="b00d4-125">Planlamayı En İyi Duruma Getirme ayarlandıktan sonra master planlama çalıştırıldığında ana veriler ve hareket verileri Supply Chain Management'tan Planlamayı En İyi Duruma Getirme hizmetine gönderilir.</span><span class="sxs-lookup"><span data-stu-id="b00d4-125">After Planning Optimization is set up, when master planning is run, master data and transactional data are sent from Supply Chain Management to the Planning Optimization service.</span></span>

<span data-ttu-id="b00d4-126">Planlamayı En İyi Duruma Getirme Eklentisi kaldırılırsa Planlamayı En İyi Duruma Getirme hizmetindeki ilgili tüm veriler kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="b00d4-126">If the Planning Optimization Add-in is uninstalled, all related data in the Planning Optimization service is removed.</span></span>

### <a name="high-level-data-flow-for-regeneration-runs"></a><span data-ttu-id="b00d4-127">Yeniden oluşturma çalışmaları için üst düzey veri akışı</span><span class="sxs-lookup"><span data-stu-id="b00d4-127">High-level data flow for regeneration runs</span></span>

1. <span data-ttu-id="b00d4-128">Supply Chain Management istemcisi, Planlamayı En İyi Duruma Getirme hizmetinden bir planlama çalışması istemek için bir sinyal gönderir.</span><span class="sxs-lookup"><span data-stu-id="b00d4-128">The Supply Chain Management client sends a signal to request a planning run from Planning Optimization.</span></span>
2. <span data-ttu-id="b00d4-129">Planlamayı En İyi Duruma Getirme, tümleşik bağlayıcı aracılığıyla gerekli verileri ister.</span><span class="sxs-lookup"><span data-stu-id="b00d4-129">Planning Optimization requests the required data via the integrated connector.</span></span>
3. <span data-ttu-id="b00d4-130">SQL veritabanı, bağlayıcı aracılığıyla Planlamayı En İyi Duruma Getirme hizmetine ayar, ana veriler ve hareket verileri hakkında istenen bilgileri gönderir.</span><span class="sxs-lookup"><span data-stu-id="b00d4-130">The SQL database sends the requested information about setup, master, and transactional data to Planning Optimization via the connector.</span></span> <span data-ttu-id="b00d4-131">Bağlayıcı, Supply Chain Management ile Planlamayı En İyi Duruma Getirme hizmeti arasında bilgileri çevirir.</span><span class="sxs-lookup"><span data-stu-id="b00d4-131">The connector translates information between Supply Chain Management and the Planning Optimization service.</span></span>
4. <span data-ttu-id="b00d4-132">Planlamayı En İyi Duruma Getirme hizmeti, planlamayla ilgili verileri bellekte tutar ve gerekli hesaplamaları yapar.</span><span class="sxs-lookup"><span data-stu-id="b00d4-132">The Planning Optimization service holds planning-related data in memory and does the required calculations.</span></span>
5. <span data-ttu-id="b00d4-133">Planlama sonucu, bağlayıcı aracılığıyla Supply Chain Management veritabanına gönderilir.</span><span class="sxs-lookup"><span data-stu-id="b00d4-133">The planning result is sent to the Supply Chain Management database via the connector.</span></span> <span data-ttu-id="b00d4-134">Sonuçlar, planlı siparişler ve ilişkilendirme bilgileri gibi bilgiler içerir.</span><span class="sxs-lookup"><span data-stu-id="b00d4-134">The results include information such as planned orders and pegging information.</span></span> <span data-ttu-id="b00d4-135">Planlamayı En İyi Duruma Getirme hizmeti, planlama çalışmasının tamamlandığını belirletecek şekilde Supply Chain Management'a bir sinyal gönderir.</span><span class="sxs-lookup"><span data-stu-id="b00d4-135">Planning Optimization sends a signal to Supply Chain Management to indicate that the planning run has been completed.</span></span> <span data-ttu-id="b00d4-136">Ayrıca ilgili tüm iletileri ve uyarıları da gönderir.</span><span class="sxs-lookup"><span data-stu-id="b00d4-136">It also sends any relevant messages and warnings.</span></span>

<span data-ttu-id="b00d4-137">Aşağıdaki resimde, veri akışı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="b00d4-137">The following illustration shows the data flow.</span></span>

![Yeniden oluşturma çalışmaları için veri akışı](media/PlanningOptimization2.png)

## <a name="related-resources"></a><span data-ttu-id="b00d4-139">İlgili kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b00d4-139">Related resources</span></span>

[<span data-ttu-id="b00d4-140">Planlamayı En İyi Duruma Getirmeye başlayın</span><span class="sxs-lookup"><span data-stu-id="b00d4-140">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="b00d4-141">Planlamayı En İyi Duruma Getirme uygunluk analizi</span><span class="sxs-lookup"><span data-stu-id="b00d4-141">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="b00d4-142">Plan geçmişini ve planlama günlüklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="b00d4-142">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="b00d4-143">Plana filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="b00d4-143">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="b00d4-144">Planlama işini iptal etme</span><span class="sxs-lookup"><span data-stu-id="b00d4-144">Cancel a planning job</span></span>](cancel-planning-job.md)
