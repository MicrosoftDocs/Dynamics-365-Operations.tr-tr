---
title: Emniyet marjları
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management güvenlik boşluklarının uygulamasında Planlamayı En İyi Duruma Getirme Eklentisi ile nasıl kullanılabileceği açıklanmaktadır.
author: ChristianRytt
manager: tfehr
ms.date: 09/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-9-14
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 05ac817081689f27cdf55cb86a3235d7707a737b
ms.sourcegitcommit: 5bb36b74935ffe140367fd6ecf956b4857ad12e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/14/2020
ms.locfileid: "3803433"
---
# <a name="safety-margins"></a><span data-ttu-id="94809-103">Emniyet marjları</span><span class="sxs-lookup"><span data-stu-id="94809-103">Safety margins</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="94809-104">Bu konuda, Microsoft Dynamics 365 Supply Chain Management güvenlik boşluklarının uygulamasında Planlamayı En İyi Duruma Getirme Eklentisi ile nasıl kullanılabileceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="94809-104">This topic describes how safety margins can be used with the Planning Optimization Add-in for Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="safety-margins-overview"></a><span data-ttu-id="94809-105">Emniyet marjlarına genel bakış</span><span class="sxs-lookup"><span data-stu-id="94809-105">Safety margins overview</span></span>

<span data-ttu-id="94809-106">Emniyet marjlarının amacı, normal sağlama süresinin ötesinde bazı tampon zaman sağlayan bir kurulumu etkinleştirmeyi sağlamaktır.</span><span class="sxs-lookup"><span data-stu-id="94809-106">The purpose of safety margins is to enable a setup that provides some buffer time beyond the normal lead time.</span></span> <span data-ttu-id="94809-107">Örneğin, satıcıdan alındıktan sonra malzemenin paketinden çıkarılarak incelenmesi gerektiğinde, yalnızca satınalma sağlama süresine ek süre ekleyemezsiniz, çünkü bu yaklaşım tedarikçiye ek tampon süre verir.</span><span class="sxs-lookup"><span data-stu-id="94809-107">For example, when material must be unpacked or inspected after it arrives from the vendor, you can't just add the extra time to the purchase lead time, because this approach will give the additional buffer time to the supplier.</span></span> <span data-ttu-id="94809-108">Bu örnekte, tedarikçinin daha erken teslim ettiğinden emin olmak için giriş marjı kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="94809-108">In this example, the receipt margin can be used to ensure that the supplier delivers earlier.</span></span> <span data-ttu-id="94809-109">Bu yaklaşım, malların içeride işlenebilmesi için tampon zaman sağlar.</span><span class="sxs-lookup"><span data-stu-id="94809-109">This approach provides buffer time so that the goods can be handled internally.</span></span>

<span data-ttu-id="94809-110">Üç tip emniyet marjı vardır:</span><span class="sxs-lookup"><span data-stu-id="94809-110">There are three types of safety margins:</span></span>

- <span data-ttu-id="94809-111">**Sipariş yenileme sınırı**: tedarik emrinin oluşturulması için tampon süre</span><span class="sxs-lookup"><span data-stu-id="94809-111">**Reorder margin** – The buffer time for placing the supply order</span></span>
- <span data-ttu-id="94809-112">**Giriş marjı**: gelen tedariki işlemek için tampon süre</span><span class="sxs-lookup"><span data-stu-id="94809-112">**Receipt margin** – The buffer time for handling incoming supply</span></span>
- <span data-ttu-id="94809-113">**Çıkış marjı**: sevkiyatların işlenmesi için tampon süre</span><span class="sxs-lookup"><span data-stu-id="94809-113">**Issue margin** – The buffer time for handling shipments</span></span>

<span data-ttu-id="94809-114">Aşağıdaki şekilde, bu emniyet marjlarının zamanla nasıl uygulanacağını gösterilir.</span><span class="sxs-lookup"><span data-stu-id="94809-114">The following illustration shows how these safety margins apply over time.</span></span>

![Emniyet marjları](media/safety-margins-1.png)

