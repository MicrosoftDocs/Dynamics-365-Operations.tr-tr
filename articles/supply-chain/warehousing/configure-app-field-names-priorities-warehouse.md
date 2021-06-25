---
title: Ambar Yönetimi mobil uygulaması için alanları yapılandırma
description: Bu konu, Ambar Yönetimi mobil uygulamasında gösterilen alan adlarını ve önceliklerini tanımlamayı ve yapılandırmayı açıklamaktadır.
author: MarkusFogelberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: bc224d3fd6cf5b111f61066202090f10ba4a7e8a
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189262"
---
# <a name="configure-fields-for-the-warehouse-management-mobile-app"></a><span data-ttu-id="61cbb-103">Ambar Yönetimi mobil uygulaması için alanları yapılandırma</span><span class="sxs-lookup"><span data-stu-id="61cbb-103">Configure fields for the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="61cbb-104">Bu konu, Ambar Yönetimi mobil uygulamasında gösterilen alan adlarını ve önceliklerini tanımlamayı ve yapılandırmayı açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="61cbb-104">This topic describes how to define and configure names and priorities of fields shown in the Warehouse Management mobile app.</span></span>

> [!NOTE]
> <span data-ttu-id="61cbb-105">Bu konu, Ambar yönetimindeki özellikler için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="61cbb-105">This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="61cbb-106">Stok yönetimindeki özellikler için geçerli değildir.</span><span class="sxs-lookup"><span data-stu-id="61cbb-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="61cbb-107">Ambar Yönetimi mobil uygulaması ambar görevlerini gerçekleştirmek için kullanabileceğiniz bir uygulamadır.</span><span class="sxs-lookup"><span data-stu-id="61cbb-107">The Warehouse Management mobile app is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="61cbb-108">Uygulama içerisinde kullanılan alan adlarını tanımlayabilir ve yapılandırabilirsiniz ve ayrıca alan adlarının atanacağı önceliği de yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="61cbb-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="61cbb-109">Bu konu, bu Ambar Yönetimi mobil uygulamalarının alan adlarını ve önceliklerini nasıl tanımlayacağını ve yapılandıracağını ve bunların nasıl kullanıldıklarını açıklar.</span><span class="sxs-lookup"><span data-stu-id="61cbb-109">This topic explains how to define and configure these Warehouse Management mobile app field names and priorities, and how they are used.</span></span>

## <a name="configure-warehouse-app-field-names"></a><span data-ttu-id="61cbb-110">Ambar uygulaması alan adlarını yapılandırın</span><span class="sxs-lookup"><span data-stu-id="61cbb-110">Configure warehouse app field names</span></span>

