--- 
title: "Elektronik raporlama (ER) için biçim çıktılarında Belge Yönetimi dosyalarını kullanmak üzere biçimi değiştirme ve çalıştırma"
description: "Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının, ER çıktısında Belge Yönetimi belgelerini (eklerini) kullanmak amacıyla bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar."
author: NickSelin
manager: AnnBe
ms.date: 10/31/2016
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 76915a7294e078d76ed3ca9c41755e12b0791f3c
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="modify-and-run-format-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a><span data-ttu-id="1cc60-103">Elektronik raporlama (ER) için biçim çıktılarında Belge Yönetimi dosyalarını kullanmak üzere biçimi değiştirme ve çalıştırma</span><span class="sxs-lookup"><span data-stu-id="1cc60-103">Modify and run format to use Document Management files in format outputs for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1cc60-104">Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının, ER çıktısında Belge Yönetimi belgelerini (eklerini) kullanmak amacıyla bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="1cc60-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="1cc60-105">Bu adımlar DEMF şirketinde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="1cc60-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="1cc60-106">Bu adımları tamamlamak için öncelikle "ER Biçim çıktılarında Belge Yönetimi dosyalarını kullanma (Bölüm 4): Biçimi çalıştırma" yordamındaki adımları tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="1cc60-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 4): Run format” procedure.</span></span>

<span data-ttu-id="1cc60-107">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="1cc60-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="1cc60-108">Ekleri oluşturulan iletilere ikili biçimde doldurmak için biçimi değiştirin</span><span class="sxs-lookup"><span data-stu-id="1cc60-108">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="1cc60-109">Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="1cc60-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="1cc60-110">Ağaçta "Müşteri fatura modeli" seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="1cc60-110">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="1cc60-111">Ağaçta, "Müşteri faturası modeli\Müşteri faturası modeli (özel)"i genişletin.</span><span class="sxs-lookup"><span data-stu-id="1cc60-111">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="1cc60-112">Ağaçta, "Müşteri faturası modeli\Müşteri faturası modeli (özel)\Elektronik fatura örnek iletisi"ni seçin.</span><span class="sxs-lookup"><span data-stu-id="1cc60-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="1cc60-113">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1cc60-113">Click Designer.</span></span>
    * <span data-ttu-id="1cc60-114">UNICODE kodlaması kullanarak XML dosyası olarak oluşturulan çıktıda fatura iletisini doldurun.</span><span class="sxs-lookup"><span data-stu-id="1cc60-114">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="1cc60-115">İletişim kutusunu açmak için Kök ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1cc60-115">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="1cc60-116">Ağaçta seçin 'Common\File'.</span><span class="sxs-lookup"><span data-stu-id="1cc60-116">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="1cc60-117">Ad alanında, "Xml iletisi" yazın.</span><span class="sxs-lookup"><span data-stu-id="1cc60-117">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="1cc60-118">Xml iletisi</span><span class="sxs-lookup"><span data-stu-id="1cc60-118">Xml message</span></span>  
9. <span data-ttu-id="1cc60-119">Kodlama alanına 'UTF-8' yazın.</span><span class="sxs-lookup"><span data-stu-id="1cc60-119">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="1cc60-120">UTF-8</span><span class="sxs-lookup"><span data-stu-id="1cc60-120">UTF-8</span></span>  
10. <span data-ttu-id="1cc60-121">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1cc60-121">Click OK.</span></span>
    * <span data-ttu-id="1cc60-122">Oluşturulan çıktıyı sıkıştırılmış bir dosya olarak yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="1cc60-122">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="1cc60-123">İletişim kutusunu açmak için Kök ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1cc60-123">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="1cc60-124">Ağaçta, "Ortak\Klasör"ü seçin.</span><span class="sxs-lookup"><span data-stu-id="1cc60-124">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="1cc60-125">Ad alanına "Zip çıktısı" yazın.</span><span class="sxs-lookup"><span data-stu-id="1cc60-125">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="1cc60-126">Zip çıktısı</span><span class="sxs-lookup"><span data-stu-id="1cc60-126">Zip output</span></span>  
