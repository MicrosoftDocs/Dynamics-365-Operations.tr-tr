---
title: "Genel gider hesaplaması"
description: "Bu konu, genel gider maliyetlerinin hesaplanması için tipik işlemleri açıklar."
author: YuyuScheller
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 1eb5560ba795ab6df61b5af889049810dd00d79e
ms.contentlocale: tr-tr
ms.lasthandoff: 06/29/2017


---

# <a name="overhead-calculation"></a><span data-ttu-id="79dcf-103">Genel gider hesaplaması</span><span class="sxs-lookup"><span data-stu-id="79dcf-103">Overhead calculation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="79dcf-104">Bu konu, genel gider maliyetlerinin hesaplanması için tipik işlemleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="79dcf-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="79dcf-105">Terim tanımı</span><span class="sxs-lookup"><span data-stu-id="79dcf-105">Term definition</span></span>
---------------

<span data-ttu-id="79dcf-106">Genel gider maliyetleri bir işletmenin çalışması için normalde uygulanan, ancak doğrudan herhangi bir özel iş, faaliyet, ürün veya hizmete ilişkilendirilmemiş olan maliyetlerdir.</span><span class="sxs-lookup"><span data-stu-id="79dcf-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="79dcf-107">Genel gider maliyetleri kar sağlama faaliyetlerinin oluşturulması için kritik destek sağlar.</span><span class="sxs-lookup"><span data-stu-id="79dcf-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="79dcf-108">Aşağıda bazı genel gider örnekleri verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="79dcf-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="79dcf-109">Kira</span><span class="sxs-lookup"><span data-stu-id="79dcf-109">Rent</span></span>
-   <span data-ttu-id="79dcf-110">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-110">Electricity</span></span>
-   <span data-ttu-id="79dcf-111">Yönetim maaşları</span><span class="sxs-lookup"><span data-stu-id="79dcf-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="79dcf-112">Genel gider hesaplaması genel bakış</span><span class="sxs-lookup"><span data-stu-id="79dcf-112">Overhead calculation overview</span></span>
<span data-ttu-id="79dcf-113">Genel gider hesaplama, maliyet muhasebesi ilkelerini doğru sırayla çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="79dcf-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="79dcf-114">Maliyet muhasebesi ilkeleri değiştiyse veya belirli hatalar algılandıysa, genel gider hesaplamasını aynı mali dönem için birden fazla kez yürütebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79dcf-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="79dcf-115">Her genel gider hesaplaması depolanır ve önceki sürümlerdeki hesaplamaları kıyaslamanıza olanak sağlayan, benzersiz bir sürüm kimliğine sahip olur.</span><span class="sxs-lookup"><span data-stu-id="79dcf-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="79dcf-116">Genel gider hesaplamasının oluşturduğu maliyet girişleri bir muhasebe tarihi alır.</span><span class="sxs-lookup"><span data-stu-id="79dcf-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="79dcf-117">Bu muhasebe tarihi, hesaplamada kullanılan mali dönemin bitiş tarihiyle eşleşir.</span><span class="sxs-lookup"><span data-stu-id="79dcf-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="79dcf-118">Benzersiz sürüm kimliği aşağıdaki öğelerden oluşur:</span><span class="sxs-lookup"><span data-stu-id="79dcf-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="79dcf-119">Sürüm türü</span><span class="sxs-lookup"><span data-stu-id="79dcf-119">Version type</span></span>
-   <span data-ttu-id="79dcf-120">Tarih ve saat</span><span class="sxs-lookup"><span data-stu-id="79dcf-120">Date and time</span></span>
-   <span data-ttu-id="79dcf-121">Maliyet muhasebesi defteri</span><span class="sxs-lookup"><span data-stu-id="79dcf-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="79dcf-122">Mali yıl</span><span class="sxs-lookup"><span data-stu-id="79dcf-122">Fiscal year</span></span>
-   <span data-ttu-id="79dcf-123">Mali dönem</span><span class="sxs-lookup"><span data-stu-id="79dcf-123">Fiscal period</span></span>

