--- 
title: "Word biçiminde raporlar oluşturmak için ER yapılandırmaları tasarlama"
description: "Aşağıdaki adımlar, bir Sistem yöneticisi veya Elektronik raporlama geliştirici rolündeki bir kullanıcının, Microsoft Word dosyaları şeklinde raporlar oluşturmak için bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar."
author: NickSelin
manager: AnnBe
ms.date: 12/21/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 615ab4a4f932478b8b847112d4fed8310187f03b
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---
# <a name="design-er-configurations-to-generate-reports-in-word-format"></a><span data-ttu-id="568fd-103">Word biçiminde raporlar oluşturmak için ER yapılandırmaları tasarlama</span><span class="sxs-lookup"><span data-stu-id="568fd-103">Design ER configurations to generate reports in Word format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="568fd-104">Aşağıdaki adımlar, bir Sistem yöneticisi veya Elektronik raporlama geliştirici rolündeki bir kullanıcının, Microsoft Word dosyaları şeklinde raporlar oluşturmak için bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="568fd-104">The following steps explain how a user in either the System administrator or Electronic reporting developer role can configure an Electronic reporting (ER) formats to generate reports as Microsoft Word files.</span></span> <span data-ttu-id="568fd-105">Bu adımlar GBSI şirketinde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="568fd-105">These steps can be performed in the GBSI company.</span></span>

<span data-ttu-id="568fd-106">Bu adımları tamamlamak için öncelikle "OPENXML biçiminde raporlar oluşturmak için bir ER yapılandırması oluşturma" görev kılavuzundaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="568fd-106">To complete these steps, you must first complete the steps in the “Create an ER configuration for generating reports in OPENXML format” task guide.</span></span> <span data-ttu-id="568fd-107">Aşağıdaki şablonları aynı rapor için önceden indirmeli ve yerel olarak kaydetmelisiniz:</span><span class="sxs-lookup"><span data-stu-id="568fd-107">In advance, you must also download and save the following templates locally for the sample report:</span></span>

[<span data-ttu-id="568fd-108">Ödeme Raporu şablonu</span><span class="sxs-lookup"><span data-stu-id="568fd-108">Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)

[<span data-ttu-id="568fd-109">Ödeme Raporunun Bağlı Şablonu</span><span class="sxs-lookup"><span data-stu-id="568fd-109">Bounded Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)

<span data-ttu-id="568fd-110">Bu yordam, Microsoft Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="568fd-110">This procedure is for a feature that was added in Microsoft Dynamics 365 for Operations version 1611.</span></span>


## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="568fd-111">Mevcut ER rapor yapılandırmasını seçme</span><span class="sxs-lookup"><span data-stu-id="568fd-111">Select the existing ER report configuration</span></span>
1. <span data-ttu-id="568fd-112">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="568fd-112">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="568fd-113">Yapılandırma sağlayıcısı olan "Litware, Inc." şirketinin etkin olarak seçildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="568fd-113">Make sure that the configuration provider ‘Litware, Inc.’</span></span> <span data-ttu-id="568fd-114">Etkin olarak işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="568fd-114">is selected as active.</span></span>  
2. <span data-ttu-id="568fd-115">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="568fd-115">Click Reporting configurations.</span></span>
    * <span data-ttu-id="568fd-116">Rapor çıktısını OPENXML biçiminde oluşturmak için özgün olarak tasarlanmış olan mevcut ER yapılandırmasını yeniden kullanacağız.</span><span class="sxs-lookup"><span data-stu-id="568fd-116">We will re-use the existing ER configuration that has been originally designed to generate the report output in OPENXML format.</span></span>  
3. <span data-ttu-id="568fd-117">Ağaçta, 'Ödeme modeli' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="568fd-117">In the tree, expand 'Payment model'.</span></span>
4. <span data-ttu-id="568fd-118">Ağaçta, 'Ödeme modeli\Örnek çalışma sayfası raporu' seçin.</span><span class="sxs-lookup"><span data-stu-id="568fd-118">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
5. <span data-ttu-id="568fd-119">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="568fd-119">Click Designer.</span></span>

