---
title: Dynamics 365 Commerce uygulamasında etki alanları
description: Bu konuda, etki alanlarının Microsoft Dynamics 365 Commerce uygulamasında nasıl yönetildiği açıklanmaktadır.
author: BrShoo
manager: AnnBe
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: BrShoo
ms.search.validFrom: ''
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 84becee12363ca38951ff13073d87d1b1f14b616
ms.sourcegitcommit: a47a4652a29fdb567a8ba67c4f914a8698e8c48c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/03/2020
ms.locfileid: "3765013"
---
# <a name="domains-in-dynamics-365-commerce"></a><span data-ttu-id="558bb-103">Dynamics 365 Commerce uygulamasında etki alanları</span><span class="sxs-lookup"><span data-stu-id="558bb-103">Domains in Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="558bb-104">Bu konuda, etki alanlarının Microsoft Dynamics 365 Commerce uygulamasında nasıl yönetildiği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="558bb-104">This topic describes how domains are handled in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="558bb-105">Etki alanları, bir web tarayıcısında Dynamics 365 Commerce sitelerinde gezinmek için kullanılan web adresleridir.</span><span class="sxs-lookup"><span data-stu-id="558bb-105">Domains are web addresses used to navigate to Dynamics 365 Commerce sites in a web browser.</span></span> <span data-ttu-id="558bb-106">Etki alanının yönetimini seçilen bir etki alanı adı sunucusu (DNS) sağlayıcısıyla denetleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="558bb-106">You control management of your domain with a chosen Domain Name Server (DNS) provider.</span></span> <span data-ttu-id="558bb-107">Dynamics 365 Commerce site oluşturucusunda yayımlandığında bir siteye nasıl erişileceğini koordine etmek için etki alanlarına başvurulur.</span><span class="sxs-lookup"><span data-stu-id="558bb-107">Domains are referenced throughout Dynamics 365 Commerce site builder to coordinate how a site will be accessed when published.</span></span> <span data-ttu-id="558bb-108">Bu konuda, Commerce site geliştirme ve başlatma yaşam döngüsü boyunca etki alanlarının nasıl yönetildiği ve başvurulduğu incelenir.</span><span class="sxs-lookup"><span data-stu-id="558bb-108">This topic reviews how domains are handled and referenced throughout the lifecycle of the Commerce site development and launch.</span></span>

## <a name="provisioning-and-supported-host-names"></a><span data-ttu-id="558bb-109">Hazırlama ve desteklenen ana bilgisayar adları</span><span class="sxs-lookup"><span data-stu-id="558bb-109">Provisioning and supported host names</span></span>

<span data-ttu-id="558bb-110">[Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/) içinde bir e-ticaret ortamı hazırlanırken, dağıtılmış Commerce ortamıyla ilişkilendirilecek etki alanlarını girmek için e-ticaret hazırlama ekranındaki **Desteklenen ana bilgisayar adları** kutusu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="558bb-110">When provisioning an e-Commerce environment in [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/), the **Supported host names** box on the e-Commerce provisioning screen is used to enter domains that will be associated with the deployed Commerce environment.</span></span> <span data-ttu-id="558bb-111">Bu etki alanları, e-ticaret web sitelerinin barındırıldığı müşteri tarafındaki etki alanı adı sunucusu (DNS) adları olacaktır.</span><span class="sxs-lookup"><span data-stu-id="558bb-111">These domains will be the customer-facing Domain Name Server (DNS) names where e-Commerce websites will be hosted.</span></span> <span data-ttu-id="558bb-112">Bu aşamada bir etki alanı girildiğinde, etki alanının trafiği Dynamics 365 Commerce uygulamasına yönlendirilmeye başlamaz.</span><span class="sxs-lookup"><span data-stu-id="558bb-112">Entering a domain at this stage does not start diverting traffic for the domain to Dynamics 365 Commerce.</span></span> <span data-ttu-id="558bb-113">Etki alanının trafiği, yalnızca DNS CNAME kaydı etki alanı ile Commerce uç noktasını kullanacak şekilde güncelleştirildiğinde Commerce uç noktasına yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="558bb-113">Traffic for a domain will only be routed to the Commerce endpoint when the DNS CNAME record is updated to use the Commerce endpoint with the domain.</span></span>

