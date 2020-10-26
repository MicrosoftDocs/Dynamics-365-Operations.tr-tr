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
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976487"
---
# <a name="overhead-calculation"></a><span data-ttu-id="90d0a-103">Genel gider hesaplaması</span><span class="sxs-lookup"><span data-stu-id="90d0a-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="90d0a-104">Bu konu, genel gider maliyetlerinin hesaplanması için tipik işlemleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="90d0a-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="90d0a-105">Terim tanımı</span><span class="sxs-lookup"><span data-stu-id="90d0a-105">Term definition</span></span>
---------------

<span data-ttu-id="90d0a-106">Genel gider maliyetleri bir işletmenin çalışması için normalde uygulanan, ancak doğrudan herhangi bir özel iş, faaliyet, ürün veya hizmete ilişkilendirilmemiş olan maliyetlerdir.</span><span class="sxs-lookup"><span data-stu-id="90d0a-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="90d0a-107">Genel gider maliyetleri kar sağlama faaliyetlerinin oluşturulması için kritik destek sağlar.</span><span class="sxs-lookup"><span data-stu-id="90d0a-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="90d0a-108">Aşağıda bazı genel gider örnekleri verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="90d0a-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="90d0a-109">Kira</span><span class="sxs-lookup"><span data-stu-id="90d0a-109">Rent</span></span>
-   <span data-ttu-id="90d0a-110">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-110">Electricity</span></span>
-   <span data-ttu-id="90d0a-111">Yönetim maaşları</span><span class="sxs-lookup"><span data-stu-id="90d0a-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="90d0a-112">Genel gider hesaplaması genel bakış</span><span class="sxs-lookup"><span data-stu-id="90d0a-112">Overhead calculation overview</span></span>
<span data-ttu-id="90d0a-113">Genel gider hesaplama, maliyet muhasebesi ilkelerini doğru sırayla çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="90d0a-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="90d0a-114">Maliyet muhasebesi ilkeleri değiştiyse veya belirli hatalar algılandıysa, genel gider hesaplamasını aynı mali dönem için birden fazla kez yürütebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="90d0a-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="90d0a-115">Her genel gider hesaplaması depolanır ve önceki sürümlerdeki hesaplamaları kıyaslamanıza olanak sağlayan, benzersiz bir sürüm kimliğine sahip olur.</span><span class="sxs-lookup"><span data-stu-id="90d0a-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="90d0a-116">Genel gider hesaplamasının oluşturduğu maliyet girişleri bir muhasebe tarihi alır.</span><span class="sxs-lookup"><span data-stu-id="90d0a-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="90d0a-117">Bu muhasebe tarihi, hesaplamada kullanılan mali dönemin bitiş tarihiyle eşleşir.</span><span class="sxs-lookup"><span data-stu-id="90d0a-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="90d0a-118">Benzersiz sürüm kimliği aşağıdaki öğelerden oluşur:</span><span class="sxs-lookup"><span data-stu-id="90d0a-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="90d0a-119">Sürüm türü</span><span class="sxs-lookup"><span data-stu-id="90d0a-119">Version type</span></span>
-   <span data-ttu-id="90d0a-120">Tarih ve saat</span><span class="sxs-lookup"><span data-stu-id="90d0a-120">Date and time</span></span>
-   <span data-ttu-id="90d0a-121">Maliyet muhasebesi defteri</span><span class="sxs-lookup"><span data-stu-id="90d0a-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="90d0a-122">Mali yıl</span><span class="sxs-lookup"><span data-stu-id="90d0a-122">Fiscal year</span></span>
-   <span data-ttu-id="90d0a-123">Mali dönem</span><span class="sxs-lookup"><span data-stu-id="90d0a-123">Fiscal period</span></span>

<span data-ttu-id="90d0a-124">Genel gider hesaplama, sürümden bağımsız olarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="90d0a-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="90d0a-125">Bu nedenle, Gerçek sürümden önce Bütçe sürümünü hesaplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="90d0a-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="90d0a-126">Genel gider hesaplama dört adımdan oluşur, aşağıdaki çizimde gösterildiği gibi.</span><span class="sxs-lookup"><span data-stu-id="90d0a-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="90d0a-127">Her adımda, günlük girişleri olan bir günlük başlığı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="90d0a-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="90d0a-128">Bu günlük başlığı, her hesaplama adımı için giriş verilerini tutar.</span><span class="sxs-lookup"><span data-stu-id="90d0a-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="90d0a-129">İlkeler ve kurallar her günlük satırına uygulanır ve maliyet girişleri çıkış olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="90d0a-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="90d0a-130">Bu nedenle, her zaman tam izlenebilirliğe sahip olursunuz.</span><span class="sxs-lookup"><span data-stu-id="90d0a-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="90d0a-131">[![Genel gider hesaplaması](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="90d0a-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="90d0a-132">Elektrik genel gideri maliyetini hesapla ve tahsis et</span><span class="sxs-lookup"><span data-stu-id="90d0a-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="90d0a-133">Mali muhasebede, elektrik gibi bazı maliyetler peşin ödeme olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="90d0a-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="90d0a-134">Bu nedenle, Maliyet muhasebesi için ayrıntılı yönetim bilgiler sağlanmaz.</span><span class="sxs-lookup"><span data-stu-id="90d0a-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="90d0a-135">Maliyet muhasebesinde doğru yönetimsel bilgileri tüm yönetim birim ve düzeylerinde sağlamak için, maliyetlerin kuruluş birimleri arasında akması gerekir.</span><span class="sxs-lookup"><span data-stu-id="90d0a-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="90d0a-136">Bu akış, tüketimin doğru bir kaydına ya da adil bir değerlendirmeye dayanıyor olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="90d0a-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="90d0a-137">Genel muhasebede, bir elektrik maliyeti aşağıdaki tabloda gösterildiği gibi deftere nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="90d0a-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="90d0a-138">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="90d0a-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="90d0a-139">Maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="90d0a-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="90d0a-140">Ana hesap</span><span class="sxs-lookup"><span data-stu-id="90d0a-140">Main account</span></span></th>
<th><span data-ttu-id="90d0a-141">Muhasebe para birimi cinsinden tutar</span><span class="sxs-lookup"><span data-stu-id="90d0a-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="90d0a-142">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="90d0a-143">CC099</span><span class="sxs-lookup"><span data-stu-id="90d0a-143">CC099</span></span></td>
<td><span data-ttu-id="90d0a-144">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="90d0a-144">Default cost center</span></span></td>
<td><span data-ttu-id="90d0a-145">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-145">10001</span></span></td>
<td><span data-ttu-id="90d0a-146">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-146">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="90d0a-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="90d0a-148">Adım 1: Maliyet davranışı hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="90d0a-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="90d0a-149">Varsayılan olarak, maliyeti girişleri kaynak veriden içeri alındığında, Maliyet muhasebesinde **Sınıflandırılmamış** maliyet davranışı sınıflandırmasını alırlar.</span><span class="sxs-lookup"><span data-stu-id="90d0a-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="90d0a-150">Maliyet davranışı ilke kuralları ekleyerek, maliyet girişlerini **Sabit maliyet** veya **Değişken maliyet** olarak yeniden sınıflandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="90d0a-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="90d0a-151">Maliyet davranış kuralını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="90d0a-151">Define the cost behavior rule</span></span>

