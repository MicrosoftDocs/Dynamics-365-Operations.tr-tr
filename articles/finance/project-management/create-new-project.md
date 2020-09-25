---
title: Yeni proje oluştur
description: Bu konuda yeni bir proje oluşturma hakkında bilgiler yer alır.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c8c52b8c1c86ea2f6e03cf439ba5930f1006ab4f
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760683"
---
# <a name="create-a-new-project"></a><span data-ttu-id="4ac20-103">Yeni proje oluştur</span><span class="sxs-lookup"><span data-stu-id="4ac20-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4ac20-104">Yeni bir proje oluşturmak için aşağıdaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="4ac20-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="4ac20-105">**Proje yönetimi** sayfasında **Yeni proje**'yi seçin ve aşağıdaki değerleri girin:</span><span class="sxs-lookup"><span data-stu-id="4ac20-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="4ac20-106">**Proje türü:** Zaman ve malzeme</span><span class="sxs-lookup"><span data-stu-id="4ac20-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="4ac20-107">**Proje adı:** XYZ Yükseltme Aşaması 2</span><span class="sxs-lookup"><span data-stu-id="4ac20-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="4ac20-108">**Proje grubu:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="4ac20-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="4ac20-109">**Proje sözleşme kodu:** 00000002</span><span class="sxs-lookup"><span data-stu-id="4ac20-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="4ac20-110">**Proje oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="4ac20-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="4ac20-111">Projeye kaynak atama</span><span class="sxs-lookup"><span data-stu-id="4ac20-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="4ac20-112">**Çalışanlar** sayfasında, **Çalışanlar** listesinde, daha önce yetkinlikleri ayarladığınız çalışanın kaydını seçin ve çalışan kaydını açın.</span><span class="sxs-lookup"><span data-stu-id="4ac20-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="4ac20-113">Eylem Bölmesinde, **Proje** sekmesindeki **Ayar** gurubunda **Projeleri ata**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="4ac20-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="4ac20-114">**Kaynak doğrulama proje atamaları** sayfasında, **Projeler** sekmesinde, **Projeyi seçilen projelere ekle** alanında, **XYZ Yükseltme Aşaması 2** projesinde filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="4ac20-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="4ac20-115">**Kalan projeler** bölmesinde, bir proje seçin ve ardından **Seçilen projeler** bölmesine eklemek için ok düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4ac20-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="4ac20-116">Gerekirse, kaynak için kategoriler de atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4ac20-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="4ac20-117">Kategori türü **Maliyet** veya **Gelir**'dir.</span><span class="sxs-lookup"><span data-stu-id="4ac20-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="4ac20-118">Kategori türü, kuruluşunuz tarafından belirlenir.</span><span class="sxs-lookup"><span data-stu-id="4ac20-118">The category type is determined by your organization.</span></span> <span data-ttu-id="4ac20-119">Kaynak için hiçbir kategori atanmamışsa Finance, maliyet ve gelir için saat fiyatlarında varsayılan kategoriyi arar.</span><span class="sxs-lookup"><span data-stu-id="4ac20-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="4ac20-120">Proje kaynağını ve rol özelliklerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="4ac20-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="4ac20-121">Proje yöneticisi, bir proje için gerekli olan rolleri oluşturmak için proje kaynak oluşturma işlevini kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="4ac20-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="4ac20-122">Roller, teyit edilen kaynaklar kaynaklar rezerve edildiğinde hala bilinmediğinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4ac20-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="4ac20-123">Roller geçici olarak planlanan kaynak olarak kullanılabilir; bu durumda proje planlama aşamalarına devam edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4ac20-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="4ac20-124">[![Rol örneği](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="4ac20-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="4ac20-125">**Senaryo:** Contoso, onaylanmış bir proje tüzüğü olan bir Zaman ve malzeme projesini tamamlamak üzere işe alınmıştır.</span><span class="sxs-lookup"><span data-stu-id="4ac20-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="4ac20-126">Yardımcı proje müdürü, projenin amacını doldurmaya devam etmektedir.</span><span class="sxs-lookup"><span data-stu-id="4ac20-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="4ac20-127">Kaynak yöneticisi, yeni projede çalışmak üzere rezerve edilecek belirli kaynakları belirlemektedir.</span><span class="sxs-lookup"><span data-stu-id="4ac20-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="4ac20-128">Projenin kritik doğası sebebiyle, proje sponsoru, Kıdemli proje yöneticisini rollerden biri olarak talep etmiştir.</span><span class="sxs-lookup"><span data-stu-id="4ac20-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="4ac20-129">Kaynak yöneticisinin yeni bir kaynak alması ve yardımcı proje yöneticisi için proje planlama sırasında kaynak bilgisi gerekli olduğundan, rolü sistemde tanımlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="4ac20-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="4ac20-130">Aşağıdaki adımlarda, kaynak yöneticisinin Kıdemli proje yöneticisi rolünü nasıl ayarlayabileceği ve kaynak özelliklerini bununla nasıl ilişkilendirebileceği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="4ac20-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="4ac20-131">Daha sonra, rol istenen kaynak yetkinlikleriyle eşleşen kullanılabilir kaynakları aramak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4ac20-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="4ac20-132">**Kurulum rolleri** sayfasında **Yeni**'yi seçin ve aşağıdaki değerleri girin:</span><span class="sxs-lookup"><span data-stu-id="4ac20-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="4ac20-133">**Rol Kimliği:** Kıdemli Proje Yöneticisi</span><span class="sxs-lookup"><span data-stu-id="4ac20-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="4ac20-134">**Açıklama:** Kıdemli Proje Yöneticisi</span><span class="sxs-lookup"><span data-stu-id="4ac20-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="4ac20-135">**Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="4ac20-135">Select **Create**.</span></span>
3. <span data-ttu-id="4ac20-136">**Kıdemli Proje Yöneticisi** rolünü seçip **Özellikleri yapılandır**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4ac20-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="4ac20-137">**Özelliklerin türü** alanında, **Beceri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4ac20-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="4ac20-138">**Kullanılabilir özellikler** alanına, aradığınız yeteneği girin.</span><span class="sxs-lookup"><span data-stu-id="4ac20-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="4ac20-139">**Özellik türü** alanında **Sertifika**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="4ac20-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="4ac20-140">**Kullanılabilir özellikler** alanına, aradığınız sertifika türünü girin.</span><span class="sxs-lookup"><span data-stu-id="4ac20-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="4ac20-141">Projeye proje kaynağı atama</span><span class="sxs-lookup"><span data-stu-id="4ac20-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="4ac20-142">**Tüm projeler** sayfasında, **XYZ Yükseltme Aşaması 2** projesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4ac20-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="4ac20-143">**Proje ekibi ve planlama** sekmesinde **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4ac20-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="4ac20-144">**Rol** alanında **Ekip üyesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="4ac20-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="4ac20-145">**Takvimden rezerve et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4ac20-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="4ac20-146">**Kaynak kullanılabilirliği** sayfasında, **Görünüm ayarları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="4ac20-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="4ac20-147">**Görünüm ayarlarını ayarla** sayfasına şu değerleri girin:</span><span class="sxs-lookup"><span data-stu-id="4ac20-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="4ac20-148">**Tarih aralığı görünüm biçimi:** Gün</span><span class="sxs-lookup"><span data-stu-id="4ac20-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="4ac20-149">**Uygunluk açıklamalarını görüntüle:** Evet</span><span class="sxs-lookup"><span data-stu-id="4ac20-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="4ac20-150">**Kalan kapasiteyi görüntüle:** Evet</span><span class="sxs-lookup"><span data-stu-id="4ac20-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="4ac20-151">Kaynak listesinde, bir kaynak seçin.</span><span class="sxs-lookup"><span data-stu-id="4ac20-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="4ac20-152">**Sabit defter** ve **Tam kapasite**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4ac20-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="4ac20-153">Varsayılan bir role kaynak atama</span><span class="sxs-lookup"><span data-stu-id="4ac20-153">Assign a resource to a default role</span></span>

