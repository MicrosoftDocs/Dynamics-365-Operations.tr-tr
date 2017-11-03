---
title: "Ambar iş ilkeleri"
description: "Ambar işi ilkeleri ambar işinin üretimdeki ambar işlemleri tarafından oluşturulup oluşturulmadığını, iş emri türüne, stok yerleşimine ve ürüne dayanarak kontrol eder."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 196561
ms.assetid: cbf48ec6-1836-48d5-ad66-a9b534af1786
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 83e8dc76350e0d40a392e9a04ddca5b4b45d0da0
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="warehouse-work-policies"></a><span data-ttu-id="2ae47-103">Ambar iş ilkeleri</span><span class="sxs-lookup"><span data-stu-id="2ae47-103">Warehouse work policies</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="2ae47-104">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition'daki ambar işi ilkeleri ambar işinin üretimdeki ambar işlemleri tarafından oluşturulup oluşturulmadığını, iş emri türüne, stok yerleşimine ve ürüne dayanarak kontrol eder.</span><span class="sxs-lookup"><span data-stu-id="2ae47-104">Warehouse work policies in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition control whether warehouse work is created by warehouse processes in manufacturing, based on work order type, inventory location, and product.</span></span>

<span data-ttu-id="2ae47-105">Bu iş ilkesi ambar işinin üretimdeki ambar işlemleri için oluşturulup oluşturulmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="2ae47-105">This work policy controls whether warehouse work is created for warehouse processes in manufacturing.</span></span> <span data-ttu-id="2ae47-106">**İş emri türleri**, bir **stok konumu** ve bir **ürün** birleşimini kullanarak iş ilkesini ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ae47-106">You can set up the work policy by using a combination of **work order types**, an **inventory location**, and a **product**.</span></span> <span data-ttu-id="2ae47-107">Örneğin, L0101 numaralı ürün 001 numaralı çıktı konumuna tamamlandı olarak bildirilir.</span><span class="sxs-lookup"><span data-stu-id="2ae47-107">For example, product L0101 is reported as finished to output location 001.</span></span> <span data-ttu-id="2ae47-108">Bunun üzerine, tamamlanan mal 001 numaralı çıktı konumundaki başka bir üretim emrinde tüketilir.</span><span class="sxs-lookup"><span data-stu-id="2ae47-108">The finished good is later consumed in another production order at output location 001.</span></span> <span data-ttu-id="2ae47-109">Bu durumda, L0101 numaralı ürünü 001 numaralı çıktı konumuna tamamlandı olarak bildirdiğiniz zaman mamul mallara yönelik işin oluşturulmasını önlemek için bir iş ilkesi ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ae47-109">In this case, you can set up a work policy to prevent the work for finished goods put-away from being created when you report product L0101 as finished to output location 001.</span></span> <span data-ttu-id="2ae47-110">İş ilkesi, aşağıdaki bilgilerle açıklanabilen ayrı bir varlıktır:</span><span class="sxs-lookup"><span data-stu-id="2ae47-110">The work policy is an individual entity that can be described through the following information:</span></span>

-   <span data-ttu-id="2ae47-111">**İş ilkesi adı**(iş ilkesinin benzersiz tanımlayıcısı)</span><span class="sxs-lookup"><span data-stu-id="2ae47-111">**Work policy name** (the unique identifier of the work policy)</span></span>
-   <span data-ttu-id="2ae47-112">**İş emri türleri** ve **İş oluşturma yöntemi**</span><span class="sxs-lookup"><span data-stu-id="2ae47-112">**Work order types** and **Work creation method**</span></span>
-   <span data-ttu-id="2ae47-113">**Stok konumları**</span><span class="sxs-lookup"><span data-stu-id="2ae47-113">**Inventory locations**</span></span>
-   <span data-ttu-id="2ae47-114">**Ürünler**</span><span class="sxs-lookup"><span data-stu-id="2ae47-114">**Products**</span></span>

## <a name="work-order-types"></a><span data-ttu-id="2ae47-115">İş emri türleri</span><span class="sxs-lookup"><span data-stu-id="2ae47-115">Work order types</span></span>
<span data-ttu-id="2ae47-116">Aşağıdaki iş emri türlerini seçebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="2ae47-116">You can select the following work order types:</span></span>

