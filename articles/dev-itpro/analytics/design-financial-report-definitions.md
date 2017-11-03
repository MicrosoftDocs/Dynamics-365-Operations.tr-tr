---
title: "Finansal rapor tasarımcısında rapor tanımları"
description: "Bu makalede rapor tanımları hakkında bilgi verilmektedir. Bir rapor tanımı, bir satır tanımı, bir sütun tanımı ve rapor oluşturmak için isteğe bağlı bir raporlama ağacı tanımı kullanılan bir rapor bileşenidir (veya yapı taşıdır). Bir rapor tanımı ayrıca bir raporu özelleştirmek için kullanılan seçenek ve ayarlar sunar."
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
ms.search.scope: Operations, Core
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 58030df8db467f754ec93ecc3f41585b20f03893
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="7a0d9-105">Finansal rapor tasarımcısında rapor tanımları</span><span class="sxs-lookup"><span data-stu-id="7a0d9-105">Report definitions in financial report designer</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="7a0d9-106">Bu makalede rapor tanımları hakkında bilgi verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="7a0d9-106">This article provides information about report definitions.</span></span> <span data-ttu-id="7a0d9-107">Bir rapor tanımı, bir satır tanımı, bir sütun tanımı ve rapor oluşturmak için isteğe bağlı bir raporlama ağacı tanımı kullanılan bir rapor bileşenidir (veya yapı taşıdır).</span><span class="sxs-lookup"><span data-stu-id="7a0d9-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="7a0d9-108">Bir rapor tanımı ayrıca bir raporu özelleştirmek için kullanılan seçenek ve ayarlar sunar.</span><span class="sxs-lookup"><span data-stu-id="7a0d9-108">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="7a0d9-109">Bir rapor tanımı bir rapor oluşturmak üzere bir satır tanımı, bir sütun tanımı ve bir opsiyonel raporlama ağacı tanımı kullanan bir rapor bileşenidir (veya yapı taşıdır).</span><span class="sxs-lookup"><span data-stu-id="7a0d9-109">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="7a0d9-110">Ayrıca bir rapor tanımı, bir raporu özelleştirmek için kullanabileceğiniz seçenekler ve ayarlar sağlar.</span><span class="sxs-lookup"><span data-stu-id="7a0d9-110">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="7a0d9-111">Satır tanımları ile sütun tanımlarını belirlemenizin ardından, bunları bir rapor tanımında birleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="7a0d9-111">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="7a0d9-112">Bu noktada, ayrıntı düzeyi ve rapor tarihi gibi diğer tanım yönlerini de tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="7a0d9-112">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="7a0d9-113">Ardından kaydedebilir ve rapor oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7a0d9-113">You can then save and generate a report.</span></span> <span data-ttu-id="7a0d9-114">Mali raporlama aşağıdaki ayrıntı düzeylerini sunar:</span><span class="sxs-lookup"><span data-stu-id="7a0d9-114">Financial reporting offers the following levels of detail:</span></span>

-   <span data-ttu-id="7a0d9-115">Mali</span><span class="sxs-lookup"><span data-stu-id="7a0d9-115">Financial</span></span>
-   <span data-ttu-id="7a0d9-116">Finans ve Hesap</span><span class="sxs-lookup"><span data-stu-id="7a0d9-116">Financial and Account</span></span>
-   <span data-ttu-id="7a0d9-117">Finans, Hesap ve İşlem</span><span class="sxs-lookup"><span data-stu-id="7a0d9-117">Financial, Account, and Transaction</span></span>

