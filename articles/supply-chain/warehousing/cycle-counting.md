---
title: "Döngü sayımı"
description: "Bu makalede, sayım döngüsünü Ambar yönetiminde bulunan ambar çözümü ile birlikte nasıl kullanabileceğiniz açıklanmaktadır. Bu makale, Stok yönetiminde bulunan ambar çözümü için geçerli değildir."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSCycleCountThreshold, WHSWorkTableListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 50671
ms.assetid: 49f5c431-b043-4170-aa24-b7d5d1ee063e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ddb035eaa496a7c84f117f0523d509eccdf58505
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="cycle-counting"></a><span data-ttu-id="c6a20-104">Döngü sayımı</span><span class="sxs-lookup"><span data-stu-id="c6a20-104">Cycle counting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c6a20-105">Bu makalede, sayım döngüsünü Ambar yönetiminde bulunan ambar çözümü ile birlikte nasıl kullanabileceğiniz açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="c6a20-105">This article describes how you can use cycle counting with the warehousing solution that is available in Warehouse management.</span></span> <span data-ttu-id="c6a20-106">Bu makale, Stok yönetiminde bulunan ambar çözümü için geçerli değildir.</span><span class="sxs-lookup"><span data-stu-id="c6a20-106">This article doesn't apply to the warehousing solution that's available in Inventory management.</span></span>

<span data-ttu-id="c6a20-107">Döngü sayımı eldeki stok maddelerini denetlemek için kullanabileceğiniz bir ambar işlemidir.</span><span class="sxs-lookup"><span data-stu-id="c6a20-107">Cycle counting is a warehouse process that you can use to audit on-hand inventory items.</span></span> <span data-ttu-id="c6a20-108">Döngü sayım işlemi üç adımda açıklanabilir:</span><span class="sxs-lookup"><span data-stu-id="c6a20-108">The cycle counting process can be described in three steps:</span></span>

1.  <span data-ttu-id="c6a20-109">**Döngü sayım işi oluşturma** – Döngü sayım işi, maddeler için eşik parametrelerine dayalı olarak veya bir döngü sayım planı kullanılarak otomatik olarak oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="c6a20-109">**Create cycle counting work** – Cycle counting work can be created automatically, based on threshold parameters for items or by using a cycle counting plan.</span></span> <span data-ttu-id="c6a20-110">Alternatif olarak, **Maddeye göre döngü sayım işi** sayfası veya **Konuma göre döngü sayım işi** sayfasındaki madde veya ambar parametrelerini kullanarak döngü sayım işini el ile de oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c6a20-110">Alternatively, you can manually create cycle counting work by using the item or warehouse parameters on the **Cycle count work by item** page or the **Cycle count work by location** page.</span></span>
2.  <span data-ttu-id="c6a20-111">**Döngü sayımını işleme** – Döngü sayım işi oluşturduktan sonra, döngü sayım işini bir ambar konumundaki maddeleri sayıp sonucu bir mobil cihaz kullanarak Microsoft Dynamics 365 for Finance and Operations'a girerek gerçekleştirirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c6a20-111">**Process the cycle count** – After cycle counting work is created, you do the cycle counting work by counting items in a warehouse location and then using a mobile device to enter the result in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="c6a20-112">Alternatif olarak, döngü sayım işi oluşturmadan bir ambar konumundaki maddeleri sayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c6a20-112">Alternatively, you can count items in a warehouse location without creating cycle counting work.</span></span> <span data-ttu-id="c6a20-113">Bu süreç, *nokta döngü sayımı* olarak bilinmektedir.</span><span class="sxs-lookup"><span data-stu-id="c6a20-113">This process is referred to as *spot cycle counting*.</span></span>
3.  <span data-ttu-id="c6a20-114">**Sayılan değerdeki farkları düzeltme** – Bir döngü sayımından sonra, sayılan değerde farklılık olan tüm maddeler **Tüm işler** sayfasında **Gözden geçirilmeyi bekliyor** şeklinde bir iş durumuna sahip olacaktır.</span><span class="sxs-lookup"><span data-stu-id="c6a20-114">**Resolve differences in the counted value** – After a cycle count, any items that have differences in the counted value will have a work status of **Pending review** on the **All work** page.</span></span> <span data-ttu-id="c6a20-115">Bu farkları **Gözden geçirilmeyi bekleyen döngü sayım işi** sayfasında düzeltebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c6a20-115">You can resolve these differences on the **Cycle count work pending review** page.</span></span>

