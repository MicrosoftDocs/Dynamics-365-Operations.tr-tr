---
title: Dynamics 365 Commerce'ten Microsoft Teams sağlama
description: Bu konu, Dynamics 365 Commerce'deki organizasyon verilerini kullanarak nasıl Microsoft Teams sağlanacağını açıklar.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 96382c072e03506294d72899072a358091bda8ab
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842764"
---
# <a name="provision-microsoft-teams-from-dynamics-365-commerce"></a><span data-ttu-id="3e13c-103">Dynamics 365 Commerce'ten Microsoft Teams sağlama</span><span class="sxs-lookup"><span data-stu-id="3e13c-103">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="3e13c-104">Bu konu, Dynamics 365 Commerce'deki organizasyon verilerini kullanarak nasıl Microsoft Teams sağlanacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="3e13c-104">This topic describes how to provision Microsoft Teams by using organizational data from Dynamics 365 Commerce.</span></span>

<span data-ttu-id="3e13c-105">Dynamics 365 Commerce henüz perakende mağazalarınız için Teams'i ayarlamadıysanız, Teams sağlamak için kolay bir yol sunar.</span><span class="sxs-lookup"><span data-stu-id="3e13c-105">Dynamics 365 Commerce offers an easy way to provision Teams if you haven't yet set up teams for your retail stores there.</span></span> <span data-ttu-id="3e13c-106">Teams'de kullanmak istediğiniz Commerce'teki iyi tanımlanmış bilgilerden yararlanarak, mağaza çalışanlarınızın Teams'i kullanmaya başlaması konusunda yardımcı olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3e13c-106">By taking advantage of well-defined information from Commerce that you want to use in Teams, you can help your store employees get started in Teams.</span></span> <span data-ttu-id="3e13c-107">Bu bilgiler, organizasyon hiyerarşisi, mağaza adları, çalışan bilgileri ve Azure Active Directory (Azure AD) hesaplarını içerir.</span><span class="sxs-lookup"><span data-stu-id="3e13c-107">This information includes the organizational hierarchy, store names, employee information, and Azure Active Directory (Azure AD) accounts.</span></span> 

<span data-ttu-id="3e13c-108">Teams sağlama işleminin iki ana adımı vardır:</span><span class="sxs-lookup"><span data-stu-id="3e13c-108">The process of provisioning Teams has two main steps:</span></span>

1. <span data-ttu-id="3e13c-109">Teams'de her perakende mağazası için bir ekip oluşturun ve mağaza çalışanlarını uygun ekibin üyeleri olarak ekleyin.</span><span class="sxs-lookup"><span data-stu-id="3e13c-109">In Teams, create a team for each retail store, and add store workers as members of the appropriate team.</span></span> <span data-ttu-id="3e13c-110">Bir çalışan birden fazla perakende mağazası ile ilişkilendirilmişse, ekip üyeliği bu olguyu yansıtır.</span><span class="sxs-lookup"><span data-stu-id="3e13c-110">If an employee is associated with more than one retail store, team membership will reflect that fact.</span></span> <span data-ttu-id="3e13c-111">Teams'den görev yayımlamaya yardımcı olmak üzere, bölgesel yöneticilerini üye olarak içeren bir iletişim ekibi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3e13c-111">A communications team that includes regional managers as members will be created to help publish tasks from Teams.</span></span>
1. <span data-ttu-id="3e13c-112">Organizasyon hiyerarşinizi Commerce'ten Teams'e yükleyin.</span><span class="sxs-lookup"><span data-stu-id="3e13c-112">Upload your organizational hierarchy from Commerce to Teams.</span></span>

## <a name="provision-teams-in-commerce-headquarters"></a><span data-ttu-id="3e13c-113">Commerce Headquarters'da Teams'i sağlama</span><span class="sxs-lookup"><span data-stu-id="3e13c-113">Provision Teams in Commerce headquarters</span></span>

