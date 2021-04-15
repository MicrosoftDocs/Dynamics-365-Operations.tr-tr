---
title: Katıştırılmış resimlere sahip Office biçiminde rapor oluşturmak için yapılandırmaları gözden geçirme
description: Bu konuda, katıştırılmış resimler içeren elektronik belgeler oluşturmak için raporlama yapılandırmalarının nasıl tasarlanacağı açıklanmaktadır. (1. Bölüm - Parametreleri ayarlama).
author: NickSelin
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: de815b363daa9135b50a2f5c9c4ac19e87b6b7ee
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751594"
---
# <a name="review-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="895bd-104">Katıştırılmış resimlere sahip Office biçiminde rapor oluşturmak için yapılandırmaları gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="895bd-104">Review configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="895bd-105">Bu adımları tamamlamak için öncelikle "ER Katıştırılmış resimler barındıran MS Office biçimlerinde raporlar hazırla (Bölüm 1 - Parametrelerin kurulumu)" görev kılavuzundaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="895bd-105">To complete these steps, you must first complete the steps in the "ER Make reports in MS Office formats with embedded images (Part 1: Set up parameters)" task guide.</span></span>

<span data-ttu-id="895bd-106">Bu yordam, Microsoft Excel ve Microsoft Word'te katıştırılmış resimler içeren elektronik belgelerin Elektronik raporlama (ER) yapılandırmalarının nasıl tasarlanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="895bd-106">This procedure shows how to design Electronic reporting (ER) configurations to generate electronic documents that contain embedded images in Microsoft Excel and Microsoft Word.</span></span> <span data-ttu-id="895bd-107">Bu örnekte, 'Litware, Inc.' örnek şirketi için ER yapılandırmalarını gözden geçireceksiniz.</span><span class="sxs-lookup"><span data-stu-id="895bd-107">In this example, you will review ER configurations for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="895bd-108">Bu yordam Sistem yöneticisi veya Elektronik raporlama geliştiricisi rolüne atanmış kullanıcılar içindir.</span><span class="sxs-lookup"><span data-stu-id="895bd-108">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="895bd-109">Adımlar USMF veri kümesi kullanılarak tamamlanabilir.</span><span class="sxs-lookup"><span data-stu-id="895bd-109">The steps can be completed by using the USMF data set.</span></span>


## <a name="review-the-imported-data-model"></a><span data-ttu-id="895bd-110">İçe aktarılan veri modelini gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="895bd-110">Review the imported data model</span></span>
1. <span data-ttu-id="895bd-111">Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="895bd-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="895bd-112">Ağaçta, 'Çekler için model' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="895bd-112">In the tree, select 'Model for cheques'.</span></span>
3. <span data-ttu-id="895bd-113">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="895bd-113">Click Designer.</span></span>
    * <span data-ttu-id="895bd-114">Bu model, bu modelin uygulamanın veri kaynaklarına işletme bakış açısından ödeme çeklerini temsil etmek için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="895bd-114">This model is designed to represent payment cheques from the business standpoint and the mapping of this model to the application's data sources.</span></span> <span data-ttu-id="895bd-115">Bu modeli ER Operasyonlar tasarımcısında ön izleyin.</span><span class="sxs-lookup"><span data-stu-id="895bd-115">Review this model by the ER Operations designer.</span></span> <span data-ttu-id="895bd-116">Sunulan model öğelerinin özniteliklerini göz önünde bulundurun: yapı, ad, açıklama, veri türü ve benzeri.</span><span class="sxs-lookup"><span data-stu-id="895bd-116">Note the attributes of the model elements that are presented: structure, name, description, data type, and so on.</span></span>   
