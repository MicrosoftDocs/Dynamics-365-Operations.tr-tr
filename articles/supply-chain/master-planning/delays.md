---
title: Gecikmeler
description: Bu konu, ana planlamadaki gecikmeli tarihler hakkında bilgi sağlar. Gecikmeli bir tarih, bir hareketin talep edilen tarihi, ana planlama tarafından hesaplanan en erken tamamlanma tarihinden sonraysa alacağı gerçekçi bir tarihtir.
author: roxanadiaconu
manager: AnnBe
ms.date: 03/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c26fedf15118a304469604527c33a25871356be
ms.sourcegitcommit: 8eac5eee94bb32143df44c82a2dfdbe903967af8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/20/2019
ms.locfileid: "878322"
---
# <a name="delays"></a><span data-ttu-id="1871a-104">Gecikmeler</span><span class="sxs-lookup"><span data-stu-id="1871a-104">Delays</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1871a-105">Bu konu, ana planlamadaki gecikmeli tarihler hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="1871a-105">This topic provides information about delayed dates in master planning.</span></span> <span data-ttu-id="1871a-106">Gecikmeli bir tarih, bir hareketin talep edilen tarihi, ana planlama tarafından hesaplanan en erken tamamlanma tarihinden sonraysa alacağı gerçekçi bir tarihtir.</span><span class="sxs-lookup"><span data-stu-id="1871a-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="1871a-107">Master planlama, bir işlem için en erken gerçekleşme tarihini teslim sürelerine, malzeme durumuna, kapasite durumuna ve çeşitli planlama parametrelerine göre hesaplayabilir.</span><span class="sxs-lookup"><span data-stu-id="1871a-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="1871a-108">Master planlama, bir sipariş tarihini mevcut tarihten önce hesaplıyorsa o sipariş zamanında gerçekleştirilemez.</span><span class="sxs-lookup"><span data-stu-id="1871a-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="1871a-109">Bu nedenle, sipariş gecikir.</span><span class="sxs-lookup"><span data-stu-id="1871a-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="1871a-110">Bu durumda master planlama, siparişi mevcut tarihten ileri doğru planlar ve teslim tarihlerini içerir..</span><span class="sxs-lookup"><span data-stu-id="1871a-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="1871a-111">Bu teslim tarihleri daha düşük seviyedeki bileşen ürünleriyle başlar.</span><span class="sxs-lookup"><span data-stu-id="1871a-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="1871a-112">Sipariş daha sonra bir gecikme tarihi alır.</span><span class="sxs-lookup"><span data-stu-id="1871a-112">The order then receives a delayed date.</span></span> <span data-ttu-id="1871a-113">Gecikme tarihi mevcut verilere göre belirlenmiş, gerçekçi bir teslim tarihidir.</span><span class="sxs-lookup"><span data-stu-id="1871a-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="1871a-114">Master planlama ayrıca gecikme gün sayısını da hesaplar.</span><span class="sxs-lookup"><span data-stu-id="1871a-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="1871a-115">Bazı durumlarda, örneğin kullanıcıların teslim sürelerini alternatif teslimat yöntemleri seçerek kısaltabileceklerini bildikleri durumlarda gecikmeleri hesaplamamayı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1871a-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="1871a-116">Tanımlı bir grup için gecikmelerin nasıl hesaplanacağını yapılandırılabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1871a-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="1871a-117">Ardından tanımlı grubu daha sonraki bir ürüne ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1871a-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="1871a-118">**Master planlama parametreleri** sayfasından gecikme hesaplaması için başlangıç saatini ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1871a-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="1871a-119">Bir sipariş bu saatten sonra tamamlanırsa, siparişin gecikme tarihine bir gün eklenir.</span><span class="sxs-lookup"><span data-stu-id="1871a-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

> <span data-ttu-id="1871a-120">[!NOT}: Önceki sürümlerde hesaplanan gecikmeler, *gelecek mesajları*, gecikme tarihi *gelecek tarihi* ve geciken işlem *ileriye ayarlanmış bir işlem* olarak geçiyordu.</span><span class="sxs-lookup"><span data-stu-id="1871a-120">[!NOTE} In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

## <a name="desired-date"></a><span data-ttu-id="1871a-121">İstenen tarih</span><span class="sxs-lookup"><span data-stu-id="1871a-121">Desired date</span></span>

<span data-ttu-id="1871a-122">**Planlanan siparişler** sayfasında, planlanan sipariş için **Gecikmeler** sekmesi, **İstenilen tarihtir**.</span><span class="sxs-lookup"><span data-stu-id="1871a-122">On the **Planned order** page, under the **Delays** tab is the **Desired date** for the planned order.</span></span> <span data-ttu-id="1871a-123">Planlanan siparişin istenilen tarihi, **Net Gereksinim**'den hesaplanan **Talep edilen tarih**'e eşit olan gecikmeler için temel tarihtir.</span><span class="sxs-lookup"><span data-stu-id="1871a-123">The desired date of a planned order is the base date for delays, which is a computed date that equals the **Requested date** calculated from the **Net Requirement**.</span></span> <span data-ttu-id="1871a-124">Planlanan sipariş bir BOM satırı, üretim satırı veya kanban satırıysa, istenilen tarih **Gereksinim tarihi** üzerine dayanır ve istenilen tarih **Planlanan sipariş** sayfasında görüntülenmez.</span><span class="sxs-lookup"><span data-stu-id="1871a-124">If the planned order is a BOM line, production line or kanban line, the desired date is based on the **Requirement date** and the desired date will not be shown on the **Planned order** page.</span></span>

<a name="additional-resources"></a><span data-ttu-id="1871a-125">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="1871a-125">Additional resources</span></span>
--------

[<span data-ttu-id="1871a-126">Kapsam ayarları</span><span class="sxs-lookup"><span data-stu-id="1871a-126">Coverage settings</span></span>](coverage-settings.md)
