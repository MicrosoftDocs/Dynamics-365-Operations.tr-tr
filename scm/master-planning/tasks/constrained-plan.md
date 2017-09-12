--- 
title: "Kısıtlanmış plan oluşturma"
description: "Bu yordam, hem malzeme hem de kapasite kısıtlamalarını dikkate alan bir planın nasıl oluşturulacağını gösterir."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 9deb615d05b90865ea6a050599bf91879b5688d0
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="ef479-103">Kısıtlanmış plan oluşturma</span><span class="sxs-lookup"><span data-stu-id="ef479-103">Generate a constrained plan</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ef479-104">Bu yordam, hem malzeme hem de kapasite kısıtlamalarını dikkate alan bir planın nasıl oluşturulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ef479-104">This procedure shows how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="ef479-105">Plan, üretimin malzemeler hazır olmadan ve kaynaklar kapasite üzerinde rezerve edilmeden önce başlamamasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="ef479-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="ef479-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="ef479-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ef479-107">Bu yordam için üretim planlayıcısına yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="ef479-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="ef479-108">Kısıtlı bir plan ayarlayın</span><span class="sxs-lookup"><span data-stu-id="ef479-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="ef479-109">Master planlama'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ef479-109">Click Master planning.</span></span>
2. <span data-ttu-id="ef479-110">Master planlar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ef479-110">Click Master plans.</span></span>
3. <span data-ttu-id="ef479-111">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ef479-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ef479-112">Örnek: StaticPlan</span><span class="sxs-lookup"><span data-stu-id="ef479-112">Example: StaticPlan</span></span>  
4. <span data-ttu-id="ef479-113">Sınırlı kapasite alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ef479-113">Select Yes in the Finite capacity field.</span></span>
5. <span data-ttu-id="ef479-114">Sınırlı kapasite zaman dilimi alanına '30' girin.</span><span class="sxs-lookup"><span data-stu-id="ef479-114">In the Finite capacity time fence field, enter '30'.</span></span>
6. <span data-ttu-id="ef479-115">Gün cinsinden zaman dilimleri bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="ef479-115">Expand the Time fences in days section.</span></span>
7. <span data-ttu-id="ef479-116">Kapasite alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ef479-116">Select Yes in the Capacity field.</span></span>
8. <span data-ttu-id="ef479-117">Kapasite planlama zaman dilimi (gün) alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="ef479-117">In the Capacity scheduling time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="ef479-118">Örnek: 60</span><span class="sxs-lookup"><span data-stu-id="ef479-118">Example: 60</span></span>  
9. <span data-ttu-id="ef479-119">Hesaplanan gecikmeler alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ef479-119">Select Yes in the Calculated delays field.</span></span>
10. <span data-ttu-id="ef479-120">Gecikme zaman dilimini (gün) hesapla alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="ef479-120">In the Calculate delays time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="ef479-121">Örnek: 60</span><span class="sxs-lookup"><span data-stu-id="ef479-121">Example: 60</span></span>  
11. <span data-ttu-id="ef479-122">Hesaplanan gecikmeler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="ef479-122">Expand the Calculated delays section.</span></span>
12. <span data-ttu-id="ef479-123">Hesaplanan gecikmeyi gereksinim tarihine ekle alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ef479-123">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
13. <span data-ttu-id="ef479-124">Hesaplanan gecikmeyi gereksinim tarihine ekle alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ef479-124">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
14. <span data-ttu-id="ef479-125">Hesaplanan gecikmeyi gereksinim tarihine ekle alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ef479-125">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
15. <span data-ttu-id="ef479-126">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ef479-126">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="ef479-127">Sınırlandırılmış bir plan oluşturma</span><span class="sxs-lookup"><span data-stu-id="ef479-127">Create a constrained plan</span></span>
1. <span data-ttu-id="ef479-128">Çalıştır öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ef479-128">Click Run.</span></span>
2. <span data-ttu-id="ef479-129">Master plan alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="ef479-129">In the Master plan field, enter or select a value.</span></span>
    * <span data-ttu-id="ef479-130">Kısıtlamalar ayarladığınız planı seçin.</span><span class="sxs-lookup"><span data-stu-id="ef479-130">Select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="ef479-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ef479-131">Click OK.</span></span>
    * <span data-ttu-id="ef479-132">Bu işlem biraz zaman alabilir.</span><span class="sxs-lookup"><span data-stu-id="ef479-132">This may take a while.</span></span>  
4. <span data-ttu-id="ef479-133">Planlı siparişler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ef479-133">Click Planned orders.</span></span>