4. <span data-ttu-id="895bd-117">Ağaçta, 'kök' metnini genişletin.</span><span class="sxs-lookup"><span data-stu-id="895bd-117">In the tree, expand 'root'.</span></span>
5. <span data-ttu-id="895bd-118">Ağaçta 'kök\çekler' genişletin.</span><span class="sxs-lookup"><span data-stu-id="895bd-118">In the tree, select 'root\cheques'.</span></span>
6. <span data-ttu-id="895bd-119">Ağaçta, 'kök\çekler' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="895bd-119">In the tree, expand 'root\cheques'.</span></span>
7. <span data-ttu-id="895bd-120">Ağaçta 'kök\çekler\öznitelikler' seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="895bd-120">In the tree, expand 'root\cheques\attributes'.</span></span>
8. <span data-ttu-id="895bd-121">Ağaçta 'kök\ödeyen' seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="895bd-121">In the tree, expand 'root\payer'.</span></span>
9. <span data-ttu-id="895bd-122">Ağaçta 'kök\istestrun' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="895bd-122">In the tree, select 'root\istestrun'.</span></span>
10. <span data-ttu-id="895bd-123">Ağaçta 'kök\düzen' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="895bd-123">In the tree, select 'root\layout'.</span></span>
    * <span data-ttu-id="895bd-124">Bu modelin düzen öğesi, seçilen banka hesabı için yazdırılan çek biçimi düzeninin ayrıntılarını temsil eder.</span><span class="sxs-lookup"><span data-stu-id="895bd-124">The layout element of this model represents the details of the printing cheque form layout for the selected bank account.</span></span> <span data-ttu-id="895bd-125">Resimleri depolamak için konteyner veri türünün iki düğümünü de içerir.</span><span class="sxs-lookup"><span data-stu-id="895bd-125">It also includes two nodes of the Container data type to store images.</span></span>   
11. <span data-ttu-id="895bd-126">Ağaçta 'kök\düzen' görünümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="895bd-126">In the tree, expand 'root\layout'.</span></span>
12. <span data-ttu-id="895bd-127">Ağaçta 'kök\düzen\şirket logosu' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="895bd-127">In the tree, select 'root\layout\company logo'.</span></span>
13. <span data-ttu-id="895bd-128">Ağaçta 'kök\düzen\şirket logosu' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="895bd-128">In the tree, expand 'root\layout\company logo'.</span></span>
14. <span data-ttu-id="895bd-129">Ağaçta 'kök\düzen\şirket logosu\resim' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="895bd-129">In the tree, select 'root\layout\company logo\image'.</span></span>
15. <span data-ttu-id="895bd-130">Ağaçta 'kök\düzen\şirket logosu\isprinted' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="895bd-130">In the tree, select 'root\layout\company logo\isprinted'.</span></span>
16. <span data-ttu-id="895bd-131">Ağaçta 'kök\düzen\imza' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="895bd-131">In the tree, select 'root\layout\signature'.</span></span>
17. <span data-ttu-id="895bd-132">Ağaçta, 'kök\düzen\imza' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="895bd-132">In the tree, expand 'root\layout\signature'.</span></span>
18. <span data-ttu-id="895bd-133">Ağaçta 'kök\düzen\imza\resim' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="895bd-133">In the tree, select 'root\layout\signature\image'.</span></span>
19. <span data-ttu-id="895bd-134">Ağaçta 'kök\düzen\imza\isprinted' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="895bd-134">In the tree, select 'root\layout\signature\isprinted'.</span></span>
    * <span data-ttu-id="895bd-135">İki resim veri modeli öğesinin, şirket logosunun ve yetkili kişinin imzasının ikili biçimdeki resimlerini içeren alanlara bağlı olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="895bd-135">Note that two image data model elements are bound to the fields of the tables that contain images of the company logo and the authorized person's signature in binary format.</span></span>  
