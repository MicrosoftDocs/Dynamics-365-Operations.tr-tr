---
title: Uygulama verileri içeren belgeler oluşturmak için modelleri ve eşlemeleri değiştirme
description: Bu konuda, elektronik belge oluşturmak ve uygulama verilerini güncelleştirmek için raporlama yapılandırmalarının nasıl tasarlanacağı açıklanmaktadır. (2. Bölüm - Belge oluşturma).
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 025429c8e6775d20634703853df04d63c0651b98
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092909"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a><span data-ttu-id="86bf5-104">Uygulama verileri içeren belgeler oluşturmak için modelleri ve eşlemeleri değiştirme</span><span class="sxs-lookup"><span data-stu-id="86bf5-104">Modify models and mappings to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="86bf5-105">Bu yordamdaki adımları tamamlamak için ilk önce "ER Uygulama veri güncelleştirmesi ile belgeler oluştur (Bölüm 2 - Belgeler oluştur)" yordamını tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="86bf5-105">To complete the steps in this procedure, you must first complete the procedure, "ER Generate documents with application data update (Part 2: Generate documents)".</span></span> 

<span data-ttu-id="86bf5-106">Bu yordamdaki adımlar bir Elektronik raporlama (ER) yapılandırmasının, bir elektronik belge oluşturmak ve uygulama verisini güncelleştirmek için nasıl kullanılacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="86bf5-106">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="86bf5-107">Bu yordamda, ER yapılandırmalarını elektronik belgeler oluşturmakta kullanmaya başlamak ve aynı zamanda uygulama verisini güncelleştirmek için de değiştirirsiniz.</span><span class="sxs-lookup"><span data-stu-id="86bf5-107">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="86bf5-108">Bu yordam, sistem yöneticisi veya elektronik raporlama geliştiricisi rolüne atanmış kullanıcılar için oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="86bf5-108">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="86bf5-109">Bu adımlar DEMF veri kümesi kullanılarak tamamlanabilir.</span><span class="sxs-lookup"><span data-stu-id="86bf5-109">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="86bf5-110">Veri modelini değiştir</span><span class="sxs-lookup"><span data-stu-id="86bf5-110">Modify data model</span></span>
1. <span data-ttu-id="86bf5-111">Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="86bf5-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="86bf5-112">Ağaçta, 'Intrastat (model)' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-112">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="86bf5-113">Veri modelini nasıl kullandığınızı genişleteceksiniz.</span><span class="sxs-lookup"><span data-stu-id="86bf5-113">You will extend how you use the data model.</span></span> <span data-ttu-id="86bf5-114">Intrastat raporunu oluşturmak için veri kaynağı olarak kullanmanın yanı sıra, veri modeli, Intrastat raporlama işleminin ayrıntılarını toplamak için kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="86bf5-114">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="86bf5-115">Ayrıntılar daha sonra uygulama verisini güncelleştirmek için kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="86bf5-115">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="86bf5-116">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-116">Click Designer.</span></span>
4. <span data-ttu-id="86bf5-117">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-117">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="86bf5-118">Yeni düğüm biçimi alanına "Model kökü" girin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-118">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="86bf5-119">İsim alanında 'Uygulama veri güncelleştirmesi için' yazın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-119">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="86bf5-120">Uygulama için veri güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="86bf5-120">For application data update</span></span>  
7. <span data-ttu-id="86bf5-121">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-121">Click Add.</span></span>
8. <span data-ttu-id="86bf5-122">Ağaçta, 'Uygulama veri güncelleştirmesi için' seçin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-122">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="86bf5-123">Bu yeni kök öğesi (veri kaynağı olarak kullanılan) Intrastat raporundan uygulama tablolalarına (güncelleştirme hedefi) hareket eden veri akışını belirtmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="86bf5-123">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="86bf5-124">Farklı kök öğelerinin, giden belgeye nakledilen veriyi almak ve uygulama verisini güncelleştirmek için belgeden veriyi almak için kullanılması gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-124">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="86bf5-125">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-125">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="86bf5-126">Ad alanına 'Arşiv başlığı' yazın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-126">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="86bf5-127">Arşiv başlığı</span><span class="sxs-lookup"><span data-stu-id="86bf5-127">Archive header</span></span>  
11. <span data-ttu-id="86bf5-128">Madde türü alanında 'Kayıt listesi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-128">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="86bf5-129">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-129">Click Add.</span></span>
    * <span data-ttu-id="86bf5-130">Oluşturulan her bir Intrastat raporu için bir kayıt oluşturacağınız için, önce bunun için bir madde oluşturmalısınız.</span><span class="sxs-lookup"><span data-stu-id="86bf5-130">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="86bf5-131">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-131">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="86bf5-132">Ad alanına "Dosya adı" yazın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-132">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="86bf5-133">Dosya adı</span><span class="sxs-lookup"><span data-stu-id="86bf5-133">File name</span></span>  
