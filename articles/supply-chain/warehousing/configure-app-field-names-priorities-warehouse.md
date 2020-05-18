---
title: Ambarlama uygulaması içerisinde alan adlarını yapılandırma
description: Bu konu, Dynamics 365 Supply Chain Management için ambarlama uygulaması alan adlarını ve önceliklerini tanımlamayı ve yapılandırmayı açıklamaktadır.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0390900d97e74bb9fd8deac913b1606cb775aa7c
ms.sourcegitcommit: ffd845d4230646499b6f074cb43e69ab95787671
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2020
ms.locfileid: "3346411"
---
# <a name="configure-app-field-names-in-warehousing-app"></a><span data-ttu-id="f378f-103">Ambarlama uygulaması içerisinde alan adlarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="f378f-103">Configure app field names in Warehousing app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f378f-104">Bu konu, Dynamics 365 Supply Chain Management için ambarlama uygulaması alan adlarını ve önceliklerini tanımlamayı ve yapılandırmayı açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="f378f-104">This topic describes how to define and configure warehousing app field names and priorities in Dynamics 365 Supply Chain Management.</span></span> 

> [!NOTE]
> <span data-ttu-id="f378f-105">Bu konu, Ambar yönetimindeki özellikler için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="f378f-105">This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="f378f-106">Stok yönetimindeki özellikler için geçerli değildir.</span><span class="sxs-lookup"><span data-stu-id="f378f-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="f378f-107">Ambarlama, ambar görevlerini gerçekleştirmek için kullanabileceğiniz bir uygulamadır.</span><span class="sxs-lookup"><span data-stu-id="f378f-107">Warehousing is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="f378f-108">Uygulama içerisinde kullanılan alan adlarını tanımlayabilir ve yapılandırabilirsiniz ve ayrıca alan adlarının atanacağı önceliği de yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f378f-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="f378f-109">Bu konu, bu ambarlama uygulamaların alan adlarını ve önceliklerini nasıl tanımlayacağını ve yapılandıracağını ve bunların Ambarlama içerisinde nasıl kullanıldıklarını açıklar.</span><span class="sxs-lookup"><span data-stu-id="f378f-109">This topic explains how to define and configure these warehousing app field names and priorities, and how they are used in Warehousing.</span></span> <span data-ttu-id="f378f-110">Ambarlama'ya bağlantıyı yapılandırma hakkında ayrıntılı bilgi için [Ambarlama uygulamasını yükleme ve yapılandırmaya genel bakış](install-configure-warehousing-app.md) eğitimine bakın.</span><span class="sxs-lookup"><span data-stu-id="f378f-110">For detailed information about how to configure the connection to FWarehousing, refer to the tutorial [Install and configure the Warehousing app overview](install-configure-warehousing-app.md).</span></span>

## <a name="configure-warehousing-app-field-names"></a><span data-ttu-id="f378f-111">Ambarlama uygulaması alan adlarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="f378f-111">Configure warehousing app field names</span></span>

