---
title: Satınalma talepleri
description: Bu konuda, satın alma taleplerinin Planlamayı En İyi Duruma Getirme işlevinde nasıl desteklendiği açıklanmaktadır.
author: ChristianRytt
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 564f87fe78e79107feb103f953ed4769e4734aa1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808052"
---
# <a name="purchase-requisitions"></a><span data-ttu-id="903dc-103">Satınalma talepleri</span><span class="sxs-lookup"><span data-stu-id="903dc-103">Purchase requisitions</span></span>

<span data-ttu-id="903dc-104">Master planlama onaylı satın alma taleplerini yenileyebilir.</span><span class="sxs-lookup"><span data-stu-id="903dc-104">Master planning can replenish approved purchase requisitions.</span></span> <span data-ttu-id="903dc-105">Bu sayede, kullanıcılar satın alma taleplerini karşılamak için iş akışı kullanarak satınalma siparişi oluşturmak zorunda kalmaz.</span><span class="sxs-lookup"><span data-stu-id="903dc-105">Therefore, to cover purchase requisitions, users don't have to use a workflow to create purchase orders.</span></span> <span data-ttu-id="903dc-106">Bunun yerine, satınalma talepleri master planlama tarafından karşılanabilir.</span><span class="sxs-lookup"><span data-stu-id="903dc-106">Instead, purchase requisitions can be covered by master planning.</span></span> <span data-ttu-id="903dc-107">Bu işlevsellik sayesinde satınalma talebi, ilgili ürün için ayarlanan **Planlı sipariş türü** değerine bağlı olarak satınalma siparişi, transfer emri veya üretim emri oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="903dc-107">Because of this functionality, a purchase requisition can produce a purchase order, a transfer order, or a production order, depending on the **Planned order type** value that is set for the related product.</span></span>

## <a name="enable-master-plans-to-include-requisitions"></a><span data-ttu-id="903dc-108">Talepleri dahil etmek için master planları etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="903dc-108">Enable master plans to include requisitions</span></span>

<span data-ttu-id="903dc-109">Bir master plan için karşılama hesaplaması sırasında talepleri dahil etmek üzere aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="903dc-109">To include requisitions during the coverage calculation for a master plan, follow these steps.</span></span>

1. <span data-ttu-id="903dc-110">**Master planlama** \> **Kurulum** \> **Planlar** \> **Master planlar** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="903dc-110">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="903dc-111">Bir master plan oluşturun veya seçin.</span><span class="sxs-lookup"><span data-stu-id="903dc-111">Create or select a master plan.</span></span>
1. <span data-ttu-id="903dc-112">**Genel** hızlı sekmesinde, **Talepleri dahil et** seçeneğini *Evet* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="903dc-112">On the **General** FastTab, set the **Include requisitions** option to *Yes*.</span></span>
1. <span data-ttu-id="903dc-113">Talepleri dahil etmek istediğiniz her ek master plan için 2 ve 3 numaralı adımları yineleyin.</span><span class="sxs-lookup"><span data-stu-id="903dc-113">Repeat steps 2 and 3 for each additional master plan where you want to include requisitions.</span></span>

## <a name="approved-requisitions-time-fence"></a><span data-ttu-id="903dc-114">Onaylanmış talepler zaman dilimi</span><span class="sxs-lookup"><span data-stu-id="903dc-114">Approved requisitions time fence</span></span>

<span data-ttu-id="903dc-115">*Onaylı talepler zaman dilimi*, master planın onaylı stok yenileme taleplerinde ne kadar önceden (gün cinsinden) talepleri dahil edeceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="903dc-115">The *approved requisitions time fence* establishes how far back (in days) a master plan will include demand from approved replenishment requisitions.</span></span> <span data-ttu-id="903dc-116">Onaylı talep zaman dilimini, hem kapsam grubu düzeyinde hem de master plan düzeyinde ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="903dc-116">You can set an approved requisitions time fence at both the coverage group level and the master plan level.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-a-coverage-group"></a><span data-ttu-id="903dc-117">Kapsam grubu için onaylı taleplerin zaman dilimini ayarlama</span><span class="sxs-lookup"><span data-stu-id="903dc-117">Set the approved requisitions time fence for a coverage group</span></span>

1. <span data-ttu-id="903dc-118">**Master planlama** \> **Kurulum** \> **Kapsam** \> **Kapsam grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="903dc-118">Go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**.</span></span>
1. <span data-ttu-id="903dc-119">Kapsam grubu oluşturun veya seçin.</span><span class="sxs-lookup"><span data-stu-id="903dc-119">Create or select a coverage group.</span></span>
1. <span data-ttu-id="903dc-120">**Diğer** hızlı sekmesinde, **Onaylanmış talepler zaman dilimi (gün)** alanını zaman dilimine dahil edilecek gün sayısına göre ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="903dc-120">On the **Other** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="903dc-121">Onaylanmış talepler zaman dilimini ayarlamak istediğiniz her ek kapsam grubu için 2. ve 3. adımları tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="903dc-121">Repeat steps 2 and 3 for each additional coverage group where you want to set an approved requisitions time fence.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-individual-master-plans"></a><span data-ttu-id="903dc-122">Ayrı master planlar için onaylanmış talepler zaman dilimini ayarlama</span><span class="sxs-lookup"><span data-stu-id="903dc-122">Set the approved requisitions time fence for individual master plans</span></span>

