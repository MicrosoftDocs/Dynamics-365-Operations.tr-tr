---
title: Word biçiminde raporlar oluşturmak için Excel şablonlarıyla ER yapılandırmalarını yeniden kullanma
description: Bu konuda, Excel çalışma kitapları olarak rapor oluşturmak üzere tasarlanmış rapor biçimlerinin, Word belgeleri olarak rapor oluşturmak üzere nasıl yapılandırılabileceği açıklanmaktadır.
author: NickSelin
ms.date: 01/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab4cd4a390782936a74977ac2aef3790aa8ac1af
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891707"
---
# <a name="reuse-er-configurations-with-excel-templates-to-generate-reports-in-word-format"></a><span data-ttu-id="b91fe-103">Word biçiminde raporlar oluşturmak için Excel şablonlarıyla ER yapılandırmalarını yeniden kullanma</span><span class="sxs-lookup"><span data-stu-id="b91fe-103">Reuse ER configurations with Excel templates to generate reports in Word format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b91fe-104">Microsoft Word belgeleri olarak rapor oluşturmak için yeni bir [Elektronik raporlama (ER)](../general-electronic-reporting.md) [biçimi](../general-electronic-reporting.md#FormatComponentOutbound) [yapılandırabilirsiniz](../er-design-configuration-word.md).</span><span class="sxs-lookup"><span data-stu-id="b91fe-104">To generate reports as Microsoft Word documents, you can [configure](../er-design-configuration-word.md) a new [Electronic reporting (ER)](../general-electronic-reporting.md) [format](../general-electronic-reporting.md#FormatComponentOutbound).</span></span> <span data-ttu-id="b91fe-105">Alternatif olarak, başlangıçta Excel çalışma kitabı olarak rapor üretmek üzere tasarlanan bir ER biçimini yeniden kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b91fe-105">Alternatively, you can reuse an ER format that was originally designed to generate reports as Excel workbooks.</span></span> <span data-ttu-id="b91fe-106">Bu durumda, Excel şablonunu bir Word şablonuyla değiştirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="b91fe-106">In this case, you must replace the Excel template with a Word template.</span></span>

<span data-ttu-id="b91fe-107">Aşağıdaki yordamlarda, Sistem yöneticisi veya Elektronik raporlama geliştiricisi rolündeki bir kullanıcının, Excel dosyaları halinde rapor oluşturmak üzere tasarlanan bir ER biçimini yeniden kullanarak Word dosyası halinde rapor oluşturmak için ER biçimini nasıl yapılandırabileceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="b91fe-107">The following procedures show how a user in either the System administrator role or the Electronic reporting developer role can configure an ER format to generate reports as Word files by reusing an ER format that was designed to generate reports as Excel files.</span></span>

<span data-ttu-id="b91fe-108">Bu yordamlar, GBSI şirketinde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="b91fe-108">These procedures can be completed in the GBSI company.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b91fe-109">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="b91fe-109">Prerequisites</span></span>

<span data-ttu-id="b91fe-110">Bu yordamları tamamlamak için öncelikle [OPENXML biçiminde raporlar oluşturmak için bir ER yapılandırması tasarlama](er-design-reports-openxml-2016-11.md) görev kılavuzundaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b91fe-110">To complete these procedures, you must first follow the steps in the [Design a configuration for generating reports in OPENXML format](er-design-reports-openxml-2016-11.md) task guide.</span></span>

<span data-ttu-id="b91fe-111">Ayrıca örnek rapor için aşağıdaki şablonları indirmeli ve yerel olarak kaydetmelisiniz:</span><span class="sxs-lookup"><span data-stu-id="b91fe-111">You must also download and locally save the following templates for the sample report:</span></span>

- [<span data-ttu-id="b91fe-112">Ödeme Raporu Şablonu (SampleVendPaymDocReport.docx)</span><span class="sxs-lookup"><span data-stu-id="b91fe-112">Template of Payment Report (SampleVendPaymDocReport.docx)</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)
- [<span data-ttu-id="b91fe-113">Ödeme Raporunun Bağlı Şablonu (SampleVendPaymDocReportBounded.docx)</span><span class="sxs-lookup"><span data-stu-id="b91fe-113">Bounded Template of Payment Report (SampleVendPaymDocReportBounded.docx)</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)

