---
title: Ayrı ER yapılandırmalarında ER model eşlemesini yönetme
description: Bu konuda, ayrı ER yapılandırmalarında Elektronik raporlama (ER) modeli eşlemelerinin nasıl yönetileceği açıklanmaktadır.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fdd6804c33cc153974229c60b64c3bd76426241a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569425"
---
# <a name="manage-er-model-mapping-in-separate-er-configurations"></a><span data-ttu-id="00344-103">Ayrı ER yapılandırmalarında ER model eşlemesini yönetme</span><span class="sxs-lookup"><span data-stu-id="00344-103">Manage ER model mapping in separate ER configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="00344-104">Aşağıdaki adımlar Sistem yöneticisi veya elektronik raporlama geliştiricisi rolüne atanan bir kullanıcının, Elektronik raporlama (ER) model eşleşmelerini ayrı ER yapılandırmalarında nasıl yönetebileceklerini açıklar.</span><span class="sxs-lookup"><span data-stu-id="00344-104">The following steps explain how a user assigned to the System administrator or Electronic reporting developer role can manage Electronic reporting (ER) model mappings in separate ER configurations.</span></span> <span data-ttu-id="00344-105">Bu görev kılavuzunda bir örnek şirket olan Litware, Inc. için gerekli ER yapılandırmalarını oluşturacaksınız. Bu görev kılavuzunu tamamlamak için önce "ER Bir yapılandırma sağlayıcısı oluştur ve bunu etkin olarak işaretle" görev kılavuzundaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="00344-105">In this task guide, you will create required ER configurations for the sample company, Litware, Inc. To complete this task guide, you must first complete the steps in the task guide, "ER Create a configuration provider" and mark it as active.</span></span> 

<span data-ttu-id="00344-106">ER yapılandırmalarının şirketler arasında paylaşılması nedeniyle, bu görev kılavuzunu istediğiniz şirketin veri kümesini kullanarak tamamlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="00344-106">Because ER configurations are shared among companies, you can complete this task guide using the company data set of your choice.</span></span> <span data-ttu-id="00344-107">Bu görev kılavuzunu işlevleri, aşağıdaki düzeltmelerden birini yüklediyseniz kullanılabilir: Dynamics AX 7.0 sürümü için https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 veya Dynamics 365 for Operations sürümü için https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871.</span><span class="sxs-lookup"><span data-stu-id="00344-107">The functionality for this task guide is available if you have installed one of the following hotfixes: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 for the Dynamics AX 7.0 version or https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 for the Dynamics 365 for Operations version.</span></span>

1. <span data-ttu-id="00344-108">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="00344-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="00344-109">Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve etkin olarak işaretlendiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="00344-109">Verify that the configuration provider for the sample company Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="00344-110">Bu yapılandırma sağlayıcısını göremiyorsanız öncelikle görev kılavuzundaki adımları tamamlamanız, yapılandırma sağlayıcısı oluşturmanız ve sağlayıcı etkin olarak işaretlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="00344-110">If you don't see this configuration provider, you must first complete the steps in the task guide, Create a configuration provider, and mark it as active.</span></span>   

## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="00344-111">Yeni bir ER model yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="00344-111">Add a new ER model configuration</span></span>
1. <span data-ttu-id="00344-112">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-112">Click Reporting configurations.</span></span>
    * <span data-ttu-id="00344-113">Yeni bir model yapılandırması ekleme.</span><span class="sxs-lookup"><span data-stu-id="00344-113">Add a new model configuration.</span></span> <span data-ttu-id="00344-114">Adı, yapılandırma ağacında benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="00344-114">The name must be unique in the configurations tree.</span></span>  
2. <span data-ttu-id="00344-115">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-115">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="00344-116">İsim alanında 'Örnek veri modeli' yazın.</span><span class="sxs-lookup"><span data-stu-id="00344-116">In the Name field, type 'Sample data model'.</span></span>
    * <span data-ttu-id="00344-117">Örnek veri modeli</span><span class="sxs-lookup"><span data-stu-id="00344-117">Sample data model</span></span>  
