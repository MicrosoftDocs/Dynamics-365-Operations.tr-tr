--- 
title: "Elektronik raporlama (ER) için OpenXML biçiminde rapor oluşturmak üzere bir yapılandırma tasarlama"
description: "Aşağıdaki yordamda, Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolündeki bir kullanıcının OPENXML biçiminde elektronik ödeme belgeleri oluşturmak için bir şablon içeren, yeni bir Elektronik Raporlama (ER) yapılandırmasını nasıl oluşturabileceği açıklanmıştır."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
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
ms.openlocfilehash: 51208cbc5118e95fd402cca3cbc228ef1b87a47f
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="design-a-configuration-for-generating-reports-in-openxml-format-for-electronic-reporting-er"></a><span data-ttu-id="8af6b-103">Elektronik raporlama (ER) için OpenXML biçiminde rapor oluşturmak üzere bir yapılandırma tasarlama</span><span class="sxs-lookup"><span data-stu-id="8af6b-103">Design a configuration for generating reports in OpenXML format for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8af6b-104">Aşağıdaki yordamda, Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolündeki bir kullanıcının OPENXML biçiminde elektronik ödeme belgeleri oluşturmak için bir şablon içeren, yeni bir Elektronik Raporlama (ER) yapılandırmasını nasıl oluşturabileceği açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="8af6b-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="8af6b-105">Bu yapılandırma, satıcı ödemelerini işlemek için kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="8af6b-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="8af6b-106">Bu örnekte Litware, Inc. örnek şirketi için bir yapılandırma oluşturacaksınız. Bu adımlar, herhangi bir GBSI şirketinde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="8af6b-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="8af6b-107">Bu adımları tamamlamak için, öncelikle "Bir yapılandırma sağlayıcı oluşturun ve etkin olarak işaretleyin" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="8af6b-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="8af6b-108">Ayrıca, şablonu oluştururken, alınacak olan bir Excel dosyası olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8af6b-108">You must also have an Excel file which will be imported when creating the template.</span></span> <span data-ttu-id="8af6b-109">Bu dosyaya şu adresten erişilebilir: https://msdynamics.blob.core.windows.net/media/2016/04/SampleVendPaymWsReport.xlsx</span><span class="sxs-lookup"><span data-stu-id="8af6b-109">This file can be accessed from:  https://msdynamics.blob.core.windows.net/media/2016/04/SampleVendPaymWsReport.xlsx</span></span>


## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="8af6b-110">Ödemeler veri modeli konfigürasyonunu yükleme</span><span class="sxs-lookup"><span data-stu-id="8af6b-110">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="8af6b-111">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="8af6b-112">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="8af6b-113">Örnek şirket Litware, Inc. için yapılandırma sağlayıcısını seçin. Bu yapılandırma sağlayıcısını göremiyorsanız, önce "Yapılandırma sağlayıcı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="8af6b-113">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="8af6b-114">Etkin olarak ayarla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-114">Click Set active.</span></span>
4. <span data-ttu-id="8af6b-115">Depolar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-115">Click Repositories.</span></span>
    * <span data-ttu-id="8af6b-116">Varsa, Operations Kaynakları türü için bir depo seçin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-116">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="8af6b-117">Kullanılabiliyorsa, yeni bir havuz oluşturmak hakkındaki aşağıdaki adımları atlayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-117">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="8af6b-118">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-118">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="8af6b-119">Yapılandırma havuzu türü alanına "Operasyon kaynakları" yazın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-119">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="8af6b-120">Havuz oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-120">Click Create repository.</span></span>
8. <span data-ttu-id="8af6b-121">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-121">Click OK.</span></span>
9. <span data-ttu-id="8af6b-122">Aç'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-122">Click Open.</span></span>
10. <span data-ttu-id="8af6b-123">Ağaçta 'Ödeme modeli' seçin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-123">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="8af6b-124">İçe aktar'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-124">Click Import.</span></span>
    * <span data-ttu-id="8af6b-125">Bu veri modelini içeri alın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-125">Import this data model.</span></span> <span data-ttu-id="8af6b-126">Yeni bir biçim yapılandırılmasında veri kaynağı olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8af6b-126">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="8af6b-127">Bu yapılandırmayı zaten içe aktardıysanız, bu adımı atlayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-127">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="8af6b-128">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-128">Click Yes.</span></span>
