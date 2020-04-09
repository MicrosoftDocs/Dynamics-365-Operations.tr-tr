---
title: Uygulama verileri içeren belgeler oluşturmak için modelleri ve eşlemeleri değiştirme
description: Bu yordamdaki adımları tamamlamak için ilk önce "ER Uygulama veri güncelleştirmesi ile belgeler oluştur (Bölüm 2 - Belgeler oluştur)" yordamını tamamlamalısınız.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4546de2c5c1773aadce0ec084ee7058ff2ae153
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141891"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a><span data-ttu-id="6d72a-103">Uygulama verileri içeren belgeler oluşturmak için modelleri ve eşlemeleri değiştirme</span><span class="sxs-lookup"><span data-stu-id="6d72a-103">Modify models and mappings to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6d72a-104">Bu yordamdaki adımları tamamlamak için ilk önce "ER Uygulama veri güncelleştirmesi ile belgeler oluştur (Bölüm 2 - Belgeler oluştur)" yordamını tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="6d72a-104">To complete the steps in this procedure, you must first complete the procedure, "ER Generate documents with application data update (Part 2: Generate documents)".</span></span> 

<span data-ttu-id="6d72a-105">Bu yordamdaki adımlar bir Elektronik raporlama (ER) yapılandırmasının, bir elektronik belge oluşturmak ve uygulama verisini güncelleştirmek için nasıl kullanılacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="6d72a-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="6d72a-106">Bu yordamda, ER yapılandırmalarını elektronik belgeler oluşturmakta kullanmaya başlamak ve aynı zamanda uygulama verisini güncelleştirmek için de değiştirirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6d72a-106">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="6d72a-107">Bu yordam, sistem yöneticisi veya elektronik raporlama geliştiricisi rolüne atanmış kullanıcılar için oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="6d72a-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="6d72a-108">Bu adımlar DEMF veri kümesi kullanılarak tamamlanabilir.</span><span class="sxs-lookup"><span data-stu-id="6d72a-108">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="6d72a-109">Veri modelini değiştir</span><span class="sxs-lookup"><span data-stu-id="6d72a-109">Modify data model</span></span>
1. <span data-ttu-id="6d72a-110">Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="6d72a-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="6d72a-111">Ağaçta, 'Intrastat (model)' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-111">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="6d72a-112">Veri modelini nasıl kullandığınızı genişleteceksiniz.</span><span class="sxs-lookup"><span data-stu-id="6d72a-112">You will extend how you use the data model.</span></span> <span data-ttu-id="6d72a-113">Intrastat raporunu oluşturmak için veri kaynağı olarak kullanmanın yanı sıra, veri modeli, Intrastat raporlama işleminin ayrıntılarını toplamak için kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="6d72a-113">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="6d72a-114">Ayrıntılar daha sonra uygulama verisini güncelleştirmek için kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="6d72a-114">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="6d72a-115">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-115">Click Designer.</span></span>
4. <span data-ttu-id="6d72a-116">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-116">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="6d72a-117">Yeni düğüm biçimi alanına "Model kökü" girin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-117">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="6d72a-118">İsim alanında 'Uygulama veri güncelleştirmesi için' yazın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-118">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="6d72a-119">Uygulama için veri güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="6d72a-119">For application data update</span></span>  
7. <span data-ttu-id="6d72a-120">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-120">Click Add.</span></span>
8. <span data-ttu-id="6d72a-121">Ağaçta, 'Uygulama veri güncelleştirmesi için' seçin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-121">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="6d72a-122">Bu yeni kök öğesi (veri kaynağı olarak kullanılan) Intrastat raporundan uygulama tablolalarına (güncelleştirme hedefi) hareket eden veri akışını belirtmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6d72a-122">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="6d72a-123">Farklı kök öğelerinin, giden belgeye nakledilen veriyi almak ve uygulama verisini güncelleştirmek için belgeden veriyi almak için kullanılması gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-123">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="6d72a-124">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="6d72a-125">Ad alanına 'Arşiv başlığı' yazın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-125">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="6d72a-126">Arşiv başlığı</span><span class="sxs-lookup"><span data-stu-id="6d72a-126">Archive header</span></span>  
11. <span data-ttu-id="6d72a-127">Madde türü alanında 'Kayıt listesi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-127">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="6d72a-128">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-128">Click Add.</span></span>
    * <span data-ttu-id="6d72a-129">Oluşturulan her bir Intrastat raporu için bir kayıt oluşturacağınız için, önce bunun için bir madde oluşturmalısınız.</span><span class="sxs-lookup"><span data-stu-id="6d72a-129">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="6d72a-130">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-130">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="6d72a-131">Ad alanına "Dosya adı" yazın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-131">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="6d72a-132">Dosya adı</span><span class="sxs-lookup"><span data-stu-id="6d72a-132">File name</span></span>  
