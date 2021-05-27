---
title: Kalite ilişkileri
description: Bu konu, satış, satınalma ve üretim süreçleriniz ile ilgili kalite emirlerini otomatik olarak oluşturmak için Microsoft Dynamics 365 Supply Chain Management'ta kalite ilişkilendirmelerini nasıl kullanabileceğinizi açıklamaktadır.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2020-06-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c6fab1b89b7e58d9e443c27da03a6b13afcc9c6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022336"
---
# <a name="quality-associations"></a><span data-ttu-id="9cdec-103">Kalite ilişkileri</span><span class="sxs-lookup"><span data-stu-id="9cdec-103">Quality associations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9cdec-104">Bu konu, satış, satınalma ve üretim süreçleriniz ile ilgili kalite emirlerini otomatik olarak oluşturmak için Microsoft Dynamics 365 Supply Chain Management'ta kalite ilişkilendirmelerini nasıl kullanabileceğinizi açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="9cdec-104">This topic describes how you can use quality associations in Microsoft Dynamics 365 Supply Chain Management to automatically generate quality orders that are related to your sales, purchase, and production processes.</span></span>

<span data-ttu-id="9cdec-105">Bir kalite ilişkisi oluşturulan bir kalite emri için aşağıdaki tüm bilgileri tanımlar:</span><span class="sxs-lookup"><span data-stu-id="9cdec-105">A quality association defines all the following information for a quality order that is generated:</span></span>

- <span data-ttu-id="9cdec-106">Hareket olayı</span><span class="sxs-lookup"><span data-stu-id="9cdec-106">The transaction event</span></span>
- <span data-ttu-id="9cdec-107">Öğeler üzerinde gerçekleştirilmesi gereken test dizileri</span><span class="sxs-lookup"><span data-stu-id="9cdec-107">The set of tests that must be performed on the items</span></span>
- <span data-ttu-id="9cdec-108">Kabul edilebilir kalite düzeyi (AQL)</span><span class="sxs-lookup"><span data-stu-id="9cdec-108">The acceptable quality level (AQL)</span></span>
- <span data-ttu-id="9cdec-109">Örnekleme planı</span><span class="sxs-lookup"><span data-stu-id="9cdec-109">The sampling plan</span></span>

<span data-ttu-id="9cdec-110">Kalite emirlerinin otomatik olarak oluşturulmasını gerektiren iş işlemindeki her farklılık için bir kalite eşleştirmesi tanımlamanız gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="9cdec-110">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="9cdec-111">Örneğin, satınalma siparişleri, karantina siparişleri, satış siparişleri ve üretim emirleri için iş süreçlerinde bir kalite emri oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="9cdec-111">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="9cdec-112">Kalite ilişkileri ile çalışmak</span><span class="sxs-lookup"><span data-stu-id="9cdec-112">Working with quality associations</span></span>

<span data-ttu-id="9cdec-113">Kalite ilişkisini kullanan iş süreci, satınalma siparişleri, satış siparişleri veya üretim emirleri gibi çeşitli kaynak belgelere ilişkili olabilir.</span><span class="sxs-lookup"><span data-stu-id="9cdec-113">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="9cdec-114">Her kalite bağlantısı kaydı oluşturulan kalite emirlerine geçerli olacak testler kümesini, AQL'yi ve örnek alma planını da tanımlamaktadır.</span><span class="sxs-lookup"><span data-stu-id="9cdec-114">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="9cdec-115">Bir iş sürecindeki her değişim için bir kalite ilişkisi kaydı tanımlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="9cdec-115">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="9cdec-116">Örneğin, bir satınalma siparişi ürün alış irsaliyesi güncelleştirildiğinde, kalite emri oluşturacak bir kalite ilişkisi ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9cdec-116">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="9cdec-117">Yürütme planının kurulumuna bağlı olarak, tetikleme işleminin kendisi açık bir kalite emri olduğunda bloke edilebilir.</span><span class="sxs-lookup"><span data-stu-id="9cdec-117">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order.</span></span> <span data-ttu-id="9cdec-118">Ayrıca, satınalma siparişi faturalama gibi sonraki işlemler bloke edilebilir.</span><span class="sxs-lookup"><span data-stu-id="9cdec-118">Alternatively, subsequent processes, such as purchase order invoicing, can be blocked.</span></span>

> [!NOTE]
> <span data-ttu-id="9cdec-119">Açık kalite emirleri olduğunda, stok miktarlarının çıkarılması otomatik olarak engellenir.</span><span class="sxs-lookup"><span data-stu-id="9cdec-119">While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="9cdec-120">**Madde örnekleri** sayfasında bulunan **Tam engelleme** alanı ayarlarına bağlı olarak, miktar kalite emrindeki miktardır ya da kaynak belge satırındaki miktardır.</span><span class="sxs-lookup"><span data-stu-id="9cdec-120">Depending on the setting of the **Full blocking** field on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span> <span data-ttu-id="9cdec-121">Daha fazla bilgi için bkz. [Kalite yönetimi madde örnekleme](quality-item-sampling.md).</span><span class="sxs-lookup"><span data-stu-id="9cdec-121">For more information, see [Quality management item sampling](quality-item-sampling.md).</span></span>