13. <span data-ttu-id="8af6b-129">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-129">Close the page.</span></span>
14. <span data-ttu-id="8af6b-130">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-130">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="8af6b-131">Yeni bir biçim yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="8af6b-131">Create a new format configuration</span></span>
1. <span data-ttu-id="8af6b-132">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-132">Click Reporting configurations.</span></span>
2. <span data-ttu-id="8af6b-133">Ağaçta 'Ödeme modeli' seçin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-133">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="8af6b-134">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-134">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="8af6b-135">Yeni alanına, 'Biçim veri modeline PaymentModel dayalı' girin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-135">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="8af6b-136">Bir biçimi, PaymentModel veri modeline dayalı olarak oluşturun.</span><span class="sxs-lookup"><span data-stu-id="8af6b-136">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="8af6b-137">Ad alanında 'Örnek çalışma sayfası raporu' yazın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-137">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="8af6b-138">Örnek çalışma sayfası raporu</span><span class="sxs-lookup"><span data-stu-id="8af6b-138">Sample worksheet report</span></span>  
6. <span data-ttu-id="8af6b-139">Açıklama alanında, 'Satıcıların ödemeleri için örnek çalışma sayfası raporu' yazın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-139">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="8af6b-140">Satıcıların ödemeleri için örnek çalışma sayfası raporu.</span><span class="sxs-lookup"><span data-stu-id="8af6b-140">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="8af6b-141">Veri modeli tanımı alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-141">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="8af6b-142">'CustomerCreditTransferInitiation' tanımını seçin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-142">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="8af6b-143">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-143">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="8af6b-144">OPENXML çalışma sayfası biçiminde yeni bir belge tasarlama</span><span class="sxs-lookup"><span data-stu-id="8af6b-144">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="8af6b-145">Ağaçta, 'Ödeme modeli\Örnek çalışma sayfası raporu' seçin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-145">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="8af6b-146">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-146">Click Designer.</span></span>
3. <span data-ttu-id="8af6b-147">Eylem Bölmesinde, İçeri Al'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-147">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="8af6b-148">Microsoft Excel'den içe aktar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-148">Click Import from Excel.</span></span>
5. <span data-ttu-id="8af6b-149">Ekler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-149">Click Attachments.</span></span>
    * <span data-ttu-id="8af6b-150">Şablon olarak mevcut Excel belgesini iliştirin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-150">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="8af6b-151">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-151">Click New.</span></span>
7. <span data-ttu-id="8af6b-152">Dosya'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-152">Click File.</span></span>
    * <span data-ttu-id="8af6b-153">Mevcut Excel dosyasına yönlendirin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-153">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="8af6b-154">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-154">Close the page.</span></span>
9. <span data-ttu-id="8af6b-155">Şablon alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-155">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="8af6b-156">Şablon olarak kullanılmak üzere ekli Excel dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-156">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="8af6b-157">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-157">Click OK.</span></span>
    * <span data-ttu-id="8af6b-158">ER biçim bileşenlerinin, başvurulan MS Excel belgesinin (adlandırılmış aralıklar) yapısına dayalı bir tasarım biçiminde oluşturulduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-158">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="8af6b-159">Para birimi kodlarına göre toplamları hesaplamak için yeni bir veri kaynağı oluşturma</span><span class="sxs-lookup"><span data-stu-id="8af6b-159">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="8af6b-160">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-160">Click the Mapping tab.</span></span>
