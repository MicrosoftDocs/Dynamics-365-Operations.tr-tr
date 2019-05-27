---
title: Katıştırılmış resimlere sahip Office biçiminde raporlar oluşturma
description: Aşağıdaki adımlar 'Sistem yöneticisi' veya 'Elektronik raporlama geliştiricisi' rolündeki bir kullanıcının, MS office biçimlerinde (Excel ve Word) katıştırılmış resimler içeren elektronik belgeler oluşturmak için Elektronik raporlama (ER) yapılandırmalarını nasıl tasarlayabileceklerini açıklar.
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
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
ms.openlocfilehash: 5ef7ec2f8b5b7fdf456ebb71b863e620ae21e6b5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544392"
---
# <a name="generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="f44cc-103">Katıştırılmış resimlere sahip Office biçiminde raporlar oluşturma</span><span class="sxs-lookup"><span data-stu-id="f44cc-103">Generate reports in Office format that have embedded images</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f44cc-104">Aşağıdaki adımlar 'Sistem yöneticisi' veya 'Elektronik raporlama geliştiricisi' rolündeki bir kullanıcının, MS office biçimlerinde (Excel ve Word) katıştırılmış resimler içeren elektronik belgeler oluşturmak için Elektronik raporlama (ER) yapılandırmalarını nasıl tasarlayabileceklerini açıklar.</span><span class="sxs-lookup"><span data-stu-id="f44cc-104">The following steps explain how a user playing either ‘System administrator’ or ‘Electronic reporting developer’ role can design Electronic reporting (ER) configurations to generate electronic documents in MS office formats (Excel and Word) containing embedded images.</span></span>

<span data-ttu-id="f44cc-105">Bu örnekte, 'Litware, Inc.' örnek şirketi için oluşturulmuş ER yapılandırmalarını kullanacaksınız.</span><span class="sxs-lookup"><span data-stu-id="f44cc-105">In this example, you will use created ER configurations for sample company, ‘Litware, Inc.’.</span></span>  <span data-ttu-id="f44cc-106">Bu adımları tamamlamak için öncelikle "ER Katıştırılmış resimler barındıran MS Office biçimlerinde raporlar hazırla (Bölüm 2: Yapılandırmaları gözden geçir)" görev kılavuzundaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-106">To complete these steps, you must first complete the steps in the “ER Make reports in MS Office formats with embedded images (Part 2: Review configurations)” task guide.</span></span> <span data-ttu-id="f44cc-107">Bu adımlar 'USMF' şirketinde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="f44cc-107">These steps can be performed in ‘USMF’ company.</span></span>


## <a name="run-format-with-initial-model-mapping"></a><span data-ttu-id="f44cc-108">Biçimi ilk model eşleme ile çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f44cc-108">Run format with initial model mapping</span></span>
1. <span data-ttu-id="f44cc-109">Nakit ve banka yönetimi > Banka hesapları > Banka hesapları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="f44cc-109">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="f44cc-110">Banka hesabı alanında "USMF OPER" değeriyle filtre uygulamak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-110">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="f44cc-111">Eylem Bölmesinde Kurulum'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-111">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="f44cc-112">Denetle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-112">Click Check.</span></span>
5. <span data-ttu-id="f44cc-113">Testi yazdır'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-113">Click Print test.</span></span>
    * <span data-ttu-id="f44cc-114">Test amacıyla biçimi çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-114">Run the format for testing purposes.</span></span>  
6. <span data-ttu-id="f44cc-115">Ciro edilebilir çek biçimi alanında Evet'i işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="f44cc-115">Select Yes in the Negotiable check format field.</span></span>
7. <span data-ttu-id="f44cc-116">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-116">Click OK.</span></span>
    * <span data-ttu-id="f44cc-117">Oluşturulan sonucu inceleyin.</span><span class="sxs-lookup"><span data-stu-id="f44cc-117">Review the created output.</span></span> <span data-ttu-id="f44cc-118">Şirket logosunun hem raporda hem de kişinin imzasında görüleceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-118">Note that the company logo is presented in the report as well as the authorized person’s signature.</span></span> <span data-ttu-id="f44cc-119">İmza resmi seçilen banka hesabıyla ilişkilendirilmiş 'Konteyner' veri türünün çek düzeni alanından alınır.</span><span class="sxs-lookup"><span data-stu-id="f44cc-119">The signature image is taken from the field of the ‘Container’ data type of the cheque layout record which is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="f44cc-120">Kopyalar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="f44cc-120">Expand the Copies section.</span></span>
