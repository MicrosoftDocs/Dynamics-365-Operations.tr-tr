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
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544067"
---
# <a name="overhead-calculation"></a><span data-ttu-id="7c306-103">Genel gider hesaplaması</span><span class="sxs-lookup"><span data-stu-id="7c306-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7c306-104">Bu konu, genel gider maliyetlerinin hesaplanması için tipik işlemleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="7c306-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="7c306-105">Terim tanımı</span><span class="sxs-lookup"><span data-stu-id="7c306-105">Term definition</span></span>
---------------

<span data-ttu-id="7c306-106">Genel gider maliyetleri bir işletmenin çalışması için normalde uygulanan, ancak doğrudan herhangi bir özel iş, faaliyet, ürün veya hizmete ilişkilendirilmemiş olan maliyetlerdir.</span><span class="sxs-lookup"><span data-stu-id="7c306-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="7c306-107">Genel gider maliyetleri kar sağlama faaliyetlerinin oluşturulması için kritik destek sağlar.</span><span class="sxs-lookup"><span data-stu-id="7c306-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="7c306-108">Aşağıda bazı genel gider örnekleri verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="7c306-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="7c306-109">Kira</span><span class="sxs-lookup"><span data-stu-id="7c306-109">Rent</span></span>
-   <span data-ttu-id="7c306-110">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-110">Electricity</span></span>
-   <span data-ttu-id="7c306-111">Yönetim maaşları</span><span class="sxs-lookup"><span data-stu-id="7c306-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="7c306-112">Genel gider hesaplaması genel bakış</span><span class="sxs-lookup"><span data-stu-id="7c306-112">Overhead calculation overview</span></span>
<span data-ttu-id="7c306-113">Genel gider hesaplama, maliyet muhasebesi ilkelerini doğru sırayla çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="7c306-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="7c306-114">Maliyet muhasebesi ilkeleri değiştiyse veya belirli hatalar algılandıysa, genel gider hesaplamasını aynı mali dönem için birden fazla kez yürütebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7c306-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="7c306-115">Her genel gider hesaplaması depolanır ve önceki sürümlerdeki hesaplamaları kıyaslamanıza olanak sağlayan, benzersiz bir sürüm kimliğine sahip olur.</span><span class="sxs-lookup"><span data-stu-id="7c306-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="7c306-116">Genel gider hesaplamasının oluşturduğu maliyet girişleri bir muhasebe tarihi alır.</span><span class="sxs-lookup"><span data-stu-id="7c306-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="7c306-117">Bu muhasebe tarihi, hesaplamada kullanılan mali dönemin bitiş tarihiyle eşleşir.</span><span class="sxs-lookup"><span data-stu-id="7c306-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="7c306-118">Benzersiz sürüm kimliği aşağıdaki öğelerden oluşur:</span><span class="sxs-lookup"><span data-stu-id="7c306-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="7c306-119">Sürüm türü</span><span class="sxs-lookup"><span data-stu-id="7c306-119">Version type</span></span>
-   <span data-ttu-id="7c306-120">Tarih ve saat</span><span class="sxs-lookup"><span data-stu-id="7c306-120">Date and time</span></span>
-   <span data-ttu-id="7c306-121">Maliyet muhasebesi defteri</span><span class="sxs-lookup"><span data-stu-id="7c306-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="7c306-122">Mali yıl</span><span class="sxs-lookup"><span data-stu-id="7c306-122">Fiscal year</span></span>
-   <span data-ttu-id="7c306-123">Mali dönem</span><span class="sxs-lookup"><span data-stu-id="7c306-123">Fiscal period</span></span>

