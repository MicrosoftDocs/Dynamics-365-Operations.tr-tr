---
title: Yeni bir e-ticaret kiracısını dağıtma
description: Bu konu, Microsoft Dynamics Lifecycle Services (LCS) kullanarak yeni bir Dynamics 365 Commerce e-ticaret sitesi dağıtımının nasıl dağıtılacağını açıklamaktadır.
author: psimolin
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3b750ee89a85688dcebe673f9c3ff13693e9fcad
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976750"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="af581-103">Yeni bir e-ticaret kiracısını dağıtma</span><span class="sxs-lookup"><span data-stu-id="af581-103">Deploy a new e-commerce tenant</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="af581-104">Bu konu, Microsoft Dynamics Lifecycle Services (LCS) kullanarak yeni bir Dynamics 365 Commerce e-ticaret sitesi dağıtımının nasıl dağıtılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="af581-104">This topic describes how to deploy a new Dynamics 365 Commerce e-commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="overview"></a><span data-ttu-id="af581-105">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="af581-105">Overview</span></span>

<span data-ttu-id="af581-106">Microsoft Dynamics Lifecycle Services (LCS), iş ortaklarının ve müşterilerin projelerini ve ortamlarını yönetmek, Microsoft Dynamics ürünlerle ve özelliklerle ilgili en son bilgileri görüntülemek ve destek olayları oluşturmak, izlemek ve bunlara gözatmak için kullanılabilecek bulut tabanlı bir ortak çalışma alanıdır.</span><span class="sxs-lookup"><span data-stu-id="af581-106">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="af581-107">E-ticaret yönetim özellikleri LCS ile tümleşiktir.</span><span class="sxs-lookup"><span data-stu-id="af581-107">E-commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="af581-108">LCS hakkında daha fazla bilgi edinmek için, [Lifecycle Services Kullanıcı Kılavuzu](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)'na bakın.</span><span class="sxs-lookup"><span data-stu-id="af581-108">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="af581-109">Başlayın</span><span class="sxs-lookup"><span data-stu-id="af581-109">Get started</span></span>

<span data-ttu-id="af581-110">E-ticaretin ilk önce başlatılması için bir proje, ortam ve bir Retail Cloud Scale Unit (rcsu) başlatmalısınız.</span><span class="sxs-lookup"><span data-stu-id="af581-110">Before you can initialize e-commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="af581-111">LCS'de başlatma yapmak için, proje sahibi veya ortam yöneticisi rolü için izinleriniz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="af581-111">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="af581-112">Üretim ve korumalı alan ortam topolojileri desteklenir.</span><span class="sxs-lookup"><span data-stu-id="af581-112">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="af581-113">Ortamlar hakkında daha fazla bilgi için [ortam planlama](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="af581-113">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="af581-114">RCSU hakkında daha fazla bilgi için, bkz. [Retail Cloud Scale Unit Başlat](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="af581-114">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="af581-115">e-Ticaret başlat</span><span class="sxs-lookup"><span data-stu-id="af581-115">Initialize e-commerce</span></span>

<span data-ttu-id="af581-116">Varolan bir ortamdaki e-ticaret özelliğini başlatmak için bu yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="af581-116">Use this procedure to initialize the e-commerce feature in an existing environment.</span></span>

