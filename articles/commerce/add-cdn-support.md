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
ms.openlocfilehash: d653b072eca134c765a5db5659b228648fc13c4a
ms.sourcegitcommit: 3fe4d9a33447aa8a62d704fbbf18aeb9cb667baa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/12/2021
ms.locfileid: "5582731"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="dbd49-103">İçerik teslim ağı (CDN) için destek ekleme</span><span class="sxs-lookup"><span data-stu-id="dbd49-103">Add support for a content delivery network (CDN)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="dbd49-104">Bu konuda, Microsoft Dynamics 365 Commerce ortamınıza bir içerik teslim ağının (CDN) nasıl ekleneceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="dbd49-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="dbd49-105">Dynamics 365 Commerce uygulamasında bir e-ticaret ortamı kurduğunuzda, bunu CDN hizmetiyle çalışacak şekilde konfigüre edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dbd49-105">When you set up an e-commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="dbd49-106">Özel etki alanınız e-ticaret ortamınız için sağlama işlemi sırasında etkinleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="dbd49-106">Your custom domain can be enabled during the provisioning process for your e-commerce environment.</span></span> <span data-ttu-id="dbd49-107">Alternatif olarak, bir servis talebini, sağlama işlemi tamamlandıktan sonra ayarlamak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dbd49-107">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="dbd49-108">E-ticaret ortamı için sağlama işlemi, ortamla ilişkilendirilmiş bir ana bilgisayar adı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dbd49-108">The provisioning process for the e-commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="dbd49-109">Bu ana bilgisayar adının aşağıdaki biçimi vardır; burada \<*e-commerce-tenant-name*\> ortamınızın adıdır:</span><span class="sxs-lookup"><span data-stu-id="dbd49-109">This host name has the following format, where \<*e-commerce-tenant-name*\> is the name of your environment:</span></span>

<span data-ttu-id="dbd49-110">&lt;e-ticaret-kiracı-adı&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="dbd49-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="dbd49-111">Sağlama işlemi sırasında oluşturulan ana bilgisayar adı veya bitiş noktası, yalnızca. \*commerce.dynamics.com için bir güvenli yuva katmanı (SSL) sertifikasını destekler.</span><span class="sxs-lookup"><span data-stu-id="dbd49-111">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="dbd49-112">Özel etki alanları için SSL'yi desteklemez.</span><span class="sxs-lookup"><span data-stu-id="dbd49-112">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="dbd49-113">Bu nedenle, CDN'den özel etki alanları için SSL'yi sonlandırmalı ve CDN'den Commerce'in ürettiği ana bilgisayar adına veya bitiş noktasına iletme trafiğine son vermek zorundasınız.</span><span class="sxs-lookup"><span data-stu-id="dbd49-113">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="dbd49-114">Ek olarak, Commerce *statikleri* (JavaScript veya geçişli stil sayfaları \[CSS\] dosyaları) Commerce tarafından üretilen bitiş noktasından (\*.commerce.dynamics.com) sunulur.</span><span class="sxs-lookup"><span data-stu-id="dbd49-114">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="dbd49-115">Statikler, yalnızca Commerce tarafından oluşturulan ana bilgisayar adı veya bitiş noktası CDN'nin arkasına konulursa önbelleğe alınabilir.</span><span class="sxs-lookup"><span data-stu-id="dbd49-115">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="dbd49-116">SSL'yi ayarlama</span><span class="sxs-lookup"><span data-stu-id="dbd49-116">Set up SSL</span></span>

<span data-ttu-id="dbd49-117">SSL'nin ayarlandığını ve bu tür önbelleğe alınmış olduğunu garantilemek için, CDN'nizi, ortamınız için ticaret tarafından üretilen ana bilgisayar adıyla ilişkilendirilmiş olacak şekilde konfigüre etmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="dbd49-117">To help guarantee that SSL is set up, and that statics are cached, you must configure your CDN so that it is associated with the host name that Commerce generated for your environment.</span></span> <span data-ttu-id="dbd49-118">Ayrıca, yalnızca statiği için aşağıdaki kalıbı da önbelleğe almalısınız:</span><span class="sxs-lookup"><span data-stu-id="dbd49-118">You must also cache the following pattern for statics only:</span></span> 

<span data-ttu-id="dbd49-119">/\_msdyn365/\_scnr/\*</span><span class="sxs-lookup"><span data-stu-id="dbd49-119">/\_msdyn365/\_scnr/\*</span></span>

