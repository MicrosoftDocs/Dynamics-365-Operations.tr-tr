--- 
title: "Elektronik raporlama (ER) için biçim çıktılarında Belge Yönetimi dosyalarını kullanmak üzere veri modelini hazırlama"
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
ms.openlocfilehash: 5d224afd799306828a59e97f7f3bcd4cb831537c
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="prepare-data-model-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a><span data-ttu-id="89df2-103">Elektronik raporlama (ER) için biçim çıktılarında Belge Yönetimi dosyalarını kullanmak üzere veri modelini hazırlama</span><span class="sxs-lookup"><span data-stu-id="89df2-103">Prepare data model to use Document Management files in format outputs for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="89df2-104">Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının, ER çıktısında Belge Yönetimi belgelerini (eklerini) kullanmak amacıyla bir Elektronik raporlama (ER) biçimini nasıl yapılandırabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="89df2-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="89df2-105">Bu adımlar tüm şirketlerde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="89df2-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="89df2-106">Bu adımları tamamlamak için, öncelikle "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="89df2-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="89df2-107">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="89df2-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="89df2-108">Microsoft tarafından sağlanan yapılandırma listesine erişim alma</span><span class="sxs-lookup"><span data-stu-id="89df2-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="89df2-109">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="89df2-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="89df2-110">'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="89df2-110">Make sure that the 'Litware, Inc.'</span></span> <span data-ttu-id="89df2-111">sağlayıcısının kullanılabilir ve etkin olarak işaretlendiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="89df2-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="89df2-112">Litware, Inc. seçin.</span><span class="sxs-lookup"><span data-stu-id="89df2-112">Select the 'Litware, Inc.'</span></span> <span data-ttu-id="89df2-113">sağlayıcısını seçin.</span><span class="sxs-lookup"><span data-stu-id="89df2-113">provider.</span></span>
3. <span data-ttu-id="89df2-114">Depolar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89df2-114">Click Repositories.</span></span>
    * <span data-ttu-id="89df2-115">"Operasyon kaynakları" türünün bir havuzu zaten varsa geçerli alt görevin kalan adımlarını atlayın.</span><span class="sxs-lookup"><span data-stu-id="89df2-115">If a repository of the 'Operations resources' type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="89df2-116">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="89df2-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="89df2-117">Yapılandırma havuzu türü alanına "Operasyon kaynakları" yazın.</span><span class="sxs-lookup"><span data-stu-id="89df2-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="89df2-118">Havuz oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89df2-118">Click Create repository.</span></span>
7. <span data-ttu-id="89df2-119">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89df2-119">Click OK.</span></span>

## <a name="get-the-customer-invoice-model-configurations-provided-by-microsoft"></a><span data-ttu-id="89df2-120">Microsoft tarafından sağlanan müşteri fatura modeli yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="89df2-120">Get the Customer invoice model configurations provided by Microsoft</span></span>
1. <span data-ttu-id="89df2-121">Filtreleri göster'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89df2-121">Click Show filters.</span></span>
2. <span data-ttu-id="89df2-122">Şu filtreleri uygulayın: "ile başlar" filtre işlecini kullanarak "Ad" alanında "Operasyon kaynakları" için bir filtre değeri girin; "ile başlar" filtre işlecini kullanarak "Açıklama" alanında "" için bir filtre değeri girin</span><span class="sxs-lookup"><span data-stu-id="89df2-122">Apply the following filters: Enter a filter value of "Operations resources" on the "Name" field using the "begins with" filter operator; Enter a filter value of "" on the "Description" field using the "begins with" filter operator</span></span>
3. <span data-ttu-id="89df2-123">Filtreleri göster'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89df2-123">Click Show filters.</span></span>
4. <span data-ttu-id="89df2-124">Aç'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89df2-124">Click Open.</span></span>
5. <span data-ttu-id="89df2-125">Ağaçta, "Müşteri fatura modeli" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="89df2-125">In the tree, select 'Customer invoice model'.</span></span>
    * <span data-ttu-id="89df2-126">İçe aktarmak için "Müşteri fatura modeli" model yapılandırmasını seçin.</span><span class="sxs-lookup"><span data-stu-id="89df2-126">Select the model configuration 'Customer invoice model' to import it.</span></span>  
6. <span data-ttu-id="89df2-127">İçe aktar'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="89df2-127">Click Import.</span></span>
    * <span data-ttu-id="89df2-128">Seçili yapılandırmanın 1 sürümü için İthalat'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89df2-128">Click Import for version 1 of the selected configuration.</span></span>  
7. <span data-ttu-id="89df2-129">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="89df2-129">Click Yes.</span></span>
8. <span data-ttu-id="89df2-130">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="89df2-130">Close the page.</span></span>
9. <span data-ttu-id="89df2-131">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="89df2-131">Close the page.</span></span>
10. <span data-ttu-id="89df2-132">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89df2-132">Click Reporting configurations.</span></span>
11. <span data-ttu-id="89df2-133">Ağaçta, "Müşteri fatura modeli" seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="89df2-133">In the tree, select 'Customer invoice model'.</span></span>

## <a name="create-the-derived-model-to-support-access-to-the-document-management-files"></a><span data-ttu-id="89df2-134">Belge Yönetimi dosyalarına erişimi desteklemek için türetilmiş model oluşturun.</span><span class="sxs-lookup"><span data-stu-id="89df2-134">Create the derived model to support access to the Document Management files.</span></span>
    * <span data-ttu-id="89df2-135">Müşteri fatura modelinin kendinize özel yapılandırmasını Microsoft tarafından sağlanan yapılandırmadan türeterek yapılandırırsınız.</span><span class="sxs-lookup"><span data-stu-id="89df2-135">You will create our own configuration of the Customer invoice model deriving it from the configuration provided by Microsoft.</span></span> <span data-ttu-id="89df2-136">Belge Yönetimi dosyalarına erişmek ve bu modeli temel alarak oluşturacağınız elektronik belgeler için kullanılabilir duruma getirmek için bu yapılandırmayı kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="89df2-136">You will use this configuration to implement access to the Document Management files and make them available for electronic documents that you will create based on this model.</span></span>  
1. <span data-ttu-id="89df2-137">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="89df2-137">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="89df2-138">Yeni alana "İsimden Türet: Müşteri fatura modeli, Microsoft" yazın.</span><span class="sxs-lookup"><span data-stu-id="89df2-138">In the New field, enter 'Derive from Name: Customer invoice model, Microsoft'.</span></span>
3. <span data-ttu-id="89df2-139">Ad alanına "Müşteri fatura modeli (özel)" yazın.</span><span class="sxs-lookup"><span data-stu-id="89df2-139">In the Name field, type 'Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="89df2-140">Müşteri faturası modeli (özel)</span><span class="sxs-lookup"><span data-stu-id="89df2-140">Customer invoice model (custom)</span></span>  
4. <span data-ttu-id="89df2-141">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="89df2-141">Click Create configuration.</span></span>

