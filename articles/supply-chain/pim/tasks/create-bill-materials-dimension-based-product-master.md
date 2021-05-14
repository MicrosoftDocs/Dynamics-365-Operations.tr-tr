---
title: Boyut tabanlı ana ürün için ürün reçetesi oluşturma
description: Bu prosedür için bu sekiz kayıt sırasındaki, önceki 4 kılavuzu tamamlamış olmanız gerekir.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13053dd87242963586678b46c64493feb3383c4c
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920717"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="df404-103">Boyut tabanlı ana ürün için ürün reçetesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="df404-103">Create a bill of materials for a dimension-based product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="df404-104">Bu prosedür için bu sekiz kayıt sırasındaki, önceki 4 kılavuzu tamamlamış olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="df404-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="df404-105">İlk 4 kayıtta bu prosedürün tamamlanması için gereken verileri kurulur.</span><span class="sxs-lookup"><span data-stu-id="df404-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="df404-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="df404-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="df404-107">Bu görev tipik olarak ürün tasarımcısı tarafından ele alınır.</span><span class="sxs-lookup"><span data-stu-id="df404-107">This task is typically handled by the product designer.</span></span>

## <a name="select-the-product"></a><span data-ttu-id="df404-108">Ürün seçme</span><span class="sxs-lookup"><span data-stu-id="df404-108">Select the product</span></span>

1. <span data-ttu-id="df404-109">**Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="df404-109">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="df404-110">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="df404-110">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="df404-111">Bu sıradaki ilk görev kılavuzunda oluşturduğunuz, boyut tabanlı yapılandırma teknolojisiyle, serbest bırakılan ürün mastarını bulun.</span><span class="sxs-lookup"><span data-stu-id="df404-111">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
1. <span data-ttu-id="df404-112">Eylem Bölmesi'nde **Mühendis**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="df404-112">On the Action Pane, select **Engineer**.</span></span>
1. <span data-ttu-id="df404-113">**Ürün Reçetesi sürümleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="df404-113">Select **BOM versions**.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="df404-114">Yeni BOM ve BOM sürümünü oluşturma</span><span class="sxs-lookup"><span data-stu-id="df404-114">Create new BOM and BOM version</span></span>

1. <span data-ttu-id="df404-115">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="df404-115">Select **New**.</span></span>
1. <span data-ttu-id="df404-116">**Ürün Reçetesi ve Ürün Reçetesi sürümü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="df404-116">Select **BOM and BOM version**.</span></span>
1. <span data-ttu-id="df404-117">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="df404-117">In the **Name** field, type a value.</span></span>
    * <span data-ttu-id="df404-118">Bir saha ayarlanması</span><span class="sxs-lookup"><span data-stu-id="df404-118">Setting a site</span></span>  
    * <span data-ttu-id="df404-119">Bu prosedürde BOM için belirli bir saha ayarlamıyoruz.</span><span class="sxs-lookup"><span data-stu-id="df404-119">In this procedure we don't set a specific site for the BOM.</span></span>  
1. <span data-ttu-id="df404-120">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="df404-120">Select **OK**.</span></span>
1. <span data-ttu-id="df404-121">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="df404-121">Select **New**.</span></span>
    * <span data-ttu-id="df404-122">Bu prosedürde BOM'a dört satır ekleyeceğiz.</span><span class="sxs-lookup"><span data-stu-id="df404-122">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="df404-123">İki satır, kablo seçeneklerini temsil ederken; iki satır, dolap seçeneklerini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="df404-123">Two lines represent cable options and two lines represent cabinet options.</span></span>  
1. <span data-ttu-id="df404-124">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="df404-124">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="df404-125">**Madde numarası** alanına bir değer girin veya bu alanda bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="df404-125">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="df404-126">A0001, HDMI 6' Kablo madde numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="df404-126">Select item number A0001, HDMI 6' Cables.</span></span>  
1. <span data-ttu-id="df404-127">**Yapılandırma grubu** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="df404-127">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="df404-128">Bu sıradaki kılavuz 4'te oluşturulan kablo yapılandırma grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="df404-128">Select the cable configuration group created in guide 4 in this sequence.</span></span>  
1. <span data-ttu-id="df404-129">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="df404-129">Select **New**.</span></span>
    * <span data-ttu-id="df404-130">A0002, HDMI 12' Kablo madde numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="df404-130">Select item number A0002, HDMI 12' Cables.</span></span>  
1. <span data-ttu-id="df404-131">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="df404-131">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="df404-132">**Madde numarası** alanına bir değer girin veya bu alanda bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="df404-132">In the **Item number** field, enter or select a value.</span></span>
1. <span data-ttu-id="df404-133">**Yapılandırma grubu** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="df404-133">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="df404-134">Kablo yapılandırma grubunu yeniden seçin.</span><span class="sxs-lookup"><span data-stu-id="df404-134">Select the cable configuration group again.</span></span>  
1. <span data-ttu-id="df404-135">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="df404-135">Select **New**.</span></span>
1. <span data-ttu-id="df404-136">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="df404-136">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="df404-137">**Madde numarası** alanına bir değer girin veya bu alanda bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="df404-137">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="df404-138">D0002 Dolap madde numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="df404-138">Select item number D0002 Cabinet.</span></span>  
1. <span data-ttu-id="df404-139">**Yapılandırma grubu** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="df404-139">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="df404-140">Bu Ürün Reçetesi satırı için dolap yapılandırma grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="df404-140">Select the cabinet configuration group for this BOM line.</span></span>  
1. <span data-ttu-id="df404-141">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="df404-141">Select **New**.</span></span>
1. <span data-ttu-id="df404-142">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="df404-142">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="df404-143">**Madde numarası** alanına bir değer girin veya bu alanda bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="df404-143">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="df404-144">Son BOM satırı olarak, M0007 Standart Dolap madde numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="df404-144">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
1. <span data-ttu-id="df404-145">**Yapılandırma grubu** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="df404-145">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="df404-146">Son Ürün Reçetesi satırı için Dolap yapılandırma grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="df404-146">Select the Cabinet configuration group for the last BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="df404-147">Onayla ve etkinleştir</span><span class="sxs-lookup"><span data-stu-id="df404-147">Approve and activate</span></span>

1. <span data-ttu-id="df404-148">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="df404-148">Close the page.</span></span>
1. <span data-ttu-id="df404-149">**Onayla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="df404-149">Select **Approve**.</span></span>
1. <span data-ttu-id="df404-150">**Onaylayan** alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="df404-150">In the **Approved by** field, enter or select a value.</span></span>
1. <span data-ttu-id="df404-151">**Ürün reçetesini de onaylamak ister misiniz?** sorusunu *Evet* olarak yanıtlayın.</span><span class="sxs-lookup"><span data-stu-id="df404-151">Select *Yes* in the **Do you also want to approve the bill of materials?** field.</span></span>
1. <span data-ttu-id="df404-152">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="df404-152">Select **OK**.</span></span>
1. <span data-ttu-id="df404-153">**Etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="df404-153">Select **Activate**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]