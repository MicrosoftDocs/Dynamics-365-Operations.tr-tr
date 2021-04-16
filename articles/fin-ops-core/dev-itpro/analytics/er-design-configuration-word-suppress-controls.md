---
title: Oluşturulan raporlarda Word içerik denetimlerini gizleme
description: Bu konu, içerik denetimlerinin gizlendiği Microsoft Word dosyaları olarak raporlar oluşturmak üzere elektronik raporlama (ER) biçiminin nasıl yapılandırılacağını açıklamaktadır.
author: NickSelin
ms.date: 02/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: 8c99203110cfdc7f8123c30488611d55f48e8f67
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753621"
---
# <a name="suppress-word-content-controls-in-generated-reports"></a><span data-ttu-id="7c463-103">Oluşturulan raporlarda Word içerik denetimlerini gizleme</span><span class="sxs-lookup"><span data-stu-id="7c463-103">Suppress Word content controls in generated reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7c463-104">Raporları Microsoft Word belgeleri olarak oluşturmak için, raporlar için Word belgesi şeklinde bir şablon tasarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="7c463-104">To generate reports as Microsoft Word documents, you must design a template for the reports as a Word document.</span></span> <span data-ttu-id="7c463-105">Bu şablon, çalışma zamanında doldurulacak veriler için yer tutucu olarak Word içerik denetimleri içermelidir.</span><span class="sxs-lookup"><span data-stu-id="7c463-105">This template must contain Word content controls as placeholders for data that will be filled in at runtime.</span></span> <span data-ttu-id="7c463-106">Raporlarınız için şablon olarak oluşturulan Word belgesini kullanmak için yeni bir [Elektronik raporlama (ER)](general-electronic-reporting.md) [çözümü](er-quick-start1-new-solution.md) [yapılandırabilirsiniz](er-design-configuration-word.md).</span><span class="sxs-lookup"><span data-stu-id="7c463-106">To use the Word document that is created as a template for your reports, you can [configure](er-design-configuration-word.md) a new [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md).</span></span> <span data-ttu-id="7c463-107">Çözüm, ER [biçimi](general-electronic-reporting.md#FormatComponentOutbound) bileşeni içeren bir ER [yapılandırması](general-electronic-reporting.md#Configuration) içermelidir.</span><span class="sxs-lookup"><span data-stu-id="7c463-107">The solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="7c463-108">Bu ER biçimi, rapor oluşturma için tasarlanmış şablonu kullanacak şekilde yapılandırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7c463-108">This ER format must be configured to use the designed template for report generation.</span></span>

<span data-ttu-id="7c463-109">Dynamics 365 Finance sürüm 10.0.6 ve sonrasında, oluşturulan belgelerdeki bazı Word içerik denetimlerini gizlemek için ER biçiminizde formüller yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7c463-109">In version 10.0.6 and later of Dynamics 365 Finance, you can configure formulas in your ER format to suppress some Word content controls in generated documents.</span></span>

<span data-ttu-id="7c463-110">Aşağıdaki adımlarda, sistem yöneticisine veya elektronik raporlama işlevsel Danışman rolüne atanan bir kullanıcının, Word dosyaları olarak raporlar oluşturan ve bir Word şablonu kullanılarak yapılandırılmış olan oluşturulan raporlarda bazı içerik denetimlerini gizleyen bir ER biçiminin nasıl yapılandırılabileceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="7c463-110">The following steps explain how a user who is assigned to the System administrator or Electronic reporting functional consultant role can configure an ER format that generates reports as Word files and suppresses some of the content controls in the generated reports that have been configured by using a Word template.</span></span>

<span data-ttu-id="7c463-111">Bu adımlar GBSI şirketinde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="7c463-111">These steps can be completed in the GBSI company.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7c463-112">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="7c463-112">Prerequisites</span></span>

<span data-ttu-id="7c463-113">Bu adımları tamamlamak için önce şu görev kılavuzlarındaki adımları tamamlamalısınız:</span><span class="sxs-lookup"><span data-stu-id="7c463-113">To complete these steps, you must first complete the steps in the following task guides:</span></span>

