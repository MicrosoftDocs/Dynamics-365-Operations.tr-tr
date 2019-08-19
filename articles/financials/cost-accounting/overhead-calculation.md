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
ms.openlocfilehash: cef4a80aa12927fdbffea4bb6bcb108ad81494a6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841501"
---
# <a name="overhead-calculation"></a><span data-ttu-id="2fea8-103">Genel gider hesaplaması</span><span class="sxs-lookup"><span data-stu-id="2fea8-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2fea8-104">Bu konu, genel gider maliyetlerinin hesaplanması için tipik işlemleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="2fea8-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="2fea8-105">Terim tanımı</span><span class="sxs-lookup"><span data-stu-id="2fea8-105">Term definition</span></span>
---------------

<span data-ttu-id="2fea8-106">Genel gider maliyetleri bir işletmenin çalışması için normalde uygulanan, ancak doğrudan herhangi bir özel iş, faaliyet, ürün veya hizmete ilişkilendirilmemiş olan maliyetlerdir.</span><span class="sxs-lookup"><span data-stu-id="2fea8-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="2fea8-107">Genel gider maliyetleri kar sağlama faaliyetlerinin oluşturulması için kritik destek sağlar.</span><span class="sxs-lookup"><span data-stu-id="2fea8-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="2fea8-108">Aşağıda bazı genel gider örnekleri verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="2fea8-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="2fea8-109">Kira</span><span class="sxs-lookup"><span data-stu-id="2fea8-109">Rent</span></span>
-   <span data-ttu-id="2fea8-110">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-110">Electricity</span></span>
-   <span data-ttu-id="2fea8-111">Yönetim maaşları</span><span class="sxs-lookup"><span data-stu-id="2fea8-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="2fea8-112">Genel gider hesaplaması genel bakış</span><span class="sxs-lookup"><span data-stu-id="2fea8-112">Overhead calculation overview</span></span>
<span data-ttu-id="2fea8-113">Genel gider hesaplama, maliyet muhasebesi ilkelerini doğru sırayla çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="2fea8-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="2fea8-114">Maliyet muhasebesi ilkeleri değiştiyse veya belirli hatalar algılandıysa, genel gider hesaplamasını aynı mali dönem için birden fazla kez yürütebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2fea8-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="2fea8-115">Her genel gider hesaplaması depolanır ve önceki sürümlerdeki hesaplamaları kıyaslamanıza olanak sağlayan, benzersiz bir sürüm kimliğine sahip olur.</span><span class="sxs-lookup"><span data-stu-id="2fea8-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="2fea8-116">Genel gider hesaplamasının oluşturduğu maliyet girişleri bir muhasebe tarihi alır.</span><span class="sxs-lookup"><span data-stu-id="2fea8-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="2fea8-117">Bu muhasebe tarihi, hesaplamada kullanılan mali dönemin bitiş tarihiyle eşleşir.</span><span class="sxs-lookup"><span data-stu-id="2fea8-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="2fea8-118">Benzersiz sürüm kimliği aşağıdaki öğelerden oluşur:</span><span class="sxs-lookup"><span data-stu-id="2fea8-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="2fea8-119">Sürüm türü</span><span class="sxs-lookup"><span data-stu-id="2fea8-119">Version type</span></span>
-   <span data-ttu-id="2fea8-120">Tarih ve saat</span><span class="sxs-lookup"><span data-stu-id="2fea8-120">Date and time</span></span>
-   <span data-ttu-id="2fea8-121">Maliyet muhasebesi defteri</span><span class="sxs-lookup"><span data-stu-id="2fea8-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="2fea8-122">Mali yıl</span><span class="sxs-lookup"><span data-stu-id="2fea8-122">Fiscal year</span></span>
-   <span data-ttu-id="2fea8-123">Mali dönem</span><span class="sxs-lookup"><span data-stu-id="2fea8-123">Fiscal period</span></span>