<span data-ttu-id="af581-117">Başlamadan önce, aşağıdaki gerekli bilgilere sahip olduğunuzdan emin olun:</span><span class="sxs-lookup"><span data-stu-id="af581-117">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="af581-118">Kullanılacak RCSU.</span><span class="sxs-lookup"><span data-stu-id="af581-118">The RCSU that will be used.</span></span>
- <span data-ttu-id="af581-119">E-ticaret sistem yöneticileri Için kullanılacak Microsoft Azure Active Directory güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="af581-119">The Microsoft Azure Active Directory security group that will be used for e-commerce system admins.</span></span>
- <span data-ttu-id="af581-120">Derecelendirme v inceleme moderatörleri için kullanılacak Microsoft Azure Active Directory güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="af581-120">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="af581-121">Ortam ile ilişkilendirilecek etki alanları.</span><span class="sxs-lookup"><span data-stu-id="af581-121">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="af581-122">Ek olarak, aşağıdaki isteğe bağlı bilgileri toplayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="af581-122">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="af581-123">Azure AD işletme-müşteri arası (B2C) bilgiler:</span><span class="sxs-lookup"><span data-stu-id="af581-123">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="af581-124">Kiracı adı.</span><span class="sxs-lookup"><span data-stu-id="af581-124">Tenant Name.</span></span>
    - <span data-ttu-id="af581-125">İstemci kodu.</span><span class="sxs-lookup"><span data-stu-id="af581-125">Client ID.</span></span>
    - <span data-ttu-id="af581-126">Özel Etki Alanında Oturum Aç.</span><span class="sxs-lookup"><span data-stu-id="af581-126">Login Custom Domain.</span></span>
    - <span data-ttu-id="af581-127">URL yanıtı.</span><span class="sxs-lookup"><span data-stu-id="af581-127">Reply URL.</span></span>
    - <span data-ttu-id="af581-128">Kaydolma Oturum Açma İlkesi Kodu.</span><span class="sxs-lookup"><span data-stu-id="af581-128">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="af581-129">Parola sıfırlama ilkesi kodu.</span><span class="sxs-lookup"><span data-stu-id="af581-129">Reset password Policy ID.</span></span>
    - <span data-ttu-id="af581-130">Profil İlkesi Kodunu Düzenle.</span><span class="sxs-lookup"><span data-stu-id="af581-130">Edit Profile Policy ID.</span></span>

> [!NOTE]
> <span data-ttu-id="af581-131">Bu bilgiler daha sonra bir servis isteği aracılığıyla eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="af581-131">This information can be added later, through a service request.</span></span>

<span data-ttu-id="af581-132">Gerekli bilgileri topladıktan sonra, e-ticaret başlatmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="af581-132">After you've collected the required information, follow these steps to initialize e-commerce.</span></span>

