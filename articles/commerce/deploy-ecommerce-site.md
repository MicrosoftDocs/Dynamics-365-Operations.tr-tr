---
title: Yeni bir e-ticaret kiracısını dağıtma
description: Bu konu, Microsoft Dynamics Lifecycle Services (LCS) kullanarak yeni bir Dynamics 365 Commerce e-ticaret sitesi dağıtımının nasıl dağıtılacağını açıklamaktadır.
author: psimolin
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6b228babfd32a4191eeed2a6d924a8b99f1a5311
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936718"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="84d45-103">Yeni bir e-ticaret kiracısını dağıtma</span><span class="sxs-lookup"><span data-stu-id="84d45-103">Deploy a new e-commerce tenant</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="84d45-104">Bu konu, Microsoft Dynamics Lifecycle Services (LCS) kullanarak yeni bir Dynamics 365 Commerce e-ticaret sitesi dağıtımının nasıl dağıtılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="84d45-104">This topic describes how to deploy a new Dynamics 365 Commerce e-commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="84d45-105">Microsoft Dynamics Lifecycle Services (LCS), iş ortaklarının ve müşterilerin projelerini ve ortamlarını yönetmek, Microsoft Dynamics ürünlerle ve özelliklerle ilgili en son bilgileri görüntülemek ve destek olayları oluşturmak, izlemek ve bunlara gözatmak için kullanılabilecek bulut tabanlı bir ortak çalışma alanıdır.</span><span class="sxs-lookup"><span data-stu-id="84d45-105">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="84d45-106">E-ticaret yönetim özellikleri LCS ile tümleşiktir.</span><span class="sxs-lookup"><span data-stu-id="84d45-106">E-commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="84d45-107">LCS hakkında daha fazla bilgi edinmek için, [Lifecycle Services Kullanıcı Kılavuzu](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)'na bakın.</span><span class="sxs-lookup"><span data-stu-id="84d45-107">To learn more about LCS, see the [Lifecycle Services User Guide](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="84d45-108">Başlayın</span><span class="sxs-lookup"><span data-stu-id="84d45-108">Get started</span></span>

<span data-ttu-id="84d45-109">E-ticaretin ilk önce başlatılması için bir proje, ortam ve bir Retail Cloud Scale Unit (rcsu) başlatmalısınız.</span><span class="sxs-lookup"><span data-stu-id="84d45-109">Before you can initialize e-commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="84d45-110">LCS'de başlatma yapmak için, proje sahibi veya ortam yöneticisi rolü için izinleriniz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="84d45-110">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="84d45-111">Üretim ve korumalı alan ortam topolojileri desteklenir.</span><span class="sxs-lookup"><span data-stu-id="84d45-111">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="84d45-112">Ortamlar hakkında daha fazla bilgi için [ortam planlama](/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="84d45-112">For more information about environments, see [Environment planning](/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="84d45-113">RCSU hakkında daha fazla bilgi için, bkz. [Retail Cloud Scale Unit Başlat](/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="84d45-113">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="84d45-114">e-Ticaret başlat</span><span class="sxs-lookup"><span data-stu-id="84d45-114">Initialize e-commerce</span></span>

<span data-ttu-id="84d45-115">Varolan bir ortamdaki e-ticaret özelliğini başlatmak için bu yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="84d45-115">Use this procedure to initialize the e-commerce feature in an existing environment.</span></span>