<span data-ttu-id="c6a20-116">Aşağıdaki çizimde döngü sayım işlemi gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="c6a20-116">The following illustration shows the cycle counting process.</span></span> ![Döngü sayımı için süreç akışı](./media/performcyclecountinginawarehouselocation.jpg)

## <a name="cycle-counting-prerequisites"></a><span data-ttu-id="c6a20-118">Döngü sayım öngereklilikleri</span><span class="sxs-lookup"><span data-stu-id="c6a20-118">Cycle counting prerequisites</span></span>
<span data-ttu-id="c6a20-119">Aşağıdaki tabloda, döngü sayımını kullanmadan önce yerine getirilmesi gereken öngereklilikler gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="c6a20-119">The following table shows the prerequisites that must be in place before you can use cycle counting.</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c6a20-120">Önkoşul</span><span class="sxs-lookup"><span data-stu-id="c6a20-120">Prerequisite</span></span></th>
<th><span data-ttu-id="c6a20-121">Açıklama</span><span class="sxs-lookup"><span data-stu-id="c6a20-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c6a20-122">Madde</span><span class="sxs-lookup"><span data-stu-id="c6a20-122">Item</span></span></td>
<td><span data-ttu-id="c6a20-123">Madde mutlaka ambar yönetimi süreçleri için etkinleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="c6a20-123">The item must be enabled for warehouse management processes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6a20-124">Ambar</span><span class="sxs-lookup"><span data-stu-id="c6a20-124">Warehouse</span></span></td>
<td><span data-ttu-id="c6a20-125">Ambar mutlaka ambar yönetimi süreçleri için etkinleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="c6a20-125">The warehouse must be enabled for warehouse management processes.</span></span> <span data-ttu-id="c6a20-126">Ambarı ambar yönetim süreçleri için etkinleştirmek üzere, <strong>Ambarlar</strong> sayfasında ambarı seçin, ardından <strong>Ambar yönetim süreçlerini kullan</strong> seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="c6a20-126">To enable the warehouse for warehouse management processes, on the <strong>Warehouses</strong> page, select the warehouse, and then select the <strong>Use warehouse management processes</strong> option.</span></span> <span data-ttu-id="c6a20-127">Bir döngü sayımı sırasında işçilerin paletleri taşımasına imkan vermek için, <strong>Ambar yönetimi</strong> FastTab'inde <strong>Paletlerin döngü sayımı sırasında taşınmasına izin ver</strong> seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="c6a20-127">To enable workers to move pallets during a cycle count, on the <strong>Warehouse management</strong> FastTab, select the <strong>Allow pallet moves during cycle counting</strong> option.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6a20-128">İş havuzları</span><span class="sxs-lookup"><span data-stu-id="c6a20-128">Work pools</span></span></td>
<td><span data-ttu-id="c6a20-129">İsteğe bağlı: Ambar işini iş türüne göre ayrıştırmak için bir iş havuzu oluşturun (bu durumda, döngü sayım işi).</span><span class="sxs-lookup"><span data-stu-id="c6a20-129">Optional: Create a work pool to segregate the warehouse work, based on the type of work (in this case, cycle counting work).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6a20-130">Konumlar</span><span class="sxs-lookup"><span data-stu-id="c6a20-130">Locations</span></span></td>
<td><span data-ttu-id="c6a20-131">Konumlar için döngü sayımını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="c6a20-131">Enable cycle counting for locations.</span></span> <span data-ttu-id="c6a20-132">Bir ambar konumu için döngü sayımına izin vermek üzere, <strong>Konum profilleri</strong> sayfasında <strong>Döngü sayımına izin ver</strong> seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="c6a20-132">To enable cycle counting for a warehouse location, on the <strong>Location profiles</strong> page, select the <strong>Allow cycle counting</strong> option.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6a20-133">Ambar yönetim parametreleri</span><span class="sxs-lookup"><span data-stu-id="c6a20-133">Warehouse management parameters</span></span></td>
<td><span data-ttu-id="c6a20-134">Döngü sayımı için parametreleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c6a20-134">Set up parameters for cycle counting.</span></span> <span data-ttu-id="c6a20-135"><strong>Ambar yönetim parametreleri</strong> sayfasında, döngü sayımı için varsayılan ayar türü kodunu, iş sınıfı kimliğini ve iş önceliğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="c6a20-135">On the <strong>Warehouse management parameters</strong> page, specify the default adjustment type code, work class ID, and work priority for cycle counting.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6a20-136">Mobil cihaz</span><span class="sxs-lookup"><span data-stu-id="c6a20-136">Mobile device</span></span></td>
<td><ul>
<li><span data-ttu-id="c6a20-137">Aşağıdaki yöntemlerden biri için <strong>Mobil cihaz menü öğeleri</strong> sayfasında bir menü öğesi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="c6a20-137">Create a menu item for one of the following methods on the <strong>Mobile device menu items</strong> page:</span></span>
<ul>
<li><span data-ttu-id="c6a20-138">Kullanıcı tarafından yönlendirilen döngü sayımı</span><span class="sxs-lookup"><span data-stu-id="c6a20-138">User directed cycle counting</span></span></li>
<li><span data-ttu-id="c6a20-139">Sistem tarafından yönlendirilen döngü sayımı</span><span class="sxs-lookup"><span data-stu-id="c6a20-139">System directed cycle counting</span></span></li>
<li><span data-ttu-id="c6a20-140">Döngü sayımı gruplandırma</span><span class="sxs-lookup"><span data-stu-id="c6a20-140">Cycle count grouping</span></span></li>
<li><span data-ttu-id="c6a20-141">Nokta döngü sayımı</span><span class="sxs-lookup"><span data-stu-id="c6a20-141">Spot cycle counting</span></span></li>
</ul>
</li>
<li><span data-ttu-id="c6a20-142">Mobil aygıt için bir menü oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c6a20-142">Set up a menu for the mobile device.</span></span></li>
<li><span data-ttu-id="c6a20-143">Bir iş kullanıcı hesabı oluşturun ve iş kullanıcı kimliğine bir mobil cihaz menüsü atayın.</span><span class="sxs-lookup"><span data-stu-id="c6a20-143">Create a work user account, and assign a mobile device menu to the work user ID.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6a20-144">İlgili kurulum görevi</span><span class="sxs-lookup"><span data-stu-id="c6a20-144">Related setup task</span></span></td>
<td><span data-ttu-id="c6a20-145">Bir ambar konumu için bir döngü sayımı planı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c6a20-145">Set up a cycle counting plan for a warehouse location.</span></span></td>
</tr>
</tbody>
</table>