<span data-ttu-id="7a0d9-118">Ancak, verilerin Microsoft Dynamics ERP sisteminde nasıl saklandığına bağlı olarak, hareket ayrıntıları raporlarda kullanılamayabilir.</span><span class="sxs-lookup"><span data-stu-id="7a0d9-118">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="7a0d9-119">Rapor tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="7a0d9-119">Create a report definition</span></span>
1.  <span data-ttu-id="7a0d9-120">Rapor Tasarımcısı'ndaki **Dosya** menüsünde, **Yeni**'ye tıklayın ve ardından **Rapor Tanımı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="7a0d9-120">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2.  <span data-ttu-id="7a0d9-121">**Rapor**, **Çıkış ve Dağıtım**, **Üst Bilgiler ve Alt Bilgiler** ve **Ayarlar** sekmelerinde ilgili bilgileri belirtin.</span><span class="sxs-lookup"><span data-stu-id="7a0d9-121">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="7a0d9-122">Bir rapor tanımının içerikleri</span><span class="sxs-lookup"><span data-stu-id="7a0d9-122">Contents of a report definition</span></span>
<span data-ttu-id="7a0d9-123">Aşağıdaki tabloda bir rapor tanımındaki sekmeler ve bilgilerin nasıl kullanıldığı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="7a0d9-123">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7a0d9-124">Sekme</span><span class="sxs-lookup"><span data-stu-id="7a0d9-124">Tab</span></span></th>
<th><span data-ttu-id="7a0d9-125">Açıklama</span><span class="sxs-lookup"><span data-stu-id="7a0d9-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7a0d9-126">Rapor</span><span class="sxs-lookup"><span data-stu-id="7a0d9-126">Report</span></span></td>
<td><span data-ttu-id="7a0d9-127">Rapor oluşturun, rapor yapılandırın veya var olan bir raporu değiştirin.</span><span class="sxs-lookup"><span data-stu-id="7a0d9-127">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a0d9-128">Çıkış ve Dağıtım</span><span class="sxs-lookup"><span data-stu-id="7a0d9-128">Output and Distribution</span></span></td>
<td><span data-ttu-id="7a0d9-129">Raporun çıkış türünü ve hedefini değiştirin.</span><span class="sxs-lookup"><span data-stu-id="7a0d9-129">Change the output type and destination of the report.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7a0d9-130">Üst Bilgiler ve Alt Bilgiler</span><span class="sxs-lookup"><span data-stu-id="7a0d9-130">Headers and Footers</span></span></td>
<td><span data-ttu-id="7a0d9-131">Raporun üst bilgilerini ve alt bilgilerini tanımlayıp biçimlendirin.</span><span class="sxs-lookup"><span data-stu-id="7a0d9-131">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="7a0d9-132">Örneğin, üstbilgiye veya altbilgiye metin veya resim ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7a0d9-132">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="7a0d9-133">Mali raporlama görüntülerde .bmp, .jpg ve .png dosyalarını destekler.</span><span class="sxs-lookup"><span data-stu-id="7a0d9-133">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="7a0d9-134">Şirket adı, rapor adı veya sayfa numarası gibi diğer bilgileri eklemek için otomatik metin kodlarını da ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7a0d9-134">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7a0d9-135">Ayarlar</span><span class="sxs-lookup"><span data-stu-id="7a0d9-135">Settings</span></span></td>
<td><span data-ttu-id="7a0d9-136">Aşağıdaki ayarlar gibi rapor tanımı ayarlarını belirtin:</span><span class="sxs-lookup"><span data-stu-id="7a0d9-136">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="7a0d9-137">Tutarları biçimlendirme ve yuvarlama</span><span class="sxs-lookup"><span data-stu-id="7a0d9-137">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="7a0d9-138">Ayrıntı raporlarını biçimlendirme</span><span class="sxs-lookup"><span data-stu-id="7a0d9-138">Format detail reports</span></span></li>
<li><span data-ttu-id="7a0d9-139">Raporlama ağaçlarını biçimlendirme</span><span class="sxs-lookup"><span data-stu-id="7a0d9-139">Format reporting trees</span></span></li>
<li><span data-ttu-id="7a0d9-140">Özel durum raporu oluşturma</span><span class="sxs-lookup"><span data-stu-id="7a0d9-140">Generate an exception report</span></span></li>
<li><span data-ttu-id="7a0d9-141">Para birimi dönüştürme belirtme</span><span class="sxs-lookup"><span data-stu-id="7a0d9-141">Specify currency conversion</span></span></li>
<li><span data-ttu-id="7a0d9-142">Alt toplam ve filtre hesap ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="7a0d9-142">Subtotal and filter account details</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a><span data-ttu-id="7a0d9-143">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="7a0d9-143">See also</span></span>
--------

[<span data-ttu-id="7a0d9-144">Mali raporlama</span><span class="sxs-lookup"><span data-stu-id="7a0d9-144">Financial reporting</span></span>](financial-reporting-intro.md)