<span data-ttu-id="94809-116">Tüm marjlar gün olarak tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="94809-116">All margins are defined in days.</span></span> <span data-ttu-id="94809-117">Varsayılan değer olan *0* (sıfır) hiçbir marjın uygulanmadığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="94809-117">The default value, *0* (zero), indicates that no margin is applied.</span></span> <span data-ttu-id="94809-118">Birden fazla marj ayarlarsanız, bunların tümü tedarik *emri tarihinden* talep *gereksinim tarihine* kadar olan toplam zamana eklenir.</span><span class="sxs-lookup"><span data-stu-id="94809-118">If you set up multiple margins, they all add to the total time from the supply *order date* to the demand *requirement date*.</span></span> <span data-ttu-id="94809-119">Örneğin, bir kurulum sağlama süresine sahip değildir ve üç marj türünün tümü bir güne ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="94809-119">For example, a setup has no lead time, and all three margin types are set to one day.</span></span> <span data-ttu-id="94809-120">Bu durumda, tedarik emri tarihi ile talep gereksinim tarihi arasında üç gün olacaktır, bu nedenle sipariş tarihi 1 Temmuz ise, gereksinim tarihi 4 Temmuz olur.</span><span class="sxs-lookup"><span data-stu-id="94809-120">In this case, there will be three days between the supply order date and the demand requirement date, so if the order date is July 1, the requirement date would be July 4.</span></span>

### <a name="receipt-margin"></a><span data-ttu-id="94809-121">Giriş marjı</span><span class="sxs-lookup"><span data-stu-id="94809-121">Receipt margin</span></span>

<span data-ttu-id="94809-122">Giriş marjı büyük olasılıkla üç emniyet marjının en çok kullanılanıdır.</span><span class="sxs-lookup"><span data-stu-id="94809-122">The receipt margin is probably the most used of the three safety margins.</span></span> <span data-ttu-id="94809-123">*Teslimat tarihine* ve *gereksinim tarihinden* geriye doğru uygulanır.</span><span class="sxs-lookup"><span data-stu-id="94809-123">It's applied to the *delivery date* and backward from the *requirement date*.</span></span> <span data-ttu-id="94809-124">Başka bir deyişle, ürünler, gerek duyuldukları günden önceki belirtilen sayıda giriş marjı günü kadar önce alınması gerekir.</span><span class="sxs-lookup"><span data-stu-id="94809-124">In other words, the products should be received the specified number of receipt margin days before they are required.</span></span>

<span data-ttu-id="94809-125">Aşağıdaki çizimde giriş marjları vurgulanır.</span><span class="sxs-lookup"><span data-stu-id="94809-125">The following illustration highlights the receipt margin.</span></span>

![Giriş marjı](media/safety-margins-2.png)

<span data-ttu-id="94809-127">Giriş marjı genellikle, ambar kaydı veya sistemdeki genel sağlama süresinin bir parçası olarak hesaba katılmayan başka zaman alan süreçler için zaman sağlamak amacıyla tampon olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="94809-127">The receipt margin is typically used as a buffer to ensure time for warehouse registration or other time-consuming processes that aren't captured as part of the general lead time in the system.</span></span> <span data-ttu-id="94809-128">Satınalmalar için, bir avantajı ise satınalma emrine ait *teslimat tarihinin* uygun şekilde ileriye doğru hareket ettirilebilmesidir.</span><span class="sxs-lookup"><span data-stu-id="94809-128">For purchases, one benefit is that the *delivery date* of the purchase order is moved forward accordingly.</span></span> <span data-ttu-id="94809-129">Bir emniyet marjı kullanmak yerine sağlama süresini artırdığınızda, satıcıdan son dakikada teslim etmesi istenecektir.</span><span class="sxs-lookup"><span data-stu-id="94809-129">If you  increase the lead time instead of using a safety margin, the vendor will still be asked to deliver at the last minute.</span></span>

