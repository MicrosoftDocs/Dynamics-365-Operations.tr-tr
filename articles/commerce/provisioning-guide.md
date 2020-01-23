---
title: Commerce önizleme ortamı sağlama
description: Bu konu, hazırlandıktan sonra Microsoft Dynamics 365 Commerce önizleme ortamının nasıl yapılandırılacağını açıklamaktadır.
author: psimolin
manager: annbe
ms.date: 01/06/2020
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
ms.openlocfilehash: b77d2cbbc100aeae5dcd53ddbe69ff2e4435da13
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934760"
---
# <a name="provision-a-commerce-preview-environment"></a><span data-ttu-id="ceb08-103">Commerce önizleme ortamı sağlama</span><span class="sxs-lookup"><span data-stu-id="ceb08-103">Provision a Commerce preview environment</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="ceb08-104">Bu konu, hazırlandıktan sonra Microsoft Dynamics 365 Commerce önizleme ortamının nasıl yapılandırılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="ceb08-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce preview environment.</span></span>

<span data-ttu-id="ceb08-105">Başlamadan önce, işlemin ne olduğunu ve konunun neler içerdiğini öğrenmek için belgeleri en azından bir fikir almak için inclemeenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="ceb08-105">Before you begin, we recommend that you at least skim through this whole topic to get an idea of what the process entails and what this topic contains.</span></span>

