---
title: Kanban miktarı önerilerini hesaplama
description: Bu yordam, kanban boyutunu ve miktarlarını belirli bir kanban kuralı için, kanban miktarı hesaplamayı kullanarak en iyi duruma getirme üzerinde odaklanır.
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 540dd32c5da5859ef5e69f55d6806eada90bc840
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558207"
---
# <a name="calculate-kanban-quantity-suggestions"></a><span data-ttu-id="bf567-103">Kanban miktarı önerilerini hesaplama</span><span class="sxs-lookup"><span data-stu-id="bf567-103">Calculate kanban quantity suggestions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bf567-104">Bu yordam, kanban boyutunu ve miktarlarını belirli bir kanban kuralı için, kanban miktarı hesaplamayı kullanarak en iyi duruma getirme üzerinde odaklanır.</span><span class="sxs-lookup"><span data-stu-id="bf567-104">This procedure focuses on optimizing the kanban size and quantities for a specific kanban rule by using the kanban quantity calculation.</span></span> <span data-ttu-id="bf567-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="bf567-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="bf567-106">Bu yordam değer akışı yöneticisi için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="bf567-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="bf567-107">Yeni bir kanban miktar hesaplama ilkesini bir kanban kuralına ekle yordamını tamamlamış olmanız bir önkoşuldur.</span><span class="sxs-lookup"><span data-stu-id="bf567-107">It is a prerequisite that you have completed the procedure Add a new kanban quantity calculation policy to a kanban rule.</span></span>


## <a name="create-a-kanban-quantity-calculation"></a><span data-ttu-id="bf567-108">Bir kanban miktar hesaplaması oluşturun</span><span class="sxs-lookup"><span data-stu-id="bf567-108">Create a kanban quantity calculation</span></span>
1. <span data-ttu-id="bf567-109">Üretim kontrol > Periyodik görevler > Kanban miktarı hesaplama > Kanban miktarı hesapla seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="bf567-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Calculate kanban quantity.</span></span>
2. <span data-ttu-id="bf567-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bf567-110">Click New.</span></span>
3. <span data-ttu-id="bf567-111">İsim alanına 'Speaker2016' yazın.</span><span class="sxs-lookup"><span data-stu-id="bf567-111">In the Name field, type 'Speaker2016'.</span></span>
4. <span data-ttu-id="bf567-112">Ad alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="bf567-112">In the Name field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="bf567-113">Kanban kural için yeni bir kanban miktarı hesaplama İlkesi ekle yordamında oluşturduğunuz ilkeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="bf567-113">Select the policy that you have created in the procedure Add a new kanban quantity calculation policy to a kanban rule.</span></span> <span data-ttu-id="bf567-114">Örneğin Speaker2016.</span><span class="sxs-lookup"><span data-stu-id="bf567-114">For example, Speaker2016.</span></span>  
5. <span data-ttu-id="bf567-115">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bf567-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="bf567-116">Kuralın aktif olacağı tarih alanına tarih ve saati '2012-12-17T08:00:00' olarak yazın.</span><span class="sxs-lookup"><span data-stu-id="bf567-116">In the Rule active as of date field, set the date and time to '2012-12-17T08:00:00'.</span></span>
    * <span data-ttu-id="bf567-117">Bu tarih, Kanban miktarı hesaplamasına hangi sabit kanban kurallarının dahil edileceğinin belirlenmesi için temel olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bf567-117">This date serves as the basis for determining which fixed kanban rules are included in the kanban quantity calculation.</span></span>  
7. <span data-ttu-id="bf567-118">Kuralın aktif olacağı tarih alanına tarih ve saati '2012-11-17T09:00:00' yazın.</span><span class="sxs-lookup"><span data-stu-id="bf567-118">In the Fulfilled demand period start date field, set the date and time to '2012-11-17T09:00:00'.</span></span>
    * <span data-ttu-id="bf567-119">Kanban miktarını hesaplamak için geçmiş talep hareketlerinin dahil edilmeye başlayacağı tarih.</span><span class="sxs-lookup"><span data-stu-id="bf567-119">The date from when past demand transactions are included to calculate the kanban quantity.</span></span>  
