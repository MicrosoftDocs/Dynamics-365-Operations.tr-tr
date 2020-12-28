---
title: ER Biçim çıktılarında Belge Yönetimi dosyalarını kullanma (Bölüm 1 - Veri modelini hazırlama)
description: Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının, ER çıktısında Belge Yönetimi belgelerini (eklerini) kullanmak amacıyla bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0b82c63c572cc946737ba54deb10a03dc437c01b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681840"
---
# <a name="er-use-document-management-files-in-format-outputs-part-1---prepare-data-model"></a><span data-ttu-id="8747f-103">ER Biçim çıktılarında Belge Yönetimi dosyalarını kullanma (Bölüm 1 - Veri modelini hazırlama)</span><span class="sxs-lookup"><span data-stu-id="8747f-103">ER Use Document Management files in format outputs (Part 1 - Prepare data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8747f-104">Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının, ER çıktısında Belge Yönetimi belgelerini (eklerini) kullanmak amacıyla bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="8747f-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="8747f-105">Bu adımlar tüm şirketlerde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="8747f-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="8747f-106">Bu adımları tamamlamak için öncelikle "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="8747f-106">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="8747f-107">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="8747f-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="8747f-108">Microsoft tarafından sağlanan yapılandırma listesine erişim alma</span><span class="sxs-lookup"><span data-stu-id="8747f-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="8747f-109">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="8747f-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="8747f-110">'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="8747f-110">Make sure that the 'Litware, Inc.'</span></span> <span data-ttu-id="8747f-111">sağlayıcısının kullanılabilir ve etkin olarak işaretlendiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="8747f-111">provider is available and marked as active.</span></span>  

2. <span data-ttu-id="8747f-112">Litware, Inc. seçin.</span><span class="sxs-lookup"><span data-stu-id="8747f-112">Select the 'Litware, Inc.'</span></span> <span data-ttu-id="8747f-113">sağlayıcısını seçin.</span><span class="sxs-lookup"><span data-stu-id="8747f-113">provider.</span></span>
3. <span data-ttu-id="8747f-114">Depolar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8747f-114">Click Repositories.</span></span>

    <span data-ttu-id="8747f-115">"Operasyon kaynakları" türünün bir havuzu zaten varsa geçerli alt görevin kalan adımlarını atlayın.</span><span class="sxs-lookup"><span data-stu-id="8747f-115">If a repository of the 'Operations resources' type already exists, skip the remaining steps of the current sub-task.</span></span>  

4. <span data-ttu-id="8747f-116">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8747f-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="8747f-117">Yapılandırma havuzu türü alanına "Operasyon kaynakları" yazın.</span><span class="sxs-lookup"><span data-stu-id="8747f-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="8747f-118">Havuz oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8747f-118">Click Create repository.</span></span>
7. <span data-ttu-id="8747f-119">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8747f-119">Click OK.</span></span>

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a><span data-ttu-id="8747f-120">Microsoft tarafından sağlanan müşteri fatura modeli yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="8747f-120">Get the Customer invoice model configurations provided by Microsoft</span></span>
1. <span data-ttu-id="8747f-121">Filtreleri göster'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8747f-121">Click Show filters.</span></span>
2. <span data-ttu-id="8747f-122">Şu filtreleri uygulayın: "ile başlar" filtre işlecini kullanarak "Ad" alanında "Operasyon kaynakları" için bir filtre değeri girin; "ile başlar" filtre işlecini kullanarak "Açıklama" alanında "" için bir filtre değeri girin</span><span class="sxs-lookup"><span data-stu-id="8747f-122">Apply the following filters: Enter a filter value of "Operations resources" on the "Name" field using the "begins with" filter operator; Enter a filter value of "" on the "Description" field using the "begins with" filter operator</span></span>
3. <span data-ttu-id="8747f-123">Filtreleri göster'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8747f-123">Click Show filters.</span></span>
4. <span data-ttu-id="8747f-124">Aç'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8747f-124">Click Open.</span></span>
5. <span data-ttu-id="8747f-125">Ağaçta, "Müşteri fatura modeli" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="8747f-125">In the tree, select 'Customer invoice model'.</span></span>

    <span data-ttu-id="8747f-126">İçe aktarmak için "Müşteri fatura modeli" model yapılandırmasını seçin.</span><span class="sxs-lookup"><span data-stu-id="8747f-126">Select the model configuration 'Customer invoice model' to import it.</span></span>  

6. <span data-ttu-id="8747f-127">İçe aktar'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8747f-127">Click Import.</span></span>

    <span data-ttu-id="8747f-128">Seçili yapılandırmanın 1 sürümü için İthalat'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8747f-128">Click Import for version 1 of the selected configuration.</span></span>  

7. <span data-ttu-id="8747f-129">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8747f-129">Click Yes.</span></span>
8. <span data-ttu-id="8747f-130">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8747f-130">Close the page.</span></span>
9. <span data-ttu-id="8747f-131">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8747f-131">Close the page.</span></span>
10. <span data-ttu-id="8747f-132">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8747f-132">Click Reporting configurations.</span></span>
11. <span data-ttu-id="8747f-133">Ağaçta, "Müşteri fatura modeli" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="8747f-133">In the tree, select 'Customer invoice model'.</span></span>

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a><span data-ttu-id="8747f-134">Belge Yönetimi dosyalarına erişimi desteklemek için türetilmiş model oluşturun.</span><span class="sxs-lookup"><span data-stu-id="8747f-134">Create the derived model to support access to the Document Management files.</span></span>
<span data-ttu-id="8747f-135">Müşteri fatura modelinin kendinize özel yapılandırmasını Microsoft tarafından sağlanan yapılandırmadan türeterek yapılandırırsınız.</span><span class="sxs-lookup"><span data-stu-id="8747f-135">You will create our own configuration of the Customer invoice model deriving it from the configuration provided by Microsoft.</span></span> <span data-ttu-id="8747f-136">Belge Yönetimi dosyalarına erişmek ve bu modeli temel alarak oluşturacağınız elektronik belgeler için kullanılabilir duruma getirmek için bu yapılandırmayı kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="8747f-136">You will use this configuration to implement access to the Document Management files and make them available for electronic documents that you will create based on this model.</span></span>  
1. <span data-ttu-id="8747f-137">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8747f-137">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="8747f-138">Yeni alana "İsimden Türet: Müşteri fatura modeli, Microsoft" yazın.</span><span class="sxs-lookup"><span data-stu-id="8747f-138">In the New field, enter 'Derive from Name: Customer invoice model, Microsoft'.</span></span>
3. <span data-ttu-id="8747f-139">Ad alanına "Müşteri fatura modeli (özel)" yazın.</span><span class="sxs-lookup"><span data-stu-id="8747f-139">In the Name field, type 'Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="8747f-140">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8747f-140">Click Create configuration.</span></span>

