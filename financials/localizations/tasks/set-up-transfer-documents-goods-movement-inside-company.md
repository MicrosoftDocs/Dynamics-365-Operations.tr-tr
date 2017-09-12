--- 
title: "Malların şirket içinde taşınması için transfer belgelerini ayarlama"
description: "Bu yordam, bir şirket içinde malların taşınması için transfer belgeleri oluşturmayı gösterir."
author: v-oloski
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2f10f627f33108b8750a1d71d24a99763178e2ef
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-the-transfer-documents-for-goods-movement-inside-a-company"></a><span data-ttu-id="9ea90-103">Malların şirket içinde taşınması için transfer belgelerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="9ea90-103">Set up the transfer documents for goods movement inside a company</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9ea90-104">Bu yordam, bir şirket içinde malların taşınması için transfer belgeleri oluşturmayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="9ea90-104">This procedure shows how to create transfer documents for goods movement inside a company.</span></span> <span data-ttu-id="9ea90-105">Bu yordam yalnızca birincil adresi Litvanya'da bulunan tüzel kişilikler tarafından kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9ea90-105">This procedure is only available for legal entities with a primary address in Lithuania.</span></span> <span data-ttu-id="9ea90-106">Bu yordam, birincil adresi Litvanya'da bulunan demo veri şirketi DEMF kullanılarak oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="9ea90-106">The procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="9ea90-107">Bu yordamı tamamlayabilmeniz için "Şirket içinde malların taşınması için transfer belgelerini ayarlama" yordamını tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="9ea90-107">Before you can complete this procedure, you must complete the “Set up transfer documents for goods movement inside a company” procedure.</span></span> <span data-ttu-id="9ea90-108">Bu yordam stok muhasebecileri için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="9ea90-108">This procedure is intended for inventory accountants.</span></span> <span data-ttu-id="9ea90-109">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="9ea90-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-transfer-order"></a><span data-ttu-id="9ea90-110">Transfer emri oluşturma</span><span class="sxs-lookup"><span data-stu-id="9ea90-110">Create a transfer order</span></span>
1. <span data-ttu-id="9ea90-111">Stok Yönetimi > Gelen siparişler > Transfer emri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="9ea90-111">Go to Inventory management > Inbound orders > Transfer order.</span></span>
2. <span data-ttu-id="9ea90-112">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9ea90-112">Click New.</span></span>
3. <span data-ttu-id="9ea90-113">Kaynak ambar alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9ea90-113">In the From warehouse field, enter or select a value.</span></span>
4. <span data-ttu-id="9ea90-114">Hedef ambar alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="9ea90-114">In the To warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="9ea90-115">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9ea90-115">Click Add.</span></span>
6. <span data-ttu-id="9ea90-116">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="9ea90-116">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="9ea90-117">Madde numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="9ea90-117">In the Item number field, enter or select a value.</span></span>

## <a name="enter-transportation-details-for-the-transfer-order"></a><span data-ttu-id="9ea90-118">Transfer emri için taşıma ayrıntılarını girme</span><span class="sxs-lookup"><span data-stu-id="9ea90-118">Enter transportation details for the transfer order</span></span>
1. <span data-ttu-id="9ea90-119">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9ea90-119">Click Save.</span></span>
2. <span data-ttu-id="9ea90-120">Eylem Bölmesinde, Sevk et'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9ea90-120">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="9ea90-121">Taşıma Ayrıntıları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9ea90-121">Click Transportation details.</span></span>
4. <span data-ttu-id="9ea90-122">Taşıma ayrıntılarını yazdır alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9ea90-122">Select Yes in the Print transportation details field.</span></span>
5. <span data-ttu-id="9ea90-123">Malları veren alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="9ea90-123">In the Goods issued by field, enter or select a value.</span></span>
6. <span data-ttu-id="9ea90-124">Paket alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="9ea90-124">In the Package field, type a value.</span></span>
7. <span data-ttu-id="9ea90-125">Yükün risk düzeyi alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="9ea90-125">In the Risk level of the load field, type a value.</span></span>
8. <span data-ttu-id="9ea90-126">Taşıyıcı alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="9ea90-126">In the Carrier field, enter or select a value.</span></span>
9. <span data-ttu-id="9ea90-127">Model alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="9ea90-127">In the Model field, enter or select a value.</span></span>
10. <span data-ttu-id="9ea90-128">Kayıt numarası alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="9ea90-128">In the Registration number field, type a value.</span></span>
11. <span data-ttu-id="9ea90-129">Treyler kayıt numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="9ea90-129">In the Trailer registration number field, type a value.</span></span>
12. <span data-ttu-id="9ea90-130">Sürücü alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="9ea90-130">In the Driver field, enter or select a value.</span></span>
13. <span data-ttu-id="9ea90-131">Sürücü adı alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="9ea90-131">In the Driver name field, type a value.</span></span>
14. <span data-ttu-id="9ea90-132">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9ea90-132">Click Save.</span></span>
15. <span data-ttu-id="9ea90-133">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9ea90-133">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a><span data-ttu-id="9ea90-134">Nakledilmemiş bir transfer emri için sevk irsaliyesini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="9ea90-134">View the packing slip for the unposted transfer order</span></span>
1. <span data-ttu-id="9ea90-135">Sevk irsaliyesi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9ea90-135">Click Packing slip.</span></span>
2. <span data-ttu-id="9ea90-136">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9ea90-136">Click OK.</span></span>
3. <span data-ttu-id="9ea90-137">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9ea90-137">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a><span data-ttu-id="9ea90-138">Nakledilmiş transfer emri için sevk irsaliyesini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="9ea90-138">View the packing slip for the posted transfer order</span></span>
1. <span data-ttu-id="9ea90-139">Eylem Bölmesi'nde, Transfer emri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9ea90-139">On the Action Pane, click Transfer order.</span></span>
2. <span data-ttu-id="9ea90-140">Eylem Bölmesinde, Sevk et'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9ea90-140">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="9ea90-141">Sevk transfer emri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9ea90-141">Click Ship transfer order.</span></span>
4. <span data-ttu-id="9ea90-142">Genel sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9ea90-142">Click the General tab.</span></span>
5. <span data-ttu-id="9ea90-143">Güncelleştir alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="9ea90-143">In the Update field, select an option.</span></span>
6. <span data-ttu-id="9ea90-144">Özet sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9ea90-144">Click the Overview tab.</span></span>
7. <span data-ttu-id="9ea90-145">Sevk irsaliyesi alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="9ea90-145">In the Packing slip field, type a value.</span></span>
8. <span data-ttu-id="9ea90-146">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9ea90-146">Click OK.</span></span>
9. <span data-ttu-id="9ea90-147">Eylem Bölmesinde, Sevk et'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9ea90-147">On the Action Pane, click Ship.</span></span>
10. <span data-ttu-id="9ea90-148">Sevk irsaliyesi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9ea90-148">Click Packing slip.</span></span>
11. <span data-ttu-id="9ea90-149">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9ea90-149">Click OK.</span></span>