<span data-ttu-id="3e13c-114">Microsoft Teams'i sağlamadan önce, aşağıdaki görevleri tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="3e13c-114">Before you provision Microsoft Teams, complete these tasks:</span></span>

- <span data-ttu-id="3e13c-115">Tüm bölgesel yöneticilerin iletişim yöneticileri yapıldığını onaylayın.</span><span class="sxs-lookup"><span data-stu-id="3e13c-115">Confirm that all regional managers have been made communications managers.</span></span>
- <span data-ttu-id="3e13c-116">Her mağaza yöneticisinin ve çalışanın Azure hesabının Commerce Headquarters'da o yöneticinin veya çalışanın çalışan kaydıyla ilişkilendirildiğini onaylayın.</span><span class="sxs-lookup"><span data-stu-id="3e13c-116">Confirm that the Azure account of every store manager and worker has been associated with that manager's or worker's worker record in Commerce headquarters.</span></span>

<span data-ttu-id="3e13c-117">Commerce Headquarters'da Teams'i sağlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="3e13c-117">To provision Teams in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="3e13c-118">**Retail ve Commerce \> Kanal kurulumu \> Microsoft Teams tümleştirme yapılandırması** na gidin.</span><span class="sxs-lookup"><span data-stu-id="3e13c-118">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="3e13c-119">Eylem bölmesinde, **Teams sağla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="3e13c-119">On the Action Pane, select **Provision teams**.</span></span> <span data-ttu-id="3e13c-120">**Teams sağlama** adlı bir toplu iş oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3e13c-120">A batch job that is named **Teams provision** is created.</span></span>
1. <span data-ttu-id="3e13c-121">**Sistem Yönetimi \> sorgular \> toplu işler**'e gidin ve **Teams sağlama** açıklamasına sahip en son işi bulun.</span><span class="sxs-lookup"><span data-stu-id="3e13c-121">Go to **System administration \> Inquiries \> Batch jobs**, and find the most recent job that has the description **Teams provision**.</span></span> <span data-ttu-id="3e13c-122">Bu işin çalışması bitene kadar bekleyin.</span><span class="sxs-lookup"><span data-stu-id="3e13c-122">Wait until this job has finished running.</span></span>

> [!TIP]
> <span data-ttu-id="3e13c-123">Bölgesel yöneticileriniz, mağaza yöneticileri ve mağaza arkadaşlarınız bir Teams lisansıyla ilişkilendirilmediği takdirde, aşağıdaki hata iletisini alabilirsiniz: "Kullanıcı için appliable SKU kategorileri alınamadı."</span><span class="sxs-lookup"><span data-stu-id="3e13c-123">If none of your regional managers, store managers, and store workers have been associated with a Teams license, you might receive the following error message: "Failed to retrieve appliable Sku categories for the user."</span></span> <span data-ttu-id="3e13c-124">Sorunu düzeltmek için, Eylem bölmesinde, **Teams ve üyeleri Eşitle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3e13c-124">To correct the issue, select **Sync teams and members** on the Action Pane.</span></span>

<!-- ![Dynamics 365 Commerce - Teams integration configuration](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)-->

## <a name="validate-teams-provisioning-in-the-teams-admin-center"></a><span data-ttu-id="3e13c-125">Teams Yönetim merkezinde Teams sağlamayı doğrulama</span><span class="sxs-lookup"><span data-stu-id="3e13c-125">Validate Teams provisioning in the Teams admin center</span></span>

<span data-ttu-id="3e13c-126">Microsoft Teams Yönetim Merkezi'nde Microsoft Teams sağlamayı doğrulamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="3e13c-126">To validate Microsoft Teams provisioning in the Microsoft Teams admin center, follow these steps.</span></span>
    
