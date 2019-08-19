---
title: ER çıktısında Belge Yönetimi dosyalarını kullanmak için biçimler oluşturma
description: Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının, ER çıktısında Belge Yönetimi belgelerini kullanmak amacıyla bir Elektronik raporlama biçimini nasıl yapılandırabileceğini açıklar.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 05c0c4a38f34774e7018504c5e3fab834a2ec1b1
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850291"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3-create-format"></a><span data-ttu-id="bc612-103">ER Biçim çıktılarında Belge Yönetimi dosyalarını kullanma (Bölüm 3: Biçimi oluşturma)</span><span class="sxs-lookup"><span data-stu-id="bc612-103">ER Use Document Management files in format outputs (Part 3: Create format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bc612-104">Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının, ER çıktısında Belge Yönetimi belgelerini (eklerini) kullanmak amacıyla bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="bc612-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="bc612-105">Bu adımlar tüm şirketlerde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="bc612-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="bc612-106">Bu adımları tamamlamak için öncelikle "ER Biçim çıktılarında Belge Yönetimi dosyalarını kullanma (Bölüm 2: Veri modelini genişletme" yordamındaki adımları tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="bc612-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 2: Extend data model” procedure.</span></span>

<span data-ttu-id="bc612-107">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="bc612-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="bc612-108">Faturaları işlemek için bir biçim oluşturma</span><span class="sxs-lookup"><span data-stu-id="bc612-108">Create a format to process invoices</span></span>
1. <span data-ttu-id="bc612-109">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="bc612-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="bc612-110">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bc612-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="bc612-111">Ağaçta "Müşteri fatura modeli" seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="bc612-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="bc612-112">Ağaçta, "Müşteri faturası modeli\Müşteri faturası modeli (özel)" seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="bc612-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="bc612-113">Faturayı elektronik işlemeyle ilgili bir satış siparişine eklenmiş her türlü dosya hakkındaki bilgilerle elektronik iletiler oluşturmak için bir biçim oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="bc612-113">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="bc612-114">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bc612-114">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="bc612-115">Yeni alanına, "Müşteri faturası modeli (özel) veri modeline bağlı biçim" yazın.</span><span class="sxs-lookup"><span data-stu-id="bc612-115">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="bc612-116">Ad alanına "Elektronik fatura örnek iletisi" yazın.</span><span class="sxs-lookup"><span data-stu-id="bc612-116">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="bc612-117">Elektronik fatura örnek iletisi</span><span class="sxs-lookup"><span data-stu-id="bc612-117">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="bc612-118">Veri modeli tanımı alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="bc612-118">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="bc612-119">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="bc612-119">InvoiceCustomer</span></span>  
9. <span data-ttu-id="bc612-120">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bc612-120">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="bc612-121">Ekleri oluşturulan iletiye MIME biçiminde doldurmak için bir biçim tasarlama</span><span class="sxs-lookup"><span data-stu-id="bc612-121">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="bc612-122">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bc612-122">Click Designer.</span></span>
2. <span data-ttu-id="bc612-123">İletişim kutusunu açmak için Kök ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bc612-123">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="bc612-124">Ağaçta seçin 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="bc612-124">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="bc612-125">Ad alanına "Fatura" yazın.</span><span class="sxs-lookup"><span data-stu-id="bc612-125">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="bc612-126">Fatura</span><span class="sxs-lookup"><span data-stu-id="bc612-126">Invoice</span></span>  
5. <span data-ttu-id="bc612-127">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bc612-127">Click OK.</span></span>
6. <span data-ttu-id="bc612-128">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bc612-128">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="bc612-129">Ağaçta seçin 'XML\Attribute'.</span><span class="sxs-lookup"><span data-stu-id="bc612-129">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="bc612-130">Ad alanına "SalesOrder" yazın.</span><span class="sxs-lookup"><span data-stu-id="bc612-130">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="bc612-131">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="bc612-131">SalesOrder</span></span>  
9. <span data-ttu-id="bc612-132">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bc612-132">Click OK.</span></span>
10. <span data-ttu-id="bc612-133">Öznitelik Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bc612-133">Click Add Attribute.</span></span>
11. <span data-ttu-id="bc612-134">Ad alanına "InvoiceNumber" yazın.</span><span class="sxs-lookup"><span data-stu-id="bc612-134">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="bc612-135">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="bc612-135">InvoiceNumber</span></span>  
12. <span data-ttu-id="bc612-136">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bc612-136">Click OK.</span></span>
13. <span data-ttu-id="bc612-137">Öznitelik Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bc612-137">Click Add Attribute.</span></span>
14. <span data-ttu-id="bc612-138">Ad alanına "InvoiceAmount" yazın.</span><span class="sxs-lookup"><span data-stu-id="bc612-138">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="bc612-139">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="bc612-139">InvoiceAmount</span></span>  
15. <span data-ttu-id="bc612-140">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bc612-140">Click OK.</span></span>
16. <span data-ttu-id="bc612-141">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bc612-141">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="bc612-142">Ağaçta seçin 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="bc612-142">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="bc612-143">Ad alanına "EnclosedDocs" yazın.</span><span class="sxs-lookup"><span data-stu-id="bc612-143">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="bc612-144">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="bc612-144">EnclosedDocs</span></span>  
19. <span data-ttu-id="bc612-145">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bc612-145">Click OK.</span></span>
20. <span data-ttu-id="bc612-146">Ağaçta, "Fatura\EnclosedDocs" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bc612-146">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="bc612-147">Öğe Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bc612-147">Click Add Element.</span></span>
22. <span data-ttu-id="bc612-148">Ad alanına "Belge" yazın.</span><span class="sxs-lookup"><span data-stu-id="bc612-148">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="bc612-149">Belge</span><span class="sxs-lookup"><span data-stu-id="bc612-149">Document</span></span>  
23. <span data-ttu-id="bc612-150">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bc612-150">Click OK.</span></span>
24. <span data-ttu-id="bc612-151">Ağaçta, "Fatura\EnclosedDocs\Belge" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bc612-151">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="bc612-152">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bc612-152">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="bc612-153">Ağaçta seçin 'XML\Attribute'.</span><span class="sxs-lookup"><span data-stu-id="bc612-153">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="bc612-154">Ad alanına "FileName" yazın.</span><span class="sxs-lookup"><span data-stu-id="bc612-154">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="bc612-155">FileName</span><span class="sxs-lookup"><span data-stu-id="bc612-155">FileName</span></span>  
28. <span data-ttu-id="bc612-156">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bc612-156">Click OK.</span></span>
29. <span data-ttu-id="bc612-157">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bc612-157">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="bc612-158">Ağaçta seçin 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="bc612-158">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="bc612-159">Ad alanına "FileContent" yazın.</span><span class="sxs-lookup"><span data-stu-id="bc612-159">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="bc612-160">FileContent</span><span class="sxs-lookup"><span data-stu-id="bc612-160">FileContent</span></span>  
32. <span data-ttu-id="bc612-161">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bc612-161">Click OK.</span></span>
33. <span data-ttu-id="bc612-162">Ağaçta, "Fatura\EnclosedDocs\Belgeler\FileContent" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bc612-162">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="bc612-163">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bc612-163">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="bc612-164">Ağaçta, "Metin\Base64" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bc612-164">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="bc612-165">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bc612-165">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="bc612-166">Veri kaynağı olarak veri modeline biçim öğelerini eşleme</span><span class="sxs-lookup"><span data-stu-id="bc612-166">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="bc612-167">Ağaçta, "Fatura\SalesOrder" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bc612-167">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="bc612-168">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bc612-168">Click the Mapping tab.</span></span>
3. <span data-ttu-id="bc612-169">Ağaçta, 'model'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="bc612-169">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="bc612-170">Ağaçta, "model\Satış siparişi numarası(SalesId)" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bc612-170">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="bc612-171">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bc612-171">Click Bind.</span></span>
6. <span data-ttu-id="bc612-172">Ağaçta, "Fatura\InvoiceNumber" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bc612-172">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="bc612-173">Ağaçta, "model\Temel fatura(InvoiceBase)" seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="bc612-173">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="bc612-174">Ağaçta, "model\Temel fatura(InvoiceBase)\Fatura numarası(Id)" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bc612-174">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="bc612-175">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bc612-175">Click Bind.</span></span>
10. <span data-ttu-id="bc612-176">Ağaçta, "Fatura\InvoiceAmount" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bc612-176">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="bc612-177">Ağaçta, "model\Temel fatura(InvoiceBase)\Fatura tutarı(Tutar)" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bc612-177">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="bc612-178">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bc612-178">Click Bind.</span></span>
13. <span data-ttu-id="bc612-179">Ağaçta, "model\Fatura ekleri" seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="bc612-179">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="bc612-180">Ağaçta, "model\Fatura ekleri\Dosya içeriği" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bc612-180">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="bc612-181">Ağaçta, "Fatura\EnclosedDocs\Belge\FileContent\Base64" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bc612-181">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="bc612-182">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bc612-182">Click Bind.</span></span>
17. <span data-ttu-id="bc612-183">Ağaçta "model\Fatura ekleri\Dosya adı" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bc612-183">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="bc612-184">Ağaçta, "Fatura\EnclosedDocs\Belgeler\FileName" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bc612-184">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="bc612-185">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bc612-185">Click Bind.</span></span>
20. <span data-ttu-id="bc612-186">Ağaçta, "model\Fatura ekleri" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bc612-186">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="bc612-187">Ağaçta, "Fatura\EnclosedDocs\Belge" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bc612-187">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="bc612-188">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bc612-188">Click Bind.</span></span>
23. <span data-ttu-id="bc612-189">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bc612-189">Click Save.</span></span>
24. <span data-ttu-id="bc612-190">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="bc612-190">Close the page.</span></span>

