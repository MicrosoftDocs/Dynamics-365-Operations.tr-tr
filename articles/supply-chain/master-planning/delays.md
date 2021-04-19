---
title: Gecikmeler
description: Bu konu, ana planlamadaki gecikmeli tarihler hakkında bilgi sağlar. Gecikmeli bir tarih, bir hareketin talep edilen tarihi, ana planlama tarafından hesaplanan en erken tamamlanma tarihinden sonraysa alacağı gerçekçi bir tarihtir.
author: roxanadiaconu
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4216ed1d9b981eee94cfd4c621abd1da99111512
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813687"
---
# <a name="delays"></a><span data-ttu-id="6f0d6-104">Gecikmeler</span><span class="sxs-lookup"><span data-stu-id="6f0d6-104">Delays</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f0d6-105">Bu konu, ana planlamadaki gecikmeli tarihler hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="6f0d6-105">This topic provides information about delayed dates in master planning.</span></span> <span data-ttu-id="6f0d6-106">Gecikmeli bir tarih, bir hareketin talep edilen tarihi, ana planlama tarafından hesaplanan en erken tamamlanma tarihinden sonraysa alacağı gerçekçi bir tarihtir.</span><span class="sxs-lookup"><span data-stu-id="6f0d6-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="6f0d6-107">Master planlama, bir işlem için en erken gerçekleşme tarihini teslim sürelerine, malzeme durumuna, kapasite durumuna ve çeşitli planlama parametrelerine göre hesaplayabilir.</span><span class="sxs-lookup"><span data-stu-id="6f0d6-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="6f0d6-108">Master planlama, bir sipariş tarihini mevcut tarihten önce hesaplıyorsa o sipariş zamanında gerçekleştirilemez.</span><span class="sxs-lookup"><span data-stu-id="6f0d6-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="6f0d6-109">Bu nedenle, sipariş gecikir.</span><span class="sxs-lookup"><span data-stu-id="6f0d6-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="6f0d6-110">Bu durumda master planlama, siparişi mevcut tarihten ileri doğru planlar ve teslim tarihlerini içerir..</span><span class="sxs-lookup"><span data-stu-id="6f0d6-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="6f0d6-111">Bu teslim tarihleri daha düşük seviyedeki bileşen ürünleriyle başlar.</span><span class="sxs-lookup"><span data-stu-id="6f0d6-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="6f0d6-112">Sipariş daha sonra bir gecikme tarihi alır.</span><span class="sxs-lookup"><span data-stu-id="6f0d6-112">The order then receives a delayed date.</span></span> <span data-ttu-id="6f0d6-113">Gecikme tarihi mevcut verilere göre belirlenmiş, gerçekçi bir teslim tarihidir.</span><span class="sxs-lookup"><span data-stu-id="6f0d6-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="6f0d6-114">Master planlama ayrıca gecikme gün sayısını da hesaplar.</span><span class="sxs-lookup"><span data-stu-id="6f0d6-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="6f0d6-115">Bazı durumlarda, örneğin kullanıcıların teslim sürelerini alternatif teslimat yöntemleri seçerek kısaltabileceklerini bildikleri durumlarda gecikmeleri hesaplamamayı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6f0d6-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="6f0d6-116">Tanımlı bir grup için gecikmelerin nasıl hesaplanacağını yapılandırılabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6f0d6-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="6f0d6-117">Ardından tanımlı grubu daha sonraki bir ürüne ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6f0d6-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="6f0d6-118">**Master planlama parametreleri** sayfasından gecikme hesaplaması için başlangıç saatini ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6f0d6-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="6f0d6-119">Bir sipariş bu saatten sonra tamamlanırsa, siparişin gecikme tarihine bir gün eklenir.</span><span class="sxs-lookup"><span data-stu-id="6f0d6-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

> [!NOTE]
> <span data-ttu-id="6f0d6-120">Önceki sürümlerde hesaplanan gecikmeler, *gelecek mesajları*, gecikme tarihi *gelecek tarihi* ve geciken hareket *ileriye ayarlanmış bir hareket* olarak geçiyordu.</span><span class="sxs-lookup"><span data-stu-id="6f0d6-120">In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

