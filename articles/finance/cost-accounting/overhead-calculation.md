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
ms.openlocfilehash: 882804141a6b520e2420343958c7a6b02a7e09ae
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208859"
---
# <a name="overhead-calculation"></a><span data-ttu-id="b59d1-103">Genel gider hesaplaması</span><span class="sxs-lookup"><span data-stu-id="b59d1-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b59d1-104">Bu konu, genel gider maliyetlerinin hesaplanması için tipik işlemleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="b59d1-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="b59d1-105">Terim tanımı</span><span class="sxs-lookup"><span data-stu-id="b59d1-105">Term definition</span></span>
---------------

<span data-ttu-id="b59d1-106">Genel gider maliyetleri bir işletmenin çalışması için normalde uygulanan, ancak doğrudan herhangi bir özel iş, faaliyet, ürün veya hizmete ilişkilendirilmemiş olan maliyetlerdir.</span><span class="sxs-lookup"><span data-stu-id="b59d1-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="b59d1-107">Genel gider maliyetleri kar sağlama faaliyetlerinin oluşturulması için kritik destek sağlar.</span><span class="sxs-lookup"><span data-stu-id="b59d1-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="b59d1-108">Aşağıda bazı genel gider örnekleri verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="b59d1-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="b59d1-109">Kira</span><span class="sxs-lookup"><span data-stu-id="b59d1-109">Rent</span></span>
-   <span data-ttu-id="b59d1-110">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-110">Electricity</span></span>
-   <span data-ttu-id="b59d1-111">Yönetim maaşları</span><span class="sxs-lookup"><span data-stu-id="b59d1-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="b59d1-112">Genel gider hesaplaması genel bakış</span><span class="sxs-lookup"><span data-stu-id="b59d1-112">Overhead calculation overview</span></span>
<span data-ttu-id="b59d1-113">Genel gider hesaplama, maliyet muhasebesi ilkelerini doğru sırayla çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="b59d1-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="b59d1-114">Maliyet muhasebesi ilkeleri değiştiyse veya belirli hatalar algılandıysa, genel gider hesaplamasını aynı mali dönem için birden fazla kez yürütebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b59d1-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="b59d1-115">Her genel gider hesaplaması depolanır ve önceki sürümlerdeki hesaplamaları kıyaslamanıza olanak sağlayan, benzersiz bir sürüm kimliğine sahip olur.</span><span class="sxs-lookup"><span data-stu-id="b59d1-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="b59d1-116">Genel gider hesaplamasının oluşturduğu maliyet girişleri bir muhasebe tarihi alır.</span><span class="sxs-lookup"><span data-stu-id="b59d1-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="b59d1-117">Bu muhasebe tarihi, hesaplamada kullanılan mali dönemin bitiş tarihiyle eşleşir.</span><span class="sxs-lookup"><span data-stu-id="b59d1-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="b59d1-118">Benzersiz sürüm kimliği aşağıdaki öğelerden oluşur:</span><span class="sxs-lookup"><span data-stu-id="b59d1-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="b59d1-119">Sürüm türü</span><span class="sxs-lookup"><span data-stu-id="b59d1-119">Version type</span></span>
-   <span data-ttu-id="b59d1-120">Tarih ve saat</span><span class="sxs-lookup"><span data-stu-id="b59d1-120">Date and time</span></span>
-   <span data-ttu-id="b59d1-121">Maliyet muhasebesi defteri</span><span class="sxs-lookup"><span data-stu-id="b59d1-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="b59d1-122">Mali yıl</span><span class="sxs-lookup"><span data-stu-id="b59d1-122">Fiscal year</span></span>
-   <span data-ttu-id="b59d1-123">Mali dönem</span><span class="sxs-lookup"><span data-stu-id="b59d1-123">Fiscal period</span></span>