<span data-ttu-id="94809-130">Giriş marjının, tedarikin *gereksinim tarihini* değiştirmediğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="94809-130">Notice that the receipt margin doesn't change the *requirement date* of the supply.</span></span> <span data-ttu-id="94809-131">Bu nedenle, talep ve tedarik için gereksinim tarihleri karşılaştırıldığı zaman, giriş marjı doğrudan görünmez (örneğin, **Net gereksinimler** sayfasında).</span><span class="sxs-lookup"><span data-stu-id="94809-131">Therefore, the receipt margin isn't directly visible when requirement dates for demand and supply are compared (for example, on the **Net requirements** page).</span></span> <span data-ttu-id="94809-132">Örneğin giriş marjı 4 gün olarak belirlenir ve bir satınalma siparişi satırının ayın 15'inde alınması planlanırsa, master planlama ayarlanan giriş tarihini ayın 19'u olarak hesaplar.</span><span class="sxs-lookup"><span data-stu-id="94809-132">For example, if the receipt margin is set to four days, and a purchase order line is planned for receipt on the fifteenth of the month, master planning calculates the adjusted receipt date as the nineteenth of the month.</span></span>

<span data-ttu-id="94809-133">Eldeki stok tedarik olarak kullanıldığında bir giriş marjının uygulanmadığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="94809-133">Note that a receipt margin isn't applied when on-hand inventory is used as the supply.</span></span> <span data-ttu-id="94809-134">Eldeki tüm stokların, gerçekten ne zaman teslim alındığında bağımsız olarak hemen kullanılabilir olduğu varsayılır.</span><span class="sxs-lookup"><span data-stu-id="94809-134">All on-hand inventory is assumed to be available immediately, regardless of when it was actually received.</span></span>

### <a name="reorder-margin"></a><span data-ttu-id="94809-135">Sipariş yenileme sınırı</span><span class="sxs-lookup"><span data-stu-id="94809-135">Reorder margin</span></span>

> [!NOTE]
> <span data-ttu-id="94809-136">**Çok yakında:** Bu özellik henüz Planlama Optimizasyonu için desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="94809-136">**Coming soon:** This feature isn't yet supported for Planning Optimization.</span></span> <span data-ttu-id="94809-137">Desteklenene kadar, **Madde sağlama süresine eklenen sipariş yenileme sınırı** için girilen tüm değerler *0* (sıfır) olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="94809-137">Until it's supported, all values that are entered for **Reorder margin added to item lead time** will be treated as *0* (zero).</span></span>

<span data-ttu-id="94809-138">Aşağıdaki çizimde sipariş yenileme sınırı vurgulanır.</span><span class="sxs-lookup"><span data-stu-id="94809-138">The following illustration highlights the reorder margin.</span></span>

![Sipariş yenileme sınırı](media/safety-margins-3.png)

<span data-ttu-id="94809-140">Sipariş yenileme sınırı, master planlama sırasında planlanan tüm siparişler için malzeme sağlama zamanının önüne eklenir.</span><span class="sxs-lookup"><span data-stu-id="94809-140">The reorder margin is added before the item lead time for all planned orders during master planning.</span></span> <span data-ttu-id="94809-141">Bu nedenle, bir tedarik emrinin oluşturulması için ek süre sağlar.</span><span class="sxs-lookup"><span data-stu-id="94809-141">Therefore, it ensures additional time for a supply order to be placed.</span></span> <span data-ttu-id="94809-142">Bu marj genellikle, tedarik emirlerinin oluşturulması sırasında gerekli olan onay işlemleri veya diğer iç işlemlere zaman sağlamak amacıyla tampon olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="94809-142">This margin is typically used as a buffer to ensure time for approval processes or other internal processes that are required during the creation of supply orders.</span></span> <span data-ttu-id="94809-143">Yeniden sipariş sınırı tedarik *emri tarihi* ile *başlangıç tarihi* arasına konur.</span><span class="sxs-lookup"><span data-stu-id="94809-143">The reorder margin is put between the supply *order date* and *start date*.</span></span>

### <a name="issue-margin"></a><span data-ttu-id="94809-144">Çıkış marjı</span><span class="sxs-lookup"><span data-stu-id="94809-144">Issue margin</span></span>

