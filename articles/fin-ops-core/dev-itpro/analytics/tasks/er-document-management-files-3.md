---
title: ER Biçim çıktılarında Belge Yönetimi dosyalarını kullanma (Bölüm 3 - Biçimi oluşturma)
description: Bu konuda, ER çıktılarında Belge Yönetimi dosyaları kullanmak üzere Elektronik raporlama biçiminin nasıl yapılandırılacağı açıklanmaktadır. (3. Bölüm)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1ec1ebc15cd980734aebec63d6758404868c1e36
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559761"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a><span data-ttu-id="ddbe9-104">ER Biçim çıktılarında Belge Yönetimi dosyalarını kullanma (Bölüm 3 - Biçimi oluşturma)</span><span class="sxs-lookup"><span data-stu-id="ddbe9-104">ER Use Document Management files in format outputs (Part 3 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ddbe9-105">Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının, ER çıktısında Belge Yönetimi belgelerini (eklerini) kullanmak amacıyla bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="ddbe9-106">Bu adımlar tüm şirketlerde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="ddbe9-107">Bu adımları tamamlamak için öncelikle "ER Biçim çıktılarında Belge Yönetimi dosyalarını kullanma (Bölüm 2: Veri modelini genişletme" yordamındaki adımları tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 2: Extend data model" procedure.</span></span>

