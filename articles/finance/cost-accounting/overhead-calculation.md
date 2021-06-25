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
ms.openlocfilehash: 8dc312e66dc666ac6c23bac6b705ffc7893fd06b
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188009"
---
# <a name="overhead-calculation"></a><span data-ttu-id="5ef53-103">Genel gider hesaplaması</span><span class="sxs-lookup"><span data-stu-id="5ef53-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5ef53-104">Bu konu, genel gider maliyetlerinin hesaplanması için tipik işlemleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="5ef53-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

## <a name="term-definition"></a><span data-ttu-id="5ef53-105">Terim tanımı</span><span class="sxs-lookup"><span data-stu-id="5ef53-105">Term definition</span></span>

<span data-ttu-id="5ef53-106">Genel gider maliyetleri bir işletmenin çalışması için normalde uygulanan, ancak doğrudan herhangi bir özel iş, faaliyet, ürün veya hizmete ilişkilendirilmemiş olan maliyetlerdir.</span><span class="sxs-lookup"><span data-stu-id="5ef53-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="5ef53-107">Genel gider maliyetleri kar sağlama faaliyetlerinin oluşturulması için kritik destek sağlar.</span><span class="sxs-lookup"><span data-stu-id="5ef53-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="5ef53-108">Aşağıda bazı genel gider örnekleri verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="5ef53-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="5ef53-109">Kira</span><span class="sxs-lookup"><span data-stu-id="5ef53-109">Rent</span></span>
-   <span data-ttu-id="5ef53-110">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-110">Electricity</span></span>
-   <span data-ttu-id="5ef53-111">Yönetim maaşları</span><span class="sxs-lookup"><span data-stu-id="5ef53-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="5ef53-112">Genel gider hesaplaması genel bakış</span><span class="sxs-lookup"><span data-stu-id="5ef53-112">Overhead calculation overview</span></span>
<span data-ttu-id="5ef53-113">Genel gider hesaplama, maliyet muhasebesi ilkelerini doğru sırayla çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="5ef53-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="5ef53-114">Maliyet muhasebesi ilkeleri değiştiyse veya belirli hatalar algılandıysa, genel gider hesaplamasını aynı mali dönem için birden fazla kez yürütebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5ef53-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="5ef53-115">Her genel gider hesaplaması depolanır ve önceki sürümlerdeki hesaplamaları kıyaslamanıza olanak sağlayan, benzersiz bir sürüm kimliğine sahip olur.</span><span class="sxs-lookup"><span data-stu-id="5ef53-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="5ef53-116">Genel gider hesaplamasının oluşturduğu maliyet girişleri bir muhasebe tarihi alır.</span><span class="sxs-lookup"><span data-stu-id="5ef53-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="5ef53-117">Bu muhasebe tarihi, hesaplamada kullanılan mali dönemin bitiş tarihiyle eşleşir.</span><span class="sxs-lookup"><span data-stu-id="5ef53-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="5ef53-118">Benzersiz sürüm kimliği aşağıdaki öğelerden oluşur:</span><span class="sxs-lookup"><span data-stu-id="5ef53-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="5ef53-119">Sürüm türü</span><span class="sxs-lookup"><span data-stu-id="5ef53-119">Version type</span></span>
-   <span data-ttu-id="5ef53-120">Tarih ve saat</span><span class="sxs-lookup"><span data-stu-id="5ef53-120">Date and time</span></span>
-   <span data-ttu-id="5ef53-121">Maliyet muhasebesi defteri</span><span class="sxs-lookup"><span data-stu-id="5ef53-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="5ef53-122">Mali yıl</span><span class="sxs-lookup"><span data-stu-id="5ef53-122">Fiscal year</span></span>
-   <span data-ttu-id="5ef53-123">Mali dönem</span><span class="sxs-lookup"><span data-stu-id="5ef53-123">Fiscal period</span></span>