1. <span data-ttu-id="af581-133">[LCS](https://lcs.dynamics.com)'de oturum açın</span><span class="sxs-lookup"><span data-stu-id="af581-133">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="af581-134">E-ticaret başlatmak istediğiniz ortamı içeren projeyi açın.</span><span class="sxs-lookup"><span data-stu-id="af581-134">Open the project that contains the environment where you want to initialize e-commerce.</span></span>
1. <span data-ttu-id="af581-135">**Ortamlar** bölümünde, ortamı seçin.</span><span class="sxs-lookup"><span data-stu-id="af581-135">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="af581-136">**Ortam özellikleri** altında, **perakende Yönet** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="af581-136">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="af581-137">**E-ticaret** sekmesinde, **kurulum**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="af581-137">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="af581-138">Sağlama için gerekli bilgileri girmeniz gereken bir iletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="af581-138">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="af581-139">Gerekli bilgileri doldurun ve sonraki sayfaya gidin.</span><span class="sxs-lookup"><span data-stu-id="af581-139">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="af581-140">Sonraki sayfada, gerekli bilgileri doldurun ve formu gönderin.</span><span class="sxs-lookup"><span data-stu-id="af581-140">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="af581-141">Başlatmanın başlatıldığını görmek istediğiniz **e-ticaret** sekmesine iade ediyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="af581-141">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="af581-142">Başlatma durumunu görüntülemek için ya **Yenile** ya da **e-ticaret** sekmesine daha sonra dönün.</span><span class="sxs-lookup"><span data-stu-id="af581-142">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="af581-143">E-ticaret LCS'den başlatıldığında, sistem e-ticaret için gerekli olan birçok bileşeni sağlar ve bunları ortamla ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="af581-143">When e-commerce is initialized from LCS, the system provisions several components that are required for e-commerce and associates them with the environment.</span></span> <span data-ttu-id="af581-144">Sağlama tamamlandıktan sonra, **Perakende yönetim** sayfasındaki **e-ticaret** sekmesi sağlama işlemini yansıtacak şekilde güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="af581-144">After provisioning is complete, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="af581-145">Sayfa en son özelleştirme dağıtımlarını ve devam eden diğer tüm dağıtımları gösterir.</span><span class="sxs-lookup"><span data-stu-id="af581-145">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="af581-146">Ayrıca e-ticaret sitesi ve e-ticaret sitesi oluşturucu (sitelerin içeriğinin yazıldığı araç) bağlantıları da içerir.</span><span class="sxs-lookup"><span data-stu-id="af581-146">It also includes links to the e-commerce site and the Commerce site builder where sites are authored.</span></span>

## <a name="access-commerce-site-builder"></a><span data-ttu-id="af581-147">Commerce Site oluşturucuya erişim</span><span class="sxs-lookup"><span data-stu-id="af581-147">Access Commerce site builder</span></span>

<span data-ttu-id="af581-148">Commerce site oluşturucuya erişmek için, LCS'de **Retail Management** sayfasındaki **e-ticaret** sekmesine gidin ve **E-ticaret sitesi yönetim aracı** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="af581-148">To access Commerce site builder, go to the **e-Commerce** tab on the **Retail management** page in LCS and select the **e-Commerce site management tool** link.</span></span> <span data-ttu-id="af581-149">Site oluşturucunun giriş sayfası, kiracı düzeyinde bir ekran görüntüler.</span><span class="sxs-lookup"><span data-stu-id="af581-149">The site builder landing page displays a tenant-level view.</span></span> <span data-ttu-id="af581-150">Bu sayfadan şunları yapabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="af581-150">From this page, you can:</span></span>

- <span data-ttu-id="af581-151">Kiracı düzeyinde ayarları değiştirin.</span><span class="sxs-lookup"><span data-stu-id="af581-151">Modify tenant-level settings.</span></span>
- <span data-ttu-id="af581-152">Oluşturduğunuz ve görüntüleme iznine sahip olduğunuz bir siteye gidin.</span><span class="sxs-lookup"><span data-stu-id="af581-152">Navigate to any site you have created, and have permission to view.</span></span> 
- <span data-ttu-id="af581-153">Moderasyon ve raporlama gibi İncelemeler özelliklerine erişin.</span><span class="sxs-lookup"><span data-stu-id="af581-153">Access Reviews features such as moderation and reporting.</span></span>
- <span data-ttu-id="af581-154">Yeni bir site oluşturun.</span><span class="sxs-lookup"><span data-stu-id="af581-154">Create a new site.</span></span> <span data-ttu-id="af581-155">Yeni site oluşturma hakkında daha fazla bilgi için bkz. [Yeni e-ticaret sitesi oluşturma](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="af581-155">For more information about how to create a new site, see [Create an e-commerce site](create-ecommerce-site.md) .</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="af581-156">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="af581-156">Additional resources</span></span>

[<span data-ttu-id="af581-157">Etki alanı adınızı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="af581-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="af581-158">E-ticaret sitesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="af581-158">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="af581-159">Dynamics 365 Commerce sitesini çevrimiçi bir kanalla ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="af581-159">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="af581-160">robots.txt dosyalarını yönetme</span><span class="sxs-lookup"><span data-stu-id="af581-160">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="af581-161">URL yeniden yönlendirmelerini toplu olarak yükleme</span><span class="sxs-lookup"><span data-stu-id="af581-161">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="af581-162">Commerce'ta B2C kiracısı ayarlama</span><span class="sxs-lookup"><span data-stu-id="af581-162">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="af581-163">Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama</span><span class="sxs-lookup"><span data-stu-id="af581-163">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="af581-164">Commerce ortamında birden fazla B2C kiracısı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="af581-164">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="af581-165">İçerik teslim ağı (CDN) için destek ekleme</span><span class="sxs-lookup"><span data-stu-id="af581-165">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="af581-166">Konum tabanlı mağaza algılamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="af581-166">Enable location-based store detection</span></span>](enable-store-detection.md)