15. <span data-ttu-id="86bf5-134">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-134">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="86bf5-135">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-135">Click Add.</span></span>
17. <span data-ttu-id="86bf5-136">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-136">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="86bf5-137">İsim alanına 'Satır sayısı' yazın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-137">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="86bf5-138">Satır sayısı</span><span class="sxs-lookup"><span data-stu-id="86bf5-138">Number of lines</span></span>  
19. <span data-ttu-id="86bf5-139">Madde türü alanında 'Tamsayı' seçin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-139">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="86bf5-140">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-140">Click Add.</span></span>
    * <span data-ttu-id="86bf5-141">Geçerli raporlama işlemi sırasında raporlanan Intrastat hareketlerinin sayısını temsil etmek için bu öğeyi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-141">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="86bf5-142">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-142">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="86bf5-143">Ad alanına 'Arşiv satırları' yazın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-143">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="86bf5-144">Arşiv satırları</span><span class="sxs-lookup"><span data-stu-id="86bf5-144">Archive lines</span></span>  
23. <span data-ttu-id="86bf5-145">Madde türü alanında 'Kayıt listesi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-145">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="86bf5-146">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-146">Click Add.</span></span>
    * <span data-ttu-id="86bf5-147">Geçerli raporlama işlemi sırasında raporlanan Intrastat hareketlerinin listesini temsil etmek için bu öğeyi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-147">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="86bf5-148">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-148">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="86bf5-149">İsim alanına 'Tutar' yazın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-149">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="86bf5-150">Tutar</span><span class="sxs-lookup"><span data-stu-id="86bf5-150">Amount</span></span>  
27. <span data-ttu-id="86bf5-151">Madde türü alanında 'Gerçek' seçin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-151">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="86bf5-152">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-152">Click Add.</span></span>
29. <span data-ttu-id="86bf5-153">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-153">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="86bf5-154">İsim alanına 'Emtia rec id' yazın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-154">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="86bf5-155">Emtia rec id</span><span class="sxs-lookup"><span data-stu-id="86bf5-155">Commodity rec id</span></span>  
31. <span data-ttu-id="86bf5-156">Madde türü alanında 'Int64' seçin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-156">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="86bf5-157">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-157">Click Add.</span></span>
33. <span data-ttu-id="86bf5-158">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-158">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="86bf5-159">İsim alanına 'Madde numarası' yazın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-159">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="86bf5-160">Madde kodu</span><span class="sxs-lookup"><span data-stu-id="86bf5-160">Item number</span></span>  
35. <span data-ttu-id="86bf5-161">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-161">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="86bf5-162">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-162">Click Add.</span></span>
37. <span data-ttu-id="86bf5-163">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-163">Click Save.</span></span>
38. <span data-ttu-id="86bf5-164">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-164">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="86bf5-165">Model eşlemeyi değiştir</span><span class="sxs-lookup"><span data-stu-id="86bf5-165">Modify model mapping</span></span>
1. <span data-ttu-id="86bf5-166">Ağaçta, 'Intrastat (model)' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-166">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="86bf5-167">Ağaçta, 'Intrastat (model)\Intrastat (eşleme)' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-167">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="86bf5-168">Mevcut model eşlemesini uygulama veri güncelleştirmesine başlamak ve Intrastat raporlama ayrıntılarını arşivlemek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-168">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="86bf5-169">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-169">Click Designer.</span></span>
4. <span data-ttu-id="86bf5-170">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-170">Click New.</span></span>
5. <span data-ttu-id="86bf5-171">Ad alanına 'Arşivi güncelleştir' yazın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-171">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="86bf5-172">Arşivi güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="86bf5-172">Update archive</span></span>  
6. <span data-ttu-id="86bf5-173">Yön alanında 'Hedefe'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-173">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="86bf5-174">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-174">Click Save.</span></span>
    * <span data-ttu-id="86bf5-175">Bu yeni eşleme, veri modelinden uygulama tablolarına (güncelleştirme hedefi) hareket eden veri (Intrastat raporlama ayrıntıları) için veri akışını belirtir.</span><span class="sxs-lookup"><span data-stu-id="86bf5-175">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="86bf5-176">Farklı modellerin kök öğelerinin, raporlama işlemi için uygulamadan veri almak için kullanılması gerektiğini unutmayın ve daha sonra veri modelinden gelen veriyi uygulama veri güncelleştirmesi için kullanın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-176">Note that different model's root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="86bf5-177">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-177">Click Designer.</span></span>
