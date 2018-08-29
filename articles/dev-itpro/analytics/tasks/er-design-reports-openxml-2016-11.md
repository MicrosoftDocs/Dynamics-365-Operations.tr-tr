--- 
title: "Raporları OpenXML biçiminde oluşturmak için ER yapılandırmaları tasarlama"
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: b42cfe36c57a9526e585bbad0fcd31ff60b90397
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---
# <a name="design-er-configurations-to-generate-reports-in-openxml-format"></a><span data-ttu-id="48275-103">Raporları OpenXML biçiminde oluşturmak için ER yapılandırmaları tasarlama</span><span class="sxs-lookup"><span data-stu-id="48275-103">Design ER configurations to generate reports in OpenXML format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="48275-104">Aşağıdaki yordamda, Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolündeki bir kullanıcının OPENXML biçiminde elektronik ödeme belgeleri oluşturmak için bir şablon içeren, yeni bir Elektronik Raporlama (ER) yapılandırmasını nasıl oluşturabileceği açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="48275-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="48275-105">Bu yapılandırma, satıcı ödemelerini işlemek için kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="48275-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="48275-106">Bu örnekte Litware, Inc. örnek şirketi için bir yapılandırma oluşturacaksınız. Bu adımlar, herhangi bir GBSI şirketinde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="48275-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="48275-107">Bu adımları tamamlamak için, öncelikle "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="48275-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="48275-108">Ayrıca Microsoft Excel dosyasını [Ödeme Raporu Şablonu](https://go.microsoft.com/fwlink/?linkid=862266) indirmeniz ve kaydetmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="48275-108">You must also download and save the Microsoft Excel file, [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span> 

## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="48275-109">Ödemeler veri modeli konfigürasyonunu yükleme</span><span class="sxs-lookup"><span data-stu-id="48275-109">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="48275-110">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="48275-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="48275-111">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="48275-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="48275-112">Örnek şirket Litware, Inc. için yapılandırma sağlayıcısını seçin. Bu yapılandırma sağlayıcısını göremiyorsanız, önce "Yapılandırma sağlayıcı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="48275-112">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="48275-113">Etkin olarak ayarla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-113">Click Set active.</span></span>
4. <span data-ttu-id="48275-114">Depolar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-114">Click Repositories.</span></span>
    * <span data-ttu-id="48275-115">Varsa, Operations Kaynakları türü için bir depo seçin.</span><span class="sxs-lookup"><span data-stu-id="48275-115">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="48275-116">Kullanılabiliyorsa, yeni bir havuz oluşturmak hakkındaki aşağıdaki adımları atlayın.</span><span class="sxs-lookup"><span data-stu-id="48275-116">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="48275-117">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="48275-117">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="48275-118">Yapılandırma havuzu türü alanına "Operasyon kaynakları" yazın.</span><span class="sxs-lookup"><span data-stu-id="48275-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="48275-119">Havuz oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-119">Click Create repository.</span></span>
8. <span data-ttu-id="48275-120">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-120">Click OK.</span></span>
9. <span data-ttu-id="48275-121">Aç'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-121">Click Open.</span></span>
10. <span data-ttu-id="48275-122">Ağaçta 'Ödeme modeli' seçin.</span><span class="sxs-lookup"><span data-stu-id="48275-122">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="48275-123">İçe aktar'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="48275-123">Click Import.</span></span>
    * <span data-ttu-id="48275-124">Bu veri modelini içeri alın.</span><span class="sxs-lookup"><span data-stu-id="48275-124">Import this data model.</span></span> <span data-ttu-id="48275-125">Yeni bir biçim yapılandırılmasında veri kaynağı olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="48275-125">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="48275-126">Bu yapılandırmayı zaten içe aktardıysanız, bu adımı atlayın.</span><span class="sxs-lookup"><span data-stu-id="48275-126">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="48275-127">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="48275-127">Click Yes.</span></span>
