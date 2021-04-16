---
title: Genel gider hesaplaması
description: Bu konu, genel gider maliyetlerinin hesaplanması için tipik işlemleri açıklar.
author: AndersGirke
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation, CAMOverheadRateCalculationJournalEntry, CAMFormulaAllocationBase
audience: Application User
ms.reviewer: roschlom
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 2dddc22128621dc148a253cd568430587f294544
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822915"
---
# <a name="overhead-calculation"></a><span data-ttu-id="4807b-103">Genel gider hesaplaması</span><span class="sxs-lookup"><span data-stu-id="4807b-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4807b-104">Bu konu, genel gider maliyetlerinin hesaplanması için tipik işlemleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="4807b-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="4807b-105">Terim tanımı</span><span class="sxs-lookup"><span data-stu-id="4807b-105">Term definition</span></span>
---------------

<span data-ttu-id="4807b-106">Genel gider maliyetleri bir işletmenin çalışması için normalde uygulanan, ancak doğrudan herhangi bir özel iş, faaliyet, ürün veya hizmete ilişkilendirilmemiş olan maliyetlerdir.</span><span class="sxs-lookup"><span data-stu-id="4807b-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="4807b-107">Genel gider maliyetleri kar sağlama faaliyetlerinin oluşturulması için kritik destek sağlar.</span><span class="sxs-lookup"><span data-stu-id="4807b-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="4807b-108">Aşağıda bazı genel gider örnekleri verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="4807b-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="4807b-109">Kira</span><span class="sxs-lookup"><span data-stu-id="4807b-109">Rent</span></span>
-   <span data-ttu-id="4807b-110">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-110">Electricity</span></span>
-   <span data-ttu-id="4807b-111">Yönetim maaşları</span><span class="sxs-lookup"><span data-stu-id="4807b-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="4807b-112">Genel gider hesaplaması genel bakış</span><span class="sxs-lookup"><span data-stu-id="4807b-112">Overhead calculation overview</span></span>
<span data-ttu-id="4807b-113">Genel gider hesaplama, maliyet muhasebesi ilkelerini doğru sırayla çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="4807b-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="4807b-114">Maliyet muhasebesi ilkeleri değiştiyse veya belirli hatalar algılandıysa, genel gider hesaplamasını aynı mali dönem için birden fazla kez yürütebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4807b-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="4807b-115">Her genel gider hesaplaması depolanır ve önceki sürümlerdeki hesaplamaları kıyaslamanıza olanak sağlayan, benzersiz bir sürüm kimliğine sahip olur.</span><span class="sxs-lookup"><span data-stu-id="4807b-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="4807b-116">Genel gider hesaplamasının oluşturduğu maliyet girişleri bir muhasebe tarihi alır.</span><span class="sxs-lookup"><span data-stu-id="4807b-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="4807b-117">Bu muhasebe tarihi, hesaplamada kullanılan mali dönemin bitiş tarihiyle eşleşir.</span><span class="sxs-lookup"><span data-stu-id="4807b-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="4807b-118">Benzersiz sürüm kimliği aşağıdaki öğelerden oluşur:</span><span class="sxs-lookup"><span data-stu-id="4807b-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="4807b-119">Sürüm türü</span><span class="sxs-lookup"><span data-stu-id="4807b-119">Version type</span></span>
-   <span data-ttu-id="4807b-120">Tarih ve saat</span><span class="sxs-lookup"><span data-stu-id="4807b-120">Date and time</span></span>
-   <span data-ttu-id="4807b-121">Maliyet muhasebesi defteri</span><span class="sxs-lookup"><span data-stu-id="4807b-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="4807b-122">Mali yıl</span><span class="sxs-lookup"><span data-stu-id="4807b-122">Fiscal year</span></span>
-   <span data-ttu-id="4807b-123">Mali dönem</span><span class="sxs-lookup"><span data-stu-id="4807b-123">Fiscal period</span></span>