4. <span data-ttu-id="00344-118">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="00344-118">Click Create configuration.</span></span>
5. <span data-ttu-id="00344-119">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="00344-119">Click Designer.</span></span>
6. <span data-ttu-id="00344-120">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-120">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="00344-121">Ad alanına 'Kök' yazın.</span><span class="sxs-lookup"><span data-stu-id="00344-121">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="00344-122">Kök</span><span class="sxs-lookup"><span data-stu-id="00344-122">Root</span></span>  
8. <span data-ttu-id="00344-123">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="00344-123">Click Add.</span></span>
9. <span data-ttu-id="00344-124">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="00344-125">İsim alanına 'Şirket' yazın.</span><span class="sxs-lookup"><span data-stu-id="00344-125">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="00344-126">Şirket</span><span class="sxs-lookup"><span data-stu-id="00344-126">Company</span></span>  
11. <span data-ttu-id="00344-127">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="00344-127">Click Add.</span></span>
12. <span data-ttu-id="00344-128">Açıklama alanında kullanıcın çalışma zamanında oturum açtığı metni, tüzel kişiliği veya şirketi girin.</span><span class="sxs-lookup"><span data-stu-id="00344-128">In the Description field, enter the text, Description of the legal entity or company in which a user logged at run-time.</span></span> 
    * <span data-ttu-id="00344-129">Kullanıcının çalışma zamanında oturum açmış olduğu tüzel kişinin veya şirketin açıklaması.</span><span class="sxs-lookup"><span data-stu-id="00344-129">Description of the legal entity or company in which a user logged at run-time.</span></span>  
13. <span data-ttu-id="00344-130">Kök referansına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-130">Click Root reference.</span></span>
14. <span data-ttu-id="00344-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-131">Click OK.</span></span>
15. <span data-ttu-id="00344-132">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-132">Click Save.</span></span>
16. <span data-ttu-id="00344-133">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="00344-133">Close the page.</span></span>
17. <span data-ttu-id="00344-134">Durumu değiştir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-134">Click Change status.</span></span>
18. <span data-ttu-id="00344-135">Tamamla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-135">Click Complete.</span></span>
19. <span data-ttu-id="00344-136">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-136">Click OK.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="00344-137">Yeni bir ER model eşleme yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="00344-137">Add a new ER model-mapping configuration</span></span>
1. <span data-ttu-id="00344-138">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="00344-139">Yeni alanına, 'Örnek veri modeli veri modelini temel alan Model Eşleme' yazın.</span><span class="sxs-lookup"><span data-stu-id="00344-139">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
3. <span data-ttu-id="00344-140">İsim alanına 'Örnek eşleme' yazın.</span><span class="sxs-lookup"><span data-stu-id="00344-140">In the Name field, type 'Sample mapping'.</span></span>
    * <span data-ttu-id="00344-141">Örnek eşleme</span><span class="sxs-lookup"><span data-stu-id="00344-141">Sample mapping</span></span>  
4. <span data-ttu-id="00344-142">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="00344-142">Click Create configuration.</span></span>
5. <span data-ttu-id="00344-143">Önkoşullar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="00344-143">Expand the Prerequisites section.</span></span>
    * <span data-ttu-id="00344-144">Uygulama ön koşulları grubu, otomatik olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="00344-144">The Implementations prerequisites group has been added automatically.</span></span> <span data-ttu-id="00344-145">Grup, ana veri modeli yapılandırmasına referans gösteren önkoşul bileşenini içerir ve Uygulama olarak işaretlenmiştir.</span><span class="sxs-lookup"><span data-stu-id="00344-145">The group contains the prerequisite component that refers to the parent data model configuration and is marked as Implementation.</span></span> <span data-ttu-id="00344-146">Bu drurum, Örnek eşleme model eşleme yapılandırmasının Örnek veri modelinin uygulaması kabul edildiği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="00344-146">This means that this Sample-mapping model-mapping configuration is considered the implementation of the data model, Sample data model.</span></span> <span data-ttu-id="00344-147">Bu nedenle, Örnek veri modeli model yapılandırılması indirildiğinde bu bileşen, ER'nin ER deposundan Örnek eşleme model eşleme yapılandırmasını indirmesini sağlayacaktır.</span><span class="sxs-lookup"><span data-stu-id="00344-147">Therefore, this component will force ER to download the model-mapping configuration, Sample mapping from an ER repository when the model configuration, Sample data model, is downloaded.</span></span>   
