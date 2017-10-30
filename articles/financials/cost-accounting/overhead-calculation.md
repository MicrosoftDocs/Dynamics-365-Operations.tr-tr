---
title: "Genel gider hesaplaması"
description: "Bu konu, genel gider maliyetlerinin hesaplanması için tipik işlemleri açıklar."
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: e57db8f4b692aa9c27916625897e268f63031782
ms.openlocfilehash: 285799d70a945c2dae1e3c65296282d5c432a243
ms.contentlocale: tr-tr
ms.lasthandoff: 10/30/2017

---

# <a name="overhead-calculation"></a><span data-ttu-id="3f6e5-103">Genel gider hesaplaması</span><span class="sxs-lookup"><span data-stu-id="3f6e5-103">Overhead calculation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3f6e5-104">Bu konu, genel gider maliyetlerinin hesaplanması için tipik işlemleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="3f6e5-105">Terim tanımı</span><span class="sxs-lookup"><span data-stu-id="3f6e5-105">Term definition</span></span>
---------------

<span data-ttu-id="3f6e5-106">Genel gider maliyetleri bir işletmenin çalışması için normalde uygulanan, ancak doğrudan herhangi bir özel iş, faaliyet, ürün veya hizmete ilişkilendirilmemiş olan maliyetlerdir.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="3f6e5-107">Genel gider maliyetleri kar sağlama faaliyetlerinin oluşturulması için kritik destek sağlar.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="3f6e5-108">Aşağıda bazı genel gider örnekleri verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="3f6e5-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="3f6e5-109">Kira</span><span class="sxs-lookup"><span data-stu-id="3f6e5-109">Rent</span></span>
-   <span data-ttu-id="3f6e5-110">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-110">Electricity</span></span>
-   <span data-ttu-id="3f6e5-111">Yönetim maaşları</span><span class="sxs-lookup"><span data-stu-id="3f6e5-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="3f6e5-112">Genel gider hesaplaması genel bakış</span><span class="sxs-lookup"><span data-stu-id="3f6e5-112">Overhead calculation overview</span></span>
<span data-ttu-id="3f6e5-113">Genel gider hesaplama, maliyet muhasebesi ilkelerini doğru sırayla çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="3f6e5-114">Maliyet muhasebesi ilkeleri değiştiyse veya belirli hatalar algılandıysa, genel gider hesaplamasını aynı mali dönem için birden fazla kez yürütebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="3f6e5-115">Her genel gider hesaplaması depolanır ve önceki sürümlerdeki hesaplamaları kıyaslamanıza olanak sağlayan, benzersiz bir sürüm kimliğine sahip olur.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="3f6e5-116">Genel gider hesaplamasının oluşturduğu maliyet girişleri bir muhasebe tarihi alır.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="3f6e5-117">Bu muhasebe tarihi, hesaplamada kullanılan mali dönemin bitiş tarihiyle eşleşir.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="3f6e5-118">Benzersiz sürüm kimliği aşağıdaki öğelerden oluşur:</span><span class="sxs-lookup"><span data-stu-id="3f6e5-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="3f6e5-119">Sürüm türü</span><span class="sxs-lookup"><span data-stu-id="3f6e5-119">Version type</span></span>
-   <span data-ttu-id="3f6e5-120">Tarih ve saat</span><span class="sxs-lookup"><span data-stu-id="3f6e5-120">Date and time</span></span>
-   <span data-ttu-id="3f6e5-121">Maliyet muhasebesi defteri</span><span class="sxs-lookup"><span data-stu-id="3f6e5-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="3f6e5-122">Mali yıl</span><span class="sxs-lookup"><span data-stu-id="3f6e5-122">Fiscal year</span></span>
-   <span data-ttu-id="3f6e5-123">Mali dönem</span><span class="sxs-lookup"><span data-stu-id="3f6e5-123">Fiscal period</span></span>

