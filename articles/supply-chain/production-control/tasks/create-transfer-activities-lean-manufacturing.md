---
title: Yalın imalat için transfer faaliyetleri oluşturma
description: Yalın imalat için bir transfer faaliyeti oluşturun.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5e3c92c5fc9cdba7c77942fae5c32d625cc939f1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237930"
---
# <a name="create-transfer-activities-for-lean-manufacturing"></a><span data-ttu-id="e1733-103">Yalın imalat için transfer faaliyetleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="e1733-103">Create transfer activities for lean manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e1733-104">Yalın imalat için bir transfer faaliyeti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e1733-104">Create a transfer activity for lean manufacturing.</span></span> 

<span data-ttu-id="e1733-105">Ön koşullar:</span><span class="sxs-lookup"><span data-stu-id="e1733-105">Prerequisites:</span></span> 

1. <span data-ttu-id="e1733-106">Bir üretim akışı ve etkin olmayan sürüm oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e1733-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="e1733-107">Başlangıç ve bitiş ambarı ve konumları oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e1733-107">The from and to warehouse and locations must be created.</span></span> <span data-ttu-id="e1733-108">İsteğe bağlı olarak, yenileme veya yenilenen iş hücresi oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e1733-108">Optionally, the replenishing or the replenished work cell should be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="e1733-109">Üretim akışı sürümünü bul</span><span class="sxs-lookup"><span data-stu-id="e1733-109">Find the production flow version</span></span>
1. <span data-ttu-id="e1733-110">Üretim kontrolü > Kurulum > Yalın üretim akışı > Üretim akışları seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="e1733-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="e1733-111">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="e1733-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e1733-112">Üretim akışı sürümünün taslak durumda olması gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="e1733-112">Note that the production flow must have a version in draft status.</span></span>  
3. <span data-ttu-id="e1733-113">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e1733-113">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="e1733-114">Yeni bir faaliyet oluştur</span><span class="sxs-lookup"><span data-stu-id="e1733-114">Create a new activity</span></span>
1. <span data-ttu-id="e1733-115">Faaliyetler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e1733-115">Click Activities.</span></span>
    * <span data-ttu-id="e1733-116">Seçili üretim akışında taslak halde bir sürüm olduğundan emin olun ve o sürümü seçin.</span><span class="sxs-lookup"><span data-stu-id="e1733-116">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="e1733-117">Yeni plan faaliyeti oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e1733-117">Click Create new plan activity.</span></span>
3. <span data-ttu-id="e1733-118">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e1733-118">Click Next.</span></span>
4. <span data-ttu-id="e1733-119">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="e1733-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="e1733-120">Faaliyet türü alanında, 'Transfer' seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="e1733-120">In the Activity type field, select 'Transfer'.</span></span>
6. <span data-ttu-id="e1733-121">İşlem miktarı alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="e1733-121">In the Process quantity field, enter a number.</span></span>
7. <span data-ttu-id="e1733-122">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e1733-122">Click Next.</span></span>

## <a name="select-the-work-cells"></a><span data-ttu-id="e1733-123">İş hücrelerini seç</span><span class="sxs-lookup"><span data-stu-id="e1733-123">Select the Work cells</span></span>
1. <span data-ttu-id="e1733-124">Yenileme alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e1733-124">In the Replenishing field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="e1733-125">İş hücresi çıkış konumunu transfer faaliyetindeki çıkış konumu olarak kullanmak için bir iş hücresi seçin.</span><span class="sxs-lookup"><span data-stu-id="e1733-125">To use the work cell output location as the from location in the transfer activity, select a work cell.</span></span> <span data-ttu-id="e1733-126">Aynı işlem transfer faaliyetinin hedef konumunu ayarlayan yenilenen iş hücresi için de yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="e1733-126">The same can be done with the replenished work cell, which sets the target location of the transfer activity.</span></span>  
2. <span data-ttu-id="e1733-127">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e1733-127">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="e1733-128">Stok güncelleştirmelerini tanımla</span><span class="sxs-lookup"><span data-stu-id="e1733-128">Define the inventory updates</span></span>
1. <span data-ttu-id="e1733-129">Ürün türü alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="e1733-129">In the Product type field, select an option.</span></span>
    * <span data-ttu-id="e1733-130">Yapılan bir transferin ürünün türünü değiştirmeyeceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="e1733-130">Note that a transfer does not change the type of product.</span></span> <span data-ttu-id="e1733-131">Bitmiş ürünlerin veya yarı bitmiş ürünlerin transferini gerçekleştirebilirsiniz (bir üretim akışı ve olası bir kanban akışı iki faaliyet arasındaki transfer).</span><span class="sxs-lookup"><span data-stu-id="e1733-131">You can transfer finished products or semi-finished products (transfer between two activities of a production flow and possibly a kanban flow).</span></span>     <span data-ttu-id="e1733-132">Bitmiş ürünlerin transferi yapılırken, malzeme çekilmesi veya alınması sonuçlarını bir stok hareketinde görmeyi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e1733-132">When transferring finished products, you can select if picking or receiving results in an inventory transaction.</span></span>  

