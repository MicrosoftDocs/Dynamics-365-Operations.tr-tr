--- 
title: "Elektronik raporlama (ER) için katıştırılmış resimlere sahip Microsoft Office biçimlerinde rapor oluşturma"
description: "Aşağıdaki adımlar 'Sistem yöneticisi' veya 'Elektronik raporlama geliştiricisi' rolündeki bir kullanıcının, MS office biçimlerinde (Excel ve Word) katıştırılmış resimler içeren elektronik belgeler oluşturmak için Elektronik raporlama (ER) yapılandırmalarını nasıl tasarlayabileceklerini açıklar."
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
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
ms.openlocfilehash: de2840ebc6c91e313546859f5c0d8939eb80977b
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="generate-reports-in-microsoft-office-formats-with-embedded-images-for-electronic-reporting-er"></a><span data-ttu-id="89fa5-103">Elektronik raporlama (ER) için katıştırılmış resimlere sahip Microsoft Office biçimlerinde rapor oluşturma</span><span class="sxs-lookup"><span data-stu-id="89fa5-103">Generate reports in Microsoft Office formats with embedded images for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="89fa5-104">Aşağıdaki adımlar 'Sistem yöneticisi' veya 'Elektronik raporlama geliştiricisi' rolündeki bir kullanıcının, MS office biçimlerinde (Excel ve Word) katıştırılmış resimler içeren elektronik belgeler oluşturmak için Elektronik raporlama (ER) yapılandırmalarını nasıl tasarlayabileceklerini açıklar.</span><span class="sxs-lookup"><span data-stu-id="89fa5-104">The following steps explain how a user playing either ‘System administrator’ or ‘Electronic reporting developer’ role can design Electronic reporting (ER) configurations to generate electronic documents in MS office formats (Excel and Word) containing embedded images.</span></span>

<span data-ttu-id="89fa5-105">Bu örnekte, 'Litware, Inc.' örnek şirketi için oluşturulmuş ER yapılandırmalarını kullanacaksınız.</span><span class="sxs-lookup"><span data-stu-id="89fa5-105">In this example, you will use created ER configurations for sample company, ‘Litware, Inc.’.</span></span>  <span data-ttu-id="89fa5-106">Bu adımları tamamlamak için öncelikle "ER Katıştırılmış resimler barındıran MS Office biçimlerinde raporlar hazırla (Bölüm 2: Yapılandırmaları gözden geçir)" görev kılavuzundaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-106">To complete these steps, you must first complete the steps in the “ER Make reports in MS Office formats with embedded images (Part 2: Review configurations)” task guide.</span></span> <span data-ttu-id="89fa5-107">Bu adımlar 'USMF' şirketinde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="89fa5-107">These steps can be performed in ‘USMF’ company.</span></span>


## <a name="run-format-with-initial-model-mapping"></a><span data-ttu-id="89fa5-108">Biçimi ilk model eşleme ile çalıştırın</span><span class="sxs-lookup"><span data-stu-id="89fa5-108">Run format with initial model mapping</span></span>
1. <span data-ttu-id="89fa5-109">Nakit ve banka yönetimi > Banka hesapları > Banka hesapları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="89fa5-109">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="89fa5-110">Banka hesabı alanında "USMF OPER" değeriyle filtre uygulamak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-110">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="89fa5-111">Eylem Bölmesinde Kurulum'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-111">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="89fa5-112">Denetle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-112">Click Check.</span></span>
5. <span data-ttu-id="89fa5-113">Testi yazdır'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-113">Click Print test.</span></span>
    * <span data-ttu-id="89fa5-114">Test amacıyla biçimi çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-114">Run the format for testing purposes.</span></span>  
