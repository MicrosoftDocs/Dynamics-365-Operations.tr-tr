---
title: Kalite yönetimine genel bakış
description: Bu koun, tedarik zincirinizde ürün kalitesini artırmak için Dynamics 365 Supply Chain Management'teki kalite yönetimini nasıl kullanabileceğiniz açıklar.
author: perlynne
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c2d51c659d9d06f075458359d81de978e7a6d14b
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814410"
---
# <a name="quality-management-overview"></a><span data-ttu-id="5b037-103">Kalite yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="5b037-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5b037-104">Bu koun, tedarik zincirinizde ürün kalitesini artırmak için Dynamics 365 Supply Chain Management'teki kalite yönetimini nasıl kullanabileceğiniz açıklar.</span><span class="sxs-lookup"><span data-stu-id="5b037-104">This topic describes how you can use quality management in Dynamics 365 Supply Chain Management to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="5b037-105">Kalite Yönetimi, uyumsuz ürünler,, kendi başlangıç noktalarını dikkate almadan işleyecek döngü sürelerini yönetmenize yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="5b037-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="5b037-106">Tanı türleri düzeltme raporlaması ile bağlantılı olduğundan, Supply Chain Management sorunları düzeltmek ve oluşmalarını önlemek için görevleri zamanlayabilir.</span><span class="sxs-lookup"><span data-stu-id="5b037-106">Because diagnostic types are linked to correction reporting, Supply Chain Management can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="5b037-107">Uygunsuzluğu yönetmek için daha fazla işlevselliğe ek olarak, Kalite Yönetimi sorun türüne göre sorunları (hatta iç sorunları) izlemek için ve çözümleri kısa vadeli veya uzun vadeli olarak tanımlamak için işlev içerir.</span><span class="sxs-lookup"><span data-stu-id="5b037-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="5b037-108">Anahtar performans göstergeleri (APG) ile ilgili istatistikler, önceki uygunsuzluk sorunlarının geçmişi ve bunları düzeltmek için kullanılan çözümler hakkında bir anlayış sağlar.</span><span class="sxs-lookup"><span data-stu-id="5b037-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="5b037-109">Önceki kalite ölçülerinin geçmişteki etkilerini incelemek ve ileride kullanılmaya uygun önlemleri belirlemek için geçmişe dönük verileri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5b037-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="5b037-110">Bir kalite ilişkisi ayarladığınızda, Supply Chain Management çeşitli iş süreçleri, olaylar ve koşullar için kalite emirleri oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="5b037-110">When you set up a quality association, Supply Chain Management can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="5b037-111">Kalite ilişkisi, belirli bir madde, belirli bir madde grubu veya tüm öğeleri kapsayabilir.</span><span class="sxs-lookup"><span data-stu-id="5b037-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="5b037-112">Kalite yönetimi kullanımına örnekler</span><span class="sxs-lookup"><span data-stu-id="5b037-112">Examples of the use of quality management</span></span>
<span data-ttu-id="5b037-113">Kalite Yönetimi esnektir ve tedarik zinciri işlemlerinin belirli düzeylerdeki gereksinimlerini karşılamak için çeşitli şekillerde uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="5b037-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="5b037-114">Aşağıdaki örneklerde, bu özelliklerin olası kullanımı gösterilmektedir:</span><span class="sxs-lookup"><span data-stu-id="5b037-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="5b037-115">Önceden tanımlanmış ölçütlere (belirli bir satıcı satınalma siparişinden, ambar kaydı) dayalı bir kalite kontrol işlemini otomatik olarak başlatın.</span><span class="sxs-lookup"><span data-stu-id="5b037-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="5b037-116">Onaylanmamış stokun kullanılmasını engellemek için inceleme sırasında stoku bloklayın(Tüm satınalma siparişi miktarlarını engelleme).</span><span class="sxs-lookup"><span data-stu-id="5b037-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="5b037-117">Madde örneklemeyi kalite ilişkilendirmesinin bir parçası olarak, denetlenmesi gereken geçerli fiziksel stok miktarını tanımlamak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="5b037-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="5b037-118">Örnekleme miktar veya yüzde tabanlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="5b037-118">Sampling can be based on fixed quantities or a percentage.</span></span>
-   <span data-ttu-id="5b037-119">Kısmi alış irsaliyeleri için kalite emirleri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5b037-119">Create quality orders for partial receipts.</span></span> <span data-ttu-id="5b037-120">Bir siparişten fiziksel olarak alına miktara bağlı olarak oluşturulan bir kalite emri oluşturmak için **Madde örnekleme** formundaki **Güncelleştirilen miktar başına** onay kutusunu seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="5b037-120">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="5b037-121">Minimum, maksimum ve hedef test değerleri içeren test türleri oluşturun ve doğrulama sonuçları önceden tanımlanmış olan niteliğe karşı nicelik sınamaları gerçekleştirin.</span><span class="sxs-lookup"><span data-stu-id="5b037-121">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="5b037-122">Kalite Ölçüm toleranslarını kontrol etmek için bir kabul edilebilir kalite düzeyi (AQL) belirtin.</span><span class="sxs-lookup"><span data-stu-id="5b037-122">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="5b037-123">Denetleme işlemi için gereken test alanı ve test aletleri gibi kaynakları belirtin.</span><span class="sxs-lookup"><span data-stu-id="5b037-123">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="5b037-124">Kalite ilişkileri ile çalışmak</span><span class="sxs-lookup"><span data-stu-id="5b037-124">Working with quality associations</span></span>
<span data-ttu-id="5b037-125">Kalite ilişkisini kullanan iş süreci, satınalma siparişleri, satış siparişleri veya üretim emirleri gibi çeşitli kaynak belgelere ilişkili olabilir.</span><span class="sxs-lookup"><span data-stu-id="5b037-125">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="5b037-126">Her kalite bağlantısı kaydı oluşturulan kalite emirlerine geçerli olacak testler kümesini, AQL'yi ve örnek alma planını da tanımlamaktadır.</span><span class="sxs-lookup"><span data-stu-id="5b037-126">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="5b037-127">Bir iş sürecindeki her değişim için bir kalite ilişkisi kaydı tanımlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="5b037-127">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="5b037-128">Örneğin, bir satınalma siparişi ürün alış irsaliyesi güncelleştirildiğinde, kalite emri oluşturacak bir kalite ilişkisi ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5b037-128">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="5b037-129">Yürütme planı kurulumuna bağlı olarak, açık bir kalite emri yok ya da satınalma siparişi faturalama gibi sonraki işlemler, engellenen tetikleyici işlem engellenebilir.</span><span class="sxs-lookup"><span data-stu-id="5b037-129">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="5b037-130">**Not:** Açık kalite emirleri olduğunda, stok miktarlarının çıkarılması otomatik olarak engellenir.</span><span class="sxs-lookup"><span data-stu-id="5b037-130">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="5b037-131">**Madde örnekleri** sayfasında bulunan **Tam engelleme** ayarına bağlı olarak, miktar kalite emrindeki miktardır ya da kaynak belge satırındaki miktardır.</span><span class="sxs-lookup"><span data-stu-id="5b037-131">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="5b037-132">Bir iş süreci için, kalite ilişkisi kaydı, kalite emrinin oluşturulduğu olay ve koşulları tanımlar.</span><span class="sxs-lookup"><span data-stu-id="5b037-132">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="5b037-133">Koşullar bir siteye veya bir tüzel kişiliğe özel olabilir.</span><span class="sxs-lookup"><span data-stu-id="5b037-133">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="5b037-134">Bozucu testler içeren bir kalite emri yalnızca olay için eldeki stok bulunması durumunda oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="5b037-134">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="5b037-135">Aşağıdaki örnekler, her iş sürecindeki değişiklikler için bir kalite bağlantısını tanımlamayı açıklar.</span><span class="sxs-lookup"><span data-stu-id="5b037-135">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="5b037-136">Her örnek için, aşağıdaki tablo kalite ilişki kaydındaki olayları ve durumları özetler.</span><span class="sxs-lookup"><span data-stu-id="5b037-136">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="5b037-137">Referans türü</span><span class="sxs-lookup"><span data-stu-id="5b037-137">Reference type</span></span></th>
<th><span data-ttu-id="5b037-138">Olay türü</span><span class="sxs-lookup"><span data-stu-id="5b037-138">Event type</span></span></th>
<th><span data-ttu-id="5b037-139">Yürütme</span><span class="sxs-lookup"><span data-stu-id="5b037-139">Execution</span></span></th>
<th><span data-ttu-id="5b037-140">Olay durdurma</span><span class="sxs-lookup"><span data-stu-id="5b037-140">Event blocking</span></span></th>
<th><span data-ttu-id="5b037-141">Belge başvurusu</span><span class="sxs-lookup"><span data-stu-id="5b037-141">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="5b037-142">Stok</span><span class="sxs-lookup"><span data-stu-id="5b037-142">Inventory</span></span></td>
<td><span data-ttu-id="5b037-143">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="5b037-143">Not applicable</span></span></td>
<td><span data-ttu-id="5b037-144">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="5b037-144">Not applicable</span></span></td>
<td><span data-ttu-id="5b037-145">Yok</span><span class="sxs-lookup"><span data-stu-id="5b037-145">None</span></span></td>
<td><span data-ttu-id="5b037-146">Tümü</span><span class="sxs-lookup"><span data-stu-id="5b037-146">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="5b037-147">Satışlar</span><span class="sxs-lookup"><span data-stu-id="5b037-147">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="5b037-148">Malzeme çekme işlemi planlandı</span><span class="sxs-lookup"><span data-stu-id="5b037-148">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="5b037-149">Önce</span><span class="sxs-lookup"><span data-stu-id="5b037-149">Before</span></span></td>
<td><span data-ttu-id="5b037-150">Yok</span><span class="sxs-lookup"><span data-stu-id="5b037-150">None</span></span></td>
<td rowspan="22"><span data-ttu-id="5b037-151">Belirli Kimlik, Grup veya Yalnızca tümü</span><span class="sxs-lookup"><span data-stu-id="5b037-151">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b037-152">Malzeme çekme işlemi</span><span class="sxs-lookup"><span data-stu-id="5b037-152">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b037-153">Sevk irsaliyesi</span><span class="sxs-lookup"><span data-stu-id="5b037-153">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b037-154">Fatura</span><span class="sxs-lookup"><span data-stu-id="5b037-154">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5b037-155">Sevk irsaliyesi</span><span class="sxs-lookup"><span data-stu-id="5b037-155">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="5b037-156">Önce</span><span class="sxs-lookup"><span data-stu-id="5b037-156">Before</span></span></td>
<td><span data-ttu-id="5b037-157">Yok</span><span class="sxs-lookup"><span data-stu-id="5b037-157">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b037-158">Sevk irsaliyesi</span><span class="sxs-lookup"><span data-stu-id="5b037-158">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b037-159">Fatura</span><span class="sxs-lookup"><span data-stu-id="5b037-159">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="5b037-160">Satınalma</span><span class="sxs-lookup"><span data-stu-id="5b037-160">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="5b037-161">Giriş listesi</span><span class="sxs-lookup"><span data-stu-id="5b037-161">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="5b037-162">Önce</span><span class="sxs-lookup"><span data-stu-id="5b037-162">Before</span></span></td>
<td><span data-ttu-id="5b037-163">Yok</span><span class="sxs-lookup"><span data-stu-id="5b037-163">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b037-164">Giriş listesi</span><span class="sxs-lookup"><span data-stu-id="5b037-164">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b037-165">Ürün girişi</span><span class="sxs-lookup"><span data-stu-id="5b037-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b037-166">Fatura</span><span class="sxs-lookup"><span data-stu-id="5b037-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5b037-167">Sonra</span><span class="sxs-lookup"><span data-stu-id="5b037-167">After</span></span></td>
<td><span data-ttu-id="5b037-168">Yok</span><span class="sxs-lookup"><span data-stu-id="5b037-168">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b037-169">Ürün girişi</span><span class="sxs-lookup"><span data-stu-id="5b037-169">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b037-170">Fatura</span><span class="sxs-lookup"><span data-stu-id="5b037-170">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5b037-171">Kayıt</span><span class="sxs-lookup"><span data-stu-id="5b037-171">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="5b037-172">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="5b037-172">Not applicable</span></span></td>
<td><span data-ttu-id="5b037-173">Yok</span><span class="sxs-lookup"><span data-stu-id="5b037-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b037-174">Ürün girişi</span><span class="sxs-lookup"><span data-stu-id="5b037-174">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b037-175">Fatura</span><span class="sxs-lookup"><span data-stu-id="5b037-175">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="5b037-176">Ürün girişi</span><span class="sxs-lookup"><span data-stu-id="5b037-176">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="5b037-177">Önce</span><span class="sxs-lookup"><span data-stu-id="5b037-177">Before</span></span></td>
<td><span data-ttu-id="5b037-178">Yok</span><span class="sxs-lookup"><span data-stu-id="5b037-178">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b037-179">Ürün girişi</span><span class="sxs-lookup"><span data-stu-id="5b037-179">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b037-180">Fatura</span><span class="sxs-lookup"><span data-stu-id="5b037-180">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5b037-181">Sonra</span><span class="sxs-lookup"><span data-stu-id="5b037-181">After</span></span></td>
<td><span data-ttu-id="5b037-182">Yok</span><span class="sxs-lookup"><span data-stu-id="5b037-182">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b037-183">Fatura</span><span class="sxs-lookup"><span data-stu-id="5b037-183">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="5b037-184">Üretim</span><span class="sxs-lookup"><span data-stu-id="5b037-184">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="5b037-185">Kayıt</span><span class="sxs-lookup"><span data-stu-id="5b037-185">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="5b037-186">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="5b037-186">Not applicable</span></span></td>
<td><span data-ttu-id="5b037-187">Yok</span><span class="sxs-lookup"><span data-stu-id="5b037-187">None</span></span></td>
<td rowspan="12"><span data-ttu-id="5b037-188">Tümü</span><span class="sxs-lookup"><span data-stu-id="5b037-188">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b037-189">Tamamlandı bildirimi</span><span class="sxs-lookup"><span data-stu-id="5b037-189">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b037-190">Bitir</span><span class="sxs-lookup"><span data-stu-id="5b037-190">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="5b037-191">Tamamlandı bildirimi</span><span class="sxs-lookup"><span data-stu-id="5b037-191">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="5b037-192">Önce</span><span class="sxs-lookup"><span data-stu-id="5b037-192">Before</span></span></td>
<td><span data-ttu-id="5b037-193">Yok</span><span class="sxs-lookup"><span data-stu-id="5b037-193">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b037-194">Tamamlandı bildirimi</span><span class="sxs-lookup"><span data-stu-id="5b037-194">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b037-195">Bitir</span><span class="sxs-lookup"><span data-stu-id="5b037-195">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5b037-196">Sonra</span><span class="sxs-lookup"><span data-stu-id="5b037-196">After</span></span></td>
<td><span data-ttu-id="5b037-197">Yok</span><span class="sxs-lookup"><span data-stu-id="5b037-197">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b037-198">Bitir</span><span class="sxs-lookup"><span data-stu-id="5b037-198">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="5b037-199">Karantina</span><span class="sxs-lookup"><span data-stu-id="5b037-199">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="5b037-200">Tamamlandı bildirimi</span><span class="sxs-lookup"><span data-stu-id="5b037-200">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="5b037-201">Önce</span><span class="sxs-lookup"><span data-stu-id="5b037-201">Before</span></span></td>
<td><span data-ttu-id="5b037-202">Tamamlandı bildirimi</span><span class="sxs-lookup"><span data-stu-id="5b037-202">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b037-203">Bitir</span><span class="sxs-lookup"><span data-stu-id="5b037-203">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b037-204">Sonra</span><span class="sxs-lookup"><span data-stu-id="5b037-204">After</span></span></td>
<td><span data-ttu-id="5b037-205">Bitir</span><span class="sxs-lookup"><span data-stu-id="5b037-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b037-206">Bitir</span><span class="sxs-lookup"><span data-stu-id="5b037-206">End</span></span></td>
<td><span data-ttu-id="5b037-207">Önce</span><span class="sxs-lookup"><span data-stu-id="5b037-207">Before</span></span></td>
<td><span data-ttu-id="5b037-208">Bitir</span><span class="sxs-lookup"><span data-stu-id="5b037-208">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5b037-209">Rota operasyonu</span><span class="sxs-lookup"><span data-stu-id="5b037-209">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="5b037-210">Tamamlandı bildirimi</span><span class="sxs-lookup"><span data-stu-id="5b037-210">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="5b037-211">Önce</span><span class="sxs-lookup"><span data-stu-id="5b037-211">Before</span></span></td>
<td><span data-ttu-id="5b037-212">Yok</span><span class="sxs-lookup"><span data-stu-id="5b037-212">None</span></span></td>
<td rowspan="3"><span data-ttu-id="5b037-213">Belirli Kimlik, Grup veya Tümü ve Kaynağa özel, Grup veya Tümü</span><span class="sxs-lookup"><span data-stu-id="5b037-213">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b037-214">Tamamlandı bildirimi</span><span class="sxs-lookup"><span data-stu-id="5b037-214">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b037-215">Sonra</span><span class="sxs-lookup"><span data-stu-id="5b037-215">After</span></span></td>
<td><span data-ttu-id="5b037-216">Yok</span><span class="sxs-lookup"><span data-stu-id="5b037-216">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5b037-217">Ortak ürün üretimi</span><span class="sxs-lookup"><span data-stu-id="5b037-217">Co-product production</span></span></td>
<td><span data-ttu-id="5b037-218">Kayıt</span><span class="sxs-lookup"><span data-stu-id="5b037-218">Registration</span></span></td>
<td><span data-ttu-id="5b037-219">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="5b037-219">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5b037-220">Yok</span><span class="sxs-lookup"><span data-stu-id="5b037-220">None</span></span></td>
<td rowspan="3"><span data-ttu-id="5b037-221">Tümü</span><span class="sxs-lookup"><span data-stu-id="5b037-221">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5b037-222">Tamamlandı bildirimi</span><span class="sxs-lookup"><span data-stu-id="5b037-222">Report as finished</span></span></td>
<td><span data-ttu-id="5b037-223">Önce</span><span class="sxs-lookup"><span data-stu-id="5b037-223">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b037-224">Sonra</span><span class="sxs-lookup"><span data-stu-id="5b037-224">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5b037-225">Aşağıdaki tabloda belirli türde işlemler için kalite emirlerinin nasıl oluşturulabileceği hakkında daha fazla bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="5b037-225">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="5b037-226">İşleme türü</span><span class="sxs-lookup"><span data-stu-id="5b037-226">Type of process</span></span></th>
<th><span data-ttu-id="5b037-227">Kalite emirlerinin ne zaman otomatik olarak oluşturulabileceği</span><span class="sxs-lookup"><span data-stu-id="5b037-227">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="5b037-228">Bozucu sınama yapılması gerekirse kalite emirlerinin ne zaman oluşturulabileceği</span><span class="sxs-lookup"><span data-stu-id="5b037-228">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="5b037-229">Koşul bilgisi</span><span class="sxs-lookup"><span data-stu-id="5b037-229">Condition information</span></span></th>
<th><span data-ttu-id="5b037-230">El ile oluşturma bilgisi</span><span class="sxs-lookup"><span data-stu-id="5b037-230">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="5b037-231">Satın alma siparişi</span><span class="sxs-lookup"><span data-stu-id="5b037-231">Purchase order</span></span></td>
<td><span data-ttu-id="5b037-232">Alınan malzeme için ürün girişi ya da giriş listesi nakledildikten önce veya sonra.</span><span class="sxs-lookup"><span data-stu-id="5b037-232">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="5b037-233">Alınan malzeme için ürün girişi nakledildikten sonra, çünkü malzemenin bozucu test için mevcut olması gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="5b037-233">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="5b037-234">Kalite emri gereksinimi özel bir tesisi, maddeyi veya satıcıyı ya da bunların bir birleşimini yansıtabilir.</span><span class="sxs-lookup"><span data-stu-id="5b037-234">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="5b037-235">Bir satınalma siparişine gönderme yapan ve el ile oluşturulmuş bir kalite emri, tasarlanmış örnek alma planı gibi, bir kalite bağlantısı kaydında bulunan bilgileri kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="5b037-235">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b037-236">Karantina emri</span><span class="sxs-lookup"><span data-stu-id="5b037-236">Quarantine order</span></span></td>
<td><span data-ttu-id="5b037-237">Karantina siparişi tamamlandı veya sona erdi olarak bildirildikten önce veya sonra.</span><span class="sxs-lookup"><span data-stu-id="5b037-237">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="5b037-238">Yıkıcı testler gerektiren kalite emirleri oluşturulamaz.</span><span class="sxs-lookup"><span data-stu-id="5b037-238">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="5b037-239">Karantina siparişi işlevinin, yok edilen malzemenin değerlendirmesini üstleneceği kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="5b037-239">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="5b037-240">Kalite emri gereksinimi özel bir tesisi, maddeyi veya satıcıyı ya da bunların bir birleşimini yansıtabilir.</span><span class="sxs-lookup"><span data-stu-id="5b037-240">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="5b037-241">Bir karantina siparişine gönderme yapan ve el ile oluşturulmuş bir kalite emri, tasarlanmış örnek alma planı gibi, bir kalite bağlantısı kaydında bulunan bilgileri kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="5b037-241">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b037-242">Satış siparişi</span><span class="sxs-lookup"><span data-stu-id="5b037-242">Sales order</span></span></td>
<td><span data-ttu-id="5b037-243">Bir zamanlanmış malzeme çekme işlem veya sevk irsaliyesi güncelleştirmesi sevk maddeler için önce</span><span class="sxs-lookup"><span data-stu-id="5b037-243">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="5b037-244">Herhangi bir adımda</span><span class="sxs-lookup"><span data-stu-id="5b037-244">At any step</span></span></td>
<td><span data-ttu-id="5b037-245">Kalite emri gereksinimi özel bir tesisi, maddeyi veya satıcıyı ya da bunların bir birleşimini yansıtabilir.</span><span class="sxs-lookup"><span data-stu-id="5b037-245">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="5b037-246">Bir satış siparişine gönderme yapan ve el ile oluşturulmuş bir kalite emri, tasarlanmış örnek alma planı gibi, bir kalite bağlantısı kaydında bulunan bilgileri kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="5b037-246">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b037-247">Üretim emri</span><span class="sxs-lookup"><span data-stu-id="5b037-247">Production order</span></span></td>
<td><span data-ttu-id="5b037-248">Üretim emri için bitmiş miktar rapor edildikten önce veya sonra</span><span class="sxs-lookup"><span data-stu-id="5b037-248">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="5b037-249">Üretim emri için bitmiş miktar rapor edildikten sonra</span><span class="sxs-lookup"><span data-stu-id="5b037-249">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="5b037-250">Kalite emri gereksinimi özel bir tesisi, maddeyi veya satıcıyı ya da bunların bir birleşimini yansıtabilir.</span><span class="sxs-lookup"><span data-stu-id="5b037-250">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="5b037-251">Bir üretim emrine gönderme yapan ve el ile oluşturulmuş bir kalite emri, tasarlanmış örnek alma planı gibi, bir kalite bağlantısı kaydında bulunan bilgileri kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="5b037-251">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b037-252">Bir rota operasyonuna sahip olan üretim emri</span><span class="sxs-lookup"><span data-stu-id="5b037-252">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="5b037-253">Bir operasyon için bir rapor sona erdikten önce veya sonra</span><span class="sxs-lookup"><span data-stu-id="5b037-253">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="5b037-254">Son operasyon için raporlama üretimi bittikten sonra.</span><span class="sxs-lookup"><span data-stu-id="5b037-254">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="5b037-255">Kalite emri gereksinimi özel bir tesisi, maddeyi veya operasyon kaynağı ya da bunların bir birleşimini yansıtabilir.</span><span class="sxs-lookup"><span data-stu-id="5b037-255">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="5b037-256">Bir rota operasyonu gönderme yapan ve el ile oluşturulmuş bir kalite emri, tasarlanmış örnek alma planı gibi, bir kalite bağlantısı kaydında bulunan bilgileri kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="5b037-256">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5b037-257">Stok</span><span class="sxs-lookup"><span data-stu-id="5b037-257">Inventory</span></span></td>
<td><span data-ttu-id="5b037-258">Bir kalite emri, transfer emri hareketleri veya bir stok günlüğünde bir hareket için otomatik olarak oluşturulamaz.</span><span class="sxs-lookup"><span data-stu-id="5b037-258">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="5b037-259">Bir kalite emrinin bir maddenin stok miktarı için el ile oluşturulması gerekir.</span><span class="sxs-lookup"><span data-stu-id="5b037-259">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="5b037-260">Fiziksel eldeki stok gereklidir.</span><span class="sxs-lookup"><span data-stu-id="5b037-260">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-order-auto-generation-examples"></a><span data-ttu-id="5b037-261">Kalite emri otomatik oluşturma örnekleri</span><span class="sxs-lookup"><span data-stu-id="5b037-261">Quality order auto-generation examples</span></span>

