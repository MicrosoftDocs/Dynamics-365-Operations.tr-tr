---
title: "Finansal rapor tasarımcısında rapor tanımları"
description: "Bu makalede rapor tanımları hakkında bilgi verilmektedir. Bir rapor tanımı bir rapor oluşturmak üzere bir satır tanımı, bir sütun tanımı ve bir opsiyonel raporlama ağacı tanımı kullanan bir rapor bileşenidir (veya yapı taşıdır). Bir rapor tanımı ayrıca bir raporu özelleştirmek için kullanılan seçenek ve ayarlar sunar."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Management Reporter, UnifiedOperations, Core
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 96090a3ae15294d98d6207c8eb4a1e58429ca9eb
ms.contentlocale: tr-tr
ms.lasthandoff: 07/18/2017

---

# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="28ff0-105">Finansal rapor tasarımcısında rapor tanımları</span><span class="sxs-lookup"><span data-stu-id="28ff0-105">Report definitions in financial report designer</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="28ff0-106">Bu makalede rapor tanımları hakkında bilgi verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="28ff0-106">This article provides information about report definitions.</span></span> <span data-ttu-id="28ff0-107">Bir rapor tanımı bir rapor oluşturmak üzere bir satır tanımı, bir sütun tanımı ve bir opsiyonel raporlama ağacı tanımı kullanan bir rapor bileşenidir (veya yapı taşıdır).</span><span class="sxs-lookup"><span data-stu-id="28ff0-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="28ff0-108">Bir rapor tanımı ayrıca bir raporu özelleştirmek için kullanılan seçenek ve ayarlar sunar.</span><span class="sxs-lookup"><span data-stu-id="28ff0-108">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="28ff0-109">Bir rapor tanımı bir rapor oluşturmak üzere bir satır tanımı, bir sütun tanımı ve bir opsiyonel raporlama ağacı tanımı kullanan bir rapor bileşenidir (veya yapı taşıdır).</span><span class="sxs-lookup"><span data-stu-id="28ff0-109">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="28ff0-110">Bir rapor tanımı, ayrıca raporun özelleştirilmesi için kullanabileceğiniz ilave seçenekler ve ayarlar da sağlar.</span><span class="sxs-lookup"><span data-stu-id="28ff0-110">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="28ff0-111">Satır tanımlarını ve sütun tanımları tanımladıktan sonra rapor tanımında birleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="28ff0-111">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="28ff0-112">Bu noktada, ayrıntı düzeyi ve rapor tarihi gibi diğer tanım yönlerini de tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="28ff0-112">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="28ff0-113">Ardından kaydedebilir ve rapor oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="28ff0-113">You can then save and generate a report.</span></span> <span data-ttu-id="28ff0-114">Mali raporlama aşağıdaki ayrıntı düzeylerini sunar:</span><span class="sxs-lookup"><span data-stu-id="28ff0-114">Financial reporting offers the following levels of detail:</span></span>

-   <span data-ttu-id="28ff0-115">Mali</span><span class="sxs-lookup"><span data-stu-id="28ff0-115">Financial</span></span>
-   <span data-ttu-id="28ff0-116">Finans ve Hesap</span><span class="sxs-lookup"><span data-stu-id="28ff0-116">Financial and Account</span></span>
-   <span data-ttu-id="28ff0-117">Finans, Hesap ve İşlem</span><span class="sxs-lookup"><span data-stu-id="28ff0-117">Financial, Account, and Transaction</span></span>