6. <span data-ttu-id="89fa5-115">Ciro edilebilir çek biçimi alanında Evet'i işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="89fa5-115">Select Yes in the Negotiable check format field.</span></span>
7. <span data-ttu-id="89fa5-116">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-116">Click OK.</span></span>
    * <span data-ttu-id="89fa5-117">Oluşturulan sonucu inceleyin.</span><span class="sxs-lookup"><span data-stu-id="89fa5-117">Review the created output.</span></span> <span data-ttu-id="89fa5-118">Şirket logosunun hem raporda hem de kişinin imzasında görüleceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-118">Note that the company logo is presented in the report as well as the authorized person’s signature.</span></span> <span data-ttu-id="89fa5-119">İmza resmi seçilen banka hesabıyla ilişkilendirilmiş 'Konteyner' veri türünün çek düzeni alanından alınır.</span><span class="sxs-lookup"><span data-stu-id="89fa5-119">The signature image is taken from the field of the ‘Container’ data type of the cheque layout record which is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="89fa5-120">Kopyalar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="89fa5-120">Expand the Copies section.</span></span>
9. <span data-ttu-id="89fa5-121">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-121">Click Edit.</span></span>
10. <span data-ttu-id="89fa5-122">Filigran alanında 'Filigranı Geçersiz olarak yazdır' girin.</span><span class="sxs-lookup"><span data-stu-id="89fa5-122">In the Watermark field, enter 'Print watermark as Void'.</span></span>
    * <span data-ttu-id="89fa5-123">Bir Excel şekli öğesinde belge oluştururken filigranı göstermek için filigran biçim ayarını değiştirin.</span><span class="sxs-lookup"><span data-stu-id="89fa5-123">Change the watermark layout setting to show the watermark text in generating document in an Excel shape element.</span></span>  
11. <span data-ttu-id="89fa5-124">Testi yazdır'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-124">Click Print test.</span></span>
12. <span data-ttu-id="89fa5-125">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-125">Click OK.</span></span>
    * <span data-ttu-id="89fa5-126">Oluşturulan sonucu inceleyin.</span><span class="sxs-lookup"><span data-stu-id="89fa5-126">Review the created output.</span></span> <span data-ttu-id="89fa5-127">Filigranın oluşturulan raporda seçin seçeneğine uygun olarak gösterileceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-127">Note that the watermark is shown in the created report in accordance to the selection option.</span></span>  
13. <span data-ttu-id="89fa5-128">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-128">Close the page.</span></span>
14. <span data-ttu-id="89fa5-129">Eylem Bölmesinde, Ödemeleri yönet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-129">On the Action Pane, click Manage payments.</span></span>
15. <span data-ttu-id="89fa5-130">Çekler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-130">Click Checks.</span></span>
16. <span data-ttu-id="89fa5-131">Filtreleri göster'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-131">Click Show filters.</span></span>
17. <span data-ttu-id="89fa5-132">Aşağıdaki filtreleri uygulayın: "Çek numarası" alanında "şunlardan biri" filtre işlecini kullanarak "381", "385", "389" filtre değerini girin.</span><span class="sxs-lookup"><span data-stu-id="89fa5-132">Apply the following filters: Enter a filter value of "381","385","389" on the "Check number" field using the "is one of" filter operator.</span></span>
18. <span data-ttu-id="89fa5-133">Listede, tüm satırları işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="89fa5-133">In the list, mark all rows.</span></span>
19. <span data-ttu-id="89fa5-134">Çek kopyasını yazdır'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-134">Click Print check copy.</span></span>
    * <span data-ttu-id="89fa5-135">Seçilen çekleri yeniden yazdırmak için biçimi çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-135">Run the format to re-print the selected cheques.</span></span>  
    * <span data-ttu-id="89fa5-136">Oluşturulan sonucu inceleyin.</span><span class="sxs-lookup"><span data-stu-id="89fa5-136">Review the created output.</span></span> <span data-ttu-id="89fa5-137">Seçilen çeklerin yeniden yazdırıldığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-137">Note that the selected cheques have been re-printed.</span></span> <span data-ttu-id="89fa5-138">Şirket logosu ve etiketleri yazdırılmaz çünkü önceden yazdırılmış formda mevcutturlar.</span><span class="sxs-lookup"><span data-stu-id="89fa5-138">The company logo and labels are not printed out since they are presented on the pre-printed form.</span></span>  

