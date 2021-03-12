---
title: Kalite yönetimine genel bakış
description: Bu koun, tedarik zincirinizde ürün kalitesini artırmak için Dynamics 365 Supply Chain Management'teki kalite yönetimini nasıl kullanabileceğiniz açıklar.
author: perlynne
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 711ce21d0e522a737e6307e7de1889c8badd5ce0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005239"
---
# <a name="quality-management-overview"></a><span data-ttu-id="5186c-103">Kalite yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="5186c-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5186c-104">Bu koun, tedarik zincirinizde ürün kalitesini artırmak için Dynamics 365 Supply Chain Management'teki kalite yönetimini nasıl kullanabileceğiniz açıklar.</span><span class="sxs-lookup"><span data-stu-id="5186c-104">This topic describes how you can use quality management in Dynamics 365 Supply Chain Management to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="5186c-105">Kalite Yönetimi, uyumsuz ürünler,, kendi başlangıç noktalarını dikkate almadan işleyecek döngü sürelerini yönetmenize yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="5186c-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="5186c-106">Tanı türleri düzeltme raporlaması ile bağlantılı olduğundan, Supply Chain Management sorunları düzeltmek ve oluşmalarını önlemek için görevleri zamanlayabilir.</span><span class="sxs-lookup"><span data-stu-id="5186c-106">Because diagnostic types are linked to correction reporting, Supply Chain Management can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="5186c-107">Uygunsuzluğu yönetmek için daha fazla işlevselliğe ek olarak, Kalite Yönetimi sorun türüne göre sorunları (hatta iç sorunları) izlemek için ve çözümleri kısa vadeli veya uzun vadeli olarak tanımlamak için işlev içerir.</span><span class="sxs-lookup"><span data-stu-id="5186c-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="5186c-108">Anahtar performans göstergeleri (APG) ile ilgili istatistikler, önceki uygunsuzluk sorunlarının geçmişi ve bunları düzeltmek için kullanılan çözümler hakkında bir anlayış sağlar.</span><span class="sxs-lookup"><span data-stu-id="5186c-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="5186c-109">Önceki kalite ölçülerinin geçmişteki etkilerini incelemek ve ileride kullanılmaya uygun önlemleri belirlemek için geçmişe dönük verileri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5186c-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="5186c-110">Bir kalite ilişkisi ayarladığınızda, Supply Chain Management çeşitli iş süreçleri, olaylar ve koşullar için kalite emirleri oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="5186c-110">When you set up a quality association, Supply Chain Management can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="5186c-111">Kalite ilişkisi, belirli bir madde, belirli bir madde grubu veya tüm öğeleri kapsayabilir.</span><span class="sxs-lookup"><span data-stu-id="5186c-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="5186c-112">Kalite yönetimi kullanımına örnekler</span><span class="sxs-lookup"><span data-stu-id="5186c-112">Examples of the use of quality management</span></span>
<span data-ttu-id="5186c-113">Kalite Yönetimi esnektir ve tedarik zinciri işlemlerinin belirli düzeylerdeki gereksinimlerini karşılamak için çeşitli şekillerde uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="5186c-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="5186c-114">Aşağıdaki örneklerde, bu özelliklerin olası kullanımı gösterilmektedir:</span><span class="sxs-lookup"><span data-stu-id="5186c-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="5186c-115">Önceden tanımlanmış ölçütlere (belirli bir satıcı satınalma siparişinden, ambar kaydı) dayalı bir kalite kontrol işlemini otomatik olarak başlatın.</span><span class="sxs-lookup"><span data-stu-id="5186c-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="5186c-116">Onaylanmamış stokun kullanılmasını engellemek için inceleme sırasında stoku bloklayın(Tüm satınalma siparişi miktarlarını engelleme).</span><span class="sxs-lookup"><span data-stu-id="5186c-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="5186c-117">Madde örneklemeyi kalite ilişkilendirmesinin bir parçası olarak, denetlenmesi gereken geçerli fiziksel stok miktarını tanımlamak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="5186c-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="5186c-118">Örnekleme miktar, yüzde veya tam plaka tabanlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="5186c-118">Sampling can be based on fixed quantities, a percentage, or full license plate.</span></span>

> [!NOTE]
> <span data-ttu-id="5186c-119">_Ambar işlemleri için kalite yöntemleri_ özelliği, kalite yönetimi özelliğinin yeteneklerini genişletir.</span><span class="sxs-lookup"><span data-stu-id="5186c-119">The _Quality management for warehouse processes_ feature extends the capabilities of quality management.</span></span> <span data-ttu-id="5186c-120">Bu özelliği kullanıyorsanız, kalite yönetiminin etkinleştirildiğinde nasıl çalıştığına ilişkin örnekler için [Ambar işlemleri için kalite yönetimi](quality-management-for-warehouses-processes.md)'ne bakın.</span><span class="sxs-lookup"><span data-stu-id="5186c-120">If you are using this feature, then see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md) for examples of how quality management works when it's enabled.</span></span>

