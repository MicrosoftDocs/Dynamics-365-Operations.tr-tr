--- 
title: "Yalın imalat için işlem faaliyetleri oluşturma"
description: "Yalın imalat için bir işlem faaliyeti oluşturun."
author: cvocph
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c1e7cb939c9b936a58486de13f73150aebccb548
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---
# <a name="create-process-activities-for-lean-manufacturing"></a><span data-ttu-id="cc1e4-103">Yalın imalat için işlem faaliyetleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="cc1e4-103">Create process activities for lean manufacturing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cc1e4-104">Yalın imalat için bir işlem faaliyeti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-104">Create a process activity for lean manufacturing.</span></span> 

<span data-ttu-id="cc1e4-105">Ön koşullar:</span><span class="sxs-lookup"><span data-stu-id="cc1e4-105">Prerequisites:</span></span> 

1. <span data-ttu-id="cc1e4-106">Bir üretim akışı ve etkin olmayan sürüm oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="cc1e4-107">Bir iş hücresi oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-107">A work cell must be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="cc1e4-108">Üretim akışı sürümünü bul</span><span class="sxs-lookup"><span data-stu-id="cc1e4-108">Find the production flow version</span></span>
1. <span data-ttu-id="cc1e4-109">Üretim kontrolü > Kurulum > Yalın üretim akışı > Üretim akışları seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="cc1e4-110">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="cc1e4-111">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-111">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="cc1e4-112">Yeni bir faaliyet oluştur</span><span class="sxs-lookup"><span data-stu-id="cc1e4-112">Create a new activity</span></span>
1. <span data-ttu-id="cc1e4-113">Faaliyetler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-113">Click Activities.</span></span>
    * <span data-ttu-id="cc1e4-114">Seçili üretim akışında taslak halde bir sürüm olduğundan emin olun ve o sürümü seçin.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-114">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="cc1e4-115">Yeni plan faaliyeti oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-115">Click Create new plan activity.</span></span>
3. <span data-ttu-id="cc1e4-116">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-116">Click Next.</span></span>
4. <span data-ttu-id="cc1e4-117">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="cc1e4-118">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="cc1e4-119">Adın, tüm sürümlerde, sağlanan üretim akışına özgü olması gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-119">Note that the name must be unique for a given production flow for all versions.</span></span>  
6. <span data-ttu-id="cc1e4-120">İşlem miktarı alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-120">In the Process quantity field, enter a number.</span></span>
    * <span data-ttu-id="cc1e4-121">Bunun, işçilik miktarını hesaplamak için, ne miktarda iş işleme alınacağına bakılmaksızın iş başına minimum miktar olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-121">Note that no matter what job quantity will be processed, this is the minimum quantity per job to calculate the labor cost.</span></span> <span data-ttu-id="cc1e4-122">İş miktarları bu miktardan saparsa, işçilik maliyeti farkı ortaya çıkar.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-122">If job quantities deviate from this quantity, labor cost variance will be created.</span></span>  
7. <span data-ttu-id="cc1e4-123">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-123">Click Next.</span></span>

## <a name="select-the-work-cell"></a><span data-ttu-id="cc1e4-124">İş hücresini seç</span><span class="sxs-lookup"><span data-stu-id="cc1e4-124">Select the work cell</span></span>
1. <span data-ttu-id="cc1e4-125">İş hücresi alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-125">In the Work cell field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="cc1e4-126">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-126">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="cc1e4-127">Stok güncelleştirmelerini tanımla</span><span class="sxs-lookup"><span data-stu-id="cc1e4-127">Define the inventory updates</span></span>
1. <span data-ttu-id="cc1e4-128">Eldeki girişi güncelleştir onay kutusunu işaretleyin veya işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-128">Select or clear the Update on hand receipt check box.</span></span>
    * <span data-ttu-id="cc1e4-129">Eldekini Güncelleştir = Hayır ise, faaliyeti yarı bitmiş bir ürünü alacak şekilde tanımlayabilirsiniz (faaliyet bir sonraki ürün reçetesi düzeyine ulaşmaz).</span><span class="sxs-lookup"><span data-stu-id="cc1e4-129">If Update On hand = No, you can define the activity to receive a semi-finished product (the activity does not reach the next BOM level).</span></span>    <span data-ttu-id="cc1e4-130">Yarı bitmiş ürünleri tüketmek için de seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-130">You can also select to consume semi-finished products.</span></span>  