<span data-ttu-id="dbd49-120">Sağlanan özel etki alanı ile Commerce ortamınızı hazırladıktan sonra veya hizmet isteği kullanarak ortamınız için özel etki alanı sağlamadıktan sonra, özel etki alanınızı Commerce'in oluşturduğu ana bilgisayar adına veya bitiş noktasına getirin.</span><span class="sxs-lookup"><span data-stu-id="dbd49-120">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, point your custom domain to the host name or endpoint that Commerce generated.</span></span>

<span data-ttu-id="dbd49-121">Daha önce belirtildiği gibi, oluşturulan ana bilgisayar adı veya bitiş noktası yalnızca \*.commerce.dynamics.com için bir SSL sertifikasını destekliyor.</span><span class="sxs-lookup"><span data-stu-id="dbd49-121">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="dbd49-122">Özel etki alanları için SSL'yi desteklemez.</span><span class="sxs-lookup"><span data-stu-id="dbd49-122">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="dbd49-123">CDN hizmetleri</span><span class="sxs-lookup"><span data-stu-id="dbd49-123">CDN services</span></span>

<span data-ttu-id="dbd49-124">Herhangi bir CDN hizmeti, bir Commerce ortamıyla kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="dbd49-124">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="dbd49-125">Burada iki örnek verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="dbd49-125">Here are two examples:</span></span>