> [!NOTE]
> <span data-ttu-id="94809-145">**Çok yakında:** Bu özellik henüz Planlama Optimizasyonu için desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="94809-145">**Coming soon:** This feature isn't yet supported for Planning Optimization.</span></span> <span data-ttu-id="94809-146">Desteklenene kadar, **Gereksinim tarihinden kesilen çıkış marjı** için girilen tüm değerler *0* (sıfır) olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="94809-146">Until it's supported, all values that are entered for **Issue margin deducted from requirement date** will be treated as *0* (zero).</span></span>

<span data-ttu-id="94809-147">Aşağıdaki çizimde çıkış marjı vurgulanır.</span><span class="sxs-lookup"><span data-stu-id="94809-147">The following illustration highlights the issue margin.</span></span>

![Çıkış marjı](media/safety-margins-4.png)

<span data-ttu-id="94809-149">Master planlama sırasında çıkış marjı talep gereksinim tarihinden düşülür.</span><span class="sxs-lookup"><span data-stu-id="94809-149">The issue margin is deducted from the demand requirement date during master planning.</span></span> <span data-ttu-id="94809-150">Gelen talep emirlerine cevap vermek ve sevk etmek için zaman kazanmanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="94809-150">It helps ensure that you have time to react to and ship incoming demand orders.</span></span> <span data-ttu-id="94809-151">Bu marj, genellikle sevkiyat ve ilgili ambar çıkış işlemlerine zaman sağlamak amacıyla tampon olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="94809-151">This margin is typically used as a buffer to ensure time for shipment and related outbound warehouse processes.</span></span>

<span data-ttu-id="94809-152">Bir çıkış marjı uygulandığında, ilgili tedarik ve talep gereksinim tarihlerinin eşleşmediğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="94809-152">Notice that when an issue margin is applied, related supply and demand requirement dates don't match.</span></span> <span data-ttu-id="94809-153">Bunun yerine, çıkış marjı tedarik *gereksinim tarihi* ve talep *gereksinim tarihi* arasına eklendiği için çıkış marjına göre farklılık gösterir.</span><span class="sxs-lookup"><span data-stu-id="94809-153">Instead, they differ by the issue margin, because the issue margin is added between the supply *requirement date* and the demand *requirement date*.</span></span>

## <a name="set-up-safety-margins"></a><span data-ttu-id="94809-154">Emniyet marjlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="94809-154">Set up safety margins</span></span>

### <a name="turn-on-safety-margins-in-feature-management"></a><span data-ttu-id="94809-155">Özellik yönetiminde Emniyet marjlarını açma</span><span class="sxs-lookup"><span data-stu-id="94809-155">Turn on safety margins in Feature management</span></span>

