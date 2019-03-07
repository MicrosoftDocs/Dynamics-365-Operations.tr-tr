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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0e2265f7788fd2a4a37f6fb96d7562649dbc5b1c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "336049"
---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="08cf0-103">Kısıtlanmış plan oluşturma</span><span class="sxs-lookup"><span data-stu-id="08cf0-103">Generate a constrained plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="08cf0-104">Bu yordam, hem malzeme hem de kapasite kısıtlamalarını dikkate alan bir planın nasıl oluşturulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="08cf0-104">This procedure shows how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="08cf0-105">Plan, üretimin malzemeler hazır olmadan ve kaynaklar kapasite üzerinde rezerve edilmeden önce başlamamasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="08cf0-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="08cf0-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="08cf0-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="08cf0-107">Bu yordam için üretim planlayıcısına yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="08cf0-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="08cf0-108">Kısıtlı bir plan ayarlayın</span><span class="sxs-lookup"><span data-stu-id="08cf0-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="08cf0-109">Master planlama'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="08cf0-109">Click Master planning.</span></span>
2. <span data-ttu-id="08cf0-110">Master planlar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="08cf0-110">Click Master plans.</span></span>
3. <span data-ttu-id="08cf0-111">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="08cf0-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="08cf0-112">Örnek: StaticPlan</span><span class="sxs-lookup"><span data-stu-id="08cf0-112">Example: StaticPlan</span></span>  
4. <span data-ttu-id="08cf0-113">Sınırlı kapasite alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="08cf0-113">Select Yes in the Finite capacity field.</span></span>
5. <span data-ttu-id="08cf0-114">Sınırlı kapasite zaman dilimi alanına '30' girin.</span><span class="sxs-lookup"><span data-stu-id="08cf0-114">In the Finite capacity time fence field, enter '30'.</span></span>
6. <span data-ttu-id="08cf0-115">Gün cinsinden zaman dilimleri bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="08cf0-115">Expand the Time fences in days section.</span></span>
7. <span data-ttu-id="08cf0-116">Kapasite alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="08cf0-116">Select Yes in the Capacity field.</span></span>
8. <span data-ttu-id="08cf0-117">Kapasite planlama zaman dilimi (gün) alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="08cf0-117">In the Capacity scheduling time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="08cf0-118">Örnek: 60</span><span class="sxs-lookup"><span data-stu-id="08cf0-118">Example: 60</span></span>  
9. <span data-ttu-id="08cf0-119">Hesaplanan gecikmeler alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="08cf0-119">Select Yes in the Calculated delays field.</span></span>
10. <span data-ttu-id="08cf0-120">Gecikme zaman dilimini (gün) hesapla alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="08cf0-120">In the Calculate delays time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="08cf0-121">Örnek: 60</span><span class="sxs-lookup"><span data-stu-id="08cf0-121">Example: 60</span></span>  
11. <span data-ttu-id="08cf0-122">Hesaplanan gecikmeler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="08cf0-122">Expand the Calculated delays section.</span></span>
12. <span data-ttu-id="08cf0-123">Hesaplanan gecikmeyi gereksinim tarihine ekle alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="08cf0-123">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
13. <span data-ttu-id="08cf0-124">Hesaplanan gecikmeyi gereksinim tarihine ekle alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="08cf0-124">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
14. <span data-ttu-id="08cf0-125">Hesaplanan gecikmeyi gereksinim tarihine ekle alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="08cf0-125">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
15. <span data-ttu-id="08cf0-126">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="08cf0-126">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="08cf0-127">Sınırlandırılmış bir plan oluşturma</span><span class="sxs-lookup"><span data-stu-id="08cf0-127">Create a constrained plan</span></span>
1. <span data-ttu-id="08cf0-128">Çalıştır öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="08cf0-128">Click Run.</span></span>
2. <span data-ttu-id="08cf0-129">Master plan alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="08cf0-129">In the Master plan field, enter or select a value.</span></span>
    * <span data-ttu-id="08cf0-130">Kısıtlamalar ayarladığınız planı seçin.</span><span class="sxs-lookup"><span data-stu-id="08cf0-130">Select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="08cf0-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="08cf0-131">Click OK.</span></span>
    * <span data-ttu-id="08cf0-132">Bu işlem biraz zaman alabilir.</span><span class="sxs-lookup"><span data-stu-id="08cf0-132">This may take a while.</span></span>  
4. <span data-ttu-id="08cf0-133">Planlı siparişler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="08cf0-133">Click Planned orders.</span></span>