<span data-ttu-id="28ff0-118">Ancak, verilerin Microsoft Dynamics ERP sisteminde nasıl depolandığına bağlı olarak, işlem ayrıntıları raporlarda mevcut olmayabilir.</span><span class="sxs-lookup"><span data-stu-id="28ff0-118">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="28ff0-119">Rapor tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="28ff0-119">Create a report definition</span></span>
1.  <span data-ttu-id="28ff0-120">Rapor Tasarımcısı'nda **Dosya** menüsünde **Yeni** seçeneğini tıklatın ve sonra **Rapor Tanımı** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="28ff0-120">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2.  <span data-ttu-id="28ff0-121">**Rapor**, **Çıktı ve Dağıtım**, **Üstbilgiler ve Altbilgiler** ve **Ayarlar** sekmelerinde uygun bilgileri belirtin.</span><span class="sxs-lookup"><span data-stu-id="28ff0-121">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="28ff0-122">Bir rapor tanımı içeriği</span><span class="sxs-lookup"><span data-stu-id="28ff0-122">Contents of a report definition</span></span>
<span data-ttu-id="28ff0-123">Aşağıdaki tablo, rapor tanımı sekmeleirni ve bilgilerin nasıl kullanıldığını açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="28ff0-123">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="28ff0-124">Sekme</span><span class="sxs-lookup"><span data-stu-id="28ff0-124">Tab</span></span></th>
<th><span data-ttu-id="28ff0-125">Açıklama</span><span class="sxs-lookup"><span data-stu-id="28ff0-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="28ff0-126">Rapor</span><span class="sxs-lookup"><span data-stu-id="28ff0-126">Report</span></span></td>
<td><span data-ttu-id="28ff0-127">Rapor oluşturma, rapor yapılandırma veya varolan bir raporu değiştirme.</span><span class="sxs-lookup"><span data-stu-id="28ff0-127">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="28ff0-128">Çıktı ve Dağıtım</span><span class="sxs-lookup"><span data-stu-id="28ff0-128">Output and Distribution</span></span></td>
<td><span data-ttu-id="28ff0-129">Çıktı türünü ve rapor hedefini değiştirin.</span><span class="sxs-lookup"><span data-stu-id="28ff0-129">Change the output type and destination of the report.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="28ff0-130">Üst Bilgiler ve Alt bilgiler</span><span class="sxs-lookup"><span data-stu-id="28ff0-130">Headers and Footers</span></span></td>
<td><span data-ttu-id="28ff0-131">Rapor için üst bilgileri ve alt bilgileri tanımlayın ve biçimlendirin.</span><span class="sxs-lookup"><span data-stu-id="28ff0-131">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="28ff0-132">Örneğin, üstbilgiye veya altbilgiye metin veya resim ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="28ff0-132">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="28ff0-133">Mali raporlama görüntülerde .bmp, .jpg ve .png dosyalarını destekler.</span><span class="sxs-lookup"><span data-stu-id="28ff0-133">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="28ff0-134">Şirket adı, rapor adı veya sayfa numarası gibi diğer bilgileri eklemek için otomatik metin kodlarını da ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="28ff0-134">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="28ff0-135">Ayarlar</span><span class="sxs-lookup"><span data-stu-id="28ff0-135">Settings</span></span></td>
<td><span data-ttu-id="28ff0-136">Aşağıdaki ayarları gibi rapor tanımı ayarlarını belirtin:</span><span class="sxs-lookup"><span data-stu-id="28ff0-136">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="28ff0-137">Biçimlendirme ve tutarların yuvarlanması</span><span class="sxs-lookup"><span data-stu-id="28ff0-137">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="28ff0-138">Ayrıntı raporlarını biçimlendirme</span><span class="sxs-lookup"><span data-stu-id="28ff0-138">Format detail reports</span></span></li>
<li><span data-ttu-id="28ff0-139">Raporlama ağaçlarını biçimlendirme</span><span class="sxs-lookup"><span data-stu-id="28ff0-139">Format reporting trees</span></span></li>
<li><span data-ttu-id="28ff0-140">Özel durum raporu oluşturma</span><span class="sxs-lookup"><span data-stu-id="28ff0-140">Generate an exception report</span></span></li>
<li><span data-ttu-id="28ff0-141">Para birimi dönüştürme belirtme</span><span class="sxs-lookup"><span data-stu-id="28ff0-141">Specify currency conversion</span></span></li>
<li><span data-ttu-id="28ff0-142">Alt toplam ve filtre hesap ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="28ff0-142">Subtotal and filter account details</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a><span data-ttu-id="28ff0-143">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="28ff0-143">See also</span></span>
--------

[<span data-ttu-id="28ff0-144">Mali raporlama</span><span class="sxs-lookup"><span data-stu-id="28ff0-144">Financial reporting</span></span>](financial-reporting-intro.md)