## <a name="automatically-create-cycle-counting-work"></a><span data-ttu-id="c6a20-146">Döngü sayım işini otomatik olarak oluşturma</span><span class="sxs-lookup"><span data-stu-id="c6a20-146">Automatically create cycle counting work</span></span>
<span data-ttu-id="c6a20-147">Döngü sayım işinin tekrarlı oluşturulmasının iki yolu vardır: döngü sayım eşikleri ayarlama veya döngü sayım planları ayarlama.</span><span class="sxs-lookup"><span data-stu-id="c6a20-147">There are two ways to schedule recurring creation of cycle counting work: set up cycle counting thresholds or set up cycle counting plans.</span></span>

-   <span data-ttu-id="c6a20-148">Bir döngü sayımı eşiği stok maddelerinin miktar veya yüzde sınırını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6a20-148">A cycle counting threshold indicates the quantity or percentage limit of inventory items.</span></span> <span data-ttu-id="c6a20-149">Döngü sayımı işi, eşik sınırına ulaşıldığında otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c6a20-149">Cycle counting work is automatically created when the threshold limit is reached.</span></span>
-   <span data-ttu-id="c6a20-150">Bir döngü sayım planı, döngü sayım işini ya hemen ya da bir toplu iş üzerinden periyodik olarak oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c6a20-150">A cycle counting plan creates cycle counting work either immediately or periodically through a batch job.</span></span> <span data-ttu-id="c6a20-151">Döngü sayım işi oluşturulduğunda, sayım iş satırı sayılacak konum hakkında bilgi içerir.</span><span class="sxs-lookup"><span data-stu-id="c6a20-151">When cycle counting work is created, the counting work line includes information about the location to count.</span></span> <span data-ttu-id="c6a20-152">Bu konumla ilişkilendirilmiş olan eldeki stok durdurulmuş değil ve dolayısıyla açık sayım işi mevcut olsa bile rezervasyona ve giden işleme uygun.</span><span class="sxs-lookup"><span data-stu-id="c6a20-152">The on-hand inventory that is associated with this location isn't blocked, and is therefore available for reservation and outbound processing, even though open counting work exists.</span></span>

### <a name="create-cycle-counting-work-based-on-threshold-parameters-for-items"></a><span data-ttu-id="c6a20-153">Maddeler için eşik parametrelerine dayalı olarak döngü sayım işi oluşturma</span><span class="sxs-lookup"><span data-stu-id="c6a20-153">Create cycle counting work, based on threshold parameters for items</span></span>

