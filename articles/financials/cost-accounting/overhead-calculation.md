---
title: "Genel gider hesaplaması"
description: "Bu konu, genel gider maliyetlerinin hesaplanması için tipik işlemleri açıklar."
author: AndersGirke
manager: AnnBe
ms.date: 10/04/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 12ae99c15bafcd9cc08b30903fe3f251f446b17d
ms.openlocfilehash: 4de705324ac497cfb11fae3dadc6f57d038fd0b5
ms.contentlocale: tr-tr
ms.lasthandoff: 10/05/2018

---

# <a name="overhead-calculation"></a><span data-ttu-id="c72d4-103">Genel gider hesaplaması</span><span class="sxs-lookup"><span data-stu-id="c72d4-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c72d4-104">Bu konu, genel gider maliyetlerinin hesaplanması için tipik işlemleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="c72d4-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="c72d4-105">Terim tanımı</span><span class="sxs-lookup"><span data-stu-id="c72d4-105">Term definition</span></span>
---------------

<span data-ttu-id="c72d4-106">Genel gider maliyetleri bir işletmenin çalışması için normalde uygulanan, ancak doğrudan herhangi bir özel iş, faaliyet, ürün veya hizmete ilişkilendirilmemiş olan maliyetlerdir.</span><span class="sxs-lookup"><span data-stu-id="c72d4-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="c72d4-107">Genel gider maliyetleri kar sağlama faaliyetlerinin oluşturulması için kritik destek sağlar.</span><span class="sxs-lookup"><span data-stu-id="c72d4-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="c72d4-108">Aşağıda bazı genel gider örnekleri verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="c72d4-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="c72d4-109">Kira</span><span class="sxs-lookup"><span data-stu-id="c72d4-109">Rent</span></span>
-   <span data-ttu-id="c72d4-110">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-110">Electricity</span></span>
-   <span data-ttu-id="c72d4-111">Yönetim maaşları</span><span class="sxs-lookup"><span data-stu-id="c72d4-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="c72d4-112">Genel gider hesaplaması genel bakış</span><span class="sxs-lookup"><span data-stu-id="c72d4-112">Overhead calculation overview</span></span>
<span data-ttu-id="c72d4-113">Genel gider hesaplama, maliyet muhasebesi ilkelerini doğru sırayla çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="c72d4-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="c72d4-114">Maliyet muhasebesi ilkeleri değiştiyse veya belirli hatalar algılandıysa, genel gider hesaplamasını aynı mali dönem için birden fazla kez yürütebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c72d4-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="c72d4-115">Her genel gider hesaplaması depolanır ve önceki sürümlerdeki hesaplamaları kıyaslamanıza olanak sağlayan, benzersiz bir sürüm kimliğine sahip olur.</span><span class="sxs-lookup"><span data-stu-id="c72d4-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="c72d4-116">Genel gider hesaplamasının oluşturduğu maliyet girişleri bir muhasebe tarihi alır.</span><span class="sxs-lookup"><span data-stu-id="c72d4-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="c72d4-117">Bu muhasebe tarihi, hesaplamada kullanılan mali dönemin bitiş tarihiyle eşleşir.</span><span class="sxs-lookup"><span data-stu-id="c72d4-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="c72d4-118">Benzersiz sürüm kimliği aşağıdaki öğelerden oluşur:</span><span class="sxs-lookup"><span data-stu-id="c72d4-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="c72d4-119">Sürüm türü</span><span class="sxs-lookup"><span data-stu-id="c72d4-119">Version type</span></span>
-   <span data-ttu-id="c72d4-120">Tarih ve saat</span><span class="sxs-lookup"><span data-stu-id="c72d4-120">Date and time</span></span>
-   <span data-ttu-id="c72d4-121">Maliyet muhasebesi defteri</span><span class="sxs-lookup"><span data-stu-id="c72d4-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="c72d4-122">Mali yıl</span><span class="sxs-lookup"><span data-stu-id="c72d4-122">Fiscal year</span></span>
-   <span data-ttu-id="c72d4-123">Mali dönem</span><span class="sxs-lookup"><span data-stu-id="c72d4-123">Fiscal period</span></span>

