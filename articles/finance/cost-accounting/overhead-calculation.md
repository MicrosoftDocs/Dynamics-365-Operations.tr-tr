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
ms.openlocfilehash: 954e0669c3d24bcc20fe667c22b7dcc367aba1e7
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770816"
---
# <a name="overhead-calculation"></a><span data-ttu-id="a8d33-103">Genel gider hesaplaması</span><span class="sxs-lookup"><span data-stu-id="a8d33-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a8d33-104">Bu konu, genel gider maliyetlerinin hesaplanması için tipik işlemleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="a8d33-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="a8d33-105">Terim tanımı</span><span class="sxs-lookup"><span data-stu-id="a8d33-105">Term definition</span></span>
---------------

<span data-ttu-id="a8d33-106">Genel gider maliyetleri bir işletmenin çalışması için normalde uygulanan, ancak doğrudan herhangi bir özel iş, faaliyet, ürün veya hizmete ilişkilendirilmemiş olan maliyetlerdir.</span><span class="sxs-lookup"><span data-stu-id="a8d33-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="a8d33-107">Genel gider maliyetleri kar sağlama faaliyetlerinin oluşturulması için kritik destek sağlar.</span><span class="sxs-lookup"><span data-stu-id="a8d33-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="a8d33-108">Aşağıda bazı genel gider örnekleri verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="a8d33-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="a8d33-109">Kira</span><span class="sxs-lookup"><span data-stu-id="a8d33-109">Rent</span></span>
-   <span data-ttu-id="a8d33-110">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-110">Electricity</span></span>
-   <span data-ttu-id="a8d33-111">Yönetim maaşları</span><span class="sxs-lookup"><span data-stu-id="a8d33-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="a8d33-112">Genel gider hesaplaması genel bakış</span><span class="sxs-lookup"><span data-stu-id="a8d33-112">Overhead calculation overview</span></span>
<span data-ttu-id="a8d33-113">Genel gider hesaplama, maliyet muhasebesi ilkelerini doğru sırayla çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="a8d33-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="a8d33-114">Maliyet muhasebesi ilkeleri değiştiyse veya belirli hatalar algılandıysa, genel gider hesaplamasını aynı mali dönem için birden fazla kez yürütebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a8d33-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="a8d33-115">Her genel gider hesaplaması depolanır ve önceki sürümlerdeki hesaplamaları kıyaslamanıza olanak sağlayan, benzersiz bir sürüm kimliğine sahip olur.</span><span class="sxs-lookup"><span data-stu-id="a8d33-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="a8d33-116">Genel gider hesaplamasının oluşturduğu maliyet girişleri bir muhasebe tarihi alır.</span><span class="sxs-lookup"><span data-stu-id="a8d33-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="a8d33-117">Bu muhasebe tarihi, hesaplamada kullanılan mali dönemin bitiş tarihiyle eşleşir.</span><span class="sxs-lookup"><span data-stu-id="a8d33-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="a8d33-118">Benzersiz sürüm kimliği aşağıdaki öğelerden oluşur:</span><span class="sxs-lookup"><span data-stu-id="a8d33-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="a8d33-119">Sürüm türü</span><span class="sxs-lookup"><span data-stu-id="a8d33-119">Version type</span></span>
-   <span data-ttu-id="a8d33-120">Tarih ve saat</span><span class="sxs-lookup"><span data-stu-id="a8d33-120">Date and time</span></span>
-   <span data-ttu-id="a8d33-121">Maliyet muhasebesi defteri</span><span class="sxs-lookup"><span data-stu-id="a8d33-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="a8d33-122">Mali yıl</span><span class="sxs-lookup"><span data-stu-id="a8d33-122">Fiscal year</span></span>
-   <span data-ttu-id="a8d33-123">Mali dönem</span><span class="sxs-lookup"><span data-stu-id="a8d33-123">Fiscal period</span></span>