15. <span data-ttu-id="6d72a-133">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-133">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="6d72a-134">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-134">Click Add.</span></span>
17. <span data-ttu-id="6d72a-135">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-135">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="6d72a-136">İsim alanına 'Satır sayısı' yazın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-136">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="6d72a-137">Satır sayısı</span><span class="sxs-lookup"><span data-stu-id="6d72a-137">Number of lines</span></span>  
19. <span data-ttu-id="6d72a-138">Madde türü alanında 'Tamsayı' seçin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-138">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="6d72a-139">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-139">Click Add.</span></span>
    * <span data-ttu-id="6d72a-140">Geçerli raporlama işlemi sırasında raporlanan Intrastat hareketlerinin sayısını temsil etmek için bu öğeyi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-140">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="6d72a-141">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-141">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="6d72a-142">Ad alanına 'Arşiv satırları' yazın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-142">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="6d72a-143">Arşiv satırları</span><span class="sxs-lookup"><span data-stu-id="6d72a-143">Archive lines</span></span>  
23. <span data-ttu-id="6d72a-144">Madde türü alanında 'Kayıt listesi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-144">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="6d72a-145">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-145">Click Add.</span></span>
    * <span data-ttu-id="6d72a-146">Geçerli raporlama işlemi sırasında raporlanan Intrastat hareketlerinin listesini temsil etmek için bu öğeyi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-146">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="6d72a-147">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-147">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="6d72a-148">İsim alanına 'Tutar' yazın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-148">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="6d72a-149">Tutar</span><span class="sxs-lookup"><span data-stu-id="6d72a-149">Amount</span></span>  
27. <span data-ttu-id="6d72a-150">Madde türü alanında 'Gerçek' seçin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-150">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="6d72a-151">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-151">Click Add.</span></span>
29. <span data-ttu-id="6d72a-152">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-152">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="6d72a-153">İsim alanına 'Emtia rec id' yazın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-153">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="6d72a-154">Emtia rec id</span><span class="sxs-lookup"><span data-stu-id="6d72a-154">Commodity rec id</span></span>  
31. <span data-ttu-id="6d72a-155">Madde türü alanında 'Int64' seçin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-155">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="6d72a-156">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-156">Click Add.</span></span>
33. <span data-ttu-id="6d72a-157">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-157">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="6d72a-158">İsim alanına 'Madde numarası' yazın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-158">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="6d72a-159">Madde kodu</span><span class="sxs-lookup"><span data-stu-id="6d72a-159">Item number</span></span>  
35. <span data-ttu-id="6d72a-160">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-160">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="6d72a-161">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-161">Click Add.</span></span>
37. <span data-ttu-id="6d72a-162">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-162">Click Save.</span></span>
38. <span data-ttu-id="6d72a-163">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-163">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="6d72a-164">Model eşlemeyi değiştir</span><span class="sxs-lookup"><span data-stu-id="6d72a-164">Modify model mapping</span></span>
1. <span data-ttu-id="6d72a-165">Ağaçta, 'Intrastat (model)' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-165">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="6d72a-166">Ağaçta, 'Intrastat (model)\Intrastat (eşleme)' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-166">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="6d72a-167">Mevcut model eşlemesini uygulama veri güncelleştirmesine başlamak ve Intrastat raporlama ayrıntılarını arşivlemek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-167">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="6d72a-168">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-168">Click Designer.</span></span>
4. <span data-ttu-id="6d72a-169">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-169">Click New.</span></span>
5. <span data-ttu-id="6d72a-170">Ad alanına 'Arşivi güncelleştir' yazın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-170">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="6d72a-171">Arşivi güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="6d72a-171">Update archive</span></span>  
6. <span data-ttu-id="6d72a-172">Yön alanında 'Hedefe'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-172">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="6d72a-173">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-173">Click Save.</span></span>
    * <span data-ttu-id="6d72a-174">Bu yeni eşleme, veri modelinden uygulama tablolarına (güncelleştirme hedefi) hareket eden veri (Intrastat raporlama ayrıntıları) için veri akışını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d72a-174">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="6d72a-175">Farklı modellerin kök öğelerinin, raporlama işlemi için uygulamadan veri almak için kullanılması gerektiğini unutmayın ve daha sonra veri modelinden gelen veriyi uygulama veri güncelleştirmesi için kullanın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-175">Note that different model's root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="6d72a-176">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-176">Click Designer.</span></span>