9. <span data-ttu-id="86bf5-178">Ağaçta, 'Veri modeli\Veri modeli' seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-178">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="86bf5-179">Gerekli veri kaynağını ekle.</span><span class="sxs-lookup"><span data-stu-id="86bf5-179">Add the required data source.</span></span> <span data-ttu-id="86bf5-180">Bu, raporlanan ve arşivlenmesi gereken Intrastat hareketlerinin ayrıntılarını içeren veri modelidir.</span><span class="sxs-lookup"><span data-stu-id="86bf5-180">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="86bf5-181">Kök ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-181">Click Add root.</span></span>
11. <span data-ttu-id="86bf5-182">Ad alanında 'model' yazın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-182">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="86bf5-183">model</span><span class="sxs-lookup"><span data-stu-id="86bf5-183">model</span></span>  
12. <span data-ttu-id="86bf5-184">Tanım alanında, 'Uygulama veri güncelleştirmesi' değerini girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-184">In the Definition field, enter or select the value 'For application data update'.</span></span>
    * <span data-ttu-id="86bf5-185">Uygulama için veri güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="86bf5-185">For application data update</span></span>  
13. <span data-ttu-id="86bf5-186">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-186">Click OK.</span></span>
14. <span data-ttu-id="86bf5-187">Ağaçta, 'model'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-187">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="86bf5-188">Ağaçta, 'Functions\Calculated field' seçin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-188">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="86bf5-189">Ağaçta 'model\Arşiv başlığı'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-189">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="86bf5-190">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-190">Click Add.</span></span>
    * <span data-ttu-id="86bf5-191">Arşivleme için raporlanan Intrastat hareketlerini numaralandırmak istediğiniz için uygun veri kaynağının eklenmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="86bf5-191">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="86bf5-192">İsim alanına 'Numaralandırılan satırlar' yazın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-192">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="86bf5-193">Numaralandırılmış satırlar</span><span class="sxs-lookup"><span data-stu-id="86bf5-193">Enumerated lines</span></span>  
19. <span data-ttu-id="86bf5-194">Formülü düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-194">Click Edit formula.</span></span>
20. <span data-ttu-id="86bf5-195">Ağaçta 'Liste\ENUMARATE'i seçin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-195">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="86bf5-196">Fonksiyon ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-196">Click Add function.</span></span>
22. <span data-ttu-id="86bf5-197">Ağaçta, 'model'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-197">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="86bf5-198">Ağaçta 'model\Arşiv başlığı'nı genişletin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-198">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="86bf5-199">Ağaçta 'model\Arşiv başlığı\Arşiv satırları'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-199">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="86bf5-200">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-200">Click Add data source.</span></span>
26. <span data-ttu-id="86bf5-201">Formül alnında, 'ENUMERATE(model.'Arşiv başlığı'.'Arşiv satırları')' girin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-201">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="86bf5-202">ENUMERATE(model.'Arşiv başlığı'.'Arşiv satırları')</span><span class="sxs-lookup"><span data-stu-id="86bf5-202">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="86bf5-203">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-203">Click Save.</span></span>
28. <span data-ttu-id="86bf5-204">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-204">Close the page.</span></span>
29. <span data-ttu-id="86bf5-205">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-205">Click OK.</span></span>
30. <span data-ttu-id="86bf5-206">Hedef ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-206">Click Add destination.</span></span>
    * <span data-ttu-id="86bf5-207">Uygulama tablolarını, raporlanan Intrastat hareketlerinin ayrıntılarını arşivlemek için gerek duyulan hedefler olarak ekle.</span><span class="sxs-lookup"><span data-stu-id="86bf5-207">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="86bf5-208">Ad alanında, 'Arşiv' yazın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-208">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="86bf5-209">Arşivle</span><span class="sxs-lookup"><span data-stu-id="86bf5-209">Archive</span></span>  