<span data-ttu-id="c6a20-154">Döngü sayım işi, bir konumdaki madde sayısının belirli bir eşik değerinin altına düşmesi durumunda oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="c6a20-154">Cycle counting work can be created when the number of items falls below a specific threshold value in a location.</span></span> <span data-ttu-id="c6a20-155">Örneğin, döngü sayımı eşiği 40 olan bir konumda 60 öğe vardır.</span><span class="sxs-lookup"><span data-stu-id="c6a20-155">For example, there are 60 items in a location that has a cycle counting threshold of 40.</span></span> <span data-ttu-id="c6a20-156">Bir satış siparişi hareketi sırasında, 25 öğe konumdan alınır ve bir hazırlama konumuna koyulur.</span><span class="sxs-lookup"><span data-stu-id="c6a20-156">During a sales order transaction, 25 items are picked from the location and put in a staging location.</span></span> <span data-ttu-id="c6a20-157">35 olan yeni madde sayısı, eşik miktarından az olduğundan döngü sayım işi bu konum için otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c6a20-157">Because the new item count, 35, is less than the threshold quantity, cycle counting work is automatically created for the location.</span></span>

### <a name="schedule-cycle-counting-work"></a><span data-ttu-id="c6a20-158">Döngü sayım işi planlama</span><span class="sxs-lookup"><span data-stu-id="c6a20-158">Schedule cycle counting work</span></span>

<span data-ttu-id="c6a20-159">Hemen veya periyodik olarak döngü sayım işi oluşturmak için döngü sayım planları yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c6a20-159">You can schedule cycle counting plans to create cycle counting work immediately or periodically.</span></span> <span data-ttu-id="c6a20-160">Döngü sayım planları ayarlayarak, döngü sayım işinin oluşturulduğu iş havuzunu, farklı konumlardaki maddeler için oluşturulan döngü sayımlarının maksimum sayısını ve bir ambar konumu yeniden sayılmadan önce geçecek gün sayısını kontrol edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c6a20-160">By setting up cycle counting plans, you can control the work pool that cycle counting work is created for, the maximum number of cycle counts that are created for items in different locations, and the number of days before a warehouse location is counted again.</span></span> <span data-ttu-id="c6a20-161">Örneğin, bir madde ambarda üç konumda mevcut ve maksimum döngü sayımı sayısı **2** olarak ayarlı.</span><span class="sxs-lookup"><span data-stu-id="c6a20-161">For example, an item is available in three locations in the warehouse, and the maximum number of cycle counts is set to **2**.</span></span> <span data-ttu-id="c6a20-162">Bu durumda, döngü sayımı planını çalıştırdığınızda iki döngü sayımı maddenin mevcut olduğu iki konum için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c6a20-162">In this case, when you run the cycle counting plan, two cycle counts are created for the two locations where the item is present.</span></span> <span data-ttu-id="c6a20-163">Başka bir örnek olarak, döngü sayımları arasındaki gün sayısını **5** olarak ayarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="c6a20-163">As another example, you set the number of days between cycle counts to **5**.</span></span> <span data-ttu-id="c6a20-164">Bu durumda, her beş günde bir döngü sayım işi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c6a20-164">In this case, cycle counting work is created every five days.</span></span> <span data-ttu-id="c6a20-165">Ancak, döngü sayım işi üçüncü günde işleniyorsa, bir sonraki döngü sayım işi son döngü sayımı işlendikten beş gün sonra, sekizinci gün içinde oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c6a20-165">However, if cycle counting work is processed on day 3, the next cycle counting work will be created five days after the last cycle counting was processed, on day 8.</span></span>