-   <span data-ttu-id="5186c-121">Kısmi alış irsaliyeleri için kalite emirleri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5186c-121">Create quality orders for partial receipts.</span></span> <span data-ttu-id="5186c-122">Bir siparişten fiziksel olarak alına miktara bağlı olarak oluşturulan bir kalite emri oluşturmak için **Madde örnekleme** formundaki **Güncelleştirilen miktar başına** onay kutusunu seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="5186c-122">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="5186c-123">Minimum, maksimum ve hedef test değerleri içeren test türleri oluşturun ve doğrulama sonuçları önceden tanımlanmış olan niteliğe karşı nicelik sınamaları gerçekleştirin.</span><span class="sxs-lookup"><span data-stu-id="5186c-123">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="5186c-124">Kalite Ölçüm toleranslarını kontrol etmek için bir kabul edilebilir kalite düzeyi (AQL) belirtin.</span><span class="sxs-lookup"><span data-stu-id="5186c-124">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="5186c-125">Denetleme işlemi için gereken test alanı ve test aletleri gibi kaynakları belirtin.</span><span class="sxs-lookup"><span data-stu-id="5186c-125">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="5186c-126">Kalite ilişkileri ile çalışmak</span><span class="sxs-lookup"><span data-stu-id="5186c-126">Working with quality associations</span></span>
<span data-ttu-id="5186c-127">Kalite ilişkisini kullanan iş süreci, satınalma siparişleri, satış siparişleri veya üretim emirleri gibi çeşitli kaynak belgelere ilişkili olabilir.</span><span class="sxs-lookup"><span data-stu-id="5186c-127">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="5186c-128">Her kalite bağlantısı kaydı oluşturulan kalite emirlerine geçerli olacak testler kümesini, AQL'yi ve örnek alma planını da tanımlamaktadır.</span><span class="sxs-lookup"><span data-stu-id="5186c-128">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="5186c-129">Bir iş sürecindeki her değişim için bir kalite ilişkisi kaydı tanımlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="5186c-129">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="5186c-130">Örneğin, bir satınalma siparişi ürün alış irsaliyesi güncelleştirildiğinde, kalite emri oluşturacak bir kalite ilişkisi ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5186c-130">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="5186c-131">Yürütme planı kurulumuna bağlı olarak, açık bir kalite emri yok ya da satınalma siparişi faturalama gibi sonraki işlemler, engellenen tetikleyici işlem engellenebilir.</span><span class="sxs-lookup"><span data-stu-id="5186c-131">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="5186c-132">**Not:** Açık kalite emirleri olduğunda, stok miktarlarının çıkarılması otomatik olarak engellenir.</span><span class="sxs-lookup"><span data-stu-id="5186c-132">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="5186c-133">**Madde örnekleri** sayfasında bulunan **Tam engelleme** ayarına bağlı olarak, miktar kalite emrindeki miktardır ya da kaynak belge satırındaki miktardır.</span><span class="sxs-lookup"><span data-stu-id="5186c-133">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="5186c-134">Bir iş süreci için, kalite ilişkisi kaydı, kalite emrinin oluşturulduğu olay ve koşulları tanımlar.</span><span class="sxs-lookup"><span data-stu-id="5186c-134">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="5186c-135">Koşullar bir siteye veya bir tüzel kişiliğe özel olabilir.</span><span class="sxs-lookup"><span data-stu-id="5186c-135">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="5186c-136">Bozucu testler içeren bir kalite emri yalnızca olay için eldeki stok bulunması durumunda oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="5186c-136">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="5186c-137">Aşağıdaki örnekler, her iş sürecindeki değişiklikler için bir kalite bağlantısını tanımlamayı açıklar.</span><span class="sxs-lookup"><span data-stu-id="5186c-137">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="5186c-138">Her örnek için, aşağıdaki tablo kalite ilişki kaydındaki olayları ve durumları özetler.</span><span class="sxs-lookup"><span data-stu-id="5186c-138">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="5186c-139">Referans türü</span><span class="sxs-lookup"><span data-stu-id="5186c-139">Reference type</span></span></th>
<th><span data-ttu-id="5186c-140">Olay türü</span><span class="sxs-lookup"><span data-stu-id="5186c-140">Event type</span></span></th>
<th><span data-ttu-id="5186c-141">Yürütme</span><span class="sxs-lookup"><span data-stu-id="5186c-141">Execution</span></span></th>
<th><span data-ttu-id="5186c-142">Olay durdurma</span><span class="sxs-lookup"><span data-stu-id="5186c-142">Event blocking</span></span></th>
<th><span data-ttu-id="5186c-143">Belge başvurusu</span><span class="sxs-lookup"><span data-stu-id="5186c-143">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="5186c-144">Stok</span><span class="sxs-lookup"><span data-stu-id="5186c-144">Inventory</span></span></td>
<td><span data-ttu-id="5186c-145">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="5186c-145">Not applicable</span></span></td>
<td><span data-ttu-id="5186c-146">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="5186c-146">Not applicable</span></span></td>
<td><span data-ttu-id="5186c-147">Yok</span><span class="sxs-lookup"><span data-stu-id="5186c-147">None</span></span></td>
<td><span data-ttu-id="5186c-148">Tümü</span><span class="sxs-lookup"><span data-stu-id="5186c-148">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="5186c-149">Satışlar</span><span class="sxs-lookup"><span data-stu-id="5186c-149">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="5186c-150">Malzeme çekme işlemi planlandı</span><span class="sxs-lookup"><span data-stu-id="5186c-150">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="5186c-151">Önce</span><span class="sxs-lookup"><span data-stu-id="5186c-151">Before</span></span></td>
<td><span data-ttu-id="5186c-152">Yok</span><span class="sxs-lookup"><span data-stu-id="5186c-152">None</span></span></td>
<td rowspan="22"><span data-ttu-id="5186c-153">Belirli Kimlik, Grup veya Yalnızca tümü</span><span class="sxs-lookup"><span data-stu-id="5186c-153">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5186c-154">Malzeme çekme işlemi</span><span class="sxs-lookup"><span data-stu-id="5186c-154">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5186c-155">Sevk irsaliyesi</span><span class="sxs-lookup"><span data-stu-id="5186c-155">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5186c-156">Fatura</span><span class="sxs-lookup"><span data-stu-id="5186c-156">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5186c-157">Sevk irsaliyesi</span><span class="sxs-lookup"><span data-stu-id="5186c-157">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="5186c-158">Önce</span><span class="sxs-lookup"><span data-stu-id="5186c-158">Before</span></span></td>
<td><span data-ttu-id="5186c-159">Yok</span><span class="sxs-lookup"><span data-stu-id="5186c-159">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5186c-160">Sevk irsaliyesi</span><span class="sxs-lookup"><span data-stu-id="5186c-160">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5186c-161">Fatura</span><span class="sxs-lookup"><span data-stu-id="5186c-161">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="5186c-162">Satınalma</span><span class="sxs-lookup"><span data-stu-id="5186c-162">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="5186c-163">Giriş listesi</span><span class="sxs-lookup"><span data-stu-id="5186c-163">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="5186c-164">Önce</span><span class="sxs-lookup"><span data-stu-id="5186c-164">Before</span></span></td>
<td><span data-ttu-id="5186c-165">Yok</span><span class="sxs-lookup"><span data-stu-id="5186c-165">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5186c-166">Giriş listesi</span><span class="sxs-lookup"><span data-stu-id="5186c-166">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5186c-167">Ürün girişi</span><span class="sxs-lookup"><span data-stu-id="5186c-167">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5186c-168">Fatura</span><span class="sxs-lookup"><span data-stu-id="5186c-168">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5186c-169">Sonra</span><span class="sxs-lookup"><span data-stu-id="5186c-169">After</span></span></td>
<td><span data-ttu-id="5186c-170">Yok</span><span class="sxs-lookup"><span data-stu-id="5186c-170">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5186c-171">Ürün girişi</span><span class="sxs-lookup"><span data-stu-id="5186c-171">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5186c-172">Fatura</span><span class="sxs-lookup"><span data-stu-id="5186c-172">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5186c-173">Kayıt</span><span class="sxs-lookup"><span data-stu-id="5186c-173">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="5186c-174">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="5186c-174">Not applicable</span></span></td>
<td><span data-ttu-id="5186c-175">Yok</span><span class="sxs-lookup"><span data-stu-id="5186c-175">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5186c-176">Ürün girişi</span><span class="sxs-lookup"><span data-stu-id="5186c-176">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5186c-177">Fatura</span><span class="sxs-lookup"><span data-stu-id="5186c-177">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="5186c-178">Ürün girişi</span><span class="sxs-lookup"><span data-stu-id="5186c-178">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="5186c-179">Önce</span><span class="sxs-lookup"><span data-stu-id="5186c-179">Before</span></span></td>
<td><span data-ttu-id="5186c-180">Yok</span><span class="sxs-lookup"><span data-stu-id="5186c-180">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5186c-181">Ürün girişi</span><span class="sxs-lookup"><span data-stu-id="5186c-181">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5186c-182">Fatura</span><span class="sxs-lookup"><span data-stu-id="5186c-182">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5186c-183">Sonra</span><span class="sxs-lookup"><span data-stu-id="5186c-183">After</span></span></td>
<td><span data-ttu-id="5186c-184">Yok</span><span class="sxs-lookup"><span data-stu-id="5186c-184">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5186c-185">Fatura</span><span class="sxs-lookup"><span data-stu-id="5186c-185">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="5186c-186">Üretim</span><span class="sxs-lookup"><span data-stu-id="5186c-186">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="5186c-187">Kayıt</span><span class="sxs-lookup"><span data-stu-id="5186c-187">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="5186c-188">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="5186c-188">Not applicable</span></span></td>
<td><span data-ttu-id="5186c-189">Yok</span><span class="sxs-lookup"><span data-stu-id="5186c-189">None</span></span></td>
<td rowspan="12"><span data-ttu-id="5186c-190">Tümü</span><span class="sxs-lookup"><span data-stu-id="5186c-190">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5186c-191">Tamamlandı bildirimi</span><span class="sxs-lookup"><span data-stu-id="5186c-191">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5186c-192">Bitir</span><span class="sxs-lookup"><span data-stu-id="5186c-192">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="5186c-193">Tamamlandı bildirimi</span><span class="sxs-lookup"><span data-stu-id="5186c-193">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="5186c-194">Önce</span><span class="sxs-lookup"><span data-stu-id="5186c-194">Before</span></span></td>
<td><span data-ttu-id="5186c-195">Yok</span><span class="sxs-lookup"><span data-stu-id="5186c-195">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5186c-196">Tamamlandı bildirimi</span><span class="sxs-lookup"><span data-stu-id="5186c-196">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5186c-197">Bitir</span><span class="sxs-lookup"><span data-stu-id="5186c-197">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5186c-198">Sonra</span><span class="sxs-lookup"><span data-stu-id="5186c-198">After</span></span></td>
<td><span data-ttu-id="5186c-199">Yok</span><span class="sxs-lookup"><span data-stu-id="5186c-199">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5186c-200">Bitir</span><span class="sxs-lookup"><span data-stu-id="5186c-200">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="5186c-201">Karantina</span><span class="sxs-lookup"><span data-stu-id="5186c-201">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="5186c-202">Tamamlandı bildirimi</span><span class="sxs-lookup"><span data-stu-id="5186c-202">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="5186c-203">Önce</span><span class="sxs-lookup"><span data-stu-id="5186c-203">Before</span></span></td>
<td><span data-ttu-id="5186c-204">Tamamlandı bildirimi</span><span class="sxs-lookup"><span data-stu-id="5186c-204">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5186c-205">Bitir</span><span class="sxs-lookup"><span data-stu-id="5186c-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5186c-206">Sonra</span><span class="sxs-lookup"><span data-stu-id="5186c-206">After</span></span></td>
<td><span data-ttu-id="5186c-207">Bitir</span><span class="sxs-lookup"><span data-stu-id="5186c-207">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5186c-208">Bitir</span><span class="sxs-lookup"><span data-stu-id="5186c-208">End</span></span></td>
<td><span data-ttu-id="5186c-209">Önce</span><span class="sxs-lookup"><span data-stu-id="5186c-209">Before</span></span></td>
<td><span data-ttu-id="5186c-210">Bitir</span><span class="sxs-lookup"><span data-stu-id="5186c-210">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5186c-211">Rota operasyonu</span><span class="sxs-lookup"><span data-stu-id="5186c-211">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="5186c-212">Tamamlandı bildirimi</span><span class="sxs-lookup"><span data-stu-id="5186c-212">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="5186c-213">Önce</span><span class="sxs-lookup"><span data-stu-id="5186c-213">Before</span></span></td>
<td><span data-ttu-id="5186c-214">Yok</span><span class="sxs-lookup"><span data-stu-id="5186c-214">None</span></span></td>
<td rowspan="3"><span data-ttu-id="5186c-215">Belirli Kimlik, Grup veya Tümü ve Kaynağa özel, Grup veya Tümü</span><span class="sxs-lookup"><span data-stu-id="5186c-215">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5186c-216">Tamamlandı bildirimi</span><span class="sxs-lookup"><span data-stu-id="5186c-216">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5186c-217">Sonra</span><span class="sxs-lookup"><span data-stu-id="5186c-217">After</span></span></td>
<td><span data-ttu-id="5186c-218">Yok</span><span class="sxs-lookup"><span data-stu-id="5186c-218">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5186c-219">Ortak ürün üretimi</span><span class="sxs-lookup"><span data-stu-id="5186c-219">Co-product production</span></span></td>
<td><span data-ttu-id="5186c-220">Kayıt</span><span class="sxs-lookup"><span data-stu-id="5186c-220">Registration</span></span></td>
<td><span data-ttu-id="5186c-221">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="5186c-221">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5186c-222">Yok</span><span class="sxs-lookup"><span data-stu-id="5186c-222">None</span></span></td>
<td rowspan="3"><span data-ttu-id="5186c-223">Tümü</span><span class="sxs-lookup"><span data-stu-id="5186c-223">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5186c-224">Tamamlandı bildirimi</span><span class="sxs-lookup"><span data-stu-id="5186c-224">Report as finished</span></span></td>
<td><span data-ttu-id="5186c-225">Önce</span><span class="sxs-lookup"><span data-stu-id="5186c-225">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5186c-226">Sonra</span><span class="sxs-lookup"><span data-stu-id="5186c-226">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5186c-227">Aşağıdaki tabloda belirli türde işlemler için kalite emirlerinin nasıl oluşturulabileceği hakkında daha fazla bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="5186c-227">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="5186c-228">İşleme türü</span><span class="sxs-lookup"><span data-stu-id="5186c-228">Type of process</span></span></th>
<th><span data-ttu-id="5186c-229">Kalite emirlerinin ne zaman otomatik olarak oluşturulabileceği</span><span class="sxs-lookup"><span data-stu-id="5186c-229">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="5186c-230">Bozucu sınama yapılması gerekirse kalite emirlerinin ne zaman oluşturulabileceği</span><span class="sxs-lookup"><span data-stu-id="5186c-230">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="5186c-231">Koşul bilgisi</span><span class="sxs-lookup"><span data-stu-id="5186c-231">Condition information</span></span></th>
<th><span data-ttu-id="5186c-232">El ile oluşturma bilgisi</span><span class="sxs-lookup"><span data-stu-id="5186c-232">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="5186c-233">Satın alma siparişi</span><span class="sxs-lookup"><span data-stu-id="5186c-233">Purchase order</span></span></td>
<td><span data-ttu-id="5186c-234">Alınan malzeme için ürün girişi ya da giriş listesi nakledildikten önce veya sonra.</span><span class="sxs-lookup"><span data-stu-id="5186c-234">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="5186c-235">Alınan malzeme için ürün girişi nakledildikten sonra, çünkü malzemenin bozucu test için mevcut olması gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="5186c-235">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="5186c-236">Kalite emri gereksinimi özel bir tesisi, maddeyi veya satıcıyı ya da bunların bir birleşimini yansıtabilir.</span><span class="sxs-lookup"><span data-stu-id="5186c-236">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="5186c-237">Bir satınalma siparişine gönderme yapan ve el ile oluşturulmuş bir kalite emri, tasarlanmış örnek alma planı gibi, bir kalite bağlantısı kaydında bulunan bilgileri kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="5186c-237">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5186c-238">Karantina emri</span><span class="sxs-lookup"><span data-stu-id="5186c-238">Quarantine order</span></span></td>
<td><span data-ttu-id="5186c-239">Karantina siparişi tamamlandı veya sona erdi olarak bildirildikten önce veya sonra.</span><span class="sxs-lookup"><span data-stu-id="5186c-239">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="5186c-240">Yıkıcı testler gerektiren kalite emirleri oluşturulamaz.</span><span class="sxs-lookup"><span data-stu-id="5186c-240">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="5186c-241">Karantina siparişi işlevinin, yok edilen malzemenin değerlendirmesini üstleneceği kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="5186c-241">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="5186c-242">Kalite emri gereksinimi özel bir tesisi, maddeyi veya satıcıyı ya da bunların bir birleşimini yansıtabilir.</span><span class="sxs-lookup"><span data-stu-id="5186c-242">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="5186c-243">Bir karantina siparişine gönderme yapan ve el ile oluşturulmuş bir kalite emri, tasarlanmış örnek alma planı gibi, bir kalite bağlantısı kaydında bulunan bilgileri kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="5186c-243">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5186c-244">Satış siparişi</span><span class="sxs-lookup"><span data-stu-id="5186c-244">Sales order</span></span></td>
<td><span data-ttu-id="5186c-245">Bir zamanlanmış malzeme çekme işlem veya sevk irsaliyesi güncelleştirmesi sevk maddeler için önce</span><span class="sxs-lookup"><span data-stu-id="5186c-245">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="5186c-246">Herhangi bir adımda</span><span class="sxs-lookup"><span data-stu-id="5186c-246">At any step</span></span></td>
<td><span data-ttu-id="5186c-247">Kalite emri gereksinimi özel bir tesisi, maddeyi veya satıcıyı ya da bunların bir birleşimini yansıtabilir.</span><span class="sxs-lookup"><span data-stu-id="5186c-247">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="5186c-248">Bir satış siparişine gönderme yapan ve el ile oluşturulmuş bir kalite emri, tasarlanmış örnek alma planı gibi, bir kalite bağlantısı kaydında bulunan bilgileri kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="5186c-248">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5186c-249">Üretim emri</span><span class="sxs-lookup"><span data-stu-id="5186c-249">Production order</span></span></td>
<td><span data-ttu-id="5186c-250">Üretim emri için bitmiş miktar rapor edildikten önce veya sonra</span><span class="sxs-lookup"><span data-stu-id="5186c-250">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="5186c-251">Üretim emri için bitmiş miktar rapor edildikten sonra</span><span class="sxs-lookup"><span data-stu-id="5186c-251">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="5186c-252">Kalite emri gereksinimi özel bir tesisi, maddeyi veya satıcıyı ya da bunların bir birleşimini yansıtabilir.</span><span class="sxs-lookup"><span data-stu-id="5186c-252">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="5186c-253">Bir üretim emrine gönderme yapan ve el ile oluşturulmuş bir kalite emri, tasarlanmış örnek alma planı gibi, bir kalite bağlantısı kaydında bulunan bilgileri kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="5186c-253">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5186c-254">Bir rota operasyonuna sahip olan üretim emri</span><span class="sxs-lookup"><span data-stu-id="5186c-254">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="5186c-255">Bir operasyon için bir rapor sona erdikten önce veya sonra</span><span class="sxs-lookup"><span data-stu-id="5186c-255">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="5186c-256">Son operasyon için raporlama üretimi bittikten sonra.</span><span class="sxs-lookup"><span data-stu-id="5186c-256">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="5186c-257">Kalite emri gereksinimi özel bir tesisi, maddeyi veya operasyon kaynağı ya da bunların bir birleşimini yansıtabilir.</span><span class="sxs-lookup"><span data-stu-id="5186c-257">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="5186c-258">Bir rota operasyonu gönderme yapan ve el ile oluşturulmuş bir kalite emri, tasarlanmış örnek alma planı gibi, bir kalite bağlantısı kaydında bulunan bilgileri kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="5186c-258">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5186c-259">Stok</span><span class="sxs-lookup"><span data-stu-id="5186c-259">Inventory</span></span></td>
<td><span data-ttu-id="5186c-260">Bir kalite emri, transfer emri hareketleri veya bir stok günlüğünde bir hareket için otomatik olarak oluşturulamaz.</span><span class="sxs-lookup"><span data-stu-id="5186c-260">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="5186c-261">Bir kalite emrinin bir maddenin stok miktarı için el ile oluşturulması gerekir.</span><span class="sxs-lookup"><span data-stu-id="5186c-261">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="5186c-262">Fiziksel eldeki stok gereklidir.</span><span class="sxs-lookup"><span data-stu-id="5186c-262">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-order-auto-generation-examples"></a><span data-ttu-id="5186c-263">Kalite emri otomatik oluşturma örnekleri</span><span class="sxs-lookup"><span data-stu-id="5186c-263">Quality order auto-generation examples</span></span>

