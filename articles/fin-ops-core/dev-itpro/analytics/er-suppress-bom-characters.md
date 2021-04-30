---
title: Oluşturulan dosyalardaki BOM karakterlerini gizlemek için ER yapılandırmaları tasarlama
description: Bu konuda, bayt sırası işaretlerini (BOM) gizleyen raporlar oluşturmak için Elektronik raporlama (ER) biçiminin nasıl yapılandırılacağı açıklanmaktadır.
author: NickSelin
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d5ada93c0192aadac70c38c8c8c4f3af86ff6fc3
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893288"
---
# <a name="design-er-configurations-to-suppress-bom-characters-in-generated-files"></a><span data-ttu-id="583c2-103">Oluşturulan dosyalardaki BOM karakterlerini gizlemek için ER yapılandırmaları tasarlama</span><span class="sxs-lookup"><span data-stu-id="583c2-103">Design ER configurations to suppress BOM characters in generated files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="583c2-104">Giden belgeler oluşturmak için bir [Elektronik raporlama (ER)](general-electronic-reporting.md) [çözümü](er-quick-start1-new-solution.md) tasarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="583c2-104">You can design an [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md) to generate outgoing documents.</span></span> <span data-ttu-id="583c2-105">Belgeleri metin veya XML dosyaları olarak oluşturmak için çözümde, ER [biçimi](general-electronic-reporting.md#FormatComponentOutbound) içeren bir ER [yapılandırması](general-electronic-reporting.md#Configuration) bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="583c2-105">To generate the documents as text or XML files, the solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="583c2-106">Oluşturulan dosyalardaki karakter kümesini temsil eden [karakter kodlamasını](/windows/win32/intl/character-sets) belirtmek için ER biçimi, **Common\\File** biçim öğesini içermelidir.</span><span class="sxs-lookup"><span data-stu-id="583c2-106">To specify the [character encoding](/windows/win32/intl/character-sets) that represents the set of characters in generated files, the ER format must contain the **Common\\File** format element.</span></span> <span data-ttu-id="583c2-107">ER biçim bileşenini yapılandırmak için ER biçim tasarımcısında ER yapılandırmasının [taslak](general-electronic-reporting.md#component-versioning) sürümünü açın ve **Common\\File** öğesini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="583c2-107">To configure the ER format component, open the [draft](general-electronic-reporting.md#component-versioning) version of the ER configuration in the ER format designer, and add the **Common\\File** element.</span></span> <span data-ttu-id="583c2-108">**Kodlama** alanında, bu bileşen kullanılarak çalışma zamanında oluşturulan giden dosyaların kodlamasını belirtin.</span><span class="sxs-lookup"><span data-stu-id="583c2-108">In the **Encoding** field, specify the encoding of outbound files that are generated at runtime by using this component.</span></span>

> [!NOTE]
> <span data-ttu-id="583c2-109">Biçim yanlış bir kodlama adı içeriyorsa değişikliklerinizi biçim ayarlarında kaydettiğinizde hata oluşur.</span><span class="sxs-lookup"><span data-stu-id="583c2-109">If the format contains an incorrect encoding name, an error is thrown when you save your changes to the format's settings.</span></span>

![Biçim tasarımcısı sayfasına kök öğe ekleme](./media/er-suppress-bom-characters-image1.gif)

<span data-ttu-id="583c2-111">Kodlama olarak **UTF-8**, **UTF-16** veya **UTF-32** kodlamalarını belirtirseniz **BOM karakterlerini gizle** seçeneği sunulur.</span><span class="sxs-lookup"><span data-stu-id="583c2-111">If you specify **UTF-8**, **UTF-16**, or **UTF-32** as the encoding, the **Suppress BOM characters** option becomes available.</span></span> <span data-ttu-id="583c2-112">Düzenlenebilir ER biçimi çalıştırıldığında çalışma zamanında oluşturulan giden dosyalarda [bayt sırası işareti (BOM) karakterlerini](/globalization/encoding/byte-order-mark) gizlemek için bu seçeneği **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="583c2-112">Set this option to **Yes** to suppress [byte order mark (BOM) characters](/globalization/encoding/byte-order-mark) in outbound files that are generated at runtime when the editable ER format is run.</span></span>

> [!NOTE]
> <span data-ttu-id="583c2-113">**Kodlama** alanını boş bırakırsanız varsayılan **UTF-8** kodlaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="583c2-113">If you leave the **Encoding** field blank, the default **UTF-8** encoding is used.</span></span>

![Biçim tasarımcısı sayfasında BOM karakterlerini gizle seçeneğini ayarlama](./media/er-suppress-bom-characters-image2.gif)

