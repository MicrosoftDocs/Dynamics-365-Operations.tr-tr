---
title: Planlı siparişleri koruma
description: Bu konuda planlı siparişleri yönetme yöntemleri hakkında bilgiler yer alır. Planlı siparişlerin durumunun nasıl güncelleştirileceğini, kesinleştirileceğini ve seçilen planlı sipariş ile aynı duruma sahip planlı siparişlerin nasıl filtreleneceğini açıklar.
author: roxanadiaconu
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo, ReqTransFirmLog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f62381ca212e711fd61e12c9ec8f066ec124a933
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983036"
---
# <a name="maintain-planned-orders"></a><span data-ttu-id="ff924-104">Planlı siparişleri koruma</span><span class="sxs-lookup"><span data-stu-id="ff924-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ff924-105">Bu konuda planlı siparişleri yönetme yöntemleri hakkında bilgiler yer alır.</span><span class="sxs-lookup"><span data-stu-id="ff924-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="ff924-106">Planlı siparişlerin durumunun nasıl güncelleştirileceğini, kesinleştirileceğini ve seçilen planlı sipariş ile aynı duruma sahip planlı siparişlerin nasıl filtreleneceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="ff924-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="ff924-107">Planlı siparişleri **Master planlama** çalışma alanından, **Planlı sipariş** listesinden veya **Planlı üretim emirleri**, **Planlı satınalma emirleri** ve **Planlı transfer** listelerinden yönetebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ff924-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> 

## <a name="planned-order-status"></a><span data-ttu-id="ff924-108">Planlı sipariş durumu</span><span class="sxs-lookup"><span data-stu-id="ff924-108">Planned order status</span></span>
<span data-ttu-id="ff924-109">İlerlemenizi takip etmeye yardımcı olan **Durum** alanını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ff924-109">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="ff924-110">Aşağıdaki değerler kullanılır:</span><span class="sxs-lookup"><span data-stu-id="ff924-110">The following values are used:</span></span>

-   <span data-ttu-id="ff924-111">Master planlama planlı siparişler ürettiğinde, planlı siparişler **İşlem görmedi** durumunda olur.</span><span class="sxs-lookup"><span data-stu-id="ff924-111">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="ff924-112">Planlı bir siparişi kesinleştirmemeye karar vermeniz halinde, durumunu **Tamamlandı** olarak ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ff924-112">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="ff924-113">Planlı bir siparişi kesinleştirmek isterseniz sipariş durumunu **Onaylandı** olarak değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ff924-113">If you want to firm a planned order, you can change the status to **Approved**.</span></span> <span data-ttu-id="ff924-114">Sonraki bir master planlama çalışması sırasında değiştirilmemeleri veya silinmemeleri için **Onaylandı** durumundaki planlı siparişlere master planlama tarafından riayet edilir.</span><span class="sxs-lookup"><span data-stu-id="ff924-114">Planned orders with **Approved** status are respected by master planning, so they are not modified or deleted during a later master planning run.</span></span> <span data-ttu-id="ff924-115">Bunu başarmak için, planlama mantığı, Master planlama sırasında eski plan versiyonundaki **onaylanan** planlı siparişleri yeni plan sürümüne kopyalar.</span><span class="sxs-lookup"><span data-stu-id="ff924-115">To achieve this, the planning logic copies the **Approved** planned orders from the old plan version to the new plan version during master planning.</span></span>

## <a name="firming-planned-orders"></a><span data-ttu-id="ff924-116">Planlı siparişleri kesinleştirme</span><span class="sxs-lookup"><span data-stu-id="ff924-116">Firming planned orders</span></span> 
<span data-ttu-id="ff924-117">Planlı siparişler kesinleştirilerek gerçek siparişler oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ff924-117">By firming planned orders, real orders are created.</span></span> <span data-ttu-id="ff924-118">Bunlar *serbest bırakılmış* veya *açık siparişler* olarak da bilinirler.</span><span class="sxs-lookup"><span data-stu-id="ff924-118">These are also known as *released* or *open orders*.</span></span> <span data-ttu-id="ff924-119">Planlı bir sipariş kesinleştirildiğinde, ilgili modülün siparişler bölümüne taşınır.</span><span class="sxs-lookup"><span data-stu-id="ff924-119">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span>

