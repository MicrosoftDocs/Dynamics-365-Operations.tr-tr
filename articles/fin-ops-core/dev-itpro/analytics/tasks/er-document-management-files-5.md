---
title: ER Biçim çıktılarında Belge Yönetimi dosyalarını kullanma (Bölüm 5 - Biçimi değiştirme ve çalıştırma)
description: Bu konuda, ER çıktılarında Belge Yönetimi dosyaları (ekler) kullanmak üzere Elektronik raporlama (ER) biçiminin nasıl yapılandırılacağı açıklanmaktadır. (5. Bölüm)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERComponentTypeDropDialog, ERExpressionDesignerFormula, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6062945dfea0eec02e5055e9ebe697189267e051
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564822"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5---modify-and-run-format"></a><span data-ttu-id="ffaba-104">ER Biçim çıktılarında Belge Yönetimi dosyalarını kullanma (Bölüm 5 - Biçimi değiştirme ve çalıştırma)</span><span class="sxs-lookup"><span data-stu-id="ffaba-104">ER Use Document Management files in format outputs (Part 5 - Modify and run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ffaba-105">Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının, ER çıktısında Belge Yönetimi belgelerini (eklerini) kullanmak amacıyla bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="ffaba-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="ffaba-106">Bu adımlar DEMF şirketinde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="ffaba-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="ffaba-107">Bu adımları tamamlamak için öncelikle "ER Biçim çıktılarında Belge Yönetimi dosyalarını kullanma (Bölüm 4: Biçimi çalıştırma)" yordamındaki adımları tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="ffaba-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 4: Run format)" procedure.</span></span>

<span data-ttu-id="ffaba-108">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="ffaba-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="ffaba-109">Ekleri oluşturulan iletilere ikili biçimde doldurmak için biçimi değiştirin</span><span class="sxs-lookup"><span data-stu-id="ffaba-109">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="ffaba-110">Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="ffaba-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="ffaba-111">Ağaçta "Müşteri fatura modeli" seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="ffaba-111">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="ffaba-112">Ağaçta, "Müşteri faturası modeli\Müşteri faturası modeli (özel)"i genişletin.</span><span class="sxs-lookup"><span data-stu-id="ffaba-112">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="ffaba-113">Ağaçta, "Müşteri faturası modeli\Müşteri faturası modeli (özel)\Elektronik fatura örnek iletisi"ni seçin.</span><span class="sxs-lookup"><span data-stu-id="ffaba-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="ffaba-114">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ffaba-114">Click Designer.</span></span>
    * <span data-ttu-id="ffaba-115">UNICODE kodlaması kullanarak XML dosyası olarak oluşturulan çıktıda fatura iletisini doldurun.</span><span class="sxs-lookup"><span data-stu-id="ffaba-115">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="ffaba-116">İletişim kutusunu açmak için Kök ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ffaba-116">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="ffaba-117">Ağaçta seçin 'Common\File'.</span><span class="sxs-lookup"><span data-stu-id="ffaba-117">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="ffaba-118">Ad alanında, "Xml iletisi" yazın.</span><span class="sxs-lookup"><span data-stu-id="ffaba-118">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="ffaba-119">Xml iletisi</span><span class="sxs-lookup"><span data-stu-id="ffaba-119">Xml message</span></span>  
9. <span data-ttu-id="ffaba-120">Kodlama alanına 'UTF-8' yazın.</span><span class="sxs-lookup"><span data-stu-id="ffaba-120">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="ffaba-121">UTF-8</span><span class="sxs-lookup"><span data-stu-id="ffaba-121">UTF-8</span></span>  
10. <span data-ttu-id="ffaba-122">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ffaba-122">Click OK.</span></span>
    * <span data-ttu-id="ffaba-123">Oluşturulan çıktıyı sıkıştırılmış bir dosya olarak yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="ffaba-123">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="ffaba-124">İletişim kutusunu açmak için Kök ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ffaba-124">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="ffaba-125">Ağaçta, "Ortak\Klasör"ü seçin.</span><span class="sxs-lookup"><span data-stu-id="ffaba-125">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="ffaba-126">Ad alanına "Zip çıktısı" yazın.</span><span class="sxs-lookup"><span data-stu-id="ffaba-126">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="ffaba-127">Zip çıktısı</span><span class="sxs-lookup"><span data-stu-id="ffaba-127">Zip output</span></span>  