<span data-ttu-id="79dcf-124">Genel gider hesaplama, sürümden bağımsız olarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="79dcf-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="79dcf-125">Bu nedenle, Gerçek sürümden önce Bütçe sürümünü hesaplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79dcf-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="79dcf-126">Genel gider hesaplama dört adımdan oluşur, aşağıdaki çizimde gösterildiği gibi.</span><span class="sxs-lookup"><span data-stu-id="79dcf-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="79dcf-127">Her adımda, günlük girişleri olan bir günlük başlığı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="79dcf-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="79dcf-128">Bu günlük başlığı, her hesaplama adımı için giriş verilerini tutar.</span><span class="sxs-lookup"><span data-stu-id="79dcf-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="79dcf-129">İlkeler ve kurallar her günlük satırına uygulanır ve maliyet girişleri çıkış olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="79dcf-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="79dcf-130">Bu nedenle, her zaman tam izlenebilirliğe sahip olursunuz.</span><span class="sxs-lookup"><span data-stu-id="79dcf-130">Therefore, you always have full traceability.</span></span> 
<span data-ttu-id="79dcf-131">[![Genel gider hesaplaması](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="79dcf-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="79dcf-132">Elektrik genel gideri maliyetini hesapla ve tahsis et</span><span class="sxs-lookup"><span data-stu-id="79dcf-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="79dcf-133">Mali muhasebede, elektrik gibi bazı maliyetler peşin ödeme olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="79dcf-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="79dcf-134">Bu nedenle, Maliyet muhasebesi için ayrıntılı yönetim bilgiler sağlanmaz.</span><span class="sxs-lookup"><span data-stu-id="79dcf-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="79dcf-135">Maliyet muhasebesinde doğru yönetimsel bilgileri tüm yönetim birim ve düzeylerinde sağlamak için, maliyetlerin kuruluş birimleri arasında akması gerekir.</span><span class="sxs-lookup"><span data-stu-id="79dcf-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="79dcf-136">Bu akış, tüketimin doğru bir kaydına ya da adil bir değerlendirmeye dayanıyor olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="79dcf-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="79dcf-137">Genel muhasebede, bir elektrik maliyeti aşağıdaki tabloda gösterildiği gibi deftere nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="79dcf-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="79dcf-138">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="79dcf-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="79dcf-139">Maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="79dcf-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="79dcf-140">Ana hesap</span><span class="sxs-lookup"><span data-stu-id="79dcf-140">Main account</span></span></th>
<th><span data-ttu-id="79dcf-141">Muhasebe para birimi cinsinden tutar</span><span class="sxs-lookup"><span data-stu-id="79dcf-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79dcf-142">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="79dcf-143">CC099</span><span class="sxs-lookup"><span data-stu-id="79dcf-143">CC099</span></span></td>
<td><span data-ttu-id="79dcf-144">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="79dcf-144">Default cost center</span></span></td>
<td><span data-ttu-id="79dcf-145">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-145">10001</span></span></td>
<td><span data-ttu-id="79dcf-146">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-146">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="79dcf-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="79dcf-148">Adım 1: Maliyet davranışı hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="79dcf-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="79dcf-149">Varsayılan olarak, maliyeti girişleri kaynak veriden içeri alındığında, Maliyet muhasebesinde **Sınıflandırılmamış** maliyet davranışı sınıflandırmasını alırlar.</span><span class="sxs-lookup"><span data-stu-id="79dcf-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="79dcf-150">Maliyet davranışı ilke kuralları ekleyerek, maliyet girişlerini **Sabit maliyet** veya **Değişken maliyet** olarak yeniden sınıflandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79dcf-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="79dcf-151">Maliyet davranış kuralını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="79dcf-151">Define the cost behavior rule</span></span>

<span data-ttu-id="79dcf-152">Bazı durumlarda, sabit bir ücret maliyet parçasıdır ve kalan maliyet, tüketime dayanır.</span><span class="sxs-lookup"><span data-stu-id="79dcf-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="79dcf-153">Elektrik faturaları genellikle bu tanıma uyar.</span><span class="sxs-lookup"><span data-stu-id="79dcf-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="79dcf-154">Belirli bir sabit ücret ödedikten sonra, kilovat saatlik (Kwh) tüketim başına ödeme yaparsınız.</span><span class="sxs-lookup"><span data-stu-id="79dcf-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="79dcf-155">Örneğin, sabit maliyet masrafı 1.000,00 ise, maliyet davranışı kural nasıl tanımlanır:</span><span class="sxs-lookup"><span data-stu-id="79dcf-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="79dcf-156">Sabit tutar 1.000,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="79dcf-157">0 &lt;= 1.000,00 = Sabit</span><span class="sxs-lookup"><span data-stu-id="79dcf-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="79dcf-158">1000,01 &lt; N = Değişken</span><span class="sxs-lookup"><span data-stu-id="79dcf-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="79dcf-159">Günlük</span><span class="sxs-lookup"><span data-stu-id="79dcf-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="79dcf-160">Günlük</span><span class="sxs-lookup"><span data-stu-id="79dcf-160">Journal</span></span></th>
<th><span data-ttu-id="79dcf-161">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="79dcf-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="79dcf-162">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="79dcf-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="79dcf-163">Sürüm</span><span class="sxs-lookup"><span data-stu-id="79dcf-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79dcf-164">00001</span><span class="sxs-lookup"><span data-stu-id="79dcf-164">00001</span></span></td>
<td><span data-ttu-id="79dcf-165">Maliyet davranışı hesaplama günlüğü</span><span class="sxs-lookup"><span data-stu-id="79dcf-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="79dcf-166">Mali</span><span class="sxs-lookup"><span data-stu-id="79dcf-166">Fiscal</span></span></td>
<td><span data-ttu-id="79dcf-167">2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-167">2017</span></span></td>
<td><span data-ttu-id="79dcf-168">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-168">Period 1</span></span></td>
<td><span data-ttu-id="79dcf-169">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="79dcf-170">Günlük girişleri (Maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="79dcf-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="79dcf-171">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="79dcf-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="79dcf-172">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="79dcf-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="79dcf-173">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="79dcf-173">Cost element</span></span></th>
<th><span data-ttu-id="79dcf-174">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="79dcf-174">Cost behavior</span></span></th>
<th><span data-ttu-id="79dcf-175">Tutar</span><span class="sxs-lookup"><span data-stu-id="79dcf-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79dcf-176">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="79dcf-177">CC099</span><span class="sxs-lookup"><span data-stu-id="79dcf-177">CC099</span></span></td>
<td><span data-ttu-id="79dcf-178">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="79dcf-178">Default cost center</span></span></td>
<td><span data-ttu-id="79dcf-179">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-179">10001</span></span></td>
<td><span data-ttu-id="79dcf-180">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-180">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-181">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="79dcf-181">Unclassified</span></span></td>
<td><span data-ttu-id="79dcf-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="79dcf-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="79dcf-183">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="79dcf-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79dcf-184">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="79dcf-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="79dcf-185">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="79dcf-185">Cost element</span></span></th>
<th><span data-ttu-id="79dcf-186">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="79dcf-186">Cost behavior</span></span></th>
<th><span data-ttu-id="79dcf-187">Tutar</span><span class="sxs-lookup"><span data-stu-id="79dcf-187">Amount</span></span></th>
<th><span data-ttu-id="79dcf-188">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="79dcf-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79dcf-189">CC099</span><span class="sxs-lookup"><span data-stu-id="79dcf-189">CC099</span></span></td>
<td><span data-ttu-id="79dcf-190">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="79dcf-190">Default cost center</span></span></td>
<td><span data-ttu-id="79dcf-191">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-191">10001</span></span></td>
<td><span data-ttu-id="79dcf-192">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-192">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-193">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="79dcf-193">Unclassified</span></span></td>
<td><span data-ttu-id="79dcf-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="79dcf-194">10,000.00</span></span></td>
<td><span data-ttu-id="79dcf-195">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-196">CC099</span><span class="sxs-lookup"><span data-stu-id="79dcf-196">CC099</span></span></td>
<td><span data-ttu-id="79dcf-197">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="79dcf-197">Default cost center</span></span></td>
<td><span data-ttu-id="79dcf-198">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-198">10001</span></span></td>
<td><span data-ttu-id="79dcf-199">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-199">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-200">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="79dcf-200">Unclassified</span></span></td>
<td><span data-ttu-id="79dcf-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-201">-10,000.00</span></span></td>
<td><span data-ttu-id="79dcf-202">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-203">CC099</span><span class="sxs-lookup"><span data-stu-id="79dcf-203">CC099</span></span></td>
<td><span data-ttu-id="79dcf-204">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="79dcf-204">Default cost center</span></span></td>
<td><span data-ttu-id="79dcf-205">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-205">10001</span></span></td>
<td><span data-ttu-id="79dcf-206">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-206">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-207">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-207">Fixed cost</span></span></td>
<td><span data-ttu-id="79dcf-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-208">1,000.00</span></span></td>
<td><span data-ttu-id="79dcf-209">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-210">CC099</span><span class="sxs-lookup"><span data-stu-id="79dcf-210">CC099</span></span></td>
<td><span data-ttu-id="79dcf-211">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="79dcf-211">Default cost center</span></span></td>
<td><span data-ttu-id="79dcf-212">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-212">10001</span></span></td>
<td><span data-ttu-id="79dcf-213">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-213">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-214">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-214">Variable cost</span></span></td>
<td><span data-ttu-id="79dcf-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="79dcf-215">9,000.00</span></span></td>
<td><span data-ttu-id="79dcf-216">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="79dcf-217">Maliyet davranışı hakkında ayrıntılı bilgi için bkz. Maliyet davranışı ilkesi.</span><span class="sxs-lookup"><span data-stu-id="79dcf-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="79dcf-218">(Bu konunun henüz tamamlanmadığını ancak yakında tamamlanacağını göz önünde bulundurun.)</span><span class="sxs-lookup"><span data-stu-id="79dcf-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="79dcf-219">Adım 2: Maliyet dağıtımı hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="79dcf-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="79dcf-220">Maliyet dağıtımı, bir nesneden bir veya daha fazlasına ilgili tahsisat tabanı uygulayarak maliyeti yeniden dağıtmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="79dcf-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="79dcf-221">Maliyet dağıtımı ve maliyet tahsisatı, maliyet dağıtımının her zaman orijinal maliyetin birincil maliyet öğesinde bulunmasıyla farklılık gösterir.</span><span class="sxs-lookup"><span data-stu-id="79dcf-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="79dcf-222">Maliyet dağıtım kuralını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="79dcf-222">Define the cost distribution rule</span></span>

<span data-ttu-id="79dcf-223">Mali muhasebede, elektrik maliyetleri çoğu zaman peşin ödeme olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="79dcf-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="79dcf-224">Maliyet muhasebesinde ise bu yöntem yeterince ayrıntılı değildir.</span><span class="sxs-lookup"><span data-stu-id="79dcf-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="79dcf-225">Değişken maliyet, maliyet nesnelerine tek tek, adil bir temele dayanarak dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="79dcf-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="79dcf-226">En mantıklı tahsisat, elektrik kullanımını (Kwh) temel alarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="79dcf-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="79dcf-227">Elektrik adına sahip, istatistiksel bir boyut üyesi oluşturulur ve elektrik tüketimi kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="79dcf-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="79dcf-228">Varsayıla olarak, tüm istatistiksel boyut üyeleri tahsisat tabanları olarak kullanılabilir hale gelir.</span><span class="sxs-lookup"><span data-stu-id="79dcf-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79dcf-229">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="79dcf-229">Cost object</span></span></th>
<th><span data-ttu-id="79dcf-230">Kwh</span><span class="sxs-lookup"><span data-stu-id="79dcf-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79dcf-231">CC001</span><span class="sxs-lookup"><span data-stu-id="79dcf-231">CC001</span></span></td>
<td><span data-ttu-id="79dcf-232">İK</span><span class="sxs-lookup"><span data-stu-id="79dcf-232">HR</span></span></td>
<td><span data-ttu-id="79dcf-233">1.000</span><span class="sxs-lookup"><span data-stu-id="79dcf-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-234">CC002</span><span class="sxs-lookup"><span data-stu-id="79dcf-234">CC002</span></span></td>
<td><span data-ttu-id="79dcf-235">Finans</span><span class="sxs-lookup"><span data-stu-id="79dcf-235">Finance</span></span></td>
<td><span data-ttu-id="79dcf-236">6,000</span><span class="sxs-lookup"><span data-stu-id="79dcf-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-237">CC003</span><span class="sxs-lookup"><span data-stu-id="79dcf-237">CC003</span></span></td>
<td><span data-ttu-id="79dcf-238">Montaj</span><span class="sxs-lookup"><span data-stu-id="79dcf-238">Assembly</span></span></td>
<td><span data-ttu-id="79dcf-239">0</span><span class="sxs-lookup"><span data-stu-id="79dcf-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="79dcf-240">Aşağıdaki tablo, elektrik tüketiminin değişken maliyetler için bir tahsisat tabanlı olarak uygulandığındaki sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="79dcf-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79dcf-241">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="79dcf-241">Cost object</span></span></th>
<th><span data-ttu-id="79dcf-242">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="79dcf-242">Magnitude</span></span></th>
<th><span data-ttu-id="79dcf-243">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="79dcf-243">Allocation factor</span></span></th>
<th><span data-ttu-id="79dcf-244">Tutar</span><span class="sxs-lookup"><span data-stu-id="79dcf-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79dcf-245">CC001</span><span class="sxs-lookup"><span data-stu-id="79dcf-245">CC001</span></span></td>
<td><span data-ttu-id="79dcf-246">İK</span><span class="sxs-lookup"><span data-stu-id="79dcf-246">HR</span></span></td>
<td><span data-ttu-id="79dcf-247">1.000</span><span class="sxs-lookup"><span data-stu-id="79dcf-247">1,000</span></span></td>
<td><span data-ttu-id="79dcf-248">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="79dcf-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="79dcf-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-250">CC002</span><span class="sxs-lookup"><span data-stu-id="79dcf-250">CC002</span></span></td>
<td><span data-ttu-id="79dcf-251">Finans</span><span class="sxs-lookup"><span data-stu-id="79dcf-251">Finance</span></span></td>
<td><span data-ttu-id="79dcf-252">6,000</span><span class="sxs-lookup"><span data-stu-id="79dcf-252">6,000</span></span></td>
<td><span data-ttu-id="79dcf-253">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="79dcf-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="79dcf-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-255">CC003</span><span class="sxs-lookup"><span data-stu-id="79dcf-255">CC003</span></span></td>
<td><span data-ttu-id="79dcf-256">Montaj</span><span class="sxs-lookup"><span data-stu-id="79dcf-256">Assembly</span></span></td>
<td><span data-ttu-id="79dcf-257">0</span><span class="sxs-lookup"><span data-stu-id="79dcf-257">0</span></span></td>
<td><span data-ttu-id="79dcf-258">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="79dcf-259">0,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="79dcf-260">Sabit maliyet, elektrik tüketmiş olan tekil maliyet nesnelerine eşit miktarda dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="79dcf-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="79dcf-261">Bu sonuca, Elektrik istatistiksel boyut öğesini bir formül tahsisat tabanında kullanarak ulaşabilirsiniz: (Elektrik &gt; 0,00) Aşağıdaki tablo, elektrik tüketimi değişken maliyetler için bir tahsisat tabanı olarak kullanıldığında ortaya çıkan sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="79dcf-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79dcf-262">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="79dcf-262">Cost object</span></span></th>
<th><span data-ttu-id="79dcf-263">Formül</span><span class="sxs-lookup"><span data-stu-id="79dcf-263">Formula</span></span></th>
<th><span data-ttu-id="79dcf-264">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="79dcf-264">Magnitude</span></span></th>
<th><span data-ttu-id="79dcf-265">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="79dcf-265">Allocation factor</span></span></th>
<th><span data-ttu-id="79dcf-266">Tutar</span><span class="sxs-lookup"><span data-stu-id="79dcf-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79dcf-267">CC001</span><span class="sxs-lookup"><span data-stu-id="79dcf-267">CC001</span></span></td>
<td><span data-ttu-id="79dcf-268">İK</span><span class="sxs-lookup"><span data-stu-id="79dcf-268">HR</span></span></td>
<td><span data-ttu-id="79dcf-269">(1,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="79dcf-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="79dcf-270">1</span><span class="sxs-lookup"><span data-stu-id="79dcf-270">1</span></span></td>
<td><span data-ttu-id="79dcf-271">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="79dcf-272">500.00</span><span class="sxs-lookup"><span data-stu-id="79dcf-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-273">CC002</span><span class="sxs-lookup"><span data-stu-id="79dcf-273">CC002</span></span></td>
<td><span data-ttu-id="79dcf-274">Finans</span><span class="sxs-lookup"><span data-stu-id="79dcf-274">Finance</span></span></td>
<td><span data-ttu-id="79dcf-275">(6,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="79dcf-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="79dcf-276">1</span><span class="sxs-lookup"><span data-stu-id="79dcf-276">1</span></span></td>
<td><span data-ttu-id="79dcf-277">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="79dcf-278">500.00</span><span class="sxs-lookup"><span data-stu-id="79dcf-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-279">CC003</span><span class="sxs-lookup"><span data-stu-id="79dcf-279">CC003</span></span></td>
<td><span data-ttu-id="79dcf-280">Montaj</span><span class="sxs-lookup"><span data-stu-id="79dcf-280">Assembly</span></span></td>
<td><span data-ttu-id="79dcf-281">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="79dcf-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="79dcf-282">0</span><span class="sxs-lookup"><span data-stu-id="79dcf-282">0</span></span></td>
<td><span data-ttu-id="79dcf-283">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="79dcf-284">0,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="79dcf-285">Günlük</span><span class="sxs-lookup"><span data-stu-id="79dcf-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="79dcf-286">Günlük</span><span class="sxs-lookup"><span data-stu-id="79dcf-286">Journal</span></span></th>
<th><span data-ttu-id="79dcf-287">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="79dcf-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="79dcf-288">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="79dcf-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="79dcf-289">Sürüm</span><span class="sxs-lookup"><span data-stu-id="79dcf-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79dcf-290">00002</span><span class="sxs-lookup"><span data-stu-id="79dcf-290">00002</span></span></td>
<td><span data-ttu-id="79dcf-291">Maliyet dağıtımı hesaplama günlüğü</span><span class="sxs-lookup"><span data-stu-id="79dcf-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="79dcf-292">Mali</span><span class="sxs-lookup"><span data-stu-id="79dcf-292">Fiscal</span></span></td>
<td><span data-ttu-id="79dcf-293">2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-293">2017</span></span></td>
<td><span data-ttu-id="79dcf-294">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-294">Period 1</span></span></td>
<td><span data-ttu-id="79dcf-295">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="79dcf-296">Günlük girişleri (Maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="79dcf-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="79dcf-297">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="79dcf-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="79dcf-298">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="79dcf-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="79dcf-299">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="79dcf-299">Cost element</span></span></th>
<th><span data-ttu-id="79dcf-300">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="79dcf-300">Cost behavior</span></span></th>
<th><span data-ttu-id="79dcf-301">Tutar</span><span class="sxs-lookup"><span data-stu-id="79dcf-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79dcf-302">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="79dcf-303">CC099</span><span class="sxs-lookup"><span data-stu-id="79dcf-303">CC099</span></span></td>
<td><span data-ttu-id="79dcf-304">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="79dcf-304">Default cost center</span></span></td>
<td><span data-ttu-id="79dcf-305">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-305">10001</span></span></td>
<td><span data-ttu-id="79dcf-306">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-306">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-307">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-307">Fixed cost</span></span></td>
<td><span data-ttu-id="79dcf-308">1.000,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-309">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="79dcf-310">CC099</span><span class="sxs-lookup"><span data-stu-id="79dcf-310">CC099</span></span></td>
<td><span data-ttu-id="79dcf-311">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="79dcf-311">Default cost center</span></span></td>
<td><span data-ttu-id="79dcf-312">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-312">10001</span></span></td>
<td><span data-ttu-id="79dcf-313">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-313">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-314">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-314">Variable cost</span></span></td>
<td><span data-ttu-id="79dcf-315">9,000.00</span><span class="sxs-lookup"><span data-stu-id="79dcf-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="79dcf-316">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="79dcf-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79dcf-317">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="79dcf-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="79dcf-318">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="79dcf-318">Cost element</span></span></th>
<th><span data-ttu-id="79dcf-319">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="79dcf-319">Cost behavior</span></span></th>
<th><span data-ttu-id="79dcf-320">Tutar</span><span class="sxs-lookup"><span data-stu-id="79dcf-320">Amount</span></span></th>
<th><span data-ttu-id="79dcf-321">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="79dcf-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79dcf-322">CC099</span><span class="sxs-lookup"><span data-stu-id="79dcf-322">CC099</span></span></td>
<td><span data-ttu-id="79dcf-323">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="79dcf-323">Default cost center</span></span></td>
<td><span data-ttu-id="79dcf-324">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-324">10001</span></span></td>
<td><span data-ttu-id="79dcf-325">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-325">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-326">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-326">Fixed cost</span></span></td>
<td><span data-ttu-id="79dcf-327">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-327">-1,000.00</span></span></td>
<td><span data-ttu-id="79dcf-328">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-329">CC001</span><span class="sxs-lookup"><span data-stu-id="79dcf-329">CC001</span></span></td>
<td><span data-ttu-id="79dcf-330">İK</span><span class="sxs-lookup"><span data-stu-id="79dcf-330">HR</span></span></td>
<td><span data-ttu-id="79dcf-331">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-331">10001</span></span></td>
<td><span data-ttu-id="79dcf-332">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-332">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-333">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-333">Fixed cost</span></span></td>
<td><span data-ttu-id="79dcf-334">500.00</span><span class="sxs-lookup"><span data-stu-id="79dcf-334">500.00</span></span></td>
<td><span data-ttu-id="79dcf-335">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-336">CC002</span><span class="sxs-lookup"><span data-stu-id="79dcf-336">CC002</span></span></td>
<td><span data-ttu-id="79dcf-337">Finans</span><span class="sxs-lookup"><span data-stu-id="79dcf-337">Finance</span></span></td>
<td><span data-ttu-id="79dcf-338">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-338">10001</span></span></td>
<td><span data-ttu-id="79dcf-339">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-339">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-340">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-340">Fixed cost</span></span></td>
<td><span data-ttu-id="79dcf-341">500.00</span><span class="sxs-lookup"><span data-stu-id="79dcf-341">500.00</span></span></td>
<td><span data-ttu-id="79dcf-342">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-343">CC099</span><span class="sxs-lookup"><span data-stu-id="79dcf-343">CC099</span></span></td>
<td><span data-ttu-id="79dcf-344">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="79dcf-344">Default cost center</span></span></td>
<td><span data-ttu-id="79dcf-345">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-345">10001</span></span></td>
<td><span data-ttu-id="79dcf-346">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-346">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-347">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-347">Variable cost</span></span></td>
<td><span data-ttu-id="79dcf-348">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-348">-9,000.00</span></span></td>
<td><span data-ttu-id="79dcf-349">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-350">CC001</span><span class="sxs-lookup"><span data-stu-id="79dcf-350">CC001</span></span></td>
<td><span data-ttu-id="79dcf-351">İK</span><span class="sxs-lookup"><span data-stu-id="79dcf-351">HR</span></span></td>
<td><span data-ttu-id="79dcf-352">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-352">10001</span></span></td>
<td><span data-ttu-id="79dcf-353">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-353">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-354">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-354">Variable cost</span></span></td>
<td><span data-ttu-id="79dcf-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="79dcf-355">1,285.71</span></span></td>
<td><span data-ttu-id="79dcf-356">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-357">CC002</span><span class="sxs-lookup"><span data-stu-id="79dcf-357">CC002</span></span></td>
<td><span data-ttu-id="79dcf-358">Finans</span><span class="sxs-lookup"><span data-stu-id="79dcf-358">Finance</span></span></td>
<td><span data-ttu-id="79dcf-359">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-359">10001</span></span></td>
<td><span data-ttu-id="79dcf-360">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-360">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-361">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-361">Variable cost</span></span></td>
<td><span data-ttu-id="79dcf-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="79dcf-362">7,714.29</span></span></td>
<td><span data-ttu-id="79dcf-363">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="79dcf-364">Maliyet dağıtımı ve tahsisat tabanları hakkında ayrıntılı bilgi için, bakınız Maliyet dağıtım ilkesi ve Tahsisat tabanları.</span><span class="sxs-lookup"><span data-stu-id="79dcf-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="79dcf-365">(Bu konunun henüz tamamlanmadığını ancak yakında tamamlanacağını göz önünde bulundurun.)</span><span class="sxs-lookup"><span data-stu-id="79dcf-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="79dcf-366">Adım 3: Genel gider oranı hesaplama işlemi</span><span class="sxs-lookup"><span data-stu-id="79dcf-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="79dcf-367">Genel gider oranı, bir veya birden fazla belirli maliyet nesnesine masraf yüklemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="79dcf-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="79dcf-368">Masraf, önceden belirlenmiş maliyet oranına ve tahsisat tabanından hesaplanan büyüklüğe dayanır.</span><span class="sxs-lookup"><span data-stu-id="79dcf-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="79dcf-369">Genel gider oranını tanımlama</span><span class="sxs-lookup"><span data-stu-id="79dcf-369">Define the overhead rate</span></span>

<span data-ttu-id="79dcf-370">Maliyet nesnesi CC001 HR, bir dizi dahili projeye katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="79dcf-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="79dcf-371">HR projeleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="79dcf-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79dcf-372">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="79dcf-372">Cost object</span></span></th>
<th><span data-ttu-id="79dcf-373">Saatler</span><span class="sxs-lookup"><span data-stu-id="79dcf-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79dcf-374">Proj 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-374">Proj 1</span></span></td>
<td><span data-ttu-id="79dcf-375">Proje 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-375">Project 1</span></span></td>
<td><span data-ttu-id="79dcf-376">3</span><span class="sxs-lookup"><span data-stu-id="79dcf-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-377">Proj 2</span><span class="sxs-lookup"><span data-stu-id="79dcf-377">Proj 2</span></span></td>
<td><span data-ttu-id="79dcf-378">Proje 2</span><span class="sxs-lookup"><span data-stu-id="79dcf-378">Project 2</span></span></td>
<td><span data-ttu-id="79dcf-379">1</span><span class="sxs-lookup"><span data-stu-id="79dcf-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="79dcf-380">Maliyet projeleri dağıtımı için bir önceden belirlenmiş maliyet oranı tanımlandı.</span><span class="sxs-lookup"><span data-stu-id="79dcf-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79dcf-381">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="79dcf-381">Cost object</span></span></th>
<th><span data-ttu-id="79dcf-382">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="79dcf-382">Cost element</span></span></th>
<th><span data-ttu-id="79dcf-383">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="79dcf-383">Cost behavior</span></span></th>
<th><span data-ttu-id="79dcf-384">Birimler</span><span class="sxs-lookup"><span data-stu-id="79dcf-384">Units</span></span></th>
<th><span data-ttu-id="79dcf-385">Ücret</span><span class="sxs-lookup"><span data-stu-id="79dcf-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79dcf-386">CC001</span><span class="sxs-lookup"><span data-stu-id="79dcf-386">CC001</span></span></td>
<td><span data-ttu-id="79dcf-387">İK</span><span class="sxs-lookup"><span data-stu-id="79dcf-387">HR</span></span></td>
<td><span data-ttu-id="79dcf-388">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-388">10001</span></span></td>
<td><span data-ttu-id="79dcf-389">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-389">Variable cost</span></span></td>
<td><span data-ttu-id="79dcf-390">1</span><span class="sxs-lookup"><span data-stu-id="79dcf-390">1</span></span></td>
<td><span data-ttu-id="79dcf-391">10</span><span class="sxs-lookup"><span data-stu-id="79dcf-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="79dcf-392">Aşağıdaki tablo, HR projeleri bir tahsisat tabanı olarak uygulandığındaki sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="79dcf-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79dcf-393">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="79dcf-393">Cost object</span></span></th>
<th><span data-ttu-id="79dcf-394">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="79dcf-394">Magnitude</span></span></th>
<th><span data-ttu-id="79dcf-395">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="79dcf-395">Cost element</span></span></th>
<th><span data-ttu-id="79dcf-396">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="79dcf-396">Allocation factor</span></span></th>
<th><span data-ttu-id="79dcf-397">Tutar</span><span class="sxs-lookup"><span data-stu-id="79dcf-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79dcf-398">Proj 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-398">Proj 1</span></span></td>
<td><span data-ttu-id="79dcf-399">Proje 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-399">Project 1</span></span></td>
<td><span data-ttu-id="79dcf-400">3</span><span class="sxs-lookup"><span data-stu-id="79dcf-400">3</span></span></td>
<td><span data-ttu-id="79dcf-401">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-401">10001</span></span></td>
<td><span data-ttu-id="79dcf-402">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="79dcf-403">30.00</span><span class="sxs-lookup"><span data-stu-id="79dcf-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-404">Proj 2</span><span class="sxs-lookup"><span data-stu-id="79dcf-404">Proj 2</span></span></td>
<td><span data-ttu-id="79dcf-405">Proje 2</span><span class="sxs-lookup"><span data-stu-id="79dcf-405">Project 2</span></span></td>
<td><span data-ttu-id="79dcf-406">1</span><span class="sxs-lookup"><span data-stu-id="79dcf-406">1</span></span></td>
<td><span data-ttu-id="79dcf-407">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-407">10001</span></span></td>
<td><span data-ttu-id="79dcf-408">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="79dcf-409">10,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="79dcf-410">Günlük</span><span class="sxs-lookup"><span data-stu-id="79dcf-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="79dcf-411">Günlük</span><span class="sxs-lookup"><span data-stu-id="79dcf-411">Journal</span></span></th>
<th><span data-ttu-id="79dcf-412">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="79dcf-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="79dcf-413">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="79dcf-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="79dcf-414">Sürüm</span><span class="sxs-lookup"><span data-stu-id="79dcf-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79dcf-415">00003</span><span class="sxs-lookup"><span data-stu-id="79dcf-415">00003</span></span></td>
<td><span data-ttu-id="79dcf-416">Genel gider oranı hesaplaması günlüğü</span><span class="sxs-lookup"><span data-stu-id="79dcf-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="79dcf-417">Mali</span><span class="sxs-lookup"><span data-stu-id="79dcf-417">Fiscal</span></span></td>
<td><span data-ttu-id="79dcf-418">2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-418">2017</span></span></td>
<td><span data-ttu-id="79dcf-419">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-419">Period 1</span></span></td>
<td><span data-ttu-id="79dcf-420">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="79dcf-421">Günlük girişleri (Genel gider oranı hesaplaması için günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="79dcf-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="79dcf-422">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="79dcf-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="79dcf-423">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="79dcf-423">Cost object</span></span></th>
<th><span data-ttu-id="79dcf-424">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="79dcf-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79dcf-425">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="79dcf-426">Proj 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-426">Proj 1</span></span></td>
<td><span data-ttu-id="79dcf-427">Dahili Proj 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="79dcf-428">3,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-429">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="79dcf-430">Proj 2</span><span class="sxs-lookup"><span data-stu-id="79dcf-430">Proj 2</span></span></td>
<td><span data-ttu-id="79dcf-431">Dahili Proj 2</span><span class="sxs-lookup"><span data-stu-id="79dcf-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="79dcf-432">1.00</span><span class="sxs-lookup"><span data-stu-id="79dcf-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="79dcf-433">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="79dcf-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79dcf-434">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="79dcf-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="79dcf-435">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="79dcf-435">Cost element</span></span></th>
<th><span data-ttu-id="79dcf-436">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="79dcf-436">Cost behavior</span></span></th>
<th><span data-ttu-id="79dcf-437">Tutar</span><span class="sxs-lookup"><span data-stu-id="79dcf-437">Amount</span></span></th>
<th><span data-ttu-id="79dcf-438">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="79dcf-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79dcf-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="79dcf-439">CC0001</span></span></td>
<td><span data-ttu-id="79dcf-440">İK</span><span class="sxs-lookup"><span data-stu-id="79dcf-440">HR</span></span></td>
<td><span data-ttu-id="79dcf-441">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-441">10001</span></span></td>
<td><span data-ttu-id="79dcf-442">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-442">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-443">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-443">Variable cost</span></span></td>
<td><span data-ttu-id="79dcf-444">-30,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-444">-30.00</span></span></td>
<td><span data-ttu-id="79dcf-445">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-446">Proj 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-446">Proj 1</span></span></td>
<td><span data-ttu-id="79dcf-447">Dahili Proj 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="79dcf-448">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-448">10001</span></span></td>
<td><span data-ttu-id="79dcf-449">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-449">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-450">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-450">Variable cost</span></span></td>
<td><span data-ttu-id="79dcf-451">30.00</span><span class="sxs-lookup"><span data-stu-id="79dcf-451">30.00</span></span></td>
<td><span data-ttu-id="79dcf-452">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-453">CC001</span><span class="sxs-lookup"><span data-stu-id="79dcf-453">CC001</span></span></td>
<td><span data-ttu-id="79dcf-454">İK</span><span class="sxs-lookup"><span data-stu-id="79dcf-454">HR</span></span></td>
<td><span data-ttu-id="79dcf-455">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-455">10001</span></span></td>
<td><span data-ttu-id="79dcf-456">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-456">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-457">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-457">Variable cost</span></span></td>
<td><span data-ttu-id="79dcf-458">-10,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-458">-10.00</span></span></td>
<td><span data-ttu-id="79dcf-459">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-460">Proj 2</span><span class="sxs-lookup"><span data-stu-id="79dcf-460">Proj 2</span></span></td>
<td><span data-ttu-id="79dcf-461">Dahili Proj 2</span><span class="sxs-lookup"><span data-stu-id="79dcf-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="79dcf-462">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-462">10001</span></span></td>
<td><span data-ttu-id="79dcf-463">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-463">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-464">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-464">Variable cost</span></span></td>
<td><span data-ttu-id="79dcf-465">10,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-465">10.00</span></span></td>
<td><span data-ttu-id="79dcf-466">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="79dcf-467">Genel gider oranı ilkesi hakkında ayrıntılı bilgi için, Genel gider oranları ilkesi ve Tahsisat tabanlarına bakın.</span><span class="sxs-lookup"><span data-stu-id="79dcf-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="79dcf-468">(Bu konunun henüz tamamlanmadığını ancak yakında tamamlanacağını göz önünde bulundurun.)</span><span class="sxs-lookup"><span data-stu-id="79dcf-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="79dcf-469">Adım 4: Maliyet tahsisat hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="79dcf-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="79dcf-470">Tahsisat, bir tahsisat tabanı kullanarak bir maliyet nesnesinin diğer maliyet nesnelerine bakiyesini tahsis eder.</span><span class="sxs-lookup"><span data-stu-id="79dcf-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="79dcf-471">Finance and Operations karşılıklı tahsisat yöntemin destekler.</span><span class="sxs-lookup"><span data-stu-id="79dcf-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="79dcf-472">Karşılıklı tahsisat yönteminde, yardımcı maliyet nesnelerinin değiştiği karşılıklı hizmetler tümüyle tanınır.</span><span class="sxs-lookup"><span data-stu-id="79dcf-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="79dcf-473">Sistem, tahsisatların doğru gerçekleştireceği sırayı otomatik olarak belirler.</span><span class="sxs-lookup"><span data-stu-id="79dcf-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="79dcf-474">Bir maliyet nesnesinin bakiyesi tek bir tahsisat tabanı tarafından tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="79dcf-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="79dcf-475">Yeni maliyet nesnesi boyutları arasındaki tahsisatlar ve onların üyeleri desteklenir.</span><span class="sxs-lookup"><span data-stu-id="79dcf-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="79dcf-476">Tahsisatın sırası, maliyet kontrol birimi tarafından kontrol edilir.</span><span class="sxs-lookup"><span data-stu-id="79dcf-476">The allocation order is controlled by the cost control unit.</span></span> <span data-ttu-id="79dcf-477">[![Karşılıklı yöntemi](./media/reciprocal-method.png)]</span><span class="sxs-lookup"><span data-stu-id="79dcf-477">[![Reciprocal method](./media/reciprocal-method.png)]</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="79dcf-478">Maliyet tahsisatını tanımla</span><span class="sxs-lookup"><span data-stu-id="79dcf-478">Define the cost allocation</span></span>

<span data-ttu-id="79dcf-479">Bir maliyetin akışını nasıl izleyeceğinize dair basit bir örnek aşağıda verilmiştir,</span><span class="sxs-lookup"><span data-stu-id="79dcf-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="79dcf-480">Maliyet nesnesi CC001 HR, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="79dcf-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="79dcf-481">HR hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="79dcf-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79dcf-482">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="79dcf-482">Cost object</span></span></th>
<th><span data-ttu-id="79dcf-483">HR hizmetleri</span><span class="sxs-lookup"><span data-stu-id="79dcf-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79dcf-484">CC002</span><span class="sxs-lookup"><span data-stu-id="79dcf-484">CC002</span></span></td>
<td><span data-ttu-id="79dcf-485">Finans</span><span class="sxs-lookup"><span data-stu-id="79dcf-485">Finance</span></span></td>
<td><span data-ttu-id="79dcf-486">35</span><span class="sxs-lookup"><span data-stu-id="79dcf-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-487">CC003</span><span class="sxs-lookup"><span data-stu-id="79dcf-487">CC003</span></span></td>
<td><span data-ttu-id="79dcf-488">Montaj</span><span class="sxs-lookup"><span data-stu-id="79dcf-488">Assembly</span></span></td>
<td><span data-ttu-id="79dcf-489">55</span><span class="sxs-lookup"><span data-stu-id="79dcf-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-490">CC004</span><span class="sxs-lookup"><span data-stu-id="79dcf-490">CC004</span></span></td>
<td><span data-ttu-id="79dcf-491">Paketleme</span><span class="sxs-lookup"><span data-stu-id="79dcf-491">Packaging</span></span></td>
<td><span data-ttu-id="79dcf-492">10</span><span class="sxs-lookup"><span data-stu-id="79dcf-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="79dcf-493">Maliyet nesnesi CC002 Finans, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="79dcf-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="79dcf-494">Finans hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="79dcf-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79dcf-495">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="79dcf-495">Cost object</span></span></th>
<th><span data-ttu-id="79dcf-496">Finans hizmetleri</span><span class="sxs-lookup"><span data-stu-id="79dcf-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79dcf-497">CC003</span><span class="sxs-lookup"><span data-stu-id="79dcf-497">CC003</span></span></td>
<td><span data-ttu-id="79dcf-498">Montaj</span><span class="sxs-lookup"><span data-stu-id="79dcf-498">Assembly</span></span></td>
<td><span data-ttu-id="79dcf-499">65</span><span class="sxs-lookup"><span data-stu-id="79dcf-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-500">CC004</span><span class="sxs-lookup"><span data-stu-id="79dcf-500">CC004</span></span></td>
<td><span data-ttu-id="79dcf-501">Paketleme</span><span class="sxs-lookup"><span data-stu-id="79dcf-501">Packaging</span></span></td>
<td><span data-ttu-id="79dcf-502">35</span><span class="sxs-lookup"><span data-stu-id="79dcf-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="79dcf-503">Maliyet nesnesi CC003 Derleme, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="79dcf-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="79dcf-504">Derleme hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="79dcf-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79dcf-505">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="79dcf-505">Cost object</span></span></th>
<th><span data-ttu-id="79dcf-506">Derleme Hizmetleri (saat)</span><span class="sxs-lookup"><span data-stu-id="79dcf-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79dcf-507">Prod 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-507">Prod 1</span></span></td>
<td><span data-ttu-id="79dcf-508">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-508">Product 1</span></span></td>
<td><span data-ttu-id="79dcf-509">60</span><span class="sxs-lookup"><span data-stu-id="79dcf-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-510">Prod 2</span><span class="sxs-lookup"><span data-stu-id="79dcf-510">Prod 2</span></span></td>
<td><span data-ttu-id="79dcf-511">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="79dcf-511">Product 2</span></span></td>
<td><span data-ttu-id="79dcf-512">20</span><span class="sxs-lookup"><span data-stu-id="79dcf-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="79dcf-513">Maliyet nesnesi CC004 Ambalajlama, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="79dcf-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="79dcf-514">Ambalajlama hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="79dcf-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79dcf-515">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="79dcf-515">Cost object</span></span></th>
<th><span data-ttu-id="79dcf-516">Ambalajlama hizmetleri (saat)</span><span class="sxs-lookup"><span data-stu-id="79dcf-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79dcf-517">Prod 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-517">Prod 1</span></span></td>
<td><span data-ttu-id="79dcf-518">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-518">Product 1</span></span></td>
<td><span data-ttu-id="79dcf-519">80</span><span class="sxs-lookup"><span data-stu-id="79dcf-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-520">Prod 2</span><span class="sxs-lookup"><span data-stu-id="79dcf-520">Prod 2</span></span></td>
<td><span data-ttu-id="79dcf-521">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="79dcf-521">Product 2</span></span></td>
<td><span data-ttu-id="79dcf-522">15</span><span class="sxs-lookup"><span data-stu-id="79dcf-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="79dcf-523">**Not:** Finance and Operations'ta, bir ürünün tükettiği üretim saatleri gibi istatistiki ölçümler doğrudan kaynak verisinden alınabilir.</span><span class="sxs-lookup"><span data-stu-id="79dcf-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="79dcf-524">İstatistiki ölçüm sağlayıcılar hakkında daha ayrıntılı bilgi için İstatistiki ölçü sağlayıcı şablonuna göz atın.</span><span class="sxs-lookup"><span data-stu-id="79dcf-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="79dcf-525">(Bu konun henüz tamamlanmamış olduğunu ancak yakında tamamlanacağını unutmayın) Aşağıdaki tablo, HR hizmetleri toplam maliyet (sabit ve değişken maliyet) için bir tahsisat tabanı olarak uygulandığında oluşacak sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="79dcf-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79dcf-526">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="79dcf-526">Cost object</span></span></th>
<th><span data-ttu-id="79dcf-527">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="79dcf-527">Magnitude</span></span></th>
<th><span data-ttu-id="79dcf-528">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="79dcf-528">Allocation factor</span></span></th>
<th><span data-ttu-id="79dcf-529">Tutar</span><span class="sxs-lookup"><span data-stu-id="79dcf-529">Amount</span></span></th>
<th><span data-ttu-id="79dcf-530">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="79dcf-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79dcf-531">CC002</span><span class="sxs-lookup"><span data-stu-id="79dcf-531">CC002</span></span></td>
<td><span data-ttu-id="79dcf-532">Finans</span><span class="sxs-lookup"><span data-stu-id="79dcf-532">Finance</span></span></td>
<td><span data-ttu-id="79dcf-533">35</span><span class="sxs-lookup"><span data-stu-id="79dcf-533">35</span></span></td>
<td><span data-ttu-id="79dcf-534">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="79dcf-535">175.00</span><span class="sxs-lookup"><span data-stu-id="79dcf-535">175.00</span></span></td>
<td><span data-ttu-id="79dcf-536">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-537">CC003</span><span class="sxs-lookup"><span data-stu-id="79dcf-537">CC003</span></span></td>
<td><span data-ttu-id="79dcf-538">Montaj</span><span class="sxs-lookup"><span data-stu-id="79dcf-538">Assembly</span></span></td>
<td><span data-ttu-id="79dcf-539">55</span><span class="sxs-lookup"><span data-stu-id="79dcf-539">55</span></span></td>
<td><span data-ttu-id="79dcf-540">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="79dcf-541">275.00</span><span class="sxs-lookup"><span data-stu-id="79dcf-541">275.00</span></span></td>
<td><span data-ttu-id="79dcf-542">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-543">CC004</span><span class="sxs-lookup"><span data-stu-id="79dcf-543">CC004</span></span></td>
<td><span data-ttu-id="79dcf-544">Paketleme</span><span class="sxs-lookup"><span data-stu-id="79dcf-544">Packaging</span></span></td>
<td><span data-ttu-id="79dcf-545">10</span><span class="sxs-lookup"><span data-stu-id="79dcf-545">10</span></span></td>
<td><span data-ttu-id="79dcf-546">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="79dcf-547">50,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-547">50.00</span></span></td>
<td><span data-ttu-id="79dcf-548">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-549">CC002</span><span class="sxs-lookup"><span data-stu-id="79dcf-549">CC002</span></span></td>
<td><span data-ttu-id="79dcf-550">Finans</span><span class="sxs-lookup"><span data-stu-id="79dcf-550">Finance</span></span></td>
<td><span data-ttu-id="79dcf-551">35</span><span class="sxs-lookup"><span data-stu-id="79dcf-551">35</span></span></td>
<td><span data-ttu-id="79dcf-552">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="79dcf-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="79dcf-553">436.00</span><span class="sxs-lookup"><span data-stu-id="79dcf-553">436.00</span></span></td>
<td><span data-ttu-id="79dcf-554">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-555">CC003</span><span class="sxs-lookup"><span data-stu-id="79dcf-555">CC003</span></span></td>
<td><span data-ttu-id="79dcf-556">Montaj</span><span class="sxs-lookup"><span data-stu-id="79dcf-556">Assembly</span></span></td>
<td><span data-ttu-id="79dcf-557">55</span><span class="sxs-lookup"><span data-stu-id="79dcf-557">55</span></span></td>
<td><span data-ttu-id="79dcf-558">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="79dcf-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="79dcf-559">685.14</span><span class="sxs-lookup"><span data-stu-id="79dcf-559">685.14</span></span></td>
<td><span data-ttu-id="79dcf-560">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-561">CC004</span><span class="sxs-lookup"><span data-stu-id="79dcf-561">CC004</span></span></td>
<td><span data-ttu-id="79dcf-562">Paketleme</span><span class="sxs-lookup"><span data-stu-id="79dcf-562">Packaging</span></span></td>
<td><span data-ttu-id="79dcf-563">10</span><span class="sxs-lookup"><span data-stu-id="79dcf-563">10</span></span></td>
<td><span data-ttu-id="79dcf-564">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="79dcf-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="79dcf-565">124.57</span><span class="sxs-lookup"><span data-stu-id="79dcf-565">124.57</span></span></td>
<td><span data-ttu-id="79dcf-566">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="79dcf-567">Aşağıdaki tablo, Finans hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="79dcf-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79dcf-568">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="79dcf-568">Cost object</span></span></th>
<th><span data-ttu-id="79dcf-569">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="79dcf-569">Magnitude</span></span></th>
<th><span data-ttu-id="79dcf-570">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="79dcf-570">Allocation factor</span></span></th>
<th><span data-ttu-id="79dcf-571">Tutar</span><span class="sxs-lookup"><span data-stu-id="79dcf-571">Amount</span></span></th>
<th><span data-ttu-id="79dcf-572">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="79dcf-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79dcf-573">CC003</span><span class="sxs-lookup"><span data-stu-id="79dcf-573">CC003</span></span></td>
<td><span data-ttu-id="79dcf-574">Montaj</span><span class="sxs-lookup"><span data-stu-id="79dcf-574">Assembly</span></span></td>
<td><span data-ttu-id="79dcf-575">65</span><span class="sxs-lookup"><span data-stu-id="79dcf-575">65</span></span></td>
<td><span data-ttu-id="79dcf-576">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="79dcf-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="79dcf-577">438.75</span><span class="sxs-lookup"><span data-stu-id="79dcf-577">438.75</span></span></td>
<td><span data-ttu-id="79dcf-578">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-579">CC004</span><span class="sxs-lookup"><span data-stu-id="79dcf-579">CC004</span></span></td>
<td><span data-ttu-id="79dcf-580">Paketleme</span><span class="sxs-lookup"><span data-stu-id="79dcf-580">Packaging</span></span></td>
<td><span data-ttu-id="79dcf-581">35</span><span class="sxs-lookup"><span data-stu-id="79dcf-581">35</span></span></td>
<td><span data-ttu-id="79dcf-582">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="79dcf-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="79dcf-583">236.25</span><span class="sxs-lookup"><span data-stu-id="79dcf-583">236.25</span></span></td>
<td><span data-ttu-id="79dcf-584">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-585">CC003</span><span class="sxs-lookup"><span data-stu-id="79dcf-585">CC003</span></span></td>
<td><span data-ttu-id="79dcf-586">Montaj</span><span class="sxs-lookup"><span data-stu-id="79dcf-586">Assembly</span></span></td>
<td><span data-ttu-id="79dcf-587">65</span><span class="sxs-lookup"><span data-stu-id="79dcf-587">65</span></span></td>
<td><span data-ttu-id="79dcf-588">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="79dcf-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="79dcf-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="79dcf-589">5,297.69</span></span></td>
<td><span data-ttu-id="79dcf-590">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-591">CC004</span><span class="sxs-lookup"><span data-stu-id="79dcf-591">CC004</span></span></td>
<td><span data-ttu-id="79dcf-592">Paketleme</span><span class="sxs-lookup"><span data-stu-id="79dcf-592">Packaging</span></span></td>
<td><span data-ttu-id="79dcf-593">35</span><span class="sxs-lookup"><span data-stu-id="79dcf-593">35</span></span></td>
<td><span data-ttu-id="79dcf-594">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="79dcf-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="79dcf-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="79dcf-595">2,852.60</span></span></td>
<td><span data-ttu-id="79dcf-596">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="79dcf-597">Aşağıdaki tablo, Derleme hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="79dcf-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79dcf-598">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="79dcf-598">Cost object</span></span></th>
<th><span data-ttu-id="79dcf-599">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="79dcf-599">Magnitude</span></span></th>
<th><span data-ttu-id="79dcf-600">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="79dcf-600">Allocation factor</span></span></th>
<th><span data-ttu-id="79dcf-601">Tutar</span><span class="sxs-lookup"><span data-stu-id="79dcf-601">Amount</span></span></th>
<th><span data-ttu-id="79dcf-602">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="79dcf-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79dcf-603">Prod 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-603">Prod 1</span></span></td>
<td><span data-ttu-id="79dcf-604">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-604">Product 1</span></span></td>
<td><span data-ttu-id="79dcf-605">60</span><span class="sxs-lookup"><span data-stu-id="79dcf-605">60</span></span></td>
<td><span data-ttu-id="79dcf-606">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="79dcf-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="79dcf-607">535.31</span><span class="sxs-lookup"><span data-stu-id="79dcf-607">535.31</span></span></td>
<td><span data-ttu-id="79dcf-608">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-609">Prod 2</span><span class="sxs-lookup"><span data-stu-id="79dcf-609">Prod 2</span></span></td>
<td><span data-ttu-id="79dcf-610">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="79dcf-610">Product 2</span></span></td>
<td><span data-ttu-id="79dcf-611">20</span><span class="sxs-lookup"><span data-stu-id="79dcf-611">20</span></span></td>
<td><span data-ttu-id="79dcf-612">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="79dcf-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="79dcf-613">178.44</span><span class="sxs-lookup"><span data-stu-id="79dcf-613">178.44</span></span></td>
<td><span data-ttu-id="79dcf-614">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-615">Prod 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-615">Prod 1</span></span></td>
<td><span data-ttu-id="79dcf-616">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-616">Product 1</span></span></td>
<td><span data-ttu-id="79dcf-617">60</span><span class="sxs-lookup"><span data-stu-id="79dcf-617">60</span></span></td>
<td><span data-ttu-id="79dcf-618">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="79dcf-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="79dcf-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="79dcf-619">4,487.12</span></span></td>
<td><span data-ttu-id="79dcf-620">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-621">Prod 2</span><span class="sxs-lookup"><span data-stu-id="79dcf-621">Prod 2</span></span></td>
<td><span data-ttu-id="79dcf-622">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="79dcf-622">Product 2</span></span></td>
<td><span data-ttu-id="79dcf-623">20</span><span class="sxs-lookup"><span data-stu-id="79dcf-623">20</span></span></td>
<td><span data-ttu-id="79dcf-624">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="79dcf-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="79dcf-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="79dcf-625">1,495.71</span></span></td>
<td><span data-ttu-id="79dcf-626">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="79dcf-627">Aşağıdaki tablo, Paketleme hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="79dcf-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79dcf-628">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="79dcf-628">Cost object</span></span></th>
<th><span data-ttu-id="79dcf-629">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="79dcf-629">Magnitude</span></span></th>
<th><span data-ttu-id="79dcf-630">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="79dcf-630">Allocation factor</span></span></th>
<th><span data-ttu-id="79dcf-631">Tutar</span><span class="sxs-lookup"><span data-stu-id="79dcf-631">Amount</span></span></th>
<th><span data-ttu-id="79dcf-632">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="79dcf-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79dcf-633">Prod 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-633">Prod 1</span></span></td>
<td><span data-ttu-id="79dcf-634">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-634">Product 1</span></span></td>
<td><span data-ttu-id="79dcf-635">80</span><span class="sxs-lookup"><span data-stu-id="79dcf-635">80</span></span></td>
<td><span data-ttu-id="79dcf-636">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="79dcf-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="79dcf-637">241.05</span><span class="sxs-lookup"><span data-stu-id="79dcf-637">241.05</span></span></td>
<td><span data-ttu-id="79dcf-638">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-639">Prod 2</span><span class="sxs-lookup"><span data-stu-id="79dcf-639">Prod 2</span></span></td>
<td><span data-ttu-id="79dcf-640">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="79dcf-640">Product 2</span></span></td>
<td><span data-ttu-id="79dcf-641">15</span><span class="sxs-lookup"><span data-stu-id="79dcf-641">15</span></span></td>
<td><span data-ttu-id="79dcf-642">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="79dcf-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="79dcf-643">45.20</span><span class="sxs-lookup"><span data-stu-id="79dcf-643">45.20</span></span></td>
<td><span data-ttu-id="79dcf-644">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-645">Prod 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-645">Prod 1</span></span></td>
<td><span data-ttu-id="79dcf-646">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-646">Product 1</span></span></td>
<td><span data-ttu-id="79dcf-647">80</span><span class="sxs-lookup"><span data-stu-id="79dcf-647">80</span></span></td>
<td><span data-ttu-id="79dcf-648">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="79dcf-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="79dcf-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="79dcf-649">2,507.09</span></span></td>
<td><span data-ttu-id="79dcf-650">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-651">Prod 2</span><span class="sxs-lookup"><span data-stu-id="79dcf-651">Prod 2</span></span></td>
<td><span data-ttu-id="79dcf-652">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="79dcf-652">Product 2</span></span></td>
<td><span data-ttu-id="79dcf-653">15</span><span class="sxs-lookup"><span data-stu-id="79dcf-653">15</span></span></td>
<td><span data-ttu-id="79dcf-654">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="79dcf-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="79dcf-655">470.08</span><span class="sxs-lookup"><span data-stu-id="79dcf-655">470.08</span></span></td>
<td><span data-ttu-id="79dcf-656">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="79dcf-657">Günlük girişleri (maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="79dcf-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="79dcf-658">Günlük</span><span class="sxs-lookup"><span data-stu-id="79dcf-658">Journal</span></span></th>
<th><span data-ttu-id="79dcf-659">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="79dcf-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="79dcf-660">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="79dcf-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="79dcf-661">Sürüm</span><span class="sxs-lookup"><span data-stu-id="79dcf-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79dcf-662">00004</span><span class="sxs-lookup"><span data-stu-id="79dcf-662">00004</span></span></td>
<td><span data-ttu-id="79dcf-663">Maliyet tahsisatı günlüğü</span><span class="sxs-lookup"><span data-stu-id="79dcf-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="79dcf-664">Mali</span><span class="sxs-lookup"><span data-stu-id="79dcf-664">Fiscal</span></span></td>
<td><span data-ttu-id="79dcf-665">2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-665">2017</span></span></td>
<td><span data-ttu-id="79dcf-666">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-666">Period 1</span></span></td>
<td><span data-ttu-id="79dcf-667">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="79dcf-668">Günlük satırları</span><span class="sxs-lookup"><span data-stu-id="79dcf-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="79dcf-669">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="79dcf-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="79dcf-670">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="79dcf-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="79dcf-671">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="79dcf-671">Cost element</span></span></th>
<th><span data-ttu-id="79dcf-672">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="79dcf-672">Cost behavior</span></span></th>
<th><span data-ttu-id="79dcf-673">Tutar</span><span class="sxs-lookup"><span data-stu-id="79dcf-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79dcf-674">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="79dcf-675">CC001</span><span class="sxs-lookup"><span data-stu-id="79dcf-675">CC001</span></span></td>
<td><span data-ttu-id="79dcf-676">İK</span><span class="sxs-lookup"><span data-stu-id="79dcf-676">HR</span></span></td>
<td><span data-ttu-id="79dcf-677">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-677">10001</span></span></td>
<td><span data-ttu-id="79dcf-678">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-678">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-679">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-679">Fixed cost</span></span></td>
<td><span data-ttu-id="79dcf-680">500.00</span><span class="sxs-lookup"><span data-stu-id="79dcf-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-681">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="79dcf-682">CC001</span><span class="sxs-lookup"><span data-stu-id="79dcf-682">CC001</span></span></td>
<td><span data-ttu-id="79dcf-683">İK</span><span class="sxs-lookup"><span data-stu-id="79dcf-683">HR</span></span></td>
<td><span data-ttu-id="79dcf-684">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-684">10001</span></span></td>
<td><span data-ttu-id="79dcf-685">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-685">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-686">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-686">Variable cost</span></span></td>
<td><span data-ttu-id="79dcf-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="79dcf-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-688">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="79dcf-689">CC002</span><span class="sxs-lookup"><span data-stu-id="79dcf-689">CC002</span></span></td>
<td><span data-ttu-id="79dcf-690">Finans</span><span class="sxs-lookup"><span data-stu-id="79dcf-690">Finance</span></span></td>
<td><span data-ttu-id="79dcf-691">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-691">10001</span></span></td>
<td><span data-ttu-id="79dcf-692">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-692">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-693">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-693">Fixed cost</span></span></td>
<td><span data-ttu-id="79dcf-694">675.00</span><span class="sxs-lookup"><span data-stu-id="79dcf-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-695">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="79dcf-696">CC002</span><span class="sxs-lookup"><span data-stu-id="79dcf-696">CC002</span></span></td>
<td><span data-ttu-id="79dcf-697">Finans</span><span class="sxs-lookup"><span data-stu-id="79dcf-697">Finance</span></span></td>
<td><span data-ttu-id="79dcf-698">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-698">10001</span></span></td>
<td><span data-ttu-id="79dcf-699">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-699">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-700">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-700">Variable cost</span></span></td>
<td><span data-ttu-id="79dcf-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="79dcf-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-702">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="79dcf-703">CC003</span><span class="sxs-lookup"><span data-stu-id="79dcf-703">CC003</span></span></td>
<td><span data-ttu-id="79dcf-704">Montaj</span><span class="sxs-lookup"><span data-stu-id="79dcf-704">Assembly</span></span></td>
<td><span data-ttu-id="79dcf-705">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-705">10001</span></span></td>
<td><span data-ttu-id="79dcf-706">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-706">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-707">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-707">Fixed cost</span></span></td>
<td><span data-ttu-id="79dcf-708">713.75</span><span class="sxs-lookup"><span data-stu-id="79dcf-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-709">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="79dcf-710">CC003</span><span class="sxs-lookup"><span data-stu-id="79dcf-710">CC003</span></span></td>
<td><span data-ttu-id="79dcf-711">Montaj</span><span class="sxs-lookup"><span data-stu-id="79dcf-711">Assembly</span></span></td>
<td><span data-ttu-id="79dcf-712">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-712">10001</span></span></td>
<td><span data-ttu-id="79dcf-713">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-713">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-714">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-714">Variable cost</span></span></td>
<td><span data-ttu-id="79dcf-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="79dcf-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-716">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="79dcf-717">CC003</span><span class="sxs-lookup"><span data-stu-id="79dcf-717">CC003</span></span></td>
<td><span data-ttu-id="79dcf-718">Paketleme</span><span class="sxs-lookup"><span data-stu-id="79dcf-718">Packaging</span></span></td>
<td><span data-ttu-id="79dcf-719">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-719">10001</span></span></td>
<td><span data-ttu-id="79dcf-720">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-720">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-721">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-721">Fixed cost</span></span></td>
<td><span data-ttu-id="79dcf-722">286.25</span><span class="sxs-lookup"><span data-stu-id="79dcf-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-723">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="79dcf-724">CC003</span><span class="sxs-lookup"><span data-stu-id="79dcf-724">CC003</span></span></td>
<td><span data-ttu-id="79dcf-725">Paketleme</span><span class="sxs-lookup"><span data-stu-id="79dcf-725">Packaging</span></span></td>
<td><span data-ttu-id="79dcf-726">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-726">10001</span></span></td>
<td><span data-ttu-id="79dcf-727">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-727">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-728">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-728">Variable cost</span></span></td>
<td><span data-ttu-id="79dcf-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="79dcf-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-730">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="79dcf-731">Prod 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-731">Prod 1</span></span></td>
<td><span data-ttu-id="79dcf-732">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-732">Product 1</span></span></td>
<td><span data-ttu-id="79dcf-733">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-733">10001</span></span></td>
<td><span data-ttu-id="79dcf-734">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-734">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-735">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-735">Fixed cost</span></span></td>
<td><span data-ttu-id="79dcf-736">776.36</span><span class="sxs-lookup"><span data-stu-id="79dcf-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-737">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="79dcf-738">Prod 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-738">Prod 1</span></span></td>
<td><span data-ttu-id="79dcf-739">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-739">Product 1</span></span></td>
<td><span data-ttu-id="79dcf-740">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-740">10001</span></span></td>
<td><span data-ttu-id="79dcf-741">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-741">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-742">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-742">Variable cost</span></span></td>
<td><span data-ttu-id="79dcf-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="79dcf-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-744">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="79dcf-745">Prod 2</span><span class="sxs-lookup"><span data-stu-id="79dcf-745">Prod 2</span></span></td>
<td><span data-ttu-id="79dcf-746">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-746">Product 1</span></span></td>
<td><span data-ttu-id="79dcf-747">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-747">10001</span></span></td>
<td><span data-ttu-id="79dcf-748">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-748">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-749">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-749">Fixed cost</span></span></td>
<td><span data-ttu-id="79dcf-750">223.64</span><span class="sxs-lookup"><span data-stu-id="79dcf-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-751">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="79dcf-752">Prod 2</span><span class="sxs-lookup"><span data-stu-id="79dcf-752">Prod 2</span></span></td>
<td><span data-ttu-id="79dcf-753">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-753">Product 1</span></span></td>
<td><span data-ttu-id="79dcf-754">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-754">10001</span></span></td>
<td><span data-ttu-id="79dcf-755">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-755">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-756">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-756">Variable cost</span></span></td>
<td><span data-ttu-id="79dcf-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="79dcf-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="79dcf-758">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="79dcf-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="79dcf-759">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="79dcf-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="79dcf-760">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="79dcf-760">Cost element</span></span></th>
<th><span data-ttu-id="79dcf-761">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="79dcf-761">Cost behavior</span></span></th>
<th><span data-ttu-id="79dcf-762">Tutar</span><span class="sxs-lookup"><span data-stu-id="79dcf-762">Amount</span></span></th>
<th><span data-ttu-id="79dcf-763">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="79dcf-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="79dcf-764">CC001</span><span class="sxs-lookup"><span data-stu-id="79dcf-764">CC001</span></span></td>
<td><span data-ttu-id="79dcf-765">İK</span><span class="sxs-lookup"><span data-stu-id="79dcf-765">HR</span></span></td>
<td><span data-ttu-id="79dcf-766">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-766">10001</span></span></td>
<td><span data-ttu-id="79dcf-767">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-767">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-768">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-768">Fixed cost</span></span></td>
<td><span data-ttu-id="79dcf-769">-500.00</span><span class="sxs-lookup"><span data-stu-id="79dcf-769">-500.00</span></span></td>
<td><span data-ttu-id="79dcf-770">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-771">CC002</span><span class="sxs-lookup"><span data-stu-id="79dcf-771">CC002</span></span></td>
<td><span data-ttu-id="79dcf-772">Finans</span><span class="sxs-lookup"><span data-stu-id="79dcf-772">Finance</span></span></td>
<td><span data-ttu-id="79dcf-773">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-773">10001</span></span></td>
<td><span data-ttu-id="79dcf-774">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-774">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-775">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-775">Fixed cost</span></span></td>
<td><span data-ttu-id="79dcf-776">175.00</span><span class="sxs-lookup"><span data-stu-id="79dcf-776">175.00</span></span></td>
<td><span data-ttu-id="79dcf-777">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-778">CC003</span><span class="sxs-lookup"><span data-stu-id="79dcf-778">CC003</span></span></td>
<td><span data-ttu-id="79dcf-779">Montaj</span><span class="sxs-lookup"><span data-stu-id="79dcf-779">Assembly</span></span></td>
<td><span data-ttu-id="79dcf-780">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-780">10001</span></span></td>
<td><span data-ttu-id="79dcf-781">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-781">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-782">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-782">Fixed cost</span></span></td>
<td><span data-ttu-id="79dcf-783">275.00</span><span class="sxs-lookup"><span data-stu-id="79dcf-783">275.00</span></span></td>
<td><span data-ttu-id="79dcf-784">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-785">CC004</span><span class="sxs-lookup"><span data-stu-id="79dcf-785">CC004</span></span></td>
<td><span data-ttu-id="79dcf-786">Paketleme</span><span class="sxs-lookup"><span data-stu-id="79dcf-786">Packaging</span></span></td>
<td><span data-ttu-id="79dcf-787">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-787">10001</span></span></td>
<td><span data-ttu-id="79dcf-788">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-788">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-789">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-789">Fixed cost</span></span></td>
<td><span data-ttu-id="79dcf-790">50,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-790">50,00</span></span></td>
<td><span data-ttu-id="79dcf-791">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-792">CC001</span><span class="sxs-lookup"><span data-stu-id="79dcf-792">CC001</span></span></td>
<td><span data-ttu-id="79dcf-793">İK</span><span class="sxs-lookup"><span data-stu-id="79dcf-793">HR</span></span></td>
<td><span data-ttu-id="79dcf-794">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-794">10001</span></span></td>
<td><span data-ttu-id="79dcf-795">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-795">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-796">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-796">Variable cost</span></span></td>
<td><span data-ttu-id="79dcf-797">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="79dcf-797">-1,245.71</span></span></td>
<td><span data-ttu-id="79dcf-798">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-799">CC002</span><span class="sxs-lookup"><span data-stu-id="79dcf-799">CC002</span></span></td>
<td><span data-ttu-id="79dcf-800">Finans</span><span class="sxs-lookup"><span data-stu-id="79dcf-800">Finance</span></span></td>
<td><span data-ttu-id="79dcf-801">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-801">10001</span></span></td>
<td><span data-ttu-id="79dcf-802">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-802">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-803">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-803">Variable cost</span></span></td>
<td><span data-ttu-id="79dcf-804">436.00</span><span class="sxs-lookup"><span data-stu-id="79dcf-804">436.00</span></span></td>
<td><span data-ttu-id="79dcf-805">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-806">CC003</span><span class="sxs-lookup"><span data-stu-id="79dcf-806">CC003</span></span></td>
<td><span data-ttu-id="79dcf-807">Montaj</span><span class="sxs-lookup"><span data-stu-id="79dcf-807">Assembly</span></span></td>
<td><span data-ttu-id="79dcf-808">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-808">10001</span></span></td>
<td><span data-ttu-id="79dcf-809">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-809">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-810">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-810">Variable cost</span></span></td>
<td><span data-ttu-id="79dcf-811">685.14</span><span class="sxs-lookup"><span data-stu-id="79dcf-811">685.14</span></span></td>
<td><span data-ttu-id="79dcf-812">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-813">CC004</span><span class="sxs-lookup"><span data-stu-id="79dcf-813">CC004</span></span></td>
<td><span data-ttu-id="79dcf-814">Paketleme</span><span class="sxs-lookup"><span data-stu-id="79dcf-814">Packaging</span></span></td>
<td><span data-ttu-id="79dcf-815">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-815">10001</span></span></td>
<td><span data-ttu-id="79dcf-816">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-816">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-817">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-817">Variable cost</span></span></td>
<td><span data-ttu-id="79dcf-818">124.57</span><span class="sxs-lookup"><span data-stu-id="79dcf-818">124.57</span></span></td>
<td><span data-ttu-id="79dcf-819">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-820">CC002</span><span class="sxs-lookup"><span data-stu-id="79dcf-820">CC002</span></span></td>
<td><span data-ttu-id="79dcf-821">Finans</span><span class="sxs-lookup"><span data-stu-id="79dcf-821">Finance</span></span></td>
<td><span data-ttu-id="79dcf-822">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-822">10001</span></span></td>
<td><span data-ttu-id="79dcf-823">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-823">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-824">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-824">Fixed cost</span></span></td>
<td><span data-ttu-id="79dcf-825">-675,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-825">-675.00</span></span></td>
<td><span data-ttu-id="79dcf-826">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-827">CC003</span><span class="sxs-lookup"><span data-stu-id="79dcf-827">CC003</span></span></td>
<td><span data-ttu-id="79dcf-828">Montaj</span><span class="sxs-lookup"><span data-stu-id="79dcf-828">Assembly</span></span></td>
<td><span data-ttu-id="79dcf-829">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-829">10001</span></span></td>
<td><span data-ttu-id="79dcf-830">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-830">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-831">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-831">Fixed cost</span></span></td>
<td><span data-ttu-id="79dcf-832">438.75</span><span class="sxs-lookup"><span data-stu-id="79dcf-832">438.75</span></span></td>
<td><span data-ttu-id="79dcf-833">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-834">CC004</span><span class="sxs-lookup"><span data-stu-id="79dcf-834">CC004</span></span></td>
<td><span data-ttu-id="79dcf-835">Paketleme</span><span class="sxs-lookup"><span data-stu-id="79dcf-835">Packaging</span></span></td>
<td><span data-ttu-id="79dcf-836">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-836">10001</span></span></td>
<td><span data-ttu-id="79dcf-837">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-837">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-838">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-838">Fixed cost</span></span></td>
<td><span data-ttu-id="79dcf-839">236.25</span><span class="sxs-lookup"><span data-stu-id="79dcf-839">236.25</span></span></td>
<td><span data-ttu-id="79dcf-840">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-841">CC002</span><span class="sxs-lookup"><span data-stu-id="79dcf-841">CC002</span></span></td>
<td><span data-ttu-id="79dcf-842">Finans</span><span class="sxs-lookup"><span data-stu-id="79dcf-842">Finance</span></span></td>
<td><span data-ttu-id="79dcf-843">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-843">10001</span></span></td>
<td><span data-ttu-id="79dcf-844">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-844">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-845">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-845">Variable cost</span></span></td>
<td><span data-ttu-id="79dcf-846">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="79dcf-846">-8,150.29</span></span></td>
<td><span data-ttu-id="79dcf-847">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-848">CC003</span><span class="sxs-lookup"><span data-stu-id="79dcf-848">CC003</span></span></td>
<td><span data-ttu-id="79dcf-849">Montaj</span><span class="sxs-lookup"><span data-stu-id="79dcf-849">Assembly</span></span></td>
<td><span data-ttu-id="79dcf-850">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-850">10001</span></span></td>
<td><span data-ttu-id="79dcf-851">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-851">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-852">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-852">Variable cost</span></span></td>
<td><span data-ttu-id="79dcf-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="79dcf-853">5,297.69</span></span></td>
<td><span data-ttu-id="79dcf-854">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-855">CC004</span><span class="sxs-lookup"><span data-stu-id="79dcf-855">CC004</span></span></td>
<td><span data-ttu-id="79dcf-856">Paketleme</span><span class="sxs-lookup"><span data-stu-id="79dcf-856">Packaging</span></span></td>
<td><span data-ttu-id="79dcf-857">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-857">10001</span></span></td>
<td><span data-ttu-id="79dcf-858">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-858">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-859">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-859">Variable cost</span></span></td>
<td><span data-ttu-id="79dcf-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="79dcf-860">2,852.60</span></span></td>
<td><span data-ttu-id="79dcf-861">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-862">CC003</span><span class="sxs-lookup"><span data-stu-id="79dcf-862">CC003</span></span></td>
<td><span data-ttu-id="79dcf-863">Montaj</span><span class="sxs-lookup"><span data-stu-id="79dcf-863">Assembly</span></span></td>
<td><span data-ttu-id="79dcf-864">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-864">10001</span></span></td>
<td><span data-ttu-id="79dcf-865">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-865">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-866">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-866">Fixed cost</span></span></td>
<td><span data-ttu-id="79dcf-867">-713.75</span><span class="sxs-lookup"><span data-stu-id="79dcf-867">-713.75</span></span></td>
<td><span data-ttu-id="79dcf-868">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-869">Prod 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-869">Prod 1</span></span></td>
<td><span data-ttu-id="79dcf-870">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-870">Product 1</span></span></td>
<td><span data-ttu-id="79dcf-871">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-871">10001</span></span></td>
<td><span data-ttu-id="79dcf-872">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-872">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-873">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-873">Fixed cost</span></span></td>
<td><span data-ttu-id="79dcf-874">535.31</span><span class="sxs-lookup"><span data-stu-id="79dcf-874">535.31</span></span></td>
<td><span data-ttu-id="79dcf-875">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-876">Prod 2</span><span class="sxs-lookup"><span data-stu-id="79dcf-876">Prod 2</span></span></td>
<td><span data-ttu-id="79dcf-877">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="79dcf-877">Product 2</span></span></td>
<td><span data-ttu-id="79dcf-878">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-878">10001</span></span></td>
<td><span data-ttu-id="79dcf-879">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-879">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-880">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-880">Fixed cost</span></span></td>
<td><span data-ttu-id="79dcf-881">178.44</span><span class="sxs-lookup"><span data-stu-id="79dcf-881">178.44</span></span></td>
<td><span data-ttu-id="79dcf-882">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-883">CC003</span><span class="sxs-lookup"><span data-stu-id="79dcf-883">CC003</span></span></td>
<td><span data-ttu-id="79dcf-884">Montaj</span><span class="sxs-lookup"><span data-stu-id="79dcf-884">Assembly</span></span></td>
<td><span data-ttu-id="79dcf-885">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-885">10001</span></span></td>
<td><span data-ttu-id="79dcf-886">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-886">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-887">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-887">Variable cost</span></span></td>
<td><span data-ttu-id="79dcf-888">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="79dcf-888">-5,982.83</span></span></td>
<td><span data-ttu-id="79dcf-889">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-890">Prod 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-890">Prod 1</span></span></td>
<td><span data-ttu-id="79dcf-891">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-891">Product 1</span></span></td>
<td><span data-ttu-id="79dcf-892">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-892">10001</span></span></td>
<td><span data-ttu-id="79dcf-893">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-893">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-894">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-894">Variable cost</span></span></td>
<td><span data-ttu-id="79dcf-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="79dcf-895">4,487.12</span></span></td>
<td><span data-ttu-id="79dcf-896">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-897">Prod 2</span><span class="sxs-lookup"><span data-stu-id="79dcf-897">Prod 2</span></span></td>
<td><span data-ttu-id="79dcf-898">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="79dcf-898">Product 2</span></span></td>
<td><span data-ttu-id="79dcf-899">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-899">10001</span></span></td>
<td><span data-ttu-id="79dcf-900">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-900">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-901">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-901">Variable cost</span></span></td>
<td><span data-ttu-id="79dcf-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="79dcf-902">1,495.71</span></span></td>
<td><span data-ttu-id="79dcf-903">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-904">CC003</span><span class="sxs-lookup"><span data-stu-id="79dcf-904">CC003</span></span></td>
<td><span data-ttu-id="79dcf-905">Montaj</span><span class="sxs-lookup"><span data-stu-id="79dcf-905">Assembly</span></span></td>
<td><span data-ttu-id="79dcf-906">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-906">10001</span></span></td>
<td><span data-ttu-id="79dcf-907">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-907">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-908">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-908">Fixed cost</span></span></td>
<td><span data-ttu-id="79dcf-909">-286,25</span><span class="sxs-lookup"><span data-stu-id="79dcf-909">-286.25</span></span></td>
<td><span data-ttu-id="79dcf-910">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-911">Prod 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-911">Prod 1</span></span></td>
<td><span data-ttu-id="79dcf-912">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-912">Product 1</span></span></td>
<td><span data-ttu-id="79dcf-913">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-913">10001</span></span></td>
<td><span data-ttu-id="79dcf-914">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-914">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-915">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-915">Fixed cost</span></span></td>
<td><span data-ttu-id="79dcf-916">241.05</span><span class="sxs-lookup"><span data-stu-id="79dcf-916">241.05</span></span></td>
<td><span data-ttu-id="79dcf-917">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-918">Prod 2</span><span class="sxs-lookup"><span data-stu-id="79dcf-918">Prod 2</span></span></td>
<td><span data-ttu-id="79dcf-919">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="79dcf-919">Product 2</span></span></td>
<td><span data-ttu-id="79dcf-920">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-920">10001</span></span></td>
<td><span data-ttu-id="79dcf-921">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-921">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-922">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-922">Fixed cost</span></span></td>
<td><span data-ttu-id="79dcf-923">45.20</span><span class="sxs-lookup"><span data-stu-id="79dcf-923">45.20</span></span></td>
<td><span data-ttu-id="79dcf-924">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-925">CC003</span><span class="sxs-lookup"><span data-stu-id="79dcf-925">CC003</span></span></td>
<td><span data-ttu-id="79dcf-926">Montaj</span><span class="sxs-lookup"><span data-stu-id="79dcf-926">Assembly</span></span></td>
<td><span data-ttu-id="79dcf-927">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-927">10001</span></span></td>
<td><span data-ttu-id="79dcf-928">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-928">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-929">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-929">Variable cost</span></span></td>
<td><span data-ttu-id="79dcf-930">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="79dcf-930">-2,977.17</span></span></td>
<td><span data-ttu-id="79dcf-931">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-932">Prod 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-932">Prod 1</span></span></td>
<td><span data-ttu-id="79dcf-933">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-933">Product 1</span></span></td>
<td><span data-ttu-id="79dcf-934">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-934">10001</span></span></td>
<td><span data-ttu-id="79dcf-935">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-935">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-936">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-936">Variable cost</span></span></td>
<td><span data-ttu-id="79dcf-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="79dcf-937">2,507.09</span></span></td>
<td><span data-ttu-id="79dcf-938">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="79dcf-939">Prod 2</span><span class="sxs-lookup"><span data-stu-id="79dcf-939">Prod 2</span></span></td>
<td><span data-ttu-id="79dcf-940">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="79dcf-940">Product 2</span></span></td>
<td><span data-ttu-id="79dcf-941">10001</span><span class="sxs-lookup"><span data-stu-id="79dcf-941">10001</span></span></td>
<td><span data-ttu-id="79dcf-942">Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-942">Electricity</span></span></td>
<td><span data-ttu-id="79dcf-943">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-943">Variable cost</span></span></td>
<td><span data-ttu-id="79dcf-944">470.08</span><span class="sxs-lookup"><span data-stu-id="79dcf-944">470.08</span></span></td>
<td><span data-ttu-id="79dcf-945">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="79dcf-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="79dcf-946">Sonuç</span><span class="sxs-lookup"><span data-stu-id="79dcf-946">Conclusion</span></span>
<span data-ttu-id="79dcf-947">Mali muhasebede, Elektrik için 10.000,00 maliyet bir sözde maliyet merkezi kimliğine nakledilmiştir.</span><span class="sxs-lookup"><span data-stu-id="79dcf-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="79dcf-948">Bu nedenle, maliyet muhasebecileri bu maliyetin tahsis edilmesi gerektiğini bilirler.</span><span class="sxs-lookup"><span data-stu-id="79dcf-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="79dcf-949">Maliyet muhasebesinde, maliyetler kuruluş birimleri ve seviyeleri arasında, uygulanan kural ve ilkelere dayalı olarak akar.</span><span class="sxs-lookup"><span data-stu-id="79dcf-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="79dcf-950">Her maliyet, maliyetlerin tahsisatı için en iyi değerlendirmeyi sağlayan bir tahsisat tabanı ile ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="79dcf-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="79dcf-951">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="79dcf-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="79dcf-952">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="79dcf-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="79dcf-953">Toplam</span><span class="sxs-lookup"><span data-stu-id="79dcf-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="79dcf-954">CC099</span><span class="sxs-lookup"><span data-stu-id="79dcf-954">CC099</span></span></th>
<th><span data-ttu-id="79dcf-955">CC001</span><span class="sxs-lookup"><span data-stu-id="79dcf-955">CC001</span></span></th>
<th><span data-ttu-id="79dcf-956">CC002</span><span class="sxs-lookup"><span data-stu-id="79dcf-956">CC002</span></span></th>
<th><span data-ttu-id="79dcf-957">CC003</span><span class="sxs-lookup"><span data-stu-id="79dcf-957">CC003</span></span></th>
<th><span data-ttu-id="79dcf-958">CC004</span><span class="sxs-lookup"><span data-stu-id="79dcf-958">CC004</span></span></th>
<th><span data-ttu-id="79dcf-959">Proj 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-959">Proj 1</span></span></th>
<th><span data-ttu-id="79dcf-960">Proj 2</span><span class="sxs-lookup"><span data-stu-id="79dcf-960">Proj 2</span></span></th>
<th><span data-ttu-id="79dcf-961">Prod 1</span><span class="sxs-lookup"><span data-stu-id="79dcf-961">Prod 1</span></span></th>
<th><span data-ttu-id="79dcf-962">Prod 2</span><span class="sxs-lookup"><span data-stu-id="79dcf-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="79dcf-963">10001 Elektrik</span><span class="sxs-lookup"><span data-stu-id="79dcf-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79dcf-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="79dcf-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="79dcf-965"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="79dcf-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="79dcf-966"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="79dcf-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="79dcf-967"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="79dcf-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="79dcf-968"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="79dcf-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="79dcf-969"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="79dcf-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="79dcf-970"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="79dcf-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="79dcf-971"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="79dcf-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="79dcf-972"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="79dcf-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="79dcf-973">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="79dcf-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79dcf-974">0,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="79dcf-975">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79dcf-976">0,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79dcf-977">0,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79dcf-978">0,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79dcf-979">0,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79dcf-980">0,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="79dcf-981">776.36</span><span class="sxs-lookup"><span data-stu-id="79dcf-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79dcf-982">223.64</span><span class="sxs-lookup"><span data-stu-id="79dcf-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79dcf-983"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="79dcf-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="79dcf-984">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="79dcf-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79dcf-985">000</span><span class="sxs-lookup"><span data-stu-id="79dcf-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79dcf-986">0,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79dcf-987">0,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79dcf-988">0,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79dcf-989">0,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79dcf-990">30.00</span><span class="sxs-lookup"><span data-stu-id="79dcf-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79dcf-991">10,00</span><span class="sxs-lookup"><span data-stu-id="79dcf-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79dcf-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="79dcf-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79dcf-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="79dcf-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="79dcf-994"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="79dcf-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="79dcf-995">Bu konu, birincil maliyet öğesi, 10001 Elektrik'in maliyet nesneleri arasında nasıl aktığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="79dcf-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="79dcf-996">Bu nedenle, bu genel gider maliyeti kuruluşun en düşük seviyesine tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="79dcf-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="79dcf-997">Başka bir deyişle, maliyet en alt düzeydeki maliyet nesnelerine aittir.</span><span class="sxs-lookup"><span data-stu-id="79dcf-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="79dcf-998">Maliyetin, maliyet nesneleri arasında görsel bir akışına ihtiyacınız varsa, maliyetin akışını görselleştirmek için maliyet toplamı ilke kurallarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79dcf-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="79dcf-999">Daha ayrıntılı bilgi için, Maliyet toplam ilkesine bakınız.</span><span class="sxs-lookup"><span data-stu-id="79dcf-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="79dcf-1000">(Bu konunun henüz tamamlanmadığını ancak yakında tamamlanacağını göz önünde bulundurun.)</span><span class="sxs-lookup"><span data-stu-id="79dcf-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




