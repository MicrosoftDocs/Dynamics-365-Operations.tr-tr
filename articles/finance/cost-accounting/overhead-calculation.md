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
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: cc6ad48ef80aa01739129b59cc1133d0a1930f24
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759484"
---
# <a name="overhead-calculation"></a><span data-ttu-id="7a1ee-103">Genel gider hesaplaması</span><span class="sxs-lookup"><span data-stu-id="7a1ee-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a1ee-104">Bu konu, genel gider maliyetlerinin hesaplanması için tipik işlemleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="7a1ee-105">Terim tanımı</span><span class="sxs-lookup"><span data-stu-id="7a1ee-105">Term definition</span></span>
---------------

<span data-ttu-id="7a1ee-106">Genel gider maliyetleri bir işletmenin çalışması için normalde uygulanan, ancak doğrudan herhangi bir özel iş, faaliyet, ürün veya hizmete ilişkilendirilmemiş olan maliyetlerdir.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="7a1ee-107">Genel gider maliyetleri kar sağlama faaliyetlerinin oluşturulması için kritik destek sağlar.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="7a1ee-108">Aşağıda bazı genel gider örnekleri verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="7a1ee-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="7a1ee-109">Kira</span><span class="sxs-lookup"><span data-stu-id="7a1ee-109">Rent</span></span>
-   <span data-ttu-id="7a1ee-110">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-110">Electricity</span></span>
-   <span data-ttu-id="7a1ee-111">Yönetim maaşları</span><span class="sxs-lookup"><span data-stu-id="7a1ee-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="7a1ee-112">Genel gider hesaplaması genel bakış</span><span class="sxs-lookup"><span data-stu-id="7a1ee-112">Overhead calculation overview</span></span>
<span data-ttu-id="7a1ee-113">Genel gider hesaplama, maliyet muhasebesi ilkelerini doğru sırayla çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="7a1ee-114">Maliyet muhasebesi ilkeleri değiştiyse veya belirli hatalar algılandıysa, genel gider hesaplamasını aynı mali dönem için birden fazla kez yürütebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="7a1ee-115">Her genel gider hesaplaması depolanır ve önceki sürümlerdeki hesaplamaları kıyaslamanıza olanak sağlayan, benzersiz bir sürüm kimliğine sahip olur.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="7a1ee-116">Genel gider hesaplamasının oluşturduğu maliyet girişleri bir muhasebe tarihi alır.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="7a1ee-117">Bu muhasebe tarihi, hesaplamada kullanılan mali dönemin bitiş tarihiyle eşleşir.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="7a1ee-118">Benzersiz sürüm kimliği aşağıdaki öğelerden oluşur:</span><span class="sxs-lookup"><span data-stu-id="7a1ee-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="7a1ee-119">Sürüm türü</span><span class="sxs-lookup"><span data-stu-id="7a1ee-119">Version type</span></span>
-   <span data-ttu-id="7a1ee-120">Tarih ve saat</span><span class="sxs-lookup"><span data-stu-id="7a1ee-120">Date and time</span></span>
-   <span data-ttu-id="7a1ee-121">Maliyet muhasebesi defteri</span><span class="sxs-lookup"><span data-stu-id="7a1ee-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="7a1ee-122">Mali yıl</span><span class="sxs-lookup"><span data-stu-id="7a1ee-122">Fiscal year</span></span>
-   <span data-ttu-id="7a1ee-123">Mali dönem</span><span class="sxs-lookup"><span data-stu-id="7a1ee-123">Fiscal period</span></span>