## <a name="limited-delays-in-production-setup-with-multiple-bom-levels"></a><span data-ttu-id="6f0d6-121">Birden çok ürün reçetesi düzeyi olan üretim kurulumunda sınırlı gecikmeler</span><span class="sxs-lookup"><span data-stu-id="6f0d6-121">Limited delays in production setup with multiple BOM levels</span></span>
<span data-ttu-id="6f0d6-122">Birden çok ürün reçetesi düzeyi olan bir üretim kurulumunda gecikmeler ile çalıştığınızda, yalnızca gecikmeye neden olan maddenin doğrudan üstündeki maddelerin (ürün reçetesi yapısında), master planlama çalıştırmasının bir parçası olarak güncelleştirileceği unutulmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="6f0d6-122">When you work with delays in a production setup that has multiple BOM levels, it is important to note that only the items directly above the item (in the BOM structure) causing the delay, will be updated with a delay as part of the master planning run.</span></span> <span data-ttu-id="6f0d6-123">En üst düzey için planlanan sipariş onaylandığında veya kesinleştirildiğinde, ürün reçetesi yapısındaki diğer maddeler, ilk master planlama çalıştırılıncaya kadar uygulanan gecikmeyi alamaz.</span><span class="sxs-lookup"><span data-stu-id="6f0d6-123">Other items in the BOM structure will not get the delay applied until the first master planning run, when the planned order for the top level is approved or firmed.</span></span> 

<span data-ttu-id="6f0d6-124">Bu bilinen sınırlamaya geçici bir çözüm bulmak için, ürün reçetesi yapısının üst kısmındaki üretim emirleri bir sonraki master planlama çalıştırılmadan önce onaylanabilir (veya kesinleştirilebilir).</span><span class="sxs-lookup"><span data-stu-id="6f0d6-124">To work around this known limitation, the production orders on the top of the BOM structure with delays can be approved (or firmed) prior to the next master planning run.</span></span> <span data-ttu-id="6f0d6-125">Bu şekilde, ertelenen onaylanmış planlı üretim emrinden gelen gecikme korunur ve tüm alt bileşenler de buna göre güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="6f0d6-125">This way the delay from the delayed approved planned production order will be kept and all underlying components will be updated accordingly.</span></span>
<span data-ttu-id="6f0d6-126">Eylem iletileri, ürün reçetesi yapısındaki başka gecikmelerden dolayı sonraki bir tarihe taşınabilecek planlı siparişleri tanımlamak için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6f0d6-126">Action messages can also be used to identify planned orders that can be moved to a later date, due to other delays in the BOM structure.</span></span>

## <a name="desired-date"></a><span data-ttu-id="6f0d6-127">İstenen tarih</span><span class="sxs-lookup"><span data-stu-id="6f0d6-127">Desired date</span></span>

<span data-ttu-id="6f0d6-128">**Planlanan siparişler** sayfasında, planlanan sipariş için **Gecikmeler** sekmesi, **İstenilen tarihtir**.</span><span class="sxs-lookup"><span data-stu-id="6f0d6-128">On the **Planned order** page, under the **Delays** tab is the **Desired date** for the planned order.</span></span> <span data-ttu-id="6f0d6-129">Planlanan siparişin istenilen tarihi, **Net Gereksinim**'den hesaplanan **Talep edilen tarih**'e eşit olan gecikmeler için temel tarihtir.</span><span class="sxs-lookup"><span data-stu-id="6f0d6-129">The desired date of a planned order is the base date for delays, which is a computed date that equals the **Requested date** calculated from the **Net Requirement**.</span></span> <span data-ttu-id="6f0d6-130">Planlanan sipariş bir BOM satırı, üretim satırı veya kanban satırıysa, istenilen tarih **Gereksinim tarihi** üzerine dayanır ve istenilen tarih **Planlanan sipariş** sayfasında görüntülenmez.</span><span class="sxs-lookup"><span data-stu-id="6f0d6-130">If the planned order is a BOM line, production line or kanban line, the desired date is based on the **Requirement date** and the desired date will not be shown on the **Planned order** page.</span></span>

<a name="additional-resources"></a><span data-ttu-id="6f0d6-131">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="6f0d6-131">Additional resources</span></span>
--------

[<span data-ttu-id="6f0d6-132">Kapsam ayarları</span><span class="sxs-lookup"><span data-stu-id="6f0d6-132">Coverage settings</span></span>](coverage-settings.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]