- [<span data-ttu-id="7c463-114">OPENXML formatında raporların oluşturulması için bir yapılandırma tasarlama</span><span class="sxs-lookup"><span data-stu-id="7c463-114">Design a configuration for generating reports in OPENXML format</span></span>](./tasks/er-design-reports-openxml-2016-11.md)
- [<span data-ttu-id="7c463-115">Word biçiminde raporlar oluşturmak için ER yapılandırmalarını Excel şablonlarıyla yeniden kullanma</span><span class="sxs-lookup"><span data-stu-id="7c463-115">Re-use ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)

<span data-ttu-id="7c463-116">Bu görev kılavuzlarının adımlarını tamamladığınızda, aşağıdaki öğeler hazırlanır:</span><span class="sxs-lookup"><span data-stu-id="7c463-116">When you complete the steps of these task guides, the following items are prepared:</span></span>

- <span data-ttu-id="7c463-117">Word biçiminde belge oluşturmak üzere yapılandırılan **örnek çalışma sayfası raporu** ER biçimi</span><span class="sxs-lookup"><span data-stu-id="7c463-117">A **Sample worksheet report** ER format that is configured to generate a document in Word format</span></span>
- <span data-ttu-id="7c463-118">**Çalıştırılabilir** olarak işaretlenmiş **örnek çalışma sayfası raporu** ER biçiminin bir [taslak](general-electronic-reporting.md#component-versioning) versiyonu</span><span class="sxs-lookup"><span data-stu-id="7c463-118">A [draft](general-electronic-reporting.md#component-versioning) version of the **Sample worksheet report** ER format that is marked as **Runnable**</span></span>
- <span data-ttu-id="7c463-119">Satıcı ödeme işlemleri için **örnek çalışma sayfası raporu** ER biçimini kullanmak üzere yapılandırılan bir **elektronik** ödeme yöntemi</span><span class="sxs-lookup"><span data-stu-id="7c463-119">An **Electronic** method of payments that is configured to use the **Sample worksheet report** ER format for vendor payment processing</span></span>

<span data-ttu-id="7c463-120">Ayrıca örnek rapor için aşağıdaki şablonu indirmeli ve kaydetmelisiniz:</span><span class="sxs-lookup"><span data-stu-id="7c463-120">You must also download and save the following template for the sample report:</span></span>

- [<span data-ttu-id="7c463-121">Ödeme Raporunun Bağlı Şablonu 2 (SampleVendPaymDocReportBounded2.docx)</span><span class="sxs-lookup"><span data-stu-id="7c463-121">Bounded Template 2 of Payment Report (SampleVendPaymDocReportBounded2.docx)</span></span>](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded2.docx)

## <a name="review-the-downloaded-word-template"></a><a id="tag-control"></a><span data-ttu-id="7c463-122">İndirilen Word şablonunu inceleme</span><span class="sxs-lookup"><span data-stu-id="7c463-122">Review the downloaded Word template</span></span>

1. <span data-ttu-id="7c463-123">Word masaüstü uygulamasında, daha önce indirdiğiniz **SampleVendPaymDocReportBounded2.docx** şablon dosyasını açın.</span><span class="sxs-lookup"><span data-stu-id="7c463-123">In the Word desktop application, open the **SampleVendPaymDocReportBounded2.docx** template file that you downloaded earlier.</span></span>
2. <span data-ttu-id="7c463-124">Şablon dosyasının, işlenmiş ödemelerde karşılanan her bir para birimi kodu için toplam ödeme tutarlarını gösteren bir Özet bölümü içerdiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="7c463-124">Verify that the template file contains a summary section that shows the total payment amounts for every currency code that has been met in the processed payments.</span></span>

    - <span data-ttu-id="7c463-125">Özet bölümü, Word belgesinin ayrı bir tablosunda bulunur.</span><span class="sxs-lookup"><span data-stu-id="7c463-125">The summary section resides in a separate table of the Word document.</span></span>
    - <span data-ttu-id="7c463-126">Bu tablonun ilk satırı bölüm başlığı olarak tablo sütunları başlıklarını içerir.</span><span class="sxs-lookup"><span data-stu-id="7c463-126">The first row of this table holds the table columns headings as the section header.</span></span>
    - <span data-ttu-id="7c463-127">Bu tablonun ikinci satırı, Bölüm ayrıntıları olarak tekrarlanan içerik denetimini içerir.</span><span class="sxs-lookup"><span data-stu-id="7c463-127">The second row of this table holds the repeating content control as the section details.</span></span>
    - <span data-ttu-id="7c463-128">Bu içerik denetimi **Rapor** özel XML parçasının **summarylines** alanıyla eşleştirilir.</span><span class="sxs-lookup"><span data-stu-id="7c463-128">This content control is mapped to the **SummaryLines** field of the **Report** custom XML part.</span></span>
    - <span data-ttu-id="7c463-129">Bu eşlemeye dayalı olarak içerik denetimi, düzenlenebilir ER biçiminin **summarylines** öğesiyle ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="7c463-129">Based on this mapping, the content control is associated with the **SummaryLines** element of the editable ER format.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7c463-130">Tekrarlanan içerik denetimi, eşlendiği özel XML parçasının alanıyla eşleşen **summarylines** anahtarı tarafından etiketlenir.</span><span class="sxs-lookup"><span data-stu-id="7c463-130">The repeating content control is tagged by the **SummaryLines** key that matches the field of the custom XML part that it has been mapped to.</span></span>

    ![Word şablonu düzeni](./media/er-design-configuration-word-suppress-controls-image1.gif)

## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="7c463-132">Mevcut ER rapor yapılandırmasını seçme</span><span class="sxs-lookup"><span data-stu-id="7c463-132">Select the existing ER report configuration</span></span>

<span data-ttu-id="7c463-133">Aşağıdaki adımlarda, daha önce sözü edilen görev kılavuzlarındaki adımları tamamladığınızda yapılandırdığınız varolan ER yapılandırmasını yeniden kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7c463-133">For the following steps, you will reuse the existing ER configuration that you configured when you completed the steps in the previously mentioned task guides.</span></span>

1. <span data-ttu-id="7c463-134">**Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="7c463-134">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="7c463-135">**Raporlama yapılandırmaları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="7c463-135">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="7c463-136">**Yapılandırmalar** sayfasında, yapılandırma ağacında, **Ödeme modeli**'ni genişletin ve **Örnek çalışma sayfası raporu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="7c463-136">On the **Configurations** page, in the configuration tree, expand **Payment model**, and select **Sample worksheet report**.</span></span>
4. <span data-ttu-id="7c463-137">Seçili ER biçiminin taslak sürümünü düzenlemek için **Tasarımcı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="7c463-137">Select **Designer** to edit the draft version of the selected ER format.</span></span>

## <a name="replace-the-current-template-with-the-new-template"></a><span data-ttu-id="7c463-138">Geçerli şablonu yeni şablon ile değiştirme</span><span class="sxs-lookup"><span data-stu-id="7c463-138">Replace the current template with the new template</span></span>

<span data-ttu-id="7c463-139">Şu anda, Word biçiminde çıktı oluşturmak için SampleVendPaymDocReportBounded.docx dosyası şablon olarak kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="7c463-139">Currently, the SampleVendPaymDocReportBounded.docx file is used as a template to generate the output in Word format.</span></span> <span data-ttu-id="7c463-140">Aşağıdaki adımlarda bu Word şablonunu, daha önce indirdiğiniz SampleVendPaymDocReportBounded2.docx Word şablonuyla değiştireceksiniz.</span><span class="sxs-lookup"><span data-stu-id="7c463-140">In the following steps, you will replace this Word template with the new Word template, SampleVendPaymDocReportBounded2.docx, that you downloaded earlier.</span></span>

1. <span data-ttu-id="7c463-141">**Biçim tasarımcısı** sayfasında, **Ekler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7c463-141">On the **Format designer** page, select **Attachments**.</span></span>
2. <span data-ttu-id="7c463-142">**Ekler** sayfasında, mevcut şablonu kaldırmak için **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7c463-142">On the **Attachments** page, select **Delete** to remove the existing template.</span></span>
3. <span data-ttu-id="7c463-143">Silmeyi onaylamak için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7c463-143">Select **Yes** to confirm the deletion.</span></span>
4. <span data-ttu-id="7c463-144">**Yeni** \> **Dosya**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="7c463-144">Select **New** \> **File**.</span></span>
5. <span data-ttu-id="7c463-145">**Göz at**'ı seçin ve daha önce indirdiğiniz **SampleVendPaymDocReportBounded2.docx** dosyasını bulup seçin.</span><span class="sxs-lookup"><span data-stu-id="7c463-145">Select **Browse**, and browse to and select the **SampleVendPaymDocReportBounded2.docx** file that you downloaded earlier.</span></span>
6. <span data-ttu-id="7c463-146">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7c463-146">Select **OK**.</span></span>
7. <span data-ttu-id="7c463-147">**Ekler** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="7c463-147">Close the **Attachments** page.</span></span>
8. <span data-ttu-id="7c463-148">**Biçim Tasarımcısı** sayfasında, **şablon** alanında **SampleVendPaymDocReportBounded2.docx** dosyasını girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="7c463-148">On the **Format designer** page, in the **Template** field, enter or select the **SampleVendPaymDocReportBounded2.docx** file.</span></span>

## <a name="run-the-format-to-create-word-output"></a><span data-ttu-id="7c463-149">Word çıktısı oluşturmak için biçimi yürütme</span><span class="sxs-lookup"><span data-stu-id="7c463-149">Run the format to create Word output</span></span>

1. <span data-ttu-id="7c463-150">**Borç hesapları** \> **Ödemeler** \> **Ödeme günlüğü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="7c463-150">Go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="7c463-151">**Satıcı ödemeleri** sayfasında, **liste** sekmesinde, tüm ödemeleri seçin.</span><span class="sxs-lookup"><span data-stu-id="7c463-151">On the **Vendor payments** page, on the **List** tab, select all the payments.</span></span>
3. <span data-ttu-id="7c463-152">**Ödeme durumu** \> **Hiçbiri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="7c463-152">Select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="7c463-153">**Ödemeleri oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="7c463-153">Select **Generate payments**.</span></span>
5. <span data-ttu-id="7c463-154">**Ödeme yöntemi** alanında **Elektronik**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7c463-154">In the **Method of payment** field, select **Electronic**.</span></span>
6. <span data-ttu-id="7c463-155">**Banka hesabı** alanında **GBSI OPER** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7c463-155">In the **Bank account** field, select **GBSI OPER**.</span></span>
7. <span data-ttu-id="7c463-156">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7c463-156">Select **OK**.</span></span>
8. <span data-ttu-id="7c463-157">**Elektronik rapor parametreleri** iletişim kutusunda **Tamam**'ı seçin ve oluşturulan çıktıyı analiz edin.</span><span class="sxs-lookup"><span data-stu-id="7c463-157">In the **Electronic report parameters** dialog box, select **OK**, and analyze the generated output.</span></span>

    ![Satıcı ödemeleri sayfasındaki işlenecek ödemeler](./media/er-design-configuration-word-suppress-controls-image2.gif)

    <span data-ttu-id="7c463-159">Çıktı Word biçiminde sunulur ve Özet bölümünü içerir.</span><span class="sxs-lookup"><span data-stu-id="7c463-159">The output is presented in Word format and contains the summary section.</span></span>

## <a name="configure-the-editable-format-to-suppress-the-summary-section"></a><a id="configure-to-suppress-control"></a><span data-ttu-id="7c463-160">Özet bölümünü gizlemek için düzenlenebilir biçimi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="7c463-160">Configure the editable format to suppress the summary section</span></span>

<span data-ttu-id="7c463-161">Oluşturulan bir belgede Özet bölümünü gizlemek istiyorsanız, bu ER biçimini çalıştıran bir kullanıcının isteğine bağlı olarak, düzenlenebilir ER biçimini değiştirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="7c463-161">If you want to suppress the summary section in a generated document, based on the request of a user who runs this ER format, you must modify the editable ER format.</span></span>

1. <span data-ttu-id="7c463-162">**Kuruluş Yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin ve düzenleme için ER biçiminin taslak sürümünü açın.</span><span class="sxs-lookup"><span data-stu-id="7c463-162">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**, and open the draft version of the ER format for editing.</span></span>
2. <span data-ttu-id="7c463-163">**Raporlama yapılandırmaları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="7c463-163">Select **Reporting configurations**.</span></span> 
3. <span data-ttu-id="7c463-164">**Yapılandırmalar** sayfasında, yapılandırma ağacında, **Ödeme modeli** \> **Örnek çalışma sayfası raporu**'nu genişletin.</span><span class="sxs-lookup"><span data-stu-id="7c463-164">On the **Configurations** page, in the configuration tree, expand **Payment model** \> **Sample worksheet report**.</span></span>
4. <span data-ttu-id="7c463-165">**Tasarımcı**’yı seçin.</span><span class="sxs-lookup"><span data-stu-id="7c463-165">Select **Designer**.</span></span>
5. <span data-ttu-id="7c463-166">**Biçim Tasarımcısı** sayfasında, **Word**'ü genişletin ve **summarylines**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7c463-166">On the **Format designer** page, expand **Word**, and select **SummaryLines**.</span></span>
6. <span data-ttu-id="7c463-167">**Eşleme** sekmesinde, çalışma zamanında kullanıcıya Özet bölümünün gizlenip gizlenmeyeceğini sormak için yeni bir veri kaynağı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="7c463-167">On the **Mapping** tab, add a new data source to ask the user, at runtime, whether the summary section should be suppressed:</span></span>

    1. <span data-ttu-id="7c463-168">**Kök ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7c463-168">Select **Add root**.</span></span>
    2. <span data-ttu-id="7c463-169">**Veri kaynağı ekle** iletişim kutusunda **Kullanıcı giriş parametresi veri kaynağı özellikleri** iletişim kutusunu açmak için **Genel\Kullanıcı girişi parametresi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="7c463-169">In the **Add data source** dialog box, select **General\User input parameter** to open the **'User input parameter' data source properties** dialog box.</span></span>
    3. <span data-ttu-id="7c463-170">**Ad** alanına, **uipSuppress** yazın.</span><span class="sxs-lookup"><span data-stu-id="7c463-170">In the **Name** field, enter **uipSuppress**.</span></span>
    4. <span data-ttu-id="7c463-171">**Etiket** alanına **Özet bölümünü gizle** yazın.</span><span class="sxs-lookup"><span data-stu-id="7c463-171">In the **Label** field, enter **Suppress summary section**.</span></span>
    5. <span data-ttu-id="7c463-172">**Operasyonlar veri türü adı** alanında, **NoYes** yazın veya girin.</span><span class="sxs-lookup"><span data-stu-id="7c463-172">In the **Operations data type name** field, select or enter **NoYes**.</span></span>
    6. <span data-ttu-id="7c463-173">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7c463-173">Select **OK**.</span></span>

7. <span data-ttu-id="7c463-174">**NoYes** uygulama numaralandırmasının yeni bir veri kaynağını ekleyin:</span><span class="sxs-lookup"><span data-stu-id="7c463-174">Add a new data source of the **NoYes** application enumeration type:</span></span>

    1. <span data-ttu-id="7c463-175">**Kök ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7c463-175">Select **Add root**.</span></span>
    2. <span data-ttu-id="7c463-176">**Veri kaynağı Ekle** iletişim kutusunda, **Dynamics 365 for Operations\Numaralandırma**'yı seçerek **'Numaralandırma'veri kaynağı özellikleri** iletişim kutusunu açın.</span><span class="sxs-lookup"><span data-stu-id="7c463-176">In the **Add data source** dialog box, select **Dynamics 365 for Operations\Enumeration** to open the **'Enumeration' data source properties** dialog box.</span></span>
    3. <span data-ttu-id="7c463-177">**Ad** alanına, **enumNoYes** yazın.</span><span class="sxs-lookup"><span data-stu-id="7c463-177">In the **Name** field, enter **enumNoYes**.</span></span>
    4. <span data-ttu-id="7c463-178">**Etiket** alanına **Seçenekleri gizle** yazın.</span><span class="sxs-lookup"><span data-stu-id="7c463-178">In the **Label** field, enter **Suppress options**.</span></span>
    5. <span data-ttu-id="7c463-179">**Operasyonlar veri türü adı** alanında, **NoYes** yazın veya girin.</span><span class="sxs-lookup"><span data-stu-id="7c463-179">In the **Operations data type name** field, select or enter **NoYes**.</span></span>
    6. <span data-ttu-id="7c463-180">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7c463-180">Select **OK**.</span></span>

8. <span data-ttu-id="7c463-181">Seçili **summarylines** biçim öğesi için, seçili biçim öğesiyle ilişkilendirilmiş Word içerik denetiminin ne zaman gizleneceğini belirten formülü yapılandırın:</span><span class="sxs-lookup"><span data-stu-id="7c463-181">For the selected **SummaryLines** format element, configure the formula to specify when the Word content control that is associated with the selected format element should be suppressed:</span></span>

    1. <span data-ttu-id="7c463-182">**Eşleme** sekmesinde, **kaldırılan** bölümünde **[Formül Tasarımcısı sayfasını](general-electronic-reporting-formula-designer.md)** sayfasını açmak için **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7c463-182">On the **Mapping** tab, in the **Removed** section, select **Edit** to open the **[Formula designer](general-electronic-reporting-formula-designer.md)** page.</span></span>
    2. <span data-ttu-id="7c463-183">**Formül** alanına, `uipSuppress = enumNoYes.Yes` formülünü girin.</span><span class="sxs-lookup"><span data-stu-id="7c463-183">In the **Formula** field, enter the formula `uipSuppress = enumNoYes.Yes`.</span></span>
    3. <span data-ttu-id="7c463-184">**Kaydet**'i seçin ve sonra **Formül tasarımcısı** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="7c463-184">Select **Save**, and close the **Formula designer** page.</span></span>

        > [!NOTE]
        > <span data-ttu-id="7c463-185">Bu formül oluşturulan belgeye, **diğer tüm biçim öğeleri çalıştırıldıktan sonra** uygulanacaktır.</span><span class="sxs-lookup"><span data-stu-id="7c463-185">This formula will be applied to a generated document **after all other format elements are run**.</span></span> <span data-ttu-id="7c463-186">Bu formülü uygulamak için formülün yapılandırıldığı bir biçim öğesi (Bu örnekte **summarylines**) olarak etiketlenmiş bir Word içerik denetimi, oluşturulmuş bir belgede bulunur.</span><span class="sxs-lookup"><span data-stu-id="7c463-186">To apply this formula, a Word content control that is tagged as a format element that the formula is configured for (**SummaryLines** in this case) is found in a generated document.</span></span> <span data-ttu-id="7c463-187">Bu içerik denetimi, bulunduğu Word tablosu satırıyla birlikte tümüyle kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="7c463-187">That content control is then completely removed, together with the row in the Word table that holds it.</span></span> <span data-ttu-id="7c463-188">Özet bölümünün ayrıntılar satırı oluşturulan belgeden kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="7c463-188">The details row of the summary section is removed from the generated document.</span></span>
        >
        > <span data-ttu-id="7c463-189">Tasarım zamanında, kullandığınız Word şablonunda hiçbir içerik denetiminin, **kaldırılmış** özelliğin yapılandırıldığı bir biçim öğesinin adıyla eşleşen bir etikete sahip olmamasına rağmen, bir biçim öğesi için **kaldırılmış** formülü yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7c463-189">At design time, you might configure the **Removed** formula for a format element, even though no content control in the Word template that you're using has a tag that matches the name of a format element that the **Removed** property is configured for.</span></span> <span data-ttu-id="7c463-190">Tasarım zamanında biçimi doğruladığınızda, bu tutarsızlık hakkında bir [uyarı](er-components-inspections.md#i14) alırsınız.</span><span class="sxs-lookup"><span data-stu-id="7c463-190">When you validate the format at design time, you receive a [warning](er-components-inspections.md#i14) about this inconsistency.</span></span>
        >
        > <span data-ttu-id="7c463-191">Çalışma zamanında, Word şablonunda kullandığınız herhangi bir içerik denetiminin, **kaldırılmış** özelliğinin yapılandırıldığı bir biçim öğesinin adıyla eşleşen bir etiketi yoksa bir özel durum oluşur.</span><span class="sxs-lookup"><span data-stu-id="7c463-191">At runtime, an exception is thrown if no content control in the Word template that you're using has a tag that matches the name of a format element that the **Removed** property is configured for.</span></span>

    4. <span data-ttu-id="7c463-192">**Eşleme** sekmesinde, **kaldırılan** bölümünde, **Üst öğe ile** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7c463-192">On the **Mapping** tab, in the **Removed** section, set the **With parent** option to **Yes**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="7c463-193">Özet bölüm detaylarının bulunduğu satırın üst nesnesi olarak tüm Word tablosunu kaldırmak için bu seçeneği **Evet** olarak ayarlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="7c463-193">You must set this option to **Yes** to remove the whole Word table as the parent object of the row that holds the summary section details.</span></span> <span data-ttu-id="7c463-194">Bu seçeneği **Hayır** olarak ayarlarsanız , bölüm başlığı satırı oluşturulan belgede kalır.</span><span class="sxs-lookup"><span data-stu-id="7c463-194">If you set this option to **No**, the section header row remains in the generated document.</span></span>

9. <span data-ttu-id="7c463-195">Düzenlenebilir biçime yaptığınız değişiklikleri kaydetmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7c463-195">Select **Save** to save your changes to the editable format.</span></span>

    ![Word biçiminde oluşturulan çıktı](./media/er-design-configuration-word-suppress-controls-image3.gif)

## <a name="run-the-modified-format-to-create-word-output"></a><span data-ttu-id="7c463-197">Word çıktısı oluşturmak için değiştirilen biçimi yürütme</span><span class="sxs-lookup"><span data-stu-id="7c463-197">Run the modified format to create Word output</span></span>

1. <span data-ttu-id="7c463-198">**Borç hesapları** \> **Ödemeler** \> **Ödeme günlüğü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="7c463-198">Go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="7c463-199">Oluşturduğunuz ödeme günlüğünü seçin ve ardından **Satırlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7c463-199">Select the payment journal that you created, and then select **Lines**.</span></span>
3. <span data-ttu-id="7c463-200">**Satıcı ödemeleri** sayfasında, tüm satırları seçin ve ardından **ödeme durumu** \> **Yok**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="7c463-200">On the **Vendor payments** page, select all the rows, and then select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="7c463-201">**Ödemeleri oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="7c463-201">Select **Generate payments**.</span></span>
5. <span data-ttu-id="7c463-202">**Ödeme yöntemi** alanında **Elektronik**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7c463-202">In the **Method of payment** field, select **Electronic**.</span></span>
6. <span data-ttu-id="7c463-203">**Banka hesabı** alanında **GBSI OPER** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7c463-203">In the **Bank account** field, select **GBSI OPER**.</span></span>
7. <span data-ttu-id="7c463-204">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7c463-204">Select **OK**.</span></span>
8. <span data-ttu-id="7c463-205">**Elektronik rapor parametreleri** iletişim kutusunda **Özet bölümünü gizle** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7c463-205">In the **Electronic report parameters** dialog box, in the **Suppress summary section** field, select **Yes**.</span></span>
9. <span data-ttu-id="7c463-206">**Tamam**'ı seçin ve oluşturulan çıktıyı analiz edin.</span><span class="sxs-lookup"><span data-stu-id="7c463-206">Select **OK**, and analyze the generated output.</span></span>

    ![Word biçiminde oluşturulan çıktı](./media/er-design-configuration-word-suppress-controls-image4.gif)

    <span data-ttu-id="7c463-208">Gizlenmiş olduğu için, çıktıda Özet bölümü bulunmadığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="7c463-208">Notice that the output doesn't contain the summary section, because it has been suppressed.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7c463-209">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="7c463-209">Additional resources</span></span>

- [<span data-ttu-id="7c463-210">OPENXML formatında raporların oluşturulması için bir yapılandırma tasarlama</span><span class="sxs-lookup"><span data-stu-id="7c463-210">Design a configuration for generating reports in OPENXML format</span></span>](./tasks/er-design-reports-openxml-2016-11.md)
- [<span data-ttu-id="7c463-211">Word biçiminde raporlar oluşturmak için yeni ER yapılandırması tasarlama</span><span class="sxs-lookup"><span data-stu-id="7c463-211">Design a new ER configuration to generate reports in Word format</span></span>](er-design-configuration-word.md)
- [<span data-ttu-id="7c463-212">Word biçiminde raporlar oluşturmak için ER yapılandırmalarını Excel şablonlarıyla yeniden kullanma</span><span class="sxs-lookup"><span data-stu-id="7c463-212">Re-use ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)
- [<span data-ttu-id="7c463-213">Çalışma zamanı sorunlarını önlemek için yapılandırılmış ER bileşenini denetleme</span><span class="sxs-lookup"><span data-stu-id="7c463-213">Inspect the configured ER component to prevent runtime issues</span></span>](er-components-inspections.md#i14)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]