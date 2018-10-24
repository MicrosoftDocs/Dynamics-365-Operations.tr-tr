--- 
title: "ER Lifecycle Services'tan bir yapılandırmayı içe aktarma"
description: "Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcı, yeni bir Elektronik Raporlama (ER) sürümü oluşturabilir. ve bunu Microsoft Lifecycle Services (LCS)'den içe aktarabilir."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable,  ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 036d7e7e3f79e0945d6fef866a30edd41e688c07
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2018

---

# <a name="er-import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="c59da-103">ER Lifecycle Services'tan bir yapılandırmayı içe aktarma</span><span class="sxs-lookup"><span data-stu-id="c59da-103">ER Import a configuration from Lifecycle Services</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c59da-104">Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcı, yeni bir Elektronik Raporlama (ER) sürümü oluşturabilir. ve bunu Microsoft Lifecycle Services (LCS)'den içe aktarabilir.</span><span class="sxs-lookup"><span data-stu-id="c59da-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="c59da-105">Bu örnekte Litware, Inc. örnek şirketi için bir istenilen ER yapılandırmasını seçecek ve bunu LCS'ye içe aktaracaksınız. Bu adımlar, ER yapılandırmaları şirketler arasında paylaşımlı olduğundan herhangi bir şirkette gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="c59da-105">In this example, you will select the desired version of the ER configuration and import it for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="c59da-106">Bu adımları tamamlamak için, öncelikle "Bir ER yapılandırmasını Lifecycle Services'a içeri almak" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="c59da-106">To complete these steps, you must first complete the steps in the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="c59da-107">Bu adımları tamamlamak için LCS erişimi de gereklidir.</span><span class="sxs-lookup"><span data-stu-id="c59da-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="c59da-108">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="c59da-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="c59da-109">Yapılandırmalar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c59da-109">Click Configurations.</span></span>

## <a name="delete-a-shared-version-of-data-model-configuration"></a><span data-ttu-id="c59da-110">Veri modeli yapılandırmasının paylaşılan bir sürümünü silin</span><span class="sxs-lookup"><span data-stu-id="c59da-110">Delete a shared version of data model configuration</span></span>
1. <span data-ttu-id="c59da-111">Ağaçta seçin 'Örnek model yapılandırması' seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="c59da-111">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="c59da-112">Örnek veri modeli yapılandırmasının ilk sürümü oluşturuldu ve LCS'ye "ER yapılandırmasını Lifecycle Services'a karşıya yüklemek" yordamında yayımlandı.</span><span class="sxs-lookup"><span data-stu-id="c59da-112">The first version of a sample data model configuration has been created and published to LCS during the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="c59da-113">Bu yordamda, ER yapılandırmasının bu sürümünü sileceksiniz.</span><span class="sxs-lookup"><span data-stu-id="c59da-113">In this procedure, you will delete this version of the ER configuration.</span></span> <span data-ttu-id="c59da-114">Bir örnek veri modeli yapılandırmasının bu modeli daha sonra LCS'den içe aktarılacaktır.</span><span class="sxs-lookup"><span data-stu-id="c59da-114">This version of a sample data model configuration will be imported later from LCS.</span></span>  
2. <span data-ttu-id="c59da-115">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="c59da-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c59da-116">Bu yapılandırmanın 'Paylaşımlı' durumda olan sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="c59da-116">Select the version of this configuration that is in the ‘Shared’ status.</span></span> <span data-ttu-id="c59da-117">Bu durum, yapılandırmanın LCS için yayımlandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c59da-117">This status indicates that the configuration has been published to LCS.</span></span>  
3. <span data-ttu-id="c59da-118">Durumu değiştir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c59da-118">Click Change status.</span></span>
4. <span data-ttu-id="c59da-119">Devam ettirme'ye tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c59da-119">Click Discontinue.</span></span>
    * <span data-ttu-id="c59da-120">Seçili sürümün durumunu, silinebilir duruma gelmesi için 'Paylaşılan'dan 'Devam ettirilmeyen' olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="c59da-120">Change the status of the selected version from ‘Shared’ to ‘Discontinued’ to make it available for deletion.</span></span>  