### <a name="purchasing"></a><span data-ttu-id="5b037-262">Satınalma</span><span class="sxs-lookup"><span data-stu-id="5b037-262">Purchasing</span></span>

<span data-ttu-id="5b037-263">Satınalmada, **Kalite ilişkilendirmeleri** sayfasında **Olay türü** alanını **Ürün girişi** ve **Yürütme** alanını **Sonra** olarak ayarlarsanız aşağıdaki sonuçları elde edersiniz:</span><span class="sxs-lookup"><span data-stu-id="5b037-263">In purchasing, if you set the **Event type** field to **Product receipt** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span> 

- <span data-ttu-id="5b037-264">**Güncelleştirilen miktar başına** seçeneği **Evet** olarak ayarlanmışsa, madde örneklemesindeki teslim alınan miktar ve ayarlar temel alınarak satınalma siparişiyle ilgili her giriş için bir kalite emri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5b037-264">If the **Per updated quantity** option is set to **Yes**, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="5b037-265">Satınalma siparişine göre bir miktar her teslim alındığında, yeni teslim alınan miktar temel alınarak geçerli kalite emirleri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5b037-265">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="5b037-266">**Güncelleştirilen miktar başına** seçeneği **Hayır** olarak ayarlanmışsa, teslim alınan miktar ve ayarlar temel alınarak satınalma siparişiyle ilgili ilk giriş için bir kalite emri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5b037-266">If the **Per updated quantity** option is set to **No**, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="5b037-267">Ayrıca, izleme boyutlarına bağlı olarak kalan miktar temel alınarak bir veya daha fazla kalite emri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5b037-267">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="5b037-268">Satınalma siparişiyle ilgili sonraki girişler için kalite emirleri oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="5b037-268">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="5b037-269">Kalite belirtimi</span><span class="sxs-lookup"><span data-stu-id="5b037-269">Quality specification</span></span></th>
<th><span data-ttu-id="5b037-270">Güncelleştirilen miktar başına</span><span class="sxs-lookup"><span data-stu-id="5b037-270">Per updated quantity</span></span></th>
<th><span data-ttu-id="5b037-271">İzleme boyutu başına</span><span class="sxs-lookup"><span data-stu-id="5b037-271">Per tracking dimension</span></span></th>
<th><span data-ttu-id="5b037-272">Sonuç</span><span class="sxs-lookup"><span data-stu-id="5b037-272">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="5b037-273">Yüzde: %10</span><span class="sxs-lookup"><span data-stu-id="5b037-273">Percentage: 10%</span></span></td>
<td><span data-ttu-id="5b037-274">Evet</span><span class="sxs-lookup"><span data-stu-id="5b037-274">Yes</span></span></td>
<td>
<p><span data-ttu-id="5b037-275">Toplu iş numarası: Hayır</span><span class="sxs-lookup"><span data-stu-id="5b037-275">Batch number: No</span></span></p>
<p><span data-ttu-id="5b037-276">Seri numarası: Hayır</span><span class="sxs-lookup"><span data-stu-id="5b037-276">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="5b037-277">Sipariş miktarı: 100</span><span class="sxs-lookup"><span data-stu-id="5b037-277">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="5b037-278">30 için tamamlandı olarak bildir</span><span class="sxs-lookup"><span data-stu-id="5b037-278">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="5b037-279">3 için (30'un %10'u) için kalite emri #1</span><span class="sxs-lookup"><span data-stu-id="5b037-279">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="5b037-280">70 için tamamlandı olarak bildir</span><span class="sxs-lookup"><span data-stu-id="5b037-280">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="5b037-281">7 (kalan sipariş miktarının %10'u; bu durumda 70'e eşittir) için kalite emri #2</span><span class="sxs-lookup"><span data-stu-id="5b037-281">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="5b037-282">Sabit miktar: 1</span><span class="sxs-lookup"><span data-stu-id="5b037-282">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="5b037-283">Hayır</span><span class="sxs-lookup"><span data-stu-id="5b037-283">No</span></span></td>
<td>
<p><span data-ttu-id="5b037-284">Toplu iş numarası: Hayır</span><span class="sxs-lookup"><span data-stu-id="5b037-284">Batch number: No</span></span></p>
<p><span data-ttu-id="5b037-285">Seri numarası: Hayır</span><span class="sxs-lookup"><span data-stu-id="5b037-285">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="5b037-286">Sipariş miktarı: 100</span><span class="sxs-lookup"><span data-stu-id="5b037-286">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="5b037-287">30 için tamamlandı olarak bildir</span><span class="sxs-lookup"><span data-stu-id="5b037-287">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="5b037-288">1 için kalite emri #1 oluşturulur (sabit değeri 1 olan ilk tamamlandı bildirimi miktarı için).</span><span class="sxs-lookup"><span data-stu-id="5b037-288">Quality order #1 is created for 1 (for the first reported-as-finished quantity, which has a fixed value of 1).</span></span></li>
<li><span data-ttu-id="5b037-289">Kalan miktara göre başka kalite emri oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="5b037-289">No more quality orders are created against the remaining quantity.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="5b037-290">10 için tamamlandı olarak bildir</span><span class="sxs-lookup"><span data-stu-id="5b037-290">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="5b037-291">Kalite emri oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="5b037-291">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="5b037-292">60 için tamamlandı olarak bildir</span><span class="sxs-lookup"><span data-stu-id="5b037-292">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="5b037-293">Kalite emri oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="5b037-293">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="5b037-294">Sabit miktar: 1</span><span class="sxs-lookup"><span data-stu-id="5b037-294">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="5b037-295">Evet</span><span class="sxs-lookup"><span data-stu-id="5b037-295">Yes</span></span></td>
<td>
<p><span data-ttu-id="5b037-296">Toplu iş numarası: Evet</span><span class="sxs-lookup"><span data-stu-id="5b037-296">Batch number: Yes</span></span></p>
<p><span data-ttu-id="5b037-297">Seri numarası: Evet</span><span class="sxs-lookup"><span data-stu-id="5b037-297">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="5b037-298">Sipariş miktarı: 10</span><span class="sxs-lookup"><span data-stu-id="5b037-298">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="5b037-299">3 için tamamlandı olarak bildir</span><span class="sxs-lookup"><span data-stu-id="5b037-299">Report as finished for 3</span></span>
<ul>
<li><span data-ttu-id="5b037-300">Toplu iş #b1, seri #s1'deki 1 için kalite emri #1</span><span class="sxs-lookup"><span data-stu-id="5b037-300">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="5b037-301">Toplu iş #b2, seri #s2'deki 1 için kalite emri #2</span><span class="sxs-lookup"><span data-stu-id="5b037-301">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="5b037-302">Toplu iş #b3, seri #s3'deki 1 için kalite emri #3</span><span class="sxs-lookup"><span data-stu-id="5b037-302">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="5b037-303">2 için tamamlandı olarak bildir</span><span class="sxs-lookup"><span data-stu-id="5b037-303">Report as finished for 2</span></span>
<ul>
<li><span data-ttu-id="5b037-304">Toplu iş #b4, seri #s4'deki 1 için kalite emri #4</span><span class="sxs-lookup"><span data-stu-id="5b037-304">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="5b037-305">Toplu iş #b5, seri #s5'deki 1 için kalite emri #5</span><span class="sxs-lookup"><span data-stu-id="5b037-305">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="5b037-306"><strong>Not:</strong> Toplu iş yeniden kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="5b037-306"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="5b037-307">Sabit miktar: 2</span><span class="sxs-lookup"><span data-stu-id="5b037-307">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="5b037-308">Hayır</span><span class="sxs-lookup"><span data-stu-id="5b037-308">No</span></span></td>
<td>
<p><span data-ttu-id="5b037-309">Toplu iş numarası: Evet</span><span class="sxs-lookup"><span data-stu-id="5b037-309">Batch number: Yes</span></span></p>
<p><span data-ttu-id="5b037-310">Seri numarası: Evet</span><span class="sxs-lookup"><span data-stu-id="5b037-310">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="5b037-311">Sipariş miktarı: 10</span><span class="sxs-lookup"><span data-stu-id="5b037-311">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="5b037-312">4 için tamamlandı olarak bildir</span><span class="sxs-lookup"><span data-stu-id="5b037-312">Report as finished for 4</span></span>
<ul>
<li><span data-ttu-id="5b037-313">Toplu iş #b1, seri #s1'deki 1 için kalite emri #1.</span><span class="sxs-lookup"><span data-stu-id="5b037-313">Quality order #1 for 1 of batch #b1, serial #s1.</span></span></li>
<li><span data-ttu-id="5b037-314">Toplu iş #b2, seri #s2'deki 1 için kalite emri #2.</span><span class="sxs-lookup"><span data-stu-id="5b037-314">Quality order #2 for 1 of batch #b2, serial #s2.</span></span></li>
<li><span data-ttu-id="5b037-315">Toplu iş #b3, seri #s3'deki 1 için kalite emri #3.</span><span class="sxs-lookup"><span data-stu-id="5b037-315">Quality order #3 for 1 of batch #b3, serial #s3.</span></span></li>
<li><span data-ttu-id="5b037-316">Toplu iş #b4, seri #s4'deki 1 için kalite emri #4.</span><span class="sxs-lookup"><span data-stu-id="5b037-316">Quality order #4 for 1 of batch #b4, serial #s4.</span></span></li>
<li><span data-ttu-id="5b037-317">Kalan miktara göre başka kalite emri oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="5b037-317">No more quality orders are created against the remaining quantity.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="5b037-318">6 için tamamlandı olarak bildir</span><span class="sxs-lookup"><span data-stu-id="5b037-318">Report as finished for 6</span></span>
<ul>
<li><span data-ttu-id="5b037-319">Kalite emri oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="5b037-319">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="production"></a><span data-ttu-id="5b037-320">Üretim</span><span class="sxs-lookup"><span data-stu-id="5b037-320">Production</span></span>