> [!NOTE]
> <span data-ttu-id="558bb-114">**Desteklenen ana bilgisayar adları** kutusuna, noktalı virgüllerle ayırarak birden fazla etki alanı girilebilir.</span><span class="sxs-lookup"><span data-stu-id="558bb-114">Multiple domains can be entered into the **Supported host names** box by separating them with semi-colons.</span></span>

<span data-ttu-id="558bb-115">Aşağıdaki resimde, **desteklenen ana bilgisayar adları kutusu** vurgulanmış olarak LCS e-Commerce hazırlama ekranı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="558bb-115">The following illustration shows the LCS e-Commerce provisioning screen with the **Supported host names** box highlighted.</span></span> 

![Vurgulanmış olarak **Desteklenen ana bilgisayar adları** kutusunun bulunduğu LCS e-Commerce hazırlama ekranı](./media/Domains_ProvisioningeCommerceScreen.png)

<span data-ttu-id="558bb-117">Hazırlama işlemi oluşturulmaya başlandıysa, ortama ek etki alanları eklemek için bir servis isteği oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="558bb-117">You can create a service request to add additional domains to an environment if provisioning has already occurred.</span></span> <span data-ttu-id="558bb-118">LCS içinde bir servis talebi oluşturmak için, ortamınızda **Destek \> Destek sorunları** bölümüne gidin ve **Bir olay gönderin** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="558bb-118">To create a service request in LCS, within your environment go to **Support \> Support issues** and select **Submit an incident**.</span></span>

## <a name="commerce-generated-urls"></a><span data-ttu-id="558bb-119">Commerce tarafından oluşturulan URL'Ler</span><span class="sxs-lookup"><span data-stu-id="558bb-119">Commerce-generated URLs</span></span>

<span data-ttu-id="558bb-120">Bir e-ticaret ortamı hazırlanırken Commerce, ortam için çalışma adresi olacak bir URL oluşturur.</span><span class="sxs-lookup"><span data-stu-id="558bb-120">When provisioning an e-Commerce environment, Commerce will generate a URL that will be the working address for the environment.</span></span> <span data-ttu-id="558bb-121">Bu URL'ye, ortam hazırlandıktan sonra LCS'de gösterilen e-ticaret site bağlantısında başvurulur.</span><span class="sxs-lookup"><span data-stu-id="558bb-121">This URL is referenced in the e-Commerce site link shown in LCS after the environment is provisioned.</span></span> <span data-ttu-id="558bb-122">Commerce tarafından oluşturulan bir URL, Commerce ortamı için e-ticaret kiracı adının LCS'de girildiği `https://<e-Commerce tenant name>.commerce.dynamics.com` adresi şeklindedir.</span><span class="sxs-lookup"><span data-stu-id="558bb-122">A Commerce-generated URL is in the format `https://<e-Commerce tenant name>.commerce.dynamics.com`, where the e-Commerce tenant name is the name entered in LCS for the Commerce environment.</span></span>

<span data-ttu-id="558bb-123">Üretim sitesi ana bilgisayar adlarını, bir korumalı alan ortamında da kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="558bb-123">You can use production site host names in a sandbox environment as well.</span></span> <span data-ttu-id="558bb-124">Bu seçenek, bir siteyi bir korumalı alan ortamından üretime kopyalayacaksanız ideal bir seçenektir.</span><span class="sxs-lookup"><span data-stu-id="558bb-124">This option is ideal when you will be copying a site from a sandbox environment to production.</span></span>

## <a name="site-setup"></a><span data-ttu-id="558bb-125">Site kurulumu</span><span class="sxs-lookup"><span data-stu-id="558bb-125">Site setup</span></span>

<span data-ttu-id="558bb-126">E-ticaret ortamınız hazırlandıktan sonra, sitenizi çalışma URL'siyle ilişkilendirmek için Commerce site oluşturucusunda sitenizi kurmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="558bb-126">After your e-Commerce environment is provisioned, you must set up your site in Commerce site builder to associate your site to the working URL.</span></span>

<span data-ttu-id="558bb-127">Site oluşturucusunda ilk kez bir site kurarken, **Sitenizi kurun** iletişim kutusu açılır.</span><span class="sxs-lookup"><span data-stu-id="558bb-127">When you first set up a site in site builder, the **Setup your Site** dialog box will appear.</span></span>

