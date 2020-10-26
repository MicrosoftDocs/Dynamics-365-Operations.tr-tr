---
title: Yalın imalat için işlem faaliyetleri oluşturma
description: Yalın imalat için bir işlem faaliyeti oluşturun.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup, PlanActivityDetails, KanbanJobPickingListPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3cb096eb25fa449b521c370bcb1677e38e399658
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983410"
---
# <a name="create-process-activities-for-lean-manufacturing"></a><span data-ttu-id="d840e-103">Yalın imalat için işlem faaliyetleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="d840e-103">Create process activities for lean manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d840e-104">Yalın imalat için bir işlem faaliyeti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d840e-104">Create a process activity for lean manufacturing.</span></span> 

<span data-ttu-id="d840e-105">Ön koşullar:</span><span class="sxs-lookup"><span data-stu-id="d840e-105">Prerequisites:</span></span> 

1. <span data-ttu-id="d840e-106">Bir üretim akışı ve etkin olmayan sürüm oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d840e-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="d840e-107">Bir iş hücresi oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d840e-107">A work cell must be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="d840e-108">Üretim akışı sürümünü bul</span><span class="sxs-lookup"><span data-stu-id="d840e-108">Find the production flow version</span></span>
1. <span data-ttu-id="d840e-109">Üretim kontrolü > Kurulum > Yalın üretim akışı > Üretim akışları seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="d840e-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="d840e-110">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="d840e-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d840e-111">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d840e-111">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="d840e-112">Yeni bir faaliyet oluştur</span><span class="sxs-lookup"><span data-stu-id="d840e-112">Create a new activity</span></span>
1. <span data-ttu-id="d840e-113">Faaliyetler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d840e-113">Click Activities.</span></span>
    * <span data-ttu-id="d840e-114">Seçili üretim akışında taslak halde bir sürüm olduğundan emin olun ve o sürümü seçin.</span><span class="sxs-lookup"><span data-stu-id="d840e-114">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="d840e-115">Yeni plan faaliyeti oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d840e-115">Click Create new plan activity.</span></span>
3. <span data-ttu-id="d840e-116">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d840e-116">Click Next.</span></span>
4. <span data-ttu-id="d840e-117">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="d840e-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="d840e-118">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="d840e-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="d840e-119">Adın, tüm sürümlerde, sağlanan üretim akışına özgü olması gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="d840e-119">Note that the name must be unique for a given production flow for all versions.</span></span>  
6. <span data-ttu-id="d840e-120">İşlem miktarı alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="d840e-120">In the Process quantity field, enter a number.</span></span>
    * <span data-ttu-id="d840e-121">Bunun, işçilik miktarını hesaplamak için, ne miktarda iş işleme alınacağına bakılmaksızın iş başına minimum miktar olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="d840e-121">Note that no matter what job quantity will be processed, this is the minimum quantity per job to calculate the labor cost.</span></span> <span data-ttu-id="d840e-122">İş miktarları bu miktardan saparsa, işçilik maliyeti farkı ortaya çıkar.</span><span class="sxs-lookup"><span data-stu-id="d840e-122">If job quantities deviate from this quantity, labor cost variance will be created.</span></span>  
7. <span data-ttu-id="d840e-123">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d840e-123">Click Next.</span></span>

## <a name="select-the-work-cell"></a><span data-ttu-id="d840e-124">İş hücresini seç</span><span class="sxs-lookup"><span data-stu-id="d840e-124">Select the work cell</span></span>
1. <span data-ttu-id="d840e-125">İş hücresi alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="d840e-125">In the Work cell field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="d840e-126">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d840e-126">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="d840e-127">Stok güncelleştirmelerini tanımla</span><span class="sxs-lookup"><span data-stu-id="d840e-127">Define the inventory updates</span></span>
1. <span data-ttu-id="d840e-128">Eldeki girişi güncelleştir onay kutusunu işaretleyin veya işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="d840e-128">Select or clear the Update on hand receipt check box.</span></span>
    * <span data-ttu-id="d840e-129">Eldekini Güncelleştir = Hayır ise, faaliyeti yarı bitmiş bir ürünü alacak şekilde tanımlayabilirsiniz (faaliyet bir sonraki ürün reçetesi düzeyine ulaşmaz).</span><span class="sxs-lookup"><span data-stu-id="d840e-129">If Update On hand = No, you can define the activity to receive a semi-finished product (the activity does not reach the next BOM level).</span></span>    <span data-ttu-id="d840e-130">Yarı bitmiş ürünleri tüketmek için de seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d840e-130">You can also select to consume semi-finished products.</span></span>  