<span data-ttu-id="9cdec-122">Bir iş süreci için, kalite ilişkisi kaydı, kalite emrinin oluşturulduğu olay ve koşulları tanımlar.</span><span class="sxs-lookup"><span data-stu-id="9cdec-122">For a given business process, the quality association record identifies the event and conditions that a quality order is generated for.</span></span> <span data-ttu-id="9cdec-123">Koşullar bir siteye veya bir tüzel kişiliğe özel olabilir.</span><span class="sxs-lookup"><span data-stu-id="9cdec-123">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="9cdec-124">Bozucu testler içeren bir kalite emri yalnızca olay için eldeki stok bulunması durumunda oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="9cdec-124">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="9cdec-125">Kalite ilişkilendirmeleriyle çalışmak için **Stok yönetimi \> Kurulum \> Kalite kontrol \> Kalite ilişkilendirmeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="9cdec-125">To work with quality associations, go to **Inventory management \> Setup \> Quality control \> Quality associations**.</span></span> <span data-ttu-id="9cdec-126">Aşağıdaki örnekler, her iş sürecindeki değişiklikler için bir kalite bağlantısını tanımlamayı açıklar.</span><span class="sxs-lookup"><span data-stu-id="9cdec-126">The following examples show how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="9cdec-127">Her örnek için, aşağıdaki tablo kalite ilişki kaydındaki olayları ve durumları özetler.</span><span class="sxs-lookup"><span data-stu-id="9cdec-127">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9cdec-128">Referans türü</span><span class="sxs-lookup"><span data-stu-id="9cdec-128">Reference type</span></span></th>
<th><span data-ttu-id="9cdec-129">Olay türü</span><span class="sxs-lookup"><span data-stu-id="9cdec-129">Event type</span></span></th>
<th><span data-ttu-id="9cdec-130">Yürütme</span><span class="sxs-lookup"><span data-stu-id="9cdec-130">Execution</span></span></th>
<th><span data-ttu-id="9cdec-131">Olay durdurma</span><span class="sxs-lookup"><span data-stu-id="9cdec-131">Event blocking</span></span></th>
<th><span data-ttu-id="9cdec-132">Belge başvurusu</span><span class="sxs-lookup"><span data-stu-id="9cdec-132">Document reference</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9cdec-133">Stok</span><span class="sxs-lookup"><span data-stu-id="9cdec-133">Inventory</span></span></td>
<td><span data-ttu-id="9cdec-134">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="9cdec-134">Not applicable</span></span></td>
<td><span data-ttu-id="9cdec-135">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="9cdec-135">Not applicable</span></span></td>
<td><span data-ttu-id="9cdec-136">Yok</span><span class="sxs-lookup"><span data-stu-id="9cdec-136">None</span></span></td>
<td><span data-ttu-id="9cdec-137">Tümü</span><span class="sxs-lookup"><span data-stu-id="9cdec-137">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="9cdec-138">Satışlar</span><span class="sxs-lookup"><span data-stu-id="9cdec-138">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="9cdec-139">Malzeme çekme işlemi planlandı</span><span class="sxs-lookup"><span data-stu-id="9cdec-139">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="9cdec-140">Önce</span><span class="sxs-lookup"><span data-stu-id="9cdec-140">Before</span></span></td>
<td><span data-ttu-id="9cdec-141">Yok</span><span class="sxs-lookup"><span data-stu-id="9cdec-141">None</span></span></td>
<td rowspan="22"><span data-ttu-id="9cdec-142">Belirli Kimlik, Grup veya Yalnızca tümü</span><span class="sxs-lookup"><span data-stu-id="9cdec-142">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cdec-143">Malzeme çekme işlemi</span><span class="sxs-lookup"><span data-stu-id="9cdec-143">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cdec-144">Sevk irsaliyesi</span><span class="sxs-lookup"><span data-stu-id="9cdec-144">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cdec-145">Fatura</span><span class="sxs-lookup"><span data-stu-id="9cdec-145">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9cdec-146">Sevk irsaliyesi</span><span class="sxs-lookup"><span data-stu-id="9cdec-146">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="9cdec-147">Önce</span><span class="sxs-lookup"><span data-stu-id="9cdec-147">Before</span></span></td>
<td><span data-ttu-id="9cdec-148">Yok</span><span class="sxs-lookup"><span data-stu-id="9cdec-148">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cdec-149">Sevk irsaliyesi</span><span class="sxs-lookup"><span data-stu-id="9cdec-149">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cdec-150">Fatura</span><span class="sxs-lookup"><span data-stu-id="9cdec-150">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="9cdec-151">Satınalma</span><span class="sxs-lookup"><span data-stu-id="9cdec-151">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="9cdec-152">Giriş listesi</span><span class="sxs-lookup"><span data-stu-id="9cdec-152">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="9cdec-153">Önce</span><span class="sxs-lookup"><span data-stu-id="9cdec-153">Before</span></span></td>
<td><span data-ttu-id="9cdec-154">Yok</span><span class="sxs-lookup"><span data-stu-id="9cdec-154">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cdec-155">Giriş listesi</span><span class="sxs-lookup"><span data-stu-id="9cdec-155">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cdec-156">Ürün girişi</span><span class="sxs-lookup"><span data-stu-id="9cdec-156">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cdec-157">Fatura</span><span class="sxs-lookup"><span data-stu-id="9cdec-157">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9cdec-158">Sonra</span><span class="sxs-lookup"><span data-stu-id="9cdec-158">After</span></span></td>
<td><span data-ttu-id="9cdec-159">Yok</span><span class="sxs-lookup"><span data-stu-id="9cdec-159">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cdec-160">Ürün girişi</span><span class="sxs-lookup"><span data-stu-id="9cdec-160">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cdec-161">Fatura</span><span class="sxs-lookup"><span data-stu-id="9cdec-161">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9cdec-162">Kayıt</span><span class="sxs-lookup"><span data-stu-id="9cdec-162">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="9cdec-163">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="9cdec-163">Not applicable</span></span></td>
<td><span data-ttu-id="9cdec-164">Yok</span><span class="sxs-lookup"><span data-stu-id="9cdec-164">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cdec-165">Ürün girişi</span><span class="sxs-lookup"><span data-stu-id="9cdec-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cdec-166">Fatura</span><span class="sxs-lookup"><span data-stu-id="9cdec-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="9cdec-167">Ürün girişi</span><span class="sxs-lookup"><span data-stu-id="9cdec-167">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="9cdec-168">Önce</span><span class="sxs-lookup"><span data-stu-id="9cdec-168">Before</span></span></td>
<td><span data-ttu-id="9cdec-169">Yok</span><span class="sxs-lookup"><span data-stu-id="9cdec-169">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cdec-170">Ürün girişi</span><span class="sxs-lookup"><span data-stu-id="9cdec-170">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cdec-171">Fatura</span><span class="sxs-lookup"><span data-stu-id="9cdec-171">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="9cdec-172">Sonra</span><span class="sxs-lookup"><span data-stu-id="9cdec-172">After</span></span></td>
<td><span data-ttu-id="9cdec-173">Yok</span><span class="sxs-lookup"><span data-stu-id="9cdec-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cdec-174">Fatura</span><span class="sxs-lookup"><span data-stu-id="9cdec-174">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="9cdec-175">Üretim</span><span class="sxs-lookup"><span data-stu-id="9cdec-175">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="9cdec-176">Kayıt</span><span class="sxs-lookup"><span data-stu-id="9cdec-176">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="9cdec-177">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="9cdec-177">Not applicable</span></span></td>
<td><span data-ttu-id="9cdec-178">Yok</span><span class="sxs-lookup"><span data-stu-id="9cdec-178">None</span></span></td>
<td rowspan="12"><span data-ttu-id="9cdec-179">Tümü</span><span class="sxs-lookup"><span data-stu-id="9cdec-179">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cdec-180">Tamamlandı bildirimi</span><span class="sxs-lookup"><span data-stu-id="9cdec-180">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cdec-181">Bitir</span><span class="sxs-lookup"><span data-stu-id="9cdec-181">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="9cdec-182">Tamamlandı bildirimi</span><span class="sxs-lookup"><span data-stu-id="9cdec-182">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="9cdec-183">Önce</span><span class="sxs-lookup"><span data-stu-id="9cdec-183">Before</span></span></td>
<td><span data-ttu-id="9cdec-184">Yok</span><span class="sxs-lookup"><span data-stu-id="9cdec-184">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cdec-185">Tamamlandı bildirimi</span><span class="sxs-lookup"><span data-stu-id="9cdec-185">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cdec-186">Bitir</span><span class="sxs-lookup"><span data-stu-id="9cdec-186">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="9cdec-187">Sonra</span><span class="sxs-lookup"><span data-stu-id="9cdec-187">After</span></span></td>
<td><span data-ttu-id="9cdec-188">Yok</span><span class="sxs-lookup"><span data-stu-id="9cdec-188">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cdec-189">Bitir</span><span class="sxs-lookup"><span data-stu-id="9cdec-189">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="9cdec-190">Karantina</span><span class="sxs-lookup"><span data-stu-id="9cdec-190">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="9cdec-191">Tamamlandı bildirimi</span><span class="sxs-lookup"><span data-stu-id="9cdec-191">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="9cdec-192">Önce</span><span class="sxs-lookup"><span data-stu-id="9cdec-192">Before</span></span></td>
<td><span data-ttu-id="9cdec-193">Tamamlandı bildirimi</span><span class="sxs-lookup"><span data-stu-id="9cdec-193">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cdec-194">Bitir</span><span class="sxs-lookup"><span data-stu-id="9cdec-194">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cdec-195">Sonra</span><span class="sxs-lookup"><span data-stu-id="9cdec-195">After</span></span></td>
<td><span data-ttu-id="9cdec-196">Bitir</span><span class="sxs-lookup"><span data-stu-id="9cdec-196">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cdec-197">Bitir</span><span class="sxs-lookup"><span data-stu-id="9cdec-197">End</span></span></td>
<td><span data-ttu-id="9cdec-198">Önce</span><span class="sxs-lookup"><span data-stu-id="9cdec-198">Before</span></span></td>
<td><span data-ttu-id="9cdec-199">Bitir</span><span class="sxs-lookup"><span data-stu-id="9cdec-199">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9cdec-200">Rota operasyonu</span><span class="sxs-lookup"><span data-stu-id="9cdec-200">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="9cdec-201">Tamamlandı bildirimi</span><span class="sxs-lookup"><span data-stu-id="9cdec-201">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="9cdec-202">Önce</span><span class="sxs-lookup"><span data-stu-id="9cdec-202">Before</span></span></td>
<td><span data-ttu-id="9cdec-203">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="9cdec-203">None</span></span></td>
<td rowspan="3"><span data-ttu-id="9cdec-204">Belirli Kimlik, Grup veya Tümü ve Kaynağa özel, Grup veya Tümü</span><span class="sxs-lookup"><span data-stu-id="9cdec-204">Specific ID, Group, or All, and specific Resource, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cdec-205">Tamamlandı bildirimi</span><span class="sxs-lookup"><span data-stu-id="9cdec-205">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cdec-206">Sonra</span><span class="sxs-lookup"><span data-stu-id="9cdec-206">After</span></span></td>
<td><span data-ttu-id="9cdec-207">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="9cdec-207">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9cdec-208">Ortak ürün üretimi</span><span class="sxs-lookup"><span data-stu-id="9cdec-208">Co-product production</span></span></td>
<td><span data-ttu-id="9cdec-209">Kayıt</span><span class="sxs-lookup"><span data-stu-id="9cdec-209">Registration</span></span></td>
<td><span data-ttu-id="9cdec-210">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="9cdec-210">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="9cdec-211">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="9cdec-211">None</span></span></td>
<td rowspan="3"><span data-ttu-id="9cdec-212">Tümü</span><span class="sxs-lookup"><span data-stu-id="9cdec-212">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="9cdec-213">Tamamlandı bildirimi</span><span class="sxs-lookup"><span data-stu-id="9cdec-213">Report as finished</span></span></td>
<td><span data-ttu-id="9cdec-214">Önce</span><span class="sxs-lookup"><span data-stu-id="9cdec-214">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cdec-215">Sonra</span><span class="sxs-lookup"><span data-stu-id="9cdec-215">After</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="9cdec-216">*Ambar işlemleri için kalite yönetimi* özelliği, **Olay Türü** alanı *Tamamlandı olarak bildir*, **Yürütme** alanı *Sonra* olarak ayarlanmış olan üretim ve **Olay türü** alanı *Kayıt* olarak ayarlanmış satınalmalar için kalite emri işleme yetenekleri ekler.</span><span class="sxs-lookup"><span data-stu-id="9cdec-216">The *Quality management for warehouse processes* feature adds capabilities for quality order processing for production where the **Event type** field is set to *Report as finished* and the **Execution** field is set to *After*, and for purchases where the **Event type** field is set to *Registration*.</span></span> <span data-ttu-id="9cdec-217">Daha fazla bilgi için bkz. [Ambar işlemleri için kalite yönetimi](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="9cdec-217">For more information, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

