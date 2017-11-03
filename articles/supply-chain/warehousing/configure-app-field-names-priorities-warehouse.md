---
title: "Ambarlama uygulaması içerisinde alan adlarını yapılandırma"
description: "Bu konu, Finance and Operations için ambar uygulaması alan adlarını ve önceliklerini tanımlamayı ve yapılandırmayı açıklamaktadır."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2fbf9d84fa0fec32004936542003115cf580d91c
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="configure-app-field-names-in-warehousing-app"></a><span data-ttu-id="564c9-103">Ambarlama uygulaması içerisinde alan adlarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="564c9-103">Configure app field names in Warehousing app</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="564c9-104">Bu konu, Finance and Operations için ambar uygulaması alan adlarını ve önceliklerini tanımlamayı ve yapılandırmayı açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="564c9-104">This topic describes how to define and configure warehouse app field names and priorities in Finance and Operations.</span></span> 

<span data-ttu-id="564c9-105">**Not:** Bu konu, Ambar yönetimindeki özellikler için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="564c9-105">**Note:** This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="564c9-106">Stok yönetimindeki özellikler için geçerli değildir.</span><span class="sxs-lookup"><span data-stu-id="564c9-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="564c9-107">Finance and Operations - Ambarlama, ambar görevlerini gerçekleştirmek için kullanabileceğiniz bir uygulamadır.</span><span class="sxs-lookup"><span data-stu-id="564c9-107">Finance and Operations - Warehousing is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="564c9-108">Uygulama içerisinde kullanılan alan adlarını tanımlayabilir ve yapılandırabilirsiniz ve ayrıca alan adlarının atanacağı önceliği de yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="564c9-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="564c9-109">Bu konu, bu ambar uygulamaların alan adlarını ve önceliklerini nasıl tanımlayacağını ve yapılandıracağını ve bunların Finance and Operations - Ambarlama içerisinde nasıl kullanıldıklarını açıklar.</span><span class="sxs-lookup"><span data-stu-id="564c9-109">This topic explains how to define and configure these warehouse app field names and priorities, and how they are used in Finance and Operations - Warehousing.</span></span> <span data-ttu-id="564c9-110">Finance and Operations - Ambarlama'ya bağlantıyı yapılandırmak hakkında ayrıntılı bilgi için şu kılavuza bakınız [Finance and Operations - Ambarlama'yı kurma ve yapılandırma](install-configure-warehousing-app.md).</span><span class="sxs-lookup"><span data-stu-id="564c9-110">For detailed information about how to configure the connection to Finance and Operations  - Warehousing, refer to the tutorial [Install and configure Finance and Operations - Warehousing](install-configure-warehousing-app.md).</span></span>

<a name="configure-warehouse-app-field-names"></a><span data-ttu-id="564c9-111">Ambar uygulaması alan adlarını yapılandırın</span><span class="sxs-lookup"><span data-stu-id="564c9-111">Configure warehouse app field names</span></span>
===================================

