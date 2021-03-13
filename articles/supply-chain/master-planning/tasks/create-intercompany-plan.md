---
title: Şirketlerarası plan oluşturma
description: Bu yordam şirketlerarası plan oluşturmayı gösterir.
author: ShylaThompson
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c368e461860a41d0110f5aed79c2aac49c437d68
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011430"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="23532-103">Şirketlerarası plan oluşturma</span><span class="sxs-lookup"><span data-stu-id="23532-103">Create an intercompany plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="23532-104">Bu yordam şirketlerarası plan oluşturmayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="23532-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="23532-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="23532-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="23532-106">Şirketlerarası planlama grubu ayarlama</span><span class="sxs-lookup"><span data-stu-id="23532-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="23532-107">**Gezinti bölmesinde**, **Modüller > Master planlama > Kurulum > Şirketlerarası planlama grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="23532-107">In the **Navigation pane**, go to **Modules > Master planning > Setup > Intercompany planning groups**.</span></span> 
2. <span data-ttu-id="23532-108">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="23532-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="23532-109">Örneğin, İsim alanı üzerinde '10' değerini girerek filtreleme yapın.</span><span class="sxs-lookup"><span data-stu-id="23532-109">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="23532-110">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="23532-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="23532-111">**Sil** öğesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23532-111">Click **Delete**.</span></span> <span data-ttu-id="23532-112">Bu adım, şirketlerarası planlama çalışmasını kısaltmak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="23532-112">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="23532-113">Şirketlerarası planlama, en düşük planlama serisinden başlayarak bir planlama grubu içindeki tüm şirketlerde master planlamayı çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="23532-113">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="23532-114">**Evet** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="23532-114">Click **Yes**.</span></span>
6. <span data-ttu-id="23532-115">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="23532-115">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="23532-116">Şirketlerarası plan oluşturma</span><span class="sxs-lookup"><span data-stu-id="23532-116">Create an intercompany plan</span></span>
1. <span data-ttu-id="23532-117">**Gezinti bölmesinde**, **Modüller > Master planlama > Çalışma alanları > Master planlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="23532-117">In the **Navigation pane**, go to **Modules > Master planning > Workspaces > Master planning**.</span></span>
2. <span data-ttu-id="23532-118">**Şirketlerarası master planlama**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23532-118">Click **Intercompany master planning**.</span></span>  
3. <span data-ttu-id="23532-119">**Şirketlerarası planlama grubu** alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23532-119">In the **Intercompany planning group** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="23532-120">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23532-120">In the list, click the link in the selected row.</span></span> <span data-ttu-id="23532-121">Şirketlerarası planlama grubu 10'u seçin.</span><span class="sxs-lookup"><span data-stu-id="23532-121">Select intercompany planning group 10.</span></span>  
5. <span data-ttu-id="23532-122">**Şirketlerarası planlama tekrar sayısı** alanına '2' yazın.</span><span class="sxs-lookup"><span data-stu-id="23532-122">In the **Number of intercompany planning iterations** field, enter '2'.</span></span> <span data-ttu-id="23532-123">Şirketlerarası planlama grubu 10 iki üyeye sahip.</span><span class="sxs-lookup"><span data-stu-id="23532-123">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="23532-124">Gecikmeleri kaynak şirketten (USMF) müşteri şirkete (DEMF) yaymak için, iki şirkette de şirketlerarası işlevini iki kez çalıştırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="23532-124">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="23532-125">İlk tekrar, talebi yayar ve kaynak şirketteki (USMF) gecikmeleri tanımlar.</span><span class="sxs-lookup"><span data-stu-id="23532-125">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="23532-126">İkinci tekrar, gecikmeleri USMF'den DEMF'ye yayar.</span><span class="sxs-lookup"><span data-stu-id="23532-126">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
6. <span data-ttu-id="23532-127">**İlk tekrarlama** alanında 'Yeniden oluşturma' seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="23532-127">In the **First iteration** field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="23532-128">**Sonraki tekrarlamalar** alanında 'Yeniden oluşturma' seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="23532-128">In the **Subsequent iterations** field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="23532-129">**İş parçacığı sayısı** alanına bir rakam girin.</span><span class="sxs-lookup"><span data-stu-id="23532-129">In the **Number of threads** field, enter a number.</span></span> <span data-ttu-id="23532-130">Bu, planlama için kullanılan paralel iş parçacıklarının sayısını temsil eder.</span><span class="sxs-lookup"><span data-stu-id="23532-130">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="23532-131">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23532-131">Click **OK**.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="23532-132">Planın sonucunu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="23532-132">View the result of the plan</span></span>
1. <span data-ttu-id="23532-133">**Plan** alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23532-133">In the **Plan** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="23532-134">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23532-134">In the list, click the link in the selected row.</span></span> <span data-ttu-id="23532-135">StaticPlan için bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23532-135">Click the link for StaticPlan.</span></span> <span data-ttu-id="23532-136">USMF şirketinde olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="23532-136">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="23532-137">**Planlı siparişler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23532-137">Click **Planned orders**.</span></span>

