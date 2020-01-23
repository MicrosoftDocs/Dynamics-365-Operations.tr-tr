---
title: Yeni bir e-Ticaret kiracısını dağıtma
description: Bu konu, Microsoft Dynamics Lifecycle Services (LCS) kullanarak yeni bir e-ticaret kiracısı dağıtımının nasıl dağıtılacağını açıklamaktadır.
author: psimolin
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 10dab1e62446ff7f60ad48fd0841bde5cfd29e12
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945525"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="4d2ae-103">Yeni bir e-Ticaret kiracısını dağıtma</span><span class="sxs-lookup"><span data-stu-id="4d2ae-103">Deploy a new e-Commerce tenant</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="4d2ae-104">Bu konu, Microsoft Dynamics Lifecycle Services (LCS) kullanarak yeni bir e-ticaret sitesi dağıtımının nasıl dağıtılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-104">This topic describes how to deploy a new e-Commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="overview"></a><span data-ttu-id="4d2ae-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="4d2ae-105">Overview</span></span>
    
<span data-ttu-id="4d2ae-106">Microsoft Dynamics Lifecycle Services (LCS), iş ortaklarının ve müşterilerin projelerini ve ortamlarını yönetmek, Microsoft Dynamics ürünlerle ve özelliklerle ilgili en son bilgileri görüntülemek ve destek olayları oluşturmak, izlemek ve bunlara gözatmak için kullanılabilecek bulut tabanlı bir ortak çalışma alanıdır.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-106">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="4d2ae-107">E-ticaret yönetim özellikleri LCS ile tümleşiktir.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-107">E-Commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="4d2ae-108">LCS hakkında daha fazla bilgi edinmek için, [Lifecycle Services Kullanıcı Kılavuzu](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)'na bakın.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-108">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="4d2ae-109">Başlayın</span><span class="sxs-lookup"><span data-stu-id="4d2ae-109">Get started</span></span>

