---
title: İçerik teslim ağı (CDN) için destek ekleme
description: Bu konuda, Microsoft Dynamics 365 Commerce ortamınıza bir içerik teslim ağının (CDN) nasıl ekleneceği açıklanmaktadır.
author: brianshook
manager: annbe
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1d9482a45cb8f2ea52e7f58d55e30cfe56694d04
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985966"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="e9895-103">İçerik teslim ağı (CDN) için destek ekleme</span><span class="sxs-lookup"><span data-stu-id="e9895-103">Add support for a content delivery network (CDN)</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="e9895-104">Bu konuda, Microsoft Dynamics 365 Commerce ortamınıza bir içerik teslim ağının (CDN) nasıl ekleneceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="e9895-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

## <a name="overview"></a><span data-ttu-id="e9895-105">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="e9895-105">Overview</span></span>

<span data-ttu-id="e9895-106">Dynamics 365 Commerce uygulamasında bir e-ticaret ortamı kurduğunuzda, bunu CDN hizmetiyle çalışacak şekilde konfigüre edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e9895-106">When you set up an e-commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="e9895-107">Özel etki alanınız e-ticaret ortamınız için sağlama işlemi sırasında etkinleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="e9895-107">Your custom domain can be enabled during the provisioning process for your e-commerce environment.</span></span> <span data-ttu-id="e9895-108">Alternatif olarak, bir servis talebini, sağlama işlemi tamamlandıktan sonra ayarlamak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e9895-108">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="e9895-109">E-ticaret ortamı için sağlama işlemi, ortamla ilişkilendirilmiş bir ana bilgisayar adı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e9895-109">The provisioning process for the e-commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="e9895-110">Bu ana bilgisayar adının aşağıdaki biçimi vardır; burada \<*e-commerce-tenant-name*\> ortamınızın adıdır:</span><span class="sxs-lookup"><span data-stu-id="e9895-110">This host name has the following format, where \<*e-commerce-tenant-name*\> is the name of your environment:</span></span>

<span data-ttu-id="e9895-111">&lt;e-ticaret-kiracı-adı&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="e9895-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="e9895-112">Sağlama işlemi sırasında oluşturulan ana bilgisayar adı veya bitiş noktası, yalnızca. \*commerce.dynamics.com için bir güvenli yuva katmanı (SSL) sertifikasını destekler.</span><span class="sxs-lookup"><span data-stu-id="e9895-112">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="e9895-113">Özel etki alanları için SSL'yi desteklemez.</span><span class="sxs-lookup"><span data-stu-id="e9895-113">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="e9895-114">Bu nedenle, CDN'den özel etki alanları için SSL'yi sonlandırmalı ve CDN'den Commerce'in ürettiği ana bilgisayar adına veya bitiş noktasına iletme trafiğine son vermek zorundasınız.</span><span class="sxs-lookup"><span data-stu-id="e9895-114">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="e9895-115">Ek olarak, Commerce *statikleri* (JavaScript veya geçişli stil sayfaları \[CSS\] dosyaları) Commerce tarafından üretilen bitiş noktasından (\*.commerce.dynamics.com) sunulur.</span><span class="sxs-lookup"><span data-stu-id="e9895-115">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="e9895-116">Statikler, yalnızca Commerce tarafından oluşturulan ana bilgisayar adı veya bitiş noktası CDN'nin arkasına konulursa önbelleğe alınabilir.</span><span class="sxs-lookup"><span data-stu-id="e9895-116">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="e9895-117">SSL'yi ayarlama</span><span class="sxs-lookup"><span data-stu-id="e9895-117">Set up SSL</span></span>

<span data-ttu-id="e9895-118">SSL'nin ayarlandığını ve bu tür önbelleğe alınmış olduğunu garantilemek için, CDN'nizi, ortamınız için ticaret tarafından üretilen ana bilgisayar adıyla ilişkilendirilmiş olacak şekilde konfigüre etmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="e9895-118">To help guarantee that SSL is set up, and that statics are cached, you must configure your CDN so that it is associated with the host name that Commerce generated for your environment.</span></span> <span data-ttu-id="e9895-119">Ayrıca, yalnızca statiği için aşağıdaki kalıbı da önbelleğe almalısınız:</span><span class="sxs-lookup"><span data-stu-id="e9895-119">You must also cache the following pattern for statics only:</span></span> 

<span data-ttu-id="e9895-120">/\_msdyn365/\_scnr/\*</span><span class="sxs-lookup"><span data-stu-id="e9895-120">/\_msdyn365/\_scnr/\*</span></span>