1. <span data-ttu-id="3e13c-127">[Teams yönetim merkezine gidin](https://admin.teams.microsoft.com/) ve e-ticaret kiracınızın Yöneticisi olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="3e13c-127">Go to the [Teams admin center](https://admin.teams.microsoft.com/), and sign in as the administrator of your e-commerce tenant.</span></span>
1. <span data-ttu-id="3e13c-128">Sol gezinti bölmesinde, genişletmek için **Teams**'i seçin ve sonra **Ekipleri yönet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3e13c-128">In the left navigation pane, select **Teams** to expand it, and then select **Manage teams**.</span></span>
1. <span data-ttu-id="3e13c-129">Her bir Commerce Retail Store için bir ekibin oluşturulmuş olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="3e13c-129">Confirm that one team has been created for each Commerce retail store.</span></span>
1. <span data-ttu-id="3e13c-130">Bir ekip seçin ve mağaza çalışanlarının üye olarak eklendiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="3e13c-130">Select a team, and confirm that store workers have been added to it as members.</span></span>
1. <span data-ttu-id="3e13c-131">Sol gezinti bölmesinde, **kullanıcıları** seçin ve tüm mağazalardaki tüm mağaza çalışanlarının Kullanıcı olarak eklendiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="3e13c-131">In the left navigation pane, select **Users**, and confirm that all store employees in all stores have been added as users.</span></span>

<span data-ttu-id="3e13c-132">Aşağıdaki çizimde, Teams Yönetim merkezinde bulunan **Ekipleri Yönet** sayfasının bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="3e13c-132">The following illustration shows an example of the **Manage teams** page in the Teams admin center.</span></span>

![Teams Yönetim Merkezi'ndeki ekipleri Yönet sayfası örneği](media/Teams-FLW-Admin-Teams.png)

## <a name="upload-a-commerce-organizational-hierarchy-to-teams"></a><span data-ttu-id="3e13c-134">Commerce Organizasyon hiyerarşinizi Teams'e yükleme</span><span class="sxs-lookup"><span data-stu-id="3e13c-134">Upload a Commerce organizational hierarchy to Teams</span></span>
    
<span data-ttu-id="3e13c-135">Commerce organizasyon hiyerarşisi, aynı hiyerarşi yapısını kullanan tüm ya da seçilen mağazalara görev yayınlamak için Microsoft Teams'de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="3e13c-135">The Commerce organizational hierarchy can be used in Microsoft Teams to publish tasks to all or selected stores that use the same hierarchy structure.</span></span>

<span data-ttu-id="3e13c-136">Commerce organizasyon hiyerarşisini Teams'e yüklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="3e13c-136">To upload a Commerce organizational hierarchy to Teams, follow these steps.</span></span>
    
1. <span data-ttu-id="3e13c-137">Commerce headquarters'da **Retail ve Commerce \> Kanal ayarı \> Microsoft Teams Tümleştirme Yapılandırması**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="3e13c-137">In Commerce headquarters, go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="3e13c-138">Organizasyon hiyerarşisinin bir virgülle ayrılmış değerler (CSV) dosyasını indirmek için, **hedef hiyerarşiyi yükle**'yi seçin ve **bölgeye göre perakende mağazalardan** birini seçin.</span><span class="sxs-lookup"><span data-stu-id="3e13c-138">Select **Download targeting hierarchy**, and then select **Retail Stores by Region** to download a comma-separated values (CSV) file of the organizational hierarchy.</span></span>
1. <span data-ttu-id="3e13c-139">Microsoft Teams PowerShell modülünü [Microsoft Teams PowerShell modülünü yükleme](https://docs.microsoft.com/microsoftteams/teams-powershell-install) bölümündeki adımları kullanarak yükleyin.</span><span class="sxs-lookup"><span data-stu-id="3e13c-139">Install the Microsoft Teams PowerShell module by following the steps in [Install Microsoft Teams PowerShell](https://docs.microsoft.com/microsoftteams/teams-powershell-install).</span></span>
1. <span data-ttu-id="3e13c-140">Teams PowerShell penceresinde sorulduğunda, Azure AD kiracınıza ait yönetici hesabını kullanarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="3e13c-140">When you're prompted in the Teams PowerShell window, sign in by using the administrator account for your Azure AD tenant.</span></span>
1. <span data-ttu-id="3e13c-141">Hedefleme hiyerarşisinin CSV dosyasını yüklemek için [takım hedefleme hiyerarşinizi ayarlama](https://docs.microsoft.com/microsoftteams/set-up-your-team-hierarchy) adımlarını izleyin.</span><span class="sxs-lookup"><span data-stu-id="3e13c-141">Follow the steps in [Set up your team targeting hierarchy](https://docs.microsoft.com/microsoftteams/set-up-your-team-hierarchy) to upload the CSV file for the targeting hierarchy.</span></span>

## <a name="verify-that-the-organizational-hierarchy-was-uploaded-to-teams"></a><span data-ttu-id="3e13c-142">Kuruluş hiyerarşisinin Teams'e yüklenmiş olduğunu doğrulayın</span><span class="sxs-lookup"><span data-stu-id="3e13c-142">Verify that the organizational hierarchy was uploaded to Teams</span></span>

<span data-ttu-id="3e13c-143">Kuruluş hiyerarşisinin Microsoft Teams'e yüklenmiş olduğunu doğrulamak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="3e13c-143">To verify that the organizational hierarchy was uploaded to Microsoft Teams, follow these steps.</span></span>

1. <span data-ttu-id="3e13c-144">Teams'de iletişim yöneticisi olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="3e13c-144">Sign in to Teams as a communications manager.</span></span>
1. <span data-ttu-id="3e13c-145">Sol gezinti bölmesinde, **Planner'daki Görevler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3e13c-145">In the left navigation pane, select **Tasks by Planner**.</span></span>
1. <span data-ttu-id="3e13c-146">**Yayınlanan listeler** sekmesinde, sözde görevi olan yeni bir liste oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3e13c-146">On the **Published lists** tab, create a new list that has a dummy task.</span></span>
1. <span data-ttu-id="3e13c-147">**Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="3e13c-147">Select **Publish**.</span></span> <span data-ttu-id="3e13c-148">Aşağıdaki çizimdeki örnekte gösterildiği gibi, kuruluş hiyerarşisi **Kime yayımlanacağını seç** iletişim kutusunda görünür.</span><span class="sxs-lookup"><span data-stu-id="3e13c-148">The organizational hierarchy should appear in the **Select who to publish to** dialog box, as shown in the example in the following illustration.</span></span>

![Kime yayımlanacağını seç iletişim kutusunda kuruluş hiyerarşisi örneği](media/Microsoft-teams-verify-org-hierarchy.png)

## <a name="additional-resources"></a><span data-ttu-id="3e13c-150">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="3e13c-150">Additional resources</span></span>

[<span data-ttu-id="3e13c-151">Dynamics 365 Commerce ve Microsoft Teams tümleştirmesine genel bakış</span><span class="sxs-lookup"><span data-stu-id="3e13c-151">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="3e13c-152">Dynamics 365 Commerce ve Microsoft Teams tümleştirmesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="3e13c-152">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="3e13c-153">Microsoft Teams ve Dynamics 365 Commerce POS arasında görev yönetimini eşitleme</span><span class="sxs-lookup"><span data-stu-id="3e13c-153">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="3e13c-154">Microsoft Teams'de kullanıcı rollerini yönetme</span><span class="sxs-lookup"><span data-stu-id="3e13c-154">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="3e13c-155">Microsoft Teams'de önceden var olan ekipler varsa mağazaları ve ekipleri eşleme</span><span class="sxs-lookup"><span data-stu-id="3e13c-155">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="3e13c-156">Dynamics 365 Commerce ve Microsoft Teams tümleştirmesi SSS</span><span class="sxs-lookup"><span data-stu-id="3e13c-156">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