<span data-ttu-id="b91fe-114">Bu yordamlar, Dynamics 365 for Operations 1611 sürümüne (Kasım 2016) eklenmiş bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="b91fe-114">These procedures are for a feature that was added in Dynamics 365 for Operations version 1611 (November 2016).</span></span>

## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="b91fe-115">Mevcut ER rapor yapılandırmasını seçme</span><span class="sxs-lookup"><span data-stu-id="b91fe-115">Select the existing ER report configuration</span></span>

1. <span data-ttu-id="b91fe-116">Dynamics 365 Finance'te **Kuruluş yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-116">In Dynamics 365 Finance, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="b91fe-117">**Litware, Inc.** yapılandırma sağlayıcısının **Etkin** olarak seçildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="b91fe-117">Make sure that the **Litware, Inc.** configuration provider is selected as **Active**.</span></span> <span data-ttu-id="b91fe-118">Böyle değilse, [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](er-configuration-provider-mark-it-active-2016-11.md) görev kılavuzundaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-118">If it isn't, follow the steps in the [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md) task guide.</span></span>
3. <span data-ttu-id="b91fe-119">**Raporlama yapılandırmaları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-119">Select **Reporting configurations**.</span></span> <span data-ttu-id="b91fe-120">Rapor çıktısını OPENXML biçiminde oluşturmak için tasarlanmış olan mevcut ER yapılandırmasını yeniden kullanacaksınız.</span><span class="sxs-lookup"><span data-stu-id="b91fe-120">You will reuse the existing ER configuration that was designed to generate the report output in OPENXML format.</span></span>
4. <span data-ttu-id="b91fe-121">**Yapılandırmalar** sayfasında sol bölmedeki yapılandırma ağacında, **Ödeme modeli**'ni genişletin ve **Örnek çalışma sayfası raporu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-121">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and select **Sample worksheet report**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b91fe-122">Seçili ER biçiminin taslak sürümü, **Sürümler** hızlı sekmesinde düzenlenebilir.</span><span class="sxs-lookup"><span data-stu-id="b91fe-122">The draft version of the selected ER format can be edited on the **Versions** FastTab.</span></span>

5. <span data-ttu-id="b91fe-123">**Tasarımcı**’yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-123">Select **Designer**.</span></span>
6. <span data-ttu-id="b91fe-124">**Biçim tasarımcısı** sayfasında, kök biçim öğesinin başlığının Excel şablonunun şu anda kullanıldığını belirttiğini görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b91fe-124">On the **Format designer** page, notice that the title of the root format element indicates that an Excel template is currently used.</span></span>

![Mevcut yapılandırmayı seçme](../media/er-design-configuration-word-2016-11-image01.gif)

## <a name="review-the-downloaded-word-template"></a><span data-ttu-id="b91fe-126">İndirilen Word şablonunu inceleme</span><span class="sxs-lookup"><span data-stu-id="b91fe-126">Review the downloaded Word template</span></span>

1. <span data-ttu-id="b91fe-127">Word masaüstü uygulamasında, daha önce indirdiğiniz **SampleVendPaymDocReport.docx** şablon dosyasını açın.</span><span class="sxs-lookup"><span data-stu-id="b91fe-127">In the Word desktop application, open the **SampleVendPaymDocReport.docx** template file that you downloaded earlier.</span></span>
2. <span data-ttu-id="b91fe-128">Şablonun yalnızca ER çıkışı olarak oluşturmak istediğiniz belgenin düzenini içerdiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="b91fe-128">Verify that the template contains only the layout of the document that you want to generate as ER output.</span></span>

![Masaüstü uygulamasındaki Word şablon düzeni](../media/er-design-configuration-word-2016-11-image02.png)

## <a name="replace-the-excel-template-with-the-word-template-and-add-a-custom-xml-part"></a><span data-ttu-id="b91fe-130">Excel şablonunu Word şablonuyla değiştirin ve özel bir XML bölümü ekleyin</span><span class="sxs-lookup"><span data-stu-id="b91fe-130">Replace the Excel template with the Word template and add a custom XML part</span></span>

