---
title: Kıymet yönetimi mobil çalışma alanını kullanma
description: Bu konu Varlık yönetimi mobil çalışma alanı hakkında bilgiler sağlar.
author: josaw1
manager: tfehr
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.dyn365.ops.version: 10.0.5
ms.search.validFrom: 2019-08-31
ms.openlocfilehash: afda807714f14efb1cbab4ecfdd273aac52f4558
ms.sourcegitcommit: 995c678b4715be267f1f97148902a6b3dde3bcab
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/20/2021
ms.locfileid: "5033164"
---
# <a name="use-the-asset-management-mobile-workspace"></a><span data-ttu-id="c73e8-103">Kıymet yönetimi mobil çalışma alanını kullanma</span><span class="sxs-lookup"><span data-stu-id="c73e8-103">Use the Asset management mobile workspace</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c73e8-104">Bu konu **Kıymet yönetimi** mobil çalışma alanı hakkında bilgiler sağlar.</span><span class="sxs-lookup"><span data-stu-id="c73e8-104">This topic provides information about the **Asset management** mobile workspace.</span></span> <span data-ttu-id="c73e8-105">Bu çalışma alanı, kullanıcıların bakım taleplerini ve iş emirlerini görüntüleyip oluşturmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="c73e8-105">This workspace lets users view and create maintenance requests and work orders.</span></span> <span data-ttu-id="c73e8-106">Ayrıca kullanıcılar, atanan iş emri işlerini takvim veya liste görünümünde görüntüleyebilirler.</span><span class="sxs-lookup"><span data-stu-id="c73e8-106">Users can also view the assigned work order jobs in a calendar or list view.</span></span> <span data-ttu-id="c73e8-107">Varlıklar ve işlem yapılacak yerleşimler de görüntülenip aranabilir.</span><span class="sxs-lookup"><span data-stu-id="c73e8-107">Assets and functional locations can also be viewed and searched for.</span></span>

## <a name="overview"></a><span data-ttu-id="c73e8-108">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="c73e8-108">Overview</span></span>

<span data-ttu-id="c73e8-109">Varlık Yönetimi, Dynamics 365 Supply Chain Management'da varlıkların ve iş emri işlerinin yönetilmesine yönelik gelişmiş bir modüldür.</span><span class="sxs-lookup"><span data-stu-id="c73e8-109">Asset Management is an advanced module for managing assets and work order jobs in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="c73e8-110">**Varlık yönetimi** mobil çalışma alanı, kullanıcıların istedikleri mobil cihazda atanan iş siparişi işlerini hızlı şekilde görüntülemesine olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="c73e8-110">The **Asset management** mobile workspace lets users quickly view assigned work order jobs on the mobile device of their choice.</span></span> <span data-ttu-id="c73e8-111">Kullanıcılar ayrıca bakım talepleri oluşturabilir ve yönetebilir, yaşam döngüsü durumunu güncelleştirebilir ve varlık ve işlem yapılacak yerleşim ayrıntılarını mobil cihazlarını kullanarak görüntüleyebilir.</span><span class="sxs-lookup"><span data-stu-id="c73e8-111">Users can also create and manage maintenance requests, update lifecycle state, and view asset and functional location details by using their mobile device.</span></span>

<span data-ttu-id="c73e8-112">Özellikle, **Varlık yönetimi** mobil çalışma alanı, kullanıcıların şu görevleri yerine getirmesini sağlar:</span><span class="sxs-lookup"><span data-stu-id="c73e8-112">Specifically, the **Asset management** mobile workspace lets users perform these tasks:</span></span>