<span data-ttu-id="9cdec-218">Aşağıdaki tabloda belirli türde işlemler için kalite emirlerinin nasıl oluşturulabileceği hakkında daha fazla bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="9cdec-218">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>

<div class="tableSection">
<table>
<thead>
<tr>
<th><span data-ttu-id="9cdec-219">İşleme türü</span><span class="sxs-lookup"><span data-stu-id="9cdec-219">Type of process</span></span></th>
<th><span data-ttu-id="9cdec-220">Kalite emirlerinin ne zaman otomatik olarak oluşturulabileceği</span><span class="sxs-lookup"><span data-stu-id="9cdec-220">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="9cdec-221">Bozucu sınama yapılması gerekirse kalite emirlerinin ne zaman oluşturulabileceği</span><span class="sxs-lookup"><span data-stu-id="9cdec-221">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="9cdec-222">Koşul bilgisi</span><span class="sxs-lookup"><span data-stu-id="9cdec-222">Condition information</span></span></th>
<th><span data-ttu-id="9cdec-223">El ile oluşturma bilgisi</span><span class="sxs-lookup"><span data-stu-id="9cdec-223">Manual generation information</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9cdec-224">Satın alma siparişi</span><span class="sxs-lookup"><span data-stu-id="9cdec-224">Purchase order</span></span></td>
<td><span data-ttu-id="9cdec-225">Alınan malzeme için ürün girişi ya da giriş listesi nakledildikten önce veya sonra.</span><span class="sxs-lookup"><span data-stu-id="9cdec-225">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="9cdec-226">Alınan malzeme için ürün girişi nakledildikten sonra, çünkü malzemenin bozucu test için mevcut olması gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="9cdec-226">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="9cdec-227">Kalite emri gereksinimi özel bir tesisi, maddeyi veya satıcıyı ya da bunların bir birleşimini yansıtabilir.</span><span class="sxs-lookup"><span data-stu-id="9cdec-227">The requirement for a quality order can reflect a specific site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="9cdec-228">Bir satınalma siparişine gönderme yapan ve el ile oluşturulmuş bir kalite emri, tasarlanmış örnek alma planı gibi, bir kalite bağlantısı kaydında bulunan bilgileri kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="9cdec-228">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cdec-229">Karantina emri</span><span class="sxs-lookup"><span data-stu-id="9cdec-229">Quarantine order</span></span></td>
<td><span data-ttu-id="9cdec-230">Karantina siparişi tamamlandı veya sona erdi olarak bildirildikten önce veya sonra.</span><span class="sxs-lookup"><span data-stu-id="9cdec-230">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="9cdec-231">Yıkıcı testler gerektiren kalite emirleri oluşturulamaz.</span><span class="sxs-lookup"><span data-stu-id="9cdec-231">Quality orders that require destructive tests can't be generated.</span></span> <span data-ttu-id="9cdec-232">Karantina siparişi işlevinin, yok edilen malzemenin elden çıkarılmasını üstleneceği kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="9cdec-232">It's assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="9cdec-233">Kalite emri gereksinimi özel bir tesisi, maddeyi veya satıcıyı ya da bunların bir birleşimini yansıtabilir.</span><span class="sxs-lookup"><span data-stu-id="9cdec-233">The requirement for a quality order can reflect a specific site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="9cdec-234">Bir karantina siparişine gönderme yapan ve el ile oluşturulmuş bir kalite emri, tasarlanmış örnek alma planı gibi, bir kalite bağlantısı kaydında bulunan bilgileri kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="9cdec-234">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cdec-235">Satış siparişi</span><span class="sxs-lookup"><span data-stu-id="9cdec-235">Sales order</span></span></td>
<td><span data-ttu-id="9cdec-236">Bir zamanlanmış malzeme çekme işlem veya sevk irsaliyesi güncelleştirmesi sevk maddeler için önce</span><span class="sxs-lookup"><span data-stu-id="9cdec-236">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="9cdec-237">Herhangi bir adımda</span><span class="sxs-lookup"><span data-stu-id="9cdec-237">At any step</span></span></td>
<td><span data-ttu-id="9cdec-238">Kalite emri gereksinimi özel bir tesisi, maddeyi veya satıcıyı ya da bunların bir birleşimini yansıtabilir.</span><span class="sxs-lookup"><span data-stu-id="9cdec-238">The requirement for a quality order can reflect a specific site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="9cdec-239">Bir satış siparişine gönderme yapan ve el ile oluşturulmuş bir kalite emri, tasarlanmış örnek alma planı gibi, bir kalite bağlantısı kaydında bulunan bilgileri kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="9cdec-239">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cdec-240">Üretim emri</span><span class="sxs-lookup"><span data-stu-id="9cdec-240">Production order</span></span></td>
<td><span data-ttu-id="9cdec-241">Üretim emri için bitmiş miktar rapor edildikten önce veya sonra</span><span class="sxs-lookup"><span data-stu-id="9cdec-241">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="9cdec-242">Üretim emri için bitmiş miktar rapor edildikten sonra</span><span class="sxs-lookup"><span data-stu-id="9cdec-242">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="9cdec-243">Kalite emri gereksinimi özel bir tesisi veya satıcıyı ya da bunların bir birleşimini yansıtabilir.</span><span class="sxs-lookup"><span data-stu-id="9cdec-243">The requirement for a quality order can reflect a specific site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="9cdec-244">Bir üretim emrine gönderme yapan ve el ile oluşturulmuş bir kalite emri, tasarlanmış örnek alma planı gibi, bir kalite bağlantısı kaydında bulunan bilgileri kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="9cdec-244">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cdec-245">Bir rota operasyonuna sahip olan üretim emri</span><span class="sxs-lookup"><span data-stu-id="9cdec-245">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="9cdec-246">Bir operasyon için bir rapor sona erdikten önce veya sonra</span><span class="sxs-lookup"><span data-stu-id="9cdec-246">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="9cdec-247">Son operasyon için raporlama üretimi bittikten sonra.</span><span class="sxs-lookup"><span data-stu-id="9cdec-247">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="9cdec-248">Kalite emri gereksinimi özel bir tesisi, maddeyi veya operasyon kaynağı ya da bunların bir birleşimini yansıtabilir.</span><span class="sxs-lookup"><span data-stu-id="9cdec-248">The requirement for a quality order can reflect a specific site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="9cdec-249">Bir rota operasyonu gönderme yapan ve el ile oluşturulmuş bir kalite emri, tasarlanmış örnek alma planı gibi, bir kalite bağlantısı kaydında bulunan bilgileri kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="9cdec-249">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9cdec-250">Stok</span><span class="sxs-lookup"><span data-stu-id="9cdec-250">Inventory</span></span></td>
<td><span data-ttu-id="9cdec-251">Bir kalite emri, transfer emri hareketleri veya bir stok günlüğünde bir hareket için otomatik olarak oluşturulamaz.</span><span class="sxs-lookup"><span data-stu-id="9cdec-251">A quality order can't be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="9cdec-252">Bir kalite emrinin bir maddenin stok miktarı için el ile oluşturulması gerekir.</span><span class="sxs-lookup"><span data-stu-id="9cdec-252">A quality order must be manually created for an item's inventory quantity.</span></span> <span data-ttu-id="9cdec-253">Fiziksel eldeki stok gereklidir.</span><span class="sxs-lookup"><span data-stu-id="9cdec-253">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>
</div>

