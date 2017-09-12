--- 
title: "Elektronik raporlama (ER) için Microsoft Word biçiminde rapor oluşturmak üzere bir yapılandırma tasarlama"
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 950133ad73fd609938a64c3df16c34439ab860c1
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="design-a-configuration-for-generating-reports-in-microsoft-word-format-for-electronic-reporting-er"></a><span data-ttu-id="86377-103">Elektronik raporlama (ER) için Microsoft Word biçiminde rapor oluşturmak üzere bir yapılandırma tasarlama</span><span class="sxs-lookup"><span data-stu-id="86377-103">Design a configuration for generating reports in Microsoft Word format for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="86377-104">Aşağıdaki adımlar, bir Sistem yöneticisi veya Elektronik raporlama geliştirici rolündeki bir kullanıcının, Microsoft Word dosyaları şeklinde raporlar oluşturmak için bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="86377-104">The following steps explain how a user in either the System administrator or Electronic reporting developer role can configure an Electronic reporting (ER) formats to generate reports as Microsoft Word files.</span></span> <span data-ttu-id="86377-105">Bu adımlar GBSI şirketinde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="86377-105">These steps can be performed in the GBSI company.</span></span>

<span data-ttu-id="86377-106">Bu adımları tamamlamak için öncelikle "OPENXML biçiminde raporlar oluşturmak için bir ER yapılandırması oluşturma" görev kılavuzundaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="86377-106">To complete these steps, you must first complete the steps in the “Create an ER configuration for generating reports in OPENXML format” task guide.</span></span> <span data-ttu-id="86377-107">Aşağıdaki şablonları aynı rapor için önceden indirmeli ve yerel olarak kaydetmelisiniz:</span><span class="sxs-lookup"><span data-stu-id="86377-107">In advance, you must also download and save the following templates locally for the sample report:</span></span>

<span data-ttu-id="86377-108">http://msdynamics.blob.core.windows.net/media/2016/10/SampleVendPaymDocReport.docx</span><span class="sxs-lookup"><span data-stu-id="86377-108">http://msdynamics.blob.core.windows.net/media/2016/10/SampleVendPaymDocReport.docx</span></span>

<span data-ttu-id="86377-109">http://msdynamics.blob.core.windows.net/media/2016/10/SampleVendPaymDocReportBounded.docx</span><span class="sxs-lookup"><span data-stu-id="86377-109">http://msdynamics.blob.core.windows.net/media/2016/10/SampleVendPaymDocReportBounded.docx</span></span>

<span data-ttu-id="86377-110">Bu yordam, Microsoft Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="86377-110">This procedure is for a feature that was added in Microsoft Dynamics 365 for Operations version 1611.</span></span>


## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="86377-111">Mevcut ER rapor yapılandırmasını seçme</span><span class="sxs-lookup"><span data-stu-id="86377-111">Select the existing ER report configuration</span></span>
1. <span data-ttu-id="86377-112">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="86377-112">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="86377-113">Yapılandırma sağlayıcısı olan "Litware, Inc." şirketinin etkin olarak seçildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="86377-113">Make sure that the configuration provider ‘Litware, Inc.’</span></span> <span data-ttu-id="86377-114">Etkin olarak işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="86377-114">is selected as active.</span></span>  
2. <span data-ttu-id="86377-115">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86377-115">Click Reporting configurations.</span></span>
    * <span data-ttu-id="86377-116">Rapor çıktısını OPENXML biçiminde oluşturmak için özgün olarak tasarlanmış olan mevcut ER yapılandırmasını yeniden kullanacağız.</span><span class="sxs-lookup"><span data-stu-id="86377-116">We will re-use the existing ER configuration that has been originally designed to generate the report output in OPENXML format.</span></span>  
3. <span data-ttu-id="86377-117">Ağaçta, 'Ödeme modeli' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="86377-117">In the tree, expand 'Payment model'.</span></span>
4. <span data-ttu-id="86377-118">Ağaçta, 'Ödeme modeli\Örnek çalışma sayfası raporu' seçin.</span><span class="sxs-lookup"><span data-stu-id="86377-118">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
5. <span data-ttu-id="86377-119">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="86377-119">Click Designer.</span></span>

