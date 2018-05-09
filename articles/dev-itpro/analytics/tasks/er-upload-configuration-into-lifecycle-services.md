--- 
title: "Elektronik raporlama (ER) için Lifecycle Services'a bir yapılandırmayı yükleme"
description: "Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcı, yeni bir Elektronik Raporlama (ER) oluşturabilir. ve bunu Microsoft Lifecycle Services (LCS)'ye yükleyebilir."
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 41e114ee3e76c3989fcf9a57046cbb20a96798db
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---
# <a name="upload-a-configuration-into-lifecycle-services-for-electronic-reporting-er"></a><span data-ttu-id="61029-103">Elektronik raporlama (ER) için Lifecycle Services'a bir yapılandırmayı yükleme</span><span class="sxs-lookup"><span data-stu-id="61029-103">Upload a configuration into Lifecycle Services for electronic reporting (ER)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="61029-104">Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcı, yeni bir Elektronik Raporlama (ER) oluşturabilir. ve bunu Microsoft Lifecycle Services (LCS)'ye yükleyebilir.</span><span class="sxs-lookup"><span data-stu-id="61029-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration and upload it into Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="61029-105">Bu örnekte Litware, Inc. örnek şirketi için bir yapılandırma oluşturacak ve bunu LCS'ye yükleyeceksiniz. Bu adımlar, ER yapılandırmaları şirketler arasında paylaşımlı olduğundan herhangi bir şirkette gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="61029-105">In this example, you will create a configuration and upload it to LCS for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="61029-106">Bu adımları tamamlamak için, öncelikle "Bir yapılandırma sağlayıcı oluşturun ve etkin olarak işaretleyin" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="61029-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="61029-107">Bu adımları tamamlamak için LCS erişimi de gereklidir.</span><span class="sxs-lookup"><span data-stu-id="61029-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="61029-108">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="61029-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="61029-109">'Litware, Inc.'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="61029-109">Select ‘Litware, Inc.’</span></span> <span data-ttu-id="61029-110">ve etkin olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="61029-110">and set it as active.</span></span>
3. <span data-ttu-id="61029-111">Yapılandırmalar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="61029-111">Click Configurations.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="61029-112">Yeni bir veri modeli yapılandırması oluşturun</span><span class="sxs-lookup"><span data-stu-id="61029-112">Create a new data model configuration</span></span>
1. <span data-ttu-id="61029-113">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="61029-113">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="61029-114">Elektronik belgeler için bir örnek veri modeli içeren bir yapılandırma oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="61029-114">You will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="61029-115">Bu veri modeli yapılandırması daha sonra LCS'ye yüklenecektir.</span><span class="sxs-lookup"><span data-stu-id="61029-115">This data model configuration will be uploaded into LCS later.</span></span>  
2. <span data-ttu-id="61029-116">İsim alanında 'Örnek model yapılandırması' yazın.</span><span class="sxs-lookup"><span data-stu-id="61029-116">In the Name field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="61029-117">Örnek model yapılandırması</span><span class="sxs-lookup"><span data-stu-id="61029-117">Sample model configuration</span></span>  
3. <span data-ttu-id="61029-118">Açıklama alanına, 'Örnek model yapılandırması' yazın.</span><span class="sxs-lookup"><span data-stu-id="61029-118">In the Description field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="61029-119">Örnek model yapılandırması</span><span class="sxs-lookup"><span data-stu-id="61029-119">Sample model configuration</span></span>  
4. <span data-ttu-id="61029-120">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="61029-120">Click Create configuration.</span></span>
5. <span data-ttu-id="61029-121">Model tasarımcısı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="61029-121">Click Model designer.</span></span>
6. <span data-ttu-id="61029-122">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="61029-122">Click New.</span></span>
7. <span data-ttu-id="61029-123">İsim alanına 'Giriş noktası' yazın.</span><span class="sxs-lookup"><span data-stu-id="61029-123">In the Name field, type 'Entry point'.</span></span>
    * <span data-ttu-id="61029-124">Giriş noktası</span><span class="sxs-lookup"><span data-stu-id="61029-124">Entry point</span></span>  