<span data-ttu-id="61cbb-111">Ambarlama'yı mobil cihazınızda kullandığınızda, meta verini cihazınızda nasıl görüntüleceğini **Ambar uygulaması alan adları** sayfasından ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="61cbb-111">When you use Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="61cbb-112">Yeni bir şirkette ambar mobil cihaz iş akışlarında kullanılacak tüm alan adlarını oluşturmak için **Varsayılan kurulum oluşturma**'yı seçin ve daha sonra tercih edilen giriş modunu ve giriş türünü bunlara atayın.</span><span class="sxs-lookup"><span data-stu-id="61cbb-112">In a new company, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="61cbb-113">Tüm alan adlarını oluşturduktan sonra, aşağıdaki giriş seçeneklerini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="61cbb-113">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="61cbb-114">Seçenek</span><span class="sxs-lookup"><span data-stu-id="61cbb-114">Option</span></span></th>
<th><span data-ttu-id="61cbb-115">Açıklama</span><span class="sxs-lookup"><span data-stu-id="61cbb-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="61cbb-116">Tercih edilen giriş modu</span><span class="sxs-lookup"><span data-stu-id="61cbb-116">Preferred input mode</span></span></td>
<td><span data-ttu-id="61cbb-117">Bu seçenek, seçilen alan adı için bir tarama alanının mı yoksa elle girdi girişi alanının mı gösterileceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="61cbb-117">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="61cbb-118">Bu, barkodlar alanda kullanılıyorsa alanların ayırt edilmesi için kullanışlıdır.</span><span class="sxs-lookup"><span data-stu-id="61cbb-118">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="61cbb-119"><strong>Not:</strong> Tercih edilen giriş modu <strong>Tarama</strong> olarak ayarlanmış alanlar için, barkod okunamaz veya zarar görmüşse, bilgileri el ile girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="61cbb-119"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61cbb-120">Giriş türü</span><span class="sxs-lookup"><span data-stu-id="61cbb-120">Input type</span></span></td>
<td><span data-ttu-id="61cbb-121">Bu seçenek, seçilen alan adı için hangi giriş türünün kullanılacağını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="61cbb-121">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="61cbb-122">Dört seçenek kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="61cbb-122">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="61cbb-123"><strong>Seçim</strong> - Aralarından seçim yapabileceğiniz seçeneklerin listesini içerir.</span><span class="sxs-lookup"><span data-stu-id="61cbb-123"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="61cbb-124">Bu seçenekle alan adları düzenlenebilir değildir.</span><span class="sxs-lookup"><span data-stu-id="61cbb-124">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="61cbb-125"><strong>Tarih</strong> - Tarih olarak belirtilen alan adları etiket ile bir tarih biçimi gösterir.</span><span class="sxs-lookup"><span data-stu-id="61cbb-125"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="61cbb-126">Bu, ambar çalışanlarının tarihi hangi biçimde gireceklerini görmelerine yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="61cbb-126">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="61cbb-127">Bu seçenekle alan adları düzenlenebilir değildir.</span><span class="sxs-lookup"><span data-stu-id="61cbb-127">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="61cbb-128"><strong>Alfa</strong> - Seçiliyse, cihazın klavyesi bilgiyi uygulamaya el ile girmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="61cbb-128"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="61cbb-129">Klavye deneyimi, hangi cihazın kullanıldığına göre değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="61cbb-129">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="61cbb-130"><strong>Sayısal</strong> - Yalnızca sayısal giriş kullanan alan adları için giriş alanında cihaz klavyesi yerine özel bir sayısal klavye görüntülemek için bu seçeneği kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="61cbb-130"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="61cbb-131">Ambar uygulaması alan önceliğini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="61cbb-131">Configure warehouse app field priority</span></span>