<span data-ttu-id="583c2-115">Çalışma zamanında işlevi incelemek için uygun yordamı tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="583c2-115">To review the functionality at runtime, complete the appropriate procedure.</span></span> <span data-ttu-id="583c2-116">Örneğin, [ER biçimindeki XML öğelerinin yürütülmesini erteleme](er-defer-xml-element.md) konusundaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="583c2-116">For example, complete the steps in the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic.</span></span> <span data-ttu-id="583c2-117">Konunun [Hesaplamada, oluşturulan çıktının temel alınması için biçimi değiştirme](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) bölümündeki adımları tamamladıktan sonra aşağıdaki ek adımları da izleyin.</span><span class="sxs-lookup"><span data-stu-id="583c2-117">After you've completed the steps in the [Modify the format so that the calculation is based on generated output](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) section of that topic, follow these additional steps.</span></span>

1. <span data-ttu-id="583c2-118">UTF kodlamasını belirtin:</span><span class="sxs-lookup"><span data-stu-id="583c2-118">Specify the UTF encoding:</span></span>

    1. <span data-ttu-id="583c2-119">**Common\\File** türünün **Rapor** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="583c2-119">Select the **Report** element of the **Common\\File** type.</span></span>
    2. <span data-ttu-id="583c2-120">**Kodlama** alanında **UTF-8** kodlamasını belirtin.</span><span class="sxs-lookup"><span data-stu-id="583c2-120">In the **Encoding** field, specify the **UTF-8** encoding.</span></span>

2. <span data-ttu-id="583c2-121">BOM karakteri içeren bir XML dosyası oluşturun:</span><span class="sxs-lookup"><span data-stu-id="583c2-121">Generate an XML file that includes a BOM character:</span></span>

    1. <span data-ttu-id="583c2-122">Oluşturulan XML dosyalarına BOM karakterlerini eklemek için **BOM karakterlerini gizle** seçeneğini **Hayır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="583c2-122">Set the **Suppress BOM characters** option to **No** to include BOM characters in generated XML files.</span></span>
    2. <span data-ttu-id="583c2-123">[ER biçimindeki XML öğelerinin yürütülmesini erteleme](er-defer-xml-element.md) konusunun [Hesaplanan toplamın kullanılmasını sağlamak için özet XML öğesinin yürütülmesini erteleme](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) bölümündeki adımları tamamlayın ve oluşturulan dosyayı **SampleXmlReport.xml** olarak kaydedin.</span><span class="sxs-lookup"><span data-stu-id="583c2-123">Complete the steps in the [Defer the execution of the summary XML element so that the calculated total is used](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) section of the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic, and save the generated file as **SampleXmlReport.xml**.</span></span>

3. <span data-ttu-id="583c2-124">BOM karakteri içermeyen bir XML dosyası oluşturun:</span><span class="sxs-lookup"><span data-stu-id="583c2-124">Generate an XML file that doesn't include a BOM character:</span></span>

    1. <span data-ttu-id="583c2-125">Oluşturulan XML dosyalarında BOM karakterlerini gizlemek için **BOM karakterlerini gizle** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="583c2-125">Set the **Suppress BOM characters** option to **Yes** to suppress BOM characters in generated XML files.</span></span>
    2. <span data-ttu-id="583c2-126">[ER biçimindeki XML öğelerinin yürütülmesini erteleme](er-defer-xml-element.md) konusunun [Hesaplanan toplamın kullanılmasını sağlamak için özet XML öğesinin yürütülmesini erteleme](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) bölümündeki adımları tamamlayın ve oluşturulan dosyayı **SampleXmlReport (1).xml** olarak kaydedin.</span><span class="sxs-lookup"><span data-stu-id="583c2-126">Complete the steps in the [Defer the execution of the summary XML element so that the calculated total is used](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) section of the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic, and save the generated file as **SampleXmlReport (1).xml**.</span></span>

4. <span data-ttu-id="583c2-127">Dosya karşılaştırma yardımcı programında, oluşturulan dosyaları karşılaştırın.</span><span class="sxs-lookup"><span data-stu-id="583c2-127">In a file comparison utility, compare the generated files.</span></span>

    <span data-ttu-id="583c2-128">Göreceğiniz ilk fark dosya üst bilgisinde olur.</span><span class="sxs-lookup"><span data-stu-id="583c2-128">The first difference that you will notice is in the file header.</span></span> <span data-ttu-id="583c2-129">SampleXmlReport.xml file dosyası, BOM karakteri içerirken SampleXmlReport (1).xml dosyası içermez.</span><span class="sxs-lookup"><span data-stu-id="583c2-129">The SampleXmlReport.xml file contains a BOM character, where the SampleXmlReport (1).xml file doesn't.</span></span>

    ![Dosya karşılaştırma yardımcı programı kullanarak, oluşturulan dosyaları karşılaştırma](./media/er-suppress-bom-characters-image3.png)

## <a name="see-also"></a><span data-ttu-id="583c2-131">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="583c2-131">See also</span></span>

- [<span data-ttu-id="583c2-132">ER biçimindeki XML öğelerinin yürütülmesini erteleme</span><span class="sxs-lookup"><span data-stu-id="583c2-132">Defer the execution of XML elements in ER formats</span></span>](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]