20. <span data-ttu-id="895bd-136">Ağaçta 'kök\düzen\filigran' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="895bd-136">In the tree, expand 'root\layout\watermark'.</span></span>
21. <span data-ttu-id="895bd-137">Modeli veri kaynağına eşle'yi tıklayın.</span><span class="sxs-lookup"><span data-stu-id="895bd-137">Click Map model to datasource.</span></span>
22. <span data-ttu-id="895bd-138">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="895bd-138">Click Designer.</span></span>
23. <span data-ttu-id="895bd-139">Ağaçta 'chequesselected' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="895bd-139">In the tree, expand 'chequesselected'.</span></span>
24. <span data-ttu-id="895bd-140">Ağaçta, 'düzen' metnini genişletin.</span><span class="sxs-lookup"><span data-stu-id="895bd-140">In the tree, expand 'layout'.</span></span>
25. <span data-ttu-id="895bd-141">Ağaçta 'düzen\şirket logosu' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="895bd-141">In the tree, expand 'layout\company logo'.</span></span>
26. <span data-ttu-id="895bd-142">Ağaçta, 'düzen\imza' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="895bd-142">In the tree, expand 'layout\signature'.</span></span>
27. <span data-ttu-id="895bd-143">Ağaçta, 'düzen\filigran' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="895bd-143">In the tree, expand 'layout\watermark'.</span></span>
28. <span data-ttu-id="895bd-144">"Ayrıntıları göster" öğesini açın.</span><span class="sxs-lookup"><span data-stu-id="895bd-144">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="895bd-145">Çekler veri modeli öğesinin çalışma zamanında kullanıcının yazdırılmak üzere seçtiği çeklerin kayıtlarını içeren TmpChequePrintout tablosuna bağlı olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="895bd-145">Note that the cheques data model element is bound to the TmpChequePrintout table that, at runtime, will contain records for cheques that the user has selected for printing.</span></span>   
29. <span data-ttu-id="895bd-146">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="895bd-146">Close the page.</span></span>
30. <span data-ttu-id="895bd-147">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="895bd-147">Close the page.</span></span>
31. <span data-ttu-id="895bd-148">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="895bd-148">Close the page.</span></span>

## <a name="review-the-imported-format"></a><span data-ttu-id="895bd-149">İçe aktarılan biçimi gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="895bd-149">Review the imported format</span></span>
1. <span data-ttu-id="895bd-150">Ağaçta, 'Çekler için model' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="895bd-150">In the tree, expand 'Model for cheques'.</span></span>
2. <span data-ttu-id="895bd-151">Ağaçta 'Çekler için model\Çek yazdırma biçimi' seçin.</span><span class="sxs-lookup"><span data-stu-id="895bd-151">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
3. <span data-ttu-id="895bd-152">Tasarımcı'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="895bd-152">Click Designer.</span></span>
4. <span data-ttu-id="895bd-153">Ekler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="895bd-153">Click Attachments.</span></span>
5. <span data-ttu-id="895bd-154">Aç'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="895bd-154">Click Open.</span></span>
    * <span data-ttu-id="895bd-155">Eklenen raporun şablonunu Excel'de açın.</span><span class="sxs-lookup"><span data-stu-id="895bd-155">Open the attached report's template in Excel.</span></span>  
    * <span data-ttu-id="895bd-156">Eklenen raporun Excel şablonu, çekleri yazdırmak için kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="895bd-156">Review the attached report's Excel template that will be used to print cheques.</span></span> <span data-ttu-id="895bd-157">Şablon sayfa başına iki çek içerir ve çekleri önceden yazdırılmış biçimde yazdırmak için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="895bd-157">The template contains two cheques per page and is designed to print cheques to the preprinted form.</span></span> <span data-ttu-id="895bd-158">İki boş resmin katıştırılmış olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="895bd-158">Note that two blank images are embedded.</span></span> <span data-ttu-id="895bd-159">Bu boş resimler şirket logosu ve ödemeye izin veren kişinin imzası içindir.</span><span class="sxs-lookup"><span data-stu-id="895bd-159">These blank images are for the company logo and the signature of the person who is authorizing a payment.</span></span> <span data-ttu-id="895bd-160">Resimlerin Excel'de sırasıyla CompLogo ve SignatureImage olarak adlandırıldığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="895bd-160">Verify that the images are named CompLogo and SignatureImage, respectively, in Excel.</span></span>   