<span data-ttu-id="94809-156">Bu özelliği Planlama Optimizasyonu ile kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="94809-156">Before you can use this feature with Planning Optimization, it must be turned on in your system.</span></span> <span data-ttu-id="94809-157">Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) çalışma alanını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="94809-157">Admins can use the [Feature management](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="94809-158">Burada, özellik aşağıdaki şekilde listelenmiştir:</span><span class="sxs-lookup"><span data-stu-id="94809-158">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="94809-159">**Modül:** _Master planlama_</span><span class="sxs-lookup"><span data-stu-id="94809-159">**Module:** _Master planning_</span></span>
- <span data-ttu-id="94809-160">**Özellik adı:** _Planlama Optimizasyonu_ için Marjlar</span><span class="sxs-lookup"><span data-stu-id="94809-160">**Feature name:** _Margins for Planning Optimization_</span></span>

### <a name="define-safety-margins"></a><span data-ttu-id="94809-161">Emniyet marjlarını tanımlama</span><span class="sxs-lookup"><span data-stu-id="94809-161">Define safety margins</span></span>

<span data-ttu-id="94809-162">Emniyet marjlarının esnek bir ayarı vardır.</span><span class="sxs-lookup"><span data-stu-id="94809-162">Safety margins have a flexible setup.</span></span> <span data-ttu-id="94809-163">Bunlar hem *karşılama grubunda*, hem de *master planda* ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="94809-163">They can be set on both the *coverage group* and the *master plan*.</span></span> <span data-ttu-id="94809-164">Marjların birbirlerinin üzerine eklendiğinin bilinmesi önemlidir.</span><span class="sxs-lookup"><span data-stu-id="94809-164">It's important that you understand that the margins are added on top of each other.</span></span> <span data-ttu-id="94809-165">Örneğin, karşılama grubunda iki günlük giriş marjı ve master plandaki üç gün, beş günlük etkin giriş marjı oluşturacaktır.</span><span class="sxs-lookup"><span data-stu-id="94809-165">For example, a receipt margin of two days on the coverage group and three days on the master plan will produce an effective receipt margin of five days.</span></span>

<span data-ttu-id="94809-166">Master planda marj ayarlama yeteneği, belirli bir plan için günlük planlamayı etkilemeden daha uzun bir sağlama süresi veya belirsizlik senaryosunu canlandırmak istediğinizde yararlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="94809-166">The ability to set the margin on the master plan can be useful when you want to simulate longer lead times or uncertainty for a specific plan, but without affecting the daily planning.</span></span>

#### <a name="coverage-group-safety-margins"></a><span data-ttu-id="94809-167">Karşılama grubu emniyet marjları</span><span class="sxs-lookup"><span data-stu-id="94809-167">Coverage group safety margins</span></span>

<span data-ttu-id="94809-168">Bir karşılama grubuna emniyet marjı uygulamak için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="94809-168">To apply a safety margin to a coverage group, follow these steps.</span></span>

1. <span data-ttu-id="94809-169">**Master planlama \> Kurulum \> Karşılama grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="94809-169">Go to **Master planning \> Setup \> Coverage groups**.</span></span>
1. <span data-ttu-id="94809-170">Liste bölmesinde, istediğiniz karşılama grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="94809-170">In the list pane, select the desired coverage group.</span></span>
1. <span data-ttu-id="94809-171">**Diğer** hızlı sekmesinde, **Gün cinsinden emniyet marjları** bölümünde, gerekli emniyet marjlarını (gün cinsinden) ayarlamak için aşağıdaki alanları kullanın:</span><span class="sxs-lookup"><span data-stu-id="94809-171">On the **Other** FastTab, in the **Safety margins in days** section, use the following fields to set the required safety margins (in days):</span></span>

    - <span data-ttu-id="94809-172">Gereksinim tarihine eklenen giriş marjı</span><span class="sxs-lookup"><span data-stu-id="94809-172">Receipt margin added to requirement date</span></span>
    - <span data-ttu-id="94809-173">Gereksinim tarihinden kesilen çıkış marjı</span><span class="sxs-lookup"><span data-stu-id="94809-173">Issue margin deducted from requirement date</span></span>
    - <span data-ttu-id="94809-174">Madde sağlama süresine eklenen sipariş yenileme sınırı</span><span class="sxs-lookup"><span data-stu-id="94809-174">Reorder margin added to item lead time</span></span>

#### <a name="master-plan-safety-margins"></a><span data-ttu-id="94809-175">Master plan emniyet marjları</span><span class="sxs-lookup"><span data-stu-id="94809-175">Master plan safety margins</span></span>

<span data-ttu-id="94809-176">Bir master plana emniyet marjı uygulamak için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="94809-176">To apply a safety margin to a master plan, follow these steps.</span></span>

1. <span data-ttu-id="94809-177">**Master planlama \> Kurulum \> Planlar \> Master planlar** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="94809-177">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="94809-178">Liste bölmesinde, istediğiniz master planı seçin.</span><span class="sxs-lookup"><span data-stu-id="94809-178">In the list pane, select the desired master plan.</span></span>
1. <span data-ttu-id="94809-179">**Gün cinsinden emniyet marjları** hızlı sekmesinde, gerekli emniyet marjlarını (gün cinsinden) ayarlamak için aşağıdaki alanları kullanın:</span><span class="sxs-lookup"><span data-stu-id="94809-179">On the **Safety margins in days** FastTab, use the following fields to set the required safety margins (in days):</span></span>

    - <span data-ttu-id="94809-180">Gereksinim tarihine eklenen giriş marjı</span><span class="sxs-lookup"><span data-stu-id="94809-180">Receipt margin added to requirement date</span></span>
    - <span data-ttu-id="94809-181">Gereksinim tarihinden kesilen çıkış marjı</span><span class="sxs-lookup"><span data-stu-id="94809-181">Issue margin deducted from requirement date</span></span>
    - <span data-ttu-id="94809-182">Madde sağlama süresine eklenen sipariş yenileme sınırı</span><span class="sxs-lookup"><span data-stu-id="94809-182">Reorder margin added to item lead time</span></span>

### <a name="define-whether-calculations-are-based-on-calendar-days-or-work-days"></a><span data-ttu-id="94809-183">Hesaplamaların takvim günlerini mi yoksa iş günlerini mi temel alacağını tanımlama</span><span class="sxs-lookup"><span data-stu-id="94809-183">Define whether calculations are based on calendar days or work days</span></span>

<span data-ttu-id="94809-184">Tüm Emniyet marjlarını, takvim günleri veya iş günleri temel alınarak hesaplanacak şekilde ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="94809-184">You can set all safety margins so that they are calculated based on either calendar days or work days.</span></span>

1. <span data-ttu-id="94809-185">**Master planlama \> Kurulum \> Master planlama parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="94809-185">Go to **Master planning \> Setup \> Master planning parameters**.</span></span>
1. <span data-ttu-id="94809-186">**Genel** sekmesinde, **Gün cinsinden emniyet marjları** bölümünde, çalışma günlerini temel alarak marjları hesaplamak için **Çalışma günleri** seçeneğini *Evet* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="94809-186">On the **General** tab, in the **Safety margins in days** section, set the **Working days** option to *Yes* to calculate margins based on working days.</span></span> <span data-ttu-id="94809-187">Takvim günlerini temel alarak marjları hesaplamak için bu seçeneği *Hayır* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="94809-187">Set the option to *No* to calculate margins based on calendar days.</span></span>

<span data-ttu-id="94809-188">Örneğin, bir takvim Pazartesi'den Cuma gününe kadar açık ve Cumartesi'den Pazar'a kapalıdır.</span><span class="sxs-lookup"><span data-stu-id="94809-188">For example, a calendar is open from Monday through Friday and closed from Saturday through Sunday.</span></span> <span data-ttu-id="94809-189">Bir günlük giriş marjı varsa, Pazartesi günündeki gereksinim tarihi önceki Cuma günü teslim tarihi oluşturur, çünkü Cumartesi ve Pazar günleri çalışma günleri değildir.</span><span class="sxs-lookup"><span data-stu-id="94809-189">If there is a receipt margin of one day, a requirement date on a Monday produces a delivery date on the previous Friday, because Saturday and Sunday aren't working days.</span></span>

<span data-ttu-id="94809-190">Çalışma günlerini belirlemek için kullanılan takvim, kuruluma ve tedarik türüne bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="94809-190">The calendar that is used to determine the working days depends on the setup and the supply type.</span></span> <span data-ttu-id="94809-191">Karşılama grubu, ambar ve satıcı takvimleri tarafından denetlenebilir.</span><span class="sxs-lookup"><span data-stu-id="94809-191">It can be controlled by the calendars of the coverage group, the warehouse, and the vendor.</span></span>

> [!NOTE]
> <span data-ttu-id="94809-192">*Ambar* kapsam boyutunun bir parçası değilse (başka bir deyişle, planlama yalnızca *tesis*'i temel alır), ambar takvimi kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="94809-192">If *warehouse* isn't part of the coverage dimension (in other words, planning is based only on *site*), the warehouse calendar isn't used.</span></span>

<span data-ttu-id="94809-193">Sistem, bir veya daha fazla takvim tanımlandığı bir kurulumu kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="94809-193">The system can handle a setup where one or more calendars are defined.</span></span> <span data-ttu-id="94809-194">Aşağıdaki alt kısımlar sonucu kontrol etmek için kullanılabilen olası birleşimleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="94809-194">The following subsections describe the possible combinations that can be used to control the result.</span></span>

#### <a name="calendar-that-is-used-for-the-duration"></a><span data-ttu-id="94809-195">Süre için kullanılan takvim</span><span class="sxs-lookup"><span data-stu-id="94809-195">Calendar that is used for the duration</span></span>

<span data-ttu-id="94809-196">Tanımlanan takvimler, tedarik emri tarihinden talep gereksinim tarihine kadar olan gerçek toplam sağlama süresini takvim günlerinde kontrol eder.</span><span class="sxs-lookup"><span data-stu-id="94809-196">The defined calendars control the actual total lead time in calendar days, from the supply order date to the demand requirement date.</span></span> <span data-ttu-id="94809-197">Aşağıdaki takvim öncelik belirlemesi kullanılır:</span><span class="sxs-lookup"><span data-stu-id="94809-197">The following calendar prioritization is used:</span></span>

- <span data-ttu-id="94809-198">**Satınalma sağlama süresi**: Yalnızca karşılama grubu takvimi dikkate alınır.</span><span class="sxs-lookup"><span data-stu-id="94809-198">**Purchase lead time** – Only the coverage group calendar is considered.</span></span>
- <span data-ttu-id="94809-199">**Giriş marjı**: Tanımlanmışsa, karşılama grubu takvimi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="94809-199">**Receipt margin** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="94809-200">Aksi halde, ambar takvimi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="94809-200">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="94809-201">**Çıkış marjı**: Tanımlanmışsa, karşılama grubu takvimi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="94809-201">**Issue margin** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="94809-202">Aksi halde, ambar takvimi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="94809-202">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="94809-203">**Sipariş sınırı**: Yalnızca karşılama grubu takvimi dikkate alınır.</span><span class="sxs-lookup"><span data-stu-id="94809-203">**Order margin** – Only the coverage group calendar is considered.</span></span>

#### <a name="calendar-that-is-used-for-the-final-date"></a><span data-ttu-id="94809-204">Son tarih için kullanılan takvim</span><span class="sxs-lookup"><span data-stu-id="94809-204">Calendar that is used for the final date</span></span>

<span data-ttu-id="94809-205">Planlama altyapısının belirli bir tarih türü için belirli bir tarihi kullanıp kullanamayacağını belirlemek için aşağıdaki kurallar uygulanır:</span><span class="sxs-lookup"><span data-stu-id="94809-205">The following rules are applied to determine whether the planning engine can use a given date for a given date type:</span></span>

- <span data-ttu-id="94809-206">**Satınalma giriş tarihi**: Tanımlanmışsa, satıcı takvimi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="94809-206">**Purchase receipt date** – The vendor calendar is used, if it's defined.</span></span> <span data-ttu-id="94809-207">Aksi takdirde tanımlanmışsa, karşılama grubu takvimi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="94809-207">Otherwise, the coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="94809-208">Bu takvimlerden hiçbiri tanımlanmadıysa, ambar takvimi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="94809-208">If neither of those calendars is defined, the warehouse calendar is used.</span></span>
- <span data-ttu-id="94809-209">**Transfer giriş tarihi**: Tanımlanmışsa, karşılama grubu takvimi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="94809-209">**Transfer receipt date** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="94809-210">Aksi halde, ambar takvimi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="94809-210">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="94809-211">**Üretim giriş tarihi**: Tanımlanmışsa, karşılama grubu takvimi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="94809-211">**Production receipt date** – The coverage group calendar is used, if it's defined.</span></span> <span data-ttu-id="94809-212">Aksi halde, ambar takvimi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="94809-212">Otherwise, the warehouse calendar is used.</span></span>
- <span data-ttu-id="94809-213">**Talep çıkış açık günü**: Tanımlanmışsa, karşılama grubu takvimi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="94809-213">**Demand issue open day** – The warehouse calendar is used, if it's defined.</span></span> <span data-ttu-id="94809-214">Aksi takdirde karşılama grubu takvimi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="94809-214">Otherwise, the coverage group calendar is used.</span></span>
- <span data-ttu-id="94809-215">**Sipariş açık günü**: Karşılama grubu takviminin ve satıcı takviminin bir birleşimi (kesişim) kullanılır.</span><span class="sxs-lookup"><span data-stu-id="94809-215">**Order open day** – A combination (intersection) of the coverage group calendar and the vendor calendar is used.</span></span> <span data-ttu-id="94809-216">Tarihi kullanmak için iki takvim de açık olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="94809-216">Both calendars must be open to use the date.</span></span> <span data-ttu-id="94809-217">Bu takvimlerden yalnızca biri tanımlandıysa, söz konusu takvimi tek başına kullanılır.</span><span class="sxs-lookup"><span data-stu-id="94809-217">If only one of the calendars is defined, that calendar is used alone.</span></span>

#### <a name="calendar-setup-overview-matrix"></a><span data-ttu-id="94809-218">Takvim kurulumu genel görünüm matrisi</span><span class="sxs-lookup"><span data-stu-id="94809-218">Calendar setup overview matrix</span></span>

<span data-ttu-id="94809-219">Aşağıdaki şekilde, emniyet marjları hesaplanırken hangi takvimlerin uygulanacağını özetleyen bir matris gösterilir.</span><span class="sxs-lookup"><span data-stu-id="94809-219">The following illustration presents a matrix that summarizes which calendars apply when safety margins are calculated.</span></span> <span data-ttu-id="94809-220">Aşağıdaki kısaltmalar ve renkler, her bir takvim türünün belirtildiği yeri belirtmek için kullanılır:</span><span class="sxs-lookup"><span data-stu-id="94809-220">The following abbreviations and colors are used to indicate where each type of calendar is specified:</span></span>

- <span data-ttu-id="94809-221">**Karşılama grubu (CG):** yeşil</span><span class="sxs-lookup"><span data-stu-id="94809-221">**Coverage group (CG):** Green</span></span>
- <span data-ttu-id="94809-222">**Ambar (WH):** sarı</span><span class="sxs-lookup"><span data-stu-id="94809-222">**Warehouse (WH):** Yellow</span></span>
- <span data-ttu-id="94809-223">**(V) satıcı:** mavi</span><span class="sxs-lookup"><span data-stu-id="94809-223">**Vendor (V):** Blue</span></span>

![Takvim kurulumu genel görünüm matrisi](media/safety-margins-calendar-matrix.png)

## <a name="calculating-delays"></a><span data-ttu-id="94809-225">Gecikmeleri hesaplama</span><span class="sxs-lookup"><span data-stu-id="94809-225">Calculating delays</span></span>

<span data-ttu-id="94809-226">Sistem bir siparişin geciktirilip gecikmediğini belirlediğinde, üç güvenlik marjı türünün tümü de eklenir.</span><span class="sxs-lookup"><span data-stu-id="94809-226">All three types of safety margins are included when the system determines whether an order is delayed.</span></span>

<span data-ttu-id="94809-227">Örneğin, bir maddenin bir günlük sağlama süresi ve üç günlük giriş marjı vardır.</span><span class="sxs-lookup"><span data-stu-id="94809-227">For example, an item has lead time of one day and a receipt margin of three days.</span></span> <span data-ttu-id="94809-228">Bu madde için bir satış siparişi bugün gerekli olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="94809-228">A sales order for this item is set as required today.</span></span> <span data-ttu-id="94809-229">Bu durumda, gecikme, *sağlama süresi* + *girişi marjı* = dört gün olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="94809-229">In this case, the delay is calculated as *lead time* + *receipt margin* = four days.</span></span> <span data-ttu-id="94809-230">Bu nedenle, bugün 14 Ağustos ise, dört günlük gecikme 18 Ağustos'ta bir teslimat oluşturur.</span><span class="sxs-lookup"><span data-stu-id="94809-230">Therefore, if today is August 14, the four days of delay produces a delivery on August 18.</span></span> <span data-ttu-id="94809-231">Aşağıdaki şekilde bu örnek gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="94809-231">The following illustration shows this example.</span></span>

![Gecikme hesaplama örneği](media/safety-margins-delays.png)

## <a name="additional-resources"></a><span data-ttu-id="94809-233">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="94809-233">Additional resources</span></span>

[<span data-ttu-id="94809-234">Planlamayı En İyi Duruma Getirmeyi kullanmaya başlama</span><span class="sxs-lookup"><span data-stu-id="94809-234">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="94809-235">Planlamayı En İyi Duruma Getirme uygunluk analizi</span><span class="sxs-lookup"><span data-stu-id="94809-235">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)