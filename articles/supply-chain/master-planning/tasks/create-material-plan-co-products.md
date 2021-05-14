---
title: Ortak ürünler için bir malzeme planı oluşturma
description: Üretim Planlayıcısı formül yan ürünleri olan maddeler için malzeme gereksinimleri planlaması yapar.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b51e4b4d00da2babb5128d8c4c22139b0c1853d4
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920741"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="4aa6b-103">Ortak ürünler için bir malzeme planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="4aa6b-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4aa6b-104">Üretim Planlayıcısı formül yan ürünleri olan maddeler için malzeme gereksinimleri planlaması yapar.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="4aa6b-105">Bu yöntemi oluşturmak için kullanılan demo verisi şirketi USP2'dir.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-105">The demo data company used to create this procedure is USP2.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="4aa6b-106">Ortak bir ürün için gereksinim oluşturun</span><span class="sxs-lookup"><span data-stu-id="4aa6b-106">Create requirement for a co-product</span></span>

1. <span data-ttu-id="4aa6b-107">**Satış ve pazarlama \> Çalışma alanları \> Satış siparişi işleme ve sorgulama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-107">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="4aa6b-108">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-108">Select **New**.</span></span>
1. <span data-ttu-id="4aa6b-109">**Satış siparişi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-109">Select **Sales order**.</span></span>
1. <span data-ttu-id="4aa6b-110">**Müşteri hesabı** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-110">In the **Customer account** field, type a value.</span></span>
    * <span data-ttu-id="4aa6b-111">Örnek: US-001</span><span class="sxs-lookup"><span data-stu-id="4aa6b-111">Example: US-001</span></span>  
1. <span data-ttu-id="4aa6b-112">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-112">Select **OK**.</span></span>
1. <span data-ttu-id="4aa6b-113">**Madde numarası** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-113">In the **Item number** field, type a value.</span></span>
    * <span data-ttu-id="4aa6b-114">Örnek: P6003</span><span class="sxs-lookup"><span data-stu-id="4aa6b-114">Example: P6003</span></span>  
1. <span data-ttu-id="4aa6b-115">**Miktar** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-115">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="4aa6b-116">Örnek: 50000</span><span class="sxs-lookup"><span data-stu-id="4aa6b-116">Example: 50000</span></span>  
1. <span data-ttu-id="4aa6b-117">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-117">Select **Save**.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="4aa6b-118">Ortak ürünler için malzeme planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="4aa6b-118">Create a material plan for co-products</span></span>

1. <span data-ttu-id="4aa6b-119">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-119">Close the page.</span></span>
1. <span data-ttu-id="4aa6b-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-120">Close the page.</span></span>
1. <span data-ttu-id="4aa6b-121">**Master planlama**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-121">Select **Master planning**.</span></span>
1. <span data-ttu-id="4aa6b-122">**Plan** alanında, aramayı açmak için açılır menü düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-122">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
1. <span data-ttu-id="4aa6b-123">Listeden, seçilen satırdaki bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-123">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="4aa6b-124">Örnek: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="4aa6b-124">Example: MasterPlan</span></span>  
1. <span data-ttu-id="4aa6b-125">**Çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-125">Select **Run**.</span></span>
1. <span data-ttu-id="4aa6b-126">**Eklenecek kayıtlar** bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-126">Expand or collapse the **Records to include** section.</span></span>
1. <span data-ttu-id="4aa6b-127">**Filtre**'yi seç.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-127">Select **Filter**.</span></span>
1. <span data-ttu-id="4aa6b-128">Listede, **Alan** =  *Madde numarası* satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-128">In the list, select the row for **Field** = *Item number*.</span></span>
1. <span data-ttu-id="4aa6b-129">**Ölçütler** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-129">In the **Criteria** field, type a value.</span></span>
    * <span data-ttu-id="4aa6b-130">Örnek: P6003</span><span class="sxs-lookup"><span data-stu-id="4aa6b-130">Example: P6003</span></span>  
1. <span data-ttu-id="4aa6b-131">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-131">Select **OK**.</span></span>
1. <span data-ttu-id="4aa6b-132">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-132">Select **OK**.</span></span>
1. <span data-ttu-id="4aa6b-133">**Planlı siparişler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-133">Select **Planned orders**.</span></span>
1. <span data-ttu-id="4aa6b-134">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-134">Use the Quick Filter to find records.</span></span> <span data-ttu-id="4aa6b-135">Örneğin, **Öğe numarası** alanını 'P6000' değeriyle filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-135">For example, filter on the **Item number** field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="4aa6b-136">Bir satış siparişi oluşturduğunuz maddeyi, ortak ürün olarak içeren formül maddesine göre filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-136">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
1. <span data-ttu-id="4aa6b-137">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="4aa6b-138">Filtre tarafından geri getirilen satırlardan herhangi birini seçin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-138">Select any of the rows returned by the filter.</span></span>  
1. <span data-ttu-id="4aa6b-139">Listeden, seçilen satırdaki bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-139">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="4aa6b-140">**İlişkilendirme** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-140">Expand the **Pegging** section.</span></span>
1. <span data-ttu-id="4aa6b-141">Listeden, seçilen satırdaki bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-141">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="4aa6b-142">Planlı sipariş, ortak ürünün satış siparişine ilişkilendirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-142">The planned order is pegged to the sales order for the co-product.</span></span>  
1. <span data-ttu-id="4aa6b-143">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-143">Close the page.</span></span>

