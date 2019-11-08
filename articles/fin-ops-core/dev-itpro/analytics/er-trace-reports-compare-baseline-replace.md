---
title: Oluşturulan ER raporları sonuçlarının izlenmesi ve temel değerlerle karşılaştırılmasına ilişkin geliştirmeler
description: Bu konu, 10.0.3 (Haziran 2019) sürümünde ER temel özelliklerinin Microsoft Dynamics 365 for Finance and Operations'da nasıl geliştirildiği hakkında bilgi sağlar.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 1e144e2623f3ddfafaee749bb334de40ef5aec1b
ms.sourcegitcommit: dd960cf07d8be791fd27c7bb72e6baa2d63ccd51
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/14/2019
ms.locfileid: "2578230"
---
# <a name="improvements-in-tracing-the-results-of-generated-er-reports-and-comparing-them-with-baseline-values"></a><span data-ttu-id="87107-103">Oluşturulan ER raporları sonuçlarının izlenmesi ve temel değerlerle karşılaştırılmasına ilişkin geliştirmeler</span><span class="sxs-lookup"><span data-stu-id="87107-103">Improvements in tracing the results of generated ER reports and comparing them with baseline values</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="87107-104">Bu konuda, Elektronik raporlama (ER) çerçevesinin temel özelliğinde yapılan ilk iyileştirmeler kümesi açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="87107-104">This topic describes the first set of improvements that have been made to the baseline feature of the Electronic reporting (ER) framework.</span></span> <span data-ttu-id="87107-105">Bu iyileştirmeler Microsoft Dynamics 365 for Finance and Operations 10.0.3 (Haziran 2019) sürümünde ve sonrasında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="87107-105">These improvements are available in Microsoft Dynamics 365 for Finance and Operations version 10.0.3 (June 2019) and later.</span></span>

## <a name="automate-the-setting-of-baseline-rules"></a><span data-ttu-id="87107-106">Temel kuralları ayarını otomatikleştirme</span><span class="sxs-lookup"><span data-stu-id="87107-106">Automate the setting of baseline rules</span></span>