## <a name="replace-the-excel-template-with-the-word-template"></a><span data-ttu-id="86377-120">Excel şablonunu Word şablonu ile değiştirme</span><span class="sxs-lookup"><span data-stu-id="86377-120">Replace the Excel template with the Word template</span></span>
    * <span data-ttu-id="86377-121">Şu anda, Excel belgesi OPENXML biçiminde çıktı üretmek için şablon olarak kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="86377-121">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="86377-122">Raporun şablonunu Word biçiminde içeri aktaracağız.</span><span class="sxs-lookup"><span data-stu-id="86377-122">We will import the report’s template in Word format.</span></span>  
1. <span data-ttu-id="86377-123">Ekler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86377-123">Click Attachments.</span></span>
    * <span data-ttu-id="86377-124">Mevcut Excel şablonunu daha önce indirdiğiniz Word şablonuyla (SampleVendPaymDocReport.docx) değiştirin.</span><span class="sxs-lookup"><span data-stu-id="86377-124">Replace the existing Excel template with the Word template that you downloaded earlier, SampleVendPaymDocReport.docx.</span></span> <span data-ttu-id="86377-125">Bu şablonun yalnızca ER çıktısı olarak oluşturmak istediğimiz belgenin düzenini içerdiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="86377-125">Note, this template only contains the layout of the document we want to generate as ER output.</span></span>  
2. <span data-ttu-id="86377-126">Sil'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="86377-126">Click Delete.</span></span>
3. <span data-ttu-id="86377-127">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="86377-127">Click Yes.</span></span>
4. <span data-ttu-id="86377-128">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86377-128">Click New.</span></span>
5. <span data-ttu-id="86377-129">Dosya'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86377-129">Click File.</span></span>
6. <span data-ttu-id="86377-130">Gözat düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86377-130">Click Browse.</span></span> <span data-ttu-id="86377-131">Daha önceden indirdiğiniz SampleVendPaymDocReport.docx dosyasına gidin ve dosyayı seçin.</span><span class="sxs-lookup"><span data-stu-id="86377-131">Navigate to and select SampleVendPaymDocReport.docx that you previously downloaded.</span></span> <span data-ttu-id="86377-132">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86377-132">Click OK.</span></span>
    * <span data-ttu-id="86377-133">Önceki adımda indirdiğiniz şablonu seçin.</span><span class="sxs-lookup"><span data-stu-id="86377-133">Select the template that you downloaded in the previous step.</span></span>  
7. <span data-ttu-id="86377-134">Şablon alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="86377-134">In the Template field, enter or select a value.</span></span>

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a><span data-ttu-id="86377-135">Özel bir XML bölümü ekleyerek Word şablonunu genişletme</span><span class="sxs-lookup"><span data-stu-id="86377-135">Extend the Word template by adding a custom XML part</span></span>
1. <span data-ttu-id="86377-136">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86377-136">Click Save.</span></span>
    * <span data-ttu-id="86377-137">Kaydet eylemi, yapılandırma değişikliklerini depolamanın yanı sıra ekli Word şablonunu da güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="86377-137">In addition to storing configuration changes, the Save action also updates the attached Word template.</span></span> <span data-ttu-id="86377-138">Tasarlanan biçimin yapısı, ekli Word belgesine "Rapor" adında yeni bir özel XML bölümü olarak verilir.</span><span class="sxs-lookup"><span data-stu-id="86377-138">The structure of the designed format is ported to the attached Word document as a new custom XML part with the name ‘Report’.</span></span> <span data-ttu-id="86377-139">Ekli Word şablonunun yalnızca ER çıktısı olarak oluşturmak istediğimiz belgenin düzeninin yanı sıra ER'nin çalışma zamanında bu şablonu dolduracağı verilerin yapısını da içerdiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="86377-139">Note that the attached Word template contains not only the layout of the document we want to generate as ER output, it also contains the structure of data that ER will populate into this template at runtime.</span></span>  
