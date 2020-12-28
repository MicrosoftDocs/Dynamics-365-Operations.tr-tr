---
title: ER Biçim çıktılarında Belge Yönetimi dosyalarını kullanma (Bölüm 4 - Biçimi çalıştırma)
description: Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının, ER çıktısında Belge Yönetimi belgelerini kullanmak amacıyla bir Elektronik raporlama biçimini nasıl yapılandırabileceğini açıklar.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 89e09d79389dc2c883c429cfee3164632e0cdc0f
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681793"
---
# <a name="er-use-document-management-files-in-format-outputs-part-4---run-format"></a><span data-ttu-id="36821-103">ER Biçim çıktılarında Belge Yönetimi dosyalarını kullanma (Bölüm 4 - Biçimi çalıştırma)</span><span class="sxs-lookup"><span data-stu-id="36821-103">ER Use Document Management files in format outputs (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="36821-104">Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının, ER çıktısında Belge Yönetimi belgelerini (eklerini) kullanmak amacıyla bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="36821-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="36821-105">Bu adımlar DEMF şirketinde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="36821-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="36821-106">Bu adımları tamamlamak için öncelikle "ER Biçim çıktılarında Belge Yönetimi dosyalarını kullanma (Bölüm 3: Biçimi çalıştırma)" yordamındaki adımları tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="36821-106">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 3: Create format)" procedure.</span></span>

<span data-ttu-id="36821-107">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="36821-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a><span data-ttu-id="36821-108">Tek bir faturanın satış siparişi için gerekli ekleri ekleyin</span><span class="sxs-lookup"><span data-stu-id="36821-108">Add necessary attachments for sales order of a single invoice</span></span>
1. <span data-ttu-id="36821-109">Alacak hesapları > Faturalar > Açık müşteri faturaları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="36821-109">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="36821-110">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="36821-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="36821-111">Örneğin, "CIV-000148" değerine sahip Fatura alanı üzerinde filtreleme uygulayın.</span><span class="sxs-lookup"><span data-stu-id="36821-111">For example, filter on the Invoice field with a value of 'CIV-000148'.</span></span>
    * <span data-ttu-id="36821-112">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="36821-112">CIV-000148</span></span>  
3. <span data-ttu-id="36821-113">Seçilen faturanın bağlantısını izlemek için tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36821-113">Click to follow the selected invoice's link.</span></span>
    * <span data-ttu-id="36821-114">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="36821-114">CIV-000148</span></span>  
4. <span data-ttu-id="36821-115">Satış siparişi alanındaki bağlantıyı izlemek için tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36821-115">Click to follow the link in the Sales order field.</span></span>
    * <span data-ttu-id="36821-116">000148</span><span class="sxs-lookup"><span data-stu-id="36821-116">000148</span></span>  
5. <span data-ttu-id="36821-117">Satırlar veya başlık alanında Başlık seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="36821-117">In the Lines or header field, select the option of Header.</span></span>
    * <span data-ttu-id="36821-118">Ekleri eklemek için hedef olacağını belirtmek için Başlığı seçin.</span><span class="sxs-lookup"><span data-stu-id="36821-118">Select Header to indicate that this will be the target for adding attachments.</span></span>  
6. <span data-ttu-id="36821-119">İliştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36821-119">Click Attach.</span></span>
    * <span data-ttu-id="36821-120">Bu satış siparişi için ek olarak birkaç dosya ekleyin.</span><span class="sxs-lookup"><span data-stu-id="36821-120">Add a few files as attachments for this sales order.</span></span> <span data-ttu-id="36821-121">Belge Yönetimi tarafından desteklenen belge türlerinden dosyaları kullanın (DOCX, DPF, XML, JPG, vb. dosya uzantıları).</span><span class="sxs-lookup"><span data-stu-id="36821-121">Use the files of the document types that are supported by the Document Management (with file extensions DOCX, DPF, XML, JPG, etc.).</span></span> <span data-ttu-id="36821-122">Eklenecek ve ER elektronik iletisinde faturayla ilgili olarak işlenecek dosyalara göz atın ve seçin.</span><span class="sxs-lookup"><span data-stu-id="36821-122">Browse and select files to be attached and further processed with the related invoice in the ER electronic message.</span></span>  
7. <span data-ttu-id="36821-123">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36821-123">Click New.</span></span>
8. <span data-ttu-id="36821-124">Dosya'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36821-124">Click File.</span></span>
9. <span data-ttu-id="36821-125">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36821-125">Click New.</span></span>
10. <span data-ttu-id="36821-126">Dosya'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36821-126">Click File.</span></span>
11. <span data-ttu-id="36821-127">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="36821-127">Close the page.</span></span>
12. <span data-ttu-id="36821-128">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="36821-128">Close the page.</span></span>
13. <span data-ttu-id="36821-129">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="36821-129">Close the page.</span></span>
14. <span data-ttu-id="36821-130">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="36821-130">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="36821-131">Seçili fatura için tasarlanan raporu çalıştırın</span><span class="sxs-lookup"><span data-stu-id="36821-131">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="36821-132">Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="36821-132">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="36821-133">Ağaçta "Müşteri fatura modeli" seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="36821-133">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="36821-134">Ağaçta, "Müşteri faturası modeli\Müşteri faturası modeli (özel)"i genişletin.</span><span class="sxs-lookup"><span data-stu-id="36821-134">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="36821-135">Ağaçta, "Müşteri faturası modeli\Müşteri faturası modeli (özel)\Elektronik fatura örnek iletisi"ni seçin.</span><span class="sxs-lookup"><span data-stu-id="36821-135">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="36821-136">Çalıştır öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36821-136">Click Run.</span></span>
6. <span data-ttu-id="36821-137">Eklenecek kayıtlar () bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="36821-137">Expand the Records to include () section.</span></span>
7. <span data-ttu-id="36821-138">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36821-138">Click Filter.</span></span>
8. <span data-ttu-id="36821-139">Müşteri fatura günlüğü satırını ve Satış siparişi alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="36821-139">Select the row of the Customer invoice journal and the Sales order field.</span></span>
9. <span data-ttu-id="36821-140">Ölçütler alanına '000148' yazın.</span><span class="sxs-lookup"><span data-stu-id="36821-140">In the Criteria field, type '000148'.</span></span>
    * <span data-ttu-id="36821-141">"Satış siparişi" ölçütler alanında sipariş numarası olarak 000148 yazın.</span><span class="sxs-lookup"><span data-stu-id="36821-141">In the criteria "Sales order" field, type the order number 000148.</span></span>  
10. <span data-ttu-id="36821-142">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36821-142">Click OK.</span></span>
11. <span data-ttu-id="36821-143">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36821-143">Click OK.</span></span>
    * <span data-ttu-id="36821-144">Ortaya çıkan sonucu inceleyin.</span><span class="sxs-lookup"><span data-stu-id="36821-144">Review the generated output.</span></span> <span data-ttu-id="36821-145">Her ek için tek bir XML düğümü oluşturulduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="36821-145">Note that for each attachment a single XML node has been created.</span></span> <span data-ttu-id="36821-146">Ek'in içeriği XML çıktısına MIME (base64) metin biçiminde doldurulur.</span><span class="sxs-lookup"><span data-stu-id="36821-146">The attachment's content is populated to the XML output in MIME (base64) text format.</span></span>  