6. <span data-ttu-id="895bd-161">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="895bd-161">Close the page.</span></span>
7. <span data-ttu-id="895bd-162">Ağaçta, 'Rapor' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="895bd-162">In the tree, expand 'Report'.</span></span>
8. <span data-ttu-id="895bd-163">Ağaçta, 'Rapor\ChequeLines' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="895bd-163">In the tree, expand 'Report\ChequeLines'.</span></span>
9. <span data-ttu-id="895bd-164">Ağaçta 'Rapor\ChequeLines\CompLogo' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="895bd-164">In the tree, select 'Report\ChequeLines\CompLogo'.</span></span>
10. <span data-ttu-id="895bd-165">"Ayrıntıları göster" öğesini açın.</span><span class="sxs-lookup"><span data-stu-id="895bd-165">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="895bd-166">'CompLogo' biçiminin hücre öğesi, raporda şirket logosu resmini doldurmak için kullanılan Excel öğesini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="895bd-166">Note that the 'CompLogo' format's cell element represents the Excel item that is used to populate the company logo image in the report.</span></span> <span data-ttu-id="895bd-167">Bu biçim öğesi, çalışma zamanında bir şirket logosunu ikili biçimde içeren bir resim veri modeli öğesine bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="895bd-167">This format element is bound to the image data model element that, at runtime, contains a company logo image in binary format.</span></span>   
11. <span data-ttu-id="895bd-168">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="895bd-168">Click the Mapping tab.</span></span>
12. <span data-ttu-id="895bd-169">Düzenleme etkinleştirildi'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="895bd-169">Click Edit enabled.</span></span>
    * <span data-ttu-id="895bd-170">'CompLogo' biçiminin hücre öğesini daha fazla etkin olmayacağı şekilde yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="895bd-170">Note that you can make the 'CompLogo' format's cell element so that it's no longer enabled.</span></span> <span data-ttu-id="895bd-171">Bu durumda, ilişkilendirilen Excel resim öğesi, bir şirket logosunu oluşturulan raporda gizleyecektir.</span><span class="sxs-lookup"><span data-stu-id="895bd-171">In this case, the associated Excel image element will hide a company logo in the generated report.</span></span> <span data-ttu-id="895bd-172">Etkinleştirilen deyim DOĞRU sonucunu getirirse ve tanımlanan bağlama resim getirmez, ilişkilendirilen Excel resim dosyası, Excel şablonu kaydedilmiş olan bir resmi gösterir.</span><span class="sxs-lookup"><span data-stu-id="895bd-172">If the enabled expression returns TRUE and the defined binding brings no image, the associated Excel image element will show an image that has been saved in the Excel template.</span></span>   
13. <span data-ttu-id="895bd-173">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="895bd-173">Close the page.</span></span>
14. <span data-ttu-id="895bd-174">Ağaçta, 'etiketler: Konteyner' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="895bd-174">In the tree, expand 'labels: Container'.</span></span>
    * <span data-ttu-id="895bd-175">Önceden yazdırılmış çek formunda sunulan bazı etiketler, test amaçlı oluşturulduğunda rapora dahil edilecektir.</span><span class="sxs-lookup"><span data-stu-id="895bd-175">Some labels that are presented in the preprinted cheque form will be included in the report when it's created for testing purposes.</span></span> <span data-ttu-id="895bd-176">Ancak, bu etiketler gerçek yazdırma sırasında yazdırılmayacaktır çünkü önceden yazdırılmış form zaten bunları içerir.</span><span class="sxs-lookup"><span data-stu-id="895bd-176">However, those labels won't be printed during real printing, because the preprinted form already includes them.</span></span>  
15. <span data-ttu-id="895bd-177">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="895bd-177">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]