<span data-ttu-id="7a1ee-124">Genel gider hesaplama, sürümden bağımsız olarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="7a1ee-125">Bu nedenle, Gerçek sürümden önce Bütçe sürümünü hesaplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="7a1ee-126">Genel gider hesaplama dört adımdan oluşur, aşağıdaki çizimde gösterildiği gibi.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="7a1ee-127">Her adımda, günlük girişleri olan bir günlük başlığı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="7a1ee-128">Bu günlük başlığı, her hesaplama adımı için giriş verilerini tutar.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="7a1ee-129">İlkeler ve kurallar her günlük satırına uygulanır ve maliyet girişleri çıkış olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="7a1ee-130">Bu nedenle, her zaman tam izlenebilirliğe sahip olursunuz.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="7a1ee-131">[![Genel gider hesaplaması](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="7a1ee-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="7a1ee-132">Elektrik genel gideri maliyetini hesapla ve tahsis et</span><span class="sxs-lookup"><span data-stu-id="7a1ee-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="7a1ee-133">Mali muhasebede, elektrik gibi bazı maliyetler peşin ödeme olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="7a1ee-134">Bu nedenle, Maliyet muhasebesi için ayrıntılı yönetim bilgiler sağlanmaz.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="7a1ee-135">Maliyet muhasebesinde doğru yönetimsel bilgileri tüm yönetim birim ve düzeylerinde sağlamak için, maliyetlerin kuruluş birimleri arasında akması gerekir.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="7a1ee-136">Bu akış, tüketimin doğru bir kaydına ya da adil bir değerlendirmeye dayanıyor olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="7a1ee-137">Genel muhasebede, bir elektrik maliyeti aşağıdaki tabloda gösterildiği gibi deftere nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7a1ee-138">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7a1ee-139">Maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="7a1ee-140">Ana hesap</span><span class="sxs-lookup"><span data-stu-id="7a1ee-140">Main account</span></span></th>
<th><span data-ttu-id="7a1ee-141">Muhasebe para birimi cinsinden tutar</span><span class="sxs-lookup"><span data-stu-id="7a1ee-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a1ee-142">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="7a1ee-143">CC099</span><span class="sxs-lookup"><span data-stu-id="7a1ee-143">CC099</span></span></td>
<td><span data-ttu-id="7a1ee-144">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-144">Default cost center</span></span></td>
<td><span data-ttu-id="7a1ee-145">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-145">10001</span></span></td>
<td><span data-ttu-id="7a1ee-146">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-146">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="7a1ee-148">Adım 1: Maliyet davranışı hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="7a1ee-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="7a1ee-149">Varsayılan olarak, maliyeti girişleri kaynak veriden içeri alındığında, Maliyet muhasebesinde **Sınıflandırılmamış** maliyet davranışı sınıflandırmasını alırlar.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="7a1ee-150">Maliyet davranışı ilke kuralları ekleyerek, maliyet girişlerini **Sabit maliyet** veya **Değişken maliyet** olarak yeniden sınıflandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="7a1ee-151">Maliyet davranış kuralını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="7a1ee-151">Define the cost behavior rule</span></span>

<span data-ttu-id="7a1ee-152">Bazı durumlarda, sabit bir ücret maliyet parçasıdır ve kalan maliyet, tüketime dayanır.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="7a1ee-153">Elektrik faturaları genellikle bu tanıma uyar.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="7a1ee-154">Belirli bir sabit ücret ödedikten sonra, kilovat saatlik (Kwh) tüketim başına ödeme yaparsınız.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="7a1ee-155">Örneğin, sabit maliyet masrafı 1.000,00 ise, maliyet davranışı kural nasıl tanımlanır:</span><span class="sxs-lookup"><span data-stu-id="7a1ee-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="7a1ee-156">Sabit tutar 1.000,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="7a1ee-157">0 &lt;= 1.000,00 = Sabit</span><span class="sxs-lookup"><span data-stu-id="7a1ee-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="7a1ee-158">1000,01 &lt; N = Değişken</span><span class="sxs-lookup"><span data-stu-id="7a1ee-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="7a1ee-159">Günlük</span><span class="sxs-lookup"><span data-stu-id="7a1ee-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7a1ee-160">Günlük</span><span class="sxs-lookup"><span data-stu-id="7a1ee-160">Journal</span></span></th>
<th><span data-ttu-id="7a1ee-161">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="7a1ee-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="7a1ee-162">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="7a1ee-163">Sürüm</span><span class="sxs-lookup"><span data-stu-id="7a1ee-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a1ee-164">00001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-164">00001</span></span></td>
<td><span data-ttu-id="7a1ee-165">Maliyet davranışı hesaplama günlüğü</span><span class="sxs-lookup"><span data-stu-id="7a1ee-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="7a1ee-166">Mali</span><span class="sxs-lookup"><span data-stu-id="7a1ee-166">Fiscal</span></span></td>
<td><span data-ttu-id="7a1ee-167">2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-167">2017</span></span></td>
<td><span data-ttu-id="7a1ee-168">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-168">Period 1</span></span></td>
<td><span data-ttu-id="7a1ee-169">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="7a1ee-170">Günlük girişleri (Maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="7a1ee-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7a1ee-171">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7a1ee-172">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7a1ee-173">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-173">Cost element</span></span></th>
<th><span data-ttu-id="7a1ee-174">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="7a1ee-174">Cost behavior</span></span></th>
<th><span data-ttu-id="7a1ee-175">Tutar</span><span class="sxs-lookup"><span data-stu-id="7a1ee-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a1ee-176">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="7a1ee-177">CC099</span><span class="sxs-lookup"><span data-stu-id="7a1ee-177">CC099</span></span></td>
<td><span data-ttu-id="7a1ee-178">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-178">Default cost center</span></span></td>
<td><span data-ttu-id="7a1ee-179">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-179">10001</span></span></td>
<td><span data-ttu-id="7a1ee-180">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-180">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-181">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="7a1ee-181">Unclassified</span></span></td>
<td><span data-ttu-id="7a1ee-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="7a1ee-183">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="7a1ee-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a1ee-184">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7a1ee-185">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-185">Cost element</span></span></th>
<th><span data-ttu-id="7a1ee-186">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="7a1ee-186">Cost behavior</span></span></th>
<th><span data-ttu-id="7a1ee-187">Tutar</span><span class="sxs-lookup"><span data-stu-id="7a1ee-187">Amount</span></span></th>
<th><span data-ttu-id="7a1ee-188">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a1ee-189">CC099</span><span class="sxs-lookup"><span data-stu-id="7a1ee-189">CC099</span></span></td>
<td><span data-ttu-id="7a1ee-190">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-190">Default cost center</span></span></td>
<td><span data-ttu-id="7a1ee-191">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-191">10001</span></span></td>
<td><span data-ttu-id="7a1ee-192">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-192">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-193">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="7a1ee-193">Unclassified</span></span></td>
<td><span data-ttu-id="7a1ee-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-194">10,000.00</span></span></td>
<td><span data-ttu-id="7a1ee-195">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-196">CC099</span><span class="sxs-lookup"><span data-stu-id="7a1ee-196">CC099</span></span></td>
<td><span data-ttu-id="7a1ee-197">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-197">Default cost center</span></span></td>
<td><span data-ttu-id="7a1ee-198">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-198">10001</span></span></td>
<td><span data-ttu-id="7a1ee-199">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-199">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-200">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="7a1ee-200">Unclassified</span></span></td>
<td><span data-ttu-id="7a1ee-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-201">-10,000.00</span></span></td>
<td><span data-ttu-id="7a1ee-202">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-203">CC099</span><span class="sxs-lookup"><span data-stu-id="7a1ee-203">CC099</span></span></td>
<td><span data-ttu-id="7a1ee-204">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-204">Default cost center</span></span></td>
<td><span data-ttu-id="7a1ee-205">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-205">10001</span></span></td>
<td><span data-ttu-id="7a1ee-206">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-206">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-207">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-207">Fixed cost</span></span></td>
<td><span data-ttu-id="7a1ee-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-208">1,000.00</span></span></td>
<td><span data-ttu-id="7a1ee-209">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-210">CC099</span><span class="sxs-lookup"><span data-stu-id="7a1ee-210">CC099</span></span></td>
<td><span data-ttu-id="7a1ee-211">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-211">Default cost center</span></span></td>
<td><span data-ttu-id="7a1ee-212">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-212">10001</span></span></td>
<td><span data-ttu-id="7a1ee-213">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-213">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-214">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-214">Variable cost</span></span></td>
<td><span data-ttu-id="7a1ee-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-215">9,000.00</span></span></td>
<td><span data-ttu-id="7a1ee-216">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7a1ee-217">Daha fazla bilgi için bkz. [Maliyet davranışı ilkesi oluşturma ve bir maliyet kontrol birimine atama](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="7a1ee-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="7a1ee-218">Adım 2: Maliyet dağıtımı hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="7a1ee-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="7a1ee-219">Maliyet dağıtımı, bir nesneden bir veya daha fazlasına ilgili tahsisat tabanı uygulayarak maliyeti yeniden dağıtmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="7a1ee-220">Maliyet dağıtımı ve maliyet tahsisatı, maliyet dağıtımının her zaman orijinal maliyetin birincil maliyet öğesinde bulunmasıyla farklılık gösterir.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="7a1ee-221">Maliyet dağıtım kuralını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="7a1ee-221">Define the cost distribution rule</span></span>

<span data-ttu-id="7a1ee-222">Mali muhasebede, elektrik maliyetleri çoğu zaman peşin ödeme olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="7a1ee-223">Maliyet muhasebesinde ise bu yöntem yeterince ayrıntılı değildir.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="7a1ee-224">Değişken maliyet, maliyet nesnelerine tek tek, adil bir temele dayanarak dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="7a1ee-225">En mantıklı tahsisat, elektrik kullanımını (Kwh) temel alarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="7a1ee-226">Elektrik adına sahip, istatistiksel bir boyut üyesi oluşturulur ve elektrik tüketimi kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="7a1ee-227">Varsayıla olarak, tüm istatistiksel boyut üyeleri tahsisat tabanları olarak kullanılabilir hale gelir.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a1ee-228">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-228">Cost object</span></span></th>
<th><span data-ttu-id="7a1ee-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="7a1ee-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a1ee-230">CC001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-230">CC001</span></span></td>
<td><span data-ttu-id="7a1ee-231">İK</span><span class="sxs-lookup"><span data-stu-id="7a1ee-231">HR</span></span></td>
<td><span data-ttu-id="7a1ee-232">1.000</span><span class="sxs-lookup"><span data-stu-id="7a1ee-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-233">CC002</span><span class="sxs-lookup"><span data-stu-id="7a1ee-233">CC002</span></span></td>
<td><span data-ttu-id="7a1ee-234">Finans</span><span class="sxs-lookup"><span data-stu-id="7a1ee-234">Finance</span></span></td>
<td><span data-ttu-id="7a1ee-235">6,000</span><span class="sxs-lookup"><span data-stu-id="7a1ee-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-236">CC003</span><span class="sxs-lookup"><span data-stu-id="7a1ee-236">CC003</span></span></td>
<td><span data-ttu-id="7a1ee-237">Montaj</span><span class="sxs-lookup"><span data-stu-id="7a1ee-237">Assembly</span></span></td>
<td><span data-ttu-id="7a1ee-238">0</span><span class="sxs-lookup"><span data-stu-id="7a1ee-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7a1ee-239">Aşağıdaki tablo, elektrik tüketiminin değişken maliyetler için bir tahsisat tabanlı olarak uygulandığındaki sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a1ee-240">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-240">Cost object</span></span></th>
<th><span data-ttu-id="7a1ee-241">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="7a1ee-241">Magnitude</span></span></th>
<th><span data-ttu-id="7a1ee-242">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="7a1ee-242">Allocation factor</span></span></th>
<th><span data-ttu-id="7a1ee-243">Tutar</span><span class="sxs-lookup"><span data-stu-id="7a1ee-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a1ee-244">CC001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-244">CC001</span></span></td>
<td><span data-ttu-id="7a1ee-245">İK</span><span class="sxs-lookup"><span data-stu-id="7a1ee-245">HR</span></span></td>
<td><span data-ttu-id="7a1ee-246">1.000</span><span class="sxs-lookup"><span data-stu-id="7a1ee-246">1,000</span></span></td>
<td><span data-ttu-id="7a1ee-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="7a1ee-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="7a1ee-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-249">CC002</span><span class="sxs-lookup"><span data-stu-id="7a1ee-249">CC002</span></span></td>
<td><span data-ttu-id="7a1ee-250">Finans</span><span class="sxs-lookup"><span data-stu-id="7a1ee-250">Finance</span></span></td>
<td><span data-ttu-id="7a1ee-251">6,000</span><span class="sxs-lookup"><span data-stu-id="7a1ee-251">6,000</span></span></td>
<td><span data-ttu-id="7a1ee-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="7a1ee-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="7a1ee-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-254">CC003</span><span class="sxs-lookup"><span data-stu-id="7a1ee-254">CC003</span></span></td>
<td><span data-ttu-id="7a1ee-255">Montaj</span><span class="sxs-lookup"><span data-stu-id="7a1ee-255">Assembly</span></span></td>
<td><span data-ttu-id="7a1ee-256">0</span><span class="sxs-lookup"><span data-stu-id="7a1ee-256">0</span></span></td>
<td><span data-ttu-id="7a1ee-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="7a1ee-258">0,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7a1ee-259">Sabit maliyet, elektrik tüketmiş olan tekil maliyet nesnelerine eşit miktarda dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="7a1ee-260">Bu sonuca, Elektrik istatistiksel boyut öğesini bir formül tahsisat tabanında kullanarak ulaşabilirsiniz: (Elektrik &gt; 0,00) Aşağıdaki tablo, elektrik tüketimi değişken maliyetler için bir tahsisat tabanı olarak kullanıldığında ortaya çıkan sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a1ee-261">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-261">Cost object</span></span></th>
<th><span data-ttu-id="7a1ee-262">Formül</span><span class="sxs-lookup"><span data-stu-id="7a1ee-262">Formula</span></span></th>
<th><span data-ttu-id="7a1ee-263">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="7a1ee-263">Magnitude</span></span></th>
<th><span data-ttu-id="7a1ee-264">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="7a1ee-264">Allocation factor</span></span></th>
<th><span data-ttu-id="7a1ee-265">Tutar</span><span class="sxs-lookup"><span data-stu-id="7a1ee-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a1ee-266">CC001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-266">CC001</span></span></td>
<td><span data-ttu-id="7a1ee-267">İK</span><span class="sxs-lookup"><span data-stu-id="7a1ee-267">HR</span></span></td>
<td><span data-ttu-id="7a1ee-268">(1,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="7a1ee-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="7a1ee-269">1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-269">1</span></span></td>
<td><span data-ttu-id="7a1ee-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="7a1ee-271">500.00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-272">CC002</span><span class="sxs-lookup"><span data-stu-id="7a1ee-272">CC002</span></span></td>
<td><span data-ttu-id="7a1ee-273">Finans</span><span class="sxs-lookup"><span data-stu-id="7a1ee-273">Finance</span></span></td>
<td><span data-ttu-id="7a1ee-274">(6,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="7a1ee-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="7a1ee-275">1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-275">1</span></span></td>
<td><span data-ttu-id="7a1ee-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="7a1ee-277">500.00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-278">CC003</span><span class="sxs-lookup"><span data-stu-id="7a1ee-278">CC003</span></span></td>
<td><span data-ttu-id="7a1ee-279">Montaj</span><span class="sxs-lookup"><span data-stu-id="7a1ee-279">Assembly</span></span></td>
<td><span data-ttu-id="7a1ee-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="7a1ee-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="7a1ee-281">0</span><span class="sxs-lookup"><span data-stu-id="7a1ee-281">0</span></span></td>
<td><span data-ttu-id="7a1ee-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="7a1ee-283">0,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="7a1ee-284">Günlük</span><span class="sxs-lookup"><span data-stu-id="7a1ee-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7a1ee-285">Günlük</span><span class="sxs-lookup"><span data-stu-id="7a1ee-285">Journal</span></span></th>
<th><span data-ttu-id="7a1ee-286">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="7a1ee-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="7a1ee-287">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="7a1ee-288">Sürüm</span><span class="sxs-lookup"><span data-stu-id="7a1ee-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a1ee-289">00002</span><span class="sxs-lookup"><span data-stu-id="7a1ee-289">00002</span></span></td>
<td><span data-ttu-id="7a1ee-290">Maliyet dağıtımı hesaplama günlüğü</span><span class="sxs-lookup"><span data-stu-id="7a1ee-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="7a1ee-291">Mali</span><span class="sxs-lookup"><span data-stu-id="7a1ee-291">Fiscal</span></span></td>
<td><span data-ttu-id="7a1ee-292">2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-292">2017</span></span></td>
<td><span data-ttu-id="7a1ee-293">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-293">Period 1</span></span></td>
<td><span data-ttu-id="7a1ee-294">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="7a1ee-295">Günlük girişleri (Maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="7a1ee-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7a1ee-296">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7a1ee-297">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7a1ee-298">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-298">Cost element</span></span></th>
<th><span data-ttu-id="7a1ee-299">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="7a1ee-299">Cost behavior</span></span></th>
<th><span data-ttu-id="7a1ee-300">Tutar</span><span class="sxs-lookup"><span data-stu-id="7a1ee-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a1ee-301">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="7a1ee-302">CC099</span><span class="sxs-lookup"><span data-stu-id="7a1ee-302">CC099</span></span></td>
<td><span data-ttu-id="7a1ee-303">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-303">Default cost center</span></span></td>
<td><span data-ttu-id="7a1ee-304">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-304">10001</span></span></td>
<td><span data-ttu-id="7a1ee-305">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-305">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-306">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-306">Fixed cost</span></span></td>
<td><span data-ttu-id="7a1ee-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-308">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="7a1ee-309">CC099</span><span class="sxs-lookup"><span data-stu-id="7a1ee-309">CC099</span></span></td>
<td><span data-ttu-id="7a1ee-310">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-310">Default cost center</span></span></td>
<td><span data-ttu-id="7a1ee-311">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-311">10001</span></span></td>
<td><span data-ttu-id="7a1ee-312">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-312">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-313">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-313">Variable cost</span></span></td>
<td><span data-ttu-id="7a1ee-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="7a1ee-315">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="7a1ee-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a1ee-316">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7a1ee-317">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-317">Cost element</span></span></th>
<th><span data-ttu-id="7a1ee-318">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="7a1ee-318">Cost behavior</span></span></th>
<th><span data-ttu-id="7a1ee-319">Tutar</span><span class="sxs-lookup"><span data-stu-id="7a1ee-319">Amount</span></span></th>
<th><span data-ttu-id="7a1ee-320">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a1ee-321">CC099</span><span class="sxs-lookup"><span data-stu-id="7a1ee-321">CC099</span></span></td>
<td><span data-ttu-id="7a1ee-322">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-322">Default cost center</span></span></td>
<td><span data-ttu-id="7a1ee-323">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-323">10001</span></span></td>
<td><span data-ttu-id="7a1ee-324">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-324">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-325">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-325">Fixed cost</span></span></td>
<td><span data-ttu-id="7a1ee-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-326">-1,000.00</span></span></td>
<td><span data-ttu-id="7a1ee-327">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-328">CC001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-328">CC001</span></span></td>
<td><span data-ttu-id="7a1ee-329">İK</span><span class="sxs-lookup"><span data-stu-id="7a1ee-329">HR</span></span></td>
<td><span data-ttu-id="7a1ee-330">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-330">10001</span></span></td>
<td><span data-ttu-id="7a1ee-331">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-331">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-332">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-332">Fixed cost</span></span></td>
<td><span data-ttu-id="7a1ee-333">500.00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-333">500.00</span></span></td>
<td><span data-ttu-id="7a1ee-334">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-335">CC002</span><span class="sxs-lookup"><span data-stu-id="7a1ee-335">CC002</span></span></td>
<td><span data-ttu-id="7a1ee-336">Finans</span><span class="sxs-lookup"><span data-stu-id="7a1ee-336">Finance</span></span></td>
<td><span data-ttu-id="7a1ee-337">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-337">10001</span></span></td>
<td><span data-ttu-id="7a1ee-338">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-338">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-339">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-339">Fixed cost</span></span></td>
<td><span data-ttu-id="7a1ee-340">500.00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-340">500.00</span></span></td>
<td><span data-ttu-id="7a1ee-341">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-342">CC099</span><span class="sxs-lookup"><span data-stu-id="7a1ee-342">CC099</span></span></td>
<td><span data-ttu-id="7a1ee-343">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-343">Default cost center</span></span></td>
<td><span data-ttu-id="7a1ee-344">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-344">10001</span></span></td>
<td><span data-ttu-id="7a1ee-345">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-345">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-346">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-346">Variable cost</span></span></td>
<td><span data-ttu-id="7a1ee-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-347">-9,000.00</span></span></td>
<td><span data-ttu-id="7a1ee-348">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-349">CC001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-349">CC001</span></span></td>
<td><span data-ttu-id="7a1ee-350">İK</span><span class="sxs-lookup"><span data-stu-id="7a1ee-350">HR</span></span></td>
<td><span data-ttu-id="7a1ee-351">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-351">10001</span></span></td>
<td><span data-ttu-id="7a1ee-352">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-352">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-353">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-353">Variable cost</span></span></td>
<td><span data-ttu-id="7a1ee-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="7a1ee-354">1,285.71</span></span></td>
<td><span data-ttu-id="7a1ee-355">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-356">CC002</span><span class="sxs-lookup"><span data-stu-id="7a1ee-356">CC002</span></span></td>
<td><span data-ttu-id="7a1ee-357">Finans</span><span class="sxs-lookup"><span data-stu-id="7a1ee-357">Finance</span></span></td>
<td><span data-ttu-id="7a1ee-358">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-358">10001</span></span></td>
<td><span data-ttu-id="7a1ee-359">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-359">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-360">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-360">Variable cost</span></span></td>
<td><span data-ttu-id="7a1ee-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="7a1ee-361">7,714.29</span></span></td>
<td><span data-ttu-id="7a1ee-362">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7a1ee-363">Daha fazla bilgi için bkz. [Maliyet dağıtımı ilkesi oluşturma ve bir maliyet kontrol birimine atama](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="7a1ee-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="7a1ee-364">Adım 3: Genel gider oranı hesaplama işlemi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="7a1ee-365">Genel gider oranı, bir veya birden fazla belirli maliyet nesnesine masraf yüklemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="7a1ee-366">Masraf, önceden belirlenmiş maliyet oranına ve tahsisat tabanından hesaplanan büyüklüğe dayanır.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="7a1ee-367">Genel gider oranını tanımlama</span><span class="sxs-lookup"><span data-stu-id="7a1ee-367">Define the overhead rate</span></span>

<span data-ttu-id="7a1ee-368">Maliyet nesnesi CC001 HR, bir dizi dahili projeye katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="7a1ee-369">HR projeleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a1ee-370">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-370">Cost object</span></span></th>
<th><span data-ttu-id="7a1ee-371">Saatler</span><span class="sxs-lookup"><span data-stu-id="7a1ee-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a1ee-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-372">Proj 1</span></span></td>
<td><span data-ttu-id="7a1ee-373">Proje 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-373">Project 1</span></span></td>
<td><span data-ttu-id="7a1ee-374">3</span><span class="sxs-lookup"><span data-stu-id="7a1ee-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="7a1ee-375">Proj 2</span></span></td>
<td><span data-ttu-id="7a1ee-376">Proje 2</span><span class="sxs-lookup"><span data-stu-id="7a1ee-376">Project 2</span></span></td>
<td><span data-ttu-id="7a1ee-377">1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7a1ee-378">Maliyet projeleri dağıtımı için bir önceden belirlenmiş maliyet oranı tanımlandı.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a1ee-379">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-379">Cost object</span></span></th>
<th><span data-ttu-id="7a1ee-380">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-380">Cost element</span></span></th>
<th><span data-ttu-id="7a1ee-381">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="7a1ee-381">Cost behavior</span></span></th>
<th><span data-ttu-id="7a1ee-382">Birimler</span><span class="sxs-lookup"><span data-stu-id="7a1ee-382">Units</span></span></th>
<th><span data-ttu-id="7a1ee-383">Ücret</span><span class="sxs-lookup"><span data-stu-id="7a1ee-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a1ee-384">CC001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-384">CC001</span></span></td>
<td><span data-ttu-id="7a1ee-385">İK</span><span class="sxs-lookup"><span data-stu-id="7a1ee-385">HR</span></span></td>
<td><span data-ttu-id="7a1ee-386">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-386">10001</span></span></td>
<td><span data-ttu-id="7a1ee-387">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-387">Variable cost</span></span></td>
<td><span data-ttu-id="7a1ee-388">1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-388">1</span></span></td>
<td><span data-ttu-id="7a1ee-389">10</span><span class="sxs-lookup"><span data-stu-id="7a1ee-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7a1ee-390">Aşağıdaki tablo, HR projeleri bir tahsisat tabanı olarak uygulandığındaki sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a1ee-391">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-391">Cost object</span></span></th>
<th><span data-ttu-id="7a1ee-392">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="7a1ee-392">Magnitude</span></span></th>
<th><span data-ttu-id="7a1ee-393">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-393">Cost element</span></span></th>
<th><span data-ttu-id="7a1ee-394">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="7a1ee-394">Allocation factor</span></span></th>
<th><span data-ttu-id="7a1ee-395">Tutar</span><span class="sxs-lookup"><span data-stu-id="7a1ee-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a1ee-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-396">Proj 1</span></span></td>
<td><span data-ttu-id="7a1ee-397">Proje 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-397">Project 1</span></span></td>
<td><span data-ttu-id="7a1ee-398">3</span><span class="sxs-lookup"><span data-stu-id="7a1ee-398">3</span></span></td>
<td><span data-ttu-id="7a1ee-399">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-399">10001</span></span></td>
<td><span data-ttu-id="7a1ee-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="7a1ee-401">30.00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="7a1ee-402">Proj 2</span></span></td>
<td><span data-ttu-id="7a1ee-403">Proje 2</span><span class="sxs-lookup"><span data-stu-id="7a1ee-403">Project 2</span></span></td>
<td><span data-ttu-id="7a1ee-404">1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-404">1</span></span></td>
<td><span data-ttu-id="7a1ee-405">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-405">10001</span></span></td>
<td><span data-ttu-id="7a1ee-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="7a1ee-407">10,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="7a1ee-408">Günlük</span><span class="sxs-lookup"><span data-stu-id="7a1ee-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7a1ee-409">Günlük</span><span class="sxs-lookup"><span data-stu-id="7a1ee-409">Journal</span></span></th>
<th><span data-ttu-id="7a1ee-410">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="7a1ee-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="7a1ee-411">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="7a1ee-412">Sürüm</span><span class="sxs-lookup"><span data-stu-id="7a1ee-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a1ee-413">00003</span><span class="sxs-lookup"><span data-stu-id="7a1ee-413">00003</span></span></td>
<td><span data-ttu-id="7a1ee-414">Genel gider oranı hesaplaması günlüğü</span><span class="sxs-lookup"><span data-stu-id="7a1ee-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="7a1ee-415">Mali</span><span class="sxs-lookup"><span data-stu-id="7a1ee-415">Fiscal</span></span></td>
<td><span data-ttu-id="7a1ee-416">2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-416">2017</span></span></td>
<td><span data-ttu-id="7a1ee-417">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-417">Period 1</span></span></td>
<td><span data-ttu-id="7a1ee-418">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="7a1ee-419">Günlük girişleri (Genel gider oranı hesaplaması için günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="7a1ee-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7a1ee-420">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7a1ee-421">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-421">Cost object</span></span></th>
<th><span data-ttu-id="7a1ee-422">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="7a1ee-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a1ee-423">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="7a1ee-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-424">Proj 1</span></span></td>
<td><span data-ttu-id="7a1ee-425">Dahili Proj 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="7a1ee-426">3,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-427">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="7a1ee-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="7a1ee-428">Proj 2</span></span></td>
<td><span data-ttu-id="7a1ee-429">Dahili Proj 2</span><span class="sxs-lookup"><span data-stu-id="7a1ee-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="7a1ee-430">1.00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="7a1ee-431">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="7a1ee-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a1ee-432">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7a1ee-433">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-433">Cost element</span></span></th>
<th><span data-ttu-id="7a1ee-434">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="7a1ee-434">Cost behavior</span></span></th>
<th><span data-ttu-id="7a1ee-435">Tutar</span><span class="sxs-lookup"><span data-stu-id="7a1ee-435">Amount</span></span></th>
<th><span data-ttu-id="7a1ee-436">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a1ee-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-437">CC0001</span></span></td>
<td><span data-ttu-id="7a1ee-438">İK</span><span class="sxs-lookup"><span data-stu-id="7a1ee-438">HR</span></span></td>
<td><span data-ttu-id="7a1ee-439">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-439">10001</span></span></td>
<td><span data-ttu-id="7a1ee-440">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-440">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-441">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-441">Variable cost</span></span></td>
<td><span data-ttu-id="7a1ee-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-442">-30.00</span></span></td>
<td><span data-ttu-id="7a1ee-443">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-444">Proj 1</span></span></td>
<td><span data-ttu-id="7a1ee-445">Dahili Proj 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="7a1ee-446">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-446">10001</span></span></td>
<td><span data-ttu-id="7a1ee-447">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-447">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-448">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-448">Variable cost</span></span></td>
<td><span data-ttu-id="7a1ee-449">30.00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-449">30.00</span></span></td>
<td><span data-ttu-id="7a1ee-450">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-451">CC001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-451">CC001</span></span></td>
<td><span data-ttu-id="7a1ee-452">İK</span><span class="sxs-lookup"><span data-stu-id="7a1ee-452">HR</span></span></td>
<td><span data-ttu-id="7a1ee-453">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-453">10001</span></span></td>
<td><span data-ttu-id="7a1ee-454">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-454">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-455">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-455">Variable cost</span></span></td>
<td><span data-ttu-id="7a1ee-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-456">-10.00</span></span></td>
<td><span data-ttu-id="7a1ee-457">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="7a1ee-458">Proj 2</span></span></td>
<td><span data-ttu-id="7a1ee-459">Dahili Proj 2</span><span class="sxs-lookup"><span data-stu-id="7a1ee-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="7a1ee-460">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-460">10001</span></span></td>
<td><span data-ttu-id="7a1ee-461">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-461">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-462">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-462">Variable cost</span></span></td>
<td><span data-ttu-id="7a1ee-463">10,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-463">10.00</span></span></td>
<td><span data-ttu-id="7a1ee-464">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7a1ee-465">Daha fazla bilgi için [Genel gider hesaplaması gerçekleştir](cost-rollup.md#perform-overhead-calculation) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="7a1ee-466">Adım 4: Maliyet tahsisat hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="7a1ee-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="7a1ee-467">Tahsisat, bir tahsisat tabanı kullanarak bir maliyet nesnesinin diğer maliyet nesnelerine bakiyesini tahsis eder.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="7a1ee-468">Finance karşılıklı tahsisat yöntemini desteklemektedir.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="7a1ee-469">Karşılıklı tahsisat yönteminde, yardımcı maliyet nesnelerinin değiştiği karşılıklı hizmetler tümüyle tanınır.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="7a1ee-470">Sistem, tahsisatların doğru gerçekleştireceği sırayı otomatik olarak belirler.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="7a1ee-471">Bir maliyet nesnesinin bakiyesi tek bir tahsisat tabanı tarafından tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="7a1ee-472">Yeni maliyet nesnesi boyutları arasındaki tahsisatlar ve onların üyeleri desteklenir.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="7a1ee-473">Tahsisatın sırası, maliyet kontrol birimi tarafından kontrol edilir.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="7a1ee-474">[![Karşılıklı yöntemi](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="7a1ee-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="7a1ee-475">Maliyet tahsisatını tanımla</span><span class="sxs-lookup"><span data-stu-id="7a1ee-475">Define the cost allocation</span></span>

<span data-ttu-id="7a1ee-476">Bir maliyetin akışını nasıl izleyeceğinize dair basit bir örnek aşağıda verilmiştir,</span><span class="sxs-lookup"><span data-stu-id="7a1ee-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="7a1ee-477">Maliyet nesnesi CC001 HR, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="7a1ee-478">HR hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a1ee-479">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-479">Cost object</span></span></th>
<th><span data-ttu-id="7a1ee-480">HR hizmetleri</span><span class="sxs-lookup"><span data-stu-id="7a1ee-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a1ee-481">CC002</span><span class="sxs-lookup"><span data-stu-id="7a1ee-481">CC002</span></span></td>
<td><span data-ttu-id="7a1ee-482">Finans</span><span class="sxs-lookup"><span data-stu-id="7a1ee-482">Finance</span></span></td>
<td><span data-ttu-id="7a1ee-483">35</span><span class="sxs-lookup"><span data-stu-id="7a1ee-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-484">CC003</span><span class="sxs-lookup"><span data-stu-id="7a1ee-484">CC003</span></span></td>
<td><span data-ttu-id="7a1ee-485">Montaj</span><span class="sxs-lookup"><span data-stu-id="7a1ee-485">Assembly</span></span></td>
<td><span data-ttu-id="7a1ee-486">55</span><span class="sxs-lookup"><span data-stu-id="7a1ee-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-487">CC004</span><span class="sxs-lookup"><span data-stu-id="7a1ee-487">CC004</span></span></td>
<td><span data-ttu-id="7a1ee-488">Paketleme</span><span class="sxs-lookup"><span data-stu-id="7a1ee-488">Packaging</span></span></td>
<td><span data-ttu-id="7a1ee-489">10</span><span class="sxs-lookup"><span data-stu-id="7a1ee-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7a1ee-490">Maliyet nesnesi CC002 Finans, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="7a1ee-491">Finans hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a1ee-492">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-492">Cost object</span></span></th>
<th><span data-ttu-id="7a1ee-493">Finans hizmetleri</span><span class="sxs-lookup"><span data-stu-id="7a1ee-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a1ee-494">CC003</span><span class="sxs-lookup"><span data-stu-id="7a1ee-494">CC003</span></span></td>
<td><span data-ttu-id="7a1ee-495">Montaj</span><span class="sxs-lookup"><span data-stu-id="7a1ee-495">Assembly</span></span></td>
<td><span data-ttu-id="7a1ee-496">65</span><span class="sxs-lookup"><span data-stu-id="7a1ee-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-497">CC004</span><span class="sxs-lookup"><span data-stu-id="7a1ee-497">CC004</span></span></td>
<td><span data-ttu-id="7a1ee-498">Paketleme</span><span class="sxs-lookup"><span data-stu-id="7a1ee-498">Packaging</span></span></td>
<td><span data-ttu-id="7a1ee-499">35</span><span class="sxs-lookup"><span data-stu-id="7a1ee-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7a1ee-500">Maliyet nesnesi CC003 Derleme, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="7a1ee-501">Derleme hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a1ee-502">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-502">Cost object</span></span></th>
<th><span data-ttu-id="7a1ee-503">Derleme Hizmetleri (saat)</span><span class="sxs-lookup"><span data-stu-id="7a1ee-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a1ee-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-504">Prod 1</span></span></td>
<td><span data-ttu-id="7a1ee-505">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-505">Product 1</span></span></td>
<td><span data-ttu-id="7a1ee-506">60</span><span class="sxs-lookup"><span data-stu-id="7a1ee-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7a1ee-507">Prod 2</span></span></td>
<td><span data-ttu-id="7a1ee-508">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="7a1ee-508">Product 2</span></span></td>
<td><span data-ttu-id="7a1ee-509">20</span><span class="sxs-lookup"><span data-stu-id="7a1ee-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7a1ee-510">Maliyet nesnesi CC004 Ambalajlama, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="7a1ee-511">Ambalajlama hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a1ee-512">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-512">Cost object</span></span></th>
<th><span data-ttu-id="7a1ee-513">Ambalajlama hizmetleri (saat)</span><span class="sxs-lookup"><span data-stu-id="7a1ee-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a1ee-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-514">Prod 1</span></span></td>
<td><span data-ttu-id="7a1ee-515">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-515">Product 1</span></span></td>
<td><span data-ttu-id="7a1ee-516">80</span><span class="sxs-lookup"><span data-stu-id="7a1ee-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7a1ee-517">Prod 2</span></span></td>
<td><span data-ttu-id="7a1ee-518">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="7a1ee-518">Product 2</span></span></td>
<td><span data-ttu-id="7a1ee-519">15</span><span class="sxs-lookup"><span data-stu-id="7a1ee-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="7a1ee-520">Bir ürünün tükettiği üretim saatleri gibi istatistiki ölçümler, doğrudan kaynak verilerinden alınabilir.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="7a1ee-521">Daha fazla bilgi için, [İstatistiksel ölçüm sağlayıcı şablonu](statistical-measure-provider-template.md#statistical-measure-provider-template) bakın.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="7a1ee-522">Aşağıdaki tablo, İK hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığında ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a1ee-523">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-523">Cost object</span></span></th>
<th><span data-ttu-id="7a1ee-524">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="7a1ee-524">Magnitude</span></span></th>
<th><span data-ttu-id="7a1ee-525">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="7a1ee-525">Allocation factor</span></span></th>
<th><span data-ttu-id="7a1ee-526">Tutar</span><span class="sxs-lookup"><span data-stu-id="7a1ee-526">Amount</span></span></th>
<th><span data-ttu-id="7a1ee-527">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="7a1ee-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a1ee-528">CC002</span><span class="sxs-lookup"><span data-stu-id="7a1ee-528">CC002</span></span></td>
<td><span data-ttu-id="7a1ee-529">Finans</span><span class="sxs-lookup"><span data-stu-id="7a1ee-529">Finance</span></span></td>
<td><span data-ttu-id="7a1ee-530">35</span><span class="sxs-lookup"><span data-stu-id="7a1ee-530">35</span></span></td>
<td><span data-ttu-id="7a1ee-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="7a1ee-532">175.00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-532">175.00</span></span></td>
<td><span data-ttu-id="7a1ee-533">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-534">CC003</span><span class="sxs-lookup"><span data-stu-id="7a1ee-534">CC003</span></span></td>
<td><span data-ttu-id="7a1ee-535">Montaj</span><span class="sxs-lookup"><span data-stu-id="7a1ee-535">Assembly</span></span></td>
<td><span data-ttu-id="7a1ee-536">55</span><span class="sxs-lookup"><span data-stu-id="7a1ee-536">55</span></span></td>
<td><span data-ttu-id="7a1ee-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="7a1ee-538">275.00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-538">275.00</span></span></td>
<td><span data-ttu-id="7a1ee-539">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-540">CC004</span><span class="sxs-lookup"><span data-stu-id="7a1ee-540">CC004</span></span></td>
<td><span data-ttu-id="7a1ee-541">Paketleme</span><span class="sxs-lookup"><span data-stu-id="7a1ee-541">Packaging</span></span></td>
<td><span data-ttu-id="7a1ee-542">10</span><span class="sxs-lookup"><span data-stu-id="7a1ee-542">10</span></span></td>
<td><span data-ttu-id="7a1ee-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="7a1ee-544">50,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-544">50.00</span></span></td>
<td><span data-ttu-id="7a1ee-545">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-546">CC002</span><span class="sxs-lookup"><span data-stu-id="7a1ee-546">CC002</span></span></td>
<td><span data-ttu-id="7a1ee-547">Finans</span><span class="sxs-lookup"><span data-stu-id="7a1ee-547">Finance</span></span></td>
<td><span data-ttu-id="7a1ee-548">35</span><span class="sxs-lookup"><span data-stu-id="7a1ee-548">35</span></span></td>
<td><span data-ttu-id="7a1ee-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="7a1ee-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="7a1ee-550">436.00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-550">436.00</span></span></td>
<td><span data-ttu-id="7a1ee-551">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-552">CC003</span><span class="sxs-lookup"><span data-stu-id="7a1ee-552">CC003</span></span></td>
<td><span data-ttu-id="7a1ee-553">Montaj</span><span class="sxs-lookup"><span data-stu-id="7a1ee-553">Assembly</span></span></td>
<td><span data-ttu-id="7a1ee-554">55</span><span class="sxs-lookup"><span data-stu-id="7a1ee-554">55</span></span></td>
<td><span data-ttu-id="7a1ee-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="7a1ee-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="7a1ee-556">685.14</span><span class="sxs-lookup"><span data-stu-id="7a1ee-556">685.14</span></span></td>
<td><span data-ttu-id="7a1ee-557">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-558">CC004</span><span class="sxs-lookup"><span data-stu-id="7a1ee-558">CC004</span></span></td>
<td><span data-ttu-id="7a1ee-559">Paketleme</span><span class="sxs-lookup"><span data-stu-id="7a1ee-559">Packaging</span></span></td>
<td><span data-ttu-id="7a1ee-560">10</span><span class="sxs-lookup"><span data-stu-id="7a1ee-560">10</span></span></td>
<td><span data-ttu-id="7a1ee-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="7a1ee-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="7a1ee-562">124.57</span><span class="sxs-lookup"><span data-stu-id="7a1ee-562">124.57</span></span></td>
<td><span data-ttu-id="7a1ee-563">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7a1ee-564">Aşağıdaki tablo, Finans hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a1ee-565">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-565">Cost object</span></span></th>
<th><span data-ttu-id="7a1ee-566">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="7a1ee-566">Magnitude</span></span></th>
<th><span data-ttu-id="7a1ee-567">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="7a1ee-567">Allocation factor</span></span></th>
<th><span data-ttu-id="7a1ee-568">Tutar</span><span class="sxs-lookup"><span data-stu-id="7a1ee-568">Amount</span></span></th>
<th><span data-ttu-id="7a1ee-569">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="7a1ee-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a1ee-570">CC003</span><span class="sxs-lookup"><span data-stu-id="7a1ee-570">CC003</span></span></td>
<td><span data-ttu-id="7a1ee-571">Montaj</span><span class="sxs-lookup"><span data-stu-id="7a1ee-571">Assembly</span></span></td>
<td><span data-ttu-id="7a1ee-572">65</span><span class="sxs-lookup"><span data-stu-id="7a1ee-572">65</span></span></td>
<td><span data-ttu-id="7a1ee-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="7a1ee-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="7a1ee-574">438.75</span><span class="sxs-lookup"><span data-stu-id="7a1ee-574">438.75</span></span></td>
<td><span data-ttu-id="7a1ee-575">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-576">CC004</span><span class="sxs-lookup"><span data-stu-id="7a1ee-576">CC004</span></span></td>
<td><span data-ttu-id="7a1ee-577">Paketleme</span><span class="sxs-lookup"><span data-stu-id="7a1ee-577">Packaging</span></span></td>
<td><span data-ttu-id="7a1ee-578">35</span><span class="sxs-lookup"><span data-stu-id="7a1ee-578">35</span></span></td>
<td><span data-ttu-id="7a1ee-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="7a1ee-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="7a1ee-580">236.25</span><span class="sxs-lookup"><span data-stu-id="7a1ee-580">236.25</span></span></td>
<td><span data-ttu-id="7a1ee-581">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-582">CC003</span><span class="sxs-lookup"><span data-stu-id="7a1ee-582">CC003</span></span></td>
<td><span data-ttu-id="7a1ee-583">Montaj</span><span class="sxs-lookup"><span data-stu-id="7a1ee-583">Assembly</span></span></td>
<td><span data-ttu-id="7a1ee-584">65</span><span class="sxs-lookup"><span data-stu-id="7a1ee-584">65</span></span></td>
<td><span data-ttu-id="7a1ee-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="7a1ee-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="7a1ee-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="7a1ee-586">5,297.69</span></span></td>
<td><span data-ttu-id="7a1ee-587">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-588">CC004</span><span class="sxs-lookup"><span data-stu-id="7a1ee-588">CC004</span></span></td>
<td><span data-ttu-id="7a1ee-589">Paketleme</span><span class="sxs-lookup"><span data-stu-id="7a1ee-589">Packaging</span></span></td>
<td><span data-ttu-id="7a1ee-590">35</span><span class="sxs-lookup"><span data-stu-id="7a1ee-590">35</span></span></td>
<td><span data-ttu-id="7a1ee-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="7a1ee-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="7a1ee-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="7a1ee-592">2,852.60</span></span></td>
<td><span data-ttu-id="7a1ee-593">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7a1ee-594">Aşağıdaki tablo, Derleme hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a1ee-595">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-595">Cost object</span></span></th>
<th><span data-ttu-id="7a1ee-596">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="7a1ee-596">Magnitude</span></span></th>
<th><span data-ttu-id="7a1ee-597">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="7a1ee-597">Allocation factor</span></span></th>
<th><span data-ttu-id="7a1ee-598">Tutar</span><span class="sxs-lookup"><span data-stu-id="7a1ee-598">Amount</span></span></th>
<th><span data-ttu-id="7a1ee-599">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="7a1ee-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a1ee-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-600">Prod 1</span></span></td>
<td><span data-ttu-id="7a1ee-601">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-601">Product 1</span></span></td>
<td><span data-ttu-id="7a1ee-602">60</span><span class="sxs-lookup"><span data-stu-id="7a1ee-602">60</span></span></td>
<td><span data-ttu-id="7a1ee-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="7a1ee-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="7a1ee-604">535.31</span><span class="sxs-lookup"><span data-stu-id="7a1ee-604">535.31</span></span></td>
<td><span data-ttu-id="7a1ee-605">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7a1ee-606">Prod 2</span></span></td>
<td><span data-ttu-id="7a1ee-607">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="7a1ee-607">Product 2</span></span></td>
<td><span data-ttu-id="7a1ee-608">20</span><span class="sxs-lookup"><span data-stu-id="7a1ee-608">20</span></span></td>
<td><span data-ttu-id="7a1ee-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="7a1ee-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="7a1ee-610">178.44</span><span class="sxs-lookup"><span data-stu-id="7a1ee-610">178.44</span></span></td>
<td><span data-ttu-id="7a1ee-611">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-612">Prod 1</span></span></td>
<td><span data-ttu-id="7a1ee-613">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-613">Product 1</span></span></td>
<td><span data-ttu-id="7a1ee-614">60</span><span class="sxs-lookup"><span data-stu-id="7a1ee-614">60</span></span></td>
<td><span data-ttu-id="7a1ee-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="7a1ee-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="7a1ee-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="7a1ee-616">4,487.12</span></span></td>
<td><span data-ttu-id="7a1ee-617">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7a1ee-618">Prod 2</span></span></td>
<td><span data-ttu-id="7a1ee-619">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="7a1ee-619">Product 2</span></span></td>
<td><span data-ttu-id="7a1ee-620">20</span><span class="sxs-lookup"><span data-stu-id="7a1ee-620">20</span></span></td>
<td><span data-ttu-id="7a1ee-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="7a1ee-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="7a1ee-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="7a1ee-622">1,495.71</span></span></td>
<td><span data-ttu-id="7a1ee-623">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7a1ee-624">Aşağıdaki tablo, Paketleme hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a1ee-625">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-625">Cost object</span></span></th>
<th><span data-ttu-id="7a1ee-626">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="7a1ee-626">Magnitude</span></span></th>
<th><span data-ttu-id="7a1ee-627">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="7a1ee-627">Allocation factor</span></span></th>
<th><span data-ttu-id="7a1ee-628">Tutar</span><span class="sxs-lookup"><span data-stu-id="7a1ee-628">Amount</span></span></th>
<th><span data-ttu-id="7a1ee-629">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="7a1ee-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a1ee-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-630">Prod 1</span></span></td>
<td><span data-ttu-id="7a1ee-631">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-631">Product 1</span></span></td>
<td><span data-ttu-id="7a1ee-632">80</span><span class="sxs-lookup"><span data-stu-id="7a1ee-632">80</span></span></td>
<td><span data-ttu-id="7a1ee-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="7a1ee-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="7a1ee-634">241.05</span><span class="sxs-lookup"><span data-stu-id="7a1ee-634">241.05</span></span></td>
<td><span data-ttu-id="7a1ee-635">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7a1ee-636">Prod 2</span></span></td>
<td><span data-ttu-id="7a1ee-637">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="7a1ee-637">Product 2</span></span></td>
<td><span data-ttu-id="7a1ee-638">15</span><span class="sxs-lookup"><span data-stu-id="7a1ee-638">15</span></span></td>
<td><span data-ttu-id="7a1ee-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="7a1ee-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="7a1ee-640">45.20</span><span class="sxs-lookup"><span data-stu-id="7a1ee-640">45.20</span></span></td>
<td><span data-ttu-id="7a1ee-641">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-642">Prod 1</span></span></td>
<td><span data-ttu-id="7a1ee-643">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-643">Product 1</span></span></td>
<td><span data-ttu-id="7a1ee-644">80</span><span class="sxs-lookup"><span data-stu-id="7a1ee-644">80</span></span></td>
<td><span data-ttu-id="7a1ee-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="7a1ee-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="7a1ee-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="7a1ee-646">2,507.09</span></span></td>
<td><span data-ttu-id="7a1ee-647">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7a1ee-648">Prod 2</span></span></td>
<td><span data-ttu-id="7a1ee-649">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="7a1ee-649">Product 2</span></span></td>
<td><span data-ttu-id="7a1ee-650">15</span><span class="sxs-lookup"><span data-stu-id="7a1ee-650">15</span></span></td>
<td><span data-ttu-id="7a1ee-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="7a1ee-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="7a1ee-652">470.08</span><span class="sxs-lookup"><span data-stu-id="7a1ee-652">470.08</span></span></td>
<td><span data-ttu-id="7a1ee-653">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="7a1ee-654">Günlük girişleri (maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="7a1ee-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7a1ee-655">Günlük</span><span class="sxs-lookup"><span data-stu-id="7a1ee-655">Journal</span></span></th>
<th><span data-ttu-id="7a1ee-656">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="7a1ee-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="7a1ee-657">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="7a1ee-658">Sürüm</span><span class="sxs-lookup"><span data-stu-id="7a1ee-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a1ee-659">00004</span><span class="sxs-lookup"><span data-stu-id="7a1ee-659">00004</span></span></td>
<td><span data-ttu-id="7a1ee-660">Maliyet tahsisatı günlüğü</span><span class="sxs-lookup"><span data-stu-id="7a1ee-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="7a1ee-661">Mali</span><span class="sxs-lookup"><span data-stu-id="7a1ee-661">Fiscal</span></span></td>
<td><span data-ttu-id="7a1ee-662">2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-662">2017</span></span></td>
<td><span data-ttu-id="7a1ee-663">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-663">Period 1</span></span></td>
<td><span data-ttu-id="7a1ee-664">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="7a1ee-665">Günlük satırları</span><span class="sxs-lookup"><span data-stu-id="7a1ee-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7a1ee-666">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7a1ee-667">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7a1ee-668">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-668">Cost element</span></span></th>
<th><span data-ttu-id="7a1ee-669">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="7a1ee-669">Cost behavior</span></span></th>
<th><span data-ttu-id="7a1ee-670">Tutar</span><span class="sxs-lookup"><span data-stu-id="7a1ee-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a1ee-671">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="7a1ee-672">CC001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-672">CC001</span></span></td>
<td><span data-ttu-id="7a1ee-673">İK</span><span class="sxs-lookup"><span data-stu-id="7a1ee-673">HR</span></span></td>
<td><span data-ttu-id="7a1ee-674">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-674">10001</span></span></td>
<td><span data-ttu-id="7a1ee-675">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-675">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-676">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-676">Fixed cost</span></span></td>
<td><span data-ttu-id="7a1ee-677">500.00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-678">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="7a1ee-679">CC001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-679">CC001</span></span></td>
<td><span data-ttu-id="7a1ee-680">İK</span><span class="sxs-lookup"><span data-stu-id="7a1ee-680">HR</span></span></td>
<td><span data-ttu-id="7a1ee-681">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-681">10001</span></span></td>
<td><span data-ttu-id="7a1ee-682">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-682">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-683">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-683">Variable cost</span></span></td>
<td><span data-ttu-id="7a1ee-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="7a1ee-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-685">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="7a1ee-686">CC002</span><span class="sxs-lookup"><span data-stu-id="7a1ee-686">CC002</span></span></td>
<td><span data-ttu-id="7a1ee-687">Finans</span><span class="sxs-lookup"><span data-stu-id="7a1ee-687">Finance</span></span></td>
<td><span data-ttu-id="7a1ee-688">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-688">10001</span></span></td>
<td><span data-ttu-id="7a1ee-689">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-689">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-690">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-690">Fixed cost</span></span></td>
<td><span data-ttu-id="7a1ee-691">675.00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-692">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="7a1ee-693">CC002</span><span class="sxs-lookup"><span data-stu-id="7a1ee-693">CC002</span></span></td>
<td><span data-ttu-id="7a1ee-694">Finans</span><span class="sxs-lookup"><span data-stu-id="7a1ee-694">Finance</span></span></td>
<td><span data-ttu-id="7a1ee-695">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-695">10001</span></span></td>
<td><span data-ttu-id="7a1ee-696">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-696">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-697">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-697">Variable cost</span></span></td>
<td><span data-ttu-id="7a1ee-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="7a1ee-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-699">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="7a1ee-700">CC003</span><span class="sxs-lookup"><span data-stu-id="7a1ee-700">CC003</span></span></td>
<td><span data-ttu-id="7a1ee-701">Montaj</span><span class="sxs-lookup"><span data-stu-id="7a1ee-701">Assembly</span></span></td>
<td><span data-ttu-id="7a1ee-702">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-702">10001</span></span></td>
<td><span data-ttu-id="7a1ee-703">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-703">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-704">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-704">Fixed cost</span></span></td>
<td><span data-ttu-id="7a1ee-705">713.75</span><span class="sxs-lookup"><span data-stu-id="7a1ee-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-706">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="7a1ee-707">CC003</span><span class="sxs-lookup"><span data-stu-id="7a1ee-707">CC003</span></span></td>
<td><span data-ttu-id="7a1ee-708">Montaj</span><span class="sxs-lookup"><span data-stu-id="7a1ee-708">Assembly</span></span></td>
<td><span data-ttu-id="7a1ee-709">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-709">10001</span></span></td>
<td><span data-ttu-id="7a1ee-710">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-710">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-711">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-711">Variable cost</span></span></td>
<td><span data-ttu-id="7a1ee-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="7a1ee-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-713">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="7a1ee-714">CC003</span><span class="sxs-lookup"><span data-stu-id="7a1ee-714">CC003</span></span></td>
<td><span data-ttu-id="7a1ee-715">Paketleme</span><span class="sxs-lookup"><span data-stu-id="7a1ee-715">Packaging</span></span></td>
<td><span data-ttu-id="7a1ee-716">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-716">10001</span></span></td>
<td><span data-ttu-id="7a1ee-717">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-717">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-718">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-718">Fixed cost</span></span></td>
<td><span data-ttu-id="7a1ee-719">286.25</span><span class="sxs-lookup"><span data-stu-id="7a1ee-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-720">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="7a1ee-721">CC003</span><span class="sxs-lookup"><span data-stu-id="7a1ee-721">CC003</span></span></td>
<td><span data-ttu-id="7a1ee-722">Paketleme</span><span class="sxs-lookup"><span data-stu-id="7a1ee-722">Packaging</span></span></td>
<td><span data-ttu-id="7a1ee-723">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-723">10001</span></span></td>
<td><span data-ttu-id="7a1ee-724">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-724">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-725">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-725">Variable cost</span></span></td>
<td><span data-ttu-id="7a1ee-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="7a1ee-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-727">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="7a1ee-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-728">Prod 1</span></span></td>
<td><span data-ttu-id="7a1ee-729">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-729">Product 1</span></span></td>
<td><span data-ttu-id="7a1ee-730">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-730">10001</span></span></td>
<td><span data-ttu-id="7a1ee-731">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-731">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-732">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-732">Fixed cost</span></span></td>
<td><span data-ttu-id="7a1ee-733">776.36</span><span class="sxs-lookup"><span data-stu-id="7a1ee-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-734">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="7a1ee-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-735">Prod 1</span></span></td>
<td><span data-ttu-id="7a1ee-736">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-736">Product 1</span></span></td>
<td><span data-ttu-id="7a1ee-737">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-737">10001</span></span></td>
<td><span data-ttu-id="7a1ee-738">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-738">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-739">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-739">Variable cost</span></span></td>
<td><span data-ttu-id="7a1ee-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="7a1ee-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-741">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="7a1ee-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7a1ee-742">Prod 2</span></span></td>
<td><span data-ttu-id="7a1ee-743">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-743">Product 1</span></span></td>
<td><span data-ttu-id="7a1ee-744">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-744">10001</span></span></td>
<td><span data-ttu-id="7a1ee-745">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-745">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-746">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-746">Fixed cost</span></span></td>
<td><span data-ttu-id="7a1ee-747">223.64</span><span class="sxs-lookup"><span data-stu-id="7a1ee-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-748">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="7a1ee-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7a1ee-749">Prod 2</span></span></td>
<td><span data-ttu-id="7a1ee-750">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-750">Product 1</span></span></td>
<td><span data-ttu-id="7a1ee-751">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-751">10001</span></span></td>
<td><span data-ttu-id="7a1ee-752">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-752">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-753">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-753">Variable cost</span></span></td>
<td><span data-ttu-id="7a1ee-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="7a1ee-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="7a1ee-755">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="7a1ee-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a1ee-756">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7a1ee-757">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-757">Cost element</span></span></th>
<th><span data-ttu-id="7a1ee-758">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="7a1ee-758">Cost behavior</span></span></th>
<th><span data-ttu-id="7a1ee-759">Tutar</span><span class="sxs-lookup"><span data-stu-id="7a1ee-759">Amount</span></span></th>
<th><span data-ttu-id="7a1ee-760">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a1ee-761">CC001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-761">CC001</span></span></td>
<td><span data-ttu-id="7a1ee-762">İK</span><span class="sxs-lookup"><span data-stu-id="7a1ee-762">HR</span></span></td>
<td><span data-ttu-id="7a1ee-763">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-763">10001</span></span></td>
<td><span data-ttu-id="7a1ee-764">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-764">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-765">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-765">Fixed cost</span></span></td>
<td><span data-ttu-id="7a1ee-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-766">-500.00</span></span></td>
<td><span data-ttu-id="7a1ee-767">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-768">CC002</span><span class="sxs-lookup"><span data-stu-id="7a1ee-768">CC002</span></span></td>
<td><span data-ttu-id="7a1ee-769">Finans</span><span class="sxs-lookup"><span data-stu-id="7a1ee-769">Finance</span></span></td>
<td><span data-ttu-id="7a1ee-770">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-770">10001</span></span></td>
<td><span data-ttu-id="7a1ee-771">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-771">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-772">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-772">Fixed cost</span></span></td>
<td><span data-ttu-id="7a1ee-773">175.00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-773">175.00</span></span></td>
<td><span data-ttu-id="7a1ee-774">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-775">CC003</span><span class="sxs-lookup"><span data-stu-id="7a1ee-775">CC003</span></span></td>
<td><span data-ttu-id="7a1ee-776">Montaj</span><span class="sxs-lookup"><span data-stu-id="7a1ee-776">Assembly</span></span></td>
<td><span data-ttu-id="7a1ee-777">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-777">10001</span></span></td>
<td><span data-ttu-id="7a1ee-778">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-778">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-779">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-779">Fixed cost</span></span></td>
<td><span data-ttu-id="7a1ee-780">275.00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-780">275.00</span></span></td>
<td><span data-ttu-id="7a1ee-781">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-782">CC004</span><span class="sxs-lookup"><span data-stu-id="7a1ee-782">CC004</span></span></td>
<td><span data-ttu-id="7a1ee-783">Paketleme</span><span class="sxs-lookup"><span data-stu-id="7a1ee-783">Packaging</span></span></td>
<td><span data-ttu-id="7a1ee-784">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-784">10001</span></span></td>
<td><span data-ttu-id="7a1ee-785">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-785">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-786">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-786">Fixed cost</span></span></td>
<td><span data-ttu-id="7a1ee-787">50,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-787">50,00</span></span></td>
<td><span data-ttu-id="7a1ee-788">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-789">CC001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-789">CC001</span></span></td>
<td><span data-ttu-id="7a1ee-790">İK</span><span class="sxs-lookup"><span data-stu-id="7a1ee-790">HR</span></span></td>
<td><span data-ttu-id="7a1ee-791">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-791">10001</span></span></td>
<td><span data-ttu-id="7a1ee-792">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-792">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-793">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-793">Variable cost</span></span></td>
<td><span data-ttu-id="7a1ee-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="7a1ee-794">-1,245.71</span></span></td>
<td><span data-ttu-id="7a1ee-795">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-796">CC002</span><span class="sxs-lookup"><span data-stu-id="7a1ee-796">CC002</span></span></td>
<td><span data-ttu-id="7a1ee-797">Finans</span><span class="sxs-lookup"><span data-stu-id="7a1ee-797">Finance</span></span></td>
<td><span data-ttu-id="7a1ee-798">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-798">10001</span></span></td>
<td><span data-ttu-id="7a1ee-799">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-799">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-800">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-800">Variable cost</span></span></td>
<td><span data-ttu-id="7a1ee-801">436.00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-801">436.00</span></span></td>
<td><span data-ttu-id="7a1ee-802">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-803">CC003</span><span class="sxs-lookup"><span data-stu-id="7a1ee-803">CC003</span></span></td>
<td><span data-ttu-id="7a1ee-804">Montaj</span><span class="sxs-lookup"><span data-stu-id="7a1ee-804">Assembly</span></span></td>
<td><span data-ttu-id="7a1ee-805">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-805">10001</span></span></td>
<td><span data-ttu-id="7a1ee-806">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-806">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-807">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-807">Variable cost</span></span></td>
<td><span data-ttu-id="7a1ee-808">685.14</span><span class="sxs-lookup"><span data-stu-id="7a1ee-808">685.14</span></span></td>
<td><span data-ttu-id="7a1ee-809">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-810">CC004</span><span class="sxs-lookup"><span data-stu-id="7a1ee-810">CC004</span></span></td>
<td><span data-ttu-id="7a1ee-811">Paketleme</span><span class="sxs-lookup"><span data-stu-id="7a1ee-811">Packaging</span></span></td>
<td><span data-ttu-id="7a1ee-812">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-812">10001</span></span></td>
<td><span data-ttu-id="7a1ee-813">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-813">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-814">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-814">Variable cost</span></span></td>
<td><span data-ttu-id="7a1ee-815">124.57</span><span class="sxs-lookup"><span data-stu-id="7a1ee-815">124.57</span></span></td>
<td><span data-ttu-id="7a1ee-816">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-817">CC002</span><span class="sxs-lookup"><span data-stu-id="7a1ee-817">CC002</span></span></td>
<td><span data-ttu-id="7a1ee-818">Finans</span><span class="sxs-lookup"><span data-stu-id="7a1ee-818">Finance</span></span></td>
<td><span data-ttu-id="7a1ee-819">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-819">10001</span></span></td>
<td><span data-ttu-id="7a1ee-820">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-820">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-821">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-821">Fixed cost</span></span></td>
<td><span data-ttu-id="7a1ee-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-822">-675.00</span></span></td>
<td><span data-ttu-id="7a1ee-823">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-824">CC003</span><span class="sxs-lookup"><span data-stu-id="7a1ee-824">CC003</span></span></td>
<td><span data-ttu-id="7a1ee-825">Montaj</span><span class="sxs-lookup"><span data-stu-id="7a1ee-825">Assembly</span></span></td>
<td><span data-ttu-id="7a1ee-826">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-826">10001</span></span></td>
<td><span data-ttu-id="7a1ee-827">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-827">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-828">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-828">Fixed cost</span></span></td>
<td><span data-ttu-id="7a1ee-829">438.75</span><span class="sxs-lookup"><span data-stu-id="7a1ee-829">438.75</span></span></td>
<td><span data-ttu-id="7a1ee-830">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-831">CC004</span><span class="sxs-lookup"><span data-stu-id="7a1ee-831">CC004</span></span></td>
<td><span data-ttu-id="7a1ee-832">Paketleme</span><span class="sxs-lookup"><span data-stu-id="7a1ee-832">Packaging</span></span></td>
<td><span data-ttu-id="7a1ee-833">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-833">10001</span></span></td>
<td><span data-ttu-id="7a1ee-834">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-834">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-835">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-835">Fixed cost</span></span></td>
<td><span data-ttu-id="7a1ee-836">236.25</span><span class="sxs-lookup"><span data-stu-id="7a1ee-836">236.25</span></span></td>
<td><span data-ttu-id="7a1ee-837">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-838">CC002</span><span class="sxs-lookup"><span data-stu-id="7a1ee-838">CC002</span></span></td>
<td><span data-ttu-id="7a1ee-839">Finans</span><span class="sxs-lookup"><span data-stu-id="7a1ee-839">Finance</span></span></td>
<td><span data-ttu-id="7a1ee-840">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-840">10001</span></span></td>
<td><span data-ttu-id="7a1ee-841">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-841">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-842">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-842">Variable cost</span></span></td>
<td><span data-ttu-id="7a1ee-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="7a1ee-843">-8,150.29</span></span></td>
<td><span data-ttu-id="7a1ee-844">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-845">CC003</span><span class="sxs-lookup"><span data-stu-id="7a1ee-845">CC003</span></span></td>
<td><span data-ttu-id="7a1ee-846">Montaj</span><span class="sxs-lookup"><span data-stu-id="7a1ee-846">Assembly</span></span></td>
<td><span data-ttu-id="7a1ee-847">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-847">10001</span></span></td>
<td><span data-ttu-id="7a1ee-848">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-848">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-849">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-849">Variable cost</span></span></td>
<td><span data-ttu-id="7a1ee-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="7a1ee-850">5,297.69</span></span></td>
<td><span data-ttu-id="7a1ee-851">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-852">CC004</span><span class="sxs-lookup"><span data-stu-id="7a1ee-852">CC004</span></span></td>
<td><span data-ttu-id="7a1ee-853">Paketleme</span><span class="sxs-lookup"><span data-stu-id="7a1ee-853">Packaging</span></span></td>
<td><span data-ttu-id="7a1ee-854">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-854">10001</span></span></td>
<td><span data-ttu-id="7a1ee-855">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-855">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-856">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-856">Variable cost</span></span></td>
<td><span data-ttu-id="7a1ee-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="7a1ee-857">2,852.60</span></span></td>
<td><span data-ttu-id="7a1ee-858">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-859">CC003</span><span class="sxs-lookup"><span data-stu-id="7a1ee-859">CC003</span></span></td>
<td><span data-ttu-id="7a1ee-860">Montaj</span><span class="sxs-lookup"><span data-stu-id="7a1ee-860">Assembly</span></span></td>
<td><span data-ttu-id="7a1ee-861">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-861">10001</span></span></td>
<td><span data-ttu-id="7a1ee-862">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-862">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-863">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-863">Fixed cost</span></span></td>
<td><span data-ttu-id="7a1ee-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="7a1ee-864">-713.75</span></span></td>
<td><span data-ttu-id="7a1ee-865">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-866">Prod 1</span></span></td>
<td><span data-ttu-id="7a1ee-867">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-867">Product 1</span></span></td>
<td><span data-ttu-id="7a1ee-868">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-868">10001</span></span></td>
<td><span data-ttu-id="7a1ee-869">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-869">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-870">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-870">Fixed cost</span></span></td>
<td><span data-ttu-id="7a1ee-871">535.31</span><span class="sxs-lookup"><span data-stu-id="7a1ee-871">535.31</span></span></td>
<td><span data-ttu-id="7a1ee-872">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7a1ee-873">Prod 2</span></span></td>
<td><span data-ttu-id="7a1ee-874">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="7a1ee-874">Product 2</span></span></td>
<td><span data-ttu-id="7a1ee-875">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-875">10001</span></span></td>
<td><span data-ttu-id="7a1ee-876">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-876">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-877">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-877">Fixed cost</span></span></td>
<td><span data-ttu-id="7a1ee-878">178.44</span><span class="sxs-lookup"><span data-stu-id="7a1ee-878">178.44</span></span></td>
<td><span data-ttu-id="7a1ee-879">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-880">CC003</span><span class="sxs-lookup"><span data-stu-id="7a1ee-880">CC003</span></span></td>
<td><span data-ttu-id="7a1ee-881">Montaj</span><span class="sxs-lookup"><span data-stu-id="7a1ee-881">Assembly</span></span></td>
<td><span data-ttu-id="7a1ee-882">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-882">10001</span></span></td>
<td><span data-ttu-id="7a1ee-883">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-883">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-884">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-884">Variable cost</span></span></td>
<td><span data-ttu-id="7a1ee-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="7a1ee-885">-5,982.83</span></span></td>
<td><span data-ttu-id="7a1ee-886">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-887">Prod 1</span></span></td>
<td><span data-ttu-id="7a1ee-888">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-888">Product 1</span></span></td>
<td><span data-ttu-id="7a1ee-889">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-889">10001</span></span></td>
<td><span data-ttu-id="7a1ee-890">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-890">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-891">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-891">Variable cost</span></span></td>
<td><span data-ttu-id="7a1ee-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="7a1ee-892">4,487.12</span></span></td>
<td><span data-ttu-id="7a1ee-893">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7a1ee-894">Prod 2</span></span></td>
<td><span data-ttu-id="7a1ee-895">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="7a1ee-895">Product 2</span></span></td>
<td><span data-ttu-id="7a1ee-896">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-896">10001</span></span></td>
<td><span data-ttu-id="7a1ee-897">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-897">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-898">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-898">Variable cost</span></span></td>
<td><span data-ttu-id="7a1ee-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="7a1ee-899">1,495.71</span></span></td>
<td><span data-ttu-id="7a1ee-900">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-901">CC003</span><span class="sxs-lookup"><span data-stu-id="7a1ee-901">CC003</span></span></td>
<td><span data-ttu-id="7a1ee-902">Montaj</span><span class="sxs-lookup"><span data-stu-id="7a1ee-902">Assembly</span></span></td>
<td><span data-ttu-id="7a1ee-903">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-903">10001</span></span></td>
<td><span data-ttu-id="7a1ee-904">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-904">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-905">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-905">Fixed cost</span></span></td>
<td><span data-ttu-id="7a1ee-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="7a1ee-906">-286.25</span></span></td>
<td><span data-ttu-id="7a1ee-907">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-908">Prod 1</span></span></td>
<td><span data-ttu-id="7a1ee-909">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-909">Product 1</span></span></td>
<td><span data-ttu-id="7a1ee-910">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-910">10001</span></span></td>
<td><span data-ttu-id="7a1ee-911">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-911">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-912">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-912">Fixed cost</span></span></td>
<td><span data-ttu-id="7a1ee-913">241.05</span><span class="sxs-lookup"><span data-stu-id="7a1ee-913">241.05</span></span></td>
<td><span data-ttu-id="7a1ee-914">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7a1ee-915">Prod 2</span></span></td>
<td><span data-ttu-id="7a1ee-916">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="7a1ee-916">Product 2</span></span></td>
<td><span data-ttu-id="7a1ee-917">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-917">10001</span></span></td>
<td><span data-ttu-id="7a1ee-918">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-918">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-919">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-919">Fixed cost</span></span></td>
<td><span data-ttu-id="7a1ee-920">45.20</span><span class="sxs-lookup"><span data-stu-id="7a1ee-920">45.20</span></span></td>
<td><span data-ttu-id="7a1ee-921">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-922">CC003</span><span class="sxs-lookup"><span data-stu-id="7a1ee-922">CC003</span></span></td>
<td><span data-ttu-id="7a1ee-923">Montaj</span><span class="sxs-lookup"><span data-stu-id="7a1ee-923">Assembly</span></span></td>
<td><span data-ttu-id="7a1ee-924">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-924">10001</span></span></td>
<td><span data-ttu-id="7a1ee-925">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-925">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-926">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-926">Variable cost</span></span></td>
<td><span data-ttu-id="7a1ee-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="7a1ee-927">-2,977.17</span></span></td>
<td><span data-ttu-id="7a1ee-928">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-929">Prod 1</span></span></td>
<td><span data-ttu-id="7a1ee-930">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-930">Product 1</span></span></td>
<td><span data-ttu-id="7a1ee-931">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-931">10001</span></span></td>
<td><span data-ttu-id="7a1ee-932">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-932">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-933">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-933">Variable cost</span></span></td>
<td><span data-ttu-id="7a1ee-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="7a1ee-934">2,507.09</span></span></td>
<td><span data-ttu-id="7a1ee-935">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a1ee-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7a1ee-936">Prod 2</span></span></td>
<td><span data-ttu-id="7a1ee-937">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="7a1ee-937">Product 2</span></span></td>
<td><span data-ttu-id="7a1ee-938">10001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-938">10001</span></span></td>
<td><span data-ttu-id="7a1ee-939">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-939">Electricity</span></span></td>
<td><span data-ttu-id="7a1ee-940">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-940">Variable cost</span></span></td>
<td><span data-ttu-id="7a1ee-941">470.08</span><span class="sxs-lookup"><span data-stu-id="7a1ee-941">470.08</span></span></td>
<td><span data-ttu-id="7a1ee-942">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7a1ee-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="7a1ee-943">Sonuç</span><span class="sxs-lookup"><span data-stu-id="7a1ee-943">Conclusion</span></span>
<span data-ttu-id="7a1ee-944">Mali muhasebede, Elektrik için 10.000,00 maliyet bir sözde maliyet merkezi kimliğine nakledilmiştir.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="7a1ee-945">Bu nedenle, maliyet muhasebecileri bu maliyetin tahsis edilmesi gerektiğini bilirler.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="7a1ee-946">Maliyet muhasebesinde, maliyetler kuruluş birimleri ve seviyeleri arasında, uygulanan kural ve ilkelere dayalı olarak akar.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="7a1ee-947">Her maliyet, maliyetlerin tahsisatı için en iyi değerlendirmeyi sağlayan bir tahsisat tabanı ile ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="7a1ee-948">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="7a1ee-949">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7a1ee-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="7a1ee-950">Toplam</span><span class="sxs-lookup"><span data-stu-id="7a1ee-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="7a1ee-951">CC099</span><span class="sxs-lookup"><span data-stu-id="7a1ee-951">CC099</span></span></th>
<th><span data-ttu-id="7a1ee-952">CC001</span><span class="sxs-lookup"><span data-stu-id="7a1ee-952">CC001</span></span></th>
<th><span data-ttu-id="7a1ee-953">CC002</span><span class="sxs-lookup"><span data-stu-id="7a1ee-953">CC002</span></span></th>
<th><span data-ttu-id="7a1ee-954">CC003</span><span class="sxs-lookup"><span data-stu-id="7a1ee-954">CC003</span></span></th>
<th><span data-ttu-id="7a1ee-955">CC004</span><span class="sxs-lookup"><span data-stu-id="7a1ee-955">CC004</span></span></th>
<th><span data-ttu-id="7a1ee-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-956">Proj 1</span></span></th>
<th><span data-ttu-id="7a1ee-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="7a1ee-957">Proj 2</span></span></th>
<th><span data-ttu-id="7a1ee-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7a1ee-958">Prod 1</span></span></th>
<th><span data-ttu-id="7a1ee-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7a1ee-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="7a1ee-960">10001 Elektrik</span><span class="sxs-lookup"><span data-stu-id="7a1ee-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a1ee-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="7a1ee-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a1ee-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="7a1ee-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a1ee-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="7a1ee-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a1ee-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="7a1ee-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="7a1ee-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="7a1ee-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a1ee-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="7a1ee-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a1ee-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="7a1ee-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a1ee-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="7a1ee-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a1ee-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="7a1ee-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="7a1ee-970">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="7a1ee-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a1ee-971">0,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="7a1ee-972">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a1ee-973">0,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a1ee-974">0,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a1ee-975">0,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a1ee-976">0,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a1ee-977">0,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="7a1ee-978">776.36</span><span class="sxs-lookup"><span data-stu-id="7a1ee-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a1ee-979">223.64</span><span class="sxs-lookup"><span data-stu-id="7a1ee-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a1ee-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="7a1ee-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="7a1ee-981">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7a1ee-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a1ee-982">000</span><span class="sxs-lookup"><span data-stu-id="7a1ee-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a1ee-983">0,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a1ee-984">0,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a1ee-985">0,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a1ee-986">0,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a1ee-987">30.00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a1ee-988">10,00</span><span class="sxs-lookup"><span data-stu-id="7a1ee-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a1ee-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="7a1ee-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a1ee-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="7a1ee-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a1ee-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="7a1ee-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="7a1ee-992">Bu konu, birincil maliyet öğesi, 10001 Elektrik'in maliyet nesneleri arasında nasıl aktığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="7a1ee-993">Bu nedenle, bu genel gider maliyeti kuruluşun en düşük seviyesine tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="7a1ee-994">Başka bir deyişle, maliyet en alt düzeydeki maliyet nesnelerine aittir.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="7a1ee-995">Maliyetin, maliyet nesneleri arasında görsel bir akışına ihtiyacınız varsa, maliyetin akışını görselleştirmek için maliyet toplamı ilke kurallarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7a1ee-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="7a1ee-996">Daha fazla bilgi için bkz. [Maliyet yuvarlama ilkesi ve genel gider hesaplaması](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="7a1ee-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



