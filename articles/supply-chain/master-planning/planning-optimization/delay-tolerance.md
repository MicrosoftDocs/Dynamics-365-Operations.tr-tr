---
title: Gecikme toleransı (negatif günler)
description: Bu konu, gecikme toleransı hesaplaması ve bunun Planlamayı En İyi Duruma Getirme'de planlı sipariş oluşturmayı nasıl etkilediği hakkında bilgi sağlar.
author: crytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 748e047e89747f2eabccc04a40c79bcb1e6f3dea
ms.sourcegitcommit: f21659f1c23bc2cd65bbe7fb7210910d5a8e1cb9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/24/2021
ms.locfileid: "6306475"
---
# <a name="delay-tolerance-negative-days"></a><span data-ttu-id="a2f47-103">Gecikme toleransı (negatif günler)</span><span class="sxs-lookup"><span data-stu-id="a2f47-103">Delay tolerance (negative days)</span></span>

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="a2f47-104">Gecikme toleransı işlevi, Planlamayı En İyi Duruma Getirme özelliğinin karşılama grupları için ayarlanan **Negatif günler** değerini dikkate almasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="a2f47-104">The delay tolerance functionality enables Planning Optimization to consider the **Negative days** value that is set for coverage groups.</span></span> <span data-ttu-id="a2f47-105">Master planlama sırasında uygulanan gecikme toleransı süresini uzatmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a2f47-105">It's used to extend the delay tolerance period that is applied during master planning.</span></span> <span data-ttu-id="a2f47-106">Bu şekilde, mevcut tedarik talebi kısa bir gecikmeyle karşılayabilecekse yeni tedarik emirleri oluşturmaktan kaçınabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a2f47-106">In this way, you can avoid creating new supply orders if existing supply will be able to cover the demand after a short delay.</span></span> <span data-ttu-id="a2f47-107">İşlev'n amacı, belirli bir talep için yeni bir tedarik emri oluşturmanın mantıklı olup olmadığını belirlemektir.</span><span class="sxs-lookup"><span data-stu-id="a2f47-107">The purpose of the functionality is to determine whether it makes sense to create a new supply order for a given demand.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="a2f47-108">Sisteminizdeki özelliği etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="a2f47-108">Turn on the feature in your system</span></span>