<span data-ttu-id="b91fe-131">Şu anda, Excel belgesi OPENXML biçiminde çıktı üretmek için şablon olarak kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="b91fe-131">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="b91fe-132">Bu şablonu, daha önce indirdiğiniz SampleVendPaymDocReport.docx Word şablon dosyasıyla değiştireceksiniz.</span><span class="sxs-lookup"><span data-stu-id="b91fe-132">You will replace this template with the SampleVendPaymDocReport.docx Word template file that you downloaded earlier.</span></span> <span data-ttu-id="b91fe-133">Ayrıca özel bir XML bölümü ekleyerek Word şablonunu genişleteceksiniz.</span><span class="sxs-lookup"><span data-stu-id="b91fe-133">You will also extend the Word template by adding a custom XML part.</span></span>

1. <span data-ttu-id="b91fe-134">Finance'teki **Biçim tasarımcısı** sayfasında yer alan **Biçim** sekmesinde **Ekler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-134">In Finance, on the **Format designer** page, on the **Format** tab, select **Attachments**.</span></span>
2. <span data-ttu-id="b91fe-135">**Ekler** sayfasında, mevcut Excel şablonunu kaldırmak için **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-135">On the **Attachments** page, select **Delete** to remove the existing Excel template.</span></span> <span data-ttu-id="b91fe-136">Değişikliği onaylamak için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-136">Select **Yes** to confirm the change.</span></span>
3. <span data-ttu-id="b91fe-137">**Yeni** \> **Dosya**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-137">Select **New** \> **File**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b91fe-138">ER biçimlerinin şablonlarını depolamak için ER parametrelerinde [yapılandırılan](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) bir belge türünü seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b91fe-138">You must select a document type that has been [configured](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

4. <span data-ttu-id="b91fe-139">**Göz at**'ı seçin ve daha önce indirdiğiniz **SampleVendPaymDocReport.docx** dosyasını bulup seçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-139">Select **Browse**, and then browse to and select the **SampleVendPaymDocReport.docx** file that you downloaded earlier.</span></span>
5. <span data-ttu-id="b91fe-140">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-140">Select **OK**.</span></span>
6. <span data-ttu-id="b91fe-141">**Ekler** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="b91fe-141">Close the **Attachments** page.</span></span>
7. <span data-ttu-id="b91fe-142">**Biçim tasarımcısı** sayfasındaki **Şablon** alanında, daha önce kullanılan Excel şablonu yerine Word şablonunu kullanmak için **SampleVendPaymDocReport.docx** dosyasını girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-142">On the **Format designer** page, in the **Template** field, enter or select the **SampleVendPaymDocReport.docx** file to use that Word template instead of the Excel template that was previously used.</span></span>
8. <span data-ttu-id="b91fe-143">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-143">Select **Save**.</span></span>

    <span data-ttu-id="b91fe-144">**Kaydet** eylemi, yapılandırma değişikliklerini depolamanın yanı sıra ekli Word şablonunu da güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b91fe-144">In addition to storing configuration changes, the **Save** action updates the attached Word template.</span></span> <span data-ttu-id="b91fe-145">Tasarlanan biçimin hiyerarşi yapısı, ekli Word belgesine **Rapor** adında yeni bir özel XML bölümü olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="b91fe-145">The hierarchical structure of the designed format is added to the attached Word document as a new custom XML part that is named **Report**.</span></span> <span data-ttu-id="b91fe-146">Ekli Word şablonu, ER çıkışı olarak oluşturulacak belgenin düzenini ve ER'nin çalışma zamanında bu şablona gireceği verilerin yapısını içerir.</span><span class="sxs-lookup"><span data-stu-id="b91fe-146">The attached Word template contains the layout of the document that will be generated as ER output and the structure of data that ER will enter in that template at runtime.</span></span>

9. <span data-ttu-id="b91fe-147">Kök biçim öğesinin başlığının Word şablonunun şu anda kullanıldığını belirttiğini görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b91fe-147">Notice that the title of the root format element indicates that a Word template is currently used.</span></span>

    ![Excel şablonunu Word şablonuyla değiştirme ve özel bir XML bölümü ekleme](../media/er-design-configuration-word-2016-11-image03.gif)

10. <span data-ttu-id="b91fe-149">**Biçim** sekmesinde, **Ekler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-149">On the **Format** tab, select **Attachments**.</span></span>

<span data-ttu-id="b91fe-150">Şimdi, **Rapor** özel XML bölümünün öğelerini Word belgesinin içerik denetimleriyle eşleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b91fe-150">You can now map the elements of the **Report** custom XML part to the content controls of the Word document.</span></span>