8. <span data-ttu-id="61029-125">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="61029-125">Click Add.</span></span>
9. <span data-ttu-id="61029-126">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="61029-126">Click Save.</span></span>
10. <span data-ttu-id="61029-127">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="61029-127">Close the page.</span></span>
11. <span data-ttu-id="61029-128">Durumu değiştir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="61029-128">Click Change status.</span></span>
12. <span data-ttu-id="61029-129">Tamamla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="61029-129">Click Complete.</span></span>
13. <span data-ttu-id="61029-130">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="61029-130">Click OK.</span></span>

## <a name="register-a-new--repository"></a><span data-ttu-id="61029-131">Yeni bir havuz kaydedin</span><span class="sxs-lookup"><span data-stu-id="61029-131">Register a new  repository</span></span>
1. <span data-ttu-id="61029-132">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="61029-132">Close the page.</span></span>
2. <span data-ttu-id="61029-133">Depolar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="61029-133">Click Repositories.</span></span>
    * <span data-ttu-id="61029-134">Bu, Litware, Inc. için havuzların listesini açmanızı sağlayacaktır. yapılandırma sağlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="61029-134">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
3. <span data-ttu-id="61029-135">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="61029-135">Click Add to open the drop dialog.</span></span>
    * <span data-ttu-id="61029-136">Bu, yeni bir havuz eklemenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="61029-136">This allows you to add a new repository.</span></span>  
4. <span data-ttu-id="61029-137">Yapılandırma havuz türü alanında LCS'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="61029-137">In the Configuration repository type field, select LCS.</span></span>
5. <span data-ttu-id="61029-138">Havuz oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="61029-138">Click Create repository.</span></span>
6. <span data-ttu-id="61029-139">Proje alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="61029-139">In the Project field, enter or select a value.</span></span>
    * <span data-ttu-id="61029-140">İstenilen LCS projesini seçin.</span><span class="sxs-lookup"><span data-stu-id="61029-140">Select the desired LCS project.</span></span> <span data-ttu-id="61029-141">Projeye erişiminiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="61029-141">You must have access to the project.</span></span>  
7. <span data-ttu-id="61029-142">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="61029-142">Click OK.</span></span>
    * <span data-ttu-id="61029-143">Yeni bir havuz girişini tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="61029-143">Complete a new repository entry.</span></span>  
8. <span data-ttu-id="61029-144">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="61029-144">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="61029-145">LCS havuz kaydını seçin.</span><span class="sxs-lookup"><span data-stu-id="61029-145">Select the LCS repository record.</span></span>  
    * <span data-ttu-id="61029-146">Mevcut sağlayıcı tarafından işaretlenen kayıtlı bir havuzun, yani sadece bu sağlayıcının sahip olduğu yapılandırmaların bu havuzda kullanılabileceğini ve bunun doğrultusunda, seçili LCS projesine karşıya yüklenebileceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="61029-146">Note that a registered repository is marked by the current provider meaning that the only configurations owned by that provider can be placed to this repository and, consequently, uploaded into the selected LCS project.</span></span>  
9. <span data-ttu-id="61029-147">Aç'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="61029-147">Click Open.</span></span>
    * <span data-ttu-id="61029-148">ER yapılandırmalarının listesini görüntülemek için havuzu açın.</span><span class="sxs-lookup"><span data-stu-id="61029-148">Open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="61029-149">Bu proje ER yapılandırmaları paylaşımı için henüz kullanılmamışsa, bu boş olacaktır.</span><span class="sxs-lookup"><span data-stu-id="61029-149">It will be empty if this project has not yet been used for ER configurations sharing.</span></span>  
10. <span data-ttu-id="61029-150">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="61029-150">Close the page.</span></span>
11. <span data-ttu-id="61029-151">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="61029-151">Close the page.</span></span>

