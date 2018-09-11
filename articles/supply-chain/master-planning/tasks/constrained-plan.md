--- 
title: "Kısıtlanmış plan oluşturma"
description: "Bu yordam, hem malzeme hem de kapasite kısıtlamalarını dikkate alan bir planın nasıl oluşturulacağını gösterir."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 6dfda1664e487bb4d31cf3e9aaee191dc69d699a
ms.contentlocale: tr-tr
ms.lasthandoff: 09/11/2018

---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="c6d67-103">Kısıtlanmış plan oluşturma</span><span class="sxs-lookup"><span data-stu-id="c6d67-103">Generate a constrained plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c6d67-104">Bu yordam, hem malzeme hem de kapasite kısıtlamalarını dikkate alan bir planın nasıl oluşturulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c6d67-104">This procedure shows how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="c6d67-105">Plan, üretimin malzemeler hazır olmadan ve kaynaklar kapasite üzerinde rezerve edilmeden önce başlamamasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="c6d67-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="c6d67-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="c6d67-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c6d67-107">Bu yordam için üretim planlayıcısına yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="c6d67-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="c6d67-108">Kısıtlı bir plan ayarlayın</span><span class="sxs-lookup"><span data-stu-id="c6d67-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="c6d67-109">Master planlama'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c6d67-109">Click Master planning.</span></span>
2. <span data-ttu-id="c6d67-110">Master planlar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c6d67-110">Click Master plans.</span></span>
3. <span data-ttu-id="c6d67-111">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="c6d67-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c6d67-112">Örnek: StaticPlan</span><span class="sxs-lookup"><span data-stu-id="c6d67-112">Example: StaticPlan</span></span>  
4. <span data-ttu-id="c6d67-113">Sınırlı kapasite alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c6d67-113">Select Yes in the Finite capacity field.</span></span>
5. <span data-ttu-id="c6d67-114">Sınırlı kapasite zaman dilimi alanına '30' girin.</span><span class="sxs-lookup"><span data-stu-id="c6d67-114">In the Finite capacity time fence field, enter '30'.</span></span>
6. <span data-ttu-id="c6d67-115">Gün cinsinden zaman dilimleri bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="c6d67-115">Expand the Time fences in days section.</span></span>
7. <span data-ttu-id="c6d67-116">Kapasite alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c6d67-116">Select Yes in the Capacity field.</span></span>
8. <span data-ttu-id="c6d67-117">Kapasite planlama zaman dilimi (gün) alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="c6d67-117">In the Capacity scheduling time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="c6d67-118">Örnek: 60</span><span class="sxs-lookup"><span data-stu-id="c6d67-118">Example: 60</span></span>  
9. <span data-ttu-id="c6d67-119">Hesaplanan gecikmeler alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c6d67-119">Select Yes in the Calculated delays field.</span></span>
10. <span data-ttu-id="c6d67-120">Gecikme zaman dilimini (gün) hesapla alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="c6d67-120">In the Calculate delays time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="c6d67-121">Örnek: 60</span><span class="sxs-lookup"><span data-stu-id="c6d67-121">Example: 60</span></span>  
11. <span data-ttu-id="c6d67-122">Hesaplanan gecikmeler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="c6d67-122">Expand the Calculated delays section.</span></span>
12. <span data-ttu-id="c6d67-123">Hesaplanan gecikmeyi gereksinim tarihine ekle alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c6d67-123">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
13. <span data-ttu-id="c6d67-124">Hesaplanan gecikmeyi gereksinim tarihine ekle alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c6d67-124">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
14. <span data-ttu-id="c6d67-125">Hesaplanan gecikmeyi gereksinim tarihine ekle alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c6d67-125">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
15. <span data-ttu-id="c6d67-126">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c6d67-126">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="c6d67-127">Sınırlandırılmış bir plan oluşturma</span><span class="sxs-lookup"><span data-stu-id="c6d67-127">Create a constrained plan</span></span>
1. <span data-ttu-id="c6d67-128">Çalıştır öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c6d67-128">Click Run.</span></span>
2. <span data-ttu-id="c6d67-129">Master plan alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="c6d67-129">In the Master plan field, enter or select a value.</span></span>
    * <span data-ttu-id="c6d67-130">Kısıtlamalar ayarladığınız planı seçin.</span><span class="sxs-lookup"><span data-stu-id="c6d67-130">Select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="c6d67-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c6d67-131">Click OK.</span></span>
    * <span data-ttu-id="c6d67-132">Bu işlem biraz zaman alabilir.</span><span class="sxs-lookup"><span data-stu-id="c6d67-132">This may take a while.</span></span>  
4. <span data-ttu-id="c6d67-133">Planlı siparişler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c6d67-133">Click Planned orders.</span></span>


