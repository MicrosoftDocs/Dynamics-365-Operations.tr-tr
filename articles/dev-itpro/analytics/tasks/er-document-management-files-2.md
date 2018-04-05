--- 
title: "Elektronik raporlama (ER) için biçim çıktılarında Belge Yönetimi dosyalarını kullanmak üzere veri modelini genişletme"
description: "Aşağıdaki adımlar, bir Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolü atanan bir kullanıcının, ER çıktısında Belge Yönetimi belgelerini (eklerini) kullanmak amacıyla bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar."
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
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: ebbd442c9f69290dc995c05462ca70b554f7d9f2
ms.contentlocale: tr-tr
ms.lasthandoff: 03/26/2018

---
# <a name="extend-data-model-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a><span data-ttu-id="03a16-103">Elektronik raporlama (ER) için biçim çıktılarında Belge Yönetimi dosyalarını kullanmak üzere veri modelini genişletme</span><span class="sxs-lookup"><span data-stu-id="03a16-103">Extend data model to use Document Management files in format outputs for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="03a16-104">Aşağıdaki adımlar, bir Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolü atanan bir kullanıcının, ER çıktısında Belge Yönetimi belgelerini (eklerini) kullanmak amacıyla bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="03a16-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="03a16-105">Bu adımlar tüm şirketlerde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="03a16-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="03a16-106">Bu adımları tamamlamak için öncelikle "ER Biçim çıktılarında Belge Yönetimi dosyalarını kullanma (Bölüm 1: Veri modelini hazırlama" görev kılavuzundaki adımları tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="03a16-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="03a16-107">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="03a16-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="03a16-108">İçerdiği Belge Yönetimi dosyalarını sunmak için veri modelini genişletme</span><span class="sxs-lookup"><span data-stu-id="03a16-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="03a16-109">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="03a16-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="03a16-110">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03a16-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="03a16-111">Ağaçta "Müşteri fatura modeli" seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="03a16-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="03a16-112">Ağaçta, "Müşteri faturası modeli\Müşteri faturası modeli (özel)" seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="03a16-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="03a16-113">Tasarımcı'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03a16-113">Click Designer.</span></span>
6. <span data-ttu-id="03a16-114">Ağaçta "Müşteri fatura modeli(InvoiceCustomer)" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="03a16-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="03a16-115">Bu veri modelini, içerisindeki faturayı elektronik işlemeyle ilgili bir satış siparişine eklenmiş her türlü dosyayı açığa çıkarmak için genişletiriz.</span><span class="sxs-lookup"><span data-stu-id="03a16-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="03a16-116">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03a16-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="03a16-117">Ad alanına "Fatura ekleri" yazın.</span><span class="sxs-lookup"><span data-stu-id="03a16-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="03a16-118">Fatura ekleri</span><span class="sxs-lookup"><span data-stu-id="03a16-118">Invoice attachments</span></span>  
9. <span data-ttu-id="03a16-119">Madde türü alanında 'Kayıt listesi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="03a16-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="03a16-120">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="03a16-120">Click Add.</span></span>
11. <span data-ttu-id="03a16-121">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03a16-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="03a16-122">Ad alanına "Dosya içeriği" yazın.</span><span class="sxs-lookup"><span data-stu-id="03a16-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="03a16-123">Dosya içeriği</span><span class="sxs-lookup"><span data-stu-id="03a16-123">File content</span></span>  
13. <span data-ttu-id="03a16-124">Madde türü alanında "Konteyner" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="03a16-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="03a16-125">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="03a16-125">Click Add.</span></span>
15. <span data-ttu-id="03a16-126">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03a16-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="03a16-127">Ad alanına "Dosya adı" yazın.</span><span class="sxs-lookup"><span data-stu-id="03a16-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="03a16-128">Dosya adı</span><span class="sxs-lookup"><span data-stu-id="03a16-128">File name</span></span>  
17. <span data-ttu-id="03a16-129">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="03a16-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="03a16-130">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="03a16-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-data-sources"></a><span data-ttu-id="03a16-131">Microsoft Dynamics 365 for Finance and Operations veri kaynaklarına yeni veri modeli öğeleri eşleyin</span><span class="sxs-lookup"><span data-stu-id="03a16-131">Map new data model elements to Dynamics 365 for Finance and Operations data sources</span></span>
1. <span data-ttu-id="03a16-132">Modeli veri kaynağına eşle'yi tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03a16-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="03a16-133">Açıklama alanına bir "InvoiceCustomer" değeriyle filtre uygulamak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="03a16-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="03a16-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="03a16-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="03a16-135">Uygun veri kaynaklarına yeni model öğeleri eşleriz.</span><span class="sxs-lookup"><span data-stu-id="03a16-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="03a16-136">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="03a16-136">Click Designer.</span></span>
4. <span data-ttu-id="03a16-137">Ağaçta "Fatura ekleri" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="03a16-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="03a16-138">Ağaçta, "Fatura ekleri" seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="03a16-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="03a16-139">Ağaçta, "Fatura ekleri\Dosya adı" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="03a16-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="03a16-140">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03a16-140">Click Edit.</span></span>
8. <span data-ttu-id="03a16-141">Formül alanına, 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'' yazın.</span><span class="sxs-lookup"><span data-stu-id="03a16-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="03a16-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="03a16-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="03a16-143">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03a16-143">Click Save.</span></span>
10. <span data-ttu-id="03a16-144">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="03a16-144">Close the page.</span></span>
11. <span data-ttu-id="03a16-145">Ağaçta, "Fatura ekleri\Dosya içeriği" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="03a16-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="03a16-146">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03a16-146">Click Edit.</span></span>
13. <span data-ttu-id="03a16-147">Formül alanına, '>CustInvoiceJour.'<Relations'.SalesTable.'Relations'.'<Documents'.'getFileContentAsContainer()'' yazın.</span><span class="sxs-lookup"><span data-stu-id="03a16-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="03a16-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="03a16-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="03a16-149">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03a16-149">Click Save.</span></span>
15. <span data-ttu-id="03a16-150">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="03a16-150">Close the page.</span></span>
16. <span data-ttu-id="03a16-151">Ağaçta "Fatura ekleri" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="03a16-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="03a16-152">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03a16-152">Click Edit.</span></span>
18. <span data-ttu-id="03a16-153">Formül alanına, 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'' yazın.</span><span class="sxs-lookup"><span data-stu-id="03a16-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="03a16-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="03a16-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="03a16-155">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03a16-155">Click Save.</span></span>
20. <span data-ttu-id="03a16-156">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="03a16-156">Close the page.</span></span>
21. <span data-ttu-id="03a16-157">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03a16-157">Click Save.</span></span>
22. <span data-ttu-id="03a16-158">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="03a16-158">Close the page.</span></span>
23. <span data-ttu-id="03a16-159">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="03a16-159">Close the page.</span></span>
24. <span data-ttu-id="03a16-160">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="03a16-160">Close the page.</span></span>
25. <span data-ttu-id="03a16-161">Durumu değiştir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03a16-161">Click Change status.</span></span>
26. <span data-ttu-id="03a16-162">Tamamla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03a16-162">Click Complete.</span></span>
27. <span data-ttu-id="03a16-163">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03a16-163">Click OK.</span></span>