8. <span data-ttu-id="bf567-120">Tamamlanan isteğin dönem bitiş tarihi alanına, tarihi ve saati '2012-12-17T07:59:59' olarak yazın.</span><span class="sxs-lookup"><span data-stu-id="bf567-120">In the Fulfilled demand period end date field, set the date and time to '2012-12-17T07:59:59'.</span></span>
    * <span data-ttu-id="bf567-121">Kanban miktarını hesaplamak için geçmiş talep hareketlerinin dahil edileceği son tarih.</span><span class="sxs-lookup"><span data-stu-id="bf567-121">The date until when past demand transactions are included to calculate the kanban quantity.</span></span>  
9. <span data-ttu-id="bf567-122">Talep tarihi başlangıç zamanı alanına, tarihi ve saati '2012-12-17T08:00:00' olarak yazın.</span><span class="sxs-lookup"><span data-stu-id="bf567-122">In the Demand period start date field, set the date and time to '2012-12-17T08:00:00'.</span></span>
    * <span data-ttu-id="bf567-123">Kanban miktarını hesaplamak için geçerli talep hareketlerinin dahil edilmeye başlayacağı tarih.</span><span class="sxs-lookup"><span data-stu-id="bf567-123">The date from when current demand transactions are included to calculate the kanban quantity.</span></span>  
10. <span data-ttu-id="bf567-124">Talep dönem bitiş tarihi alanına, tarihi ve saati '2013-01-16T07:59:59' olarak yazın.</span><span class="sxs-lookup"><span data-stu-id="bf567-124">In the Demand period end date field, set the date and time to '2013-01-16T07:59:59'.</span></span>
    * <span data-ttu-id="bf567-125">Kanban miktarını hesaplamak için geçerli talep hareketlerinin dahil edileceği son tarih.</span><span class="sxs-lookup"><span data-stu-id="bf567-125">The date until when current demand transactions are included to calculate the kanban quantity.</span></span>  

## <a name="generate-kanban-quantity-proposal"></a><span data-ttu-id="bf567-126">Kanban miktarı teklifi oluşturun</span><span class="sxs-lookup"><span data-stu-id="bf567-126">Generate kanban quantity proposal</span></span>
1. <span data-ttu-id="bf567-127">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bf567-127">Click Save.</span></span>
2. <span data-ttu-id="bf567-128">Üret'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bf567-128">Click Generate.</span></span>
    * <span data-ttu-id="bf567-129">Bu 000020 kanban kuralı için bir kanban miktar teklif satırı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bf567-129">This generates a kanban quantity proposal line for the kanban rule 000020.</span></span>  

## <a name="run-kanban-quantity-calculation"></a><span data-ttu-id="bf567-130">Kanban miktarı hesaplamasını çalıştırın</span><span class="sxs-lookup"><span data-stu-id="bf567-130">Run kanban quantity calculation</span></span>
1. <span data-ttu-id="bf567-131">Hesapla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bf567-131">Click Calculate.</span></span>
    * <span data-ttu-id="bf567-132">Bu kanban miktarı teklifini hesaplar.</span><span class="sxs-lookup"><span data-stu-id="bf567-132">This calculates the kanban quantity proposal.</span></span>  
2. <span data-ttu-id="bf567-133">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bf567-133">Click OK.</span></span>
3. <span data-ttu-id="bf567-134">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bf567-134">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="bf567-135">Önerilen kanban miktarının 2 olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="bf567-135">Notice the suggested kanban quantity is 2.</span></span>  