13. <span data-ttu-id="48275-128">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="48275-128">Close the page.</span></span>
14. <span data-ttu-id="48275-129">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="48275-129">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="48275-130">Yeni bir biçim yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="48275-130">Create a new format configuration</span></span>
1. <span data-ttu-id="48275-131">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-131">Click Reporting configurations.</span></span>
2. <span data-ttu-id="48275-132">Ağaçta 'Ödeme modeli' seçin.</span><span class="sxs-lookup"><span data-stu-id="48275-132">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="48275-133">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-133">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="48275-134">Yeni alanına, 'Biçim veri modeline PaymentModel dayalı' girin.</span><span class="sxs-lookup"><span data-stu-id="48275-134">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="48275-135">Bir biçimi, PaymentModel veri modeline dayalı olarak oluşturun.</span><span class="sxs-lookup"><span data-stu-id="48275-135">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="48275-136">Ad alanında 'Örnek çalışma sayfası raporu' yazın.</span><span class="sxs-lookup"><span data-stu-id="48275-136">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="48275-137">Örnek çalışma sayfası raporu</span><span class="sxs-lookup"><span data-stu-id="48275-137">Sample worksheet report</span></span>  
6. <span data-ttu-id="48275-138">Açıklama alanında, 'Satıcıların ödemeleri için örnek çalışma sayfası raporu' yazın.</span><span class="sxs-lookup"><span data-stu-id="48275-138">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="48275-139">Satıcıların ödemeleri için örnek çalışma sayfası raporu.</span><span class="sxs-lookup"><span data-stu-id="48275-139">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="48275-140">Veri modeli tanımı alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="48275-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="48275-141">'CustomerCreditTransferInitiation' tanımını seçin.</span><span class="sxs-lookup"><span data-stu-id="48275-141">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="48275-142">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="48275-142">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="48275-143">OPENXML çalışma sayfası biçiminde yeni bir belge tasarlama</span><span class="sxs-lookup"><span data-stu-id="48275-143">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="48275-144">Ağaçta, 'Ödeme modeli\Örnek çalışma sayfası raporu' seçin.</span><span class="sxs-lookup"><span data-stu-id="48275-144">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="48275-145">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="48275-145">Click Designer.</span></span>
3. <span data-ttu-id="48275-146">Eylem Bölmesinde, İçeri Al'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-146">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="48275-147">Microsoft Excel'den içe aktar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-147">Click Import from Excel.</span></span>
5. <span data-ttu-id="48275-148">Ekler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-148">Click Attachments.</span></span>
    * <span data-ttu-id="48275-149">Şablon olarak mevcut Excel belgesini iliştirin.</span><span class="sxs-lookup"><span data-stu-id="48275-149">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="48275-150">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-150">Click New.</span></span>
7. <span data-ttu-id="48275-151">Dosya'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-151">Click File.</span></span>
    * <span data-ttu-id="48275-152">Mevcut Excel dosyasına yönlendirin.</span><span class="sxs-lookup"><span data-stu-id="48275-152">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="48275-153">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="48275-153">Close the page.</span></span>
9. <span data-ttu-id="48275-154">Şablon alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="48275-154">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="48275-155">Şablon olarak kullanılmak üzere ekli Excel dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="48275-155">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="48275-156">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-156">Click OK.</span></span>
    * <span data-ttu-id="48275-157">ER biçim bileşenlerinin, başvurulan MS Excel belgesinin (adlandırılmış aralıklar) yapısına dayalı bir tasarım biçiminde oluşturulduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="48275-157">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="48275-158">Para birimi kodlarına göre toplamları hesaplamak için yeni bir veri kaynağı oluşturma</span><span class="sxs-lookup"><span data-stu-id="48275-158">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="48275-159">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="48275-159">Click the Mapping tab.</span></span>
