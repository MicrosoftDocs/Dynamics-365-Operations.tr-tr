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
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: d60248f2bd6774b2e9afdb3632b6eb31d67349ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009530"
---
# <a name="overhead-calculation"></a><span data-ttu-id="6de04-103">Genel gider hesaplaması</span><span class="sxs-lookup"><span data-stu-id="6de04-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6de04-104">Bu konu, genel gider maliyetlerinin hesaplanması için tipik işlemleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="6de04-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="6de04-105">Terim tanımı</span><span class="sxs-lookup"><span data-stu-id="6de04-105">Term definition</span></span>
---------------

<span data-ttu-id="6de04-106">Genel gider maliyetleri bir işletmenin çalışması için normalde uygulanan, ancak doğrudan herhangi bir özel iş, faaliyet, ürün veya hizmete ilişkilendirilmemiş olan maliyetlerdir.</span><span class="sxs-lookup"><span data-stu-id="6de04-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="6de04-107">Genel gider maliyetleri kar sağlama faaliyetlerinin oluşturulması için kritik destek sağlar.</span><span class="sxs-lookup"><span data-stu-id="6de04-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="6de04-108">Aşağıda bazı genel gider örnekleri verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="6de04-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="6de04-109">Kira</span><span class="sxs-lookup"><span data-stu-id="6de04-109">Rent</span></span>
-   <span data-ttu-id="6de04-110">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-110">Electricity</span></span>
-   <span data-ttu-id="6de04-111">Yönetim maaşları</span><span class="sxs-lookup"><span data-stu-id="6de04-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="6de04-112">Genel gider hesaplaması genel bakış</span><span class="sxs-lookup"><span data-stu-id="6de04-112">Overhead calculation overview</span></span>
<span data-ttu-id="6de04-113">Genel gider hesaplama, maliyet muhasebesi ilkelerini doğru sırayla çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="6de04-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="6de04-114">Maliyet muhasebesi ilkeleri değiştiyse veya belirli hatalar algılandıysa, genel gider hesaplamasını aynı mali dönem için birden fazla kez yürütebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6de04-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="6de04-115">Her genel gider hesaplaması depolanır ve önceki sürümlerdeki hesaplamaları kıyaslamanıza olanak sağlayan, benzersiz bir sürüm kimliğine sahip olur.</span><span class="sxs-lookup"><span data-stu-id="6de04-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="6de04-116">Genel gider hesaplamasının oluşturduğu maliyet girişleri bir muhasebe tarihi alır.</span><span class="sxs-lookup"><span data-stu-id="6de04-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="6de04-117">Bu muhasebe tarihi, hesaplamada kullanılan mali dönemin bitiş tarihiyle eşleşir.</span><span class="sxs-lookup"><span data-stu-id="6de04-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="6de04-118">Benzersiz sürüm kimliği aşağıdaki öğelerden oluşur:</span><span class="sxs-lookup"><span data-stu-id="6de04-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="6de04-119">Sürüm türü</span><span class="sxs-lookup"><span data-stu-id="6de04-119">Version type</span></span>
-   <span data-ttu-id="6de04-120">Tarih ve saat</span><span class="sxs-lookup"><span data-stu-id="6de04-120">Date and time</span></span>
-   <span data-ttu-id="6de04-121">Maliyet muhasebesi defteri</span><span class="sxs-lookup"><span data-stu-id="6de04-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="6de04-122">Mali yıl</span><span class="sxs-lookup"><span data-stu-id="6de04-122">Fiscal year</span></span>
-   <span data-ttu-id="6de04-123">Mali dönem</span><span class="sxs-lookup"><span data-stu-id="6de04-123">Fiscal period</span></span>

