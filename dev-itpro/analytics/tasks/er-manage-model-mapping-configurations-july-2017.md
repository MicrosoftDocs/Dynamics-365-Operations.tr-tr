--- 
title: "Elektronik raporlama (ER) için model eşleme yapılandırmalarını yönetme"
description: "Aşağıdaki adımlar Sistem yöneticisi veya elektronik raporlama geliştiricisi rolüne atanan bir kullanıcının, Elektronik raporlama (ER) model eşleşmelerini ayrı ER yapılandırmalarında nasıl yönetebileceklerini açıklar."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.openlocfilehash: 473cad588253b0eb42eb927834e186ccfa4c4f1e
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="manage-model-mapping-configurations-for-electronic-reporting-er"></a><span data-ttu-id="23458-103">Elektronik raporlama (ER) için model eşleme yapılandırmalarını yönetme</span><span class="sxs-lookup"><span data-stu-id="23458-103">Manage model mapping configurations for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="23458-104">Aşağıdaki adımlar Sistem yöneticisi veya elektronik raporlama geliştiricisi rolüne atanan bir kullanıcının, Elektronik raporlama (ER) model eşleşmelerini ayrı ER yapılandırmalarında nasıl yönetebileceklerini açıklar.</span><span class="sxs-lookup"><span data-stu-id="23458-104">The following steps explain how a user assigned to the System administrator or Electronic reporting developer role can manage Electronic reporting (ER) model mappings in separate ER configurations.</span></span> <span data-ttu-id="23458-105">Bu görev kılavuzunda bir örnek şirket olan Litware, Inc. için gerekli ER yapılandırmalarını oluşturacaksınız. Bu görev kılavuzunu tamamlamak için önce "ER Bir yapılandırma sağlayıcısı oluştur ve bunu etkin olarak işaretle" görev kılavuzundaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="23458-105">In this task guide, you will create required ER configurations for the sample company, Litware, Inc. To complete this task guide, you must first complete the steps in the task guide, “ER Create a configuration provider” and mark it as active.</span></span> 

<span data-ttu-id="23458-106">ER yapılandırmalarının şirketler arasında paylaşılması nedeniyle, bu görev kılavuzunu istediğiniz şirketin veri kümesini kullanarak tamamlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="23458-106">Because ER configurations are shared among companies, you can complete this task guide using the company data set of your choice.</span></span> <span data-ttu-id="23458-107">Bu görev kılavuzunu işlevleri, aşağıdaki düzeltmelerden birini yüklediyseniz kullanılabilir: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 , Dynamics AX 7.0 sürümü için veya https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 Dynamics 365 for Operations sürümü için.</span><span class="sxs-lookup"><span data-stu-id="23458-107">The functionality for this task guide is available if you have installed one of the following hotfixes: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 for the Dynamics AX 7.0 version or https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 for the Dynamics 365 for Operations version.</span></span>

1. <span data-ttu-id="23458-108">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="23458-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="23458-109">Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve etkin olarak işaretlendiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="23458-109">Verify that the configuration provider for the sample company Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="23458-110">Bu yapılandırma sağlayıcısını göremiyorsanız öncelikle Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme görev kılavuzundaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="23458-110">If you don’t see this configuration provider, you must first complete the steps in the task guide, Create a configuration provider and mark it as active.</span></span>   

## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="23458-111">Yeni bir ER model yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="23458-111">Add a new ER model configuration</span></span>
1. <span data-ttu-id="23458-112">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-112">Click Reporting configurations.</span></span>
    * <span data-ttu-id="23458-113">Yeni bir model yapılandırması ekleme.</span><span class="sxs-lookup"><span data-stu-id="23458-113">Add a new model configuration.</span></span> <span data-ttu-id="23458-114">Adı, yapılandırma ağacında benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="23458-114">The name must be unique in the configurations tree.</span></span>  
2. <span data-ttu-id="23458-115">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-115">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="23458-116">İsim alanında 'Örnek veri modeli' yazın.</span><span class="sxs-lookup"><span data-stu-id="23458-116">In the Name field, type 'Sample data model'.</span></span>
    * <span data-ttu-id="23458-117">Örnek veri modeli</span><span class="sxs-lookup"><span data-stu-id="23458-117">Sample data model</span></span>  
