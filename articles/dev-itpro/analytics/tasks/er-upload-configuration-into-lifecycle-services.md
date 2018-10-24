--- 
title: "ER Lifecycle Services'a bir yapılandırma yükleme"
description: "Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcı, yeni bir Elektronik Raporlama (ER) oluşturabilir. ve bunu Microsoft Lifecycle Services (LCS)'ye yükleyebilir."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 19ae8820e5d4a798a5789e9632edb431fe9fede4
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2018

---
# <a name="er-upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="cfcbb-103">ER Lifecycle Services'a bir yapılandırma yükleme</span><span class="sxs-lookup"><span data-stu-id="cfcbb-103">ER Upload a configuration into Lifecycle Services</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cfcbb-104">Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcı, yeni bir Elektronik Raporlama (ER) oluşturabilir. ve bunu Microsoft Lifecycle Services (LCS)'ye yükleyebilir.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration and upload it into Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="cfcbb-105">Bu örnekte Litware, Inc. örnek şirketi için bir yapılandırma oluşturacak ve bunu LCS'ye yükleyeceksiniz. Bu adımlar, ER yapılandırmaları şirketler arasında paylaşımlı olduğundan herhangi bir şirkette gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-105">In this example, you will create a configuration and upload it to LCS for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="cfcbb-106">Bu adımları tamamlamak için, öncelikle "Bir yapılandırma sağlayıcı oluşturun ve etkin olarak işaretleyin" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="cfcbb-107">Bu adımları tamamlamak için LCS erişimi de gereklidir.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="cfcbb-108">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="cfcbb-109">'Litware, Inc.'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-109">Select ‘Litware, Inc.’</span></span> <span data-ttu-id="cfcbb-110">ve etkin olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-110">and set it as active.</span></span>
3. <span data-ttu-id="cfcbb-111">Yapılandırmalar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-111">Click Configurations.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="cfcbb-112">Yeni bir veri modeli yapılandırması oluşturun</span><span class="sxs-lookup"><span data-stu-id="cfcbb-112">Create a new data model configuration</span></span>
1. <span data-ttu-id="cfcbb-113">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-113">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="cfcbb-114">Elektronik belgeler için bir örnek veri modeli içeren bir yapılandırma oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-114">You will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="cfcbb-115">Bu veri modeli yapılandırması daha sonra LCS'ye yüklenecektir.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-115">This data model configuration will be uploaded into LCS later.</span></span>  
2. <span data-ttu-id="cfcbb-116">İsim alanında 'Örnek model yapılandırması' yazın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-116">In the Name field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="cfcbb-117">Örnek model yapılandırması</span><span class="sxs-lookup"><span data-stu-id="cfcbb-117">Sample model configuration</span></span>  
3. <span data-ttu-id="cfcbb-118">Açıklama alanına, 'Örnek model yapılandırması' yazın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-118">In the Description field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="cfcbb-119">Örnek model yapılandırması</span><span class="sxs-lookup"><span data-stu-id="cfcbb-119">Sample model configuration</span></span>  
4. <span data-ttu-id="cfcbb-120">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-120">Click Create configuration.</span></span>
5. <span data-ttu-id="cfcbb-121">Model tasarımcısı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-121">Click Model designer.</span></span>
6. <span data-ttu-id="cfcbb-122">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-122">Click New.</span></span>
7. <span data-ttu-id="cfcbb-123">İsim alanına 'Giriş noktası' yazın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-123">In the Name field, type 'Entry point'.</span></span>
    * <span data-ttu-id="cfcbb-124">Giriş noktası</span><span class="sxs-lookup"><span data-stu-id="cfcbb-124">Entry point</span></span>  
8. <span data-ttu-id="cfcbb-125">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-125">Click Add.</span></span>
9. <span data-ttu-id="cfcbb-126">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-126">Click Save.</span></span>
10. <span data-ttu-id="cfcbb-127">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-127">Close the page.</span></span>
11. <span data-ttu-id="cfcbb-128">Durumu değiştir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-128">Click Change status.</span></span>
12. <span data-ttu-id="cfcbb-129">Tamamla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-129">Click Complete.</span></span>
13. <span data-ttu-id="cfcbb-130">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-130">Click OK.</span></span>

## <a name="register-a-new--repository"></a><span data-ttu-id="cfcbb-131">Yeni bir havuz kaydedin</span><span class="sxs-lookup"><span data-stu-id="cfcbb-131">Register a new  repository</span></span>
1. <span data-ttu-id="cfcbb-132">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-132">Close the page.</span></span>
2. <span data-ttu-id="cfcbb-133">Depolar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-133">Click Repositories.</span></span>
    * <span data-ttu-id="cfcbb-134">Bu, Litware, Inc. için havuzların listesini açmanızı sağlayacaktır. yapılandırma sağlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-134">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
3. <span data-ttu-id="cfcbb-135">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-135">Click Add to open the drop dialog.</span></span>
    * <span data-ttu-id="cfcbb-136">Bu, yeni bir havuz eklemenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-136">This allows you to add a new repository.</span></span>  
4. <span data-ttu-id="cfcbb-137">Yapılandırma havuz türü alanında LCS'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-137">In the Configuration repository type field, select LCS.</span></span>
5. <span data-ttu-id="cfcbb-138">Havuz oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-138">Click Create repository.</span></span>
6. <span data-ttu-id="cfcbb-139">Proje alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-139">In the Project field, enter or select a value.</span></span>
    * <span data-ttu-id="cfcbb-140">İstenilen LCS projesini seçin.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-140">Select the desired LCS project.</span></span> <span data-ttu-id="cfcbb-141">Projeye erişiminiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-141">You must have access to the project.</span></span>  