2. <span data-ttu-id="48275-160">İletişim kutusunu açmak için Kök ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="48275-160">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="48275-161">Ağaçta 'İşleveler\Grupla'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="48275-161">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="48275-162">Ad alanında 'PaymentByCurrency' yazın.</span><span class="sxs-lookup"><span data-stu-id="48275-162">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="48275-163">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="48275-163">PaymentByCurrency</span></span>  
5. <span data-ttu-id="48275-164">Grubu buna göre düzenle'ye tıklatın.</span><span class="sxs-lookup"><span data-stu-id="48275-164">Click Edit group by.</span></span>
6. <span data-ttu-id="48275-165">Ağaçta, 'model'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="48275-165">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="48275-166">Ağaçta seçin 'model\Payments'.</span><span class="sxs-lookup"><span data-stu-id="48275-166">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="48275-167">Alanı buna ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="48275-167">Click Add field to.</span></span>
9. <span data-ttu-id="48275-168">Neler gruplanacak'ı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-168">Click What to group.</span></span>
10. <span data-ttu-id="48275-169">Ağaçta genişletin 'model\Payments'.</span><span class="sxs-lookup"><span data-stu-id="48275-169">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="48275-170">Ağaçta seçin 'model\Payments\Currency'.</span><span class="sxs-lookup"><span data-stu-id="48275-170">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="48275-171">Alanı buna ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="48275-171">Click Add field to.</span></span>
13. <span data-ttu-id="48275-172">Gruplandırılmış alanlar'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="48275-172">Click Grouped fields.</span></span>
14. <span data-ttu-id="48275-173">Ağaçta seçin: 'model\Payments\Instructed Amount(InstructedAmount)'.</span><span class="sxs-lookup"><span data-stu-id="48275-173">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="48275-174">Alanı buna ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="48275-174">Click Add field to.</span></span>
16. <span data-ttu-id="48275-175">Toplam alanları'nı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="48275-175">Click Aggregation fields.</span></span>
17. <span data-ttu-id="48275-176">Yöntem alanında bir seçenek belirtin.</span><span class="sxs-lookup"><span data-stu-id="48275-176">In the Method field, select an option.</span></span>
    * <span data-ttu-id="48275-177">SUM toplama işlevini seçin.</span><span class="sxs-lookup"><span data-stu-id="48275-177">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="48275-178">Ad alanında 'TotalInstructuredAmount' yazın.</span><span class="sxs-lookup"><span data-stu-id="48275-178">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="48275-179">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="48275-179">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="48275-180">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-180">Click Save.</span></span>
