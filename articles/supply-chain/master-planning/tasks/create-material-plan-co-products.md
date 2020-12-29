---
title: Ortak ürünler için bir malzeme planı oluşturma
description: Üretim Planlayıcısı formül yan ürünleri olan maddeler için malzeme gereksinimleri planlaması yapar.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 14de9a1085ac1cae88ad93c35385dd43c60ed4d1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439318"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="847b7-103">Ortak ürünler için bir malzeme planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="847b7-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="847b7-104">Üretim Planlayıcısı formül yan ürünleri olan maddeler için malzeme gereksinimleri planlaması yapar.</span><span class="sxs-lookup"><span data-stu-id="847b7-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="847b7-105">Bu yöntemi oluşturmak için kullanılan demo verisi şirketi USP2'dir.</span><span class="sxs-lookup"><span data-stu-id="847b7-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="847b7-106">Ortak bir ürün için gereksinim oluşturun</span><span class="sxs-lookup"><span data-stu-id="847b7-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="847b7-107">Varsayılan panoya gidin.</span><span class="sxs-lookup"><span data-stu-id="847b7-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="847b7-108">Satış siparişi işleme ve sorgulama'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="847b7-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="847b7-109">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="847b7-109">Click New.</span></span>
4. <span data-ttu-id="847b7-110">Satış siparişi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="847b7-110">Click Sales order.</span></span>
5. <span data-ttu-id="847b7-111">Müşteri hesabı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="847b7-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="847b7-112">Örnek: US-001</span><span class="sxs-lookup"><span data-stu-id="847b7-112">Example: US-001</span></span>  
6. <span data-ttu-id="847b7-113">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="847b7-113">Click OK.</span></span>
7. <span data-ttu-id="847b7-114">Madde numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="847b7-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="847b7-115">Örnek: P6003</span><span class="sxs-lookup"><span data-stu-id="847b7-115">Example: P6003</span></span>  
8. <span data-ttu-id="847b7-116">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="847b7-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="847b7-117">Örnek: 50000</span><span class="sxs-lookup"><span data-stu-id="847b7-117">Example: 50000</span></span>  
9. <span data-ttu-id="847b7-118">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="847b7-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="847b7-119">Ortak ürünler için malzeme planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="847b7-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="847b7-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="847b7-120">Close the page.</span></span>
2. <span data-ttu-id="847b7-121">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="847b7-121">Close the page.</span></span>
3. <span data-ttu-id="847b7-122">Master planlama'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="847b7-122">Click Master planning.</span></span>
4. <span data-ttu-id="847b7-123">Plan alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="847b7-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="847b7-124">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="847b7-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="847b7-125">Örnek: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="847b7-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="847b7-126">Çalıştır öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="847b7-126">Click Run.</span></span>
7. <span data-ttu-id="847b7-127">Eklenecek kayıtlar bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="847b7-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="847b7-128">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="847b7-128">Click Filter.</span></span>
9. <span data-ttu-id="847b7-129">Listede, Alan = Madde numarası alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="847b7-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="847b7-130">Ölçütler alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="847b7-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="847b7-131">Örnek: P6003</span><span class="sxs-lookup"><span data-stu-id="847b7-131">Example: P6003</span></span>  
11. <span data-ttu-id="847b7-132">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="847b7-132">Click OK.</span></span>
12. <span data-ttu-id="847b7-133">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="847b7-133">Click OK.</span></span>
13. <span data-ttu-id="847b7-134">Planlı siparişler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="847b7-134">Click Planned orders.</span></span>
14. <span data-ttu-id="847b7-135">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="847b7-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="847b7-136">Örneğin, Ürün numarası alanını 'P6000' değeriyle filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="847b7-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="847b7-137">Bir satış siparişi oluşturduğunuz maddeyi, ortak ürün olarak içeren formül maddesine göre filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="847b7-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="847b7-138">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="847b7-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="847b7-139">Filtre tarafından geri getirilen satırlardan herhangi birini seçin.</span><span class="sxs-lookup"><span data-stu-id="847b7-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="847b7-140">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="847b7-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="847b7-141">İlişkilendirme bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="847b7-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="847b7-142">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="847b7-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="847b7-143">Planlı sipariş, ortak ürünün satış siparişine ilişkilendirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="847b7-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="847b7-144">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="847b7-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="847b7-145">Ortak bir ürün için gereksinim oluşturun</span><span class="sxs-lookup"><span data-stu-id="847b7-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="847b7-146">Varsayılan panoya gidin.</span><span class="sxs-lookup"><span data-stu-id="847b7-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="847b7-147">Satış siparişi işleme ve sorgulama'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="847b7-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="847b7-148">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="847b7-148">Click New.</span></span>
4. <span data-ttu-id="847b7-149">Satış siparişi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="847b7-149">Click Sales order.</span></span>
5. <span data-ttu-id="847b7-150">Müşteri hesabı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="847b7-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="847b7-151">Örnek: US-001</span><span class="sxs-lookup"><span data-stu-id="847b7-151">Example: US-001</span></span>  
6. <span data-ttu-id="847b7-152">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="847b7-152">Click OK.</span></span>
7. <span data-ttu-id="847b7-153">Madde numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="847b7-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="847b7-154">Örnek: P6003</span><span class="sxs-lookup"><span data-stu-id="847b7-154">Example: P6003</span></span>  
8. <span data-ttu-id="847b7-155">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="847b7-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="847b7-156">Örnek: 50000</span><span class="sxs-lookup"><span data-stu-id="847b7-156">Example: 50000</span></span>  
9. <span data-ttu-id="847b7-157">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="847b7-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="847b7-158">Ortak ürünler için malzeme planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="847b7-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="847b7-159">Plan alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="847b7-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="847b7-160">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="847b7-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="847b7-161">Örnek: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="847b7-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="847b7-162">Çalıştır öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="847b7-162">Click Run.</span></span>
4. <span data-ttu-id="847b7-163">Eklenecek kayıtlar bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="847b7-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="847b7-164">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="847b7-164">Click Filter.</span></span>
6. <span data-ttu-id="847b7-165">Listede, Alan = Madde numarası alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="847b7-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="847b7-166">Ölçütler alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="847b7-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="847b7-167">Örnek: P6003</span><span class="sxs-lookup"><span data-stu-id="847b7-167">Example: P6003</span></span>  
8. <span data-ttu-id="847b7-168">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="847b7-168">Click OK.</span></span>
9. <span data-ttu-id="847b7-169">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="847b7-169">Click OK.</span></span>
10. <span data-ttu-id="847b7-170">Planlı siparişler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="847b7-170">Click Planned orders.</span></span>
11. <span data-ttu-id="847b7-171">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="847b7-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="847b7-172">Örneğin, Ürün numarası alanını 'P6000' değeriyle filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="847b7-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="847b7-173">Bir satış siparişi oluşturduğunuz maddeyi, ortak ürün olarak içeren formül maddesine göre filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="847b7-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="847b7-174">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="847b7-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="847b7-175">Filtre tarafından geri getirilen satırlardan herhangi birini seçin.</span><span class="sxs-lookup"><span data-stu-id="847b7-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="847b7-176">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="847b7-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="847b7-177">İlişkilendirme bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="847b7-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="847b7-178">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="847b7-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="847b7-179">Planlı sipariş, ortak ürünün satış siparişine ilişkilendirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="847b7-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="847b7-180">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="847b7-180">Close the page.</span></span>
17. <span data-ttu-id="847b7-181">Master planlama'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="847b7-181">Click Master planning.</span></span>
18. <span data-ttu-id="847b7-182">Master planlama > Kurulum > Master planlama parametreleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="847b7-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="847b7-183">Tüm planlama işlemlerini devre dışı bırak alanında Hayır'ı işaretle.</span><span class="sxs-lookup"><span data-stu-id="847b7-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="847b7-184">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="847b7-184">Close the page.</span></span>