-   <span data-ttu-id="2ae47-117">Yerine konan mamul mallar</span><span class="sxs-lookup"><span data-stu-id="2ae47-117">Finished goods put away</span></span>
-   <span data-ttu-id="2ae47-118">Yerine konan ortak ürün ve yan ürün</span><span class="sxs-lookup"><span data-stu-id="2ae47-118">Co-product and by-product put away</span></span>
-   <span data-ttu-id="2ae47-119">Hammadde çekme</span><span class="sxs-lookup"><span data-stu-id="2ae47-119">Raw material picking</span></span>

<span data-ttu-id="2ae47-120">**İş oluşturma yöntemi** alanı **Asla** değerine sahiptir.</span><span class="sxs-lookup"><span data-stu-id="2ae47-120">The **Work creation method** field has the value **Never**.</span></span> <span data-ttu-id="2ae47-121">Bu değer iş ilkesinin seçili iş emri türü için ambar işinin oluşturulmasını önleyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ae47-121">This value indicates that the work policy will prevent warehouse work from being created for the selected work order type.</span></span>

## <a name="inventory-locations"></a><span data-ttu-id="2ae47-122">Stok konumları</span><span class="sxs-lookup"><span data-stu-id="2ae47-122">Inventory locations</span></span>
<span data-ttu-id="2ae47-123">İş ilkesinin geçerli olduğu bir konum seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ae47-123">You can select a location that the work policy applies to.</span></span> <span data-ttu-id="2ae47-124">İş ilkesi ile ilişkilendirilmiş bir konum yoksa iş ilkesi herhangi bir işleme uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="2ae47-124">If no location is associated with a work policy, the work policy doesn’t apply to any processes.</span></span> <span data-ttu-id="2ae47-125">**Konumlar** sayfasında, belirli bir konum için iş ilkesi seçimini yapabilir veya iptal edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ae47-125">On the **Locations** page, you can also select or cancel the selection of the work policy for a specific location.</span></span>

## <a name="products"></a><span data-ttu-id="2ae47-126">Ürünler</span><span class="sxs-lookup"><span data-stu-id="2ae47-126">Products</span></span>
<span data-ttu-id="2ae47-127">İş ilkesinin geçerli olduğu bir ürün seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ae47-127">You can select a product that the work policy applies to.</span></span> <span data-ttu-id="2ae47-128">İş ilkesini tüm ürünlere veya seçili ürünlere uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ae47-128">You can apply the work policy to either all products or selected products.</span></span>

## <a name="example"></a><span data-ttu-id="2ae47-129">Örnek</span><span class="sxs-lookup"><span data-stu-id="2ae47-129">Example</span></span>
<span data-ttu-id="2ae47-130">Aşağıdaki örnekte, PRD-001 ve PRD-00*2* olmak üzere iki üretim emri bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="2ae47-130">In the following example, there are two production orders, PRD-001 and PRD-00*2*.</span></span> <span data-ttu-id="2ae47-131">Üretim emri PRD-001, SC1 ürününün O1 konumuna tamamlandı olarak bildirildiği **Derleme** adlı bir işleme sahiptir.</span><span class="sxs-lookup"><span data-stu-id="2ae47-131">Production order PRD-001 has an operation that is named **Assembly**, where product SC1 is being reported as finished to location O1.</span></span> <span data-ttu-id="2ae47-132">Üretim emri PRD-002 **Boyama** adlı bir işleme sahiptir ve O1 konumundan SC1 ürününü kullanır.</span><span class="sxs-lookup"><span data-stu-id="2ae47-132">Production order PRD-002 has an operation that is named **Painting** and consumes product SC1 from location O1.</span></span> <span data-ttu-id="2ae47-133">Üretim emri PRD-002 ayrıca O1 konumundan RM1 hammaddesini de kullanır.</span><span class="sxs-lookup"><span data-stu-id="2ae47-133">Production order PRD-002 also consumes raw material RM1 from location O1.</span></span> <span data-ttu-id="2ae47-134">RM1, BULK-001 ambar konumunda depolanır ve hammadde çekme işlemi için ambar işi tarafından O1 konumuna çekilir.</span><span class="sxs-lookup"><span data-stu-id="2ae47-134">RM1 is stored in warehouse location BULK-001 and will be picked to location O1 by warehouse work for raw material picking.</span></span> <span data-ttu-id="2ae47-135">Malzeme çekme işi PRD-002 üretimi serbest bırakıldığında oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2ae47-135">The picking work is generated when production PRD-002 is released.</span></span> 

