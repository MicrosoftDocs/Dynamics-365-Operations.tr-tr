---
title: "Microsoft Project istemci tümleştirmesi"
description: "Bir proje planı hazırlamak ve sürdürmek karmaşık olabilir bu nedenle proje yöneticilerinin kendilerine görevi yönetmede yardımcı olacak araçlar kullanması gerekir. Microsoft Project İstemcisi ile tümleştirme, bir proje iş kırılım yapısını açmayı ve yönetmeyi destekler."
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d412c60f22347a38e38ca5f2c5515bd132814f25
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---

# <a name="microsoft-project-client-integration"></a><span data-ttu-id="175da-104">Microsoft Project istemci tümleştirmesi</span><span class="sxs-lookup"><span data-stu-id="175da-104">Microsoft Project client integration</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="175da-105">Bir proje planı hazırlamak ve sürdürmek karmaşık olabilir bu nedenle proje yöneticilerinin kendilerine görevi yönetmede yardımcı olacak araçlar kullanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="175da-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="175da-106">Microsoft Project İstemcisi ile tümleştirme, bir proje iş kırılım yapısını açmayı ve yönetmeyi destekler.</span><span class="sxs-lookup"><span data-stu-id="175da-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="175da-107">Proje yöneticisi, yaptığı değişiklikleri Finance and Operations proje iş kırılım yapısına geri yayımlayabilir.</span><span class="sxs-lookup"><span data-stu-id="175da-107">The project manager can publish any changes back to the Finance and Operations project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="175da-108">Microsoft Dynamics 365 for Finance and Operations Temmuz güncelleştirmesini kullanıyorsanız KB 4054797 ve 4055884'ü yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="175da-108">If you are using Microsoft Dynamics 365 for Finance and Operations, July update, you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="175da-109">Microsoft Project İstemcisi eklentisini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="175da-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="175da-110">Microsoft Project İstemcisiyle tümleştirmeyi etkinleştirmek için, kullanıcının istemcisindeki Microsoft Project uygulamasına bir Microsoft Dynamics 365 eklentisi yüklenmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="175da-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="175da-111">Bu işlem **Proje yönetimi çalışma alanı** açılarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="175da-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="175da-112">•   Çalışma alanının **Bağlantılar** > **Kurulum** bölümünden **Proje istemcisi eklentisini yapılandır**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="175da-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="175da-113">•   **Aç**'a ve ardından istendiğinde **Çalıştır**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="175da-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="175da-114">Microsoft Project İstemcisinde mevcut bir taslak iş kırılım yapısını açın ve düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="175da-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="175da-115">Finance and Operations'taki bir projede zaten oluşturulmuş bir işi kırılım yapısı varsa, iş kırılım yapısının taslak durumunda olması durumunda iş kırılım yapısı Microsoft Project İstemcisi uygulamasında açılabilir.</span><span class="sxs-lookup"><span data-stu-id="175da-115">If a project in Finance and Operations already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="175da-116">**Proje** sayfasından açmak için, **Plan** sekmesindeki **Microsoft Project'te aç** bağlantısına tıklayın. Bu sayfa, Microsoft Project İstemcisi uygulaması içinden **Microsoft Dynamics 365** sekmesindeki **Aç** öğesine tıklayarak da açılabilir. **Tüzel kişiliği** ve listeden **Proje**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="175da-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="175da-117">Tarayıcı olarak Internet Explorer kullanıyorsanız, dosyanın indirildiği konumdan el ile açmak için **Kaydet**'e tıklamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="175da-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="175da-118">Veya, **Kaydet ve aç**'a tıklayarak dosyayı Microsoft Project İstemcisinde açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="175da-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="175da-119">Kaydederken dosyayı yeniden adlandırmayın.</span><span class="sxs-lookup"><span data-stu-id="175da-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="175da-120">Dosyada Microsoft Project İstemcisi kullanarak düzenleme yapmadan önce dosyayı kullanıma almanız gerekir. **Microsoft Dynamics 365** sekmesinde **Kullanıma al**'a tıklayın. Bu, diğer kullanıcıların sizinle aynı anda Finance and Operations içinden iş kırılım yapısında düzenleme yapmasını engeller.</span><span class="sxs-lookup"><span data-stu-id="175da-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance and Operations at the same time.</span></span> <span data-ttu-id="175da-121">Tüm düzenlemeleri tamamladıktan sonra iş kırılım yapısını yayımlamak için **Microsoft Dynamics 365** sekmesinde **İade et**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="175da-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="175da-122">Bir proje ekibi Finance and Operations'ta zaten projeye eklendiyse, kaynak listesi bu ekibin üyeleri ile doldurulur.</span><span class="sxs-lookup"><span data-stu-id="175da-122">If a project team has already been added to the project in Finance and Operations, the resource list will be populated with the team members.</span></span> <span data-ttu-id="175da-123">Projeye henüz atanmış bir proje ekibi yoksa, kaynakları seçebilir ve ekibi Microsoft Project İstemcisi içinde **Microsoft Dynamics 365** sekmesinde yer alan **Kaynaklar**'a tıklayarak oluşturabilirsiniz..</span><span class="sxs-lookup"><span data-stu-id="175da-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="175da-124">Aşağıdaki veriler iade etme işleminin bir parçası olarak Finance and Operations ile eşitlenecektir:</span><span class="sxs-lookup"><span data-stu-id="175da-124">The following data will be synced back to Finance and Operations as part of the check in process:</span></span>