9. <span data-ttu-id="f44cc-121">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-121">Click Edit.</span></span>
10. <span data-ttu-id="f44cc-122">Filigran alanında 'Filigranı Geçersiz olarak yazdır' girin.</span><span class="sxs-lookup"><span data-stu-id="f44cc-122">In the Watermark field, enter 'Print watermark as Void'.</span></span>
    * <span data-ttu-id="f44cc-123">Bir Excel şekli öğesinde belge oluştururken filigranı göstermek için filigran biçim ayarını değiştirin.</span><span class="sxs-lookup"><span data-stu-id="f44cc-123">Change the watermark layout setting to show the watermark text in generating document in an Excel shape element.</span></span>  
11. <span data-ttu-id="f44cc-124">Testi yazdır'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-124">Click Print test.</span></span>
12. <span data-ttu-id="f44cc-125">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-125">Click OK.</span></span>
    * <span data-ttu-id="f44cc-126">Oluşturulan sonucu inceleyin.</span><span class="sxs-lookup"><span data-stu-id="f44cc-126">Review the created output.</span></span> <span data-ttu-id="f44cc-127">Filigranın oluşturulan raporda seçin seçeneğine uygun olarak gösterileceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-127">Note that the watermark is shown in the created report in accordance to the selection option.</span></span>  
13. <span data-ttu-id="f44cc-128">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-128">Close the page.</span></span>
14. <span data-ttu-id="f44cc-129">Eylem Bölmesinde, Ödemeleri yönet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-129">On the Action Pane, click Manage payments.</span></span>
15. <span data-ttu-id="f44cc-130">Çekler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-130">Click Checks.</span></span>
16. <span data-ttu-id="f44cc-131">Filtreleri göster'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-131">Click Show filters.</span></span>
17. <span data-ttu-id="f44cc-132">Aşağıdaki filtreleri uygulayın: "Çek numarası" alanında "şunlardan biri" filtre işlecini kullanarak "381", "385", "389" filtre değerini girin.</span><span class="sxs-lookup"><span data-stu-id="f44cc-132">Apply the following filters: Enter a filter value of "381","385","389" on the "Check number" field using the "is one of" filter operator.</span></span>
18. <span data-ttu-id="f44cc-133">Listede, tüm satırları işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="f44cc-133">In the list, mark all rows.</span></span>
19. <span data-ttu-id="f44cc-134">Çek kopyasını yazdır'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-134">Click Print check copy.</span></span>
    * <span data-ttu-id="f44cc-135">Seçilen çekleri yeniden yazdırmak için biçimi çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-135">Run the format to re-print the selected cheques.</span></span>  
    * <span data-ttu-id="f44cc-136">Oluşturulan sonucu inceleyin.</span><span class="sxs-lookup"><span data-stu-id="f44cc-136">Review the created output.</span></span> <span data-ttu-id="f44cc-137">Seçilen çeklerin yeniden yazdırıldığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-137">Note that the selected cheques have been re-printed.</span></span> <span data-ttu-id="f44cc-138">Şirket logosu ve etiketleri yazdırılmaz çünkü önceden yazdırılmış formda mevcutturlar.</span><span class="sxs-lookup"><span data-stu-id="f44cc-138">The company logo and labels are not printed out since they are presented on the pre-printed form.</span></span>  

