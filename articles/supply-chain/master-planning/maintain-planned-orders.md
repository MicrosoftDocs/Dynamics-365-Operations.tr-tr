---
title: Planlı siparişleri koruma
description: Bu konuda planlı siparişleri yönetme yöntemleri hakkında bilgiler yer alır. Planlı siparişlerin durumunun nasıl güncelleştirileceğini, kesinleştirileceğini ve seçilen planlı sipariş ile aynı duruma sahip planlı siparişlerin nasıl filtreleneceğini açıklar.
author: roxanadiaconu
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ddf2c7b4c67bec6c29387c78d1fdb021d85d702
ms.sourcegitcommit: 620e15555d176eec3905b48d5001af1c50107ce6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/09/2019
ms.locfileid: "1993452"
---
# <a name="maintain-planned-orders"></a><span data-ttu-id="6fad1-104">Planlı siparişleri koruma</span><span class="sxs-lookup"><span data-stu-id="6fad1-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6fad1-105">Bu konuda planlı siparişleri yönetme yöntemleri hakkında bilgiler yer alır.</span><span class="sxs-lookup"><span data-stu-id="6fad1-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="6fad1-106">Planlı siparişlerin durumunun nasıl güncelleştirileceğini, kesinleştirileceğini ve seçilen planlı sipariş ile aynı duruma sahip planlı siparişlerin nasıl filtreleneceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="6fad1-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="6fad1-107">Planlı siparişleri **Master planlama** çalışma alanından, **Planlı sipariş** listesinden veya **Planlı üretim emirleri**, **Planlı satınalma emirleri** ve **Planlı transfer** listelerinden yönetebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6fad1-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> 

## <a name="planned-order-status"></a><span data-ttu-id="6fad1-108">Planlı sipariş durumu</span><span class="sxs-lookup"><span data-stu-id="6fad1-108">Planned order status</span></span>
<span data-ttu-id="6fad1-109">İlerlemenizi takip etmeye yardımcı olan **Durum** alanını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6fad1-109">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="6fad1-110">Aşağıdaki değerler kullanılır:</span><span class="sxs-lookup"><span data-stu-id="6fad1-110">The following values are used:</span></span>

-   <span data-ttu-id="6fad1-111">Master planlama planlı siparişler ürettiğinde, planlı siparişler **İşlem görmedi** durumunda olur.</span><span class="sxs-lookup"><span data-stu-id="6fad1-111">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="6fad1-112">Planlı bir siparişi kesinleştirmemeye karar vermeniz halinde, durumunu **Tamamlandı** olarak ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6fad1-112">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="6fad1-113">Planlı bir siparişi kesinleştirmek isterseniz sipariş durumunu **Onaylandı** olarak değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6fad1-113">If you want to firm a planned order, you can change the status to **Approved**.</span></span> <span data-ttu-id="6fad1-114">Değiştirilmemeleri veya silinmemeleri için **Onaylandı** durumundaki planlı siparişlere ana planlama tarafından riayet edilir.</span><span class="sxs-lookup"><span data-stu-id="6fad1-114">Planned orders with **Approved** status are respected by master planning, so they are not modified or deleted.</span></span> 

## <a name="firming-planned-orders"></a><span data-ttu-id="6fad1-115">Planlı siparişleri kesinleştirme</span><span class="sxs-lookup"><span data-stu-id="6fad1-115">Firming planned orders</span></span> 
<span data-ttu-id="6fad1-116">Planlı siparişler kesinleştirilerek gerçek siparişler oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6fad1-116">By firming planned orders, real orders are created.</span></span> <span data-ttu-id="6fad1-117">Bunlar *serbest bırakılmış* veya *açık siparişler* olarak da bilinirler.</span><span class="sxs-lookup"><span data-stu-id="6fad1-117">These are also know as *released* or *open orders*.</span></span> <span data-ttu-id="6fad1-118">Planlı bir sipariş kesinleştirildiğinde, ilgili modülün siparişler bölümüne taşınır.</span><span class="sxs-lookup"><span data-stu-id="6fad1-118">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span>

