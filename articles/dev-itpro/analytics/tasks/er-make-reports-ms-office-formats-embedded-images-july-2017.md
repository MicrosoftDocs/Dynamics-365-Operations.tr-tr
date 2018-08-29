--- 
title: "Katıştırılmış resimlere sahip Office biçiminde rapor oluşturmak için yapılandırmalar tasarlama"
description: "Bu konudaki adımlar, Microsoft Office biçimlerinde (Excel ve Word) katıştırılmış resimler içeren elektronik belgelerin Elektronik raporlama (ER) yapılandırmalarının nasıl tasarlanacağını hakkında bilgi verir."
author: NickSelin
manager: AnnBe
ms.date: 01/23/2018
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
ms.openlocfilehash: 1fb02e561f6792c57b924ba64a5ca3d3974289ee
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="f7dbd-103">Katıştırılmış resimlere sahip Office biçiminde rapor oluşturmak için yapılandırmalar tasarlama</span><span class="sxs-lookup"><span data-stu-id="f7dbd-103">Design configurations to generate reports in Office format that have embedded images</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f7dbd-104">Bu yordamdaki adımları tamamlamak için öncelikle "ER Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamını tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-104">To complete the steps in this procedure, first complete the procedure, “ER Create a configuration provider and mark it as active.”</span></span> <span data-ttu-id="f7dbd-105">Bu yordam, katıştırılmış resimler içeren Microsoft Excel veya Word belgeleri oluşturmak üzere Elektronik raporlama (ER) yapılandırmalarının nasıl tasarlanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="f7dbd-106">Bu yordamda, Litware, Inc. adlı örnek şirket için gerekli ER yapılandırmalarını oluşturacaksınız. Bu adımlar USMF veri kümesi kullanılarak tamamlanabilir.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="f7dbd-107">Bu yordam, sistem yöneticisi veya elektronik raporlama geliştiricisi rolüne atanmış kullanıcılar için oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="f7dbd-108">Başlamadan önce [Elektronik raporlama aracı kullanılarak oluşturulan iş belgelerine görüntü ve şekil katıştırma](../electronic-reporting-embed-images-shapes.md) Yardım konusunda listelenen dosyaları indirin ve kaydedin.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-108">Before you begin, download and save the files listed in the Help topic, [Embed images and shapes in business documents that are generated with the Electronic reporting tool](../electronic-reporting-embed-images-shapes.md).</span></span> <span data-ttu-id="f7dbd-109">Bu dosyalar şunlardır: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png, and Cheque template Word.docx.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-109">The files are: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png, and Cheque template Word.docx.</span></span>

