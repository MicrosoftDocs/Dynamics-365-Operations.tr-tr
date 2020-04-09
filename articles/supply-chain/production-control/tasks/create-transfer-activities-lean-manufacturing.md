---
title: Yalın imalat için transfer faaliyetleri oluşturma
description: Yalın imalat için bir transfer faaliyeti oluşturun.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c80283162f0d2d000dfd7d023c3de188511865ba
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149274"
---
# <a name="create-transfer-activities-for-lean-manufacturing"></a><span data-ttu-id="e62a9-103">Yalın imalat için transfer faaliyetleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="e62a9-103">Create transfer activities for lean manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e62a9-104">Yalın imalat için bir transfer faaliyeti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e62a9-104">Create a transfer activity for lean manufacturing.</span></span> 

<span data-ttu-id="e62a9-105">Ön koşullar:</span><span class="sxs-lookup"><span data-stu-id="e62a9-105">Prerequisites:</span></span> 

1. <span data-ttu-id="e62a9-106">Bir üretim akışı ve etkin olmayan sürüm oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e62a9-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="e62a9-107">Başlangıç ve bitiş ambarı ve konumları oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e62a9-107">The from and to warehouse and locations must be created.</span></span> <span data-ttu-id="e62a9-108">İsteğe bağlı olarak, yenileme veya yenilenen iş hücresi oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e62a9-108">Optionally, the replenishing or the replenished work cell should be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="e62a9-109">Üretim akışı sürümünü bul</span><span class="sxs-lookup"><span data-stu-id="e62a9-109">Find the production flow version</span></span>
1. <span data-ttu-id="e62a9-110">Üretim kontrolü > Kurulum > Yalın üretim akışı > Üretim akışları seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="e62a9-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="e62a9-111">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="e62a9-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e62a9-112">Üretim akışı sürümünün taslak durumda olması gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="e62a9-112">Note that the production flow must have a version in draft status.</span></span>  
3. <span data-ttu-id="e62a9-113">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e62a9-113">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="e62a9-114">Yeni bir faaliyet oluştur</span><span class="sxs-lookup"><span data-stu-id="e62a9-114">Create a new activity</span></span>
1. <span data-ttu-id="e62a9-115">Faaliyetler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e62a9-115">Click Activities.</span></span>
    * <span data-ttu-id="e62a9-116">Seçili üretim akışında taslak halde bir sürüm olduğundan emin olun ve o sürümü seçin.</span><span class="sxs-lookup"><span data-stu-id="e62a9-116">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="e62a9-117">Yeni plan faaliyeti oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e62a9-117">Click Create new plan activity.</span></span>
3. <span data-ttu-id="e62a9-118">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e62a9-118">Click Next.</span></span>
4. <span data-ttu-id="e62a9-119">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="e62a9-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="e62a9-120">Faaliyet türü alanında, 'Transfer' seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="e62a9-120">In the Activity type field, select 'Transfer'.</span></span>
6. <span data-ttu-id="e62a9-121">İşlem miktarı alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="e62a9-121">In the Process quantity field, enter a number.</span></span>
7. <span data-ttu-id="e62a9-122">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e62a9-122">Click Next.</span></span>

## <a name="select-the-work-cells"></a><span data-ttu-id="e62a9-123">İş hücrelerini seç</span><span class="sxs-lookup"><span data-stu-id="e62a9-123">Select the Work cells</span></span>
1. <span data-ttu-id="e62a9-124">Yenileme alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e62a9-124">In the Replenishing field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="e62a9-125">İş hücresi çıkış konumunu transfer faaliyetindeki çıkış konumu olarak kullanmak için bir iş hücresi seçin.</span><span class="sxs-lookup"><span data-stu-id="e62a9-125">To use the work cell output location as the from location in the transfer activity, select a work cell.</span></span> <span data-ttu-id="e62a9-126">Aynı işlem transfer faaliyetinin hedef konumunu ayarlayan yenilenen iş hücresi için de yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="e62a9-126">The same can be done with the replenished work cell, which sets the target location of the transfer activity.</span></span>  
2. <span data-ttu-id="e62a9-127">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e62a9-127">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="e62a9-128">Stok güncelleştirmelerini tanımla</span><span class="sxs-lookup"><span data-stu-id="e62a9-128">Define the inventory updates</span></span>
1. <span data-ttu-id="e62a9-129">Ürün türü alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="e62a9-129">In the Product type field, select an option.</span></span>
    * <span data-ttu-id="e62a9-130">Yapılan bir transferin ürünün türünü değiştirmeyeceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="e62a9-130">Note that a transfer does not change the type of product.</span></span> <span data-ttu-id="e62a9-131">Bitmiş ürünlerin veya yarı bitmiş ürünlerin transferini gerçekleştirebilirsiniz (bir üretim akışı ve olası bir kanban akışı iki faaliyet arasındaki transfer).</span><span class="sxs-lookup"><span data-stu-id="e62a9-131">You can transfer finished products or semi-finished products (transfer between two activities of a production flow and possibly a kanban flow).</span></span>     <span data-ttu-id="e62a9-132">Bitmiş ürünlerin transferi yapılırken, malzeme çekilmesi veya alınması sonuçlarını bir stok hareketinde görmeyi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e62a9-132">When transferring finished products, you can select if picking or receiving results in an inventory transaction.</span></span>  

