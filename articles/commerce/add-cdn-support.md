---
title: İçerik teslim ağı (CDN) için destek ekleme
description: Bu konuda, Microsoft Dynamics 365 Commerce ortamınıza bir içerik teslim ağının (CDN) nasıl ekleneceği açıklanmaktadır.
author: brianshook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a56f675b1fb43160625101a067c74e9fcf4f714a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797851"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="6c433-103">İçerik teslim ağı (CDN) için destek ekleme</span><span class="sxs-lookup"><span data-stu-id="6c433-103">Add support for a content delivery network (CDN)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6c433-104">Bu konuda, Microsoft Dynamics 365 Commerce ortamınıza bir içerik teslim ağının (CDN) nasıl ekleneceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="6c433-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="6c433-105">Dynamics 365 Commerce uygulamasında bir e-ticaret ortamı kurduğunuzda, bunu CDN hizmetiyle çalışacak şekilde konfigüre edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6c433-105">When you set up an e-commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="6c433-106">Özel etki alanınız e-ticaret ortamınız için sağlama işlemi sırasında etkinleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="6c433-106">Your custom domain can be enabled during the provisioning process for your e-commerce environment.</span></span> <span data-ttu-id="6c433-107">Alternatif olarak, bir servis talebini, sağlama işlemi tamamlandıktan sonra ayarlamak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6c433-107">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="6c433-108">E-ticaret ortamı için sağlama işlemi, ortamla ilişkilendirilmiş bir ana bilgisayar adı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6c433-108">The provisioning process for the e-commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="6c433-109">Bu ana bilgisayar adının aşağıdaki biçimi vardır; burada \<*e-commerce-tenant-name*\> ortamınızın adıdır:</span><span class="sxs-lookup"><span data-stu-id="6c433-109">This host name has the following format, where \<*e-commerce-tenant-name*\> is the name of your environment:</span></span>

<span data-ttu-id="6c433-110">&lt;e-ticaret-kiracı-adı&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="6c433-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="6c433-111">Sağlama işlemi sırasında oluşturulan ana bilgisayar adı veya bitiş noktası, yalnızca. \*commerce.dynamics.com için bir güvenli yuva katmanı (SSL) sertifikasını destekler.</span><span class="sxs-lookup"><span data-stu-id="6c433-111">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="6c433-112">Özel etki alanları için SSL'yi desteklemez.</span><span class="sxs-lookup"><span data-stu-id="6c433-112">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="6c433-113">Bu nedenle, CDN'den özel etki alanları için SSL'yi sonlandırmalı ve CDN'den Commerce'in ürettiği ana bilgisayar adına veya bitiş noktasına iletme trafiğine son vermek zorundasınız.</span><span class="sxs-lookup"><span data-stu-id="6c433-113">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="6c433-114">Ek olarak, Commerce *statikleri* (JavaScript veya geçişli stil sayfaları \[CSS\] dosyaları) Commerce tarafından üretilen bitiş noktasından (\*.commerce.dynamics.com) sunulur.</span><span class="sxs-lookup"><span data-stu-id="6c433-114">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="6c433-115">Statikler, yalnızca Commerce tarafından oluşturulan ana bilgisayar adı veya bitiş noktası CDN'nin arkasına konulursa önbelleğe alınabilir.</span><span class="sxs-lookup"><span data-stu-id="6c433-115">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="6c433-116">SSL'u ayarla</span><span class="sxs-lookup"><span data-stu-id="6c433-116">Set up SSL</span></span>

<span data-ttu-id="6c433-117">Sağlanan özel etki alanı ile Commerce ortamınızı hazırladıktan sonra veya hizmet isteği kullanarak ortamınız için özel etki alanı sağladıktan sonra, DNS değişikliklerini planlamak için Commerce işe alım ekibiyle birlikte çalışmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="6c433-117">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, you need to work with the Commerce onboarding team to plan the DNS changes.</span></span>

<span data-ttu-id="6c433-118">Daha önce belirtildiği gibi, oluşturulan ana bilgisayar adı veya bitiş noktası yalnızca \*.commerce.dynamics.com için bir SSL sertifikasını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="6c433-118">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="6c433-119">Özel etki alanları için SSL'yi desteklemez.</span><span class="sxs-lookup"><span data-stu-id="6c433-119">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="6c433-120">CDN hizmetleri</span><span class="sxs-lookup"><span data-stu-id="6c433-120">CDN services</span></span>

<span data-ttu-id="6c433-121">Herhangi bir CDN hizmeti, bir Commerce ortamıyla kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6c433-121">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="6c433-122">Burada iki örnek verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="6c433-122">Here are two examples:</span></span>