<span data-ttu-id="84d45-116">Başlamadan önce, aşağıdaki gerekli bilgilere sahip olduğunuzdan emin olun:</span><span class="sxs-lookup"><span data-stu-id="84d45-116">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="84d45-117">Kullanılacak RCSU.</span><span class="sxs-lookup"><span data-stu-id="84d45-117">The RCSU that will be used.</span></span>
- <span data-ttu-id="84d45-118">E-ticaret sistem yöneticileri Için kullanılacak Microsoft Azure Active Directory güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="84d45-118">The Microsoft Azure Active Directory security group that will be used for e-commerce system admins.</span></span>
- <span data-ttu-id="84d45-119">Derecelendirme v inceleme moderatörleri için kullanılacak Microsoft Azure Active Directory güvenlik grubu.</span><span class="sxs-lookup"><span data-stu-id="84d45-119">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="84d45-120">Ortam ile ilişkilendirilecek etki alanları.</span><span class="sxs-lookup"><span data-stu-id="84d45-120">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="84d45-121">Ek olarak, aşağıdaki isteğe bağlı bilgileri toplayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="84d45-121">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="84d45-122">Azure AD işletme-müşteri arası (B2C) bilgiler:</span><span class="sxs-lookup"><span data-stu-id="84d45-122">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="84d45-123">Kiracı adı.</span><span class="sxs-lookup"><span data-stu-id="84d45-123">Tenant Name.</span></span>
    - <span data-ttu-id="84d45-124">İstemci kodu.</span><span class="sxs-lookup"><span data-stu-id="84d45-124">Client ID.</span></span>
    - <span data-ttu-id="84d45-125">Özel Etki Alanında Oturum Aç.</span><span class="sxs-lookup"><span data-stu-id="84d45-125">Login Custom Domain.</span></span>
    - <span data-ttu-id="84d45-126">URL yanıtı.</span><span class="sxs-lookup"><span data-stu-id="84d45-126">Reply URL.</span></span>
    - <span data-ttu-id="84d45-127">Kaydolma Oturum Açma İlkesi Kodu.</span><span class="sxs-lookup"><span data-stu-id="84d45-127">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="84d45-128">Parola sıfırlama ilkesi kodu.</span><span class="sxs-lookup"><span data-stu-id="84d45-128">Reset password Policy ID.</span></span>
    - <span data-ttu-id="84d45-129">Profil İlkesi Kodunu Düzenle.</span><span class="sxs-lookup"><span data-stu-id="84d45-129">Edit Profile Policy ID.</span></span>

> [!NOTE]
> <span data-ttu-id="84d45-130">Bu bilgiler daha sonra bir servis isteği aracılığıyla eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="84d45-130">This information can be added later, through a service request.</span></span>

<span data-ttu-id="84d45-131">Gerekli bilgileri topladıktan sonra, e-ticaret başlatmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="84d45-131">After you've collected the required information, follow these steps to initialize e-commerce.</span></span>

