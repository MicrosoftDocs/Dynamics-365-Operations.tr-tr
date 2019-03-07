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
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 4de705324ac497cfb11fae3dadc6f57d038fd0b5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "335129"
---
# <a name="overhead-calculation"></a><span data-ttu-id="57622-103">Genel gider hesaplaması</span><span class="sxs-lookup"><span data-stu-id="57622-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="57622-104">Bu konu, genel gider maliyetlerinin hesaplanması için tipik işlemleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="57622-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="57622-105">Terim tanımı</span><span class="sxs-lookup"><span data-stu-id="57622-105">Term definition</span></span>
---------------

<span data-ttu-id="57622-106">Genel gider maliyetleri bir işletmenin çalışması için normalde uygulanan, ancak doğrudan herhangi bir özel iş, faaliyet, ürün veya hizmete ilişkilendirilmemiş olan maliyetlerdir.</span><span class="sxs-lookup"><span data-stu-id="57622-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="57622-107">Genel gider maliyetleri kar sağlama faaliyetlerinin oluşturulması için kritik destek sağlar.</span><span class="sxs-lookup"><span data-stu-id="57622-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="57622-108">Aşağıda bazı genel gider örnekleri verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="57622-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="57622-109">Kira</span><span class="sxs-lookup"><span data-stu-id="57622-109">Rent</span></span>
-   <span data-ttu-id="57622-110">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-110">Electricity</span></span>
-   <span data-ttu-id="57622-111">Yönetim maaşları</span><span class="sxs-lookup"><span data-stu-id="57622-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="57622-112">Genel gider hesaplaması genel bakış</span><span class="sxs-lookup"><span data-stu-id="57622-112">Overhead calculation overview</span></span>
<span data-ttu-id="57622-113">Genel gider hesaplama, maliyet muhasebesi ilkelerini doğru sırayla çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="57622-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="57622-114">Maliyet muhasebesi ilkeleri değiştiyse veya belirli hatalar algılandıysa, genel gider hesaplamasını aynı mali dönem için birden fazla kez yürütebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="57622-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="57622-115">Her genel gider hesaplaması depolanır ve önceki sürümlerdeki hesaplamaları kıyaslamanıza olanak sağlayan, benzersiz bir sürüm kimliğine sahip olur.</span><span class="sxs-lookup"><span data-stu-id="57622-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="57622-116">Genel gider hesaplamasının oluşturduğu maliyet girişleri bir muhasebe tarihi alır.</span><span class="sxs-lookup"><span data-stu-id="57622-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="57622-117">Bu muhasebe tarihi, hesaplamada kullanılan mali dönemin bitiş tarihiyle eşleşir.</span><span class="sxs-lookup"><span data-stu-id="57622-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="57622-118">Benzersiz sürüm kimliği aşağıdaki öğelerden oluşur:</span><span class="sxs-lookup"><span data-stu-id="57622-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="57622-119">Sürüm türü</span><span class="sxs-lookup"><span data-stu-id="57622-119">Version type</span></span>
-   <span data-ttu-id="57622-120">Tarih ve saat</span><span class="sxs-lookup"><span data-stu-id="57622-120">Date and time</span></span>
-   <span data-ttu-id="57622-121">Maliyet muhasebesi defteri</span><span class="sxs-lookup"><span data-stu-id="57622-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="57622-122">Mali yıl</span><span class="sxs-lookup"><span data-stu-id="57622-122">Fiscal year</span></span>
-   <span data-ttu-id="57622-123">Mali dönem</span><span class="sxs-lookup"><span data-stu-id="57622-123">Fiscal period</span></span>

<span data-ttu-id="57622-124">Genel gider hesaplama, sürümden bağımsız olarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="57622-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="57622-125">Bu nedenle, Gerçek sürümden önce Bütçe sürümünü hesaplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="57622-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="57622-126">Genel gider hesaplama dört adımdan oluşur, aşağıdaki çizimde gösterildiği gibi.</span><span class="sxs-lookup"><span data-stu-id="57622-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="57622-127">Her adımda, günlük girişleri olan bir günlük başlığı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="57622-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="57622-128">Bu günlük başlığı, her hesaplama adımı için giriş verilerini tutar.</span><span class="sxs-lookup"><span data-stu-id="57622-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="57622-129">İlkeler ve kurallar her günlük satırına uygulanır ve maliyet girişleri çıkış olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="57622-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="57622-130">Bu nedenle, her zaman tam izlenebilirliğe sahip olursunuz.</span><span class="sxs-lookup"><span data-stu-id="57622-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="57622-131">[![Genel gider hesaplaması](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="57622-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="57622-132">Elektrik genel gideri maliyetini hesapla ve tahsis et</span><span class="sxs-lookup"><span data-stu-id="57622-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="57622-133">Mali muhasebede, elektrik gibi bazı maliyetler peşin ödeme olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="57622-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="57622-134">Bu nedenle, Maliyet muhasebesi için ayrıntılı yönetim bilgiler sağlanmaz.</span><span class="sxs-lookup"><span data-stu-id="57622-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="57622-135">Maliyet muhasebesinde doğru yönetimsel bilgileri tüm yönetim birim ve düzeylerinde sağlamak için, maliyetlerin kuruluş birimleri arasında akması gerekir.</span><span class="sxs-lookup"><span data-stu-id="57622-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="57622-136">Bu akış, tüketimin doğru bir kaydına ya da adil bir değerlendirmeye dayanıyor olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="57622-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="57622-137">Genel muhasebede, bir elektrik maliyeti aşağıdaki tabloda gösterildiği gibi deftere nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="57622-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="57622-138">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="57622-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="57622-139">Maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="57622-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="57622-140">Ana hesap</span><span class="sxs-lookup"><span data-stu-id="57622-140">Main account</span></span></th>
<th><span data-ttu-id="57622-141">Muhasebe para birimi cinsinden tutar</span><span class="sxs-lookup"><span data-stu-id="57622-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="57622-142">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="57622-143">CC099</span><span class="sxs-lookup"><span data-stu-id="57622-143">CC099</span></span></td>
<td><span data-ttu-id="57622-144">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="57622-144">Default cost center</span></span></td>
<td><span data-ttu-id="57622-145">10001</span><span class="sxs-lookup"><span data-stu-id="57622-145">10001</span></span></td>
<td><span data-ttu-id="57622-146">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-146">Electricity</span></span></td>
<td><span data-ttu-id="57622-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="57622-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="57622-148">Adım 1: Maliyet davranışı hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="57622-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="57622-149">Varsayılan olarak, maliyeti girişleri kaynak veriden içeri alındığında, Maliyet muhasebesinde **Sınıflandırılmamış** maliyet davranışı sınıflandırmasını alırlar.</span><span class="sxs-lookup"><span data-stu-id="57622-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="57622-150">Maliyet davranışı ilke kuralları ekleyerek, maliyet girişlerini **Sabit maliyet** veya **Değişken maliyet** olarak yeniden sınıflandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="57622-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="57622-151">Maliyet davranış kuralını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="57622-151">Define the cost behavior rule</span></span>