9. <span data-ttu-id="6d72a-177">Ağaçta, 'Veri modeli\Veri modeli' seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-177">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="6d72a-178">Gerekli veri kaynağını ekle.</span><span class="sxs-lookup"><span data-stu-id="6d72a-178">Add the required data source.</span></span> <span data-ttu-id="6d72a-179">Bu, raporlanan ve arşivlenmesi gereken Intrastat hareketlerinin ayrıntılarını içeren veri modelidir.</span><span class="sxs-lookup"><span data-stu-id="6d72a-179">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="6d72a-180">Kök ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-180">Click Add root.</span></span>
11. <span data-ttu-id="6d72a-181">Ad alanında 'model' yazın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-181">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="6d72a-182">model</span><span class="sxs-lookup"><span data-stu-id="6d72a-182">model</span></span>  
12. <span data-ttu-id="6d72a-183">Tanım alanında, 'Uygulama veri güncelleştirmesi' değerini girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-183">In the Definition field, enter or select the value 'For application data update'.</span></span>
    * <span data-ttu-id="6d72a-184">Uygulama için veri güncelleştirmesi</span><span class="sxs-lookup"><span data-stu-id="6d72a-184">For application data update</span></span>  
13. <span data-ttu-id="6d72a-185">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-185">Click OK.</span></span>
14. <span data-ttu-id="6d72a-186">Ağaçta, 'model'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-186">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="6d72a-187">Ağaçta, 'Functions\Calculated field' seçin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-187">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="6d72a-188">Ağaçta 'model\Arşiv başlığı'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-188">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="6d72a-189">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-189">Click Add.</span></span>
    * <span data-ttu-id="6d72a-190">Arşivleme için raporlanan Intrastat hareketlerini numaralandırmak istediğiniz için uygun veri kaynağının eklenmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="6d72a-190">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="6d72a-191">İsim alanına 'Numaralandırılan satırlar' yazın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-191">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="6d72a-192">Numaralandırılmış satırlar</span><span class="sxs-lookup"><span data-stu-id="6d72a-192">Enumerated lines</span></span>  
19. <span data-ttu-id="6d72a-193">Formülü düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-193">Click Edit formula.</span></span>
20. <span data-ttu-id="6d72a-194">Ağaçta 'Liste\ENUMARATE'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-194">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="6d72a-195">Fonksiyon ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-195">Click Add function.</span></span>
22. <span data-ttu-id="6d72a-196">Ağaçta, 'model'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-196">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="6d72a-197">Ağaçta 'model\Arşiv başlığı'nı genişletin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-197">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="6d72a-198">Ağaçta 'model\Arşiv başlığı\Arşiv satırları'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-198">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="6d72a-199">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-199">Click Add data source.</span></span>
26. <span data-ttu-id="6d72a-200">Formül alnında, 'ENUMERATE(model.'Arşiv başlığı'.'Arşiv satırları')' girin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-200">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="6d72a-201">ENUMERATE(model.'Arşiv başlığı'.'Arşiv satırları')</span><span class="sxs-lookup"><span data-stu-id="6d72a-201">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="6d72a-202">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-202">Click Save.</span></span>
28. <span data-ttu-id="6d72a-203">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-203">Close the page.</span></span>
29. <span data-ttu-id="6d72a-204">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-204">Click OK.</span></span>
30. <span data-ttu-id="6d72a-205">Hedef ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-205">Click Add destination.</span></span>
    * <span data-ttu-id="6d72a-206">Uygulama tablolarını, raporlanan Intrastat hareketlerinin ayrıntılarını arşivlemek için gerek duyulan hedefler olarak ekle.</span><span class="sxs-lookup"><span data-stu-id="6d72a-206">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="6d72a-207">Ad alanında, 'Arşiv' yazın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-207">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="6d72a-208">Arşivle</span><span class="sxs-lookup"><span data-stu-id="6d72a-208">Archive</span></span>  
