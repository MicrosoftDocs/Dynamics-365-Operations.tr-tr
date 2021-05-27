---
title: Microsoft Teams ve Dynamics 365 Commerce POS arasında görev yönetimini eşitleme
description: Bu konu görev yönetiminin Microsoft Teams ile Dynamics 365 Commerce Satış noktası (POS) arasında nasıl eşitleneceğini açıklar.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 74d53a850113c83979fba6baa4ff3c3e5d9ca02d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020639"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a><span data-ttu-id="9a278-103">Microsoft Teams ve Dynamics 365 Commerce POS arasında görev yönetimini eşitleme</span><span class="sxs-lookup"><span data-stu-id="9a278-103">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9a278-104">Bu konu görev yönetiminin Microsoft Teams ile Dynamics 365 Commerce Satış noktası (POS) arasında nasıl eşitleneceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="9a278-104">This topic describes how to synchronize task management between Microsoft Teams and Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="9a278-105">Teams tümleştirmesinin başlıca amaçlarından biri, POS uygulaması ve Teams arasında görev yönetiminin eşitlenmesini etkinleştirmektir.</span><span class="sxs-lookup"><span data-stu-id="9a278-105">One of the main purposes of Teams integration is to enable the synchronization of task management between the POS application and Teams.</span></span> <span data-ttu-id="9a278-106">Böylece, mağaza çalışanları, görevleri yönetmek için POS uygulamasını veya Teams'i kullanabilir ve uygulamalarda geçiş yapmak zorunda kalmaz.</span><span class="sxs-lookup"><span data-stu-id="9a278-106">In this way, store employees can use either the POS application or Teams to manage tasks, and don't have to switch applications.</span></span>

<span data-ttu-id="9a278-107">Planner Teams'deki görevler için bir depo olarak kullanıldığı için, Teams ile Dynamics 365 Commerce arasında bir bağlantı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9a278-107">Because Planner is used as a repository for tasks in Teams, there must be a link between Teams and Dynamics 365 Commerce.</span></span> <span data-ttu-id="9a278-108">Bu bağlantı, belirli bir mağaza ekibi için özel bir plan kodu kullanılarak kurulur.</span><span class="sxs-lookup"><span data-stu-id="9a278-108">This link is established by using a specific plan ID for a given store team.</span></span>

<span data-ttu-id="9a278-109">Aşağıdaki yordamlarda, POS ve Teams uygulamaları arasında görev yönetimi eşitlemesinin nasıl ayarlanacağı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="9a278-109">The following procedures show how to set up task management synchronization between the POS and Teams applications.</span></span>

## <a name="publish-a-test-task-list-in-teams"></a><span data-ttu-id="9a278-110">Teams'de bir test görev listesi yayımlama</span><span class="sxs-lookup"><span data-stu-id="9a278-110">Publish a test task list in Teams</span></span>

<span data-ttu-id="9a278-111">Aşağıdaki prosedür, mağaza ekiplerinizin Commerce ile Microsoft Teams görev yönetimi tümleştirmesini ilk kez kullanmakta olduğunu varsayar.</span><span class="sxs-lookup"><span data-stu-id="9a278-111">The following procedure assumes that your store teams are using Microsoft Teams task management integration with Commerce for the first time.</span></span>

<span data-ttu-id="9a278-112">Teams'de bir test görev listesi yayımlamak için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="9a278-112">To publish a test task list in Teams, follow these steps.</span></span>

1. <span data-ttu-id="9a278-113">Teams'de iletişim yöneticisi olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="9a278-113">Sign in to Teams as a communications manager.</span></span> <span data-ttu-id="9a278-114">Genel olarak, iletişim yöneticileri Commerce'te **bölge yöneticisi** rolüne sahip kullanıcılardır.</span><span class="sxs-lookup"><span data-stu-id="9a278-114">Typically, communications managers are users who have the **Regional manager** role in Commerce.</span></span>
1. <span data-ttu-id="9a278-115">Sol gezinti bölmesinde, **Planner'daki Görevler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9a278-115">In the left navigation pane, select **Tasks by Planner**.</span></span>
1. <span data-ttu-id="9a278-116">**Yayımlanan listeler** sekmesinde, sol alt tarafta **yeni liste**'yi seçin ve yeni listeyi **Test görev listesi** olarak adlandırın.</span><span class="sxs-lookup"><span data-stu-id="9a278-116">On the **Published lists** tab, select **New list** in the lower left, and name the new list **Test task list**.</span></span>
1. <span data-ttu-id="9a278-117">**Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="9a278-117">Select **Create**.</span></span> <span data-ttu-id="9a278-118">Yeni liste **Taslaklar** altında görünür.</span><span class="sxs-lookup"><span data-stu-id="9a278-118">The new list appears under **Drafts**.</span></span>
1. <span data-ttu-id="9a278-119">**Görev başlığı** altında, ilk göreve,**Teams tümleştirmesi testi** başlığını verin.</span><span class="sxs-lookup"><span data-stu-id="9a278-119">Under **Task title**, give the first task the title **Testing Teams integration**.</span></span> <span data-ttu-id="9a278-120">**GİR**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="9a278-120">Then select **Enter**.</span></span>
1. <span data-ttu-id="9a278-121">**Taslaklar** listesinde, görev listesini seçin.</span><span class="sxs-lookup"><span data-stu-id="9a278-121">In the **Drafts** list, select the task list.</span></span> <span data-ttu-id="9a278-122">Ardından, sağ üst köşede  **yayımla** 'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="9a278-122">Then select **Publish** in the upper-right corner.</span></span>
1. <span data-ttu-id="9a278-123">**Kime yayımlanacağını seç** iletişim kutusunda, test görev listesini alması gereken ekipleri seçin.</span><span class="sxs-lookup"><span data-stu-id="9a278-123">In the **Select who to publish to** dialog box, select the teams that should receive the test task list.</span></span>
1. <span data-ttu-id="9a278-124">Yayın planınızı gözden geçirmek için **ileri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="9a278-124">Select **Next** to review your publication plan.</span></span> <span data-ttu-id="9a278-125">Değişiklik yapmanız gerekiyorsa,  **geri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="9a278-125">If you must make changes, select **Back**.</span></span> 
1. <span data-ttu-id="9a278-126">**Devam etmek için Onayla**'yı, ardından da **Yayınla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="9a278-126">Select **Confirm to proceed**, and then select **Publish**.</span></span>
1. <span data-ttu-id="9a278-127">Yayımlama tamamlandıktan sonra, **yayımlanan listeler** sekmesinin başındaki bir ileti, Görev listenizin başarıyla teslim edilip edilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a278-127">After publishing is completed, a message at the top of the **Published lists** tab indicates whether your task list was successfully delivered.</span></span>

