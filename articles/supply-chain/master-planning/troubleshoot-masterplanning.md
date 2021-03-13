---
title: Master planlama sorunlarını giderme
description: Bu konu, master planlama üzerinde çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklamaktadır.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 44291f5bcd9ffedf717150f8efe32e9eeda02f2e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011371"
---
# <a name="troubleshoot-master-planning"></a><span data-ttu-id="824de-103">Master planlama sorunlarını giderme</span><span class="sxs-lookup"><span data-stu-id="824de-103">Troubleshoot master planning</span></span>

<span data-ttu-id="824de-104">Bu konu, master planlama üzerinde çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="824de-104">This topic describes how to fix issues that you might encounter while you work with master planning.</span></span>

## <a name="bill-of-materials-explosion-behaves-differently-for-firmed-production-orders-and-for-estimated-production-orders-for-manually-created-work"></a><span data-ttu-id="824de-105">Ürün reçetesi açılımı, kesinleştirilen üretim emirleri için ve el ile oluşturulmuş iş için tahmini üretim emirlerinde farklı şekilde davranır.</span><span class="sxs-lookup"><span data-stu-id="824de-105">Bill of materials explosion behaves differently for firmed production orders and for estimated production orders for manually created work.</span></span>

### <a name="issue-description"></a><span data-ttu-id="824de-106">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="824de-106">Issue description</span></span>

<span data-ttu-id="824de-107">Bir üretim emri kesinleştirildiğinde, ürün reçetesini açtığınızda maddeler açılmaz.</span><span class="sxs-lookup"><span data-stu-id="824de-107">When a production order is firmed, the items aren't exploded when you explode the bill of materials (BOM).</span></span> <span data-ttu-id="824de-108">Ancak, bir iş emrini el ile oluşturduğunuzda ve üretim emrini tahmin ettiğinizde, maddeler açılır.</span><span class="sxs-lookup"><span data-stu-id="824de-108">However, when you manually create a work order and then estimate the production order, the items are exploded.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="824de-109">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="824de-109">Issue resolution</span></span>

<span data-ttu-id="824de-110">Sistem beklendiği gibi çalışmaktadır.</span><span class="sxs-lookup"><span data-stu-id="824de-110">The system is working as expected.</span></span> <span data-ttu-id="824de-111">Üretim emri kesinleştirildiğinde gerçekleşen açılım, planlı siparişi işaret eder ancak bu durumda planlı sipariş kesinleştirilmiş olduğu görünmüyor.</span><span class="sxs-lookup"><span data-stu-id="824de-111">The explosion that occurs when the production order is firmed will point to the planned order, but it doesn't appear that the planned order is currently firmed in this case.</span></span> <span data-ttu-id="824de-112">Ancak üretim emri tahmin edildiyse açılım, planlanmış sipariş bulunmayan serbest bırakılmış üretim emrinden tetiklenir.</span><span class="sxs-lookup"><span data-stu-id="824de-112">However, if the production order has been estimated, the explosion is triggered from the released production order where no planned order exists.</span></span>

## <a name="the-delay-value-isnt-updated-when-i-reschedule-a-planned-order"></a><span data-ttu-id="824de-113">Planlanan bir siparişi yeniden zamanladıktan sonra, Gecikme değeri güncelleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="824de-113">The Delay value isn't updated when I reschedule a planned order.</span></span>

<span data-ttu-id="824de-114">Planlı sipariş gecikmesini güncelleştirmek için planlı sipariş için **Yeniden Programlama** iletişim kutusunu açın.</span><span class="sxs-lookup"><span data-stu-id="824de-114">To update the delay for planned orders, open the **Rescheduling** dialog box for the planned order.</span></span> <span data-ttu-id="824de-115">**Açılım** hızlı sekmesinde, **Yeniden programlamadan sonra açılım gerçekleştir** seçeneğinin *Evet* olarak ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="824de-115">On the **Explosion** FastTab, make sure that the **Perform explosion after rescheduling** option is set to *Yes*.</span></span>

## <a name="production-scheduling-doesnt-consider-the-safety-margins-that-are-set-on-the-item-coverage-for-pegged-supply"></a><span data-ttu-id="824de-116">Üretim programlaması, ilişkilendirilmiş arz için madde karşılamasının ayarlandığı emniyet marjlarını dikkate almaz.</span><span class="sxs-lookup"><span data-stu-id="824de-116">Production scheduling doesn't consider the safety margins that are set on the item coverage for pegged supply.</span></span>

### <a name="issue-description"></a><span data-ttu-id="824de-117">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="824de-117">Issue description</span></span>

