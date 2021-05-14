---
title: Katıştırılmış resimlere sahip Office biçiminde rapor oluşturmak için yapılandırmalar tasarlama
description: Bu konuda, katıştırılmış resimler içeren Excel ve Word biçimlerinde elektronik belgeler oluşturan yapılandırmaların nasıl tasarlanacağı açıklanmaktadır.
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5eea178a351716425706f481ae66c5b5183a52e5
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944569"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="0b364-103">Katıştırılmış resimlere sahip Office biçiminde rapor oluşturmak için yapılandırmalar tasarlama</span><span class="sxs-lookup"><span data-stu-id="0b364-103">Design configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0b364-104">Bu yordamdaki adımları tamamlamak için öncelikle "ER Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamını tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="0b364-104">To complete the steps in this procedure, first complete the procedure, "ER Create a configuration provider and mark it as active."</span></span> <span data-ttu-id="0b364-105">Bu yordam, katıştırılmış resimler içeren Microsoft Excel veya Word belgeleri oluşturmak üzere Elektronik raporlama (ER) yapılandırmalarının nasıl tasarlanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b364-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="0b364-106">Bu yordamda, Litware, Inc. adlı örnek şirket için gerekli ER yapılandırmalarını oluşturacaksınız. Bu adımlar USMF veri kümesi kullanılarak tamamlanabilir.</span><span class="sxs-lookup"><span data-stu-id="0b364-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="0b364-107">Bu yordam, sistem yöneticisi veya elektronik raporlama geliştiricisi rolüne atanmış kullanıcılar için oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="0b364-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="0b364-108">Başlamadan önce aşağıdaki dosyaları da indirip kaydetmelisiniz:</span><span class="sxs-lookup"><span data-stu-id="0b364-108">Before you begin, download and save the following files:</span></span> 