20. <span data-ttu-id="48275-181">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="48275-181">Close the page.</span></span>
21. <span data-ttu-id="48275-182">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-182">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="48275-183">Biçim bileşenlerini veri kaynaklarına eşleme</span><span class="sxs-lookup"><span data-stu-id="48275-183">Map format components to data sources</span></span>
1. <span data-ttu-id="48275-184">Ağaçta, 'model'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="48275-184">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="48275-185">Ağaçta genişletin 'model\Payments'.</span><span class="sxs-lookup"><span data-stu-id="48275-185">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="48275-186">Ağaçta, 'model\Payments\Initiating Party(InitiatingParty)' seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="48275-186">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="48275-187">Ağaçta 'model\Payments\Initiating Party(InitiatingParty)\Name' seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="48275-187">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="48275-188">Ağaçta, "Excel\ReportHeader" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="48275-188">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="48275-189">Ağaçta, "Excel\ReportHeader\CompanyName" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="48275-189">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="48275-190">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-190">Click Bind.</span></span>
8. <span data-ttu-id="48275-191">Ağaçta genişletin 'model\Payments\Creditor'.</span><span class="sxs-lookup"><span data-stu-id="48275-191">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="48275-192">Ağaçta genişletin 'model\Payments\Creditor\Identification'.</span><span class="sxs-lookup"><span data-stu-id="48275-192">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="48275-193">Ağaçta seçin: 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span><span class="sxs-lookup"><span data-stu-id="48275-193">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="48275-194">Ağaçta, "Excel\PaymLines" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="48275-194">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="48275-195">Ağaçta, "Excel\PaymLines\VendAccountName" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="48275-195">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="48275-196">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-196">Click Bind.</span></span>
14. <span data-ttu-id="48275-197">Ağaçta seçin 'model\Payments\Creditor\Name'.</span><span class="sxs-lookup"><span data-stu-id="48275-197">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="48275-198">Ağaçta, "Excel\PaymLines\VendName" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="48275-198">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="48275-199">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-199">Click Bind.</span></span>
17. <span data-ttu-id="48275-200">Ağaçta genişletin: 'model\Payments\Creditor Agent(CreditorAgent)'.</span><span class="sxs-lookup"><span data-stu-id="48275-200">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="48275-201">Ağaçta seçin: 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span><span class="sxs-lookup"><span data-stu-id="48275-201">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="48275-202">Ağaçta, "Excel\PaymLines\Banka" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="48275-202">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="48275-203">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-203">Click Bind.</span></span>
21. <span data-ttu-id="48275-204">Ağaçta seçin 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span><span class="sxs-lookup"><span data-stu-id="48275-204">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="48275-205">Ağaçta, "Excel\PaymLines\RoutingNumber" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="48275-205">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="48275-206">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-206">Click Bind.</span></span>
24. <span data-ttu-id="48275-207">Ağaçta 'Model\Payments\Creditor Account(CreditorAccount)' genişletin.</span><span class="sxs-lookup"><span data-stu-id="48275-207">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="48275-208">Ağaçta 'Model\Payments\Creditor Account(CreditorAccount)' genişletin.</span><span class="sxs-lookup"><span data-stu-id="48275-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="48275-209">Ağaçta seçin 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span><span class="sxs-lookup"><span data-stu-id="48275-209">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="48275-210">Ağaçta, "Excel\PaymLines\AccountNumber" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="48275-210">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="48275-211">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-211">Click Bind.</span></span>
29. <span data-ttu-id="48275-212">Ağaçta seçin: 'model\Payments\Instructed Amount(InstructedAmount)'.</span><span class="sxs-lookup"><span data-stu-id="48275-212">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="48275-213">Ağaçta, "Excel\PaymLines\Borç" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="48275-213">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="48275-214">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-214">Click Bind.</span></span>
32. <span data-ttu-id="48275-215">Ağaçta genişletin 'model\Payments\Creditor'.</span><span class="sxs-lookup"><span data-stu-id="48275-215">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="48275-216">Ağaçta 'Model\Payments\Creditor Account(CreditorAccount)' genişletin.</span><span class="sxs-lookup"><span data-stu-id="48275-216">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="48275-217">Ağaçta genişletin: 'model\Payments\Creditor Agent(CreditorAgent)'.</span><span class="sxs-lookup"><span data-stu-id="48275-217">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="48275-218">Ağaçta seçin 'model\Payments\Currency'.</span><span class="sxs-lookup"><span data-stu-id="48275-218">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="48275-219">Ağaçta, "Excel\PaymLines\Para Birimi" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="48275-219">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="48275-220">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-220">Click Bind.</span></span>
38. <span data-ttu-id="48275-221">Ağaçta 'PaymentByCurrency' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="48275-221">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="48275-222">Ağaçta genişletin: 'PaymentByCurrency\grouped'.</span><span class="sxs-lookup"><span data-stu-id="48275-222">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="48275-223">Ağaçta seçin 'PaymentByCurrency\grouped\Currency'.</span><span class="sxs-lookup"><span data-stu-id="48275-223">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="48275-224">Ağaçta, "Excel\SummaryLines" öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="48275-224">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="48275-225">Ağaçta, "Excel\SummaryLines\SummaryCurrency" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="48275-225">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="48275-226">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-226">Click Bind.</span></span>
44. <span data-ttu-id="48275-227">Ağaçta genişletin 'PaymentByCurrency\aggregated'.</span><span class="sxs-lookup"><span data-stu-id="48275-227">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="48275-228">Ağaçta seçin 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span><span class="sxs-lookup"><span data-stu-id="48275-228">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="48275-229">Ağaçta, "Excel\SummaryLines\SummaryAmount" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="48275-229">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="48275-230">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-230">Click Bind.</span></span>
48. <span data-ttu-id="48275-231">Ağaçta 'PaymentByCurrency' seçin.</span><span class="sxs-lookup"><span data-stu-id="48275-231">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="48275-232">Ağaçta, "Excel\SummaryLines" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="48275-232">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="48275-233">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-233">Click Bind.</span></span>
51. <span data-ttu-id="48275-234">Ağaçta seçin 'model\Payments'.</span><span class="sxs-lookup"><span data-stu-id="48275-234">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="48275-235">Ağaçta, "Excel\PaymLines" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="48275-235">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="48275-236">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-236">Click Bind.</span></span>
54. <span data-ttu-id="48275-237">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-237">Click Save.</span></span>
55. <span data-ttu-id="48275-238">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="48275-238">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="48275-239">Ödemeleri işlemek için oluşturulan yapılandırmayı kullanın</span><span class="sxs-lookup"><span data-stu-id="48275-239">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="48275-240">Durumu değiştir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-240">Click Change status.</span></span>
2. <span data-ttu-id="48275-241">Tamamla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-241">Click Complete.</span></span>
3. <span data-ttu-id="48275-242">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-242">Click OK.</span></span>
4. <span data-ttu-id="48275-243">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="48275-243">Close the page.</span></span>
5. <span data-ttu-id="48275-244">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="48275-244">Close the page.</span></span>
6. <span data-ttu-id="48275-245">Borç hesapları > Ödeme kurulumu > Ödeme yöntemleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="48275-245">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="48275-246">Ödeme yöntemi alanına "Elektronik" değeriyle filtre uygulamak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="48275-246">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="48275-247">Elektronik</span><span class="sxs-lookup"><span data-stu-id="48275-247">Electronic</span></span>  
8. <span data-ttu-id="48275-248">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-248">Click Edit.</span></span>
9. <span data-ttu-id="48275-249">Dosya biçimleri bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="48275-249">Expand the File formats section.</span></span>
10. <span data-ttu-id="48275-250">Genel elektronik raporlama alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="48275-250">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="48275-251">Biçim yapılandırmasını dışa aktar alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="48275-251">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="48275-252">'Örnek çalışma sayfası raporu yapılandırması'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="48275-252">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="48275-253">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-253">Click Save.</span></span>
13. <span data-ttu-id="48275-254">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="48275-254">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="48275-255">Oluşturulan yapılandırmayı ödeme günlüklerini işleme için kullanma</span><span class="sxs-lookup"><span data-stu-id="48275-255">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="48275-256">Borç hesapları > Ödemeler > Ödeme günlüğü'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="48275-256">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="48275-257">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-257">Click New.</span></span>
    * <span data-ttu-id="48275-258">Yeni bir ödeme günlüğü oluşturun.</span><span class="sxs-lookup"><span data-stu-id="48275-258">Create a new payment journal.</span></span>  