<span data-ttu-id="4d2ae-110">E-ticaretin ilk önce başlatılması için bir proje, ortam ve bir Retail Cloud Scale Unit (rcsu) başlatmalısınız.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-110">Before you can initialize e-Commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="4d2ae-111">LCS'de başlatma yapmak için, proje sahibi veya ortam yöneticisi rolü için izinleriniz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-111">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="4d2ae-112">Üretim ve korumalı alan ortam topolojileri desteklenir.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-112">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="4d2ae-113">Ortamlar hakkında daha fazla bilgi için [ortam planlama](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-113">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="4d2ae-114">RCSU hakkında daha fazla bilgi için, bkz. [Retail Cloud Scale Unit Başlat](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="4d2ae-114">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="4d2ae-115">e-Ticaret başlat</span><span class="sxs-lookup"><span data-stu-id="4d2ae-115">Initialize e-Commerce</span></span>

<span data-ttu-id="4d2ae-116">Varolan bir ortamdaki e-ticaret özelliğini başlatmak için bu yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-116">Use this procedure to initialize the e-Commerce feature in an existing environment.</span></span>

<span data-ttu-id="4d2ae-117">Başlamadan önce, aşağıdaki gerekli bilgilere sahip olduğunuzdan emin olun:</span><span class="sxs-lookup"><span data-stu-id="4d2ae-117">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="4d2ae-118">Kullanılacak RCSU.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-118">The RCSU that will be used.</span></span>
- <span data-ttu-id="4d2ae-119">E-ticaret sistem yöneticileri Için kullanılacak Microsoft Azure Active Directory güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-119">The Microsoft Azure Active Directory security group that will be used for e-Commerce system admins.</span></span>
- <span data-ttu-id="4d2ae-120">Derecelendirme v inceleme moderatörleri için kullanılacak Microsoft Azure Active Directory güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-120">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="4d2ae-121">Ortam ile ilişkilendirilecek etki alanları.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-121">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="4d2ae-122">Ek olarak, aşağıdaki isteğe bağlı bilgileri toplayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="4d2ae-122">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="4d2ae-123">Azure AD işletme-müşteri arası (B2C) bilgiler:</span><span class="sxs-lookup"><span data-stu-id="4d2ae-123">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="4d2ae-124">Kiracı adı.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-124">Tenant Name.</span></span>
    - <span data-ttu-id="4d2ae-125">İstemci kodu.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-125">Client ID.</span></span>
    - <span data-ttu-id="4d2ae-126">Özel Etki Alanında Oturum Aç.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-126">Login Custom Domain.</span></span>
    - <span data-ttu-id="4d2ae-127">URL yanıtı.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-127">Reply URL.</span></span>
    - <span data-ttu-id="4d2ae-128">Kaydolma Oturum Açma İlkesi Kodu.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-128">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="4d2ae-129">Parola sıfırlama ilkesi kodu.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-129">Reset password Policy ID.</span></span>
    - <span data-ttu-id="4d2ae-130">Profil İlkesi Kodunu Düzenle.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-130">Edit Profile Policy ID.</span></span>

[!NOTE]
<span data-ttu-id="4d2ae-131">Bu bilgiler daha sonra bir servis isteği aracılığıyla eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-131">This information can be added later, through a service request.</span></span>

<span data-ttu-id="4d2ae-132">Gerekli bilgileri topladıktan sonra, e-ticaret başlatmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-132">After you've collected the required information, follow these steps to initialize e-Commerce.</span></span>

1. <span data-ttu-id="4d2ae-133">[LCS](https://lcs.dynamics.com)'de oturum açın</span><span class="sxs-lookup"><span data-stu-id="4d2ae-133">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="4d2ae-134">E-ticaret başlatmak istediğiniz ortamı içeren projeyi açın.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-134">Open the project that contains the environment where you want to initialize e-Commerce.</span></span>
1. <span data-ttu-id="4d2ae-135">**Ortamlar** bölümünde, ortamı seçin.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-135">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="4d2ae-136">**Ortam özellikleri**altında, **perakende Yönet** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-136">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="4d2ae-137">**E-ticaret** sekmesinde, **kurulum**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-137">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="4d2ae-138">Sağlama için gerekli bilgileri girmeniz gereken bir iletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-138">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="4d2ae-139">Gerekli bilgileri doldurun ve sonraki sayfaya gidin.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-139">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="4d2ae-140">Sonraki sayfada, gerekli bilgileri doldurun ve formu gönderin.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-140">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="4d2ae-141">Başlatmanın başlatıldığını görmek istediğiniz **e-ticaret** sekmesine iade ediyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-141">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="4d2ae-142">Başlatma durumunu görüntülemek için ya **Yenile** ya da **e-ticaret** sekmesine daha sonra dönün.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-142">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="4d2ae-143">E-ticaret LCS'den başlatıldığında, sistem e-ticaret için gerekli olan birçok bileşeni sağlar ve bunları ortamla ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-143">When e-Commerce is initialized from LCS, the system provisions several components that are required for e-Commerce and associates them with the environment.</span></span> <span data-ttu-id="4d2ae-144">Sağlama tamamlandıktan sonra, **Perakende yönetim** sayfasındaki **e-ticaret** sekmesi sağlama işlemini yansıtacak şekilde güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-144">After provisioning is completed, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="4d2ae-145">Sayfa en son özelleştirme dağıtımlarını ve devam eden diğer tüm dağıtımları gösterir.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-145">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="4d2ae-146">Ayrıca e-ticaret sitesi ve e-ticaret sitesi yönetim aracı (geliştirme aracı) bağlantıları da içerir.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-146">It also includes links to the e-Commerce site and the e-Commerce site management tool (the authoring tool).</span></span>

## <a name="access-the-authoring-environment"></a><span data-ttu-id="4d2ae-147">Yazma ortamına erişim</span><span class="sxs-lookup"><span data-stu-id="4d2ae-147">Access the authoring environment</span></span>

<span data-ttu-id="4d2ae-148">Geliştirme ortamına erişmek için, **Perakende yönetimi** sayfasındaki **e-ticaret** sekmesine gidin.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-148">To access the authoring environment, go to the **e-Commerce** tab on the **Retail management** page.</span></span> <span data-ttu-id="4d2ae-149">Burada e-ticaret sitenize ve site yönetim aracına bağlantılar bulacaksınız.</span><span class="sxs-lookup"><span data-stu-id="4d2ae-149">There, you will find links to your e-Commerce site and the site management tool.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4d2ae-150">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="4d2ae-150">Additional resources</span></span>

[<span data-ttu-id="4d2ae-151">Etki alanı adınızı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="4d2ae-151">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="4d2ae-152">e-Ticaret sitesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="4d2ae-152">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="4d2ae-153">Çevrimiçi siteyi bir kanalla ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="4d2ae-153">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="4d2ae-154">Robots.txt dosyalarını yönetme</span><span class="sxs-lookup"><span data-stu-id="4d2ae-154">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="4d2ae-155">Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama</span><span class="sxs-lookup"><span data-stu-id="4d2ae-155">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="4d2ae-156">İçerik teslim ağı (CDN) için destek ekleme</span><span class="sxs-lookup"><span data-stu-id="4d2ae-156">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="4d2ae-157">Konum tabanlı mağaza algılamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="4d2ae-157">Enable location-based store detection</span></span>](enable-store-detection.md)
