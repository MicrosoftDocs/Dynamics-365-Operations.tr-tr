---
title: Yalın imalat için alt sözleşmeli iş hücresi oluşturma
description: Yalın imalat için taşeron işi modellemek için işi sağlayan satıcı ile ilişkilendirilmiş bir iş hücresi oluşturmanız gerekir.
author: cvocph
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 58b725af456f1a5c7f158f01ffe48a2d8cdf056b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "319167"
---
# <a name="create-a-subcontracted-work-cell-for-lean-manufacturing"></a><span data-ttu-id="5dc4b-103">Yalın imalat için alt sözleşmeli iş hücresi oluşturma</span><span class="sxs-lookup"><span data-stu-id="5dc4b-103">Create a subcontracted work cell for lean manufacturing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5dc4b-104">Yalın imalat için taşeron işi modellemek için işi sağlayan satıcı ile ilişkilendirilmiş bir iş hücresi oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-104">To model subcontracted work for lean manufacturing, you must create a work cell that is associated with the vendor that provides the work.</span></span> <span data-ttu-id="5dc4b-105">Taşeron iş hücresi satıcıya Satıcı türündeki bir kaynağın ilişkilendirilmesi aracılığıyla atanmıştır.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-105">A subcontracted work cell is linked to the vendor through the association of a resource of the Vendor type.</span></span> <span data-ttu-id="5dc4b-106">Bu kaydın USMF demo şirketinde yürütürseniz, satıcı hesap kodu 1002 ve tesis 1'i seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-106">If you play this recording in the USMF demo company, you can select vendor account ID 1002 and site 1.</span></span>


## <a name="create-a-vendor-resource"></a><span data-ttu-id="5dc4b-107">Bir satıcı kaynağı oluştur</span><span class="sxs-lookup"><span data-stu-id="5dc4b-107">Create a vendor resource</span></span>
1. <span data-ttu-id="5dc4b-108">Kaynaklar'a gidin.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-108">Go to Resources.</span></span>
2. <span data-ttu-id="5dc4b-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-109">Click New.</span></span>
3. <span data-ttu-id="5dc4b-110">Kaynak alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-110">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="5dc4b-111">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="5dc4b-112">Tür alanında 'Satıcı' seçin.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-112">In the Type field, select 'Vendor'.</span></span>
6. <span data-ttu-id="5dc4b-113">Satıcı alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-113">In the Vendor field, click the drop-down button to open the lookup.</span></span>

