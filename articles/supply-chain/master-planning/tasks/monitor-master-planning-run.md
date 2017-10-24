--- 
title: "Master planlama çalışmasını izleme"
description: "Üretim planlayıcısı, bir master planlama çalışmasının devam edip etmediğini görmek istiyor."
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1e08d9fd3388561563e6fb982416186a652b4ce2
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="2d1ee-103">Master planlama çalışmasını izleme</span><span class="sxs-lookup"><span data-stu-id="2d1ee-103">Monitor a master planning run</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2d1ee-104">Üretim planlayıcısı, bir master planlama çalışmasının devam edip etmediğini görmek istiyor.</span><span class="sxs-lookup"><span data-stu-id="2d1ee-104">The production planner wants to see if a master planning run is in progress.</span></span> <span data-ttu-id="2d1ee-105">Bu prosedürü tamamlamak için USMF demo veri şirketini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2d1ee-105">Use the demo data company USMF to complete this procedure.</span></span>


## <a name="run-master-planning"></a><span data-ttu-id="2d1ee-106">Master planlamayı çalıştırma</span><span class="sxs-lookup"><span data-stu-id="2d1ee-106">Run master planning</span></span>
1. <span data-ttu-id="2d1ee-107">Master planlama'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2d1ee-107">Click Master planning.</span></span>
    * <span data-ttu-id="2d1ee-108">Bunu varsayılan panosunda bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2d1ee-108">You'll find this on the default dashboard.</span></span>  
2. <span data-ttu-id="2d1ee-109">Plan alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="2d1ee-109">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="2d1ee-110">Örnek: StaticPlan</span><span class="sxs-lookup"><span data-stu-id="2d1ee-110">Example: StaticPlan</span></span>  
3. <span data-ttu-id="2d1ee-111">Çalıştır öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2d1ee-111">Click Run.</span></span>
4. <span data-ttu-id="2d1ee-112">Takip işleme süresi alanından Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2d1ee-112">Select Yes in the Track processing time field.</span></span>
    * <span data-ttu-id="2d1ee-113">Alan zaten seçilmişse bu adımı atlayın.</span><span class="sxs-lookup"><span data-stu-id="2d1ee-113">If the field is already selected, skip this step.</span></span>  
5. <span data-ttu-id="2d1ee-114">İş parçacığı sayısı alanına bir rakam girin.</span><span class="sxs-lookup"><span data-stu-id="2d1ee-114">In the Number of threads field, enter a number.</span></span>
6. <span data-ttu-id="2d1ee-115">Eklenecek kayıtlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="2d1ee-115">Expand the Records to include section.</span></span>
7. <span data-ttu-id="2d1ee-116">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2d1ee-116">Click Filter.</span></span>
8. <span data-ttu-id="2d1ee-117">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="2d1ee-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="2d1ee-118">Alan = Madde numarası olan sırayı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="2d1ee-118">Mark the row where Field = Item number.</span></span>  
9. <span data-ttu-id="2d1ee-119">Ölçütler alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="2d1ee-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="2d1ee-120">Örnek: T0001</span><span class="sxs-lookup"><span data-stu-id="2d1ee-120">Example: T0001</span></span>  
10. <span data-ttu-id="2d1ee-121">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2d1ee-121">Click OK.</span></span>
11. <span data-ttu-id="2d1ee-122">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2d1ee-122">Click OK.</span></span>

## <a name="monitor-the-master-planning-run"></a><span data-ttu-id="2d1ee-123">Master planlama yürütmeyi izleme</span><span class="sxs-lookup"><span data-stu-id="2d1ee-123">Monitor the master planning run</span></span>
1. <span data-ttu-id="2d1ee-124">Geçmiş öğesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2d1ee-124">Click History.</span></span>
2. <span data-ttu-id="2d1ee-125">Sorgulamalar’ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2d1ee-125">Click Inquiries.</span></span>
3. <span data-ttu-id="2d1ee-126">İşlem görevi süresi öğesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2d1ee-126">Click Process task duration.</span></span>
4. <span data-ttu-id="2d1ee-127">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="2d1ee-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2d1ee-128">Her madde için, planlama adımlarının her birinin ne kadar sürede tamamlandığını görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2d1ee-128">For each item you can get an overview of how long it took to complete each planning step.</span></span>  


