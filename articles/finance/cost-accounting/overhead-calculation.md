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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 6c045f82f3288dba193721dd80c90e68750af9a7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180354"
---
# <a name="overhead-calculation"></a><span data-ttu-id="ce348-103">Genel gider hesaplaması</span><span class="sxs-lookup"><span data-stu-id="ce348-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce348-104">Bu konu, genel gider maliyetlerinin hesaplanması için tipik işlemleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="ce348-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="ce348-105">Terim tanımı</span><span class="sxs-lookup"><span data-stu-id="ce348-105">Term definition</span></span>
---------------

<span data-ttu-id="ce348-106">Genel gider maliyetleri bir işletmenin çalışması için normalde uygulanan, ancak doğrudan herhangi bir özel iş, faaliyet, ürün veya hizmete ilişkilendirilmemiş olan maliyetlerdir.</span><span class="sxs-lookup"><span data-stu-id="ce348-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="ce348-107">Genel gider maliyetleri kar sağlama faaliyetlerinin oluşturulması için kritik destek sağlar.</span><span class="sxs-lookup"><span data-stu-id="ce348-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="ce348-108">Aşağıda bazı genel gider örnekleri verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="ce348-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="ce348-109">Kira</span><span class="sxs-lookup"><span data-stu-id="ce348-109">Rent</span></span>
-   <span data-ttu-id="ce348-110">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-110">Electricity</span></span>
-   <span data-ttu-id="ce348-111">Yönetim maaşları</span><span class="sxs-lookup"><span data-stu-id="ce348-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="ce348-112">Genel gider hesaplaması genel bakış</span><span class="sxs-lookup"><span data-stu-id="ce348-112">Overhead calculation overview</span></span>
<span data-ttu-id="ce348-113">Genel gider hesaplama, maliyet muhasebesi ilkelerini doğru sırayla çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="ce348-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="ce348-114">Maliyet muhasebesi ilkeleri değiştiyse veya belirli hatalar algılandıysa, genel gider hesaplamasını aynı mali dönem için birden fazla kez yürütebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ce348-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="ce348-115">Her genel gider hesaplaması depolanır ve önceki sürümlerdeki hesaplamaları kıyaslamanıza olanak sağlayan, benzersiz bir sürüm kimliğine sahip olur.</span><span class="sxs-lookup"><span data-stu-id="ce348-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="ce348-116">Genel gider hesaplamasının oluşturduğu maliyet girişleri bir muhasebe tarihi alır.</span><span class="sxs-lookup"><span data-stu-id="ce348-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="ce348-117">Bu muhasebe tarihi, hesaplamada kullanılan mali dönemin bitiş tarihiyle eşleşir.</span><span class="sxs-lookup"><span data-stu-id="ce348-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="ce348-118">Benzersiz sürüm kimliği aşağıdaki öğelerden oluşur:</span><span class="sxs-lookup"><span data-stu-id="ce348-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="ce348-119">Sürüm türü</span><span class="sxs-lookup"><span data-stu-id="ce348-119">Version type</span></span>
-   <span data-ttu-id="ce348-120">Tarih ve saat</span><span class="sxs-lookup"><span data-stu-id="ce348-120">Date and time</span></span>
-   <span data-ttu-id="ce348-121">Maliyet muhasebesi defteri</span><span class="sxs-lookup"><span data-stu-id="ce348-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="ce348-122">Mali yıl</span><span class="sxs-lookup"><span data-stu-id="ce348-122">Fiscal year</span></span>
-   <span data-ttu-id="ce348-123">Mali dönem</span><span class="sxs-lookup"><span data-stu-id="ce348-123">Fiscal period</span></span>