## <a name="create-cycle-counting-work-manually"></a><span data-ttu-id="c6a20-166">Döngü sayım işini manuel olarak oluşturma</span><span class="sxs-lookup"><span data-stu-id="c6a20-166">Create cycle counting work manually</span></span>
<span data-ttu-id="c6a20-167">Döngü sayım işini el ile oluşturmak için, **Maddeye göre döngü sayım işi** veya **Konuma göre döngü sayım işi** sayfasını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c6a20-167">To create cycle counting work manually, you can use the **Cycle count work by item** or **Cycle count work by location** page.</span></span> <span data-ttu-id="c6a20-168">Oluşturulacak maksimum döngü sayımı sayısını belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c6a20-168">You can specify the maximum number of cycle counts to create.</span></span> <span data-ttu-id="c6a20-169">Örneğin ambar yöneticisi değeri **5** olarak belirlerse, madde 10 konumda olsa bile döngü sayım işi beş konum için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c6a20-169">For example, if the warehouse manager specifies a value of **5**, cycle counting work is created for five locations, even if the item is present in 10 locations.</span></span> <span data-ttu-id="c6a20-170">Oluşturulan döngü sayım işi kimliklerinin atandığı bir iş havuzu kimliği de seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c6a20-170">You can also select a work pool ID to assign the cycle counting work IDs that are created to.</span></span> <span data-ttu-id="c6a20-171">Döngü sayımı için bir iş havuzu kimliği işlendiğinde, iş havuzuna atanan döngü sayım işi kimlikleri grup olarak işlenir.</span><span class="sxs-lookup"><span data-stu-id="c6a20-171">When a work pool ID is processed for cycle counting, the cycle counting work IDs that are assigned to the work pool are processed as a group.</span></span>

## <a name="perform-a-cycle-count-by-using-a-mobile-device"></a><span data-ttu-id="c6a20-172">Mobil cihaz kullanarak döngü sayımı gerçekleştirme</span><span class="sxs-lookup"><span data-stu-id="c6a20-172">Perform a cycle count by using a mobile device</span></span>
<span data-ttu-id="c6a20-173">Bir mobil cihazda Dynamics 365 for Finance and Operations kullanarak döngü sayım işi işlemenin birçok yöntemi vardır:</span><span class="sxs-lookup"><span data-stu-id="c6a20-173">There are several methods for processing cycle counting work by using Finance and Operations on a mobile device:</span></span>

-   <span data-ttu-id="c6a20-174">**Kullanıcı yönlendirmeli** – İşçi, **Açık** durumuna sahip bir döngü sayım işi kimliği belirtebilir.</span><span class="sxs-lookup"><span data-stu-id="c6a20-174">**User directed** – The worker can specify a cycle counting work ID that has a status of **Open**.</span></span>
-   <span data-ttu-id="c6a20-175">**Sistem yönlendirmesinde** – Finance and Operations işçiye bir döngü sayım işi kimliği atar.</span><span class="sxs-lookup"><span data-stu-id="c6a20-175">**System directed** – Finance and Operations assigns a cycle counting work ID to the worker.</span></span>
-   <span data-ttu-id="c6a20-176">**Döngü sayım gruplaması** – İşçi, belirli bir konuma, bölgeye veya iş havuzuna özgü döngü sayım işi kimliklerini gruplandırabilir.</span><span class="sxs-lookup"><span data-stu-id="c6a20-176">**Cycle count grouping** – The worker can group cycle counting work IDs that are specific to a particular location, zone, or work pool.</span></span>
-   <span data-ttu-id="c6a20-177">**Nokta döngü sayımı** – İşçi, bir ambar konumundaki maddeleri döngü sayım işi oluşturmaksızın her zaman sayabilir.</span><span class="sxs-lookup"><span data-stu-id="c6a20-177">**Spot cycle counting** – The worker can count items in a warehouse location at any time, without creating cycle counting work.</span></span> <span data-ttu-id="c6a20-178">Bir konumda nokta döngü sayımı gerçekleştirmek için işçi konum kimliğini girer.</span><span class="sxs-lookup"><span data-stu-id="c6a20-178">To perform spot cycle counting in a location, the worker enters the location ID.</span></span>

<span data-ttu-id="c6a20-179">Aşağıdaki örneklerde, nokta döngü sayımını mobil cihaz kullanarak nasıl gerçekleştirebileceğiniz gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="c6a20-179">The following example shows how you can perform spot cycle counting by using a mobile device.</span></span> <span data-ttu-id="c6a20-180">İşçinin cihazda gördüğü yönergeler, nokta döngü sayımına yönelik menünün kurulumuna bağlı olarak değişebilir.</span><span class="sxs-lookup"><span data-stu-id="c6a20-180">The instructions that the worker sees on the device vary, depending on the setup of the menu item for spot cycle counting.</span></span>