## <a name="modify-the-mapping-of-the-imported-data-model"></a><span data-ttu-id="89fa5-139">İçe aktarılan veri modelinin eşlemesini değiştirin</span><span class="sxs-lookup"><span data-stu-id="89fa5-139">Modify the mapping of the imported data model</span></span>
1. <span data-ttu-id="89fa5-140">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-140">Close the page.</span></span>
2. <span data-ttu-id="89fa5-141">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-141">Close the page.</span></span>
3. <span data-ttu-id="89fa5-142">Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="89fa5-142">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="89fa5-143">Ağaçta, 'Çekler için model' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="89fa5-143">In the tree, select 'Model for cheques'.</span></span>
5. <span data-ttu-id="89fa5-144">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-144">Click Designer.</span></span>
6. <span data-ttu-id="89fa5-145">Modeli veri kaynağına eşle'yi tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-145">Click Map model to datasource.</span></span>
7. <span data-ttu-id="89fa5-146">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-146">Click Designer.</span></span>
    * <span data-ttu-id="89fa5-147">Seçilen banka hesabıyla ilişkilendirilmiş çek biçim kaydına eklenmiş olan dosyadan imza resmi almak için veri modelinin imza öğesini değiştireceğiz.</span><span class="sxs-lookup"><span data-stu-id="89fa5-147">We will change the binding of the data model’s signature item to get the signature image from the file that has been attached to the cheque layout record which is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="89fa5-148">Ayrıntıları göster'i kapatın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-148">Turn Show details off.</span></span>
9. <span data-ttu-id="89fa5-149">Ağaçta, 'düzen' metnini genişletin.</span><span class="sxs-lookup"><span data-stu-id="89fa5-149">In the tree, expand 'layout'.</span></span>
10. <span data-ttu-id="89fa5-150">Ağaçta, 'düzen\imza' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="89fa5-150">In the tree, expand 'layout\signature'.</span></span>
11. <span data-ttu-id="89fa5-151">Ağaçta 'düzen\imza\resim = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp' seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="89fa5-151">In the tree, select 'layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp'.</span></span>
12. <span data-ttu-id="89fa5-152">Ağaçta, 'chequesaccount' öğesini genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-152">In the tree, expand 'chequesaccount'.</span></span>
13. <span data-ttu-id="89fa5-153">Ağaç altından 'chequesaccount\<İlişkiler' seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="89fa5-153">In the tree, expand 'chequesaccount\<Relations'.</span></span>
14. <span data-ttu-id="89fa5-154">Ağaçta 'chequesaccount\<İlişkiler\BankChequeLayout' seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="89fa5-154">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout'.</span></span>
15. <span data-ttu-id="89fa5-155">Ağaçta 'chequesaccount\<İlişkiler\BankChequeLayout\<İlişkiler' seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="89fa5-155">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations'.</span></span>
16. <span data-ttu-id="89fa5-156">Ağaçta 'chequesaccount\<İlişkiler\BankChequeLayout\<İlişkiler\<Belgeler' seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="89fa5-156">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents'.</span></span>
17. <span data-ttu-id="89fa5-157">Ağaçta 'chequesaccount\<İlişkiler\BankChequeLayout\<İlişkiler\Belgeler\<getFileContentAsContainer()' seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="89fa5-157">In the tree, select 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer()'.</span></span>
18. <span data-ttu-id="89fa5-158">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-158">Click Bind.</span></span>
19. <span data-ttu-id="89fa5-159">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-159">Click Save.</span></span>
20. <span data-ttu-id="89fa5-160">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-160">Close the page.</span></span>
21. <span data-ttu-id="89fa5-161">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-161">Close the page.</span></span>
22. <span data-ttu-id="89fa5-162">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-162">Close the page.</span></span>
23. <span data-ttu-id="89fa5-163">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-163">Close the page.</span></span>

