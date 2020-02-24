---
title: Dynamics 365 Commerce önizleme ortamını hazırlama
description: Bu konu, hazırlandıktan sonra Microsoft Dynamics 365 Commerce önizleme ortamının nasıl yapılandırılacağını açıklamaktadır.
author: psimolin
manager: annbe
ms.date: 01/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: cbd4c118de2e91c8849461b20a01403049a07e66
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024648"
---
# <a name="provision-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="759fa-103">Dynamics 365 Commerce önizleme ortamını hazırlama</span><span class="sxs-lookup"><span data-stu-id="759fa-103">Provision a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="759fa-104">Bu konu, hazırlandıktan sonra Dynamics 365 Commerce önizleme ortamının nasıl yapılandırılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="759fa-104">This topic explains how to provision a Dynamics 365 Commerce preview environment.</span></span>

<span data-ttu-id="759fa-105">Başlamadan önce, işlemin gerek duyduğu bir fikir almak için bu konu hakkında hızlı bir tarama yapmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="759fa-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="759fa-106">Dynamics 365 Commerce önizleme'ye erişim izni verilmemişse, [Dynamics 365 Commerce Web sitesinden](https://aka.ms/Dynamics365CommerceWebsite) önizleme erişimi isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="759fa-106">If you haven't yet been granted access to the Dynamics 365 Commerce preview, you can request preview access from the [Dynamics 365 Commerce website](https://aka.ms/Dynamics365CommerceWebsite).</span></span>

## <a name="overview"></a><span data-ttu-id="759fa-107">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="759fa-107">Overview</span></span>