<span data-ttu-id="564c9-112">Finance and Operations - Ambarlama'yı mobil cihazınızda kullandığınızda, meta verini cihazınızda nasıl görüntüleceğini **Ambar uygulaması alan adları** sayfasından ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="564c9-112">When you use Finance and Operations - Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="564c9-113">Finance and Operations içerisindeki yeni bir şirkette ambar mobil cihaz iş akışlarında kullanılacak tüm alan adlarını oluşturmak için **Varsayılan kurulum oluşturma**'yı seçin ve daha sonra tercih edilen giriş modunu ve giriş türünü bunlara atayın.</span><span class="sxs-lookup"><span data-stu-id="564c9-113">In a new company in Finance and Operations, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="564c9-114">Tüm alan adlarını oluşturduktan sonra, aşağıdaki giriş seçeneklerini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="564c9-114">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="564c9-115">Seçenek</span><span class="sxs-lookup"><span data-stu-id="564c9-115">Option</span></span></th>
<th><span data-ttu-id="564c9-116">Açıklama</span><span class="sxs-lookup"><span data-stu-id="564c9-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="564c9-117">Tercih edilen giriş modu</span><span class="sxs-lookup"><span data-stu-id="564c9-117">Preferred input mode</span></span></td>
<td><span data-ttu-id="564c9-118">Bu seçenek, seçilen alan adı için bir tarama alanının mı yoksa elle girdi girişi alanının mı gösterileceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="564c9-118">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="564c9-119">Bu, barkodlar alanda kullanılıyorsa alanların ayırt edilmesi için kullanışlıdır.</span><span class="sxs-lookup"><span data-stu-id="564c9-119">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="564c9-120"><strong>Not:</strong> Tercih edilen giriş modu <strong>Tarama</strong> olarak ayarlanmış alanlar için, barkod okunamaz veya zarar görmüşse, bilgileri el ile girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="564c9-120"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="564c9-121">Giriş türü</span><span class="sxs-lookup"><span data-stu-id="564c9-121">Input type</span></span></td>
<td><span data-ttu-id="564c9-122">Bu seçenek, seçilen alan adı için hangi giriş türünün kullanılacağını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="564c9-122">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="564c9-123">Dört seçenek kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="564c9-123">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="564c9-124"><strong>Seçim</strong> - Aralarından seçim yapabileceğiniz seçeneklerin listesini içerir.</span><span class="sxs-lookup"><span data-stu-id="564c9-124"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="564c9-125">Bu seçenekle alan adları düzenlenebilir değildir.</span><span class="sxs-lookup"><span data-stu-id="564c9-125">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="564c9-126"><strong>Tarih</strong> - Tarih olarak belirtilen alan adları etiket ile bir tarih biçimi gösterir.</span><span class="sxs-lookup"><span data-stu-id="564c9-126"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="564c9-127">Bu, ambar çalışanlarının tarihi hangi biçimde gireceklerini görmelerine yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="564c9-127">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="564c9-128">Bu seçenekle alan adları düzenlenebilir değildir.</span><span class="sxs-lookup"><span data-stu-id="564c9-128">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="564c9-129"><strong>Alfa</strong> - Seçiliyse, cihazın klavyesi bilgiyi uygulamaya el ile girmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="564c9-129"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="564c9-130">Klavye deneyimi, hangi cihazın kullanıldığına göre değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="564c9-130">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="564c9-131"><strong>Sayısal</strong> - Yalnızca sayısal giriş kullanan alan adları için giriş alanında cihaz klavyesi yerine özel bir sayısal klavye görüntülemek için bu seçeneği kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="564c9-131"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="564c9-132">Ambar uygulaması alan önceliğini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="564c9-132">Configure warehouse app field priority</span></span>
======================================