<span data-ttu-id="558bb-128">Aşağıdaki şekilde, site oluşturucusuna ilk kez eriştiğinizde "varsayılan" adlı bir site için **Sitenizi kurun** iletişim kutusu gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="558bb-128">The following illustration shows the **Setup your Site** dialog box for a site named "default" when you access the site for the first time in site builder.</span></span>

![**Sitenizi kurun** iletişim kutusu](./media/Domains_SetupyoursiteScreen.png)

<span data-ttu-id="558bb-130">**Bir etki alanı seçin** kutusu, LCS içindeki siteniz için sağlanan desteklenen ana bilgisayar adlarından birini site oluşturucusundaki sitenize ilişkilendirmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="558bb-130">The **Select a domain** box allows you to associate one of the supported host names provided for your site in LCS to your site in site builder.</span></span>

<span data-ttu-id="558bb-131">**Yol** kutusu boş bırakılabilir veya çalışma URL'nize yansıyacak başka bir yol dizesi eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="558bb-131">The **Path** box can be left blank, or an additional path string can be added that will be reflected in your working URL.</span></span> <span data-ttu-id="558bb-132">**Yol** kutusunu boş bırakmak, temel Commerce tarafından oluşturulan URL'yi, site oluşturucusunda kurulan siteyle ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="558bb-132">Leaving the **Path** box blank associates the base Commerce-generated URL with the site being set up in site builder.</span></span> <span data-ttu-id="558bb-133">Yollar her site/etki alanı çifti için benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="558bb-133">Paths must be unique for each site/domain pair.</span></span> <span data-ttu-id="558bb-134">Seçili site ve etki alanı içinde, ortamdaki yalnızca bir site boş yolu kullanabilir veya benzersiz bir yol dizesiyle ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="558bb-134">Within the site and domain selected, only one site in the environment can use the blank path or be associated with a unique path string.</span></span> <span data-ttu-id="558bb-135">Site kurulumu sırasında **Yol** alanına eklenen tüm dizeler, web tarayıcısında siteye erişmek için kullanılan, Commerce tarafından üretilen temel URL'nin bir alt yolu olur.</span><span class="sxs-lookup"><span data-stu-id="558bb-135">Any string added to the **Path** field during site setup will become a subpath of the base Commerce-generated URL used to access the site in a web browser.</span></span>

> [!NOTE]
> <span data-ttu-id="558bb-136">Yol, site oluşturucusunun **Site ayarları \> Kanallar** yapılandırması bölümüne bir kanal eklerken **Eşleşme yolu** olarak da bilinir.</span><span class="sxs-lookup"><span data-stu-id="558bb-136">The path is also known as the **Match path** when adding a channel in the **Site Settings \> Channels** configuration section of site builder.</span></span>

<span data-ttu-id="558bb-137">Örneğin, "xyz" adlı bir e-ticaret kiracısında site oluşturucusunda "Fabrikam" adlı bir siteniz varsa ve siteyi boş bir yolla ayarlarsanız, Commerce tarafından olarak oluşturulan temel URL'ye doğrudan giderek, bir web tarayıcısındaki yayınlanan site içeriğine erişebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="558bb-137">For example, if you have a site in site builder called "fabrikam" in an e-Commerce tenant named "xyz," and if you set up the site with a blank path, then you would access the published site content in a web browser by going directly to the base Commerce-generated URL:</span></span>

`https://xyz.commerce.dynamics.com`

<span data-ttu-id="558bb-138">Alternatif olarak, aynı sitenin kurulumu sırasında "fabrikam" yolunu eklediyseniz, aşağıdaki URL'yi kullanarak bir web tarayıcısında yayınlanan site içeriğine erişebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="558bb-138">Alternately, if you had added a path of "fabrikam" during this same site's setup, you would access the published site content in a web browser using the following URL:</span></span>

`https://xyz.commerce.dynamics.com/fabrikam`

## <a name="pages-and-urls"></a><span data-ttu-id="558bb-139">Sayfalar ve URL'Ler</span><span class="sxs-lookup"><span data-stu-id="558bb-139">Pages and URLs</span></span>