<span data-ttu-id="f378f-112">Ambarlama'yı mobil cihazınızda kullandığınızda, meta verini cihazınızda nasıl görüntüleceğini **Ambar uygulaması alan adları** sayfasından ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f378f-112">When you use Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="f378f-113">Yeni bir şirkette ambar mobil cihaz iş akışlarında kullanılacak tüm alan adlarını oluşturmak için **Varsayılan kurulum oluşturma**'yı seçin ve daha sonra tercih edilen giriş modunu ve giriş türünü bunlara atayın.</span><span class="sxs-lookup"><span data-stu-id="f378f-113">In a new company, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="f378f-114">Tüm alan adlarını oluşturduktan sonra, aşağıdaki giriş seçeneklerini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f378f-114">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f378f-115">Seçenek</span><span class="sxs-lookup"><span data-stu-id="f378f-115">Option</span></span></th>
<th><span data-ttu-id="f378f-116">Açıklama</span><span class="sxs-lookup"><span data-stu-id="f378f-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f378f-117">Tercih edilen giriş modu</span><span class="sxs-lookup"><span data-stu-id="f378f-117">Preferred input mode</span></span></td>
<td><span data-ttu-id="f378f-118">Bu seçenek, seçilen alan adı için bir tarama alanının mı yoksa elle girdi girişi alanının mı gösterileceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="f378f-118">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="f378f-119">Bu, barkodlar alanda kullanılıyorsa alanların ayırt edilmesi için kullanışlıdır.</span><span class="sxs-lookup"><span data-stu-id="f378f-119">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="f378f-120"><strong>Not:</strong> Tercih edilen giriş modu <strong>Tarama</strong> olarak ayarlanmış alanlar için, barkod okunamaz veya zarar görmüşse, bilgileri el ile girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f378f-120"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f378f-121">Giriş türü</span><span class="sxs-lookup"><span data-stu-id="f378f-121">Input type</span></span></td>
<td><span data-ttu-id="f378f-122">Bu seçenek, seçilen alan adı için hangi giriş türünün kullanılacağını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="f378f-122">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="f378f-123">Dört seçenek kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="f378f-123">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="f378f-124"><strong>Seçim</strong> - Aralarından seçim yapabileceğiniz seçeneklerin listesini içerir.</span><span class="sxs-lookup"><span data-stu-id="f378f-124"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="f378f-125">Bu seçenekle alan adları düzenlenebilir değildir.</span><span class="sxs-lookup"><span data-stu-id="f378f-125">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="f378f-126"><strong>Tarih</strong> - Tarih olarak belirtilen alan adları etiket ile bir tarih biçimi gösterir.</span><span class="sxs-lookup"><span data-stu-id="f378f-126"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="f378f-127">Bu, ambar çalışanlarının tarihi hangi biçimde gireceklerini görmelerine yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="f378f-127">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="f378f-128">Bu seçenekle alan adları düzenlenebilir değildir.</span><span class="sxs-lookup"><span data-stu-id="f378f-128">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="f378f-129"><strong>Alfa</strong> - Seçiliyse, cihazın klavyesi bilgiyi uygulamaya el ile girmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f378f-129"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="f378f-130">Klavye deneyimi, hangi cihazın kullanıldığına göre değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="f378f-130">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="f378f-131"><strong>Sayısal</strong> - Yalnızca sayısal giriş kullanan alan adları için giriş alanında cihaz klavyesi yerine özel bir sayısal klavye görüntülemek için bu seçeneği kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f378f-131"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehousing-app-field-priority"></a><span data-ttu-id="f378f-132">Ambarlama uygulaması alan önceliğini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="f378f-132">Configure warehousing app field priority</span></span>