14. <span data-ttu-id="ffaba-128">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ffaba-128">Click OK.</span></span>
15. <span data-ttu-id="ffaba-129">Ağaçta, "Zip çıktısı" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ffaba-129">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="ffaba-130">Oluşturulan sıkıştırılmış dosyaya ekleri orijinal adları ve uzantıları ile dosyalar olarak ekleyin.</span><span class="sxs-lookup"><span data-stu-id="ffaba-130">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="ffaba-131">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ffaba-131">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="ffaba-132">Ağaçta seçin 'Common\File'.</span><span class="sxs-lookup"><span data-stu-id="ffaba-132">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="ffaba-133">Ad alanına "Ekli dosya" yazın.</span><span class="sxs-lookup"><span data-stu-id="ffaba-133">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="ffaba-134">Ekli dosya</span><span class="sxs-lookup"><span data-stu-id="ffaba-134">Attached file</span></span>  
19. <span data-ttu-id="ffaba-135">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ffaba-135">Click OK.</span></span>
20. <span data-ttu-id="ffaba-136">Ağaçta, "Zip çıktısı\Ekli dosya" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ffaba-136">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="ffaba-137">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ffaba-137">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="ffaba-138">Ağaçta, "Metin\Base64" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ffaba-138">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="ffaba-139">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ffaba-139">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="ffaba-140">Veri modeline yeni biçim öğeleri eşleme</span><span class="sxs-lookup"><span data-stu-id="ffaba-140">Map new format elements to data model</span></span>
1. <span data-ttu-id="ffaba-141">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ffaba-141">Click the Mapping tab.</span></span>
2. <span data-ttu-id="ffaba-142">Ağaçta, 'model'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="ffaba-142">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="ffaba-143">Ağaçta, "model\Fatura ekleri" seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="ffaba-143">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="ffaba-144">Ağaçta, "Zip çıktısı\Ekli dosya\Base64" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ffaba-144">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="ffaba-145">Ağaçta, "model\Fatura ekleri\Dosya içeriği" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ffaba-145">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="ffaba-146">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ffaba-146">Click Bind.</span></span>
7. <span data-ttu-id="ffaba-147">Ağaçta, "Zip çıktısı\Ekli dosya" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ffaba-147">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="ffaba-148">Dosya adını düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ffaba-148">Click Edit filename.</span></span>
9. <span data-ttu-id="ffaba-149">Ağaçta, 'model'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="ffaba-149">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="ffaba-150">Ağaçta, "model\Fatura ekleri" seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="ffaba-150">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="ffaba-151">Ağaçta "model\Fatura ekleri\Dosya adı" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ffaba-151">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="ffaba-152">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ffaba-152">Click Add data source.</span></span>
13. <span data-ttu-id="ffaba-153">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ffaba-153">Click Save.</span></span>
14. <span data-ttu-id="ffaba-154">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ffaba-154">Close the page.</span></span>
15. <span data-ttu-id="ffaba-155">Ağaçta, "model\Fatura ekleri" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ffaba-155">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="ffaba-156">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ffaba-156">Click Bind.</span></span>
17. <span data-ttu-id="ffaba-157">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ffaba-157">Click Save.</span></span>
18. <span data-ttu-id="ffaba-158">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ffaba-158">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="ffaba-159">Seçili fatura için tasarlanan raporu çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ffaba-159">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="ffaba-160">Çalıştır öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ffaba-160">Click Run.</span></span>
2. <span data-ttu-id="ffaba-161">Eklenecek kayıtlar () bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="ffaba-161">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="ffaba-162">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ffaba-162">Click Filter.</span></span>
4. <span data-ttu-id="ffaba-163">Müşteri fatura günlüğü satırını ve Satış siparişi alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="ffaba-163">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="ffaba-164">Ölçütler alanında "Satış siparişi" alanına 000148 no.lu sipariş numarasını yazın.</span><span class="sxs-lookup"><span data-stu-id="ffaba-164">In the Criteria field, In the criteria "Sales order" field, type the order number 000148.</span></span>
    * <span data-ttu-id="ffaba-165">000148</span><span class="sxs-lookup"><span data-stu-id="ffaba-165">000148</span></span>  
6. <span data-ttu-id="ffaba-166">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ffaba-166">Click OK.</span></span>
7. <span data-ttu-id="ffaba-167">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ffaba-167">Click OK.</span></span>
    * <span data-ttu-id="ffaba-168">Ortaya çıkan sonucu inceleyin.</span><span class="sxs-lookup"><span data-stu-id="ffaba-168">Review the generated output.</span></span> <span data-ttu-id="ffaba-169">XML biçimindeki fatura iletisine ek olarak her bir ek için tek bir dosya oluşturulduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="ffaba-169">Note,that in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="ffaba-170">Ek dosyaları ikili biçimde sıkıştırılmış çıktı ile doldurulur.</span><span class="sxs-lookup"><span data-stu-id="ffaba-170">The attachment files are populated with the zipped output in binary format.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]