<span data-ttu-id="558bb-140">Siteniz bir yolla oluşturulduktan sonra, site oluşturucusundaki sayfalarla ilişkilendirilmiş tüm URL'Ler, sitenin çalıştığı URL'de (Commerce tarafından oluşturulan URL'de veya Commerce tarafından oluşturulan URL ve yol) oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="558bb-140">After your site is set up with a path, all URLs associated with pages in site builder will build on the working URL (the Commerce-generated URL, or the Commerce-generated URL plus the path) for the site.</span></span> <span data-ttu-id="558bb-141">**Yeni URL** iletişim kutusundaki listeden bir sayfa seçip bu sayfanın URL yolunu girerek, site oluşturucusunda yeni bir URL oluşturmak (**URL'ler /> + Yeni**) URL'yi seçili sayfayla ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="558bb-141">Creating a new URL in site builder (**URLS /> +New**) by selecting a page from the list in the **New URL** dialog box and entering the URL path for that page will associate that URL with the selected page.</span></span> <span data-ttu-id="558bb-142">URL yolu değeri sayfaya erişmek için sitenin çalışma URL'sine eklenir ve site oluşturucusundaki **URL'ler** sayfasının URL listesinde `./<URL path>` olarak etiketlenir.</span><span class="sxs-lookup"><span data-stu-id="558bb-142">The URL path value then appends to the site's working URL to access the page, and is labeled as `./<URL path>` in the URL list of the **URLs** page in site builder.</span></span>

<span data-ttu-id="558bb-143">Aşağıdaki şekilde, URL yolunun vurgulandığı bir örnek bulunan site oluşturucusundaki **Yeni URL** iletişim kutusu gösterilir.</span><span class="sxs-lookup"><span data-stu-id="558bb-143">The following illustration shows the **New URL** dialog box in site builder with an example URL path highlighted.</span></span> 

![Site oluşturucusundaki **Yeni URL** iletişim kutusu](./media/Domains_PageSetup2a.png)

<span data-ttu-id="558bb-145">Aşağıdaki şekilde, listede URL yolunun vurgulandığı bir örnek bulunan site oluşturucusundaki **URL'ler** sayfası gösterilir.</span><span class="sxs-lookup"><span data-stu-id="558bb-145">The following illustration shows the **URLs** page in site builder with an example URL highlighted in the list.</span></span>

![İlke akışında kullanıcı akışı seçeneğini çalıştır](./media/Domains_URLsInSiteBuilder2a.png)

## <a name="domains-in-site-builder"></a><span data-ttu-id="558bb-147">Site oluşturucusundaki etki alanları</span><span class="sxs-lookup"><span data-stu-id="558bb-147">Domains in site builder</span></span>

<span data-ttu-id="558bb-148">Desteklenen ana bilgisayar adları değerleri, bir siteyi kurarken etki alanı olarak ilişkilendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="558bb-148">The supported host names values are available to be associated as a domain when setting up a site.</span></span> <span data-ttu-id="558bb-149">Etki alanı olarak desteklenen bir ana bilgisayar adı değeri seçerken, site oluşturucusunda başvurulan etki alanının görüntülendiğini görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="558bb-149">When selecting a supported host name value as the domain, you will see the chosen domain referenced throughout site builder.</span></span> <span data-ttu-id="558bb-150">Bu etki alanı yalnızca Commerce ortamı içinde bulunan bir başvurudur, o etki alanının canlı trafiği henüz Dynamics 365 Commerce uygulamasına yönlendirilmez.</span><span class="sxs-lookup"><span data-stu-id="558bb-150">This domain is only a reference within the Commerce environment, live traffic for that domain will not yet be forwarded to Dynamics 365 Commerce.</span></span>

<span data-ttu-id="558bb-151">Site oluşturucusunda sitelerle çalışırken, iki farklı etki alanı ile kurulmuş iki siteniz varsa, bir tarayıcıda yayınlanan site içeriğine erişmek için, çalışma URL'nize **?domain=** özniteliğini ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="558bb-151">When working with sites in site builder, if you have two sites set up with two different domains, you can append the **?domain=** attribute to your working URL to access the published site content in a browser.</span></span>