<span data-ttu-id="564c9-133">**Ambar uygulaması alan önceliği** sayfasında, alan adlarını farklı öncelik gruplarına yerleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="564c9-133">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="564c9-134">Ambar çalışanları uygulamayı kullanırlarken ana görev sayfasında hangi bilginin gösterileceğini belirlemeyi mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="564c9-134">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="564c9-135">**Varsayılan kurulum oluştur** üzerine tıklarsanız, öncelik gruplarının varsayılan bir kümesi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="564c9-135">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="564c9-136">İhtiyaç duyulduğu kadar öncelik grubu oluşturmak mümkündür, ancak görev sayfasında sadece üç öncelik grubu gösterilir.</span><span class="sxs-lookup"><span data-stu-id="564c9-136">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="564c9-137">Finance and Operations uygulamaya meta veri gönderdiğinde her alanın öncelik grubuna göre bir göreceli öncelik atar ve uygulama, görev sayfası içerisindeki meta veride içerilen ilk üç öncelik grubunu görüntüler.</span><span class="sxs-lookup"><span data-stu-id="564c9-137">When Finance and Operations sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="564c9-138">Taşan meta verinin geri kalanı, ikincil ayrıntılar sayfasında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="564c9-138">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="564c9-139">Aşağıdaki tablo beş öncelik grubu örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="564c9-139">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="564c9-140">Önceli grubu</span><span class="sxs-lookup"><span data-stu-id="564c9-140">Priority group</span></span></th>
<th><span data-ttu-id="564c9-141">Atanan alanlar</span><span class="sxs-lookup"><span data-stu-id="564c9-141">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="564c9-142">Ölçüt 10</span><span class="sxs-lookup"><span data-stu-id="564c9-142">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="564c9-143">Madde</span><span class="sxs-lookup"><span data-stu-id="564c9-143">Item</span></span></li>
<li><span data-ttu-id="564c9-144">Miktar</span><span class="sxs-lookup"><span data-stu-id="564c9-144">Quantity</span></span></li>
<li><span data-ttu-id="564c9-145">Ölçü birimi</span><span class="sxs-lookup"><span data-stu-id="564c9-145">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="564c9-146">Ölçüt 20</span><span class="sxs-lookup"><span data-stu-id="564c9-146">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="564c9-147">Küme konumu</span><span class="sxs-lookup"><span data-stu-id="564c9-147">Cluster position</span></span></li>
<li><span data-ttu-id="564c9-148">Küme</span><span class="sxs-lookup"><span data-stu-id="564c9-148">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="564c9-149">Ölçüt 30</span><span class="sxs-lookup"><span data-stu-id="564c9-149">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="564c9-150">Madde açıklaması</span><span class="sxs-lookup"><span data-stu-id="564c9-150">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="564c9-151">Ölçüt 40</span><span class="sxs-lookup"><span data-stu-id="564c9-151">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="564c9-152">Yapılandırma</span><span class="sxs-lookup"><span data-stu-id="564c9-152">Configuration</span></span></li>
<li><span data-ttu-id="564c9-153">Renk</span><span class="sxs-lookup"><span data-stu-id="564c9-153">Color</span></span></li>
<li><span data-ttu-id="564c9-154">Ebat</span><span class="sxs-lookup"><span data-stu-id="564c9-154">Size</span></span></li>
<li><span data-ttu-id="564c9-155">Stil</span><span class="sxs-lookup"><span data-stu-id="564c9-155">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="564c9-156">Ölçüt 50</span><span class="sxs-lookup"><span data-stu-id="564c9-156">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="564c9-157">Yer</span><span class="sxs-lookup"><span data-stu-id="564c9-157">Location</span></span></li>
<li><span data-ttu-id="564c9-158">Plaka</span><span class="sxs-lookup"><span data-stu-id="564c9-158">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="564c9-159">Örneğin bir ambar çalışanı mobil cihaz üzerinde bir görev yerine getirdiğinde, uygulamada görüntülenen meta veri aşağıdaki alanlardan oluşuyorsa:</span><span class="sxs-lookup"><span data-stu-id="564c9-159">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="564c9-160">Madde</span><span class="sxs-lookup"><span data-stu-id="564c9-160">Item</span></span>
-   <span data-ttu-id="564c9-161">Miktar</span><span class="sxs-lookup"><span data-stu-id="564c9-161">Quantity</span></span>
-   <span data-ttu-id="564c9-162">Ölçü birimi</span><span class="sxs-lookup"><span data-stu-id="564c9-162">Unit of measure</span></span>
-   <span data-ttu-id="564c9-163">Madde açıklaması</span><span class="sxs-lookup"><span data-stu-id="564c9-163">Item description</span></span>
-   <span data-ttu-id="564c9-164">Boyut ve Konum</span><span class="sxs-lookup"><span data-stu-id="564c9-164">Size and Location</span></span>

<span data-ttu-id="564c9-165">Yukarıdaki tabloda ayarlanmış olan ambar uygulaması alan öncelik kümesine dayanarak, aşağıdaki 3 bilgi satırı görev sayfasında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="564c9-165">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="564c9-166">Satır 1: Madde, Miktar ve Ölçü Birimi</span><span class="sxs-lookup"><span data-stu-id="564c9-166">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="564c9-167">Satır 2: Madde açıklaması</span><span class="sxs-lookup"><span data-stu-id="564c9-167">Row 2: Item description</span></span>
-   <span data-ttu-id="564c9-168">Satır 3: Boyut</span><span class="sxs-lookup"><span data-stu-id="564c9-168">Row 3: Size</span></span>

<span data-ttu-id="564c9-169">Kalan meta veri, örneğin Konum, görev sayfasında görüntülenmeyecektir, ancak bir ayrıntılar sayfasında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="564c9-169">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="564c9-170">Kullanıcı arabirimi hakkında daha fazla bilgi almak ve örnekler görmek için şu blog gönderisine bakın [Finance and Operations - Ambarlama](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/)</span><span class="sxs-lookup"><span data-stu-id="564c9-170">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

<a name="see-also"></a><span data-ttu-id="564c9-171">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="564c9-171">See also</span></span>
--------

[<span data-ttu-id="564c9-172">Microsoft Dynamics 365 for Finance and Operations – Ambarlama yükleme ve yapılandırma</span><span class="sxs-lookup"><span data-stu-id="564c9-172">Install and configure Microsoft Dynamics 365 for Finance and Operations – Warehousing</span></span>](install-configure-warehousing-app.md)