## <a name="run-format-using-the-adjusted-model-mapping"></a><span data-ttu-id="89fa5-164">Ayarlanan model eşlemesini kullanarak biçimi çalıştırın</span><span class="sxs-lookup"><span data-stu-id="89fa5-164">Run format using the adjusted model mapping</span></span>
1. <span data-ttu-id="89fa5-165">Nakit ve banka yönetimi > Banka hesapları > Banka hesapları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="89fa5-165">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="89fa5-166">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-166">Use the Quick Filter to find records.</span></span> <span data-ttu-id="89fa5-167">Örneğin, Banka hesabı alanında 'USMF OPER' değerini girerek filtreleme yapın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-167">For example, filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="89fa5-168">Eylem Bölmesinde Kurulum'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-168">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="89fa5-169">Denetle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-169">Click Check.</span></span>
5. <span data-ttu-id="89fa5-170">Testi yazdır'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-170">Click Print test.</span></span>
6. <span data-ttu-id="89fa5-171">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-171">Click OK.</span></span>
    * <span data-ttu-id="89fa5-172">Oluşturulan sonucu inceleyin.</span><span class="sxs-lookup"><span data-stu-id="89fa5-172">Review the created output.</span></span> <span data-ttu-id="89fa5-173">Belge yönetim ekinin, yetkili bir kişinin imzası olarak gösterileceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-173">Note that the image from the Document Management attachment is presented as the signature of an authorized person.</span></span>  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a><span data-ttu-id="89fa5-174">MS Word belgesini içe aktarılan biçimde bir şablon olarak kullanın</span><span class="sxs-lookup"><span data-stu-id="89fa5-174">Use MS Word document as a template in the imported format</span></span>
1. <span data-ttu-id="89fa5-175">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-175">Close the page.</span></span>
2. <span data-ttu-id="89fa5-176">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-176">Close the page.</span></span>
3. <span data-ttu-id="89fa5-177">Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="89fa5-177">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="89fa5-178">Ağaçta, 'Çekler için model' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="89fa5-178">In the tree, expand 'Model for cheques'.</span></span>
5. <span data-ttu-id="89fa5-179">Ağaçta 'Çekler için model\Çek yazdırma biçimi' seçin.</span><span class="sxs-lookup"><span data-stu-id="89fa5-179">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
6. <span data-ttu-id="89fa5-180">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-180">Click Designer.</span></span>
7. <span data-ttu-id="89fa5-181">Ekler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-181">Click Attachments.</span></span>
8. <span data-ttu-id="89fa5-182">Sil'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-182">Click Delete.</span></span>
9. <span data-ttu-id="89fa5-183">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-183">Click Yes.</span></span>
10. <span data-ttu-id="89fa5-184">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-184">Click New.</span></span>
11. <span data-ttu-id="89fa5-185">Dosya'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-185">Click File.</span></span>
    * <span data-ttu-id="89fa5-186">Gözat'ı tıklatın ve önceden indirilen 'Çek şablonu Word.docx' dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="89fa5-186">Click Browse and select the downloaded in advance ‘Cheque template Word.docx’ file.</span></span>  
12. <span data-ttu-id="89fa5-187">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-187">Close the page.</span></span>
13. <span data-ttu-id="89fa5-188">Şablon alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="89fa5-188">In the Template field, enter or select a value.</span></span>
14. <span data-ttu-id="89fa5-189">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-189">Click Save.</span></span>
15. <span data-ttu-id="89fa5-190">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-190">Close the page.</span></span>
16. <span data-ttu-id="89fa5-191">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-191">Click Edit.</span></span>
17. <span data-ttu-id="89fa5-192">Taslak Çalıştır alanında Evet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-192">Select Yes in the Run Draft field.</span></span>
18. <span data-ttu-id="89fa5-193">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-193">Close the page.</span></span>
19. <span data-ttu-id="89fa5-194">Nakit ve banka yönetimi > Banka hesapları > Banka hesapları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="89fa5-194">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
20. <span data-ttu-id="89fa5-195">Banka hesabı alanında "USMF OPER" değeriyle filtre uygulamak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-195">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
21. <span data-ttu-id="89fa5-196">Denetle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-196">Click Check.</span></span>
22. <span data-ttu-id="89fa5-197">Testi yazdır'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-197">Click Print test.</span></span>
23. <span data-ttu-id="89fa5-198">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-198">Click OK.</span></span>
    * <span data-ttu-id="89fa5-199">Oluşturulan sonucu inceleyin.</span><span class="sxs-lookup"><span data-stu-id="89fa5-199">Review the created output.</span></span> <span data-ttu-id="89fa5-200">Çıktının şirket logosunu, yetkili kişinin imzasını ve filigranın seçilen metnini gösteren bir MS Word belgesi olarak oluşturulduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="89fa5-200">Note that the output has been generated as a MS Word document with embedded images presenting the company logo, the signature of an authorized person and the selected text of the watermark.</span></span>  