2. <span data-ttu-id="8af6b-161">İletişim kutusunu açmak için Kök ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-161">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="8af6b-162">Ağaçta 'İşleveler\Grupla'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-162">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="8af6b-163">Ad alanında 'PaymentByCurrency' yazın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-163">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="8af6b-164">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="8af6b-164">PaymentByCurrency</span></span>  
5. <span data-ttu-id="8af6b-165">Grubu buna göre düzenle'ye tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-165">Click Edit group by.</span></span>
6. <span data-ttu-id="8af6b-166">Ağaçta, 'model'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-166">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="8af6b-167">Ağaçta seçin 'model\Payments'.</span><span class="sxs-lookup"><span data-stu-id="8af6b-167">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="8af6b-168">Alanı buna ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-168">Click Add field to.</span></span>
9. <span data-ttu-id="8af6b-169">Neler gruplanacak'ı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-169">Click What to group.</span></span>
10. <span data-ttu-id="8af6b-170">Ağaçta genişletin 'model\Payments'.</span><span class="sxs-lookup"><span data-stu-id="8af6b-170">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="8af6b-171">Ağaçta seçin 'model\Payments\Currency'.</span><span class="sxs-lookup"><span data-stu-id="8af6b-171">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="8af6b-172">Alanı buna ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-172">Click Add field to.</span></span>
13. <span data-ttu-id="8af6b-173">Gruplandırılmış alanlar'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-173">Click Grouped fields.</span></span>
14. <span data-ttu-id="8af6b-174">Ağaçta seçin: 'model\Payments\Instructed Amount(InstructedAmount)'.</span><span class="sxs-lookup"><span data-stu-id="8af6b-174">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="8af6b-175">Alanı buna ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-175">Click Add field to.</span></span>
16. <span data-ttu-id="8af6b-176">Toplam alanları'nı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-176">Click Aggregation fields.</span></span>
17. <span data-ttu-id="8af6b-177">Yöntem alanında bir seçenek belirtin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-177">In the Method field, select an option.</span></span>
    * <span data-ttu-id="8af6b-178">SUM toplama işlevini seçin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-178">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="8af6b-179">Ad alanında 'TotalInstructuredAmount' yazın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-179">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="8af6b-180">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="8af6b-180">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="8af6b-181">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-181">Click Save.</span></span>