## <a name="replace-the-excel-template-with-the-word-template"></a><span data-ttu-id="568fd-120">Excel şablonunu Word şablonu ile değiştirme</span><span class="sxs-lookup"><span data-stu-id="568fd-120">Replace the Excel template with the Word template</span></span>
    * <span data-ttu-id="568fd-121">Şu anda, Excel belgesi OPENXML biçiminde çıktı üretmek için şablon olarak kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="568fd-121">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="568fd-122">Raporun şablonunu Word biçiminde içeri aktaracağız.</span><span class="sxs-lookup"><span data-stu-id="568fd-122">We will import the report’s template in Word format.</span></span>  
1. <span data-ttu-id="568fd-123">Ekler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="568fd-123">Click Attachments.</span></span>
    * <span data-ttu-id="568fd-124">Mevcut Excel şablonunu daha önce indirdiğiniz Word şablonuyla (Ödeme Raporu Şablonu) değiştirin.</span><span class="sxs-lookup"><span data-stu-id="568fd-124">Replace the existing Excel template with the Word template that you downloaded earlier, Template of Payment Report.</span></span> <span data-ttu-id="568fd-125">Bu şablonun yalnızca ER çıktısı olarak oluşturmak istediğimiz belgenin düzenini içerdiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="568fd-125">Note, this template only contains the layout of the document we want to generate as ER output.</span></span>  
2. <span data-ttu-id="568fd-126">Sil'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="568fd-126">Click Delete.</span></span>
3. <span data-ttu-id="568fd-127">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="568fd-127">Click Yes.</span></span>
4. <span data-ttu-id="568fd-128">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="568fd-128">Click New.</span></span>
5. <span data-ttu-id="568fd-129">Dosya'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="568fd-129">Click File.</span></span>
6. <span data-ttu-id="568fd-130">Gözat düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="568fd-130">Click Browse.</span></span> <span data-ttu-id="568fd-131">Daha önceden indirdiğiniz SampleVendPaymDocReport.docx dosyasına gidin ve dosyayı seçin.</span><span class="sxs-lookup"><span data-stu-id="568fd-131">Navigate to and select SampleVendPaymDocReport.docx that you previously downloaded.</span></span> <span data-ttu-id="568fd-132">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="568fd-132">Click OK.</span></span>
    * <span data-ttu-id="568fd-133">Önceki adımda indirdiğiniz şablonu seçin.</span><span class="sxs-lookup"><span data-stu-id="568fd-133">Select the template that you downloaded in the previous step.</span></span>  
7. <span data-ttu-id="568fd-134">Şablon alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="568fd-134">In the Template field, enter or select a value.</span></span>

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a><span data-ttu-id="568fd-135">Özel bir XML bölümü ekleyerek Word şablonunu genişletme</span><span class="sxs-lookup"><span data-stu-id="568fd-135">Extend the Word template by adding a custom XML part</span></span>
1. <span data-ttu-id="568fd-136">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="568fd-136">Click Save.</span></span>
    * <span data-ttu-id="568fd-137">Kaydet eylemi, yapılandırma değişikliklerini depolamanın yanı sıra ekli Word şablonunu da güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="568fd-137">In addition to storing configuration changes, the Save action also updates the attached Word template.</span></span> <span data-ttu-id="568fd-138">Tasarlanan biçimin yapısı, ekli Word belgesine "Rapor" adında yeni bir özel XML bölümü olarak verilir.</span><span class="sxs-lookup"><span data-stu-id="568fd-138">The structure of the designed format is ported to the attached Word document as a new custom XML part with the name ‘Report’.</span></span> <span data-ttu-id="568fd-139">Ekli Word şablonunun yalnızca ER çıktısı olarak oluşturmak istediğimiz belgenin düzeninin yanı sıra ER'nin çalışma zamanında bu şablonu dolduracağı verilerin yapısını da içerdiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="568fd-139">Note that the attached Word template contains not only the layout of the document we want to generate as ER output, it also contains the structure of data that ER will populate into this template at runtime.</span></span>  
