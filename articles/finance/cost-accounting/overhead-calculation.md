---
title: Genel gider hesaplaması
description: Bu konu, genel gider maliyetlerinin hesaplanması için tipik işlemleri açıklar.
author: AndersGirke
manager: AnnBe
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation, CAMOverheadRateCalculationJournalEntry, CAMFormulaAllocationBase
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 923e6e38a664e17ec3349d839c4b77ec903c5dc2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448924"
---
# <a name="overhead-calculation"></a><span data-ttu-id="34c61-103">Genel gider hesaplaması</span><span class="sxs-lookup"><span data-stu-id="34c61-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="34c61-104">Bu konu, genel gider maliyetlerinin hesaplanması için tipik işlemleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="34c61-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="34c61-105">Terim tanımı</span><span class="sxs-lookup"><span data-stu-id="34c61-105">Term definition</span></span>
---------------

<span data-ttu-id="34c61-106">Genel gider maliyetleri bir işletmenin çalışması için normalde uygulanan, ancak doğrudan herhangi bir özel iş, faaliyet, ürün veya hizmete ilişkilendirilmemiş olan maliyetlerdir.</span><span class="sxs-lookup"><span data-stu-id="34c61-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="34c61-107">Genel gider maliyetleri kar sağlama faaliyetlerinin oluşturulması için kritik destek sağlar.</span><span class="sxs-lookup"><span data-stu-id="34c61-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="34c61-108">Aşağıda bazı genel gider örnekleri verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="34c61-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="34c61-109">Kira</span><span class="sxs-lookup"><span data-stu-id="34c61-109">Rent</span></span>
-   <span data-ttu-id="34c61-110">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-110">Electricity</span></span>
-   <span data-ttu-id="34c61-111">Yönetim maaşları</span><span class="sxs-lookup"><span data-stu-id="34c61-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="34c61-112">Genel gider hesaplaması genel bakış</span><span class="sxs-lookup"><span data-stu-id="34c61-112">Overhead calculation overview</span></span>
<span data-ttu-id="34c61-113">Genel gider hesaplama, maliyet muhasebesi ilkelerini doğru sırayla çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="34c61-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="34c61-114">Maliyet muhasebesi ilkeleri değiştiyse veya belirli hatalar algılandıysa, genel gider hesaplamasını aynı mali dönem için birden fazla kez yürütebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34c61-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="34c61-115">Her genel gider hesaplaması depolanır ve önceki sürümlerdeki hesaplamaları kıyaslamanıza olanak sağlayan, benzersiz bir sürüm kimliğine sahip olur.</span><span class="sxs-lookup"><span data-stu-id="34c61-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="34c61-116">Genel gider hesaplamasının oluşturduğu maliyet girişleri bir muhasebe tarihi alır.</span><span class="sxs-lookup"><span data-stu-id="34c61-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="34c61-117">Bu muhasebe tarihi, hesaplamada kullanılan mali dönemin bitiş tarihiyle eşleşir.</span><span class="sxs-lookup"><span data-stu-id="34c61-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="34c61-118">Benzersiz sürüm kimliği aşağıdaki öğelerden oluşur:</span><span class="sxs-lookup"><span data-stu-id="34c61-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="34c61-119">Sürüm türü</span><span class="sxs-lookup"><span data-stu-id="34c61-119">Version type</span></span>
-   <span data-ttu-id="34c61-120">Tarih ve saat</span><span class="sxs-lookup"><span data-stu-id="34c61-120">Date and time</span></span>
-   <span data-ttu-id="34c61-121">Maliyet muhasebesi defteri</span><span class="sxs-lookup"><span data-stu-id="34c61-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="34c61-122">Mali yıl</span><span class="sxs-lookup"><span data-stu-id="34c61-122">Fiscal year</span></span>
-   <span data-ttu-id="34c61-123">Mali dönem</span><span class="sxs-lookup"><span data-stu-id="34c61-123">Fiscal period</span></span>

