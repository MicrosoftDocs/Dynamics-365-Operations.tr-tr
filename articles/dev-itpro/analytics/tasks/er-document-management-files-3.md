--- 
title: "ER çıktısında Belge Yönetimi dosyalarını kullanmak için biçimler oluşturma"
description: "Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının, ER çıktısında Belge Yönetimi belgelerini kullanmak amacıyla bir Elektronik raporlama biçimini nasıl yapılandırabileceğini açıklar."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 1815a0004eee6734b3c7d2c2f9e75ce5fe16af1c
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2018

---

# <a name="create-formats-to-use-document-management-files-in-er-output"></a><span data-ttu-id="1015e-103">ER çıktısında Belge Yönetimi dosyalarını kullanmak için biçimler oluşturma</span><span class="sxs-lookup"><span data-stu-id="1015e-103">Create formats to use Document Management files in ER output</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1015e-104">Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının, ER çıktısında Belge Yönetimi belgelerini (eklerini) kullanmak amacıyla bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="1015e-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="1015e-105">Bu adımlar tüm şirketlerde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="1015e-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="1015e-106">Bu adımları tamamlamak için öncelikle "ER Biçim çıktılarında Belge Yönetimi dosyalarını kullanma (Bölüm 2: Veri modelini genişletme" yordamındaki adımları tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="1015e-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 2: Extend data model” procedure.</span></span>