2. <span data-ttu-id="568fd-140">Ekler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="568fd-140">Click Attachments.</span></span>
    * <span data-ttu-id="568fd-141">Şimdi de "Rapor" adlı özel XML bölümünün öğelerini Word belgesi bölümlerine bağlamanız gerekiyor.</span><span class="sxs-lookup"><span data-stu-id="568fd-141">Now you need to bind the elements of the custom XML part ‘Report’ to the Word document parts.</span></span>  
    * <span data-ttu-id="568fd-142">Özel XML bölümlerinin öğeleriyle bağlı içerik denetimleri içeren formlar olarak tasarlanabilen Word belgeleri kullanıyorsanız bir sonraki alt görevin tüm adımlarını yürüterek bu tür bir belge oluşturun.</span><span class="sxs-lookup"><span data-stu-id="568fd-142">If you're familiar with Word documents that can be designed as forms containing content controls that are bounded with elements of custom XML parts – play all steps of the next sub-task to create such a document.</span></span> <span data-ttu-id="568fd-143">Daha ayrıntılı bilgi için bu bağlantıya bakın: https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US.</span><span class="sxs-lookup"><span data-stu-id="568fd-143">For more details, see this link https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US.</span></span> <span data-ttu-id="568fd-144">Aksi durumda, bir sonraki alt görevdeki tüm adımları atlayın.</span><span class="sxs-lookup"><span data-stu-id="568fd-144">Otherwise, skip all the steps in the next sub-task.</span></span>  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a><span data-ttu-id="568fd-145">Veri ilişkilendirmeleri yapmak için özel XML bölümlü Word edinme</span><span class="sxs-lookup"><span data-stu-id="568fd-145">Get Word with custom XML part to do data bindings</span></span>
    * <span data-ttu-id="568fd-146">Bu belgeyi Word'de açın ve aşağıdakileri yapın:  - Word Geliştiricisi sekmesini açın (henüz etkin değilse şeridi özelleştirin).</span><span class="sxs-lookup"><span data-stu-id="568fd-146">Open this document in Word and do the following:  - Open the Word Developer tab (customize the ribbon if it is not enabled yet).</span></span>  <span data-ttu-id="568fd-147">- XML eşleme bölmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="568fd-147">- Select XML mapping pane.</span></span>  <span data-ttu-id="568fd-148">- Aramada "Rapor" özel XML bölümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="568fd-148">- Select the ‘Report’ custom XML part in the lookup.</span></span>  <span data-ttu-id="568fd-149">- Seçili özel XML bölümü öğelerinin ve Word belgesinin içerik denetimlerinin eşlemesini yapın.</span><span class="sxs-lookup"><span data-stu-id="568fd-149">- Do mapping of the elements of the selected custom XML part and content controls of the Word document.</span></span>  <span data-ttu-id="568fd-150">- Güncelleştirilmiş Word belgesini bir yerel sürücüye kaydedin.</span><span class="sxs-lookup"><span data-stu-id="568fd-150">- Save the updated Word document on a local drive.</span></span>  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a><span data-ttu-id="568fd-151">İçerik denetimlerine bağlanmış özel XML bölümlü Word şablonunu yükleme</span><span class="sxs-lookup"><span data-stu-id="568fd-151">Upload the Word template with custom XML part bounded to content controls</span></span>
1. <span data-ttu-id="568fd-152">Sil'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="568fd-152">Click Delete.</span></span>
2. <span data-ttu-id="568fd-153">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="568fd-153">Click Yes.</span></span>
    * <span data-ttu-id="568fd-154">Yeni bir şablon ekleyin.</span><span class="sxs-lookup"><span data-stu-id="568fd-154">Add a new template.</span></span> <span data-ttu-id="568fd-155">Bir önceki alt görevdeki adımları tamamladıysanız hazırladığınız ve yerel olarak kaydettiğiniz Word belgesini seçin.</span><span class="sxs-lookup"><span data-stu-id="568fd-155">If you competed the steps in the previous subtask, select the Word document that you prepared and saved locally.</span></span> <span data-ttu-id="568fd-156">Aksi durumda, daha önce indirdiğiniz MS Word şablonunu (SampleVendPaymDocReportBounded.docx) seçin.</span><span class="sxs-lookup"><span data-stu-id="568fd-156">Otherwise, select the SampleVendPaymDocReportBounded.docx MS Word template that you downloaded earlier.</span></span>  