<span data-ttu-id="ff924-120">**Planlı siparişler** sayfasındaki iki kesinleştirme seçeneğinden birini belirleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="ff924-120">You can select two firming options from the **Planned orders** page:</span></span>

-   <span data-ttu-id="ff924-121">**Kesinleştir** – Bu seçenek, bir veya birden fazla seçili planlı siparişi kesinleştirir.</span><span class="sxs-lookup"><span data-stu-id="ff924-121">**Firm** – This will firm one or multiple selected planned orders.</span></span>
-   <span data-ttu-id="ff924-122">**Tümünü kesinleştir** – Bu seçenek, filtredeki tüm planlı siparişleri kesinleştirir.</span><span class="sxs-lookup"><span data-stu-id="ff924-122">**Firm all** – This will firm all planned orders in the filter.</span></span> <span data-ttu-id="ff924-123">**Tümünü kesinleştir** seçeneğini kullandığınızda planlı siparişi seçmeniz gerekmez; filtrdeki tüm planlı siparişler kesinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="ff924-123">Using **Firm all** you don’t have to select the planned order, all planned orders within the filter will be firmed.</span></span> <span data-ttu-id="ff924-124">Çok sayıda planlı siparişi kesinleştirmek istiyorsanız bu seçenek yararlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="ff924-124">This option can be useful if you are firming a high number of planned orders.</span></span>

> [!NOTE]
> <span data-ttu-id="ff924-125">**Planlı siparişler formu > Görüntüle > Kesinleştirme geçmişi** altındaki **Kesinleştirme geçmişi**'nden kesinleştirilen planlı bir siparişi izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ff924-125">You can track a planned order that was firmed from **Firming history** under **Planned orders form > View > Firming history**.</span></span>

## <a name="parallelize-firming"></a><span data-ttu-id="ff924-126">Kesinleştirmeyi paralel yap</span><span class="sxs-lookup"><span data-stu-id="ff924-126">Parallelize firming</span></span>
<span data-ttu-id="ff924-127">Birçok siparişi aynı anda kesinleştirmek istiyorsanız çalışmayı koşut hale getirmek, çalışma süresini veya performansını iyileştirebilir.</span><span class="sxs-lookup"><span data-stu-id="ff924-127">If you are planning to firm many orders at the same time, parallelizing the run can improve the run time or performance.</span></span> <span data-ttu-id="ff924-128">**Kesinleştir** veya **Tümünü kesinleştir** seçenekleriyle birden fazla planlı siparişi kesinleştirirken bu seçeneği kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ff924-128">This option is available when firming multiple planned orders with either **Firm** or **Firm all**.</span></span> <span data-ttu-id="ff924-129">Aşağıdaki parametreler kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="ff924-129">The following parameters are available:</span></span>

-   <span data-ttu-id="ff924-130">**Kesinleştirmeyi koşut hale getir** – **Evet** seçilirse kesinleştirme işlemi, **Dizi sayısı**'nda tanımlanan dizilerin sayısıyla koşut hale getirilir.</span><span class="sxs-lookup"><span data-stu-id="ff924-130">**Parallelize firming** – If **Yes**, the firming process will be parallelized with the number of threads defined in **Number of threads**.</span></span>
-   <span data-ttu-id="ff924-131">**Dizi sayısı** – Kesinleştirme işlemini koşut hale getirmek için kullanılan dizi sayısını denetler.</span><span class="sxs-lookup"><span data-stu-id="ff924-131">**Number of threads** – Controls the number of threads used to parallelize the firming process.</span></span> <span data-ttu-id="ff924-132">Parametre, yalnızca **Kesinleştirmeyi koşut hale getir** seçeneği **Evet** olarak ayarlandığında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="ff924-132">The parameter is only shown when **Parallelize firming** is set to **Yes**.</span></span>

> [!NOTE]
> <span data-ttu-id="ff924-133">**Parallelize Kesinleştirme** seçeneği yalnızca Kesinleştirmede birden fazla planlı sipariş seçildiğinde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="ff924-133">The option for **Parallelize firming** is only shown when you have more than one planned order selected for firming.</span></span>

<a name="additional-resources"></a><span data-ttu-id="ff924-134">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="ff924-134">Additional resources</span></span>
--------

[<span data-ttu-id="ff924-135">Master planlara genel bakış</span><span class="sxs-lookup"><span data-stu-id="ff924-135">Master plans overview</span></span>](master-plans.md)