14. <span data-ttu-id="1cc60-127">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1cc60-127">Click OK.</span></span>
15. <span data-ttu-id="1cc60-128">Ağaçta, "Zip çıktısı" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1cc60-128">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="1cc60-129">Oluşturulan sıkıştırılmış dosyaya ekleri orijinal adları ve uzantıları ile dosyalar olarak ekleyin.</span><span class="sxs-lookup"><span data-stu-id="1cc60-129">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="1cc60-130">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1cc60-130">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="1cc60-131">Ağaçta seçin 'Common\File'.</span><span class="sxs-lookup"><span data-stu-id="1cc60-131">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="1cc60-132">Ad alanına "Ekli dosya" yazın.</span><span class="sxs-lookup"><span data-stu-id="1cc60-132">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="1cc60-133">Ekli dosya</span><span class="sxs-lookup"><span data-stu-id="1cc60-133">Attached file</span></span>  
19. <span data-ttu-id="1cc60-134">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1cc60-134">Click OK.</span></span>
20. <span data-ttu-id="1cc60-135">Ağaçta, "Zip çıktısı\Ekli dosya" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1cc60-135">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="1cc60-136">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1cc60-136">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="1cc60-137">Ağaçta, "Metin\Base64" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1cc60-137">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="1cc60-138">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1cc60-138">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="1cc60-139">Veri modeline yeni biçim öğeleri eşleme</span><span class="sxs-lookup"><span data-stu-id="1cc60-139">Map new format elements to data model</span></span>
1. <span data-ttu-id="1cc60-140">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1cc60-140">Click the Mapping tab.</span></span>
2. <span data-ttu-id="1cc60-141">Ağaçta, 'model'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="1cc60-141">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="1cc60-142">Ağaçta, "model\Fatura ekleri" seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="1cc60-142">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="1cc60-143">Ağaçta, "Zip çıktısı\Ekli dosya\Base64" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1cc60-143">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="1cc60-144">Ağaçta, "model\Fatura ekleri\Dosya içeriği" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1cc60-144">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="1cc60-145">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1cc60-145">Click Bind.</span></span>
7. <span data-ttu-id="1cc60-146">Ağaçta, "Zip çıktısı\Ekli dosya" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1cc60-146">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="1cc60-147">Dosya adını düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1cc60-147">Click Edit filename.</span></span>
9. <span data-ttu-id="1cc60-148">Ağaçta, 'model'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="1cc60-148">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="1cc60-149">Ağaçta, "model\Fatura ekleri" seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="1cc60-149">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="1cc60-150">Ağaçta "model\Fatura ekleri\Dosya adı" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1cc60-150">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="1cc60-151">Veri kaynağı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1cc60-151">Click Add data source.</span></span>
13. <span data-ttu-id="1cc60-152">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1cc60-152">Click Save.</span></span>
14. <span data-ttu-id="1cc60-153">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="1cc60-153">Close the page.</span></span>
15. <span data-ttu-id="1cc60-154">Ağaçta, "model\Fatura ekleri" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1cc60-154">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="1cc60-155">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1cc60-155">Click Bind.</span></span>
17. <span data-ttu-id="1cc60-156">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1cc60-156">Click Save.</span></span>
18. <span data-ttu-id="1cc60-157">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="1cc60-157">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="1cc60-158">Seçili fatura için tasarlanan raporu çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1cc60-158">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="1cc60-159">Çalıştır öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1cc60-159">Click Run.</span></span>
2. <span data-ttu-id="1cc60-160">Eklenecek kayıtlar () bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="1cc60-160">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="1cc60-161">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1cc60-161">Click Filter.</span></span>
4. <span data-ttu-id="1cc60-162">Müşteri fatura günlüğü satırını ve Satış siparişi alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="1cc60-162">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="1cc60-163">Ölçütler alanında "Satış siparişi" alanına 000148 no.lu sipariş numarasını yazın.</span><span class="sxs-lookup"><span data-stu-id="1cc60-163">In the Criteria field, In the criteria “Sales order” field, type the order number 000148.</span></span>
    * <span data-ttu-id="1cc60-164">000148</span><span class="sxs-lookup"><span data-stu-id="1cc60-164">000148</span></span>  
6. <span data-ttu-id="1cc60-165">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1cc60-165">Click OK.</span></span>
7. <span data-ttu-id="1cc60-166">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1cc60-166">Click OK.</span></span>
    * <span data-ttu-id="1cc60-167">Ortaya çıkan sonucu inceleyin.</span><span class="sxs-lookup"><span data-stu-id="1cc60-167">Review the generated output.</span></span> <span data-ttu-id="1cc60-168">XML biçimindeki fatura iletisine ek olarak her bir ek için tek bir dosya oluşturulduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="1cc60-168">Note,that in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="1cc60-169">Ek dosyaları ikili biçimde sıkıştırılmış çıktı ile doldurulur.</span><span class="sxs-lookup"><span data-stu-id="1cc60-169">The attachment files are populated with the zipped output in binary format.</span></span>  