<span data-ttu-id="6de04-124">Genel gider hesaplama, sürümden bağımsız olarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="6de04-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="6de04-125">Bu nedenle, Gerçek sürümden önce Bütçe sürümünü hesaplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6de04-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="6de04-126">Genel gider hesaplama dört adımdan oluşur, aşağıdaki çizimde gösterildiği gibi.</span><span class="sxs-lookup"><span data-stu-id="6de04-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="6de04-127">Her adımda, günlük girişleri olan bir günlük başlığı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6de04-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="6de04-128">Bu günlük başlığı, her hesaplama adımı için giriş verilerini tutar.</span><span class="sxs-lookup"><span data-stu-id="6de04-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="6de04-129">İlkeler ve kurallar her günlük satırına uygulanır ve maliyet girişleri çıkış olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6de04-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="6de04-130">Bu nedenle, her zaman tam izlenebilirliğe sahip olursunuz.</span><span class="sxs-lookup"><span data-stu-id="6de04-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="6de04-131">[![Genel gider hesaplaması](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="6de04-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="6de04-132">Elektrik genel gideri maliyetini hesapla ve tahsis et</span><span class="sxs-lookup"><span data-stu-id="6de04-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="6de04-133">Mali muhasebede, elektrik gibi bazı maliyetler peşin ödeme olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="6de04-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="6de04-134">Bu nedenle, Maliyet muhasebesi için ayrıntılı yönetim bilgiler sağlanmaz.</span><span class="sxs-lookup"><span data-stu-id="6de04-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="6de04-135">Maliyet muhasebesinde doğru yönetimsel bilgileri tüm yönetim birim ve düzeylerinde sağlamak için, maliyetlerin kuruluş birimleri arasında akması gerekir.</span><span class="sxs-lookup"><span data-stu-id="6de04-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="6de04-136">Bu akış, tüketimin doğru bir kaydına ya da adil bir değerlendirmeye dayanıyor olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6de04-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="6de04-137">Genel muhasebede, bir elektrik maliyeti aşağıdaki tabloda gösterildiği gibi deftere nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="6de04-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6de04-138">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="6de04-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6de04-139">Maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="6de04-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="6de04-140">Ana hesap</span><span class="sxs-lookup"><span data-stu-id="6de04-140">Main account</span></span></th>
<th><span data-ttu-id="6de04-141">Muhasebe para birimi cinsinden tutar</span><span class="sxs-lookup"><span data-stu-id="6de04-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6de04-142">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="6de04-143">CC099</span><span class="sxs-lookup"><span data-stu-id="6de04-143">CC099</span></span></td>
<td><span data-ttu-id="6de04-144">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="6de04-144">Default cost center</span></span></td>
<td><span data-ttu-id="6de04-145">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-145">10001</span></span></td>
<td><span data-ttu-id="6de04-146">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-146">Electricity</span></span></td>
<td><span data-ttu-id="6de04-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="6de04-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="6de04-148">Adım 1: Maliyet davranışı hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="6de04-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="6de04-149">Varsayılan olarak, maliyeti girişleri kaynak veriden içeri alındığında, Maliyet muhasebesinde **Sınıflandırılmamış** maliyet davranışı sınıflandırmasını alırlar.</span><span class="sxs-lookup"><span data-stu-id="6de04-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="6de04-150">Maliyet davranışı ilke kuralları ekleyerek, maliyet girişlerini **Sabit maliyet** veya **Değişken maliyet** olarak yeniden sınıflandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6de04-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="6de04-151">Maliyet davranış kuralını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="6de04-151">Define the cost behavior rule</span></span>

<span data-ttu-id="6de04-152">Bazı durumlarda, sabit bir ücret maliyet parçasıdır ve kalan maliyet, tüketime dayanır.</span><span class="sxs-lookup"><span data-stu-id="6de04-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="6de04-153">Elektrik faturaları genellikle bu tanıma uyar.</span><span class="sxs-lookup"><span data-stu-id="6de04-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="6de04-154">Belirli bir sabit ücret ödedikten sonra, kilovat saatlik (Kwh) tüketim başına ödeme yaparsınız.</span><span class="sxs-lookup"><span data-stu-id="6de04-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="6de04-155">Örneğin, sabit maliyet masrafı 1.000,00 ise, maliyet davranışı kural nasıl tanımlanır:</span><span class="sxs-lookup"><span data-stu-id="6de04-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="6de04-156">Sabit tutar 1.000,00</span><span class="sxs-lookup"><span data-stu-id="6de04-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="6de04-157">0 &lt;= 1.000,00 = Sabit</span><span class="sxs-lookup"><span data-stu-id="6de04-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="6de04-158">1000,01 &lt; N = Değişken</span><span class="sxs-lookup"><span data-stu-id="6de04-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="6de04-159">Günlük</span><span class="sxs-lookup"><span data-stu-id="6de04-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6de04-160">Günlük</span><span class="sxs-lookup"><span data-stu-id="6de04-160">Journal</span></span></th>
<th><span data-ttu-id="6de04-161">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="6de04-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6de04-162">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="6de04-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6de04-163">Sürüm</span><span class="sxs-lookup"><span data-stu-id="6de04-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6de04-164">00001</span><span class="sxs-lookup"><span data-stu-id="6de04-164">00001</span></span></td>
<td><span data-ttu-id="6de04-165">Maliyet davranışı hesaplama günlüğü</span><span class="sxs-lookup"><span data-stu-id="6de04-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="6de04-166">Mali</span><span class="sxs-lookup"><span data-stu-id="6de04-166">Fiscal</span></span></td>
<td><span data-ttu-id="6de04-167">2017</span><span class="sxs-lookup"><span data-stu-id="6de04-167">2017</span></span></td>
<td><span data-ttu-id="6de04-168">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="6de04-168">Period 1</span></span></td>
<td><span data-ttu-id="6de04-169">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="6de04-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="6de04-170">Günlük girişleri (Maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="6de04-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6de04-171">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="6de04-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6de04-172">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="6de04-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6de04-173">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="6de04-173">Cost element</span></span></th>
<th><span data-ttu-id="6de04-174">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="6de04-174">Cost behavior</span></span></th>
<th><span data-ttu-id="6de04-175">Tutar</span><span class="sxs-lookup"><span data-stu-id="6de04-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6de04-176">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="6de04-177">CC099</span><span class="sxs-lookup"><span data-stu-id="6de04-177">CC099</span></span></td>
<td><span data-ttu-id="6de04-178">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="6de04-178">Default cost center</span></span></td>
<td><span data-ttu-id="6de04-179">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-179">10001</span></span></td>
<td><span data-ttu-id="6de04-180">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-180">Electricity</span></span></td>
<td><span data-ttu-id="6de04-181">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="6de04-181">Unclassified</span></span></td>
<td><span data-ttu-id="6de04-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="6de04-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6de04-183">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="6de04-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6de04-184">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="6de04-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6de04-185">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="6de04-185">Cost element</span></span></th>
<th><span data-ttu-id="6de04-186">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="6de04-186">Cost behavior</span></span></th>
<th><span data-ttu-id="6de04-187">Tutar</span><span class="sxs-lookup"><span data-stu-id="6de04-187">Amount</span></span></th>
<th><span data-ttu-id="6de04-188">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="6de04-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6de04-189">CC099</span><span class="sxs-lookup"><span data-stu-id="6de04-189">CC099</span></span></td>
<td><span data-ttu-id="6de04-190">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="6de04-190">Default cost center</span></span></td>
<td><span data-ttu-id="6de04-191">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-191">10001</span></span></td>
<td><span data-ttu-id="6de04-192">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-192">Electricity</span></span></td>
<td><span data-ttu-id="6de04-193">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="6de04-193">Unclassified</span></span></td>
<td><span data-ttu-id="6de04-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="6de04-194">10,000.00</span></span></td>
<td><span data-ttu-id="6de04-195">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-196">CC099</span><span class="sxs-lookup"><span data-stu-id="6de04-196">CC099</span></span></td>
<td><span data-ttu-id="6de04-197">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="6de04-197">Default cost center</span></span></td>
<td><span data-ttu-id="6de04-198">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-198">10001</span></span></td>
<td><span data-ttu-id="6de04-199">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-199">Electricity</span></span></td>
<td><span data-ttu-id="6de04-200">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="6de04-200">Unclassified</span></span></td>
<td><span data-ttu-id="6de04-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="6de04-201">-10,000.00</span></span></td>
<td><span data-ttu-id="6de04-202">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-203">CC099</span><span class="sxs-lookup"><span data-stu-id="6de04-203">CC099</span></span></td>
<td><span data-ttu-id="6de04-204">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="6de04-204">Default cost center</span></span></td>
<td><span data-ttu-id="6de04-205">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-205">10001</span></span></td>
<td><span data-ttu-id="6de04-206">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-206">Electricity</span></span></td>
<td><span data-ttu-id="6de04-207">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-207">Fixed cost</span></span></td>
<td><span data-ttu-id="6de04-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="6de04-208">1,000.00</span></span></td>
<td><span data-ttu-id="6de04-209">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-210">CC099</span><span class="sxs-lookup"><span data-stu-id="6de04-210">CC099</span></span></td>
<td><span data-ttu-id="6de04-211">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="6de04-211">Default cost center</span></span></td>
<td><span data-ttu-id="6de04-212">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-212">10001</span></span></td>
<td><span data-ttu-id="6de04-213">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-213">Electricity</span></span></td>
<td><span data-ttu-id="6de04-214">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-214">Variable cost</span></span></td>
<td><span data-ttu-id="6de04-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="6de04-215">9,000.00</span></span></td>
<td><span data-ttu-id="6de04-216">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6de04-217">Daha fazla bilgi için bkz. [Maliyet davranışı ilkesi oluşturma ve bir maliyet kontrol birimine atama](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="6de04-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="6de04-218">Adım 2: Maliyet dağıtımı hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="6de04-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="6de04-219">Maliyet dağıtımı, bir nesneden bir veya daha fazlasına ilgili tahsisat tabanı uygulayarak maliyeti yeniden dağıtmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6de04-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="6de04-220">Maliyet dağıtımı ve maliyet tahsisatı, maliyet dağıtımının her zaman orijinal maliyetin birincil maliyet öğesinde bulunmasıyla farklılık gösterir.</span><span class="sxs-lookup"><span data-stu-id="6de04-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="6de04-221">Maliyet dağıtım kuralını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="6de04-221">Define the cost distribution rule</span></span>

<span data-ttu-id="6de04-222">Mali muhasebede, elektrik maliyetleri çoğu zaman peşin ödeme olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="6de04-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="6de04-223">Maliyet muhasebesinde ise bu yöntem yeterince ayrıntılı değildir.</span><span class="sxs-lookup"><span data-stu-id="6de04-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="6de04-224">Değişken maliyet, maliyet nesnelerine tek tek, adil bir temele dayanarak dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6de04-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="6de04-225">En mantıklı tahsisat, elektrik kullanımını (Kwh) temel alarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6de04-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="6de04-226">Elektrik adına sahip, istatistiksel bir boyut üyesi oluşturulur ve elektrik tüketimi kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="6de04-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="6de04-227">Varsayıla olarak, tüm istatistiksel boyut üyeleri tahsisat tabanları olarak kullanılabilir hale gelir.</span><span class="sxs-lookup"><span data-stu-id="6de04-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6de04-228">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="6de04-228">Cost object</span></span></th>
<th><span data-ttu-id="6de04-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="6de04-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6de04-230">CC001</span><span class="sxs-lookup"><span data-stu-id="6de04-230">CC001</span></span></td>
<td><span data-ttu-id="6de04-231">İK</span><span class="sxs-lookup"><span data-stu-id="6de04-231">HR</span></span></td>
<td><span data-ttu-id="6de04-232">1.000</span><span class="sxs-lookup"><span data-stu-id="6de04-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-233">CC002</span><span class="sxs-lookup"><span data-stu-id="6de04-233">CC002</span></span></td>
<td><span data-ttu-id="6de04-234">Finans</span><span class="sxs-lookup"><span data-stu-id="6de04-234">Finance</span></span></td>
<td><span data-ttu-id="6de04-235">6,000</span><span class="sxs-lookup"><span data-stu-id="6de04-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-236">CC003</span><span class="sxs-lookup"><span data-stu-id="6de04-236">CC003</span></span></td>
<td><span data-ttu-id="6de04-237">Montaj</span><span class="sxs-lookup"><span data-stu-id="6de04-237">Assembly</span></span></td>
<td><span data-ttu-id="6de04-238">0</span><span class="sxs-lookup"><span data-stu-id="6de04-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6de04-239">Aşağıdaki tablo, elektrik tüketiminin değişken maliyetler için bir tahsisat tabanlı olarak uygulandığındaki sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="6de04-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6de04-240">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="6de04-240">Cost object</span></span></th>
<th><span data-ttu-id="6de04-241">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="6de04-241">Magnitude</span></span></th>
<th><span data-ttu-id="6de04-242">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="6de04-242">Allocation factor</span></span></th>
<th><span data-ttu-id="6de04-243">Tutar</span><span class="sxs-lookup"><span data-stu-id="6de04-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6de04-244">CC001</span><span class="sxs-lookup"><span data-stu-id="6de04-244">CC001</span></span></td>
<td><span data-ttu-id="6de04-245">İK</span><span class="sxs-lookup"><span data-stu-id="6de04-245">HR</span></span></td>
<td><span data-ttu-id="6de04-246">1.000</span><span class="sxs-lookup"><span data-stu-id="6de04-246">1,000</span></span></td>
<td><span data-ttu-id="6de04-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="6de04-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="6de04-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="6de04-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-249">CC002</span><span class="sxs-lookup"><span data-stu-id="6de04-249">CC002</span></span></td>
<td><span data-ttu-id="6de04-250">Finans</span><span class="sxs-lookup"><span data-stu-id="6de04-250">Finance</span></span></td>
<td><span data-ttu-id="6de04-251">6,000</span><span class="sxs-lookup"><span data-stu-id="6de04-251">6,000</span></span></td>
<td><span data-ttu-id="6de04-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="6de04-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="6de04-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="6de04-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-254">CC003</span><span class="sxs-lookup"><span data-stu-id="6de04-254">CC003</span></span></td>
<td><span data-ttu-id="6de04-255">Montaj</span><span class="sxs-lookup"><span data-stu-id="6de04-255">Assembly</span></span></td>
<td><span data-ttu-id="6de04-256">0</span><span class="sxs-lookup"><span data-stu-id="6de04-256">0</span></span></td>
<td><span data-ttu-id="6de04-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="6de04-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="6de04-258">0,00</span><span class="sxs-lookup"><span data-stu-id="6de04-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6de04-259">Sabit maliyet, elektrik tüketmiş olan tekil maliyet nesnelerine eşit miktarda dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6de04-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="6de04-260">Bu sonuca, Elektrik istatistiksel boyut öğesini bir formül tahsisat tabanında kullanarak ulaşabilirsiniz: (Elektrik &gt; 0,00) Aşağıdaki tablo, elektrik tüketimi değişken maliyetler için bir tahsisat tabanı olarak kullanıldığında ortaya çıkan sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="6de04-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6de04-261">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="6de04-261">Cost object</span></span></th>
<th><span data-ttu-id="6de04-262">Formül</span><span class="sxs-lookup"><span data-stu-id="6de04-262">Formula</span></span></th>
<th><span data-ttu-id="6de04-263">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="6de04-263">Magnitude</span></span></th>
<th><span data-ttu-id="6de04-264">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="6de04-264">Allocation factor</span></span></th>
<th><span data-ttu-id="6de04-265">Tutar</span><span class="sxs-lookup"><span data-stu-id="6de04-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6de04-266">CC001</span><span class="sxs-lookup"><span data-stu-id="6de04-266">CC001</span></span></td>
<td><span data-ttu-id="6de04-267">İK</span><span class="sxs-lookup"><span data-stu-id="6de04-267">HR</span></span></td>
<td><span data-ttu-id="6de04-268">(1,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="6de04-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="6de04-269">1</span><span class="sxs-lookup"><span data-stu-id="6de04-269">1</span></span></td>
<td><span data-ttu-id="6de04-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="6de04-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="6de04-271">500.00</span><span class="sxs-lookup"><span data-stu-id="6de04-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-272">CC002</span><span class="sxs-lookup"><span data-stu-id="6de04-272">CC002</span></span></td>
<td><span data-ttu-id="6de04-273">Finans</span><span class="sxs-lookup"><span data-stu-id="6de04-273">Finance</span></span></td>
<td><span data-ttu-id="6de04-274">(6,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="6de04-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="6de04-275">1</span><span class="sxs-lookup"><span data-stu-id="6de04-275">1</span></span></td>
<td><span data-ttu-id="6de04-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="6de04-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="6de04-277">500.00</span><span class="sxs-lookup"><span data-stu-id="6de04-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-278">CC003</span><span class="sxs-lookup"><span data-stu-id="6de04-278">CC003</span></span></td>
<td><span data-ttu-id="6de04-279">Montaj</span><span class="sxs-lookup"><span data-stu-id="6de04-279">Assembly</span></span></td>
<td><span data-ttu-id="6de04-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="6de04-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="6de04-281">0</span><span class="sxs-lookup"><span data-stu-id="6de04-281">0</span></span></td>
<td><span data-ttu-id="6de04-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="6de04-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="6de04-283">0,00</span><span class="sxs-lookup"><span data-stu-id="6de04-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="6de04-284">Günlük</span><span class="sxs-lookup"><span data-stu-id="6de04-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6de04-285">Günlük</span><span class="sxs-lookup"><span data-stu-id="6de04-285">Journal</span></span></th>
<th><span data-ttu-id="6de04-286">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="6de04-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6de04-287">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="6de04-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6de04-288">Sürüm</span><span class="sxs-lookup"><span data-stu-id="6de04-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6de04-289">00002</span><span class="sxs-lookup"><span data-stu-id="6de04-289">00002</span></span></td>
<td><span data-ttu-id="6de04-290">Maliyet dağıtımı hesaplama günlüğü</span><span class="sxs-lookup"><span data-stu-id="6de04-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="6de04-291">Mali</span><span class="sxs-lookup"><span data-stu-id="6de04-291">Fiscal</span></span></td>
<td><span data-ttu-id="6de04-292">2017</span><span class="sxs-lookup"><span data-stu-id="6de04-292">2017</span></span></td>
<td><span data-ttu-id="6de04-293">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="6de04-293">Period 1</span></span></td>
<td><span data-ttu-id="6de04-294">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="6de04-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="6de04-295">Günlük girişleri (Maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="6de04-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6de04-296">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="6de04-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6de04-297">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="6de04-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6de04-298">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="6de04-298">Cost element</span></span></th>
<th><span data-ttu-id="6de04-299">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="6de04-299">Cost behavior</span></span></th>
<th><span data-ttu-id="6de04-300">Tutar</span><span class="sxs-lookup"><span data-stu-id="6de04-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6de04-301">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="6de04-302">CC099</span><span class="sxs-lookup"><span data-stu-id="6de04-302">CC099</span></span></td>
<td><span data-ttu-id="6de04-303">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="6de04-303">Default cost center</span></span></td>
<td><span data-ttu-id="6de04-304">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-304">10001</span></span></td>
<td><span data-ttu-id="6de04-305">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-305">Electricity</span></span></td>
<td><span data-ttu-id="6de04-306">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-306">Fixed cost</span></span></td>
<td><span data-ttu-id="6de04-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="6de04-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-308">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="6de04-309">CC099</span><span class="sxs-lookup"><span data-stu-id="6de04-309">CC099</span></span></td>
<td><span data-ttu-id="6de04-310">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="6de04-310">Default cost center</span></span></td>
<td><span data-ttu-id="6de04-311">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-311">10001</span></span></td>
<td><span data-ttu-id="6de04-312">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-312">Electricity</span></span></td>
<td><span data-ttu-id="6de04-313">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-313">Variable cost</span></span></td>
<td><span data-ttu-id="6de04-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="6de04-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6de04-315">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="6de04-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6de04-316">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="6de04-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6de04-317">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="6de04-317">Cost element</span></span></th>
<th><span data-ttu-id="6de04-318">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="6de04-318">Cost behavior</span></span></th>
<th><span data-ttu-id="6de04-319">Tutar</span><span class="sxs-lookup"><span data-stu-id="6de04-319">Amount</span></span></th>
<th><span data-ttu-id="6de04-320">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="6de04-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6de04-321">CC099</span><span class="sxs-lookup"><span data-stu-id="6de04-321">CC099</span></span></td>
<td><span data-ttu-id="6de04-322">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="6de04-322">Default cost center</span></span></td>
<td><span data-ttu-id="6de04-323">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-323">10001</span></span></td>
<td><span data-ttu-id="6de04-324">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-324">Electricity</span></span></td>
<td><span data-ttu-id="6de04-325">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-325">Fixed cost</span></span></td>
<td><span data-ttu-id="6de04-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="6de04-326">-1,000.00</span></span></td>
<td><span data-ttu-id="6de04-327">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-328">CC001</span><span class="sxs-lookup"><span data-stu-id="6de04-328">CC001</span></span></td>
<td><span data-ttu-id="6de04-329">İK</span><span class="sxs-lookup"><span data-stu-id="6de04-329">HR</span></span></td>
<td><span data-ttu-id="6de04-330">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-330">10001</span></span></td>
<td><span data-ttu-id="6de04-331">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-331">Electricity</span></span></td>
<td><span data-ttu-id="6de04-332">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-332">Fixed cost</span></span></td>
<td><span data-ttu-id="6de04-333">500.00</span><span class="sxs-lookup"><span data-stu-id="6de04-333">500.00</span></span></td>
<td><span data-ttu-id="6de04-334">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-335">CC002</span><span class="sxs-lookup"><span data-stu-id="6de04-335">CC002</span></span></td>
<td><span data-ttu-id="6de04-336">Finans</span><span class="sxs-lookup"><span data-stu-id="6de04-336">Finance</span></span></td>
<td><span data-ttu-id="6de04-337">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-337">10001</span></span></td>
<td><span data-ttu-id="6de04-338">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-338">Electricity</span></span></td>
<td><span data-ttu-id="6de04-339">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-339">Fixed cost</span></span></td>
<td><span data-ttu-id="6de04-340">500.00</span><span class="sxs-lookup"><span data-stu-id="6de04-340">500.00</span></span></td>
<td><span data-ttu-id="6de04-341">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-342">CC099</span><span class="sxs-lookup"><span data-stu-id="6de04-342">CC099</span></span></td>
<td><span data-ttu-id="6de04-343">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="6de04-343">Default cost center</span></span></td>
<td><span data-ttu-id="6de04-344">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-344">10001</span></span></td>
<td><span data-ttu-id="6de04-345">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-345">Electricity</span></span></td>
<td><span data-ttu-id="6de04-346">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-346">Variable cost</span></span></td>
<td><span data-ttu-id="6de04-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="6de04-347">-9,000.00</span></span></td>
<td><span data-ttu-id="6de04-348">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-349">CC001</span><span class="sxs-lookup"><span data-stu-id="6de04-349">CC001</span></span></td>
<td><span data-ttu-id="6de04-350">İK</span><span class="sxs-lookup"><span data-stu-id="6de04-350">HR</span></span></td>
<td><span data-ttu-id="6de04-351">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-351">10001</span></span></td>
<td><span data-ttu-id="6de04-352">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-352">Electricity</span></span></td>
<td><span data-ttu-id="6de04-353">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-353">Variable cost</span></span></td>
<td><span data-ttu-id="6de04-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="6de04-354">1,285.71</span></span></td>
<td><span data-ttu-id="6de04-355">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-356">CC002</span><span class="sxs-lookup"><span data-stu-id="6de04-356">CC002</span></span></td>
<td><span data-ttu-id="6de04-357">Finans</span><span class="sxs-lookup"><span data-stu-id="6de04-357">Finance</span></span></td>
<td><span data-ttu-id="6de04-358">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-358">10001</span></span></td>
<td><span data-ttu-id="6de04-359">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-359">Electricity</span></span></td>
<td><span data-ttu-id="6de04-360">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-360">Variable cost</span></span></td>
<td><span data-ttu-id="6de04-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="6de04-361">7,714.29</span></span></td>
<td><span data-ttu-id="6de04-362">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6de04-363">Daha fazla bilgi için bkz. [Maliyet dağıtımı ilkesi oluşturma ve bir maliyet kontrol birimine atama](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="6de04-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="6de04-364">Adım 3: Genel gider oranı hesaplama işlemi</span><span class="sxs-lookup"><span data-stu-id="6de04-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="6de04-365">Genel gider oranı, bir veya birden fazla belirli maliyet nesnesine masraf yüklemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6de04-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="6de04-366">Masraf, önceden belirlenmiş maliyet oranına ve tahsisat tabanından hesaplanan büyüklüğe dayanır.</span><span class="sxs-lookup"><span data-stu-id="6de04-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="6de04-367">Genel gider oranını tanımlama</span><span class="sxs-lookup"><span data-stu-id="6de04-367">Define the overhead rate</span></span>

<span data-ttu-id="6de04-368">Maliyet nesnesi CC001 HR, bir dizi dahili projeye katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="6de04-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="6de04-369">HR projeleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6de04-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6de04-370">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="6de04-370">Cost object</span></span></th>
<th><span data-ttu-id="6de04-371">Saatler</span><span class="sxs-lookup"><span data-stu-id="6de04-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6de04-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="6de04-372">Proj 1</span></span></td>
<td><span data-ttu-id="6de04-373">Proje 1</span><span class="sxs-lookup"><span data-stu-id="6de04-373">Project 1</span></span></td>
<td><span data-ttu-id="6de04-374">3</span><span class="sxs-lookup"><span data-stu-id="6de04-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="6de04-375">Proj 2</span></span></td>
<td><span data-ttu-id="6de04-376">Proje 2</span><span class="sxs-lookup"><span data-stu-id="6de04-376">Project 2</span></span></td>
<td><span data-ttu-id="6de04-377">1</span><span class="sxs-lookup"><span data-stu-id="6de04-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6de04-378">Maliyet projeleri dağıtımı için bir önceden belirlenmiş maliyet oranı tanımlandı.</span><span class="sxs-lookup"><span data-stu-id="6de04-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6de04-379">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="6de04-379">Cost object</span></span></th>
<th><span data-ttu-id="6de04-380">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="6de04-380">Cost element</span></span></th>
<th><span data-ttu-id="6de04-381">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="6de04-381">Cost behavior</span></span></th>
<th><span data-ttu-id="6de04-382">Birimler</span><span class="sxs-lookup"><span data-stu-id="6de04-382">Units</span></span></th>
<th><span data-ttu-id="6de04-383">Ücret</span><span class="sxs-lookup"><span data-stu-id="6de04-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6de04-384">CC001</span><span class="sxs-lookup"><span data-stu-id="6de04-384">CC001</span></span></td>
<td><span data-ttu-id="6de04-385">İK</span><span class="sxs-lookup"><span data-stu-id="6de04-385">HR</span></span></td>
<td><span data-ttu-id="6de04-386">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-386">10001</span></span></td>
<td><span data-ttu-id="6de04-387">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-387">Variable cost</span></span></td>
<td><span data-ttu-id="6de04-388">1</span><span class="sxs-lookup"><span data-stu-id="6de04-388">1</span></span></td>
<td><span data-ttu-id="6de04-389">10</span><span class="sxs-lookup"><span data-stu-id="6de04-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6de04-390">Aşağıdaki tablo, HR projeleri bir tahsisat tabanı olarak uygulandığındaki sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="6de04-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6de04-391">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="6de04-391">Cost object</span></span></th>
<th><span data-ttu-id="6de04-392">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="6de04-392">Magnitude</span></span></th>
<th><span data-ttu-id="6de04-393">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="6de04-393">Cost element</span></span></th>
<th><span data-ttu-id="6de04-394">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="6de04-394">Allocation factor</span></span></th>
<th><span data-ttu-id="6de04-395">Tutar</span><span class="sxs-lookup"><span data-stu-id="6de04-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6de04-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="6de04-396">Proj 1</span></span></td>
<td><span data-ttu-id="6de04-397">Proje 1</span><span class="sxs-lookup"><span data-stu-id="6de04-397">Project 1</span></span></td>
<td><span data-ttu-id="6de04-398">3</span><span class="sxs-lookup"><span data-stu-id="6de04-398">3</span></span></td>
<td><span data-ttu-id="6de04-399">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-399">10001</span></span></td>
<td><span data-ttu-id="6de04-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="6de04-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="6de04-401">30.00</span><span class="sxs-lookup"><span data-stu-id="6de04-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="6de04-402">Proj 2</span></span></td>
<td><span data-ttu-id="6de04-403">Proje 2</span><span class="sxs-lookup"><span data-stu-id="6de04-403">Project 2</span></span></td>
<td><span data-ttu-id="6de04-404">1</span><span class="sxs-lookup"><span data-stu-id="6de04-404">1</span></span></td>
<td><span data-ttu-id="6de04-405">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-405">10001</span></span></td>
<td><span data-ttu-id="6de04-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="6de04-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="6de04-407">10,00</span><span class="sxs-lookup"><span data-stu-id="6de04-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="6de04-408">Günlük</span><span class="sxs-lookup"><span data-stu-id="6de04-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6de04-409">Günlük</span><span class="sxs-lookup"><span data-stu-id="6de04-409">Journal</span></span></th>
<th><span data-ttu-id="6de04-410">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="6de04-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6de04-411">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="6de04-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6de04-412">Sürüm</span><span class="sxs-lookup"><span data-stu-id="6de04-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6de04-413">00003</span><span class="sxs-lookup"><span data-stu-id="6de04-413">00003</span></span></td>
<td><span data-ttu-id="6de04-414">Genel gider oranı hesaplaması günlüğü</span><span class="sxs-lookup"><span data-stu-id="6de04-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="6de04-415">Mali</span><span class="sxs-lookup"><span data-stu-id="6de04-415">Fiscal</span></span></td>
<td><span data-ttu-id="6de04-416">2017</span><span class="sxs-lookup"><span data-stu-id="6de04-416">2017</span></span></td>
<td><span data-ttu-id="6de04-417">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="6de04-417">Period 1</span></span></td>
<td><span data-ttu-id="6de04-418">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="6de04-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="6de04-419">Günlük girişleri (Genel gider oranı hesaplaması için günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="6de04-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6de04-420">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="6de04-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6de04-421">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="6de04-421">Cost object</span></span></th>
<th><span data-ttu-id="6de04-422">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="6de04-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6de04-423">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="6de04-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="6de04-424">Proj 1</span></span></td>
<td><span data-ttu-id="6de04-425">Dahili Proj 1</span><span class="sxs-lookup"><span data-stu-id="6de04-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="6de04-426">3,00</span><span class="sxs-lookup"><span data-stu-id="6de04-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-427">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="6de04-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="6de04-428">Proj 2</span></span></td>
<td><span data-ttu-id="6de04-429">Dahili Proj 2</span><span class="sxs-lookup"><span data-stu-id="6de04-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="6de04-430">1.00</span><span class="sxs-lookup"><span data-stu-id="6de04-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6de04-431">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="6de04-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6de04-432">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="6de04-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6de04-433">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="6de04-433">Cost element</span></span></th>
<th><span data-ttu-id="6de04-434">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="6de04-434">Cost behavior</span></span></th>
<th><span data-ttu-id="6de04-435">Tutar</span><span class="sxs-lookup"><span data-stu-id="6de04-435">Amount</span></span></th>
<th><span data-ttu-id="6de04-436">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="6de04-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6de04-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="6de04-437">CC0001</span></span></td>
<td><span data-ttu-id="6de04-438">İK</span><span class="sxs-lookup"><span data-stu-id="6de04-438">HR</span></span></td>
<td><span data-ttu-id="6de04-439">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-439">10001</span></span></td>
<td><span data-ttu-id="6de04-440">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-440">Electricity</span></span></td>
<td><span data-ttu-id="6de04-441">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-441">Variable cost</span></span></td>
<td><span data-ttu-id="6de04-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="6de04-442">-30.00</span></span></td>
<td><span data-ttu-id="6de04-443">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="6de04-444">Proj 1</span></span></td>
<td><span data-ttu-id="6de04-445">Dahili Proj 1</span><span class="sxs-lookup"><span data-stu-id="6de04-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="6de04-446">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-446">10001</span></span></td>
<td><span data-ttu-id="6de04-447">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-447">Electricity</span></span></td>
<td><span data-ttu-id="6de04-448">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-448">Variable cost</span></span></td>
<td><span data-ttu-id="6de04-449">30.00</span><span class="sxs-lookup"><span data-stu-id="6de04-449">30.00</span></span></td>
<td><span data-ttu-id="6de04-450">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-451">CC001</span><span class="sxs-lookup"><span data-stu-id="6de04-451">CC001</span></span></td>
<td><span data-ttu-id="6de04-452">İK</span><span class="sxs-lookup"><span data-stu-id="6de04-452">HR</span></span></td>
<td><span data-ttu-id="6de04-453">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-453">10001</span></span></td>
<td><span data-ttu-id="6de04-454">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-454">Electricity</span></span></td>
<td><span data-ttu-id="6de04-455">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-455">Variable cost</span></span></td>
<td><span data-ttu-id="6de04-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="6de04-456">-10.00</span></span></td>
<td><span data-ttu-id="6de04-457">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="6de04-458">Proj 2</span></span></td>
<td><span data-ttu-id="6de04-459">Dahili Proj 2</span><span class="sxs-lookup"><span data-stu-id="6de04-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="6de04-460">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-460">10001</span></span></td>
<td><span data-ttu-id="6de04-461">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-461">Electricity</span></span></td>
<td><span data-ttu-id="6de04-462">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-462">Variable cost</span></span></td>
<td><span data-ttu-id="6de04-463">10,00</span><span class="sxs-lookup"><span data-stu-id="6de04-463">10.00</span></span></td>
<td><span data-ttu-id="6de04-464">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6de04-465">Daha fazla bilgi için [Genel gider hesaplaması gerçekleştir](cost-rollup.md#perform-overhead-calculation) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="6de04-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="6de04-466">Adım 4: Maliyet tahsisat hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="6de04-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="6de04-467">Tahsisat, bir tahsisat tabanı kullanarak bir maliyet nesnesinin diğer maliyet nesnelerine bakiyesini tahsis eder.</span><span class="sxs-lookup"><span data-stu-id="6de04-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="6de04-468">Finance karşılıklı tahsisat yöntemini desteklemektedir.</span><span class="sxs-lookup"><span data-stu-id="6de04-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="6de04-469">Karşılıklı tahsisat yönteminde, yardımcı maliyet nesnelerinin değiştiği karşılıklı hizmetler tümüyle tanınır.</span><span class="sxs-lookup"><span data-stu-id="6de04-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="6de04-470">Sistem, tahsisatların doğru gerçekleştireceği sırayı otomatik olarak belirler.</span><span class="sxs-lookup"><span data-stu-id="6de04-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="6de04-471">Bir maliyet nesnesinin bakiyesi tek bir tahsisat tabanı tarafından tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="6de04-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="6de04-472">Yeni maliyet nesnesi boyutları arasındaki tahsisatlar ve onların üyeleri desteklenir.</span><span class="sxs-lookup"><span data-stu-id="6de04-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="6de04-473">Tahsisatın sırası, maliyet kontrol birimi tarafından kontrol edilir.</span><span class="sxs-lookup"><span data-stu-id="6de04-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="6de04-474">[![Karşılıklı yöntemi](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="6de04-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="6de04-475">Maliyet tahsisatını tanımla</span><span class="sxs-lookup"><span data-stu-id="6de04-475">Define the cost allocation</span></span>

<span data-ttu-id="6de04-476">Bir maliyetin akışını nasıl izleyeceğinize dair basit bir örnek aşağıda verilmiştir,</span><span class="sxs-lookup"><span data-stu-id="6de04-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="6de04-477">Maliyet nesnesi CC001 HR, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="6de04-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="6de04-478">HR hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6de04-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6de04-479">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="6de04-479">Cost object</span></span></th>
<th><span data-ttu-id="6de04-480">HR hizmetleri</span><span class="sxs-lookup"><span data-stu-id="6de04-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6de04-481">CC002</span><span class="sxs-lookup"><span data-stu-id="6de04-481">CC002</span></span></td>
<td><span data-ttu-id="6de04-482">Finans</span><span class="sxs-lookup"><span data-stu-id="6de04-482">Finance</span></span></td>
<td><span data-ttu-id="6de04-483">35</span><span class="sxs-lookup"><span data-stu-id="6de04-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-484">CC003</span><span class="sxs-lookup"><span data-stu-id="6de04-484">CC003</span></span></td>
<td><span data-ttu-id="6de04-485">Montaj</span><span class="sxs-lookup"><span data-stu-id="6de04-485">Assembly</span></span></td>
<td><span data-ttu-id="6de04-486">55</span><span class="sxs-lookup"><span data-stu-id="6de04-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-487">CC004</span><span class="sxs-lookup"><span data-stu-id="6de04-487">CC004</span></span></td>
<td><span data-ttu-id="6de04-488">Paketleme</span><span class="sxs-lookup"><span data-stu-id="6de04-488">Packaging</span></span></td>
<td><span data-ttu-id="6de04-489">10</span><span class="sxs-lookup"><span data-stu-id="6de04-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6de04-490">Maliyet nesnesi CC002 Finans, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="6de04-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="6de04-491">Finans hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6de04-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6de04-492">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="6de04-492">Cost object</span></span></th>
<th><span data-ttu-id="6de04-493">Finans hizmetleri</span><span class="sxs-lookup"><span data-stu-id="6de04-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6de04-494">CC003</span><span class="sxs-lookup"><span data-stu-id="6de04-494">CC003</span></span></td>
<td><span data-ttu-id="6de04-495">Montaj</span><span class="sxs-lookup"><span data-stu-id="6de04-495">Assembly</span></span></td>
<td><span data-ttu-id="6de04-496">65</span><span class="sxs-lookup"><span data-stu-id="6de04-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-497">CC004</span><span class="sxs-lookup"><span data-stu-id="6de04-497">CC004</span></span></td>
<td><span data-ttu-id="6de04-498">Paketleme</span><span class="sxs-lookup"><span data-stu-id="6de04-498">Packaging</span></span></td>
<td><span data-ttu-id="6de04-499">35</span><span class="sxs-lookup"><span data-stu-id="6de04-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6de04-500">Maliyet nesnesi CC003 Derleme, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="6de04-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="6de04-501">Derleme hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6de04-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6de04-502">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="6de04-502">Cost object</span></span></th>
<th><span data-ttu-id="6de04-503">Derleme Hizmetleri (saat)</span><span class="sxs-lookup"><span data-stu-id="6de04-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6de04-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6de04-504">Prod 1</span></span></td>
<td><span data-ttu-id="6de04-505">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="6de04-505">Product 1</span></span></td>
<td><span data-ttu-id="6de04-506">60</span><span class="sxs-lookup"><span data-stu-id="6de04-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6de04-507">Prod 2</span></span></td>
<td><span data-ttu-id="6de04-508">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="6de04-508">Product 2</span></span></td>
<td><span data-ttu-id="6de04-509">20</span><span class="sxs-lookup"><span data-stu-id="6de04-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6de04-510">Maliyet nesnesi CC004 Ambalajlama, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="6de04-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="6de04-511">Ambalajlama hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6de04-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6de04-512">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="6de04-512">Cost object</span></span></th>
<th><span data-ttu-id="6de04-513">Ambalajlama hizmetleri (saat)</span><span class="sxs-lookup"><span data-stu-id="6de04-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6de04-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6de04-514">Prod 1</span></span></td>
<td><span data-ttu-id="6de04-515">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="6de04-515">Product 1</span></span></td>
<td><span data-ttu-id="6de04-516">80</span><span class="sxs-lookup"><span data-stu-id="6de04-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6de04-517">Prod 2</span></span></td>
<td><span data-ttu-id="6de04-518">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="6de04-518">Product 2</span></span></td>
<td><span data-ttu-id="6de04-519">15</span><span class="sxs-lookup"><span data-stu-id="6de04-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="6de04-520">Bir ürünün tükettiği üretim saatleri gibi istatistiki ölçümler, doğrudan kaynak verilerinden alınabilir.</span><span class="sxs-lookup"><span data-stu-id="6de04-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="6de04-521">Daha fazla bilgi için, [İstatistiksel ölçüm sağlayıcı şablonu](statistical-measure-provider-template.md#statistical-measure-provider-template) bakın.</span><span class="sxs-lookup"><span data-stu-id="6de04-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="6de04-522">Aşağıdaki tablo, İK hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığında ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="6de04-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6de04-523">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="6de04-523">Cost object</span></span></th>
<th><span data-ttu-id="6de04-524">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="6de04-524">Magnitude</span></span></th>
<th><span data-ttu-id="6de04-525">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="6de04-525">Allocation factor</span></span></th>
<th><span data-ttu-id="6de04-526">Tutar</span><span class="sxs-lookup"><span data-stu-id="6de04-526">Amount</span></span></th>
<th><span data-ttu-id="6de04-527">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="6de04-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6de04-528">CC002</span><span class="sxs-lookup"><span data-stu-id="6de04-528">CC002</span></span></td>
<td><span data-ttu-id="6de04-529">Finans</span><span class="sxs-lookup"><span data-stu-id="6de04-529">Finance</span></span></td>
<td><span data-ttu-id="6de04-530">35</span><span class="sxs-lookup"><span data-stu-id="6de04-530">35</span></span></td>
<td><span data-ttu-id="6de04-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="6de04-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="6de04-532">175.00</span><span class="sxs-lookup"><span data-stu-id="6de04-532">175.00</span></span></td>
<td><span data-ttu-id="6de04-533">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-534">CC003</span><span class="sxs-lookup"><span data-stu-id="6de04-534">CC003</span></span></td>
<td><span data-ttu-id="6de04-535">Montaj</span><span class="sxs-lookup"><span data-stu-id="6de04-535">Assembly</span></span></td>
<td><span data-ttu-id="6de04-536">55</span><span class="sxs-lookup"><span data-stu-id="6de04-536">55</span></span></td>
<td><span data-ttu-id="6de04-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="6de04-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="6de04-538">275.00</span><span class="sxs-lookup"><span data-stu-id="6de04-538">275.00</span></span></td>
<td><span data-ttu-id="6de04-539">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-540">CC004</span><span class="sxs-lookup"><span data-stu-id="6de04-540">CC004</span></span></td>
<td><span data-ttu-id="6de04-541">Paketleme</span><span class="sxs-lookup"><span data-stu-id="6de04-541">Packaging</span></span></td>
<td><span data-ttu-id="6de04-542">10</span><span class="sxs-lookup"><span data-stu-id="6de04-542">10</span></span></td>
<td><span data-ttu-id="6de04-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="6de04-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="6de04-544">50,00</span><span class="sxs-lookup"><span data-stu-id="6de04-544">50.00</span></span></td>
<td><span data-ttu-id="6de04-545">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-546">CC002</span><span class="sxs-lookup"><span data-stu-id="6de04-546">CC002</span></span></td>
<td><span data-ttu-id="6de04-547">Finans</span><span class="sxs-lookup"><span data-stu-id="6de04-547">Finance</span></span></td>
<td><span data-ttu-id="6de04-548">35</span><span class="sxs-lookup"><span data-stu-id="6de04-548">35</span></span></td>
<td><span data-ttu-id="6de04-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="6de04-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="6de04-550">436.00</span><span class="sxs-lookup"><span data-stu-id="6de04-550">436.00</span></span></td>
<td><span data-ttu-id="6de04-551">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-552">CC003</span><span class="sxs-lookup"><span data-stu-id="6de04-552">CC003</span></span></td>
<td><span data-ttu-id="6de04-553">Montaj</span><span class="sxs-lookup"><span data-stu-id="6de04-553">Assembly</span></span></td>
<td><span data-ttu-id="6de04-554">55</span><span class="sxs-lookup"><span data-stu-id="6de04-554">55</span></span></td>
<td><span data-ttu-id="6de04-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="6de04-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="6de04-556">685.14</span><span class="sxs-lookup"><span data-stu-id="6de04-556">685.14</span></span></td>
<td><span data-ttu-id="6de04-557">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-558">CC004</span><span class="sxs-lookup"><span data-stu-id="6de04-558">CC004</span></span></td>
<td><span data-ttu-id="6de04-559">Paketleme</span><span class="sxs-lookup"><span data-stu-id="6de04-559">Packaging</span></span></td>
<td><span data-ttu-id="6de04-560">10</span><span class="sxs-lookup"><span data-stu-id="6de04-560">10</span></span></td>
<td><span data-ttu-id="6de04-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="6de04-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="6de04-562">124.57</span><span class="sxs-lookup"><span data-stu-id="6de04-562">124.57</span></span></td>
<td><span data-ttu-id="6de04-563">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6de04-564">Aşağıdaki tablo, Finans hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="6de04-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6de04-565">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="6de04-565">Cost object</span></span></th>
<th><span data-ttu-id="6de04-566">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="6de04-566">Magnitude</span></span></th>
<th><span data-ttu-id="6de04-567">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="6de04-567">Allocation factor</span></span></th>
<th><span data-ttu-id="6de04-568">Tutar</span><span class="sxs-lookup"><span data-stu-id="6de04-568">Amount</span></span></th>
<th><span data-ttu-id="6de04-569">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="6de04-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6de04-570">CC003</span><span class="sxs-lookup"><span data-stu-id="6de04-570">CC003</span></span></td>
<td><span data-ttu-id="6de04-571">Montaj</span><span class="sxs-lookup"><span data-stu-id="6de04-571">Assembly</span></span></td>
<td><span data-ttu-id="6de04-572">65</span><span class="sxs-lookup"><span data-stu-id="6de04-572">65</span></span></td>
<td><span data-ttu-id="6de04-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="6de04-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="6de04-574">438.75</span><span class="sxs-lookup"><span data-stu-id="6de04-574">438.75</span></span></td>
<td><span data-ttu-id="6de04-575">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-576">CC004</span><span class="sxs-lookup"><span data-stu-id="6de04-576">CC004</span></span></td>
<td><span data-ttu-id="6de04-577">Paketleme</span><span class="sxs-lookup"><span data-stu-id="6de04-577">Packaging</span></span></td>
<td><span data-ttu-id="6de04-578">35</span><span class="sxs-lookup"><span data-stu-id="6de04-578">35</span></span></td>
<td><span data-ttu-id="6de04-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="6de04-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="6de04-580">236.25</span><span class="sxs-lookup"><span data-stu-id="6de04-580">236.25</span></span></td>
<td><span data-ttu-id="6de04-581">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-582">CC003</span><span class="sxs-lookup"><span data-stu-id="6de04-582">CC003</span></span></td>
<td><span data-ttu-id="6de04-583">Montaj</span><span class="sxs-lookup"><span data-stu-id="6de04-583">Assembly</span></span></td>
<td><span data-ttu-id="6de04-584">65</span><span class="sxs-lookup"><span data-stu-id="6de04-584">65</span></span></td>
<td><span data-ttu-id="6de04-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="6de04-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="6de04-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="6de04-586">5,297.69</span></span></td>
<td><span data-ttu-id="6de04-587">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-588">CC004</span><span class="sxs-lookup"><span data-stu-id="6de04-588">CC004</span></span></td>
<td><span data-ttu-id="6de04-589">Paketleme</span><span class="sxs-lookup"><span data-stu-id="6de04-589">Packaging</span></span></td>
<td><span data-ttu-id="6de04-590">35</span><span class="sxs-lookup"><span data-stu-id="6de04-590">35</span></span></td>
<td><span data-ttu-id="6de04-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="6de04-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="6de04-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="6de04-592">2,852.60</span></span></td>
<td><span data-ttu-id="6de04-593">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6de04-594">Aşağıdaki tablo, Derleme hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="6de04-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6de04-595">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="6de04-595">Cost object</span></span></th>
<th><span data-ttu-id="6de04-596">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="6de04-596">Magnitude</span></span></th>
<th><span data-ttu-id="6de04-597">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="6de04-597">Allocation factor</span></span></th>
<th><span data-ttu-id="6de04-598">Tutar</span><span class="sxs-lookup"><span data-stu-id="6de04-598">Amount</span></span></th>
<th><span data-ttu-id="6de04-599">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="6de04-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6de04-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6de04-600">Prod 1</span></span></td>
<td><span data-ttu-id="6de04-601">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="6de04-601">Product 1</span></span></td>
<td><span data-ttu-id="6de04-602">60</span><span class="sxs-lookup"><span data-stu-id="6de04-602">60</span></span></td>
<td><span data-ttu-id="6de04-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="6de04-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="6de04-604">535.31</span><span class="sxs-lookup"><span data-stu-id="6de04-604">535.31</span></span></td>
<td><span data-ttu-id="6de04-605">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6de04-606">Prod 2</span></span></td>
<td><span data-ttu-id="6de04-607">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="6de04-607">Product 2</span></span></td>
<td><span data-ttu-id="6de04-608">20</span><span class="sxs-lookup"><span data-stu-id="6de04-608">20</span></span></td>
<td><span data-ttu-id="6de04-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="6de04-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="6de04-610">178.44</span><span class="sxs-lookup"><span data-stu-id="6de04-610">178.44</span></span></td>
<td><span data-ttu-id="6de04-611">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6de04-612">Prod 1</span></span></td>
<td><span data-ttu-id="6de04-613">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="6de04-613">Product 1</span></span></td>
<td><span data-ttu-id="6de04-614">60</span><span class="sxs-lookup"><span data-stu-id="6de04-614">60</span></span></td>
<td><span data-ttu-id="6de04-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="6de04-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="6de04-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="6de04-616">4,487.12</span></span></td>
<td><span data-ttu-id="6de04-617">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6de04-618">Prod 2</span></span></td>
<td><span data-ttu-id="6de04-619">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="6de04-619">Product 2</span></span></td>
<td><span data-ttu-id="6de04-620">20</span><span class="sxs-lookup"><span data-stu-id="6de04-620">20</span></span></td>
<td><span data-ttu-id="6de04-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="6de04-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="6de04-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="6de04-622">1,495.71</span></span></td>
<td><span data-ttu-id="6de04-623">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6de04-624">Aşağıdaki tablo, Paketleme hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="6de04-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6de04-625">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="6de04-625">Cost object</span></span></th>
<th><span data-ttu-id="6de04-626">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="6de04-626">Magnitude</span></span></th>
<th><span data-ttu-id="6de04-627">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="6de04-627">Allocation factor</span></span></th>
<th><span data-ttu-id="6de04-628">Tutar</span><span class="sxs-lookup"><span data-stu-id="6de04-628">Amount</span></span></th>
<th><span data-ttu-id="6de04-629">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="6de04-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6de04-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6de04-630">Prod 1</span></span></td>
<td><span data-ttu-id="6de04-631">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="6de04-631">Product 1</span></span></td>
<td><span data-ttu-id="6de04-632">80</span><span class="sxs-lookup"><span data-stu-id="6de04-632">80</span></span></td>
<td><span data-ttu-id="6de04-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="6de04-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="6de04-634">241.05</span><span class="sxs-lookup"><span data-stu-id="6de04-634">241.05</span></span></td>
<td><span data-ttu-id="6de04-635">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6de04-636">Prod 2</span></span></td>
<td><span data-ttu-id="6de04-637">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="6de04-637">Product 2</span></span></td>
<td><span data-ttu-id="6de04-638">15</span><span class="sxs-lookup"><span data-stu-id="6de04-638">15</span></span></td>
<td><span data-ttu-id="6de04-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="6de04-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="6de04-640">45.20</span><span class="sxs-lookup"><span data-stu-id="6de04-640">45.20</span></span></td>
<td><span data-ttu-id="6de04-641">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6de04-642">Prod 1</span></span></td>
<td><span data-ttu-id="6de04-643">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="6de04-643">Product 1</span></span></td>
<td><span data-ttu-id="6de04-644">80</span><span class="sxs-lookup"><span data-stu-id="6de04-644">80</span></span></td>
<td><span data-ttu-id="6de04-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="6de04-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="6de04-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="6de04-646">2,507.09</span></span></td>
<td><span data-ttu-id="6de04-647">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6de04-648">Prod 2</span></span></td>
<td><span data-ttu-id="6de04-649">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="6de04-649">Product 2</span></span></td>
<td><span data-ttu-id="6de04-650">15</span><span class="sxs-lookup"><span data-stu-id="6de04-650">15</span></span></td>
<td><span data-ttu-id="6de04-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="6de04-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="6de04-652">470.08</span><span class="sxs-lookup"><span data-stu-id="6de04-652">470.08</span></span></td>
<td><span data-ttu-id="6de04-653">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="6de04-654">Günlük girişleri (maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="6de04-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6de04-655">Günlük</span><span class="sxs-lookup"><span data-stu-id="6de04-655">Journal</span></span></th>
<th><span data-ttu-id="6de04-656">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="6de04-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="6de04-657">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="6de04-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="6de04-658">Sürüm</span><span class="sxs-lookup"><span data-stu-id="6de04-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6de04-659">00004</span><span class="sxs-lookup"><span data-stu-id="6de04-659">00004</span></span></td>
<td><span data-ttu-id="6de04-660">Maliyet tahsisatı günlüğü</span><span class="sxs-lookup"><span data-stu-id="6de04-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="6de04-661">Mali</span><span class="sxs-lookup"><span data-stu-id="6de04-661">Fiscal</span></span></td>
<td><span data-ttu-id="6de04-662">2017</span><span class="sxs-lookup"><span data-stu-id="6de04-662">2017</span></span></td>
<td><span data-ttu-id="6de04-663">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="6de04-663">Period 1</span></span></td>
<td><span data-ttu-id="6de04-664">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="6de04-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="6de04-665">Günlük satırları</span><span class="sxs-lookup"><span data-stu-id="6de04-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6de04-666">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="6de04-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="6de04-667">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="6de04-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6de04-668">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="6de04-668">Cost element</span></span></th>
<th><span data-ttu-id="6de04-669">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="6de04-669">Cost behavior</span></span></th>
<th><span data-ttu-id="6de04-670">Tutar</span><span class="sxs-lookup"><span data-stu-id="6de04-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6de04-671">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="6de04-672">CC001</span><span class="sxs-lookup"><span data-stu-id="6de04-672">CC001</span></span></td>
<td><span data-ttu-id="6de04-673">İK</span><span class="sxs-lookup"><span data-stu-id="6de04-673">HR</span></span></td>
<td><span data-ttu-id="6de04-674">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-674">10001</span></span></td>
<td><span data-ttu-id="6de04-675">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-675">Electricity</span></span></td>
<td><span data-ttu-id="6de04-676">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-676">Fixed cost</span></span></td>
<td><span data-ttu-id="6de04-677">500.00</span><span class="sxs-lookup"><span data-stu-id="6de04-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-678">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="6de04-679">CC001</span><span class="sxs-lookup"><span data-stu-id="6de04-679">CC001</span></span></td>
<td><span data-ttu-id="6de04-680">İK</span><span class="sxs-lookup"><span data-stu-id="6de04-680">HR</span></span></td>
<td><span data-ttu-id="6de04-681">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-681">10001</span></span></td>
<td><span data-ttu-id="6de04-682">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-682">Electricity</span></span></td>
<td><span data-ttu-id="6de04-683">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-683">Variable cost</span></span></td>
<td><span data-ttu-id="6de04-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="6de04-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-685">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="6de04-686">CC002</span><span class="sxs-lookup"><span data-stu-id="6de04-686">CC002</span></span></td>
<td><span data-ttu-id="6de04-687">Finans</span><span class="sxs-lookup"><span data-stu-id="6de04-687">Finance</span></span></td>
<td><span data-ttu-id="6de04-688">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-688">10001</span></span></td>
<td><span data-ttu-id="6de04-689">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-689">Electricity</span></span></td>
<td><span data-ttu-id="6de04-690">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-690">Fixed cost</span></span></td>
<td><span data-ttu-id="6de04-691">675.00</span><span class="sxs-lookup"><span data-stu-id="6de04-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-692">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="6de04-693">CC002</span><span class="sxs-lookup"><span data-stu-id="6de04-693">CC002</span></span></td>
<td><span data-ttu-id="6de04-694">Finans</span><span class="sxs-lookup"><span data-stu-id="6de04-694">Finance</span></span></td>
<td><span data-ttu-id="6de04-695">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-695">10001</span></span></td>
<td><span data-ttu-id="6de04-696">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-696">Electricity</span></span></td>
<td><span data-ttu-id="6de04-697">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-697">Variable cost</span></span></td>
<td><span data-ttu-id="6de04-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="6de04-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-699">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="6de04-700">CC003</span><span class="sxs-lookup"><span data-stu-id="6de04-700">CC003</span></span></td>
<td><span data-ttu-id="6de04-701">Montaj</span><span class="sxs-lookup"><span data-stu-id="6de04-701">Assembly</span></span></td>
<td><span data-ttu-id="6de04-702">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-702">10001</span></span></td>
<td><span data-ttu-id="6de04-703">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-703">Electricity</span></span></td>
<td><span data-ttu-id="6de04-704">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-704">Fixed cost</span></span></td>
<td><span data-ttu-id="6de04-705">713.75</span><span class="sxs-lookup"><span data-stu-id="6de04-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-706">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="6de04-707">CC003</span><span class="sxs-lookup"><span data-stu-id="6de04-707">CC003</span></span></td>
<td><span data-ttu-id="6de04-708">Montaj</span><span class="sxs-lookup"><span data-stu-id="6de04-708">Assembly</span></span></td>
<td><span data-ttu-id="6de04-709">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-709">10001</span></span></td>
<td><span data-ttu-id="6de04-710">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-710">Electricity</span></span></td>
<td><span data-ttu-id="6de04-711">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-711">Variable cost</span></span></td>
<td><span data-ttu-id="6de04-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="6de04-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-713">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="6de04-714">CC003</span><span class="sxs-lookup"><span data-stu-id="6de04-714">CC003</span></span></td>
<td><span data-ttu-id="6de04-715">Paketleme</span><span class="sxs-lookup"><span data-stu-id="6de04-715">Packaging</span></span></td>
<td><span data-ttu-id="6de04-716">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-716">10001</span></span></td>
<td><span data-ttu-id="6de04-717">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-717">Electricity</span></span></td>
<td><span data-ttu-id="6de04-718">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-718">Fixed cost</span></span></td>
<td><span data-ttu-id="6de04-719">286.25</span><span class="sxs-lookup"><span data-stu-id="6de04-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-720">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="6de04-721">CC003</span><span class="sxs-lookup"><span data-stu-id="6de04-721">CC003</span></span></td>
<td><span data-ttu-id="6de04-722">Paketleme</span><span class="sxs-lookup"><span data-stu-id="6de04-722">Packaging</span></span></td>
<td><span data-ttu-id="6de04-723">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-723">10001</span></span></td>
<td><span data-ttu-id="6de04-724">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-724">Electricity</span></span></td>
<td><span data-ttu-id="6de04-725">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-725">Variable cost</span></span></td>
<td><span data-ttu-id="6de04-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="6de04-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-727">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="6de04-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6de04-728">Prod 1</span></span></td>
<td><span data-ttu-id="6de04-729">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="6de04-729">Product 1</span></span></td>
<td><span data-ttu-id="6de04-730">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-730">10001</span></span></td>
<td><span data-ttu-id="6de04-731">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-731">Electricity</span></span></td>
<td><span data-ttu-id="6de04-732">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-732">Fixed cost</span></span></td>
<td><span data-ttu-id="6de04-733">776.36</span><span class="sxs-lookup"><span data-stu-id="6de04-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-734">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="6de04-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6de04-735">Prod 1</span></span></td>
<td><span data-ttu-id="6de04-736">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="6de04-736">Product 1</span></span></td>
<td><span data-ttu-id="6de04-737">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-737">10001</span></span></td>
<td><span data-ttu-id="6de04-738">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-738">Electricity</span></span></td>
<td><span data-ttu-id="6de04-739">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-739">Variable cost</span></span></td>
<td><span data-ttu-id="6de04-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="6de04-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-741">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="6de04-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6de04-742">Prod 2</span></span></td>
<td><span data-ttu-id="6de04-743">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="6de04-743">Product 1</span></span></td>
<td><span data-ttu-id="6de04-744">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-744">10001</span></span></td>
<td><span data-ttu-id="6de04-745">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-745">Electricity</span></span></td>
<td><span data-ttu-id="6de04-746">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-746">Fixed cost</span></span></td>
<td><span data-ttu-id="6de04-747">223.64</span><span class="sxs-lookup"><span data-stu-id="6de04-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-748">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="6de04-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6de04-749">Prod 2</span></span></td>
<td><span data-ttu-id="6de04-750">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="6de04-750">Product 1</span></span></td>
<td><span data-ttu-id="6de04-751">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-751">10001</span></span></td>
<td><span data-ttu-id="6de04-752">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-752">Electricity</span></span></td>
<td><span data-ttu-id="6de04-753">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-753">Variable cost</span></span></td>
<td><span data-ttu-id="6de04-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="6de04-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="6de04-755">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="6de04-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="6de04-756">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="6de04-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="6de04-757">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="6de04-757">Cost element</span></span></th>
<th><span data-ttu-id="6de04-758">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="6de04-758">Cost behavior</span></span></th>
<th><span data-ttu-id="6de04-759">Tutar</span><span class="sxs-lookup"><span data-stu-id="6de04-759">Amount</span></span></th>
<th><span data-ttu-id="6de04-760">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="6de04-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6de04-761">CC001</span><span class="sxs-lookup"><span data-stu-id="6de04-761">CC001</span></span></td>
<td><span data-ttu-id="6de04-762">İK</span><span class="sxs-lookup"><span data-stu-id="6de04-762">HR</span></span></td>
<td><span data-ttu-id="6de04-763">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-763">10001</span></span></td>
<td><span data-ttu-id="6de04-764">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-764">Electricity</span></span></td>
<td><span data-ttu-id="6de04-765">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-765">Fixed cost</span></span></td>
<td><span data-ttu-id="6de04-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="6de04-766">-500.00</span></span></td>
<td><span data-ttu-id="6de04-767">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-768">CC002</span><span class="sxs-lookup"><span data-stu-id="6de04-768">CC002</span></span></td>
<td><span data-ttu-id="6de04-769">Finans</span><span class="sxs-lookup"><span data-stu-id="6de04-769">Finance</span></span></td>
<td><span data-ttu-id="6de04-770">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-770">10001</span></span></td>
<td><span data-ttu-id="6de04-771">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-771">Electricity</span></span></td>
<td><span data-ttu-id="6de04-772">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-772">Fixed cost</span></span></td>
<td><span data-ttu-id="6de04-773">175.00</span><span class="sxs-lookup"><span data-stu-id="6de04-773">175.00</span></span></td>
<td><span data-ttu-id="6de04-774">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-775">CC003</span><span class="sxs-lookup"><span data-stu-id="6de04-775">CC003</span></span></td>
<td><span data-ttu-id="6de04-776">Montaj</span><span class="sxs-lookup"><span data-stu-id="6de04-776">Assembly</span></span></td>
<td><span data-ttu-id="6de04-777">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-777">10001</span></span></td>
<td><span data-ttu-id="6de04-778">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-778">Electricity</span></span></td>
<td><span data-ttu-id="6de04-779">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-779">Fixed cost</span></span></td>
<td><span data-ttu-id="6de04-780">275.00</span><span class="sxs-lookup"><span data-stu-id="6de04-780">275.00</span></span></td>
<td><span data-ttu-id="6de04-781">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-782">CC004</span><span class="sxs-lookup"><span data-stu-id="6de04-782">CC004</span></span></td>
<td><span data-ttu-id="6de04-783">Paketleme</span><span class="sxs-lookup"><span data-stu-id="6de04-783">Packaging</span></span></td>
<td><span data-ttu-id="6de04-784">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-784">10001</span></span></td>
<td><span data-ttu-id="6de04-785">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-785">Electricity</span></span></td>
<td><span data-ttu-id="6de04-786">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-786">Fixed cost</span></span></td>
<td><span data-ttu-id="6de04-787">50,00</span><span class="sxs-lookup"><span data-stu-id="6de04-787">50,00</span></span></td>
<td><span data-ttu-id="6de04-788">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-789">CC001</span><span class="sxs-lookup"><span data-stu-id="6de04-789">CC001</span></span></td>
<td><span data-ttu-id="6de04-790">İK</span><span class="sxs-lookup"><span data-stu-id="6de04-790">HR</span></span></td>
<td><span data-ttu-id="6de04-791">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-791">10001</span></span></td>
<td><span data-ttu-id="6de04-792">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-792">Electricity</span></span></td>
<td><span data-ttu-id="6de04-793">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-793">Variable cost</span></span></td>
<td><span data-ttu-id="6de04-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="6de04-794">-1,245.71</span></span></td>
<td><span data-ttu-id="6de04-795">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-796">CC002</span><span class="sxs-lookup"><span data-stu-id="6de04-796">CC002</span></span></td>
<td><span data-ttu-id="6de04-797">Finans</span><span class="sxs-lookup"><span data-stu-id="6de04-797">Finance</span></span></td>
<td><span data-ttu-id="6de04-798">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-798">10001</span></span></td>
<td><span data-ttu-id="6de04-799">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-799">Electricity</span></span></td>
<td><span data-ttu-id="6de04-800">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-800">Variable cost</span></span></td>
<td><span data-ttu-id="6de04-801">436.00</span><span class="sxs-lookup"><span data-stu-id="6de04-801">436.00</span></span></td>
<td><span data-ttu-id="6de04-802">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-803">CC003</span><span class="sxs-lookup"><span data-stu-id="6de04-803">CC003</span></span></td>
<td><span data-ttu-id="6de04-804">Montaj</span><span class="sxs-lookup"><span data-stu-id="6de04-804">Assembly</span></span></td>
<td><span data-ttu-id="6de04-805">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-805">10001</span></span></td>
<td><span data-ttu-id="6de04-806">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-806">Electricity</span></span></td>
<td><span data-ttu-id="6de04-807">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-807">Variable cost</span></span></td>
<td><span data-ttu-id="6de04-808">685.14</span><span class="sxs-lookup"><span data-stu-id="6de04-808">685.14</span></span></td>
<td><span data-ttu-id="6de04-809">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-810">CC004</span><span class="sxs-lookup"><span data-stu-id="6de04-810">CC004</span></span></td>
<td><span data-ttu-id="6de04-811">Paketleme</span><span class="sxs-lookup"><span data-stu-id="6de04-811">Packaging</span></span></td>
<td><span data-ttu-id="6de04-812">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-812">10001</span></span></td>
<td><span data-ttu-id="6de04-813">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-813">Electricity</span></span></td>
<td><span data-ttu-id="6de04-814">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-814">Variable cost</span></span></td>
<td><span data-ttu-id="6de04-815">124.57</span><span class="sxs-lookup"><span data-stu-id="6de04-815">124.57</span></span></td>
<td><span data-ttu-id="6de04-816">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-817">CC002</span><span class="sxs-lookup"><span data-stu-id="6de04-817">CC002</span></span></td>
<td><span data-ttu-id="6de04-818">Finans</span><span class="sxs-lookup"><span data-stu-id="6de04-818">Finance</span></span></td>
<td><span data-ttu-id="6de04-819">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-819">10001</span></span></td>
<td><span data-ttu-id="6de04-820">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-820">Electricity</span></span></td>
<td><span data-ttu-id="6de04-821">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-821">Fixed cost</span></span></td>
<td><span data-ttu-id="6de04-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="6de04-822">-675.00</span></span></td>
<td><span data-ttu-id="6de04-823">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-824">CC003</span><span class="sxs-lookup"><span data-stu-id="6de04-824">CC003</span></span></td>
<td><span data-ttu-id="6de04-825">Montaj</span><span class="sxs-lookup"><span data-stu-id="6de04-825">Assembly</span></span></td>
<td><span data-ttu-id="6de04-826">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-826">10001</span></span></td>
<td><span data-ttu-id="6de04-827">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-827">Electricity</span></span></td>
<td><span data-ttu-id="6de04-828">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-828">Fixed cost</span></span></td>
<td><span data-ttu-id="6de04-829">438.75</span><span class="sxs-lookup"><span data-stu-id="6de04-829">438.75</span></span></td>
<td><span data-ttu-id="6de04-830">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-831">CC004</span><span class="sxs-lookup"><span data-stu-id="6de04-831">CC004</span></span></td>
<td><span data-ttu-id="6de04-832">Paketleme</span><span class="sxs-lookup"><span data-stu-id="6de04-832">Packaging</span></span></td>
<td><span data-ttu-id="6de04-833">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-833">10001</span></span></td>
<td><span data-ttu-id="6de04-834">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-834">Electricity</span></span></td>
<td><span data-ttu-id="6de04-835">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-835">Fixed cost</span></span></td>
<td><span data-ttu-id="6de04-836">236.25</span><span class="sxs-lookup"><span data-stu-id="6de04-836">236.25</span></span></td>
<td><span data-ttu-id="6de04-837">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-838">CC002</span><span class="sxs-lookup"><span data-stu-id="6de04-838">CC002</span></span></td>
<td><span data-ttu-id="6de04-839">Finans</span><span class="sxs-lookup"><span data-stu-id="6de04-839">Finance</span></span></td>
<td><span data-ttu-id="6de04-840">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-840">10001</span></span></td>
<td><span data-ttu-id="6de04-841">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-841">Electricity</span></span></td>
<td><span data-ttu-id="6de04-842">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-842">Variable cost</span></span></td>
<td><span data-ttu-id="6de04-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="6de04-843">-8,150.29</span></span></td>
<td><span data-ttu-id="6de04-844">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-845">CC003</span><span class="sxs-lookup"><span data-stu-id="6de04-845">CC003</span></span></td>
<td><span data-ttu-id="6de04-846">Montaj</span><span class="sxs-lookup"><span data-stu-id="6de04-846">Assembly</span></span></td>
<td><span data-ttu-id="6de04-847">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-847">10001</span></span></td>
<td><span data-ttu-id="6de04-848">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-848">Electricity</span></span></td>
<td><span data-ttu-id="6de04-849">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-849">Variable cost</span></span></td>
<td><span data-ttu-id="6de04-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="6de04-850">5,297.69</span></span></td>
<td><span data-ttu-id="6de04-851">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-852">CC004</span><span class="sxs-lookup"><span data-stu-id="6de04-852">CC004</span></span></td>
<td><span data-ttu-id="6de04-853">Paketleme</span><span class="sxs-lookup"><span data-stu-id="6de04-853">Packaging</span></span></td>
<td><span data-ttu-id="6de04-854">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-854">10001</span></span></td>
<td><span data-ttu-id="6de04-855">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-855">Electricity</span></span></td>
<td><span data-ttu-id="6de04-856">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-856">Variable cost</span></span></td>
<td><span data-ttu-id="6de04-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="6de04-857">2,852.60</span></span></td>
<td><span data-ttu-id="6de04-858">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-859">CC003</span><span class="sxs-lookup"><span data-stu-id="6de04-859">CC003</span></span></td>
<td><span data-ttu-id="6de04-860">Montaj</span><span class="sxs-lookup"><span data-stu-id="6de04-860">Assembly</span></span></td>
<td><span data-ttu-id="6de04-861">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-861">10001</span></span></td>
<td><span data-ttu-id="6de04-862">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-862">Electricity</span></span></td>
<td><span data-ttu-id="6de04-863">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-863">Fixed cost</span></span></td>
<td><span data-ttu-id="6de04-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="6de04-864">-713.75</span></span></td>
<td><span data-ttu-id="6de04-865">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6de04-866">Prod 1</span></span></td>
<td><span data-ttu-id="6de04-867">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="6de04-867">Product 1</span></span></td>
<td><span data-ttu-id="6de04-868">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-868">10001</span></span></td>
<td><span data-ttu-id="6de04-869">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-869">Electricity</span></span></td>
<td><span data-ttu-id="6de04-870">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-870">Fixed cost</span></span></td>
<td><span data-ttu-id="6de04-871">535.31</span><span class="sxs-lookup"><span data-stu-id="6de04-871">535.31</span></span></td>
<td><span data-ttu-id="6de04-872">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6de04-873">Prod 2</span></span></td>
<td><span data-ttu-id="6de04-874">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="6de04-874">Product 2</span></span></td>
<td><span data-ttu-id="6de04-875">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-875">10001</span></span></td>
<td><span data-ttu-id="6de04-876">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-876">Electricity</span></span></td>
<td><span data-ttu-id="6de04-877">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-877">Fixed cost</span></span></td>
<td><span data-ttu-id="6de04-878">178.44</span><span class="sxs-lookup"><span data-stu-id="6de04-878">178.44</span></span></td>
<td><span data-ttu-id="6de04-879">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-880">CC003</span><span class="sxs-lookup"><span data-stu-id="6de04-880">CC003</span></span></td>
<td><span data-ttu-id="6de04-881">Montaj</span><span class="sxs-lookup"><span data-stu-id="6de04-881">Assembly</span></span></td>
<td><span data-ttu-id="6de04-882">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-882">10001</span></span></td>
<td><span data-ttu-id="6de04-883">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-883">Electricity</span></span></td>
<td><span data-ttu-id="6de04-884">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-884">Variable cost</span></span></td>
<td><span data-ttu-id="6de04-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="6de04-885">-5,982.83</span></span></td>
<td><span data-ttu-id="6de04-886">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6de04-887">Prod 1</span></span></td>
<td><span data-ttu-id="6de04-888">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="6de04-888">Product 1</span></span></td>
<td><span data-ttu-id="6de04-889">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-889">10001</span></span></td>
<td><span data-ttu-id="6de04-890">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-890">Electricity</span></span></td>
<td><span data-ttu-id="6de04-891">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-891">Variable cost</span></span></td>
<td><span data-ttu-id="6de04-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="6de04-892">4,487.12</span></span></td>
<td><span data-ttu-id="6de04-893">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6de04-894">Prod 2</span></span></td>
<td><span data-ttu-id="6de04-895">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="6de04-895">Product 2</span></span></td>
<td><span data-ttu-id="6de04-896">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-896">10001</span></span></td>
<td><span data-ttu-id="6de04-897">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-897">Electricity</span></span></td>
<td><span data-ttu-id="6de04-898">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-898">Variable cost</span></span></td>
<td><span data-ttu-id="6de04-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="6de04-899">1,495.71</span></span></td>
<td><span data-ttu-id="6de04-900">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-901">CC003</span><span class="sxs-lookup"><span data-stu-id="6de04-901">CC003</span></span></td>
<td><span data-ttu-id="6de04-902">Montaj</span><span class="sxs-lookup"><span data-stu-id="6de04-902">Assembly</span></span></td>
<td><span data-ttu-id="6de04-903">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-903">10001</span></span></td>
<td><span data-ttu-id="6de04-904">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-904">Electricity</span></span></td>
<td><span data-ttu-id="6de04-905">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-905">Fixed cost</span></span></td>
<td><span data-ttu-id="6de04-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="6de04-906">-286.25</span></span></td>
<td><span data-ttu-id="6de04-907">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6de04-908">Prod 1</span></span></td>
<td><span data-ttu-id="6de04-909">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="6de04-909">Product 1</span></span></td>
<td><span data-ttu-id="6de04-910">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-910">10001</span></span></td>
<td><span data-ttu-id="6de04-911">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-911">Electricity</span></span></td>
<td><span data-ttu-id="6de04-912">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-912">Fixed cost</span></span></td>
<td><span data-ttu-id="6de04-913">241.05</span><span class="sxs-lookup"><span data-stu-id="6de04-913">241.05</span></span></td>
<td><span data-ttu-id="6de04-914">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6de04-915">Prod 2</span></span></td>
<td><span data-ttu-id="6de04-916">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="6de04-916">Product 2</span></span></td>
<td><span data-ttu-id="6de04-917">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-917">10001</span></span></td>
<td><span data-ttu-id="6de04-918">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-918">Electricity</span></span></td>
<td><span data-ttu-id="6de04-919">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-919">Fixed cost</span></span></td>
<td><span data-ttu-id="6de04-920">45.20</span><span class="sxs-lookup"><span data-stu-id="6de04-920">45.20</span></span></td>
<td><span data-ttu-id="6de04-921">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-922">CC003</span><span class="sxs-lookup"><span data-stu-id="6de04-922">CC003</span></span></td>
<td><span data-ttu-id="6de04-923">Montaj</span><span class="sxs-lookup"><span data-stu-id="6de04-923">Assembly</span></span></td>
<td><span data-ttu-id="6de04-924">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-924">10001</span></span></td>
<td><span data-ttu-id="6de04-925">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-925">Electricity</span></span></td>
<td><span data-ttu-id="6de04-926">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-926">Variable cost</span></span></td>
<td><span data-ttu-id="6de04-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="6de04-927">-2,977.17</span></span></td>
<td><span data-ttu-id="6de04-928">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6de04-929">Prod 1</span></span></td>
<td><span data-ttu-id="6de04-930">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="6de04-930">Product 1</span></span></td>
<td><span data-ttu-id="6de04-931">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-931">10001</span></span></td>
<td><span data-ttu-id="6de04-932">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-932">Electricity</span></span></td>
<td><span data-ttu-id="6de04-933">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-933">Variable cost</span></span></td>
<td><span data-ttu-id="6de04-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="6de04-934">2,507.09</span></span></td>
<td><span data-ttu-id="6de04-935">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6de04-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6de04-936">Prod 2</span></span></td>
<td><span data-ttu-id="6de04-937">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="6de04-937">Product 2</span></span></td>
<td><span data-ttu-id="6de04-938">10001</span><span class="sxs-lookup"><span data-stu-id="6de04-938">10001</span></span></td>
<td><span data-ttu-id="6de04-939">Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-939">Electricity</span></span></td>
<td><span data-ttu-id="6de04-940">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-940">Variable cost</span></span></td>
<td><span data-ttu-id="6de04-941">470.08</span><span class="sxs-lookup"><span data-stu-id="6de04-941">470.08</span></span></td>
<td><span data-ttu-id="6de04-942">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="6de04-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="6de04-943">Sonuç</span><span class="sxs-lookup"><span data-stu-id="6de04-943">Conclusion</span></span>
<span data-ttu-id="6de04-944">Mali muhasebede, Elektrik için 10.000,00 maliyet bir sözde maliyet merkezi kimliğine nakledilmiştir.</span><span class="sxs-lookup"><span data-stu-id="6de04-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="6de04-945">Bu nedenle, maliyet muhasebecileri bu maliyetin tahsis edilmesi gerektiğini bilirler.</span><span class="sxs-lookup"><span data-stu-id="6de04-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="6de04-946">Maliyet muhasebesinde, maliyetler kuruluş birimleri ve seviyeleri arasında, uygulanan kural ve ilkelere dayalı olarak akar.</span><span class="sxs-lookup"><span data-stu-id="6de04-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="6de04-947">Her maliyet, maliyetlerin tahsisatı için en iyi değerlendirmeyi sağlayan bir tahsisat tabanı ile ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="6de04-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="6de04-948">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="6de04-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="6de04-949">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="6de04-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="6de04-950">Toplam</span><span class="sxs-lookup"><span data-stu-id="6de04-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="6de04-951">CC099</span><span class="sxs-lookup"><span data-stu-id="6de04-951">CC099</span></span></th>
<th><span data-ttu-id="6de04-952">CC001</span><span class="sxs-lookup"><span data-stu-id="6de04-952">CC001</span></span></th>
<th><span data-ttu-id="6de04-953">CC002</span><span class="sxs-lookup"><span data-stu-id="6de04-953">CC002</span></span></th>
<th><span data-ttu-id="6de04-954">CC003</span><span class="sxs-lookup"><span data-stu-id="6de04-954">CC003</span></span></th>
<th><span data-ttu-id="6de04-955">CC004</span><span class="sxs-lookup"><span data-stu-id="6de04-955">CC004</span></span></th>
<th><span data-ttu-id="6de04-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="6de04-956">Proj 1</span></span></th>
<th><span data-ttu-id="6de04-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="6de04-957">Proj 2</span></span></th>
<th><span data-ttu-id="6de04-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="6de04-958">Prod 1</span></span></th>
<th><span data-ttu-id="6de04-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="6de04-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="6de04-960">10001 Elektrik</span><span class="sxs-lookup"><span data-stu-id="6de04-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6de04-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="6de04-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6de04-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="6de04-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6de04-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="6de04-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6de04-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="6de04-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="6de04-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="6de04-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6de04-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="6de04-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6de04-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="6de04-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6de04-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="6de04-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="6de04-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="6de04-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="6de04-970">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="6de04-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6de04-971">0,00</span><span class="sxs-lookup"><span data-stu-id="6de04-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="6de04-972">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6de04-973">0,00</span><span class="sxs-lookup"><span data-stu-id="6de04-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6de04-974">0,00</span><span class="sxs-lookup"><span data-stu-id="6de04-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6de04-975">0,00</span><span class="sxs-lookup"><span data-stu-id="6de04-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6de04-976">0,00</span><span class="sxs-lookup"><span data-stu-id="6de04-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6de04-977">0,00</span><span class="sxs-lookup"><span data-stu-id="6de04-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="6de04-978">776.36</span><span class="sxs-lookup"><span data-stu-id="6de04-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6de04-979">223.64</span><span class="sxs-lookup"><span data-stu-id="6de04-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6de04-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="6de04-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="6de04-981">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="6de04-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6de04-982">000</span><span class="sxs-lookup"><span data-stu-id="6de04-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6de04-983">0,00</span><span class="sxs-lookup"><span data-stu-id="6de04-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6de04-984">0,00</span><span class="sxs-lookup"><span data-stu-id="6de04-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6de04-985">0,00</span><span class="sxs-lookup"><span data-stu-id="6de04-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6de04-986">0,00</span><span class="sxs-lookup"><span data-stu-id="6de04-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6de04-987">30.00</span><span class="sxs-lookup"><span data-stu-id="6de04-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6de04-988">10,00</span><span class="sxs-lookup"><span data-stu-id="6de04-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6de04-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="6de04-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6de04-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="6de04-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="6de04-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="6de04-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="6de04-992">Bu konu, birincil maliyet öğesi, 10001 Elektrik'in maliyet nesneleri arasında nasıl aktığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6de04-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="6de04-993">Bu nedenle, bu genel gider maliyeti kuruluşun en düşük seviyesine tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="6de04-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="6de04-994">Başka bir deyişle, maliyet en alt düzeydeki maliyet nesnelerine aittir.</span><span class="sxs-lookup"><span data-stu-id="6de04-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="6de04-995">Maliyetin, maliyet nesneleri arasında görsel bir akışına ihtiyacınız varsa, maliyetin akışını görselleştirmek için maliyet toplamı ilke kurallarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6de04-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="6de04-996">Daha fazla bilgi için bkz. [Maliyet yuvarlama ilkesi ve genel gider hesaplaması](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="6de04-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



