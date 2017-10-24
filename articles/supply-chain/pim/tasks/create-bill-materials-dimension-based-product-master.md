--- 
title: "Boyut tabanlı ana ürün için ürün reçetesi oluşturma"
description: "Bu prosedür için bu sekiz kayıt sırasındaki, önceki 4 kılavuzu tamamlamış olmanız gerekir."
author: YuyuScheller
manager: AnnBe
ms.date: 06/21/2016
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
ms.openlocfilehash: 4f9f9473d0872d68571b87409b93e0cf5455364c
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="f5c9f-103">Boyut tabanlı ana ürün için ürün reçetesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="f5c9f-103">Create a bill of materials for a dimension-based product master</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f5c9f-104">Bu prosedür için bu sekiz kayıt sırasındaki, önceki 4 kılavuzu tamamlamış olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="f5c9f-105">İlk 4 kayıtta bu prosedürün tamamlanması için gereken verileri kurulur.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="f5c9f-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f5c9f-107">Bu görev tipik olarak ürün tasarımcısı tarafından ele alınır.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-107">This task is typically handled by the product designer.</span></span>


## <a name="select-the-product"></a><span data-ttu-id="f5c9f-108">Ürün seçme</span><span class="sxs-lookup"><span data-stu-id="f5c9f-108">Select the product</span></span>
1. <span data-ttu-id="f5c9f-109">Serbest bırakılan ürün bakımı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="f5c9f-110">Sevk edilen ürünler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-110">Click Released products.</span></span>
3. <span data-ttu-id="f5c9f-111">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="f5c9f-112">Bu sıradaki ilk görev kılavuzunda oluşturduğunuz, boyut tabanlı yapılandırma teknolojisiyle, serbest bırakılan ürün mastarını bulun.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-112">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
4. <span data-ttu-id="f5c9f-113">Eylem Bölmesinde, Mühendis öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-113">On the Action Pane, click Engineer.</span></span>
5. <span data-ttu-id="f5c9f-114">BOM sürümlerini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-114">Click BOM versions.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="f5c9f-115">Yeni BOM ve BOM sürümünü oluşturma</span><span class="sxs-lookup"><span data-stu-id="f5c9f-115">Create new BOM and BOM version</span></span>
1. <span data-ttu-id="f5c9f-116">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-116">Click New.</span></span>
2. <span data-ttu-id="f5c9f-117">BOM ve BOM sürümünü tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-117">Click BOM and BOM version.</span></span>
3. <span data-ttu-id="f5c9f-118">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="f5c9f-119">Bir saha ayarlanması</span><span class="sxs-lookup"><span data-stu-id="f5c9f-119">Setting a site</span></span>  
    * <span data-ttu-id="f5c9f-120">Bu prosedürde BOM için belirli bir saha ayarlamıyoruz.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-120">In this procedure we don't set a specific site for the BOM.</span></span>  
4. <span data-ttu-id="f5c9f-121">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-121">Click OK.</span></span>
5. <span data-ttu-id="f5c9f-122">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-122">Click New.</span></span>
    * <span data-ttu-id="f5c9f-123">Bu prosedürde BOM'a dört satır ekleyeceğiz.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-123">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="f5c9f-124">İki satır, kablo seçeneklerini temsil ederken; iki satır, dolap seçeneklerini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-124">Two lines represent cable options and two lines represent cabinet options.</span></span>  
6. <span data-ttu-id="f5c9f-125">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-125">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="f5c9f-126">Madde numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-126">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="f5c9f-127">A0001, HDMI 6' Kablo madde numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-127">Select item number A0001, HDMI 6' Cables.</span></span>  
8. <span data-ttu-id="f5c9f-128">Yapılandırma grubu alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-128">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="f5c9f-129">Bu sıradaki kılavuz 4'te oluşturulan Kablo yapılandırma grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-129">Select the Cable configuration group created in guide 4 in this sequence.</span></span>  
9. <span data-ttu-id="f5c9f-130">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-130">Click New.</span></span>
    * <span data-ttu-id="f5c9f-131">A0002, HDMI 12' Kablo madde numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-131">Select item number A0002, HDMI 12' Cables.</span></span>  
10. <span data-ttu-id="f5c9f-132">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-132">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="f5c9f-133">Madde numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-133">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="f5c9f-134">Yapılandırma grubu alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-134">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="f5c9f-135">Kablo yapılandırma grubunu tekrar seçin.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-135">Select the Cable configuration group again.</span></span>  
13. <span data-ttu-id="f5c9f-136">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-136">Click New.</span></span>
14. <span data-ttu-id="f5c9f-137">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-137">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="f5c9f-138">Madde numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-138">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="f5c9f-139">D0002 Dolap madde numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-139">Select item number D0002 Cabinet.</span></span>  
16. <span data-ttu-id="f5c9f-140">Yapılandırma grubu alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-140">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="f5c9f-141">Bu BOM satırı için Dolap yapılandırma grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-141">Select the Cabinet configuration group for this BOM line.</span></span>  
17. <span data-ttu-id="f5c9f-142">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-142">Click New.</span></span>
18. <span data-ttu-id="f5c9f-143">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-143">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="f5c9f-144">Madde numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-144">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="f5c9f-145">Son BOM satırı olarak, M0007 Standart Dolap madde numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-145">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
20. <span data-ttu-id="f5c9f-146">Yapılandırma grubu alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-146">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="f5c9f-147">Son BOM satırı için Dolap yapılandırma grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-147">Select the Cabinet configuration group for the laste BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="f5c9f-148">Onayla ve etkinleştir</span><span class="sxs-lookup"><span data-stu-id="f5c9f-148">Approve and activate</span></span>
1. <span data-ttu-id="f5c9f-149">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-149">Close the page.</span></span>
2. <span data-ttu-id="f5c9f-150">Onayla’yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-150">Click Approve.</span></span>
3. <span data-ttu-id="f5c9f-151">Onaylayan alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-151">In the Approved by field, enter or select a value.</span></span>
4. <span data-ttu-id="f5c9f-152">Ürün reçetesini de onaylamak ister misiniz? sorusunu Evet olarak yanıtlayın. alanda kullandığınızda otomatik olarak işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-152">Select Yes in the Do you also want to approve the bill of materials? field.</span></span>
5. <span data-ttu-id="f5c9f-153">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-153">Click OK.</span></span>
6. <span data-ttu-id="f5c9f-154">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f5c9f-154">Click Activate.</span></span>