<span data-ttu-id="903dc-123">Ayrı master planlar için onaylanmış taleplerin zaman dilimi ayarladığınızda ayar, geçerli kapsam grubunun zaman dilimi ayarını geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="903dc-123">When you set an approved requisitions time fence for an individual master plan, the setting overrides the time fence setting for any applicable coverage group.</span></span>

1. <span data-ttu-id="903dc-124">**Master planlama** \> **Kurulum** \> **Planlar** \> **Master planlar** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="903dc-124">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="903dc-125">Bir master plan oluşturun veya seçin.</span><span class="sxs-lookup"><span data-stu-id="903dc-125">Create or select a master plan.</span></span>
1. <span data-ttu-id="903dc-126">**Gün cinsinden zaman dilimleri** hızlı sekmesinde, **Onaylanmış talepler zaman dilimi (gün)** alanını zaman dilimine dahil edilecek gün sayısına göre ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="903dc-126">On the **TIme fences in days** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="903dc-127">Onaylanmış talepler zaman dilimini ayarlamak istediğiniz her ek master plan için 2. ve 3. adımları tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="903dc-127">Repeat steps 2 and 3 for each additional master plan where you want to set an approved requisitions time fence.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="903dc-128">**Çok yakında:** Onaylı taleplerin zaman dilimleri, henüz Planlamayı En İyi Duruma Getirme için desteklenmemektedir.</span><span class="sxs-lookup"><span data-stu-id="903dc-128">**Coming soon:** Approved requisitions time fences aren't yet supported for Planning Optimization.</span></span> <span data-ttu-id="903dc-129">Desteklenene kadar **Onaylanmış talepler zaman dilimi (gün)** alanına gireceğiniz tüm değerler yoksayılır.</span><span class="sxs-lookup"><span data-stu-id="903dc-129">Until they are supported, all values that you enter in the **Approved requisitions time fence (days)** field will be ignored.</span></span>

## <a name="independent-supply-regardless-of-coverage-code"></a><span data-ttu-id="903dc-130">Kapsam koduna bakılmaksızın bağımsız tedarik</span><span class="sxs-lookup"><span data-stu-id="903dc-130">Independent supply, regardless of coverage code</span></span>

<span data-ttu-id="903dc-131">Kapsam kodu ne olursa olsun, satın alma talepleri he zaman bağımsız planlı siparişler tarafından kapsanır.</span><span class="sxs-lookup"><span data-stu-id="903dc-131">Purchase requisitions are always covered by independent planned orders, regardless of the coverage code.</span></span> <span data-ttu-id="903dc-132">Bu davranış, satın alma talepleri ve stok yenileme siparişleri arasında daha net izlenebilirlik ve iş akışları sağlar.</span><span class="sxs-lookup"><span data-stu-id="903dc-132">This behavior ensures clear traceability and workflows between purchase requisitions and replenishment orders.</span></span>

### <a name="example-1"></a><span data-ttu-id="903dc-133">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="903dc-133">Example 1</span></span>

<span data-ttu-id="903dc-134">**Kapsam kodu** değeri *Min/maks* olacak şekilde bir ürün ayarlanır. Ürünün, stok ve talep durumları aşağıdaki şekildedir.</span><span class="sxs-lookup"><span data-stu-id="903dc-134">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="903dc-135">Eldeki stok miktarı = 10.</span><span class="sxs-lookup"><span data-stu-id="903dc-135">Inventory on-hand quantity = 10.</span></span>
- <span data-ttu-id="903dc-136">Minimum stok miktarı = 15.</span><span class="sxs-lookup"><span data-stu-id="903dc-136">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="903dc-137">Maksimum stok miktarı = 20.</span><span class="sxs-lookup"><span data-stu-id="903dc-137">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="903dc-138">Tek bir adet için satınalma talebi var.</span><span class="sxs-lookup"><span data-stu-id="903dc-138">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="903dc-139">Talep edilme tarihi bugün.</span><span class="sxs-lookup"><span data-stu-id="903dc-139">It has a requested date of today.</span></span>

<span data-ttu-id="903dc-140">Master planlama çalıştırıldığında, iki planlı sipariş oluşturulur: Biri, stoku maksimum miktara göre yenilemek için 10 adede göre, diğeri ise satınalma talebini karşılamak için bir adede göredir.</span><span class="sxs-lookup"><span data-stu-id="903dc-140">When master planning runs, two planned orders are created: one for 10 pieces to replenish inventory to the maximum quantity, and one for one piece to replenish the purchase requisition.</span></span>

