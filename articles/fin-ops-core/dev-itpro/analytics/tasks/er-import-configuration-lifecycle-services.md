---
title: ER Lifecycle Services'tan bir yapılandırmayı içe aktarma
description: Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcı, yeni bir Elektronik Raporlama (ER) sürümü oluşturabilir. ve bunu Microsoft Lifecycle Services (LCS)'den içe aktarabilir.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable,  ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 67e09e3187ac49e12727116f55066b64a386e2de
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142398"
---
# <a name="er-import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="6f012-103">ER Lifecycle Services'tan bir yapılandırmayı içe aktarma</span><span class="sxs-lookup"><span data-stu-id="6f012-103">ER Import a configuration from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6f012-104">Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcı, yeni bir Elektronik Raporlama (ER) sürümü oluşturabilir. ve bunu Microsoft Lifecycle Services (LCS)'den içe aktarabilir.</span><span class="sxs-lookup"><span data-stu-id="6f012-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="6f012-105">Bu örnekte Litware, Inc. örnek şirketi için bir istenilen ER yapılandırmasını seçecek ve bunu LCS'ye içe aktaracaksınız. Bu adımlar, ER yapılandırmaları şirketler arasında paylaşımlı olduğundan herhangi bir şirkette gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="6f012-105">In this example, you will select the desired version of the ER configuration and import it for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="6f012-106">Bu adımları tamamlamak için, öncelikle "Bir ER yapılandırmasını Lifecycle Services'a içeri almak" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="6f012-106">To complete these steps, you must first complete the steps in the "Upload an ER configuration into Lifecycle Services" procedure.</span></span> <span data-ttu-id="6f012-107">Bu adımları tamamlamak için LCS erişimi de gereklidir.</span><span class="sxs-lookup"><span data-stu-id="6f012-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="6f012-108">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="6f012-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="6f012-109">Yapılandırmalar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f012-109">Click Configurations.</span></span>

## <a name="delete-a-shared-version-of-data-model-configuration"></a><span data-ttu-id="6f012-110">Veri modeli yapılandırmasının paylaşılan bir sürümünü silin</span><span class="sxs-lookup"><span data-stu-id="6f012-110">Delete a shared version of data model configuration</span></span>
1. <span data-ttu-id="6f012-111">Ağaçta seçin 'Örnek model yapılandırması' seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="6f012-111">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="6f012-112">Örnek veri modeli yapılandırmasının ilk sürümü oluşturuldu ve LCS'ye "ER yapılandırmasını Lifecycle Services'a karşıya yüklemek" yordamında yayımlandı.</span><span class="sxs-lookup"><span data-stu-id="6f012-112">The first version of a sample data model configuration has been created and published to LCS during the "Upload an ER configuration into Lifecycle Services" procedure.</span></span> <span data-ttu-id="6f012-113">Bu yordamda, ER yapılandırmasının bu sürümünü sileceksiniz.</span><span class="sxs-lookup"><span data-stu-id="6f012-113">In this procedure, you will delete this version of the ER configuration.</span></span> <span data-ttu-id="6f012-114">Bir örnek veri modeli yapılandırmasının bu modeli daha sonra LCS'den içe aktarılacaktır.</span><span class="sxs-lookup"><span data-stu-id="6f012-114">This version of a sample data model configuration will be imported later from LCS.</span></span>  
2. <span data-ttu-id="6f012-115">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="6f012-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6f012-116">Bu yapılandırmanın 'Paylaşımlı' durumda olan sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="6f012-116">Select the version of this configuration that is in the 'Shared' status.</span></span> <span data-ttu-id="6f012-117">Bu durum, yapılandırmanın LCS için yayımlandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6f012-117">This status indicates that the configuration has been published to LCS.</span></span>  
3. <span data-ttu-id="6f012-118">Durumu değiştir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f012-118">Click Change status.</span></span>
4. <span data-ttu-id="6f012-119">Devam ettirme'ye tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6f012-119">Click Discontinue.</span></span>
    * <span data-ttu-id="6f012-120">Seçili sürümün durumunu, silinebilir duruma gelmesi için 'Paylaşılan'dan 'Devam ettirilmeyen' olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="6f012-120">Change the status of the selected version from 'Shared' to 'Discontinued' to make it available for deletion.</span></span>  
