---
title: Finansal rapor tasarımcısında rapor tanımları
description: Bu makalede rapor tanımları hakkında bilgi verilmektedir. Bir rapor tanımı, bir satır tanımı, bir sütun tanımı ve rapor oluşturmak için isteğe bağlı bir raporlama ağacı tanımı kullanılan bir rapor bileşenidir (veya yapı taşıdır). Bir rapor tanımı ayrıca bir raporu özelleştirmek için kullanılan seçenek ve ayarlar sunar.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 07f49e63fc2e0410d2673f3ca9378325e9b4ebf8
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174156"
---
# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="86b21-105">Finansal rapor tasarımcısında rapor tanımları</span><span class="sxs-lookup"><span data-stu-id="86b21-105">Report definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="86b21-106">Bu makalede rapor tanımları hakkında bilgi verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="86b21-106">This article provides information about report definitions.</span></span> <span data-ttu-id="86b21-107">Bir rapor tanımı, bir satır tanımı, bir sütun tanımı ve rapor oluşturmak için isteğe bağlı bir raporlama ağacı tanımı kullanılan bir rapor bileşenidir (veya yapı taşıdır).</span><span class="sxs-lookup"><span data-stu-id="86b21-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="86b21-108">Bir rapor tanımı ayrıca bir raporu özelleştirmek için kullanılan seçenek ve ayarlar sunar.</span><span class="sxs-lookup"><span data-stu-id="86b21-108">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="86b21-109">Bir rapor tanımı bir rapor oluşturmak üzere bir satır tanımı, bir sütun tanımı ve bir opsiyonel raporlama ağacı tanımı kullanan bir rapor bileşenidir (veya yapı taşıdır).</span><span class="sxs-lookup"><span data-stu-id="86b21-109">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="86b21-110">Ayrıca bir rapor tanımı, bir raporu özelleştirmek için kullanabileceğiniz seçenekler ve ayarlar sağlar.</span><span class="sxs-lookup"><span data-stu-id="86b21-110">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="86b21-111">Satır tanımları ile sütun tanımlarını belirlemenizin ardından, bunları bir rapor tanımında birleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="86b21-111">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="86b21-112">Bu noktada, ayrıntı düzeyi ve rapor tarihi gibi diğer tanım yönlerini de tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="86b21-112">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="86b21-113">Ardından kaydedebilir ve rapor oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="86b21-113">You can then save and generate a report.</span></span> <span data-ttu-id="86b21-114">Mali raporlama aşağıdaki ayrıntı düzeylerini sunar:</span><span class="sxs-lookup"><span data-stu-id="86b21-114">Financial reporting offers the following levels of detail:</span></span>

- <span data-ttu-id="86b21-115">Mali</span><span class="sxs-lookup"><span data-stu-id="86b21-115">Financial</span></span>
- <span data-ttu-id="86b21-116">Finans ve Hesap</span><span class="sxs-lookup"><span data-stu-id="86b21-116">Financial and Account</span></span>
- <span data-ttu-id="86b21-117">Mali, Hesap ve Hareket</span><span class="sxs-lookup"><span data-stu-id="86b21-117">Financial, Account, and Transaction</span></span>