2. <span data-ttu-id="86377-140">Ekler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86377-140">Click Attachments.</span></span>
    * <span data-ttu-id="86377-141">Şimdi de "Rapor" adlı özel XML bölümünün öğelerini Word belgesi bölümlerine bağlamanız gerekiyor.</span><span class="sxs-lookup"><span data-stu-id="86377-141">Now you need to bind the elements of the custom XML part ‘Report’ to the Word document parts.</span></span>  
    * <span data-ttu-id="86377-142">Özel XML bölümlerinin öğeleriyle bağlı içerik denetimleri içeren formlar olarak tasarlanabilen Word belgeleri kullanıyorsanız bir sonraki alt görevin tüm adımlarını yürüterek bu tür bir belge oluşturun.</span><span class="sxs-lookup"><span data-stu-id="86377-142">If you're familiar with Word documents that can be designed as forms containing content controls that are bounded with elements of custom XML parts – play all steps of the next sub-task to create such a document.</span></span> <span data-ttu-id="86377-143">Daha fazla bilgi için şu bağlantıya bakın: https://support.office.com/tr-tr/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=tr-TR&rs=tr-TR&ad=TR.</span><span class="sxs-lookup"><span data-stu-id="86377-143">For more details, see this link https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US.</span></span> <span data-ttu-id="86377-144">Aksi durumda, bir sonraki alt görevdeki tüm adımları atlayın.</span><span class="sxs-lookup"><span data-stu-id="86377-144">Otherwise, skip all the steps in the next sub-task.</span></span>  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a><span data-ttu-id="86377-145">Veri ilişkilendirmeleri yapmak için özel XML bölümlü Word edinme</span><span class="sxs-lookup"><span data-stu-id="86377-145">Get Word with custom XML part to do data bindings</span></span>
    * <span data-ttu-id="86377-146">Bu belgeyi Word'de açın ve aşağıdakileri yapın:  - Word Geliştiricisi sekmesini açın (henüz etkin değilse şeridi özelleştirin).</span><span class="sxs-lookup"><span data-stu-id="86377-146">Open this document in Word and do the following:  - Open the Word Developer tab (customize the ribbon if it is not enabled yet).</span></span>  <span data-ttu-id="86377-147">- XML eşleme bölmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="86377-147">- Select XML mapping pane.</span></span>  <span data-ttu-id="86377-148">- Aramada "Rapor" özel XML bölümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="86377-148">- Select the ‘Report’ custom XML part in the lookup.</span></span>  <span data-ttu-id="86377-149">- Seçili özel XML bölümü öğelerinin ve Word belgesinin içerik denetimlerinin eşlemesini yapın.</span><span class="sxs-lookup"><span data-stu-id="86377-149">- Do mapping of the elements of the selected custom XML part and content controls of the Word document.</span></span>  <span data-ttu-id="86377-150">- Güncelleştirilmiş Word belgesini bir yerel sürücüye kaydedin.</span><span class="sxs-lookup"><span data-stu-id="86377-150">- Save the updated Word document on a local drive.</span></span>  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a><span data-ttu-id="86377-151">İçerik denetimlerine bağlanmış özel XML bölümlü Word şablonunu yükleme</span><span class="sxs-lookup"><span data-stu-id="86377-151">Upload the Word template with custom XML part bounded to content controls</span></span>
1. <span data-ttu-id="86377-152">Sil'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="86377-152">Click Delete.</span></span>
2. <span data-ttu-id="86377-153">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="86377-153">Click Yes.</span></span>
    * <span data-ttu-id="86377-154">Yeni bir şablon ekleyin.</span><span class="sxs-lookup"><span data-stu-id="86377-154">Add a new template.</span></span> <span data-ttu-id="86377-155">Bir önceki alt görevdeki adımları tamamladıysanız hazırladığınız ve yerel olarak kaydettiğiniz Word belgesini seçin.</span><span class="sxs-lookup"><span data-stu-id="86377-155">If you competed the steps in the previous subtask, select the Word document that you prepared and saved locally.</span></span> <span data-ttu-id="86377-156">Aksi durumda, daha önce indirdiğiniz MS Word şablonunu (SampleVendPaymDocReportBounded.docx) seçin.</span><span class="sxs-lookup"><span data-stu-id="86377-156">Otherwise, select the SampleVendPaymDocReportBounded.docx MS Word template that you downloaded earlier.</span></span>  
