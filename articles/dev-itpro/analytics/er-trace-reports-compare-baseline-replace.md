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
ms.openlocfilehash: 222a415f686c8028fc2a414f97eed0291d850ae7
ms.sourcegitcommit: 9917df8c0c9320955c61186cd922c8df894a4f25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/21/2019
ms.locfileid: "1700694"
---
# <a name="improvements-in-tracing-the-results-of-generated-er-reports-and-comparing-them-with-baseline-values"></a><span data-ttu-id="c59c1-103">Oluşturulan ER raporları sonuçlarının izlenmesi ve temel değerlerle karşılaştırılmasına ilişkin geliştirmeler</span><span class="sxs-lookup"><span data-stu-id="c59c1-103">Improvements in tracing the results of generated ER reports and comparing them with baseline values</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c59c1-104">Bu konuda, Elektronik raporlama (ER) çerçevesinin temel özelliğinde yapılan ilk iyileştirmeler kümesi açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="c59c1-104">This topic describes the first set of improvements that have been made to the baseline feature of the Electronic reporting (ER) framework.</span></span> <span data-ttu-id="c59c1-105">Bu iyileştirmeler Microsoft Dynamics 365 for Finance and Operations 10.0.3 (Haziran 2019) sürümünde ve sonrasında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c59c1-105">These improvements are available in Microsoft Dynamics 365 for Finance and Operations version 10.0.3 (June 2019) and later.</span></span>

## <a name="automate-the-setting-of-baseline-rules"></a><span data-ttu-id="c59c1-106">Temel kuralları ayarını otomatikleştirme</span><span class="sxs-lookup"><span data-stu-id="c59c1-106">Automate the setting of baseline rules</span></span>