<span data-ttu-id="34c61-124">Genel gider hesaplama, sürümden bağımsız olarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="34c61-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="34c61-125">Bu nedenle, Gerçek sürümden önce Bütçe sürümünü hesaplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34c61-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="34c61-126">Genel gider hesaplama dört adımdan oluşur, aşağıdaki çizimde gösterildiği gibi.</span><span class="sxs-lookup"><span data-stu-id="34c61-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="34c61-127">Her adımda, günlük girişleri olan bir günlük başlığı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="34c61-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="34c61-128">Bu günlük başlığı, her hesaplama adımı için giriş verilerini tutar.</span><span class="sxs-lookup"><span data-stu-id="34c61-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="34c61-129">İlkeler ve kurallar her günlük satırına uygulanır ve maliyet girişleri çıkış olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="34c61-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="34c61-130">Bu nedenle, her zaman tam izlenebilirliğe sahip olursunuz.</span><span class="sxs-lookup"><span data-stu-id="34c61-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="34c61-131">[![Genel gider hesaplaması](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="34c61-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="34c61-132">Elektrik genel gideri maliyetini hesapla ve tahsis et</span><span class="sxs-lookup"><span data-stu-id="34c61-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="34c61-133">Mali muhasebede, elektrik gibi bazı maliyetler peşin ödeme olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="34c61-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="34c61-134">Bu nedenle, Maliyet muhasebesi için ayrıntılı yönetim bilgiler sağlanmaz.</span><span class="sxs-lookup"><span data-stu-id="34c61-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="34c61-135">Maliyet muhasebesinde doğru yönetimsel bilgileri tüm yönetim birim ve düzeylerinde sağlamak için, maliyetlerin kuruluş birimleri arasında akması gerekir.</span><span class="sxs-lookup"><span data-stu-id="34c61-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="34c61-136">Bu akış, tüketimin doğru bir kaydına ya da adil bir değerlendirmeye dayanıyor olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="34c61-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="34c61-137">Genel muhasebede, bir elektrik maliyeti aşağıdaki tabloda gösterildiği gibi deftere nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="34c61-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="34c61-138">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="34c61-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="34c61-139">Maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="34c61-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="34c61-140">Ana hesap</span><span class="sxs-lookup"><span data-stu-id="34c61-140">Main account</span></span></th>
<th><span data-ttu-id="34c61-141">Muhasebe para birimi cinsinden tutar</span><span class="sxs-lookup"><span data-stu-id="34c61-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="34c61-142">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="34c61-143">CC099</span><span class="sxs-lookup"><span data-stu-id="34c61-143">CC099</span></span></td>
<td><span data-ttu-id="34c61-144">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="34c61-144">Default cost center</span></span></td>
<td><span data-ttu-id="34c61-145">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-145">10001</span></span></td>
<td><span data-ttu-id="34c61-146">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-146">Electricity</span></span></td>
<td><span data-ttu-id="34c61-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="34c61-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="34c61-148">Adım 1: Maliyet davranışı hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="34c61-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="34c61-149">Varsayılan olarak, maliyeti girişleri kaynak veriden içeri alındığında, Maliyet muhasebesinde **Sınıflandırılmamış** maliyet davranışı sınıflandırmasını alırlar.</span><span class="sxs-lookup"><span data-stu-id="34c61-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="34c61-150">Maliyet davranışı ilke kuralları ekleyerek, maliyet girişlerini **Sabit maliyet** veya **Değişken maliyet** olarak yeniden sınıflandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34c61-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="34c61-151">Maliyet davranış kuralını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="34c61-151">Define the cost behavior rule</span></span>

<span data-ttu-id="34c61-152">Bazı durumlarda, sabit bir ücret maliyet parçasıdır ve kalan maliyet, tüketime dayanır.</span><span class="sxs-lookup"><span data-stu-id="34c61-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="34c61-153">Elektrik faturaları genellikle bu tanıma uyar.</span><span class="sxs-lookup"><span data-stu-id="34c61-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="34c61-154">Belirli bir sabit ücret ödedikten sonra, kilovat saatlik (Kwh) tüketim başına ödeme yaparsınız.</span><span class="sxs-lookup"><span data-stu-id="34c61-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="34c61-155">Örneğin, sabit maliyet masrafı 1.000,00 ise, maliyet davranışı kural nasıl tanımlanır:</span><span class="sxs-lookup"><span data-stu-id="34c61-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="34c61-156">Sabit tutar 1.000,00</span><span class="sxs-lookup"><span data-stu-id="34c61-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="34c61-157">0 &lt;= 1.000,00 = Sabit</span><span class="sxs-lookup"><span data-stu-id="34c61-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="34c61-158">1000,01 &lt; N = Değişken</span><span class="sxs-lookup"><span data-stu-id="34c61-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="34c61-159">Günlük</span><span class="sxs-lookup"><span data-stu-id="34c61-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="34c61-160">Günlük</span><span class="sxs-lookup"><span data-stu-id="34c61-160">Journal</span></span></th>
<th><span data-ttu-id="34c61-161">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="34c61-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="34c61-162">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="34c61-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="34c61-163">Sürüm</span><span class="sxs-lookup"><span data-stu-id="34c61-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="34c61-164">00001</span><span class="sxs-lookup"><span data-stu-id="34c61-164">00001</span></span></td>
<td><span data-ttu-id="34c61-165">Maliyet davranışı hesaplama günlüğü</span><span class="sxs-lookup"><span data-stu-id="34c61-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="34c61-166">Mali</span><span class="sxs-lookup"><span data-stu-id="34c61-166">Fiscal</span></span></td>
<td><span data-ttu-id="34c61-167">2017</span><span class="sxs-lookup"><span data-stu-id="34c61-167">2017</span></span></td>
<td><span data-ttu-id="34c61-168">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="34c61-168">Period 1</span></span></td>
<td><span data-ttu-id="34c61-169">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="34c61-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="34c61-170">Günlük girişleri (Maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="34c61-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="34c61-171">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="34c61-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="34c61-172">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="34c61-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="34c61-173">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="34c61-173">Cost element</span></span></th>
<th><span data-ttu-id="34c61-174">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="34c61-174">Cost behavior</span></span></th>
<th><span data-ttu-id="34c61-175">Tutar</span><span class="sxs-lookup"><span data-stu-id="34c61-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="34c61-176">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="34c61-177">CC099</span><span class="sxs-lookup"><span data-stu-id="34c61-177">CC099</span></span></td>
<td><span data-ttu-id="34c61-178">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="34c61-178">Default cost center</span></span></td>
<td><span data-ttu-id="34c61-179">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-179">10001</span></span></td>
<td><span data-ttu-id="34c61-180">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-180">Electricity</span></span></td>
<td><span data-ttu-id="34c61-181">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="34c61-181">Unclassified</span></span></td>
<td><span data-ttu-id="34c61-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="34c61-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="34c61-183">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="34c61-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="34c61-184">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="34c61-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="34c61-185">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="34c61-185">Cost element</span></span></th>
<th><span data-ttu-id="34c61-186">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="34c61-186">Cost behavior</span></span></th>
<th><span data-ttu-id="34c61-187">Tutar</span><span class="sxs-lookup"><span data-stu-id="34c61-187">Amount</span></span></th>
<th><span data-ttu-id="34c61-188">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="34c61-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="34c61-189">CC099</span><span class="sxs-lookup"><span data-stu-id="34c61-189">CC099</span></span></td>
<td><span data-ttu-id="34c61-190">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="34c61-190">Default cost center</span></span></td>
<td><span data-ttu-id="34c61-191">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-191">10001</span></span></td>
<td><span data-ttu-id="34c61-192">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-192">Electricity</span></span></td>
<td><span data-ttu-id="34c61-193">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="34c61-193">Unclassified</span></span></td>
<td><span data-ttu-id="34c61-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="34c61-194">10,000.00</span></span></td>
<td><span data-ttu-id="34c61-195">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-196">CC099</span><span class="sxs-lookup"><span data-stu-id="34c61-196">CC099</span></span></td>
<td><span data-ttu-id="34c61-197">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="34c61-197">Default cost center</span></span></td>
<td><span data-ttu-id="34c61-198">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-198">10001</span></span></td>
<td><span data-ttu-id="34c61-199">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-199">Electricity</span></span></td>
<td><span data-ttu-id="34c61-200">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="34c61-200">Unclassified</span></span></td>
<td><span data-ttu-id="34c61-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="34c61-201">-10,000.00</span></span></td>
<td><span data-ttu-id="34c61-202">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-203">CC099</span><span class="sxs-lookup"><span data-stu-id="34c61-203">CC099</span></span></td>
<td><span data-ttu-id="34c61-204">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="34c61-204">Default cost center</span></span></td>
<td><span data-ttu-id="34c61-205">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-205">10001</span></span></td>
<td><span data-ttu-id="34c61-206">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-206">Electricity</span></span></td>
<td><span data-ttu-id="34c61-207">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-207">Fixed cost</span></span></td>
<td><span data-ttu-id="34c61-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="34c61-208">1,000.00</span></span></td>
<td><span data-ttu-id="34c61-209">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-210">CC099</span><span class="sxs-lookup"><span data-stu-id="34c61-210">CC099</span></span></td>
<td><span data-ttu-id="34c61-211">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="34c61-211">Default cost center</span></span></td>
<td><span data-ttu-id="34c61-212">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-212">10001</span></span></td>
<td><span data-ttu-id="34c61-213">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-213">Electricity</span></span></td>
<td><span data-ttu-id="34c61-214">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-214">Variable cost</span></span></td>
<td><span data-ttu-id="34c61-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="34c61-215">9,000.00</span></span></td>
<td><span data-ttu-id="34c61-216">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="34c61-217">Daha fazla bilgi için bkz. [Maliyet davranışı ilkesi oluşturma ve bir maliyet kontrol birimine atama](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="34c61-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="34c61-218">Adım 2: Maliyet dağıtımı hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="34c61-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="34c61-219">Maliyet dağıtımı, bir nesneden bir veya daha fazlasına ilgili tahsisat tabanı uygulayarak maliyeti yeniden dağıtmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="34c61-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="34c61-220">Maliyet dağıtımı ve maliyet tahsisatı, maliyet dağıtımının her zaman orijinal maliyetin birincil maliyet öğesinde bulunmasıyla farklılık gösterir.</span><span class="sxs-lookup"><span data-stu-id="34c61-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="34c61-221">Maliyet dağıtım kuralını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="34c61-221">Define the cost distribution rule</span></span>

<span data-ttu-id="34c61-222">Mali muhasebede, elektrik maliyetleri çoğu zaman peşin ödeme olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="34c61-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="34c61-223">Maliyet muhasebesinde ise bu yöntem yeterince ayrıntılı değildir.</span><span class="sxs-lookup"><span data-stu-id="34c61-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="34c61-224">Değişken maliyet, maliyet nesnelerine tek tek, adil bir temele dayanarak dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="34c61-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="34c61-225">En mantıklı tahsisat, elektrik kullanımını (Kwh) temel alarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="34c61-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="34c61-226">Elektrik adına sahip, istatistiksel bir boyut üyesi oluşturulur ve elektrik tüketimi kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="34c61-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="34c61-227">Varsayıla olarak, tüm istatistiksel boyut üyeleri tahsisat tabanları olarak kullanılabilir hale gelir.</span><span class="sxs-lookup"><span data-stu-id="34c61-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="34c61-228">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="34c61-228">Cost object</span></span></th>
<th><span data-ttu-id="34c61-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="34c61-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="34c61-230">CC001</span><span class="sxs-lookup"><span data-stu-id="34c61-230">CC001</span></span></td>
<td><span data-ttu-id="34c61-231">İK</span><span class="sxs-lookup"><span data-stu-id="34c61-231">HR</span></span></td>
<td><span data-ttu-id="34c61-232">1.000</span><span class="sxs-lookup"><span data-stu-id="34c61-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-233">CC002</span><span class="sxs-lookup"><span data-stu-id="34c61-233">CC002</span></span></td>
<td><span data-ttu-id="34c61-234">Finans</span><span class="sxs-lookup"><span data-stu-id="34c61-234">Finance</span></span></td>
<td><span data-ttu-id="34c61-235">6,000</span><span class="sxs-lookup"><span data-stu-id="34c61-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-236">CC003</span><span class="sxs-lookup"><span data-stu-id="34c61-236">CC003</span></span></td>
<td><span data-ttu-id="34c61-237">Montaj</span><span class="sxs-lookup"><span data-stu-id="34c61-237">Assembly</span></span></td>
<td><span data-ttu-id="34c61-238">0</span><span class="sxs-lookup"><span data-stu-id="34c61-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="34c61-239">Aşağıdaki tablo, elektrik tüketiminin değişken maliyetler için bir tahsisat tabanlı olarak uygulandığındaki sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="34c61-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="34c61-240">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="34c61-240">Cost object</span></span></th>
<th><span data-ttu-id="34c61-241">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="34c61-241">Magnitude</span></span></th>
<th><span data-ttu-id="34c61-242">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="34c61-242">Allocation factor</span></span></th>
<th><span data-ttu-id="34c61-243">Tutar</span><span class="sxs-lookup"><span data-stu-id="34c61-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="34c61-244">CC001</span><span class="sxs-lookup"><span data-stu-id="34c61-244">CC001</span></span></td>
<td><span data-ttu-id="34c61-245">İK</span><span class="sxs-lookup"><span data-stu-id="34c61-245">HR</span></span></td>
<td><span data-ttu-id="34c61-246">1.000</span><span class="sxs-lookup"><span data-stu-id="34c61-246">1,000</span></span></td>
<td><span data-ttu-id="34c61-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="34c61-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="34c61-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="34c61-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-249">CC002</span><span class="sxs-lookup"><span data-stu-id="34c61-249">CC002</span></span></td>
<td><span data-ttu-id="34c61-250">Finans</span><span class="sxs-lookup"><span data-stu-id="34c61-250">Finance</span></span></td>
<td><span data-ttu-id="34c61-251">6,000</span><span class="sxs-lookup"><span data-stu-id="34c61-251">6,000</span></span></td>
<td><span data-ttu-id="34c61-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="34c61-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="34c61-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="34c61-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-254">CC003</span><span class="sxs-lookup"><span data-stu-id="34c61-254">CC003</span></span></td>
<td><span data-ttu-id="34c61-255">Montaj</span><span class="sxs-lookup"><span data-stu-id="34c61-255">Assembly</span></span></td>
<td><span data-ttu-id="34c61-256">0</span><span class="sxs-lookup"><span data-stu-id="34c61-256">0</span></span></td>
<td><span data-ttu-id="34c61-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="34c61-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="34c61-258">0,00</span><span class="sxs-lookup"><span data-stu-id="34c61-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="34c61-259">Sabit maliyet, elektrik tüketmiş olan tekil maliyet nesnelerine eşit miktarda dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="34c61-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="34c61-260">Bu sonuca, Elektrik istatistiksel boyut öğesini bir formül tahsisat tabanında kullanarak ulaşabilirsiniz: (Elektrik &gt; 0,00) Aşağıdaki tablo, elektrik tüketimi değişken maliyetler için bir tahsisat tabanı olarak kullanıldığında ortaya çıkan sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="34c61-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="34c61-261">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="34c61-261">Cost object</span></span></th>
<th><span data-ttu-id="34c61-262">Formül</span><span class="sxs-lookup"><span data-stu-id="34c61-262">Formula</span></span></th>
<th><span data-ttu-id="34c61-263">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="34c61-263">Magnitude</span></span></th>
<th><span data-ttu-id="34c61-264">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="34c61-264">Allocation factor</span></span></th>
<th><span data-ttu-id="34c61-265">Tutar</span><span class="sxs-lookup"><span data-stu-id="34c61-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="34c61-266">CC001</span><span class="sxs-lookup"><span data-stu-id="34c61-266">CC001</span></span></td>
<td><span data-ttu-id="34c61-267">İK</span><span class="sxs-lookup"><span data-stu-id="34c61-267">HR</span></span></td>
<td><span data-ttu-id="34c61-268">(1,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="34c61-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="34c61-269">1</span><span class="sxs-lookup"><span data-stu-id="34c61-269">1</span></span></td>
<td><span data-ttu-id="34c61-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="34c61-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="34c61-271">500.00</span><span class="sxs-lookup"><span data-stu-id="34c61-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-272">CC002</span><span class="sxs-lookup"><span data-stu-id="34c61-272">CC002</span></span></td>
<td><span data-ttu-id="34c61-273">Finans</span><span class="sxs-lookup"><span data-stu-id="34c61-273">Finance</span></span></td>
<td><span data-ttu-id="34c61-274">(6,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="34c61-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="34c61-275">1</span><span class="sxs-lookup"><span data-stu-id="34c61-275">1</span></span></td>
<td><span data-ttu-id="34c61-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="34c61-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="34c61-277">500.00</span><span class="sxs-lookup"><span data-stu-id="34c61-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-278">CC003</span><span class="sxs-lookup"><span data-stu-id="34c61-278">CC003</span></span></td>
<td><span data-ttu-id="34c61-279">Montaj</span><span class="sxs-lookup"><span data-stu-id="34c61-279">Assembly</span></span></td>
<td><span data-ttu-id="34c61-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="34c61-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="34c61-281">0</span><span class="sxs-lookup"><span data-stu-id="34c61-281">0</span></span></td>
<td><span data-ttu-id="34c61-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="34c61-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="34c61-283">0,00</span><span class="sxs-lookup"><span data-stu-id="34c61-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="34c61-284">Günlük</span><span class="sxs-lookup"><span data-stu-id="34c61-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="34c61-285">Günlük</span><span class="sxs-lookup"><span data-stu-id="34c61-285">Journal</span></span></th>
<th><span data-ttu-id="34c61-286">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="34c61-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="34c61-287">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="34c61-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="34c61-288">Sürüm</span><span class="sxs-lookup"><span data-stu-id="34c61-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="34c61-289">00002</span><span class="sxs-lookup"><span data-stu-id="34c61-289">00002</span></span></td>
<td><span data-ttu-id="34c61-290">Maliyet dağıtımı hesaplama günlüğü</span><span class="sxs-lookup"><span data-stu-id="34c61-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="34c61-291">Mali</span><span class="sxs-lookup"><span data-stu-id="34c61-291">Fiscal</span></span></td>
<td><span data-ttu-id="34c61-292">2017</span><span class="sxs-lookup"><span data-stu-id="34c61-292">2017</span></span></td>
<td><span data-ttu-id="34c61-293">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="34c61-293">Period 1</span></span></td>
<td><span data-ttu-id="34c61-294">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="34c61-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="34c61-295">Günlük girişleri (Maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="34c61-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="34c61-296">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="34c61-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="34c61-297">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="34c61-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="34c61-298">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="34c61-298">Cost element</span></span></th>
<th><span data-ttu-id="34c61-299">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="34c61-299">Cost behavior</span></span></th>
<th><span data-ttu-id="34c61-300">Tutar</span><span class="sxs-lookup"><span data-stu-id="34c61-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="34c61-301">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="34c61-302">CC099</span><span class="sxs-lookup"><span data-stu-id="34c61-302">CC099</span></span></td>
<td><span data-ttu-id="34c61-303">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="34c61-303">Default cost center</span></span></td>
<td><span data-ttu-id="34c61-304">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-304">10001</span></span></td>
<td><span data-ttu-id="34c61-305">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-305">Electricity</span></span></td>
<td><span data-ttu-id="34c61-306">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-306">Fixed cost</span></span></td>
<td><span data-ttu-id="34c61-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="34c61-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-308">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="34c61-309">CC099</span><span class="sxs-lookup"><span data-stu-id="34c61-309">CC099</span></span></td>
<td><span data-ttu-id="34c61-310">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="34c61-310">Default cost center</span></span></td>
<td><span data-ttu-id="34c61-311">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-311">10001</span></span></td>
<td><span data-ttu-id="34c61-312">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-312">Electricity</span></span></td>
<td><span data-ttu-id="34c61-313">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-313">Variable cost</span></span></td>
<td><span data-ttu-id="34c61-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="34c61-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="34c61-315">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="34c61-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="34c61-316">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="34c61-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="34c61-317">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="34c61-317">Cost element</span></span></th>
<th><span data-ttu-id="34c61-318">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="34c61-318">Cost behavior</span></span></th>
<th><span data-ttu-id="34c61-319">Tutar</span><span class="sxs-lookup"><span data-stu-id="34c61-319">Amount</span></span></th>
<th><span data-ttu-id="34c61-320">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="34c61-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="34c61-321">CC099</span><span class="sxs-lookup"><span data-stu-id="34c61-321">CC099</span></span></td>
<td><span data-ttu-id="34c61-322">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="34c61-322">Default cost center</span></span></td>
<td><span data-ttu-id="34c61-323">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-323">10001</span></span></td>
<td><span data-ttu-id="34c61-324">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-324">Electricity</span></span></td>
<td><span data-ttu-id="34c61-325">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-325">Fixed cost</span></span></td>
<td><span data-ttu-id="34c61-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="34c61-326">-1,000.00</span></span></td>
<td><span data-ttu-id="34c61-327">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-328">CC001</span><span class="sxs-lookup"><span data-stu-id="34c61-328">CC001</span></span></td>
<td><span data-ttu-id="34c61-329">İK</span><span class="sxs-lookup"><span data-stu-id="34c61-329">HR</span></span></td>
<td><span data-ttu-id="34c61-330">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-330">10001</span></span></td>
<td><span data-ttu-id="34c61-331">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-331">Electricity</span></span></td>
<td><span data-ttu-id="34c61-332">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-332">Fixed cost</span></span></td>
<td><span data-ttu-id="34c61-333">500.00</span><span class="sxs-lookup"><span data-stu-id="34c61-333">500.00</span></span></td>
<td><span data-ttu-id="34c61-334">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-335">CC002</span><span class="sxs-lookup"><span data-stu-id="34c61-335">CC002</span></span></td>
<td><span data-ttu-id="34c61-336">Finans</span><span class="sxs-lookup"><span data-stu-id="34c61-336">Finance</span></span></td>
<td><span data-ttu-id="34c61-337">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-337">10001</span></span></td>
<td><span data-ttu-id="34c61-338">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-338">Electricity</span></span></td>
<td><span data-ttu-id="34c61-339">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-339">Fixed cost</span></span></td>
<td><span data-ttu-id="34c61-340">500.00</span><span class="sxs-lookup"><span data-stu-id="34c61-340">500.00</span></span></td>
<td><span data-ttu-id="34c61-341">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-342">CC099</span><span class="sxs-lookup"><span data-stu-id="34c61-342">CC099</span></span></td>
<td><span data-ttu-id="34c61-343">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="34c61-343">Default cost center</span></span></td>
<td><span data-ttu-id="34c61-344">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-344">10001</span></span></td>
<td><span data-ttu-id="34c61-345">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-345">Electricity</span></span></td>
<td><span data-ttu-id="34c61-346">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-346">Variable cost</span></span></td>
<td><span data-ttu-id="34c61-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="34c61-347">-9,000.00</span></span></td>
<td><span data-ttu-id="34c61-348">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-349">CC001</span><span class="sxs-lookup"><span data-stu-id="34c61-349">CC001</span></span></td>
<td><span data-ttu-id="34c61-350">İK</span><span class="sxs-lookup"><span data-stu-id="34c61-350">HR</span></span></td>
<td><span data-ttu-id="34c61-351">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-351">10001</span></span></td>
<td><span data-ttu-id="34c61-352">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-352">Electricity</span></span></td>
<td><span data-ttu-id="34c61-353">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-353">Variable cost</span></span></td>
<td><span data-ttu-id="34c61-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="34c61-354">1,285.71</span></span></td>
<td><span data-ttu-id="34c61-355">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-356">CC002</span><span class="sxs-lookup"><span data-stu-id="34c61-356">CC002</span></span></td>
<td><span data-ttu-id="34c61-357">Finans</span><span class="sxs-lookup"><span data-stu-id="34c61-357">Finance</span></span></td>
<td><span data-ttu-id="34c61-358">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-358">10001</span></span></td>
<td><span data-ttu-id="34c61-359">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-359">Electricity</span></span></td>
<td><span data-ttu-id="34c61-360">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-360">Variable cost</span></span></td>
<td><span data-ttu-id="34c61-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="34c61-361">7,714.29</span></span></td>
<td><span data-ttu-id="34c61-362">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="34c61-363">Daha fazla bilgi için bkz. [Maliyet dağıtımı ilkesi oluşturma ve bir maliyet kontrol birimine atama](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="34c61-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="34c61-364">Adım 3: Genel gider oranı hesaplama işlemi</span><span class="sxs-lookup"><span data-stu-id="34c61-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="34c61-365">Genel gider oranı, bir veya birden fazla belirli maliyet nesnesine masraf yüklemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="34c61-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="34c61-366">Masraf, önceden belirlenmiş maliyet oranına ve tahsisat tabanından hesaplanan büyüklüğe dayanır.</span><span class="sxs-lookup"><span data-stu-id="34c61-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="34c61-367">Genel gider oranını tanımlama</span><span class="sxs-lookup"><span data-stu-id="34c61-367">Define the overhead rate</span></span>

<span data-ttu-id="34c61-368">Maliyet nesnesi CC001 HR, bir dizi dahili projeye katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="34c61-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="34c61-369">HR projeleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="34c61-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="34c61-370">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="34c61-370">Cost object</span></span></th>
<th><span data-ttu-id="34c61-371">Saatler</span><span class="sxs-lookup"><span data-stu-id="34c61-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="34c61-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="34c61-372">Proj 1</span></span></td>
<td><span data-ttu-id="34c61-373">Proje 1</span><span class="sxs-lookup"><span data-stu-id="34c61-373">Project 1</span></span></td>
<td><span data-ttu-id="34c61-374">3</span><span class="sxs-lookup"><span data-stu-id="34c61-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="34c61-375">Proj 2</span></span></td>
<td><span data-ttu-id="34c61-376">Proje 2</span><span class="sxs-lookup"><span data-stu-id="34c61-376">Project 2</span></span></td>
<td><span data-ttu-id="34c61-377">1</span><span class="sxs-lookup"><span data-stu-id="34c61-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="34c61-378">Maliyet projeleri dağıtımı için bir önceden belirlenmiş maliyet oranı tanımlandı.</span><span class="sxs-lookup"><span data-stu-id="34c61-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="34c61-379">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="34c61-379">Cost object</span></span></th>
<th><span data-ttu-id="34c61-380">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="34c61-380">Cost element</span></span></th>
<th><span data-ttu-id="34c61-381">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="34c61-381">Cost behavior</span></span></th>
<th><span data-ttu-id="34c61-382">Birimler</span><span class="sxs-lookup"><span data-stu-id="34c61-382">Units</span></span></th>
<th><span data-ttu-id="34c61-383">Ücret</span><span class="sxs-lookup"><span data-stu-id="34c61-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="34c61-384">CC001</span><span class="sxs-lookup"><span data-stu-id="34c61-384">CC001</span></span></td>
<td><span data-ttu-id="34c61-385">İK</span><span class="sxs-lookup"><span data-stu-id="34c61-385">HR</span></span></td>
<td><span data-ttu-id="34c61-386">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-386">10001</span></span></td>
<td><span data-ttu-id="34c61-387">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-387">Variable cost</span></span></td>
<td><span data-ttu-id="34c61-388">1</span><span class="sxs-lookup"><span data-stu-id="34c61-388">1</span></span></td>
<td><span data-ttu-id="34c61-389">10</span><span class="sxs-lookup"><span data-stu-id="34c61-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="34c61-390">Aşağıdaki tablo, HR projeleri bir tahsisat tabanı olarak uygulandığındaki sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="34c61-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="34c61-391">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="34c61-391">Cost object</span></span></th>
<th><span data-ttu-id="34c61-392">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="34c61-392">Magnitude</span></span></th>
<th><span data-ttu-id="34c61-393">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="34c61-393">Cost element</span></span></th>
<th><span data-ttu-id="34c61-394">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="34c61-394">Allocation factor</span></span></th>
<th><span data-ttu-id="34c61-395">Tutar</span><span class="sxs-lookup"><span data-stu-id="34c61-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="34c61-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="34c61-396">Proj 1</span></span></td>
<td><span data-ttu-id="34c61-397">Proje 1</span><span class="sxs-lookup"><span data-stu-id="34c61-397">Project 1</span></span></td>
<td><span data-ttu-id="34c61-398">3</span><span class="sxs-lookup"><span data-stu-id="34c61-398">3</span></span></td>
<td><span data-ttu-id="34c61-399">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-399">10001</span></span></td>
<td><span data-ttu-id="34c61-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="34c61-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="34c61-401">30.00</span><span class="sxs-lookup"><span data-stu-id="34c61-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="34c61-402">Proj 2</span></span></td>
<td><span data-ttu-id="34c61-403">Proje 2</span><span class="sxs-lookup"><span data-stu-id="34c61-403">Project 2</span></span></td>
<td><span data-ttu-id="34c61-404">1</span><span class="sxs-lookup"><span data-stu-id="34c61-404">1</span></span></td>
<td><span data-ttu-id="34c61-405">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-405">10001</span></span></td>
<td><span data-ttu-id="34c61-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="34c61-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="34c61-407">10,00</span><span class="sxs-lookup"><span data-stu-id="34c61-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="34c61-408">Günlük</span><span class="sxs-lookup"><span data-stu-id="34c61-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="34c61-409">Günlük</span><span class="sxs-lookup"><span data-stu-id="34c61-409">Journal</span></span></th>
<th><span data-ttu-id="34c61-410">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="34c61-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="34c61-411">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="34c61-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="34c61-412">Sürüm</span><span class="sxs-lookup"><span data-stu-id="34c61-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="34c61-413">00003</span><span class="sxs-lookup"><span data-stu-id="34c61-413">00003</span></span></td>
<td><span data-ttu-id="34c61-414">Genel gider oranı hesaplaması günlüğü</span><span class="sxs-lookup"><span data-stu-id="34c61-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="34c61-415">Mali</span><span class="sxs-lookup"><span data-stu-id="34c61-415">Fiscal</span></span></td>
<td><span data-ttu-id="34c61-416">2017</span><span class="sxs-lookup"><span data-stu-id="34c61-416">2017</span></span></td>
<td><span data-ttu-id="34c61-417">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="34c61-417">Period 1</span></span></td>
<td><span data-ttu-id="34c61-418">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="34c61-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="34c61-419">Günlük girişleri (Genel gider oranı hesaplaması için günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="34c61-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="34c61-420">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="34c61-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="34c61-421">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="34c61-421">Cost object</span></span></th>
<th><span data-ttu-id="34c61-422">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="34c61-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="34c61-423">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="34c61-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="34c61-424">Proj 1</span></span></td>
<td><span data-ttu-id="34c61-425">Dahili Proj 1</span><span class="sxs-lookup"><span data-stu-id="34c61-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="34c61-426">3,00</span><span class="sxs-lookup"><span data-stu-id="34c61-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-427">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="34c61-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="34c61-428">Proj 2</span></span></td>
<td><span data-ttu-id="34c61-429">Dahili Proj 2</span><span class="sxs-lookup"><span data-stu-id="34c61-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="34c61-430">1.00</span><span class="sxs-lookup"><span data-stu-id="34c61-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="34c61-431">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="34c61-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="34c61-432">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="34c61-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="34c61-433">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="34c61-433">Cost element</span></span></th>
<th><span data-ttu-id="34c61-434">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="34c61-434">Cost behavior</span></span></th>
<th><span data-ttu-id="34c61-435">Tutar</span><span class="sxs-lookup"><span data-stu-id="34c61-435">Amount</span></span></th>
<th><span data-ttu-id="34c61-436">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="34c61-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="34c61-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="34c61-437">CC0001</span></span></td>
<td><span data-ttu-id="34c61-438">İK</span><span class="sxs-lookup"><span data-stu-id="34c61-438">HR</span></span></td>
<td><span data-ttu-id="34c61-439">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-439">10001</span></span></td>
<td><span data-ttu-id="34c61-440">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-440">Electricity</span></span></td>
<td><span data-ttu-id="34c61-441">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-441">Variable cost</span></span></td>
<td><span data-ttu-id="34c61-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="34c61-442">-30.00</span></span></td>
<td><span data-ttu-id="34c61-443">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="34c61-444">Proj 1</span></span></td>
<td><span data-ttu-id="34c61-445">Dahili Proj 1</span><span class="sxs-lookup"><span data-stu-id="34c61-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="34c61-446">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-446">10001</span></span></td>
<td><span data-ttu-id="34c61-447">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-447">Electricity</span></span></td>
<td><span data-ttu-id="34c61-448">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-448">Variable cost</span></span></td>
<td><span data-ttu-id="34c61-449">30.00</span><span class="sxs-lookup"><span data-stu-id="34c61-449">30.00</span></span></td>
<td><span data-ttu-id="34c61-450">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-451">CC001</span><span class="sxs-lookup"><span data-stu-id="34c61-451">CC001</span></span></td>
<td><span data-ttu-id="34c61-452">İK</span><span class="sxs-lookup"><span data-stu-id="34c61-452">HR</span></span></td>
<td><span data-ttu-id="34c61-453">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-453">10001</span></span></td>
<td><span data-ttu-id="34c61-454">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-454">Electricity</span></span></td>
<td><span data-ttu-id="34c61-455">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-455">Variable cost</span></span></td>
<td><span data-ttu-id="34c61-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="34c61-456">-10.00</span></span></td>
<td><span data-ttu-id="34c61-457">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="34c61-458">Proj 2</span></span></td>
<td><span data-ttu-id="34c61-459">Dahili Proj 2</span><span class="sxs-lookup"><span data-stu-id="34c61-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="34c61-460">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-460">10001</span></span></td>
<td><span data-ttu-id="34c61-461">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-461">Electricity</span></span></td>
<td><span data-ttu-id="34c61-462">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-462">Variable cost</span></span></td>
<td><span data-ttu-id="34c61-463">10,00</span><span class="sxs-lookup"><span data-stu-id="34c61-463">10.00</span></span></td>
<td><span data-ttu-id="34c61-464">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="34c61-465">Daha fazla bilgi için [Genel gider hesaplaması gerçekleştir](cost-rollup.md#perform-overhead-calculation) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="34c61-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="34c61-466">Adım 4: Maliyet tahsisat hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="34c61-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="34c61-467">Tahsisat, bir tahsisat tabanı kullanarak bir maliyet nesnesinin diğer maliyet nesnelerine bakiyesini tahsis eder.</span><span class="sxs-lookup"><span data-stu-id="34c61-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="34c61-468">Finance karşılıklı tahsisat yöntemini desteklemektedir.</span><span class="sxs-lookup"><span data-stu-id="34c61-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="34c61-469">Karşılıklı tahsisat yönteminde, yardımcı maliyet nesnelerinin değiştiği karşılıklı hizmetler tümüyle tanınır.</span><span class="sxs-lookup"><span data-stu-id="34c61-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="34c61-470">Sistem, tahsisatların doğru gerçekleştireceği sırayı otomatik olarak belirler.</span><span class="sxs-lookup"><span data-stu-id="34c61-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="34c61-471">Bir maliyet nesnesinin bakiyesi tek bir tahsisat tabanı tarafından tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="34c61-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="34c61-472">Yeni maliyet nesnesi boyutları arasındaki tahsisatlar ve onların üyeleri desteklenir.</span><span class="sxs-lookup"><span data-stu-id="34c61-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="34c61-473">Tahsisatın sırası, maliyet kontrol birimi tarafından kontrol edilir.</span><span class="sxs-lookup"><span data-stu-id="34c61-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="34c61-474">[![Karşılıklı yöntemi](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="34c61-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="34c61-475">Maliyet tahsisatını tanımla</span><span class="sxs-lookup"><span data-stu-id="34c61-475">Define the cost allocation</span></span>

<span data-ttu-id="34c61-476">Bir maliyetin akışını nasıl izleyeceğinize dair basit bir örnek aşağıda verilmiştir,</span><span class="sxs-lookup"><span data-stu-id="34c61-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="34c61-477">Maliyet nesnesi CC001 HR, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="34c61-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="34c61-478">HR hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="34c61-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="34c61-479">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="34c61-479">Cost object</span></span></th>
<th><span data-ttu-id="34c61-480">HR hizmetleri</span><span class="sxs-lookup"><span data-stu-id="34c61-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="34c61-481">CC002</span><span class="sxs-lookup"><span data-stu-id="34c61-481">CC002</span></span></td>
<td><span data-ttu-id="34c61-482">Finans</span><span class="sxs-lookup"><span data-stu-id="34c61-482">Finance</span></span></td>
<td><span data-ttu-id="34c61-483">35</span><span class="sxs-lookup"><span data-stu-id="34c61-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-484">CC003</span><span class="sxs-lookup"><span data-stu-id="34c61-484">CC003</span></span></td>
<td><span data-ttu-id="34c61-485">Montaj</span><span class="sxs-lookup"><span data-stu-id="34c61-485">Assembly</span></span></td>
<td><span data-ttu-id="34c61-486">55</span><span class="sxs-lookup"><span data-stu-id="34c61-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-487">CC004</span><span class="sxs-lookup"><span data-stu-id="34c61-487">CC004</span></span></td>
<td><span data-ttu-id="34c61-488">Paketleme</span><span class="sxs-lookup"><span data-stu-id="34c61-488">Packaging</span></span></td>
<td><span data-ttu-id="34c61-489">10</span><span class="sxs-lookup"><span data-stu-id="34c61-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="34c61-490">Maliyet nesnesi CC002 Finans, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="34c61-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="34c61-491">Finans hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="34c61-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="34c61-492">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="34c61-492">Cost object</span></span></th>
<th><span data-ttu-id="34c61-493">Finans hizmetleri</span><span class="sxs-lookup"><span data-stu-id="34c61-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="34c61-494">CC003</span><span class="sxs-lookup"><span data-stu-id="34c61-494">CC003</span></span></td>
<td><span data-ttu-id="34c61-495">Montaj</span><span class="sxs-lookup"><span data-stu-id="34c61-495">Assembly</span></span></td>
<td><span data-ttu-id="34c61-496">65</span><span class="sxs-lookup"><span data-stu-id="34c61-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-497">CC004</span><span class="sxs-lookup"><span data-stu-id="34c61-497">CC004</span></span></td>
<td><span data-ttu-id="34c61-498">Paketleme</span><span class="sxs-lookup"><span data-stu-id="34c61-498">Packaging</span></span></td>
<td><span data-ttu-id="34c61-499">35</span><span class="sxs-lookup"><span data-stu-id="34c61-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="34c61-500">Maliyet nesnesi CC003 Derleme, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="34c61-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="34c61-501">Derleme hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="34c61-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="34c61-502">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="34c61-502">Cost object</span></span></th>
<th><span data-ttu-id="34c61-503">Derleme Hizmetleri (saat)</span><span class="sxs-lookup"><span data-stu-id="34c61-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="34c61-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="34c61-504">Prod 1</span></span></td>
<td><span data-ttu-id="34c61-505">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="34c61-505">Product 1</span></span></td>
<td><span data-ttu-id="34c61-506">60</span><span class="sxs-lookup"><span data-stu-id="34c61-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="34c61-507">Prod 2</span></span></td>
<td><span data-ttu-id="34c61-508">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="34c61-508">Product 2</span></span></td>
<td><span data-ttu-id="34c61-509">20</span><span class="sxs-lookup"><span data-stu-id="34c61-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="34c61-510">Maliyet nesnesi CC004 Ambalajlama, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="34c61-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="34c61-511">Ambalajlama hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="34c61-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="34c61-512">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="34c61-512">Cost object</span></span></th>
<th><span data-ttu-id="34c61-513">Ambalajlama hizmetleri (saat)</span><span class="sxs-lookup"><span data-stu-id="34c61-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="34c61-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="34c61-514">Prod 1</span></span></td>
<td><span data-ttu-id="34c61-515">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="34c61-515">Product 1</span></span></td>
<td><span data-ttu-id="34c61-516">80</span><span class="sxs-lookup"><span data-stu-id="34c61-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="34c61-517">Prod 2</span></span></td>
<td><span data-ttu-id="34c61-518">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="34c61-518">Product 2</span></span></td>
<td><span data-ttu-id="34c61-519">15</span><span class="sxs-lookup"><span data-stu-id="34c61-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="34c61-520">Bir ürünün tükettiği üretim saatleri gibi istatistiki ölçümler, doğrudan kaynak verilerinden alınabilir.</span><span class="sxs-lookup"><span data-stu-id="34c61-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="34c61-521">Daha fazla bilgi için, [İstatistiksel ölçüm sağlayıcı şablonu](statistical-measure-provider-template.md#statistical-measure-provider-template) bakın.</span><span class="sxs-lookup"><span data-stu-id="34c61-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="34c61-522">Aşağıdaki tablo, İK hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığında ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="34c61-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="34c61-523">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="34c61-523">Cost object</span></span></th>
<th><span data-ttu-id="34c61-524">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="34c61-524">Magnitude</span></span></th>
<th><span data-ttu-id="34c61-525">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="34c61-525">Allocation factor</span></span></th>
<th><span data-ttu-id="34c61-526">Tutar</span><span class="sxs-lookup"><span data-stu-id="34c61-526">Amount</span></span></th>
<th><span data-ttu-id="34c61-527">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="34c61-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="34c61-528">CC002</span><span class="sxs-lookup"><span data-stu-id="34c61-528">CC002</span></span></td>
<td><span data-ttu-id="34c61-529">Finans</span><span class="sxs-lookup"><span data-stu-id="34c61-529">Finance</span></span></td>
<td><span data-ttu-id="34c61-530">35</span><span class="sxs-lookup"><span data-stu-id="34c61-530">35</span></span></td>
<td><span data-ttu-id="34c61-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="34c61-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="34c61-532">175.00</span><span class="sxs-lookup"><span data-stu-id="34c61-532">175.00</span></span></td>
<td><span data-ttu-id="34c61-533">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-534">CC003</span><span class="sxs-lookup"><span data-stu-id="34c61-534">CC003</span></span></td>
<td><span data-ttu-id="34c61-535">Montaj</span><span class="sxs-lookup"><span data-stu-id="34c61-535">Assembly</span></span></td>
<td><span data-ttu-id="34c61-536">55</span><span class="sxs-lookup"><span data-stu-id="34c61-536">55</span></span></td>
<td><span data-ttu-id="34c61-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="34c61-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="34c61-538">275.00</span><span class="sxs-lookup"><span data-stu-id="34c61-538">275.00</span></span></td>
<td><span data-ttu-id="34c61-539">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-540">CC004</span><span class="sxs-lookup"><span data-stu-id="34c61-540">CC004</span></span></td>
<td><span data-ttu-id="34c61-541">Paketleme</span><span class="sxs-lookup"><span data-stu-id="34c61-541">Packaging</span></span></td>
<td><span data-ttu-id="34c61-542">10</span><span class="sxs-lookup"><span data-stu-id="34c61-542">10</span></span></td>
<td><span data-ttu-id="34c61-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="34c61-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="34c61-544">50,00</span><span class="sxs-lookup"><span data-stu-id="34c61-544">50.00</span></span></td>
<td><span data-ttu-id="34c61-545">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-546">CC002</span><span class="sxs-lookup"><span data-stu-id="34c61-546">CC002</span></span></td>
<td><span data-ttu-id="34c61-547">Finans</span><span class="sxs-lookup"><span data-stu-id="34c61-547">Finance</span></span></td>
<td><span data-ttu-id="34c61-548">35</span><span class="sxs-lookup"><span data-stu-id="34c61-548">35</span></span></td>
<td><span data-ttu-id="34c61-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="34c61-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="34c61-550">436.00</span><span class="sxs-lookup"><span data-stu-id="34c61-550">436.00</span></span></td>
<td><span data-ttu-id="34c61-551">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-552">CC003</span><span class="sxs-lookup"><span data-stu-id="34c61-552">CC003</span></span></td>
<td><span data-ttu-id="34c61-553">Montaj</span><span class="sxs-lookup"><span data-stu-id="34c61-553">Assembly</span></span></td>
<td><span data-ttu-id="34c61-554">55</span><span class="sxs-lookup"><span data-stu-id="34c61-554">55</span></span></td>
<td><span data-ttu-id="34c61-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="34c61-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="34c61-556">685.14</span><span class="sxs-lookup"><span data-stu-id="34c61-556">685.14</span></span></td>
<td><span data-ttu-id="34c61-557">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-558">CC004</span><span class="sxs-lookup"><span data-stu-id="34c61-558">CC004</span></span></td>
<td><span data-ttu-id="34c61-559">Paketleme</span><span class="sxs-lookup"><span data-stu-id="34c61-559">Packaging</span></span></td>
<td><span data-ttu-id="34c61-560">10</span><span class="sxs-lookup"><span data-stu-id="34c61-560">10</span></span></td>
<td><span data-ttu-id="34c61-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="34c61-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="34c61-562">124.57</span><span class="sxs-lookup"><span data-stu-id="34c61-562">124.57</span></span></td>
<td><span data-ttu-id="34c61-563">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="34c61-564">Aşağıdaki tablo, Finans hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="34c61-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="34c61-565">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="34c61-565">Cost object</span></span></th>
<th><span data-ttu-id="34c61-566">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="34c61-566">Magnitude</span></span></th>
<th><span data-ttu-id="34c61-567">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="34c61-567">Allocation factor</span></span></th>
<th><span data-ttu-id="34c61-568">Tutar</span><span class="sxs-lookup"><span data-stu-id="34c61-568">Amount</span></span></th>
<th><span data-ttu-id="34c61-569">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="34c61-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="34c61-570">CC003</span><span class="sxs-lookup"><span data-stu-id="34c61-570">CC003</span></span></td>
<td><span data-ttu-id="34c61-571">Montaj</span><span class="sxs-lookup"><span data-stu-id="34c61-571">Assembly</span></span></td>
<td><span data-ttu-id="34c61-572">65</span><span class="sxs-lookup"><span data-stu-id="34c61-572">65</span></span></td>
<td><span data-ttu-id="34c61-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="34c61-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="34c61-574">438.75</span><span class="sxs-lookup"><span data-stu-id="34c61-574">438.75</span></span></td>
<td><span data-ttu-id="34c61-575">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-576">CC004</span><span class="sxs-lookup"><span data-stu-id="34c61-576">CC004</span></span></td>
<td><span data-ttu-id="34c61-577">Paketleme</span><span class="sxs-lookup"><span data-stu-id="34c61-577">Packaging</span></span></td>
<td><span data-ttu-id="34c61-578">35</span><span class="sxs-lookup"><span data-stu-id="34c61-578">35</span></span></td>
<td><span data-ttu-id="34c61-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="34c61-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="34c61-580">236.25</span><span class="sxs-lookup"><span data-stu-id="34c61-580">236.25</span></span></td>
<td><span data-ttu-id="34c61-581">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-582">CC003</span><span class="sxs-lookup"><span data-stu-id="34c61-582">CC003</span></span></td>
<td><span data-ttu-id="34c61-583">Montaj</span><span class="sxs-lookup"><span data-stu-id="34c61-583">Assembly</span></span></td>
<td><span data-ttu-id="34c61-584">65</span><span class="sxs-lookup"><span data-stu-id="34c61-584">65</span></span></td>
<td><span data-ttu-id="34c61-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="34c61-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="34c61-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="34c61-586">5,297.69</span></span></td>
<td><span data-ttu-id="34c61-587">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-588">CC004</span><span class="sxs-lookup"><span data-stu-id="34c61-588">CC004</span></span></td>
<td><span data-ttu-id="34c61-589">Paketleme</span><span class="sxs-lookup"><span data-stu-id="34c61-589">Packaging</span></span></td>
<td><span data-ttu-id="34c61-590">35</span><span class="sxs-lookup"><span data-stu-id="34c61-590">35</span></span></td>
<td><span data-ttu-id="34c61-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="34c61-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="34c61-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="34c61-592">2,852.60</span></span></td>
<td><span data-ttu-id="34c61-593">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="34c61-594">Aşağıdaki tablo, Derleme hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="34c61-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="34c61-595">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="34c61-595">Cost object</span></span></th>
<th><span data-ttu-id="34c61-596">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="34c61-596">Magnitude</span></span></th>
<th><span data-ttu-id="34c61-597">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="34c61-597">Allocation factor</span></span></th>
<th><span data-ttu-id="34c61-598">Tutar</span><span class="sxs-lookup"><span data-stu-id="34c61-598">Amount</span></span></th>
<th><span data-ttu-id="34c61-599">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="34c61-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="34c61-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="34c61-600">Prod 1</span></span></td>
<td><span data-ttu-id="34c61-601">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="34c61-601">Product 1</span></span></td>
<td><span data-ttu-id="34c61-602">60</span><span class="sxs-lookup"><span data-stu-id="34c61-602">60</span></span></td>
<td><span data-ttu-id="34c61-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="34c61-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="34c61-604">535.31</span><span class="sxs-lookup"><span data-stu-id="34c61-604">535.31</span></span></td>
<td><span data-ttu-id="34c61-605">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="34c61-606">Prod 2</span></span></td>
<td><span data-ttu-id="34c61-607">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="34c61-607">Product 2</span></span></td>
<td><span data-ttu-id="34c61-608">20</span><span class="sxs-lookup"><span data-stu-id="34c61-608">20</span></span></td>
<td><span data-ttu-id="34c61-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="34c61-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="34c61-610">178.44</span><span class="sxs-lookup"><span data-stu-id="34c61-610">178.44</span></span></td>
<td><span data-ttu-id="34c61-611">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="34c61-612">Prod 1</span></span></td>
<td><span data-ttu-id="34c61-613">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="34c61-613">Product 1</span></span></td>
<td><span data-ttu-id="34c61-614">60</span><span class="sxs-lookup"><span data-stu-id="34c61-614">60</span></span></td>
<td><span data-ttu-id="34c61-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="34c61-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="34c61-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="34c61-616">4,487.12</span></span></td>
<td><span data-ttu-id="34c61-617">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="34c61-618">Prod 2</span></span></td>
<td><span data-ttu-id="34c61-619">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="34c61-619">Product 2</span></span></td>
<td><span data-ttu-id="34c61-620">20</span><span class="sxs-lookup"><span data-stu-id="34c61-620">20</span></span></td>
<td><span data-ttu-id="34c61-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="34c61-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="34c61-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="34c61-622">1,495.71</span></span></td>
<td><span data-ttu-id="34c61-623">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="34c61-624">Aşağıdaki tablo, Paketleme hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="34c61-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="34c61-625">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="34c61-625">Cost object</span></span></th>
<th><span data-ttu-id="34c61-626">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="34c61-626">Magnitude</span></span></th>
<th><span data-ttu-id="34c61-627">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="34c61-627">Allocation factor</span></span></th>
<th><span data-ttu-id="34c61-628">Tutar</span><span class="sxs-lookup"><span data-stu-id="34c61-628">Amount</span></span></th>
<th><span data-ttu-id="34c61-629">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="34c61-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="34c61-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="34c61-630">Prod 1</span></span></td>
<td><span data-ttu-id="34c61-631">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="34c61-631">Product 1</span></span></td>
<td><span data-ttu-id="34c61-632">80</span><span class="sxs-lookup"><span data-stu-id="34c61-632">80</span></span></td>
<td><span data-ttu-id="34c61-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="34c61-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="34c61-634">241.05</span><span class="sxs-lookup"><span data-stu-id="34c61-634">241.05</span></span></td>
<td><span data-ttu-id="34c61-635">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="34c61-636">Prod 2</span></span></td>
<td><span data-ttu-id="34c61-637">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="34c61-637">Product 2</span></span></td>
<td><span data-ttu-id="34c61-638">15</span><span class="sxs-lookup"><span data-stu-id="34c61-638">15</span></span></td>
<td><span data-ttu-id="34c61-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="34c61-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="34c61-640">45.20</span><span class="sxs-lookup"><span data-stu-id="34c61-640">45.20</span></span></td>
<td><span data-ttu-id="34c61-641">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="34c61-642">Prod 1</span></span></td>
<td><span data-ttu-id="34c61-643">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="34c61-643">Product 1</span></span></td>
<td><span data-ttu-id="34c61-644">80</span><span class="sxs-lookup"><span data-stu-id="34c61-644">80</span></span></td>
<td><span data-ttu-id="34c61-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="34c61-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="34c61-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="34c61-646">2,507.09</span></span></td>
<td><span data-ttu-id="34c61-647">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="34c61-648">Prod 2</span></span></td>
<td><span data-ttu-id="34c61-649">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="34c61-649">Product 2</span></span></td>
<td><span data-ttu-id="34c61-650">15</span><span class="sxs-lookup"><span data-stu-id="34c61-650">15</span></span></td>
<td><span data-ttu-id="34c61-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="34c61-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="34c61-652">470.08</span><span class="sxs-lookup"><span data-stu-id="34c61-652">470.08</span></span></td>
<td><span data-ttu-id="34c61-653">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="34c61-654">Günlük girişleri (maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="34c61-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="34c61-655">Günlük</span><span class="sxs-lookup"><span data-stu-id="34c61-655">Journal</span></span></th>
<th><span data-ttu-id="34c61-656">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="34c61-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="34c61-657">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="34c61-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="34c61-658">Sürüm</span><span class="sxs-lookup"><span data-stu-id="34c61-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="34c61-659">00004</span><span class="sxs-lookup"><span data-stu-id="34c61-659">00004</span></span></td>
<td><span data-ttu-id="34c61-660">Maliyet tahsisatı günlüğü</span><span class="sxs-lookup"><span data-stu-id="34c61-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="34c61-661">Mali</span><span class="sxs-lookup"><span data-stu-id="34c61-661">Fiscal</span></span></td>
<td><span data-ttu-id="34c61-662">2017</span><span class="sxs-lookup"><span data-stu-id="34c61-662">2017</span></span></td>
<td><span data-ttu-id="34c61-663">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="34c61-663">Period 1</span></span></td>
<td><span data-ttu-id="34c61-664">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="34c61-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="34c61-665">Günlük satırları</span><span class="sxs-lookup"><span data-stu-id="34c61-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="34c61-666">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="34c61-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="34c61-667">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="34c61-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="34c61-668">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="34c61-668">Cost element</span></span></th>
<th><span data-ttu-id="34c61-669">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="34c61-669">Cost behavior</span></span></th>
<th><span data-ttu-id="34c61-670">Tutar</span><span class="sxs-lookup"><span data-stu-id="34c61-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="34c61-671">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="34c61-672">CC001</span><span class="sxs-lookup"><span data-stu-id="34c61-672">CC001</span></span></td>
<td><span data-ttu-id="34c61-673">İK</span><span class="sxs-lookup"><span data-stu-id="34c61-673">HR</span></span></td>
<td><span data-ttu-id="34c61-674">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-674">10001</span></span></td>
<td><span data-ttu-id="34c61-675">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-675">Electricity</span></span></td>
<td><span data-ttu-id="34c61-676">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-676">Fixed cost</span></span></td>
<td><span data-ttu-id="34c61-677">500.00</span><span class="sxs-lookup"><span data-stu-id="34c61-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-678">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="34c61-679">CC001</span><span class="sxs-lookup"><span data-stu-id="34c61-679">CC001</span></span></td>
<td><span data-ttu-id="34c61-680">İK</span><span class="sxs-lookup"><span data-stu-id="34c61-680">HR</span></span></td>
<td><span data-ttu-id="34c61-681">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-681">10001</span></span></td>
<td><span data-ttu-id="34c61-682">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-682">Electricity</span></span></td>
<td><span data-ttu-id="34c61-683">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-683">Variable cost</span></span></td>
<td><span data-ttu-id="34c61-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="34c61-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-685">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="34c61-686">CC002</span><span class="sxs-lookup"><span data-stu-id="34c61-686">CC002</span></span></td>
<td><span data-ttu-id="34c61-687">Finans</span><span class="sxs-lookup"><span data-stu-id="34c61-687">Finance</span></span></td>
<td><span data-ttu-id="34c61-688">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-688">10001</span></span></td>
<td><span data-ttu-id="34c61-689">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-689">Electricity</span></span></td>
<td><span data-ttu-id="34c61-690">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-690">Fixed cost</span></span></td>
<td><span data-ttu-id="34c61-691">675.00</span><span class="sxs-lookup"><span data-stu-id="34c61-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-692">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="34c61-693">CC002</span><span class="sxs-lookup"><span data-stu-id="34c61-693">CC002</span></span></td>
<td><span data-ttu-id="34c61-694">Finans</span><span class="sxs-lookup"><span data-stu-id="34c61-694">Finance</span></span></td>
<td><span data-ttu-id="34c61-695">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-695">10001</span></span></td>
<td><span data-ttu-id="34c61-696">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-696">Electricity</span></span></td>
<td><span data-ttu-id="34c61-697">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-697">Variable cost</span></span></td>
<td><span data-ttu-id="34c61-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="34c61-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-699">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="34c61-700">CC003</span><span class="sxs-lookup"><span data-stu-id="34c61-700">CC003</span></span></td>
<td><span data-ttu-id="34c61-701">Montaj</span><span class="sxs-lookup"><span data-stu-id="34c61-701">Assembly</span></span></td>
<td><span data-ttu-id="34c61-702">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-702">10001</span></span></td>
<td><span data-ttu-id="34c61-703">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-703">Electricity</span></span></td>
<td><span data-ttu-id="34c61-704">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-704">Fixed cost</span></span></td>
<td><span data-ttu-id="34c61-705">713.75</span><span class="sxs-lookup"><span data-stu-id="34c61-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-706">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="34c61-707">CC003</span><span class="sxs-lookup"><span data-stu-id="34c61-707">CC003</span></span></td>
<td><span data-ttu-id="34c61-708">Montaj</span><span class="sxs-lookup"><span data-stu-id="34c61-708">Assembly</span></span></td>
<td><span data-ttu-id="34c61-709">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-709">10001</span></span></td>
<td><span data-ttu-id="34c61-710">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-710">Electricity</span></span></td>
<td><span data-ttu-id="34c61-711">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-711">Variable cost</span></span></td>
<td><span data-ttu-id="34c61-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="34c61-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-713">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="34c61-714">CC003</span><span class="sxs-lookup"><span data-stu-id="34c61-714">CC003</span></span></td>
<td><span data-ttu-id="34c61-715">Paketleme</span><span class="sxs-lookup"><span data-stu-id="34c61-715">Packaging</span></span></td>
<td><span data-ttu-id="34c61-716">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-716">10001</span></span></td>
<td><span data-ttu-id="34c61-717">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-717">Electricity</span></span></td>
<td><span data-ttu-id="34c61-718">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-718">Fixed cost</span></span></td>
<td><span data-ttu-id="34c61-719">286.25</span><span class="sxs-lookup"><span data-stu-id="34c61-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-720">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="34c61-721">CC003</span><span class="sxs-lookup"><span data-stu-id="34c61-721">CC003</span></span></td>
<td><span data-ttu-id="34c61-722">Paketleme</span><span class="sxs-lookup"><span data-stu-id="34c61-722">Packaging</span></span></td>
<td><span data-ttu-id="34c61-723">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-723">10001</span></span></td>
<td><span data-ttu-id="34c61-724">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-724">Electricity</span></span></td>
<td><span data-ttu-id="34c61-725">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-725">Variable cost</span></span></td>
<td><span data-ttu-id="34c61-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="34c61-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-727">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="34c61-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="34c61-728">Prod 1</span></span></td>
<td><span data-ttu-id="34c61-729">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="34c61-729">Product 1</span></span></td>
<td><span data-ttu-id="34c61-730">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-730">10001</span></span></td>
<td><span data-ttu-id="34c61-731">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-731">Electricity</span></span></td>
<td><span data-ttu-id="34c61-732">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-732">Fixed cost</span></span></td>
<td><span data-ttu-id="34c61-733">776.36</span><span class="sxs-lookup"><span data-stu-id="34c61-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-734">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="34c61-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="34c61-735">Prod 1</span></span></td>
<td><span data-ttu-id="34c61-736">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="34c61-736">Product 1</span></span></td>
<td><span data-ttu-id="34c61-737">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-737">10001</span></span></td>
<td><span data-ttu-id="34c61-738">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-738">Electricity</span></span></td>
<td><span data-ttu-id="34c61-739">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-739">Variable cost</span></span></td>
<td><span data-ttu-id="34c61-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="34c61-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-741">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="34c61-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="34c61-742">Prod 2</span></span></td>
<td><span data-ttu-id="34c61-743">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="34c61-743">Product 1</span></span></td>
<td><span data-ttu-id="34c61-744">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-744">10001</span></span></td>
<td><span data-ttu-id="34c61-745">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-745">Electricity</span></span></td>
<td><span data-ttu-id="34c61-746">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-746">Fixed cost</span></span></td>
<td><span data-ttu-id="34c61-747">223.64</span><span class="sxs-lookup"><span data-stu-id="34c61-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-748">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="34c61-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="34c61-749">Prod 2</span></span></td>
<td><span data-ttu-id="34c61-750">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="34c61-750">Product 1</span></span></td>
<td><span data-ttu-id="34c61-751">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-751">10001</span></span></td>
<td><span data-ttu-id="34c61-752">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-752">Electricity</span></span></td>
<td><span data-ttu-id="34c61-753">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-753">Variable cost</span></span></td>
<td><span data-ttu-id="34c61-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="34c61-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="34c61-755">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="34c61-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="34c61-756">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="34c61-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="34c61-757">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="34c61-757">Cost element</span></span></th>
<th><span data-ttu-id="34c61-758">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="34c61-758">Cost behavior</span></span></th>
<th><span data-ttu-id="34c61-759">Tutar</span><span class="sxs-lookup"><span data-stu-id="34c61-759">Amount</span></span></th>
<th><span data-ttu-id="34c61-760">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="34c61-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="34c61-761">CC001</span><span class="sxs-lookup"><span data-stu-id="34c61-761">CC001</span></span></td>
<td><span data-ttu-id="34c61-762">İK</span><span class="sxs-lookup"><span data-stu-id="34c61-762">HR</span></span></td>
<td><span data-ttu-id="34c61-763">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-763">10001</span></span></td>
<td><span data-ttu-id="34c61-764">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-764">Electricity</span></span></td>
<td><span data-ttu-id="34c61-765">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-765">Fixed cost</span></span></td>
<td><span data-ttu-id="34c61-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="34c61-766">-500.00</span></span></td>
<td><span data-ttu-id="34c61-767">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-768">CC002</span><span class="sxs-lookup"><span data-stu-id="34c61-768">CC002</span></span></td>
<td><span data-ttu-id="34c61-769">Finans</span><span class="sxs-lookup"><span data-stu-id="34c61-769">Finance</span></span></td>
<td><span data-ttu-id="34c61-770">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-770">10001</span></span></td>
<td><span data-ttu-id="34c61-771">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-771">Electricity</span></span></td>
<td><span data-ttu-id="34c61-772">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-772">Fixed cost</span></span></td>
<td><span data-ttu-id="34c61-773">175.00</span><span class="sxs-lookup"><span data-stu-id="34c61-773">175.00</span></span></td>
<td><span data-ttu-id="34c61-774">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-775">CC003</span><span class="sxs-lookup"><span data-stu-id="34c61-775">CC003</span></span></td>
<td><span data-ttu-id="34c61-776">Montaj</span><span class="sxs-lookup"><span data-stu-id="34c61-776">Assembly</span></span></td>
<td><span data-ttu-id="34c61-777">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-777">10001</span></span></td>
<td><span data-ttu-id="34c61-778">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-778">Electricity</span></span></td>
<td><span data-ttu-id="34c61-779">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-779">Fixed cost</span></span></td>
<td><span data-ttu-id="34c61-780">275.00</span><span class="sxs-lookup"><span data-stu-id="34c61-780">275.00</span></span></td>
<td><span data-ttu-id="34c61-781">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-782">CC004</span><span class="sxs-lookup"><span data-stu-id="34c61-782">CC004</span></span></td>
<td><span data-ttu-id="34c61-783">Paketleme</span><span class="sxs-lookup"><span data-stu-id="34c61-783">Packaging</span></span></td>
<td><span data-ttu-id="34c61-784">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-784">10001</span></span></td>
<td><span data-ttu-id="34c61-785">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-785">Electricity</span></span></td>
<td><span data-ttu-id="34c61-786">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-786">Fixed cost</span></span></td>
<td><span data-ttu-id="34c61-787">50,00</span><span class="sxs-lookup"><span data-stu-id="34c61-787">50,00</span></span></td>
<td><span data-ttu-id="34c61-788">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-789">CC001</span><span class="sxs-lookup"><span data-stu-id="34c61-789">CC001</span></span></td>
<td><span data-ttu-id="34c61-790">İK</span><span class="sxs-lookup"><span data-stu-id="34c61-790">HR</span></span></td>
<td><span data-ttu-id="34c61-791">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-791">10001</span></span></td>
<td><span data-ttu-id="34c61-792">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-792">Electricity</span></span></td>
<td><span data-ttu-id="34c61-793">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-793">Variable cost</span></span></td>
<td><span data-ttu-id="34c61-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="34c61-794">-1,245.71</span></span></td>
<td><span data-ttu-id="34c61-795">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-796">CC002</span><span class="sxs-lookup"><span data-stu-id="34c61-796">CC002</span></span></td>
<td><span data-ttu-id="34c61-797">Finans</span><span class="sxs-lookup"><span data-stu-id="34c61-797">Finance</span></span></td>
<td><span data-ttu-id="34c61-798">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-798">10001</span></span></td>
<td><span data-ttu-id="34c61-799">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-799">Electricity</span></span></td>
<td><span data-ttu-id="34c61-800">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-800">Variable cost</span></span></td>
<td><span data-ttu-id="34c61-801">436.00</span><span class="sxs-lookup"><span data-stu-id="34c61-801">436.00</span></span></td>
<td><span data-ttu-id="34c61-802">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-803">CC003</span><span class="sxs-lookup"><span data-stu-id="34c61-803">CC003</span></span></td>
<td><span data-ttu-id="34c61-804">Montaj</span><span class="sxs-lookup"><span data-stu-id="34c61-804">Assembly</span></span></td>
<td><span data-ttu-id="34c61-805">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-805">10001</span></span></td>
<td><span data-ttu-id="34c61-806">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-806">Electricity</span></span></td>
<td><span data-ttu-id="34c61-807">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-807">Variable cost</span></span></td>
<td><span data-ttu-id="34c61-808">685.14</span><span class="sxs-lookup"><span data-stu-id="34c61-808">685.14</span></span></td>
<td><span data-ttu-id="34c61-809">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-810">CC004</span><span class="sxs-lookup"><span data-stu-id="34c61-810">CC004</span></span></td>
<td><span data-ttu-id="34c61-811">Paketleme</span><span class="sxs-lookup"><span data-stu-id="34c61-811">Packaging</span></span></td>
<td><span data-ttu-id="34c61-812">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-812">10001</span></span></td>
<td><span data-ttu-id="34c61-813">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-813">Electricity</span></span></td>
<td><span data-ttu-id="34c61-814">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-814">Variable cost</span></span></td>
<td><span data-ttu-id="34c61-815">124.57</span><span class="sxs-lookup"><span data-stu-id="34c61-815">124.57</span></span></td>
<td><span data-ttu-id="34c61-816">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-817">CC002</span><span class="sxs-lookup"><span data-stu-id="34c61-817">CC002</span></span></td>
<td><span data-ttu-id="34c61-818">Finans</span><span class="sxs-lookup"><span data-stu-id="34c61-818">Finance</span></span></td>
<td><span data-ttu-id="34c61-819">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-819">10001</span></span></td>
<td><span data-ttu-id="34c61-820">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-820">Electricity</span></span></td>
<td><span data-ttu-id="34c61-821">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-821">Fixed cost</span></span></td>
<td><span data-ttu-id="34c61-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="34c61-822">-675.00</span></span></td>
<td><span data-ttu-id="34c61-823">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-824">CC003</span><span class="sxs-lookup"><span data-stu-id="34c61-824">CC003</span></span></td>
<td><span data-ttu-id="34c61-825">Montaj</span><span class="sxs-lookup"><span data-stu-id="34c61-825">Assembly</span></span></td>
<td><span data-ttu-id="34c61-826">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-826">10001</span></span></td>
<td><span data-ttu-id="34c61-827">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-827">Electricity</span></span></td>
<td><span data-ttu-id="34c61-828">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-828">Fixed cost</span></span></td>
<td><span data-ttu-id="34c61-829">438.75</span><span class="sxs-lookup"><span data-stu-id="34c61-829">438.75</span></span></td>
<td><span data-ttu-id="34c61-830">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-831">CC004</span><span class="sxs-lookup"><span data-stu-id="34c61-831">CC004</span></span></td>
<td><span data-ttu-id="34c61-832">Paketleme</span><span class="sxs-lookup"><span data-stu-id="34c61-832">Packaging</span></span></td>
<td><span data-ttu-id="34c61-833">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-833">10001</span></span></td>
<td><span data-ttu-id="34c61-834">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-834">Electricity</span></span></td>
<td><span data-ttu-id="34c61-835">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-835">Fixed cost</span></span></td>
<td><span data-ttu-id="34c61-836">236.25</span><span class="sxs-lookup"><span data-stu-id="34c61-836">236.25</span></span></td>
<td><span data-ttu-id="34c61-837">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-838">CC002</span><span class="sxs-lookup"><span data-stu-id="34c61-838">CC002</span></span></td>
<td><span data-ttu-id="34c61-839">Finans</span><span class="sxs-lookup"><span data-stu-id="34c61-839">Finance</span></span></td>
<td><span data-ttu-id="34c61-840">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-840">10001</span></span></td>
<td><span data-ttu-id="34c61-841">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-841">Electricity</span></span></td>
<td><span data-ttu-id="34c61-842">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-842">Variable cost</span></span></td>
<td><span data-ttu-id="34c61-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="34c61-843">-8,150.29</span></span></td>
<td><span data-ttu-id="34c61-844">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-845">CC003</span><span class="sxs-lookup"><span data-stu-id="34c61-845">CC003</span></span></td>
<td><span data-ttu-id="34c61-846">Montaj</span><span class="sxs-lookup"><span data-stu-id="34c61-846">Assembly</span></span></td>
<td><span data-ttu-id="34c61-847">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-847">10001</span></span></td>
<td><span data-ttu-id="34c61-848">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-848">Electricity</span></span></td>
<td><span data-ttu-id="34c61-849">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-849">Variable cost</span></span></td>
<td><span data-ttu-id="34c61-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="34c61-850">5,297.69</span></span></td>
<td><span data-ttu-id="34c61-851">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-852">CC004</span><span class="sxs-lookup"><span data-stu-id="34c61-852">CC004</span></span></td>
<td><span data-ttu-id="34c61-853">Paketleme</span><span class="sxs-lookup"><span data-stu-id="34c61-853">Packaging</span></span></td>
<td><span data-ttu-id="34c61-854">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-854">10001</span></span></td>
<td><span data-ttu-id="34c61-855">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-855">Electricity</span></span></td>
<td><span data-ttu-id="34c61-856">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-856">Variable cost</span></span></td>
<td><span data-ttu-id="34c61-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="34c61-857">2,852.60</span></span></td>
<td><span data-ttu-id="34c61-858">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-859">CC003</span><span class="sxs-lookup"><span data-stu-id="34c61-859">CC003</span></span></td>
<td><span data-ttu-id="34c61-860">Montaj</span><span class="sxs-lookup"><span data-stu-id="34c61-860">Assembly</span></span></td>
<td><span data-ttu-id="34c61-861">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-861">10001</span></span></td>
<td><span data-ttu-id="34c61-862">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-862">Electricity</span></span></td>
<td><span data-ttu-id="34c61-863">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-863">Fixed cost</span></span></td>
<td><span data-ttu-id="34c61-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="34c61-864">-713.75</span></span></td>
<td><span data-ttu-id="34c61-865">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="34c61-866">Prod 1</span></span></td>
<td><span data-ttu-id="34c61-867">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="34c61-867">Product 1</span></span></td>
<td><span data-ttu-id="34c61-868">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-868">10001</span></span></td>
<td><span data-ttu-id="34c61-869">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-869">Electricity</span></span></td>
<td><span data-ttu-id="34c61-870">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-870">Fixed cost</span></span></td>
<td><span data-ttu-id="34c61-871">535.31</span><span class="sxs-lookup"><span data-stu-id="34c61-871">535.31</span></span></td>
<td><span data-ttu-id="34c61-872">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="34c61-873">Prod 2</span></span></td>
<td><span data-ttu-id="34c61-874">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="34c61-874">Product 2</span></span></td>
<td><span data-ttu-id="34c61-875">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-875">10001</span></span></td>
<td><span data-ttu-id="34c61-876">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-876">Electricity</span></span></td>
<td><span data-ttu-id="34c61-877">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-877">Fixed cost</span></span></td>
<td><span data-ttu-id="34c61-878">178.44</span><span class="sxs-lookup"><span data-stu-id="34c61-878">178.44</span></span></td>
<td><span data-ttu-id="34c61-879">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-880">CC003</span><span class="sxs-lookup"><span data-stu-id="34c61-880">CC003</span></span></td>
<td><span data-ttu-id="34c61-881">Montaj</span><span class="sxs-lookup"><span data-stu-id="34c61-881">Assembly</span></span></td>
<td><span data-ttu-id="34c61-882">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-882">10001</span></span></td>
<td><span data-ttu-id="34c61-883">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-883">Electricity</span></span></td>
<td><span data-ttu-id="34c61-884">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-884">Variable cost</span></span></td>
<td><span data-ttu-id="34c61-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="34c61-885">-5,982.83</span></span></td>
<td><span data-ttu-id="34c61-886">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="34c61-887">Prod 1</span></span></td>
<td><span data-ttu-id="34c61-888">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="34c61-888">Product 1</span></span></td>
<td><span data-ttu-id="34c61-889">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-889">10001</span></span></td>
<td><span data-ttu-id="34c61-890">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-890">Electricity</span></span></td>
<td><span data-ttu-id="34c61-891">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-891">Variable cost</span></span></td>
<td><span data-ttu-id="34c61-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="34c61-892">4,487.12</span></span></td>
<td><span data-ttu-id="34c61-893">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="34c61-894">Prod 2</span></span></td>
<td><span data-ttu-id="34c61-895">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="34c61-895">Product 2</span></span></td>
<td><span data-ttu-id="34c61-896">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-896">10001</span></span></td>
<td><span data-ttu-id="34c61-897">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-897">Electricity</span></span></td>
<td><span data-ttu-id="34c61-898">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-898">Variable cost</span></span></td>
<td><span data-ttu-id="34c61-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="34c61-899">1,495.71</span></span></td>
<td><span data-ttu-id="34c61-900">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-901">CC003</span><span class="sxs-lookup"><span data-stu-id="34c61-901">CC003</span></span></td>
<td><span data-ttu-id="34c61-902">Montaj</span><span class="sxs-lookup"><span data-stu-id="34c61-902">Assembly</span></span></td>
<td><span data-ttu-id="34c61-903">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-903">10001</span></span></td>
<td><span data-ttu-id="34c61-904">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-904">Electricity</span></span></td>
<td><span data-ttu-id="34c61-905">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-905">Fixed cost</span></span></td>
<td><span data-ttu-id="34c61-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="34c61-906">-286.25</span></span></td>
<td><span data-ttu-id="34c61-907">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="34c61-908">Prod 1</span></span></td>
<td><span data-ttu-id="34c61-909">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="34c61-909">Product 1</span></span></td>
<td><span data-ttu-id="34c61-910">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-910">10001</span></span></td>
<td><span data-ttu-id="34c61-911">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-911">Electricity</span></span></td>
<td><span data-ttu-id="34c61-912">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-912">Fixed cost</span></span></td>
<td><span data-ttu-id="34c61-913">241.05</span><span class="sxs-lookup"><span data-stu-id="34c61-913">241.05</span></span></td>
<td><span data-ttu-id="34c61-914">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="34c61-915">Prod 2</span></span></td>
<td><span data-ttu-id="34c61-916">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="34c61-916">Product 2</span></span></td>
<td><span data-ttu-id="34c61-917">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-917">10001</span></span></td>
<td><span data-ttu-id="34c61-918">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-918">Electricity</span></span></td>
<td><span data-ttu-id="34c61-919">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-919">Fixed cost</span></span></td>
<td><span data-ttu-id="34c61-920">45.20</span><span class="sxs-lookup"><span data-stu-id="34c61-920">45.20</span></span></td>
<td><span data-ttu-id="34c61-921">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-922">CC003</span><span class="sxs-lookup"><span data-stu-id="34c61-922">CC003</span></span></td>
<td><span data-ttu-id="34c61-923">Montaj</span><span class="sxs-lookup"><span data-stu-id="34c61-923">Assembly</span></span></td>
<td><span data-ttu-id="34c61-924">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-924">10001</span></span></td>
<td><span data-ttu-id="34c61-925">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-925">Electricity</span></span></td>
<td><span data-ttu-id="34c61-926">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-926">Variable cost</span></span></td>
<td><span data-ttu-id="34c61-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="34c61-927">-2,977.17</span></span></td>
<td><span data-ttu-id="34c61-928">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="34c61-929">Prod 1</span></span></td>
<td><span data-ttu-id="34c61-930">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="34c61-930">Product 1</span></span></td>
<td><span data-ttu-id="34c61-931">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-931">10001</span></span></td>
<td><span data-ttu-id="34c61-932">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-932">Electricity</span></span></td>
<td><span data-ttu-id="34c61-933">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-933">Variable cost</span></span></td>
<td><span data-ttu-id="34c61-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="34c61-934">2,507.09</span></span></td>
<td><span data-ttu-id="34c61-935">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="34c61-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="34c61-936">Prod 2</span></span></td>
<td><span data-ttu-id="34c61-937">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="34c61-937">Product 2</span></span></td>
<td><span data-ttu-id="34c61-938">10001</span><span class="sxs-lookup"><span data-stu-id="34c61-938">10001</span></span></td>
<td><span data-ttu-id="34c61-939">Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-939">Electricity</span></span></td>
<td><span data-ttu-id="34c61-940">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-940">Variable cost</span></span></td>
<td><span data-ttu-id="34c61-941">470.08</span><span class="sxs-lookup"><span data-stu-id="34c61-941">470.08</span></span></td>
<td><span data-ttu-id="34c61-942">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="34c61-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="34c61-943">Sonuç</span><span class="sxs-lookup"><span data-stu-id="34c61-943">Conclusion</span></span>
<span data-ttu-id="34c61-944">Mali muhasebede, Elektrik için 10.000,00 maliyet bir sözde maliyet merkezi kimliğine nakledilmiştir.</span><span class="sxs-lookup"><span data-stu-id="34c61-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="34c61-945">Bu nedenle, maliyet muhasebecileri bu maliyetin tahsis edilmesi gerektiğini bilirler.</span><span class="sxs-lookup"><span data-stu-id="34c61-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="34c61-946">Maliyet muhasebesinde, maliyetler kuruluş birimleri ve seviyeleri arasında, uygulanan kural ve ilkelere dayalı olarak akar.</span><span class="sxs-lookup"><span data-stu-id="34c61-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="34c61-947">Her maliyet, maliyetlerin tahsisatı için en iyi değerlendirmeyi sağlayan bir tahsisat tabanı ile ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="34c61-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="34c61-948">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="34c61-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="34c61-949">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="34c61-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="34c61-950">Toplam</span><span class="sxs-lookup"><span data-stu-id="34c61-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="34c61-951">CC099</span><span class="sxs-lookup"><span data-stu-id="34c61-951">CC099</span></span></th>
<th><span data-ttu-id="34c61-952">CC001</span><span class="sxs-lookup"><span data-stu-id="34c61-952">CC001</span></span></th>
<th><span data-ttu-id="34c61-953">CC002</span><span class="sxs-lookup"><span data-stu-id="34c61-953">CC002</span></span></th>
<th><span data-ttu-id="34c61-954">CC003</span><span class="sxs-lookup"><span data-stu-id="34c61-954">CC003</span></span></th>
<th><span data-ttu-id="34c61-955">CC004</span><span class="sxs-lookup"><span data-stu-id="34c61-955">CC004</span></span></th>
<th><span data-ttu-id="34c61-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="34c61-956">Proj 1</span></span></th>
<th><span data-ttu-id="34c61-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="34c61-957">Proj 2</span></span></th>
<th><span data-ttu-id="34c61-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="34c61-958">Prod 1</span></span></th>
<th><span data-ttu-id="34c61-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="34c61-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="34c61-960">10001 Elektrik</span><span class="sxs-lookup"><span data-stu-id="34c61-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="34c61-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="34c61-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="34c61-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="34c61-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="34c61-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="34c61-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="34c61-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="34c61-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="34c61-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="34c61-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="34c61-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="34c61-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="34c61-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="34c61-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="34c61-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="34c61-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="34c61-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="34c61-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="34c61-970">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="34c61-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="34c61-971">0,00</span><span class="sxs-lookup"><span data-stu-id="34c61-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="34c61-972">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="34c61-973">0,00</span><span class="sxs-lookup"><span data-stu-id="34c61-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="34c61-974">0,00</span><span class="sxs-lookup"><span data-stu-id="34c61-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="34c61-975">0,00</span><span class="sxs-lookup"><span data-stu-id="34c61-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="34c61-976">0,00</span><span class="sxs-lookup"><span data-stu-id="34c61-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="34c61-977">0,00</span><span class="sxs-lookup"><span data-stu-id="34c61-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="34c61-978">776.36</span><span class="sxs-lookup"><span data-stu-id="34c61-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="34c61-979">223.64</span><span class="sxs-lookup"><span data-stu-id="34c61-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="34c61-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="34c61-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="34c61-981">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="34c61-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="34c61-982">000</span><span class="sxs-lookup"><span data-stu-id="34c61-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="34c61-983">0,00</span><span class="sxs-lookup"><span data-stu-id="34c61-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="34c61-984">0,00</span><span class="sxs-lookup"><span data-stu-id="34c61-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="34c61-985">0,00</span><span class="sxs-lookup"><span data-stu-id="34c61-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="34c61-986">0,00</span><span class="sxs-lookup"><span data-stu-id="34c61-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="34c61-987">30.00</span><span class="sxs-lookup"><span data-stu-id="34c61-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="34c61-988">10,00</span><span class="sxs-lookup"><span data-stu-id="34c61-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="34c61-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="34c61-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="34c61-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="34c61-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="34c61-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="34c61-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="34c61-992">Bu konu, birincil maliyet öğesi, 10001 Elektrik'in maliyet nesneleri arasında nasıl aktığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="34c61-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="34c61-993">Bu nedenle, bu genel gider maliyeti kuruluşun en düşük seviyesine tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="34c61-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="34c61-994">Başka bir deyişle, maliyet en alt düzeydeki maliyet nesnelerine aittir.</span><span class="sxs-lookup"><span data-stu-id="34c61-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="34c61-995">Maliyetin, maliyet nesneleri arasında görsel bir akışına ihtiyacınız varsa, maliyetin akışını görselleştirmek için maliyet toplamı ilke kurallarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34c61-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="34c61-996">Daha fazla bilgi için bkz. [Maliyet yuvarlama ilkesi ve genel gider hesaplaması](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="34c61-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



