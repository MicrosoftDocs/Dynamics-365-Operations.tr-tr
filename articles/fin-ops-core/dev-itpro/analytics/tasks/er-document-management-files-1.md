---
title: ER Biçim çıktılarında Belge Yönetimi dosyalarını kullanma (Bölüm 1 - Veri modelini hazırlama)
description: Bu konuda, ER çıktılarında Belge Yönetimi dosyaları (ekler) kullanmak üzere Elektronik raporlama (ER) biçiminin nasıl yapılandırılacağı açıklanmaktadır. (1. Bölüm)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 35bffd6d3688a9887fcdaf4edbd89c344cb9b18d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559809"
---
# <a name="er-use-document-management-files-in-format-outputs-part-1---prepare-data-model"></a><span data-ttu-id="4d096-104">ER Biçim çıktılarında Belge Yönetimi dosyalarını kullanma (Bölüm 1 - Veri modelini hazırlama)</span><span class="sxs-lookup"><span data-stu-id="4d096-104">ER Use Document Management files in format outputs (Part 1 - Prepare data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4d096-105">Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının, ER çıktısında Belge Yönetimi belgelerini (eklerini) kullanmak amacıyla bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="4d096-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="4d096-106">Bu adımlar tüm şirketlerde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="4d096-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="4d096-107">Bu adımları tamamlamak için öncelikle "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="4d096-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="4d096-108">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="4d096-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="4d096-109">Microsoft tarafından sağlanan yapılandırma listesine erişim alma</span><span class="sxs-lookup"><span data-stu-id="4d096-109">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="4d096-110">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="4d096-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="4d096-111">'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="4d096-111">Make sure that the 'Litware, Inc.'</span></span> <span data-ttu-id="4d096-112">sağlayıcısının kullanılabilir ve etkin olarak işaretlendiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="4d096-112">provider is available and marked as active.</span></span>  

2. <span data-ttu-id="4d096-113">Litware, Inc. seçin.</span><span class="sxs-lookup"><span data-stu-id="4d096-113">Select the 'Litware, Inc.'</span></span> <span data-ttu-id="4d096-114">sağlayıcısını seçin.</span><span class="sxs-lookup"><span data-stu-id="4d096-114">provider.</span></span>
3. <span data-ttu-id="4d096-115">Depolar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4d096-115">Click Repositories.</span></span>

    <span data-ttu-id="4d096-116">"Operasyon kaynakları" türünün bir havuzu zaten varsa geçerli alt görevin kalan adımlarını atlayın.</span><span class="sxs-lookup"><span data-stu-id="4d096-116">If a repository of the 'Operations resources' type already exists, skip the remaining steps of the current sub-task.</span></span>  

4. <span data-ttu-id="4d096-117">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4d096-117">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="4d096-118">Yapılandırma havuzu türü alanına "Operasyon kaynakları" yazın.</span><span class="sxs-lookup"><span data-stu-id="4d096-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="4d096-119">Havuz oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4d096-119">Click Create repository.</span></span>
7. <span data-ttu-id="4d096-120">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4d096-120">Click OK.</span></span>

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a><span data-ttu-id="4d096-121">Microsoft tarafından sağlanan müşteri fatura modeli yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="4d096-121">Get the Customer invoice model configurations provided by Microsoft</span></span>
1. <span data-ttu-id="4d096-122">Filtreleri göster'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4d096-122">Click Show filters.</span></span>
2. <span data-ttu-id="4d096-123">Şu filtreleri uygulayın: "ile başlar" filtre işlecini kullanarak "Ad" alanında "Operasyon kaynakları" için bir filtre değeri girin; "ile başlar" filtre işlecini kullanarak "Açıklama" alanında "" için bir filtre değeri girin</span><span class="sxs-lookup"><span data-stu-id="4d096-123">Apply the following filters: Enter a filter value of "Operations resources" on the "Name" field using the "begins with" filter operator; Enter a filter value of "" on the "Description" field using the "begins with" filter operator</span></span>
3. <span data-ttu-id="4d096-124">Filtreleri göster'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4d096-124">Click Show filters.</span></span>
4. <span data-ttu-id="4d096-125">Aç'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4d096-125">Click Open.</span></span>
5. <span data-ttu-id="4d096-126">Ağaçta, "Müşteri fatura modeli" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="4d096-126">In the tree, select 'Customer invoice model'.</span></span>

    <span data-ttu-id="4d096-127">İçe aktarmak için "Müşteri fatura modeli" model yapılandırmasını seçin.</span><span class="sxs-lookup"><span data-stu-id="4d096-127">Select the model configuration 'Customer invoice model' to import it.</span></span>  

6. <span data-ttu-id="4d096-128">İçe aktar'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4d096-128">Click Import.</span></span>

    <span data-ttu-id="4d096-129">Seçili yapılandırmanın 1 sürümü için İthalat'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4d096-129">Click Import for version 1 of the selected configuration.</span></span>  

7. <span data-ttu-id="4d096-130">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4d096-130">Click Yes.</span></span>
8. <span data-ttu-id="4d096-131">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4d096-131">Close the page.</span></span>
9. <span data-ttu-id="4d096-132">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4d096-132">Close the page.</span></span>
10. <span data-ttu-id="4d096-133">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4d096-133">Click Reporting configurations.</span></span>
11. <span data-ttu-id="4d096-134">Ağaçta, "Müşteri fatura modeli" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="4d096-134">In the tree, select 'Customer invoice model'.</span></span>

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a><span data-ttu-id="4d096-135">Belge Yönetimi dosyalarına erişimi desteklemek için türetilmiş model oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4d096-135">Create the derived model to support access to the Document Management files.</span></span>
<span data-ttu-id="4d096-136">Müşteri fatura modelinin kendinize özel yapılandırmasını Microsoft tarafından sağlanan yapılandırmadan türeterek yapılandırırsınız.</span><span class="sxs-lookup"><span data-stu-id="4d096-136">You will create our own configuration of the Customer invoice model deriving it from the configuration provided by Microsoft.</span></span> <span data-ttu-id="4d096-137">Belge Yönetimi dosyalarına erişmek ve bu modeli temel alarak oluşturacağınız elektronik belgeler için kullanılabilir duruma getirmek için bu yapılandırmayı kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="4d096-137">You will use this configuration to implement access to the Document Management files and make them available for electronic documents that you will create based on this model.</span></span>  
1. <span data-ttu-id="4d096-138">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4d096-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="4d096-139">Yeni alana "İsimden Türet: Müşteri fatura modeli, Microsoft" yazın.</span><span class="sxs-lookup"><span data-stu-id="4d096-139">In the New field, enter 'Derive from Name: Customer invoice model, Microsoft'.</span></span>
3. <span data-ttu-id="4d096-140">Ad alanına "Müşteri fatura modeli (özel)" yazın.</span><span class="sxs-lookup"><span data-stu-id="4d096-140">In the Name field, type 'Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="4d096-141">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4d096-141">Click Create configuration.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]