---
title: Vergi hesaplaması performansı, hareketleri etkiliyor
description: Bu konu, vergi hesaplama performansı ve bu performansın hareketler üzerindeki etkisiyle ilgili sorun giderme bilgiler sağlar.
author: shtao
manager: beya
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7ff9d9b80172c3b337737b1cd53b4c56d1befe57
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947725"
---
# <a name="tax-calculation-performance-affects-transactions"></a><span data-ttu-id="b034e-103">Vergi hesaplaması performansı, hareketleri etkiliyor</span><span class="sxs-lookup"><span data-stu-id="b034e-103">Tax calculation performance affects transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b034e-104">Bazen bir hareket, vergi hesaplamasında bulunan performans sorunlarından etkilenir.</span><span class="sxs-lookup"><span data-stu-id="b034e-104">Sometimes, a transaction is affected by performance issues that tax calculation is having.</span></span> <span data-ttu-id="b034e-105">Bu sorunu gidermek için, aşağıdaki bölümlerde gereken adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b034e-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="review-the-transaction-line-count"></a><span data-ttu-id="b034e-106">Hareket satır sayısını gözden geçirin</span><span class="sxs-lookup"><span data-stu-id="b034e-106">Review the transaction line count</span></span>

<span data-ttu-id="b034e-107">Hareketin çok sayıda satırı olup olmadığını (örneğin, birkaç yüz) belirleyin.</span><span class="sxs-lookup"><span data-stu-id="b034e-107">Determine whether the transaction has a large number of lines (for example, more than several hundred).</span></span> <span data-ttu-id="b034e-108">Çok sayıda satır yoksa bir sonraki bölüme geçin.</span><span class="sxs-lookup"><span data-stu-id="b034e-108">If it doesn't, move on to the next section.</span></span> <span data-ttu-id="b034e-109">Harekette birkaç yüz satır varsa, vergi hesaplamasını erteleyin.</span><span class="sxs-lookup"><span data-stu-id="b034e-109">If the transaction does have several hundred lines, delay the tax calculation.</span></span> <span data-ttu-id="b034e-110">Daha fazla bilgi için bkz. [Defterlerde ertelenmiş vergi hesaplamayı etkinleştirme](enable-delayed-tax-calculation.md).</span><span class="sxs-lookup"><span data-stu-id="b034e-110">For more information, see [Enable delayed tax calculation on journals](enable-delayed-tax-calculation.md).</span></span> 

<span data-ttu-id="b034e-111">Ardından, aşağıdaki koşullardan herhangi birinin yerine getirilip getirilmediğini belirleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="b034e-111">Next, you can determine whether any of the following conditions are met:</span></span>