<span data-ttu-id="9a278-128">Daha fazla bilgi için, bkz. [Kuruluşunuzda iş oluşturmak ve izlemek için görev listelerini yayımlama](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).</span><span class="sxs-lookup"><span data-stu-id="9a278-128">For more information, see [Publish task lists to create and track work in your organization](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).</span></span>

## <a name="link-pos-and-teams-for-task-management"></a><span data-ttu-id="9a278-129">Görev yönetimi için POS ve Teams'i bağlama</span><span class="sxs-lookup"><span data-stu-id="9a278-129">Link POS and Teams for task management</span></span>

<span data-ttu-id="9a278-130">POS ve Microsoft Teams uygulamalarını Commerce Headquarters'da görev yönetimi için bağlamak amacıyla aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="9a278-130">To link the POS and Microsoft Teams applications for task management in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="9a278-131">**Retail ve Commerce \> Veri yönetimi \> Microsoft Teams ile görev tümleştirme** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="9a278-131">Go to **Retail and Commerce \> Task management \> Tasks integration with Microsoft Teams**.</span></span>
1. <span data-ttu-id="9a278-132">Eylem Bölmesi'nde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="9a278-132">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="9a278-133">**Görev Yönetimi tümleştirmesini etkinleştir** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9a278-133">Set the **Enable Task Management Integration** option to **Yes**.</span></span>
1. <span data-ttu-id="9a278-134">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9a278-134">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="9a278-135">Eylem Panosundan **Görevi yönetimini ayarla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="9a278-135">On the Action Pane, select **Setup task management**.</span></span> <span data-ttu-id="9a278-136">**Teams sağlama** adlı bir toplu işin oluşturulmakta olduğunu gösteren bir bildirim almalısınız.</span><span class="sxs-lookup"><span data-stu-id="9a278-136">You should receive a notification that indicates that a batch job that is named **Teams provision** is being created.</span></span>
1. <span data-ttu-id="9a278-137">**Sistem Yönetimi \> sorgular \> toplu işler**'e gidin ve **Teams sağlama** açıklamasına sahip en son işi bulun.</span><span class="sxs-lookup"><span data-stu-id="9a278-137">Go to **System administration \> Inquiries \> Batch jobs**, and find the most recent job that has the description **Teams provision**.</span></span> <span data-ttu-id="9a278-138">Bu işin çalışması bitene kadar bekleyin.</span><span class="sxs-lookup"><span data-stu-id="9a278-138">Wait until this job has finished running.</span></span>
1. <span data-ttu-id="9a278-139">Plan kodunu ve mağaza referanslarını Retail Server'a yayımlamak için **CDX İş 1070**'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="9a278-139">Run the **CDX job 1070** to publish the plan ID and store references to Retail Server.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9a278-140">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="9a278-140">Additional resources</span></span>

[<span data-ttu-id="9a278-141">Dynamics 365 Commerce ve Microsoft Teams tümleştirmesine genel bakış</span><span class="sxs-lookup"><span data-stu-id="9a278-141">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="9a278-142">Dynamics 365 Commerce ve Microsoft Teams tümleştirmesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="9a278-142">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="9a278-143">Dynamics 365 Commerce'ten Microsoft Teams sağlama</span><span class="sxs-lookup"><span data-stu-id="9a278-143">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="9a278-144">Microsoft Teams'de kullanıcı rollerini yönetme</span><span class="sxs-lookup"><span data-stu-id="9a278-144">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="9a278-145">Microsoft Teams'de önceden var olan ekipler varsa mağazaları ve ekipleri eşleme</span><span class="sxs-lookup"><span data-stu-id="9a278-145">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="9a278-146">Dynamics 365 Commerce ve Microsoft Teams tümleştirmesi SSS</span><span class="sxs-lookup"><span data-stu-id="9a278-146">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