<span data-ttu-id="b59d1-124">Genel gider hesaplama, sürümden bağımsız olarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="b59d1-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="b59d1-125">Bu nedenle, Gerçek sürümden önce Bütçe sürümünü hesaplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b59d1-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="b59d1-126">Genel gider hesaplama dört adımdan oluşur, aşağıdaki çizimde gösterildiği gibi.</span><span class="sxs-lookup"><span data-stu-id="b59d1-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="b59d1-127">Her adımda, günlük girişleri olan bir günlük başlığı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b59d1-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="b59d1-128">Bu günlük başlığı, her hesaplama adımı için giriş verilerini tutar.</span><span class="sxs-lookup"><span data-stu-id="b59d1-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="b59d1-129">İlkeler ve kurallar her günlük satırına uygulanır ve maliyet girişleri çıkış olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b59d1-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="b59d1-130">Bu nedenle, her zaman tam izlenebilirliğe sahip olursunuz.</span><span class="sxs-lookup"><span data-stu-id="b59d1-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="b59d1-131">[![Genel gider hesaplaması](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="b59d1-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="b59d1-132">Elektrik genel gideri maliyetini hesapla ve tahsis et</span><span class="sxs-lookup"><span data-stu-id="b59d1-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="b59d1-133">Mali muhasebede, elektrik gibi bazı maliyetler peşin ödeme olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="b59d1-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="b59d1-134">Bu nedenle, Maliyet muhasebesi için ayrıntılı yönetim bilgiler sağlanmaz.</span><span class="sxs-lookup"><span data-stu-id="b59d1-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="b59d1-135">Maliyet muhasebesinde doğru yönetimsel bilgileri tüm yönetim birim ve düzeylerinde sağlamak için, maliyetlerin kuruluş birimleri arasında akması gerekir.</span><span class="sxs-lookup"><span data-stu-id="b59d1-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="b59d1-136">Bu akış, tüketimin doğru bir kaydına ya da adil bir değerlendirmeye dayanıyor olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b59d1-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="b59d1-137">Genel muhasebede, bir elektrik maliyeti aşağıdaki tabloda gösterildiği gibi deftere nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="b59d1-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b59d1-138">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="b59d1-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b59d1-139">Maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="b59d1-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="b59d1-140">Ana hesap</span><span class="sxs-lookup"><span data-stu-id="b59d1-140">Main account</span></span></th>
<th><span data-ttu-id="b59d1-141">Muhasebe para birimi cinsinden tutar</span><span class="sxs-lookup"><span data-stu-id="b59d1-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b59d1-142">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="b59d1-143">CC099</span><span class="sxs-lookup"><span data-stu-id="b59d1-143">CC099</span></span></td>
<td><span data-ttu-id="b59d1-144">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="b59d1-144">Default cost center</span></span></td>
<td><span data-ttu-id="b59d1-145">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-145">10001</span></span></td>
<td><span data-ttu-id="b59d1-146">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-146">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="b59d1-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="b59d1-148">Adım 1: Maliyet davranışı hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="b59d1-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="b59d1-149">Varsayılan olarak, maliyeti girişleri kaynak veriden içeri alındığında, Maliyet muhasebesinde **Sınıflandırılmamış** maliyet davranışı sınıflandırmasını alırlar.</span><span class="sxs-lookup"><span data-stu-id="b59d1-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="b59d1-150">Maliyet davranışı ilke kuralları ekleyerek, maliyet girişlerini **Sabit maliyet** veya **Değişken maliyet** olarak yeniden sınıflandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b59d1-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="b59d1-151">Maliyet davranış kuralını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="b59d1-151">Define the cost behavior rule</span></span>

<span data-ttu-id="b59d1-152">Bazı durumlarda, sabit bir ücret maliyet parçasıdır ve kalan maliyet, tüketime dayanır.</span><span class="sxs-lookup"><span data-stu-id="b59d1-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="b59d1-153">Elektrik faturaları genellikle bu tanıma uyar.</span><span class="sxs-lookup"><span data-stu-id="b59d1-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="b59d1-154">Belirli bir sabit ücret ödedikten sonra, kilovat saatlik (Kwh) tüketim başına ödeme yaparsınız.</span><span class="sxs-lookup"><span data-stu-id="b59d1-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="b59d1-155">Örneğin, sabit maliyet masrafı 1.000,00 ise, maliyet davranışı kural nasıl tanımlanır:</span><span class="sxs-lookup"><span data-stu-id="b59d1-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="b59d1-156">Sabit tutar 1.000,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="b59d1-157">0 &lt;= 1.000,00 = Sabit</span><span class="sxs-lookup"><span data-stu-id="b59d1-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="b59d1-158">1000,01 &lt; N = Değişken</span><span class="sxs-lookup"><span data-stu-id="b59d1-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="b59d1-159">Günlük</span><span class="sxs-lookup"><span data-stu-id="b59d1-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b59d1-160">Günlük</span><span class="sxs-lookup"><span data-stu-id="b59d1-160">Journal</span></span></th>
<th><span data-ttu-id="b59d1-161">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="b59d1-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="b59d1-162">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="b59d1-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="b59d1-163">Sürüm</span><span class="sxs-lookup"><span data-stu-id="b59d1-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b59d1-164">00001</span><span class="sxs-lookup"><span data-stu-id="b59d1-164">00001</span></span></td>
<td><span data-ttu-id="b59d1-165">Maliyet davranışı hesaplama günlüğü</span><span class="sxs-lookup"><span data-stu-id="b59d1-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="b59d1-166">Mali</span><span class="sxs-lookup"><span data-stu-id="b59d1-166">Fiscal</span></span></td>
<td><span data-ttu-id="b59d1-167">2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-167">2017</span></span></td>
<td><span data-ttu-id="b59d1-168">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-168">Period 1</span></span></td>
<td><span data-ttu-id="b59d1-169">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="b59d1-170">Günlük girişleri (Maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="b59d1-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b59d1-171">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="b59d1-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b59d1-172">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="b59d1-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b59d1-173">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="b59d1-173">Cost element</span></span></th>
<th><span data-ttu-id="b59d1-174">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="b59d1-174">Cost behavior</span></span></th>
<th><span data-ttu-id="b59d1-175">Tutar</span><span class="sxs-lookup"><span data-stu-id="b59d1-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b59d1-176">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="b59d1-177">CC099</span><span class="sxs-lookup"><span data-stu-id="b59d1-177">CC099</span></span></td>
<td><span data-ttu-id="b59d1-178">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="b59d1-178">Default cost center</span></span></td>
<td><span data-ttu-id="b59d1-179">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-179">10001</span></span></td>
<td><span data-ttu-id="b59d1-180">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-180">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-181">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="b59d1-181">Unclassified</span></span></td>
<td><span data-ttu-id="b59d1-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="b59d1-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="b59d1-183">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="b59d1-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b59d1-184">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="b59d1-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b59d1-185">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="b59d1-185">Cost element</span></span></th>
<th><span data-ttu-id="b59d1-186">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="b59d1-186">Cost behavior</span></span></th>
<th><span data-ttu-id="b59d1-187">Tutar</span><span class="sxs-lookup"><span data-stu-id="b59d1-187">Amount</span></span></th>
<th><span data-ttu-id="b59d1-188">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="b59d1-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b59d1-189">CC099</span><span class="sxs-lookup"><span data-stu-id="b59d1-189">CC099</span></span></td>
<td><span data-ttu-id="b59d1-190">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="b59d1-190">Default cost center</span></span></td>
<td><span data-ttu-id="b59d1-191">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-191">10001</span></span></td>
<td><span data-ttu-id="b59d1-192">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-192">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-193">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="b59d1-193">Unclassified</span></span></td>
<td><span data-ttu-id="b59d1-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="b59d1-194">10,000.00</span></span></td>
<td><span data-ttu-id="b59d1-195">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-196">CC099</span><span class="sxs-lookup"><span data-stu-id="b59d1-196">CC099</span></span></td>
<td><span data-ttu-id="b59d1-197">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="b59d1-197">Default cost center</span></span></td>
<td><span data-ttu-id="b59d1-198">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-198">10001</span></span></td>
<td><span data-ttu-id="b59d1-199">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-199">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-200">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="b59d1-200">Unclassified</span></span></td>
<td><span data-ttu-id="b59d1-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-201">-10,000.00</span></span></td>
<td><span data-ttu-id="b59d1-202">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-203">CC099</span><span class="sxs-lookup"><span data-stu-id="b59d1-203">CC099</span></span></td>
<td><span data-ttu-id="b59d1-204">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="b59d1-204">Default cost center</span></span></td>
<td><span data-ttu-id="b59d1-205">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-205">10001</span></span></td>
<td><span data-ttu-id="b59d1-206">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-206">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-207">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-207">Fixed cost</span></span></td>
<td><span data-ttu-id="b59d1-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-208">1,000.00</span></span></td>
<td><span data-ttu-id="b59d1-209">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-210">CC099</span><span class="sxs-lookup"><span data-stu-id="b59d1-210">CC099</span></span></td>
<td><span data-ttu-id="b59d1-211">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="b59d1-211">Default cost center</span></span></td>
<td><span data-ttu-id="b59d1-212">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-212">10001</span></span></td>
<td><span data-ttu-id="b59d1-213">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-213">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-214">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-214">Variable cost</span></span></td>
<td><span data-ttu-id="b59d1-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="b59d1-215">9,000.00</span></span></td>
<td><span data-ttu-id="b59d1-216">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b59d1-217">Daha fazla bilgi için bkz. [Maliyet davranışı ilkesi oluşturma ve bir maliyet kontrol birimine atama](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="b59d1-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="b59d1-218">Adım 2: Maliyet dağıtımı hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="b59d1-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="b59d1-219">Maliyet dağıtımı, bir nesneden bir veya daha fazlasına ilgili tahsisat tabanı uygulayarak maliyeti yeniden dağıtmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b59d1-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="b59d1-220">Maliyet dağıtımı ve maliyet tahsisatı, maliyet dağıtımının her zaman orijinal maliyetin birincil maliyet öğesinde bulunmasıyla farklılık gösterir.</span><span class="sxs-lookup"><span data-stu-id="b59d1-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="b59d1-221">Maliyet dağıtım kuralını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="b59d1-221">Define the cost distribution rule</span></span>

<span data-ttu-id="b59d1-222">Mali muhasebede, elektrik maliyetleri çoğu zaman peşin ödeme olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="b59d1-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="b59d1-223">Maliyet muhasebesinde ise bu yöntem yeterince ayrıntılı değildir.</span><span class="sxs-lookup"><span data-stu-id="b59d1-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="b59d1-224">Değişken maliyet, maliyet nesnelerine tek tek, adil bir temele dayanarak dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b59d1-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="b59d1-225">En mantıklı tahsisat, elektrik kullanımını (Kwh) temel alarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b59d1-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="b59d1-226">Elektrik adına sahip, istatistiksel bir boyut üyesi oluşturulur ve elektrik tüketimi kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="b59d1-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="b59d1-227">Varsayıla olarak, tüm istatistiksel boyut üyeleri tahsisat tabanları olarak kullanılabilir hale gelir.</span><span class="sxs-lookup"><span data-stu-id="b59d1-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b59d1-228">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="b59d1-228">Cost object</span></span></th>
<th><span data-ttu-id="b59d1-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="b59d1-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b59d1-230">CC001</span><span class="sxs-lookup"><span data-stu-id="b59d1-230">CC001</span></span></td>
<td><span data-ttu-id="b59d1-231">İK</span><span class="sxs-lookup"><span data-stu-id="b59d1-231">HR</span></span></td>
<td><span data-ttu-id="b59d1-232">1.000</span><span class="sxs-lookup"><span data-stu-id="b59d1-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-233">CC002</span><span class="sxs-lookup"><span data-stu-id="b59d1-233">CC002</span></span></td>
<td><span data-ttu-id="b59d1-234">Finans</span><span class="sxs-lookup"><span data-stu-id="b59d1-234">Finance</span></span></td>
<td><span data-ttu-id="b59d1-235">6,000</span><span class="sxs-lookup"><span data-stu-id="b59d1-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-236">CC003</span><span class="sxs-lookup"><span data-stu-id="b59d1-236">CC003</span></span></td>
<td><span data-ttu-id="b59d1-237">Montaj</span><span class="sxs-lookup"><span data-stu-id="b59d1-237">Assembly</span></span></td>
<td><span data-ttu-id="b59d1-238">0</span><span class="sxs-lookup"><span data-stu-id="b59d1-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b59d1-239">Aşağıdaki tablo, elektrik tüketiminin değişken maliyetler için bir tahsisat tabanlı olarak uygulandığındaki sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="b59d1-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b59d1-240">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="b59d1-240">Cost object</span></span></th>
<th><span data-ttu-id="b59d1-241">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="b59d1-241">Magnitude</span></span></th>
<th><span data-ttu-id="b59d1-242">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="b59d1-242">Allocation factor</span></span></th>
<th><span data-ttu-id="b59d1-243">Tutar</span><span class="sxs-lookup"><span data-stu-id="b59d1-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b59d1-244">CC001</span><span class="sxs-lookup"><span data-stu-id="b59d1-244">CC001</span></span></td>
<td><span data-ttu-id="b59d1-245">İK</span><span class="sxs-lookup"><span data-stu-id="b59d1-245">HR</span></span></td>
<td><span data-ttu-id="b59d1-246">1.000</span><span class="sxs-lookup"><span data-stu-id="b59d1-246">1,000</span></span></td>
<td><span data-ttu-id="b59d1-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="b59d1-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="b59d1-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-249">CC002</span><span class="sxs-lookup"><span data-stu-id="b59d1-249">CC002</span></span></td>
<td><span data-ttu-id="b59d1-250">Finans</span><span class="sxs-lookup"><span data-stu-id="b59d1-250">Finance</span></span></td>
<td><span data-ttu-id="b59d1-251">6,000</span><span class="sxs-lookup"><span data-stu-id="b59d1-251">6,000</span></span></td>
<td><span data-ttu-id="b59d1-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="b59d1-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="b59d1-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-254">CC003</span><span class="sxs-lookup"><span data-stu-id="b59d1-254">CC003</span></span></td>
<td><span data-ttu-id="b59d1-255">Montaj</span><span class="sxs-lookup"><span data-stu-id="b59d1-255">Assembly</span></span></td>
<td><span data-ttu-id="b59d1-256">0</span><span class="sxs-lookup"><span data-stu-id="b59d1-256">0</span></span></td>
<td><span data-ttu-id="b59d1-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="b59d1-258">0,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b59d1-259">Sabit maliyet, elektrik tüketmiş olan tekil maliyet nesnelerine eşit miktarda dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b59d1-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="b59d1-260">Bu sonuca, Elektrik istatistiksel boyut öğesini bir formül tahsisat tabanında kullanarak ulaşabilirsiniz: (Elektrik &gt; 0,00) Aşağıdaki tablo, elektrik tüketimi değişken maliyetler için bir tahsisat tabanı olarak kullanıldığında ortaya çıkan sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="b59d1-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b59d1-261">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="b59d1-261">Cost object</span></span></th>
<th><span data-ttu-id="b59d1-262">Formül</span><span class="sxs-lookup"><span data-stu-id="b59d1-262">Formula</span></span></th>
<th><span data-ttu-id="b59d1-263">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="b59d1-263">Magnitude</span></span></th>
<th><span data-ttu-id="b59d1-264">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="b59d1-264">Allocation factor</span></span></th>
<th><span data-ttu-id="b59d1-265">Tutar</span><span class="sxs-lookup"><span data-stu-id="b59d1-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b59d1-266">CC001</span><span class="sxs-lookup"><span data-stu-id="b59d1-266">CC001</span></span></td>
<td><span data-ttu-id="b59d1-267">İK</span><span class="sxs-lookup"><span data-stu-id="b59d1-267">HR</span></span></td>
<td><span data-ttu-id="b59d1-268">(1,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="b59d1-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="b59d1-269">1</span><span class="sxs-lookup"><span data-stu-id="b59d1-269">1</span></span></td>
<td><span data-ttu-id="b59d1-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="b59d1-271">500.00</span><span class="sxs-lookup"><span data-stu-id="b59d1-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-272">CC002</span><span class="sxs-lookup"><span data-stu-id="b59d1-272">CC002</span></span></td>
<td><span data-ttu-id="b59d1-273">Finans</span><span class="sxs-lookup"><span data-stu-id="b59d1-273">Finance</span></span></td>
<td><span data-ttu-id="b59d1-274">(6,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="b59d1-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="b59d1-275">1</span><span class="sxs-lookup"><span data-stu-id="b59d1-275">1</span></span></td>
<td><span data-ttu-id="b59d1-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="b59d1-277">500.00</span><span class="sxs-lookup"><span data-stu-id="b59d1-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-278">CC003</span><span class="sxs-lookup"><span data-stu-id="b59d1-278">CC003</span></span></td>
<td><span data-ttu-id="b59d1-279">Montaj</span><span class="sxs-lookup"><span data-stu-id="b59d1-279">Assembly</span></span></td>
<td><span data-ttu-id="b59d1-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="b59d1-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="b59d1-281">0</span><span class="sxs-lookup"><span data-stu-id="b59d1-281">0</span></span></td>
<td><span data-ttu-id="b59d1-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="b59d1-283">0,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="b59d1-284">Günlük</span><span class="sxs-lookup"><span data-stu-id="b59d1-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b59d1-285">Günlük</span><span class="sxs-lookup"><span data-stu-id="b59d1-285">Journal</span></span></th>
<th><span data-ttu-id="b59d1-286">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="b59d1-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="b59d1-287">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="b59d1-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="b59d1-288">Sürüm</span><span class="sxs-lookup"><span data-stu-id="b59d1-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b59d1-289">00002</span><span class="sxs-lookup"><span data-stu-id="b59d1-289">00002</span></span></td>
<td><span data-ttu-id="b59d1-290">Maliyet dağıtımı hesaplama günlüğü</span><span class="sxs-lookup"><span data-stu-id="b59d1-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="b59d1-291">Mali</span><span class="sxs-lookup"><span data-stu-id="b59d1-291">Fiscal</span></span></td>
<td><span data-ttu-id="b59d1-292">2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-292">2017</span></span></td>
<td><span data-ttu-id="b59d1-293">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-293">Period 1</span></span></td>
<td><span data-ttu-id="b59d1-294">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="b59d1-295">Günlük girişleri (Maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="b59d1-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b59d1-296">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="b59d1-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b59d1-297">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="b59d1-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b59d1-298">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="b59d1-298">Cost element</span></span></th>
<th><span data-ttu-id="b59d1-299">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="b59d1-299">Cost behavior</span></span></th>
<th><span data-ttu-id="b59d1-300">Tutar</span><span class="sxs-lookup"><span data-stu-id="b59d1-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b59d1-301">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="b59d1-302">CC099</span><span class="sxs-lookup"><span data-stu-id="b59d1-302">CC099</span></span></td>
<td><span data-ttu-id="b59d1-303">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="b59d1-303">Default cost center</span></span></td>
<td><span data-ttu-id="b59d1-304">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-304">10001</span></span></td>
<td><span data-ttu-id="b59d1-305">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-305">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-306">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-306">Fixed cost</span></span></td>
<td><span data-ttu-id="b59d1-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-308">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="b59d1-309">CC099</span><span class="sxs-lookup"><span data-stu-id="b59d1-309">CC099</span></span></td>
<td><span data-ttu-id="b59d1-310">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="b59d1-310">Default cost center</span></span></td>
<td><span data-ttu-id="b59d1-311">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-311">10001</span></span></td>
<td><span data-ttu-id="b59d1-312">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-312">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-313">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-313">Variable cost</span></span></td>
<td><span data-ttu-id="b59d1-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="b59d1-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="b59d1-315">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="b59d1-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b59d1-316">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="b59d1-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b59d1-317">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="b59d1-317">Cost element</span></span></th>
<th><span data-ttu-id="b59d1-318">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="b59d1-318">Cost behavior</span></span></th>
<th><span data-ttu-id="b59d1-319">Tutar</span><span class="sxs-lookup"><span data-stu-id="b59d1-319">Amount</span></span></th>
<th><span data-ttu-id="b59d1-320">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="b59d1-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b59d1-321">CC099</span><span class="sxs-lookup"><span data-stu-id="b59d1-321">CC099</span></span></td>
<td><span data-ttu-id="b59d1-322">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="b59d1-322">Default cost center</span></span></td>
<td><span data-ttu-id="b59d1-323">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-323">10001</span></span></td>
<td><span data-ttu-id="b59d1-324">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-324">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-325">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-325">Fixed cost</span></span></td>
<td><span data-ttu-id="b59d1-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-326">-1,000.00</span></span></td>
<td><span data-ttu-id="b59d1-327">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-328">CC001</span><span class="sxs-lookup"><span data-stu-id="b59d1-328">CC001</span></span></td>
<td><span data-ttu-id="b59d1-329">İK</span><span class="sxs-lookup"><span data-stu-id="b59d1-329">HR</span></span></td>
<td><span data-ttu-id="b59d1-330">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-330">10001</span></span></td>
<td><span data-ttu-id="b59d1-331">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-331">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-332">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-332">Fixed cost</span></span></td>
<td><span data-ttu-id="b59d1-333">500.00</span><span class="sxs-lookup"><span data-stu-id="b59d1-333">500.00</span></span></td>
<td><span data-ttu-id="b59d1-334">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-335">CC002</span><span class="sxs-lookup"><span data-stu-id="b59d1-335">CC002</span></span></td>
<td><span data-ttu-id="b59d1-336">Finans</span><span class="sxs-lookup"><span data-stu-id="b59d1-336">Finance</span></span></td>
<td><span data-ttu-id="b59d1-337">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-337">10001</span></span></td>
<td><span data-ttu-id="b59d1-338">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-338">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-339">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-339">Fixed cost</span></span></td>
<td><span data-ttu-id="b59d1-340">500.00</span><span class="sxs-lookup"><span data-stu-id="b59d1-340">500.00</span></span></td>
<td><span data-ttu-id="b59d1-341">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-342">CC099</span><span class="sxs-lookup"><span data-stu-id="b59d1-342">CC099</span></span></td>
<td><span data-ttu-id="b59d1-343">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="b59d1-343">Default cost center</span></span></td>
<td><span data-ttu-id="b59d1-344">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-344">10001</span></span></td>
<td><span data-ttu-id="b59d1-345">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-345">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-346">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-346">Variable cost</span></span></td>
<td><span data-ttu-id="b59d1-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-347">-9,000.00</span></span></td>
<td><span data-ttu-id="b59d1-348">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-349">CC001</span><span class="sxs-lookup"><span data-stu-id="b59d1-349">CC001</span></span></td>
<td><span data-ttu-id="b59d1-350">İK</span><span class="sxs-lookup"><span data-stu-id="b59d1-350">HR</span></span></td>
<td><span data-ttu-id="b59d1-351">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-351">10001</span></span></td>
<td><span data-ttu-id="b59d1-352">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-352">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-353">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-353">Variable cost</span></span></td>
<td><span data-ttu-id="b59d1-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="b59d1-354">1,285.71</span></span></td>
<td><span data-ttu-id="b59d1-355">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-356">CC002</span><span class="sxs-lookup"><span data-stu-id="b59d1-356">CC002</span></span></td>
<td><span data-ttu-id="b59d1-357">Finans</span><span class="sxs-lookup"><span data-stu-id="b59d1-357">Finance</span></span></td>
<td><span data-ttu-id="b59d1-358">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-358">10001</span></span></td>
<td><span data-ttu-id="b59d1-359">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-359">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-360">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-360">Variable cost</span></span></td>
<td><span data-ttu-id="b59d1-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="b59d1-361">7,714.29</span></span></td>
<td><span data-ttu-id="b59d1-362">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b59d1-363">Daha fazla bilgi için bkz. [Maliyet dağıtımı ilkesi oluşturma ve bir maliyet kontrol birimine atama](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="b59d1-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="b59d1-364">Adım 3: Genel gider oranı hesaplama işlemi</span><span class="sxs-lookup"><span data-stu-id="b59d1-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="b59d1-365">Genel gider oranı, bir veya birden fazla belirli maliyet nesnesine masraf yüklemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b59d1-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="b59d1-366">Masraf, önceden belirlenmiş maliyet oranına ve tahsisat tabanından hesaplanan büyüklüğe dayanır.</span><span class="sxs-lookup"><span data-stu-id="b59d1-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="b59d1-367">Genel gider oranını tanımlama</span><span class="sxs-lookup"><span data-stu-id="b59d1-367">Define the overhead rate</span></span>

<span data-ttu-id="b59d1-368">Maliyet nesnesi CC001 HR, bir dizi dahili projeye katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="b59d1-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="b59d1-369">HR projeleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b59d1-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b59d1-370">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="b59d1-370">Cost object</span></span></th>
<th><span data-ttu-id="b59d1-371">Saatler</span><span class="sxs-lookup"><span data-stu-id="b59d1-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b59d1-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-372">Proj 1</span></span></td>
<td><span data-ttu-id="b59d1-373">Proje 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-373">Project 1</span></span></td>
<td><span data-ttu-id="b59d1-374">3</span><span class="sxs-lookup"><span data-stu-id="b59d1-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="b59d1-375">Proj 2</span></span></td>
<td><span data-ttu-id="b59d1-376">Proje 2</span><span class="sxs-lookup"><span data-stu-id="b59d1-376">Project 2</span></span></td>
<td><span data-ttu-id="b59d1-377">1</span><span class="sxs-lookup"><span data-stu-id="b59d1-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b59d1-378">Maliyet projeleri dağıtımı için bir önceden belirlenmiş maliyet oranı tanımlandı.</span><span class="sxs-lookup"><span data-stu-id="b59d1-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b59d1-379">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="b59d1-379">Cost object</span></span></th>
<th><span data-ttu-id="b59d1-380">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="b59d1-380">Cost element</span></span></th>
<th><span data-ttu-id="b59d1-381">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="b59d1-381">Cost behavior</span></span></th>
<th><span data-ttu-id="b59d1-382">Birimler</span><span class="sxs-lookup"><span data-stu-id="b59d1-382">Units</span></span></th>
<th><span data-ttu-id="b59d1-383">Ücret</span><span class="sxs-lookup"><span data-stu-id="b59d1-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b59d1-384">CC001</span><span class="sxs-lookup"><span data-stu-id="b59d1-384">CC001</span></span></td>
<td><span data-ttu-id="b59d1-385">İK</span><span class="sxs-lookup"><span data-stu-id="b59d1-385">HR</span></span></td>
<td><span data-ttu-id="b59d1-386">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-386">10001</span></span></td>
<td><span data-ttu-id="b59d1-387">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-387">Variable cost</span></span></td>
<td><span data-ttu-id="b59d1-388">1</span><span class="sxs-lookup"><span data-stu-id="b59d1-388">1</span></span></td>
<td><span data-ttu-id="b59d1-389">10</span><span class="sxs-lookup"><span data-stu-id="b59d1-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b59d1-390">Aşağıdaki tablo, HR projeleri bir tahsisat tabanı olarak uygulandığındaki sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="b59d1-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b59d1-391">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="b59d1-391">Cost object</span></span></th>
<th><span data-ttu-id="b59d1-392">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="b59d1-392">Magnitude</span></span></th>
<th><span data-ttu-id="b59d1-393">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="b59d1-393">Cost element</span></span></th>
<th><span data-ttu-id="b59d1-394">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="b59d1-394">Allocation factor</span></span></th>
<th><span data-ttu-id="b59d1-395">Tutar</span><span class="sxs-lookup"><span data-stu-id="b59d1-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b59d1-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-396">Proj 1</span></span></td>
<td><span data-ttu-id="b59d1-397">Proje 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-397">Project 1</span></span></td>
<td><span data-ttu-id="b59d1-398">3</span><span class="sxs-lookup"><span data-stu-id="b59d1-398">3</span></span></td>
<td><span data-ttu-id="b59d1-399">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-399">10001</span></span></td>
<td><span data-ttu-id="b59d1-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="b59d1-401">30.00</span><span class="sxs-lookup"><span data-stu-id="b59d1-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="b59d1-402">Proj 2</span></span></td>
<td><span data-ttu-id="b59d1-403">Proje 2</span><span class="sxs-lookup"><span data-stu-id="b59d1-403">Project 2</span></span></td>
<td><span data-ttu-id="b59d1-404">1</span><span class="sxs-lookup"><span data-stu-id="b59d1-404">1</span></span></td>
<td><span data-ttu-id="b59d1-405">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-405">10001</span></span></td>
<td><span data-ttu-id="b59d1-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="b59d1-407">10,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="b59d1-408">Günlük</span><span class="sxs-lookup"><span data-stu-id="b59d1-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b59d1-409">Günlük</span><span class="sxs-lookup"><span data-stu-id="b59d1-409">Journal</span></span></th>
<th><span data-ttu-id="b59d1-410">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="b59d1-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="b59d1-411">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="b59d1-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="b59d1-412">Sürüm</span><span class="sxs-lookup"><span data-stu-id="b59d1-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b59d1-413">00003</span><span class="sxs-lookup"><span data-stu-id="b59d1-413">00003</span></span></td>
<td><span data-ttu-id="b59d1-414">Genel gider oranı hesaplaması günlüğü</span><span class="sxs-lookup"><span data-stu-id="b59d1-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="b59d1-415">Mali</span><span class="sxs-lookup"><span data-stu-id="b59d1-415">Fiscal</span></span></td>
<td><span data-ttu-id="b59d1-416">2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-416">2017</span></span></td>
<td><span data-ttu-id="b59d1-417">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-417">Period 1</span></span></td>
<td><span data-ttu-id="b59d1-418">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="b59d1-419">Günlük girişleri (Genel gider oranı hesaplaması için günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="b59d1-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b59d1-420">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="b59d1-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b59d1-421">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="b59d1-421">Cost object</span></span></th>
<th><span data-ttu-id="b59d1-422">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="b59d1-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b59d1-423">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="b59d1-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-424">Proj 1</span></span></td>
<td><span data-ttu-id="b59d1-425">Dahili Proj 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="b59d1-426">3,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-427">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="b59d1-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="b59d1-428">Proj 2</span></span></td>
<td><span data-ttu-id="b59d1-429">Dahili Proj 2</span><span class="sxs-lookup"><span data-stu-id="b59d1-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="b59d1-430">1.00</span><span class="sxs-lookup"><span data-stu-id="b59d1-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="b59d1-431">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="b59d1-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b59d1-432">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="b59d1-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b59d1-433">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="b59d1-433">Cost element</span></span></th>
<th><span data-ttu-id="b59d1-434">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="b59d1-434">Cost behavior</span></span></th>
<th><span data-ttu-id="b59d1-435">Tutar</span><span class="sxs-lookup"><span data-stu-id="b59d1-435">Amount</span></span></th>
<th><span data-ttu-id="b59d1-436">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="b59d1-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b59d1-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="b59d1-437">CC0001</span></span></td>
<td><span data-ttu-id="b59d1-438">İK</span><span class="sxs-lookup"><span data-stu-id="b59d1-438">HR</span></span></td>
<td><span data-ttu-id="b59d1-439">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-439">10001</span></span></td>
<td><span data-ttu-id="b59d1-440">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-440">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-441">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-441">Variable cost</span></span></td>
<td><span data-ttu-id="b59d1-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-442">-30.00</span></span></td>
<td><span data-ttu-id="b59d1-443">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-444">Proj 1</span></span></td>
<td><span data-ttu-id="b59d1-445">Dahili Proj 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="b59d1-446">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-446">10001</span></span></td>
<td><span data-ttu-id="b59d1-447">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-447">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-448">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-448">Variable cost</span></span></td>
<td><span data-ttu-id="b59d1-449">30.00</span><span class="sxs-lookup"><span data-stu-id="b59d1-449">30.00</span></span></td>
<td><span data-ttu-id="b59d1-450">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-451">CC001</span><span class="sxs-lookup"><span data-stu-id="b59d1-451">CC001</span></span></td>
<td><span data-ttu-id="b59d1-452">İK</span><span class="sxs-lookup"><span data-stu-id="b59d1-452">HR</span></span></td>
<td><span data-ttu-id="b59d1-453">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-453">10001</span></span></td>
<td><span data-ttu-id="b59d1-454">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-454">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-455">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-455">Variable cost</span></span></td>
<td><span data-ttu-id="b59d1-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-456">-10.00</span></span></td>
<td><span data-ttu-id="b59d1-457">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="b59d1-458">Proj 2</span></span></td>
<td><span data-ttu-id="b59d1-459">Dahili Proj 2</span><span class="sxs-lookup"><span data-stu-id="b59d1-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="b59d1-460">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-460">10001</span></span></td>
<td><span data-ttu-id="b59d1-461">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-461">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-462">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-462">Variable cost</span></span></td>
<td><span data-ttu-id="b59d1-463">10,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-463">10.00</span></span></td>
<td><span data-ttu-id="b59d1-464">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b59d1-465">Daha fazla bilgi için [Genel gider hesaplaması gerçekleştir](cost-rollup.md#perform-overhead-calculation) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="b59d1-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="b59d1-466">Adım 4: Maliyet tahsisat hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="b59d1-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="b59d1-467">Tahsisat, bir tahsisat tabanı kullanarak bir maliyet nesnesinin diğer maliyet nesnelerine bakiyesini tahsis eder.</span><span class="sxs-lookup"><span data-stu-id="b59d1-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="b59d1-468">Finance karşılıklı tahsisat yöntemini desteklemektedir.</span><span class="sxs-lookup"><span data-stu-id="b59d1-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="b59d1-469">Karşılıklı tahsisat yönteminde, yardımcı maliyet nesnelerinin değiştiği karşılıklı hizmetler tümüyle tanınır.</span><span class="sxs-lookup"><span data-stu-id="b59d1-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="b59d1-470">Sistem, tahsisatların doğru gerçekleştireceği sırayı otomatik olarak belirler.</span><span class="sxs-lookup"><span data-stu-id="b59d1-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="b59d1-471">Bir maliyet nesnesinin bakiyesi tek bir tahsisat tabanı tarafından tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="b59d1-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="b59d1-472">Yeni maliyet nesnesi boyutları arasındaki tahsisatlar ve onların üyeleri desteklenir.</span><span class="sxs-lookup"><span data-stu-id="b59d1-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="b59d1-473">Tahsisatın sırası, maliyet kontrol birimi tarafından kontrol edilir.</span><span class="sxs-lookup"><span data-stu-id="b59d1-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="b59d1-474">[![Karşılıklı yöntemi](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="b59d1-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="b59d1-475">Maliyet tahsisatını tanımla</span><span class="sxs-lookup"><span data-stu-id="b59d1-475">Define the cost allocation</span></span>

<span data-ttu-id="b59d1-476">Bir maliyetin akışını nasıl izleyeceğinize dair basit bir örnek aşağıda verilmiştir,</span><span class="sxs-lookup"><span data-stu-id="b59d1-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="b59d1-477">Maliyet nesnesi CC001 HR, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="b59d1-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="b59d1-478">HR hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b59d1-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b59d1-479">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="b59d1-479">Cost object</span></span></th>
<th><span data-ttu-id="b59d1-480">HR hizmetleri</span><span class="sxs-lookup"><span data-stu-id="b59d1-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b59d1-481">CC002</span><span class="sxs-lookup"><span data-stu-id="b59d1-481">CC002</span></span></td>
<td><span data-ttu-id="b59d1-482">Finans</span><span class="sxs-lookup"><span data-stu-id="b59d1-482">Finance</span></span></td>
<td><span data-ttu-id="b59d1-483">35</span><span class="sxs-lookup"><span data-stu-id="b59d1-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-484">CC003</span><span class="sxs-lookup"><span data-stu-id="b59d1-484">CC003</span></span></td>
<td><span data-ttu-id="b59d1-485">Montaj</span><span class="sxs-lookup"><span data-stu-id="b59d1-485">Assembly</span></span></td>
<td><span data-ttu-id="b59d1-486">55</span><span class="sxs-lookup"><span data-stu-id="b59d1-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-487">CC004</span><span class="sxs-lookup"><span data-stu-id="b59d1-487">CC004</span></span></td>
<td><span data-ttu-id="b59d1-488">Paketleme</span><span class="sxs-lookup"><span data-stu-id="b59d1-488">Packaging</span></span></td>
<td><span data-ttu-id="b59d1-489">10</span><span class="sxs-lookup"><span data-stu-id="b59d1-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b59d1-490">Maliyet nesnesi CC002 Finans, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="b59d1-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="b59d1-491">Finans hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b59d1-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b59d1-492">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="b59d1-492">Cost object</span></span></th>
<th><span data-ttu-id="b59d1-493">Finans hizmetleri</span><span class="sxs-lookup"><span data-stu-id="b59d1-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b59d1-494">CC003</span><span class="sxs-lookup"><span data-stu-id="b59d1-494">CC003</span></span></td>
<td><span data-ttu-id="b59d1-495">Montaj</span><span class="sxs-lookup"><span data-stu-id="b59d1-495">Assembly</span></span></td>
<td><span data-ttu-id="b59d1-496">65</span><span class="sxs-lookup"><span data-stu-id="b59d1-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-497">CC004</span><span class="sxs-lookup"><span data-stu-id="b59d1-497">CC004</span></span></td>
<td><span data-ttu-id="b59d1-498">Paketleme</span><span class="sxs-lookup"><span data-stu-id="b59d1-498">Packaging</span></span></td>
<td><span data-ttu-id="b59d1-499">35</span><span class="sxs-lookup"><span data-stu-id="b59d1-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b59d1-500">Maliyet nesnesi CC003 Derleme, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="b59d1-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="b59d1-501">Derleme hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b59d1-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b59d1-502">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="b59d1-502">Cost object</span></span></th>
<th><span data-ttu-id="b59d1-503">Derleme Hizmetleri (saat)</span><span class="sxs-lookup"><span data-stu-id="b59d1-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b59d1-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-504">Prod 1</span></span></td>
<td><span data-ttu-id="b59d1-505">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-505">Product 1</span></span></td>
<td><span data-ttu-id="b59d1-506">60</span><span class="sxs-lookup"><span data-stu-id="b59d1-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b59d1-507">Prod 2</span></span></td>
<td><span data-ttu-id="b59d1-508">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="b59d1-508">Product 2</span></span></td>
<td><span data-ttu-id="b59d1-509">20</span><span class="sxs-lookup"><span data-stu-id="b59d1-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b59d1-510">Maliyet nesnesi CC004 Ambalajlama, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="b59d1-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="b59d1-511">Ambalajlama hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b59d1-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b59d1-512">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="b59d1-512">Cost object</span></span></th>
<th><span data-ttu-id="b59d1-513">Ambalajlama hizmetleri (saat)</span><span class="sxs-lookup"><span data-stu-id="b59d1-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b59d1-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-514">Prod 1</span></span></td>
<td><span data-ttu-id="b59d1-515">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-515">Product 1</span></span></td>
<td><span data-ttu-id="b59d1-516">80</span><span class="sxs-lookup"><span data-stu-id="b59d1-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b59d1-517">Prod 2</span></span></td>
<td><span data-ttu-id="b59d1-518">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="b59d1-518">Product 2</span></span></td>
<td><span data-ttu-id="b59d1-519">15</span><span class="sxs-lookup"><span data-stu-id="b59d1-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="b59d1-520">Bir ürünün tükettiği üretim saatleri gibi istatistiki ölçümler, doğrudan kaynak verilerinden alınabilir.</span><span class="sxs-lookup"><span data-stu-id="b59d1-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="b59d1-521">Daha fazla bilgi için, [İstatistiksel ölçüm sağlayıcı şablonu](statistical-measure-provider-template.md#statistical-measure-provider-template) bakın.</span><span class="sxs-lookup"><span data-stu-id="b59d1-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="b59d1-522">Aşağıdaki tablo, İK hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığında ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="b59d1-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b59d1-523">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="b59d1-523">Cost object</span></span></th>
<th><span data-ttu-id="b59d1-524">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="b59d1-524">Magnitude</span></span></th>
<th><span data-ttu-id="b59d1-525">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="b59d1-525">Allocation factor</span></span></th>
<th><span data-ttu-id="b59d1-526">Tutar</span><span class="sxs-lookup"><span data-stu-id="b59d1-526">Amount</span></span></th>
<th><span data-ttu-id="b59d1-527">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="b59d1-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b59d1-528">CC002</span><span class="sxs-lookup"><span data-stu-id="b59d1-528">CC002</span></span></td>
<td><span data-ttu-id="b59d1-529">Finans</span><span class="sxs-lookup"><span data-stu-id="b59d1-529">Finance</span></span></td>
<td><span data-ttu-id="b59d1-530">35</span><span class="sxs-lookup"><span data-stu-id="b59d1-530">35</span></span></td>
<td><span data-ttu-id="b59d1-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="b59d1-532">175.00</span><span class="sxs-lookup"><span data-stu-id="b59d1-532">175.00</span></span></td>
<td><span data-ttu-id="b59d1-533">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-534">CC003</span><span class="sxs-lookup"><span data-stu-id="b59d1-534">CC003</span></span></td>
<td><span data-ttu-id="b59d1-535">Montaj</span><span class="sxs-lookup"><span data-stu-id="b59d1-535">Assembly</span></span></td>
<td><span data-ttu-id="b59d1-536">55</span><span class="sxs-lookup"><span data-stu-id="b59d1-536">55</span></span></td>
<td><span data-ttu-id="b59d1-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="b59d1-538">275.00</span><span class="sxs-lookup"><span data-stu-id="b59d1-538">275.00</span></span></td>
<td><span data-ttu-id="b59d1-539">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-540">CC004</span><span class="sxs-lookup"><span data-stu-id="b59d1-540">CC004</span></span></td>
<td><span data-ttu-id="b59d1-541">Paketleme</span><span class="sxs-lookup"><span data-stu-id="b59d1-541">Packaging</span></span></td>
<td><span data-ttu-id="b59d1-542">10</span><span class="sxs-lookup"><span data-stu-id="b59d1-542">10</span></span></td>
<td><span data-ttu-id="b59d1-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="b59d1-544">50,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-544">50.00</span></span></td>
<td><span data-ttu-id="b59d1-545">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-546">CC002</span><span class="sxs-lookup"><span data-stu-id="b59d1-546">CC002</span></span></td>
<td><span data-ttu-id="b59d1-547">Finans</span><span class="sxs-lookup"><span data-stu-id="b59d1-547">Finance</span></span></td>
<td><span data-ttu-id="b59d1-548">35</span><span class="sxs-lookup"><span data-stu-id="b59d1-548">35</span></span></td>
<td><span data-ttu-id="b59d1-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="b59d1-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="b59d1-550">436.00</span><span class="sxs-lookup"><span data-stu-id="b59d1-550">436.00</span></span></td>
<td><span data-ttu-id="b59d1-551">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-552">CC003</span><span class="sxs-lookup"><span data-stu-id="b59d1-552">CC003</span></span></td>
<td><span data-ttu-id="b59d1-553">Montaj</span><span class="sxs-lookup"><span data-stu-id="b59d1-553">Assembly</span></span></td>
<td><span data-ttu-id="b59d1-554">55</span><span class="sxs-lookup"><span data-stu-id="b59d1-554">55</span></span></td>
<td><span data-ttu-id="b59d1-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="b59d1-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="b59d1-556">685.14</span><span class="sxs-lookup"><span data-stu-id="b59d1-556">685.14</span></span></td>
<td><span data-ttu-id="b59d1-557">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-558">CC004</span><span class="sxs-lookup"><span data-stu-id="b59d1-558">CC004</span></span></td>
<td><span data-ttu-id="b59d1-559">Paketleme</span><span class="sxs-lookup"><span data-stu-id="b59d1-559">Packaging</span></span></td>
<td><span data-ttu-id="b59d1-560">10</span><span class="sxs-lookup"><span data-stu-id="b59d1-560">10</span></span></td>
<td><span data-ttu-id="b59d1-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="b59d1-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="b59d1-562">124.57</span><span class="sxs-lookup"><span data-stu-id="b59d1-562">124.57</span></span></td>
<td><span data-ttu-id="b59d1-563">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b59d1-564">Aşağıdaki tablo, Finans hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="b59d1-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b59d1-565">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="b59d1-565">Cost object</span></span></th>
<th><span data-ttu-id="b59d1-566">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="b59d1-566">Magnitude</span></span></th>
<th><span data-ttu-id="b59d1-567">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="b59d1-567">Allocation factor</span></span></th>
<th><span data-ttu-id="b59d1-568">Tutar</span><span class="sxs-lookup"><span data-stu-id="b59d1-568">Amount</span></span></th>
<th><span data-ttu-id="b59d1-569">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="b59d1-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b59d1-570">CC003</span><span class="sxs-lookup"><span data-stu-id="b59d1-570">CC003</span></span></td>
<td><span data-ttu-id="b59d1-571">Montaj</span><span class="sxs-lookup"><span data-stu-id="b59d1-571">Assembly</span></span></td>
<td><span data-ttu-id="b59d1-572">65</span><span class="sxs-lookup"><span data-stu-id="b59d1-572">65</span></span></td>
<td><span data-ttu-id="b59d1-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="b59d1-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="b59d1-574">438.75</span><span class="sxs-lookup"><span data-stu-id="b59d1-574">438.75</span></span></td>
<td><span data-ttu-id="b59d1-575">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-576">CC004</span><span class="sxs-lookup"><span data-stu-id="b59d1-576">CC004</span></span></td>
<td><span data-ttu-id="b59d1-577">Paketleme</span><span class="sxs-lookup"><span data-stu-id="b59d1-577">Packaging</span></span></td>
<td><span data-ttu-id="b59d1-578">35</span><span class="sxs-lookup"><span data-stu-id="b59d1-578">35</span></span></td>
<td><span data-ttu-id="b59d1-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="b59d1-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="b59d1-580">236.25</span><span class="sxs-lookup"><span data-stu-id="b59d1-580">236.25</span></span></td>
<td><span data-ttu-id="b59d1-581">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-582">CC003</span><span class="sxs-lookup"><span data-stu-id="b59d1-582">CC003</span></span></td>
<td><span data-ttu-id="b59d1-583">Montaj</span><span class="sxs-lookup"><span data-stu-id="b59d1-583">Assembly</span></span></td>
<td><span data-ttu-id="b59d1-584">65</span><span class="sxs-lookup"><span data-stu-id="b59d1-584">65</span></span></td>
<td><span data-ttu-id="b59d1-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="b59d1-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="b59d1-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="b59d1-586">5,297.69</span></span></td>
<td><span data-ttu-id="b59d1-587">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-588">CC004</span><span class="sxs-lookup"><span data-stu-id="b59d1-588">CC004</span></span></td>
<td><span data-ttu-id="b59d1-589">Paketleme</span><span class="sxs-lookup"><span data-stu-id="b59d1-589">Packaging</span></span></td>
<td><span data-ttu-id="b59d1-590">35</span><span class="sxs-lookup"><span data-stu-id="b59d1-590">35</span></span></td>
<td><span data-ttu-id="b59d1-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="b59d1-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="b59d1-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="b59d1-592">2,852.60</span></span></td>
<td><span data-ttu-id="b59d1-593">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b59d1-594">Aşağıdaki tablo, Derleme hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="b59d1-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b59d1-595">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="b59d1-595">Cost object</span></span></th>
<th><span data-ttu-id="b59d1-596">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="b59d1-596">Magnitude</span></span></th>
<th><span data-ttu-id="b59d1-597">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="b59d1-597">Allocation factor</span></span></th>
<th><span data-ttu-id="b59d1-598">Tutar</span><span class="sxs-lookup"><span data-stu-id="b59d1-598">Amount</span></span></th>
<th><span data-ttu-id="b59d1-599">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="b59d1-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b59d1-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-600">Prod 1</span></span></td>
<td><span data-ttu-id="b59d1-601">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-601">Product 1</span></span></td>
<td><span data-ttu-id="b59d1-602">60</span><span class="sxs-lookup"><span data-stu-id="b59d1-602">60</span></span></td>
<td><span data-ttu-id="b59d1-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="b59d1-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="b59d1-604">535.31</span><span class="sxs-lookup"><span data-stu-id="b59d1-604">535.31</span></span></td>
<td><span data-ttu-id="b59d1-605">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b59d1-606">Prod 2</span></span></td>
<td><span data-ttu-id="b59d1-607">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="b59d1-607">Product 2</span></span></td>
<td><span data-ttu-id="b59d1-608">20</span><span class="sxs-lookup"><span data-stu-id="b59d1-608">20</span></span></td>
<td><span data-ttu-id="b59d1-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="b59d1-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="b59d1-610">178.44</span><span class="sxs-lookup"><span data-stu-id="b59d1-610">178.44</span></span></td>
<td><span data-ttu-id="b59d1-611">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-612">Prod 1</span></span></td>
<td><span data-ttu-id="b59d1-613">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-613">Product 1</span></span></td>
<td><span data-ttu-id="b59d1-614">60</span><span class="sxs-lookup"><span data-stu-id="b59d1-614">60</span></span></td>
<td><span data-ttu-id="b59d1-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="b59d1-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="b59d1-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="b59d1-616">4,487.12</span></span></td>
<td><span data-ttu-id="b59d1-617">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b59d1-618">Prod 2</span></span></td>
<td><span data-ttu-id="b59d1-619">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="b59d1-619">Product 2</span></span></td>
<td><span data-ttu-id="b59d1-620">20</span><span class="sxs-lookup"><span data-stu-id="b59d1-620">20</span></span></td>
<td><span data-ttu-id="b59d1-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="b59d1-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="b59d1-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="b59d1-622">1,495.71</span></span></td>
<td><span data-ttu-id="b59d1-623">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b59d1-624">Aşağıdaki tablo, Paketleme hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="b59d1-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b59d1-625">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="b59d1-625">Cost object</span></span></th>
<th><span data-ttu-id="b59d1-626">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="b59d1-626">Magnitude</span></span></th>
<th><span data-ttu-id="b59d1-627">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="b59d1-627">Allocation factor</span></span></th>
<th><span data-ttu-id="b59d1-628">Tutar</span><span class="sxs-lookup"><span data-stu-id="b59d1-628">Amount</span></span></th>
<th><span data-ttu-id="b59d1-629">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="b59d1-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b59d1-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-630">Prod 1</span></span></td>
<td><span data-ttu-id="b59d1-631">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-631">Product 1</span></span></td>
<td><span data-ttu-id="b59d1-632">80</span><span class="sxs-lookup"><span data-stu-id="b59d1-632">80</span></span></td>
<td><span data-ttu-id="b59d1-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="b59d1-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="b59d1-634">241.05</span><span class="sxs-lookup"><span data-stu-id="b59d1-634">241.05</span></span></td>
<td><span data-ttu-id="b59d1-635">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b59d1-636">Prod 2</span></span></td>
<td><span data-ttu-id="b59d1-637">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="b59d1-637">Product 2</span></span></td>
<td><span data-ttu-id="b59d1-638">15</span><span class="sxs-lookup"><span data-stu-id="b59d1-638">15</span></span></td>
<td><span data-ttu-id="b59d1-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="b59d1-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="b59d1-640">45.20</span><span class="sxs-lookup"><span data-stu-id="b59d1-640">45.20</span></span></td>
<td><span data-ttu-id="b59d1-641">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-642">Prod 1</span></span></td>
<td><span data-ttu-id="b59d1-643">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-643">Product 1</span></span></td>
<td><span data-ttu-id="b59d1-644">80</span><span class="sxs-lookup"><span data-stu-id="b59d1-644">80</span></span></td>
<td><span data-ttu-id="b59d1-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="b59d1-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="b59d1-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="b59d1-646">2,507.09</span></span></td>
<td><span data-ttu-id="b59d1-647">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b59d1-648">Prod 2</span></span></td>
<td><span data-ttu-id="b59d1-649">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="b59d1-649">Product 2</span></span></td>
<td><span data-ttu-id="b59d1-650">15</span><span class="sxs-lookup"><span data-stu-id="b59d1-650">15</span></span></td>
<td><span data-ttu-id="b59d1-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="b59d1-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="b59d1-652">470.08</span><span class="sxs-lookup"><span data-stu-id="b59d1-652">470.08</span></span></td>
<td><span data-ttu-id="b59d1-653">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="b59d1-654">Günlük girişleri (maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="b59d1-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b59d1-655">Günlük</span><span class="sxs-lookup"><span data-stu-id="b59d1-655">Journal</span></span></th>
<th><span data-ttu-id="b59d1-656">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="b59d1-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="b59d1-657">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="b59d1-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="b59d1-658">Sürüm</span><span class="sxs-lookup"><span data-stu-id="b59d1-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b59d1-659">00004</span><span class="sxs-lookup"><span data-stu-id="b59d1-659">00004</span></span></td>
<td><span data-ttu-id="b59d1-660">Maliyet tahsisatı günlüğü</span><span class="sxs-lookup"><span data-stu-id="b59d1-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="b59d1-661">Mali</span><span class="sxs-lookup"><span data-stu-id="b59d1-661">Fiscal</span></span></td>
<td><span data-ttu-id="b59d1-662">2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-662">2017</span></span></td>
<td><span data-ttu-id="b59d1-663">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-663">Period 1</span></span></td>
<td><span data-ttu-id="b59d1-664">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="b59d1-665">Günlük satırları</span><span class="sxs-lookup"><span data-stu-id="b59d1-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b59d1-666">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="b59d1-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b59d1-667">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="b59d1-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b59d1-668">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="b59d1-668">Cost element</span></span></th>
<th><span data-ttu-id="b59d1-669">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="b59d1-669">Cost behavior</span></span></th>
<th><span data-ttu-id="b59d1-670">Tutar</span><span class="sxs-lookup"><span data-stu-id="b59d1-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b59d1-671">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="b59d1-672">CC001</span><span class="sxs-lookup"><span data-stu-id="b59d1-672">CC001</span></span></td>
<td><span data-ttu-id="b59d1-673">İK</span><span class="sxs-lookup"><span data-stu-id="b59d1-673">HR</span></span></td>
<td><span data-ttu-id="b59d1-674">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-674">10001</span></span></td>
<td><span data-ttu-id="b59d1-675">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-675">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-676">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-676">Fixed cost</span></span></td>
<td><span data-ttu-id="b59d1-677">500.00</span><span class="sxs-lookup"><span data-stu-id="b59d1-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-678">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="b59d1-679">CC001</span><span class="sxs-lookup"><span data-stu-id="b59d1-679">CC001</span></span></td>
<td><span data-ttu-id="b59d1-680">İK</span><span class="sxs-lookup"><span data-stu-id="b59d1-680">HR</span></span></td>
<td><span data-ttu-id="b59d1-681">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-681">10001</span></span></td>
<td><span data-ttu-id="b59d1-682">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-682">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-683">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-683">Variable cost</span></span></td>
<td><span data-ttu-id="b59d1-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="b59d1-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-685">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="b59d1-686">CC002</span><span class="sxs-lookup"><span data-stu-id="b59d1-686">CC002</span></span></td>
<td><span data-ttu-id="b59d1-687">Finans</span><span class="sxs-lookup"><span data-stu-id="b59d1-687">Finance</span></span></td>
<td><span data-ttu-id="b59d1-688">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-688">10001</span></span></td>
<td><span data-ttu-id="b59d1-689">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-689">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-690">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-690">Fixed cost</span></span></td>
<td><span data-ttu-id="b59d1-691">675.00</span><span class="sxs-lookup"><span data-stu-id="b59d1-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-692">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="b59d1-693">CC002</span><span class="sxs-lookup"><span data-stu-id="b59d1-693">CC002</span></span></td>
<td><span data-ttu-id="b59d1-694">Finans</span><span class="sxs-lookup"><span data-stu-id="b59d1-694">Finance</span></span></td>
<td><span data-ttu-id="b59d1-695">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-695">10001</span></span></td>
<td><span data-ttu-id="b59d1-696">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-696">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-697">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-697">Variable cost</span></span></td>
<td><span data-ttu-id="b59d1-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="b59d1-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-699">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="b59d1-700">CC003</span><span class="sxs-lookup"><span data-stu-id="b59d1-700">CC003</span></span></td>
<td><span data-ttu-id="b59d1-701">Montaj</span><span class="sxs-lookup"><span data-stu-id="b59d1-701">Assembly</span></span></td>
<td><span data-ttu-id="b59d1-702">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-702">10001</span></span></td>
<td><span data-ttu-id="b59d1-703">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-703">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-704">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-704">Fixed cost</span></span></td>
<td><span data-ttu-id="b59d1-705">713.75</span><span class="sxs-lookup"><span data-stu-id="b59d1-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-706">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="b59d1-707">CC003</span><span class="sxs-lookup"><span data-stu-id="b59d1-707">CC003</span></span></td>
<td><span data-ttu-id="b59d1-708">Montaj</span><span class="sxs-lookup"><span data-stu-id="b59d1-708">Assembly</span></span></td>
<td><span data-ttu-id="b59d1-709">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-709">10001</span></span></td>
<td><span data-ttu-id="b59d1-710">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-710">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-711">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-711">Variable cost</span></span></td>
<td><span data-ttu-id="b59d1-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="b59d1-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-713">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="b59d1-714">CC003</span><span class="sxs-lookup"><span data-stu-id="b59d1-714">CC003</span></span></td>
<td><span data-ttu-id="b59d1-715">Paketleme</span><span class="sxs-lookup"><span data-stu-id="b59d1-715">Packaging</span></span></td>
<td><span data-ttu-id="b59d1-716">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-716">10001</span></span></td>
<td><span data-ttu-id="b59d1-717">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-717">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-718">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-718">Fixed cost</span></span></td>
<td><span data-ttu-id="b59d1-719">286.25</span><span class="sxs-lookup"><span data-stu-id="b59d1-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-720">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="b59d1-721">CC003</span><span class="sxs-lookup"><span data-stu-id="b59d1-721">CC003</span></span></td>
<td><span data-ttu-id="b59d1-722">Paketleme</span><span class="sxs-lookup"><span data-stu-id="b59d1-722">Packaging</span></span></td>
<td><span data-ttu-id="b59d1-723">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-723">10001</span></span></td>
<td><span data-ttu-id="b59d1-724">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-724">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-725">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-725">Variable cost</span></span></td>
<td><span data-ttu-id="b59d1-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="b59d1-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-727">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="b59d1-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-728">Prod 1</span></span></td>
<td><span data-ttu-id="b59d1-729">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-729">Product 1</span></span></td>
<td><span data-ttu-id="b59d1-730">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-730">10001</span></span></td>
<td><span data-ttu-id="b59d1-731">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-731">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-732">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-732">Fixed cost</span></span></td>
<td><span data-ttu-id="b59d1-733">776.36</span><span class="sxs-lookup"><span data-stu-id="b59d1-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-734">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="b59d1-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-735">Prod 1</span></span></td>
<td><span data-ttu-id="b59d1-736">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-736">Product 1</span></span></td>
<td><span data-ttu-id="b59d1-737">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-737">10001</span></span></td>
<td><span data-ttu-id="b59d1-738">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-738">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-739">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-739">Variable cost</span></span></td>
<td><span data-ttu-id="b59d1-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="b59d1-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-741">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="b59d1-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b59d1-742">Prod 2</span></span></td>
<td><span data-ttu-id="b59d1-743">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-743">Product 1</span></span></td>
<td><span data-ttu-id="b59d1-744">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-744">10001</span></span></td>
<td><span data-ttu-id="b59d1-745">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-745">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-746">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-746">Fixed cost</span></span></td>
<td><span data-ttu-id="b59d1-747">223.64</span><span class="sxs-lookup"><span data-stu-id="b59d1-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-748">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="b59d1-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b59d1-749">Prod 2</span></span></td>
<td><span data-ttu-id="b59d1-750">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-750">Product 1</span></span></td>
<td><span data-ttu-id="b59d1-751">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-751">10001</span></span></td>
<td><span data-ttu-id="b59d1-752">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-752">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-753">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-753">Variable cost</span></span></td>
<td><span data-ttu-id="b59d1-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="b59d1-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="b59d1-755">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="b59d1-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b59d1-756">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="b59d1-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b59d1-757">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="b59d1-757">Cost element</span></span></th>
<th><span data-ttu-id="b59d1-758">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="b59d1-758">Cost behavior</span></span></th>
<th><span data-ttu-id="b59d1-759">Tutar</span><span class="sxs-lookup"><span data-stu-id="b59d1-759">Amount</span></span></th>
<th><span data-ttu-id="b59d1-760">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="b59d1-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b59d1-761">CC001</span><span class="sxs-lookup"><span data-stu-id="b59d1-761">CC001</span></span></td>
<td><span data-ttu-id="b59d1-762">İK</span><span class="sxs-lookup"><span data-stu-id="b59d1-762">HR</span></span></td>
<td><span data-ttu-id="b59d1-763">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-763">10001</span></span></td>
<td><span data-ttu-id="b59d1-764">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-764">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-765">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-765">Fixed cost</span></span></td>
<td><span data-ttu-id="b59d1-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="b59d1-766">-500.00</span></span></td>
<td><span data-ttu-id="b59d1-767">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-768">CC002</span><span class="sxs-lookup"><span data-stu-id="b59d1-768">CC002</span></span></td>
<td><span data-ttu-id="b59d1-769">Finans</span><span class="sxs-lookup"><span data-stu-id="b59d1-769">Finance</span></span></td>
<td><span data-ttu-id="b59d1-770">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-770">10001</span></span></td>
<td><span data-ttu-id="b59d1-771">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-771">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-772">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-772">Fixed cost</span></span></td>
<td><span data-ttu-id="b59d1-773">175.00</span><span class="sxs-lookup"><span data-stu-id="b59d1-773">175.00</span></span></td>
<td><span data-ttu-id="b59d1-774">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-775">CC003</span><span class="sxs-lookup"><span data-stu-id="b59d1-775">CC003</span></span></td>
<td><span data-ttu-id="b59d1-776">Montaj</span><span class="sxs-lookup"><span data-stu-id="b59d1-776">Assembly</span></span></td>
<td><span data-ttu-id="b59d1-777">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-777">10001</span></span></td>
<td><span data-ttu-id="b59d1-778">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-778">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-779">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-779">Fixed cost</span></span></td>
<td><span data-ttu-id="b59d1-780">275.00</span><span class="sxs-lookup"><span data-stu-id="b59d1-780">275.00</span></span></td>
<td><span data-ttu-id="b59d1-781">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-782">CC004</span><span class="sxs-lookup"><span data-stu-id="b59d1-782">CC004</span></span></td>
<td><span data-ttu-id="b59d1-783">Paketleme</span><span class="sxs-lookup"><span data-stu-id="b59d1-783">Packaging</span></span></td>
<td><span data-ttu-id="b59d1-784">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-784">10001</span></span></td>
<td><span data-ttu-id="b59d1-785">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-785">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-786">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-786">Fixed cost</span></span></td>
<td><span data-ttu-id="b59d1-787">50,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-787">50,00</span></span></td>
<td><span data-ttu-id="b59d1-788">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-789">CC001</span><span class="sxs-lookup"><span data-stu-id="b59d1-789">CC001</span></span></td>
<td><span data-ttu-id="b59d1-790">İK</span><span class="sxs-lookup"><span data-stu-id="b59d1-790">HR</span></span></td>
<td><span data-ttu-id="b59d1-791">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-791">10001</span></span></td>
<td><span data-ttu-id="b59d1-792">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-792">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-793">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-793">Variable cost</span></span></td>
<td><span data-ttu-id="b59d1-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="b59d1-794">-1,245.71</span></span></td>
<td><span data-ttu-id="b59d1-795">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-796">CC002</span><span class="sxs-lookup"><span data-stu-id="b59d1-796">CC002</span></span></td>
<td><span data-ttu-id="b59d1-797">Finans</span><span class="sxs-lookup"><span data-stu-id="b59d1-797">Finance</span></span></td>
<td><span data-ttu-id="b59d1-798">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-798">10001</span></span></td>
<td><span data-ttu-id="b59d1-799">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-799">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-800">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-800">Variable cost</span></span></td>
<td><span data-ttu-id="b59d1-801">436.00</span><span class="sxs-lookup"><span data-stu-id="b59d1-801">436.00</span></span></td>
<td><span data-ttu-id="b59d1-802">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-803">CC003</span><span class="sxs-lookup"><span data-stu-id="b59d1-803">CC003</span></span></td>
<td><span data-ttu-id="b59d1-804">Montaj</span><span class="sxs-lookup"><span data-stu-id="b59d1-804">Assembly</span></span></td>
<td><span data-ttu-id="b59d1-805">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-805">10001</span></span></td>
<td><span data-ttu-id="b59d1-806">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-806">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-807">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-807">Variable cost</span></span></td>
<td><span data-ttu-id="b59d1-808">685.14</span><span class="sxs-lookup"><span data-stu-id="b59d1-808">685.14</span></span></td>
<td><span data-ttu-id="b59d1-809">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-810">CC004</span><span class="sxs-lookup"><span data-stu-id="b59d1-810">CC004</span></span></td>
<td><span data-ttu-id="b59d1-811">Paketleme</span><span class="sxs-lookup"><span data-stu-id="b59d1-811">Packaging</span></span></td>
<td><span data-ttu-id="b59d1-812">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-812">10001</span></span></td>
<td><span data-ttu-id="b59d1-813">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-813">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-814">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-814">Variable cost</span></span></td>
<td><span data-ttu-id="b59d1-815">124.57</span><span class="sxs-lookup"><span data-stu-id="b59d1-815">124.57</span></span></td>
<td><span data-ttu-id="b59d1-816">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-817">CC002</span><span class="sxs-lookup"><span data-stu-id="b59d1-817">CC002</span></span></td>
<td><span data-ttu-id="b59d1-818">Finans</span><span class="sxs-lookup"><span data-stu-id="b59d1-818">Finance</span></span></td>
<td><span data-ttu-id="b59d1-819">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-819">10001</span></span></td>
<td><span data-ttu-id="b59d1-820">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-820">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-821">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-821">Fixed cost</span></span></td>
<td><span data-ttu-id="b59d1-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-822">-675.00</span></span></td>
<td><span data-ttu-id="b59d1-823">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-824">CC003</span><span class="sxs-lookup"><span data-stu-id="b59d1-824">CC003</span></span></td>
<td><span data-ttu-id="b59d1-825">Montaj</span><span class="sxs-lookup"><span data-stu-id="b59d1-825">Assembly</span></span></td>
<td><span data-ttu-id="b59d1-826">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-826">10001</span></span></td>
<td><span data-ttu-id="b59d1-827">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-827">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-828">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-828">Fixed cost</span></span></td>
<td><span data-ttu-id="b59d1-829">438.75</span><span class="sxs-lookup"><span data-stu-id="b59d1-829">438.75</span></span></td>
<td><span data-ttu-id="b59d1-830">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-831">CC004</span><span class="sxs-lookup"><span data-stu-id="b59d1-831">CC004</span></span></td>
<td><span data-ttu-id="b59d1-832">Paketleme</span><span class="sxs-lookup"><span data-stu-id="b59d1-832">Packaging</span></span></td>
<td><span data-ttu-id="b59d1-833">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-833">10001</span></span></td>
<td><span data-ttu-id="b59d1-834">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-834">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-835">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-835">Fixed cost</span></span></td>
<td><span data-ttu-id="b59d1-836">236.25</span><span class="sxs-lookup"><span data-stu-id="b59d1-836">236.25</span></span></td>
<td><span data-ttu-id="b59d1-837">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-838">CC002</span><span class="sxs-lookup"><span data-stu-id="b59d1-838">CC002</span></span></td>
<td><span data-ttu-id="b59d1-839">Finans</span><span class="sxs-lookup"><span data-stu-id="b59d1-839">Finance</span></span></td>
<td><span data-ttu-id="b59d1-840">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-840">10001</span></span></td>
<td><span data-ttu-id="b59d1-841">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-841">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-842">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-842">Variable cost</span></span></td>
<td><span data-ttu-id="b59d1-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="b59d1-843">-8,150.29</span></span></td>
<td><span data-ttu-id="b59d1-844">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-845">CC003</span><span class="sxs-lookup"><span data-stu-id="b59d1-845">CC003</span></span></td>
<td><span data-ttu-id="b59d1-846">Montaj</span><span class="sxs-lookup"><span data-stu-id="b59d1-846">Assembly</span></span></td>
<td><span data-ttu-id="b59d1-847">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-847">10001</span></span></td>
<td><span data-ttu-id="b59d1-848">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-848">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-849">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-849">Variable cost</span></span></td>
<td><span data-ttu-id="b59d1-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="b59d1-850">5,297.69</span></span></td>
<td><span data-ttu-id="b59d1-851">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-852">CC004</span><span class="sxs-lookup"><span data-stu-id="b59d1-852">CC004</span></span></td>
<td><span data-ttu-id="b59d1-853">Paketleme</span><span class="sxs-lookup"><span data-stu-id="b59d1-853">Packaging</span></span></td>
<td><span data-ttu-id="b59d1-854">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-854">10001</span></span></td>
<td><span data-ttu-id="b59d1-855">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-855">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-856">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-856">Variable cost</span></span></td>
<td><span data-ttu-id="b59d1-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="b59d1-857">2,852.60</span></span></td>
<td><span data-ttu-id="b59d1-858">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-859">CC003</span><span class="sxs-lookup"><span data-stu-id="b59d1-859">CC003</span></span></td>
<td><span data-ttu-id="b59d1-860">Montaj</span><span class="sxs-lookup"><span data-stu-id="b59d1-860">Assembly</span></span></td>
<td><span data-ttu-id="b59d1-861">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-861">10001</span></span></td>
<td><span data-ttu-id="b59d1-862">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-862">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-863">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-863">Fixed cost</span></span></td>
<td><span data-ttu-id="b59d1-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="b59d1-864">-713.75</span></span></td>
<td><span data-ttu-id="b59d1-865">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-866">Prod 1</span></span></td>
<td><span data-ttu-id="b59d1-867">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-867">Product 1</span></span></td>
<td><span data-ttu-id="b59d1-868">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-868">10001</span></span></td>
<td><span data-ttu-id="b59d1-869">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-869">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-870">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-870">Fixed cost</span></span></td>
<td><span data-ttu-id="b59d1-871">535.31</span><span class="sxs-lookup"><span data-stu-id="b59d1-871">535.31</span></span></td>
<td><span data-ttu-id="b59d1-872">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b59d1-873">Prod 2</span></span></td>
<td><span data-ttu-id="b59d1-874">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="b59d1-874">Product 2</span></span></td>
<td><span data-ttu-id="b59d1-875">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-875">10001</span></span></td>
<td><span data-ttu-id="b59d1-876">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-876">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-877">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-877">Fixed cost</span></span></td>
<td><span data-ttu-id="b59d1-878">178.44</span><span class="sxs-lookup"><span data-stu-id="b59d1-878">178.44</span></span></td>
<td><span data-ttu-id="b59d1-879">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-880">CC003</span><span class="sxs-lookup"><span data-stu-id="b59d1-880">CC003</span></span></td>
<td><span data-ttu-id="b59d1-881">Montaj</span><span class="sxs-lookup"><span data-stu-id="b59d1-881">Assembly</span></span></td>
<td><span data-ttu-id="b59d1-882">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-882">10001</span></span></td>
<td><span data-ttu-id="b59d1-883">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-883">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-884">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-884">Variable cost</span></span></td>
<td><span data-ttu-id="b59d1-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="b59d1-885">-5,982.83</span></span></td>
<td><span data-ttu-id="b59d1-886">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-887">Prod 1</span></span></td>
<td><span data-ttu-id="b59d1-888">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-888">Product 1</span></span></td>
<td><span data-ttu-id="b59d1-889">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-889">10001</span></span></td>
<td><span data-ttu-id="b59d1-890">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-890">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-891">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-891">Variable cost</span></span></td>
<td><span data-ttu-id="b59d1-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="b59d1-892">4,487.12</span></span></td>
<td><span data-ttu-id="b59d1-893">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b59d1-894">Prod 2</span></span></td>
<td><span data-ttu-id="b59d1-895">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="b59d1-895">Product 2</span></span></td>
<td><span data-ttu-id="b59d1-896">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-896">10001</span></span></td>
<td><span data-ttu-id="b59d1-897">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-897">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-898">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-898">Variable cost</span></span></td>
<td><span data-ttu-id="b59d1-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="b59d1-899">1,495.71</span></span></td>
<td><span data-ttu-id="b59d1-900">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-901">CC003</span><span class="sxs-lookup"><span data-stu-id="b59d1-901">CC003</span></span></td>
<td><span data-ttu-id="b59d1-902">Montaj</span><span class="sxs-lookup"><span data-stu-id="b59d1-902">Assembly</span></span></td>
<td><span data-ttu-id="b59d1-903">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-903">10001</span></span></td>
<td><span data-ttu-id="b59d1-904">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-904">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-905">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-905">Fixed cost</span></span></td>
<td><span data-ttu-id="b59d1-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="b59d1-906">-286.25</span></span></td>
<td><span data-ttu-id="b59d1-907">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-908">Prod 1</span></span></td>
<td><span data-ttu-id="b59d1-909">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-909">Product 1</span></span></td>
<td><span data-ttu-id="b59d1-910">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-910">10001</span></span></td>
<td><span data-ttu-id="b59d1-911">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-911">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-912">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-912">Fixed cost</span></span></td>
<td><span data-ttu-id="b59d1-913">241.05</span><span class="sxs-lookup"><span data-stu-id="b59d1-913">241.05</span></span></td>
<td><span data-ttu-id="b59d1-914">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b59d1-915">Prod 2</span></span></td>
<td><span data-ttu-id="b59d1-916">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="b59d1-916">Product 2</span></span></td>
<td><span data-ttu-id="b59d1-917">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-917">10001</span></span></td>
<td><span data-ttu-id="b59d1-918">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-918">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-919">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-919">Fixed cost</span></span></td>
<td><span data-ttu-id="b59d1-920">45.20</span><span class="sxs-lookup"><span data-stu-id="b59d1-920">45.20</span></span></td>
<td><span data-ttu-id="b59d1-921">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-922">CC003</span><span class="sxs-lookup"><span data-stu-id="b59d1-922">CC003</span></span></td>
<td><span data-ttu-id="b59d1-923">Montaj</span><span class="sxs-lookup"><span data-stu-id="b59d1-923">Assembly</span></span></td>
<td><span data-ttu-id="b59d1-924">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-924">10001</span></span></td>
<td><span data-ttu-id="b59d1-925">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-925">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-926">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-926">Variable cost</span></span></td>
<td><span data-ttu-id="b59d1-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="b59d1-927">-2,977.17</span></span></td>
<td><span data-ttu-id="b59d1-928">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-929">Prod 1</span></span></td>
<td><span data-ttu-id="b59d1-930">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-930">Product 1</span></span></td>
<td><span data-ttu-id="b59d1-931">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-931">10001</span></span></td>
<td><span data-ttu-id="b59d1-932">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-932">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-933">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-933">Variable cost</span></span></td>
<td><span data-ttu-id="b59d1-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="b59d1-934">2,507.09</span></span></td>
<td><span data-ttu-id="b59d1-935">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b59d1-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b59d1-936">Prod 2</span></span></td>
<td><span data-ttu-id="b59d1-937">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="b59d1-937">Product 2</span></span></td>
<td><span data-ttu-id="b59d1-938">10001</span><span class="sxs-lookup"><span data-stu-id="b59d1-938">10001</span></span></td>
<td><span data-ttu-id="b59d1-939">Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-939">Electricity</span></span></td>
<td><span data-ttu-id="b59d1-940">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-940">Variable cost</span></span></td>
<td><span data-ttu-id="b59d1-941">470.08</span><span class="sxs-lookup"><span data-stu-id="b59d1-941">470.08</span></span></td>
<td><span data-ttu-id="b59d1-942">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="b59d1-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="b59d1-943">Sonuç</span><span class="sxs-lookup"><span data-stu-id="b59d1-943">Conclusion</span></span>
<span data-ttu-id="b59d1-944">Mali muhasebede, Elektrik için 10.000,00 maliyet bir sözde maliyet merkezi kimliğine nakledilmiştir.</span><span class="sxs-lookup"><span data-stu-id="b59d1-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="b59d1-945">Bu nedenle, maliyet muhasebecileri bu maliyetin tahsis edilmesi gerektiğini bilirler.</span><span class="sxs-lookup"><span data-stu-id="b59d1-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="b59d1-946">Maliyet muhasebesinde, maliyetler kuruluş birimleri ve seviyeleri arasında, uygulanan kural ve ilkelere dayalı olarak akar.</span><span class="sxs-lookup"><span data-stu-id="b59d1-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="b59d1-947">Her maliyet, maliyetlerin tahsisatı için en iyi değerlendirmeyi sağlayan bir tahsisat tabanı ile ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="b59d1-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="b59d1-948">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="b59d1-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="b59d1-949">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="b59d1-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="b59d1-950">Toplam</span><span class="sxs-lookup"><span data-stu-id="b59d1-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="b59d1-951">CC099</span><span class="sxs-lookup"><span data-stu-id="b59d1-951">CC099</span></span></th>
<th><span data-ttu-id="b59d1-952">CC001</span><span class="sxs-lookup"><span data-stu-id="b59d1-952">CC001</span></span></th>
<th><span data-ttu-id="b59d1-953">CC002</span><span class="sxs-lookup"><span data-stu-id="b59d1-953">CC002</span></span></th>
<th><span data-ttu-id="b59d1-954">CC003</span><span class="sxs-lookup"><span data-stu-id="b59d1-954">CC003</span></span></th>
<th><span data-ttu-id="b59d1-955">CC004</span><span class="sxs-lookup"><span data-stu-id="b59d1-955">CC004</span></span></th>
<th><span data-ttu-id="b59d1-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-956">Proj 1</span></span></th>
<th><span data-ttu-id="b59d1-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="b59d1-957">Proj 2</span></span></th>
<th><span data-ttu-id="b59d1-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="b59d1-958">Prod 1</span></span></th>
<th><span data-ttu-id="b59d1-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="b59d1-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="b59d1-960">10001 Elektrik</span><span class="sxs-lookup"><span data-stu-id="b59d1-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b59d1-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="b59d1-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b59d1-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="b59d1-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b59d1-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="b59d1-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b59d1-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="b59d1-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="b59d1-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="b59d1-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b59d1-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="b59d1-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b59d1-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="b59d1-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b59d1-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="b59d1-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b59d1-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="b59d1-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="b59d1-970">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="b59d1-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b59d1-971">0,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="b59d1-972">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b59d1-973">0,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b59d1-974">0,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b59d1-975">0,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b59d1-976">0,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b59d1-977">0,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="b59d1-978">776.36</span><span class="sxs-lookup"><span data-stu-id="b59d1-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b59d1-979">223.64</span><span class="sxs-lookup"><span data-stu-id="b59d1-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b59d1-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="b59d1-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="b59d1-981">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="b59d1-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b59d1-982">000</span><span class="sxs-lookup"><span data-stu-id="b59d1-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b59d1-983">0,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b59d1-984">0,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b59d1-985">0,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b59d1-986">0,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b59d1-987">30.00</span><span class="sxs-lookup"><span data-stu-id="b59d1-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b59d1-988">10,00</span><span class="sxs-lookup"><span data-stu-id="b59d1-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b59d1-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="b59d1-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b59d1-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="b59d1-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b59d1-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="b59d1-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="b59d1-992">Bu konu, birincil maliyet öğesi, 10001 Elektrik'in maliyet nesneleri arasında nasıl aktığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b59d1-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="b59d1-993">Bu nedenle, bu genel gider maliyeti kuruluşun en düşük seviyesine tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="b59d1-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="b59d1-994">Başka bir deyişle, maliyet en alt düzeydeki maliyet nesnelerine aittir.</span><span class="sxs-lookup"><span data-stu-id="b59d1-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="b59d1-995">Maliyetin, maliyet nesneleri arasında görsel bir akışına ihtiyacınız varsa, maliyetin akışını görselleştirmek için maliyet toplamı ilke kurallarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b59d1-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="b59d1-996">Daha fazla bilgi için bkz. [Maliyet yuvarlama ilkesi ve genel gider hesaplaması](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="b59d1-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]