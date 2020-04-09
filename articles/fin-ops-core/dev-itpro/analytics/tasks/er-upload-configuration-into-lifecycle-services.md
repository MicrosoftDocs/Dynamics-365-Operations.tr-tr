---
title: ER Lifecycle Services'a bir yapılandırma yükleme
description: Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcı, yeni bir Elektronik Raporlama (ER) oluşturabilir. ve bunu Microsoft Lifecycle Services (LCS)'ye yükleyebilir.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5def757de8fb9d347f5fd0f828039dad5c989c19
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143304"
---
# <a name="er-upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="7a2a4-103">ER Lifecycle Services'a bir yapılandırma yükleme</span><span class="sxs-lookup"><span data-stu-id="7a2a4-103">ER Upload a configuration into Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7a2a4-104">Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcı, yeni bir Elektronik Raporlama (ER) oluşturabilir. ve bunu Microsoft Lifecycle Services (LCS)'ye yükleyebilir.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration and upload it into Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="7a2a4-105">Bu örnekte Litware, Inc. örnek şirketi için bir yapılandırma oluşturacak ve bunu LCS'ye yükleyeceksiniz. Bu adımlar, ER yapılandırmaları şirketler arasında paylaşımlı olduğundan herhangi bir şirkette gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-105">In this example, you will create a configuration and upload it to LCS for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="7a2a4-106">Bu adımları tamamlamak için öncelikle "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-106">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span> <span data-ttu-id="7a2a4-107">Bu adımları tamamlamak için LCS erişimi de gereklidir.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="7a2a4-108">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="7a2a4-109">'Litware, Inc.'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-109">Select 'Litware, Inc.'</span></span> <span data-ttu-id="7a2a4-110">ve etkin olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-110">and set it as active.</span></span>
3. <span data-ttu-id="7a2a4-111">Yapılandırmalar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-111">Click Configurations.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="7a2a4-112">Yeni bir veri modeli yapılandırması oluşturun</span><span class="sxs-lookup"><span data-stu-id="7a2a4-112">Create a new data model configuration</span></span>
1. <span data-ttu-id="7a2a4-113">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-113">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="7a2a4-114">Elektronik belgeler için bir örnek veri modeli içeren bir yapılandırma oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-114">You will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="7a2a4-115">Bu veri modeli yapılandırması daha sonra LCS'ye yüklenecektir.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-115">This data model configuration will be uploaded into LCS later.</span></span>  
2. <span data-ttu-id="7a2a4-116">İsim alanında 'Örnek model yapılandırması' yazın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-116">In the Name field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="7a2a4-117">Örnek model yapılandırması</span><span class="sxs-lookup"><span data-stu-id="7a2a4-117">Sample model configuration</span></span>  
3. <span data-ttu-id="7a2a4-118">Açıklama alanına, 'Örnek model yapılandırması' yazın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-118">In the Description field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="7a2a4-119">Örnek model yapılandırması</span><span class="sxs-lookup"><span data-stu-id="7a2a4-119">Sample model configuration</span></span>  
4. <span data-ttu-id="7a2a4-120">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-120">Click Create configuration.</span></span>
5. <span data-ttu-id="7a2a4-121">Model tasarımcısı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-121">Click Model designer.</span></span>
6. <span data-ttu-id="7a2a4-122">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-122">Click New.</span></span>
7. <span data-ttu-id="7a2a4-123">İsim alanına 'Giriş noktası' yazın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-123">In the Name field, type 'Entry point'.</span></span>
    * <span data-ttu-id="7a2a4-124">Giriş noktası</span><span class="sxs-lookup"><span data-stu-id="7a2a4-124">Entry point</span></span>  
8. <span data-ttu-id="7a2a4-125">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-125">Click Add.</span></span>
9. <span data-ttu-id="7a2a4-126">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-126">Click Save.</span></span>
10. <span data-ttu-id="7a2a4-127">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-127">Close the page.</span></span>
11. <span data-ttu-id="7a2a4-128">Durumu değiştir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-128">Click Change status.</span></span>
12. <span data-ttu-id="7a2a4-129">Tamamla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-129">Click Complete.</span></span>
13. <span data-ttu-id="7a2a4-130">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-130">Click OK.</span></span>

## <a name="register-a-new--repository"></a><span data-ttu-id="7a2a4-131">Yeni bir havuz kaydedin</span><span class="sxs-lookup"><span data-stu-id="7a2a4-131">Register a new  repository</span></span>
1. <span data-ttu-id="7a2a4-132">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-132">Close the page.</span></span>
2. <span data-ttu-id="7a2a4-133">Depolar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-133">Click Repositories.</span></span>
    * <span data-ttu-id="7a2a4-134">Bu, Litware, Inc. için havuzların listesini açmanızı sağlayacaktır. yapılandırma sağlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-134">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
3. <span data-ttu-id="7a2a4-135">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-135">Click Add to open the drop dialog.</span></span>
    * <span data-ttu-id="7a2a4-136">Bu, yeni bir havuz eklemenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-136">This allows you to add a new repository.</span></span>  
4. <span data-ttu-id="7a2a4-137">Yapılandırma havuz türü alanında LCS'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-137">In the Configuration repository type field, select LCS.</span></span>
5. <span data-ttu-id="7a2a4-138">Havuz oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-138">Click Create repository.</span></span>
6. <span data-ttu-id="7a2a4-139">Proje alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-139">In the Project field, enter or select a value.</span></span>
    * <span data-ttu-id="7a2a4-140">İstenilen LCS projesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-140">Select the desired LCS project.</span></span> <span data-ttu-id="7a2a4-141">Projeye erişiminiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-141">You must have access to the project.</span></span>  