4. <span data-ttu-id="23458-118">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="23458-118">Click Create configuration.</span></span>
5. <span data-ttu-id="23458-119">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="23458-119">Click Designer.</span></span>
6. <span data-ttu-id="23458-120">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-120">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="23458-121">Ad alanına 'Kök' yazın.</span><span class="sxs-lookup"><span data-stu-id="23458-121">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="23458-122">Kök</span><span class="sxs-lookup"><span data-stu-id="23458-122">Root</span></span>  
8. <span data-ttu-id="23458-123">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="23458-123">Click Add.</span></span>
9. <span data-ttu-id="23458-124">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="23458-125">İsim alanına 'Şirket' yazın.</span><span class="sxs-lookup"><span data-stu-id="23458-125">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="23458-126">Şirket</span><span class="sxs-lookup"><span data-stu-id="23458-126">Company</span></span>  
11. <span data-ttu-id="23458-127">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="23458-127">Click Add.</span></span>
12. <span data-ttu-id="23458-128">Açıklama alanında kullanıcın çalışma zamanında oturum açtığı metni, tüzel kişiliği veya şirketi girin.</span><span class="sxs-lookup"><span data-stu-id="23458-128">In the Description field, enter the text, Description of the legal entity or company in which a user logged at run-time.</span></span> 
    * <span data-ttu-id="23458-129">Kullanıcının çalışma zamanında oturum açmış olduğu tüzel kişinin veya şirketin açıklaması.</span><span class="sxs-lookup"><span data-stu-id="23458-129">Description of the legal entity or company in which a user logged at run-time.</span></span>  
13. <span data-ttu-id="23458-130">Kök referansına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-130">Click Root reference.</span></span>
14. <span data-ttu-id="23458-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-131">Click OK.</span></span>
15. <span data-ttu-id="23458-132">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-132">Click Save.</span></span>
16. <span data-ttu-id="23458-133">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="23458-133">Close the page.</span></span>
17. <span data-ttu-id="23458-134">Durumu değiştir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-134">Click Change status.</span></span>
18. <span data-ttu-id="23458-135">Tamamla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-135">Click Complete.</span></span>
19. <span data-ttu-id="23458-136">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-136">Click OK.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="23458-137">Yeni bir ER modeli eşleme yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="23458-137">Add a new ER model mapping configuration</span></span>
1. <span data-ttu-id="23458-138">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="23458-139">Yeni alanına, 'Örnek veri modeli veri modelini temel alan Model Eşleme' yazın.</span><span class="sxs-lookup"><span data-stu-id="23458-139">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
3. <span data-ttu-id="23458-140">İsim alanına 'Örnek eşleme' yazın.</span><span class="sxs-lookup"><span data-stu-id="23458-140">In the Name field, type 'Sample mapping'.</span></span>
    * <span data-ttu-id="23458-141">Örnek eşleme</span><span class="sxs-lookup"><span data-stu-id="23458-141">Sample mapping</span></span>  
4. <span data-ttu-id="23458-142">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="23458-142">Click Create configuration.</span></span>
5. <span data-ttu-id="23458-143">Önkoşullar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="23458-143">Expand the Prerequisites section.</span></span>
    * <span data-ttu-id="23458-144">Uygulama önkoşulları grubunun otomatik olarak eklenmiş olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="23458-144">Note that the Implementations prerequisites group has been added automatically.</span></span> <span data-ttu-id="23458-145">Grup, ana veri modeli yapılandırmasına referans gösteren önkoşul bileşenini içerir ve Uygulama olarak işaretlenmiştir.</span><span class="sxs-lookup"><span data-stu-id="23458-145">The group contains the prerequisite component that refers to the parent data model configuration and is marked as Implementation.</span></span> <span data-ttu-id="23458-146">Bu, Örnek eşleme modeli eşleme yapılandırmasının, veri modeli, Örnek veri modelinin uygulaması olarak kabul edildiği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="23458-146">This means that this Sample mapping model mapping configuration is considered the implementation of the data model, Sample data model.</span></span> <span data-ttu-id="23458-147">Bu nedenle, bu bileşen ER'nin model yapılandırması, Örnek veri modeli indirildiğinde model eşleme yapılandırmasını, bir ER havuzundan indirmesini zorlayacaktır.</span><span class="sxs-lookup"><span data-stu-id="23458-147">Therefore, this component will force ER to download the model mapping configuration, Sample mapping from an ER repository when the model configuration, Sample data model, is downloaded.</span></span>   