<span data-ttu-id="759fa-108">Commerce önizleme ortamınızı başarıyla sağlamak için, belirli bir ürün adı ve türü olan bir proje oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="759fa-108">To successfully provision your Commerce preview environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="759fa-109">Ortam ve commerce scale unit (CSU), ayrıca, e-ticaret sağlamasının daha sonra başlatmak için kullanmanız gereken belirli parametreleri de vardır.</span><span class="sxs-lookup"><span data-stu-id="759fa-109">The environment and commerce scale unit (CSU) also have some specific parameters that you must use when you provision e-Commerce later.</span></span> <span data-ttu-id="759fa-110">Bu konudaki yönergeler, tamamlamanız gereken tüm gerekli adımları ve kullanmanız gereken parametreleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="759fa-110">The instructions in this topic describe all the steps required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="759fa-111">Sağlama başarılı olduktan sonra, Ticari önizleme ortamınızı hazırlamak için almanız gereken birkaç son işlem adımı vardır.</span><span class="sxs-lookup"><span data-stu-id="759fa-111">After you successfully provision your Commerce preview environment, you must complete a few post-provisioning steps to prepare it.</span></span> <span data-ttu-id="759fa-112">Sistemin hangi yönlere göre değerlendirileceğini bağlı olarak bazı adımlar isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="759fa-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="759fa-113">İsteğe bağlı adımları istediğiniz zaman daha sonra da tamamlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="759fa-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="759fa-114">Commerce önizleme ortamını yapılandırma hakkında bilgi için bkz. [Commerce önizleme ortamı yapılandırma](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="759fa-114">For information about how to configure your Commerce preview environment after you provision it, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="759fa-115">Commerce Preview ortamınızla ilgili isteğe bağlı özellikleri konfigüre etmek için, bkz. [Commerce önizleme ortamınız için isteğe bağlı özellikler yapılandırın](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="759fa-115">For information about how to configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

<span data-ttu-id="759fa-116">Sağlama adımlarıyla ilgili sorularınız varsa veya herhangi bir sorunla karşılaşırsanız, lütfen [Microsoft Dynamics 365 Commerce önizleme Yammer grubunda](https://aka.ms/Dynamics365CommercePreviewYammer) Microsoft'a bildirin.</span><span class="sxs-lookup"><span data-stu-id="759fa-116">If you have any questions about the provisioning steps, or if you encounter any issues, let Microsoft know in the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="759fa-117">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="759fa-117">Prerequisites</span></span>

<span data-ttu-id="759fa-118">Commerce önizleme ortamınızı hazırlayabilmeniz için aşağıdaki önkoşulların yerinde olması gerekir:</span><span class="sxs-lookup"><span data-stu-id="759fa-118">The following prerequisites must be in place before you can provision your Commerce preview environment:</span></span>

- <span data-ttu-id="759fa-119">Microsoft Dynamics Lifecycle Services (LCS) portalına erişim hakkınız var</span><span class="sxs-lookup"><span data-stu-id="759fa-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="759fa-120">Varolan Microsoft Dynamics 365 ortağı veya müşterisiyseniz ve Dynamics 365 Commerce proje oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="759fa-120">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="759fa-121">Dynamics 365 Commerce Önizleme programına kabul edilmiş olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="759fa-121">You've been accepted into the Dynamics 365 Commerce Preview program.</span></span>
- <span data-ttu-id="759fa-122">**Geçiş yapmak, çözüm oluşturmak ve daha fazla bilgi edinmek** için bir proje oluşturmaya gerekli izinleriniz vardır.</span><span class="sxs-lookup"><span data-stu-id="759fa-122">You have the required permissions to create a project for **Migrate, create solutions, and learn**.</span></span>
- <span data-ttu-id="759fa-123">Ortamı sağlamak istediğiniz **Ortam yöneticisi** veya **Proje sahibi** rolünün bir üyesisinizdir.</span><span class="sxs-lookup"><span data-stu-id="759fa-123">You're a member of the **Environment manager** or **Project owner** role in the project where you will provision the environment.</span></span>
- <span data-ttu-id="759fa-124">Microsoft Azure aboneliğinize yönetici erişiminiz var veya sizin adınıza yönetici izinleri gerektiren iki adımı gerçekleştirebilecek bir abonelik Yöneticisi ile ilişki kurun.</span><span class="sxs-lookup"><span data-stu-id="759fa-124">You have admin access to your Microsoft Azure subscription, or you're in contact with a subscription admin who can complete the two steps that require admin permissions on your behalf.</span></span>
- <span data-ttu-id="759fa-125">Azure Active Directory (Azure AD) kiracı kimliğiniz kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="759fa-125">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="759fa-126">E-ticaret sistem yöneticileri grubu olarak kullanılacak bir Azure AD güvenlik grubu oluşturdunuz ve kimliğiniz kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="759fa-126">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="759fa-127">Derecelendirme ve incelemeler grubu olarak kullanılacak bir Azure AD güvenlik grubu oluşturdunuz ve kimliğiniz kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="759fa-127">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="759fa-128">(Bu güvenlik grubu e-ticaret Sistem Yöneticisi grubuyla aynı olabilir.)</span><span class="sxs-lookup"><span data-stu-id="759fa-128">(This security group can be the same as the e-Commerce system admin group.)</span></span>

## <a name="provision-your-commerce-preview-environment"></a><span data-ttu-id="759fa-129">Commerce önizleme ortamınızı sağlama</span><span class="sxs-lookup"><span data-stu-id="759fa-129">Provision your Commerce preview environment</span></span>

<span data-ttu-id="759fa-130">Bu yöntemlerde, bir Commerce Preview ortamının nasıl sağlanacağı açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="759fa-130">These procedures explain how to provision a Commerce preview environment.</span></span> <span data-ttu-id="759fa-131">Bunları başarıyla tamamladıktan sonra, Commerce Preview ortamı konfigürasyon için hazır olacak.</span><span class="sxs-lookup"><span data-stu-id="759fa-131">After you successfully complete them, the Commerce preview environment will be ready for configuration.</span></span> <span data-ttu-id="759fa-132">Burada açıklanan tüm etkinlikler LCS portalında yer alabilir.</span><span class="sxs-lookup"><span data-stu-id="759fa-132">All the activities that are described here occur in the LCS portal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="759fa-133">Önizleme erişimi, Commerce önizleme uygulamanızda belirttiğiniz LCS hesabına ve kuruluşa bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="759fa-133">Preview access is tied to the LCS account and organization that you specified in your Commerce preview application.</span></span> <span data-ttu-id="759fa-134">Commerce Preview ortamını sağlamak için aynı hesabı kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="759fa-134">You must use the same account to provision the Commerce preview environment.</span></span> <span data-ttu-id="759fa-135">Commerce Preview ortamı için farklı bir LCS hesabı veya kiracı kullanmanız gerekiyorsa, bu ayrıntıları Microsoft'a sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="759fa-135">If you need to use a different LCS account or tenant for the Commerce preview environment, you must provide those details to Microsoft.</span></span> <span data-ttu-id="759fa-136">Başvuru bilgileri için bu konudaki [Commerce önizleme ortam desteği](#commerce-preview-environment-support) başlıklı bölüme bakın.</span><span class="sxs-lookup"><span data-stu-id="759fa-136">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section later in this topic.</span></span>

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a><span data-ttu-id="759fa-137">Önizleme özelliklerinin kullanılabilir ve LCS'de açık olduğunu onaylayın</span><span class="sxs-lookup"><span data-stu-id="759fa-137">Confirm that preview features are available and turned on in LCS</span></span>

<span data-ttu-id="759fa-138">Önizleme özelliklerinin kullanılabilir ve LCS'de açık olduğunu onaylamak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="759fa-138">To confirm that preview features are available and turned on in LCS, follow these steps.</span></span>

1. <span data-ttu-id="759fa-139">Bu önizlemeye erişim istemek için kullandığınız LCS hesabını kullanarak [LCS portalında](https://lcs.dynamics.com) oturum açın.</span><span class="sxs-lookup"><span data-stu-id="759fa-139">Sign in to the [LCS portal](https://lcs.dynamics.com) by using the same LCS account that you used to request access to the preview.</span></span>
1. <span data-ttu-id="759fa-140">LCS ana sayfasında, tüm yolu sağa kaydırın ve **önizleme özelliği yönetim** kutucuğunu tıklatın.</span><span class="sxs-lookup"><span data-stu-id="759fa-140">On the LCS home page, scroll all the way to the right, and select the **Preview feature management** tile.</span></span>

    ![Önizleme yönetimi kutucuğu](./media/preview1.png)

1. <span data-ttu-id="759fa-142">**ÖZEL ÖNİZLEME ÖZELLİKLERİ**'ne gidin ve aşağıdaki özelliklerin kullanılabilir ve açık olduğundan emin olun:</span><span class="sxs-lookup"><span data-stu-id="759fa-142">Scroll down to **Private preview features**, and confirm that the following features are available and turned on:</span></span>

    - <span data-ttu-id="759fa-143">e-Ticaret değerlendirmesi</span><span class="sxs-lookup"><span data-stu-id="759fa-143">e-Commerce Evaluation</span></span>
    - <span data-ttu-id="759fa-144">Ticaret Önizleme Programı Ortamları</span><span class="sxs-lookup"><span data-stu-id="759fa-144">Commerce Preview Program Environments</span></span>

    ![Özel önizleme özellikleri](./media/preview2.png)

1. <span data-ttu-id="759fa-146">Listede bu özellikler görüntülenmiyorsa, Microsoft'a başvurun ve iş e-posta adresiniz, LCS hesabı ve kiracı ayrıntılarını sağlayın.</span><span class="sxs-lookup"><span data-stu-id="759fa-146">If those features don't appear in the list, contact Microsoft, and provide your work email address, LCS account, and tenant details.</span></span> <span data-ttu-id="759fa-147">Başvuru bilgileri için [Commerce önizleme ortam desteği](#commerce-preview-environment-support) başlıklı bölüme bakın.</span><span class="sxs-lookup"><span data-stu-id="759fa-147">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="759fa-148">Yeni proje oluştur</span><span class="sxs-lookup"><span data-stu-id="759fa-148">Create a new project</span></span>

<span data-ttu-id="759fa-149">LCS'de bir yeni proje oluşturmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="759fa-149">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="759fa-150">LCS giriş sayfasında, bir proje oluşturmak için artı işaretini (**+**) seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-150">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="759fa-151">Sağ bölmede aşağıdaki adımlardan birini izleyin:</span><span class="sxs-lookup"><span data-stu-id="759fa-151">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="759fa-152">Bir ortaksanız **taşı, çözüm oluştur ve öğren**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-152">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="759fa-153">Müşterisiyseniz, **olası ön satışlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-153">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="759fa-154">Şablon adı, açıklama ve sektör girin.</span><span class="sxs-lookup"><span data-stu-id="759fa-154">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="759fa-155">**Ürün adı** alanından **Dynamics 365 Retail** seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-155">In the **Product name** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="759fa-156">**Ürün sürümü** alanından **Dynamics 365 Retail** seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-156">In the **Product version** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="759fa-157">**Metodoloji** alanında **Dynamics Retail uygulama metodoloji**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-157">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="759fa-158">İsteğe bağlı: Roller ve kullanıcılar mevcut projeden içeri aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="759fa-158">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="759fa-159">**Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-159">Select **Create**.</span></span> <span data-ttu-id="759fa-160">Proje görünümü gösterilir.</span><span class="sxs-lookup"><span data-stu-id="759fa-160">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="759fa-161">Azure bağlayıcısı ekle</span><span class="sxs-lookup"><span data-stu-id="759fa-161">Add the Azure Connector</span></span>

<span data-ttu-id="759fa-162">Bir Azure Connector'ı LCS projenize eklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="759fa-162">To add the Azure Connector to your LCS project, follow these steps.</span></span>

1. <span data-ttu-id="759fa-163">Şu adımlardan birini izleyin:</span><span class="sxs-lookup"><span data-stu-id="759fa-163">Follow one of these steps:</span></span>

    - <span data-ttu-id="759fa-164">Ortak iseniz, en sağdaki **proje ayarları** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-164">If you're a partner, select the **Project settings** tile on the far right.</span></span>
    - <span data-ttu-id="759fa-165">Müşterisiyseniz, üst menüden **proje ayarları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-165">If you're a customer, select **Project settings** on the top menu.</span></span>

1. <span data-ttu-id="759fa-166">**Azure bağlayıcısı** seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-166">Select **Azure connectors**.</span></span>
1. <span data-ttu-id="759fa-167">Bir Azure bağlayıcısı eklemek için, **Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="759fa-167">Select **Add** to add the Azure Connector.</span></span>
1. <span data-ttu-id="759fa-168">Bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="759fa-168">Enter a name.</span></span>
1. <span data-ttu-id="759fa-169">Azure abonelik kimliğinizi girin.</span><span class="sxs-lookup"><span data-stu-id="759fa-169">Enter your Azure subscription ID.</span></span>
1. <span data-ttu-id="759fa-170">**Azure Resource Manager (ARM) kullanmak için yapılandırın** seçeneğini açın.</span><span class="sxs-lookup"><span data-stu-id="759fa-170">Turn on the **Configure to use Azure Resource Manager (ARM)** option.</span></span>
1. <span data-ttu-id="759fa-171">**Azure aboneliği AAD kiracı etki alanının (veya kimlik)** değerinin doğru olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="759fa-171">Verify that the **Azure subscription AAD Tenant Domain (or ID)** value is correct.</span></span> <span data-ttu-id="759fa-172">Gerekiyorsa, Azure abonelik yöneticinize başvurun.</span><span class="sxs-lookup"><span data-stu-id="759fa-172">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="759fa-173">**Sonraki**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-173">Select **Next**.</span></span>
1. <span data-ttu-id="759fa-174">Gerekli uygulamaların aboneliğinize erişim izni vermek için sayfadaki yönergeleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="759fa-174">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="759fa-175">Gerekiyorsa, Azure abonelik yöneticinize başvurun.</span><span class="sxs-lookup"><span data-stu-id="759fa-175">Consult your Azure subscription admin as required.</span></span>

    1. <span data-ttu-id="759fa-176">[Azure portalında](https://portal.azure.com/) adresinden oturum açın.</span><span class="sxs-lookup"><span data-stu-id="759fa-176">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
    1. <span data-ttu-id="759fa-177">Doğru dizinin seçildiğinden emin olun ve soldaki menüde **Abonelikler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-177">Make sure that the correct directory is selected, and then, on the menu on the left, select **Subscriptions**.</span></span>
    1. <span data-ttu-id="759fa-178">Listeden doğru aboneliği bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-178">Find the correct subscription in the list, and select it.</span></span> <span data-ttu-id="759fa-179">Gerektiğinde arama işlevini kullanın.</span><span class="sxs-lookup"><span data-stu-id="759fa-179">Use the search functionality as required.</span></span>
    1. <span data-ttu-id="759fa-180">Menüde, **erişim denetimi (IAM)** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="759fa-180">On the menu, select **Access control (IAM)**.</span></span>
    1. <span data-ttu-id="759fa-181">Sağ tarafta **rol ataması eklemek** için **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="759fa-181">On the right, under **Add a role assignment**, select **Add**.</span></span> <span data-ttu-id="759fa-182">**Role atama ekle** bölmesi görünür.</span><span class="sxs-lookup"><span data-stu-id="759fa-182">The **Add role assignment** pane appears.</span></span>
    1. <span data-ttu-id="759fa-183">**Rol** alanında **Katkı sağlayan**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-183">In the **Role** field, select **Contributor**.</span></span>
    1. <span data-ttu-id="759fa-184">**Erişimi ata** alanında, varsayılan değeri, **Azure AD kullanıcıyı, grubu veya servis sorumlusunu** bırakın.</span><span class="sxs-lookup"><span data-stu-id="759fa-184">In the **Assign access to** field, leave the default value, **Azure AD user, group, or service principal**.</span></span>
    1. <span data-ttu-id="759fa-185">**Seç** altında, **b96b7e94-b82e-4e71-99a0-cf7fb188acea** girin.</span><span class="sxs-lookup"><span data-stu-id="759fa-185">Under **Select**, enter **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span></span>
    1. <span data-ttu-id="759fa-186">Listeden **Dynamics dağıtım hizmetlerini \[wsfed-etkin\]** seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-186">Select **Dynamics Deployment Services \[wsfed-enabled\]** in the list.</span></span>
    1. <span data-ttu-id="759fa-187">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-187">Select **Save**.</span></span>

1. <span data-ttu-id="759fa-188">**Sonraki**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-188">Select **Next**.</span></span>
1. <span data-ttu-id="759fa-189">Gerekli uygulamaların aboneliğinize erişim izni vermek için sayfadaki yönergeleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="759fa-189">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="759fa-190">Gerekiyorsa, Azure abonelik yöneticinize başvurun.</span><span class="sxs-lookup"><span data-stu-id="759fa-190">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="759fa-191">**Sonraki**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-191">Select **Next**.</span></span>
1. <span data-ttu-id="759fa-192">**Azure bölgesi** alanında, **Doğu ABD**, **Doğu ABD 2**, **Batı ABD** veya **Batı ABD 2** seçeneklerinden birini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="759fa-192">In the **Azure region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="759fa-193">**Bağlan**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-193">Select **Connect**.</span></span> <span data-ttu-id="759fa-194">Azure Bağlayıcınız listede görünmelidir.</span><span class="sxs-lookup"><span data-stu-id="759fa-194">Your Azure Connector should appear in the list.</span></span>

### <a name="import-the-commerce-preview-demo-base-extension"></a><span data-ttu-id="759fa-195">Commerce önizleme demo temel uzantısını içe aktar</span><span class="sxs-lookup"><span data-stu-id="759fa-195">Import the Commerce Preview Demo Base Extension</span></span>

<span data-ttu-id="759fa-196">Commerce Önizleme demo temel uzantısını projenize içe aktarmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="759fa-196">To import the Commerce Preview Demo Base Extension into your project, follow these steps.</span></span>

1. <span data-ttu-id="759fa-197">En üstte proje adını seçerek projenizin giriş sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="759fa-197">Open the home page for your project by selecting the project name at the top.</span></span>
1. <span data-ttu-id="759fa-198">Şu adımlardan birini izleyin:</span><span class="sxs-lookup"><span data-stu-id="759fa-198">Follow one of these steps:</span></span>

    - <span data-ttu-id="759fa-199">Ortak iseniz, en sağdaki **Varlık kitaplığı** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-199">If you're a partner, select the **Asset library** tile on the far right.</span></span>
    - <span data-ttu-id="759fa-200">Müşterisiyseniz, üst menüden **Varlık kitaplığı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-200">If you're a customer, select **Asset library** on the top menu.</span></span>

1. <span data-ttu-id="759fa-201">Soldaki listeden **yazılımla dağıtılabilir paket**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-201">In the list on the left, select **Software deployable package**.</span></span>
1. <span data-ttu-id="759fa-202">**İçe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-202">Select **Import**.</span></span>
1. <span data-ttu-id="759fa-203">**Paylaşılan varlık kitaplığı**'nın altındaki kıymetler listesinden **Commerce önizleme demo temel uzantıyı** seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-203">Under **Shared asset library**, select **Commerce Preview Demo Base Extension** in the list of assets.</span></span>
1. <span data-ttu-id="759fa-204">**Çek**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-204">Select **Pick**.</span></span> <span data-ttu-id="759fa-205">Varlık kitaplığına iade edilecek ve listede uzantıyı görmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="759fa-205">You're returned to the Asset library, and you should see the extension in the list.</span></span>

<span data-ttu-id="759fa-206">Aşağıdaki şekilde, LCS **varlık Kitaplığı** sayfasında yapılması gereken eylemler gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="759fa-206">The following illustration shows the actions that must be taken on the LCS **Asset library** page.</span></span>

![Commerce önizleme demo temel uzantısını içe aktarma](./media/import.png)

### <a name="deploy-the-environment"></a><span data-ttu-id="759fa-208">Ortamı dağıtın</span><span class="sxs-lookup"><span data-stu-id="759fa-208">Deploy the environment</span></span>

<span data-ttu-id="759fa-209">Ortamı dağıtmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="759fa-209">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="759fa-210">Tek bir seçeneği olan sayfalar atlandığından 6., 7. ve/veya 8. adımı tamamlamanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="759fa-210">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="759fa-211">**Ortam parametreleri** görünümünde olduğunuzda, **ortam adı** alanının metin **Dynamics 365 Commerce-demo (*xx\* platform güncelleştirmesi 10.0.* x)\*\* ile doğrudan göründüğünü onaylayın.</span><span class="sxs-lookup"><span data-stu-id="759fa-211">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="759fa-212">Ayrıntılar için, 8. adımdan sonra görünen çizime bakın.</span><span class="sxs-lookup"><span data-stu-id="759fa-212">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="759fa-213">Üst menüden **bulut ile barındırılan ortamları** seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-213">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="759fa-214">Ortam eklemek için **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="759fa-214">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="759fa-215">**Uygulama sürümü** alanında, en güncel sürümü seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-215">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="759fa-216">En güncel sürümden farklı bir uygulama sürümünü seçmeniz için özel bir gereksinim duyuyorsanız, **10.0.8** önceki bir sürümü seçmeyin.</span><span class="sxs-lookup"><span data-stu-id="759fa-216">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.8**.</span></span>
1. <span data-ttu-id="759fa-217">**Platform sürümü** alanında, seçtiğiniz uygulama sürümü için otomatik olarak seçilen platform sürümünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="759fa-217">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![Uygulamayı ve platform sürümünü seçme](./media/project1.png)

1. <span data-ttu-id="759fa-219">**Sonraki**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-219">Select **Next**.</span></span>
1. <span data-ttu-id="759fa-220">Ortam topolojisi olarak **Demo**'yu seçinç</span><span class="sxs-lookup"><span data-stu-id="759fa-220">Select **Demo** as the environment topology.</span></span>

    ![Ortam topolojisini 1 seçme](./media/project2.png)

1. <span data-ttu-id="759fa-222">Ortam topolojisi olarak **Dynamics 365 Commerce - Demo**'yu seçinç</span><span class="sxs-lookup"><span data-stu-id="759fa-222">Select **Dynamics 365 Commerce - Demo** as the environment topology.</span></span> <span data-ttu-id="759fa-223">Daha önce tek bir Azure Bağlayıcısı yapılandırdıysanız bu ortam için kullanılacak.</span><span class="sxs-lookup"><span data-stu-id="759fa-223">If you configured a single Azure Connector earlier, it will be used for this environment.</span></span> <span data-ttu-id="759fa-224">Birden fazla Azure Bağlayıcısı konfigüre ediyorsanız, hangi bağlayıcının kullanılacağını seçebilirsiniz: **Doğu ABD**, **Doğu ABD 2**, **Batı ABD** veya **Batı ABD 2**.</span><span class="sxs-lookup"><span data-stu-id="759fa-224">If you configured multiple Azure Connectors, you can select which connector to use: **East US**, **East US 2**, **West US**, or **West US 2**.</span></span> <span data-ttu-id="759fa-225">(En iyi uçtan uca performans için, **Batı ABD 2**'yi seçmeniz önerilir.)</span><span class="sxs-lookup"><span data-stu-id="759fa-225">(For the best end-to-end performance, we recommend that you select **West US 2**.)</span></span>

    ![Ortam topolojisini 2 seçme](./media/project3.png)

1. <span data-ttu-id="759fa-227">**Ortam dağıt** sayfasında bir ortam adı girin.</span><span class="sxs-lookup"><span data-stu-id="759fa-227">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="759fa-228">Gelişmiş ayarları olduğu gibi bırakın.</span><span class="sxs-lookup"><span data-stu-id="759fa-228">Leave the advanced settings as they are.</span></span>

    ![Ortamı dağıtın sayfası](./media/project4.png)

1. <span data-ttu-id="759fa-230">VM boyutunu gerektiği gibi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="759fa-230">Adjust the VM size as required.</span></span> <span data-ttu-id="759fa-231">(VM stok tutma birimi \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="759fa-231">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="759fa-232">Fiyat ve lisans koşullarını gözden geçirin ve kabul ettiğiniz onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="759fa-232">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="759fa-233">**Sonraki**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-233">Select **Next**.</span></span>
1. <span data-ttu-id="759fa-234">Dağıtım onayı sayfasında, ayrıntıların doğru olduğunu doğruladıktan sonra **Dağıt**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-234">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="759fa-235">**Bulut içinde barındırılan ortamlar** görünümüne geri dönersiniz ve ortamınız listede görünmelidir.</span><span class="sxs-lookup"><span data-stu-id="759fa-235">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="759fa-236">İstediğiniz ortam kuyruğa alındı ve sonra dağıtılıyor.</span><span class="sxs-lookup"><span data-stu-id="759fa-236">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="759fa-237">Ortam iş akışlarının tamamlanması biraz zaman alır.</span><span class="sxs-lookup"><span data-stu-id="759fa-237">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="759fa-238">Bu nedenle, yaklaşık altı ile dokuz saatten sonra yeniden kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="759fa-238">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="759fa-239">Devam etmeden önce, ortam durumlarınızın **dağıtıldığından** emin olun.</span><span class="sxs-lookup"><span data-stu-id="759fa-239">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-csu"></a><span data-ttu-id="759fa-240">Commerce scale unit (CSU) Başlat</span><span class="sxs-lookup"><span data-stu-id="759fa-240">Initialize the commerce scale unit (CSU)</span></span>

<span data-ttu-id="759fa-241">Bir CSU başlatmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="759fa-241">To initialize CSU, follow these steps.</span></span>

1. <span data-ttu-id="759fa-242">**Bulut barındırılan ortamlar** görünümünde, listeden ortamınızı seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-242">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="759fa-243">Sağdaki ortam görünümünde **tam ayrıntılar** 'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="759fa-243">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="759fa-244">Ortam ayrıntıları görünümü görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="759fa-244">The environment details view appears.</span></span>
1. <span data-ttu-id="759fa-245">**Ortam özellikleri** altında, **Yönet**'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="759fa-245">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="759fa-246">**Commerce** sekmesinde, **Başlat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-246">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="759fa-247">CSU başlatma parametreleri görünümü görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="759fa-247">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="759fa-248">**Bölge** alanında, **Doğu ABD**, **Doğu ABD 2**, **Batı ABD** veya **Batı ABD 2** seçeneklerinden birini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="759fa-248">In the **Region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="759fa-249">**Sürüm** alanında, listeden bir **sürüm belirtin** ve sonra görüntülenen alanda **9.18.20014.4** belirtin.</span><span class="sxs-lookup"><span data-stu-id="759fa-249">In the **Version** field, select **Specify a version** in the list, and then specify **9.18.20014.4** in the field that appears.</span></span> <span data-ttu-id="759fa-250">Burada belirtilen sürümü tam olarak belirttiğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="759fa-250">Be sure to specify the exact version that is indicated here.</span></span> <span data-ttu-id="759fa-251">Aksi durumda, RCSU öğesini daha sonra doğru sürüme güncelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="759fa-251">Otherwise, you will have to update RCSU to the correct version later.</span></span>
1. <span data-ttu-id="759fa-252">**Uzantıyı Uygula** seçeneğini açın.</span><span class="sxs-lookup"><span data-stu-id="759fa-252">Turn on the **Apply extension** option.</span></span>
1. <span data-ttu-id="759fa-253">Uzantılar listesinden, **Commerce Önizleme demo temel uzantısını** seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-253">In the list of extensions, select **Commerce Preview Demo Base Extension**.</span></span>
1. <span data-ttu-id="759fa-254">**Başlat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-254">Select **Initialize**.</span></span>
1. <span data-ttu-id="759fa-255">Dağıtım onayı sayfasında, ayrıntıların doğru olduğunu doğruladıktan sonra **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-255">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="759fa-256">**Ticaret yönetimi** görünümü, **Commerce** sekmesinin seçildiği yerde tekrar görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="759fa-256">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="759fa-257">CSU kaynak ayırma işlemi için sıraya alındı.</span><span class="sxs-lookup"><span data-stu-id="759fa-257">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="759fa-258">Devam etmeden önce, CSU durumlarınız **Başarılı** olur.</span><span class="sxs-lookup"><span data-stu-id="759fa-258">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="759fa-259">Başlatma yaklaşık iki ile beş saat arasında sürer.</span><span class="sxs-lookup"><span data-stu-id="759fa-259">Initialization takes approximately two to five hours.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="759fa-260">e-Ticaret başlat</span><span class="sxs-lookup"><span data-stu-id="759fa-260">Initialize e-Commerce</span></span>

<span data-ttu-id="759fa-261">Bir e-Ticaret başlatmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="759fa-261">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="759fa-262">**E-ticaret** sekmesinde, önizleme onayını gözden geçirip **kurulum**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-262">On the **e-Commerce** tab, review the preview consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="759fa-263">**E-ticaret kiracı adı** için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="759fa-263">In the **e-Commerce tenant name** field, enter a name.</span></span> <span data-ttu-id="759fa-264">Ancak, e-ticaret örneğinizi gösteren bazı URL'lerde bu dosyanın görülebileceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="759fa-264">However, be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="759fa-265">**Commerce Scale Unit adı** alanında, listesindeki CSU alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-265">In the **Commerce scale unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="759fa-266">(Listede yalnızca bir seçenek bulunmalıdır.)</span><span class="sxs-lookup"><span data-stu-id="759fa-266">(The list should have only one option.)</span></span>

    <span data-ttu-id="759fa-267">**E-ticaret coğrafyası** alanı otomatik olarak ayarlanır ve değer değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="759fa-267">The **e-Commerce geography** field is set automatically, and the value can't be changed.</span></span>

1. <span data-ttu-id="759fa-268">Devam etmek için **İleri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-268">Select **Next** to continue.</span></span>
1. <span data-ttu-id="759fa-269">**Desteklenen ana bilgisayar adları** alanında, `www.fabrikam.com` gibi geçerli herhangi bir etki alanını girin.</span><span class="sxs-lookup"><span data-stu-id="759fa-269">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1.  <span data-ttu-id="759fa-270">**Sistem Yöneticisi için AAD güvenlik grubunda** alanına, kullanmak istediğiniz güvenlik grubunun adının ilk birkaç harfini girin.</span><span class="sxs-lookup"><span data-stu-id="759fa-270">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="759fa-271">Arama sonuçlarını görüntülemek için büyüteç simgesini seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-271">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="759fa-272">Listeden doğru bir güvenlik grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-272">Select the correct security group from the list.</span></span>
2.  <span data-ttu-id="759fa-273">**Derecelendirme ve inceleme moderatörü için AAD güvenlik grubunda** alanına, kullanmak istediğiniz güvenlik grubunun adının ilk birkaç harfini girin.</span><span class="sxs-lookup"><span data-stu-id="759fa-273">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="759fa-274">Arama sonuçlarını görüntülemek için büyüteç simgesini seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-274">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="759fa-275">Listeden doğru bir güvenlik grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-275">Select the correct security group from the list.</span></span>
1. <span data-ttu-id="759fa-276">**Derecelendirmeleri etkinleştir ve gözden geçirme hizmeti** seçeneğini açık olarak bırakın.</span><span class="sxs-lookup"><span data-stu-id="759fa-276">Leave the **Enable ratings and review service** option turned on.</span></span>
1. <span data-ttu-id="759fa-277">**Başlat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="759fa-277">Select **Initialize**.</span></span> <span data-ttu-id="759fa-278">**Ticaret yönetimi** görünümü, **e-Commerce** sekmesinin seçildiği yerde tekrar görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="759fa-278">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="759fa-279">E-ticaret başlatma işlemi başlatıldı.</span><span class="sxs-lookup"><span data-stu-id="759fa-279">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="759fa-280">Devam etmeden önce, e-ticaret başlatma durumunuz **başlatma başarılı** olana kadar bekleyin.</span><span class="sxs-lookup"><span data-stu-id="759fa-280">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="759fa-281">Alt sağdaki **bağlantılar** altında, aşağıdaki bağlantıların URL 'lerini not alın:</span><span class="sxs-lookup"><span data-stu-id="759fa-281">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="759fa-282">**e-ticaret sitesi** – E-ticaret sitenizin köküne olan bağlantı.</span><span class="sxs-lookup"><span data-stu-id="759fa-282">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="759fa-283">**e-ticaret site yönetimi aracı** – site yönetimi aracına bağlantı.</span><span class="sxs-lookup"><span data-stu-id="759fa-283">**e-Commerce site management tool** – The link to the site management tool.</span></span>

## <a name="commerce-preview-environment-support"></a><span data-ttu-id="759fa-284">Commerce önizleme ortamı desteği</span><span class="sxs-lookup"><span data-stu-id="759fa-284">Commerce preview environment support</span></span>

<span data-ttu-id="759fa-285">Sağlama adımlarını gerçekleştirirken sorunlarla karşılaşırsanız, yardım için lütfen [Microsoft Dynamics 365 Commerce Önizleme Yammer grubunu](https://aka.ms/Dynamics365CommercePreviewYammer) ziyaret edin.</span><span class="sxs-lookup"><span data-stu-id="759fa-285">If you experience issues while you're completing the provisioning steps, visit the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer) for help.</span></span>

<span data-ttu-id="759fa-286">Yammer Gruba erişmeye çalıştığınızda sorunlarla karşılaşırsanız, Microsoft'a e-posta ile başvurabilirsiniz:  <Dynamics365Commerce@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="759fa-286">If you experience issues when you try to access the Yammer group, you can contact Microsoft by email at <Dynamics365Commerce@microsoft.com>.</span></span> <span data-ttu-id="759fa-287">Bu e-posta adresi etkin şekilde izlenmiyor.</span><span class="sxs-lookup"><span data-stu-id="759fa-287">This email address isn't actively monitored.</span></span> <span data-ttu-id="759fa-288">Bu nedenle, yanıtta bir gecikme olmasını bekler.</span><span class="sxs-lookup"><span data-stu-id="759fa-288">Therefore, expect a delay in the response.</span></span>

## <a name="next-steps"></a><span data-ttu-id="759fa-289">Sonraki adımlar</span><span class="sxs-lookup"><span data-stu-id="759fa-289">Next steps</span></span>

<span data-ttu-id="759fa-290">Commerce önizleme ortamını hazırlam ve yapılandırma işlemine devam etmek için bkz. [Commerce önizleme ortamı yapılandırma](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="759fa-290">To continue the process of provisioning and configuring your Commerce preview environment, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="759fa-291">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="759fa-291">Additional resources</span></span>

[<span data-ttu-id="759fa-292">Dynamics 365 Commerce önizleme ortamına genel bakış</span><span class="sxs-lookup"><span data-stu-id="759fa-292">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="759fa-293">Dynamics 365 Commerce önizleme ortamını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="759fa-293">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="759fa-294">Dynamics 365 Commerce önizleme ortamı için isteğe bağlı özellikleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="759fa-294">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="759fa-295">Dynamics 365 Commerce önizleme ortamıyla ilgili SSS</span><span class="sxs-lookup"><span data-stu-id="759fa-295">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="759fa-296">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="759fa-296">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="759fa-297">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="759fa-297">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="759fa-298">Microsoft Azure portalı</span><span class="sxs-lookup"><span data-stu-id="759fa-298">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="759fa-299">Dynamics 365 Commerce web sitesi</span><span class="sxs-lookup"><span data-stu-id="759fa-299">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