<span data-ttu-id="558bb-152">Örneğin, "xyz" ortamı hazırlandı ve site oluşturucusunda iki site oluşturulup ilişkilendirildi: Biri `www.fabrikam.com` etki alanına sahip ve diğeri `www.constoso.com` etki alanına sahip.</span><span class="sxs-lookup"><span data-stu-id="558bb-152">For example, environment "xyz" has been provisioned, and two sites have been created and associated in site builder: one with the domain `www.fabrikam.com` and the other with the domain `www.constoso.com`.</span></span> <span data-ttu-id="558bb-153">Her site boş bir yol kullanarak kuruldu.</span><span class="sxs-lookup"><span data-stu-id="558bb-153">Each site was set up using a blank path.</span></span> <span data-ttu-id="558bb-154">Daha sonra bu iki siteye, **?domain=** özniteliğini kullanarak bir web tarayıcısından aşağıdaki gibi erişilebilir:</span><span class="sxs-lookup"><span data-stu-id="558bb-154">These two sites could then be accessed in a web browser as follows using the **?domain=** attribute:</span></span>
- `https://xyz.commerce.dynamics.com?domain=www.fabrikam.com`
- `https://xyz.commerce.dynamics.com?domain=www.contoso.com`

<span data-ttu-id="558bb-155">Birden çok etki alanı bulunan bir ortamda bir etki alanı sorgusu dizesi verilmediğinde, Commerce, verdiğiniz ilk etki alanını kullanır.</span><span class="sxs-lookup"><span data-stu-id="558bb-155">When a domain query string is not given in an environment with multiple domains provided, Commerce uses the first domain you provided.</span></span> <span data-ttu-id="558bb-156">Örneğin, site kurulumu sırasında ilk olarak "fabrikam" yolu sağlanmışsa, `https://xyz.commerce.dynamics.com` URL'si `www.fabrikam.com` için yayımlanan sitenin içerik sitesine erişmek amacıyla kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="558bb-156">For example, if the path "fabrikam" was provided first during site setup, the URL `https://xyz.commerce.dynamics.com` could be used to access the published site content site for `www.fabrikam.com`.</span></span>

## <a name="traffic-forwarding-in-production"></a><span data-ttu-id="558bb-157">Üretimde trafiği yönlendirme</span><span class="sxs-lookup"><span data-stu-id="558bb-157">Traffic forwarding in production</span></span>

<span data-ttu-id="558bb-158">commerce.dynamics.com uç noktasının kendisi üzerindeki etki alanı sorgulama dizesi parametrelerini kullanarak birden çok etki alanı benzetimi yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="558bb-158">You can simulate multiple domains using domain query string parameters on the commerce.dynamics.com endpoint itself.</span></span> <span data-ttu-id="558bb-159">Ancak, üretimde canlıya geçmeniz gerektiğinde, özel etki alanınıza ilişkin trafiği `<e-Commerce tenant name>.commerce.dynamics.com` uç noktasına yönlendirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="558bb-159">But when you need to go live in production, you must forward the traffic for your custom domain to the `<e-Commerce tenant name>.commerce.dynamics.com` endpoint.</span></span>