### <a name="purchasing"></a><span data-ttu-id="5186c-264">Satınalma</span><span class="sxs-lookup"><span data-stu-id="5186c-264">Purchasing</span></span>

<span data-ttu-id="5186c-265">Satınalmada, **Kalite ilişkilendirmeleri** sayfasında **Olay türü** alanını **Ürün girişi** ve **Yürütme** alanını **Sonra** olarak ayarlarsanız aşağıdaki sonuçları elde edersiniz:</span><span class="sxs-lookup"><span data-stu-id="5186c-265">In purchasing, if you set the **Event type** field to **Product receipt** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span> 

- <span data-ttu-id="5186c-266">**Güncelleştirilen miktar başına** seçeneği **Evet** olarak ayarlanmışsa, madde örneklemesindeki teslim alınan miktar ve ayarlar temel alınarak satınalma siparişiyle ilgili her giriş için bir kalite emri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5186c-266">If the **Per updated quantity** option is set to **Yes**, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="5186c-267">Satınalma siparişine göre bir miktar her teslim alındığında, yeni teslim alınan miktar temel alınarak geçerli kalite emirleri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5186c-267">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="5186c-268">**Güncelleştirilen miktar başına** seçeneği **Hayır** olarak ayarlanmışsa, teslim alınan miktar ve ayarlar temel alınarak satınalma siparişiyle ilgili ilk giriş için bir kalite emri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5186c-268">If the **Per updated quantity** option is set to **No**, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="5186c-269">Ayrıca, izleme boyutlarına bağlı olarak kalan miktar temel alınarak bir veya daha fazla kalite emri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5186c-269">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="5186c-270">Satınalma siparişiyle ilgili sonraki girişler için kalite emirleri oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="5186c-270">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="5186c-271">Üretim</span><span class="sxs-lookup"><span data-stu-id="5186c-271">Production</span></span>