<span data-ttu-id="57622-152">Bazı durumlarda, sabit bir ücret maliyet parçasıdır ve kalan maliyet, tüketime dayanır.</span><span class="sxs-lookup"><span data-stu-id="57622-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="57622-153">Elektrik faturaları genellikle bu tanıma uyar.</span><span class="sxs-lookup"><span data-stu-id="57622-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="57622-154">Belirli bir sabit ücret ödedikten sonra, kilovat saatlik (Kwh) tüketim başına ödeme yaparsınız.</span><span class="sxs-lookup"><span data-stu-id="57622-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="57622-155">Örneğin, sabit maliyet masrafı 1.000,00 ise, maliyet davranışı kural nasıl tanımlanır:</span><span class="sxs-lookup"><span data-stu-id="57622-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="57622-156">Sabit tutar 1.000,00</span><span class="sxs-lookup"><span data-stu-id="57622-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="57622-157">0 &lt;= 1.000,00 = Sabit</span><span class="sxs-lookup"><span data-stu-id="57622-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="57622-158">1000,01 &lt; N = Değişken</span><span class="sxs-lookup"><span data-stu-id="57622-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="57622-159">Günlük</span><span class="sxs-lookup"><span data-stu-id="57622-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="57622-160">Günlük</span><span class="sxs-lookup"><span data-stu-id="57622-160">Journal</span></span></th>
<th><span data-ttu-id="57622-161">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="57622-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="57622-162">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="57622-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="57622-163">Sürüm</span><span class="sxs-lookup"><span data-stu-id="57622-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="57622-164">00001</span><span class="sxs-lookup"><span data-stu-id="57622-164">00001</span></span></td>
<td><span data-ttu-id="57622-165">Maliyet davranışı hesaplama günlüğü</span><span class="sxs-lookup"><span data-stu-id="57622-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="57622-166">Mali</span><span class="sxs-lookup"><span data-stu-id="57622-166">Fiscal</span></span></td>
<td><span data-ttu-id="57622-167">2017</span><span class="sxs-lookup"><span data-stu-id="57622-167">2017</span></span></td>
<td><span data-ttu-id="57622-168">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="57622-168">Period 1</span></span></td>
<td><span data-ttu-id="57622-169">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="57622-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="57622-170">Günlük girişleri (Maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="57622-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="57622-171">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="57622-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="57622-172">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="57622-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="57622-173">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="57622-173">Cost element</span></span></th>
<th><span data-ttu-id="57622-174">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="57622-174">Cost behavior</span></span></th>
<th><span data-ttu-id="57622-175">Tutar</span><span class="sxs-lookup"><span data-stu-id="57622-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="57622-176">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="57622-177">CC099</span><span class="sxs-lookup"><span data-stu-id="57622-177">CC099</span></span></td>
<td><span data-ttu-id="57622-178">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="57622-178">Default cost center</span></span></td>
<td><span data-ttu-id="57622-179">10001</span><span class="sxs-lookup"><span data-stu-id="57622-179">10001</span></span></td>
<td><span data-ttu-id="57622-180">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-180">Electricity</span></span></td>
<td><span data-ttu-id="57622-181">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="57622-181">Unclassified</span></span></td>
<td><span data-ttu-id="57622-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="57622-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="57622-183">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="57622-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="57622-184">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="57622-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="57622-185">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="57622-185">Cost element</span></span></th>
<th><span data-ttu-id="57622-186">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="57622-186">Cost behavior</span></span></th>
<th><span data-ttu-id="57622-187">Tutar</span><span class="sxs-lookup"><span data-stu-id="57622-187">Amount</span></span></th>
<th><span data-ttu-id="57622-188">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="57622-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="57622-189">CC099</span><span class="sxs-lookup"><span data-stu-id="57622-189">CC099</span></span></td>
<td><span data-ttu-id="57622-190">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="57622-190">Default cost center</span></span></td>
<td><span data-ttu-id="57622-191">10001</span><span class="sxs-lookup"><span data-stu-id="57622-191">10001</span></span></td>
<td><span data-ttu-id="57622-192">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-192">Electricity</span></span></td>
<td><span data-ttu-id="57622-193">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="57622-193">Unclassified</span></span></td>
<td><span data-ttu-id="57622-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="57622-194">10,000.00</span></span></td>
<td><span data-ttu-id="57622-195">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-196">CC099</span><span class="sxs-lookup"><span data-stu-id="57622-196">CC099</span></span></td>
<td><span data-ttu-id="57622-197">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="57622-197">Default cost center</span></span></td>
<td><span data-ttu-id="57622-198">10001</span><span class="sxs-lookup"><span data-stu-id="57622-198">10001</span></span></td>
<td><span data-ttu-id="57622-199">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-199">Electricity</span></span></td>
<td><span data-ttu-id="57622-200">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="57622-200">Unclassified</span></span></td>
<td><span data-ttu-id="57622-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="57622-201">-10,000.00</span></span></td>
<td><span data-ttu-id="57622-202">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-203">CC099</span><span class="sxs-lookup"><span data-stu-id="57622-203">CC099</span></span></td>
<td><span data-ttu-id="57622-204">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="57622-204">Default cost center</span></span></td>
<td><span data-ttu-id="57622-205">10001</span><span class="sxs-lookup"><span data-stu-id="57622-205">10001</span></span></td>
<td><span data-ttu-id="57622-206">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-206">Electricity</span></span></td>
<td><span data-ttu-id="57622-207">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-207">Fixed cost</span></span></td>
<td><span data-ttu-id="57622-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="57622-208">1,000.00</span></span></td>
<td><span data-ttu-id="57622-209">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-210">CC099</span><span class="sxs-lookup"><span data-stu-id="57622-210">CC099</span></span></td>
<td><span data-ttu-id="57622-211">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="57622-211">Default cost center</span></span></td>
<td><span data-ttu-id="57622-212">10001</span><span class="sxs-lookup"><span data-stu-id="57622-212">10001</span></span></td>
<td><span data-ttu-id="57622-213">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-213">Electricity</span></span></td>
<td><span data-ttu-id="57622-214">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-214">Variable cost</span></span></td>
<td><span data-ttu-id="57622-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="57622-215">9,000.00</span></span></td>
<td><span data-ttu-id="57622-216">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="57622-217">Daha fazla bilgi için bkz. [Maliyet davranışı ilkesi oluşturma ve bir maliyet kontrol birimine atama](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="57622-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="57622-218">Adım 2: Maliyet dağıtımı hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="57622-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="57622-219">Maliyet dağıtımı, bir nesneden bir veya daha fazlasına ilgili tahsisat tabanı uygulayarak maliyeti yeniden dağıtmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="57622-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="57622-220">Maliyet dağıtımı ve maliyet tahsisatı, maliyet dağıtımının her zaman orijinal maliyetin birincil maliyet öğesinde bulunmasıyla farklılık gösterir.</span><span class="sxs-lookup"><span data-stu-id="57622-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="57622-221">Maliyet dağıtım kuralını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="57622-221">Define the cost distribution rule</span></span>

<span data-ttu-id="57622-222">Mali muhasebede, elektrik maliyetleri çoğu zaman peşin ödeme olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="57622-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="57622-223">Maliyet muhasebesinde ise bu yöntem yeterince ayrıntılı değildir.</span><span class="sxs-lookup"><span data-stu-id="57622-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="57622-224">Değişken maliyet, maliyet nesnelerine tek tek, adil bir temele dayanarak dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="57622-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="57622-225">En mantıklı tahsisat, elektrik kullanımını (Kwh) temel alarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="57622-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="57622-226">Elektrik adına sahip, istatistiksel bir boyut üyesi oluşturulur ve elektrik tüketimi kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="57622-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="57622-227">Varsayıla olarak, tüm istatistiksel boyut üyeleri tahsisat tabanları olarak kullanılabilir hale gelir.</span><span class="sxs-lookup"><span data-stu-id="57622-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="57622-228">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="57622-228">Cost object</span></span></th>
<th><span data-ttu-id="57622-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="57622-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="57622-230">CC001</span><span class="sxs-lookup"><span data-stu-id="57622-230">CC001</span></span></td>
<td><span data-ttu-id="57622-231">İK</span><span class="sxs-lookup"><span data-stu-id="57622-231">HR</span></span></td>
<td><span data-ttu-id="57622-232">1.000</span><span class="sxs-lookup"><span data-stu-id="57622-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-233">CC002</span><span class="sxs-lookup"><span data-stu-id="57622-233">CC002</span></span></td>
<td><span data-ttu-id="57622-234">Finans</span><span class="sxs-lookup"><span data-stu-id="57622-234">Finance</span></span></td>
<td><span data-ttu-id="57622-235">6,000</span><span class="sxs-lookup"><span data-stu-id="57622-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-236">CC003</span><span class="sxs-lookup"><span data-stu-id="57622-236">CC003</span></span></td>
<td><span data-ttu-id="57622-237">Montaj</span><span class="sxs-lookup"><span data-stu-id="57622-237">Assembly</span></span></td>
<td><span data-ttu-id="57622-238">0</span><span class="sxs-lookup"><span data-stu-id="57622-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="57622-239">Aşağıdaki tablo, elektrik tüketiminin değişken maliyetler için bir tahsisat tabanlı olarak uygulandığındaki sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="57622-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="57622-240">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="57622-240">Cost object</span></span></th>
<th><span data-ttu-id="57622-241">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="57622-241">Magnitude</span></span></th>
<th><span data-ttu-id="57622-242">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="57622-242">Allocation factor</span></span></th>
<th><span data-ttu-id="57622-243">Tutar</span><span class="sxs-lookup"><span data-stu-id="57622-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="57622-244">CC001</span><span class="sxs-lookup"><span data-stu-id="57622-244">CC001</span></span></td>
<td><span data-ttu-id="57622-245">İK</span><span class="sxs-lookup"><span data-stu-id="57622-245">HR</span></span></td>
<td><span data-ttu-id="57622-246">1.000</span><span class="sxs-lookup"><span data-stu-id="57622-246">1,000</span></span></td>
<td><span data-ttu-id="57622-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="57622-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="57622-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="57622-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-249">CC002</span><span class="sxs-lookup"><span data-stu-id="57622-249">CC002</span></span></td>
<td><span data-ttu-id="57622-250">Finans</span><span class="sxs-lookup"><span data-stu-id="57622-250">Finance</span></span></td>
<td><span data-ttu-id="57622-251">6,000</span><span class="sxs-lookup"><span data-stu-id="57622-251">6,000</span></span></td>
<td><span data-ttu-id="57622-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="57622-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="57622-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="57622-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-254">CC003</span><span class="sxs-lookup"><span data-stu-id="57622-254">CC003</span></span></td>
<td><span data-ttu-id="57622-255">Montaj</span><span class="sxs-lookup"><span data-stu-id="57622-255">Assembly</span></span></td>
<td><span data-ttu-id="57622-256">0</span><span class="sxs-lookup"><span data-stu-id="57622-256">0</span></span></td>
<td><span data-ttu-id="57622-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="57622-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="57622-258">0,00</span><span class="sxs-lookup"><span data-stu-id="57622-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="57622-259">Sabit maliyet, elektrik tüketmiş olan tekil maliyet nesnelerine eşit miktarda dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="57622-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="57622-260">Bu sonuca, Elektrik istatistiksel boyut öğesini bir formül tahsisat tabanında kullanarak ulaşabilirsiniz: (Elektrik &gt; 0,00) Aşağıdaki tablo, elektrik tüketimi değişken maliyetler için bir tahsisat tabanı olarak kullanıldığında ortaya çıkan sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="57622-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="57622-261">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="57622-261">Cost object</span></span></th>
<th><span data-ttu-id="57622-262">Formül</span><span class="sxs-lookup"><span data-stu-id="57622-262">Formula</span></span></th>
<th><span data-ttu-id="57622-263">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="57622-263">Magnitude</span></span></th>
<th><span data-ttu-id="57622-264">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="57622-264">Allocation factor</span></span></th>
<th><span data-ttu-id="57622-265">Tutar</span><span class="sxs-lookup"><span data-stu-id="57622-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="57622-266">CC001</span><span class="sxs-lookup"><span data-stu-id="57622-266">CC001</span></span></td>
<td><span data-ttu-id="57622-267">İK</span><span class="sxs-lookup"><span data-stu-id="57622-267">HR</span></span></td>
<td><span data-ttu-id="57622-268">(1,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="57622-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="57622-269">1</span><span class="sxs-lookup"><span data-stu-id="57622-269">1</span></span></td>
<td><span data-ttu-id="57622-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="57622-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="57622-271">500.00</span><span class="sxs-lookup"><span data-stu-id="57622-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-272">CC002</span><span class="sxs-lookup"><span data-stu-id="57622-272">CC002</span></span></td>
<td><span data-ttu-id="57622-273">Finans</span><span class="sxs-lookup"><span data-stu-id="57622-273">Finance</span></span></td>
<td><span data-ttu-id="57622-274">(6,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="57622-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="57622-275">1</span><span class="sxs-lookup"><span data-stu-id="57622-275">1</span></span></td>
<td><span data-ttu-id="57622-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="57622-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="57622-277">500.00</span><span class="sxs-lookup"><span data-stu-id="57622-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-278">CC003</span><span class="sxs-lookup"><span data-stu-id="57622-278">CC003</span></span></td>
<td><span data-ttu-id="57622-279">Montaj</span><span class="sxs-lookup"><span data-stu-id="57622-279">Assembly</span></span></td>
<td><span data-ttu-id="57622-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="57622-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="57622-281">0</span><span class="sxs-lookup"><span data-stu-id="57622-281">0</span></span></td>
<td><span data-ttu-id="57622-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="57622-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="57622-283">0,00</span><span class="sxs-lookup"><span data-stu-id="57622-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="57622-284">Günlük</span><span class="sxs-lookup"><span data-stu-id="57622-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="57622-285">Günlük</span><span class="sxs-lookup"><span data-stu-id="57622-285">Journal</span></span></th>
<th><span data-ttu-id="57622-286">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="57622-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="57622-287">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="57622-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="57622-288">Sürüm</span><span class="sxs-lookup"><span data-stu-id="57622-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="57622-289">00002</span><span class="sxs-lookup"><span data-stu-id="57622-289">00002</span></span></td>
<td><span data-ttu-id="57622-290">Maliyet dağıtımı hesaplama günlüğü</span><span class="sxs-lookup"><span data-stu-id="57622-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="57622-291">Mali</span><span class="sxs-lookup"><span data-stu-id="57622-291">Fiscal</span></span></td>
<td><span data-ttu-id="57622-292">2017</span><span class="sxs-lookup"><span data-stu-id="57622-292">2017</span></span></td>
<td><span data-ttu-id="57622-293">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="57622-293">Period 1</span></span></td>
<td><span data-ttu-id="57622-294">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="57622-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="57622-295">Günlük girişleri (Maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="57622-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="57622-296">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="57622-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="57622-297">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="57622-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="57622-298">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="57622-298">Cost element</span></span></th>
<th><span data-ttu-id="57622-299">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="57622-299">Cost behavior</span></span></th>
<th><span data-ttu-id="57622-300">Tutar</span><span class="sxs-lookup"><span data-stu-id="57622-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="57622-301">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="57622-302">CC099</span><span class="sxs-lookup"><span data-stu-id="57622-302">CC099</span></span></td>
<td><span data-ttu-id="57622-303">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="57622-303">Default cost center</span></span></td>
<td><span data-ttu-id="57622-304">10001</span><span class="sxs-lookup"><span data-stu-id="57622-304">10001</span></span></td>
<td><span data-ttu-id="57622-305">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-305">Electricity</span></span></td>
<td><span data-ttu-id="57622-306">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-306">Fixed cost</span></span></td>
<td><span data-ttu-id="57622-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="57622-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-308">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="57622-309">CC099</span><span class="sxs-lookup"><span data-stu-id="57622-309">CC099</span></span></td>
<td><span data-ttu-id="57622-310">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="57622-310">Default cost center</span></span></td>
<td><span data-ttu-id="57622-311">10001</span><span class="sxs-lookup"><span data-stu-id="57622-311">10001</span></span></td>
<td><span data-ttu-id="57622-312">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-312">Electricity</span></span></td>
<td><span data-ttu-id="57622-313">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-313">Variable cost</span></span></td>
<td><span data-ttu-id="57622-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="57622-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="57622-315">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="57622-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="57622-316">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="57622-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="57622-317">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="57622-317">Cost element</span></span></th>
<th><span data-ttu-id="57622-318">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="57622-318">Cost behavior</span></span></th>
<th><span data-ttu-id="57622-319">Tutar</span><span class="sxs-lookup"><span data-stu-id="57622-319">Amount</span></span></th>
<th><span data-ttu-id="57622-320">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="57622-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="57622-321">CC099</span><span class="sxs-lookup"><span data-stu-id="57622-321">CC099</span></span></td>
<td><span data-ttu-id="57622-322">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="57622-322">Default cost center</span></span></td>
<td><span data-ttu-id="57622-323">10001</span><span class="sxs-lookup"><span data-stu-id="57622-323">10001</span></span></td>
<td><span data-ttu-id="57622-324">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-324">Electricity</span></span></td>
<td><span data-ttu-id="57622-325">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-325">Fixed cost</span></span></td>
<td><span data-ttu-id="57622-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="57622-326">-1,000.00</span></span></td>
<td><span data-ttu-id="57622-327">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-328">CC001</span><span class="sxs-lookup"><span data-stu-id="57622-328">CC001</span></span></td>
<td><span data-ttu-id="57622-329">İK</span><span class="sxs-lookup"><span data-stu-id="57622-329">HR</span></span></td>
<td><span data-ttu-id="57622-330">10001</span><span class="sxs-lookup"><span data-stu-id="57622-330">10001</span></span></td>
<td><span data-ttu-id="57622-331">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-331">Electricity</span></span></td>
<td><span data-ttu-id="57622-332">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-332">Fixed cost</span></span></td>
<td><span data-ttu-id="57622-333">500.00</span><span class="sxs-lookup"><span data-stu-id="57622-333">500.00</span></span></td>
<td><span data-ttu-id="57622-334">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-335">CC002</span><span class="sxs-lookup"><span data-stu-id="57622-335">CC002</span></span></td>
<td><span data-ttu-id="57622-336">Finans</span><span class="sxs-lookup"><span data-stu-id="57622-336">Finance</span></span></td>
<td><span data-ttu-id="57622-337">10001</span><span class="sxs-lookup"><span data-stu-id="57622-337">10001</span></span></td>
<td><span data-ttu-id="57622-338">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-338">Electricity</span></span></td>
<td><span data-ttu-id="57622-339">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-339">Fixed cost</span></span></td>
<td><span data-ttu-id="57622-340">500.00</span><span class="sxs-lookup"><span data-stu-id="57622-340">500.00</span></span></td>
<td><span data-ttu-id="57622-341">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-342">CC099</span><span class="sxs-lookup"><span data-stu-id="57622-342">CC099</span></span></td>
<td><span data-ttu-id="57622-343">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="57622-343">Default cost center</span></span></td>
<td><span data-ttu-id="57622-344">10001</span><span class="sxs-lookup"><span data-stu-id="57622-344">10001</span></span></td>
<td><span data-ttu-id="57622-345">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-345">Electricity</span></span></td>
<td><span data-ttu-id="57622-346">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-346">Variable cost</span></span></td>
<td><span data-ttu-id="57622-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="57622-347">-9,000.00</span></span></td>
<td><span data-ttu-id="57622-348">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-349">CC001</span><span class="sxs-lookup"><span data-stu-id="57622-349">CC001</span></span></td>
<td><span data-ttu-id="57622-350">İK</span><span class="sxs-lookup"><span data-stu-id="57622-350">HR</span></span></td>
<td><span data-ttu-id="57622-351">10001</span><span class="sxs-lookup"><span data-stu-id="57622-351">10001</span></span></td>
<td><span data-ttu-id="57622-352">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-352">Electricity</span></span></td>
<td><span data-ttu-id="57622-353">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-353">Variable cost</span></span></td>
<td><span data-ttu-id="57622-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="57622-354">1,285.71</span></span></td>
<td><span data-ttu-id="57622-355">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-356">CC002</span><span class="sxs-lookup"><span data-stu-id="57622-356">CC002</span></span></td>
<td><span data-ttu-id="57622-357">Finans</span><span class="sxs-lookup"><span data-stu-id="57622-357">Finance</span></span></td>
<td><span data-ttu-id="57622-358">10001</span><span class="sxs-lookup"><span data-stu-id="57622-358">10001</span></span></td>
<td><span data-ttu-id="57622-359">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-359">Electricity</span></span></td>
<td><span data-ttu-id="57622-360">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-360">Variable cost</span></span></td>
<td><span data-ttu-id="57622-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="57622-361">7,714.29</span></span></td>
<td><span data-ttu-id="57622-362">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="57622-363">Daha fazla bilgi için bkz. [Maliyet dağıtımı ilkesi oluşturma ve bir maliyet kontrol birimine atama](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="57622-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="57622-364">Adım 3: Genel gider oranı hesaplama işlemi</span><span class="sxs-lookup"><span data-stu-id="57622-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="57622-365">Genel gider oranı, bir veya birden fazla belirli maliyet nesnesine masraf yüklemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="57622-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="57622-366">Masraf, önceden belirlenmiş maliyet oranına ve tahsisat tabanından hesaplanan büyüklüğe dayanır.</span><span class="sxs-lookup"><span data-stu-id="57622-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="57622-367">Genel gider oranını tanımlama</span><span class="sxs-lookup"><span data-stu-id="57622-367">Define the overhead rate</span></span>

<span data-ttu-id="57622-368">Maliyet nesnesi CC001 HR, bir dizi dahili projeye katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="57622-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="57622-369">HR projeleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="57622-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="57622-370">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="57622-370">Cost object</span></span></th>
<th><span data-ttu-id="57622-371">Saatler</span><span class="sxs-lookup"><span data-stu-id="57622-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="57622-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="57622-372">Proj 1</span></span></td>
<td><span data-ttu-id="57622-373">Proje 1</span><span class="sxs-lookup"><span data-stu-id="57622-373">Project 1</span></span></td>
<td><span data-ttu-id="57622-374">3</span><span class="sxs-lookup"><span data-stu-id="57622-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="57622-375">Proj 2</span></span></td>
<td><span data-ttu-id="57622-376">Proje 2</span><span class="sxs-lookup"><span data-stu-id="57622-376">Project 2</span></span></td>
<td><span data-ttu-id="57622-377">1</span><span class="sxs-lookup"><span data-stu-id="57622-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="57622-378">Maliyet projeleri dağıtımı için bir önceden belirlenmiş maliyet oranı tanımlandı.</span><span class="sxs-lookup"><span data-stu-id="57622-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="57622-379">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="57622-379">Cost object</span></span></th>
<th><span data-ttu-id="57622-380">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="57622-380">Cost element</span></span></th>
<th><span data-ttu-id="57622-381">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="57622-381">Cost behavior</span></span></th>
<th><span data-ttu-id="57622-382">Birimler</span><span class="sxs-lookup"><span data-stu-id="57622-382">Units</span></span></th>
<th><span data-ttu-id="57622-383">Ücret</span><span class="sxs-lookup"><span data-stu-id="57622-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="57622-384">CC001</span><span class="sxs-lookup"><span data-stu-id="57622-384">CC001</span></span></td>
<td><span data-ttu-id="57622-385">İK</span><span class="sxs-lookup"><span data-stu-id="57622-385">HR</span></span></td>
<td><span data-ttu-id="57622-386">10001</span><span class="sxs-lookup"><span data-stu-id="57622-386">10001</span></span></td>
<td><span data-ttu-id="57622-387">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-387">Variable cost</span></span></td>
<td><span data-ttu-id="57622-388">1</span><span class="sxs-lookup"><span data-stu-id="57622-388">1</span></span></td>
<td><span data-ttu-id="57622-389">10</span><span class="sxs-lookup"><span data-stu-id="57622-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="57622-390">Aşağıdaki tablo, HR projeleri bir tahsisat tabanı olarak uygulandığındaki sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="57622-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="57622-391">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="57622-391">Cost object</span></span></th>
<th><span data-ttu-id="57622-392">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="57622-392">Magnitude</span></span></th>
<th><span data-ttu-id="57622-393">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="57622-393">Cost element</span></span></th>
<th><span data-ttu-id="57622-394">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="57622-394">Allocation factor</span></span></th>
<th><span data-ttu-id="57622-395">Tutar</span><span class="sxs-lookup"><span data-stu-id="57622-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="57622-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="57622-396">Proj 1</span></span></td>
<td><span data-ttu-id="57622-397">Proje 1</span><span class="sxs-lookup"><span data-stu-id="57622-397">Project 1</span></span></td>
<td><span data-ttu-id="57622-398">3</span><span class="sxs-lookup"><span data-stu-id="57622-398">3</span></span></td>
<td><span data-ttu-id="57622-399">10001</span><span class="sxs-lookup"><span data-stu-id="57622-399">10001</span></span></td>
<td><span data-ttu-id="57622-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="57622-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="57622-401">30.00</span><span class="sxs-lookup"><span data-stu-id="57622-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="57622-402">Proj 2</span></span></td>
<td><span data-ttu-id="57622-403">Proje 2</span><span class="sxs-lookup"><span data-stu-id="57622-403">Project 2</span></span></td>
<td><span data-ttu-id="57622-404">1</span><span class="sxs-lookup"><span data-stu-id="57622-404">1</span></span></td>
<td><span data-ttu-id="57622-405">10001</span><span class="sxs-lookup"><span data-stu-id="57622-405">10001</span></span></td>
<td><span data-ttu-id="57622-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="57622-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="57622-407">10,00</span><span class="sxs-lookup"><span data-stu-id="57622-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="57622-408">Günlük</span><span class="sxs-lookup"><span data-stu-id="57622-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="57622-409">Günlük</span><span class="sxs-lookup"><span data-stu-id="57622-409">Journal</span></span></th>
<th><span data-ttu-id="57622-410">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="57622-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="57622-411">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="57622-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="57622-412">Sürüm</span><span class="sxs-lookup"><span data-stu-id="57622-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="57622-413">00003</span><span class="sxs-lookup"><span data-stu-id="57622-413">00003</span></span></td>
<td><span data-ttu-id="57622-414">Genel gider oranı hesaplaması günlüğü</span><span class="sxs-lookup"><span data-stu-id="57622-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="57622-415">Mali</span><span class="sxs-lookup"><span data-stu-id="57622-415">Fiscal</span></span></td>
<td><span data-ttu-id="57622-416">2017</span><span class="sxs-lookup"><span data-stu-id="57622-416">2017</span></span></td>
<td><span data-ttu-id="57622-417">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="57622-417">Period 1</span></span></td>
<td><span data-ttu-id="57622-418">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="57622-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="57622-419">Günlük girişleri (Genel gider oranı hesaplaması için günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="57622-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="57622-420">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="57622-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="57622-421">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="57622-421">Cost object</span></span></th>
<th><span data-ttu-id="57622-422">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="57622-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="57622-423">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="57622-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="57622-424">Proj 1</span></span></td>
<td><span data-ttu-id="57622-425">Dahili Proj 1</span><span class="sxs-lookup"><span data-stu-id="57622-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="57622-426">3,00</span><span class="sxs-lookup"><span data-stu-id="57622-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-427">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="57622-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="57622-428">Proj 2</span></span></td>
<td><span data-ttu-id="57622-429">Dahili Proj 2</span><span class="sxs-lookup"><span data-stu-id="57622-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="57622-430">1.00</span><span class="sxs-lookup"><span data-stu-id="57622-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="57622-431">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="57622-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="57622-432">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="57622-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="57622-433">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="57622-433">Cost element</span></span></th>
<th><span data-ttu-id="57622-434">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="57622-434">Cost behavior</span></span></th>
<th><span data-ttu-id="57622-435">Tutar</span><span class="sxs-lookup"><span data-stu-id="57622-435">Amount</span></span></th>
<th><span data-ttu-id="57622-436">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="57622-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="57622-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="57622-437">CC0001</span></span></td>
<td><span data-ttu-id="57622-438">İK</span><span class="sxs-lookup"><span data-stu-id="57622-438">HR</span></span></td>
<td><span data-ttu-id="57622-439">10001</span><span class="sxs-lookup"><span data-stu-id="57622-439">10001</span></span></td>
<td><span data-ttu-id="57622-440">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-440">Electricity</span></span></td>
<td><span data-ttu-id="57622-441">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-441">Variable cost</span></span></td>
<td><span data-ttu-id="57622-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="57622-442">-30.00</span></span></td>
<td><span data-ttu-id="57622-443">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="57622-444">Proj 1</span></span></td>
<td><span data-ttu-id="57622-445">Dahili Proj 1</span><span class="sxs-lookup"><span data-stu-id="57622-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="57622-446">10001</span><span class="sxs-lookup"><span data-stu-id="57622-446">10001</span></span></td>
<td><span data-ttu-id="57622-447">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-447">Electricity</span></span></td>
<td><span data-ttu-id="57622-448">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-448">Variable cost</span></span></td>
<td><span data-ttu-id="57622-449">30.00</span><span class="sxs-lookup"><span data-stu-id="57622-449">30.00</span></span></td>
<td><span data-ttu-id="57622-450">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-451">CC001</span><span class="sxs-lookup"><span data-stu-id="57622-451">CC001</span></span></td>
<td><span data-ttu-id="57622-452">İK</span><span class="sxs-lookup"><span data-stu-id="57622-452">HR</span></span></td>
<td><span data-ttu-id="57622-453">10001</span><span class="sxs-lookup"><span data-stu-id="57622-453">10001</span></span></td>
<td><span data-ttu-id="57622-454">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-454">Electricity</span></span></td>
<td><span data-ttu-id="57622-455">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-455">Variable cost</span></span></td>
<td><span data-ttu-id="57622-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="57622-456">-10.00</span></span></td>
<td><span data-ttu-id="57622-457">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="57622-458">Proj 2</span></span></td>
<td><span data-ttu-id="57622-459">Dahili Proj 2</span><span class="sxs-lookup"><span data-stu-id="57622-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="57622-460">10001</span><span class="sxs-lookup"><span data-stu-id="57622-460">10001</span></span></td>
<td><span data-ttu-id="57622-461">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-461">Electricity</span></span></td>
<td><span data-ttu-id="57622-462">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-462">Variable cost</span></span></td>
<td><span data-ttu-id="57622-463">10,00</span><span class="sxs-lookup"><span data-stu-id="57622-463">10.00</span></span></td>
<td><span data-ttu-id="57622-464">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="57622-465">Daha fazla bilgi için [Genel gider hesaplaması gerçekleştir](cost-rollup.md#perform-overhead-calculation) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="57622-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="57622-466">Adım 4: Maliyet tahsisat hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="57622-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="57622-467">Tahsisat, bir tahsisat tabanı kullanarak bir maliyet nesnesinin diğer maliyet nesnelerine bakiyesini tahsis eder.</span><span class="sxs-lookup"><span data-stu-id="57622-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="57622-468">Finance and Operations karşılıklı tahsisat yöntemin destekler.</span><span class="sxs-lookup"><span data-stu-id="57622-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="57622-469">Karşılıklı tahsisat yönteminde, yardımcı maliyet nesnelerinin değiştiği karşılıklı hizmetler tümüyle tanınır.</span><span class="sxs-lookup"><span data-stu-id="57622-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="57622-470">Sistem, tahsisatların doğru gerçekleştireceği sırayı otomatik olarak belirler.</span><span class="sxs-lookup"><span data-stu-id="57622-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="57622-471">Bir maliyet nesnesinin bakiyesi tek bir tahsisat tabanı tarafından tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="57622-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="57622-472">Yeni maliyet nesnesi boyutları arasındaki tahsisatlar ve onların üyeleri desteklenir.</span><span class="sxs-lookup"><span data-stu-id="57622-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="57622-473">Tahsisatın sırası, maliyet kontrol birimi tarafından kontrol edilir.</span><span class="sxs-lookup"><span data-stu-id="57622-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="57622-474">[![Karşılıklı yöntemi](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="57622-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="57622-475">Maliyet tahsisatını tanımla</span><span class="sxs-lookup"><span data-stu-id="57622-475">Define the cost allocation</span></span>

<span data-ttu-id="57622-476">Bir maliyetin akışını nasıl izleyeceğinize dair basit bir örnek aşağıda verilmiştir,</span><span class="sxs-lookup"><span data-stu-id="57622-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="57622-477">Maliyet nesnesi CC001 HR, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="57622-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="57622-478">HR hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="57622-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="57622-479">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="57622-479">Cost object</span></span></th>
<th><span data-ttu-id="57622-480">HR hizmetleri</span><span class="sxs-lookup"><span data-stu-id="57622-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="57622-481">CC002</span><span class="sxs-lookup"><span data-stu-id="57622-481">CC002</span></span></td>
<td><span data-ttu-id="57622-482">Finans</span><span class="sxs-lookup"><span data-stu-id="57622-482">Finance</span></span></td>
<td><span data-ttu-id="57622-483">35</span><span class="sxs-lookup"><span data-stu-id="57622-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-484">CC003</span><span class="sxs-lookup"><span data-stu-id="57622-484">CC003</span></span></td>
<td><span data-ttu-id="57622-485">Montaj</span><span class="sxs-lookup"><span data-stu-id="57622-485">Assembly</span></span></td>
<td><span data-ttu-id="57622-486">55</span><span class="sxs-lookup"><span data-stu-id="57622-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-487">CC004</span><span class="sxs-lookup"><span data-stu-id="57622-487">CC004</span></span></td>
<td><span data-ttu-id="57622-488">Paketleme</span><span class="sxs-lookup"><span data-stu-id="57622-488">Packaging</span></span></td>
<td><span data-ttu-id="57622-489">10</span><span class="sxs-lookup"><span data-stu-id="57622-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="57622-490">Maliyet nesnesi CC002 Finans, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="57622-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="57622-491">Finans hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="57622-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="57622-492">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="57622-492">Cost object</span></span></th>
<th><span data-ttu-id="57622-493">Finans hizmetleri</span><span class="sxs-lookup"><span data-stu-id="57622-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="57622-494">CC003</span><span class="sxs-lookup"><span data-stu-id="57622-494">CC003</span></span></td>
<td><span data-ttu-id="57622-495">Montaj</span><span class="sxs-lookup"><span data-stu-id="57622-495">Assembly</span></span></td>
<td><span data-ttu-id="57622-496">65</span><span class="sxs-lookup"><span data-stu-id="57622-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-497">CC004</span><span class="sxs-lookup"><span data-stu-id="57622-497">CC004</span></span></td>
<td><span data-ttu-id="57622-498">Paketleme</span><span class="sxs-lookup"><span data-stu-id="57622-498">Packaging</span></span></td>
<td><span data-ttu-id="57622-499">35</span><span class="sxs-lookup"><span data-stu-id="57622-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="57622-500">Maliyet nesnesi CC003 Derleme, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="57622-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="57622-501">Derleme hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="57622-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="57622-502">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="57622-502">Cost object</span></span></th>
<th><span data-ttu-id="57622-503">Derleme Hizmetleri (saat)</span><span class="sxs-lookup"><span data-stu-id="57622-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="57622-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="57622-504">Prod 1</span></span></td>
<td><span data-ttu-id="57622-505">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="57622-505">Product 1</span></span></td>
<td><span data-ttu-id="57622-506">60</span><span class="sxs-lookup"><span data-stu-id="57622-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="57622-507">Prod 2</span></span></td>
<td><span data-ttu-id="57622-508">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="57622-508">Product 2</span></span></td>
<td><span data-ttu-id="57622-509">20</span><span class="sxs-lookup"><span data-stu-id="57622-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="57622-510">Maliyet nesnesi CC004 Ambalajlama, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="57622-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="57622-511">Ambalajlama hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="57622-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="57622-512">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="57622-512">Cost object</span></span></th>
<th><span data-ttu-id="57622-513">Ambalajlama hizmetleri (saat)</span><span class="sxs-lookup"><span data-stu-id="57622-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="57622-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="57622-514">Prod 1</span></span></td>
<td><span data-ttu-id="57622-515">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="57622-515">Product 1</span></span></td>
<td><span data-ttu-id="57622-516">80</span><span class="sxs-lookup"><span data-stu-id="57622-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="57622-517">Prod 2</span></span></td>
<td><span data-ttu-id="57622-518">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="57622-518">Product 2</span></span></td>
<td><span data-ttu-id="57622-519">15</span><span class="sxs-lookup"><span data-stu-id="57622-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="57622-520">Finance and Operations'ta, bir ürünün tükettiği üretim saatleri gibi istatistiki ölçümler doğrudan kaynak verisinden alınabilir.</span><span class="sxs-lookup"><span data-stu-id="57622-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="57622-521">Daha fazla bilgi için, [İstatistiksel ölçüm sağlayıcı şablonu](statistical-measure-provider-template.md#statistical-measure-provider-template) bakın.</span><span class="sxs-lookup"><span data-stu-id="57622-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="57622-522">Aşağıdaki tablo, İK hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığında ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="57622-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="57622-523">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="57622-523">Cost object</span></span></th>
<th><span data-ttu-id="57622-524">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="57622-524">Magnitude</span></span></th>
<th><span data-ttu-id="57622-525">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="57622-525">Allocation factor</span></span></th>
<th><span data-ttu-id="57622-526">Tutar</span><span class="sxs-lookup"><span data-stu-id="57622-526">Amount</span></span></th>
<th><span data-ttu-id="57622-527">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="57622-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="57622-528">CC002</span><span class="sxs-lookup"><span data-stu-id="57622-528">CC002</span></span></td>
<td><span data-ttu-id="57622-529">Finans</span><span class="sxs-lookup"><span data-stu-id="57622-529">Finance</span></span></td>
<td><span data-ttu-id="57622-530">35</span><span class="sxs-lookup"><span data-stu-id="57622-530">35</span></span></td>
<td><span data-ttu-id="57622-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="57622-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="57622-532">175.00</span><span class="sxs-lookup"><span data-stu-id="57622-532">175.00</span></span></td>
<td><span data-ttu-id="57622-533">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-534">CC003</span><span class="sxs-lookup"><span data-stu-id="57622-534">CC003</span></span></td>
<td><span data-ttu-id="57622-535">Montaj</span><span class="sxs-lookup"><span data-stu-id="57622-535">Assembly</span></span></td>
<td><span data-ttu-id="57622-536">55</span><span class="sxs-lookup"><span data-stu-id="57622-536">55</span></span></td>
<td><span data-ttu-id="57622-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="57622-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="57622-538">275.00</span><span class="sxs-lookup"><span data-stu-id="57622-538">275.00</span></span></td>
<td><span data-ttu-id="57622-539">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-540">CC004</span><span class="sxs-lookup"><span data-stu-id="57622-540">CC004</span></span></td>
<td><span data-ttu-id="57622-541">Paketleme</span><span class="sxs-lookup"><span data-stu-id="57622-541">Packaging</span></span></td>
<td><span data-ttu-id="57622-542">10</span><span class="sxs-lookup"><span data-stu-id="57622-542">10</span></span></td>
<td><span data-ttu-id="57622-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="57622-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="57622-544">50,00</span><span class="sxs-lookup"><span data-stu-id="57622-544">50.00</span></span></td>
<td><span data-ttu-id="57622-545">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-546">CC002</span><span class="sxs-lookup"><span data-stu-id="57622-546">CC002</span></span></td>
<td><span data-ttu-id="57622-547">Finans</span><span class="sxs-lookup"><span data-stu-id="57622-547">Finance</span></span></td>
<td><span data-ttu-id="57622-548">35</span><span class="sxs-lookup"><span data-stu-id="57622-548">35</span></span></td>
<td><span data-ttu-id="57622-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="57622-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="57622-550">436.00</span><span class="sxs-lookup"><span data-stu-id="57622-550">436.00</span></span></td>
<td><span data-ttu-id="57622-551">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-552">CC003</span><span class="sxs-lookup"><span data-stu-id="57622-552">CC003</span></span></td>
<td><span data-ttu-id="57622-553">Montaj</span><span class="sxs-lookup"><span data-stu-id="57622-553">Assembly</span></span></td>
<td><span data-ttu-id="57622-554">55</span><span class="sxs-lookup"><span data-stu-id="57622-554">55</span></span></td>
<td><span data-ttu-id="57622-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="57622-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="57622-556">685.14</span><span class="sxs-lookup"><span data-stu-id="57622-556">685.14</span></span></td>
<td><span data-ttu-id="57622-557">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-558">CC004</span><span class="sxs-lookup"><span data-stu-id="57622-558">CC004</span></span></td>
<td><span data-ttu-id="57622-559">Paketleme</span><span class="sxs-lookup"><span data-stu-id="57622-559">Packaging</span></span></td>
<td><span data-ttu-id="57622-560">10</span><span class="sxs-lookup"><span data-stu-id="57622-560">10</span></span></td>
<td><span data-ttu-id="57622-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="57622-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="57622-562">124.57</span><span class="sxs-lookup"><span data-stu-id="57622-562">124.57</span></span></td>
<td><span data-ttu-id="57622-563">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="57622-564">Aşağıdaki tablo, Finans hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="57622-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="57622-565">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="57622-565">Cost object</span></span></th>
<th><span data-ttu-id="57622-566">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="57622-566">Magnitude</span></span></th>
<th><span data-ttu-id="57622-567">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="57622-567">Allocation factor</span></span></th>
<th><span data-ttu-id="57622-568">Tutar</span><span class="sxs-lookup"><span data-stu-id="57622-568">Amount</span></span></th>
<th><span data-ttu-id="57622-569">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="57622-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="57622-570">CC003</span><span class="sxs-lookup"><span data-stu-id="57622-570">CC003</span></span></td>
<td><span data-ttu-id="57622-571">Montaj</span><span class="sxs-lookup"><span data-stu-id="57622-571">Assembly</span></span></td>
<td><span data-ttu-id="57622-572">65</span><span class="sxs-lookup"><span data-stu-id="57622-572">65</span></span></td>
<td><span data-ttu-id="57622-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="57622-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="57622-574">438.75</span><span class="sxs-lookup"><span data-stu-id="57622-574">438.75</span></span></td>
<td><span data-ttu-id="57622-575">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-576">CC004</span><span class="sxs-lookup"><span data-stu-id="57622-576">CC004</span></span></td>
<td><span data-ttu-id="57622-577">Paketleme</span><span class="sxs-lookup"><span data-stu-id="57622-577">Packaging</span></span></td>
<td><span data-ttu-id="57622-578">35</span><span class="sxs-lookup"><span data-stu-id="57622-578">35</span></span></td>
<td><span data-ttu-id="57622-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="57622-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="57622-580">236.25</span><span class="sxs-lookup"><span data-stu-id="57622-580">236.25</span></span></td>
<td><span data-ttu-id="57622-581">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-582">CC003</span><span class="sxs-lookup"><span data-stu-id="57622-582">CC003</span></span></td>
<td><span data-ttu-id="57622-583">Montaj</span><span class="sxs-lookup"><span data-stu-id="57622-583">Assembly</span></span></td>
<td><span data-ttu-id="57622-584">65</span><span class="sxs-lookup"><span data-stu-id="57622-584">65</span></span></td>
<td><span data-ttu-id="57622-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="57622-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="57622-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="57622-586">5,297.69</span></span></td>
<td><span data-ttu-id="57622-587">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-588">CC004</span><span class="sxs-lookup"><span data-stu-id="57622-588">CC004</span></span></td>
<td><span data-ttu-id="57622-589">Paketleme</span><span class="sxs-lookup"><span data-stu-id="57622-589">Packaging</span></span></td>
<td><span data-ttu-id="57622-590">35</span><span class="sxs-lookup"><span data-stu-id="57622-590">35</span></span></td>
<td><span data-ttu-id="57622-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="57622-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="57622-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="57622-592">2,852.60</span></span></td>
<td><span data-ttu-id="57622-593">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="57622-594">Aşağıdaki tablo, Derleme hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="57622-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="57622-595">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="57622-595">Cost object</span></span></th>
<th><span data-ttu-id="57622-596">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="57622-596">Magnitude</span></span></th>
<th><span data-ttu-id="57622-597">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="57622-597">Allocation factor</span></span></th>
<th><span data-ttu-id="57622-598">Tutar</span><span class="sxs-lookup"><span data-stu-id="57622-598">Amount</span></span></th>
<th><span data-ttu-id="57622-599">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="57622-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="57622-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="57622-600">Prod 1</span></span></td>
<td><span data-ttu-id="57622-601">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="57622-601">Product 1</span></span></td>
<td><span data-ttu-id="57622-602">60</span><span class="sxs-lookup"><span data-stu-id="57622-602">60</span></span></td>
<td><span data-ttu-id="57622-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="57622-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="57622-604">535.31</span><span class="sxs-lookup"><span data-stu-id="57622-604">535.31</span></span></td>
<td><span data-ttu-id="57622-605">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="57622-606">Prod 2</span></span></td>
<td><span data-ttu-id="57622-607">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="57622-607">Product 2</span></span></td>
<td><span data-ttu-id="57622-608">20</span><span class="sxs-lookup"><span data-stu-id="57622-608">20</span></span></td>
<td><span data-ttu-id="57622-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="57622-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="57622-610">178.44</span><span class="sxs-lookup"><span data-stu-id="57622-610">178.44</span></span></td>
<td><span data-ttu-id="57622-611">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="57622-612">Prod 1</span></span></td>
<td><span data-ttu-id="57622-613">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="57622-613">Product 1</span></span></td>
<td><span data-ttu-id="57622-614">60</span><span class="sxs-lookup"><span data-stu-id="57622-614">60</span></span></td>
<td><span data-ttu-id="57622-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="57622-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="57622-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="57622-616">4,487.12</span></span></td>
<td><span data-ttu-id="57622-617">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="57622-618">Prod 2</span></span></td>
<td><span data-ttu-id="57622-619">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="57622-619">Product 2</span></span></td>
<td><span data-ttu-id="57622-620">20</span><span class="sxs-lookup"><span data-stu-id="57622-620">20</span></span></td>
<td><span data-ttu-id="57622-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="57622-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="57622-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="57622-622">1,495.71</span></span></td>
<td><span data-ttu-id="57622-623">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="57622-624">Aşağıdaki tablo, Paketleme hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="57622-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="57622-625">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="57622-625">Cost object</span></span></th>
<th><span data-ttu-id="57622-626">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="57622-626">Magnitude</span></span></th>
<th><span data-ttu-id="57622-627">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="57622-627">Allocation factor</span></span></th>
<th><span data-ttu-id="57622-628">Tutar</span><span class="sxs-lookup"><span data-stu-id="57622-628">Amount</span></span></th>
<th><span data-ttu-id="57622-629">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="57622-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="57622-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="57622-630">Prod 1</span></span></td>
<td><span data-ttu-id="57622-631">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="57622-631">Product 1</span></span></td>
<td><span data-ttu-id="57622-632">80</span><span class="sxs-lookup"><span data-stu-id="57622-632">80</span></span></td>
<td><span data-ttu-id="57622-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="57622-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="57622-634">241.05</span><span class="sxs-lookup"><span data-stu-id="57622-634">241.05</span></span></td>
<td><span data-ttu-id="57622-635">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="57622-636">Prod 2</span></span></td>
<td><span data-ttu-id="57622-637">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="57622-637">Product 2</span></span></td>
<td><span data-ttu-id="57622-638">15</span><span class="sxs-lookup"><span data-stu-id="57622-638">15</span></span></td>
<td><span data-ttu-id="57622-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="57622-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="57622-640">45.20</span><span class="sxs-lookup"><span data-stu-id="57622-640">45.20</span></span></td>
<td><span data-ttu-id="57622-641">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="57622-642">Prod 1</span></span></td>
<td><span data-ttu-id="57622-643">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="57622-643">Product 1</span></span></td>
<td><span data-ttu-id="57622-644">80</span><span class="sxs-lookup"><span data-stu-id="57622-644">80</span></span></td>
<td><span data-ttu-id="57622-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="57622-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="57622-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="57622-646">2,507.09</span></span></td>
<td><span data-ttu-id="57622-647">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="57622-648">Prod 2</span></span></td>
<td><span data-ttu-id="57622-649">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="57622-649">Product 2</span></span></td>
<td><span data-ttu-id="57622-650">15</span><span class="sxs-lookup"><span data-stu-id="57622-650">15</span></span></td>
<td><span data-ttu-id="57622-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="57622-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="57622-652">470.08</span><span class="sxs-lookup"><span data-stu-id="57622-652">470.08</span></span></td>
<td><span data-ttu-id="57622-653">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="57622-654">Günlük girişleri (maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="57622-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="57622-655">Günlük</span><span class="sxs-lookup"><span data-stu-id="57622-655">Journal</span></span></th>
<th><span data-ttu-id="57622-656">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="57622-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="57622-657">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="57622-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="57622-658">Sürüm</span><span class="sxs-lookup"><span data-stu-id="57622-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="57622-659">00004</span><span class="sxs-lookup"><span data-stu-id="57622-659">00004</span></span></td>
<td><span data-ttu-id="57622-660">Maliyet tahsisatı günlüğü</span><span class="sxs-lookup"><span data-stu-id="57622-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="57622-661">Mali</span><span class="sxs-lookup"><span data-stu-id="57622-661">Fiscal</span></span></td>
<td><span data-ttu-id="57622-662">2017</span><span class="sxs-lookup"><span data-stu-id="57622-662">2017</span></span></td>
<td><span data-ttu-id="57622-663">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="57622-663">Period 1</span></span></td>
<td><span data-ttu-id="57622-664">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="57622-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="57622-665">Günlük satırları</span><span class="sxs-lookup"><span data-stu-id="57622-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="57622-666">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="57622-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="57622-667">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="57622-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="57622-668">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="57622-668">Cost element</span></span></th>
<th><span data-ttu-id="57622-669">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="57622-669">Cost behavior</span></span></th>
<th><span data-ttu-id="57622-670">Tutar</span><span class="sxs-lookup"><span data-stu-id="57622-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="57622-671">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="57622-672">CC001</span><span class="sxs-lookup"><span data-stu-id="57622-672">CC001</span></span></td>
<td><span data-ttu-id="57622-673">İK</span><span class="sxs-lookup"><span data-stu-id="57622-673">HR</span></span></td>
<td><span data-ttu-id="57622-674">10001</span><span class="sxs-lookup"><span data-stu-id="57622-674">10001</span></span></td>
<td><span data-ttu-id="57622-675">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-675">Electricity</span></span></td>
<td><span data-ttu-id="57622-676">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-676">Fixed cost</span></span></td>
<td><span data-ttu-id="57622-677">500.00</span><span class="sxs-lookup"><span data-stu-id="57622-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-678">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="57622-679">CC001</span><span class="sxs-lookup"><span data-stu-id="57622-679">CC001</span></span></td>
<td><span data-ttu-id="57622-680">İK</span><span class="sxs-lookup"><span data-stu-id="57622-680">HR</span></span></td>
<td><span data-ttu-id="57622-681">10001</span><span class="sxs-lookup"><span data-stu-id="57622-681">10001</span></span></td>
<td><span data-ttu-id="57622-682">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-682">Electricity</span></span></td>
<td><span data-ttu-id="57622-683">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-683">Variable cost</span></span></td>
<td><span data-ttu-id="57622-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="57622-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-685">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="57622-686">CC002</span><span class="sxs-lookup"><span data-stu-id="57622-686">CC002</span></span></td>
<td><span data-ttu-id="57622-687">Finans</span><span class="sxs-lookup"><span data-stu-id="57622-687">Finance</span></span></td>
<td><span data-ttu-id="57622-688">10001</span><span class="sxs-lookup"><span data-stu-id="57622-688">10001</span></span></td>
<td><span data-ttu-id="57622-689">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-689">Electricity</span></span></td>
<td><span data-ttu-id="57622-690">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-690">Fixed cost</span></span></td>
<td><span data-ttu-id="57622-691">675.00</span><span class="sxs-lookup"><span data-stu-id="57622-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-692">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="57622-693">CC002</span><span class="sxs-lookup"><span data-stu-id="57622-693">CC002</span></span></td>
<td><span data-ttu-id="57622-694">Finans</span><span class="sxs-lookup"><span data-stu-id="57622-694">Finance</span></span></td>
<td><span data-ttu-id="57622-695">10001</span><span class="sxs-lookup"><span data-stu-id="57622-695">10001</span></span></td>
<td><span data-ttu-id="57622-696">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-696">Electricity</span></span></td>
<td><span data-ttu-id="57622-697">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-697">Variable cost</span></span></td>
<td><span data-ttu-id="57622-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="57622-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-699">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="57622-700">CC003</span><span class="sxs-lookup"><span data-stu-id="57622-700">CC003</span></span></td>
<td><span data-ttu-id="57622-701">Montaj</span><span class="sxs-lookup"><span data-stu-id="57622-701">Assembly</span></span></td>
<td><span data-ttu-id="57622-702">10001</span><span class="sxs-lookup"><span data-stu-id="57622-702">10001</span></span></td>
<td><span data-ttu-id="57622-703">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-703">Electricity</span></span></td>
<td><span data-ttu-id="57622-704">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-704">Fixed cost</span></span></td>
<td><span data-ttu-id="57622-705">713.75</span><span class="sxs-lookup"><span data-stu-id="57622-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-706">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="57622-707">CC003</span><span class="sxs-lookup"><span data-stu-id="57622-707">CC003</span></span></td>
<td><span data-ttu-id="57622-708">Montaj</span><span class="sxs-lookup"><span data-stu-id="57622-708">Assembly</span></span></td>
<td><span data-ttu-id="57622-709">10001</span><span class="sxs-lookup"><span data-stu-id="57622-709">10001</span></span></td>
<td><span data-ttu-id="57622-710">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-710">Electricity</span></span></td>
<td><span data-ttu-id="57622-711">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-711">Variable cost</span></span></td>
<td><span data-ttu-id="57622-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="57622-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-713">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="57622-714">CC003</span><span class="sxs-lookup"><span data-stu-id="57622-714">CC003</span></span></td>
<td><span data-ttu-id="57622-715">Paketleme</span><span class="sxs-lookup"><span data-stu-id="57622-715">Packaging</span></span></td>
<td><span data-ttu-id="57622-716">10001</span><span class="sxs-lookup"><span data-stu-id="57622-716">10001</span></span></td>
<td><span data-ttu-id="57622-717">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-717">Electricity</span></span></td>
<td><span data-ttu-id="57622-718">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-718">Fixed cost</span></span></td>
<td><span data-ttu-id="57622-719">286.25</span><span class="sxs-lookup"><span data-stu-id="57622-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-720">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="57622-721">CC003</span><span class="sxs-lookup"><span data-stu-id="57622-721">CC003</span></span></td>
<td><span data-ttu-id="57622-722">Paketleme</span><span class="sxs-lookup"><span data-stu-id="57622-722">Packaging</span></span></td>
<td><span data-ttu-id="57622-723">10001</span><span class="sxs-lookup"><span data-stu-id="57622-723">10001</span></span></td>
<td><span data-ttu-id="57622-724">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-724">Electricity</span></span></td>
<td><span data-ttu-id="57622-725">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-725">Variable cost</span></span></td>
<td><span data-ttu-id="57622-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="57622-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-727">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="57622-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="57622-728">Prod 1</span></span></td>
<td><span data-ttu-id="57622-729">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="57622-729">Product 1</span></span></td>
<td><span data-ttu-id="57622-730">10001</span><span class="sxs-lookup"><span data-stu-id="57622-730">10001</span></span></td>
<td><span data-ttu-id="57622-731">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-731">Electricity</span></span></td>
<td><span data-ttu-id="57622-732">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-732">Fixed cost</span></span></td>
<td><span data-ttu-id="57622-733">776.36</span><span class="sxs-lookup"><span data-stu-id="57622-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-734">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="57622-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="57622-735">Prod 1</span></span></td>
<td><span data-ttu-id="57622-736">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="57622-736">Product 1</span></span></td>
<td><span data-ttu-id="57622-737">10001</span><span class="sxs-lookup"><span data-stu-id="57622-737">10001</span></span></td>
<td><span data-ttu-id="57622-738">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-738">Electricity</span></span></td>
<td><span data-ttu-id="57622-739">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-739">Variable cost</span></span></td>
<td><span data-ttu-id="57622-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="57622-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-741">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="57622-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="57622-742">Prod 2</span></span></td>
<td><span data-ttu-id="57622-743">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="57622-743">Product 1</span></span></td>
<td><span data-ttu-id="57622-744">10001</span><span class="sxs-lookup"><span data-stu-id="57622-744">10001</span></span></td>
<td><span data-ttu-id="57622-745">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-745">Electricity</span></span></td>
<td><span data-ttu-id="57622-746">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-746">Fixed cost</span></span></td>
<td><span data-ttu-id="57622-747">223.64</span><span class="sxs-lookup"><span data-stu-id="57622-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-748">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="57622-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="57622-749">Prod 2</span></span></td>
<td><span data-ttu-id="57622-750">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="57622-750">Product 1</span></span></td>
<td><span data-ttu-id="57622-751">10001</span><span class="sxs-lookup"><span data-stu-id="57622-751">10001</span></span></td>
<td><span data-ttu-id="57622-752">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-752">Electricity</span></span></td>
<td><span data-ttu-id="57622-753">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-753">Variable cost</span></span></td>
<td><span data-ttu-id="57622-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="57622-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="57622-755">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="57622-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="57622-756">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="57622-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="57622-757">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="57622-757">Cost element</span></span></th>
<th><span data-ttu-id="57622-758">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="57622-758">Cost behavior</span></span></th>
<th><span data-ttu-id="57622-759">Tutar</span><span class="sxs-lookup"><span data-stu-id="57622-759">Amount</span></span></th>
<th><span data-ttu-id="57622-760">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="57622-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="57622-761">CC001</span><span class="sxs-lookup"><span data-stu-id="57622-761">CC001</span></span></td>
<td><span data-ttu-id="57622-762">İK</span><span class="sxs-lookup"><span data-stu-id="57622-762">HR</span></span></td>
<td><span data-ttu-id="57622-763">10001</span><span class="sxs-lookup"><span data-stu-id="57622-763">10001</span></span></td>
<td><span data-ttu-id="57622-764">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-764">Electricity</span></span></td>
<td><span data-ttu-id="57622-765">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-765">Fixed cost</span></span></td>
<td><span data-ttu-id="57622-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="57622-766">-500.00</span></span></td>
<td><span data-ttu-id="57622-767">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-768">CC002</span><span class="sxs-lookup"><span data-stu-id="57622-768">CC002</span></span></td>
<td><span data-ttu-id="57622-769">Finans</span><span class="sxs-lookup"><span data-stu-id="57622-769">Finance</span></span></td>
<td><span data-ttu-id="57622-770">10001</span><span class="sxs-lookup"><span data-stu-id="57622-770">10001</span></span></td>
<td><span data-ttu-id="57622-771">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-771">Electricity</span></span></td>
<td><span data-ttu-id="57622-772">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-772">Fixed cost</span></span></td>
<td><span data-ttu-id="57622-773">175.00</span><span class="sxs-lookup"><span data-stu-id="57622-773">175.00</span></span></td>
<td><span data-ttu-id="57622-774">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-775">CC003</span><span class="sxs-lookup"><span data-stu-id="57622-775">CC003</span></span></td>
<td><span data-ttu-id="57622-776">Montaj</span><span class="sxs-lookup"><span data-stu-id="57622-776">Assembly</span></span></td>
<td><span data-ttu-id="57622-777">10001</span><span class="sxs-lookup"><span data-stu-id="57622-777">10001</span></span></td>
<td><span data-ttu-id="57622-778">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-778">Electricity</span></span></td>
<td><span data-ttu-id="57622-779">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-779">Fixed cost</span></span></td>
<td><span data-ttu-id="57622-780">275.00</span><span class="sxs-lookup"><span data-stu-id="57622-780">275.00</span></span></td>
<td><span data-ttu-id="57622-781">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-782">CC004</span><span class="sxs-lookup"><span data-stu-id="57622-782">CC004</span></span></td>
<td><span data-ttu-id="57622-783">Paketleme</span><span class="sxs-lookup"><span data-stu-id="57622-783">Packaging</span></span></td>
<td><span data-ttu-id="57622-784">10001</span><span class="sxs-lookup"><span data-stu-id="57622-784">10001</span></span></td>
<td><span data-ttu-id="57622-785">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-785">Electricity</span></span></td>
<td><span data-ttu-id="57622-786">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-786">Fixed cost</span></span></td>
<td><span data-ttu-id="57622-787">50,00</span><span class="sxs-lookup"><span data-stu-id="57622-787">50,00</span></span></td>
<td><span data-ttu-id="57622-788">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-789">CC001</span><span class="sxs-lookup"><span data-stu-id="57622-789">CC001</span></span></td>
<td><span data-ttu-id="57622-790">İK</span><span class="sxs-lookup"><span data-stu-id="57622-790">HR</span></span></td>
<td><span data-ttu-id="57622-791">10001</span><span class="sxs-lookup"><span data-stu-id="57622-791">10001</span></span></td>
<td><span data-ttu-id="57622-792">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-792">Electricity</span></span></td>
<td><span data-ttu-id="57622-793">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-793">Variable cost</span></span></td>
<td><span data-ttu-id="57622-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="57622-794">-1,245.71</span></span></td>
<td><span data-ttu-id="57622-795">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-796">CC002</span><span class="sxs-lookup"><span data-stu-id="57622-796">CC002</span></span></td>
<td><span data-ttu-id="57622-797">Finans</span><span class="sxs-lookup"><span data-stu-id="57622-797">Finance</span></span></td>
<td><span data-ttu-id="57622-798">10001</span><span class="sxs-lookup"><span data-stu-id="57622-798">10001</span></span></td>
<td><span data-ttu-id="57622-799">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-799">Electricity</span></span></td>
<td><span data-ttu-id="57622-800">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-800">Variable cost</span></span></td>
<td><span data-ttu-id="57622-801">436.00</span><span class="sxs-lookup"><span data-stu-id="57622-801">436.00</span></span></td>
<td><span data-ttu-id="57622-802">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-803">CC003</span><span class="sxs-lookup"><span data-stu-id="57622-803">CC003</span></span></td>
<td><span data-ttu-id="57622-804">Montaj</span><span class="sxs-lookup"><span data-stu-id="57622-804">Assembly</span></span></td>
<td><span data-ttu-id="57622-805">10001</span><span class="sxs-lookup"><span data-stu-id="57622-805">10001</span></span></td>
<td><span data-ttu-id="57622-806">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-806">Electricity</span></span></td>
<td><span data-ttu-id="57622-807">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-807">Variable cost</span></span></td>
<td><span data-ttu-id="57622-808">685.14</span><span class="sxs-lookup"><span data-stu-id="57622-808">685.14</span></span></td>
<td><span data-ttu-id="57622-809">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-810">CC004</span><span class="sxs-lookup"><span data-stu-id="57622-810">CC004</span></span></td>
<td><span data-ttu-id="57622-811">Paketleme</span><span class="sxs-lookup"><span data-stu-id="57622-811">Packaging</span></span></td>
<td><span data-ttu-id="57622-812">10001</span><span class="sxs-lookup"><span data-stu-id="57622-812">10001</span></span></td>
<td><span data-ttu-id="57622-813">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-813">Electricity</span></span></td>
<td><span data-ttu-id="57622-814">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-814">Variable cost</span></span></td>
<td><span data-ttu-id="57622-815">124.57</span><span class="sxs-lookup"><span data-stu-id="57622-815">124.57</span></span></td>
<td><span data-ttu-id="57622-816">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-817">CC002</span><span class="sxs-lookup"><span data-stu-id="57622-817">CC002</span></span></td>
<td><span data-ttu-id="57622-818">Finans</span><span class="sxs-lookup"><span data-stu-id="57622-818">Finance</span></span></td>
<td><span data-ttu-id="57622-819">10001</span><span class="sxs-lookup"><span data-stu-id="57622-819">10001</span></span></td>
<td><span data-ttu-id="57622-820">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-820">Electricity</span></span></td>
<td><span data-ttu-id="57622-821">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-821">Fixed cost</span></span></td>
<td><span data-ttu-id="57622-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="57622-822">-675.00</span></span></td>
<td><span data-ttu-id="57622-823">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-824">CC003</span><span class="sxs-lookup"><span data-stu-id="57622-824">CC003</span></span></td>
<td><span data-ttu-id="57622-825">Montaj</span><span class="sxs-lookup"><span data-stu-id="57622-825">Assembly</span></span></td>
<td><span data-ttu-id="57622-826">10001</span><span class="sxs-lookup"><span data-stu-id="57622-826">10001</span></span></td>
<td><span data-ttu-id="57622-827">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-827">Electricity</span></span></td>
<td><span data-ttu-id="57622-828">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-828">Fixed cost</span></span></td>
<td><span data-ttu-id="57622-829">438.75</span><span class="sxs-lookup"><span data-stu-id="57622-829">438.75</span></span></td>
<td><span data-ttu-id="57622-830">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-831">CC004</span><span class="sxs-lookup"><span data-stu-id="57622-831">CC004</span></span></td>
<td><span data-ttu-id="57622-832">Paketleme</span><span class="sxs-lookup"><span data-stu-id="57622-832">Packaging</span></span></td>
<td><span data-ttu-id="57622-833">10001</span><span class="sxs-lookup"><span data-stu-id="57622-833">10001</span></span></td>
<td><span data-ttu-id="57622-834">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-834">Electricity</span></span></td>
<td><span data-ttu-id="57622-835">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-835">Fixed cost</span></span></td>
<td><span data-ttu-id="57622-836">236.25</span><span class="sxs-lookup"><span data-stu-id="57622-836">236.25</span></span></td>
<td><span data-ttu-id="57622-837">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-838">CC002</span><span class="sxs-lookup"><span data-stu-id="57622-838">CC002</span></span></td>
<td><span data-ttu-id="57622-839">Finans</span><span class="sxs-lookup"><span data-stu-id="57622-839">Finance</span></span></td>
<td><span data-ttu-id="57622-840">10001</span><span class="sxs-lookup"><span data-stu-id="57622-840">10001</span></span></td>
<td><span data-ttu-id="57622-841">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-841">Electricity</span></span></td>
<td><span data-ttu-id="57622-842">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-842">Variable cost</span></span></td>
<td><span data-ttu-id="57622-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="57622-843">-8,150.29</span></span></td>
<td><span data-ttu-id="57622-844">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-845">CC003</span><span class="sxs-lookup"><span data-stu-id="57622-845">CC003</span></span></td>
<td><span data-ttu-id="57622-846">Montaj</span><span class="sxs-lookup"><span data-stu-id="57622-846">Assembly</span></span></td>
<td><span data-ttu-id="57622-847">10001</span><span class="sxs-lookup"><span data-stu-id="57622-847">10001</span></span></td>
<td><span data-ttu-id="57622-848">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-848">Electricity</span></span></td>
<td><span data-ttu-id="57622-849">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-849">Variable cost</span></span></td>
<td><span data-ttu-id="57622-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="57622-850">5,297.69</span></span></td>
<td><span data-ttu-id="57622-851">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-852">CC004</span><span class="sxs-lookup"><span data-stu-id="57622-852">CC004</span></span></td>
<td><span data-ttu-id="57622-853">Paketleme</span><span class="sxs-lookup"><span data-stu-id="57622-853">Packaging</span></span></td>
<td><span data-ttu-id="57622-854">10001</span><span class="sxs-lookup"><span data-stu-id="57622-854">10001</span></span></td>
<td><span data-ttu-id="57622-855">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-855">Electricity</span></span></td>
<td><span data-ttu-id="57622-856">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-856">Variable cost</span></span></td>
<td><span data-ttu-id="57622-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="57622-857">2,852.60</span></span></td>
<td><span data-ttu-id="57622-858">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-859">CC003</span><span class="sxs-lookup"><span data-stu-id="57622-859">CC003</span></span></td>
<td><span data-ttu-id="57622-860">Montaj</span><span class="sxs-lookup"><span data-stu-id="57622-860">Assembly</span></span></td>
<td><span data-ttu-id="57622-861">10001</span><span class="sxs-lookup"><span data-stu-id="57622-861">10001</span></span></td>
<td><span data-ttu-id="57622-862">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-862">Electricity</span></span></td>
<td><span data-ttu-id="57622-863">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-863">Fixed cost</span></span></td>
<td><span data-ttu-id="57622-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="57622-864">-713.75</span></span></td>
<td><span data-ttu-id="57622-865">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="57622-866">Prod 1</span></span></td>
<td><span data-ttu-id="57622-867">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="57622-867">Product 1</span></span></td>
<td><span data-ttu-id="57622-868">10001</span><span class="sxs-lookup"><span data-stu-id="57622-868">10001</span></span></td>
<td><span data-ttu-id="57622-869">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-869">Electricity</span></span></td>
<td><span data-ttu-id="57622-870">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-870">Fixed cost</span></span></td>
<td><span data-ttu-id="57622-871">535.31</span><span class="sxs-lookup"><span data-stu-id="57622-871">535.31</span></span></td>
<td><span data-ttu-id="57622-872">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="57622-873">Prod 2</span></span></td>
<td><span data-ttu-id="57622-874">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="57622-874">Product 2</span></span></td>
<td><span data-ttu-id="57622-875">10001</span><span class="sxs-lookup"><span data-stu-id="57622-875">10001</span></span></td>
<td><span data-ttu-id="57622-876">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-876">Electricity</span></span></td>
<td><span data-ttu-id="57622-877">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-877">Fixed cost</span></span></td>
<td><span data-ttu-id="57622-878">178.44</span><span class="sxs-lookup"><span data-stu-id="57622-878">178.44</span></span></td>
<td><span data-ttu-id="57622-879">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-880">CC003</span><span class="sxs-lookup"><span data-stu-id="57622-880">CC003</span></span></td>
<td><span data-ttu-id="57622-881">Montaj</span><span class="sxs-lookup"><span data-stu-id="57622-881">Assembly</span></span></td>
<td><span data-ttu-id="57622-882">10001</span><span class="sxs-lookup"><span data-stu-id="57622-882">10001</span></span></td>
<td><span data-ttu-id="57622-883">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-883">Electricity</span></span></td>
<td><span data-ttu-id="57622-884">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-884">Variable cost</span></span></td>
<td><span data-ttu-id="57622-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="57622-885">-5,982.83</span></span></td>
<td><span data-ttu-id="57622-886">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="57622-887">Prod 1</span></span></td>
<td><span data-ttu-id="57622-888">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="57622-888">Product 1</span></span></td>
<td><span data-ttu-id="57622-889">10001</span><span class="sxs-lookup"><span data-stu-id="57622-889">10001</span></span></td>
<td><span data-ttu-id="57622-890">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-890">Electricity</span></span></td>
<td><span data-ttu-id="57622-891">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-891">Variable cost</span></span></td>
<td><span data-ttu-id="57622-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="57622-892">4,487.12</span></span></td>
<td><span data-ttu-id="57622-893">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="57622-894">Prod 2</span></span></td>
<td><span data-ttu-id="57622-895">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="57622-895">Product 2</span></span></td>
<td><span data-ttu-id="57622-896">10001</span><span class="sxs-lookup"><span data-stu-id="57622-896">10001</span></span></td>
<td><span data-ttu-id="57622-897">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-897">Electricity</span></span></td>
<td><span data-ttu-id="57622-898">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-898">Variable cost</span></span></td>
<td><span data-ttu-id="57622-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="57622-899">1,495.71</span></span></td>
<td><span data-ttu-id="57622-900">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-901">CC003</span><span class="sxs-lookup"><span data-stu-id="57622-901">CC003</span></span></td>
<td><span data-ttu-id="57622-902">Montaj</span><span class="sxs-lookup"><span data-stu-id="57622-902">Assembly</span></span></td>
<td><span data-ttu-id="57622-903">10001</span><span class="sxs-lookup"><span data-stu-id="57622-903">10001</span></span></td>
<td><span data-ttu-id="57622-904">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-904">Electricity</span></span></td>
<td><span data-ttu-id="57622-905">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-905">Fixed cost</span></span></td>
<td><span data-ttu-id="57622-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="57622-906">-286.25</span></span></td>
<td><span data-ttu-id="57622-907">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="57622-908">Prod 1</span></span></td>
<td><span data-ttu-id="57622-909">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="57622-909">Product 1</span></span></td>
<td><span data-ttu-id="57622-910">10001</span><span class="sxs-lookup"><span data-stu-id="57622-910">10001</span></span></td>
<td><span data-ttu-id="57622-911">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-911">Electricity</span></span></td>
<td><span data-ttu-id="57622-912">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-912">Fixed cost</span></span></td>
<td><span data-ttu-id="57622-913">241.05</span><span class="sxs-lookup"><span data-stu-id="57622-913">241.05</span></span></td>
<td><span data-ttu-id="57622-914">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="57622-915">Prod 2</span></span></td>
<td><span data-ttu-id="57622-916">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="57622-916">Product 2</span></span></td>
<td><span data-ttu-id="57622-917">10001</span><span class="sxs-lookup"><span data-stu-id="57622-917">10001</span></span></td>
<td><span data-ttu-id="57622-918">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-918">Electricity</span></span></td>
<td><span data-ttu-id="57622-919">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-919">Fixed cost</span></span></td>
<td><span data-ttu-id="57622-920">45.20</span><span class="sxs-lookup"><span data-stu-id="57622-920">45.20</span></span></td>
<td><span data-ttu-id="57622-921">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-922">CC003</span><span class="sxs-lookup"><span data-stu-id="57622-922">CC003</span></span></td>
<td><span data-ttu-id="57622-923">Montaj</span><span class="sxs-lookup"><span data-stu-id="57622-923">Assembly</span></span></td>
<td><span data-ttu-id="57622-924">10001</span><span class="sxs-lookup"><span data-stu-id="57622-924">10001</span></span></td>
<td><span data-ttu-id="57622-925">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-925">Electricity</span></span></td>
<td><span data-ttu-id="57622-926">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-926">Variable cost</span></span></td>
<td><span data-ttu-id="57622-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="57622-927">-2,977.17</span></span></td>
<td><span data-ttu-id="57622-928">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="57622-929">Prod 1</span></span></td>
<td><span data-ttu-id="57622-930">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="57622-930">Product 1</span></span></td>
<td><span data-ttu-id="57622-931">10001</span><span class="sxs-lookup"><span data-stu-id="57622-931">10001</span></span></td>
<td><span data-ttu-id="57622-932">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-932">Electricity</span></span></td>
<td><span data-ttu-id="57622-933">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-933">Variable cost</span></span></td>
<td><span data-ttu-id="57622-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="57622-934">2,507.09</span></span></td>
<td><span data-ttu-id="57622-935">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="57622-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="57622-936">Prod 2</span></span></td>
<td><span data-ttu-id="57622-937">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="57622-937">Product 2</span></span></td>
<td><span data-ttu-id="57622-938">10001</span><span class="sxs-lookup"><span data-stu-id="57622-938">10001</span></span></td>
<td><span data-ttu-id="57622-939">Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-939">Electricity</span></span></td>
<td><span data-ttu-id="57622-940">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-940">Variable cost</span></span></td>
<td><span data-ttu-id="57622-941">470.08</span><span class="sxs-lookup"><span data-stu-id="57622-941">470.08</span></span></td>
<td><span data-ttu-id="57622-942">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="57622-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="57622-943">Sonuç</span><span class="sxs-lookup"><span data-stu-id="57622-943">Conclusion</span></span>
<span data-ttu-id="57622-944">Mali muhasebede, Elektrik için 10.000,00 maliyet bir sözde maliyet merkezi kimliğine nakledilmiştir.</span><span class="sxs-lookup"><span data-stu-id="57622-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="57622-945">Bu nedenle, maliyet muhasebecileri bu maliyetin tahsis edilmesi gerektiğini bilirler.</span><span class="sxs-lookup"><span data-stu-id="57622-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="57622-946">Maliyet muhasebesinde, maliyetler kuruluş birimleri ve seviyeleri arasında, uygulanan kural ve ilkelere dayalı olarak akar.</span><span class="sxs-lookup"><span data-stu-id="57622-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="57622-947">Her maliyet, maliyetlerin tahsisatı için en iyi değerlendirmeyi sağlayan bir tahsisat tabanı ile ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="57622-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="57622-948">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="57622-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="57622-949">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="57622-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="57622-950">Toplam</span><span class="sxs-lookup"><span data-stu-id="57622-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="57622-951">CC099</span><span class="sxs-lookup"><span data-stu-id="57622-951">CC099</span></span></th>
<th><span data-ttu-id="57622-952">CC001</span><span class="sxs-lookup"><span data-stu-id="57622-952">CC001</span></span></th>
<th><span data-ttu-id="57622-953">CC002</span><span class="sxs-lookup"><span data-stu-id="57622-953">CC002</span></span></th>
<th><span data-ttu-id="57622-954">CC003</span><span class="sxs-lookup"><span data-stu-id="57622-954">CC003</span></span></th>
<th><span data-ttu-id="57622-955">CC004</span><span class="sxs-lookup"><span data-stu-id="57622-955">CC004</span></span></th>
<th><span data-ttu-id="57622-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="57622-956">Proj 1</span></span></th>
<th><span data-ttu-id="57622-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="57622-957">Proj 2</span></span></th>
<th><span data-ttu-id="57622-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="57622-958">Prod 1</span></span></th>
<th><span data-ttu-id="57622-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="57622-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="57622-960">10001 Elektrik</span><span class="sxs-lookup"><span data-stu-id="57622-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="57622-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="57622-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="57622-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="57622-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="57622-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="57622-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="57622-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="57622-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="57622-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="57622-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="57622-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="57622-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="57622-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="57622-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="57622-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="57622-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="57622-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="57622-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="57622-970">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="57622-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="57622-971">0,00</span><span class="sxs-lookup"><span data-stu-id="57622-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="57622-972">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="57622-973">0,00</span><span class="sxs-lookup"><span data-stu-id="57622-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="57622-974">0,00</span><span class="sxs-lookup"><span data-stu-id="57622-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="57622-975">0,00</span><span class="sxs-lookup"><span data-stu-id="57622-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="57622-976">0,00</span><span class="sxs-lookup"><span data-stu-id="57622-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="57622-977">0,00</span><span class="sxs-lookup"><span data-stu-id="57622-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="57622-978">776.36</span><span class="sxs-lookup"><span data-stu-id="57622-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="57622-979">223.64</span><span class="sxs-lookup"><span data-stu-id="57622-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="57622-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="57622-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="57622-981">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="57622-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="57622-982">000</span><span class="sxs-lookup"><span data-stu-id="57622-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="57622-983">0,00</span><span class="sxs-lookup"><span data-stu-id="57622-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="57622-984">0,00</span><span class="sxs-lookup"><span data-stu-id="57622-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="57622-985">0,00</span><span class="sxs-lookup"><span data-stu-id="57622-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="57622-986">0,00</span><span class="sxs-lookup"><span data-stu-id="57622-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="57622-987">30.00</span><span class="sxs-lookup"><span data-stu-id="57622-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="57622-988">10,00</span><span class="sxs-lookup"><span data-stu-id="57622-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="57622-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="57622-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="57622-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="57622-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="57622-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="57622-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="57622-992">Bu konu, birincil maliyet öğesi, 10001 Elektrik'in maliyet nesneleri arasında nasıl aktığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="57622-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="57622-993">Bu nedenle, bu genel gider maliyeti kuruluşun en düşük seviyesine tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="57622-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="57622-994">Başka bir deyişle, maliyet en alt düzeydeki maliyet nesnelerine aittir.</span><span class="sxs-lookup"><span data-stu-id="57622-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="57622-995">Maliyetin, maliyet nesneleri arasında görsel bir akışına ihtiyacınız varsa, maliyetin akışını görselleştirmek için maliyet toplamı ilke kurallarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="57622-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="57622-996">Daha fazla bilgi için [Maliyet yukarı yuvarlama](cost-rollup.md) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="57622-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



