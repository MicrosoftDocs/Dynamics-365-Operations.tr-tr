---
title: Malların şirket içinde taşınması için transfer belgelerini ayarlama
description: Bu yordam, bir şirket içinde malların taşınması için transfer belgeleri oluşturmayı gösterir.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fe4dd04595c961e1c66178e6ac6955e945869ded
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/02/2019
ms.locfileid: "1852558"
---
# <a name="set-up-the-transfer-documents-for-goods-movement-inside-a-company"></a><span data-ttu-id="b158c-103">Malların şirket içinde taşınması için transfer belgelerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="b158c-103">Set up the transfer documents for goods movement inside a company</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b158c-104">Bu yordam, bir şirket içinde malların taşınması için transfer belgeleri oluşturmayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="b158c-104">This procedure shows how to create transfer documents for goods movement inside a company.</span></span> <span data-ttu-id="b158c-105">Bu yordam yalnızca birincil adresi Litvanya'da bulunan tüzel kişilikler tarafından kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b158c-105">This procedure is only available for legal entities with a primary address in Lithuania.</span></span> <span data-ttu-id="b158c-106">Bu yordam, birincil adresi Litvanya'da bulunan demo veri şirketi DEMF kullanılarak oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="b158c-106">The procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="b158c-107">Bu yordamı tamamlayabilmeniz için "Şirket içinde malların taşınması için transfer belgelerini ayarlama" yordamını tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b158c-107">Before you can complete this procedure, you must complete the “Set up transfer documents for goods movement inside a company” procedure.</span></span> <span data-ttu-id="b158c-108">Bu yordam stok muhasebecileri için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="b158c-108">This procedure is intended for inventory accountants.</span></span> <span data-ttu-id="b158c-109">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="b158c-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-transfer-order"></a><span data-ttu-id="b158c-110">Transfer emri oluşturma</span><span class="sxs-lookup"><span data-stu-id="b158c-110">Create a transfer order</span></span>
1. <span data-ttu-id="b158c-111">Stok Yönetimi > Gelen siparişler > Transfer emri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="b158c-111">Go to Inventory management > Inbound orders > Transfer order.</span></span>
2. <span data-ttu-id="b158c-112">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b158c-112">Click New.</span></span>
3. <span data-ttu-id="b158c-113">Kaynak ambar alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="b158c-113">In the From warehouse field, enter or select a value.</span></span>
4. <span data-ttu-id="b158c-114">Hedef ambar alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="b158c-114">In the To warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="b158c-115">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b158c-115">Click Add.</span></span>
6. <span data-ttu-id="b158c-116">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="b158c-116">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="b158c-117">Madde numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="b158c-117">In the Item number field, enter or select a value.</span></span>

## <a name="enter-transportation-details-for-the-transfer-order"></a><span data-ttu-id="b158c-118">Transfer emri için taşıma ayrıntılarını girme</span><span class="sxs-lookup"><span data-stu-id="b158c-118">Enter transportation details for the transfer order</span></span>
1. <span data-ttu-id="b158c-119">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b158c-119">Click Save.</span></span>
2. <span data-ttu-id="b158c-120">Eylem Bölmesinde, Sevk et'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b158c-120">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="b158c-121">Taşıma Ayrıntıları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b158c-121">Click Transportation details.</span></span>
4. <span data-ttu-id="b158c-122">Taşıma ayrıntılarını yazdır alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b158c-122">Select Yes in the Print transportation details field.</span></span>
5. <span data-ttu-id="b158c-123">Malları veren alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="b158c-123">In the Goods issued by field, enter or select a value.</span></span>
6. <span data-ttu-id="b158c-124">Paket alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="b158c-124">In the Package field, type a value.</span></span>
7. <span data-ttu-id="b158c-125">Yükün risk düzeyi alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="b158c-125">In the Risk level of the load field, type a value.</span></span>
8. <span data-ttu-id="b158c-126">Taşıyıcı alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="b158c-126">In the Carrier field, enter or select a value.</span></span>
9. <span data-ttu-id="b158c-127">Model alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="b158c-127">In the Model field, enter or select a value.</span></span>
10. <span data-ttu-id="b158c-128">Kayıt numarası alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="b158c-128">In the Registration number field, type a value.</span></span>
11. <span data-ttu-id="b158c-129">Treyler kayıt numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="b158c-129">In the Trailer registration number field, type a value.</span></span>
12. <span data-ttu-id="b158c-130">Sürücü alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="b158c-130">In the Driver field, enter or select a value.</span></span>
13. <span data-ttu-id="b158c-131">Sürücü adı alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="b158c-131">In the Driver name field, type a value.</span></span>
14. <span data-ttu-id="b158c-132">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b158c-132">Click Save.</span></span>
15. <span data-ttu-id="b158c-133">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="b158c-133">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a><span data-ttu-id="b158c-134">Nakledilmemiş bir transfer emri için sevk irsaliyesini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="b158c-134">View the packing slip for the unposted transfer order</span></span>
1. <span data-ttu-id="b158c-135">Sevk irsaliyesi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b158c-135">Click Packing slip.</span></span>
2. <span data-ttu-id="b158c-136">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b158c-136">Click OK.</span></span>
3. <span data-ttu-id="b158c-137">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="b158c-137">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a><span data-ttu-id="b158c-138">Nakledilmiş transfer emri için sevk irsaliyesini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="b158c-138">View the packing slip for the posted transfer order</span></span>
1. <span data-ttu-id="b158c-139">Eylem Bölmesi'nde, Transfer emri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b158c-139">On the Action Pane, click Transfer order.</span></span>
2. <span data-ttu-id="b158c-140">Eylem Bölmesinde, Sevk et'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b158c-140">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="b158c-141">Sevk transfer emri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b158c-141">Click Ship transfer order.</span></span>
4. <span data-ttu-id="b158c-142">Genel sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b158c-142">Click the General tab.</span></span>
5. <span data-ttu-id="b158c-143">Güncelleştir alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="b158c-143">In the Update field, select an option.</span></span>
6. <span data-ttu-id="b158c-144">Özet sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b158c-144">Click the Overview tab.</span></span>
7. <span data-ttu-id="b158c-145">Sevk irsaliyesi alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="b158c-145">In the Packing slip field, type a value.</span></span>
8. <span data-ttu-id="b158c-146">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b158c-146">Click OK.</span></span>
9. <span data-ttu-id="b158c-147">Eylem Bölmesinde, Sevk et'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b158c-147">On the Action Pane, click Ship.</span></span>
10. <span data-ttu-id="b158c-148">Sevk irsaliyesi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b158c-148">Click Packing slip.</span></span>
11. <span data-ttu-id="b158c-149">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b158c-149">Click OK.</span></span>