20. <span data-ttu-id="8af6b-182">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-182">Close the page.</span></span>
21. <span data-ttu-id="8af6b-183">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-183">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="8af6b-184">Biçim bileşenlerini veri kaynaklarına eşleme</span><span class="sxs-lookup"><span data-stu-id="8af6b-184">Map format components to data sources</span></span>
1. <span data-ttu-id="8af6b-185">Ağaçta, 'model'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-185">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="8af6b-186">Ağaçta genişletin 'model\Payments'.</span><span class="sxs-lookup"><span data-stu-id="8af6b-186">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="8af6b-187">Ağaçta, 'model\Payments\Initiating Party(InitiatingParty)' seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-187">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="8af6b-188">Ağaçta 'model\Payments\Initiating Party(InitiatingParty)\Name' seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-188">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="8af6b-189">Ağaçta, "Excel\ReportHeader" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-189">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="8af6b-190">Ağaçta, "Excel\ReportHeader\CompanyName" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-190">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="8af6b-191">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-191">Click Bind.</span></span>
8. <span data-ttu-id="8af6b-192">Ağaçta genişletin 'model\Payments\Creditor'.</span><span class="sxs-lookup"><span data-stu-id="8af6b-192">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="8af6b-193">Ağaçta genişletin 'model\Payments\Creditor\Identification'.</span><span class="sxs-lookup"><span data-stu-id="8af6b-193">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="8af6b-194">Ağaçta seçin: 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span><span class="sxs-lookup"><span data-stu-id="8af6b-194">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="8af6b-195">Ağaçta, "Excel\PaymLines" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-195">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="8af6b-196">Ağaçta, "Excel\PaymLines\VendAccountName" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-196">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="8af6b-197">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-197">Click Bind.</span></span>
14. <span data-ttu-id="8af6b-198">Ağaçta seçin 'model\Payments\Creditor\Name'.</span><span class="sxs-lookup"><span data-stu-id="8af6b-198">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="8af6b-199">Ağaçta, "Excel\PaymLines\VendName" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-199">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="8af6b-200">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-200">Click Bind.</span></span>
17. <span data-ttu-id="8af6b-201">Ağaçta genişletin: 'model\Payments\Creditor Agent(CreditorAgent)'.</span><span class="sxs-lookup"><span data-stu-id="8af6b-201">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="8af6b-202">Ağaçta seçin: 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span><span class="sxs-lookup"><span data-stu-id="8af6b-202">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="8af6b-203">Ağaçta, "Excel\PaymLines\Banka" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-203">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="8af6b-204">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-204">Click Bind.</span></span>
21. <span data-ttu-id="8af6b-205">Ağaçta seçin 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span><span class="sxs-lookup"><span data-stu-id="8af6b-205">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="8af6b-206">Ağaçta, "Excel\PaymLines\RoutingNumber" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-206">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="8af6b-207">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-207">Click Bind.</span></span>
24. <span data-ttu-id="8af6b-208">Ağaçta 'Model\Payments\Creditor Account(CreditorAccount)' genişletin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="8af6b-209">Ağaçta 'Model\Payments\Creditor Account(CreditorAccount)' genişletin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-209">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="8af6b-210">Ağaçta seçin 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span><span class="sxs-lookup"><span data-stu-id="8af6b-210">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="8af6b-211">Ağaçta, "Excel\PaymLines\AccountNumber" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-211">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="8af6b-212">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-212">Click Bind.</span></span>
29. <span data-ttu-id="8af6b-213">Ağaçta seçin: 'model\Payments\Instructed Amount(InstructedAmount)'.</span><span class="sxs-lookup"><span data-stu-id="8af6b-213">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="8af6b-214">Ağaçta, "Excel\PaymLines\Borç" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-214">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="8af6b-215">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-215">Click Bind.</span></span>
32. <span data-ttu-id="8af6b-216">Ağaçta genişletin 'model\Payments\Creditor'.</span><span class="sxs-lookup"><span data-stu-id="8af6b-216">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="8af6b-217">Ağaçta 'Model\Payments\Creditor Account(CreditorAccount)' genişletin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-217">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="8af6b-218">Ağaçta genişletin: 'model\Payments\Creditor Agent(CreditorAgent)'.</span><span class="sxs-lookup"><span data-stu-id="8af6b-218">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="8af6b-219">Ağaçta seçin 'model\Payments\Currency'.</span><span class="sxs-lookup"><span data-stu-id="8af6b-219">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="8af6b-220">Ağaçta, "Excel\PaymLines\Para Birimi" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-220">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="8af6b-221">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-221">Click Bind.</span></span>
38. <span data-ttu-id="8af6b-222">Ağaçta 'PaymentByCurrency' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-222">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="8af6b-223">Ağaçta genişletin: 'PaymentByCurrency\grouped'.</span><span class="sxs-lookup"><span data-stu-id="8af6b-223">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="8af6b-224">Ağaçta seçin 'PaymentByCurrency\grouped\Currency'.</span><span class="sxs-lookup"><span data-stu-id="8af6b-224">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="8af6b-225">Ağaçta, "Excel\SummaryLines" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-225">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="8af6b-226">Ağaçta, "Excel\SummaryLines\SummaryCurrency" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-226">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="8af6b-227">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-227">Click Bind.</span></span>
44. <span data-ttu-id="8af6b-228">Ağaçta genişletin 'PaymentByCurrency\aggregated'.</span><span class="sxs-lookup"><span data-stu-id="8af6b-228">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="8af6b-229">Ağaçta seçin 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span><span class="sxs-lookup"><span data-stu-id="8af6b-229">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="8af6b-230">Ağaçta, "Excel\SummaryLines\SummaryAmount" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-230">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="8af6b-231">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-231">Click Bind.</span></span>
48. <span data-ttu-id="8af6b-232">Ağaçta 'PaymentByCurrency' seçin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-232">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="8af6b-233">Ağaçta, "Excel\SummaryLines" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-233">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="8af6b-234">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-234">Click Bind.</span></span>
51. <span data-ttu-id="8af6b-235">Ağaçta seçin 'model\Payments'.</span><span class="sxs-lookup"><span data-stu-id="8af6b-235">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="8af6b-236">Ağaçta, "Excel\PaymLines" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-236">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="8af6b-237">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-237">Click Bind.</span></span>
54. <span data-ttu-id="8af6b-238">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-238">Click Save.</span></span>
55. <span data-ttu-id="8af6b-239">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-239">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="8af6b-240">Ödemeleri işlemek için oluşturulan yapılandırmayı kullanın</span><span class="sxs-lookup"><span data-stu-id="8af6b-240">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="8af6b-241">Durumu değiştir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-241">Click Change status.</span></span>
2. <span data-ttu-id="8af6b-242">Tamamla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-242">Click Complete.</span></span>
3. <span data-ttu-id="8af6b-243">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-243">Click OK.</span></span>
4. <span data-ttu-id="8af6b-244">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-244">Close the page.</span></span>
5. <span data-ttu-id="8af6b-245">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-245">Close the page.</span></span>
6. <span data-ttu-id="8af6b-246">Borç hesapları > Ödeme kurulumu > Ödeme yöntemleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-246">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="8af6b-247">Ödeme yöntemi alanına "Elektronik" değeriyle filtre uygulamak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-247">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="8af6b-248">Elektronik</span><span class="sxs-lookup"><span data-stu-id="8af6b-248">Electronic</span></span>  
8. <span data-ttu-id="8af6b-249">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-249">Click Edit.</span></span>
9. <span data-ttu-id="8af6b-250">Dosya biçimleri bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-250">Expand the File formats section.</span></span>
10. <span data-ttu-id="8af6b-251">Genel elektronik raporlama alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-251">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="8af6b-252">Biçim yapılandırmasını dışa aktar alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-252">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="8af6b-253">'Örnek çalışma sayfası raporu yapılandırması'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-253">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="8af6b-254">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-254">Click Save.</span></span>
13. <span data-ttu-id="8af6b-255">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-255">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="8af6b-256">Oluşturulan yapılandırmayı ödeme günlüklerini işleme için kullanma</span><span class="sxs-lookup"><span data-stu-id="8af6b-256">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="8af6b-257">Borç hesapları > Ödemeler > Ödeme günlüğü'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-257">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="8af6b-258">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-258">Click New.</span></span>
    * <span data-ttu-id="8af6b-259">Yeni bir ödeme günlüğü oluşturun.</span><span class="sxs-lookup"><span data-stu-id="8af6b-259">Create a new payment journal.</span></span>  