<span data-ttu-id="b91fe-151">[Özel XML bölümlerinin](/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019) öğeleriyle eşleştirilen [içerik denetimlerine](/office/client-developer/word/content-controls-in-word) sahip formlar olarak Word belgeleri tasarlama işlemi hakkında bilgi sahibiyseniz belgeyi oluşturmak için bir sonraki yordamda yer alan adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="b91fe-151">If you're familiar with the process of designing Word documents as forms that contain [content controls](/office/client-developer/word/content-controls-in-word) that are mapped to elements of [custom XML parts](/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019), complete all steps in the next procedure to create the document.</span></span> <span data-ttu-id="b91fe-152">Daha fazla bilgi için bkz. [Kullanıcıların Word'de doldurduğu veya yazdırdığı formlar oluşturma](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b).</span><span class="sxs-lookup"><span data-stu-id="b91fe-152">For more information, see [Create forms that users complete or print in Words](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b).</span></span> <span data-ttu-id="b91fe-153">Aksi takdirde, sonraki yordama geçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-153">Otherwise, skip the next procedure.</span></span>

## <a name="get-a-word-document-that-has-a-custom-xml-part-and-do-data-mapping"></a><a id='get-word-doc'></a><span data-ttu-id="b91fe-154">Özel XML bölümüne sahip bir Word belgesi alma ve veri eşleme işlemini gerçekleştirme</span><span class="sxs-lookup"><span data-stu-id="b91fe-154">Get a Word document that has a custom XML part and do data mapping</span></span>

1. <span data-ttu-id="b91fe-155">Finance'teki **Ekler** sayfasında, Finance'te seçili şablonu indirmek ve yerel olarak Word belgesi biçiminde saklamak için **Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-155">In Finance, on the **Attachments** page, select **Open** to download the selected template from Finance and store it locally as a Word document.</span></span>
3. <span data-ttu-id="b91fe-156">Word masaüstü uygulamasında biraz önce indirdiğiniz belgeyi açın.</span><span class="sxs-lookup"><span data-stu-id="b91fe-156">In the Word desktop application, open the document that you just downloaded.</span></span>
4. <span data-ttu-id="b91fe-157">**Geliştirici** sekmesinde **XML Eşleme Bölmesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-157">On the **Developer** tab, select **XML Mapping Pane**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b91fe-158">**Geliştirici** sekmesi şeritte görüntülenmezse eklemek için şeridi özelleştirin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-158">If the **Developer** tab doesn't appear on the ribbon, customize the ribbon to add it.</span></span>

5. <span data-ttu-id="b91fe-159">**XML Eşleme** bölmesindeki **Özel XML Bölümü** alanında **Rapor** özel XML bölümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-159">In the **XML Mapping** pane, in the **Custom XML Part** field, select the **Report** custom XML part.</span></span>
6. <span data-ttu-id="b91fe-160">Seçili **Rapor** özel XML bölümü ile Word belgesinin içerik denetimlerini eşleyin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-160">Map the elements of the selected **Report** custom XML part and the content controls of the Word document.</span></span>
7. <span data-ttu-id="b91fe-161">Güncelleştirilmiş Word belgesini yerel olarak **SampleVendPaymDocReportBounded.docx** adıyla kaydedin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-161">Save the updated Word document locally as **SampleVendPaymDocReportBounded.docx**.</span></span>

## <a name="review-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a><span data-ttu-id="b91fe-162">Özel XML bölümünün içerik denetimleriyle eşlendiği Word şablonunu gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="b91fe-162">Review the Word template where the custom XML part is mapped to content controls</span></span>

1. <span data-ttu-id="b91fe-163">Word masaüstü uygulamasında **SampleVendPaymDocReportBounded.docx** şablon dosyasını açın.</span><span class="sxs-lookup"><span data-stu-id="b91fe-163">In the Word desktop application, open the **SampleVendPaymDocReportBounded.docx** template file.</span></span>
2. <span data-ttu-id="b91fe-164">Şablonun ER çıkışı olarak oluşturmak istediğiniz belgenin düzenini içerdiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="b91fe-164">Verify that the template contains the layout of the document that you want to generate as ER output.</span></span> <span data-ttu-id="b91fe-165">Çalışma zamanında ER'nin bu şablona gireceği veriler için yer tutucu olarak kullanılan içerik denetimleri, **Rapor** özel XML bölümü öğeleri ile Word belgesinin içerik denetimleri arasında yapılandırılan eşlemelere bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="b91fe-165">The content controls that are used as placeholders for data that ER will enter in this template at runtime are based on the mappings that are configured between elements of the **Report** custom XML part and the content controls of the Word document.</span></span>