5. <span data-ttu-id="c59da-121">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c59da-121">Click OK.</span></span>
6. <span data-ttu-id="c59da-122">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="c59da-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c59da-123">Bu yapılandırmanın 'Devam ettirilmeyen' durumda olan sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="c59da-123">Select the version of this configuration that has a status of ‘Discontinued’.</span></span>  
7. <span data-ttu-id="c59da-124">Sil'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c59da-124">Click Delete.</span></span>
8. <span data-ttu-id="c59da-125">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c59da-125">Click Yes.</span></span>
    * <span data-ttu-id="c59da-126">Yalnızca seçili veri modeli yapılandırması için taslak sürümü 2'nin kullanılabilir olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="c59da-126">Note that the only draft version 2 of the selected data model configuration is available.</span></span>  
9. <span data-ttu-id="c59da-127">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c59da-127">Close the page.</span></span>

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a><span data-ttu-id="c59da-128">Veri modeli yapılandırmasının paylaşılan bir sürümünü LCS'den içeri alın</span><span class="sxs-lookup"><span data-stu-id="c59da-128">Import a shared version of data model configuration from LCS</span></span>
1. <span data-ttu-id="c59da-129">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="c59da-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c59da-130">'Litware, Inc.' yapılandırma sağlayıcısı için havuzların listesini açın.</span><span class="sxs-lookup"><span data-stu-id="c59da-130">Open the list of repositories for the ‘Litware, Inc.’</span></span> <span data-ttu-id="c59da-131">yapılandırma sağlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="c59da-131">configuration provider.</span></span>  
2. <span data-ttu-id="c59da-132">Depolar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c59da-132">Click Repositories.</span></span>
3. <span data-ttu-id="c59da-133">Aç'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c59da-133">Click Open.</span></span>
    * <span data-ttu-id="c59da-134">LCS deposunu seçin ve açın.</span><span class="sxs-lookup"><span data-stu-id="c59da-134">Select the LCS repository and open it.</span></span>  
4. <span data-ttu-id="c59da-135">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="c59da-135">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c59da-136">'Örnek yapılandırma modeli'nin ilk sürümü sürümlerin listesinde seçin.</span><span class="sxs-lookup"><span data-stu-id="c59da-136">Select the first version of the 'Sample model configuration' in the versions list.</span></span>  
5. <span data-ttu-id="c59da-137">İçe aktar'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c59da-137">Click Import.</span></span>
6. <span data-ttu-id="c59da-138">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c59da-138">Click Yes.</span></span>
    * <span data-ttu-id="c59da-139">Seçili sürümün LCS'den aktarıldığını onaylayın.</span><span class="sxs-lookup"><span data-stu-id="c59da-139">Confirm the import of the selected version from LCS .</span></span>  
    * <span data-ttu-id="c59da-140">Bilgi iletisinin (formun üstünde bulunan) seçili sürümün alma işleminin başarılı tamamlama onayladığını dikkate alın.</span><span class="sxs-lookup"><span data-stu-id="c59da-140">Note that the information message (above the form) confirms the successful completion of the import of the selected version.</span></span>  
7. <span data-ttu-id="c59da-141">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c59da-141">Close the page.</span></span>
8. <span data-ttu-id="c59da-142">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c59da-142">Close the page.</span></span>
9. <span data-ttu-id="c59da-143">Yapılandırmalar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c59da-143">Click Configurations.</span></span>
10. <span data-ttu-id="c59da-144">Ağaçta seçin 'Örnek model yapılandırması' seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="c59da-144">In the tree, select 'Sample model configuration'.</span></span>
11. <span data-ttu-id="c59da-145">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="c59da-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c59da-146">Bu yapılandırmanın 'Paylaşılan' durumda olan sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="c59da-146">Select the version of this configuration that has a status of ‘Shared’.</span></span>  
    * <span data-ttu-id="c59da-147">Yalnızca seçili veri modeli yapılandırması için paylaşılan sürümü 1'in de artık kullanılabilir olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="c59da-147">Note that the shared version 1 of the selected data model configuration is available now as well.</span></span>  