3. <span data-ttu-id="568fd-157">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="568fd-157">Click New.</span></span>
4. <span data-ttu-id="568fd-158">Dosya'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="568fd-158">Click File.</span></span>
5. <span data-ttu-id="568fd-159">Gözat düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="568fd-159">Click Browse.</span></span> <span data-ttu-id="568fd-160">Daha önceden indirdiğiniz SampleVendPaymDocReportBounded.docx dosyasına gidin ve dosyayı seçin.</span><span class="sxs-lookup"><span data-stu-id="568fd-160">Navigate to and select SampleVendPaymDocReportBounded.docx that you previously downloaded.</span></span> <span data-ttu-id="568fd-161">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="568fd-161">Click OK.</span></span>
6. <span data-ttu-id="568fd-162">Şablon alanında, bir önceki adımda indirdiğiniz belgeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="568fd-162">In the Template field, select the document that you downloaded in the previous step.</span></span>
7. <span data-ttu-id="568fd-163">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="568fd-163">Click Save.</span></span>
8. <span data-ttu-id="568fd-164">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="568fd-164">Close the page.</span></span>

## <a name="execute-the-format-to-create-word-output"></a><span data-ttu-id="568fd-165">Word çıktısı oluşturmak için biçimi yürütme</span><span class="sxs-lookup"><span data-stu-id="568fd-165">Execute the format to create Word output</span></span>
1. <span data-ttu-id="568fd-166">Eylem Bölmesi'nde, Yapılandırmalar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="568fd-166">On the Action Pane, click Configurations.</span></span>
2. <span data-ttu-id="568fd-167">Kullanıcı parametreleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="568fd-167">Click User parameters.</span></span>
3. <span data-ttu-id="568fd-168">Çalıştırma ayarları alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="568fd-168">Select Yes in the Run settings field.</span></span>
4. <span data-ttu-id="568fd-169">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="568fd-169">Click OK.</span></span>
5. <span data-ttu-id="568fd-170">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="568fd-170">Click Edit.</span></span>
6. <span data-ttu-id="568fd-171">Taslak Çalıştır alanında Evet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="568fd-171">Select Yes in the Run Draft field.</span></span>
7. <span data-ttu-id="568fd-172">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="568fd-172">Click Save.</span></span>
8. <span data-ttu-id="568fd-173">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="568fd-173">Close the page.</span></span>
9. <span data-ttu-id="568fd-174">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="568fd-174">Close the page.</span></span>
10. <span data-ttu-id="568fd-175">Borç hesapları > Ödemeler > Ödeme günlüğü'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="568fd-175">Go to Accounts payable > Payments > Payment journal.</span></span>
11. <span data-ttu-id="568fd-176">Satırlar seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="568fd-176">Click Lines.</span></span>
12. <span data-ttu-id="568fd-177">Listede, tüm satırları işaretleyin veya tüm satırların işaretlerini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="568fd-177">In the list, mark or unmark all rows.</span></span>
13. <span data-ttu-id="568fd-178">Ödeme durumu'nu tıklatın.</span><span class="sxs-lookup"><span data-stu-id="568fd-178">Click Payment status.</span></span>
14. <span data-ttu-id="568fd-179">Hiçbiri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="568fd-179">Click None.</span></span>
15. <span data-ttu-id="568fd-180">Ödemeler oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="568fd-180">Click Generate payments.</span></span>
16. <span data-ttu-id="568fd-181">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="568fd-181">Click OK.</span></span>
17. <span data-ttu-id="568fd-182">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="568fd-182">Click OK.</span></span>
    * <span data-ttu-id="568fd-183">Oluşturulan çıktıyı analiz edin.</span><span class="sxs-lookup"><span data-stu-id="568fd-183">Analyze the generated output.</span></span> <span data-ttu-id="568fd-184">Oluşturulan çıktının Word biçiminde sunulduğuna ve işlenen ödemelerin ayrıntılarını içerdiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="568fd-184">Note that the created output is presented in Word format and contains the details of the processed payments.</span></span>  