- <span data-ttu-id="b034e-112">Büyük dosyalardan içe aktarma hareketleri var.</span><span class="sxs-lookup"><span data-stu-id="b034e-112">There are import transactions from large files.</span></span>
- <span data-ttu-id="b034e-113">Aynı anda birden çok oturum, aynı hareket vergisi hesaplamasını işliyor.</span><span class="sxs-lookup"><span data-stu-id="b034e-113">Multiple sessions process the same transaction tax calculation at the same time.</span></span>
- <span data-ttu-id="b034e-114">Hareketin birden çok satırı var ve görünümler gerçek zamanlı olarak güncelleştiriliyor.</span><span class="sxs-lookup"><span data-stu-id="b034e-114">The transaction has multiple lines, and the views are updated in real time.</span></span> <span data-ttu-id="b034e-115">Örneğin, bir satırın alanları değiştirildiğinde, **Genel günlük** sayfasındaki **Hesaplanan satış vergisi tutarı** alanı gerçek zamanlı olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="b034e-115">For example, the **Calculated sales tax amount** field on the **General journal** page is updated in real time when a line's fields are changed.</span></span>

   <span data-ttu-id="b034e-116">[![Günlük fişi sayfasındaki hesaplanan satış vergisi tutarı alanı](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="b034e-116">[![Calculated sales tax amount field on the Jounal voucher page](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)</span></span>

<span data-ttu-id="b034e-117">Bu durumlardan herhangi biri geçerliyse vergi hesaplamasını erteleyin.</span><span class="sxs-lookup"><span data-stu-id="b034e-117">If any of these conditions are met, delay the tax calculation.</span></span>

## <a name="review-the-call-stack"></a><span data-ttu-id="b034e-118">Çağrı yığınını gözden geçirin</span><span class="sxs-lookup"><span data-stu-id="b034e-118">Review the call stack</span></span>

<span data-ttu-id="b034e-119">Vergi hesaplamasının birden çok kez çağrılıp çağrılmadığını belirlemek için çağrı yığınını gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="b034e-119">Review the call stack to determine whether tax calculation is called multiple times.</span></span> <span data-ttu-id="b034e-120">Çok defa çağrılmadıysa bir sonraki bölüme geçin.</span><span class="sxs-lookup"><span data-stu-id="b034e-120">If it isn't, move on to the next section.</span></span> <span data-ttu-id="b034e-121">Çağrı yığını çok defa çağrılmışsa vergi hesaplama zamanlarının azaltılmasına yardımcı olacak aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b034e-121">If the call stack is called multiple times, follow these steps to help reduce the tax calculation times.</span></span>

1. <span data-ttu-id="b034e-122">Defter, hareketi ele aldıysa vergi hesaplamayı erteleyin.</span><span class="sxs-lookup"><span data-stu-id="b034e-122">If the journal has considered the transaction, delay the tax calculation.</span></span> <span data-ttu-id="b034e-123">Daha fazla bilgi için bkz. [Defterlerde ertelenmiş vergi hesaplamayı etkinleştirme](enable-delayed-tax-calculation.md).</span><span class="sxs-lookup"><span data-stu-id="b034e-123">For more information, see [Enable delayed tax calculation on journals](enable-delayed-tax-calculation.md).</span></span>
2. <span data-ttu-id="b034e-124">Hareket bir satınalma siparişi ise ve uygulama sürümü 10.0.15'den daha yeni ise, **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch** için denemeyi etkinleştirerek, vergi hesaplamasını son hesaplamaya kadar erteleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b034e-124">If the transaction is a purchase order, and the application version is later than 10.0.15, you can delay the tax calculation until the final calculation by enabling the flighting for **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch**.</span></span>

## <a name="review-the-call-stack-timeline"></a><span data-ttu-id="b034e-125">Çağrı yığını zaman çizelgesini gözden geçirin</span><span class="sxs-lookup"><span data-stu-id="b034e-125">Review the call stack timeline</span></span>

<span data-ttu-id="b034e-126">Aşağıdaki sorunların mevcut olup olmadığını belirlemek için çağrı yığını zaman çizelgesini gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="b034e-126">Review the call stack timeline to determine whether the following issues exist.</span></span> <span data-ttu-id="b034e-127">Bunlar mevcutsa sorunu gidermek için **TaxUncommittedDoIsolateScopeFlighting** için denemeyi etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="b034e-127">If they do, enable the flighting for **TaxUncommittedDoIsolateScopeFlighting** to fix the issue.</span></span>

- <span data-ttu-id="b034e-128">Hareket, sistemin oturum sona erene kadar yanıt vermemesine neden olur.</span><span class="sxs-lookup"><span data-stu-id="b034e-128">The transaction causes the system to stop responding until the session ends.</span></span> <span data-ttu-id="b034e-129">Bu nedenle, hareket vergi sonucunu hesaplayamıyor.</span><span class="sxs-lookup"><span data-stu-id="b034e-129">Therefore, the transaction can't calculate the tax result.</span></span> <span data-ttu-id="b034e-130">Aşağıdaki görselde, aldığınız "Oturum sona erdi" ileti kutusu gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="b034e-130">The following illustration shows the "Session ended" message box that you receive.</span></span>

    <span data-ttu-id="b034e-131">[![Oturum bitti iletisi](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="b034e-131">[![Session ended message](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)</span></span>

- <span data-ttu-id="b034e-132">**TaxUncommitted** yöntemleri, diğer yöntemlerden daha fazla zaman alabilir.</span><span class="sxs-lookup"><span data-stu-id="b034e-132">The **TaxUncommitted** methods take more time than other methods.</span></span> <span data-ttu-id="b034e-133">Örneğin, aşağıdaki görselde **TaxUncommitted::updateTaxUncommitted()** yöntemi 43,347.42 saniye sürer ancak diğer yöntemler 0,09 saniye sürer.</span><span class="sxs-lookup"><span data-stu-id="b034e-133">For example, in the following illustration, the **TaxUncommitted::updateTaxUncommitted()** method takes 43,347.42 seconds, but other methods take 0.09 seconds.</span></span>

    <span data-ttu-id="b034e-134">[![Yöntem süreleri](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="b034e-134">[![Method durations](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)</span></span>

## <a name="customizing-and-calling-tax-calculation"></a><span data-ttu-id="b034e-135">Vergi hesaplamasını özelleştirme ve çağırma</span><span class="sxs-lookup"><span data-stu-id="b034e-135">Customizing and calling tax calculation</span></span>

<span data-ttu-id="b034e-136">Özelleştirdiğinizde, her satır için **insert()** veya **update()** yönteminde vergi hesaplamasını çağırmayın.</span><span class="sxs-lookup"><span data-stu-id="b034e-136">When you customize, don't call tax calculation at the **insert()** or **update()** method for each line.</span></span> <span data-ttu-id="b034e-137">Vergi hesaplaması, hareket düzeyinde çağrılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b034e-137">Tax calculation should be called at the transaction level.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="b034e-138">Özelleştirme olup olmadığını belirleyin</span><span class="sxs-lookup"><span data-stu-id="b034e-138">Determine whether customization exists</span></span>

<span data-ttu-id="b034e-139">Önceki bölümlerdeki adımları tamamladıysanız ve bir sorun bulamadıysanız bir özelleştirme olup olmadığını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="b034e-139">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="b034e-140">Hiçbir özelleştirme yoksa daha fazla destek için bir Microsoft servis talebi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b034e-140">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