- <span data-ttu-id="dbd49-126">**Microsoft Azure Ön kapı hizmeti** – Azure CDN çözümü.</span><span class="sxs-lookup"><span data-stu-id="dbd49-126">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="dbd49-127">Azure ön kapı hizmeti hakkında daha fazla bilgi için [Azure ön kapı hizmeti belgelerine](https://docs.microsoft.com/azure/frontdoor/) bakın.</span><span class="sxs-lookup"><span data-stu-id="dbd49-127">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="dbd49-128">**Akamai dinamik sitesi Hızlandırıcısı** – daha fazla bilgi için bkz. [Dinamik Site Hızlandırıcısı](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="dbd49-128">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="dbd49-129">CDN kurulumu</span><span class="sxs-lookup"><span data-stu-id="dbd49-129">CDN setup</span></span>

<span data-ttu-id="dbd49-130">CDN kurulum işlemi aşağıdaki adımlardan oluşur:</span><span class="sxs-lookup"><span data-stu-id="dbd49-130">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="dbd49-131">Ön uç ana bilgisayar ekleyin.</span><span class="sxs-lookup"><span data-stu-id="dbd49-131">Add a front-end host.</span></span>
1. <span data-ttu-id="dbd49-132">Bir arka uç havuzu yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="dbd49-132">Configure a backend pool.</span></span>
1. <span data-ttu-id="dbd49-133">Rota ve ön belleğe alma kurallarını ayarla.</span><span class="sxs-lookup"><span data-stu-id="dbd49-133">Set up rules for routing and caching.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="dbd49-134">Ön uç ana bilgisayar ekleyin</span><span class="sxs-lookup"><span data-stu-id="dbd49-134">Add a front-end host</span></span>

<span data-ttu-id="dbd49-135">Tüm CDN hizmetleri kullanılabilir, ancak bu konudaki örnek için Azure ön kapı hizmeti kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dbd49-135">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="dbd49-136">Azure ön kapı hizmeti'ni kurma hakkında bilgi için bkz. [Hızlı başlangıç: yüksek oranda kullanılabilir bir Global Web uygulaması için ön kapı oluşturun.](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door)</span><span class="sxs-lookup"><span data-stu-id="dbd49-136">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a><span data-ttu-id="dbd49-137">Azure Front Door Service'te bir arka uç havuzu yapılandırın</span><span class="sxs-lookup"><span data-stu-id="dbd49-137">Configure a backend pool in Azure Front Door Service</span></span>

<span data-ttu-id="dbd49-138">Azure Front Door Service'te bir arka uç havuzu yapılandırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="dbd49-138">To configure a backend pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="dbd49-139">Arka uç havuzuna boş arka uç ana bilgisayar üst bilgisi olan özel bir ana bilgisayar olarak **&lt;ecom-kiraci-adi&gt;.commerce.dynamics.com** ekleyin.</span><span class="sxs-lookup"><span data-stu-id="dbd49-139">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a backend pool as a custom host that has an empty backend host header.</span></span>
1. <span data-ttu-id="dbd49-140">**Yük dengelemesi** altında, varsayılan değerleri bırakın.</span><span class="sxs-lookup"><span data-stu-id="dbd49-140">Under **Load balancing**, leave the default values.</span></span>

<span data-ttu-id="dbd49-141">Aşağıdaki resimde, Azure Front Door Service'te arka uç ana bilgisayar adı girilmiş halde **Bir arka uç ekle** iletişim kutusu gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="dbd49-141">The following illustration shows the **Add a backend** dialog box in Azure Front Door Service with the backend host name entered.</span></span>

![Arka uç havuzu iletişim kutusu Ekle](./media/CDN_BackendPool.png)

<span data-ttu-id="dbd49-143">Aşağıdaki resimde, Azure Front Door Service'te varsayılan yük dengeleme değerleriyle birlikte **Bir arka uç havuzu ekle** iletişim kutusu gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="dbd49-143">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service with the default load balancing values.</span></span>

![Arka uç havuzu iletişim kutusu ekle devamı](./media/CDN_BackendPool_2.png)

### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="dbd49-145">Azure ön kapı hizmeti'nde kuralları ayarla</span><span class="sxs-lookup"><span data-stu-id="dbd49-145">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="dbd49-146">Azure ön kapı hizmeti'nde bir yönlendirme kuralı ayarlamak için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="dbd49-146">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="dbd49-147">Rota kuralı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="dbd49-147">Add a routing rule.</span></span>
1. <span data-ttu-id="dbd49-148">**Ad** alanına, **varsayılan** yazın.</span><span class="sxs-lookup"><span data-stu-id="dbd49-148">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="dbd49-149">**Kabul edilen iletişim kuralı** alanında, **http ve https**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="dbd49-149">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="dbd49-150">**Ön uç ana bilgisayarlar** alanında, **dynamics-ecom-tenant-name.azurefd.net** girin.</span><span class="sxs-lookup"><span data-stu-id="dbd49-150">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="dbd49-151">**Eşleştirilecek desenler** altında, üst alana şunu girin: **/\***.</span><span class="sxs-lookup"><span data-stu-id="dbd49-151">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="dbd49-152">**Rota Ayrıntıları** altında, **rota türü** seçeneğini **ileri** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="dbd49-152">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="dbd49-153">**Arka uç havuzu** alanında, **ecom-arka uç**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="dbd49-153">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="dbd49-154">**İletme Protokolü** alan grubunda, **isteği eşleştir** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="dbd49-154">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="dbd49-155">**URL yeniden yazma** seçeneğini **devre dışı** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="dbd49-155">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="dbd49-156">**Önbelleğe alma** seçeneğini **devre dışı** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="dbd49-156">Set the **Caching** option to **Disabled**.</span></span>

<span data-ttu-id="dbd49-157">Azure ön kapı hizmeti'nde bir önbelleğe alma kuralı ayarlamak için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="dbd49-157">To set up a caching rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="dbd49-158">Önbelleğe alma kuralı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="dbd49-158">Add a caching rule.</span></span>
1. <span data-ttu-id="dbd49-159">**Ad** alanına, **statikler** yazın.</span><span class="sxs-lookup"><span data-stu-id="dbd49-159">In the **Name** field, enter **statics**.</span></span>
1. <span data-ttu-id="dbd49-160">**Kabul edilen iletişim kuralı** alanında, **http ve https**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="dbd49-160">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="dbd49-161">**Ön uç ana bilgisayarlar** alanında, **dynamics-ecom-tenant-name.azurefd.net** girin.</span><span class="sxs-lookup"><span data-stu-id="dbd49-161">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="dbd49-162">**Eşleştirilecek desenler** altında, üst alana şunu girin: **/\_msdyn365/\_scnr/\***.</span><span class="sxs-lookup"><span data-stu-id="dbd49-162">Under **Patterns to match**, in the upper field, **/\_msdyn365/\_scnr/\***.</span></span>
1. <span data-ttu-id="dbd49-163">**Rota Ayrıntıları** altında, **rota türü** seçeneğini **ileri** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="dbd49-163">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="dbd49-164">**Arka uç havuzu** alanında, **ecom-arka uç**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="dbd49-164">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="dbd49-165">**İletme Protokolü** alan grubunda, **isteği eşleştir** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="dbd49-165">In the **Forwarding protocol** field group, select the **Match request** option.</span></span>
1. <span data-ttu-id="dbd49-166">**URL yeniden yazma** seçeneğini **devre dışı** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="dbd49-166">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="dbd49-167">**Önbelleğe alma** seçeneğini **devre dışı** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="dbd49-167">Set the **Caching** option to **Disabled**.</span></span>
1. <span data-ttu-id="dbd49-168">**Sorgu dizesi önbelleğe alma davranışı** alanında, **her benzersiz URL 'yi önbelleğe al** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="dbd49-168">In the **Query string caching behavior** field, select **Cache every unique URL**.</span></span>
1. <span data-ttu-id="dbd49-169">**Dinamik sıkıştırma** alan grubunda, **etkin** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="dbd49-169">In the **Dynamic compression** field group, select the **Enabled** option.</span></span>

<span data-ttu-id="dbd49-170">Aşağıdaki resimde, Azure ön kapı hizmeti'ndeki **bir kural Ekle** iletişim kutusu gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="dbd49-170">The following illustration shows the **Add a rule** dialog box in Azure Front Door Service.</span></span>

![Kural Ekle iletişim kutusu](./media/CDN_CachingRule.png)

> [!WARNING]
> <span data-ttu-id="dbd49-172">Kullanacağınız etki alanı zaten etkin ve yayında ise, sonraki adımlarınız için yardım almak üzere, [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/)'teki **Destek** kutucuğunda bir destek bileti oluşturun.</span><span class="sxs-lookup"><span data-stu-id="dbd49-172">If the domain that you will use is already active and live, create a support ticket from the **Support** tile in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) to get assistance for your next steps.</span></span> <span data-ttu-id="dbd49-173">Daha fazla bilgi için bkz. [Finance and Operations uygulamaları veya Lifecycle Services (LCS) için destek alma](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="dbd49-173">For more information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

<span data-ttu-id="dbd49-174">Etki alanınız yeniyse ve önceden varolan yayındaki bir etki alanı değilse, özel etki alanınızı Azure Front Door Service yapılandırmasına ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dbd49-174">If your domain is new and is not a pre-existing live domain, you can add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="dbd49-175">Bu, Azure Front Door örneği aracılığıyla web trafiğini sitenize yönlendirmeyi sağlar.</span><span class="sxs-lookup"><span data-stu-id="dbd49-175">This will enable web traffic to direct to your site via the Azure Front Door instance.</span></span> <span data-ttu-id="dbd49-176">Özel etki alanı eklemek için (örneğin `www.fabrikam.com`), etki alanı için kurallı bir ad (CNAME) yapılandırmalısınız.</span><span class="sxs-lookup"><span data-stu-id="dbd49-176">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="dbd49-177">Aşağıdaki resimde, Azure ön kapı hizmeti'ndeki **CNAME yapılandırması** iletişim kutusu gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="dbd49-177">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![CNAME Konfigürasyon iletişim kutusu](./media/CNAME_Configuration.png)

<span data-ttu-id="dbd49-179">Sertifikayı yönetmek için Azure ön kapı hizmetini kullanabilir veya özel etki alanı için kendi sertifikanızı kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dbd49-179">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="dbd49-180">Aşağıdaki resimde, Azure ön kapı hizmeti'ndeki **Özel alan HTTPS** iletişim kutusu gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="dbd49-180">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![Özel etki alanı HTTPS iletişim kutusu](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="dbd49-182">Azure Front Door'unuza özel etki alanı eklemeyle ilgili ayrıntılı yönergeler için bkz. [Front Door'a özel etki alanı ekleme](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span><span class="sxs-lookup"><span data-stu-id="dbd49-182">For detailed instructions on adding a custom domain to your Azure Front Door, see [Add a custom domain to your Front Door](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span></span>

<span data-ttu-id="dbd49-183">CDN'niz şimdi Commerce sitenizde kullanılabilecek şekilde doğru konfigüre edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="dbd49-183">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dbd49-184">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="dbd49-184">Additional resources</span></span>

[<span data-ttu-id="dbd49-185">İçerik teslimi ağı uygulama seçenekleri</span><span class="sxs-lookup"><span data-stu-id="dbd49-185">Content delivery network implementation options</span></span>](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