> [!NOTE]
> <span data-ttu-id="ceb08-106">Dynamics 365 Commerce önizleme'ye erişim izni verilmemişse, [Commerce Web sitesinden](https://aka.ms/Dynamics365CommerceWebsite) önizleme erişimi isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ceb08-106">If you haven't yet been granted access to the Dynamics 365 Commerce preview, you can request preview access from the [Commerce website](https://aka.ms/Dynamics365CommerceWebsite).</span></span>

## <a name="overview"></a><span data-ttu-id="ceb08-107">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="ceb08-107">Overview</span></span>

<span data-ttu-id="ceb08-108">Commerce önizleme ortamınızı başarıyla sağlamak için, belirli bir ürün adı ve türü olan bir proje oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ceb08-108">To successfully provision your Commerce preview environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="ceb08-109">Ortam ve Retail Cloud Scale Unit (RCSU), ayrıca, e-ticaret sağlamasının daha sonra başlatmak için kullanmanız gereken belirli parametreleri de vardır.</span><span class="sxs-lookup"><span data-stu-id="ceb08-109">The environment and Retail Cloud Scale Unit (RCSU) also have some specific parameters that you must use when you provision e-Commerce later.</span></span> <span data-ttu-id="ceb08-110">Bu konudaki yönergeler, tamamlamanız gereken tüm gerekli adımları ve kullanmanız gereken parametreleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="ceb08-110">The instructions in this topic describe all the required steps that you must complete and the parameters that you must use.</span></span>

<span data-ttu-id="ceb08-111">Sağlama başarılı olduktan sonra, Ticari önizleme ortamınızı hazırlamak için almanız gereken birkaç son işlem adımı vardır.</span><span class="sxs-lookup"><span data-stu-id="ceb08-111">After you successfully provision your Commerce preview environment, you must complete a few post-provisioning steps to prepare it.</span></span> <span data-ttu-id="ceb08-112">Sistemin hangi yönlere göre değerlendirileceğini bağlı olarak bazı adımlar isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="ceb08-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="ceb08-113">İsteğe bağlı adımları istediğiniz zaman daha sonra da tamamlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ceb08-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="ceb08-114">Commerce önizleme ortamını yapılandırma hakkında bilgi için bkz. [Commerce önizleme ortamı yapılandırma](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="ceb08-114">For information about how to configure your Commerce preview environment after you provision it, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="ceb08-115">Commerce Preview ortamınızla ilgili isteğe bağlı özellikleri konfigüre etmek için, bkz. [Commerce önizleme ortamınız için isteğe bağlı özellikler yapılandırın](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="ceb08-115">For information about how to configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

<span data-ttu-id="ceb08-116">Sağlama adımlarıyla ilgili sorularınız varsa veya herhangi bir sorunla karşılaşırsanız, lütfen [Microsoft Dynamics 365 Commerce önizleme Yammer grubunda](https://aka.ms/Dynamics365CommercePreviewYammer) Microsoft'a bildirin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-116">If you have any questions about the provisioning steps, or if you encounter any issues, let Microsoft know in the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ceb08-117">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="ceb08-117">Prerequisites</span></span>

<span data-ttu-id="ceb08-118">Commerce önizleme ortamınızı hazırlayabilmeniz için aşağıdaki önkoşulların yerinde olması gerekir:</span><span class="sxs-lookup"><span data-stu-id="ceb08-118">The following prerequisites must be in place before you can provision your Commerce preview environment:</span></span>

- <span data-ttu-id="ceb08-119">Microsoft Dynamics Lifecycle Services (LCS) portalına erişim hakkınız var</span><span class="sxs-lookup"><span data-stu-id="ceb08-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="ceb08-120">Dynamics 365 Commerce Önizleme programına kabul edilmiş olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ceb08-120">You've been accepted into the Dynamics 365 Commerce Preview program.</span></span>
- <span data-ttu-id="ceb08-121">**Olası ön satışlar** için bir proje oluşturmak veya **geçiş yapmak, çözüm oluşturmak ve daha fazla bilgi** edinmek için gerekli izinleriniz vardır.</span><span class="sxs-lookup"><span data-stu-id="ceb08-121">You have the required permissions to create a project for **Prospective presales** or **Migrate, create solutions, and learn**.</span></span>
- <span data-ttu-id="ceb08-122">Ortamı sağlamak istediğiniz **Ortam yöneticisi** veya **Proje sahibi** rolünün bir üyesisinizdir.</span><span class="sxs-lookup"><span data-stu-id="ceb08-122">You're a member of the **Environment manager** or **Project owner** role in the project where you will provision the environment.</span></span>
- <span data-ttu-id="ceb08-123">Microsoft Azure aboneliğinize yönetici erişiminiz var veya sizin adınıza yönetici izinleri gerektiren iki adımı gerçekleştirebilecek bir abonelik Yöneticisi ile ilişki kurun.</span><span class="sxs-lookup"><span data-stu-id="ceb08-123">You have admin access to your Microsoft Azure subscription, or you're in contact with a subscription admin who can complete the two steps that require admin permissions on your behalf.</span></span>
- <span data-ttu-id="ceb08-124">Azure Active Directory (Azure AD) kiracı kimliğiniz kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ceb08-124">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="ceb08-125">E-ticaret sistem yöneticileri grubu olarak kullanılacak bir Azure AD güvenlik grubu oluşturdunuz ve kimliğiniz kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="ceb08-125">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="ceb08-126">Derecelendirme ve incelemeler grubu olarak kullanılacak bir Azure AD güvenlik grubu oluşturdunuz ve kimliğiniz kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="ceb08-126">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="ceb08-127">(Bu güvenlik grubu e-ticaret Sistem Yöneticisi grubuyla aynı olabilir.)</span><span class="sxs-lookup"><span data-stu-id="ceb08-127">(This security group can be the same as the e-Commerce system admin group.)</span></span>

### <a name="find-your-azure-ad-tenant-id"></a><span data-ttu-id="ceb08-128">Azure AD kiracı kimliğinizi bulun</span><span class="sxs-lookup"><span data-stu-id="ceb08-128">Find your Azure AD tenant ID</span></span>

<span data-ttu-id="ceb08-129">Azure AD kiracı kimliğiniz, bu örneğe benzeyen bir genel benzersiz tanımlayıcıdır (GUID): **72f988bf-86f1-41af-91ab-2d7cd011db47**.</span><span class="sxs-lookup"><span data-stu-id="ceb08-129">Your Azure AD tenant ID is a globally unique identifier (GUID) that resembles this example: **72f988bf-86f1-41af-91ab-2d7cd011db47**.</span></span>

#### <a name="find-your-azure-ad-tenant-id-by-using-the-azure-portal"></a><span data-ttu-id="ceb08-130">Azure portalını kullanarak Azure AD kiracı kimliğinizi bulun</span><span class="sxs-lookup"><span data-stu-id="ceb08-130">Find your Azure AD tenant ID by using the Azure portal</span></span>

1. <span data-ttu-id="ceb08-131">[Azure portalında](https://portal.azure.com/) adresinden oturum açın.</span><span class="sxs-lookup"><span data-stu-id="ceb08-131">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="ceb08-132">Doğru dizin seçimi yaptığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="ceb08-132">Make sure that the correct directory is selected.</span></span>
1. <span data-ttu-id="ceb08-133">Soldaki menüden **Azure Active Directory** seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-133">On the menu on the left, select **Azure Active Directory**.</span></span>
1. <span data-ttu-id="ceb08-134">**Yönet** altında **Özellikler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-134">Under **Manage**, select **Properties**.</span></span> <span data-ttu-id="ceb08-135">Azure AD kiracı kimliğiniz **dizin kimliği** altında görünür.</span><span class="sxs-lookup"><span data-stu-id="ceb08-135">Your Azure AD tenant ID appears under **Directory ID**.</span></span>

#### <a name="find-your-azure-ad-tenant-id-by-using-openid-connect-metadata"></a><span data-ttu-id="ceb08-136">OpenID bağlantı meta verilerini kullanarak Azure AD kiracı kimliğinizi bulun</span><span class="sxs-lookup"><span data-stu-id="ceb08-136">Find your Azure AD tenant ID by using OpenID Connect metadata</span></span>

<span data-ttu-id="ceb08-137">Etki alanınızı `microsoft.com` gibi **\{ETKİ\_ALANI\}** ile değiştirerek bir OpenID URL'si oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ceb08-137">Create an OpenID URL by replacing **\{YOUR\_DOMAIN\}** with your domain, such as `microsoft.com`.</span></span> <span data-ttu-id="ceb08-138">Örneğin, `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration`, `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration` olur.</span><span class="sxs-lookup"><span data-stu-id="ceb08-138">For example, `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` will become `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`.</span></span>

1. <span data-ttu-id="ceb08-139">Etki alanınızı içeren OpenID URL'sine gidin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-139">Go to the OpenID URL that contains your domain.</span></span>

    <span data-ttu-id="ceb08-140">Azure AD kiracı kimliğinizi birden çok özellik değerlerinde bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ceb08-140">You can find you Azure AD tenant ID in multiple property values.</span></span>

1. <span data-ttu-id="ceb08-141">**yetkilendirme\_bitişnoktası**'nı bulun, hemen `login.microsoftonline.com/` sonrasında görünen GUID'i çıkarın.</span><span class="sxs-lookup"><span data-stu-id="ceb08-141">Find **authorization\_endpoint**, and extract the GUID that appears immediately after `login.microsoftonline.com/`.</span></span>

### <a name="find-your-azure-ad-security-group-id"></a><span data-ttu-id="ceb08-142">Azure AD güvenlik grubu kimliğinizi bulun</span><span class="sxs-lookup"><span data-stu-id="ceb08-142">Find your Azure AD security group ID</span></span>

<span data-ttu-id="ceb08-143">Azure AD güvenlik grubunuzun kodu aşağıdaki örneğe benzer bir GUID'dir: **436ea7f5-ee6c-40c1-9f08-825c5811066a**.</span><span class="sxs-lookup"><span data-stu-id="ceb08-143">The ID of your Azure AD security group is a GUID that resembles this example: **436ea7f5-ee6c-40c1-9f08-825c5811066a**.</span></span>

<span data-ttu-id="ceb08-144">Bu yordam, kimliğini bulmaya çalıştığınız grubun bir üyesi olduğunuzu varsayar.</span><span class="sxs-lookup"><span data-stu-id="ceb08-144">This procedure assumes that you're a member of the group that you're trying to find the ID for.</span></span>

1. <span data-ttu-id="ceb08-145">[Grafik Gezginini](https://developer.microsoft.com/graph/graph-explorer#) açın.</span><span class="sxs-lookup"><span data-stu-id="ceb08-145">Open the [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer#).</span></span>
1. <span data-ttu-id="ceb08-146">**Microsoft ile oturum aç**'ı tıklatın ve kimlik bilgilerinizi kullanarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="ceb08-146">Select **Sign In with Microsoft**, and sign in by using your credentials.</span></span>
1. <span data-ttu-id="ceb08-147">Solda, **diğer örnekleri göster**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-147">On the left, select **show more samples**.</span></span>
1. <span data-ttu-id="ceb08-148">**Grupları** sağ bölmeden etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-148">In the right pane, enable **Groups**.</span></span>
1. <span data-ttu-id="ceb08-149">Sağ bölmeyi kapatın.</span><span class="sxs-lookup"><span data-stu-id="ceb08-149">Close the right pane.</span></span>
1. <span data-ttu-id="ceb08-150">**Ait olduğum tüm grupları** seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-150">Select **all groups I belong to**.</span></span>
1. <span data-ttu-id="ceb08-151">**Yanıt Önizleme** alanında, grubunu bulun.</span><span class="sxs-lookup"><span data-stu-id="ceb08-151">In the **Response Preview** field, find your group.</span></span> <span data-ttu-id="ceb08-152">Güvenlik grubu kodu, **ID** özelliği altında görünür.</span><span class="sxs-lookup"><span data-stu-id="ceb08-152">The security group ID appears under the **id** property.</span></span>

## <a name="provision-your-commerce-preview-environment"></a><span data-ttu-id="ceb08-153">Commerce önizleme ortamınızı sağlama</span><span class="sxs-lookup"><span data-stu-id="ceb08-153">Provision your Commerce preview environment</span></span>

<span data-ttu-id="ceb08-154">Bu yöntemlerde, bir Commerce Preview ortamının nasıl sağlanacağı açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="ceb08-154">These procedures explain how to provision a Commerce preview environment.</span></span> <span data-ttu-id="ceb08-155">Bunları başarıyla tamamladıktan sonra, Commerce Preview ortamı konfigürasyon için hazır olacak.</span><span class="sxs-lookup"><span data-stu-id="ceb08-155">After you successfully complete them, the Commerce preview environment will be ready for configuration.</span></span> <span data-ttu-id="ceb08-156">Burada açıklanan tüm etkinlikler LCS portalında yer alabilir.</span><span class="sxs-lookup"><span data-stu-id="ceb08-156">All the activities that are described here occur in the LCS portal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ceb08-157">Önizleme erişimi, önizleme uygulamanızda belirttiğiniz LCS hesabına ve kuruluşa bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="ceb08-157">Preview access is tied to the LCS account and organization that you specified in your preview application.</span></span> <span data-ttu-id="ceb08-158">Commerce Preview ortamını sağlamak için aynı hesabı kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ceb08-158">You must use the same account to provision the Commerce preview environment.</span></span> <span data-ttu-id="ceb08-159">Commerce Preview ortamı için farklı bir LCS hesabı veya kiracı kullanmanız gerekiyorsa, bu ayrıntıları Microsoft'a sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ceb08-159">If you must use a different LCS account or tenant for the Commerce preview environment, you must provide those details to Microsoft.</span></span> <span data-ttu-id="ceb08-160">Başvuru bilgileri için bu konudaki [Commerce önizleme ortam desteği](#commerce-preview-environment-support) başlıklı bölüme bakın.</span><span class="sxs-lookup"><span data-stu-id="ceb08-160">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section later in this topic.</span></span>

### <a name="grant-access-to-e-commerce-applications"></a><span data-ttu-id="ceb08-161">E-ticaret uygulamalarına erişim ver</span><span class="sxs-lookup"><span data-stu-id="ceb08-161">Grant access to e-Commerce applications</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ceb08-162">Oturum açan kişinin Azure AD kiracı kimliğine sahip bir Azure AD kiracı yöneticisi olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="ceb08-162">The person who signs in must be an Azure AD tenant admin who has the Azure AD tenant ID.</span></span> <span data-ttu-id="ceb08-163">Bu adım başarılı bir şekilde tamamlanmazsa, kalan sağlama adımları başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="ceb08-163">If this step isn't successfully completed, the remaining provisioning steps will fail.</span></span>

<span data-ttu-id="ceb08-164">E-ticaret uygulamalarına Azure aboneliğinize erişim yetkisi vermek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-164">To authorize e-Commerce applications to access your Azure subscription, follow these steps.</span></span>

1. <span data-ttu-id="ceb08-165">URL'yi aşağıdaki biçimde birleştirin:</span><span class="sxs-lookup"><span data-stu-id="ceb08-165">Assemble a URL in the following format:</span></span>

    `https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345`

1. <span data-ttu-id="ceb08-166">URL'yi kopyalayıp tarayıcınıza veya metin düzenleyicisine yapıştırın ve **\{AAD\_KİRACI\_KİMLİĞİ\}** Azure AD kiracı kimliğiniz ile değiştirin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-166">Copy and paste the URL into your browser or text editor, and replace **\{AAD\_TENANT\_ID\}** with your Azure AD tenant ID.</span></span> <span data-ttu-id="ceb08-167">URL'yi açın.</span><span class="sxs-lookup"><span data-stu-id="ceb08-167">Then open the URL.</span></span>
1. <span data-ttu-id="ceb08-168">Azure AD oturum aç iletişim kutusunda oturum açın ve aboneliğinize **Dynamics 365 Commerce** erişimi vermek istediğinizi doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="ceb08-168">In the Azure AD sign-in dialog box, sign in, and confirm that you want to grant **Dynamics 365 Commerce (Preview)** access to your subscription.</span></span> <span data-ttu-id="ceb08-169">İşlemin başarılı olduğunu gösteren bir sayfaya gönderilecektir.</span><span class="sxs-lookup"><span data-stu-id="ceb08-169">You're redirected to a page that indicates whether the operation was successful.</span></span>

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a><span data-ttu-id="ceb08-170">Önizleme özelliklerinin kullanılabilir ve LCS'de açık olduğunu onaylayın</span><span class="sxs-lookup"><span data-stu-id="ceb08-170">Confirm that preview features are available and turned on in LCS</span></span>

<span data-ttu-id="ceb08-171">Önizleme özelliklerinin kullanılabilir ve LCS'de açık olduğunu onaylamak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-171">To confirm that preview features are available and turned on in LCS, follow these steps.</span></span>

1. <span data-ttu-id="ceb08-172">Bu önizlemeye erişim istemek için kullandığınız LCS hesabını kullanarak [LCS portalında](https://lcs.dynamics.com) oturum açın.</span><span class="sxs-lookup"><span data-stu-id="ceb08-172">Sign in to the [LCS portal](https://lcs.dynamics.com) by using the same LCS account that you used to request access to the preview.</span></span>
1. <span data-ttu-id="ceb08-173">LCS ana sayfasında, tüm yolu sağa kaydırın ve **önizleme özelliği yönetim** kutucuğunu tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ceb08-173">On the LCS home page, scroll all the way to the right, and select the **Preview feature management** tile.</span></span>

    ![Önizleme yönetimi kutucuğu](./media/preview1.png)

1. <span data-ttu-id="ceb08-175">**ÖZEL ÖNİZLEME ÖZELLİKLERİ**'ne gidin ve aşağıdaki özelliklerin kullanılabilir ve açık olduğundan emin olun:</span><span class="sxs-lookup"><span data-stu-id="ceb08-175">Scroll down to **Private preview features**, and confirm that the following features are available and turned on:</span></span>

    - <span data-ttu-id="ceb08-176">e-Ticaret değerlendirmesi</span><span class="sxs-lookup"><span data-stu-id="ceb08-176">e-Commerce Evaluation</span></span>
    - <span data-ttu-id="ceb08-177">Ticaret Önizleme Programı Ortamları</span><span class="sxs-lookup"><span data-stu-id="ceb08-177">Commerce Preview Program Environments</span></span>

    ![Özel önizleme özellikleri](./media/preview2.png)

1. <span data-ttu-id="ceb08-179">Listede bu özellikler görüntülenmiyorsa, Microsoft'a başvurun ve iş e-posta adresiniz, LCS hesabı ve kiracı ayrıntılarını sağlayın.</span><span class="sxs-lookup"><span data-stu-id="ceb08-179">If those features don't appear in the list, contact Microsoft, and provide your work email address, LCS account, and tenant details.</span></span> <span data-ttu-id="ceb08-180">Başvuru bilgileri için [Commerce önizleme ortam desteği](#commerce-preview-environment-support) başlıklı bölüme bakın.</span><span class="sxs-lookup"><span data-stu-id="ceb08-180">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="ceb08-181">Yeni proje oluştur</span><span class="sxs-lookup"><span data-stu-id="ceb08-181">Create a new project</span></span>

<span data-ttu-id="ceb08-182">LCS'de bir yeni proje oluşturmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-182">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="ceb08-183">LCS giriş sayfasında, bir proje oluşturmak için artı işaretini (**+**) seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-183">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="ceb08-184">Sağ bölmede aşağıdaki adımlardan birini izleyin:</span><span class="sxs-lookup"><span data-stu-id="ceb08-184">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="ceb08-185">Bir ortaksanız **taşı, çözüm oluştur ve öğren**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-185">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="ceb08-186">Müşterisiyseniz, **olası ön satışlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-186">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="ceb08-187">Şablon adı, açıklama ve sektör girin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-187">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="ceb08-188">**Ürün adı** alanından **Dynamics 365 Retail** seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-188">In the **Product name** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="ceb08-189">**Ürün sürümü** alanından **Dynamics 365 Retail** seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-189">In the **Product version** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="ceb08-190">**Metodoloji** alanında **Dynamics Retail uygulama metodoloji**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-190">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="ceb08-191">İsteğe bağlı: Roller ve kullanıcılar mevcut projeden içeri aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ceb08-191">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="ceb08-192">**Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-192">Select **Create**.</span></span> <span data-ttu-id="ceb08-193">Proje görünümü gösterilir.</span><span class="sxs-lookup"><span data-stu-id="ceb08-193">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="ceb08-194">Azure bağlayıcısı ekle</span><span class="sxs-lookup"><span data-stu-id="ceb08-194">Add the Azure Connector</span></span>

<span data-ttu-id="ceb08-195">Bir Azure Connector'ı LCS projenize eklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-195">To add the Azure Connector to your LCS project, follow these steps.</span></span>

1. <span data-ttu-id="ceb08-196">Şu adımlardan birini izleyin:</span><span class="sxs-lookup"><span data-stu-id="ceb08-196">Follow one of these steps:</span></span>

    - <span data-ttu-id="ceb08-197">Ortak iseniz, en sağdaki **proje ayarları** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-197">If you're a partner, select the **Project settings** tile on the far right.</span></span>
    - <span data-ttu-id="ceb08-198">Müşterisiyseniz, üst menüden **proje ayarları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-198">If you're a customer, select **Project settings** on the top menu.</span></span>

1. <span data-ttu-id="ceb08-199">**Azure bağlayıcısı** seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-199">Select **Azure connectors**.</span></span>
1. <span data-ttu-id="ceb08-200">Bir Azure bağlayıcısı eklemek için, **Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ceb08-200">Select **Add** to add the Azure Connector.</span></span>
1. <span data-ttu-id="ceb08-201">Bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-201">Enter a name.</span></span>
1. <span data-ttu-id="ceb08-202">Azure abonelik kimliğinizi girin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-202">Enter your Azure subscription ID.</span></span>
1. <span data-ttu-id="ceb08-203">**Azure Resource Manager (ARM) kullanmak için yapılandırın** seçeneğini açın.</span><span class="sxs-lookup"><span data-stu-id="ceb08-203">Turn on the **Configure to use Azure Resource Manager (ARM)** option.</span></span>
1. <span data-ttu-id="ceb08-204">**Azure aboneliği AAD kiracı etki alanının (veya kimlik)** değerinin doğru olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="ceb08-204">Verify that the **Azure subscription AAD Tenant Domain (or ID)** value is correct.</span></span> <span data-ttu-id="ceb08-205">Gerekiyorsa, Azure abonelik yöneticinize başvurun.</span><span class="sxs-lookup"><span data-stu-id="ceb08-205">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="ceb08-206">**Sonraki**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-206">Select **Next**.</span></span>
1. <span data-ttu-id="ceb08-207">Gerekli uygulamaların aboneliğinize erişim izni vermek için sayfadaki yönergeleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-207">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="ceb08-208">Gerekiyorsa, Azure abonelik yöneticinize başvurun.</span><span class="sxs-lookup"><span data-stu-id="ceb08-208">Consult your Azure subscription admin as required.</span></span>

    1. <span data-ttu-id="ceb08-209">[Azure portalında](https://portal.azure.com/) adresinden oturum açın.</span><span class="sxs-lookup"><span data-stu-id="ceb08-209">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
    1. <span data-ttu-id="ceb08-210">Doğru dizinin seçildiğinden emin olun ve soldaki menüde **Abonelikler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-210">Make sure that the correct directory is selected, and then, on the menu on the left, select **Subscriptions**.</span></span>
    1. <span data-ttu-id="ceb08-211">Listeden doğru aboneliği bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-211">Find the correct subscription in the list, and select it.</span></span> <span data-ttu-id="ceb08-212">Gerektiğinde arama işlevini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ceb08-212">Use the search functionality as required.</span></span>
    1. <span data-ttu-id="ceb08-213">Menüde, **erişim denetimi (IAM)** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-213">On the menu, select **Access control (IAM)**.</span></span>
    1. <span data-ttu-id="ceb08-214">Sağ tarafta **rol ataması eklemek** için **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ceb08-214">On the right, under **Add a role assignment**, select **Add**.</span></span> <span data-ttu-id="ceb08-215">**Role atama ekle** bölmesi görünür.</span><span class="sxs-lookup"><span data-stu-id="ceb08-215">The **Add role assignment** pane appears.</span></span>
    1. <span data-ttu-id="ceb08-216">**Rol** alanında **Katkı sağlayan**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-216">In the **Role** field, select **Contributor**.</span></span>
    1. <span data-ttu-id="ceb08-217">**Erişimi ata** alanında, varsayılan değeri, **Azure AD kullanıcıyı, grubu veya servis sorumlusunu** bırakın.</span><span class="sxs-lookup"><span data-stu-id="ceb08-217">In the **Assign access to** field, leave the default value, **Azure AD user, group, or service principal**.</span></span>
    1. <span data-ttu-id="ceb08-218">**Seç** altında, **b96b7e94-b82e-4e71-99a0-cf7fb188acea** girin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-218">Under **Select**, enter **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span></span>
    1. <span data-ttu-id="ceb08-219">Listeden **Dynamics dağıtım hizmetlerini \[wsfed-etkin\]** seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-219">Select **Dynamics Deployment Services \[wsfed-enabled\]** in the list.</span></span>
    1. <span data-ttu-id="ceb08-220">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-220">Select **Save**.</span></span>

1. <span data-ttu-id="ceb08-221">**Sonraki**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-221">Select **Next**.</span></span>
1. <span data-ttu-id="ceb08-222">Gerekli uygulamaların aboneliğinize erişim izni vermek için sayfadaki yönergeleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-222">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="ceb08-223">Gerekiyorsa, Azure abonelik yöneticinize başvurun.</span><span class="sxs-lookup"><span data-stu-id="ceb08-223">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="ceb08-224">**Sonraki**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-224">Select **Next**.</span></span>
1. <span data-ttu-id="ceb08-225">**Azure bölgesi** alanında, **Doğu ABD**, **Doğu ABD 2**, **Batı ABD** veya **Batı ABD 2** seçeneklerinden birini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-225">In the **Azure region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="ceb08-226">**Bağlan**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-226">Select **Connect**.</span></span> <span data-ttu-id="ceb08-227">Azure Bağlayıcınız listede görünmelidir.</span><span class="sxs-lookup"><span data-stu-id="ceb08-227">Your Azure Connector should appear in the list.</span></span>

### <a name="import-the-commerce-preview-demo-base-extension"></a><span data-ttu-id="ceb08-228">Commerce önizleme demo temel uzantısını içe aktar</span><span class="sxs-lookup"><span data-stu-id="ceb08-228">Import the Commerce Preview Demo Base Extension</span></span>

<span data-ttu-id="ceb08-229">Commerce Önizleme demo temel uzantısını projenize içe aktarmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-229">To import the Commerce Preview Demo Base Extension into your project, follow these steps.</span></span>

1. <span data-ttu-id="ceb08-230">En üstte proje adını seçerek projenizin giriş sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="ceb08-230">Open the home page for your project by selecting the project name at the top.</span></span>
1. <span data-ttu-id="ceb08-231">Şu adımlardan birini izleyin:</span><span class="sxs-lookup"><span data-stu-id="ceb08-231">Follow one of these steps:</span></span>

    - <span data-ttu-id="ceb08-232">Ortak iseniz, en sağdaki **Varlık kitaplığı** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-232">If you're a partner, select the **Asset library** tile on the far right.</span></span>
    - <span data-ttu-id="ceb08-233">Müşterisiyseniz, üst menüden **Varlık kitaplığı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-233">If you're a customer, select **Asset library** on the top menu.</span></span>

1. <span data-ttu-id="ceb08-234">Soldaki listeden **yazılımla dağıtılabilir paket**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-234">In the list on the left, select **Software deployable package**.</span></span>
1. <span data-ttu-id="ceb08-235">**İçe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-235">Select **Import**.</span></span>
1. <span data-ttu-id="ceb08-236">**Paylaşılan varlık kitaplığı**'nın altındaki kıymetler listesinden **Commerce önizleme demo temel uzantıyı** seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-236">Under **Shared asset library**, select **Commerce Preview Demo Base Extension** in the list of assets.</span></span>
1. <span data-ttu-id="ceb08-237">**Çek**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-237">Select **Pick**.</span></span> <span data-ttu-id="ceb08-238">Varlık kitaplığına iade edilecek ve listede uzantıyı görmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="ceb08-238">You're returned to the Asset library, and you should see the extension in the list.</span></span>

<span data-ttu-id="ceb08-239">Aşağıdaki şekilde, LCS **varlık Kitaplığı** sayfasında yapılması gereken eylemler gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="ceb08-239">The following illustration shows the actions that must be taken on the LCS **Asset library** page.</span></span>

![Commerce önizleme demo temel uzantısını içe aktarma](./media/import.png)

### <a name="deploy-the-environment"></a><span data-ttu-id="ceb08-241">Ortamı dağıtın</span><span class="sxs-lookup"><span data-stu-id="ceb08-241">Deploy the environment</span></span>

<span data-ttu-id="ceb08-242">Ortamı dağıtmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-242">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="ceb08-243">Tek bir seçeneği olan sayfalar atlandığından 6., 7. ve/veya 8. adımı tamamlamanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="ceb08-243">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="ceb08-244">**Ortam parametreleri** görünümünde olduğunuzda, **Dynamics 365 Commerce**'in **ortam adı** alanının metin (Önizleme)-demo (30 platform güncelleştirmesi 10.0.6) ile doğrudan göründüğünü onaylayın.</span><span class="sxs-lookup"><span data-stu-id="ceb08-244">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce (Preview) - Demo (10.0.6 with Platform update 30)** appears directly above the **Environment name** field.</span></span> <span data-ttu-id="ceb08-245">8. adımdan sonra görünen çizime bakın.</span><span class="sxs-lookup"><span data-stu-id="ceb08-245">See the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="ceb08-246">Üst menüden **bulut ile barındırılan ortamları** seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-246">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="ceb08-247">Ortam eklemek için **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ceb08-247">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="ceb08-248">**Uygulama sürümü** alanından **10.0.6** seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-248">In the **Application version** field, select **10.0.6**.</span></span>
1. <span data-ttu-id="ceb08-249">**Platform sürümü** alanında **Platform Update 30**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-249">In the **Platform version** field, select **Platform Update 30**.</span></span>

    ![Uygulamayı ve platform sürümünü seçme](./media/project1.png)

1. <span data-ttu-id="ceb08-251">**Sonraki**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-251">Select **Next**.</span></span>
1. <span data-ttu-id="ceb08-252">Ortam topolojisi olarak **Demo**'yu seçinç</span><span class="sxs-lookup"><span data-stu-id="ceb08-252">Select **Demo** as the environment topology.</span></span>

    ![Ortam topolojisini 1 seçme](./media/project2.png)

1. <span data-ttu-id="ceb08-254">Ortam topolojisi olarak **Dynamics 365 Commerce (Önizleme) - Demo**'yu seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-254">Select **Dynamics 365 Commerce (Preview) - Demo** as the environment topology.</span></span> <span data-ttu-id="ceb08-255">Daha önce tek bir Azure Bağlayıcısı yapılandırdıysanız bu ortam için kullanılacak.</span><span class="sxs-lookup"><span data-stu-id="ceb08-255">If you configured a single Azure Connector earlier, it will be used for this environment.</span></span> <span data-ttu-id="ceb08-256">Birden fazla Azure Bağlayıcısı konfigüre ediyorsanız, hangi bağlayıcının kullanılacağını seçebilirsiniz: **Doğu ABD**, **Doğu ABD 2**, **Batı ABD** veya **Batı ABD 2**.</span><span class="sxs-lookup"><span data-stu-id="ceb08-256">If you configured multiple Azure Connectors, you can select which connector to use: **East US**, **East US 2**, **West US**, or **West US 2**.</span></span> <span data-ttu-id="ceb08-257">(En iyi uçtan uca performans için, **Batı ABD 2**'yi seçmeniz önerilir.)</span><span class="sxs-lookup"><span data-stu-id="ceb08-257">(For the best end-to-end performance, we recommend that you select **West US 2**.)</span></span>

    ![Ortam topolojisini 2 seçme](./media/project3.png)

1. <span data-ttu-id="ceb08-259">**Ortam dağıt** sayfasında bir ortam adı girin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-259">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="ceb08-260">Gelişmiş ayarları olduğu gibi bırakın.</span><span class="sxs-lookup"><span data-stu-id="ceb08-260">Leave the advanced settings as they are.</span></span>

    ![Ortamı dağıtın sayfası](./media/project4.png)

1. <span data-ttu-id="ceb08-262">VM boyutunu gerektiği gibi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ceb08-262">Adjust the VM size as required.</span></span> <span data-ttu-id="ceb08-263">(VM stok tutma birimi \[SKU\] **D13 v2**.)</span><span class="sxs-lookup"><span data-stu-id="ceb08-263">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="ceb08-264">Fiyat ve lisans koşullarını gözden geçirin ve kabul ettiğiniz onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-264">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="ceb08-265">**Sonraki**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-265">Select **Next**.</span></span>
1. <span data-ttu-id="ceb08-266">Dağıtım onayı sayfasında, ayrıntıların doğru olduğunu doğruladıktan sonra **Dağıt**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-266">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="ceb08-267">**Bulut içinde barındırılan ortamlar** görünümüne geri dönersiniz ve ortamınız listede görünmelidir.</span><span class="sxs-lookup"><span data-stu-id="ceb08-267">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="ceb08-268">İstediğiniz ortam kuyruğa alındı ve sonra dağıtılıyor.</span><span class="sxs-lookup"><span data-stu-id="ceb08-268">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="ceb08-269">Ortam iş akışlarının tamamlanması biraz zaman alır.</span><span class="sxs-lookup"><span data-stu-id="ceb08-269">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="ceb08-270">Bu nedenle, yaklaşık altı ile dokuz saatten sonra yeniden kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-270">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="ceb08-271">Devam etmeden önce, ortam durumlarınızın **dağıtıldığından** emin olun.</span><span class="sxs-lookup"><span data-stu-id="ceb08-271">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-rcsu"></a><span data-ttu-id="ceb08-272">RCSU başlatma</span><span class="sxs-lookup"><span data-stu-id="ceb08-272">Initialize RCSU</span></span>

<span data-ttu-id="ceb08-273">Bir RCSU başlatmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-273">To initialize RCSU, follow these steps.</span></span>

1. <span data-ttu-id="ceb08-274">**Bulut barındırılan ortamlar** görünümünde, listeden ortamınızı seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-274">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="ceb08-275">Sağdaki ortam görünümünde **tam ayrıntılar** 'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ceb08-275">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="ceb08-276">Ortam ayrıntıları görünümü görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="ceb08-276">The environment details view appears.</span></span>
1. <span data-ttu-id="ceb08-277">**Ortam özellikleri** altında, **Yönet**'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ceb08-277">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="ceb08-278">**Perakende** sekmesinde, **Başlat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-278">On the **Retail** tab, select **Initialize**.</span></span> <span data-ttu-id="ceb08-279">RCSU başlatma parametreleri görünümü görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="ceb08-279">The RCSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="ceb08-280">**Bölge** alanında, **Doğu ABD**, **Doğu ABD 2**, **Batı ABD** veya **Batı ABD 2** seçeneklerinden birini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-280">In the **Region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="ceb08-281">**Sürüm** alanında, listeden bir **sürüm belirtin** ve sonra görüntülenen alanda **9.16.19262.5** belirtin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-281">In the **Version** field, select **Specify a version** in the list, and then specify **9.16.19262.5** in the field that appears.</span></span> <span data-ttu-id="ceb08-282">Burada belirtilen sürümü tam olarak belirttiğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="ceb08-282">Be sure to specify the exact version that is indicated here.</span></span> <span data-ttu-id="ceb08-283">Aksi durumda, RCSU öğesini daha sonra doğru sürüme güncelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ceb08-283">Otherwise, you will have to update RCSU to the correct version later.</span></span>
1. <span data-ttu-id="ceb08-284">**Uzantıyı Uygula** seçeneğini açın.</span><span class="sxs-lookup"><span data-stu-id="ceb08-284">Turn on the **Apply extension** option.</span></span>
1. <span data-ttu-id="ceb08-285">Uzantılar listesinden, **Commerce Önizleme demo temel uzantısını** seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-285">In the list of extensions, select **Commerce Preview Demo Base Extension**.</span></span>
1. <span data-ttu-id="ceb08-286">**Başlat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-286">Select **Initialize**.</span></span>
1. <span data-ttu-id="ceb08-287">Dağıtım onayı sayfasında, ayrıntıların doğru olduğunu doğruladıktan sonra **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-287">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="ceb08-288">**Perakende** sekmesi etkinleştirildiğinde, **Perakende Yönetim** görünümüne iade edilir.</span><span class="sxs-lookup"><span data-stu-id="ceb08-288">You're returned to the **Retail management** view, where the **Retail** tab is selected.</span></span> <span data-ttu-id="ceb08-289">RCSU kaynak ayırma işlemi için sıraya alındı.</span><span class="sxs-lookup"><span data-stu-id="ceb08-289">Your RCSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="ceb08-290">Devam etmeden önce, RCSU durumlarınız **Başarılı** olur.</span><span class="sxs-lookup"><span data-stu-id="ceb08-290">Before you continue, make sure that the status of your RCSU is **Success**.</span></span> <span data-ttu-id="ceb08-291">Başlatma yaklaşık iki ile beş saat arasında sürer.</span><span class="sxs-lookup"><span data-stu-id="ceb08-291">Initialization takes approximately two to five hours.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="ceb08-292">e-Ticaret başlat</span><span class="sxs-lookup"><span data-stu-id="ceb08-292">Initialize e-Commerce</span></span>

<span data-ttu-id="ceb08-293">Bir e-Ticaret başlatmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-293">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="ceb08-294">**E-ticaret (Önizleme)** sekmesinde, önizleme onayını gözden geçirip **kurulum**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-294">On the **e-Commerce (Preview)** tab, review the preview consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="ceb08-295">**E-ticaret kiracı adı** için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-295">In the **e-Commerce tenant name** field, enter a name.</span></span> <span data-ttu-id="ceb08-296">Ancak, e-ticaret örneğinizi gösteren bazı URL'lerde bu dosyanın görülebileceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="ceb08-296">However, be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="ceb08-297">**Retail Cloud Scale Unit adı** alanında, listesindeki RCSU alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-297">In the **Retail cloud scale unit name** field, select your RCSU in the list.</span></span> <span data-ttu-id="ceb08-298">(Listede yalnızca bir seçenek bulunmalıdır.)</span><span class="sxs-lookup"><span data-stu-id="ceb08-298">(The list should have only one option.)</span></span>

    <span data-ttu-id="ceb08-299">**E-ticaret coğrafyası** alanı otomatik olarak ayarlanır ve değer değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="ceb08-299">The **e-Commerce geography** field is set automatically, and the value can't be changed.</span></span>

1. <span data-ttu-id="ceb08-300">Devam etmek için **İleri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-300">Select **Next** to continue.</span></span>
1. <span data-ttu-id="ceb08-301">**Desteklenen ana bilgisayar adları** alanında, `www.fabrikam.com` gibi geçerli herhangi bir etki alanını girin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-301">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1.  <span data-ttu-id="ceb08-302">**Sistem Yöneticisi için AAD güvenlik grubunda** alanına, kullanmak istediğiniz güvenlik grubunun adının ilk birkaç harfini girin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-302">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="ceb08-303">Arama sonuçlarını görüntülemek için büyüteç simgesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-303">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="ceb08-304">Listeden bir güvenlik grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-304">Select a security group from the list.</span></span>
2.  <span data-ttu-id="ceb08-305">**Derecelendirme ve inceleme moderatörü için AAD güvenlik grubunda** alanına, kullanmak istediğiniz güvenlik grubunun adının ilk birkaç harfini girin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-305">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="ceb08-306">Arama sonuçlarını görüntülemek için büyüteç simgesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-306">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="ceb08-307">Listeden bir güvenlik grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-307">Select a security group from the list.</span></span>
1. <span data-ttu-id="ceb08-308">**Derecelendirmeleri etkinleştir ve gözden geçirme hizmeti** seçeneğini açık olarak bırakın.</span><span class="sxs-lookup"><span data-stu-id="ceb08-308">Leave the **Enable ratings and review service** option turned on.</span></span>
1. <span data-ttu-id="ceb08-309">"E-ticaret uygulamalarına erişim izni verme" bölümünde açıklandığı gibi Microsoft Azure Active Directory (Azure AD) onay adımını önceden tamamladıysanız, onayınızı onaylamak için onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-309">If you have already completed the Microsoft Azure Active Directory (Azure AD) consent step as described in the "Grant access to e-Commerce applications" section, select the check box to confirm your consent.</span></span> <span data-ttu-id="ceb08-310">Bu adımı henüz tamamlamadınız, başlatma işlemine devam etmeden önce bunu yapmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ceb08-310">If you have not yet completed this step, you need to do that before proceeding with the initialization.</span></span> <span data-ttu-id="ceb08-311">Kabul iletişim kutusunu açmak ve adımı tamamlamak için onay kutusunun yanındaki metinde bulunan bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-311">Select the link within the text next to the check box to open the consent dialog box and complete the step.</span></span>
1. <span data-ttu-id="ceb08-312">**Başlat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-312">Select **Initialize**.</span></span> <span data-ttu-id="ceb08-313">**e-Ticaret (önizleme) sekmesi** seçildiğinde, **Perakende Yönetim** görünümüne iade edilir.</span><span class="sxs-lookup"><span data-stu-id="ceb08-313">You're returned to the **Retail management** view, where the **e-Commerce (Preview)** tab is selected.</span></span> <span data-ttu-id="ceb08-314">E-ticaret başlatma işlemi başlatıldı.</span><span class="sxs-lookup"><span data-stu-id="ceb08-314">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="ceb08-315">Devam etmeden önce, e-ticaret başlatma durumunuz **başlatma başarılı** olana kadar bekleyin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-315">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="ceb08-316">Alt sağdaki **bağlantılar** altında, aşağıdaki bağlantıların URL 'lerini not alın:</span><span class="sxs-lookup"><span data-stu-id="ceb08-316">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="ceb08-317">**e-ticaret sitesi** – E-ticaret sitenizin köküne olan bağlantı.</span><span class="sxs-lookup"><span data-stu-id="ceb08-317">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="ceb08-318">**e-ticaret site yönetimi aracı** – site yönetimi aracına bağlantı.</span><span class="sxs-lookup"><span data-stu-id="ceb08-318">**e-Commerce site management tool** – The link to the site management tool.</span></span>

## <a name="commerce-preview-environment-support"></a><span data-ttu-id="ceb08-319">Commerce önizleme ortamı desteği</span><span class="sxs-lookup"><span data-stu-id="ceb08-319">Commerce preview environment support</span></span>

<span data-ttu-id="ceb08-320">Sağlama adımlarını gerçekleştirirken sorunlarla karşılaşırsanız, yardım için lütfen [Microsoft Dynamics 365 Commerce Önizleme Yammer grubunu](https://aka.ms/Dynamics365CommercePreviewYammer) ziyaret edin.</span><span class="sxs-lookup"><span data-stu-id="ceb08-320">If you experience issues while you're completing the provisioning steps, visit the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer) for help.</span></span>

<span data-ttu-id="ceb08-321">Yammer Gruba erişmeye çalıştığınızda sorunlarla karşılaşırsanız, Microsoft'a e-posta ile başvurabilirsiniz:  <Dynamics365Commerce@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="ceb08-321">If you experience issues when you try to access the Yammer group, you can contact Microsoft by email at <Dynamics365Commerce@microsoft.com>.</span></span> <span data-ttu-id="ceb08-322">Bu e-posta adresi etkin şekilde izlenmiyor.</span><span class="sxs-lookup"><span data-stu-id="ceb08-322">This email address isn't actively monitored.</span></span> <span data-ttu-id="ceb08-323">Bu nedenle, yanıtta bir gecikme olmasını bekler.</span><span class="sxs-lookup"><span data-stu-id="ceb08-323">Therefore, expect a delay in the response.</span></span>

## <a name="next-steps"></a><span data-ttu-id="ceb08-324">Sonraki adımlar</span><span class="sxs-lookup"><span data-stu-id="ceb08-324">Next steps</span></span>

<span data-ttu-id="ceb08-325">Commerce önizleme ortamını hazırlam ve yapılandırma işlemine devam etmek için bkz. [Commerce önizleme ortamı yapılandırma](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="ceb08-325">To continue the process of provisioning and configuring your Commerce preview environment, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ceb08-326">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="ceb08-326">Additional resources</span></span>

[<span data-ttu-id="ceb08-327">Ticaret önizleme ortamına genel bakış</span><span class="sxs-lookup"><span data-stu-id="ceb08-327">Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="ceb08-328">Ticaret önizleme ortamı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="ceb08-328">Configure a Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="ceb08-329">Bir Commerce Preview ortamı için isteğe bağlı özellikleri konfigüre edin</span><span class="sxs-lookup"><span data-stu-id="ceb08-329">Configure optional features for a Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="ceb08-330">Ticaret önizleme ortamı SSS</span><span class="sxs-lookup"><span data-stu-id="ceb08-330">Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="ceb08-331">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="ceb08-331">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="ceb08-332">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="ceb08-332">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="ceb08-333">Microsoft Azure portalı</span><span class="sxs-lookup"><span data-stu-id="ceb08-333">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="ceb08-334">Dynamics 365 Commerce web sitesi</span><span class="sxs-lookup"><span data-stu-id="ceb08-334">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="ceb08-335">Dynamics 365 Retail için yardım kaynakları</span><span class="sxs-lookup"><span data-stu-id="ceb08-335">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)