## <a name="examples-of-automatic-generation-of-quality-orders"></a><span data-ttu-id="9cdec-254">Kalite emirlerinin otomatik oluşturulmasına ilişkin örnekler</span><span class="sxs-lookup"><span data-stu-id="9cdec-254">Examples of automatic generation of quality orders</span></span>

### <a name="purchasing"></a><span data-ttu-id="9cdec-255">Satınalma</span><span class="sxs-lookup"><span data-stu-id="9cdec-255">Purchasing</span></span>

<span data-ttu-id="9cdec-256">Satınalmada, **Kalite ilişkilendirmeleri** sayfasında **Olay türü** alanını *Ürün girişi* ve **Yürütme** alanını *Sonra* olarak ayarlarsanız aşağıdaki sonuçları elde edersiniz:</span><span class="sxs-lookup"><span data-stu-id="9cdec-256">In purchasing, if you set the **Event type** field to *Product receipt* and the **Execution** field to *After* on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="9cdec-257">**Güncelleştirilen miktar başına** seçeneği *Evet* olarak ayarlanmışsa, madde örneklemesindeki teslim alınan miktar ve ayarlar temel alınarak satınalma siparişiyle ilgili her giriş için bir kalite emri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="9cdec-257">If the **Per updated quantity** option is set to *Yes*, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="9cdec-258">Satınalma siparişine göre bir miktar her teslim alındığında, yeni teslim alınan miktar temel alınarak geçerli kalite emirleri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="9cdec-258">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="9cdec-259">**Güncelleştirilen miktar başına** seçeneği *Hayır* olarak ayarlanmışsa, teslim alınan miktar ve ayarlar temel alınarak satınalma siparişiyle ilgili ilk giriş için bir kalite emri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="9cdec-259">If the **Per updated quantity** option is set to *No*, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="9cdec-260">Ayrıca, izleme boyutlarına bağlı olarak kalan miktar temel alınarak bir veya daha fazla kalite emri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="9cdec-260">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="9cdec-261">Satınalma siparişiyle ilgili sonraki girişler için kalite emirleri oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="9cdec-261">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="9cdec-262">Üretim</span><span class="sxs-lookup"><span data-stu-id="9cdec-262">Production</span></span>

