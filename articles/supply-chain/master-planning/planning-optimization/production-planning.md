---
title: Üretim planlama
description: Bu konuda üretim planlaması açıklanır ve Planlamayı En İyi Duruma Getirme kullanılarak planlı üretim emirlerinin nasıl değiştirileceği anlatılır.
author: ChristianRytt
manager: tfehr
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: f9b5e4122fbd83ff76e0605b2f0816e10d2d9aab
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470845"
---
# <a name="production-planning"></a><span data-ttu-id="4aa04-103">Üretim planlama</span><span class="sxs-lookup"><span data-stu-id="4aa04-103">Production planning</span></span>

<span data-ttu-id="4aa04-104">Planlamayı En İyi Duruma Getirme, birçok üretim senaryosunu destekler.</span><span class="sxs-lookup"><span data-stu-id="4aa04-104">Planning Optimizations supports several production scenarios.</span></span> <span data-ttu-id="4aa04-105">Mevcut, yerleşik master planlama altyapısından geçiş yapıyorsanız değiştirilen bazı davranışları öğrenmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="4aa04-105">If you're migrating from the existing, built-in master planning engine, it's important that you be aware of some changed behavior.</span></span>

<span data-ttu-id="4aa04-106">Aşağıdaki video, bu konuda ele alınan bazı kavramlara kısa bir giriş sağlar: [Dynamics 365 Supply Chain Management: Planlamayı İyileştirme'deki geliştirmeler](https://youtu.be/u1pcmZuZBTw).</span><span class="sxs-lookup"><span data-stu-id="4aa04-106">The following video gives a short introduction to some of the concepts discussed in this topic: [Dynamics 365 Supply Chain Management: Planning Optimization enhancements](https://youtu.be/u1pcmZuZBTw).</span></span>

## <a name="planned-production-orders"></a><span data-ttu-id="4aa04-107">Planlı üretim emirleri</span><span class="sxs-lookup"><span data-stu-id="4aa04-107">Planned production orders</span></span>

<span data-ttu-id="4aa04-108">Master planlama gereksinimleri karşılamak üzere planlı siparişler oluşturduğunda, sipariş türü **Planlı sipariş türü** alanındaki değere göre belirlenir.</span><span class="sxs-lookup"><span data-stu-id="4aa04-108">When master planning creates planned orders to fulfill requirements, the order type is determined by the value of the **Planned order type** field.</span></span> <span data-ttu-id="4aa04-109">**Planlı sipariş türü** alanı *Üretim* olarak ayarlanmışsa, planlanan üretim emirleri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4aa04-109">If the **Planned order type** field is set to *Production*, planned production orders are created.</span></span> <span data-ttu-id="4aa04-110">Bu planlı üretim emirleri, etkin ürün reçeteleri (BOM) ve ilgili üretim kurulumundaki rota kodu hakkında bilgiler içerir.</span><span class="sxs-lookup"><span data-stu-id="4aa04-110">These planned production orders include information about the active bill of materials (BOM) and the route ID from the related production setup.</span></span>

## <a name="requirements-from-boms"></a><span data-ttu-id="4aa04-111">Ürün reçetelerindeki gereksinimler</span><span class="sxs-lookup"><span data-stu-id="4aa04-111">Requirements from BOMs</span></span>

<span data-ttu-id="4aa04-112">Master planlama sırasında ürün reçetesi bilgileri dikkate alınır.</span><span class="sxs-lookup"><span data-stu-id="4aa04-112">BOM information is honored during master planning.</span></span> <span data-ttu-id="4aa04-113">Plan çıktısı, üretim için ilgili malzeme talebini kapsayacak malzeme tedarikini içerir.</span><span class="sxs-lookup"><span data-stu-id="4aa04-113">The plan output includes material supply to cover related material demand for production.</span></span>

<span data-ttu-id="4aa04-114">Master planlama sırasında geçerli, etkin ürün reçetesi üretim için gerekli olan malzemeleri belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4aa04-114">During master planning, the current, active BOM is used to determine the materials that are required for production.</span></span> <span data-ttu-id="4aa04-115">Bu adım, gerekli üretim emriyle ilişkili ürün reçetesi yapısının tüm düzeylerinde gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="4aa04-115">This step is done through all levels of the BOM structure that is related to the required production order.</span></span> <span data-ttu-id="4aa04-116">Malzeme gereksinimi, kullanılabilir eldeki stok, siparişteki mevcut tedarik ve onaylanmış planlı siparişler kullanılarak yerine getirilir.</span><span class="sxs-lookup"><span data-stu-id="4aa04-116">Material requirement is fulfilled by using available on-hand inventory, existing on-order supply, and approved planned orders.</span></span> <span data-ttu-id="4aa04-117">Herhangi bir yerde ek malzeme gerekiyorsa talebi kapsayacak şekilde planlı bir sipariş oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4aa04-117">If additional material is required anywhere, a planned order is created to cover the demand.</span></span>

## <a name="scheduling-during-firming"></a><span data-ttu-id="4aa04-118">Kesinleştirme sırasında planlama</span><span class="sxs-lookup"><span data-stu-id="4aa04-118">Scheduling during firming</span></span>

<span data-ttu-id="4aa04-119">Planlı üretim emirleri, üretim planlaması için gerekli rota kodunu içerir.</span><span class="sxs-lookup"><span data-stu-id="4aa04-119">Planned production orders include the route ID that is required for production scheduling.</span></span> <span data-ttu-id="4aa04-120">Ancak, planlı siparişler için planlama çalıştırması sırasında destek zamanlama işlemi bekler.</span><span class="sxs-lookup"><span data-stu-id="4aa04-120">However, scheduling support during the planning run for planned orders is pending.</span></span> <span data-ttu-id="4aa04-121">Rota kodu, kesinleştirme sırasında planlanan üretim emirlerini zamanlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4aa04-121">The route ID is used to schedule planned production orders during firming.</span></span> <span data-ttu-id="4aa04-122">Bu nedenle, planlanan üretim emirlerindeki sağlama süresi, burada açıklandığı gibi, bunlar temel alınarak oluşturulan ilgili zamanlanmış, kesinleştirilmiş üretim emirlerindeki sağlama süresinden farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="4aa04-122">Therefore, the lead time on planned production orders can differ from the lead time on related scheduled, firmed production orders that are generated from them, as described here:</span></span>

- <span data-ttu-id="4aa04-123">**Planlı üretim emri**: Sağlama süresi, serbest bırakılan ürünün statik sağlama süresini temel alan bir görevdir.</span><span class="sxs-lookup"><span data-stu-id="4aa04-123">**Planned production order** – The lead time is based on the static lead time from the released product.</span></span>
- <span data-ttu-id="4aa04-124">**Kesinleştirilmiş üretim emri**: Sağlama süresi rota bilgilerini ve ilgili kaynak kısıtlamalarını kullanan zamanlamaya dayanır.</span><span class="sxs-lookup"><span data-stu-id="4aa04-124">**Firmed production order** – The lead time is based on scheduling that uses route information and related resource constraints.</span></span>

<span data-ttu-id="4aa04-125">Beklenen özellik kullanılabilirliği hakkında daha fazla bilgi için bkz. [Planlamayı En İyi Duruma Getirme uygunluk analizi](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="4aa04-125">For more information about expected feature availability, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

<span data-ttu-id="4aa04-126">Henüz Planlamayı En İyi Duruma Getirme için sunulmayan üretim işlevini kullanıyorsanız yerleşik master planlama altyapısını kullanmaya devam edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4aa04-126">If you depend on production functionality that isn't yet available for Planning Optimization, you can continue to use the built-in master planning engine.</span></span> <span data-ttu-id="4aa04-127">Özel durum gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="4aa04-127">No exception is required.</span></span>

## <a name="delays"></a><span data-ttu-id="4aa04-128">Gecikmeler</span><span class="sxs-lookup"><span data-stu-id="4aa04-128">Delays</span></span>

<span data-ttu-id="4aa04-129">Gerekli malzemenin sağlama süresi bugünün tarihi ile malzeme gereksinim tarihi arasındaki dönemden uzunsa, gerekli malzeme ve ilgili üretim emri için planlanan emir geciktirilir.</span><span class="sxs-lookup"><span data-stu-id="4aa04-129">If the lead time for required material is longer than the period between today's date and the material requirement date, the planned order for the required material and the related production order will be delayed.</span></span> <span data-ttu-id="4aa04-130">Planlı emirler için, gün cinsinden gecikme serbest bırakılan ürünün sağlama süresine göre hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="4aa04-130">For planned orders, the delay (in days) is calculated based on the lead time from the released product.</span></span> <span data-ttu-id="4aa04-131">Sonra, gecikme bilgileri ürün reçetesi yapısının tüm düzeylerinde uygulanır.</span><span class="sxs-lookup"><span data-stu-id="4aa04-131">The delay information is then propagated through all levels of the BOM structure.</span></span> <span data-ttu-id="4aa04-132">Bu nedenle, gecikmiş ham maddenin etkisini müşterinin satış siparişine göre takip edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4aa04-132">Therefore, you can follow the impact of delayed raw material all the way to the customer sales order.</span></span>

## <a name="modifying-planned-orders"></a><span data-ttu-id="4aa04-133">Planlı siparişleri değiştirme</span><span class="sxs-lookup"><span data-stu-id="4aa04-133">Modifying planned orders</span></span>

<span data-ttu-id="4aa04-134">Planlı sipariş ile ilgili bilgileri değiştirdiğinizde şu iletiyi alırsınız: "Planlı siparişlerde el ile yapılan değişikliklerin etkisi, bir sonraki master planlamayı çalıştırma işlemine kadar planın geri kalanına yansıtılmaz."</span><span class="sxs-lookup"><span data-stu-id="4aa04-134">When you change information on a planned order, you receive the following message: "Note that the impact of manual changes on planned orders won't be reflected in the rest of the plan until the next master planning run."</span></span>

<span data-ttu-id="4aa04-135">Planlı bir siparişte yer alan bilgileri değiştirmek ve ilgili malzeme gereksinimleri üzerindeki etkiyi görmek istiyorsanız aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4aa04-135">If you want to change information on a planned order and see the impact on the related material requirements, follow these steps.</span></span>

1. <span data-ttu-id="4aa04-136">Planlı siparişi güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="4aa04-136">Update the planned order.</span></span>
2. <span data-ttu-id="4aa04-137">Planlı siparişi onaylayın.</span><span class="sxs-lookup"><span data-stu-id="4aa04-137">Approve the planned order.</span></span>
3. <span data-ttu-id="4aa04-138">Master planlamayı çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="4aa04-138">Run master planning.</span></span>

<span data-ttu-id="4aa04-139">Master planlamayı çalıştırdığınızda, planlanan üretim emirleri dahilse filtre kullanmamalısınız.</span><span class="sxs-lookup"><span data-stu-id="4aa04-139">When you run master planning, you should not use filters if planned production orders are included.</span></span> <span data-ttu-id="4aa04-140">Daha fazla bilgi için bu konunun sonraki kısımlarında yer alan [Filtreler](#filters) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="4aa04-140">For more information, see the [Filters](#filters) section later in this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="4aa04-141">Planlı siparişin teslimat tarihi sonraki bir tarihe değiştirilirse talep yeni bir planlı siparişle ilişkilendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="4aa04-141">If the delivery date of the planned order is changed to a later date, the demand might be pegged against a new planned order.</span></span> <span data-ttu-id="4aa04-142">Bu davranış, yeni tedarik tarihi ilişkilendirilmiş talep için gecikmeye neden olduğunda ancak sağlama süresi ayarlarına göre gecikme önlenebileceğinde gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="4aa04-142">This behavior occurs when the new supply date causes a delay for the pegged demand but, according to the lead time settings, the delay can be avoided.</span></span>

## <a name="explosion-page"></a><span data-ttu-id="4aa04-143">Açılım sayfası</span><span class="sxs-lookup"><span data-stu-id="4aa04-143">Explosion page</span></span>

<span data-ttu-id="4aa04-144">Belirli bir üretim emri veya planlı üretim emri için gerekli talebi, ilgili kapsamı ve ilişkilendirme bilgilerini analiz etmek için **Açılım** sayfasını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4aa04-144">You can use the **Explosion** page to analyze the demand that is required for a specific production order or planned production order, the related coverage, and pegging information.</span></span> <span data-ttu-id="4aa04-145">**Açılım** sayfasındaki bilgiler master planlama sırasında güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="4aa04-145">Information on the **Explosion** page is updated during master planning.</span></span> <span data-ttu-id="4aa04-146">Bilgileri, doğrudan **Açılım** sayfasından güncelleştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="4aa04-146">You can't update the information directly from the **Explosion** page.</span></span>

## <a name="filters"></a><a name="filters"></a><span data-ttu-id="4aa04-147">Filtreler</span><span class="sxs-lookup"><span data-stu-id="4aa04-147">Filters</span></span>

<span data-ttu-id="4aa04-148">Üretim içeren planlama senaryoları için filtre uygulanmış master planlama çalıştırmaların kullanmamanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="4aa04-148">For planning scenarios that include production, we recommend that you avoid filtered master planning runs.</span></span> <span data-ttu-id="4aa04-149">Planlamayı En İyi Duruma Getirme işlevinin doğru sonucu hesaplamak için gerekli bilgilere sahip olmasını sağlamak için planlı siparişin tüm ürün reçetesi yapısındaki ürünlerle ilişkisi olan tüm ürünleri dahil etmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="4aa04-149">To ensure that Planning Optimization has the information that is required to calculate the correct result, you must include all products that have any relation to products in the whole BOM structure of the planned order.</span></span>

<span data-ttu-id="4aa04-150">Yerleşik master planlama altyapısı kullanıldığında bağımlı alt öğeler otomatik olarak tespit edilip master planlama çalışmalarına dahil edilse de Planlamayı En İyi Duruma Getirme bu eylemi gerçekleştirmez.</span><span class="sxs-lookup"><span data-stu-id="4aa04-150">Although dependent child items are automatically detected and included in master planning runs when the built-in master planning engine is used, Planning Optimization doesn't perform this action.</span></span>

<span data-ttu-id="4aa04-151">Örneğin, A ürününün ürün reçetesi yapısından yapılan tek bir cıvata, B ürününü üretmek için de kullanılırsa A ve B ürünlerinin ürün reçetesi yapısındaki tüm ürünler filtreye dahil edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="4aa04-151">For example, if a single bolt from the BOM structure of product A is also used to produce product B, all products in the BOM structure of products A and B must be included in the filter.</span></span> <span data-ttu-id="4aa04-152">Tüm ürünlerin filtrenin parçası olduğundan emin olmak çok karmaşık olabileceğinden, üretim emirleri söz konusu olduğunda filtre uygulanmış master planlama çalıştırmalarını kullanmamanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="4aa04-152">Because it can be very complex to ensure that all products are part of the filter, we recommend that you avoid filtered master planning runs when production orders are involved.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]