<span data-ttu-id="3f6e5-124">Genel gider hesaplama, sürümden bağımsız olarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="3f6e5-125">Bu nedenle, Gerçek sürümden önce Bütçe sürümünü hesaplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="3f6e5-126">Genel gider hesaplama dört adımdan oluşur, aşağıdaki çizimde gösterildiği gibi.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="3f6e5-127">Her adımda, günlük girişleri olan bir günlük başlığı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="3f6e5-128">Bu günlük başlığı, her hesaplama adımı için giriş verilerini tutar.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="3f6e5-129">İlkeler ve kurallar her günlük satırına uygulanır ve maliyet girişleri çıkış olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="3f6e5-130">Bu nedenle, her zaman tam izlenebilirliğe sahip olursunuz.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="3f6e5-131">[![Genel gider hesaplaması](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="3f6e5-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="3f6e5-132">Elektrik genel gideri maliyetini hesapla ve tahsis et</span><span class="sxs-lookup"><span data-stu-id="3f6e5-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="3f6e5-133">Mali muhasebede, elektrik gibi bazı maliyetler peşin ödeme olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="3f6e5-134">Bu nedenle, Maliyet muhasebesi için ayrıntılı yönetim bilgiler sağlanmaz.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="3f6e5-135">Maliyet muhasebesinde doğru yönetimsel bilgileri tüm yönetim birim ve düzeylerinde sağlamak için, maliyetlerin kuruluş birimleri arasında akması gerekir.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="3f6e5-136">Bu akış, tüketimin doğru bir kaydına ya da adil bir değerlendirmeye dayanıyor olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="3f6e5-137">Genel muhasebede, bir elektrik maliyeti aşağıdaki tabloda gösterildiği gibi deftere nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3f6e5-138">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="3f6e5-139">Maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="3f6e5-140">Ana hesap</span><span class="sxs-lookup"><span data-stu-id="3f6e5-140">Main account</span></span></th>
<th><span data-ttu-id="3f6e5-141">Muhasebe para birimi cinsinden tutar</span><span class="sxs-lookup"><span data-stu-id="3f6e5-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3f6e5-142">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="3f6e5-143">CC099</span><span class="sxs-lookup"><span data-stu-id="3f6e5-143">CC099</span></span></td>
<td><span data-ttu-id="3f6e5-144">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-144">Default cost center</span></span></td>
<td><span data-ttu-id="3f6e5-145">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-145">10001</span></span></td>
<td><span data-ttu-id="3f6e5-146">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-146">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="3f6e5-148">Adım 1: Maliyet davranışı hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="3f6e5-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="3f6e5-149">Varsayılan olarak, maliyeti girişleri kaynak veriden içeri alındığında, Maliyet muhasebesinde **Sınıflandırılmamış** maliyet davranışı sınıflandırmasını alırlar.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="3f6e5-150">Maliyet davranışı ilke kuralları ekleyerek, maliyet girişlerini **Sabit maliyet** veya **Değişken maliyet** olarak yeniden sınıflandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="3f6e5-151">Maliyet davranış kuralını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="3f6e5-151">Define the cost behavior rule</span></span>

<span data-ttu-id="3f6e5-152">Bazı durumlarda, sabit bir ücret maliyet parçasıdır ve kalan maliyet, tüketime dayanır.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="3f6e5-153">Elektrik faturaları genellikle bu tanıma uyar.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="3f6e5-154">Belirli bir sabit ücret ödedikten sonra, kilovat saatlik (Kwh) tüketim başına ödeme yaparsınız.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="3f6e5-155">Örneğin, sabit maliyet masrafı 1.000,00 ise, maliyet davranışı kural nasıl tanımlanır:</span><span class="sxs-lookup"><span data-stu-id="3f6e5-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="3f6e5-156">Sabit tutar 1.000,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="3f6e5-157">0 &lt;= 1.000,00 = Sabit</span><span class="sxs-lookup"><span data-stu-id="3f6e5-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="3f6e5-158">1000,01 &lt; N = Değişken</span><span class="sxs-lookup"><span data-stu-id="3f6e5-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="3f6e5-159">Günlük</span><span class="sxs-lookup"><span data-stu-id="3f6e5-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3f6e5-160">Günlük</span><span class="sxs-lookup"><span data-stu-id="3f6e5-160">Journal</span></span></th>
<th><span data-ttu-id="3f6e5-161">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="3f6e5-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="3f6e5-162">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="3f6e5-163">Sürüm</span><span class="sxs-lookup"><span data-stu-id="3f6e5-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3f6e5-164">00001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-164">00001</span></span></td>
<td><span data-ttu-id="3f6e5-165">Maliyet davranışı hesaplama günlüğü</span><span class="sxs-lookup"><span data-stu-id="3f6e5-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="3f6e5-166">Mali</span><span class="sxs-lookup"><span data-stu-id="3f6e5-166">Fiscal</span></span></td>
<td><span data-ttu-id="3f6e5-167">2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-167">2017</span></span></td>
<td><span data-ttu-id="3f6e5-168">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-168">Period 1</span></span></td>
<td><span data-ttu-id="3f6e5-169">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="3f6e5-170">Günlük girişleri (Maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="3f6e5-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3f6e5-171">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="3f6e5-172">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="3f6e5-173">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-173">Cost element</span></span></th>
<th><span data-ttu-id="3f6e5-174">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="3f6e5-174">Cost behavior</span></span></th>
<th><span data-ttu-id="3f6e5-175">Tutar</span><span class="sxs-lookup"><span data-stu-id="3f6e5-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3f6e5-176">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="3f6e5-177">CC099</span><span class="sxs-lookup"><span data-stu-id="3f6e5-177">CC099</span></span></td>
<td><span data-ttu-id="3f6e5-178">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-178">Default cost center</span></span></td>
<td><span data-ttu-id="3f6e5-179">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-179">10001</span></span></td>
<td><span data-ttu-id="3f6e5-180">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-180">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-181">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="3f6e5-181">Unclassified</span></span></td>
<td><span data-ttu-id="3f6e5-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="3f6e5-183">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="3f6e5-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3f6e5-184">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="3f6e5-185">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-185">Cost element</span></span></th>
<th><span data-ttu-id="3f6e5-186">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="3f6e5-186">Cost behavior</span></span></th>
<th><span data-ttu-id="3f6e5-187">Tutar</span><span class="sxs-lookup"><span data-stu-id="3f6e5-187">Amount</span></span></th>
<th><span data-ttu-id="3f6e5-188">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3f6e5-189">CC099</span><span class="sxs-lookup"><span data-stu-id="3f6e5-189">CC099</span></span></td>
<td><span data-ttu-id="3f6e5-190">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-190">Default cost center</span></span></td>
<td><span data-ttu-id="3f6e5-191">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-191">10001</span></span></td>
<td><span data-ttu-id="3f6e5-192">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-192">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-193">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="3f6e5-193">Unclassified</span></span></td>
<td><span data-ttu-id="3f6e5-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-194">10,000.00</span></span></td>
<td><span data-ttu-id="3f6e5-195">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-196">CC099</span><span class="sxs-lookup"><span data-stu-id="3f6e5-196">CC099</span></span></td>
<td><span data-ttu-id="3f6e5-197">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-197">Default cost center</span></span></td>
<td><span data-ttu-id="3f6e5-198">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-198">10001</span></span></td>
<td><span data-ttu-id="3f6e5-199">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-199">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-200">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="3f6e5-200">Unclassified</span></span></td>
<td><span data-ttu-id="3f6e5-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-201">-10,000.00</span></span></td>
<td><span data-ttu-id="3f6e5-202">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-203">CC099</span><span class="sxs-lookup"><span data-stu-id="3f6e5-203">CC099</span></span></td>
<td><span data-ttu-id="3f6e5-204">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-204">Default cost center</span></span></td>
<td><span data-ttu-id="3f6e5-205">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-205">10001</span></span></td>
<td><span data-ttu-id="3f6e5-206">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-206">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-207">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-207">Fixed cost</span></span></td>
<td><span data-ttu-id="3f6e5-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-208">1,000.00</span></span></td>
<td><span data-ttu-id="3f6e5-209">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-210">CC099</span><span class="sxs-lookup"><span data-stu-id="3f6e5-210">CC099</span></span></td>
<td><span data-ttu-id="3f6e5-211">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-211">Default cost center</span></span></td>
<td><span data-ttu-id="3f6e5-212">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-212">10001</span></span></td>
<td><span data-ttu-id="3f6e5-213">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-213">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-214">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-214">Variable cost</span></span></td>
<td><span data-ttu-id="3f6e5-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-215">9,000.00</span></span></td>
<td><span data-ttu-id="3f6e5-216">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3f6e5-217">Maliyet davranışı hakkında ayrıntılı bilgi için bkz. Maliyet davranışı ilkesi.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="3f6e5-218">(Bu konunun henüz tamamlanmadığını ancak yakında tamamlanacağını göz önünde bulundurun.)</span><span class="sxs-lookup"><span data-stu-id="3f6e5-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="3f6e5-219">Adım 2: Maliyet dağıtımı hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="3f6e5-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="3f6e5-220">Maliyet dağıtımı, bir nesneden bir veya daha fazlasına ilgili tahsisat tabanı uygulayarak maliyeti yeniden dağıtmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="3f6e5-221">Maliyet dağıtımı ve maliyet tahsisatı, maliyet dağıtımının her zaman orijinal maliyetin birincil maliyet öğesinde bulunmasıyla farklılık gösterir.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="3f6e5-222">Maliyet dağıtım kuralını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="3f6e5-222">Define the cost distribution rule</span></span>

<span data-ttu-id="3f6e5-223">Mali muhasebede, elektrik maliyetleri çoğu zaman peşin ödeme olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="3f6e5-224">Maliyet muhasebesinde ise bu yöntem yeterince ayrıntılı değildir.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="3f6e5-225">Değişken maliyet, maliyet nesnelerine tek tek, adil bir temele dayanarak dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="3f6e5-226">En mantıklı tahsisat, elektrik kullanımını (Kwh) temel alarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="3f6e5-227">Elektrik adına sahip, istatistiksel bir boyut üyesi oluşturulur ve elektrik tüketimi kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="3f6e5-228">Varsayıla olarak, tüm istatistiksel boyut üyeleri tahsisat tabanları olarak kullanılabilir hale gelir.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3f6e5-229">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-229">Cost object</span></span></th>
<th><span data-ttu-id="3f6e5-230">Kwh</span><span class="sxs-lookup"><span data-stu-id="3f6e5-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3f6e5-231">CC001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-231">CC001</span></span></td>
<td><span data-ttu-id="3f6e5-232">İK</span><span class="sxs-lookup"><span data-stu-id="3f6e5-232">HR</span></span></td>
<td><span data-ttu-id="3f6e5-233">1.000</span><span class="sxs-lookup"><span data-stu-id="3f6e5-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-234">CC002</span><span class="sxs-lookup"><span data-stu-id="3f6e5-234">CC002</span></span></td>
<td><span data-ttu-id="3f6e5-235">Finans</span><span class="sxs-lookup"><span data-stu-id="3f6e5-235">Finance</span></span></td>
<td><span data-ttu-id="3f6e5-236">6,000</span><span class="sxs-lookup"><span data-stu-id="3f6e5-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-237">CC003</span><span class="sxs-lookup"><span data-stu-id="3f6e5-237">CC003</span></span></td>
<td><span data-ttu-id="3f6e5-238">Montaj</span><span class="sxs-lookup"><span data-stu-id="3f6e5-238">Assembly</span></span></td>
<td><span data-ttu-id="3f6e5-239">0</span><span class="sxs-lookup"><span data-stu-id="3f6e5-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3f6e5-240">Aşağıdaki tablo, elektrik tüketiminin değişken maliyetler için bir tahsisat tabanlı olarak uygulandığındaki sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3f6e5-241">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-241">Cost object</span></span></th>
<th><span data-ttu-id="3f6e5-242">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="3f6e5-242">Magnitude</span></span></th>
<th><span data-ttu-id="3f6e5-243">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="3f6e5-243">Allocation factor</span></span></th>
<th><span data-ttu-id="3f6e5-244">Tutar</span><span class="sxs-lookup"><span data-stu-id="3f6e5-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3f6e5-245">CC001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-245">CC001</span></span></td>
<td><span data-ttu-id="3f6e5-246">İK</span><span class="sxs-lookup"><span data-stu-id="3f6e5-246">HR</span></span></td>
<td><span data-ttu-id="3f6e5-247">1.000</span><span class="sxs-lookup"><span data-stu-id="3f6e5-247">1,000</span></span></td>
<td><span data-ttu-id="3f6e5-248">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="3f6e5-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="3f6e5-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-250">CC002</span><span class="sxs-lookup"><span data-stu-id="3f6e5-250">CC002</span></span></td>
<td><span data-ttu-id="3f6e5-251">Finans</span><span class="sxs-lookup"><span data-stu-id="3f6e5-251">Finance</span></span></td>
<td><span data-ttu-id="3f6e5-252">6,000</span><span class="sxs-lookup"><span data-stu-id="3f6e5-252">6,000</span></span></td>
<td><span data-ttu-id="3f6e5-253">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="3f6e5-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="3f6e5-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-255">CC003</span><span class="sxs-lookup"><span data-stu-id="3f6e5-255">CC003</span></span></td>
<td><span data-ttu-id="3f6e5-256">Montaj</span><span class="sxs-lookup"><span data-stu-id="3f6e5-256">Assembly</span></span></td>
<td><span data-ttu-id="3f6e5-257">0</span><span class="sxs-lookup"><span data-stu-id="3f6e5-257">0</span></span></td>
<td><span data-ttu-id="3f6e5-258">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="3f6e5-259">0,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3f6e5-260">Sabit maliyet, elektrik tüketmiş olan tekil maliyet nesnelerine eşit miktarda dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="3f6e5-261">Bu sonuca, Elektrik istatistiksel boyut öğesini bir formül tahsisat tabanında kullanarak ulaşabilirsiniz: (Elektrik &gt; 0,00) Aşağıdaki tablo, elektrik tüketimi değişken maliyetler için bir tahsisat tabanı olarak kullanıldığında ortaya çıkan sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3f6e5-262">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-262">Cost object</span></span></th>
<th><span data-ttu-id="3f6e5-263">Formül</span><span class="sxs-lookup"><span data-stu-id="3f6e5-263">Formula</span></span></th>
<th><span data-ttu-id="3f6e5-264">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="3f6e5-264">Magnitude</span></span></th>
<th><span data-ttu-id="3f6e5-265">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="3f6e5-265">Allocation factor</span></span></th>
<th><span data-ttu-id="3f6e5-266">Tutar</span><span class="sxs-lookup"><span data-stu-id="3f6e5-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3f6e5-267">CC001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-267">CC001</span></span></td>
<td><span data-ttu-id="3f6e5-268">İK</span><span class="sxs-lookup"><span data-stu-id="3f6e5-268">HR</span></span></td>
<td><span data-ttu-id="3f6e5-269">(1,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="3f6e5-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="3f6e5-270">1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-270">1</span></span></td>
<td><span data-ttu-id="3f6e5-271">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="3f6e5-272">500.00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-273">CC002</span><span class="sxs-lookup"><span data-stu-id="3f6e5-273">CC002</span></span></td>
<td><span data-ttu-id="3f6e5-274">Finans</span><span class="sxs-lookup"><span data-stu-id="3f6e5-274">Finance</span></span></td>
<td><span data-ttu-id="3f6e5-275">(6,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="3f6e5-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="3f6e5-276">1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-276">1</span></span></td>
<td><span data-ttu-id="3f6e5-277">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="3f6e5-278">500.00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-279">CC003</span><span class="sxs-lookup"><span data-stu-id="3f6e5-279">CC003</span></span></td>
<td><span data-ttu-id="3f6e5-280">Montaj</span><span class="sxs-lookup"><span data-stu-id="3f6e5-280">Assembly</span></span></td>
<td><span data-ttu-id="3f6e5-281">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="3f6e5-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="3f6e5-282">0</span><span class="sxs-lookup"><span data-stu-id="3f6e5-282">0</span></span></td>
<td><span data-ttu-id="3f6e5-283">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="3f6e5-284">0,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="3f6e5-285">Günlük</span><span class="sxs-lookup"><span data-stu-id="3f6e5-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3f6e5-286">Günlük</span><span class="sxs-lookup"><span data-stu-id="3f6e5-286">Journal</span></span></th>
<th><span data-ttu-id="3f6e5-287">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="3f6e5-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="3f6e5-288">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="3f6e5-289">Sürüm</span><span class="sxs-lookup"><span data-stu-id="3f6e5-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3f6e5-290">00002</span><span class="sxs-lookup"><span data-stu-id="3f6e5-290">00002</span></span></td>
<td><span data-ttu-id="3f6e5-291">Maliyet dağıtımı hesaplama günlüğü</span><span class="sxs-lookup"><span data-stu-id="3f6e5-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="3f6e5-292">Mali</span><span class="sxs-lookup"><span data-stu-id="3f6e5-292">Fiscal</span></span></td>
<td><span data-ttu-id="3f6e5-293">2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-293">2017</span></span></td>
<td><span data-ttu-id="3f6e5-294">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-294">Period 1</span></span></td>
<td><span data-ttu-id="3f6e5-295">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="3f6e5-296">Günlük girişleri (Maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="3f6e5-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3f6e5-297">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="3f6e5-298">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="3f6e5-299">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-299">Cost element</span></span></th>
<th><span data-ttu-id="3f6e5-300">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="3f6e5-300">Cost behavior</span></span></th>
<th><span data-ttu-id="3f6e5-301">Tutar</span><span class="sxs-lookup"><span data-stu-id="3f6e5-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3f6e5-302">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="3f6e5-303">CC099</span><span class="sxs-lookup"><span data-stu-id="3f6e5-303">CC099</span></span></td>
<td><span data-ttu-id="3f6e5-304">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-304">Default cost center</span></span></td>
<td><span data-ttu-id="3f6e5-305">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-305">10001</span></span></td>
<td><span data-ttu-id="3f6e5-306">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-306">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-307">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-307">Fixed cost</span></span></td>
<td><span data-ttu-id="3f6e5-308">1.000,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-309">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="3f6e5-310">CC099</span><span class="sxs-lookup"><span data-stu-id="3f6e5-310">CC099</span></span></td>
<td><span data-ttu-id="3f6e5-311">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-311">Default cost center</span></span></td>
<td><span data-ttu-id="3f6e5-312">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-312">10001</span></span></td>
<td><span data-ttu-id="3f6e5-313">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-313">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-314">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-314">Variable cost</span></span></td>
<td><span data-ttu-id="3f6e5-315">9,000.00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="3f6e5-316">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="3f6e5-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3f6e5-317">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="3f6e5-318">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-318">Cost element</span></span></th>
<th><span data-ttu-id="3f6e5-319">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="3f6e5-319">Cost behavior</span></span></th>
<th><span data-ttu-id="3f6e5-320">Tutar</span><span class="sxs-lookup"><span data-stu-id="3f6e5-320">Amount</span></span></th>
<th><span data-ttu-id="3f6e5-321">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3f6e5-322">CC099</span><span class="sxs-lookup"><span data-stu-id="3f6e5-322">CC099</span></span></td>
<td><span data-ttu-id="3f6e5-323">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-323">Default cost center</span></span></td>
<td><span data-ttu-id="3f6e5-324">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-324">10001</span></span></td>
<td><span data-ttu-id="3f6e5-325">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-325">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-326">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-326">Fixed cost</span></span></td>
<td><span data-ttu-id="3f6e5-327">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-327">-1,000.00</span></span></td>
<td><span data-ttu-id="3f6e5-328">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-329">CC001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-329">CC001</span></span></td>
<td><span data-ttu-id="3f6e5-330">İK</span><span class="sxs-lookup"><span data-stu-id="3f6e5-330">HR</span></span></td>
<td><span data-ttu-id="3f6e5-331">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-331">10001</span></span></td>
<td><span data-ttu-id="3f6e5-332">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-332">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-333">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-333">Fixed cost</span></span></td>
<td><span data-ttu-id="3f6e5-334">500.00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-334">500.00</span></span></td>
<td><span data-ttu-id="3f6e5-335">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-336">CC002</span><span class="sxs-lookup"><span data-stu-id="3f6e5-336">CC002</span></span></td>
<td><span data-ttu-id="3f6e5-337">Finans</span><span class="sxs-lookup"><span data-stu-id="3f6e5-337">Finance</span></span></td>
<td><span data-ttu-id="3f6e5-338">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-338">10001</span></span></td>
<td><span data-ttu-id="3f6e5-339">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-339">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-340">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-340">Fixed cost</span></span></td>
<td><span data-ttu-id="3f6e5-341">500.00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-341">500.00</span></span></td>
<td><span data-ttu-id="3f6e5-342">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-343">CC099</span><span class="sxs-lookup"><span data-stu-id="3f6e5-343">CC099</span></span></td>
<td><span data-ttu-id="3f6e5-344">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-344">Default cost center</span></span></td>
<td><span data-ttu-id="3f6e5-345">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-345">10001</span></span></td>
<td><span data-ttu-id="3f6e5-346">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-346">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-347">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-347">Variable cost</span></span></td>
<td><span data-ttu-id="3f6e5-348">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-348">-9,000.00</span></span></td>
<td><span data-ttu-id="3f6e5-349">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-350">CC001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-350">CC001</span></span></td>
<td><span data-ttu-id="3f6e5-351">İK</span><span class="sxs-lookup"><span data-stu-id="3f6e5-351">HR</span></span></td>
<td><span data-ttu-id="3f6e5-352">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-352">10001</span></span></td>
<td><span data-ttu-id="3f6e5-353">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-353">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-354">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-354">Variable cost</span></span></td>
<td><span data-ttu-id="3f6e5-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="3f6e5-355">1,285.71</span></span></td>
<td><span data-ttu-id="3f6e5-356">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-357">CC002</span><span class="sxs-lookup"><span data-stu-id="3f6e5-357">CC002</span></span></td>
<td><span data-ttu-id="3f6e5-358">Finans</span><span class="sxs-lookup"><span data-stu-id="3f6e5-358">Finance</span></span></td>
<td><span data-ttu-id="3f6e5-359">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-359">10001</span></span></td>
<td><span data-ttu-id="3f6e5-360">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-360">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-361">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-361">Variable cost</span></span></td>
<td><span data-ttu-id="3f6e5-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="3f6e5-362">7,714.29</span></span></td>
<td><span data-ttu-id="3f6e5-363">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3f6e5-364">Maliyet dağıtımı ve tahsisat tabanları hakkında ayrıntılı bilgi için, bakınız Maliyet dağıtım ilkesi ve Tahsisat tabanları.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="3f6e5-365">(Bu konunun henüz tamamlanmadığını ancak yakında tamamlanacağını göz önünde bulundurun.)</span><span class="sxs-lookup"><span data-stu-id="3f6e5-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="3f6e5-366">Adım 3: Genel gider oranı hesaplama işlemi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="3f6e5-367">Genel gider oranı, bir veya birden fazla belirli maliyet nesnesine masraf yüklemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="3f6e5-368">Masraf, önceden belirlenmiş maliyet oranına ve tahsisat tabanından hesaplanan büyüklüğe dayanır.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="3f6e5-369">Genel gider oranını tanımlama</span><span class="sxs-lookup"><span data-stu-id="3f6e5-369">Define the overhead rate</span></span>

<span data-ttu-id="3f6e5-370">Maliyet nesnesi CC001 HR, bir dizi dahili projeye katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="3f6e5-371">HR projeleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3f6e5-372">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-372">Cost object</span></span></th>
<th><span data-ttu-id="3f6e5-373">Saatler</span><span class="sxs-lookup"><span data-stu-id="3f6e5-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3f6e5-374">Proj 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-374">Proj 1</span></span></td>
<td><span data-ttu-id="3f6e5-375">Proje 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-375">Project 1</span></span></td>
<td><span data-ttu-id="3f6e5-376">3</span><span class="sxs-lookup"><span data-stu-id="3f6e5-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-377">Proj 2</span><span class="sxs-lookup"><span data-stu-id="3f6e5-377">Proj 2</span></span></td>
<td><span data-ttu-id="3f6e5-378">Proje 2</span><span class="sxs-lookup"><span data-stu-id="3f6e5-378">Project 2</span></span></td>
<td><span data-ttu-id="3f6e5-379">1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3f6e5-380">Maliyet projeleri dağıtımı için bir önceden belirlenmiş maliyet oranı tanımlandı.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3f6e5-381">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-381">Cost object</span></span></th>
<th><span data-ttu-id="3f6e5-382">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-382">Cost element</span></span></th>
<th><span data-ttu-id="3f6e5-383">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="3f6e5-383">Cost behavior</span></span></th>
<th><span data-ttu-id="3f6e5-384">Birimler</span><span class="sxs-lookup"><span data-stu-id="3f6e5-384">Units</span></span></th>
<th><span data-ttu-id="3f6e5-385">Ücret</span><span class="sxs-lookup"><span data-stu-id="3f6e5-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3f6e5-386">CC001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-386">CC001</span></span></td>
<td><span data-ttu-id="3f6e5-387">İK</span><span class="sxs-lookup"><span data-stu-id="3f6e5-387">HR</span></span></td>
<td><span data-ttu-id="3f6e5-388">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-388">10001</span></span></td>
<td><span data-ttu-id="3f6e5-389">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-389">Variable cost</span></span></td>
<td><span data-ttu-id="3f6e5-390">1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-390">1</span></span></td>
<td><span data-ttu-id="3f6e5-391">10</span><span class="sxs-lookup"><span data-stu-id="3f6e5-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3f6e5-392">Aşağıdaki tablo, HR projeleri bir tahsisat tabanı olarak uygulandığındaki sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3f6e5-393">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-393">Cost object</span></span></th>
<th><span data-ttu-id="3f6e5-394">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="3f6e5-394">Magnitude</span></span></th>
<th><span data-ttu-id="3f6e5-395">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-395">Cost element</span></span></th>
<th><span data-ttu-id="3f6e5-396">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="3f6e5-396">Allocation factor</span></span></th>
<th><span data-ttu-id="3f6e5-397">Tutar</span><span class="sxs-lookup"><span data-stu-id="3f6e5-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3f6e5-398">Proj 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-398">Proj 1</span></span></td>
<td><span data-ttu-id="3f6e5-399">Proje 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-399">Project 1</span></span></td>
<td><span data-ttu-id="3f6e5-400">3</span><span class="sxs-lookup"><span data-stu-id="3f6e5-400">3</span></span></td>
<td><span data-ttu-id="3f6e5-401">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-401">10001</span></span></td>
<td><span data-ttu-id="3f6e5-402">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="3f6e5-403">30.00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-404">Proj 2</span><span class="sxs-lookup"><span data-stu-id="3f6e5-404">Proj 2</span></span></td>
<td><span data-ttu-id="3f6e5-405">Proje 2</span><span class="sxs-lookup"><span data-stu-id="3f6e5-405">Project 2</span></span></td>
<td><span data-ttu-id="3f6e5-406">1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-406">1</span></span></td>
<td><span data-ttu-id="3f6e5-407">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-407">10001</span></span></td>
<td><span data-ttu-id="3f6e5-408">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="3f6e5-409">10,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="3f6e5-410">Günlük</span><span class="sxs-lookup"><span data-stu-id="3f6e5-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3f6e5-411">Günlük</span><span class="sxs-lookup"><span data-stu-id="3f6e5-411">Journal</span></span></th>
<th><span data-ttu-id="3f6e5-412">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="3f6e5-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="3f6e5-413">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="3f6e5-414">Sürüm</span><span class="sxs-lookup"><span data-stu-id="3f6e5-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3f6e5-415">00003</span><span class="sxs-lookup"><span data-stu-id="3f6e5-415">00003</span></span></td>
<td><span data-ttu-id="3f6e5-416">Genel gider oranı hesaplaması günlüğü</span><span class="sxs-lookup"><span data-stu-id="3f6e5-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="3f6e5-417">Mali</span><span class="sxs-lookup"><span data-stu-id="3f6e5-417">Fiscal</span></span></td>
<td><span data-ttu-id="3f6e5-418">2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-418">2017</span></span></td>
<td><span data-ttu-id="3f6e5-419">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-419">Period 1</span></span></td>
<td><span data-ttu-id="3f6e5-420">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="3f6e5-421">Günlük girişleri (Genel gider oranı hesaplaması için günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="3f6e5-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3f6e5-422">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="3f6e5-423">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-423">Cost object</span></span></th>
<th><span data-ttu-id="3f6e5-424">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="3f6e5-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3f6e5-425">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="3f6e5-426">Proj 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-426">Proj 1</span></span></td>
<td><span data-ttu-id="3f6e5-427">Dahili Proj 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="3f6e5-428">3,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-429">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="3f6e5-430">Proj 2</span><span class="sxs-lookup"><span data-stu-id="3f6e5-430">Proj 2</span></span></td>
<td><span data-ttu-id="3f6e5-431">Dahili Proj 2</span><span class="sxs-lookup"><span data-stu-id="3f6e5-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="3f6e5-432">1.00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="3f6e5-433">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="3f6e5-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3f6e5-434">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="3f6e5-435">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-435">Cost element</span></span></th>
<th><span data-ttu-id="3f6e5-436">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="3f6e5-436">Cost behavior</span></span></th>
<th><span data-ttu-id="3f6e5-437">Tutar</span><span class="sxs-lookup"><span data-stu-id="3f6e5-437">Amount</span></span></th>
<th><span data-ttu-id="3f6e5-438">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3f6e5-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-439">CC0001</span></span></td>
<td><span data-ttu-id="3f6e5-440">İK</span><span class="sxs-lookup"><span data-stu-id="3f6e5-440">HR</span></span></td>
<td><span data-ttu-id="3f6e5-441">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-441">10001</span></span></td>
<td><span data-ttu-id="3f6e5-442">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-442">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-443">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-443">Variable cost</span></span></td>
<td><span data-ttu-id="3f6e5-444">-30,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-444">-30.00</span></span></td>
<td><span data-ttu-id="3f6e5-445">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-446">Proj 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-446">Proj 1</span></span></td>
<td><span data-ttu-id="3f6e5-447">Dahili Proj 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="3f6e5-448">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-448">10001</span></span></td>
<td><span data-ttu-id="3f6e5-449">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-449">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-450">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-450">Variable cost</span></span></td>
<td><span data-ttu-id="3f6e5-451">30.00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-451">30.00</span></span></td>
<td><span data-ttu-id="3f6e5-452">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-453">CC001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-453">CC001</span></span></td>
<td><span data-ttu-id="3f6e5-454">İK</span><span class="sxs-lookup"><span data-stu-id="3f6e5-454">HR</span></span></td>
<td><span data-ttu-id="3f6e5-455">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-455">10001</span></span></td>
<td><span data-ttu-id="3f6e5-456">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-456">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-457">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-457">Variable cost</span></span></td>
<td><span data-ttu-id="3f6e5-458">-10,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-458">-10.00</span></span></td>
<td><span data-ttu-id="3f6e5-459">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-460">Proj 2</span><span class="sxs-lookup"><span data-stu-id="3f6e5-460">Proj 2</span></span></td>
<td><span data-ttu-id="3f6e5-461">Dahili Proj 2</span><span class="sxs-lookup"><span data-stu-id="3f6e5-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="3f6e5-462">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-462">10001</span></span></td>
<td><span data-ttu-id="3f6e5-463">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-463">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-464">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-464">Variable cost</span></span></td>
<td><span data-ttu-id="3f6e5-465">10,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-465">10.00</span></span></td>
<td><span data-ttu-id="3f6e5-466">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3f6e5-467">Genel gider oranı ilkesi hakkında ayrıntılı bilgi için, Genel gider oranları ilkesi ve Tahsisat tabanlarına bakın.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="3f6e5-468">(Bu konunun henüz tamamlanmadığını ancak yakında tamamlanacağını göz önünde bulundurun.)</span><span class="sxs-lookup"><span data-stu-id="3f6e5-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="3f6e5-469">Adım 4: Maliyet tahsisat hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="3f6e5-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="3f6e5-470">Tahsisat, bir tahsisat tabanı kullanarak bir maliyet nesnesinin diğer maliyet nesnelerine bakiyesini tahsis eder.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="3f6e5-471">Finance and Operations karşılıklı tahsisat yöntemin destekler.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="3f6e5-472">Karşılıklı tahsisat yönteminde, yardımcı maliyet nesnelerinin değiştiği karşılıklı hizmetler tümüyle tanınır.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="3f6e5-473">Sistem, tahsisatların doğru gerçekleştireceği sırayı otomatik olarak belirler.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="3f6e5-474">Bir maliyet nesnesinin bakiyesi tek bir tahsisat tabanı tarafından tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="3f6e5-475">Yeni maliyet nesnesi boyutları arasındaki tahsisatlar ve onların üyeleri desteklenir.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="3f6e5-476">Tahsisatın sırası, maliyet kontrol birimi tarafından kontrol edilir.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-476">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="3f6e5-477">[![Karşılıklı yöntemi](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="3f6e5-477">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="3f6e5-478">Maliyet tahsisatını tanımla</span><span class="sxs-lookup"><span data-stu-id="3f6e5-478">Define the cost allocation</span></span>

<span data-ttu-id="3f6e5-479">Bir maliyetin akışını nasıl izleyeceğinize dair basit bir örnek aşağıda verilmiştir,</span><span class="sxs-lookup"><span data-stu-id="3f6e5-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="3f6e5-480">Maliyet nesnesi CC001 HR, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="3f6e5-481">HR hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3f6e5-482">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-482">Cost object</span></span></th>
<th><span data-ttu-id="3f6e5-483">HR hizmetleri</span><span class="sxs-lookup"><span data-stu-id="3f6e5-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3f6e5-484">CC002</span><span class="sxs-lookup"><span data-stu-id="3f6e5-484">CC002</span></span></td>
<td><span data-ttu-id="3f6e5-485">Finans</span><span class="sxs-lookup"><span data-stu-id="3f6e5-485">Finance</span></span></td>
<td><span data-ttu-id="3f6e5-486">35</span><span class="sxs-lookup"><span data-stu-id="3f6e5-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-487">CC003</span><span class="sxs-lookup"><span data-stu-id="3f6e5-487">CC003</span></span></td>
<td><span data-ttu-id="3f6e5-488">Montaj</span><span class="sxs-lookup"><span data-stu-id="3f6e5-488">Assembly</span></span></td>
<td><span data-ttu-id="3f6e5-489">55</span><span class="sxs-lookup"><span data-stu-id="3f6e5-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-490">CC004</span><span class="sxs-lookup"><span data-stu-id="3f6e5-490">CC004</span></span></td>
<td><span data-ttu-id="3f6e5-491">Paketleme</span><span class="sxs-lookup"><span data-stu-id="3f6e5-491">Packaging</span></span></td>
<td><span data-ttu-id="3f6e5-492">10</span><span class="sxs-lookup"><span data-stu-id="3f6e5-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3f6e5-493">Maliyet nesnesi CC002 Finans, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="3f6e5-494">Finans hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3f6e5-495">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-495">Cost object</span></span></th>
<th><span data-ttu-id="3f6e5-496">Finans hizmetleri</span><span class="sxs-lookup"><span data-stu-id="3f6e5-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3f6e5-497">CC003</span><span class="sxs-lookup"><span data-stu-id="3f6e5-497">CC003</span></span></td>
<td><span data-ttu-id="3f6e5-498">Montaj</span><span class="sxs-lookup"><span data-stu-id="3f6e5-498">Assembly</span></span></td>
<td><span data-ttu-id="3f6e5-499">65</span><span class="sxs-lookup"><span data-stu-id="3f6e5-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-500">CC004</span><span class="sxs-lookup"><span data-stu-id="3f6e5-500">CC004</span></span></td>
<td><span data-ttu-id="3f6e5-501">Paketleme</span><span class="sxs-lookup"><span data-stu-id="3f6e5-501">Packaging</span></span></td>
<td><span data-ttu-id="3f6e5-502">35</span><span class="sxs-lookup"><span data-stu-id="3f6e5-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3f6e5-503">Maliyet nesnesi CC003 Derleme, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="3f6e5-504">Derleme hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3f6e5-505">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-505">Cost object</span></span></th>
<th><span data-ttu-id="3f6e5-506">Derleme Hizmetleri (saat)</span><span class="sxs-lookup"><span data-stu-id="3f6e5-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3f6e5-507">Prod 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-507">Prod 1</span></span></td>
<td><span data-ttu-id="3f6e5-508">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-508">Product 1</span></span></td>
<td><span data-ttu-id="3f6e5-509">60</span><span class="sxs-lookup"><span data-stu-id="3f6e5-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-510">Prod 2</span><span class="sxs-lookup"><span data-stu-id="3f6e5-510">Prod 2</span></span></td>
<td><span data-ttu-id="3f6e5-511">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="3f6e5-511">Product 2</span></span></td>
<td><span data-ttu-id="3f6e5-512">20</span><span class="sxs-lookup"><span data-stu-id="3f6e5-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3f6e5-513">Maliyet nesnesi CC004 Ambalajlama, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="3f6e5-514">Ambalajlama hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3f6e5-515">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-515">Cost object</span></span></th>
<th><span data-ttu-id="3f6e5-516">Ambalajlama hizmetleri (saat)</span><span class="sxs-lookup"><span data-stu-id="3f6e5-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3f6e5-517">Prod 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-517">Prod 1</span></span></td>
<td><span data-ttu-id="3f6e5-518">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-518">Product 1</span></span></td>
<td><span data-ttu-id="3f6e5-519">80</span><span class="sxs-lookup"><span data-stu-id="3f6e5-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-520">Prod 2</span><span class="sxs-lookup"><span data-stu-id="3f6e5-520">Prod 2</span></span></td>
<td><span data-ttu-id="3f6e5-521">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="3f6e5-521">Product 2</span></span></td>
<td><span data-ttu-id="3f6e5-522">15</span><span class="sxs-lookup"><span data-stu-id="3f6e5-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3f6e5-523">**Not:** Finance and Operations'ta, bir ürünün tükettiği üretim saatleri gibi istatistiki ölçümler doğrudan kaynak verisinden alınabilir.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="3f6e5-524">İstatistiki ölçüm sağlayıcılar hakkında daha ayrıntılı bilgi için İstatistiki ölçü sağlayıcı şablonuna göz atın.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="3f6e5-525">(Bu konun henüz tamamlanmamış olduğunu ancak yakında tamamlanacağını unutmayın) Aşağıdaki tablo, HR hizmetleri toplam maliyet (sabit ve değişken maliyet) için bir tahsisat tabanı olarak uygulandığında oluşacak sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3f6e5-526">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-526">Cost object</span></span></th>
<th><span data-ttu-id="3f6e5-527">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="3f6e5-527">Magnitude</span></span></th>
<th><span data-ttu-id="3f6e5-528">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="3f6e5-528">Allocation factor</span></span></th>
<th><span data-ttu-id="3f6e5-529">Tutar</span><span class="sxs-lookup"><span data-stu-id="3f6e5-529">Amount</span></span></th>
<th><span data-ttu-id="3f6e5-530">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="3f6e5-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3f6e5-531">CC002</span><span class="sxs-lookup"><span data-stu-id="3f6e5-531">CC002</span></span></td>
<td><span data-ttu-id="3f6e5-532">Finans</span><span class="sxs-lookup"><span data-stu-id="3f6e5-532">Finance</span></span></td>
<td><span data-ttu-id="3f6e5-533">35</span><span class="sxs-lookup"><span data-stu-id="3f6e5-533">35</span></span></td>
<td><span data-ttu-id="3f6e5-534">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="3f6e5-535">175.00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-535">175.00</span></span></td>
<td><span data-ttu-id="3f6e5-536">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-537">CC003</span><span class="sxs-lookup"><span data-stu-id="3f6e5-537">CC003</span></span></td>
<td><span data-ttu-id="3f6e5-538">Montaj</span><span class="sxs-lookup"><span data-stu-id="3f6e5-538">Assembly</span></span></td>
<td><span data-ttu-id="3f6e5-539">55</span><span class="sxs-lookup"><span data-stu-id="3f6e5-539">55</span></span></td>
<td><span data-ttu-id="3f6e5-540">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="3f6e5-541">275.00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-541">275.00</span></span></td>
<td><span data-ttu-id="3f6e5-542">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-543">CC004</span><span class="sxs-lookup"><span data-stu-id="3f6e5-543">CC004</span></span></td>
<td><span data-ttu-id="3f6e5-544">Paketleme</span><span class="sxs-lookup"><span data-stu-id="3f6e5-544">Packaging</span></span></td>
<td><span data-ttu-id="3f6e5-545">10</span><span class="sxs-lookup"><span data-stu-id="3f6e5-545">10</span></span></td>
<td><span data-ttu-id="3f6e5-546">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="3f6e5-547">50,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-547">50.00</span></span></td>
<td><span data-ttu-id="3f6e5-548">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-549">CC002</span><span class="sxs-lookup"><span data-stu-id="3f6e5-549">CC002</span></span></td>
<td><span data-ttu-id="3f6e5-550">Finans</span><span class="sxs-lookup"><span data-stu-id="3f6e5-550">Finance</span></span></td>
<td><span data-ttu-id="3f6e5-551">35</span><span class="sxs-lookup"><span data-stu-id="3f6e5-551">35</span></span></td>
<td><span data-ttu-id="3f6e5-552">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="3f6e5-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="3f6e5-553">436.00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-553">436.00</span></span></td>
<td><span data-ttu-id="3f6e5-554">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-555">CC003</span><span class="sxs-lookup"><span data-stu-id="3f6e5-555">CC003</span></span></td>
<td><span data-ttu-id="3f6e5-556">Montaj</span><span class="sxs-lookup"><span data-stu-id="3f6e5-556">Assembly</span></span></td>
<td><span data-ttu-id="3f6e5-557">55</span><span class="sxs-lookup"><span data-stu-id="3f6e5-557">55</span></span></td>
<td><span data-ttu-id="3f6e5-558">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="3f6e5-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="3f6e5-559">685.14</span><span class="sxs-lookup"><span data-stu-id="3f6e5-559">685.14</span></span></td>
<td><span data-ttu-id="3f6e5-560">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-561">CC004</span><span class="sxs-lookup"><span data-stu-id="3f6e5-561">CC004</span></span></td>
<td><span data-ttu-id="3f6e5-562">Paketleme</span><span class="sxs-lookup"><span data-stu-id="3f6e5-562">Packaging</span></span></td>
<td><span data-ttu-id="3f6e5-563">10</span><span class="sxs-lookup"><span data-stu-id="3f6e5-563">10</span></span></td>
<td><span data-ttu-id="3f6e5-564">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="3f6e5-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="3f6e5-565">124.57</span><span class="sxs-lookup"><span data-stu-id="3f6e5-565">124.57</span></span></td>
<td><span data-ttu-id="3f6e5-566">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3f6e5-567">Aşağıdaki tablo, Finans hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3f6e5-568">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-568">Cost object</span></span></th>
<th><span data-ttu-id="3f6e5-569">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="3f6e5-569">Magnitude</span></span></th>
<th><span data-ttu-id="3f6e5-570">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="3f6e5-570">Allocation factor</span></span></th>
<th><span data-ttu-id="3f6e5-571">Tutar</span><span class="sxs-lookup"><span data-stu-id="3f6e5-571">Amount</span></span></th>
<th><span data-ttu-id="3f6e5-572">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="3f6e5-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3f6e5-573">CC003</span><span class="sxs-lookup"><span data-stu-id="3f6e5-573">CC003</span></span></td>
<td><span data-ttu-id="3f6e5-574">Montaj</span><span class="sxs-lookup"><span data-stu-id="3f6e5-574">Assembly</span></span></td>
<td><span data-ttu-id="3f6e5-575">65</span><span class="sxs-lookup"><span data-stu-id="3f6e5-575">65</span></span></td>
<td><span data-ttu-id="3f6e5-576">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="3f6e5-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="3f6e5-577">438.75</span><span class="sxs-lookup"><span data-stu-id="3f6e5-577">438.75</span></span></td>
<td><span data-ttu-id="3f6e5-578">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-579">CC004</span><span class="sxs-lookup"><span data-stu-id="3f6e5-579">CC004</span></span></td>
<td><span data-ttu-id="3f6e5-580">Paketleme</span><span class="sxs-lookup"><span data-stu-id="3f6e5-580">Packaging</span></span></td>
<td><span data-ttu-id="3f6e5-581">35</span><span class="sxs-lookup"><span data-stu-id="3f6e5-581">35</span></span></td>
<td><span data-ttu-id="3f6e5-582">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="3f6e5-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="3f6e5-583">236.25</span><span class="sxs-lookup"><span data-stu-id="3f6e5-583">236.25</span></span></td>
<td><span data-ttu-id="3f6e5-584">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-585">CC003</span><span class="sxs-lookup"><span data-stu-id="3f6e5-585">CC003</span></span></td>
<td><span data-ttu-id="3f6e5-586">Montaj</span><span class="sxs-lookup"><span data-stu-id="3f6e5-586">Assembly</span></span></td>
<td><span data-ttu-id="3f6e5-587">65</span><span class="sxs-lookup"><span data-stu-id="3f6e5-587">65</span></span></td>
<td><span data-ttu-id="3f6e5-588">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="3f6e5-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="3f6e5-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="3f6e5-589">5,297.69</span></span></td>
<td><span data-ttu-id="3f6e5-590">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-591">CC004</span><span class="sxs-lookup"><span data-stu-id="3f6e5-591">CC004</span></span></td>
<td><span data-ttu-id="3f6e5-592">Paketleme</span><span class="sxs-lookup"><span data-stu-id="3f6e5-592">Packaging</span></span></td>
<td><span data-ttu-id="3f6e5-593">35</span><span class="sxs-lookup"><span data-stu-id="3f6e5-593">35</span></span></td>
<td><span data-ttu-id="3f6e5-594">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="3f6e5-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="3f6e5-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="3f6e5-595">2,852.60</span></span></td>
<td><span data-ttu-id="3f6e5-596">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3f6e5-597">Aşağıdaki tablo, Derleme hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3f6e5-598">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-598">Cost object</span></span></th>
<th><span data-ttu-id="3f6e5-599">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="3f6e5-599">Magnitude</span></span></th>
<th><span data-ttu-id="3f6e5-600">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="3f6e5-600">Allocation factor</span></span></th>
<th><span data-ttu-id="3f6e5-601">Tutar</span><span class="sxs-lookup"><span data-stu-id="3f6e5-601">Amount</span></span></th>
<th><span data-ttu-id="3f6e5-602">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="3f6e5-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3f6e5-603">Prod 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-603">Prod 1</span></span></td>
<td><span data-ttu-id="3f6e5-604">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-604">Product 1</span></span></td>
<td><span data-ttu-id="3f6e5-605">60</span><span class="sxs-lookup"><span data-stu-id="3f6e5-605">60</span></span></td>
<td><span data-ttu-id="3f6e5-606">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="3f6e5-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="3f6e5-607">535.31</span><span class="sxs-lookup"><span data-stu-id="3f6e5-607">535.31</span></span></td>
<td><span data-ttu-id="3f6e5-608">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-609">Prod 2</span><span class="sxs-lookup"><span data-stu-id="3f6e5-609">Prod 2</span></span></td>
<td><span data-ttu-id="3f6e5-610">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="3f6e5-610">Product 2</span></span></td>
<td><span data-ttu-id="3f6e5-611">20</span><span class="sxs-lookup"><span data-stu-id="3f6e5-611">20</span></span></td>
<td><span data-ttu-id="3f6e5-612">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="3f6e5-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="3f6e5-613">178.44</span><span class="sxs-lookup"><span data-stu-id="3f6e5-613">178.44</span></span></td>
<td><span data-ttu-id="3f6e5-614">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-615">Prod 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-615">Prod 1</span></span></td>
<td><span data-ttu-id="3f6e5-616">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-616">Product 1</span></span></td>
<td><span data-ttu-id="3f6e5-617">60</span><span class="sxs-lookup"><span data-stu-id="3f6e5-617">60</span></span></td>
<td><span data-ttu-id="3f6e5-618">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="3f6e5-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="3f6e5-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="3f6e5-619">4,487.12</span></span></td>
<td><span data-ttu-id="3f6e5-620">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-621">Prod 2</span><span class="sxs-lookup"><span data-stu-id="3f6e5-621">Prod 2</span></span></td>
<td><span data-ttu-id="3f6e5-622">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="3f6e5-622">Product 2</span></span></td>
<td><span data-ttu-id="3f6e5-623">20</span><span class="sxs-lookup"><span data-stu-id="3f6e5-623">20</span></span></td>
<td><span data-ttu-id="3f6e5-624">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="3f6e5-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="3f6e5-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="3f6e5-625">1,495.71</span></span></td>
<td><span data-ttu-id="3f6e5-626">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3f6e5-627">Aşağıdaki tablo, Paketleme hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3f6e5-628">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-628">Cost object</span></span></th>
<th><span data-ttu-id="3f6e5-629">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="3f6e5-629">Magnitude</span></span></th>
<th><span data-ttu-id="3f6e5-630">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="3f6e5-630">Allocation factor</span></span></th>
<th><span data-ttu-id="3f6e5-631">Tutar</span><span class="sxs-lookup"><span data-stu-id="3f6e5-631">Amount</span></span></th>
<th><span data-ttu-id="3f6e5-632">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="3f6e5-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3f6e5-633">Prod 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-633">Prod 1</span></span></td>
<td><span data-ttu-id="3f6e5-634">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-634">Product 1</span></span></td>
<td><span data-ttu-id="3f6e5-635">80</span><span class="sxs-lookup"><span data-stu-id="3f6e5-635">80</span></span></td>
<td><span data-ttu-id="3f6e5-636">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="3f6e5-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="3f6e5-637">241.05</span><span class="sxs-lookup"><span data-stu-id="3f6e5-637">241.05</span></span></td>
<td><span data-ttu-id="3f6e5-638">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-639">Prod 2</span><span class="sxs-lookup"><span data-stu-id="3f6e5-639">Prod 2</span></span></td>
<td><span data-ttu-id="3f6e5-640">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="3f6e5-640">Product 2</span></span></td>
<td><span data-ttu-id="3f6e5-641">15</span><span class="sxs-lookup"><span data-stu-id="3f6e5-641">15</span></span></td>
<td><span data-ttu-id="3f6e5-642">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="3f6e5-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="3f6e5-643">45.20</span><span class="sxs-lookup"><span data-stu-id="3f6e5-643">45.20</span></span></td>
<td><span data-ttu-id="3f6e5-644">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-645">Prod 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-645">Prod 1</span></span></td>
<td><span data-ttu-id="3f6e5-646">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-646">Product 1</span></span></td>
<td><span data-ttu-id="3f6e5-647">80</span><span class="sxs-lookup"><span data-stu-id="3f6e5-647">80</span></span></td>
<td><span data-ttu-id="3f6e5-648">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="3f6e5-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="3f6e5-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="3f6e5-649">2,507.09</span></span></td>
<td><span data-ttu-id="3f6e5-650">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-651">Prod 2</span><span class="sxs-lookup"><span data-stu-id="3f6e5-651">Prod 2</span></span></td>
<td><span data-ttu-id="3f6e5-652">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="3f6e5-652">Product 2</span></span></td>
<td><span data-ttu-id="3f6e5-653">15</span><span class="sxs-lookup"><span data-stu-id="3f6e5-653">15</span></span></td>
<td><span data-ttu-id="3f6e5-654">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="3f6e5-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="3f6e5-655">470.08</span><span class="sxs-lookup"><span data-stu-id="3f6e5-655">470.08</span></span></td>
<td><span data-ttu-id="3f6e5-656">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="3f6e5-657">Günlük girişleri (maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="3f6e5-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3f6e5-658">Günlük</span><span class="sxs-lookup"><span data-stu-id="3f6e5-658">Journal</span></span></th>
<th><span data-ttu-id="3f6e5-659">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="3f6e5-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="3f6e5-660">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="3f6e5-661">Sürüm</span><span class="sxs-lookup"><span data-stu-id="3f6e5-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3f6e5-662">00004</span><span class="sxs-lookup"><span data-stu-id="3f6e5-662">00004</span></span></td>
<td><span data-ttu-id="3f6e5-663">Maliyet tahsisatı günlüğü</span><span class="sxs-lookup"><span data-stu-id="3f6e5-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="3f6e5-664">Mali</span><span class="sxs-lookup"><span data-stu-id="3f6e5-664">Fiscal</span></span></td>
<td><span data-ttu-id="3f6e5-665">2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-665">2017</span></span></td>
<td><span data-ttu-id="3f6e5-666">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-666">Period 1</span></span></td>
<td><span data-ttu-id="3f6e5-667">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="3f6e5-668">Günlük satırları</span><span class="sxs-lookup"><span data-stu-id="3f6e5-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3f6e5-669">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="3f6e5-670">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="3f6e5-671">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-671">Cost element</span></span></th>
<th><span data-ttu-id="3f6e5-672">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="3f6e5-672">Cost behavior</span></span></th>
<th><span data-ttu-id="3f6e5-673">Tutar</span><span class="sxs-lookup"><span data-stu-id="3f6e5-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3f6e5-674">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="3f6e5-675">CC001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-675">CC001</span></span></td>
<td><span data-ttu-id="3f6e5-676">İK</span><span class="sxs-lookup"><span data-stu-id="3f6e5-676">HR</span></span></td>
<td><span data-ttu-id="3f6e5-677">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-677">10001</span></span></td>
<td><span data-ttu-id="3f6e5-678">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-678">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-679">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-679">Fixed cost</span></span></td>
<td><span data-ttu-id="3f6e5-680">500.00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-681">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="3f6e5-682">CC001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-682">CC001</span></span></td>
<td><span data-ttu-id="3f6e5-683">İK</span><span class="sxs-lookup"><span data-stu-id="3f6e5-683">HR</span></span></td>
<td><span data-ttu-id="3f6e5-684">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-684">10001</span></span></td>
<td><span data-ttu-id="3f6e5-685">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-685">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-686">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-686">Variable cost</span></span></td>
<td><span data-ttu-id="3f6e5-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="3f6e5-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-688">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="3f6e5-689">CC002</span><span class="sxs-lookup"><span data-stu-id="3f6e5-689">CC002</span></span></td>
<td><span data-ttu-id="3f6e5-690">Finans</span><span class="sxs-lookup"><span data-stu-id="3f6e5-690">Finance</span></span></td>
<td><span data-ttu-id="3f6e5-691">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-691">10001</span></span></td>
<td><span data-ttu-id="3f6e5-692">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-692">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-693">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-693">Fixed cost</span></span></td>
<td><span data-ttu-id="3f6e5-694">675.00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-695">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="3f6e5-696">CC002</span><span class="sxs-lookup"><span data-stu-id="3f6e5-696">CC002</span></span></td>
<td><span data-ttu-id="3f6e5-697">Finans</span><span class="sxs-lookup"><span data-stu-id="3f6e5-697">Finance</span></span></td>
<td><span data-ttu-id="3f6e5-698">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-698">10001</span></span></td>
<td><span data-ttu-id="3f6e5-699">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-699">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-700">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-700">Variable cost</span></span></td>
<td><span data-ttu-id="3f6e5-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="3f6e5-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-702">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="3f6e5-703">CC003</span><span class="sxs-lookup"><span data-stu-id="3f6e5-703">CC003</span></span></td>
<td><span data-ttu-id="3f6e5-704">Montaj</span><span class="sxs-lookup"><span data-stu-id="3f6e5-704">Assembly</span></span></td>
<td><span data-ttu-id="3f6e5-705">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-705">10001</span></span></td>
<td><span data-ttu-id="3f6e5-706">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-706">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-707">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-707">Fixed cost</span></span></td>
<td><span data-ttu-id="3f6e5-708">713.75</span><span class="sxs-lookup"><span data-stu-id="3f6e5-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-709">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="3f6e5-710">CC003</span><span class="sxs-lookup"><span data-stu-id="3f6e5-710">CC003</span></span></td>
<td><span data-ttu-id="3f6e5-711">Montaj</span><span class="sxs-lookup"><span data-stu-id="3f6e5-711">Assembly</span></span></td>
<td><span data-ttu-id="3f6e5-712">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-712">10001</span></span></td>
<td><span data-ttu-id="3f6e5-713">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-713">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-714">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-714">Variable cost</span></span></td>
<td><span data-ttu-id="3f6e5-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="3f6e5-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-716">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="3f6e5-717">CC003</span><span class="sxs-lookup"><span data-stu-id="3f6e5-717">CC003</span></span></td>
<td><span data-ttu-id="3f6e5-718">Paketleme</span><span class="sxs-lookup"><span data-stu-id="3f6e5-718">Packaging</span></span></td>
<td><span data-ttu-id="3f6e5-719">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-719">10001</span></span></td>
<td><span data-ttu-id="3f6e5-720">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-720">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-721">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-721">Fixed cost</span></span></td>
<td><span data-ttu-id="3f6e5-722">286.25</span><span class="sxs-lookup"><span data-stu-id="3f6e5-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-723">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="3f6e5-724">CC003</span><span class="sxs-lookup"><span data-stu-id="3f6e5-724">CC003</span></span></td>
<td><span data-ttu-id="3f6e5-725">Paketleme</span><span class="sxs-lookup"><span data-stu-id="3f6e5-725">Packaging</span></span></td>
<td><span data-ttu-id="3f6e5-726">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-726">10001</span></span></td>
<td><span data-ttu-id="3f6e5-727">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-727">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-728">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-728">Variable cost</span></span></td>
<td><span data-ttu-id="3f6e5-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="3f6e5-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-730">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="3f6e5-731">Prod 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-731">Prod 1</span></span></td>
<td><span data-ttu-id="3f6e5-732">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-732">Product 1</span></span></td>
<td><span data-ttu-id="3f6e5-733">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-733">10001</span></span></td>
<td><span data-ttu-id="3f6e5-734">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-734">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-735">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-735">Fixed cost</span></span></td>
<td><span data-ttu-id="3f6e5-736">776.36</span><span class="sxs-lookup"><span data-stu-id="3f6e5-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-737">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="3f6e5-738">Prod 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-738">Prod 1</span></span></td>
<td><span data-ttu-id="3f6e5-739">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-739">Product 1</span></span></td>
<td><span data-ttu-id="3f6e5-740">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-740">10001</span></span></td>
<td><span data-ttu-id="3f6e5-741">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-741">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-742">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-742">Variable cost</span></span></td>
<td><span data-ttu-id="3f6e5-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="3f6e5-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-744">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="3f6e5-745">Prod 2</span><span class="sxs-lookup"><span data-stu-id="3f6e5-745">Prod 2</span></span></td>
<td><span data-ttu-id="3f6e5-746">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-746">Product 1</span></span></td>
<td><span data-ttu-id="3f6e5-747">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-747">10001</span></span></td>
<td><span data-ttu-id="3f6e5-748">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-748">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-749">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-749">Fixed cost</span></span></td>
<td><span data-ttu-id="3f6e5-750">223.64</span><span class="sxs-lookup"><span data-stu-id="3f6e5-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-751">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="3f6e5-752">Prod 2</span><span class="sxs-lookup"><span data-stu-id="3f6e5-752">Prod 2</span></span></td>
<td><span data-ttu-id="3f6e5-753">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-753">Product 1</span></span></td>
<td><span data-ttu-id="3f6e5-754">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-754">10001</span></span></td>
<td><span data-ttu-id="3f6e5-755">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-755">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-756">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-756">Variable cost</span></span></td>
<td><span data-ttu-id="3f6e5-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="3f6e5-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="3f6e5-758">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="3f6e5-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="3f6e5-759">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="3f6e5-760">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-760">Cost element</span></span></th>
<th><span data-ttu-id="3f6e5-761">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="3f6e5-761">Cost behavior</span></span></th>
<th><span data-ttu-id="3f6e5-762">Tutar</span><span class="sxs-lookup"><span data-stu-id="3f6e5-762">Amount</span></span></th>
<th><span data-ttu-id="3f6e5-763">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3f6e5-764">CC001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-764">CC001</span></span></td>
<td><span data-ttu-id="3f6e5-765">İK</span><span class="sxs-lookup"><span data-stu-id="3f6e5-765">HR</span></span></td>
<td><span data-ttu-id="3f6e5-766">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-766">10001</span></span></td>
<td><span data-ttu-id="3f6e5-767">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-767">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-768">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-768">Fixed cost</span></span></td>
<td><span data-ttu-id="3f6e5-769">-500.00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-769">-500.00</span></span></td>
<td><span data-ttu-id="3f6e5-770">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-771">CC002</span><span class="sxs-lookup"><span data-stu-id="3f6e5-771">CC002</span></span></td>
<td><span data-ttu-id="3f6e5-772">Finans</span><span class="sxs-lookup"><span data-stu-id="3f6e5-772">Finance</span></span></td>
<td><span data-ttu-id="3f6e5-773">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-773">10001</span></span></td>
<td><span data-ttu-id="3f6e5-774">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-774">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-775">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-775">Fixed cost</span></span></td>
<td><span data-ttu-id="3f6e5-776">175.00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-776">175.00</span></span></td>
<td><span data-ttu-id="3f6e5-777">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-778">CC003</span><span class="sxs-lookup"><span data-stu-id="3f6e5-778">CC003</span></span></td>
<td><span data-ttu-id="3f6e5-779">Montaj</span><span class="sxs-lookup"><span data-stu-id="3f6e5-779">Assembly</span></span></td>
<td><span data-ttu-id="3f6e5-780">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-780">10001</span></span></td>
<td><span data-ttu-id="3f6e5-781">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-781">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-782">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-782">Fixed cost</span></span></td>
<td><span data-ttu-id="3f6e5-783">275.00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-783">275.00</span></span></td>
<td><span data-ttu-id="3f6e5-784">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-785">CC004</span><span class="sxs-lookup"><span data-stu-id="3f6e5-785">CC004</span></span></td>
<td><span data-ttu-id="3f6e5-786">Paketleme</span><span class="sxs-lookup"><span data-stu-id="3f6e5-786">Packaging</span></span></td>
<td><span data-ttu-id="3f6e5-787">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-787">10001</span></span></td>
<td><span data-ttu-id="3f6e5-788">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-788">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-789">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-789">Fixed cost</span></span></td>
<td><span data-ttu-id="3f6e5-790">50,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-790">50,00</span></span></td>
<td><span data-ttu-id="3f6e5-791">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-792">CC001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-792">CC001</span></span></td>
<td><span data-ttu-id="3f6e5-793">İK</span><span class="sxs-lookup"><span data-stu-id="3f6e5-793">HR</span></span></td>
<td><span data-ttu-id="3f6e5-794">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-794">10001</span></span></td>
<td><span data-ttu-id="3f6e5-795">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-795">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-796">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-796">Variable cost</span></span></td>
<td><span data-ttu-id="3f6e5-797">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="3f6e5-797">-1,245.71</span></span></td>
<td><span data-ttu-id="3f6e5-798">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-799">CC002</span><span class="sxs-lookup"><span data-stu-id="3f6e5-799">CC002</span></span></td>
<td><span data-ttu-id="3f6e5-800">Finans</span><span class="sxs-lookup"><span data-stu-id="3f6e5-800">Finance</span></span></td>
<td><span data-ttu-id="3f6e5-801">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-801">10001</span></span></td>
<td><span data-ttu-id="3f6e5-802">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-802">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-803">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-803">Variable cost</span></span></td>
<td><span data-ttu-id="3f6e5-804">436.00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-804">436.00</span></span></td>
<td><span data-ttu-id="3f6e5-805">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-806">CC003</span><span class="sxs-lookup"><span data-stu-id="3f6e5-806">CC003</span></span></td>
<td><span data-ttu-id="3f6e5-807">Montaj</span><span class="sxs-lookup"><span data-stu-id="3f6e5-807">Assembly</span></span></td>
<td><span data-ttu-id="3f6e5-808">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-808">10001</span></span></td>
<td><span data-ttu-id="3f6e5-809">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-809">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-810">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-810">Variable cost</span></span></td>
<td><span data-ttu-id="3f6e5-811">685.14</span><span class="sxs-lookup"><span data-stu-id="3f6e5-811">685.14</span></span></td>
<td><span data-ttu-id="3f6e5-812">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-813">CC004</span><span class="sxs-lookup"><span data-stu-id="3f6e5-813">CC004</span></span></td>
<td><span data-ttu-id="3f6e5-814">Paketleme</span><span class="sxs-lookup"><span data-stu-id="3f6e5-814">Packaging</span></span></td>
<td><span data-ttu-id="3f6e5-815">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-815">10001</span></span></td>
<td><span data-ttu-id="3f6e5-816">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-816">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-817">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-817">Variable cost</span></span></td>
<td><span data-ttu-id="3f6e5-818">124.57</span><span class="sxs-lookup"><span data-stu-id="3f6e5-818">124.57</span></span></td>
<td><span data-ttu-id="3f6e5-819">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-820">CC002</span><span class="sxs-lookup"><span data-stu-id="3f6e5-820">CC002</span></span></td>
<td><span data-ttu-id="3f6e5-821">Finans</span><span class="sxs-lookup"><span data-stu-id="3f6e5-821">Finance</span></span></td>
<td><span data-ttu-id="3f6e5-822">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-822">10001</span></span></td>
<td><span data-ttu-id="3f6e5-823">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-823">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-824">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-824">Fixed cost</span></span></td>
<td><span data-ttu-id="3f6e5-825">-675,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-825">-675.00</span></span></td>
<td><span data-ttu-id="3f6e5-826">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-827">CC003</span><span class="sxs-lookup"><span data-stu-id="3f6e5-827">CC003</span></span></td>
<td><span data-ttu-id="3f6e5-828">Montaj</span><span class="sxs-lookup"><span data-stu-id="3f6e5-828">Assembly</span></span></td>
<td><span data-ttu-id="3f6e5-829">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-829">10001</span></span></td>
<td><span data-ttu-id="3f6e5-830">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-830">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-831">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-831">Fixed cost</span></span></td>
<td><span data-ttu-id="3f6e5-832">438.75</span><span class="sxs-lookup"><span data-stu-id="3f6e5-832">438.75</span></span></td>
<td><span data-ttu-id="3f6e5-833">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-834">CC004</span><span class="sxs-lookup"><span data-stu-id="3f6e5-834">CC004</span></span></td>
<td><span data-ttu-id="3f6e5-835">Paketleme</span><span class="sxs-lookup"><span data-stu-id="3f6e5-835">Packaging</span></span></td>
<td><span data-ttu-id="3f6e5-836">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-836">10001</span></span></td>
<td><span data-ttu-id="3f6e5-837">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-837">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-838">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-838">Fixed cost</span></span></td>
<td><span data-ttu-id="3f6e5-839">236.25</span><span class="sxs-lookup"><span data-stu-id="3f6e5-839">236.25</span></span></td>
<td><span data-ttu-id="3f6e5-840">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-841">CC002</span><span class="sxs-lookup"><span data-stu-id="3f6e5-841">CC002</span></span></td>
<td><span data-ttu-id="3f6e5-842">Finans</span><span class="sxs-lookup"><span data-stu-id="3f6e5-842">Finance</span></span></td>
<td><span data-ttu-id="3f6e5-843">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-843">10001</span></span></td>
<td><span data-ttu-id="3f6e5-844">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-844">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-845">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-845">Variable cost</span></span></td>
<td><span data-ttu-id="3f6e5-846">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="3f6e5-846">-8,150.29</span></span></td>
<td><span data-ttu-id="3f6e5-847">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-848">CC003</span><span class="sxs-lookup"><span data-stu-id="3f6e5-848">CC003</span></span></td>
<td><span data-ttu-id="3f6e5-849">Montaj</span><span class="sxs-lookup"><span data-stu-id="3f6e5-849">Assembly</span></span></td>
<td><span data-ttu-id="3f6e5-850">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-850">10001</span></span></td>
<td><span data-ttu-id="3f6e5-851">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-851">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-852">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-852">Variable cost</span></span></td>
<td><span data-ttu-id="3f6e5-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="3f6e5-853">5,297.69</span></span></td>
<td><span data-ttu-id="3f6e5-854">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-855">CC004</span><span class="sxs-lookup"><span data-stu-id="3f6e5-855">CC004</span></span></td>
<td><span data-ttu-id="3f6e5-856">Paketleme</span><span class="sxs-lookup"><span data-stu-id="3f6e5-856">Packaging</span></span></td>
<td><span data-ttu-id="3f6e5-857">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-857">10001</span></span></td>
<td><span data-ttu-id="3f6e5-858">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-858">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-859">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-859">Variable cost</span></span></td>
<td><span data-ttu-id="3f6e5-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="3f6e5-860">2,852.60</span></span></td>
<td><span data-ttu-id="3f6e5-861">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-862">CC003</span><span class="sxs-lookup"><span data-stu-id="3f6e5-862">CC003</span></span></td>
<td><span data-ttu-id="3f6e5-863">Montaj</span><span class="sxs-lookup"><span data-stu-id="3f6e5-863">Assembly</span></span></td>
<td><span data-ttu-id="3f6e5-864">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-864">10001</span></span></td>
<td><span data-ttu-id="3f6e5-865">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-865">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-866">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-866">Fixed cost</span></span></td>
<td><span data-ttu-id="3f6e5-867">-713.75</span><span class="sxs-lookup"><span data-stu-id="3f6e5-867">-713.75</span></span></td>
<td><span data-ttu-id="3f6e5-868">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-869">Prod 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-869">Prod 1</span></span></td>
<td><span data-ttu-id="3f6e5-870">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-870">Product 1</span></span></td>
<td><span data-ttu-id="3f6e5-871">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-871">10001</span></span></td>
<td><span data-ttu-id="3f6e5-872">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-872">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-873">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-873">Fixed cost</span></span></td>
<td><span data-ttu-id="3f6e5-874">535.31</span><span class="sxs-lookup"><span data-stu-id="3f6e5-874">535.31</span></span></td>
<td><span data-ttu-id="3f6e5-875">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-876">Prod 2</span><span class="sxs-lookup"><span data-stu-id="3f6e5-876">Prod 2</span></span></td>
<td><span data-ttu-id="3f6e5-877">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="3f6e5-877">Product 2</span></span></td>
<td><span data-ttu-id="3f6e5-878">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-878">10001</span></span></td>
<td><span data-ttu-id="3f6e5-879">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-879">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-880">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-880">Fixed cost</span></span></td>
<td><span data-ttu-id="3f6e5-881">178.44</span><span class="sxs-lookup"><span data-stu-id="3f6e5-881">178.44</span></span></td>
<td><span data-ttu-id="3f6e5-882">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-883">CC003</span><span class="sxs-lookup"><span data-stu-id="3f6e5-883">CC003</span></span></td>
<td><span data-ttu-id="3f6e5-884">Montaj</span><span class="sxs-lookup"><span data-stu-id="3f6e5-884">Assembly</span></span></td>
<td><span data-ttu-id="3f6e5-885">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-885">10001</span></span></td>
<td><span data-ttu-id="3f6e5-886">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-886">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-887">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-887">Variable cost</span></span></td>
<td><span data-ttu-id="3f6e5-888">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="3f6e5-888">-5,982.83</span></span></td>
<td><span data-ttu-id="3f6e5-889">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-890">Prod 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-890">Prod 1</span></span></td>
<td><span data-ttu-id="3f6e5-891">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-891">Product 1</span></span></td>
<td><span data-ttu-id="3f6e5-892">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-892">10001</span></span></td>
<td><span data-ttu-id="3f6e5-893">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-893">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-894">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-894">Variable cost</span></span></td>
<td><span data-ttu-id="3f6e5-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="3f6e5-895">4,487.12</span></span></td>
<td><span data-ttu-id="3f6e5-896">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-897">Prod 2</span><span class="sxs-lookup"><span data-stu-id="3f6e5-897">Prod 2</span></span></td>
<td><span data-ttu-id="3f6e5-898">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="3f6e5-898">Product 2</span></span></td>
<td><span data-ttu-id="3f6e5-899">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-899">10001</span></span></td>
<td><span data-ttu-id="3f6e5-900">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-900">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-901">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-901">Variable cost</span></span></td>
<td><span data-ttu-id="3f6e5-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="3f6e5-902">1,495.71</span></span></td>
<td><span data-ttu-id="3f6e5-903">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-904">CC003</span><span class="sxs-lookup"><span data-stu-id="3f6e5-904">CC003</span></span></td>
<td><span data-ttu-id="3f6e5-905">Montaj</span><span class="sxs-lookup"><span data-stu-id="3f6e5-905">Assembly</span></span></td>
<td><span data-ttu-id="3f6e5-906">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-906">10001</span></span></td>
<td><span data-ttu-id="3f6e5-907">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-907">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-908">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-908">Fixed cost</span></span></td>
<td><span data-ttu-id="3f6e5-909">-286,25</span><span class="sxs-lookup"><span data-stu-id="3f6e5-909">-286.25</span></span></td>
<td><span data-ttu-id="3f6e5-910">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-911">Prod 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-911">Prod 1</span></span></td>
<td><span data-ttu-id="3f6e5-912">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-912">Product 1</span></span></td>
<td><span data-ttu-id="3f6e5-913">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-913">10001</span></span></td>
<td><span data-ttu-id="3f6e5-914">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-914">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-915">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-915">Fixed cost</span></span></td>
<td><span data-ttu-id="3f6e5-916">241.05</span><span class="sxs-lookup"><span data-stu-id="3f6e5-916">241.05</span></span></td>
<td><span data-ttu-id="3f6e5-917">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-918">Prod 2</span><span class="sxs-lookup"><span data-stu-id="3f6e5-918">Prod 2</span></span></td>
<td><span data-ttu-id="3f6e5-919">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="3f6e5-919">Product 2</span></span></td>
<td><span data-ttu-id="3f6e5-920">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-920">10001</span></span></td>
<td><span data-ttu-id="3f6e5-921">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-921">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-922">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-922">Fixed cost</span></span></td>
<td><span data-ttu-id="3f6e5-923">45.20</span><span class="sxs-lookup"><span data-stu-id="3f6e5-923">45.20</span></span></td>
<td><span data-ttu-id="3f6e5-924">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-925">CC003</span><span class="sxs-lookup"><span data-stu-id="3f6e5-925">CC003</span></span></td>
<td><span data-ttu-id="3f6e5-926">Montaj</span><span class="sxs-lookup"><span data-stu-id="3f6e5-926">Assembly</span></span></td>
<td><span data-ttu-id="3f6e5-927">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-927">10001</span></span></td>
<td><span data-ttu-id="3f6e5-928">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-928">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-929">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-929">Variable cost</span></span></td>
<td><span data-ttu-id="3f6e5-930">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="3f6e5-930">-2,977.17</span></span></td>
<td><span data-ttu-id="3f6e5-931">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-932">Prod 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-932">Prod 1</span></span></td>
<td><span data-ttu-id="3f6e5-933">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-933">Product 1</span></span></td>
<td><span data-ttu-id="3f6e5-934">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-934">10001</span></span></td>
<td><span data-ttu-id="3f6e5-935">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-935">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-936">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-936">Variable cost</span></span></td>
<td><span data-ttu-id="3f6e5-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="3f6e5-937">2,507.09</span></span></td>
<td><span data-ttu-id="3f6e5-938">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3f6e5-939">Prod 2</span><span class="sxs-lookup"><span data-stu-id="3f6e5-939">Prod 2</span></span></td>
<td><span data-ttu-id="3f6e5-940">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="3f6e5-940">Product 2</span></span></td>
<td><span data-ttu-id="3f6e5-941">10001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-941">10001</span></span></td>
<td><span data-ttu-id="3f6e5-942">Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-942">Electricity</span></span></td>
<td><span data-ttu-id="3f6e5-943">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-943">Variable cost</span></span></td>
<td><span data-ttu-id="3f6e5-944">470.08</span><span class="sxs-lookup"><span data-stu-id="3f6e5-944">470.08</span></span></td>
<td><span data-ttu-id="3f6e5-945">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="3f6e5-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="3f6e5-946">Sonuç</span><span class="sxs-lookup"><span data-stu-id="3f6e5-946">Conclusion</span></span>
<span data-ttu-id="3f6e5-947">Mali muhasebede, Elektrik için 10.000,00 maliyet bir sözde maliyet merkezi kimliğine nakledilmiştir.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="3f6e5-948">Bu nedenle, maliyet muhasebecileri bu maliyetin tahsis edilmesi gerektiğini bilirler.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="3f6e5-949">Maliyet muhasebesinde, maliyetler kuruluş birimleri ve seviyeleri arasında, uygulanan kural ve ilkelere dayalı olarak akar.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="3f6e5-950">Her maliyet, maliyetlerin tahsisatı için en iyi değerlendirmeyi sağlayan bir tahsisat tabanı ile ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="3f6e5-951">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="3f6e5-952">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="3f6e5-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="3f6e5-953">Toplam</span><span class="sxs-lookup"><span data-stu-id="3f6e5-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="3f6e5-954">CC099</span><span class="sxs-lookup"><span data-stu-id="3f6e5-954">CC099</span></span></th>
<th><span data-ttu-id="3f6e5-955">CC001</span><span class="sxs-lookup"><span data-stu-id="3f6e5-955">CC001</span></span></th>
<th><span data-ttu-id="3f6e5-956">CC002</span><span class="sxs-lookup"><span data-stu-id="3f6e5-956">CC002</span></span></th>
<th><span data-ttu-id="3f6e5-957">CC003</span><span class="sxs-lookup"><span data-stu-id="3f6e5-957">CC003</span></span></th>
<th><span data-ttu-id="3f6e5-958">CC004</span><span class="sxs-lookup"><span data-stu-id="3f6e5-958">CC004</span></span></th>
<th><span data-ttu-id="3f6e5-959">Proj 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-959">Proj 1</span></span></th>
<th><span data-ttu-id="3f6e5-960">Proj 2</span><span class="sxs-lookup"><span data-stu-id="3f6e5-960">Proj 2</span></span></th>
<th><span data-ttu-id="3f6e5-961">Prod 1</span><span class="sxs-lookup"><span data-stu-id="3f6e5-961">Prod 1</span></span></th>
<th><span data-ttu-id="3f6e5-962">Prod 2</span><span class="sxs-lookup"><span data-stu-id="3f6e5-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="3f6e5-963">10001 Elektrik</span><span class="sxs-lookup"><span data-stu-id="3f6e5-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3f6e5-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="3f6e5-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="3f6e5-965"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="3f6e5-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="3f6e5-966"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="3f6e5-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="3f6e5-967"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="3f6e5-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="3f6e5-968"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="3f6e5-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="3f6e5-969"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="3f6e5-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="3f6e5-970"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="3f6e5-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="3f6e5-971"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="3f6e5-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="3f6e5-972"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="3f6e5-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="3f6e5-973">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="3f6e5-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3f6e5-974">0,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-974">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="3f6e5-975">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3f6e5-976">0,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3f6e5-977">0,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3f6e5-978">0,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3f6e5-979">0,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3f6e5-980">0,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="3f6e5-981">776.36</span><span class="sxs-lookup"><span data-stu-id="3f6e5-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3f6e5-982">223.64</span><span class="sxs-lookup"><span data-stu-id="3f6e5-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3f6e5-983"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="3f6e5-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="3f6e5-984">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="3f6e5-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3f6e5-985">000</span><span class="sxs-lookup"><span data-stu-id="3f6e5-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3f6e5-986">0,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3f6e5-987">0,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3f6e5-988">0,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3f6e5-989">0,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3f6e5-990">30.00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3f6e5-991">10,00</span><span class="sxs-lookup"><span data-stu-id="3f6e5-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3f6e5-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="3f6e5-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3f6e5-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="3f6e5-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="3f6e5-994"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="3f6e5-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="3f6e5-995">Bu konu, birincil maliyet öğesi, 10001 Elektrik'in maliyet nesneleri arasında nasıl aktığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="3f6e5-996">Bu nedenle, bu genel gider maliyeti kuruluşun en düşük seviyesine tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="3f6e5-997">Başka bir deyişle, maliyet en alt düzeydeki maliyet nesnelerine aittir.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="3f6e5-998">Maliyetin, maliyet nesneleri arasında görsel bir akışına ihtiyacınız varsa, maliyetin akışını görselleştirmek için maliyet toplamı ilke kurallarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="3f6e5-999">Daha ayrıntılı bilgi için, Maliyet toplam ilkesine bakınız.</span><span class="sxs-lookup"><span data-stu-id="3f6e5-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="3f6e5-1000">(Bu konunun henüz tamamlanmadığını ancak yakında tamamlanacağını göz önünde bulundurun.)</span><span class="sxs-lookup"><span data-stu-id="3f6e5-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




