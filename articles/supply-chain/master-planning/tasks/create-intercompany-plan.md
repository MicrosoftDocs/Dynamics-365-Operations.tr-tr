---
title: Şirketlerarası plan oluşturma
description: Bu yordam şirketlerarası plan oluşturmayı gösterir.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d378a89bbb4de6d67db0019dc72a27945d50c4e9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "333749"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="8db0c-103">Şirketlerarası plan oluşturma</span><span class="sxs-lookup"><span data-stu-id="8db0c-103">Create an intercompany plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8db0c-104">Bu yordam şirketlerarası plan oluşturmayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="8db0c-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="8db0c-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="8db0c-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="8db0c-106">Şirketlerarası planlama grubu ayarlama</span><span class="sxs-lookup"><span data-stu-id="8db0c-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="8db0c-107">Şirketlerarası planlama grupları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="8db0c-107">Go to Intercompany planning groups.</span></span>
    * <span data-ttu-id="8db0c-108">Master planlama > Kurulum > Şirketlerarası planlama grupları</span><span class="sxs-lookup"><span data-stu-id="8db0c-108">Master planning > Setup > Intercompany planning groups</span></span>  
2. <span data-ttu-id="8db0c-109">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="8db0c-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="8db0c-110">Örneğin, İsim alanı üzerinde '10' değerini girerek filtreleme yapın.</span><span class="sxs-lookup"><span data-stu-id="8db0c-110">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="8db0c-111">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="8db0c-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="8db0c-112">Sil'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8db0c-112">Click Delete.</span></span>
    * <span data-ttu-id="8db0c-113">Bu adım, şirketlerarası planlama çalışmasını kısaltmak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="8db0c-113">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="8db0c-114">Şirketlerarası planlama, en düşük planlama serisinden başlayarak bir planlama grubu içindeki tüm şirketlerde master planlamayı çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="8db0c-114">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="8db0c-115">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8db0c-115">Click Yes.</span></span>
6. <span data-ttu-id="8db0c-116">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8db0c-116">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="8db0c-117">Şirketlerarası plan oluşturma</span><span class="sxs-lookup"><span data-stu-id="8db0c-117">Create an intercompany plan</span></span>
1. <span data-ttu-id="8db0c-118">Şirketlerarası master planlama'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8db0c-118">Click Intercompany master planning.</span></span>
    * <span data-ttu-id="8db0c-119">Bu, Master planlama çalışma alanında olur.</span><span class="sxs-lookup"><span data-stu-id="8db0c-119">This is on the Master planning workspace.</span></span>  
2. <span data-ttu-id="8db0c-120">Şirketlerarası planlama grubu alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8db0c-120">In the Intercompany planning group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="8db0c-121">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8db0c-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8db0c-122">Şirketlerarası planlama grubu 10'u seçin.</span><span class="sxs-lookup"><span data-stu-id="8db0c-122">Select intercompany planning group 10.</span></span>  
4. <span data-ttu-id="8db0c-123">Şirketlerarası planlama tekrar sayısı alanına '2' yazın.</span><span class="sxs-lookup"><span data-stu-id="8db0c-123">In the Number of intercompany planning iterations field, enter '2'.</span></span>
    * <span data-ttu-id="8db0c-124">Şirketlerarası planlama grubu 10 iki üyeye sahip.</span><span class="sxs-lookup"><span data-stu-id="8db0c-124">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="8db0c-125">Gecikmeleri kaynak şirketten (USMF) müşteri şirkete (DEMF) yaymak için, iki şirkette de şirketlerarası işlevini iki kez çalıştırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="8db0c-125">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="8db0c-126">İlk tekrar, talebi yayar ve kaynak şirketteki (USMF) gecikmeleri tanımlar.</span><span class="sxs-lookup"><span data-stu-id="8db0c-126">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="8db0c-127">İkinci tekrar, gecikmeleri USMF'den DEMF'ye yayar.</span><span class="sxs-lookup"><span data-stu-id="8db0c-127">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
5. <span data-ttu-id="8db0c-128">İlk tekrarlama alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="8db0c-128">In the First iteration field, select an option.</span></span>
6. <span data-ttu-id="8db0c-129">İlk tekrarlama alanında 'Yeniden oluşturma' seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="8db0c-129">In the First iteration field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="8db0c-130">Sonraki tekrarlamalar alanında 'Yeniden oluşturma' seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="8db0c-130">In the Subsequent iterations field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="8db0c-131">İş parçacığı sayısı alanına bir rakam girin.</span><span class="sxs-lookup"><span data-stu-id="8db0c-131">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="8db0c-132">Bu, planlama için kullanılan paralel iş parçacıklarının sayısını temsil eder.</span><span class="sxs-lookup"><span data-stu-id="8db0c-132">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="8db0c-133">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8db0c-133">Click OK.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="8db0c-134">Planın sonucunu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="8db0c-134">View the result of the plan</span></span>
1. <span data-ttu-id="8db0c-135">Plan alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8db0c-135">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="8db0c-136">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8db0c-136">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8db0c-137">StaticPlan için bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8db0c-137">Click the link for StaticPlan.</span></span> <span data-ttu-id="8db0c-138">USMF şirketinde olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="8db0c-138">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="8db0c-139">Planlı siparişler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8db0c-139">Click Planned orders.</span></span>