1. <span data-ttu-id="84d45-132">[LCS](https://lcs.dynamics.com)'de oturum açın</span><span class="sxs-lookup"><span data-stu-id="84d45-132">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="84d45-133">E-ticaret başlatmak istediğiniz ortamı içeren projeyi açın.</span><span class="sxs-lookup"><span data-stu-id="84d45-133">Open the project that contains the environment where you want to initialize e-commerce.</span></span>
1. <span data-ttu-id="84d45-134">**Ortamlar** bölümünde, ortamı seçin.</span><span class="sxs-lookup"><span data-stu-id="84d45-134">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="84d45-135">**Ortam özellikleri** altında, **perakende Yönet** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="84d45-135">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="84d45-136">**E-ticaret** sekmesinde, **kurulum**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="84d45-136">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="84d45-137">Sağlama için gerekli bilgileri girmeniz gereken bir iletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="84d45-137">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="84d45-138">Gerekli bilgileri doldurun ve sonraki sayfaya gidin.</span><span class="sxs-lookup"><span data-stu-id="84d45-138">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="84d45-139">Sonraki sayfada, gerekli bilgileri doldurun ve formu gönderin.</span><span class="sxs-lookup"><span data-stu-id="84d45-139">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="84d45-140">Başlatmanın başlatıldığını görmek istediğiniz **e-ticaret** sekmesine iade ediyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="84d45-140">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="84d45-141">Başlatma durumunu görüntülemek için ya **Yenile** ya da **e-ticaret** sekmesine daha sonra dönün.</span><span class="sxs-lookup"><span data-stu-id="84d45-141">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="84d45-142">E-ticaret LCS'den başlatıldığında, sistem e-ticaret için gerekli olan birçok bileşeni sağlar ve bunları ortamla ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="84d45-142">When e-commerce is initialized from LCS, the system provisions several components that are required for e-commerce and associates them with the environment.</span></span> <span data-ttu-id="84d45-143">Sağlama tamamlandıktan sonra, **Perakende yönetim** sayfasındaki **e-ticaret** sekmesi sağlama işlemini yansıtacak şekilde güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="84d45-143">After provisioning is complete, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="84d45-144">Sayfa en son özelleştirme dağıtımlarını ve devam eden diğer tüm dağıtımları gösterir.</span><span class="sxs-lookup"><span data-stu-id="84d45-144">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="84d45-145">Ayrıca e-ticaret sitesi ve e-ticaret sitesi oluşturucu (sitelerin içeriğinin yazıldığı araç) bağlantıları da içerir.</span><span class="sxs-lookup"><span data-stu-id="84d45-145">It also includes links to the e-commerce site and the Commerce site builder where sites are authored.</span></span>

## <a name="access-commerce-site-builder"></a><span data-ttu-id="84d45-146">Commerce Site oluşturucuya erişim</span><span class="sxs-lookup"><span data-stu-id="84d45-146">Access Commerce site builder</span></span>

<span data-ttu-id="84d45-147">Commerce site oluşturucuya erişmek için, LCS'de **Retail Management** sayfasındaki **e-ticaret** sekmesine gidin ve **E-ticaret sitesi yönetim aracı** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="84d45-147">To access Commerce site builder, go to the **e-Commerce** tab on the **Retail management** page in LCS and select the **e-Commerce site management tool** link.</span></span> <span data-ttu-id="84d45-148">Site oluşturucunun giriş sayfası, kiracı düzeyinde bir ekran görüntüler.</span><span class="sxs-lookup"><span data-stu-id="84d45-148">The site builder landing page displays a tenant-level view.</span></span> <span data-ttu-id="84d45-149">Bu sayfadan şunları yapabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="84d45-149">From this page, you can:</span></span>

- <span data-ttu-id="84d45-150">Kiracı düzeyinde ayarları değiştirin.</span><span class="sxs-lookup"><span data-stu-id="84d45-150">Modify tenant-level settings.</span></span>
- <span data-ttu-id="84d45-151">Oluşturduğunuz ve görüntüleme iznine sahip olduğunuz bir siteye gidin.</span><span class="sxs-lookup"><span data-stu-id="84d45-151">Navigate to any site you have created, and have permission to view.</span></span> 
- <span data-ttu-id="84d45-152">Moderasyon ve raporlama gibi İncelemeler özelliklerine erişin.</span><span class="sxs-lookup"><span data-stu-id="84d45-152">Access Reviews features such as moderation and reporting.</span></span>
- <span data-ttu-id="84d45-153">Yeni bir site oluşturun.</span><span class="sxs-lookup"><span data-stu-id="84d45-153">Create a new site.</span></span> <span data-ttu-id="84d45-154">Yeni site oluşturma hakkında daha fazla bilgi için bkz. [Yeni e-ticaret sitesi oluşturma](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="84d45-154">For more information about how to create a new site, see [Create an e-commerce site](create-ecommerce-site.md) .</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="84d45-155">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="84d45-155">Additional resources</span></span>

[<span data-ttu-id="84d45-156">Etki alanı adınızı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="84d45-156">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="84d45-157">E-ticaret sitesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="84d45-157">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="84d45-158">Dynamics 365 Commerce sitesini çevrimiçi bir kanalla ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="84d45-158">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="84d45-159">robots.txt dosyalarını yönetme</span><span class="sxs-lookup"><span data-stu-id="84d45-159">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="84d45-160">URL yeniden yönlendirmelerini toplu olarak yükleme</span><span class="sxs-lookup"><span data-stu-id="84d45-160">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="84d45-161">Commerce'ta B2C kiracısı ayarlama</span><span class="sxs-lookup"><span data-stu-id="84d45-161">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="84d45-162">Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama</span><span class="sxs-lookup"><span data-stu-id="84d45-162">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="84d45-163">Commerce ortamında birden fazla B2C kiracısı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="84d45-163">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="84d45-164">İçerik teslim ağı (CDN) için destek ekleme</span><span class="sxs-lookup"><span data-stu-id="84d45-164">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="84d45-165">Konum tabanlı mağaza algılamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="84d45-165">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]