<span data-ttu-id="824de-118">Master planlama emniyet marjlarını dikkate alır.</span><span class="sxs-lookup"><span data-stu-id="824de-118">Master planning considers the safety margins.</span></span> <span data-ttu-id="824de-119">Ancak planlanan üretim emirleri planlandığında emniyet marjları yoksayılır.</span><span class="sxs-lookup"><span data-stu-id="824de-119">However, the safety margins are ignored when planned production orders are scheduled.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="824de-120">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="824de-120">Issue resolution</span></span>

<span data-ttu-id="824de-121">Marjlar yalnızca master planlama sırasında değerlendirilir, el ile zamanlama sırasında değil.</span><span class="sxs-lookup"><span data-stu-id="824de-121">Margins are considered only during master planning, not during manual scheduling.</span></span> <span data-ttu-id="824de-122">Marjlar planlama aşamasında, gerçek işleme "marj" vermek için bir tampon olarak çalışacak şekilde tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="824de-122">Margins are designed to act as a buffer during the planning phase, to give some "margin" for the actual process.</span></span>

<span data-ttu-id="824de-123">İstenen sonuca ulaşmak için marjı kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="824de-123">To get the desired result, you can remove the margin.</span></span> <span data-ttu-id="824de-124">Rotanın istenen saati (örneğin, kuyruk süresi olarak) içermesi için güncelleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="824de-124">The route must then be updated so that it includes the desired time (for example, as queue time).</span></span> <span data-ttu-id="824de-125">Hem master planlama hem de el ile programlamanın aynı sonucu üretmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="824de-125">Both master planning and manual scheduling should then produce the same result.</span></span>

## <a name="planned-orders-are-generated-even-though-we-have-items-in-stock-and-production-orders-already-exist-for-them"></a><span data-ttu-id="824de-126">Stokta maddeler ve maddeler için üretim emirleri olsa bile planlı siparişler oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="824de-126">Planned orders are generated even though we have items in stock and production orders already exist for them.</span></span>

<span data-ttu-id="824de-127">**Kapsam grubu** sayfasında, ilgili grupların **Pozitif günler** değerlerini artırarak bu sorunu giderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="824de-127">You might be able to fix this issue by increasing the **Positive days** value for the relevant groups on the **Coverage group** page.</span></span> <span data-ttu-id="824de-128">Bu değişiklik, sistemin talep için eldeki stoğun kullanılabileceği konusunda karar vermesine neden olur.</span><span class="sxs-lookup"><span data-stu-id="824de-128">This change will cause the system to determine whether on-hand inventory can be used for the demand.</span></span> <span data-ttu-id="824de-129">Daha sonra, stokta bulunan maddeler için yeni bir planlı sipariş oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="824de-129">Then a new planned order won't be generated for the items that are in stock.</span></span>

## <a name="master-planning-doesnt-seem-to-respect-capacity-limitations-and-is-scheduling-more-than-the-available-capacity"></a><span data-ttu-id="824de-130">Master planlama, kapasite sınırlamalarını dikkate almıyor ve kullanılabilir kapasitenin fazlasını planlıyor.</span><span class="sxs-lookup"><span data-stu-id="824de-130">Master planning doesn't seem to respect capacity limitations and is scheduling more than the available capacity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="824de-131">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="824de-131">Issue description</span></span>

<span data-ttu-id="824de-132">Sınırlı kapasite bulunan ve rotanın hem bir kaynak grubu hem de bağımsız kaynaklar için çeşitli gereksinimler belirttiği durumlarda işlem programlamayı kullandığınızda, algoritmanın kapasite çakışmalarını doğrulama biçimi nedeniyle küçük bir aşırı planlama olasılığı vardır.</span><span class="sxs-lookup"><span data-stu-id="824de-132">When you use operation scheduling where there is finite capacity, and where the route specifies a mix of requirements for both a resource group and individual resources, there is a small chance of overbooking because of the way that the algorithm validates for capacity conflicts.</span></span> <span data-ttu-id="824de-133">Bu fazla planlama, master planlamayı çalıştırmak için yardımcıları kullandığınızda ortaya çıkabilir.</span><span class="sxs-lookup"><span data-stu-id="824de-133">This overbooking can occur when you use helpers to run master planning.</span></span> <span data-ttu-id="824de-134">Görece daha kısa bir çalışma zamanı olan birçok iş olduğunda ortaya çıkması olasıdır.</span><span class="sxs-lookup"><span data-stu-id="824de-134">It's most likely to occur if there are many jobs that have a relatively short runtime.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="824de-135">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="824de-135">Issue resolution</span></span>

