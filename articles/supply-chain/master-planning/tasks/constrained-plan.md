---
title: Kısıtlanmış plan oluşturma
description: Bu yordam, hem malzeme hem de kapasite kısıtlamalarını dikkate alan bir planın nasıl oluşturulacağını gösterir.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72cddd58b7068e08cddf24df83da8da2f7af7168
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845330"
---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="5d878-103">Kısıtlanmış plan oluşturma</span><span class="sxs-lookup"><span data-stu-id="5d878-103">Generate a constrained plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5d878-104">Bu yordam, hem malzeme hem de kapasite kısıtlamalarını dikkate alan bir planın nasıl oluşturulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5d878-104">This procedure shows how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="5d878-105">Plan, üretimin malzemeler hazır olmadan ve kaynaklar kapasite üzerinde rezerve edilmeden önce başlamamasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="5d878-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="5d878-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="5d878-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="5d878-107">Bu yordam için üretim planlayıcısına yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="5d878-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="5d878-108">Kısıtlı bir plan ayarlayın</span><span class="sxs-lookup"><span data-stu-id="5d878-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="5d878-109">Master planlama'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5d878-109">Click Master planning.</span></span>
2. <span data-ttu-id="5d878-110">Master planlar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5d878-110">Click Master plans.</span></span>
3. <span data-ttu-id="5d878-111">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="5d878-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5d878-112">Örnek: StaticPlan</span><span class="sxs-lookup"><span data-stu-id="5d878-112">Example: StaticPlan</span></span>  
4. <span data-ttu-id="5d878-113">Sınırlı kapasite alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5d878-113">Select Yes in the Finite capacity field.</span></span>
5. <span data-ttu-id="5d878-114">Sınırlı kapasite zaman dilimi alanına '30' girin.</span><span class="sxs-lookup"><span data-stu-id="5d878-114">In the Finite capacity time fence field, enter '30'.</span></span>
6. <span data-ttu-id="5d878-115">Gün cinsinden zaman dilimleri bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="5d878-115">Expand the Time fences in days section.</span></span>
7. <span data-ttu-id="5d878-116">Kapasite alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5d878-116">Select Yes in the Capacity field.</span></span>
8. <span data-ttu-id="5d878-117">Kapasite planlama zaman dilimi (gün) alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="5d878-117">In the Capacity scheduling time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="5d878-118">Örnek: 60</span><span class="sxs-lookup"><span data-stu-id="5d878-118">Example: 60</span></span>  
9. <span data-ttu-id="5d878-119">Hesaplanan gecikmeler alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5d878-119">Select Yes in the Calculated delays field.</span></span>
10. <span data-ttu-id="5d878-120">Gecikme zaman dilimini (gün) hesapla alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="5d878-120">In the Calculate delays time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="5d878-121">Örnek: 60</span><span class="sxs-lookup"><span data-stu-id="5d878-121">Example: 60</span></span>  
11. <span data-ttu-id="5d878-122">Hesaplanan gecikmeler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="5d878-122">Expand the Calculated delays section.</span></span>
12. <span data-ttu-id="5d878-123">Hesaplanan gecikmeyi gereksinim tarihine ekle alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5d878-123">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
13. <span data-ttu-id="5d878-124">Hesaplanan gecikmeyi gereksinim tarihine ekle alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5d878-124">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
14. <span data-ttu-id="5d878-125">Hesaplanan gecikmeyi gereksinim tarihine ekle alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5d878-125">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
15. <span data-ttu-id="5d878-126">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="5d878-126">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="5d878-127">Sınırlandırılmış bir plan oluşturma</span><span class="sxs-lookup"><span data-stu-id="5d878-127">Create a constrained plan</span></span>
1. <span data-ttu-id="5d878-128">Çalıştır öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5d878-128">Click Run.</span></span>
2. <span data-ttu-id="5d878-129">Master plan alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="5d878-129">In the Master plan field, enter or select a value.</span></span>
    * <span data-ttu-id="5d878-130">Kısıtlamalar ayarladığınız planı seçin.</span><span class="sxs-lookup"><span data-stu-id="5d878-130">Select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="5d878-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5d878-131">Click OK.</span></span>
    * <span data-ttu-id="5d878-132">Bu işlem biraz zaman alabilir.</span><span class="sxs-lookup"><span data-stu-id="5d878-132">This may take a while.</span></span>  
4. <span data-ttu-id="5d878-133">Planlı siparişler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5d878-133">Click Planned orders.</span></span>