## <a name="change-product-quantity-and-calculate-again"></a><span data-ttu-id="bf567-136">Ürün miktarını değiştirin ve yeniden hesaplayın</span><span class="sxs-lookup"><span data-stu-id="bf567-136">Change product quantity and calculate again</span></span>
1. <span data-ttu-id="bf567-137">Toplam ürün miktarını '5'e ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="bf567-137">Set Product quantity to '5'.</span></span>
2. <span data-ttu-id="bf567-138">Hesapla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bf567-138">Click Calculate.</span></span>
3. <span data-ttu-id="bf567-139">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bf567-139">Click OK.</span></span>
    * <span data-ttu-id="bf567-140">5 kanban miktarı ile önerinin 4 kanban miktarına değiştirildiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="bf567-140">Notice that with a kanban quantity of 5, the suggestion is changed to a kanban quantity of 4.</span></span>  
    * <span data-ttu-id="bf567-141">Daha az ürün miktarıyla, talebini karşılamak için daha fazla kanbana gerek duyuyor olduğumuz gerçeğinden kaynaklanır.</span><span class="sxs-lookup"><span data-stu-id="bf567-141">This is caused by the fact that with a lower product quantity, we need more kanbans to fulfill the demand.</span></span>  

## <a name="update-kanban-rule"></a><span data-ttu-id="bf567-142">Kanban kuralını güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="bf567-142">Update kanban rule</span></span>
1. <span data-ttu-id="bf567-143">Kural yürürlük tarihi alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="bf567-143">In the Rule effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="bf567-144">'Kural tarihi itibariyle etkin' gelecekte bir tarih olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="bf567-144">Set the 'Rule active as of date' to a date in the future.</span></span> <span data-ttu-id="bf567-145">Örneğin, bugün + bir yıl.</span><span class="sxs-lookup"><span data-stu-id="bf567-145">For example, today + one year.</span></span>  
2. <span data-ttu-id="bf567-146">Güncelleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bf567-146">Click Update.</span></span>
3. <span data-ttu-id="bf567-147">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bf567-147">Click OK.</span></span>
4. <span data-ttu-id="bf567-148">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="bf567-148">Close the page.</span></span>

## <a name="validate-change-on-kanban-rule"></a><span data-ttu-id="bf567-149">Kanban kural değişimini doğrulayın</span><span class="sxs-lookup"><span data-stu-id="bf567-149">Validate change on kanban rule</span></span>
1. <span data-ttu-id="bf567-150">Ürün bilgi yönetimi > Yalın imalat > Kanban kuralları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="bf567-150">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="bf567-151">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bf567-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="bf567-152">Önceki alt görevinde oluşturulan kanban kuralını seçin.</span><span class="sxs-lookup"><span data-stu-id="bf567-152">Select the kanban rule that was created in the previous sub-task.</span></span> <span data-ttu-id="bf567-153">Bu listede, numarasına göre sıralanmış ilk kanban kuralı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="bf567-153">This should be the first kanban rule in the list sorted by number.</span></span>  
3. <span data-ttu-id="bf567-154">Ayrıntılar bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="bf567-154">Toggle the expansion of the Details section.</span></span>
    * <span data-ttu-id="bf567-155">Bu tarihe kadar kuralın etkin hale gelmeyeceği anlamına gelen etkin tarihe dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="bf567-155">Notice the effective date, which means that this rule is not activated until this date.</span></span>  
4. <span data-ttu-id="bf567-156">Miktarlar bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="bf567-156">Toggle the expansion of the Quantities section.</span></span>
    * <span data-ttu-id="bf567-157">Bunun kanban miktarı hesaplamak için girilen varsayılan miktar olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="bf567-157">Notice this is the default quantity that you entered on the kanban quantity calculation.</span></span>  
    * <span data-ttu-id="bf567-158">Bu kanban miktar hesaplamasından gelen sabit kanban miktarı olan 4'tür.</span><span class="sxs-lookup"><span data-stu-id="bf567-158">Notice this is the fixed kanban quantity of 4 from the kanban quantity calculation.</span></span>  
5. <span data-ttu-id="bf567-159">ListPanel sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bf567-159">Click the ListPanel tab.</span></span>