6. <span data-ttu-id="23458-148">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="23458-148">Click Designer.</span></span>
    * <span data-ttu-id="23458-149">Oluşturulan model eşleme yapılandırmasının, oluşturulan yapılandırma ile aynı ada sahip bir boş eşlemeye sahip olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="23458-149">Note that the created model mapping configuration contains a new blank mapping with the same name as the created configuration.</span></span> <span data-ttu-id="23458-150">Seçilen bir ana model yapılandırması, model eşlemeleri içeriyorsa, bunların yeni bir model eşleme yapılandırmasına kopyalanacağını göz önünde bulundurun.</span><span class="sxs-lookup"><span data-stu-id="23458-150">Be aware that when a selected parent model configuration contains model mappings, they will be copied to a new model mapping configuration.</span></span>   
7. <span data-ttu-id="23458-151">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="23458-151">Click Designer.</span></span>
8. <span data-ttu-id="23458-152">Ağaçta, 'Dynamics 365 for Operations\Tablo' seçin.</span><span class="sxs-lookup"><span data-stu-id="23458-152">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="23458-153">Kök ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-153">Click Add root.</span></span>
10. <span data-ttu-id="23458-154">İsim alanına 'Şirket' yazın.</span><span class="sxs-lookup"><span data-stu-id="23458-154">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="23458-155">Şirket</span><span class="sxs-lookup"><span data-stu-id="23458-155">Company</span></span>  
11. <span data-ttu-id="23458-156">Tablo alanına 'CompanyInfo' yazın.</span><span class="sxs-lookup"><span data-stu-id="23458-156">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="23458-157">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="23458-157">CompanyInfo</span></span>  
12. <span data-ttu-id="23458-158">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-158">Click OK.</span></span>
13. <span data-ttu-id="23458-159">Ağaçta, 'Şirket' metnini genişletin.</span><span class="sxs-lookup"><span data-stu-id="23458-159">In the tree, expand 'Company'.</span></span>
14. <span data-ttu-id="23458-160">Ağaçta, 'Şirket\find()' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="23458-160">In the tree, expand 'Company\find()'.</span></span>
15. <span data-ttu-id="23458-161">Ağaçta, 'Şirket\find()\Ad' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="23458-161">In the tree, select 'Company\find()\Name'.</span></span>
16. <span data-ttu-id="23458-162">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-162">Click Bind.</span></span>
17. <span data-ttu-id="23458-163">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-163">Click Save.</span></span>
18. <span data-ttu-id="23458-164">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="23458-164">Close the page.</span></span>
19. <span data-ttu-id="23458-165">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="23458-165">Close the page.</span></span>
20. <span data-ttu-id="23458-166">Eylem Bölmesi'nde, Yapılandırmalar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-166">On the Action Pane, click Configurations.</span></span>
21. <span data-ttu-id="23458-167">Kullanıcı parametreleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-167">Click User parameters.</span></span>
22. <span data-ttu-id="23458-168">Çalıştırma ayarları alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="23458-168">Select Yes in the Run settings field.</span></span>
23. <span data-ttu-id="23458-169">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-169">Click OK.</span></span>
24. <span data-ttu-id="23458-170">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-170">Click Edit.</span></span>
25. <span data-ttu-id="23458-171">Taslak Çalıştır alanında Evet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-171">Select Yes in the Run Draft field.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="23458-172">Yeni bir ER biçim yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="23458-172">Add a new ER format configuration</span></span>
1. <span data-ttu-id="23458-173">Ağaçta 'Örnek veri modeli' seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="23458-173">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="23458-174">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-174">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="23458-175">Yeni alanına, 'Örnek veri modeli veri modelini temel alan biçim' yazın.</span><span class="sxs-lookup"><span data-stu-id="23458-175">In the New field, enter 'Format based on data model Sample data model'.</span></span>
4. <span data-ttu-id="23458-176">İsim alanına 'Örnek biçim' yazın.</span><span class="sxs-lookup"><span data-stu-id="23458-176">In the Name field, type 'Sample format'.</span></span>
    * <span data-ttu-id="23458-177">Örnek biçim</span><span class="sxs-lookup"><span data-stu-id="23458-177">Sample format</span></span>  