<span data-ttu-id="a8d33-124">Genel gider hesaplama, sürümden bağımsız olarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="a8d33-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="a8d33-125">Bu nedenle, Gerçek sürümden önce Bütçe sürümünü hesaplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a8d33-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="a8d33-126">Genel gider hesaplama dört adımdan oluşur, aşağıdaki çizimde gösterildiği gibi.</span><span class="sxs-lookup"><span data-stu-id="a8d33-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="a8d33-127">Her adımda, günlük girişleri olan bir günlük başlığı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="a8d33-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="a8d33-128">Bu günlük başlığı, her hesaplama adımı için giriş verilerini tutar.</span><span class="sxs-lookup"><span data-stu-id="a8d33-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="a8d33-129">İlkeler ve kurallar her günlük satırına uygulanır ve maliyet girişleri çıkış olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="a8d33-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="a8d33-130">Bu nedenle, her zaman tam izlenebilirliğe sahip olursunuz.</span><span class="sxs-lookup"><span data-stu-id="a8d33-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="a8d33-131">[![Genel gider hesaplaması](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="a8d33-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="a8d33-132">Elektrik genel gideri maliyetini hesapla ve tahsis et</span><span class="sxs-lookup"><span data-stu-id="a8d33-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="a8d33-133">Mali muhasebede, elektrik gibi bazı maliyetler peşin ödeme olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="a8d33-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="a8d33-134">Bu nedenle, Maliyet muhasebesi için ayrıntılı yönetim bilgiler sağlanmaz.</span><span class="sxs-lookup"><span data-stu-id="a8d33-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="a8d33-135">Maliyet muhasebesinde doğru yönetimsel bilgileri tüm yönetim birim ve düzeylerinde sağlamak için, maliyetlerin kuruluş birimleri arasında akması gerekir.</span><span class="sxs-lookup"><span data-stu-id="a8d33-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="a8d33-136">Bu akış, tüketimin doğru bir kaydına ya da adil bir değerlendirmeye dayanıyor olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a8d33-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="a8d33-137">Genel muhasebede, bir elektrik maliyeti aşağıdaki tabloda gösterildiği gibi deftere nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="a8d33-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a8d33-138">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="a8d33-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a8d33-139">Maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="a8d33-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="a8d33-140">Ana hesap</span><span class="sxs-lookup"><span data-stu-id="a8d33-140">Main account</span></span></th>
<th><span data-ttu-id="a8d33-141">Muhasebe para birimi cinsinden tutar</span><span class="sxs-lookup"><span data-stu-id="a8d33-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a8d33-142">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="a8d33-143">CC099</span><span class="sxs-lookup"><span data-stu-id="a8d33-143">CC099</span></span></td>
<td><span data-ttu-id="a8d33-144">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="a8d33-144">Default cost center</span></span></td>
<td><span data-ttu-id="a8d33-145">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-145">10001</span></span></td>
<td><span data-ttu-id="a8d33-146">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-146">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="a8d33-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="a8d33-148">Adım 1: Maliyet davranışı hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="a8d33-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="a8d33-149">Varsayılan olarak, maliyeti girişleri kaynak veriden içeri alındığında, Maliyet muhasebesinde **Sınıflandırılmamış** maliyet davranışı sınıflandırmasını alırlar.</span><span class="sxs-lookup"><span data-stu-id="a8d33-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="a8d33-150">Maliyet davranışı ilke kuralları ekleyerek, maliyet girişlerini **Sabit maliyet** veya **Değişken maliyet** olarak yeniden sınıflandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a8d33-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="a8d33-151">Maliyet davranış kuralını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="a8d33-151">Define the cost behavior rule</span></span>

<span data-ttu-id="a8d33-152">Bazı durumlarda, sabit bir ücret maliyet parçasıdır ve kalan maliyet, tüketime dayanır.</span><span class="sxs-lookup"><span data-stu-id="a8d33-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="a8d33-153">Elektrik faturaları genellikle bu tanıma uyar.</span><span class="sxs-lookup"><span data-stu-id="a8d33-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="a8d33-154">Belirli bir sabit ücret ödedikten sonra, kilovat saatlik (Kwh) tüketim başına ödeme yaparsınız.</span><span class="sxs-lookup"><span data-stu-id="a8d33-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="a8d33-155">Örneğin, sabit maliyet masrafı 1.000,00 ise, maliyet davranışı kural nasıl tanımlanır:</span><span class="sxs-lookup"><span data-stu-id="a8d33-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="a8d33-156">Sabit tutar 1.000,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="a8d33-157">0 &lt;= 1.000,00 = Sabit</span><span class="sxs-lookup"><span data-stu-id="a8d33-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="a8d33-158">1000,01 &lt; N = Değişken</span><span class="sxs-lookup"><span data-stu-id="a8d33-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="a8d33-159">Günlük</span><span class="sxs-lookup"><span data-stu-id="a8d33-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a8d33-160">Günlük</span><span class="sxs-lookup"><span data-stu-id="a8d33-160">Journal</span></span></th>
<th><span data-ttu-id="a8d33-161">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="a8d33-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="a8d33-162">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="a8d33-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="a8d33-163">Sürüm</span><span class="sxs-lookup"><span data-stu-id="a8d33-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a8d33-164">00001</span><span class="sxs-lookup"><span data-stu-id="a8d33-164">00001</span></span></td>
<td><span data-ttu-id="a8d33-165">Maliyet davranışı hesaplama günlüğü</span><span class="sxs-lookup"><span data-stu-id="a8d33-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="a8d33-166">Mali</span><span class="sxs-lookup"><span data-stu-id="a8d33-166">Fiscal</span></span></td>
<td><span data-ttu-id="a8d33-167">2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-167">2017</span></span></td>
<td><span data-ttu-id="a8d33-168">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-168">Period 1</span></span></td>
<td><span data-ttu-id="a8d33-169">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="a8d33-170">Günlük girişleri (Maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="a8d33-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a8d33-171">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="a8d33-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a8d33-172">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="a8d33-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a8d33-173">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="a8d33-173">Cost element</span></span></th>
<th><span data-ttu-id="a8d33-174">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="a8d33-174">Cost behavior</span></span></th>
<th><span data-ttu-id="a8d33-175">Tutar</span><span class="sxs-lookup"><span data-stu-id="a8d33-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a8d33-176">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="a8d33-177">CC099</span><span class="sxs-lookup"><span data-stu-id="a8d33-177">CC099</span></span></td>
<td><span data-ttu-id="a8d33-178">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="a8d33-178">Default cost center</span></span></td>
<td><span data-ttu-id="a8d33-179">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-179">10001</span></span></td>
<td><span data-ttu-id="a8d33-180">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-180">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-181">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="a8d33-181">Unclassified</span></span></td>
<td><span data-ttu-id="a8d33-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="a8d33-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="a8d33-183">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="a8d33-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a8d33-184">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="a8d33-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a8d33-185">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="a8d33-185">Cost element</span></span></th>
<th><span data-ttu-id="a8d33-186">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="a8d33-186">Cost behavior</span></span></th>
<th><span data-ttu-id="a8d33-187">Tutar</span><span class="sxs-lookup"><span data-stu-id="a8d33-187">Amount</span></span></th>
<th><span data-ttu-id="a8d33-188">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="a8d33-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a8d33-189">CC099</span><span class="sxs-lookup"><span data-stu-id="a8d33-189">CC099</span></span></td>
<td><span data-ttu-id="a8d33-190">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="a8d33-190">Default cost center</span></span></td>
<td><span data-ttu-id="a8d33-191">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-191">10001</span></span></td>
<td><span data-ttu-id="a8d33-192">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-192">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-193">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="a8d33-193">Unclassified</span></span></td>
<td><span data-ttu-id="a8d33-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="a8d33-194">10,000.00</span></span></td>
<td><span data-ttu-id="a8d33-195">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-196">CC099</span><span class="sxs-lookup"><span data-stu-id="a8d33-196">CC099</span></span></td>
<td><span data-ttu-id="a8d33-197">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="a8d33-197">Default cost center</span></span></td>
<td><span data-ttu-id="a8d33-198">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-198">10001</span></span></td>
<td><span data-ttu-id="a8d33-199">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-199">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-200">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="a8d33-200">Unclassified</span></span></td>
<td><span data-ttu-id="a8d33-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-201">-10,000.00</span></span></td>
<td><span data-ttu-id="a8d33-202">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-203">CC099</span><span class="sxs-lookup"><span data-stu-id="a8d33-203">CC099</span></span></td>
<td><span data-ttu-id="a8d33-204">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="a8d33-204">Default cost center</span></span></td>
<td><span data-ttu-id="a8d33-205">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-205">10001</span></span></td>
<td><span data-ttu-id="a8d33-206">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-206">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-207">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-207">Fixed cost</span></span></td>
<td><span data-ttu-id="a8d33-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-208">1,000.00</span></span></td>
<td><span data-ttu-id="a8d33-209">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-210">CC099</span><span class="sxs-lookup"><span data-stu-id="a8d33-210">CC099</span></span></td>
<td><span data-ttu-id="a8d33-211">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="a8d33-211">Default cost center</span></span></td>
<td><span data-ttu-id="a8d33-212">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-212">10001</span></span></td>
<td><span data-ttu-id="a8d33-213">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-213">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-214">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-214">Variable cost</span></span></td>
<td><span data-ttu-id="a8d33-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="a8d33-215">9,000.00</span></span></td>
<td><span data-ttu-id="a8d33-216">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a8d33-217">Daha fazla bilgi için bkz. [Maliyet davranışı ilkesi oluşturma ve bir maliyet kontrol birimine atama](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="a8d33-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="a8d33-218">Adım 2: Maliyet dağıtımı hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="a8d33-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="a8d33-219">Maliyet dağıtımı, bir nesneden bir veya daha fazlasına ilgili tahsisat tabanı uygulayarak maliyeti yeniden dağıtmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a8d33-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="a8d33-220">Maliyet dağıtımı ve maliyet tahsisatı, maliyet dağıtımının her zaman orijinal maliyetin birincil maliyet öğesinde bulunmasıyla farklılık gösterir.</span><span class="sxs-lookup"><span data-stu-id="a8d33-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="a8d33-221">Maliyet dağıtım kuralını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="a8d33-221">Define the cost distribution rule</span></span>

<span data-ttu-id="a8d33-222">Mali muhasebede, elektrik maliyetleri çoğu zaman peşin ödeme olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="a8d33-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="a8d33-223">Maliyet muhasebesinde ise bu yöntem yeterince ayrıntılı değildir.</span><span class="sxs-lookup"><span data-stu-id="a8d33-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="a8d33-224">Değişken maliyet, maliyet nesnelerine tek tek, adil bir temele dayanarak dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a8d33-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="a8d33-225">En mantıklı tahsisat, elektrik kullanımını (Kwh) temel alarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="a8d33-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="a8d33-226">Elektrik adına sahip, istatistiksel bir boyut üyesi oluşturulur ve elektrik tüketimi kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="a8d33-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="a8d33-227">Varsayıla olarak, tüm istatistiksel boyut üyeleri tahsisat tabanları olarak kullanılabilir hale gelir.</span><span class="sxs-lookup"><span data-stu-id="a8d33-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a8d33-228">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="a8d33-228">Cost object</span></span></th>
<th><span data-ttu-id="a8d33-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="a8d33-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a8d33-230">CC001</span><span class="sxs-lookup"><span data-stu-id="a8d33-230">CC001</span></span></td>
<td><span data-ttu-id="a8d33-231">İK</span><span class="sxs-lookup"><span data-stu-id="a8d33-231">HR</span></span></td>
<td><span data-ttu-id="a8d33-232">1.000</span><span class="sxs-lookup"><span data-stu-id="a8d33-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-233">CC002</span><span class="sxs-lookup"><span data-stu-id="a8d33-233">CC002</span></span></td>
<td><span data-ttu-id="a8d33-234">Finans</span><span class="sxs-lookup"><span data-stu-id="a8d33-234">Finance</span></span></td>
<td><span data-ttu-id="a8d33-235">6,000</span><span class="sxs-lookup"><span data-stu-id="a8d33-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-236">CC003</span><span class="sxs-lookup"><span data-stu-id="a8d33-236">CC003</span></span></td>
<td><span data-ttu-id="a8d33-237">Montaj</span><span class="sxs-lookup"><span data-stu-id="a8d33-237">Assembly</span></span></td>
<td><span data-ttu-id="a8d33-238">0</span><span class="sxs-lookup"><span data-stu-id="a8d33-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a8d33-239">Aşağıdaki tablo, elektrik tüketiminin değişken maliyetler için bir tahsisat tabanlı olarak uygulandığındaki sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="a8d33-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a8d33-240">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="a8d33-240">Cost object</span></span></th>
<th><span data-ttu-id="a8d33-241">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="a8d33-241">Magnitude</span></span></th>
<th><span data-ttu-id="a8d33-242">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="a8d33-242">Allocation factor</span></span></th>
<th><span data-ttu-id="a8d33-243">Tutar</span><span class="sxs-lookup"><span data-stu-id="a8d33-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a8d33-244">CC001</span><span class="sxs-lookup"><span data-stu-id="a8d33-244">CC001</span></span></td>
<td><span data-ttu-id="a8d33-245">İK</span><span class="sxs-lookup"><span data-stu-id="a8d33-245">HR</span></span></td>
<td><span data-ttu-id="a8d33-246">1.000</span><span class="sxs-lookup"><span data-stu-id="a8d33-246">1,000</span></span></td>
<td><span data-ttu-id="a8d33-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="a8d33-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="a8d33-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-249">CC002</span><span class="sxs-lookup"><span data-stu-id="a8d33-249">CC002</span></span></td>
<td><span data-ttu-id="a8d33-250">Finans</span><span class="sxs-lookup"><span data-stu-id="a8d33-250">Finance</span></span></td>
<td><span data-ttu-id="a8d33-251">6,000</span><span class="sxs-lookup"><span data-stu-id="a8d33-251">6,000</span></span></td>
<td><span data-ttu-id="a8d33-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="a8d33-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="a8d33-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-254">CC003</span><span class="sxs-lookup"><span data-stu-id="a8d33-254">CC003</span></span></td>
<td><span data-ttu-id="a8d33-255">Montaj</span><span class="sxs-lookup"><span data-stu-id="a8d33-255">Assembly</span></span></td>
<td><span data-ttu-id="a8d33-256">0</span><span class="sxs-lookup"><span data-stu-id="a8d33-256">0</span></span></td>
<td><span data-ttu-id="a8d33-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="a8d33-258">0,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a8d33-259">Sabit maliyet, elektrik tüketmiş olan tekil maliyet nesnelerine eşit miktarda dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a8d33-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="a8d33-260">Bu sonuca, Elektrik istatistiksel boyut öğesini bir formül tahsisat tabanında kullanarak ulaşabilirsiniz: (Elektrik &gt; 0,00) Aşağıdaki tablo, elektrik tüketimi değişken maliyetler için bir tahsisat tabanı olarak kullanıldığında ortaya çıkan sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="a8d33-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a8d33-261">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="a8d33-261">Cost object</span></span></th>
<th><span data-ttu-id="a8d33-262">Formül</span><span class="sxs-lookup"><span data-stu-id="a8d33-262">Formula</span></span></th>
<th><span data-ttu-id="a8d33-263">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="a8d33-263">Magnitude</span></span></th>
<th><span data-ttu-id="a8d33-264">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="a8d33-264">Allocation factor</span></span></th>
<th><span data-ttu-id="a8d33-265">Tutar</span><span class="sxs-lookup"><span data-stu-id="a8d33-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a8d33-266">CC001</span><span class="sxs-lookup"><span data-stu-id="a8d33-266">CC001</span></span></td>
<td><span data-ttu-id="a8d33-267">İK</span><span class="sxs-lookup"><span data-stu-id="a8d33-267">HR</span></span></td>
<td><span data-ttu-id="a8d33-268">(1,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="a8d33-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="a8d33-269">1</span><span class="sxs-lookup"><span data-stu-id="a8d33-269">1</span></span></td>
<td><span data-ttu-id="a8d33-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="a8d33-271">500.00</span><span class="sxs-lookup"><span data-stu-id="a8d33-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-272">CC002</span><span class="sxs-lookup"><span data-stu-id="a8d33-272">CC002</span></span></td>
<td><span data-ttu-id="a8d33-273">Finans</span><span class="sxs-lookup"><span data-stu-id="a8d33-273">Finance</span></span></td>
<td><span data-ttu-id="a8d33-274">(6,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="a8d33-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="a8d33-275">1</span><span class="sxs-lookup"><span data-stu-id="a8d33-275">1</span></span></td>
<td><span data-ttu-id="a8d33-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="a8d33-277">500.00</span><span class="sxs-lookup"><span data-stu-id="a8d33-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-278">CC003</span><span class="sxs-lookup"><span data-stu-id="a8d33-278">CC003</span></span></td>
<td><span data-ttu-id="a8d33-279">Montaj</span><span class="sxs-lookup"><span data-stu-id="a8d33-279">Assembly</span></span></td>
<td><span data-ttu-id="a8d33-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="a8d33-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="a8d33-281">0</span><span class="sxs-lookup"><span data-stu-id="a8d33-281">0</span></span></td>
<td><span data-ttu-id="a8d33-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="a8d33-283">0,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="a8d33-284">Günlük</span><span class="sxs-lookup"><span data-stu-id="a8d33-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a8d33-285">Günlük</span><span class="sxs-lookup"><span data-stu-id="a8d33-285">Journal</span></span></th>
<th><span data-ttu-id="a8d33-286">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="a8d33-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="a8d33-287">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="a8d33-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="a8d33-288">Sürüm</span><span class="sxs-lookup"><span data-stu-id="a8d33-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a8d33-289">00002</span><span class="sxs-lookup"><span data-stu-id="a8d33-289">00002</span></span></td>
<td><span data-ttu-id="a8d33-290">Maliyet dağıtımı hesaplama günlüğü</span><span class="sxs-lookup"><span data-stu-id="a8d33-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="a8d33-291">Mali</span><span class="sxs-lookup"><span data-stu-id="a8d33-291">Fiscal</span></span></td>
<td><span data-ttu-id="a8d33-292">2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-292">2017</span></span></td>
<td><span data-ttu-id="a8d33-293">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-293">Period 1</span></span></td>
<td><span data-ttu-id="a8d33-294">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="a8d33-295">Günlük girişleri (Maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="a8d33-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a8d33-296">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="a8d33-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a8d33-297">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="a8d33-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a8d33-298">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="a8d33-298">Cost element</span></span></th>
<th><span data-ttu-id="a8d33-299">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="a8d33-299">Cost behavior</span></span></th>
<th><span data-ttu-id="a8d33-300">Tutar</span><span class="sxs-lookup"><span data-stu-id="a8d33-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a8d33-301">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="a8d33-302">CC099</span><span class="sxs-lookup"><span data-stu-id="a8d33-302">CC099</span></span></td>
<td><span data-ttu-id="a8d33-303">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="a8d33-303">Default cost center</span></span></td>
<td><span data-ttu-id="a8d33-304">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-304">10001</span></span></td>
<td><span data-ttu-id="a8d33-305">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-305">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-306">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-306">Fixed cost</span></span></td>
<td><span data-ttu-id="a8d33-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-308">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="a8d33-309">CC099</span><span class="sxs-lookup"><span data-stu-id="a8d33-309">CC099</span></span></td>
<td><span data-ttu-id="a8d33-310">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="a8d33-310">Default cost center</span></span></td>
<td><span data-ttu-id="a8d33-311">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-311">10001</span></span></td>
<td><span data-ttu-id="a8d33-312">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-312">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-313">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-313">Variable cost</span></span></td>
<td><span data-ttu-id="a8d33-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="a8d33-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="a8d33-315">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="a8d33-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a8d33-316">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="a8d33-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a8d33-317">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="a8d33-317">Cost element</span></span></th>
<th><span data-ttu-id="a8d33-318">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="a8d33-318">Cost behavior</span></span></th>
<th><span data-ttu-id="a8d33-319">Tutar</span><span class="sxs-lookup"><span data-stu-id="a8d33-319">Amount</span></span></th>
<th><span data-ttu-id="a8d33-320">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="a8d33-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a8d33-321">CC099</span><span class="sxs-lookup"><span data-stu-id="a8d33-321">CC099</span></span></td>
<td><span data-ttu-id="a8d33-322">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="a8d33-322">Default cost center</span></span></td>
<td><span data-ttu-id="a8d33-323">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-323">10001</span></span></td>
<td><span data-ttu-id="a8d33-324">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-324">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-325">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-325">Fixed cost</span></span></td>
<td><span data-ttu-id="a8d33-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-326">-1,000.00</span></span></td>
<td><span data-ttu-id="a8d33-327">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-328">CC001</span><span class="sxs-lookup"><span data-stu-id="a8d33-328">CC001</span></span></td>
<td><span data-ttu-id="a8d33-329">İK</span><span class="sxs-lookup"><span data-stu-id="a8d33-329">HR</span></span></td>
<td><span data-ttu-id="a8d33-330">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-330">10001</span></span></td>
<td><span data-ttu-id="a8d33-331">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-331">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-332">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-332">Fixed cost</span></span></td>
<td><span data-ttu-id="a8d33-333">500.00</span><span class="sxs-lookup"><span data-stu-id="a8d33-333">500.00</span></span></td>
<td><span data-ttu-id="a8d33-334">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-335">CC002</span><span class="sxs-lookup"><span data-stu-id="a8d33-335">CC002</span></span></td>
<td><span data-ttu-id="a8d33-336">Finans</span><span class="sxs-lookup"><span data-stu-id="a8d33-336">Finance</span></span></td>
<td><span data-ttu-id="a8d33-337">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-337">10001</span></span></td>
<td><span data-ttu-id="a8d33-338">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-338">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-339">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-339">Fixed cost</span></span></td>
<td><span data-ttu-id="a8d33-340">500.00</span><span class="sxs-lookup"><span data-stu-id="a8d33-340">500.00</span></span></td>
<td><span data-ttu-id="a8d33-341">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-342">CC099</span><span class="sxs-lookup"><span data-stu-id="a8d33-342">CC099</span></span></td>
<td><span data-ttu-id="a8d33-343">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="a8d33-343">Default cost center</span></span></td>
<td><span data-ttu-id="a8d33-344">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-344">10001</span></span></td>
<td><span data-ttu-id="a8d33-345">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-345">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-346">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-346">Variable cost</span></span></td>
<td><span data-ttu-id="a8d33-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-347">-9,000.00</span></span></td>
<td><span data-ttu-id="a8d33-348">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-349">CC001</span><span class="sxs-lookup"><span data-stu-id="a8d33-349">CC001</span></span></td>
<td><span data-ttu-id="a8d33-350">İK</span><span class="sxs-lookup"><span data-stu-id="a8d33-350">HR</span></span></td>
<td><span data-ttu-id="a8d33-351">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-351">10001</span></span></td>
<td><span data-ttu-id="a8d33-352">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-352">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-353">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-353">Variable cost</span></span></td>
<td><span data-ttu-id="a8d33-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="a8d33-354">1,285.71</span></span></td>
<td><span data-ttu-id="a8d33-355">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-356">CC002</span><span class="sxs-lookup"><span data-stu-id="a8d33-356">CC002</span></span></td>
<td><span data-ttu-id="a8d33-357">Finans</span><span class="sxs-lookup"><span data-stu-id="a8d33-357">Finance</span></span></td>
<td><span data-ttu-id="a8d33-358">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-358">10001</span></span></td>
<td><span data-ttu-id="a8d33-359">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-359">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-360">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-360">Variable cost</span></span></td>
<td><span data-ttu-id="a8d33-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="a8d33-361">7,714.29</span></span></td>
<td><span data-ttu-id="a8d33-362">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a8d33-363">Daha fazla bilgi için bkz. [Maliyet dağıtımı ilkesi oluşturma ve bir maliyet kontrol birimine atama](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="a8d33-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="a8d33-364">Adım 3: Genel gider oranı hesaplama işlemi</span><span class="sxs-lookup"><span data-stu-id="a8d33-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="a8d33-365">Genel gider oranı, bir veya birden fazla belirli maliyet nesnesine masraf yüklemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a8d33-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="a8d33-366">Masraf, önceden belirlenmiş maliyet oranına ve tahsisat tabanından hesaplanan büyüklüğe dayanır.</span><span class="sxs-lookup"><span data-stu-id="a8d33-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="a8d33-367">Genel gider oranını tanımlama</span><span class="sxs-lookup"><span data-stu-id="a8d33-367">Define the overhead rate</span></span>

<span data-ttu-id="a8d33-368">Maliyet nesnesi CC001 HR, bir dizi dahili projeye katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="a8d33-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="a8d33-369">HR projeleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="a8d33-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a8d33-370">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="a8d33-370">Cost object</span></span></th>
<th><span data-ttu-id="a8d33-371">Saatler</span><span class="sxs-lookup"><span data-stu-id="a8d33-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a8d33-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-372">Proj 1</span></span></td>
<td><span data-ttu-id="a8d33-373">Proje 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-373">Project 1</span></span></td>
<td><span data-ttu-id="a8d33-374">3</span><span class="sxs-lookup"><span data-stu-id="a8d33-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="a8d33-375">Proj 2</span></span></td>
<td><span data-ttu-id="a8d33-376">Proje 2</span><span class="sxs-lookup"><span data-stu-id="a8d33-376">Project 2</span></span></td>
<td><span data-ttu-id="a8d33-377">1</span><span class="sxs-lookup"><span data-stu-id="a8d33-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a8d33-378">Maliyet projeleri dağıtımı için bir önceden belirlenmiş maliyet oranı tanımlandı.</span><span class="sxs-lookup"><span data-stu-id="a8d33-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a8d33-379">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="a8d33-379">Cost object</span></span></th>
<th><span data-ttu-id="a8d33-380">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="a8d33-380">Cost element</span></span></th>
<th><span data-ttu-id="a8d33-381">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="a8d33-381">Cost behavior</span></span></th>
<th><span data-ttu-id="a8d33-382">Birimler</span><span class="sxs-lookup"><span data-stu-id="a8d33-382">Units</span></span></th>
<th><span data-ttu-id="a8d33-383">Ücret</span><span class="sxs-lookup"><span data-stu-id="a8d33-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a8d33-384">CC001</span><span class="sxs-lookup"><span data-stu-id="a8d33-384">CC001</span></span></td>
<td><span data-ttu-id="a8d33-385">İK</span><span class="sxs-lookup"><span data-stu-id="a8d33-385">HR</span></span></td>
<td><span data-ttu-id="a8d33-386">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-386">10001</span></span></td>
<td><span data-ttu-id="a8d33-387">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-387">Variable cost</span></span></td>
<td><span data-ttu-id="a8d33-388">1</span><span class="sxs-lookup"><span data-stu-id="a8d33-388">1</span></span></td>
<td><span data-ttu-id="a8d33-389">10</span><span class="sxs-lookup"><span data-stu-id="a8d33-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a8d33-390">Aşağıdaki tablo, HR projeleri bir tahsisat tabanı olarak uygulandığındaki sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="a8d33-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a8d33-391">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="a8d33-391">Cost object</span></span></th>
<th><span data-ttu-id="a8d33-392">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="a8d33-392">Magnitude</span></span></th>
<th><span data-ttu-id="a8d33-393">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="a8d33-393">Cost element</span></span></th>
<th><span data-ttu-id="a8d33-394">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="a8d33-394">Allocation factor</span></span></th>
<th><span data-ttu-id="a8d33-395">Tutar</span><span class="sxs-lookup"><span data-stu-id="a8d33-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a8d33-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-396">Proj 1</span></span></td>
<td><span data-ttu-id="a8d33-397">Proje 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-397">Project 1</span></span></td>
<td><span data-ttu-id="a8d33-398">3</span><span class="sxs-lookup"><span data-stu-id="a8d33-398">3</span></span></td>
<td><span data-ttu-id="a8d33-399">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-399">10001</span></span></td>
<td><span data-ttu-id="a8d33-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="a8d33-401">30.00</span><span class="sxs-lookup"><span data-stu-id="a8d33-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="a8d33-402">Proj 2</span></span></td>
<td><span data-ttu-id="a8d33-403">Proje 2</span><span class="sxs-lookup"><span data-stu-id="a8d33-403">Project 2</span></span></td>
<td><span data-ttu-id="a8d33-404">1</span><span class="sxs-lookup"><span data-stu-id="a8d33-404">1</span></span></td>
<td><span data-ttu-id="a8d33-405">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-405">10001</span></span></td>
<td><span data-ttu-id="a8d33-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="a8d33-407">10,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="a8d33-408">Günlük</span><span class="sxs-lookup"><span data-stu-id="a8d33-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a8d33-409">Günlük</span><span class="sxs-lookup"><span data-stu-id="a8d33-409">Journal</span></span></th>
<th><span data-ttu-id="a8d33-410">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="a8d33-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="a8d33-411">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="a8d33-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="a8d33-412">Sürüm</span><span class="sxs-lookup"><span data-stu-id="a8d33-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a8d33-413">00003</span><span class="sxs-lookup"><span data-stu-id="a8d33-413">00003</span></span></td>
<td><span data-ttu-id="a8d33-414">Genel gider oranı hesaplaması günlüğü</span><span class="sxs-lookup"><span data-stu-id="a8d33-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="a8d33-415">Mali</span><span class="sxs-lookup"><span data-stu-id="a8d33-415">Fiscal</span></span></td>
<td><span data-ttu-id="a8d33-416">2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-416">2017</span></span></td>
<td><span data-ttu-id="a8d33-417">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-417">Period 1</span></span></td>
<td><span data-ttu-id="a8d33-418">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="a8d33-419">Günlük girişleri (Genel gider oranı hesaplaması için günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="a8d33-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a8d33-420">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="a8d33-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a8d33-421">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="a8d33-421">Cost object</span></span></th>
<th><span data-ttu-id="a8d33-422">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="a8d33-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a8d33-423">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="a8d33-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-424">Proj 1</span></span></td>
<td><span data-ttu-id="a8d33-425">Dahili Proj 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="a8d33-426">3,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-427">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="a8d33-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="a8d33-428">Proj 2</span></span></td>
<td><span data-ttu-id="a8d33-429">Dahili Proj 2</span><span class="sxs-lookup"><span data-stu-id="a8d33-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="a8d33-430">1.00</span><span class="sxs-lookup"><span data-stu-id="a8d33-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="a8d33-431">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="a8d33-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a8d33-432">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="a8d33-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a8d33-433">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="a8d33-433">Cost element</span></span></th>
<th><span data-ttu-id="a8d33-434">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="a8d33-434">Cost behavior</span></span></th>
<th><span data-ttu-id="a8d33-435">Tutar</span><span class="sxs-lookup"><span data-stu-id="a8d33-435">Amount</span></span></th>
<th><span data-ttu-id="a8d33-436">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="a8d33-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a8d33-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="a8d33-437">CC0001</span></span></td>
<td><span data-ttu-id="a8d33-438">İK</span><span class="sxs-lookup"><span data-stu-id="a8d33-438">HR</span></span></td>
<td><span data-ttu-id="a8d33-439">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-439">10001</span></span></td>
<td><span data-ttu-id="a8d33-440">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-440">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-441">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-441">Variable cost</span></span></td>
<td><span data-ttu-id="a8d33-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-442">-30.00</span></span></td>
<td><span data-ttu-id="a8d33-443">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-444">Proj 1</span></span></td>
<td><span data-ttu-id="a8d33-445">Dahili Proj 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="a8d33-446">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-446">10001</span></span></td>
<td><span data-ttu-id="a8d33-447">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-447">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-448">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-448">Variable cost</span></span></td>
<td><span data-ttu-id="a8d33-449">30.00</span><span class="sxs-lookup"><span data-stu-id="a8d33-449">30.00</span></span></td>
<td><span data-ttu-id="a8d33-450">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-451">CC001</span><span class="sxs-lookup"><span data-stu-id="a8d33-451">CC001</span></span></td>
<td><span data-ttu-id="a8d33-452">İK</span><span class="sxs-lookup"><span data-stu-id="a8d33-452">HR</span></span></td>
<td><span data-ttu-id="a8d33-453">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-453">10001</span></span></td>
<td><span data-ttu-id="a8d33-454">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-454">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-455">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-455">Variable cost</span></span></td>
<td><span data-ttu-id="a8d33-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-456">-10.00</span></span></td>
<td><span data-ttu-id="a8d33-457">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="a8d33-458">Proj 2</span></span></td>
<td><span data-ttu-id="a8d33-459">Dahili Proj 2</span><span class="sxs-lookup"><span data-stu-id="a8d33-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="a8d33-460">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-460">10001</span></span></td>
<td><span data-ttu-id="a8d33-461">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-461">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-462">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-462">Variable cost</span></span></td>
<td><span data-ttu-id="a8d33-463">10,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-463">10.00</span></span></td>
<td><span data-ttu-id="a8d33-464">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a8d33-465">Daha fazla bilgi için [Genel gider hesaplaması gerçekleştir](cost-rollup.md#perform-overhead-calculation) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="a8d33-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="a8d33-466">Adım 4: Maliyet tahsisat hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="a8d33-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="a8d33-467">Tahsisat, bir tahsisat tabanı kullanarak bir maliyet nesnesinin diğer maliyet nesnelerine bakiyesini tahsis eder.</span><span class="sxs-lookup"><span data-stu-id="a8d33-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="a8d33-468">Finance karşılıklı tahsisat yöntemini desteklemektedir.</span><span class="sxs-lookup"><span data-stu-id="a8d33-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="a8d33-469">Karşılıklı tahsisat yönteminde, yardımcı maliyet nesnelerinin değiştiği karşılıklı hizmetler tümüyle tanınır.</span><span class="sxs-lookup"><span data-stu-id="a8d33-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="a8d33-470">Sistem, tahsisatların doğru gerçekleştireceği sırayı otomatik olarak belirler.</span><span class="sxs-lookup"><span data-stu-id="a8d33-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="a8d33-471">Bir maliyet nesnesinin bakiyesi tek bir tahsisat tabanı tarafından tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="a8d33-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="a8d33-472">Yeni maliyet nesnesi boyutları arasındaki tahsisatlar ve onların üyeleri desteklenir.</span><span class="sxs-lookup"><span data-stu-id="a8d33-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="a8d33-473">Tahsisatın sırası, maliyet kontrol birimi tarafından kontrol edilir.</span><span class="sxs-lookup"><span data-stu-id="a8d33-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="a8d33-474">[![Karşılıklı yöntemi](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="a8d33-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="a8d33-475">Maliyet tahsisatını tanımla</span><span class="sxs-lookup"><span data-stu-id="a8d33-475">Define the cost allocation</span></span>

<span data-ttu-id="a8d33-476">Bir maliyetin akışını nasıl izleyeceğinize dair basit bir örnek aşağıda verilmiştir,</span><span class="sxs-lookup"><span data-stu-id="a8d33-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="a8d33-477">Maliyet nesnesi CC001 HR, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="a8d33-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="a8d33-478">HR hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="a8d33-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a8d33-479">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="a8d33-479">Cost object</span></span></th>
<th><span data-ttu-id="a8d33-480">HR hizmetleri</span><span class="sxs-lookup"><span data-stu-id="a8d33-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a8d33-481">CC002</span><span class="sxs-lookup"><span data-stu-id="a8d33-481">CC002</span></span></td>
<td><span data-ttu-id="a8d33-482">Finans</span><span class="sxs-lookup"><span data-stu-id="a8d33-482">Finance</span></span></td>
<td><span data-ttu-id="a8d33-483">35</span><span class="sxs-lookup"><span data-stu-id="a8d33-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-484">CC003</span><span class="sxs-lookup"><span data-stu-id="a8d33-484">CC003</span></span></td>
<td><span data-ttu-id="a8d33-485">Montaj</span><span class="sxs-lookup"><span data-stu-id="a8d33-485">Assembly</span></span></td>
<td><span data-ttu-id="a8d33-486">55</span><span class="sxs-lookup"><span data-stu-id="a8d33-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-487">CC004</span><span class="sxs-lookup"><span data-stu-id="a8d33-487">CC004</span></span></td>
<td><span data-ttu-id="a8d33-488">Paketleme</span><span class="sxs-lookup"><span data-stu-id="a8d33-488">Packaging</span></span></td>
<td><span data-ttu-id="a8d33-489">10</span><span class="sxs-lookup"><span data-stu-id="a8d33-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a8d33-490">Maliyet nesnesi CC002 Finans, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="a8d33-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="a8d33-491">Finans hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="a8d33-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a8d33-492">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="a8d33-492">Cost object</span></span></th>
<th><span data-ttu-id="a8d33-493">Finans hizmetleri</span><span class="sxs-lookup"><span data-stu-id="a8d33-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a8d33-494">CC003</span><span class="sxs-lookup"><span data-stu-id="a8d33-494">CC003</span></span></td>
<td><span data-ttu-id="a8d33-495">Montaj</span><span class="sxs-lookup"><span data-stu-id="a8d33-495">Assembly</span></span></td>
<td><span data-ttu-id="a8d33-496">65</span><span class="sxs-lookup"><span data-stu-id="a8d33-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-497">CC004</span><span class="sxs-lookup"><span data-stu-id="a8d33-497">CC004</span></span></td>
<td><span data-ttu-id="a8d33-498">Paketleme</span><span class="sxs-lookup"><span data-stu-id="a8d33-498">Packaging</span></span></td>
<td><span data-ttu-id="a8d33-499">35</span><span class="sxs-lookup"><span data-stu-id="a8d33-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a8d33-500">Maliyet nesnesi CC003 Derleme, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="a8d33-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="a8d33-501">Derleme hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="a8d33-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a8d33-502">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="a8d33-502">Cost object</span></span></th>
<th><span data-ttu-id="a8d33-503">Derleme Hizmetleri (saat)</span><span class="sxs-lookup"><span data-stu-id="a8d33-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a8d33-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-504">Prod 1</span></span></td>
<td><span data-ttu-id="a8d33-505">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-505">Product 1</span></span></td>
<td><span data-ttu-id="a8d33-506">60</span><span class="sxs-lookup"><span data-stu-id="a8d33-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a8d33-507">Prod 2</span></span></td>
<td><span data-ttu-id="a8d33-508">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="a8d33-508">Product 2</span></span></td>
<td><span data-ttu-id="a8d33-509">20</span><span class="sxs-lookup"><span data-stu-id="a8d33-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a8d33-510">Maliyet nesnesi CC004 Ambalajlama, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="a8d33-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="a8d33-511">Ambalajlama hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="a8d33-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a8d33-512">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="a8d33-512">Cost object</span></span></th>
<th><span data-ttu-id="a8d33-513">Ambalajlama hizmetleri (saat)</span><span class="sxs-lookup"><span data-stu-id="a8d33-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a8d33-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-514">Prod 1</span></span></td>
<td><span data-ttu-id="a8d33-515">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-515">Product 1</span></span></td>
<td><span data-ttu-id="a8d33-516">80</span><span class="sxs-lookup"><span data-stu-id="a8d33-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a8d33-517">Prod 2</span></span></td>
<td><span data-ttu-id="a8d33-518">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="a8d33-518">Product 2</span></span></td>
<td><span data-ttu-id="a8d33-519">15</span><span class="sxs-lookup"><span data-stu-id="a8d33-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="a8d33-520">Bir ürünün tükettiği üretim saatleri gibi istatistiki ölçümler, doğrudan kaynak verilerinden alınabilir.</span><span class="sxs-lookup"><span data-stu-id="a8d33-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="a8d33-521">Daha fazla bilgi için, [İstatistiksel ölçüm sağlayıcı şablonu](statistical-measure-provider-template.md#statistical-measure-provider-template) bakın.</span><span class="sxs-lookup"><span data-stu-id="a8d33-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="a8d33-522">Aşağıdaki tablo, İK hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığında ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="a8d33-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a8d33-523">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="a8d33-523">Cost object</span></span></th>
<th><span data-ttu-id="a8d33-524">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="a8d33-524">Magnitude</span></span></th>
<th><span data-ttu-id="a8d33-525">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="a8d33-525">Allocation factor</span></span></th>
<th><span data-ttu-id="a8d33-526">Tutar</span><span class="sxs-lookup"><span data-stu-id="a8d33-526">Amount</span></span></th>
<th><span data-ttu-id="a8d33-527">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="a8d33-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a8d33-528">CC002</span><span class="sxs-lookup"><span data-stu-id="a8d33-528">CC002</span></span></td>
<td><span data-ttu-id="a8d33-529">Finans</span><span class="sxs-lookup"><span data-stu-id="a8d33-529">Finance</span></span></td>
<td><span data-ttu-id="a8d33-530">35</span><span class="sxs-lookup"><span data-stu-id="a8d33-530">35</span></span></td>
<td><span data-ttu-id="a8d33-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="a8d33-532">175.00</span><span class="sxs-lookup"><span data-stu-id="a8d33-532">175.00</span></span></td>
<td><span data-ttu-id="a8d33-533">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-534">CC003</span><span class="sxs-lookup"><span data-stu-id="a8d33-534">CC003</span></span></td>
<td><span data-ttu-id="a8d33-535">Montaj</span><span class="sxs-lookup"><span data-stu-id="a8d33-535">Assembly</span></span></td>
<td><span data-ttu-id="a8d33-536">55</span><span class="sxs-lookup"><span data-stu-id="a8d33-536">55</span></span></td>
<td><span data-ttu-id="a8d33-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="a8d33-538">275.00</span><span class="sxs-lookup"><span data-stu-id="a8d33-538">275.00</span></span></td>
<td><span data-ttu-id="a8d33-539">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-540">CC004</span><span class="sxs-lookup"><span data-stu-id="a8d33-540">CC004</span></span></td>
<td><span data-ttu-id="a8d33-541">Paketleme</span><span class="sxs-lookup"><span data-stu-id="a8d33-541">Packaging</span></span></td>
<td><span data-ttu-id="a8d33-542">10</span><span class="sxs-lookup"><span data-stu-id="a8d33-542">10</span></span></td>
<td><span data-ttu-id="a8d33-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="a8d33-544">50,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-544">50.00</span></span></td>
<td><span data-ttu-id="a8d33-545">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-546">CC002</span><span class="sxs-lookup"><span data-stu-id="a8d33-546">CC002</span></span></td>
<td><span data-ttu-id="a8d33-547">Finans</span><span class="sxs-lookup"><span data-stu-id="a8d33-547">Finance</span></span></td>
<td><span data-ttu-id="a8d33-548">35</span><span class="sxs-lookup"><span data-stu-id="a8d33-548">35</span></span></td>
<td><span data-ttu-id="a8d33-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="a8d33-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="a8d33-550">436.00</span><span class="sxs-lookup"><span data-stu-id="a8d33-550">436.00</span></span></td>
<td><span data-ttu-id="a8d33-551">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-552">CC003</span><span class="sxs-lookup"><span data-stu-id="a8d33-552">CC003</span></span></td>
<td><span data-ttu-id="a8d33-553">Montaj</span><span class="sxs-lookup"><span data-stu-id="a8d33-553">Assembly</span></span></td>
<td><span data-ttu-id="a8d33-554">55</span><span class="sxs-lookup"><span data-stu-id="a8d33-554">55</span></span></td>
<td><span data-ttu-id="a8d33-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="a8d33-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="a8d33-556">685.14</span><span class="sxs-lookup"><span data-stu-id="a8d33-556">685.14</span></span></td>
<td><span data-ttu-id="a8d33-557">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-558">CC004</span><span class="sxs-lookup"><span data-stu-id="a8d33-558">CC004</span></span></td>
<td><span data-ttu-id="a8d33-559">Paketleme</span><span class="sxs-lookup"><span data-stu-id="a8d33-559">Packaging</span></span></td>
<td><span data-ttu-id="a8d33-560">10</span><span class="sxs-lookup"><span data-stu-id="a8d33-560">10</span></span></td>
<td><span data-ttu-id="a8d33-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="a8d33-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="a8d33-562">124.57</span><span class="sxs-lookup"><span data-stu-id="a8d33-562">124.57</span></span></td>
<td><span data-ttu-id="a8d33-563">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a8d33-564">Aşağıdaki tablo, Finans hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="a8d33-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a8d33-565">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="a8d33-565">Cost object</span></span></th>
<th><span data-ttu-id="a8d33-566">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="a8d33-566">Magnitude</span></span></th>
<th><span data-ttu-id="a8d33-567">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="a8d33-567">Allocation factor</span></span></th>
<th><span data-ttu-id="a8d33-568">Tutar</span><span class="sxs-lookup"><span data-stu-id="a8d33-568">Amount</span></span></th>
<th><span data-ttu-id="a8d33-569">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="a8d33-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a8d33-570">CC003</span><span class="sxs-lookup"><span data-stu-id="a8d33-570">CC003</span></span></td>
<td><span data-ttu-id="a8d33-571">Montaj</span><span class="sxs-lookup"><span data-stu-id="a8d33-571">Assembly</span></span></td>
<td><span data-ttu-id="a8d33-572">65</span><span class="sxs-lookup"><span data-stu-id="a8d33-572">65</span></span></td>
<td><span data-ttu-id="a8d33-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="a8d33-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="a8d33-574">438.75</span><span class="sxs-lookup"><span data-stu-id="a8d33-574">438.75</span></span></td>
<td><span data-ttu-id="a8d33-575">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-576">CC004</span><span class="sxs-lookup"><span data-stu-id="a8d33-576">CC004</span></span></td>
<td><span data-ttu-id="a8d33-577">Paketleme</span><span class="sxs-lookup"><span data-stu-id="a8d33-577">Packaging</span></span></td>
<td><span data-ttu-id="a8d33-578">35</span><span class="sxs-lookup"><span data-stu-id="a8d33-578">35</span></span></td>
<td><span data-ttu-id="a8d33-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="a8d33-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="a8d33-580">236.25</span><span class="sxs-lookup"><span data-stu-id="a8d33-580">236.25</span></span></td>
<td><span data-ttu-id="a8d33-581">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-582">CC003</span><span class="sxs-lookup"><span data-stu-id="a8d33-582">CC003</span></span></td>
<td><span data-ttu-id="a8d33-583">Montaj</span><span class="sxs-lookup"><span data-stu-id="a8d33-583">Assembly</span></span></td>
<td><span data-ttu-id="a8d33-584">65</span><span class="sxs-lookup"><span data-stu-id="a8d33-584">65</span></span></td>
<td><span data-ttu-id="a8d33-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="a8d33-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="a8d33-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="a8d33-586">5,297.69</span></span></td>
<td><span data-ttu-id="a8d33-587">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-588">CC004</span><span class="sxs-lookup"><span data-stu-id="a8d33-588">CC004</span></span></td>
<td><span data-ttu-id="a8d33-589">Paketleme</span><span class="sxs-lookup"><span data-stu-id="a8d33-589">Packaging</span></span></td>
<td><span data-ttu-id="a8d33-590">35</span><span class="sxs-lookup"><span data-stu-id="a8d33-590">35</span></span></td>
<td><span data-ttu-id="a8d33-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="a8d33-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="a8d33-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="a8d33-592">2,852.60</span></span></td>
<td><span data-ttu-id="a8d33-593">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a8d33-594">Aşağıdaki tablo, Derleme hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="a8d33-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a8d33-595">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="a8d33-595">Cost object</span></span></th>
<th><span data-ttu-id="a8d33-596">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="a8d33-596">Magnitude</span></span></th>
<th><span data-ttu-id="a8d33-597">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="a8d33-597">Allocation factor</span></span></th>
<th><span data-ttu-id="a8d33-598">Tutar</span><span class="sxs-lookup"><span data-stu-id="a8d33-598">Amount</span></span></th>
<th><span data-ttu-id="a8d33-599">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="a8d33-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a8d33-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-600">Prod 1</span></span></td>
<td><span data-ttu-id="a8d33-601">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-601">Product 1</span></span></td>
<td><span data-ttu-id="a8d33-602">60</span><span class="sxs-lookup"><span data-stu-id="a8d33-602">60</span></span></td>
<td><span data-ttu-id="a8d33-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="a8d33-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="a8d33-604">535.31</span><span class="sxs-lookup"><span data-stu-id="a8d33-604">535.31</span></span></td>
<td><span data-ttu-id="a8d33-605">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a8d33-606">Prod 2</span></span></td>
<td><span data-ttu-id="a8d33-607">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="a8d33-607">Product 2</span></span></td>
<td><span data-ttu-id="a8d33-608">20</span><span class="sxs-lookup"><span data-stu-id="a8d33-608">20</span></span></td>
<td><span data-ttu-id="a8d33-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="a8d33-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="a8d33-610">178.44</span><span class="sxs-lookup"><span data-stu-id="a8d33-610">178.44</span></span></td>
<td><span data-ttu-id="a8d33-611">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-612">Prod 1</span></span></td>
<td><span data-ttu-id="a8d33-613">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-613">Product 1</span></span></td>
<td><span data-ttu-id="a8d33-614">60</span><span class="sxs-lookup"><span data-stu-id="a8d33-614">60</span></span></td>
<td><span data-ttu-id="a8d33-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="a8d33-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="a8d33-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="a8d33-616">4,487.12</span></span></td>
<td><span data-ttu-id="a8d33-617">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a8d33-618">Prod 2</span></span></td>
<td><span data-ttu-id="a8d33-619">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="a8d33-619">Product 2</span></span></td>
<td><span data-ttu-id="a8d33-620">20</span><span class="sxs-lookup"><span data-stu-id="a8d33-620">20</span></span></td>
<td><span data-ttu-id="a8d33-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="a8d33-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="a8d33-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="a8d33-622">1,495.71</span></span></td>
<td><span data-ttu-id="a8d33-623">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a8d33-624">Aşağıdaki tablo, Paketleme hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="a8d33-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a8d33-625">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="a8d33-625">Cost object</span></span></th>
<th><span data-ttu-id="a8d33-626">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="a8d33-626">Magnitude</span></span></th>
<th><span data-ttu-id="a8d33-627">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="a8d33-627">Allocation factor</span></span></th>
<th><span data-ttu-id="a8d33-628">Tutar</span><span class="sxs-lookup"><span data-stu-id="a8d33-628">Amount</span></span></th>
<th><span data-ttu-id="a8d33-629">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="a8d33-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a8d33-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-630">Prod 1</span></span></td>
<td><span data-ttu-id="a8d33-631">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-631">Product 1</span></span></td>
<td><span data-ttu-id="a8d33-632">80</span><span class="sxs-lookup"><span data-stu-id="a8d33-632">80</span></span></td>
<td><span data-ttu-id="a8d33-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="a8d33-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="a8d33-634">241.05</span><span class="sxs-lookup"><span data-stu-id="a8d33-634">241.05</span></span></td>
<td><span data-ttu-id="a8d33-635">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a8d33-636">Prod 2</span></span></td>
<td><span data-ttu-id="a8d33-637">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="a8d33-637">Product 2</span></span></td>
<td><span data-ttu-id="a8d33-638">15</span><span class="sxs-lookup"><span data-stu-id="a8d33-638">15</span></span></td>
<td><span data-ttu-id="a8d33-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="a8d33-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="a8d33-640">45.20</span><span class="sxs-lookup"><span data-stu-id="a8d33-640">45.20</span></span></td>
<td><span data-ttu-id="a8d33-641">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-642">Prod 1</span></span></td>
<td><span data-ttu-id="a8d33-643">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-643">Product 1</span></span></td>
<td><span data-ttu-id="a8d33-644">80</span><span class="sxs-lookup"><span data-stu-id="a8d33-644">80</span></span></td>
<td><span data-ttu-id="a8d33-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="a8d33-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="a8d33-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="a8d33-646">2,507.09</span></span></td>
<td><span data-ttu-id="a8d33-647">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a8d33-648">Prod 2</span></span></td>
<td><span data-ttu-id="a8d33-649">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="a8d33-649">Product 2</span></span></td>
<td><span data-ttu-id="a8d33-650">15</span><span class="sxs-lookup"><span data-stu-id="a8d33-650">15</span></span></td>
<td><span data-ttu-id="a8d33-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="a8d33-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="a8d33-652">470.08</span><span class="sxs-lookup"><span data-stu-id="a8d33-652">470.08</span></span></td>
<td><span data-ttu-id="a8d33-653">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="a8d33-654">Günlük girişleri (maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="a8d33-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a8d33-655">Günlük</span><span class="sxs-lookup"><span data-stu-id="a8d33-655">Journal</span></span></th>
<th><span data-ttu-id="a8d33-656">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="a8d33-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="a8d33-657">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="a8d33-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="a8d33-658">Sürüm</span><span class="sxs-lookup"><span data-stu-id="a8d33-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a8d33-659">00004</span><span class="sxs-lookup"><span data-stu-id="a8d33-659">00004</span></span></td>
<td><span data-ttu-id="a8d33-660">Maliyet tahsisatı günlüğü</span><span class="sxs-lookup"><span data-stu-id="a8d33-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="a8d33-661">Mali</span><span class="sxs-lookup"><span data-stu-id="a8d33-661">Fiscal</span></span></td>
<td><span data-ttu-id="a8d33-662">2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-662">2017</span></span></td>
<td><span data-ttu-id="a8d33-663">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-663">Period 1</span></span></td>
<td><span data-ttu-id="a8d33-664">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="a8d33-665">Günlük satırları</span><span class="sxs-lookup"><span data-stu-id="a8d33-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a8d33-666">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="a8d33-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="a8d33-667">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="a8d33-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a8d33-668">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="a8d33-668">Cost element</span></span></th>
<th><span data-ttu-id="a8d33-669">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="a8d33-669">Cost behavior</span></span></th>
<th><span data-ttu-id="a8d33-670">Tutar</span><span class="sxs-lookup"><span data-stu-id="a8d33-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a8d33-671">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="a8d33-672">CC001</span><span class="sxs-lookup"><span data-stu-id="a8d33-672">CC001</span></span></td>
<td><span data-ttu-id="a8d33-673">İK</span><span class="sxs-lookup"><span data-stu-id="a8d33-673">HR</span></span></td>
<td><span data-ttu-id="a8d33-674">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-674">10001</span></span></td>
<td><span data-ttu-id="a8d33-675">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-675">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-676">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-676">Fixed cost</span></span></td>
<td><span data-ttu-id="a8d33-677">500.00</span><span class="sxs-lookup"><span data-stu-id="a8d33-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-678">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="a8d33-679">CC001</span><span class="sxs-lookup"><span data-stu-id="a8d33-679">CC001</span></span></td>
<td><span data-ttu-id="a8d33-680">İK</span><span class="sxs-lookup"><span data-stu-id="a8d33-680">HR</span></span></td>
<td><span data-ttu-id="a8d33-681">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-681">10001</span></span></td>
<td><span data-ttu-id="a8d33-682">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-682">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-683">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-683">Variable cost</span></span></td>
<td><span data-ttu-id="a8d33-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="a8d33-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-685">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="a8d33-686">CC002</span><span class="sxs-lookup"><span data-stu-id="a8d33-686">CC002</span></span></td>
<td><span data-ttu-id="a8d33-687">Finans</span><span class="sxs-lookup"><span data-stu-id="a8d33-687">Finance</span></span></td>
<td><span data-ttu-id="a8d33-688">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-688">10001</span></span></td>
<td><span data-ttu-id="a8d33-689">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-689">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-690">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-690">Fixed cost</span></span></td>
<td><span data-ttu-id="a8d33-691">675.00</span><span class="sxs-lookup"><span data-stu-id="a8d33-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-692">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="a8d33-693">CC002</span><span class="sxs-lookup"><span data-stu-id="a8d33-693">CC002</span></span></td>
<td><span data-ttu-id="a8d33-694">Finans</span><span class="sxs-lookup"><span data-stu-id="a8d33-694">Finance</span></span></td>
<td><span data-ttu-id="a8d33-695">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-695">10001</span></span></td>
<td><span data-ttu-id="a8d33-696">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-696">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-697">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-697">Variable cost</span></span></td>
<td><span data-ttu-id="a8d33-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="a8d33-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-699">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="a8d33-700">CC003</span><span class="sxs-lookup"><span data-stu-id="a8d33-700">CC003</span></span></td>
<td><span data-ttu-id="a8d33-701">Montaj</span><span class="sxs-lookup"><span data-stu-id="a8d33-701">Assembly</span></span></td>
<td><span data-ttu-id="a8d33-702">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-702">10001</span></span></td>
<td><span data-ttu-id="a8d33-703">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-703">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-704">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-704">Fixed cost</span></span></td>
<td><span data-ttu-id="a8d33-705">713.75</span><span class="sxs-lookup"><span data-stu-id="a8d33-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-706">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="a8d33-707">CC003</span><span class="sxs-lookup"><span data-stu-id="a8d33-707">CC003</span></span></td>
<td><span data-ttu-id="a8d33-708">Montaj</span><span class="sxs-lookup"><span data-stu-id="a8d33-708">Assembly</span></span></td>
<td><span data-ttu-id="a8d33-709">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-709">10001</span></span></td>
<td><span data-ttu-id="a8d33-710">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-710">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-711">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-711">Variable cost</span></span></td>
<td><span data-ttu-id="a8d33-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="a8d33-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-713">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="a8d33-714">CC003</span><span class="sxs-lookup"><span data-stu-id="a8d33-714">CC003</span></span></td>
<td><span data-ttu-id="a8d33-715">Paketleme</span><span class="sxs-lookup"><span data-stu-id="a8d33-715">Packaging</span></span></td>
<td><span data-ttu-id="a8d33-716">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-716">10001</span></span></td>
<td><span data-ttu-id="a8d33-717">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-717">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-718">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-718">Fixed cost</span></span></td>
<td><span data-ttu-id="a8d33-719">286.25</span><span class="sxs-lookup"><span data-stu-id="a8d33-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-720">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="a8d33-721">CC003</span><span class="sxs-lookup"><span data-stu-id="a8d33-721">CC003</span></span></td>
<td><span data-ttu-id="a8d33-722">Paketleme</span><span class="sxs-lookup"><span data-stu-id="a8d33-722">Packaging</span></span></td>
<td><span data-ttu-id="a8d33-723">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-723">10001</span></span></td>
<td><span data-ttu-id="a8d33-724">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-724">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-725">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-725">Variable cost</span></span></td>
<td><span data-ttu-id="a8d33-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="a8d33-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-727">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="a8d33-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-728">Prod 1</span></span></td>
<td><span data-ttu-id="a8d33-729">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-729">Product 1</span></span></td>
<td><span data-ttu-id="a8d33-730">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-730">10001</span></span></td>
<td><span data-ttu-id="a8d33-731">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-731">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-732">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-732">Fixed cost</span></span></td>
<td><span data-ttu-id="a8d33-733">776.36</span><span class="sxs-lookup"><span data-stu-id="a8d33-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-734">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="a8d33-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-735">Prod 1</span></span></td>
<td><span data-ttu-id="a8d33-736">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-736">Product 1</span></span></td>
<td><span data-ttu-id="a8d33-737">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-737">10001</span></span></td>
<td><span data-ttu-id="a8d33-738">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-738">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-739">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-739">Variable cost</span></span></td>
<td><span data-ttu-id="a8d33-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="a8d33-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-741">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="a8d33-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a8d33-742">Prod 2</span></span></td>
<td><span data-ttu-id="a8d33-743">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-743">Product 1</span></span></td>
<td><span data-ttu-id="a8d33-744">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-744">10001</span></span></td>
<td><span data-ttu-id="a8d33-745">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-745">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-746">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-746">Fixed cost</span></span></td>
<td><span data-ttu-id="a8d33-747">223.64</span><span class="sxs-lookup"><span data-stu-id="a8d33-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-748">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="a8d33-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a8d33-749">Prod 2</span></span></td>
<td><span data-ttu-id="a8d33-750">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-750">Product 1</span></span></td>
<td><span data-ttu-id="a8d33-751">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-751">10001</span></span></td>
<td><span data-ttu-id="a8d33-752">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-752">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-753">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-753">Variable cost</span></span></td>
<td><span data-ttu-id="a8d33-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="a8d33-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="a8d33-755">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="a8d33-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="a8d33-756">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="a8d33-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="a8d33-757">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="a8d33-757">Cost element</span></span></th>
<th><span data-ttu-id="a8d33-758">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="a8d33-758">Cost behavior</span></span></th>
<th><span data-ttu-id="a8d33-759">Tutar</span><span class="sxs-lookup"><span data-stu-id="a8d33-759">Amount</span></span></th>
<th><span data-ttu-id="a8d33-760">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="a8d33-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a8d33-761">CC001</span><span class="sxs-lookup"><span data-stu-id="a8d33-761">CC001</span></span></td>
<td><span data-ttu-id="a8d33-762">İK</span><span class="sxs-lookup"><span data-stu-id="a8d33-762">HR</span></span></td>
<td><span data-ttu-id="a8d33-763">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-763">10001</span></span></td>
<td><span data-ttu-id="a8d33-764">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-764">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-765">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-765">Fixed cost</span></span></td>
<td><span data-ttu-id="a8d33-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="a8d33-766">-500.00</span></span></td>
<td><span data-ttu-id="a8d33-767">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-768">CC002</span><span class="sxs-lookup"><span data-stu-id="a8d33-768">CC002</span></span></td>
<td><span data-ttu-id="a8d33-769">Finans</span><span class="sxs-lookup"><span data-stu-id="a8d33-769">Finance</span></span></td>
<td><span data-ttu-id="a8d33-770">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-770">10001</span></span></td>
<td><span data-ttu-id="a8d33-771">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-771">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-772">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-772">Fixed cost</span></span></td>
<td><span data-ttu-id="a8d33-773">175.00</span><span class="sxs-lookup"><span data-stu-id="a8d33-773">175.00</span></span></td>
<td><span data-ttu-id="a8d33-774">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-775">CC003</span><span class="sxs-lookup"><span data-stu-id="a8d33-775">CC003</span></span></td>
<td><span data-ttu-id="a8d33-776">Montaj</span><span class="sxs-lookup"><span data-stu-id="a8d33-776">Assembly</span></span></td>
<td><span data-ttu-id="a8d33-777">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-777">10001</span></span></td>
<td><span data-ttu-id="a8d33-778">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-778">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-779">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-779">Fixed cost</span></span></td>
<td><span data-ttu-id="a8d33-780">275.00</span><span class="sxs-lookup"><span data-stu-id="a8d33-780">275.00</span></span></td>
<td><span data-ttu-id="a8d33-781">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-782">CC004</span><span class="sxs-lookup"><span data-stu-id="a8d33-782">CC004</span></span></td>
<td><span data-ttu-id="a8d33-783">Paketleme</span><span class="sxs-lookup"><span data-stu-id="a8d33-783">Packaging</span></span></td>
<td><span data-ttu-id="a8d33-784">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-784">10001</span></span></td>
<td><span data-ttu-id="a8d33-785">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-785">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-786">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-786">Fixed cost</span></span></td>
<td><span data-ttu-id="a8d33-787">50,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-787">50,00</span></span></td>
<td><span data-ttu-id="a8d33-788">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-789">CC001</span><span class="sxs-lookup"><span data-stu-id="a8d33-789">CC001</span></span></td>
<td><span data-ttu-id="a8d33-790">İK</span><span class="sxs-lookup"><span data-stu-id="a8d33-790">HR</span></span></td>
<td><span data-ttu-id="a8d33-791">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-791">10001</span></span></td>
<td><span data-ttu-id="a8d33-792">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-792">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-793">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-793">Variable cost</span></span></td>
<td><span data-ttu-id="a8d33-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="a8d33-794">-1,245.71</span></span></td>
<td><span data-ttu-id="a8d33-795">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-796">CC002</span><span class="sxs-lookup"><span data-stu-id="a8d33-796">CC002</span></span></td>
<td><span data-ttu-id="a8d33-797">Finans</span><span class="sxs-lookup"><span data-stu-id="a8d33-797">Finance</span></span></td>
<td><span data-ttu-id="a8d33-798">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-798">10001</span></span></td>
<td><span data-ttu-id="a8d33-799">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-799">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-800">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-800">Variable cost</span></span></td>
<td><span data-ttu-id="a8d33-801">436.00</span><span class="sxs-lookup"><span data-stu-id="a8d33-801">436.00</span></span></td>
<td><span data-ttu-id="a8d33-802">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-803">CC003</span><span class="sxs-lookup"><span data-stu-id="a8d33-803">CC003</span></span></td>
<td><span data-ttu-id="a8d33-804">Montaj</span><span class="sxs-lookup"><span data-stu-id="a8d33-804">Assembly</span></span></td>
<td><span data-ttu-id="a8d33-805">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-805">10001</span></span></td>
<td><span data-ttu-id="a8d33-806">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-806">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-807">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-807">Variable cost</span></span></td>
<td><span data-ttu-id="a8d33-808">685.14</span><span class="sxs-lookup"><span data-stu-id="a8d33-808">685.14</span></span></td>
<td><span data-ttu-id="a8d33-809">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-810">CC004</span><span class="sxs-lookup"><span data-stu-id="a8d33-810">CC004</span></span></td>
<td><span data-ttu-id="a8d33-811">Paketleme</span><span class="sxs-lookup"><span data-stu-id="a8d33-811">Packaging</span></span></td>
<td><span data-ttu-id="a8d33-812">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-812">10001</span></span></td>
<td><span data-ttu-id="a8d33-813">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-813">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-814">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-814">Variable cost</span></span></td>
<td><span data-ttu-id="a8d33-815">124.57</span><span class="sxs-lookup"><span data-stu-id="a8d33-815">124.57</span></span></td>
<td><span data-ttu-id="a8d33-816">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-817">CC002</span><span class="sxs-lookup"><span data-stu-id="a8d33-817">CC002</span></span></td>
<td><span data-ttu-id="a8d33-818">Finans</span><span class="sxs-lookup"><span data-stu-id="a8d33-818">Finance</span></span></td>
<td><span data-ttu-id="a8d33-819">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-819">10001</span></span></td>
<td><span data-ttu-id="a8d33-820">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-820">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-821">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-821">Fixed cost</span></span></td>
<td><span data-ttu-id="a8d33-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-822">-675.00</span></span></td>
<td><span data-ttu-id="a8d33-823">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-824">CC003</span><span class="sxs-lookup"><span data-stu-id="a8d33-824">CC003</span></span></td>
<td><span data-ttu-id="a8d33-825">Montaj</span><span class="sxs-lookup"><span data-stu-id="a8d33-825">Assembly</span></span></td>
<td><span data-ttu-id="a8d33-826">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-826">10001</span></span></td>
<td><span data-ttu-id="a8d33-827">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-827">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-828">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-828">Fixed cost</span></span></td>
<td><span data-ttu-id="a8d33-829">438.75</span><span class="sxs-lookup"><span data-stu-id="a8d33-829">438.75</span></span></td>
<td><span data-ttu-id="a8d33-830">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-831">CC004</span><span class="sxs-lookup"><span data-stu-id="a8d33-831">CC004</span></span></td>
<td><span data-ttu-id="a8d33-832">Paketleme</span><span class="sxs-lookup"><span data-stu-id="a8d33-832">Packaging</span></span></td>
<td><span data-ttu-id="a8d33-833">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-833">10001</span></span></td>
<td><span data-ttu-id="a8d33-834">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-834">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-835">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-835">Fixed cost</span></span></td>
<td><span data-ttu-id="a8d33-836">236.25</span><span class="sxs-lookup"><span data-stu-id="a8d33-836">236.25</span></span></td>
<td><span data-ttu-id="a8d33-837">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-838">CC002</span><span class="sxs-lookup"><span data-stu-id="a8d33-838">CC002</span></span></td>
<td><span data-ttu-id="a8d33-839">Finans</span><span class="sxs-lookup"><span data-stu-id="a8d33-839">Finance</span></span></td>
<td><span data-ttu-id="a8d33-840">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-840">10001</span></span></td>
<td><span data-ttu-id="a8d33-841">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-841">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-842">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-842">Variable cost</span></span></td>
<td><span data-ttu-id="a8d33-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="a8d33-843">-8,150.29</span></span></td>
<td><span data-ttu-id="a8d33-844">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-845">CC003</span><span class="sxs-lookup"><span data-stu-id="a8d33-845">CC003</span></span></td>
<td><span data-ttu-id="a8d33-846">Montaj</span><span class="sxs-lookup"><span data-stu-id="a8d33-846">Assembly</span></span></td>
<td><span data-ttu-id="a8d33-847">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-847">10001</span></span></td>
<td><span data-ttu-id="a8d33-848">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-848">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-849">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-849">Variable cost</span></span></td>
<td><span data-ttu-id="a8d33-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="a8d33-850">5,297.69</span></span></td>
<td><span data-ttu-id="a8d33-851">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-852">CC004</span><span class="sxs-lookup"><span data-stu-id="a8d33-852">CC004</span></span></td>
<td><span data-ttu-id="a8d33-853">Paketleme</span><span class="sxs-lookup"><span data-stu-id="a8d33-853">Packaging</span></span></td>
<td><span data-ttu-id="a8d33-854">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-854">10001</span></span></td>
<td><span data-ttu-id="a8d33-855">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-855">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-856">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-856">Variable cost</span></span></td>
<td><span data-ttu-id="a8d33-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="a8d33-857">2,852.60</span></span></td>
<td><span data-ttu-id="a8d33-858">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-859">CC003</span><span class="sxs-lookup"><span data-stu-id="a8d33-859">CC003</span></span></td>
<td><span data-ttu-id="a8d33-860">Montaj</span><span class="sxs-lookup"><span data-stu-id="a8d33-860">Assembly</span></span></td>
<td><span data-ttu-id="a8d33-861">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-861">10001</span></span></td>
<td><span data-ttu-id="a8d33-862">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-862">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-863">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-863">Fixed cost</span></span></td>
<td><span data-ttu-id="a8d33-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="a8d33-864">-713.75</span></span></td>
<td><span data-ttu-id="a8d33-865">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-866">Prod 1</span></span></td>
<td><span data-ttu-id="a8d33-867">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-867">Product 1</span></span></td>
<td><span data-ttu-id="a8d33-868">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-868">10001</span></span></td>
<td><span data-ttu-id="a8d33-869">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-869">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-870">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-870">Fixed cost</span></span></td>
<td><span data-ttu-id="a8d33-871">535.31</span><span class="sxs-lookup"><span data-stu-id="a8d33-871">535.31</span></span></td>
<td><span data-ttu-id="a8d33-872">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a8d33-873">Prod 2</span></span></td>
<td><span data-ttu-id="a8d33-874">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="a8d33-874">Product 2</span></span></td>
<td><span data-ttu-id="a8d33-875">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-875">10001</span></span></td>
<td><span data-ttu-id="a8d33-876">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-876">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-877">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-877">Fixed cost</span></span></td>
<td><span data-ttu-id="a8d33-878">178.44</span><span class="sxs-lookup"><span data-stu-id="a8d33-878">178.44</span></span></td>
<td><span data-ttu-id="a8d33-879">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-880">CC003</span><span class="sxs-lookup"><span data-stu-id="a8d33-880">CC003</span></span></td>
<td><span data-ttu-id="a8d33-881">Montaj</span><span class="sxs-lookup"><span data-stu-id="a8d33-881">Assembly</span></span></td>
<td><span data-ttu-id="a8d33-882">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-882">10001</span></span></td>
<td><span data-ttu-id="a8d33-883">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-883">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-884">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-884">Variable cost</span></span></td>
<td><span data-ttu-id="a8d33-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="a8d33-885">-5,982.83</span></span></td>
<td><span data-ttu-id="a8d33-886">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-887">Prod 1</span></span></td>
<td><span data-ttu-id="a8d33-888">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-888">Product 1</span></span></td>
<td><span data-ttu-id="a8d33-889">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-889">10001</span></span></td>
<td><span data-ttu-id="a8d33-890">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-890">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-891">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-891">Variable cost</span></span></td>
<td><span data-ttu-id="a8d33-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="a8d33-892">4,487.12</span></span></td>
<td><span data-ttu-id="a8d33-893">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a8d33-894">Prod 2</span></span></td>
<td><span data-ttu-id="a8d33-895">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="a8d33-895">Product 2</span></span></td>
<td><span data-ttu-id="a8d33-896">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-896">10001</span></span></td>
<td><span data-ttu-id="a8d33-897">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-897">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-898">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-898">Variable cost</span></span></td>
<td><span data-ttu-id="a8d33-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="a8d33-899">1,495.71</span></span></td>
<td><span data-ttu-id="a8d33-900">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-901">CC003</span><span class="sxs-lookup"><span data-stu-id="a8d33-901">CC003</span></span></td>
<td><span data-ttu-id="a8d33-902">Montaj</span><span class="sxs-lookup"><span data-stu-id="a8d33-902">Assembly</span></span></td>
<td><span data-ttu-id="a8d33-903">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-903">10001</span></span></td>
<td><span data-ttu-id="a8d33-904">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-904">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-905">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-905">Fixed cost</span></span></td>
<td><span data-ttu-id="a8d33-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="a8d33-906">-286.25</span></span></td>
<td><span data-ttu-id="a8d33-907">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-908">Prod 1</span></span></td>
<td><span data-ttu-id="a8d33-909">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-909">Product 1</span></span></td>
<td><span data-ttu-id="a8d33-910">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-910">10001</span></span></td>
<td><span data-ttu-id="a8d33-911">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-911">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-912">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-912">Fixed cost</span></span></td>
<td><span data-ttu-id="a8d33-913">241.05</span><span class="sxs-lookup"><span data-stu-id="a8d33-913">241.05</span></span></td>
<td><span data-ttu-id="a8d33-914">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a8d33-915">Prod 2</span></span></td>
<td><span data-ttu-id="a8d33-916">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="a8d33-916">Product 2</span></span></td>
<td><span data-ttu-id="a8d33-917">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-917">10001</span></span></td>
<td><span data-ttu-id="a8d33-918">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-918">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-919">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-919">Fixed cost</span></span></td>
<td><span data-ttu-id="a8d33-920">45.20</span><span class="sxs-lookup"><span data-stu-id="a8d33-920">45.20</span></span></td>
<td><span data-ttu-id="a8d33-921">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-922">CC003</span><span class="sxs-lookup"><span data-stu-id="a8d33-922">CC003</span></span></td>
<td><span data-ttu-id="a8d33-923">Montaj</span><span class="sxs-lookup"><span data-stu-id="a8d33-923">Assembly</span></span></td>
<td><span data-ttu-id="a8d33-924">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-924">10001</span></span></td>
<td><span data-ttu-id="a8d33-925">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-925">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-926">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-926">Variable cost</span></span></td>
<td><span data-ttu-id="a8d33-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="a8d33-927">-2,977.17</span></span></td>
<td><span data-ttu-id="a8d33-928">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-929">Prod 1</span></span></td>
<td><span data-ttu-id="a8d33-930">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-930">Product 1</span></span></td>
<td><span data-ttu-id="a8d33-931">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-931">10001</span></span></td>
<td><span data-ttu-id="a8d33-932">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-932">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-933">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-933">Variable cost</span></span></td>
<td><span data-ttu-id="a8d33-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="a8d33-934">2,507.09</span></span></td>
<td><span data-ttu-id="a8d33-935">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8d33-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a8d33-936">Prod 2</span></span></td>
<td><span data-ttu-id="a8d33-937">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="a8d33-937">Product 2</span></span></td>
<td><span data-ttu-id="a8d33-938">10001</span><span class="sxs-lookup"><span data-stu-id="a8d33-938">10001</span></span></td>
<td><span data-ttu-id="a8d33-939">Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-939">Electricity</span></span></td>
<td><span data-ttu-id="a8d33-940">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-940">Variable cost</span></span></td>
<td><span data-ttu-id="a8d33-941">470.08</span><span class="sxs-lookup"><span data-stu-id="a8d33-941">470.08</span></span></td>
<td><span data-ttu-id="a8d33-942">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="a8d33-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="a8d33-943">Sonuç</span><span class="sxs-lookup"><span data-stu-id="a8d33-943">Conclusion</span></span>
<span data-ttu-id="a8d33-944">Mali muhasebede, Elektrik için 10.000,00 maliyet bir sözde maliyet merkezi kimliğine nakledilmiştir.</span><span class="sxs-lookup"><span data-stu-id="a8d33-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="a8d33-945">Bu nedenle, maliyet muhasebecileri bu maliyetin tahsis edilmesi gerektiğini bilirler.</span><span class="sxs-lookup"><span data-stu-id="a8d33-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="a8d33-946">Maliyet muhasebesinde, maliyetler kuruluş birimleri ve seviyeleri arasında, uygulanan kural ve ilkelere dayalı olarak akar.</span><span class="sxs-lookup"><span data-stu-id="a8d33-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="a8d33-947">Her maliyet, maliyetlerin tahsisatı için en iyi değerlendirmeyi sağlayan bir tahsisat tabanı ile ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="a8d33-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="a8d33-948">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="a8d33-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="a8d33-949">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="a8d33-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="a8d33-950">Toplam</span><span class="sxs-lookup"><span data-stu-id="a8d33-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a8d33-951">CC099</span><span class="sxs-lookup"><span data-stu-id="a8d33-951">CC099</span></span></th>
<th><span data-ttu-id="a8d33-952">CC001</span><span class="sxs-lookup"><span data-stu-id="a8d33-952">CC001</span></span></th>
<th><span data-ttu-id="a8d33-953">CC002</span><span class="sxs-lookup"><span data-stu-id="a8d33-953">CC002</span></span></th>
<th><span data-ttu-id="a8d33-954">CC003</span><span class="sxs-lookup"><span data-stu-id="a8d33-954">CC003</span></span></th>
<th><span data-ttu-id="a8d33-955">CC004</span><span class="sxs-lookup"><span data-stu-id="a8d33-955">CC004</span></span></th>
<th><span data-ttu-id="a8d33-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-956">Proj 1</span></span></th>
<th><span data-ttu-id="a8d33-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="a8d33-957">Proj 2</span></span></th>
<th><span data-ttu-id="a8d33-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="a8d33-958">Prod 1</span></span></th>
<th><span data-ttu-id="a8d33-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="a8d33-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="a8d33-960">10001 Elektrik</span><span class="sxs-lookup"><span data-stu-id="a8d33-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a8d33-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="a8d33-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a8d33-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="a8d33-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a8d33-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="a8d33-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a8d33-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="a8d33-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="a8d33-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="a8d33-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a8d33-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="a8d33-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a8d33-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="a8d33-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a8d33-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="a8d33-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="a8d33-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="a8d33-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="a8d33-970">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="a8d33-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a8d33-971">0,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="a8d33-972">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a8d33-973">0,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a8d33-974">0,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a8d33-975">0,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a8d33-976">0,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a8d33-977">0,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="a8d33-978">776.36</span><span class="sxs-lookup"><span data-stu-id="a8d33-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a8d33-979">223.64</span><span class="sxs-lookup"><span data-stu-id="a8d33-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a8d33-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="a8d33-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="a8d33-981">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="a8d33-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a8d33-982">000</span><span class="sxs-lookup"><span data-stu-id="a8d33-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a8d33-983">0,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a8d33-984">0,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a8d33-985">0,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a8d33-986">0,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a8d33-987">30.00</span><span class="sxs-lookup"><span data-stu-id="a8d33-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a8d33-988">10,00</span><span class="sxs-lookup"><span data-stu-id="a8d33-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a8d33-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="a8d33-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a8d33-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="a8d33-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="a8d33-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="a8d33-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="a8d33-992">Bu konu, birincil maliyet öğesi, 10001 Elektrik'in maliyet nesneleri arasında nasıl aktığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a8d33-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="a8d33-993">Bu nedenle, bu genel gider maliyeti kuruluşun en düşük seviyesine tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="a8d33-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="a8d33-994">Başka bir deyişle, maliyet en alt düzeydeki maliyet nesnelerine aittir.</span><span class="sxs-lookup"><span data-stu-id="a8d33-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="a8d33-995">Maliyetin, maliyet nesneleri arasında görsel bir akışına ihtiyacınız varsa, maliyetin akışını görselleştirmek için maliyet toplamı ilke kurallarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a8d33-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="a8d33-996">Daha fazla bilgi için bkz. [Maliyet yuvarlama ilkesi ve genel gider hesaplaması](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="a8d33-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



