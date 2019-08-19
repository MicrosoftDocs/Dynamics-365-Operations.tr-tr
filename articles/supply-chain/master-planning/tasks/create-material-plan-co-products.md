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
ms.openlocfilehash: e59ff769685677b0970dbc7d4c9d4d2c1e5b63d1
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835970"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="b1036-103">Ortak ürünler için bir malzeme planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="b1036-103">Create a material plan for co products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b1036-104">Üretim Planlayıcısı formül yan ürünleri olan maddeler için malzeme gereksinimleri planlaması yapar.</span><span class="sxs-lookup"><span data-stu-id="b1036-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="b1036-105">Bu yöntemi oluşturmak için kullanılan demo verisi şirketi USP2'dir.</span><span class="sxs-lookup"><span data-stu-id="b1036-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="b1036-106">Ortak bir ürün için gereksinim oluşturun</span><span class="sxs-lookup"><span data-stu-id="b1036-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="b1036-107">Varsayılan panoya gidin.</span><span class="sxs-lookup"><span data-stu-id="b1036-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="b1036-108">Satış siparişi işleme ve sorgulama'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1036-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="b1036-109">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b1036-109">Click New.</span></span>
4. <span data-ttu-id="b1036-110">Satış siparişi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1036-110">Click Sales order.</span></span>
5. <span data-ttu-id="b1036-111">Müşteri hesabı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="b1036-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="b1036-112">Örnek: US-001</span><span class="sxs-lookup"><span data-stu-id="b1036-112">Example: US-001</span></span>  
6. <span data-ttu-id="b1036-113">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1036-113">Click OK.</span></span>
7. <span data-ttu-id="b1036-114">Madde numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="b1036-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="b1036-115">Örnek: P6003</span><span class="sxs-lookup"><span data-stu-id="b1036-115">Example: P6003</span></span>  
8. <span data-ttu-id="b1036-116">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="b1036-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="b1036-117">Örnek: 50000</span><span class="sxs-lookup"><span data-stu-id="b1036-117">Example: 50000</span></span>  
9. <span data-ttu-id="b1036-118">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1036-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="b1036-119">Ortak ürünler için malzeme planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="b1036-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="b1036-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="b1036-120">Close the page.</span></span>
2. <span data-ttu-id="b1036-121">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="b1036-121">Close the page.</span></span>
3. <span data-ttu-id="b1036-122">Master planlama'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1036-122">Click Master planning.</span></span>
4. <span data-ttu-id="b1036-123">Plan alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1036-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="b1036-124">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1036-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b1036-125">Örnek: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="b1036-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="b1036-126">Çalıştır öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1036-126">Click Run.</span></span>
7. <span data-ttu-id="b1036-127">Eklenecek kayıtlar bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="b1036-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="b1036-128">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1036-128">Click Filter.</span></span>
9. <span data-ttu-id="b1036-129">Listede, Alan = Madde numarası alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="b1036-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="b1036-130">Ölçütler alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="b1036-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="b1036-131">Örnek: P6003</span><span class="sxs-lookup"><span data-stu-id="b1036-131">Example: P6003</span></span>  
11. <span data-ttu-id="b1036-132">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1036-132">Click OK.</span></span>
12. <span data-ttu-id="b1036-133">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1036-133">Click OK.</span></span>
13. <span data-ttu-id="b1036-134">Planlı siparişler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1036-134">Click Planned orders.</span></span>
14. <span data-ttu-id="b1036-135">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="b1036-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b1036-136">Örneğin, Ürün numarası alanını 'P6000' değeriyle filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="b1036-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="b1036-137">Bir satış siparişi oluşturduğunuz maddeyi, ortak ürün olarak içeren formül maddesine göre filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="b1036-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="b1036-138">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="b1036-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b1036-139">Filtre tarafından geri getirilen satırlardan herhangi birini seçin.</span><span class="sxs-lookup"><span data-stu-id="b1036-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="b1036-140">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1036-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="b1036-141">İlişkilendirme bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="b1036-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="b1036-142">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1036-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b1036-143">Planlı sipariş, ortak ürünün satış siparişine ilişkilendirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="b1036-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="b1036-144">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="b1036-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="b1036-145">Ortak bir ürün için gereksinim oluşturun</span><span class="sxs-lookup"><span data-stu-id="b1036-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="b1036-146">Varsayılan panoya gidin.</span><span class="sxs-lookup"><span data-stu-id="b1036-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="b1036-147">Satış siparişi işleme ve sorgulama'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1036-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="b1036-148">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b1036-148">Click New.</span></span>
4. <span data-ttu-id="b1036-149">Satış siparişi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1036-149">Click Sales order.</span></span>
5. <span data-ttu-id="b1036-150">Müşteri hesabı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="b1036-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="b1036-151">Örnek: US-001</span><span class="sxs-lookup"><span data-stu-id="b1036-151">Example: US-001</span></span>  
6. <span data-ttu-id="b1036-152">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1036-152">Click OK.</span></span>
7. <span data-ttu-id="b1036-153">Madde numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="b1036-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="b1036-154">Örnek: P6003</span><span class="sxs-lookup"><span data-stu-id="b1036-154">Example: P6003</span></span>  
8. <span data-ttu-id="b1036-155">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="b1036-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="b1036-156">Örnek: 50000</span><span class="sxs-lookup"><span data-stu-id="b1036-156">Example: 50000</span></span>  
9. <span data-ttu-id="b1036-157">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1036-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="b1036-158">Ortak ürünler için malzeme planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="b1036-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="b1036-159">Plan alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1036-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="b1036-160">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1036-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b1036-161">Örnek: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="b1036-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="b1036-162">Çalıştır öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1036-162">Click Run.</span></span>
4. <span data-ttu-id="b1036-163">Eklenecek kayıtlar bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="b1036-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="b1036-164">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1036-164">Click Filter.</span></span>
6. <span data-ttu-id="b1036-165">Listede, Alan = Madde numarası alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="b1036-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="b1036-166">Ölçütler alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="b1036-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="b1036-167">Örnek: P6003</span><span class="sxs-lookup"><span data-stu-id="b1036-167">Example: P6003</span></span>  
8. <span data-ttu-id="b1036-168">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1036-168">Click OK.</span></span>
9. <span data-ttu-id="b1036-169">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1036-169">Click OK.</span></span>
10. <span data-ttu-id="b1036-170">Planlı siparişler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1036-170">Click Planned orders.</span></span>
11. <span data-ttu-id="b1036-171">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="b1036-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b1036-172">Örneğin, Ürün numarası alanını 'P6000' değeriyle filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="b1036-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="b1036-173">Bir satış siparişi oluşturduğunuz maddeyi, ortak ürün olarak içeren formül maddesine göre filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="b1036-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="b1036-174">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="b1036-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b1036-175">Filtre tarafından geri getirilen satırlardan herhangi birini seçin.</span><span class="sxs-lookup"><span data-stu-id="b1036-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="b1036-176">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1036-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="b1036-177">İlişkilendirme bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="b1036-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="b1036-178">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1036-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b1036-179">Planlı sipariş, ortak ürünün satış siparişine ilişkilendirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="b1036-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="b1036-180">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="b1036-180">Close the page.</span></span>
17. <span data-ttu-id="b1036-181">Master planlama'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1036-181">Click Master planning.</span></span>
18. <span data-ttu-id="b1036-182">Master planlama > Kurulum > Master planlama parametreleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="b1036-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="b1036-183">Tüm planlama işlemlerini devre dışı bırak alanında Hayır'ı işaretle.</span><span class="sxs-lookup"><span data-stu-id="b1036-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="b1036-184">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="b1036-184">Close the page.</span></span>