7. <span data-ttu-id="cfcbb-142">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-142">Click OK.</span></span>
    * <span data-ttu-id="cfcbb-143">Yeni bir havuz girişini tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-143">Complete a new repository entry.</span></span>  
8. <span data-ttu-id="cfcbb-144">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-144">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="cfcbb-145">LCS havuz kaydını seçin.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-145">Select the LCS repository record.</span></span>  
    * <span data-ttu-id="cfcbb-146">Mevcut sağlayıcı tarafından işaretlenen kayıtlı bir havuzun, yani sadece bu sağlayıcının sahip olduğu yapılandırmaların bu havuzda kullanılabileceğini ve bunun doğrultusunda, seçili LCS projesine karşıya yüklenebileceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-146">Note that a registered repository is marked by the current provider meaning that the only configurations owned by that provider can be placed to this repository and, consequently, uploaded into the selected LCS project.</span></span>  
9. <span data-ttu-id="cfcbb-147">Aç'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-147">Click Open.</span></span>
    * <span data-ttu-id="cfcbb-148">ER yapılandırmalarının listesini görüntülemek için havuzu açın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-148">Open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="cfcbb-149">Bu proje ER yapılandırmaları paylaşımı için henüz kullanılmamışsa, bu boş olacaktır.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-149">It will be empty if this project has not yet been used for ER configurations sharing.</span></span>  
10. <span data-ttu-id="cfcbb-150">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-150">Close the page.</span></span>
11. <span data-ttu-id="cfcbb-151">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-151">Close the page.</span></span>

## <a name="upload-configuration-into-lcs"></a><span data-ttu-id="cfcbb-152">Yapılandırmayı LCS'ye karşıya yükleyin</span><span class="sxs-lookup"><span data-stu-id="cfcbb-152">Upload configuration into LCS</span></span>
1. <span data-ttu-id="cfcbb-153">Yapılandırmalar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-153">Click Configurations.</span></span>
2. <span data-ttu-id="cfcbb-154">Ağaçta seçin 'Örnek model yapılandırması' seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-154">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="cfcbb-155">Tamamlanmış olan oluşturulan bir yapılandırmayı seçin.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-155">Select a created configuration that has been already completed.</span></span>  
3. <span data-ttu-id="cfcbb-156">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="cfcbb-157">'Tamamlandı' durumuna sahip seçili konfigürasyona sahip sürümü seçin.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-157">Select the version of the selected configuration with the status of ‘Completed’.</span></span>  
4. <span data-ttu-id="cfcbb-158">Durumu değiştir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-158">Click Change status.</span></span>
5. <span data-ttu-id="cfcbb-159">Paylaş'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-159">Click Share.</span></span>
    * <span data-ttu-id="cfcbb-160">LCS'de yayımlandığında yapılandırma durumu 'Tamamlandı' seçeneğinden 'Paylaşıldı' seçeneğine değişecektir.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-160">The configuration status will change from ‘Completed’ to ‘Shared’ when it is published in LCS.</span></span>  
6. <span data-ttu-id="cfcbb-161">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-161">Click OK.</span></span>
7. <span data-ttu-id="cfcbb-162">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-162">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="cfcbb-163">'Paylaşıldı' durumuna sahip yapılandırma sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-163">Select the configuration version with the status of 'Shared'.</span></span>  
    * <span data-ttu-id="cfcbb-164">Seçili sürümün durumunun 'Paylaşılan'dan 'Tamamlandı'ya değiştiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-164">Note that the status of the selected version has changed from ‘Completed’ to ‘Shared’.</span></span>  
8. <span data-ttu-id="cfcbb-165">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-165">Close the page.</span></span>
9. <span data-ttu-id="cfcbb-166">Depolar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-166">Click Repositories.</span></span>
    * <span data-ttu-id="cfcbb-167">Bu, Litware, Inc. için havuzların listesini açmanızı sağlayacaktır. yapılandırma sağlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-167">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
10. <span data-ttu-id="cfcbb-168">Aç'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-168">Click Open.</span></span>
    * <span data-ttu-id="cfcbb-169">LCS deposunu seçin ve açın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-169">Select the LCS repository and open it.</span></span>  
    * <span data-ttu-id="cfcbb-170">Not: Seçili yapılandırma, LCS projesinin seçili bir varlığı olarak gösterilir.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-170">Note that the selected configuration is shown as an asset of the selected LCS project.</span></span>  
    * <span data-ttu-id="cfcbb-171">https://lcs.dynamics.com kullanarak LCS'yi açın.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-171">Open LCS using https://lcs.dynamics.com.</span></span> <span data-ttu-id="cfcbb-172">Daha önce havuz kaydı için kullanılan bir proje açın, bu projenin 'Varlık kütüphanesini' açın ve 'Kural Yöneticisi yapılandırma' kıymet türünün içeriğini genişletin – karşıya yüklenen ER yapılandırma kullanılabilir olacaktır.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-172">Open a project that was used earlier for repository registration, open the ‘Asset library’ of this project, and expand the content of the ‘GER configuration’ asset type – the uploaded ER configuration will be available.</span></span> <span data-ttu-id="cfcbb-173">Not: Bu LCS projesine erişim sağlayıcısının erişimi varsa, karşıya yüklenen LCS yapılandırmasını başka bir Microsoft Dynamics 365 for Finance and Operations, Enterprise edition örneğine alınabilir.</span><span class="sxs-lookup"><span data-stu-id="cfcbb-173">Note that the uploaded LCS configuration can be imported to another Microsoft Dynamics 365 for Finance and Operations, Enterprise edition instance if providers have access to this LCS project.</span></span>  


