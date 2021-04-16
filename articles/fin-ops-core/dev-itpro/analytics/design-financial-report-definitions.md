---
title: Finansal rapor tasarımcısında rapor tanımları
description: Bu makalede rapor tanımları hakkında bilgi verilmektedir.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 52322453328814b06bacefb4829bb10bf9953186
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755456"
---
# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="b0002-103">Finansal rapor tasarımcısında rapor tanımları</span><span class="sxs-lookup"><span data-stu-id="b0002-103">Report definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b0002-104">Bu makalede rapor tanımları hakkında bilgi verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="b0002-104">This article provides information about report definitions.</span></span> <span data-ttu-id="b0002-105">Bir rapor tanımı, bir satır tanımı, bir sütun tanımı ve rapor oluşturmak için isteğe bağlı bir raporlama ağacı tanımı kullanılan bir rapor bileşenidir (veya yapı taşıdır).</span><span class="sxs-lookup"><span data-stu-id="b0002-105">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="b0002-106">Bir rapor tanımı ayrıca bir raporu özelleştirmek için kullanılan seçenek ve ayarlar sunar.</span><span class="sxs-lookup"><span data-stu-id="b0002-106">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="b0002-107">Bir rapor tanımı bir rapor oluşturmak üzere bir satır tanımı, bir sütun tanımı ve bir opsiyonel raporlama ağacı tanımı kullanan bir rapor bileşenidir (veya yapı taşıdır).</span><span class="sxs-lookup"><span data-stu-id="b0002-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="b0002-108">Ayrıca bir rapor tanımı, bir raporu özelleştirmek için kullanabileceğiniz seçenekler ve ayarlar sağlar.</span><span class="sxs-lookup"><span data-stu-id="b0002-108">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="b0002-109">Satır tanımları ile sütun tanımlarını belirlemenizin ardından, bunları bir rapor tanımında birleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b0002-109">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="b0002-110">Bu noktada, ayrıntı düzeyi ve rapor tarihi gibi diğer tanım yönlerini de tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="b0002-110">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="b0002-111">Ardından kaydedebilir ve rapor oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b0002-111">You can then save and generate a report.</span></span> <span data-ttu-id="b0002-112">Mali raporlama aşağıdaki ayrıntı düzeylerini sunar:</span><span class="sxs-lookup"><span data-stu-id="b0002-112">Financial reporting offers the following levels of detail:</span></span>

- <span data-ttu-id="b0002-113">Mali</span><span class="sxs-lookup"><span data-stu-id="b0002-113">Financial</span></span>
- <span data-ttu-id="b0002-114">Finans ve Hesap</span><span class="sxs-lookup"><span data-stu-id="b0002-114">Financial and Account</span></span>
- <span data-ttu-id="b0002-115">Mali, Hesap ve Hareket</span><span class="sxs-lookup"><span data-stu-id="b0002-115">Financial, Account, and Transaction</span></span>

<span data-ttu-id="b0002-116">Ancak, verilerin Microsoft Dynamics ERP sisteminde nasıl saklandığına bağlı olarak, hareket ayrıntıları raporlarda kullanılamayabilir.</span><span class="sxs-lookup"><span data-stu-id="b0002-116">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="b0002-117">Rapor tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="b0002-117">Create a report definition</span></span>
1. <span data-ttu-id="b0002-118">Rapor Tasarımcısı'ndaki **Dosya** menüsünde, **Yeni**'ye tıklayın ve ardından **Rapor Tanımı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="b0002-118">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2. <span data-ttu-id="b0002-119">**Rapor**, **Çıkış ve Dağıtım**, **Üst Bilgiler ve Alt Bilgiler** ve **Ayarlar** sekmelerinde ilgili bilgileri belirtin.</span><span class="sxs-lookup"><span data-stu-id="b0002-119">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="b0002-120">Bir rapor tanımının içerikleri</span><span class="sxs-lookup"><span data-stu-id="b0002-120">Contents of a report definition</span></span>
<span data-ttu-id="b0002-121">Aşağıdaki tabloda bir rapor tanımındaki sekmeler ve bilgilerin nasıl kullanıldığı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="b0002-121">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b0002-122">Sekme</span><span class="sxs-lookup"><span data-stu-id="b0002-122">Tab</span></span></th>
<th><span data-ttu-id="b0002-123">Açıklama</span><span class="sxs-lookup"><span data-stu-id="b0002-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b0002-124">Rapor</span><span class="sxs-lookup"><span data-stu-id="b0002-124">Report</span></span></td>
<td><span data-ttu-id="b0002-125">Rapor oluşturun, rapor yapılandırın veya var olan bir raporu değiştirin.</span><span class="sxs-lookup"><span data-stu-id="b0002-125">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b0002-126">Çıkış ve Dağıtım</span><span class="sxs-lookup"><span data-stu-id="b0002-126">Output and Distribution</span></span></td>
<td><span data-ttu-id="b0002-127">Raporun çıkış türünü ve hedefini değiştirin.</span><span class="sxs-lookup"><span data-stu-id="b0002-127">Change the output type and destination of the report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b0002-128">Üst Bilgiler ve Alt Bilgiler</span><span class="sxs-lookup"><span data-stu-id="b0002-128">Headers and Footers</span></span></td>
<td><span data-ttu-id="b0002-129">Raporun üst bilgilerini ve alt bilgilerini tanımlayıp biçimlendirin.</span><span class="sxs-lookup"><span data-stu-id="b0002-129">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="b0002-130">Örneğin, üstbilgiye veya altbilgiye metin veya resim ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b0002-130">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="b0002-131">Mali raporlama görüntülerde .bmp, .jpg ve .png dosyalarını destekler.</span><span class="sxs-lookup"><span data-stu-id="b0002-131">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="b0002-132">Şirket adı, rapor adı veya sayfa numarası gibi diğer bilgileri eklemek için otomatik metin kodlarını da ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b0002-132">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b0002-133">Ayarlar</span><span class="sxs-lookup"><span data-stu-id="b0002-133">Settings</span></span></td>
<td><span data-ttu-id="b0002-134">Aşağıdaki ayarlar gibi rapor tanımı ayarlarını belirtin:</span><span class="sxs-lookup"><span data-stu-id="b0002-134">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="b0002-135">Tutarları biçimlendirme ve yuvarlama</span><span class="sxs-lookup"><span data-stu-id="b0002-135">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="b0002-136">Ayrıntı raporlarını biçimlendirme</span><span class="sxs-lookup"><span data-stu-id="b0002-136">Format detail reports</span></span></li>
<li><span data-ttu-id="b0002-137">Raporlama ağaçlarını biçimlendirme</span><span class="sxs-lookup"><span data-stu-id="b0002-137">Format reporting trees</span></span></li>
<li><span data-ttu-id="b0002-138">Özel durum raporu oluşturma</span><span class="sxs-lookup"><span data-stu-id="b0002-138">Generate an exception report</span></span></li>
<li><span data-ttu-id="b0002-139">Para birimi dönüşümü belirtme</span><span class="sxs-lookup"><span data-stu-id="b0002-139">Specify currency conversion</span></span></li>
<li><span data-ttu-id="b0002-140">Alt toplam ve filtre hesabı ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="b0002-140">Subtotal and filter account details</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="b0002-141">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b0002-141">Additional resources</span></span>

[<span data-ttu-id="b0002-142">Mali raporlama</span><span class="sxs-lookup"><span data-stu-id="b0002-142">Financial reporting</span></span>](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]