## <a name="modify-the-mapping-of-the-imported-data-model"></a><span data-ttu-id="f44cc-139">İçe aktarılan veri modelinin eşlemesini değiştirin</span><span class="sxs-lookup"><span data-stu-id="f44cc-139">Modify the mapping of the imported data model</span></span>
1. <span data-ttu-id="f44cc-140">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-140">Close the page.</span></span>
2. <span data-ttu-id="f44cc-141">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-141">Close the page.</span></span>
3. <span data-ttu-id="f44cc-142">Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="f44cc-142">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="f44cc-143">Ağaçta, 'Çekler için model' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="f44cc-143">In the tree, select 'Model for cheques'.</span></span>
5. <span data-ttu-id="f44cc-144">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-144">Click Designer.</span></span>
6. <span data-ttu-id="f44cc-145">Modeli veri kaynağına eşle'yi tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-145">Click Map model to datasource.</span></span>
7. <span data-ttu-id="f44cc-146">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-146">Click Designer.</span></span>
    * <span data-ttu-id="f44cc-147">Seçilen banka hesabıyla ilişkilendirilmiş çek biçim kaydına eklenmiş olan dosyadan imza resmi almak için veri modelinin imza öğesini değiştireceğiz.</span><span class="sxs-lookup"><span data-stu-id="f44cc-147">We will change the binding of the data model’s signature item to get the signature image from the file that has been attached to the cheque layout record which is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="f44cc-148">Ayrıntıları göster'i kapatın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-148">Turn Show details off.</span></span>
9. <span data-ttu-id="f44cc-149">Ağaçta, 'düzen' metnini genişletin.</span><span class="sxs-lookup"><span data-stu-id="f44cc-149">In the tree, expand 'layout'.</span></span>
10. <span data-ttu-id="f44cc-150">Ağaçta, 'düzen\imza' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="f44cc-150">In the tree, expand 'layout\signature'.</span></span>
11. <span data-ttu-id="f44cc-151">Ağaçta 'düzen\imza\resim = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp' seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="f44cc-151">In the tree, select 'layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp'.</span></span>
12. <span data-ttu-id="f44cc-152">Ağaçta, 'chequesaccount' öğesini genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-152">In the tree, expand 'chequesaccount'.</span></span>
13. <span data-ttu-id="f44cc-153">Ağaç altından 'chequesaccount\<İlişkiler' seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="f44cc-153">In the tree, expand 'chequesaccount\<Relations'.</span></span>
14. <span data-ttu-id="f44cc-154">Ağaçta 'chequesaccount\<İlişkiler\BankChequeLayout' seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="f44cc-154">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout'.</span></span>
15. <span data-ttu-id="f44cc-155">Ağaçta 'chequesaccount\<İlişkiler\BankChequeLayout\<İlişkiler' seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="f44cc-155">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations'.</span></span>
16. <span data-ttu-id="f44cc-156">Ağaçta 'chequesaccount\<İlişkiler\BankChequeLayout\<İlişkiler\<Belgeler' seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="f44cc-156">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents'.</span></span>
17. <span data-ttu-id="f44cc-157">Ağaçta 'chequesaccount\<İlişkiler\BankChequeLayout\<İlişkiler\Belgeler\<getFileContentAsContainer()' seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="f44cc-157">In the tree, select 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer()'.</span></span>
18. <span data-ttu-id="f44cc-158">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-158">Click Bind.</span></span>
19. <span data-ttu-id="f44cc-159">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-159">Click Save.</span></span>
20. <span data-ttu-id="f44cc-160">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-160">Close the page.</span></span>
21. <span data-ttu-id="f44cc-161">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-161">Close the page.</span></span>
22. <span data-ttu-id="f44cc-162">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-162">Close the page.</span></span>
23. <span data-ttu-id="f44cc-163">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-163">Close the page.</span></span>