## <a name="verify-prerequisites"></a><span data-ttu-id="f7dbd-110">Ön koşulları doğrulama</span><span class="sxs-lookup"><span data-stu-id="f7dbd-110">Verify prerequisites</span></span>  
 1. <span data-ttu-id="f7dbd-111">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="f7dbd-112">Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve etkin olarak işaretlemiş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-112">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="f7dbd-113">Bu yapılandırma sağlayıcısını göremiyorsanız "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-113">If you don’t see this configuration provider, complete the steps in the procedure, “Create a configuration provider and mark it as active.”</span></span>   
 3. <span data-ttu-id="f7dbd-114">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-114">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="f7dbd-115">Yeni bir ER model yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="f7dbd-115">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="f7dbd-116">Yeni bir model oluşturmak yerine, daha önce kaydetmiş olduğunuz ER modeli yapılandırma dosyasını (Model for cheques.xml) yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-116">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="f7dbd-117">Bu dosya ödeme çekleri için örnek veri modelini ve veri modelinin Dynamics 365 for Operations uygulamasındaki veri bileşenleriyle eşleşmesini içerir.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-117">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="f7dbd-118">Sürümler hızlı sekmesinde, Değiştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-118">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="f7dbd-119">XML dosyasından yükle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-119">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="f7dbd-120">Gözat'a tıklayın ve sonra Model for cheques.xml dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-120">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="f7dbd-121">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-121">Click OK.</span></span>  
 6. <span data-ttu-id="f7dbd-122">Yüklenen model resimler içeren Excel ve Word biçiminde belgeler oluşturmak için veri kaynağı olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-122">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="f7dbd-123">Yeni bir ER biçim yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="f7dbd-123">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="f7dbd-124">Yeni bir biçim oluşturmak yerine, daha önce kaydetmiş olduğunuz ER biçimi yapılandırma dosyasını (Cheques printing format.xml) yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-124">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="f7dbd-125">Bu dosya, önceden yazdırılan formu ve bu biçimin 'Çekler için model' veri modelindeki eşlemesini kullanan çekleri yazdırmaya yönelik biçim için örnek düzeni içerir.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-125">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the ‘Model for cheques’ data model.</span></span>   
 2. <span data-ttu-id="f7dbd-126">Değiştir seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-126">Click Exchange.</span></span>  
 3. <span data-ttu-id="f7dbd-127">XML dosyasından yükle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-127">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="f7dbd-128">Gözat'a tıklayın ve Çek yazdırma biçimi.xml dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-128">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="f7dbd-129">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-129">Click OK.</span></span>  
 6. <span data-ttu-id="f7dbd-130">Ağaçta, 'Çekler için model' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-130">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="f7dbd-131">Ağaçta 'Çekler için model\Çek yazdırma biçimi' seçin.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-131">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="f7dbd-132">Yüklenen biçim resimler içeren Excel ve Word biçiminde belgeler oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-132">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="f7dbd-133">ER kullanıcı parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="f7dbd-133">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="f7dbd-134">Eylem Bölmesi'nde, Yapılandırmalar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-134">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="f7dbd-135">Kullanıcı parametreleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-135">Click User parameters.</span></span>  
 3. <span data-ttu-id="f7dbd-136">Çalıştırma ayarları alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-136">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="f7dbd-137">Seçilen biçimin tamamlanmış sürümü yerine taslak sürümünü başlatmak için 'Taslak çalıştır' bayrağını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-137">Turn on the ‘Run draft’ flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="f7dbd-138">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-138">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="f7dbd-139">Nakit ve banka yönetimi parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="f7dbd-139">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="f7dbd-140">Nakit ve banka yönetimi > Banka hesapları > Banka hesapları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-140">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="f7dbd-141">Banka hesabı alanında "USMF OPER" değeriyle filtre uygulamak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-141">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="f7dbd-142">Eylem Bölmesinde Kurulum'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-142">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="f7dbd-143">Denetle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-143">Click Check.</span></span>  
 5. <span data-ttu-id="f7dbd-144">Kurulum bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-144">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="f7dbd-145">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-145">Click Edit.</span></span>  
 7. <span data-ttu-id="f7dbd-146">Şirket logosu alanından Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-146">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="f7dbd-147">Şirket logosuna tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-147">Click Company logo.</span></span>  
 9. <span data-ttu-id="f7dbd-148">Değiştir seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-148">Click Change.</span></span>  
 10. <span data-ttu-id="f7dbd-149">Gözat'a tıklayın ve daha önce indirdiğiniz Şirket logosu.png dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-149">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="f7dbd-150">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-150">Click Save.</span></span>  
 12. <span data-ttu-id="f7dbd-151">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-151">Close the page.</span></span>  
 13. <span data-ttu-id="f7dbd-152">İmza bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-152">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="f7dbd-153">İlk imzayı yazdır alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-153">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="f7dbd-154">Değiştir seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-154">Click Change.</span></span>  
 16. <span data-ttu-id="f7dbd-155">Gözat'a tıklayın ve daha önce indirdiğiniz İmza görüntüsü.png dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-155">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="f7dbd-156">Kopyalar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-156">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="f7dbd-157">Filigran alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-157">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="f7dbd-158">Genel elektronik Dışa aktarma biçimi alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-158">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="f7dbd-159">'Çek yazdırma formu' yapılandırmasını seçin.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-159">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="f7dbd-160">Seçilen ER biçimi artık çekleri yazdırmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-160">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="f7dbd-161">İliştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-161">Click Attach.</span></span>  
 23. <span data-ttu-id="f7dbd-162">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-162">Click New.</span></span>  
 24. <span data-ttu-id="f7dbd-163">Dosya'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-163">Click File.</span></span>  
 25. <span data-ttu-id="f7dbd-164">Gözat'a tıklayın ve daha önce indirdiğiniz İmza görüntüsü 2.png dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-164">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="f7dbd-165">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-165">Close the page.</span></span>  
 27. <span data-ttu-id="f7dbd-166">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-166">Close the page.</span></span>  
 28. <span data-ttu-id="f7dbd-167">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-167">Close the page.</span></span>  
 29. <span data-ttu-id="f7dbd-168">Nakit ve Banka yönetimi > Kurulum > Nakit ve Banka yönetim parametreleri.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-168">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="f7dbd-169">Etkin olmayan banka hesaplarında açık provizyon oluşturmaya izin ver: alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-169">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="f7dbd-170">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-170">Click Save.</span></span>  
 32. <span data-ttu-id="f7dbd-171">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f7dbd-171">Close the page.</span></span>  