<span data-ttu-id="f378f-133">**Ambar uygulaması alan önceliği** sayfasında, alan adlarını farklı öncelik gruplarına yerleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f378f-133">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="f378f-134">Ambar çalışanları uygulamayı kullanırlarken ana görev sayfasında hangi bilginin gösterileceğini belirlemeyi mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="f378f-134">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="f378f-135">**Varsayılan kurulum oluştur** üzerine tıklarsanız, öncelik gruplarının varsayılan bir kümesi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="f378f-135">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="f378f-136">İhtiyaç duyulduğu kadar öncelik grubu oluşturmak mümkündür, ancak görev sayfasında sadece üç öncelik grubu gösterilir.</span><span class="sxs-lookup"><span data-stu-id="f378f-136">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="f378f-137">Sistem uygulamaya meta veri gönderdiğinde her alanın öncelik grubuna göre bir göreceli öncelik atar ve uygulama, görev sayfası içerisindeki meta veride içerilen ilk üç öncelik grubunu görüntüler.</span><span class="sxs-lookup"><span data-stu-id="f378f-137">When the system sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="f378f-138">Taşan meta verinin geri kalanı, ikincil ayrıntılar sayfasında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="f378f-138">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="f378f-139">Aşağıdaki tablo beş öncelik grubu örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f378f-139">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f378f-140">Önceli grubu</span><span class="sxs-lookup"><span data-stu-id="f378f-140">Priority group</span></span></th>
<th><span data-ttu-id="f378f-141">Atanan alanlar</span><span class="sxs-lookup"><span data-stu-id="f378f-141">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="f378f-142">Ölçüt 10</span><span class="sxs-lookup"><span data-stu-id="f378f-142">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="f378f-143">Madde</span><span class="sxs-lookup"><span data-stu-id="f378f-143">Item</span></span></li>
<li><span data-ttu-id="f378f-144">Miktar</span><span class="sxs-lookup"><span data-stu-id="f378f-144">Quantity</span></span></li>
<li><span data-ttu-id="f378f-145">Ölçü birimi</span><span class="sxs-lookup"><span data-stu-id="f378f-145">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="f378f-146">Ölçüt 20</span><span class="sxs-lookup"><span data-stu-id="f378f-146">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="f378f-147">Küme konumu</span><span class="sxs-lookup"><span data-stu-id="f378f-147">Cluster position</span></span></li>
<li><span data-ttu-id="f378f-148">Küme</span><span class="sxs-lookup"><span data-stu-id="f378f-148">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="f378f-149">Ölçüt 30</span><span class="sxs-lookup"><span data-stu-id="f378f-149">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="f378f-150">Madde açıklaması</span><span class="sxs-lookup"><span data-stu-id="f378f-150">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="f378f-151">Ölçüt 40</span><span class="sxs-lookup"><span data-stu-id="f378f-151">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="f378f-152">Yapılandırma</span><span class="sxs-lookup"><span data-stu-id="f378f-152">Configuration</span></span></li>
<li><span data-ttu-id="f378f-153">Renk</span><span class="sxs-lookup"><span data-stu-id="f378f-153">Color</span></span></li>
<li><span data-ttu-id="f378f-154">Ebat</span><span class="sxs-lookup"><span data-stu-id="f378f-154">Size</span></span></li>
<li><span data-ttu-id="f378f-155">Stil</span><span class="sxs-lookup"><span data-stu-id="f378f-155">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="f378f-156">Ölçüt 50</span><span class="sxs-lookup"><span data-stu-id="f378f-156">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="f378f-157">Yer</span><span class="sxs-lookup"><span data-stu-id="f378f-157">Location</span></span></li>
<li><span data-ttu-id="f378f-158">Plaka</span><span class="sxs-lookup"><span data-stu-id="f378f-158">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f378f-159">Örneğin bir ambar çalışanı mobil cihaz üzerinde bir görev yerine getirdiğinde, uygulamada görüntülenen meta veri aşağıdaki alanlardan oluşuyorsa:</span><span class="sxs-lookup"><span data-stu-id="f378f-159">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="f378f-160">Madde</span><span class="sxs-lookup"><span data-stu-id="f378f-160">Item</span></span>
-   <span data-ttu-id="f378f-161">Miktar</span><span class="sxs-lookup"><span data-stu-id="f378f-161">Quantity</span></span>
-   <span data-ttu-id="f378f-162">Ölçü birimi</span><span class="sxs-lookup"><span data-stu-id="f378f-162">Unit of measure</span></span>
-   <span data-ttu-id="f378f-163">Madde açıklaması</span><span class="sxs-lookup"><span data-stu-id="f378f-163">Item description</span></span>
-   <span data-ttu-id="f378f-164">Boyut ve Konum</span><span class="sxs-lookup"><span data-stu-id="f378f-164">Size and Location</span></span>

<span data-ttu-id="f378f-165">Yukarıdaki tabloda ayarlanmış olan ambarlama uygulaması alan öncelik kümesine dayanarak, aşağıdaki 3 bilgi satırı görev sayfasında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="f378f-165">Based on the warehousing app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="f378f-166">Satır 1: Madde, Miktar ve Ölçü Birimi</span><span class="sxs-lookup"><span data-stu-id="f378f-166">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="f378f-167">Satır 2: Madde açıklaması</span><span class="sxs-lookup"><span data-stu-id="f378f-167">Row 2: Item description</span></span>
-   <span data-ttu-id="f378f-168">Satır 3: Boyut</span><span class="sxs-lookup"><span data-stu-id="f378f-168">Row 3: Size</span></span>

<span data-ttu-id="f378f-169">Kalan meta veri, örneğin Konum, görev sayfasında görüntülenmeyecektir, ancak bir ayrıntılar sayfasında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="f378f-169">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="f378f-170">Kullanıcı arabirimi hakkında daha fazla bilgi almak ve örnekler görmek için şu blog gönderisine bakın [Finance and Operations - Ambarlama](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span><span class="sxs-lookup"><span data-stu-id="f378f-170">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

<a name="additional-resources"></a><span data-ttu-id="f378f-171">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="f378f-171">Additional resources</span></span>
--------

[<span data-ttu-id="f378f-172">Ambarlama uygulamasını yükleme ve yapılandırmaya genel bakış</span><span class="sxs-lookup"><span data-stu-id="f378f-172">Install and configure the Warehousing app overview</span></span>](install-configure-warehousing-app.md)