<span data-ttu-id="824de-136">İşlem programlama için hiçbir fazla planlama oluşmuyorsa **Master planlama parametreleri** sayfasında **İşlem Programlaması için Sınırlı Doğru Kapasite**'yi açarak master planlamanın programlama bölümünü tekli iş parçacıklı hale getirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="824de-136">If it's essential that no overbooking occur for operation scheduling, you can make the scheduling part of master planning single-threaded by turning on the **Accurate finite capacity for Operation Scheduling** option on the **Master planning parameters** page.</span></span> <span data-ttu-id="824de-137">Bu seçenek varsayılan olarak kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="824de-137">This option isn't available by default.</span></span> <span data-ttu-id="824de-138">Kişiselleştirme özelliklerini kullanarak bunu sayfaya el ile eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="824de-138">You must manually add it to the page by using personalization features.</span></span> <span data-ttu-id="824de-139">Bu seçeneği kullandığınızda, paralel işlem olmaması nedeniyle planlama daha yavaş çalışır.</span><span class="sxs-lookup"><span data-stu-id="824de-139">When you use this option, scheduling will run more slowly because of the lack of parallel processing.</span></span>

## <a name="planned-orders-take-a-long-time-to-update"></a><span data-ttu-id="824de-140">Planlı siparişlerin güncelleştirilmesi uzun zaman alabilir.</span><span class="sxs-lookup"><span data-stu-id="824de-140">Planned orders take a long time to update.</span></span>

### <a name="issue-description"></a><span data-ttu-id="824de-141">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="824de-141">Issue description</span></span>

<span data-ttu-id="824de-142">Planlı bir siparişte gereksinim miktarı ve/veya teslimat tarihi güncelleştirilirken, güncelleştirmeyi kaydetmek için genellikle sipariş başına en az 30 saniye süre gerekir.</span><span class="sxs-lookup"><span data-stu-id="824de-142">When updating the requirement quantity and/or delivery date on a planned order, it typically takes at least 30 seconds per order to save the update.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="824de-143">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="824de-143">Issue resolution</span></span>

<span data-ttu-id="824de-144">Bu, yerleşik master planlama altyapısında oluşan bilinen bir sorundur.</span><span class="sxs-lookup"><span data-stu-id="824de-144">This is a known issue with the built-in master planning engine.</span></span> <span data-ttu-id="824de-145">Düzenleme sırasında, ürün reçetesi yapısı üzerinden, temel alınan otomatik açılımdan kaynaklanır.</span><span class="sxs-lookup"><span data-stu-id="824de-145">It is caused by the underlying auto explosion through the BOM structure during edits.</span></span> <span data-ttu-id="824de-146">Bu sorun, Planlama İyileştirmesi'nde giderilmiştir ve burada bir planlayıcı ilgili siparişleri güncelleştirebilir ve onaylayabilir ve istendiğinde, temel alınan ürün reçetesi yapısı için planlı siparişleri güncelleştirmek amacıyla bir planlama çalıştırmasını tetikleyebilir.</span><span class="sxs-lookup"><span data-stu-id="824de-146">This issue is addressed in Planning Optimization, where a planner can update and approve the relevant orders and, when desired, trigger a planning run to update planned orders for the underlying BOM structure.</span></span>

<span data-ttu-id="824de-147">Yerleşik master planlama altyapısıyla performansı artırmanın bir yolu aşağıdakileri yapmaktır:</span><span class="sxs-lookup"><span data-stu-id="824de-147">One way to improve performance with the built-in master planning engine is to do the following:</span></span>

1. <span data-ttu-id="824de-148">**Master planlama \> Kurulum \> Planlar \> Master planlar** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="824de-148">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="824de-149">Plan seçin.</span><span class="sxs-lookup"><span data-stu-id="824de-149">Select a plan.</span></span>
1. <span data-ttu-id="824de-150">**Gün cinsinden zaman dilimi** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="824de-150">Expand the **Time fence in days** FastTab.</span></span>
1. <span data-ttu-id="824de-151">**Açılım**'ı *Evet* olarak ayarlayın ve bu ayarın altındaki alanı 0 (sıfır) olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="824de-151">Set **Explosion** to *Yes*, and set the field below this setting to 0 (zero).</span></span>

> [!NOTE]
> <span data-ttu-id="824de-152">Bu, bu master plan için gerçekleştirilen açılımları tek bir güne sınırlandırır.</span><span class="sxs-lookup"><span data-stu-id="824de-152">This will limit the period for explosions performed for this master plan to a single day.</span></span>