![Masaüstü uygulamasındaki Word şablonunun önizlemesi](../media/er-design-configuration-word-2016-11-image04.png)

## <a name="upload-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a><span data-ttu-id="b91fe-167">Özel XML bölümünün içerik denetimleriyle eşlendiği Word şablonunu indirme</span><span class="sxs-lookup"><span data-stu-id="b91fe-167">Upload the Word template where the custom XML part is mapped to content controls</span></span>

1. <span data-ttu-id="b91fe-168">Finance'teki **Ekler** sayfasında, **Rapor** özel XML bölümü öğeleri ve içerik denetimleri arasında eşleme olmayan Word şablonunu kaldırmak için **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-168">In Finance, on the **Attachments** page, select **Delete** to remove the Word template that has no mappings between elements of the **Report** custom XML part and content controls.</span></span> <span data-ttu-id="b91fe-169">Değişikliği onaylamak için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-169">Select **Yes** to confirm the change.</span></span>
2. <span data-ttu-id="b91fe-170">**Rapor** özel XML bölümü öğeleri ve içerik denetimleri arasında eşleme içeren yeni bir şablon dosyası eklemek için **Yeni** \> **Dosya**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-170">Select **New** \> **File** to add a new template file that contains mappings between elements of the **Report** custom XML part and content controls.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b91fe-171">ER biçimlerinin şablonlarını depolamak için ER parametrelerinde [yapılandırılan](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) bir belge türünü seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b91fe-171">You must select a document type that has been [configured](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

3. <span data-ttu-id="b91fe-172">**Göz at**'ı seçin ve ardından indirdiğiniz veya [Özel XML bölümüne sahip bir Word belgesi alma ve veri eşleme işlemini gerçekleştirme](#get-word-doc) bölümündeki yordamı tamamlayarak hazırladığınız **SampleVendPaymDocReportBounded.docx** dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-172">Select **Browse**, and then browse to and select the **SampleVendPaymDocReportBounded.docx** file that you downloaded or prepared by completing the procedure in the [Get a Word that has a custom XML part to do data mapping](#get-word-doc) section.</span></span>
4. <span data-ttu-id="b91fe-173">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-173">Select **OK**.</span></span>
5. <span data-ttu-id="b91fe-174">**Ekler** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="b91fe-174">Close the **Attachments** page.</span></span>
6. <span data-ttu-id="b91fe-175">**Biçim tasarımcısı** sayfasındaki **Şablon** alanında az önce indirdiğiniz belgeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-175">On the **Format designer** page, in the **Template** field, select the document that you just downloaded.</span></span>
7. <span data-ttu-id="b91fe-176">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-176">Select **Save**.</span></span>
8. <span data-ttu-id="b91fe-177">**Biçim tasarımcısı** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="b91fe-177">Close the **Format designer** page.</span></span>

## <a name="mark-the-configured-format-as-runnable"></a><span data-ttu-id="b91fe-178">Yapılandırılmış biçimi çalıştırılabilir olarak işaretleme</span><span class="sxs-lookup"><span data-stu-id="b91fe-178">Mark the configured format as runnable</span></span>