<span data-ttu-id="5ef53-124">Genel gider hesaplama, sürümden bağımsız olarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="5ef53-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="5ef53-125">Bu nedenle, Gerçek sürümden önce Bütçe sürümünü hesaplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5ef53-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="5ef53-126">Genel gider hesaplama dört adımdan oluşur, aşağıdaki çizimde gösterildiği gibi.</span><span class="sxs-lookup"><span data-stu-id="5ef53-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="5ef53-127">Her adımda, günlük girişleri olan bir günlük başlığı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5ef53-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="5ef53-128">Bu günlük başlığı, her hesaplama adımı için giriş verilerini tutar.</span><span class="sxs-lookup"><span data-stu-id="5ef53-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="5ef53-129">İlkeler ve kurallar her günlük satırına uygulanır ve maliyet girişleri çıkış olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5ef53-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="5ef53-130">Bu nedenle, her zaman tam izlenebilirliğe sahip olursunuz.</span><span class="sxs-lookup"><span data-stu-id="5ef53-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="5ef53-131">[![Genel gider hesaplaması](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="5ef53-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="5ef53-132">Elektrik genel gideri maliyetini hesapla ve tahsis et</span><span class="sxs-lookup"><span data-stu-id="5ef53-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="5ef53-133">Mali muhasebede, elektrik gibi bazı maliyetler peşin ödeme olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="5ef53-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="5ef53-134">Bu nedenle, Maliyet muhasebesi için ayrıntılı yönetim bilgiler sağlanmaz.</span><span class="sxs-lookup"><span data-stu-id="5ef53-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="5ef53-135">Maliyet muhasebesinde doğru yönetimsel bilgileri tüm yönetim birim ve düzeylerinde sağlamak için, maliyetlerin kuruluş birimleri arasında akması gerekir.</span><span class="sxs-lookup"><span data-stu-id="5ef53-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="5ef53-136">Bu akış, tüketimin doğru bir kaydına ya da adil bir değerlendirmeye dayanıyor olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5ef53-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="5ef53-137">Genel muhasebede, bir elektrik maliyeti aşağıdaki tabloda gösterildiği gibi deftere nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="5ef53-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5ef53-138">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="5ef53-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5ef53-139">Maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="5ef53-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="5ef53-140">Ana hesap</span><span class="sxs-lookup"><span data-stu-id="5ef53-140">Main account</span></span></th>
<th><span data-ttu-id="5ef53-141">Muhasebe para birimi cinsinden tutar</span><span class="sxs-lookup"><span data-stu-id="5ef53-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ef53-142">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="5ef53-143">CC099</span><span class="sxs-lookup"><span data-stu-id="5ef53-143">CC099</span></span></td>
<td><span data-ttu-id="5ef53-144">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="5ef53-144">Default cost center</span></span></td>
<td><span data-ttu-id="5ef53-145">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-145">10001</span></span></td>
<td><span data-ttu-id="5ef53-146">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-146">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="5ef53-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="5ef53-148">Adım 1: Maliyet davranışı hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="5ef53-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="5ef53-149">Varsayılan olarak, maliyeti girişleri kaynak veriden içeri alındığında, Maliyet muhasebesinde **Sınıflandırılmamış** maliyet davranışı sınıflandırmasını alırlar.</span><span class="sxs-lookup"><span data-stu-id="5ef53-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="5ef53-150">Maliyet davranışı ilke kuralları ekleyerek, maliyet girişlerini **Sabit maliyet** veya **Değişken maliyet** olarak yeniden sınıflandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5ef53-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="5ef53-151">Maliyet davranış kuralını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="5ef53-151">Define the cost behavior rule</span></span>

<span data-ttu-id="5ef53-152">Bazı durumlarda, sabit bir ücret maliyet parçasıdır ve kalan maliyet, tüketime dayanır.</span><span class="sxs-lookup"><span data-stu-id="5ef53-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="5ef53-153">Elektrik faturaları genellikle bu tanıma uyar.</span><span class="sxs-lookup"><span data-stu-id="5ef53-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="5ef53-154">Belirli bir sabit ücret ödedikten sonra, kilovat saatlik (Kwh) tüketim başına ödeme yaparsınız.</span><span class="sxs-lookup"><span data-stu-id="5ef53-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="5ef53-155">Örneğin, sabit maliyet masrafı 1.000,00 ise, maliyet davranışı kural nasıl tanımlanır:</span><span class="sxs-lookup"><span data-stu-id="5ef53-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="5ef53-156">Sabit tutar 1.000,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="5ef53-157">0 &lt;= 1.000,00 = Sabit</span><span class="sxs-lookup"><span data-stu-id="5ef53-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="5ef53-158">1000,01 &lt; N = Değişken</span><span class="sxs-lookup"><span data-stu-id="5ef53-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="5ef53-159">Günlük</span><span class="sxs-lookup"><span data-stu-id="5ef53-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5ef53-160">Günlük</span><span class="sxs-lookup"><span data-stu-id="5ef53-160">Journal</span></span></th>
<th><span data-ttu-id="5ef53-161">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="5ef53-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5ef53-162">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="5ef53-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5ef53-163">Sürüm</span><span class="sxs-lookup"><span data-stu-id="5ef53-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ef53-164">00001</span><span class="sxs-lookup"><span data-stu-id="5ef53-164">00001</span></span></td>
<td><span data-ttu-id="5ef53-165">Maliyet davranışı hesaplama günlüğü</span><span class="sxs-lookup"><span data-stu-id="5ef53-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="5ef53-166">Mali</span><span class="sxs-lookup"><span data-stu-id="5ef53-166">Fiscal</span></span></td>
<td><span data-ttu-id="5ef53-167">2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-167">2017</span></span></td>
<td><span data-ttu-id="5ef53-168">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-168">Period 1</span></span></td>
<td><span data-ttu-id="5ef53-169">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="5ef53-170">Günlük girişleri (Maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="5ef53-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5ef53-171">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="5ef53-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5ef53-172">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="5ef53-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5ef53-173">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="5ef53-173">Cost element</span></span></th>
<th><span data-ttu-id="5ef53-174">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="5ef53-174">Cost behavior</span></span></th>
<th><span data-ttu-id="5ef53-175">Tutar</span><span class="sxs-lookup"><span data-stu-id="5ef53-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ef53-176">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="5ef53-177">CC099</span><span class="sxs-lookup"><span data-stu-id="5ef53-177">CC099</span></span></td>
<td><span data-ttu-id="5ef53-178">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="5ef53-178">Default cost center</span></span></td>
<td><span data-ttu-id="5ef53-179">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-179">10001</span></span></td>
<td><span data-ttu-id="5ef53-180">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-180">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-181">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="5ef53-181">Unclassified</span></span></td>
<td><span data-ttu-id="5ef53-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="5ef53-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5ef53-183">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="5ef53-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ef53-184">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="5ef53-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5ef53-185">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="5ef53-185">Cost element</span></span></th>
<th><span data-ttu-id="5ef53-186">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="5ef53-186">Cost behavior</span></span></th>
<th><span data-ttu-id="5ef53-187">Tutar</span><span class="sxs-lookup"><span data-stu-id="5ef53-187">Amount</span></span></th>
<th><span data-ttu-id="5ef53-188">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="5ef53-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ef53-189">CC099</span><span class="sxs-lookup"><span data-stu-id="5ef53-189">CC099</span></span></td>
<td><span data-ttu-id="5ef53-190">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="5ef53-190">Default cost center</span></span></td>
<td><span data-ttu-id="5ef53-191">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-191">10001</span></span></td>
<td><span data-ttu-id="5ef53-192">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-192">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-193">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="5ef53-193">Unclassified</span></span></td>
<td><span data-ttu-id="5ef53-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="5ef53-194">10,000.00</span></span></td>
<td><span data-ttu-id="5ef53-195">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-196">CC099</span><span class="sxs-lookup"><span data-stu-id="5ef53-196">CC099</span></span></td>
<td><span data-ttu-id="5ef53-197">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="5ef53-197">Default cost center</span></span></td>
<td><span data-ttu-id="5ef53-198">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-198">10001</span></span></td>
<td><span data-ttu-id="5ef53-199">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-199">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-200">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="5ef53-200">Unclassified</span></span></td>
<td><span data-ttu-id="5ef53-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-201">-10,000.00</span></span></td>
<td><span data-ttu-id="5ef53-202">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-203">CC099</span><span class="sxs-lookup"><span data-stu-id="5ef53-203">CC099</span></span></td>
<td><span data-ttu-id="5ef53-204">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="5ef53-204">Default cost center</span></span></td>
<td><span data-ttu-id="5ef53-205">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-205">10001</span></span></td>
<td><span data-ttu-id="5ef53-206">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-206">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-207">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-207">Fixed cost</span></span></td>
<td><span data-ttu-id="5ef53-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-208">1,000.00</span></span></td>
<td><span data-ttu-id="5ef53-209">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-210">CC099</span><span class="sxs-lookup"><span data-stu-id="5ef53-210">CC099</span></span></td>
<td><span data-ttu-id="5ef53-211">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="5ef53-211">Default cost center</span></span></td>
<td><span data-ttu-id="5ef53-212">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-212">10001</span></span></td>
<td><span data-ttu-id="5ef53-213">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-213">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-214">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-214">Variable cost</span></span></td>
<td><span data-ttu-id="5ef53-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="5ef53-215">9,000.00</span></span></td>
<td><span data-ttu-id="5ef53-216">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ef53-217">Daha fazla bilgi için bkz. [Maliyet davranışı ilkesi oluşturma ve bir maliyet kontrol birimine atama](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="5ef53-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="5ef53-218">Adım 2: Maliyet dağıtımı hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="5ef53-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="5ef53-219">Maliyet dağıtımı, bir nesneden bir veya daha fazlasına ilgili tahsisat tabanı uygulayarak maliyeti yeniden dağıtmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5ef53-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="5ef53-220">Maliyet dağıtımı ve maliyet tahsisatı, maliyet dağıtımının her zaman orijinal maliyetin birincil maliyet öğesinde bulunmasıyla farklılık gösterir.</span><span class="sxs-lookup"><span data-stu-id="5ef53-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="5ef53-221">Maliyet dağıtım kuralını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="5ef53-221">Define the cost distribution rule</span></span>

<span data-ttu-id="5ef53-222">Mali muhasebede, elektrik maliyetleri çoğu zaman peşin ödeme olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="5ef53-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="5ef53-223">Maliyet muhasebesinde ise bu yöntem yeterince ayrıntılı değildir.</span><span class="sxs-lookup"><span data-stu-id="5ef53-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="5ef53-224">Değişken maliyet, maliyet nesnelerine tek tek, adil bir temele dayanarak dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5ef53-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="5ef53-225">En mantıklı tahsisat, elektrik kullanımını (Kwh) temel alarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5ef53-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="5ef53-226">Elektrik adına sahip, istatistiksel bir boyut üyesi oluşturulur ve elektrik tüketimi kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="5ef53-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="5ef53-227">Varsayıla olarak, tüm istatistiksel boyut üyeleri tahsisat tabanları olarak kullanılabilir hale gelir.</span><span class="sxs-lookup"><span data-stu-id="5ef53-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ef53-228">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="5ef53-228">Cost object</span></span></th>
<th><span data-ttu-id="5ef53-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="5ef53-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ef53-230">CC001</span><span class="sxs-lookup"><span data-stu-id="5ef53-230">CC001</span></span></td>
<td><span data-ttu-id="5ef53-231">İK</span><span class="sxs-lookup"><span data-stu-id="5ef53-231">HR</span></span></td>
<td><span data-ttu-id="5ef53-232">1.000</span><span class="sxs-lookup"><span data-stu-id="5ef53-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-233">CC002</span><span class="sxs-lookup"><span data-stu-id="5ef53-233">CC002</span></span></td>
<td><span data-ttu-id="5ef53-234">Finans</span><span class="sxs-lookup"><span data-stu-id="5ef53-234">Finance</span></span></td>
<td><span data-ttu-id="5ef53-235">6,000</span><span class="sxs-lookup"><span data-stu-id="5ef53-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-236">CC003</span><span class="sxs-lookup"><span data-stu-id="5ef53-236">CC003</span></span></td>
<td><span data-ttu-id="5ef53-237">Montaj</span><span class="sxs-lookup"><span data-stu-id="5ef53-237">Assembly</span></span></td>
<td><span data-ttu-id="5ef53-238">0</span><span class="sxs-lookup"><span data-stu-id="5ef53-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ef53-239">Aşağıdaki tablo, elektrik tüketiminin değişken maliyetler için bir tahsisat tabanlı olarak uygulandığındaki sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="5ef53-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ef53-240">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="5ef53-240">Cost object</span></span></th>
<th><span data-ttu-id="5ef53-241">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="5ef53-241">Magnitude</span></span></th>
<th><span data-ttu-id="5ef53-242">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="5ef53-242">Allocation factor</span></span></th>
<th><span data-ttu-id="5ef53-243">Tutar</span><span class="sxs-lookup"><span data-stu-id="5ef53-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ef53-244">CC001</span><span class="sxs-lookup"><span data-stu-id="5ef53-244">CC001</span></span></td>
<td><span data-ttu-id="5ef53-245">İK</span><span class="sxs-lookup"><span data-stu-id="5ef53-245">HR</span></span></td>
<td><span data-ttu-id="5ef53-246">1.000</span><span class="sxs-lookup"><span data-stu-id="5ef53-246">1,000</span></span></td>
<td><span data-ttu-id="5ef53-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="5ef53-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="5ef53-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-249">CC002</span><span class="sxs-lookup"><span data-stu-id="5ef53-249">CC002</span></span></td>
<td><span data-ttu-id="5ef53-250">Finans</span><span class="sxs-lookup"><span data-stu-id="5ef53-250">Finance</span></span></td>
<td><span data-ttu-id="5ef53-251">6,000</span><span class="sxs-lookup"><span data-stu-id="5ef53-251">6,000</span></span></td>
<td><span data-ttu-id="5ef53-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="5ef53-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="5ef53-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-254">CC003</span><span class="sxs-lookup"><span data-stu-id="5ef53-254">CC003</span></span></td>
<td><span data-ttu-id="5ef53-255">Montaj</span><span class="sxs-lookup"><span data-stu-id="5ef53-255">Assembly</span></span></td>
<td><span data-ttu-id="5ef53-256">0</span><span class="sxs-lookup"><span data-stu-id="5ef53-256">0</span></span></td>
<td><span data-ttu-id="5ef53-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="5ef53-258">0,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ef53-259">Sabit maliyet, elektrik tüketmiş olan tekil maliyet nesnelerine eşit miktarda dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5ef53-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="5ef53-260">Bu sonuca, Elektrik istatistiksel boyut öğesini bir formül tahsisat tabanında kullanarak ulaşabilirsiniz: (Elektrik &gt; 0,00) Aşağıdaki tablo, elektrik tüketimi değişken maliyetler için bir tahsisat tabanı olarak kullanıldığında ortaya çıkan sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="5ef53-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ef53-261">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="5ef53-261">Cost object</span></span></th>
<th><span data-ttu-id="5ef53-262">Formül</span><span class="sxs-lookup"><span data-stu-id="5ef53-262">Formula</span></span></th>
<th><span data-ttu-id="5ef53-263">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="5ef53-263">Magnitude</span></span></th>
<th><span data-ttu-id="5ef53-264">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="5ef53-264">Allocation factor</span></span></th>
<th><span data-ttu-id="5ef53-265">Tutar</span><span class="sxs-lookup"><span data-stu-id="5ef53-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ef53-266">CC001</span><span class="sxs-lookup"><span data-stu-id="5ef53-266">CC001</span></span></td>
<td><span data-ttu-id="5ef53-267">İK</span><span class="sxs-lookup"><span data-stu-id="5ef53-267">HR</span></span></td>
<td><span data-ttu-id="5ef53-268">(1,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="5ef53-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="5ef53-269">1</span><span class="sxs-lookup"><span data-stu-id="5ef53-269">1</span></span></td>
<td><span data-ttu-id="5ef53-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="5ef53-271">500.00</span><span class="sxs-lookup"><span data-stu-id="5ef53-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-272">CC002</span><span class="sxs-lookup"><span data-stu-id="5ef53-272">CC002</span></span></td>
<td><span data-ttu-id="5ef53-273">Finans</span><span class="sxs-lookup"><span data-stu-id="5ef53-273">Finance</span></span></td>
<td><span data-ttu-id="5ef53-274">(6,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="5ef53-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="5ef53-275">1</span><span class="sxs-lookup"><span data-stu-id="5ef53-275">1</span></span></td>
<td><span data-ttu-id="5ef53-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="5ef53-277">500.00</span><span class="sxs-lookup"><span data-stu-id="5ef53-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-278">CC003</span><span class="sxs-lookup"><span data-stu-id="5ef53-278">CC003</span></span></td>
<td><span data-ttu-id="5ef53-279">Montaj</span><span class="sxs-lookup"><span data-stu-id="5ef53-279">Assembly</span></span></td>
<td><span data-ttu-id="5ef53-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="5ef53-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="5ef53-281">0</span><span class="sxs-lookup"><span data-stu-id="5ef53-281">0</span></span></td>
<td><span data-ttu-id="5ef53-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="5ef53-283">0,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="5ef53-284">Günlük</span><span class="sxs-lookup"><span data-stu-id="5ef53-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5ef53-285">Günlük</span><span class="sxs-lookup"><span data-stu-id="5ef53-285">Journal</span></span></th>
<th><span data-ttu-id="5ef53-286">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="5ef53-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5ef53-287">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="5ef53-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5ef53-288">Sürüm</span><span class="sxs-lookup"><span data-stu-id="5ef53-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ef53-289">00002</span><span class="sxs-lookup"><span data-stu-id="5ef53-289">00002</span></span></td>
<td><span data-ttu-id="5ef53-290">Maliyet dağıtımı hesaplama günlüğü</span><span class="sxs-lookup"><span data-stu-id="5ef53-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="5ef53-291">Mali</span><span class="sxs-lookup"><span data-stu-id="5ef53-291">Fiscal</span></span></td>
<td><span data-ttu-id="5ef53-292">2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-292">2017</span></span></td>
<td><span data-ttu-id="5ef53-293">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-293">Period 1</span></span></td>
<td><span data-ttu-id="5ef53-294">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="5ef53-295">Günlük girişleri (Maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="5ef53-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5ef53-296">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="5ef53-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5ef53-297">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="5ef53-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5ef53-298">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="5ef53-298">Cost element</span></span></th>
<th><span data-ttu-id="5ef53-299">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="5ef53-299">Cost behavior</span></span></th>
<th><span data-ttu-id="5ef53-300">Tutar</span><span class="sxs-lookup"><span data-stu-id="5ef53-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ef53-301">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ef53-302">CC099</span><span class="sxs-lookup"><span data-stu-id="5ef53-302">CC099</span></span></td>
<td><span data-ttu-id="5ef53-303">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="5ef53-303">Default cost center</span></span></td>
<td><span data-ttu-id="5ef53-304">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-304">10001</span></span></td>
<td><span data-ttu-id="5ef53-305">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-305">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-306">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-306">Fixed cost</span></span></td>
<td><span data-ttu-id="5ef53-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-308">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ef53-309">CC099</span><span class="sxs-lookup"><span data-stu-id="5ef53-309">CC099</span></span></td>
<td><span data-ttu-id="5ef53-310">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="5ef53-310">Default cost center</span></span></td>
<td><span data-ttu-id="5ef53-311">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-311">10001</span></span></td>
<td><span data-ttu-id="5ef53-312">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-312">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-313">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-313">Variable cost</span></span></td>
<td><span data-ttu-id="5ef53-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="5ef53-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5ef53-315">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="5ef53-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ef53-316">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="5ef53-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5ef53-317">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="5ef53-317">Cost element</span></span></th>
<th><span data-ttu-id="5ef53-318">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="5ef53-318">Cost behavior</span></span></th>
<th><span data-ttu-id="5ef53-319">Tutar</span><span class="sxs-lookup"><span data-stu-id="5ef53-319">Amount</span></span></th>
<th><span data-ttu-id="5ef53-320">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="5ef53-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ef53-321">CC099</span><span class="sxs-lookup"><span data-stu-id="5ef53-321">CC099</span></span></td>
<td><span data-ttu-id="5ef53-322">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="5ef53-322">Default cost center</span></span></td>
<td><span data-ttu-id="5ef53-323">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-323">10001</span></span></td>
<td><span data-ttu-id="5ef53-324">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-324">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-325">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-325">Fixed cost</span></span></td>
<td><span data-ttu-id="5ef53-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-326">-1,000.00</span></span></td>
<td><span data-ttu-id="5ef53-327">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-328">CC001</span><span class="sxs-lookup"><span data-stu-id="5ef53-328">CC001</span></span></td>
<td><span data-ttu-id="5ef53-329">İK</span><span class="sxs-lookup"><span data-stu-id="5ef53-329">HR</span></span></td>
<td><span data-ttu-id="5ef53-330">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-330">10001</span></span></td>
<td><span data-ttu-id="5ef53-331">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-331">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-332">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-332">Fixed cost</span></span></td>
<td><span data-ttu-id="5ef53-333">500.00</span><span class="sxs-lookup"><span data-stu-id="5ef53-333">500.00</span></span></td>
<td><span data-ttu-id="5ef53-334">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-335">CC002</span><span class="sxs-lookup"><span data-stu-id="5ef53-335">CC002</span></span></td>
<td><span data-ttu-id="5ef53-336">Finans</span><span class="sxs-lookup"><span data-stu-id="5ef53-336">Finance</span></span></td>
<td><span data-ttu-id="5ef53-337">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-337">10001</span></span></td>
<td><span data-ttu-id="5ef53-338">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-338">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-339">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-339">Fixed cost</span></span></td>
<td><span data-ttu-id="5ef53-340">500.00</span><span class="sxs-lookup"><span data-stu-id="5ef53-340">500.00</span></span></td>
<td><span data-ttu-id="5ef53-341">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-342">CC099</span><span class="sxs-lookup"><span data-stu-id="5ef53-342">CC099</span></span></td>
<td><span data-ttu-id="5ef53-343">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="5ef53-343">Default cost center</span></span></td>
<td><span data-ttu-id="5ef53-344">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-344">10001</span></span></td>
<td><span data-ttu-id="5ef53-345">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-345">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-346">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-346">Variable cost</span></span></td>
<td><span data-ttu-id="5ef53-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-347">-9,000.00</span></span></td>
<td><span data-ttu-id="5ef53-348">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-349">CC001</span><span class="sxs-lookup"><span data-stu-id="5ef53-349">CC001</span></span></td>
<td><span data-ttu-id="5ef53-350">İK</span><span class="sxs-lookup"><span data-stu-id="5ef53-350">HR</span></span></td>
<td><span data-ttu-id="5ef53-351">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-351">10001</span></span></td>
<td><span data-ttu-id="5ef53-352">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-352">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-353">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-353">Variable cost</span></span></td>
<td><span data-ttu-id="5ef53-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="5ef53-354">1,285.71</span></span></td>
<td><span data-ttu-id="5ef53-355">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-356">CC002</span><span class="sxs-lookup"><span data-stu-id="5ef53-356">CC002</span></span></td>
<td><span data-ttu-id="5ef53-357">Finans</span><span class="sxs-lookup"><span data-stu-id="5ef53-357">Finance</span></span></td>
<td><span data-ttu-id="5ef53-358">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-358">10001</span></span></td>
<td><span data-ttu-id="5ef53-359">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-359">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-360">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-360">Variable cost</span></span></td>
<td><span data-ttu-id="5ef53-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="5ef53-361">7,714.29</span></span></td>
<td><span data-ttu-id="5ef53-362">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ef53-363">Daha fazla bilgi için bkz. [Maliyet dağıtımı ilkesi oluşturma ve bir maliyet kontrol birimine atama](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="5ef53-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="5ef53-364">Adım 3: Genel gider oranı hesaplama işlemi</span><span class="sxs-lookup"><span data-stu-id="5ef53-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="5ef53-365">Genel gider oranı, bir veya birden fazla belirli maliyet nesnesine masraf yüklemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5ef53-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="5ef53-366">Masraf, önceden belirlenmiş maliyet oranına ve tahsisat tabanından hesaplanan büyüklüğe dayanır.</span><span class="sxs-lookup"><span data-stu-id="5ef53-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="5ef53-367">Genel gider oranını tanımlama</span><span class="sxs-lookup"><span data-stu-id="5ef53-367">Define the overhead rate</span></span>

<span data-ttu-id="5ef53-368">Maliyet nesnesi CC001 HR, bir dizi dahili projeye katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="5ef53-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="5ef53-369">HR projeleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5ef53-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ef53-370">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="5ef53-370">Cost object</span></span></th>
<th><span data-ttu-id="5ef53-371">Saatler</span><span class="sxs-lookup"><span data-stu-id="5ef53-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ef53-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-372">Proj 1</span></span></td>
<td><span data-ttu-id="5ef53-373">Proje 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-373">Project 1</span></span></td>
<td><span data-ttu-id="5ef53-374">3</span><span class="sxs-lookup"><span data-stu-id="5ef53-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5ef53-375">Proj 2</span></span></td>
<td><span data-ttu-id="5ef53-376">Proje 2</span><span class="sxs-lookup"><span data-stu-id="5ef53-376">Project 2</span></span></td>
<td><span data-ttu-id="5ef53-377">1</span><span class="sxs-lookup"><span data-stu-id="5ef53-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ef53-378">Maliyet projeleri dağıtımı için bir önceden belirlenmiş maliyet oranı tanımlandı.</span><span class="sxs-lookup"><span data-stu-id="5ef53-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ef53-379">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="5ef53-379">Cost object</span></span></th>
<th><span data-ttu-id="5ef53-380">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="5ef53-380">Cost element</span></span></th>
<th><span data-ttu-id="5ef53-381">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="5ef53-381">Cost behavior</span></span></th>
<th><span data-ttu-id="5ef53-382">Birimler</span><span class="sxs-lookup"><span data-stu-id="5ef53-382">Units</span></span></th>
<th><span data-ttu-id="5ef53-383">Ücret</span><span class="sxs-lookup"><span data-stu-id="5ef53-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ef53-384">CC001</span><span class="sxs-lookup"><span data-stu-id="5ef53-384">CC001</span></span></td>
<td><span data-ttu-id="5ef53-385">İK</span><span class="sxs-lookup"><span data-stu-id="5ef53-385">HR</span></span></td>
<td><span data-ttu-id="5ef53-386">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-386">10001</span></span></td>
<td><span data-ttu-id="5ef53-387">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-387">Variable cost</span></span></td>
<td><span data-ttu-id="5ef53-388">1</span><span class="sxs-lookup"><span data-stu-id="5ef53-388">1</span></span></td>
<td><span data-ttu-id="5ef53-389">10</span><span class="sxs-lookup"><span data-stu-id="5ef53-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ef53-390">Aşağıdaki tablo, HR projeleri bir tahsisat tabanı olarak uygulandığındaki sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="5ef53-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ef53-391">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="5ef53-391">Cost object</span></span></th>
<th><span data-ttu-id="5ef53-392">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="5ef53-392">Magnitude</span></span></th>
<th><span data-ttu-id="5ef53-393">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="5ef53-393">Cost element</span></span></th>
<th><span data-ttu-id="5ef53-394">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="5ef53-394">Allocation factor</span></span></th>
<th><span data-ttu-id="5ef53-395">Tutar</span><span class="sxs-lookup"><span data-stu-id="5ef53-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ef53-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-396">Proj 1</span></span></td>
<td><span data-ttu-id="5ef53-397">Proje 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-397">Project 1</span></span></td>
<td><span data-ttu-id="5ef53-398">3</span><span class="sxs-lookup"><span data-stu-id="5ef53-398">3</span></span></td>
<td><span data-ttu-id="5ef53-399">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-399">10001</span></span></td>
<td><span data-ttu-id="5ef53-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="5ef53-401">30.00</span><span class="sxs-lookup"><span data-stu-id="5ef53-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5ef53-402">Proj 2</span></span></td>
<td><span data-ttu-id="5ef53-403">Proje 2</span><span class="sxs-lookup"><span data-stu-id="5ef53-403">Project 2</span></span></td>
<td><span data-ttu-id="5ef53-404">1</span><span class="sxs-lookup"><span data-stu-id="5ef53-404">1</span></span></td>
<td><span data-ttu-id="5ef53-405">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-405">10001</span></span></td>
<td><span data-ttu-id="5ef53-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="5ef53-407">10,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="5ef53-408">Günlük</span><span class="sxs-lookup"><span data-stu-id="5ef53-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5ef53-409">Günlük</span><span class="sxs-lookup"><span data-stu-id="5ef53-409">Journal</span></span></th>
<th><span data-ttu-id="5ef53-410">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="5ef53-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5ef53-411">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="5ef53-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5ef53-412">Sürüm</span><span class="sxs-lookup"><span data-stu-id="5ef53-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ef53-413">00003</span><span class="sxs-lookup"><span data-stu-id="5ef53-413">00003</span></span></td>
<td><span data-ttu-id="5ef53-414">Genel gider oranı hesaplaması günlüğü</span><span class="sxs-lookup"><span data-stu-id="5ef53-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="5ef53-415">Mali</span><span class="sxs-lookup"><span data-stu-id="5ef53-415">Fiscal</span></span></td>
<td><span data-ttu-id="5ef53-416">2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-416">2017</span></span></td>
<td><span data-ttu-id="5ef53-417">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-417">Period 1</span></span></td>
<td><span data-ttu-id="5ef53-418">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="5ef53-419">Günlük girişleri (Genel gider oranı hesaplaması için günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="5ef53-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5ef53-420">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="5ef53-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5ef53-421">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="5ef53-421">Cost object</span></span></th>
<th><span data-ttu-id="5ef53-422">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="5ef53-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ef53-423">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ef53-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-424">Proj 1</span></span></td>
<td><span data-ttu-id="5ef53-425">Dahili Proj 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="5ef53-426">3,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-427">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ef53-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5ef53-428">Proj 2</span></span></td>
<td><span data-ttu-id="5ef53-429">Dahili Proj 2</span><span class="sxs-lookup"><span data-stu-id="5ef53-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="5ef53-430">1.00</span><span class="sxs-lookup"><span data-stu-id="5ef53-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5ef53-431">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="5ef53-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ef53-432">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="5ef53-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5ef53-433">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="5ef53-433">Cost element</span></span></th>
<th><span data-ttu-id="5ef53-434">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="5ef53-434">Cost behavior</span></span></th>
<th><span data-ttu-id="5ef53-435">Tutar</span><span class="sxs-lookup"><span data-stu-id="5ef53-435">Amount</span></span></th>
<th><span data-ttu-id="5ef53-436">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="5ef53-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ef53-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="5ef53-437">CC0001</span></span></td>
<td><span data-ttu-id="5ef53-438">İK</span><span class="sxs-lookup"><span data-stu-id="5ef53-438">HR</span></span></td>
<td><span data-ttu-id="5ef53-439">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-439">10001</span></span></td>
<td><span data-ttu-id="5ef53-440">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-440">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-441">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-441">Variable cost</span></span></td>
<td><span data-ttu-id="5ef53-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-442">-30.00</span></span></td>
<td><span data-ttu-id="5ef53-443">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-444">Proj 1</span></span></td>
<td><span data-ttu-id="5ef53-445">Dahili Proj 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="5ef53-446">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-446">10001</span></span></td>
<td><span data-ttu-id="5ef53-447">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-447">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-448">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-448">Variable cost</span></span></td>
<td><span data-ttu-id="5ef53-449">30.00</span><span class="sxs-lookup"><span data-stu-id="5ef53-449">30.00</span></span></td>
<td><span data-ttu-id="5ef53-450">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-451">CC001</span><span class="sxs-lookup"><span data-stu-id="5ef53-451">CC001</span></span></td>
<td><span data-ttu-id="5ef53-452">İK</span><span class="sxs-lookup"><span data-stu-id="5ef53-452">HR</span></span></td>
<td><span data-ttu-id="5ef53-453">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-453">10001</span></span></td>
<td><span data-ttu-id="5ef53-454">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-454">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-455">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-455">Variable cost</span></span></td>
<td><span data-ttu-id="5ef53-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-456">-10.00</span></span></td>
<td><span data-ttu-id="5ef53-457">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5ef53-458">Proj 2</span></span></td>
<td><span data-ttu-id="5ef53-459">Dahili Proj 2</span><span class="sxs-lookup"><span data-stu-id="5ef53-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="5ef53-460">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-460">10001</span></span></td>
<td><span data-ttu-id="5ef53-461">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-461">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-462">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-462">Variable cost</span></span></td>
<td><span data-ttu-id="5ef53-463">10,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-463">10.00</span></span></td>
<td><span data-ttu-id="5ef53-464">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ef53-465">Daha fazla bilgi için [Genel gider hesaplaması gerçekleştir](cost-rollup.md#perform-overhead-calculation) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="5ef53-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="5ef53-466">Adım 4: Maliyet tahsisat hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="5ef53-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="5ef53-467">Tahsisat, bir tahsisat tabanı kullanarak bir maliyet nesnesinin diğer maliyet nesnelerine bakiyesini tahsis eder.</span><span class="sxs-lookup"><span data-stu-id="5ef53-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="5ef53-468">Finance karşılıklı tahsisat yöntemini desteklemektedir.</span><span class="sxs-lookup"><span data-stu-id="5ef53-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="5ef53-469">Karşılıklı tahsisat yönteminde, yardımcı maliyet nesnelerinin değiştiği karşılıklı hizmetler tümüyle tanınır.</span><span class="sxs-lookup"><span data-stu-id="5ef53-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="5ef53-470">Sistem, tahsisatların doğru gerçekleştireceği sırayı otomatik olarak belirler.</span><span class="sxs-lookup"><span data-stu-id="5ef53-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="5ef53-471">Bir maliyet nesnesinin bakiyesi tek bir tahsisat tabanı tarafından tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="5ef53-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="5ef53-472">Yeni maliyet nesnesi boyutları arasındaki tahsisatlar ve onların üyeleri desteklenir.</span><span class="sxs-lookup"><span data-stu-id="5ef53-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="5ef53-473">Tahsisatın sırası, maliyet kontrol birimi tarafından kontrol edilir.</span><span class="sxs-lookup"><span data-stu-id="5ef53-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="5ef53-474">[![Karşılıklı yöntemi](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="5ef53-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="5ef53-475">Maliyet tahsisatını tanımla</span><span class="sxs-lookup"><span data-stu-id="5ef53-475">Define the cost allocation</span></span>

<span data-ttu-id="5ef53-476">Bir maliyetin akışını nasıl izleyeceğinize dair basit bir örnek aşağıda verilmiştir,</span><span class="sxs-lookup"><span data-stu-id="5ef53-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="5ef53-477">Maliyet nesnesi CC001 HR, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="5ef53-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="5ef53-478">HR hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5ef53-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ef53-479">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="5ef53-479">Cost object</span></span></th>
<th><span data-ttu-id="5ef53-480">HR hizmetleri</span><span class="sxs-lookup"><span data-stu-id="5ef53-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ef53-481">CC002</span><span class="sxs-lookup"><span data-stu-id="5ef53-481">CC002</span></span></td>
<td><span data-ttu-id="5ef53-482">Finans</span><span class="sxs-lookup"><span data-stu-id="5ef53-482">Finance</span></span></td>
<td><span data-ttu-id="5ef53-483">35</span><span class="sxs-lookup"><span data-stu-id="5ef53-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-484">CC003</span><span class="sxs-lookup"><span data-stu-id="5ef53-484">CC003</span></span></td>
<td><span data-ttu-id="5ef53-485">Montaj</span><span class="sxs-lookup"><span data-stu-id="5ef53-485">Assembly</span></span></td>
<td><span data-ttu-id="5ef53-486">55</span><span class="sxs-lookup"><span data-stu-id="5ef53-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-487">CC004</span><span class="sxs-lookup"><span data-stu-id="5ef53-487">CC004</span></span></td>
<td><span data-ttu-id="5ef53-488">Paketleme</span><span class="sxs-lookup"><span data-stu-id="5ef53-488">Packaging</span></span></td>
<td><span data-ttu-id="5ef53-489">10</span><span class="sxs-lookup"><span data-stu-id="5ef53-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ef53-490">Maliyet nesnesi CC002 Finans, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="5ef53-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="5ef53-491">Finans hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5ef53-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ef53-492">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="5ef53-492">Cost object</span></span></th>
<th><span data-ttu-id="5ef53-493">Finans hizmetleri</span><span class="sxs-lookup"><span data-stu-id="5ef53-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ef53-494">CC003</span><span class="sxs-lookup"><span data-stu-id="5ef53-494">CC003</span></span></td>
<td><span data-ttu-id="5ef53-495">Montaj</span><span class="sxs-lookup"><span data-stu-id="5ef53-495">Assembly</span></span></td>
<td><span data-ttu-id="5ef53-496">65</span><span class="sxs-lookup"><span data-stu-id="5ef53-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-497">CC004</span><span class="sxs-lookup"><span data-stu-id="5ef53-497">CC004</span></span></td>
<td><span data-ttu-id="5ef53-498">Paketleme</span><span class="sxs-lookup"><span data-stu-id="5ef53-498">Packaging</span></span></td>
<td><span data-ttu-id="5ef53-499">35</span><span class="sxs-lookup"><span data-stu-id="5ef53-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ef53-500">Maliyet nesnesi CC003 Derleme, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="5ef53-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="5ef53-501">Derleme hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5ef53-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ef53-502">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="5ef53-502">Cost object</span></span></th>
<th><span data-ttu-id="5ef53-503">Derleme Hizmetleri (saat)</span><span class="sxs-lookup"><span data-stu-id="5ef53-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ef53-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-504">Prod 1</span></span></td>
<td><span data-ttu-id="5ef53-505">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-505">Product 1</span></span></td>
<td><span data-ttu-id="5ef53-506">60</span><span class="sxs-lookup"><span data-stu-id="5ef53-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5ef53-507">Prod 2</span></span></td>
<td><span data-ttu-id="5ef53-508">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="5ef53-508">Product 2</span></span></td>
<td><span data-ttu-id="5ef53-509">20</span><span class="sxs-lookup"><span data-stu-id="5ef53-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ef53-510">Maliyet nesnesi CC004 Ambalajlama, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="5ef53-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="5ef53-511">Ambalajlama hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5ef53-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ef53-512">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="5ef53-512">Cost object</span></span></th>
<th><span data-ttu-id="5ef53-513">Ambalajlama hizmetleri (saat)</span><span class="sxs-lookup"><span data-stu-id="5ef53-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ef53-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-514">Prod 1</span></span></td>
<td><span data-ttu-id="5ef53-515">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-515">Product 1</span></span></td>
<td><span data-ttu-id="5ef53-516">80</span><span class="sxs-lookup"><span data-stu-id="5ef53-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5ef53-517">Prod 2</span></span></td>
<td><span data-ttu-id="5ef53-518">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="5ef53-518">Product 2</span></span></td>
<td><span data-ttu-id="5ef53-519">15</span><span class="sxs-lookup"><span data-stu-id="5ef53-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="5ef53-520">Bir ürünün tükettiği üretim saatleri gibi istatistiki ölçümler, doğrudan kaynak verilerinden alınabilir.</span><span class="sxs-lookup"><span data-stu-id="5ef53-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="5ef53-521">Daha fazla bilgi için, [İstatistiksel ölçüm sağlayıcı şablonu](statistical-measure-provider-template.md#statistical-measure-provider-template) bakın.</span><span class="sxs-lookup"><span data-stu-id="5ef53-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="5ef53-522">Aşağıdaki tablo, İK hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığında ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="5ef53-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ef53-523">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="5ef53-523">Cost object</span></span></th>
<th><span data-ttu-id="5ef53-524">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="5ef53-524">Magnitude</span></span></th>
<th><span data-ttu-id="5ef53-525">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="5ef53-525">Allocation factor</span></span></th>
<th><span data-ttu-id="5ef53-526">Tutar</span><span class="sxs-lookup"><span data-stu-id="5ef53-526">Amount</span></span></th>
<th><span data-ttu-id="5ef53-527">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="5ef53-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ef53-528">CC002</span><span class="sxs-lookup"><span data-stu-id="5ef53-528">CC002</span></span></td>
<td><span data-ttu-id="5ef53-529">Finans</span><span class="sxs-lookup"><span data-stu-id="5ef53-529">Finance</span></span></td>
<td><span data-ttu-id="5ef53-530">35</span><span class="sxs-lookup"><span data-stu-id="5ef53-530">35</span></span></td>
<td><span data-ttu-id="5ef53-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="5ef53-532">175.00</span><span class="sxs-lookup"><span data-stu-id="5ef53-532">175.00</span></span></td>
<td><span data-ttu-id="5ef53-533">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-534">CC003</span><span class="sxs-lookup"><span data-stu-id="5ef53-534">CC003</span></span></td>
<td><span data-ttu-id="5ef53-535">Montaj</span><span class="sxs-lookup"><span data-stu-id="5ef53-535">Assembly</span></span></td>
<td><span data-ttu-id="5ef53-536">55</span><span class="sxs-lookup"><span data-stu-id="5ef53-536">55</span></span></td>
<td><span data-ttu-id="5ef53-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="5ef53-538">275.00</span><span class="sxs-lookup"><span data-stu-id="5ef53-538">275.00</span></span></td>
<td><span data-ttu-id="5ef53-539">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-540">CC004</span><span class="sxs-lookup"><span data-stu-id="5ef53-540">CC004</span></span></td>
<td><span data-ttu-id="5ef53-541">Paketleme</span><span class="sxs-lookup"><span data-stu-id="5ef53-541">Packaging</span></span></td>
<td><span data-ttu-id="5ef53-542">10</span><span class="sxs-lookup"><span data-stu-id="5ef53-542">10</span></span></td>
<td><span data-ttu-id="5ef53-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="5ef53-544">50,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-544">50.00</span></span></td>
<td><span data-ttu-id="5ef53-545">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-546">CC002</span><span class="sxs-lookup"><span data-stu-id="5ef53-546">CC002</span></span></td>
<td><span data-ttu-id="5ef53-547">Finans</span><span class="sxs-lookup"><span data-stu-id="5ef53-547">Finance</span></span></td>
<td><span data-ttu-id="5ef53-548">35</span><span class="sxs-lookup"><span data-stu-id="5ef53-548">35</span></span></td>
<td><span data-ttu-id="5ef53-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="5ef53-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="5ef53-550">436.00</span><span class="sxs-lookup"><span data-stu-id="5ef53-550">436.00</span></span></td>
<td><span data-ttu-id="5ef53-551">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-552">CC003</span><span class="sxs-lookup"><span data-stu-id="5ef53-552">CC003</span></span></td>
<td><span data-ttu-id="5ef53-553">Montaj</span><span class="sxs-lookup"><span data-stu-id="5ef53-553">Assembly</span></span></td>
<td><span data-ttu-id="5ef53-554">55</span><span class="sxs-lookup"><span data-stu-id="5ef53-554">55</span></span></td>
<td><span data-ttu-id="5ef53-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="5ef53-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="5ef53-556">685.14</span><span class="sxs-lookup"><span data-stu-id="5ef53-556">685.14</span></span></td>
<td><span data-ttu-id="5ef53-557">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-558">CC004</span><span class="sxs-lookup"><span data-stu-id="5ef53-558">CC004</span></span></td>
<td><span data-ttu-id="5ef53-559">Paketleme</span><span class="sxs-lookup"><span data-stu-id="5ef53-559">Packaging</span></span></td>
<td><span data-ttu-id="5ef53-560">10</span><span class="sxs-lookup"><span data-stu-id="5ef53-560">10</span></span></td>
<td><span data-ttu-id="5ef53-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="5ef53-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="5ef53-562">124.57</span><span class="sxs-lookup"><span data-stu-id="5ef53-562">124.57</span></span></td>
<td><span data-ttu-id="5ef53-563">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ef53-564">Aşağıdaki tablo, Finans hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="5ef53-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ef53-565">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="5ef53-565">Cost object</span></span></th>
<th><span data-ttu-id="5ef53-566">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="5ef53-566">Magnitude</span></span></th>
<th><span data-ttu-id="5ef53-567">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="5ef53-567">Allocation factor</span></span></th>
<th><span data-ttu-id="5ef53-568">Tutar</span><span class="sxs-lookup"><span data-stu-id="5ef53-568">Amount</span></span></th>
<th><span data-ttu-id="5ef53-569">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="5ef53-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ef53-570">CC003</span><span class="sxs-lookup"><span data-stu-id="5ef53-570">CC003</span></span></td>
<td><span data-ttu-id="5ef53-571">Montaj</span><span class="sxs-lookup"><span data-stu-id="5ef53-571">Assembly</span></span></td>
<td><span data-ttu-id="5ef53-572">65</span><span class="sxs-lookup"><span data-stu-id="5ef53-572">65</span></span></td>
<td><span data-ttu-id="5ef53-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="5ef53-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="5ef53-574">438.75</span><span class="sxs-lookup"><span data-stu-id="5ef53-574">438.75</span></span></td>
<td><span data-ttu-id="5ef53-575">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-576">CC004</span><span class="sxs-lookup"><span data-stu-id="5ef53-576">CC004</span></span></td>
<td><span data-ttu-id="5ef53-577">Paketleme</span><span class="sxs-lookup"><span data-stu-id="5ef53-577">Packaging</span></span></td>
<td><span data-ttu-id="5ef53-578">35</span><span class="sxs-lookup"><span data-stu-id="5ef53-578">35</span></span></td>
<td><span data-ttu-id="5ef53-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="5ef53-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="5ef53-580">236.25</span><span class="sxs-lookup"><span data-stu-id="5ef53-580">236.25</span></span></td>
<td><span data-ttu-id="5ef53-581">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-582">CC003</span><span class="sxs-lookup"><span data-stu-id="5ef53-582">CC003</span></span></td>
<td><span data-ttu-id="5ef53-583">Montaj</span><span class="sxs-lookup"><span data-stu-id="5ef53-583">Assembly</span></span></td>
<td><span data-ttu-id="5ef53-584">65</span><span class="sxs-lookup"><span data-stu-id="5ef53-584">65</span></span></td>
<td><span data-ttu-id="5ef53-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="5ef53-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="5ef53-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="5ef53-586">5,297.69</span></span></td>
<td><span data-ttu-id="5ef53-587">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-588">CC004</span><span class="sxs-lookup"><span data-stu-id="5ef53-588">CC004</span></span></td>
<td><span data-ttu-id="5ef53-589">Paketleme</span><span class="sxs-lookup"><span data-stu-id="5ef53-589">Packaging</span></span></td>
<td><span data-ttu-id="5ef53-590">35</span><span class="sxs-lookup"><span data-stu-id="5ef53-590">35</span></span></td>
<td><span data-ttu-id="5ef53-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="5ef53-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="5ef53-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="5ef53-592">2,852.60</span></span></td>
<td><span data-ttu-id="5ef53-593">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ef53-594">Aşağıdaki tablo, Derleme hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="5ef53-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ef53-595">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="5ef53-595">Cost object</span></span></th>
<th><span data-ttu-id="5ef53-596">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="5ef53-596">Magnitude</span></span></th>
<th><span data-ttu-id="5ef53-597">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="5ef53-597">Allocation factor</span></span></th>
<th><span data-ttu-id="5ef53-598">Tutar</span><span class="sxs-lookup"><span data-stu-id="5ef53-598">Amount</span></span></th>
<th><span data-ttu-id="5ef53-599">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="5ef53-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ef53-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-600">Prod 1</span></span></td>
<td><span data-ttu-id="5ef53-601">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-601">Product 1</span></span></td>
<td><span data-ttu-id="5ef53-602">60</span><span class="sxs-lookup"><span data-stu-id="5ef53-602">60</span></span></td>
<td><span data-ttu-id="5ef53-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="5ef53-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="5ef53-604">535.31</span><span class="sxs-lookup"><span data-stu-id="5ef53-604">535.31</span></span></td>
<td><span data-ttu-id="5ef53-605">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5ef53-606">Prod 2</span></span></td>
<td><span data-ttu-id="5ef53-607">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="5ef53-607">Product 2</span></span></td>
<td><span data-ttu-id="5ef53-608">20</span><span class="sxs-lookup"><span data-stu-id="5ef53-608">20</span></span></td>
<td><span data-ttu-id="5ef53-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="5ef53-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="5ef53-610">178.44</span><span class="sxs-lookup"><span data-stu-id="5ef53-610">178.44</span></span></td>
<td><span data-ttu-id="5ef53-611">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-612">Prod 1</span></span></td>
<td><span data-ttu-id="5ef53-613">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-613">Product 1</span></span></td>
<td><span data-ttu-id="5ef53-614">60</span><span class="sxs-lookup"><span data-stu-id="5ef53-614">60</span></span></td>
<td><span data-ttu-id="5ef53-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="5ef53-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="5ef53-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="5ef53-616">4,487.12</span></span></td>
<td><span data-ttu-id="5ef53-617">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5ef53-618">Prod 2</span></span></td>
<td><span data-ttu-id="5ef53-619">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="5ef53-619">Product 2</span></span></td>
<td><span data-ttu-id="5ef53-620">20</span><span class="sxs-lookup"><span data-stu-id="5ef53-620">20</span></span></td>
<td><span data-ttu-id="5ef53-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="5ef53-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="5ef53-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="5ef53-622">1,495.71</span></span></td>
<td><span data-ttu-id="5ef53-623">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ef53-624">Aşağıdaki tablo, Paketleme hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="5ef53-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ef53-625">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="5ef53-625">Cost object</span></span></th>
<th><span data-ttu-id="5ef53-626">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="5ef53-626">Magnitude</span></span></th>
<th><span data-ttu-id="5ef53-627">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="5ef53-627">Allocation factor</span></span></th>
<th><span data-ttu-id="5ef53-628">Tutar</span><span class="sxs-lookup"><span data-stu-id="5ef53-628">Amount</span></span></th>
<th><span data-ttu-id="5ef53-629">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="5ef53-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ef53-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-630">Prod 1</span></span></td>
<td><span data-ttu-id="5ef53-631">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-631">Product 1</span></span></td>
<td><span data-ttu-id="5ef53-632">80</span><span class="sxs-lookup"><span data-stu-id="5ef53-632">80</span></span></td>
<td><span data-ttu-id="5ef53-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="5ef53-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="5ef53-634">241.05</span><span class="sxs-lookup"><span data-stu-id="5ef53-634">241.05</span></span></td>
<td><span data-ttu-id="5ef53-635">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5ef53-636">Prod 2</span></span></td>
<td><span data-ttu-id="5ef53-637">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="5ef53-637">Product 2</span></span></td>
<td><span data-ttu-id="5ef53-638">15</span><span class="sxs-lookup"><span data-stu-id="5ef53-638">15</span></span></td>
<td><span data-ttu-id="5ef53-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="5ef53-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="5ef53-640">45.20</span><span class="sxs-lookup"><span data-stu-id="5ef53-640">45.20</span></span></td>
<td><span data-ttu-id="5ef53-641">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-642">Prod 1</span></span></td>
<td><span data-ttu-id="5ef53-643">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-643">Product 1</span></span></td>
<td><span data-ttu-id="5ef53-644">80</span><span class="sxs-lookup"><span data-stu-id="5ef53-644">80</span></span></td>
<td><span data-ttu-id="5ef53-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="5ef53-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="5ef53-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="5ef53-646">2,507.09</span></span></td>
<td><span data-ttu-id="5ef53-647">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5ef53-648">Prod 2</span></span></td>
<td><span data-ttu-id="5ef53-649">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="5ef53-649">Product 2</span></span></td>
<td><span data-ttu-id="5ef53-650">15</span><span class="sxs-lookup"><span data-stu-id="5ef53-650">15</span></span></td>
<td><span data-ttu-id="5ef53-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="5ef53-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="5ef53-652">470.08</span><span class="sxs-lookup"><span data-stu-id="5ef53-652">470.08</span></span></td>
<td><span data-ttu-id="5ef53-653">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="5ef53-654">Günlük girişleri (maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="5ef53-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5ef53-655">Günlük</span><span class="sxs-lookup"><span data-stu-id="5ef53-655">Journal</span></span></th>
<th><span data-ttu-id="5ef53-656">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="5ef53-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5ef53-657">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="5ef53-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5ef53-658">Sürüm</span><span class="sxs-lookup"><span data-stu-id="5ef53-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ef53-659">00004</span><span class="sxs-lookup"><span data-stu-id="5ef53-659">00004</span></span></td>
<td><span data-ttu-id="5ef53-660">Maliyet tahsisatı günlüğü</span><span class="sxs-lookup"><span data-stu-id="5ef53-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="5ef53-661">Mali</span><span class="sxs-lookup"><span data-stu-id="5ef53-661">Fiscal</span></span></td>
<td><span data-ttu-id="5ef53-662">2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-662">2017</span></span></td>
<td><span data-ttu-id="5ef53-663">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-663">Period 1</span></span></td>
<td><span data-ttu-id="5ef53-664">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="5ef53-665">Günlük satırları</span><span class="sxs-lookup"><span data-stu-id="5ef53-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5ef53-666">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="5ef53-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5ef53-667">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="5ef53-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5ef53-668">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="5ef53-668">Cost element</span></span></th>
<th><span data-ttu-id="5ef53-669">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="5ef53-669">Cost behavior</span></span></th>
<th><span data-ttu-id="5ef53-670">Tutar</span><span class="sxs-lookup"><span data-stu-id="5ef53-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ef53-671">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ef53-672">CC001</span><span class="sxs-lookup"><span data-stu-id="5ef53-672">CC001</span></span></td>
<td><span data-ttu-id="5ef53-673">İK</span><span class="sxs-lookup"><span data-stu-id="5ef53-673">HR</span></span></td>
<td><span data-ttu-id="5ef53-674">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-674">10001</span></span></td>
<td><span data-ttu-id="5ef53-675">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-675">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-676">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-676">Fixed cost</span></span></td>
<td><span data-ttu-id="5ef53-677">500.00</span><span class="sxs-lookup"><span data-stu-id="5ef53-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-678">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ef53-679">CC001</span><span class="sxs-lookup"><span data-stu-id="5ef53-679">CC001</span></span></td>
<td><span data-ttu-id="5ef53-680">İK</span><span class="sxs-lookup"><span data-stu-id="5ef53-680">HR</span></span></td>
<td><span data-ttu-id="5ef53-681">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-681">10001</span></span></td>
<td><span data-ttu-id="5ef53-682">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-682">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-683">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-683">Variable cost</span></span></td>
<td><span data-ttu-id="5ef53-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="5ef53-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-685">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ef53-686">CC002</span><span class="sxs-lookup"><span data-stu-id="5ef53-686">CC002</span></span></td>
<td><span data-ttu-id="5ef53-687">Finans</span><span class="sxs-lookup"><span data-stu-id="5ef53-687">Finance</span></span></td>
<td><span data-ttu-id="5ef53-688">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-688">10001</span></span></td>
<td><span data-ttu-id="5ef53-689">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-689">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-690">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-690">Fixed cost</span></span></td>
<td><span data-ttu-id="5ef53-691">675.00</span><span class="sxs-lookup"><span data-stu-id="5ef53-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-692">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ef53-693">CC002</span><span class="sxs-lookup"><span data-stu-id="5ef53-693">CC002</span></span></td>
<td><span data-ttu-id="5ef53-694">Finans</span><span class="sxs-lookup"><span data-stu-id="5ef53-694">Finance</span></span></td>
<td><span data-ttu-id="5ef53-695">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-695">10001</span></span></td>
<td><span data-ttu-id="5ef53-696">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-696">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-697">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-697">Variable cost</span></span></td>
<td><span data-ttu-id="5ef53-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="5ef53-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-699">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ef53-700">CC003</span><span class="sxs-lookup"><span data-stu-id="5ef53-700">CC003</span></span></td>
<td><span data-ttu-id="5ef53-701">Montaj</span><span class="sxs-lookup"><span data-stu-id="5ef53-701">Assembly</span></span></td>
<td><span data-ttu-id="5ef53-702">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-702">10001</span></span></td>
<td><span data-ttu-id="5ef53-703">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-703">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-704">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-704">Fixed cost</span></span></td>
<td><span data-ttu-id="5ef53-705">713.75</span><span class="sxs-lookup"><span data-stu-id="5ef53-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-706">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ef53-707">CC003</span><span class="sxs-lookup"><span data-stu-id="5ef53-707">CC003</span></span></td>
<td><span data-ttu-id="5ef53-708">Montaj</span><span class="sxs-lookup"><span data-stu-id="5ef53-708">Assembly</span></span></td>
<td><span data-ttu-id="5ef53-709">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-709">10001</span></span></td>
<td><span data-ttu-id="5ef53-710">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-710">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-711">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-711">Variable cost</span></span></td>
<td><span data-ttu-id="5ef53-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="5ef53-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-713">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ef53-714">CC003</span><span class="sxs-lookup"><span data-stu-id="5ef53-714">CC003</span></span></td>
<td><span data-ttu-id="5ef53-715">Paketleme</span><span class="sxs-lookup"><span data-stu-id="5ef53-715">Packaging</span></span></td>
<td><span data-ttu-id="5ef53-716">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-716">10001</span></span></td>
<td><span data-ttu-id="5ef53-717">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-717">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-718">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-718">Fixed cost</span></span></td>
<td><span data-ttu-id="5ef53-719">286.25</span><span class="sxs-lookup"><span data-stu-id="5ef53-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-720">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ef53-721">CC003</span><span class="sxs-lookup"><span data-stu-id="5ef53-721">CC003</span></span></td>
<td><span data-ttu-id="5ef53-722">Paketleme</span><span class="sxs-lookup"><span data-stu-id="5ef53-722">Packaging</span></span></td>
<td><span data-ttu-id="5ef53-723">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-723">10001</span></span></td>
<td><span data-ttu-id="5ef53-724">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-724">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-725">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-725">Variable cost</span></span></td>
<td><span data-ttu-id="5ef53-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="5ef53-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-727">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ef53-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-728">Prod 1</span></span></td>
<td><span data-ttu-id="5ef53-729">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-729">Product 1</span></span></td>
<td><span data-ttu-id="5ef53-730">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-730">10001</span></span></td>
<td><span data-ttu-id="5ef53-731">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-731">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-732">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-732">Fixed cost</span></span></td>
<td><span data-ttu-id="5ef53-733">776.36</span><span class="sxs-lookup"><span data-stu-id="5ef53-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-734">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ef53-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-735">Prod 1</span></span></td>
<td><span data-ttu-id="5ef53-736">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-736">Product 1</span></span></td>
<td><span data-ttu-id="5ef53-737">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-737">10001</span></span></td>
<td><span data-ttu-id="5ef53-738">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-738">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-739">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-739">Variable cost</span></span></td>
<td><span data-ttu-id="5ef53-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="5ef53-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-741">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ef53-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5ef53-742">Prod 2</span></span></td>
<td><span data-ttu-id="5ef53-743">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-743">Product 1</span></span></td>
<td><span data-ttu-id="5ef53-744">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-744">10001</span></span></td>
<td><span data-ttu-id="5ef53-745">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-745">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-746">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-746">Fixed cost</span></span></td>
<td><span data-ttu-id="5ef53-747">223.64</span><span class="sxs-lookup"><span data-stu-id="5ef53-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-748">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ef53-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5ef53-749">Prod 2</span></span></td>
<td><span data-ttu-id="5ef53-750">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-750">Product 1</span></span></td>
<td><span data-ttu-id="5ef53-751">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-751">10001</span></span></td>
<td><span data-ttu-id="5ef53-752">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-752">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-753">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-753">Variable cost</span></span></td>
<td><span data-ttu-id="5ef53-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="5ef53-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5ef53-755">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="5ef53-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ef53-756">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="5ef53-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5ef53-757">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="5ef53-757">Cost element</span></span></th>
<th><span data-ttu-id="5ef53-758">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="5ef53-758">Cost behavior</span></span></th>
<th><span data-ttu-id="5ef53-759">Tutar</span><span class="sxs-lookup"><span data-stu-id="5ef53-759">Amount</span></span></th>
<th><span data-ttu-id="5ef53-760">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="5ef53-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ef53-761">CC001</span><span class="sxs-lookup"><span data-stu-id="5ef53-761">CC001</span></span></td>
<td><span data-ttu-id="5ef53-762">İK</span><span class="sxs-lookup"><span data-stu-id="5ef53-762">HR</span></span></td>
<td><span data-ttu-id="5ef53-763">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-763">10001</span></span></td>
<td><span data-ttu-id="5ef53-764">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-764">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-765">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-765">Fixed cost</span></span></td>
<td><span data-ttu-id="5ef53-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="5ef53-766">-500.00</span></span></td>
<td><span data-ttu-id="5ef53-767">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-768">CC002</span><span class="sxs-lookup"><span data-stu-id="5ef53-768">CC002</span></span></td>
<td><span data-ttu-id="5ef53-769">Finans</span><span class="sxs-lookup"><span data-stu-id="5ef53-769">Finance</span></span></td>
<td><span data-ttu-id="5ef53-770">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-770">10001</span></span></td>
<td><span data-ttu-id="5ef53-771">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-771">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-772">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-772">Fixed cost</span></span></td>
<td><span data-ttu-id="5ef53-773">175.00</span><span class="sxs-lookup"><span data-stu-id="5ef53-773">175.00</span></span></td>
<td><span data-ttu-id="5ef53-774">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-775">CC003</span><span class="sxs-lookup"><span data-stu-id="5ef53-775">CC003</span></span></td>
<td><span data-ttu-id="5ef53-776">Montaj</span><span class="sxs-lookup"><span data-stu-id="5ef53-776">Assembly</span></span></td>
<td><span data-ttu-id="5ef53-777">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-777">10001</span></span></td>
<td><span data-ttu-id="5ef53-778">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-778">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-779">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-779">Fixed cost</span></span></td>
<td><span data-ttu-id="5ef53-780">275.00</span><span class="sxs-lookup"><span data-stu-id="5ef53-780">275.00</span></span></td>
<td><span data-ttu-id="5ef53-781">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-782">CC004</span><span class="sxs-lookup"><span data-stu-id="5ef53-782">CC004</span></span></td>
<td><span data-ttu-id="5ef53-783">Paketleme</span><span class="sxs-lookup"><span data-stu-id="5ef53-783">Packaging</span></span></td>
<td><span data-ttu-id="5ef53-784">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-784">10001</span></span></td>
<td><span data-ttu-id="5ef53-785">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-785">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-786">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-786">Fixed cost</span></span></td>
<td><span data-ttu-id="5ef53-787">50,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-787">50,00</span></span></td>
<td><span data-ttu-id="5ef53-788">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-789">CC001</span><span class="sxs-lookup"><span data-stu-id="5ef53-789">CC001</span></span></td>
<td><span data-ttu-id="5ef53-790">İK</span><span class="sxs-lookup"><span data-stu-id="5ef53-790">HR</span></span></td>
<td><span data-ttu-id="5ef53-791">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-791">10001</span></span></td>
<td><span data-ttu-id="5ef53-792">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-792">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-793">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-793">Variable cost</span></span></td>
<td><span data-ttu-id="5ef53-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="5ef53-794">-1,245.71</span></span></td>
<td><span data-ttu-id="5ef53-795">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-796">CC002</span><span class="sxs-lookup"><span data-stu-id="5ef53-796">CC002</span></span></td>
<td><span data-ttu-id="5ef53-797">Finans</span><span class="sxs-lookup"><span data-stu-id="5ef53-797">Finance</span></span></td>
<td><span data-ttu-id="5ef53-798">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-798">10001</span></span></td>
<td><span data-ttu-id="5ef53-799">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-799">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-800">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-800">Variable cost</span></span></td>
<td><span data-ttu-id="5ef53-801">436.00</span><span class="sxs-lookup"><span data-stu-id="5ef53-801">436.00</span></span></td>
<td><span data-ttu-id="5ef53-802">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-803">CC003</span><span class="sxs-lookup"><span data-stu-id="5ef53-803">CC003</span></span></td>
<td><span data-ttu-id="5ef53-804">Montaj</span><span class="sxs-lookup"><span data-stu-id="5ef53-804">Assembly</span></span></td>
<td><span data-ttu-id="5ef53-805">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-805">10001</span></span></td>
<td><span data-ttu-id="5ef53-806">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-806">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-807">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-807">Variable cost</span></span></td>
<td><span data-ttu-id="5ef53-808">685.14</span><span class="sxs-lookup"><span data-stu-id="5ef53-808">685.14</span></span></td>
<td><span data-ttu-id="5ef53-809">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-810">CC004</span><span class="sxs-lookup"><span data-stu-id="5ef53-810">CC004</span></span></td>
<td><span data-ttu-id="5ef53-811">Paketleme</span><span class="sxs-lookup"><span data-stu-id="5ef53-811">Packaging</span></span></td>
<td><span data-ttu-id="5ef53-812">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-812">10001</span></span></td>
<td><span data-ttu-id="5ef53-813">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-813">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-814">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-814">Variable cost</span></span></td>
<td><span data-ttu-id="5ef53-815">124.57</span><span class="sxs-lookup"><span data-stu-id="5ef53-815">124.57</span></span></td>
<td><span data-ttu-id="5ef53-816">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-817">CC002</span><span class="sxs-lookup"><span data-stu-id="5ef53-817">CC002</span></span></td>
<td><span data-ttu-id="5ef53-818">Finans</span><span class="sxs-lookup"><span data-stu-id="5ef53-818">Finance</span></span></td>
<td><span data-ttu-id="5ef53-819">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-819">10001</span></span></td>
<td><span data-ttu-id="5ef53-820">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-820">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-821">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-821">Fixed cost</span></span></td>
<td><span data-ttu-id="5ef53-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-822">-675.00</span></span></td>
<td><span data-ttu-id="5ef53-823">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-824">CC003</span><span class="sxs-lookup"><span data-stu-id="5ef53-824">CC003</span></span></td>
<td><span data-ttu-id="5ef53-825">Montaj</span><span class="sxs-lookup"><span data-stu-id="5ef53-825">Assembly</span></span></td>
<td><span data-ttu-id="5ef53-826">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-826">10001</span></span></td>
<td><span data-ttu-id="5ef53-827">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-827">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-828">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-828">Fixed cost</span></span></td>
<td><span data-ttu-id="5ef53-829">438.75</span><span class="sxs-lookup"><span data-stu-id="5ef53-829">438.75</span></span></td>
<td><span data-ttu-id="5ef53-830">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-831">CC004</span><span class="sxs-lookup"><span data-stu-id="5ef53-831">CC004</span></span></td>
<td><span data-ttu-id="5ef53-832">Paketleme</span><span class="sxs-lookup"><span data-stu-id="5ef53-832">Packaging</span></span></td>
<td><span data-ttu-id="5ef53-833">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-833">10001</span></span></td>
<td><span data-ttu-id="5ef53-834">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-834">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-835">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-835">Fixed cost</span></span></td>
<td><span data-ttu-id="5ef53-836">236.25</span><span class="sxs-lookup"><span data-stu-id="5ef53-836">236.25</span></span></td>
<td><span data-ttu-id="5ef53-837">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-838">CC002</span><span class="sxs-lookup"><span data-stu-id="5ef53-838">CC002</span></span></td>
<td><span data-ttu-id="5ef53-839">Finans</span><span class="sxs-lookup"><span data-stu-id="5ef53-839">Finance</span></span></td>
<td><span data-ttu-id="5ef53-840">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-840">10001</span></span></td>
<td><span data-ttu-id="5ef53-841">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-841">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-842">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-842">Variable cost</span></span></td>
<td><span data-ttu-id="5ef53-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="5ef53-843">-8,150.29</span></span></td>
<td><span data-ttu-id="5ef53-844">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-845">CC003</span><span class="sxs-lookup"><span data-stu-id="5ef53-845">CC003</span></span></td>
<td><span data-ttu-id="5ef53-846">Montaj</span><span class="sxs-lookup"><span data-stu-id="5ef53-846">Assembly</span></span></td>
<td><span data-ttu-id="5ef53-847">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-847">10001</span></span></td>
<td><span data-ttu-id="5ef53-848">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-848">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-849">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-849">Variable cost</span></span></td>
<td><span data-ttu-id="5ef53-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="5ef53-850">5,297.69</span></span></td>
<td><span data-ttu-id="5ef53-851">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-852">CC004</span><span class="sxs-lookup"><span data-stu-id="5ef53-852">CC004</span></span></td>
<td><span data-ttu-id="5ef53-853">Paketleme</span><span class="sxs-lookup"><span data-stu-id="5ef53-853">Packaging</span></span></td>
<td><span data-ttu-id="5ef53-854">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-854">10001</span></span></td>
<td><span data-ttu-id="5ef53-855">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-855">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-856">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-856">Variable cost</span></span></td>
<td><span data-ttu-id="5ef53-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="5ef53-857">2,852.60</span></span></td>
<td><span data-ttu-id="5ef53-858">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-859">CC003</span><span class="sxs-lookup"><span data-stu-id="5ef53-859">CC003</span></span></td>
<td><span data-ttu-id="5ef53-860">Montaj</span><span class="sxs-lookup"><span data-stu-id="5ef53-860">Assembly</span></span></td>
<td><span data-ttu-id="5ef53-861">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-861">10001</span></span></td>
<td><span data-ttu-id="5ef53-862">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-862">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-863">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-863">Fixed cost</span></span></td>
<td><span data-ttu-id="5ef53-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="5ef53-864">-713.75</span></span></td>
<td><span data-ttu-id="5ef53-865">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-866">Prod 1</span></span></td>
<td><span data-ttu-id="5ef53-867">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-867">Product 1</span></span></td>
<td><span data-ttu-id="5ef53-868">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-868">10001</span></span></td>
<td><span data-ttu-id="5ef53-869">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-869">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-870">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-870">Fixed cost</span></span></td>
<td><span data-ttu-id="5ef53-871">535.31</span><span class="sxs-lookup"><span data-stu-id="5ef53-871">535.31</span></span></td>
<td><span data-ttu-id="5ef53-872">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5ef53-873">Prod 2</span></span></td>
<td><span data-ttu-id="5ef53-874">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="5ef53-874">Product 2</span></span></td>
<td><span data-ttu-id="5ef53-875">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-875">10001</span></span></td>
<td><span data-ttu-id="5ef53-876">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-876">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-877">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-877">Fixed cost</span></span></td>
<td><span data-ttu-id="5ef53-878">178.44</span><span class="sxs-lookup"><span data-stu-id="5ef53-878">178.44</span></span></td>
<td><span data-ttu-id="5ef53-879">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-880">CC003</span><span class="sxs-lookup"><span data-stu-id="5ef53-880">CC003</span></span></td>
<td><span data-ttu-id="5ef53-881">Montaj</span><span class="sxs-lookup"><span data-stu-id="5ef53-881">Assembly</span></span></td>
<td><span data-ttu-id="5ef53-882">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-882">10001</span></span></td>
<td><span data-ttu-id="5ef53-883">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-883">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-884">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-884">Variable cost</span></span></td>
<td><span data-ttu-id="5ef53-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="5ef53-885">-5,982.83</span></span></td>
<td><span data-ttu-id="5ef53-886">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-887">Prod 1</span></span></td>
<td><span data-ttu-id="5ef53-888">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-888">Product 1</span></span></td>
<td><span data-ttu-id="5ef53-889">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-889">10001</span></span></td>
<td><span data-ttu-id="5ef53-890">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-890">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-891">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-891">Variable cost</span></span></td>
<td><span data-ttu-id="5ef53-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="5ef53-892">4,487.12</span></span></td>
<td><span data-ttu-id="5ef53-893">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5ef53-894">Prod 2</span></span></td>
<td><span data-ttu-id="5ef53-895">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="5ef53-895">Product 2</span></span></td>
<td><span data-ttu-id="5ef53-896">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-896">10001</span></span></td>
<td><span data-ttu-id="5ef53-897">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-897">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-898">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-898">Variable cost</span></span></td>
<td><span data-ttu-id="5ef53-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="5ef53-899">1,495.71</span></span></td>
<td><span data-ttu-id="5ef53-900">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-901">CC003</span><span class="sxs-lookup"><span data-stu-id="5ef53-901">CC003</span></span></td>
<td><span data-ttu-id="5ef53-902">Montaj</span><span class="sxs-lookup"><span data-stu-id="5ef53-902">Assembly</span></span></td>
<td><span data-ttu-id="5ef53-903">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-903">10001</span></span></td>
<td><span data-ttu-id="5ef53-904">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-904">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-905">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-905">Fixed cost</span></span></td>
<td><span data-ttu-id="5ef53-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="5ef53-906">-286.25</span></span></td>
<td><span data-ttu-id="5ef53-907">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-908">Prod 1</span></span></td>
<td><span data-ttu-id="5ef53-909">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-909">Product 1</span></span></td>
<td><span data-ttu-id="5ef53-910">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-910">10001</span></span></td>
<td><span data-ttu-id="5ef53-911">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-911">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-912">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-912">Fixed cost</span></span></td>
<td><span data-ttu-id="5ef53-913">241.05</span><span class="sxs-lookup"><span data-stu-id="5ef53-913">241.05</span></span></td>
<td><span data-ttu-id="5ef53-914">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5ef53-915">Prod 2</span></span></td>
<td><span data-ttu-id="5ef53-916">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="5ef53-916">Product 2</span></span></td>
<td><span data-ttu-id="5ef53-917">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-917">10001</span></span></td>
<td><span data-ttu-id="5ef53-918">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-918">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-919">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-919">Fixed cost</span></span></td>
<td><span data-ttu-id="5ef53-920">45.20</span><span class="sxs-lookup"><span data-stu-id="5ef53-920">45.20</span></span></td>
<td><span data-ttu-id="5ef53-921">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-922">CC003</span><span class="sxs-lookup"><span data-stu-id="5ef53-922">CC003</span></span></td>
<td><span data-ttu-id="5ef53-923">Montaj</span><span class="sxs-lookup"><span data-stu-id="5ef53-923">Assembly</span></span></td>
<td><span data-ttu-id="5ef53-924">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-924">10001</span></span></td>
<td><span data-ttu-id="5ef53-925">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-925">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-926">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-926">Variable cost</span></span></td>
<td><span data-ttu-id="5ef53-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="5ef53-927">-2,977.17</span></span></td>
<td><span data-ttu-id="5ef53-928">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-929">Prod 1</span></span></td>
<td><span data-ttu-id="5ef53-930">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-930">Product 1</span></span></td>
<td><span data-ttu-id="5ef53-931">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-931">10001</span></span></td>
<td><span data-ttu-id="5ef53-932">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-932">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-933">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-933">Variable cost</span></span></td>
<td><span data-ttu-id="5ef53-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="5ef53-934">2,507.09</span></span></td>
<td><span data-ttu-id="5ef53-935">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ef53-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5ef53-936">Prod 2</span></span></td>
<td><span data-ttu-id="5ef53-937">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="5ef53-937">Product 2</span></span></td>
<td><span data-ttu-id="5ef53-938">10001</span><span class="sxs-lookup"><span data-stu-id="5ef53-938">10001</span></span></td>
<td><span data-ttu-id="5ef53-939">Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-939">Electricity</span></span></td>
<td><span data-ttu-id="5ef53-940">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-940">Variable cost</span></span></td>
<td><span data-ttu-id="5ef53-941">470.08</span><span class="sxs-lookup"><span data-stu-id="5ef53-941">470.08</span></span></td>
<td><span data-ttu-id="5ef53-942">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="5ef53-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="5ef53-943">Sonuç</span><span class="sxs-lookup"><span data-stu-id="5ef53-943">Conclusion</span></span>
<span data-ttu-id="5ef53-944">Mali muhasebede, Elektrik için 10.000,00 maliyet bir sözde maliyet merkezi kimliğine nakledilmiştir.</span><span class="sxs-lookup"><span data-stu-id="5ef53-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="5ef53-945">Bu nedenle, maliyet muhasebecileri bu maliyetin tahsis edilmesi gerektiğini bilirler.</span><span class="sxs-lookup"><span data-stu-id="5ef53-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="5ef53-946">Maliyet muhasebesinde, maliyetler kuruluş birimleri ve seviyeleri arasında, uygulanan kural ve ilkelere dayalı olarak akar.</span><span class="sxs-lookup"><span data-stu-id="5ef53-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="5ef53-947">Her maliyet, maliyetlerin tahsisatı için en iyi değerlendirmeyi sağlayan bir tahsisat tabanı ile ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="5ef53-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="5ef53-948">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="5ef53-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="5ef53-949">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="5ef53-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="5ef53-950">Toplam</span><span class="sxs-lookup"><span data-stu-id="5ef53-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="5ef53-951">CC099</span><span class="sxs-lookup"><span data-stu-id="5ef53-951">CC099</span></span></th>
<th><span data-ttu-id="5ef53-952">CC001</span><span class="sxs-lookup"><span data-stu-id="5ef53-952">CC001</span></span></th>
<th><span data-ttu-id="5ef53-953">CC002</span><span class="sxs-lookup"><span data-stu-id="5ef53-953">CC002</span></span></th>
<th><span data-ttu-id="5ef53-954">CC003</span><span class="sxs-lookup"><span data-stu-id="5ef53-954">CC003</span></span></th>
<th><span data-ttu-id="5ef53-955">CC004</span><span class="sxs-lookup"><span data-stu-id="5ef53-955">CC004</span></span></th>
<th><span data-ttu-id="5ef53-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-956">Proj 1</span></span></th>
<th><span data-ttu-id="5ef53-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="5ef53-957">Proj 2</span></span></th>
<th><span data-ttu-id="5ef53-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="5ef53-958">Prod 1</span></span></th>
<th><span data-ttu-id="5ef53-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="5ef53-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="5ef53-960">10001 Elektrik</span><span class="sxs-lookup"><span data-stu-id="5ef53-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ef53-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="5ef53-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ef53-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="5ef53-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ef53-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="5ef53-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ef53-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="5ef53-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="5ef53-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="5ef53-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ef53-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="5ef53-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ef53-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="5ef53-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ef53-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="5ef53-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ef53-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="5ef53-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="5ef53-970">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="5ef53-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ef53-971">0,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="5ef53-972">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ef53-973">0,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ef53-974">0,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ef53-975">0,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ef53-976">0,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ef53-977">0,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="5ef53-978">776.36</span><span class="sxs-lookup"><span data-stu-id="5ef53-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ef53-979">223.64</span><span class="sxs-lookup"><span data-stu-id="5ef53-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ef53-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="5ef53-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="5ef53-981">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="5ef53-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ef53-982">000</span><span class="sxs-lookup"><span data-stu-id="5ef53-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ef53-983">0,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ef53-984">0,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ef53-985">0,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ef53-986">0,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ef53-987">30.00</span><span class="sxs-lookup"><span data-stu-id="5ef53-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ef53-988">10,00</span><span class="sxs-lookup"><span data-stu-id="5ef53-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ef53-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="5ef53-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ef53-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="5ef53-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ef53-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="5ef53-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="5ef53-992">Bu konu, birincil maliyet öğesi, 10001 Elektrik'in maliyet nesneleri arasında nasıl aktığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5ef53-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="5ef53-993">Bu nedenle, bu genel gider maliyeti kuruluşun en düşük seviyesine tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="5ef53-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="5ef53-994">Başka bir deyişle, maliyet en alt düzeydeki maliyet nesnelerine aittir.</span><span class="sxs-lookup"><span data-stu-id="5ef53-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="5ef53-995">Maliyetin, maliyet nesneleri arasında görsel bir akışına ihtiyacınız varsa, maliyetin akışını görselleştirmek için maliyet toplamı ilke kurallarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5ef53-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="5ef53-996">Daha fazla bilgi için bkz. [Maliyet yuvarlama ilkesi ve genel gider hesaplaması](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="5ef53-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]