---
title: "Genel gider hesaplaması"
description: "Bu konu, genel gider maliyetlerinin hesaplanması için tipik işlemleri açıklar."
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2f37b5957974c927ade698fea65de7e3807d998a
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---

# <a name="overhead-calculation"></a><span data-ttu-id="4b3fd-103">Genel gider hesaplaması</span><span class="sxs-lookup"><span data-stu-id="4b3fd-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4b3fd-104">Bu konu, genel gider maliyetlerinin hesaplanması için tipik işlemleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="4b3fd-105">Terim tanımı</span><span class="sxs-lookup"><span data-stu-id="4b3fd-105">Term definition</span></span>
---------------

<span data-ttu-id="4b3fd-106">Genel gider maliyetleri bir işletmenin çalışması için normalde uygulanan, ancak doğrudan herhangi bir özel iş, faaliyet, ürün veya hizmete ilişkilendirilmemiş olan maliyetlerdir.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="4b3fd-107">Genel gider maliyetleri kar sağlama faaliyetlerinin oluşturulması için kritik destek sağlar.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="4b3fd-108">Aşağıda bazı genel gider örnekleri verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="4b3fd-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="4b3fd-109">Kira</span><span class="sxs-lookup"><span data-stu-id="4b3fd-109">Rent</span></span>
-   <span data-ttu-id="4b3fd-110">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-110">Electricity</span></span>
-   <span data-ttu-id="4b3fd-111">Yönetim maaşları</span><span class="sxs-lookup"><span data-stu-id="4b3fd-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="4b3fd-112">Genel gider hesaplaması genel bakış</span><span class="sxs-lookup"><span data-stu-id="4b3fd-112">Overhead calculation overview</span></span>
<span data-ttu-id="4b3fd-113">Genel gider hesaplama, maliyet muhasebesi ilkelerini doğru sırayla çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="4b3fd-114">Maliyet muhasebesi ilkeleri değiştiyse veya belirli hatalar algılandıysa, genel gider hesaplamasını aynı mali dönem için birden fazla kez yürütebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="4b3fd-115">Her genel gider hesaplaması depolanır ve önceki sürümlerdeki hesaplamaları kıyaslamanıza olanak sağlayan, benzersiz bir sürüm kimliğine sahip olur.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="4b3fd-116">Genel gider hesaplamasının oluşturduğu maliyet girişleri bir muhasebe tarihi alır.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="4b3fd-117">Bu muhasebe tarihi, hesaplamada kullanılan mali dönemin bitiş tarihiyle eşleşir.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="4b3fd-118">Benzersiz sürüm kimliği aşağıdaki öğelerden oluşur:</span><span class="sxs-lookup"><span data-stu-id="4b3fd-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="4b3fd-119">Sürüm türü</span><span class="sxs-lookup"><span data-stu-id="4b3fd-119">Version type</span></span>
-   <span data-ttu-id="4b3fd-120">Tarih ve saat</span><span class="sxs-lookup"><span data-stu-id="4b3fd-120">Date and time</span></span>
-   <span data-ttu-id="4b3fd-121">Maliyet muhasebesi defteri</span><span class="sxs-lookup"><span data-stu-id="4b3fd-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="4b3fd-122">Mali yıl</span><span class="sxs-lookup"><span data-stu-id="4b3fd-122">Fiscal year</span></span>
-   <span data-ttu-id="4b3fd-123">Mali dönem</span><span class="sxs-lookup"><span data-stu-id="4b3fd-123">Fiscal period</span></span>