32. <span data-ttu-id="86bf5-210">Tablo adı alanında, 'IntrastatArchiveGeneral' yazın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-210">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="86bf5-211">IntrastatArchiveGeneral</span><span class="sxs-lookup"><span data-stu-id="86bf5-211">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="86bf5-212">Kayıt eylemini 'Ekle' olarak tutun, böylece her bir Intrastat raporlama işlemi sırasında kayıtlar ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="86bf5-212">Keep the record action 'Insert' so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="86bf5-213">infolog kaydet alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-213">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="86bf5-214">Uygulama eri güncelleştirmesi sorunları hakkında bilgi almak için Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-214">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="86bf5-215">Kaydı atlama eylemi doğrulama alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-215">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="86bf5-216">Boş 'Intrastat arşiv kodu' alanı hakkında doğrulama hatalarını kaldırmak için Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-216">Select Yes to suppress validation errors about the empty 'Intrastat archive ID' field.</span></span> <span data-ttu-id="86bf5-217">Bu, kayıtlar eklendikten sonra yapılacaktır, Dış ticaret parametreler formunda bu tablo için yapılandırılmış sıra numarası ayarlarına dayalı olarak.</span><span class="sxs-lookup"><span data-stu-id="86bf5-217">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="86bf5-218">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-218">Click OK.</span></span>
    * <span data-ttu-id="86bf5-219">Eklenen veri kaynağının (seçilen kök öğesine dayalı filtrelenen model) öğelerini, eklenen hedeften öğelerle bağlayın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-219">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="86bf5-220">Ağaçta, 'Arşiv' metnini genişletin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-220">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="86bf5-221">Ağaçta 'Arşiv\<İlişkiler'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-221">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="86bf5-222">Ağaçta 'Arşiv\<İlişkiler\IntrastatArchiveDetail'ı genişletin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-222">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="86bf5-223">Ağaçta 'Arşiv\<İlişkiler\IntrastatArchiveDetail\Amount(AmountMST)'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-223">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="86bf5-224">Ağaçta 'model\Arşiv başlığı\Numaralandırılmış satırlar'ı genişletin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-224">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="86bf5-225">Ağaçta 'model\Arşiv başlığı\Numaralandırılmış satırlar\Değer'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-225">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="86bf5-226">Ağaçta 'model\Arşiv başlığı\Numaralandırılmış satırlar\Değer\Tutar'ı genişletin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-226">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="86bf5-227">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-227">Click Bind.</span></span>
44. <span data-ttu-id="86bf5-228">Ağaçta 'Arşiv\<İlişkiler\IntrastatArchiveDetail\Commodity(IntrastatCommodity)' seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-228">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="86bf5-229">Ağaçta 'model\Arşiv başlığı\Numaralandırılmış satırlar\Değer\Emtia rec id'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-229">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="86bf5-230">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-230">Click Bind.</span></span>
47. <span data-ttu-id="86bf5-231">Ağaçta 'Arşiv\<İlişkiler\IntrastatArchiveDetail\Madde numarası(ItemId)'i seçin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-231">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="86bf5-232">Ağaçta 'model\Arşiv başlığı\Numaralandırılmış satırlar\Değer\Madde numarası'nı genişletin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-232">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="86bf5-233">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-233">Click Bind.</span></span>
50. <span data-ttu-id="86bf5-234">Ağaçta 'Arşiv\<İlişkiler\IntrastatArchiveDetail\Satır numarası(LineNumber)'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-234">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="86bf5-235">Ağaçta 'model\Arşiv başlığı\Numaralandırılmış satırlar\Numara'yı genişletin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-235">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="86bf5-236">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-236">Click Bind.</span></span>
53. <span data-ttu-id="86bf5-237">Ağaçta 'Arşiv\<İlişkiler\IntrastatArchiveDetail'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-237">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="86bf5-238">Ağaçta 'model\Arşiv başlığı\Numaralandırılmış satırlar'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-238">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="86bf5-239">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-239">Click Bind.</span></span>
56. <span data-ttu-id="86bf5-240">Ağaçta 'Arşiv\Dosya adı(FileName)'i seçin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-240">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="86bf5-241">Ağaçta 'model\Arşiv başlığı\Dosya adı'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-241">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="86bf5-242">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-242">Click Bind.</span></span>
59. <span data-ttu-id="86bf5-243">Ağaçta 'Arşiv\Satır sayısı(NumberOfLines)'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-243">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="86bf5-244">Ağaçta 'model\Arşiv başlığı\Satır sayısı'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-244">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="86bf5-245">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-245">Click Bind.</span></span>
62. <span data-ttu-id="86bf5-246">Ağaçta, 'Arşiv'i seçin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-246">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="86bf5-247">Ağaçta 'model\Arşiv başlığı'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="86bf5-247">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="86bf5-248">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-248">Click Bind.</span></span>
65. <span data-ttu-id="86bf5-249">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-249">Click Save.</span></span>
66. <span data-ttu-id="86bf5-250">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-250">Close the page.</span></span>
67. <span data-ttu-id="86bf5-251">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="86bf5-251">Close the page.</span></span>