<span data-ttu-id="2ae47-136">[![Ambar iş ilkeleri](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span><span class="sxs-lookup"><span data-stu-id="2ae47-136">[![Warehouse work policies](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span></span> 

<span data-ttu-id="2ae47-137">Bu senaryo için bir ambar işi ilkesi yapılandırmayı planlarken, aşağıdaki bilgileri göz önünde bulundurmalısınız:</span><span class="sxs-lookup"><span data-stu-id="2ae47-137">When you plan to configure a warehouse work policy for this scenario, you should consider the following information:</span></span>

-   <span data-ttu-id="2ae47-138">Yerine konan mamul mallar için ambar işi, SC1 ürününü PRD-001 üretim emrinden O1 konumuna tamamlandı olarak bildirdiğinizde gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="2ae47-138">Warehouse work for finished goods put-away isn’t required when you report product SC1 as finished from production order PRD-001 to location O1.</span></span> <span data-ttu-id="2ae47-139">Bunun nedeni PRD-002 üretim emrinin **Boyama** işleminin SC1 ürününü aynı konumda kullanmasıdır.</span><span class="sxs-lookup"><span data-stu-id="2ae47-139">This is because the **Painting** operation for production order PRD-002 consumes SC1 at the same location.</span></span>
-   <span data-ttu-id="2ae47-140">Hammadde çekme için ambar işi RM1 hammaddesini BULK-001 ambar konumundan O1 konumuna taşımak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2ae47-140">Warehouse work for raw material picking is required in order to move raw material RM1 from warehouse location BULK-001 to location O1.</span></span>

<span data-ttu-id="2ae47-141">Bu noktalara göre, ayarlayabileceğiniz iş ilkesine bir örneği aşağıda bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ae47-141">Here is an example of the work policy that you can set up, based on these considerations.</span></span>

|                                         |                                                       |
|-----------------------------------------|-------------------------------------------------------|
|<span data-ttu-id="2ae47-142">**İş ilkesi adı**</span><span class="sxs-lookup"><span data-stu-id="2ae47-142">**Work policy name**</span></span><br>                 |<span data-ttu-id="2ae47-143">**İş emri türleri**</span><span class="sxs-lookup"><span data-stu-id="2ae47-143">**Work order types**</span></span><br>                               |
| <span data-ttu-id="2ae47-144">Yerine koyma yok - 01     \`</span><span class="sxs-lookup"><span data-stu-id="2ae47-144">No put away 01     \`</span></span>                    |<span data-ttu-id="2ae47-145">- Mamul ürünü yerine koy</span><span class="sxs-lookup"><span data-stu-id="2ae47-145">- Finished good put away</span></span><br>                           |
|                                         |<span data-ttu-id="2ae47-146">**Yerleşimler**</span><span class="sxs-lookup"><span data-stu-id="2ae47-146">**Locations**</span></span><br>                                      |
|                                         |<span data-ttu-id="2ae47-147">- O1</span><span class="sxs-lookup"><span data-stu-id="2ae47-147">- O1</span></span>   |                                               |
|                                         |<span data-ttu-id="2ae47-148">**Ürünler**</span><span class="sxs-lookup"><span data-stu-id="2ae47-148">**Products**</span></span> <br>                                      |
|                                         |<span data-ttu-id="2ae47-149">- SC1</span><span class="sxs-lookup"><span data-stu-id="2ae47-149">- SC1</span></span>                                                  |

<span data-ttu-id="2ae47-150">Aşağıdaki yordamlar bu senaryo için ambar iş ilkesini ayarlama konusunda adım adım yönergeler sağlar.</span><span class="sxs-lookup"><span data-stu-id="2ae47-150">The following procedures provide step-by-step instructions about how to set up the warehouse work policy for this scenario.</span></span> <span data-ttu-id="2ae47-151">Bir üretim emrinin plaka denetimli olmayan bir konuma tamamlandı olarak nasıl bildirileceğini gösteren örnek bir kurulum da açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="2ae47-151">A sample setup showing how to report a production order as finished to a location that isn’t license plate–controlled is also described.</span></span>

## <a name="set-up-a-warehouse-work-policy"></a><span data-ttu-id="2ae47-152">Ambar iş ilkesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="2ae47-152">Set up a warehouse work policy</span></span>
<span data-ttu-id="2ae47-153">Ambar işlemi her zaman ambar çalışmasını içermezler.</span><span class="sxs-lookup"><span data-stu-id="2ae47-153">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="2ae47-154">Bir çalışma ilkesi tanımlayarak, hammadde çekme ve tamamlanmış malların yerine koyması işlerinin oluşturulmasını, çeşitli bir ürün dizisi veya belirtilen konumlar için engelleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ae47-154">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="2ae47-155">Bu yordamı oluşturmak için USMF demo verileri şirketi kullanılmıştır.</span><span class="sxs-lookup"><span data-stu-id="2ae47-155">The USMF demo data company was used to create this procedure.</span></span> 

<span data-ttu-id="2ae47-156">ADIMLAR (21)</span><span class="sxs-lookup"><span data-stu-id="2ae47-156">STEPS (21)</span></span>

|     |                                                                            |
|-----|----------------------------------------------------------------------------|
| <span data-ttu-id="2ae47-157">1.</span><span class="sxs-lookup"><span data-stu-id="2ae47-157">1.</span></span>  | <span data-ttu-id="2ae47-158">Ambar Yönetimi &gt; Kurulum &gt; İş &gt; İş ilkeleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="2ae47-158">Go to Warehouse management &gt; Setup &gt; Work &gt; Work policies.</span></span>        |
| <span data-ttu-id="2ae47-159">2.</span><span class="sxs-lookup"><span data-stu-id="2ae47-159">2.</span></span>  | <span data-ttu-id="2ae47-160">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ae47-160">Click New.</span></span>                                                                 |
| <span data-ttu-id="2ae47-161">3.</span><span class="sxs-lookup"><span data-stu-id="2ae47-161">3.</span></span>  | <span data-ttu-id="2ae47-162">Çalışma ilkesi ad alanına 'Hiçbir yerine koyma çalışma' yazın.</span><span class="sxs-lookup"><span data-stu-id="2ae47-162">In the Work policy name field, type 'No put-away work'.</span></span>                    |
| <span data-ttu-id="2ae47-163">4.</span><span class="sxs-lookup"><span data-stu-id="2ae47-163">4.</span></span>  | <span data-ttu-id="2ae47-164">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ae47-164">Click Save.</span></span>                                                                |
| <span data-ttu-id="2ae47-165">5.</span><span class="sxs-lookup"><span data-stu-id="2ae47-165">5.</span></span>  | <span data-ttu-id="2ae47-166">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ae47-166">Click Add.</span></span>                                                                 |
| <span data-ttu-id="2ae47-167">6.</span><span class="sxs-lookup"><span data-stu-id="2ae47-167">6.</span></span>  | <span data-ttu-id="2ae47-168">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="2ae47-168">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="2ae47-169">7.</span><span class="sxs-lookup"><span data-stu-id="2ae47-169">7.</span></span>  | <span data-ttu-id="2ae47-170">İş siparişi türü alanına, 'Mamul mallar yerine koyma' seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="2ae47-170">In the Work order type field, select 'Finished goods put away'.</span></span>            |
| <span data-ttu-id="2ae47-171">8.</span><span class="sxs-lookup"><span data-stu-id="2ae47-171">8.</span></span>  | <span data-ttu-id="2ae47-172">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ae47-172">Click Add.</span></span>                                                                 |
| <span data-ttu-id="2ae47-173">9.</span><span class="sxs-lookup"><span data-stu-id="2ae47-173">9.</span></span>  | <span data-ttu-id="2ae47-174">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="2ae47-174">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="2ae47-175">10.</span><span class="sxs-lookup"><span data-stu-id="2ae47-175">10.</span></span> | <span data-ttu-id="2ae47-176">İş emri türü alanında, "Ortak ürün ve yan ürün yerine koyma" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="2ae47-176">In the Work order type field, select 'Co-product and by-product put away'.</span></span> |
| <span data-ttu-id="2ae47-177">11.</span><span class="sxs-lookup"><span data-stu-id="2ae47-177">11.</span></span> | <span data-ttu-id="2ae47-178">Stok konumları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="2ae47-178">Expand the Inventory locations section.</span></span>                                    |
| <span data-ttu-id="2ae47-179">12.</span><span class="sxs-lookup"><span data-stu-id="2ae47-179">12.</span></span> | <span data-ttu-id="2ae47-180">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ae47-180">Click Add.</span></span>                                                                 |
| <span data-ttu-id="2ae47-181">13.</span><span class="sxs-lookup"><span data-stu-id="2ae47-181">13.</span></span> | <span data-ttu-id="2ae47-182">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="2ae47-182">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="2ae47-183">14.</span><span class="sxs-lookup"><span data-stu-id="2ae47-183">14.</span></span> | <span data-ttu-id="2ae47-184">Ambar listesinde '51' girin.</span><span class="sxs-lookup"><span data-stu-id="2ae47-184">In the Warehouse list, enter '51'.</span></span>                                         |
| <span data-ttu-id="2ae47-185">15.</span><span class="sxs-lookup"><span data-stu-id="2ae47-185">15.</span></span> | <span data-ttu-id="2ae47-186">Konum alanına bir '001' girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="2ae47-186">In the Location field, enter or select '001'.</span></span>                              |
| <span data-ttu-id="2ae47-187">16.</span><span class="sxs-lookup"><span data-stu-id="2ae47-187">16.</span></span> | <span data-ttu-id="2ae47-188">Ürünler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="2ae47-188">Expand the Products section.</span></span>                                               |
| <span data-ttu-id="2ae47-189">17.</span><span class="sxs-lookup"><span data-stu-id="2ae47-189">17.</span></span> | <span data-ttu-id="2ae47-190">Ürün seçimi alanında, 'Seçili'yi işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="2ae47-190">In the Product selection field, select 'Selected'.</span></span>                         |
| <span data-ttu-id="2ae47-191">18.</span><span class="sxs-lookup"><span data-stu-id="2ae47-191">18.</span></span> | <span data-ttu-id="2ae47-192">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ae47-192">Click Add.</span></span>                                                                 |
| <span data-ttu-id="2ae47-193">19.</span><span class="sxs-lookup"><span data-stu-id="2ae47-193">19.</span></span> | <span data-ttu-id="2ae47-194">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="2ae47-194">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="2ae47-195">20.</span><span class="sxs-lookup"><span data-stu-id="2ae47-195">20.</span></span> | <span data-ttu-id="2ae47-196">Madde numarası alanında 'L0101' girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="2ae47-196">In the Item number field, enter or select 'L0101'.</span></span>                         |
| <span data-ttu-id="2ae47-197">21.</span><span class="sxs-lookup"><span data-stu-id="2ae47-197">21.</span></span> | <span data-ttu-id="2ae47-198">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ae47-198">Click Save.</span></span>                                                                |

## <a name="report-a-production-order-as-finished-to-a-location-that-isnt-license-platecontrolled"></a><span data-ttu-id="2ae47-199">Üretim emrini plaka denetimli olmayan bir konuma tamamlandı olarak bildirme</span><span class="sxs-lookup"><span data-stu-id="2ae47-199">Report a production order as finished to a location that isn’t license plate–controlled</span></span>
<span data-ttu-id="2ae47-200">Bu yordamda, plaka kontrollü olmayan bir konumuna tamamlandı olarak raporlama yapılmasına ilişkin bir örnek gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="2ae47-200">This procedure shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="2ae47-201">Geçerli bir iş politikasının olması bu görev için bir ön koşuldur.</span><span class="sxs-lookup"><span data-stu-id="2ae47-201">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="2ae47-202">Önceki yordamda iş ilkesinin kurulumu gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="2ae47-202">The previous procedure shows the setup of the work policy.</span></span> 

<span data-ttu-id="2ae47-203">ADIMLAR (25)</span><span class="sxs-lookup"><span data-stu-id="2ae47-203">STEPS (25)</span></span>

<table>
<tbody>
<tr>
<td colspan="3"><span data-ttu-id="2ae47-204"><strong>Alt görev: Bir çıkış konumu ayarlayın.</strong></span><span class="sxs-lookup"><span data-stu-id="2ae47-204"><strong>Sub-task: Set up an output location.</strong></span></span></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td><span data-ttu-id="2ae47-205">Organizasyon yönetimi &gt; Kaynaklar &gt; Kaynak grupları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="2ae47-205">Go to Organization administration &gt; Resources &gt; Resource groups.</span></span></td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td><span data-ttu-id="2ae47-206">Listeden '5102' kaynak grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="2ae47-206">In the list, select resource group '5102'.</span></span></td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td><span data-ttu-id="2ae47-207">Düzenle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2ae47-207">Click Edit.</span></span></td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td><span data-ttu-id="2ae47-208">Çıkış ambarı alanına '51' girin.</span><span class="sxs-lookup"><span data-stu-id="2ae47-208">In the Output warehouse field, enter '51'.</span></span></td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td><span data-ttu-id="2ae47-209">Çıkış konumu alanına '001' girin.</span><span class="sxs-lookup"><span data-stu-id="2ae47-209">In the Output location field, enter '001'.</span></span></td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td><span data-ttu-id="2ae47-210">Konum 001, plaka kontrollü bir konum değildir.</span><span class="sxs-lookup"><span data-stu-id="2ae47-210">Location 001 isn't a license plate–controlled location.</span></span> <span data-ttu-id="2ae47-211">Konum için geçerli bir çalışma politikası bulunuyorsa sadece, plaka dışı bir çıkış konumu ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ae47-211">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span></td>
</tr>
<tr>
<td colspan="3"><span data-ttu-id="2ae47-212"><strong>Alt görev: Bir üretim emri oluşturun ve bunu tamamlandı olarak rapor edin.</strong></span><span class="sxs-lookup"><span data-stu-id="2ae47-212"><strong>Sub-task: Create a production order and report it as finished.</strong></span></span></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td><span data-ttu-id="2ae47-213">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="2ae47-213">Close the page.</span></span></td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td><span data-ttu-id="2ae47-214">Üretim denetimi &gt; Üretim emirleri &gt; Tüm üretim emirleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="2ae47-214">Go to Production control &gt; Production orders &gt; All production orders.</span></span></td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td><span data-ttu-id="2ae47-215">Yeni üretim emri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ae47-215">Click New production order.</span></span></td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td><span data-ttu-id="2ae47-216">Madde numarası alanına 'L0101' girin.</span><span class="sxs-lookup"><span data-stu-id="2ae47-216">In the Item number field, enter 'L0101'.</span></span></td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td><span data-ttu-id="2ae47-217">Oluştur öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ae47-217">Click Create.</span></span></td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td><span data-ttu-id="2ae47-218">Eylem Bölmesinde Üretime emri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ae47-218">On the Action Pane, click Production order.</span></span></td>
</tr>
<tr>
<td></td>
<td>7.</td>
<td><span data-ttu-id="2ae47-219">Tahmin seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ae47-219">Click Estimate.</span></span></td>
</tr>
<tr>
<td></td>
<td>8.</td>
<td><span data-ttu-id="2ae47-220">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2ae47-220">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>9.</td>
<td><span data-ttu-id="2ae47-221">Başlat'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ae47-221">Click Start.</span></span></td>
</tr>
<tr>
<td></td>
<td>10.</td>
<td><span data-ttu-id="2ae47-222">Genel sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2ae47-222">Click the General tab.</span></span></td>
</tr>
<tr>
<td></td>
<td>11.</td>
<td><span data-ttu-id="2ae47-223">Otomatik malzeme listesi tüketimi alanında, 'Hiçbir zaman' seçin.</span><span class="sxs-lookup"><span data-stu-id="2ae47-223">In the Automatic BOM consumption field, select 'Never'.</span></span></td>
</tr>
<tr>
<td></td>
<td>12.</td>
<td><span data-ttu-id="2ae47-224">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2ae47-224">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>13.</td>
<td><span data-ttu-id="2ae47-225">Tamamlandı olarak bildir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2ae47-225">Click Report as finished.</span></span></td>
</tr>
<tr>
<td></td>
<td>14.</td>
<td><span data-ttu-id="2ae47-226">Genel sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2ae47-226">Click the General tab.</span></span></td>
</tr>
<tr>
<td></td>
<td>15.</td>
<td><span data-ttu-id="2ae47-227">Kabul hatası alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2ae47-227">Select Yes in the Accept error field.</span></span></td>
</tr>
<tr>
<td></td>
<td>16.</td>
<td><span data-ttu-id="2ae47-228">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2ae47-228">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>17.</td>
<td><span data-ttu-id="2ae47-229">Eylem Bölmesinde, Ambar öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ae47-229">On the Action Pane, click Warehouse.</span></span></td>
</tr>
<tr>
<td></td>
<td>18.</td>
<td><span data-ttu-id="2ae47-230">İş ayrıntıları öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2ae47-230">Click Work details.</span></span></td>
</tr>
<tr>
<td></td>
<td>19.</td>
<td><span data-ttu-id="2ae47-231">Üretim emri, tamamlandı olarak rapor edilmişse, hiçbir iş üretilmez.</span><span class="sxs-lookup"><span data-stu-id="2ae47-231">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="2ae47-232">Bu durum, Ürün L0101, konum 001'e bitirildi olarak rapor edildiğinde işin oluşturulmasının engellenmesi için tanımlanan bir iş politikası bulunmasından kaynaklanır.</span><span class="sxs-lookup"><span data-stu-id="2ae47-232">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span></td>
</tr>
</tbody>
</table>