<span data-ttu-id="175da-125">•   Görev adı</span><span class="sxs-lookup"><span data-stu-id="175da-125">•   Task name</span></span>

<span data-ttu-id="175da-126">•   Başlangıç tarihi</span><span class="sxs-lookup"><span data-stu-id="175da-126">•   Start date</span></span>

<span data-ttu-id="175da-127">•   Bitiş tarihi</span><span class="sxs-lookup"><span data-stu-id="175da-127">•   Finish date</span></span>

<span data-ttu-id="175da-128">•   Önceller</span><span class="sxs-lookup"><span data-stu-id="175da-128">•   Predecessors</span></span>

<span data-ttu-id="175da-129">•   Kaynak adları</span><span class="sxs-lookup"><span data-stu-id="175da-129">•   Resource names</span></span>

<span data-ttu-id="175da-130">•   Kategori</span><span class="sxs-lookup"><span data-stu-id="175da-130">•   Category</span></span>

<span data-ttu-id="175da-131">•   Kaynak kategorisi</span><span class="sxs-lookup"><span data-stu-id="175da-131">•   Resource category</span></span>

<span data-ttu-id="175da-132">•   Çalışma saatleri</span><span class="sxs-lookup"><span data-stu-id="175da-132">•   Work hours</span></span>

<span data-ttu-id="175da-133">•   Notlar</span><span class="sxs-lookup"><span data-stu-id="175da-133">•   Notes</span></span>

<span data-ttu-id="175da-134">•   Öncelik</span><span class="sxs-lookup"><span data-stu-id="175da-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="175da-135">Microsoft Project İstemcisi dosyasına başka sütunlar eklerseniz, eklediğiniz sütunlar dosyaya kaydedilmez ve dosya tekrar açıldığında görüntülenmez.</span><span class="sxs-lookup"><span data-stu-id="175da-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="175da-136">Microsoft Project İstemcisi'ni kullanarak varolan bir proje için iş kırılım yapısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="175da-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="175da-137">Microsoft Project İstemcisi'ni kullanarak yeni iş kırılım yapısı oluşturmak için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="175da-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="175da-138">Microsoft Project İstemcisini açın.</span><span class="sxs-lookup"><span data-stu-id="175da-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="175da-139">**Microsoft Dynamics 365** sekmesinde **Aç**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="175da-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="175da-140">Proje için **tüzel kişilik** seçin.</span><span class="sxs-lookup"><span data-stu-id="175da-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="175da-141">**Proje**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="175da-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="175da-142">**Microsoft Dynamics 365** sekmesinde **Kullanıma al**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="175da-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="175da-143">Finance and Operations'a yayımlamaya hazır olduğunda, **Microsoft Dynamics 365** sekmesinde **İade et**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="175da-143">When ready to publish to Finance and Operations, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="175da-144">Microsoft Project İstemcisi'ni kullanarak varolan bir proje için mevcut iş kırılım yapısını değiştirme</span><span class="sxs-lookup"><span data-stu-id="175da-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="175da-145">Microsoft Project İstemcisi kullanarak yeni bir iş kırılım yapısı oluşturmak ve mevcut bir proje için mevcut iş kırılım yapısını değiştirmek için aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="175da-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="175da-146">Microsoft Project İstemcisini açın.</span><span class="sxs-lookup"><span data-stu-id="175da-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="175da-147">Microsoft Project İstemcisinde planı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="175da-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="175da-148">**Microsoft Dynamics 365** sekmesinde, **Değişiklikleri kaydet** > **Mevcut projeyi değiştir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="175da-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="175da-149">Proje için **tüzel kişilik** seçin.</span><span class="sxs-lookup"><span data-stu-id="175da-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="175da-150">**Proje**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="175da-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="175da-151">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="175da-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="175da-152">Microsoft Project İstemcisinden yeni bir proje oluşturma</span><span class="sxs-lookup"><span data-stu-id="175da-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="175da-153">Microsoft Project İstemcisini açın.</span><span class="sxs-lookup"><span data-stu-id="175da-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="175da-154">Microsoft Project İstemcisinde planı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="175da-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="175da-155">**Microsoft Dynamics 365** sekmesinde, **Değişiklikleri kaydet** > **Yeni Projeye kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="175da-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="175da-156">Proje için **tüzel kişilik** seçin.</span><span class="sxs-lookup"><span data-stu-id="175da-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="175da-157">Gerekirse **Proje kodu** girin.</span><span class="sxs-lookup"><span data-stu-id="175da-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="175da-158">**Proje adı** girin.</span><span class="sxs-lookup"><span data-stu-id="175da-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="175da-159">**Proje türü**'nü, **Proje grubu**'nu ve **Proje sözleşme kodu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="175da-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="175da-160">Alternatif olarak, **Yeni**'ye tıklayarak yeni bir proje sözleşmesi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="175da-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="175da-161">Kaynak atama için kullanılacak **Takvim**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="175da-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="175da-162">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="175da-162">Click **OK**.</span></span>