7. <span data-ttu-id="7a2a4-142">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-142">Click OK.</span></span>
    * <span data-ttu-id="7a2a4-143">Yeni bir havuz girişini tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-143">Complete a new repository entry.</span></span>  
8. <span data-ttu-id="7a2a4-144">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-144">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="7a2a4-145">LCS havuz kaydını seçin.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-145">Select the LCS repository record.</span></span>  
    * <span data-ttu-id="7a2a4-146">Mevcut sağlayıcı tarafından işaretlenen kayıtlı bir havuzun, yani sadece bu sağlayıcının sahip olduğu yapılandırmaların bu havuzda kullanılabileceğini ve bunun doğrultusunda, seçili LCS projesine karşıya yüklenebileceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-146">Note that a registered repository is marked by the current provider meaning that the only configurations owned by that provider can be placed to this repository and, consequently, uploaded into the selected LCS project.</span></span>  
9. <span data-ttu-id="7a2a4-147">Aç'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-147">Click Open.</span></span>
    * <span data-ttu-id="7a2a4-148">ER yapılandırmalarının listesini görüntülemek için havuzu açın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-148">Open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="7a2a4-149">Bu proje ER yapılandırmaları paylaşımı için henüz kullanılmamışsa, bu boş olacaktır.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-149">It will be empty if this project has not yet been used for ER configurations sharing.</span></span>  
10. <span data-ttu-id="7a2a4-150">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-150">Close the page.</span></span>
11. <span data-ttu-id="7a2a4-151">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-151">Close the page.</span></span>

## <a name="upload-configuration-into-lcs"></a><span data-ttu-id="7a2a4-152">Yapılandırmayı LCS'ye karşıya yükleyin</span><span class="sxs-lookup"><span data-stu-id="7a2a4-152">Upload configuration into LCS</span></span>
1. <span data-ttu-id="7a2a4-153">Yapılandırmalar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-153">Click Configurations.</span></span>
2. <span data-ttu-id="7a2a4-154">Ağaçta seçin 'Örnek model yapılandırması' seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-154">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="7a2a4-155">Tamamlanmış olan oluşturulan bir yapılandırmayı seçin.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-155">Select a created configuration that has been already completed.</span></span>  
3. <span data-ttu-id="7a2a4-156">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7a2a4-157">'Tamamlandı' durumuna sahip seçili konfigürasyona sahip sürümü seçin.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-157">Select the version of the selected configuration with the status of 'Completed'.</span></span>  
4. <span data-ttu-id="7a2a4-158">Durumu değiştir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-158">Click Change status.</span></span>
5. <span data-ttu-id="7a2a4-159">Paylaş'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-159">Click Share.</span></span>
    * <span data-ttu-id="7a2a4-160">LCS'de yayımlandığında yapılandırma durumu 'Tamamlandı' seçeneğinden 'Paylaşıldı' seçeneğine değişecektir.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-160">The configuration status will change from 'Completed' to 'Shared' when it is published in LCS.</span></span>  
6. <span data-ttu-id="7a2a4-161">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-161">Click OK.</span></span>
7. <span data-ttu-id="7a2a4-162">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-162">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7a2a4-163">'Paylaşıldı' durumuna sahip yapılandırma sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-163">Select the configuration version with the status of 'Shared'.</span></span>  
    * <span data-ttu-id="7a2a4-164">Seçili sürümün durumunun 'Paylaşılan'dan 'Tamamlandı'ya değiştiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-164">Note that the status of the selected version has changed from 'Completed' to 'Shared'.</span></span>  
8. <span data-ttu-id="7a2a4-165">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-165">Close the page.</span></span>
9. <span data-ttu-id="7a2a4-166">Depolar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-166">Click Repositories.</span></span>
    * <span data-ttu-id="7a2a4-167">Bu, Litware, Inc. için havuzların listesini açmanızı sağlayacaktır. yapılandırma sağlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-167">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
10. <span data-ttu-id="7a2a4-168">Aç'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-168">Click Open.</span></span>
    * <span data-ttu-id="7a2a4-169">LCS deposunu seçin ve açın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-169">Select the LCS repository and open it.</span></span>  
    * <span data-ttu-id="7a2a4-170">Not: Seçili yapılandırma, LCS projesinin seçili bir varlığı olarak gösterilir.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-170">Note that the selected configuration is shown as an asset of the selected LCS project.</span></span>  
    * <span data-ttu-id="7a2a4-171">https://lcs.dynamics.com kullanarak LCS'yi açın.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-171">Open LCS using https://lcs.dynamics.com.</span></span> <span data-ttu-id="7a2a4-172">Daha önce havuz kaydı için kullanılan bir proje açın, bu projenin 'Varlık kütüphanesini' açın ve 'Kural Yöneticisi yapılandırma' kıymet türünün içeriğini genişletin – karşıya yüklenen ER yapılandırma kullanılabilir olacaktır.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-172">Open a project that was used earlier for repository registration, open the 'Asset library' of this project, and expand the content of the 'GER configuration' asset type – the uploaded ER configuration will be available.</span></span> <span data-ttu-id="7a2a4-173">Not: Bu LCS projesine erişim sağlayıcısının erişimi varsa, karşıya yüklenen LCS yapılandırması başka bir örneğe aktarılabilir.</span><span class="sxs-lookup"><span data-stu-id="7a2a4-173">Note that the uploaded LCS configuration can be imported to another instance if providers have access to this LCS project.</span></span>  