3. <span data-ttu-id="86377-157">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86377-157">Click New.</span></span>
4. <span data-ttu-id="86377-158">Dosya'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86377-158">Click File.</span></span>
5. <span data-ttu-id="86377-159">Gözat düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86377-159">Click Browse.</span></span> <span data-ttu-id="86377-160">Daha önceden indirdiğiniz SampleVendPaymDocReportBounded.docx dosyasına gidin ve dosyayı seçin.</span><span class="sxs-lookup"><span data-stu-id="86377-160">Navigate to and select SampleVendPaymDocReportBounded.docx that you previously downloaded.</span></span> <span data-ttu-id="86377-161">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="86377-161">Click OK.</span></span>
6. <span data-ttu-id="86377-162">Şablon alanında, bir önceki adımda indirdiğiniz belgeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="86377-162">In the Template field, select the document that you downloaded in the previous step.</span></span>
7. <span data-ttu-id="86377-163">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86377-163">Click Save.</span></span>
8. <span data-ttu-id="86377-164">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="86377-164">Close the page.</span></span>

## <a name="execute-the-format-to-create-word-output"></a><span data-ttu-id="86377-165">Word çıktısı oluşturmak için biçimi yürütme</span><span class="sxs-lookup"><span data-stu-id="86377-165">Execute the format to create Word output</span></span>
1. <span data-ttu-id="86377-166">Eylem Bölmesi'nde, Yapılandırmalar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86377-166">On the Action Pane, click Configurations.</span></span>
2. <span data-ttu-id="86377-167">Kullanıcı parametreleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86377-167">Click User parameters.</span></span>
3. <span data-ttu-id="86377-168">Çalıştırma ayarları alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="86377-168">Select Yes in the Run settings field.</span></span>
4. <span data-ttu-id="86377-169">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86377-169">Click OK.</span></span>
5. <span data-ttu-id="86377-170">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86377-170">Click Edit.</span></span>
6. <span data-ttu-id="86377-171">Taslak Çalıştır alanında Evet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86377-171">Select Yes in the Run Draft field.</span></span>
7. <span data-ttu-id="86377-172">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86377-172">Click Save.</span></span>
8. <span data-ttu-id="86377-173">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="86377-173">Close the page.</span></span>
9. <span data-ttu-id="86377-174">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="86377-174">Close the page.</span></span>
10. <span data-ttu-id="86377-175">Borç hesapları > Ödemeler > Ödeme günlüğü'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="86377-175">Go to Accounts payable > Payments > Payment journal.</span></span>
11. <span data-ttu-id="86377-176">Satırlar seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86377-176">Click Lines.</span></span>
12. <span data-ttu-id="86377-177">Listede, tüm satırları işaretleyin veya tüm satırların işaretlerini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="86377-177">In the list, mark or unmark all rows.</span></span>
13. <span data-ttu-id="86377-178">Ödeme durumu'nu tıklatın.</span><span class="sxs-lookup"><span data-stu-id="86377-178">Click Payment status.</span></span>
14. <span data-ttu-id="86377-179">Hiçbiri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86377-179">Click None.</span></span>
15. <span data-ttu-id="86377-180">Ödemeler oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="86377-180">Click Generate payments.</span></span>
16. <span data-ttu-id="86377-181">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86377-181">Click OK.</span></span>
17. <span data-ttu-id="86377-182">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86377-182">Click OK.</span></span>
    * <span data-ttu-id="86377-183">Oluşturulan çıktıyı analiz edin.</span><span class="sxs-lookup"><span data-stu-id="86377-183">Analyze the generated output.</span></span> <span data-ttu-id="86377-184">Oluşturulan çıktının Word biçiminde sunulduğuna ve işlenen ödemelerin ayrıntılarını içerdiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="86377-184">Note that the created output is presented in Word format and contains the details of the processed payments.</span></span>  