<span data-ttu-id="9cdec-263">Üretimde, **Kalite ilişkilendirmeleri** sayfasında **Olay türü** alanını *Tamamlandı olarak bildir* ve **Yürütme** alanını *Sonra* olarak ayarlarsanız aşağıdaki sonuçları elde edersiniz:</span><span class="sxs-lookup"><span data-stu-id="9cdec-263">In production, if you set the **Event type** field to *Report as finished* and the **Execution** field to *After* on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="9cdec-264">**Güncelleştirilen miktar başına** seçeneği *Evet* olarak ayarlanmışsa, madde örneklemesindeki her tamamlanan miktar için bir kalite emri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="9cdec-264">If the **Per updated quantity** option is set to *Yes*, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="9cdec-265">Üretim emrine göre bir miktar her tamamlandı olarak bildirildiğinde, yeni tamamlanan miktar temel alınarak geçerli kalite emirleri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="9cdec-265">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on the newly finished quantity.</span></span> <span data-ttu-id="9cdec-266">Bu oluşturma mantığı satın alma ile tutarlıdır.</span><span class="sxs-lookup"><span data-stu-id="9cdec-266">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="9cdec-267">**Güncelleştirilen miktar başına** seçeneği *Hayır* olarak ayarlanmışsa, tamamlanan miktar temel alınarak bir miktar ilk kez tamamlandı olarak bildirildiğinde bir kalite emri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="9cdec-267">If the **Per updated quantity** option is set to *No*, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="9cdec-268">Ayrıca, madde örneklemesinin izleme boyutlarına bağlı olarak kalan miktar temel alınarak bir veya daha fazla kalite emri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="9cdec-268">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="9cdec-269">Sonraki tamamlanan miktarlar için kalite emirleri oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="9cdec-269">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9cdec-270">Kalite belirtimi</span><span class="sxs-lookup"><span data-stu-id="9cdec-270">Quality specification</span></span></th>
<th><span data-ttu-id="9cdec-271">Güncelleştirilen miktar başına</span><span class="sxs-lookup"><span data-stu-id="9cdec-271">Per updated quantity</span></span></th>
<th><span data-ttu-id="9cdec-272">İzleme boyutu başına</span><span class="sxs-lookup"><span data-stu-id="9cdec-272">Per tracking dimension</span></span></th>
<th><span data-ttu-id="9cdec-273">Sonuç</span><span class="sxs-lookup"><span data-stu-id="9cdec-273">Result</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9cdec-274">Yüzde: %10</span><span class="sxs-lookup"><span data-stu-id="9cdec-274">Percentage: 10%</span></span></td>
<td><span data-ttu-id="9cdec-275">Evet</span><span class="sxs-lookup"><span data-stu-id="9cdec-275">Yes</span></span></td>
<td>
<p><span data-ttu-id="9cdec-276">Toplu iş numarası: Hayır</span><span class="sxs-lookup"><span data-stu-id="9cdec-276">Batch number: No</span></span></p>
<p><span data-ttu-id="9cdec-277">Seri numarası: Hayır</span><span class="sxs-lookup"><span data-stu-id="9cdec-277">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="9cdec-278">Sipariş miktarı: 100</span><span class="sxs-lookup"><span data-stu-id="9cdec-278">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="9cdec-279">30 için tamamlandı olarak bildir</span><span class="sxs-lookup"><span data-stu-id="9cdec-279">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="9cdec-280">3 için (30'un %10'u) için kalite emri 1</span><span class="sxs-lookup"><span data-stu-id="9cdec-280">Quality order 1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="9cdec-281">70 için tamamlandı olarak bildir</span><span class="sxs-lookup"><span data-stu-id="9cdec-281">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="9cdec-282">7 (kalan sipariş miktarının %10'u; bu durumda 70'e eşittir) için kalite emri 2</span><span class="sxs-lookup"><span data-stu-id="9cdec-282">Quality order 2 for 7 (10% of the remaining order quantity, which is 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="9cdec-283">Sabit miktar: 1</span><span class="sxs-lookup"><span data-stu-id="9cdec-283">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="9cdec-284">No</span><span class="sxs-lookup"><span data-stu-id="9cdec-284">No</span></span></td>
<td>
<p><span data-ttu-id="9cdec-285">Toplu iş numarası: Hayır</span><span class="sxs-lookup"><span data-stu-id="9cdec-285">Batch number: No</span></span></p>
<p><span data-ttu-id="9cdec-286">Seri numarası: Hayır</span><span class="sxs-lookup"><span data-stu-id="9cdec-286">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="9cdec-287">Sipariş miktarı: 100</span><span class="sxs-lookup"><span data-stu-id="9cdec-287">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="9cdec-288">30 için tamamlandı olarak bildir</span><span class="sxs-lookup"><span data-stu-id="9cdec-288">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="9cdec-289">1 için kalite emri 1 (sabit değeri 1 olan ilk tamamlandı bildirimi miktarı için)</span><span class="sxs-lookup"><span data-stu-id="9cdec-289">Quality order 1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="9cdec-290">1 için kalite emri 2 (sabit değeri hala 1 olan kalan miktar için)</span><span class="sxs-lookup"><span data-stu-id="9cdec-290">Quality order 2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="9cdec-291">10 için tamamlandı olarak bildir</span><span class="sxs-lookup"><span data-stu-id="9cdec-291">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="9cdec-292">Kalite emri oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="9cdec-292">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="9cdec-293">60 için tamamlandı olarak bildir</span><span class="sxs-lookup"><span data-stu-id="9cdec-293">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="9cdec-294">Kalite emri oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="9cdec-294">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="9cdec-295">Sabit miktar: 1</span><span class="sxs-lookup"><span data-stu-id="9cdec-295">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="9cdec-296">Evet</span><span class="sxs-lookup"><span data-stu-id="9cdec-296">Yes</span></span></td>
<td>
<p><span data-ttu-id="9cdec-297">Toplu iş numarası: Evet</span><span class="sxs-lookup"><span data-stu-id="9cdec-297">Batch number: Yes</span></span></p>
<p><span data-ttu-id="9cdec-298">Seri numarası: Evet</span><span class="sxs-lookup"><span data-stu-id="9cdec-298">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="9cdec-299">Sipariş miktarı: 10</span><span class="sxs-lookup"><span data-stu-id="9cdec-299">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="9cdec-300">3 için tamamlanmış haliyle rapor: toplu iş numarası b1, seri numarası s için 1; toplu iş numarası b2, seri numarası s2 için 1 ve toplu iş numarası b3, seri numarası s3 için 1</span><span class="sxs-lookup"><span data-stu-id="9cdec-300">Report as finished for 3: 1 for batch number b1, serial number s1; 1 for batch number b2, serial number s2; and 1 for batch number b3, serial number s3</span></span>
<ul>
<li><span data-ttu-id="9cdec-301">Toplu iş b1, seri s1'in 1'i için kalite emri 1</span><span class="sxs-lookup"><span data-stu-id="9cdec-301">Quality order 1 for 1 of batch number b1, serial number s1</span></span></li>
<li><span data-ttu-id="9cdec-302">Toplu iş b2, seri s2'nin 1'i için kalite emri 2</span><span class="sxs-lookup"><span data-stu-id="9cdec-302">Quality order 2 for 1 of batch number b2, serial number s2</span></span></li>
<li><span data-ttu-id="9cdec-303">Toplu iş b3, seri s3'ün 1'i için kalite emri 3</span><span class="sxs-lookup"><span data-stu-id="9cdec-303">Quality order 3 for 1 of batch number b3, serial number s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="9cdec-304">2 için tamamlanmış haliyle rapor: toplu iş numarası b4, seri numarası s4 için 1 ve toplu iş numarası b5, seri numarası s5 için 1</span><span class="sxs-lookup"><span data-stu-id="9cdec-304">Report as finished for 2: 1 for batch number b4, serial number s4; and 1 for batch number b5, serial number s5</span></span>
<ul>
<li><span data-ttu-id="9cdec-305">Toplu iş b4, seri s4'ün 1'i için kalite emri 4</span><span class="sxs-lookup"><span data-stu-id="9cdec-305">Quality order 4 for 1 of batch number b4, serial number s4</span></span></li>
<li><span data-ttu-id="9cdec-306">Toplu iş b5, seri s5'in 1'i için kalite emri 5</span><span class="sxs-lookup"><span data-stu-id="9cdec-306">Quality order 5 for 1 of batch number b5, serial number s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="9cdec-307"><strong>Not:</strong> Toplu iş yeniden kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9cdec-307"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="9cdec-308">Sabit miktar: 2</span><span class="sxs-lookup"><span data-stu-id="9cdec-308">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="9cdec-309">No</span><span class="sxs-lookup"><span data-stu-id="9cdec-309">No</span></span></td>
<td>
<p><span data-ttu-id="9cdec-310">Toplu iş numarası: Evet</span><span class="sxs-lookup"><span data-stu-id="9cdec-310">Batch number: Yes</span></span></p>
<p><span data-ttu-id="9cdec-311">Seri numarası: Evet</span><span class="sxs-lookup"><span data-stu-id="9cdec-311">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="9cdec-312">Sipariş miktarı: 10</span><span class="sxs-lookup"><span data-stu-id="9cdec-312">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="9cdec-313">4 için tamamlanmış haliyle rapor: toplu iş numarası b1, seri numarası s için 1; toplu iş numarası b2, seri numarası s2 için 1 ve toplu iş numarası b3, seri numarası s3 için 1 ve toplu iş numarası b4, seri numarası s4 için 1</span><span class="sxs-lookup"><span data-stu-id="9cdec-313">Report as finished for 4: 1 for batch number b1, serial number s1; 1 for batch number b2, serial number s2; 1 for batch number b3, serial number s3; and 1 for batch number b4, serial number s4</span></span>
<ul>
<li><span data-ttu-id="9cdec-314">Toplu iş b1, seri s1'in 1'i için kalite emri 1</span><span class="sxs-lookup"><span data-stu-id="9cdec-314">Quality order 1 for 1 of batch number b1, serial number s1</span></span></li>
<li><span data-ttu-id="9cdec-315">Toplu iş b2, seri s2'nin 1'i için kalite emri 2</span><span class="sxs-lookup"><span data-stu-id="9cdec-315">Quality order 2 for 1 of batch number b2, serial number s2</span></span></li>
<li><span data-ttu-id="9cdec-316">Toplu iş b3, seri s3'ün 1'i için kalite emri 3</span><span class="sxs-lookup"><span data-stu-id="9cdec-316">Quality order 3 for 1 of batch number b3, serial number s3</span></span></li>
<li><span data-ttu-id="9cdec-317">Toplu iş b4, seri s4'ün 1'i için kalite emri 4</span><span class="sxs-lookup"><span data-stu-id="9cdec-317">Quality order 4 for 1 of batch number b4, serial number s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="9cdec-318">Bir toplu iş numarası ve bir seri numarasına referans olmadan, 2 için kalite emri 5.</span><span class="sxs-lookup"><span data-stu-id="9cdec-318">Quality order 5 for 2, without a reference to a batch number and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="9cdec-319">6 için tamamlanmış haliyle: toplu iş numarası b5, seri numarası s5 için 1; toplu iş numarası b6, seri numarası s6 için 1; toplu iş numarası b7, seri numara s7 için 1; toplu iş numarası b8, seri numarası s8 için 1; toplu iş numarası b9, seri numarası s9 için 1 ve toplu iş numarası b10, seri numarası s10 için 1</span><span class="sxs-lookup"><span data-stu-id="9cdec-319">Report as finished for 6: 1 for batch number b5, serial number s5; 1 for batch number b6, serial number s6; 1 for batch number b7, serial number s7; 1 for batch number b8, serial number s8; 1 for batch number b9, serial number s9; and 1 for batch number b10, serial number s10</span></span>
<ul>
<li><span data-ttu-id="9cdec-320">Kalite emri oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="9cdec-320">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="9cdec-321">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="9cdec-321">Additional resources</span></span>

- [<span data-ttu-id="9cdec-322">Kalite yönetimi işlemleri</span><span class="sxs-lookup"><span data-stu-id="9cdec-322">Quality management processes</span></span>](quality-management-processes.md)
- [<span data-ttu-id="9cdec-323">Kalite ve uygunsuzluk yönetimini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="9cdec-323">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="9cdec-324">Ambar işlemleri için kalite yönetimi</span><span class="sxs-lookup"><span data-stu-id="9cdec-324">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