<span data-ttu-id="c59c1-107">[Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) konusu ER formatındaki uygulamalar hakkında bilgi toplamak için ER çerçevesini nasıl yapılandıracağınızı ve bu uygulamaların sonuçlarını nasıl değerlendireceğinizi açıklar.</span><span class="sxs-lookup"><span data-stu-id="c59c1-107">The [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic explains how to configure the ER framework to collect information about ER format executions and evaluate the results of those executions.</span></span> <span data-ttu-id="c59c1-108">Bu konudaki örnekte, tamamlanması gereken adımlar gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="c59c1-108">The example in this topic shows the steps that must be completed.</span></span>

<span data-ttu-id="c59c1-109">Adımlara bir kaç örnek:</span><span class="sxs-lookup"><span data-stu-id="c59c1-109">Here are some of the steps:</span></span>

- <span data-ttu-id="c59c1-110">Giden dosya oluşturmak için bir ER biçimi çalıştırın ve dosyayı yerel olarak depolayın.</span><span class="sxs-lookup"><span data-stu-id="c59c1-110">Run an ER format to generate an outbound file, and store the file locally.</span></span>
- <span data-ttu-id="c59c1-111">Yerel olarak depolanan dosyayı bir ER biçimi için eklenmiş olan temel bir ek olarak ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-111">Add the locally stored file as an attachment of the baseline that was added for an ER format.</span></span>
- <span data-ttu-id="c59c1-112">Eklenen temel için bir temel kuralı yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="c59c1-112">Configure the baseline rule for the added baseline.</span></span> <span data-ttu-id="c59c1-113">Bu yapılandırma aşağıdaki adımları içerir:</span><span class="sxs-lookup"><span data-stu-id="c59c1-113">This configuration includes the following steps:</span></span>

    - <span data-ttu-id="c59c1-114">Giden dosya oluşturmak için kullanılan bir ER biçimi öğesi belirtin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-114">Specify an ER format element that is used to generate an outbound file.</span></span>
    - <span data-ttu-id="c59c1-115">Oluşturulan giden dosyaya başvuran eki seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-115">Select the attachment that refers to the generated outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="c59c1-116">Yeni ER özellikleri otomatik olmasını etkinleştirse bile bu adımların el ile gerçekleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="c59c1-116">These steps must be done manually, even though the new ER capabilities enable them to be automated.</span></span> <span data-ttu-id="c59c1-117">Bu özellik hakkında daha fazla bilgi edinmek için aşağıdaki örneği tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="c59c1-117">To learn more about this feature, complete the following example.</span></span>

## <a name="example-automate-the-setting-of-baseline-rules"></a><span data-ttu-id="c59c1-118">Örnek: Temel kurallar ayarını otomatikleştirme</span><span class="sxs-lookup"><span data-stu-id="c59c1-118">Example: Automate the setting of baseline rules</span></span>

<span data-ttu-id="c59c1-119">Bu örnekteki adımları tamamlamak için ilk önce [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) yukardaki "Add a new baseline for a designed ER format" bölümünün adımlarını tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="c59c1-119">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, up through the "Add a new baseline for a designed ER format" section.</span></span>

### <a name="review-added-baseline"></a><span data-ttu-id="c59c1-120">Eklenen temeli inceleme</span><span class="sxs-lookup"><span data-stu-id="c59c1-120">Review added baseline</span></span>

1. <span data-ttu-id="c59c1-121">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-121">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="c59c1-122">**Temelleri** seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-122">Select **Baselines**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c59c1-123">Eylem Bölmesi'ndeki **Temeller** düğmesi yalnızca **Şirket içi hata ayıklama modu**'nda ER kullanıcı parametresi açıldığında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c59c1-123">The **Baselines** button on the Action Pane is available only when the **Run in debug mode** ER user parameter is turned on for the current company.</span></span>

<span data-ttu-id="c59c1-124">Temel, seçilmiş **ER temellerini öğrenme biçimi** formatında eklendi ancak temel kuralları bu temel için henüz eklenmedi.</span><span class="sxs-lookup"><span data-stu-id="c59c1-124">The baseline has been added for the selected **Format to learn ER baselines** format, but the baseline rules haven't yet been added for this baseline.</span></span>

<span data-ttu-id="c59c1-125">![Elektronik raporlama biçim temelleri sayfası](media/GER-BaselineSample-AddBaseline2.PNG "Elektronik raporlama biçim temelleri sayfası ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="c59c1-125">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline2.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="c59c1-126">Yeni temel kuralı oluştur</span><span class="sxs-lookup"><span data-stu-id="c59c1-126">Make a new baseline rule</span></span>

1. <span data-ttu-id="c59c1-127">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-127">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="c59c1-128">Ağaçta, **ER temelini öğrenme modeli**'ni genişletin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-128">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="c59c1-129">Ağaçta **ER temelini öğrenme modeli\\ER temelini öğrenme biçimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-129">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="c59c1-130">**Sürümler** hızlı sekmesinde **Çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-130">On the **Versions** FastTab, select **Run**.</span></span>
5. <span data-ttu-id="c59c1-131">**Kimlik Gir** alanına, **1** yazın.</span><span class="sxs-lookup"><span data-stu-id="c59c1-131">In the **Enter Id** field, enter **1**.</span></span>
6. <span data-ttu-id="c59c1-132">**Temel dosyaları oluştur** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c59c1-132">Set the **Make baseline files** option to **Yes**.</span></span>
7. <span data-ttu-id="c59c1-133">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-133">Select **OK**.</span></span>

    <span data-ttu-id="c59c1-134">![Elektronik rapor parametreleri iletişim kutusu](media/GER-BaselineSample-FormatRunToMakeBaselineFile3.PNG "Elektronik rapor parametreleri iletişim kutusu ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="c59c1-134">![Electronic report parameters dialog box](media/GER-BaselineSample-FormatRunToMakeBaselineFile3.PNG "Screenshot of the Electronic report parameters dialog box")</span></span>

8. <span data-ttu-id="c59c1-135">**Temelleri** seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-135">Select **Baselines**.</span></span>

    <span data-ttu-id="c59c1-136">![Elektronik raporlama biçim temelleri sayfası](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Elektronik raporlama biçim temelleri sayfası ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="c59c1-136">![Electronic reporting format baselines page](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

    <span data-ttu-id="c59c1-137">Oluşturulan giden dosya otomatik olarak yürütülen ER biçiminin temeline iliştirildi.</span><span class="sxs-lookup"><span data-stu-id="c59c1-137">The generated outbound file has been automatically attached to the baseline of the executed ER format.</span></span> <span data-ttu-id="c59c1-138">Temel kuralı bu temele otomatik olarak eklendi ve eklenen dosyaya referans da içeriyor.</span><span class="sxs-lookup"><span data-stu-id="c59c1-138">The baseline rule has been automatically added to this baseline and also contains the reference to the attached file.</span></span>

9. <span data-ttu-id="c59c1-139">**Ad** alanına, **Temel 1** yazın.</span><span class="sxs-lookup"><span data-stu-id="c59c1-139">In the **Name** field, enter **Baseline 1**.</span></span>
10. <span data-ttu-id="c59c1-140">**Dosya adı maskesi** alanında **.xml** girin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-140">In the **File name mask** field, enter **.xml**.</span></span>
11. <span data-ttu-id="c59c1-141">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-141">Select **Save**.</span></span>

### <a name="run-the-format"></a><span data-ttu-id="c59c1-142">Biçimi çalıştır</span><span class="sxs-lookup"><span data-stu-id="c59c1-142">Run the format</span></span>

<span data-ttu-id="c59c1-143">Artık [Oluşturulan rapor sonuçlarını izleme ve bunları temel değerlerle karşılaştırma](er-trace-reports-compare-baseline.md) konusunun örneğindeki kalan adımları, "Tasarlanan ER biçimini çalıştırma ve sonuçları analiz etmek için günlüğü gözden geçirme" bölümünden başlayarak tamamlamaya hazırsınız.</span><span class="sxs-lookup"><span data-stu-id="c59c1-143">You're now ready to complete the remaining steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, starting from the "Run the designed ER format and review the log to analyze the results" section.</span></span>

> [!NOTE]
> <span data-ttu-id="c59c1-144">**Temel** hızlı sekmesinde otomatik olarak eklenen temel kurallarını sildiğinizde başvurulan ek otomatik olarak silinmez.</span><span class="sxs-lookup"><span data-stu-id="c59c1-144">When you delete the automatically added baseline rule on the **Baselines** FastTab, the referenced attachment isn't automatically deleted.</span></span>

## <a name="configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="c59c1-145">Temeli, ER çıktısının sürekli değişen kısımlarını yok sayacak şekilde yapılandırma</span><span class="sxs-lookup"><span data-stu-id="c59c1-145">Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="c59c1-146">Bir ER biçimi, biçim çalıştırıldığında değiştirilen bilgileri içerecek şekilde tasarlandığında, oluşturulan sonuçları temel değerleriyle karşılaştırmak üzere ER temel özelliğini kullanması için biçim gerekir.</span><span class="sxs-lookup"><span data-stu-id="c59c1-146">When an ER format has been designed to contain information that is changed when the format is run, the format must be required to use the ER baseline feature to compare the generated results with baseline values.</span></span> <span data-ttu-id="c59c1-147">Örneğin, bilgi işleme tarihi ve saati ya da üretilen bir belgenin farklı biçimlerdeki (genel benzersiz kimlik tanımlayıcı\[GUID\], vb.) benzersiz kimlik tanımlayıcısı olabilir.</span><span class="sxs-lookup"><span data-stu-id="c59c1-147">For example, the information might be the processing date and time or the unique identifier of a generated document in different formats (globally unique identifier \[GUID\], and so on).</span></span> <span data-ttu-id="c59c1-148">Yeni ER Me özellikleri temel kuralını, biçim yürütmesinin sonuçlarıyla temel değerlerini karşılaştırmak amacıyla kullanırken, bir ER biçiminin değiştirilebilir öğelerini yoksaymak için yapılandırmanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="c59c1-148">The new ER capabilities let you configure the baseline rule so that it ignores changeable elements of an ER format when the format is run with the purpose of comparing baseline values with the results of the format's execution.</span></span> <span data-ttu-id="c59c1-149">Bu özellik hakkında daha fazla bilgi edinmek için aşağıdaki örneği tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="c59c1-149">To learn more about this feature, complete the following example.</span></span>

## <a name="example-configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="c59c1-150">Örnek: Temeli, ER çıktısının sürekli değişen kısımlarını yoksayacak şekilde yapılandırma</span><span class="sxs-lookup"><span data-stu-id="c59c1-150">Example: Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="c59c1-151">Bu örnekteki adımları tamamlamak için ilk önce [Oluşturulan rapor sonuçlarını izleme ve bunları temel değerlerle karşılaştırma](er-trace-reports-compare-baseline.md) konusunun örneklerinin adımlarını tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="c59c1-151">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic.</span></span>

### <a name="modify-a-configured-er-format"></a><span data-ttu-id="c59c1-152">Yapılandırılmış ER biçimini değiştirme</span><span class="sxs-lookup"><span data-stu-id="c59c1-152">Modify a configured ER format</span></span>

1. <span data-ttu-id="c59c1-153">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-153">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="c59c1-154">Ağaçta, **ER temelini öğrenme modeli**'ni genişletin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-154">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="c59c1-155">Ağaçta **ER temelini öğrenme modeli\\ER temelini öğrenme biçimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-155">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="c59c1-156">**Tasarımcı**’yı seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-156">Select **Designer**.</span></span>
5. <span data-ttu-id="c59c1-157">Ağaçta **Output\\Document**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-157">In the tree, select **Output\\Document**.</span></span>
6. <span data-ttu-id="c59c1-158">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-158">Select **Add**.</span></span>
7. <span data-ttu-id="c59c1-159">Açılan iletişim kutusunda, ağaçta **XML\\Attribute** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-159">In the drop-down dialog box, in the tree, select **XML\\Attribute**.</span></span>
8. <span data-ttu-id="c59c1-160">**Ad** alanına **ProcessingDateTime** girin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-160">In the **Name** field, enter **ProcessingDateTime**.</span></span>
9. <span data-ttu-id="c59c1-161">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-161">Select **OK**.</span></span>
10. <span data-ttu-id="c59c1-162">Ağaçtaki**Eşleştirme** sekmesinde **Çıkış\\Belge\\ProcessingDateTime**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-162">On the **Mapping** tab, in the tree, select **Output\\Document\\ProcessingDateTime**.</span></span>
11. <span data-ttu-id="c59c1-163">**Formül düzenle**’yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-163">Select **Edit formula**.</span></span>
12. <span data-ttu-id="c59c1-164">**Formül** alanına şu ifadeyi girin: **DATETIMEFORMAT(NOW(), "O")**</span><span class="sxs-lookup"><span data-stu-id="c59c1-164">In the **Formula** field, enter the following expression: **DATETIMEFORMAT(NOW(), "O")**</span></span>
13. <span data-ttu-id="c59c1-165">**Kaydet**i seçin ve sonra **Test et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-165">Select **Save**, and then select **Test**.</span></span>
14. <span data-ttu-id="c59c1-166">Yapılandırılan ifadeyi yeniden test etmek için tekrar **Test et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-166">Select **Test** again to retest the configured expression.</span></span>

    <span data-ttu-id="c59c1-167">![Formül tasarımcı sayfası](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Formül tasarımcı sayfası ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="c59c1-167">![Formula designer page](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Screenshot of the Formula designer page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="c59c1-168">**Test sonucu** sekmesi, yapılandırılan ifadenin her çağrıldığında farklı bir tarih ve saat değeri döndürdüğünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="c59c1-168">The **Test result** tab shows that the configured expression returns a different date and time value whenever it's called.</span></span>

15. <span data-ttu-id="c59c1-169">**Formül tasarımcısı** sayfasını kapatın ve sonra **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-169">Close the **Formula designer** page, and then select **Save**.</span></span>

    <span data-ttu-id="c59c1-170">![Biçim tasarımcı sayfası](media/GER-BaselineSample-FormatMappingDesign2.PNG "Biçim tasarımcı sayfası ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="c59c1-170">![Format designer page](media/GER-BaselineSample-FormatMappingDesign2.PNG "Screenshot of the Format designer page")</span></span>

16. <span data-ttu-id="c59c1-171">**Biçim tasarımcısı** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="c59c1-171">Close the **Format designer** page.</span></span>

### <a name="remove-an-existing-baseline-rule"></a><span data-ttu-id="c59c1-172">Varolan temel kuralı kaldır</span><span class="sxs-lookup"><span data-stu-id="c59c1-172">Remove an existing baseline rule</span></span>

1. <span data-ttu-id="c59c1-173">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-173">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="c59c1-174">**Temelleri** seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-174">Select **Baselines**.</span></span>
3. <span data-ttu-id="c59c1-175">Temel listesinde, **ER temellerini öğrenme biçimi**'ni yapılandırmak üzere biçim için yapılandırılan temeli seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-175">In the list of baselines, select the baseline that is configured for the **Format to learn ER baselines** format.</span></span>
4. <span data-ttu-id="c59c1-176">Daha önce yapılandırdığınız **Temeller** hızlı sekmesinde temel kuralını kaldırmak için **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-176">On the **Baselines** FastTab, select **Delete** to remove the baseline rule that you configured earlier.</span></span>

<span data-ttu-id="c59c1-177">![Elektronik raporlama biçim temelleri sayfası](media/GER-BaselineSample-AddBaseline3.PNG "Elektronik raporlama biçim temelleri sayfası ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="c59c1-177">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline3.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="define-replacements-for-bindings-of-designed-er-format"></a><span data-ttu-id="c59c1-178">Tasarlanan ER biçiminin bağlaması için değişiklikleri tanımlama</span><span class="sxs-lookup"><span data-stu-id="c59c1-178">Define replacements for bindings of designed ER format</span></span>

1. <span data-ttu-id="c59c1-179">**Yapılandırmalar** sayfasında, **Değişiklikler** hızlı sekmesinde **Seçili bileşenler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-179">On the **Configurations** page, on the **Replacements** FastTab, select **Select components**.</span></span>
2. <span data-ttu-id="c59c1-180">Biçim bileşenleri ağacında **Çıktı**'yı genişletin, **Çıktı\\Belge**'yi genişletin ve sonra onay kutusunu **Çıktı\\Belge\\ProcessingDateTime** için seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-180">In the format components tree, expand **Output**, expand **Output\\Document**, and then select the check box for **Output\\Document\\ProcessingDateTime**.</span></span>

    <span data-ttu-id="c59c1-181">![Bileşenler iletişim kutusunu seçme](media/GER-BaselineSample-SelectComponentForBindingReplacement.PNG "Bileşenler iletişim kutusunu seçme ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="c59c1-181">![Select Components dialog box](media/GER-BaselineSample-SelectComponentForBindingReplacement.PNG "Screenshot of the Select Components dialog box")</span></span>

3. <span data-ttu-id="c59c1-182">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-182">Select **OK**.</span></span>

<span data-ttu-id="c59c1-183">![Elektronik raporlama biçim temelleri sayfası](media/GER-BaselineSample-AddBaseline4.PNG "Elektronik raporlama biçim temelleri sayfası ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="c59c1-183">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline4.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

<span data-ttu-id="c59c1-184">Seçilen ER biçim bileşeni, **Değişiklikler** hızlı sekmesindeki bileşenler listesine eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="c59c1-184">The selected ER format component has been added to the list of components on the **Replacements** FastTab.</span></span> <span data-ttu-id="c59c1-185">Taban ER biçimi hata ayıklama modunda çalıştırıldığında, her bileşen için biçimin bağlaması, **Bağlama** sütununda gösterilen bağlama ile değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="c59c1-185">When the base ER format is run in debug mode, the format's binding for each component will be replaced by the binding that is shown in the **Binding** column.</span></span> <span data-ttu-id="c59c1-186">**Değişiklikler** hızlı sekmesinde listelenen bir bileşenin varsayılan bağlamasını değiştirmek için, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-186">To change the default binding for a component that is listed on the **Replacements** FastTab, select **Edit**.</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="c59c1-187">Yeni temel kuralı oluştur</span><span class="sxs-lookup"><span data-stu-id="c59c1-187">Make a new baseline rule</span></span>

<span data-ttu-id="c59c1-188">Bu konunun yukarısındaki "Örnek": temel kurallar ayarını otomatikleştirme" bölümündek adımları takip edin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-188">Follow the steps in the "Example: Automate the setting of baseline rules" section earlier in this topic.</span></span> <span data-ttu-id="c59c1-189">Bir bildirim, giden dosyanın temel ayarları kullanılarak üretildiğini ve biçim bağlamalarının zorlanmış bir şekilde değiştirilmesini size bildirir.</span><span class="sxs-lookup"><span data-stu-id="c59c1-189">A notification warns you that the outbound file has been generated by using baseline settings, and that a forced replacement of the format bindings has occurred.</span></span>

<span data-ttu-id="c59c1-190">![Yapılandırma sayfasında Bildirim](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Yapılandırma sayfasında Bildirim ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="c59c1-190">![Notification on the Configurations page](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Screenshot of the notification on the Configurations page")</span></span>

### <a name="suppress-warnings-about-the-replacement-of-format-bindings"></a><span data-ttu-id="c59c1-191">Formaların değiştirilmesine ilişkin uyarıları gizleme</span><span class="sxs-lookup"><span data-stu-id="c59c1-191">Suppress warnings about the replacement of format bindings</span></span>

<span data-ttu-id="c59c1-192">Belirli ER. parametreleri ayarlayarak, biçim bağlamalarının değiştirilmesi hakkında uyarıcı bildirimleri gizleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c59c1-192">By setting specific ER parameters, you can suppress notifications that warn about the replacement of format bindings.</span></span> <span data-ttu-id="c59c1-193">Bu gizleme Regression Suite Automation Tool kullanılarak biçim bağlamaları müdahalesiz modda değiştirildiğinde yararlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="c59c1-193">This suppression can be useful when format bindings are replaced in an unattended mode by using the Regression Suite Automation Tool.</span></span> <span data-ttu-id="c59c1-194">Bu durumda, uyarı çalışan test olayının hatası olarak kabul edilebilir.</span><span class="sxs-lookup"><span data-stu-id="c59c1-194">In this case, the warning can be considered a failure of the test case that is running.</span></span>

1. <span data-ttu-id="c59c1-195">**Yapılandırmalar** sayfasında, Eylem Bölmesinde **Yapılandırmalar** sekmesinde **Kullanıcı parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-195">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, select **User parameters**.</span></span>
2. <span data-ttu-id="c59c1-196">**Temel uyarıları bastır** seçeneğini **Evet** olarak ayarlayıp **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-196">Set the **Suppress baseline warnings** option to **Yes**, and then select **OK**.</span></span>

<span data-ttu-id="c59c1-197">![Kullanıcı parametreleri iletişim kutusu](media/GER-BaselineSample-ERUserParameters1.png "Kullanıcı parametreleri iletişim kutusu ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="c59c1-197">![User parameters dialog box](media/GER-BaselineSample-ERUserParameters1.png "Screenshot of the User parameters dialog box")</span></span>

### <a name="review-the-generated-baseline-file"></a><span data-ttu-id="c59c1-198">Oluşturulan temel dosyayı gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-198">Review the generated baseline file</span></span>

1. <span data-ttu-id="c59c1-199">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-199">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="c59c1-200">**Temelleri** seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-200">Select **Baselines**.</span></span>
3. <span data-ttu-id="c59c1-201">**Ekler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-201">Select **Attachments**.</span></span>

    <span data-ttu-id="c59c1-202">![Ekler sayfası](media/GER-BaselineSample-AttachedBaselineFile.PNG "Ekler sayfası ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="c59c1-202">![Attachments page](media/GER-BaselineSample-AttachedBaselineFile.PNG "Screenshot of the Attachments page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="c59c1-203">Oluşturulan dosya, formatın bağlayıcısından değil, eklenen temel kuralda yapılandırılan bağlamanın işlem tarih ve saat metnini (**"#"**) içerir.</span><span class="sxs-lookup"><span data-stu-id="c59c1-203">The generated file contains the processing date and time text (**"#"**) from the binding that was configured in the added baseline rule, not from the format's binding.</span></span>

4. <span data-ttu-id="c59c1-204">**Ekler** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="c59c1-204">Close the **Attachments** page.</span></span>

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a><span data-ttu-id="c59c1-205">Tasarlanan ER biçimini çalıştırma ve sonuçları analiz etmek için günlüğü gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="c59c1-205">Run the designed ER format and review the log to analyze the results</span></span>

1. <span data-ttu-id="c59c1-206">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-206">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="c59c1-207">Ağaçta, **ER temelini öğrenme modeli**'ni genişletin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-207">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="c59c1-208">Ağaçta **ER temelini öğrenme modeli\\ER temelini öğrenme biçimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-208">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="c59c1-209">**Sürümler** hızlı sekmesinde **Çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-209">On the **Versions** FastTab select **Run**.</span></span>
5. <span data-ttu-id="c59c1-210">**Kimlik Gir** alanına, **1** yazın.</span><span class="sxs-lookup"><span data-stu-id="c59c1-210">In the **Enter Id** field, type **1**.</span></span>
6. <span data-ttu-id="c59c1-211">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-211">Select **OK**.</span></span>
7. <span data-ttu-id="c59c1-212">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar hata ayıklama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-212">Go to **Organization administration** \> **Electronic reporting** \> **Configuration debug logs**.</span></span>

<span data-ttu-id="c59c1-213">Yürütme günlükleri, oluşturulan dosyanın yapılandırılmış bir temelle karşılaştırılmasının sonuçlarıyla ilgili bilgiler içerir.</span><span class="sxs-lookup"><span data-stu-id="c59c1-213">The execution log contains information about the results of the comparison of the generated file with the configured baseline.</span></span> <span data-ttu-id="c59c1-214">Bu günlükte, yürütülen biçim, giden dosyasında sürekli değişen bir tarih ve saat değeri girmek için bağlama içerse bile oluşturulan dosya ve taban temelin eşit olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="c59c1-214">The log indicates that the generated file and the baseline are equal, even though the executed format contains the binding to enter a constantly changing date and time value in the outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="c59c1-215">Giden dosya, biçimlerin bağlarını değiştirmeye zorlayan temel ayarlar kullanılarak oluşturulmuş olsa da değiştirme ile ilgili herhangi bir uyarı almazsınız.</span><span class="sxs-lookup"><span data-stu-id="c59c1-215">Although the outbound file has been generated by using baseline settings that force the replacement of the format's bindings, you don't receive any warnings about the replacement.</span></span>

## <a name="exchange-baseline-settings-between-environments"></a><span data-ttu-id="c59c1-216">Ortamlar arasında Döviz temeli ayarları</span><span class="sxs-lookup"><span data-stu-id="c59c1-216">Exchange baseline settings between environments</span></span>

### <a name="export-baseline-settings"></a><span data-ttu-id="c59c1-217">Dışa aktarma temeli ayarları</span><span class="sxs-lookup"><span data-stu-id="c59c1-217">Export baseline settings</span></span>

<span data-ttu-id="c59c1-218">Yeni ER özellikleri, geçerli Finance and Operations ortamından seçili ER biçimi için temel ayarlarını dışa aktarmanız ve bunları XML dosyaları olarak depolayabilmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="c59c1-218">The new ER capabilities let you export baseline settings for the selected ER format from the current Finance and Operations environment and store them as XML files.</span></span> 

<span data-ttu-id="c59c1-219">Temel ayarlarını dışa aktarmak için **Elektronik raporlama biçim temelleri** sayfasında **Dışa aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-219">To export baseline settings, on the **Electronic reporting format baselines** page, select **Export**.</span></span>

### <a name="import-baseline-settings"></a><span data-ttu-id="c59c1-220">Temel ayarları içe aktar</span><span class="sxs-lookup"><span data-stu-id="c59c1-220">Import baseline settings</span></span>

<span data-ttu-id="c59c1-221">Dışa aktarılan temel ayarları farklı Finance and Operations ortamına içe aktarılabilir.</span><span class="sxs-lookup"><span data-stu-id="c59c1-221">Exported baseline settings can be imported into a different Finance and Operations environment.</span></span> <span data-ttu-id="c59c1-222">Ortam önce bir ER biçimi olarak içe aktarılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c59c1-222">The environment must first be imported as an ER format.</span></span> <span data-ttu-id="c59c1-223">Bundan sonra temel ayarları içe aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c59c1-223">You can then import the baseline settings.</span></span>

<span data-ttu-id="c59c1-224">Yerel olarak depolanmış bir XML dosyasından ayarları dışa aktarmak için **Elekronik raporlama biçimi temelleri** sayfasında **Dışa aktarı**'ı seçin ve sonra XML dosyasını seçmek için **Gözat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-224">To import baseline settings from a locally stored XML file, on the **Electronic reporting format baselines** page, select **Import**, and then select **Browse** to select the XML file.</span></span>

<span data-ttu-id="c59c1-225">![Temel ayarları iletişim kutusunu içe aktar](media/GER-BaselineSample-ImportBaseline1.PNG "Temel ayarları iletişim kutusunu içe aktar ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="c59c1-225">![Import baseline settings dialog box](media/GER-BaselineSample-ImportBaseline1.PNG "Screenshot of the Import baseline settings dialog box")</span></span>

<span data-ttu-id="c59c1-226">Geçerli belge yönetimi ayarları ve seçili belge türü temel alınarak Microsoft SharePoint Sunucusunda depolanan bir XML dosyasından temel ayarları almak için **Elektronik raporlama biçim temelleri** sayfasında **Kaynaktan içe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-226">To import baseline settings from an XML file that is stored on the Microsoft SharePoint Server, based on the current Document management settings and the selected document type, on the **Electronic reporting format baselines** page, select **Import from source**.</span></span> <span data-ttu-id="c59c1-227">Sonra belge türünü ve XML dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="c59c1-227">Then select the document type and the XML file.</span></span> <span data-ttu-id="c59c1-228">SharePoint klasöre erişmek için gereken belge türü önceden yapılandırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c59c1-228">The required document type to access the SharePoint folder must be configured in advance.</span></span>

<span data-ttu-id="c59c1-229">![Kaynak iletişim kutusundan içe aktar](media/GER-BaselineSample-ImportBaseline2.PNG "Kaynak iletişim kutusundan içe aktar ekran görüntüsü")</span><span class="sxs-lookup"><span data-stu-id="c59c1-229">![Import from source dialog box](media/GER-BaselineSample-ImportBaseline2.PNG "Screenshot of the Import from source dialog box")</span></span>

> [!NOTE]
> <span data-ttu-id="c59c1-230">Görev kaydediciyi **Kaynağı içe aktar** iletişim kutusunda gereken belge türünü ve dosya adını seçmeye yönelik adımları kaydetmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c59c1-230">You can use Task recorder to record the steps for selecting the required document type and the file name in the **Import from source** dialog box.</span></span> <span data-ttu-id="c59c1-231">Bu şekilde, gerekli temel ayarları SharePoint sunucusunda tutabilir ve Regression Suite Automation Tool'u kullanarak otomatik testleri çalıştırdığınızda, bunları bir görev kaydı yürüterek otomatik olarak alabilirsiniz .</span><span class="sxs-lookup"><span data-stu-id="c59c1-231">In this way, you can keep required baseline settings on SharePoint Server and then automatically import them by playing a task recording when you run automated tests by using the Regression Suite Automation Tool.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c59c1-232">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="c59c1-232">Additional resources</span></span>

- [<span data-ttu-id="c59c1-233">Oluşturulan rapor sonuçlarını izleme ve temel değerlerle karşılaştırma</span><span class="sxs-lookup"><span data-stu-id="c59c1-233">Trace generated report results and compare them with baseline values</span></span>](er-trace-reports-compare-baseline.md)
- [<span data-ttu-id="c59c1-234">Görev kaydedici</span><span class="sxs-lookup"><span data-stu-id="c59c1-234">Task recorder</span></span>](../user-interface/task-recorder.md)