<span data-ttu-id="ce348-124">Genel gider hesaplama, sürümden bağımsız olarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="ce348-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="ce348-125">Bu nedenle, Gerçek sürümden önce Bütçe sürümünü hesaplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ce348-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="ce348-126">Genel gider hesaplama dört adımdan oluşur, aşağıdaki çizimde gösterildiği gibi.</span><span class="sxs-lookup"><span data-stu-id="ce348-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="ce348-127">Her adımda, günlük girişleri olan bir günlük başlığı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ce348-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="ce348-128">Bu günlük başlığı, her hesaplama adımı için giriş verilerini tutar.</span><span class="sxs-lookup"><span data-stu-id="ce348-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="ce348-129">İlkeler ve kurallar her günlük satırına uygulanır ve maliyet girişleri çıkış olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ce348-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="ce348-130">Bu nedenle, her zaman tam izlenebilirliğe sahip olursunuz.</span><span class="sxs-lookup"><span data-stu-id="ce348-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="ce348-131">[![Genel gider hesaplaması](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="ce348-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="ce348-132">Elektrik genel gideri maliyetini hesapla ve tahsis et</span><span class="sxs-lookup"><span data-stu-id="ce348-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="ce348-133">Mali muhasebede, elektrik gibi bazı maliyetler peşin ödeme olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="ce348-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="ce348-134">Bu nedenle, Maliyet muhasebesi için ayrıntılı yönetim bilgiler sağlanmaz.</span><span class="sxs-lookup"><span data-stu-id="ce348-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="ce348-135">Maliyet muhasebesinde doğru yönetimsel bilgileri tüm yönetim birim ve düzeylerinde sağlamak için, maliyetlerin kuruluş birimleri arasında akması gerekir.</span><span class="sxs-lookup"><span data-stu-id="ce348-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="ce348-136">Bu akış, tüketimin doğru bir kaydına ya da adil bir değerlendirmeye dayanıyor olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ce348-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="ce348-137">Genel muhasebede, bir elektrik maliyeti aşağıdaki tabloda gösterildiği gibi deftere nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="ce348-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ce348-138">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="ce348-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ce348-139">Maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="ce348-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="ce348-140">Ana hesap</span><span class="sxs-lookup"><span data-stu-id="ce348-140">Main account</span></span></th>
<th><span data-ttu-id="ce348-141">Muhasebe para birimi cinsinden tutar</span><span class="sxs-lookup"><span data-stu-id="ce348-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ce348-142">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="ce348-143">CC099</span><span class="sxs-lookup"><span data-stu-id="ce348-143">CC099</span></span></td>
<td><span data-ttu-id="ce348-144">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="ce348-144">Default cost center</span></span></td>
<td><span data-ttu-id="ce348-145">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-145">10001</span></span></td>
<td><span data-ttu-id="ce348-146">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-146">Electricity</span></span></td>
<td><span data-ttu-id="ce348-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="ce348-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="ce348-148">Adım 1: Maliyet davranışı hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="ce348-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="ce348-149">Varsayılan olarak, maliyeti girişleri kaynak veriden içeri alındığında, Maliyet muhasebesinde **Sınıflandırılmamış** maliyet davranışı sınıflandırmasını alırlar.</span><span class="sxs-lookup"><span data-stu-id="ce348-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="ce348-150">Maliyet davranışı ilke kuralları ekleyerek, maliyet girişlerini **Sabit maliyet** veya **Değişken maliyet** olarak yeniden sınıflandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ce348-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="ce348-151">Maliyet davranış kuralını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="ce348-151">Define the cost behavior rule</span></span>

<span data-ttu-id="ce348-152">Bazı durumlarda, sabit bir ücret maliyet parçasıdır ve kalan maliyet, tüketime dayanır.</span><span class="sxs-lookup"><span data-stu-id="ce348-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="ce348-153">Elektrik faturaları genellikle bu tanıma uyar.</span><span class="sxs-lookup"><span data-stu-id="ce348-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="ce348-154">Belirli bir sabit ücret ödedikten sonra, kilovat saatlik (Kwh) tüketim başına ödeme yaparsınız.</span><span class="sxs-lookup"><span data-stu-id="ce348-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="ce348-155">Örneğin, sabit maliyet masrafı 1.000,00 ise, maliyet davranışı kural nasıl tanımlanır:</span><span class="sxs-lookup"><span data-stu-id="ce348-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="ce348-156">Sabit tutar 1.000,00</span><span class="sxs-lookup"><span data-stu-id="ce348-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="ce348-157">0 &lt;= 1.000,00 = Sabit</span><span class="sxs-lookup"><span data-stu-id="ce348-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="ce348-158">1000,01 &lt; N = Değişken</span><span class="sxs-lookup"><span data-stu-id="ce348-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="ce348-159">Günlük</span><span class="sxs-lookup"><span data-stu-id="ce348-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ce348-160">Günlük</span><span class="sxs-lookup"><span data-stu-id="ce348-160">Journal</span></span></th>
<th><span data-ttu-id="ce348-161">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="ce348-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="ce348-162">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="ce348-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="ce348-163">Sürüm</span><span class="sxs-lookup"><span data-stu-id="ce348-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ce348-164">00001</span><span class="sxs-lookup"><span data-stu-id="ce348-164">00001</span></span></td>
<td><span data-ttu-id="ce348-165">Maliyet davranışı hesaplama günlüğü</span><span class="sxs-lookup"><span data-stu-id="ce348-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="ce348-166">Mali</span><span class="sxs-lookup"><span data-stu-id="ce348-166">Fiscal</span></span></td>
<td><span data-ttu-id="ce348-167">2017</span><span class="sxs-lookup"><span data-stu-id="ce348-167">2017</span></span></td>
<td><span data-ttu-id="ce348-168">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="ce348-168">Period 1</span></span></td>
<td><span data-ttu-id="ce348-169">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="ce348-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="ce348-170">Günlük girişleri (Maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="ce348-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ce348-171">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="ce348-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ce348-172">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="ce348-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ce348-173">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="ce348-173">Cost element</span></span></th>
<th><span data-ttu-id="ce348-174">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="ce348-174">Cost behavior</span></span></th>
<th><span data-ttu-id="ce348-175">Tutar</span><span class="sxs-lookup"><span data-stu-id="ce348-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ce348-176">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="ce348-177">CC099</span><span class="sxs-lookup"><span data-stu-id="ce348-177">CC099</span></span></td>
<td><span data-ttu-id="ce348-178">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="ce348-178">Default cost center</span></span></td>
<td><span data-ttu-id="ce348-179">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-179">10001</span></span></td>
<td><span data-ttu-id="ce348-180">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-180">Electricity</span></span></td>
<td><span data-ttu-id="ce348-181">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="ce348-181">Unclassified</span></span></td>
<td><span data-ttu-id="ce348-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="ce348-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="ce348-183">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="ce348-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ce348-184">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="ce348-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ce348-185">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="ce348-185">Cost element</span></span></th>
<th><span data-ttu-id="ce348-186">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="ce348-186">Cost behavior</span></span></th>
<th><span data-ttu-id="ce348-187">Tutar</span><span class="sxs-lookup"><span data-stu-id="ce348-187">Amount</span></span></th>
<th><span data-ttu-id="ce348-188">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="ce348-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ce348-189">CC099</span><span class="sxs-lookup"><span data-stu-id="ce348-189">CC099</span></span></td>
<td><span data-ttu-id="ce348-190">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="ce348-190">Default cost center</span></span></td>
<td><span data-ttu-id="ce348-191">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-191">10001</span></span></td>
<td><span data-ttu-id="ce348-192">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-192">Electricity</span></span></td>
<td><span data-ttu-id="ce348-193">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="ce348-193">Unclassified</span></span></td>
<td><span data-ttu-id="ce348-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="ce348-194">10,000.00</span></span></td>
<td><span data-ttu-id="ce348-195">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-196">CC099</span><span class="sxs-lookup"><span data-stu-id="ce348-196">CC099</span></span></td>
<td><span data-ttu-id="ce348-197">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="ce348-197">Default cost center</span></span></td>
<td><span data-ttu-id="ce348-198">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-198">10001</span></span></td>
<td><span data-ttu-id="ce348-199">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-199">Electricity</span></span></td>
<td><span data-ttu-id="ce348-200">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="ce348-200">Unclassified</span></span></td>
<td><span data-ttu-id="ce348-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="ce348-201">-10,000.00</span></span></td>
<td><span data-ttu-id="ce348-202">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-203">CC099</span><span class="sxs-lookup"><span data-stu-id="ce348-203">CC099</span></span></td>
<td><span data-ttu-id="ce348-204">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="ce348-204">Default cost center</span></span></td>
<td><span data-ttu-id="ce348-205">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-205">10001</span></span></td>
<td><span data-ttu-id="ce348-206">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-206">Electricity</span></span></td>
<td><span data-ttu-id="ce348-207">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-207">Fixed cost</span></span></td>
<td><span data-ttu-id="ce348-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="ce348-208">1,000.00</span></span></td>
<td><span data-ttu-id="ce348-209">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-210">CC099</span><span class="sxs-lookup"><span data-stu-id="ce348-210">CC099</span></span></td>
<td><span data-ttu-id="ce348-211">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="ce348-211">Default cost center</span></span></td>
<td><span data-ttu-id="ce348-212">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-212">10001</span></span></td>
<td><span data-ttu-id="ce348-213">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-213">Electricity</span></span></td>
<td><span data-ttu-id="ce348-214">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-214">Variable cost</span></span></td>
<td><span data-ttu-id="ce348-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="ce348-215">9,000.00</span></span></td>
<td><span data-ttu-id="ce348-216">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ce348-217">Daha fazla bilgi için bkz. [Maliyet davranışı ilkesi oluşturma ve bir maliyet kontrol birimine atama](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="ce348-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="ce348-218">Adım 2: Maliyet dağıtımı hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="ce348-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="ce348-219">Maliyet dağıtımı, bir nesneden bir veya daha fazlasına ilgili tahsisat tabanı uygulayarak maliyeti yeniden dağıtmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ce348-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="ce348-220">Maliyet dağıtımı ve maliyet tahsisatı, maliyet dağıtımının her zaman orijinal maliyetin birincil maliyet öğesinde bulunmasıyla farklılık gösterir.</span><span class="sxs-lookup"><span data-stu-id="ce348-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="ce348-221">Maliyet dağıtım kuralını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="ce348-221">Define the cost distribution rule</span></span>

<span data-ttu-id="ce348-222">Mali muhasebede, elektrik maliyetleri çoğu zaman peşin ödeme olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="ce348-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="ce348-223">Maliyet muhasebesinde ise bu yöntem yeterince ayrıntılı değildir.</span><span class="sxs-lookup"><span data-stu-id="ce348-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="ce348-224">Değişken maliyet, maliyet nesnelerine tek tek, adil bir temele dayanarak dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ce348-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="ce348-225">En mantıklı tahsisat, elektrik kullanımını (Kwh) temel alarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ce348-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="ce348-226">Elektrik adına sahip, istatistiksel bir boyut üyesi oluşturulur ve elektrik tüketimi kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="ce348-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="ce348-227">Varsayıla olarak, tüm istatistiksel boyut üyeleri tahsisat tabanları olarak kullanılabilir hale gelir.</span><span class="sxs-lookup"><span data-stu-id="ce348-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ce348-228">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="ce348-228">Cost object</span></span></th>
<th><span data-ttu-id="ce348-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="ce348-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ce348-230">CC001</span><span class="sxs-lookup"><span data-stu-id="ce348-230">CC001</span></span></td>
<td><span data-ttu-id="ce348-231">İK</span><span class="sxs-lookup"><span data-stu-id="ce348-231">HR</span></span></td>
<td><span data-ttu-id="ce348-232">1.000</span><span class="sxs-lookup"><span data-stu-id="ce348-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-233">CC002</span><span class="sxs-lookup"><span data-stu-id="ce348-233">CC002</span></span></td>
<td><span data-ttu-id="ce348-234">Finans</span><span class="sxs-lookup"><span data-stu-id="ce348-234">Finance</span></span></td>
<td><span data-ttu-id="ce348-235">6,000</span><span class="sxs-lookup"><span data-stu-id="ce348-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-236">CC003</span><span class="sxs-lookup"><span data-stu-id="ce348-236">CC003</span></span></td>
<td><span data-ttu-id="ce348-237">Montaj</span><span class="sxs-lookup"><span data-stu-id="ce348-237">Assembly</span></span></td>
<td><span data-ttu-id="ce348-238">0</span><span class="sxs-lookup"><span data-stu-id="ce348-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ce348-239">Aşağıdaki tablo, elektrik tüketiminin değişken maliyetler için bir tahsisat tabanlı olarak uygulandığındaki sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="ce348-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ce348-240">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="ce348-240">Cost object</span></span></th>
<th><span data-ttu-id="ce348-241">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="ce348-241">Magnitude</span></span></th>
<th><span data-ttu-id="ce348-242">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="ce348-242">Allocation factor</span></span></th>
<th><span data-ttu-id="ce348-243">Tutar</span><span class="sxs-lookup"><span data-stu-id="ce348-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ce348-244">CC001</span><span class="sxs-lookup"><span data-stu-id="ce348-244">CC001</span></span></td>
<td><span data-ttu-id="ce348-245">İK</span><span class="sxs-lookup"><span data-stu-id="ce348-245">HR</span></span></td>
<td><span data-ttu-id="ce348-246">1.000</span><span class="sxs-lookup"><span data-stu-id="ce348-246">1,000</span></span></td>
<td><span data-ttu-id="ce348-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="ce348-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="ce348-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="ce348-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-249">CC002</span><span class="sxs-lookup"><span data-stu-id="ce348-249">CC002</span></span></td>
<td><span data-ttu-id="ce348-250">Finans</span><span class="sxs-lookup"><span data-stu-id="ce348-250">Finance</span></span></td>
<td><span data-ttu-id="ce348-251">6,000</span><span class="sxs-lookup"><span data-stu-id="ce348-251">6,000</span></span></td>
<td><span data-ttu-id="ce348-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="ce348-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="ce348-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="ce348-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-254">CC003</span><span class="sxs-lookup"><span data-stu-id="ce348-254">CC003</span></span></td>
<td><span data-ttu-id="ce348-255">Montaj</span><span class="sxs-lookup"><span data-stu-id="ce348-255">Assembly</span></span></td>
<td><span data-ttu-id="ce348-256">0</span><span class="sxs-lookup"><span data-stu-id="ce348-256">0</span></span></td>
<td><span data-ttu-id="ce348-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="ce348-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="ce348-258">0,00</span><span class="sxs-lookup"><span data-stu-id="ce348-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ce348-259">Sabit maliyet, elektrik tüketmiş olan tekil maliyet nesnelerine eşit miktarda dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ce348-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="ce348-260">Bu sonuca, Elektrik istatistiksel boyut öğesini bir formül tahsisat tabanında kullanarak ulaşabilirsiniz: (Elektrik &gt; 0,00) Aşağıdaki tablo, elektrik tüketimi değişken maliyetler için bir tahsisat tabanı olarak kullanıldığında ortaya çıkan sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="ce348-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ce348-261">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="ce348-261">Cost object</span></span></th>
<th><span data-ttu-id="ce348-262">Formül</span><span class="sxs-lookup"><span data-stu-id="ce348-262">Formula</span></span></th>
<th><span data-ttu-id="ce348-263">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="ce348-263">Magnitude</span></span></th>
<th><span data-ttu-id="ce348-264">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="ce348-264">Allocation factor</span></span></th>
<th><span data-ttu-id="ce348-265">Tutar</span><span class="sxs-lookup"><span data-stu-id="ce348-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ce348-266">CC001</span><span class="sxs-lookup"><span data-stu-id="ce348-266">CC001</span></span></td>
<td><span data-ttu-id="ce348-267">İK</span><span class="sxs-lookup"><span data-stu-id="ce348-267">HR</span></span></td>
<td><span data-ttu-id="ce348-268">(1,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="ce348-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="ce348-269">1</span><span class="sxs-lookup"><span data-stu-id="ce348-269">1</span></span></td>
<td><span data-ttu-id="ce348-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="ce348-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="ce348-271">500.00</span><span class="sxs-lookup"><span data-stu-id="ce348-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-272">CC002</span><span class="sxs-lookup"><span data-stu-id="ce348-272">CC002</span></span></td>
<td><span data-ttu-id="ce348-273">Finans</span><span class="sxs-lookup"><span data-stu-id="ce348-273">Finance</span></span></td>
<td><span data-ttu-id="ce348-274">(6,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="ce348-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="ce348-275">1</span><span class="sxs-lookup"><span data-stu-id="ce348-275">1</span></span></td>
<td><span data-ttu-id="ce348-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="ce348-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="ce348-277">500.00</span><span class="sxs-lookup"><span data-stu-id="ce348-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-278">CC003</span><span class="sxs-lookup"><span data-stu-id="ce348-278">CC003</span></span></td>
<td><span data-ttu-id="ce348-279">Montaj</span><span class="sxs-lookup"><span data-stu-id="ce348-279">Assembly</span></span></td>
<td><span data-ttu-id="ce348-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="ce348-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="ce348-281">0</span><span class="sxs-lookup"><span data-stu-id="ce348-281">0</span></span></td>
<td><span data-ttu-id="ce348-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="ce348-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="ce348-283">0,00</span><span class="sxs-lookup"><span data-stu-id="ce348-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="ce348-284">Günlük</span><span class="sxs-lookup"><span data-stu-id="ce348-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ce348-285">Günlük</span><span class="sxs-lookup"><span data-stu-id="ce348-285">Journal</span></span></th>
<th><span data-ttu-id="ce348-286">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="ce348-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="ce348-287">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="ce348-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="ce348-288">Sürüm</span><span class="sxs-lookup"><span data-stu-id="ce348-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ce348-289">00002</span><span class="sxs-lookup"><span data-stu-id="ce348-289">00002</span></span></td>
<td><span data-ttu-id="ce348-290">Maliyet dağıtımı hesaplama günlüğü</span><span class="sxs-lookup"><span data-stu-id="ce348-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="ce348-291">Mali</span><span class="sxs-lookup"><span data-stu-id="ce348-291">Fiscal</span></span></td>
<td><span data-ttu-id="ce348-292">2017</span><span class="sxs-lookup"><span data-stu-id="ce348-292">2017</span></span></td>
<td><span data-ttu-id="ce348-293">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="ce348-293">Period 1</span></span></td>
<td><span data-ttu-id="ce348-294">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="ce348-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="ce348-295">Günlük girişleri (Maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="ce348-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ce348-296">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="ce348-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ce348-297">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="ce348-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ce348-298">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="ce348-298">Cost element</span></span></th>
<th><span data-ttu-id="ce348-299">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="ce348-299">Cost behavior</span></span></th>
<th><span data-ttu-id="ce348-300">Tutar</span><span class="sxs-lookup"><span data-stu-id="ce348-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ce348-301">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="ce348-302">CC099</span><span class="sxs-lookup"><span data-stu-id="ce348-302">CC099</span></span></td>
<td><span data-ttu-id="ce348-303">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="ce348-303">Default cost center</span></span></td>
<td><span data-ttu-id="ce348-304">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-304">10001</span></span></td>
<td><span data-ttu-id="ce348-305">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-305">Electricity</span></span></td>
<td><span data-ttu-id="ce348-306">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-306">Fixed cost</span></span></td>
<td><span data-ttu-id="ce348-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="ce348-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-308">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="ce348-309">CC099</span><span class="sxs-lookup"><span data-stu-id="ce348-309">CC099</span></span></td>
<td><span data-ttu-id="ce348-310">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="ce348-310">Default cost center</span></span></td>
<td><span data-ttu-id="ce348-311">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-311">10001</span></span></td>
<td><span data-ttu-id="ce348-312">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-312">Electricity</span></span></td>
<td><span data-ttu-id="ce348-313">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-313">Variable cost</span></span></td>
<td><span data-ttu-id="ce348-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="ce348-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="ce348-315">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="ce348-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ce348-316">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="ce348-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ce348-317">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="ce348-317">Cost element</span></span></th>
<th><span data-ttu-id="ce348-318">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="ce348-318">Cost behavior</span></span></th>
<th><span data-ttu-id="ce348-319">Tutar</span><span class="sxs-lookup"><span data-stu-id="ce348-319">Amount</span></span></th>
<th><span data-ttu-id="ce348-320">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="ce348-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ce348-321">CC099</span><span class="sxs-lookup"><span data-stu-id="ce348-321">CC099</span></span></td>
<td><span data-ttu-id="ce348-322">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="ce348-322">Default cost center</span></span></td>
<td><span data-ttu-id="ce348-323">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-323">10001</span></span></td>
<td><span data-ttu-id="ce348-324">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-324">Electricity</span></span></td>
<td><span data-ttu-id="ce348-325">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-325">Fixed cost</span></span></td>
<td><span data-ttu-id="ce348-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="ce348-326">-1,000.00</span></span></td>
<td><span data-ttu-id="ce348-327">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-328">CC001</span><span class="sxs-lookup"><span data-stu-id="ce348-328">CC001</span></span></td>
<td><span data-ttu-id="ce348-329">İK</span><span class="sxs-lookup"><span data-stu-id="ce348-329">HR</span></span></td>
<td><span data-ttu-id="ce348-330">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-330">10001</span></span></td>
<td><span data-ttu-id="ce348-331">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-331">Electricity</span></span></td>
<td><span data-ttu-id="ce348-332">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-332">Fixed cost</span></span></td>
<td><span data-ttu-id="ce348-333">500.00</span><span class="sxs-lookup"><span data-stu-id="ce348-333">500.00</span></span></td>
<td><span data-ttu-id="ce348-334">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-335">CC002</span><span class="sxs-lookup"><span data-stu-id="ce348-335">CC002</span></span></td>
<td><span data-ttu-id="ce348-336">Finans</span><span class="sxs-lookup"><span data-stu-id="ce348-336">Finance</span></span></td>
<td><span data-ttu-id="ce348-337">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-337">10001</span></span></td>
<td><span data-ttu-id="ce348-338">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-338">Electricity</span></span></td>
<td><span data-ttu-id="ce348-339">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-339">Fixed cost</span></span></td>
<td><span data-ttu-id="ce348-340">500.00</span><span class="sxs-lookup"><span data-stu-id="ce348-340">500.00</span></span></td>
<td><span data-ttu-id="ce348-341">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-342">CC099</span><span class="sxs-lookup"><span data-stu-id="ce348-342">CC099</span></span></td>
<td><span data-ttu-id="ce348-343">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="ce348-343">Default cost center</span></span></td>
<td><span data-ttu-id="ce348-344">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-344">10001</span></span></td>
<td><span data-ttu-id="ce348-345">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-345">Electricity</span></span></td>
<td><span data-ttu-id="ce348-346">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-346">Variable cost</span></span></td>
<td><span data-ttu-id="ce348-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="ce348-347">-9,000.00</span></span></td>
<td><span data-ttu-id="ce348-348">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-349">CC001</span><span class="sxs-lookup"><span data-stu-id="ce348-349">CC001</span></span></td>
<td><span data-ttu-id="ce348-350">İK</span><span class="sxs-lookup"><span data-stu-id="ce348-350">HR</span></span></td>
<td><span data-ttu-id="ce348-351">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-351">10001</span></span></td>
<td><span data-ttu-id="ce348-352">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-352">Electricity</span></span></td>
<td><span data-ttu-id="ce348-353">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-353">Variable cost</span></span></td>
<td><span data-ttu-id="ce348-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="ce348-354">1,285.71</span></span></td>
<td><span data-ttu-id="ce348-355">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-356">CC002</span><span class="sxs-lookup"><span data-stu-id="ce348-356">CC002</span></span></td>
<td><span data-ttu-id="ce348-357">Finans</span><span class="sxs-lookup"><span data-stu-id="ce348-357">Finance</span></span></td>
<td><span data-ttu-id="ce348-358">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-358">10001</span></span></td>
<td><span data-ttu-id="ce348-359">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-359">Electricity</span></span></td>
<td><span data-ttu-id="ce348-360">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-360">Variable cost</span></span></td>
<td><span data-ttu-id="ce348-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="ce348-361">7,714.29</span></span></td>
<td><span data-ttu-id="ce348-362">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ce348-363">Daha fazla bilgi için bkz. [Maliyet dağıtımı ilkesi oluşturma ve bir maliyet kontrol birimine atama](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="ce348-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="ce348-364">Adım 3: Genel gider oranı hesaplama işlemi</span><span class="sxs-lookup"><span data-stu-id="ce348-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="ce348-365">Genel gider oranı, bir veya birden fazla belirli maliyet nesnesine masraf yüklemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ce348-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="ce348-366">Masraf, önceden belirlenmiş maliyet oranına ve tahsisat tabanından hesaplanan büyüklüğe dayanır.</span><span class="sxs-lookup"><span data-stu-id="ce348-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="ce348-367">Genel gider oranını tanımlama</span><span class="sxs-lookup"><span data-stu-id="ce348-367">Define the overhead rate</span></span>

<span data-ttu-id="ce348-368">Maliyet nesnesi CC001 HR, bir dizi dahili projeye katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="ce348-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="ce348-369">HR projeleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ce348-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ce348-370">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="ce348-370">Cost object</span></span></th>
<th><span data-ttu-id="ce348-371">Saatler</span><span class="sxs-lookup"><span data-stu-id="ce348-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ce348-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="ce348-372">Proj 1</span></span></td>
<td><span data-ttu-id="ce348-373">Proje 1</span><span class="sxs-lookup"><span data-stu-id="ce348-373">Project 1</span></span></td>
<td><span data-ttu-id="ce348-374">3</span><span class="sxs-lookup"><span data-stu-id="ce348-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="ce348-375">Proj 2</span></span></td>
<td><span data-ttu-id="ce348-376">Proje 2</span><span class="sxs-lookup"><span data-stu-id="ce348-376">Project 2</span></span></td>
<td><span data-ttu-id="ce348-377">1</span><span class="sxs-lookup"><span data-stu-id="ce348-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ce348-378">Maliyet projeleri dağıtımı için bir önceden belirlenmiş maliyet oranı tanımlandı.</span><span class="sxs-lookup"><span data-stu-id="ce348-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ce348-379">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="ce348-379">Cost object</span></span></th>
<th><span data-ttu-id="ce348-380">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="ce348-380">Cost element</span></span></th>
<th><span data-ttu-id="ce348-381">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="ce348-381">Cost behavior</span></span></th>
<th><span data-ttu-id="ce348-382">Birimler</span><span class="sxs-lookup"><span data-stu-id="ce348-382">Units</span></span></th>
<th><span data-ttu-id="ce348-383">Ücret</span><span class="sxs-lookup"><span data-stu-id="ce348-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ce348-384">CC001</span><span class="sxs-lookup"><span data-stu-id="ce348-384">CC001</span></span></td>
<td><span data-ttu-id="ce348-385">İK</span><span class="sxs-lookup"><span data-stu-id="ce348-385">HR</span></span></td>
<td><span data-ttu-id="ce348-386">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-386">10001</span></span></td>
<td><span data-ttu-id="ce348-387">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-387">Variable cost</span></span></td>
<td><span data-ttu-id="ce348-388">1</span><span class="sxs-lookup"><span data-stu-id="ce348-388">1</span></span></td>
<td><span data-ttu-id="ce348-389">10</span><span class="sxs-lookup"><span data-stu-id="ce348-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ce348-390">Aşağıdaki tablo, HR projeleri bir tahsisat tabanı olarak uygulandığındaki sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="ce348-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ce348-391">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="ce348-391">Cost object</span></span></th>
<th><span data-ttu-id="ce348-392">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="ce348-392">Magnitude</span></span></th>
<th><span data-ttu-id="ce348-393">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="ce348-393">Cost element</span></span></th>
<th><span data-ttu-id="ce348-394">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="ce348-394">Allocation factor</span></span></th>
<th><span data-ttu-id="ce348-395">Tutar</span><span class="sxs-lookup"><span data-stu-id="ce348-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ce348-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="ce348-396">Proj 1</span></span></td>
<td><span data-ttu-id="ce348-397">Proje 1</span><span class="sxs-lookup"><span data-stu-id="ce348-397">Project 1</span></span></td>
<td><span data-ttu-id="ce348-398">3</span><span class="sxs-lookup"><span data-stu-id="ce348-398">3</span></span></td>
<td><span data-ttu-id="ce348-399">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-399">10001</span></span></td>
<td><span data-ttu-id="ce348-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="ce348-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="ce348-401">30.00</span><span class="sxs-lookup"><span data-stu-id="ce348-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="ce348-402">Proj 2</span></span></td>
<td><span data-ttu-id="ce348-403">Proje 2</span><span class="sxs-lookup"><span data-stu-id="ce348-403">Project 2</span></span></td>
<td><span data-ttu-id="ce348-404">1</span><span class="sxs-lookup"><span data-stu-id="ce348-404">1</span></span></td>
<td><span data-ttu-id="ce348-405">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-405">10001</span></span></td>
<td><span data-ttu-id="ce348-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="ce348-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="ce348-407">10,00</span><span class="sxs-lookup"><span data-stu-id="ce348-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="ce348-408">Günlük</span><span class="sxs-lookup"><span data-stu-id="ce348-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ce348-409">Günlük</span><span class="sxs-lookup"><span data-stu-id="ce348-409">Journal</span></span></th>
<th><span data-ttu-id="ce348-410">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="ce348-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="ce348-411">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="ce348-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="ce348-412">Sürüm</span><span class="sxs-lookup"><span data-stu-id="ce348-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ce348-413">00003</span><span class="sxs-lookup"><span data-stu-id="ce348-413">00003</span></span></td>
<td><span data-ttu-id="ce348-414">Genel gider oranı hesaplaması günlüğü</span><span class="sxs-lookup"><span data-stu-id="ce348-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="ce348-415">Mali</span><span class="sxs-lookup"><span data-stu-id="ce348-415">Fiscal</span></span></td>
<td><span data-ttu-id="ce348-416">2017</span><span class="sxs-lookup"><span data-stu-id="ce348-416">2017</span></span></td>
<td><span data-ttu-id="ce348-417">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="ce348-417">Period 1</span></span></td>
<td><span data-ttu-id="ce348-418">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="ce348-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="ce348-419">Günlük girişleri (Genel gider oranı hesaplaması için günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="ce348-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ce348-420">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="ce348-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ce348-421">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="ce348-421">Cost object</span></span></th>
<th><span data-ttu-id="ce348-422">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="ce348-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ce348-423">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="ce348-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="ce348-424">Proj 1</span></span></td>
<td><span data-ttu-id="ce348-425">Dahili Proj 1</span><span class="sxs-lookup"><span data-stu-id="ce348-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="ce348-426">3,00</span><span class="sxs-lookup"><span data-stu-id="ce348-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-427">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="ce348-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="ce348-428">Proj 2</span></span></td>
<td><span data-ttu-id="ce348-429">Dahili Proj 2</span><span class="sxs-lookup"><span data-stu-id="ce348-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="ce348-430">1.00</span><span class="sxs-lookup"><span data-stu-id="ce348-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="ce348-431">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="ce348-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ce348-432">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="ce348-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ce348-433">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="ce348-433">Cost element</span></span></th>
<th><span data-ttu-id="ce348-434">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="ce348-434">Cost behavior</span></span></th>
<th><span data-ttu-id="ce348-435">Tutar</span><span class="sxs-lookup"><span data-stu-id="ce348-435">Amount</span></span></th>
<th><span data-ttu-id="ce348-436">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="ce348-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ce348-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="ce348-437">CC0001</span></span></td>
<td><span data-ttu-id="ce348-438">İK</span><span class="sxs-lookup"><span data-stu-id="ce348-438">HR</span></span></td>
<td><span data-ttu-id="ce348-439">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-439">10001</span></span></td>
<td><span data-ttu-id="ce348-440">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-440">Electricity</span></span></td>
<td><span data-ttu-id="ce348-441">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-441">Variable cost</span></span></td>
<td><span data-ttu-id="ce348-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="ce348-442">-30.00</span></span></td>
<td><span data-ttu-id="ce348-443">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="ce348-444">Proj 1</span></span></td>
<td><span data-ttu-id="ce348-445">Dahili Proj 1</span><span class="sxs-lookup"><span data-stu-id="ce348-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="ce348-446">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-446">10001</span></span></td>
<td><span data-ttu-id="ce348-447">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-447">Electricity</span></span></td>
<td><span data-ttu-id="ce348-448">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-448">Variable cost</span></span></td>
<td><span data-ttu-id="ce348-449">30.00</span><span class="sxs-lookup"><span data-stu-id="ce348-449">30.00</span></span></td>
<td><span data-ttu-id="ce348-450">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-451">CC001</span><span class="sxs-lookup"><span data-stu-id="ce348-451">CC001</span></span></td>
<td><span data-ttu-id="ce348-452">İK</span><span class="sxs-lookup"><span data-stu-id="ce348-452">HR</span></span></td>
<td><span data-ttu-id="ce348-453">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-453">10001</span></span></td>
<td><span data-ttu-id="ce348-454">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-454">Electricity</span></span></td>
<td><span data-ttu-id="ce348-455">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-455">Variable cost</span></span></td>
<td><span data-ttu-id="ce348-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="ce348-456">-10.00</span></span></td>
<td><span data-ttu-id="ce348-457">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="ce348-458">Proj 2</span></span></td>
<td><span data-ttu-id="ce348-459">Dahili Proj 2</span><span class="sxs-lookup"><span data-stu-id="ce348-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="ce348-460">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-460">10001</span></span></td>
<td><span data-ttu-id="ce348-461">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-461">Electricity</span></span></td>
<td><span data-ttu-id="ce348-462">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-462">Variable cost</span></span></td>
<td><span data-ttu-id="ce348-463">10,00</span><span class="sxs-lookup"><span data-stu-id="ce348-463">10.00</span></span></td>
<td><span data-ttu-id="ce348-464">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ce348-465">Daha fazla bilgi için [Genel gider hesaplaması gerçekleştir](cost-rollup.md#perform-overhead-calculation) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="ce348-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="ce348-466">Adım 4: Maliyet tahsisat hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="ce348-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="ce348-467">Tahsisat, bir tahsisat tabanı kullanarak bir maliyet nesnesinin diğer maliyet nesnelerine bakiyesini tahsis eder.</span><span class="sxs-lookup"><span data-stu-id="ce348-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="ce348-468">Finance karşılıklı tahsisat yöntemini desteklemektedir.</span><span class="sxs-lookup"><span data-stu-id="ce348-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="ce348-469">Karşılıklı tahsisat yönteminde, yardımcı maliyet nesnelerinin değiştiği karşılıklı hizmetler tümüyle tanınır.</span><span class="sxs-lookup"><span data-stu-id="ce348-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="ce348-470">Sistem, tahsisatların doğru gerçekleştireceği sırayı otomatik olarak belirler.</span><span class="sxs-lookup"><span data-stu-id="ce348-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="ce348-471">Bir maliyet nesnesinin bakiyesi tek bir tahsisat tabanı tarafından tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="ce348-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="ce348-472">Yeni maliyet nesnesi boyutları arasındaki tahsisatlar ve onların üyeleri desteklenir.</span><span class="sxs-lookup"><span data-stu-id="ce348-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="ce348-473">Tahsisatın sırası, maliyet kontrol birimi tarafından kontrol edilir.</span><span class="sxs-lookup"><span data-stu-id="ce348-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="ce348-474">[![Karşılıklı yöntemi](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="ce348-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="ce348-475">Maliyet tahsisatını tanımla</span><span class="sxs-lookup"><span data-stu-id="ce348-475">Define the cost allocation</span></span>

<span data-ttu-id="ce348-476">Bir maliyetin akışını nasıl izleyeceğinize dair basit bir örnek aşağıda verilmiştir,</span><span class="sxs-lookup"><span data-stu-id="ce348-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="ce348-477">Maliyet nesnesi CC001 HR, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="ce348-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="ce348-478">HR hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ce348-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ce348-479">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="ce348-479">Cost object</span></span></th>
<th><span data-ttu-id="ce348-480">HR hizmetleri</span><span class="sxs-lookup"><span data-stu-id="ce348-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ce348-481">CC002</span><span class="sxs-lookup"><span data-stu-id="ce348-481">CC002</span></span></td>
<td><span data-ttu-id="ce348-482">Finans</span><span class="sxs-lookup"><span data-stu-id="ce348-482">Finance</span></span></td>
<td><span data-ttu-id="ce348-483">35</span><span class="sxs-lookup"><span data-stu-id="ce348-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-484">CC003</span><span class="sxs-lookup"><span data-stu-id="ce348-484">CC003</span></span></td>
<td><span data-ttu-id="ce348-485">Montaj</span><span class="sxs-lookup"><span data-stu-id="ce348-485">Assembly</span></span></td>
<td><span data-ttu-id="ce348-486">55</span><span class="sxs-lookup"><span data-stu-id="ce348-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-487">CC004</span><span class="sxs-lookup"><span data-stu-id="ce348-487">CC004</span></span></td>
<td><span data-ttu-id="ce348-488">Paketleme</span><span class="sxs-lookup"><span data-stu-id="ce348-488">Packaging</span></span></td>
<td><span data-ttu-id="ce348-489">10</span><span class="sxs-lookup"><span data-stu-id="ce348-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ce348-490">Maliyet nesnesi CC002 Finans, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="ce348-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="ce348-491">Finans hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ce348-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ce348-492">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="ce348-492">Cost object</span></span></th>
<th><span data-ttu-id="ce348-493">Finans hizmetleri</span><span class="sxs-lookup"><span data-stu-id="ce348-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ce348-494">CC003</span><span class="sxs-lookup"><span data-stu-id="ce348-494">CC003</span></span></td>
<td><span data-ttu-id="ce348-495">Montaj</span><span class="sxs-lookup"><span data-stu-id="ce348-495">Assembly</span></span></td>
<td><span data-ttu-id="ce348-496">65</span><span class="sxs-lookup"><span data-stu-id="ce348-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-497">CC004</span><span class="sxs-lookup"><span data-stu-id="ce348-497">CC004</span></span></td>
<td><span data-ttu-id="ce348-498">Paketleme</span><span class="sxs-lookup"><span data-stu-id="ce348-498">Packaging</span></span></td>
<td><span data-ttu-id="ce348-499">35</span><span class="sxs-lookup"><span data-stu-id="ce348-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ce348-500">Maliyet nesnesi CC003 Derleme, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="ce348-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="ce348-501">Derleme hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ce348-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ce348-502">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="ce348-502">Cost object</span></span></th>
<th><span data-ttu-id="ce348-503">Derleme Hizmetleri (saat)</span><span class="sxs-lookup"><span data-stu-id="ce348-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ce348-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ce348-504">Prod 1</span></span></td>
<td><span data-ttu-id="ce348-505">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="ce348-505">Product 1</span></span></td>
<td><span data-ttu-id="ce348-506">60</span><span class="sxs-lookup"><span data-stu-id="ce348-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ce348-507">Prod 2</span></span></td>
<td><span data-ttu-id="ce348-508">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="ce348-508">Product 2</span></span></td>
<td><span data-ttu-id="ce348-509">20</span><span class="sxs-lookup"><span data-stu-id="ce348-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ce348-510">Maliyet nesnesi CC004 Ambalajlama, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="ce348-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="ce348-511">Ambalajlama hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ce348-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ce348-512">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="ce348-512">Cost object</span></span></th>
<th><span data-ttu-id="ce348-513">Ambalajlama hizmetleri (saat)</span><span class="sxs-lookup"><span data-stu-id="ce348-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ce348-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ce348-514">Prod 1</span></span></td>
<td><span data-ttu-id="ce348-515">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="ce348-515">Product 1</span></span></td>
<td><span data-ttu-id="ce348-516">80</span><span class="sxs-lookup"><span data-stu-id="ce348-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ce348-517">Prod 2</span></span></td>
<td><span data-ttu-id="ce348-518">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="ce348-518">Product 2</span></span></td>
<td><span data-ttu-id="ce348-519">15</span><span class="sxs-lookup"><span data-stu-id="ce348-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="ce348-520">Bir ürünün tükettiği üretim saatleri gibi istatistiki ölçümler, doğrudan kaynak verilerinden alınabilir.</span><span class="sxs-lookup"><span data-stu-id="ce348-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="ce348-521">Daha fazla bilgi için, [İstatistiksel ölçüm sağlayıcı şablonu](statistical-measure-provider-template.md#statistical-measure-provider-template) bakın.</span><span class="sxs-lookup"><span data-stu-id="ce348-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="ce348-522">Aşağıdaki tablo, İK hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığında ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="ce348-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ce348-523">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="ce348-523">Cost object</span></span></th>
<th><span data-ttu-id="ce348-524">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="ce348-524">Magnitude</span></span></th>
<th><span data-ttu-id="ce348-525">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="ce348-525">Allocation factor</span></span></th>
<th><span data-ttu-id="ce348-526">Tutar</span><span class="sxs-lookup"><span data-stu-id="ce348-526">Amount</span></span></th>
<th><span data-ttu-id="ce348-527">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="ce348-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ce348-528">CC002</span><span class="sxs-lookup"><span data-stu-id="ce348-528">CC002</span></span></td>
<td><span data-ttu-id="ce348-529">Finans</span><span class="sxs-lookup"><span data-stu-id="ce348-529">Finance</span></span></td>
<td><span data-ttu-id="ce348-530">35</span><span class="sxs-lookup"><span data-stu-id="ce348-530">35</span></span></td>
<td><span data-ttu-id="ce348-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="ce348-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="ce348-532">175.00</span><span class="sxs-lookup"><span data-stu-id="ce348-532">175.00</span></span></td>
<td><span data-ttu-id="ce348-533">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-534">CC003</span><span class="sxs-lookup"><span data-stu-id="ce348-534">CC003</span></span></td>
<td><span data-ttu-id="ce348-535">Montaj</span><span class="sxs-lookup"><span data-stu-id="ce348-535">Assembly</span></span></td>
<td><span data-ttu-id="ce348-536">55</span><span class="sxs-lookup"><span data-stu-id="ce348-536">55</span></span></td>
<td><span data-ttu-id="ce348-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="ce348-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="ce348-538">275.00</span><span class="sxs-lookup"><span data-stu-id="ce348-538">275.00</span></span></td>
<td><span data-ttu-id="ce348-539">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-540">CC004</span><span class="sxs-lookup"><span data-stu-id="ce348-540">CC004</span></span></td>
<td><span data-ttu-id="ce348-541">Paketleme</span><span class="sxs-lookup"><span data-stu-id="ce348-541">Packaging</span></span></td>
<td><span data-ttu-id="ce348-542">10</span><span class="sxs-lookup"><span data-stu-id="ce348-542">10</span></span></td>
<td><span data-ttu-id="ce348-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="ce348-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="ce348-544">50,00</span><span class="sxs-lookup"><span data-stu-id="ce348-544">50.00</span></span></td>
<td><span data-ttu-id="ce348-545">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-546">CC002</span><span class="sxs-lookup"><span data-stu-id="ce348-546">CC002</span></span></td>
<td><span data-ttu-id="ce348-547">Finans</span><span class="sxs-lookup"><span data-stu-id="ce348-547">Finance</span></span></td>
<td><span data-ttu-id="ce348-548">35</span><span class="sxs-lookup"><span data-stu-id="ce348-548">35</span></span></td>
<td><span data-ttu-id="ce348-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="ce348-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="ce348-550">436.00</span><span class="sxs-lookup"><span data-stu-id="ce348-550">436.00</span></span></td>
<td><span data-ttu-id="ce348-551">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-552">CC003</span><span class="sxs-lookup"><span data-stu-id="ce348-552">CC003</span></span></td>
<td><span data-ttu-id="ce348-553">Montaj</span><span class="sxs-lookup"><span data-stu-id="ce348-553">Assembly</span></span></td>
<td><span data-ttu-id="ce348-554">55</span><span class="sxs-lookup"><span data-stu-id="ce348-554">55</span></span></td>
<td><span data-ttu-id="ce348-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="ce348-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="ce348-556">685.14</span><span class="sxs-lookup"><span data-stu-id="ce348-556">685.14</span></span></td>
<td><span data-ttu-id="ce348-557">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-558">CC004</span><span class="sxs-lookup"><span data-stu-id="ce348-558">CC004</span></span></td>
<td><span data-ttu-id="ce348-559">Paketleme</span><span class="sxs-lookup"><span data-stu-id="ce348-559">Packaging</span></span></td>
<td><span data-ttu-id="ce348-560">10</span><span class="sxs-lookup"><span data-stu-id="ce348-560">10</span></span></td>
<td><span data-ttu-id="ce348-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="ce348-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="ce348-562">124.57</span><span class="sxs-lookup"><span data-stu-id="ce348-562">124.57</span></span></td>
<td><span data-ttu-id="ce348-563">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ce348-564">Aşağıdaki tablo, Finans hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="ce348-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ce348-565">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="ce348-565">Cost object</span></span></th>
<th><span data-ttu-id="ce348-566">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="ce348-566">Magnitude</span></span></th>
<th><span data-ttu-id="ce348-567">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="ce348-567">Allocation factor</span></span></th>
<th><span data-ttu-id="ce348-568">Tutar</span><span class="sxs-lookup"><span data-stu-id="ce348-568">Amount</span></span></th>
<th><span data-ttu-id="ce348-569">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="ce348-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ce348-570">CC003</span><span class="sxs-lookup"><span data-stu-id="ce348-570">CC003</span></span></td>
<td><span data-ttu-id="ce348-571">Montaj</span><span class="sxs-lookup"><span data-stu-id="ce348-571">Assembly</span></span></td>
<td><span data-ttu-id="ce348-572">65</span><span class="sxs-lookup"><span data-stu-id="ce348-572">65</span></span></td>
<td><span data-ttu-id="ce348-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="ce348-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="ce348-574">438.75</span><span class="sxs-lookup"><span data-stu-id="ce348-574">438.75</span></span></td>
<td><span data-ttu-id="ce348-575">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-576">CC004</span><span class="sxs-lookup"><span data-stu-id="ce348-576">CC004</span></span></td>
<td><span data-ttu-id="ce348-577">Paketleme</span><span class="sxs-lookup"><span data-stu-id="ce348-577">Packaging</span></span></td>
<td><span data-ttu-id="ce348-578">35</span><span class="sxs-lookup"><span data-stu-id="ce348-578">35</span></span></td>
<td><span data-ttu-id="ce348-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="ce348-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="ce348-580">236.25</span><span class="sxs-lookup"><span data-stu-id="ce348-580">236.25</span></span></td>
<td><span data-ttu-id="ce348-581">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-582">CC003</span><span class="sxs-lookup"><span data-stu-id="ce348-582">CC003</span></span></td>
<td><span data-ttu-id="ce348-583">Montaj</span><span class="sxs-lookup"><span data-stu-id="ce348-583">Assembly</span></span></td>
<td><span data-ttu-id="ce348-584">65</span><span class="sxs-lookup"><span data-stu-id="ce348-584">65</span></span></td>
<td><span data-ttu-id="ce348-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="ce348-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="ce348-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="ce348-586">5,297.69</span></span></td>
<td><span data-ttu-id="ce348-587">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-588">CC004</span><span class="sxs-lookup"><span data-stu-id="ce348-588">CC004</span></span></td>
<td><span data-ttu-id="ce348-589">Paketleme</span><span class="sxs-lookup"><span data-stu-id="ce348-589">Packaging</span></span></td>
<td><span data-ttu-id="ce348-590">35</span><span class="sxs-lookup"><span data-stu-id="ce348-590">35</span></span></td>
<td><span data-ttu-id="ce348-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="ce348-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="ce348-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="ce348-592">2,852.60</span></span></td>
<td><span data-ttu-id="ce348-593">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ce348-594">Aşağıdaki tablo, Derleme hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="ce348-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ce348-595">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="ce348-595">Cost object</span></span></th>
<th><span data-ttu-id="ce348-596">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="ce348-596">Magnitude</span></span></th>
<th><span data-ttu-id="ce348-597">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="ce348-597">Allocation factor</span></span></th>
<th><span data-ttu-id="ce348-598">Tutar</span><span class="sxs-lookup"><span data-stu-id="ce348-598">Amount</span></span></th>
<th><span data-ttu-id="ce348-599">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="ce348-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ce348-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ce348-600">Prod 1</span></span></td>
<td><span data-ttu-id="ce348-601">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="ce348-601">Product 1</span></span></td>
<td><span data-ttu-id="ce348-602">60</span><span class="sxs-lookup"><span data-stu-id="ce348-602">60</span></span></td>
<td><span data-ttu-id="ce348-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="ce348-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="ce348-604">535.31</span><span class="sxs-lookup"><span data-stu-id="ce348-604">535.31</span></span></td>
<td><span data-ttu-id="ce348-605">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ce348-606">Prod 2</span></span></td>
<td><span data-ttu-id="ce348-607">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="ce348-607">Product 2</span></span></td>
<td><span data-ttu-id="ce348-608">20</span><span class="sxs-lookup"><span data-stu-id="ce348-608">20</span></span></td>
<td><span data-ttu-id="ce348-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="ce348-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="ce348-610">178.44</span><span class="sxs-lookup"><span data-stu-id="ce348-610">178.44</span></span></td>
<td><span data-ttu-id="ce348-611">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ce348-612">Prod 1</span></span></td>
<td><span data-ttu-id="ce348-613">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="ce348-613">Product 1</span></span></td>
<td><span data-ttu-id="ce348-614">60</span><span class="sxs-lookup"><span data-stu-id="ce348-614">60</span></span></td>
<td><span data-ttu-id="ce348-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="ce348-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="ce348-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="ce348-616">4,487.12</span></span></td>
<td><span data-ttu-id="ce348-617">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ce348-618">Prod 2</span></span></td>
<td><span data-ttu-id="ce348-619">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="ce348-619">Product 2</span></span></td>
<td><span data-ttu-id="ce348-620">20</span><span class="sxs-lookup"><span data-stu-id="ce348-620">20</span></span></td>
<td><span data-ttu-id="ce348-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="ce348-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="ce348-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="ce348-622">1,495.71</span></span></td>
<td><span data-ttu-id="ce348-623">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ce348-624">Aşağıdaki tablo, Paketleme hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="ce348-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ce348-625">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="ce348-625">Cost object</span></span></th>
<th><span data-ttu-id="ce348-626">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="ce348-626">Magnitude</span></span></th>
<th><span data-ttu-id="ce348-627">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="ce348-627">Allocation factor</span></span></th>
<th><span data-ttu-id="ce348-628">Tutar</span><span class="sxs-lookup"><span data-stu-id="ce348-628">Amount</span></span></th>
<th><span data-ttu-id="ce348-629">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="ce348-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ce348-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ce348-630">Prod 1</span></span></td>
<td><span data-ttu-id="ce348-631">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="ce348-631">Product 1</span></span></td>
<td><span data-ttu-id="ce348-632">80</span><span class="sxs-lookup"><span data-stu-id="ce348-632">80</span></span></td>
<td><span data-ttu-id="ce348-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="ce348-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="ce348-634">241.05</span><span class="sxs-lookup"><span data-stu-id="ce348-634">241.05</span></span></td>
<td><span data-ttu-id="ce348-635">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ce348-636">Prod 2</span></span></td>
<td><span data-ttu-id="ce348-637">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="ce348-637">Product 2</span></span></td>
<td><span data-ttu-id="ce348-638">15</span><span class="sxs-lookup"><span data-stu-id="ce348-638">15</span></span></td>
<td><span data-ttu-id="ce348-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="ce348-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="ce348-640">45.20</span><span class="sxs-lookup"><span data-stu-id="ce348-640">45.20</span></span></td>
<td><span data-ttu-id="ce348-641">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ce348-642">Prod 1</span></span></td>
<td><span data-ttu-id="ce348-643">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="ce348-643">Product 1</span></span></td>
<td><span data-ttu-id="ce348-644">80</span><span class="sxs-lookup"><span data-stu-id="ce348-644">80</span></span></td>
<td><span data-ttu-id="ce348-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="ce348-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="ce348-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="ce348-646">2,507.09</span></span></td>
<td><span data-ttu-id="ce348-647">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ce348-648">Prod 2</span></span></td>
<td><span data-ttu-id="ce348-649">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="ce348-649">Product 2</span></span></td>
<td><span data-ttu-id="ce348-650">15</span><span class="sxs-lookup"><span data-stu-id="ce348-650">15</span></span></td>
<td><span data-ttu-id="ce348-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="ce348-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="ce348-652">470.08</span><span class="sxs-lookup"><span data-stu-id="ce348-652">470.08</span></span></td>
<td><span data-ttu-id="ce348-653">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="ce348-654">Günlük girişleri (maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="ce348-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ce348-655">Günlük</span><span class="sxs-lookup"><span data-stu-id="ce348-655">Journal</span></span></th>
<th><span data-ttu-id="ce348-656">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="ce348-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="ce348-657">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="ce348-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="ce348-658">Sürüm</span><span class="sxs-lookup"><span data-stu-id="ce348-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ce348-659">00004</span><span class="sxs-lookup"><span data-stu-id="ce348-659">00004</span></span></td>
<td><span data-ttu-id="ce348-660">Maliyet tahsisatı günlüğü</span><span class="sxs-lookup"><span data-stu-id="ce348-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="ce348-661">Mali</span><span class="sxs-lookup"><span data-stu-id="ce348-661">Fiscal</span></span></td>
<td><span data-ttu-id="ce348-662">2017</span><span class="sxs-lookup"><span data-stu-id="ce348-662">2017</span></span></td>
<td><span data-ttu-id="ce348-663">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="ce348-663">Period 1</span></span></td>
<td><span data-ttu-id="ce348-664">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="ce348-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="ce348-665">Günlük satırları</span><span class="sxs-lookup"><span data-stu-id="ce348-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="ce348-666">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="ce348-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="ce348-667">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="ce348-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ce348-668">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="ce348-668">Cost element</span></span></th>
<th><span data-ttu-id="ce348-669">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="ce348-669">Cost behavior</span></span></th>
<th><span data-ttu-id="ce348-670">Tutar</span><span class="sxs-lookup"><span data-stu-id="ce348-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ce348-671">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="ce348-672">CC001</span><span class="sxs-lookup"><span data-stu-id="ce348-672">CC001</span></span></td>
<td><span data-ttu-id="ce348-673">İK</span><span class="sxs-lookup"><span data-stu-id="ce348-673">HR</span></span></td>
<td><span data-ttu-id="ce348-674">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-674">10001</span></span></td>
<td><span data-ttu-id="ce348-675">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-675">Electricity</span></span></td>
<td><span data-ttu-id="ce348-676">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-676">Fixed cost</span></span></td>
<td><span data-ttu-id="ce348-677">500.00</span><span class="sxs-lookup"><span data-stu-id="ce348-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-678">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="ce348-679">CC001</span><span class="sxs-lookup"><span data-stu-id="ce348-679">CC001</span></span></td>
<td><span data-ttu-id="ce348-680">İK</span><span class="sxs-lookup"><span data-stu-id="ce348-680">HR</span></span></td>
<td><span data-ttu-id="ce348-681">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-681">10001</span></span></td>
<td><span data-ttu-id="ce348-682">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-682">Electricity</span></span></td>
<td><span data-ttu-id="ce348-683">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-683">Variable cost</span></span></td>
<td><span data-ttu-id="ce348-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="ce348-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-685">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="ce348-686">CC002</span><span class="sxs-lookup"><span data-stu-id="ce348-686">CC002</span></span></td>
<td><span data-ttu-id="ce348-687">Finans</span><span class="sxs-lookup"><span data-stu-id="ce348-687">Finance</span></span></td>
<td><span data-ttu-id="ce348-688">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-688">10001</span></span></td>
<td><span data-ttu-id="ce348-689">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-689">Electricity</span></span></td>
<td><span data-ttu-id="ce348-690">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-690">Fixed cost</span></span></td>
<td><span data-ttu-id="ce348-691">675.00</span><span class="sxs-lookup"><span data-stu-id="ce348-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-692">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="ce348-693">CC002</span><span class="sxs-lookup"><span data-stu-id="ce348-693">CC002</span></span></td>
<td><span data-ttu-id="ce348-694">Finans</span><span class="sxs-lookup"><span data-stu-id="ce348-694">Finance</span></span></td>
<td><span data-ttu-id="ce348-695">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-695">10001</span></span></td>
<td><span data-ttu-id="ce348-696">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-696">Electricity</span></span></td>
<td><span data-ttu-id="ce348-697">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-697">Variable cost</span></span></td>
<td><span data-ttu-id="ce348-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="ce348-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-699">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="ce348-700">CC003</span><span class="sxs-lookup"><span data-stu-id="ce348-700">CC003</span></span></td>
<td><span data-ttu-id="ce348-701">Montaj</span><span class="sxs-lookup"><span data-stu-id="ce348-701">Assembly</span></span></td>
<td><span data-ttu-id="ce348-702">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-702">10001</span></span></td>
<td><span data-ttu-id="ce348-703">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-703">Electricity</span></span></td>
<td><span data-ttu-id="ce348-704">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-704">Fixed cost</span></span></td>
<td><span data-ttu-id="ce348-705">713.75</span><span class="sxs-lookup"><span data-stu-id="ce348-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-706">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="ce348-707">CC003</span><span class="sxs-lookup"><span data-stu-id="ce348-707">CC003</span></span></td>
<td><span data-ttu-id="ce348-708">Montaj</span><span class="sxs-lookup"><span data-stu-id="ce348-708">Assembly</span></span></td>
<td><span data-ttu-id="ce348-709">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-709">10001</span></span></td>
<td><span data-ttu-id="ce348-710">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-710">Electricity</span></span></td>
<td><span data-ttu-id="ce348-711">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-711">Variable cost</span></span></td>
<td><span data-ttu-id="ce348-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="ce348-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-713">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="ce348-714">CC003</span><span class="sxs-lookup"><span data-stu-id="ce348-714">CC003</span></span></td>
<td><span data-ttu-id="ce348-715">Paketleme</span><span class="sxs-lookup"><span data-stu-id="ce348-715">Packaging</span></span></td>
<td><span data-ttu-id="ce348-716">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-716">10001</span></span></td>
<td><span data-ttu-id="ce348-717">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-717">Electricity</span></span></td>
<td><span data-ttu-id="ce348-718">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-718">Fixed cost</span></span></td>
<td><span data-ttu-id="ce348-719">286.25</span><span class="sxs-lookup"><span data-stu-id="ce348-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-720">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="ce348-721">CC003</span><span class="sxs-lookup"><span data-stu-id="ce348-721">CC003</span></span></td>
<td><span data-ttu-id="ce348-722">Paketleme</span><span class="sxs-lookup"><span data-stu-id="ce348-722">Packaging</span></span></td>
<td><span data-ttu-id="ce348-723">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-723">10001</span></span></td>
<td><span data-ttu-id="ce348-724">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-724">Electricity</span></span></td>
<td><span data-ttu-id="ce348-725">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-725">Variable cost</span></span></td>
<td><span data-ttu-id="ce348-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="ce348-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-727">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="ce348-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ce348-728">Prod 1</span></span></td>
<td><span data-ttu-id="ce348-729">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="ce348-729">Product 1</span></span></td>
<td><span data-ttu-id="ce348-730">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-730">10001</span></span></td>
<td><span data-ttu-id="ce348-731">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-731">Electricity</span></span></td>
<td><span data-ttu-id="ce348-732">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-732">Fixed cost</span></span></td>
<td><span data-ttu-id="ce348-733">776.36</span><span class="sxs-lookup"><span data-stu-id="ce348-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-734">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="ce348-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ce348-735">Prod 1</span></span></td>
<td><span data-ttu-id="ce348-736">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="ce348-736">Product 1</span></span></td>
<td><span data-ttu-id="ce348-737">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-737">10001</span></span></td>
<td><span data-ttu-id="ce348-738">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-738">Electricity</span></span></td>
<td><span data-ttu-id="ce348-739">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-739">Variable cost</span></span></td>
<td><span data-ttu-id="ce348-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="ce348-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-741">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="ce348-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ce348-742">Prod 2</span></span></td>
<td><span data-ttu-id="ce348-743">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="ce348-743">Product 1</span></span></td>
<td><span data-ttu-id="ce348-744">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-744">10001</span></span></td>
<td><span data-ttu-id="ce348-745">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-745">Electricity</span></span></td>
<td><span data-ttu-id="ce348-746">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-746">Fixed cost</span></span></td>
<td><span data-ttu-id="ce348-747">223.64</span><span class="sxs-lookup"><span data-stu-id="ce348-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-748">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="ce348-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ce348-749">Prod 2</span></span></td>
<td><span data-ttu-id="ce348-750">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="ce348-750">Product 1</span></span></td>
<td><span data-ttu-id="ce348-751">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-751">10001</span></span></td>
<td><span data-ttu-id="ce348-752">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-752">Electricity</span></span></td>
<td><span data-ttu-id="ce348-753">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-753">Variable cost</span></span></td>
<td><span data-ttu-id="ce348-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="ce348-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="ce348-755">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="ce348-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="ce348-756">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="ce348-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="ce348-757">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="ce348-757">Cost element</span></span></th>
<th><span data-ttu-id="ce348-758">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="ce348-758">Cost behavior</span></span></th>
<th><span data-ttu-id="ce348-759">Tutar</span><span class="sxs-lookup"><span data-stu-id="ce348-759">Amount</span></span></th>
<th><span data-ttu-id="ce348-760">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="ce348-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ce348-761">CC001</span><span class="sxs-lookup"><span data-stu-id="ce348-761">CC001</span></span></td>
<td><span data-ttu-id="ce348-762">İK</span><span class="sxs-lookup"><span data-stu-id="ce348-762">HR</span></span></td>
<td><span data-ttu-id="ce348-763">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-763">10001</span></span></td>
<td><span data-ttu-id="ce348-764">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-764">Electricity</span></span></td>
<td><span data-ttu-id="ce348-765">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-765">Fixed cost</span></span></td>
<td><span data-ttu-id="ce348-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="ce348-766">-500.00</span></span></td>
<td><span data-ttu-id="ce348-767">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-768">CC002</span><span class="sxs-lookup"><span data-stu-id="ce348-768">CC002</span></span></td>
<td><span data-ttu-id="ce348-769">Finans</span><span class="sxs-lookup"><span data-stu-id="ce348-769">Finance</span></span></td>
<td><span data-ttu-id="ce348-770">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-770">10001</span></span></td>
<td><span data-ttu-id="ce348-771">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-771">Electricity</span></span></td>
<td><span data-ttu-id="ce348-772">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-772">Fixed cost</span></span></td>
<td><span data-ttu-id="ce348-773">175.00</span><span class="sxs-lookup"><span data-stu-id="ce348-773">175.00</span></span></td>
<td><span data-ttu-id="ce348-774">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-775">CC003</span><span class="sxs-lookup"><span data-stu-id="ce348-775">CC003</span></span></td>
<td><span data-ttu-id="ce348-776">Montaj</span><span class="sxs-lookup"><span data-stu-id="ce348-776">Assembly</span></span></td>
<td><span data-ttu-id="ce348-777">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-777">10001</span></span></td>
<td><span data-ttu-id="ce348-778">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-778">Electricity</span></span></td>
<td><span data-ttu-id="ce348-779">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-779">Fixed cost</span></span></td>
<td><span data-ttu-id="ce348-780">275.00</span><span class="sxs-lookup"><span data-stu-id="ce348-780">275.00</span></span></td>
<td><span data-ttu-id="ce348-781">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-782">CC004</span><span class="sxs-lookup"><span data-stu-id="ce348-782">CC004</span></span></td>
<td><span data-ttu-id="ce348-783">Paketleme</span><span class="sxs-lookup"><span data-stu-id="ce348-783">Packaging</span></span></td>
<td><span data-ttu-id="ce348-784">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-784">10001</span></span></td>
<td><span data-ttu-id="ce348-785">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-785">Electricity</span></span></td>
<td><span data-ttu-id="ce348-786">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-786">Fixed cost</span></span></td>
<td><span data-ttu-id="ce348-787">50,00</span><span class="sxs-lookup"><span data-stu-id="ce348-787">50,00</span></span></td>
<td><span data-ttu-id="ce348-788">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-789">CC001</span><span class="sxs-lookup"><span data-stu-id="ce348-789">CC001</span></span></td>
<td><span data-ttu-id="ce348-790">İK</span><span class="sxs-lookup"><span data-stu-id="ce348-790">HR</span></span></td>
<td><span data-ttu-id="ce348-791">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-791">10001</span></span></td>
<td><span data-ttu-id="ce348-792">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-792">Electricity</span></span></td>
<td><span data-ttu-id="ce348-793">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-793">Variable cost</span></span></td>
<td><span data-ttu-id="ce348-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="ce348-794">-1,245.71</span></span></td>
<td><span data-ttu-id="ce348-795">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-796">CC002</span><span class="sxs-lookup"><span data-stu-id="ce348-796">CC002</span></span></td>
<td><span data-ttu-id="ce348-797">Finans</span><span class="sxs-lookup"><span data-stu-id="ce348-797">Finance</span></span></td>
<td><span data-ttu-id="ce348-798">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-798">10001</span></span></td>
<td><span data-ttu-id="ce348-799">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-799">Electricity</span></span></td>
<td><span data-ttu-id="ce348-800">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-800">Variable cost</span></span></td>
<td><span data-ttu-id="ce348-801">436.00</span><span class="sxs-lookup"><span data-stu-id="ce348-801">436.00</span></span></td>
<td><span data-ttu-id="ce348-802">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-803">CC003</span><span class="sxs-lookup"><span data-stu-id="ce348-803">CC003</span></span></td>
<td><span data-ttu-id="ce348-804">Montaj</span><span class="sxs-lookup"><span data-stu-id="ce348-804">Assembly</span></span></td>
<td><span data-ttu-id="ce348-805">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-805">10001</span></span></td>
<td><span data-ttu-id="ce348-806">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-806">Electricity</span></span></td>
<td><span data-ttu-id="ce348-807">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-807">Variable cost</span></span></td>
<td><span data-ttu-id="ce348-808">685.14</span><span class="sxs-lookup"><span data-stu-id="ce348-808">685.14</span></span></td>
<td><span data-ttu-id="ce348-809">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-810">CC004</span><span class="sxs-lookup"><span data-stu-id="ce348-810">CC004</span></span></td>
<td><span data-ttu-id="ce348-811">Paketleme</span><span class="sxs-lookup"><span data-stu-id="ce348-811">Packaging</span></span></td>
<td><span data-ttu-id="ce348-812">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-812">10001</span></span></td>
<td><span data-ttu-id="ce348-813">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-813">Electricity</span></span></td>
<td><span data-ttu-id="ce348-814">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-814">Variable cost</span></span></td>
<td><span data-ttu-id="ce348-815">124.57</span><span class="sxs-lookup"><span data-stu-id="ce348-815">124.57</span></span></td>
<td><span data-ttu-id="ce348-816">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-817">CC002</span><span class="sxs-lookup"><span data-stu-id="ce348-817">CC002</span></span></td>
<td><span data-ttu-id="ce348-818">Finans</span><span class="sxs-lookup"><span data-stu-id="ce348-818">Finance</span></span></td>
<td><span data-ttu-id="ce348-819">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-819">10001</span></span></td>
<td><span data-ttu-id="ce348-820">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-820">Electricity</span></span></td>
<td><span data-ttu-id="ce348-821">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-821">Fixed cost</span></span></td>
<td><span data-ttu-id="ce348-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="ce348-822">-675.00</span></span></td>
<td><span data-ttu-id="ce348-823">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-824">CC003</span><span class="sxs-lookup"><span data-stu-id="ce348-824">CC003</span></span></td>
<td><span data-ttu-id="ce348-825">Montaj</span><span class="sxs-lookup"><span data-stu-id="ce348-825">Assembly</span></span></td>
<td><span data-ttu-id="ce348-826">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-826">10001</span></span></td>
<td><span data-ttu-id="ce348-827">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-827">Electricity</span></span></td>
<td><span data-ttu-id="ce348-828">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-828">Fixed cost</span></span></td>
<td><span data-ttu-id="ce348-829">438.75</span><span class="sxs-lookup"><span data-stu-id="ce348-829">438.75</span></span></td>
<td><span data-ttu-id="ce348-830">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-831">CC004</span><span class="sxs-lookup"><span data-stu-id="ce348-831">CC004</span></span></td>
<td><span data-ttu-id="ce348-832">Paketleme</span><span class="sxs-lookup"><span data-stu-id="ce348-832">Packaging</span></span></td>
<td><span data-ttu-id="ce348-833">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-833">10001</span></span></td>
<td><span data-ttu-id="ce348-834">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-834">Electricity</span></span></td>
<td><span data-ttu-id="ce348-835">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-835">Fixed cost</span></span></td>
<td><span data-ttu-id="ce348-836">236.25</span><span class="sxs-lookup"><span data-stu-id="ce348-836">236.25</span></span></td>
<td><span data-ttu-id="ce348-837">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-838">CC002</span><span class="sxs-lookup"><span data-stu-id="ce348-838">CC002</span></span></td>
<td><span data-ttu-id="ce348-839">Finans</span><span class="sxs-lookup"><span data-stu-id="ce348-839">Finance</span></span></td>
<td><span data-ttu-id="ce348-840">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-840">10001</span></span></td>
<td><span data-ttu-id="ce348-841">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-841">Electricity</span></span></td>
<td><span data-ttu-id="ce348-842">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-842">Variable cost</span></span></td>
<td><span data-ttu-id="ce348-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="ce348-843">-8,150.29</span></span></td>
<td><span data-ttu-id="ce348-844">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-845">CC003</span><span class="sxs-lookup"><span data-stu-id="ce348-845">CC003</span></span></td>
<td><span data-ttu-id="ce348-846">Montaj</span><span class="sxs-lookup"><span data-stu-id="ce348-846">Assembly</span></span></td>
<td><span data-ttu-id="ce348-847">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-847">10001</span></span></td>
<td><span data-ttu-id="ce348-848">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-848">Electricity</span></span></td>
<td><span data-ttu-id="ce348-849">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-849">Variable cost</span></span></td>
<td><span data-ttu-id="ce348-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="ce348-850">5,297.69</span></span></td>
<td><span data-ttu-id="ce348-851">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-852">CC004</span><span class="sxs-lookup"><span data-stu-id="ce348-852">CC004</span></span></td>
<td><span data-ttu-id="ce348-853">Paketleme</span><span class="sxs-lookup"><span data-stu-id="ce348-853">Packaging</span></span></td>
<td><span data-ttu-id="ce348-854">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-854">10001</span></span></td>
<td><span data-ttu-id="ce348-855">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-855">Electricity</span></span></td>
<td><span data-ttu-id="ce348-856">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-856">Variable cost</span></span></td>
<td><span data-ttu-id="ce348-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="ce348-857">2,852.60</span></span></td>
<td><span data-ttu-id="ce348-858">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-859">CC003</span><span class="sxs-lookup"><span data-stu-id="ce348-859">CC003</span></span></td>
<td><span data-ttu-id="ce348-860">Montaj</span><span class="sxs-lookup"><span data-stu-id="ce348-860">Assembly</span></span></td>
<td><span data-ttu-id="ce348-861">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-861">10001</span></span></td>
<td><span data-ttu-id="ce348-862">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-862">Electricity</span></span></td>
<td><span data-ttu-id="ce348-863">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-863">Fixed cost</span></span></td>
<td><span data-ttu-id="ce348-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="ce348-864">-713.75</span></span></td>
<td><span data-ttu-id="ce348-865">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ce348-866">Prod 1</span></span></td>
<td><span data-ttu-id="ce348-867">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="ce348-867">Product 1</span></span></td>
<td><span data-ttu-id="ce348-868">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-868">10001</span></span></td>
<td><span data-ttu-id="ce348-869">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-869">Electricity</span></span></td>
<td><span data-ttu-id="ce348-870">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-870">Fixed cost</span></span></td>
<td><span data-ttu-id="ce348-871">535.31</span><span class="sxs-lookup"><span data-stu-id="ce348-871">535.31</span></span></td>
<td><span data-ttu-id="ce348-872">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ce348-873">Prod 2</span></span></td>
<td><span data-ttu-id="ce348-874">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="ce348-874">Product 2</span></span></td>
<td><span data-ttu-id="ce348-875">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-875">10001</span></span></td>
<td><span data-ttu-id="ce348-876">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-876">Electricity</span></span></td>
<td><span data-ttu-id="ce348-877">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-877">Fixed cost</span></span></td>
<td><span data-ttu-id="ce348-878">178.44</span><span class="sxs-lookup"><span data-stu-id="ce348-878">178.44</span></span></td>
<td><span data-ttu-id="ce348-879">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-880">CC003</span><span class="sxs-lookup"><span data-stu-id="ce348-880">CC003</span></span></td>
<td><span data-ttu-id="ce348-881">Montaj</span><span class="sxs-lookup"><span data-stu-id="ce348-881">Assembly</span></span></td>
<td><span data-ttu-id="ce348-882">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-882">10001</span></span></td>
<td><span data-ttu-id="ce348-883">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-883">Electricity</span></span></td>
<td><span data-ttu-id="ce348-884">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-884">Variable cost</span></span></td>
<td><span data-ttu-id="ce348-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="ce348-885">-5,982.83</span></span></td>
<td><span data-ttu-id="ce348-886">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ce348-887">Prod 1</span></span></td>
<td><span data-ttu-id="ce348-888">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="ce348-888">Product 1</span></span></td>
<td><span data-ttu-id="ce348-889">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-889">10001</span></span></td>
<td><span data-ttu-id="ce348-890">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-890">Electricity</span></span></td>
<td><span data-ttu-id="ce348-891">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-891">Variable cost</span></span></td>
<td><span data-ttu-id="ce348-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="ce348-892">4,487.12</span></span></td>
<td><span data-ttu-id="ce348-893">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ce348-894">Prod 2</span></span></td>
<td><span data-ttu-id="ce348-895">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="ce348-895">Product 2</span></span></td>
<td><span data-ttu-id="ce348-896">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-896">10001</span></span></td>
<td><span data-ttu-id="ce348-897">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-897">Electricity</span></span></td>
<td><span data-ttu-id="ce348-898">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-898">Variable cost</span></span></td>
<td><span data-ttu-id="ce348-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="ce348-899">1,495.71</span></span></td>
<td><span data-ttu-id="ce348-900">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-901">CC003</span><span class="sxs-lookup"><span data-stu-id="ce348-901">CC003</span></span></td>
<td><span data-ttu-id="ce348-902">Montaj</span><span class="sxs-lookup"><span data-stu-id="ce348-902">Assembly</span></span></td>
<td><span data-ttu-id="ce348-903">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-903">10001</span></span></td>
<td><span data-ttu-id="ce348-904">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-904">Electricity</span></span></td>
<td><span data-ttu-id="ce348-905">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-905">Fixed cost</span></span></td>
<td><span data-ttu-id="ce348-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="ce348-906">-286.25</span></span></td>
<td><span data-ttu-id="ce348-907">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ce348-908">Prod 1</span></span></td>
<td><span data-ttu-id="ce348-909">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="ce348-909">Product 1</span></span></td>
<td><span data-ttu-id="ce348-910">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-910">10001</span></span></td>
<td><span data-ttu-id="ce348-911">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-911">Electricity</span></span></td>
<td><span data-ttu-id="ce348-912">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-912">Fixed cost</span></span></td>
<td><span data-ttu-id="ce348-913">241.05</span><span class="sxs-lookup"><span data-stu-id="ce348-913">241.05</span></span></td>
<td><span data-ttu-id="ce348-914">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ce348-915">Prod 2</span></span></td>
<td><span data-ttu-id="ce348-916">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="ce348-916">Product 2</span></span></td>
<td><span data-ttu-id="ce348-917">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-917">10001</span></span></td>
<td><span data-ttu-id="ce348-918">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-918">Electricity</span></span></td>
<td><span data-ttu-id="ce348-919">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-919">Fixed cost</span></span></td>
<td><span data-ttu-id="ce348-920">45.20</span><span class="sxs-lookup"><span data-stu-id="ce348-920">45.20</span></span></td>
<td><span data-ttu-id="ce348-921">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-922">CC003</span><span class="sxs-lookup"><span data-stu-id="ce348-922">CC003</span></span></td>
<td><span data-ttu-id="ce348-923">Montaj</span><span class="sxs-lookup"><span data-stu-id="ce348-923">Assembly</span></span></td>
<td><span data-ttu-id="ce348-924">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-924">10001</span></span></td>
<td><span data-ttu-id="ce348-925">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-925">Electricity</span></span></td>
<td><span data-ttu-id="ce348-926">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-926">Variable cost</span></span></td>
<td><span data-ttu-id="ce348-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="ce348-927">-2,977.17</span></span></td>
<td><span data-ttu-id="ce348-928">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ce348-929">Prod 1</span></span></td>
<td><span data-ttu-id="ce348-930">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="ce348-930">Product 1</span></span></td>
<td><span data-ttu-id="ce348-931">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-931">10001</span></span></td>
<td><span data-ttu-id="ce348-932">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-932">Electricity</span></span></td>
<td><span data-ttu-id="ce348-933">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-933">Variable cost</span></span></td>
<td><span data-ttu-id="ce348-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="ce348-934">2,507.09</span></span></td>
<td><span data-ttu-id="ce348-935">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ce348-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ce348-936">Prod 2</span></span></td>
<td><span data-ttu-id="ce348-937">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="ce348-937">Product 2</span></span></td>
<td><span data-ttu-id="ce348-938">10001</span><span class="sxs-lookup"><span data-stu-id="ce348-938">10001</span></span></td>
<td><span data-ttu-id="ce348-939">Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-939">Electricity</span></span></td>
<td><span data-ttu-id="ce348-940">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-940">Variable cost</span></span></td>
<td><span data-ttu-id="ce348-941">470.08</span><span class="sxs-lookup"><span data-stu-id="ce348-941">470.08</span></span></td>
<td><span data-ttu-id="ce348-942">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="ce348-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="ce348-943">Sonuç</span><span class="sxs-lookup"><span data-stu-id="ce348-943">Conclusion</span></span>
<span data-ttu-id="ce348-944">Mali muhasebede, Elektrik için 10.000,00 maliyet bir sözde maliyet merkezi kimliğine nakledilmiştir.</span><span class="sxs-lookup"><span data-stu-id="ce348-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="ce348-945">Bu nedenle, maliyet muhasebecileri bu maliyetin tahsis edilmesi gerektiğini bilirler.</span><span class="sxs-lookup"><span data-stu-id="ce348-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="ce348-946">Maliyet muhasebesinde, maliyetler kuruluş birimleri ve seviyeleri arasında, uygulanan kural ve ilkelere dayalı olarak akar.</span><span class="sxs-lookup"><span data-stu-id="ce348-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="ce348-947">Her maliyet, maliyetlerin tahsisatı için en iyi değerlendirmeyi sağlayan bir tahsisat tabanı ile ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="ce348-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="ce348-948">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="ce348-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="ce348-949">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="ce348-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="ce348-950">Toplam</span><span class="sxs-lookup"><span data-stu-id="ce348-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="ce348-951">CC099</span><span class="sxs-lookup"><span data-stu-id="ce348-951">CC099</span></span></th>
<th><span data-ttu-id="ce348-952">CC001</span><span class="sxs-lookup"><span data-stu-id="ce348-952">CC001</span></span></th>
<th><span data-ttu-id="ce348-953">CC002</span><span class="sxs-lookup"><span data-stu-id="ce348-953">CC002</span></span></th>
<th><span data-ttu-id="ce348-954">CC003</span><span class="sxs-lookup"><span data-stu-id="ce348-954">CC003</span></span></th>
<th><span data-ttu-id="ce348-955">CC004</span><span class="sxs-lookup"><span data-stu-id="ce348-955">CC004</span></span></th>
<th><span data-ttu-id="ce348-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="ce348-956">Proj 1</span></span></th>
<th><span data-ttu-id="ce348-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="ce348-957">Proj 2</span></span></th>
<th><span data-ttu-id="ce348-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="ce348-958">Prod 1</span></span></th>
<th><span data-ttu-id="ce348-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="ce348-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="ce348-960">10001 Elektrik</span><span class="sxs-lookup"><span data-stu-id="ce348-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ce348-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="ce348-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ce348-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="ce348-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ce348-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="ce348-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ce348-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="ce348-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="ce348-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="ce348-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ce348-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="ce348-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ce348-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="ce348-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ce348-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="ce348-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="ce348-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="ce348-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="ce348-970">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="ce348-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ce348-971">0,00</span><span class="sxs-lookup"><span data-stu-id="ce348-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="ce348-972">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ce348-973">0,00</span><span class="sxs-lookup"><span data-stu-id="ce348-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ce348-974">0,00</span><span class="sxs-lookup"><span data-stu-id="ce348-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ce348-975">0,00</span><span class="sxs-lookup"><span data-stu-id="ce348-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ce348-976">0,00</span><span class="sxs-lookup"><span data-stu-id="ce348-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ce348-977">0,00</span><span class="sxs-lookup"><span data-stu-id="ce348-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="ce348-978">776.36</span><span class="sxs-lookup"><span data-stu-id="ce348-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ce348-979">223.64</span><span class="sxs-lookup"><span data-stu-id="ce348-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ce348-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="ce348-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="ce348-981">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="ce348-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ce348-982">000</span><span class="sxs-lookup"><span data-stu-id="ce348-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ce348-983">0,00</span><span class="sxs-lookup"><span data-stu-id="ce348-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ce348-984">0,00</span><span class="sxs-lookup"><span data-stu-id="ce348-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ce348-985">0,00</span><span class="sxs-lookup"><span data-stu-id="ce348-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ce348-986">0,00</span><span class="sxs-lookup"><span data-stu-id="ce348-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ce348-987">30.00</span><span class="sxs-lookup"><span data-stu-id="ce348-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ce348-988">10,00</span><span class="sxs-lookup"><span data-stu-id="ce348-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ce348-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="ce348-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ce348-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="ce348-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="ce348-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="ce348-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="ce348-992">Bu konu, birincil maliyet öğesi, 10001 Elektrik'in maliyet nesneleri arasında nasıl aktığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ce348-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="ce348-993">Bu nedenle, bu genel gider maliyeti kuruluşun en düşük seviyesine tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="ce348-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="ce348-994">Başka bir deyişle, maliyet en alt düzeydeki maliyet nesnelerine aittir.</span><span class="sxs-lookup"><span data-stu-id="ce348-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="ce348-995">Maliyetin, maliyet nesneleri arasında görsel bir akışına ihtiyacınız varsa, maliyetin akışını görselleştirmek için maliyet toplamı ilke kurallarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ce348-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="ce348-996">Daha fazla bilgi için [Maliyet yukarı yuvarlama](cost-rollup.md) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="ce348-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