<span data-ttu-id="87107-107">[Oluşturulan rapor sonuçlarını izleme ve bunları temel değerlerle karşılaştırma](er-trace-reports-compare-baseline.md) konusu ER formatındaki uygulamalar hakkında bilgi toplamak için ER çerçevesini nasıl yapılandıracağınızı ve bu uygulamaların sonuçlarını nasıl değerlendireceğinizi açıklar.</span><span class="sxs-lookup"><span data-stu-id="87107-107">The [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic explains how to configure the ER framework to collect information about ER format executions and evaluate the results of those executions.</span></span> <span data-ttu-id="87107-108">Bu konudaki örnekte, tamamlanması gereken adımlar gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="87107-108">The example in this topic shows the steps that must be completed.</span></span>

<span data-ttu-id="87107-109">Adımlara bir kaç örnek:</span><span class="sxs-lookup"><span data-stu-id="87107-109">Here are some of the steps:</span></span>

- <span data-ttu-id="87107-110">Giden dosya oluşturmak için bir ER biçimi çalıştırın ve dosyayı yerel olarak depolayın.</span><span class="sxs-lookup"><span data-stu-id="87107-110">Run an ER format to generate an outbound file, and store the file locally.</span></span>
- <span data-ttu-id="87107-111">Yerel olarak depolanan dosyayı bir ER biçimi için eklenmiş olan temel bir ek olarak ekleyin.</span><span class="sxs-lookup"><span data-stu-id="87107-111">Add the locally stored file as an attachment of the baseline that was added for an ER format.</span></span>
- <span data-ttu-id="87107-112">Eklenen temel için bir temel kuralı yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="87107-112">Configure the baseline rule for the added baseline.</span></span> <span data-ttu-id="87107-113">Bu yapılandırma aşağıdaki adımları içerir:</span><span class="sxs-lookup"><span data-stu-id="87107-113">This configuration includes the following steps:</span></span>

    - <span data-ttu-id="87107-114">Giden dosya oluşturmak için kullanılan bir ER biçimi öğesi belirtin.</span><span class="sxs-lookup"><span data-stu-id="87107-114">Specify an ER format element that is used to generate an outbound file.</span></span>
    - <span data-ttu-id="87107-115">Oluşturulan giden dosyaya başvuran eki seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-115">Select the attachment that refers to the generated outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="87107-116">Yeni ER özellikleri otomatik olmasını etkinleştirse bile bu adımların el ile gerçekleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="87107-116">These steps must be done manually, even though the new ER capabilities enable them to be automated.</span></span> <span data-ttu-id="87107-117">Bu özellik hakkında daha fazla bilgi edinmek için aşağıdaki örneği tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="87107-117">To learn more about this feature, complete the following example.</span></span>

## <a name="example-automate-the-setting-of-baseline-rules"></a><span data-ttu-id="87107-118">Örnek: Temel kurallar ayarını otomatikleştirme</span><span class="sxs-lookup"><span data-stu-id="87107-118">Example: Automate the setting of baseline rules</span></span>

<span data-ttu-id="87107-119">Bu örnekteki adımları tamamlamak için ilk önce [Oluşturulan rapor sonuçlarını izleme ve bunları temel değerlerle karşılaştırma](er-trace-reports-compare-baseline.md) yukardaki "Add a new baseline for a designed ER format" bölümünün adımlarını tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="87107-119">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, up through the "Add a new baseline for a designed ER format" section.</span></span>

### <a name="review-added-baseline"></a><span data-ttu-id="87107-120">Eklenen temeli inceleme</span><span class="sxs-lookup"><span data-stu-id="87107-120">Review added baseline</span></span>

1. <span data-ttu-id="87107-121">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="87107-121">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="87107-122">**Temelleri** seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-122">Select **Baselines**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="87107-123">Eylem Bölmesi'ndeki **Temeller** düğmesi yalnızca **Şirket içi hata ayıklama modu**'nda ER kullanıcı parametresi açıldığında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="87107-123">The **Baselines** button on the Action Pane is available only when the **Run in debug mode** ER user parameter is turned on for the current company.</span></span>

<span data-ttu-id="87107-124">Temel, seçilmiş **ER temellerini öğrenme biçimi** formatında eklendi ancak temel kuralları bu temel için henüz eklenmedi.</span><span class="sxs-lookup"><span data-stu-id="87107-124">The baseline has been added for the selected **Format to learn ER baselines** format, but the baseline rules haven't yet been added for this baseline.</span></span>

<span data-ttu-id="87107-125">![Elektronik raporlama biçim temelleri sayfası](media/GER-BaselineSample-AddBaseline2.PNG "Elektronik raporlama biçim temelleri sayfası ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="87107-125">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline2.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="87107-126">Yeni temel kuralı oluştur</span><span class="sxs-lookup"><span data-stu-id="87107-126">Make a new baseline rule</span></span>

1. <span data-ttu-id="87107-127">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="87107-127">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="87107-128">Ağaçta, **ER temelini öğrenme modeli**'ni genişletin.</span><span class="sxs-lookup"><span data-stu-id="87107-128">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="87107-129">Ağaçta **ER temelini öğrenme modeli\\ER temelini öğrenme biçimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-129">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="87107-130">**Sürümler** hızlı sekmesinde **Çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-130">On the **Versions** FastTab, select **Run**.</span></span>
5. <span data-ttu-id="87107-131">**Kimlik Gir** alanına, **1** yazın.</span><span class="sxs-lookup"><span data-stu-id="87107-131">In the **Enter Id** field, enter **1**.</span></span>
6. <span data-ttu-id="87107-132">**Temel dosyaları oluştur** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="87107-132">Set the **Make baseline files** option to **Yes**.</span></span>
7. <span data-ttu-id="87107-133">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-133">Select **OK**.</span></span>
8. <span data-ttu-id="87107-134">**Temelleri** seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-134">Select **Baselines**.</span></span>

    <span data-ttu-id="87107-135">![Elektronik raporlama biçim temelleri sayfası](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Elektronik raporlama biçim temelleri sayfası ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="87107-135">![Electronic reporting format baselines page](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

    <span data-ttu-id="87107-136">Oluşturulan giden dosya otomatik olarak yürütülen ER biçiminin temeline iliştirildi.</span><span class="sxs-lookup"><span data-stu-id="87107-136">The generated outbound file has been automatically attached to the baseline of the executed ER format.</span></span> <span data-ttu-id="87107-137">Temel kuralı bu temele otomatik olarak eklendi ve eklenen dosyaya referans da içeriyor.</span><span class="sxs-lookup"><span data-stu-id="87107-137">The baseline rule has been automatically added to this baseline and also contains the reference to the attached file.</span></span>

9. <span data-ttu-id="87107-138">**Ad** alanına, **Temel 1** yazın.</span><span class="sxs-lookup"><span data-stu-id="87107-138">In the **Name** field, enter **Baseline 1**.</span></span>
10. <span data-ttu-id="87107-139">**Dosya adı maskesi** alanında **.xml** girin.</span><span class="sxs-lookup"><span data-stu-id="87107-139">In the **File name mask** field, enter **.xml**.</span></span>
11. <span data-ttu-id="87107-140">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-140">Select **Save**.</span></span>

### <a name="run-the-format"></a><span data-ttu-id="87107-141">Biçimi çalıştır</span><span class="sxs-lookup"><span data-stu-id="87107-141">Run the format</span></span>

<span data-ttu-id="87107-142">Artık [Oluşturulan rapor sonuçlarını izleme ve bunları temel değerlerle karşılaştırma](er-trace-reports-compare-baseline.md) konusunun örneğindeki kalan adımları, "Tasarlanan ER biçimini çalıştırma ve sonuçları analiz etmek için günlüğü gözden geçirme" bölümünden başlayarak tamamlamaya hazırsınız.</span><span class="sxs-lookup"><span data-stu-id="87107-142">You're now ready to complete the remaining steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, starting from the "Run the designed ER format and review the log to analyze the results" section.</span></span>

> [!NOTE]
> <span data-ttu-id="87107-143">**Temel** hızlı sekmesinde otomatik olarak eklenen temel kurallarını sildiğinizde başvurulan ek otomatik olarak silinmez.</span><span class="sxs-lookup"><span data-stu-id="87107-143">When you delete the automatically added baseline rule on the **Baselines** FastTab, the referenced attachment isn't automatically deleted.</span></span>

## <a name="configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="87107-144">Temeli, ER çıktısının sürekli değişen kısımlarını yok sayacak şekilde yapılandırma</span><span class="sxs-lookup"><span data-stu-id="87107-144">Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="87107-145">Bir ER biçimi, biçim çalıştırıldığında değiştirilen bilgileri içerecek şekilde tasarlandığında, oluşturulan sonuçları temel değerleriyle karşılaştırmak üzere ER temel özelliğini kullanması için biçim gerekir.</span><span class="sxs-lookup"><span data-stu-id="87107-145">When an ER format has been designed to contain information that is changed when the format is run, the format must be required to use the ER baseline feature to compare the generated results with baseline values.</span></span> <span data-ttu-id="87107-146">Örneğin, bilgi işleme tarihi ve saati ya da üretilen bir belgenin farklı biçimlerdeki (genel benzersiz kimlik tanımlayıcı\[GUID\], vb.) benzersiz kimlik tanımlayıcısı olabilir.</span><span class="sxs-lookup"><span data-stu-id="87107-146">For example, the information might be the processing date and time or the unique identifier of a generated document in different formats (globally unique identifier \[GUID\], and so on).</span></span> <span data-ttu-id="87107-147">Yeni ER Me özellikleri temel kuralını, biçim yürütmesinin sonuçlarıyla temel değerlerini karşılaştırmak amacıyla kullanırken, bir ER biçiminin değiştirilebilir öğelerini yoksaymak için yapılandırmanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="87107-147">The new ER capabilities let you configure the baseline rule so that it ignores changeable elements of an ER format when the format is run with the purpose of comparing baseline values with the results of the format's execution.</span></span> <span data-ttu-id="87107-148">Bu özellik hakkında daha fazla bilgi edinmek için aşağıdaki örneği tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="87107-148">To learn more about this feature, complete the following example.</span></span>

## <a name="example-configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="87107-149">Örnek: Temeli, ER çıktısının sürekli değişen kısımlarını yoksayacak şekilde yapılandırma</span><span class="sxs-lookup"><span data-stu-id="87107-149">Example: Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="87107-150">Bu örnekteki adımları tamamlamak için ilk önce [Oluşturulan rapor sonuçlarını izleme ve bunları temel değerlerle karşılaştırma](er-trace-reports-compare-baseline.md) konusunun örneklerinin adımlarını tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="87107-150">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic.</span></span>

### <a name="modify-a-configured-er-format"></a><span data-ttu-id="87107-151">Yapılandırılmış ER biçimini değiştirme</span><span class="sxs-lookup"><span data-stu-id="87107-151">Modify a configured ER format</span></span>

1. <span data-ttu-id="87107-152">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="87107-152">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="87107-153">Ağaçta, **ER temelini öğrenme modeli**'ni genişletin.</span><span class="sxs-lookup"><span data-stu-id="87107-153">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="87107-154">Ağaçta **ER temelini öğrenme modeli\\ER temelini öğrenme biçimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-154">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="87107-155">**Tasarımcı**’yı seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-155">Select **Designer**.</span></span>
5. <span data-ttu-id="87107-156">Ağaçta **Output\\Document**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-156">In the tree, select **Output\\Document**.</span></span>
6. <span data-ttu-id="87107-157">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-157">Select **Add**.</span></span>
7. <span data-ttu-id="87107-158">Açılan iletişim kutusunda, ağaçta **XML\\Attribute** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-158">In the drop-down dialog box, in the tree, select **XML\\Attribute**.</span></span>
8. <span data-ttu-id="87107-159">**Ad** alanına **ProcessingDateTime** girin.</span><span class="sxs-lookup"><span data-stu-id="87107-159">In the **Name** field, enter **ProcessingDateTime**.</span></span>
9. <span data-ttu-id="87107-160">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-160">Select **OK**.</span></span>
10. <span data-ttu-id="87107-161">Ağaçtaki**Eşleştirme** sekmesinde **Çıkış\\Belge\\ProcessingDateTime**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-161">On the **Mapping** tab, in the tree, select **Output\\Document\\ProcessingDateTime**.</span></span>
11. <span data-ttu-id="87107-162">**Formül düzenle**’yi seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-162">Select **Edit formula**.</span></span>
12. <span data-ttu-id="87107-163">**Formül** alanına şu ifadeyi girin: **DATETIMEFORMAT(NOW(), "O")**</span><span class="sxs-lookup"><span data-stu-id="87107-163">In the **Formula** field, enter the following expression: **DATETIMEFORMAT(NOW(), "O")**</span></span>
13. <span data-ttu-id="87107-164">**Kaydet**i seçin ve sonra **Test et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-164">Select **Save**, and then select **Test**.</span></span>
14. <span data-ttu-id="87107-165">Yapılandırılan ifadeyi yeniden test etmek için tekrar **Test et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-165">Select **Test** again to retest the configured expression.</span></span>

    <span data-ttu-id="87107-166">![Formül tasarımcı sayfası](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Formül tasarımcı sayfası ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="87107-166">![Formula designer page](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Screenshot of the Formula designer page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="87107-167">**Test sonucu** sekmesi, yapılandırılan ifadenin her çağrıldığında farklı bir tarih ve saat değeri döndürdüğünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="87107-167">The **Test result** tab shows that the configured expression returns a different date and time value whenever it's called.</span></span>

15. <span data-ttu-id="87107-168">**Formül tasarımcısı** sayfasını kapatın ve sonra **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-168">Close the **Formula designer** page, and then select **Save**.</span></span>

    <span data-ttu-id="87107-169">![Biçim tasarımcı sayfası](media/GER-BaselineSample-FormatMappingDesign2.PNG "Biçim tasarımcı sayfası ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="87107-169">![Format designer page](media/GER-BaselineSample-FormatMappingDesign2.PNG "Screenshot of the Format designer page")</span></span>

16. <span data-ttu-id="87107-170">**Biçim tasarımcısı** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="87107-170">Close the **Format designer** page.</span></span>

### <a name="remove-an-existing-baseline-rule"></a><span data-ttu-id="87107-171">Varolan temel kuralı kaldır</span><span class="sxs-lookup"><span data-stu-id="87107-171">Remove an existing baseline rule</span></span>

1. <span data-ttu-id="87107-172">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="87107-172">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="87107-173">**Temelleri** seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-173">Select **Baselines**.</span></span>
3. <span data-ttu-id="87107-174">Temel listesinde, **ER temellerini öğrenme biçimi**'ni yapılandırmak üzere biçim için yapılandırılan temeli seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-174">In the list of baselines, select the baseline that is configured for the **Format to learn ER baselines** format.</span></span>
4. <span data-ttu-id="87107-175">Daha önce yapılandırdığınız **Temeller** hızlı sekmesinde temel kuralını kaldırmak için **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-175">On the **Baselines** FastTab, select **Delete** to remove the baseline rule that you configured earlier.</span></span>

<span data-ttu-id="87107-176">![Elektronik raporlama biçim temelleri sayfası](media/GER-BaselineSample-AddBaseline3.PNG "Elektronik raporlama biçim temelleri sayfası ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="87107-176">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline3.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="define-replacements-for-bindings-of-designed-er-format"></a><span data-ttu-id="87107-177">Tasarlanan ER biçiminin bağlaması için değişiklikleri tanımlama</span><span class="sxs-lookup"><span data-stu-id="87107-177">Define replacements for bindings of designed ER format</span></span>

1. <span data-ttu-id="87107-178">**Yapılandırmalar** sayfasında, **Değişiklikler** hızlı sekmesinde **Seçili bileşenler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-178">On the **Configurations** page, on the **Replacements** FastTab, select **Select components**.</span></span>
2. <span data-ttu-id="87107-179">Biçim bileşenleri ağacında **Çıktı**'yı genişletin, **Çıktı\\Belge**'yi genişletin ve sonra onay kutusunu **Çıktı\\Belge\\ProcessingDateTime** için seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-179">In the format components tree, expand **Output**, expand **Output\\Document**, and then select the check box for **Output\\Document\\ProcessingDateTime**.</span></span>
3. <span data-ttu-id="87107-180">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-180">Select **OK**.</span></span>

<span data-ttu-id="87107-181">![Elektronik raporlama biçim temelleri sayfası](media/GER-BaselineSample-AddBaseline4.PNG "Elektronik raporlama biçim temelleri sayfası ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="87107-181">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline4.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

<span data-ttu-id="87107-182">Seçilen ER biçim bileşeni, **Değişiklikler** hızlı sekmesindeki bileşenler listesine eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="87107-182">The selected ER format component has been added to the list of components on the **Replacements** FastTab.</span></span> <span data-ttu-id="87107-183">Taban ER biçimi hata ayıklama modunda çalıştırıldığında, her bileşen için biçimin bağlaması, **Bağlama** sütununda gösterilen bağlama ile değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="87107-183">When the base ER format is run in debug mode, the format's binding for each component will be replaced by the binding that is shown in the **Binding** column.</span></span> <span data-ttu-id="87107-184">**Değişiklikler** hızlı sekmesinde listelenen bir bileşenin varsayılan bağlamasını değiştirmek için, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-184">To change the default binding for a component that is listed on the **Replacements** FastTab, select **Edit**.</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="87107-185">Yeni temel kuralı oluştur</span><span class="sxs-lookup"><span data-stu-id="87107-185">Make a new baseline rule</span></span>

<span data-ttu-id="87107-186">Bu konunun yukarısındaki "Örnek": temel kurallar ayarını otomatikleştirme" bölümündek adımları takip edin.</span><span class="sxs-lookup"><span data-stu-id="87107-186">Follow the steps in the "Example: Automate the setting of baseline rules" section earlier in this topic.</span></span> <span data-ttu-id="87107-187">Bir bildirim, giden dosyanın temel ayarları kullanılarak üretildiğini ve biçim bağlamalarının zorlanmış bir şekilde değiştirilmesini size bildirir.</span><span class="sxs-lookup"><span data-stu-id="87107-187">A notification warns you that the outbound file has been generated by using baseline settings, and that a forced replacement of the format bindings has occurred.</span></span>

<span data-ttu-id="87107-188">![Yapılandırma sayfasında Bildirim](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Yapılandırma sayfasında Bildirim ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="87107-188">![Notification on the Configurations page](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Screenshot of the notification on the Configurations page")</span></span>

### <a name="suppress-warnings-about-the-replacement-of-format-bindings"></a><span data-ttu-id="87107-189">Formaların değiştirilmesine ilişkin uyarıları gizleme</span><span class="sxs-lookup"><span data-stu-id="87107-189">Suppress warnings about the replacement of format bindings</span></span>

<span data-ttu-id="87107-190">Belirli ER. parametreleri ayarlayarak, biçim bağlamalarının değiştirilmesi hakkında uyarıcı bildirimleri gizleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="87107-190">By setting specific ER parameters, you can suppress notifications that warn about the replacement of format bindings.</span></span> <span data-ttu-id="87107-191">Bu gizleme Regression Suite Automation Tool kullanılarak biçim bağlamaları müdahalesiz modda değiştirildiğinde yararlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="87107-191">This suppression can be useful when format bindings are replaced in an unattended mode by using the Regression Suite Automation Tool.</span></span> <span data-ttu-id="87107-192">Bu durumda, uyarı çalışan test olayının hatası olarak kabul edilebilir.</span><span class="sxs-lookup"><span data-stu-id="87107-192">In this case, the warning can be considered a failure of the test case that is running.</span></span>

1. <span data-ttu-id="87107-193">**Yapılandırmalar** sayfasında, Eylem Bölmesinde **Yapılandırmalar** sekmesinde **Kullanıcı parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-193">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, select **User parameters**.</span></span>
2. <span data-ttu-id="87107-194">**Temel uyarıları bastır** seçeneğini **Evet** olarak ayarlayıp **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-194">Set the **Suppress baseline warnings** option to **Yes**, and then select **OK**.</span></span>

### <a name="review-the-generated-baseline-file"></a><span data-ttu-id="87107-195">Oluşturulan temel dosyayı gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="87107-195">Review the generated baseline file</span></span>

1. <span data-ttu-id="87107-196">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="87107-196">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="87107-197">**Temelleri** seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-197">Select **Baselines**.</span></span>
3. <span data-ttu-id="87107-198">**Ekler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-198">Select **Attachments**.</span></span>
    > [!NOTE]
    > <span data-ttu-id="87107-199">Oluşturulan dosya, formatın bağlayıcısından değil, eklenen temel kuralda yapılandırılan bağlamanın işlem tarih ve saat metnini (**"#"**) içerir.</span><span class="sxs-lookup"><span data-stu-id="87107-199">The generated file contains the processing date and time text (**"#"**) from the binding that was configured in the added baseline rule, not from the format's binding.</span></span>
    
4. <span data-ttu-id="87107-200">**Ekler** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="87107-200">Close the **Attachments** page.</span></span>

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a><span data-ttu-id="87107-201">Tasarlanan ER biçimini çalıştırma ve sonuçları analiz etmek için günlüğü gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="87107-201">Run the designed ER format and review the log to analyze the results</span></span>

1. <span data-ttu-id="87107-202">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="87107-202">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="87107-203">Ağaçta, **ER temelini öğrenme modeli**'ni genişletin.</span><span class="sxs-lookup"><span data-stu-id="87107-203">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="87107-204">Ağaçta **ER temelini öğrenme modeli\\ER temelini öğrenme biçimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-204">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="87107-205">**Sürümler** hızlı sekmesinde **Çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-205">On the **Versions** FastTab select **Run**.</span></span>
5. <span data-ttu-id="87107-206">**Kimlik Gir** alanına, **1** yazın.</span><span class="sxs-lookup"><span data-stu-id="87107-206">In the **Enter Id** field, type **1**.</span></span>
6. <span data-ttu-id="87107-207">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-207">Select **OK**.</span></span>
7. <span data-ttu-id="87107-208">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar hata ayıklama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="87107-208">Go to **Organization administration** \> **Electronic reporting** \> **Configuration debug logs**.</span></span>

<span data-ttu-id="87107-209">Yürütme günlükleri, oluşturulan dosyanın yapılandırılmış bir temelle karşılaştırılmasının sonuçlarıyla ilgili bilgiler içerir.</span><span class="sxs-lookup"><span data-stu-id="87107-209">The execution log contains information about the results of the comparison of the generated file with the configured baseline.</span></span> <span data-ttu-id="87107-210">Bu günlükte, yürütülen biçim, giden dosyasında sürekli değişen bir tarih ve saat değeri girmek için bağlama içerse bile oluşturulan dosya ve taban temelin eşit olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="87107-210">The log indicates that the generated file and the baseline are equal, even though the executed format contains the binding to enter a constantly changing date and time value in the outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="87107-211">Giden dosya, biçimlerin bağlarını değiştirmeye zorlayan temel ayarlar kullanılarak oluşturulmuş olsa da değiştirme ile ilgili herhangi bir uyarı almazsınız.</span><span class="sxs-lookup"><span data-stu-id="87107-211">Although the outbound file has been generated by using baseline settings that force the replacement of the format's bindings, you don't receive any warnings about the replacement.</span></span>

## <a name="exchange-baseline-settings-between-environments"></a><span data-ttu-id="87107-212">Ortamlar arasında Döviz temeli ayarları</span><span class="sxs-lookup"><span data-stu-id="87107-212">Exchange baseline settings between environments</span></span>

### <a name="export-baseline-settings"></a><span data-ttu-id="87107-213">Dışa aktarma temeli ayarları</span><span class="sxs-lookup"><span data-stu-id="87107-213">Export baseline settings</span></span>

<span data-ttu-id="87107-214">Yeni ER özellikleri, geçerli ortamdan seçili ER biçimi için temel ayarlarını dışa aktarmanız ve bunları XML dosyaları olarak depolayabilmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="87107-214">The new ER capabilities let you export baseline settings for the selected ER format from the current environment and store them as XML files.</span></span> 

<span data-ttu-id="87107-215">Temel ayarlarını dışa aktarmak için **Elektronik raporlama biçim temelleri** sayfasında **Dışa aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-215">To export baseline settings, on the **Electronic reporting format baselines** page, select **Export**.</span></span>

### <a name="import-baseline-settings"></a><span data-ttu-id="87107-216">Temel ayarları içe aktar</span><span class="sxs-lookup"><span data-stu-id="87107-216">Import baseline settings</span></span>

<span data-ttu-id="87107-217">Dışa aktarılan temel ayarları farklı bir ortama aktarılabilir.</span><span class="sxs-lookup"><span data-stu-id="87107-217">Exported baseline settings can be imported into a different environment.</span></span> <span data-ttu-id="87107-218">Ortam önce bir ER biçimi olarak içe aktarılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="87107-218">The environment must first be imported as an ER format.</span></span> <span data-ttu-id="87107-219">Bundan sonra temel ayarları içe aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="87107-219">You can then import the baseline settings.</span></span>

<span data-ttu-id="87107-220">Yerel olarak depolanmış bir XML dosyasından ayarları dışa aktarmak için **Elekronik raporlama biçimi temelleri** sayfasında **Dışa aktarı**'ı seçin ve sonra XML dosyasını seçmek için **Gözat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-220">To import baseline settings from a locally stored XML file, on the **Electronic reporting format baselines** page, select **Import**, and then select **Browse** to select the XML file.</span></span>

<span data-ttu-id="87107-221">![Temel ayarları iletişim kutusunu içe aktar](media/GER-BaselineSample-ImportBaseline1.PNG "Temel ayarları iletişim kutusunu içe aktar ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="87107-221">![Import baseline settings dialog box](media/GER-BaselineSample-ImportBaseline1.PNG "Screenshot of the Import baseline settings dialog box")</span></span>

<span data-ttu-id="87107-222">Geçerli belge yönetimi ayarları ve seçili belge türü temel alınarak Microsoft SharePoint Sunucusunda depolanan bir XML dosyasından temel ayarları almak için **Elektronik raporlama biçim temelleri** sayfasında **Kaynaktan içe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-222">To import baseline settings from an XML file that is stored on the Microsoft SharePoint Server, based on the current Document management settings and the selected document type, on the **Electronic reporting format baselines** page, select **Import from source**.</span></span> <span data-ttu-id="87107-223">Sonra belge türünü ve XML dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="87107-223">Then select the document type and the XML file.</span></span> <span data-ttu-id="87107-224">SharePoint klasöre erişmek için gereken belge türü önceden yapılandırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="87107-224">The required document type to access the SharePoint folder must be configured in advance.</span></span>

<span data-ttu-id="87107-225">![Kaynak iletişim kutusundan içe aktar](media/GER-BaselineSample-ImportBaseline2.PNG "Kaynak iletişim kutusundan içe aktar ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="87107-225">![Import from source dialog box](media/GER-BaselineSample-ImportBaseline2.PNG "Screenshot of the Import from source dialog box")</span></span>

> [!NOTE]
> <span data-ttu-id="87107-226">Görev kaydediciyi **Kaynağı içe aktar** iletişim kutusunda gereken belge türünü ve dosya adını seçmeye yönelik adımları kaydetmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="87107-226">You can use Task recorder to record the steps for selecting the required document type and the file name in the **Import from source** dialog box.</span></span> <span data-ttu-id="87107-227">Bu şekilde, gerekli temel ayarları SharePoint sunucusunda tutabilir ve Regression Suite Automation Tool'u kullanarak otomatik testleri çalıştırdığınızda, bunları bir görev kaydı yürüterek otomatik olarak alabilirsiniz .</span><span class="sxs-lookup"><span data-stu-id="87107-227">In this way, you can keep required baseline settings on SharePoint Server and then automatically import them by playing a task recording when you run automated tests by using the Regression Suite Automation Tool.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="87107-228">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="87107-228">Additional resources</span></span>

- [<span data-ttu-id="87107-229">Oluşturulan rapor sonuçlarını izleme ve temel değerlerle karşılaştırma</span><span class="sxs-lookup"><span data-stu-id="87107-229">Trace generated report results and compare them with baseline values</span></span>](er-trace-reports-compare-baseline.md)
- [<span data-ttu-id="87107-230">Görev kaydedici</span><span class="sxs-lookup"><span data-stu-id="87107-230">Task recorder</span></span>](../user-interface/task-recorder.md)