5. <span data-ttu-id="23458-178">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="23458-178">Click Create configuration.</span></span>
6. <span data-ttu-id="23458-179">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="23458-179">Click Designer.</span></span>
7. <span data-ttu-id="23458-180">İletişim kutusunu açmak için Kök ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="23458-180">Click Add root to open the drop dialog.</span></span>
8. <span data-ttu-id="23458-181">Ağaçta seçin 'Text\String'.</span><span class="sxs-lookup"><span data-stu-id="23458-181">In the tree, select 'Text\String'.</span></span>
9. <span data-ttu-id="23458-182">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-182">Click OK.</span></span>
10. <span data-ttu-id="23458-183">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="23458-183">Click the Mapping tab.</span></span>
11. <span data-ttu-id="23458-184">Ağaçta, 'model'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="23458-184">In the tree, expand 'model'.</span></span>
12. <span data-ttu-id="23458-185">Ağaçta, 'model\Şirket' metnini seçin.</span><span class="sxs-lookup"><span data-stu-id="23458-185">In the tree, select 'model\Company'.</span></span>
13. <span data-ttu-id="23458-186">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-186">Click Bind.</span></span>
14. <span data-ttu-id="23458-187">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-187">Click Save.</span></span>
15. <span data-ttu-id="23458-188">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="23458-188">Close the page.</span></span>
    * <span data-ttu-id="23458-189">Test amacıyla oluşturulan biçimin taslak sürümünü çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="23458-189">Run the draft version of the created format for testing purposes.</span></span>  
16. <span data-ttu-id="23458-190">Çalıştır öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-190">Click Run.</span></span>
    * <span data-ttu-id="23458-191">Sürümler hızlı sekmesinde, Çalıştır'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="23458-191">On the Versions FastTab, click Run.</span></span>  
17. <span data-ttu-id="23458-192">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-192">Click OK.</span></span>
    * <span data-ttu-id="23458-193">Bu biçim yapılandırmasını çalıştıran kullanıcının oturum açmış olduğu şirketin adını içeren çıktıyı gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="23458-193">Review the output that contains the name of the company in which the user who is running this format configuration is logged into.</span></span> <span data-ttu-id="23458-194">Oluşturulan modelleme yapılandırmasının bu biçim yapılandırıcısı tarafından, gerekli model eşlemelerini içeren tek bir yapılandırma mevcut olduğu için kullanıldığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="23458-194">Note that the created model mapping configuration is used by this format configuration because there is only one configuration available that contains required model mappings.</span></span>   

## <a name="add-alternative-er-model-mapping-configuration"></a><span data-ttu-id="23458-195">Alternatif bir ER modeli eşleme yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="23458-195">Add alternative ER model mapping configuration</span></span>
1. <span data-ttu-id="23458-196">Ağaçta 'Örnek veri modeli' seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="23458-196">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="23458-197">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-197">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="23458-198">Yeni alanına, 'Örnek veri modeli veri modelini temel alan Model Eşleme' yazın.</span><span class="sxs-lookup"><span data-stu-id="23458-198">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
4. <span data-ttu-id="23458-199">İsim alanında 'Örnek eşleme (alternatif)' yazın.</span><span class="sxs-lookup"><span data-stu-id="23458-199">In the Name field, type 'Sample mapping (alternative)'.</span></span>
    * <span data-ttu-id="23458-200">Örnek eşleme (alternatif)</span><span class="sxs-lookup"><span data-stu-id="23458-200">Sample mapping (alternative)</span></span>  