<span data-ttu-id="558bb-160">`<e-Commerce tenant name>.commerce.dynamics.com` uç noktası özel etki alanı güvenli yuva katmanlarını (SSL'ler) desteklemediğinden, front door hizmeti veya içerik teslim ağı (CDN) kullanarak özel etki alanları kurmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="558bb-160">The `<e-Commerce tenant name>.commerce.dynamics.com` endpoint does not support custom domain Secure Sockets Layers (SSLs), so you must set up custom domains using a front door service or content delivery network (CDN).</span></span> 

<span data-ttu-id="558bb-161">Bir front door hizmeti veya CDN kullanarak özel etki alanları ayarlamak için iki seçeneğiniz vardır:</span><span class="sxs-lookup"><span data-stu-id="558bb-161">To set up custom domains using a front door service or CDN, you have two options:</span></span>

- <span data-ttu-id="558bb-162">Ön uç trafiği yönetmek ve Commerce ortamınıza bağlamak için, Azure Front Door gibi bir front door hizmeti kurun.</span><span class="sxs-lookup"><span data-stu-id="558bb-162">Set up a front door service like Azure Front Door to handle front-end traffic and connect to your Commerce environment.</span></span> <span data-ttu-id="558bb-163">Bu, etki alanı ve sertifika yönetimi ve daha ayrıntılı güvenlik ilkeleri üzerinde daha fazla denetim sağlar.</span><span class="sxs-lookup"><span data-stu-id="558bb-163">This provides greater control over domain and certificate management and more granular security policies.</span></span>
- <span data-ttu-id="558bb-164">Commerce tarafından sağlanan Azure Front Door örneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="558bb-164">Use the Commerce-supplied Azure Front Door instance.</span></span> <span data-ttu-id="558bb-165">Bu, etki alanı doğrulaması için Dynamics 365 Commerce ekibi ile eşgüdümlü eylemi ve üretim etki alanınız için SSL sertifikaları elde etmeyi gerektirir.</span><span class="sxs-lookup"><span data-stu-id="558bb-165">This requires coordinating action with the Dynamics 365 Commerce team for domain verification and obtaining SSL certificates for your production domain.</span></span>

<span data-ttu-id="558bb-166">CDN hizmetinin doğrudan nasıl kurulacağı hakkında bilgi için, bkz. [İçerik teslim ağı (CDN) için destek ekleme](add-cdn-support.md).</span><span class="sxs-lookup"><span data-stu-id="558bb-166">For information about how to set up a CDN service directly, see [Add support for a content delivery network (CDN)](add-cdn-support.md).</span></span>

<span data-ttu-id="558bb-167">Commerce tarafından sağlanan Azure Front Door örneğini kullanmak için, Commerce katılım ekibinden CDN kurulum için bir servis isteği oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="558bb-167">To use the Commerce-supplied Azure Front Door instance, you must create a service request for CDN setup assistance from the Commerce onboarding team.</span></span> 

- <span data-ttu-id="558bb-168">Şirket adınızı, üretim etki alanınızı, ortam kimliğini ve üretim e-ticaret kiracı adını sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="558bb-168">You will need to provide your company name, the production domain, environment ID, and production e-Commerce tenant name.</span></span> 
- <span data-ttu-id="558bb-169">Bunun var olan bir etki alanı (halen etkin bir site için kullanılan) veya yeni bir etki alanı olup olmadığı onaylamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="558bb-169">You will need to confirm if this is an existing domain (used for a currently active site) or a new domain.</span></span> 
- <span data-ttu-id="558bb-170">Yeni bir etki alanı için, etki alanı doğrulaması ve SSL sertifikası tek bir adımda elde edilebilir.</span><span class="sxs-lookup"><span data-stu-id="558bb-170">For a new domain, the domain verification and SSL certificate can be achieved in a single step.</span></span> 
- <span data-ttu-id="558bb-171">Var olan bir web sitesine hizmet veren bir etki alanı için, etki alanı doğrulaması ve SSL sertifikası oluşturmak için çok adımlı bir işlem gerekir.</span><span class="sxs-lookup"><span data-stu-id="558bb-171">For a domain serving an existing website, there is a multistep process required to establish the domain verification and SSL certificate.</span></span> <span data-ttu-id="558bb-172">Bu işlemde; birden çok sıralı adım içerdiği için, bir etki alanının canlıya geçmesi 7 çalışma günlük hizmet düzeyi anlaşması (SLA) vardır.</span><span class="sxs-lookup"><span data-stu-id="558bb-172">This process has a 7-working-day service level agreement (SLA) for a domain to go live, because it includes multiple sequential steps.</span></span>

<span data-ttu-id="558bb-173">LCS içinde bir servis talebi oluşturmak için, ortamınızda **Destek \> Destek sorunları** bölümüne gidin ve **Bir olay gönderin** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="558bb-173">To create a service request in LCS, within your environment go to **Support \> Support issues** and select **Submit an incident**.</span></span>

> [!NOTE]
> <span data-ttu-id="558bb-174">SSL bulunan özel etki alanları yalnızca üretim ortamlarında desteklenir.</span><span class="sxs-lookup"><span data-stu-id="558bb-174">Custom domains with SSL are only supported on production environments.</span></span> <span data-ttu-id="558bb-175">Korumalı alan ve kullanıcı kabul testleri (UAT) gibi üretim dışı ortamlarda, web tarayıcısında yayınlanan içeriğe erişmek için Commerce tarafından oluşturulan URL'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="558bb-175">For non-production environments such as sandbox and user acceptance testing (UAT), use the Commerce-generated URL to access published content in a web browser.</span></span>

## <a name="ssl-certificate-process"></a><span data-ttu-id="558bb-176">SSL sertifikası işlemi</span><span class="sxs-lookup"><span data-stu-id="558bb-176">SSL certificate process</span></span>

<span data-ttu-id="558bb-177">Bir servis talebi oluşturulduğu zaman, Commerce ekibi aşağıdaki adımları sizinle koordine edecektir.</span><span class="sxs-lookup"><span data-stu-id="558bb-177">When a service request is filed, the Commerce team will coordinate the following steps with you.</span></span>

<span data-ttu-id="558bb-178">Yeni etki alanları için:</span><span class="sxs-lookup"><span data-stu-id="558bb-178">For new domains:</span></span>
- <span data-ttu-id="558bb-179">Commerce ekibi, Azure Front Door örneğini (Commerce barındırmalı) kurar.</span><span class="sxs-lookup"><span data-stu-id="558bb-179">The Commerce team will set up the Azure Front Door instance (Commerce-hosted).</span></span>
- <span data-ttu-id="558bb-180">Böylece Commerce ekibi özel etki alanınızı işaret etmek için CNAME kaydını sağlar.</span><span class="sxs-lookup"><span data-stu-id="558bb-180">The Commerce team will then provide the CNAME record to point your custom domain.</span></span>
- <span data-ttu-id="558bb-181">CNAME kaydı güncelleştirildikten sonra, Commerce tarafından barındırılan Azure Front Door örneği etki alanı sahipliğini doğrulayabilir ve SSL sertifikasını alabilir.</span><span class="sxs-lookup"><span data-stu-id="558bb-181">After the CNAME record is updated, the Commerce-hosted Azure Front Door instance will be able to verify the domain ownership and get the SSL certificate.</span></span>

<span data-ttu-id="558bb-182">Var olan/etkin etki alanları için:</span><span class="sxs-lookup"><span data-stu-id="558bb-182">For existing/active domains:</span></span>
- <span data-ttu-id="558bb-183">Commerce ekibi, etki alanı DNS sağlayıcınızı sağlamak üzere `afdverify.<custom-domain>` CNAME kaydının eklenmesi konusunda sizi yönlendirecektir.</span><span class="sxs-lookup"><span data-stu-id="558bb-183">The Commerce team will instruct you to add an `afdverify.<custom-domain>` CNAME record to provide to your domain DNS provider.</span></span>
- <span data-ttu-id="558bb-184">Tamamlandığında, Commerce ekibi etki alanını Azure Front Door örneğine ekler ve etki alanı için DNS'ye eklenecek ek DNS TXT kayıtlarını sağlar.</span><span class="sxs-lookup"><span data-stu-id="558bb-184">When complete, the Commerce team will add the domain to the Azure Front Door instance and provide additional DNS TXT records to be added to the DNS for the domain.</span></span>
- <span data-ttu-id="558bb-185">TXT kayıtları tamamlandıktan sonra, Commerce ekibi SSL sertifikasının kurulacağı etki alanı için Azure Front Door güncelleştirmelerini tamamlayacaktır.</span><span class="sxs-lookup"><span data-stu-id="558bb-185">After the TXT records are completed, the Commerce team will complete the Azure Front Door updates for the domain that will set up the SSL certificate.</span></span>

## <a name="apex-domains"></a><span data-ttu-id="558bb-186">Zirve etki alanları</span><span class="sxs-lookup"><span data-stu-id="558bb-186">Apex domains</span></span>

<span data-ttu-id="558bb-187">Commerce tarafından sağlanan Azure Front Door örneği zirve etki alanlarını (alt etki alanı içermeyen kök etki alanları) desteklemez.</span><span class="sxs-lookup"><span data-stu-id="558bb-187">The Commerce-supplied Azure Front Door instance does not support apex domains (root domains that do not contain subdomains).</span></span> <span data-ttu-id="558bb-188">Zirve etki alanları çözümlemek için bir IP adresi gerektirir ve Commerce Azure Front Door örneği yalnızca sanal uç noktalarda bulunur.</span><span class="sxs-lookup"><span data-stu-id="558bb-188">Apex domains require an IP address to resolve, and the Commerce Azure Front Door instance exists with virtual endpoints only.</span></span> <span data-ttu-id="558bb-189">Zirve bir etki alanı kullanmak için iki seçeneğiniz vardır:</span><span class="sxs-lookup"><span data-stu-id="558bb-189">To use an apex domain, you have two options:</span></span>

- <span data-ttu-id="558bb-190">**Seçenek 1:** Zirve etki alanını bir "www" etki alanına yönlendirmek için DNS sağlayıcınızı kullanın.</span><span class="sxs-lookup"><span data-stu-id="558bb-190">**Option 1** - Use your DNS provider to redirect the apex domain to a "www" domain.</span></span> <span data-ttu-id="558bb-191">Örneğin, `www.fabrikam.com` Commerce tarafından barındırılan Azure Front Door örneğine işaret eden CNAME kaydının olduğu `www.fabrikam.com` adresine yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="558bb-191">For example, fabrikam.com redirects to `www.fabrikam.com` where `www.fabrikam.com` is the CNAME record that points to the Commerce-hosted Azure Front Door instance.</span></span>

- <span data-ttu-id="558bb-192">**Seçenek 2:** Zirve etki alanını barındırmak için kendi kendinize bir CDN/Front Door örneği kurun.</span><span class="sxs-lookup"><span data-stu-id="558bb-192">**Option 2** - Set up a CDN/front door instance on your own to host the apex domain.</span></span>

> [!NOTE]
> <span data-ttu-id="558bb-193">Azure Front Door kullanıyorsanız, aynı abonelikte bir Azure DNS'yi de ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="558bb-193">If you are using Azure Front Door, you must also set up an Azure DNS in the same subscription.</span></span> <span data-ttu-id="558bb-194">Azure DNS'de barındırılan zirve etki alanı, bir diğer ad kaydı olarak Azure Front Door hizmetine işaret edebilir.</span><span class="sxs-lookup"><span data-stu-id="558bb-194">The apex domain hosted on Azure DNS can point to your Azure Front Door as an alias record.</span></span> <span data-ttu-id="558bb-195">Bu, zirve etki alanlarının her zaman bir IP adresine işaret etmesi gerektiğinden geçici bir çözümdür.</span><span class="sxs-lookup"><span data-stu-id="558bb-195">This is the only work around, as apex domains must always point to an IP address.</span></span>

  ## <a name="additional-resources"></a><span data-ttu-id="558bb-196">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="558bb-196">Additional resources</span></span>

  [<span data-ttu-id="558bb-197">Yeni e-Ticaret sitesini dağıtma</span><span class="sxs-lookup"><span data-stu-id="558bb-197">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

  [<span data-ttu-id="558bb-198">Çevrimiçi mağaza kanalı ayarlama</span><span class="sxs-lookup"><span data-stu-id="558bb-198">Set up an online store channel</span></span>](online-stores.md)

  [<span data-ttu-id="558bb-199">e-Ticaret sitesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="558bb-199">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

  [<span data-ttu-id="558bb-200">Çevrimiçi siteyi bir kanalla ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="558bb-200">Associate an online site with a channel</span></span>](associate-site-online-store.md)

  [<span data-ttu-id="558bb-201">robots.txt dosyalarını yönetme</span><span class="sxs-lookup"><span data-stu-id="558bb-201">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

  [<span data-ttu-id="558bb-202">URL yeniden yönlendirmelerini toplu olarak yükleme</span><span class="sxs-lookup"><span data-stu-id="558bb-202">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

  [<span data-ttu-id="558bb-203">Commerce'ta B2C kiracısı ayarlama</span><span class="sxs-lookup"><span data-stu-id="558bb-203">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

  [<span data-ttu-id="558bb-204">Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama</span><span class="sxs-lookup"><span data-stu-id="558bb-204">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

  [<span data-ttu-id="558bb-205">Commerce ortamında birden fazla B2C kiracısı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="558bb-205">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

  [<span data-ttu-id="558bb-206">İçerik teslim ağı (CDN) için destek ekleme</span><span class="sxs-lookup"><span data-stu-id="558bb-206">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

  [<span data-ttu-id="558bb-207">Konum tabanlı mağaza algılamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="558bb-207">Enable location-based store detection</span></span>](enable-store-detection.md)