## <a name="create-the-resource-group"></a><span data-ttu-id="5dc4b-114">Bir kaynak grubu oluştur</span><span class="sxs-lookup"><span data-stu-id="5dc4b-114">Create the resource group</span></span>
1. <span data-ttu-id="5dc4b-115">Kaynak grupları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-115">Go to Resource groups.</span></span>
2. <span data-ttu-id="5dc4b-116">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-116">Click New.</span></span>
3. <span data-ttu-id="5dc4b-117">Kaynak grubu alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-117">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="5dc4b-118">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-118">In the Description field, type a value.</span></span>
5. <span data-ttu-id="5dc4b-119">Tesis alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-119">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="5dc4b-120">İş hücrelerinin tahsis edileceği tesisi seçin.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-120">Select the site that the work cell should be allocated to.</span></span> <span data-ttu-id="5dc4b-121">Bir tesis teorik olarak bir satıcı tarafından çalıştırılan tek bir tesisi temsil edebilir.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-121">In theory, a site can represent a single site that is operated by a vendor.</span></span> <span data-ttu-id="5dc4b-122">Ancak pek çok durumda taşeron kaynaklar, taşeron verilen işlerin siparişinin verildiği tesise tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-122">However, in most cases, subcontracted resources are just allocated to the site that orders the subcontracted work.</span></span> <span data-ttu-id="5dc4b-123">Taşeron iş hücrelerinin giren ve çıkan ambarlarının aynı tesiste olması gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-123">Note that the input and output warehouses of subcontracted work cells must be on the same site.</span></span>  
6. <span data-ttu-id="5dc4b-124">Tesis alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-124">In the Site field, type a value.</span></span>
7. <span data-ttu-id="5dc4b-125">@SysTaskRecorder:_RequestClose</span><span class="sxs-lookup"><span data-stu-id="5dc4b-125">@SysTaskRecorder:_RequestClose</span></span>
8. <span data-ttu-id="5dc4b-126">İş hücresi onay kutusunu seçin veya temizleyin.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-126">Select or clear the Work cell check box.</span></span>
9. <span data-ttu-id="5dc4b-127">Giriş ambarı alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-127">In the Input warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="5dc4b-128">Satıcı tarafından yönetilen iş hücresi için malzemeyi hazırlamak amacıyla kullanılan ambar ve konumu seçin.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-128">Select the warehouse and location that are used to stage the material for the vendor-managed work cell.</span></span> <span data-ttu-id="5dc4b-129">Pek çok durumda ambar ve konum, satıcı başına ayrı bir ambar ve iş hücresi başına bir konum kullanılarak modellenir.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-129">In many cases, the warehouse and location are modeled by using a separate warehouse per vendor and one location per work cell.</span></span>  
10. <span data-ttu-id="5dc4b-130">Giriş yerleşimi alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-130">In the Input location field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="5dc4b-131">Çıkış ambarı alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-131">In the Output warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="5dc4b-132">İş hücresinin taşeron işlemleri gönderildiğinde malzemenin gönderildiği ambarı ve konumu tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-132">Define the warehouse and location where the material is posted when the subcontracted activities of the work cell are posted.</span></span> <span data-ttu-id="5dc4b-133">Satıcı kanban işlerini raporluyorsa, ambar ve konum satıcının tesisinde olabilir.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-133">The warehouse and location can be at the vendor site if the vendor reports the kanban jobs.</span></span> <span data-ttu-id="5dc4b-134">Alternatif olarak, ambar konum üretim akışının bir sonraki adımıyla ilişkilendirilmiş alma konumu olabilir.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-134">Alternatively, the warehouse and location can be the receiving location that is associated with the next step of the production flow.</span></span>  
12. <span data-ttu-id="5dc4b-135">Çıkış yerleşimi alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-135">In the Output location field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="5dc4b-136">Takvimler bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-136">Expand or collapse the Calendars section.</span></span>
14. <span data-ttu-id="5dc4b-137">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-137">Click Add.</span></span>
15. <span data-ttu-id="5dc4b-138">Takvim alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-138">In the Calendar field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="5dc4b-139">İş hücresinin çalışma zamanı takvimini kaynak grubu ile ilişkilendirin.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-139">Associate the working time calendar of the work cell with the resource group.</span></span> <span data-ttu-id="5dc4b-140">Kritik kaynaklar için, iş hücresi veya satıcı tesisinin tam çalışma zamanlarını ve ilişkili kapasitelerini temsil eden belirli takvimler tanımlamanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-140">For critical resources, we recommend that you define specific calendars that represent the exact working times and related capacities of the work cell or vendor site.</span></span>  
16. <span data-ttu-id="5dc4b-141">Kaynaklar bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-141">Expand or collapse the Resources section.</span></span>
17. <span data-ttu-id="5dc4b-142">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-142">Click Add.</span></span>
    * <span data-ttu-id="5dc4b-143">Bir taşeron kaynak grubu, kaynak grubunu satıcı hesabına bağlayan Satıcı türünde bir ilişkilendirilmiş kaynağa sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-143">A subcontracted resource group must have an associated resource of the Vendor type that links the resource group to the vendor account.</span></span>  
18. <span data-ttu-id="5dc4b-144">Kaynak alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-144">In the Resource field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="5dc4b-145">Önceki alt görevde oluşturmuş olduğunuz satıcı kaynağını seçin veya girin.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-145">Select or enter the vendor resource that you created in the previous sub-task.</span></span>  
19. <span data-ttu-id="5dc4b-146">İş hücresi kapasitesi bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-146">Expand or collapse the Work cell capacity section.</span></span>
20. <span data-ttu-id="5dc4b-147">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-147">Click Add.</span></span>
    * <span data-ttu-id="5dc4b-148">Bir iş hücresi tanımlanmış bir kapasiteye sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-148">A work cell must have a defined capacity.</span></span> <span data-ttu-id="5dc4b-149">Bu örnekte, standart bir iş günü için 100 parçalık çıkış kapasitesi oluştururuz.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-149">In this example, we create a throughput capacity of 100 pieces per standard workday.</span></span>  
21. <span data-ttu-id="5dc4b-150">Üretim akışı modeli alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-150">In the Production flow model field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="5dc4b-151">Kapasite dönemi alanında bir seçenek belirtin.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-151">In the Capacity period field, select an option.</span></span>
23. <span data-ttu-id="5dc4b-152">Ortalama iş çıkarma yeteneği miktarı alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-152">In the Average throughput quantity field, enter a number.</span></span>
24. <span data-ttu-id="5dc4b-153">Birim alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-153">In the Unit field, click the drop-down button to open the lookup.</span></span>
25. <span data-ttu-id="5dc4b-154">Birimi ResolveChanges.</span><span class="sxs-lookup"><span data-stu-id="5dc4b-154">ResolveChanges the Unit.</span></span>