<span data-ttu-id="e9895-121">Sağlanan özel etki alanı ile Commerce ortamınızı hazırladıktan sonra veya hizmet isteği kullanarak ortamınız için özel etki alanı sağlamadıktan sonra, özel etki alanınızı Commerce'in oluşturduğu ana bilgisayar adına veya bitiş noktasına getirin.</span><span class="sxs-lookup"><span data-stu-id="e9895-121">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, point your custom domain to the host name or endpoint that Commerce generated.</span></span>

<span data-ttu-id="e9895-122">Daha önce belirtildiği gibi, oluşturulan ana bilgisayar adı veya bitiş noktası yalnızca \*.commerce.dynamics.com için bir SSL sertifikasını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="e9895-122">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="e9895-123">Özel etki alanları için SSL'yi desteklemez.</span><span class="sxs-lookup"><span data-stu-id="e9895-123">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="e9895-124">CDN hizmetleri</span><span class="sxs-lookup"><span data-stu-id="e9895-124">CDN services</span></span>

<span data-ttu-id="e9895-125">Herhangi bir CDN hizmeti, bir Commerce ortamıyla kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e9895-125">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="e9895-126">Burada iki örnek verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="e9895-126">Here are two examples:</span></span>

- <span data-ttu-id="e9895-127">**Microsoft Azure Ön kapı hizmeti** – Azure CDN çözümü.</span><span class="sxs-lookup"><span data-stu-id="e9895-127">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="e9895-128">Azure ön kapı hizmeti hakkında daha fazla bilgi için [Azure ön kapı hizmeti belgelerine](https://docs.microsoft.com/azure/frontdoor/) bakın.</span><span class="sxs-lookup"><span data-stu-id="e9895-128">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="e9895-129">**Akamai dinamik sitesi Hızlandırıcısı** – daha fazla bilgi için bkz. [Dinamik Site Hızlandırıcısı](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="e9895-129">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="e9895-130">CDN kurulumu</span><span class="sxs-lookup"><span data-stu-id="e9895-130">CDN setup</span></span>

<span data-ttu-id="e9895-131">CDN kurulum işlemi aşağıdaki adımlardan oluşur:</span><span class="sxs-lookup"><span data-stu-id="e9895-131">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="e9895-132">Ön uç ana bilgisayar ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e9895-132">Add a front-end host.</span></span>
1. <span data-ttu-id="e9895-133">Bir arka uç havuzu yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="e9895-133">Configure a backend pool.</span></span>
1. <span data-ttu-id="e9895-134">Rota ve ön belleğe alma kurallarını ayarla.</span><span class="sxs-lookup"><span data-stu-id="e9895-134">Set up rules for routing and caching.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="e9895-135">Ön uç ana bilgisayar ekleyin</span><span class="sxs-lookup"><span data-stu-id="e9895-135">Add a front-end host</span></span>

<span data-ttu-id="e9895-136">Tüm CDN hizmetleri kullanılabilir, ancak bu konudaki örnek için Azure ön kapı hizmeti kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e9895-136">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="e9895-137">Azure ön kapı hizmeti'ni kurma hakkında bilgi için bkz. [Hızlı başlangıç: yüksek oranda kullanılabilir bir Global Web uygulaması için ön kapı oluşturun.](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door)</span><span class="sxs-lookup"><span data-stu-id="e9895-137">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a><span data-ttu-id="e9895-138">Azure Front Door Service'te bir arka uç havuzu yapılandırın</span><span class="sxs-lookup"><span data-stu-id="e9895-138">Configure a backend pool in Azure Front Door Service</span></span>

<span data-ttu-id="e9895-139">Azure Front Door Service'te bir arka uç havuzu yapılandırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e9895-139">To configure a backend pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="e9895-140">Arka uç havuzuna boş arka uç ana bilgisayar üst bilgisi olan özel bir ana bilgisayar olarak **&lt;ecom-kiraci-adi&gt;.commerce.dynamics.com** ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e9895-140">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a backend pool as a custom host that has an empty backend host header.</span></span>
1. <span data-ttu-id="e9895-141">**Yük dengelemesi** altında, varsayılan değerleri bırakın.</span><span class="sxs-lookup"><span data-stu-id="e9895-141">Under **Load balancing**, leave the default values.</span></span>

<span data-ttu-id="e9895-142">Aşağıdaki resimde, Azure Front Door Service'te arka uç ana bilgisayar adı girilmiş halde **Bir arka uç ekle** iletişim kutusu gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="e9895-142">The following illustration shows the **Add a backend** dialog box in Azure Front Door Service with the backend host name entered.</span></span>

![Arka uç havuzu iletişim kutusu Ekle](./media/CDN_BackendPool.png)

<span data-ttu-id="e9895-144">Aşağıdaki resimde, Azure Front Door Service'te varsayılan yük dengeleme değerleriyle birlikte **Bir arka uç havuzu ekle** iletişim kutusu gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="e9895-144">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service with the default load balancing values.</span></span>

![Arka uç havuzu iletişim kutusu ekle devamı](./media/CDN_BackendPool_2.png)

### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="e9895-146">Azure ön kapı hizmeti'nde kuralları ayarla</span><span class="sxs-lookup"><span data-stu-id="e9895-146">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="e9895-147">Azure ön kapı hizmeti'nde bir yönlendirme kuralı ayarlamak için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e9895-147">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="e9895-148">Rota kuralı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e9895-148">Add a routing rule.</span></span>
1. <span data-ttu-id="e9895-149">**Ad** alanına, **varsayılan** yazın.</span><span class="sxs-lookup"><span data-stu-id="e9895-149">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="e9895-150">**Kabul edilen iletişim kuralı** alanında, **http ve https**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e9895-150">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="e9895-151">**Ön uç ana bilgisayarlar** alanında, **dynamics-ecom-tenant-name.azurefd.net** girin.</span><span class="sxs-lookup"><span data-stu-id="e9895-151">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="e9895-152">**Eşleştirilecek desenler** altında, üst alana şunu girin: \**/\** _.</span><span class="sxs-lookup"><span data-stu-id="e9895-152">Under **Patterns to match**, in the upper field, enter \**/\** _.</span></span>
1. <span data-ttu-id="e9895-153">_*Rota Ayrıntıları*\* altında, **rota türü** seçeneğini **ileri** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e9895-153">Under _\*Route Details\*\*, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="e9895-154">**Arka uç havuzu** alanında, **ecom-arka uç**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e9895-154">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="e9895-155">**İletme Protokolü** alan grubunda, **isteği eşleştir** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="e9895-155">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="e9895-156">**URL yeniden yazma** seçeneğini **devre dışı** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e9895-156">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="e9895-157">**Önbelleğe alma** seçeneğini **devre dışı** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e9895-157">Set the **Caching** option to **Disabled**.</span></span>

<span data-ttu-id="e9895-158">Azure ön kapı hizmeti'nde bir önbelleğe alma kuralı ayarlamak için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e9895-158">To set up a caching rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="e9895-159">Önbelleğe alma kuralı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e9895-159">Add a caching rule.</span></span>
1. <span data-ttu-id="e9895-160">**Ad** alanına, **statikler** yazın.</span><span class="sxs-lookup"><span data-stu-id="e9895-160">In the **Name** field, enter **statics**.</span></span>
1. <span data-ttu-id="e9895-161">**Kabul edilen iletişim kuralı** alanında, **http ve https**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e9895-161">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="e9895-162">**Ön uç ana bilgisayarlar** alanında, **dynamics-ecom-tenant-name.azurefd.net** girin.</span><span class="sxs-lookup"><span data-stu-id="e9895-162">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="e9895-163">**Eşleştirilecek desenler** altında, üst alana şunu girin: \**/\_msdyn365/\_scnr/\** _.</span><span class="sxs-lookup"><span data-stu-id="e9895-163">Under **Patterns to match**, in the upper field, \**/\_msdyn365/\_scnr/\** _.</span></span>
1. <span data-ttu-id="e9895-164">_*Rota Ayrıntıları*\* altında, **rota türü** seçeneğini **ileri** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e9895-164">Under _\*Route Details\*\*, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="e9895-165">**Arka uç havuzu** alanında, **ecom-arka uç**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e9895-165">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="e9895-166">**İletme Protokolü** alan grubunda, **isteği eşleştir** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="e9895-166">In the **Forwarding protocol** field group, select the **Match request** option.</span></span>
1. <span data-ttu-id="e9895-167">**URL yeniden yazma** seçeneğini **devre dışı** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e9895-167">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="e9895-168">**Önbelleğe alma** seçeneğini **devre dışı** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e9895-168">Set the **Caching** option to **Disabled**.</span></span>
1. <span data-ttu-id="e9895-169">**Sorgu dizesi önbelleğe alma davranışı** alanında, **her benzersiz URL 'yi önbelleğe al** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e9895-169">In the **Query string caching behavior** field, select **Cache every unique URL**.</span></span>
1. <span data-ttu-id="e9895-170">**Dinamik sıkıştırma** alan grubunda, **etkin** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="e9895-170">In the **Dynamic compression** field group, select the **Enabled** option.</span></span>

<span data-ttu-id="e9895-171">Aşağıdaki resimde, Azure ön kapı hizmeti'ndeki **bir kural Ekle** iletişim kutusu gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="e9895-171">The following illustration shows the **Add a rule** dialog box in Azure Front Door Service.</span></span>

![Kural Ekle iletişim kutusu](./media/CDN_CachingRule.png)

> [!WARNING]
> <span data-ttu-id="e9895-173">Kullanacağınız etki alanı zaten etkin ve yayında ise, sonraki adımlarınız için yardım almak üzere, [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/)'teki **Destek** kutucuğunda bir destek bileti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e9895-173">If the domain that you will use is already active and live, create a support ticket from the **Support** tile in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) to get assistance for your next steps.</span></span> <span data-ttu-id="e9895-174">Daha fazla bilgi için bkz. [Finance and Operations uygulamaları veya Lifecycle Services (LCS) için destek alma](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="e9895-174">For more information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

<span data-ttu-id="e9895-175">Etki alanınız yeniyse ve önceden varolan yayındaki bir etki alanı değilse, özel etki alanınızı Azure Front Door Service yapılandırmasına ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e9895-175">If your domain is new and is not a pre-existing live domain, you can add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="e9895-176">Bu, Azure Front Door örneği aracılığıyla web trafiğini sitenize yönlendirmeyi sağlar.</span><span class="sxs-lookup"><span data-stu-id="e9895-176">This will enable web traffic to direct to your site via the Azure Front Door instance.</span></span> <span data-ttu-id="e9895-177">Özel etki alanı eklemek için (örneğin `www.fabrikam.com`), etki alanı için kurallı bir ad (CNAME) yapılandırmalısınız.</span><span class="sxs-lookup"><span data-stu-id="e9895-177">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="e9895-178">Aşağıdaki resimde, Azure ön kapı hizmeti'ndeki **CNAME yapılandırması** iletişim kutusu gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="e9895-178">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![CNAME Konfigürasyon iletişim kutusu](./media/CNAME_Configuration.png)

<span data-ttu-id="e9895-180">Sertifikayı yönetmek için Azure ön kapı hizmetini kullanabilir veya özel etki alanı için kendi sertifikanızı kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e9895-180">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="e9895-181">Aşağıdaki resimde, Azure ön kapı hizmeti'ndeki **Özel alan HTTPS** iletişim kutusu gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="e9895-181">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![Özel etki alanı HTTPS iletişim kutusu](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="e9895-183">Azure Front Door'unuza özel etki alanı eklemeyle ilgili ayrıntılı yönergeler için bkz. [Front Door'a özel etki alanı ekleme](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span><span class="sxs-lookup"><span data-stu-id="e9895-183">For detailed instructions on adding a custom domain to your Azure Front Door, see [Add a custom domain to your Front Door](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span></span>

<span data-ttu-id="e9895-184">CDN'niz şimdi Commerce sitenizde kullanılabilecek şekilde doğru konfigüre edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="e9895-184">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e9895-185">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="e9895-185">Additional resources</span></span>

[<span data-ttu-id="e9895-186">Etki alanı adınızı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="e9895-186">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="e9895-187">Yeni bir e-ticaret kiracısını dağıtma</span><span class="sxs-lookup"><span data-stu-id="e9895-187">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="e9895-188">E-ticaret sitesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="e9895-188">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="e9895-189">Dynamics 365 Commerce sitesini çevrimiçi bir kanalla ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="e9895-189">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="e9895-190">robots.txt dosyalarını yönetme</span><span class="sxs-lookup"><span data-stu-id="e9895-190">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="e9895-191">URL yeniden yönlendirmelerini toplu olarak yükleme</span><span class="sxs-lookup"><span data-stu-id="e9895-191">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="e9895-192">Commerce'ta B2C kiracısı ayarlama</span><span class="sxs-lookup"><span data-stu-id="e9895-192">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="e9895-193">Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama</span><span class="sxs-lookup"><span data-stu-id="e9895-193">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="e9895-194">Commerce ortamında birden fazla B2C kiracısı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="e9895-194">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="e9895-195">Konum tabanlı mağaza algılamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="e9895-195">Enable location-based store detection</span></span>](enable-store-detection.md)