<span data-ttu-id="b91fe-179">Düzenlenebilir biçimin taslak sürümünü çalıştırmak için sürümü [çalıştırılabilir](../er-quick-start2-customize-report.md#MarkFormatRunnable) hale getirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b91fe-179">To run the draft version of the editable format, you must make it [runnable](../er-quick-start2-customize-report.md#MarkFormatRunnable).</span></span>

1. <span data-ttu-id="b91fe-180">Finance'te **Yapılandırmalar** sayfasındaki Eylem Bölmesinde, **Yapılandırmalar** sekmesinin **Gelişmiş ayarlar** grubunda **Kullanıcı parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-180">In Finance, on the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
2. <span data-ttu-id="b91fe-181">**Kullanıcı parametreleri** iletişim kutusunda, **Çalıştırma ayarları** seçeneğini **Evet** olarak ayarlayıp **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-181">In the **User parameters** dialog box, set the **Run settings** option to **Yes**, and then select **OK**.</span></span>
3. <span data-ttu-id="b91fe-182">Geçerli sayfayı düzenlemeye hazır hale getirmek için gerektiğinde **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-182">Select **Edit** to make the current page editable, as required.</span></span>
4. <span data-ttu-id="b91fe-183">Seçili durumdaki **Örnek çalışma sayfası** yapılandırması için **Taslak Çalıştır** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b91fe-183">For the currently selected **Sample worksheet report** configuration, set the **Run Draft** option to **Yes**.</span></span>
5. <span data-ttu-id="b91fe-184">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-184">Select **Save**.</span></span>

## <a name="run-the-format-to-create-output-in-word-format"></a><span data-ttu-id="b91fe-185">Word biçiminde çıktı oluşturmak için biçimi çalıştırma</span><span class="sxs-lookup"><span data-stu-id="b91fe-185">Run the format to create output in Word format</span></span>

1. <span data-ttu-id="b91fe-186">Finance'te **Borç hesapları** \> **Ödemeler** \> **Ödeme günlüğü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-186">In Finance, go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="b91fe-187">Daha önce girmiş olduğunuz bir ödeme günlüğünde **Satırlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-187">In a payment journal that you entered earlier, select **Lines**.</span></span>
3. <span data-ttu-id="b91fe-188">**Satıcı ödemeleri** sayfasında, ızgaradaki tüm satırları seçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-188">On the **Vendor payments** page, select all rows in the grid.</span></span>
4. <span data-ttu-id="b91fe-189">**Ödeme durumu** \> **Hiçbiri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-189">Select **Payment status** \> **None**.</span></span>

    ![Satıcı ödemeleri sayfasındaki işlenecek ödemeler](../media/er-design-configuration-word-2016-11-image05.png)

5. <span data-ttu-id="b91fe-191">Eylem bölmesinde, **Ödeme oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-191">On the Action Pane, select **Generate payments**.</span></span>
6. <span data-ttu-id="b91fe-192">Gösterilen iletişim kutusunda şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="b91fe-192">In the dialog box that appears, follow these steps:</span></span>

    1. <span data-ttu-id="b91fe-193">**Ödeme yöntemi** alanında **Elektronik**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-193">In the **Method of payment** field, select **Electronic**.</span></span>
    2. <span data-ttu-id="b91fe-194">**Banka hesabı** alanında **GBSI OPER** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-194">In the **Bank account** field, select **GBSI OPER**.</span></span>
    3. <span data-ttu-id="b91fe-195">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-195">Select **OK**.</span></span>

7. <span data-ttu-id="b91fe-196">**Elektronik rapor parametreleri** iletişim kutusunda **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-196">In the **Electronic report parameters** dialog box, select **OK**.</span></span>
8. <span data-ttu-id="b91fe-197">Oluşturulan çıktı, Word biçiminde sunulur ve işlenen ödemelerin ayrıntılarını içerir.</span><span class="sxs-lookup"><span data-stu-id="b91fe-197">The generated output is presented in Word format and contains the details of the processed payments.</span></span> <span data-ttu-id="b91fe-198">Oluşturulan çıktıyı analiz edin.</span><span class="sxs-lookup"><span data-stu-id="b91fe-198">Analyze the generated output.</span></span>

    ![Word biçiminde oluşturulan çıktı](../media/er-design-configuration-word-2016-11-image06.png)

## <a name="additional-resources"></a><span data-ttu-id="b91fe-200">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b91fe-200">Additional resources</span></span>

- [<span data-ttu-id="b91fe-201">Word biçiminde raporlar oluşturmak için yeni bir ER yapılandırması tasarlama</span><span class="sxs-lookup"><span data-stu-id="b91fe-201">Design a new ER configuration to generate reports in Word format</span></span>](../er-design-configuration-word.md)
- [<span data-ttu-id="b91fe-202">Er kullanarak oluşturduğunuz belgelere resimler ve şekiller katıştırma</span><span class="sxs-lookup"><span data-stu-id="b91fe-202">Embed images and shapes in documents that you generate by using ER</span></span>](../electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]