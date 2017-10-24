--- 
title: "Elektronik raporlama (ER) için biçim çıktılarında Belge Yönetimi dosyalarını kullanmak üzere biçimi oluşturma"
description: "Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının, ER çıktısında Belge Yönetimi belgelerini (eklerini) kullanmak amacıyla bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.openlocfilehash: 71e40351e8b54092d1bbcbc73c6da69073791b74
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="create-format-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a><span data-ttu-id="ae192-103">Elektronik raporlama (ER) için biçim çıktılarında Belge Yönetimi dosyalarını kullanmak üzere biçimi oluşturma</span><span class="sxs-lookup"><span data-stu-id="ae192-103">Create format to use Document Management files in format outputs for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ae192-104">Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının, ER çıktısında Belge Yönetimi belgelerini (eklerini) kullanmak amacıyla bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="ae192-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="ae192-105">Bu adımlar tüm şirketlerde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="ae192-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="ae192-106">Bu adımları tamamlamak için öncelikle "ER Biçim çıktılarında Belge Yönetimi dosyalarını kullanma (Bölüm 2: Veri modelini genişletme" yordamındaki adımları tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="ae192-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 2: Extend data model” procedure.</span></span>

<span data-ttu-id="ae192-107">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="ae192-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="ae192-108">Faturaları işlemek için bir biçim oluşturma</span><span class="sxs-lookup"><span data-stu-id="ae192-108">Create a format to process invoices</span></span>
1. <span data-ttu-id="ae192-109">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="ae192-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="ae192-110">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae192-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="ae192-111">Ağaçta "Müşteri fatura modeli" seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="ae192-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="ae192-112">Ağaçta, "Müşteri faturası modeli\Müşteri faturası modeli (özel)" seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="ae192-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="ae192-113">Faturayı elektronik işlemeyle ilgili bir satış siparişine eklenmiş her türlü dosya hakkındaki bilgilerle elektronik iletiler oluşturmak için bir biçim oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="ae192-113">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="ae192-114">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae192-114">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="ae192-115">Yeni alanına, "Müşteri faturası modeli (özel) veri modeline bağlı biçim" yazın.</span><span class="sxs-lookup"><span data-stu-id="ae192-115">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="ae192-116">Ad alanına "Elektronik fatura örnek iletisi" yazın.</span><span class="sxs-lookup"><span data-stu-id="ae192-116">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="ae192-117">Elektronik fatura örnek iletisi</span><span class="sxs-lookup"><span data-stu-id="ae192-117">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="ae192-118">Veri modeli tanımı alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="ae192-118">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="ae192-119">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="ae192-119">InvoiceCustomer</span></span>  
9. <span data-ttu-id="ae192-120">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ae192-120">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="ae192-121">Ekleri oluşturulan iletiye MIME biçiminde doldurmak için bir biçim tasarlama</span><span class="sxs-lookup"><span data-stu-id="ae192-121">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="ae192-122">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ae192-122">Click Designer.</span></span>
2. <span data-ttu-id="ae192-123">İletişim kutusunu açmak için Kök ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ae192-123">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="ae192-124">Ağaçta seçin 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="ae192-124">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="ae192-125">Ad alanına "Fatura" yazın.</span><span class="sxs-lookup"><span data-stu-id="ae192-125">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="ae192-126">Fatura</span><span class="sxs-lookup"><span data-stu-id="ae192-126">Invoice</span></span>  
5. <span data-ttu-id="ae192-127">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae192-127">Click OK.</span></span>
6. <span data-ttu-id="ae192-128">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ae192-128">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="ae192-129">Ağaçta seçin 'XML\Attribute'.</span><span class="sxs-lookup"><span data-stu-id="ae192-129">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="ae192-130">Ad alanına "SalesOrder" yazın.</span><span class="sxs-lookup"><span data-stu-id="ae192-130">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="ae192-131">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="ae192-131">SalesOrder</span></span>  
9. <span data-ttu-id="ae192-132">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae192-132">Click OK.</span></span>
10. <span data-ttu-id="ae192-133">Öznitelik Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae192-133">Click Add Attribute.</span></span>
11. <span data-ttu-id="ae192-134">Ad alanına "InvoiceNumber" yazın.</span><span class="sxs-lookup"><span data-stu-id="ae192-134">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="ae192-135">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="ae192-135">InvoiceNumber</span></span>  
12. <span data-ttu-id="ae192-136">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae192-136">Click OK.</span></span>
13. <span data-ttu-id="ae192-137">Öznitelik Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae192-137">Click Add Attribute.</span></span>
14. <span data-ttu-id="ae192-138">Ad alanına "InvoiceAmount" yazın.</span><span class="sxs-lookup"><span data-stu-id="ae192-138">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="ae192-139">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="ae192-139">InvoiceAmount</span></span>  
15. <span data-ttu-id="ae192-140">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae192-140">Click OK.</span></span>
16. <span data-ttu-id="ae192-141">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ae192-141">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="ae192-142">Ağaçta seçin 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="ae192-142">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="ae192-143">Ad alanına "EnclosedDocs" yazın.</span><span class="sxs-lookup"><span data-stu-id="ae192-143">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="ae192-144">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="ae192-144">EnclosedDocs</span></span>  
19. <span data-ttu-id="ae192-145">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae192-145">Click OK.</span></span>
20. <span data-ttu-id="ae192-146">Ağaçta, "Fatura\EnclosedDocs" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ae192-146">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="ae192-147">Öğe Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae192-147">Click Add Element.</span></span>
22. <span data-ttu-id="ae192-148">Ad alanına "Belge" yazın.</span><span class="sxs-lookup"><span data-stu-id="ae192-148">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="ae192-149">Belge</span><span class="sxs-lookup"><span data-stu-id="ae192-149">Document</span></span>  
23. <span data-ttu-id="ae192-150">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae192-150">Click OK.</span></span>
24. <span data-ttu-id="ae192-151">Ağaçta, "Fatura\EnclosedDocs\Belge" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ae192-151">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="ae192-152">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ae192-152">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="ae192-153">Ağaçta seçin 'XML\Attribute'.</span><span class="sxs-lookup"><span data-stu-id="ae192-153">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="ae192-154">Ad alanına "FileName" yazın.</span><span class="sxs-lookup"><span data-stu-id="ae192-154">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="ae192-155">FileName</span><span class="sxs-lookup"><span data-stu-id="ae192-155">FileName</span></span>  
28. <span data-ttu-id="ae192-156">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae192-156">Click OK.</span></span>
29. <span data-ttu-id="ae192-157">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ae192-157">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="ae192-158">Ağaçta seçin 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="ae192-158">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="ae192-159">Ad alanına "FileContent" yazın.</span><span class="sxs-lookup"><span data-stu-id="ae192-159">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="ae192-160">FileContent</span><span class="sxs-lookup"><span data-stu-id="ae192-160">FileContent</span></span>  
32. <span data-ttu-id="ae192-161">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae192-161">Click OK.</span></span>
33. <span data-ttu-id="ae192-162">Ağaçta, "Fatura\EnclosedDocs\Belgeler\FileContent" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ae192-162">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="ae192-163">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ae192-163">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="ae192-164">Ağaçta, "Metin\Base64" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ae192-164">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="ae192-165">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae192-165">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="ae192-166">Veri kaynağı olarak veri modeline biçim öğelerini eşleme</span><span class="sxs-lookup"><span data-stu-id="ae192-166">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="ae192-167">Ağaçta, "Fatura\SalesOrder" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ae192-167">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="ae192-168">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ae192-168">Click the Mapping tab.</span></span>
3. <span data-ttu-id="ae192-169">Ağaçta, 'model'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="ae192-169">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="ae192-170">Ağaçta, "model\Satış siparişi numarası(SalesId)" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ae192-170">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="ae192-171">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae192-171">Click Bind.</span></span>
6. <span data-ttu-id="ae192-172">Ağaçta, "Fatura\InvoiceNumber" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ae192-172">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="ae192-173">Ağaçta, "model\Temel fatura(InvoiceBase)" seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="ae192-173">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="ae192-174">Ağaçta, "model\Temel fatura(InvoiceBase)\Fatura numarası(Id)" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ae192-174">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="ae192-175">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae192-175">Click Bind.</span></span>
10. <span data-ttu-id="ae192-176">Ağaçta, "Fatura\InvoiceAmount" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ae192-176">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="ae192-177">Ağaçta, "model\Temel fatura(InvoiceBase)\Fatura tutarı(Tutar)" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ae192-177">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="ae192-178">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae192-178">Click Bind.</span></span>
13. <span data-ttu-id="ae192-179">Ağaçta, "model\Fatura ekleri" seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="ae192-179">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="ae192-180">Ağaçta, "model\Fatura ekleri\Dosya içeriği" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ae192-180">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="ae192-181">Ağaçta, "Fatura\EnclosedDocs\Belge\FileContent\Base64" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ae192-181">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="ae192-182">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae192-182">Click Bind.</span></span>
17. <span data-ttu-id="ae192-183">Ağaçta "model\Fatura ekleri\Dosya adı" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ae192-183">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="ae192-184">Ağaçta, "Fatura\EnclosedDocs\Belgeler\FileName" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ae192-184">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="ae192-185">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae192-185">Click Bind.</span></span>
20. <span data-ttu-id="ae192-186">Ağaçta, "model\Fatura ekleri" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ae192-186">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="ae192-187">Ağaçta, "Fatura\EnclosedDocs\Belge" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ae192-187">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="ae192-188">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae192-188">Click Bind.</span></span>
23. <span data-ttu-id="ae192-189">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae192-189">Click Save.</span></span>
24. <span data-ttu-id="ae192-190">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ae192-190">Close the page.</span></span>