5. <span data-ttu-id="6f012-121">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f012-121">Click OK.</span></span>
6. <span data-ttu-id="6f012-122">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="6f012-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6f012-123">Bu yapılandırmanın 'Devam ettirilmeyen' durumda olan sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="6f012-123">Select the version of this configuration that has a status of 'Discontinued'.</span></span>  
7. <span data-ttu-id="6f012-124">Sil'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6f012-124">Click Delete.</span></span>
8. <span data-ttu-id="6f012-125">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6f012-125">Click Yes.</span></span>
    * <span data-ttu-id="6f012-126">Yalnızca seçili veri modeli yapılandırması için taslak sürümü 2'nin kullanılabilir olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="6f012-126">Note that the only draft version 2 of the selected data model configuration is available.</span></span>  
9. <span data-ttu-id="6f012-127">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6f012-127">Close the page.</span></span>

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a><span data-ttu-id="6f012-128">Veri modeli yapılandırmasının paylaşılan bir sürümünü LCS'den içeri alın</span><span class="sxs-lookup"><span data-stu-id="6f012-128">Import a shared version of data model configuration from LCS</span></span>
1. <span data-ttu-id="6f012-129">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="6f012-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="6f012-130">'Litware, Inc.' yapılandırma sağlayıcısı için havuzların listesini açın.</span><span class="sxs-lookup"><span data-stu-id="6f012-130">Open the list of repositories for the 'Litware, Inc.'</span></span> <span data-ttu-id="6f012-131">yapılandırma sağlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="6f012-131">configuration provider.</span></span>  
2. <span data-ttu-id="6f012-132">Depolar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f012-132">Click Repositories.</span></span>
3. <span data-ttu-id="6f012-133">Aç'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f012-133">Click Open.</span></span>
    * <span data-ttu-id="6f012-134">LCS deposunu seçin ve açın.</span><span class="sxs-lookup"><span data-stu-id="6f012-134">Select the LCS repository and open it.</span></span>  
4. <span data-ttu-id="6f012-135">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="6f012-135">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="6f012-136">'Örnek yapılandırma modeli'nin ilk sürümü sürümlerin listesinde seçin.</span><span class="sxs-lookup"><span data-stu-id="6f012-136">Select the first version of the 'Sample model configuration' in the versions list.</span></span>  
5. <span data-ttu-id="6f012-137">İçe aktar'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6f012-137">Click Import.</span></span>
6. <span data-ttu-id="6f012-138">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6f012-138">Click Yes.</span></span>
    * <span data-ttu-id="6f012-139">Seçili sürümün LCS'den aktarıldığını onaylayın.</span><span class="sxs-lookup"><span data-stu-id="6f012-139">Confirm the import of the selected version from LCS .</span></span>  
    * <span data-ttu-id="6f012-140">Bilgi iletisinin (formun üstünde bulunan) seçili sürümün alma işleminin başarılı tamamlama onayladığını dikkate alın.</span><span class="sxs-lookup"><span data-stu-id="6f012-140">Note that the information message (above the form) confirms the successful completion of the import of the selected version.</span></span>  
7. <span data-ttu-id="6f012-141">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6f012-141">Close the page.</span></span>
8. <span data-ttu-id="6f012-142">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6f012-142">Close the page.</span></span>
9. <span data-ttu-id="6f012-143">Yapılandırmalar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6f012-143">Click Configurations.</span></span>
10. <span data-ttu-id="6f012-144">Ağaçta seçin 'Örnek model yapılandırması' seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="6f012-144">In the tree, select 'Sample model configuration'.</span></span>
11. <span data-ttu-id="6f012-145">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="6f012-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6f012-146">Bu yapılandırmanın 'Paylaşılan' durumda olan sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="6f012-146">Select the version of this configuration that has a status of 'Shared'.</span></span>  
    * <span data-ttu-id="6f012-147">Yalnızca seçili veri modeli yapılandırması için paylaşılan sürümü 1'in de artık kullanılabilir olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="6f012-147">Note that the shared version 1 of the selected data model configuration is available now as well.</span></span>  