- <span data-ttu-id="c73e8-113">Bakım talepleri oluşturmak, görüntülemek ve düzenlemek, bir fotoğraf çekmek veya mevcut bir görüntüyü bakım talebine eklemek ve bakım talebi yaşam döngüsü durumunu değiştirmek.</span><span class="sxs-lookup"><span data-stu-id="c73e8-113">Create, view, and edit maintenance requests, take a photo or attach an existing image to the maintenance request, change the maintenance request lifecycle state.</span></span> 
- <span data-ttu-id="c73e8-114">İş emirleri oluşturmak, görüntülemek ve düzenlemek, bir fotoğraf çekmek veya mevcut bir görüntüyü iş emrine eklemek, iş emri yaşam döngüsü durumunu değiştirmek ve iş emri işlerini görüntülemek.</span><span class="sxs-lookup"><span data-stu-id="c73e8-114">Create, view, and edit work orders, take a photo or attach an existing image to the work order, change the work order lifecycle state, view work order jobs.</span></span>
- <span data-ttu-id="c73e8-115">Atanan iş emri işlerini Takvim görünümünde görüntülemek.</span><span class="sxs-lookup"><span data-stu-id="c73e8-115">View assigned work order jobs in a calendar view.</span></span>
- <span data-ttu-id="c73e8-116">İş emri işi oluşturmak, görüntülemek ve düzenlemek, varlık sayaçlarını güncelleştirmek, bakım denetim listesini görüntülemek, iş emri iş notlarını görüntülemek ve düzenlemek, iş emri işi için gerekli araçları görüntülemek.</span><span class="sxs-lookup"><span data-stu-id="c73e8-116">Create, view, and edit work order job, update asset counters, view maintenance checklist, view and edit work order job notes, view the tools required for the work order job.</span></span>
- <span data-ttu-id="c73e8-117">Belirli bir varlık veya işlem yapılacak yerleşimi görüntülemek veya aramak.</span><span class="sxs-lookup"><span data-stu-id="c73e8-117">View or search for a specific asset or functional location.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c73e8-118">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="c73e8-118">Prerequisites</span></span>

<span data-ttu-id="c73e8-119">**Kıymet yönetimi** mobil çalışma alanını kullanabilmeniz için, yöneticinizin gerekli kullanıcı ve çalışan hesaplarını ayarlamış ve çalışma alanını yayımlamış olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="c73e8-119">Before you can use the **Asset management** mobile workspace, your admin must set up the required user and worker accounts, and publish the workspace.</span></span> <span data-ttu-id="c73e8-120">Daha fazla bilgi için bkz. [Kıymet yönetimi mobil çalışma alanını ayarlama](set-up-asset-management-mobile.md).</span><span class="sxs-lookup"><span data-stu-id="c73e8-120">For more information, see [Set up the Asset management mobile workspace](set-up-asset-management-mobile.md).</span></span>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="c73e8-121">Mobil uygulamayı indirin ve yükleyin</span><span class="sxs-lookup"><span data-stu-id="c73e8-121">Download and install the mobile app</span></span>

<span data-ttu-id="c73e8-122">Dynamics 365 for Unified Operations mobil uygulamasını yükleyin ve kurun:</span><span class="sxs-lookup"><span data-stu-id="c73e8-122">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