6. <span data-ttu-id="00344-148">Tasarımcı'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-148">Click Designer.</span></span>
    * <span data-ttu-id="00344-149">Oluşturulan model eşleme yapılandırması, oluşturulan yapılandırma ile aynı ada sahip bir boş eşleme içerir.</span><span class="sxs-lookup"><span data-stu-id="00344-149">The created model-mapping configuration contains a new blank mapping with the same name as the created configuration.</span></span> <span data-ttu-id="00344-150">Seçilen bir üst model yapılandırması, model eşlemeleri içeriyorsa bunlar yeni bir model eşleme yapılandırmasına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="00344-150">When a selected parent model configuration contains model mappings, they will be copied to a new model-mapping configuration.</span></span>   
7. <span data-ttu-id="00344-151">Tasarımcı'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-151">Click Designer.</span></span>
8. <span data-ttu-id="00344-152">Ağaçta, 'Dynamics 365 for Operations\Tablo' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="00344-152">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="00344-153">Kök ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-153">Click Add root.</span></span>
10. <span data-ttu-id="00344-154">İsim alanına 'Şirket' yazın.</span><span class="sxs-lookup"><span data-stu-id="00344-154">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="00344-155">Şirket</span><span class="sxs-lookup"><span data-stu-id="00344-155">Company</span></span>  
11. <span data-ttu-id="00344-156">Tablo alanına 'CompanyInfo' yazın.</span><span class="sxs-lookup"><span data-stu-id="00344-156">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="00344-157">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="00344-157">CompanyInfo</span></span>  
12. <span data-ttu-id="00344-158">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-158">Click OK.</span></span>
13. <span data-ttu-id="00344-159">Ağaçta, 'Şirket' metnini genişletin.</span><span class="sxs-lookup"><span data-stu-id="00344-159">In the tree, expand 'Company'.</span></span>
14. <span data-ttu-id="00344-160">Ağaçta, 'Şirket\find()' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="00344-160">In the tree, expand 'Company\find()'.</span></span>
15. <span data-ttu-id="00344-161">Ağaçta, 'Şirket\find()\Ad' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="00344-161">In the tree, select 'Company\find()\Name'.</span></span>
16. <span data-ttu-id="00344-162">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-162">Click Bind.</span></span>
17. <span data-ttu-id="00344-163">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-163">Click Save.</span></span>
18. <span data-ttu-id="00344-164">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="00344-164">Close the page.</span></span>
19. <span data-ttu-id="00344-165">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="00344-165">Close the page.</span></span>
20. <span data-ttu-id="00344-166">Eylem Bölmesi'nde, Yapılandırmalar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-166">On the Action Pane, click Configurations.</span></span>
21. <span data-ttu-id="00344-167">Kullanıcı parametreleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-167">Click User parameters.</span></span>
22. <span data-ttu-id="00344-168">Çalıştırma ayarları alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="00344-168">Select Yes in the Run settings field.</span></span>
23. <span data-ttu-id="00344-169">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-169">Click OK.</span></span>
24. <span data-ttu-id="00344-170">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-170">Click Edit.</span></span>
25. <span data-ttu-id="00344-171">Taslak Çalıştır alanında Evet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-171">Select Yes in the Run Draft field.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="00344-172">Yeni bir ER biçim yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="00344-172">Add a new ER format configuration</span></span>
1. <span data-ttu-id="00344-173">Ağaçta 'Örnek veri modeli' seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="00344-173">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="00344-174">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-174">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="00344-175">Yeni alanına, 'Örnek veri modeli veri modelini temel alan biçim' yazın.</span><span class="sxs-lookup"><span data-stu-id="00344-175">In the New field, enter 'Format based on data model Sample data model'.</span></span>
4. <span data-ttu-id="00344-176">İsim alanına 'Örnek biçim' yazın.</span><span class="sxs-lookup"><span data-stu-id="00344-176">In the Name field, type 'Sample format'.</span></span>
    * <span data-ttu-id="00344-177">Örnek biçim</span><span class="sxs-lookup"><span data-stu-id="00344-177">Sample format</span></span>  