<span data-ttu-id="5186c-272">Üretimde, **Kalite ilişkilendirmeleri** sayfasında **Olay türü** alanını **Tamamlandı olarak bildir** ve **Yürütme** alanını **Sonra** olarak ayarlarsanız aşağıdaki sonuçları elde edersiniz:</span><span class="sxs-lookup"><span data-stu-id="5186c-272">In production, if you set the **Event type** field to **Report as finished** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="5186c-273">**Güncelleştirilen miktar başına** seçeneği **Evet** olarak ayarlanmışsa, madde örneklemesindeki her tamamlanan miktar için bir kalite emri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5186c-273">If the **Per updated quantity** option is set to **Yes**, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="5186c-274">Üretim emrine göre bir miktar her tamamlandı olarak bildirildiğinde, yeni tamamlanan miktar temel alınarak geçerli kalite emirleri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5186c-274">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on newly finished quantity.</span></span> <span data-ttu-id="5186c-275">Bu oluşturma mantığı satın alma ile tutarlıdır.</span><span class="sxs-lookup"><span data-stu-id="5186c-275">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="5186c-276">**Güncelleştirilen miktar başına** seçeneği **Hayır** olarak ayarlanmışsa, tamamlanan miktar temel alınarak bir miktar ilk kez tamamlandı olarak bildirildiğinde bir kalite emri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5186c-276">If the **Per updated quantity** option is set to **No**, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="5186c-277">Ayrıca, madde örneklemesinin izleme boyutlarına bağlı olarak kalan miktar temel alınarak bir veya daha fazla kalite emri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5186c-277">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="5186c-278">Sonraki tamamlanan miktarlar için kalite emirleri oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="5186c-278">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="5186c-279">Kalite belirtimi</span><span class="sxs-lookup"><span data-stu-id="5186c-279">Quality specification</span></span></th>
<th><span data-ttu-id="5186c-280">Güncelleştirilen miktar başına</span><span class="sxs-lookup"><span data-stu-id="5186c-280">Per updated quantity</span></span></th>
<th><span data-ttu-id="5186c-281">İzleme boyutu başına</span><span class="sxs-lookup"><span data-stu-id="5186c-281">Per tracking dimension</span></span></th>
<th><span data-ttu-id="5186c-282">Sonuç</span><span class="sxs-lookup"><span data-stu-id="5186c-282">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="5186c-283">Yüzde: %10</span><span class="sxs-lookup"><span data-stu-id="5186c-283">Percentage: 10%</span></span></td>
<td><span data-ttu-id="5186c-284">Evet</span><span class="sxs-lookup"><span data-stu-id="5186c-284">Yes</span></span></td>
<td>
<p><span data-ttu-id="5186c-285">Toplu iş numarası: Hayır</span><span class="sxs-lookup"><span data-stu-id="5186c-285">Batch number: No</span></span></p>
<p><span data-ttu-id="5186c-286">Seri numarası: Hayır</span><span class="sxs-lookup"><span data-stu-id="5186c-286">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="5186c-287">Sipariş miktarı: 100</span><span class="sxs-lookup"><span data-stu-id="5186c-287">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="5186c-288">30 için tamamlandı olarak bildir</span><span class="sxs-lookup"><span data-stu-id="5186c-288">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="5186c-289">3 için (30'un %10'u) için kalite emri #1</span><span class="sxs-lookup"><span data-stu-id="5186c-289">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="5186c-290">70 için tamamlandı olarak bildir</span><span class="sxs-lookup"><span data-stu-id="5186c-290">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="5186c-291">7 (kalan sipariş miktarının %10'u; bu durumda 70'e eşittir) için kalite emri #2</span><span class="sxs-lookup"><span data-stu-id="5186c-291">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="5186c-292">Sabit miktar: 1</span><span class="sxs-lookup"><span data-stu-id="5186c-292">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="5186c-293">Hayır</span><span class="sxs-lookup"><span data-stu-id="5186c-293">No</span></span></td>
<td>
<p><span data-ttu-id="5186c-294">Toplu iş numarası: Hayır</span><span class="sxs-lookup"><span data-stu-id="5186c-294">Batch number: No</span></span></p>
<p><span data-ttu-id="5186c-295">Seri numarası: Hayır</span><span class="sxs-lookup"><span data-stu-id="5186c-295">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="5186c-296">Sipariş miktarı: 100</span><span class="sxs-lookup"><span data-stu-id="5186c-296">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="5186c-297">30 için tamamlandı olarak bildir</span><span class="sxs-lookup"><span data-stu-id="5186c-297">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="5186c-298">1 için kalite emri #1 (sabit değeri 1 olan ilk tamamlandı bildirimi miktarı için)</span><span class="sxs-lookup"><span data-stu-id="5186c-298">Quality order #1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="5186c-299">1 için kalite emri #2 (sabit değeri hala 1 olan kalan miktar için)</span><span class="sxs-lookup"><span data-stu-id="5186c-299">Quality order #2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="5186c-300">10 için tamamlandı olarak bildir</span><span class="sxs-lookup"><span data-stu-id="5186c-300">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="5186c-301">Kalite emri oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="5186c-301">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="5186c-302">60 için tamamlandı olarak bildir</span><span class="sxs-lookup"><span data-stu-id="5186c-302">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="5186c-303">Kalite emri oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="5186c-303">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="5186c-304">Sabit miktar: 1</span><span class="sxs-lookup"><span data-stu-id="5186c-304">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="5186c-305">Evet</span><span class="sxs-lookup"><span data-stu-id="5186c-305">Yes</span></span></td>
<td>
<p><span data-ttu-id="5186c-306">Toplu iş numarası: Evet</span><span class="sxs-lookup"><span data-stu-id="5186c-306">Batch number: Yes</span></span></p>
<p><span data-ttu-id="5186c-307">Seri numarası: Evet</span><span class="sxs-lookup"><span data-stu-id="5186c-307">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="5186c-308">Sipariş miktarı: 10</span><span class="sxs-lookup"><span data-stu-id="5186c-308">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="5186c-309">3 için tamamlandı olarak bildir: #b1, #s1 için 1; #b2, #s2 için 1 ve #b3, #s3 için 1</span><span class="sxs-lookup"><span data-stu-id="5186c-309">Report as finished for 3: 1 for #b1, #s1; 1 for #b2, #s2; and 1 for #b3, #s3</span></span>
<ul>
<li><span data-ttu-id="5186c-310">Toplu iş #b1, seri #s1'deki 1 için kalite emri #1</span><span class="sxs-lookup"><span data-stu-id="5186c-310">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="5186c-311">Toplu iş #b2, seri #s2'deki 1 için kalite emri #2</span><span class="sxs-lookup"><span data-stu-id="5186c-311">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="5186c-312">Toplu iş #b3, seri #s3'deki 1 için kalite emri #3</span><span class="sxs-lookup"><span data-stu-id="5186c-312">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="5186c-313">2 için tamamlandı olarak bildir: #b4, #s4 için 1 ve #b5, #s5 için 1</span><span class="sxs-lookup"><span data-stu-id="5186c-313">Report as finished for 2: 1 for #b4, #s4; and 1 for #b5, #s5</span></span>
<ul>
<li><span data-ttu-id="5186c-314">Toplu iş #b4, seri #s4'deki 1 için kalite emri #4</span><span class="sxs-lookup"><span data-stu-id="5186c-314">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="5186c-315">Toplu iş #b5, seri #s5'deki 1 için kalite emri #5</span><span class="sxs-lookup"><span data-stu-id="5186c-315">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="5186c-316"><strong>Not:</strong> Toplu iş yeniden kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="5186c-316"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="5186c-317">Sabit miktar: 2</span><span class="sxs-lookup"><span data-stu-id="5186c-317">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="5186c-318">Hayır</span><span class="sxs-lookup"><span data-stu-id="5186c-318">No</span></span></td>
<td>
<p><span data-ttu-id="5186c-319">Toplu iş numarası: Evet</span><span class="sxs-lookup"><span data-stu-id="5186c-319">Batch number: Yes</span></span></p>
<p><span data-ttu-id="5186c-320">Seri numarası: Evet</span><span class="sxs-lookup"><span data-stu-id="5186c-320">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="5186c-321">Sipariş miktarı: 10</span><span class="sxs-lookup"><span data-stu-id="5186c-321">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="5186c-322">4 için tamamlandı olarak bildir: #b1, #s1 için 1; #b2, #s2 için 1; #b3, #s3 için 1 ve #b4, #s4 için 1</span><span class="sxs-lookup"><span data-stu-id="5186c-322">Report as finished for 4: 1 for #b1, #s1; 1 for #b2, #s2; 1 for #b3, #s3; and 1 for #b4, #s4</span></span>
<ul>
<li><span data-ttu-id="5186c-323">Toplu iş #b1, seri #s1'deki 1 için kalite emri #1</span><span class="sxs-lookup"><span data-stu-id="5186c-323">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="5186c-324">Toplu iş #b2, seri #s2'deki 1 için kalite emri #2</span><span class="sxs-lookup"><span data-stu-id="5186c-324">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="5186c-325">Toplu iş #b3, seri #s3'deki 1 için kalite emri #3</span><span class="sxs-lookup"><span data-stu-id="5186c-325">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
<li><span data-ttu-id="5186c-326">Toplu iş #b4, seri #s4'deki 1 için kalite emri #4</span><span class="sxs-lookup"><span data-stu-id="5186c-326">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="5186c-327">Bir toplu iş ve bir seri numarasına referans olmadan, 2 için kalite emri #5.</span><span class="sxs-lookup"><span data-stu-id="5186c-327">Quality order #5 for 2, without a reference to a batch and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="5186c-328">6 için tamamlandı olarak bildir: #b5, #s5 için 1; #b6, #s6 için 1; #b7, #s7 için 1; #b8, #s8 için 1; #b9, #s9 için 1 ve #b10, #s10 için 1</span><span class="sxs-lookup"><span data-stu-id="5186c-328">Report as finished for 6: 1 for #b5, #s5; 1 for #b6, #s6; 1 for #b7, #s7; 1 for #b8, #s8; 1 for #b9, #s9; and 1 for #b10, #s10</span></span>
<ul>
<li><span data-ttu-id="5186c-329">Kalite emri oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="5186c-329">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="5186c-330">*Ambar işlemleri için kalite yönetimi* özelliği, **Olay Türü** *Tamamlandı olarak bildir*, **Yürütme** *Sonra* olarak ayarlanmış olan üretim ve **Olay türü** *Kayıt* olarak ayarlanmış satınalmalar için kalite emri işleme yetenekleri ekler.</span><span class="sxs-lookup"><span data-stu-id="5186c-330">The *Quality management for warehouse processes* feature adds capabilities for quality order processing for production with **Event type** set to *Report as finished* and **Execution** set to *After*, and for purchases with **Event type** set to *Registration*.</span></span> <span data-ttu-id="5186c-331">Ayrıntılar için bkz. [Ambar işlemleri için kalite yönetimi](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="5186c-331">For details, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

## <a name="quality-management-pages"></a><span data-ttu-id="5186c-332">Kalite yönetim sayfaları</span><span class="sxs-lookup"><span data-stu-id="5186c-332">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5186c-333">Sayfa</span><span class="sxs-lookup"><span data-stu-id="5186c-333">Page</span></span></th>
<th><span data-ttu-id="5186c-334">Tanım</span><span class="sxs-lookup"><span data-stu-id="5186c-334">Description</span></span></th>
<th><span data-ttu-id="5186c-335">Örnek</span><span class="sxs-lookup"><span data-stu-id="5186c-335">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5186c-336">Kalite ilişkileri</span><span class="sxs-lookup"><span data-stu-id="5186c-336">Quality associations</span></span></td>
<td><span data-ttu-id="5186c-337">Bu makalenin önceki bölümlerine bakınız.</span><span class="sxs-lookup"><span data-stu-id="5186c-337">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="5186c-338">Bir kalite ilişkisi oluşturulan bir kalite emri için aşağıdaki tüm bilgileri tanımlar:</span><span class="sxs-lookup"><span data-stu-id="5186c-338">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="5186c-339">Hareket olayı</span><span class="sxs-lookup"><span data-stu-id="5186c-339">The transaction event</span></span></li>
<li><span data-ttu-id="5186c-340">Öğeler üzerinde gerçekleştirilmesi gereken test dizileri</span><span class="sxs-lookup"><span data-stu-id="5186c-340">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="5186c-341">Kabul edilebilir kalite düzeyi</span><span class="sxs-lookup"><span data-stu-id="5186c-341">The AQL</span></span></li>
<li><span data-ttu-id="5186c-342">Örnekleme planı</span><span class="sxs-lookup"><span data-stu-id="5186c-342">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="5186c-343">Kalite emirlerinin otomatik olarak oluşturulmasını gerektiren iş işlemindeki her farklılık için bir kalite eşleştirmesi tanımlamanız gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="5186c-343">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="5186c-344">Örneğin, satınalma siparişleri, karantina siparişleri, satış siparişleri ve üretim emirleri için iş süreçlerinde bir kalite emri oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="5186c-344">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5186c-345">Testler</span><span class="sxs-lookup"><span data-stu-id="5186c-345">Tests</span></span></td>
<td><span data-ttu-id="5186c-346">Ürünlerinizin kalite belirtimlerini sağlayıp sağlamadığını belirleyen tek tek testler tanımlamak ve görüntülemek için bu sayfayı kullanın.</span><span class="sxs-lookup"><span data-stu-id="5186c-346">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="5186c-347">Bir veya daha çok bireysel testleri bir test grubuna atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5186c-347">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="5186c-348">Bu durumda, kabul edilebilir ölçüm değerleri gibi teste özgü bilgileri de belirtirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5186c-348">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="5186c-349">Ölçüm değerleri nicel testleri için kullanılır ve nitel testler için test değişkenleri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5186c-349">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="5186c-350">Nicel bir testin bir test tür <strong>tamsayı</strong> veya <strong>kesir</strong>, ve de atanmış bir ölçüsü vardır.</span><span class="sxs-lookup"><span data-stu-id="5186c-350">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="5186c-351">Kalite belirtimleri ve test sonuçları sayı olarak ifade edilir.</span><span class="sxs-lookup"><span data-stu-id="5186c-351">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="5186c-352">Kalite testi, <strong>Seçenek</strong> test tipindedir.</span><span class="sxs-lookup"><span data-stu-id="5186c-352">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="5186c-353">Kalite testleri, ölçülmekte olan değişken ve onun numaralandırılmış seçenekleri hakkında ek bilgi gerektirirler.</span><span class="sxs-lookup"><span data-stu-id="5186c-353">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="5186c-354">Kalite belirtimleri ve test sonuçları bir sonuca göre ifade edilirler.</span><span class="sxs-lookup"><span data-stu-id="5186c-354">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="5186c-355">Bir üretim şirketi satınalınan malzeme üzerinde, malzeme kalitesi hakkında bir sayısal test ile ambalaj hasarı üzerine bir kalite testi dahil olmak üzere iki test gerçekleştiriyor.</span><span class="sxs-lookup"><span data-stu-id="5186c-355">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="5186c-356">Şirket, test değişkenini (hasarlı ambalaj) ve sonuçlarını tanımlamak için ek bilgiler tanımlıyor.</span><span class="sxs-lookup"><span data-stu-id="5186c-356">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="5186c-357">Şirket <strong>Test grupları</strong> sayfasını iki testleri bir test grubuna atamak için ve teste özgü bilgileri belirtmek için kullanır.</span><span class="sxs-lookup"><span data-stu-id="5186c-357">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="5186c-358">Test grubu, şirketin iki teste ait test sonuçlarını rapor edebilmesi için bir kalite emrine atanır.</span><span class="sxs-lookup"><span data-stu-id="5186c-358">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5186c-359">Test grupları</span><span class="sxs-lookup"><span data-stu-id="5186c-359">Test groups</span></span></td>
<td><span data-ttu-id="5186c-360">Test gruplarını ve test grubuna atanmış bireysel testleri ayarlamak, düzenlemek ve görüntülemek için bu sayfayı kullanın.</span><span class="sxs-lookup"><span data-stu-id="5186c-360">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="5186c-361">Üst bölme test gruplarını gösterir ve alt bölme seçili bir test grubuna atanan testleri görüntüler.</span><span class="sxs-lookup"><span data-stu-id="5186c-361">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="5186c-362">Test grubuna; örnekleme planı, kabul edilebilir kalite düzeyi ve bozucu test gereksinimi gibi birçok ilke atarsınız.</span><span class="sxs-lookup"><span data-stu-id="5186c-362">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="5186c-363">Tek bir testi bir test grubuna atadığınızda, sıra, belgeler ve geçerlilik tarihleri gibi ek bilgiler tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="5186c-363">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="5186c-364">Nicel bir test için tanımladığınız bilgilere kabul edilebilir ölçüm değerleri de dahildir.</span><span class="sxs-lookup"><span data-stu-id="5186c-364">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="5186c-365">Nitel bir test için bu bilgilere test değişkeni ve varsayılan sonuç dahildir.</span><span class="sxs-lookup"><span data-stu-id="5186c-365">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="5186c-366">Bir kalite emrine atanan test grubu, belirtilen öğe üzerinde gerçekleştirilmesi gereken testlerin varsayılan kümesini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="5186c-366">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="5186c-367">Bununla birlikte, kalite emrindeki testleri değiştirebilirsiniz, ekleyebilir veya silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5186c-367">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="5186c-368">Test sonuçları, kalite emrindeki her test için rapor edilir.</span><span class="sxs-lookup"><span data-stu-id="5186c-368">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="5186c-369">Bir üretim şirketi, kalite yönergelerindeki her sapma için bir test grubu tanımlıyor.</span><span class="sxs-lookup"><span data-stu-id="5186c-369">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="5186c-370">Çeşitli test grupları, örnekleme planları arasındaki farklılıkları, birlikte gerçekleştirilmesi gereken testler kümesini, kabul edilebilir kalite düzeyini ve diğer etkenleri yansıtır.</span><span class="sxs-lookup"><span data-stu-id="5186c-370">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="5186c-371">Nicel testleri için, kabul edilebilir ölçüm değerleri için de farklılıklar vardır.</span><span class="sxs-lookup"><span data-stu-id="5186c-371">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="5186c-372">Şirket, kalite kurallarını uygulayabilmek için kalite emirlerini otomatik oluşturabilmek için her kurala bir test grubunu <strong>Kalite ilişkilendirmeleri</strong> sayfasından atar ve ayrıca el ile oluşturulan kalite emirlerine de bir test grubu atar.</span><span class="sxs-lookup"><span data-stu-id="5186c-372">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5186c-373">Madde kalite grupları</span><span class="sxs-lookup"><span data-stu-id="5186c-373">Item quality groups</span></span></td>
<td><span data-ttu-id="5186c-374">Bir kalite grubuna atanmış maddeleri veya bir maddeye atanmış kalite gruplarını ayarlamak, düzenlemek ve görüntülemek için bu sayfayı kullanın.</span><span class="sxs-lookup"><span data-stu-id="5186c-374">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="5186c-375">Kalite grubu, maddeler için ortak test gereksinimlerini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="5186c-375">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="5186c-376"><strong>Test grupları</strong> sayfasındaki test gereksinimlerini tanımladıktan sonra, kalite emirlerini otomatik olarak oluşturmak için kurallar tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5186c-376">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="5186c-377">İşlemi basitleştirmek için, kuralları her bir öğe için tanımlamanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="5186c-377">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="5186c-378">Bunun yerine, <strong>Kalite ilişkileri</strong> sayfasını kullanarak bir kalite grubu için kurallar tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="5186c-378">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="5186c-379">Ayrıca <strong>Madde kalite grupları</strong> sayfasını kullanarak belirlenmiş bir kalite grubuna ilgili maddeleri atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5186c-379">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="5186c-380">Ayrıca <strong>Madde kalite grupları</strong> sayfasını kullanarak belirlenmiş bir maddeye bir kalite grubuna ilgili maddeye atabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5186c-380">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="5186c-381">Üretim şirketi, gelen denetim için aynı test gereksinimlerine sahip çeşitli hammaddeler satın alıyor.</span><span class="sxs-lookup"><span data-stu-id="5186c-381">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="5186c-382">Şirket bir kalite grubu tanımlar ve artından hammaddeler ile ilişkilendirilmiş olan madde numaralarını bu gruba atar.</span><span class="sxs-lookup"><span data-stu-id="5186c-382">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="5186c-383">Daha sonra aynı sınama gereksinimleri olan yeni bir hammadde türü şirket tarafından satın alınır.</span><span class="sxs-lookup"><span data-stu-id="5186c-383">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="5186c-384">Yeni malzeme için yeni test gereksinimleri ayarlamak yerine, şirket yeni malzeme için madde numarasını mevcut kalite grubuna ekler.</span><span class="sxs-lookup"><span data-stu-id="5186c-384">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="5186c-385">Aynı üretim şirketi, aynı üretim testi gereksinimlerine sahip maddeler de üretiyor ve ön sevkiyat testleri için aynı gereksinimlere sahip maddeleri sevk ediyor.</span><span class="sxs-lookup"><span data-stu-id="5186c-385">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="5186c-386">Şirket iki ek kalite grubu tanımlıyor ve sonra her gruba ilgili madde numaralarını atıyor.</span><span class="sxs-lookup"><span data-stu-id="5186c-386">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5186c-387">Test değişkenleri</span><span class="sxs-lookup"><span data-stu-id="5186c-387">Test variables</span></span></td>
<td><span data-ttu-id="5186c-388">Nitel bir test ile ilişkili değişkenleri görüntülemek ve tanımlamak için bu sayfayı kullanın.</span><span class="sxs-lookup"><span data-stu-id="5186c-388">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="5186c-389">Her değişken için olası sonuçları gösteren numaralandırılmış seçenekleri tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="5186c-389">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="5186c-390">Testleri tanımlamak için <strong>Testler</strong> sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="5186c-390">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="5186c-391">Nitel testler için test türünü <strong>Seçenek</strong> olarak ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="5186c-391">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="5186c-392"><strong>Test grupları</strong> sayfasını kullanarak bir teste bir test değişkeni atayın.</span><span class="sxs-lookup"><span data-stu-id="5186c-392">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="5186c-393">Kurabiye üreten bir üretim şirketi, tamamlanan ürüne yönelik bir denetim testi uyguluyor.</span><span class="sxs-lookup"><span data-stu-id="5186c-393">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="5186c-394">Bu inceleme testinin birçok değişkeni vardır.</span><span class="sxs-lookup"><span data-stu-id="5186c-394">This inspection test has several variables.</span></span> <span data-ttu-id="5186c-395">Bir değişken lezzettir ve bu değişkenin olası sonuçları iyi veya kötü olabilir.</span><span class="sxs-lookup"><span data-stu-id="5186c-395">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="5186c-396">İkinci bir değişken, çok koyu, çok açık ve doğru sonuçları ile temsil edilen renk değişkeni oluyor.</span><span class="sxs-lookup"><span data-stu-id="5186c-396">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5186c-397">Test değişkeni sonuçları</span><span class="sxs-lookup"><span data-stu-id="5186c-397">Test variable outcomes</span></span></td>
<td><span data-ttu-id="5186c-398">Bir kalite testiyle ilişkili bir test değişkenine ait olası test sonuçlarını ayarlamak, düzenlemek ve görüntülemek için bu sayfayı kullanın.</span><span class="sxs-lookup"><span data-stu-id="5186c-398">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="5186c-399">Her sonuç için bir <strong>geçti</strong> veya <strong>başarısız</strong> oldu durumu atarsınız.</span><span class="sxs-lookup"><span data-stu-id="5186c-399">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="5186c-400"><strong>Testler</strong> sayfasında tanımlanan her nitel test için bir değişken ve sonuçlarını tanımlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="5186c-400">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="5186c-401">(Kalite testleri için, test türü <strong>Testler</strong> sayfasında <strong>Seçenek</strong> olarak ayarlanmıştır.) <strong>Test grupları</strong> sayfasını kullanıp, bir test değişkenini ve varsayılan sonucu bir kişisel kalite testine atayın.</span><span class="sxs-lookup"><span data-stu-id="5186c-401">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="5186c-402">Kurabiye üreten bir üretim şirketi, tamamlanan ürüne yönelik bir denetim testi uyguluyor.</span><span class="sxs-lookup"><span data-stu-id="5186c-402">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="5186c-403">Bu inceleme testinin birçok değişkeni vardır.</span><span class="sxs-lookup"><span data-stu-id="5186c-403">This inspection test has of several variables.</span></span> <span data-ttu-id="5186c-404">Bir değişken lezzettir ve bu değişkenin olası sonuçları iyi veya kötü olabilir.</span><span class="sxs-lookup"><span data-stu-id="5186c-404">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="5186c-405">İkinci bir değişken, çok koyu, çok açık ve doğru sonuçları ile temsil edilen renk değişkeni oluyor.</span><span class="sxs-lookup"><span data-stu-id="5186c-405">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="5186c-406">Her sonuca <strong>geçti</strong> veya <strong>kaldı</strong> durumu atanır.</span><span class="sxs-lookup"><span data-stu-id="5186c-406">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="5186c-407">Her değişkene yönelik denetim testi sırasında, denetçi sonuçlardan birini seçerek test sonucunu rapor ediyor.</span><span class="sxs-lookup"><span data-stu-id="5186c-407">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="5186c-408">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="5186c-408">Additional resources</span></span>
--------

[<span data-ttu-id="5186c-409">Kalite yönetimi işlemleri</span><span class="sxs-lookup"><span data-stu-id="5186c-409">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="5186c-410">Uygunsuzluk yönetimi</span><span class="sxs-lookup"><span data-stu-id="5186c-410">Nonconformance management</span></span>](enable-nonconformance-management.md)

[<span data-ttu-id="5186c-411">Ambar işlemleri için kalite yönetimi</span><span class="sxs-lookup"><span data-stu-id="5186c-411">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)