<span data-ttu-id="5b037-321">Üretimde, **Kalite ilişkilendirmeleri** sayfasında **Olay türü** alanını **Tamamlandı olarak bildir** ve **Yürütme** alanını **Sonra** olarak ayarlarsanız aşağıdaki sonuçları elde edersiniz:</span><span class="sxs-lookup"><span data-stu-id="5b037-321">In production, if you set the **Event type** field to **Report as finished** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="5b037-322">**Güncelleştirilen miktar başına** seçeneği **Evet** olarak ayarlanmışsa, madde örneklemesindeki her tamamlanan miktar için bir kalite emri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5b037-322">If the **Per updated quantity** option is set to **Yes**, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="5b037-323">Üretim emrine göre bir miktar her tamamlandı olarak bildirildiğinde, yeni tamamlanan miktar temel alınarak geçerli kalite emirleri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5b037-323">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on newly finished quantity.</span></span> <span data-ttu-id="5b037-324">Bu oluşturma mantığı satın alma ile tutarlıdır.</span><span class="sxs-lookup"><span data-stu-id="5b037-324">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="5b037-325">**Güncelleştirilen miktar başına** seçeneği **Hayır** olarak ayarlanmışsa, tamamlanan miktar temel alınarak bir miktar ilk kez tamamlandı olarak bildirildiğinde bir kalite emri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5b037-325">If the **Per updated quantity** option is set to **No**, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="5b037-326">Ayrıca, madde örneklemesinin izleme boyutlarına bağlı olarak kalan miktar temel alınarak bir veya daha fazla kalite emri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5b037-326">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="5b037-327">Sonraki tamamlanan miktarlar için kalite emirleri oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="5b037-327">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="5b037-328">Kalite belirtimi</span><span class="sxs-lookup"><span data-stu-id="5b037-328">Quality specification</span></span></th>
<th><span data-ttu-id="5b037-329">Güncelleştirilen miktar başına</span><span class="sxs-lookup"><span data-stu-id="5b037-329">Per updated quantity</span></span></th>
<th><span data-ttu-id="5b037-330">İzleme boyutu başına</span><span class="sxs-lookup"><span data-stu-id="5b037-330">Per tracking dimension</span></span></th>
<th><span data-ttu-id="5b037-331">Sonuç</span><span class="sxs-lookup"><span data-stu-id="5b037-331">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="5b037-332">Yüzde: %10</span><span class="sxs-lookup"><span data-stu-id="5b037-332">Percentage: 10%</span></span></td>
<td><span data-ttu-id="5b037-333">Evet</span><span class="sxs-lookup"><span data-stu-id="5b037-333">Yes</span></span></td>
<td>
<p><span data-ttu-id="5b037-334">Toplu iş numarası: Hayır</span><span class="sxs-lookup"><span data-stu-id="5b037-334">Batch number: No</span></span></p>
<p><span data-ttu-id="5b037-335">Seri numarası: Hayır</span><span class="sxs-lookup"><span data-stu-id="5b037-335">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="5b037-336">Sipariş miktarı: 100</span><span class="sxs-lookup"><span data-stu-id="5b037-336">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="5b037-337">30 için tamamlandı olarak bildir</span><span class="sxs-lookup"><span data-stu-id="5b037-337">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="5b037-338">3 için (30'un %10'u) için kalite emri #1</span><span class="sxs-lookup"><span data-stu-id="5b037-338">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="5b037-339">70 için tamamlandı olarak bildir</span><span class="sxs-lookup"><span data-stu-id="5b037-339">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="5b037-340">7 (kalan sipariş miktarının %10'u; bu durumda 70'e eşittir) için kalite emri #2</span><span class="sxs-lookup"><span data-stu-id="5b037-340">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="5b037-341">Sabit miktar: 1</span><span class="sxs-lookup"><span data-stu-id="5b037-341">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="5b037-342">Hayır</span><span class="sxs-lookup"><span data-stu-id="5b037-342">No</span></span></td>
<td>
<p><span data-ttu-id="5b037-343">Toplu iş numarası: Hayır</span><span class="sxs-lookup"><span data-stu-id="5b037-343">Batch number: No</span></span></p>
<p><span data-ttu-id="5b037-344">Seri numarası: Hayır</span><span class="sxs-lookup"><span data-stu-id="5b037-344">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="5b037-345">Sipariş miktarı: 100</span><span class="sxs-lookup"><span data-stu-id="5b037-345">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="5b037-346">30 için tamamlandı olarak bildir</span><span class="sxs-lookup"><span data-stu-id="5b037-346">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="5b037-347">1 için kalite emri #1 (sabit değeri 1 olan ilk tamamlandı bildirimi miktarı için)</span><span class="sxs-lookup"><span data-stu-id="5b037-347">Quality order #1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="5b037-348">1 için kalite emri #2 (sabit değeri hala 1 olan kalan miktar için)</span><span class="sxs-lookup"><span data-stu-id="5b037-348">Quality order #2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="5b037-349">10 için tamamlandı olarak bildir</span><span class="sxs-lookup"><span data-stu-id="5b037-349">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="5b037-350">Kalite emri oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="5b037-350">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="5b037-351">60 için tamamlandı olarak bildir</span><span class="sxs-lookup"><span data-stu-id="5b037-351">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="5b037-352">Kalite emri oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="5b037-352">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="5b037-353">Sabit miktar: 1</span><span class="sxs-lookup"><span data-stu-id="5b037-353">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="5b037-354">Evet</span><span class="sxs-lookup"><span data-stu-id="5b037-354">Yes</span></span></td>
<td>
<p><span data-ttu-id="5b037-355">Toplu iş numarası: Evet</span><span class="sxs-lookup"><span data-stu-id="5b037-355">Batch number: Yes</span></span></p>
<p><span data-ttu-id="5b037-356">Seri numarası: Evet</span><span class="sxs-lookup"><span data-stu-id="5b037-356">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="5b037-357">Sipariş miktarı: 10</span><span class="sxs-lookup"><span data-stu-id="5b037-357">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="5b037-358">3 için tamamlandı olarak bildir: #b1, #s1 için 1; #b2, #s2 için 1 ve #b3, #s3 için 1</span><span class="sxs-lookup"><span data-stu-id="5b037-358">Report as finished for 3: 1 for #b1, #s1; 1 for #b2, #s2; and 1 for #b3, #s3</span></span>
<ul>
<li><span data-ttu-id="5b037-359">Toplu iş #b1, seri #s1'deki 1 için kalite emri #1</span><span class="sxs-lookup"><span data-stu-id="5b037-359">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="5b037-360">Toplu iş #b2, seri #s2'deki 1 için kalite emri #2</span><span class="sxs-lookup"><span data-stu-id="5b037-360">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="5b037-361">Toplu iş #b3, seri #s3'deki 1 için kalite emri #3</span><span class="sxs-lookup"><span data-stu-id="5b037-361">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="5b037-362">2 için tamamlandı olarak bildir: #b4, #s4 için 1 ve #b5, #s5 için 1</span><span class="sxs-lookup"><span data-stu-id="5b037-362">Report as finished for 2: 1 for #b4, #s4; and 1 for #b5, #s5</span></span>
<ul>
<li><span data-ttu-id="5b037-363">Toplu iş #b4, seri #s4'deki 1 için kalite emri #4</span><span class="sxs-lookup"><span data-stu-id="5b037-363">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="5b037-364">Toplu iş #b5, seri #s5'deki 1 için kalite emri #5</span><span class="sxs-lookup"><span data-stu-id="5b037-364">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="5b037-365"><strong>Not:</strong> Toplu iş yeniden kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="5b037-365"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="5b037-366">Sabit miktar: 2</span><span class="sxs-lookup"><span data-stu-id="5b037-366">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="5b037-367">Hayır</span><span class="sxs-lookup"><span data-stu-id="5b037-367">No</span></span></td>
<td>
<p><span data-ttu-id="5b037-368">Toplu iş numarası: Evet</span><span class="sxs-lookup"><span data-stu-id="5b037-368">Batch number: Yes</span></span></p>
<p><span data-ttu-id="5b037-369">Seri numarası: Evet</span><span class="sxs-lookup"><span data-stu-id="5b037-369">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="5b037-370">Sipariş miktarı: 10</span><span class="sxs-lookup"><span data-stu-id="5b037-370">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="5b037-371">4 için tamamlandı olarak bildir: #b1, #s1 için 1; #b2, #s2 için 1; #b3, #s3 için 1 ve #b4, #s4 için 1</span><span class="sxs-lookup"><span data-stu-id="5b037-371">Report as finished for 4: 1 for #b1, #s1; 1 for #b2, #s2; 1 for #b3, #s3; and 1 for #b4, #s4</span></span>
<ul>
<li><span data-ttu-id="5b037-372">Toplu iş #b1, seri #s1'deki 1 için kalite emri #1</span><span class="sxs-lookup"><span data-stu-id="5b037-372">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="5b037-373">Toplu iş #b2, seri #s2'deki 1 için kalite emri #2</span><span class="sxs-lookup"><span data-stu-id="5b037-373">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="5b037-374">Toplu iş #b3, seri #s3'deki 1 için kalite emri #3</span><span class="sxs-lookup"><span data-stu-id="5b037-374">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
<li><span data-ttu-id="5b037-375">Toplu iş #b4, seri #s4'deki 1 için kalite emri #4</span><span class="sxs-lookup"><span data-stu-id="5b037-375">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="5b037-376">Bir toplu iş ve bir seri numarasına referans olmadan, 2 için kalite emri #5.</span><span class="sxs-lookup"><span data-stu-id="5b037-376">Quality order #5 for 2, without a reference to a batch and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="5b037-377">6 için tamamlandı olarak bildir: #b5, #s5 için 1; #b6, #s6 için 1; #b7, #s7 için 1; #b8, #s8 için 1; #b9, #s9 için 1 ve #b10, #s10 için 1</span><span class="sxs-lookup"><span data-stu-id="5b037-377">Report as finished for 6: 1 for #b5, #s5; 1 for #b6, #s6; 1 for #b7, #s7; 1 for #b8, #s8; 1 for #b9, #s9; and 1 for #b10, #s10</span></span>
<ul>
<li><span data-ttu-id="5b037-378">Kalite emri oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="5b037-378">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a><span data-ttu-id="5b037-379">Kalite yönetim sayfaları</span><span class="sxs-lookup"><span data-stu-id="5b037-379">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5b037-380">Sayfa</span><span class="sxs-lookup"><span data-stu-id="5b037-380">Page</span></span></th>
<th><span data-ttu-id="5b037-381">Tanım</span><span class="sxs-lookup"><span data-stu-id="5b037-381">Description</span></span></th>
<th><span data-ttu-id="5b037-382">Örnek</span><span class="sxs-lookup"><span data-stu-id="5b037-382">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5b037-383">Kalite ilişkileri</span><span class="sxs-lookup"><span data-stu-id="5b037-383">Quality associations</span></span></td>
<td><span data-ttu-id="5b037-384">Bu makalenin önceki bölümlerine bakınız.</span><span class="sxs-lookup"><span data-stu-id="5b037-384">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="5b037-385">Bir kalite ilişkisi oluşturulan bir kalite emri için aşağıdaki tüm bilgileri tanımlar:</span><span class="sxs-lookup"><span data-stu-id="5b037-385">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="5b037-386">Hareket olayı</span><span class="sxs-lookup"><span data-stu-id="5b037-386">The transaction event</span></span></li>
<li><span data-ttu-id="5b037-387">Öğeler üzerinde gerçekleştirilmesi gereken test dizileri</span><span class="sxs-lookup"><span data-stu-id="5b037-387">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="5b037-388">Kabul edilebilir kalite düzeyi</span><span class="sxs-lookup"><span data-stu-id="5b037-388">The AQL</span></span></li>
<li><span data-ttu-id="5b037-389">Örnekleme planı</span><span class="sxs-lookup"><span data-stu-id="5b037-389">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="5b037-390">Kalite emirlerinin otomatik olarak oluşturulmasını gerektiren iş işlemindeki her farklılık için bir kalite eşleştirmesi tanımlamanız gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="5b037-390">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="5b037-391">Örneğin, satınalma siparişleri, karantina siparişleri, satış siparişleri ve üretim emirleri için iş süreçlerinde bir kalite emri oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="5b037-391">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b037-392">Testler</span><span class="sxs-lookup"><span data-stu-id="5b037-392">Tests</span></span></td>
<td><span data-ttu-id="5b037-393">Ürünlerinizin kalite belirtimlerini sağlayıp sağlamadığını belirleyen tek tek testler tanımlamak ve görüntülemek için bu sayfayı kullanın.</span><span class="sxs-lookup"><span data-stu-id="5b037-393">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="5b037-394">Bir veya daha çok bireysel testleri bir test grubuna atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5b037-394">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="5b037-395">Bu durumda, kabul edilebilir ölçüm değerleri gibi teste özgü bilgileri de belirtirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5b037-395">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="5b037-396">Ölçüm değerleri nicel testleri için kullanılır ve nitel testler için test değişkenleri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5b037-396">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="5b037-397">Nicel bir testin bir test tür <strong>tamsayı</strong> veya <strong>kesir</strong>, ve de atanmış bir ölçüsü vardır.</span><span class="sxs-lookup"><span data-stu-id="5b037-397">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="5b037-398">Kalite belirtimleri ve test sonuçları sayı olarak ifade edilir.</span><span class="sxs-lookup"><span data-stu-id="5b037-398">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="5b037-399">Kalite testi, <strong>Seçenek</strong> test tipindedir.</span><span class="sxs-lookup"><span data-stu-id="5b037-399">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="5b037-400">Kalite testleri, ölçülmekte olan değişken ve onun numaralandırılmış seçenekleri hakkında ek bilgi gerektirirler.</span><span class="sxs-lookup"><span data-stu-id="5b037-400">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="5b037-401">Kalite belirtimleri ve test sonuçları bir sonuca göre ifade edilirler.</span><span class="sxs-lookup"><span data-stu-id="5b037-401">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="5b037-402">Bir üretim şirketi satınalınan malzeme üzerinde, malzeme kalitesi hakkında bir sayısal test ile ambalaj hasarı üzerine bir kalite testi dahil olmak üzere iki test gerçekleştiriyor.</span><span class="sxs-lookup"><span data-stu-id="5b037-402">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="5b037-403">Şirket, test değişkenini (hasarlı ambalaj) ve sonuçlarını tanımlamak için ek bilgiler tanımlıyor.</span><span class="sxs-lookup"><span data-stu-id="5b037-403">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="5b037-404">Şirket <strong>Test grupları</strong> sayfasını iki testleri bir test grubuna atamak için ve teste özgü bilgileri belirtmek için kullanır.</span><span class="sxs-lookup"><span data-stu-id="5b037-404">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="5b037-405">Test grubu, şirketin iki teste ait test sonuçlarını rapor edebilmesi için bir kalite emrine atanır.</span><span class="sxs-lookup"><span data-stu-id="5b037-405">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b037-406">Test grupları</span><span class="sxs-lookup"><span data-stu-id="5b037-406">Test groups</span></span></td>
<td><span data-ttu-id="5b037-407">Test gruplarını ve test grubuna atanmış bireysel testleri ayarlamak, düzenlemek ve görüntülemek için bu sayfayı kullanın.</span><span class="sxs-lookup"><span data-stu-id="5b037-407">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="5b037-408">Üst bölme test gruplarını gösterir ve alt bölme seçili bir test grubuna atanan testleri görüntüler.</span><span class="sxs-lookup"><span data-stu-id="5b037-408">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="5b037-409">Test grubuna; örnekleme planı, kabul edilebilir kalite düzeyi ve bozucu test gereksinimi gibi birçok ilke atarsınız.</span><span class="sxs-lookup"><span data-stu-id="5b037-409">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="5b037-410">Tek bir testi bir test grubuna atadığınızda, sıra, belgeler ve geçerlilik tarihleri gibi ek bilgiler tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="5b037-410">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="5b037-411">Nicel bir test için tanımladığınız bilgilere kabul edilebilir ölçüm değerleri de dahildir.</span><span class="sxs-lookup"><span data-stu-id="5b037-411">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="5b037-412">Nitel bir test için bu bilgilere test değişkeni ve varsayılan sonuç dahildir.</span><span class="sxs-lookup"><span data-stu-id="5b037-412">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="5b037-413">Bir kalite emrine atanan test grubu, belirtilen öğe üzerinde gerçekleştirilmesi gereken testlerin varsayılan kümesini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="5b037-413">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="5b037-414">Bununla birlikte, kalite emrindeki testleri değiştirebilirsiniz, ekleyebilir veya silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5b037-414">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="5b037-415">Test sonuçları, kalite emrindeki her test için rapor edilir.</span><span class="sxs-lookup"><span data-stu-id="5b037-415">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="5b037-416">Bir üretim şirketi, kalite yönergelerindeki her sapma için bir test grubu tanımlıyor.</span><span class="sxs-lookup"><span data-stu-id="5b037-416">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="5b037-417">Çeşitli test grupları, örnekleme planları arasındaki farklılıkları, birlikte gerçekleştirilmesi gereken testler kümesini, kabul edilebilir kalite düzeyini ve diğer etkenleri yansıtır.</span><span class="sxs-lookup"><span data-stu-id="5b037-417">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="5b037-418">Nicel testleri için, kabul edilebilir ölçüm değerleri için de farklılıklar vardır.</span><span class="sxs-lookup"><span data-stu-id="5b037-418">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="5b037-419">Şirket, kalite kurallarını uygulayabilmek için kalite emirlerini otomatik oluşturabilmek için her kurala bir test grubunu <strong>Kalite ilişkilendirmeleri</strong> sayfasından atar ve ayrıca el ile oluşturulan kalite emirlerine de bir test grubu atar.</span><span class="sxs-lookup"><span data-stu-id="5b037-419">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b037-420">Madde kalite grupları</span><span class="sxs-lookup"><span data-stu-id="5b037-420">Item quality groups</span></span></td>
<td><span data-ttu-id="5b037-421">Bir kalite grubuna atanmış maddeleri veya bir maddeye atanmış kalite gruplarını ayarlamak, düzenlemek ve görüntülemek için bu sayfayı kullanın.</span><span class="sxs-lookup"><span data-stu-id="5b037-421">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="5b037-422">Kalite grubu, maddeler için ortak test gereksinimlerini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="5b037-422">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="5b037-423"><strong>Test grupları</strong> sayfasındaki test gereksinimlerini tanımladıktan sonra, kalite emirlerini otomatik olarak oluşturmak için kurallar tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5b037-423">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="5b037-424">İşlemi basitleştirmek için, kuralları her bir öğe için tanımlamanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="5b037-424">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="5b037-425">Bunun yerine, <strong>Kalite ilişkileri</strong> sayfasını kullanarak bir kalite grubu için kurallar tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="5b037-425">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="5b037-426">Ayrıca <strong>Madde kalite grupları</strong> sayfasını kullanarak belirlenmiş bir kalite grubuna ilgili maddeleri atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5b037-426">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="5b037-427">Ayrıca <strong>Madde kalite grupları</strong> sayfasını kullanarak belirlenmiş bir maddeye bir kalite grubuna ilgili maddeye atabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5b037-427">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="5b037-428">Üretim şirketi, gelen denetim için aynı test gereksinimlerine sahip çeşitli hammaddeler satın alıyor.</span><span class="sxs-lookup"><span data-stu-id="5b037-428">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="5b037-429">Şirket bir kalite grubu tanımlar ve artından hammaddeler ile ilişkilendirilmiş olan madde numaralarını bu gruba atar.</span><span class="sxs-lookup"><span data-stu-id="5b037-429">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="5b037-430">Daha sonra aynı sınama gereksinimleri olan yeni bir hammadde türü şirket tarafından satın alınır.</span><span class="sxs-lookup"><span data-stu-id="5b037-430">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="5b037-431">Yeni malzeme için yeni test gereksinimleri ayarlamak yerine, şirket yeni malzeme için madde numarasını mevcut kalite grubuna ekler.</span><span class="sxs-lookup"><span data-stu-id="5b037-431">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="5b037-432">Aynı üretim şirketi, aynı üretim testi gereksinimlerine sahip maddeler de üretiyor ve ön sevkiyat testleri için aynı gereksinimlere sahip maddeleri sevk ediyor.</span><span class="sxs-lookup"><span data-stu-id="5b037-432">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="5b037-433">Şirket iki ek kalite grubu tanımlıyor ve sonra her gruba ilgili madde numaralarını atıyor.</span><span class="sxs-lookup"><span data-stu-id="5b037-433">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b037-434">Test değişkenleri</span><span class="sxs-lookup"><span data-stu-id="5b037-434">Test variables</span></span></td>
<td><span data-ttu-id="5b037-435">Nitel bir test ile ilişkili değişkenleri görüntülemek ve tanımlamak için bu sayfayı kullanın.</span><span class="sxs-lookup"><span data-stu-id="5b037-435">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="5b037-436">Her değişken için olası sonuçları gösteren numaralandırılmış seçenekleri tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="5b037-436">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="5b037-437">Testleri tanımlamak için <strong>Testler</strong> sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="5b037-437">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="5b037-438">Nitel testler için test türünü <strong>Seçenek</strong> olarak ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="5b037-438">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="5b037-439"><strong>Test grupları</strong> sayfasını kullanarak bir teste bir test değişkeni atayın.</span><span class="sxs-lookup"><span data-stu-id="5b037-439">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="5b037-440">Kurabiye üreten bir üretim şirketi, tamamlanan ürüne yönelik bir denetim testi uyguluyor.</span><span class="sxs-lookup"><span data-stu-id="5b037-440">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="5b037-441">Bu inceleme testinin birçok değişkeni vardır.</span><span class="sxs-lookup"><span data-stu-id="5b037-441">This inspection test has several variables.</span></span> <span data-ttu-id="5b037-442">Bir değişken lezzettir ve bu değişkenin olası sonuçları iyi veya kötü olabilir.</span><span class="sxs-lookup"><span data-stu-id="5b037-442">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="5b037-443">İkinci bir değişken, çok koyu, çok açık ve doğru sonuçları ile temsil edilen renk değişkeni oluyor.</span><span class="sxs-lookup"><span data-stu-id="5b037-443">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b037-444">Test değişkeni sonuçları</span><span class="sxs-lookup"><span data-stu-id="5b037-444">Test variable outcomes</span></span></td>
<td><span data-ttu-id="5b037-445">Bir kalite testiyle ilişkili bir test değişkenine ait olası test sonuçlarını ayarlamak, düzenlemek ve görüntülemek için bu sayfayı kullanın.</span><span class="sxs-lookup"><span data-stu-id="5b037-445">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="5b037-446">Her sonuç için bir <strong>geçti</strong> veya <strong>başarısız</strong> oldu durumu atarsınız.</span><span class="sxs-lookup"><span data-stu-id="5b037-446">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="5b037-447"><strong>Testler</strong> sayfasında tanımlanan her nitel test için bir değişken ve sonuçlarını tanımlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="5b037-447">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="5b037-448">(Kalite testleri için, test türü <strong>Testler</strong> sayfasında <strong>Seçenek</strong> olarak ayarlanmıştır.) <strong>Test grupları</strong> sayfasını kullanıp, bir test değişkenini ve varsayılan sonucu bir kişisel kalite testine atayın.</span><span class="sxs-lookup"><span data-stu-id="5b037-448">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="5b037-449">Kurabiye üreten bir üretim şirketi, tamamlanan ürüne yönelik bir denetim testi uyguluyor.</span><span class="sxs-lookup"><span data-stu-id="5b037-449">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="5b037-450">Bu inceleme testinin birçok değişkeni vardır.</span><span class="sxs-lookup"><span data-stu-id="5b037-450">This inspection test has of several variables.</span></span> <span data-ttu-id="5b037-451">Bir değişken lezzettir ve bu değişkenin olası sonuçları iyi veya kötü olabilir.</span><span class="sxs-lookup"><span data-stu-id="5b037-451">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="5b037-452">İkinci bir değişken, çok koyu, çok açık ve doğru sonuçları ile temsil edilen renk değişkeni oluyor.</span><span class="sxs-lookup"><span data-stu-id="5b037-452">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="5b037-453">Her sonuca <strong>geçti</strong> veya <strong>kaldı</strong> durumu atanır.</span><span class="sxs-lookup"><span data-stu-id="5b037-453">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="5b037-454">Her değişkene yönelik denetim testi sırasında, denetçi sonuçlardan birini seçerek test sonucunu rapor ediyor.</span><span class="sxs-lookup"><span data-stu-id="5b037-454">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="5b037-455">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="5b037-455">Additional resources</span></span>
--------

[<span data-ttu-id="5b037-456">Kalite yönetimi işlemleri</span><span class="sxs-lookup"><span data-stu-id="5b037-456">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="5b037-457">Uygunsuzluk yönetimi</span><span class="sxs-lookup"><span data-stu-id="5b037-457">Nonconformance management</span></span>](enable-nonconformance-management.md)