5. <span data-ttu-id="00344-178">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="00344-178">Click Create configuration.</span></span>
6. <span data-ttu-id="00344-179">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="00344-179">Click Designer.</span></span>
7. <span data-ttu-id="00344-180">İletişim kutusunu açmak için Kök ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="00344-180">Click Add root to open the drop dialog.</span></span>
8. <span data-ttu-id="00344-181">Ağaçta seçin 'Text\String'.</span><span class="sxs-lookup"><span data-stu-id="00344-181">In the tree, select 'Text\String'.</span></span>
9. <span data-ttu-id="00344-182">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-182">Click OK.</span></span>
10. <span data-ttu-id="00344-183">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="00344-183">Click the Mapping tab.</span></span>
11. <span data-ttu-id="00344-184">Ağaçta, 'model'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="00344-184">In the tree, expand 'model'.</span></span>
12. <span data-ttu-id="00344-185">Ağaçta, 'model\Şirket' metnini seçin.</span><span class="sxs-lookup"><span data-stu-id="00344-185">In the tree, select 'model\Company'.</span></span>
13. <span data-ttu-id="00344-186">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-186">Click Bind.</span></span>
14. <span data-ttu-id="00344-187">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-187">Click Save.</span></span>
15. <span data-ttu-id="00344-188">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="00344-188">Close the page.</span></span>
    * <span data-ttu-id="00344-189">Test amacıyla oluşturulan biçimin taslak sürümünü çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="00344-189">Run the draft version of the created format for testing purposes.</span></span>  
16. <span data-ttu-id="00344-190">Çalıştır öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-190">Click Run.</span></span>
    * <span data-ttu-id="00344-191">Sürümler hızlı sekmesinde, Çalıştır'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="00344-191">On the Versions FastTab, click Run.</span></span>  
17. <span data-ttu-id="00344-192">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-192">Click OK.</span></span>
    * <span data-ttu-id="00344-193">Bu biçim yapılandırmasını çalıştıran kullanıcının oturum açmış olduğu şirketin adını içeren çıktıyı gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="00344-193">Review the output that contains the name of the company in which the user who is running this format configuration is logged into.</span></span> <span data-ttu-id="00344-194">Gerekli model eşlemelerini içeren tek bir yapılandırma mevcut olduğundan, oluşturulan model eşleme yapılandırması bu biçim yapılandırması tarafından kullanılır.</span><span class="sxs-lookup"><span data-stu-id="00344-194">The created model-mapping configuration is used by this format configuration because there is only one configuration available that contains required model mappings.</span></span>   

## <a name="add-alternative-er-model-mapping-configuration"></a><span data-ttu-id="00344-195">Alternatif bir ER model eşleme yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="00344-195">Add alternative ER model-mapping configuration</span></span>
1. <span data-ttu-id="00344-196">Ağaçta 'Örnek veri modeli' seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="00344-196">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="00344-197">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-197">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="00344-198">Yeni alanına, 'Örnek veri modeli veri modelini temel alan Model Eşleme' yazın.</span><span class="sxs-lookup"><span data-stu-id="00344-198">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
4. <span data-ttu-id="00344-199">İsim alanında 'Örnek eşleme (alternatif)' yazın.</span><span class="sxs-lookup"><span data-stu-id="00344-199">In the Name field, type 'Sample mapping (alternative)'.</span></span>
    * <span data-ttu-id="00344-200">Örnek eşleme (alternatif)</span><span class="sxs-lookup"><span data-stu-id="00344-200">Sample mapping (alternative)</span></span>  