## <a name="define-the-picking-activities"></a><span data-ttu-id="cc1e4-131">Malzeme çekme faaliyetlerini tanımla</span><span class="sxs-lookup"><span data-stu-id="cc1e4-131">Define the picking activities</span></span>
1. <span data-ttu-id="cc1e4-132">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-132">Click Next.</span></span>
2. <span data-ttu-id="cc1e4-133">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-133">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="cc1e4-134">Seçili iş hücresinin giriş konumu için varsayılan bir malzeme çekme faaliyeti oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-134">A default picking activity is created for the input location of the selected work cell.</span></span>  
3. <span data-ttu-id="cc1e4-135">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-135">Click Add.</span></span>
    * <span data-ttu-id="cc1e4-136">İş hücresi giriş faaliyeti aşamasında olmayan belirli ürünler için ek malzeme çekme faaliyetleri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-136">You can create additional picking activities for specific products, that are not staged at the work cell input activity.</span></span>  
4. <span data-ttu-id="cc1e4-137">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="cc1e4-138">Madde numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-138">In the Item number field, type a value.</span></span>
6. <span data-ttu-id="cc1e4-139">Ambar alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-139">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="cc1e4-140">Bu tanım ile, faaliyette tüketilen tüm malzemeler (ikinci malzeme çekme faaliyetinde tanımlanan ürün dışında) varsayılan giriş ambarından ve konumundan çekilir.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-140">With this definition, all materials consumed in the activity are picked from the default input warehouse and location except the item that is defined in the second picking activity.</span></span> <span data-ttu-id="cc1e4-141">Bu ürün farklı bir ambar ve konumdan çekilir.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-141">This item will be picked from a different warehouse and location.</span></span>  
7. <span data-ttu-id="cc1e4-142">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-142">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="cc1e4-143">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-143">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="cc1e4-144">Hurda kaydet onay kutusunu işaretleyin veya işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-144">Select or clear the Register scrap check box.</span></span>
10. <span data-ttu-id="cc1e4-145">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-145">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="cc1e4-146">Faaliyet sürelerini tanımla</span><span class="sxs-lookup"><span data-stu-id="cc1e4-146">Define the activity times</span></span>
1. <span data-ttu-id="cc1e4-147">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-147">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="cc1e4-148">Çalışma zamanı tanımı gereklidir.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-148">The definition of a Runtime is required.</span></span> <span data-ttu-id="cc1e4-149">Çalışma zamanı, kanban işlerinin maliyetlerini ve iş çıkarma yeteneği sürelerini hesaplamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-149">The Runtime is used to calculate costs and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="cc1e4-150">Çalışma zamanları kapasite yükü ve tüketimi hesaplamak için kullanılmaz, bu, üretim akışı sürümü görevinden türetilmiş döngü süresiyle hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-150">Runtimes are not used to calculate capacity load and consumption, this is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="cc1e4-151">Zaman alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-151">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="cc1e4-152">Birim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-152">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="cc1e4-153">Zaman birimini seçin.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-153">Select the Time unit.</span></span>
5. <span data-ttu-id="cc1e4-154">Miktar başına alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-154">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="cc1e4-155">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-155">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="cc1e4-156">Kuyruk süreleri isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-156">Queue times are optional.</span></span>  
7. <span data-ttu-id="cc1e4-157">Zaman alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-157">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="cc1e4-158">Birim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-158">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="cc1e4-159">Zaman birimini seçin.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-159">Select the Time unit.</span></span>
10. <span data-ttu-id="cc1e4-160">Miktar başına alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-160">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="cc1e4-161">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-161">Click Next.</span></span>
12. <span data-ttu-id="cc1e4-162">Son düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-162">Click Finish.</span></span>
13. <span data-ttu-id="cc1e4-163">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="cc1e4-163">Close the page.</span></span>