3. <span data-ttu-id="8af6b-260">İsim alanına VendPay' yazın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-260">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="8af6b-261">VendPay</span><span class="sxs-lookup"><span data-stu-id="8af6b-261">VendPay</span></span>  
4. <span data-ttu-id="8af6b-262">Satırlar seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-262">Click Lines.</span></span>
5. <span data-ttu-id="8af6b-263">Hesap alanında, 'GB_SI_000001' değerlerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-263">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="8af6b-264">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="8af6b-264">GB_SI_000001</span></span>  
6. <span data-ttu-id="8af6b-265">Borcu '1000' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-265">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="8af6b-266">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-266">Click New.</span></span>
8. <span data-ttu-id="8af6b-267">Hesap alanında, 'GB_SI_000005' değerlerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-267">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="8af6b-268">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="8af6b-268">GB_SI_000005</span></span>  
9. <span data-ttu-id="8af6b-269">Borcu '2000' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-269">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="8af6b-270">Para birimi alanına 'EUR' yazın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-270">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="8af6b-271">Euro</span><span class="sxs-lookup"><span data-stu-id="8af6b-271">EUR</span></span>  
11. <span data-ttu-id="8af6b-272">Mahsup hesabı alanında, 'GBSI OPER' değerlerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-272">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="8af6b-273">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="8af6b-273">GBSI OPER</span></span>  
12. <span data-ttu-id="8af6b-274">Ödeme yöntemi alanına 'Elektronik' girin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-274">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="8af6b-275">Elektronik</span><span class="sxs-lookup"><span data-stu-id="8af6b-275">Electronic</span></span>  
13. <span data-ttu-id="8af6b-276">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-276">Click Save.</span></span>
14. <span data-ttu-id="8af6b-277">Ödemeler oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-277">Click Generate payments.</span></span>
15. <span data-ttu-id="8af6b-278">Ödeme yöntemi alanına 'Elektronik' girin.</span><span class="sxs-lookup"><span data-stu-id="8af6b-278">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="8af6b-279">Elektronik</span><span class="sxs-lookup"><span data-stu-id="8af6b-279">Electronic</span></span>  
16. <span data-ttu-id="8af6b-280">Ad alanına, "Ödemeler" yazın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-280">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="8af6b-281">Örneğin 'Ödemeler' yazın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-281">For example, type Payments.</span></span>  
17. <span data-ttu-id="8af6b-282">Banka hesabı alanında 'GBSI OPER' yazın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-282">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="8af6b-283">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="8af6b-283">GBSI OPER</span></span>  
18. <span data-ttu-id="8af6b-284">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-284">Click OK.</span></span>
19. <span data-ttu-id="8af6b-285">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8af6b-285">Click OK.</span></span>
    * <span data-ttu-id="8af6b-286">Oluşturulan çalışma sayfasını gözden geçirin; ödeme ayrıntı satırları ve bu ödeme iletisinde kullanılacak her bir para birimi kodu için toplamlar da dahil olmak üzere.</span><span class="sxs-lookup"><span data-stu-id="8af6b-286">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  