5. <span data-ttu-id="00344-201">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="00344-201">Click Create configuration.</span></span>
6. <span data-ttu-id="00344-202">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="00344-202">Click Designer.</span></span>
7. <span data-ttu-id="00344-203">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="00344-203">Click Designer.</span></span>
8. <span data-ttu-id="00344-204">Ağaçta, 'Dynamics 365 for Operations\Tablo' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="00344-204">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="00344-205">Kök ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-205">Click Add root.</span></span>
10. <span data-ttu-id="00344-206">İsim alanına 'Şirket' yazın.</span><span class="sxs-lookup"><span data-stu-id="00344-206">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="00344-207">Şirket</span><span class="sxs-lookup"><span data-stu-id="00344-207">Company</span></span>  
11. <span data-ttu-id="00344-208">Tablo alanına 'CompanyInfo' yazın.</span><span class="sxs-lookup"><span data-stu-id="00344-208">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="00344-209">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="00344-209">CompanyInfo</span></span>  
12. <span data-ttu-id="00344-210">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-210">Click OK.</span></span>
13. <span data-ttu-id="00344-211">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-211">Click Edit.</span></span>
14. <span data-ttu-id="00344-212">Ağaçta 'String\CONCATENATE' seçin.</span><span class="sxs-lookup"><span data-stu-id="00344-212">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="00344-213">Fonksiyon ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-213">Click Add function.</span></span>
16. <span data-ttu-id="00344-214">Ağaçta, 'Şirket' metnini genişletin.</span><span class="sxs-lookup"><span data-stu-id="00344-214">In the tree, expand 'Company'.</span></span>
17. <span data-ttu-id="00344-215">Ağaçta, 'Şirket\find()' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="00344-215">In the tree, expand 'Company\find()'.</span></span>
18. <span data-ttu-id="00344-216">Ağaçta, 'Şirket\find()\Ad' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="00344-216">In the tree, select 'Company\find()\Name'.</span></span>
19. <span data-ttu-id="00344-217">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-217">Click Add data source.</span></span>
20. <span data-ttu-id="00344-218">Formül alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="00344-218">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="00344-219">CONCATENATE(Company.'find()'.Name, ";",</span><span class="sxs-lookup"><span data-stu-id="00344-219">CONCATENATE(Company.'find()'.Name, ";",</span></span>  
21. <span data-ttu-id="00344-220">Ağaçta, 'Şirket\find()\Şirket(DataArea)' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="00344-220">In the tree, select 'Company\find()\Company(DataArea)'.</span></span>
22. <span data-ttu-id="00344-221">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-221">Click Add data source.</span></span>
23. <span data-ttu-id="00344-222">Formül alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="00344-222">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="00344-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span><span class="sxs-lookup"><span data-stu-id="00344-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span></span>  
24. <span data-ttu-id="00344-224">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-224">Click Save.</span></span>
25. <span data-ttu-id="00344-225">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="00344-225">Close the page.</span></span>
26. <span data-ttu-id="00344-226">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-226">Click Save.</span></span>
27. <span data-ttu-id="00344-227">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="00344-227">Close the page.</span></span>
28. <span data-ttu-id="00344-228">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="00344-228">Close the page.</span></span>
29. <span data-ttu-id="00344-229">Taslak Çalıştır alanında Evet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-229">Select Yes in the Run Draft field.</span></span>

## <a name="use-an-existing-er-model-mapping-configuration"></a><span data-ttu-id="00344-230">Mevcut bir ER model eşleme yapılandırmasının kullanma</span><span class="sxs-lookup"><span data-stu-id="00344-230">Use an existing ER model-mapping configuration</span></span>
1. <span data-ttu-id="00344-231">Ağaçta, 'Örnek veri modeli\Örnek biçim' seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="00344-231">In the tree, select 'Sample data model\Sample format'.</span></span>
2. <span data-ttu-id="00344-232">Çalıştır'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-232">Click Run.</span></span>
    * <span data-ttu-id="00344-233">Çalıştırılan ER biçiminin veri kaynağı olarak seçilen tanımsız veri modeli için birden fazla model eşleme yapılandırması mevcut olduğundan, ER biçimi yapılandırmasının seçili taslak sürümü yürütülemez.</span><span class="sxs-lookup"><span data-stu-id="00344-233">The selected draft version of the ER format configuration can't be executed because there is more than one model-mapping configuration available for the undefined data model that has been selected as the data source of the running ER format.</span></span>   
    * <span data-ttu-id="00344-234">Daha sonra, alternatif model eşleme yapılandırmasını, çalışan ER biçimi için veri kaynakları olarak kullanılacak model eşlemelerinden biri olarak tanımlayacaksınız.</span><span class="sxs-lookup"><span data-stu-id="00344-234">Next, you will define the alternative model-mapping configuration as the one from which model mappings will be used as data sources for running ER format.</span></span>   
3. <span data-ttu-id="00344-235">Ağaçta, 'Örnek veri modeli\Örnek eşleme (alternatif)' seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="00344-235">In the tree, select 'Sample data model\Sample mapping (alternative)'.</span></span>
4. <span data-ttu-id="00344-236">Model eşleme için varsayılan alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="00344-236">Select Yes in the Default for model-mapping field.</span></span>
5. <span data-ttu-id="00344-237">Ağaçta, 'Örnek veri modeli\Örnek biçim' seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="00344-237">In the tree, select 'Sample data model\Sample format'.</span></span>
6. <span data-ttu-id="00344-238">Çalıştır'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-238">Click Run.</span></span>
7. <span data-ttu-id="00344-239">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00344-239">Click OK.</span></span>
    * <span data-ttu-id="00344-240">Varsayılan model eşleme yapılandırması, bu biçim yapılandırması tarafından elektronik belge oluşturmak için kullanılır (oluşturulan çıktı şirket kodunu içerir).</span><span class="sxs-lookup"><span data-stu-id="00344-240">The default model-mapping configuration is used by this format configuration for generating the electronic document (the created output contains the company code).</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]