- [<span data-ttu-id="c73e8-123">Android telefonlar için</span><span class="sxs-lookup"><span data-stu-id="c73e8-123">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
- [<span data-ttu-id="c73e8-124">İPhone'lar için</span><span class="sxs-lookup"><span data-stu-id="c73e8-124">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="c73e8-125">Mobil uygulamaya oturum açın</span><span class="sxs-lookup"><span data-stu-id="c73e8-125">Sign in to the mobile app</span></span>

1. <span data-ttu-id="c73e8-126">Mobil cihazınızda uygulamayı başlatın.</span><span class="sxs-lookup"><span data-stu-id="c73e8-126">Start the app on your mobile device.</span></span>

1. <span data-ttu-id="c73e8-127">Dynamics 365 URL'nizi girin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-127">Enter your Dynamics 365 URL.</span></span>

1. <span data-ttu-id="c73e8-128">İlk kez oturum açtığınızda, kullanıcı adınız ve parolanız istenir.</span><span class="sxs-lookup"><span data-stu-id="c73e8-128">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="c73e8-129">Kimlik bilgilerinizi girin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-129">Enter your credentials.</span></span>

1. <span data-ttu-id="c73e8-130">Oturum açtıktan sonra şirketiniz için kullanılabilir çalışma alanları gösterilir.</span><span class="sxs-lookup"><span data-stu-id="c73e8-130">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="c73e8-131">Sistem yöneticiniz yeni bir çalışma alanını daha sonra yayınlarsa, mobil çalışma alanlarının listesini yenilemeniz gerekeceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="c73e8-131">Note that if your system administrator publishes a new workspace later, you'll have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="c73e8-132">![Çalışma alanını seçme](media/am-mobile-01.png "Çalışma alanını seçme")</span><span class="sxs-lookup"><span data-stu-id="c73e8-132">![Select a workspace](media/am-mobile-01.png "Select a workspace")</span></span>

## <a name="view-assigned-work-order-jobs-in-calendar-view"></a><span data-ttu-id="c73e8-133">Atanan iş emri işlerini Takvim görünümünde görüntüleme</span><span class="sxs-lookup"><span data-stu-id="c73e8-133">View assigned work order jobs in calendar view</span></span>

1. <span data-ttu-id="c73e8-134">Mobil cihazınızda **Varlık yönetimi** çalışma alanını açın.</span><span class="sxs-lookup"><span data-stu-id="c73e8-134">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="c73e8-135">**İş emri işleri takvimim**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-135">Select **My work order jobs calendar**.</span></span>

1. <span data-ttu-id="c73e8-136">İş emri işlerini görüntülemek istediğiniz tarihi seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-136">Select the date you want to view work order jobs for.</span></span> <span data-ttu-id="c73e8-137">Listede, her iş emri işi için varlık kodunu ve işlem yapılacak yerleşim kodunu görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="c73e8-137">In the list, you'll see the asset ID and functional location ID for each work order job.</span></span>

1. <span data-ttu-id="c73e8-138">İş ayrıntılarını görmek için listeden bir iş emri işi seçin: Varlık ve işlem yapılacak yerleşim ayrıntıları ile **Ekler**, **Denetim listeleri**, **Araçlar**, **Varlık sayaçları**, **Notlar**, **Günlükler**'i görüntülemek için diğer gezinti bağlantıları.</span><span class="sxs-lookup"><span data-stu-id="c73e8-138">Select a work order job in the list to see job details: Asset and functional location details as well as other navigation links to view **Attachments**, **Checklists**, **Tools**, **Asset counters**, **Notes**, **Journals**.</span></span>

    <span data-ttu-id="c73e8-139">![Atanan iş emri işlerini Takvim görünümünde görüntüleme](media/am-mobile-02.png "Atanan iş emri işlerini Takvim görünümünde görüntüleme")</span><span class="sxs-lookup"><span data-stu-id="c73e8-139">![View assigned work order jobs in calendar view](media/am-mobile-02.png "View assigned work order jobs in calendar view")</span></span>

## <a name="create-a-work-order-job"></a><span data-ttu-id="c73e8-140">İş emri işi oluşturma</span><span class="sxs-lookup"><span data-stu-id="c73e8-140">Create a work order job</span></span>

1. <span data-ttu-id="c73e8-141">Mobil cihazınızda **Varlık yönetimi** çalışma alanını açın.</span><span class="sxs-lookup"><span data-stu-id="c73e8-141">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="c73e8-142">**Tüm bakım iş emirleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-142">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="c73e8-143">Yeni bir iş emri işi oluşturmak istediğiniz iş emrini seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-143">Select the work order you want to create a new work order job for.</span></span>

1. <span data-ttu-id="c73e8-144">**Satır ekle** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-144">Select the **Add line** button.</span></span>

1. <span data-ttu-id="c73e8-145">Yeni bir iş emri işi oluşturmak istediğiniz **Varlığı** seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-145">Select the **Asset** you want to create a work order job for.</span></span>

1. <span data-ttu-id="c73e8-146">**Bakım İşi türü**, **Bakım işi türü çeşidi** ve **Zanaat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-146">Select **Maintenance job type**, **Maintenance job type variant** and **Trade**.</span></span>

1. <span data-ttu-id="c73e8-147">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-147">Select **Done**.</span></span>

    <span data-ttu-id="c73e8-148">![Satır ekle ekranı](media/am-mobile-03.png "Satır ekle ekranı")</span><span class="sxs-lookup"><span data-stu-id="c73e8-148">![The Add line screen](media/am-mobile-03.png "The Add line screen")</span></span>


## <a name="add-attachment-to-a-work-order-job"></a><span data-ttu-id="c73e8-149">İş emri işine ek ekleme</span><span class="sxs-lookup"><span data-stu-id="c73e8-149">Add attachment to a work order job</span></span>

1. <span data-ttu-id="c73e8-150">Mobil cihazınızda **Varlık yönetimi** çalışma alanını açın.</span><span class="sxs-lookup"><span data-stu-id="c73e8-150">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="c73e8-151">**Tüm bakım iş emirleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-151">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="c73e8-152">Ek eklemek istediğiniz iş emrini > iş emri işini seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-152">Select the work order > work order job you want to add an attachment to.</span></span>
    - <span data-ttu-id="c73e8-153">Alternatif olarak, **İş emri işi ayrıntıları** sayfasına gitmek için ana sayfada **İş emri işleri listem** veya **İş emri işleri takvimim**'i seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c73e8-153">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **Work order job details** page.</span></span>

1. <span data-ttu-id="c73e8-154">**İş emri işi ayrıntıları** sayfasında **Ekler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-154">Select **Attachments** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="c73e8-155">İş emri işindeki mevcut ekleri göreceksiniz.</span><span class="sxs-lookup"><span data-stu-id="c73e8-155">You'll see existing attachments on the work order job.</span></span> <span data-ttu-id="c73e8-156">**Ek ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-156">Select **Add attachment**.</span></span>

1. <span data-ttu-id="c73e8-157">Ek için **Ad** ve **Notlar** girin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-157">Enter **Name** and **Notes** for the attachment.</span></span>

1. <span data-ttu-id="c73e8-158">Mobil galeriden fotoğraf seçmek için **Görüntü seç**'i veya fotoğraf çekmek için **Fotoğraf çek**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-158">Select **Choose image** to select a photo from the mobile gallery, or **Take photo** to take a photo.</span></span>

1. <span data-ttu-id="c73e8-159">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-159">Select **Done**.</span></span>

    <span data-ttu-id="c73e8-160">![İş emri işi için ekleri görüntüleme ve ekleme](media/am-mobile-04.png "İş emri işi için ekleri görüntüleme ve ekleme")</span><span class="sxs-lookup"><span data-stu-id="c73e8-160">![View and add attachments for a work order job](media/am-mobile-04.png "View and add attachments for a work order job")</span></span>

## <a name="view-maintenance-checklist-on-a-work-order-job"></a><span data-ttu-id="c73e8-161">İş emri işindeki bakım denetim listesini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="c73e8-161">View maintenance checklist on a work order job</span></span>

1. <span data-ttu-id="c73e8-162">Mobil cihazınızda **Varlık yönetimi** çalışma alanını açın.</span><span class="sxs-lookup"><span data-stu-id="c73e8-162">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="c73e8-163">**Tüm bakım iş emirleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-163">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="c73e8-164">Denetim listelerini görüntülemek istediğiniz iş emrini > iş emri işini seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-164">Select the work order > work order job you want to view checklists for.</span></span>
    - <span data-ttu-id="c73e8-165">Alternatif olarak, **İş emri işi ayrıntıları** sayfasına gitmek için ana sayfada **İş emri işleri listem** veya **İş emri işleri takvimim**'i seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c73e8-165">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **work order job details** page.</span></span>

1. <span data-ttu-id="c73e8-166">**İş emri işi ayrıntıları** sayfasında **Denetim listeleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-166">Select **Checklists** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="c73e8-167">İş emri işiyle ilgili denetim listesi satırlarının listesini göreceksiniz.</span><span class="sxs-lookup"><span data-stu-id="c73e8-167">You'll see a list of checklist lines related to the work order job.</span></span> <span data-ttu-id="c73e8-168">**Yönergeleri** görüntülemek ve **Ekler** eklemek için denetim listesi satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-168">Select a checklist line to view **Instructions** and add **Notes**.</span></span>

1. <span data-ttu-id="c73e8-169">Önceki sayfaya dönmek için geri düğmesini (**<**) seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-169">Select the back button (**<**) to return to the previous page.</span></span>

    <span data-ttu-id="c73e8-170">![Bakım denetim listesi ve satır ayrıntıları](media/am-mobile-05.png "Bakım denetim listesi ve satır ayrıntıları")</span><span class="sxs-lookup"><span data-stu-id="c73e8-170">![Maintenance checklist and line details](media/am-mobile-05.png "Maintenance checklist and line details")</span></span>

## <a name="view-and-update-asset-counters-on-a-work-order-job"></a><span data-ttu-id="c73e8-171">Bir iş emri işinde varlık sayaçlarını görüntüleme ve güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c73e8-171">View and update asset counters on a work order job</span></span>

1. <span data-ttu-id="c73e8-172">Mobil cihazınızda **Varlık yönetimi** çalışma alanını açın.</span><span class="sxs-lookup"><span data-stu-id="c73e8-172">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="c73e8-173">**Tüm bakım iş emirleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-173">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="c73e8-174">Varlık sayaçlarını görüntülemek istediğiniz iş emrini > iş emri işini seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-174">Select the work order > work order job you want to view asset counters for.</span></span>
    - <span data-ttu-id="c73e8-175">Alternatif olarak, **İş emri işi ayrıntıları** sayfasına gitmek için ana sayfada **İş emri işleri listem** veya **İş emri işleri takvimim**'i seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c73e8-175">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **work order job details** page.</span></span>

1. <span data-ttu-id="c73e8-176">**İş emri işi ayrıntıları** sayfasında **Varlık sayaçları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-176">Select **Asset counters** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="c73e8-177">İş emri işiyle ilgili varlık sayaçlarının listesini göreceksiniz.</span><span class="sxs-lookup"><span data-stu-id="c73e8-177">You see a list of asset counters related to the work order job.</span></span> <span data-ttu-id="c73e8-178">Sayaç değerini güncelleştirmek için bir varlık sayacı satırındaki kalem simgesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-178">Select the pencil icon on an asset counter line to update the counter value.</span></span>

1. <span data-ttu-id="c73e8-179">Yeni bir sayaç değeri girin ve **Bitti**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-179">Enter a new counter value, and select **Done**.</span></span>

    <span data-ttu-id="c73e8-180">![Kıymet sayaçlarını görüntüleme ve güncelleştirme](media/am-mobile-06.png "Kıymet sayaçlarını görüntüleme ve güncelleştirme")</span><span class="sxs-lookup"><span data-stu-id="c73e8-180">![View and update asset counters](media/am-mobile-06.png "View and update asset counters")</span></span>

## <a name="register-consumption-on-a-work-order-job"></a><span data-ttu-id="c73e8-181">İş emri işinde tüketimi kaydetme</span><span class="sxs-lookup"><span data-stu-id="c73e8-181">Register consumption on a work order job</span></span>

1. <span data-ttu-id="c73e8-182">Mobil cihazınızda **Varlık yönetimi** çalışma alanını açın.</span><span class="sxs-lookup"><span data-stu-id="c73e8-182">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="c73e8-183">**Tüm bakım iş emirleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-183">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="c73e8-184">Tüketim kayıtları eklemek istediğiniz istediğiniz iş emrini > iş emri işini seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-184">Select the work order > work order job you want to add consumption registrations for.</span></span>
    - <span data-ttu-id="c73e8-185">Alternatif olarak, **İş emri işi ayrıntıları** sayfasına gitmek için ana sayfada **İş emri işleri listem** veya **İş emri işleri takvimim**'i seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c73e8-185">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **work order job details** page.</span></span>

1. <span data-ttu-id="c73e8-186">**İş emri işi ayrıntıları** sayfasında **Günlükler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-186">Select **Journals** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="c73e8-187">Çalışma saati kayıtları oluşturmak için **Saat ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-187">Select **Add hours** to create work hour registrations.</span></span>
    1. <span data-ttu-id="c73e8-188">Aramadan **Kategori**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-188">Select the **Category** from the lookup.</span></span>
    1. <span data-ttu-id="c73e8-189">**Saat** alanında, iş emri işinde harcanan çalışma saatlerinin sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-189">In the **Hours** field, enter the number of work hours spent on the work order job.</span></span>
    1. <span data-ttu-id="c73e8-190">Uygun **Satır özelliği** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-190">Select the appropriate **Line property**.</span></span>
    1. <span data-ttu-id="c73e8-191">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-191">Select **Done**.</span></span>

1. <span data-ttu-id="c73e8-192">Madde kayıtları oluşturmak için **Madde ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-192">Select **Add items** to create item registrations.</span></span>
    1. <span data-ttu-id="c73e8-193">Aramadan **Madde numarası**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-193">Select the **Item number** from the lookup.</span></span>
    1. <span data-ttu-id="c73e8-194">Aramadan **Tesis**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-194">Select the **Site** from the lookup.</span></span>
    1. <span data-ttu-id="c73e8-195">Tüketilen madde **Miktarını** girin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-195">Enter the **Quantity** of items consumed.</span></span>
    1. <span data-ttu-id="c73e8-196">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-196">Select **Done**.</span></span>

1. <span data-ttu-id="c73e8-197">Gider kayıtları oluşturmak için **Gider ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-197">Select **Add expense** to create expense registrations.</span></span>
    1. <span data-ttu-id="c73e8-198">Aramadan **Kategori**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-198">Select the **Category** from the lookup.</span></span>
    1. <span data-ttu-id="c73e8-199">Gider kaydı için miktarı girin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-199">Enter the quantity for the expense registration.</span></span>
    1. <span data-ttu-id="c73e8-200">Aramadan **Satış para birimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-200">Select the **Sales currency** from the lookup.</span></span>
    1. <span data-ttu-id="c73e8-201">Gider kaydı için **Maiyet fiyatı**'nı girin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-201">Enter the **Cost price** for the expense registration.</span></span>
    1. <span data-ttu-id="c73e8-202">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-202">Select **Done**.</span></span>

    <span data-ttu-id="c73e8-203">![İş emri günlüğünü güncelleştirme](media/am-mobile-07.png "İş emri günlüğünü güncelleştirme")</span><span class="sxs-lookup"><span data-stu-id="c73e8-203">![Update a work order journal](media/am-mobile-07.png "Update a work order journal")</span></span>

## <a name="update-lifecycle-state-on-a-work-order"></a><span data-ttu-id="c73e8-204">İş emrindeki yaşam döngüsü durumunu güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c73e8-204">Update lifecycle state on a work order</span></span>

1. <span data-ttu-id="c73e8-205">Mobil cihazınızda **Varlık yönetimi** çalışma alanını açın.</span><span class="sxs-lookup"><span data-stu-id="c73e8-205">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="c73e8-206">**Tüm bakım iş emirleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-206">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="c73e8-207">Yaşam döngüsü durumunu güncelleştirmek istediğiniz iş emrini seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-207">Select the work order you want to update lifecycle state for.</span></span>

1. <span data-ttu-id="c73e8-208">Ekranın alt kısmındaki **Durumu güncelleştir** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-208">Select the **Update state** button at the bottom of the screen.</span></span>

1. <span data-ttu-id="c73e8-209">Listeden yeni bir yaşam döngüsü durumu seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-209">Select a new lifecycle state from the list.</span></span>

1. <span data-ttu-id="c73e8-210">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-210">Select **Done**.</span></span>

    <span data-ttu-id="c73e8-211">![İş emrindeki yaşam döngüsü durumunu güncelleştirme](media/am-mobile-08.png "İş emrindeki yaşam döngüsü durumunu güncelleştirme")</span><span class="sxs-lookup"><span data-stu-id="c73e8-211">![Update lifecycle state on a work order](media/am-mobile-08.png "Update lifecycle state on a work order")</span></span>

## <a name="create-a-maintenance-request"></a><span data-ttu-id="c73e8-212">Bakım talebi oluşturma</span><span class="sxs-lookup"><span data-stu-id="c73e8-212">Create a maintenance request</span></span>

1. <span data-ttu-id="c73e8-213">Mobil cihazınızda **Varlık yönetimi** çalışma alanını açın.</span><span class="sxs-lookup"><span data-stu-id="c73e8-213">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="c73e8-214">**Tüm bakım talepleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-214">Select **All maintenance requests**.</span></span>

1. <span data-ttu-id="c73e8-215">Ekranın altınaki **Eylemler** öğesini ve **Bakım talebi oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-215">Select **Actions** at the bottom of the screen, and select **Create maintenance request**.</span></span>

1. <span data-ttu-id="c73e8-216">**Varlık yönetimi**'nde bakım talepleri için numara serisi etkinleştirilmişse, **Bakım talebi** alanı gizlenir çünkü bu alan otomatik olarak doldurulur. **Bakım talebi** alanı görünüyorsa bir bakım talebi kimliği girin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-216">If number sequence is enabled for maintenance requests in **Asset management**, the **Maintenance request** field is hidden because it is automatically filled out. If the **Maintenance request** field is visible, enter a maintenance request ID.</span></span>

1. <span data-ttu-id="c73e8-217">Bir **Bakım talebi türü** seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-217">Select a **Maintenance request type**.</span></span>

1. <span data-ttu-id="c73e8-218">Bakım talebi için bir **Açıklama** girin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-218">Enter a **Description** for the maintenance request.</span></span>

1. <span data-ttu-id="c73e8-219">Talep oluşturmak istediğiniz **Varlığı** seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-219">Select the **Asset** you want to create the request for.</span></span>

1. <span data-ttu-id="c73e8-220">Bakım talebi için **Hizmet düzeyi** seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-220">Select the **Service level** for the maintenance request.</span></span>

1. <span data-ttu-id="c73e8-221">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-221">Select **Done**.</span></span>

    <span data-ttu-id="c73e8-222">![Bakım talebi oluşturma](media/am-mobile-09.png "Bakım talebi oluşturma")</span><span class="sxs-lookup"><span data-stu-id="c73e8-222">![Create a maintenance request](media/am-mobile-09.png "Create a maintenance request")</span></span>

## <a name="add-attachment-to-a-maintenance-request"></a><span data-ttu-id="c73e8-223">Bakım talebine ek ekleme</span><span class="sxs-lookup"><span data-stu-id="c73e8-223">Add attachment to a maintenance request</span></span>

1. <span data-ttu-id="c73e8-224">Mobil cihazınızda **Varlık yönetimi** çalışma alanını açın.</span><span class="sxs-lookup"><span data-stu-id="c73e8-224">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="c73e8-225">**Tüm bakım talepleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-225">Select **All maintenance requests**.</span></span>

1. <span data-ttu-id="c73e8-226">Ek eklemek istediğiniz bakım talebini seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-226">Select the maintenance request you want to add an attachment to.</span></span>

1. <span data-ttu-id="c73e8-227">Ekranın alt kısmındaki **Ekler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-227">Select **Attachments** at the bottom of the screen.</span></span>

1. <span data-ttu-id="c73e8-228">**Ekler ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-228">Select **Add attachments**.</span></span>

1. <span data-ttu-id="c73e8-229">Ek için **Ad** ve **Notlar** girin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-229">Enter **Name** and **Notes** for the attachment.</span></span>

1. <span data-ttu-id="c73e8-230">Mobil galeriden fotoğraf seçmek için **Resim seç**'i veya fotoğraf çekmek için **Fotoğraf çek**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-230">Select **Choose image** to select a photo from the mobile gallery or **Take photo** to take a photo.</span></span>

1. <span data-ttu-id="c73e8-231">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c73e8-231">Select **Done**.</span></span>

    <span data-ttu-id="c73e8-232">![Bakım talebine ek ekleme](media/am-mobile-10.png "Bakım talebine ek ekleme")</span><span class="sxs-lookup"><span data-stu-id="c73e8-232">![Add an attachment to a maintenance request](media/am-mobile-10.png "Add an attachment to a maintenance request")</span></span>
