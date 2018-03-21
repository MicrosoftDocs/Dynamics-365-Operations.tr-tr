--- 
title: "Model eşleme yapılandırması oluşturma (ER)"
description: "Yeni bir Elektronik raporlama (ER) modeli eşleme yapılandırması tasarlamak ve etkili toplam hesaplamalar için yerleşik ER işlevlerini kullanmak için bu yordamı kullanın."
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 74606b1378e94e8a6945a408520c8b68648970d8
ms.openlocfilehash: f7206126bfa6150078f1bfb4f7e07c1cf2819ce0
ms.contentlocale: tr-tr
ms.lasthandoff: 02/07/2018

---
# <a name="create-a-model-mapping-configuration-er"></a><span data-ttu-id="d546f-103">Model eşleme yapılandırması oluşturma (ER)</span><span class="sxs-lookup"><span data-stu-id="d546f-103">Create a model mapping configuration (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d546f-104">Yeni bir Elektronik raporlama (ER) modeli eşleme yapılandırması tasarlamak ve etkili toplam hesaplamalar için yerleşik ER işlevlerini kullanmak için bu yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="d546f-104">Use this procedure to design a new Electronic reporting (ER) model mapping configuration and use built-in ER functions for efficient aggregate calculations.</span></span> <span data-ttu-id="d546f-105">Bu yordamda, Litware, Inc. örnek şirketi için bir yapılandırma oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="d546f-105">In this procedure, you will create a configuration for sample company, Litware, Inc.</span></span> 

<span data-ttu-id="d546f-106">Bu yordam, Sistem yöneticisi veya Elektronik raporlama geliştiricisi rolüne atanmış kullanıcılar için oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="d546f-106">This procedure is created for uses with the assigned role of System administrator or Electronic reporting developer.</span></span>

<span data-ttu-id="d546f-107">Bu adımlar herhangi bir veri kümesi kullanılarak tamamlanabilir.</span><span class="sxs-lookup"><span data-stu-id="d546f-107">These steps can be completed using any dataset.</span></span> <span data-ttu-id="d546f-108">Bu adımları tamamlamak için ilk olarak "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d546f-108">To complete these steps, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active.”</span></span>

1. <span data-ttu-id="d546f-109">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="d546f-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="d546f-110">Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve etkin olarak işaretlemiş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="d546f-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="d546f-111">Bu yapılandırma sağlayıcısını göremiyorsanız "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="d546f-111">If you don’t see this configuration provider, complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>  
2. <span data-ttu-id="d546f-112">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d546f-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="d546f-113">Filtreleri göster'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d546f-113">Click Show filters.</span></span>
4. <span data-ttu-id="d546f-114">"Ad" alanına "Intrastat" filtre değerini girin ve "ile başlar" filtre işlecini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d546f-114">In the "Name" field, enter the filter value, "Intrastat" and use the filter operator "begins with".</span></span>
    * <span data-ttu-id="d546f-115">'Intrastat' veri modeli yapılandırmasını bulmak için bu filtreyi uygulayın.</span><span class="sxs-lookup"><span data-stu-id="d546f-115">Apply this filter to find the ‘Intrastat’ data model configuration.</span></span> <span data-ttu-id="d546f-116">Bu model zaten yapılandırmalar ağacında bulunuyor olabilir.</span><span class="sxs-lookup"><span data-stu-id="d546f-116">This model may already exist in the configurations tree.</span></span> <span data-ttu-id="d546f-117">Varsa, bir sonraki alt görevi atlayın.</span><span class="sxs-lookup"><span data-stu-id="d546f-117">If it does, skip the next sub-task.</span></span>   

## <a name="get-the-intrastat-model-configuration-provided-by-microsoft"></a><span data-ttu-id="d546f-118">Microsoft tarafından sağlanan Intrastat modeli yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="d546f-118">Get the Intrastat model configuration provided by Microsoft</span></span>
1. <span data-ttu-id="d546f-119">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="d546f-119">Close the page.</span></span>
2. <span data-ttu-id="d546f-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="d546f-120">Close the page.</span></span>
3. <span data-ttu-id="d546f-121">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="d546f-121">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
4. <span data-ttu-id="d546f-122">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="d546f-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d546f-123">Microsoft sağlayıcısı kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="d546f-123">Select the Microsoft provider tile.</span></span>  
5. <span data-ttu-id="d546f-124">Depolar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d546f-124">Click Repositories.</span></span>
    * <span data-ttu-id="d546f-125">Microsoft sağlayıcısı kutucuğunda Depolar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d546f-125">Click Repositories in the Microsoft provider tile.</span></span>  
6. <span data-ttu-id="d546f-126">Filtreleri göster'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d546f-126">Click Show filters.</span></span>
7. <span data-ttu-id="d546f-127">"Tür adı" alanına "kaynaklar" filtre değerini girin ve "içerir" filtre işlecini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d546f-127">In the "Type name" field, enter the filter value, “resources” and use the filter operator "contains".</span></span> 
8. <span data-ttu-id="d546f-128">Aç'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d546f-128">Click Open.</span></span>
9. <span data-ttu-id="d546f-129">Ağaçta, 'Intrastat modeli' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d546f-129">In the tree, select 'Intrastat model'.</span></span>
10. <span data-ttu-id="d546f-130">İçe aktar'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d546f-130">Click Import.</span></span>
11. <span data-ttu-id="d546f-131">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d546f-131">Click Yes.</span></span>
    * <span data-ttu-id="d546f-132">Yeni ER işlevinin nasıl kullanılacağını keşfetmek için kullanacağınız veri modelini içeren ER modeli yapılandırmasını içe aktardınız.</span><span class="sxs-lookup"><span data-stu-id="d546f-132">You imported the ER model configuration that contains the data model that you will use to explore how the new ER functionality can be used.</span></span>  
12. <span data-ttu-id="d546f-133">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="d546f-133">Close the page.</span></span>
13. <span data-ttu-id="d546f-134">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="d546f-134">Close the page.</span></span>
14. <span data-ttu-id="d546f-135">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d546f-135">Click Reporting configurations.</span></span>

## <a name="add-a-new-model-mapping-configuration"></a><span data-ttu-id="d546f-136">Yeni bir model eşleme yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="d546f-136">Add a new model mapping configuration</span></span>
1. <span data-ttu-id="d546f-137">Ağaçta, 'Intrastat modeli' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d546f-137">In the tree, select 'Intrastat model'.</span></span>
2. <span data-ttu-id="d546f-138">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d546f-138">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="d546f-139">Yeni alanına, "Intrastat veri modeline dayalı model eşlemesi" yazın.</span><span class="sxs-lookup"><span data-stu-id="d546f-139">In the New field, enter 'Model Mapping based on data model Intrastat'.</span></span>
4. <span data-ttu-id="d546f-140">Ad alanına 'Intrastat örnek eşlemesi' yazın.</span><span class="sxs-lookup"><span data-stu-id="d546f-140">In the Name field, type 'Intrastat sample mapping'.</span></span>
    * <span data-ttu-id="d546f-141">Intrastat örneği eşleme</span><span class="sxs-lookup"><span data-stu-id="d546f-141">Intrastat sample mapping</span></span>  
5. <span data-ttu-id="d546f-142">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d546f-142">Click Create configuration.</span></span>