32. <span data-ttu-id="6d72a-209">Tablo adı alanında, 'IntrastatArchiveGeneral' yazın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-209">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="6d72a-210">IntrastatArchiveGeneral</span><span class="sxs-lookup"><span data-stu-id="6d72a-210">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="6d72a-211">Kayıt eylemini 'Ekle' olarak tutun, böylece her bir Intrastat raporlama işlemi sırasında kayıtlar ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6d72a-211">Keep the record action 'Insert' so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="6d72a-212">infolog kaydet alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-212">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="6d72a-213">Uygulama eri güncelleştirmesi sorunları hakkında bilgi almak için Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-213">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="6d72a-214">Kaydı atlama eylemi doğrulama alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-214">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="6d72a-215">Boş 'Intrastat arşiv kodu' alanı hakkında doğrulama hatalarını kaldırmak için Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-215">Select Yes to suppress validation errors about the empty 'Intrastat archive ID' field.</span></span> <span data-ttu-id="6d72a-216">Bu, kayıtlar eklendikten sonra yapılacaktır, Dış ticaret parametreler formunda bu tablo için yapılandırılmış sıra numarası ayarlarına dayalı olarak.</span><span class="sxs-lookup"><span data-stu-id="6d72a-216">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="6d72a-217">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-217">Click OK.</span></span>
    * <span data-ttu-id="6d72a-218">Eklenen veri kaynağının (seçilen kök öğesine dayalı filtrelenen model) öğelerini, eklenen hedeften öğelerle bağlayın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-218">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="6d72a-219">Ağaçta, 'Arşiv' metnini genişletin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-219">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="6d72a-220">Ağaçta 'Arşiv\<İlişkiler'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-220">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="6d72a-221">Ağaçta 'Arşiv\<İlişkiler\IntrastatArchiveDetail'ı genişletin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-221">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="6d72a-222">Ağaçta 'Arşiv\<İlişkiler\IntrastatArchiveDetail\Amount(AmountMST)'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-222">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="6d72a-223">Ağaçta 'model\Arşiv başlığı\Numaralandırılmış satırlar'ı genişletin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-223">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="6d72a-224">Ağaçta 'model\Arşiv başlığı\Numaralandırılmış satırlar\Değer'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-224">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="6d72a-225">Ağaçta 'model\Arşiv başlığı\Numaralandırılmış satırlar\Değer\Tutar'ı genişletin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-225">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="6d72a-226">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-226">Click Bind.</span></span>
44. <span data-ttu-id="6d72a-227">Ağaçta 'Arşiv\<İlişkiler\IntrastatArchiveDetail\Commodity(IntrastatCommodity)' seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-227">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="6d72a-228">Ağaçta 'model\Arşiv başlığı\Numaralandırılmış satırlar\Değer\Emtia rec id'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-228">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="6d72a-229">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-229">Click Bind.</span></span>
47. <span data-ttu-id="6d72a-230">Ağaçta 'Arşiv\<İlişkiler\IntrastatArchiveDetail\Madde numarası(ItemId)'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-230">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="6d72a-231">Ağaçta 'model\Arşiv başlığı\Numaralandırılmış satırlar\Değer\Madde numarası'nı genişletin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-231">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="6d72a-232">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-232">Click Bind.</span></span>
50. <span data-ttu-id="6d72a-233">Ağaçta 'Arşiv\<İlişkiler\IntrastatArchiveDetail\Satır numarası(LineNumber)'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-233">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="6d72a-234">Ağaçta 'model\Arşiv başlığı\Numaralandırılmış satırlar\Numara'yı genişletin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-234">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="6d72a-235">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-235">Click Bind.</span></span>
53. <span data-ttu-id="6d72a-236">Ağaçta 'Arşiv\<İlişkiler\IntrastatArchiveDetail'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-236">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="6d72a-237">Ağaçta 'model\Arşiv başlığı\Numaralandırılmış satırlar'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-237">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="6d72a-238">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-238">Click Bind.</span></span>
56. <span data-ttu-id="6d72a-239">Ağaçta 'Arşiv\Dosya adı(FileName)'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-239">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="6d72a-240">Ağaçta 'model\Arşiv başlığı\Dosya adı'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-240">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="6d72a-241">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-241">Click Bind.</span></span>
59. <span data-ttu-id="6d72a-242">Ağaçta 'Arşiv\Satır sayısı(NumberOfLines)'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-242">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="6d72a-243">Ağaçta 'model\Arşiv başlığı\Satır sayısı'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-243">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="6d72a-244">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-244">Click Bind.</span></span>
62. <span data-ttu-id="6d72a-245">Ağaçta, 'Arşiv'i seçin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-245">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="6d72a-246">Ağaçta 'model\Arşiv başlığı'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="6d72a-246">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="6d72a-247">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-247">Click Bind.</span></span>
65. <span data-ttu-id="6d72a-248">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-248">Click Save.</span></span>
66. <span data-ttu-id="6d72a-249">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-249">Close the page.</span></span>
67. <span data-ttu-id="6d72a-250">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6d72a-250">Close the page.</span></span>