| <span data-ttu-id="0b364-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b364-109">Description</span></span>                                          | <span data-ttu-id="0b364-110">Dosya adı</span><span class="sxs-lookup"><span data-stu-id="0b364-110">File name</span></span>                   |
|------------------------------------------------------|-----------------------------|
| <span data-ttu-id="0b364-111">ER data model configuration</span><span class="sxs-lookup"><span data-stu-id="0b364-111">ER data model configuration</span></span>                          | [<span data-ttu-id="0b364-112">Model for cheques.xml</span><span class="sxs-lookup"><span data-stu-id="0b364-112">Model for cheques.xml</span></span>](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| <span data-ttu-id="0b364-113">ER format configuration</span><span class="sxs-lookup"><span data-stu-id="0b364-113">ER format configuration</span></span>                              | [<span data-ttu-id="0b364-114">Cheques printing format.xml</span><span class="sxs-lookup"><span data-stu-id="0b364-114">Cheques printing format.xml</span></span>](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| <span data-ttu-id="0b364-115">Şirket logosu resmi</span><span class="sxs-lookup"><span data-stu-id="0b364-115">Company logo image</span></span>                                   | [<span data-ttu-id="0b364-116">Şirket logosu.png</span><span class="sxs-lookup"><span data-stu-id="0b364-116">Company logo.png</span></span>](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| <span data-ttu-id="0b364-117">İmza resmi</span><span class="sxs-lookup"><span data-stu-id="0b364-117">Signature image</span></span>                                      | [<span data-ttu-id="0b364-118">İmza resmi.png</span><span class="sxs-lookup"><span data-stu-id="0b364-118">Signature image.png</span></span>](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| <span data-ttu-id="0b364-119">Alternatif imza resmi</span><span class="sxs-lookup"><span data-stu-id="0b364-119">Alternative signature image</span></span>                          | [<span data-ttu-id="0b364-120">İmza resmi 2.png</span><span class="sxs-lookup"><span data-stu-id="0b364-120">Signature image 2.png</span></span>](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| <span data-ttu-id="0b364-121">Ödeme çeklerini yazdırmak için Microsoft Word şablonu</span><span class="sxs-lookup"><span data-stu-id="0b364-121">Microsoft Word template for printing payment checks</span></span>  | [<span data-ttu-id="0b364-122">Cheque template Word.docx</span><span class="sxs-lookup"><span data-stu-id="0b364-122">Cheque template Word.docx</span></span>](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |

## <a name="verify-prerequisites"></a><span data-ttu-id="0b364-123">Ön koşulları doğrulama</span><span class="sxs-lookup"><span data-stu-id="0b364-123">Verify prerequisites</span></span>  
 1. <span data-ttu-id="0b364-124">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="0b364-124">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="0b364-125">Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve etkin olarak işaretlemiş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="0b364-125">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="0b364-126">Bu yapılandırma sağlayıcısını göremiyorsanız "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="0b364-126">If you don't see this configuration provider, complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>   
 3. <span data-ttu-id="0b364-127">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b364-127">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="0b364-128">Yeni bir ER model yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="0b364-128">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="0b364-129">Yeni bir model oluşturmak yerine, daha önce kaydetmiş olduğunuz ER modeli yapılandırma dosyasını (Model for cheques.xml) yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0b364-129">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="0b364-130">Bu dosya ödeme çekleri için örnek veri modelini ve veri modelinin Dynamics 365 for Operations uygulamasındaki veri bileşenleriyle eşleşmesini içerir.</span><span class="sxs-lookup"><span data-stu-id="0b364-130">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="0b364-131">Sürümler hızlı sekmesinde, Değiştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b364-131">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="0b364-132">XML dosyasından yükle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b364-132">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="0b364-133">Gözat'a tıklayın ve sonra Model for cheques.xml dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="0b364-133">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="0b364-134">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b364-134">Click OK.</span></span>  
 6. <span data-ttu-id="0b364-135">Yüklenen model resimler içeren Excel ve Word biçiminde belgeler oluşturmak için veri kaynağı olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0b364-135">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="0b364-136">Yeni bir ER biçim yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="0b364-136">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="0b364-137">Yeni bir biçim oluşturmak yerine, daha önce kaydetmiş olduğunuz ER biçimi yapılandırma dosyasını (Cheques printing format.xml) yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0b364-137">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="0b364-138">Bu dosya, önceden yazdırılan formu ve bu biçimin 'Çekler için model' veri modelindeki eşlemesini kullanan çekleri yazdırmaya yönelik biçim için örnek düzeni içerir.</span><span class="sxs-lookup"><span data-stu-id="0b364-138">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the 'Model for cheques' data model.</span></span>   
 2. <span data-ttu-id="0b364-139">Değiştir seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b364-139">Click Exchange.</span></span>  
 3. <span data-ttu-id="0b364-140">XML dosyasından yükle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b364-140">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="0b364-141">Gözat'a tıklayın ve Çek yazdırma biçimi.xml dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="0b364-141">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="0b364-142">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b364-142">Click OK.</span></span>  
 6. <span data-ttu-id="0b364-143">Ağaçta, 'Çekler için model' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="0b364-143">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="0b364-144">Ağaçta 'Çekler için model\Çek yazdırma biçimi' seçin.</span><span class="sxs-lookup"><span data-stu-id="0b364-144">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="0b364-145">Yüklenen biçim resimler içeren Excel ve Word biçiminde belgeler oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0b364-145">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="0b364-146">ER kullanıcı parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="0b364-146">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="0b364-147">Eylem Bölmesi'nde, Yapılandırmalar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b364-147">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="0b364-148">Kullanıcı parametreleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b364-148">Click User parameters.</span></span>  
 3. <span data-ttu-id="0b364-149">Çalıştırma ayarları alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0b364-149">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="0b364-150">Seçilen biçimin tamamlanmış sürümü yerine taslak sürümünü başlatmak için 'Taslak çalıştır' bayrağını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="0b364-150">Turn on the 'Run draft' flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="0b364-151">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b364-151">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="0b364-152">Nakit ve banka yönetimi parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="0b364-152">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="0b364-153">Nakit ve banka yönetimi > Banka hesapları > Banka hesapları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="0b364-153">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="0b364-154">Banka hesabı alanında "USMF OPER" değeriyle filtre uygulamak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="0b364-154">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="0b364-155">Eylem Bölmesinde Kurulum'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b364-155">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="0b364-156">Denetle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="0b364-156">Click Check.</span></span>  
 5. <span data-ttu-id="0b364-157">Kurulum bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="0b364-157">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="0b364-158">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b364-158">Click Edit.</span></span>  
 7. <span data-ttu-id="0b364-159">Şirket logosu alanından Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0b364-159">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="0b364-160">Şirket logosuna tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b364-160">Click Company logo.</span></span>  
 9. <span data-ttu-id="0b364-161">Değiştir seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b364-161">Click Change.</span></span>  
 10. <span data-ttu-id="0b364-162">Gözat'a tıklayın ve daha önce indirdiğiniz Şirket logosu.png dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="0b364-162">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="0b364-163">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b364-163">Click Save.</span></span>  
 12. <span data-ttu-id="0b364-164">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0b364-164">Close the page.</span></span>  
 13. <span data-ttu-id="0b364-165">İmza bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="0b364-165">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="0b364-166">İlk imzayı yazdır alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0b364-166">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="0b364-167">Değiştir seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b364-167">Click Change.</span></span>  
 16. <span data-ttu-id="0b364-168">Gözat'a tıklayın ve daha önce indirdiğiniz İmza görüntüsü.png dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="0b364-168">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="0b364-169">Kopyalar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="0b364-169">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="0b364-170">Filigran alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="0b364-170">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="0b364-171">Genel elektronik Dışa aktarma biçimi alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0b364-171">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="0b364-172">'Çek yazdırma formu' yapılandırmasını seçin.</span><span class="sxs-lookup"><span data-stu-id="0b364-172">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="0b364-173">Seçilen ER biçimi artık çekleri yazdırmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0b364-173">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="0b364-174">İliştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b364-174">Click Attach.</span></span>  
 23. <span data-ttu-id="0b364-175">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b364-175">Click New.</span></span>  
 24. <span data-ttu-id="0b364-176">Dosya'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b364-176">Click File.</span></span>  
 25. <span data-ttu-id="0b364-177">Gözat'a tıklayın ve daha önce indirdiğiniz Signature image 2.png dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="0b364-177">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="0b364-178">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0b364-178">Close the page.</span></span>  
 27. <span data-ttu-id="0b364-179">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0b364-179">Close the page.</span></span>  
 28. <span data-ttu-id="0b364-180">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0b364-180">Close the page.</span></span>  
 29. <span data-ttu-id="0b364-181">Nakit ve Banka yönetimi > Kurulum > Nakit ve Banka yönetim parametreleri.</span><span class="sxs-lookup"><span data-stu-id="0b364-181">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="0b364-182">Etkin olmayan banka hesaplarında açık provizyon oluşturmaya izin ver: alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0b364-182">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="0b364-183">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0b364-183">Click Save.</span></span>  
 32. <span data-ttu-id="0b364-184">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0b364-184">Close the page.</span></span>  


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