## <a name="create-a-second-requirement-for-a-co-product"></a><span data-ttu-id="4aa6b-144">Ortak bir ürün için ikinci bir gereksinim oluşturma</span><span class="sxs-lookup"><span data-stu-id="4aa6b-144">Create a second requirement for a co-product</span></span>

1. <span data-ttu-id="4aa6b-145">**Satış ve pazarlama \> Çalışma alanları \> Satış siparişi işleme ve sorgulama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-145">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="4aa6b-146">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-146">Select **New**.</span></span>
1. <span data-ttu-id="4aa6b-147">**Satış siparişi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-147">Select **Sales order**.</span></span>
1. <span data-ttu-id="4aa6b-148">**Müşteri hesabı** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-148">In the **Customer account** field, type a value.</span></span>
    * <span data-ttu-id="4aa6b-149">Örnek: US-001</span><span class="sxs-lookup"><span data-stu-id="4aa6b-149">Example: US-001</span></span>  
1. <span data-ttu-id="4aa6b-150">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-150">Select **OK**.</span></span>
1. <span data-ttu-id="4aa6b-151">**Madde numarası** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-151">In the **Item number** field, type a value.</span></span>
    * <span data-ttu-id="4aa6b-152">Örnek: P6003</span><span class="sxs-lookup"><span data-stu-id="4aa6b-152">Example: P6003</span></span>  
1. <span data-ttu-id="4aa6b-153">**Miktar** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-153">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="4aa6b-154">Örnek: 50000</span><span class="sxs-lookup"><span data-stu-id="4aa6b-154">Example: 50000</span></span>  
1. <span data-ttu-id="4aa6b-155">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-155">Select **Save**.</span></span>

## <a name="create-a-second-material-plan-for-co-products"></a><span data-ttu-id="4aa6b-156">Ortak ürünler için ikinci bir malzeme planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="4aa6b-156">Create a second material plan for co-products</span></span>

1. <span data-ttu-id="4aa6b-157">**Plan** alanında, aramayı açmak için açılır menü düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-157">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="4aa6b-158">Listeden, seçilen satırdaki bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-158">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="4aa6b-159">Örnek: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="4aa6b-159">Example: MasterPlan</span></span>  
3. <span data-ttu-id="4aa6b-160">**Çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-160">Select **Run**.</span></span>
4. <span data-ttu-id="4aa6b-161">**Eklenecek kayıtlar** bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-161">Expand or collapse the **Records to include** section.</span></span>
5. <span data-ttu-id="4aa6b-162">**Filtre**'yi seç.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-162">Select **Filter**.</span></span>
6. <span data-ttu-id="4aa6b-163">Listede, **Alan** =  *Madde numarası* satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-163">In the list, select the row for **Field** = *Item number*.</span></span>
7. <span data-ttu-id="4aa6b-164">*Ölçütler* alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-164">In the *Criteria* field, type a value.</span></span>
    * <span data-ttu-id="4aa6b-165">Örnek: P6003</span><span class="sxs-lookup"><span data-stu-id="4aa6b-165">Example: P6003</span></span>  
8. <span data-ttu-id="4aa6b-166">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-166">Select **OK**.</span></span>
9. <span data-ttu-id="4aa6b-167">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-167">Select **OK**.</span></span>
10. <span data-ttu-id="4aa6b-168">**Planlı siparişler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-168">Select **Planned orders**.</span></span>
11. <span data-ttu-id="4aa6b-169">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-169">Use the Quick Filter to find records.</span></span> <span data-ttu-id="4aa6b-170">Örneğin, **Öğe numarası** alanını 'P6000' değeriyle filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-170">For example, filter on the **Item number** field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="4aa6b-171">Bir satış siparişi oluşturduğunuz maddeyi, ortak ürün olarak içeren formül maddesine göre filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-171">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="4aa6b-172">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-172">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="4aa6b-173">Filtre tarafından geri getirilen satırlardan herhangi birini seçin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-173">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="4aa6b-174">Listeden, seçilen satırdaki bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-174">In the list, select the link in the selected row.</span></span>
14. <span data-ttu-id="4aa6b-175">**İlişkilendirme** bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-175">Expand or collapse the **Pegging** section.</span></span>
15. <span data-ttu-id="4aa6b-176">Listeden, seçilen satırdaki bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-176">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="4aa6b-177">Planlı sipariş, ortak ürünün satış siparişine ilişkilendirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-177">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="4aa6b-178">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-178">Close the page.</span></span>
17. <span data-ttu-id="4aa6b-179">**Master planlama**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-179">Select **Master planning**.</span></span>
18. <span data-ttu-id="4aa6b-180">**Master planlama \> Kurulum \> Master planlama parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-180">Go to **Master planning \> Setup \> Master planning parameters**.</span></span>
19. <span data-ttu-id="4aa6b-181">**Tüm planlama işlemlerini devre dışı bırak** alanında *Hayır*'ı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-181">Select *No* in the **Disable all planning processes** field.</span></span>
20. <span data-ttu-id="4aa6b-182">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4aa6b-182">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]