## <a name="define-the-transfer-locations"></a><span data-ttu-id="e1733-133">Transfer konumlarını tanımla</span><span class="sxs-lookup"><span data-stu-id="e1733-133">Define the transfer locations</span></span>
1. <span data-ttu-id="e1733-134">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e1733-134">Click Next.</span></span>
2. <span data-ttu-id="e1733-135">Ambar alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="e1733-135">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="e1733-136">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="e1733-136">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="e1733-137">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e1733-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="e1733-138">Yerleşim alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="e1733-138">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="e1733-139">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e1733-139">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="e1733-140">Navlun sorumlusu alanında 'Sevkiyatçı' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e1733-140">In the Freighted by field, select 'Shipper'.</span></span>
    * <span data-ttu-id="e1733-141">Seçenekler şunlardır: Sevkiyatçı - sevk ambarını işleten şirket, Alıcı - alım ambarını işleten şirket, Taşıyıcı - üçüncü taraf sağlayıcı.</span><span class="sxs-lookup"><span data-stu-id="e1733-141">Options include: Shipper - the organization operating the shipping warehouse, Recipient -  the organization operating the receiving warehouse, Carrier - a third party vendor.</span></span> <span data-ttu-id="e1733-142">Faaliyet gösteren şirket bir satıcıysa, transfer faaliyeti için bir alt sözleşme gerekir.</span><span class="sxs-lookup"><span data-stu-id="e1733-142">If the operating organization is a vendor, the transfer activity requires a subcontracting agreement.</span></span>  
8. <span data-ttu-id="e1733-143">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e1733-143">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="e1733-144">Faaliyet sürelerini tanımla</span><span class="sxs-lookup"><span data-stu-id="e1733-144">Define the activity times</span></span>
1. <span data-ttu-id="e1733-145">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="e1733-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e1733-146">Çalışma zamanı tanımı gereklidir.</span><span class="sxs-lookup"><span data-stu-id="e1733-146">The definition of a Runtime is required.</span></span> <span data-ttu-id="e1733-147">Çalışma zamanı, kanban işlerinin maliyetini ve iş çıkarma yeteneği sürelerini hesaplamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e1733-147">The Runtime is used to calculate cost and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="e1733-148">Çalışma zamanları kapasite yükü ve tüketimi hesaplamak için kullanılmaz, üretim akışı sürümü görevinden türetilmiş döngü süresiyle hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="e1733-148">Runtimes are not used to calculate capacity load and consumption, which is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="e1733-149">Zaman alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="e1733-149">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="e1733-150">Birim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="e1733-150">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="e1733-151">Zaman birimini seçin.</span><span class="sxs-lookup"><span data-stu-id="e1733-151">Select the Time unit.</span></span>
5. <span data-ttu-id="e1733-152">Miktar başına alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="e1733-152">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="e1733-153">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="e1733-153">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e1733-154">Kuyruk süreleri isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e1733-154">Queue times are optional.</span></span>  
7. <span data-ttu-id="e1733-155">Zaman alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="e1733-155">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="e1733-156">Birim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="e1733-156">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="e1733-157">Zaman birimini seçin.</span><span class="sxs-lookup"><span data-stu-id="e1733-157">Select the Time unit.</span></span>
10. <span data-ttu-id="e1733-158">Miktar başına alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="e1733-158">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="e1733-159">İleri düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e1733-159">Click Next.</span></span>
12. <span data-ttu-id="e1733-160">Son düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e1733-160">Click Finish.</span></span>
13. <span data-ttu-id="e1733-161">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e1733-161">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]