1.  <span data-ttu-id="c6a20-181">Mobil aygıtta, nokta döngü sayım işini yürütmek için menü öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c6a20-181">On the mobile device, select the menu item to process spot cycle counting work.</span></span>
2.  <span data-ttu-id="c6a20-182">Nokta döngü sayımı gerçekleştirilecek konumu kaydettirin.</span><span class="sxs-lookup"><span data-stu-id="c6a20-182">Register the location to perform spot cycle counting for.</span></span>
3.  <span data-ttu-id="c6a20-183">Madde numarasını ve sayılan madde miktarını kaydettirin ve doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="c6a20-183">Register and confirm the item number and the counted item quantity.</span></span> <span data-ttu-id="c6a20-184">**Not:** Döngü sayım işinin durumu **İşçi** sayfasında ayarlı parametrelere bağlı olarak **Tüm iş** sayfasında **Gözden geçirilmeyi bekliyor** ya da **Kapalı** olarak güncellenir.</span><span class="sxs-lookup"><span data-stu-id="c6a20-184">**Note:** The status of the cycle counting work is updated to either **Pending review** or **Closed** on the **All work** page, depending on the parameters that are set on the **Worker** page.</span></span>
4.  <span data-ttu-id="c6a20-185">İsteğe bağlı: 3. adımı konumda kalan maddeler için tekrarlayın ve sayım için başka madde kalmadığını kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="c6a20-185">Optional: Repeat step 3 for the remaining items in the location, and confirm that no additional items are available for counting.</span></span>

## <a name="resolve-cycle-counting-differences"></a><span data-ttu-id="c6a20-186">Döngü sayım farklarını düzeltme</span><span class="sxs-lookup"><span data-stu-id="c6a20-186">Resolve cycle counting differences</span></span>
<span data-ttu-id="c6a20-187">Aşağıdaki senaryolarda, bir iş kullanıcısı kimliği için **Bir döngü sayım denetimi** seçeneği **Hayır** olarak ayarlı ise bir döngü sayım farkı ortaya çıkar:</span><span class="sxs-lookup"><span data-stu-id="c6a20-187">A cycle counting difference occurs in the following scenarios if the **Is a cycle count supervisor** option is set to **No** for a work user ID:</span></span>

-   <span data-ttu-id="c6a20-188">Sayılan değer **İş kullanıcıları** sayfasındaki **Maksimum yüzde sınırı** veya **Maksimum miktar sınırı** alanlarında belirtilen sapma sınırları dahilinde değilse.</span><span class="sxs-lookup"><span data-stu-id="c6a20-188">The counted value isn't within the deviation limits that are specified in the **Maximum percentage limit** or **Maximum quantity limit** fields on the **Work users** page.</span></span> <span data-ttu-id="c6a20-189">Örneğin, bir konumdaki eldeki stok miktarı 50'dir ve iş kullanıcısı için sapma sınırı 10'dur.</span><span class="sxs-lookup"><span data-stu-id="c6a20-189">For example, the on-hand inventory quantity in a location is 50, and the deviation limit for the work user is 10.</span></span> <span data-ttu-id="c6a20-190">İş kullanıcısı, 40 ile 60 arasında olmayan bir değer girdiğinde, bir fark ortaya çıkar.</span><span class="sxs-lookup"><span data-stu-id="c6a20-190">If the work user enters a value that isn't between 40 and 60, a difference occurs.</span></span>
-   <span data-ttu-id="c6a20-191">Sayılan döngü değeri, eldeki stok miktarından farklı olur ve ayarlanmış sapma sınırları yoktur.</span><span class="sxs-lookup"><span data-stu-id="c6a20-191">The counted value differs from the on-hand inventory quantity, and no deviation limits are set.</span></span>

<span data-ttu-id="c6a20-192">Sayılan değerdeki farkları düzeltebilir ve ardından sayılan değeri **Gözden geçirilmeyi bekleyen döngü sayımı** sayfasında kabul edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c6a20-192">You can adjust differences in the counted value and then accept the counted value on the **Cycle count pending review** page.</span></span> <span data-ttu-id="c6a20-193">Madde miktarının değiştirilen sayısını **Konuma göre eldeki** sayfasında doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c6a20-193">You can verify the modified count of the item quantity on the **On hand by location** page.</span></span> <span data-ttu-id="c6a20-194">Fark onaylanamıyorsa, sayılan değer reddedilir.</span><span class="sxs-lookup"><span data-stu-id="c6a20-194">The counted value is rejected if the difference can't be approved.</span></span>

# <a name="see-also"></a><span data-ttu-id="c6a20-195">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="c6a20-195">See also</span></span>
[<span data-ttu-id="c6a20-196">Ambar işi için mobil cihazları yapılandırma</span><span class="sxs-lookup"><span data-stu-id="c6a20-196">Configure mobile devices for warehouse work</span></span>](configure-mobile-devices-warehouse.md)