<span data-ttu-id="2fea8-124">Genel gider hesaplama, sürümden bağımsız olarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="2fea8-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="2fea8-125">Bu nedenle, Gerçek sürümden önce Bütçe sürümünü hesaplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2fea8-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="2fea8-126">Genel gider hesaplama dört adımdan oluşur, aşağıdaki çizimde gösterildiği gibi.</span><span class="sxs-lookup"><span data-stu-id="2fea8-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="2fea8-127">Her adımda, günlük girişleri olan bir günlük başlığı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2fea8-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="2fea8-128">Bu günlük başlığı, her hesaplama adımı için giriş verilerini tutar.</span><span class="sxs-lookup"><span data-stu-id="2fea8-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="2fea8-129">İlkeler ve kurallar her günlük satırına uygulanır ve maliyet girişleri çıkış olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2fea8-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="2fea8-130">Bu nedenle, her zaman tam izlenebilirliğe sahip olursunuz.</span><span class="sxs-lookup"><span data-stu-id="2fea8-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="2fea8-131">[![Genel gider hesaplaması](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="2fea8-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="2fea8-132">Elektrik genel gideri maliyetini hesapla ve tahsis et</span><span class="sxs-lookup"><span data-stu-id="2fea8-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="2fea8-133">Mali muhasebede, elektrik gibi bazı maliyetler peşin ödeme olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="2fea8-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="2fea8-134">Bu nedenle, Maliyet muhasebesi için ayrıntılı yönetim bilgiler sağlanmaz.</span><span class="sxs-lookup"><span data-stu-id="2fea8-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="2fea8-135">Maliyet muhasebesinde doğru yönetimsel bilgileri tüm yönetim birim ve düzeylerinde sağlamak için, maliyetlerin kuruluş birimleri arasında akması gerekir.</span><span class="sxs-lookup"><span data-stu-id="2fea8-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="2fea8-136">Bu akış, tüketimin doğru bir kaydına ya da adil bir değerlendirmeye dayanıyor olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2fea8-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="2fea8-137">Genel muhasebede, bir elektrik maliyeti aşağıdaki tabloda gösterildiği gibi deftere nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="2fea8-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2fea8-138">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="2fea8-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="2fea8-139">Maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="2fea8-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="2fea8-140">Ana hesap</span><span class="sxs-lookup"><span data-stu-id="2fea8-140">Main account</span></span></th>
<th><span data-ttu-id="2fea8-141">Muhasebe para birimi cinsinden tutar</span><span class="sxs-lookup"><span data-stu-id="2fea8-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2fea8-142">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="2fea8-143">CC099</span><span class="sxs-lookup"><span data-stu-id="2fea8-143">CC099</span></span></td>
<td><span data-ttu-id="2fea8-144">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="2fea8-144">Default cost center</span></span></td>
<td><span data-ttu-id="2fea8-145">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-145">10001</span></span></td>
<td><span data-ttu-id="2fea8-146">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-146">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="2fea8-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="2fea8-148">Adım 1: Maliyet davranışı hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="2fea8-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="2fea8-149">Varsayılan olarak, maliyeti girişleri kaynak veriden içeri alındığında, Maliyet muhasebesinde **Sınıflandırılmamış** maliyet davranışı sınıflandırmasını alırlar.</span><span class="sxs-lookup"><span data-stu-id="2fea8-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="2fea8-150">Maliyet davranışı ilke kuralları ekleyerek, maliyet girişlerini **Sabit maliyet** veya **Değişken maliyet** olarak yeniden sınıflandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2fea8-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="2fea8-151">Maliyet davranış kuralını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="2fea8-151">Define the cost behavior rule</span></span>

<span data-ttu-id="2fea8-152">Bazı durumlarda, sabit bir ücret maliyet parçasıdır ve kalan maliyet, tüketime dayanır.</span><span class="sxs-lookup"><span data-stu-id="2fea8-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="2fea8-153">Elektrik faturaları genellikle bu tanıma uyar.</span><span class="sxs-lookup"><span data-stu-id="2fea8-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="2fea8-154">Belirli bir sabit ücret ödedikten sonra, kilovat saatlik (Kwh) tüketim başına ödeme yaparsınız.</span><span class="sxs-lookup"><span data-stu-id="2fea8-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="2fea8-155">Örneğin, sabit maliyet masrafı 1.000,00 ise, maliyet davranışı kural nasıl tanımlanır:</span><span class="sxs-lookup"><span data-stu-id="2fea8-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="2fea8-156">Sabit tutar 1.000,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="2fea8-157">0 &lt;= 1.000,00 = Sabit</span><span class="sxs-lookup"><span data-stu-id="2fea8-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="2fea8-158">1000,01 &lt; N = Değişken</span><span class="sxs-lookup"><span data-stu-id="2fea8-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="2fea8-159">Günlük</span><span class="sxs-lookup"><span data-stu-id="2fea8-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2fea8-160">Günlük</span><span class="sxs-lookup"><span data-stu-id="2fea8-160">Journal</span></span></th>
<th><span data-ttu-id="2fea8-161">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="2fea8-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="2fea8-162">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="2fea8-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="2fea8-163">Sürüm</span><span class="sxs-lookup"><span data-stu-id="2fea8-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2fea8-164">00001</span><span class="sxs-lookup"><span data-stu-id="2fea8-164">00001</span></span></td>
<td><span data-ttu-id="2fea8-165">Maliyet davranışı hesaplama günlüğü</span><span class="sxs-lookup"><span data-stu-id="2fea8-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="2fea8-166">Mali</span><span class="sxs-lookup"><span data-stu-id="2fea8-166">Fiscal</span></span></td>
<td><span data-ttu-id="2fea8-167">2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-167">2017</span></span></td>
<td><span data-ttu-id="2fea8-168">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-168">Period 1</span></span></td>
<td><span data-ttu-id="2fea8-169">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="2fea8-170">Günlük girişleri (Maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="2fea8-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2fea8-171">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="2fea8-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="2fea8-172">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="2fea8-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="2fea8-173">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="2fea8-173">Cost element</span></span></th>
<th><span data-ttu-id="2fea8-174">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="2fea8-174">Cost behavior</span></span></th>
<th><span data-ttu-id="2fea8-175">Tutar</span><span class="sxs-lookup"><span data-stu-id="2fea8-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2fea8-176">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="2fea8-177">CC099</span><span class="sxs-lookup"><span data-stu-id="2fea8-177">CC099</span></span></td>
<td><span data-ttu-id="2fea8-178">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="2fea8-178">Default cost center</span></span></td>
<td><span data-ttu-id="2fea8-179">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-179">10001</span></span></td>
<td><span data-ttu-id="2fea8-180">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-180">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-181">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="2fea8-181">Unclassified</span></span></td>
<td><span data-ttu-id="2fea8-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="2fea8-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="2fea8-183">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="2fea8-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2fea8-184">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="2fea8-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="2fea8-185">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="2fea8-185">Cost element</span></span></th>
<th><span data-ttu-id="2fea8-186">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="2fea8-186">Cost behavior</span></span></th>
<th><span data-ttu-id="2fea8-187">Tutar</span><span class="sxs-lookup"><span data-stu-id="2fea8-187">Amount</span></span></th>
<th><span data-ttu-id="2fea8-188">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="2fea8-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2fea8-189">CC099</span><span class="sxs-lookup"><span data-stu-id="2fea8-189">CC099</span></span></td>
<td><span data-ttu-id="2fea8-190">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="2fea8-190">Default cost center</span></span></td>
<td><span data-ttu-id="2fea8-191">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-191">10001</span></span></td>
<td><span data-ttu-id="2fea8-192">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-192">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-193">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="2fea8-193">Unclassified</span></span></td>
<td><span data-ttu-id="2fea8-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="2fea8-194">10,000.00</span></span></td>
<td><span data-ttu-id="2fea8-195">3 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-196">CC099</span><span class="sxs-lookup"><span data-stu-id="2fea8-196">CC099</span></span></td>
<td><span data-ttu-id="2fea8-197">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="2fea8-197">Default cost center</span></span></td>
<td><span data-ttu-id="2fea8-198">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-198">10001</span></span></td>
<td><span data-ttu-id="2fea8-199">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-199">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-200">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="2fea8-200">Unclassified</span></span></td>
<td><span data-ttu-id="2fea8-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-201">-10,000.00</span></span></td>
<td><span data-ttu-id="2fea8-202">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-203">CC099</span><span class="sxs-lookup"><span data-stu-id="2fea8-203">CC099</span></span></td>
<td><span data-ttu-id="2fea8-204">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="2fea8-204">Default cost center</span></span></td>
<td><span data-ttu-id="2fea8-205">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-205">10001</span></span></td>
<td><span data-ttu-id="2fea8-206">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-206">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-207">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-207">Fixed cost</span></span></td>
<td><span data-ttu-id="2fea8-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-208">1,000.00</span></span></td>
<td><span data-ttu-id="2fea8-209">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-210">CC099</span><span class="sxs-lookup"><span data-stu-id="2fea8-210">CC099</span></span></td>
<td><span data-ttu-id="2fea8-211">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="2fea8-211">Default cost center</span></span></td>
<td><span data-ttu-id="2fea8-212">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-212">10001</span></span></td>
<td><span data-ttu-id="2fea8-213">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-213">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-214">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-214">Variable cost</span></span></td>
<td><span data-ttu-id="2fea8-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="2fea8-215">9,000.00</span></span></td>
<td><span data-ttu-id="2fea8-216">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2fea8-217">Daha fazla bilgi için bkz. [Maliyet davranışı ilkesi oluşturma ve bir maliyet kontrol birimine atama](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="2fea8-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="2fea8-218">Adım 2: Maliyet dağıtımı hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="2fea8-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="2fea8-219">Maliyet dağıtımı, bir nesneden bir veya daha fazlasına ilgili tahsisat tabanı uygulayarak maliyeti yeniden dağıtmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2fea8-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="2fea8-220">Maliyet dağıtımı ve maliyet tahsisatı, maliyet dağıtımının her zaman orijinal maliyetin birincil maliyet öğesinde bulunmasıyla farklılık gösterir.</span><span class="sxs-lookup"><span data-stu-id="2fea8-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="2fea8-221">Maliyet dağıtım kuralını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="2fea8-221">Define the cost distribution rule</span></span>

<span data-ttu-id="2fea8-222">Mali muhasebede, elektrik maliyetleri çoğu zaman peşin ödeme olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="2fea8-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="2fea8-223">Maliyet muhasebesinde ise bu yöntem yeterince ayrıntılı değildir.</span><span class="sxs-lookup"><span data-stu-id="2fea8-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="2fea8-224">Değişken maliyet, maliyet nesnelerine tek tek, adil bir temele dayanarak dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2fea8-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="2fea8-225">En mantıklı tahsisat, elektrik kullanımını (Kwh) temel alarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2fea8-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="2fea8-226">Elektrik adına sahip, istatistiksel bir boyut üyesi oluşturulur ve elektrik tüketimi kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="2fea8-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="2fea8-227">Varsayıla olarak, tüm istatistiksel boyut üyeleri tahsisat tabanları olarak kullanılabilir hale gelir.</span><span class="sxs-lookup"><span data-stu-id="2fea8-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2fea8-228">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="2fea8-228">Cost object</span></span></th>
<th><span data-ttu-id="2fea8-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="2fea8-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2fea8-230">CC001</span><span class="sxs-lookup"><span data-stu-id="2fea8-230">CC001</span></span></td>
<td><span data-ttu-id="2fea8-231">İK</span><span class="sxs-lookup"><span data-stu-id="2fea8-231">HR</span></span></td>
<td><span data-ttu-id="2fea8-232">1.000</span><span class="sxs-lookup"><span data-stu-id="2fea8-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-233">CC002</span><span class="sxs-lookup"><span data-stu-id="2fea8-233">CC002</span></span></td>
<td><span data-ttu-id="2fea8-234">Finans</span><span class="sxs-lookup"><span data-stu-id="2fea8-234">Finance</span></span></td>
<td><span data-ttu-id="2fea8-235">6,000</span><span class="sxs-lookup"><span data-stu-id="2fea8-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-236">CC003</span><span class="sxs-lookup"><span data-stu-id="2fea8-236">CC003</span></span></td>
<td><span data-ttu-id="2fea8-237">Montaj</span><span class="sxs-lookup"><span data-stu-id="2fea8-237">Assembly</span></span></td>
<td><span data-ttu-id="2fea8-238">0</span><span class="sxs-lookup"><span data-stu-id="2fea8-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2fea8-239">Aşağıdaki tablo, elektrik tüketiminin değişken maliyetler için bir tahsisat tabanlı olarak uygulandığındaki sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="2fea8-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2fea8-240">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="2fea8-240">Cost object</span></span></th>
<th><span data-ttu-id="2fea8-241">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="2fea8-241">Magnitude</span></span></th>
<th><span data-ttu-id="2fea8-242">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="2fea8-242">Allocation factor</span></span></th>
<th><span data-ttu-id="2fea8-243">Tutar</span><span class="sxs-lookup"><span data-stu-id="2fea8-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2fea8-244">CC001</span><span class="sxs-lookup"><span data-stu-id="2fea8-244">CC001</span></span></td>
<td><span data-ttu-id="2fea8-245">İK</span><span class="sxs-lookup"><span data-stu-id="2fea8-245">HR</span></span></td>
<td><span data-ttu-id="2fea8-246">1.000</span><span class="sxs-lookup"><span data-stu-id="2fea8-246">1,000</span></span></td>
<td><span data-ttu-id="2fea8-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="2fea8-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="2fea8-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-249">CC002</span><span class="sxs-lookup"><span data-stu-id="2fea8-249">CC002</span></span></td>
<td><span data-ttu-id="2fea8-250">Finans</span><span class="sxs-lookup"><span data-stu-id="2fea8-250">Finance</span></span></td>
<td><span data-ttu-id="2fea8-251">6,000</span><span class="sxs-lookup"><span data-stu-id="2fea8-251">6,000</span></span></td>
<td><span data-ttu-id="2fea8-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="2fea8-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="2fea8-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-254">CC003</span><span class="sxs-lookup"><span data-stu-id="2fea8-254">CC003</span></span></td>
<td><span data-ttu-id="2fea8-255">Montaj</span><span class="sxs-lookup"><span data-stu-id="2fea8-255">Assembly</span></span></td>
<td><span data-ttu-id="2fea8-256">0</span><span class="sxs-lookup"><span data-stu-id="2fea8-256">0</span></span></td>
<td><span data-ttu-id="2fea8-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="2fea8-258">0,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2fea8-259">Sabit maliyet, elektrik tüketmiş olan tekil maliyet nesnelerine eşit miktarda dağıtılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2fea8-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="2fea8-260">Bu sonuca, Elektrik istatistiksel boyut öğesini bir formül tahsisat tabanında kullanarak ulaşabilirsiniz: (Elektrik &gt; 0,00) Aşağıdaki tablo, elektrik tüketimi değişken maliyetler için bir tahsisat tabanı olarak kullanıldığında ortaya çıkan sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="2fea8-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2fea8-261">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="2fea8-261">Cost object</span></span></th>
<th><span data-ttu-id="2fea8-262">Formül</span><span class="sxs-lookup"><span data-stu-id="2fea8-262">Formula</span></span></th>
<th><span data-ttu-id="2fea8-263">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="2fea8-263">Magnitude</span></span></th>
<th><span data-ttu-id="2fea8-264">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="2fea8-264">Allocation factor</span></span></th>
<th><span data-ttu-id="2fea8-265">Tutar</span><span class="sxs-lookup"><span data-stu-id="2fea8-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2fea8-266">CC001</span><span class="sxs-lookup"><span data-stu-id="2fea8-266">CC001</span></span></td>
<td><span data-ttu-id="2fea8-267">İK</span><span class="sxs-lookup"><span data-stu-id="2fea8-267">HR</span></span></td>
<td><span data-ttu-id="2fea8-268">(1,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="2fea8-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="2fea8-269">1</span><span class="sxs-lookup"><span data-stu-id="2fea8-269">1</span></span></td>
<td><span data-ttu-id="2fea8-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="2fea8-271">500.00</span><span class="sxs-lookup"><span data-stu-id="2fea8-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-272">CC002</span><span class="sxs-lookup"><span data-stu-id="2fea8-272">CC002</span></span></td>
<td><span data-ttu-id="2fea8-273">Finans</span><span class="sxs-lookup"><span data-stu-id="2fea8-273">Finance</span></span></td>
<td><span data-ttu-id="2fea8-274">(6,000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="2fea8-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="2fea8-275">1</span><span class="sxs-lookup"><span data-stu-id="2fea8-275">1</span></span></td>
<td><span data-ttu-id="2fea8-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="2fea8-277">500.00</span><span class="sxs-lookup"><span data-stu-id="2fea8-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-278">CC003</span><span class="sxs-lookup"><span data-stu-id="2fea8-278">CC003</span></span></td>
<td><span data-ttu-id="2fea8-279">Montaj</span><span class="sxs-lookup"><span data-stu-id="2fea8-279">Assembly</span></span></td>
<td><span data-ttu-id="2fea8-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="2fea8-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="2fea8-281">0</span><span class="sxs-lookup"><span data-stu-id="2fea8-281">0</span></span></td>
<td><span data-ttu-id="2fea8-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="2fea8-283">0,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="2fea8-284">Günlük</span><span class="sxs-lookup"><span data-stu-id="2fea8-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2fea8-285">Günlük</span><span class="sxs-lookup"><span data-stu-id="2fea8-285">Journal</span></span></th>
<th><span data-ttu-id="2fea8-286">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="2fea8-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="2fea8-287">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="2fea8-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="2fea8-288">Sürüm</span><span class="sxs-lookup"><span data-stu-id="2fea8-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2fea8-289">00002</span><span class="sxs-lookup"><span data-stu-id="2fea8-289">00002</span></span></td>
<td><span data-ttu-id="2fea8-290">Maliyet dağıtımı hesaplama günlüğü</span><span class="sxs-lookup"><span data-stu-id="2fea8-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="2fea8-291">Mali</span><span class="sxs-lookup"><span data-stu-id="2fea8-291">Fiscal</span></span></td>
<td><span data-ttu-id="2fea8-292">2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-292">2017</span></span></td>
<td><span data-ttu-id="2fea8-293">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-293">Period 1</span></span></td>
<td><span data-ttu-id="2fea8-294">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="2fea8-295">Günlük girişleri (Maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="2fea8-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2fea8-296">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="2fea8-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="2fea8-297">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="2fea8-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="2fea8-298">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="2fea8-298">Cost element</span></span></th>
<th><span data-ttu-id="2fea8-299">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="2fea8-299">Cost behavior</span></span></th>
<th><span data-ttu-id="2fea8-300">Tutar</span><span class="sxs-lookup"><span data-stu-id="2fea8-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2fea8-301">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="2fea8-302">CC099</span><span class="sxs-lookup"><span data-stu-id="2fea8-302">CC099</span></span></td>
<td><span data-ttu-id="2fea8-303">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="2fea8-303">Default cost center</span></span></td>
<td><span data-ttu-id="2fea8-304">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-304">10001</span></span></td>
<td><span data-ttu-id="2fea8-305">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-305">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-306">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-306">Fixed cost</span></span></td>
<td><span data-ttu-id="2fea8-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-308">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="2fea8-309">CC099</span><span class="sxs-lookup"><span data-stu-id="2fea8-309">CC099</span></span></td>
<td><span data-ttu-id="2fea8-310">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="2fea8-310">Default cost center</span></span></td>
<td><span data-ttu-id="2fea8-311">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-311">10001</span></span></td>
<td><span data-ttu-id="2fea8-312">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-312">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-313">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-313">Variable cost</span></span></td>
<td><span data-ttu-id="2fea8-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="2fea8-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="2fea8-315">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="2fea8-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2fea8-316">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="2fea8-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="2fea8-317">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="2fea8-317">Cost element</span></span></th>
<th><span data-ttu-id="2fea8-318">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="2fea8-318">Cost behavior</span></span></th>
<th><span data-ttu-id="2fea8-319">Tutar</span><span class="sxs-lookup"><span data-stu-id="2fea8-319">Amount</span></span></th>
<th><span data-ttu-id="2fea8-320">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="2fea8-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2fea8-321">CC099</span><span class="sxs-lookup"><span data-stu-id="2fea8-321">CC099</span></span></td>
<td><span data-ttu-id="2fea8-322">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="2fea8-322">Default cost center</span></span></td>
<td><span data-ttu-id="2fea8-323">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-323">10001</span></span></td>
<td><span data-ttu-id="2fea8-324">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-324">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-325">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-325">Fixed cost</span></span></td>
<td><span data-ttu-id="2fea8-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-326">-1,000.00</span></span></td>
<td><span data-ttu-id="2fea8-327">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-328">CC001</span><span class="sxs-lookup"><span data-stu-id="2fea8-328">CC001</span></span></td>
<td><span data-ttu-id="2fea8-329">İK</span><span class="sxs-lookup"><span data-stu-id="2fea8-329">HR</span></span></td>
<td><span data-ttu-id="2fea8-330">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-330">10001</span></span></td>
<td><span data-ttu-id="2fea8-331">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-331">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-332">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-332">Fixed cost</span></span></td>
<td><span data-ttu-id="2fea8-333">500.00</span><span class="sxs-lookup"><span data-stu-id="2fea8-333">500.00</span></span></td>
<td><span data-ttu-id="2fea8-334">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-335">CC002</span><span class="sxs-lookup"><span data-stu-id="2fea8-335">CC002</span></span></td>
<td><span data-ttu-id="2fea8-336">Finans</span><span class="sxs-lookup"><span data-stu-id="2fea8-336">Finance</span></span></td>
<td><span data-ttu-id="2fea8-337">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-337">10001</span></span></td>
<td><span data-ttu-id="2fea8-338">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-338">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-339">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-339">Fixed cost</span></span></td>
<td><span data-ttu-id="2fea8-340">500.00</span><span class="sxs-lookup"><span data-stu-id="2fea8-340">500.00</span></span></td>
<td><span data-ttu-id="2fea8-341">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-342">CC099</span><span class="sxs-lookup"><span data-stu-id="2fea8-342">CC099</span></span></td>
<td><span data-ttu-id="2fea8-343">Varsayılan maliyet merkezi</span><span class="sxs-lookup"><span data-stu-id="2fea8-343">Default cost center</span></span></td>
<td><span data-ttu-id="2fea8-344">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-344">10001</span></span></td>
<td><span data-ttu-id="2fea8-345">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-345">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-346">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-346">Variable cost</span></span></td>
<td><span data-ttu-id="2fea8-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-347">-9,000.00</span></span></td>
<td><span data-ttu-id="2fea8-348">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-349">CC001</span><span class="sxs-lookup"><span data-stu-id="2fea8-349">CC001</span></span></td>
<td><span data-ttu-id="2fea8-350">İK</span><span class="sxs-lookup"><span data-stu-id="2fea8-350">HR</span></span></td>
<td><span data-ttu-id="2fea8-351">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-351">10001</span></span></td>
<td><span data-ttu-id="2fea8-352">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-352">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-353">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-353">Variable cost</span></span></td>
<td><span data-ttu-id="2fea8-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="2fea8-354">1,285.71</span></span></td>
<td><span data-ttu-id="2fea8-355">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-356">CC002</span><span class="sxs-lookup"><span data-stu-id="2fea8-356">CC002</span></span></td>
<td><span data-ttu-id="2fea8-357">Finans</span><span class="sxs-lookup"><span data-stu-id="2fea8-357">Finance</span></span></td>
<td><span data-ttu-id="2fea8-358">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-358">10001</span></span></td>
<td><span data-ttu-id="2fea8-359">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-359">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-360">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-360">Variable cost</span></span></td>
<td><span data-ttu-id="2fea8-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="2fea8-361">7,714.29</span></span></td>
<td><span data-ttu-id="2fea8-362">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2fea8-363">Daha fazla bilgi için bkz. [Maliyet dağıtımı ilkesi oluşturma ve bir maliyet kontrol birimine atama](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="2fea8-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="2fea8-364">Adım 3: Genel gider oranı hesaplama işlemi</span><span class="sxs-lookup"><span data-stu-id="2fea8-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="2fea8-365">Genel gider oranı, bir veya birden fazla belirli maliyet nesnesine masraf yüklemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2fea8-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="2fea8-366">Masraf, önceden belirlenmiş maliyet oranına ve tahsisat tabanından hesaplanan büyüklüğe dayanır.</span><span class="sxs-lookup"><span data-stu-id="2fea8-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="2fea8-367">Genel gider oranını tanımlama</span><span class="sxs-lookup"><span data-stu-id="2fea8-367">Define the overhead rate</span></span>

<span data-ttu-id="2fea8-368">Maliyet nesnesi CC001 HR, bir dizi dahili projeye katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="2fea8-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="2fea8-369">HR projeleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2fea8-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2fea8-370">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="2fea8-370">Cost object</span></span></th>
<th><span data-ttu-id="2fea8-371">Saatler</span><span class="sxs-lookup"><span data-stu-id="2fea8-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2fea8-372">Proj 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-372">Proj 1</span></span></td>
<td><span data-ttu-id="2fea8-373">Proje 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-373">Project 1</span></span></td>
<td><span data-ttu-id="2fea8-374">3</span><span class="sxs-lookup"><span data-stu-id="2fea8-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-375">Proj 2</span><span class="sxs-lookup"><span data-stu-id="2fea8-375">Proj 2</span></span></td>
<td><span data-ttu-id="2fea8-376">Proje 2</span><span class="sxs-lookup"><span data-stu-id="2fea8-376">Project 2</span></span></td>
<td><span data-ttu-id="2fea8-377">1</span><span class="sxs-lookup"><span data-stu-id="2fea8-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2fea8-378">Maliyet projeleri dağıtımı için bir önceden belirlenmiş maliyet oranı tanımlandı.</span><span class="sxs-lookup"><span data-stu-id="2fea8-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2fea8-379">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="2fea8-379">Cost object</span></span></th>
<th><span data-ttu-id="2fea8-380">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="2fea8-380">Cost element</span></span></th>
<th><span data-ttu-id="2fea8-381">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="2fea8-381">Cost behavior</span></span></th>
<th><span data-ttu-id="2fea8-382">Birimler</span><span class="sxs-lookup"><span data-stu-id="2fea8-382">Units</span></span></th>
<th><span data-ttu-id="2fea8-383">Ücret</span><span class="sxs-lookup"><span data-stu-id="2fea8-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2fea8-384">CC001</span><span class="sxs-lookup"><span data-stu-id="2fea8-384">CC001</span></span></td>
<td><span data-ttu-id="2fea8-385">İK</span><span class="sxs-lookup"><span data-stu-id="2fea8-385">HR</span></span></td>
<td><span data-ttu-id="2fea8-386">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-386">10001</span></span></td>
<td><span data-ttu-id="2fea8-387">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-387">Variable cost</span></span></td>
<td><span data-ttu-id="2fea8-388">1</span><span class="sxs-lookup"><span data-stu-id="2fea8-388">1</span></span></td>
<td><span data-ttu-id="2fea8-389">10</span><span class="sxs-lookup"><span data-stu-id="2fea8-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2fea8-390">Aşağıdaki tablo, HR projeleri bir tahsisat tabanı olarak uygulandığındaki sonuçları gösterir.</span><span class="sxs-lookup"><span data-stu-id="2fea8-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2fea8-391">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="2fea8-391">Cost object</span></span></th>
<th><span data-ttu-id="2fea8-392">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="2fea8-392">Magnitude</span></span></th>
<th><span data-ttu-id="2fea8-393">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="2fea8-393">Cost element</span></span></th>
<th><span data-ttu-id="2fea8-394">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="2fea8-394">Allocation factor</span></span></th>
<th><span data-ttu-id="2fea8-395">Tutar</span><span class="sxs-lookup"><span data-stu-id="2fea8-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2fea8-396">Proj 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-396">Proj 1</span></span></td>
<td><span data-ttu-id="2fea8-397">Proje 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-397">Project 1</span></span></td>
<td><span data-ttu-id="2fea8-398">3</span><span class="sxs-lookup"><span data-stu-id="2fea8-398">3</span></span></td>
<td><span data-ttu-id="2fea8-399">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-399">10001</span></span></td>
<td><span data-ttu-id="2fea8-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="2fea8-401">30.00</span><span class="sxs-lookup"><span data-stu-id="2fea8-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-402">Proj 2</span><span class="sxs-lookup"><span data-stu-id="2fea8-402">Proj 2</span></span></td>
<td><span data-ttu-id="2fea8-403">Proje 2</span><span class="sxs-lookup"><span data-stu-id="2fea8-403">Project 2</span></span></td>
<td><span data-ttu-id="2fea8-404">1</span><span class="sxs-lookup"><span data-stu-id="2fea8-404">1</span></span></td>
<td><span data-ttu-id="2fea8-405">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-405">10001</span></span></td>
<td><span data-ttu-id="2fea8-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="2fea8-407">10,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="2fea8-408">Günlük</span><span class="sxs-lookup"><span data-stu-id="2fea8-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2fea8-409">Günlük</span><span class="sxs-lookup"><span data-stu-id="2fea8-409">Journal</span></span></th>
<th><span data-ttu-id="2fea8-410">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="2fea8-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="2fea8-411">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="2fea8-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="2fea8-412">Sürüm</span><span class="sxs-lookup"><span data-stu-id="2fea8-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2fea8-413">00003</span><span class="sxs-lookup"><span data-stu-id="2fea8-413">00003</span></span></td>
<td><span data-ttu-id="2fea8-414">Genel gider oranı hesaplaması günlüğü</span><span class="sxs-lookup"><span data-stu-id="2fea8-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="2fea8-415">Mali</span><span class="sxs-lookup"><span data-stu-id="2fea8-415">Fiscal</span></span></td>
<td><span data-ttu-id="2fea8-416">2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-416">2017</span></span></td>
<td><span data-ttu-id="2fea8-417">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-417">Period 1</span></span></td>
<td><span data-ttu-id="2fea8-418">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="2fea8-419">Günlük girişleri (Genel gider oranı hesaplaması için günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="2fea8-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2fea8-420">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="2fea8-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="2fea8-421">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="2fea8-421">Cost object</span></span></th>
<th><span data-ttu-id="2fea8-422">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="2fea8-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2fea8-423">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="2fea8-424">Proj 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-424">Proj 1</span></span></td>
<td><span data-ttu-id="2fea8-425">Dahili Proj 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="2fea8-426">3,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-427">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="2fea8-428">Proj 2</span><span class="sxs-lookup"><span data-stu-id="2fea8-428">Proj 2</span></span></td>
<td><span data-ttu-id="2fea8-429">Dahili Proj 2</span><span class="sxs-lookup"><span data-stu-id="2fea8-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="2fea8-430">1.00</span><span class="sxs-lookup"><span data-stu-id="2fea8-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="2fea8-431">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="2fea8-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2fea8-432">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="2fea8-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="2fea8-433">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="2fea8-433">Cost element</span></span></th>
<th><span data-ttu-id="2fea8-434">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="2fea8-434">Cost behavior</span></span></th>
<th><span data-ttu-id="2fea8-435">Tutar</span><span class="sxs-lookup"><span data-stu-id="2fea8-435">Amount</span></span></th>
<th><span data-ttu-id="2fea8-436">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="2fea8-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2fea8-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="2fea8-437">CC0001</span></span></td>
<td><span data-ttu-id="2fea8-438">İK</span><span class="sxs-lookup"><span data-stu-id="2fea8-438">HR</span></span></td>
<td><span data-ttu-id="2fea8-439">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-439">10001</span></span></td>
<td><span data-ttu-id="2fea8-440">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-440">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-441">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-441">Variable cost</span></span></td>
<td><span data-ttu-id="2fea8-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-442">-30.00</span></span></td>
<td><span data-ttu-id="2fea8-443">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-444">Proj 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-444">Proj 1</span></span></td>
<td><span data-ttu-id="2fea8-445">Dahili Proj 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="2fea8-446">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-446">10001</span></span></td>
<td><span data-ttu-id="2fea8-447">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-447">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-448">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-448">Variable cost</span></span></td>
<td><span data-ttu-id="2fea8-449">30.00</span><span class="sxs-lookup"><span data-stu-id="2fea8-449">30.00</span></span></td>
<td><span data-ttu-id="2fea8-450">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-451">CC001</span><span class="sxs-lookup"><span data-stu-id="2fea8-451">CC001</span></span></td>
<td><span data-ttu-id="2fea8-452">İK</span><span class="sxs-lookup"><span data-stu-id="2fea8-452">HR</span></span></td>
<td><span data-ttu-id="2fea8-453">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-453">10001</span></span></td>
<td><span data-ttu-id="2fea8-454">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-454">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-455">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-455">Variable cost</span></span></td>
<td><span data-ttu-id="2fea8-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-456">-10.00</span></span></td>
<td><span data-ttu-id="2fea8-457">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-458">Proj 2</span><span class="sxs-lookup"><span data-stu-id="2fea8-458">Proj 2</span></span></td>
<td><span data-ttu-id="2fea8-459">Dahili Proj 2</span><span class="sxs-lookup"><span data-stu-id="2fea8-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="2fea8-460">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-460">10001</span></span></td>
<td><span data-ttu-id="2fea8-461">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-461">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-462">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-462">Variable cost</span></span></td>
<td><span data-ttu-id="2fea8-463">10,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-463">10.00</span></span></td>
<td><span data-ttu-id="2fea8-464">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2fea8-465">Daha fazla bilgi için [Genel gider hesaplaması gerçekleştir](cost-rollup.md#perform-overhead-calculation) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="2fea8-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="2fea8-466">Adım 4: Maliyet tahsisat hesaplamayı işle</span><span class="sxs-lookup"><span data-stu-id="2fea8-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="2fea8-467">Tahsisat, bir tahsisat tabanı kullanarak bir maliyet nesnesinin diğer maliyet nesnelerine bakiyesini tahsis eder.</span><span class="sxs-lookup"><span data-stu-id="2fea8-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="2fea8-468">Finance and Operations karşılıklı tahsisat yöntemin destekler.</span><span class="sxs-lookup"><span data-stu-id="2fea8-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="2fea8-469">Karşılıklı tahsisat yönteminde, yardımcı maliyet nesnelerinin değiştiği karşılıklı hizmetler tümüyle tanınır.</span><span class="sxs-lookup"><span data-stu-id="2fea8-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="2fea8-470">Sistem, tahsisatların doğru gerçekleştireceği sırayı otomatik olarak belirler.</span><span class="sxs-lookup"><span data-stu-id="2fea8-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="2fea8-471">Bir maliyet nesnesinin bakiyesi tek bir tahsisat tabanı tarafından tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="2fea8-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="2fea8-472">Yeni maliyet nesnesi boyutları arasındaki tahsisatlar ve onların üyeleri desteklenir.</span><span class="sxs-lookup"><span data-stu-id="2fea8-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="2fea8-473">Tahsisatın sırası, maliyet kontrol birimi tarafından kontrol edilir.</span><span class="sxs-lookup"><span data-stu-id="2fea8-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="2fea8-474">[![Karşılıklı yöntemi](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="2fea8-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="2fea8-475">Maliyet tahsisatını tanımla</span><span class="sxs-lookup"><span data-stu-id="2fea8-475">Define the cost allocation</span></span>

<span data-ttu-id="2fea8-476">Bir maliyetin akışını nasıl izleyeceğinize dair basit bir örnek aşağıda verilmiştir,</span><span class="sxs-lookup"><span data-stu-id="2fea8-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="2fea8-477">Maliyet nesnesi CC001 HR, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="2fea8-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="2fea8-478">HR hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2fea8-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2fea8-479">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="2fea8-479">Cost object</span></span></th>
<th><span data-ttu-id="2fea8-480">HR hizmetleri</span><span class="sxs-lookup"><span data-stu-id="2fea8-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2fea8-481">CC002</span><span class="sxs-lookup"><span data-stu-id="2fea8-481">CC002</span></span></td>
<td><span data-ttu-id="2fea8-482">Finans</span><span class="sxs-lookup"><span data-stu-id="2fea8-482">Finance</span></span></td>
<td><span data-ttu-id="2fea8-483">35</span><span class="sxs-lookup"><span data-stu-id="2fea8-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-484">CC003</span><span class="sxs-lookup"><span data-stu-id="2fea8-484">CC003</span></span></td>
<td><span data-ttu-id="2fea8-485">Montaj</span><span class="sxs-lookup"><span data-stu-id="2fea8-485">Assembly</span></span></td>
<td><span data-ttu-id="2fea8-486">55</span><span class="sxs-lookup"><span data-stu-id="2fea8-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-487">CC004</span><span class="sxs-lookup"><span data-stu-id="2fea8-487">CC004</span></span></td>
<td><span data-ttu-id="2fea8-488">Paketleme</span><span class="sxs-lookup"><span data-stu-id="2fea8-488">Packaging</span></span></td>
<td><span data-ttu-id="2fea8-489">10</span><span class="sxs-lookup"><span data-stu-id="2fea8-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2fea8-490">Maliyet nesnesi CC002 Finans, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="2fea8-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="2fea8-491">Finans hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2fea8-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2fea8-492">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="2fea8-492">Cost object</span></span></th>
<th><span data-ttu-id="2fea8-493">Finans hizmetleri</span><span class="sxs-lookup"><span data-stu-id="2fea8-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2fea8-494">CC003</span><span class="sxs-lookup"><span data-stu-id="2fea8-494">CC003</span></span></td>
<td><span data-ttu-id="2fea8-495">Montaj</span><span class="sxs-lookup"><span data-stu-id="2fea8-495">Assembly</span></span></td>
<td><span data-ttu-id="2fea8-496">65</span><span class="sxs-lookup"><span data-stu-id="2fea8-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-497">CC004</span><span class="sxs-lookup"><span data-stu-id="2fea8-497">CC004</span></span></td>
<td><span data-ttu-id="2fea8-498">Paketleme</span><span class="sxs-lookup"><span data-stu-id="2fea8-498">Packaging</span></span></td>
<td><span data-ttu-id="2fea8-499">35</span><span class="sxs-lookup"><span data-stu-id="2fea8-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2fea8-500">Maliyet nesnesi CC003 Derleme, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="2fea8-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="2fea8-501">Derleme hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2fea8-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2fea8-502">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="2fea8-502">Cost object</span></span></th>
<th><span data-ttu-id="2fea8-503">Derleme Hizmetleri (saat)</span><span class="sxs-lookup"><span data-stu-id="2fea8-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2fea8-504">Prod 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-504">Prod 1</span></span></td>
<td><span data-ttu-id="2fea8-505">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-505">Product 1</span></span></td>
<td><span data-ttu-id="2fea8-506">60</span><span class="sxs-lookup"><span data-stu-id="2fea8-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-507">Prod 2</span><span class="sxs-lookup"><span data-stu-id="2fea8-507">Prod 2</span></span></td>
<td><span data-ttu-id="2fea8-508">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="2fea8-508">Product 2</span></span></td>
<td><span data-ttu-id="2fea8-509">20</span><span class="sxs-lookup"><span data-stu-id="2fea8-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2fea8-510">Maliyet nesnesi CC004 Ambalajlama, birden fazla maliyet nesnesine katkıda bulunur.</span><span class="sxs-lookup"><span data-stu-id="2fea8-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="2fea8-511">Ambalajlama hizmetleri olarak adlandırılan bir istatistiki boyut üyesi, tüketilen büyüklüğü ölçmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2fea8-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2fea8-512">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="2fea8-512">Cost object</span></span></th>
<th><span data-ttu-id="2fea8-513">Ambalajlama hizmetleri (saat)</span><span class="sxs-lookup"><span data-stu-id="2fea8-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2fea8-514">Prod 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-514">Prod 1</span></span></td>
<td><span data-ttu-id="2fea8-515">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-515">Product 1</span></span></td>
<td><span data-ttu-id="2fea8-516">80</span><span class="sxs-lookup"><span data-stu-id="2fea8-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-517">Prod 2</span><span class="sxs-lookup"><span data-stu-id="2fea8-517">Prod 2</span></span></td>
<td><span data-ttu-id="2fea8-518">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="2fea8-518">Product 2</span></span></td>
<td><span data-ttu-id="2fea8-519">15</span><span class="sxs-lookup"><span data-stu-id="2fea8-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="2fea8-520">Finance and Operations'ta, bir ürünün tükettiği üretim saatleri gibi istatistiki ölçümler doğrudan kaynak verisinden alınabilir.</span><span class="sxs-lookup"><span data-stu-id="2fea8-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="2fea8-521">Daha fazla bilgi için, [İstatistiksel ölçüm sağlayıcı şablonu](statistical-measure-provider-template.md#statistical-measure-provider-template) bakın.</span><span class="sxs-lookup"><span data-stu-id="2fea8-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="2fea8-522">Aşağıdaki tablo, İK hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığında ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="2fea8-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2fea8-523">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="2fea8-523">Cost object</span></span></th>
<th><span data-ttu-id="2fea8-524">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="2fea8-524">Magnitude</span></span></th>
<th><span data-ttu-id="2fea8-525">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="2fea8-525">Allocation factor</span></span></th>
<th><span data-ttu-id="2fea8-526">Tutar</span><span class="sxs-lookup"><span data-stu-id="2fea8-526">Amount</span></span></th>
<th><span data-ttu-id="2fea8-527">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="2fea8-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2fea8-528">CC002</span><span class="sxs-lookup"><span data-stu-id="2fea8-528">CC002</span></span></td>
<td><span data-ttu-id="2fea8-529">Finans</span><span class="sxs-lookup"><span data-stu-id="2fea8-529">Finance</span></span></td>
<td><span data-ttu-id="2fea8-530">35</span><span class="sxs-lookup"><span data-stu-id="2fea8-530">35</span></span></td>
<td><span data-ttu-id="2fea8-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="2fea8-532">175.00</span><span class="sxs-lookup"><span data-stu-id="2fea8-532">175.00</span></span></td>
<td><span data-ttu-id="2fea8-533">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-534">CC003</span><span class="sxs-lookup"><span data-stu-id="2fea8-534">CC003</span></span></td>
<td><span data-ttu-id="2fea8-535">Montaj</span><span class="sxs-lookup"><span data-stu-id="2fea8-535">Assembly</span></span></td>
<td><span data-ttu-id="2fea8-536">55</span><span class="sxs-lookup"><span data-stu-id="2fea8-536">55</span></span></td>
<td><span data-ttu-id="2fea8-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="2fea8-538">275.00</span><span class="sxs-lookup"><span data-stu-id="2fea8-538">275.00</span></span></td>
<td><span data-ttu-id="2fea8-539">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-540">CC004</span><span class="sxs-lookup"><span data-stu-id="2fea8-540">CC004</span></span></td>
<td><span data-ttu-id="2fea8-541">Paketleme</span><span class="sxs-lookup"><span data-stu-id="2fea8-541">Packaging</span></span></td>
<td><span data-ttu-id="2fea8-542">10</span><span class="sxs-lookup"><span data-stu-id="2fea8-542">10</span></span></td>
<td><span data-ttu-id="2fea8-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="2fea8-544">50,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-544">50.00</span></span></td>
<td><span data-ttu-id="2fea8-545">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-546">CC002</span><span class="sxs-lookup"><span data-stu-id="2fea8-546">CC002</span></span></td>
<td><span data-ttu-id="2fea8-547">Finans</span><span class="sxs-lookup"><span data-stu-id="2fea8-547">Finance</span></span></td>
<td><span data-ttu-id="2fea8-548">35</span><span class="sxs-lookup"><span data-stu-id="2fea8-548">35</span></span></td>
<td><span data-ttu-id="2fea8-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="2fea8-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="2fea8-550">436.00</span><span class="sxs-lookup"><span data-stu-id="2fea8-550">436.00</span></span></td>
<td><span data-ttu-id="2fea8-551">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-552">CC003</span><span class="sxs-lookup"><span data-stu-id="2fea8-552">CC003</span></span></td>
<td><span data-ttu-id="2fea8-553">Montaj</span><span class="sxs-lookup"><span data-stu-id="2fea8-553">Assembly</span></span></td>
<td><span data-ttu-id="2fea8-554">55</span><span class="sxs-lookup"><span data-stu-id="2fea8-554">55</span></span></td>
<td><span data-ttu-id="2fea8-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="2fea8-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="2fea8-556">685.14</span><span class="sxs-lookup"><span data-stu-id="2fea8-556">685.14</span></span></td>
<td><span data-ttu-id="2fea8-557">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-558">CC004</span><span class="sxs-lookup"><span data-stu-id="2fea8-558">CC004</span></span></td>
<td><span data-ttu-id="2fea8-559">Paketleme</span><span class="sxs-lookup"><span data-stu-id="2fea8-559">Packaging</span></span></td>
<td><span data-ttu-id="2fea8-560">10</span><span class="sxs-lookup"><span data-stu-id="2fea8-560">10</span></span></td>
<td><span data-ttu-id="2fea8-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="2fea8-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="2fea8-562">124.57</span><span class="sxs-lookup"><span data-stu-id="2fea8-562">124.57</span></span></td>
<td><span data-ttu-id="2fea8-563">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2fea8-564">Aşağıdaki tablo, Finans hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="2fea8-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2fea8-565">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="2fea8-565">Cost object</span></span></th>
<th><span data-ttu-id="2fea8-566">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="2fea8-566">Magnitude</span></span></th>
<th><span data-ttu-id="2fea8-567">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="2fea8-567">Allocation factor</span></span></th>
<th><span data-ttu-id="2fea8-568">Tutar</span><span class="sxs-lookup"><span data-stu-id="2fea8-568">Amount</span></span></th>
<th><span data-ttu-id="2fea8-569">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="2fea8-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2fea8-570">CC003</span><span class="sxs-lookup"><span data-stu-id="2fea8-570">CC003</span></span></td>
<td><span data-ttu-id="2fea8-571">Montaj</span><span class="sxs-lookup"><span data-stu-id="2fea8-571">Assembly</span></span></td>
<td><span data-ttu-id="2fea8-572">65</span><span class="sxs-lookup"><span data-stu-id="2fea8-572">65</span></span></td>
<td><span data-ttu-id="2fea8-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="2fea8-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="2fea8-574">438.75</span><span class="sxs-lookup"><span data-stu-id="2fea8-574">438.75</span></span></td>
<td><span data-ttu-id="2fea8-575">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-576">CC004</span><span class="sxs-lookup"><span data-stu-id="2fea8-576">CC004</span></span></td>
<td><span data-ttu-id="2fea8-577">Paketleme</span><span class="sxs-lookup"><span data-stu-id="2fea8-577">Packaging</span></span></td>
<td><span data-ttu-id="2fea8-578">35</span><span class="sxs-lookup"><span data-stu-id="2fea8-578">35</span></span></td>
<td><span data-ttu-id="2fea8-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="2fea8-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="2fea8-580">236.25</span><span class="sxs-lookup"><span data-stu-id="2fea8-580">236.25</span></span></td>
<td><span data-ttu-id="2fea8-581">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-582">CC003</span><span class="sxs-lookup"><span data-stu-id="2fea8-582">CC003</span></span></td>
<td><span data-ttu-id="2fea8-583">Montaj</span><span class="sxs-lookup"><span data-stu-id="2fea8-583">Assembly</span></span></td>
<td><span data-ttu-id="2fea8-584">65</span><span class="sxs-lookup"><span data-stu-id="2fea8-584">65</span></span></td>
<td><span data-ttu-id="2fea8-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="2fea8-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="2fea8-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="2fea8-586">5,297.69</span></span></td>
<td><span data-ttu-id="2fea8-587">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-588">CC004</span><span class="sxs-lookup"><span data-stu-id="2fea8-588">CC004</span></span></td>
<td><span data-ttu-id="2fea8-589">Paketleme</span><span class="sxs-lookup"><span data-stu-id="2fea8-589">Packaging</span></span></td>
<td><span data-ttu-id="2fea8-590">35</span><span class="sxs-lookup"><span data-stu-id="2fea8-590">35</span></span></td>
<td><span data-ttu-id="2fea8-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="2fea8-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="2fea8-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="2fea8-592">2,852.60</span></span></td>
<td><span data-ttu-id="2fea8-593">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2fea8-594">Aşağıdaki tablo, Derleme hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="2fea8-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2fea8-595">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="2fea8-595">Cost object</span></span></th>
<th><span data-ttu-id="2fea8-596">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="2fea8-596">Magnitude</span></span></th>
<th><span data-ttu-id="2fea8-597">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="2fea8-597">Allocation factor</span></span></th>
<th><span data-ttu-id="2fea8-598">Tutar</span><span class="sxs-lookup"><span data-stu-id="2fea8-598">Amount</span></span></th>
<th><span data-ttu-id="2fea8-599">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="2fea8-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2fea8-600">Prod 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-600">Prod 1</span></span></td>
<td><span data-ttu-id="2fea8-601">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-601">Product 1</span></span></td>
<td><span data-ttu-id="2fea8-602">60</span><span class="sxs-lookup"><span data-stu-id="2fea8-602">60</span></span></td>
<td><span data-ttu-id="2fea8-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="2fea8-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="2fea8-604">535.31</span><span class="sxs-lookup"><span data-stu-id="2fea8-604">535.31</span></span></td>
<td><span data-ttu-id="2fea8-605">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-606">Prod 2</span><span class="sxs-lookup"><span data-stu-id="2fea8-606">Prod 2</span></span></td>
<td><span data-ttu-id="2fea8-607">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="2fea8-607">Product 2</span></span></td>
<td><span data-ttu-id="2fea8-608">20</span><span class="sxs-lookup"><span data-stu-id="2fea8-608">20</span></span></td>
<td><span data-ttu-id="2fea8-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="2fea8-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="2fea8-610">178.44</span><span class="sxs-lookup"><span data-stu-id="2fea8-610">178.44</span></span></td>
<td><span data-ttu-id="2fea8-611">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-612">Prod 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-612">Prod 1</span></span></td>
<td><span data-ttu-id="2fea8-613">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-613">Product 1</span></span></td>
<td><span data-ttu-id="2fea8-614">60</span><span class="sxs-lookup"><span data-stu-id="2fea8-614">60</span></span></td>
<td><span data-ttu-id="2fea8-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="2fea8-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="2fea8-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="2fea8-616">4,487.12</span></span></td>
<td><span data-ttu-id="2fea8-617">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-618">Prod 2</span><span class="sxs-lookup"><span data-stu-id="2fea8-618">Prod 2</span></span></td>
<td><span data-ttu-id="2fea8-619">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="2fea8-619">Product 2</span></span></td>
<td><span data-ttu-id="2fea8-620">20</span><span class="sxs-lookup"><span data-stu-id="2fea8-620">20</span></span></td>
<td><span data-ttu-id="2fea8-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="2fea8-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="2fea8-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="2fea8-622">1,495.71</span></span></td>
<td><span data-ttu-id="2fea8-623">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2fea8-624">Aşağıdaki tablo, Paketleme hizmetleri toplam maliyet için bir tahsisat tabanı olarak ayarlandığnda ortaya çıkan sonucu gösterir.</span><span class="sxs-lookup"><span data-stu-id="2fea8-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2fea8-625">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="2fea8-625">Cost object</span></span></th>
<th><span data-ttu-id="2fea8-626">Büyüklük</span><span class="sxs-lookup"><span data-stu-id="2fea8-626">Magnitude</span></span></th>
<th><span data-ttu-id="2fea8-627">Tahsisat faktörü</span><span class="sxs-lookup"><span data-stu-id="2fea8-627">Allocation factor</span></span></th>
<th><span data-ttu-id="2fea8-628">Tutar</span><span class="sxs-lookup"><span data-stu-id="2fea8-628">Amount</span></span></th>
<th><span data-ttu-id="2fea8-629">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="2fea8-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2fea8-630">Prod 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-630">Prod 1</span></span></td>
<td><span data-ttu-id="2fea8-631">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-631">Product 1</span></span></td>
<td><span data-ttu-id="2fea8-632">80</span><span class="sxs-lookup"><span data-stu-id="2fea8-632">80</span></span></td>
<td><span data-ttu-id="2fea8-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="2fea8-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="2fea8-634">241.05</span><span class="sxs-lookup"><span data-stu-id="2fea8-634">241.05</span></span></td>
<td><span data-ttu-id="2fea8-635">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-636">Prod 2</span><span class="sxs-lookup"><span data-stu-id="2fea8-636">Prod 2</span></span></td>
<td><span data-ttu-id="2fea8-637">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="2fea8-637">Product 2</span></span></td>
<td><span data-ttu-id="2fea8-638">15</span><span class="sxs-lookup"><span data-stu-id="2fea8-638">15</span></span></td>
<td><span data-ttu-id="2fea8-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="2fea8-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="2fea8-640">45.20</span><span class="sxs-lookup"><span data-stu-id="2fea8-640">45.20</span></span></td>
<td><span data-ttu-id="2fea8-641">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-642">Prod 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-642">Prod 1</span></span></td>
<td><span data-ttu-id="2fea8-643">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-643">Product 1</span></span></td>
<td><span data-ttu-id="2fea8-644">80</span><span class="sxs-lookup"><span data-stu-id="2fea8-644">80</span></span></td>
<td><span data-ttu-id="2fea8-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="2fea8-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="2fea8-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="2fea8-646">2,507.09</span></span></td>
<td><span data-ttu-id="2fea8-647">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-648">Prod 2</span><span class="sxs-lookup"><span data-stu-id="2fea8-648">Prod 2</span></span></td>
<td><span data-ttu-id="2fea8-649">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="2fea8-649">Product 2</span></span></td>
<td><span data-ttu-id="2fea8-650">15</span><span class="sxs-lookup"><span data-stu-id="2fea8-650">15</span></span></td>
<td><span data-ttu-id="2fea8-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="2fea8-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="2fea8-652">470.08</span><span class="sxs-lookup"><span data-stu-id="2fea8-652">470.08</span></span></td>
<td><span data-ttu-id="2fea8-653">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="2fea8-654">Günlük girişleri (maliyet nesnesi bakiyesi günlük girişleri)</span><span class="sxs-lookup"><span data-stu-id="2fea8-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2fea8-655">Günlük</span><span class="sxs-lookup"><span data-stu-id="2fea8-655">Journal</span></span></th>
<th><span data-ttu-id="2fea8-656">Günlük türü:</span><span class="sxs-lookup"><span data-stu-id="2fea8-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="2fea8-657">Mali takvim dönemi</span><span class="sxs-lookup"><span data-stu-id="2fea8-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="2fea8-658">Sürüm</span><span class="sxs-lookup"><span data-stu-id="2fea8-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2fea8-659">00004</span><span class="sxs-lookup"><span data-stu-id="2fea8-659">00004</span></span></td>
<td><span data-ttu-id="2fea8-660">Maliyet tahsisatı günlüğü</span><span class="sxs-lookup"><span data-stu-id="2fea8-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="2fea8-661">Mali</span><span class="sxs-lookup"><span data-stu-id="2fea8-661">Fiscal</span></span></td>
<td><span data-ttu-id="2fea8-662">2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-662">2017</span></span></td>
<td><span data-ttu-id="2fea8-663">Dönem 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-663">Period 1</span></span></td>
<td><span data-ttu-id="2fea8-664">Genel gider hesaplama / 01-02-2017 23:51:00 / Genel muhasebe /2017 / Dönem 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="2fea8-665">Günlük satırları</span><span class="sxs-lookup"><span data-stu-id="2fea8-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="2fea8-666">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="2fea8-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="2fea8-667">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="2fea8-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="2fea8-668">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="2fea8-668">Cost element</span></span></th>
<th><span data-ttu-id="2fea8-669">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="2fea8-669">Cost behavior</span></span></th>
<th><span data-ttu-id="2fea8-670">Tutar</span><span class="sxs-lookup"><span data-stu-id="2fea8-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2fea8-671">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="2fea8-672">CC001</span><span class="sxs-lookup"><span data-stu-id="2fea8-672">CC001</span></span></td>
<td><span data-ttu-id="2fea8-673">İK</span><span class="sxs-lookup"><span data-stu-id="2fea8-673">HR</span></span></td>
<td><span data-ttu-id="2fea8-674">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-674">10001</span></span></td>
<td><span data-ttu-id="2fea8-675">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-675">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-676">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-676">Fixed cost</span></span></td>
<td><span data-ttu-id="2fea8-677">500.00</span><span class="sxs-lookup"><span data-stu-id="2fea8-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-678">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="2fea8-679">CC001</span><span class="sxs-lookup"><span data-stu-id="2fea8-679">CC001</span></span></td>
<td><span data-ttu-id="2fea8-680">İK</span><span class="sxs-lookup"><span data-stu-id="2fea8-680">HR</span></span></td>
<td><span data-ttu-id="2fea8-681">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-681">10001</span></span></td>
<td><span data-ttu-id="2fea8-682">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-682">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-683">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-683">Variable cost</span></span></td>
<td><span data-ttu-id="2fea8-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="2fea8-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-685">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="2fea8-686">CC002</span><span class="sxs-lookup"><span data-stu-id="2fea8-686">CC002</span></span></td>
<td><span data-ttu-id="2fea8-687">Finans</span><span class="sxs-lookup"><span data-stu-id="2fea8-687">Finance</span></span></td>
<td><span data-ttu-id="2fea8-688">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-688">10001</span></span></td>
<td><span data-ttu-id="2fea8-689">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-689">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-690">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-690">Fixed cost</span></span></td>
<td><span data-ttu-id="2fea8-691">675.00</span><span class="sxs-lookup"><span data-stu-id="2fea8-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-692">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="2fea8-693">CC002</span><span class="sxs-lookup"><span data-stu-id="2fea8-693">CC002</span></span></td>
<td><span data-ttu-id="2fea8-694">Finans</span><span class="sxs-lookup"><span data-stu-id="2fea8-694">Finance</span></span></td>
<td><span data-ttu-id="2fea8-695">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-695">10001</span></span></td>
<td><span data-ttu-id="2fea8-696">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-696">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-697">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-697">Variable cost</span></span></td>
<td><span data-ttu-id="2fea8-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="2fea8-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-699">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="2fea8-700">CC003</span><span class="sxs-lookup"><span data-stu-id="2fea8-700">CC003</span></span></td>
<td><span data-ttu-id="2fea8-701">Montaj</span><span class="sxs-lookup"><span data-stu-id="2fea8-701">Assembly</span></span></td>
<td><span data-ttu-id="2fea8-702">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-702">10001</span></span></td>
<td><span data-ttu-id="2fea8-703">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-703">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-704">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-704">Fixed cost</span></span></td>
<td><span data-ttu-id="2fea8-705">713.75</span><span class="sxs-lookup"><span data-stu-id="2fea8-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-706">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="2fea8-707">CC003</span><span class="sxs-lookup"><span data-stu-id="2fea8-707">CC003</span></span></td>
<td><span data-ttu-id="2fea8-708">Montaj</span><span class="sxs-lookup"><span data-stu-id="2fea8-708">Assembly</span></span></td>
<td><span data-ttu-id="2fea8-709">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-709">10001</span></span></td>
<td><span data-ttu-id="2fea8-710">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-710">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-711">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-711">Variable cost</span></span></td>
<td><span data-ttu-id="2fea8-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="2fea8-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-713">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="2fea8-714">CC003</span><span class="sxs-lookup"><span data-stu-id="2fea8-714">CC003</span></span></td>
<td><span data-ttu-id="2fea8-715">Paketleme</span><span class="sxs-lookup"><span data-stu-id="2fea8-715">Packaging</span></span></td>
<td><span data-ttu-id="2fea8-716">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-716">10001</span></span></td>
<td><span data-ttu-id="2fea8-717">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-717">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-718">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-718">Fixed cost</span></span></td>
<td><span data-ttu-id="2fea8-719">286.25</span><span class="sxs-lookup"><span data-stu-id="2fea8-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-720">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="2fea8-721">CC003</span><span class="sxs-lookup"><span data-stu-id="2fea8-721">CC003</span></span></td>
<td><span data-ttu-id="2fea8-722">Paketleme</span><span class="sxs-lookup"><span data-stu-id="2fea8-722">Packaging</span></span></td>
<td><span data-ttu-id="2fea8-723">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-723">10001</span></span></td>
<td><span data-ttu-id="2fea8-724">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-724">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-725">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-725">Variable cost</span></span></td>
<td><span data-ttu-id="2fea8-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="2fea8-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-727">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="2fea8-728">Prod 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-728">Prod 1</span></span></td>
<td><span data-ttu-id="2fea8-729">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-729">Product 1</span></span></td>
<td><span data-ttu-id="2fea8-730">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-730">10001</span></span></td>
<td><span data-ttu-id="2fea8-731">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-731">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-732">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-732">Fixed cost</span></span></td>
<td><span data-ttu-id="2fea8-733">776.36</span><span class="sxs-lookup"><span data-stu-id="2fea8-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-734">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="2fea8-735">Prod 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-735">Prod 1</span></span></td>
<td><span data-ttu-id="2fea8-736">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-736">Product 1</span></span></td>
<td><span data-ttu-id="2fea8-737">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-737">10001</span></span></td>
<td><span data-ttu-id="2fea8-738">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-738">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-739">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-739">Variable cost</span></span></td>
<td><span data-ttu-id="2fea8-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="2fea8-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-741">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="2fea8-742">Prod 2</span><span class="sxs-lookup"><span data-stu-id="2fea8-742">Prod 2</span></span></td>
<td><span data-ttu-id="2fea8-743">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-743">Product 1</span></span></td>
<td><span data-ttu-id="2fea8-744">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-744">10001</span></span></td>
<td><span data-ttu-id="2fea8-745">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-745">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-746">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-746">Fixed cost</span></span></td>
<td><span data-ttu-id="2fea8-747">223.64</span><span class="sxs-lookup"><span data-stu-id="2fea8-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-748">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="2fea8-749">Prod 2</span><span class="sxs-lookup"><span data-stu-id="2fea8-749">Prod 2</span></span></td>
<td><span data-ttu-id="2fea8-750">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-750">Product 1</span></span></td>
<td><span data-ttu-id="2fea8-751">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-751">10001</span></span></td>
<td><span data-ttu-id="2fea8-752">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-752">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-753">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-753">Variable cost</span></span></td>
<td><span data-ttu-id="2fea8-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="2fea8-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="2fea8-755">Maliyet girişleri</span><span class="sxs-lookup"><span data-stu-id="2fea8-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="2fea8-756">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="2fea8-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="2fea8-757">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="2fea8-757">Cost element</span></span></th>
<th><span data-ttu-id="2fea8-758">Maliyet davranışı</span><span class="sxs-lookup"><span data-stu-id="2fea8-758">Cost behavior</span></span></th>
<th><span data-ttu-id="2fea8-759">Tutar</span><span class="sxs-lookup"><span data-stu-id="2fea8-759">Amount</span></span></th>
<th><span data-ttu-id="2fea8-760">Muhasebeleşme tarihi</span><span class="sxs-lookup"><span data-stu-id="2fea8-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2fea8-761">CC001</span><span class="sxs-lookup"><span data-stu-id="2fea8-761">CC001</span></span></td>
<td><span data-ttu-id="2fea8-762">İK</span><span class="sxs-lookup"><span data-stu-id="2fea8-762">HR</span></span></td>
<td><span data-ttu-id="2fea8-763">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-763">10001</span></span></td>
<td><span data-ttu-id="2fea8-764">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-764">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-765">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-765">Fixed cost</span></span></td>
<td><span data-ttu-id="2fea8-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="2fea8-766">-500.00</span></span></td>
<td><span data-ttu-id="2fea8-767">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-768">CC002</span><span class="sxs-lookup"><span data-stu-id="2fea8-768">CC002</span></span></td>
<td><span data-ttu-id="2fea8-769">Finans</span><span class="sxs-lookup"><span data-stu-id="2fea8-769">Finance</span></span></td>
<td><span data-ttu-id="2fea8-770">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-770">10001</span></span></td>
<td><span data-ttu-id="2fea8-771">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-771">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-772">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-772">Fixed cost</span></span></td>
<td><span data-ttu-id="2fea8-773">175.00</span><span class="sxs-lookup"><span data-stu-id="2fea8-773">175.00</span></span></td>
<td><span data-ttu-id="2fea8-774">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-775">CC003</span><span class="sxs-lookup"><span data-stu-id="2fea8-775">CC003</span></span></td>
<td><span data-ttu-id="2fea8-776">Montaj</span><span class="sxs-lookup"><span data-stu-id="2fea8-776">Assembly</span></span></td>
<td><span data-ttu-id="2fea8-777">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-777">10001</span></span></td>
<td><span data-ttu-id="2fea8-778">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-778">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-779">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-779">Fixed cost</span></span></td>
<td><span data-ttu-id="2fea8-780">275.00</span><span class="sxs-lookup"><span data-stu-id="2fea8-780">275.00</span></span></td>
<td><span data-ttu-id="2fea8-781">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-782">CC004</span><span class="sxs-lookup"><span data-stu-id="2fea8-782">CC004</span></span></td>
<td><span data-ttu-id="2fea8-783">Paketleme</span><span class="sxs-lookup"><span data-stu-id="2fea8-783">Packaging</span></span></td>
<td><span data-ttu-id="2fea8-784">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-784">10001</span></span></td>
<td><span data-ttu-id="2fea8-785">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-785">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-786">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-786">Fixed cost</span></span></td>
<td><span data-ttu-id="2fea8-787">50,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-787">50,00</span></span></td>
<td><span data-ttu-id="2fea8-788">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-789">CC001</span><span class="sxs-lookup"><span data-stu-id="2fea8-789">CC001</span></span></td>
<td><span data-ttu-id="2fea8-790">İK</span><span class="sxs-lookup"><span data-stu-id="2fea8-790">HR</span></span></td>
<td><span data-ttu-id="2fea8-791">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-791">10001</span></span></td>
<td><span data-ttu-id="2fea8-792">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-792">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-793">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-793">Variable cost</span></span></td>
<td><span data-ttu-id="2fea8-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="2fea8-794">-1,245.71</span></span></td>
<td><span data-ttu-id="2fea8-795">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-796">CC002</span><span class="sxs-lookup"><span data-stu-id="2fea8-796">CC002</span></span></td>
<td><span data-ttu-id="2fea8-797">Finans</span><span class="sxs-lookup"><span data-stu-id="2fea8-797">Finance</span></span></td>
<td><span data-ttu-id="2fea8-798">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-798">10001</span></span></td>
<td><span data-ttu-id="2fea8-799">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-799">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-800">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-800">Variable cost</span></span></td>
<td><span data-ttu-id="2fea8-801">436.00</span><span class="sxs-lookup"><span data-stu-id="2fea8-801">436.00</span></span></td>
<td><span data-ttu-id="2fea8-802">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-803">CC003</span><span class="sxs-lookup"><span data-stu-id="2fea8-803">CC003</span></span></td>
<td><span data-ttu-id="2fea8-804">Montaj</span><span class="sxs-lookup"><span data-stu-id="2fea8-804">Assembly</span></span></td>
<td><span data-ttu-id="2fea8-805">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-805">10001</span></span></td>
<td><span data-ttu-id="2fea8-806">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-806">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-807">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-807">Variable cost</span></span></td>
<td><span data-ttu-id="2fea8-808">685.14</span><span class="sxs-lookup"><span data-stu-id="2fea8-808">685.14</span></span></td>
<td><span data-ttu-id="2fea8-809">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-810">CC004</span><span class="sxs-lookup"><span data-stu-id="2fea8-810">CC004</span></span></td>
<td><span data-ttu-id="2fea8-811">Paketleme</span><span class="sxs-lookup"><span data-stu-id="2fea8-811">Packaging</span></span></td>
<td><span data-ttu-id="2fea8-812">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-812">10001</span></span></td>
<td><span data-ttu-id="2fea8-813">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-813">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-814">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-814">Variable cost</span></span></td>
<td><span data-ttu-id="2fea8-815">124.57</span><span class="sxs-lookup"><span data-stu-id="2fea8-815">124.57</span></span></td>
<td><span data-ttu-id="2fea8-816">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-817">CC002</span><span class="sxs-lookup"><span data-stu-id="2fea8-817">CC002</span></span></td>
<td><span data-ttu-id="2fea8-818">Finans</span><span class="sxs-lookup"><span data-stu-id="2fea8-818">Finance</span></span></td>
<td><span data-ttu-id="2fea8-819">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-819">10001</span></span></td>
<td><span data-ttu-id="2fea8-820">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-820">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-821">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-821">Fixed cost</span></span></td>
<td><span data-ttu-id="2fea8-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-822">-675.00</span></span></td>
<td><span data-ttu-id="2fea8-823">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-824">CC003</span><span class="sxs-lookup"><span data-stu-id="2fea8-824">CC003</span></span></td>
<td><span data-ttu-id="2fea8-825">Montaj</span><span class="sxs-lookup"><span data-stu-id="2fea8-825">Assembly</span></span></td>
<td><span data-ttu-id="2fea8-826">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-826">10001</span></span></td>
<td><span data-ttu-id="2fea8-827">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-827">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-828">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-828">Fixed cost</span></span></td>
<td><span data-ttu-id="2fea8-829">438.75</span><span class="sxs-lookup"><span data-stu-id="2fea8-829">438.75</span></span></td>
<td><span data-ttu-id="2fea8-830">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-831">CC004</span><span class="sxs-lookup"><span data-stu-id="2fea8-831">CC004</span></span></td>
<td><span data-ttu-id="2fea8-832">Paketleme</span><span class="sxs-lookup"><span data-stu-id="2fea8-832">Packaging</span></span></td>
<td><span data-ttu-id="2fea8-833">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-833">10001</span></span></td>
<td><span data-ttu-id="2fea8-834">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-834">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-835">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-835">Fixed cost</span></span></td>
<td><span data-ttu-id="2fea8-836">236.25</span><span class="sxs-lookup"><span data-stu-id="2fea8-836">236.25</span></span></td>
<td><span data-ttu-id="2fea8-837">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-838">CC002</span><span class="sxs-lookup"><span data-stu-id="2fea8-838">CC002</span></span></td>
<td><span data-ttu-id="2fea8-839">Finans</span><span class="sxs-lookup"><span data-stu-id="2fea8-839">Finance</span></span></td>
<td><span data-ttu-id="2fea8-840">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-840">10001</span></span></td>
<td><span data-ttu-id="2fea8-841">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-841">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-842">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-842">Variable cost</span></span></td>
<td><span data-ttu-id="2fea8-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="2fea8-843">-8,150.29</span></span></td>
<td><span data-ttu-id="2fea8-844">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-845">CC003</span><span class="sxs-lookup"><span data-stu-id="2fea8-845">CC003</span></span></td>
<td><span data-ttu-id="2fea8-846">Montaj</span><span class="sxs-lookup"><span data-stu-id="2fea8-846">Assembly</span></span></td>
<td><span data-ttu-id="2fea8-847">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-847">10001</span></span></td>
<td><span data-ttu-id="2fea8-848">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-848">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-849">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-849">Variable cost</span></span></td>
<td><span data-ttu-id="2fea8-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="2fea8-850">5,297.69</span></span></td>
<td><span data-ttu-id="2fea8-851">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-852">CC004</span><span class="sxs-lookup"><span data-stu-id="2fea8-852">CC004</span></span></td>
<td><span data-ttu-id="2fea8-853">Paketleme</span><span class="sxs-lookup"><span data-stu-id="2fea8-853">Packaging</span></span></td>
<td><span data-ttu-id="2fea8-854">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-854">10001</span></span></td>
<td><span data-ttu-id="2fea8-855">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-855">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-856">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-856">Variable cost</span></span></td>
<td><span data-ttu-id="2fea8-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="2fea8-857">2,852.60</span></span></td>
<td><span data-ttu-id="2fea8-858">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-859">CC003</span><span class="sxs-lookup"><span data-stu-id="2fea8-859">CC003</span></span></td>
<td><span data-ttu-id="2fea8-860">Montaj</span><span class="sxs-lookup"><span data-stu-id="2fea8-860">Assembly</span></span></td>
<td><span data-ttu-id="2fea8-861">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-861">10001</span></span></td>
<td><span data-ttu-id="2fea8-862">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-862">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-863">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-863">Fixed cost</span></span></td>
<td><span data-ttu-id="2fea8-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="2fea8-864">-713.75</span></span></td>
<td><span data-ttu-id="2fea8-865">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-866">Prod 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-866">Prod 1</span></span></td>
<td><span data-ttu-id="2fea8-867">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-867">Product 1</span></span></td>
<td><span data-ttu-id="2fea8-868">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-868">10001</span></span></td>
<td><span data-ttu-id="2fea8-869">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-869">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-870">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-870">Fixed cost</span></span></td>
<td><span data-ttu-id="2fea8-871">535.31</span><span class="sxs-lookup"><span data-stu-id="2fea8-871">535.31</span></span></td>
<td><span data-ttu-id="2fea8-872">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-873">Prod 2</span><span class="sxs-lookup"><span data-stu-id="2fea8-873">Prod 2</span></span></td>
<td><span data-ttu-id="2fea8-874">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="2fea8-874">Product 2</span></span></td>
<td><span data-ttu-id="2fea8-875">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-875">10001</span></span></td>
<td><span data-ttu-id="2fea8-876">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-876">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-877">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-877">Fixed cost</span></span></td>
<td><span data-ttu-id="2fea8-878">178.44</span><span class="sxs-lookup"><span data-stu-id="2fea8-878">178.44</span></span></td>
<td><span data-ttu-id="2fea8-879">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-880">CC003</span><span class="sxs-lookup"><span data-stu-id="2fea8-880">CC003</span></span></td>
<td><span data-ttu-id="2fea8-881">Montaj</span><span class="sxs-lookup"><span data-stu-id="2fea8-881">Assembly</span></span></td>
<td><span data-ttu-id="2fea8-882">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-882">10001</span></span></td>
<td><span data-ttu-id="2fea8-883">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-883">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-884">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-884">Variable cost</span></span></td>
<td><span data-ttu-id="2fea8-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="2fea8-885">-5,982.83</span></span></td>
<td><span data-ttu-id="2fea8-886">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-887">Prod 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-887">Prod 1</span></span></td>
<td><span data-ttu-id="2fea8-888">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-888">Product 1</span></span></td>
<td><span data-ttu-id="2fea8-889">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-889">10001</span></span></td>
<td><span data-ttu-id="2fea8-890">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-890">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-891">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-891">Variable cost</span></span></td>
<td><span data-ttu-id="2fea8-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="2fea8-892">4,487.12</span></span></td>
<td><span data-ttu-id="2fea8-893">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-894">Prod 2</span><span class="sxs-lookup"><span data-stu-id="2fea8-894">Prod 2</span></span></td>
<td><span data-ttu-id="2fea8-895">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="2fea8-895">Product 2</span></span></td>
<td><span data-ttu-id="2fea8-896">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-896">10001</span></span></td>
<td><span data-ttu-id="2fea8-897">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-897">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-898">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-898">Variable cost</span></span></td>
<td><span data-ttu-id="2fea8-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="2fea8-899">1,495.71</span></span></td>
<td><span data-ttu-id="2fea8-900">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-901">CC003</span><span class="sxs-lookup"><span data-stu-id="2fea8-901">CC003</span></span></td>
<td><span data-ttu-id="2fea8-902">Montaj</span><span class="sxs-lookup"><span data-stu-id="2fea8-902">Assembly</span></span></td>
<td><span data-ttu-id="2fea8-903">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-903">10001</span></span></td>
<td><span data-ttu-id="2fea8-904">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-904">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-905">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-905">Fixed cost</span></span></td>
<td><span data-ttu-id="2fea8-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="2fea8-906">-286.25</span></span></td>
<td><span data-ttu-id="2fea8-907">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-908">Prod 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-908">Prod 1</span></span></td>
<td><span data-ttu-id="2fea8-909">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-909">Product 1</span></span></td>
<td><span data-ttu-id="2fea8-910">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-910">10001</span></span></td>
<td><span data-ttu-id="2fea8-911">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-911">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-912">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-912">Fixed cost</span></span></td>
<td><span data-ttu-id="2fea8-913">241.05</span><span class="sxs-lookup"><span data-stu-id="2fea8-913">241.05</span></span></td>
<td><span data-ttu-id="2fea8-914">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-915">Prod 2</span><span class="sxs-lookup"><span data-stu-id="2fea8-915">Prod 2</span></span></td>
<td><span data-ttu-id="2fea8-916">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="2fea8-916">Product 2</span></span></td>
<td><span data-ttu-id="2fea8-917">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-917">10001</span></span></td>
<td><span data-ttu-id="2fea8-918">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-918">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-919">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-919">Fixed cost</span></span></td>
<td><span data-ttu-id="2fea8-920">45.20</span><span class="sxs-lookup"><span data-stu-id="2fea8-920">45.20</span></span></td>
<td><span data-ttu-id="2fea8-921">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-922">CC003</span><span class="sxs-lookup"><span data-stu-id="2fea8-922">CC003</span></span></td>
<td><span data-ttu-id="2fea8-923">Montaj</span><span class="sxs-lookup"><span data-stu-id="2fea8-923">Assembly</span></span></td>
<td><span data-ttu-id="2fea8-924">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-924">10001</span></span></td>
<td><span data-ttu-id="2fea8-925">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-925">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-926">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-926">Variable cost</span></span></td>
<td><span data-ttu-id="2fea8-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="2fea8-927">-2,977.17</span></span></td>
<td><span data-ttu-id="2fea8-928">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-929">Prod 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-929">Prod 1</span></span></td>
<td><span data-ttu-id="2fea8-930">Ürün 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-930">Product 1</span></span></td>
<td><span data-ttu-id="2fea8-931">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-931">10001</span></span></td>
<td><span data-ttu-id="2fea8-932">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-932">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-933">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-933">Variable cost</span></span></td>
<td><span data-ttu-id="2fea8-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="2fea8-934">2,507.09</span></span></td>
<td><span data-ttu-id="2fea8-935">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2fea8-936">Prod 2</span><span class="sxs-lookup"><span data-stu-id="2fea8-936">Prod 2</span></span></td>
<td><span data-ttu-id="2fea8-937">Ürün 2</span><span class="sxs-lookup"><span data-stu-id="2fea8-937">Product 2</span></span></td>
<td><span data-ttu-id="2fea8-938">10001</span><span class="sxs-lookup"><span data-stu-id="2fea8-938">10001</span></span></td>
<td><span data-ttu-id="2fea8-939">Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-939">Electricity</span></span></td>
<td><span data-ttu-id="2fea8-940">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-940">Variable cost</span></span></td>
<td><span data-ttu-id="2fea8-941">470.08</span><span class="sxs-lookup"><span data-stu-id="2fea8-941">470.08</span></span></td>
<td><span data-ttu-id="2fea8-942">31 Ocak 2017</span><span class="sxs-lookup"><span data-stu-id="2fea8-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="2fea8-943">Sonuç</span><span class="sxs-lookup"><span data-stu-id="2fea8-943">Conclusion</span></span>
<span data-ttu-id="2fea8-944">Mali muhasebede, Elektrik için 10.000,00 maliyet bir sözde maliyet merkezi kimliğine nakledilmiştir.</span><span class="sxs-lookup"><span data-stu-id="2fea8-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="2fea8-945">Bu nedenle, maliyet muhasebecileri bu maliyetin tahsis edilmesi gerektiğini bilirler.</span><span class="sxs-lookup"><span data-stu-id="2fea8-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="2fea8-946">Maliyet muhasebesinde, maliyetler kuruluş birimleri ve seviyeleri arasında, uygulanan kural ve ilkelere dayalı olarak akar.</span><span class="sxs-lookup"><span data-stu-id="2fea8-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="2fea8-947">Her maliyet, maliyetlerin tahsisatı için en iyi değerlendirmeyi sağlayan bir tahsisat tabanı ile ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="2fea8-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="2fea8-948">Maliyet öğesi</span><span class="sxs-lookup"><span data-stu-id="2fea8-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="2fea8-949">Maliyet nesnesi</span><span class="sxs-lookup"><span data-stu-id="2fea8-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="2fea8-950">Toplam</span><span class="sxs-lookup"><span data-stu-id="2fea8-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="2fea8-951">CC099</span><span class="sxs-lookup"><span data-stu-id="2fea8-951">CC099</span></span></th>
<th><span data-ttu-id="2fea8-952">CC001</span><span class="sxs-lookup"><span data-stu-id="2fea8-952">CC001</span></span></th>
<th><span data-ttu-id="2fea8-953">CC002</span><span class="sxs-lookup"><span data-stu-id="2fea8-953">CC002</span></span></th>
<th><span data-ttu-id="2fea8-954">CC003</span><span class="sxs-lookup"><span data-stu-id="2fea8-954">CC003</span></span></th>
<th><span data-ttu-id="2fea8-955">CC004</span><span class="sxs-lookup"><span data-stu-id="2fea8-955">CC004</span></span></th>
<th><span data-ttu-id="2fea8-956">Proj 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-956">Proj 1</span></span></th>
<th><span data-ttu-id="2fea8-957">Proj 2</span><span class="sxs-lookup"><span data-stu-id="2fea8-957">Proj 2</span></span></th>
<th><span data-ttu-id="2fea8-958">Prod 1</span><span class="sxs-lookup"><span data-stu-id="2fea8-958">Prod 1</span></span></th>
<th><span data-ttu-id="2fea8-959">Prod 2</span><span class="sxs-lookup"><span data-stu-id="2fea8-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="2fea8-960">10001 Elektrik</span><span class="sxs-lookup"><span data-stu-id="2fea8-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2fea8-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="2fea8-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="2fea8-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="2fea8-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="2fea8-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="2fea8-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="2fea8-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="2fea8-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="2fea8-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="2fea8-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="2fea8-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="2fea8-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="2fea8-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="2fea8-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="2fea8-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="2fea8-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="2fea8-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="2fea8-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="2fea8-970">Sınıflandırılmamış</span><span class="sxs-lookup"><span data-stu-id="2fea8-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2fea8-971">0,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="2fea8-972">Sabit maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2fea8-973">0,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2fea8-974">0,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2fea8-975">0,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2fea8-976">0,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2fea8-977">0,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="2fea8-978">776.36</span><span class="sxs-lookup"><span data-stu-id="2fea8-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2fea8-979">223.64</span><span class="sxs-lookup"><span data-stu-id="2fea8-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2fea8-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="2fea8-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="2fea8-981">Değişken maliyet</span><span class="sxs-lookup"><span data-stu-id="2fea8-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2fea8-982">000</span><span class="sxs-lookup"><span data-stu-id="2fea8-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2fea8-983">0,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2fea8-984">0,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2fea8-985">0,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2fea8-986">0,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2fea8-987">30.00</span><span class="sxs-lookup"><span data-stu-id="2fea8-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2fea8-988">10,00</span><span class="sxs-lookup"><span data-stu-id="2fea8-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2fea8-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="2fea8-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2fea8-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="2fea8-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="2fea8-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="2fea8-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="2fea8-992">Bu konu, birincil maliyet öğesi, 10001 Elektrik'in maliyet nesneleri arasında nasıl aktığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2fea8-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="2fea8-993">Bu nedenle, bu genel gider maliyeti kuruluşun en düşük seviyesine tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="2fea8-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="2fea8-994">Başka bir deyişle, maliyet en alt düzeydeki maliyet nesnelerine aittir.</span><span class="sxs-lookup"><span data-stu-id="2fea8-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="2fea8-995">Maliyetin, maliyet nesneleri arasında görsel bir akışına ihtiyacınız varsa, maliyetin akışını görselleştirmek için maliyet toplamı ilke kurallarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2fea8-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="2fea8-996">Daha fazla bilgi için [Maliyet yukarı yuvarlama](cost-rollup.md) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="2fea8-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