5. <span data-ttu-id="23458-201">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="23458-201">Click Create configuration.</span></span>
6. <span data-ttu-id="23458-202">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="23458-202">Click Designer.</span></span>
7. <span data-ttu-id="23458-203">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="23458-203">Click Designer.</span></span>
8. <span data-ttu-id="23458-204">Ağaçta, 'Dynamics 365 for Operations\Tablo' seçin.</span><span class="sxs-lookup"><span data-stu-id="23458-204">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="23458-205">Kök ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-205">Click Add root.</span></span>
10. <span data-ttu-id="23458-206">İsim alanına 'Şirket' yazın.</span><span class="sxs-lookup"><span data-stu-id="23458-206">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="23458-207">Şirket</span><span class="sxs-lookup"><span data-stu-id="23458-207">Company</span></span>  
11. <span data-ttu-id="23458-208">Tablo alanına 'CompanyInfo' yazın.</span><span class="sxs-lookup"><span data-stu-id="23458-208">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="23458-209">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="23458-209">CompanyInfo</span></span>  
12. <span data-ttu-id="23458-210">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-210">Click OK.</span></span>
13. <span data-ttu-id="23458-211">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-211">Click Edit.</span></span>
14. <span data-ttu-id="23458-212">Ağaçta 'String\CONCATENATE' seçin.</span><span class="sxs-lookup"><span data-stu-id="23458-212">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="23458-213">Fonksiyon ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-213">Click Add function.</span></span>
16. <span data-ttu-id="23458-214">Ağaçta, 'Şirket' metnini genişletin.</span><span class="sxs-lookup"><span data-stu-id="23458-214">In the tree, expand 'Company'.</span></span>
17. <span data-ttu-id="23458-215">Ağaçta, 'Şirket\find()' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="23458-215">In the tree, expand 'Company\find()'.</span></span>
18. <span data-ttu-id="23458-216">Ağaçta, 'Şirket\find()\Ad' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="23458-216">In the tree, select 'Company\find()\Name'.</span></span>
19. <span data-ttu-id="23458-217">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-217">Click Add data source.</span></span>
20. <span data-ttu-id="23458-218">Formül alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="23458-218">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="23458-219">CONCATENATE(Company.'find()'.Name, ";",</span><span class="sxs-lookup"><span data-stu-id="23458-219">CONCATENATE(Company.'find()'.Name, ";",</span></span>  
21. <span data-ttu-id="23458-220">Ağaçta, 'Şirket\find()\Şirket(DataArea)' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="23458-220">In the tree, select 'Company\find()\Company(DataArea)'.</span></span>
22. <span data-ttu-id="23458-221">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-221">Click Add data source.</span></span>
23. <span data-ttu-id="23458-222">Formül alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="23458-222">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="23458-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span><span class="sxs-lookup"><span data-stu-id="23458-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span></span>  
24. <span data-ttu-id="23458-224">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-224">Click Save.</span></span>
25. <span data-ttu-id="23458-225">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="23458-225">Close the page.</span></span>
26. <span data-ttu-id="23458-226">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-226">Click Save.</span></span>
27. <span data-ttu-id="23458-227">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="23458-227">Close the page.</span></span>
28. <span data-ttu-id="23458-228">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="23458-228">Close the page.</span></span>
29. <span data-ttu-id="23458-229">Taslak Çalıştır alanında Evet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-229">Select Yes in the Run Draft field.</span></span>

## <a name="use-an-existing-er-model-mapping-configuration"></a><span data-ttu-id="23458-230">Mevcut bir ER model eşleme yapılandırmasının kullanın</span><span class="sxs-lookup"><span data-stu-id="23458-230">Use an existing ER model mapping configuration</span></span>
1. <span data-ttu-id="23458-231">Ağaçta, 'Örnek veri modeli\Örnek biçim' seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="23458-231">In the tree, select 'Sample data model\Sample format'.</span></span>
2. <span data-ttu-id="23458-232">Çalıştır öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-232">Click Run.</span></span>
    * <span data-ttu-id="23458-233">ER biçim yapılandırmasının, çalışan ER biçiminin veri kaynağı olarak seçilen belirtilmemiş veri modelinin birden fazla model eşlemesine sahip olduğu için ER biçim yapılandırmasının taslak sürümünün çalıştırılamayacağını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="23458-233">Note that the selected draft version of the ER format configuration can’t be executed because there is more than one model mapping configuration available for the undefined data model that has been selected as the data source of the running ER format.</span></span>   
    * <span data-ttu-id="23458-234">Daha sonra, alternatif model eşleme yapılandırmasını, çalışan ER biçimi için veri kaynakları olarak kullanılacak model eşlemelerinin tanımlayacaksınız.</span><span class="sxs-lookup"><span data-stu-id="23458-234">Next, you will define the alternative model mapping configuration as the one from which model mappings will be used as data sources for running ER format.</span></span>   
3. <span data-ttu-id="23458-235">Ağaçta, 'Örnek veri modeli\Örnek eşleme (alternatif)' seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="23458-235">In the tree, select 'Sample data model\Sample mapping (alternative)'.</span></span>
4. <span data-ttu-id="23458-236">Model eşleme varsayılanı alanında, Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="23458-236">Select Yes in the Default for model mapping field.</span></span>
5. <span data-ttu-id="23458-237">Ağaçta, 'Örnek veri modeli\Örnek biçim' seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="23458-237">In the tree, select 'Sample data model\Sample format'.</span></span>
6. <span data-ttu-id="23458-238">Çalıştır öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-238">Click Run.</span></span>
7. <span data-ttu-id="23458-239">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="23458-239">Click OK.</span></span>
    * <span data-ttu-id="23458-240">Varsayılan model yapılandırasının, bu biçim yapılandırması tarafından elektronik belge oluşturmak için kullanıldığını unutmayın (oluşturulan çıktı şirket kodunu içerir).</span><span class="sxs-lookup"><span data-stu-id="23458-240">Note that the default model mapping configuration is used by this format configuration for generating the electronic document (the created output contains the company code).</span></span>  