## <a name="run-format-using-the-adjusted-model-mapping"></a><span data-ttu-id="f44cc-164">Ayarlanan model eşlemesini kullanarak biçimi çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f44cc-164">Run format using the adjusted model mapping</span></span>
1. <span data-ttu-id="f44cc-165">Nakit ve banka yönetimi > Banka hesapları > Banka hesapları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="f44cc-165">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="f44cc-166">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-166">Use the Quick Filter to find records.</span></span> <span data-ttu-id="f44cc-167">Örneğin, Banka hesabı alanında 'USMF OPER' değerini girerek filtreleme yapın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-167">For example, filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="f44cc-168">Eylem Bölmesinde Kurulum'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-168">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="f44cc-169">Denetle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-169">Click Check.</span></span>
5. <span data-ttu-id="f44cc-170">Testi yazdır'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-170">Click Print test.</span></span>
6. <span data-ttu-id="f44cc-171">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-171">Click OK.</span></span>
    * <span data-ttu-id="f44cc-172">Oluşturulan sonucu inceleyin.</span><span class="sxs-lookup"><span data-stu-id="f44cc-172">Review the created output.</span></span> <span data-ttu-id="f44cc-173">Belge yönetim ekinin, yetkili bir kişinin imzası olarak gösterileceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-173">Note that the image from the Document Management attachment is presented as the signature of an authorized person.</span></span>  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a><span data-ttu-id="f44cc-174">MS Word belgesini içe aktarılan biçimde bir şablon olarak kullanın</span><span class="sxs-lookup"><span data-stu-id="f44cc-174">Use MS Word document as a template in the imported format</span></span>
1. <span data-ttu-id="f44cc-175">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-175">Close the page.</span></span>
2. <span data-ttu-id="f44cc-176">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-176">Close the page.</span></span>
3. <span data-ttu-id="f44cc-177">Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="f44cc-177">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="f44cc-178">Ağaçta, 'Çekler için model' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="f44cc-178">In the tree, expand 'Model for cheques'.</span></span>
5. <span data-ttu-id="f44cc-179">Ağaçta 'Çekler için model\Çek yazdırma biçimi' seçin.</span><span class="sxs-lookup"><span data-stu-id="f44cc-179">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
6. <span data-ttu-id="f44cc-180">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-180">Click Designer.</span></span>
7. <span data-ttu-id="f44cc-181">Ekler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-181">Click Attachments.</span></span>
8. <span data-ttu-id="f44cc-182">Sil'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-182">Click Delete.</span></span>
9. <span data-ttu-id="f44cc-183">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-183">Click Yes.</span></span>
10. <span data-ttu-id="f44cc-184">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-184">Click New.</span></span>
11. <span data-ttu-id="f44cc-185">Dosya'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-185">Click File.</span></span>
    * <span data-ttu-id="f44cc-186">Gözat'ı tıklatın ve önceden indirilen 'Çek şablonu Word.docx' dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="f44cc-186">Click Browse and select the downloaded in advance ‘Cheque template Word.docx’ file.</span></span>  
12. <span data-ttu-id="f44cc-187">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-187">Close the page.</span></span>
13. <span data-ttu-id="f44cc-188">Şablon alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="f44cc-188">In the Template field, enter or select a value.</span></span>
14. <span data-ttu-id="f44cc-189">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-189">Click Save.</span></span>
15. <span data-ttu-id="f44cc-190">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-190">Close the page.</span></span>
16. <span data-ttu-id="f44cc-191">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-191">Click Edit.</span></span>
17. <span data-ttu-id="f44cc-192">Taslak Çalıştır alanında Evet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-192">Select Yes in the Run Draft field.</span></span>
18. <span data-ttu-id="f44cc-193">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-193">Close the page.</span></span>
19. <span data-ttu-id="f44cc-194">Nakit ve banka yönetimi > Banka hesapları > Banka hesapları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="f44cc-194">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
20. <span data-ttu-id="f44cc-195">Banka hesabı alanında "USMF OPER" değeriyle filtre uygulamak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-195">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
21. <span data-ttu-id="f44cc-196">Denetle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-196">Click Check.</span></span>
22. <span data-ttu-id="f44cc-197">Testi yazdır'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-197">Click Print test.</span></span>
23. <span data-ttu-id="f44cc-198">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-198">Click OK.</span></span>
    * <span data-ttu-id="f44cc-199">Oluşturulan sonucu inceleyin.</span><span class="sxs-lookup"><span data-stu-id="f44cc-199">Review the created output.</span></span> <span data-ttu-id="f44cc-200">Çıktının şirket logosunu, yetkili kişinin imzasını ve filigranın seçilen metnini gösteren bir MS Word belgesi olarak oluşturulduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="f44cc-200">Note that the output has been generated as a MS Word document with embedded images presenting the company logo, the signature of an authorized person and the selected text of the watermark.</span></span>  