## <a name="upload-configuration-into-lcs"></a><span data-ttu-id="61029-152">Yapılandırmayı LCS'ye karşıya yükleyin</span><span class="sxs-lookup"><span data-stu-id="61029-152">Upload configuration into LCS</span></span>
1. <span data-ttu-id="61029-153">Yapılandırmalar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="61029-153">Click Configurations.</span></span>
2. <span data-ttu-id="61029-154">Ağaçta seçin 'Örnek model yapılandırması' seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="61029-154">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="61029-155">Tamamlanmış olan oluşturulan bir yapılandırmayı seçin.</span><span class="sxs-lookup"><span data-stu-id="61029-155">Select a created configuration that has been already completed.</span></span>  
3. <span data-ttu-id="61029-156">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="61029-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="61029-157">'Tamamlandı' durumuna sahip seçili konfigürasyona sahip sürümü seçin.</span><span class="sxs-lookup"><span data-stu-id="61029-157">Select the version of the selected configuration with the status of ‘Completed’.</span></span>  
4. <span data-ttu-id="61029-158">Durumu değiştir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="61029-158">Click Change status.</span></span>
5. <span data-ttu-id="61029-159">Paylaş'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="61029-159">Click Share.</span></span>
    * <span data-ttu-id="61029-160">LCS'de yayımlandığında yapılandırma durumu 'Tamamlandı' seçeneğinden 'Paylaşıldı' seçeneğine değişecektir.</span><span class="sxs-lookup"><span data-stu-id="61029-160">The configuration status will change from ‘Completed’ to ‘Shared’ when it is published in LCS.</span></span>  
6. <span data-ttu-id="61029-161">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="61029-161">Click OK.</span></span>
7. <span data-ttu-id="61029-162">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="61029-162">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="61029-163">'Paylaşıldı' durumuna sahip yapılandırma sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="61029-163">Select the configuration version with the status of 'Shared'.</span></span>  
    * <span data-ttu-id="61029-164">Seçili sürümün durumunun 'Paylaşılan'dan 'Tamamlandı'ya değiştiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="61029-164">Note that the status of the selected version has changed from ‘Completed’ to ‘Shared’.</span></span>  
8. <span data-ttu-id="61029-165">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="61029-165">Close the page.</span></span>
9. <span data-ttu-id="61029-166">Depolar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="61029-166">Click Repositories.</span></span>
    * <span data-ttu-id="61029-167">Bu, Litware, Inc. için havuzların listesini açmanızı sağlayacaktır. yapılandırma sağlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="61029-167">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
10. <span data-ttu-id="61029-168">Aç'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="61029-168">Click Open.</span></span>
    * <span data-ttu-id="61029-169">LCS deposunu seçin ve açın.</span><span class="sxs-lookup"><span data-stu-id="61029-169">Select the LCS repository and open it.</span></span>  
    * <span data-ttu-id="61029-170">Not: Seçili yapılandırma, LCS projesinin seçili bir varlığı olarak gösterilir.</span><span class="sxs-lookup"><span data-stu-id="61029-170">Note that the selected configuration is shown as an asset of the selected LCS project.</span></span>  
    * <span data-ttu-id="61029-171">https://lcs.dynamics.com kullanarak LCS'yi açın. Daha önce havuz kaydı için kullanılan bir proje açın, bu projenin 'Varlık kütüphanesini' açın ve 'Kural Yöneticisi yapılandırma' kıymet türünün içeriğini genişletin – karşıya yüklenen ER yapılandırma kullanılabilir olacaktır.</span><span class="sxs-lookup"><span data-stu-id="61029-171">Open LCS using https://lcs.dynamics.com. Open a project that was used earlier for repository registration, open the ‘Asset library’ of this project, and expand the content of the ‘GER configuration’ asset type – the uploaded ER configuration will be available.</span></span> <span data-ttu-id="61029-172">Not: Bu LCS projesine erişim sağlayıcısının erişimi varsa, karşıya yüklenen LCS yapılandırmasını başka bir Microsoft Dynamics 365 for Finance and Operations örneğine alınabilir.</span><span class="sxs-lookup"><span data-stu-id="61029-172">Note that the uploaded LCS configuration can be imported to another Microsoft Dynamics 365 for Finance and Operations instance if providers have access to this LCS project.</span></span>  