### <a name="example-2"></a><span data-ttu-id="903dc-141">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="903dc-141">Example 2</span></span>

<span data-ttu-id="903dc-142">**Kapsam kodu** değeri *Min/maks* olacak şekilde bir ürün ayarlanır. Ürünün, stok ve talep durumları aşağıdaki şekildedir.</span><span class="sxs-lookup"><span data-stu-id="903dc-142">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="903dc-143">Eldeki stok miktarı = 17.</span><span class="sxs-lookup"><span data-stu-id="903dc-143">Inventory on-hand quantity = 17.</span></span>
- <span data-ttu-id="903dc-144">Minimum stok miktarı = 15.</span><span class="sxs-lookup"><span data-stu-id="903dc-144">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="903dc-145">Maksimum stok miktarı = 20.</span><span class="sxs-lookup"><span data-stu-id="903dc-145">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="903dc-146">Tek bir adet için satınalma talebi var.</span><span class="sxs-lookup"><span data-stu-id="903dc-146">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="903dc-147">Talep edilme tarihi bugün.</span><span class="sxs-lookup"><span data-stu-id="903dc-147">It has a requested date of today.</span></span>

<span data-ttu-id="903dc-148">Master planlama çalıştırıldığında, satınalma talebini karşılamak için bir adet için bir planlı sipariş oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="903dc-148">When master planning runs, one planned order for one piece is created to replenish the purchase requisition.</span></span>

### <a name="example-3"></a><span data-ttu-id="903dc-149">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="903dc-149">Example 3</span></span>

<span data-ttu-id="903dc-150">**Kapsam kodu** *Dönem* olak ve dönem uzunluğu yedi gün olan bir ürün ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="903dc-150">A product is set up so that it has a **Coverage code** value of *Period* and a period length of seven days.</span></span> <span data-ttu-id="903dc-151">Aşağıdaki stok, satış siparişi ve talep durumlarına sahiptir:</span><span class="sxs-lookup"><span data-stu-id="903dc-151">It has the following inventory, sales order, and requisition statuses:</span></span>

- <span data-ttu-id="903dc-152">Eldeki stok miktarı = 0.</span><span class="sxs-lookup"><span data-stu-id="903dc-152">Inventory on-hand quantity = 0.</span></span>
- <span data-ttu-id="903dc-153">Beş adet için bir satış siparişi var.</span><span class="sxs-lookup"><span data-stu-id="903dc-153">A sales order for five pieces exists.</span></span> <span data-ttu-id="903dc-154">Beklenen sevkiyat tarihi bugün artı bir gündür.</span><span class="sxs-lookup"><span data-stu-id="903dc-154">It has an expected ship date of today plus one day.</span></span>
- <span data-ttu-id="903dc-155">Üç adet için satınalma talebi var.</span><span class="sxs-lookup"><span data-stu-id="903dc-155">A purchase requisition for three pieces exists.</span></span> <span data-ttu-id="903dc-156">Talep edilme tarihi bugün artı üç gündür.</span><span class="sxs-lookup"><span data-stu-id="903dc-156">It has a requested date of today plus three days.</span></span>

<span data-ttu-id="903dc-157">Master planlama çalıştırıldığında, iki planlı sipariş oluşturulur: Biri, satınalma talebini karşılamak için üç adede göre, diğer satış siparişi talebini karşılamak için beş adede göredir.</span><span class="sxs-lookup"><span data-stu-id="903dc-157">When master planning runs, two planned orders are created: one for three pieces to replenish the purchase requisition and one for five pieces to replenish sales order demand.</span></span>

> [!NOTE]
> <span data-ttu-id="903dc-158">Bir satınalma talebiyle ilişkilendirilmiş bir planlı sipariş kesinleştirildikten sonra, planlama altyapısı, satınalma talebiyle ilişkilendirmeyi korur.</span><span class="sxs-lookup"><span data-stu-id="903dc-158">After a planned order that is pegged to a purchase requisition is firmed, the planning engine keeps the pegging to the purchase requisition.</span></span> <span data-ttu-id="903dc-159">Kesinleştirilmiş siparişin satınalma talebini yerine getirmek için gerekli miktara sahip olmadığı görülürse sistem, aradaki fark için yeni bir planlı sipariş oluşturur.</span><span class="sxs-lookup"><span data-stu-id="903dc-159">If the firmed order is later found to be missing some quantity that is required to fulfill the purchase requisition, the system will create a new planned order for the difference.</span></span>

<span data-ttu-id="903dc-160">Satın alma talepleri hakkında daha fazla bilgi için bkz. [Satınalma talebine genel bakış](../../procurement/purchase-requisitions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="903dc-160">For more information about purchase requisitions, see [Purchase requisition overview](../../procurement/purchase-requisitions-overview.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]