<span data-ttu-id="a2f47-109">Gecikme toleransı işlevini sisteminizde kullanılabilir yapmak için, [Özellik yönetimi](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ne gidin ve *Planlamayı En İyi Duruma Getirme için negatif günler* özelliğini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="a2f47-109">To make the delay tolerance functionality available in your system, go to [Feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Negative days for Planning Optimization* feature.</span></span>

## <a name="delay-tolerance-in-planning-optimization"></a><span data-ttu-id="a2f47-110">Planlamayı En İyi Duruma Getirmede gecikme toleransı</span><span class="sxs-lookup"><span data-stu-id="a2f47-110">Delay tolerance in Planning Optimization</span></span>

<span data-ttu-id="a2f47-111">Gecikme toleransı, mevcut tedarik zaten planlandığında yeni stok yenileme istemeden önce beklemeye istekli olduğunuz sağlama süresi ötesindeki gün sayısını temsil eder.</span><span class="sxs-lookup"><span data-stu-id="a2f47-111">Delay tolerance represents the number of days beyond the lead time that you're willing to wait before you order new replenishment when existing supply is already planned.</span></span> <span data-ttu-id="a2f47-112">Gecikme toleransı, iş günleri değil takvim günleri kullanılarak tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="a2f47-112">Delay tolerance is defined by using calendar days, not business days.</span></span>

<span data-ttu-id="a2f47-113">Master planlama sırasında, sistem gecikme toleransını hesapladığında, **Negatif günler** ayarını dikkate alır.</span><span class="sxs-lookup"><span data-stu-id="a2f47-113">At the time of master planning, when the system calculates the delay tolerance, it considers the **Negative days** setting.</span></span> <span data-ttu-id="a2f47-114">**Negatif günler** değerini, **Karşılama grupları** sayfasında veya **Madde karşılama** sayfasında ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a2f47-114">You can set the **Negative days** value on either the **Coverage groups** page or the **Item coverage** page.</span></span>

<span data-ttu-id="a2f47-115">Sistem gecikme toleransı hesaplamasını *en erken stok yenileme tarihine* bağlar; bu da bugünün tarihi + sağlama süresine eşittir.</span><span class="sxs-lookup"><span data-stu-id="a2f47-115">The system links the delay tolerance calculation to the *earliest replenishment date*, which equals today's date plus the lead time.</span></span> <span data-ttu-id="a2f47-116">Gecikme toleransı, *maks()* öğesinin iki değerden daha büyük olanı bulduğu aşağıdaki formül kullanılarak hesaplanır:</span><span class="sxs-lookup"><span data-stu-id="a2f47-116">The delay tolerance is calculated by using following formula, where *max()* finds the larger of two values:</span></span>

<span data-ttu-id="a2f47-117">*maks(En erken stok yenileme tarihi, Talep son tarihi)* – *Talep son tarihi* + *Negatif günler*</span><span class="sxs-lookup"><span data-stu-id="a2f47-117">*max(Earliest replenishment date, Demand due date)* – *Demand due date* + *Negative days*</span></span>

<span data-ttu-id="a2f47-118">Bu formül, ürün sağlama süresi boyunca yeterli tedarik olduğunda master planlamanın yeni tedarik emirleri oluşturmamasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="a2f47-118">This formula ensures that master planning doesn't create new supply orders when enough supply exists during the product lead time.</span></span>

> [!NOTE]
> <span data-ttu-id="a2f47-119">Planlamayı En İyi Duruma Getirme'de gecikme toleransı hesaplaması her zaman yerleşik master planlamadan alınan dinamik negatif gün hesaplamasını kullanır.</span><span class="sxs-lookup"><span data-stu-id="a2f47-119">The delay tolerance calculation in Planning Optimization always uses the dynamic negative days calculation from built-in master planning.</span></span> <span data-ttu-id="a2f47-120">**Master planlama parametreleri** sayfasindaki **Dinamik negatif günleri kullan** ayarının bu davranış üzerinde hiçbir etkisi yoktur.</span><span class="sxs-lookup"><span data-stu-id="a2f47-120">The **Use dynamic negative days** setting on the **Master planning parameters** page has no effect on this behavior.</span></span>

<span data-ttu-id="a2f47-121">Mevcut tedarik, hesaplanan gecikme toleransından daha az veya buna eşit bir talep gecikmesi anlamına gelirse Planlamayı En İyi Duruma Getirme, mevcut tedariki taleple birlikte sabitler.</span><span class="sxs-lookup"><span data-stu-id="a2f47-121">If the existing supply implies a demand delay that is less than or equal to the calculated delay tolerance, Planning Optimization pegs existing supply with the demand.</span></span> <span data-ttu-id="a2f47-122">Bazı durumlarda, aşırı tedarikle sonuçlanmaktansa talebi geciktirmek daha iyidir.</span><span class="sxs-lookup"><span data-stu-id="a2f47-122">In some cases, it's better to delay the demand than to end up with oversupply.</span></span>

<span data-ttu-id="a2f47-123">Aşağıdaki alt bölümler, gecikme toleransının Planlamayı En İyi Duruma Getirmedeki planlı siparişlerin oluşturulmasını nasıl etkilediğini gösteren örnekler sağlar.</span><span class="sxs-lookup"><span data-stu-id="a2f47-123">The following subsections provide examples that show how delay tolerance affects the creation of planned orders in Planning Optimization.</span></span>

### <a name="example-1"></a><span data-ttu-id="a2f47-124">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a2f47-124">Example 1</span></span>

<span data-ttu-id="a2f47-125">Bir ürün aşağıdaki yapılandırmaya sahiptir:</span><span class="sxs-lookup"><span data-stu-id="a2f47-125">A product has the following configuration:</span></span>

- <span data-ttu-id="a2f47-126">**Sağlama süresi:** *10*</span><span class="sxs-lookup"><span data-stu-id="a2f47-126">**Lead time:** *10*</span></span>
- <span data-ttu-id="a2f47-127">**Negatif günler:** *2*</span><span class="sxs-lookup"><span data-stu-id="a2f47-127">**Negative days:** *2*</span></span>

<span data-ttu-id="a2f47-128">Ürün için aşağıdaki tedarik ve talep mevcuttur:</span><span class="sxs-lookup"><span data-stu-id="a2f47-128">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="a2f47-129">**Bugün için talep:** 10 adet için satış siparişi</span><span class="sxs-lookup"><span data-stu-id="a2f47-129">**Demand for today:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="a2f47-130">**12 günde tedarik:** 10 adet için satınalma siparişi</span><span class="sxs-lookup"><span data-stu-id="a2f47-130">**Supply in 12 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="a2f47-131">Mevcut tedarik, talebi 12 gün içinde karşılayabilir ve bu süre gecikme toleransına eşittir.</span><span class="sxs-lookup"><span data-stu-id="a2f47-131">Existing supply can cover the demand within 12 days, and that period equals the delay tolerance.</span></span> <span data-ttu-id="a2f47-132">Bu nedenle, master planlama çalıştığında, planlı sipariş oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="a2f47-132">Therefore, when master planning runs, no planned orders are created.</span></span>

### <a name="example-2"></a><span data-ttu-id="a2f47-133">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a2f47-133">Example 2</span></span>

<span data-ttu-id="a2f47-134">Bir ürün aşağıdaki yapılandırmaya sahiptir:</span><span class="sxs-lookup"><span data-stu-id="a2f47-134">A product has the following configuration:</span></span>

- <span data-ttu-id="a2f47-135">**Sağlama süresi:** *10*</span><span class="sxs-lookup"><span data-stu-id="a2f47-135">**Lead time:** *10*</span></span>
- <span data-ttu-id="a2f47-136">**Negatif günler:** *0*</span><span class="sxs-lookup"><span data-stu-id="a2f47-136">**Negative days:** *0*</span></span>

<span data-ttu-id="a2f47-137">Ürün için aşağıdaki tedarik ve talep mevcuttur:</span><span class="sxs-lookup"><span data-stu-id="a2f47-137">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="a2f47-138">**Bugün için talep:** 10 adet için satış siparişi</span><span class="sxs-lookup"><span data-stu-id="a2f47-138">**Demand for today:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="a2f47-139">**12 günde tedarik:** 10 adet için satınalma siparişi</span><span class="sxs-lookup"><span data-stu-id="a2f47-139">**Supply in 12 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="a2f47-140">Mevcut tedairk talebi ancak 12 gün sonra karşılayabilir.</span><span class="sxs-lookup"><span data-stu-id="a2f47-140">Existing supply can cover the demand only after 12 days.</span></span> <span data-ttu-id="a2f47-141">Ancak, gecikme toleransı 10 gündür.</span><span class="sxs-lookup"><span data-stu-id="a2f47-141">However, the delay tolerance is 10 days.</span></span> <span data-ttu-id="a2f47-142">Bu nedenle, master planlama çalıştığında, 10 adet için planlı bir sipariş oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="a2f47-142">Therefore, when master planning runs, a planned order for a quantity of 10 is created.</span></span>

### <a name="example-3"></a><span data-ttu-id="a2f47-143">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="a2f47-143">Example 3</span></span>

<span data-ttu-id="a2f47-144">Bir ürün aşağıdaki yapılandırmaya sahiptir:</span><span class="sxs-lookup"><span data-stu-id="a2f47-144">A product has the following configuration:</span></span>

- <span data-ttu-id="a2f47-145">**Sağlama süresi:** *10*</span><span class="sxs-lookup"><span data-stu-id="a2f47-145">**Lead time:** *10*</span></span>
- <span data-ttu-id="a2f47-146">**Negatif günler:** *2*</span><span class="sxs-lookup"><span data-stu-id="a2f47-146">**Negative days:** *2*</span></span>

<span data-ttu-id="a2f47-147">Ürün için aşağıdaki tedarik ve talep mevcuttur:</span><span class="sxs-lookup"><span data-stu-id="a2f47-147">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="a2f47-148">**11 gün içinde talep:** 10 adet için satış siparişi</span><span class="sxs-lookup"><span data-stu-id="a2f47-148">**Demand in 11 days:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="a2f47-149">**14 günde tedarik:** 10 adet için satınalma siparişi</span><span class="sxs-lookup"><span data-stu-id="a2f47-149">**Supply in 14 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="a2f47-150">Mevcut tedairk talebi ancak üç gün sonra karşılayabilir.</span><span class="sxs-lookup"><span data-stu-id="a2f47-150">Existing supply can cover the demand only after three days.</span></span> <span data-ttu-id="a2f47-151">Ancak, gecikme toleransı iki gündür.</span><span class="sxs-lookup"><span data-stu-id="a2f47-151">However, the delay tolerance is two days.</span></span> <span data-ttu-id="a2f47-152">(Bu durumda, gecikme toleransı yalnızca iki negatif günü içerir.</span><span class="sxs-lookup"><span data-stu-id="a2f47-152">(In this case, the delay tolerance includes only the two negative days.</span></span> <span data-ttu-id="a2f47-153">Talep tarihi, ürün sağlama süresinden sonra olduğu için dahil edilmez.) Bu nedenle, master planlama çalıştığında, 10 miktarı için planlı bir sipariş oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="a2f47-153">The demand date isn't included because it's after the product lead time.) Therefore, when master planning runs, a planned order for a quantity of 10 is created.</span></span>