3. <span data-ttu-id="48275-259">İsim alanına VendPay' yazın.</span><span class="sxs-lookup"><span data-stu-id="48275-259">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="48275-260">VendPay</span><span class="sxs-lookup"><span data-stu-id="48275-260">VendPay</span></span>  
4. <span data-ttu-id="48275-261">Satırlar seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-261">Click Lines.</span></span>
5. <span data-ttu-id="48275-262">Hesap alanında, 'GB_SI_000001' değerlerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="48275-262">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="48275-263">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="48275-263">GB_SI_000001</span></span>  
6. <span data-ttu-id="48275-264">Borcu '1000' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="48275-264">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="48275-265">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-265">Click New.</span></span>
8. <span data-ttu-id="48275-266">Hesap alanında, 'GB_SI_000005' değerlerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="48275-266">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="48275-267">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="48275-267">GB_SI_000005</span></span>  
9. <span data-ttu-id="48275-268">Borcu '2000' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="48275-268">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="48275-269">Para birimi alanına 'EUR' yazın.</span><span class="sxs-lookup"><span data-stu-id="48275-269">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="48275-270">Euro</span><span class="sxs-lookup"><span data-stu-id="48275-270">EUR</span></span>  
11. <span data-ttu-id="48275-271">Mahsup hesabı alanında, 'GBSI OPER' değerlerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="48275-271">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="48275-272">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="48275-272">GBSI OPER</span></span>  
12. <span data-ttu-id="48275-273">Ödeme yöntemi alanına 'Elektronik' girin.</span><span class="sxs-lookup"><span data-stu-id="48275-273">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="48275-274">Elektronik</span><span class="sxs-lookup"><span data-stu-id="48275-274">Electronic</span></span>  
13. <span data-ttu-id="48275-275">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-275">Click Save.</span></span>
14. <span data-ttu-id="48275-276">Ödemeler oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="48275-276">Click Generate payments.</span></span>
15. <span data-ttu-id="48275-277">Ödeme yöntemi alanına 'Elektronik' girin.</span><span class="sxs-lookup"><span data-stu-id="48275-277">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="48275-278">Elektronik</span><span class="sxs-lookup"><span data-stu-id="48275-278">Electronic</span></span>  
16. <span data-ttu-id="48275-279">Ad alanına, "Ödemeler" yazın.</span><span class="sxs-lookup"><span data-stu-id="48275-279">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="48275-280">Örneğin 'Ödemeler' yazın.</span><span class="sxs-lookup"><span data-stu-id="48275-280">For example, type Payments.</span></span>  
17. <span data-ttu-id="48275-281">Banka hesabı alanında 'GBSI OPER' yazın.</span><span class="sxs-lookup"><span data-stu-id="48275-281">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="48275-282">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="48275-282">GBSI OPER</span></span>  
18. <span data-ttu-id="48275-283">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-283">Click OK.</span></span>
19. <span data-ttu-id="48275-284">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48275-284">Click OK.</span></span>
    * <span data-ttu-id="48275-285">Oluşturulan çalışma sayfasını gözden geçirin; ödeme ayrıntı satırları ve bu ödeme iletisinde kullanılacak her bir para birimi kodu için toplamlar da dahil olmak üzere.</span><span class="sxs-lookup"><span data-stu-id="48275-285">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  


