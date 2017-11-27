---
title: Gecikmeler
description: "Bu makale, ana planlamadaki gecikmeli tarihler hakkında bilgi sağlar. Gecikmeli bir tarih, bir hareketin talep edilen tarihi, ana planlama tarafından hesaplanan en erken tamamlanma tarihinden sonraysa alacağı gerçekçi bir tarihtir."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ed0df1abbf4f70ea70046eff7b91a25fdd59016c
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="delays"></a><span data-ttu-id="8e26a-104">Gecikmeler</span><span class="sxs-lookup"><span data-stu-id="8e26a-104">Delays</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="8e26a-105">Bu makale, ana planlamadaki gecikmeli tarihler hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="8e26a-105">This article provides information about delayed dates in master planning.</span></span> <span data-ttu-id="8e26a-106">Gecikmeli bir tarih, bir hareketin talep edilen tarihi, ana planlama tarafından hesaplanan en erken tamamlanma tarihinden sonraysa alacağı gerçekçi bir tarihtir.</span><span class="sxs-lookup"><span data-stu-id="8e26a-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="8e26a-107">Master planlama, bir işlem için en erken gerçekleşme tarihini teslim sürelerine, malzeme durumuna, kapasite durumuna ve çeşitli planlama parametrelerine göre hesaplayabilir.</span><span class="sxs-lookup"><span data-stu-id="8e26a-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="8e26a-108">Master planlama, bir sipariş tarihini mevcut tarihten önce hesaplıyorsa o sipariş zamanında gerçekleştirilemez.</span><span class="sxs-lookup"><span data-stu-id="8e26a-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="8e26a-109">Bu nedenle, sipariş gecikir.</span><span class="sxs-lookup"><span data-stu-id="8e26a-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="8e26a-110">Bu durumda master planlama, siparişi mevcut tarihten ileri doğru planlar ve teslim tarihlerini içerir..</span><span class="sxs-lookup"><span data-stu-id="8e26a-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="8e26a-111">Bu teslim tarihleri daha düşük seviyedeki bileşen ürünleriyle başlar.</span><span class="sxs-lookup"><span data-stu-id="8e26a-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="8e26a-112">Sipariş daha sonra bir gecikme tarihi alır.</span><span class="sxs-lookup"><span data-stu-id="8e26a-112">The order then receives a delayed date.</span></span> <span data-ttu-id="8e26a-113">Gecikme tarihi mevcut verilere göre belirlenmiş, gerçekçi bir teslim tarihidir.</span><span class="sxs-lookup"><span data-stu-id="8e26a-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="8e26a-114">Master planlama ayrıca gecikme gün sayısını da hesaplar.</span><span class="sxs-lookup"><span data-stu-id="8e26a-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="8e26a-115">Bazı durumlarda, örneğin kullanıcıların teslim sürelerini alternatif teslimat yöntemleri seçerek kısaltabileceklerini bildikleri durumlarda gecikmeleri hesaplamamayı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8e26a-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="8e26a-116">Tanımlı bir grup için gecikmelerin nasıl hesaplanacağını yapılandırılabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8e26a-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="8e26a-117">Ardından tanımlı grubu daha sonraki bir ürüne ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8e26a-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="8e26a-118">**Master planlama parametreleri** sayfasından gecikme hesaplaması için başlangıç saatini ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8e26a-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="8e26a-119">Bir sipariş bu saatten sonra tamamlanırsa, siparişin gecikme tarihine bir gün eklenir.</span><span class="sxs-lookup"><span data-stu-id="8e26a-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

<span data-ttu-id="8e26a-120">**Not:** Önceki sürümlerde hesaplanan gecikmeler, *gelecek mesajları*, gecikme tarihi *gelecek tarihi* ve geciken işlem *ileriye ayarlanmış bir işlem* olarak geçiyordu.</span><span class="sxs-lookup"><span data-stu-id="8e26a-120">**Note:** In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

<a name="see-also"></a><span data-ttu-id="8e26a-121">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="8e26a-121">See also</span></span>
--------

[<span data-ttu-id="8e26a-122">Kapsam ayarları</span><span class="sxs-lookup"><span data-stu-id="8e26a-122">Coverage settings</span></span>](coverage-settings.md)