## <a name="define-the-transfer-locations"></a><span data-ttu-id="e62a9-133">Transfer konumlarını tanımla</span><span class="sxs-lookup"><span data-stu-id="e62a9-133">Define the transfer locations</span></span>
1. <span data-ttu-id="e62a9-134">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e62a9-134">Click Next.</span></span>
2. <span data-ttu-id="e62a9-135">Ambar alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="e62a9-135">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="e62a9-136">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="e62a9-136">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="e62a9-137">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e62a9-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="e62a9-138">Yerleşim alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="e62a9-138">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="e62a9-139">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e62a9-139">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="e62a9-140">Navlun sorumlusu alanında 'Sevkiyatçı' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e62a9-140">In the Freighted by field, select 'Shipper'.</span></span>
    * <span data-ttu-id="e62a9-141">Seçenekler şunlardır: Sevkiyatçı - sevk ambarını işleten şirket, Alıcı - alım ambarını işleten şirket, Taşıyıcı - üçüncü taraf sağlayıcı.</span><span class="sxs-lookup"><span data-stu-id="e62a9-141">Options include: Shipper - the organization operating the shipping warehouse, Recipient -  the organization operating the receiving warehouse, Carrier - a third party vendor.</span></span> <span data-ttu-id="e62a9-142">Faaliyet gösteren şirket bir satıcıysa, transfer faaliyeti için bir alt sözleşme gerekir.</span><span class="sxs-lookup"><span data-stu-id="e62a9-142">If the operating organization is a vendor, the transfer activity requires a subcontracting agreement.</span></span>  
8. <span data-ttu-id="e62a9-143">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e62a9-143">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="e62a9-144">Faaliyet sürelerini tanımla</span><span class="sxs-lookup"><span data-stu-id="e62a9-144">Define the activity times</span></span>
1. <span data-ttu-id="e62a9-145">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="e62a9-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e62a9-146">Çalışma zamanı tanımı gereklidir.</span><span class="sxs-lookup"><span data-stu-id="e62a9-146">The definition of a Runtime is required.</span></span> <span data-ttu-id="e62a9-147">Çalışma zamanı, kanban işlerinin maliyetini ve iş çıkarma yeteneği sürelerini hesaplamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e62a9-147">The Runtime is used to calculate cost and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="e62a9-148">Çalışma zamanları kapasite yükü ve tüketimi hesaplamak için kullanılmaz, üretim akışı sürümü görevinden türetilmiş döngü süresiyle hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="e62a9-148">Runtimes are not used to calculate capacity load and consumption, which is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="e62a9-149">Zaman alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="e62a9-149">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="e62a9-150">Birim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="e62a9-150">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="e62a9-151">Zaman birimini seçin.</span><span class="sxs-lookup"><span data-stu-id="e62a9-151">Select the Time unit.</span></span>
5. <span data-ttu-id="e62a9-152">Miktar başına alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="e62a9-152">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="e62a9-153">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="e62a9-153">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e62a9-154">Kuyruk süreleri isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e62a9-154">Queue times are optional.</span></span>  
7. <span data-ttu-id="e62a9-155">Zaman alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="e62a9-155">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="e62a9-156">Birim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="e62a9-156">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="e62a9-157">Zaman birimini seçin.</span><span class="sxs-lookup"><span data-stu-id="e62a9-157">Select the Time unit.</span></span>
10. <span data-ttu-id="e62a9-158">Miktar başına alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="e62a9-158">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="e62a9-159">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e62a9-159">Click Next.</span></span>
12. <span data-ttu-id="e62a9-160">Son düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e62a9-160">Click Finish.</span></span>
13. <span data-ttu-id="e62a9-161">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e62a9-161">Close the page.</span></span>