<span data-ttu-id="4ac20-154">Proje veya kaynak yöneticilerine yardımcı olmak için, bir proje için rezerve edilebilecek kaynaklarla ilgili daha ayrıntılı inceleme yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4ac20-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="4ac20-155">Varsayılan bir rolü mevcut bir kaynakla veya yeni edinilen bir kaynakla ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4ac20-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="4ac20-156">örneğin, Daniel işe alındığında, İş analisti rolünü yerine getirmek için beceri ve deneyimi vardı.</span><span class="sxs-lookup"><span data-stu-id="4ac20-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="4ac20-157">Kaynak yöneticisi, bu rolü Daniel'ın varsayılan rolü olarak atadı.</span><span class="sxs-lookup"><span data-stu-id="4ac20-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="4ac20-158">Bu nedenle, kaynak yöneticisi Daniel'ı projelerde çalışmak üzere kullanılabilir olan iş analistleri havuzuna eklendi.</span><span class="sxs-lookup"><span data-stu-id="4ac20-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="4ac20-159">Kaynak rezervasyonu sırasında, proje yöneticileri projede çalışabilecek rol kaynaklarını filtreleyebilir.</span><span class="sxs-lookup"><span data-stu-id="4ac20-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="4ac20-160">Bu bilgiyi, kaynak karşılama sırasında çok ölçütlü karar analizi gerçekleştirirken bir ölçüt olarak kullanabilirler.</span><span class="sxs-lookup"><span data-stu-id="4ac20-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="4ac20-161">Ayrıca, söz konusu proje için belirli becerileri, eğitimi ve deneyimi olan kaynakları aramak için filtre uygulamak amacıyla diğer kaynak özelliklerini ekleyebilirler.</span><span class="sxs-lookup"><span data-stu-id="4ac20-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="4ac20-162">**Senaryo:** Onaylanmış bir proje başlamıştır ve Kıdemli proje yöneticisi rolü proje planlama aşamasında planlanan kaynak olarak rezerve edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="4ac20-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="4ac20-163">Kaynak yöneticisi, Kıdemli proje yöneticisi rolünü yerine getirecek bir kaynak edinmiştir.</span><span class="sxs-lookup"><span data-stu-id="4ac20-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="4ac20-164">**Kaynaklar listesi** sayfasında, **Daniel Goldschmidt**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4ac20-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="4ac20-165">**Kaynak rolleri** sayfasında **Yeni**'yi seçin ve aşağıdaki değerleri girin:</span><span class="sxs-lookup"><span data-stu-id="4ac20-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="4ac20-166">**Yürürlük başlangıcı:** Geçerli tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="4ac20-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="4ac20-167">**Bitiş:** **Asla** girin.</span><span class="sxs-lookup"><span data-stu-id="4ac20-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="4ac20-168">**Rol:** **Kıdemli Proje Yöneticisi** girin.</span><span class="sxs-lookup"><span data-stu-id="4ac20-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="4ac20-169">**Kaydet**'i seçip sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4ac20-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="4ac20-170">**Yetkinlikler** sekmesinde, **ProjectMgmt** becerisini ve **PMP** sertifikasını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="4ac20-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>
