---
title: ER Biçim çıktılarında Belge Yönetimi dosyalarını kullanma (Bölüm 2 - Veri modelini genişletme)
description: Bu konuda, ER çıktılarında Belge Yönetimi dosyaları (ekler) kullanmak üzere Elektronik raporlama (ER) biçiminin nasıl yapılandırılacağı açıklanmaktadır. (2. Bölüm)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e79dd0a6c68aa6ba7b857c31c9159c68543d93b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754926"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a><span data-ttu-id="a9f0c-104">ER Biçim çıktılarında Belge Yönetimi dosyalarını kullanma (Bölüm 2 - Veri modelini genişletme)</span><span class="sxs-lookup"><span data-stu-id="a9f0c-104">ER Use Document Management files in format outputs (Part 2 - Extend data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a9f0c-105">Aşağıdaki adımlar, bir Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolü atanan bir kullanıcının, ER çıktısında Belge Yönetimi belgelerini (eklerini) kullanmak amacıyla bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-105">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="a9f0c-106">Bu adımlar tüm şirketlerde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="a9f0c-107">Bu adımları tamamlamak için öncelikle "ER Biçim çıktılarında Belge Yönetimi dosyalarını kullanma (Bölüm 1: Veri modelini hazırlama") görev kılavuzundaki adımları tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 1: Prepare data model)" task guide.</span></span>

<span data-ttu-id="a9f0c-108">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="a9f0c-109">İçerdiği Belge Yönetimi dosyalarını sunmak için veri modelini genişletme</span><span class="sxs-lookup"><span data-stu-id="a9f0c-109">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="a9f0c-110">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="a9f0c-111">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="a9f0c-112">Ağaçta "Müşteri fatura modeli" seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="a9f0c-113">Ağaçta, "Müşteri faturası modeli\Müşteri faturası modeli (özel)" seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="a9f0c-114">Tasarımcı'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-114">Click Designer.</span></span>
6. <span data-ttu-id="a9f0c-115">Ağaçta "Müşteri fatura modeli(InvoiceCustomer)" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-115">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="a9f0c-116">Bu veri modelini, içerisindeki faturayı elektronik işlemeyle ilgili bir satış siparişine eklenmiş her türlü dosyayı açığa çıkarmak için genişletiriz.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-116">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="a9f0c-117">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="a9f0c-118">Ad alanına "Fatura ekleri" yazın.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-118">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="a9f0c-119">Fatura ekleri</span><span class="sxs-lookup"><span data-stu-id="a9f0c-119">Invoice attachments</span></span>  
9. <span data-ttu-id="a9f0c-120">Madde türü alanında 'Kayıt listesi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-120">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="a9f0c-121">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-121">Click Add.</span></span>
11. <span data-ttu-id="a9f0c-122">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-122">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="a9f0c-123">Ad alanına "Dosya içeriği" yazın.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-123">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="a9f0c-124">Dosya içeriği</span><span class="sxs-lookup"><span data-stu-id="a9f0c-124">File content</span></span>  
13. <span data-ttu-id="a9f0c-125">Madde türü alanında "Konteyner" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-125">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="a9f0c-126">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-126">Click Add.</span></span>
15. <span data-ttu-id="a9f0c-127">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-127">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="a9f0c-128">Ad alanına "Dosya adı" yazın.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-128">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="a9f0c-129">Dosya adı</span><span class="sxs-lookup"><span data-stu-id="a9f0c-129">File name</span></span>  
17. <span data-ttu-id="a9f0c-130">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-130">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="a9f0c-131">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-131">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-data-sources"></a><span data-ttu-id="a9f0c-132">Veri kaynaklarına yeni veri modeli öğelerini eşleme</span><span class="sxs-lookup"><span data-stu-id="a9f0c-132">Map new data model elements to data sources</span></span>
1. <span data-ttu-id="a9f0c-133">Modeli veri kaynağına eşle'yi tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-133">Click Map model to datasource.</span></span>
2. <span data-ttu-id="a9f0c-134">Açıklama alanına bir "InvoiceCustomer" değeriyle filtre uygulamak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-134">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="a9f0c-135">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="a9f0c-135">InvoiceCustomer</span></span>  
    * <span data-ttu-id="a9f0c-136">Uygun veri kaynaklarına yeni model öğeleri eşleriz.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-136">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="a9f0c-137">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-137">Click Designer.</span></span>
4. <span data-ttu-id="a9f0c-138">Ağaçta "Fatura ekleri" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-138">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="a9f0c-139">Ağaçta, "Fatura ekleri" seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-139">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="a9f0c-140">Ağaçta, "Fatura ekleri\Dosya adı" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-140">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="a9f0c-141">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-141">Click Edit.</span></span>
8. <span data-ttu-id="a9f0c-142">Formül alanına, 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'' yazın.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-142">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="a9f0c-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="a9f0c-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="a9f0c-144">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-144">Click Save.</span></span>
10. <span data-ttu-id="a9f0c-145">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-145">Close the page.</span></span>
11. <span data-ttu-id="a9f0c-146">Ağaçta, "Fatura ekleri\Dosya içeriği" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-146">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="a9f0c-147">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-147">Click Edit.</span></span>
13. <span data-ttu-id="a9f0c-148">Formül alanına, '>CustInvoiceJour.'<Relations'.SalesTable.'Relations'.'<Documents'.'getFileContentAsContainer()'' yazın.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-148">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="a9f0c-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="a9f0c-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="a9f0c-150">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-150">Click Save.</span></span>
15. <span data-ttu-id="a9f0c-151">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-151">Close the page.</span></span>
16. <span data-ttu-id="a9f0c-152">Ağaçta "Fatura ekleri" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-152">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="a9f0c-153">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-153">Click Edit.</span></span>
18. <span data-ttu-id="a9f0c-154">Formül alanına, 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'' yazın.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-154">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="a9f0c-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="a9f0c-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="a9f0c-156">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-156">Click Save.</span></span>
20. <span data-ttu-id="a9f0c-157">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-157">Close the page.</span></span>
21. <span data-ttu-id="a9f0c-158">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-158">Click Save.</span></span>
22. <span data-ttu-id="a9f0c-159">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-159">Close the page.</span></span>
23. <span data-ttu-id="a9f0c-160">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-160">Close the page.</span></span>
24. <span data-ttu-id="a9f0c-161">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-161">Close the page.</span></span>
25. <span data-ttu-id="a9f0c-162">Durumu değiştir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-162">Click Change status.</span></span>
26. <span data-ttu-id="a9f0c-163">Tamamla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-163">Click Complete.</span></span>
27. <span data-ttu-id="a9f0c-164">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9f0c-164">Click OK.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]