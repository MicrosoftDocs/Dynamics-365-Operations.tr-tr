---
title: Bonus amortisman
description: "Bu makalede, bonus amortisman işlevselliğine bir genel bakış verilmektedir."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBonus
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3621
ms.assetid: 835ec594-744e-461c-a676-1b9abc094173
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 48d50cbba648beb9831e186cd160853abe79c4e4
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="bonus-depreciation"></a><span data-ttu-id="c2392-103">Bonus amortisman</span><span class="sxs-lookup"><span data-stu-id="c2392-103">Bonus depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c2392-104">Bu makalede, bonus amortisman işlevselliğine bir genel bakış verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="c2392-104">This article provides an overview of the bonus depreciation functionality.</span></span>

<span data-ttu-id="c2392-105">Ek amortisman için, kıymetin hizmete girdiği ve amortisman uygulandığı ilk yıl boyunca ek amortisman tutarları alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c2392-105">For bonus depreciation, you can take extra or bonus depreciation amounts during the first year that the asset is put in service and depreciated.</span></span> <span data-ttu-id="c2392-106">Ek amortismanın, diğer her türlü amortisman hesaplamasından önce alınması gerekir.</span><span class="sxs-lookup"><span data-stu-id="c2392-106">Bonus depreciation must be taken before any other depreciation calculations.</span></span> <span data-ttu-id="c2392-107">Bu nedenle, genel muhasebe işlemlerine nakil devre dışı olduğunda defterlerle ek amortismanı kullanmak en iyisidir.</span><span class="sxs-lookup"><span data-stu-id="c2392-107">Therefore, it's best to use bonus depreciation with books where the Post to general ledger functionality is disabled.</span></span> <span data-ttu-id="c2392-108">Genel muhasebeye nakledilmeyen defterler için geçmiş hareketleri silmek için **Genel muhasebe defterine nakledilmeyen hareketleri sil** seçeneğini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c2392-108">You can use the **Delete transactions not posted to general ledger** option to delete historical transactions for books that don't post to the general ledger.</span></span> <span data-ttu-id="c2392-109">Daha önceden nakledilen amortisman hareketlerini silerek kıymet yaşam döngüsünde ek amortismanı barındırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c2392-109">You can then accommodate bonus depreciation later in the asset life cycle by deleting depreciation transactions that were previously posted.</span></span> 

<span data-ttu-id="c2392-110">Ek amortismanı, teklif işlemini kullanarak hesaplayabilir veya el ile ek amortisman hareketleri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c2392-110">You can calculate bonus depreciation by using the proposal process, or you can create manual bonus depreciation transactions.</span></span> <span data-ttu-id="c2392-111">Kıymet defteri için amortisman hareketleri veya amortisman düzeltme hareketleri varsa, ek amortisman hareketleri oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="c2392-111">You can't create bonus depreciation transactions if depreciation transactions or depreciation adjustment transactions exist for that asset book.</span></span>

<span data-ttu-id="c2392-112">Ek amortismanı hesaplamak için teklif işlemini kullandığınızda, varolan tüm ek hareketler temel hesaplamasına dahil.</span><span class="sxs-lookup"><span data-stu-id="c2392-112">When you use the proposal process to calculate bonus depreciation, all existing bonus transactions are included in the calculation of the basis.</span></span> <span data-ttu-id="c2392-113">Bu hesaplama, kıymet için el ile girdiğiniz önceki ek amortismanları da içerir.</span><span class="sxs-lookup"><span data-stu-id="c2392-113">The calculation also includes any previous bonus depreciations that you manually entered for the asset.</span></span> 

<span data-ttu-id="c2392-114">Kıymet için alınacak birden fazla ek amortisman varsa öncelik dikkate alınır.</span><span class="sxs-lookup"><span data-stu-id="c2392-114">If more than one bonus depreciation will be taken for an asset, the priority is considered.</span></span> <span data-ttu-id="c2392-115">Her ek, bir sonraki ekin kıymet temelini düşürür.</span><span class="sxs-lookup"><span data-stu-id="c2392-115">Each bonus reduces the asset basis for the next bonus.</span></span> <span data-ttu-id="c2392-116">Hurda değeri, ek amortisman hesaplamaları için kıymet temelinde hesaba katılmaz ve ek amortisman için amortisman yöntemi uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="c2392-116">Salvage value isn't considered in the asset basis for bonus depreciation calculations, and the depreciation convention doesn't apply for bonus depreciation.</span></span> 

<span data-ttu-id="c2392-117">Şu anda Amerika Birleşik Devletleri'nde bazı mülkiyetler, Bölüm 179 mülkiyeti olarak görülür.</span><span class="sxs-lookup"><span data-stu-id="c2392-117">Currently, in the United States, some property qualifies as Section 179 property.</span></span> <span data-ttu-id="c2392-118">Bölüm 179 kesintisini kullanarak, bazı mülkiyetlerin maliyetinin bir bölümünü veya tümünü (bir sınıra kadar) kurtarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c2392-118">By using the Section 179 deduction, you can recover all or part of the cost of some property, up to a limit.</span></span> <span data-ttu-id="c2392-119">Mülkiyeti servise koyduğunuz yıl indirim yaparak maliyet kurtarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c2392-119">You can recover the cost by deducting it in the year when you put the property in service.</span></span>