<span data-ttu-id="4b3fd-124">Genel gider hesaplama, sürümden bağımsız olarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="4b3fd-125">Bu nedenle, Gerçek sürümden önce Bütçe sürümünü hesaplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="4b3fd-126">Genel gider hesaplama dört adımdan oluşur, aşağıdaki çizimde gösterildiği gibi.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="4b3fd-127">Her adımda, günlük girişleri olan bir günlük başlığı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="4b3fd-128">Bu günlük başlığı, her hesaplama adımı için giriş verilerini tutar.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="4b3fd-129">İlkeler ve kurallar her günlük satırına uygulanır ve maliyet girişleri çıkış olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="4b3fd-130">Bu nedenle, her zaman tam izlenebilirliğe sahip olursunuz.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="4b3fd-131">[![Genel gider hesaplaması](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="4b3fd-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="4b3fd-132">Elektrik genel gideri maliyetini hesapla ve tahsis et</span><span class="sxs-lookup"><span data-stu-id="4b3fd-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="4b3fd-133">Mali muhasebede, elektrik gibi bazı maliyetler peşin ödeme olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="4b3fd-134">Bu nedenle, Maliyet muhasebesi için ayrıntılı yönetim bilgiler sağlanmaz.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="4b3fd-135">Maliyet muhasebesinde doğru yönetimsel bilgileri tüm yönetim birim ve düzeylerinde sağlamak için, maliyetlerin kuruluş birimleri arasında akması gerekir.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="4b3fd-136">Bu akış, tüketimin doğru bir kaydına ya da adil bir değerlendirmeye dayanıyor olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="4b3fd-137">Genel muhasebede, bir elektrik maliyeti aşağıdaki tabloda gösterildiği gibi deftere nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4b3fd-138">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4b3fd-139">Maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="4b3fd-140">Ana hesap</span><span class="sxs-lookup"><span data-stu-id="4b3fd-140">Main account</span></span></th>
<th><span data-ttu-id="4b3fd-141">Muhasebe para birimi cinsinden tutar</span><span class="sxs-lookup"><span data-stu-id="4b3fd-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b3fd-142">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="4b3fd-143">CC099</span><span class="sxs-lookup"><span data-stu-id="4b3fd-143">CC099</span></span></td>
<td><span data-ttu-id="4b3fd-144">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-144">Default cost center</span></span></td>
<td><span data-ttu-id="4b3fd-145">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-145">10001</span></span></td>
<td><span data-ttu-id="4b3fd-146">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-146">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="4b3fd-148">Adım 1: Maliyet davranışı hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="4b3fd-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="4b3fd-149">Varsayılan olarak, maliyeti girişleri kaynak veriden içeri alındığında, Maliyet muhasebesinde **Sınıflandırılmamış** maliyet davranışı sınıflandırmasını alırlar.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="4b3fd-150">Maliyet davranışı ilke kuralları ekleyerek, maliyet girişlerini **Sabit maliyet** veya **Değişken maliyet** olarak yeniden sınıflandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="4b3fd-151">Maliyet davranış kuralını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="4b3fd-151">Define the cost behavior rule</span></span>

<span data-ttu-id="4b3fd-152">Bazı durumlarda, sabit bir ücret maliyet parçasıdır ve kalan maliyet, tüketime dayanır.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="4b3fd-153">Elektrik faturaları genellikle bu tanıma uyar.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="4b3fd-154">Belirli bir sabit ücret ödedikten sonra, kilovat saatlik (Kwh) tüketim başına ödeme yaparsınız.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="4b3fd-155">Örneğin, sabit maliyet masrafı 1.000,00 ise, maliyet davranışı kural nasıl tanımlanır:</span><span class="sxs-lookup"><span data-stu-id="4b3fd-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="4b3fd-156">Sabit tutar 1.000,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="4b3fd-157">0 &lt;= 1.000,00 = Sabit</span><span class="sxs-lookup"><span data-stu-id="4b3fd-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="4b3fd-158">1000,01 &lt; N = Değişken</span><span class="sxs-lookup"><span data-stu-id="4b3fd-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="4b3fd-159">Günlük</span><span class="sxs-lookup"><span data-stu-id="4b3fd-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4b3fd-160">Günlük</span><span class="sxs-lookup"><span data-stu-id="4b3fd-160">Journal</span></span></th>
<th><span data-ttu-id="4b3fd-161">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="4b3fd-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4b3fd-162">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4b3fd-163">Sürüm</span><span class="sxs-lookup"><span data-stu-id="4b3fd-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b3fd-164">00001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-164">00001</span></span></td>
<td><span data-ttu-id="4b3fd-165">Maliyet davranışı hesaplama günlüğü</span><span class="sxs-lookup"><span data-stu-id="4b3fd-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="4b3fd-166">Mali</span><span class="sxs-lookup"><span data-stu-id="4b3fd-166">Fiscal</span></span></td>
<td><span data-ttu-id="4b3fd-167">2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-167">2017</span></span></td>
<td><span data-ttu-id="4b3fd-168">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-168">Period 1</span></span></td>
<td><span data-ttu-id="4b3fd-169">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="4b3fd-170">Günlük girişleri (Maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="4b3fd-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4b3fd-171">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4b3fd-172">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4b3fd-173">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-173">Cost element</span></span></th>
<th><span data-ttu-id="4b3fd-174">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="4b3fd-174">Cost behavior</span></span></th>
<th><span data-ttu-id="4b3fd-175">Tutar</span><span class="sxs-lookup"><span data-stu-id="4b3fd-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b3fd-176">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="4b3fd-177">CC099</span><span class="sxs-lookup"><span data-stu-id="4b3fd-177">CC099</span></span></td>
<td><span data-ttu-id="4b3fd-178">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-178">Default cost center</span></span></td>
<td><span data-ttu-id="4b3fd-179">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-179">10001</span></span></td>
<td><span data-ttu-id="4b3fd-180">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-180">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-181">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="4b3fd-181">Unclassified</span></span></td>
<td><span data-ttu-id="4b3fd-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4b3fd-183">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="4b3fd-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b3fd-184">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4b3fd-185">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-185">Cost element</span></span></th>
<th><span data-ttu-id="4b3fd-186">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="4b3fd-186">Cost behavior</span></span></th>
<th><span data-ttu-id="4b3fd-187">Tutar</span><span class="sxs-lookup"><span data-stu-id="4b3fd-187">Amount</span></span></th>
<th><span data-ttu-id="4b3fd-188">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b3fd-189">CC099</span><span class="sxs-lookup"><span data-stu-id="4b3fd-189">CC099</span></span></td>
<td><span data-ttu-id="4b3fd-190">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-190">Default cost center</span></span></td>
<td><span data-ttu-id="4b3fd-191">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-191">10001</span></span></td>
<td><span data-ttu-id="4b3fd-192">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-192">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-193">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="4b3fd-193">Unclassified</span></span></td>
<td><span data-ttu-id="4b3fd-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-194">10,000.00</span></span></td>
<td><span data-ttu-id="4b3fd-195">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-196">CC099</span><span class="sxs-lookup"><span data-stu-id="4b3fd-196">CC099</span></span></td>
<td><span data-ttu-id="4b3fd-197">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-197">Default cost center</span></span></td>
<td><span data-ttu-id="4b3fd-198">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-198">10001</span></span></td>
<td><span data-ttu-id="4b3fd-199">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-199">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-200">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="4b3fd-200">Unclassified</span></span></td>
<td><span data-ttu-id="4b3fd-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-201">-10,000.00</span></span></td>
<td><span data-ttu-id="4b3fd-202">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-203">CC099</span><span class="sxs-lookup"><span data-stu-id="4b3fd-203">CC099</span></span></td>
<td><span data-ttu-id="4b3fd-204">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-204">Default cost center</span></span></td>
<td><span data-ttu-id="4b3fd-205">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-205">10001</span></span></td>
<td><span data-ttu-id="4b3fd-206">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-206">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-207">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-207">Fixed cost</span></span></td>
<td><span data-ttu-id="4b3fd-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-208">1,000.00</span></span></td>
<td><span data-ttu-id="4b3fd-209">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-210">CC099</span><span class="sxs-lookup"><span data-stu-id="4b3fd-210">CC099</span></span></td>
<td><span data-ttu-id="4b3fd-211">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-211">Default cost center</span></span></td>
<td><span data-ttu-id="4b3fd-212">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-212">10001</span></span></td>
<td><span data-ttu-id="4b3fd-213">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-213">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-214">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-214">Variable cost</span></span></td>
<td><span data-ttu-id="4b3fd-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-215">9,000.00</span></span></td>
<td><span data-ttu-id="4b3fd-216">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4b3fd-217">Maliyet davranışı hakkında ayrıntılı bilgi için bkz. Maliyet davranışı ilkesi.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="4b3fd-218">(Bu konunun henüz tamamlanmadığını ancak yakında tamamlanacağını göz önünde bulundurun.)</span><span class="sxs-lookup"><span data-stu-id="4b3fd-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="4b3fd-219">Adım 2: Maliyet dağıtımı hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="4b3fd-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="4b3fd-220">Maliyet dağıtımı, bir nesneden bir veya daha fazlasına ilgili tahsisat tabanı uygulayarak maliyeti yeniden dağıtmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="4b3fd-221">Maliyet dağıtımı ve maliyet tahsisatı, maliyet dağıtımının her zaman orijinal maliyetin birincil maliyet öğesinde bulunmasıyla farklılık gösterir.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="4b3fd-222">Maliyet dağıtım kuralını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="4b3fd-222">Define the cost distribution rule</span></span>

<span data-ttu-id="4b3fd-223">Mali muhasebede, elektrik maliyetleri çoğu zaman peşin ödeme olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="4b3fd-224">Maliyet muhasebesinde ise bu yöntem yeterince ayrıntılı değildir.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="4b3fd-225">Değişken maliyet, maliyet nesnelerine tek tek, adil bir temele dayanarak dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="4b3fd-226">En mantıklı tahsisat, elektrik kullanımını (Kwh) temel alarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="4b3fd-227">Elektrik adına sahip, istatistiksel bir boyut üyesi oluşturulur ve elektrik tüketimi kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="4b3fd-228">Varsayıla olarak, tüm istatistiksel boyut üyeleri tahsisat tabanları olarak kullanılabilir hale gelir.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b3fd-229">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-229">Cost object</span></span></th>
<th><span data-ttu-id="4b3fd-230">Kwh</span><span class="sxs-lookup"><span data-stu-id="4b3fd-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b3fd-231">CC001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-231">CC001</span></span></td>
<td><span data-ttu-id="4b3fd-232">İK</span><span class="sxs-lookup"><span data-stu-id="4b3fd-232">HR</span></span></td>
<td><span data-ttu-id="4b3fd-233">1.000</span><span class="sxs-lookup"><span data-stu-id="4b3fd-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-234">CC002</span><span class="sxs-lookup"><span data-stu-id="4b3fd-234">CC002</span></span></td>
<td><span data-ttu-id="4b3fd-235">Finans</span><span class="sxs-lookup"><span data-stu-id="4b3fd-235">Finance</span></span></td>
<td><span data-ttu-id="4b3fd-236">6,000</span><span class="sxs-lookup"><span data-stu-id="4b3fd-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-237">CC003</span><span class="sxs-lookup"><span data-stu-id="4b3fd-237">CC003</span></span></td>
<td><span data-ttu-id="4b3fd-238">Montaj</span><span class="sxs-lookup"><span data-stu-id="4b3fd-238">Assembly</span></span></td>
<td><span data-ttu-id="4b3fd-239">0</span><span class="sxs-lookup"><span data-stu-id="4b3fd-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4b3fd-240">Aşağıdaki tablo, elektrik tüketiminin değişken maliyetler için bir tahsisat tabanlı olarak uygulandığındaki sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b3fd-241">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-241">Cost object</span></span></th>
<th><span data-ttu-id="4b3fd-242">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="4b3fd-242">Magnitude</span></span></th>
<th><span data-ttu-id="4b3fd-243">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="4b3fd-243">Allocation factor</span></span></th>
<th><span data-ttu-id="4b3fd-244">Tutar</span><span class="sxs-lookup"><span data-stu-id="4b3fd-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b3fd-245">CC001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-245">CC001</span></span></td>
<td><span data-ttu-id="4b3fd-246">İK</span><span class="sxs-lookup"><span data-stu-id="4b3fd-246">HR</span></span></td>
<td><span data-ttu-id="4b3fd-247">1.000</span><span class="sxs-lookup"><span data-stu-id="4b3fd-247">1,000</span></span></td>
<td><span data-ttu-id="4b3fd-248">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="4b3fd-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="4b3fd-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-250">CC002</span><span class="sxs-lookup"><span data-stu-id="4b3fd-250">CC002</span></span></td>
<td><span data-ttu-id="4b3fd-251">Finans</span><span class="sxs-lookup"><span data-stu-id="4b3fd-251">Finance</span></span></td>
<td><span data-ttu-id="4b3fd-252">6,000</span><span class="sxs-lookup"><span data-stu-id="4b3fd-252">6,000</span></span></td>
<td><span data-ttu-id="4b3fd-253">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="4b3fd-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="4b3fd-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-255">CC003</span><span class="sxs-lookup"><span data-stu-id="4b3fd-255">CC003</span></span></td>
<td><span data-ttu-id="4b3fd-256">Montaj</span><span class="sxs-lookup"><span data-stu-id="4b3fd-256">Assembly</span></span></td>
<td><span data-ttu-id="4b3fd-257">0</span><span class="sxs-lookup"><span data-stu-id="4b3fd-257">0</span></span></td>
<td><span data-ttu-id="4b3fd-258">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="4b3fd-259">0,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4b3fd-260">Sabit maliyet, elektrik tüketmiş olan tekil maliyet nesnelerine eşit miktarda dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="4b3fd-261">Bu sonuca, Elektrik istatistiksel boyut öğesini bir formül tahsisat tabanında kullanarak ulaşabilirsiniz: (Elektrik &gt; 0,00) Aşağıdaki tablo, elektrik tüketimi değişken maliyetler için bir tahsisat tabanı olarak kullanıldığında ortaya çıkan sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b3fd-262">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-262">Cost object</span></span></th>
<th><span data-ttu-id="4b3fd-263">Formül</span><span class="sxs-lookup"><span data-stu-id="4b3fd-263">Formula</span></span></th>
<th><span data-ttu-id="4b3fd-264">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="4b3fd-264">Magnitude</span></span></th>
<th><span data-ttu-id="4b3fd-265">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="4b3fd-265">Allocation factor</span></span></th>
<th><span data-ttu-id="4b3fd-266">Tutar</span><span class="sxs-lookup"><span data-stu-id="4b3fd-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b3fd-267">CC001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-267">CC001</span></span></td>
<td><span data-ttu-id="4b3fd-268">İK</span><span class="sxs-lookup"><span data-stu-id="4b3fd-268">HR</span></span></td>
<td><span data-ttu-id="4b3fd-269">(1,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="4b3fd-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="4b3fd-270">1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-270">1</span></span></td>
<td><span data-ttu-id="4b3fd-271">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="4b3fd-272">500.00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-273">CC002</span><span class="sxs-lookup"><span data-stu-id="4b3fd-273">CC002</span></span></td>
<td><span data-ttu-id="4b3fd-274">Finans</span><span class="sxs-lookup"><span data-stu-id="4b3fd-274">Finance</span></span></td>
<td><span data-ttu-id="4b3fd-275">(6,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="4b3fd-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="4b3fd-276">1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-276">1</span></span></td>
<td><span data-ttu-id="4b3fd-277">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="4b3fd-278">500.00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-279">CC003</span><span class="sxs-lookup"><span data-stu-id="4b3fd-279">CC003</span></span></td>
<td><span data-ttu-id="4b3fd-280">Montaj</span><span class="sxs-lookup"><span data-stu-id="4b3fd-280">Assembly</span></span></td>
<td><span data-ttu-id="4b3fd-281">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="4b3fd-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="4b3fd-282">0</span><span class="sxs-lookup"><span data-stu-id="4b3fd-282">0</span></span></td>
<td><span data-ttu-id="4b3fd-283">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="4b3fd-284">0,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="4b3fd-285">Günlük</span><span class="sxs-lookup"><span data-stu-id="4b3fd-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4b3fd-286">Günlük</span><span class="sxs-lookup"><span data-stu-id="4b3fd-286">Journal</span></span></th>
<th><span data-ttu-id="4b3fd-287">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="4b3fd-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4b3fd-288">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4b3fd-289">Sürüm</span><span class="sxs-lookup"><span data-stu-id="4b3fd-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b3fd-290">00002</span><span class="sxs-lookup"><span data-stu-id="4b3fd-290">00002</span></span></td>
<td><span data-ttu-id="4b3fd-291">Maliyet dağıtımı hesaplama günlüğü</span><span class="sxs-lookup"><span data-stu-id="4b3fd-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="4b3fd-292">Mali</span><span class="sxs-lookup"><span data-stu-id="4b3fd-292">Fiscal</span></span></td>
<td><span data-ttu-id="4b3fd-293">2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-293">2017</span></span></td>
<td><span data-ttu-id="4b3fd-294">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-294">Period 1</span></span></td>
<td><span data-ttu-id="4b3fd-295">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="4b3fd-296">Günlük girişleri (Maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="4b3fd-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4b3fd-297">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4b3fd-298">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4b3fd-299">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-299">Cost element</span></span></th>
<th><span data-ttu-id="4b3fd-300">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="4b3fd-300">Cost behavior</span></span></th>
<th><span data-ttu-id="4b3fd-301">Tutar</span><span class="sxs-lookup"><span data-stu-id="4b3fd-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b3fd-302">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="4b3fd-303">CC099</span><span class="sxs-lookup"><span data-stu-id="4b3fd-303">CC099</span></span></td>
<td><span data-ttu-id="4b3fd-304">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-304">Default cost center</span></span></td>
<td><span data-ttu-id="4b3fd-305">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-305">10001</span></span></td>
<td><span data-ttu-id="4b3fd-306">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-306">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-307">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-307">Fixed cost</span></span></td>
<td><span data-ttu-id="4b3fd-308">1.000,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-309">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="4b3fd-310">CC099</span><span class="sxs-lookup"><span data-stu-id="4b3fd-310">CC099</span></span></td>
<td><span data-ttu-id="4b3fd-311">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-311">Default cost center</span></span></td>
<td><span data-ttu-id="4b3fd-312">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-312">10001</span></span></td>
<td><span data-ttu-id="4b3fd-313">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-313">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-314">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-314">Variable cost</span></span></td>
<td><span data-ttu-id="4b3fd-315">9,000.00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4b3fd-316">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="4b3fd-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b3fd-317">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4b3fd-318">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-318">Cost element</span></span></th>
<th><span data-ttu-id="4b3fd-319">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="4b3fd-319">Cost behavior</span></span></th>
<th><span data-ttu-id="4b3fd-320">Tutar</span><span class="sxs-lookup"><span data-stu-id="4b3fd-320">Amount</span></span></th>
<th><span data-ttu-id="4b3fd-321">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b3fd-322">CC099</span><span class="sxs-lookup"><span data-stu-id="4b3fd-322">CC099</span></span></td>
<td><span data-ttu-id="4b3fd-323">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-323">Default cost center</span></span></td>
<td><span data-ttu-id="4b3fd-324">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-324">10001</span></span></td>
<td><span data-ttu-id="4b3fd-325">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-325">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-326">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-326">Fixed cost</span></span></td>
<td><span data-ttu-id="4b3fd-327">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-327">-1,000.00</span></span></td>
<td><span data-ttu-id="4b3fd-328">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-329">CC001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-329">CC001</span></span></td>
<td><span data-ttu-id="4b3fd-330">İK</span><span class="sxs-lookup"><span data-stu-id="4b3fd-330">HR</span></span></td>
<td><span data-ttu-id="4b3fd-331">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-331">10001</span></span></td>
<td><span data-ttu-id="4b3fd-332">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-332">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-333">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-333">Fixed cost</span></span></td>
<td><span data-ttu-id="4b3fd-334">500.00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-334">500.00</span></span></td>
<td><span data-ttu-id="4b3fd-335">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-336">CC002</span><span class="sxs-lookup"><span data-stu-id="4b3fd-336">CC002</span></span></td>
<td><span data-ttu-id="4b3fd-337">Finans</span><span class="sxs-lookup"><span data-stu-id="4b3fd-337">Finance</span></span></td>
<td><span data-ttu-id="4b3fd-338">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-338">10001</span></span></td>
<td><span data-ttu-id="4b3fd-339">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-339">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-340">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-340">Fixed cost</span></span></td>
<td><span data-ttu-id="4b3fd-341">500.00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-341">500.00</span></span></td>
<td><span data-ttu-id="4b3fd-342">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-343">CC099</span><span class="sxs-lookup"><span data-stu-id="4b3fd-343">CC099</span></span></td>
<td><span data-ttu-id="4b3fd-344">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-344">Default cost center</span></span></td>
<td><span data-ttu-id="4b3fd-345">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-345">10001</span></span></td>
<td><span data-ttu-id="4b3fd-346">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-346">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-347">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-347">Variable cost</span></span></td>
<td><span data-ttu-id="4b3fd-348">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-348">-9,000.00</span></span></td>
<td><span data-ttu-id="4b3fd-349">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-350">CC001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-350">CC001</span></span></td>
<td><span data-ttu-id="4b3fd-351">İK</span><span class="sxs-lookup"><span data-stu-id="4b3fd-351">HR</span></span></td>
<td><span data-ttu-id="4b3fd-352">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-352">10001</span></span></td>
<td><span data-ttu-id="4b3fd-353">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-353">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-354">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-354">Variable cost</span></span></td>
<td><span data-ttu-id="4b3fd-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="4b3fd-355">1,285.71</span></span></td>
<td><span data-ttu-id="4b3fd-356">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-357">CC002</span><span class="sxs-lookup"><span data-stu-id="4b3fd-357">CC002</span></span></td>
<td><span data-ttu-id="4b3fd-358">Finans</span><span class="sxs-lookup"><span data-stu-id="4b3fd-358">Finance</span></span></td>
<td><span data-ttu-id="4b3fd-359">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-359">10001</span></span></td>
<td><span data-ttu-id="4b3fd-360">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-360">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-361">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-361">Variable cost</span></span></td>
<td><span data-ttu-id="4b3fd-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="4b3fd-362">7,714.29</span></span></td>
<td><span data-ttu-id="4b3fd-363">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4b3fd-364">Maliyet dağıtımı ve tahsisat tabanları hakkında ayrıntılı bilgi için, bakınız Maliyet dağıtım ilkesi ve Tahsisat tabanları.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="4b3fd-365">(Bu konunun henüz tamamlanmadığını ancak yakında tamamlanacağını göz önünde bulundurun.)</span><span class="sxs-lookup"><span data-stu-id="4b3fd-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="4b3fd-366">Adım 3: Genel gider oranı hesaplama işlemi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="4b3fd-367">Genel gider oranı, bir veya birden fazla belirli maliyet nesnesine masraf yüklemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="4b3fd-368">Masraf, önceden belirlenmiş maliyet oranına ve tahsisat tabanından hesaplanan büyüklüğe dayanır.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="4b3fd-369">Genel gider oranını tanımlama</span><span class="sxs-lookup"><span data-stu-id="4b3fd-369">Define the overhead rate</span></span>

<span data-ttu-id="4b3fd-370">Maliyet nesnesi CC001 HR, bir dizi dahili projeye katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="4b3fd-371">HR projeleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b3fd-372">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-372">Cost object</span></span></th>
<th><span data-ttu-id="4b3fd-373">Saatler</span><span class="sxs-lookup"><span data-stu-id="4b3fd-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b3fd-374">Proj 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-374">Proj 1</span></span></td>
<td><span data-ttu-id="4b3fd-375">Proje 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-375">Project 1</span></span></td>
<td><span data-ttu-id="4b3fd-376">3</span><span class="sxs-lookup"><span data-stu-id="4b3fd-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-377">Proj 2</span><span class="sxs-lookup"><span data-stu-id="4b3fd-377">Proj 2</span></span></td>
<td><span data-ttu-id="4b3fd-378">Proje 2</span><span class="sxs-lookup"><span data-stu-id="4b3fd-378">Project 2</span></span></td>
<td><span data-ttu-id="4b3fd-379">1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4b3fd-380">Maliyet projeleri dağıtımı için bir önceden belirlenmiş maliyet oranı tanımlandı.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b3fd-381">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-381">Cost object</span></span></th>
<th><span data-ttu-id="4b3fd-382">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-382">Cost element</span></span></th>
<th><span data-ttu-id="4b3fd-383">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="4b3fd-383">Cost behavior</span></span></th>
<th><span data-ttu-id="4b3fd-384">Birimler</span><span class="sxs-lookup"><span data-stu-id="4b3fd-384">Units</span></span></th>
<th><span data-ttu-id="4b3fd-385">Ücret</span><span class="sxs-lookup"><span data-stu-id="4b3fd-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b3fd-386">CC001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-386">CC001</span></span></td>
<td><span data-ttu-id="4b3fd-387">İK</span><span class="sxs-lookup"><span data-stu-id="4b3fd-387">HR</span></span></td>
<td><span data-ttu-id="4b3fd-388">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-388">10001</span></span></td>
<td><span data-ttu-id="4b3fd-389">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-389">Variable cost</span></span></td>
<td><span data-ttu-id="4b3fd-390">1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-390">1</span></span></td>
<td><span data-ttu-id="4b3fd-391">10</span><span class="sxs-lookup"><span data-stu-id="4b3fd-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4b3fd-392">Aşağıdaki tablo, HR projeleri bir tahsisat tabanı olarak uygulandığındaki sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b3fd-393">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-393">Cost object</span></span></th>
<th><span data-ttu-id="4b3fd-394">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="4b3fd-394">Magnitude</span></span></th>
<th><span data-ttu-id="4b3fd-395">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-395">Cost element</span></span></th>
<th><span data-ttu-id="4b3fd-396">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="4b3fd-396">Allocation factor</span></span></th>
<th><span data-ttu-id="4b3fd-397">Tutar</span><span class="sxs-lookup"><span data-stu-id="4b3fd-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b3fd-398">Proj 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-398">Proj 1</span></span></td>
<td><span data-ttu-id="4b3fd-399">Proje 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-399">Project 1</span></span></td>
<td><span data-ttu-id="4b3fd-400">3</span><span class="sxs-lookup"><span data-stu-id="4b3fd-400">3</span></span></td>
<td><span data-ttu-id="4b3fd-401">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-401">10001</span></span></td>
<td><span data-ttu-id="4b3fd-402">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="4b3fd-403">30.00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-404">Proj 2</span><span class="sxs-lookup"><span data-stu-id="4b3fd-404">Proj 2</span></span></td>
<td><span data-ttu-id="4b3fd-405">Proje 2</span><span class="sxs-lookup"><span data-stu-id="4b3fd-405">Project 2</span></span></td>
<td><span data-ttu-id="4b3fd-406">1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-406">1</span></span></td>
<td><span data-ttu-id="4b3fd-407">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-407">10001</span></span></td>
<td><span data-ttu-id="4b3fd-408">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="4b3fd-409">10,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="4b3fd-410">Günlük</span><span class="sxs-lookup"><span data-stu-id="4b3fd-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4b3fd-411">Günlük</span><span class="sxs-lookup"><span data-stu-id="4b3fd-411">Journal</span></span></th>
<th><span data-ttu-id="4b3fd-412">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="4b3fd-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4b3fd-413">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4b3fd-414">Sürüm</span><span class="sxs-lookup"><span data-stu-id="4b3fd-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b3fd-415">00003</span><span class="sxs-lookup"><span data-stu-id="4b3fd-415">00003</span></span></td>
<td><span data-ttu-id="4b3fd-416">Genel gider oranı hesaplaması günlüğü</span><span class="sxs-lookup"><span data-stu-id="4b3fd-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="4b3fd-417">Mali</span><span class="sxs-lookup"><span data-stu-id="4b3fd-417">Fiscal</span></span></td>
<td><span data-ttu-id="4b3fd-418">2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-418">2017</span></span></td>
<td><span data-ttu-id="4b3fd-419">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-419">Period 1</span></span></td>
<td><span data-ttu-id="4b3fd-420">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="4b3fd-421">Günlük girişleri (Genel gider oranı hesaplaması için günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="4b3fd-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4b3fd-422">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4b3fd-423">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-423">Cost object</span></span></th>
<th><span data-ttu-id="4b3fd-424">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="4b3fd-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b3fd-425">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="4b3fd-426">Proj 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-426">Proj 1</span></span></td>
<td><span data-ttu-id="4b3fd-427">Dahili Proj 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="4b3fd-428">3,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-429">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="4b3fd-430">Proj 2</span><span class="sxs-lookup"><span data-stu-id="4b3fd-430">Proj 2</span></span></td>
<td><span data-ttu-id="4b3fd-431">Dahili Proj 2</span><span class="sxs-lookup"><span data-stu-id="4b3fd-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="4b3fd-432">1.00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4b3fd-433">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="4b3fd-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b3fd-434">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4b3fd-435">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-435">Cost element</span></span></th>
<th><span data-ttu-id="4b3fd-436">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="4b3fd-436">Cost behavior</span></span></th>
<th><span data-ttu-id="4b3fd-437">Tutar</span><span class="sxs-lookup"><span data-stu-id="4b3fd-437">Amount</span></span></th>
<th><span data-ttu-id="4b3fd-438">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b3fd-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-439">CC0001</span></span></td>
<td><span data-ttu-id="4b3fd-440">İK</span><span class="sxs-lookup"><span data-stu-id="4b3fd-440">HR</span></span></td>
<td><span data-ttu-id="4b3fd-441">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-441">10001</span></span></td>
<td><span data-ttu-id="4b3fd-442">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-442">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-443">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-443">Variable cost</span></span></td>
<td><span data-ttu-id="4b3fd-444">-30,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-444">-30.00</span></span></td>
<td><span data-ttu-id="4b3fd-445">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-446">Proj 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-446">Proj 1</span></span></td>
<td><span data-ttu-id="4b3fd-447">Dahili Proj 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="4b3fd-448">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-448">10001</span></span></td>
<td><span data-ttu-id="4b3fd-449">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-449">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-450">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-450">Variable cost</span></span></td>
<td><span data-ttu-id="4b3fd-451">30.00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-451">30.00</span></span></td>
<td><span data-ttu-id="4b3fd-452">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-453">CC001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-453">CC001</span></span></td>
<td><span data-ttu-id="4b3fd-454">İK</span><span class="sxs-lookup"><span data-stu-id="4b3fd-454">HR</span></span></td>
<td><span data-ttu-id="4b3fd-455">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-455">10001</span></span></td>
<td><span data-ttu-id="4b3fd-456">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-456">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-457">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-457">Variable cost</span></span></td>
<td><span data-ttu-id="4b3fd-458">-10,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-458">-10.00</span></span></td>
<td><span data-ttu-id="4b3fd-459">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-460">Proj 2</span><span class="sxs-lookup"><span data-stu-id="4b3fd-460">Proj 2</span></span></td>
<td><span data-ttu-id="4b3fd-461">Dahili Proj 2</span><span class="sxs-lookup"><span data-stu-id="4b3fd-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="4b3fd-462">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-462">10001</span></span></td>
<td><span data-ttu-id="4b3fd-463">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-463">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-464">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-464">Variable cost</span></span></td>
<td><span data-ttu-id="4b3fd-465">10,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-465">10.00</span></span></td>
<td><span data-ttu-id="4b3fd-466">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4b3fd-467">Genel gider oranı ilkesi hakkında ayrıntılı bilgi için, Genel gider oranları ilkesi ve Tahsisat tabanlarına bakın.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="4b3fd-468">(Bu konunun henüz tamamlanmadığını ancak yakında tamamlanacağını göz önünde bulundurun.)</span><span class="sxs-lookup"><span data-stu-id="4b3fd-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="4b3fd-469">Adım 4: Maliyet tahsisat hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="4b3fd-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="4b3fd-470">Tahsisat, bir tahsisat tabanı kullanarak bir maliyet nesnesinin diğer maliyet nesnelerine bakiyesini tahsis eder.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="4b3fd-471">Finance and Operations karşılıklı tahsisat yöntemin destekler.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="4b3fd-472">Karşılıklı tahsisat yönteminde, yardımcı maliyet nesnelerinin değiştiği karşılıklı hizmetler tümüyle tanınır.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="4b3fd-473">Sistem, tahsisatların doğru gerçekleştireceği sırayı otomatik olarak belirler.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="4b3fd-474">Bir maliyet nesnesinin bakiyesi tek bir tahsisat tabanı tarafından tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="4b3fd-475">Yeni maliyet nesnesi boyutları arasındaki tahsisatlar ve onların üyeleri desteklenir.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="4b3fd-476">Tahsisatın sırası, maliyet kontrol birimi tarafından kontrol edilir.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-476">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="4b3fd-477">[![Karşılıklı yöntemi](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="4b3fd-477">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="4b3fd-478">Maliyet tahsisatını tanımla</span><span class="sxs-lookup"><span data-stu-id="4b3fd-478">Define the cost allocation</span></span>

<span data-ttu-id="4b3fd-479">Bir maliyetin akışını nasıl izleyeceğinize dair basit bir örnek aşağıda verilmiştir,</span><span class="sxs-lookup"><span data-stu-id="4b3fd-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="4b3fd-480">Maliyet nesnesi CC001 HR, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="4b3fd-481">HR hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b3fd-482">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-482">Cost object</span></span></th>
<th><span data-ttu-id="4b3fd-483">HR hizmetleri</span><span class="sxs-lookup"><span data-stu-id="4b3fd-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b3fd-484">CC002</span><span class="sxs-lookup"><span data-stu-id="4b3fd-484">CC002</span></span></td>
<td><span data-ttu-id="4b3fd-485">Finans</span><span class="sxs-lookup"><span data-stu-id="4b3fd-485">Finance</span></span></td>
<td><span data-ttu-id="4b3fd-486">35</span><span class="sxs-lookup"><span data-stu-id="4b3fd-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-487">CC003</span><span class="sxs-lookup"><span data-stu-id="4b3fd-487">CC003</span></span></td>
<td><span data-ttu-id="4b3fd-488">Montaj</span><span class="sxs-lookup"><span data-stu-id="4b3fd-488">Assembly</span></span></td>
<td><span data-ttu-id="4b3fd-489">55</span><span class="sxs-lookup"><span data-stu-id="4b3fd-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-490">CC004</span><span class="sxs-lookup"><span data-stu-id="4b3fd-490">CC004</span></span></td>
<td><span data-ttu-id="4b3fd-491">Paketleme</span><span class="sxs-lookup"><span data-stu-id="4b3fd-491">Packaging</span></span></td>
<td><span data-ttu-id="4b3fd-492">10</span><span class="sxs-lookup"><span data-stu-id="4b3fd-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4b3fd-493">Maliyet nesnesi CC002 Finans, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="4b3fd-494">Finans hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b3fd-495">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-495">Cost object</span></span></th>
<th><span data-ttu-id="4b3fd-496">Finans hizmetleri</span><span class="sxs-lookup"><span data-stu-id="4b3fd-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b3fd-497">CC003</span><span class="sxs-lookup"><span data-stu-id="4b3fd-497">CC003</span></span></td>
<td><span data-ttu-id="4b3fd-498">Montaj</span><span class="sxs-lookup"><span data-stu-id="4b3fd-498">Assembly</span></span></td>
<td><span data-ttu-id="4b3fd-499">65</span><span class="sxs-lookup"><span data-stu-id="4b3fd-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-500">CC004</span><span class="sxs-lookup"><span data-stu-id="4b3fd-500">CC004</span></span></td>
<td><span data-ttu-id="4b3fd-501">Paketleme</span><span class="sxs-lookup"><span data-stu-id="4b3fd-501">Packaging</span></span></td>
<td><span data-ttu-id="4b3fd-502">35</span><span class="sxs-lookup"><span data-stu-id="4b3fd-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4b3fd-503">Maliyet nesnesi CC003 Derleme, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="4b3fd-504">Derleme hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b3fd-505">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-505">Cost object</span></span></th>
<th><span data-ttu-id="4b3fd-506">Derleme Hizmetleri (saat)</span><span class="sxs-lookup"><span data-stu-id="4b3fd-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b3fd-507">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-507">Prod 1</span></span></td>
<td><span data-ttu-id="4b3fd-508">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-508">Product 1</span></span></td>
<td><span data-ttu-id="4b3fd-509">60</span><span class="sxs-lookup"><span data-stu-id="4b3fd-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-510">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4b3fd-510">Prod 2</span></span></td>
<td><span data-ttu-id="4b3fd-511">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="4b3fd-511">Product 2</span></span></td>
<td><span data-ttu-id="4b3fd-512">20</span><span class="sxs-lookup"><span data-stu-id="4b3fd-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4b3fd-513">Maliyet nesnesi CC004 Ambalajlama, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="4b3fd-514">Ambalajlama hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b3fd-515">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-515">Cost object</span></span></th>
<th><span data-ttu-id="4b3fd-516">Ambalajlama hizmetleri (saat)</span><span class="sxs-lookup"><span data-stu-id="4b3fd-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b3fd-517">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-517">Prod 1</span></span></td>
<td><span data-ttu-id="4b3fd-518">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-518">Product 1</span></span></td>
<td><span data-ttu-id="4b3fd-519">80</span><span class="sxs-lookup"><span data-stu-id="4b3fd-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-520">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4b3fd-520">Prod 2</span></span></td>
<td><span data-ttu-id="4b3fd-521">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="4b3fd-521">Product 2</span></span></td>
<td><span data-ttu-id="4b3fd-522">15</span><span class="sxs-lookup"><span data-stu-id="4b3fd-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4b3fd-523">**Not:** Finance and Operations'ta, bir ürünün tükettiği üretim saatleri gibi istatistiki ölçümler doğrudan kaynak verisinden alınabilir.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="4b3fd-524">İstatistiki ölçüm sağlayıcılar hakkında daha ayrıntılı bilgi için İstatistiki ölçü sağlayıcı şablonuna göz atın.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="4b3fd-525">(Bu konun henüz tamamlanmamış olduğunu ancak yakında tamamlanacağını unutmayın) Aşağıdaki tablo, HR hizmetleri toplam maliyet (sabit ve değişken maliyet) için bir tahsisat tabanı olarak uygulandığında oluşacak sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b3fd-526">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-526">Cost object</span></span></th>
<th><span data-ttu-id="4b3fd-527">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="4b3fd-527">Magnitude</span></span></th>
<th><span data-ttu-id="4b3fd-528">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="4b3fd-528">Allocation factor</span></span></th>
<th><span data-ttu-id="4b3fd-529">Tutar</span><span class="sxs-lookup"><span data-stu-id="4b3fd-529">Amount</span></span></th>
<th><span data-ttu-id="4b3fd-530">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="4b3fd-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b3fd-531">CC002</span><span class="sxs-lookup"><span data-stu-id="4b3fd-531">CC002</span></span></td>
<td><span data-ttu-id="4b3fd-532">Finans</span><span class="sxs-lookup"><span data-stu-id="4b3fd-532">Finance</span></span></td>
<td><span data-ttu-id="4b3fd-533">35</span><span class="sxs-lookup"><span data-stu-id="4b3fd-533">35</span></span></td>
<td><span data-ttu-id="4b3fd-534">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="4b3fd-535">175.00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-535">175.00</span></span></td>
<td><span data-ttu-id="4b3fd-536">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-537">CC003</span><span class="sxs-lookup"><span data-stu-id="4b3fd-537">CC003</span></span></td>
<td><span data-ttu-id="4b3fd-538">Montaj</span><span class="sxs-lookup"><span data-stu-id="4b3fd-538">Assembly</span></span></td>
<td><span data-ttu-id="4b3fd-539">55</span><span class="sxs-lookup"><span data-stu-id="4b3fd-539">55</span></span></td>
<td><span data-ttu-id="4b3fd-540">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="4b3fd-541">275.00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-541">275.00</span></span></td>
<td><span data-ttu-id="4b3fd-542">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-543">CC004</span><span class="sxs-lookup"><span data-stu-id="4b3fd-543">CC004</span></span></td>
<td><span data-ttu-id="4b3fd-544">Paketleme</span><span class="sxs-lookup"><span data-stu-id="4b3fd-544">Packaging</span></span></td>
<td><span data-ttu-id="4b3fd-545">10</span><span class="sxs-lookup"><span data-stu-id="4b3fd-545">10</span></span></td>
<td><span data-ttu-id="4b3fd-546">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="4b3fd-547">50,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-547">50.00</span></span></td>
<td><span data-ttu-id="4b3fd-548">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-549">CC002</span><span class="sxs-lookup"><span data-stu-id="4b3fd-549">CC002</span></span></td>
<td><span data-ttu-id="4b3fd-550">Finans</span><span class="sxs-lookup"><span data-stu-id="4b3fd-550">Finance</span></span></td>
<td><span data-ttu-id="4b3fd-551">35</span><span class="sxs-lookup"><span data-stu-id="4b3fd-551">35</span></span></td>
<td><span data-ttu-id="4b3fd-552">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="4b3fd-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="4b3fd-553">436.00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-553">436.00</span></span></td>
<td><span data-ttu-id="4b3fd-554">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-555">CC003</span><span class="sxs-lookup"><span data-stu-id="4b3fd-555">CC003</span></span></td>
<td><span data-ttu-id="4b3fd-556">Montaj</span><span class="sxs-lookup"><span data-stu-id="4b3fd-556">Assembly</span></span></td>
<td><span data-ttu-id="4b3fd-557">55</span><span class="sxs-lookup"><span data-stu-id="4b3fd-557">55</span></span></td>
<td><span data-ttu-id="4b3fd-558">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="4b3fd-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="4b3fd-559">685.14</span><span class="sxs-lookup"><span data-stu-id="4b3fd-559">685.14</span></span></td>
<td><span data-ttu-id="4b3fd-560">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-561">CC004</span><span class="sxs-lookup"><span data-stu-id="4b3fd-561">CC004</span></span></td>
<td><span data-ttu-id="4b3fd-562">Paketleme</span><span class="sxs-lookup"><span data-stu-id="4b3fd-562">Packaging</span></span></td>
<td><span data-ttu-id="4b3fd-563">10</span><span class="sxs-lookup"><span data-stu-id="4b3fd-563">10</span></span></td>
<td><span data-ttu-id="4b3fd-564">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="4b3fd-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="4b3fd-565">124.57</span><span class="sxs-lookup"><span data-stu-id="4b3fd-565">124.57</span></span></td>
<td><span data-ttu-id="4b3fd-566">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4b3fd-567">Aşağıdaki tablo, Finans hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b3fd-568">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-568">Cost object</span></span></th>
<th><span data-ttu-id="4b3fd-569">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="4b3fd-569">Magnitude</span></span></th>
<th><span data-ttu-id="4b3fd-570">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="4b3fd-570">Allocation factor</span></span></th>
<th><span data-ttu-id="4b3fd-571">Tutar</span><span class="sxs-lookup"><span data-stu-id="4b3fd-571">Amount</span></span></th>
<th><span data-ttu-id="4b3fd-572">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="4b3fd-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b3fd-573">CC003</span><span class="sxs-lookup"><span data-stu-id="4b3fd-573">CC003</span></span></td>
<td><span data-ttu-id="4b3fd-574">Montaj</span><span class="sxs-lookup"><span data-stu-id="4b3fd-574">Assembly</span></span></td>
<td><span data-ttu-id="4b3fd-575">65</span><span class="sxs-lookup"><span data-stu-id="4b3fd-575">65</span></span></td>
<td><span data-ttu-id="4b3fd-576">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="4b3fd-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="4b3fd-577">438.75</span><span class="sxs-lookup"><span data-stu-id="4b3fd-577">438.75</span></span></td>
<td><span data-ttu-id="4b3fd-578">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-579">CC004</span><span class="sxs-lookup"><span data-stu-id="4b3fd-579">CC004</span></span></td>
<td><span data-ttu-id="4b3fd-580">Paketleme</span><span class="sxs-lookup"><span data-stu-id="4b3fd-580">Packaging</span></span></td>
<td><span data-ttu-id="4b3fd-581">35</span><span class="sxs-lookup"><span data-stu-id="4b3fd-581">35</span></span></td>
<td><span data-ttu-id="4b3fd-582">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="4b3fd-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="4b3fd-583">236.25</span><span class="sxs-lookup"><span data-stu-id="4b3fd-583">236.25</span></span></td>
<td><span data-ttu-id="4b3fd-584">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-585">CC003</span><span class="sxs-lookup"><span data-stu-id="4b3fd-585">CC003</span></span></td>
<td><span data-ttu-id="4b3fd-586">Montaj</span><span class="sxs-lookup"><span data-stu-id="4b3fd-586">Assembly</span></span></td>
<td><span data-ttu-id="4b3fd-587">65</span><span class="sxs-lookup"><span data-stu-id="4b3fd-587">65</span></span></td>
<td><span data-ttu-id="4b3fd-588">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="4b3fd-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="4b3fd-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="4b3fd-589">5,297.69</span></span></td>
<td><span data-ttu-id="4b3fd-590">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-591">CC004</span><span class="sxs-lookup"><span data-stu-id="4b3fd-591">CC004</span></span></td>
<td><span data-ttu-id="4b3fd-592">Paketleme</span><span class="sxs-lookup"><span data-stu-id="4b3fd-592">Packaging</span></span></td>
<td><span data-ttu-id="4b3fd-593">35</span><span class="sxs-lookup"><span data-stu-id="4b3fd-593">35</span></span></td>
<td><span data-ttu-id="4b3fd-594">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="4b3fd-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="4b3fd-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="4b3fd-595">2,852.60</span></span></td>
<td><span data-ttu-id="4b3fd-596">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4b3fd-597">Aşağıdaki tablo, Derleme hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b3fd-598">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-598">Cost object</span></span></th>
<th><span data-ttu-id="4b3fd-599">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="4b3fd-599">Magnitude</span></span></th>
<th><span data-ttu-id="4b3fd-600">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="4b3fd-600">Allocation factor</span></span></th>
<th><span data-ttu-id="4b3fd-601">Tutar</span><span class="sxs-lookup"><span data-stu-id="4b3fd-601">Amount</span></span></th>
<th><span data-ttu-id="4b3fd-602">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="4b3fd-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b3fd-603">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-603">Prod 1</span></span></td>
<td><span data-ttu-id="4b3fd-604">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-604">Product 1</span></span></td>
<td><span data-ttu-id="4b3fd-605">60</span><span class="sxs-lookup"><span data-stu-id="4b3fd-605">60</span></span></td>
<td><span data-ttu-id="4b3fd-606">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="4b3fd-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="4b3fd-607">535.31</span><span class="sxs-lookup"><span data-stu-id="4b3fd-607">535.31</span></span></td>
<td><span data-ttu-id="4b3fd-608">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-609">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4b3fd-609">Prod 2</span></span></td>
<td><span data-ttu-id="4b3fd-610">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="4b3fd-610">Product 2</span></span></td>
<td><span data-ttu-id="4b3fd-611">20</span><span class="sxs-lookup"><span data-stu-id="4b3fd-611">20</span></span></td>
<td><span data-ttu-id="4b3fd-612">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="4b3fd-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="4b3fd-613">178.44</span><span class="sxs-lookup"><span data-stu-id="4b3fd-613">178.44</span></span></td>
<td><span data-ttu-id="4b3fd-614">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-615">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-615">Prod 1</span></span></td>
<td><span data-ttu-id="4b3fd-616">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-616">Product 1</span></span></td>
<td><span data-ttu-id="4b3fd-617">60</span><span class="sxs-lookup"><span data-stu-id="4b3fd-617">60</span></span></td>
<td><span data-ttu-id="4b3fd-618">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="4b3fd-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="4b3fd-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="4b3fd-619">4,487.12</span></span></td>
<td><span data-ttu-id="4b3fd-620">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-621">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4b3fd-621">Prod 2</span></span></td>
<td><span data-ttu-id="4b3fd-622">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="4b3fd-622">Product 2</span></span></td>
<td><span data-ttu-id="4b3fd-623">20</span><span class="sxs-lookup"><span data-stu-id="4b3fd-623">20</span></span></td>
<td><span data-ttu-id="4b3fd-624">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="4b3fd-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="4b3fd-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="4b3fd-625">1,495.71</span></span></td>
<td><span data-ttu-id="4b3fd-626">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4b3fd-627">Aşağıdaki tablo, Paketleme hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b3fd-628">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-628">Cost object</span></span></th>
<th><span data-ttu-id="4b3fd-629">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="4b3fd-629">Magnitude</span></span></th>
<th><span data-ttu-id="4b3fd-630">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="4b3fd-630">Allocation factor</span></span></th>
<th><span data-ttu-id="4b3fd-631">Tutar</span><span class="sxs-lookup"><span data-stu-id="4b3fd-631">Amount</span></span></th>
<th><span data-ttu-id="4b3fd-632">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="4b3fd-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b3fd-633">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-633">Prod 1</span></span></td>
<td><span data-ttu-id="4b3fd-634">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-634">Product 1</span></span></td>
<td><span data-ttu-id="4b3fd-635">80</span><span class="sxs-lookup"><span data-stu-id="4b3fd-635">80</span></span></td>
<td><span data-ttu-id="4b3fd-636">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="4b3fd-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="4b3fd-637">241.05</span><span class="sxs-lookup"><span data-stu-id="4b3fd-637">241.05</span></span></td>
<td><span data-ttu-id="4b3fd-638">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-639">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4b3fd-639">Prod 2</span></span></td>
<td><span data-ttu-id="4b3fd-640">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="4b3fd-640">Product 2</span></span></td>
<td><span data-ttu-id="4b3fd-641">15</span><span class="sxs-lookup"><span data-stu-id="4b3fd-641">15</span></span></td>
<td><span data-ttu-id="4b3fd-642">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="4b3fd-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="4b3fd-643">45.20</span><span class="sxs-lookup"><span data-stu-id="4b3fd-643">45.20</span></span></td>
<td><span data-ttu-id="4b3fd-644">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-645">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-645">Prod 1</span></span></td>
<td><span data-ttu-id="4b3fd-646">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-646">Product 1</span></span></td>
<td><span data-ttu-id="4b3fd-647">80</span><span class="sxs-lookup"><span data-stu-id="4b3fd-647">80</span></span></td>
<td><span data-ttu-id="4b3fd-648">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="4b3fd-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="4b3fd-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="4b3fd-649">2,507.09</span></span></td>
<td><span data-ttu-id="4b3fd-650">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-651">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4b3fd-651">Prod 2</span></span></td>
<td><span data-ttu-id="4b3fd-652">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="4b3fd-652">Product 2</span></span></td>
<td><span data-ttu-id="4b3fd-653">15</span><span class="sxs-lookup"><span data-stu-id="4b3fd-653">15</span></span></td>
<td><span data-ttu-id="4b3fd-654">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="4b3fd-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="4b3fd-655">470.08</span><span class="sxs-lookup"><span data-stu-id="4b3fd-655">470.08</span></span></td>
<td><span data-ttu-id="4b3fd-656">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="4b3fd-657">Günlük girişleri (maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="4b3fd-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4b3fd-658">Günlük</span><span class="sxs-lookup"><span data-stu-id="4b3fd-658">Journal</span></span></th>
<th><span data-ttu-id="4b3fd-659">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="4b3fd-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4b3fd-660">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4b3fd-661">Sürüm</span><span class="sxs-lookup"><span data-stu-id="4b3fd-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b3fd-662">00004</span><span class="sxs-lookup"><span data-stu-id="4b3fd-662">00004</span></span></td>
<td><span data-ttu-id="4b3fd-663">Maliyet tahsisatı günlüğü</span><span class="sxs-lookup"><span data-stu-id="4b3fd-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="4b3fd-664">Mali</span><span class="sxs-lookup"><span data-stu-id="4b3fd-664">Fiscal</span></span></td>
<td><span data-ttu-id="4b3fd-665">2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-665">2017</span></span></td>
<td><span data-ttu-id="4b3fd-666">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-666">Period 1</span></span></td>
<td><span data-ttu-id="4b3fd-667">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="4b3fd-668">Günlük satırları</span><span class="sxs-lookup"><span data-stu-id="4b3fd-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4b3fd-669">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4b3fd-670">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4b3fd-671">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-671">Cost element</span></span></th>
<th><span data-ttu-id="4b3fd-672">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="4b3fd-672">Cost behavior</span></span></th>
<th><span data-ttu-id="4b3fd-673">Tutar</span><span class="sxs-lookup"><span data-stu-id="4b3fd-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b3fd-674">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="4b3fd-675">CC001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-675">CC001</span></span></td>
<td><span data-ttu-id="4b3fd-676">İK</span><span class="sxs-lookup"><span data-stu-id="4b3fd-676">HR</span></span></td>
<td><span data-ttu-id="4b3fd-677">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-677">10001</span></span></td>
<td><span data-ttu-id="4b3fd-678">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-678">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-679">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-679">Fixed cost</span></span></td>
<td><span data-ttu-id="4b3fd-680">500.00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-681">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="4b3fd-682">CC001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-682">CC001</span></span></td>
<td><span data-ttu-id="4b3fd-683">İK</span><span class="sxs-lookup"><span data-stu-id="4b3fd-683">HR</span></span></td>
<td><span data-ttu-id="4b3fd-684">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-684">10001</span></span></td>
<td><span data-ttu-id="4b3fd-685">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-685">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-686">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-686">Variable cost</span></span></td>
<td><span data-ttu-id="4b3fd-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="4b3fd-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-688">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="4b3fd-689">CC002</span><span class="sxs-lookup"><span data-stu-id="4b3fd-689">CC002</span></span></td>
<td><span data-ttu-id="4b3fd-690">Finans</span><span class="sxs-lookup"><span data-stu-id="4b3fd-690">Finance</span></span></td>
<td><span data-ttu-id="4b3fd-691">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-691">10001</span></span></td>
<td><span data-ttu-id="4b3fd-692">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-692">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-693">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-693">Fixed cost</span></span></td>
<td><span data-ttu-id="4b3fd-694">675.00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-695">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="4b3fd-696">CC002</span><span class="sxs-lookup"><span data-stu-id="4b3fd-696">CC002</span></span></td>
<td><span data-ttu-id="4b3fd-697">Finans</span><span class="sxs-lookup"><span data-stu-id="4b3fd-697">Finance</span></span></td>
<td><span data-ttu-id="4b3fd-698">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-698">10001</span></span></td>
<td><span data-ttu-id="4b3fd-699">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-699">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-700">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-700">Variable cost</span></span></td>
<td><span data-ttu-id="4b3fd-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="4b3fd-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-702">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="4b3fd-703">CC003</span><span class="sxs-lookup"><span data-stu-id="4b3fd-703">CC003</span></span></td>
<td><span data-ttu-id="4b3fd-704">Montaj</span><span class="sxs-lookup"><span data-stu-id="4b3fd-704">Assembly</span></span></td>
<td><span data-ttu-id="4b3fd-705">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-705">10001</span></span></td>
<td><span data-ttu-id="4b3fd-706">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-706">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-707">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-707">Fixed cost</span></span></td>
<td><span data-ttu-id="4b3fd-708">713.75</span><span class="sxs-lookup"><span data-stu-id="4b3fd-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-709">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="4b3fd-710">CC003</span><span class="sxs-lookup"><span data-stu-id="4b3fd-710">CC003</span></span></td>
<td><span data-ttu-id="4b3fd-711">Montaj</span><span class="sxs-lookup"><span data-stu-id="4b3fd-711">Assembly</span></span></td>
<td><span data-ttu-id="4b3fd-712">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-712">10001</span></span></td>
<td><span data-ttu-id="4b3fd-713">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-713">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-714">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-714">Variable cost</span></span></td>
<td><span data-ttu-id="4b3fd-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="4b3fd-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-716">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="4b3fd-717">CC003</span><span class="sxs-lookup"><span data-stu-id="4b3fd-717">CC003</span></span></td>
<td><span data-ttu-id="4b3fd-718">Paketleme</span><span class="sxs-lookup"><span data-stu-id="4b3fd-718">Packaging</span></span></td>
<td><span data-ttu-id="4b3fd-719">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-719">10001</span></span></td>
<td><span data-ttu-id="4b3fd-720">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-720">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-721">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-721">Fixed cost</span></span></td>
<td><span data-ttu-id="4b3fd-722">286.25</span><span class="sxs-lookup"><span data-stu-id="4b3fd-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-723">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="4b3fd-724">CC003</span><span class="sxs-lookup"><span data-stu-id="4b3fd-724">CC003</span></span></td>
<td><span data-ttu-id="4b3fd-725">Paketleme</span><span class="sxs-lookup"><span data-stu-id="4b3fd-725">Packaging</span></span></td>
<td><span data-ttu-id="4b3fd-726">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-726">10001</span></span></td>
<td><span data-ttu-id="4b3fd-727">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-727">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-728">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-728">Variable cost</span></span></td>
<td><span data-ttu-id="4b3fd-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="4b3fd-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-730">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="4b3fd-731">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-731">Prod 1</span></span></td>
<td><span data-ttu-id="4b3fd-732">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-732">Product 1</span></span></td>
<td><span data-ttu-id="4b3fd-733">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-733">10001</span></span></td>
<td><span data-ttu-id="4b3fd-734">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-734">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-735">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-735">Fixed cost</span></span></td>
<td><span data-ttu-id="4b3fd-736">776.36</span><span class="sxs-lookup"><span data-stu-id="4b3fd-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-737">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="4b3fd-738">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-738">Prod 1</span></span></td>
<td><span data-ttu-id="4b3fd-739">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-739">Product 1</span></span></td>
<td><span data-ttu-id="4b3fd-740">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-740">10001</span></span></td>
<td><span data-ttu-id="4b3fd-741">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-741">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-742">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-742">Variable cost</span></span></td>
<td><span data-ttu-id="4b3fd-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="4b3fd-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-744">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="4b3fd-745">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4b3fd-745">Prod 2</span></span></td>
<td><span data-ttu-id="4b3fd-746">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-746">Product 1</span></span></td>
<td><span data-ttu-id="4b3fd-747">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-747">10001</span></span></td>
<td><span data-ttu-id="4b3fd-748">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-748">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-749">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-749">Fixed cost</span></span></td>
<td><span data-ttu-id="4b3fd-750">223.64</span><span class="sxs-lookup"><span data-stu-id="4b3fd-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-751">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="4b3fd-752">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4b3fd-752">Prod 2</span></span></td>
<td><span data-ttu-id="4b3fd-753">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-753">Product 1</span></span></td>
<td><span data-ttu-id="4b3fd-754">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-754">10001</span></span></td>
<td><span data-ttu-id="4b3fd-755">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-755">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-756">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-756">Variable cost</span></span></td>
<td><span data-ttu-id="4b3fd-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="4b3fd-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4b3fd-758">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="4b3fd-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4b3fd-759">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4b3fd-760">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-760">Cost element</span></span></th>
<th><span data-ttu-id="4b3fd-761">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="4b3fd-761">Cost behavior</span></span></th>
<th><span data-ttu-id="4b3fd-762">Tutar</span><span class="sxs-lookup"><span data-stu-id="4b3fd-762">Amount</span></span></th>
<th><span data-ttu-id="4b3fd-763">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4b3fd-764">CC001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-764">CC001</span></span></td>
<td><span data-ttu-id="4b3fd-765">İK</span><span class="sxs-lookup"><span data-stu-id="4b3fd-765">HR</span></span></td>
<td><span data-ttu-id="4b3fd-766">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-766">10001</span></span></td>
<td><span data-ttu-id="4b3fd-767">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-767">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-768">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-768">Fixed cost</span></span></td>
<td><span data-ttu-id="4b3fd-769">-500.00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-769">-500.00</span></span></td>
<td><span data-ttu-id="4b3fd-770">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-771">CC002</span><span class="sxs-lookup"><span data-stu-id="4b3fd-771">CC002</span></span></td>
<td><span data-ttu-id="4b3fd-772">Finans</span><span class="sxs-lookup"><span data-stu-id="4b3fd-772">Finance</span></span></td>
<td><span data-ttu-id="4b3fd-773">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-773">10001</span></span></td>
<td><span data-ttu-id="4b3fd-774">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-774">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-775">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-775">Fixed cost</span></span></td>
<td><span data-ttu-id="4b3fd-776">175.00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-776">175.00</span></span></td>
<td><span data-ttu-id="4b3fd-777">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-778">CC003</span><span class="sxs-lookup"><span data-stu-id="4b3fd-778">CC003</span></span></td>
<td><span data-ttu-id="4b3fd-779">Montaj</span><span class="sxs-lookup"><span data-stu-id="4b3fd-779">Assembly</span></span></td>
<td><span data-ttu-id="4b3fd-780">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-780">10001</span></span></td>
<td><span data-ttu-id="4b3fd-781">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-781">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-782">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-782">Fixed cost</span></span></td>
<td><span data-ttu-id="4b3fd-783">275.00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-783">275.00</span></span></td>
<td><span data-ttu-id="4b3fd-784">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-785">CC004</span><span class="sxs-lookup"><span data-stu-id="4b3fd-785">CC004</span></span></td>
<td><span data-ttu-id="4b3fd-786">Paketleme</span><span class="sxs-lookup"><span data-stu-id="4b3fd-786">Packaging</span></span></td>
<td><span data-ttu-id="4b3fd-787">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-787">10001</span></span></td>
<td><span data-ttu-id="4b3fd-788">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-788">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-789">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-789">Fixed cost</span></span></td>
<td><span data-ttu-id="4b3fd-790">50,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-790">50,00</span></span></td>
<td><span data-ttu-id="4b3fd-791">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-792">CC001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-792">CC001</span></span></td>
<td><span data-ttu-id="4b3fd-793">İK</span><span class="sxs-lookup"><span data-stu-id="4b3fd-793">HR</span></span></td>
<td><span data-ttu-id="4b3fd-794">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-794">10001</span></span></td>
<td><span data-ttu-id="4b3fd-795">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-795">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-796">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-796">Variable cost</span></span></td>
<td><span data-ttu-id="4b3fd-797">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="4b3fd-797">-1,245.71</span></span></td>
<td><span data-ttu-id="4b3fd-798">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-799">CC002</span><span class="sxs-lookup"><span data-stu-id="4b3fd-799">CC002</span></span></td>
<td><span data-ttu-id="4b3fd-800">Finans</span><span class="sxs-lookup"><span data-stu-id="4b3fd-800">Finance</span></span></td>
<td><span data-ttu-id="4b3fd-801">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-801">10001</span></span></td>
<td><span data-ttu-id="4b3fd-802">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-802">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-803">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-803">Variable cost</span></span></td>
<td><span data-ttu-id="4b3fd-804">436.00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-804">436.00</span></span></td>
<td><span data-ttu-id="4b3fd-805">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-806">CC003</span><span class="sxs-lookup"><span data-stu-id="4b3fd-806">CC003</span></span></td>
<td><span data-ttu-id="4b3fd-807">Montaj</span><span class="sxs-lookup"><span data-stu-id="4b3fd-807">Assembly</span></span></td>
<td><span data-ttu-id="4b3fd-808">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-808">10001</span></span></td>
<td><span data-ttu-id="4b3fd-809">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-809">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-810">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-810">Variable cost</span></span></td>
<td><span data-ttu-id="4b3fd-811">685.14</span><span class="sxs-lookup"><span data-stu-id="4b3fd-811">685.14</span></span></td>
<td><span data-ttu-id="4b3fd-812">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-813">CC004</span><span class="sxs-lookup"><span data-stu-id="4b3fd-813">CC004</span></span></td>
<td><span data-ttu-id="4b3fd-814">Paketleme</span><span class="sxs-lookup"><span data-stu-id="4b3fd-814">Packaging</span></span></td>
<td><span data-ttu-id="4b3fd-815">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-815">10001</span></span></td>
<td><span data-ttu-id="4b3fd-816">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-816">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-817">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-817">Variable cost</span></span></td>
<td><span data-ttu-id="4b3fd-818">124.57</span><span class="sxs-lookup"><span data-stu-id="4b3fd-818">124.57</span></span></td>
<td><span data-ttu-id="4b3fd-819">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-820">CC002</span><span class="sxs-lookup"><span data-stu-id="4b3fd-820">CC002</span></span></td>
<td><span data-ttu-id="4b3fd-821">Finans</span><span class="sxs-lookup"><span data-stu-id="4b3fd-821">Finance</span></span></td>
<td><span data-ttu-id="4b3fd-822">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-822">10001</span></span></td>
<td><span data-ttu-id="4b3fd-823">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-823">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-824">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-824">Fixed cost</span></span></td>
<td><span data-ttu-id="4b3fd-825">-675,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-825">-675.00</span></span></td>
<td><span data-ttu-id="4b3fd-826">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-827">CC003</span><span class="sxs-lookup"><span data-stu-id="4b3fd-827">CC003</span></span></td>
<td><span data-ttu-id="4b3fd-828">Montaj</span><span class="sxs-lookup"><span data-stu-id="4b3fd-828">Assembly</span></span></td>
<td><span data-ttu-id="4b3fd-829">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-829">10001</span></span></td>
<td><span data-ttu-id="4b3fd-830">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-830">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-831">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-831">Fixed cost</span></span></td>
<td><span data-ttu-id="4b3fd-832">438.75</span><span class="sxs-lookup"><span data-stu-id="4b3fd-832">438.75</span></span></td>
<td><span data-ttu-id="4b3fd-833">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-834">CC004</span><span class="sxs-lookup"><span data-stu-id="4b3fd-834">CC004</span></span></td>
<td><span data-ttu-id="4b3fd-835">Paketleme</span><span class="sxs-lookup"><span data-stu-id="4b3fd-835">Packaging</span></span></td>
<td><span data-ttu-id="4b3fd-836">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-836">10001</span></span></td>
<td><span data-ttu-id="4b3fd-837">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-837">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-838">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-838">Fixed cost</span></span></td>
<td><span data-ttu-id="4b3fd-839">236.25</span><span class="sxs-lookup"><span data-stu-id="4b3fd-839">236.25</span></span></td>
<td><span data-ttu-id="4b3fd-840">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-841">CC002</span><span class="sxs-lookup"><span data-stu-id="4b3fd-841">CC002</span></span></td>
<td><span data-ttu-id="4b3fd-842">Finans</span><span class="sxs-lookup"><span data-stu-id="4b3fd-842">Finance</span></span></td>
<td><span data-ttu-id="4b3fd-843">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-843">10001</span></span></td>
<td><span data-ttu-id="4b3fd-844">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-844">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-845">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-845">Variable cost</span></span></td>
<td><span data-ttu-id="4b3fd-846">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="4b3fd-846">-8,150.29</span></span></td>
<td><span data-ttu-id="4b3fd-847">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-848">CC003</span><span class="sxs-lookup"><span data-stu-id="4b3fd-848">CC003</span></span></td>
<td><span data-ttu-id="4b3fd-849">Montaj</span><span class="sxs-lookup"><span data-stu-id="4b3fd-849">Assembly</span></span></td>
<td><span data-ttu-id="4b3fd-850">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-850">10001</span></span></td>
<td><span data-ttu-id="4b3fd-851">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-851">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-852">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-852">Variable cost</span></span></td>
<td><span data-ttu-id="4b3fd-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="4b3fd-853">5,297.69</span></span></td>
<td><span data-ttu-id="4b3fd-854">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-855">CC004</span><span class="sxs-lookup"><span data-stu-id="4b3fd-855">CC004</span></span></td>
<td><span data-ttu-id="4b3fd-856">Paketleme</span><span class="sxs-lookup"><span data-stu-id="4b3fd-856">Packaging</span></span></td>
<td><span data-ttu-id="4b3fd-857">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-857">10001</span></span></td>
<td><span data-ttu-id="4b3fd-858">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-858">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-859">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-859">Variable cost</span></span></td>
<td><span data-ttu-id="4b3fd-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="4b3fd-860">2,852.60</span></span></td>
<td><span data-ttu-id="4b3fd-861">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-862">CC003</span><span class="sxs-lookup"><span data-stu-id="4b3fd-862">CC003</span></span></td>
<td><span data-ttu-id="4b3fd-863">Montaj</span><span class="sxs-lookup"><span data-stu-id="4b3fd-863">Assembly</span></span></td>
<td><span data-ttu-id="4b3fd-864">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-864">10001</span></span></td>
<td><span data-ttu-id="4b3fd-865">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-865">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-866">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-866">Fixed cost</span></span></td>
<td><span data-ttu-id="4b3fd-867">-713.75</span><span class="sxs-lookup"><span data-stu-id="4b3fd-867">-713.75</span></span></td>
<td><span data-ttu-id="4b3fd-868">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-869">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-869">Prod 1</span></span></td>
<td><span data-ttu-id="4b3fd-870">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-870">Product 1</span></span></td>
<td><span data-ttu-id="4b3fd-871">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-871">10001</span></span></td>
<td><span data-ttu-id="4b3fd-872">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-872">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-873">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-873">Fixed cost</span></span></td>
<td><span data-ttu-id="4b3fd-874">535.31</span><span class="sxs-lookup"><span data-stu-id="4b3fd-874">535.31</span></span></td>
<td><span data-ttu-id="4b3fd-875">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-876">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4b3fd-876">Prod 2</span></span></td>
<td><span data-ttu-id="4b3fd-877">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="4b3fd-877">Product 2</span></span></td>
<td><span data-ttu-id="4b3fd-878">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-878">10001</span></span></td>
<td><span data-ttu-id="4b3fd-879">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-879">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-880">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-880">Fixed cost</span></span></td>
<td><span data-ttu-id="4b3fd-881">178.44</span><span class="sxs-lookup"><span data-stu-id="4b3fd-881">178.44</span></span></td>
<td><span data-ttu-id="4b3fd-882">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-883">CC003</span><span class="sxs-lookup"><span data-stu-id="4b3fd-883">CC003</span></span></td>
<td><span data-ttu-id="4b3fd-884">Montaj</span><span class="sxs-lookup"><span data-stu-id="4b3fd-884">Assembly</span></span></td>
<td><span data-ttu-id="4b3fd-885">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-885">10001</span></span></td>
<td><span data-ttu-id="4b3fd-886">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-886">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-887">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-887">Variable cost</span></span></td>
<td><span data-ttu-id="4b3fd-888">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="4b3fd-888">-5,982.83</span></span></td>
<td><span data-ttu-id="4b3fd-889">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-890">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-890">Prod 1</span></span></td>
<td><span data-ttu-id="4b3fd-891">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-891">Product 1</span></span></td>
<td><span data-ttu-id="4b3fd-892">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-892">10001</span></span></td>
<td><span data-ttu-id="4b3fd-893">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-893">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-894">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-894">Variable cost</span></span></td>
<td><span data-ttu-id="4b3fd-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="4b3fd-895">4,487.12</span></span></td>
<td><span data-ttu-id="4b3fd-896">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-897">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4b3fd-897">Prod 2</span></span></td>
<td><span data-ttu-id="4b3fd-898">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="4b3fd-898">Product 2</span></span></td>
<td><span data-ttu-id="4b3fd-899">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-899">10001</span></span></td>
<td><span data-ttu-id="4b3fd-900">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-900">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-901">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-901">Variable cost</span></span></td>
<td><span data-ttu-id="4b3fd-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="4b3fd-902">1,495.71</span></span></td>
<td><span data-ttu-id="4b3fd-903">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-904">CC003</span><span class="sxs-lookup"><span data-stu-id="4b3fd-904">CC003</span></span></td>
<td><span data-ttu-id="4b3fd-905">Montaj</span><span class="sxs-lookup"><span data-stu-id="4b3fd-905">Assembly</span></span></td>
<td><span data-ttu-id="4b3fd-906">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-906">10001</span></span></td>
<td><span data-ttu-id="4b3fd-907">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-907">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-908">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-908">Fixed cost</span></span></td>
<td><span data-ttu-id="4b3fd-909">-286,25</span><span class="sxs-lookup"><span data-stu-id="4b3fd-909">-286.25</span></span></td>
<td><span data-ttu-id="4b3fd-910">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-911">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-911">Prod 1</span></span></td>
<td><span data-ttu-id="4b3fd-912">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-912">Product 1</span></span></td>
<td><span data-ttu-id="4b3fd-913">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-913">10001</span></span></td>
<td><span data-ttu-id="4b3fd-914">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-914">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-915">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-915">Fixed cost</span></span></td>
<td><span data-ttu-id="4b3fd-916">241.05</span><span class="sxs-lookup"><span data-stu-id="4b3fd-916">241.05</span></span></td>
<td><span data-ttu-id="4b3fd-917">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-918">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4b3fd-918">Prod 2</span></span></td>
<td><span data-ttu-id="4b3fd-919">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="4b3fd-919">Product 2</span></span></td>
<td><span data-ttu-id="4b3fd-920">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-920">10001</span></span></td>
<td><span data-ttu-id="4b3fd-921">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-921">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-922">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-922">Fixed cost</span></span></td>
<td><span data-ttu-id="4b3fd-923">45.20</span><span class="sxs-lookup"><span data-stu-id="4b3fd-923">45.20</span></span></td>
<td><span data-ttu-id="4b3fd-924">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-925">CC003</span><span class="sxs-lookup"><span data-stu-id="4b3fd-925">CC003</span></span></td>
<td><span data-ttu-id="4b3fd-926">Montaj</span><span class="sxs-lookup"><span data-stu-id="4b3fd-926">Assembly</span></span></td>
<td><span data-ttu-id="4b3fd-927">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-927">10001</span></span></td>
<td><span data-ttu-id="4b3fd-928">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-928">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-929">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-929">Variable cost</span></span></td>
<td><span data-ttu-id="4b3fd-930">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="4b3fd-930">-2,977.17</span></span></td>
<td><span data-ttu-id="4b3fd-931">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-932">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-932">Prod 1</span></span></td>
<td><span data-ttu-id="4b3fd-933">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-933">Product 1</span></span></td>
<td><span data-ttu-id="4b3fd-934">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-934">10001</span></span></td>
<td><span data-ttu-id="4b3fd-935">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-935">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-936">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-936">Variable cost</span></span></td>
<td><span data-ttu-id="4b3fd-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="4b3fd-937">2,507.09</span></span></td>
<td><span data-ttu-id="4b3fd-938">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4b3fd-939">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4b3fd-939">Prod 2</span></span></td>
<td><span data-ttu-id="4b3fd-940">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="4b3fd-940">Product 2</span></span></td>
<td><span data-ttu-id="4b3fd-941">10001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-941">10001</span></span></td>
<td><span data-ttu-id="4b3fd-942">Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-942">Electricity</span></span></td>
<td><span data-ttu-id="4b3fd-943">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-943">Variable cost</span></span></td>
<td><span data-ttu-id="4b3fd-944">470.08</span><span class="sxs-lookup"><span data-stu-id="4b3fd-944">470.08</span></span></td>
<td><span data-ttu-id="4b3fd-945">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="4b3fd-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="4b3fd-946">Sonuç</span><span class="sxs-lookup"><span data-stu-id="4b3fd-946">Conclusion</span></span>
<span data-ttu-id="4b3fd-947">Mali muhasebede, Elektrik için 10.000,00 maliyet bir sözde maliyet merkezi kimliğine nakledilmiştir.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="4b3fd-948">Bu nedenle, maliyet muhasebecileri bu maliyetin tahsis edilmesi gerektiğini bilirler.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="4b3fd-949">Maliyet muhasebesinde, maliyetler kuruluş birimleri ve seviyeleri arasında, uygulanan kural ve ilkelere dayalı olarak akar.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="4b3fd-950">Her maliyet, maliyetlerin tahsisatı için en iyi değerlendirmeyi sağlayan bir tahsisat tabanı ile ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="4b3fd-951">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="4b3fd-952">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="4b3fd-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="4b3fd-953">Toplam</span><span class="sxs-lookup"><span data-stu-id="4b3fd-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="4b3fd-954">CC099</span><span class="sxs-lookup"><span data-stu-id="4b3fd-954">CC099</span></span></th>
<th><span data-ttu-id="4b3fd-955">CC001</span><span class="sxs-lookup"><span data-stu-id="4b3fd-955">CC001</span></span></th>
<th><span data-ttu-id="4b3fd-956">CC002</span><span class="sxs-lookup"><span data-stu-id="4b3fd-956">CC002</span></span></th>
<th><span data-ttu-id="4b3fd-957">CC003</span><span class="sxs-lookup"><span data-stu-id="4b3fd-957">CC003</span></span></th>
<th><span data-ttu-id="4b3fd-958">CC004</span><span class="sxs-lookup"><span data-stu-id="4b3fd-958">CC004</span></span></th>
<th><span data-ttu-id="4b3fd-959">Proj 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-959">Proj 1</span></span></th>
<th><span data-ttu-id="4b3fd-960">Proj 2</span><span class="sxs-lookup"><span data-stu-id="4b3fd-960">Proj 2</span></span></th>
<th><span data-ttu-id="4b3fd-961">Prod 1</span><span class="sxs-lookup"><span data-stu-id="4b3fd-961">Prod 1</span></span></th>
<th><span data-ttu-id="4b3fd-962">Prod 2</span><span class="sxs-lookup"><span data-stu-id="4b3fd-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="4b3fd-963">10001 Elektrik</span><span class="sxs-lookup"><span data-stu-id="4b3fd-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b3fd-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="4b3fd-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b3fd-965"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="4b3fd-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b3fd-966"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="4b3fd-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b3fd-967"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="4b3fd-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="4b3fd-968"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="4b3fd-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b3fd-969"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="4b3fd-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b3fd-970"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="4b3fd-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b3fd-971"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="4b3fd-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b3fd-972"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="4b3fd-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="4b3fd-973">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="4b3fd-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b3fd-974">0,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="4b3fd-975">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b3fd-976">0,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b3fd-977">0,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b3fd-978">0,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b3fd-979">0,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b3fd-980">0,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="4b3fd-981">776.36</span><span class="sxs-lookup"><span data-stu-id="4b3fd-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b3fd-982">223.64</span><span class="sxs-lookup"><span data-stu-id="4b3fd-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b3fd-983"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="4b3fd-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="4b3fd-984">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="4b3fd-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b3fd-985">000</span><span class="sxs-lookup"><span data-stu-id="4b3fd-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b3fd-986">0,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b3fd-987">0,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b3fd-988">0,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b3fd-989">0,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b3fd-990">30.00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b3fd-991">10,00</span><span class="sxs-lookup"><span data-stu-id="4b3fd-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b3fd-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="4b3fd-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b3fd-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="4b3fd-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4b3fd-994"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="4b3fd-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="4b3fd-995">Bu konu, birincil maliyet öğesi, 10001 Elektrik'in maliyet nesneleri arasında nasıl aktığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="4b3fd-996">Bu nedenle, bu genel gider maliyeti kuruluşun en düşük seviyesine tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="4b3fd-997">Başka bir deyişle, maliyet en alt düzeydeki maliyet nesnelerine aittir.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="4b3fd-998">Maliyetin, maliyet nesneleri arasında görsel bir akışına ihtiyacınız varsa, maliyetin akışını görselleştirmek için maliyet toplamı ilke kurallarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="4b3fd-999">Daha ayrıntılı bilgi için, Maliyet toplam ilkesine bakınız.</span><span class="sxs-lookup"><span data-stu-id="4b3fd-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="4b3fd-1000">(Bu konunun henüz tamamlanmadığını ancak yakında tamamlanacağını göz önünde bulundurun.)</span><span class="sxs-lookup"><span data-stu-id="4b3fd-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




