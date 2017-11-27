---
title: "Kalite yönetimine genel bakış"
description: "Bu konuda, tedarik zincirinizde ürün kalitesini artırmak için Microsoft Dynamics 365 for Finance and Operations'daki kalite yönetimini nasıl kullanabileceğiniz açıklanmaktadır."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c8961d1c62167192fcf32d17c2941b8813ea0629
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="quality-management-overview"></a><span data-ttu-id="1da7c-103">Kalite yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="1da7c-103">Quality management overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1da7c-104">Bu konuda, tedarik zincirinizde ürün kalitesini artırmak için Microsoft Dynamics 365 for Finance and Operations'daki kalite yönetimini nasıl kullanabileceğiniz açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="1da7c-104">This topic describes how you can use quality management in Microsoft Dynamics 365 for Finance and Operations to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="1da7c-105">Kalite Yönetimi, uyumsuz ürünler,, kendi başlangıç noktalarını dikkate almadan işleyecek döngü sürelerini yönetmenize yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="1da7c-106">Tanı türleri düzeltme raporlaması ile bağlantılı olduğundan, Microsoft Dynamics 365 for Finance and Operations sorunları düzeltmek ve oluşmalarını önlemek için görevleri zamanlayabilir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-106">Because diagnostic types are linked to correction reporting, Microsoft Dynamics 365 for Finance and Operations can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="1da7c-107">Uygunsuzluğu yönetmek için daha fazla işlevselliğe ek olarak, Kalite Yönetimi sorun türüne göre sorunları (hatta iç sorunları) izlemek için ve çözümleri kısa vadeli veya uzun vadeli olarak tanımlamak için işlev içerir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="1da7c-108">Anahtar performans göstergeleri (APG) ile ilgili istatistikler, önceki uygunsuzluk sorunlarının geçmişi ve bunları düzeltmek için kullanılan çözümler hakkında bir anlayış sağlar.</span><span class="sxs-lookup"><span data-stu-id="1da7c-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="1da7c-109">Önceki kalite ölçülerinin geçmişteki etkilerini incelemek ve ileride kullanılmaya uygun önlemleri belirlemek için geçmişe dönük verileri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1da7c-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="1da7c-110">Bir kalite ilişkisi ayarladığınızda, Finance and Operations çeşitli iş süreçleri, olaylar ve koşullar için kalite emirleri oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-110">When you set up a quality association, Finance and Operations can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="1da7c-111">Kalite ilişkisi, belirli bir madde, belirli bir madde grubu veya tüm öğeleri kapsayabilir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="1da7c-112">Kalite yönetimi kullanımına örnekler</span><span class="sxs-lookup"><span data-stu-id="1da7c-112">Examples of the use of quality management</span></span>
<span data-ttu-id="1da7c-113">Kalite Yönetimi esnektir ve tedarik zinciri işlemlerinin belirli düzeylerdeki gereksinimlerini karşılamak için çeşitli şekillerde uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="1da7c-114">Aşağıdaki örneklerde, bu özelliklerin olası kullanımı gösterilmektedir:</span><span class="sxs-lookup"><span data-stu-id="1da7c-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="1da7c-115">Önceden tanımlanmış ölçütlere (belirli bir satıcı satınalma siparişinden, ambar kaydı) dayalı bir kalite kontrol işlemini otomatik olarak başlatın.</span><span class="sxs-lookup"><span data-stu-id="1da7c-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="1da7c-116">Onaylanmamış stokun kullanılmasını engellemek için inceleme sırasında stoku bloklayın(Tüm satınalma siparişi miktarlarını engelleme).</span><span class="sxs-lookup"><span data-stu-id="1da7c-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="1da7c-117">Madde örneklemeyi kalite ilişkilendirmesinin bir parçası olarak, denetlenmesi gereken geçerli fiziksel stok miktarını tanımlamak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="1da7c-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="1da7c-118">Örnekleme miktar veya yüzde tabanlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-118">Sampling can be based on fixed quantities or a percentage.</span></span>
-   <span data-ttu-id="1da7c-119">Kısmi alış irsaliyeleri için kalite emirleri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1da7c-119">Create quality orders for partial receipts.</span></span> <span data-ttu-id="1da7c-120">Bir siparişten fiziksel olarak alına miktara bağlı olarak oluşturulan bir kalite emri oluşturmak için **Madde örnekleme** formundaki **Güncelleştirilen miktar başına** onay kutusunu seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="1da7c-120">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="1da7c-121">Minimum, maksimum ve hedef test değerleri içeren test türleri oluşturun ve doğrulama sonuçları önceden tanımlanmış olan niteliğe karşı nicelik sınamaları gerçekleştirin.</span><span class="sxs-lookup"><span data-stu-id="1da7c-121">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="1da7c-122">Kalite Ölçüm toleranslarını kontrol etmek için bir kabul edilebilir kalite düzeyi (AQL) belirtin.</span><span class="sxs-lookup"><span data-stu-id="1da7c-122">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="1da7c-123">Denetleme işlemi için gereken test alanı ve test aletleri gibi kaynakları belirtin.</span><span class="sxs-lookup"><span data-stu-id="1da7c-123">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="1da7c-124">Kalite ilişkileri ile çalışmak</span><span class="sxs-lookup"><span data-stu-id="1da7c-124">Working with quality associations</span></span>
<span data-ttu-id="1da7c-125">Kalite ilişkisini kullanan iş süreci, satınalma siparişleri, satış siparişleri veya üretim emirleri gibi çeşitli kaynak belgelere ilişkili olabilir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-125">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="1da7c-126">Her kalite bağlantısı kaydı oluşturulan kalite emirlerine geçerli olacak testler kümesini, AQL'yi ve örnek alma planını da tanımlamaktadır.</span><span class="sxs-lookup"><span data-stu-id="1da7c-126">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="1da7c-127">Bir iş sürecindeki her değişim için bir kalite ilişkisi kaydı tanımlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-127">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="1da7c-128">Örneğin, bir satınalma siparişi ürün alış irsaliyesi güncelleştirildiğinde, kalite emri oluşturacak bir kalite ilişkisi ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1da7c-128">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="1da7c-129">Yürütme planı kurulumuna bağlı olarak, açık bir kalite emri yok ya da satınalma siparişi faturalama gibi sonraki işlemler, engellenen tetikleyici işlem engellenebilir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-129">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="1da7c-130">**Not:** Açık kalite emirleri olduğunda, stok miktarlarının çıkarılması otomatik olarak engellenir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-130">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="1da7c-131">**Madde örnekleri** sayfasında bulunan **Tam engelleme** ayarına bağlı olarak, miktar kalite emrindeki miktardır ya da kaynak belge satırındaki miktardır.</span><span class="sxs-lookup"><span data-stu-id="1da7c-131">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="1da7c-132">Bir iş süreci için, kalite ilişkisi kaydı, kalite emrinin oluşturulduğu olay ve koşulları tanımlar.</span><span class="sxs-lookup"><span data-stu-id="1da7c-132">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="1da7c-133">Koşullar bir siteye veya bir tüzel kişiliğe özel olabilir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-133">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="1da7c-134">Bozucu testler içeren bir kalite emri yalnızca olay için eldeki stok bulunması durumunda oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-134">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="1da7c-135">Aşağıdaki örnekler, her iş sürecindeki değişiklikler için bir kalite bağlantısını tanımlamayı açıklar.</span><span class="sxs-lookup"><span data-stu-id="1da7c-135">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="1da7c-136">Her örnek için, aşağıdaki tablo kalite ilişki kaydındaki olayları ve durumları özetler.</span><span class="sxs-lookup"><span data-stu-id="1da7c-136">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="1da7c-137">Referans türü</span><span class="sxs-lookup"><span data-stu-id="1da7c-137">Reference type</span></span></th>
<th><span data-ttu-id="1da7c-138">Olay türü</span><span class="sxs-lookup"><span data-stu-id="1da7c-138">Event type</span></span></th>
<th><span data-ttu-id="1da7c-139">Yürütme</span><span class="sxs-lookup"><span data-stu-id="1da7c-139">Execution</span></span></th>
<th><span data-ttu-id="1da7c-140">Olay durdurma</span><span class="sxs-lookup"><span data-stu-id="1da7c-140">Event blocking</span></span></th>
<th><span data-ttu-id="1da7c-141">Belge başvurusu</span><span class="sxs-lookup"><span data-stu-id="1da7c-141">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="1da7c-142">Stok</span><span class="sxs-lookup"><span data-stu-id="1da7c-142">Inventory</span></span></td>
<td><span data-ttu-id="1da7c-143">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="1da7c-143">Not applicable</span></span></td>
<td><span data-ttu-id="1da7c-144">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="1da7c-144">Not applicable</span></span></td>
<td><span data-ttu-id="1da7c-145">Yok</span><span class="sxs-lookup"><span data-stu-id="1da7c-145">None</span></span></td>
<td><span data-ttu-id="1da7c-146">Tümü</span><span class="sxs-lookup"><span data-stu-id="1da7c-146">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="1da7c-147">Satışlar</span><span class="sxs-lookup"><span data-stu-id="1da7c-147">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="1da7c-148">Malzeme çekme işlemi planlandı</span><span class="sxs-lookup"><span data-stu-id="1da7c-148">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="1da7c-149">Önce</span><span class="sxs-lookup"><span data-stu-id="1da7c-149">Before</span></span></td>
<td><span data-ttu-id="1da7c-150">Yok</span><span class="sxs-lookup"><span data-stu-id="1da7c-150">None</span></span></td>
<td rowspan="22"><span data-ttu-id="1da7c-151">Belirli Kimlik, Grup veya Yalnızca tümü</span><span class="sxs-lookup"><span data-stu-id="1da7c-151">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1da7c-152">Malzeme çekme işlemi</span><span class="sxs-lookup"><span data-stu-id="1da7c-152">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1da7c-153">Sevk irsaliyesi</span><span class="sxs-lookup"><span data-stu-id="1da7c-153">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1da7c-154">Fatura</span><span class="sxs-lookup"><span data-stu-id="1da7c-154">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1da7c-155">Sevk irsaliyesi</span><span class="sxs-lookup"><span data-stu-id="1da7c-155">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="1da7c-156">Önce</span><span class="sxs-lookup"><span data-stu-id="1da7c-156">Before</span></span></td>
<td><span data-ttu-id="1da7c-157">Yok</span><span class="sxs-lookup"><span data-stu-id="1da7c-157">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1da7c-158">Sevk irsaliyesi</span><span class="sxs-lookup"><span data-stu-id="1da7c-158">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1da7c-159">Fatura</span><span class="sxs-lookup"><span data-stu-id="1da7c-159">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="1da7c-160">Satınalma</span><span class="sxs-lookup"><span data-stu-id="1da7c-160">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="1da7c-161">Giriş listesi</span><span class="sxs-lookup"><span data-stu-id="1da7c-161">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="1da7c-162">Önce</span><span class="sxs-lookup"><span data-stu-id="1da7c-162">Before</span></span></td>
<td><span data-ttu-id="1da7c-163">Yok</span><span class="sxs-lookup"><span data-stu-id="1da7c-163">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1da7c-164">Giriş listesi</span><span class="sxs-lookup"><span data-stu-id="1da7c-164">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1da7c-165">Ürün girişi</span><span class="sxs-lookup"><span data-stu-id="1da7c-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1da7c-166">Fatura</span><span class="sxs-lookup"><span data-stu-id="1da7c-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1da7c-167">Sonra</span><span class="sxs-lookup"><span data-stu-id="1da7c-167">After</span></span></td>
<td><span data-ttu-id="1da7c-168">Yok</span><span class="sxs-lookup"><span data-stu-id="1da7c-168">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1da7c-169">Ürün girişi</span><span class="sxs-lookup"><span data-stu-id="1da7c-169">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1da7c-170">Fatura</span><span class="sxs-lookup"><span data-stu-id="1da7c-170">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1da7c-171">Kayıt</span><span class="sxs-lookup"><span data-stu-id="1da7c-171">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="1da7c-172">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="1da7c-172">Not applicable</span></span></td>
<td><span data-ttu-id="1da7c-173">Yok</span><span class="sxs-lookup"><span data-stu-id="1da7c-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1da7c-174">Ürün girişi</span><span class="sxs-lookup"><span data-stu-id="1da7c-174">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1da7c-175">Fatura</span><span class="sxs-lookup"><span data-stu-id="1da7c-175">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="1da7c-176">Ürün girişi</span><span class="sxs-lookup"><span data-stu-id="1da7c-176">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="1da7c-177">Önce</span><span class="sxs-lookup"><span data-stu-id="1da7c-177">Before</span></span></td>
<td><span data-ttu-id="1da7c-178">Yok</span><span class="sxs-lookup"><span data-stu-id="1da7c-178">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1da7c-179">Ürün girişi</span><span class="sxs-lookup"><span data-stu-id="1da7c-179">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1da7c-180">Fatura</span><span class="sxs-lookup"><span data-stu-id="1da7c-180">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1da7c-181">Sonra</span><span class="sxs-lookup"><span data-stu-id="1da7c-181">After</span></span></td>
<td><span data-ttu-id="1da7c-182">Yok</span><span class="sxs-lookup"><span data-stu-id="1da7c-182">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1da7c-183">Fatura</span><span class="sxs-lookup"><span data-stu-id="1da7c-183">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="1da7c-184">Üretim</span><span class="sxs-lookup"><span data-stu-id="1da7c-184">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="1da7c-185">Kayıt</span><span class="sxs-lookup"><span data-stu-id="1da7c-185">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="1da7c-186">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="1da7c-186">Not applicable</span></span></td>
<td><span data-ttu-id="1da7c-187">Yok</span><span class="sxs-lookup"><span data-stu-id="1da7c-187">None</span></span></td>
<td rowspan="12"><span data-ttu-id="1da7c-188">Tümü</span><span class="sxs-lookup"><span data-stu-id="1da7c-188">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1da7c-189">Tamamlandı bildirimi</span><span class="sxs-lookup"><span data-stu-id="1da7c-189">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1da7c-190">Bitir</span><span class="sxs-lookup"><span data-stu-id="1da7c-190">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="1da7c-191">Tamamlandı bildirimi</span><span class="sxs-lookup"><span data-stu-id="1da7c-191">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="1da7c-192">Önce</span><span class="sxs-lookup"><span data-stu-id="1da7c-192">Before</span></span></td>
<td><span data-ttu-id="1da7c-193">Yok</span><span class="sxs-lookup"><span data-stu-id="1da7c-193">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1da7c-194">Tamamlandı bildirimi</span><span class="sxs-lookup"><span data-stu-id="1da7c-194">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1da7c-195">Bitir</span><span class="sxs-lookup"><span data-stu-id="1da7c-195">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1da7c-196">Sonra</span><span class="sxs-lookup"><span data-stu-id="1da7c-196">After</span></span></td>
<td><span data-ttu-id="1da7c-197">Yok</span><span class="sxs-lookup"><span data-stu-id="1da7c-197">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1da7c-198">Bitir</span><span class="sxs-lookup"><span data-stu-id="1da7c-198">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="1da7c-199">Karantina</span><span class="sxs-lookup"><span data-stu-id="1da7c-199">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="1da7c-200">Tamamlandı bildirimi</span><span class="sxs-lookup"><span data-stu-id="1da7c-200">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="1da7c-201">Önce</span><span class="sxs-lookup"><span data-stu-id="1da7c-201">Before</span></span></td>
<td><span data-ttu-id="1da7c-202">Tamamlandı bildirimi</span><span class="sxs-lookup"><span data-stu-id="1da7c-202">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1da7c-203">Bitir</span><span class="sxs-lookup"><span data-stu-id="1da7c-203">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1da7c-204">Sonra</span><span class="sxs-lookup"><span data-stu-id="1da7c-204">After</span></span></td>
<td><span data-ttu-id="1da7c-205">Bitir</span><span class="sxs-lookup"><span data-stu-id="1da7c-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1da7c-206">Bitir</span><span class="sxs-lookup"><span data-stu-id="1da7c-206">End</span></span></td>
<td><span data-ttu-id="1da7c-207">Önce</span><span class="sxs-lookup"><span data-stu-id="1da7c-207">Before</span></span></td>
<td><span data-ttu-id="1da7c-208">Bitir</span><span class="sxs-lookup"><span data-stu-id="1da7c-208">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1da7c-209">Rota operasyonu</span><span class="sxs-lookup"><span data-stu-id="1da7c-209">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="1da7c-210">Tamamlandı bildirimi</span><span class="sxs-lookup"><span data-stu-id="1da7c-210">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="1da7c-211">Önce</span><span class="sxs-lookup"><span data-stu-id="1da7c-211">Before</span></span></td>
<td><span data-ttu-id="1da7c-212">Yok</span><span class="sxs-lookup"><span data-stu-id="1da7c-212">None</span></span></td>
<td rowspan="3"><span data-ttu-id="1da7c-213">Belirli Kimlik, Grup veya Tümü ve Kaynağa özel, Grup veya Tümü</span><span class="sxs-lookup"><span data-stu-id="1da7c-213">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1da7c-214">Tamamlandı bildirimi</span><span class="sxs-lookup"><span data-stu-id="1da7c-214">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1da7c-215">Sonra</span><span class="sxs-lookup"><span data-stu-id="1da7c-215">After</span></span></td>
<td><span data-ttu-id="1da7c-216">Yok</span><span class="sxs-lookup"><span data-stu-id="1da7c-216">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1da7c-217">Ortak ürün üretimi</span><span class="sxs-lookup"><span data-stu-id="1da7c-217">Co-product production</span></span></td>
<td><span data-ttu-id="1da7c-218">Kayıt</span><span class="sxs-lookup"><span data-stu-id="1da7c-218">Registration</span></span></td>
<td><span data-ttu-id="1da7c-219">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="1da7c-219">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1da7c-220">Yok</span><span class="sxs-lookup"><span data-stu-id="1da7c-220">None</span></span></td>
<td rowspan="3"><span data-ttu-id="1da7c-221">Tümü</span><span class="sxs-lookup"><span data-stu-id="1da7c-221">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1da7c-222">Tamamlandı bildirimi</span><span class="sxs-lookup"><span data-stu-id="1da7c-222">Report as finished</span></span></td>
<td><span data-ttu-id="1da7c-223">Önce</span><span class="sxs-lookup"><span data-stu-id="1da7c-223">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1da7c-224">Sonra</span><span class="sxs-lookup"><span data-stu-id="1da7c-224">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1da7c-225">Aşağıdaki tabloda belirli türde işlemler için kalite emirlerinin nasıl oluşturulabileceği hakkında daha fazla bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="1da7c-225">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="1da7c-226">İşleme türü</span><span class="sxs-lookup"><span data-stu-id="1da7c-226">Type of process</span></span></th>
<th><span data-ttu-id="1da7c-227">Kalite emirlerinin ne zaman otomatik olarak oluşturulabileceği</span><span class="sxs-lookup"><span data-stu-id="1da7c-227">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="1da7c-228">Bozucu sınama yapılması gerekirse kalite emirlerinin ne zaman oluşturulabileceği</span><span class="sxs-lookup"><span data-stu-id="1da7c-228">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="1da7c-229">Koşul bilgisi</span><span class="sxs-lookup"><span data-stu-id="1da7c-229">Condition information</span></span></th>
<th><span data-ttu-id="1da7c-230">El ile oluşturma bilgisi</span><span class="sxs-lookup"><span data-stu-id="1da7c-230">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="1da7c-231">Satın alma siparişi</span><span class="sxs-lookup"><span data-stu-id="1da7c-231">Purchase order</span></span></td>
<td><span data-ttu-id="1da7c-232">Alınan malzeme için ürün girişi ya da giriş listesi nakledildikten önce veya sonra.</span><span class="sxs-lookup"><span data-stu-id="1da7c-232">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="1da7c-233">Alınan malzeme için ürün girişi nakledildikten sonra, çünkü malzemenin bozucu test için mevcut olması gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-233">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="1da7c-234">Kalite emri gereksinimi özel bir tesisi, maddeyi veya satıcıyı ya da bunların bir birleşimini yansıtabilir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-234">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="1da7c-235">Bir satınalma siparişine gönderme yapan ve el ile oluşturulmuş bir kalite emri, tasarlanmış örnek alma planı gibi, bir kalite bağlantısı kaydında bulunan bilgileri kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-235">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1da7c-236">Karantina emri</span><span class="sxs-lookup"><span data-stu-id="1da7c-236">Quarantine order</span></span></td>
<td><span data-ttu-id="1da7c-237">Karantina siparişi tamamlandı veya sona erdi olarak bildirildikten önce veya sonra.</span><span class="sxs-lookup"><span data-stu-id="1da7c-237">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="1da7c-238">Yıkıcı testler gerektiren kalite emirleri oluşturulamaz.</span><span class="sxs-lookup"><span data-stu-id="1da7c-238">Quality orders that require destructive tests can't be generated.</span></span> <span data-ttu-id="1da7c-239">Karantina siparişi işlevinin, yok edilen malzemenin değerlendirmesini üstleneceği kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-239">It's assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="1da7c-240">Kalite emri gereksinimi özel bir tesisi, maddeyi veya satıcıyı ya da bunların bir birleşimini yansıtabilir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-240">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="1da7c-241">Bir karantina siparişine gönderme yapan ve el ile oluşturulmuş bir kalite emri, tasarlanmış örnek alma planı gibi, bir kalite bağlantısı kaydında bulunan bilgileri kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-241">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1da7c-242">Satış siparişi</span><span class="sxs-lookup"><span data-stu-id="1da7c-242">Sales order</span></span></td>
<td><span data-ttu-id="1da7c-243">Bir zamanlanmış malzeme çekme işlem veya sevk irsaliyesi güncelleştirmesi sevk maddeler için önce</span><span class="sxs-lookup"><span data-stu-id="1da7c-243">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="1da7c-244">Herhangi bir adımda</span><span class="sxs-lookup"><span data-stu-id="1da7c-244">At any step</span></span></td>
<td><span data-ttu-id="1da7c-245">Kalite emri gereksinimi özel bir tesisi, maddeyi veya satıcıyı ya da bunların bir birleşimini yansıtabilir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-245">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="1da7c-246">Bir satış siparişine gönderme yapan ve el ile oluşturulmuş bir kalite emri, tasarlanmış örnek alma planı gibi, bir kalite bağlantısı kaydında bulunan bilgileri kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-246">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1da7c-247">Üretim emri</span><span class="sxs-lookup"><span data-stu-id="1da7c-247">Production order</span></span></td>
<td><span data-ttu-id="1da7c-248">Üretim emri için bitmiş miktar rapor edildikten önce veya sonra</span><span class="sxs-lookup"><span data-stu-id="1da7c-248">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="1da7c-249">Üretim emri için bitmiş miktar rapor edildikten sonra</span><span class="sxs-lookup"><span data-stu-id="1da7c-249">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="1da7c-250">Kalite emri gereksinimi özel bir tesisi, maddeyi veya satıcıyı ya da bunların bir birleşimini yansıtabilir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-250">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="1da7c-251">Bir üretim emrine gönderme yapan ve el ile oluşturulmuş bir kalite emri, tasarlanmış örnek alma planı gibi, bir kalite bağlantısı kaydında bulunan bilgileri kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-251">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1da7c-252">Bir rota operasyonuna sahip olan üretim emri</span><span class="sxs-lookup"><span data-stu-id="1da7c-252">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="1da7c-253">Bir operasyon için bir rapor sona erdikten önce veya sonra</span><span class="sxs-lookup"><span data-stu-id="1da7c-253">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="1da7c-254">Son operasyon için raporlama üretimi bittikten sonra.</span><span class="sxs-lookup"><span data-stu-id="1da7c-254">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="1da7c-255">Kalite emri gereksinimi özel bir tesisi, maddeyi veya operasyon kaynağı ya da bunların bir birleşimini yansıtabilir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-255">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="1da7c-256">Bir rota operasyonu gönderme yapan ve el ile oluşturulmuş bir kalite emri, tasarlanmış örnek alma planı gibi, bir kalite bağlantısı kaydında bulunan bilgileri kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-256">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1da7c-257">Stok</span><span class="sxs-lookup"><span data-stu-id="1da7c-257">Inventory</span></span></td>
<td><span data-ttu-id="1da7c-258">Bir kalite emri, transfer emri hareketleri veya bir stok günlüğünde bir hareket için otomatik olarak oluşturulamaz.</span><span class="sxs-lookup"><span data-stu-id="1da7c-258">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="1da7c-259">Bir kalite emrinin bir maddenin stok miktarı için el ile oluşturulması gerekir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-259">A quality order must be created manually for an item's inventory quantity.</span></span> <span data-ttu-id="1da7c-260">Fiziksel eldeki stok gereklidir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-260">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a><span data-ttu-id="1da7c-261">Kalite yönetim sayfaları</span><span class="sxs-lookup"><span data-stu-id="1da7c-261">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1da7c-262">Sayfa</span><span class="sxs-lookup"><span data-stu-id="1da7c-262">Page</span></span></th>
<th><span data-ttu-id="1da7c-263">Açıklama</span><span class="sxs-lookup"><span data-stu-id="1da7c-263">Description</span></span></th>
<th><span data-ttu-id="1da7c-264">Örnek</span><span class="sxs-lookup"><span data-stu-id="1da7c-264">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1da7c-265">Kalite ilişkileri</span><span class="sxs-lookup"><span data-stu-id="1da7c-265">Quality associations</span></span></td>
<td><span data-ttu-id="1da7c-266">Bu makalenin önceki bölümlerine bakınız.</span><span class="sxs-lookup"><span data-stu-id="1da7c-266">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="1da7c-267">Bir kalite ilişkisi oluşturulan bir kalite emri için aşağıdaki tüm bilgileri tanımlar:</span><span class="sxs-lookup"><span data-stu-id="1da7c-267">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="1da7c-268">Hareket olayı</span><span class="sxs-lookup"><span data-stu-id="1da7c-268">The transaction event</span></span></li>
<li><span data-ttu-id="1da7c-269">Öğeler üzerinde gerçekleştirilmesi gereken test dizileri</span><span class="sxs-lookup"><span data-stu-id="1da7c-269">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="1da7c-270">Kabul edilebilir kalite düzeyi</span><span class="sxs-lookup"><span data-stu-id="1da7c-270">The AQL</span></span></li>
<li><span data-ttu-id="1da7c-271">Örnekleme planı</span><span class="sxs-lookup"><span data-stu-id="1da7c-271">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="1da7c-272">Kalite emirlerinin otomatik olarak oluşturulmasını gerektiren iş işlemindeki her farklılık için bir kalite eşleştirmesi tanımlamanız gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-272">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="1da7c-273">Örneğin, satınalma siparişleri, karantina siparişleri, satış siparişleri ve üretim emirleri için iş süreçlerinde bir kalite emri oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-273">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1da7c-274">Testler</span><span class="sxs-lookup"><span data-stu-id="1da7c-274">Tests</span></span></td>
<td><span data-ttu-id="1da7c-275">Ürünlerinizin kalite belirtimlerini sağlayıp sağlamadığını belirleyen tek tek testler tanımlamak ve görüntülemek için bu sayfayı kullanın.</span><span class="sxs-lookup"><span data-stu-id="1da7c-275">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="1da7c-276">Bir veya daha çok bireysel testleri bir test grubuna atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1da7c-276">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="1da7c-277">Bu durumda, kabul edilebilir ölçüm değerleri gibi teste özgü bilgileri de belirtirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1da7c-277">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="1da7c-278">Ölçüm değerleri nicel testleri için kullanılır ve nitel testler için test değişkenleri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1da7c-278">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="1da7c-279">Nicel bir testin bir test tür <strong>tamsayı</strong> veya <strong>kesir</strong>, ve de atanmış bir ölçüsü vardır.</span><span class="sxs-lookup"><span data-stu-id="1da7c-279">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="1da7c-280">Kalite belirtimleri ve test sonuçları sayı olarak ifade edilir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-280">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="1da7c-281">Kalite testi, <strong>Seçenek</strong> test tipindedir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-281">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="1da7c-282">Kalite testleri, ölçülmekte olan değişken ve onun numaralandırılmış seçenekleri hakkında ek bilgi gerektirirler.</span><span class="sxs-lookup"><span data-stu-id="1da7c-282">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="1da7c-283">Kalite belirtimleri ve test sonuçları bir sonuca göre ifade edilirler.</span><span class="sxs-lookup"><span data-stu-id="1da7c-283">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="1da7c-284">Bir üretim şirketi satınalınan malzeme üzerinde, malzeme kalitesi hakkında bir sayısal test ile ambalaj hasarı üzerine bir kalite testi dahil olmak üzere iki test gerçekleştiriyor.</span><span class="sxs-lookup"><span data-stu-id="1da7c-284">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="1da7c-285">Şirket, test değişkenini (hasarlı ambalaj) ve sonuçlarını tanımlamak için ek bilgiler tanımlıyor.</span><span class="sxs-lookup"><span data-stu-id="1da7c-285">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="1da7c-286">Şirket <strong>Test grupları</strong> sayfasını iki testleri bir test grubuna atamak için ve teste özgü bilgileri belirtmek için kullanır.</span><span class="sxs-lookup"><span data-stu-id="1da7c-286">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="1da7c-287">Test grubu, şirketin iki teste ait test sonuçlarını rapor edebilmesi için bir kalite emrine atanır.</span><span class="sxs-lookup"><span data-stu-id="1da7c-287">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1da7c-288">Test grupları</span><span class="sxs-lookup"><span data-stu-id="1da7c-288">Test groups</span></span></td>
<td><span data-ttu-id="1da7c-289">Test gruplarını ve test grubuna atanmış bireysel testleri ayarlamak, düzenlemek ve görüntülemek için bu sayfayı kullanın.</span><span class="sxs-lookup"><span data-stu-id="1da7c-289">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="1da7c-290">Üst bölme test gruplarını gösterir ve alt bölme seçili bir test grubuna atanan testleri görüntüler.</span><span class="sxs-lookup"><span data-stu-id="1da7c-290">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="1da7c-291">Test grubuna; örnekleme planı, kabul edilebilir kalite düzeyi ve bozucu test gereksinimi gibi birçok ilke atarsınız.</span><span class="sxs-lookup"><span data-stu-id="1da7c-291">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="1da7c-292">Tek bir testi bir test grubuna atadığınızda, sıra, belgeler ve geçerlilik tarihleri gibi ek bilgiler tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="1da7c-292">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="1da7c-293">Nicel bir test için tanımladığınız bilgilere kabul edilebilir ölçüm değerleri de dahildir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-293">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="1da7c-294">Nitel bir test için bu bilgilere test değişkeni ve varsayılan sonuç dahildir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-294">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="1da7c-295">Bir kalite emrine atanan test grubu, belirtilen öğe üzerinde gerçekleştirilmesi gereken testlerin varsayılan kümesini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="1da7c-295">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="1da7c-296">Bununla birlikte, kalite emrindeki testleri değiştirebilirsiniz, ekleyebilir veya silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1da7c-296">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="1da7c-297">Test sonuçları, kalite emrindeki her test için rapor edilir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-297">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="1da7c-298">Bir üretim şirketi, kalite yönergelerindeki her sapma için bir test grubu tanımlıyor.</span><span class="sxs-lookup"><span data-stu-id="1da7c-298">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="1da7c-299">Çeşitli test grupları, örnekleme planları arasındaki farklılıkları, birlikte gerçekleştirilmesi gereken testler kümesini, kabul edilebilir kalite düzeyini ve diğer etkenleri yansıtır.</span><span class="sxs-lookup"><span data-stu-id="1da7c-299">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="1da7c-300">Nicel testleri için, kabul edilebilir ölçüm değerleri için de farklılıklar vardır.</span><span class="sxs-lookup"><span data-stu-id="1da7c-300">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="1da7c-301">Şirket, kalite kurallarını uygulayabilmek için kalite emirlerini otomatik oluşturabilmek için her kurala bir test grubunu <strong>Kalite ilişkilendirmeleri</strong> sayfasından atar ve ayrıca el ile oluşturulan kalite emirlerine de bir test grubu atar.</span><span class="sxs-lookup"><span data-stu-id="1da7c-301">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1da7c-302">Madde kalite grupları</span><span class="sxs-lookup"><span data-stu-id="1da7c-302">Item quality groups</span></span></td>
<td><span data-ttu-id="1da7c-303">Bir kalite grubuna atanmış maddeleri veya bir maddeye atanmış kalite gruplarını ayarlamak, düzenlemek ve görüntülemek için bu sayfayı kullanın.</span><span class="sxs-lookup"><span data-stu-id="1da7c-303">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="1da7c-304">Kalite grubu, maddeler için ortak test gereksinimlerini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="1da7c-304">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="1da7c-305"><strong>Test grupları</strong> sayfasındaki test gereksinimlerini tanımladıktan sonra, kalite emirlerini otomatik olarak oluşturmak için kurallar tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1da7c-305">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="1da7c-306">İşlemi basitleştirmek için, kuralları her bir öğe için tanımlamanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="1da7c-306">To simplify the process, you don't define rules for individual items.</span></span> <span data-ttu-id="1da7c-307">Bunun yerine, <strong>Kalite ilişkileri</strong> sayfasını kullanarak bir kalite grubu için kurallar tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="1da7c-307">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="1da7c-308">Ayrıca <strong>Madde kalite grupları</strong> sayfasını kullanarak belirlenmiş bir kalite grubuna ilgili maddeleri atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1da7c-308">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="1da7c-309">Ayrıca <strong>Madde kalite grupları</strong> sayfasını kullanarak belirlenmiş bir maddeye bir kalite grubuna ilgili maddeye atabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1da7c-309">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="1da7c-310">Üretim şirketi, gelen denetim için aynı test gereksinimlerine sahip çeşitli hammaddeler satın alıyor.</span><span class="sxs-lookup"><span data-stu-id="1da7c-310">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="1da7c-311">Şirket bir kalite grubu tanımlar ve artından hammaddeler ile ilişkilendirilmiş olan madde numaralarını bu gruba atar.</span><span class="sxs-lookup"><span data-stu-id="1da7c-311">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="1da7c-312">Daha sonra aynı sınama gereksinimleri olan yeni bir hammadde türü şirket tarafından satın alınır.</span><span class="sxs-lookup"><span data-stu-id="1da7c-312">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="1da7c-313">Yeni malzeme için yeni test gereksinimleri ayarlamak yerine, şirket yeni malzeme için madde numarasını mevcut kalite grubuna ekler.</span><span class="sxs-lookup"><span data-stu-id="1da7c-313">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="1da7c-314">Aynı üretim şirketi, aynı üretim testi gereksinimlerine sahip maddeler de üretiyor ve ön sevkiyat testleri için aynı gereksinimlere sahip maddeleri sevk ediyor.</span><span class="sxs-lookup"><span data-stu-id="1da7c-314">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="1da7c-315">Şirket iki ek kalite grubu tanımlıyor ve sonra her gruba ilgili madde numaralarını atıyor.</span><span class="sxs-lookup"><span data-stu-id="1da7c-315">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1da7c-316">Test değişkenleri</span><span class="sxs-lookup"><span data-stu-id="1da7c-316">Test variables</span></span></td>
<td><span data-ttu-id="1da7c-317">Nitel bir test ile ilişkili değişkenleri görüntülemek ve tanımlamak için bu sayfayı kullanın.</span><span class="sxs-lookup"><span data-stu-id="1da7c-317">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="1da7c-318">Her değişken için olası sonuçları gösteren numaralandırılmış seçenekleri tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="1da7c-318">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="1da7c-319">Testleri tanımlamak için <strong>Testler</strong> sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="1da7c-319">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="1da7c-320">Nitel testler için test türünü <strong>Seçenek</strong> olarak ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-320">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="1da7c-321"><strong>Test grupları</strong> sayfasını kullanarak bir teste bir test değişkeni atayın.</span><span class="sxs-lookup"><span data-stu-id="1da7c-321">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="1da7c-322">Kurabiye üreten bir üretim şirketi, tamamlanan ürüne yönelik bir denetim testi uyguluyor.</span><span class="sxs-lookup"><span data-stu-id="1da7c-322">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="1da7c-323">Bu inceleme testinin birçok değişkeni vardır.</span><span class="sxs-lookup"><span data-stu-id="1da7c-323">This inspection test has several variables.</span></span> <span data-ttu-id="1da7c-324">Bir değişken lezzettir ve bu değişkenin olası sonuçları iyi veya kötü olabilir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-324">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="1da7c-325">İkinci bir değişken, çok koyu, çok açık ve doğru sonuçları ile temsil edilen renk değişkeni oluyor.</span><span class="sxs-lookup"><span data-stu-id="1da7c-325">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1da7c-326">Test değişkeni sonuçları</span><span class="sxs-lookup"><span data-stu-id="1da7c-326">Test variable outcomes</span></span></td>
<td><span data-ttu-id="1da7c-327">Bir kalite testiyle ilişkili bir test değişkenine ait olası test sonuçlarını ayarlamak, düzenlemek ve görüntülemek için bu sayfayı kullanın.</span><span class="sxs-lookup"><span data-stu-id="1da7c-327">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="1da7c-328">Her sonuç için bir <strong>geçti</strong> veya <strong>başarısız</strong> oldu durumu atarsınız.</span><span class="sxs-lookup"><span data-stu-id="1da7c-328">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="1da7c-329"><strong>Testler</strong> sayfasında tanımlanan her nitel test için bir değişken ve sonuçlarını tanımlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="1da7c-329">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="1da7c-330">(Kalite testleri için, test türü <strong>Testler</strong> sayfasında <strong>Seçenek</strong> olarak ayarlanmıştır.) <strong>Test grupları</strong> sayfasını kullanıp, bir test değişkenini ve varsayılan sonucu bir kişisel kalite testine atayın.</span><span class="sxs-lookup"><span data-stu-id="1da7c-330">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="1da7c-331">Kurabiye üreten bir üretim şirketi, tamamlanan ürüne yönelik bir denetim testi uyguluyor.</span><span class="sxs-lookup"><span data-stu-id="1da7c-331">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="1da7c-332">Bu inceleme testinin birçok değişkeni vardır.</span><span class="sxs-lookup"><span data-stu-id="1da7c-332">This inspection test has of several variables.</span></span> <span data-ttu-id="1da7c-333">Bir değişken lezzettir ve bu değişkenin olası sonuçları iyi veya kötü olabilir.</span><span class="sxs-lookup"><span data-stu-id="1da7c-333">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="1da7c-334">İkinci bir değişken, çok koyu, çok açık ve doğru sonuçları ile temsil edilen renk değişkeni oluyor.</span><span class="sxs-lookup"><span data-stu-id="1da7c-334">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="1da7c-335">Her sonuca <strong>geçti</strong> veya <strong>kaldı</strong> durumu atanır.</span><span class="sxs-lookup"><span data-stu-id="1da7c-335">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="1da7c-336">Her değişkene yönelik denetim testi sırasında, denetçi sonuçlardan birini seçerek test sonucunu rapor ediyor.</span><span class="sxs-lookup"><span data-stu-id="1da7c-336">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="see-also"></a><span data-ttu-id="1da7c-337">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="1da7c-337">See also</span></span>
--------

[<span data-ttu-id="1da7c-338">Kalite yönetimi işlemleri</span><span class="sxs-lookup"><span data-stu-id="1da7c-338">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="1da7c-339">Uygunsuzluk yönetiminin etkinleştirilmesi</span><span class="sxs-lookup"><span data-stu-id="1da7c-339">Enabling nonconformance management</span></span>](enable-nonconformance-management.md)