<span data-ttu-id="61cbb-132">**Ambar uygulaması alan önceliği** sayfasında, alan adlarını farklı öncelik gruplarına yerleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="61cbb-132">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="61cbb-133">Ambar çalışanları uygulamayı kullanırlarken ana görev sayfasında hangi bilginin gösterileceğini belirlemeyi mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="61cbb-133">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="61cbb-134">**Varsayılan kurulum oluştur** üzerine tıklarsanız, öncelik gruplarının varsayılan bir kümesi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="61cbb-134">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="61cbb-135">İhtiyaç duyulduğu kadar öncelik grubu oluşturmak mümkündür, ancak görev sayfasında sadece üç öncelik grubu gösterilir.</span><span class="sxs-lookup"><span data-stu-id="61cbb-135">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="61cbb-136">Sistem uygulamaya meta veri gönderdiğinde her alanın öncelik grubuna göre bir göreceli öncelik atar ve uygulama, görev sayfası içerisindeki meta veride içerilen ilk üç öncelik grubunu görüntüler.</span><span class="sxs-lookup"><span data-stu-id="61cbb-136">When the system sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="61cbb-137">Taşan meta verinin geri kalanı, ikincil ayrıntılar sayfasında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="61cbb-137">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="61cbb-138">Aşağıdaki tablo beş öncelik grubu örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="61cbb-138">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="61cbb-139">Önceli grubu</span><span class="sxs-lookup"><span data-stu-id="61cbb-139">Priority group</span></span></th>
<th><span data-ttu-id="61cbb-140">Atanan alanlar</span><span class="sxs-lookup"><span data-stu-id="61cbb-140">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="61cbb-141">Ölçüt 10</span><span class="sxs-lookup"><span data-stu-id="61cbb-141">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="61cbb-142">Madde</span><span class="sxs-lookup"><span data-stu-id="61cbb-142">Item</span></span></li>
<li><span data-ttu-id="61cbb-143">Miktar</span><span class="sxs-lookup"><span data-stu-id="61cbb-143">Quantity</span></span></li>
<li><span data-ttu-id="61cbb-144">Ölçü birimi</span><span class="sxs-lookup"><span data-stu-id="61cbb-144">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="61cbb-145">Ölçüt 20</span><span class="sxs-lookup"><span data-stu-id="61cbb-145">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="61cbb-146">Küme konumu</span><span class="sxs-lookup"><span data-stu-id="61cbb-146">Cluster position</span></span></li>
<li><span data-ttu-id="61cbb-147">Küme</span><span class="sxs-lookup"><span data-stu-id="61cbb-147">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="61cbb-148">Ölçüt 30</span><span class="sxs-lookup"><span data-stu-id="61cbb-148">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="61cbb-149">Madde açıklaması</span><span class="sxs-lookup"><span data-stu-id="61cbb-149">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="61cbb-150">Ölçüt 40</span><span class="sxs-lookup"><span data-stu-id="61cbb-150">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="61cbb-151">Yapılandırma</span><span class="sxs-lookup"><span data-stu-id="61cbb-151">Configuration</span></span></li>
<li><span data-ttu-id="61cbb-152">Renk</span><span class="sxs-lookup"><span data-stu-id="61cbb-152">Color</span></span></li>
<li><span data-ttu-id="61cbb-153">Ebat</span><span class="sxs-lookup"><span data-stu-id="61cbb-153">Size</span></span></li>
<li><span data-ttu-id="61cbb-154">Stil</span><span class="sxs-lookup"><span data-stu-id="61cbb-154">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="61cbb-155">Ölçüt 50</span><span class="sxs-lookup"><span data-stu-id="61cbb-155">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="61cbb-156">Yer</span><span class="sxs-lookup"><span data-stu-id="61cbb-156">Location</span></span></li>
<li><span data-ttu-id="61cbb-157">Plaka</span><span class="sxs-lookup"><span data-stu-id="61cbb-157">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="61cbb-158">Örneğin bir ambar çalışanı mobil cihaz üzerinde bir görev yerine getirdiğinde, uygulamada görüntülenen meta veri aşağıdaki alanlardan oluşuyorsa:</span><span class="sxs-lookup"><span data-stu-id="61cbb-158">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="61cbb-159">Madde</span><span class="sxs-lookup"><span data-stu-id="61cbb-159">Item</span></span>
-   <span data-ttu-id="61cbb-160">Miktar</span><span class="sxs-lookup"><span data-stu-id="61cbb-160">Quantity</span></span>
-   <span data-ttu-id="61cbb-161">Ölçü birimi</span><span class="sxs-lookup"><span data-stu-id="61cbb-161">Unit of measure</span></span>
-   <span data-ttu-id="61cbb-162">Madde açıklaması</span><span class="sxs-lookup"><span data-stu-id="61cbb-162">Item description</span></span>
-   <span data-ttu-id="61cbb-163">Boyut ve Konum</span><span class="sxs-lookup"><span data-stu-id="61cbb-163">Size and Location</span></span>

<span data-ttu-id="61cbb-164">Yukarıdaki tabloda ayarlanmış olan ambar uygulaması alan öncelik kümesine dayanarak, aşağıdaki 3 bilgi satırı görev sayfasında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="61cbb-164">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="61cbb-165">Satır 1: Madde, Miktar ve Ölçü Birimi</span><span class="sxs-lookup"><span data-stu-id="61cbb-165">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="61cbb-166">Satır 2: Madde açıklaması</span><span class="sxs-lookup"><span data-stu-id="61cbb-166">Row 2: Item description</span></span>
-   <span data-ttu-id="61cbb-167">Satır 3: Boyut</span><span class="sxs-lookup"><span data-stu-id="61cbb-167">Row 3: Size</span></span>

<span data-ttu-id="61cbb-168">Kalan meta veri, örneğin Konum, görev sayfasında görüntülenmeyecektir, ancak bir ayrıntılar sayfasında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="61cbb-168">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="61cbb-169">Kullanıcı arabirimi hakkında daha fazla bilgi almak ve örnekler görmek için şu blog gönderisine bakın [Finance and Operations - Ambarlama](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span><span class="sxs-lookup"><span data-stu-id="61cbb-169">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="61cbb-170">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="61cbb-170">Additional resources</span></span>

[<span data-ttu-id="61cbb-171">Ambar Yönetimi mobil uygulamasını yükleme ve bağlama</span><span class="sxs-lookup"><span data-stu-id="61cbb-171">Install and connect the Warehouse Management mobile app</span></span>](../warehousing/install-configure-warehouse-management-app.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]