<span data-ttu-id="86b21-118">Ancak, verilerin Microsoft Dynamics ERP sisteminde nasıl saklandığına bağlı olarak, hareket ayrıntıları raporlarda kullanılamayabilir.</span><span class="sxs-lookup"><span data-stu-id="86b21-118">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="86b21-119">Rapor tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="86b21-119">Create a report definition</span></span>
1. <span data-ttu-id="86b21-120">Rapor Tasarımcısı'ndaki **Dosya** menüsünde, **Yeni**'ye tıklayın ve ardından **Rapor Tanımı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="86b21-120">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2. <span data-ttu-id="86b21-121">**Rapor**, **Çıkış ve Dağıtım**, **Üst Bilgiler ve Alt Bilgiler** ve **Ayarlar** sekmelerinde ilgili bilgileri belirtin.</span><span class="sxs-lookup"><span data-stu-id="86b21-121">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="86b21-122">Bir rapor tanımının içerikleri</span><span class="sxs-lookup"><span data-stu-id="86b21-122">Contents of a report definition</span></span>
<span data-ttu-id="86b21-123">Aşağıdaki tabloda bir rapor tanımındaki sekmeler ve bilgilerin nasıl kullanıldığı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="86b21-123">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="86b21-124">Sekme</span><span class="sxs-lookup"><span data-stu-id="86b21-124">Tab</span></span></th>
<th><span data-ttu-id="86b21-125">Açıklama</span><span class="sxs-lookup"><span data-stu-id="86b21-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="86b21-126">Rapor</span><span class="sxs-lookup"><span data-stu-id="86b21-126">Report</span></span></td>
<td><span data-ttu-id="86b21-127">Rapor oluşturun, rapor yapılandırın veya var olan bir raporu değiştirin.</span><span class="sxs-lookup"><span data-stu-id="86b21-127">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86b21-128">Çıkış ve Dağıtım</span><span class="sxs-lookup"><span data-stu-id="86b21-128">Output and Distribution</span></span></td>
<td><span data-ttu-id="86b21-129">Raporun çıkış türünü ve hedefini değiştirin.</span><span class="sxs-lookup"><span data-stu-id="86b21-129">Change the output type and destination of the report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86b21-130">Üst Bilgiler ve Alt Bilgiler</span><span class="sxs-lookup"><span data-stu-id="86b21-130">Headers and Footers</span></span></td>
<td><span data-ttu-id="86b21-131">Raporun üst bilgilerini ve alt bilgilerini tanımlayıp biçimlendirin.</span><span class="sxs-lookup"><span data-stu-id="86b21-131">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="86b21-132">Örneğin, üstbilgiye veya altbilgiye metin veya resim ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="86b21-132">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="86b21-133">Mali raporlama görüntülerde .bmp, .jpg ve .png dosyalarını destekler.</span><span class="sxs-lookup"><span data-stu-id="86b21-133">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="86b21-134">Şirket adı, rapor adı veya sayfa numarası gibi diğer bilgileri eklemek için otomatik metin kodlarını da ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="86b21-134">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="86b21-135">Ayarlar</span><span class="sxs-lookup"><span data-stu-id="86b21-135">Settings</span></span></td>
<td><span data-ttu-id="86b21-136">Aşağıdaki ayarlar gibi rapor tanımı ayarlarını belirtin:</span><span class="sxs-lookup"><span data-stu-id="86b21-136">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="86b21-137">Tutarları biçimlendirme ve yuvarlama</span><span class="sxs-lookup"><span data-stu-id="86b21-137">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="86b21-138">Ayrıntı raporlarını biçimlendirme</span><span class="sxs-lookup"><span data-stu-id="86b21-138">Format detail reports</span></span></li>
<li><span data-ttu-id="86b21-139">Raporlama ağaçlarını biçimlendirme</span><span class="sxs-lookup"><span data-stu-id="86b21-139">Format reporting trees</span></span></li>
<li><span data-ttu-id="86b21-140">Özel durum raporu oluşturma</span><span class="sxs-lookup"><span data-stu-id="86b21-140">Generate an exception report</span></span></li>
<li><span data-ttu-id="86b21-141">Para birimi dönüşümü belirtme</span><span class="sxs-lookup"><span data-stu-id="86b21-141">Specify currency conversion</span></span></li>
<li><span data-ttu-id="86b21-142">Alt toplam ve filtre hesabı ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="86b21-142">Subtotal and filter account details</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="86b21-143">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="86b21-143">Additional resources</span></span>

[<span data-ttu-id="86b21-144">Mali raporlama</span><span class="sxs-lookup"><span data-stu-id="86b21-144">Financial reporting</span></span>](financial-reporting-intro.md)