## <a name="example"></a><span data-ttu-id="c2392-120">Örnek</span><span class="sxs-lookup"><span data-stu-id="c2392-120">Example</span></span>
<span data-ttu-id="c2392-121">Aşağıdaki ek amortismanlar bir kıymet defteriyle ilişkilidir:</span><span class="sxs-lookup"><span data-stu-id="c2392-121">The following bonus depreciations are associated with an asset book:</span></span>

-   <span data-ttu-id="c2392-122">**Bölüm 179:** 1000,00, Öncelik 1</span><span class="sxs-lookup"><span data-stu-id="c2392-122">**Section 179:** 1,000.00, Priority 1</span></span>
-   <span data-ttu-id="c2392-123">**Serbest Bölge:** Yüzde 30, Öncelik 2</span><span class="sxs-lookup"><span data-stu-id="c2392-123">**Liberty Zone:** 30 percent, Priority 2</span></span>

<span data-ttu-id="c2392-124">Kıymetin alım maliyeti 5.000,00'dir.</span><span class="sxs-lookup"><span data-stu-id="c2392-124">The asset acquisition cost is 5,000.00.</span></span> <span data-ttu-id="c2392-125">Ek amortisman hesaplandığında ilk ek amortisman tutarı Bölüm 179 amortismanı için 1000,00'dir.</span><span class="sxs-lookup"><span data-stu-id="c2392-125">When bonus depreciation is calculated, the first bonus depreciation amount is 1,000.00 for the Section 179 depreciation.</span></span> 

<span data-ttu-id="c2392-126">Serbest Bölge amortismanı için sonraki ek amortisman tutarı şu şekilde hesaplanır:</span><span class="sxs-lookup"><span data-stu-id="c2392-126">The next bonus depreciation amount, for the Liberty Zone depreciation, is calculated as follows:</span></span> 

<span data-ttu-id="c2392-127">Alım maliyeti – 1000 (Bölüm 179 amortismanı) × yüzde 30 = 1.200</span><span class="sxs-lookup"><span data-stu-id="c2392-127">Acquisition cost – 1,000 (Section 179 depreciation) × 30 percent = 1,200</span></span> 

<span data-ttu-id="c2392-128">Ek amortisman tutarı, kalan alım maliyetinden daha fazlaysa ek amortisman tutarı, ek amortisman hesaplaması sonucu veya kalan amortisman alım maliyetidir (hangisi düşük ise).</span><span class="sxs-lookup"><span data-stu-id="c2392-128">If the bonus depreciation amount is more than the remaining acquisition cost, the bonus depreciation amount is either the result of the bonus depreciation calculation or the remaining acquisition cost, whichever amount is less.</span></span> 

<span data-ttu-id="c2392-129">Kalan alım maliyeti 0 (sıfır) veya sıfırdan düşükse ek amortisman hareketleri oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="c2392-129">If the remaining acquisition cost is 0 (zero) or less, bonus depreciation transactions isn't generated.</span></span> 

<span data-ttu-id="c2392-130">Ek amortisman, teklif işlemi kullanılarak hesaplandığında kıymet defteriyle ilişkili uygun tüm ek amortisman kayıtları için bir ek amortisman hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c2392-130">When bonus depreciation is calculated by using the proposal process, a bonus depreciation transaction is created for all applicable bonus depreciation records that are associated with the asset book.</span></span> 

<span data-ttu-id="c2392-131">Sınırsız sayıda bonus amortisman kaydı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c2392-131">You can create an unlimited number of bonus depreciation records.</span></span> <span data-ttu-id="c2392-132">Bu kayıtlar, kıymet grubu defterine atandıktan sonra kıymet defterine uygulanır.</span><span class="sxs-lookup"><span data-stu-id="c2392-132">After you assign those records to the asset group book, they are applied to the asset book.</span></span> 

<span data-ttu-id="c2392-133">Bonus amortisman bir yüzde veya sabit bir tutar olarak girilir.</span><span class="sxs-lookup"><span data-stu-id="c2392-133">Bonus depreciation is entered as either a percentage or a fixed amount.</span></span> <span data-ttu-id="c2392-134">Amortisman tekliflerini deftere naklettiğinizde, ek amortisman hareketleri amortisman defterine amortisman hareketlerinden ayrı hareketler olarak nakledilir.</span><span class="sxs-lookup"><span data-stu-id="c2392-134">When you post depreciation proposals, bonus depreciation transactions are posted to the book as separate transactions from the depreciation transactions.</span></span>