<span data-ttu-id="ddbe9-108">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="ddbe9-109">Faturaları işlemek için bir biçim oluşturma</span><span class="sxs-lookup"><span data-stu-id="ddbe9-109">Create a format to process invoices</span></span>
1. <span data-ttu-id="ddbe9-110">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="ddbe9-111">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="ddbe9-112">Ağaçta "Müşteri fatura modeli" seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="ddbe9-113">Ağaçta, "Müşteri faturası modeli\Müşteri faturası modeli (özel)" seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="ddbe9-114">Faturayı elektronik işlemeyle ilgili bir satış siparişine eklenmiş her türlü dosya hakkındaki bilgilerle elektronik iletiler oluşturmak için bir biçim oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-114">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="ddbe9-115">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="ddbe9-116">Yeni alanına, "Müşteri faturası modeli (özel) veri modeline bağlı biçim" yazın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-116">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="ddbe9-117">Ad alanına "Elektronik fatura örnek iletisi" yazın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-117">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="ddbe9-118">Elektronik fatura örnek iletisi</span><span class="sxs-lookup"><span data-stu-id="ddbe9-118">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="ddbe9-119">Veri modeli tanımı alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-119">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="ddbe9-120">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="ddbe9-120">InvoiceCustomer</span></span>  
9. <span data-ttu-id="ddbe9-121">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-121">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="ddbe9-122">Ekleri oluşturulan iletiye MIME biçiminde doldurmak için bir biçim tasarlama</span><span class="sxs-lookup"><span data-stu-id="ddbe9-122">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="ddbe9-123">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-123">Click Designer.</span></span>
2. <span data-ttu-id="ddbe9-124">İletişim kutusunu açmak için Kök ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-124">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="ddbe9-125">Ağaçta seçin 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-125">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="ddbe9-126">Ad alanına "Fatura" yazın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-126">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="ddbe9-127">Fatura</span><span class="sxs-lookup"><span data-stu-id="ddbe9-127">Invoice</span></span>  
5. <span data-ttu-id="ddbe9-128">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-128">Click OK.</span></span>
6. <span data-ttu-id="ddbe9-129">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-129">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="ddbe9-130">Ağaçta seçin 'XML\Attribute'.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-130">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="ddbe9-131">Ad alanına "SalesOrder" yazın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-131">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="ddbe9-132">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="ddbe9-132">SalesOrder</span></span>  
9. <span data-ttu-id="ddbe9-133">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-133">Click OK.</span></span>
10. <span data-ttu-id="ddbe9-134">Öznitelik Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-134">Click Add Attribute.</span></span>
11. <span data-ttu-id="ddbe9-135">Ad alanına "InvoiceNumber" yazın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-135">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="ddbe9-136">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="ddbe9-136">InvoiceNumber</span></span>  
12. <span data-ttu-id="ddbe9-137">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-137">Click OK.</span></span>
13. <span data-ttu-id="ddbe9-138">Öznitelik Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-138">Click Add Attribute.</span></span>
14. <span data-ttu-id="ddbe9-139">Ad alanına "InvoiceAmount" yazın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-139">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="ddbe9-140">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="ddbe9-140">InvoiceAmount</span></span>  
15. <span data-ttu-id="ddbe9-141">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-141">Click OK.</span></span>
16. <span data-ttu-id="ddbe9-142">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-142">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="ddbe9-143">Ağaçta seçin 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-143">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="ddbe9-144">Ad alanına "EnclosedDocs" yazın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-144">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="ddbe9-145">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="ddbe9-145">EnclosedDocs</span></span>  
19. <span data-ttu-id="ddbe9-146">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-146">Click OK.</span></span>
20. <span data-ttu-id="ddbe9-147">Ağaçta, "Fatura\EnclosedDocs" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-147">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="ddbe9-148">Öğe Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-148">Click Add Element.</span></span>
22. <span data-ttu-id="ddbe9-149">Ad alanına "Belge" yazın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-149">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="ddbe9-150">Belge</span><span class="sxs-lookup"><span data-stu-id="ddbe9-150">Document</span></span>  
23. <span data-ttu-id="ddbe9-151">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-151">Click OK.</span></span>
24. <span data-ttu-id="ddbe9-152">Ağaçta, "Fatura\EnclosedDocs\Belge" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-152">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="ddbe9-153">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-153">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="ddbe9-154">Ağaçta seçin 'XML\Attribute'.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-154">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="ddbe9-155">Ad alanına "FileName" yazın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-155">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="ddbe9-156">FileName</span><span class="sxs-lookup"><span data-stu-id="ddbe9-156">FileName</span></span>  
28. <span data-ttu-id="ddbe9-157">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-157">Click OK.</span></span>
29. <span data-ttu-id="ddbe9-158">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-158">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="ddbe9-159">Ağaçta seçin 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-159">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="ddbe9-160">Ad alanına "FileContent" yazın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-160">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="ddbe9-161">FileContent</span><span class="sxs-lookup"><span data-stu-id="ddbe9-161">FileContent</span></span>  
32. <span data-ttu-id="ddbe9-162">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-162">Click OK.</span></span>
33. <span data-ttu-id="ddbe9-163">Ağaçta, "Fatura\EnclosedDocs\Belgeler\FileContent" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-163">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="ddbe9-164">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-164">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="ddbe9-165">Ağaçta, "Metin\Base64" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-165">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="ddbe9-166">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-166">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="ddbe9-167">Veri kaynağı olarak veri modeline biçim öğelerini eşleme</span><span class="sxs-lookup"><span data-stu-id="ddbe9-167">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="ddbe9-168">Ağaçta, "Fatura\SalesOrder" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-168">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="ddbe9-169">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-169">Click the Mapping tab.</span></span>
3. <span data-ttu-id="ddbe9-170">Ağaçta, 'model'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-170">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="ddbe9-171">Ağaçta, "model\Satış siparişi numarası(SalesId)" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-171">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="ddbe9-172">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-172">Click Bind.</span></span>
6. <span data-ttu-id="ddbe9-173">Ağaçta, "Fatura\InvoiceNumber" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-173">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="ddbe9-174">Ağaçta, "model\Temel fatura(InvoiceBase)" seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-174">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="ddbe9-175">Ağaçta, "model\Temel fatura(InvoiceBase)\Fatura numarası(Id)" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-175">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="ddbe9-176">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-176">Click Bind.</span></span>
10. <span data-ttu-id="ddbe9-177">Ağaçta, "Fatura\InvoiceAmount" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-177">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="ddbe9-178">Ağaçta, "model\Temel fatura(InvoiceBase)\Fatura tutarı(Tutar)" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-178">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="ddbe9-179">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-179">Click Bind.</span></span>
13. <span data-ttu-id="ddbe9-180">Ağaçta, "model\Fatura ekleri" seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-180">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="ddbe9-181">Ağaçta, "model\Fatura ekleri\Dosya içeriği" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-181">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="ddbe9-182">Ağaçta, "Fatura\EnclosedDocs\Belge\FileContent\Base64" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-182">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="ddbe9-183">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-183">Click Bind.</span></span>
17. <span data-ttu-id="ddbe9-184">Ağaçta "model\Fatura ekleri\Dosya adı" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-184">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="ddbe9-185">Ağaçta, "Fatura\EnclosedDocs\Belgeler\FileName" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-185">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="ddbe9-186">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-186">Click Bind.</span></span>
20. <span data-ttu-id="ddbe9-187">Ağaçta, "model\Fatura ekleri" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-187">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="ddbe9-188">Ağaçta, "Fatura\EnclosedDocs\Belge" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-188">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="ddbe9-189">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-189">Click Bind.</span></span>
23. <span data-ttu-id="ddbe9-190">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-190">Click Save.</span></span>
24. <span data-ttu-id="ddbe9-191">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ddbe9-191">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]