<span data-ttu-id="1015e-107">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="1015e-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="1015e-108">Faturaları işlemek için bir biçim oluşturma</span><span class="sxs-lookup"><span data-stu-id="1015e-108">Create a format to process invoices</span></span>
1. <span data-ttu-id="1015e-109">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="1015e-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="1015e-110">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1015e-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="1015e-111">Ağaçta "Müşteri fatura modeli" seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="1015e-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="1015e-112">Ağaçta, "Müşteri faturası modeli\Müşteri faturası modeli (özel)" seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="1015e-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="1015e-113">Faturayı elektronik işlemeyle ilgili bir satış siparişine eklenmiş her türlü dosya hakkındaki bilgilerle elektronik iletiler oluşturmak için bir biçim oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="1015e-113">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="1015e-114">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1015e-114">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="1015e-115">Yeni alanına, "Müşteri faturası modeli (özel) veri modeline bağlı biçim" yazın.</span><span class="sxs-lookup"><span data-stu-id="1015e-115">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="1015e-116">Ad alanına "Elektronik fatura örnek iletisi" yazın.</span><span class="sxs-lookup"><span data-stu-id="1015e-116">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="1015e-117">Elektronik fatura örnek iletisi</span><span class="sxs-lookup"><span data-stu-id="1015e-117">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="1015e-118">Veri modeli tanımı alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="1015e-118">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="1015e-119">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="1015e-119">InvoiceCustomer</span></span>  
9. <span data-ttu-id="1015e-120">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1015e-120">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="1015e-121">Ekleri oluşturulan iletiye MIME biçiminde doldurmak için bir biçim tasarlama</span><span class="sxs-lookup"><span data-stu-id="1015e-121">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="1015e-122">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1015e-122">Click Designer.</span></span>
2. <span data-ttu-id="1015e-123">İletişim kutusunu açmak için Kök ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1015e-123">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="1015e-124">Ağaçta seçin 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="1015e-124">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="1015e-125">Ad alanına "Fatura" yazın.</span><span class="sxs-lookup"><span data-stu-id="1015e-125">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="1015e-126">Fatura</span><span class="sxs-lookup"><span data-stu-id="1015e-126">Invoice</span></span>  
5. <span data-ttu-id="1015e-127">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1015e-127">Click OK.</span></span>
6. <span data-ttu-id="1015e-128">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1015e-128">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="1015e-129">Ağaçta seçin 'XML\Attribute'.</span><span class="sxs-lookup"><span data-stu-id="1015e-129">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="1015e-130">Ad alanına "SalesOrder" yazın.</span><span class="sxs-lookup"><span data-stu-id="1015e-130">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="1015e-131">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="1015e-131">SalesOrder</span></span>  
9. <span data-ttu-id="1015e-132">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1015e-132">Click OK.</span></span>
10. <span data-ttu-id="1015e-133">Öznitelik Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1015e-133">Click Add Attribute.</span></span>
11. <span data-ttu-id="1015e-134">Ad alanına "InvoiceNumber" yazın.</span><span class="sxs-lookup"><span data-stu-id="1015e-134">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="1015e-135">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="1015e-135">InvoiceNumber</span></span>  
12. <span data-ttu-id="1015e-136">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1015e-136">Click OK.</span></span>
13. <span data-ttu-id="1015e-137">Öznitelik Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1015e-137">Click Add Attribute.</span></span>
14. <span data-ttu-id="1015e-138">Ad alanına "InvoiceAmount" yazın.</span><span class="sxs-lookup"><span data-stu-id="1015e-138">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="1015e-139">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="1015e-139">InvoiceAmount</span></span>  
15. <span data-ttu-id="1015e-140">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1015e-140">Click OK.</span></span>
16. <span data-ttu-id="1015e-141">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1015e-141">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="1015e-142">Ağaçta seçin 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="1015e-142">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="1015e-143">Ad alanına "EnclosedDocs" yazın.</span><span class="sxs-lookup"><span data-stu-id="1015e-143">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="1015e-144">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="1015e-144">EnclosedDocs</span></span>  
19. <span data-ttu-id="1015e-145">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1015e-145">Click OK.</span></span>
20. <span data-ttu-id="1015e-146">Ağaçta, "Fatura\EnclosedDocs" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1015e-146">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="1015e-147">Öğe Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1015e-147">Click Add Element.</span></span>
22. <span data-ttu-id="1015e-148">Ad alanına "Belge" yazın.</span><span class="sxs-lookup"><span data-stu-id="1015e-148">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="1015e-149">Belge</span><span class="sxs-lookup"><span data-stu-id="1015e-149">Document</span></span>  
23. <span data-ttu-id="1015e-150">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1015e-150">Click OK.</span></span>
24. <span data-ttu-id="1015e-151">Ağaçta, "Fatura\EnclosedDocs\Belge" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1015e-151">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="1015e-152">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1015e-152">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="1015e-153">Ağaçta seçin 'XML\Attribute'.</span><span class="sxs-lookup"><span data-stu-id="1015e-153">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="1015e-154">Ad alanına "FileName" yazın.</span><span class="sxs-lookup"><span data-stu-id="1015e-154">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="1015e-155">FileName</span><span class="sxs-lookup"><span data-stu-id="1015e-155">FileName</span></span>  
28. <span data-ttu-id="1015e-156">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1015e-156">Click OK.</span></span>
29. <span data-ttu-id="1015e-157">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1015e-157">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="1015e-158">Ağaçta seçin 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="1015e-158">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="1015e-159">Ad alanına "FileContent" yazın.</span><span class="sxs-lookup"><span data-stu-id="1015e-159">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="1015e-160">FileContent</span><span class="sxs-lookup"><span data-stu-id="1015e-160">FileContent</span></span>  
32. <span data-ttu-id="1015e-161">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1015e-161">Click OK.</span></span>
33. <span data-ttu-id="1015e-162">Ağaçta, "Fatura\EnclosedDocs\Belgeler\FileContent" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1015e-162">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="1015e-163">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1015e-163">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="1015e-164">Ağaçta, "Metin\Base64" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1015e-164">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="1015e-165">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1015e-165">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="1015e-166">Veri kaynağı olarak veri modeline biçim öğelerini eşleme</span><span class="sxs-lookup"><span data-stu-id="1015e-166">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="1015e-167">Ağaçta, "Fatura\SalesOrder" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1015e-167">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="1015e-168">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1015e-168">Click the Mapping tab.</span></span>
3. <span data-ttu-id="1015e-169">Ağaçta, 'model'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="1015e-169">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="1015e-170">Ağaçta, "model\Satış siparişi numarası(SalesId)" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1015e-170">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="1015e-171">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1015e-171">Click Bind.</span></span>
6. <span data-ttu-id="1015e-172">Ağaçta, "Fatura\InvoiceNumber" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1015e-172">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="1015e-173">Ağaçta, "model\Temel fatura(InvoiceBase)" seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="1015e-173">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="1015e-174">Ağaçta, "model\Temel fatura(InvoiceBase)\Fatura numarası(Id)" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1015e-174">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="1015e-175">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1015e-175">Click Bind.</span></span>
10. <span data-ttu-id="1015e-176">Ağaçta, "Fatura\InvoiceAmount" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1015e-176">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="1015e-177">Ağaçta, "model\Temel fatura(InvoiceBase)\Fatura tutarı(Tutar)" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1015e-177">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="1015e-178">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1015e-178">Click Bind.</span></span>
13. <span data-ttu-id="1015e-179">Ağaçta, "model\Fatura ekleri" seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="1015e-179">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="1015e-180">Ağaçta, "model\Fatura ekleri\Dosya içeriği" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1015e-180">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="1015e-181">Ağaçta, "Fatura\EnclosedDocs\Belge\FileContent\Base64" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1015e-181">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="1015e-182">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1015e-182">Click Bind.</span></span>
17. <span data-ttu-id="1015e-183">Ağaçta "model\Fatura ekleri\Dosya adı" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1015e-183">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="1015e-184">Ağaçta, "Fatura\EnclosedDocs\Belgeler\FileName" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1015e-184">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="1015e-185">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1015e-185">Click Bind.</span></span>
20. <span data-ttu-id="1015e-186">Ağaçta, "model\Fatura ekleri" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1015e-186">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="1015e-187">Ağaçta, "Fatura\EnclosedDocs\Belge" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="1015e-187">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="1015e-188">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1015e-188">Click Bind.</span></span>
23. <span data-ttu-id="1015e-189">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1015e-189">Click Save.</span></span>
24. <span data-ttu-id="1015e-190">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="1015e-190">Close the page.</span></span>