<span data-ttu-id="6fad1-119">**Planlı siparişler** sayfasındaki iki kesinleştirme seçeneğinden birini belirleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="6fad1-119">You can select two firming options from the **Planned orders** page:</span></span>

-   <span data-ttu-id="6fad1-120">**Kesinleştir** – Bu seçenek, bir veya birden fazla seçili planlı siparişi kesinleştirir.</span><span class="sxs-lookup"><span data-stu-id="6fad1-120">**Firm** – This will firm one or multiple selected planned orders.</span></span>
-   <span data-ttu-id="6fad1-121">**Tümünü kesinleştir** – Bu seçenek, filtredeki tüm planlı siparişleri kesinleştirir.</span><span class="sxs-lookup"><span data-stu-id="6fad1-121">**Firm all** – This will firm all planned orders in the filter.</span></span> <span data-ttu-id="6fad1-122">**Tümünü kesinleştir** seçeneğini kullandığınızda planlı siparişi seçmeniz gerekmez; filtrdeki tüm planlı siparişler kesinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="6fad1-122">Using **Firm all** you don’t have to select the planned order, all planned orders within the filter will be firmed.</span></span> <span data-ttu-id="6fad1-123">Çok sayıda planlı siparişi kesinleştirmek istiyorsanız bu seçenek yararlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="6fad1-123">This option can be useful if you are firming a high number of planned orders.</span></span>

> [!NOTE]
> <span data-ttu-id="6fad1-124">**Planlı siparişler formu > Görüntüle > Kesinleştirme geçmişi** altındaki **Kesinleştirme geçmişi**'nden kesinleştirilen planlı bir siparişi izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6fad1-124">You can track a planned order that was firmed from **Firming history** under **Planned orders form > View > Firming history**.</span></span>

## <a name="parallelize-firming"></a><span data-ttu-id="6fad1-125">Kesinleştirmeyi paralel yap</span><span class="sxs-lookup"><span data-stu-id="6fad1-125">Parallelize firming</span></span>
<span data-ttu-id="6fad1-126">Birçok siparişi aynı anda kesinleştirmek istiyorsanız çalışmayı koşut hale getirmek, çalışma süresini veya performansını iyileştirebilir.</span><span class="sxs-lookup"><span data-stu-id="6fad1-126">If you are planning to firm many orders at the same time, parallelizing the run can improve the run time or performance.</span></span> <span data-ttu-id="6fad1-127">**Kesinleştir** veya **Tümünü kesinleştir** seçenekleriyle birden fazla planlı siparişi kesinleştirirken bu seçeneği kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6fad1-127">This option is available when firming multiple planned orders with either **Firm** or **Firm all**.</span></span> <span data-ttu-id="6fad1-128">Aşağıdaki parametreler kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="6fad1-128">The following parameters are available:</span></span>

-   <span data-ttu-id="6fad1-129">**Kesinleştirmeyi koşut hale getir** – **Evet** seçilirse kesinleştirme işlemi, **Dizi sayısı**'nda tanımlanan dizilerin sayısıyla koşut hale getirilir.</span><span class="sxs-lookup"><span data-stu-id="6fad1-129">**Parallelize firming** – If **Yes**, the firming process will be parallelized with the number of threads defined in **Number of threads**.</span></span>
-   <span data-ttu-id="6fad1-130">**Dizi sayısı** – Kesinleştirme işlemini koşut hale getirmek için kullanılan dizi sayısını denetler.</span><span class="sxs-lookup"><span data-stu-id="6fad1-130">**Number of threads** – Controls the number of threads used to parallelize the firming process.</span></span> <span data-ttu-id="6fad1-131">Parametre, yalnızca **Kesinleştirmeyi koşut hale getir** seçeneği **Evet** olarak ayarlandığında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="6fad1-131">The parameter is only shown when **Parallelize firming** is set to **Yes**.</span></span>


<a name="additional-resources"></a><span data-ttu-id="6fad1-132">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="6fad1-132">Additional resources</span></span>
--------

[<span data-ttu-id="6fad1-133">Master planlar</span><span class="sxs-lookup"><span data-stu-id="6fad1-133">Master plans</span></span>](master-plans.md)