- <span data-ttu-id="6c433-123">**Microsoft Azure Ön kapı hizmeti** – Azure CDN çözümü.</span><span class="sxs-lookup"><span data-stu-id="6c433-123">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="6c433-124">Azure ön kapı hizmeti hakkında daha fazla bilgi için [Azure ön kapı hizmeti belgelerine](https://docs.microsoft.com/azure/frontdoor/) bakın.</span><span class="sxs-lookup"><span data-stu-id="6c433-124">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="6c433-125">**Akamai dinamik sitesi Hızlandırıcısı** – daha fazla bilgi için bkz. [Dinamik Site Hızlandırıcısı](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="6c433-125">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="6c433-126">CDN kurulumu</span><span class="sxs-lookup"><span data-stu-id="6c433-126">CDN setup</span></span>

<span data-ttu-id="6c433-127">CDN kurulum işlemi aşağıdaki adımlardan oluşur:</span><span class="sxs-lookup"><span data-stu-id="6c433-127">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="6c433-128">Ön uç ana bilgisayar ekleyin.</span><span class="sxs-lookup"><span data-stu-id="6c433-128">Add a front-end host.</span></span>
1. <span data-ttu-id="6c433-129">Bir arka uç havuzu yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="6c433-129">Configure a backend pool.</span></span>
1. <span data-ttu-id="6c433-130">Yönlendirme için kural ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6c433-130">Set up rules for routing.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="6c433-131">Ön uç ana bilgisayar ekleyin</span><span class="sxs-lookup"><span data-stu-id="6c433-131">Add a front-end host</span></span>

<span data-ttu-id="6c433-132">Tüm CDN hizmetleri kullanılabilir, ancak bu konudaki örnek için Azure ön kapı hizmeti kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6c433-132">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="6c433-133">Azure ön kapı hizmeti'ni kurma hakkında bilgi için bkz. [Hızlı başlangıç: yüksek oranda kullanılabilir bir Global Web uygulaması için ön kapı oluşturun.](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door)</span><span class="sxs-lookup"><span data-stu-id="6c433-133">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a><span data-ttu-id="6c433-134">Azure Front Door Service'te bir arka uç havuzu yapılandırın</span><span class="sxs-lookup"><span data-stu-id="6c433-134">Configure a backend pool in Azure Front Door Service</span></span>

<span data-ttu-id="6c433-135">Azure Front Door Service'te bir arka uç havuzu yapılandırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="6c433-135">To configure a backend pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="6c433-136">**&lt;ecom-tenant-name&gt;.commerce.dynamics.com** öğesini, **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** ile aynı arka uç ana bilgisayar başlığına sahip özel bir ana bilgisayar olarak arka uç havuzuna ekleyin.</span><span class="sxs-lookup"><span data-stu-id="6c433-136">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a backend pool as a custom host that has a backend host header that is the same as **&lt;ecom-tenant-name&gt;.commerce.dynamics.com**.</span></span>
1. <span data-ttu-id="6c433-137">**Yük dengelemesi** altında, varsayılan değerleri bırakın.</span><span class="sxs-lookup"><span data-stu-id="6c433-137">Under **Load balancing**, leave the default values.</span></span>
1. <span data-ttu-id="6c433-138">Arka uç havuzu için sistem durumu denetimlerini devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="6c433-138">Disable health checks for the backend pool.</span></span>

<span data-ttu-id="6c433-139">Aşağıdaki resimde, Azure Front Door Service'te arka uç ana bilgisayar adı girilmiş halde **Bir arka uç ekle** iletişim kutusu gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="6c433-139">The following illustration shows the **Add a backend** dialog box in Azure Front Door Service with the backend host name entered.</span></span>

![Arka uç havuzu iletişim kutusu Ekle](./media/CDN_BackendPool.png)

<span data-ttu-id="6c433-141">Aşağıdaki resimde, Azure Front Door Service'te varsayılan yük dengeleme değerleriyle birlikte **Bir arka uç havuzu ekle** iletişim kutusu gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="6c433-141">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service with the default load balancing values.</span></span>

![Arka uç havuzu iletişim kutusu ekle devamı](./media/CDN_BackendPool_2.png)

> [!NOTE]
> <span data-ttu-id="6c433-143">Commerce için kendi Azure Front Door Service'inizi kurarken **sistem durumu araştırmalarının** devre dışı olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="6c433-143">Be sure to disable **Health Probes** when setting up your own Azure Front Door service for Commerce.</span></span>


### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="6c433-144">Azure ön kapı hizmeti'nde kuralları ayarla</span><span class="sxs-lookup"><span data-stu-id="6c433-144">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="6c433-145">Azure ön kapı hizmeti'nde bir yönlendirme kuralı ayarlamak için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="6c433-145">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="6c433-146">Rota kuralı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="6c433-146">Add a routing rule.</span></span>
1. <span data-ttu-id="6c433-147">**Ad** alanına, **varsayılan** yazın.</span><span class="sxs-lookup"><span data-stu-id="6c433-147">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="6c433-148">**Kabul edilen iletişim kuralı** alanında, **http ve https**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6c433-148">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="6c433-149">**Ön uç ana bilgisayarlar** alanında, **dynamics-ecom-tenant-name.azurefd.net** girin.</span><span class="sxs-lookup"><span data-stu-id="6c433-149">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="6c433-150">**Eşleştirilecek desenler** altında, üst alana şunu girin: **/\***.</span><span class="sxs-lookup"><span data-stu-id="6c433-150">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="6c433-151">**Rota Ayrıntıları** altında, **rota türü** seçeneğini **ileri** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6c433-151">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="6c433-152">**Arka uç havuzu** alanında, **ecom-arka uç**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6c433-152">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="6c433-153">**İletme Protokolü** alan grubunda, **isteği eşleştir** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="6c433-153">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="6c433-154">**URL yeniden yazma** seçeneğini **devre dışı** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6c433-154">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="6c433-155">**Önbelleğe alma** seçeneğini **devre dışı** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6c433-155">Set the **Caching** option to **Disabled**.</span></span>


> [!WARNING]
> <span data-ttu-id="6c433-156">Kullanacağınız etki alanı zaten etkin ve yayında ise, sonraki adımlarınız için yardım almak üzere, [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/)'teki **Destek** kutucuğunda bir destek bileti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="6c433-156">If the domain that you will use is already active and live, create a support ticket from the **Support** tile in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) to get assistance for your next steps.</span></span> <span data-ttu-id="6c433-157">Daha fazla bilgi için bkz. [Finance and Operations uygulamaları veya Lifecycle Services (LCS) için destek alma](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="6c433-157">For more information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

<span data-ttu-id="6c433-158">Etki alanınız yeniyse ve önceden varolan yayındaki bir etki alanı değilse, özel etki alanınızı Azure Front Door Service yapılandırmasına ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6c433-158">If your domain is new and is not a pre-existing live domain, you can add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="6c433-159">Bu, Azure Front Door örneği aracılığıyla web trafiğini sitenize yönlendirmeyi sağlar.</span><span class="sxs-lookup"><span data-stu-id="6c433-159">This will enable web traffic to direct to your site via the Azure Front Door instance.</span></span> <span data-ttu-id="6c433-160">Özel etki alanı eklemek için (örneğin `www.fabrikam.com`), etki alanı için kurallı bir ad (CNAME) yapılandırmalısınız.</span><span class="sxs-lookup"><span data-stu-id="6c433-160">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="6c433-161">Aşağıdaki resimde, Azure ön kapı hizmeti'ndeki **CNAME yapılandırması** iletişim kutusu gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="6c433-161">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![CNAME Konfigürasyon iletişim kutusu](./media/CNAME_Configuration.png)

<span data-ttu-id="6c433-163">Sertifikayı yönetmek için Azure ön kapı hizmetini kullanabilir veya özel etki alanı için kendi sertifikanızı kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6c433-163">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="6c433-164">Aşağıdaki resimde, Azure ön kapı hizmeti'ndeki **Özel alan HTTPS** iletişim kutusu gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="6c433-164">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![Özel etki alanı HTTPS iletişim kutusu](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="6c433-166">Azure Front Door'unuza özel etki alanı eklemeyle ilgili ayrıntılı yönergeler için bkz. [Front Door'a özel etki alanı ekleme](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span><span class="sxs-lookup"><span data-stu-id="6c433-166">For detailed instructions on adding a custom domain to your Azure Front Door, see [Add a custom domain to your Front Door](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span></span>

<span data-ttu-id="6c433-167">CDN'niz şimdi Commerce sitenizde kullanılabilecek şekilde doğru konfigüre edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="6c433-167">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6c433-168">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="6c433-168">Additional resources</span></span>

[<span data-ttu-id="6c433-169">İçerik teslimi ağı uygulama seçenekleri</span><span class="sxs-lookup"><span data-stu-id="6c433-169">Content delivery network implementation options</span></span>](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