<span data-ttu-id="90d0a-152">Bazı durumlarda, sabit bir ücret maliyet parçasıdır ve kalan maliyet, tüketime dayanır.</span><span class="sxs-lookup"><span data-stu-id="90d0a-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="90d0a-153">Elektrik faturaları genellikle bu tanıma uyar.</span><span class="sxs-lookup"><span data-stu-id="90d0a-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="90d0a-154">Belirli bir sabit ücret ödedikten sonra, kilovat saatlik (Kwh) tüketim başına ödeme yaparsınız.</span><span class="sxs-lookup"><span data-stu-id="90d0a-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="90d0a-155">Örneğin, sabit maliyet masrafı 1.000,00 ise, maliyet davranışı kural nasıl tanımlanır:</span><span class="sxs-lookup"><span data-stu-id="90d0a-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="90d0a-156">Sabit tutar 1.000,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="90d0a-157">0 &lt;= 1.000,00 = Sabit</span><span class="sxs-lookup"><span data-stu-id="90d0a-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="90d0a-158">1000,01 &lt; N = Değişken</span><span class="sxs-lookup"><span data-stu-id="90d0a-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="90d0a-159">Günlük</span><span class="sxs-lookup"><span data-stu-id="90d0a-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="90d0a-160">Günlük</span><span class="sxs-lookup"><span data-stu-id="90d0a-160">Journal</span></span></th>
<th><span data-ttu-id="90d0a-161">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="90d0a-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="90d0a-162">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="90d0a-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="90d0a-163">Sürüm</span><span class="sxs-lookup"><span data-stu-id="90d0a-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="90d0a-164">00001</span><span class="sxs-lookup"><span data-stu-id="90d0a-164">00001</span></span></td>
<td><span data-ttu-id="90d0a-165">Maliyet davranışı hesaplama günlüğü</span><span class="sxs-lookup"><span data-stu-id="90d0a-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="90d0a-166">Mali</span><span class="sxs-lookup"><span data-stu-id="90d0a-166">Fiscal</span></span></td>
<td><span data-ttu-id="90d0a-167">2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-167">2017</span></span></td>
<td><span data-ttu-id="90d0a-168">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-168">Period 1</span></span></td>
<td><span data-ttu-id="90d0a-169">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="90d0a-170">Günlük girişleri (Maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="90d0a-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="90d0a-171">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="90d0a-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="90d0a-172">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="90d0a-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="90d0a-173">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="90d0a-173">Cost element</span></span></th>
<th><span data-ttu-id="90d0a-174">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="90d0a-174">Cost behavior</span></span></th>
<th><span data-ttu-id="90d0a-175">Tutar</span><span class="sxs-lookup"><span data-stu-id="90d0a-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="90d0a-176">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="90d0a-177">CC099</span><span class="sxs-lookup"><span data-stu-id="90d0a-177">CC099</span></span></td>
<td><span data-ttu-id="90d0a-178">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="90d0a-178">Default cost center</span></span></td>
<td><span data-ttu-id="90d0a-179">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-179">10001</span></span></td>
<td><span data-ttu-id="90d0a-180">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-180">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-181">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="90d0a-181">Unclassified</span></span></td>
<td><span data-ttu-id="90d0a-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="90d0a-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="90d0a-183">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="90d0a-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="90d0a-184">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="90d0a-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="90d0a-185">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="90d0a-185">Cost element</span></span></th>
<th><span data-ttu-id="90d0a-186">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="90d0a-186">Cost behavior</span></span></th>
<th><span data-ttu-id="90d0a-187">Tutar</span><span class="sxs-lookup"><span data-stu-id="90d0a-187">Amount</span></span></th>
<th><span data-ttu-id="90d0a-188">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="90d0a-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="90d0a-189">CC099</span><span class="sxs-lookup"><span data-stu-id="90d0a-189">CC099</span></span></td>
<td><span data-ttu-id="90d0a-190">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="90d0a-190">Default cost center</span></span></td>
<td><span data-ttu-id="90d0a-191">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-191">10001</span></span></td>
<td><span data-ttu-id="90d0a-192">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-192">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-193">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="90d0a-193">Unclassified</span></span></td>
<td><span data-ttu-id="90d0a-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="90d0a-194">10,000.00</span></span></td>
<td><span data-ttu-id="90d0a-195">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-196">CC099</span><span class="sxs-lookup"><span data-stu-id="90d0a-196">CC099</span></span></td>
<td><span data-ttu-id="90d0a-197">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="90d0a-197">Default cost center</span></span></td>
<td><span data-ttu-id="90d0a-198">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-198">10001</span></span></td>
<td><span data-ttu-id="90d0a-199">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-199">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-200">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="90d0a-200">Unclassified</span></span></td>
<td><span data-ttu-id="90d0a-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-201">-10,000.00</span></span></td>
<td><span data-ttu-id="90d0a-202">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-203">CC099</span><span class="sxs-lookup"><span data-stu-id="90d0a-203">CC099</span></span></td>
<td><span data-ttu-id="90d0a-204">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="90d0a-204">Default cost center</span></span></td>
<td><span data-ttu-id="90d0a-205">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-205">10001</span></span></td>
<td><span data-ttu-id="90d0a-206">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-206">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-207">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-207">Fixed cost</span></span></td>
<td><span data-ttu-id="90d0a-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-208">1,000.00</span></span></td>
<td><span data-ttu-id="90d0a-209">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-210">CC099</span><span class="sxs-lookup"><span data-stu-id="90d0a-210">CC099</span></span></td>
<td><span data-ttu-id="90d0a-211">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="90d0a-211">Default cost center</span></span></td>
<td><span data-ttu-id="90d0a-212">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-212">10001</span></span></td>
<td><span data-ttu-id="90d0a-213">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-213">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-214">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-214">Variable cost</span></span></td>
<td><span data-ttu-id="90d0a-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="90d0a-215">9,000.00</span></span></td>
<td><span data-ttu-id="90d0a-216">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="90d0a-217">Daha fazla bilgi için bkz. [Maliyet davranışı ilkesi oluşturma ve bir maliyet kontrol birimine atama](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="90d0a-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="90d0a-218">Adım 2: Maliyet dağıtımı hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="90d0a-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="90d0a-219">Maliyet dağıtımı, bir nesneden bir veya daha fazlasına ilgili tahsisat tabanı uygulayarak maliyeti yeniden dağıtmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="90d0a-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="90d0a-220">Maliyet dağıtımı ve maliyet tahsisatı, maliyet dağıtımının her zaman orijinal maliyetin birincil maliyet öğesinde bulunmasıyla farklılık gösterir.</span><span class="sxs-lookup"><span data-stu-id="90d0a-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="90d0a-221">Maliyet dağıtım kuralını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="90d0a-221">Define the cost distribution rule</span></span>

<span data-ttu-id="90d0a-222">Mali muhasebede, elektrik maliyetleri çoğu zaman peşin ödeme olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="90d0a-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="90d0a-223">Maliyet muhasebesinde ise bu yöntem yeterince ayrıntılı değildir.</span><span class="sxs-lookup"><span data-stu-id="90d0a-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="90d0a-224">Değişken maliyet, maliyet nesnelerine tek tek, adil bir temele dayanarak dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="90d0a-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="90d0a-225">En mantıklı tahsisat, elektrik kullanımını (Kwh) temel alarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="90d0a-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="90d0a-226">Elektrik adına sahip, istatistiksel bir boyut üyesi oluşturulur ve elektrik tüketimi kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="90d0a-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="90d0a-227">Varsayıla olarak, tüm istatistiksel boyut üyeleri tahsisat tabanları olarak kullanılabilir hale gelir.</span><span class="sxs-lookup"><span data-stu-id="90d0a-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="90d0a-228">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="90d0a-228">Cost object</span></span></th>
<th><span data-ttu-id="90d0a-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="90d0a-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="90d0a-230">CC001</span><span class="sxs-lookup"><span data-stu-id="90d0a-230">CC001</span></span></td>
<td><span data-ttu-id="90d0a-231">İK</span><span class="sxs-lookup"><span data-stu-id="90d0a-231">HR</span></span></td>
<td><span data-ttu-id="90d0a-232">1.000</span><span class="sxs-lookup"><span data-stu-id="90d0a-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-233">CC002</span><span class="sxs-lookup"><span data-stu-id="90d0a-233">CC002</span></span></td>
<td><span data-ttu-id="90d0a-234">Finans</span><span class="sxs-lookup"><span data-stu-id="90d0a-234">Finance</span></span></td>
<td><span data-ttu-id="90d0a-235">6,000</span><span class="sxs-lookup"><span data-stu-id="90d0a-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-236">CC003</span><span class="sxs-lookup"><span data-stu-id="90d0a-236">CC003</span></span></td>
<td><span data-ttu-id="90d0a-237">Montaj</span><span class="sxs-lookup"><span data-stu-id="90d0a-237">Assembly</span></span></td>
<td><span data-ttu-id="90d0a-238">0</span><span class="sxs-lookup"><span data-stu-id="90d0a-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="90d0a-239">Aşağıdaki tablo, elektrik tüketiminin değişken maliyetler için bir tahsisat tabanlı olarak uygulandığındaki sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="90d0a-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="90d0a-240">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="90d0a-240">Cost object</span></span></th>
<th><span data-ttu-id="90d0a-241">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="90d0a-241">Magnitude</span></span></th>
<th><span data-ttu-id="90d0a-242">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="90d0a-242">Allocation factor</span></span></th>
<th><span data-ttu-id="90d0a-243">Tutar</span><span class="sxs-lookup"><span data-stu-id="90d0a-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="90d0a-244">CC001</span><span class="sxs-lookup"><span data-stu-id="90d0a-244">CC001</span></span></td>
<td><span data-ttu-id="90d0a-245">İK</span><span class="sxs-lookup"><span data-stu-id="90d0a-245">HR</span></span></td>
<td><span data-ttu-id="90d0a-246">1.000</span><span class="sxs-lookup"><span data-stu-id="90d0a-246">1,000</span></span></td>
<td><span data-ttu-id="90d0a-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="90d0a-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="90d0a-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-249">CC002</span><span class="sxs-lookup"><span data-stu-id="90d0a-249">CC002</span></span></td>
<td><span data-ttu-id="90d0a-250">Finans</span><span class="sxs-lookup"><span data-stu-id="90d0a-250">Finance</span></span></td>
<td><span data-ttu-id="90d0a-251">6,000</span><span class="sxs-lookup"><span data-stu-id="90d0a-251">6,000</span></span></td>
<td><span data-ttu-id="90d0a-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="90d0a-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="90d0a-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-254">CC003</span><span class="sxs-lookup"><span data-stu-id="90d0a-254">CC003</span></span></td>
<td><span data-ttu-id="90d0a-255">Montaj</span><span class="sxs-lookup"><span data-stu-id="90d0a-255">Assembly</span></span></td>
<td><span data-ttu-id="90d0a-256">0</span><span class="sxs-lookup"><span data-stu-id="90d0a-256">0</span></span></td>
<td><span data-ttu-id="90d0a-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="90d0a-258">0,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="90d0a-259">Sabit maliyet, elektrik tüketmiş olan tekil maliyet nesnelerine eşit miktarda dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="90d0a-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="90d0a-260">Bu sonuca, Elektrik istatistiksel boyut öğesini bir formül tahsisat tabanında kullanarak ulaşabilirsiniz: (Elektrik &gt; 0,00) Aşağıdaki tablo, elektrik tüketimi değişken maliyetler için bir tahsisat tabanı olarak kullanıldığında ortaya çıkan sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="90d0a-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="90d0a-261">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="90d0a-261">Cost object</span></span></th>
<th><span data-ttu-id="90d0a-262">Formül</span><span class="sxs-lookup"><span data-stu-id="90d0a-262">Formula</span></span></th>
<th><span data-ttu-id="90d0a-263">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="90d0a-263">Magnitude</span></span></th>
<th><span data-ttu-id="90d0a-264">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="90d0a-264">Allocation factor</span></span></th>
<th><span data-ttu-id="90d0a-265">Tutar</span><span class="sxs-lookup"><span data-stu-id="90d0a-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="90d0a-266">CC001</span><span class="sxs-lookup"><span data-stu-id="90d0a-266">CC001</span></span></td>
<td><span data-ttu-id="90d0a-267">İK</span><span class="sxs-lookup"><span data-stu-id="90d0a-267">HR</span></span></td>
<td><span data-ttu-id="90d0a-268">(1,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="90d0a-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="90d0a-269">1</span><span class="sxs-lookup"><span data-stu-id="90d0a-269">1</span></span></td>
<td><span data-ttu-id="90d0a-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="90d0a-271">500.00</span><span class="sxs-lookup"><span data-stu-id="90d0a-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-272">CC002</span><span class="sxs-lookup"><span data-stu-id="90d0a-272">CC002</span></span></td>
<td><span data-ttu-id="90d0a-273">Finans</span><span class="sxs-lookup"><span data-stu-id="90d0a-273">Finance</span></span></td>
<td><span data-ttu-id="90d0a-274">(6,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="90d0a-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="90d0a-275">1</span><span class="sxs-lookup"><span data-stu-id="90d0a-275">1</span></span></td>
<td><span data-ttu-id="90d0a-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="90d0a-277">500.00</span><span class="sxs-lookup"><span data-stu-id="90d0a-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-278">CC003</span><span class="sxs-lookup"><span data-stu-id="90d0a-278">CC003</span></span></td>
<td><span data-ttu-id="90d0a-279">Montaj</span><span class="sxs-lookup"><span data-stu-id="90d0a-279">Assembly</span></span></td>
<td><span data-ttu-id="90d0a-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="90d0a-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="90d0a-281">0</span><span class="sxs-lookup"><span data-stu-id="90d0a-281">0</span></span></td>
<td><span data-ttu-id="90d0a-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="90d0a-283">0,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="90d0a-284">Günlük</span><span class="sxs-lookup"><span data-stu-id="90d0a-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="90d0a-285">Günlük</span><span class="sxs-lookup"><span data-stu-id="90d0a-285">Journal</span></span></th>
<th><span data-ttu-id="90d0a-286">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="90d0a-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="90d0a-287">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="90d0a-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="90d0a-288">Sürüm</span><span class="sxs-lookup"><span data-stu-id="90d0a-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="90d0a-289">00002</span><span class="sxs-lookup"><span data-stu-id="90d0a-289">00002</span></span></td>
<td><span data-ttu-id="90d0a-290">Maliyet dağıtımı hesaplama günlüğü</span><span class="sxs-lookup"><span data-stu-id="90d0a-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="90d0a-291">Mali</span><span class="sxs-lookup"><span data-stu-id="90d0a-291">Fiscal</span></span></td>
<td><span data-ttu-id="90d0a-292">2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-292">2017</span></span></td>
<td><span data-ttu-id="90d0a-293">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-293">Period 1</span></span></td>
<td><span data-ttu-id="90d0a-294">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="90d0a-295">Günlük girişleri (Maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="90d0a-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="90d0a-296">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="90d0a-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="90d0a-297">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="90d0a-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="90d0a-298">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="90d0a-298">Cost element</span></span></th>
<th><span data-ttu-id="90d0a-299">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="90d0a-299">Cost behavior</span></span></th>
<th><span data-ttu-id="90d0a-300">Tutar</span><span class="sxs-lookup"><span data-stu-id="90d0a-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="90d0a-301">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="90d0a-302">CC099</span><span class="sxs-lookup"><span data-stu-id="90d0a-302">CC099</span></span></td>
<td><span data-ttu-id="90d0a-303">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="90d0a-303">Default cost center</span></span></td>
<td><span data-ttu-id="90d0a-304">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-304">10001</span></span></td>
<td><span data-ttu-id="90d0a-305">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-305">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-306">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-306">Fixed cost</span></span></td>
<td><span data-ttu-id="90d0a-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-308">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="90d0a-309">CC099</span><span class="sxs-lookup"><span data-stu-id="90d0a-309">CC099</span></span></td>
<td><span data-ttu-id="90d0a-310">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="90d0a-310">Default cost center</span></span></td>
<td><span data-ttu-id="90d0a-311">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-311">10001</span></span></td>
<td><span data-ttu-id="90d0a-312">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-312">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-313">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-313">Variable cost</span></span></td>
<td><span data-ttu-id="90d0a-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="90d0a-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="90d0a-315">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="90d0a-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="90d0a-316">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="90d0a-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="90d0a-317">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="90d0a-317">Cost element</span></span></th>
<th><span data-ttu-id="90d0a-318">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="90d0a-318">Cost behavior</span></span></th>
<th><span data-ttu-id="90d0a-319">Tutar</span><span class="sxs-lookup"><span data-stu-id="90d0a-319">Amount</span></span></th>
<th><span data-ttu-id="90d0a-320">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="90d0a-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="90d0a-321">CC099</span><span class="sxs-lookup"><span data-stu-id="90d0a-321">CC099</span></span></td>
<td><span data-ttu-id="90d0a-322">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="90d0a-322">Default cost center</span></span></td>
<td><span data-ttu-id="90d0a-323">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-323">10001</span></span></td>
<td><span data-ttu-id="90d0a-324">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-324">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-325">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-325">Fixed cost</span></span></td>
<td><span data-ttu-id="90d0a-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-326">-1,000.00</span></span></td>
<td><span data-ttu-id="90d0a-327">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-328">CC001</span><span class="sxs-lookup"><span data-stu-id="90d0a-328">CC001</span></span></td>
<td><span data-ttu-id="90d0a-329">İK</span><span class="sxs-lookup"><span data-stu-id="90d0a-329">HR</span></span></td>
<td><span data-ttu-id="90d0a-330">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-330">10001</span></span></td>
<td><span data-ttu-id="90d0a-331">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-331">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-332">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-332">Fixed cost</span></span></td>
<td><span data-ttu-id="90d0a-333">500.00</span><span class="sxs-lookup"><span data-stu-id="90d0a-333">500.00</span></span></td>
<td><span data-ttu-id="90d0a-334">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-335">CC002</span><span class="sxs-lookup"><span data-stu-id="90d0a-335">CC002</span></span></td>
<td><span data-ttu-id="90d0a-336">Finans</span><span class="sxs-lookup"><span data-stu-id="90d0a-336">Finance</span></span></td>
<td><span data-ttu-id="90d0a-337">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-337">10001</span></span></td>
<td><span data-ttu-id="90d0a-338">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-338">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-339">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-339">Fixed cost</span></span></td>
<td><span data-ttu-id="90d0a-340">500.00</span><span class="sxs-lookup"><span data-stu-id="90d0a-340">500.00</span></span></td>
<td><span data-ttu-id="90d0a-341">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-342">CC099</span><span class="sxs-lookup"><span data-stu-id="90d0a-342">CC099</span></span></td>
<td><span data-ttu-id="90d0a-343">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="90d0a-343">Default cost center</span></span></td>
<td><span data-ttu-id="90d0a-344">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-344">10001</span></span></td>
<td><span data-ttu-id="90d0a-345">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-345">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-346">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-346">Variable cost</span></span></td>
<td><span data-ttu-id="90d0a-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-347">-9,000.00</span></span></td>
<td><span data-ttu-id="90d0a-348">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-349">CC001</span><span class="sxs-lookup"><span data-stu-id="90d0a-349">CC001</span></span></td>
<td><span data-ttu-id="90d0a-350">İK</span><span class="sxs-lookup"><span data-stu-id="90d0a-350">HR</span></span></td>
<td><span data-ttu-id="90d0a-351">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-351">10001</span></span></td>
<td><span data-ttu-id="90d0a-352">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-352">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-353">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-353">Variable cost</span></span></td>
<td><span data-ttu-id="90d0a-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="90d0a-354">1,285.71</span></span></td>
<td><span data-ttu-id="90d0a-355">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-356">CC002</span><span class="sxs-lookup"><span data-stu-id="90d0a-356">CC002</span></span></td>
<td><span data-ttu-id="90d0a-357">Finans</span><span class="sxs-lookup"><span data-stu-id="90d0a-357">Finance</span></span></td>
<td><span data-ttu-id="90d0a-358">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-358">10001</span></span></td>
<td><span data-ttu-id="90d0a-359">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-359">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-360">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-360">Variable cost</span></span></td>
<td><span data-ttu-id="90d0a-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="90d0a-361">7,714.29</span></span></td>
<td><span data-ttu-id="90d0a-362">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="90d0a-363">Daha fazla bilgi için bkz. [Maliyet dağıtımı ilkesi oluşturma ve bir maliyet kontrol birimine atama](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="90d0a-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="90d0a-364">Adım 3: Genel gider oranı hesaplama işlemi</span><span class="sxs-lookup"><span data-stu-id="90d0a-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="90d0a-365">Genel gider oranı, bir veya birden fazla belirli maliyet nesnesine masraf yüklemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="90d0a-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="90d0a-366">Masraf, önceden belirlenmiş maliyet oranına ve tahsisat tabanından hesaplanan büyüklüğe dayanır.</span><span class="sxs-lookup"><span data-stu-id="90d0a-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="90d0a-367">Genel gider oranını tanımlama</span><span class="sxs-lookup"><span data-stu-id="90d0a-367">Define the overhead rate</span></span>

<span data-ttu-id="90d0a-368">Maliyet nesnesi CC001 HR, bir dizi dahili projeye katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="90d0a-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="90d0a-369">HR projeleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="90d0a-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="90d0a-370">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="90d0a-370">Cost object</span></span></th>
<th><span data-ttu-id="90d0a-371">Saatler</span><span class="sxs-lookup"><span data-stu-id="90d0a-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="90d0a-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-372">Proj 1</span></span></td>
<td><span data-ttu-id="90d0a-373">Proje 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-373">Project 1</span></span></td>
<td><span data-ttu-id="90d0a-374">3</span><span class="sxs-lookup"><span data-stu-id="90d0a-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="90d0a-375">Proj 2</span></span></td>
<td><span data-ttu-id="90d0a-376">Proje 2</span><span class="sxs-lookup"><span data-stu-id="90d0a-376">Project 2</span></span></td>
<td><span data-ttu-id="90d0a-377">1</span><span class="sxs-lookup"><span data-stu-id="90d0a-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="90d0a-378">Maliyet projeleri dağıtımı için bir önceden belirlenmiş maliyet oranı tanımlandı.</span><span class="sxs-lookup"><span data-stu-id="90d0a-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="90d0a-379">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="90d0a-379">Cost object</span></span></th>
<th><span data-ttu-id="90d0a-380">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="90d0a-380">Cost element</span></span></th>
<th><span data-ttu-id="90d0a-381">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="90d0a-381">Cost behavior</span></span></th>
<th><span data-ttu-id="90d0a-382">Birimler</span><span class="sxs-lookup"><span data-stu-id="90d0a-382">Units</span></span></th>
<th><span data-ttu-id="90d0a-383">Ücret</span><span class="sxs-lookup"><span data-stu-id="90d0a-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="90d0a-384">CC001</span><span class="sxs-lookup"><span data-stu-id="90d0a-384">CC001</span></span></td>
<td><span data-ttu-id="90d0a-385">İK</span><span class="sxs-lookup"><span data-stu-id="90d0a-385">HR</span></span></td>
<td><span data-ttu-id="90d0a-386">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-386">10001</span></span></td>
<td><span data-ttu-id="90d0a-387">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-387">Variable cost</span></span></td>
<td><span data-ttu-id="90d0a-388">1</span><span class="sxs-lookup"><span data-stu-id="90d0a-388">1</span></span></td>
<td><span data-ttu-id="90d0a-389">10</span><span class="sxs-lookup"><span data-stu-id="90d0a-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="90d0a-390">Aşağıdaki tablo, HR projeleri bir tahsisat tabanı olarak uygulandığındaki sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="90d0a-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="90d0a-391">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="90d0a-391">Cost object</span></span></th>
<th><span data-ttu-id="90d0a-392">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="90d0a-392">Magnitude</span></span></th>
<th><span data-ttu-id="90d0a-393">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="90d0a-393">Cost element</span></span></th>
<th><span data-ttu-id="90d0a-394">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="90d0a-394">Allocation factor</span></span></th>
<th><span data-ttu-id="90d0a-395">Tutar</span><span class="sxs-lookup"><span data-stu-id="90d0a-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="90d0a-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-396">Proj 1</span></span></td>
<td><span data-ttu-id="90d0a-397">Proje 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-397">Project 1</span></span></td>
<td><span data-ttu-id="90d0a-398">3</span><span class="sxs-lookup"><span data-stu-id="90d0a-398">3</span></span></td>
<td><span data-ttu-id="90d0a-399">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-399">10001</span></span></td>
<td><span data-ttu-id="90d0a-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="90d0a-401">30.00</span><span class="sxs-lookup"><span data-stu-id="90d0a-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="90d0a-402">Proj 2</span></span></td>
<td><span data-ttu-id="90d0a-403">Proje 2</span><span class="sxs-lookup"><span data-stu-id="90d0a-403">Project 2</span></span></td>
<td><span data-ttu-id="90d0a-404">1</span><span class="sxs-lookup"><span data-stu-id="90d0a-404">1</span></span></td>
<td><span data-ttu-id="90d0a-405">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-405">10001</span></span></td>
<td><span data-ttu-id="90d0a-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="90d0a-407">10,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="90d0a-408">Günlük</span><span class="sxs-lookup"><span data-stu-id="90d0a-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="90d0a-409">Günlük</span><span class="sxs-lookup"><span data-stu-id="90d0a-409">Journal</span></span></th>
<th><span data-ttu-id="90d0a-410">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="90d0a-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="90d0a-411">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="90d0a-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="90d0a-412">Sürüm</span><span class="sxs-lookup"><span data-stu-id="90d0a-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="90d0a-413">00003</span><span class="sxs-lookup"><span data-stu-id="90d0a-413">00003</span></span></td>
<td><span data-ttu-id="90d0a-414">Genel gider oranı hesaplaması günlüğü</span><span class="sxs-lookup"><span data-stu-id="90d0a-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="90d0a-415">Mali</span><span class="sxs-lookup"><span data-stu-id="90d0a-415">Fiscal</span></span></td>
<td><span data-ttu-id="90d0a-416">2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-416">2017</span></span></td>
<td><span data-ttu-id="90d0a-417">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-417">Period 1</span></span></td>
<td><span data-ttu-id="90d0a-418">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="90d0a-419">Günlük girişleri (Genel gider oranı hesaplaması için günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="90d0a-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="90d0a-420">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="90d0a-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="90d0a-421">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="90d0a-421">Cost object</span></span></th>
<th><span data-ttu-id="90d0a-422">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="90d0a-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="90d0a-423">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="90d0a-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-424">Proj 1</span></span></td>
<td><span data-ttu-id="90d0a-425">Dahili Proj 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="90d0a-426">3,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-427">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="90d0a-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="90d0a-428">Proj 2</span></span></td>
<td><span data-ttu-id="90d0a-429">Dahili Proj 2</span><span class="sxs-lookup"><span data-stu-id="90d0a-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="90d0a-430">1.00</span><span class="sxs-lookup"><span data-stu-id="90d0a-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="90d0a-431">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="90d0a-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="90d0a-432">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="90d0a-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="90d0a-433">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="90d0a-433">Cost element</span></span></th>
<th><span data-ttu-id="90d0a-434">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="90d0a-434">Cost behavior</span></span></th>
<th><span data-ttu-id="90d0a-435">Tutar</span><span class="sxs-lookup"><span data-stu-id="90d0a-435">Amount</span></span></th>
<th><span data-ttu-id="90d0a-436">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="90d0a-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="90d0a-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="90d0a-437">CC0001</span></span></td>
<td><span data-ttu-id="90d0a-438">İK</span><span class="sxs-lookup"><span data-stu-id="90d0a-438">HR</span></span></td>
<td><span data-ttu-id="90d0a-439">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-439">10001</span></span></td>
<td><span data-ttu-id="90d0a-440">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-440">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-441">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-441">Variable cost</span></span></td>
<td><span data-ttu-id="90d0a-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-442">-30.00</span></span></td>
<td><span data-ttu-id="90d0a-443">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-444">Proj 1</span></span></td>
<td><span data-ttu-id="90d0a-445">Dahili Proj 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="90d0a-446">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-446">10001</span></span></td>
<td><span data-ttu-id="90d0a-447">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-447">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-448">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-448">Variable cost</span></span></td>
<td><span data-ttu-id="90d0a-449">30.00</span><span class="sxs-lookup"><span data-stu-id="90d0a-449">30.00</span></span></td>
<td><span data-ttu-id="90d0a-450">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-451">CC001</span><span class="sxs-lookup"><span data-stu-id="90d0a-451">CC001</span></span></td>
<td><span data-ttu-id="90d0a-452">İK</span><span class="sxs-lookup"><span data-stu-id="90d0a-452">HR</span></span></td>
<td><span data-ttu-id="90d0a-453">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-453">10001</span></span></td>
<td><span data-ttu-id="90d0a-454">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-454">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-455">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-455">Variable cost</span></span></td>
<td><span data-ttu-id="90d0a-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-456">-10.00</span></span></td>
<td><span data-ttu-id="90d0a-457">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="90d0a-458">Proj 2</span></span></td>
<td><span data-ttu-id="90d0a-459">Dahili Proj 2</span><span class="sxs-lookup"><span data-stu-id="90d0a-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="90d0a-460">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-460">10001</span></span></td>
<td><span data-ttu-id="90d0a-461">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-461">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-462">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-462">Variable cost</span></span></td>
<td><span data-ttu-id="90d0a-463">10,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-463">10.00</span></span></td>
<td><span data-ttu-id="90d0a-464">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="90d0a-465">Daha fazla bilgi için [Genel gider hesaplaması gerçekleştir](cost-rollup.md#perform-overhead-calculation) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="90d0a-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="90d0a-466">Adım 4: Maliyet tahsisat hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="90d0a-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="90d0a-467">Tahsisat, bir tahsisat tabanı kullanarak bir maliyet nesnesinin diğer maliyet nesnelerine bakiyesini tahsis eder.</span><span class="sxs-lookup"><span data-stu-id="90d0a-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="90d0a-468">Finance karşılıklı tahsisat yöntemini desteklemektedir.</span><span class="sxs-lookup"><span data-stu-id="90d0a-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="90d0a-469">Karşılıklı tahsisat yönteminde, yardımcı maliyet nesnelerinin değiştiği karşılıklı hizmetler tümüyle tanınır.</span><span class="sxs-lookup"><span data-stu-id="90d0a-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="90d0a-470">Sistem, tahsisatların doğru gerçekleştireceği sırayı otomatik olarak belirler.</span><span class="sxs-lookup"><span data-stu-id="90d0a-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="90d0a-471">Bir maliyet nesnesinin bakiyesi tek bir tahsisat tabanı tarafından tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="90d0a-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="90d0a-472">Yeni maliyet nesnesi boyutları arasındaki tahsisatlar ve onların üyeleri desteklenir.</span><span class="sxs-lookup"><span data-stu-id="90d0a-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="90d0a-473">Tahsisatın sırası, maliyet kontrol birimi tarafından kontrol edilir.</span><span class="sxs-lookup"><span data-stu-id="90d0a-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="90d0a-474">[![Karşılıklı yöntemi](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="90d0a-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="90d0a-475">Maliyet tahsisatını tanımla</span><span class="sxs-lookup"><span data-stu-id="90d0a-475">Define the cost allocation</span></span>

<span data-ttu-id="90d0a-476">Bir maliyetin akışını nasıl izleyeceğinize dair basit bir örnek aşağıda verilmiştir,</span><span class="sxs-lookup"><span data-stu-id="90d0a-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="90d0a-477">Maliyet nesnesi CC001 HR, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="90d0a-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="90d0a-478">HR hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="90d0a-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="90d0a-479">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="90d0a-479">Cost object</span></span></th>
<th><span data-ttu-id="90d0a-480">HR hizmetleri</span><span class="sxs-lookup"><span data-stu-id="90d0a-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="90d0a-481">CC002</span><span class="sxs-lookup"><span data-stu-id="90d0a-481">CC002</span></span></td>
<td><span data-ttu-id="90d0a-482">Finans</span><span class="sxs-lookup"><span data-stu-id="90d0a-482">Finance</span></span></td>
<td><span data-ttu-id="90d0a-483">35</span><span class="sxs-lookup"><span data-stu-id="90d0a-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-484">CC003</span><span class="sxs-lookup"><span data-stu-id="90d0a-484">CC003</span></span></td>
<td><span data-ttu-id="90d0a-485">Montaj</span><span class="sxs-lookup"><span data-stu-id="90d0a-485">Assembly</span></span></td>
<td><span data-ttu-id="90d0a-486">55</span><span class="sxs-lookup"><span data-stu-id="90d0a-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-487">CC004</span><span class="sxs-lookup"><span data-stu-id="90d0a-487">CC004</span></span></td>
<td><span data-ttu-id="90d0a-488">Paketleme</span><span class="sxs-lookup"><span data-stu-id="90d0a-488">Packaging</span></span></td>
<td><span data-ttu-id="90d0a-489">10</span><span class="sxs-lookup"><span data-stu-id="90d0a-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="90d0a-490">Maliyet nesnesi CC002 Finans, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="90d0a-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="90d0a-491">Finans hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="90d0a-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="90d0a-492">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="90d0a-492">Cost object</span></span></th>
<th><span data-ttu-id="90d0a-493">Finans hizmetleri</span><span class="sxs-lookup"><span data-stu-id="90d0a-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="90d0a-494">CC003</span><span class="sxs-lookup"><span data-stu-id="90d0a-494">CC003</span></span></td>
<td><span data-ttu-id="90d0a-495">Montaj</span><span class="sxs-lookup"><span data-stu-id="90d0a-495">Assembly</span></span></td>
<td><span data-ttu-id="90d0a-496">65</span><span class="sxs-lookup"><span data-stu-id="90d0a-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-497">CC004</span><span class="sxs-lookup"><span data-stu-id="90d0a-497">CC004</span></span></td>
<td><span data-ttu-id="90d0a-498">Paketleme</span><span class="sxs-lookup"><span data-stu-id="90d0a-498">Packaging</span></span></td>
<td><span data-ttu-id="90d0a-499">35</span><span class="sxs-lookup"><span data-stu-id="90d0a-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="90d0a-500">Maliyet nesnesi CC003 Derleme, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="90d0a-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="90d0a-501">Derleme hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="90d0a-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="90d0a-502">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="90d0a-502">Cost object</span></span></th>
<th><span data-ttu-id="90d0a-503">Derleme Hizmetleri (saat)</span><span class="sxs-lookup"><span data-stu-id="90d0a-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="90d0a-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-504">Prod 1</span></span></td>
<td><span data-ttu-id="90d0a-505">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-505">Product 1</span></span></td>
<td><span data-ttu-id="90d0a-506">60</span><span class="sxs-lookup"><span data-stu-id="90d0a-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="90d0a-507">Prod 2</span></span></td>
<td><span data-ttu-id="90d0a-508">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="90d0a-508">Product 2</span></span></td>
<td><span data-ttu-id="90d0a-509">20</span><span class="sxs-lookup"><span data-stu-id="90d0a-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="90d0a-510">Maliyet nesnesi CC004 Ambalajlama, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="90d0a-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="90d0a-511">Ambalajlama hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="90d0a-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="90d0a-512">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="90d0a-512">Cost object</span></span></th>
<th><span data-ttu-id="90d0a-513">Ambalajlama hizmetleri (saat)</span><span class="sxs-lookup"><span data-stu-id="90d0a-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="90d0a-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-514">Prod 1</span></span></td>
<td><span data-ttu-id="90d0a-515">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-515">Product 1</span></span></td>
<td><span data-ttu-id="90d0a-516">80</span><span class="sxs-lookup"><span data-stu-id="90d0a-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="90d0a-517">Prod 2</span></span></td>
<td><span data-ttu-id="90d0a-518">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="90d0a-518">Product 2</span></span></td>
<td><span data-ttu-id="90d0a-519">15</span><span class="sxs-lookup"><span data-stu-id="90d0a-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="90d0a-520">Bir ürünün tükettiği üretim saatleri gibi istatistiki ölçümler, doğrudan kaynak verilerinden alınabilir.</span><span class="sxs-lookup"><span data-stu-id="90d0a-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="90d0a-521">Daha fazla bilgi için, [İstatistiksel ölçüm sağlayıcı şablonu](statistical-measure-provider-template.md#statistical-measure-provider-template) bakın.</span><span class="sxs-lookup"><span data-stu-id="90d0a-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="90d0a-522">Aşağıdaki tablo, İK hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığında ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="90d0a-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="90d0a-523">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="90d0a-523">Cost object</span></span></th>
<th><span data-ttu-id="90d0a-524">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="90d0a-524">Magnitude</span></span></th>
<th><span data-ttu-id="90d0a-525">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="90d0a-525">Allocation factor</span></span></th>
<th><span data-ttu-id="90d0a-526">Tutar</span><span class="sxs-lookup"><span data-stu-id="90d0a-526">Amount</span></span></th>
<th><span data-ttu-id="90d0a-527">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="90d0a-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="90d0a-528">CC002</span><span class="sxs-lookup"><span data-stu-id="90d0a-528">CC002</span></span></td>
<td><span data-ttu-id="90d0a-529">Finans</span><span class="sxs-lookup"><span data-stu-id="90d0a-529">Finance</span></span></td>
<td><span data-ttu-id="90d0a-530">35</span><span class="sxs-lookup"><span data-stu-id="90d0a-530">35</span></span></td>
<td><span data-ttu-id="90d0a-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="90d0a-532">175.00</span><span class="sxs-lookup"><span data-stu-id="90d0a-532">175.00</span></span></td>
<td><span data-ttu-id="90d0a-533">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-534">CC003</span><span class="sxs-lookup"><span data-stu-id="90d0a-534">CC003</span></span></td>
<td><span data-ttu-id="90d0a-535">Montaj</span><span class="sxs-lookup"><span data-stu-id="90d0a-535">Assembly</span></span></td>
<td><span data-ttu-id="90d0a-536">55</span><span class="sxs-lookup"><span data-stu-id="90d0a-536">55</span></span></td>
<td><span data-ttu-id="90d0a-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="90d0a-538">275.00</span><span class="sxs-lookup"><span data-stu-id="90d0a-538">275.00</span></span></td>
<td><span data-ttu-id="90d0a-539">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-540">CC004</span><span class="sxs-lookup"><span data-stu-id="90d0a-540">CC004</span></span></td>
<td><span data-ttu-id="90d0a-541">Paketleme</span><span class="sxs-lookup"><span data-stu-id="90d0a-541">Packaging</span></span></td>
<td><span data-ttu-id="90d0a-542">10</span><span class="sxs-lookup"><span data-stu-id="90d0a-542">10</span></span></td>
<td><span data-ttu-id="90d0a-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="90d0a-544">50,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-544">50.00</span></span></td>
<td><span data-ttu-id="90d0a-545">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-546">CC002</span><span class="sxs-lookup"><span data-stu-id="90d0a-546">CC002</span></span></td>
<td><span data-ttu-id="90d0a-547">Finans</span><span class="sxs-lookup"><span data-stu-id="90d0a-547">Finance</span></span></td>
<td><span data-ttu-id="90d0a-548">35</span><span class="sxs-lookup"><span data-stu-id="90d0a-548">35</span></span></td>
<td><span data-ttu-id="90d0a-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="90d0a-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="90d0a-550">436.00</span><span class="sxs-lookup"><span data-stu-id="90d0a-550">436.00</span></span></td>
<td><span data-ttu-id="90d0a-551">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-552">CC003</span><span class="sxs-lookup"><span data-stu-id="90d0a-552">CC003</span></span></td>
<td><span data-ttu-id="90d0a-553">Montaj</span><span class="sxs-lookup"><span data-stu-id="90d0a-553">Assembly</span></span></td>
<td><span data-ttu-id="90d0a-554">55</span><span class="sxs-lookup"><span data-stu-id="90d0a-554">55</span></span></td>
<td><span data-ttu-id="90d0a-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="90d0a-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="90d0a-556">685.14</span><span class="sxs-lookup"><span data-stu-id="90d0a-556">685.14</span></span></td>
<td><span data-ttu-id="90d0a-557">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-558">CC004</span><span class="sxs-lookup"><span data-stu-id="90d0a-558">CC004</span></span></td>
<td><span data-ttu-id="90d0a-559">Paketleme</span><span class="sxs-lookup"><span data-stu-id="90d0a-559">Packaging</span></span></td>
<td><span data-ttu-id="90d0a-560">10</span><span class="sxs-lookup"><span data-stu-id="90d0a-560">10</span></span></td>
<td><span data-ttu-id="90d0a-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="90d0a-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="90d0a-562">124.57</span><span class="sxs-lookup"><span data-stu-id="90d0a-562">124.57</span></span></td>
<td><span data-ttu-id="90d0a-563">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="90d0a-564">Aşağıdaki tablo, Finans hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="90d0a-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="90d0a-565">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="90d0a-565">Cost object</span></span></th>
<th><span data-ttu-id="90d0a-566">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="90d0a-566">Magnitude</span></span></th>
<th><span data-ttu-id="90d0a-567">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="90d0a-567">Allocation factor</span></span></th>
<th><span data-ttu-id="90d0a-568">Tutar</span><span class="sxs-lookup"><span data-stu-id="90d0a-568">Amount</span></span></th>
<th><span data-ttu-id="90d0a-569">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="90d0a-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="90d0a-570">CC003</span><span class="sxs-lookup"><span data-stu-id="90d0a-570">CC003</span></span></td>
<td><span data-ttu-id="90d0a-571">Montaj</span><span class="sxs-lookup"><span data-stu-id="90d0a-571">Assembly</span></span></td>
<td><span data-ttu-id="90d0a-572">65</span><span class="sxs-lookup"><span data-stu-id="90d0a-572">65</span></span></td>
<td><span data-ttu-id="90d0a-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="90d0a-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="90d0a-574">438.75</span><span class="sxs-lookup"><span data-stu-id="90d0a-574">438.75</span></span></td>
<td><span data-ttu-id="90d0a-575">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-576">CC004</span><span class="sxs-lookup"><span data-stu-id="90d0a-576">CC004</span></span></td>
<td><span data-ttu-id="90d0a-577">Paketleme</span><span class="sxs-lookup"><span data-stu-id="90d0a-577">Packaging</span></span></td>
<td><span data-ttu-id="90d0a-578">35</span><span class="sxs-lookup"><span data-stu-id="90d0a-578">35</span></span></td>
<td><span data-ttu-id="90d0a-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="90d0a-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="90d0a-580">236.25</span><span class="sxs-lookup"><span data-stu-id="90d0a-580">236.25</span></span></td>
<td><span data-ttu-id="90d0a-581">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-582">CC003</span><span class="sxs-lookup"><span data-stu-id="90d0a-582">CC003</span></span></td>
<td><span data-ttu-id="90d0a-583">Montaj</span><span class="sxs-lookup"><span data-stu-id="90d0a-583">Assembly</span></span></td>
<td><span data-ttu-id="90d0a-584">65</span><span class="sxs-lookup"><span data-stu-id="90d0a-584">65</span></span></td>
<td><span data-ttu-id="90d0a-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="90d0a-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="90d0a-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="90d0a-586">5,297.69</span></span></td>
<td><span data-ttu-id="90d0a-587">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-588">CC004</span><span class="sxs-lookup"><span data-stu-id="90d0a-588">CC004</span></span></td>
<td><span data-ttu-id="90d0a-589">Paketleme</span><span class="sxs-lookup"><span data-stu-id="90d0a-589">Packaging</span></span></td>
<td><span data-ttu-id="90d0a-590">35</span><span class="sxs-lookup"><span data-stu-id="90d0a-590">35</span></span></td>
<td><span data-ttu-id="90d0a-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="90d0a-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="90d0a-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="90d0a-592">2,852.60</span></span></td>
<td><span data-ttu-id="90d0a-593">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="90d0a-594">Aşağıdaki tablo, Derleme hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="90d0a-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="90d0a-595">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="90d0a-595">Cost object</span></span></th>
<th><span data-ttu-id="90d0a-596">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="90d0a-596">Magnitude</span></span></th>
<th><span data-ttu-id="90d0a-597">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="90d0a-597">Allocation factor</span></span></th>
<th><span data-ttu-id="90d0a-598">Tutar</span><span class="sxs-lookup"><span data-stu-id="90d0a-598">Amount</span></span></th>
<th><span data-ttu-id="90d0a-599">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="90d0a-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="90d0a-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-600">Prod 1</span></span></td>
<td><span data-ttu-id="90d0a-601">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-601">Product 1</span></span></td>
<td><span data-ttu-id="90d0a-602">60</span><span class="sxs-lookup"><span data-stu-id="90d0a-602">60</span></span></td>
<td><span data-ttu-id="90d0a-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="90d0a-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="90d0a-604">535.31</span><span class="sxs-lookup"><span data-stu-id="90d0a-604">535.31</span></span></td>
<td><span data-ttu-id="90d0a-605">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="90d0a-606">Prod 2</span></span></td>
<td><span data-ttu-id="90d0a-607">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="90d0a-607">Product 2</span></span></td>
<td><span data-ttu-id="90d0a-608">20</span><span class="sxs-lookup"><span data-stu-id="90d0a-608">20</span></span></td>
<td><span data-ttu-id="90d0a-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="90d0a-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="90d0a-610">178.44</span><span class="sxs-lookup"><span data-stu-id="90d0a-610">178.44</span></span></td>
<td><span data-ttu-id="90d0a-611">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-612">Prod 1</span></span></td>
<td><span data-ttu-id="90d0a-613">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-613">Product 1</span></span></td>
<td><span data-ttu-id="90d0a-614">60</span><span class="sxs-lookup"><span data-stu-id="90d0a-614">60</span></span></td>
<td><span data-ttu-id="90d0a-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="90d0a-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="90d0a-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="90d0a-616">4,487.12</span></span></td>
<td><span data-ttu-id="90d0a-617">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="90d0a-618">Prod 2</span></span></td>
<td><span data-ttu-id="90d0a-619">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="90d0a-619">Product 2</span></span></td>
<td><span data-ttu-id="90d0a-620">20</span><span class="sxs-lookup"><span data-stu-id="90d0a-620">20</span></span></td>
<td><span data-ttu-id="90d0a-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="90d0a-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="90d0a-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="90d0a-622">1,495.71</span></span></td>
<td><span data-ttu-id="90d0a-623">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="90d0a-624">Aşağıdaki tablo, Paketleme hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="90d0a-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="90d0a-625">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="90d0a-625">Cost object</span></span></th>
<th><span data-ttu-id="90d0a-626">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="90d0a-626">Magnitude</span></span></th>
<th><span data-ttu-id="90d0a-627">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="90d0a-627">Allocation factor</span></span></th>
<th><span data-ttu-id="90d0a-628">Tutar</span><span class="sxs-lookup"><span data-stu-id="90d0a-628">Amount</span></span></th>
<th><span data-ttu-id="90d0a-629">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="90d0a-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="90d0a-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-630">Prod 1</span></span></td>
<td><span data-ttu-id="90d0a-631">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-631">Product 1</span></span></td>
<td><span data-ttu-id="90d0a-632">80</span><span class="sxs-lookup"><span data-stu-id="90d0a-632">80</span></span></td>
<td><span data-ttu-id="90d0a-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="90d0a-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="90d0a-634">241.05</span><span class="sxs-lookup"><span data-stu-id="90d0a-634">241.05</span></span></td>
<td><span data-ttu-id="90d0a-635">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="90d0a-636">Prod 2</span></span></td>
<td><span data-ttu-id="90d0a-637">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="90d0a-637">Product 2</span></span></td>
<td><span data-ttu-id="90d0a-638">15</span><span class="sxs-lookup"><span data-stu-id="90d0a-638">15</span></span></td>
<td><span data-ttu-id="90d0a-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="90d0a-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="90d0a-640">45.20</span><span class="sxs-lookup"><span data-stu-id="90d0a-640">45.20</span></span></td>
<td><span data-ttu-id="90d0a-641">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-642">Prod 1</span></span></td>
<td><span data-ttu-id="90d0a-643">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-643">Product 1</span></span></td>
<td><span data-ttu-id="90d0a-644">80</span><span class="sxs-lookup"><span data-stu-id="90d0a-644">80</span></span></td>
<td><span data-ttu-id="90d0a-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="90d0a-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="90d0a-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="90d0a-646">2,507.09</span></span></td>
<td><span data-ttu-id="90d0a-647">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="90d0a-648">Prod 2</span></span></td>
<td><span data-ttu-id="90d0a-649">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="90d0a-649">Product 2</span></span></td>
<td><span data-ttu-id="90d0a-650">15</span><span class="sxs-lookup"><span data-stu-id="90d0a-650">15</span></span></td>
<td><span data-ttu-id="90d0a-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="90d0a-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="90d0a-652">470.08</span><span class="sxs-lookup"><span data-stu-id="90d0a-652">470.08</span></span></td>
<td><span data-ttu-id="90d0a-653">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="90d0a-654">Günlük girişleri (maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="90d0a-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="90d0a-655">Günlük</span><span class="sxs-lookup"><span data-stu-id="90d0a-655">Journal</span></span></th>
<th><span data-ttu-id="90d0a-656">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="90d0a-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="90d0a-657">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="90d0a-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="90d0a-658">Sürüm</span><span class="sxs-lookup"><span data-stu-id="90d0a-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="90d0a-659">00004</span><span class="sxs-lookup"><span data-stu-id="90d0a-659">00004</span></span></td>
<td><span data-ttu-id="90d0a-660">Maliyet tahsisatı günlüğü</span><span class="sxs-lookup"><span data-stu-id="90d0a-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="90d0a-661">Mali</span><span class="sxs-lookup"><span data-stu-id="90d0a-661">Fiscal</span></span></td>
<td><span data-ttu-id="90d0a-662">2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-662">2017</span></span></td>
<td><span data-ttu-id="90d0a-663">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-663">Period 1</span></span></td>
<td><span data-ttu-id="90d0a-664">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="90d0a-665">Günlük satırları</span><span class="sxs-lookup"><span data-stu-id="90d0a-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="90d0a-666">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="90d0a-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="90d0a-667">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="90d0a-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="90d0a-668">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="90d0a-668">Cost element</span></span></th>
<th><span data-ttu-id="90d0a-669">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="90d0a-669">Cost behavior</span></span></th>
<th><span data-ttu-id="90d0a-670">Tutar</span><span class="sxs-lookup"><span data-stu-id="90d0a-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="90d0a-671">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="90d0a-672">CC001</span><span class="sxs-lookup"><span data-stu-id="90d0a-672">CC001</span></span></td>
<td><span data-ttu-id="90d0a-673">İK</span><span class="sxs-lookup"><span data-stu-id="90d0a-673">HR</span></span></td>
<td><span data-ttu-id="90d0a-674">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-674">10001</span></span></td>
<td><span data-ttu-id="90d0a-675">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-675">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-676">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-676">Fixed cost</span></span></td>
<td><span data-ttu-id="90d0a-677">500.00</span><span class="sxs-lookup"><span data-stu-id="90d0a-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-678">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="90d0a-679">CC001</span><span class="sxs-lookup"><span data-stu-id="90d0a-679">CC001</span></span></td>
<td><span data-ttu-id="90d0a-680">İK</span><span class="sxs-lookup"><span data-stu-id="90d0a-680">HR</span></span></td>
<td><span data-ttu-id="90d0a-681">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-681">10001</span></span></td>
<td><span data-ttu-id="90d0a-682">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-682">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-683">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-683">Variable cost</span></span></td>
<td><span data-ttu-id="90d0a-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="90d0a-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-685">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="90d0a-686">CC002</span><span class="sxs-lookup"><span data-stu-id="90d0a-686">CC002</span></span></td>
<td><span data-ttu-id="90d0a-687">Finans</span><span class="sxs-lookup"><span data-stu-id="90d0a-687">Finance</span></span></td>
<td><span data-ttu-id="90d0a-688">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-688">10001</span></span></td>
<td><span data-ttu-id="90d0a-689">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-689">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-690">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-690">Fixed cost</span></span></td>
<td><span data-ttu-id="90d0a-691">675.00</span><span class="sxs-lookup"><span data-stu-id="90d0a-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-692">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="90d0a-693">CC002</span><span class="sxs-lookup"><span data-stu-id="90d0a-693">CC002</span></span></td>
<td><span data-ttu-id="90d0a-694">Finans</span><span class="sxs-lookup"><span data-stu-id="90d0a-694">Finance</span></span></td>
<td><span data-ttu-id="90d0a-695">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-695">10001</span></span></td>
<td><span data-ttu-id="90d0a-696">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-696">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-697">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-697">Variable cost</span></span></td>
<td><span data-ttu-id="90d0a-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="90d0a-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-699">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="90d0a-700">CC003</span><span class="sxs-lookup"><span data-stu-id="90d0a-700">CC003</span></span></td>
<td><span data-ttu-id="90d0a-701">Montaj</span><span class="sxs-lookup"><span data-stu-id="90d0a-701">Assembly</span></span></td>
<td><span data-ttu-id="90d0a-702">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-702">10001</span></span></td>
<td><span data-ttu-id="90d0a-703">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-703">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-704">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-704">Fixed cost</span></span></td>
<td><span data-ttu-id="90d0a-705">713.75</span><span class="sxs-lookup"><span data-stu-id="90d0a-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-706">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="90d0a-707">CC003</span><span class="sxs-lookup"><span data-stu-id="90d0a-707">CC003</span></span></td>
<td><span data-ttu-id="90d0a-708">Montaj</span><span class="sxs-lookup"><span data-stu-id="90d0a-708">Assembly</span></span></td>
<td><span data-ttu-id="90d0a-709">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-709">10001</span></span></td>
<td><span data-ttu-id="90d0a-710">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-710">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-711">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-711">Variable cost</span></span></td>
<td><span data-ttu-id="90d0a-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="90d0a-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-713">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="90d0a-714">CC003</span><span class="sxs-lookup"><span data-stu-id="90d0a-714">CC003</span></span></td>
<td><span data-ttu-id="90d0a-715">Paketleme</span><span class="sxs-lookup"><span data-stu-id="90d0a-715">Packaging</span></span></td>
<td><span data-ttu-id="90d0a-716">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-716">10001</span></span></td>
<td><span data-ttu-id="90d0a-717">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-717">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-718">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-718">Fixed cost</span></span></td>
<td><span data-ttu-id="90d0a-719">286.25</span><span class="sxs-lookup"><span data-stu-id="90d0a-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-720">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="90d0a-721">CC003</span><span class="sxs-lookup"><span data-stu-id="90d0a-721">CC003</span></span></td>
<td><span data-ttu-id="90d0a-722">Paketleme</span><span class="sxs-lookup"><span data-stu-id="90d0a-722">Packaging</span></span></td>
<td><span data-ttu-id="90d0a-723">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-723">10001</span></span></td>
<td><span data-ttu-id="90d0a-724">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-724">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-725">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-725">Variable cost</span></span></td>
<td><span data-ttu-id="90d0a-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="90d0a-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-727">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="90d0a-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-728">Prod 1</span></span></td>
<td><span data-ttu-id="90d0a-729">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-729">Product 1</span></span></td>
<td><span data-ttu-id="90d0a-730">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-730">10001</span></span></td>
<td><span data-ttu-id="90d0a-731">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-731">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-732">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-732">Fixed cost</span></span></td>
<td><span data-ttu-id="90d0a-733">776.36</span><span class="sxs-lookup"><span data-stu-id="90d0a-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-734">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="90d0a-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-735">Prod 1</span></span></td>
<td><span data-ttu-id="90d0a-736">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-736">Product 1</span></span></td>
<td><span data-ttu-id="90d0a-737">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-737">10001</span></span></td>
<td><span data-ttu-id="90d0a-738">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-738">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-739">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-739">Variable cost</span></span></td>
<td><span data-ttu-id="90d0a-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="90d0a-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-741">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="90d0a-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="90d0a-742">Prod 2</span></span></td>
<td><span data-ttu-id="90d0a-743">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-743">Product 1</span></span></td>
<td><span data-ttu-id="90d0a-744">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-744">10001</span></span></td>
<td><span data-ttu-id="90d0a-745">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-745">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-746">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-746">Fixed cost</span></span></td>
<td><span data-ttu-id="90d0a-747">223.64</span><span class="sxs-lookup"><span data-stu-id="90d0a-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-748">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="90d0a-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="90d0a-749">Prod 2</span></span></td>
<td><span data-ttu-id="90d0a-750">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-750">Product 1</span></span></td>
<td><span data-ttu-id="90d0a-751">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-751">10001</span></span></td>
<td><span data-ttu-id="90d0a-752">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-752">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-753">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-753">Variable cost</span></span></td>
<td><span data-ttu-id="90d0a-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="90d0a-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="90d0a-755">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="90d0a-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="90d0a-756">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="90d0a-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="90d0a-757">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="90d0a-757">Cost element</span></span></th>
<th><span data-ttu-id="90d0a-758">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="90d0a-758">Cost behavior</span></span></th>
<th><span data-ttu-id="90d0a-759">Tutar</span><span class="sxs-lookup"><span data-stu-id="90d0a-759">Amount</span></span></th>
<th><span data-ttu-id="90d0a-760">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="90d0a-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="90d0a-761">CC001</span><span class="sxs-lookup"><span data-stu-id="90d0a-761">CC001</span></span></td>
<td><span data-ttu-id="90d0a-762">İK</span><span class="sxs-lookup"><span data-stu-id="90d0a-762">HR</span></span></td>
<td><span data-ttu-id="90d0a-763">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-763">10001</span></span></td>
<td><span data-ttu-id="90d0a-764">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-764">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-765">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-765">Fixed cost</span></span></td>
<td><span data-ttu-id="90d0a-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="90d0a-766">-500.00</span></span></td>
<td><span data-ttu-id="90d0a-767">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-768">CC002</span><span class="sxs-lookup"><span data-stu-id="90d0a-768">CC002</span></span></td>
<td><span data-ttu-id="90d0a-769">Finans</span><span class="sxs-lookup"><span data-stu-id="90d0a-769">Finance</span></span></td>
<td><span data-ttu-id="90d0a-770">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-770">10001</span></span></td>
<td><span data-ttu-id="90d0a-771">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-771">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-772">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-772">Fixed cost</span></span></td>
<td><span data-ttu-id="90d0a-773">175.00</span><span class="sxs-lookup"><span data-stu-id="90d0a-773">175.00</span></span></td>
<td><span data-ttu-id="90d0a-774">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-775">CC003</span><span class="sxs-lookup"><span data-stu-id="90d0a-775">CC003</span></span></td>
<td><span data-ttu-id="90d0a-776">Montaj</span><span class="sxs-lookup"><span data-stu-id="90d0a-776">Assembly</span></span></td>
<td><span data-ttu-id="90d0a-777">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-777">10001</span></span></td>
<td><span data-ttu-id="90d0a-778">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-778">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-779">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-779">Fixed cost</span></span></td>
<td><span data-ttu-id="90d0a-780">275.00</span><span class="sxs-lookup"><span data-stu-id="90d0a-780">275.00</span></span></td>
<td><span data-ttu-id="90d0a-781">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-782">CC004</span><span class="sxs-lookup"><span data-stu-id="90d0a-782">CC004</span></span></td>
<td><span data-ttu-id="90d0a-783">Paketleme</span><span class="sxs-lookup"><span data-stu-id="90d0a-783">Packaging</span></span></td>
<td><span data-ttu-id="90d0a-784">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-784">10001</span></span></td>
<td><span data-ttu-id="90d0a-785">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-785">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-786">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-786">Fixed cost</span></span></td>
<td><span data-ttu-id="90d0a-787">50,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-787">50,00</span></span></td>
<td><span data-ttu-id="90d0a-788">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-789">CC001</span><span class="sxs-lookup"><span data-stu-id="90d0a-789">CC001</span></span></td>
<td><span data-ttu-id="90d0a-790">İK</span><span class="sxs-lookup"><span data-stu-id="90d0a-790">HR</span></span></td>
<td><span data-ttu-id="90d0a-791">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-791">10001</span></span></td>
<td><span data-ttu-id="90d0a-792">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-792">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-793">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-793">Variable cost</span></span></td>
<td><span data-ttu-id="90d0a-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="90d0a-794">-1,245.71</span></span></td>
<td><span data-ttu-id="90d0a-795">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-796">CC002</span><span class="sxs-lookup"><span data-stu-id="90d0a-796">CC002</span></span></td>
<td><span data-ttu-id="90d0a-797">Finans</span><span class="sxs-lookup"><span data-stu-id="90d0a-797">Finance</span></span></td>
<td><span data-ttu-id="90d0a-798">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-798">10001</span></span></td>
<td><span data-ttu-id="90d0a-799">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-799">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-800">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-800">Variable cost</span></span></td>
<td><span data-ttu-id="90d0a-801">436.00</span><span class="sxs-lookup"><span data-stu-id="90d0a-801">436.00</span></span></td>
<td><span data-ttu-id="90d0a-802">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-803">CC003</span><span class="sxs-lookup"><span data-stu-id="90d0a-803">CC003</span></span></td>
<td><span data-ttu-id="90d0a-804">Montaj</span><span class="sxs-lookup"><span data-stu-id="90d0a-804">Assembly</span></span></td>
<td><span data-ttu-id="90d0a-805">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-805">10001</span></span></td>
<td><span data-ttu-id="90d0a-806">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-806">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-807">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-807">Variable cost</span></span></td>
<td><span data-ttu-id="90d0a-808">685.14</span><span class="sxs-lookup"><span data-stu-id="90d0a-808">685.14</span></span></td>
<td><span data-ttu-id="90d0a-809">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-810">CC004</span><span class="sxs-lookup"><span data-stu-id="90d0a-810">CC004</span></span></td>
<td><span data-ttu-id="90d0a-811">Paketleme</span><span class="sxs-lookup"><span data-stu-id="90d0a-811">Packaging</span></span></td>
<td><span data-ttu-id="90d0a-812">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-812">10001</span></span></td>
<td><span data-ttu-id="90d0a-813">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-813">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-814">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-814">Variable cost</span></span></td>
<td><span data-ttu-id="90d0a-815">124.57</span><span class="sxs-lookup"><span data-stu-id="90d0a-815">124.57</span></span></td>
<td><span data-ttu-id="90d0a-816">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-817">CC002</span><span class="sxs-lookup"><span data-stu-id="90d0a-817">CC002</span></span></td>
<td><span data-ttu-id="90d0a-818">Finans</span><span class="sxs-lookup"><span data-stu-id="90d0a-818">Finance</span></span></td>
<td><span data-ttu-id="90d0a-819">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-819">10001</span></span></td>
<td><span data-ttu-id="90d0a-820">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-820">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-821">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-821">Fixed cost</span></span></td>
<td><span data-ttu-id="90d0a-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-822">-675.00</span></span></td>
<td><span data-ttu-id="90d0a-823">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-824">CC003</span><span class="sxs-lookup"><span data-stu-id="90d0a-824">CC003</span></span></td>
<td><span data-ttu-id="90d0a-825">Montaj</span><span class="sxs-lookup"><span data-stu-id="90d0a-825">Assembly</span></span></td>
<td><span data-ttu-id="90d0a-826">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-826">10001</span></span></td>
<td><span data-ttu-id="90d0a-827">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-827">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-828">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-828">Fixed cost</span></span></td>
<td><span data-ttu-id="90d0a-829">438.75</span><span class="sxs-lookup"><span data-stu-id="90d0a-829">438.75</span></span></td>
<td><span data-ttu-id="90d0a-830">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-831">CC004</span><span class="sxs-lookup"><span data-stu-id="90d0a-831">CC004</span></span></td>
<td><span data-ttu-id="90d0a-832">Paketleme</span><span class="sxs-lookup"><span data-stu-id="90d0a-832">Packaging</span></span></td>
<td><span data-ttu-id="90d0a-833">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-833">10001</span></span></td>
<td><span data-ttu-id="90d0a-834">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-834">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-835">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-835">Fixed cost</span></span></td>
<td><span data-ttu-id="90d0a-836">236.25</span><span class="sxs-lookup"><span data-stu-id="90d0a-836">236.25</span></span></td>
<td><span data-ttu-id="90d0a-837">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-838">CC002</span><span class="sxs-lookup"><span data-stu-id="90d0a-838">CC002</span></span></td>
<td><span data-ttu-id="90d0a-839">Finans</span><span class="sxs-lookup"><span data-stu-id="90d0a-839">Finance</span></span></td>
<td><span data-ttu-id="90d0a-840">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-840">10001</span></span></td>
<td><span data-ttu-id="90d0a-841">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-841">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-842">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-842">Variable cost</span></span></td>
<td><span data-ttu-id="90d0a-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="90d0a-843">-8,150.29</span></span></td>
<td><span data-ttu-id="90d0a-844">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-845">CC003</span><span class="sxs-lookup"><span data-stu-id="90d0a-845">CC003</span></span></td>
<td><span data-ttu-id="90d0a-846">Montaj</span><span class="sxs-lookup"><span data-stu-id="90d0a-846">Assembly</span></span></td>
<td><span data-ttu-id="90d0a-847">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-847">10001</span></span></td>
<td><span data-ttu-id="90d0a-848">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-848">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-849">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-849">Variable cost</span></span></td>
<td><span data-ttu-id="90d0a-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="90d0a-850">5,297.69</span></span></td>
<td><span data-ttu-id="90d0a-851">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-852">CC004</span><span class="sxs-lookup"><span data-stu-id="90d0a-852">CC004</span></span></td>
<td><span data-ttu-id="90d0a-853">Paketleme</span><span class="sxs-lookup"><span data-stu-id="90d0a-853">Packaging</span></span></td>
<td><span data-ttu-id="90d0a-854">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-854">10001</span></span></td>
<td><span data-ttu-id="90d0a-855">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-855">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-856">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-856">Variable cost</span></span></td>
<td><span data-ttu-id="90d0a-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="90d0a-857">2,852.60</span></span></td>
<td><span data-ttu-id="90d0a-858">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-859">CC003</span><span class="sxs-lookup"><span data-stu-id="90d0a-859">CC003</span></span></td>
<td><span data-ttu-id="90d0a-860">Montaj</span><span class="sxs-lookup"><span data-stu-id="90d0a-860">Assembly</span></span></td>
<td><span data-ttu-id="90d0a-861">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-861">10001</span></span></td>
<td><span data-ttu-id="90d0a-862">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-862">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-863">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-863">Fixed cost</span></span></td>
<td><span data-ttu-id="90d0a-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="90d0a-864">-713.75</span></span></td>
<td><span data-ttu-id="90d0a-865">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-866">Prod 1</span></span></td>
<td><span data-ttu-id="90d0a-867">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-867">Product 1</span></span></td>
<td><span data-ttu-id="90d0a-868">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-868">10001</span></span></td>
<td><span data-ttu-id="90d0a-869">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-869">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-870">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-870">Fixed cost</span></span></td>
<td><span data-ttu-id="90d0a-871">535.31</span><span class="sxs-lookup"><span data-stu-id="90d0a-871">535.31</span></span></td>
<td><span data-ttu-id="90d0a-872">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="90d0a-873">Prod 2</span></span></td>
<td><span data-ttu-id="90d0a-874">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="90d0a-874">Product 2</span></span></td>
<td><span data-ttu-id="90d0a-875">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-875">10001</span></span></td>
<td><span data-ttu-id="90d0a-876">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-876">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-877">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-877">Fixed cost</span></span></td>
<td><span data-ttu-id="90d0a-878">178.44</span><span class="sxs-lookup"><span data-stu-id="90d0a-878">178.44</span></span></td>
<td><span data-ttu-id="90d0a-879">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-880">CC003</span><span class="sxs-lookup"><span data-stu-id="90d0a-880">CC003</span></span></td>
<td><span data-ttu-id="90d0a-881">Montaj</span><span class="sxs-lookup"><span data-stu-id="90d0a-881">Assembly</span></span></td>
<td><span data-ttu-id="90d0a-882">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-882">10001</span></span></td>
<td><span data-ttu-id="90d0a-883">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-883">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-884">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-884">Variable cost</span></span></td>
<td><span data-ttu-id="90d0a-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="90d0a-885">-5,982.83</span></span></td>
<td><span data-ttu-id="90d0a-886">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-887">Prod 1</span></span></td>
<td><span data-ttu-id="90d0a-888">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-888">Product 1</span></span></td>
<td><span data-ttu-id="90d0a-889">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-889">10001</span></span></td>
<td><span data-ttu-id="90d0a-890">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-890">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-891">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-891">Variable cost</span></span></td>
<td><span data-ttu-id="90d0a-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="90d0a-892">4,487.12</span></span></td>
<td><span data-ttu-id="90d0a-893">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="90d0a-894">Prod 2</span></span></td>
<td><span data-ttu-id="90d0a-895">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="90d0a-895">Product 2</span></span></td>
<td><span data-ttu-id="90d0a-896">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-896">10001</span></span></td>
<td><span data-ttu-id="90d0a-897">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-897">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-898">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-898">Variable cost</span></span></td>
<td><span data-ttu-id="90d0a-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="90d0a-899">1,495.71</span></span></td>
<td><span data-ttu-id="90d0a-900">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-901">CC003</span><span class="sxs-lookup"><span data-stu-id="90d0a-901">CC003</span></span></td>
<td><span data-ttu-id="90d0a-902">Montaj</span><span class="sxs-lookup"><span data-stu-id="90d0a-902">Assembly</span></span></td>
<td><span data-ttu-id="90d0a-903">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-903">10001</span></span></td>
<td><span data-ttu-id="90d0a-904">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-904">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-905">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-905">Fixed cost</span></span></td>
<td><span data-ttu-id="90d0a-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="90d0a-906">-286.25</span></span></td>
<td><span data-ttu-id="90d0a-907">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-908">Prod 1</span></span></td>
<td><span data-ttu-id="90d0a-909">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-909">Product 1</span></span></td>
<td><span data-ttu-id="90d0a-910">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-910">10001</span></span></td>
<td><span data-ttu-id="90d0a-911">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-911">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-912">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-912">Fixed cost</span></span></td>
<td><span data-ttu-id="90d0a-913">241.05</span><span class="sxs-lookup"><span data-stu-id="90d0a-913">241.05</span></span></td>
<td><span data-ttu-id="90d0a-914">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="90d0a-915">Prod 2</span></span></td>
<td><span data-ttu-id="90d0a-916">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="90d0a-916">Product 2</span></span></td>
<td><span data-ttu-id="90d0a-917">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-917">10001</span></span></td>
<td><span data-ttu-id="90d0a-918">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-918">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-919">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-919">Fixed cost</span></span></td>
<td><span data-ttu-id="90d0a-920">45.20</span><span class="sxs-lookup"><span data-stu-id="90d0a-920">45.20</span></span></td>
<td><span data-ttu-id="90d0a-921">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-922">CC003</span><span class="sxs-lookup"><span data-stu-id="90d0a-922">CC003</span></span></td>
<td><span data-ttu-id="90d0a-923">Montaj</span><span class="sxs-lookup"><span data-stu-id="90d0a-923">Assembly</span></span></td>
<td><span data-ttu-id="90d0a-924">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-924">10001</span></span></td>
<td><span data-ttu-id="90d0a-925">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-925">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-926">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-926">Variable cost</span></span></td>
<td><span data-ttu-id="90d0a-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="90d0a-927">-2,977.17</span></span></td>
<td><span data-ttu-id="90d0a-928">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-929">Prod 1</span></span></td>
<td><span data-ttu-id="90d0a-930">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-930">Product 1</span></span></td>
<td><span data-ttu-id="90d0a-931">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-931">10001</span></span></td>
<td><span data-ttu-id="90d0a-932">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-932">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-933">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-933">Variable cost</span></span></td>
<td><span data-ttu-id="90d0a-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="90d0a-934">2,507.09</span></span></td>
<td><span data-ttu-id="90d0a-935">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="90d0a-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="90d0a-936">Prod 2</span></span></td>
<td><span data-ttu-id="90d0a-937">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="90d0a-937">Product 2</span></span></td>
<td><span data-ttu-id="90d0a-938">10001</span><span class="sxs-lookup"><span data-stu-id="90d0a-938">10001</span></span></td>
<td><span data-ttu-id="90d0a-939">Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-939">Electricity</span></span></td>
<td><span data-ttu-id="90d0a-940">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-940">Variable cost</span></span></td>
<td><span data-ttu-id="90d0a-941">470.08</span><span class="sxs-lookup"><span data-stu-id="90d0a-941">470.08</span></span></td>
<td><span data-ttu-id="90d0a-942">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="90d0a-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="90d0a-943">Sonuç</span><span class="sxs-lookup"><span data-stu-id="90d0a-943">Conclusion</span></span>
<span data-ttu-id="90d0a-944">Mali muhasebede, Elektrik için 10.000,00 maliyet bir sözde maliyet merkezi kimliğine nakledilmiştir.</span><span class="sxs-lookup"><span data-stu-id="90d0a-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="90d0a-945">Bu nedenle, maliyet muhasebecileri bu maliyetin tahsis edilmesi gerektiğini bilirler.</span><span class="sxs-lookup"><span data-stu-id="90d0a-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="90d0a-946">Maliyet muhasebesinde, maliyetler kuruluş birimleri ve seviyeleri arasında, uygulanan kural ve ilkelere dayalı olarak akar.</span><span class="sxs-lookup"><span data-stu-id="90d0a-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="90d0a-947">Her maliyet, maliyetlerin tahsisatı için en iyi değerlendirmeyi sağlayan bir tahsisat tabanı ile ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="90d0a-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="90d0a-948">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="90d0a-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="90d0a-949">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="90d0a-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="90d0a-950">Toplam</span><span class="sxs-lookup"><span data-stu-id="90d0a-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="90d0a-951">CC099</span><span class="sxs-lookup"><span data-stu-id="90d0a-951">CC099</span></span></th>
<th><span data-ttu-id="90d0a-952">CC001</span><span class="sxs-lookup"><span data-stu-id="90d0a-952">CC001</span></span></th>
<th><span data-ttu-id="90d0a-953">CC002</span><span class="sxs-lookup"><span data-stu-id="90d0a-953">CC002</span></span></th>
<th><span data-ttu-id="90d0a-954">CC003</span><span class="sxs-lookup"><span data-stu-id="90d0a-954">CC003</span></span></th>
<th><span data-ttu-id="90d0a-955">CC004</span><span class="sxs-lookup"><span data-stu-id="90d0a-955">CC004</span></span></th>
<th><span data-ttu-id="90d0a-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-956">Proj 1</span></span></th>
<th><span data-ttu-id="90d0a-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="90d0a-957">Proj 2</span></span></th>
<th><span data-ttu-id="90d0a-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="90d0a-958">Prod 1</span></span></th>
<th><span data-ttu-id="90d0a-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="90d0a-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="90d0a-960">10001 Elektrik</span><span class="sxs-lookup"><span data-stu-id="90d0a-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="90d0a-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="90d0a-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="90d0a-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="90d0a-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="90d0a-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="90d0a-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="90d0a-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="90d0a-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="90d0a-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="90d0a-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="90d0a-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="90d0a-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="90d0a-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="90d0a-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="90d0a-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="90d0a-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="90d0a-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="90d0a-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="90d0a-970">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="90d0a-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="90d0a-971">0,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="90d0a-972">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="90d0a-973">0,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="90d0a-974">0,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="90d0a-975">0,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="90d0a-976">0,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="90d0a-977">0,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="90d0a-978">776.36</span><span class="sxs-lookup"><span data-stu-id="90d0a-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="90d0a-979">223.64</span><span class="sxs-lookup"><span data-stu-id="90d0a-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="90d0a-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="90d0a-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="90d0a-981">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="90d0a-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="90d0a-982">000</span><span class="sxs-lookup"><span data-stu-id="90d0a-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="90d0a-983">0,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="90d0a-984">0,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="90d0a-985">0,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="90d0a-986">0,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="90d0a-987">30.00</span><span class="sxs-lookup"><span data-stu-id="90d0a-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="90d0a-988">10,00</span><span class="sxs-lookup"><span data-stu-id="90d0a-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="90d0a-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="90d0a-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="90d0a-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="90d0a-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="90d0a-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="90d0a-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="90d0a-992">Bu konu, birincil maliyet öğesi, 10001 Elektrik'in maliyet nesneleri arasında nasıl aktığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="90d0a-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="90d0a-993">Bu nedenle, bu genel gider maliyeti kuruluşun en düşük seviyesine tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="90d0a-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="90d0a-994">Başka bir deyişle, maliyet en alt düzeydeki maliyet nesnelerine aittir.</span><span class="sxs-lookup"><span data-stu-id="90d0a-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="90d0a-995">Maliyetin, maliyet nesneleri arasında görsel bir akışına ihtiyacınız varsa, maliyetin akışını görselleştirmek için maliyet toplamı ilke kurallarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="90d0a-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="90d0a-996">Daha fazla bilgi için bkz. [Maliyet yuvarlama ilkesi ve genel gider hesaplaması](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="90d0a-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