<span data-ttu-id="c72d4-124">Genel gider hesaplama, sürümden bağımsız olarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="c72d4-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="c72d4-125">Bu nedenle, Gerçek sürümden önce Bütçe sürümünü hesaplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c72d4-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="c72d4-126">Genel gider hesaplama dört adımdan oluşur, aşağıdaki çizimde gösterildiği gibi.</span><span class="sxs-lookup"><span data-stu-id="c72d4-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="c72d4-127">Her adımda, günlük girişleri olan bir günlük başlığı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c72d4-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="c72d4-128">Bu günlük başlığı, her hesaplama adımı için giriş verilerini tutar.</span><span class="sxs-lookup"><span data-stu-id="c72d4-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="c72d4-129">İlkeler ve kurallar her günlük satırına uygulanır ve maliyet girişleri çıkış olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c72d4-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="c72d4-130">Bu nedenle, her zaman tam izlenebilirliğe sahip olursunuz.</span><span class="sxs-lookup"><span data-stu-id="c72d4-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="c72d4-131">[![Genel gider hesaplaması](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="c72d4-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="c72d4-132">Elektrik genel gideri maliyetini hesapla ve tahsis et</span><span class="sxs-lookup"><span data-stu-id="c72d4-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="c72d4-133">Mali muhasebede, elektrik gibi bazı maliyetler peşin ödeme olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="c72d4-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="c72d4-134">Bu nedenle, Maliyet muhasebesi için ayrıntılı yönetim bilgiler sağlanmaz.</span><span class="sxs-lookup"><span data-stu-id="c72d4-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="c72d4-135">Maliyet muhasebesinde doğru yönetimsel bilgileri tüm yönetim birim ve düzeylerinde sağlamak için, maliyetlerin kuruluş birimleri arasında akması gerekir.</span><span class="sxs-lookup"><span data-stu-id="c72d4-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="c72d4-136">Bu akış, tüketimin doğru bir kaydına ya da adil bir değerlendirmeye dayanıyor olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c72d4-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="c72d4-137">Genel muhasebede, bir elektrik maliyeti aşağıdaki tabloda gösterildiği gibi deftere nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="c72d4-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c72d4-138">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="c72d4-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c72d4-139">Maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="c72d4-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="c72d4-140">Ana hesap</span><span class="sxs-lookup"><span data-stu-id="c72d4-140">Main account</span></span></th>
<th><span data-ttu-id="c72d4-141">Muhasebe para birimi cinsinden tutar</span><span class="sxs-lookup"><span data-stu-id="c72d4-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c72d4-142">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="c72d4-143">CC099</span><span class="sxs-lookup"><span data-stu-id="c72d4-143">CC099</span></span></td>
<td><span data-ttu-id="c72d4-144">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="c72d4-144">Default cost center</span></span></td>
<td><span data-ttu-id="c72d4-145">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-145">10001</span></span></td>
<td><span data-ttu-id="c72d4-146">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-146">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="c72d4-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="c72d4-148">Adım 1: Maliyet davranışı hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="c72d4-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="c72d4-149">Varsayılan olarak, maliyeti girişleri kaynak veriden içeri alındığında, Maliyet muhasebesinde **Sınıflandırılmamış** maliyet davranışı sınıflandırmasını alırlar.</span><span class="sxs-lookup"><span data-stu-id="c72d4-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="c72d4-150">Maliyet davranışı ilke kuralları ekleyerek, maliyet girişlerini **Sabit maliyet** veya **Değişken maliyet** olarak yeniden sınıflandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c72d4-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="c72d4-151">Maliyet davranış kuralını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="c72d4-151">Define the cost behavior rule</span></span>

<span data-ttu-id="c72d4-152">Bazı durumlarda, sabit bir ücret maliyet parçasıdır ve kalan maliyet, tüketime dayanır.</span><span class="sxs-lookup"><span data-stu-id="c72d4-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="c72d4-153">Elektrik faturaları genellikle bu tanıma uyar.</span><span class="sxs-lookup"><span data-stu-id="c72d4-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="c72d4-154">Belirli bir sabit ücret ödedikten sonra, kilovat saatlik (Kwh) tüketim başına ödeme yaparsınız.</span><span class="sxs-lookup"><span data-stu-id="c72d4-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="c72d4-155">Örneğin, sabit maliyet masrafı 1.000,00 ise, maliyet davranışı kural nasıl tanımlanır:</span><span class="sxs-lookup"><span data-stu-id="c72d4-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="c72d4-156">Sabit tutar 1.000,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="c72d4-157">0 &lt;= 1.000,00 = Sabit</span><span class="sxs-lookup"><span data-stu-id="c72d4-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="c72d4-158">1000,01 &lt; N = Değişken</span><span class="sxs-lookup"><span data-stu-id="c72d4-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="c72d4-159">Günlük</span><span class="sxs-lookup"><span data-stu-id="c72d4-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c72d4-160">Günlük</span><span class="sxs-lookup"><span data-stu-id="c72d4-160">Journal</span></span></th>
<th><span data-ttu-id="c72d4-161">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="c72d4-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c72d4-162">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="c72d4-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c72d4-163">Sürüm</span><span class="sxs-lookup"><span data-stu-id="c72d4-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c72d4-164">00001</span><span class="sxs-lookup"><span data-stu-id="c72d4-164">00001</span></span></td>
<td><span data-ttu-id="c72d4-165">Maliyet davranışı hesaplama günlüğü</span><span class="sxs-lookup"><span data-stu-id="c72d4-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="c72d4-166">Mali</span><span class="sxs-lookup"><span data-stu-id="c72d4-166">Fiscal</span></span></td>
<td><span data-ttu-id="c72d4-167">2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-167">2017</span></span></td>
<td><span data-ttu-id="c72d4-168">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-168">Period 1</span></span></td>
<td><span data-ttu-id="c72d4-169">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="c72d4-170">Günlük girişleri (Maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="c72d4-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c72d4-171">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="c72d4-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c72d4-172">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="c72d4-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c72d4-173">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="c72d4-173">Cost element</span></span></th>
<th><span data-ttu-id="c72d4-174">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="c72d4-174">Cost behavior</span></span></th>
<th><span data-ttu-id="c72d4-175">Tutar</span><span class="sxs-lookup"><span data-stu-id="c72d4-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c72d4-176">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="c72d4-177">CC099</span><span class="sxs-lookup"><span data-stu-id="c72d4-177">CC099</span></span></td>
<td><span data-ttu-id="c72d4-178">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="c72d4-178">Default cost center</span></span></td>
<td><span data-ttu-id="c72d4-179">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-179">10001</span></span></td>
<td><span data-ttu-id="c72d4-180">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-180">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-181">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="c72d4-181">Unclassified</span></span></td>
<td><span data-ttu-id="c72d4-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="c72d4-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c72d4-183">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="c72d4-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c72d4-184">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="c72d4-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c72d4-185">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="c72d4-185">Cost element</span></span></th>
<th><span data-ttu-id="c72d4-186">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="c72d4-186">Cost behavior</span></span></th>
<th><span data-ttu-id="c72d4-187">Tutar</span><span class="sxs-lookup"><span data-stu-id="c72d4-187">Amount</span></span></th>
<th><span data-ttu-id="c72d4-188">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="c72d4-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c72d4-189">CC099</span><span class="sxs-lookup"><span data-stu-id="c72d4-189">CC099</span></span></td>
<td><span data-ttu-id="c72d4-190">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="c72d4-190">Default cost center</span></span></td>
<td><span data-ttu-id="c72d4-191">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-191">10001</span></span></td>
<td><span data-ttu-id="c72d4-192">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-192">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-193">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="c72d4-193">Unclassified</span></span></td>
<td><span data-ttu-id="c72d4-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="c72d4-194">10,000.00</span></span></td>
<td><span data-ttu-id="c72d4-195">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-196">CC099</span><span class="sxs-lookup"><span data-stu-id="c72d4-196">CC099</span></span></td>
<td><span data-ttu-id="c72d4-197">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="c72d4-197">Default cost center</span></span></td>
<td><span data-ttu-id="c72d4-198">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-198">10001</span></span></td>
<td><span data-ttu-id="c72d4-199">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-199">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-200">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="c72d4-200">Unclassified</span></span></td>
<td><span data-ttu-id="c72d4-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-201">-10,000.00</span></span></td>
<td><span data-ttu-id="c72d4-202">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-203">CC099</span><span class="sxs-lookup"><span data-stu-id="c72d4-203">CC099</span></span></td>
<td><span data-ttu-id="c72d4-204">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="c72d4-204">Default cost center</span></span></td>
<td><span data-ttu-id="c72d4-205">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-205">10001</span></span></td>
<td><span data-ttu-id="c72d4-206">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-206">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-207">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-207">Fixed cost</span></span></td>
<td><span data-ttu-id="c72d4-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-208">1,000.00</span></span></td>
<td><span data-ttu-id="c72d4-209">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-210">CC099</span><span class="sxs-lookup"><span data-stu-id="c72d4-210">CC099</span></span></td>
<td><span data-ttu-id="c72d4-211">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="c72d4-211">Default cost center</span></span></td>
<td><span data-ttu-id="c72d4-212">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-212">10001</span></span></td>
<td><span data-ttu-id="c72d4-213">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-213">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-214">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-214">Variable cost</span></span></td>
<td><span data-ttu-id="c72d4-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="c72d4-215">9,000.00</span></span></td>
<td><span data-ttu-id="c72d4-216">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c72d4-217">Daha fazla bilgi için bkz. [Maliyet davranışı ilkesi oluşturma ve bir maliyet kontrol birimine atama](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="c72d4-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="c72d4-218">Adım 2: Maliyet dağıtımı hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="c72d4-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="c72d4-219">Maliyet dağıtımı, bir nesneden bir veya daha fazlasına ilgili tahsisat tabanı uygulayarak maliyeti yeniden dağıtmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c72d4-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="c72d4-220">Maliyet dağıtımı ve maliyet tahsisatı, maliyet dağıtımının her zaman orijinal maliyetin birincil maliyet öğesinde bulunmasıyla farklılık gösterir.</span><span class="sxs-lookup"><span data-stu-id="c72d4-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="c72d4-221">Maliyet dağıtım kuralını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="c72d4-221">Define the cost distribution rule</span></span>

<span data-ttu-id="c72d4-222">Mali muhasebede, elektrik maliyetleri çoğu zaman peşin ödeme olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="c72d4-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="c72d4-223">Maliyet muhasebesinde ise bu yöntem yeterince ayrıntılı değildir.</span><span class="sxs-lookup"><span data-stu-id="c72d4-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="c72d4-224">Değişken maliyet, maliyet nesnelerine tek tek, adil bir temele dayanarak dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c72d4-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="c72d4-225">En mantıklı tahsisat, elektrik kullanımını (Kwh) temel alarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c72d4-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="c72d4-226">Elektrik adına sahip, istatistiksel bir boyut üyesi oluşturulur ve elektrik tüketimi kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="c72d4-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="c72d4-227">Varsayıla olarak, tüm istatistiksel boyut üyeleri tahsisat tabanları olarak kullanılabilir hale gelir.</span><span class="sxs-lookup"><span data-stu-id="c72d4-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c72d4-228">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="c72d4-228">Cost object</span></span></th>
<th><span data-ttu-id="c72d4-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="c72d4-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c72d4-230">CC001</span><span class="sxs-lookup"><span data-stu-id="c72d4-230">CC001</span></span></td>
<td><span data-ttu-id="c72d4-231">İK</span><span class="sxs-lookup"><span data-stu-id="c72d4-231">HR</span></span></td>
<td><span data-ttu-id="c72d4-232">1.000</span><span class="sxs-lookup"><span data-stu-id="c72d4-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-233">CC002</span><span class="sxs-lookup"><span data-stu-id="c72d4-233">CC002</span></span></td>
<td><span data-ttu-id="c72d4-234">Finans</span><span class="sxs-lookup"><span data-stu-id="c72d4-234">Finance</span></span></td>
<td><span data-ttu-id="c72d4-235">6,000</span><span class="sxs-lookup"><span data-stu-id="c72d4-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-236">CC003</span><span class="sxs-lookup"><span data-stu-id="c72d4-236">CC003</span></span></td>
<td><span data-ttu-id="c72d4-237">Montaj</span><span class="sxs-lookup"><span data-stu-id="c72d4-237">Assembly</span></span></td>
<td><span data-ttu-id="c72d4-238">0</span><span class="sxs-lookup"><span data-stu-id="c72d4-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c72d4-239">Aşağıdaki tablo, elektrik tüketiminin değişken maliyetler için bir tahsisat tabanlı olarak uygulandığındaki sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="c72d4-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c72d4-240">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="c72d4-240">Cost object</span></span></th>
<th><span data-ttu-id="c72d4-241">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="c72d4-241">Magnitude</span></span></th>
<th><span data-ttu-id="c72d4-242">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="c72d4-242">Allocation factor</span></span></th>
<th><span data-ttu-id="c72d4-243">Tutar</span><span class="sxs-lookup"><span data-stu-id="c72d4-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c72d4-244">CC001</span><span class="sxs-lookup"><span data-stu-id="c72d4-244">CC001</span></span></td>
<td><span data-ttu-id="c72d4-245">İK</span><span class="sxs-lookup"><span data-stu-id="c72d4-245">HR</span></span></td>
<td><span data-ttu-id="c72d4-246">1.000</span><span class="sxs-lookup"><span data-stu-id="c72d4-246">1,000</span></span></td>
<td><span data-ttu-id="c72d4-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="c72d4-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="c72d4-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-249">CC002</span><span class="sxs-lookup"><span data-stu-id="c72d4-249">CC002</span></span></td>
<td><span data-ttu-id="c72d4-250">Finans</span><span class="sxs-lookup"><span data-stu-id="c72d4-250">Finance</span></span></td>
<td><span data-ttu-id="c72d4-251">6,000</span><span class="sxs-lookup"><span data-stu-id="c72d4-251">6,000</span></span></td>
<td><span data-ttu-id="c72d4-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="c72d4-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="c72d4-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-254">CC003</span><span class="sxs-lookup"><span data-stu-id="c72d4-254">CC003</span></span></td>
<td><span data-ttu-id="c72d4-255">Montaj</span><span class="sxs-lookup"><span data-stu-id="c72d4-255">Assembly</span></span></td>
<td><span data-ttu-id="c72d4-256">0</span><span class="sxs-lookup"><span data-stu-id="c72d4-256">0</span></span></td>
<td><span data-ttu-id="c72d4-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="c72d4-258">0,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c72d4-259">Sabit maliyet, elektrik tüketmiş olan tekil maliyet nesnelerine eşit miktarda dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c72d4-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="c72d4-260">Bu sonuca, Elektrik istatistiksel boyut öğesini bir formül tahsisat tabanında kullanarak ulaşabilirsiniz: (Elektrik &gt; 0,00) Aşağıdaki tablo, elektrik tüketimi değişken maliyetler için bir tahsisat tabanı olarak kullanıldığında ortaya çıkan sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="c72d4-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c72d4-261">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="c72d4-261">Cost object</span></span></th>
<th><span data-ttu-id="c72d4-262">Formül</span><span class="sxs-lookup"><span data-stu-id="c72d4-262">Formula</span></span></th>
<th><span data-ttu-id="c72d4-263">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="c72d4-263">Magnitude</span></span></th>
<th><span data-ttu-id="c72d4-264">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="c72d4-264">Allocation factor</span></span></th>
<th><span data-ttu-id="c72d4-265">Tutar</span><span class="sxs-lookup"><span data-stu-id="c72d4-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c72d4-266">CC001</span><span class="sxs-lookup"><span data-stu-id="c72d4-266">CC001</span></span></td>
<td><span data-ttu-id="c72d4-267">İK</span><span class="sxs-lookup"><span data-stu-id="c72d4-267">HR</span></span></td>
<td><span data-ttu-id="c72d4-268">(1,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="c72d4-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="c72d4-269">1</span><span class="sxs-lookup"><span data-stu-id="c72d4-269">1</span></span></td>
<td><span data-ttu-id="c72d4-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="c72d4-271">500.00</span><span class="sxs-lookup"><span data-stu-id="c72d4-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-272">CC002</span><span class="sxs-lookup"><span data-stu-id="c72d4-272">CC002</span></span></td>
<td><span data-ttu-id="c72d4-273">Finans</span><span class="sxs-lookup"><span data-stu-id="c72d4-273">Finance</span></span></td>
<td><span data-ttu-id="c72d4-274">(6,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="c72d4-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="c72d4-275">1</span><span class="sxs-lookup"><span data-stu-id="c72d4-275">1</span></span></td>
<td><span data-ttu-id="c72d4-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="c72d4-277">500.00</span><span class="sxs-lookup"><span data-stu-id="c72d4-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-278">CC003</span><span class="sxs-lookup"><span data-stu-id="c72d4-278">CC003</span></span></td>
<td><span data-ttu-id="c72d4-279">Montaj</span><span class="sxs-lookup"><span data-stu-id="c72d4-279">Assembly</span></span></td>
<td><span data-ttu-id="c72d4-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="c72d4-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="c72d4-281">0</span><span class="sxs-lookup"><span data-stu-id="c72d4-281">0</span></span></td>
<td><span data-ttu-id="c72d4-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="c72d4-283">0,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="c72d4-284">Günlük</span><span class="sxs-lookup"><span data-stu-id="c72d4-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c72d4-285">Günlük</span><span class="sxs-lookup"><span data-stu-id="c72d4-285">Journal</span></span></th>
<th><span data-ttu-id="c72d4-286">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="c72d4-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c72d4-287">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="c72d4-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c72d4-288">Sürüm</span><span class="sxs-lookup"><span data-stu-id="c72d4-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c72d4-289">00002</span><span class="sxs-lookup"><span data-stu-id="c72d4-289">00002</span></span></td>
<td><span data-ttu-id="c72d4-290">Maliyet dağıtımı hesaplama günlüğü</span><span class="sxs-lookup"><span data-stu-id="c72d4-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="c72d4-291">Mali</span><span class="sxs-lookup"><span data-stu-id="c72d4-291">Fiscal</span></span></td>
<td><span data-ttu-id="c72d4-292">2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-292">2017</span></span></td>
<td><span data-ttu-id="c72d4-293">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-293">Period 1</span></span></td>
<td><span data-ttu-id="c72d4-294">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="c72d4-295">Günlük girişleri (Maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="c72d4-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c72d4-296">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="c72d4-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c72d4-297">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="c72d4-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c72d4-298">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="c72d4-298">Cost element</span></span></th>
<th><span data-ttu-id="c72d4-299">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="c72d4-299">Cost behavior</span></span></th>
<th><span data-ttu-id="c72d4-300">Tutar</span><span class="sxs-lookup"><span data-stu-id="c72d4-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c72d4-301">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="c72d4-302">CC099</span><span class="sxs-lookup"><span data-stu-id="c72d4-302">CC099</span></span></td>
<td><span data-ttu-id="c72d4-303">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="c72d4-303">Default cost center</span></span></td>
<td><span data-ttu-id="c72d4-304">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-304">10001</span></span></td>
<td><span data-ttu-id="c72d4-305">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-305">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-306">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-306">Fixed cost</span></span></td>
<td><span data-ttu-id="c72d4-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-308">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="c72d4-309">CC099</span><span class="sxs-lookup"><span data-stu-id="c72d4-309">CC099</span></span></td>
<td><span data-ttu-id="c72d4-310">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="c72d4-310">Default cost center</span></span></td>
<td><span data-ttu-id="c72d4-311">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-311">10001</span></span></td>
<td><span data-ttu-id="c72d4-312">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-312">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-313">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-313">Variable cost</span></span></td>
<td><span data-ttu-id="c72d4-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="c72d4-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c72d4-315">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="c72d4-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c72d4-316">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="c72d4-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c72d4-317">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="c72d4-317">Cost element</span></span></th>
<th><span data-ttu-id="c72d4-318">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="c72d4-318">Cost behavior</span></span></th>
<th><span data-ttu-id="c72d4-319">Tutar</span><span class="sxs-lookup"><span data-stu-id="c72d4-319">Amount</span></span></th>
<th><span data-ttu-id="c72d4-320">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="c72d4-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c72d4-321">CC099</span><span class="sxs-lookup"><span data-stu-id="c72d4-321">CC099</span></span></td>
<td><span data-ttu-id="c72d4-322">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="c72d4-322">Default cost center</span></span></td>
<td><span data-ttu-id="c72d4-323">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-323">10001</span></span></td>
<td><span data-ttu-id="c72d4-324">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-324">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-325">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-325">Fixed cost</span></span></td>
<td><span data-ttu-id="c72d4-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-326">-1,000.00</span></span></td>
<td><span data-ttu-id="c72d4-327">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-328">CC001</span><span class="sxs-lookup"><span data-stu-id="c72d4-328">CC001</span></span></td>
<td><span data-ttu-id="c72d4-329">İK</span><span class="sxs-lookup"><span data-stu-id="c72d4-329">HR</span></span></td>
<td><span data-ttu-id="c72d4-330">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-330">10001</span></span></td>
<td><span data-ttu-id="c72d4-331">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-331">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-332">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-332">Fixed cost</span></span></td>
<td><span data-ttu-id="c72d4-333">500.00</span><span class="sxs-lookup"><span data-stu-id="c72d4-333">500.00</span></span></td>
<td><span data-ttu-id="c72d4-334">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-335">CC002</span><span class="sxs-lookup"><span data-stu-id="c72d4-335">CC002</span></span></td>
<td><span data-ttu-id="c72d4-336">Finans</span><span class="sxs-lookup"><span data-stu-id="c72d4-336">Finance</span></span></td>
<td><span data-ttu-id="c72d4-337">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-337">10001</span></span></td>
<td><span data-ttu-id="c72d4-338">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-338">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-339">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-339">Fixed cost</span></span></td>
<td><span data-ttu-id="c72d4-340">500.00</span><span class="sxs-lookup"><span data-stu-id="c72d4-340">500.00</span></span></td>
<td><span data-ttu-id="c72d4-341">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-342">CC099</span><span class="sxs-lookup"><span data-stu-id="c72d4-342">CC099</span></span></td>
<td><span data-ttu-id="c72d4-343">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="c72d4-343">Default cost center</span></span></td>
<td><span data-ttu-id="c72d4-344">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-344">10001</span></span></td>
<td><span data-ttu-id="c72d4-345">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-345">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-346">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-346">Variable cost</span></span></td>
<td><span data-ttu-id="c72d4-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-347">-9,000.00</span></span></td>
<td><span data-ttu-id="c72d4-348">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-349">CC001</span><span class="sxs-lookup"><span data-stu-id="c72d4-349">CC001</span></span></td>
<td><span data-ttu-id="c72d4-350">İK</span><span class="sxs-lookup"><span data-stu-id="c72d4-350">HR</span></span></td>
<td><span data-ttu-id="c72d4-351">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-351">10001</span></span></td>
<td><span data-ttu-id="c72d4-352">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-352">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-353">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-353">Variable cost</span></span></td>
<td><span data-ttu-id="c72d4-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="c72d4-354">1,285.71</span></span></td>
<td><span data-ttu-id="c72d4-355">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-356">CC002</span><span class="sxs-lookup"><span data-stu-id="c72d4-356">CC002</span></span></td>
<td><span data-ttu-id="c72d4-357">Finans</span><span class="sxs-lookup"><span data-stu-id="c72d4-357">Finance</span></span></td>
<td><span data-ttu-id="c72d4-358">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-358">10001</span></span></td>
<td><span data-ttu-id="c72d4-359">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-359">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-360">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-360">Variable cost</span></span></td>
<td><span data-ttu-id="c72d4-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="c72d4-361">7,714.29</span></span></td>
<td><span data-ttu-id="c72d4-362">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c72d4-363">Daha fazla bilgi için bkz. [Maliyet dağıtımı ilkesi oluşturma ve bir maliyet kontrol birimine atama](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="c72d4-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="c72d4-364">Adım 3: Genel gider oranı hesaplama işlemi</span><span class="sxs-lookup"><span data-stu-id="c72d4-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="c72d4-365">Genel gider oranı, bir veya birden fazla belirli maliyet nesnesine masraf yüklemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c72d4-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="c72d4-366">Masraf, önceden belirlenmiş maliyet oranına ve tahsisat tabanından hesaplanan büyüklüğe dayanır.</span><span class="sxs-lookup"><span data-stu-id="c72d4-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="c72d4-367">Genel gider oranını tanımlama</span><span class="sxs-lookup"><span data-stu-id="c72d4-367">Define the overhead rate</span></span>

<span data-ttu-id="c72d4-368">Maliyet nesnesi CC001 HR, bir dizi dahili projeye katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="c72d4-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="c72d4-369">HR projeleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c72d4-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c72d4-370">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="c72d4-370">Cost object</span></span></th>
<th><span data-ttu-id="c72d4-371">Saatler</span><span class="sxs-lookup"><span data-stu-id="c72d4-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c72d4-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-372">Proj 1</span></span></td>
<td><span data-ttu-id="c72d4-373">Proje 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-373">Project 1</span></span></td>
<td><span data-ttu-id="c72d4-374">3</span><span class="sxs-lookup"><span data-stu-id="c72d4-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="c72d4-375">Proj 2</span></span></td>
<td><span data-ttu-id="c72d4-376">Proje 2</span><span class="sxs-lookup"><span data-stu-id="c72d4-376">Project 2</span></span></td>
<td><span data-ttu-id="c72d4-377">1</span><span class="sxs-lookup"><span data-stu-id="c72d4-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c72d4-378">Maliyet projeleri dağıtımı için bir önceden belirlenmiş maliyet oranı tanımlandı.</span><span class="sxs-lookup"><span data-stu-id="c72d4-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c72d4-379">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="c72d4-379">Cost object</span></span></th>
<th><span data-ttu-id="c72d4-380">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="c72d4-380">Cost element</span></span></th>
<th><span data-ttu-id="c72d4-381">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="c72d4-381">Cost behavior</span></span></th>
<th><span data-ttu-id="c72d4-382">Birimler</span><span class="sxs-lookup"><span data-stu-id="c72d4-382">Units</span></span></th>
<th><span data-ttu-id="c72d4-383">Ücret</span><span class="sxs-lookup"><span data-stu-id="c72d4-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c72d4-384">CC001</span><span class="sxs-lookup"><span data-stu-id="c72d4-384">CC001</span></span></td>
<td><span data-ttu-id="c72d4-385">İK</span><span class="sxs-lookup"><span data-stu-id="c72d4-385">HR</span></span></td>
<td><span data-ttu-id="c72d4-386">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-386">10001</span></span></td>
<td><span data-ttu-id="c72d4-387">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-387">Variable cost</span></span></td>
<td><span data-ttu-id="c72d4-388">1</span><span class="sxs-lookup"><span data-stu-id="c72d4-388">1</span></span></td>
<td><span data-ttu-id="c72d4-389">10</span><span class="sxs-lookup"><span data-stu-id="c72d4-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c72d4-390">Aşağıdaki tablo, HR projeleri bir tahsisat tabanı olarak uygulandığındaki sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="c72d4-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c72d4-391">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="c72d4-391">Cost object</span></span></th>
<th><span data-ttu-id="c72d4-392">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="c72d4-392">Magnitude</span></span></th>
<th><span data-ttu-id="c72d4-393">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="c72d4-393">Cost element</span></span></th>
<th><span data-ttu-id="c72d4-394">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="c72d4-394">Allocation factor</span></span></th>
<th><span data-ttu-id="c72d4-395">Tutar</span><span class="sxs-lookup"><span data-stu-id="c72d4-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c72d4-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-396">Proj 1</span></span></td>
<td><span data-ttu-id="c72d4-397">Proje 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-397">Project 1</span></span></td>
<td><span data-ttu-id="c72d4-398">3</span><span class="sxs-lookup"><span data-stu-id="c72d4-398">3</span></span></td>
<td><span data-ttu-id="c72d4-399">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-399">10001</span></span></td>
<td><span data-ttu-id="c72d4-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="c72d4-401">30.00</span><span class="sxs-lookup"><span data-stu-id="c72d4-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="c72d4-402">Proj 2</span></span></td>
<td><span data-ttu-id="c72d4-403">Proje 2</span><span class="sxs-lookup"><span data-stu-id="c72d4-403">Project 2</span></span></td>
<td><span data-ttu-id="c72d4-404">1</span><span class="sxs-lookup"><span data-stu-id="c72d4-404">1</span></span></td>
<td><span data-ttu-id="c72d4-405">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-405">10001</span></span></td>
<td><span data-ttu-id="c72d4-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="c72d4-407">10,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="c72d4-408">Günlük</span><span class="sxs-lookup"><span data-stu-id="c72d4-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c72d4-409">Günlük</span><span class="sxs-lookup"><span data-stu-id="c72d4-409">Journal</span></span></th>
<th><span data-ttu-id="c72d4-410">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="c72d4-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c72d4-411">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="c72d4-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c72d4-412">Sürüm</span><span class="sxs-lookup"><span data-stu-id="c72d4-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c72d4-413">00003</span><span class="sxs-lookup"><span data-stu-id="c72d4-413">00003</span></span></td>
<td><span data-ttu-id="c72d4-414">Genel gider oranı hesaplaması günlüğü</span><span class="sxs-lookup"><span data-stu-id="c72d4-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="c72d4-415">Mali</span><span class="sxs-lookup"><span data-stu-id="c72d4-415">Fiscal</span></span></td>
<td><span data-ttu-id="c72d4-416">2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-416">2017</span></span></td>
<td><span data-ttu-id="c72d4-417">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-417">Period 1</span></span></td>
<td><span data-ttu-id="c72d4-418">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="c72d4-419">Günlük girişleri (Genel gider oranı hesaplaması için günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="c72d4-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c72d4-420">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="c72d4-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c72d4-421">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="c72d4-421">Cost object</span></span></th>
<th><span data-ttu-id="c72d4-422">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="c72d4-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c72d4-423">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="c72d4-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-424">Proj 1</span></span></td>
<td><span data-ttu-id="c72d4-425">Dahili Proj 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="c72d4-426">3,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-427">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="c72d4-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="c72d4-428">Proj 2</span></span></td>
<td><span data-ttu-id="c72d4-429">Dahili Proj 2</span><span class="sxs-lookup"><span data-stu-id="c72d4-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="c72d4-430">1.00</span><span class="sxs-lookup"><span data-stu-id="c72d4-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c72d4-431">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="c72d4-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c72d4-432">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="c72d4-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c72d4-433">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="c72d4-433">Cost element</span></span></th>
<th><span data-ttu-id="c72d4-434">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="c72d4-434">Cost behavior</span></span></th>
<th><span data-ttu-id="c72d4-435">Tutar</span><span class="sxs-lookup"><span data-stu-id="c72d4-435">Amount</span></span></th>
<th><span data-ttu-id="c72d4-436">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="c72d4-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c72d4-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="c72d4-437">CC0001</span></span></td>
<td><span data-ttu-id="c72d4-438">İK</span><span class="sxs-lookup"><span data-stu-id="c72d4-438">HR</span></span></td>
<td><span data-ttu-id="c72d4-439">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-439">10001</span></span></td>
<td><span data-ttu-id="c72d4-440">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-440">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-441">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-441">Variable cost</span></span></td>
<td><span data-ttu-id="c72d4-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-442">-30.00</span></span></td>
<td><span data-ttu-id="c72d4-443">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-444">Proj 1</span></span></td>
<td><span data-ttu-id="c72d4-445">Dahili Proj 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="c72d4-446">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-446">10001</span></span></td>
<td><span data-ttu-id="c72d4-447">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-447">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-448">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-448">Variable cost</span></span></td>
<td><span data-ttu-id="c72d4-449">30.00</span><span class="sxs-lookup"><span data-stu-id="c72d4-449">30.00</span></span></td>
<td><span data-ttu-id="c72d4-450">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-451">CC001</span><span class="sxs-lookup"><span data-stu-id="c72d4-451">CC001</span></span></td>
<td><span data-ttu-id="c72d4-452">İK</span><span class="sxs-lookup"><span data-stu-id="c72d4-452">HR</span></span></td>
<td><span data-ttu-id="c72d4-453">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-453">10001</span></span></td>
<td><span data-ttu-id="c72d4-454">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-454">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-455">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-455">Variable cost</span></span></td>
<td><span data-ttu-id="c72d4-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-456">-10.00</span></span></td>
<td><span data-ttu-id="c72d4-457">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="c72d4-458">Proj 2</span></span></td>
<td><span data-ttu-id="c72d4-459">Dahili Proj 2</span><span class="sxs-lookup"><span data-stu-id="c72d4-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="c72d4-460">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-460">10001</span></span></td>
<td><span data-ttu-id="c72d4-461">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-461">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-462">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-462">Variable cost</span></span></td>
<td><span data-ttu-id="c72d4-463">10,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-463">10.00</span></span></td>
<td><span data-ttu-id="c72d4-464">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c72d4-465">Daha fazla bilgi için [Genel gider hesaplaması gerçekleştir](cost-rollup.md#perform-overhead-calculation) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="c72d4-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="c72d4-466">Adım 4: Maliyet tahsisat hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="c72d4-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="c72d4-467">Tahsisat, bir tahsisat tabanı kullanarak bir maliyet nesnesinin diğer maliyet nesnelerine bakiyesini tahsis eder.</span><span class="sxs-lookup"><span data-stu-id="c72d4-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="c72d4-468">Finance and Operations karşılıklı tahsisat yöntemin destekler.</span><span class="sxs-lookup"><span data-stu-id="c72d4-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="c72d4-469">Karşılıklı tahsisat yönteminde, yardımcı maliyet nesnelerinin değiştiği karşılıklı hizmetler tümüyle tanınır.</span><span class="sxs-lookup"><span data-stu-id="c72d4-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="c72d4-470">Sistem, tahsisatların doğru gerçekleştireceği sırayı otomatik olarak belirler.</span><span class="sxs-lookup"><span data-stu-id="c72d4-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="c72d4-471">Bir maliyet nesnesinin bakiyesi tek bir tahsisat tabanı tarafından tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="c72d4-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="c72d4-472">Yeni maliyet nesnesi boyutları arasındaki tahsisatlar ve onların üyeleri desteklenir.</span><span class="sxs-lookup"><span data-stu-id="c72d4-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="c72d4-473">Tahsisatın sırası, maliyet kontrol birimi tarafından kontrol edilir.</span><span class="sxs-lookup"><span data-stu-id="c72d4-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="c72d4-474">[![Karşılıklı yöntemi](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="c72d4-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="c72d4-475">Maliyet tahsisatını tanımla</span><span class="sxs-lookup"><span data-stu-id="c72d4-475">Define the cost allocation</span></span>

<span data-ttu-id="c72d4-476">Bir maliyetin akışını nasıl izleyeceğinize dair basit bir örnek aşağıda verilmiştir,</span><span class="sxs-lookup"><span data-stu-id="c72d4-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="c72d4-477">Maliyet nesnesi CC001 HR, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="c72d4-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="c72d4-478">HR hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c72d4-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c72d4-479">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="c72d4-479">Cost object</span></span></th>
<th><span data-ttu-id="c72d4-480">HR hizmetleri</span><span class="sxs-lookup"><span data-stu-id="c72d4-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c72d4-481">CC002</span><span class="sxs-lookup"><span data-stu-id="c72d4-481">CC002</span></span></td>
<td><span data-ttu-id="c72d4-482">Finans</span><span class="sxs-lookup"><span data-stu-id="c72d4-482">Finance</span></span></td>
<td><span data-ttu-id="c72d4-483">35</span><span class="sxs-lookup"><span data-stu-id="c72d4-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-484">CC003</span><span class="sxs-lookup"><span data-stu-id="c72d4-484">CC003</span></span></td>
<td><span data-ttu-id="c72d4-485">Montaj</span><span class="sxs-lookup"><span data-stu-id="c72d4-485">Assembly</span></span></td>
<td><span data-ttu-id="c72d4-486">55</span><span class="sxs-lookup"><span data-stu-id="c72d4-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-487">CC004</span><span class="sxs-lookup"><span data-stu-id="c72d4-487">CC004</span></span></td>
<td><span data-ttu-id="c72d4-488">Paketleme</span><span class="sxs-lookup"><span data-stu-id="c72d4-488">Packaging</span></span></td>
<td><span data-ttu-id="c72d4-489">10</span><span class="sxs-lookup"><span data-stu-id="c72d4-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c72d4-490">Maliyet nesnesi CC002 Finans, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="c72d4-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="c72d4-491">Finans hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c72d4-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c72d4-492">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="c72d4-492">Cost object</span></span></th>
<th><span data-ttu-id="c72d4-493">Finans hizmetleri</span><span class="sxs-lookup"><span data-stu-id="c72d4-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c72d4-494">CC003</span><span class="sxs-lookup"><span data-stu-id="c72d4-494">CC003</span></span></td>
<td><span data-ttu-id="c72d4-495">Montaj</span><span class="sxs-lookup"><span data-stu-id="c72d4-495">Assembly</span></span></td>
<td><span data-ttu-id="c72d4-496">65</span><span class="sxs-lookup"><span data-stu-id="c72d4-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-497">CC004</span><span class="sxs-lookup"><span data-stu-id="c72d4-497">CC004</span></span></td>
<td><span data-ttu-id="c72d4-498">Paketleme</span><span class="sxs-lookup"><span data-stu-id="c72d4-498">Packaging</span></span></td>
<td><span data-ttu-id="c72d4-499">35</span><span class="sxs-lookup"><span data-stu-id="c72d4-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c72d4-500">Maliyet nesnesi CC003 Derleme, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="c72d4-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="c72d4-501">Derleme hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c72d4-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c72d4-502">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="c72d4-502">Cost object</span></span></th>
<th><span data-ttu-id="c72d4-503">Derleme Hizmetleri (saat)</span><span class="sxs-lookup"><span data-stu-id="c72d4-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c72d4-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-504">Prod 1</span></span></td>
<td><span data-ttu-id="c72d4-505">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-505">Product 1</span></span></td>
<td><span data-ttu-id="c72d4-506">60</span><span class="sxs-lookup"><span data-stu-id="c72d4-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="c72d4-507">Prod 2</span></span></td>
<td><span data-ttu-id="c72d4-508">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="c72d4-508">Product 2</span></span></td>
<td><span data-ttu-id="c72d4-509">20</span><span class="sxs-lookup"><span data-stu-id="c72d4-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c72d4-510">Maliyet nesnesi CC004 Ambalajlama, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="c72d4-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="c72d4-511">Ambalajlama hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c72d4-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c72d4-512">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="c72d4-512">Cost object</span></span></th>
<th><span data-ttu-id="c72d4-513">Ambalajlama hizmetleri (saat)</span><span class="sxs-lookup"><span data-stu-id="c72d4-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c72d4-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-514">Prod 1</span></span></td>
<td><span data-ttu-id="c72d4-515">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-515">Product 1</span></span></td>
<td><span data-ttu-id="c72d4-516">80</span><span class="sxs-lookup"><span data-stu-id="c72d4-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="c72d4-517">Prod 2</span></span></td>
<td><span data-ttu-id="c72d4-518">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="c72d4-518">Product 2</span></span></td>
<td><span data-ttu-id="c72d4-519">15</span><span class="sxs-lookup"><span data-stu-id="c72d4-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="c72d4-520">Finance and Operations'ta, bir ürünün tükettiği üretim saatleri gibi istatistiki ölçümler doğrudan kaynak verisinden alınabilir.</span><span class="sxs-lookup"><span data-stu-id="c72d4-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="c72d4-521">Daha fazla bilgi için, [İstatistiksel ölçüm sağlayıcı şablonu](statistical-measure-provider-template.md#statistical-measure-provider-template) bakın.</span><span class="sxs-lookup"><span data-stu-id="c72d4-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="c72d4-522">Aşağıdaki tablo, İK hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığında ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="c72d4-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c72d4-523">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="c72d4-523">Cost object</span></span></th>
<th><span data-ttu-id="c72d4-524">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="c72d4-524">Magnitude</span></span></th>
<th><span data-ttu-id="c72d4-525">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="c72d4-525">Allocation factor</span></span></th>
<th><span data-ttu-id="c72d4-526">Tutar</span><span class="sxs-lookup"><span data-stu-id="c72d4-526">Amount</span></span></th>
<th><span data-ttu-id="c72d4-527">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="c72d4-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c72d4-528">CC002</span><span class="sxs-lookup"><span data-stu-id="c72d4-528">CC002</span></span></td>
<td><span data-ttu-id="c72d4-529">Finans</span><span class="sxs-lookup"><span data-stu-id="c72d4-529">Finance</span></span></td>
<td><span data-ttu-id="c72d4-530">35</span><span class="sxs-lookup"><span data-stu-id="c72d4-530">35</span></span></td>
<td><span data-ttu-id="c72d4-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="c72d4-532">175.00</span><span class="sxs-lookup"><span data-stu-id="c72d4-532">175.00</span></span></td>
<td><span data-ttu-id="c72d4-533">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-534">CC003</span><span class="sxs-lookup"><span data-stu-id="c72d4-534">CC003</span></span></td>
<td><span data-ttu-id="c72d4-535">Montaj</span><span class="sxs-lookup"><span data-stu-id="c72d4-535">Assembly</span></span></td>
<td><span data-ttu-id="c72d4-536">55</span><span class="sxs-lookup"><span data-stu-id="c72d4-536">55</span></span></td>
<td><span data-ttu-id="c72d4-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="c72d4-538">275.00</span><span class="sxs-lookup"><span data-stu-id="c72d4-538">275.00</span></span></td>
<td><span data-ttu-id="c72d4-539">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-540">CC004</span><span class="sxs-lookup"><span data-stu-id="c72d4-540">CC004</span></span></td>
<td><span data-ttu-id="c72d4-541">Paketleme</span><span class="sxs-lookup"><span data-stu-id="c72d4-541">Packaging</span></span></td>
<td><span data-ttu-id="c72d4-542">10</span><span class="sxs-lookup"><span data-stu-id="c72d4-542">10</span></span></td>
<td><span data-ttu-id="c72d4-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="c72d4-544">50,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-544">50.00</span></span></td>
<td><span data-ttu-id="c72d4-545">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-546">CC002</span><span class="sxs-lookup"><span data-stu-id="c72d4-546">CC002</span></span></td>
<td><span data-ttu-id="c72d4-547">Finans</span><span class="sxs-lookup"><span data-stu-id="c72d4-547">Finance</span></span></td>
<td><span data-ttu-id="c72d4-548">35</span><span class="sxs-lookup"><span data-stu-id="c72d4-548">35</span></span></td>
<td><span data-ttu-id="c72d4-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="c72d4-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="c72d4-550">436.00</span><span class="sxs-lookup"><span data-stu-id="c72d4-550">436.00</span></span></td>
<td><span data-ttu-id="c72d4-551">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-552">CC003</span><span class="sxs-lookup"><span data-stu-id="c72d4-552">CC003</span></span></td>
<td><span data-ttu-id="c72d4-553">Montaj</span><span class="sxs-lookup"><span data-stu-id="c72d4-553">Assembly</span></span></td>
<td><span data-ttu-id="c72d4-554">55</span><span class="sxs-lookup"><span data-stu-id="c72d4-554">55</span></span></td>
<td><span data-ttu-id="c72d4-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="c72d4-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="c72d4-556">685.14</span><span class="sxs-lookup"><span data-stu-id="c72d4-556">685.14</span></span></td>
<td><span data-ttu-id="c72d4-557">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-558">CC004</span><span class="sxs-lookup"><span data-stu-id="c72d4-558">CC004</span></span></td>
<td><span data-ttu-id="c72d4-559">Paketleme</span><span class="sxs-lookup"><span data-stu-id="c72d4-559">Packaging</span></span></td>
<td><span data-ttu-id="c72d4-560">10</span><span class="sxs-lookup"><span data-stu-id="c72d4-560">10</span></span></td>
<td><span data-ttu-id="c72d4-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="c72d4-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="c72d4-562">124.57</span><span class="sxs-lookup"><span data-stu-id="c72d4-562">124.57</span></span></td>
<td><span data-ttu-id="c72d4-563">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c72d4-564">Aşağıdaki tablo, Finans hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="c72d4-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c72d4-565">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="c72d4-565">Cost object</span></span></th>
<th><span data-ttu-id="c72d4-566">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="c72d4-566">Magnitude</span></span></th>
<th><span data-ttu-id="c72d4-567">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="c72d4-567">Allocation factor</span></span></th>
<th><span data-ttu-id="c72d4-568">Tutar</span><span class="sxs-lookup"><span data-stu-id="c72d4-568">Amount</span></span></th>
<th><span data-ttu-id="c72d4-569">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="c72d4-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c72d4-570">CC003</span><span class="sxs-lookup"><span data-stu-id="c72d4-570">CC003</span></span></td>
<td><span data-ttu-id="c72d4-571">Montaj</span><span class="sxs-lookup"><span data-stu-id="c72d4-571">Assembly</span></span></td>
<td><span data-ttu-id="c72d4-572">65</span><span class="sxs-lookup"><span data-stu-id="c72d4-572">65</span></span></td>
<td><span data-ttu-id="c72d4-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="c72d4-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="c72d4-574">438.75</span><span class="sxs-lookup"><span data-stu-id="c72d4-574">438.75</span></span></td>
<td><span data-ttu-id="c72d4-575">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-576">CC004</span><span class="sxs-lookup"><span data-stu-id="c72d4-576">CC004</span></span></td>
<td><span data-ttu-id="c72d4-577">Paketleme</span><span class="sxs-lookup"><span data-stu-id="c72d4-577">Packaging</span></span></td>
<td><span data-ttu-id="c72d4-578">35</span><span class="sxs-lookup"><span data-stu-id="c72d4-578">35</span></span></td>
<td><span data-ttu-id="c72d4-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="c72d4-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="c72d4-580">236.25</span><span class="sxs-lookup"><span data-stu-id="c72d4-580">236.25</span></span></td>
<td><span data-ttu-id="c72d4-581">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-582">CC003</span><span class="sxs-lookup"><span data-stu-id="c72d4-582">CC003</span></span></td>
<td><span data-ttu-id="c72d4-583">Montaj</span><span class="sxs-lookup"><span data-stu-id="c72d4-583">Assembly</span></span></td>
<td><span data-ttu-id="c72d4-584">65</span><span class="sxs-lookup"><span data-stu-id="c72d4-584">65</span></span></td>
<td><span data-ttu-id="c72d4-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="c72d4-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="c72d4-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="c72d4-586">5,297.69</span></span></td>
<td><span data-ttu-id="c72d4-587">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-588">CC004</span><span class="sxs-lookup"><span data-stu-id="c72d4-588">CC004</span></span></td>
<td><span data-ttu-id="c72d4-589">Paketleme</span><span class="sxs-lookup"><span data-stu-id="c72d4-589">Packaging</span></span></td>
<td><span data-ttu-id="c72d4-590">35</span><span class="sxs-lookup"><span data-stu-id="c72d4-590">35</span></span></td>
<td><span data-ttu-id="c72d4-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="c72d4-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="c72d4-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="c72d4-592">2,852.60</span></span></td>
<td><span data-ttu-id="c72d4-593">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c72d4-594">Aşağıdaki tablo, Derleme hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="c72d4-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c72d4-595">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="c72d4-595">Cost object</span></span></th>
<th><span data-ttu-id="c72d4-596">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="c72d4-596">Magnitude</span></span></th>
<th><span data-ttu-id="c72d4-597">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="c72d4-597">Allocation factor</span></span></th>
<th><span data-ttu-id="c72d4-598">Tutar</span><span class="sxs-lookup"><span data-stu-id="c72d4-598">Amount</span></span></th>
<th><span data-ttu-id="c72d4-599">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="c72d4-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c72d4-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-600">Prod 1</span></span></td>
<td><span data-ttu-id="c72d4-601">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-601">Product 1</span></span></td>
<td><span data-ttu-id="c72d4-602">60</span><span class="sxs-lookup"><span data-stu-id="c72d4-602">60</span></span></td>
<td><span data-ttu-id="c72d4-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="c72d4-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="c72d4-604">535.31</span><span class="sxs-lookup"><span data-stu-id="c72d4-604">535.31</span></span></td>
<td><span data-ttu-id="c72d4-605">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="c72d4-606">Prod 2</span></span></td>
<td><span data-ttu-id="c72d4-607">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="c72d4-607">Product 2</span></span></td>
<td><span data-ttu-id="c72d4-608">20</span><span class="sxs-lookup"><span data-stu-id="c72d4-608">20</span></span></td>
<td><span data-ttu-id="c72d4-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="c72d4-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="c72d4-610">178.44</span><span class="sxs-lookup"><span data-stu-id="c72d4-610">178.44</span></span></td>
<td><span data-ttu-id="c72d4-611">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-612">Prod 1</span></span></td>
<td><span data-ttu-id="c72d4-613">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-613">Product 1</span></span></td>
<td><span data-ttu-id="c72d4-614">60</span><span class="sxs-lookup"><span data-stu-id="c72d4-614">60</span></span></td>
<td><span data-ttu-id="c72d4-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="c72d4-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="c72d4-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="c72d4-616">4,487.12</span></span></td>
<td><span data-ttu-id="c72d4-617">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="c72d4-618">Prod 2</span></span></td>
<td><span data-ttu-id="c72d4-619">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="c72d4-619">Product 2</span></span></td>
<td><span data-ttu-id="c72d4-620">20</span><span class="sxs-lookup"><span data-stu-id="c72d4-620">20</span></span></td>
<td><span data-ttu-id="c72d4-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="c72d4-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="c72d4-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="c72d4-622">1,495.71</span></span></td>
<td><span data-ttu-id="c72d4-623">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c72d4-624">Aşağıdaki tablo, Paketleme hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="c72d4-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c72d4-625">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="c72d4-625">Cost object</span></span></th>
<th><span data-ttu-id="c72d4-626">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="c72d4-626">Magnitude</span></span></th>
<th><span data-ttu-id="c72d4-627">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="c72d4-627">Allocation factor</span></span></th>
<th><span data-ttu-id="c72d4-628">Tutar</span><span class="sxs-lookup"><span data-stu-id="c72d4-628">Amount</span></span></th>
<th><span data-ttu-id="c72d4-629">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="c72d4-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c72d4-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-630">Prod 1</span></span></td>
<td><span data-ttu-id="c72d4-631">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-631">Product 1</span></span></td>
<td><span data-ttu-id="c72d4-632">80</span><span class="sxs-lookup"><span data-stu-id="c72d4-632">80</span></span></td>
<td><span data-ttu-id="c72d4-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="c72d4-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="c72d4-634">241.05</span><span class="sxs-lookup"><span data-stu-id="c72d4-634">241.05</span></span></td>
<td><span data-ttu-id="c72d4-635">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="c72d4-636">Prod 2</span></span></td>
<td><span data-ttu-id="c72d4-637">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="c72d4-637">Product 2</span></span></td>
<td><span data-ttu-id="c72d4-638">15</span><span class="sxs-lookup"><span data-stu-id="c72d4-638">15</span></span></td>
<td><span data-ttu-id="c72d4-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="c72d4-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="c72d4-640">45.20</span><span class="sxs-lookup"><span data-stu-id="c72d4-640">45.20</span></span></td>
<td><span data-ttu-id="c72d4-641">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-642">Prod 1</span></span></td>
<td><span data-ttu-id="c72d4-643">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-643">Product 1</span></span></td>
<td><span data-ttu-id="c72d4-644">80</span><span class="sxs-lookup"><span data-stu-id="c72d4-644">80</span></span></td>
<td><span data-ttu-id="c72d4-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="c72d4-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="c72d4-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="c72d4-646">2,507.09</span></span></td>
<td><span data-ttu-id="c72d4-647">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="c72d4-648">Prod 2</span></span></td>
<td><span data-ttu-id="c72d4-649">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="c72d4-649">Product 2</span></span></td>
<td><span data-ttu-id="c72d4-650">15</span><span class="sxs-lookup"><span data-stu-id="c72d4-650">15</span></span></td>
<td><span data-ttu-id="c72d4-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="c72d4-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="c72d4-652">470.08</span><span class="sxs-lookup"><span data-stu-id="c72d4-652">470.08</span></span></td>
<td><span data-ttu-id="c72d4-653">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="c72d4-654">Günlük girişleri (maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="c72d4-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c72d4-655">Günlük</span><span class="sxs-lookup"><span data-stu-id="c72d4-655">Journal</span></span></th>
<th><span data-ttu-id="c72d4-656">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="c72d4-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c72d4-657">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="c72d4-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c72d4-658">Sürüm</span><span class="sxs-lookup"><span data-stu-id="c72d4-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c72d4-659">00004</span><span class="sxs-lookup"><span data-stu-id="c72d4-659">00004</span></span></td>
<td><span data-ttu-id="c72d4-660">Maliyet tahsisatı günlüğü</span><span class="sxs-lookup"><span data-stu-id="c72d4-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="c72d4-661">Mali</span><span class="sxs-lookup"><span data-stu-id="c72d4-661">Fiscal</span></span></td>
<td><span data-ttu-id="c72d4-662">2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-662">2017</span></span></td>
<td><span data-ttu-id="c72d4-663">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-663">Period 1</span></span></td>
<td><span data-ttu-id="c72d4-664">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="c72d4-665">Günlük satırları</span><span class="sxs-lookup"><span data-stu-id="c72d4-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c72d4-666">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="c72d4-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c72d4-667">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="c72d4-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c72d4-668">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="c72d4-668">Cost element</span></span></th>
<th><span data-ttu-id="c72d4-669">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="c72d4-669">Cost behavior</span></span></th>
<th><span data-ttu-id="c72d4-670">Tutar</span><span class="sxs-lookup"><span data-stu-id="c72d4-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c72d4-671">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="c72d4-672">CC001</span><span class="sxs-lookup"><span data-stu-id="c72d4-672">CC001</span></span></td>
<td><span data-ttu-id="c72d4-673">İK</span><span class="sxs-lookup"><span data-stu-id="c72d4-673">HR</span></span></td>
<td><span data-ttu-id="c72d4-674">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-674">10001</span></span></td>
<td><span data-ttu-id="c72d4-675">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-675">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-676">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-676">Fixed cost</span></span></td>
<td><span data-ttu-id="c72d4-677">500.00</span><span class="sxs-lookup"><span data-stu-id="c72d4-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-678">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="c72d4-679">CC001</span><span class="sxs-lookup"><span data-stu-id="c72d4-679">CC001</span></span></td>
<td><span data-ttu-id="c72d4-680">İK</span><span class="sxs-lookup"><span data-stu-id="c72d4-680">HR</span></span></td>
<td><span data-ttu-id="c72d4-681">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-681">10001</span></span></td>
<td><span data-ttu-id="c72d4-682">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-682">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-683">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-683">Variable cost</span></span></td>
<td><span data-ttu-id="c72d4-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="c72d4-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-685">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="c72d4-686">CC002</span><span class="sxs-lookup"><span data-stu-id="c72d4-686">CC002</span></span></td>
<td><span data-ttu-id="c72d4-687">Finans</span><span class="sxs-lookup"><span data-stu-id="c72d4-687">Finance</span></span></td>
<td><span data-ttu-id="c72d4-688">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-688">10001</span></span></td>
<td><span data-ttu-id="c72d4-689">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-689">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-690">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-690">Fixed cost</span></span></td>
<td><span data-ttu-id="c72d4-691">675.00</span><span class="sxs-lookup"><span data-stu-id="c72d4-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-692">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="c72d4-693">CC002</span><span class="sxs-lookup"><span data-stu-id="c72d4-693">CC002</span></span></td>
<td><span data-ttu-id="c72d4-694">Finans</span><span class="sxs-lookup"><span data-stu-id="c72d4-694">Finance</span></span></td>
<td><span data-ttu-id="c72d4-695">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-695">10001</span></span></td>
<td><span data-ttu-id="c72d4-696">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-696">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-697">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-697">Variable cost</span></span></td>
<td><span data-ttu-id="c72d4-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="c72d4-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-699">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="c72d4-700">CC003</span><span class="sxs-lookup"><span data-stu-id="c72d4-700">CC003</span></span></td>
<td><span data-ttu-id="c72d4-701">Montaj</span><span class="sxs-lookup"><span data-stu-id="c72d4-701">Assembly</span></span></td>
<td><span data-ttu-id="c72d4-702">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-702">10001</span></span></td>
<td><span data-ttu-id="c72d4-703">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-703">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-704">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-704">Fixed cost</span></span></td>
<td><span data-ttu-id="c72d4-705">713.75</span><span class="sxs-lookup"><span data-stu-id="c72d4-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-706">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="c72d4-707">CC003</span><span class="sxs-lookup"><span data-stu-id="c72d4-707">CC003</span></span></td>
<td><span data-ttu-id="c72d4-708">Montaj</span><span class="sxs-lookup"><span data-stu-id="c72d4-708">Assembly</span></span></td>
<td><span data-ttu-id="c72d4-709">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-709">10001</span></span></td>
<td><span data-ttu-id="c72d4-710">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-710">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-711">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-711">Variable cost</span></span></td>
<td><span data-ttu-id="c72d4-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="c72d4-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-713">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="c72d4-714">CC003</span><span class="sxs-lookup"><span data-stu-id="c72d4-714">CC003</span></span></td>
<td><span data-ttu-id="c72d4-715">Paketleme</span><span class="sxs-lookup"><span data-stu-id="c72d4-715">Packaging</span></span></td>
<td><span data-ttu-id="c72d4-716">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-716">10001</span></span></td>
<td><span data-ttu-id="c72d4-717">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-717">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-718">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-718">Fixed cost</span></span></td>
<td><span data-ttu-id="c72d4-719">286.25</span><span class="sxs-lookup"><span data-stu-id="c72d4-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-720">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="c72d4-721">CC003</span><span class="sxs-lookup"><span data-stu-id="c72d4-721">CC003</span></span></td>
<td><span data-ttu-id="c72d4-722">Paketleme</span><span class="sxs-lookup"><span data-stu-id="c72d4-722">Packaging</span></span></td>
<td><span data-ttu-id="c72d4-723">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-723">10001</span></span></td>
<td><span data-ttu-id="c72d4-724">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-724">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-725">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-725">Variable cost</span></span></td>
<td><span data-ttu-id="c72d4-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="c72d4-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-727">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="c72d4-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-728">Prod 1</span></span></td>
<td><span data-ttu-id="c72d4-729">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-729">Product 1</span></span></td>
<td><span data-ttu-id="c72d4-730">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-730">10001</span></span></td>
<td><span data-ttu-id="c72d4-731">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-731">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-732">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-732">Fixed cost</span></span></td>
<td><span data-ttu-id="c72d4-733">776.36</span><span class="sxs-lookup"><span data-stu-id="c72d4-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-734">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="c72d4-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-735">Prod 1</span></span></td>
<td><span data-ttu-id="c72d4-736">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-736">Product 1</span></span></td>
<td><span data-ttu-id="c72d4-737">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-737">10001</span></span></td>
<td><span data-ttu-id="c72d4-738">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-738">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-739">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-739">Variable cost</span></span></td>
<td><span data-ttu-id="c72d4-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="c72d4-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-741">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="c72d4-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="c72d4-742">Prod 2</span></span></td>
<td><span data-ttu-id="c72d4-743">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-743">Product 1</span></span></td>
<td><span data-ttu-id="c72d4-744">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-744">10001</span></span></td>
<td><span data-ttu-id="c72d4-745">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-745">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-746">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-746">Fixed cost</span></span></td>
<td><span data-ttu-id="c72d4-747">223.64</span><span class="sxs-lookup"><span data-stu-id="c72d4-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-748">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="c72d4-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="c72d4-749">Prod 2</span></span></td>
<td><span data-ttu-id="c72d4-750">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-750">Product 1</span></span></td>
<td><span data-ttu-id="c72d4-751">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-751">10001</span></span></td>
<td><span data-ttu-id="c72d4-752">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-752">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-753">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-753">Variable cost</span></span></td>
<td><span data-ttu-id="c72d4-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="c72d4-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c72d4-755">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="c72d4-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c72d4-756">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="c72d4-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c72d4-757">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="c72d4-757">Cost element</span></span></th>
<th><span data-ttu-id="c72d4-758">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="c72d4-758">Cost behavior</span></span></th>
<th><span data-ttu-id="c72d4-759">Tutar</span><span class="sxs-lookup"><span data-stu-id="c72d4-759">Amount</span></span></th>
<th><span data-ttu-id="c72d4-760">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="c72d4-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c72d4-761">CC001</span><span class="sxs-lookup"><span data-stu-id="c72d4-761">CC001</span></span></td>
<td><span data-ttu-id="c72d4-762">İK</span><span class="sxs-lookup"><span data-stu-id="c72d4-762">HR</span></span></td>
<td><span data-ttu-id="c72d4-763">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-763">10001</span></span></td>
<td><span data-ttu-id="c72d4-764">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-764">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-765">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-765">Fixed cost</span></span></td>
<td><span data-ttu-id="c72d4-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="c72d4-766">-500.00</span></span></td>
<td><span data-ttu-id="c72d4-767">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-768">CC002</span><span class="sxs-lookup"><span data-stu-id="c72d4-768">CC002</span></span></td>
<td><span data-ttu-id="c72d4-769">Finans</span><span class="sxs-lookup"><span data-stu-id="c72d4-769">Finance</span></span></td>
<td><span data-ttu-id="c72d4-770">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-770">10001</span></span></td>
<td><span data-ttu-id="c72d4-771">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-771">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-772">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-772">Fixed cost</span></span></td>
<td><span data-ttu-id="c72d4-773">175.00</span><span class="sxs-lookup"><span data-stu-id="c72d4-773">175.00</span></span></td>
<td><span data-ttu-id="c72d4-774">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-775">CC003</span><span class="sxs-lookup"><span data-stu-id="c72d4-775">CC003</span></span></td>
<td><span data-ttu-id="c72d4-776">Montaj</span><span class="sxs-lookup"><span data-stu-id="c72d4-776">Assembly</span></span></td>
<td><span data-ttu-id="c72d4-777">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-777">10001</span></span></td>
<td><span data-ttu-id="c72d4-778">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-778">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-779">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-779">Fixed cost</span></span></td>
<td><span data-ttu-id="c72d4-780">275.00</span><span class="sxs-lookup"><span data-stu-id="c72d4-780">275.00</span></span></td>
<td><span data-ttu-id="c72d4-781">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-782">CC004</span><span class="sxs-lookup"><span data-stu-id="c72d4-782">CC004</span></span></td>
<td><span data-ttu-id="c72d4-783">Paketleme</span><span class="sxs-lookup"><span data-stu-id="c72d4-783">Packaging</span></span></td>
<td><span data-ttu-id="c72d4-784">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-784">10001</span></span></td>
<td><span data-ttu-id="c72d4-785">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-785">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-786">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-786">Fixed cost</span></span></td>
<td><span data-ttu-id="c72d4-787">50,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-787">50,00</span></span></td>
<td><span data-ttu-id="c72d4-788">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-789">CC001</span><span class="sxs-lookup"><span data-stu-id="c72d4-789">CC001</span></span></td>
<td><span data-ttu-id="c72d4-790">İK</span><span class="sxs-lookup"><span data-stu-id="c72d4-790">HR</span></span></td>
<td><span data-ttu-id="c72d4-791">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-791">10001</span></span></td>
<td><span data-ttu-id="c72d4-792">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-792">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-793">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-793">Variable cost</span></span></td>
<td><span data-ttu-id="c72d4-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="c72d4-794">-1,245.71</span></span></td>
<td><span data-ttu-id="c72d4-795">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-796">CC002</span><span class="sxs-lookup"><span data-stu-id="c72d4-796">CC002</span></span></td>
<td><span data-ttu-id="c72d4-797">Finans</span><span class="sxs-lookup"><span data-stu-id="c72d4-797">Finance</span></span></td>
<td><span data-ttu-id="c72d4-798">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-798">10001</span></span></td>
<td><span data-ttu-id="c72d4-799">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-799">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-800">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-800">Variable cost</span></span></td>
<td><span data-ttu-id="c72d4-801">436.00</span><span class="sxs-lookup"><span data-stu-id="c72d4-801">436.00</span></span></td>
<td><span data-ttu-id="c72d4-802">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-803">CC003</span><span class="sxs-lookup"><span data-stu-id="c72d4-803">CC003</span></span></td>
<td><span data-ttu-id="c72d4-804">Montaj</span><span class="sxs-lookup"><span data-stu-id="c72d4-804">Assembly</span></span></td>
<td><span data-ttu-id="c72d4-805">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-805">10001</span></span></td>
<td><span data-ttu-id="c72d4-806">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-806">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-807">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-807">Variable cost</span></span></td>
<td><span data-ttu-id="c72d4-808">685.14</span><span class="sxs-lookup"><span data-stu-id="c72d4-808">685.14</span></span></td>
<td><span data-ttu-id="c72d4-809">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-810">CC004</span><span class="sxs-lookup"><span data-stu-id="c72d4-810">CC004</span></span></td>
<td><span data-ttu-id="c72d4-811">Paketleme</span><span class="sxs-lookup"><span data-stu-id="c72d4-811">Packaging</span></span></td>
<td><span data-ttu-id="c72d4-812">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-812">10001</span></span></td>
<td><span data-ttu-id="c72d4-813">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-813">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-814">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-814">Variable cost</span></span></td>
<td><span data-ttu-id="c72d4-815">124.57</span><span class="sxs-lookup"><span data-stu-id="c72d4-815">124.57</span></span></td>
<td><span data-ttu-id="c72d4-816">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-817">CC002</span><span class="sxs-lookup"><span data-stu-id="c72d4-817">CC002</span></span></td>
<td><span data-ttu-id="c72d4-818">Finans</span><span class="sxs-lookup"><span data-stu-id="c72d4-818">Finance</span></span></td>
<td><span data-ttu-id="c72d4-819">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-819">10001</span></span></td>
<td><span data-ttu-id="c72d4-820">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-820">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-821">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-821">Fixed cost</span></span></td>
<td><span data-ttu-id="c72d4-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-822">-675.00</span></span></td>
<td><span data-ttu-id="c72d4-823">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-824">CC003</span><span class="sxs-lookup"><span data-stu-id="c72d4-824">CC003</span></span></td>
<td><span data-ttu-id="c72d4-825">Montaj</span><span class="sxs-lookup"><span data-stu-id="c72d4-825">Assembly</span></span></td>
<td><span data-ttu-id="c72d4-826">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-826">10001</span></span></td>
<td><span data-ttu-id="c72d4-827">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-827">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-828">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-828">Fixed cost</span></span></td>
<td><span data-ttu-id="c72d4-829">438.75</span><span class="sxs-lookup"><span data-stu-id="c72d4-829">438.75</span></span></td>
<td><span data-ttu-id="c72d4-830">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-831">CC004</span><span class="sxs-lookup"><span data-stu-id="c72d4-831">CC004</span></span></td>
<td><span data-ttu-id="c72d4-832">Paketleme</span><span class="sxs-lookup"><span data-stu-id="c72d4-832">Packaging</span></span></td>
<td><span data-ttu-id="c72d4-833">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-833">10001</span></span></td>
<td><span data-ttu-id="c72d4-834">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-834">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-835">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-835">Fixed cost</span></span></td>
<td><span data-ttu-id="c72d4-836">236.25</span><span class="sxs-lookup"><span data-stu-id="c72d4-836">236.25</span></span></td>
<td><span data-ttu-id="c72d4-837">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-838">CC002</span><span class="sxs-lookup"><span data-stu-id="c72d4-838">CC002</span></span></td>
<td><span data-ttu-id="c72d4-839">Finans</span><span class="sxs-lookup"><span data-stu-id="c72d4-839">Finance</span></span></td>
<td><span data-ttu-id="c72d4-840">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-840">10001</span></span></td>
<td><span data-ttu-id="c72d4-841">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-841">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-842">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-842">Variable cost</span></span></td>
<td><span data-ttu-id="c72d4-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="c72d4-843">-8,150.29</span></span></td>
<td><span data-ttu-id="c72d4-844">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-845">CC003</span><span class="sxs-lookup"><span data-stu-id="c72d4-845">CC003</span></span></td>
<td><span data-ttu-id="c72d4-846">Montaj</span><span class="sxs-lookup"><span data-stu-id="c72d4-846">Assembly</span></span></td>
<td><span data-ttu-id="c72d4-847">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-847">10001</span></span></td>
<td><span data-ttu-id="c72d4-848">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-848">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-849">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-849">Variable cost</span></span></td>
<td><span data-ttu-id="c72d4-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="c72d4-850">5,297.69</span></span></td>
<td><span data-ttu-id="c72d4-851">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-852">CC004</span><span class="sxs-lookup"><span data-stu-id="c72d4-852">CC004</span></span></td>
<td><span data-ttu-id="c72d4-853">Paketleme</span><span class="sxs-lookup"><span data-stu-id="c72d4-853">Packaging</span></span></td>
<td><span data-ttu-id="c72d4-854">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-854">10001</span></span></td>
<td><span data-ttu-id="c72d4-855">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-855">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-856">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-856">Variable cost</span></span></td>
<td><span data-ttu-id="c72d4-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="c72d4-857">2,852.60</span></span></td>
<td><span data-ttu-id="c72d4-858">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-859">CC003</span><span class="sxs-lookup"><span data-stu-id="c72d4-859">CC003</span></span></td>
<td><span data-ttu-id="c72d4-860">Montaj</span><span class="sxs-lookup"><span data-stu-id="c72d4-860">Assembly</span></span></td>
<td><span data-ttu-id="c72d4-861">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-861">10001</span></span></td>
<td><span data-ttu-id="c72d4-862">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-862">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-863">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-863">Fixed cost</span></span></td>
<td><span data-ttu-id="c72d4-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="c72d4-864">-713.75</span></span></td>
<td><span data-ttu-id="c72d4-865">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-866">Prod 1</span></span></td>
<td><span data-ttu-id="c72d4-867">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-867">Product 1</span></span></td>
<td><span data-ttu-id="c72d4-868">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-868">10001</span></span></td>
<td><span data-ttu-id="c72d4-869">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-869">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-870">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-870">Fixed cost</span></span></td>
<td><span data-ttu-id="c72d4-871">535.31</span><span class="sxs-lookup"><span data-stu-id="c72d4-871">535.31</span></span></td>
<td><span data-ttu-id="c72d4-872">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="c72d4-873">Prod 2</span></span></td>
<td><span data-ttu-id="c72d4-874">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="c72d4-874">Product 2</span></span></td>
<td><span data-ttu-id="c72d4-875">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-875">10001</span></span></td>
<td><span data-ttu-id="c72d4-876">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-876">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-877">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-877">Fixed cost</span></span></td>
<td><span data-ttu-id="c72d4-878">178.44</span><span class="sxs-lookup"><span data-stu-id="c72d4-878">178.44</span></span></td>
<td><span data-ttu-id="c72d4-879">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-880">CC003</span><span class="sxs-lookup"><span data-stu-id="c72d4-880">CC003</span></span></td>
<td><span data-ttu-id="c72d4-881">Montaj</span><span class="sxs-lookup"><span data-stu-id="c72d4-881">Assembly</span></span></td>
<td><span data-ttu-id="c72d4-882">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-882">10001</span></span></td>
<td><span data-ttu-id="c72d4-883">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-883">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-884">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-884">Variable cost</span></span></td>
<td><span data-ttu-id="c72d4-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="c72d4-885">-5,982.83</span></span></td>
<td><span data-ttu-id="c72d4-886">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-887">Prod 1</span></span></td>
<td><span data-ttu-id="c72d4-888">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-888">Product 1</span></span></td>
<td><span data-ttu-id="c72d4-889">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-889">10001</span></span></td>
<td><span data-ttu-id="c72d4-890">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-890">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-891">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-891">Variable cost</span></span></td>
<td><span data-ttu-id="c72d4-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="c72d4-892">4,487.12</span></span></td>
<td><span data-ttu-id="c72d4-893">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="c72d4-894">Prod 2</span></span></td>
<td><span data-ttu-id="c72d4-895">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="c72d4-895">Product 2</span></span></td>
<td><span data-ttu-id="c72d4-896">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-896">10001</span></span></td>
<td><span data-ttu-id="c72d4-897">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-897">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-898">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-898">Variable cost</span></span></td>
<td><span data-ttu-id="c72d4-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="c72d4-899">1,495.71</span></span></td>
<td><span data-ttu-id="c72d4-900">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-901">CC003</span><span class="sxs-lookup"><span data-stu-id="c72d4-901">CC003</span></span></td>
<td><span data-ttu-id="c72d4-902">Montaj</span><span class="sxs-lookup"><span data-stu-id="c72d4-902">Assembly</span></span></td>
<td><span data-ttu-id="c72d4-903">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-903">10001</span></span></td>
<td><span data-ttu-id="c72d4-904">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-904">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-905">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-905">Fixed cost</span></span></td>
<td><span data-ttu-id="c72d4-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="c72d4-906">-286.25</span></span></td>
<td><span data-ttu-id="c72d4-907">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-908">Prod 1</span></span></td>
<td><span data-ttu-id="c72d4-909">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-909">Product 1</span></span></td>
<td><span data-ttu-id="c72d4-910">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-910">10001</span></span></td>
<td><span data-ttu-id="c72d4-911">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-911">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-912">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-912">Fixed cost</span></span></td>
<td><span data-ttu-id="c72d4-913">241.05</span><span class="sxs-lookup"><span data-stu-id="c72d4-913">241.05</span></span></td>
<td><span data-ttu-id="c72d4-914">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="c72d4-915">Prod 2</span></span></td>
<td><span data-ttu-id="c72d4-916">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="c72d4-916">Product 2</span></span></td>
<td><span data-ttu-id="c72d4-917">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-917">10001</span></span></td>
<td><span data-ttu-id="c72d4-918">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-918">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-919">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-919">Fixed cost</span></span></td>
<td><span data-ttu-id="c72d4-920">45.20</span><span class="sxs-lookup"><span data-stu-id="c72d4-920">45.20</span></span></td>
<td><span data-ttu-id="c72d4-921">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-922">CC003</span><span class="sxs-lookup"><span data-stu-id="c72d4-922">CC003</span></span></td>
<td><span data-ttu-id="c72d4-923">Montaj</span><span class="sxs-lookup"><span data-stu-id="c72d4-923">Assembly</span></span></td>
<td><span data-ttu-id="c72d4-924">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-924">10001</span></span></td>
<td><span data-ttu-id="c72d4-925">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-925">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-926">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-926">Variable cost</span></span></td>
<td><span data-ttu-id="c72d4-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="c72d4-927">-2,977.17</span></span></td>
<td><span data-ttu-id="c72d4-928">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-929">Prod 1</span></span></td>
<td><span data-ttu-id="c72d4-930">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-930">Product 1</span></span></td>
<td><span data-ttu-id="c72d4-931">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-931">10001</span></span></td>
<td><span data-ttu-id="c72d4-932">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-932">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-933">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-933">Variable cost</span></span></td>
<td><span data-ttu-id="c72d4-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="c72d4-934">2,507.09</span></span></td>
<td><span data-ttu-id="c72d4-935">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c72d4-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="c72d4-936">Prod 2</span></span></td>
<td><span data-ttu-id="c72d4-937">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="c72d4-937">Product 2</span></span></td>
<td><span data-ttu-id="c72d4-938">10001</span><span class="sxs-lookup"><span data-stu-id="c72d4-938">10001</span></span></td>
<td><span data-ttu-id="c72d4-939">Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-939">Electricity</span></span></td>
<td><span data-ttu-id="c72d4-940">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-940">Variable cost</span></span></td>
<td><span data-ttu-id="c72d4-941">470.08</span><span class="sxs-lookup"><span data-stu-id="c72d4-941">470.08</span></span></td>
<td><span data-ttu-id="c72d4-942">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="c72d4-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="c72d4-943">Sonuç</span><span class="sxs-lookup"><span data-stu-id="c72d4-943">Conclusion</span></span>
<span data-ttu-id="c72d4-944">Mali muhasebede, Elektrik için 10.000,00 maliyet bir sözde maliyet merkezi kimliğine nakledilmiştir.</span><span class="sxs-lookup"><span data-stu-id="c72d4-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="c72d4-945">Bu nedenle, maliyet muhasebecileri bu maliyetin tahsis edilmesi gerektiğini bilirler.</span><span class="sxs-lookup"><span data-stu-id="c72d4-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="c72d4-946">Maliyet muhasebesinde, maliyetler kuruluş birimleri ve seviyeleri arasında, uygulanan kural ve ilkelere dayalı olarak akar.</span><span class="sxs-lookup"><span data-stu-id="c72d4-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="c72d4-947">Her maliyet, maliyetlerin tahsisatı için en iyi değerlendirmeyi sağlayan bir tahsisat tabanı ile ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="c72d4-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="c72d4-948">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="c72d4-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="c72d4-949">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="c72d4-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="c72d4-950">Toplam</span><span class="sxs-lookup"><span data-stu-id="c72d4-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="c72d4-951">CC099</span><span class="sxs-lookup"><span data-stu-id="c72d4-951">CC099</span></span></th>
<th><span data-ttu-id="c72d4-952">CC001</span><span class="sxs-lookup"><span data-stu-id="c72d4-952">CC001</span></span></th>
<th><span data-ttu-id="c72d4-953">CC002</span><span class="sxs-lookup"><span data-stu-id="c72d4-953">CC002</span></span></th>
<th><span data-ttu-id="c72d4-954">CC003</span><span class="sxs-lookup"><span data-stu-id="c72d4-954">CC003</span></span></th>
<th><span data-ttu-id="c72d4-955">CC004</span><span class="sxs-lookup"><span data-stu-id="c72d4-955">CC004</span></span></th>
<th><span data-ttu-id="c72d4-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-956">Proj 1</span></span></th>
<th><span data-ttu-id="c72d4-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="c72d4-957">Proj 2</span></span></th>
<th><span data-ttu-id="c72d4-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="c72d4-958">Prod 1</span></span></th>
<th><span data-ttu-id="c72d4-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="c72d4-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="c72d4-960">10001 Elektrik</span><span class="sxs-lookup"><span data-stu-id="c72d4-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c72d4-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="c72d4-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c72d4-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="c72d4-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c72d4-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="c72d4-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c72d4-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="c72d4-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="c72d4-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="c72d4-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c72d4-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="c72d4-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c72d4-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="c72d4-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c72d4-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="c72d4-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c72d4-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="c72d4-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="c72d4-970">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="c72d4-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c72d4-971">0,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="c72d4-972">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c72d4-973">0,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c72d4-974">0,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c72d4-975">0,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c72d4-976">0,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c72d4-977">0,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="c72d4-978">776.36</span><span class="sxs-lookup"><span data-stu-id="c72d4-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c72d4-979">223.64</span><span class="sxs-lookup"><span data-stu-id="c72d4-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c72d4-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="c72d4-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="c72d4-981">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="c72d4-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c72d4-982">000</span><span class="sxs-lookup"><span data-stu-id="c72d4-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c72d4-983">0,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c72d4-984">0,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c72d4-985">0,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c72d4-986">0,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c72d4-987">30.00</span><span class="sxs-lookup"><span data-stu-id="c72d4-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c72d4-988">10,00</span><span class="sxs-lookup"><span data-stu-id="c72d4-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c72d4-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="c72d4-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c72d4-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="c72d4-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c72d4-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="c72d4-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="c72d4-992">Bu konu, birincil maliyet öğesi, 10001 Elektrik'in maliyet nesneleri arasında nasıl aktığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c72d4-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="c72d4-993">Bu nedenle, bu genel gider maliyeti kuruluşun en düşük seviyesine tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="c72d4-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="c72d4-994">Başka bir deyişle, maliyet en alt düzeydeki maliyet nesnelerine aittir.</span><span class="sxs-lookup"><span data-stu-id="c72d4-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="c72d4-995">Maliyetin, maliyet nesneleri arasında görsel bir akışına ihtiyacınız varsa, maliyetin akışını görselleştirmek için maliyet toplamı ilke kurallarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c72d4-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="c72d4-996">Daha fazla bilgi için [Maliyet yukarı yuvarlama](cost-rollup.md) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="c72d4-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>