<span data-ttu-id="7c306-124">Genel gider hesaplama, sürümden bağımsız olarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="7c306-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="7c306-125">Bu nedenle, Gerçek sürümden önce Bütçe sürümünü hesaplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7c306-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="7c306-126">Genel gider hesaplama dört adımdan oluşur, aşağıdaki çizimde gösterildiği gibi.</span><span class="sxs-lookup"><span data-stu-id="7c306-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="7c306-127">Her adımda, günlük girişleri olan bir günlük başlığı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7c306-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="7c306-128">Bu günlük başlığı, her hesaplama adımı için giriş verilerini tutar.</span><span class="sxs-lookup"><span data-stu-id="7c306-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="7c306-129">İlkeler ve kurallar her günlük satırına uygulanır ve maliyet girişleri çıkış olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7c306-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="7c306-130">Bu nedenle, her zaman tam izlenebilirliğe sahip olursunuz.</span><span class="sxs-lookup"><span data-stu-id="7c306-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="7c306-131">[![Genel gider hesaplaması](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="7c306-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="7c306-132">Elektrik genel gideri maliyetini hesapla ve tahsis et</span><span class="sxs-lookup"><span data-stu-id="7c306-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="7c306-133">Mali muhasebede, elektrik gibi bazı maliyetler peşin ödeme olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="7c306-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="7c306-134">Bu nedenle, Maliyet muhasebesi için ayrıntılı yönetim bilgiler sağlanmaz.</span><span class="sxs-lookup"><span data-stu-id="7c306-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="7c306-135">Maliyet muhasebesinde doğru yönetimsel bilgileri tüm yönetim birim ve düzeylerinde sağlamak için, maliyetlerin kuruluş birimleri arasında akması gerekir.</span><span class="sxs-lookup"><span data-stu-id="7c306-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="7c306-136">Bu akış, tüketimin doğru bir kaydına ya da adil bir değerlendirmeye dayanıyor olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7c306-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="7c306-137">Genel muhasebede, bir elektrik maliyeti aşağıdaki tabloda gösterildiği gibi deftere nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="7c306-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7c306-138">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="7c306-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7c306-139">Maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="7c306-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="7c306-140">Ana hesap</span><span class="sxs-lookup"><span data-stu-id="7c306-140">Main account</span></span></th>
<th><span data-ttu-id="7c306-141">Muhasebe para birimi cinsinden tutar</span><span class="sxs-lookup"><span data-stu-id="7c306-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7c306-142">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="7c306-143">CC099</span><span class="sxs-lookup"><span data-stu-id="7c306-143">CC099</span></span></td>
<td><span data-ttu-id="7c306-144">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="7c306-144">Default cost center</span></span></td>
<td><span data-ttu-id="7c306-145">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-145">10001</span></span></td>
<td><span data-ttu-id="7c306-146">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-146">Electricity</span></span></td>
<td><span data-ttu-id="7c306-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="7c306-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="7c306-148">Adım 1: Maliyet davranışı hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="7c306-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="7c306-149">Varsayılan olarak, maliyeti girişleri kaynak veriden içeri alındığında, Maliyet muhasebesinde **Sınıflandırılmamış** maliyet davranışı sınıflandırmasını alırlar.</span><span class="sxs-lookup"><span data-stu-id="7c306-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="7c306-150">Maliyet davranışı ilke kuralları ekleyerek, maliyet girişlerini **Sabit maliyet** veya **Değişken maliyet** olarak yeniden sınıflandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7c306-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="7c306-151">Maliyet davranış kuralını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="7c306-151">Define the cost behavior rule</span></span>

<span data-ttu-id="7c306-152">Bazı durumlarda, sabit bir ücret maliyet parçasıdır ve kalan maliyet, tüketime dayanır.</span><span class="sxs-lookup"><span data-stu-id="7c306-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="7c306-153">Elektrik faturaları genellikle bu tanıma uyar.</span><span class="sxs-lookup"><span data-stu-id="7c306-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="7c306-154">Belirli bir sabit ücret ödedikten sonra, kilovat saatlik (Kwh) tüketim başına ödeme yaparsınız.</span><span class="sxs-lookup"><span data-stu-id="7c306-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="7c306-155">Örneğin, sabit maliyet masrafı 1.000,00 ise, maliyet davranışı kural nasıl tanımlanır:</span><span class="sxs-lookup"><span data-stu-id="7c306-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="7c306-156">Sabit tutar 1.000,00</span><span class="sxs-lookup"><span data-stu-id="7c306-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="7c306-157">0 &lt;= 1.000,00 = Sabit</span><span class="sxs-lookup"><span data-stu-id="7c306-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="7c306-158">1000,01 &lt; N = Değişken</span><span class="sxs-lookup"><span data-stu-id="7c306-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="7c306-159">Günlük</span><span class="sxs-lookup"><span data-stu-id="7c306-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7c306-160">Günlük</span><span class="sxs-lookup"><span data-stu-id="7c306-160">Journal</span></span></th>
<th><span data-ttu-id="7c306-161">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="7c306-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="7c306-162">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="7c306-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="7c306-163">Sürüm</span><span class="sxs-lookup"><span data-stu-id="7c306-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7c306-164">00001</span><span class="sxs-lookup"><span data-stu-id="7c306-164">00001</span></span></td>
<td><span data-ttu-id="7c306-165">Maliyet davranışı hesaplama günlüğü</span><span class="sxs-lookup"><span data-stu-id="7c306-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="7c306-166">Mali</span><span class="sxs-lookup"><span data-stu-id="7c306-166">Fiscal</span></span></td>
<td><span data-ttu-id="7c306-167">2017</span><span class="sxs-lookup"><span data-stu-id="7c306-167">2017</span></span></td>
<td><span data-ttu-id="7c306-168">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="7c306-168">Period 1</span></span></td>
<td><span data-ttu-id="7c306-169">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="7c306-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="7c306-170">Günlük girişleri (Maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="7c306-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7c306-171">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="7c306-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7c306-172">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7c306-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7c306-173">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="7c306-173">Cost element</span></span></th>
<th><span data-ttu-id="7c306-174">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="7c306-174">Cost behavior</span></span></th>
<th><span data-ttu-id="7c306-175">Tutar</span><span class="sxs-lookup"><span data-stu-id="7c306-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7c306-176">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="7c306-177">CC099</span><span class="sxs-lookup"><span data-stu-id="7c306-177">CC099</span></span></td>
<td><span data-ttu-id="7c306-178">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="7c306-178">Default cost center</span></span></td>
<td><span data-ttu-id="7c306-179">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-179">10001</span></span></td>
<td><span data-ttu-id="7c306-180">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-180">Electricity</span></span></td>
<td><span data-ttu-id="7c306-181">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="7c306-181">Unclassified</span></span></td>
<td><span data-ttu-id="7c306-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="7c306-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="7c306-183">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="7c306-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7c306-184">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7c306-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7c306-185">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="7c306-185">Cost element</span></span></th>
<th><span data-ttu-id="7c306-186">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="7c306-186">Cost behavior</span></span></th>
<th><span data-ttu-id="7c306-187">Tutar</span><span class="sxs-lookup"><span data-stu-id="7c306-187">Amount</span></span></th>
<th><span data-ttu-id="7c306-188">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="7c306-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7c306-189">CC099</span><span class="sxs-lookup"><span data-stu-id="7c306-189">CC099</span></span></td>
<td><span data-ttu-id="7c306-190">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="7c306-190">Default cost center</span></span></td>
<td><span data-ttu-id="7c306-191">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-191">10001</span></span></td>
<td><span data-ttu-id="7c306-192">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-192">Electricity</span></span></td>
<td><span data-ttu-id="7c306-193">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="7c306-193">Unclassified</span></span></td>
<td><span data-ttu-id="7c306-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="7c306-194">10,000.00</span></span></td>
<td><span data-ttu-id="7c306-195">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-196">CC099</span><span class="sxs-lookup"><span data-stu-id="7c306-196">CC099</span></span></td>
<td><span data-ttu-id="7c306-197">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="7c306-197">Default cost center</span></span></td>
<td><span data-ttu-id="7c306-198">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-198">10001</span></span></td>
<td><span data-ttu-id="7c306-199">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-199">Electricity</span></span></td>
<td><span data-ttu-id="7c306-200">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="7c306-200">Unclassified</span></span></td>
<td><span data-ttu-id="7c306-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="7c306-201">-10,000.00</span></span></td>
<td><span data-ttu-id="7c306-202">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-203">CC099</span><span class="sxs-lookup"><span data-stu-id="7c306-203">CC099</span></span></td>
<td><span data-ttu-id="7c306-204">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="7c306-204">Default cost center</span></span></td>
<td><span data-ttu-id="7c306-205">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-205">10001</span></span></td>
<td><span data-ttu-id="7c306-206">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-206">Electricity</span></span></td>
<td><span data-ttu-id="7c306-207">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-207">Fixed cost</span></span></td>
<td><span data-ttu-id="7c306-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="7c306-208">1,000.00</span></span></td>
<td><span data-ttu-id="7c306-209">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-210">CC099</span><span class="sxs-lookup"><span data-stu-id="7c306-210">CC099</span></span></td>
<td><span data-ttu-id="7c306-211">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="7c306-211">Default cost center</span></span></td>
<td><span data-ttu-id="7c306-212">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-212">10001</span></span></td>
<td><span data-ttu-id="7c306-213">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-213">Electricity</span></span></td>
<td><span data-ttu-id="7c306-214">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-214">Variable cost</span></span></td>
<td><span data-ttu-id="7c306-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="7c306-215">9,000.00</span></span></td>
<td><span data-ttu-id="7c306-216">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7c306-217">Daha fazla bilgi için bkz. [Maliyet davranışı ilkesi oluşturma ve bir maliyet kontrol birimine atama](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="7c306-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="7c306-218">Adım 2: Maliyet dağıtımı hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="7c306-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="7c306-219">Maliyet dağıtımı, bir nesneden bir veya daha fazlasına ilgili tahsisat tabanı uygulayarak maliyeti yeniden dağıtmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7c306-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="7c306-220">Maliyet dağıtımı ve maliyet tahsisatı, maliyet dağıtımının her zaman orijinal maliyetin birincil maliyet öğesinde bulunmasıyla farklılık gösterir.</span><span class="sxs-lookup"><span data-stu-id="7c306-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="7c306-221">Maliyet dağıtım kuralını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="7c306-221">Define the cost distribution rule</span></span>

<span data-ttu-id="7c306-222">Mali muhasebede, elektrik maliyetleri çoğu zaman peşin ödeme olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="7c306-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="7c306-223">Maliyet muhasebesinde ise bu yöntem yeterince ayrıntılı değildir.</span><span class="sxs-lookup"><span data-stu-id="7c306-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="7c306-224">Değişken maliyet, maliyet nesnelerine tek tek, adil bir temele dayanarak dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7c306-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="7c306-225">En mantıklı tahsisat, elektrik kullanımını (Kwh) temel alarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7c306-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="7c306-226">Elektrik adına sahip, istatistiksel bir boyut üyesi oluşturulur ve elektrik tüketimi kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="7c306-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="7c306-227">Varsayıla olarak, tüm istatistiksel boyut üyeleri tahsisat tabanları olarak kullanılabilir hale gelir.</span><span class="sxs-lookup"><span data-stu-id="7c306-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7c306-228">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7c306-228">Cost object</span></span></th>
<th><span data-ttu-id="7c306-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="7c306-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7c306-230">CC001</span><span class="sxs-lookup"><span data-stu-id="7c306-230">CC001</span></span></td>
<td><span data-ttu-id="7c306-231">İK</span><span class="sxs-lookup"><span data-stu-id="7c306-231">HR</span></span></td>
<td><span data-ttu-id="7c306-232">1.000</span><span class="sxs-lookup"><span data-stu-id="7c306-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-233">CC002</span><span class="sxs-lookup"><span data-stu-id="7c306-233">CC002</span></span></td>
<td><span data-ttu-id="7c306-234">Finans</span><span class="sxs-lookup"><span data-stu-id="7c306-234">Finance</span></span></td>
<td><span data-ttu-id="7c306-235">6,000</span><span class="sxs-lookup"><span data-stu-id="7c306-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-236">CC003</span><span class="sxs-lookup"><span data-stu-id="7c306-236">CC003</span></span></td>
<td><span data-ttu-id="7c306-237">Montaj</span><span class="sxs-lookup"><span data-stu-id="7c306-237">Assembly</span></span></td>
<td><span data-ttu-id="7c306-238">0</span><span class="sxs-lookup"><span data-stu-id="7c306-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7c306-239">Aşağıdaki tablo, elektrik tüketiminin değişken maliyetler için bir tahsisat tabanlı olarak uygulandığındaki sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="7c306-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7c306-240">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7c306-240">Cost object</span></span></th>
<th><span data-ttu-id="7c306-241">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="7c306-241">Magnitude</span></span></th>
<th><span data-ttu-id="7c306-242">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="7c306-242">Allocation factor</span></span></th>
<th><span data-ttu-id="7c306-243">Tutar</span><span class="sxs-lookup"><span data-stu-id="7c306-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7c306-244">CC001</span><span class="sxs-lookup"><span data-stu-id="7c306-244">CC001</span></span></td>
<td><span data-ttu-id="7c306-245">İK</span><span class="sxs-lookup"><span data-stu-id="7c306-245">HR</span></span></td>
<td><span data-ttu-id="7c306-246">1.000</span><span class="sxs-lookup"><span data-stu-id="7c306-246">1,000</span></span></td>
<td><span data-ttu-id="7c306-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="7c306-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="7c306-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="7c306-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-249">CC002</span><span class="sxs-lookup"><span data-stu-id="7c306-249">CC002</span></span></td>
<td><span data-ttu-id="7c306-250">Finans</span><span class="sxs-lookup"><span data-stu-id="7c306-250">Finance</span></span></td>
<td><span data-ttu-id="7c306-251">6,000</span><span class="sxs-lookup"><span data-stu-id="7c306-251">6,000</span></span></td>
<td><span data-ttu-id="7c306-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="7c306-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="7c306-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="7c306-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-254">CC003</span><span class="sxs-lookup"><span data-stu-id="7c306-254">CC003</span></span></td>
<td><span data-ttu-id="7c306-255">Montaj</span><span class="sxs-lookup"><span data-stu-id="7c306-255">Assembly</span></span></td>
<td><span data-ttu-id="7c306-256">0</span><span class="sxs-lookup"><span data-stu-id="7c306-256">0</span></span></td>
<td><span data-ttu-id="7c306-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="7c306-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="7c306-258">0,00</span><span class="sxs-lookup"><span data-stu-id="7c306-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7c306-259">Sabit maliyet, elektrik tüketmiş olan tekil maliyet nesnelerine eşit miktarda dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7c306-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="7c306-260">Bu sonuca, Elektrik istatistiksel boyut öğesini bir formül tahsisat tabanında kullanarak ulaşabilirsiniz: (Elektrik &gt; 0,00) Aşağıdaki tablo, elektrik tüketimi değişken maliyetler için bir tahsisat tabanı olarak kullanıldığında ortaya çıkan sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="7c306-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7c306-261">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7c306-261">Cost object</span></span></th>
<th><span data-ttu-id="7c306-262">Formül</span><span class="sxs-lookup"><span data-stu-id="7c306-262">Formula</span></span></th>
<th><span data-ttu-id="7c306-263">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="7c306-263">Magnitude</span></span></th>
<th><span data-ttu-id="7c306-264">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="7c306-264">Allocation factor</span></span></th>
<th><span data-ttu-id="7c306-265">Tutar</span><span class="sxs-lookup"><span data-stu-id="7c306-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7c306-266">CC001</span><span class="sxs-lookup"><span data-stu-id="7c306-266">CC001</span></span></td>
<td><span data-ttu-id="7c306-267">İK</span><span class="sxs-lookup"><span data-stu-id="7c306-267">HR</span></span></td>
<td><span data-ttu-id="7c306-268">(1,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="7c306-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="7c306-269">1</span><span class="sxs-lookup"><span data-stu-id="7c306-269">1</span></span></td>
<td><span data-ttu-id="7c306-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="7c306-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="7c306-271">500.00</span><span class="sxs-lookup"><span data-stu-id="7c306-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-272">CC002</span><span class="sxs-lookup"><span data-stu-id="7c306-272">CC002</span></span></td>
<td><span data-ttu-id="7c306-273">Finans</span><span class="sxs-lookup"><span data-stu-id="7c306-273">Finance</span></span></td>
<td><span data-ttu-id="7c306-274">(6,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="7c306-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="7c306-275">1</span><span class="sxs-lookup"><span data-stu-id="7c306-275">1</span></span></td>
<td><span data-ttu-id="7c306-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="7c306-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="7c306-277">500.00</span><span class="sxs-lookup"><span data-stu-id="7c306-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-278">CC003</span><span class="sxs-lookup"><span data-stu-id="7c306-278">CC003</span></span></td>
<td><span data-ttu-id="7c306-279">Montaj</span><span class="sxs-lookup"><span data-stu-id="7c306-279">Assembly</span></span></td>
<td><span data-ttu-id="7c306-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="7c306-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="7c306-281">0</span><span class="sxs-lookup"><span data-stu-id="7c306-281">0</span></span></td>
<td><span data-ttu-id="7c306-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="7c306-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="7c306-283">0,00</span><span class="sxs-lookup"><span data-stu-id="7c306-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="7c306-284">Günlük</span><span class="sxs-lookup"><span data-stu-id="7c306-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7c306-285">Günlük</span><span class="sxs-lookup"><span data-stu-id="7c306-285">Journal</span></span></th>
<th><span data-ttu-id="7c306-286">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="7c306-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="7c306-287">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="7c306-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="7c306-288">Sürüm</span><span class="sxs-lookup"><span data-stu-id="7c306-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7c306-289">00002</span><span class="sxs-lookup"><span data-stu-id="7c306-289">00002</span></span></td>
<td><span data-ttu-id="7c306-290">Maliyet dağıtımı hesaplama günlüğü</span><span class="sxs-lookup"><span data-stu-id="7c306-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="7c306-291">Mali</span><span class="sxs-lookup"><span data-stu-id="7c306-291">Fiscal</span></span></td>
<td><span data-ttu-id="7c306-292">2017</span><span class="sxs-lookup"><span data-stu-id="7c306-292">2017</span></span></td>
<td><span data-ttu-id="7c306-293">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="7c306-293">Period 1</span></span></td>
<td><span data-ttu-id="7c306-294">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="7c306-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="7c306-295">Günlük girişleri (Maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="7c306-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7c306-296">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="7c306-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7c306-297">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7c306-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7c306-298">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="7c306-298">Cost element</span></span></th>
<th><span data-ttu-id="7c306-299">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="7c306-299">Cost behavior</span></span></th>
<th><span data-ttu-id="7c306-300">Tutar</span><span class="sxs-lookup"><span data-stu-id="7c306-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7c306-301">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="7c306-302">CC099</span><span class="sxs-lookup"><span data-stu-id="7c306-302">CC099</span></span></td>
<td><span data-ttu-id="7c306-303">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="7c306-303">Default cost center</span></span></td>
<td><span data-ttu-id="7c306-304">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-304">10001</span></span></td>
<td><span data-ttu-id="7c306-305">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-305">Electricity</span></span></td>
<td><span data-ttu-id="7c306-306">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-306">Fixed cost</span></span></td>
<td><span data-ttu-id="7c306-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="7c306-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-308">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="7c306-309">CC099</span><span class="sxs-lookup"><span data-stu-id="7c306-309">CC099</span></span></td>
<td><span data-ttu-id="7c306-310">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="7c306-310">Default cost center</span></span></td>
<td><span data-ttu-id="7c306-311">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-311">10001</span></span></td>
<td><span data-ttu-id="7c306-312">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-312">Electricity</span></span></td>
<td><span data-ttu-id="7c306-313">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-313">Variable cost</span></span></td>
<td><span data-ttu-id="7c306-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="7c306-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="7c306-315">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="7c306-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7c306-316">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7c306-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7c306-317">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="7c306-317">Cost element</span></span></th>
<th><span data-ttu-id="7c306-318">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="7c306-318">Cost behavior</span></span></th>
<th><span data-ttu-id="7c306-319">Tutar</span><span class="sxs-lookup"><span data-stu-id="7c306-319">Amount</span></span></th>
<th><span data-ttu-id="7c306-320">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="7c306-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7c306-321">CC099</span><span class="sxs-lookup"><span data-stu-id="7c306-321">CC099</span></span></td>
<td><span data-ttu-id="7c306-322">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="7c306-322">Default cost center</span></span></td>
<td><span data-ttu-id="7c306-323">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-323">10001</span></span></td>
<td><span data-ttu-id="7c306-324">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-324">Electricity</span></span></td>
<td><span data-ttu-id="7c306-325">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-325">Fixed cost</span></span></td>
<td><span data-ttu-id="7c306-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="7c306-326">-1,000.00</span></span></td>
<td><span data-ttu-id="7c306-327">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-328">CC001</span><span class="sxs-lookup"><span data-stu-id="7c306-328">CC001</span></span></td>
<td><span data-ttu-id="7c306-329">İK</span><span class="sxs-lookup"><span data-stu-id="7c306-329">HR</span></span></td>
<td><span data-ttu-id="7c306-330">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-330">10001</span></span></td>
<td><span data-ttu-id="7c306-331">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-331">Electricity</span></span></td>
<td><span data-ttu-id="7c306-332">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-332">Fixed cost</span></span></td>
<td><span data-ttu-id="7c306-333">500.00</span><span class="sxs-lookup"><span data-stu-id="7c306-333">500.00</span></span></td>
<td><span data-ttu-id="7c306-334">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-335">CC002</span><span class="sxs-lookup"><span data-stu-id="7c306-335">CC002</span></span></td>
<td><span data-ttu-id="7c306-336">Finans</span><span class="sxs-lookup"><span data-stu-id="7c306-336">Finance</span></span></td>
<td><span data-ttu-id="7c306-337">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-337">10001</span></span></td>
<td><span data-ttu-id="7c306-338">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-338">Electricity</span></span></td>
<td><span data-ttu-id="7c306-339">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-339">Fixed cost</span></span></td>
<td><span data-ttu-id="7c306-340">500.00</span><span class="sxs-lookup"><span data-stu-id="7c306-340">500.00</span></span></td>
<td><span data-ttu-id="7c306-341">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-342">CC099</span><span class="sxs-lookup"><span data-stu-id="7c306-342">CC099</span></span></td>
<td><span data-ttu-id="7c306-343">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="7c306-343">Default cost center</span></span></td>
<td><span data-ttu-id="7c306-344">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-344">10001</span></span></td>
<td><span data-ttu-id="7c306-345">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-345">Electricity</span></span></td>
<td><span data-ttu-id="7c306-346">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-346">Variable cost</span></span></td>
<td><span data-ttu-id="7c306-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="7c306-347">-9,000.00</span></span></td>
<td><span data-ttu-id="7c306-348">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-349">CC001</span><span class="sxs-lookup"><span data-stu-id="7c306-349">CC001</span></span></td>
<td><span data-ttu-id="7c306-350">İK</span><span class="sxs-lookup"><span data-stu-id="7c306-350">HR</span></span></td>
<td><span data-ttu-id="7c306-351">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-351">10001</span></span></td>
<td><span data-ttu-id="7c306-352">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-352">Electricity</span></span></td>
<td><span data-ttu-id="7c306-353">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-353">Variable cost</span></span></td>
<td><span data-ttu-id="7c306-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="7c306-354">1,285.71</span></span></td>
<td><span data-ttu-id="7c306-355">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-356">CC002</span><span class="sxs-lookup"><span data-stu-id="7c306-356">CC002</span></span></td>
<td><span data-ttu-id="7c306-357">Finans</span><span class="sxs-lookup"><span data-stu-id="7c306-357">Finance</span></span></td>
<td><span data-ttu-id="7c306-358">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-358">10001</span></span></td>
<td><span data-ttu-id="7c306-359">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-359">Electricity</span></span></td>
<td><span data-ttu-id="7c306-360">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-360">Variable cost</span></span></td>
<td><span data-ttu-id="7c306-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="7c306-361">7,714.29</span></span></td>
<td><span data-ttu-id="7c306-362">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7c306-363">Daha fazla bilgi için bkz. [Maliyet dağıtımı ilkesi oluşturma ve bir maliyet kontrol birimine atama](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="7c306-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="7c306-364">Adım 3: Genel gider oranı hesaplama işlemi</span><span class="sxs-lookup"><span data-stu-id="7c306-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="7c306-365">Genel gider oranı, bir veya birden fazla belirli maliyet nesnesine masraf yüklemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7c306-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="7c306-366">Masraf, önceden belirlenmiş maliyet oranına ve tahsisat tabanından hesaplanan büyüklüğe dayanır.</span><span class="sxs-lookup"><span data-stu-id="7c306-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="7c306-367">Genel gider oranını tanımlama</span><span class="sxs-lookup"><span data-stu-id="7c306-367">Define the overhead rate</span></span>

<span data-ttu-id="7c306-368">Maliyet nesnesi CC001 HR, bir dizi dahili projeye katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="7c306-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="7c306-369">HR projeleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7c306-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7c306-370">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7c306-370">Cost object</span></span></th>
<th><span data-ttu-id="7c306-371">Saatler</span><span class="sxs-lookup"><span data-stu-id="7c306-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7c306-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="7c306-372">Proj 1</span></span></td>
<td><span data-ttu-id="7c306-373">Proje 1</span><span class="sxs-lookup"><span data-stu-id="7c306-373">Project 1</span></span></td>
<td><span data-ttu-id="7c306-374">3</span><span class="sxs-lookup"><span data-stu-id="7c306-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="7c306-375">Proj 2</span></span></td>
<td><span data-ttu-id="7c306-376">Proje 2</span><span class="sxs-lookup"><span data-stu-id="7c306-376">Project 2</span></span></td>
<td><span data-ttu-id="7c306-377">1</span><span class="sxs-lookup"><span data-stu-id="7c306-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7c306-378">Maliyet projeleri dağıtımı için bir önceden belirlenmiş maliyet oranı tanımlandı.</span><span class="sxs-lookup"><span data-stu-id="7c306-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7c306-379">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7c306-379">Cost object</span></span></th>
<th><span data-ttu-id="7c306-380">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="7c306-380">Cost element</span></span></th>
<th><span data-ttu-id="7c306-381">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="7c306-381">Cost behavior</span></span></th>
<th><span data-ttu-id="7c306-382">Birimler</span><span class="sxs-lookup"><span data-stu-id="7c306-382">Units</span></span></th>
<th><span data-ttu-id="7c306-383">Ücret</span><span class="sxs-lookup"><span data-stu-id="7c306-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7c306-384">CC001</span><span class="sxs-lookup"><span data-stu-id="7c306-384">CC001</span></span></td>
<td><span data-ttu-id="7c306-385">İK</span><span class="sxs-lookup"><span data-stu-id="7c306-385">HR</span></span></td>
<td><span data-ttu-id="7c306-386">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-386">10001</span></span></td>
<td><span data-ttu-id="7c306-387">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-387">Variable cost</span></span></td>
<td><span data-ttu-id="7c306-388">1</span><span class="sxs-lookup"><span data-stu-id="7c306-388">1</span></span></td>
<td><span data-ttu-id="7c306-389">10</span><span class="sxs-lookup"><span data-stu-id="7c306-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7c306-390">Aşağıdaki tablo, HR projeleri bir tahsisat tabanı olarak uygulandığındaki sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="7c306-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7c306-391">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7c306-391">Cost object</span></span></th>
<th><span data-ttu-id="7c306-392">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="7c306-392">Magnitude</span></span></th>
<th><span data-ttu-id="7c306-393">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="7c306-393">Cost element</span></span></th>
<th><span data-ttu-id="7c306-394">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="7c306-394">Allocation factor</span></span></th>
<th><span data-ttu-id="7c306-395">Tutar</span><span class="sxs-lookup"><span data-stu-id="7c306-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7c306-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="7c306-396">Proj 1</span></span></td>
<td><span data-ttu-id="7c306-397">Proje 1</span><span class="sxs-lookup"><span data-stu-id="7c306-397">Project 1</span></span></td>
<td><span data-ttu-id="7c306-398">3</span><span class="sxs-lookup"><span data-stu-id="7c306-398">3</span></span></td>
<td><span data-ttu-id="7c306-399">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-399">10001</span></span></td>
<td><span data-ttu-id="7c306-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="7c306-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="7c306-401">30.00</span><span class="sxs-lookup"><span data-stu-id="7c306-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="7c306-402">Proj 2</span></span></td>
<td><span data-ttu-id="7c306-403">Proje 2</span><span class="sxs-lookup"><span data-stu-id="7c306-403">Project 2</span></span></td>
<td><span data-ttu-id="7c306-404">1</span><span class="sxs-lookup"><span data-stu-id="7c306-404">1</span></span></td>
<td><span data-ttu-id="7c306-405">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-405">10001</span></span></td>
<td><span data-ttu-id="7c306-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="7c306-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="7c306-407">10,00</span><span class="sxs-lookup"><span data-stu-id="7c306-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="7c306-408">Günlük</span><span class="sxs-lookup"><span data-stu-id="7c306-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7c306-409">Günlük</span><span class="sxs-lookup"><span data-stu-id="7c306-409">Journal</span></span></th>
<th><span data-ttu-id="7c306-410">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="7c306-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="7c306-411">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="7c306-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="7c306-412">Sürüm</span><span class="sxs-lookup"><span data-stu-id="7c306-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7c306-413">00003</span><span class="sxs-lookup"><span data-stu-id="7c306-413">00003</span></span></td>
<td><span data-ttu-id="7c306-414">Genel gider oranı hesaplaması günlüğü</span><span class="sxs-lookup"><span data-stu-id="7c306-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="7c306-415">Mali</span><span class="sxs-lookup"><span data-stu-id="7c306-415">Fiscal</span></span></td>
<td><span data-ttu-id="7c306-416">2017</span><span class="sxs-lookup"><span data-stu-id="7c306-416">2017</span></span></td>
<td><span data-ttu-id="7c306-417">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="7c306-417">Period 1</span></span></td>
<td><span data-ttu-id="7c306-418">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="7c306-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="7c306-419">Günlük girişleri (Genel gider oranı hesaplaması için günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="7c306-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7c306-420">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="7c306-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7c306-421">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7c306-421">Cost object</span></span></th>
<th><span data-ttu-id="7c306-422">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="7c306-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7c306-423">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="7c306-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="7c306-424">Proj 1</span></span></td>
<td><span data-ttu-id="7c306-425">Dahili Proj 1</span><span class="sxs-lookup"><span data-stu-id="7c306-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="7c306-426">3,00</span><span class="sxs-lookup"><span data-stu-id="7c306-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-427">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="7c306-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="7c306-428">Proj 2</span></span></td>
<td><span data-ttu-id="7c306-429">Dahili Proj 2</span><span class="sxs-lookup"><span data-stu-id="7c306-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="7c306-430">1.00</span><span class="sxs-lookup"><span data-stu-id="7c306-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="7c306-431">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="7c306-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7c306-432">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7c306-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7c306-433">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="7c306-433">Cost element</span></span></th>
<th><span data-ttu-id="7c306-434">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="7c306-434">Cost behavior</span></span></th>
<th><span data-ttu-id="7c306-435">Tutar</span><span class="sxs-lookup"><span data-stu-id="7c306-435">Amount</span></span></th>
<th><span data-ttu-id="7c306-436">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="7c306-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7c306-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="7c306-437">CC0001</span></span></td>
<td><span data-ttu-id="7c306-438">İK</span><span class="sxs-lookup"><span data-stu-id="7c306-438">HR</span></span></td>
<td><span data-ttu-id="7c306-439">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-439">10001</span></span></td>
<td><span data-ttu-id="7c306-440">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-440">Electricity</span></span></td>
<td><span data-ttu-id="7c306-441">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-441">Variable cost</span></span></td>
<td><span data-ttu-id="7c306-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="7c306-442">-30.00</span></span></td>
<td><span data-ttu-id="7c306-443">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="7c306-444">Proj 1</span></span></td>
<td><span data-ttu-id="7c306-445">Dahili Proj 1</span><span class="sxs-lookup"><span data-stu-id="7c306-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="7c306-446">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-446">10001</span></span></td>
<td><span data-ttu-id="7c306-447">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-447">Electricity</span></span></td>
<td><span data-ttu-id="7c306-448">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-448">Variable cost</span></span></td>
<td><span data-ttu-id="7c306-449">30.00</span><span class="sxs-lookup"><span data-stu-id="7c306-449">30.00</span></span></td>
<td><span data-ttu-id="7c306-450">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-451">CC001</span><span class="sxs-lookup"><span data-stu-id="7c306-451">CC001</span></span></td>
<td><span data-ttu-id="7c306-452">İK</span><span class="sxs-lookup"><span data-stu-id="7c306-452">HR</span></span></td>
<td><span data-ttu-id="7c306-453">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-453">10001</span></span></td>
<td><span data-ttu-id="7c306-454">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-454">Electricity</span></span></td>
<td><span data-ttu-id="7c306-455">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-455">Variable cost</span></span></td>
<td><span data-ttu-id="7c306-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="7c306-456">-10.00</span></span></td>
<td><span data-ttu-id="7c306-457">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="7c306-458">Proj 2</span></span></td>
<td><span data-ttu-id="7c306-459">Dahili Proj 2</span><span class="sxs-lookup"><span data-stu-id="7c306-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="7c306-460">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-460">10001</span></span></td>
<td><span data-ttu-id="7c306-461">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-461">Electricity</span></span></td>
<td><span data-ttu-id="7c306-462">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-462">Variable cost</span></span></td>
<td><span data-ttu-id="7c306-463">10,00</span><span class="sxs-lookup"><span data-stu-id="7c306-463">10.00</span></span></td>
<td><span data-ttu-id="7c306-464">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7c306-465">Daha fazla bilgi için [Genel gider hesaplaması gerçekleştir](cost-rollup.md#perform-overhead-calculation) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="7c306-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="7c306-466">Adım 4: Maliyet tahsisat hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="7c306-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="7c306-467">Tahsisat, bir tahsisat tabanı kullanarak bir maliyet nesnesinin diğer maliyet nesnelerine bakiyesini tahsis eder.</span><span class="sxs-lookup"><span data-stu-id="7c306-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="7c306-468">Finance and Operations karşılıklı tahsisat yöntemin destekler.</span><span class="sxs-lookup"><span data-stu-id="7c306-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="7c306-469">Karşılıklı tahsisat yönteminde, yardımcı maliyet nesnelerinin değiştiği karşılıklı hizmetler tümüyle tanınır.</span><span class="sxs-lookup"><span data-stu-id="7c306-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="7c306-470">Sistem, tahsisatların doğru gerçekleştireceği sırayı otomatik olarak belirler.</span><span class="sxs-lookup"><span data-stu-id="7c306-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="7c306-471">Bir maliyet nesnesinin bakiyesi tek bir tahsisat tabanı tarafından tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="7c306-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="7c306-472">Yeni maliyet nesnesi boyutları arasındaki tahsisatlar ve onların üyeleri desteklenir.</span><span class="sxs-lookup"><span data-stu-id="7c306-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="7c306-473">Tahsisatın sırası, maliyet kontrol birimi tarafından kontrol edilir.</span><span class="sxs-lookup"><span data-stu-id="7c306-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="7c306-474">[![Karşılıklı yöntemi](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="7c306-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="7c306-475">Maliyet tahsisatını tanımla</span><span class="sxs-lookup"><span data-stu-id="7c306-475">Define the cost allocation</span></span>

<span data-ttu-id="7c306-476">Bir maliyetin akışını nasıl izleyeceğinize dair basit bir örnek aşağıda verilmiştir,</span><span class="sxs-lookup"><span data-stu-id="7c306-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="7c306-477">Maliyet nesnesi CC001 HR, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="7c306-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="7c306-478">HR hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7c306-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7c306-479">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7c306-479">Cost object</span></span></th>
<th><span data-ttu-id="7c306-480">HR hizmetleri</span><span class="sxs-lookup"><span data-stu-id="7c306-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7c306-481">CC002</span><span class="sxs-lookup"><span data-stu-id="7c306-481">CC002</span></span></td>
<td><span data-ttu-id="7c306-482">Finans</span><span class="sxs-lookup"><span data-stu-id="7c306-482">Finance</span></span></td>
<td><span data-ttu-id="7c306-483">35</span><span class="sxs-lookup"><span data-stu-id="7c306-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-484">CC003</span><span class="sxs-lookup"><span data-stu-id="7c306-484">CC003</span></span></td>
<td><span data-ttu-id="7c306-485">Montaj</span><span class="sxs-lookup"><span data-stu-id="7c306-485">Assembly</span></span></td>
<td><span data-ttu-id="7c306-486">55</span><span class="sxs-lookup"><span data-stu-id="7c306-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-487">CC004</span><span class="sxs-lookup"><span data-stu-id="7c306-487">CC004</span></span></td>
<td><span data-ttu-id="7c306-488">Paketleme</span><span class="sxs-lookup"><span data-stu-id="7c306-488">Packaging</span></span></td>
<td><span data-ttu-id="7c306-489">10</span><span class="sxs-lookup"><span data-stu-id="7c306-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7c306-490">Maliyet nesnesi CC002 Finans, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="7c306-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="7c306-491">Finans hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7c306-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7c306-492">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7c306-492">Cost object</span></span></th>
<th><span data-ttu-id="7c306-493">Finans hizmetleri</span><span class="sxs-lookup"><span data-stu-id="7c306-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7c306-494">CC003</span><span class="sxs-lookup"><span data-stu-id="7c306-494">CC003</span></span></td>
<td><span data-ttu-id="7c306-495">Montaj</span><span class="sxs-lookup"><span data-stu-id="7c306-495">Assembly</span></span></td>
<td><span data-ttu-id="7c306-496">65</span><span class="sxs-lookup"><span data-stu-id="7c306-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-497">CC004</span><span class="sxs-lookup"><span data-stu-id="7c306-497">CC004</span></span></td>
<td><span data-ttu-id="7c306-498">Paketleme</span><span class="sxs-lookup"><span data-stu-id="7c306-498">Packaging</span></span></td>
<td><span data-ttu-id="7c306-499">35</span><span class="sxs-lookup"><span data-stu-id="7c306-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7c306-500">Maliyet nesnesi CC003 Derleme, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="7c306-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="7c306-501">Derleme hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7c306-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7c306-502">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7c306-502">Cost object</span></span></th>
<th><span data-ttu-id="7c306-503">Derleme Hizmetleri (saat)</span><span class="sxs-lookup"><span data-stu-id="7c306-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7c306-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7c306-504">Prod 1</span></span></td>
<td><span data-ttu-id="7c306-505">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="7c306-505">Product 1</span></span></td>
<td><span data-ttu-id="7c306-506">60</span><span class="sxs-lookup"><span data-stu-id="7c306-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7c306-507">Prod 2</span></span></td>
<td><span data-ttu-id="7c306-508">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="7c306-508">Product 2</span></span></td>
<td><span data-ttu-id="7c306-509">20</span><span class="sxs-lookup"><span data-stu-id="7c306-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7c306-510">Maliyet nesnesi CC004 Ambalajlama, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="7c306-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="7c306-511">Ambalajlama hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7c306-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7c306-512">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7c306-512">Cost object</span></span></th>
<th><span data-ttu-id="7c306-513">Ambalajlama hizmetleri (saat)</span><span class="sxs-lookup"><span data-stu-id="7c306-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7c306-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7c306-514">Prod 1</span></span></td>
<td><span data-ttu-id="7c306-515">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="7c306-515">Product 1</span></span></td>
<td><span data-ttu-id="7c306-516">80</span><span class="sxs-lookup"><span data-stu-id="7c306-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7c306-517">Prod 2</span></span></td>
<td><span data-ttu-id="7c306-518">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="7c306-518">Product 2</span></span></td>
<td><span data-ttu-id="7c306-519">15</span><span class="sxs-lookup"><span data-stu-id="7c306-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="7c306-520">Finance and Operations'ta, bir ürünün tükettiği üretim saatleri gibi istatistiki ölçümler doğrudan kaynak verisinden alınabilir.</span><span class="sxs-lookup"><span data-stu-id="7c306-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="7c306-521">Daha fazla bilgi için, [İstatistiksel ölçüm sağlayıcı şablonu](statistical-measure-provider-template.md#statistical-measure-provider-template) bakın.</span><span class="sxs-lookup"><span data-stu-id="7c306-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="7c306-522">Aşağıdaki tablo, İK hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığında ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="7c306-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7c306-523">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7c306-523">Cost object</span></span></th>
<th><span data-ttu-id="7c306-524">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="7c306-524">Magnitude</span></span></th>
<th><span data-ttu-id="7c306-525">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="7c306-525">Allocation factor</span></span></th>
<th><span data-ttu-id="7c306-526">Tutar</span><span class="sxs-lookup"><span data-stu-id="7c306-526">Amount</span></span></th>
<th><span data-ttu-id="7c306-527">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="7c306-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7c306-528">CC002</span><span class="sxs-lookup"><span data-stu-id="7c306-528">CC002</span></span></td>
<td><span data-ttu-id="7c306-529">Finans</span><span class="sxs-lookup"><span data-stu-id="7c306-529">Finance</span></span></td>
<td><span data-ttu-id="7c306-530">35</span><span class="sxs-lookup"><span data-stu-id="7c306-530">35</span></span></td>
<td><span data-ttu-id="7c306-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="7c306-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="7c306-532">175.00</span><span class="sxs-lookup"><span data-stu-id="7c306-532">175.00</span></span></td>
<td><span data-ttu-id="7c306-533">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-534">CC003</span><span class="sxs-lookup"><span data-stu-id="7c306-534">CC003</span></span></td>
<td><span data-ttu-id="7c306-535">Montaj</span><span class="sxs-lookup"><span data-stu-id="7c306-535">Assembly</span></span></td>
<td><span data-ttu-id="7c306-536">55</span><span class="sxs-lookup"><span data-stu-id="7c306-536">55</span></span></td>
<td><span data-ttu-id="7c306-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="7c306-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="7c306-538">275.00</span><span class="sxs-lookup"><span data-stu-id="7c306-538">275.00</span></span></td>
<td><span data-ttu-id="7c306-539">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-540">CC004</span><span class="sxs-lookup"><span data-stu-id="7c306-540">CC004</span></span></td>
<td><span data-ttu-id="7c306-541">Paketleme</span><span class="sxs-lookup"><span data-stu-id="7c306-541">Packaging</span></span></td>
<td><span data-ttu-id="7c306-542">10</span><span class="sxs-lookup"><span data-stu-id="7c306-542">10</span></span></td>
<td><span data-ttu-id="7c306-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="7c306-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="7c306-544">50,00</span><span class="sxs-lookup"><span data-stu-id="7c306-544">50.00</span></span></td>
<td><span data-ttu-id="7c306-545">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-546">CC002</span><span class="sxs-lookup"><span data-stu-id="7c306-546">CC002</span></span></td>
<td><span data-ttu-id="7c306-547">Finans</span><span class="sxs-lookup"><span data-stu-id="7c306-547">Finance</span></span></td>
<td><span data-ttu-id="7c306-548">35</span><span class="sxs-lookup"><span data-stu-id="7c306-548">35</span></span></td>
<td><span data-ttu-id="7c306-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="7c306-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="7c306-550">436.00</span><span class="sxs-lookup"><span data-stu-id="7c306-550">436.00</span></span></td>
<td><span data-ttu-id="7c306-551">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-552">CC003</span><span class="sxs-lookup"><span data-stu-id="7c306-552">CC003</span></span></td>
<td><span data-ttu-id="7c306-553">Montaj</span><span class="sxs-lookup"><span data-stu-id="7c306-553">Assembly</span></span></td>
<td><span data-ttu-id="7c306-554">55</span><span class="sxs-lookup"><span data-stu-id="7c306-554">55</span></span></td>
<td><span data-ttu-id="7c306-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="7c306-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="7c306-556">685.14</span><span class="sxs-lookup"><span data-stu-id="7c306-556">685.14</span></span></td>
<td><span data-ttu-id="7c306-557">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-558">CC004</span><span class="sxs-lookup"><span data-stu-id="7c306-558">CC004</span></span></td>
<td><span data-ttu-id="7c306-559">Paketleme</span><span class="sxs-lookup"><span data-stu-id="7c306-559">Packaging</span></span></td>
<td><span data-ttu-id="7c306-560">10</span><span class="sxs-lookup"><span data-stu-id="7c306-560">10</span></span></td>
<td><span data-ttu-id="7c306-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="7c306-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="7c306-562">124.57</span><span class="sxs-lookup"><span data-stu-id="7c306-562">124.57</span></span></td>
<td><span data-ttu-id="7c306-563">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7c306-564">Aşağıdaki tablo, Finans hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="7c306-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7c306-565">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7c306-565">Cost object</span></span></th>
<th><span data-ttu-id="7c306-566">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="7c306-566">Magnitude</span></span></th>
<th><span data-ttu-id="7c306-567">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="7c306-567">Allocation factor</span></span></th>
<th><span data-ttu-id="7c306-568">Tutar</span><span class="sxs-lookup"><span data-stu-id="7c306-568">Amount</span></span></th>
<th><span data-ttu-id="7c306-569">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="7c306-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7c306-570">CC003</span><span class="sxs-lookup"><span data-stu-id="7c306-570">CC003</span></span></td>
<td><span data-ttu-id="7c306-571">Montaj</span><span class="sxs-lookup"><span data-stu-id="7c306-571">Assembly</span></span></td>
<td><span data-ttu-id="7c306-572">65</span><span class="sxs-lookup"><span data-stu-id="7c306-572">65</span></span></td>
<td><span data-ttu-id="7c306-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="7c306-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="7c306-574">438.75</span><span class="sxs-lookup"><span data-stu-id="7c306-574">438.75</span></span></td>
<td><span data-ttu-id="7c306-575">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-576">CC004</span><span class="sxs-lookup"><span data-stu-id="7c306-576">CC004</span></span></td>
<td><span data-ttu-id="7c306-577">Paketleme</span><span class="sxs-lookup"><span data-stu-id="7c306-577">Packaging</span></span></td>
<td><span data-ttu-id="7c306-578">35</span><span class="sxs-lookup"><span data-stu-id="7c306-578">35</span></span></td>
<td><span data-ttu-id="7c306-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="7c306-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="7c306-580">236.25</span><span class="sxs-lookup"><span data-stu-id="7c306-580">236.25</span></span></td>
<td><span data-ttu-id="7c306-581">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-582">CC003</span><span class="sxs-lookup"><span data-stu-id="7c306-582">CC003</span></span></td>
<td><span data-ttu-id="7c306-583">Montaj</span><span class="sxs-lookup"><span data-stu-id="7c306-583">Assembly</span></span></td>
<td><span data-ttu-id="7c306-584">65</span><span class="sxs-lookup"><span data-stu-id="7c306-584">65</span></span></td>
<td><span data-ttu-id="7c306-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="7c306-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="7c306-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="7c306-586">5,297.69</span></span></td>
<td><span data-ttu-id="7c306-587">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-588">CC004</span><span class="sxs-lookup"><span data-stu-id="7c306-588">CC004</span></span></td>
<td><span data-ttu-id="7c306-589">Paketleme</span><span class="sxs-lookup"><span data-stu-id="7c306-589">Packaging</span></span></td>
<td><span data-ttu-id="7c306-590">35</span><span class="sxs-lookup"><span data-stu-id="7c306-590">35</span></span></td>
<td><span data-ttu-id="7c306-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="7c306-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="7c306-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="7c306-592">2,852.60</span></span></td>
<td><span data-ttu-id="7c306-593">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7c306-594">Aşağıdaki tablo, Derleme hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="7c306-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7c306-595">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7c306-595">Cost object</span></span></th>
<th><span data-ttu-id="7c306-596">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="7c306-596">Magnitude</span></span></th>
<th><span data-ttu-id="7c306-597">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="7c306-597">Allocation factor</span></span></th>
<th><span data-ttu-id="7c306-598">Tutar</span><span class="sxs-lookup"><span data-stu-id="7c306-598">Amount</span></span></th>
<th><span data-ttu-id="7c306-599">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="7c306-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7c306-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7c306-600">Prod 1</span></span></td>
<td><span data-ttu-id="7c306-601">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="7c306-601">Product 1</span></span></td>
<td><span data-ttu-id="7c306-602">60</span><span class="sxs-lookup"><span data-stu-id="7c306-602">60</span></span></td>
<td><span data-ttu-id="7c306-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="7c306-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="7c306-604">535.31</span><span class="sxs-lookup"><span data-stu-id="7c306-604">535.31</span></span></td>
<td><span data-ttu-id="7c306-605">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7c306-606">Prod 2</span></span></td>
<td><span data-ttu-id="7c306-607">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="7c306-607">Product 2</span></span></td>
<td><span data-ttu-id="7c306-608">20</span><span class="sxs-lookup"><span data-stu-id="7c306-608">20</span></span></td>
<td><span data-ttu-id="7c306-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="7c306-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="7c306-610">178.44</span><span class="sxs-lookup"><span data-stu-id="7c306-610">178.44</span></span></td>
<td><span data-ttu-id="7c306-611">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7c306-612">Prod 1</span></span></td>
<td><span data-ttu-id="7c306-613">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="7c306-613">Product 1</span></span></td>
<td><span data-ttu-id="7c306-614">60</span><span class="sxs-lookup"><span data-stu-id="7c306-614">60</span></span></td>
<td><span data-ttu-id="7c306-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="7c306-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="7c306-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="7c306-616">4,487.12</span></span></td>
<td><span data-ttu-id="7c306-617">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7c306-618">Prod 2</span></span></td>
<td><span data-ttu-id="7c306-619">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="7c306-619">Product 2</span></span></td>
<td><span data-ttu-id="7c306-620">20</span><span class="sxs-lookup"><span data-stu-id="7c306-620">20</span></span></td>
<td><span data-ttu-id="7c306-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="7c306-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="7c306-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="7c306-622">1,495.71</span></span></td>
<td><span data-ttu-id="7c306-623">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7c306-624">Aşağıdaki tablo, Paketleme hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="7c306-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7c306-625">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7c306-625">Cost object</span></span></th>
<th><span data-ttu-id="7c306-626">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="7c306-626">Magnitude</span></span></th>
<th><span data-ttu-id="7c306-627">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="7c306-627">Allocation factor</span></span></th>
<th><span data-ttu-id="7c306-628">Tutar</span><span class="sxs-lookup"><span data-stu-id="7c306-628">Amount</span></span></th>
<th><span data-ttu-id="7c306-629">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="7c306-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7c306-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7c306-630">Prod 1</span></span></td>
<td><span data-ttu-id="7c306-631">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="7c306-631">Product 1</span></span></td>
<td><span data-ttu-id="7c306-632">80</span><span class="sxs-lookup"><span data-stu-id="7c306-632">80</span></span></td>
<td><span data-ttu-id="7c306-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="7c306-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="7c306-634">241.05</span><span class="sxs-lookup"><span data-stu-id="7c306-634">241.05</span></span></td>
<td><span data-ttu-id="7c306-635">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7c306-636">Prod 2</span></span></td>
<td><span data-ttu-id="7c306-637">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="7c306-637">Product 2</span></span></td>
<td><span data-ttu-id="7c306-638">15</span><span class="sxs-lookup"><span data-stu-id="7c306-638">15</span></span></td>
<td><span data-ttu-id="7c306-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="7c306-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="7c306-640">45.20</span><span class="sxs-lookup"><span data-stu-id="7c306-640">45.20</span></span></td>
<td><span data-ttu-id="7c306-641">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7c306-642">Prod 1</span></span></td>
<td><span data-ttu-id="7c306-643">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="7c306-643">Product 1</span></span></td>
<td><span data-ttu-id="7c306-644">80</span><span class="sxs-lookup"><span data-stu-id="7c306-644">80</span></span></td>
<td><span data-ttu-id="7c306-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="7c306-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="7c306-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="7c306-646">2,507.09</span></span></td>
<td><span data-ttu-id="7c306-647">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7c306-648">Prod 2</span></span></td>
<td><span data-ttu-id="7c306-649">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="7c306-649">Product 2</span></span></td>
<td><span data-ttu-id="7c306-650">15</span><span class="sxs-lookup"><span data-stu-id="7c306-650">15</span></span></td>
<td><span data-ttu-id="7c306-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="7c306-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="7c306-652">470.08</span><span class="sxs-lookup"><span data-stu-id="7c306-652">470.08</span></span></td>
<td><span data-ttu-id="7c306-653">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="7c306-654">Günlük girişleri (maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="7c306-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7c306-655">Günlük</span><span class="sxs-lookup"><span data-stu-id="7c306-655">Journal</span></span></th>
<th><span data-ttu-id="7c306-656">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="7c306-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="7c306-657">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="7c306-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="7c306-658">Sürüm</span><span class="sxs-lookup"><span data-stu-id="7c306-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7c306-659">00004</span><span class="sxs-lookup"><span data-stu-id="7c306-659">00004</span></span></td>
<td><span data-ttu-id="7c306-660">Maliyet tahsisatı günlüğü</span><span class="sxs-lookup"><span data-stu-id="7c306-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="7c306-661">Mali</span><span class="sxs-lookup"><span data-stu-id="7c306-661">Fiscal</span></span></td>
<td><span data-ttu-id="7c306-662">2017</span><span class="sxs-lookup"><span data-stu-id="7c306-662">2017</span></span></td>
<td><span data-ttu-id="7c306-663">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="7c306-663">Period 1</span></span></td>
<td><span data-ttu-id="7c306-664">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="7c306-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="7c306-665">Günlük satırları</span><span class="sxs-lookup"><span data-stu-id="7c306-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7c306-666">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="7c306-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7c306-667">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7c306-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7c306-668">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="7c306-668">Cost element</span></span></th>
<th><span data-ttu-id="7c306-669">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="7c306-669">Cost behavior</span></span></th>
<th><span data-ttu-id="7c306-670">Tutar</span><span class="sxs-lookup"><span data-stu-id="7c306-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7c306-671">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="7c306-672">CC001</span><span class="sxs-lookup"><span data-stu-id="7c306-672">CC001</span></span></td>
<td><span data-ttu-id="7c306-673">İK</span><span class="sxs-lookup"><span data-stu-id="7c306-673">HR</span></span></td>
<td><span data-ttu-id="7c306-674">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-674">10001</span></span></td>
<td><span data-ttu-id="7c306-675">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-675">Electricity</span></span></td>
<td><span data-ttu-id="7c306-676">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-676">Fixed cost</span></span></td>
<td><span data-ttu-id="7c306-677">500.00</span><span class="sxs-lookup"><span data-stu-id="7c306-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-678">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="7c306-679">CC001</span><span class="sxs-lookup"><span data-stu-id="7c306-679">CC001</span></span></td>
<td><span data-ttu-id="7c306-680">İK</span><span class="sxs-lookup"><span data-stu-id="7c306-680">HR</span></span></td>
<td><span data-ttu-id="7c306-681">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-681">10001</span></span></td>
<td><span data-ttu-id="7c306-682">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-682">Electricity</span></span></td>
<td><span data-ttu-id="7c306-683">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-683">Variable cost</span></span></td>
<td><span data-ttu-id="7c306-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="7c306-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-685">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="7c306-686">CC002</span><span class="sxs-lookup"><span data-stu-id="7c306-686">CC002</span></span></td>
<td><span data-ttu-id="7c306-687">Finans</span><span class="sxs-lookup"><span data-stu-id="7c306-687">Finance</span></span></td>
<td><span data-ttu-id="7c306-688">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-688">10001</span></span></td>
<td><span data-ttu-id="7c306-689">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-689">Electricity</span></span></td>
<td><span data-ttu-id="7c306-690">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-690">Fixed cost</span></span></td>
<td><span data-ttu-id="7c306-691">675.00</span><span class="sxs-lookup"><span data-stu-id="7c306-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-692">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="7c306-693">CC002</span><span class="sxs-lookup"><span data-stu-id="7c306-693">CC002</span></span></td>
<td><span data-ttu-id="7c306-694">Finans</span><span class="sxs-lookup"><span data-stu-id="7c306-694">Finance</span></span></td>
<td><span data-ttu-id="7c306-695">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-695">10001</span></span></td>
<td><span data-ttu-id="7c306-696">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-696">Electricity</span></span></td>
<td><span data-ttu-id="7c306-697">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-697">Variable cost</span></span></td>
<td><span data-ttu-id="7c306-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="7c306-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-699">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="7c306-700">CC003</span><span class="sxs-lookup"><span data-stu-id="7c306-700">CC003</span></span></td>
<td><span data-ttu-id="7c306-701">Montaj</span><span class="sxs-lookup"><span data-stu-id="7c306-701">Assembly</span></span></td>
<td><span data-ttu-id="7c306-702">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-702">10001</span></span></td>
<td><span data-ttu-id="7c306-703">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-703">Electricity</span></span></td>
<td><span data-ttu-id="7c306-704">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-704">Fixed cost</span></span></td>
<td><span data-ttu-id="7c306-705">713.75</span><span class="sxs-lookup"><span data-stu-id="7c306-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-706">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="7c306-707">CC003</span><span class="sxs-lookup"><span data-stu-id="7c306-707">CC003</span></span></td>
<td><span data-ttu-id="7c306-708">Montaj</span><span class="sxs-lookup"><span data-stu-id="7c306-708">Assembly</span></span></td>
<td><span data-ttu-id="7c306-709">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-709">10001</span></span></td>
<td><span data-ttu-id="7c306-710">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-710">Electricity</span></span></td>
<td><span data-ttu-id="7c306-711">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-711">Variable cost</span></span></td>
<td><span data-ttu-id="7c306-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="7c306-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-713">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="7c306-714">CC003</span><span class="sxs-lookup"><span data-stu-id="7c306-714">CC003</span></span></td>
<td><span data-ttu-id="7c306-715">Paketleme</span><span class="sxs-lookup"><span data-stu-id="7c306-715">Packaging</span></span></td>
<td><span data-ttu-id="7c306-716">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-716">10001</span></span></td>
<td><span data-ttu-id="7c306-717">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-717">Electricity</span></span></td>
<td><span data-ttu-id="7c306-718">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-718">Fixed cost</span></span></td>
<td><span data-ttu-id="7c306-719">286.25</span><span class="sxs-lookup"><span data-stu-id="7c306-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-720">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="7c306-721">CC003</span><span class="sxs-lookup"><span data-stu-id="7c306-721">CC003</span></span></td>
<td><span data-ttu-id="7c306-722">Paketleme</span><span class="sxs-lookup"><span data-stu-id="7c306-722">Packaging</span></span></td>
<td><span data-ttu-id="7c306-723">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-723">10001</span></span></td>
<td><span data-ttu-id="7c306-724">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-724">Electricity</span></span></td>
<td><span data-ttu-id="7c306-725">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-725">Variable cost</span></span></td>
<td><span data-ttu-id="7c306-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="7c306-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-727">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="7c306-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7c306-728">Prod 1</span></span></td>
<td><span data-ttu-id="7c306-729">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="7c306-729">Product 1</span></span></td>
<td><span data-ttu-id="7c306-730">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-730">10001</span></span></td>
<td><span data-ttu-id="7c306-731">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-731">Electricity</span></span></td>
<td><span data-ttu-id="7c306-732">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-732">Fixed cost</span></span></td>
<td><span data-ttu-id="7c306-733">776.36</span><span class="sxs-lookup"><span data-stu-id="7c306-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-734">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="7c306-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7c306-735">Prod 1</span></span></td>
<td><span data-ttu-id="7c306-736">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="7c306-736">Product 1</span></span></td>
<td><span data-ttu-id="7c306-737">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-737">10001</span></span></td>
<td><span data-ttu-id="7c306-738">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-738">Electricity</span></span></td>
<td><span data-ttu-id="7c306-739">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-739">Variable cost</span></span></td>
<td><span data-ttu-id="7c306-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="7c306-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-741">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="7c306-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7c306-742">Prod 2</span></span></td>
<td><span data-ttu-id="7c306-743">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="7c306-743">Product 1</span></span></td>
<td><span data-ttu-id="7c306-744">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-744">10001</span></span></td>
<td><span data-ttu-id="7c306-745">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-745">Electricity</span></span></td>
<td><span data-ttu-id="7c306-746">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-746">Fixed cost</span></span></td>
<td><span data-ttu-id="7c306-747">223.64</span><span class="sxs-lookup"><span data-stu-id="7c306-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-748">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="7c306-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7c306-749">Prod 2</span></span></td>
<td><span data-ttu-id="7c306-750">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="7c306-750">Product 1</span></span></td>
<td><span data-ttu-id="7c306-751">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-751">10001</span></span></td>
<td><span data-ttu-id="7c306-752">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-752">Electricity</span></span></td>
<td><span data-ttu-id="7c306-753">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-753">Variable cost</span></span></td>
<td><span data-ttu-id="7c306-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="7c306-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="7c306-755">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="7c306-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7c306-756">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7c306-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7c306-757">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="7c306-757">Cost element</span></span></th>
<th><span data-ttu-id="7c306-758">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="7c306-758">Cost behavior</span></span></th>
<th><span data-ttu-id="7c306-759">Tutar</span><span class="sxs-lookup"><span data-stu-id="7c306-759">Amount</span></span></th>
<th><span data-ttu-id="7c306-760">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="7c306-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7c306-761">CC001</span><span class="sxs-lookup"><span data-stu-id="7c306-761">CC001</span></span></td>
<td><span data-ttu-id="7c306-762">İK</span><span class="sxs-lookup"><span data-stu-id="7c306-762">HR</span></span></td>
<td><span data-ttu-id="7c306-763">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-763">10001</span></span></td>
<td><span data-ttu-id="7c306-764">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-764">Electricity</span></span></td>
<td><span data-ttu-id="7c306-765">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-765">Fixed cost</span></span></td>
<td><span data-ttu-id="7c306-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="7c306-766">-500.00</span></span></td>
<td><span data-ttu-id="7c306-767">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-768">CC002</span><span class="sxs-lookup"><span data-stu-id="7c306-768">CC002</span></span></td>
<td><span data-ttu-id="7c306-769">Finans</span><span class="sxs-lookup"><span data-stu-id="7c306-769">Finance</span></span></td>
<td><span data-ttu-id="7c306-770">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-770">10001</span></span></td>
<td><span data-ttu-id="7c306-771">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-771">Electricity</span></span></td>
<td><span data-ttu-id="7c306-772">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-772">Fixed cost</span></span></td>
<td><span data-ttu-id="7c306-773">175.00</span><span class="sxs-lookup"><span data-stu-id="7c306-773">175.00</span></span></td>
<td><span data-ttu-id="7c306-774">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-775">CC003</span><span class="sxs-lookup"><span data-stu-id="7c306-775">CC003</span></span></td>
<td><span data-ttu-id="7c306-776">Montaj</span><span class="sxs-lookup"><span data-stu-id="7c306-776">Assembly</span></span></td>
<td><span data-ttu-id="7c306-777">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-777">10001</span></span></td>
<td><span data-ttu-id="7c306-778">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-778">Electricity</span></span></td>
<td><span data-ttu-id="7c306-779">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-779">Fixed cost</span></span></td>
<td><span data-ttu-id="7c306-780">275.00</span><span class="sxs-lookup"><span data-stu-id="7c306-780">275.00</span></span></td>
<td><span data-ttu-id="7c306-781">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-782">CC004</span><span class="sxs-lookup"><span data-stu-id="7c306-782">CC004</span></span></td>
<td><span data-ttu-id="7c306-783">Paketleme</span><span class="sxs-lookup"><span data-stu-id="7c306-783">Packaging</span></span></td>
<td><span data-ttu-id="7c306-784">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-784">10001</span></span></td>
<td><span data-ttu-id="7c306-785">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-785">Electricity</span></span></td>
<td><span data-ttu-id="7c306-786">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-786">Fixed cost</span></span></td>
<td><span data-ttu-id="7c306-787">50,00</span><span class="sxs-lookup"><span data-stu-id="7c306-787">50,00</span></span></td>
<td><span data-ttu-id="7c306-788">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-789">CC001</span><span class="sxs-lookup"><span data-stu-id="7c306-789">CC001</span></span></td>
<td><span data-ttu-id="7c306-790">İK</span><span class="sxs-lookup"><span data-stu-id="7c306-790">HR</span></span></td>
<td><span data-ttu-id="7c306-791">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-791">10001</span></span></td>
<td><span data-ttu-id="7c306-792">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-792">Electricity</span></span></td>
<td><span data-ttu-id="7c306-793">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-793">Variable cost</span></span></td>
<td><span data-ttu-id="7c306-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="7c306-794">-1,245.71</span></span></td>
<td><span data-ttu-id="7c306-795">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-796">CC002</span><span class="sxs-lookup"><span data-stu-id="7c306-796">CC002</span></span></td>
<td><span data-ttu-id="7c306-797">Finans</span><span class="sxs-lookup"><span data-stu-id="7c306-797">Finance</span></span></td>
<td><span data-ttu-id="7c306-798">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-798">10001</span></span></td>
<td><span data-ttu-id="7c306-799">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-799">Electricity</span></span></td>
<td><span data-ttu-id="7c306-800">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-800">Variable cost</span></span></td>
<td><span data-ttu-id="7c306-801">436.00</span><span class="sxs-lookup"><span data-stu-id="7c306-801">436.00</span></span></td>
<td><span data-ttu-id="7c306-802">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-803">CC003</span><span class="sxs-lookup"><span data-stu-id="7c306-803">CC003</span></span></td>
<td><span data-ttu-id="7c306-804">Montaj</span><span class="sxs-lookup"><span data-stu-id="7c306-804">Assembly</span></span></td>
<td><span data-ttu-id="7c306-805">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-805">10001</span></span></td>
<td><span data-ttu-id="7c306-806">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-806">Electricity</span></span></td>
<td><span data-ttu-id="7c306-807">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-807">Variable cost</span></span></td>
<td><span data-ttu-id="7c306-808">685.14</span><span class="sxs-lookup"><span data-stu-id="7c306-808">685.14</span></span></td>
<td><span data-ttu-id="7c306-809">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-810">CC004</span><span class="sxs-lookup"><span data-stu-id="7c306-810">CC004</span></span></td>
<td><span data-ttu-id="7c306-811">Paketleme</span><span class="sxs-lookup"><span data-stu-id="7c306-811">Packaging</span></span></td>
<td><span data-ttu-id="7c306-812">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-812">10001</span></span></td>
<td><span data-ttu-id="7c306-813">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-813">Electricity</span></span></td>
<td><span data-ttu-id="7c306-814">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-814">Variable cost</span></span></td>
<td><span data-ttu-id="7c306-815">124.57</span><span class="sxs-lookup"><span data-stu-id="7c306-815">124.57</span></span></td>
<td><span data-ttu-id="7c306-816">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-817">CC002</span><span class="sxs-lookup"><span data-stu-id="7c306-817">CC002</span></span></td>
<td><span data-ttu-id="7c306-818">Finans</span><span class="sxs-lookup"><span data-stu-id="7c306-818">Finance</span></span></td>
<td><span data-ttu-id="7c306-819">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-819">10001</span></span></td>
<td><span data-ttu-id="7c306-820">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-820">Electricity</span></span></td>
<td><span data-ttu-id="7c306-821">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-821">Fixed cost</span></span></td>
<td><span data-ttu-id="7c306-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="7c306-822">-675.00</span></span></td>
<td><span data-ttu-id="7c306-823">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-824">CC003</span><span class="sxs-lookup"><span data-stu-id="7c306-824">CC003</span></span></td>
<td><span data-ttu-id="7c306-825">Montaj</span><span class="sxs-lookup"><span data-stu-id="7c306-825">Assembly</span></span></td>
<td><span data-ttu-id="7c306-826">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-826">10001</span></span></td>
<td><span data-ttu-id="7c306-827">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-827">Electricity</span></span></td>
<td><span data-ttu-id="7c306-828">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-828">Fixed cost</span></span></td>
<td><span data-ttu-id="7c306-829">438.75</span><span class="sxs-lookup"><span data-stu-id="7c306-829">438.75</span></span></td>
<td><span data-ttu-id="7c306-830">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-831">CC004</span><span class="sxs-lookup"><span data-stu-id="7c306-831">CC004</span></span></td>
<td><span data-ttu-id="7c306-832">Paketleme</span><span class="sxs-lookup"><span data-stu-id="7c306-832">Packaging</span></span></td>
<td><span data-ttu-id="7c306-833">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-833">10001</span></span></td>
<td><span data-ttu-id="7c306-834">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-834">Electricity</span></span></td>
<td><span data-ttu-id="7c306-835">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-835">Fixed cost</span></span></td>
<td><span data-ttu-id="7c306-836">236.25</span><span class="sxs-lookup"><span data-stu-id="7c306-836">236.25</span></span></td>
<td><span data-ttu-id="7c306-837">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-838">CC002</span><span class="sxs-lookup"><span data-stu-id="7c306-838">CC002</span></span></td>
<td><span data-ttu-id="7c306-839">Finans</span><span class="sxs-lookup"><span data-stu-id="7c306-839">Finance</span></span></td>
<td><span data-ttu-id="7c306-840">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-840">10001</span></span></td>
<td><span data-ttu-id="7c306-841">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-841">Electricity</span></span></td>
<td><span data-ttu-id="7c306-842">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-842">Variable cost</span></span></td>
<td><span data-ttu-id="7c306-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="7c306-843">-8,150.29</span></span></td>
<td><span data-ttu-id="7c306-844">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-845">CC003</span><span class="sxs-lookup"><span data-stu-id="7c306-845">CC003</span></span></td>
<td><span data-ttu-id="7c306-846">Montaj</span><span class="sxs-lookup"><span data-stu-id="7c306-846">Assembly</span></span></td>
<td><span data-ttu-id="7c306-847">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-847">10001</span></span></td>
<td><span data-ttu-id="7c306-848">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-848">Electricity</span></span></td>
<td><span data-ttu-id="7c306-849">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-849">Variable cost</span></span></td>
<td><span data-ttu-id="7c306-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="7c306-850">5,297.69</span></span></td>
<td><span data-ttu-id="7c306-851">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-852">CC004</span><span class="sxs-lookup"><span data-stu-id="7c306-852">CC004</span></span></td>
<td><span data-ttu-id="7c306-853">Paketleme</span><span class="sxs-lookup"><span data-stu-id="7c306-853">Packaging</span></span></td>
<td><span data-ttu-id="7c306-854">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-854">10001</span></span></td>
<td><span data-ttu-id="7c306-855">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-855">Electricity</span></span></td>
<td><span data-ttu-id="7c306-856">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-856">Variable cost</span></span></td>
<td><span data-ttu-id="7c306-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="7c306-857">2,852.60</span></span></td>
<td><span data-ttu-id="7c306-858">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-859">CC003</span><span class="sxs-lookup"><span data-stu-id="7c306-859">CC003</span></span></td>
<td><span data-ttu-id="7c306-860">Montaj</span><span class="sxs-lookup"><span data-stu-id="7c306-860">Assembly</span></span></td>
<td><span data-ttu-id="7c306-861">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-861">10001</span></span></td>
<td><span data-ttu-id="7c306-862">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-862">Electricity</span></span></td>
<td><span data-ttu-id="7c306-863">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-863">Fixed cost</span></span></td>
<td><span data-ttu-id="7c306-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="7c306-864">-713.75</span></span></td>
<td><span data-ttu-id="7c306-865">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7c306-866">Prod 1</span></span></td>
<td><span data-ttu-id="7c306-867">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="7c306-867">Product 1</span></span></td>
<td><span data-ttu-id="7c306-868">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-868">10001</span></span></td>
<td><span data-ttu-id="7c306-869">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-869">Electricity</span></span></td>
<td><span data-ttu-id="7c306-870">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-870">Fixed cost</span></span></td>
<td><span data-ttu-id="7c306-871">535.31</span><span class="sxs-lookup"><span data-stu-id="7c306-871">535.31</span></span></td>
<td><span data-ttu-id="7c306-872">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7c306-873">Prod 2</span></span></td>
<td><span data-ttu-id="7c306-874">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="7c306-874">Product 2</span></span></td>
<td><span data-ttu-id="7c306-875">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-875">10001</span></span></td>
<td><span data-ttu-id="7c306-876">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-876">Electricity</span></span></td>
<td><span data-ttu-id="7c306-877">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-877">Fixed cost</span></span></td>
<td><span data-ttu-id="7c306-878">178.44</span><span class="sxs-lookup"><span data-stu-id="7c306-878">178.44</span></span></td>
<td><span data-ttu-id="7c306-879">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-880">CC003</span><span class="sxs-lookup"><span data-stu-id="7c306-880">CC003</span></span></td>
<td><span data-ttu-id="7c306-881">Montaj</span><span class="sxs-lookup"><span data-stu-id="7c306-881">Assembly</span></span></td>
<td><span data-ttu-id="7c306-882">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-882">10001</span></span></td>
<td><span data-ttu-id="7c306-883">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-883">Electricity</span></span></td>
<td><span data-ttu-id="7c306-884">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-884">Variable cost</span></span></td>
<td><span data-ttu-id="7c306-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="7c306-885">-5,982.83</span></span></td>
<td><span data-ttu-id="7c306-886">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7c306-887">Prod 1</span></span></td>
<td><span data-ttu-id="7c306-888">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="7c306-888">Product 1</span></span></td>
<td><span data-ttu-id="7c306-889">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-889">10001</span></span></td>
<td><span data-ttu-id="7c306-890">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-890">Electricity</span></span></td>
<td><span data-ttu-id="7c306-891">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-891">Variable cost</span></span></td>
<td><span data-ttu-id="7c306-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="7c306-892">4,487.12</span></span></td>
<td><span data-ttu-id="7c306-893">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7c306-894">Prod 2</span></span></td>
<td><span data-ttu-id="7c306-895">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="7c306-895">Product 2</span></span></td>
<td><span data-ttu-id="7c306-896">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-896">10001</span></span></td>
<td><span data-ttu-id="7c306-897">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-897">Electricity</span></span></td>
<td><span data-ttu-id="7c306-898">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-898">Variable cost</span></span></td>
<td><span data-ttu-id="7c306-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="7c306-899">1,495.71</span></span></td>
<td><span data-ttu-id="7c306-900">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-901">CC003</span><span class="sxs-lookup"><span data-stu-id="7c306-901">CC003</span></span></td>
<td><span data-ttu-id="7c306-902">Montaj</span><span class="sxs-lookup"><span data-stu-id="7c306-902">Assembly</span></span></td>
<td><span data-ttu-id="7c306-903">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-903">10001</span></span></td>
<td><span data-ttu-id="7c306-904">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-904">Electricity</span></span></td>
<td><span data-ttu-id="7c306-905">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-905">Fixed cost</span></span></td>
<td><span data-ttu-id="7c306-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="7c306-906">-286.25</span></span></td>
<td><span data-ttu-id="7c306-907">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7c306-908">Prod 1</span></span></td>
<td><span data-ttu-id="7c306-909">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="7c306-909">Product 1</span></span></td>
<td><span data-ttu-id="7c306-910">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-910">10001</span></span></td>
<td><span data-ttu-id="7c306-911">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-911">Electricity</span></span></td>
<td><span data-ttu-id="7c306-912">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-912">Fixed cost</span></span></td>
<td><span data-ttu-id="7c306-913">241.05</span><span class="sxs-lookup"><span data-stu-id="7c306-913">241.05</span></span></td>
<td><span data-ttu-id="7c306-914">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7c306-915">Prod 2</span></span></td>
<td><span data-ttu-id="7c306-916">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="7c306-916">Product 2</span></span></td>
<td><span data-ttu-id="7c306-917">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-917">10001</span></span></td>
<td><span data-ttu-id="7c306-918">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-918">Electricity</span></span></td>
<td><span data-ttu-id="7c306-919">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-919">Fixed cost</span></span></td>
<td><span data-ttu-id="7c306-920">45.20</span><span class="sxs-lookup"><span data-stu-id="7c306-920">45.20</span></span></td>
<td><span data-ttu-id="7c306-921">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-922">CC003</span><span class="sxs-lookup"><span data-stu-id="7c306-922">CC003</span></span></td>
<td><span data-ttu-id="7c306-923">Montaj</span><span class="sxs-lookup"><span data-stu-id="7c306-923">Assembly</span></span></td>
<td><span data-ttu-id="7c306-924">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-924">10001</span></span></td>
<td><span data-ttu-id="7c306-925">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-925">Electricity</span></span></td>
<td><span data-ttu-id="7c306-926">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-926">Variable cost</span></span></td>
<td><span data-ttu-id="7c306-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="7c306-927">-2,977.17</span></span></td>
<td><span data-ttu-id="7c306-928">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7c306-929">Prod 1</span></span></td>
<td><span data-ttu-id="7c306-930">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="7c306-930">Product 1</span></span></td>
<td><span data-ttu-id="7c306-931">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-931">10001</span></span></td>
<td><span data-ttu-id="7c306-932">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-932">Electricity</span></span></td>
<td><span data-ttu-id="7c306-933">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-933">Variable cost</span></span></td>
<td><span data-ttu-id="7c306-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="7c306-934">2,507.09</span></span></td>
<td><span data-ttu-id="7c306-935">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7c306-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7c306-936">Prod 2</span></span></td>
<td><span data-ttu-id="7c306-937">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="7c306-937">Product 2</span></span></td>
<td><span data-ttu-id="7c306-938">10001</span><span class="sxs-lookup"><span data-stu-id="7c306-938">10001</span></span></td>
<td><span data-ttu-id="7c306-939">Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-939">Electricity</span></span></td>
<td><span data-ttu-id="7c306-940">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-940">Variable cost</span></span></td>
<td><span data-ttu-id="7c306-941">470.08</span><span class="sxs-lookup"><span data-stu-id="7c306-941">470.08</span></span></td>
<td><span data-ttu-id="7c306-942">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="7c306-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="7c306-943">Sonuç</span><span class="sxs-lookup"><span data-stu-id="7c306-943">Conclusion</span></span>
<span data-ttu-id="7c306-944">Mali muhasebede, Elektrik için 10.000,00 maliyet bir sözde maliyet merkezi kimliğine nakledilmiştir.</span><span class="sxs-lookup"><span data-stu-id="7c306-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="7c306-945">Bu nedenle, maliyet muhasebecileri bu maliyetin tahsis edilmesi gerektiğini bilirler.</span><span class="sxs-lookup"><span data-stu-id="7c306-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="7c306-946">Maliyet muhasebesinde, maliyetler kuruluş birimleri ve seviyeleri arasında, uygulanan kural ve ilkelere dayalı olarak akar.</span><span class="sxs-lookup"><span data-stu-id="7c306-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="7c306-947">Her maliyet, maliyetlerin tahsisatı için en iyi değerlendirmeyi sağlayan bir tahsisat tabanı ile ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="7c306-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="7c306-948">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="7c306-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="7c306-949">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="7c306-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="7c306-950">Toplam</span><span class="sxs-lookup"><span data-stu-id="7c306-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="7c306-951">CC099</span><span class="sxs-lookup"><span data-stu-id="7c306-951">CC099</span></span></th>
<th><span data-ttu-id="7c306-952">CC001</span><span class="sxs-lookup"><span data-stu-id="7c306-952">CC001</span></span></th>
<th><span data-ttu-id="7c306-953">CC002</span><span class="sxs-lookup"><span data-stu-id="7c306-953">CC002</span></span></th>
<th><span data-ttu-id="7c306-954">CC003</span><span class="sxs-lookup"><span data-stu-id="7c306-954">CC003</span></span></th>
<th><span data-ttu-id="7c306-955">CC004</span><span class="sxs-lookup"><span data-stu-id="7c306-955">CC004</span></span></th>
<th><span data-ttu-id="7c306-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="7c306-956">Proj 1</span></span></th>
<th><span data-ttu-id="7c306-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="7c306-957">Proj 2</span></span></th>
<th><span data-ttu-id="7c306-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="7c306-958">Prod 1</span></span></th>
<th><span data-ttu-id="7c306-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="7c306-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="7c306-960">10001 Elektrik</span><span class="sxs-lookup"><span data-stu-id="7c306-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7c306-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="7c306-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7c306-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="7c306-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7c306-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="7c306-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7c306-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="7c306-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="7c306-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="7c306-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7c306-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="7c306-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7c306-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="7c306-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7c306-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="7c306-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7c306-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="7c306-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="7c306-970">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="7c306-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7c306-971">0,00</span><span class="sxs-lookup"><span data-stu-id="7c306-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="7c306-972">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7c306-973">0,00</span><span class="sxs-lookup"><span data-stu-id="7c306-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7c306-974">0,00</span><span class="sxs-lookup"><span data-stu-id="7c306-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7c306-975">0,00</span><span class="sxs-lookup"><span data-stu-id="7c306-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7c306-976">0,00</span><span class="sxs-lookup"><span data-stu-id="7c306-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7c306-977">0,00</span><span class="sxs-lookup"><span data-stu-id="7c306-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="7c306-978">776.36</span><span class="sxs-lookup"><span data-stu-id="7c306-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7c306-979">223.64</span><span class="sxs-lookup"><span data-stu-id="7c306-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7c306-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="7c306-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="7c306-981">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="7c306-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7c306-982">000</span><span class="sxs-lookup"><span data-stu-id="7c306-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7c306-983">0,00</span><span class="sxs-lookup"><span data-stu-id="7c306-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7c306-984">0,00</span><span class="sxs-lookup"><span data-stu-id="7c306-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7c306-985">0,00</span><span class="sxs-lookup"><span data-stu-id="7c306-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7c306-986">0,00</span><span class="sxs-lookup"><span data-stu-id="7c306-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7c306-987">30.00</span><span class="sxs-lookup"><span data-stu-id="7c306-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7c306-988">10,00</span><span class="sxs-lookup"><span data-stu-id="7c306-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7c306-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="7c306-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7c306-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="7c306-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7c306-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="7c306-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="7c306-992">Bu konu, birincil maliyet öğesi, 10001 Elektrik'in maliyet nesneleri arasında nasıl aktığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7c306-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="7c306-993">Bu nedenle, bu genel gider maliyeti kuruluşun en düşük seviyesine tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="7c306-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="7c306-994">Başka bir deyişle, maliyet en alt düzeydeki maliyet nesnelerine aittir.</span><span class="sxs-lookup"><span data-stu-id="7c306-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="7c306-995">Maliyetin, maliyet nesneleri arasında görsel bir akışına ihtiyacınız varsa, maliyetin akışını görselleştirmek için maliyet toplamı ilke kurallarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7c306-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="7c306-996">Daha fazla bilgi için [Maliyet yukarı yuvarlama](cost-rollup.md) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="7c306-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



