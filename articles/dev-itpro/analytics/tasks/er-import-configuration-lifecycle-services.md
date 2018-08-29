--- 
title: "Lifecycle Services'dan Elektronik raporlama yapılandırmalarını içeri aktarma"
description: "Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcı, yeni bir Elektronik Raporlama (ER) sürümü oluşturabilir. ve bunu Microsoft Lifecycle Services (LCS)'den içe aktarabilir."
author: NickSelin
manager: AnnBe
ms.date: 05/13/2016
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: f3b8cdb722cf49194faccc19fbb95265a230d48b
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---
# <a name="import-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="2e1fc-103">Lifecycle Services'dan Elektronik raporlama yapılandırmalarını içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="2e1fc-103">Import Electronic reporting configurations from Lifecycle Services</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2e1fc-104">Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcı, yeni bir Elektronik Raporlama (ER) sürümü oluşturabilir. ve bunu Microsoft Lifecycle Services (LCS)'den içe aktarabilir.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="2e1fc-105">Bu örnekte Litware, Inc. örnek şirketi için bir istenilen ER yapılandırmasını seçecek ve bunu LCS'ye içe aktaracaksınız. Bu adımlar, ER yapılandırmaları şirketler arasında paylaşımlı olduğundan herhangi bir şirkette gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-105">In this example, you will select the desired version of the ER configuration and import it for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="2e1fc-106">Bu adımları tamamlamak için, öncelikle "Bir ER yapılandırmasını Lifecycle Services'a içeri almak" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-106">To complete these steps, you must first complete the steps in the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="2e1fc-107">Bu adımları tamamlamak için LCS erişimi de gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="2e1fc-108">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="2e1fc-109">Yapılandırmalar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-109">Click Configurations.</span></span>

## <a name="delete-a-shared-version-of-data-model-configuration"></a><span data-ttu-id="2e1fc-110">Veri modeli yapılandırmasının paylaşılan bir sürümünü silin</span><span class="sxs-lookup"><span data-stu-id="2e1fc-110">Delete a shared version of data model configuration</span></span>
1. <span data-ttu-id="2e1fc-111">Ağaçta seçin 'Örnek model yapılandırması' seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-111">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="2e1fc-112">Örnek veri modeli yapılandırmasının ilk sürümü oluşturuldu ve LCS'ye "ER yapılandırmasını Lifecycle Services'a karşıya yüklemek" yordamında yayımlandı.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-112">The first version of a sample data model configuration has been created and published to LCS during the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="2e1fc-113">Bu yordamda, ER yapılandırmasının bu sürümünü sileceksiniz.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-113">In this procedure, you will delete this version of the ER configuration.</span></span> <span data-ttu-id="2e1fc-114">Bir örnek veri modeli yapılandırmasının bu modeli daha sonra LCS'den içe aktarılacaktır.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-114">This version of a sample data model configuration will be imported later from LCS.</span></span>  
2. <span data-ttu-id="2e1fc-115">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2e1fc-116">Bu yapılandırmanın 'Paylaşımlı' durumda olan sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-116">Select the version of this configuration that is in the ‘Shared’ status.</span></span> <span data-ttu-id="2e1fc-117">Bu durum, yapılandırmanın LCS için yayımlandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-117">This status indicates that the configuration has been published to LCS.</span></span>  
3. <span data-ttu-id="2e1fc-118">Durumu değiştir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-118">Click Change status.</span></span>
4. <span data-ttu-id="2e1fc-119">Devam ettirme'ye tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-119">Click Discontinue.</span></span>
    * <span data-ttu-id="2e1fc-120">Seçili sürümün durumunu, silinebilir duruma gelmesi için 'Paylaşılan'dan 'Devam ettirilmeyen' olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-120">Change the status of the selected version from ‘Shared’ to ‘Discontinued’ to make it available for deletion.</span></span>  
5. <span data-ttu-id="2e1fc-121">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-121">Click OK.</span></span>
6. <span data-ttu-id="2e1fc-122">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2e1fc-123">Bu yapılandırmanın 'Devam ettirilmeyen' durumda olan sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-123">Select the version of this configuration that has a status of ‘Discontinued’.</span></span>  
7. <span data-ttu-id="2e1fc-124">Sil'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-124">Click Delete.</span></span>
8. <span data-ttu-id="2e1fc-125">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-125">Click Yes.</span></span>
    * <span data-ttu-id="2e1fc-126">Yalnızca seçili veri modeli yapılandırması için taslak sürümü 2'nin kullanılabilir olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-126">Note that the only draft version 2 of the selected data model configuration is available.</span></span>  
9. <span data-ttu-id="2e1fc-127">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-127">Close the page.</span></span>

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a><span data-ttu-id="2e1fc-128">Veri modeli yapılandırmasının paylaşılan bir sürümünü LCS'den içeri alın</span><span class="sxs-lookup"><span data-stu-id="2e1fc-128">Import a shared version of data model configuration from LCS</span></span>
1. <span data-ttu-id="2e1fc-129">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="2e1fc-130">'Litware, Inc.' yapılandırma sağlayıcısı için havuzların listesini açın.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-130">Open the list of repositories for the ‘Litware, Inc.’</span></span> <span data-ttu-id="2e1fc-131">yapılandırma sağlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-131">configuration provider.</span></span>  
2. <span data-ttu-id="2e1fc-132">Depolar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-132">Click Repositories.</span></span>
3. <span data-ttu-id="2e1fc-133">Aç'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-133">Click Open.</span></span>
    * <span data-ttu-id="2e1fc-134">LCS deposunu seçin ve açın.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-134">Select the LCS repository and open it.</span></span>  
4. <span data-ttu-id="2e1fc-135">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-135">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="2e1fc-136">'Örnek yapılandırma modeli'nin ilk sürümü sürümlerin listesinde seçin.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-136">Select the first version of the 'Sample model configuration' in the versions list.</span></span>  
5. <span data-ttu-id="2e1fc-137">İçe aktar'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-137">Click Import.</span></span>
6. <span data-ttu-id="2e1fc-138">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-138">Click Yes.</span></span>
    * <span data-ttu-id="2e1fc-139">Seçili sürümün LCS'den aktarıldığını onaylayın.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-139">Confirm the import of the selected version from LCS .</span></span>  
    * <span data-ttu-id="2e1fc-140">Bilgi iletisinin (formun üstünde bulunan) seçili sürümün alma işleminin başarılı tamamlama onayladığını dikkate alın.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-140">Note that the information message (above the form) confirms the successful completion of the import of the selected version.</span></span>  
7. <span data-ttu-id="2e1fc-141">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-141">Close the page.</span></span>
8. <span data-ttu-id="2e1fc-142">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-142">Close the page.</span></span>
9. <span data-ttu-id="2e1fc-143">Yapılandırmalar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-143">Click Configurations.</span></span>
10. <span data-ttu-id="2e1fc-144">Ağaçta seçin 'Örnek model yapılandırması' seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-144">In the tree, select 'Sample model configuration'.</span></span>
11. <span data-ttu-id="2e1fc-145">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2e1fc-146">Bu yapılandırmanın 'Paylaşılan' durumda olan sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-146">Select the version of this configuration that has a status of ‘Shared’.</span></span>  
    * <span data-ttu-id="2e1fc-147">Yalnızca seçili veri modeli yapılandırması için paylaşılan sürümü 1'in de artık kullanılabilir olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="2e1fc-147">Note that the shared version 1 of the selected data model configuration is available now as well.</span></span>  


