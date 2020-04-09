---
title: Ortak ürünler için bir malzeme planı oluşturma
description: Üretim Planlayıcısı formül yan ürünleri olan maddeler için malzeme gereksinimleri planlaması yapar.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 714f0c5f014aac1f006b8356de8570ad7d7e0d47
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148090"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="1c568-103">Ortak ürünler için bir malzeme planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="1c568-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1c568-104">Üretim Planlayıcısı formül yan ürünleri olan maddeler için malzeme gereksinimleri planlaması yapar.</span><span class="sxs-lookup"><span data-stu-id="1c568-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="1c568-105">Bu yöntemi oluşturmak için kullanılan demo verisi şirketi USP2'dir.</span><span class="sxs-lookup"><span data-stu-id="1c568-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="1c568-106">Ortak bir ürün için gereksinim oluşturun</span><span class="sxs-lookup"><span data-stu-id="1c568-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="1c568-107">Varsayılan panoya gidin.</span><span class="sxs-lookup"><span data-stu-id="1c568-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="1c568-108">Satış siparişi işleme ve sorgulama'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c568-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="1c568-109">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1c568-109">Click New.</span></span>
4. <span data-ttu-id="1c568-110">Satış siparişi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c568-110">Click Sales order.</span></span>
5. <span data-ttu-id="1c568-111">Müşteri hesabı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="1c568-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="1c568-112">Örnek: US-001</span><span class="sxs-lookup"><span data-stu-id="1c568-112">Example: US-001</span></span>  
6. <span data-ttu-id="1c568-113">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c568-113">Click OK.</span></span>
7. <span data-ttu-id="1c568-114">Madde numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="1c568-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="1c568-115">Örnek: P6003</span><span class="sxs-lookup"><span data-stu-id="1c568-115">Example: P6003</span></span>  
8. <span data-ttu-id="1c568-116">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="1c568-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="1c568-117">Örnek: 50000</span><span class="sxs-lookup"><span data-stu-id="1c568-117">Example: 50000</span></span>  
9. <span data-ttu-id="1c568-118">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c568-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="1c568-119">Ortak ürünler için malzeme planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="1c568-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="1c568-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="1c568-120">Close the page.</span></span>
2. <span data-ttu-id="1c568-121">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="1c568-121">Close the page.</span></span>
3. <span data-ttu-id="1c568-122">Master planlama'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c568-122">Click Master planning.</span></span>
4. <span data-ttu-id="1c568-123">Plan alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c568-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="1c568-124">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c568-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1c568-125">Örnek: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="1c568-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="1c568-126">Çalıştır öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c568-126">Click Run.</span></span>
7. <span data-ttu-id="1c568-127">Eklenecek kayıtlar bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="1c568-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="1c568-128">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c568-128">Click Filter.</span></span>
9. <span data-ttu-id="1c568-129">Listede, Alan = Madde numarası alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="1c568-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="1c568-130">Ölçütler alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="1c568-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="1c568-131">Örnek: P6003</span><span class="sxs-lookup"><span data-stu-id="1c568-131">Example: P6003</span></span>  
11. <span data-ttu-id="1c568-132">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c568-132">Click OK.</span></span>
12. <span data-ttu-id="1c568-133">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c568-133">Click OK.</span></span>
13. <span data-ttu-id="1c568-134">Planlı siparişler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c568-134">Click Planned orders.</span></span>
14. <span data-ttu-id="1c568-135">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="1c568-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="1c568-136">Örneğin, Ürün numarası alanını 'P6000' değeriyle filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="1c568-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="1c568-137">Bir satış siparişi oluşturduğunuz maddeyi, ortak ürün olarak içeren formül maddesine göre filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="1c568-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="1c568-138">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1c568-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="1c568-139">Filtre tarafından geri getirilen satırlardan herhangi birini seçin.</span><span class="sxs-lookup"><span data-stu-id="1c568-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="1c568-140">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c568-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="1c568-141">İlişkilendirme bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="1c568-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="1c568-142">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c568-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1c568-143">Planlı sipariş, ortak ürünün satış siparişine ilişkilendirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="1c568-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="1c568-144">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="1c568-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="1c568-145">Ortak bir ürün için gereksinim oluşturun</span><span class="sxs-lookup"><span data-stu-id="1c568-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="1c568-146">Varsayılan panoya gidin.</span><span class="sxs-lookup"><span data-stu-id="1c568-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="1c568-147">Satış siparişi işleme ve sorgulama'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c568-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="1c568-148">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1c568-148">Click New.</span></span>
4. <span data-ttu-id="1c568-149">Satış siparişi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c568-149">Click Sales order.</span></span>
5. <span data-ttu-id="1c568-150">Müşteri hesabı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="1c568-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="1c568-151">Örnek: US-001</span><span class="sxs-lookup"><span data-stu-id="1c568-151">Example: US-001</span></span>  
6. <span data-ttu-id="1c568-152">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c568-152">Click OK.</span></span>
7. <span data-ttu-id="1c568-153">Madde numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="1c568-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="1c568-154">Örnek: P6003</span><span class="sxs-lookup"><span data-stu-id="1c568-154">Example: P6003</span></span>  
8. <span data-ttu-id="1c568-155">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="1c568-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="1c568-156">Örnek: 50000</span><span class="sxs-lookup"><span data-stu-id="1c568-156">Example: 50000</span></span>  
9. <span data-ttu-id="1c568-157">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c568-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="1c568-158">Ortak ürünler için malzeme planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="1c568-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="1c568-159">Plan alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c568-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="1c568-160">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c568-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1c568-161">Örnek: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="1c568-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="1c568-162">Çalıştır öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c568-162">Click Run.</span></span>
4. <span data-ttu-id="1c568-163">Eklenecek kayıtlar bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="1c568-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="1c568-164">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c568-164">Click Filter.</span></span>
6. <span data-ttu-id="1c568-165">Listede, Alan = Madde numarası alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="1c568-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="1c568-166">Ölçütler alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="1c568-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="1c568-167">Örnek: P6003</span><span class="sxs-lookup"><span data-stu-id="1c568-167">Example: P6003</span></span>  
8. <span data-ttu-id="1c568-168">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c568-168">Click OK.</span></span>
9. <span data-ttu-id="1c568-169">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c568-169">Click OK.</span></span>
10. <span data-ttu-id="1c568-170">Planlı siparişler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c568-170">Click Planned orders.</span></span>
11. <span data-ttu-id="1c568-171">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="1c568-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="1c568-172">Örneğin, Ürün numarası alanını 'P6000' değeriyle filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="1c568-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="1c568-173">Bir satış siparişi oluşturduğunuz maddeyi, ortak ürün olarak içeren formül maddesine göre filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="1c568-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="1c568-174">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1c568-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="1c568-175">Filtre tarafından geri getirilen satırlardan herhangi birini seçin.</span><span class="sxs-lookup"><span data-stu-id="1c568-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="1c568-176">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c568-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="1c568-177">İlişkilendirme bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="1c568-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="1c568-178">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c568-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1c568-179">Planlı sipariş, ortak ürünün satış siparişine ilişkilendirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="1c568-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="1c568-180">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="1c568-180">Close the page.</span></span>
17. <span data-ttu-id="1c568-181">Master planlama'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c568-181">Click Master planning.</span></span>
18. <span data-ttu-id="1c568-182">Master planlama > Kurulum > Master planlama parametreleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="1c568-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="1c568-183">Tüm planlama işlemlerini devre dışı bırak alanında Hayır'ı işaretle.</span><span class="sxs-lookup"><span data-stu-id="1c568-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="1c568-184">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="1c568-184">Close the page.</span></span>