<span data-ttu-id="4807b-124">Genel gider hesaplama, sürümden bağımsız olarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="4807b-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="4807b-125">Bu nedenle, Gerçek sürümden önce Bütçe sürümünü hesaplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4807b-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="4807b-126">Genel gider hesaplama dört adımdan oluşur, aşağıdaki çizimde gösterildiği gibi.</span><span class="sxs-lookup"><span data-stu-id="4807b-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="4807b-127">Her adımda, günlük girişleri olan bir günlük başlığı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4807b-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="4807b-128">Bu günlük başlığı, her hesaplama adımı için giriş verilerini tutar.</span><span class="sxs-lookup"><span data-stu-id="4807b-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="4807b-129">İlkeler ve kurallar her günlük satırına uygulanır ve maliyet girişleri çıkış olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4807b-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="4807b-130">Bu nedenle, her zaman tam izlenebilirliğe sahip olursunuz.</span><span class="sxs-lookup"><span data-stu-id="4807b-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="4807b-131">[![Genel gider hesaplaması](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="4807b-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="4807b-132">Elektrik genel gideri maliyetini hesapla ve tahsis et</span><span class="sxs-lookup"><span data-stu-id="4807b-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="4807b-133">Mali muhasebede, elektrik gibi bazı maliyetler peşin ödeme olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="4807b-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="4807b-134">Bu nedenle, Maliyet muhasebesi için ayrıntılı yönetim bilgiler sağlanmaz.</span><span class="sxs-lookup"><span data-stu-id="4807b-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="4807b-135">Maliyet muhasebesinde doğru yönetimsel bilgileri tüm yönetim birim ve düzeylerinde sağlamak için, maliyetlerin kuruluş birimleri arasında akması gerekir.</span><span class="sxs-lookup"><span data-stu-id="4807b-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="4807b-136">Bu akış, tüketimin doğru bir kaydına ya da adil bir değerlendirmeye dayanıyor olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4807b-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="4807b-137">Genel muhasebede, bir elektrik maliyeti aşağıdaki tabloda gösterildiği gibi deftere nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="4807b-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4807b-138">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="4807b-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4807b-139">Maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="4807b-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="4807b-140">Ana hesap</span><span class="sxs-lookup"><span data-stu-id="4807b-140">Main account</span></span></th>
<th><span data-ttu-id="4807b-141">Muhasebe para birimi cinsinden tutar</span><span class="sxs-lookup"><span data-stu-id="4807b-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4807b-142">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="4807b-143">CC099</span><span class="sxs-lookup"><span data-stu-id="4807b-143">CC099</span></span></td>
<td><span data-ttu-id="4807b-144">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="4807b-144">Default cost center</span></span></td>
<td><span data-ttu-id="4807b-145">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-145">10001</span></span></td>
<td><span data-ttu-id="4807b-146">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-146">Electricity</span></span></td>
<td><span data-ttu-id="4807b-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="4807b-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="4807b-148">Adım 1: Maliyet davranışı hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="4807b-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="4807b-149">Varsayılan olarak, maliyeti girişleri kaynak veriden içeri alındığında, Maliyet muhasebesinde **Sınıflandırılmamış** maliyet davranışı sınıflandırmasını alırlar.</span><span class="sxs-lookup"><span data-stu-id="4807b-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="4807b-150">Maliyet davranışı ilke kuralları ekleyerek, maliyet girişlerini **Sabit maliyet** veya **Değişken maliyet** olarak yeniden sınıflandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4807b-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="4807b-151">Maliyet davranış kuralını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="4807b-151">Define the cost behavior rule</span></span>

<span data-ttu-id="4807b-152">Bazı durumlarda, sabit bir ücret maliyet parçasıdır ve kalan maliyet, tüketime dayanır.</span><span class="sxs-lookup"><span data-stu-id="4807b-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="4807b-153">Elektrik faturaları genellikle bu tanıma uyar.</span><span class="sxs-lookup"><span data-stu-id="4807b-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="4807b-154">Belirli bir sabit ücret ödedikten sonra, kilovat saatlik (Kwh) tüketim başına ödeme yaparsınız.</span><span class="sxs-lookup"><span data-stu-id="4807b-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="4807b-155">Örneğin, sabit maliyet masrafı 1.000,00 ise, maliyet davranışı kural nasıl tanımlanır:</span><span class="sxs-lookup"><span data-stu-id="4807b-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="4807b-156">Sabit tutar 1.000,00</span><span class="sxs-lookup"><span data-stu-id="4807b-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="4807b-157">0 &lt;= 1.000,00 = Sabit</span><span class="sxs-lookup"><span data-stu-id="4807b-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="4807b-158">1000,01 &lt; N = Değişken</span><span class="sxs-lookup"><span data-stu-id="4807b-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="4807b-159">Günlük</span><span class="sxs-lookup"><span data-stu-id="4807b-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4807b-160">Günlük</span><span class="sxs-lookup"><span data-stu-id="4807b-160">Journal</span></span></th>
<th><span data-ttu-id="4807b-161">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="4807b-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4807b-162">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="4807b-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4807b-163">Sürüm</span><span class="sxs-lookup"><span data-stu-id="4807b-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4807b-164">00001</span><span class="sxs-lookup"><span data-stu-id="4807b-164">00001</span></span></td>
<td><span data-ttu-id="4807b-165">Maliyet davranışı hesaplama günlüğü</span><span class="sxs-lookup"><span data-stu-id="4807b-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="4807b-166">Mali</span><span class="sxs-lookup"><span data-stu-id="4807b-166">Fiscal</span></span></td>
<td><span data-ttu-id="4807b-167">2017</span><span class="sxs-lookup"><span data-stu-id="4807b-167">2017</span></span></td>
<td><span data-ttu-id="4807b-168">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="4807b-168">Period 1</span></span></td>
<td><span data-ttu-id="4807b-169">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="4807b-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="4807b-170">Günlük girişleri (Maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="4807b-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4807b-171">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="4807b-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4807b-172">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4807b-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4807b-173">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="4807b-173">Cost element</span></span></th>
<th><span data-ttu-id="4807b-174">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="4807b-174">Cost behavior</span></span></th>
<th><span data-ttu-id="4807b-175">Tutar</span><span class="sxs-lookup"><span data-stu-id="4807b-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4807b-176">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="4807b-177">CC099</span><span class="sxs-lookup"><span data-stu-id="4807b-177">CC099</span></span></td>
<td><span data-ttu-id="4807b-178">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="4807b-178">Default cost center</span></span></td>
<td><span data-ttu-id="4807b-179">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-179">10001</span></span></td>
<td><span data-ttu-id="4807b-180">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-180">Electricity</span></span></td>
<td><span data-ttu-id="4807b-181">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="4807b-181">Unclassified</span></span></td>
<td><span data-ttu-id="4807b-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="4807b-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4807b-183">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="4807b-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4807b-184">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4807b-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4807b-185">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="4807b-185">Cost element</span></span></th>
<th><span data-ttu-id="4807b-186">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="4807b-186">Cost behavior</span></span></th>
<th><span data-ttu-id="4807b-187">Tutar</span><span class="sxs-lookup"><span data-stu-id="4807b-187">Amount</span></span></th>
<th><span data-ttu-id="4807b-188">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="4807b-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4807b-189">CC099</span><span class="sxs-lookup"><span data-stu-id="4807b-189">CC099</span></span></td>
<td><span data-ttu-id="4807b-190">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="4807b-190">Default cost center</span></span></td>
<td><span data-ttu-id="4807b-191">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-191">10001</span></span></td>
<td><span data-ttu-id="4807b-192">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-192">Electricity</span></span></td>
<td><span data-ttu-id="4807b-193">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="4807b-193">Unclassified</span></span></td>
<td><span data-ttu-id="4807b-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="4807b-194">10,000.00</span></span></td>
<td><span data-ttu-id="4807b-195">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-196">CC099</span><span class="sxs-lookup"><span data-stu-id="4807b-196">CC099</span></span></td>
<td><span data-ttu-id="4807b-197">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="4807b-197">Default cost center</span></span></td>
<td><span data-ttu-id="4807b-198">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-198">10001</span></span></td>
<td><span data-ttu-id="4807b-199">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-199">Electricity</span></span></td>
<td><span data-ttu-id="4807b-200">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="4807b-200">Unclassified</span></span></td>
<td><span data-ttu-id="4807b-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="4807b-201">-10,000.00</span></span></td>
<td><span data-ttu-id="4807b-202">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-203">CC099</span><span class="sxs-lookup"><span data-stu-id="4807b-203">CC099</span></span></td>
<td><span data-ttu-id="4807b-204">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="4807b-204">Default cost center</span></span></td>
<td><span data-ttu-id="4807b-205">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-205">10001</span></span></td>
<td><span data-ttu-id="4807b-206">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-206">Electricity</span></span></td>
<td><span data-ttu-id="4807b-207">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-207">Fixed cost</span></span></td>
<td><span data-ttu-id="4807b-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="4807b-208">1,000.00</span></span></td>
<td><span data-ttu-id="4807b-209">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-210">CC099</span><span class="sxs-lookup"><span data-stu-id="4807b-210">CC099</span></span></td>
<td><span data-ttu-id="4807b-211">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="4807b-211">Default cost center</span></span></td>
<td><span data-ttu-id="4807b-212">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-212">10001</span></span></td>
<td><span data-ttu-id="4807b-213">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-213">Electricity</span></span></td>
<td><span data-ttu-id="4807b-214">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-214">Variable cost</span></span></td>
<td><span data-ttu-id="4807b-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="4807b-215">9,000.00</span></span></td>
<td><span data-ttu-id="4807b-216">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4807b-217">Daha fazla bilgi için bkz. [Maliyet davranışı ilkesi oluşturma ve bir maliyet kontrol birimine atama](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="4807b-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="4807b-218">Adım 2: Maliyet dağıtımı hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="4807b-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="4807b-219">Maliyet dağıtımı, bir nesneden bir veya daha fazlasına ilgili tahsisat tabanı uygulayarak maliyeti yeniden dağıtmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4807b-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="4807b-220">Maliyet dağıtımı ve maliyet tahsisatı, maliyet dağıtımının her zaman orijinal maliyetin birincil maliyet öğesinde bulunmasıyla farklılık gösterir.</span><span class="sxs-lookup"><span data-stu-id="4807b-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="4807b-221">Maliyet dağıtım kuralını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="4807b-221">Define the cost distribution rule</span></span>

<span data-ttu-id="4807b-222">Mali muhasebede, elektrik maliyetleri çoğu zaman peşin ödeme olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="4807b-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="4807b-223">Maliyet muhasebesinde ise bu yöntem yeterince ayrıntılı değildir.</span><span class="sxs-lookup"><span data-stu-id="4807b-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="4807b-224">Değişken maliyet, maliyet nesnelerine tek tek, adil bir temele dayanarak dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4807b-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="4807b-225">En mantıklı tahsisat, elektrik kullanımını (Kwh) temel alarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4807b-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="4807b-226">Elektrik adına sahip, istatistiksel bir boyut üyesi oluşturulur ve elektrik tüketimi kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="4807b-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="4807b-227">Varsayıla olarak, tüm istatistiksel boyut üyeleri tahsisat tabanları olarak kullanılabilir hale gelir.</span><span class="sxs-lookup"><span data-stu-id="4807b-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4807b-228">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4807b-228">Cost object</span></span></th>
<th><span data-ttu-id="4807b-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="4807b-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4807b-230">CC001</span><span class="sxs-lookup"><span data-stu-id="4807b-230">CC001</span></span></td>
<td><span data-ttu-id="4807b-231">İK</span><span class="sxs-lookup"><span data-stu-id="4807b-231">HR</span></span></td>
<td><span data-ttu-id="4807b-232">1.000</span><span class="sxs-lookup"><span data-stu-id="4807b-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-233">CC002</span><span class="sxs-lookup"><span data-stu-id="4807b-233">CC002</span></span></td>
<td><span data-ttu-id="4807b-234">Finans</span><span class="sxs-lookup"><span data-stu-id="4807b-234">Finance</span></span></td>
<td><span data-ttu-id="4807b-235">6,000</span><span class="sxs-lookup"><span data-stu-id="4807b-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-236">CC003</span><span class="sxs-lookup"><span data-stu-id="4807b-236">CC003</span></span></td>
<td><span data-ttu-id="4807b-237">Montaj</span><span class="sxs-lookup"><span data-stu-id="4807b-237">Assembly</span></span></td>
<td><span data-ttu-id="4807b-238">0</span><span class="sxs-lookup"><span data-stu-id="4807b-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4807b-239">Aşağıdaki tablo, elektrik tüketiminin değişken maliyetler için bir tahsisat tabanlı olarak uygulandığındaki sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="4807b-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4807b-240">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4807b-240">Cost object</span></span></th>
<th><span data-ttu-id="4807b-241">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="4807b-241">Magnitude</span></span></th>
<th><span data-ttu-id="4807b-242">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="4807b-242">Allocation factor</span></span></th>
<th><span data-ttu-id="4807b-243">Tutar</span><span class="sxs-lookup"><span data-stu-id="4807b-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4807b-244">CC001</span><span class="sxs-lookup"><span data-stu-id="4807b-244">CC001</span></span></td>
<td><span data-ttu-id="4807b-245">İK</span><span class="sxs-lookup"><span data-stu-id="4807b-245">HR</span></span></td>
<td><span data-ttu-id="4807b-246">1.000</span><span class="sxs-lookup"><span data-stu-id="4807b-246">1,000</span></span></td>
<td><span data-ttu-id="4807b-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="4807b-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="4807b-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="4807b-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-249">CC002</span><span class="sxs-lookup"><span data-stu-id="4807b-249">CC002</span></span></td>
<td><span data-ttu-id="4807b-250">Finans</span><span class="sxs-lookup"><span data-stu-id="4807b-250">Finance</span></span></td>
<td><span data-ttu-id="4807b-251">6,000</span><span class="sxs-lookup"><span data-stu-id="4807b-251">6,000</span></span></td>
<td><span data-ttu-id="4807b-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="4807b-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="4807b-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="4807b-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-254">CC003</span><span class="sxs-lookup"><span data-stu-id="4807b-254">CC003</span></span></td>
<td><span data-ttu-id="4807b-255">Montaj</span><span class="sxs-lookup"><span data-stu-id="4807b-255">Assembly</span></span></td>
<td><span data-ttu-id="4807b-256">0</span><span class="sxs-lookup"><span data-stu-id="4807b-256">0</span></span></td>
<td><span data-ttu-id="4807b-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="4807b-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="4807b-258">0,00</span><span class="sxs-lookup"><span data-stu-id="4807b-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4807b-259">Sabit maliyet, elektrik tüketmiş olan tekil maliyet nesnelerine eşit miktarda dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4807b-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="4807b-260">Bu sonuca, Elektrik istatistiksel boyut öğesini bir formül tahsisat tabanında kullanarak ulaşabilirsiniz: (Elektrik &gt; 0,00) Aşağıdaki tablo, elektrik tüketimi değişken maliyetler için bir tahsisat tabanı olarak kullanıldığında ortaya çıkan sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="4807b-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4807b-261">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4807b-261">Cost object</span></span></th>
<th><span data-ttu-id="4807b-262">Formül</span><span class="sxs-lookup"><span data-stu-id="4807b-262">Formula</span></span></th>
<th><span data-ttu-id="4807b-263">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="4807b-263">Magnitude</span></span></th>
<th><span data-ttu-id="4807b-264">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="4807b-264">Allocation factor</span></span></th>
<th><span data-ttu-id="4807b-265">Tutar</span><span class="sxs-lookup"><span data-stu-id="4807b-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4807b-266">CC001</span><span class="sxs-lookup"><span data-stu-id="4807b-266">CC001</span></span></td>
<td><span data-ttu-id="4807b-267">İK</span><span class="sxs-lookup"><span data-stu-id="4807b-267">HR</span></span></td>
<td><span data-ttu-id="4807b-268">(1,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="4807b-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="4807b-269">1</span><span class="sxs-lookup"><span data-stu-id="4807b-269">1</span></span></td>
<td><span data-ttu-id="4807b-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="4807b-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="4807b-271">500.00</span><span class="sxs-lookup"><span data-stu-id="4807b-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-272">CC002</span><span class="sxs-lookup"><span data-stu-id="4807b-272">CC002</span></span></td>
<td><span data-ttu-id="4807b-273">Finans</span><span class="sxs-lookup"><span data-stu-id="4807b-273">Finance</span></span></td>
<td><span data-ttu-id="4807b-274">(6,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="4807b-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="4807b-275">1</span><span class="sxs-lookup"><span data-stu-id="4807b-275">1</span></span></td>
<td><span data-ttu-id="4807b-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="4807b-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="4807b-277">500.00</span><span class="sxs-lookup"><span data-stu-id="4807b-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-278">CC003</span><span class="sxs-lookup"><span data-stu-id="4807b-278">CC003</span></span></td>
<td><span data-ttu-id="4807b-279">Montaj</span><span class="sxs-lookup"><span data-stu-id="4807b-279">Assembly</span></span></td>
<td><span data-ttu-id="4807b-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="4807b-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="4807b-281">0</span><span class="sxs-lookup"><span data-stu-id="4807b-281">0</span></span></td>
<td><span data-ttu-id="4807b-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="4807b-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="4807b-283">0,00</span><span class="sxs-lookup"><span data-stu-id="4807b-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="4807b-284">Günlük</span><span class="sxs-lookup"><span data-stu-id="4807b-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4807b-285">Günlük</span><span class="sxs-lookup"><span data-stu-id="4807b-285">Journal</span></span></th>
<th><span data-ttu-id="4807b-286">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="4807b-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4807b-287">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="4807b-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4807b-288">Sürüm</span><span class="sxs-lookup"><span data-stu-id="4807b-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4807b-289">00002</span><span class="sxs-lookup"><span data-stu-id="4807b-289">00002</span></span></td>
<td><span data-ttu-id="4807b-290">Maliyet dağıtımı hesaplama günlüğü</span><span class="sxs-lookup"><span data-stu-id="4807b-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="4807b-291">Mali</span><span class="sxs-lookup"><span data-stu-id="4807b-291">Fiscal</span></span></td>
<td><span data-ttu-id="4807b-292">2017</span><span class="sxs-lookup"><span data-stu-id="4807b-292">2017</span></span></td>
<td><span data-ttu-id="4807b-293">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="4807b-293">Period 1</span></span></td>
<td><span data-ttu-id="4807b-294">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="4807b-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="4807b-295">Günlük girişleri (Maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="4807b-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4807b-296">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="4807b-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4807b-297">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4807b-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4807b-298">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="4807b-298">Cost element</span></span></th>
<th><span data-ttu-id="4807b-299">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="4807b-299">Cost behavior</span></span></th>
<th><span data-ttu-id="4807b-300">Tutar</span><span class="sxs-lookup"><span data-stu-id="4807b-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4807b-301">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="4807b-302">CC099</span><span class="sxs-lookup"><span data-stu-id="4807b-302">CC099</span></span></td>
<td><span data-ttu-id="4807b-303">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="4807b-303">Default cost center</span></span></td>
<td><span data-ttu-id="4807b-304">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-304">10001</span></span></td>
<td><span data-ttu-id="4807b-305">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-305">Electricity</span></span></td>
<td><span data-ttu-id="4807b-306">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-306">Fixed cost</span></span></td>
<td><span data-ttu-id="4807b-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="4807b-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-308">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="4807b-309">CC099</span><span class="sxs-lookup"><span data-stu-id="4807b-309">CC099</span></span></td>
<td><span data-ttu-id="4807b-310">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="4807b-310">Default cost center</span></span></td>
<td><span data-ttu-id="4807b-311">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-311">10001</span></span></td>
<td><span data-ttu-id="4807b-312">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-312">Electricity</span></span></td>
<td><span data-ttu-id="4807b-313">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-313">Variable cost</span></span></td>
<td><span data-ttu-id="4807b-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="4807b-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4807b-315">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="4807b-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4807b-316">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4807b-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4807b-317">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="4807b-317">Cost element</span></span></th>
<th><span data-ttu-id="4807b-318">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="4807b-318">Cost behavior</span></span></th>
<th><span data-ttu-id="4807b-319">Tutar</span><span class="sxs-lookup"><span data-stu-id="4807b-319">Amount</span></span></th>
<th><span data-ttu-id="4807b-320">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="4807b-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4807b-321">CC099</span><span class="sxs-lookup"><span data-stu-id="4807b-321">CC099</span></span></td>
<td><span data-ttu-id="4807b-322">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="4807b-322">Default cost center</span></span></td>
<td><span data-ttu-id="4807b-323">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-323">10001</span></span></td>
<td><span data-ttu-id="4807b-324">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-324">Electricity</span></span></td>
<td><span data-ttu-id="4807b-325">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-325">Fixed cost</span></span></td>
<td><span data-ttu-id="4807b-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="4807b-326">-1,000.00</span></span></td>
<td><span data-ttu-id="4807b-327">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-328">CC001</span><span class="sxs-lookup"><span data-stu-id="4807b-328">CC001</span></span></td>
<td><span data-ttu-id="4807b-329">İK</span><span class="sxs-lookup"><span data-stu-id="4807b-329">HR</span></span></td>
<td><span data-ttu-id="4807b-330">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-330">10001</span></span></td>
<td><span data-ttu-id="4807b-331">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-331">Electricity</span></span></td>
<td><span data-ttu-id="4807b-332">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-332">Fixed cost</span></span></td>
<td><span data-ttu-id="4807b-333">500.00</span><span class="sxs-lookup"><span data-stu-id="4807b-333">500.00</span></span></td>
<td><span data-ttu-id="4807b-334">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-335">CC002</span><span class="sxs-lookup"><span data-stu-id="4807b-335">CC002</span></span></td>
<td><span data-ttu-id="4807b-336">Finans</span><span class="sxs-lookup"><span data-stu-id="4807b-336">Finance</span></span></td>
<td><span data-ttu-id="4807b-337">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-337">10001</span></span></td>
<td><span data-ttu-id="4807b-338">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-338">Electricity</span></span></td>
<td><span data-ttu-id="4807b-339">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-339">Fixed cost</span></span></td>
<td><span data-ttu-id="4807b-340">500.00</span><span class="sxs-lookup"><span data-stu-id="4807b-340">500.00</span></span></td>
<td><span data-ttu-id="4807b-341">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-342">CC099</span><span class="sxs-lookup"><span data-stu-id="4807b-342">CC099</span></span></td>
<td><span data-ttu-id="4807b-343">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="4807b-343">Default cost center</span></span></td>
<td><span data-ttu-id="4807b-344">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-344">10001</span></span></td>
<td><span data-ttu-id="4807b-345">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-345">Electricity</span></span></td>
<td><span data-ttu-id="4807b-346">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-346">Variable cost</span></span></td>
<td><span data-ttu-id="4807b-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="4807b-347">-9,000.00</span></span></td>
<td><span data-ttu-id="4807b-348">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-349">CC001</span><span class="sxs-lookup"><span data-stu-id="4807b-349">CC001</span></span></td>
<td><span data-ttu-id="4807b-350">İK</span><span class="sxs-lookup"><span data-stu-id="4807b-350">HR</span></span></td>
<td><span data-ttu-id="4807b-351">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-351">10001</span></span></td>
<td><span data-ttu-id="4807b-352">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-352">Electricity</span></span></td>
<td><span data-ttu-id="4807b-353">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-353">Variable cost</span></span></td>
<td><span data-ttu-id="4807b-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="4807b-354">1,285.71</span></span></td>
<td><span data-ttu-id="4807b-355">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-356">CC002</span><span class="sxs-lookup"><span data-stu-id="4807b-356">CC002</span></span></td>
<td><span data-ttu-id="4807b-357">Finans</span><span class="sxs-lookup"><span data-stu-id="4807b-357">Finance</span></span></td>
<td><span data-ttu-id="4807b-358">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-358">10001</span></span></td>
<td><span data-ttu-id="4807b-359">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-359">Electricity</span></span></td>
<td><span data-ttu-id="4807b-360">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-360">Variable cost</span></span></td>
<td><span data-ttu-id="4807b-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="4807b-361">7,714.29</span></span></td>
<td><span data-ttu-id="4807b-362">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4807b-363">Daha fazla bilgi için bkz. [Maliyet dağıtımı ilkesi oluşturma ve bir maliyet kontrol birimine atama](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="4807b-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="4807b-364">Adım 3: Genel gider oranı hesaplama işlemi</span><span class="sxs-lookup"><span data-stu-id="4807b-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="4807b-365">Genel gider oranı, bir veya birden fazla belirli maliyet nesnesine masraf yüklemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4807b-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="4807b-366">Masraf, önceden belirlenmiş maliyet oranına ve tahsisat tabanından hesaplanan büyüklüğe dayanır.</span><span class="sxs-lookup"><span data-stu-id="4807b-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="4807b-367">Genel gider oranını tanımlama</span><span class="sxs-lookup"><span data-stu-id="4807b-367">Define the overhead rate</span></span>

<span data-ttu-id="4807b-368">Maliyet nesnesi CC001 HR, bir dizi dahili projeye katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="4807b-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="4807b-369">HR projeleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4807b-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4807b-370">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4807b-370">Cost object</span></span></th>
<th><span data-ttu-id="4807b-371">Saatler</span><span class="sxs-lookup"><span data-stu-id="4807b-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4807b-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="4807b-372">Proj 1</span></span></td>
<td><span data-ttu-id="4807b-373">Proje 1</span><span class="sxs-lookup"><span data-stu-id="4807b-373">Project 1</span></span></td>
<td><span data-ttu-id="4807b-374">3</span><span class="sxs-lookup"><span data-stu-id="4807b-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="4807b-375">Proj 2</span></span></td>
<td><span data-ttu-id="4807b-376">Proje 2</span><span class="sxs-lookup"><span data-stu-id="4807b-376">Project 2</span></span></td>
<td><span data-ttu-id="4807b-377">1</span><span class="sxs-lookup"><span data-stu-id="4807b-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4807b-378">Maliyet projeleri dağıtımı için bir önceden belirlenmiş maliyet oranı tanımlandı.</span><span class="sxs-lookup"><span data-stu-id="4807b-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4807b-379">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4807b-379">Cost object</span></span></th>
<th><span data-ttu-id="4807b-380">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="4807b-380">Cost element</span></span></th>
<th><span data-ttu-id="4807b-381">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="4807b-381">Cost behavior</span></span></th>
<th><span data-ttu-id="4807b-382">Birimler</span><span class="sxs-lookup"><span data-stu-id="4807b-382">Units</span></span></th>
<th><span data-ttu-id="4807b-383">Ücret</span><span class="sxs-lookup"><span data-stu-id="4807b-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4807b-384">CC001</span><span class="sxs-lookup"><span data-stu-id="4807b-384">CC001</span></span></td>
<td><span data-ttu-id="4807b-385">İK</span><span class="sxs-lookup"><span data-stu-id="4807b-385">HR</span></span></td>
<td><span data-ttu-id="4807b-386">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-386">10001</span></span></td>
<td><span data-ttu-id="4807b-387">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-387">Variable cost</span></span></td>
<td><span data-ttu-id="4807b-388">1</span><span class="sxs-lookup"><span data-stu-id="4807b-388">1</span></span></td>
<td><span data-ttu-id="4807b-389">10</span><span class="sxs-lookup"><span data-stu-id="4807b-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4807b-390">Aşağıdaki tablo, HR projeleri bir tahsisat tabanı olarak uygulandığındaki sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="4807b-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4807b-391">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4807b-391">Cost object</span></span></th>
<th><span data-ttu-id="4807b-392">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="4807b-392">Magnitude</span></span></th>
<th><span data-ttu-id="4807b-393">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="4807b-393">Cost element</span></span></th>
<th><span data-ttu-id="4807b-394">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="4807b-394">Allocation factor</span></span></th>
<th><span data-ttu-id="4807b-395">Tutar</span><span class="sxs-lookup"><span data-stu-id="4807b-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4807b-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="4807b-396">Proj 1</span></span></td>
<td><span data-ttu-id="4807b-397">Proje 1</span><span class="sxs-lookup"><span data-stu-id="4807b-397">Project 1</span></span></td>
<td><span data-ttu-id="4807b-398">3</span><span class="sxs-lookup"><span data-stu-id="4807b-398">3</span></span></td>
<td><span data-ttu-id="4807b-399">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-399">10001</span></span></td>
<td><span data-ttu-id="4807b-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="4807b-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="4807b-401">30.00</span><span class="sxs-lookup"><span data-stu-id="4807b-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="4807b-402">Proj 2</span></span></td>
<td><span data-ttu-id="4807b-403">Proje 2</span><span class="sxs-lookup"><span data-stu-id="4807b-403">Project 2</span></span></td>
<td><span data-ttu-id="4807b-404">1</span><span class="sxs-lookup"><span data-stu-id="4807b-404">1</span></span></td>
<td><span data-ttu-id="4807b-405">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-405">10001</span></span></td>
<td><span data-ttu-id="4807b-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="4807b-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="4807b-407">10,00</span><span class="sxs-lookup"><span data-stu-id="4807b-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="4807b-408">Günlük</span><span class="sxs-lookup"><span data-stu-id="4807b-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4807b-409">Günlük</span><span class="sxs-lookup"><span data-stu-id="4807b-409">Journal</span></span></th>
<th><span data-ttu-id="4807b-410">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="4807b-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4807b-411">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="4807b-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4807b-412">Sürüm</span><span class="sxs-lookup"><span data-stu-id="4807b-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4807b-413">00003</span><span class="sxs-lookup"><span data-stu-id="4807b-413">00003</span></span></td>
<td><span data-ttu-id="4807b-414">Genel gider oranı hesaplaması günlüğü</span><span class="sxs-lookup"><span data-stu-id="4807b-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="4807b-415">Mali</span><span class="sxs-lookup"><span data-stu-id="4807b-415">Fiscal</span></span></td>
<td><span data-ttu-id="4807b-416">2017</span><span class="sxs-lookup"><span data-stu-id="4807b-416">2017</span></span></td>
<td><span data-ttu-id="4807b-417">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="4807b-417">Period 1</span></span></td>
<td><span data-ttu-id="4807b-418">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="4807b-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="4807b-419">Günlük girişleri (Genel gider oranı hesaplaması için günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="4807b-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4807b-420">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="4807b-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4807b-421">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4807b-421">Cost object</span></span></th>
<th><span data-ttu-id="4807b-422">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="4807b-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4807b-423">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="4807b-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="4807b-424">Proj 1</span></span></td>
<td><span data-ttu-id="4807b-425">Dahili Proj 1</span><span class="sxs-lookup"><span data-stu-id="4807b-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="4807b-426">3,00</span><span class="sxs-lookup"><span data-stu-id="4807b-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-427">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="4807b-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="4807b-428">Proj 2</span></span></td>
<td><span data-ttu-id="4807b-429">Dahili Proj 2</span><span class="sxs-lookup"><span data-stu-id="4807b-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="4807b-430">1.00</span><span class="sxs-lookup"><span data-stu-id="4807b-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4807b-431">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="4807b-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4807b-432">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4807b-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4807b-433">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="4807b-433">Cost element</span></span></th>
<th><span data-ttu-id="4807b-434">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="4807b-434">Cost behavior</span></span></th>
<th><span data-ttu-id="4807b-435">Tutar</span><span class="sxs-lookup"><span data-stu-id="4807b-435">Amount</span></span></th>
<th><span data-ttu-id="4807b-436">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="4807b-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4807b-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="4807b-437">CC0001</span></span></td>
<td><span data-ttu-id="4807b-438">İK</span><span class="sxs-lookup"><span data-stu-id="4807b-438">HR</span></span></td>
<td><span data-ttu-id="4807b-439">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-439">10001</span></span></td>
<td><span data-ttu-id="4807b-440">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-440">Electricity</span></span></td>
<td><span data-ttu-id="4807b-441">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-441">Variable cost</span></span></td>
<td><span data-ttu-id="4807b-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="4807b-442">-30.00</span></span></td>
<td><span data-ttu-id="4807b-443">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="4807b-444">Proj 1</span></span></td>
<td><span data-ttu-id="4807b-445">Dahili Proj 1</span><span class="sxs-lookup"><span data-stu-id="4807b-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="4807b-446">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-446">10001</span></span></td>
<td><span data-ttu-id="4807b-447">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-447">Electricity</span></span></td>
<td><span data-ttu-id="4807b-448">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-448">Variable cost</span></span></td>
<td><span data-ttu-id="4807b-449">30.00</span><span class="sxs-lookup"><span data-stu-id="4807b-449">30.00</span></span></td>
<td><span data-ttu-id="4807b-450">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-451">CC001</span><span class="sxs-lookup"><span data-stu-id="4807b-451">CC001</span></span></td>
<td><span data-ttu-id="4807b-452">İK</span><span class="sxs-lookup"><span data-stu-id="4807b-452">HR</span></span></td>
<td><span data-ttu-id="4807b-453">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-453">10001</span></span></td>
<td><span data-ttu-id="4807b-454">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-454">Electricity</span></span></td>
<td><span data-ttu-id="4807b-455">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-455">Variable cost</span></span></td>
<td><span data-ttu-id="4807b-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="4807b-456">-10.00</span></span></td>
<td><span data-ttu-id="4807b-457">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="4807b-458">Proj 2</span></span></td>
<td><span data-ttu-id="4807b-459">Dahili Proj 2</span><span class="sxs-lookup"><span data-stu-id="4807b-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="4807b-460">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-460">10001</span></span></td>
<td><span data-ttu-id="4807b-461">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-461">Electricity</span></span></td>
<td><span data-ttu-id="4807b-462">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-462">Variable cost</span></span></td>
<td><span data-ttu-id="4807b-463">10,00</span><span class="sxs-lookup"><span data-stu-id="4807b-463">10.00</span></span></td>
<td><span data-ttu-id="4807b-464">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4807b-465">Daha fazla bilgi için [Genel gider hesaplaması gerçekleştir](cost-rollup.md#perform-overhead-calculation) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="4807b-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="4807b-466">Adım 4: Maliyet tahsisat hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="4807b-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="4807b-467">Tahsisat, bir tahsisat tabanı kullanarak bir maliyet nesnesinin diğer maliyet nesnelerine bakiyesini tahsis eder.</span><span class="sxs-lookup"><span data-stu-id="4807b-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="4807b-468">Finance karşılıklı tahsisat yöntemini desteklemektedir.</span><span class="sxs-lookup"><span data-stu-id="4807b-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="4807b-469">Karşılıklı tahsisat yönteminde, yardımcı maliyet nesnelerinin değiştiği karşılıklı hizmetler tümüyle tanınır.</span><span class="sxs-lookup"><span data-stu-id="4807b-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="4807b-470">Sistem, tahsisatların doğru gerçekleştireceği sırayı otomatik olarak belirler.</span><span class="sxs-lookup"><span data-stu-id="4807b-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="4807b-471">Bir maliyet nesnesinin bakiyesi tek bir tahsisat tabanı tarafından tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="4807b-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="4807b-472">Yeni maliyet nesnesi boyutları arasındaki tahsisatlar ve onların üyeleri desteklenir.</span><span class="sxs-lookup"><span data-stu-id="4807b-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="4807b-473">Tahsisatın sırası, maliyet kontrol birimi tarafından kontrol edilir.</span><span class="sxs-lookup"><span data-stu-id="4807b-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="4807b-474">[![Karşılıklı yöntemi](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="4807b-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="4807b-475">Maliyet tahsisatını tanımla</span><span class="sxs-lookup"><span data-stu-id="4807b-475">Define the cost allocation</span></span>

<span data-ttu-id="4807b-476">Bir maliyetin akışını nasıl izleyeceğinize dair basit bir örnek aşağıda verilmiştir,</span><span class="sxs-lookup"><span data-stu-id="4807b-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="4807b-477">Maliyet nesnesi CC001 HR, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="4807b-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="4807b-478">HR hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4807b-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4807b-479">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4807b-479">Cost object</span></span></th>
<th><span data-ttu-id="4807b-480">HR hizmetleri</span><span class="sxs-lookup"><span data-stu-id="4807b-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4807b-481">CC002</span><span class="sxs-lookup"><span data-stu-id="4807b-481">CC002</span></span></td>
<td><span data-ttu-id="4807b-482">Finans</span><span class="sxs-lookup"><span data-stu-id="4807b-482">Finance</span></span></td>
<td><span data-ttu-id="4807b-483">35</span><span class="sxs-lookup"><span data-stu-id="4807b-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-484">CC003</span><span class="sxs-lookup"><span data-stu-id="4807b-484">CC003</span></span></td>
<td><span data-ttu-id="4807b-485">Montaj</span><span class="sxs-lookup"><span data-stu-id="4807b-485">Assembly</span></span></td>
<td><span data-ttu-id="4807b-486">55</span><span class="sxs-lookup"><span data-stu-id="4807b-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-487">CC004</span><span class="sxs-lookup"><span data-stu-id="4807b-487">CC004</span></span></td>
<td><span data-ttu-id="4807b-488">Paketleme</span><span class="sxs-lookup"><span data-stu-id="4807b-488">Packaging</span></span></td>
<td><span data-ttu-id="4807b-489">10</span><span class="sxs-lookup"><span data-stu-id="4807b-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4807b-490">Maliyet nesnesi CC002 Finans, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="4807b-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="4807b-491">Finans hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4807b-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4807b-492">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4807b-492">Cost object</span></span></th>
<th><span data-ttu-id="4807b-493">Finans hizmetleri</span><span class="sxs-lookup"><span data-stu-id="4807b-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4807b-494">CC003</span><span class="sxs-lookup"><span data-stu-id="4807b-494">CC003</span></span></td>
<td><span data-ttu-id="4807b-495">Montaj</span><span class="sxs-lookup"><span data-stu-id="4807b-495">Assembly</span></span></td>
<td><span data-ttu-id="4807b-496">65</span><span class="sxs-lookup"><span data-stu-id="4807b-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-497">CC004</span><span class="sxs-lookup"><span data-stu-id="4807b-497">CC004</span></span></td>
<td><span data-ttu-id="4807b-498">Paketleme</span><span class="sxs-lookup"><span data-stu-id="4807b-498">Packaging</span></span></td>
<td><span data-ttu-id="4807b-499">35</span><span class="sxs-lookup"><span data-stu-id="4807b-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4807b-500">Maliyet nesnesi CC003 Derleme, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="4807b-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="4807b-501">Derleme hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4807b-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4807b-502">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4807b-502">Cost object</span></span></th>
<th><span data-ttu-id="4807b-503">Derleme Hizmetleri (saat)</span><span class="sxs-lookup"><span data-stu-id="4807b-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4807b-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4807b-504">Prod 1</span></span></td>
<td><span data-ttu-id="4807b-505">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="4807b-505">Product 1</span></span></td>
<td><span data-ttu-id="4807b-506">60</span><span class="sxs-lookup"><span data-stu-id="4807b-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4807b-507">Prod 2</span></span></td>
<td><span data-ttu-id="4807b-508">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="4807b-508">Product 2</span></span></td>
<td><span data-ttu-id="4807b-509">20</span><span class="sxs-lookup"><span data-stu-id="4807b-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4807b-510">Maliyet nesnesi CC004 Ambalajlama, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="4807b-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="4807b-511">Ambalajlama hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4807b-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4807b-512">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4807b-512">Cost object</span></span></th>
<th><span data-ttu-id="4807b-513">Ambalajlama hizmetleri (saat)</span><span class="sxs-lookup"><span data-stu-id="4807b-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4807b-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4807b-514">Prod 1</span></span></td>
<td><span data-ttu-id="4807b-515">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="4807b-515">Product 1</span></span></td>
<td><span data-ttu-id="4807b-516">80</span><span class="sxs-lookup"><span data-stu-id="4807b-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4807b-517">Prod 2</span></span></td>
<td><span data-ttu-id="4807b-518">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="4807b-518">Product 2</span></span></td>
<td><span data-ttu-id="4807b-519">15</span><span class="sxs-lookup"><span data-stu-id="4807b-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="4807b-520">Bir ürünün tükettiği üretim saatleri gibi istatistiki ölçümler, doğrudan kaynak verilerinden alınabilir.</span><span class="sxs-lookup"><span data-stu-id="4807b-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="4807b-521">Daha fazla bilgi için, [İstatistiksel ölçüm sağlayıcı şablonu](statistical-measure-provider-template.md#statistical-measure-provider-template) bakın.</span><span class="sxs-lookup"><span data-stu-id="4807b-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="4807b-522">Aşağıdaki tablo, İK hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığında ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="4807b-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4807b-523">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4807b-523">Cost object</span></span></th>
<th><span data-ttu-id="4807b-524">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="4807b-524">Magnitude</span></span></th>
<th><span data-ttu-id="4807b-525">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="4807b-525">Allocation factor</span></span></th>
<th><span data-ttu-id="4807b-526">Tutar</span><span class="sxs-lookup"><span data-stu-id="4807b-526">Amount</span></span></th>
<th><span data-ttu-id="4807b-527">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="4807b-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4807b-528">CC002</span><span class="sxs-lookup"><span data-stu-id="4807b-528">CC002</span></span></td>
<td><span data-ttu-id="4807b-529">Finans</span><span class="sxs-lookup"><span data-stu-id="4807b-529">Finance</span></span></td>
<td><span data-ttu-id="4807b-530">35</span><span class="sxs-lookup"><span data-stu-id="4807b-530">35</span></span></td>
<td><span data-ttu-id="4807b-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="4807b-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="4807b-532">175.00</span><span class="sxs-lookup"><span data-stu-id="4807b-532">175.00</span></span></td>
<td><span data-ttu-id="4807b-533">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-534">CC003</span><span class="sxs-lookup"><span data-stu-id="4807b-534">CC003</span></span></td>
<td><span data-ttu-id="4807b-535">Montaj</span><span class="sxs-lookup"><span data-stu-id="4807b-535">Assembly</span></span></td>
<td><span data-ttu-id="4807b-536">55</span><span class="sxs-lookup"><span data-stu-id="4807b-536">55</span></span></td>
<td><span data-ttu-id="4807b-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="4807b-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="4807b-538">275.00</span><span class="sxs-lookup"><span data-stu-id="4807b-538">275.00</span></span></td>
<td><span data-ttu-id="4807b-539">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-540">CC004</span><span class="sxs-lookup"><span data-stu-id="4807b-540">CC004</span></span></td>
<td><span data-ttu-id="4807b-541">Paketleme</span><span class="sxs-lookup"><span data-stu-id="4807b-541">Packaging</span></span></td>
<td><span data-ttu-id="4807b-542">10</span><span class="sxs-lookup"><span data-stu-id="4807b-542">10</span></span></td>
<td><span data-ttu-id="4807b-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="4807b-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="4807b-544">50,00</span><span class="sxs-lookup"><span data-stu-id="4807b-544">50.00</span></span></td>
<td><span data-ttu-id="4807b-545">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-546">CC002</span><span class="sxs-lookup"><span data-stu-id="4807b-546">CC002</span></span></td>
<td><span data-ttu-id="4807b-547">Finans</span><span class="sxs-lookup"><span data-stu-id="4807b-547">Finance</span></span></td>
<td><span data-ttu-id="4807b-548">35</span><span class="sxs-lookup"><span data-stu-id="4807b-548">35</span></span></td>
<td><span data-ttu-id="4807b-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="4807b-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="4807b-550">436.00</span><span class="sxs-lookup"><span data-stu-id="4807b-550">436.00</span></span></td>
<td><span data-ttu-id="4807b-551">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-552">CC003</span><span class="sxs-lookup"><span data-stu-id="4807b-552">CC003</span></span></td>
<td><span data-ttu-id="4807b-553">Montaj</span><span class="sxs-lookup"><span data-stu-id="4807b-553">Assembly</span></span></td>
<td><span data-ttu-id="4807b-554">55</span><span class="sxs-lookup"><span data-stu-id="4807b-554">55</span></span></td>
<td><span data-ttu-id="4807b-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="4807b-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="4807b-556">685.14</span><span class="sxs-lookup"><span data-stu-id="4807b-556">685.14</span></span></td>
<td><span data-ttu-id="4807b-557">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-558">CC004</span><span class="sxs-lookup"><span data-stu-id="4807b-558">CC004</span></span></td>
<td><span data-ttu-id="4807b-559">Paketleme</span><span class="sxs-lookup"><span data-stu-id="4807b-559">Packaging</span></span></td>
<td><span data-ttu-id="4807b-560">10</span><span class="sxs-lookup"><span data-stu-id="4807b-560">10</span></span></td>
<td><span data-ttu-id="4807b-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="4807b-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="4807b-562">124.57</span><span class="sxs-lookup"><span data-stu-id="4807b-562">124.57</span></span></td>
<td><span data-ttu-id="4807b-563">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4807b-564">Aşağıdaki tablo, Finans hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="4807b-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4807b-565">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4807b-565">Cost object</span></span></th>
<th><span data-ttu-id="4807b-566">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="4807b-566">Magnitude</span></span></th>
<th><span data-ttu-id="4807b-567">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="4807b-567">Allocation factor</span></span></th>
<th><span data-ttu-id="4807b-568">Tutar</span><span class="sxs-lookup"><span data-stu-id="4807b-568">Amount</span></span></th>
<th><span data-ttu-id="4807b-569">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="4807b-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4807b-570">CC003</span><span class="sxs-lookup"><span data-stu-id="4807b-570">CC003</span></span></td>
<td><span data-ttu-id="4807b-571">Montaj</span><span class="sxs-lookup"><span data-stu-id="4807b-571">Assembly</span></span></td>
<td><span data-ttu-id="4807b-572">65</span><span class="sxs-lookup"><span data-stu-id="4807b-572">65</span></span></td>
<td><span data-ttu-id="4807b-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="4807b-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="4807b-574">438.75</span><span class="sxs-lookup"><span data-stu-id="4807b-574">438.75</span></span></td>
<td><span data-ttu-id="4807b-575">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-576">CC004</span><span class="sxs-lookup"><span data-stu-id="4807b-576">CC004</span></span></td>
<td><span data-ttu-id="4807b-577">Paketleme</span><span class="sxs-lookup"><span data-stu-id="4807b-577">Packaging</span></span></td>
<td><span data-ttu-id="4807b-578">35</span><span class="sxs-lookup"><span data-stu-id="4807b-578">35</span></span></td>
<td><span data-ttu-id="4807b-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="4807b-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="4807b-580">236.25</span><span class="sxs-lookup"><span data-stu-id="4807b-580">236.25</span></span></td>
<td><span data-ttu-id="4807b-581">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-582">CC003</span><span class="sxs-lookup"><span data-stu-id="4807b-582">CC003</span></span></td>
<td><span data-ttu-id="4807b-583">Montaj</span><span class="sxs-lookup"><span data-stu-id="4807b-583">Assembly</span></span></td>
<td><span data-ttu-id="4807b-584">65</span><span class="sxs-lookup"><span data-stu-id="4807b-584">65</span></span></td>
<td><span data-ttu-id="4807b-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="4807b-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="4807b-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="4807b-586">5,297.69</span></span></td>
<td><span data-ttu-id="4807b-587">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-588">CC004</span><span class="sxs-lookup"><span data-stu-id="4807b-588">CC004</span></span></td>
<td><span data-ttu-id="4807b-589">Paketleme</span><span class="sxs-lookup"><span data-stu-id="4807b-589">Packaging</span></span></td>
<td><span data-ttu-id="4807b-590">35</span><span class="sxs-lookup"><span data-stu-id="4807b-590">35</span></span></td>
<td><span data-ttu-id="4807b-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="4807b-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="4807b-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="4807b-592">2,852.60</span></span></td>
<td><span data-ttu-id="4807b-593">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4807b-594">Aşağıdaki tablo, Derleme hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="4807b-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4807b-595">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4807b-595">Cost object</span></span></th>
<th><span data-ttu-id="4807b-596">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="4807b-596">Magnitude</span></span></th>
<th><span data-ttu-id="4807b-597">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="4807b-597">Allocation factor</span></span></th>
<th><span data-ttu-id="4807b-598">Tutar</span><span class="sxs-lookup"><span data-stu-id="4807b-598">Amount</span></span></th>
<th><span data-ttu-id="4807b-599">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="4807b-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4807b-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4807b-600">Prod 1</span></span></td>
<td><span data-ttu-id="4807b-601">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="4807b-601">Product 1</span></span></td>
<td><span data-ttu-id="4807b-602">60</span><span class="sxs-lookup"><span data-stu-id="4807b-602">60</span></span></td>
<td><span data-ttu-id="4807b-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="4807b-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="4807b-604">535.31</span><span class="sxs-lookup"><span data-stu-id="4807b-604">535.31</span></span></td>
<td><span data-ttu-id="4807b-605">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4807b-606">Prod 2</span></span></td>
<td><span data-ttu-id="4807b-607">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="4807b-607">Product 2</span></span></td>
<td><span data-ttu-id="4807b-608">20</span><span class="sxs-lookup"><span data-stu-id="4807b-608">20</span></span></td>
<td><span data-ttu-id="4807b-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="4807b-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="4807b-610">178.44</span><span class="sxs-lookup"><span data-stu-id="4807b-610">178.44</span></span></td>
<td><span data-ttu-id="4807b-611">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4807b-612">Prod 1</span></span></td>
<td><span data-ttu-id="4807b-613">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="4807b-613">Product 1</span></span></td>
<td><span data-ttu-id="4807b-614">60</span><span class="sxs-lookup"><span data-stu-id="4807b-614">60</span></span></td>
<td><span data-ttu-id="4807b-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="4807b-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="4807b-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="4807b-616">4,487.12</span></span></td>
<td><span data-ttu-id="4807b-617">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4807b-618">Prod 2</span></span></td>
<td><span data-ttu-id="4807b-619">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="4807b-619">Product 2</span></span></td>
<td><span data-ttu-id="4807b-620">20</span><span class="sxs-lookup"><span data-stu-id="4807b-620">20</span></span></td>
<td><span data-ttu-id="4807b-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="4807b-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="4807b-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="4807b-622">1,495.71</span></span></td>
<td><span data-ttu-id="4807b-623">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4807b-624">Aşağıdaki tablo, Paketleme hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="4807b-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4807b-625">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4807b-625">Cost object</span></span></th>
<th><span data-ttu-id="4807b-626">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="4807b-626">Magnitude</span></span></th>
<th><span data-ttu-id="4807b-627">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="4807b-627">Allocation factor</span></span></th>
<th><span data-ttu-id="4807b-628">Tutar</span><span class="sxs-lookup"><span data-stu-id="4807b-628">Amount</span></span></th>
<th><span data-ttu-id="4807b-629">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="4807b-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4807b-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4807b-630">Prod 1</span></span></td>
<td><span data-ttu-id="4807b-631">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="4807b-631">Product 1</span></span></td>
<td><span data-ttu-id="4807b-632">80</span><span class="sxs-lookup"><span data-stu-id="4807b-632">80</span></span></td>
<td><span data-ttu-id="4807b-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="4807b-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="4807b-634">241.05</span><span class="sxs-lookup"><span data-stu-id="4807b-634">241.05</span></span></td>
<td><span data-ttu-id="4807b-635">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4807b-636">Prod 2</span></span></td>
<td><span data-ttu-id="4807b-637">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="4807b-637">Product 2</span></span></td>
<td><span data-ttu-id="4807b-638">15</span><span class="sxs-lookup"><span data-stu-id="4807b-638">15</span></span></td>
<td><span data-ttu-id="4807b-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="4807b-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="4807b-640">45.20</span><span class="sxs-lookup"><span data-stu-id="4807b-640">45.20</span></span></td>
<td><span data-ttu-id="4807b-641">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4807b-642">Prod 1</span></span></td>
<td><span data-ttu-id="4807b-643">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="4807b-643">Product 1</span></span></td>
<td><span data-ttu-id="4807b-644">80</span><span class="sxs-lookup"><span data-stu-id="4807b-644">80</span></span></td>
<td><span data-ttu-id="4807b-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="4807b-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="4807b-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="4807b-646">2,507.09</span></span></td>
<td><span data-ttu-id="4807b-647">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4807b-648">Prod 2</span></span></td>
<td><span data-ttu-id="4807b-649">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="4807b-649">Product 2</span></span></td>
<td><span data-ttu-id="4807b-650">15</span><span class="sxs-lookup"><span data-stu-id="4807b-650">15</span></span></td>
<td><span data-ttu-id="4807b-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="4807b-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="4807b-652">470.08</span><span class="sxs-lookup"><span data-stu-id="4807b-652">470.08</span></span></td>
<td><span data-ttu-id="4807b-653">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="4807b-654">Günlük girişleri (maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="4807b-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4807b-655">Günlük</span><span class="sxs-lookup"><span data-stu-id="4807b-655">Journal</span></span></th>
<th><span data-ttu-id="4807b-656">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="4807b-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4807b-657">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="4807b-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4807b-658">Sürüm</span><span class="sxs-lookup"><span data-stu-id="4807b-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4807b-659">00004</span><span class="sxs-lookup"><span data-stu-id="4807b-659">00004</span></span></td>
<td><span data-ttu-id="4807b-660">Maliyet tahsisatı günlüğü</span><span class="sxs-lookup"><span data-stu-id="4807b-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="4807b-661">Mali</span><span class="sxs-lookup"><span data-stu-id="4807b-661">Fiscal</span></span></td>
<td><span data-ttu-id="4807b-662">2017</span><span class="sxs-lookup"><span data-stu-id="4807b-662">2017</span></span></td>
<td><span data-ttu-id="4807b-663">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="4807b-663">Period 1</span></span></td>
<td><span data-ttu-id="4807b-664">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="4807b-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="4807b-665">Günlük satırları</span><span class="sxs-lookup"><span data-stu-id="4807b-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4807b-666">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="4807b-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4807b-667">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4807b-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4807b-668">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="4807b-668">Cost element</span></span></th>
<th><span data-ttu-id="4807b-669">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="4807b-669">Cost behavior</span></span></th>
<th><span data-ttu-id="4807b-670">Tutar</span><span class="sxs-lookup"><span data-stu-id="4807b-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4807b-671">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="4807b-672">CC001</span><span class="sxs-lookup"><span data-stu-id="4807b-672">CC001</span></span></td>
<td><span data-ttu-id="4807b-673">İK</span><span class="sxs-lookup"><span data-stu-id="4807b-673">HR</span></span></td>
<td><span data-ttu-id="4807b-674">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-674">10001</span></span></td>
<td><span data-ttu-id="4807b-675">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-675">Electricity</span></span></td>
<td><span data-ttu-id="4807b-676">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-676">Fixed cost</span></span></td>
<td><span data-ttu-id="4807b-677">500.00</span><span class="sxs-lookup"><span data-stu-id="4807b-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-678">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="4807b-679">CC001</span><span class="sxs-lookup"><span data-stu-id="4807b-679">CC001</span></span></td>
<td><span data-ttu-id="4807b-680">İK</span><span class="sxs-lookup"><span data-stu-id="4807b-680">HR</span></span></td>
<td><span data-ttu-id="4807b-681">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-681">10001</span></span></td>
<td><span data-ttu-id="4807b-682">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-682">Electricity</span></span></td>
<td><span data-ttu-id="4807b-683">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-683">Variable cost</span></span></td>
<td><span data-ttu-id="4807b-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="4807b-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-685">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="4807b-686">CC002</span><span class="sxs-lookup"><span data-stu-id="4807b-686">CC002</span></span></td>
<td><span data-ttu-id="4807b-687">Finans</span><span class="sxs-lookup"><span data-stu-id="4807b-687">Finance</span></span></td>
<td><span data-ttu-id="4807b-688">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-688">10001</span></span></td>
<td><span data-ttu-id="4807b-689">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-689">Electricity</span></span></td>
<td><span data-ttu-id="4807b-690">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-690">Fixed cost</span></span></td>
<td><span data-ttu-id="4807b-691">675.00</span><span class="sxs-lookup"><span data-stu-id="4807b-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-692">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="4807b-693">CC002</span><span class="sxs-lookup"><span data-stu-id="4807b-693">CC002</span></span></td>
<td><span data-ttu-id="4807b-694">Finans</span><span class="sxs-lookup"><span data-stu-id="4807b-694">Finance</span></span></td>
<td><span data-ttu-id="4807b-695">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-695">10001</span></span></td>
<td><span data-ttu-id="4807b-696">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-696">Electricity</span></span></td>
<td><span data-ttu-id="4807b-697">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-697">Variable cost</span></span></td>
<td><span data-ttu-id="4807b-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="4807b-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-699">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="4807b-700">CC003</span><span class="sxs-lookup"><span data-stu-id="4807b-700">CC003</span></span></td>
<td><span data-ttu-id="4807b-701">Montaj</span><span class="sxs-lookup"><span data-stu-id="4807b-701">Assembly</span></span></td>
<td><span data-ttu-id="4807b-702">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-702">10001</span></span></td>
<td><span data-ttu-id="4807b-703">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-703">Electricity</span></span></td>
<td><span data-ttu-id="4807b-704">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-704">Fixed cost</span></span></td>
<td><span data-ttu-id="4807b-705">713.75</span><span class="sxs-lookup"><span data-stu-id="4807b-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-706">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="4807b-707">CC003</span><span class="sxs-lookup"><span data-stu-id="4807b-707">CC003</span></span></td>
<td><span data-ttu-id="4807b-708">Montaj</span><span class="sxs-lookup"><span data-stu-id="4807b-708">Assembly</span></span></td>
<td><span data-ttu-id="4807b-709">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-709">10001</span></span></td>
<td><span data-ttu-id="4807b-710">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-710">Electricity</span></span></td>
<td><span data-ttu-id="4807b-711">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-711">Variable cost</span></span></td>
<td><span data-ttu-id="4807b-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="4807b-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-713">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="4807b-714">CC003</span><span class="sxs-lookup"><span data-stu-id="4807b-714">CC003</span></span></td>
<td><span data-ttu-id="4807b-715">Paketleme</span><span class="sxs-lookup"><span data-stu-id="4807b-715">Packaging</span></span></td>
<td><span data-ttu-id="4807b-716">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-716">10001</span></span></td>
<td><span data-ttu-id="4807b-717">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-717">Electricity</span></span></td>
<td><span data-ttu-id="4807b-718">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-718">Fixed cost</span></span></td>
<td><span data-ttu-id="4807b-719">286.25</span><span class="sxs-lookup"><span data-stu-id="4807b-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-720">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="4807b-721">CC003</span><span class="sxs-lookup"><span data-stu-id="4807b-721">CC003</span></span></td>
<td><span data-ttu-id="4807b-722">Paketleme</span><span class="sxs-lookup"><span data-stu-id="4807b-722">Packaging</span></span></td>
<td><span data-ttu-id="4807b-723">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-723">10001</span></span></td>
<td><span data-ttu-id="4807b-724">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-724">Electricity</span></span></td>
<td><span data-ttu-id="4807b-725">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-725">Variable cost</span></span></td>
<td><span data-ttu-id="4807b-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="4807b-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-727">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="4807b-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4807b-728">Prod 1</span></span></td>
<td><span data-ttu-id="4807b-729">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="4807b-729">Product 1</span></span></td>
<td><span data-ttu-id="4807b-730">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-730">10001</span></span></td>
<td><span data-ttu-id="4807b-731">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-731">Electricity</span></span></td>
<td><span data-ttu-id="4807b-732">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-732">Fixed cost</span></span></td>
<td><span data-ttu-id="4807b-733">776.36</span><span class="sxs-lookup"><span data-stu-id="4807b-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-734">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="4807b-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4807b-735">Prod 1</span></span></td>
<td><span data-ttu-id="4807b-736">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="4807b-736">Product 1</span></span></td>
<td><span data-ttu-id="4807b-737">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-737">10001</span></span></td>
<td><span data-ttu-id="4807b-738">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-738">Electricity</span></span></td>
<td><span data-ttu-id="4807b-739">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-739">Variable cost</span></span></td>
<td><span data-ttu-id="4807b-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="4807b-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-741">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="4807b-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4807b-742">Prod 2</span></span></td>
<td><span data-ttu-id="4807b-743">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="4807b-743">Product 1</span></span></td>
<td><span data-ttu-id="4807b-744">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-744">10001</span></span></td>
<td><span data-ttu-id="4807b-745">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-745">Electricity</span></span></td>
<td><span data-ttu-id="4807b-746">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-746">Fixed cost</span></span></td>
<td><span data-ttu-id="4807b-747">223.64</span><span class="sxs-lookup"><span data-stu-id="4807b-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-748">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="4807b-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4807b-749">Prod 2</span></span></td>
<td><span data-ttu-id="4807b-750">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="4807b-750">Product 1</span></span></td>
<td><span data-ttu-id="4807b-751">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-751">10001</span></span></td>
<td><span data-ttu-id="4807b-752">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-752">Electricity</span></span></td>
<td><span data-ttu-id="4807b-753">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-753">Variable cost</span></span></td>
<td><span data-ttu-id="4807b-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="4807b-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4807b-755">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="4807b-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4807b-756">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4807b-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4807b-757">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="4807b-757">Cost element</span></span></th>
<th><span data-ttu-id="4807b-758">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="4807b-758">Cost behavior</span></span></th>
<th><span data-ttu-id="4807b-759">Tutar</span><span class="sxs-lookup"><span data-stu-id="4807b-759">Amount</span></span></th>
<th><span data-ttu-id="4807b-760">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="4807b-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4807b-761">CC001</span><span class="sxs-lookup"><span data-stu-id="4807b-761">CC001</span></span></td>
<td><span data-ttu-id="4807b-762">İK</span><span class="sxs-lookup"><span data-stu-id="4807b-762">HR</span></span></td>
<td><span data-ttu-id="4807b-763">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-763">10001</span></span></td>
<td><span data-ttu-id="4807b-764">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-764">Electricity</span></span></td>
<td><span data-ttu-id="4807b-765">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-765">Fixed cost</span></span></td>
<td><span data-ttu-id="4807b-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="4807b-766">-500.00</span></span></td>
<td><span data-ttu-id="4807b-767">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-768">CC002</span><span class="sxs-lookup"><span data-stu-id="4807b-768">CC002</span></span></td>
<td><span data-ttu-id="4807b-769">Finans</span><span class="sxs-lookup"><span data-stu-id="4807b-769">Finance</span></span></td>
<td><span data-ttu-id="4807b-770">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-770">10001</span></span></td>
<td><span data-ttu-id="4807b-771">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-771">Electricity</span></span></td>
<td><span data-ttu-id="4807b-772">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-772">Fixed cost</span></span></td>
<td><span data-ttu-id="4807b-773">175.00</span><span class="sxs-lookup"><span data-stu-id="4807b-773">175.00</span></span></td>
<td><span data-ttu-id="4807b-774">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-775">CC003</span><span class="sxs-lookup"><span data-stu-id="4807b-775">CC003</span></span></td>
<td><span data-ttu-id="4807b-776">Montaj</span><span class="sxs-lookup"><span data-stu-id="4807b-776">Assembly</span></span></td>
<td><span data-ttu-id="4807b-777">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-777">10001</span></span></td>
<td><span data-ttu-id="4807b-778">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-778">Electricity</span></span></td>
<td><span data-ttu-id="4807b-779">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-779">Fixed cost</span></span></td>
<td><span data-ttu-id="4807b-780">275.00</span><span class="sxs-lookup"><span data-stu-id="4807b-780">275.00</span></span></td>
<td><span data-ttu-id="4807b-781">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-782">CC004</span><span class="sxs-lookup"><span data-stu-id="4807b-782">CC004</span></span></td>
<td><span data-ttu-id="4807b-783">Paketleme</span><span class="sxs-lookup"><span data-stu-id="4807b-783">Packaging</span></span></td>
<td><span data-ttu-id="4807b-784">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-784">10001</span></span></td>
<td><span data-ttu-id="4807b-785">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-785">Electricity</span></span></td>
<td><span data-ttu-id="4807b-786">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-786">Fixed cost</span></span></td>
<td><span data-ttu-id="4807b-787">50,00</span><span class="sxs-lookup"><span data-stu-id="4807b-787">50,00</span></span></td>
<td><span data-ttu-id="4807b-788">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-789">CC001</span><span class="sxs-lookup"><span data-stu-id="4807b-789">CC001</span></span></td>
<td><span data-ttu-id="4807b-790">İK</span><span class="sxs-lookup"><span data-stu-id="4807b-790">HR</span></span></td>
<td><span data-ttu-id="4807b-791">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-791">10001</span></span></td>
<td><span data-ttu-id="4807b-792">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-792">Electricity</span></span></td>
<td><span data-ttu-id="4807b-793">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-793">Variable cost</span></span></td>
<td><span data-ttu-id="4807b-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="4807b-794">-1,245.71</span></span></td>
<td><span data-ttu-id="4807b-795">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-796">CC002</span><span class="sxs-lookup"><span data-stu-id="4807b-796">CC002</span></span></td>
<td><span data-ttu-id="4807b-797">Finans</span><span class="sxs-lookup"><span data-stu-id="4807b-797">Finance</span></span></td>
<td><span data-ttu-id="4807b-798">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-798">10001</span></span></td>
<td><span data-ttu-id="4807b-799">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-799">Electricity</span></span></td>
<td><span data-ttu-id="4807b-800">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-800">Variable cost</span></span></td>
<td><span data-ttu-id="4807b-801">436.00</span><span class="sxs-lookup"><span data-stu-id="4807b-801">436.00</span></span></td>
<td><span data-ttu-id="4807b-802">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-803">CC003</span><span class="sxs-lookup"><span data-stu-id="4807b-803">CC003</span></span></td>
<td><span data-ttu-id="4807b-804">Montaj</span><span class="sxs-lookup"><span data-stu-id="4807b-804">Assembly</span></span></td>
<td><span data-ttu-id="4807b-805">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-805">10001</span></span></td>
<td><span data-ttu-id="4807b-806">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-806">Electricity</span></span></td>
<td><span data-ttu-id="4807b-807">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-807">Variable cost</span></span></td>
<td><span data-ttu-id="4807b-808">685.14</span><span class="sxs-lookup"><span data-stu-id="4807b-808">685.14</span></span></td>
<td><span data-ttu-id="4807b-809">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-810">CC004</span><span class="sxs-lookup"><span data-stu-id="4807b-810">CC004</span></span></td>
<td><span data-ttu-id="4807b-811">Paketleme</span><span class="sxs-lookup"><span data-stu-id="4807b-811">Packaging</span></span></td>
<td><span data-ttu-id="4807b-812">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-812">10001</span></span></td>
<td><span data-ttu-id="4807b-813">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-813">Electricity</span></span></td>
<td><span data-ttu-id="4807b-814">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-814">Variable cost</span></span></td>
<td><span data-ttu-id="4807b-815">124.57</span><span class="sxs-lookup"><span data-stu-id="4807b-815">124.57</span></span></td>
<td><span data-ttu-id="4807b-816">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-817">CC002</span><span class="sxs-lookup"><span data-stu-id="4807b-817">CC002</span></span></td>
<td><span data-ttu-id="4807b-818">Finans</span><span class="sxs-lookup"><span data-stu-id="4807b-818">Finance</span></span></td>
<td><span data-ttu-id="4807b-819">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-819">10001</span></span></td>
<td><span data-ttu-id="4807b-820">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-820">Electricity</span></span></td>
<td><span data-ttu-id="4807b-821">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-821">Fixed cost</span></span></td>
<td><span data-ttu-id="4807b-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="4807b-822">-675.00</span></span></td>
<td><span data-ttu-id="4807b-823">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-824">CC003</span><span class="sxs-lookup"><span data-stu-id="4807b-824">CC003</span></span></td>
<td><span data-ttu-id="4807b-825">Montaj</span><span class="sxs-lookup"><span data-stu-id="4807b-825">Assembly</span></span></td>
<td><span data-ttu-id="4807b-826">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-826">10001</span></span></td>
<td><span data-ttu-id="4807b-827">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-827">Electricity</span></span></td>
<td><span data-ttu-id="4807b-828">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-828">Fixed cost</span></span></td>
<td><span data-ttu-id="4807b-829">438.75</span><span class="sxs-lookup"><span data-stu-id="4807b-829">438.75</span></span></td>
<td><span data-ttu-id="4807b-830">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-831">CC004</span><span class="sxs-lookup"><span data-stu-id="4807b-831">CC004</span></span></td>
<td><span data-ttu-id="4807b-832">Paketleme</span><span class="sxs-lookup"><span data-stu-id="4807b-832">Packaging</span></span></td>
<td><span data-ttu-id="4807b-833">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-833">10001</span></span></td>
<td><span data-ttu-id="4807b-834">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-834">Electricity</span></span></td>
<td><span data-ttu-id="4807b-835">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-835">Fixed cost</span></span></td>
<td><span data-ttu-id="4807b-836">236.25</span><span class="sxs-lookup"><span data-stu-id="4807b-836">236.25</span></span></td>
<td><span data-ttu-id="4807b-837">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-838">CC002</span><span class="sxs-lookup"><span data-stu-id="4807b-838">CC002</span></span></td>
<td><span data-ttu-id="4807b-839">Finans</span><span class="sxs-lookup"><span data-stu-id="4807b-839">Finance</span></span></td>
<td><span data-ttu-id="4807b-840">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-840">10001</span></span></td>
<td><span data-ttu-id="4807b-841">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-841">Electricity</span></span></td>
<td><span data-ttu-id="4807b-842">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-842">Variable cost</span></span></td>
<td><span data-ttu-id="4807b-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="4807b-843">-8,150.29</span></span></td>
<td><span data-ttu-id="4807b-844">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-845">CC003</span><span class="sxs-lookup"><span data-stu-id="4807b-845">CC003</span></span></td>
<td><span data-ttu-id="4807b-846">Montaj</span><span class="sxs-lookup"><span data-stu-id="4807b-846">Assembly</span></span></td>
<td><span data-ttu-id="4807b-847">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-847">10001</span></span></td>
<td><span data-ttu-id="4807b-848">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-848">Electricity</span></span></td>
<td><span data-ttu-id="4807b-849">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-849">Variable cost</span></span></td>
<td><span data-ttu-id="4807b-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="4807b-850">5,297.69</span></span></td>
<td><span data-ttu-id="4807b-851">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-852">CC004</span><span class="sxs-lookup"><span data-stu-id="4807b-852">CC004</span></span></td>
<td><span data-ttu-id="4807b-853">Paketleme</span><span class="sxs-lookup"><span data-stu-id="4807b-853">Packaging</span></span></td>
<td><span data-ttu-id="4807b-854">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-854">10001</span></span></td>
<td><span data-ttu-id="4807b-855">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-855">Electricity</span></span></td>
<td><span data-ttu-id="4807b-856">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-856">Variable cost</span></span></td>
<td><span data-ttu-id="4807b-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="4807b-857">2,852.60</span></span></td>
<td><span data-ttu-id="4807b-858">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-859">CC003</span><span class="sxs-lookup"><span data-stu-id="4807b-859">CC003</span></span></td>
<td><span data-ttu-id="4807b-860">Montaj</span><span class="sxs-lookup"><span data-stu-id="4807b-860">Assembly</span></span></td>
<td><span data-ttu-id="4807b-861">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-861">10001</span></span></td>
<td><span data-ttu-id="4807b-862">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-862">Electricity</span></span></td>
<td><span data-ttu-id="4807b-863">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-863">Fixed cost</span></span></td>
<td><span data-ttu-id="4807b-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="4807b-864">-713.75</span></span></td>
<td><span data-ttu-id="4807b-865">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4807b-866">Prod 1</span></span></td>
<td><span data-ttu-id="4807b-867">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="4807b-867">Product 1</span></span></td>
<td><span data-ttu-id="4807b-868">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-868">10001</span></span></td>
<td><span data-ttu-id="4807b-869">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-869">Electricity</span></span></td>
<td><span data-ttu-id="4807b-870">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-870">Fixed cost</span></span></td>
<td><span data-ttu-id="4807b-871">535.31</span><span class="sxs-lookup"><span data-stu-id="4807b-871">535.31</span></span></td>
<td><span data-ttu-id="4807b-872">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4807b-873">Prod 2</span></span></td>
<td><span data-ttu-id="4807b-874">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="4807b-874">Product 2</span></span></td>
<td><span data-ttu-id="4807b-875">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-875">10001</span></span></td>
<td><span data-ttu-id="4807b-876">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-876">Electricity</span></span></td>
<td><span data-ttu-id="4807b-877">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-877">Fixed cost</span></span></td>
<td><span data-ttu-id="4807b-878">178.44</span><span class="sxs-lookup"><span data-stu-id="4807b-878">178.44</span></span></td>
<td><span data-ttu-id="4807b-879">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-880">CC003</span><span class="sxs-lookup"><span data-stu-id="4807b-880">CC003</span></span></td>
<td><span data-ttu-id="4807b-881">Montaj</span><span class="sxs-lookup"><span data-stu-id="4807b-881">Assembly</span></span></td>
<td><span data-ttu-id="4807b-882">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-882">10001</span></span></td>
<td><span data-ttu-id="4807b-883">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-883">Electricity</span></span></td>
<td><span data-ttu-id="4807b-884">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-884">Variable cost</span></span></td>
<td><span data-ttu-id="4807b-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="4807b-885">-5,982.83</span></span></td>
<td><span data-ttu-id="4807b-886">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4807b-887">Prod 1</span></span></td>
<td><span data-ttu-id="4807b-888">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="4807b-888">Product 1</span></span></td>
<td><span data-ttu-id="4807b-889">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-889">10001</span></span></td>
<td><span data-ttu-id="4807b-890">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-890">Electricity</span></span></td>
<td><span data-ttu-id="4807b-891">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-891">Variable cost</span></span></td>
<td><span data-ttu-id="4807b-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="4807b-892">4,487.12</span></span></td>
<td><span data-ttu-id="4807b-893">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4807b-894">Prod 2</span></span></td>
<td><span data-ttu-id="4807b-895">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="4807b-895">Product 2</span></span></td>
<td><span data-ttu-id="4807b-896">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-896">10001</span></span></td>
<td><span data-ttu-id="4807b-897">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-897">Electricity</span></span></td>
<td><span data-ttu-id="4807b-898">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-898">Variable cost</span></span></td>
<td><span data-ttu-id="4807b-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="4807b-899">1,495.71</span></span></td>
<td><span data-ttu-id="4807b-900">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-901">CC003</span><span class="sxs-lookup"><span data-stu-id="4807b-901">CC003</span></span></td>
<td><span data-ttu-id="4807b-902">Montaj</span><span class="sxs-lookup"><span data-stu-id="4807b-902">Assembly</span></span></td>
<td><span data-ttu-id="4807b-903">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-903">10001</span></span></td>
<td><span data-ttu-id="4807b-904">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-904">Electricity</span></span></td>
<td><span data-ttu-id="4807b-905">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-905">Fixed cost</span></span></td>
<td><span data-ttu-id="4807b-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="4807b-906">-286.25</span></span></td>
<td><span data-ttu-id="4807b-907">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4807b-908">Prod 1</span></span></td>
<td><span data-ttu-id="4807b-909">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="4807b-909">Product 1</span></span></td>
<td><span data-ttu-id="4807b-910">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-910">10001</span></span></td>
<td><span data-ttu-id="4807b-911">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-911">Electricity</span></span></td>
<td><span data-ttu-id="4807b-912">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-912">Fixed cost</span></span></td>
<td><span data-ttu-id="4807b-913">241.05</span><span class="sxs-lookup"><span data-stu-id="4807b-913">241.05</span></span></td>
<td><span data-ttu-id="4807b-914">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4807b-915">Prod 2</span></span></td>
<td><span data-ttu-id="4807b-916">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="4807b-916">Product 2</span></span></td>
<td><span data-ttu-id="4807b-917">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-917">10001</span></span></td>
<td><span data-ttu-id="4807b-918">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-918">Electricity</span></span></td>
<td><span data-ttu-id="4807b-919">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-919">Fixed cost</span></span></td>
<td><span data-ttu-id="4807b-920">45.20</span><span class="sxs-lookup"><span data-stu-id="4807b-920">45.20</span></span></td>
<td><span data-ttu-id="4807b-921">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-922">CC003</span><span class="sxs-lookup"><span data-stu-id="4807b-922">CC003</span></span></td>
<td><span data-ttu-id="4807b-923">Montaj</span><span class="sxs-lookup"><span data-stu-id="4807b-923">Assembly</span></span></td>
<td><span data-ttu-id="4807b-924">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-924">10001</span></span></td>
<td><span data-ttu-id="4807b-925">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-925">Electricity</span></span></td>
<td><span data-ttu-id="4807b-926">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-926">Variable cost</span></span></td>
<td><span data-ttu-id="4807b-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="4807b-927">-2,977.17</span></span></td>
<td><span data-ttu-id="4807b-928">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4807b-929">Prod 1</span></span></td>
<td><span data-ttu-id="4807b-930">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="4807b-930">Product 1</span></span></td>
<td><span data-ttu-id="4807b-931">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-931">10001</span></span></td>
<td><span data-ttu-id="4807b-932">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-932">Electricity</span></span></td>
<td><span data-ttu-id="4807b-933">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-933">Variable cost</span></span></td>
<td><span data-ttu-id="4807b-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="4807b-934">2,507.09</span></span></td>
<td><span data-ttu-id="4807b-935">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4807b-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4807b-936">Prod 2</span></span></td>
<td><span data-ttu-id="4807b-937">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="4807b-937">Product 2</span></span></td>
<td><span data-ttu-id="4807b-938">10001</span><span class="sxs-lookup"><span data-stu-id="4807b-938">10001</span></span></td>
<td><span data-ttu-id="4807b-939">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-939">Electricity</span></span></td>
<td><span data-ttu-id="4807b-940">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-940">Variable cost</span></span></td>
<td><span data-ttu-id="4807b-941">470.08</span><span class="sxs-lookup"><span data-stu-id="4807b-941">470.08</span></span></td>
<td><span data-ttu-id="4807b-942">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4807b-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="4807b-943">Sonuç</span><span class="sxs-lookup"><span data-stu-id="4807b-943">Conclusion</span></span>
<span data-ttu-id="4807b-944">Mali muhasebede, Elektrik için 10.000,00 maliyet bir sözde maliyet merkezi kimliğine nakledilmiştir.</span><span class="sxs-lookup"><span data-stu-id="4807b-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="4807b-945">Bu nedenle, maliyet muhasebecileri bu maliyetin tahsis edilmesi gerektiğini bilirler.</span><span class="sxs-lookup"><span data-stu-id="4807b-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="4807b-946">Maliyet muhasebesinde, maliyetler kuruluş birimleri ve seviyeleri arasında, uygulanan kural ve ilkelere dayalı olarak akar.</span><span class="sxs-lookup"><span data-stu-id="4807b-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="4807b-947">Her maliyet, maliyetlerin tahsisatı için en iyi değerlendirmeyi sağlayan bir tahsisat tabanı ile ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="4807b-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="4807b-948">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="4807b-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="4807b-949">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4807b-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="4807b-950">Toplam</span><span class="sxs-lookup"><span data-stu-id="4807b-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="4807b-951">CC099</span><span class="sxs-lookup"><span data-stu-id="4807b-951">CC099</span></span></th>
<th><span data-ttu-id="4807b-952">CC001</span><span class="sxs-lookup"><span data-stu-id="4807b-952">CC001</span></span></th>
<th><span data-ttu-id="4807b-953">CC002</span><span class="sxs-lookup"><span data-stu-id="4807b-953">CC002</span></span></th>
<th><span data-ttu-id="4807b-954">CC003</span><span class="sxs-lookup"><span data-stu-id="4807b-954">CC003</span></span></th>
<th><span data-ttu-id="4807b-955">CC004</span><span class="sxs-lookup"><span data-stu-id="4807b-955">CC004</span></span></th>
<th><span data-ttu-id="4807b-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="4807b-956">Proj 1</span></span></th>
<th><span data-ttu-id="4807b-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="4807b-957">Proj 2</span></span></th>
<th><span data-ttu-id="4807b-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4807b-958">Prod 1</span></span></th>
<th><span data-ttu-id="4807b-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4807b-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="4807b-960">10001 Elektrik</span><span class="sxs-lookup"><span data-stu-id="4807b-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4807b-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="4807b-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4807b-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="4807b-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4807b-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="4807b-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4807b-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="4807b-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="4807b-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="4807b-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4807b-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="4807b-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4807b-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="4807b-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4807b-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="4807b-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4807b-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="4807b-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="4807b-970">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="4807b-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4807b-971">0,00</span><span class="sxs-lookup"><span data-stu-id="4807b-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="4807b-972">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4807b-973">0,00</span><span class="sxs-lookup"><span data-stu-id="4807b-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4807b-974">0,00</span><span class="sxs-lookup"><span data-stu-id="4807b-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4807b-975">0,00</span><span class="sxs-lookup"><span data-stu-id="4807b-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4807b-976">0,00</span><span class="sxs-lookup"><span data-stu-id="4807b-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4807b-977">0,00</span><span class="sxs-lookup"><span data-stu-id="4807b-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="4807b-978">776.36</span><span class="sxs-lookup"><span data-stu-id="4807b-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4807b-979">223.64</span><span class="sxs-lookup"><span data-stu-id="4807b-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4807b-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="4807b-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="4807b-981">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4807b-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4807b-982">000</span><span class="sxs-lookup"><span data-stu-id="4807b-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4807b-983">0,00</span><span class="sxs-lookup"><span data-stu-id="4807b-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4807b-984">0,00</span><span class="sxs-lookup"><span data-stu-id="4807b-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4807b-985">0,00</span><span class="sxs-lookup"><span data-stu-id="4807b-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4807b-986">0,00</span><span class="sxs-lookup"><span data-stu-id="4807b-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4807b-987">30.00</span><span class="sxs-lookup"><span data-stu-id="4807b-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4807b-988">10,00</span><span class="sxs-lookup"><span data-stu-id="4807b-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4807b-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="4807b-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4807b-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="4807b-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4807b-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="4807b-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="4807b-992">Bu konu, birincil maliyet öğesi, 10001 Elektrik'in maliyet nesneleri arasında nasıl aktığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4807b-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="4807b-993">Bu nedenle, bu genel gider maliyeti kuruluşun en düşük seviyesine tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="4807b-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="4807b-994">Başka bir deyişle, maliyet en alt düzeydeki maliyet nesnelerine aittir.</span><span class="sxs-lookup"><span data-stu-id="4807b-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="4807b-995">Maliyetin, maliyet nesneleri arasında görsel bir akışına ihtiyacınız varsa, maliyetin akışını görselleştirmek için maliyet toplamı ilke kurallarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4807b-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="4807b-996">Daha fazla bilgi için bkz. [Maliyet yuvarlama ilkesi ve genel gider hesaplaması](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="4807b-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]