## <a name="define-the-picking-activities"></a><span data-ttu-id="d840e-131">Malzeme çekme faaliyetlerini tanımla</span><span class="sxs-lookup"><span data-stu-id="d840e-131">Define the picking activities</span></span>
1. <span data-ttu-id="d840e-132">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d840e-132">Click Next.</span></span>
2. <span data-ttu-id="d840e-133">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="d840e-133">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="d840e-134">Seçili iş hücresinin giriş konumu için varsayılan bir malzeme çekme faaliyeti oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d840e-134">A default picking activity is created for the input location of the selected work cell.</span></span>  
3. <span data-ttu-id="d840e-135">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d840e-135">Click Add.</span></span>
    * <span data-ttu-id="d840e-136">İş hücresi giriş faaliyeti aşamasında olmayan belirli ürünler için ek malzeme çekme faaliyetleri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d840e-136">You can create additional picking activities for specific products, that are not staged at the work cell input activity.</span></span>  
4. <span data-ttu-id="d840e-137">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="d840e-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="d840e-138">Madde numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="d840e-138">In the Item number field, type a value.</span></span>
6. <span data-ttu-id="d840e-139">Ambar alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="d840e-139">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d840e-140">Bu tanım ile, faaliyette tüketilen tüm malzemeler (ikinci malzeme çekme faaliyetinde tanımlanan ürün dışında) varsayılan giriş ambarından ve konumundan çekilir.</span><span class="sxs-lookup"><span data-stu-id="d840e-140">With this definition, all materials consumed in the activity are picked from the default input warehouse and location except the item that is defined in the second picking activity.</span></span> <span data-ttu-id="d840e-141">Bu ürün farklı bir ambar ve konumdan çekilir.</span><span class="sxs-lookup"><span data-stu-id="d840e-141">This item will be picked from a different warehouse and location.</span></span>  
7. <span data-ttu-id="d840e-142">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="d840e-142">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="d840e-143">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d840e-143">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="d840e-144">Hurda kaydet onay kutusunu işaretleyin veya işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="d840e-144">Select or clear the Register scrap check box.</span></span>
10. <span data-ttu-id="d840e-145">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d840e-145">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="d840e-146">Faaliyet sürelerini tanımla</span><span class="sxs-lookup"><span data-stu-id="d840e-146">Define the activity times</span></span>
1. <span data-ttu-id="d840e-147">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="d840e-147">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d840e-148">Çalışma zamanı tanımı gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d840e-148">The definition of a Runtime is required.</span></span> <span data-ttu-id="d840e-149">Çalışma zamanı, kanban işlerinin maliyetlerini ve iş çıkarma yeteneği sürelerini hesaplamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d840e-149">The Runtime is used to calculate costs and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="d840e-150">Çalışma zamanları kapasite yükü ve tüketimi hesaplamak için kullanılmaz, bu, üretim akışı sürümü görevinden türetilmiş döngü süresiyle hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="d840e-150">Runtimes are not used to calculate capacity load and consumption, this is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="d840e-151">Zaman alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="d840e-151">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="d840e-152">Birim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="d840e-152">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="d840e-153">Zaman birimini seçin.</span><span class="sxs-lookup"><span data-stu-id="d840e-153">Select the Time unit.</span></span>
5. <span data-ttu-id="d840e-154">Miktar başına alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="d840e-154">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="d840e-155">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="d840e-155">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d840e-156">Kuyruk süreleri isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="d840e-156">Queue times are optional.</span></span>  
7. <span data-ttu-id="d840e-157">Zaman alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="d840e-157">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="d840e-158">Birim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="d840e-158">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="d840e-159">Zaman birimini seçin.</span><span class="sxs-lookup"><span data-stu-id="d840e-159">Select the Time unit.</span></span>
10. <span data-ttu-id="d840e-160">Miktar başına alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="d840e-160">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="d840e-161">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d840e-161">Click Next.</span></span>
12. <span data-ttu-id="d840e-162">Son düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d840e-162">Click Finish.</span></span>
13. <span data-ttu-id="d840e-163">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="d840e-163">Close the page.</span></span>

